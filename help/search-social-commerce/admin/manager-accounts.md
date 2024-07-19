---
title: Gestione delle credenziali per gli account di Ad Network Manager
description: Scopri come fornire le credenziali per gli account  [!DNL Google Ads] manager.
exl-id: 95866a2e-4695-4b1d-ac23-844d3b9a0a74
feature: Search Admin
source-git-commit: 4cf04fc7ea22e50b5f56cd278ad9a1aac724edf7
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 0%

---

# Gestione delle credenziali per gli account di Ad Network Manager

Solo *[!DNL Google Ads]account*

Fornisci le credenziali per gli account manager [!DNL Google Ads] in cui desideri caricare le conversioni tra account diversi tramite Search, Social e Commerce. Utilizzare questa funzione se si desidera a) caricare metriche di conversione tra account [!DNL Adobe] in un account manager [!DNL Google Ads] o b) caricare obiettivi di portfolio che includono conversioni tra account diversi in [!DNL Google Ads] per l&#39;ottimizzazione ibrida.

<!-- [Maybe later: and c) sync conversion value rules for accounts that use cross-account conversion tracking with Google Ads.] -->

È possibile aggiungere le credenziali per i nuovi record account manager o autenticare nuovamente un account manager esistente.

Dopo aver aggiunto le credenziali per un account manager, le impostazioni dell&#39;account mostrano l&#39;ID account manager associato come di sola lettura. Inoltre, una colonna facoltativa &quot;[!UICONTROL Manager Account for Cross-Account Conversions]&quot; nella vista [!UICONTROL Campaigns] > [!UICONTROL Accounts] mostra l&#39;ID dell&#39;account manager per ogni account figlio e indica un errore quando l&#39;account manager non è autenticato. [!UICONTROL Notification Center] include notifiche quando mancano le credenziali di un account manager ([il [!UICONTROL Manager Account Missing Error]](/help/search-social-commerce/notifications/notification-about.md)) o quando scade un token di autenticazione dell&#39;account manager ([il [!UICONTROL Manager Account Auth Error]](/help/search-social-commerce/notifications/notification-about.md)).

## Per aggiungere le credenziali per un nuovo account manager

1. Nel menu principale, fare clic su **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. Selezionare **[!UICONTROL Create new manager account]**.

1. Immetti le credenziali di accesso per l’account manager.

   **[!UICONTROL Manager Account ID]** e **[!UICONTROL Login Email]** sono obbligatori. Search, Social e Commerce acquisiscono e memorizzano automaticamente il token dell’account da utilizzare per l’autenticazione.

   Facoltativamente, puoi includere **[!UICONTROL MCC Account Name]** per l&#39;identificazione in Search, Social e Commerce e nell&#39;account **[!UICONTROL Password]**. Immetti la password quando desideri crittografarla e salvarla in modo che l’account manager possa aggiornare i token in base alle esigenze.

1. Fare clic su **[!UICONTROL Authenticate]**.

1. Fare clic su **[!UICONTROL Save]**.

## Per autenticare nuovamente un account manager esistente

1. Nel menu principale, fare clic su **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. Selezionare **[!UICONTROL Reauthenticate existing manager account]**.

1. Selezionare l&#39;account manager.

1. Immetti le credenziali di accesso per l’account manager.

   **[!UICONTROL Manager Account ID]** e **E-mail di accesso** sono obbligatori. Search, Social e Commerce acquisiscono e memorizzano automaticamente il token dell’account da utilizzare per l’autenticazione.

   Facoltativamente, puoi includere **[!UICONTROL MCC Account Name]** per l&#39;identificazione in Search, Social e Commerce e nell&#39;account **[!UICONTROL Password]**. Immetti la password quando desideri crittografarla e salvarla in modo che l’account manager possa aggiornare i token in base alle esigenze.

1. Fare clic su **[!UICONTROL Authenticate]**.

1. Fare clic su **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Abilita il caricamento degli obiettivi nelle reti di annunci](/help/search-social-commerce/tools/objective-upload-to-networks.md)
>* [Carica metriche di conversione in [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
>* [Modifica le impostazioni delle notifiche](/help/search-social-commerce/notifications/notification-edit.md)
