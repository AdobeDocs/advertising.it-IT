---
title: Creare un’origine di pubblico per attivare tipi di pubblico di prime parti
description: Scopri come creare un’origine per importare i tipi di pubblico nel tuo account o in un account inserzionista.
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
source-git-commit: 3347bfbaec92bb13428a39207954f895eb4f5d6d
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 3%

---

# Creare un’origine di pubblico per attivare tipi di pubblico di prime parti

<!-- Will this remain for admin users/Adobe Account Team users only? -->

Crea una sorgente per importare i tipi di pubblico sul tuo account DSP o su un account inserzionista. Attualmente, puoi importare tipi di pubblico da [il [!DNL Adobe Real-Time Customer Data Profile (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=it).

>[!NOTE]
>
>Dopo aver creato un&#39;origine per [!DNL Real-Time CDP], devi attivare il tuo [!DNL Real-Time CDP] pubblico tramite la destinazione Adobe Advertising DSP in [!DNL Real-Time CDP] per iniziare a importarli. Consulta [i passaggi nel flusso di lavoro di attivazione](source-about.md#workflow-sources).

1. Nel menu principale, fai clic su **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Clic [!UICONTROL Add Source].

1. In [!UICONTROL Select a Type] selezionare il tipo di origine.

   *[!UICONTROL RT-CDP]*: questo tipo di origine, per [il [!DNL Adobe Real-Time Customer Data Profile]](source-about.md), è l’unica opzione.

1. Specifica la [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* o *[!UICONTROL Account]*.

1. Inserisci il valore rimanente [impostazioni di origine](source-settings.md).

   Mantieni una copia di [!UICONTROL Source Key] che viene generato. Il valore ti servirà più tardi.

1. Clic **[!UICONTROL Save]**.

1. Ad Experience Platform, crea una connessione di destinazione Advertising DSP utilizzando [!UICONTROL Source Key] generato nelle impostazioni di origine dell’DSP.

   Per istruzioni su come attivare la connessione di destinazione DSP, selezionare i segmenti e accedere alle autorizzazioni di controllo, vedi &quot;[Connessione Adobe Advertising Cloud DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).&quot;

>[!MORELIKETHIS]
>
>* [Impostazioni origine pubblico](source-settings.md)
>* [Informazioni sull’attivazione di segmenti autenticati da origini pubblico](source-about.md)
>* [Attivare segmenti autenticati dai partner ID resistenti](source-durable-id.md)<!-- title?-->
>* [Connessione Adobe Advertising Cloud DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Informazioni su Gestione dell&#39;audience](/help/dsp/audiences/audience-about.md)

