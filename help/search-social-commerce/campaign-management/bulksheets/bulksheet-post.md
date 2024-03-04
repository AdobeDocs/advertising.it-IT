---
title: Pubblica i bulksheet o i file di errore corretti
description: Scopri come pubblicare file di bulksheet sulle reti di annunci.
exl-id: 49b930ba-71b3-442d-a162-67cf7ae14e14
feature: Search Bulksheets
source-git-commit: 6b3c876f17d0e30dcce69048bb4041fc8cd29902
workflow-type: tm+mt
source-wordcount: '726'
ht-degree: 0%

---

# Pubblica i bulksheet o i file di errore corretti

È possibile registrare i file di bulksheet esistenti o i file di errore corretti nei relativi account per [reti pubblicitarie supportate](bulksheet-about.md#bulksheet-functionality-by-network). Se il file è in formato ZIP, non devi prima decomprimerlo.

I file di bulksheet e i file di errore vengono eliminati automaticamente 30 giorni dopo il caricamento o la generazione.

>[!NOTE]
>Puoi anche pubblicare un file bulksheet o un file di errore quando carichi il file.

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Bulksheets]**.

1. Seleziona la casella di controllo accanto a ciascun file da pubblicare.

1. Nella barra degli strumenti sopra la tabella dati, fai clic su **[!UICONTROL Post]**.

1. Nella finestra di dialogo, immetti o seleziona le informazioni nel [[!UICONTROL Post Bulksheet] impostazioni](#bulksheet-post-settings)e quindi fare clic su **[!UICONTROL Post]**.

   Le stesse impostazioni si applicano a tutti i file pubblicati.

Quando inizia l&#39;attività, lo stato e la data di registrazione pianificata per la riga vengono modificati nel [!UICONTROL Bulksheets] visualizzazione. Quando il file viene pubblicato, viene inviata una notifica e-mail con un collegamento al file. A seconda della quantità di dati compilati, la notifica e-mail potrebbe richiedere alcuni minuti o più. Tuttavia, se non è possibile pubblicare alcun dato, nella [!UICONTROL Bulksheets] e viene inviata una notifica e-mail con un collegamento al file di errore.

>[!NOTE]
>
>* La pubblicazione di grandi quantità di dati richiede più tempo. Puoi seguire l’avanzamento del file nella sezione [!UICONTROL Progress] colonna nella [!UICONTROL Bulksheets] visualizzazione.
>* Tutti i dati pubblicati sono soggetti al processo editoriale della rete.
* Prima della registrazione del file di bulksheet, è possibile annullarla.

## Impostazioni post per i bulksheet e i file di errore corretti {#bulksheet-post-settings}

| Parametro | Descrizione |
|----|----|
| [!UICONTROL Account (Search Engine)] | L’account di rete dell’annuncio per il quale vengono pubblicati i dati. Se pubblichi più file contemporaneamente o un file che si applica a più account, il valore è <i>Più account selezionati</i>.<br><br>La prima lettera del nome della rete di annunci è tra parentesi dopo il nome dell’account (ad esempio &quot;Acme Realty (G)&quot; per un [!DNL Google Ads] account). |
| [!UICONTROL Scheduling] | Quando inserire il file nella rete di annunci specificata:<ul><li><i>[!UICONTROL Post to ad network now]</i> (impostazione predefinita): inizia subito la pubblicazione dei dati.</li><li><i>[!UICONTROL Post to ad network on \[specified date\] \[specified time\]]:</i> Inizia la pubblicazione dei dati nella data e nell&#39;ora specificate. Il valore predefinito è domani alle 02:00 (2.00). Per modificare la data, immettere una data nel formato GG/MM/AAAA o GG/M/AAAA oppure fare clic su ![Calendario](/help/search-social-commerce/assets/calendar.png "Calendario") per aprire il calendario e [seleziona una data](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md). Per modificare l&#39;ora, immettere l&#39;ora nel formato HH/MM o H/M oppure selezionare un&#39;ora (in intervalli di 15 minuti) dall&#39;elenco.</li></ul> |
| [!UICONTROL Generate Tracking URLs] | Se includere modelli di tracciamento e suffissi di pagina di destinazione (per reti di annunci applicabili) in account con modelli di tracciamento o URL di destinazione con codici di tracciamento incorporati in account con URL di destinazione, per tutte le parole chiave, gli annunci, i posizionamenti, i sitelink e [!DNL Google Ads] gruppi di prodotti nella registrazione: <i>[!UICONTROL Yes]</i> (impostazione predefinita) oppure <i>[!UICONTROL No]</i>. Non importa se le unità di offerta si trovano in un portfolio.<br><br>Se si seleziona <i>[!UICONTROL Yes]</i>, quindi gli URL vengono generati in base ai parametri in [!UICONTROL Tracking Methods] sezione delle impostazioni account o delle impostazioni campagna pertinenti. Per impostazione predefinita, se esistono URL di tracciamento, questi non vengono rigenerati a meno che non siano necessari nuovi URL (ad esempio se il tipo di corrispondenza della parola chiave, il testo dell’annuncio o i parametri di tracciamento per gli account rilevanti sono cambiati).<br><br>Se si seleziona <i>[!UICONTROL No]</i>, puoi comunque generare gli URL di tracciamento in un secondo momento pubblicando manualmente il file caricato.<br><br><b>Nota:</b> Se l’inserzionista utilizza il tracciamento delle conversioni di Adobi Advertising e l’URL di base è stato modificato, devi generare nuovi URL di tracciamento, a meno che l’account non sia configurato per generare e caricare automaticamente gli URL di tracciamento. |
| [!UICONTROL Enable budget changes on optimized campaigns] | Consente modifiche di budget alle campagne nei portfolio ottimizzati in base ai dati pubblicati. Per impostazione predefinita, questa opzione non è selezionata. Se selezioni questa opzione, eventuali modifiche al budget della campagna specificate saranno applicabili fino a quando la funzionalità di ottimizzazione non determinerà che il budget deve essere riallocato (di solito al successivo ciclo di offerta).<br><br><b>Nota:</b> Eventuali modifiche di budget risultanti dai dati pubblicati per campagne in portfolio non ottimizzati si verificano quando il file viene registrato. Le modifiche vengono visualizzate nelle visualizzazioni di gestione della campagna il giorno successivo. |
| [!UICONTROL Enable bidding on ads within portfolios] | Quando i componenti della campagna inclusi si trovano in un portfolio ottimizzato, questa funzione sovrascrive la strategia di ottimizzazione e consente di modificare le offerte in base ai dati nel bulksheet fino a una data di fine specificata. Se selezioni questa opzione, specifica una data di fine compresa tra 1 e 7 giorni nel **[!UICONTROL Hold bulksheet bids until]** campo. |

>[!MORELIKETHIS]
>
>* [Informazioni sulla gestione dei dati della campagna tramite bulksheet](bulksheet-about.md)
>* [Scaricare/creare un file bulksheet](bulksheet-download.md)
>* [Carica i bulksheet o i file di errore corretti](bulksheet-upload.md)
>* [Convalidare le pagine di destinazione in file bulksheet](bulksheet-validate-landing-pages.md)
>* [Esportare un file bulksheet generato o caricato](bulksheet-export.md)
