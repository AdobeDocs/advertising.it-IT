---
title: Convalidare le pagine di destinazione in file bulksheet
description: Scopri come convalidare gli URL di destinazione in un file di bulksheet a account singolo.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 0%

---

# Convalidare le pagine di destinazione in file bulksheet

*Account con solo URL di destinazione*

Puoi convalidare le pagine di destinazione in tutti gli URL di destinazione in un file di bulksheet a account singolo. Puoi specificare qualsiasi frase e URL che indichi una pagina non valida e, facoltativamente, segnalare i reindirizzamenti della pagina di destinazione come errori. Search, Social e Commerce verificano le condizioni specificate e le pagine di destinazione mancanti (con conseguente errore HTTP 404 o &quot;Non trovato&quot;).

Quando vengono rilevati errori, in Ricerca, Social e Commerce viene creato un file di errore bulksheet che include tutte le righe del bulksheet originale e messaggi di errore per tutte le righe con pagina di destinazione non valida. Gli errori sono riportati nella [!UICONTROL EF Errors] colonna. La convenzione del nome file è `<bulksheet name>__lpv_errors.<extension used for the bulksheet>`.

Successivamente puoi scaricare il file, correggere gli errori e caricare il file corretto, quindi pubblicare il file corretto sull’account di rete dell’annuncio.

>[!NOTE]
>
>* Questa funzione non convalida i valori nella colonna URL di base/URL finale.
>* È possibile pubblicare i file di bulksheet durante la convalida o anche in caso di errori.


1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Bulksheets]**.

1. Selezionare la casella di controllo accanto a ogni file da convalidare.

1. Nella barra degli strumenti sopra la tabella dati, fai clic su **[!UICONTROL Validate URLs]**.

1. Nella finestra di dialogo immettere le informazioni nei campi e quindi fare clic su **[!UICONTROL Apply]**:

   **[!UICONTROL Enter case-sensitive text or phrases that indicate an invalid page(one per line)]:** Testo nel corpo di una pagina di destinazione che indica che la pagina non è valida. Per specificare più valori, immetterli su righe separate.

   **[!UICONTROL Enter invalid landing pages(one per line):]** Gli URL delle pagine non valide come pagine di destinazione. Per specificare più valori, immetterli su righe separate.

   **[!UICONTROL User Agent:]** Come viene identificato l’agente di convalida della pagina di destinazione nel server web in cui risiede. Il valore predefinito è, che attribuisce le visualizzazioni dell&#39;agente a un anonimo [!DNL Mozilla Firefox] utente. Se il server web blocca le richieste da anonimo [!DNL Mozilla Firefox] utenti, quindi immettere il nome di un agente diverso. Ad esempio, per [!DNL Googlebot], immetti `Googlebot/2.1;+http://www.google.com/bot.html`.

   **[!UICONTROL Report redirects as errors]:** Quando una pagina di destinazione viene reindirizzata a un’altra pagina (ad esempio, se la pagina di destinazione non è presente e il sito visualizza una pagina sostitutiva), il [!UICONTROL ER Errors] nel file di errore della pagina di destinazione indica l’URL a cui viene reindirizzata la pagina di destinazione.

Quando inizia l&#39;attività, viene aggiunta una nuova riga al [!UICONTROL Bulksheets view]. Al momento della creazione del file, viene inviata una notifica e-mail con un collegamento al file. A seconda della quantità di dati compilati, la notifica e-mail potrebbe richiedere alcuni minuti o più. Puoi scaricare il file per modificarlo e quindi ricaricarlo per la pubblicazione, oppure puoi pubblicare il file così com’è. Tuttavia, se la generazione del file non riesce, viene visualizzato un file di errore nella [!UICONTROL Bulksheet Management] e viene inviata una notifica e-mail con un collegamento al file di errore.

>[!NOTE]
>
>* La convalida dei file di grandi dimensioni richiede più tempo.
>* I file di bulksheet per più campagne possono contenere fino a 500.000 righe di dati. Se generi dati per più campagne e i dati combinati sono costituiti da oltre 500.000 righe, i dati vengono suddivisi per campagna in due o più file denominati `<bulksheet name>_1.tsv`, `<bulksheet name>_2.tsv`e così via.


>[!MORELIKETHIS]
>
>* [Informazioni sulla gestione dei dati della campagna tramite bulksheet](bulksheet-about.md)
>* [Elimina i bulksheet caricati e i file di errore](bulksheet-delete.md)
>* [Pubblica i bulksheet o i file di errore corretti](bulksheet-post.md)
>* [Interruzione di un processo di bulksheet in corso](bulksheet-stop-job.md)
>* [Carica un file di bulksheet o un file di errore corretto](bulksheet-upload.md)
>* [Esportare un file bulksheet generato o caricato](bulksheet-export.md)

