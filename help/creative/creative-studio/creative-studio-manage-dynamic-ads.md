---
title: Gestione di creatività dinamiche in Creative Studio
description: Scopri come creare, verificare la qualità, modificare, duplicare ed eliminare creatività dinamiche basate su catalogo in Adobe Advertising Creative Studio.
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 88fead9ffc4eaa572be090877790422e67831036
workflow-type: tm+mt
source-wordcount: '1469'
ht-degree: 0%
---
# Gestisci creatività dinamica in [!UICONTROL Creative Studio]

La scheda **[!UICONTROL Creatives]** in [!UICONTROL Creative Studio] elenca le tue creatività dinamiche in base alla libreria. Da qui puoi creare nuovi creativi dinamici basati su catalogo, creativi con controllo di qualità con AI, modificare i dettagli e la mappatura degli attributi dei creativi esistenti, visualizzare i registri di modifica, duplicare i creativi ed eliminare i creativi.

## Creare una creatività dinamica {#build-dynamic-creative}

Utilizza questo flusso di lavoro per creare creatività dinamiche basate su catalogo. Una procedura guidata in quattro passaggi ti guida attraverso la selezione di un modello, la connessione di un catalogo e la mappatura dei campi catalogo agli elementi del modello. Dopo la configurazione, [!UICONTROL AI Assistant] ti consente di visualizzare in anteprima e controllare la qualità di ogni combinazione di annunci generata dai dati del catalogo.

Le creatività dinamiche differiscono dagli annunci standard in un modo chiave: l’agente di intelligenza artificiale non può modificare i contenuti originati dal catalogo. È in grado di filtrare, analizzare e segnalare i problemi, ma per modificare il contenuto degli annunci è necessario aggiornare i valori del catalogo manualmente, dalla schermata di controllo qualità o nel catalogo sorgente.

### Prerequisiti

* Nella libreria di modelli deve esistere almeno un modello di annuncio visualizzato creato dall&#39;utente (non un modello di sistema).
* Nel tuo account è disponibile un catalogo di prodotti o contenuti (feed).

### Passaggio 1: aprire la procedura guidata [!UICONTROL Build Dynamic Creative] {#open-wizard}

1. Nel menu principale, fare clic su **[!UICONTROL Creative Studio]**.

1. Nella scheda **[!UICONTROL Creatives]**, fare clic su **[!UICONTROL Build]** nella scheda Azioni rapide **[!UICONTROL Build dynamic creatives from catalog data]**.

   Viene visualizzata la finestra di dialogo **[!UICONTROL Build Dynamic Creative]** in quattro passaggi.

### Passaggio 2: selezionare un modello {#select-template}

>[!NOTE]
>
>Negli elenchi della raccolta di modelli vengono visualizzati solo i modelli di annunci creati dall&#39;utente. I modelli di sistema e i modelli di annunci video non sono disponibili come punto di partenza per i creativi dinamici.

1. Nella raccolta modelli fare clic su un modello per selezionarlo.

   Il pulsante **[!UICONTROL Next]** è disattivato finché non viene selezionato un modello.

1. Fare clic su **[!UICONTROL Use this template]**.

### Passaggio 3: selezionare un catalogo {#select-catalog}

1. Configura le impostazioni creative:

   * **[!UICONTROL Ad Library]:** Seleziona la libreria creativa in cui salvare la creatività.
   * **[!UICONTROL Dynamic creative name]:** Immettere un nome per la creatività dinamica.
   * **[!UICONTROL Number of cards]:** Immetti il numero di offerte catalogo da includere in ogni combinazione di annunci (1-50).
   * **[!UICONTROL Assign dynamic creative to a bundle]:** (Facoltativo) Se questa opzione è abilitata, le creatività salvate vengono associate a un bundle. Seleziona un bundle dalla libreria.

1. Seleziona uno o più cataloghi:

   1. (Facoltativo) Utilizzare **[!UICONTROL Catalog template]** per filtrare l&#39;elenco di cataloghi in base a una famiglia di modelli specifica. Per scaricare il file modello per rivederlo, fare clic su **[!UICONTROL Download feed template]**.

   1. Cerca e seleziona i cataloghi dall’elenco. Tutti i cataloghi selezionati devono appartenere alla stessa famiglia di modelli di catalogo. Se si tenta di combinare più famiglie, viene visualizzato un avviso.

   1. (Facoltativo) Per caricare un nuovo file catalogo, trascinarlo e rilasciarlo nell&#39;area di caricamento oppure fare clic su **[!UICONTROL Browse Files]**. Formati supportati: JPG, PNG, JPEG, XLS, XLSX, CSV, TSV, ZIP e MP4. Dimensione massima del file: 25 MB. Puoi caricare un file alla volta. I cataloghi caricati vengono visualizzati nell&#39;elenco dei chip con etichetta **(caricato)**.

