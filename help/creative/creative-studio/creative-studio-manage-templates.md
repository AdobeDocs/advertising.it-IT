---
title: Gestire i modelli di annunci in Creative Studio
description: Scopri come creare, importare, organizzare e gestire i modelli di annunci in Adobe Advertising Creative.
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: fcd97d29c5009d22100283970892d258043b2d90
workflow-type: tm+mt
source-wordcount: '3697'
ht-degree: 1%
---
# Gestisci modelli di annunci in [!UICONTROL Creative Studio]

Crea, importa e gestisci modelli di annunci video e di visualizzazione da utilizzare nelle sessioni di generazione di annunci.

## Visualizzazione [!UICONTROL Creative Studio] > [!UICONTROL Templates]

La scheda **[!UICONTROL Templates]** fornisce azioni rapide per creare o importare nuovi modelli di annunci.

Nella scheda [!UICONTROL Templates] sono inoltre elencati i modelli di annunci esistenti nella parte inferiore della pagina <!-- Only in the Templates tab -->come [schede singole (impostazione predefinita) o come tabelle/elenchi](/help/creative/introduction/customize-data-views.md). L&#39;elenco dei modelli di annunci include schede per [!UICONTROL All], [!UICONTROL System Templates] (che il tuo Account Team di Adobe carica sul tuo account) e [!UICONTROL User Templates]. Per impostazione predefinita, vengono visualizzati i modelli di annunci per tutti gli inserzionisti. Per visualizzare solo i modelli di annuncio per un inserzionista specifico, seleziona dall’elenco degli inserzionisti nella parte superiore della pagina.

<!--
Probably not necessary:

* **[!UICONTROL Card view]** &mdash; Displays templates as cards. Each card shows a preview thumbnail and the ad dimensions. Hovering a card reveals action controls.

* **[!UICONTROL Table view]** &mdash; Displays templates in a table with columns for **[!UICONTROL Name]**, **[!UICONTROL Type]**, **[!UICONTROL Status]**, **[!UICONTROL Size/Duration]**, **[!UICONTROL Advertiser]**, and **[!UICONTROL Updated]**. Click the **[!UICONTROL Name]** or **[!UICONTROL Updated]** column header to sort ascending or descending. Pagination controls appear at the bottom of the list.
-->

### Azioni disponibili

