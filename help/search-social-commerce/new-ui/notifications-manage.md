---
title: (Nuova interfaccia) Gestire le notifiche
description: Scopri come visualizzare, configurare e gestire le notifiche Search, Social e Commerce, incluse le notifiche push e l’applicazione web del Centro notifiche.
feature: Search Notifications
source-git-commit: 000ed245b2ea3381e4ca8fcbdd2d6075d50f4b09
workflow-type: tm+mt
source-wordcount: '1710'
ht-degree: 0%

---

# (Nuova interfaccia) Gestire le notifiche

*funzionalità Beta*

Puoi configurare le impostazioni di notifica per abbonarti o annullare l’abbonamento a diversi tipi di avvisi. Puoi visualizzare le notifiche in uno dei seguenti modi:

* Dal pannello [!UICONTROL Notifications], disponibile in alto a destra alle ![Notifiche](/help/search-social-commerce/assets/notifications.png "Notifiche"). Dal pannello puoi filtrare l&#39;elenco, modificare le impostazioni delle notifiche o aprire [!UICONTROL Notification Center].

* Da [!UICONTROL Notification Center], che si apre in una finestra separata al di fuori di Search, Social e Commerce. Per aprire [!UICONTROL Notification Center] dal pannello [!UICONTROL Notifications], fare clic su **[!UICONTROL View All]**.

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

<!-- Update info, and update links to files for new UI once they're available-->

* [!UICONTROL Campaign Management]

   * **[!UICONTROL Bulksheets]**: notifiche relative al completamento o all&#39;errore di un&#39;operazione [bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).<!-- Update link once file for new UI available-->

   * **[!UICONTROL Manager Account Missing]**: notifiche per le quali Search, Social e Commerce non dispongono delle credenziali per un account [ad network manager](/help/search-social-commerce/admin/manager-accounts.md), necessarie per la corretta configurazione delle funzioni critiche.<!-- Moving to Campaign Management > Setup Errors at some point -->

   * **[!UICONTROL UI Actions]**: notifica del completamento o dell&#39;errore dei processi eseguiti in background. I tipi di processo includono [processi bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)<!-- Update link once file for new UI available-->, processi di modifica in blocco all&#39;interno della tabella dati o utilizzando la barra degli strumenti, processi di assegnazione di entità o altre azioni all&#39;interno dell&#39;interfaccia utente (ad esempio la sincronizzazione con reti di annunci, l&#39;incollamento di righe o la ridenominazione di entità). Le assegnazioni di entità includono l&#39;assegnazione o l&#39;annullamento dell&#39;assegnazione di un valore di classificazione [etichetta](/help/search-social-commerce/new-ui/reports/label-classifications-manage.md) a qualsiasi entità, l&#39;assegnazione di una campagna a un portfolio e l&#39;assegnazione o l&#39;annullamento dell&#39;assegnazione di un vincolo a un portfolio.

   * [!UICONTROL Data Upload]

      * **[!UICONTROL Direct File Upload]**: notifiche di caricamento di un file di dati dell&#39;account o di un caricamento di dati dell&#39;account non riuscito tramite [caricamento manuale dei dati dell&#39;account](/help/search-social-commerce/new-ui/set-up/accounts/data-upload-accounts/upload-account-data.md). <!-- Verify description-->

      * **[!UICONTROL File Upload to Cloud Storage]**: notifiche di caricamento di un file di dati dell&#39;account o di un caricamento di dati dell&#39;account non riuscito tramite [caricamento di dati dell&#39;account in un bucket [!DNL Amazon] [!DNL S3]](/help/search-social-commerce/new-ui/set-up/accounts/data-upload-accounts/upload-account-data.md). <!-- Verify description-->

   * [!UICONTROL Network Errors]

      * **[!UICONTROL Account Auth Error]**: notifiche per cui Search, Social e Commerce non sono stati in grado di accedere a un account di rete [ad](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md) a causa di credenziali non valide o token di autorizzazione non valido o scaduto.

      * **[!UICONTROL Account Missing]**: notifiche per le quali Search, Social e Commerce non dispongono delle credenziali per un account di rete [ad](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md).

      * **[!UICONTROL Manager Account Auth Error]**: notifiche che Search, Social e Commerce non sono stati in grado di sincronizzare con un account [ad network manager](/help/search-social-commerce/admin/manager-accounts.md) a causa di credenziali non valide o di un token di autorizzazione non valido o scaduto.<!-- Update link once file for new UI available-->

