---
title: (Nuova interfaccia) Gestione delle credenziali per gli account di Google Ads Manager
description: Scopri come impostare e gestire le credenziali per gli account di gestione di Google Ads nella nuova interfaccia utente.
feature: Search Admin
source-git-commit: bf1ca7f6133c19bb68dbe0395416dca8ef647464
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 0%

---

# (Nuova interfaccia) Gestione delle credenziali per gli account manager [!DNL Google Ads]

*funzionalità Beta*

Solo *[!DNL Google Ads]account*

Fornisci le credenziali per gli account manager [!DNL Google Ads] in cui desideri caricare le conversioni tra account diversi tramite Search, Social e Commerce. Utilizzare questa funzione se si desidera a) caricare metriche di conversione tra account [!DNL Adobe] in un account manager [!DNL Google Ads] o b) caricare obiettivi di portfolio che includono conversioni tra account diversi in [!DNL Google Ads] per l&#39;ottimizzazione ibrida.

È possibile aggiungere le credenziali per i nuovi record account manager o autenticare nuovamente un account manager esistente.

Dopo aver aggiunto le credenziali per un account manager, le impostazioni dell&#39;account mostrano l&#39;ID account manager associato come di sola lettura. [!UICONTROL Notification Center] include [notifiche](/help/search-social-commerce/new-ui/notifications-manage.md) quando mancano le credenziali di un account manager ([!UICONTROL Manager Account Missing Error]) o quando scade un token di autenticazione dell&#39;account manager ([!UICONTROL Manager Account Auth Error]).

## Aggiungere le credenziali per un nuovo account manager {#create-manager-account}

1. Nel menu principale, fare clic su **[!UICONTROL Setup]** \> **[!UICONTROL Manager Accounts]**.

1. Fare clic su **[!UICONTROL +]**.

1. Selezionare la rete di annunci e quindi fare clic su **[!UICONTROL Next]**.

1. Specificare le [impostazioni account manager](#manager-account-settings).

1. Fare clic su **[!UICONTROL Authenticate]** e accedere utilizzando le credenziali dell&#39;account manager.

   Search, Social e Commerce acquisiscono e memorizzano automaticamente il token di autenticazione.

1. In Ricerca, Social e Commerce, fare clic su **[!UICONTROL Save]**.

## Modifica dettagli account manager {#edit-manager-account}

1. Nel menu principale, fare clic su **[!UICONTROL Setup]** \> **[!UICONTROL Manager Accounts]**.

1. Selezionare l&#39;account in uno dei modi seguenti:

   * Selezionare la casella di controllo accanto al nome dell&#39;account, quindi fare clic su **[!UICONTROL Edit]** nella barra degli strumenti Azioni collettive.

   * Posizionare il cursore sul nome dell&#39;account, fare clic su **...**, quindi su (/help/search-social-commerce/assets/edit-new.png &quot;Modifica&quot;).

1. Modifica le impostazioni dell&#39;account [manager](#manager-account-settings).

1. Fare clic su **[!UICONTROL Re-Authenticate]** e accedere utilizzando le credenziali dell&#39;account manager.

   Search, Social e Commerce acquisiscono e memorizzano automaticamente il token di autenticazione.

1. In Ricerca, Social e Commerce, fare clic su **[!UICONTROL Save]**.

## Autenticazione di un account manager {#reauthenticate-manager-account}

Autentica nuovamente un account manager quando il token OAuth scade o non è più valido.

1. Nel menu principale, fare clic su **[!UICONTROL Setup]** \> **[!UICONTROL Manager Accounts]**.

1. Posizionare il cursore sul nome dell&#39;account, fare clic su **...** e quindi su **[!UICONTROL Reauthenticate]**.

1. Accedi utilizzando le credenziali dell&#39;account manager.

   Search, Social e Commerce acquisiscono e memorizzano automaticamente il nuovo token di autenticazione.

## Impostazioni account manager {#manager-account-settings}

**[!UICONTROL Manager Account ID]:** ID account univoco per l&#39;account manager nella rete di annunci.

**[!UICONTROL Mnaager Account Name]:** nome da visualizzare per l&#39;account manager in Search, Social e Commerce.

**[!UICONTROL Login Email]:** L&#39;indirizzo e-mail associato all&#39;accesso dell&#39;account manager. Obbligatorio per l’autenticazione.

**[!UICONTROL Password]:** (facoltativo) la password per l&#39;account. Immetti la password quando desideri crittografarla e salvarla in modo che l’account manager possa aggiornare i token in base alle esigenze.

>[!MORELIKETHIS]
>
>* [Abilita il caricamento degli obiettivi nelle reti di annunci](/help/search-social-commerce/new-ui/goals/objectives/objective-upload-to-networks.md)
>* [Gestione notifiche](/help/search-social-commerce/new-ui/notifications-manage.md)

<!--
I don't see this yet in new UI:
>* [Upload Search, Social, & Commerce-tracked conversion metrics to [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
-->
