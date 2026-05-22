---
title: Informazioni sulle origini del pubblico di prime parti
description: Scopri come convertire altri identificatori utente nei segmenti di prime parti in ID universali per il targeting senza cookie.
feature: DSP Audiences
exl-id: ba056440-fa2b-4472-bbfd-16dd0af887f1
TQID: https://experienceleague.adobe.com/8wdjwhNF-KDspEa1wSYWwlDOJxc3LiyqnSwEE-Fq9bY
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: 79f0b3872a0d5d3765093ce83cc8f1c284a8255c
workflow-type: tm+mt
source-wordcount: 710
ht-degree: 0%

---

# Informazioni sulle origini del pubblico di prime parti

La funzione di origine del pubblico consente di importare segmenti di prime parti contenenti ID universali così come sono o di convertirli in segmenti contenenti tipi di ID universali specifici:

* Gli inserzionisti in Australia possono importare segmenti di prime parti che contengono già [!DNL AdFixus] ID universali.

* DSP può acquisire segmenti di prime parti composti da ID e-mail con hash, cookie e ID mobile advertising (MAID) generati in piattaforme dati cliente (CDP) aggiuntive e convertirli in segmenti composti da [!DNL LiveRamp] [!DNL RampIDs] e [!DNL Unified ID 2.0 (UID2.0)] ID.

Per tutti i tipi di ID, ogni ID risultante è basato sulle persone e vengono applicati limiti di frequenza degli annunci a livello di ID<!-- Move that info. to somewhere else? -->. I dettagli del segmento includono la dimensione di ciascun tipo di ID universale e la dimensione di ciascun tipo di dispositivo monitorato da cookie o ID dispositivo.

## Tipi di ID universali a cui è possibile tradurre i segmenti di prime parti {#universal-id-types}

<!--
  Replace below with this once ID5 sources are possible 

Using your first-party data, you can create segments with IDs from the following universal ID partners.

* Authenticated (deterministic) IDs using hashed email addresses:

-->

È possibile tradurre i segmenti di prime parti da [!DNL ActionIQ], [!DNL Adobe] [!DNL Real-time CDP], [!DNL Amperity], [!DNL Optimizely] e [!DNL Tealium] in segmenti con ID autenticati (deterministici) dai seguenti partner ID universali.

