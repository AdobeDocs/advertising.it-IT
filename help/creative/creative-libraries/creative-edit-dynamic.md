---
title: Editing e controllo qualità delle creatività dinamiche
description: Scopri come modificare le impostazioni creative dinamiche e il contenuto del catalogo con controllo di qualità in una libreria creativa.
feature: Creative Dynamic Creatives
exl-id: b75b9aeb-ffd0-4b86-aa7a-bd6a22e7a8e4
TQID: 'https://experienceleague.adobe.com/QoQ5p4sFV-ARIMNDbPkp7axfqkVEC3sxJ6MTlPIG22Y'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
subfeature_v2:
  - id: d70c54b0-f069-4a3c-8056-7069a25e110c
    internal-label: Creative Dynamic Creatives
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: ed1682eff9ce28df30a5314de90f6f67c10f338a
workflow-type: tm+mt
source-wordcount: '1118'
ht-degree: 0%
---
# Editing e controllo qualità delle creatività dinamiche

Modifica le impostazioni creative per modificare la configurazione del contenuto, ad esempio il nome, i cataloghi e la mappatura degli attributi. Utilizza l’agente di controllo qualità per rivedere gli annunci risultanti e correggere i valori del catalogo.

## Modificare le impostazioni creative {#edit-creative-settings}

### Dalla nuova interfaccia {#from-the-new-ui}

1. Apri le impostazioni creative:

   * Da una libreria creativa:

     1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

     1. Apri la libreria in uno dei seguenti modi:

        * Fai clic sul nome della libreria.

        * Accanto al nome della libreria, fare clic su **[!UICONTROL ...]** > **[!UICONTROL Open]**.

     1. Nella scheda **[!UICONTROL Creatives]** fare clic su **[!UICONTROL ...]** accanto al nome della creatività e quindi su **[!UICONTROL Edit]**.

   * Da [!UICONTROL Creative Studio]:

     1. Nel menu principale, fare clic su **[!UICONTROL Creative]>[!UICONTROL Creative Studio]**.

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

### Dall’interfaccia utente legacy {#from-the-legacy-ui}

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Fare clic su **[!UICONTROL Switch to classic UI]**.

1. Fai clic sul nome della libreria.

1. Posizionare il cursore sulla riga creativa e fare clic su **[!UICONTROL Edit]**.

1. Modifica le [impostazioni annuncio dinamico](creative-settings-dynamic.md).

1. Fare clic su **[!UICONTROL Continue]** per visualizzare in anteprima le creatività da generare. Nell&#39;anteprima potete effettuare una delle seguenti operazioni:

   * Per filtrare le creatività in base al catalogo, al valore di filtro <!-- explain more--> e alla dimensione dell&#39;annuncio, utilizzare i filtri sopra l&#39;area di anteprima.

   * Per cercare un prodotto in base al suo ID univoco nel campo di ricerca sotto l&#39;area di anteprima.

   * Per modificare le colonne visualizzate, fare clic su ![Filtro colonna](/help/creative/assets/custom-columns.png "Filtro colonna") sotto l&#39;area di anteprima.

   * Per visualizzare in anteprima un contenuto creativo specifico, seleziona la casella di controllo relativa alla riga.

   * Modifica il contenuto:

     * (Visualizza solo annunci) Per modificare il valore di una cella all’interno della tabella, fai clic all’interno della cella e modifica il valore. Fare clic all&#39;esterno della cella o premere il tasto **[!DNL Enter]** per salvare le modifiche.

     * Per contrassegnare un singolo prodotto come predefinito<!--Explain what this means. -->, tenere premuto il cursore sulla riga e fare clic su **[!UICONTROL ...]** > **[!UICONTROL Set as Default]**.

     * (Quando l&#39;annuncio include più di un&#39;offerta) Per contrassegnare più prodotti come predefiniti, selezionare le righe (fino al numero di offerte) e fare clic su **[!UICONTROL Set as Default]** nella barra degli strumenti Azioni in blocco.

     * Per eliminare un prodotto dal catalogo, posizionare il cursore sulla riga e fare clic su **[!UICONTROL ...]** > **[!UICONTROL Delete Row]**.

     * (Quando l&#39;annuncio include più di un&#39;offerta) Per eliminare più prodotti dal catalogo, selezionare le righe (fino al numero di offerte) e fare clic su **[!UICONTROL Delete Row]** nella barra degli strumenti Azioni collettive.

1. Salva i creativi:

   * Per salvare gli annunci e aggiungerli a un [bundle creativo](bundle-manage.md) nella libreria:

     1. Fare clic su **[!UICONTROL Save and Attach to Bundle]**.

     1. Fare clic su **[!UICONTROL Save]** per salvare gli annunci.

     1. Selezionare i bundle, quindi fare clic su **[!UICONTROL Attach Creative to Bundles]**.

   * Per salvare gli annunci e uscire dall&#39;installazione, fare clic su **[!UICONTROL Save]** e quindi di nuovo su **[!UICONTROL Save]**.

## Controllo qualità per una creatività dinamica (solo nuova interfaccia utente) {#qa-dynamic-creative}

Utilizza l’agente di controllo qualità nella nuova interfaccia utente per analizzare le righe del catalogo in base al modello di un creatività dinamico, visualizzare in anteprima gli annunci risultanti e identificare potenziali problemi di contenuto. È possibile filtrare e raggruppare gli annunci utilizzando **[!UICONTROL AI Assistant]**, esaminare gli avvisi del catalogo e correggere manualmente i valori del catalogo prima di pubblicare le modifiche.

>[!NOTE]
>
>È possibile verificare la qualità delle creatività dinamiche da [!UICONTROL Creative Libraries] o [!UICONTROL Creative Studio]. Per l&#39;altro punto di ingresso, vedere &quot;[Controllo qualità di un elemento creativo dinamico da Creative Studio](/help/creative/creative-studio/creative-studio-manage-dynamic-ads.md#qa-dynamic-creative)&quot;.

L’agente di controllo qualità è disponibile solo per creative display dinamiche basate su modelli dinamici, non per creative video standard o dinamiche.

### Apri l’agente di controllo qualità {#open-qa-agent}

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Apri la libreria in uno dei seguenti modi:

   * Fai clic sul nome della libreria.
   * Accanto al nome della libreria, fare clic su **[!UICONTROL ...]** > **[!UICONTROL Open]**.

1. Nella scheda **[!UICONTROL Creatives]** fare clic su **[!UICONTROL ...]** accanto al nome della creatività dinamica e quindi su **[!UICONTROL QA Agent]**.

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

* Per salvare il contenuto creativo dinamico esistente e pubblicare eventuali modifiche al catalogo:

  1. Fare clic su **[!UICONTROL Save Dynamic Creative]** nell&#39;intestazione.

  1. Nella finestra di dialogo di conferma **[!UICONTROL Update Dynamic Creative]**, fare clic su **[!UICONTROL Update]**.

     Tornate alla libreria creativa.

* Per uscire senza pubblicare le modifiche al catalogo in sospeso, fare clic su **[!UICONTROL Cancel]** nell&#39;intestazione della pagina.

>[!MORELIKETHIS]
>
>* [Impostazioni creative dinamiche](creative-settings-dynamic.md)
>* [Aggiungere elementi creativi dinamici a una libreria creativa](creative-add-dynamic.md)
>* [Visualizza il registro delle modifiche per un contenuto creativo](/help/creative/creative-libraries/creative-view-change-log.md)
>* [Flussi di lavoro per annunci dinamici](/help/creative/introduction/workflow-dynamic-ads.md)
