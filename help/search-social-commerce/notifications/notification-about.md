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

*Funzionalità Beta*

Puoi configurare le impostazioni di notifica per abbonarti o annullare l’abbonamento a diversi tipi di avvisi. Puoi visualizzare le notifiche in uno dei seguenti modi:

* Dal pannello [!UICONTROL Notifications], disponibile dal menu principale in ![Notifiche](/help/search-social-commerce/assets/notifications-panel.png "Notifiche").

* Da [!UICONTROL Insights & Reports] > [!UICONTROL Notification Center Beta].

* Da un&#39;applicazione Web [!UICONTROL Notification Center], che apre [!UICONTROL Notification Center] in una finestra separata al di fuori di Search, Social e Commerce.

  L’applicazione viene caricata più rapidamente della versione normale del browser e viene aggiornata automaticamente. Puoi installare l’applicazione e gestirla utilizzando l’app manager del browser.

* Dalle notifiche push al browser.

  Quando abiliti le notifiche push, vengono visualizzate in base alle convenzioni di notifica del browser.

Puoi visualizzare le notifiche, contrassegnarle come lette o non lette ed eliminare le notifiche.

## Tipi di notifica

* **[!UICONTROL Notices]**: avvisi sulla versione, sui tempi di inattività e altre informazioni sulla gestione delle modifiche.

* **[!UICONTROL Recommendations]**: sono state identificate opportunità per migliorare le prestazioni, implementare best practice e così via.

* **[!UICONTROL Warnings]**: problemi che richiedono attenzione ma non sono critici per l&#39;ottimizzazione o la gestione.

* **[!UICONTROL Issues]**: problemi critici che richiedono attenzione immediata. Sono incluse le notifiche di errore di autorizzazione dell’account.

## Categorie di notifica

* [!UICONTROL Campaign Management]

   * **[!UICONTROL Bulksheets]**: notifiche di completamento o di errore di un&#39;operazione [bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

   * **[!UICONTROL Manager Account Missing]**: notifiche per le quali Search, Social e Commerce non dispongono delle credenziali per un account [ad network manager](/help/search-social-commerce/admin/manager-accounts.md), necessarie per la corretta configurazione delle funzioni critiche.

   * **[!UICONTROL UI Actions]**: notifica del completamento o dell&#39;errore dei processi eseguiti in background. I tipi di processo includono [processi bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md), processi di modifica in blocco all&#39;interno della tabella dati o utilizzando la barra degli strumenti, processi di assegnazione di entità o altre azioni all&#39;interno dell&#39;interfaccia utente (ad esempio la sincronizzazione con reti di annunci, l&#39;incollamento di righe o la ridenominazione di entità). Le assegnazioni di entità includono l&#39;assegnazione o l&#39;annullamento dell&#39;assegnazione di un valore di classificazione [etichetta](/help/search-social-commerce/campaign-management/label-classifications/classification-about.md) a qualsiasi entità, l&#39;assegnazione di una campagna a un portfolio e l&#39;assegnazione o l&#39;annullamento dell&#39;assegnazione di un vincolo a un portfolio.<!--Link "constraint" to constraint-about.md if that file is ever public -->

   * [!UICONTROL Data Upload]

      * **[!UICONTROL Direct File Upload]**: utilizzato per una versione beta chiusa

      * **[!UICONTROL File Upload to Cloud Storage]**: utilizzato per una versione beta chiusa

   * [!UICONTROL Network Errors]

      * **[!UICONTROL Account Auth Error]**: notifiche per cui Search, Social e Commerce non sono stati in grado di accedere a un account di rete [ad](/help/search-social-commerce/campaign-management/accounts/ad-network-account-about.md) a causa di credenziali non valide o token di autorizzazione non valido o scaduto.

      * **[!UICONTROL Account Missing]**: notifiche per le quali Search, Social e Commerce non dispongono delle credenziali per un account di rete [ad](/help/search-social-commerce/campaign-management/accounts/ad-network-account-about.md).

      * **[!UICONTROL Manager Account Auth Error]**: notifiche che Search, Social e Commerce non sono stati in grado di sincronizzare con un account [ad network manager](/help/search-social-commerce/admin/manager-accounts.md) a causa di credenziali non valide o token di autorizzazione non valido o scaduto.

  <!--
  * [!UICONTROL Setup Errors]
  
    * **[!UICONTROL Adobe Analytics Tracking Setup Error]**: : Notifications that the [!UICONTROL Landing Page Suffix] value is incorrect, missing, or contains an incorrect [AMO ID template](/help/integrations/analytics/ids.md#amo-id-formats); the [!UICONTROL Tracking Template] is incorrect or missing; or the [!UICONTROL Landing Page Suffix] or [!UICONTROL Tracking Template] is overridden at a lower level by an incorrect value. Separate notifications are sent a) for errors at the account level and b) for errors at the campaign and lower levels.
    
    * **[!UICONTROL Manager Account Missing]**: Notifications that Search, Social, & Commerce is missing the credentials for an [ad network manager account](/help/search-social-commerce/admin/manager-accounts.md), which are required for the correct setup of critical functions.
  -->

* [!UICONTROL Insights & Reports]

   * **[!UICONTROL Advertising Insights]**: notifiche di completamento o di errore di [an [!DNL Advertising Insight]](/help/search-social-commerce/advertising-insights/insight-about.md).

   * **[!UICONTROL Custom Alerts]**: notifica che [istanze di avviso](/help/search-social-commerce/alerts/alert-about.md) sono state attivate per un modello di avviso.

   * **[!UICONTROL Reports]**: notifiche di completamento o di errore di un [report personalizzato o pianificato](/help/search-social-commerce/reports/report-about.md).

   * **[!UICONTROL Spreadsheet Feeds]**: notifiche di completamento o di errore di un [feed di foglio di calcolo](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md).

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
>* [Visualizza le notifiche](notification-view.md)
>* [Contrassegna una notifica come letta o non letta](notification-mark-read-unread.md)
>* [Eliminare una notifica](notification-delete.md)
>* [Modifica le impostazioni delle notifiche](notification-edit.md)
>* [Attiva e disattiva le notifiche push da [!UICONTROL Notification Center]](notifications-push-enable-disable.md)
>* [Installa e disinstalla l&#39;applicazione Web [!UICONTROL Notification Center]](notification-app-install-uninstall.md)
