---
title: Gestione delle credenziali per gli account di Ad Network Manager
description: Scopri come fornire le credenziali per il [!DNL Google Ads] account manager.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 1%

---

# Gestione delle credenziali per gli account di Ad Network Manager

*Funzione beta*

*[!DNL Google Ads]solo account*

Immetti le credenziali per [!DNL Google Ads] gli account manager per i quali desideri caricare le conversioni tra account diversi tramite Search, Social e Commerce. Utilizza questa funzione per caricare a) [!DNL Adobe]-metriche di conversione tra account diversi in una [!DNL Google Ads] account manager o b) carica gli obiettivi del portfolio che includono le conversioni tra account diversi in [!DNL Google Ads] per l’ottimizzazione ibrida.

<!-- [Maybe later: and c) sync conversion value rules for accounts that use cross-account conversion tracking with Google Ads.] -->

È possibile aggiungere le credenziali per i nuovi record account manager o autenticare nuovamente un account manager esistente.

Dopo aver aggiunto le credenziali per un account manager, le impostazioni dell&#39;account mostrano l&#39;ID account manager associato come di sola lettura. Inoltre, un’&quot;[!UICONTROL Manager Account for Cross-Account Conversions]&quot; nella colonna [!UICONTROL Campaigns] > [!UICONTROL Accounts] visualizza mostra l’ID account manager per ogni account figlio e indica un errore quando l’account manager non è autenticato. [!UICONTROL Notification Center] include notifiche quando mancano le credenziali di un account manager ([il [!UICONTROL Manager Account Missing Error]](/help/search-social-commerce/notifications/notification-about.md)) o quando scade un token di autenticazione dell’account manager ([il [!UICONTROL Manager Account Auth Error]](/help/search-social-commerce/notifications/notification-about.md)).

## Per aggiungere le credenziali per un nuovo account manager

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. Seleziona **[!UICONTROL Create new manager account]**.

1. Immetti le credenziali di accesso per l’account manager.

   Il **[!UICONTROL Manager Account ID]** e **[!UICONTROL Login Email]** sono obbligatori. Search, Social e Commerce acquisiscono e memorizzano automaticamente il token dell’account da utilizzare per l’autenticazione.

   Facoltativamente, puoi includere una **[!UICONTROL MCC Account Name]** per l’identificazione all’interno di Search, Social, &amp; Commerce e dell’account **[!UICONTROL Password]**. Immetti la password quando desideri crittografarla e salvarla in modo che l’account manager possa aggiornare i token in base alle esigenze.

1. Clic **[!UICONTROL Authenticate]**.

1. Clic **[!UICONTROL Save]**.

## Per autenticare nuovamente un account manager esistente

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. Seleziona **[!UICONTROL Reauthenticate existing manager account]**.

1. Selezionare l&#39;account manager.

1. Immetti le credenziali di accesso per l’account manager.

   Il **[!UICONTROL Manager Account ID]** e **E-mail di accesso** sono obbligatori. Search, Social e Commerce acquisiscono e memorizzano automaticamente il token dell’account da utilizzare per l’autenticazione.

   Facoltativamente, puoi includere una **[!UICONTROL MCC Account Name]** per l’identificazione all’interno di Search, Social, &amp; Commerce e dell’account **[!UICONTROL Password]**. Immetti la password quando desideri crittografarla e salvarla in modo che l’account manager possa aggiornare i token in base alle esigenze.

1. Clic **[!UICONTROL Authenticate]**.

1. Clic **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Abilita il caricamento degli obiettivi nelle reti di annunci](/help/search-social-commerce/tools/objective-upload-to-networks.md)
>* [Carica metriche di conversione in [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
>* [Modifica le impostazioni delle notifiche](/help/search-social-commerce/notifications/notification-edit.md)

