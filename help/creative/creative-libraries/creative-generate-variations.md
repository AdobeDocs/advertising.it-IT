---
title: Generazione di varianti di creatività HTML5 flessibili
description: Scopri come generare e salvare varianti basate sull’intelligenza artificiale di creativi HTML5 flessibili da una libreria creativa.
feature: Creative Standard Creatives
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
subfeature_v2:
  - id: d06c1576-7039-4934-b256-7366e138fbb6
    internal-label: Creative Standard Creatives
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 1cc477f531051d94ea88eaae0a4fb83918e95ea5
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 0%
---
# Generazione di varianti di creatività HTML5 flessibili

Utilizzare [!UICONTROL Ad Variations Generator] per creare nuove varianti di una creatività HTML5 flessibile esistente. L’assistente AI genera e perfeziona titoli, CTA, immagini, colori e altro ancora e può creare nuove varianti di dimensioni in una singola sessione. Salva le varianti risultanti come nuovi annunci standard nella libreria creativa.

>[!NOTE]
>
>È inoltre possibile generare varianti di annunci da [!UICONTROL Creative Studio]. Entrambi i punti di ingresso aprono [!UICONTROL Ad Variations Generator]. Vedere &quot;[Generare varianti di annuncio per un annuncio standard in Creative Studio](/help/creative/creative-studio/creative-studio-manage-standard-ads.md#generate-ad-variations)&quot; per l&#39;altro punto di ingresso.

## Disponibilità {#availability}

L&#39;azione **[!UICONTROL Generate Variations]** è disponibile per i creativi HTML5 flessibili, inclusi quelli basati su modelli di sistema, nella nuova interfaccia utente [!UICONTROL Creative Libraries]. Non è disponibile per altri tipi di creatività, inclusi i creativi dinamici.

L’azione viene disabilitata quando il contenuto creativo non dispone del riferimento interno all’annuncio padre-modello richiesto dal generatore. Questo riferimento non è un&#39;impostazione modificabile; il caricamento o la sostituzione di un file nella scheda **[!UICONTROL Template]** del contenuto creativo non lo imposta esplicitamente.

## Aprire il generatore di varianti dell’annuncio {#open-generator}

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Apri la libreria in uno dei seguenti modi:

   * Fai clic sul nome della libreria.
   * Accanto al nome della libreria, fare clic su **[!UICONTROL ...]** > **[!UICONTROL Open]**.

1. Nella scheda **[!UICONTROL Creatives]** fare clic su **[!UICONTROL ...]** accanto al nome creativo flessibile di HTML5 e quindi su **[!UICONTROL Generate Variations]**.

   [!UICONTROL Ad Variations Generator] si apre con il contenuto del creativo selezionato. L&#39;area di lavoro mostra la sezione **[!UICONTROL Template Sizes]** con i formati di annuncio disponibili del modello e una sezione **[!UICONTROL Ad Concepts]** in cui verranno visualizzati i contenuti generati.

## Generare e perfezionare le varianti {#generate-variations}

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
      >L’assistente AI può generare e modificare testo (titoli, sottotitoli, CTA, copia del corpo), scambiare immagini di sfondo, applicare colori del marchio, cambiare versioni del logo e creare nuovi modelli di dimensioni. Non è possibile modificare la struttura del modello: posizioni degli elementi, layout, spaziatura, spaziatura interna, famiglia di caratteri, dimensioni dei caratteri o bordi. Apporta modifiche strutturali all’editor modelli prima di iniziare la sessione. Consulta [Modificare un modello](/help/creative/creative-studio/creative-studio-manage-templates.md#edit-template).

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

## Salvare le varianti {#save-variations}

1. Quando si è soddisfatti dei concetti generati, fare clic su **[!UICONTROL Save Standard Ads]** nell&#39;intestazione.

   Il pulsante è disattivato finché non esiste almeno un concetto.

1. Nella finestra di dialogo **[!UICONTROL Save Standard Ads]**, controlla le seguenti impostazioni, quindi fai clic su **[!UICONTROL Save Standard Ads]**.

   **[!UICONTROL Advertiser]:** Inserzionista associato alla libreria creativa di origine. Non puoi modificare questo valore.

   **[!UICONTROL Creative Library]:** Libreria creativa di origine in cui vengono salvati i nuovi annunci. Non puoi modificare questo valore.

   **[!UICONTROL Attach to Bundles]:** (Facoltativo) Se questa opzione è abilitata, le creatività salvate vengono associate a uno o più bundle. Per ogni variante di annuncio, seleziona un bundle oppure immetti un nuovo nome di bundle.

   **\[Impostazioni per ogni annuncio\]:** Per ogni variante di annuncio, puoi visualizzare e, facoltativamente, modificare **[!UICONTROL Name]**, **[!UICONTROL Language]** e l&#39;URL di click-through per ogni tag di clic.

   Tornate alla libreria creativa.

>[!MORELIKETHIS]
>
>* [Modifica creatività standard](creative-edit-standard.md)
>* [Gestione di annunci standard in Creative Studio](/help/creative/creative-studio/creative-studio-manage-standard-ads.md)
>* [Gestione dei profili del brand in Advertising Creative](/help/creative/brands/brand-manage.md)
>* [Metadati C2PA in [!UICONTROL Creative Studio]](/help/creative/creative-studio/creative-studio-content-credentials.md)
