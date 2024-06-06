---
title: Importare manualmente segmenti autenticati da [!DNL LiveRamp]
description: Scopri come attivare i tipi di pubblico autenticati tramite [!DNL LiveRamp].
feature: DSP Audiences
exl-id: c56a54c7-5300-4cda-96d0-82d86e76ee39
source-git-commit: 295cc610a7e5e811fe555db69373a8bf5b4012f7
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%

---

# Importare manualmente segmenti autenticati da [!DNL LiveRamp]

*Funzione beta*

Puoi inviare manualmente i messaggi autenticati [!DNL LiveRamp] segmenti all&#39;DSP utilizzando il [!DNL LiveRamp] [!DNL Connect] dashboard. Puoi utilizzare i segmenti importati per il targeting del posizionamento. Per i segmenti di prime parti, le tariffe sono pari a 0,15 USD per visualizzazione e per impression pubblicitaria distribuite e a 0,25 USD per video.

La mappatura e il caricamento dei segmenti per ogni processo di importazione possono richiedere fino a sette giorni.

<!--Is this first step relevant for this process?

1. For measurement using [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md):

   1. Complete all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and make sure that the [AMO ID and EF ID](/help/integrations/analytics/ids.md) are being populated in your tracking URLs.
   
   1. [Maybe just add a param to existing tag] Deploy a second JavaScript tag for [!DNL RampIDs] on your webpages to match onsite events to ad impressions. Contact your Adobe Account Team to get the tag and instructions for where to implement it.

 -->

1. Completa i seguenti passaggi nella sezione [!DNL Connect] dashboard:

   1. Attiva il riquadro di destinazione **[!DNL AAC API 1P Onboarding]**.

   1. Imposta [!DNL Identifier Settings] a **[!DNL Ramp ID]** solo.

      ![Impostazioni identificatore](/help/dsp/assets/liveramp-tile-settings.png)

   1. (Facoltativo) Se desideri ricevere comunque gli identificatori basati su cookie, crea un secondo [!DNL AAC API 1P Onboarding] riquadro di destinazione con &quot;[!DNL Cookies],&quot; &quot;[!DNL IDFA],&quot; e &quot;[!DNL AAID]&quot; selezionato.

   1. Verifica nella libreria del pubblico (disponibile quando crei o modifichi un pubblico da ) [!UICONTROL Audiences] > [!UICONTROL All Audiences] o nelle impostazioni di posizionamento) è stato importato l’intero conteggio dei segmenti.

>[!MORELIKETHIS]
>
>* [Informazioni sulle origini del pubblico di prime parti](source-about.md)
>* [Gestire le origini del pubblico per attivare i tipi di pubblico con ID universale](source-manage.md)
>* [Impostazioni origine pubblico](source-settings.md)
>* [Connessione Adobe Advertising DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Informazioni su Gestione dell&#39;audience](/help/dsp/audiences/audience-about.md)
