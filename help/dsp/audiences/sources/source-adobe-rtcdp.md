---
title: "Flusso di lavoro per l'utilizzo dell'integrazione DSP con [!DNL Adobe] [!DNL Real-time CDP]"
description: "Scopri come consentire all’DSP di acquisire [!DNL Adobe] [!DNL Real-time CDP] segmenti di prime parti."
feature: DSP Audiences
source-git-commit: fb42e4aacaf0ea22890e0b4a46719725c99fffdc
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---

# Flusso di lavoro per l&#39;utilizzo dell&#39;integrazione DSP con [!DNL Adobe Real-Time CDP]

1. [Consentire all’DSP di tradurre i segmenti di dati dei clienti in [!DNL LiveRamp RampIDs]](source-universal-id.md) che sono riconoscibili in un ambiente in cui è possibile fare offerte.<!-- I don't think I need this here: This requires DSP account-level and campaign-level settings to enable segment sharing with [!DNL LiveRamp], which will translate customer data to [!DNL RampIDs] to create targetable segments. Your Adobe Account Team will perform this configuration. -->

1. [Creare un’origine di pubblico](source-create.md) per importare tipi di pubblico sul tuo account DSP o su un account inserzionista.

1. Ad Experience Platform, configura una connessione di destinazione Advertising DSP utilizzando [!UICONTROL Source Key] generato nelle impostazioni di origine dell’DSP.

   Per istruzioni su come attivare la connessione di destinazione DSP, selezionare i segmenti e accedere alle autorizzazioni di controllo, vedi &quot;[Connessione Adobe Advertising Cloud DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).&quot;

Per ulteriore supporto, contatta il team del tuo account Adobe o `adcloud-support@adobe.com`.


>[!MORELIKETHIS]
>
>* [Attivare segmenti autenticati dai partner Universal ID](source-universal-id.md)
>* [Creare un’origine di pubblico per attivare tipi di pubblico di prime parti](source-create.md)
>* [Impostazioni origine pubblico](source-settings.md)
>* [Connessione Adobe Advertising DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [Panoramica del catalogo delle destinazioni](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [Flusso di lavoro per l&#39;utilizzo dell&#39;integrazione DSP con [!DNL Tealium]](/help/dsp/audiences/sources/source-tealium.md)
>* [Informazioni su Gestione dell&#39;audience](/help/dsp/audiences/audience-about.md)
