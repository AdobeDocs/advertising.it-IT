---
title: Convalidare le pagine di destinazione in file bulksheet
description: Scopri come convalidare gli URL di destinazione in un file di bulksheet a account singolo.
exl-id: 191cb1bc-54a9-4c6c-a29c-f3cbae08e0d8
feature: Search Bulksheets
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 0%

---

# Convalidare le pagine di destinazione in file bulksheet

*Account con solo URL di destinazione*

Puoi convalidare le pagine di destinazione in tutti gli URL di destinazione in un file di bulksheet a account singolo. Puoi specificare qualsiasi frase e URL che indichi una pagina non valida e, facoltativamente, segnalare i reindirizzamenti della pagina di destinazione come errori. Search, Social e Commerce verificano le condizioni specificate e le pagine di destinazione mancanti (con conseguente errore HTTP 404 o &quot;Non trovato&quot;).

Quando vengono rilevati errori, in Ricerca, Social e Commerce viene creato un file di errore bulksheet che include tutte le righe del bulksheet originale e messaggi di errore per tutte le righe con pagina di destinazione non valida. Gli errori sono riportati nella colonna [!UICONTROL EF Errors]. Convenzione nome file: `<bulksheet name>__lpv_errors.<extension used for the bulksheet>`.

Successivamente puoi scaricare il file, correggere gli errori e caricare il file corretto, quindi pubblicare il file corretto sull’account di rete dell’annuncio.

>[!NOTE]
>
>* Questa funzione non convalida i valori nella colonna URL di base/URL finale.
>* È possibile pubblicare i file di bulksheet durante la convalida o anche in caso di errori.

1. Nel menu principale, fare clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Bulksheets]**.

1. Selezionare la casella di controllo accanto a ogni file da convalidare.

1. Nella barra degli strumenti sopra la tabella dati, fare clic su **[!UICONTROL Validate URLs]**.

1. Nella finestra di dialogo immettere le informazioni nei campi, quindi fare clic su **[!UICONTROL Apply]**:

   **[!UICONTROL Enter case-sensitive text or phrases that indicate an invalid page(one per line)]:** Testo nel corpo di una pagina di destinazione che indica che la pagina non è valida. Per specificare più valori, immetterli su righe separate.

   **[!UICONTROL Enter invalid landing pages(one per line):]** URL di pagine non valide come pagine di destinazione. Per specificare più valori, immetterli su righe separate.

   **[!UICONTROL User Agent:]** Identificazione dell&#39;agente di convalida della pagina di destinazione nel server Web in cui si trova la pagina di destinazione. L&#39;impostazione predefinita attribuisce le visualizzazioni dell&#39;agente a un utente anonimo [!DNL Mozilla Firefox]. Se il server Web blocca le richieste di [!DNL Mozilla Firefox] utenti anonimi, immettere il nome di un agente diverso. Ad esempio, per [!DNL Googlebot], immettere `Googlebot/2.1;+http://www.google.com/bot.html`.

   **[!UICONTROL Report redirects as errors]:** Quando una pagina di destinazione viene reindirizzata a un&#39;altra pagina (ad esempio, se la pagina di destinazione risulta mancante e il sito visualizza una pagina sostitutiva), la colonna [!UICONTROL ER Errors] nel file di errore della pagina di destinazione indica l&#39;URL a cui viene reindirizzata la pagina di destinazione.

Quando inizia l&#39;attività, viene aggiunta una nuova riga a [!UICONTROL Bulksheets view]. Al momento della creazione del file, viene inviata una notifica e-mail con un collegamento al file. A seconda della quantità di dati compilati, la notifica e-mail potrebbe richiedere alcuni minuti o più. Puoi scaricare il file per modificarlo e quindi ricaricarlo per la pubblicazione, oppure puoi pubblicare il file così com’è. Se tuttavia la generazione del file non riesce, nella pagina [!UICONTROL Bulksheet Management] viene elencato un file di errore e viene inviata una notifica e-mail con un collegamento al file di errore.

>[!NOTE]
>
>* La convalida dei file di grandi dimensioni richiede più tempo.
>* I file di bulksheet per più campagne possono contenere fino a 500.000 righe di dati. Se si generano dati per più campagne e i dati combinati sono costituiti da oltre 500.000 righe, i dati vengono suddivisi per campagna in due o più file denominati `<bulksheet name>_1.tsv`, `<bulksheet name>_2.tsv` e così via.

>[!MORELIKETHIS]
>
>* [Informazioni sulla gestione dei dati della campagna tramite bulksheet](bulksheet-about.md)
>* [Elimina i bulksheet caricati e i file di errore](bulksheet-delete.md)
>* [Pubblica bulksheet o file di errore corretti](bulksheet-post.md)
>* [Interruzione di un processo bulksheet in corso](bulksheet-stop-job.md)
>* [Caricare un bulksheet o correggere un file di errore](bulksheet-upload.md)
>* [Esporta un file bulksheet generato o caricato](bulksheet-export.md)