* [!UICONTROL Insights & Reports]

   * **[!UICONTROL Advertising Insights]**: notifiche di completamento o di errore di [an [!DNL Advertising Insight]](/help/search-social-commerce/advertising-insights/insight-about.md).

   * **[!UICONTROL Custom Alerts]**: notifica che [istanze di avviso](/help/search-social-commerce/new-ui/alerts-manage.md) sono state attivate per un modello di avviso.

   * **[!UICONTROL Spreadsheet Feeds]**: notifiche di completamento o di errore di un [feed di foglio di calcolo](/help/search-social-commerce/new-ui/reports/spreadsheet-feeds-manage.md).

   * [!UICONTROL Reports]

      * **[!UICONTROL Grid Reports]**: notifica del completamento o dell&#39;errore di un report di visualizzazione dati da una visualizzazione specifica (ad esempio il contenuto della tabella dati nella visualizzazione [!UICONTROL Camapigns]).

      * **[!UICONTROL Reports]**: notifiche di completamento o di errore di un [report personalizzato o pianificato](/help/search-social-commerce/new-ui/reports/management/report-manage.md).

   * [!UICONTROL Portfolio Management]

      * **[!UICONTROL Intraday Optimization]**: notifiche quando l&#39;ottimizzazione infragiornaliera è disabilitata.

      * **[!UICONTROL Simulation Report]**: notifiche relative a [processi di simulazione](/help/search-social-commerce/new-ui/plan/simulations/simulation-about.md).

      * [!UICONTROL Objective & Conversion Configuration]

         * **[!UICONTROL Auto Assign Campaign Conversion Goal - Advertiser Level]**: notifiche a livello di inserzionista relative all&#39;assegnazione automatica degli obiettivi di conversione della campagna riuscita e non riuscita.

         * **[!UICONTROL Auto Assign Campaign Conversion Goal - Portfolio Level]**: notifiche a livello di portfolio sull&#39;assegnazione automatica degli obiettivi di conversione della campagna riuscita e non riuscita.

      * [!UICONTROL Portfolios]

         * **[!UICONTROL Portfolio Bulksheet Diagnostic Report]**: notifiche relative a [processi di modifica in blocco del portfolio tramite bulksheet](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-bulksheets.md).

         * **[!UICONTROL Portfolio Settings]**: notifiche su [modifiche alle impostazioni del portfolio](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-settings.md).

<!--

In Campaign Management:

  * [!UICONTROL Setup Errors]

    * **[!UICONTROL Adobe Analytics Tracking Setup Error]**: Notifications that an account-level landing page suffix is incorrect due to missing or incorrect [AMO ID (`s_kwcid` parameter)](/help/integrations/analytics/ids.md).
  
    * **[!UICONTROL Manager Account Missing]**: Notifications that Search, Social, & Commerce is missing the credentials for an [ad network manager account](/help/search-social-commerce/admin/manager-accounts.md), which are required for the correct setup of critical functions.

-->

<!--
* [!UICONTROL Optimization]

  * **[!UICONTROL Accuracy]**: Notifications when a portfolio's model accuracy deviates [by how much?] from expectations.
-->


## Azioni disponibili

