---
title: Creare un’origine di pubblico per attivare i tipi di pubblico con ID universale
description: Scopri come creare una sorgente per importare i tipi di pubblico dalla piattaforma di dati dei clienti e convertirli in segmenti contenenti ID universali.
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
source-git-commit: 16a796e02150b00c77c825d7f54c6e390c85214a
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---

# Creare un’origine di pubblico per attivare i tipi di pubblico con ID universale

*Funzione beta*

Crea un’origine in DSP per ogni pubblico di prime parti nella piattaforma di dati cliente che desideri convertire in segmenti contenenti tipi di ID universali specificati. Puoi importare i segmenti nell’account DSP della tua organizzazione o in un account inserzionista. Gli addebiti per i dati vengono applicati in base ai tipi di ID universali selezionati.

Sono necessari passaggi aggiuntivi per acquisire i tipi di pubblico da ogni piattaforma di dati cliente. Vedere la nota alla fine della procedura.

1. Nel menu principale, fai clic su **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Clic **[!UICONTROL Add Source]**.

1. In [!UICONTROL Select a Type] selezionare la piattaforma dati del cliente:

   * *[!UICONTROL RT-CDP]*: [Il [!DNL Adobe Real-Time Customer Data Platform]](source-about.md).

   * *[!UICONTROL ActionIQ]*: Il [[!DNL ActionIQ] piattaforma dati cliente](source-about.md).

   * *[!UICONTROL Tealium CDP]*: (solo utenti configurati) Il [[!DNL Tealium] piattaforma dati cliente](source-about.md).

1. Specifica la [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* o *[!UICONTROL Account]*.

1. Inserisci il valore rimanente [impostazioni di origine](source-settings.md).

   Mantieni una copia di [!UICONTROL Source Key] che viene generato. Il valore ti servirà più tardi.

1. Clic **[!UICONTROL Save]**.

>[!NOTE]
>
>Dopo aver creato un’origine per la piattaforma di dati cliente, dovrai completare ulteriori passaggi. Consulta la [flusso di lavoro per importare tipi di pubblico da [!DNL Adobe] [!DNL Real-time CDP]](source-adobe-rtcdp.md)<!-- the [activation workflow for [!DNL ActionIQ]](source-actioniq.md), --> e [flusso di lavoro per importare tipi di pubblico da [!DNL Tealium]](source-tealium.md).

>[!MORELIKETHIS]
>
>* [Impostazioni origine pubblico](source-settings.md)
>* [Informazioni sulle origini del pubblico di prime parti](source-about.md)
>* [Connessione Adobe Advertising Cloud DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Informazioni su Gestione dell&#39;audience](/help/dsp/audiences/audience-about.md)
