---
title: Creare una sorgente di pubblico per attivare il pubblico di prime parti
description: Scopri come creare un’origine per importare i tipi di pubblico nel tuo account o in un account inserzionista.
feature: DSP Audiences
exl-id: 16eb7cdb-4364-4e94-ba73-0f2d4d200cb9
source-git-commit: 1c13874967ec4ad264e5fa6a5e0dfeb6120f53cc
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 0%

---

# Creare una sorgente di pubblico per attivare il pubblico di prime parti

*Funzione beta*

<!-- Will this remain for admin users/Adobe account teams only? -->

Crea un&#39;origine per importare i tipi di pubblico nel tuo account DSP o un account inserzionista. Attualmente, puoi importare tipi di pubblico da [la [!DNL Adobe Real-Time Customer Data Profile (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html).

>[!NOTE]
>
>Dopo aver creato un&#39;origine per [!DNL Real-Time CDP], è necessario attivare il [!DNL Real-Time CDP] tipi di pubblico tramite l’Adobe Advertising DSP destinazione all’interno di [!DNL Real-Time CDP] per iniziare a importarli. Vedi [i passaggi nel flusso di lavoro di attivazione](source-about.md#workflow-sources).

1. Nel menu principale, fai clic su **[!UICONTROL Audiences] > [!UICONTROL Sources (BETA)].

1. Clic [!UICONTROL Add Source].

1. In [!UICONTROL Select a Type] selezionare il tipo di origine.

   *[!UICONTROL RT-CDP]*: Questo tipo di origine, per [la [!DNL Adobe Real-Time Customer Data Profile]](source-about.md), è l’unica opzione.

1. Specifica la [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* o *[!UICONTROL Account]*.

1. Inserisci il resto [impostazioni di origine](source-settings.md).

   Conserva una copia del [!UICONTROL Source Key] che viene generato. Il valore sarà necessario in un secondo momento.

1. Clic **[!UICONTROL Save]**.

1. Ad Experience Platform, crea una connessione di destinazione DSP pubblicità utilizzando [!UICONTROL Source Key] generato nelle impostazioni dell&#39;origine DSP.

Per istruzioni su come attivare la connessione di destinazione DSP, selezionare i segmenti e accedere alle autorizzazioni di controllo, vedere &quot;[Connessione Adobe Advertising Cloud DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).&quot;

>[!MORELIKETHIS]
>
>* [Impostazioni origine pubblico](source-settings.md)
>* [Informazioni sull’attivazione dei segmenti autenticati da Audience Sources](source-about.md)
>* [Attivare i segmenti autenticati dai partner ID durevoli](source-durable-id.md)<!-- title?-->
>* [Connessione Adobe Advertising Cloud DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Informazioni sulla gestione dell&#39;audience](/help/dsp/audiences/audience-about.md)

