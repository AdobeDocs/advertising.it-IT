---
title: Codice JavaScript per  [!DNL Analytics for Advertising]
description: Codice JavaScript per  [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 18bfb32d-2754-44b2-86c1-d102836cc08c
source-git-commit: 5d07300ab49b96daf392cb51f8936fa4c0cd20ce
workflow-type: tm+mt
source-wordcount: '919'
ht-degree: 0%

---

# Codice JavaScript per [!DNL Analytics for Advertising]

*Inserzionisti con solo Advertising DSP*

Per Advertising DSP, l&#39;integrazione di [!DNL Analytics for Advertising] tiene traccia delle interazioni del sito view-through e click-through. Le visite click-through vengono tracciate dal codice Adobe Analytics standard sulle tue pagine web; il codice [!DNL Analytics] acquisisce i parametri AMO ID e EF ID nell’URL della pagina di destinazione e li tiene traccia nelle rispettive [!DNL eVars] riservate. Puoi tenere traccia delle visite view-through distribuendo uno snippet di JavaScript nelle pagine Web.

Nella visualizzazione della prima pagina di una visita al sito, il codice JavaScript dell’Adobe Advertising controlla se il visitatore ha già visto o fatto clic su un annuncio. Se l’utente è già entrato nel sito tramite un click-through o non ha visto un annuncio, il visitatore viene ignorato. Se il visitatore ha visualizzato un annuncio e non è entrato nel sito tramite un click-through durante l&#39;[intervallo di lookback su clic](/help/integrations/analytics/prerequisites.md#lookback-a4adc) impostato in Adobe Advertising, il codice JavaScript di Adobe Advertising a) utilizza il [servizio ID Experience Cloud](https://experienceleague.adobe.com/docs/id-service/using/home.html) per generare un ID supplementare (`SDID`) oppure b) utilizza il metodo Adobe Experience Platform [!DNL Web SDK] `generateRandomID` per generare un `[!DNL StitchID]`. Entrambi gli ID vengono utilizzati per unire i dati da Adobe Advertising all’hit di Adobe Analytics del visitatore. Adobe Analytics quindi richiede all’Adobe Advertising l’AMO ID e l’EF ID associati all’esposizione dell’annuncio. AMO ID e EF ID vengono quindi compilati nei rispettivi [!DNL eVars]. Questi valori persistono per un periodo designato (per impostazione predefinita, 60 giorni).

[!DNL Analytics] invia le metriche del traffico del sito (come visualizzazioni di pagina, visite e tempo trascorso) e qualsiasi evento standard o personalizzato [!DNL Analytics] a un Adobe Advertising orario, utilizzando l&#39;ID EF come chiave. Queste metriche [!DNL Analytics] vengono quindi eseguite attraverso il sistema di attribuzione Adobe Advertising per collegare le conversioni alla cronologia di clic e di esposizione.

>[!NOTE]
>
>La logica di tracciamento di Adobe Advertising JavaScript si trova sul lato Adobe e quindi non ha virtualmente alcun impatto sul tempo di caricamento della pagina.
>
>Al contrario, la logica per il connettore dati [!DNL DCM] in [!DNL Analytics] (utilizzando [!DNL Google Campaign Manager 360]) per Advertising DSP si verifica sul lato client. L’unione lato client rallenta il caricamento della pagina e aumenta il rischio di perdita di dati. Ciò si verifica perché il JavaScript [!DNL Analytics] deve eseguire il ping di [!DNL DoubleClick] e attendere che [!DNL DoubleClick] restituisca gli ultimi dati di clic/impression a [!DNL Analytics]. Quando il team [!DNL DSP] configura il connettore dati [!DNL DCM], è necessario specificare per quanto tempo si è disposti a ritardare la pagina.

<!--
## Deploying the JavaScript Code

All users must deploy the standard JavaScript code.

Users who want to convert first-party segments from their customer data platforms to [!DNL RampIDs] or [!DNL ID5] IDs [!!!!VERIFY that it's not needed for importing segments directly from LiveRamp] must also deploy ID partner-specific JavaScript code to match conversions to view-throughs.

### The Standard Code

The standard JavaScript library consists of two lines that allow [!DNL Analytics] and Adobe Advertising to communicate with each other. If the [!DNL Analytics for Advertising] integration was completed during the Adobe Advertising implementation, then you should have already received this code with instructions on how to deploy it.

#### Implementations that use the Experience Cloud Identity Service `visitorAPI.js` code

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id','rsid');
</script>
```

#### Implementations that use the Experience Platform [!DNL Web SDK] `alloy.js`code

### Additional Code to Import First-Party Segments to [!DNL RampIDs] and [!DNL ID5] IDs

   * For [!DNL RampIDs], Contact your Adobe Account Team, who will give you instructions to register for a [!DNL LiveRamp] [!DNL LaunchPad] tag. Registration is free, but you must sign an agreement. Once you register, your Adobe Account Team will generate and provide a unique tag for your organization to implement on your webpages.

    [MAYBE PUT THIS BELOW] Place the [!DNL LaunchPad] tag on every page of your website, preferably as the first script within the page head tags but as high within the page head tags as possible.

   * For [!DNL ID5] IDs: Contact your Adobe Account Team, who will give you instructions to register for the tag with ID5. Registration is free, but you must sign an agreement. Once you register, a member of ID5’s technical team will provide a unique tag for your organization to implement on your webpages.
-->

## Distribuzione del codice JavaScript

La libreria JavaScript è costituita da due righe che consentono a [!DNL Analytics] e Adobe Advertising di comunicare tra loro. Se l&#39;integrazione di [!DNL Analytics for Advertising] è stata completata durante l&#39;implementazione di Adobe Advertising, questo codice dovrebbe essere già stato ricevuto con istruzioni su come distribuirlo.

### Il codice

#### Implementazioni che utilizzano il codice `visitorAPI.js` del servizio Experience Cloud Identity

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id','rsid');
</script>
```

#### Implementazioni che utilizzano il codice `alloy.js` di Experience Platform[!DNL Web SDK]

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id','rsid').generateRandomId();
</script>
```

### Dove inserire il codice

La funzione JavaScript [!DNL Analytics for Advertising] deve trovarsi dopo il servizio ID Experience Cloud ma prima del codice App Measurement di Analytics. In questo modo l&#39;ID supplementare (`SDID`) o `[!DNL StitchID]` sarà incluso nella chiamata Analytics.

![Inserimento codice](/help/integrations/assets/a4adc-code-placement.png)

### Convalida distribuzione codice

È possibile eseguire la convalida utilizzando qualsiasi tipo di strumento packet sniffer (ad esempio [!DNL Charles], [!DNL Fiddler] o [!DNL Chrome Developer Tools]) confrontando i valori dei quattro ID tra la richiesta in Adobe Advertising e la richiesta in [!DNL Analytics], come descritto di seguito.

#### Come confermare il codice con [!DNL Chrome Developer Tools] {#validate-js-chrome}

1. Apri [!DNL Chrome Developer Tools] e fai clic sulla scheda **Rete**.

1. Caricare una pagina del sito Web che contiene il JavaScript [!DNL Analytics for Advertising].

1. Filtra la scheda [!UICONTROL Network] per `last` e controlla due righe:

   ![Filtro sull&#39;ultimo](/help/integrations/assets/a4adc-code-validation-filter-last.png)

   * La prima riga è la chiamata alla libreria JavaScript e si chiama `last-event-tag-latest.min.js`.
   * La seconda riga è la chiamata che invia la richiesta all’Adobe Advertising. Inizia come segue: `_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]`

     Se non vedi la chiamata all’Adobe Advertising, potrebbe non essere la prima visualizzazione pagina della tua visita. A scopo di test, puoi rimuovere il cookie in modo che la chiamata successiva sia la prima visualizzazione di pagina per la visita corrispondente:

   1. Nella scheda Applicazione, individua il cookie `adcloud` e verifica che il cookie contenga `_les_v` (ultima visita) con un valore di `y` e una marca temporale dell&#39;epoca UTC che scade tra 30 minuti.
      1. Elimina il cookie `adcloud` e aggiorna la pagina.

1. (implementazioni che utilizzano il codice `visitorAPI.js` del servizio Experience Cloud Identity ) Filtra su `/b/ss` per visualizzare l&#39;hit di Analytics.

   ![Filtro su `/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)