* [[!DNL LiveRamp] [!DNL RampIDs]](https://liveramp.com/identity-resolution):

   * Per il retargeting degli utenti connessi.

     [!DNL RampIDs] sono disponibili per gli utenti in Nord America, Australia e Nuova Zelanda.

     Le tariffe sono pari a 0,15 USD per visualizzazione e per impression pubblicitaria distribuite e a 0,25 USD per video.

   * Per la misurazione tramite [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md).

* [[!DNL Unified ID 2.0 (UID2.0)] ID](https://unifiedid.com):

   * Per il retargeting degli utenti connessi.

     [!DNL UID2 IDs] non sono disponibili per gli utenti nello Spazio economico europeo e in alcuni altri paesi. Vedi l&#39;[elenco dei paesi vietati](/help/policies/universal-id-policy.md#prohibited-countries-uid2).

     Le tariffe sono pari a 0,15 USD per visualizzazione e per impression pubblicitaria distribuite e a 0,25 USD per video.

<!--
 Not yet

* Probabilistic (unauthenticated) IDs using hashed email addresses:

  * [[!DNL ID5] IDs](https://id5.io): For retargeting unauthenticated site traffic, prospecting using third-party data, and measurement for both using [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md). ID5 IDs are available for no fee.

    ID5 creates an ID by stitching together user signals (hashed email address) with various browser signals (such as IP address and timestamp).

    [!DNL Analytics] measurement requires all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and the [AMO ID and EF ID in your tracking URLs](/help/integrations/analytics/ids.md). You also must sign an agreement with [!DNL ID5] and set a parameter within your existing JavaScript tracking tags. Contact your Adobe Account Team for instructions.
-->

<!--
    >[!NOTE]
    >
    >Third-party segments from [!DNL Eyeota] may automatically include ID5 IDs, in addition to users tracked by cookies or device IDs. The segment details include the size for each type. The usual usage fee for each segment, which is stated next to the segment name, applies; no additional fees are charged for the ID5 IDs.
-->

## Piattaforme di dati cliente supportate per segmenti di prime parti

DSP ha stabilito dei connettori per i seguenti CDP per acquisire rapidamente i segmenti di prime parti.

DSP può anche connettersi a qualsiasi CDP aggiuntivo utilizzando la condivisione di dati in batch, in streaming o basata su API. Per effettuare l’integrazione con un nuovo CDP, contatta il team del tuo account Adobe.

### [!DNL ActionIQ]

Puoi condividere i dati di prime parti della tua organizzazione dalla piattaforma dati del cliente [!DNL ActionIQ] con DSP per convertire gli indirizzi e-mail con hash in ID universali per la pubblicità mirata in DSP. Questa integrazione richiede la personalizzazione. Per ulteriori informazioni, contatta il team del tuo account di Adobe.

### [!DNL Adobe Real-Time CDP]

DSP è una *destinazione* integrata per [the [!DNL Adobe Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html), che fa parte di Adobe Experience Platform.

In [!DNL Real-Time CDP], le destinazioni sono connessioni a piattaforme dati esterne che consentono l&#39;attivazione diretta dei dati. Puoi utilizzare le destinazioni per attivare gli indirizzi e-mail con hash, i cookie e gli ID mobile advertising per la pubblicità mirata in DSP. Per ulteriori informazioni sulle destinazioni, vedere la [Guida alle destinazioni](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html) di Experience Platform, inclusa una panoramica del prodotto, istruzioni per [creare aree di lavoro di destinazione](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/destinations-workspace.html) e [creare connessioni di destinazione](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html) e [attivare dati nelle destinazioni](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-segment-streaming-destinations.html).

Per consentire a DSP di acquisire i segmenti di prime parti [!DNL Adobe] [!DNL Real-time CDP] e convertire gli indirizzi e-mail con hash, i cookie e gli ID mobile advertising in ID universali, consulta &quot;[Convertire gli ID utente da [!DNL Adobe Real-Time CDP] a ID universali](/help/dsp/audiences/sources/source-adobe-rtcdp.md).&quot;

### [!DNL AdFixus]

Gli inserzionisti australiani possono utilizzare l&#39;integrazione Advertising DSP con [!DNL AdFixus] per importare segmenti di prime parti che contengono [!DNL AdFixus] ID universali. Questo percorso è separato dalla conversione degli ID e-mail o MAID con hash in un connettore CDP in [!DNL RampIDs] o [!DNL UID2] ID. Per ulteriori informazioni, consulta &quot;[Importare segmenti di prime parti da [!DNL AdFixus]](/help/dsp/audiences/sources/source-adfixus.md).&quot;

### [!DNL Amperity]

Puoi condividere i dati di prime parti della tua organizzazione dalla piattaforma dati del cliente [!DNL Amperity] con DSP per convertire gli indirizzi e-mail con hash in ID universali per la pubblicità mirata in DSP. Per ulteriori informazioni, vedere &quot;[Convertire gli ID utente da [!DNL Amperity] a ID universali](/help/dsp/audiences/sources/source-amperity.md).&quot;

### [!DNL Optimizely]

Puoi condividere i dati di prime parti della tua organizzazione dalla piattaforma dati del cliente [!DNL Optimizely] con DSP per convertire gli indirizzi e-mail con hash in ID universali per la pubblicità mirata in DSP. Per ulteriori informazioni, vedere &quot;[Convertire gli ID utente da [!DNL Optimizely] a ID universali](/help/dsp/audiences/sources/source-optimizely.md).&quot;

### [!DNL Tealium]

Puoi condividere i dati di prime parti della tua organizzazione dalla piattaforma dati del cliente [!DNL Tealium] utilizzando [!DNL Amazon Web Services]. Per ulteriori informazioni sulla conversione degli indirizzi e-mail con hash in ID universali per la pubblicità mirata in DSP, consulta &quot;[Convertire gli ID utente da [!DNL Tealium] a ID universali](/help/dsp/audiences/sources/source-tealium.md).&quot;

>[!MORELIKETHIS]
>
>* [Gestisci origini pubblico per attivare il pubblico con ID universale](source-manage.md)
>* [Supporto per l&#39;attivazione degli ID universali](/help/dsp/audiences/universal-ids.md)
>* [Converti ID utente da [!DNL Adobe Real-Time CDP] a ID universali](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Converti ID utente da [!DNL Amperity] a ID universali](/help/dsp/audiences/sources/source-amperity.md)
>* [Converti ID utente da [!DNL Optimizely] a ID universali](/help/dsp/audiences/sources/source-optimizely.md)
>* [Converti ID utente da [!DNL Tealium] a ID universali](/help/dsp/audiences/sources/source-tealium.md)
>* [Importa segmenti di prime parti da [!DNL AdFixus]](/help/dsp/audiences/sources/source-adfixus.md)
>* [Informazioni su Gestione dell&#39;audience](/help/dsp/audiences/audience-about.md)
>* [Impostazioni posizionamento](/help/dsp/campaign-management/placements/placement-settings.md)
