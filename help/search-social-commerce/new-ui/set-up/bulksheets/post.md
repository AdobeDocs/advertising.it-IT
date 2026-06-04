---
title: (Nuova interfaccia utente) Pubblica i bulksheet o correggi i file di errore
description: Scopri come pubblicare file di bulksheet sulle reti di annunci nella nuova interfaccia utente di Search, Social e Commerce.
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
source-git-commit: 739034010787c2016720bef37fb75dc8efbae58b
workflow-type: tm+mt
source-wordcount: 752
ht-degree: 0%

---

# (Nuova interfaccia utente) Pubblica i bulksheet o correggi i file di errore

È possibile pubblicare file di bulksheet esistenti o file di errore corretti negli account pertinenti per [reti di annunci supportate](about.md#bulksheet-functionality-by-network). Se il file è in formato ZIP, non devi prima decomprimerlo.

I file di bulksheet e i file di errore vengono eliminati automaticamente 30 giorni dopo il caricamento o la generazione.

>[!NOTE]
>
>Puoi anche pubblicare un file bulksheet o un file di errore quando carichi il file.

1. Nel menu principale, fare clic su **[!UICONTROL Setup]** \> **[!UICONTROL Bulksheets]**.

1. Seleziona la casella di controllo accanto a ciascun file da pubblicare.

1. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL Post]**.

1. Immettere o selezionare le informazioni nelle impostazioni [[!UICONTROL Post Bulksheet]](#bulksheet-post-settings), quindi fare clic su **[!UICONTROL Post]**.

   Le stesse impostazioni si applicano a tutti i file pubblicati.

All&#39;inizio dell&#39;attività, lo stato e la data di pubblicazione pianificata per la riga vengono aggiornati nella visualizzazione [!UICONTROL Bulksheets]. Quando le notifiche e-mail per i bulksheet sono abilitate per [&#x200B; in [!UICONTROL Notification Center]](/help/search-social-commerce/new-ui/notifications/notification-manage.md), al momento della pubblicazione del file viene inviata una notifica e-mail con un collegamento al file. A seconda della quantità di dati compilati, la notifica e-mail potrebbe richiedere alcuni minuti o più. Se non è possibile pubblicare alcun dato, nella visualizzazione [!UICONTROL Bulksheets] viene elencato un file di errore e viene inviata una notifica e-mail con un collegamento al file di errore.

>[!NOTE]
>
>* La pubblicazione di grandi quantità di dati richiede più tempo. È possibile seguire l&#39;avanzamento del file nella colonna [!UICONTROL Progress] nella visualizzazione [!UICONTROL Bulksheets].
>* Tutti i dati pubblicati sono soggetti al processo editoriale della rete.
>* Prima della registrazione del file di bulksheet, è possibile annullarla.

## Impostazioni post per i bulksheet e i file di errore corretti {#bulksheet-post-settings}

| Parametro | Descrizione |
|----|----|
| [!UICONTROL Account (Search Engine)] | L’account di rete dell’annuncio per il quale vengono pubblicati i dati. Se si pubblicano più file contemporaneamente o un file che si applica a più account, il valore è *Più account selezionati*.<br><br>La prima lettera del nome della rete di annunci è tra parentesi dopo il nome dell&#39;account, ad esempio &quot;Acme Realty (G)&quot; per un account [!DNL Google Ads]. |
| [!UICONTROL Scheduling] | Quando inserire il file nella rete di annunci specificata:<ul><li>*[!UICONTROL Post to ad network now]* (impostazione predefinita): inizia subito la pubblicazione dei dati.</li><li>*[!UICONTROL Post to ad network on \[specified date\] \[specified time\]]:* Inizia la pubblicazione dei dati alla data e all&#39;ora specificate. L&#39;impostazione predefinita è domani alle 02:00 (2.00). Per modificare la data, immettere una data nel formato GG/MM/AAAA oppure fare clic sull&#39;icona del calendario per aprire il calendario e selezionare una data. Per modificare l’ora, seleziona un’ora dall’elenco (con intervalli di 15 minuti).</li></ul> |
| [!UICONTROL Generate Tracking URLs] | Indica se includere i modelli di tracciamento e i suffissi delle pagine di destinazione (per le reti di annunci applicabili) in account con modelli di tracciamento o gli URL di destinazione con codici di tracciamento incorporati in account con URL di destinazione, per tutte le parole chiave, gli annunci, i posizionamenti, i sitelink e i gruppi di prodotti [!DNL Google Ads] nel post: *[!UICONTROL Yes]* (impostazione predefinita) o *[!UICONTROL No]*. Non importa se le unità di offerta si trovano in un portfolio.<br><br>Se si seleziona *[!UICONTROL Yes]*, gli URL vengono generati in base ai parametri nella sezione [!UICONTROL Tracking Methods] delle impostazioni account o delle campagne pertinenti. Per impostazione predefinita, se sono presenti URL di tracciamento, questi non vengono rigenerati a meno che non siano necessari nuovi URL (ad esempio se il tipo di corrispondenza delle parole chiave, il testo dell&#39;annuncio o i parametri di tracciamento per gli account rilevanti sono cambiati).<br><br>Se selezioni *[!UICONTROL No]*, puoi comunque generare gli URL di tracciamento in un secondo momento pubblicando manualmente il file caricato.<br><br>**Nota:** Se l&#39;inserzionista utilizza il tracciamento delle conversioni di Adobe Advertising e l&#39;URL di base è stato modificato, devi generare nuovi URL di tracciamento a meno che l&#39;account non sia configurato per generare e caricare automaticamente gli URL di tracciamento. |
| [!UICONTROL Replace Media Optimizer Tracking] | (Disponibile quando [!UICONTROL Generate Tracking URLs] è *[!UICONTROL Yes]*) Sostituisce qualsiasi tracciamento Adobe Advertising esistente negli URL del file caricato con un tracciamento appena generato. |
| [!UICONTROL Enable budget changes on optimized campaigns] | Consente modifiche di budget alle campagne nei portfolio ottimizzati in base ai dati pubblicati. Per impostazione predefinita, questa opzione non è selezionata. Se si seleziona questa opzione, tutte le modifiche al budget della campagna specificate saranno applicabili fino a quando la funzionalità di ottimizzazione non determinerà che il budget deve essere riallocato (in genere al successivo ciclo di offerta).<br><br>**Nota:** Qualsiasi modifica al budget derivante dai dati registrati per le campagne in portfolio non ottimizzati si verifica quando il file viene registrato. Le modifiche vengono visualizzate nelle visualizzazioni di gestione della campagna il giorno successivo. |
| [!UICONTROL Enable bidding on ads within portfolios] | Quando i componenti della campagna inclusi si trovano in un portfolio ottimizzato, questa funzione sovrascrive la strategia di ottimizzazione e consente di modificare le offerte in base ai dati nel bulksheet fino a una data di fine specificata. Se si seleziona questa opzione, specificare una data di fine compresa tra 1 e 7 giorni nel campo **[!UICONTROL Hold bulksheet bids until]**. |

>[!MORELIKETHIS]
>
>* [(Nuova interfaccia) Informazioni sulla gestione dei dati della campagna tramite bulksheet](about.md)
>* [(Nuova interfaccia) Download/creazione di un file bulksheet](download.md)
>* [(Nuova interfaccia) Carica un bulksheet o un file di errore corretto](upload.md)
>* [(Nuova interfaccia) Convalida pagine di destinazione in file bulksheet](validate-landing-pages.md)
>* [(Nuova interfaccia) Elimina i bulksheet caricati e i file di errore](delete.md)
