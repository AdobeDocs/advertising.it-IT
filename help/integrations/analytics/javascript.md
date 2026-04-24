---
title: Codice JavaScript per  [!DNL Analytics for Advertising]
description: Codice JavaScript per  [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 18bfb32d-2754-44b2-86c1-d102836cc08c
TQID: https://experienceleague.adobe.com/g9onwe1IQl1kbyQ82W2KmODPGUAReKiotxy65yCZcNY
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 941
ht-degree: 0%

---

# Codice JavaScript per [!DNL Analytics for Advertising]

*Inserzionisti con solo Advertising DSP*

Per Advertising DSP, l&#39;integrazione di [!DNL Analytics for Advertising] tiene traccia delle interazioni del sito view-through e click-through. Le visite click-through vengono tracciate dal codice Adobe Analytics standard sulle tue pagine web; il codice [!DNL Analytics] acquisisce i parametri AMO ID e EF ID nell’URL della pagina di destinazione e li tiene traccia nelle rispettive [!DNL eVars] riservate. Puoi tenere traccia delle visite view-through distribuendo uno snippet di JavaScript nelle pagine Web.

Nella visualizzazione della prima pagina di una visita al sito, il codice JavaScript di Adobe Advertising controlla se il visitatore ha già visto o fatto clic su un annuncio. Se l’utente è già entrato nel sito tramite un click-through o non ha visto un annuncio, il visitatore viene ignorato. Se il visitatore ha visualizzato un annuncio e non è entrato nel sito tramite un click-through durante l&#39;[intervallo di lookback su clic](/help/integrations/analytics/prerequisites.md#lookback-a4adc) impostato in Adobe Advertising, il codice JavaScript di Adobe Advertising a) utilizza il [servizio Experience Cloud ID](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=it) per generare un ID supplementare (`SDID`) oppure b) utilizza il metodo Adobe Experience Platform [!DNL Web SDK] `generateRandomID` per generare un `[!DNL StitchID]`. Entrambi gli ID vengono utilizzati per unire i dati da Adobe Advertising all’hit di Adobe Analytics del visitatore. Adobe Analytics quindi richiede ad Adobe Advertising l’AMO ID e l’EF ID associati all’esposizione dell’annuncio. AMO ID e EF ID vengono quindi compilati nei rispettivi [!DNL eVars]. Questi valori persistono per un periodo designato (per impostazione predefinita, 60 giorni).

[!DNL Analytics] invia metriche del traffico del sito (come visualizzazioni di pagina, visite e tempo trascorso) e qualsiasi evento standard o personalizzato [!DNL Analytics] ad Adobe Advertising ogni ora, utilizzando l&#39;ID EF come chiave. Queste metriche [!DNL Analytics] vengono quindi eseguite tramite il sistema di attribuzione Adobe Advertising per collegare le conversioni alla cronologia di clic e di esposizione.

>[!NOTE]
>
>La logica di tracciamento di Adobe Advertising JavaScript si trova sul lato Adobe e quindi non ha virtualmente alcun impatto sul tempo di caricamento della pagina.
>
>Al contrario, la logica per il connettore dati [!DNL DCM] in [!DNL Analytics] (utilizzando [!DNL Google Campaign Manager 360]) per Advertising DSP si verifica sul lato client. L’unione lato client rallenta il caricamento della pagina e aumenta il rischio di perdita di dati. Ciò si verifica perché il JavaScript [!DNL Analytics] deve eseguire il ping di [!DNL DoubleClick] e attendere che [!DNL DoubleClick] restituisca gli ultimi dati di clic/impression a [!DNL Analytics]. Quando il team [!DNL DSP] configura il connettore dati [!DNL DCM], è necessario specificare per quanto tempo si è disposti a ritardare la pagina.

<!--
## Deploying the JavaScript code

All users must deploy the standard JavaScript code.

Users who want to convert first-party segments from their customer data platforms to [!DNL RampIDs] or [!DNL ID5] IDs [!!!!VERIFY that it's not needed for importing segments directly from LiveRamp] must also deploy ID partner-specific JavaScript code to match conversions to view-throughs.

### The standard code

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

### Additional code to import first-party segments to [!DNL RampIDs] and [!DNL ID5] IDs

   * For [!DNL RampIDs], Contact your Adobe Account Team, who will give you instructions to register for a [!DNL LiveRamp] [!DNL LaunchPad] tag. Registration is free, but you must sign an agreement. Once you register, your Adobe Account Team will generate and provide a unique tag for your organization to implement on your webpages.

    [MAYBE PUT THIS BELOW] Place the [!DNL LaunchPad] tag on every page of your website, preferably as the first script within the page head tags but as high within the page head tags as possible.

   * For [!DNL ID5] IDs: Contact your Adobe Account Team, who will give you instructions to register for the tag with ID5. Registration is free, but you must sign an agreement. Once you register, a member of ID5's technical team will provide a unique tag for your organization to implement on your webpages.
-->

## Distribuzione del codice JavaScript

La libreria JavaScript è costituita da due righe che consentono a [!DNL Analytics] e Adobe Advertising di comunicare tra loro. If the [!DNL Analytics for Advertising] integration was completed during the Adobe Advertising implementation, then you should have already received this code with instructions on how to deploy it.

### The code

#### Implementations that use the Experience Cloud Identity Service `visitorAPI.js` code

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id','rsid');
</script>
```

#### Implementations that use the Experience Platform [!DNL Web SDK] `alloy.js`code

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id','rsid').generateRandomId();
</script>
```

### Where to place the code

The [!DNL Analytics for Advertising] JavaScript function must come after the Experience Cloud ID Service but before your Analytics App Measurement code. This ensures that the supplemental ID (`SDID`) or `[!DNL StitchID]` is included in your Analytics call.

![Code placement](/help/integrations/assets/a4adc-code-placement.png)

### Validating code deployment

You can perform validation using any packet sniffer type of tool (such as [!DNL Charles], [!DNL Fiddler], or [!DNL Chrome Developer Tools]) by comparing the values of the four IDs between the request going to Adobe Advertising and the request going to [!DNL Analytics], as outlined below.

#### How to confirm the code with [!DNL Chrome Developer Tools] {#validate-js-chrome}

1. Open [!DNL Chrome Developer Tools] and click the **Network** tab.

1. Load a website page that contains the [!DNL Analytics for Advertising] JavaScript.

1. Filter the [!UICONTROL Network] tab by `last` and review two rows:

   ![Filtering on last](/help/integrations/assets/a4adc-code-validation-filter-last.png)

   * The first row is the call to the JavaScript library and is titled `last-event-tag-latest.min.js`.
   * The second row is the call sending the request to Adobe Advertising. It begins as follows: `_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]`

     If you don&#39;t see the call to Adobe Advertising, then it might not be the first page view of your visit. For testing purposes, you can remove the cookie so that the next call is the first page view for the corresponding visit:

   1. On the Application tab, find the `adcloud` cookie, and verify that the cookie contains `_les_v` (last visit) with a value of `y` and a UTC epoch timestamp that expires in 30 minutes.
      1. Delete the `adcloud` cookie and refresh the page.

1. (Implementations that use the Experience Cloud Identity Service `visitorAPI.js` code) Filter on `/b/ss` to see the Analytics hit.

   ![Filtering on `/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)

1. (Implementations that use the Experience Platform [!DNL Web SDK] `alloy.js`code) Filter on `/interact` to verify that the request payload to the Edge Network contains `advertisingStitchID`.

   ![Filtro su `/interact`](/help/integrations/assets/a4adc-code-validation-filter-interact.png)

1. Confronta i valori ID tra i due risultati. Tutti i valori devono trovarsi nei parametri della stringa di query ad eccezione dell&#39;ID suite di rapporti nell&#39;hit di Analytics, che è il percorso URL immediatamente dopo `/b/ss/`.

   | ID | Parametro di Analytics | Edge Network | Parametro Adobe Advertising |
   | --- | --- | --- | --- |
   | Organizzazione Experience Cloud IMS | `mcorgid` |  | `_les_imsOrgid` |
   | ID dati supplementari | sdid |  | `_les_sdid` |
   | ID unione | stitchId | `advertisingStitchID` sotto la proprietà `_adcloud` |  |
   | Suite di rapporti di Analytics | Il valore dopo `/b/ss/` | | `_les_rsid` |
   | ID visitatore Experience Cloud | mid |  | `_les_mid` |

   Se i valori ID corrispondono, viene confermata l’implementazione di JavaScript. Adobe Advertising invia al server [!DNL Analytics] qualsiasi dettaglio di tracciamento click-through o view-through, se presente.

#### Come confermare il codice con [!DNL Adobe Experience Platform Debugger]

1. Apri [the [!DNL Adobe Experience Platform Debugger]](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html?lang=it) nella tua home page.
1. Passa alla scheda [!UICONTROL Network].
1. Nella barra degli strumenti di [!UICONTROL Solutions Filter], fare clic su [!UICONTROL Adobe Advertising] e [!UICONTROL Analytics].
1. Nella riga del parametro [!UICONTROL Request URL - Hostname], individuare `lasteventf-tm.everesttech.net`.
1. Nella riga [!UICONTROL Request - Parameters], controlla i segnali generati, in modo simile al passaggio 3 in &quot;[Come confermare il codice con [!DNL Chrome Developer Tools]](#validate-js-chrome)&quot;.
   * (Implementazioni che utilizzano il codice `visitorAPI.js` del servizio Experience Cloud Identity) Verifica che il parametro `Sdid` corrisponda al `Supplemental Data ID` nel filtro di Adobe Analytics.
   * (Implementazioni che utilizzano il codice `alloy.js` di Experience Platform [!DNL Web SDK]) Verificare che il valore del parametro `advertisingStitchID` corrisponda al `Sdid` inviato all&#39;Edge Network di Experience Platform.
   * Se il codice non viene generato, verificare che il cookie Adobe Advertising sia stato rimosso nella scheda [!UICONTROL Application]. Una volta rimossa, aggiorna la pagina e ripeti la procedura.

   ![Controllo del codice JavaScript di [!DNL Analytics for Advertising] in [!DNL Platform Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)

>[!MORELIKETHIS]
>
>* [Panoramica di [!DNL Analytics for Advertising]](overview.md)
>* [Prerequisiti e informazioni chiave per l&#39;implementazione [!DNL Analytics for Advertising]](prerequisites.md)
