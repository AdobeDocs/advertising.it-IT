---
title: Importa manualmente segmenti autenticati da [!DNL LiveRamp]
description: Scopri come attivare i tipi di pubblico autenticati tramite  [!DNL LiveRamp].
feature: DSP Audiences
exl-id: c56a54c7-5300-4cda-96d0-82d86e76ee39
source-git-commit: 0a1555875fd18b326297475bc19fcfd6f28ea0c5
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---

# Importa manualmente segmenti autenticati da [!DNL LiveRamp]

*funzionalità Beta*

È possibile inviare manualmente [!DNL LiveRamp] segmenti autenticati all&#39;DSP utilizzando il dashboard [!DNL LiveRamp] [!DNL Connect]. Puoi utilizzare i segmenti importati per il targeting del posizionamento. Per i segmenti di prime parti, le tariffe sono pari a 0,15 USD per visualizzazione e per impression pubblicitaria distribuite e a 0,25 USD per video.

La mappatura e il caricamento dei segmenti per ogni processo di importazione possono richiedere fino a sette giorni.

<!--Is this first step relevant for this process?

1. For measurement using [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md):

   1. Complete all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and make sure that the [AMO ID and EF ID](/help/integrations/analytics/ids.md) are being populated in your tracking URLs.
   
   1. [Maybe just add a param to existing tag] Deploy a second JavaScript tag for [!DNL RampIDs] on your webpages to match onsite events to ad impressions. Contact your Adobe Account Team to get the tag and instructions for where to implement it.

 -->

1. Completa i seguenti passaggi nel dashboard [!DNL Connect]:

   1. Attiva il riquadro di destinazione **[!DNL AAC API 1P Onboarding]**.

   1. Imposta [!DNL Identifier Settings] solo su **[!DNL Ramp ID]**.

      ![Impostazioni identificatore](/help/dsp/assets/liveramp-tile-settings.png)

   1. (Facoltativo) Se desideri comunque ricevere gli identificatori basati su cookie, crea una seconda sezione di destinazione [!DNL AAC API 1P Onboarding] con &quot;[!DNL Cookies],&quot; &quot;[!DNL IDFA]&quot; e &quot;[!DNL AAID]&quot; selezionati.

   1. Verifica nella libreria del pubblico (disponibile quando crei o modifichi un pubblico da [!UICONTROL Audiences] > [!UICONTROL All Audiences] o nelle impostazioni di posizionamento) che sia stato importato l&#39;intero conteggio dei segmenti.

>[!MORELIKETHIS]
>
>* [Informazioni sulle origini del pubblico di prime parti](source-about.md)
>* [Gestione delle origini del pubblico per attivare i tipi di pubblico con ID universale](source-manage.md)
>* [Connessione Adobe Advertising DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html?lang=it)
>* [Informazioni su Gestione dell&#39;audience](/help/dsp/audiences/audience-about.md)