1. (Implementazioni che utilizzano il codice `alloy.js` dell&#39;Experience Platform [!DNL Web SDK]) Filtro su `/interact` per verificare che il payload della richiesta all&#39;Edge Network contenga `advertisingStitchID`.

   ![Filtro su `/interact`](/help/integrations/assets/a4adc-code-validation-filter-interact.png)

1. Confronta i valori ID tra i due risultati. Tutti i valori devono trovarsi nei parametri della stringa di query ad eccezione dell&#39;ID suite di rapporti nell&#39;hit di Analytics, che è il percorso URL immediatamente dopo `/b/ss/`.

   | ID | Parametro di Analytics | Edge Network | Parametro Adobe Advertising |
   | --- | --- | --- | --- |
   | Organizzazione IMS di Experience Cloud | `mcorgid` |  | `_les_imsOrgid` |
   | ID dati supplementari | sdid |  | `_les_sdid` |
   | ID unione | stitchId | `advertisingStitchID` sotto la proprietà `_adcloud` |  |
   | Suite di rapporti di Analytics | Il valore dopo `/b/ss/` | | `_les_rsid` |
   | ID visitatore Experience Cloud | mid |  | `_les_mid` |

   Se i valori ID corrispondono, viene confermata l’implementazione di JavaScript. L&#39;Adobe Advertising invia al server [!DNL Analytics] qualsiasi dettaglio di tracciamento click-through o view-through, se presente.

#### Come confermare il codice con [!DNL Adobe Experience Cloud Debugger]

1. Apri [[!DNL Adobe Experience Cloud Debugger]](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html) nella tua home page.
1. Passa alla scheda [!UICONTROL Network].
1. Nella barra degli strumenti di [!UICONTROL Solutions Filter], fare clic su [!UICONTROL Adobe Advertising] e [!UICONTROL Analytics].
1. Nella riga del parametro [!UICONTROL Request URL - Hostname], individuare `lasteventf-tm.everesttech.net`.
1. Nella riga [!UICONTROL Request - Parameters], controlla i segnali generati, in modo simile al passaggio 3 in &quot;[Come confermare il codice con [!DNL Chrome Developer Tools]](#validate-js-chrome)&quot;.
   * (Implementazioni che utilizzano il codice `visitorAPI.js` di Experience Cloud Identity Service) Verifica che il parametro `Sdid` corrisponda al `Supplemental Data ID` nel filtro di Adobe Analytics.
   * (Implementazioni che utilizzano il codice `alloy.js` dell&#39;Experience Platform [!DNL Web SDK]) Verificare che il valore del parametro `advertisingStitchID` corrisponda al `Sdid` inviato all&#39;Edge Network dell&#39;Experience Platform.
   * Se il codice non viene generato, verificare che il cookie Adobe Advertising sia stato rimosso nella scheda [!UICONTROL Application]. Una volta rimossa, aggiorna la pagina e ripeti la procedura.

   ![Controllo del codice JavaScript di [!DNL Analytics for Advertising] in [!DNL Experience Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)

>[!MORELIKETHIS]
>
>* [Panoramica di [!DNL Analytics for Advertising]](overview.md)
>* [Prerequisiti e informazioni chiave per l&#39;implementazione [!DNL Analytics for Advertising]](prerequisites.md)
