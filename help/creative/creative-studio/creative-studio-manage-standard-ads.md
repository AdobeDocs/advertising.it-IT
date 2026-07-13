---
title: Gestire gli annunci standard in Creative Studio
description: Scopri come creare, modificare, duplicare, scaricare ed eliminare annunci display standard nella libreria creative di Creative Studio.
exl-id: 01d3cdec-80d0-494c-94dd-d9d0ae8ca53c
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: a6ab21a588f5b069ea0783dee711f52d906a46f9
workflow-type: tm+mt
source-wordcount: 1181
ht-degree: 0%

---

# Gestisci annunci standard in [!UICONTROL Creative Studio]

*funzionalità Beta*

La scheda **[!UICONTROL Creatives]** in [!UICONTROL Creative Studio] è la libreria di annunci di visualizzazione standard generati dai modelli. Da qui puoi creare annunci utilizzando [!UICONTROL Ad Variations Generator], modificare gli annunci salvati, generare nuove varianti da un annuncio esistente, visualizzare il registro delle modifiche, duplicare, scaricare ed eliminare.

## Creare annunci standard {#create-standard-ads}

Utilizza [!UICONTROL Ad Variations Generator] per generare contenuti di annunci di visualizzazione da un modello. L’assistente AI genera e perfeziona titoli, CTA, immagini, colori e altro ancora e può creare nuove varianti di dimensioni in una singola sessione.

>[!NOTE]
>
>La generazione di annunci standard attualmente supporta solo i modelli di annunci di visualizzazione. I modelli di annunci video non sono disponibili come punto di partenza, né dalla scheda **[!UICONTROL Creatives]** né dalla scheda **[!UICONTROL Templates]**.

### Prerequisiti

Nella libreria di modelli deve esistere almeno un modello di annuncio visualizzato.

### Generare annunci standard

1. Aprire [!UICONTROL Ad Variations Generator] in uno dei modi seguenti:

   * **Dalla scheda [!UICONTROL Creatives]:**

      1. Nel menu principale, fare clic su **[!UICONTROL Creative Studio]**.

      1. Nella scheda **[!UICONTROL Creatives]**, fare clic su **[!UICONTROL Generate]** nella scheda Azioni rapide **[!UICONTROL Generate standard ads from templates]**.

      1. Nella finestra di dialogo di selezione del modello, fare clic su un modello per selezionarlo, quindi fare clic su **[!UICONTROL Use this template]**.

   * (Visualizza solo annunci) **Dalla scheda [!UICONTROL Templates]:**

      1. Nel menu principale, fare clic su **[!UICONTROL Creative Studio]**.

      1. Fare clic sulla scheda **[!UICONTROL Templates]**.

      1. Posizionare il cursore su una scheda modello e fare clic su **[!UICONTROL ...]** > **[!UICONTROL Generate ad variations]**.

   Verrà aperto [!UICONTROL Ad Variations Generator]. L&#39;area di lavoro mostra la sezione **[!UICONTROL Template Sizes]** con i formati di annuncio disponibili del modello e una sezione **[!UICONTROL Ad Concepts]** in cui verranno visualizzati i contenuti generati.

1. (Facoltativo) Per applicare un profilo marchio agli annunci, seleziona un **[!UICONTROL Brand Profile]** nella barra degli strumenti dell&#39;area di lavoro.

   Durante la generazione del contenuto, l’assistente AI utilizza il logo del tuo marchio, la palette di colori, le linee guida vocali, gli standard di immagine e le linee guida per il canale.