1. Fare clic su **[!UICONTROL Continue]**.

### Passaggio 4: mappare i campi del catalogo agli elementi del modello {#attribute-mapping}

Mappa ogni campo catalogo all’elemento corrispondente nel modello. Ad esempio, mappa il campo del nome del prodotto del catalogo con l’elemento titolo del modello e il campo dell’immagine del prodotto con l’elemento dell’immagine di sfondo.

1. In **[!UICONTROL Targeting]**, selezionare almeno un&#39;origine dati per la personalizzazione del contenuto creativo: **[!UICONTROL Profile data]**, **[!UICONTROL Geographic data]**, **[!UICONTROL Data pass]** o **[!UICONTROL Audience Segment]**.

1. Per ogni elemento modello, seleziona il campo catalogo corrispondente dal menu a discesa.

1. Fare clic su **[!UICONTROL Continue]**.

### Passaggio 5: anteprima e controllo qualità con intelligenza artificiale {#qa}

1. Scegliere se *[!UICONTROL Save Dynamic Creative & Skip QA]* o *[!UICONTROL Continue to QA]*.

   Se si continua il controllo qualità, viene visualizzata la schermata **[!UICONTROL Dynamic Creative QA]** con un&#39;area di lavoro di anteprima e il pannello chat di **[!UICONTROL AI Assistant]**.

1. Se continui a eseguire il controllo qualità, segui le procedure descritte in &quot;[Controllo qualità di una creatività dinamica](#qa-dynamic-creative)&quot; per [analizzare e filtrare gli annunci](#analyze-ads), [esaminare anteprime e avvisi](#review-previews) e facoltativamente [correggere i valori del catalogo](#correct-catalog-values). Al termine, [salva la creatività dinamica](#save-or-exit).

## Modificare una creatività dinamica {#edit-dynamic-creative}

1. Nel menu principale, fare clic su **[!UICONTROL Creative Studio]**.

1. Nella scheda **[!UICONTROL Creatives]**, posizionare il cursore sulla scheda creativa e fare clic su **[!UICONTROL ...]** > **[!UICONTROL Edit]**.

   Si apre un editor a schermo intero con un’anteprima dell’annuncio a sinistra e un pannello delle impostazioni a destra.

1. Modificare le impostazioni creative utilizzando le schede **[!UICONTROL Details]** e **[!UICONTROL Attribute Mapping]**:

   Scheda **[!UICONTROL Details]**:

   * **[!UICONTROL Advertiser]**, **[!UICONTROL Ad Library]** e **[!UICONTROL Ad template]** sono di sola lettura.
   * **[!UICONTROL Dynamic creative name]:** Il nome visualizzato per la creatività.
   * **[!UICONTROL Number of cards]:** Il numero di offerte di catalogo incluse in ogni combinazione di annunci (1-50).
   * (Facoltativo) In **[!UICONTROL Catalogs]**, aggiornare la selezione del catalogo:
     * Utilizza **[!UICONTROL Catalog template]** per filtrare i cataloghi disponibili. Per scaricare il file modello, fare clic su **[!UICONTROL Download feed template]**.
     * Cerca e seleziona i cataloghi dall&#39;elenco, oppure carica un nuovo file di catalogo trascinandolo nell&#39;area di caricamento o facendo clic su **[!UICONTROL Browse Files]** (formati supportati: JPG, PNG, JPEG, XLS, XLSX, CSV, TSV, ZIP, MP4; massimo 25 MB; un file alla volta). I cataloghi caricati sono etichettati **(caricato)** nell&#39;elenco dei chip.

     Tutti i cataloghi devono appartenere alla stessa famiglia di modelli di catalogo.

   Scheda **[!UICONTROL Attribute Mapping]**:

   * In **[!UICONTROL Targeting]**, selezionare almeno un&#39;origine dati: **[!UICONTROL Profile data]**, **[!UICONTROL Geographic data]**, **[!UICONTROL Data pass]** o **[!UICONTROL Audience Segment]**.
   * In **[!UICONTROL Attribute Mapping]**, aggiorna il mapping da ciascun nome di livello modello all&#39;etichetta di colonna del catalogo corrispondente.

1. Fare clic su **[!UICONTROL Update Creative]**.

## Controllo qualità per una creatività dinamica {#qa-dynamic-creative}

Utilizza l’agente di controllo qualità per analizzare le righe del catalogo in base al modello di un creatività dinamico, visualizzare in anteprima gli annunci risultanti e identificare potenziali problemi di contenuto. È possibile filtrare e raggruppare gli annunci utilizzando **[!UICONTROL AI Assistant]**, esaminare gli avvisi del catalogo e correggere manualmente i valori del catalogo prima di pubblicare le modifiche.

L&#39;agente apre la schermata **[!UICONTROL Dynamic Creative QA]** da [!UICONTROL Creative Libraries] o [!UICONTROL Creative Studio]. Sebbene le etichette dei menu siano diverse, entrambi i punti di ingresso forniscono la stessa funzionalità di controllo qualità. L’analisi dipende dalla creatività, dal catalogo e dalla richiesta selezionati.

>[!NOTE]
>
>L’agente di controllo qualità è disponibile per i creativi display dinamici, non per i creativi standard o per i creativi video dinamici. In [!UICONTROL Creative Libraries], l&#39;azione è disponibile solo per i creativi dinamici basati su modelli dinamici.

### Apri l’agente di controllo qualità {#open-qa-agent}

1. Apri una creatività dinamica salvata per il controllo qualità in uno dei seguenti modi:

   * **Da [!UICONTROL Creative Libraries]:**

     1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

     1. Fai clic sul nome della libreria per aprirla.

     1. Nella scheda **[!UICONTROL Creatives]** fare clic su **[!UICONTROL ...]** accanto al nome della creatività dinamica e quindi su **[!UICONTROL QA Agent]**.

   * **Da [!UICONTROL Creative Studio]:**

     1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Creative Studio]**.

     1. Nella scheda **[!UICONTROL Creatives]**, individua la creatività dinamica nella relativa libreria creativa sotto la sezione [!UICONTROL Generate or Build Creatives].

     1. Posizionare il cursore sulla scheda creativa e fare clic su **[!UICONTROL ...]** > **[!UICONTROL QA Assistant]**.

   Viene visualizzata la schermata **[!UICONTROL Dynamic Creative QA]** con un&#39;area di lavoro di anteprima e il pannello chat di **[!UICONTROL AI Assistant]**.

