---
title: Pubblica i bulksheet o i file di errore corretti
description: Scopri come pubblicare file di bulksheet sulle reti di annunci.
exl-id: 49b930ba-71b3-442d-a162-67cf7ae14e14
feature: Search Bulksheets
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '726'
ht-degree: 0%

---

# Pubblica i bulksheet o i file di errore corretti

È possibile pubblicare file di bulksheet esistenti o file di errore corretti negli account pertinenti per [reti di annunci supportate](bulksheet-about.md#bulksheet-functionality-by-network). Se il file è in formato ZIP, non devi prima decomprimerlo.

I file di bulksheet e i file di errore vengono eliminati automaticamente 30 giorni dopo il caricamento o la generazione.

>[!NOTE]
>Puoi anche pubblicare un file bulksheet o un file di errore quando carichi il file.

1. Nel menu principale, fare clic su **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Bulksheets]**.

1. Seleziona la casella di controllo accanto a ciascun file da pubblicare.

1. Nella barra degli strumenti sopra la tabella dati, fare clic su **[!UICONTROL Post]**.

1. Nella finestra di dialogo immettere o selezionare le informazioni nelle impostazioni [[!UICONTROL Post Bulksheet]](#bulksheet-post-settings), quindi fare clic su **[!UICONTROL Post]**.

   Le stesse impostazioni si applicano a tutti i file pubblicati.

All&#39;inizio dell&#39;attività, lo stato e la data di pubblicazione pianificata per la riga vengono modificati nella visualizzazione [!UICONTROL Bulksheets]. Quando il file viene pubblicato, viene inviata una notifica e-mail con un collegamento al file. A seconda della quantità di dati compilati, la notifica e-mail potrebbe richiedere alcuni minuti o più. Se tuttavia non è possibile pubblicare alcun dato, nella visualizzazione [!UICONTROL Bulksheets] verrà elencato un file di errore e verrà inviata una notifica e-mail con un collegamento al file di errore.

>[!NOTE]
>
>* La pubblicazione di grandi quantità di dati richiede più tempo. È possibile seguire l&#39;avanzamento del file nella colonna [!UICONTROL Progress] nella visualizzazione [!UICONTROL Bulksheets].
>* Tutti i dati pubblicati sono soggetti al processo editoriale della rete.
>* Prima della registrazione del file di bulksheet, è possibile annullarla.

## Impostazioni post per i bulksheet e i file di errore corretti {#bulksheet-post-settings}

| Parametro | Descrizione |
|----|----|
| [!UICONTROL Account (Search Engine)] | L’account di rete dell’annuncio per il quale vengono pubblicati i dati. Se si pubblicano più file contemporaneamente o un file che si applica a più account, il valore è <i>Più account selezionati</i>.<br><br>La prima lettera del nome della rete di annunci è tra parentesi dopo il nome dell&#39;account, ad esempio &quot;Acme Realty (G)&quot; per un account [!DNL Google Ads]. |
| [!UICONTROL Scheduling] | Quando inserire il file nella rete di annunci specificata:<ul><li><i>[!UICONTROL Post to ad network now]</i> (impostazione predefinita): inizia subito la pubblicazione dei dati.</li><li><i>[!UICONTROL Post to ad network on \[specified date\] \[specified time\]]:</i> Inizia la pubblicazione dei dati alla data e all&#39;ora specificate. L&#39;impostazione predefinita è domani alle 02:00 (2.00). Per modificare la data, immettere una data nel formato GG/MM/AAAA o GG/M/AAAA oppure fare clic su ![Calendario](/help/search-social-commerce/assets/calendar.png "Calendario") per aprire il calendario e [selezionare una data](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md). Per modificare l&#39;ora, immettere l&#39;ora nel formato HH/MM o H/M oppure selezionare un&#39;ora (in intervalli di 15 minuti) dall&#39;elenco.</li></ul> |
| [!UICONTROL Generate Tracking URLs] | Indica se includere i modelli di tracciamento e i suffissi delle pagine di destinazione (per le reti di annunci applicabili) in account con modelli di tracciamento o gli URL di destinazione con codici di tracciamento incorporati in account con URL di destinazione, per tutte le parole chiave, gli annunci, i posizionamenti, i sitelink e i gruppi di prodotti [!DNL Google Ads] nel post: <i>[!UICONTROL Yes]</i> (impostazione predefinita) o <i>[!UICONTROL No]</i>. Non importa se le unità di offerta si trovano in un portfolio.<br><br>Se si seleziona <i>[!UICONTROL Yes]</i>, gli URL vengono generati in base ai parametri nella sezione [!UICONTROL Tracking Methods] delle impostazioni account o delle campagne pertinenti. Per impostazione predefinita, se esistono URL di tracciamento, questi non vengono rigenerati a meno che non siano necessari nuovi URL (ad esempio se il tipo di corrispondenza della parola chiave, il testo dell’annuncio o i parametri di tracciamento per gli account rilevanti sono cambiati).<br><br>Se selezioni <i>[!UICONTROL No]</i>, puoi comunque generare gli URL di tracciamento in un secondo momento pubblicando manualmente il file caricato.<br><br><b>Nota:</b> se l&#39;inserzionista utilizza il tracciamento delle conversioni di Adobe Advertising e l&#39;URL di base è stato modificato, è necessario generare nuovi URL di tracciamento a meno che l&#39;account non sia configurato per generare e caricare automaticamente gli URL di tracciamento. |
| [!UICONTROL Enable budget changes on optimized campaigns] | Consente modifiche di budget alle campagne nei portfolio ottimizzati in base ai dati pubblicati. Per impostazione predefinita, questa opzione non è selezionata. Se selezioni questa opzione, eventuali modifiche al budget della campagna specificate saranno applicabili fino a quando la funzionalità di ottimizzazione non determinerà che il budget deve essere riallocato (di solito al successivo ciclo di offerta).<br><br><b>Nota:</b> eventuali modifiche al budget derivanti dai dati pubblicati per le campagne in portfolio non ottimizzati si verificano quando il file viene registrato. Le modifiche vengono visualizzate nelle visualizzazioni di gestione della campagna il giorno successivo. |
| [!UICONTROL Enable bidding on ads within portfolios] | Quando i componenti della campagna inclusi si trovano in un portfolio ottimizzato, questa funzione sovrascrive la strategia di ottimizzazione e consente di modificare le offerte in base ai dati nel bulksheet fino a una data di fine specificata. Se si seleziona questa opzione, specificare una data di fine compresa tra 1 e 7 giorni nel campo **[!UICONTROL Hold bulksheet bids until]**. |

>[!MORELIKETHIS]
>
>* [Informazioni sulla gestione dei dati della campagna tramite bulksheet](bulksheet-about.md)
>* [Scaricare/creare un file bulksheet](bulksheet-download.md)
>* [Caricare i bulksheet o correggere i file di errore](bulksheet-upload.md)
>* [Convalida pagine di destinazione in file bulksheet](bulksheet-validate-landing-pages.md)
>* [Esporta un file bulksheet generato o caricato](bulksheet-export.md)
