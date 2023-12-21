---
title: Creare un’origine di pubblico per attivare tipi di pubblico di prime parti
description: Scopri come creare un’origine per importare i tipi di pubblico nel tuo account o in un account inserzionista.
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
source-git-commit: 6c918b387067237de5d1eae42ae8ad253884d761
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---

# Creare un’origine di pubblico per attivare tipi di pubblico di prime parti

<!-- Will this remain for admin users/Adobe Account Team users only? -->

Crea un’origine in DSP per importare tipi di pubblico di prime parti nel tuo account DSP o in un account inserzionista.

Per ulteriori passaggi necessari per acquisire segmenti da specifiche piattaforme di dati dei clienti, consulta [i flussi di lavoro di attivazione specifici per il pubblico](source-about.md)

1. Nel menu principale, fai clic su **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Clic **[!UICONTROL Add Source]**.

1. In [!UICONTROL Select a Type] selezionare il tipo di origine.

   * *[!UICONTROL RT-CDP]*: [Il [!DNL Adobe Real-Time Customer Data Platform]](source-about.md).

   <!-- * *[!UICONTROL ActionIQ]*: The [[!DNL ActionIQ] customer data platform](source-about.md). -->

   * *[!UICONTROL Tealium CDP]*: Il [[!DNL Tealium] piattaforma dati cliente](source-about.md).

1. Specifica la [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* o *[!UICONTROL Account]*.

1. Inserisci il valore rimanente [impostazioni di origine](source-settings.md).

   Mantieni una copia di [!UICONTROL Source Key] che viene generato. Il valore ti servirà più tardi.

1. Clic **[!UICONTROL Save]**.

>[!NOTE]
>
>Dopo aver creato un’origine per la piattaforma di dati cliente, dovrai completare ulteriori passaggi. Consulta la [workflow di attivazione per [!DNL Adobe] [!DNL Real-time CDP]](source-adobe-rtcdp.md)<!-- the [activation workflow for [!DNL ActionIQ]](source-actioniq.md), --> e [workflow di attivazione per [!DNL Tealium]](source-tealium.md).

>[!MORELIKETHIS]
>
>* [Impostazioni origine pubblico](source-settings.md)
>* [Informazioni sull’attivazione di segmenti autenticati da origini pubblico](source-about.md)
>* [Attivare segmenti autenticati dai partner Universal ID](source-universal-id.md)<!-- title?-->
>* [Connessione Adobe Advertising Cloud DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Informazioni su Gestione dell&#39;audience](/help/dsp/audiences/audience-about.md)
