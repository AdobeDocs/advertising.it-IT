---
title: Gestione di creatività dinamiche in Creative Studio
description: Scopri come creare, modificare, duplicare ed eliminare creatività dinamiche basate su catalogo in Adobe Advertising Creative Studio.
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 24e27656edda50f29292cb75823ef6cacdb685fe
workflow-type: tm+mt
source-wordcount: 1044
ht-degree: 0%

---

# Gestisci creatività dinamica in [!UICONTROL Creative Studio]

*funzionalità Beta*

La scheda **[!UICONTROL Creatives]** in [!UICONTROL Creative Studio] elenca le tue creatività dinamiche in base alla libreria. Da qui puoi creare nuove creatività dinamiche basate su catalogo, modificare i dettagli e la mappatura degli attributi delle creatività esistenti, visualizzare i registri di modifica, duplicare le creatività ed eliminare le creatività.

## Creare una creatività dinamica {#build-dynamic-creative}

Utilizza questo flusso di lavoro per creare creatività dinamiche basate su catalogo. Una procedura guidata in quattro passaggi ti guida attraverso la selezione di un modello, la connessione di un catalogo e la mappatura dei campi catalogo agli elementi del modello. Dopo la configurazione, [!UICONTROL AI Assistant] ti consente di visualizzare in anteprima e controllare la qualità di ogni combinazione di annunci generata dai dati del catalogo.

Le creatività dinamiche differiscono dagli annunci standard in un modo chiave: l’agente di intelligenza artificiale non può modificare i contenuti originati dal catalogo. Può filtrare, analizzare e segnalare i problemi, ma per modificare il contenuto degli annunci è necessario aggiornare il catalogo sorgente.

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

   Se continui a eseguire il controllo qualità, l’area di lavoro mostra tutte le combinazioni di annunci generate dal catalogo, visualizzate come righe con un’anteprima di ogni voce di catalogo rappresentata nel modello.

1. Se continui il controllo qualità:

   1. Effettua una delle seguenti operazioni:

      * Utilizzare i controlli **[!UICONTROL Zoom in]** e **[!UICONTROL Zoom out]** per regolare la visualizzazione dell&#39;area di lavoro.

      * Utilizzare i controlli di impaginazione (**X-Y di Z**) per scorrere le righe del catalogo.

      * Per modificare una combinazione di annunci:

         1. Posizionare il cursore sulla riga del catalogo e fare clic su **[!UICONTROL Edit]**.

         1. Nella finestra di dialogo **[!UICONTROL Edit Row]**, aggiorna i valori dei campi.

         1. Fare clic su **[!UICONTROL Save]**.

        L’area di lavoro si aggiorna per riflettere i valori aggiornati.

      * Utilizza il pannello chat di **[!UICONTROL AI Assistant]** per analizzare e filtrare le combinazioni di cataloghi. Digitare la richiesta nel campo **[!UICONTROL Ask anything]** oppure fare clic su una delle richieste suggerite:

         * **[!UICONTROL Run a comprehensive QA pass on this dynamic creative]**
         * **[!UICONTROL Show me side-by-side comparisons of A/B testing creatives]**
         * **[!UICONTROL Show me all ads for millennial women in urban markets]**

        L’agente di IA può:

         * Filtra l’area di lavoro per mostrare annunci che corrispondono a un segmento di pubblico, un’area geografica, una lingua, una categoria o un altro campo catalogo specifico.
         * Verifica la presenza di problemi di qualità quali sovraccarichi del limite di caratteri, overflow o pagina al vivo del contenuto, collegamenti immagine interrotti e visibilità della liberatoria.
         * Confrontare le combinazioni di annunci per l’analisi del test A/B.
         * Organizza gli annunci in gruppi per una revisione affiancata.

        L’agente IA non può modificare il contenuto di origine catalogo. Per modificare il contenuto degli annunci, aggiorna il catalogo sorgente.

   1. Salva **[!UICONTROL Save Dynamic Creative]** nell&#39;intestazione.

   1. Nel messaggio di conferma, fare clic su **[!UICONTROL Create]**.

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

## Riapri l’assistente al controllo qualità per una creatività dinamica {#qa-dynamic-creative}

1. Nel menu principale, fare clic su **[!UICONTROL Creative Studio]**.

1. Nella scheda **[!UICONTROL Creatives]**, posizionare il cursore sulla scheda creativa e fare clic su **[!UICONTROL ...]** > **[!UICONTROL QA Assistant]**.

   Viene visualizzata la schermata Controllo di qualità. Consulta &quot;[Passaggio 5: Anteprima e controllo qualità con IA](#qa)&quot; per informazioni sui controlli dell&#39;area di lavoro e sulle funzionalità dell&#39;assistente di IA disponibili.

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