1. Se la creatività utilizza più cataloghi, seleziona il catalogo da esaminare da **[!UICONTROL Catalog]** nell&#39;intestazione.

   L&#39;assistente analizza il catalogo selezionato. Il selettore catalogo è disattivato quando il contenuto creativo utilizza un solo catalogo.

### Analizzare e filtrare gli annunci con AI {#analyze-ads}

1. Nel pannello **[!UICONTROL AI Assistant]**, digitare una richiesta in **[!UICONTROL Ask anything]** e premere **[!UICONTROL Enter]** oppure fare clic su uno dei prompt suggeriti:

   * **[!UICONTROL Run a comprehensive QA pass on this dynamic creative]**
   * **[!UICONTROL Group ads by product]**
   * **[!UICONTROL Filter ads by geography]**
   * **[!UICONTROL Show all ads with headlines over 80 characters]**

   L’assistente risponde nel pannello chat e visualizza le righe del catalogo corrispondenti come anteprime di annunci sull’area di lavoro. Fino a quando non invii una richiesta, l’area di lavoro ti chiede di chiedere all’assistente di analizzare il catalogo.

1. Continua a perfezionare la revisione con le richieste di follow-up. L’assistente può aiutarti a:

   * Filtra gli annunci per segmento di pubblico, lingua, area geografica o codice postale.
   * Controlla la lunghezza dei caratteri utilizzando una soglia specificata.
   * Verifica la presenza di errori di feed, contenuti mancanti e contenuti sospetti.
   * Rivedi lo stato della traduzione.
   * Confrontare le varianti del test A/B.
   * Raggruppa gli annunci per la revisione, ad esempio per prodotto o problema.

   Verifica le risposte dell’assistente ed esamina le anteprime prima di salvare le modifiche.

### Esaminare anteprime e avvisi {#review-previews}

* Utilizza la barra degli strumenti dell’area di lavoro per:

  * Regolare lo zoom.
  * Passa da **[!UICONTROL Thumbnail view]** a **[!UICONTROL Actual size]**.
  * Fare clic su **[!UICONTROL Replay animations]** per riprodurre nuovamente le anteprime.
  * Selezionare il numero di righe per pagina, selezionare un numero di pagina oppure utilizzare **[!UICONTROL Previous page]** e **[!UICONTROL Next page]**.

