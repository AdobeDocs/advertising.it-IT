---
title: Informazioni sulle origini del pubblico di prime parti
description: Scopri come convertire altri identificatori utente nei segmenti di prime parti in ID universali per il targeting senza cookie.
feature: DSP Audiences
exl-id: ba056440-fa2b-4472-bbfd-16dd0af887f1
source-git-commit: 3a641db6b145e67e6e1f1daca271dd524973e075
workflow-type: tm+mt
source-wordcount: '544'
ht-degree: 0%

---

# Informazioni sulle origini del pubblico di prime parti

*funzionalità Beta*

L’DSP può acquisire segmenti di prime parti composti da ID e-mail con hash incorporati nella piattaforma di dati cliente (CDP) e convertirli in segmenti costituiti da ID universali. Ogni ID risultante è basato sulle persone e vengono applicati limiti di frequenza degli annunci a livello di ID<!-- Move that info. to somewhere else? -->.

I dettagli del segmento includono la dimensione di ogni tipo di ID universale e la dimensione di ogni tipo di dispositivo monitorato da cookie o ID dispositivo.

## Tipi di ID universali {#universal-id-types}

<!--  Replace below with this once ID5 sources are possible 

Using your first-party data, you can create segments with IDs from the following universal ID partners.

* Authenticated (deterministic) IDs using hashed email addresses:

-->

Puoi tradurre i segmenti di prime parti in segmenti con ID autenticati (deterministici) dai seguenti partner ID universali.

