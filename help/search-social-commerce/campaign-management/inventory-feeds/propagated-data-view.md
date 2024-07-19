---
title: Visualizzare i dati generati dai feed
description: Scopri come visualizzare i dati generati dai feed di dati di inventario.
exl-id: ee48f0f1-65fb-4d27-8f59-0108835d70e5
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 0%

---

# Visualizzare i dati generati dai feed

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (elimina solo azioni) e [!DNL Yandex] account solo*

Quando propaghi i dati di feed senza inviarli simultaneamente alla rete di annunci, puoi visualizzare l’anteprima dei dati in uno dei seguenti modi. In seguito puoi [pubblicare dati](propagated-data-post.md) da una delle due posizioni alle reti pubblicitarie pertinenti.

* Se è stata utilizzata l&#39;opzione per &quot;[!UICONTROL Propagate and Preview]&quot;, visualizzare il bulksheet generato (denominato &quot;`<feed file name>_<template name>`&quot;) dalla visualizzazione [!UICONTROL Bulksheets]. Nessun dato incluso nelle schede [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] e [!UICONTROL Ads]. Questa opzione ti consente di [convalidare le pagine di destinazione](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md) associate agli annunci e alle parole chiave prima di pubblicare i dati.

* Se hai utilizzato l&#39;opzione per &quot;[!UICONTROL Propagate only]&quot;, visualizza i dati generati all&#39;interno di una vista gerarchia campagne dalle schede [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] e [!UICONTROL Ads].

  Le viste gerarchiche della campagna mostrano solo i dati generati dal file di feed, non i componenti dell’account esistenti. Dopo che i dati per un componente e tutti i suoi sottocomponenti sono stati pubblicati nella rete di annunci, non vengono più elencati nella vista gerarchica della campagna.

   1. Nel menu principale, fare clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, che consente di aprire la scheda [!UICONTROL Templates].

   1. (Facoltativo) Per mostrare solo i componenti della campagna creati per un modello specifico:

      1. Fai clic sul nome del modello.

      1. Nel menu [!UICONTROL Accounts] nel riquadro di navigazione sinistro, espandere il nodo di rete dell&#39;annuncio e il nodo dell&#39;account di rete dell&#39;annuncio, quindi selezionare la casella di controllo accanto al nome del modello.

   1. Fare clic sulla scheda **[!UICONTROL Campaigns]**, **[!UICONTROL Ad Groups]**, **[!UICONTROL Keywords]** o **[!UICONTROL Ads]**, a seconda dei componenti che si desidera visualizzare.

      >[!NOTE]
      >
      >* A meno che non vengano visualizzati i dati per un modello specifico, le schede [!UICONTROL Ad Groups], [!UICONTROL Keywords] e [!UICONTROL Ads] elencano tutti i gruppi di annunci, le parole chiave e gli annunci creati da tutti i modelli e i file di feed. I gruppi di prodotti utilizzati per [!DNL Google Ads] annunci di acquisto sono elencati nella scheda [!UICONTROL Keywords].
      >* Per visualizzare solo i sottocomponenti di una campagna specifica, iniziare visualizzando la scheda [!UICONTROL Campaigns]. Allo stesso modo, per visualizzare solo i sottocomponenti di uno specifico gruppo di annunci, inizia visualizzando la scheda [!UICONTROL Ad Groups].

   1. (Facoltativo) Per visualizzare ulteriori informazioni, effettuate una delle seguenti operazioni:

      * Per visualizzare le impostazioni per qualsiasi campagna, gruppo di annunci, parola chiave o annuncio, fai clic sull&#39;icona [Visualizza/modifica impostazioni](/help/search-social-commerce/assets/settings.png "Icona Visualizza/Modifica impostazioni") accanto al nome.

      * Per visualizzare i sottocomponenti di una campagna o di un gruppo di annunci, effettua le seguenti operazioni:

         * Per elencare tutti i gruppi di annunci di una campagna, fai clic sul nome della campagna.

         * Per elencare tutte le parole chiave o i target di prodotto in un gruppo di annunci, fai clic sul nome del gruppo di annunci.

         * Per elencare tutti gli annunci di un gruppo di annunci, fare clic sul nome del gruppo di annunci e quindi sulla scheda [!UICONTROL Ads].

>[!MORELIKETHIS]
>
>* [Informazioni sui feed inventario](inventory-feeds-about.md)
>* [Modifica dati generati dai feed](propagated-data-edit.md)
>* [Pubblica i dati della campagna generati dai feed alle reti di annunci](propagated-data-post.md)
>* [Interrompere un processo di registrazione per i dati del feed inventario](stop-job.md)
>* [Stati dei dati generati dai feed](propagated-data-status.md)
