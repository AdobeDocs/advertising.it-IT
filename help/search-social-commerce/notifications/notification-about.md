---
title: Informazioni sulle notifiche
description: Scopri le notifiche, compresi i diversi tipi e categorie.
exl-id: 79495e1c-72ce-476f-83df-c4d95391f51c
feature: Search Notifications
source-git-commit: 49dc6a4a18966bbf68402d70aec9574ed11e1886
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---

# Informazioni sulle notifiche

*Funzione beta*

Puoi configurare le impostazioni di notifica per abbonarti o annullare l’abbonamento a diversi tipi di avvisi. Puoi visualizzare le notifiche in uno dei seguenti modi:

* Dalla sezione [!UICONTROL Notifications] , disponibile dal menu principale in ![Notifiche](/help/search-social-commerce/assets/notifications-panel.png "Notifiche").

* Da [!UICONTROL Insights & Reports] > [!UICONTROL Notification Center Beta].

* Da un [!UICONTROL Notification Center] applicazione web, che apre [!UICONTROL Notification Center] in una finestra separata al di fuori di Search, Social e Commerce.

  L’applicazione viene caricata più rapidamente della versione normale del browser e viene aggiornata automaticamente. Puoi installare l’applicazione e gestirla utilizzando l’app manager del browser.

* Dalle notifiche push al browser.

  Quando abiliti le notifiche push, vengono visualizzate in base alle convenzioni di notifica del browser.

Puoi visualizzare le notifiche, contrassegnarle come lette o non lette ed eliminare le notifiche.

## Tipi di notifica

* **[!UICONTROL Notices]**: avvisi sulla versione, sui tempi di inattività e su altre modifiche gestionali.

* **[!UICONTROL Recommendations]**: opportunità identificate per migliorare le prestazioni, implementare best practice e così via.

* **[!UICONTROL Warnings]**: problemi che richiedono attenzione ma non sono critici per l’ottimizzazione o la gestione.

* **[!UICONTROL Issues]**: problemi critici che richiedono attenzione immediata. Sono incluse le notifiche di errore di autorizzazione dell’account.

## Categorie di notifica

* [!UICONTROL Campaign Management]

   * **[!UICONTROL Bulksheets]**: notifiche che un [operazione bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) è stato completato o non è riuscito.

   * **[!UICONTROL Manager Account Missing]**: notifiche per cui mancano le credenziali per Search, Social e Commerce [account di ad network manager](/help/search-social-commerce/admin/manager-accounts.md), necessari per la corretta configurazione delle funzioni critiche.

   * **[!UICONTROL UI Actions]**: notifica del completamento o dell’errore dei processi eseguiti in background. I tipi di processo includono [processi bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md), i processi di modifica in blocco all’interno della tabella dati o utilizzando la barra degli strumenti, i processi di assegnazione delle entità o altre azioni all’interno dell’interfaccia utente (ad esempio la sincronizzazione con le reti di annunci, l’incollamento di righe o la ridenominazione di entità). Le assegnazioni di entità includono l&#39;assegnazione o la rimozione di un [valore di classificazione dell’etichetta](/help/search-social-commerce/campaign-management/label-classifications/classification-about.md) a qualsiasi entità, assegnando una campagna a un portfolio e assegnando o annullando l’assegnazione di un vincolo a un portfolio.<!--Link "constraint" to constraint-about.md if that file is ever public -->

   * [!UICONTROL Data Upload]

      * **[!UICONTROL Direct File Upload]**: utilizzato per una versione beta chiusa

      * **[!UICONTROL File Upload to Cloud Storage]**: utilizzato per una versione beta chiusa

   * [!UICONTROL Network Errors]

      * **[!UICONTROL Account Auth Error]**: notifiche per cui Search, Social e Commerce non sono stati in grado di accedere a un [account di rete dell’annuncio](/help/search-social-commerce/campaign-management/accounts/ad-network-account-about.md) credenziali non valide o token di autorizzazione non valido o scaduto.

      * **[!UICONTROL Account Missing]**: notifiche per cui mancano le credenziali per Search, Social e Commerce [account di rete dell’annuncio](/help/search-social-commerce/campaign-management/accounts/ad-network-account-about.md).

      * **[!UICONTROL Manager Account Auth Error]**: notifiche che Search, Social e Commerce non sono state sincronizzate con un [account di ad network manager](/help/search-social-commerce/admin/manager-accounts.md) credenziali non valide o token di autorizzazione non valido o scaduto.

  <!--
  * [!UICONTROL Setup Errors]
  
    * **[!UICONTROL Adobe Analytics Tracking Setup Error]**: : Notifications that the [!UICONTROL Landing Page Suffix] value is incorrect, missing, or contains an incorrect [AMO ID template](/help/integrations/analytics/ids.md#amo-id-formats); the [!UICONTROL Tracking Template] is incorrect or missing; or the [!UICONTROL Landing Page Suffix] or [!UICONTROL Tracking Template] is overridden at a lower level by an incorrect value. Separate notifications are sent a) for errors at the account level and b) for errors at the campaign and lower levels.
    
    * **[!UICONTROL Manager Account Missing]**: Notifications that Search, Social, & Commerce is missing the credentials for an [ad network manager account](/help/search-social-commerce/admin/manager-accounts.md), which are required for the correct setup of critical functions.
  -->

* [!UICONTROL Insights & Reports]

   * **[!UICONTROL Advertising Insights]**: notifiche che [un [!DNL Advertising Insight]](/help/search-social-commerce/advertising-insights/insight-about.md) è stato completato o non è riuscito.

   * **[!UICONTROL Custom Alerts]**: notifiche che [istanze di avviso](/help/search-social-commerce/alerts/alert-about.md) sono stati attivati per un modello di avviso.

   * **[!UICONTROL Reports]**: notifiche che un [rapporto personalizzato o pianificato](/help/search-social-commerce/reports/report-about.md) è stato completato o non è riuscito.

   * **[!UICONTROL Spreadsheet Feeds]**: notifiche che un [feed foglio di calcolo](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md) è stato completato o non è riuscito.

<!--
* [!UICONTROL Optimization]

  * **[!UICONTROL Accuracy]**: 

-->

<!--
* [!UICONTROL Portfolio Management]

  * **[!UICONTROL Simulation Report]**: 

-->

<!--
* [!UICONTROL System]

  * **[!UICONTROL Change Management]**: 

-->

>[!MORELIKETHIS]
>
>* [Visualizzare le notifiche](notification-view.md)
>* [Contrassegnare una notifica come letta o non letta](notification-mark-read-unread.md)
>* [Eliminare una notifica](notification-delete.md)
>* [Modifica le impostazioni delle notifiche](notification-edit.md)
>* [Abilitare e disabilitare le notifiche push da [!UICONTROL Notification Center]](notifications-push-enable-disable.md)
>* [Installare e disinstallare [!UICONTROL Notification Center] applicazione web](notification-app-install-uninstall.md)