* Quando l’assistente raggruppa i risultati, fai clic sul collegamento per visualizzare tutti i creativi di un gruppo. Utilizzare **[!UICONTROL Back to groups]** per tornare ai risultati raggruppati oppure **[!UICONTROL Catalog Rows]** per uscire dalla visualizzazione raggruppata.

* Quando un&#39;anteprima mostra **[!UICONTROL Issues detected]**, posiziona il cursore sull&#39;indicatore per visualizzare i dettagli del problema.

* Quando gli avvisi del catalogo sono disponibili, fare clic su **[!UICONTROL View Alerts]**. Nella finestra di dialogo **[!UICONTROL Alerts]** sono elencati il catalogo, il numero di riga, la colonna e il messaggio di errore per ogni problema. Fare clic su **[!UICONTROL Close]** per tornare all&#39;area di lavoro.

### Correggere i valori del catalogo {#correct-catalog-values}

Puoi modificare manualmente i valori del catalogo da un’anteprima dell’annuncio senza uscire dalla schermata Controllo qualità.

1. Nell&#39;anteprima da correggere fare clic su **[!UICONTROL Edit]**.

1. Nella finestra di dialogo di modifica, selezionare le colonne da modificare in **[!UICONTROL Catalog columns to edit]**. Per trovare una colonna, utilizzare **[!UICONTROL Search columns]**.

1. In **[!UICONTROL Columns content]**, aggiornare i valori dei campi selezionati.

1. Fare clic su **[!UICONTROL Update]**.

   L’anteprima viene aggiornata per riflettere i valori aggiornati. Le modifiche apportate al catalogo vengono pubblicate solo dopo il salvataggio della creatività dinamica.

>[!IMPORTANT]
>
>Queste modifiche aggiornano i dati del catalogo, non solo l’anteprima dell’annuncio. Rivedi i valori prima di pubblicarli.

### Salva le modifiche o esci {#save-or-exit}

* Per salvare la creatività dinamica e pubblicare eventuali modifiche al catalogo:

  1. Fare clic su **[!UICONTROL Save Dynamic Creative]** nell&#39;intestazione.

  1. Conferma il salvataggio:

     * Per un nuovo contenuto creativo, nella finestra di dialogo di conferma **[!UICONTROL Create Dynamic Creative]**, fare clic su **[!UICONTROL Create]**.
     * Per un elemento creativo esistente, nella finestra di dialogo di conferma **[!UICONTROL Update Dynamic Creative]**, fare clic su **[!UICONTROL Update]**.

     Si ritorna alla libreria creativa o a [!UICONTROL Creative Studio], a seconda di dove è stata aperta la schermata di controllo qualità.

* Per uscire senza pubblicare le modifiche al catalogo in sospeso, fare clic su **[!UICONTROL Cancel]** nell&#39;intestazione della pagina.

## Visualizza il registro delle modifiche per un contenuto creativo dinamico {#view-change-log}

1. Nel menu principale, fare clic su **[!UICONTROL Creative Studio]**.

1. Nella scheda **[!UICONTROL Creatives]**, posizionare il cursore sulla scheda creativa e fare clic su **[!UICONTROL ...]** > **[!UICONTROL Change Log]**.

## Duplicare una creatività dinamica {#duplicate-dynamic-creative}

Duplica un contenuto creativo dinamico per aggiungere un nuovo contenuto creativo con le stesse impostazioni alla libreria. In seguito potrai rinominare il nuovo contenuto creativo e modificare le impostazioni in base alle tue esigenze.

1. Nel menu principale, fare clic su **[!UICONTROL Creative Studio]**.

1. Nella scheda **[!UICONTROL Creatives]**, posizionare il cursore sulla scheda creativa e fare clic su **[!UICONTROL ...]** > **[!UICONTROL Duplicate]**.

   La nuova creatività è denominata `<original name> (copy)`.

## Eliminare una creatività dinamica {#delete-dynamic-creative}

1. Nel menu principale, fare clic su **[!UICONTROL Creative Studio]**.

1. Nella scheda **[!UICONTROL Creatives]**, posizionare il cursore sulla scheda creativa e fare clic su **[!UICONTROL ...]** > **[!UICONTROL Delete]**.

1. Nel messaggio di conferma, fare clic su **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Informazioni su Creative Studio in Advertising Creative](creative-studio-about.md)
>* [Gestione di annunci standard in Creative Studio](creative-studio-manage-standard-ads.md)
>* [Gestione dei modelli in Creative Studio](creative-studio-manage-templates.md)