* [Visualizzare le notifiche](#notification-view)

* [Modifica le impostazioni delle notifiche](#notification-edit)

* [Contrassegnare una notifica come letta o non letta](#notification-mark-read-unread)

* [Eliminare una notifica](#notification-delete)

* [Abilitare e disabilitare le notifiche push](#notification-push-enable-disable)

* [Installa e disinstalla l&#39;applicazione Web [!UICONTROL Notification Center]](#notification-app-install-uninstall)

## Visualizzare le notifiche {#notification-view}

Quando sei [abbonato a notifiche](#notification-edit) relative a errori di autenticazione dell&#39;account, avvisi personalizzati attivati e [!UICONTROL Advertising Insights] generati, puoi visualizzare le notifiche nel pannello [!UICONTROL Notifications] o in [!UICONTROL Notification Center].

### Visualizza notifiche nel pannello [!UICONTROL Notifications]

1. In alto a destra, fai clic su ![Notifiche](/help/search-social-commerce/assets/notifications.png "Notifiche").

1. (Facoltativo) Effettuate una delle seguenti operazioni:

   * Per visualizzare i dettagli di qualsiasi notifica, fai clic sul nome della notifica.

     In alcune notifiche, la sezione [!UICONTROL Action Recommended] può includere un collegamento che apre una visualizzazione filtrata delle entità interessate o responsabili.

   * Per contrassegnare una notifica come *letta* o *non letta*, posizionare il cursore sul nome dell&#39;avviso e fare clic su ![Segna come letta o da leggere](/help/search-social-commerce/assets/notifications-read-unread.png "Segna come letta o da leggere").

     Le notifiche contrassegnate come *lette* sono in un testo di colore più chiaro ma rimangono disponibili fino a quando non vengono eliminate.

     ![Notifiche lette e non lette](/help/search-social-commerce/assets/notifications-read-vs-unread.png "Notifiche lette e non lette")

   * Per modificare le preferenze dell&#39;abbonamento per il tipo di notifica, fare clic su ![Impostazioni](/help/search-social-commerce/assets/settings-nc.png "Impostazioni") accanto alla notifica, modificare le impostazioni e quindi fare clic su **[!UICONTROL Save]**.

   * Per eliminare una notifica, fare clic su ![Elimina](/help/search-social-commerce/assets/delete.png "Elimina") accanto alla notifica.

   * Per aprire [!UICONTROL Notification Center], fare clic su **[!UICONTROL View All]**.

### Visualizza notifiche in [!UICONTROL Notification Center]

1. In alto a destra, fai clic su ![Notifiche](/help/search-social-commerce/assets/notifications.png "Notifiche").

1. Fare clic su **[!UICONTROL View All]**.

1. (Facoltativo) Per filtrare le notifiche per tipo, fare clic su *[!UICONTROL Notices], [!UICONTROL Recommendations], [!UICONTROL Warnings] o[!UICONTROL Issues]*.

1. (Facoltativo) Effettuate una delle seguenti operazioni:

   * Per visualizzare i dettagli di qualsiasi notifica, fai clic sul nome della notifica.

     In alcune notifiche, la sezione [!UICONTROL Action Recommended] può includere un collegamento che apre una visualizzazione filtrata delle entità interessate o responsabili.

   * Per contrassegnare una notifica come *letta* o *non letta*, posizionare il cursore sul nome dell&#39;avviso e fare clic su ![Segna come letta o da leggere](/help/search-social-commerce/assets/notifications-read-unread.png "Segna come letta o da leggere").

     Le notifiche contrassegnate come *lette* sono in un testo di colore più chiaro ma rimangono disponibili fino a quando non vengono eliminate.

   * Per modificare le preferenze dell&#39;abbonamento per il tipo di notifica, fare clic su ![Impostazioni](/help/search-social-commerce/assets/settings-nc.png "Impostazioni") accanto alla notifica, modificare le impostazioni e quindi fare clic su **[!UICONTROL Save]**.

   * Per eliminare una notifica, fare clic su ![Elimina](/help/search-social-commerce/assets/delete.png "Elimina") accanto alla notifica.

## Modifica le impostazioni delle notifiche {#notification-edit}

È possibile sottoscrivere o annullare l&#39;abbonamento a notifiche e-mail e Web relative a errori di autenticazione dell&#39;account, a tutti gli avvisi personalizzati attivati e al completamento di [!UICONTROL Advertising Insights] generato.

1. Apri le impostazioni di notifica in uno dei seguenti modi:

   * In alto a destra, fai clic su ![Notifiche](/help/search-social-commerce/assets/notifications.png "Notifiche") per aprire il pannello [!UICONTROL Notifications]. In alto a destra, fare clic su ![Impostazioni](/help/search-social-commerce/assets/settings-nc.png "Impostazioni").

   * In alto a destra di qualsiasi pagina, fai clic su ![Notifiche](/help/search-social-commerce/assets/notifications.png "Notifiche"), fai clic su **[!UICONTROL View All]** per aprire [!UICONTROL Notification Center], quindi fai clic su ![Impostazioni](/help/search-social-commerce/assets/settings-nc.png "Impostazioni") nel menu a sinistra.

1. Modifica le impostazioni per qualsiasi categoria di notifica elencata sopra:

   * Per sottoscrivere o annullare l&#39;abbonamento alle notifiche, spostare il dispositivo di scorrimento nella colonna [!UICONTROL Subscribe]:

      * Per annullare l’abbonamento a tutti i tipi di notifica, sposta il cursore a sinistra (disattivato).

      * Per iscriversi a uno o più tipi di notifica, spostare il dispositivo di scorrimento verso destra (attivato).

   * (Quando [!UICONTROL Subscribe] è abilitato) Per sottoscrivere le notifiche e-mail, selezionare la casella di controllo nella colonna **[!UICONTROL Email]**.

   * (Se [!UICONTROL Subscribe] è disabilitato) Per sottoscrivere le notifiche Web in Search, Social e Commerce e le notifiche push se sono abilitate per il browser, selezionare la casella di controllo nella colonna **[!UICONTROL Web]**.

     Le notifiche Web vengono inviate solo quando [abiliti le notifiche push](#notification-push-enable-disable) nel browser.

1. Fare clic su **[!UICONTROL Save]**.

## Contrassegnare una notifica come letta o non letta {#notification-mark-read-unread}

Se si contrassegna una notifica come *letta* o *non letta*, verrà modificato il numero di notifiche non lette indicato nel collegamento [!UICONTROL Notifications] nella parte superiore di ogni pagina, ad esempio ![icona Notifiche con contatore notifiche non lette](/help/search-social-commerce/assets/notifications-unread.png "icona Notifiche con contatore notifiche non lette").

Le notifiche contrassegnate come *lette* sono in un testo di colore più chiaro ma rimangono disponibili fino a quando non vengono eliminate.

![Notifiche lette e non lette](/help/search-social-commerce/assets/notifications-read-vs-unread.png "Notifiche lette e non lette")

1. [Aprire il pannello Notifiche o il Centro notifiche](#notification-view).

1. Posizionare il cursore sul nome dell&#39;avviso e fare clic su ![Segna come letto o da leggere](/help/search-social-commerce/assets/notifications-read-unread.png "Segna come letto o da leggere").

## Eliminare una notifica {#notification-delete}

### Elimina una notifica nel pannello [!UICONTROL Notifications]

1. In alto a destra, fai clic su ![Notifiche](/help/search-social-commerce/assets/notifications.png "Notifiche").

1. Fai clic su ![Elimina](/help/search-social-commerce/assets/delete.png "Elimina") accanto alla notifica.

### Eliminare una notifica entro [!UICONTROL Notification Center]

1. In alto a destra, fai clic su ![Notifiche](/help/search-social-commerce/assets/notifications.png "Notifiche").

1. Fare clic su **[!UICONTROL View All]**.

1. (Facoltativo) Per filtrare le notifiche per tipo, fare clic su *[!UICONTROL Notices]*, *[!UICONTROL Recommendations]*, *[!UICONTROL Warnings]* o *[!UICONTROL Issues]*.

1. Fai clic su ![Elimina](/help/search-social-commerce/assets/delete.png "Elimina") accanto alla notifica.

## Abilitare e disabilitare le notifiche push {#notification-push-enable-disable}

Puoi abilitare le notifiche in Search, Social e Commerce, dove vengono visualizzate in base alle convenzioni di notifica del browser. Sui dispositivi che utilizzano [!DNL Microsoft Windows], le notifiche vengono visualizzate in basso a destra dello schermo (area di notifica). Sui dispositivi [!DNL Apple Mac], le notifiche vengono visualizzate nel menu di destra.

Le notifiche push sono disponibili nei seguenti browser:

* [!DNL Google Chrome] 40 e versioni successive

* [!DNL Microsoft Edge] 17 e versioni successive

* [!DNL Mozilla Firefox] 44 e versioni successive

Puoi disattivare le notifiche push in base alla procedura standard del browser.

### Abilitare le notifiche push

1. In alto a destra, fai clic su ![Notifiche](/help/search-social-commerce/assets/notifications.png "Notifiche").

1. Fare clic su **[!UICONTROL View All]**.

1. In basso a destra, fai clic su ![Abilita notifiche push](/help/search-social-commerce/assets/notifications-push.png "Abilita notifiche push").

1. Nel messaggio di conferma, fare clic su **[!UICONTROL Enable]**.

1. Configurare il browser per consentire le notifiche da [!UICONTROL Notification Center] alle `https://alert-center-ui-na.efrontier.com`.

   Le impostazioni di notifica predefinite variano a seconda del browser e può essere necessario a) visualizzare automaticamente l&#39;opzione per consentire le notifiche da [!UICONTROL Notification Center] oppure b) gestire manualmente le impostazioni di notifica. In [!DNL Microsoft Edge], ad esempio, è possibile consentire le notifiche da [!UICONTROL Notification Center] dalla barra degli strumenti del browser. Consulta le istruzioni nella guida del browser.

   ![Dove gestire le impostazioni di notifica in Microsoft Edge](/help/search-social-commerce/assets/notifications-blocked-dialog.png "Dove gestire le impostazioni di notifica in Microsoft Edge")

1. Nelle [impostazioni di notifica](#notification-edit), abilita [!UICONTROL Web] notifiche per i tipi di avviso che desideri inviare.

### Disattiva notifiche push

Rimuovi le notifiche da `https://alert-center-ui-na.efrontier.com` nel gestore notifiche del browser. In [!DNL Google Chrome], ad esempio, è possibile rimuovere o bloccare le notifiche dai siti specificati in `chrome://settings/content/notifications`.

Consulta le istruzioni nella guida del browser.

## Installa e disinstalla l&#39;applicazione Web [!UICONTROL Notification Center] {#notification-app-install-uninstall}

È possibile ricevere e gestire le notifiche all&#39;esterno del browser installando un&#39;applicazione Web [!UICONTROL Notification Center]. L&#39;aspetto e le funzionalità dell&#39;applicazione sono uguali a quelli di [!UICONTROL Notification Center] in Search, Social e Commerce. L&#39;applicazione è disponibile per [!DNL Google Chrome] 40 e versioni successive o [!DNL Microsoft Edge] 17 e versioni successive.

Dopo l&#39;installazione, l&#39;applicazione [!UICONTROL Notification Center] viene automaticamente abilitata nella gestione applicazioni del browser e viene caricata come una finestra separata il cui layout è disposto in modo dinamico in base alle dimensioni della finestra. È possibile aprire e chiudere l&#39;applicazione dalla gestione delle applicazioni del browser oppure fissarla alla barra delle applicazioni o all&#39;ancoraggio del sistema operativo. L’applicazione viene aggiornata automaticamente.

![Icona Centro notifiche nella barra delle applicazioni di Microsoft Windows](/help/search-social-commerce/assets/windows-taskbar.png "Icona Centro notifiche nella barra delle applicazioni di Microsoft Windows")

È possibile disabilitare o disinstallare l&#39;applicazione dalla gestione delle applicazioni del browser. Per ulteriori informazioni sulla gestione delle applicazioni web, consulta la guida del browser.

### Installa l&#39;applicazione Web [!UICONTROL Notification Center] per [!DNL Google Chrome]

1. In alto a destra, fai clic su ![Notifiche](/help/search-social-commerce/assets/notifications.png "Notifiche").

1. Fare clic su **[!UICONTROL View All]**.

1. In basso a destra, fai clic su ![Installa l&#39;app Web del Centro notifiche](/help/search-social-commerce/assets/notifications-install-app.png "Installa l&#39;app Web del Centro notifiche").

1. Nel messaggio di conferma, fare clic su **[!UICONTROL Add]**.

1. Nell’app di installazione? messaggio, fare clic su **[!UICONTROL Install]**.

### Installa l&#39;applicazione Web [!UICONTROL Notification Center] per [!DNL Microsoft Edge]

* Dall’interno di Search, Social e Commerce:

   1. In alto a destra, fai clic su ![Notifiche](/help/search-social-commerce/assets/notifications.png "Notifiche").

   1. Fare clic su **[!UICONTROL View All]**.

   1. In basso a destra, fai clic su ![Installa l&#39;app Web del Centro notifiche](/help/search-social-commerce/assets/notifications-install-app.png "Installa l&#39;app Web del Centro notifiche").

   1. Nel messaggio di conferma, fare clic su **[!UICONTROL Add]**.

   1. Nel messaggio dell&#39;app [!UICONTROL Install Notification Center], fai clic su **[!UICONTROL Install]**.

* Dal menu principale [!DNL Edge]:

   1. Nella barra degli strumenti del browser, fare clic su **...** > **[!UICONTROL Apps]** > **[!UICONTROL Install Notification Center]**.

   1. Nel messaggio dell&#39;app [!UICONTROL Install Notification Center], fai clic su **[!UICONTROL Install]**.

### Disinstalla l&#39;applicazione Web [!UICONTROL Notification Center] per [!DNL Google Chrome]

* In [!DNL Chrome], passare a `chrome://apps`, fare clic con il pulsante destro del mouse su **[!UICONTROL notification-center]** e quindi scegliere **[!UICONTROL Remove from Chrome]**.

### Disinstalla l&#39;applicazione Web [!UICONTROL Notification Center] per [!DNL Microsoft Edge]

1. Nella barra degli strumenti del browser [!DNL Edge], fare clic su **...** > **[!UICONTROL Apps]** > **[!UICONTROL Manage apps]**. In alternativa, passare a `edge://apps`.

1. Fare clic con il pulsante destro del mouse su **[!UICONTROL Notification Center]** e scegliere **[!UICONTROL Uninstall]**.