<!--  Figure out how to handle these, which relate to the template list at the bottom of the page: * [Browse and search templates](#browse-search) -->

Creazione:

* [Generare un modello di annuncio utilizzando IA](#template-generate)

* [Creare manualmente un modello di annuncio](#template-create)

* [Importare modelli di annunci HTML5](#templates-import)

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

## Generare un modello di annuncio utilizzando IA {#template-generate}

*funzionalità Beta*

Utilizzare AI in [!UICONTROL Creative Studio] per convertire un&#39;immagine annuncio di visualizzazione statica esistente in un modello di annuncio di visualizzazione modificabile. Una procedura guidata in tre passaggi consente di generare e rivedere il modello, richiedere le modifiche utilizzando il linguaggio naturale e aprire l’editor modelli per apportare modifiche manuali e salvare il modello.

### Prerequisiti

È necessario un annuncio immagine statico in una libreria Creative. Questo flusso di lavoro seleziona gli annunci dalle librerie; non carica una nuova immagine direttamente nella finestra di dialogo di generazione.

<!--

Publish this when prompt-based generation becomes available:

To generate a template from an existing image, you need a static image ad in a Creative Library. This option selects ads from your libraries; it doesn't upload a new image directly in the generation dialog. You don't need an existing ad image to generate a template from a prompt.

-->

### Passaggio 1: generare e rivedere il modello

1. Nel menu principale, fare clic su **[!UICONTROL Creative Studio]**.

1. Fare clic sulla scheda **[!UICONTROL Templates]**.

1. (Facoltativo) Seleziona un inserzionista dall&#39;elenco degli inserzionisti nella parte superiore della pagina per visualizzarne le librerie.

1. Nella casella **[!UICONTROL Use AI to Generate a New Display Ad Template]** fare clic su **[!UICONTROL Generate]**.

1. Nella finestra di dialogo **[!UICONTROL Generate New Ad Template]**, seleziona **[!UICONTROL Generate from Existing Standard Ad Image]** se non è già selezionato.

1. Selezionare la libreria contenente l&#39;annuncio immagine dall&#39;elenco **[!UICONTROL Ad Library]**.

1. Posizionare il cursore sulla scheda dell&#39;annuncio immagine e fare clic su **[!UICONTROL Use this Standard Ad]**.

   La generazione inizia automaticamente, utilizzando la larghezza e l’altezza dell’annuncio selezionato.

<!--

Switch to this when prompt-based generation becomes available:

1. In the **[!UICONTROL Generate New Ad Template]** dialog, choose how to generate the template:

   * **[!UICONTROL Generate from Prompt]:** Describe the ad template you want to create using a text prompt.

   * **[!UICONTROL Generate from Existing Standard Ad Image]:** Convert an existing static image ad into an editable template.

1. Follow the steps for your selected option:

   * From a prompt:

      1. Enter a description of the template you want to create. Include details such as the layout, headline, call to action, and visual style.

      1. Follow the on-screen instructions to generate the template.

   * From an existing standard ad image:

      1. Select the library containing the image ad from the **[!UICONTROL Ad Library]** list.

      1. Hold the cursor over the image ad card and click **[!UICONTROL Use this Standard Ad]**.

         Generation begins automatically, using the selected ad's width and height.

-->

1. [Rivedi e perfeziona il modello generato](#template-review).

### Passaggio 2: rivedere e perfezionare il modello {#template-review}

1. Attendere il termine della generazione, quindi esaminare l&#39;anteprima del modello e il pannello **[!UICONTROL Layers]**, se disponibile.

   Controlla il testo, le immagini e il layout prima di utilizzare il modello. I livelli mostrati qui sono per la revisione; apporta modifiche manuali nell&#39;editor modelli.

1. (Facoltativo) Richiedi modifiche al modello generato:

   1. Nel campo **[!UICONTROL Ask the AI for any changes]**, descrivere le modifiche desiderate. Immettere ad esempio `Change the headline to "Limited Time Offer" and the button text to "Shop Now"`.

   1. Fare clic su **[!UICONTROL Regenerate]**.

   1. Rivedi l’anteprima aggiornata. Ripetere l&#39;operazione in base alle esigenze.

1. Quando si è pronti per continuare, fare clic su **[!UICONTROL Use this Ad Template]**.

   Il modello generato si apre nell’editor di modelli di visualizzazione.

### Passaggio 3: modificare e salvare il modello {#template-save}

>[!TIP]
>
> L’assistente AI utilizza una libreria di font open-source per trovare una corrispondenza più stretta per il font nell’annuncio. Per utilizzare un tipo di carattere personalizzato, caricarlo nella scheda [!UICONTROL Assets] o dall&#39;editor modelli, quindi sostituire il tipo di carattere generato nell&#39;editor.
>
> Per ottenere risultati ottimali, sostituisci il logo generato dall’intelligenza artificiale con il logo originale, perfetto per i pixel, nell’editor modelli.

1. Nell&#39;editor modelli, esaminare gli elementi generati e apportare le modifiche rimanenti utilizzando i [controlli dell&#39;editor modelli](#template-controls).

1. Fare clic su **[!UICONTROL Save]**.

1. Nella finestra di dialogo **[!UICONTROL Update Template]**, immettere o aggiornare **[!UICONTROL Template name]**, selezionare **[!UICONTROL Advertiser]** e facoltativamente aggiungere tag.

1. Fare clic su **[!UICONTROL Update]** per salvare il modello e tornare alla visualizzazione **[!UICONTROL Templates]**.

   Per salvare una copia separata, fare clic su **[!UICONTROL Save As New]**.

Puoi quindi utilizzare il modello per [generare varianti di annunci](#ad-variations-generate).

### Risoluzione dei problemi {#troubleshooting}

| Problema | Cosa fare |
| --- | --- |
| Non sono elencate librerie o annunci di immagini durante la generazione da un’immagine | Controlla l&#39;inserzionista selezionato e **[!UICONTROL Ad Library]**. Se la libreria non dispone di immagini pubblicitarie standard, seleziona un’altra libreria contenente un annuncio immagine statico esistente. |
| La generazione basata su immagini non riesce o l’immagine non può essere convertita | Rivedi il messaggio visualizzato, fai clic su **[!UICONTROL Back to library]**, quindi seleziona un&#39;immagine e riprova. |

<!--

Add when prompt-based generation is available:

| Prompt-based generation fails | Review the displayed message and revise your prompt before trying again. |

-->

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

   * Per aggiungere un modello come preferito, fare clic su ![Preferito](/help/creative/assets/favorite-null.png "Preferito").

   * Per rimuovere un modello come preferito, fare clic su ![Preferito](/help/creative/assets/favorite.png "Preferito").

## Eliminare un modello di annuncio {#template-delete}

1. Nel menu principale, fare clic su **[!UICONTROL Creative Studio].**

1. Fare clic sulla scheda **[!UICONTROL Templates]**.

1. Tenere premuto il cursore sulla scheda modello o sulla riga tabella e fare clic su **[!UICONTROL ...]** > **[!UICONTROL Delete]**.

1. Nel messaggio di conferma, fare clic su **[!UICONTROL Delete]**.

## Controlli dell’editor modelli {#template-controls}

Gli editor di modelli video e di visualizzazione forniscono una barra degli strumenti sopra l&#39;area di lavoro per annullare le modifiche e regolare la visualizzazione, pannelli a sinistra per aggiungere risorse ed elementi e un pannello [!UICONTROL Layers] a destra per gestire i livelli. Gli strumenti per la modifica degli elementi selezionati e per il controllo della durata e della riproduzione differiscono tra i modelli di visualizzazione e i modelli video.

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

### Annullare le modifiche e regolare la visualizzazione area di lavoro

La barra degli strumenti delle azioni generali si trova sopra l’area di modifica nell’editor dei modelli di annunci e si divide in due parti (sinistra e destra).

#### Visualizzare i modelli di annuncio

| Controllo | Descrizione |
| --- | --- |
| **[!UICONTROL Undo]** | Annulla l&#39;ultima azione. |
| ![Ripeti](/help/creative/assets/cs-icon-redo.png "Ripeti") **[!UICONTROL Redo]** | Ripete l&#39;ultima azione annullata. |
| **[!UICONTROL Links]** | Apre un pannello per gestire gli URL di click-through associati agli elementi del modello. |
| Controlli di zoom | Fare clic su **[!UICONTROL Zoom out]** o **[!UICONTROL Zoom in]** per regolare l&#39;ingrandimento dell&#39;area di lavoro (10%-150%, con incrementi del 10%). Fare clic sull&#39;etichetta del livello di zoom, che mostra **[!UICONTROL Auto]** quando l&#39;area di lavoro viene adattata automaticamente o una percentuale quando impostata manualmente, per aprire un menu con le opzioni **[!UICONTROL Auto-Fit Page]**, **[!UICONTROL 100% Zoom]**, **[!UICONTROL 50% Zoom]**, **[!UICONTROL Zoom In]** e **[!UICONTROL Zoom Out]**. |
| Dimensione annuncio | Mostra le dimensioni correnti dell’annuncio (ad esempio, 300 × 250). Fai clic su per aprire il selettore dimensioni, che offre sei dimensioni standard IAB comunemente utilizzate come schede, più un menu a discesa con tutte le 19 dimensioni standard di annunci IAB. La dimensione predefinita per i nuovi modelli è 300 × 250 (Rettangolo Medium). |
| ![Apri pannello Livelli](/help/creative/assets/layers-panel-open.png "Apri pannello Livelli") | Apre il pannello [!UICONTROL Layers]. Viene visualizzato solo quando il pannello [!UICONTROL Layers] è chiuso. |

#### Modelli di annunci video

| Controllo | Descrizione |
| --- | --- |
| **[!UICONTROL Undo]** / ![Ripeti](/help/creative/assets/cs-icon-redo.png "Ripeti") **[!UICONTROL Redo]** | Annulla o ripristina l&#39;ultima azione. |
| Controlli di zoom | Fare clic su **[!UICONTROL Zoom out]** o **[!UICONTROL Zoom in]** per regolare l&#39;ingrandimento dell&#39;area di lavoro. Fare clic sul livello di zoom per aprire un menu con le opzioni: **[!UICONTROL Auto-Fit Page]**, **[!UICONTROL 100% Zoom]**, **[!UICONTROL 50% Zoom]**, **[!UICONTROL Zoom In]** e **[!UICONTROL Zoom Out]**. |
| ![Apri pannello Livelli](/help/creative/assets/layers-panel-open.png "Apri pannello Livelli") | Apre il pannello [!UICONTROL Layers]. Viene visualizzato solo quando il pannello [!UICONTROL Layers] è chiuso. |

<!--

Not there as of 10/15:

| Page resize | Opens the page-size controls to change the video template dimensions. |
| **[!UICONTROL Preview]** | Opens a preview of the video template. |

   -->

### Aggiungere risorse ed elementi

Il pannello a sinistra consente di aggiungere risorse e elementi di annunci al modello. Fai clic su un’icona per aprirne il pannello del contenuto; fai di nuovo clic sulla stessa icona per chiuderla.

#### Visualizzare i modelli di annuncio

| Icona | Descrizione |
| --- | --- |
| **[!UICONTROL Search]** | Cerca in tutti i tipi di risorse della libreria. |
| **[!UICONTROL Upload]** | Carica immagini o file di font nell’editor per utilizzarli nel modello corrente. Puoi caricare fino a 20 file alla volta. |
| **[!UICONTROL Templates]** | Sfoglia i modelli di annunci dalla libreria di Creative Studio per utilizzarli come livello di base o elemento di riferimento. |
| **[!UICONTROL My Assets]** | Sfoglia tutte le risorse caricate nella scheda [!UICONTROL Assets] di Creative Studio. |
| **[!UICONTROL Images]** | Sfogliare solo le risorse immagine caricate nella scheda [!UICONTROL Assets] di Creative Studio. |
| **[!UICONTROL Text]** | Aggiungi un elemento di testo all’area di lavoro, compresi eventuali font personalizzati caricati. |
| **[!UICONTROL Elements]** | Aggiungere forme ed elementi di layout quali pulsanti e rettangoli. |

Puoi trascinare un elemento da qualsiasi pannello direttamente nell’area di lavoro, oppure fare clic su di esso per posizionarlo nella posizione predefinita.

#### Modelli di annunci video

| Icona | Descrizione |
| --- | --- |
| **[!UICONTROL Search]** | Cerca in tutti i tipi di risorse della libreria. |
| **[!UICONTROL Upload]** | Carica file immagine, video, audio o font (TTF, OTF, WOFF, WOFF2) nell’editor per l’utilizzo nel modello corrente. Puoi caricare fino a 20 file alla volta. |
| **[!UICONTROL Templates]** | Sfoglia i modelli di annunci dalla libreria di Creative Studio. |
| **[!UICONTROL My Assets]** | Sfoglia tutte le risorse caricate nella scheda [!UICONTROL Assets] di Creative Studio. |
| **[!UICONTROL Images]** | Sfogliare solo le risorse immagine caricate nella scheda [!UICONTROL Assets] di Creative Studio. |
| **[!UICONTROL Video]** | Sfoglia solo le risorse video caricate nella scheda Creative Studio [!UICONTROL Assets]. |
| **[!UICONTROL Audio]** | Sfoglia solo le risorse audio caricate nella scheda Creative Studio [!UICONTROL Assets]. |
| **[!UICONTROL Text]** | Aggiungi un elemento di testo all’area di lavoro, compresi eventuali font personalizzati caricati. |
| **[!UICONTROL Elements]** | Aggiungere forme ed elementi vettoriali. |

Puoi trascinare un elemento da qualsiasi pannello direttamente nell’area di lavoro, oppure fare clic su di esso per posizionarlo nella posizione predefinita.

### Modifica elementi selezionati

Fai clic su un elemento nell’area di lavoro di modifica per selezionarlo. A seconda del tipo di modello, vengono visualizzate una o più barre degli strumenti con i controlli per tale elemento.

I controlli variano in base al tipo di elemento.

<!-- From inspectorbar.ts -->

#### Barra degli strumenti di modifica dei modelli di visualizzazione

| Controllo | Tipi di elementi | Descrizione |
| --- | --- | --- |
| **[!UICONTROL Properties]** | Tutti | Apre un pannello per modificare il nome del livello, contrassegnarlo come dinamico (scambiabile durante la generazione di annunci) e impostare un URL di click-through (solo collegamenti). Al di sotto, scegliere uno stato **[!UICONTROL Default]**, **[!UICONTROL Hover]**, **[!UICONTROL Click]** o **[!UICONTROL Focus]** per applicare uno stile all&#39;elemento per tale stato di interazione, quindi modificare lo stile (solo testo e collegamenti), le decorazioni (riempimento, bordo, raggio angolo), le dimensioni e la posizione in base al tipo di elemento. |
| **[!UICONTROL Effects]** | Tutti | Apre un pannello in cui si sceglie uno stato **[!UICONTROL Default]**, **[!UICONTROL Hover]**, **[!UICONTROL Click]** o **[!UICONTROL Focus]** a cui applicare effetti per lo stato di interazione, quindi regola **[!UICONTROL Transform]**, **[!UICONTROL Transition]**, **[!UICONTROL Box Shadow]**, **[!UICONTROL Filter]**, **[!UICONTROL Blend Mode]** e **[!UICONTROL Cursor]** sezioni. Gli elementi di testo includono anche una sezione **[!UICONTROL Text Shadow]**. |
| **[!UICONTROL Animations]** | Tutti | Apre un pannello per impostare l&#39;ora di entrata e di uscita del livello sulla timeline e per configurare i predefiniti **[!UICONTROL Entrance Animation]**, **[!UICONTROL Loop Animation]** e **[!UICONTROL Exit Animation]** con durata e andamento. Include **[!UICONTROL Copy]**, **[!UICONTROL Paste]** e **[!UICONTROL Reset]** azioni. |
| **[!UICONTROL Crop]** | Immagini | Apre una barra degli strumenti per tagliare l&#39;immagine. Selezionare un predefinito **[!UICONTROL Aspect Ratio]** (o **[!UICONTROL Free]**), quindi fare clic su **[!UICONTROL Apply]** o **[!UICONTROL Cancel]**. |
| **[!UICONTROL Position]** | Tutti | Apre un menu con **[!UICONTROL Move]** opzioni (**[!UICONTROL Forward]**, **[!UICONTROL Backward]**, **[!UICONTROL To front]**, **[!UICONTROL To back]**), **[!UICONTROL Align to Page]** opzioni (**[!UICONTROL Top]**, **[!UICONTROL Left]**, **[!UICONTROL Middle]**, **[!UICONTROL Center]**, **[!UICONTROL Bottom]**, **[!UICONTROL Right]**, **[!UICONTROL Fit Vertically]**, **[!UICONTROL Fit Horizontally]**, **[!UICONTROL Fit to Page]**) e, per gli elementi non immagine, **[!UICONTROL Layer Level Alignment]** opzioni (le stesse sei opzioni di allineamento più **[!UICONTROL Fit to Content]**). |

#### Barra degli strumenti di modifica dei modelli video

| Controllo | Tipi di elementi | Descrizione |
| --- | --- | --- |
| **[!UICONTROL Shape]** | Forme | Imposta le opzioni specifiche della forma. |
| Controlli ritaglio | Immagini | Regolate il tipo di ritaglio, l&#39;offset e l&#39;arrotondamento. |
| **[!UICONTROL Group]** / **[!UICONTROL Ungroup]** | Più elementi selezionati o un gruppo | Raggruppa gli elementi selezionati o separa un gruppo selezionato. |
| **[!UICONTROL Combine]** | Forme compatibili | Combina le forme selezionate in un&#39;unica forma. |
| **[!UICONTROL Audio replace]** | Audio e video | Sostituisce la traccia audio con un file della libreria di risorse. |
| **[!UICONTROL Typeface]**, **[!UICONTROL Bold]**, **[!UICONTROL Italic]**, **[!UICONTROL Font size]**, **[!UICONTROL Align horizontal]**, **[!UICONTROL Advanced]** | Testo | Consente di regolare la famiglia di caratteri, lo spessore, le dimensioni, l&#39;allineamento orizzontale e altre impostazioni tipografiche avanzate. |
| **[!UICONTROL Image]** / **[!UICONTROL Video]** | Immagini e video | Imposta l&#39;immagine di riempimento o la sorgente video per l&#39;elemento. |
| **[!UICONTROL Trim]** | Video e audio | Apre la modalità di ritaglio per impostare i punti iniziale e finale della clip. |
| ![Volume](/help/creative/assets/volume.png "Volume") ([!UICONTROL Volume]) | Video e audio | Regola il livello audio. |
| ![Velocità riproduzione](/help/creative/assets/speed.png "Velocità riproduzione") ([!UICONTROL Playback speed]) | Video e audio | Regola la velocità di riproduzione. |
| ![Ritaglio](/help/creative/assets/crop.png "Ritaglio") ([!UICONTROL Crop]) | Tutti | Ritaglia l’elemento in un’area personalizzata. |
| Controlli di rotazione e capovolgimento | Tutti | Ruota o capovolge l’elemento selezionato. |
| ![Tratto](/help/creative/assets/stroke.png "Tratto") ([!UICONTROL Stroke]) | Tutti | Imposta il colore e la larghezza del bordo. |
| **[!UICONTROL Text Background]** | Testo | Aggiunge un colore di sfondo dietro il testo. |
| **[!UICONTROL Animations]** | Tutti | Aggiunge o modifica animazioni di entrata, uscita o loop. |
| **[!UICONTROL Style]** | Tutti | Apre un menu con le opzioni **[!UICONTROL Adjustments]**, **[!UICONTROL Filter]**, **[!UICONTROL Effect]** e **[!UICONTROL Blur]**. |
| **[!UICONTROL Shadow]** | Tutti | Aggiunge o modifica un&#39;ombreggiatura esterna. |
| **[!UICONTROL Opacity]** | Tutti | Imposta il livello di trasparenza dell&#39;elemento. |
| **[!UICONTROL Position]** | Tutti | Regola numericamente la dimensione, la posizione e la rotazione dell&#39;elemento. |
| ![Pannello di modifica](/help/creative/assets/cs-template-video-editing-panel.png "Pannello di modifica") | Tutti | Apre o chiude un [pannello di modifica](#detailed-element-properties-for-video-templates) per l&#39;elemento selezionato con ulteriori funzionalità di modifica. |

#### Proprietà elemento dettagliate per i modelli video

Nell&#39;editor dei modelli video, fare clic su ![Pannello di modifica](/help/creative/assets/cs-template-video-editing-panel.png "Pannello di modifica") nella barra degli strumenti per aprire un pannello di modifica per l&#39;elemento selezionato con più funzionalità di modifica. Il pannello di modifica viene visualizzato a sinistra dell&#39;area di lavoro ed è separato dal pannello [!UICONTROL Layers], che elenca i livelli nel modello.

##### Singoli elementi

Quando selezionate una singola immagine, un video, una forma o un elemento di testo, il pannello di modifica mostra le sezioni applicabili di seguito.

| Sezione pannello | Strumento | Controlli |
| --- | --- | --- |
| [!UICONTROL Layer] | Allineamento e posizionamento dei livelli | Allinea il livello selezionato a sinistra, al centro orizzontale, a destra, in alto, al centro verticale o in basso. Il menu di disposizione cambia l&#39;ordine di impilamento da anteriore a posteriore. Questi controlli posizionano il livello stesso e non giustificano il testo all&#39;interno del livello. |
| | [!UICONTROL Rotate & Flip] | Immettere un angolo di rotazione in gradi. Utilizza ![Riflessione orizzontale](/help/creative/assets/cs-template-video-flip.png "Riflessione orizzontale") per specchiare il livello in orizzontale o ![Riflessione verticale](/help/creative/assets/cs-template-video-flip-vertical.png "Riflessione verticale") per specchiarlo in verticale. |
| | ![Opacità](/help/creative/assets/cs-template-video-opacity.png "Opacità") [!UICONTROL Opacity] | Rende il livello selezionato più o meno trasparente. |
| | ![Metodo fusione](/help/creative/assets/cs-template-video-blend-mode.png "Metodo fusione") [!UICONTROL Blend Mode] | Modifica la modalità di combinazione dei colori del livello selezionato con i livelli dietro di esso. |
| | [!UICONTROL Transform]: [!UICONTROL Position & Size] | Apre controlli aggiuntivi per la posizione e le quote del livello. La disponibilità dipende dalle autorizzazioni di trasformazione del livello selezionato. |
| [!UICONTROL Shape] | ![Opzioni forma](/help/creative/assets/cs-template-video-shape-options.png "Opzioni forma") [!UICONTROL Shape] e proprietà specifiche della forma | Modifica la forma e le proprietà disponibili, ad esempio punti, lati, diametro interno, larghezza linea o raggio angolo. I controlli dipendono dalla forma selezionata. |
| | [!UICONTROL Vector]: [!UICONTROL Edit Path] | Attiva la modalità di modifica vettoriale per modificare il percorso della forma, se disponibile. |
| [!UICONTROL Character] | ![Typeface](/help/creative/assets/cs-template-video-typeface.png "Typeface") Typeface, ![Text style](/help/creative/assets/cs-template-video-text-style.png "Text style") text style, ![Bold](/help/creative/assets/cs-template-video-text-bold.png "Bold") bold, ![Italic](/help/creative/assets/cs-template-video-text-italic.png "Italic") italic e ![Font size](/help/creative/assets/cs-template-video-font-size.png "Font size") font size | (Livelli di testo) Modifica la famiglia di caratteri, lo stile e le dimensioni del testo selezionato. |
| | ![Allinea a sinistra](/help/creative/assets/cs-template-video-text-align-l.png "Allinea a sinistra") / ![Allinea al centro](/help/creative/assets/cs-template-video-text-align-c.png "Allinea al centro") / ![Allinea a destra](/help/creative/assets/cs-template-video-text-align-r.png "Allinea a destra") Allineamento testo | (Livelli di testo) Allinea il testo all&#39;interno della cornice a sinistra, al centro o a destra oppure rileva automaticamente l&#39;allineamento. |
| | ![Impostazioni avanzate del testo](/help/creative/assets/cs-template-video-advanced-text.png "Impostazioni avanzate del testo") Impostazioni avanzate del testo | (Livelli di testo) Apre ulteriori impostazioni di composizione tipografica. |
| [!UICONTROL Fill] | ![Riempi](/help/creative/assets/cs-template-video-fill.png "Riempi") Riempi i controlli | Modifica il colore, l&#39;immagine o il riempimento video del livello selezionato. I controlli riflettono il tipo di riempimento corrente e ne aprono le impostazioni. Per il testo, modifica il colore del testo. |
| [!UICONTROL Stroke] | ![Traccia](/help/creative/assets/cs-template-video-stroke.png "Traccia") Controlli traccia | Attiva o disattiva la struttura e ne modifica il colore, la larghezza, lo stile e il posizionamento. Quando la traccia è attivata, vengono visualizzati controlli aggiuntivi. |
| [!UICONTROL Text Background] | ![Sfondo testo](/help/creative/assets/cs-template-video-text-bg.png "Sfondo testo") Controlli sfondo | (Livelli di testo) Aggiunge o modifica lo sfondo dietro il testo. |
| [!UICONTROL Animations] | ![Animazione](/help/creative/assets/cs-template-video-animation.png "Animazione") [!UICONTROL Presets] | Apre i predefiniti di animazione per il livello selezionato, incluse le animazioni di entrata, uscita e loop. |
| [!UICONTROL Appearance] | ![Adeguamenti](/help/creative/assets/cs-template-video-adjustments.png "Adeguamenti") [!UICONTROL Adjustments] | Modifica le proprietà visive del livello selezionato. |
| | ![Filtro](/help/creative/assets/cs-template-video-filter.png "Filtro") [!UICONTROL Filter] | Applica un filtro visivo al livello selezionato. |
| | ![Effetti](/help/creative/assets/cs-template-video-effects.png "Effetti") [!UICONTROL Effect] | Applica un effetto al livello selezionato. |
| | ![Sfocatura](/help/creative/assets/cs-template-video-blur.png "Sfocatura") [!UICONTROL Blur] | Applica una sfocatura al livello selezionato. |
| | ![Ombreggiatura](/help/creative/assets/cs-template-video-shadow.png "Ombreggiatura") [!UICONTROL Shadow] | Aggiunge o modifica l&#39;ombreggiatura del livello selezionato. |

##### Selezioni multiple ed elementi specializzati

Quando selezionate più elementi, un gruppo, un elemento di ritaglio o una clip audio, il pannello di modifica mostra le sezioni specifiche della selezione riportate di seguito. La sezione [!UICONTROL Layer] viene mantenuta anche da più elementi, gruppi e ritagli.

| Sezione pannello | Strumento | Controlli |
| --- | --- | --- |
| [!UICONTROL Layer] | Allineamento e posizionamento dei livelli | Allinea più elementi selezionati o un gruppo. Il menu di disposizione modifica l&#39;ordine di impilamento anteriore-posteriore. |
| | [!UICONTROL Rotate & Flip] | Ruota o capovolge gli elementi o il gruppo selezionato. |
| | ![Opacità](/help/creative/assets/cs-template-video-opacity.png "Opacità") [!UICONTROL Opacity] | Rende gli elementi o i gruppi selezionati più o meno trasparenti. |
| | ![Metodo fusione](/help/creative/assets/cs-template-video-blend-mode.png "Metodo fusione") [!UICONTROL Blend Mode] | Modifica il modo in cui i colori degli elementi o dei gruppi selezionati si combinano con i livelli dietro di essi. |
| | [!UICONTROL Transform]: [!UICONTROL Position & Size] | Apre i controlli per la posizione e le quote degli elementi o dei gruppi selezionati. I controlli disponibili dipendono dagli elementi selezionati. |
| [!UICONTROL Selection] | ![Gruppo](/help/creative/assets/cs-template-video-group.png "Gruppo") Gruppo / ![Separa](/help/creative/assets/cs-template-video-ungroup.png "Separa") Separa | Viene visualizzato sotto [!UICONTROL Layer] per più livelli selezionati o per un gruppo selezionato. Raggruppa i livelli selezionati in modo che possano essere gestiti insieme oppure separa un gruppo in singoli livelli. |
| [!UICONTROL Settings] | ![Ritaglio ritaglio](/help/creative/assets/cs-template-video-cutout-clip.png "Ritaglio ritaglio") / ![Sovrapposizione ritaglio](/help/creative/assets/cs-template-video-cutout-overlay.png "Sovrapposizione ritaglio") Controlli ritaglio | (Livelli di ritaglio) Viene visualizzato sotto [!UICONTROL Layer]. Seleziona il tipo di sfinestratura e ne regola l&#39;offset e l&#39;arrotondamento degli spigoli. |
| [!UICONTROL Audio Properties] | ![Ritaglia](/help/creative/assets/cs-template-video-trim.png "Ritaglia") Ritaglia, ![Volume](/help/creative/assets/cs-template-video-volume.png "Volume") volume e ![Velocità di riproduzione](/help/creative/assets/cs-template-video-playback-speed.png "Velocità di riproduzione") | (Livelli audio) Imposta i punti iniziale e finale della clip, il livello audio e la velocità di riproduzione. |

#### Modificare gli elementi direttamente nell’area di lavoro

##### Visualizzare i modelli di annuncio

| Azione | Descrizione |
| --- | --- |
| **[!UICONTROL Replace]** | (Solo per elementi immagine) Apre il pannello Immagini in modo da poter sostituire l’immagine con una della libreria di risorse. |
| ![Avanti](/help/creative/assets/cs-icon-move-forward.png "Avanti") **[!UICONTROL Move forward]** | Sposta l&#39;elemento di un passo in avanti nell&#39;ordine di sovrapposizione (verso la parte anteriore). |
| ![Indietro](/help/creative/assets/cs-icon-move-backward.png "Indietro") **[!UICONTROL Move backward]** | Sposta l&#39;elemento un passo indietro nell&#39;ordine di sovrapposizione (verso il retro). |
| ![Duplica](/help/creative/assets/cs-icon-duplicate.png "Duplica") **[!UICONTROL Duplicate]** | Crea una copia dell&#39;elemento. |
| ![Elimina](/help/creative/assets/cs-icon-delete.png "Elimina") **[!UICONTROL Delete]** | Rimuove l’elemento dall’area di lavoro. |
| Maniglia di rotazione | Fai clic su e trascina la maniglia sopra un elemento selezionato per ruotarlo. Tenere premuto **[!UICONTROL Shift]** mentre si trascina per agganciare la rotazione a incrementi di 15 gradi. |

Puoi anche fare clic e trascinare un elemento selezionato per riposizionarlo, quindi fare clic e trascinare le maniglie intorno ad esso per ridimensionarlo.

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

Puoi anche fare clic e trascinare un elemento selezionato per riposizionarlo, quindi fare clic e trascinare le maniglie intorno ad esso per ridimensionarlo.

### Controllo tempi e riproduzione

Gli editor video e display visualizzano un pannello timeline nella parte inferiore dell’area di lavoro.

#### Visualizzare i modelli di annuncio

La timeline mostra una traccia per ciascun livello nell&#39;area di lavoro, che si estende sull&#39;intervallo di tempo in cui il livello è visibile in base ai tempi di entrata e uscita dell&#39;animazione. Trascinate la maniglia iniziale o finale di una traccia per regolarne il tempo di entrata o di uscita oppure trascinate una traccia per riordinare i livelli. Fai clic sul righello o trascina la testina di riproduzione per spostarti su un punto nel tempo.

La barra degli strumenti della timeline include un campo **[!UICONTROL Duration]** (0-60 secondi), **[!UICONTROL Play]**/**[!UICONTROL Pause]**, una visualizzazione della durata corrente/totale, un interruttore di loop, **[!UICONTROL Timeline Scale]** controlli di zoom, un pulsante **[!UICONTROL Fit View]** e un interruttore di compressione/espansione.

#### Modelli di annunci video

La timeline mostra tutti i clip video e audio nel modello. La timeline consente di esaminare la disposizione temporale delle clip e di ritagliarle trascinando le maniglie di inizio e di fine. Non potete aggiungere una nuova clip direttamente sulla timeline; aggiungetela invece dal pannello o dall&#39;area di lavoro a sinistra, e apparirà come una clip sulla timeline.

### Gestione livelli

Il pannello [!UICONTROL Layers] sul lato destro dell&#39;area di lavoro elenca tutti gli elementi nel modello e consente di gestirne l&#39;ordine, la visibilità e le proprietà. Per i modelli di visualizzazione, fare clic su **[!UICONTROL Open Layers]** nella barra degli strumenti dell&#39;area di lavoro per aprirla. Per i modelli video, il pannello è aperto per impostazione predefinita.

Fare clic su un livello qualsiasi per selezionare l&#39;elemento corrispondente nell&#39;area di lavoro.

**Schede (solo modelli di annunci visualizzati)**

I modelli di visualizzazione hanno due schede nella parte superiore del pannello [!UICONTROL Layers]:

* **[!UICONTROL Dynamic]** — elenca solo i livelli che possono essere scambiati durante la generazione di annunci, come immagini e testo che l&#39;agente di intelligenza artificiale può sostituire. Questa è la vista predefinita per la generazione di varianti di annuncio.
* **[!UICONTROL All]** - Mostra la gerarchia completa dei livelli per il modello, inclusi i contenitori strutturali. Utilizzare questa visualizzazione per verificare o riorganizzare la nidificazione degli elementi.

I modelli video mostrano tutti i livelli in un unico elenco senza schede.

**Azioni per livello**

Tenete premuto il cursore su un livello per visualizzare le azioni riportate di seguito.

| Azione | Descrizione |
| --- | --- |
| ![Rinomina livello](/help/creative/assets/edit.png "Rinomina livello") **[!UICONTROL Rename layer]** | Consente di immettere un nuovo nome di livello nel pannello. |
| ![Blocca livello](/help/creative/assets/cs-icon-lock.png "Blocca livello") **[!UICONTROL Lock layer]** / ![Sblocca livello](/help/creative/assets/cs-icon-unlock.png "Sblocca livello") **[!UICONTROL Unlock layer]** | Impedisce o consente di spostare, modificare o riordinare il livello. |
| ![Nascondi livello](/help/creative/assets/cs-icon-hidden.png "Nascondi livello") **[!UICONTROL Hide layer]** / ![Mostra livello](/help/creative/assets/cs-icon-visible.png "Mostra livello") **[!UICONTROL Show layer]** | Nasconde o mostra il livello nell&#39;area di lavoro. I livelli nascosti vengono mantenuti nel modello, ma non vengono visualizzati durante il rendering del modello. |
| ![Trascina per riordinare](/help/creative/assets/cs-icon-drag.png "Trascina per riordinare") Trascina per riordinare | (Solo per la visualizzazione di modelli di annunci) Trascinate l&#39;icona Riordina per modificare la posizione del livello nell&#39;ordine di sovrapposizione. Il livello deve essere sbloccato per riordinarlo. |

**Piè di pagina pannello**

| Azione | Descrizione |
| --- | --- |
| ![Duplica livello selezionato](/help/creative/assets/cs-icon-duplicate.png "Duplica livello selezionato") **[!UICONTROL Duplicate selected layer]** | Crea una copia del livello selezionato. |
| ![Elimina livello selezionato](/help/creative/assets/cs-icon-delete.png "Elimina livello selezionato") **[!UICONTROL Delete selected layer]** | Elimina il livello selezionato. |
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

>[!MORELIKETHIS]
>
>* [Informazioni su Creative Studio in Advertising Creative](creative-studio-about.md)
>* [Gestione risorse in Creative Studio](creative-studio-manage-assets.md)
>* [Gestione di annunci standard in Creative Studio](creative-studio-manage-standard-ads.md)
>* [Gestione di creatività dinamiche in Creative Studio](creative-studio-manage-dynamic-ads.md)