1. Genera varianti di annuncio utilizzando [!UICONTROL AI Assistant]:

   1. Nel campo **[!UICONTROL Ask AI to generate ad variations…]**, digitare una richiesta e premere **[!UICONTROL Enter]** oppure fare clic su uno dei prompt visualizzati:

      * **[!UICONTROL Write 3 headline variations for this template]**
      * **[!UICONTROL Generate 3 versions of this ad that will help with performance]**
      * **[!UICONTROL Create a new size template]**

      L&#39;intelligenza artificiale genera i risultati sull&#39;area di lavoro e li organizza in *concetti*, ognuno dei quali rappresenta una variante di contenuto distinta. Il contatore dei concetti nella sezione **[!UICONTROL Ad Concepts]** tiene traccia del numero di concetti esistenti (ad esempio, **(2/10)**). Sono consentiti fino a 10 concetti per sessione.

   1. Continua a perfezionare inviando messaggi di follow-up. Esempi:

      * &quot;Rendi la copia più divertente e meno aziendale&quot;.
      * &quot;Sostituire il logo con la versione bianca.&quot;
      * &quot;Impostare CTA su &quot;Acquista ora&quot; per tutti i concetti.&quot;
      * &quot;Ridimensiona questo annuncio a tutte le 6 dimensioni di visualizzazione standard IAB.&quot;
      * &quot;Assegna a me 3 concetti di titolo diversi con un’immagine di sfondo corrispondente a ciascuno di essi.&quot;

      >[!NOTE]
      >
      >L’assistente AI può generare e modificare testo (titoli, sottotitoli, CTA, copia del corpo), scambiare immagini di sfondo, applicare colori del marchio, cambiare versioni del logo e creare nuovi modelli di dimensioni. Non è possibile modificare la struttura del modello: posizioni degli elementi, layout, spaziatura, spaziatura interna, famiglia di caratteri, dimensioni dei caratteri o bordi. Apporta modifiche strutturali all’editor modelli prima di iniziare la sessione. Consulta [Modificare un modello](creative-studio-manage-templates.md#edit-template).

   1. Per includere un riferimento visivo in una richiesta, fare clic sul pulsante **[!UICONTROL +]** nell&#39;area di input della chat. Nella finestra di dialogo **[!UICONTROL Select from Asset Library]**:

      * Per utilizzare una risorsa nella libreria di risorse, fai clic sulla risorsa e quindi su **[!UICONTROL Add to chat]**. Invia il messaggio per includere la risorsa come contesto.

      * Per caricare una o più risorse, fare clic su **[!UICONTROL Upload Assets]** e selezionare i file nel dispositivo o nella rete.

1. (Facoltativo) Utilizza la barra degli strumenti dell’area di lavoro per esaminare gli annunci generati:

   * **[!UICONTROL Brand]:** Seleziona o modifica il profilo marchio applicato alla sessione.
   * **[!UICONTROL Zoom in]** / **[!UICONTROL Zoom out]:** Regola il livello di zoom dell&#39;area di lavoro.
   * **[!UICONTROL Fit to screen]:** Reimpostare la visualizzazione in modo da mostrare tutte le dimensioni.
   * **[!UICONTROL Replay animations]:** Riproduci animazioni modello.

   Quando l&#39;IA crea una nuova dimensione, nella nuova scheda dimensioni vengono visualizzati i controlli **[!UICONTROL Adjust]**, **[!UICONTROL Keep]** ed elimina. Fare clic su **[!UICONTROL Keep]** per accettare le dimensioni invariate, fare clic su **[!UICONTROL Adjust]** per aprire il modello nell&#39;editor di visualizzazione in cui è possibile apportare modifiche strutturali e quindi fare clic su **[!UICONTROL Update Ad Format]** per salvare oppure fare clic sull&#39;icona Elimina per rimuovere le nuove dimensioni.

1. (Facoltativo) Gestisci concetti e varianti:

   * Per gestire un concetto, posizionare il cursore sull&#39;etichetta del concetto (ad esempio, **[!UICONTROL Concept 3]**) e fare clic su **[!UICONTROL ...]**, quindi selezionare un&#39;opzione:

      * **[!UICONTROL Add to chat]:** Fa riferimento al concetto nel prompt successivo.
      * **[!UICONTROL Delete]:** Rimuove il concetto.

   * Per gestire una singola variante, posizionare il cursore sulla scheda della variante e fare clic su **[!UICONTROL ...]**, quindi selezionare un&#39;opzione:

      * **[!UICONTROL Add to Chat]:** Fa riferimento alla variante nel prompt successivo. Puoi anche fare clic direttamente sul corpo della scheda della variante per attivare/disattivare la menzione.
      * **[!UICONTROL Edit Data]:** Apre una finestra di dialogo in cui è possibile aggiornare la variante **[!UICONTROL Name]** e l&#39;URL di click-through per ogni tag di click definito nel modello. Fare clic su **[!UICONTROL Save]** per applicare.
      * **[!UICONTROL Delete]:** Rimuove la variante.

1. Quando si è soddisfatti dei concetti generati, fare clic su **[!UICONTROL Save Standard Ads]** nell&#39;intestazione.

   Il pulsante è disattivato finché non esiste almeno un concetto.

1. Nella finestra di dialogo **[!UICONTROL Save Standard Ads]**, specifica le seguenti impostazioni, quindi fai clic su **[!UICONTROL Save Standard Ads]**.

   **[!UICONTROL Advertiser]:** (Obbligatorio) L&#39;inserzionista in cui salvare le creatività.

   **[!UICONTROL Creative Library]:** (Obbligatorio) Libreria creativa in cui salvare le creatività. Il selettore della libreria viene attivato dopo aver selezionato un inserzionista.

   **[!UICONTROL Attach to Bundles]:** (Facoltativo) Se questa opzione è abilitata, le creatività salvate vengono associate a uno o più bundle. Per ogni variante di annuncio, seleziona un bundle oppure immetti un nuovo nome di bundle.

   **\[Impostazioni per ogni annuncio\]:** Per ogni variante di annuncio, puoi visualizzare e, facoltativamente, modificare **[!UICONTROL Name],** **[!UICONTROL Language],** e **[!UICONTROL click URL].**

## Modificare un annuncio standard {#edit-standard-ad}

1. Nel menu principale, fare clic su **[!UICONTROL Creative Studio]**.

1. Nella scheda **[!UICONTROL Creatives]**, posizionare il cursore sulla scheda creativa e fare clic su **[!UICONTROL ...]** > **[!UICONTROL Edit]**.

   Si apre un editor a schermo intero con un&#39;anteprima di un annuncio live a sinistra e un pannello delle impostazioni a destra.

1. Modificare le impostazioni dell&#39;annuncio utilizzando le schede **[!UICONTROL Details]** e **[!UICONTROL Attributes]**:

   Scheda **[!UICONTROL Details]**:

   * **[!UICONTROL Creative Name]:** (obbligatorio) il nome visualizzato per la creatività.
   * **[!UICONTROL Language]:** (obbligatorio) lingua del contenuto dell&#39;annuncio.
   * **[!UICONTROL Creative Size]:** (sola lettura) dimensioni annuncio.
   * **Tag di clic:** Se il modello definisce i tag di clic, ogni tag di clic viene visualizzato come un campo obbligatorio contrassegnato con il nome del tag. Immetti l’URL di destinazione del click-through per ciascun tag.
   * **[!UICONTROL Label]:** (facoltativo) etichette per organizzare i creativi. Selezionare le etichette esistenti o immettere un nuovo tag e fare clic su **[!UICONTROL Add tag].**

   Scheda **[!UICONTROL Attributes]**:

   L’anteprima live viene aggiornata in tempo reale durante la modifica. Scheda **[!UICONTROL Attributes]** non disponibile durante il caricamento dell&#39;anteprima.

   * **Attributi di testo:** Immettere il valore di testo per ogni livello di testo modificabile definito nel modello.
   * **Attributi immagine:** mostra una miniatura dell&#39;immagine corrente. Fare clic su **[!UICONTROL Replace Image]** per caricare un sostituto (PNG, JPEG, GIF, WebP o SVG).

1. Fare clic su **[!UICONTROL Update Creative]**.

## Generare varianti di annuncio per un annuncio standard {#generate-ad-variations}

1. Nel menu principale, fare clic su **[!UICONTROL Creative Studio]**.

1. Nella scheda **[!UICONTROL Creatives]**, posizionare il cursore sulla scheda creativa e fare clic su **[!UICONTROL ...]** > **[!UICONTROL Generate Ad Variations]**.

   [!UICONTROL Ad Variations Generator] si apre con l&#39;annuncio selezionato precaricato.

1. Utilizza l’interfaccia di chat basata su IA per generare e perfezionare ulteriori varianti. Consulta &quot;[Creare annunci standard](#create-standard-ads)&quot; per il flusso di lavoro completo.

## Duplicare un annuncio standard {#duplicate-standard-ad}

Duplica un annuncio standard per aggiungere un nuovo contenuto creativo con le stesse impostazioni alla libreria. In seguito potrai rinominare il nuovo contenuto creativo e modificare le impostazioni in base alle tue esigenze.

1. Nel menu principale, fare clic su **[!UICONTROL Creative Studio]**.

1. Nella scheda **[!UICONTROL Creatives]**, posizionare il cursore sulla scheda creativa e fare clic su **[!UICONTROL ...]** > **[!UICONTROL Duplicate]**.

   La nuova creatività è denominata `<original name> (copy)`.

## Visualizzare il registro delle modifiche di un annuncio standard {#view-change-log}

1. Nel menu principale, fare clic su **[!UICONTROL Creative Studio]**.

1. Nella scheda **[!UICONTROL Creatives]**, posizionare il cursore sulla scheda creativa e fare clic su **[!UICONTROL ...]** > **[!UICONTROL Change Log]**.

   Viene visualizzata una finestra di dialogo con la tabella delle modifiche apportate all’annuncio.

## Scaricare un annuncio standard {#download-standard-ad}

1. Nel menu principale, fare clic su **[!UICONTROL Creative Studio]**.

1. Nella scheda **[!UICONTROL Creatives]**, posizionare il cursore sulla scheda creativa e fare clic su **[!UICONTROL ...]** > **[!UICONTROL Download]**.

   La creatività viene scaricata in base alla normale procedura del browser.

## Eliminare un annuncio standard {#delete-standard-ad}

>[!NOTE]
>
>Questa azione non può essere annullata.

1. Nel menu principale, fare clic su **[!UICONTROL Creative Studio]**.

1. Nella scheda **[!UICONTROL Creatives]**, posizionare il cursore sulla scheda creativa e fare clic su **[!UICONTROL ...]** > **[!UICONTROL Delete]**.

1. Nel messaggio di conferma, fare clic su **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Informazioni su Creative Studio in Advertising Creative](creative-studio-about.md)
>* [Gestione di creatività dinamiche in Creative Studio](creative-studio-manage-dynamic-ads.md)
>* [Gestione dei modelli in Creative Studio](creative-studio-manage-templates.md)
>* [Gestione dei profili del brand in Advertising Creative](/help/creative/brands/brand-manage.md)

