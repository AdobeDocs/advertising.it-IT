---
title: Gestire i modelli di annunci in Creative Studio
description: Scopri come creare, importare, organizzare e gestire i modelli di annunci nella scheda Modelli di Creative Studio in Adobe Advertising Creative.
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 24e27656edda50f29292cb75823ef6cacdb685fe
workflow-type: tm+mt
source-wordcount: 2509
ht-degree: 2%

---

# Gestisci modelli di annunci in [!UICONTROL Creative Studio]

*funzionalità Beta*

Crea, importa e gestisci modelli di annunci video e di visualizzazione da utilizzare nelle sessioni di generazione di annunci.

## Visualizzazione [!UICONTROL Creative Studio] > [!UICONTROL Templates]

La scheda **[!UICONTROL Templates]** fornisce azioni rapide per creare o importare nuovi modelli di annunci.

Nella scheda sono inoltre elencati i modelli di annunci esistenti nella parte inferiore della pagina <!-- Only in the Templates tab -->come [schede singole (impostazione predefinita) o come tabelle/elenchi](/help/creative/introduction/customize-data-views.md). L&#39;elenco dei modelli di annunci include schede per [!UICONTROL All], [!UICONTROL System Templates] (caricate sul tuo account dal team dell&#39;account Adobe) e [!UICONTROL User Templates]. Per impostazione predefinita, vengono visualizzati i modelli di annunci per tutti gli inserzionisti. Per visualizzare solo i modelli di annuncio per un inserzionista specifico, seleziona dall’elenco degli inserzionisti nella parte superiore della pagina.

<!-- 

Probably not necessary:

* **[!UICONTROL Card view]** &mdash; Displays templates as cards. Each card shows a preview thumbnail and the ad dimensions. Hovering a card reveals action controls.

* **[!UICONTROL Table view]** &mdash; Displays templates in a table with columns for **[!UICONTROL Name]**, **[!UICONTROL Type]**, **[!UICONTROL Status]**, **[!UICONTROL Size/Duration]**, **[!UICONTROL Advertiser]**, and **[!UICONTROL Updated]**. Click the **[!UICONTROL Name]** or **[!UICONTROL Updated]** column header to sort ascending or descending. Pagination controls appear at the bottom of the list.

-->

### Azioni disponibili