* [[!DNL LiveRamp] [!DNL RampIDs]](https://liveramp.com/identity-resolution):

   * Per il retargeting degli utenti connessi.

     [!DNL RampIDs] sono disponibili per gli utenti in Nord America, Australia e Nuova Zelanda.

     Le tariffe sono pari a 0,15 USD per visualizzazione e per impression pubblicitaria distribuite e a 0,25 USD per video.

   * Per la misurazione tramite [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md).

* [[!DNL Unified ID 2.0 (UID2.0)] ID](https://unifiedid.com):

   * Per il retargeting degli utenti connessi.

     [!DNL UID2 IDs] non sono disponibili per gli utenti nello Spazio economico europeo e in alcuni altri paesi. Vedi l&#39;[elenco dei paesi vietati](/help/policies/universal-id-policy.md#prohibited-countries-uid2).

     Le tariffe sono pari a 0,15 USD per visualizzazione e per impression pubblicitaria distribuite e a 0,25 USD per video.

<!-- Not yet

* Probabilistic (unauthenticated) IDs using hashed email addresses:

  * [[!DNL ID5] IDs](https://id5.io): For retargeting unauthenticated site traffic, prospecting using third-party data, and measurement for both using [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md). ID5 IDs are available for no fee.

    ID5 creates an ID by stitching together user signals (hashed email address) with various browser signals (such as IP address and timestamp).

    [!DNL Analytics] measurement requires all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and the [AMO ID and EF ID in your tracking URLs](/help/integrations/analytics/ids.md). You also must sign an agreement with [!DNL ID5] and set a parameter within your existing JavaScript tracking tags. <!-- Contact your Adobe Account Team for instructions. -->

<!--
    >[!NOTE]
    >
    >Third-party segments from [!DNL Eyeota] may automatically include ID5 IDs, in addition to users tracked by cookies or device IDs. The segment details include the size for each type. The usual usage fee for each segment, which is stated next to the segment name, applies; no additional fees are charged for the ID5 IDs.
-->

## Piattaforme di dati cliente supportate per segmenti di prime parti

L’DSP ha stabilito dei connettori per i seguenti CDP per acquisire rapidamente i segmenti di prime parti.

L’DSP può anche connettersi a qualsiasi CDP aggiuntivo utilizzando la condivisione di dati in batch, in streaming o basata su API. Per l’integrazione con un nuovo CDP, contatta il team del tuo account Adobe.

### [!DNL Adobe Real-Time CDP]

DSP è una *destinazione* integrata per [the [!DNL Adobe Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=it), che fa parte di Adobe Experience Platform.

In [!DNL Real-Time CDP], le destinazioni sono connessioni a piattaforme dati esterne che consentono l&#39;attivazione diretta dei dati. Puoi utilizzare le destinazioni per attivare gli indirizzi e-mail con hash per la pubblicità mirata in DSP. Per ulteriori informazioni sulle destinazioni, vedere l&#39;Experience Platform [Guida alle destinazioni](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html), che include una panoramica del prodotto, istruzioni per [la creazione delle aree di lavoro di destinazione](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/destinations-workspace.html) e [la creazione delle connessioni di destinazione](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html) e [l&#39;attivazione dei dati nelle destinazioni](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-segment-streaming-destinations.html).

Per consentire all&#39;DSP di acquisire i segmenti di prime parti [!DNL Adobe] [!DNL Real-time CDP] e convertire gli indirizzi e-mail con hash in ID universali, vedi &quot;[Convertire gli ID utente da [!DNL Adobe Real-Time CDP] a ID universali](/help/dsp/audiences/sources/source-adobe-rtcdp.md).&quot;

### [!DNL ActionIQ]

Puoi condividere i dati di prime parti della tua organizzazione dalla piattaforma dati cliente [!DNL ActionIQ] con DSP per convertire gli indirizzi e-mail con hash in ID universali per la pubblicità mirata in DSP. Questa integrazione richiede la personalizzazione. Per ulteriori informazioni, contatta il team del tuo account Adobe.

### [!DNL Amperity]

Puoi condividere i dati di prime parti della tua organizzazione dalla piattaforma dati cliente [!DNL Amperity] con DSP per convertire gli indirizzi e-mail con hash in ID universali per la pubblicità mirata in DSP. Per ulteriori informazioni, vedere &quot;[Convertire ID utente da [!DNL Amperity] a ID universali](/help/dsp/audiences/sources/source-amperity.md).&quot;

### [!DNL Optimizely]

Puoi condividere i dati di prime parti della tua organizzazione dalla piattaforma dati cliente [!DNL Optimizely] con DSP per convertire gli indirizzi e-mail con hash in ID universali per la pubblicità mirata in DSP. Per ulteriori informazioni, vedere &quot;[Convertire ID utente da [!DNL Optimizely] a ID universali](/help/dsp/audiences/sources/source-optimizely.md).&quot;

### [!DNL Tealium]

Puoi condividere i dati di prime parti della tua organizzazione dalla piattaforma dati del cliente [!DNL Tealium] utilizzando [!DNL Amazon Web Services]. Per ulteriori informazioni sulla conversione degli indirizzi e-mail con hash in ID universali per la pubblicità mirata in DSP, consulta &quot;[Converti ID utente da [!DNL Tealium] a ID universali](/help/dsp/audiences/sources/source-tealium.md).&quot;

>[!MORELIKETHIS]
>
>* [Gestione delle origini del pubblico per attivare i tipi di pubblico con ID universale](source-manage.md)
>* [Supporto per l&#39;attivazione di ID universali](/help/dsp/audiences/universal-ids.md)
>* [Converti ID utente da [!DNL Adobe Real-Time CDP] a ID universali](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Converti ID utente da [!DNL Amperity] a ID universali](/help/dsp/audiences/sources/source-amperity.md)
>* [Converti ID utente da [!DNL Optimizely] a ID universali](/help/dsp/audiences/sources/source-optimizely.md)
>* [Converti ID utente da [!DNL Tealium] a ID universali](/help/dsp/audiences/sources/source-tealium.md)
>* [Informazioni su Gestione dell&#39;audience](/help/dsp/audiences/audience-about.md)
>* [Impostazioni posizionamento](/help/dsp/campaign-management/placements/placement-settings.md)
