---
title: Scaricare dati da una vista di gestione delle campagne
description: Scopri come scaricare i dati dalla maggior parte delle visualizzazioni di gestione delle campagne.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# Scaricare dati da una vista di gestione delle campagne

Puoi scaricare i dati da [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] visualizzazioni ad eccezione di [!UICONTROL Keywords] - [!UICONTROL Keyword Negatives], [!UICONTROL Placements] - [!UICONTROL Placement Negatives], [!UICONTROL Audiences], e [!UICONTROL Extensions] visualizzazioni. Puoi scaricare:

* Un rapporto in [!DNL XLSM] (con attivazione macro) [!DNL Microsoft® Excel] foglio di calcolo). Se si selezionano righe specifiche nella visualizzazione, il rapporto include una riga per ogni riga selezionata. Se non si seleziona alcuna riga, viene creata una riga per ogni riga della visualizzazione.

* Un file di bulksheet in formato TXT che include tutte le entità figlio rilevanti. Se selezioni righe per le entità su più reti di annunci, viene creato un file per ogni rete di annunci rilevante. Se non selezioni alcuna riga, viene creato un file per ogni rete di annunci rappresentata nella vista. I file dei fogli collettivi generati per diverse reti di annunci includono diverse colonne di dati.

   Se generi dati per più campagne e i dati combinati sono costituiti da più di 500.000 righe, i dati vengono ulteriormente suddivisi per campagna in due o più file, a seconda delle necessità, denominati `<bulksheet name>_1.txt`, `<bulksheet name>_2.txt`e così via.

   Ogni file di bulksheet in [!UICONTROL Downloads] Il pannello è inoltre elencato nel [!UICONTROL Bulksheets] visualizzazione. Al momento della creazione del file, si riceve una notifica e-mail con un collegamento da cui è possibile scaricare il file. A seconda della quantità di dati compilati, la notifica potrebbe richiedere alcuni minuti o più. Se, tuttavia, la generazione del file non riesce, nella vista Bulksheet viene visualizzato un file di errore e si riceve una notifica e-mail con un collegamento al file di errore. Eliminazione di un file di bulksheet da [!UICONTROL Download] o il [!UICONTROL Bulksheets] eliminarla da entrambe le posizioni.

1. (Facoltativo) Seleziona singole righe da includere nel file.

   In caso contrario, vengono inclusi tutti i dati nella visualizzazione.

1. A destra della barra degli strumenti, fai clic su ![Download del rapporto](/help/search-social-commerce/assets/download.png "Download del rapporto").

1. Clic ![Crea](/help/search-social-commerce/assets/add.png "Crea") **[!UICONTROL Create]**, se necessario, aggiungi il nome del file e fai clic su **[!UICONTROL Report]** o **[!UICONTROL Bulksheet]**.

1. (Facoltativo) Una volta completato il processo di report, fai clic su ![Download del rapporto](/help/search-social-commerce/assets/download.png "Download del rapporto") per visualizzare [!UICONTROL Available Reports] e quindi scaricare o eliminare il rapporto:

   * Per aprire o salvare il file in base alla normale procedura del browser, fare clic su ![Scarica foglio di calcolo](/help/search-social-commerce/assets/download-spreadsheet.png "Scarica foglio di calcolo").

      Per ulteriori informazioni sulla procedura del browser in uso, consultare la Guida in linea del browser.

   * Per eliminare il file, fare clic su ![Elimina](/help/search-social-commerce/assets/delete.png "Elimina").

>[!MORELIKETHIS]
>
>[Eliminare un report di dati sulle prestazioni o un file di bulksheet dal [!UICONTROL Downloads] menu](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)
