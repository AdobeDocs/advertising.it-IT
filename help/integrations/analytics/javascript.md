---
title: Codice JavaScript per [!DNL Analytics for Advertising]
description: Codice JavaScript per [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 18bfb32d-2754-44b2-86c1-d102836cc08c
source-git-commit: 8689bc2b5532b0e75ebf3cee14a42fa733d5ded5
workflow-type: tm+mt
source-wordcount: '939'
ht-degree: 0%

---

# Codice JavaScript per [!DNL Analytics for Advertising]

*Per gli inserzionisti con una sola integrazione Adobi Advertising-Adobe Analytics*

*Inserzionisti solo con Advertising DSP*

Per Advertising DSP, il [!DNL Analytics for Advertising] l’integrazione tiene traccia delle interazioni del sito view-through e click-through. Le visite click-through vengono tracciate dal codice Adobe Analytics standard sulle tue pagine web; il [!DNL Analytics] Il codice acquisisce i parametri AMO ID e EF ID nell’URL della pagina di destinazione e li tiene traccia nelle rispettive eVar riservate. Puoi tenere traccia delle visite view-through distribuendo uno snippet JavaScript nelle pagine web.

Nella visualizzazione della prima pagina di una visita al sito, il codice JavaScript di Adobe Advertising controlla se il visitatore ha già visto o fatto clic su un annuncio. Se l’utente è già entrato nel sito tramite un click-through o non ha visto un annuncio, il visitatore viene ignorato. Se il visitatore ha visto un annuncio e non è entrato nel sito tramite un click-through durante il [fai clic sull’intervallo di lookback](/help/integrations/analytics/prerequisites.md#lookback-a4adc) impostato in Adobi Advertising, il codice JavaScript di Adobe Advertising a) utilizza [Servizio ID Experience Cloud](https://experienceleague.adobe.com/docs/id-service/using/home.html) per generare un ID supplementare (`SDID`a) o b) utilizza il Adobe Experience Platform [!DNL Web SDK] `generateRandomID` metodo per generare un `[!DNL StitchID]`. Entrambi gli ID vengono utilizzati per unire i dati da Adobi Advertising all’hit di Adobe Analytics del visitatore. Adobe Analytics quindi richiede all’Adobe Advertising l’AMO ID e l’EF ID associati all’esposizione dell’annuncio. Gli AMO ID e gli EF ID vengono quindi compilati nelle rispettive eVar. Questi valori persistono per un periodo designato (per impostazione predefinita, 60 giorni).

[!DNL Analytics] invia metriche del traffico del sito (come visualizzazioni di pagina, visite e tempo trascorso) e qualsiasi [!DNL Analytics] eventi personalizzati o standard per l’Adobe Advertising su base oraria, utilizzando l’ID EF come chiave. Questi [!DNL Analytics] Le metriche vengono quindi eseguite attraverso il sistema di attribuzione Adobi Advertising per collegare le conversioni alla cronologia dei clic e dell’esposizione.

>[!NOTE]
>
>La logica di tracciamento JavaScript di Adobe Advertising si trova sul lato Adobe e quindi non ha virtualmente alcun impatto sul tempo di caricamento della pagina.
>
>Al contrario, la logica [!DNL DCM] connettore dati a [!DNL Analytics] (utilizzando [!DNL Google Campaign Manager 360]) per Advertising DSP si verifica sul lato client. L’unione lato client rallenta il caricamento della pagina e aumenta il rischio di perdita di dati. Ciò si verifica perché [!DNL Analytics] JavaScript deve eseguire il ping [!DNL DoubleClick] e attendi [!DNL DoubleClick] per restituire i dati dell’ultimo clic/impression a [!DNL Analytics]. Quando [!DNL DSP] il team configura [!DNL DCM] connettore dati, è necessario specificare per quanto tempo si è disposti a ritardare la pagina.

## Distribuzione del codice JavaScript

La libreria JavaScript è costituita da due righe che consentono [!DNL Analytics] e Adobi Advertising per comunicare tra loro. Se il [!DNL Analytics for Advertising] l&#39;integrazione è stata completata durante l&#39;implementazione di Adobi Advertising, quindi dovresti aver già ricevuto questo codice con le istruzioni su come distribuirlo.

### Il codice

#### Implementazioni che utilizzano il servizio Experience Cloud Identity `visitorAPI.js` codice

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id','rsid');
</script>
```

#### Implementazioni che utilizzano l’Experience Platform [!DNL Web SDK] `alloy.js`codice

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id','rsid').generateRandomId();
</script>
```

### Dove inserire il codice

Il [!DNL Analytics for Advertising] La funzione JavaScript deve trovarsi dopo il servizio ID Experience Cloud ma prima del codice App Measurement di Analytics. In questo modo l’ID supplementare (`SDID`) o `[!DNL StitchID]` è incluso nella chiamata di Analytics.

![Posizionamento del codice](/help/integrations/assets/a4adc-code-placement.png)

### Convalida distribuzione codice

Puoi eseguire la convalida utilizzando qualsiasi tipo di strumento packet sniffer (ad esempio [!DNL Charles], [!DNL Fiddler], o [!DNL Chrome Developer Tools]) confrontando i valori dei quattro ID tra la richiesta in Adobe Advertising e la richiesta in [!DNL Analytics], come illustrato di seguito.

#### Come confermare il codice con [!DNL Chrome Developer Tools] {#validate-js-chrome}

1. Apri [!DNL Chrome Developer Tools] e fai clic su **Rete** scheda.

1. Carica una pagina del sito Web che contiene [!DNL Analytics for Advertising] JavaScript.

1. Filtra il [!UICONTROL Network] scheda per `last` e rivedi due righe:

   ![Filtraggio sull’ultimo](/help/integrations/assets/a4adc-code-validation-filter-last.png)

   * La prima riga è la chiamata alla libreria JavaScript e ha il titolo `last-event-tag-latest.min.js`.
   * La seconda riga è la chiamata che invia la richiesta all’Adobe Advertising. Esso inizia come segue: `_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]`

     Se non vedi la chiamata all’Adobe Advertising, potrebbe non essere la prima visualizzazione pagina della tua visita. A scopo di test, puoi rimuovere il cookie in modo che la chiamata successiva sia la prima visualizzazione di pagina per la visita corrispondente:

   1. Nella scheda Applicazione, individua `adcloud` cookie e verifica che il cookie contenga `_les_v` (ultima visita) con valore `y` e una marca temporale UTC che scade tra 30 minuti.
      1. Elimina `ad cloud` e aggiorna la pagina.

1. (Implementazioni che utilizzano il servizio Experience Cloud Identity) `visitorAPI.js` code) Filter on `/b/ss` per visualizzare l’hit di Analytics.

   ![Filtro attivato `/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)

1. (Implementazioni che utilizzano l’Experience Platform [!DNL Web SDK] `alloy.js`code) Filter on `/interact` per verificare che il payload della richiesta alla rete Edge contenga `advertisingStitchID`.

   ![Filtro attivato `/interact`](/help/integrations/assets/a4adc-code-validation-filter-interact.png)

1. Confronta i valori ID tra i due risultati. Tutti i valori si troveranno nei parametri della stringa di query, ad eccezione dell’ID suite di rapporti nell’hit di Analytics, che è il percorso URL immediatamente dopo `/b/ss/`.

   | ID | Parametro di Analytics | Rete Edge | Parametro Adobi Advertising |
   | --- | --- | --- | --- |
   | Organizzazione IMS di Experience Cloud | `mcorgid` |  | `_les_imsOrgid` |
   | ID dati supplementari | sdid |  | `_les_sdid` |
   | ID unione | stitchId | `advertisingStitchID` sotto `_adcloud` proprietà |  |
   | Suite di rapporti di Analytics | Il valore dopo `/b/ss/` | | `_les_rsid` |
   | ID visitatore Experience Cloud | mid |  | `_les_mid` |

   Se i valori ID corrispondono, viene confermata l’implementazione JavaScript. L’Adobe Advertising invierà il [!DNL Analytics] server qualsiasi dettaglio di tracciamento click-through o view-through, se presente.

#### Come confermare il codice con [!DNL Adobe Experience Cloud Debugger]

1. Apri [[!DNL Adobe Experience Cloud Debugger]](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html) nella tua home page.
1. Vai a [!UICONTROL Network] scheda.
1. In [!UICONTROL Solutions Filter] barra degli strumenti, fai clic su [!UICONTROL Adobe Advertising] e [!UICONTROL Analytics].
1. In [!UICONTROL Request URL – Hostname] riga parametro, individua `lasteventf-tm.everesttech.net`.
1. In [!UICONTROL Request – Parameters] riga, controlla i segnali generati, in modo simile al passaggio 3 in &quot;[Come confermare il codice con [!DNL Chrome Developer Tools]](#validate-js-chrome).&quot;
   * (Implementazioni che utilizzano il servizio Experience Cloud Identity) `visitorAPI.js` code) Accertarsi che il `Sdid` il parametro corrisponde al `Supplemental Data ID` nel filtro Adobe Analytics.
   * (Implementazioni che utilizzano l’Experience Platform [!DNL Web SDK] `alloy.js`code) Assicurati che il valore della proprietà `advertisingStitchID` il parametro corrisponde al `Sdid` inviato a Experienci Platform Edge Network.
   * Se il codice non viene generato, assicurati che il cookie di Adobe Advertising sia stato rimosso in [!UICONTROL Application] scheda. Una volta rimossa, aggiorna la pagina e ripeti la procedura.

   ![Controllo [!DNL Analytics for Advertising] Codice JavaScript in [!DNL Experience Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)

>[!MORELIKETHIS]
>
>* [Panoramica di [!DNL Analytics for Advertising]](overview.md)
>* [Prerequisiti e informazioni chiave per l’implementazione [!DNL Analytics for Advertising]](prerequisites.md)
