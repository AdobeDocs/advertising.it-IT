---
title: Modificare i dati generati dai feed
description: Scopri come modificare i dati generati dai feed di dati di inventario.
exl-id: d43b593d-758d-4561-9cda-33b235099cc6
feature: Search Inventory Feeds
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 0%

---

# Modificare i dati generati dai feed

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (elimina solo azioni) e [!DNL Yandex] account solo*

Quando propaghi i dati di feed senza inviarli simultaneamente alla rete di annunci, puoi modificarli in uno dei seguenti modi. In seguito puoi [pubblicare dati](propagated-data-post.md) da una delle due posizioni alle reti pubblicitarie pertinenti:

* Se è stata utilizzata l&#39;opzione &quot;[!UICONTROL Propagate and Preview]&quot;, è possibile modificare il file del bulksheet generato (denominato &quot;`<feed file name>_<template name>`&quot;) scaricandolo dalla visualizzazione [!UICONTROL Bulksheets], modificandolo e caricandolo nuovamente. Nessun dato incluso nelle schede [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] e [!UICONTROL Ads].

* Se hai utilizzato l&#39;opzione per &quot;[!UICONTROL Propagate only]&quot;, puoi modificare i dati generati per i componenti con lo stato [[!UICONTROL New]](propagated-data-status.md) all&#39;interno di una visualizzazione gerarchia campagne dalle schede [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] e [!UICONTROL Ads].

  Le viste gerarchiche della campagna mostrano solo i dati generati dal file di feed, non i componenti dell’account esistenti. Una volta che i dati per un componente e tutti i suoi sottocomponenti sono pubblicati nella rete di annunci, non vengono più elencati nella gerarchia della campagna.

   1. Nel menu principale, fare clic su **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, che consente di aprire la scheda [!UICONTROL Templates].

   1. (Facoltativo) Per mostrare solo i componenti della campagna creati per un modello specifico:

      1. Fai clic sul nome del modello.

      1. Nel menu [!UICONTROL Accounts] nel riquadro di navigazione sinistro, espandere il nodo di rete dell&#39;annuncio e il nodo dell&#39;account di rete dell&#39;annuncio, quindi selezionare la casella di controllo accanto al nome del modello.

   1. Fare clic sulla scheda **[!UICONTROL Campaigns]**, **[!UICONTROL Ad Groups]**, **[!UICONTROL Keywords]** o **[!UICONTROL Ads]**, a seconda dei componenti che si desidera visualizzare.

      >[!NOTE]
      >
      >* A meno che non vengano visualizzati i dati per un modello specifico, le schede [!UICONTROL Ad Groups], [!UICONTROL Keywords] e [!UICONTROL Ads] elencano tutti i gruppi di annunci, le parole chiave e gli annunci creati da tutti i modelli e i file di feed. I gruppi di prodotti utilizzati per [!DNL Google Ads] annunci di acquisto sono elencati nella scheda [!UICONTROL Keywords].
      >* Per visualizzare solo i sottocomponenti di una campagna specifica, iniziare visualizzando la scheda [!UICONTROL Campaigns]. Allo stesso modo, per visualizzare solo i sottocomponenti di uno specifico gruppo di annunci, inizia visualizzando la scheda [!UICONTROL Ad Groups].

   1. (Facoltativo; per modificare gruppi di annunci, parole chiave o solo annunci) Filtra l’elenco in modo da includere solo i sottocomponenti di una campagna o di un gruppo di annunci specifico:

      * Per elencare tutti i gruppi di annunci di una campagna, fai clic sul nome della campagna.

      * Per elencare tutte le parole chiave di un gruppo di annunci, fai clic sul nome del gruppo di annunci.

      * Per elencare tutti gli annunci come in un gruppo di annunci, fare clic sul nome del gruppo di annunci e quindi sulla scheda [!UICONTROL Ads].

   1. Fai clic sull&#39;icona [Visualizza/modifica impostazioni](/help/search-social-commerce/assets/settings.png "Icona Visualizza/Modifica impostazioni") accanto alla campagna, al gruppo di annunci, alla parola chiave o al nome dell&#39;annuncio.

   1. Modificare le impostazioni e quindi fare clic su **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Informazioni sui feed inventario](inventory-feeds-about.md)
>* [Visualizza dati generati dai feed](propagated-data-view.md)
>* [Pubblica i dati della campagna generati dai feed alle reti di annunci](propagated-data-post.md)
>* [Interrompere un processo di registrazione per i dati del feed inventario](stop-job.md)
>* [Stati dei dati generati dai feed](propagated-data-status.md)