<!--  Figure out how to handle these, which relate to the template list at the bottom of the page: * [Browse and search templates](#browse-search) -->

Creazione:

* [Importare modelli di annunci HTML5](#templates-import)

* [Creare manualmente un modello di annuncio](#template-create)

Azioni sui modelli esistenti:

* [Generare varianti di annuncio da un modello di annuncio visualizzato](#ad-variations-generate)

* [Modificare un modello di annuncio](#template-edit)

* [Aggiungere o rimuovere etichette per un modello di annuncio](#template-labels)

* [Visualizzare in anteprima un modello di annuncio](#template-preview)

* [Scaricare un modello di annuncio](#template-download)

* [Aggiungere o rimuovere un modello di annuncio come preferito](#template-favorite)

* [Eliminare un modello di annuncio](#template-delete)

<!--

Move to a Common Tasks chapter:

## Browse and search templates {#browse-search}

### Search

Type in the **[!UICONTROL Search templates]** field and press **[!UICONTROL Enter]** to find templates by name. Click the **[!UICONTROL Clear search]** button to reset.

### Filter by source

Use the filter pills in the toolbar to show a subset of templates:

* **[!UICONTROL All]** &mdash; Shows all templates.
* **[!UICONTROL System Templates]** &mdash; Shows Adobe-provided templates only.
* **[!UICONTROL User Templates]** &mdash; Shows templates you or your team have created or imported.

### Filter by status or format

1. In the main menu, click **[!UICONTROL Creative Studio].**

1. Click the **[!UICONTROL Templates]** tab.

1. Click **[!UICONTROL Filter]** in the toolbar.

1. In the **[!UICONTROL Filters]** dialog, select a filter category:

   * **[!UICONTROL Status]:** Filter by **[!UICONTROL Live]** or **[!UICONTROL Draft]**.
   * **[!UICONTROL Ad Format]:** Filter by **[!UICONTROL Display]** or **[!UICONTROL Video]**.

1. Select one or more options in the category, then click **[!UICONTROL Apply]**.

Applied filters appear as chips below the toolbar. To refine or remove an active filter, click its chip to open a popover where you can toggle options, then click **[!UICONTROL Apply]** or **[!UICONTROL Delete]** to remove the filter. To remove all active filters at once, click **[!UICONTROL Clear All]**.

-->

## Importare modelli di annunci HTML5 {#templates-import}

Carica uno o più modelli HTML5 predefiniti da includere nei pacchetti come file ZIP. I modelli vengono convalidati al momento dell’importazione; l’importazione non riesce se il HTML supera i 200.000 caratteri, il CSS supera i 60.000 caratteri, il modello contiene più di 5.000 elementi DOM o il modello include tag di script non supportati.

1. Nel menu principale, fare clic su **[!UICONTROL Creative Studio].**

1. Seleziona l’inserzionista nella parte superiore della pagina.

1. Fare clic sulla scheda **[!UICONTROL Templates]**.

1. Nella casella **[!UICONTROL Upload HTML5 Templates]** fare clic su **[!UICONTROL Upload]** e quindi selezionare **[!UICONTROL Display Ad Template]** o **[!UICONTROL Video Ad Template]**.

1. Seleziona uno o più file ZIP dal dispositivo o dalla rete.

1. Nella finestra di dialogo **[!UICONTROL Import Templates]**:

   1. Selezionare un **[!UICONTROL Advertiser]**.

      Se hai già selezionato un inserzionista specifico nella parte superiore della pagina, questo viene preselezionato.

   1. (Facoltativo) Per ogni file, modificare **[!UICONTROL Template Name]**.

      Per impostazione predefinita viene utilizzato il nome del file.

   1. (Facoltativo) Per aggiungere altri file, fare clic su **[!UICONTROL Add more]** e selezionare altri file ZIP. Specificare **[!UICONTROL Template Name]** per ogni file aggiuntivo.

1. Fare clic su **[!UICONTROL Import Templates]**.

>[!NOTE]
>
>Se l’importazione non riesce, semplifica il modello o contatta il team dell’account Adobe.

## Creare manualmente un modello di annuncio {#template-create}

Crea una visualizzazione o un modello video vuoto utilizzando l’editor di modelli.

1. Nel menu principale, fare clic su **[!UICONTROL Creative Studio].**

1. Fare clic sulla scheda **[!UICONTROL Templates]**.

1. Nella casella **[!UICONTROL Create New Ad Template]** fare clic su **[!UICONTROL Create]** e quindi selezionare **[!UICONTROL Display Ad Template]** o **[!UICONTROL Video Ad Template]**.

1. (Visualizza annunci) Selezionare le dimensioni del modello di annuncio e quindi fare clic su **[!UICONTROL Continue]**.

1. Configurare le impostazioni del modello utilizzando i [controlli nell&#39;editor modelli](#template-controls).

1. (Facoltativo) Per scaricare una copia del modello definito, fare clic su **[!UICONTROL ...]** > **[!UICONTROL Download]**.

   Il file viene scaricato in base alla normale procedura del browser.

1. Salva il modello:

   1. Effettuare una delle seguenti operazioni:

      * Fare clic su **[!UICONTROL Save]**.

      * Per salvare il modello come bozza, fare clic su **[!UICONTROL ...]** > **[!UICONTROL Save as Draft]**.

   1. Immettere **[!UICONTROL Template name]**, selezionare **[!UICONTROL Advertiser]**, facoltativamente selezionare tag esistenti o aggiungere nuovi tag al modello, quindi fare clic su **[!UICONTROL Save]**.

## Modificare un modello di annuncio {#template-edit}

*Visualizza solo i modelli di annuncio.*

>[!IMPORTANT]
>
>L’agente IA non può modificare il layout del modello, le posizioni degli elementi, la spaziatura o la tipografia. Apporta eventuali modifiche strutturali all’editor modelli prima di generare il contenuto.

1. Nel menu principale, fare clic su **[!UICONTROL Creative Studio].**

1. Fare clic sulla scheda **[!UICONTROL Templates]**.

1. Tenere premuto il cursore sulla scheda modello o sulla riga tabella e fare clic su **[!UICONTROL ...]** > **[!UICONTROL Edit Template]**.

1. Modificare il layout o gli elementi del modello utilizzando i [controlli nell&#39;editor modelli](#template-controls).

1. (Facoltativo) Per scaricare una copia del modello definito, fare clic su **[!UICONTROL ...]** > **[!UICONTROL Download]**.

   Il file viene scaricato in base alla normale procedura del browser.

1. Salva il modello:

   * Fare clic su **[!UICONTROL Save]**.

   * Per salvare il modello come bozza, fare clic su **[!UICONTROL ...]** > **[!UICONTROL Save as Draft]**. Immettere **[!UICONTROL Template name]**, selezionare **[!UICONTROL Advertiser]**, facoltativamente selezionare tag esistenti o aggiungere nuovi tag al modello, quindi fare clic su **[!UICONTROL Save]**.

<!--

I don't see this anywhere:

1. Click **[!UICONTROL Generate Ad Variations]** to proceed to content generation, or navigate away to save your changes.

-->

## Controlli dell’editor modelli {#template-controls}

Gli editor di modelli video e di visualizzazione condividono la stessa barra delle azioni generale sopra l&#39;area di modifica e il pannello [!UICONTROL Layers] a destra. Il pannello sinistro, i controlli per la modifica dei modelli di annunci e la timeline differiscono tra i modelli di visualizzazione e quelli video.

<!--

Removing -- these are actions that are used within specific procedures:

### Top toolbar

The top toolbar above the canvas is the same for both display and video templates.

| Control | Description |
| --- | --- |
| Template name | The current template name, shown at the top of the editor. Click the **[!UICONTROL Edit name]** icon next to the name to rename it inline. |
| **[!UICONTROL Save]** | Saves and publishes the template. |
| **[!UICONTROL ...]** > **[!UICONTROL Save As Draft]** | Saves the template as a draft without publishing. Enter or update the name, select the advertiser, optionally add tags, and click **[!UICONTROL Save]**. |
| **[!UICONTROL ...]** > **[!UICONTROL Download]** | Downloads the current template as a ZIP file. |
| **[!UICONTROL Cancel]** | Discards unsaved changes and returns to the Templates list. |

-->

### Barra delle azioni generali

La barra degli strumenti delle azioni generali si trova sopra l’area di modifica nell’editor dei modelli di annunci e si divide in due parti (sinistra e destra).

#### Visualizzare i modelli di annuncio

| Controllo | Descrizione |
| --- | --- |
| **[!UICONTROL Undo]** | Annulla l&#39;ultima azione. |
| ![Ripeti](/help/creative/assets/cs-icon-redo.png) **[!UICONTROL Redo]** | Ripete l&#39;ultima azione annullata. |
| **[!UICONTROL Links]** | Apre un pannello per gestire gli URL di click-through associati agli elementi del modello. |
| Controlli di zoom | Fare clic su **[!UICONTROL Zoom out]** o **[!UICONTROL Zoom in]** per regolare l&#39;ingrandimento dell&#39;area di lavoro (10%-150%, con incrementi del 10%). Fare clic sull&#39;etichetta del livello di zoom, che mostra **[!UICONTROL Auto]** quando l&#39;area di lavoro viene adattata automaticamente o una percentuale quando impostata manualmente, per aprire un menu con le opzioni **[!UICONTROL Auto-Fit Page]**, **[!UICONTROL 100% Zoom]**, **[!UICONTROL 50% Zoom]**, **[!UICONTROL Zoom In]** e **[!UICONTROL Zoom Out]**. |
| Dimensione annuncio | Mostra le dimensioni correnti dell’annuncio (ad esempio, 300 × 250). Fai clic su per aprire il selettore dimensioni, che offre sei dimensioni standard IAB comunemente utilizzate come schede, più un menu a discesa con tutte le 19 dimensioni standard di annunci IAB. La dimensione predefinita per i nuovi modelli è 300 × 250 (Rettangolo Medium). |
| ![Apri pannello Livelli](/help/creative/assets/layers-panel-open.png "Apri pannello Livelli") | Apre il pannello [!UICONTROL Layers]. Viene visualizzato solo quando il pannello [!UICONTROL Layers] è chiuso. |

#### Modelli di annunci video

| Controllo | Descrizione |
| --- | --- |
| **[!UICONTROL Undo]** / ![Ripeti](/help/creative/assets/cs-icon-redo.png) **[!UICONTROL Redo]** | Annulla o ripristina l&#39;ultima azione. |
| Controlli di zoom | Fare clic su **[!UICONTROL Zoom out]** o **[!UICONTROL Zoom in]** per regolare l&#39;ingrandimento dell&#39;area di lavoro. Fare clic sul livello di zoom per aprire un menu con le opzioni: **[!UICONTROL Auto-Fit Page]**, **[!UICONTROL 100% Zoom]**, **[!UICONTROL 50% Zoom]**, **[!UICONTROL Zoom In]** e **[!UICONTROL Zoom Out]**. |
| ![Apri pannello Livelli](/help/creative/assets/layers-panel-open.png "Apri pannello Livelli") | Apre il pannello [!UICONTROL Layers]. Viene visualizzato solo quando il pannello [!UICONTROL Layers] è chiuso. |

<!-- Not there as of 7/10:  | **[!UICONTROL Preview]** | Opens a preview of the video template. | -->

### Pannello sinistro

Il pannello a sinistra contiene una colonna di icone. Fai clic su un’icona per aprirne il pannello del contenuto; fai di nuovo clic sulla stessa icona per chiuderla.

#### Visualizzare i modelli di annuncio

| Icona | Descrizione |
| --- | --- |
| **[!UICONTROL Search]** | Cerca in tutti i tipi di risorse della libreria. |
| **[!UICONTROL Upload]** | Carica le immagini<!-- not there as of 7/10:  or font files (TTF, OTF, WOFF, WOFF2)--> nell&#39;editor per l&#39;utilizzo nel modello corrente. Puoi caricare fino a 20 file alla volta. |
| **[!UICONTROL Templates]** | Sfoglia i modelli di annunci dalla libreria di Creative Studio per utilizzarli come livello di base o elemento di riferimento. |
| **[!UICONTROL My Assets]** | Sfoglia tutte le risorse caricate nella scheda Creative Studio Assets. |
| **[!UICONTROL Images]** | Sfoglia solo le risorse immagine caricate nella scheda Creative Studio Assets. |
| **[!UICONTROL Text]** | Aggiungi un elemento di testo all’area di lavoro, compresi eventuali font personalizzati caricati. |
| **[!UICONTROL Elements]** | Aggiungere forme ed elementi di layout quali pulsanti e rettangoli. |

Puoi trascinare un elemento da qualsiasi pannello direttamente nell’area di lavoro, oppure fare clic su di esso per posizionarlo nella posizione predefinita.

#### Modelli di annunci video

| Icona | Descrizione |
| --- | --- |
| **[!UICONTROL Search]** | Cerca in tutti i tipi di risorse della libreria. |
| **[!UICONTROL Upload]** | Carica file immagine, video, audio o font (TTF, OTF, WOFF, WOFF2) nell’editor per l’utilizzo nel modello corrente. Puoi caricare fino a 20 file alla volta. |
| **[!UICONTROL Templates]** | Sfoglia i modelli di annunci dalla libreria di Creative Studio. |
| **[!UICONTROL My Assets]** | Sfoglia tutte le risorse caricate nella scheda Creative Studio Assets. |
| **[!UICONTROL Images]** | Sfoglia solo le risorse immagine caricate nella scheda Creative Studio Assets. |
| **[!UICONTROL Video]** | Sfoglia solo le risorse video caricate nella scheda Creative Studio Assets. |
| **[!UICONTROL Audio]** | Sfoglia solo le risorse audio caricate nella scheda Creative Studio Assets. |
| **[!UICONTROL Text]** | Aggiungi un elemento di testo all’area di lavoro, compresi eventuali font personalizzati caricati. |
| **[!UICONTROL Elements]** | Aggiungere forme ed elementi vettoriali. |

Puoi trascinare un elemento da qualsiasi pannello direttamente nell’area di lavoro, oppure fare clic su di esso per posizionarlo nella posizione predefinita.

### Controlli per la modifica di modelli di annunci

Fai clic su un elemento nell’area di lavoro di modifica per selezionarlo. A seconda del tipo di modello, vengono visualizzate una o più barre degli strumenti con i controlli per tale elemento.

#### Barra degli strumenti e pannello di controllo

I controlli variano in base al tipo di elemento.

<!-- From inspectorbar.ts -->

##### Visualizzare i modelli di annuncio

| Controllo | Tipi di elementi | Descrizione |
| --- | --- | --- |
| **[!UICONTROL Properties]** | Tutti | Apre un pannello per modificare il nome del livello, contrassegnarlo come dinamico (scambiabile durante la generazione di annunci) e impostare un URL di click-through (solo collegamenti). Al di sotto, scegliere uno stato **[!UICONTROL Default]**, **[!UICONTROL Hover]**, **[!UICONTROL Click]** o **[!UICONTROL Focus]** per applicare uno stile all&#39;elemento per tale stato di interazione, quindi modificare lo stile (solo testo e collegamenti), le decorazioni (riempimento, bordo, raggio angolo), le dimensioni e la posizione in base al tipo di elemento. |
| **[!UICONTROL Effects]** | Tutti | Apre un pannello in cui si sceglie uno stato **[!UICONTROL Default]**, **[!UICONTROL Hover]**, **[!UICONTROL Click]** o **[!UICONTROL Focus]** a cui applicare effetti per lo stato di interazione, quindi regola **[!UICONTROL Transform]**, **[!UICONTROL Transition]**, **[!UICONTROL Box Shadow]**, **[!UICONTROL Filter]**, **[!UICONTROL Blend Mode]** e **[!UICONTROL Cursor]** sezioni. Gli elementi di testo includono anche una sezione **[!UICONTROL Text Shadow]**. |
| **[!UICONTROL Animations]** | Tutti | Apre un pannello per impostare l&#39;ora di entrata e di uscita del livello sulla timeline e per configurare i predefiniti **[!UICONTROL Entrance Animation]**, **[!UICONTROL Loop Animation]** e **[!UICONTROL Exit Animation]** con durata e andamento. Include **[!UICONTROL Copy]**, **[!UICONTROL Paste]** e **[!UICONTROL Reset]** azioni. |
| **[!UICONTROL Crop]** | Immagini | Apre una barra degli strumenti per tagliare l&#39;immagine. Selezionare un predefinito **[!UICONTROL Aspect Ratio]** (o **[!UICONTROL Free]**), quindi fare clic su **[!UICONTROL Apply]** o **[!UICONTROL Cancel]**. |
| **[!UICONTROL Position]** | Tutti | Apre un menu con **[!UICONTROL Move]** opzioni (**[!UICONTROL Forward]**, **[!UICONTROL Backward]**, **[!UICONTROL To front]**, **[!UICONTROL To back]**), **[!UICONTROL Align to Page]** opzioni (**[!UICONTROL Top]**, **[!UICONTROL Left]**, **[!UICONTROL Middle]**, **[!UICONTROL Center]**, **[!UICONTROL Bottom]**, **[!UICONTROL Right]**, **[!UICONTROL Fit Vertically]**, **[!UICONTROL Fit Horizontally]**, **[!UICONTROL Fit to Page]**) e, per gli elementi non immagine, **[!UICONTROL Layer Level Alignment]** opzioni (le stesse sei opzioni di allineamento più **[!UICONTROL Fit to Content]**). |

##### Modelli di annunci video

| Controllo | Tipi di elementi | Descrizione |
| --- | --- | --- |
| **[!UICONTROL Shape]** | Forme | Imposta le opzioni specifiche della forma. |
| **[!UICONTROL Group]** / **[!UICONTROL Ungroup]** | Più elementi selezionati o un gruppo | Raggruppa gli elementi selezionati o separa un gruppo selezionato. |
| **[!UICONTROL Combine]** | Forme compatibili | Combina le forme selezionate in un&#39;unica forma. |
| **[!UICONTROL Audio replace]** | Audio e video | Sostituisce la traccia audio con un file della libreria di risorse. |
| **[!UICONTROL Typeface]**, **[!UICONTROL Bold]**, **[!UICONTROL Italic]**, **[!UICONTROL Font size]**, **[!UICONTROL Align horizontal]**, **[!UICONTROL Advanced]** | Testo | Consente di regolare la famiglia di caratteri, lo spessore, le dimensioni, l&#39;allineamento orizzontale e altre impostazioni tipografiche avanzate. |
| **[!UICONTROL Image]** / **[!UICONTROL Video]** | Immagini e video | Imposta l&#39;immagine di riempimento o la sorgente video per l&#39;elemento. |
| **[!UICONTROL Trim]** | Video e audio | Apre la modalità di ritaglio per impostare i punti iniziale e finale della clip. |
| ![Volume](/help/creative/assets/volume.png "Volume") ([!UICONTROL Volume]) | Video e audio | Regola il livello audio. |
| ![Velocità riproduzione](/help/creative/assets/speed.png "Velocità riproduzione") ([!UICONTROL Playback speed]) | Video e audio | Regola la velocità di riproduzione. |
| ![Ritaglio](/help/creative/assets/crop.png "Ritaglio") ([!UICONTROL Crop]) | Tutti | Ritaglia l’elemento in un’area personalizzata. |
| ![Tratto](/help/creative/assets/stroke.png "Tratto") ([!UICONTROL Stroke]) | Tutti | Imposta il colore e la larghezza del bordo. |
| **[!UICONTROL Text Background]** | Testo | Aggiunge un colore di sfondo dietro il testo. |
| **[!UICONTROL Animations]** | Tutti | Aggiunge o modifica animazioni di entrata, uscita o loop. |
| **[!UICONTROL Style]** | Tutti | Apre un menu con le opzioni **[!UICONTROL Adjustments]**, **[!UICONTROL Filter]**, **[!UICONTROL Effect]** e **[!UICONTROL Blur]**. |
| **[!UICONTROL Shadow]** | Tutti | Aggiunge o modifica un&#39;ombreggiatura esterna. |
| **[!UICONTROL Opacity]** | Tutti | Imposta il livello di trasparenza dell&#39;elemento. |
| **[!UICONTROL Position]** | Tutti | Regola numericamente la dimensione, la posizione e la rotazione dell&#39;elemento. |

#### Controlli di modifica generali

##### Visualizzare i modelli di annuncio

| Azione | Descrizione |
| --- | --- |
| **[!UICONTROL Replace]** | (Solo per elementi immagine) Apre il pannello Immagini in modo da poter sostituire l’immagine con una della libreria di risorse. |
| ![Avanti](/help/creative/assets/cs-icon-move-forward.png) **[!UICONTROL Move forward]** | Sposta l&#39;elemento di un passo in avanti nell&#39;ordine di sovrapposizione (verso la parte anteriore). |
| ![Indietro](/help/creative/assets/cs-icon-move-backward.png) **[!UICONTROL Move backward]** | Sposta l&#39;elemento un passo indietro nell&#39;ordine di sovrapposizione (verso il retro). |
| ![Duplicato](/help/creative/assets/cs-icon-duplicate.png) **[!UICONTROL Duplicate]** | Crea una copia dell&#39;elemento. |
| ![Elimina](/help/creative/assets/cs-icon-delete.png) **[!UICONTROL Delete]** | Rimuove l’elemento dall’area di lavoro. |

Puoi anche trascinare un elemento selezionato per riposizionarlo e trascinare le maniglie intorno ad esso per ridimensionarlo.

##### Modelli di annunci video

| Azione | Descrizione |
| --- | --- |
| **[!UICONTROL Edit text]** | (Solo per elementi di testo) Passa alla modalità di modifica del testo, che consente di digitare e formattare il testo direttamente nell&#39;area di lavoro. In modalità di modifica del testo, un menu secondario fornisce **[!UICONTROL Text color]**, **[!UICONTROL Bold]**, **[!UICONTROL Italic]** e **[!UICONTROL Text variables]** (segnaposto modello). |
| **[!UICONTROL Replace]** | (Solo per elementi immagine) Apre la libreria di risorse in modo da poter scambiare l’immagine. |
| **[!UICONTROL Bring forward]** | Sposta l&#39;elemento un passo avanti nell&#39;ordine di sovrapposizione. |
| **[!UICONTROL Send backward]** | Sposta l&#39;elemento un passo indietro nell&#39;ordine di sovrapposizione. |
| **[!UICONTROL Duplicate]** | Crea una copia dell&#39;elemento. |
| **[!UICONTROL Delete]** | Rimuove l’elemento dall’area di lavoro. |
| **... >[!UICONTROL Flip horizontal]** | Capovolge l&#39;elemento orizzontalmente di 180 gradi. |
| **... >[!UICONTROL Flip vertical]** | Capovolge l&#39;elemento verticalmente di 180 gradi. |
| **... >[!UICONTROL Copy Element]** | Copia l’elemento negli Appunti dell’area di lavoro. |
| **... >[!UICONTROL Pastes Element]** | Incolla l&#39;elemento copiato. |

Puoi anche trascinare un elemento selezionato per riposizionarlo e trascinare le maniglie intorno ad esso per ridimensionarlo.

### Timeline

Gli editor video e display visualizzano un pannello timeline nella parte inferiore dell’area di lavoro.

#### Visualizzare i modelli di annuncio

La timeline mostra una traccia per ciascun livello nell&#39;area di lavoro, che si estende sull&#39;intervallo di tempo in cui il livello è visibile in base ai tempi di entrata e uscita dell&#39;animazione. Trascinate la maniglia iniziale o finale di una traccia per regolarne il tempo di entrata o di uscita oppure trascinate una traccia per riordinare i livelli. Fai clic sul righello o trascina la testina di riproduzione per spostarti su un punto nel tempo.

La barra degli strumenti della timeline include un campo **[!UICONTROL Duration]** (0-60 secondi), **[!UICONTROL Play]**/**[!UICONTROL Pause]**, una visualizzazione della durata corrente/totale, un interruttore di loop, **[!UICONTROL Timeline Scale]** controlli di zoom, un pulsante **[!UICONTROL Fit View]** e un interruttore di compressione/espansione.

#### Modelli di annunci video

La timeline mostra tutti i clip video e audio nel modello. La timeline consente di esaminare la disposizione temporale delle clip e di ritagliarle trascinando le maniglie di inizio e di fine. Non potete aggiungere una nuova clip direttamente sulla timeline; aggiungetela invece dal pannello o dall&#39;area di lavoro a sinistra, e apparirà come una clip sulla timeline.

### Pannello [!UICONTROL Layers]

Il pannello [!UICONTROL Layers] sul lato destro dell&#39;area di lavoro elenca tutti gli elementi nel modello e consente di gestirne l&#39;ordine, la visibilità e le proprietà. Per i modelli di visualizzazione, fare clic su **[!UICONTROL Open Layers]** nella barra degli strumenti dell&#39;area di lavoro per aprirla. Per i modelli video, il pannello è aperto per impostazione predefinita.

Fare clic su un livello qualsiasi per selezionare l&#39;elemento corrispondente nell&#39;area di lavoro.

**Schede (solo modelli di annunci visualizzati)**

I modelli di visualizzazione hanno due schede nella parte superiore del pannello [!UICONTROL Layers]:

* **[!UICONTROL Dynamic]** — elenca solo i livelli che possono essere scambiati durante la generazione di annunci, come immagini e testo che l&#39;agente di intelligenza artificiale può sostituire. Questa è la vista predefinita per la generazione di varianti di annuncio.
* **[!UICONTROL All]** - Mostra la gerarchia completa dei livelli per il modello, inclusi i contenitori strutturali. Utilizzare questa visualizzazione per verificare o riorganizzare la nidificazione degli elementi.

I modelli video mostrano tutti i livelli in un unico elenco senza schede.

**Azioni per livello**

Tenere premuto il cursore su un livello per visualizzare le azioni seguenti:

| Azione | Descrizione |
| --- | --- |
| ![Rinomina livello](/help/creative/assets/edit.png) **[!UICONTROL Rename layer]** | Consente di immettere un nuovo nome di livello nel pannello. |
| ![Blocca livello](/help/creative/assets/cs-icon-lock.png) **[!UICONTROL Lock layer]** / ![Sblocca livello](/help/creative/assets/cs-icon-unlock.png) **[!UICONTROL Unlock layer]** | Impedisce o consente di spostare, modificare o riordinare il livello. |
| ![Nascondi livello](/help/creative/assets/cs-icon-hidden.png) **[!UICONTROL Hide layer]** / ![Mostra livello](/help/creative/assets/cs-icon-visible.png) **[!UICONTROL Show layer]** | Nasconde o mostra il livello nell&#39;area di lavoro. I livelli nascosti vengono mantenuti nel modello, ma non vengono visualizzati durante il rendering del modello. |
| ![Trascina per riordinare](/help/creative/assets/cs-icon-drag.png) Trascina per riordinare | (Solo per la visualizzazione di modelli di annunci) Trascinate l&#39;icona Riordina per modificare la posizione del livello nell&#39;ordine di sovrapposizione. Il livello deve essere sbloccato per riordinarlo. |

**Piè di pagina pannello**

| Azione | Descrizione |
| --- | --- |
| ![Duplica livello selezionato](/help/creative/assets/cs-icon-duplicate.png) **[!UICONTROL Duplicate selected layer]** | Crea una copia del livello selezionato. |
| ![Elimina livello selezionato](/help/creative/assets/cs-icon-delete.png) **[!UICONTROL Delete selected layer]** | Elimina il livello selezionato. |
| **[!UICONTROL Group selected layers]** (solo modelli video) | Raggruppa due o più livelli selezionati in un unico gruppo. Viene visualizzato solo quando sono selezionati due o più livelli. Potete separare i livelli raggruppati o rimuovere singoli livelli dal gruppo utilizzando i controlli sulla riga del gruppo. |

<!--

These are all saved with the template, but they aren't what you see, as-is, in the template settings per se. Rethink if I should include this, and how to frame it:

## Template settings {#template-settings}

### Display ad template settings

| Setting | Description |
| --- | --- |
| **[!UICONTROL Advertiser]** | (Required) The advertiser this template belongs to. |
| **[!UICONTROL Ad Template Name]** | (Required) A unique name for the template. |
| **[!UICONTROL Type]** | (Required) The HTML5 template type: **[!UICONTROL Static HTML5]** or **[!UICONTROL Dynamic HTML]**. |
| **[!UICONTROL Size]** | (Required) The ad dimensions. |
| **[!UICONTROL Description]** | (Optional) A description of the template. |
| **[!UICONTROL Tags]** | (Optional) One or more labels. Click **[!UICONTROL Add More]** to add additional tags. |
| **ZIP file** | The HTML5 creative ZIP file. For **[!UICONTROL Dynamic HTML]** templates, also upload the template data file (TDF). |

### Video ad template settings

| Setting | Description |
| --- | --- |
| **[!UICONTROL Advertiser]** | (Required) The advertiser this template belongs to. |
| **[!UICONTROL Ad Template Name]** | (Required) A unique name for the template. |
| **[!UICONTROL Description]** | (Optional) A description of the template. |
| **ZIP file** | The video ad template ZIP file. |

-->

## Generare varianti di annuncio da un modello di annuncio visualizzato {#ad-variations-generate}

*Visualizza solo i modelli di annuncio.*

1. Nel menu principale, fare clic su **[!UICONTROL Creative Studio].**

1. Fare clic sulla scheda **[!UICONTROL Templates]**.

1. Tenere premuto il cursore sulla scheda modello o sulla riga tabella e fare clic su **[!UICONTROL ...]** > **[!UICONTROL Generate Ad Variations]**.

   [!UICONTROL Ad Variations Generator] si apre con il modello precaricato.

1. Utilizza l’interfaccia di chat basata su IA per generare e perfezionare i contenuti degli annunci. Consulta &quot;[Gestire gli annunci standard in Creative Studio](creative-studio-manage-standard-ads.md)&quot; per il flusso di lavoro completo.

## Aggiungere o rimuovere etichette per un modello di annuncio {#template-labels}

*Visualizza solo i modelli di annuncio.*

Le etichette consentono di organizzare e filtrare i modelli utente. Impossibile aggiungere etichette ai modelli di sistema.

1. Nel menu principale, fare clic su **[!UICONTROL Creative Studio].**

1. Fare clic sulla scheda **[!UICONTROL Templates]**.

1. Tenere premuto il cursore sulla scheda modello o sulla riga tabella e fare clic su **[!UICONTROL ...]** > **[!UICONTROL Edit Labels]**.

1. Nella finestra di dialogo **[!UICONTROL Edit Labels]**:

   * Per aggiungere un&#39;etichetta, selezionare un&#39;etichetta esistente o immettere un nome nel campo di input e fare clic su **[!UICONTROL Add Tag]**.

   * Per rimuovere un&#39;etichetta, fare clic su **[!UICONTROL X]** accanto al tag etichetta.

1. Fare clic su **[!UICONTROL Save]**.

## Visualizzare in anteprima un modello di annuncio {#template-preview}

1. Nel menu principale, fare clic su **[!UICONTROL Creative Studio].**

1. Fare clic sulla scheda **[!UICONTROL Templates]**.

1. Tenere premuto il cursore sulla scheda modello.

1. Effettuare una delle seguenti operazioni:

   * (Vista a schede) Fai clic sull&#39;icona **[!UICONTROL Preview template]** oppure fai clic su **[!UICONTROL ...]** > **[!UICONTROL Preview]**.

   * (Vista tabella) Fare clic su **[!UICONTROL ...]** > **[!UICONTROL Preview]**.

1. Per i modelli video, fai clic su ![Riproduci](/help/creative/assets/play.png "Riproduci").

## Scaricare un modello di annuncio {#template-download}

1. Nel menu principale, fare clic su **[!UICONTROL Creative Studio].**

1. Fare clic sulla scheda **[!UICONTROL Templates]**.

1. Tenere premuto il cursore sulla scheda modello o sulla riga tabella e fare clic su **[!UICONTROL ...]** > **[!UICONTROL Download]**.

   Il modello viene scaricato come file ZIP in base alla normale procedura del browser.

## Aggiungere o rimuovere un modello di annuncio come preferito {#template-favorite}

*Solo vista a schede*

1. Nel menu principale, fare clic su **[!UICONTROL Creative Studio].**

1. Fare clic sulla scheda **[!UICONTROL Templates]**.

1. Tenere premuto il cursore sulla scheda modello.

1. Effettuare una delle seguenti operazioni:

   * Per aggiungere un modello come preferito, fare clic su ![Preferito](/help/creative/assets/favorite-null.png).

   * Per rimuovere un modello come preferito, fare clic su ![Preferito](/help/creative/assets/favorite.png).

## Eliminare un modello di annuncio {#template-delete}

1. Nel menu principale, fare clic su **[!UICONTROL Creative Studio].**

1. Fare clic sulla scheda **[!UICONTROL Templates]**.

1. Tenere premuto il cursore sulla scheda modello o sulla riga tabella e fare clic su **[!UICONTROL ...]** > **[!UICONTROL Delete]**.

1. Nel messaggio di conferma, fare clic su **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Informazioni su Creative Studio in Advertising Creative](creative-studio-about.md)
>* [Gestione risorse in Creative Studio](creative-studio-manage-assets.md)
>* [Gestione di annunci standard in Creative Studio](creative-studio-manage-standard-ads.md)
>* [Gestione di creatività dinamiche in Creative Studio](creative-studio-manage-dynamic-ads.md)
