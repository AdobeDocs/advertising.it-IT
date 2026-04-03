---
title: Sincronizza  [!DNL Adobe]  tipi di pubblico
description: Scopri come sincronizzare metadati, dati gerarchici e dati di pubblico univoci per i tuoi [!DNL Adobe] tipi di pubblico.
exl-id: 8b8c3aa0-2aa9-4ad7-a4c0-1b7ba881acd3
feature: Search Admin
TQID: https://experienceleague.adobe.com/PKWhdnMHVAI3aI--1vdCeqnX6b8j34uvHycZLw1Yvjw
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: e55292b5-d4a1-4c98-9c20-2a2c5bea07fb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 185
ht-degree: 0%

---

# Sincronizza [!DNL Adobe] tipi di pubblico

Solo *[!DNL Direct Access]amministratori e client manager*

*Inserzionisti solo con integrazione Adobe Advertising-Adobe Audience Manager o Adobe Advertising-Adobe Analytics*

È possibile consentire a Search, Social e Commerce di richiamare metadati, dati gerarchici e dati di pubblico univoci per tutti i tipi di pubblico [!DNL Adobe] di un inserzionista o di un&#39;agenzia nelle visualizzazioni [!UICONTROL Campaigns] > [!UICONTROL Audiences]. Queste informazioni includono i dati per:

* Segmenti Adobe Audience Manager

* Segmenti Adobe Analytics pubblicati in Adobe Experience Cloud

* Segmenti creati con Adobe Experience Cloud [!DNL Audience Library]

Per essere idoneo, l&#39;inserzionista o l&#39;agenzia deve implementare il [servizio Adobe Experience Platform Identity](https://experienceleague.adobe.com/docs/id-service/using/home.html) e fornire il proprio ID organizzazione (precedentemente denominato [!DNL IMS Org ID]).

La sincronizzazione iniziale richiede circa 24 ore. Successivamente, i dati vengono sincronizzati in tempo reale, con un ritardo di uno o due secondi.

1. Nel menu principale, fare clic su **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Audience Manager Setup]**.

1. Immettere l&#39;ID organizzazione univoco per l&#39;account Adobe Experience Cloud dell&#39;inserzionista, quindi fare clic su **[!UICONTROL Submit]**.

   Se non conosci l&#39;ID organizzazione dell&#39;inserzionista, cercalo nel campo **[!UICONTROL IMS Org ID]** nelle impostazioni dell&#39;inserzionista in [!UICONTROL Admin] > [!UICONTROL Manage Client].

>[!MORELIKETHIS]
>
>* [Informazioni sui tipi di pubblico](/help/search-social-commerce/campaign-management/campaigns/audience-about.md)
>* [Integrazione con soluzioni e servizi Adobe Experience Cloud](/help/search-social-commerce/introduction/integrations.md)
