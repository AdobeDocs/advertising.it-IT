---
title: Scaricare dati da una vista di gestione delle campagne
description: Scopri come scaricare i dati dalla maggior parte delle visualizzazioni di gestione delle campagne.
exl-id: f549f03c-ed0b-4d7d-8d7e-91192c17e77e
feature: Search Common Tasks
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---

# Scaricare dati da una vista di gestione delle campagne

È possibile scaricare i dati dalle viste [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] ad eccezione delle viste [!UICONTROL Keywords] - [!UICONTROL Keyword Negatives], [!UICONTROL Placements] - [!UICONTROL Placement Negatives], [!UICONTROL Audiences] e [!UICONTROL Extensions]. Puoi scaricare:

* Un report in formato [!DNL XLSM] (foglio di calcolo [!DNL Microsoft Excel] con attivazione macro). Se si selezionano righe specifiche nella visualizzazione, il rapporto include una riga per ogni riga selezionata. Se non si seleziona alcuna riga, viene creata una riga per ogni riga della visualizzazione.

* Un file di bulksheet in formato TXT che include tutte le entità figlio rilevanti. Se selezioni righe per le entità su più reti di annunci, viene creato un file per ogni rete di annunci rilevante. Se non selezioni alcuna riga, viene creato un file per ogni rete di annunci rappresentata nella vista. I file dei fogli collettivi generati per diverse reti di annunci includono diverse colonne di dati.

  Se generi dati per più campagne e i dati combinati sono costituiti da oltre 500.000 righe, i dati vengono ulteriormente suddivisi per campagna in due o più file, a seconda delle necessità, denominati `<bulksheet name>_1.txt`, `<bulksheet name>_2.txt` e così via.

  Ogni file di bulksheet nel pannello [!UICONTROL Downloads] è elencato anche nella visualizzazione [!UICONTROL Bulksheets]. Al momento della creazione del file, si riceve una notifica e-mail con un collegamento da cui è possibile scaricare il file. A seconda della quantità di dati compilati, la notifica potrebbe richiedere alcuni minuti o più. Se, tuttavia, la generazione del file non riesce, nella vista Bulksheet viene visualizzato un file di errore e si riceve una notifica e-mail con un collegamento al file di errore. L&#39;eliminazione di un file di bulksheet dal pannello [!UICONTROL Download] o dalla scheda [!UICONTROL Bulksheets] comporta l&#39;eliminazione da entrambi i percorsi.

1. (Facoltativo) Seleziona singole righe da includere nel file.

   In caso contrario, vengono inclusi tutti i dati nella visualizzazione.

1. Sulla destra della barra degli strumenti, fai clic su ![Download report](/help/search-social-commerce/assets/download.png "Download report").

1. Fare clic su ![Crea](/help/search-social-commerce/assets/add.png "Crea") **[!UICONTROL Create]**, aggiungere facoltativamente il nome del file e quindi fare clic su **[!UICONTROL Report]** o **[!UICONTROL Bulksheet]**.

1. (Facoltativo) Una volta completato il processo di report, fai clic su ![Download report](/help/search-social-commerce/assets/download.png "Download report") per visualizzare il pannello [!UICONTROL Available Reports], quindi scarica o elimina il report:

   * Per aprire o salvare il file in base alla normale procedura del browser, fare clic su ![Scarica foglio di calcolo](/help/search-social-commerce/assets/download-spreadsheet.png "Scarica foglio di calcolo").

     Per ulteriori informazioni sulla procedura del browser in uso, consultare la Guida in linea del browser.

   * Per eliminare il file, fare clic su ![Elimina](/help/search-social-commerce/assets/delete.png "Elimina").

>[!MORELIKETHIS]
>
>[Eliminare un report di dati sulle prestazioni o un file di bulksheet dal menu [!UICONTROL Downloads]](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)
