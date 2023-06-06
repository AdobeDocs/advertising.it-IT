---
title: Visualizzare i dati generati dai feed
description: Scopri come visualizzare i dati generati dai feed di dati di inventario.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 0%

---

# Visualizzare i dati generati dai feed

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (solo azioni di eliminazione), e [!DNL Yandex] solo account*

Quando propaghi i dati di feed senza inviarli simultaneamente alla rete di annunci, puoi visualizzare l’anteprima dei dati in uno dei seguenti modi. In seguito puoi facoltativamente [pubblicare dati](propagated-data-post.md) da una località all&#39;altra alle reti pubblicitarie pertinenti.

* Se hai utilizzato l’opzione per &quot;[!UICONTROL Propagate and Preview],&quot; quindi visualizzare il bulksheet generato (denominato &quot;`<feed file name>_<template name>`&quot;) dal [!UICONTROL Bulksheets] visualizzazione. Nessun dato è incluso nel [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], e [!UICONTROL Ads] schede. Questa opzione consente di: [convalidare le pagine di destinazione](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md) associati agli annunci e alle parole chiave prima di pubblicare i dati.

* Se hai utilizzato l’opzione per &quot;[!UICONTROL Propagate only],&quot; quindi visualizzare i dati generati all’interno di una visualizzazione gerarchia di campagne dalla sezione [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], e [!UICONTROL Ads] schede.

   Le viste gerarchiche della campagna mostrano solo i dati generati dal file di feed, non i componenti dell’account esistenti. Dopo che i dati per un componente e tutti i suoi sottocomponenti sono stati pubblicati nella rete di annunci, non vengono più elencati nella vista gerarchica della campagna.

   1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, che apre a [!UICONTROL Templates] scheda.

   1. (Facoltativo) Per mostrare solo i componenti della campagna creati per un modello specifico:

      1. Fai clic sul nome del modello.

      1. In [!UICONTROL Accounts] nel riquadro di navigazione sinistro espandere il nodo di rete dell&#39;annuncio e il nodo dell&#39;account di rete dell&#39;annuncio, quindi selezionare la casella di controllo accanto al nome del modello.
   1. Fai clic su **[!UICONTROL Campaigns]**, **[!UICONTROL Ad Groups]**, **[!UICONTROL Keywords]**, o **[!UICONTROL Ads]** , a seconda dei componenti che desideri visualizzare.

      >[!NOTE]
      >
      >* A meno che non si visualizzino i dati per un modello specifico, [!UICONTROL Ad Groups], [!UICONTROL Keywords], e [!UICONTROL Ads] nelle schede sono elencati tutti i gruppi di annunci, le parole chiave e gli annunci creati da tutti i modelli e i file di feed. Gruppi di prodotti utilizzati per [!DNL Google Ads] gli annunci commerciali sono elencati nella [!UICONTROL Keywords] scheda.
      >* Per visualizzare solo i sottocomponenti di una campagna specifica, inizia visualizzando il [!UICONTROL Campaigns] scheda. Allo stesso modo, per visualizzare solo i sottocomponenti di un gruppo di annunci specifico, inizia visualizzando il [!UICONTROL Ad Groups] scheda.


   1. (Facoltativo) Per visualizzare ulteriori informazioni, effettuate una delle seguenti operazioni:

      * Per visualizzare le impostazioni per qualsiasi campagna, gruppo di annunci, parola chiave o annuncio, fai clic su [Icona Visualizza/Modifica impostazioni](/help/search-social-commerce/assets/settings.png "Icona Visualizza/Modifica impostazioni") accanto al nome.

      * Per visualizzare i sottocomponenti di una campagna o di un gruppo di annunci, effettua le seguenti operazioni:

         * Per elencare tutti i gruppi di annunci di una campagna, fai clic sul nome della campagna.

         * Per elencare tutte le parole chiave o i target di prodotto in un gruppo di annunci, fai clic sul nome del gruppo di annunci.

         * Per elencare tutti gli annunci di un gruppo di annunci, fai clic sul nome del gruppo di annunci, quindi fai clic su [!UICONTROL Ads] scheda.


>[!MORELIKETHIS]
>
>* [Informazioni sui feed di inventario](inventory-feeds-about.md)
>* [Modificare i dati generati dai feed](propagated-data-edit.md)
>* [Pubblicare i dati della campagna generati dai feed nelle reti di annunci](propagated-data-post.md)
>* [Interrompere un processo di registrazione per i dati di feed inventario](stop-job.md)
>* [Stati dei dati generati dai feed](propagated-data-status.md)

