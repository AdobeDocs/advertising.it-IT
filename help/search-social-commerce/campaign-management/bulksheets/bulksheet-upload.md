---
title: Carica un file di bulksheet o un file di errore corretto
description: Scopri come caricare manualmente un file bulksheet o un file di errore di convalida della pagina di destinazione corretto.
exl-id: 44c76ca3-1d3e-43c2-868a-4868157d32b0
feature: Search Bulksheets
source-git-commit: e5102132a1e4ce25adb297f863db439b583b3ebe
workflow-type: tm+mt
source-wordcount: '800'
ht-degree: 0%

---

# Carica un file di bulksheet o un file di errore corretto

Puoi caricare file bulksheet, file di errore di convalida della pagina di destinazione corretti e altri file di errore corretti dal dispositivo o dalla rete per [reti pubblicitarie supportate](bulksheet-about.md#bulksheet-functionality-by-network). Tutte le colonne personalizzate nel file vengono eliminate quando caricate il file.

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Bulksheets]**.

1. Nella barra degli strumenti sopra la tabella dati, fai clic su **[!UICONTROL Upload Bulksheet]**.

1. Immettere o selezionare le informazioni in [[!UICONTROL Upload Bulksheet] impostazioni](#bulksheet-upload-settings).

1. Clic **[!UICONTROL Apply]**.

Quando inizia l’attività, il file viene elencato nella sezione [!UICONTROL Bulksheets] visualizzazione. Una volta completato il file, viene inviata una notifica e-mail con un collegamento al file. A seconda della quantità di dati compilati, la notifica e-mail potrebbe richiedere alcuni minuti o più. Tuttavia, se la generazione del file non riesce, viene visualizzato un file di errore nella [!UICONTROL Bulksheets] e viene inviata una notifica e-mail con un collegamento al file di errore.

>[!NOTE]
>
>Se pubblichi i dati del bulksheet nella rete di annunci, puoi seguire l’avanzamento del file in [!UICONTROL Progress] colonna nella [!UICONTROL Bulksheets] visualizzazione. La pubblicazione di grandi quantità di dati richiede più tempo.

## Impostazioni di caricamento per i bulksheet e i file di errore corretti {#bulksheet-upload-settings}

| Parametro | Descrizione |
|----|----|
| [!UICONTROL File to Upload] | Il file da caricare. Specificare il file immettendo il percorso completo e il nome del file oppure facendo clic su <b>[!UICONTROL Browse]</b> per individuare il file sul dispositivo o sulla rete.<br><br>I file di bulksheet possono avere una dimensione massima di 2,5 GB (circa 2,5 milioni di righe) e devono avere una delle seguenti estensioni: <i>[!UICONTROL .tsv]</i> (per valori separati da tabulazioni), <i>[!UICONTROL .txt]</i> (per testo ASCII conforme a Unicode), <i>[!UICONTROL .csv]</i> (per valori separati da virgola), oppure <i>[!UICONTROL .zip]</i> (per il formato ZIP compresso, che si decomprime in un file TSV). Il nome del file non può includere i seguenti caratteri: `# % &amp; * | \ : &quot; &lt; &gt; . ? /`<br><br><b>Suggerimento</b> Per i dati che includono caratteri internazionali, utilizza i file in formato TSV o TXT. |
| [!UICONTROL Single Account] | Se il file si applica a un account: <i>[!UICONTROL Yes]</i> (per un account) oppure <i>[!UICONTROL No]</i>per più account. |
| [!UICONTROL Account (Search Engine)] | (Quando il file si applica a un singolo account) L’account a cui caricare i dati. |
| [!UICONTROL Search Engine] | (Quando il file si applica a più account) La rete di annunci in cui caricare i dati. |
| [!UICONTROL Scheduling] | Quando o se pubblicare il file nella rete di annunci specificata:<ul><li><i>[!UICONTROL Post to ad network now]</i> (impostazione predefinita): inizia subito la pubblicazione dei dati.</li><li><i>[!UICONTROL Post to ad network on \[specified date\] \[specified time\]]:</i> Inizia la pubblicazione dei dati nella data e nell&#39;ora specificate. Il valore predefinito è domani alle 02:00 (2.00). Per modificare la data, immettere una data nel formato GG/MM/AAAA o GG/M/AAAA oppure fare clic su ![Calendario](/help/search-social-commerce/campaign-management/bulksheets/assets/calendar.png "Calendario") per aprire il calendario e [seleziona una data](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md). Per modificare l&#39;ora, immettere l&#39;ora nel formato HH/MM o H/M oppure selezionare un&#39;ora (in intervalli di 15 minuti) dall&#39;elenco.</li><li><i>[!UICONTROL Preview only]:</i> Per caricare il file in Search, Social e Commerce senza pubblicare i dati sulla rete di annunci; puoi comunque pubblicare il file in un secondo momento. Quando il file bulksheet è superiore a 10 MB ma inferiore a 2 GB, il file è in formato ZIP; non è necessario decomprimere il file per pubblicarlo.</li></ul> |
| [!UICONTROL Generate Tracking URLs] | Se includere modelli di tracciamento e suffissi di pagina di destinazione (per reti di annunci applicabili) in account con modelli di tracciamento o URL di destinazione con codici di tracciamento incorporati in account con URL di destinazione, per tutte le parole chiave, gli annunci, i posizionamenti, i sitelink e [!DNL Google Ads] gruppi di prodotti nella registrazione: <i>[!UICONTROL Yes]</i> (impostazione predefinita) oppure <i>[!UICONTROL No]</i>. Non importa se le unità di offerta si trovano in un portfolio.<br><br>Se si seleziona <i>[!UICONTROL Yes]</i>, quindi gli URL vengono generati in base ai parametri in [!UICONTROL Tracking Methods] sezione delle impostazioni account o delle impostazioni campagna pertinenti. Per impostazione predefinita, se esistono URL di tracciamento, questi non vengono rigenerati a meno che non siano necessari nuovi URL (ad esempio se il tipo di corrispondenza della parola chiave, il testo dell’annuncio o i parametri di tracciamento per gli account rilevanti sono cambiati).<br><br>Se si seleziona <i>[!UICONTROL No]</i>, puoi comunque generare gli URL di tracciamento in un secondo momento pubblicando manualmente il file caricato.<br><br><b>Nota:</b> Se l’inserzionista utilizza il tracciamento delle conversioni di Adobi Advertising e l’URL di base è stato modificato, devi generare nuovi URL di tracciamento, a meno che l’account non sia configurato per generare e caricare automaticamente gli URL di tracciamento. |
| [!UICONTROL Enable budget changes on optimized campaigns] | Consente modifiche di budget alle campagne nei portfolio ottimizzati in base ai dati pubblicati. Per impostazione predefinita, questa opzione non è selezionata. Se selezioni questa opzione, eventuali modifiche al budget della campagna specificate saranno applicabili fino a quando la funzionalità di ottimizzazione non determinerà che il budget deve essere riallocato (di solito al successivo ciclo di offerta).<br><br><b>Nota:</b> Eventuali modifiche di budget risultanti dai dati pubblicati per campagne in portfolio non ottimizzati si verificano quando il file viene registrato. Le modifiche vengono visualizzate nelle visualizzazioni di gestione della campagna il giorno successivo. |
| [!UICONTROL Enable bidding on ads within portfolios] | Quando i componenti della campagna inclusi si trovano in un portfolio ottimizzato, questa funzione sovrascrive la strategia di ottimizzazione e consente di modificare le offerte in base ai dati nel bulksheet fino a una data di fine specificata. Se selezioni questa opzione, specifica una data di fine compresa tra 1 e 7 giorni nel **[!UICONTROL Hold bulksheet bids until]** campo. |

>[!MORELIKETHIS]
>
>* [Informazioni sulla gestione dei dati della campagna tramite bulksheet](bulksheet-about.md)
>* [Scaricare/creare un file bulksheet](bulksheet-download.md)
>* [Pubblica i bulksheet o i file di errore corretti](bulksheet-post.md)
>* [Convalidare le pagine di destinazione in file bulksheet](bulksheet-validate-landing-pages.md)
>* [Esportare un file bulksheet generato o caricato](bulksheet-export.md)
