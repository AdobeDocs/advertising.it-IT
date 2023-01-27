---
title: Codice JavaScript per [!DNL Analytics for Advertising]
description: Codice JavaScript per [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 18bfb32d-2754-44b2-86c1-d102836cc08c
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '939'
ht-degree: 0%

---

# Codice JavaScript per [!DNL Analytics for Advertising]

*Inserzionisti con una sola integrazione Advertising-Adobe Analytics di Adobe*

*Advertising DSP solo*

Per la DSP pubblicitaria, il [!DNL Analytics for Advertising] l&#39;integrazione traccia le interazioni del sito in modalità di visualizzazione e click-through. Le visite Click-through sono tracciate dal codice Adobe Analytics standard sulle tue pagine web; la [!DNL Analytics] Il codice acquisisce i parametri AMO ID e EF ID nell’URL della pagina di destinazione e li tiene traccia nelle rispettive eVar riservate. Puoi tenere traccia delle visite view-through distribuendo uno snippet JavaScript nelle tue pagine web.

Nella visualizzazione della prima pagina di una visita al sito, il codice JavaScript di pubblicità Adobe controlla se il visitatore ha già visto o fatto clic su un annuncio. Se l&#39;utente è entrato in precedenza nel sito tramite un click-through o non ha visto un annuncio, il visitatore viene ignorato. Se il visitatore ha visto un annuncio e non è entrato nel sito tramite un click-through durante il [finestra di lookback su clic](/help/integrations/analytics/prerequisites.md#lookback-a4adc) impostato in Adobe Advertising, il codice JavaScript di Adobe Advertising a) utilizza il [Servizio Experience Cloud ID](https://experienceleague.adobe.com/docs/id-service/using/home.html) per generare un ID supplementare (`SDID`) o b) utilizza Adobe Experience Platform [!DNL Web SDK] `generateRandomID` per generare un `[!DNL StitchID]`. Entrambi gli ID vengono utilizzati per unire i dati da Adobe Advertising all’hit Adobe Analytics del visitatore. Adobe Analytics invia quindi una query ad Adobe Advertising per l’AMO ID e l’EF ID associati all’esposizione dell’annuncio. Gli ID AMO e EF vengono quindi compilati nei rispettivi eVar. Questi valori persistono per un determinato periodo (per impostazione predefinita, 60 giorni).

[!DNL Analytics] invia metriche del traffico del sito (come visualizzazioni di pagina, visite e tempo trascorso) ed eventuali [!DNL Analytics] eventi personalizzati o standard per Adobe Advertising ogni ora, utilizzando l’ID EF come chiave. Tali [!DNL Analytics] le metriche vengono quindi eseguite attraverso il sistema di attribuzione Adobe Advertising per collegare le conversioni alla cronologia dei clic e delle esposizioni.

>[!NOTE]
>
>La logica di tracciamento JavaScript per la pubblicità di Adobe si verifica sul lato Adobe e quindi non ha alcun impatto sul tempo di caricamento della pagina.
>
>Al contrario, la logica per [!DNL DCM] connettore dati a [!DNL Analytics] (utilizzando [!DNL Google Campaign Manager 360]) per Advertising DSP si verifica sul lato client. L’unione lato client rallenta il caricamento della pagina e aumenta il rischio di perdita di dati. Ciò si verifica perché la [!DNL Analytics] JavaScript deve eseguire il ping [!DNL DoubleClick] e attendere [!DNL DoubleClick] per restituire i dati dell’ultimo clic/impression a [!DNL Analytics]. Quando il [!DNL DSP] il team [!DNL DCM] connettore dati, è necessario specificare per quanto tempo si desidera ritardare la pagina.

## Distribuzione del codice JavaScript

La libreria JavaScript è costituita da due righe che consentono [!DNL Analytics] e Adobe Advertising per comunicare tra di loro. Se la [!DNL Analytics for Advertising] L&#39;integrazione è stata completata durante l&#39;implementazione di Adobe Advertising, quindi dovresti aver già ricevuto questo codice con istruzioni su come distribuirlo.

### Il codice

#### Implementazioni che utilizzano il servizio Experience Cloud Identity `visitorAPI.js` codice

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id');
</script>
```

#### Implementazioni che utilizzano l’Experience Platform [!DNL Web SDK] `alloy.js`codice

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id').generateRandomId();
</script>
```

### Dove inserire il codice

La [!DNL Analytics for Advertising] La funzione JavaScript deve avvenire dopo il servizio Experience Cloud ID ma prima del codice di misurazione app di Analytics in modo che l&#39;ID supplementare (`SDID`) o `[!DNL StitchID]` può essere incluso nella chiamata di Analytics.

![Posizionamento del codice](/help/integrations/assets/a4adc-code-placement.png)

### Convalida della distribuzione del codice

È possibile eseguire la convalida utilizzando qualsiasi tipo di strumento packet sniffer (ad esempio [!DNL Charles], [!DNL Fiddler]oppure [!DNL Chrome Developer Tools]) confrontando i valori dei quattro ID tra la richiesta indirizzata ad Adobe Advertising e la richiesta indirizzata a [!DNL Analytics], come illustrato di seguito.

#### Come confermare il codice con [!DNL Chrome Developer Tools] {#validate-js-chrome}

1. Apri [!DNL Chrome Developer Tools] e fai clic su **Rete** scheda .

1. Carica una pagina web che contiene [!DNL Analytics for Advertising] JavaScript.

1. Filtrare [!UICONTROL Network] scheda per `last` e controlla due righe:

   ![Filtraggio per ultimo](/help/integrations/assets/a4adc-code-validation-filter-last.png)

   * La prima riga è la chiamata alla libreria JavaScript e ha titolo `last-event-tag-latest.min.js`.
   * La seconda riga è la chiamata che invia la richiesta ad Adobe Advertising. Inizia come segue: `_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]`

      Se non trovi la chiamata ad Adobe Advertising, potrebbe non essere la prima visualizzazione di pagina della visita. A scopo di test, puoi rimuovere il cookie in modo che la chiamata successiva sia la prima visualizzazione di pagina per la visita corrispondente:
   1. Nella scheda Applicazione , individua il `adcloud` e verifica che il cookie contenga `_les_v` (ultima visita) con un valore di `y` e una marca temporale UTC che scade in 30 minuti.
      1. Elimina `ad cloud` cookie e aggiorna la pagina.


1. Implementazioni che utilizzano il servizio Experience Cloud Identity `visitorAPI.js` codice) Filtro su `/b/ss` per visualizzare l’hit di Analytics.

   ![Filtro su `/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)

1. (Implementazioni che utilizzano l’Experience Platform [!DNL Web SDK] `alloy.js`codice) Filtro su `/interact` per verificare che il payload della richiesta alla rete Edge contenga `advertisingStitchID`.

   ![Filtro su `/interact`](/help/integrations/assets/a4adc-code-validation-filter-interact.png)

1. Confronta i valori ID tra i due risultati. Tutti i valori saranno nei parametri della stringa di query ad eccezione dell&#39;ID della suite di rapporti nell&#39;hit Analytics, che è il percorso URL immediatamente dopo `/b/ss/`.

   | ID | Parametro di Analytics | Rete Edge | Parametro della pubblicità di Adobe |
   | --- | --- | --- | --- |
   | Organizzazione Experience Cloud IMS | `mcorgid` |  | `_les_imsOrgid` |
   | ID dati supplementari | sciocco |  | `_les_sdid` |
   | ID punto | stitchId | `advertisingStitchID` in `_adcloud` property |  |
   | Suite di rapporti di Analytics | Il valore dopo `/b/ss/` |  | `_les_rsid` |
   | ID visitatore Experience Cloud | mid |  | `_les_mid` |

   Se i valori ID corrispondono, l&#39;implementazione JavaScript viene confermata. Adobe Advertising invierà il [!DNL Analytics] eventuali dettagli di tracciamento click-through o view-through presenti nel server.

#### Come confermare il codice con [!DNL Adobe Experience Cloud Debugger]

1. Apri [[!DNL Adobe Experience Cloud Debugger]](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html) sulla tua homepage.
1. Vai a [!UICONTROL Network] scheda .
1. In [!UICONTROL Solutions Filter] barra degli strumenti, fai clic su [!UICONTROL Adobe Advertising] e [!UICONTROL Analytics].
1. In [!UICONTROL Request URL – Hostname] riga parametro, individuare `lasteventf-tm.everesttech.net`.
1. In [!UICONTROL Request – Parameters] riga, controlla i segnali generati, in modo simile al passaggio 3 in &quot;[Come confermare il codice con [!DNL Chrome Developer Tools]](#validate-js-chrome).&quot;
   * Implementazioni che utilizzano il servizio Experience Cloud Identity `visitorAPI.js` codice) Assicurati che il `Sdid` corrisponde al `Supplemental Data ID` nel filtro Adobe Analytics.
   * (Implementazioni che utilizzano l’Experience Platform [!DNL Web SDK] `alloy.js`codice) Assicurati che il valore del `advertisingStitchID` corrisponde al `Sdid` inviato ad Experience Platform Edge Network.
   * Se il codice non genera, controlla che il cookie Adobe Advertising sia stato rimosso nella sezione [!UICONTROL Application] scheda . Una volta rimosso, aggiorna la pagina e ripeti il processo.

   ![Controllo [!DNL Analytics for Advertising] Codice JavaScript in [!DNL Experience Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)

>[!MORELIKETHIS]
>
>* [Panoramica [!DNL Analytics for Advertising]](overview.md)
>* [Prerequisiti e informazioni chiave per l’implementazione [!DNL Analytics for Advertising]](prerequisites.md)

