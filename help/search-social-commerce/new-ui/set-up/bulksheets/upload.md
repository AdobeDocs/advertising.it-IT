---
title: (Nuova interfaccia) Carica un file bulksheet o di errore corretto
description: Scopri come caricare manualmente un file bulksheet o un file di errore di convalida della pagina di destinazione corretto nella nuova interfaccia utente di Search, Social e Commerce.
feature: Search Bulksheets
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2:
  - id: e58024d1-d6da-420c-80af-6be211808316
  - id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 38fd7ff63b177f13bdfb19b980fb1d1e14edcf56
workflow-type: tm+mt
source-wordcount: 830
ht-degree: 0%

---

# (Nuova interfaccia) Carica un file bulksheet o di errore corretto

Puoi caricare i file dei bulksheet, i file degli errori di convalida delle pagine di destinazione corretti e altri file degli errori corretti dal tuo dispositivo o dalla tua rete per [reti di annunci supportate](about.md#bulksheet-functionality-by-network). Tutte le colonne personalizzate nel file vengono eliminate quando caricate il file.

1. Nel menu principale, fare clic su **[!UICONTROL Setup]** \> **[!UICONTROL Bulksheets]**.

1. Nella barra degli strumenti fare clic su **[!UICONTROL Bulk Operations]** \> **[!UICONTROL Upload Bulksheet]**.

1. Immettere o selezionare le informazioni nelle impostazioni [[!UICONTROL Upload Bulksheet]](#bulksheet-upload-settings).

1. Fare clic su **[!UICONTROL Upload]**.

All&#39;inizio dell&#39;attività, il file viene elencato nella visualizzazione [!UICONTROL Bulksheets]. Quando le notifiche e-mail per i bulksheet sono abilitate per [&#x200B; in [!UICONTROL Notification Center]](/help/search-social-commerce/new-ui/notifications/notification-manage.md), viene inviata una notifica e-mail con un collegamento al file al termine del processo. A seconda della quantità di dati compilati, la notifica e-mail potrebbe richiedere alcuni minuti o più. Se la generazione del file non riesce, nella visualizzazione [!UICONTROL Bulksheets] viene elencato un file di errore e viene inviata una notifica e-mail con un collegamento al file di errore.

>[!NOTE]
>
>Se si inseriscono i dati del bulksheet nella rete di annunci, è possibile seguire l&#39;avanzamento del file nella colonna [!UICONTROL Progress] nella visualizzazione [!UICONTROL Bulksheets]. La pubblicazione di grandi quantità di dati richiede più tempo.

## Impostazioni di caricamento per i bulksheet e i file di errore corretti {#bulksheet-upload-settings}

| Parametro | Descrizione |
|----|----|
| [!UICONTROL File to Upload] | Il file da caricare. Specificare il file facendo clic su **[!UICONTROL Choose File]** per individuarlo nel dispositivo o nella rete.<br><br>I file bulksheet possono contenere fino a 2,5 GB (circa 2,5 milioni di righe) e devono avere una delle seguenti estensioni: *[!UICONTROL .tsv]* (per valori separati da tabulazioni), *[!UICONTROL .txt]* (per testo ASCII conforme a Unicode), *[!UICONTROL .csv]* (per valori separati da virgola) o *[!UICONTROL .zip]* (per il formato ZIP compresso, che si decomprime in un file TSV). Il nome del file non può includere i seguenti caratteri: `# % & * \| \ : " < > . ? /`<br><br>**Suggerimento:** Per i dati che includono caratteri internazionali, utilizzare i file in formato TSV o TXT. |
| [!UICONTROL Single Account] | Indica se il file si applica a un account: *[!UICONTROL Yes]* (per un account) o *[!UICONTROL No]* (per più account). |
| [!UICONTROL Account (Search Engine)] | (Quando il file si applica a un singolo account) L’account a cui caricare i dati. |
| [!UICONTROL Search Engine] | (Quando il file si applica a più account) La rete di annunci in cui caricare i dati.<br><br>**Nota:** le modifiche delle offerte per le parole chiave nei portfolio ottimizzati non sono supportate con i bulksheet a più account. |
| [!UICONTROL Scheduling] | Quando o se pubblicare il file nella rete di annunci specificata:<ul><li>*[!UICONTROL Post to search engine now]* (impostazione predefinita): inizia subito la pubblicazione dei dati.</li><li>*[!UICONTROL Post to search engine on \[specified date\] \[specified time\]]:* Inizia la pubblicazione dei dati alla data e all&#39;ora specificate. L&#39;impostazione predefinita è domani alle 02:00 (2.00). Per modificare la data, immettere una data nel formato GG/MM/AAAA oppure fare clic sull&#39;icona del calendario per aprire il calendario e selezionare una data. Per modificare l’ora, seleziona un’ora dall’elenco (con intervalli di 15 minuti).</li><li>*[!UICONTROL Preview only]:* Carica il file in Search, Social e Commerce senza pubblicare i dati nella rete di annunci; è comunque possibile pubblicare il file in un secondo momento. Quando il file bulksheet è superiore a 10 MB ma inferiore a 2 GB, il file è in formato ZIP; non è necessario decomprimere il file per pubblicarlo.</li></ul> |
| [!UICONTROL Generate Tracking URLs] | Indica se includere i modelli di tracciamento e i suffissi delle pagine di destinazione (per le reti di annunci applicabili) in account con modelli di tracciamento o gli URL di destinazione con codici di tracciamento incorporati in account con URL di destinazione, per tutte le parole chiave, gli annunci, i posizionamenti, i sitelink e i gruppi di prodotti [!DNL Google Ads] nel post: *[!UICONTROL Yes]* (impostazione predefinita) o *[!UICONTROL No]*. Non importa se le unità di offerta si trovano in un portfolio.<br><br>Se si seleziona *[!UICONTROL Yes]*, gli URL vengono generati in base ai parametri nella sezione [!UICONTROL Tracking Methods] delle impostazioni account o delle campagne pertinenti. Per impostazione predefinita, se sono presenti URL di tracciamento, questi non vengono rigenerati a meno che non siano necessari nuovi URL (ad esempio se il tipo di corrispondenza delle parole chiave, il testo dell&#39;annuncio o i parametri di tracciamento per gli account rilevanti sono cambiati).<br><br>Se selezioni *[!UICONTROL No]*, puoi comunque generare gli URL di tracciamento in un secondo momento pubblicando manualmente il file caricato.<br><br>**Nota:** Se l&#39;inserzionista utilizza il tracciamento delle conversioni di Adobe Advertising e l&#39;URL di base è stato modificato, devi generare nuovi URL di tracciamento a meno che l&#39;account non sia configurato per generare e caricare automaticamente gli URL di tracciamento. |
| [!UICONTROL Replace Media Optimizer Tracking] | (Disponibile quando [!UICONTROL Generate Tracking URLs] è *[!UICONTROL Yes]*) Sostituisce qualsiasi tracciamento Adobe Advertising esistente negli URL del file caricato con un tracciamento appena generato. |
| [!UICONTROL Enable budget changes on optimized campaigns] | Consente modifiche di budget alle campagne nei portfolio ottimizzati in base ai dati pubblicati. Per impostazione predefinita, questa opzione non è selezionata. Se si seleziona questa opzione, tutte le modifiche al budget della campagna specificate saranno applicabili fino a quando la funzionalità di ottimizzazione non determinerà che il budget deve essere riallocato (in genere al successivo ciclo di offerta).<br><br>**Nota:** Qualsiasi modifica al budget derivante dai dati registrati per le campagne in portfolio non ottimizzati si verifica quando il file viene registrato. Le modifiche vengono visualizzate nelle visualizzazioni di gestione della campagna il giorno successivo. |
| [!UICONTROL Enable bidding on ads within portfolios] | Quando i componenti della campagna inclusi si trovano in un portfolio ottimizzato, questa funzione sovrascrive la strategia di ottimizzazione e consente di modificare le offerte in base ai dati nel bulksheet fino a una data di fine specificata. Se si seleziona questa opzione, specificare una data di fine compresa tra 1 e 7 giorni nel campo **[!UICONTROL Hold bulksheet bids until]**. |

>[!MORELIKETHIS]
>
>* [(Nuova interfaccia) Informazioni sulla gestione dei dati della campagna tramite bulksheet](about.md)
>* [(Nuova interfaccia) Download/creazione di un file bulksheet](download.md)
>* [(Nuova interfaccia) Pubblica i bulksheet o correggi i file di errore](post.md)
>* [(Nuova interfaccia) Convalida pagine di destinazione in file bulksheet](validate-landing-pages.md)
