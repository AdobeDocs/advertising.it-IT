---
title: '[!DNL Google Ads] impostazioni campagna'
description: Fai riferimento alle impostazioni per  [!DNL Google Ads]  campagne.
exl-id: 19973286-b7c8-496e-8b87-767cda6e3542
feature: Search Campaign Management
source-git-commit: cbe18b75d49ca53460883931ecea21aa6c2d8326
workflow-type: tm+mt
source-wordcount: '2472'
ht-degree: 0%

---

# [!DNL Google Ads] impostazioni campagna

## \[Schermata Creazione campagna\]

**[!UICONTROL Campaign Type]:** (disponibile solo durante la creazione della campagna) Dove inserire annunci e quali tipi di annunci la campagna può contenere:

* *[!UICONTROL Search Network Only]:* mostra gli annunci sulla rete di ricerca, che include [!DNL Google] risultati di ricerca e, facoltativamente, siti partner di ricerca. È necessario specificare le parole chiave per ogni gruppo di annunci.

* *[!UICONTROL Search with Display Select]:* mostra gli annunci sulla rete di ricerca (che include [!DNL Google] risultati di ricerca e, facoltativamente, siti partner di ricerca) e potenzialmente gli annunci sui siti di rete di visualizzazione. Sulla rete di visualizzazione, [!DNL Google Ads] visualizza i tuoi annunci in modo selettivo utilizzando offerte automatizzate, indipendentemente dalla strategia di offerta della campagna. Per gli annunci di ricerca, specifica le parole chiave per ciascun gruppo di annunci; per gli annunci di visualizzazione, specifica i posizionamenti e facoltativamente specifica le parole chiave per ciascun gruppo di annunci.

* *[!UICONTROL Shopping Network]:* mostra gli annunci di prodotto, generati automaticamente da [!DNL Google] in base ai prodotti in [!DNL Google Merchant Center] su [!DNL Google Shopping], l&#39;area accanto ai [!DNL Google] risultati di ricerca (separati dagli annunci di testo) e (facoltativamente) i siti Web dei partner di ricerca. Per ogni gruppo di annunci della campagna, puoi specificare i gruppi di prodotti da pubblicizzare.

* *[!UICONTROL Display Network Only]:* mostra gli annunci sulla rete di visualizzazione. Per ogni gruppo di annunci, è necessario specificare i posizionamenti e, facoltativamente, le parole chiave.

* *[!UICONTROL Performance Max]:* mostra e ottimizza le conversioni per gli annunci tra canali utilizzando [!DNL Google Ads] offerte intelligenti. Nelle impostazioni della campagna devi specificare uno o più gruppi di risorse, tra cui immagini, loghi, titoli, descrizioni, video facoltativi e segnali di pubblico. [!DNL Google Ads] combina automaticamente le risorse per distribuire annunci in base al canale (ad esempio [!DNL YouTube], [!DNL Gmail] o [!DNL Search]).

  **Note:**

   * Sono disponibili solo le impostazioni richieste. Per le impostazioni facoltative, accedere all&#39;editor [!DNL Google Ads].

   * I collegamenti ai feed di prodotto [!DNL Google Merchant Center] non sono supportati.

   * Il supporto per i gruppi di voci non è disponibile. Per gestire e visualizzare i dati per l&#39;elenco dei gruppi, accedere all&#39;editor [!DNL Google Ads].

   * È supportata l’ottimizzazione ibrida. Gli obiettivi della strategia di offerta e i budget della campagna sono impostati a livello di campagna.

## [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]:** Nome di campagna univoco all&#39;interno dell&#39;account.

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

**[!UICONTROL Audience Target Method]:**(Solo campagne Gmail esistenti e di sola lettura) Indica se:

* *[!UICONTROL Target and Bid]* Per mostrare gli annunci solo agli utenti associati ai tipi di pubblico di destinazione che soddisfano anche altre destinazioni per il gruppo di annunci.

* *[!UICONTROL Bid Only]:* per mostrare annunci anche a persone non associate a tipi di pubblico di destinazione, purché soddisfino altri target a livello di gruppo di annunci. Tuttavia, puoi aumentare le possibilità che gli annunci vengano mostrati a tipi di pubblico specifici, impostando offerte più elevate per tali tipi di pubblico.

**[!UICONTROL Status]:** Lo stato di visualizzazione della campagna: *Attivo* o *In pausa*. Il valore predefinito per le nuove campagne pubblicitarie è *Attivo*.

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

**[!UICONTROL Search Partners]:** (campagne mirate solo alla rete di ricerca, incluse le campagne acquisti) Mostra
i tuoi annunci nelle reti di partner di ricerca della rete di annunci. Per impostazione predefinita, questa opzione è *[!UICONTROL Off]*.

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

**[!UICONTROL Bid strategy]:** La strategia di offerta per la campagna:

* *[!UICONTROL Enhanced CPC]:* Obsoleto. [!DNL Google Ads] ha iniziato a modificare automaticamente le [strategie di offerta CPC migliorate](https://support.google.com/google-ads/answer/2464964) esistenti in CPC manuali il 15 marzo 2025.

* *[!UICONTROL Manual CPC]* (impostazione predefinita): (non disponibile per campagne con prestazione massima) utilizza il modello CPC (cost-per-click). Facoltativamente, puoi consentire alla rete di annunci di modificare le offerte per la campagna:

   * **[!UICONTROL Enable Enhanced CPC]** (disabilitato per impostazione predefinita): equivale a utilizzare l&#39;opzione &quot;[!UICONTROL Enhanced CPC]&quot;, che è obsoleta. [!DNL Google Ads] ha iniziato a modificare automaticamente le [strategie di offerta CPC migliorate](https://support.google.com/google-ads/answer/2464964) esistenti in CPC manuali il 15 marzo 2025.

* *[!UICONTROL Maximize Clicks]:* (campagne Search, Display e Shopping) La rete di annunci, non Search, Social e Commerce, ottimizza le offerte per massimizzare i clic. Facoltativamente, immetti un **[!UICONTROL Max CPC]** (costo per clic) per garantire che la rete di annunci non paghi più di un importo specifico per ogni clic. **Attenzione:** quando aggiungi una campagna con questa strategia a un portfolio, le offerte sono guidate dal peso del clic e non dall&#39;obiettivo del portfolio.

* *[!UICONTROL Maximize Conversion Value]:* (campagne Search, Performance Max e Smart Shopping) La rete di annunci, non Search, Social e Commerce, ottimizza le offerte per massimizzare il valore di conversione. È possibile immettere un valore **[!UICONTROL Target Return on Ad Spend]** (ROAS) come percentuale. **Nota:** utilizza questa opzione per le campagne in portfolio ibridi ma non in portfolio standard. Nei portfolio ibridi, Search, Social e Commerce ottimizzano il ROAS di Target a livello di campagna o (se disponibile) di gruppo di annunci.

* *[!UICONTROL Maximize Conversions]:* (campagne Search, Display e Performance Max) La rete di annunci, non Search, Social e Commerce, ottimizza le offerte per massimizzare le conversioni. È possibile immettere un valore **[!UICONTROL Target CPA]** (costo per acquisizione). **Nota:** utilizza questa opzione per le campagne in portfolio ibridi ma non in portfolio standard. Nei portfolio ibridi, Search, Social e Commerce ottimizzano il CPA di Target a livello di campagna o (se disponibile) di gruppo di annunci.

* *[!UICONTROL Target CPA]:* (campagne di visualizzazione) La rete di annunci, non Search, Social e Commerce, ottimizza le offerte in base a un **[!UICONTROL Target CPA]** facoltativo (costo per acquisizione), che è l&#39;importo medio di 30 giorni che si desidera pagare per un&#39;acquisizione (conversione). **Nota:** utilizza questa opzione per le campagne in portfolio ibridi (ma non in portfolio standard) con qualsiasi strategia di spesa eccetto [!UICONTROL Weekly] o [!UICONTROL Google Target CPA]. Nei portfolio ibridi, Search, Social e Commerce ottimizzano il CPA di Target a livello di campagna o (se disponibile) di gruppo di annunci.

  I dati relativi alla posizione media e alle offerte CPC non sono disponibili per le campagne con questa strategia di offerta.

* *[!UICONTROL Target Impression Share]:* (campagne di ricerca) La rete di annunci, non Search, Social e Commerce, ottimizza le offerte per ottenere una quota di impression target e una posizione di annunci. Facoltativamente, immettere **[!UICONTROL Target Impression Share]** come percentuale, **[!UICONTROL Target Ad Position]** e **[!UICONTROL Max CPC]** (costo per clic). **Nota:** questa opzione non è supportata nei portfolio.

* *[!UICONTROL Target Return on Ad Spend]:* (campagne di visualizzazione e acquisto) La rete di annunci, non Search, Social e Commerce, ottimizza le offerte in base a un **[!UICONTROL Target ROAS]** specificato (ritorno sulla spesa pubblicitaria), specificato come percentuale. **Nota:** utilizza questa opzione per le campagne in portfolio ibridi (ma non in portfolio standard) con qualsiasi strategia di spesa eccetto [!UICONTROL Weekly] o [!UICONTROL Google Target ROAS]. Nei portfolio ibridi, Search, Social e Commerce ottimizzano il ROAS di Target a livello di campagna o (se disponibile) di gruppo di annunci.

  I dati relativi alla posizione media e alle offerte CPC non sono disponibili per le campagne con questa strategia di offerta.

* *[!UICONTROL Viewable CPM]:* (solo campagne [!DNL Gmail] esistenti e di sola lettura) La rete di annunci, non Search, Social e Commerce, offre offerte solo per annunci misurati come visualizzabili. **Nota:** l&#39;ottimizzazione per questa strategia non è supportata in alcun tipo di portfolio.

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]:** (solo campagne Shopping; sola lettura per campagne esistenti) Il paese in cui
i prodotti della campagna sono venduti. Poiché i prodotti sono associati ai paesi di destinazione, questa impostazione determina quali prodotti vengono pubblicizzati nella campagna.

<!-- **[!UICONTROL Campaign Priority]:** -->

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}

**[!UICONTROL Local Inventory Ads]:** (solo campagne di acquisto; inserzionisti già partecipanti al programma di acquisto locale con [!DNL Google Merchant Center] negozi negli Stati Uniti, Regno Unito, Germania, Francia, JP e AU; facoltativo) Consente a [!DNL Google Ads] di aggiungere automaticamente le informazioni di inventario locale agli annunci di acquisto su Google.com.

**Suggerimento:** Se si utilizza questa impostazione, non escludere gli annunci locali nell&#39;impostazione [!UICONTROL Inventory Filter].

**Nota:** gli annunci di inventario locali richiedono due feed aggiuntivi per [!DNL Google Merchant Center], uno con i dati di prodotto locali e l&#39;altro con l&#39;inventario di prodotti locale. Consulta la documentazione di [!DNL Google Ads] per ulteriori informazioni su [annunci per acquisti locali](https://www.google.com/retail/local-inventory-ads/).

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## [!UICONTROL Campaign Targeting]

**[!UICONTROL Languages]:** (solo reti di ricerca e visualizzazione) Una o più lingue di destinazione per gli annunci nella campagna.

[!DNL Google Ads] determina la lingua di un utente dall&#39;impostazione della lingua [!DNL Google] dell&#39;utente o dalla lingua della query di ricerca, dalla pagina corrente o dalle pagine visualizzate di recente in [!DNL Google Display Network].

**[!UICONTROL Location Targets]:** posizioni geografiche utente specifiche da includere o escludere come destinazioni. Per impostazione predefinita, tutte le posizioni sono impostate come destinazione. Puoi includere ed escludere utenti in qualsiasi combinazione di posizioni. Le esclusioni sostituiscono sempre le inclusioni.

* Per eseguire il targeting di tutte le posizioni, non selezionare alcuna posizione.

* Per eseguire il targeting o escludere posizioni specifiche:

   * (Paesi, stati, aree metropolitane o città) Fai clic su **[!UICONTROL Location Target]** (![Destinazione posizione](/help/search-social-commerce/assets/location-target.png "Destinazione posizione")) e individua le posizioni da includere ed escludere:

      * Per includere una posizione e le relative posizioni figlio, fare clic una volta sul cerchio adiacente in modo che venga visualizzato un segno di spunta blu (![Includi](/help/search-social-commerce/assets/include.png "Includi")).

      * Per escludere una posizione, fare clic due volte sul cerchio adiacente in modo che venga visualizzato un segno di spunta rosso (![Escludi](/help/search-social-commerce/assets/exclude.png "Escludi")).

      * Per espandere una posizione nei relativi sottocomponenti, ad esempio gli stati, le aree metropolitane o le città negli Stati Uniti, fare clic sul nome della posizione.

      * Per cercare una posizione, immetti o incolla almeno i primi tre caratteri della posizione nel campo di input. Nei risultati della ricerca, fare clic su **[!UICONTROL Include]** accanto a un percorso da includere o su **[!UICONTROL Exclude]** accanto a un percorso da escludere.

   * (Posizioni vicine a un indirizzo; solo destinazioni incluse) Fare clic su **[!UICONTROL Radius Target]** (![Destinazione raggio](/help/search-social-commerce/assets/radius-target.png "Destinazione raggio")) e quindi su **[!UICONTROL Address]**. Immettere l&#39;indirizzo e il raggio in miglia o chilometri intorno all&#39;indirizzo di destinazione, quindi fare clic su **[!UICONTROL Add]**.

   * (Posizioni vicine alle coordinate geografiche; solo destinazioni incluse) Fare clic su **[!UICONTROL Radius Target]** (![Destinazione raggio](/help/search-social-commerce/assets/radius-target.png "Destinazione raggio")) e quindi su **[!UICONTROL Coordinate]**. Immettere la latitudine e la longitudine e il raggio in miglia o chilometri intorno alla posizione di destinazione, quindi fare clic su **[!UICONTROL Add]**.

* Per aggiungere un adeguamento offerta per un&#39;ubicazione di destinazione inclusa, immettere un valore di adeguamento offerta:

* 0%: per non regolare le offerte per gli annunci in questa posizione.

* \[Altri valori da -90% a 300%\]: per aumentare o diminuire l&#39;offerta per gli annunci in questa posizione.

**Nota:**

* Search, Social e Commerce non forniscono regolazioni delle offerte regolate automaticamente per i seguenti target di posizione a causa di limitazioni nei dati che [!DNL Google Ads] fornisce per la mappatura delle posizioni di surfer ai target di posizione:

   * Destinazioni del raggio.

   * Alcune località al di sotto del livello di stato/provincia/regione/provincia/prefettura per le quali [!DNL Google Ads] non invia una località padre nell&#39;URL del surfista, inclusi gli aeroporti e i distretti del Congresso degli Stati Uniti.

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## [!UICONTROL Advanced Device Options]

**[!UICONTROL Mobile Carriers]:** (solo rete di visualizzazione) specifici gestori di telefonia mobile di destinazione; i gestori sono ordinati
per paese. Se non ne selezioni alcuna, viene eseguito il targeting di tutti.

**[!UICONTROL Mobile Carriers]:** (solo rete di visualizzazione) Sistemi operativi specifici per la destinazione. Se non ne selezioni alcuna, viene eseguito il targeting di tutti.

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

<!-- **[!UICONTROL Custom Parameters]:** -->

{{$include /help/_includes/custom-parameters.md}}

<!-- **[!UICONTROL Landing Page Suffix]:** -->

{{$include /help/_includes/landing-page-suffix.md}}

## [!UICONTROL DSA Options]

<!-- **[!UICONTROL Website Domain]:** -->

{{$include /help/_includes/website-domain.md}}

<!-- **[!UICONTROL DSA Language]:** -->

{{$include /help/_includes/dsa-language.md}}

## [!UICONTROL Customer Acquisition Goals]

**[!UICONTROL Customer Acquisition]:** (solo campagne di ricerca e con prestazioni massime) Come allocare le offerte per i nuovi clienti e i clienti esistenti:

* *[!UICONTROL Bid equally for new and existing customers]*

* *[!UICONTROL Bid higher for new customers than for existing customers]*

  **Nota:** Per utilizzare questa impostazione, è necessario innanzitutto attivare il nuovo obiettivo di acquisizione cliente per l&#39;account [!DNL Google Ads] o, se applicabile, per l&#39;account manager. L’obiettivo definisce gli elenchi dei clienti esistenti idonei e il valore di conversione aggiuntivo per i nuovi clienti nelle impostazioni di conversione. Consulta i passaggi 1-2 nella guida di [!DNL Google Ads] &quot;[Attiva il nuovo obiettivo di acquisizione clienti](https://support.google.com/google-ads/answer/14007601).&quot;

* *[!UICONTROL Only bid for new customers]*

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-google.md}}

## [!UICONTROL Negative Websites]

<!-- **[!UICONTROL Negative Websites]:** -->

{{$include /help/_includes/negative-websites-google.md}}

## [!UICONTROL Campaign Tracking]

<!-- **[!UICONTROL Override Account Tracking]:** -->

{{$include /help/_includes/override-account-tracking.md}}

<!-- **[!UICONTROL Tracking Type]:** -->

{{$include /help/_includes/tracking-type.md}}

<!-- **[!UICONTROL Redirect Type]:** -->

{{$include /help/_includes/redirect-type.md}}

<!-- **[!UICONTROL Auto Upload]:** -->

{{$include /help/_includes/auto-upload.md}}

<!-- **[!UICONTROL Encode Base URL]:** -->

{{$include /help/_includes/encode-base-url.md}}

<!-- **[!UICONTROL Tracking Level]:** -->

{{$include /help/_includes/tracking-level.md}}

**[!UICONTROL Track Product Group]:** (solo per [!UICONTROL EF Redirect]) Non implementato

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

## [!UICONTROL Asset Groups] (per gruppo di risorse)

**[!UICONTROL Asset Group Name]:** Il nome del gruppo di risorse. I collegamenti ai feed di prodotto [!DNL Google Merchant Center] non sono supportati.

**[!UICONTROL Asset Group Status]:** Lo stato del gruppo di risorse: *[!UICONTROL Active]* o *[!UICONTROL Paused]*.

**[!UICONTROL Final URL]:** URL finale per tutti gli annunci creati dal gruppo di risorse. <!-- For campaigns created within Search, Social, & Commerce, final URL expansion is automatically enabled for the campaign, and Google Ads replaces this value with a more relevant landing page based on the user's search query and intent, and also customizes the headline based on the landing page content. You can disable final URL expansion, or exclude specific URLs from expansion, from within the [!DNL Google Ads] editor. -->

**[!UICONTROL Images]:** Fino a 15 immagini per l&#39;annuncio, incluse le seguenti dimensioni: 1) almeno tre immagini quadrate, 2) almeno tre immagini orizzontali e 3) almeno un&#39;immagine verticale. Consulta le [[!DNL Google Ads] specifiche immagine](https://support.google.com/google-ads/answer/10724492?hl=en&amp;ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications). È possibile caricare immagini o selezionarle da [!UICONTROL Asset Library], ma non entrambe nella stessa operazione.

* Per caricare le immagini:

   1. Nella scheda [!UICONTROL Upload from Device], fare clic su **[!UICONTROL +]** e selezionare le immagini dal dispositivo o dalla rete.

   1. Per ogni immagine:

      1. Seleziona le proporzioni.

      1. Trascinate e posizionate la casella di ritaglio in base alle necessità per selezionare la parte visualizzabile dell&#39;immagine e, se possibile, ridimensionate la parte visualizzabile.

      1. (Facoltativo) Selezionate altre proporzioni e, se necessario, riposizionate e ridimensionate l&#39;immagine per ogni proporzione selezionata.

         Viene creata una risorsa per ogni proporzione selezionata.

      1. Fare clic su **[!UICONTROL Proceed]**.

   1. Dopo aver specificato le immagini, fare clic su **[!UICONTROL Upload]**.

* Per selezionare le immagini da [!UICONTROL Asset Library], fare clic su **[!UICONTROL Asset Library]** e selezionare le immagini.

**[!UICONTROL Logos]:** almeno un logo quadrato (1:1) e un logo orizzontale (4:1). Puoi includere fino a cinque di ogni dimensione. Consulta le [[!DNL Google Ads] specifiche del logo](https://support.google.com/google-ads/answer/10724492?hl=en&amp;ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications). È possibile caricare immagini o selezionarle da [!UICONTROL Asset Library], ma non entrambe nella stessa operazione.

* Per caricare le immagini:

   1. Nella scheda [!UICONTROL Upload from Device], fare clic su **[!UICONTROL +]** e selezionare le immagini dal dispositivo o dalla rete.

   1. Per ogni immagine:

      1. Seleziona le proporzioni.

      1. Trascinate e posizionate la casella di ritaglio in base alle necessità per selezionare la parte visualizzabile dell&#39;immagine e, se possibile, ridimensionate la parte visualizzabile.

      1. (Facoltativo) Selezionate altre proporzioni e, se necessario, riposizionate e ridimensionate l&#39;immagine per ogni proporzione selezionata.

         Viene creata una risorsa per ogni proporzione selezionata.

      1. Fare clic su **[!UICONTROL Proceed]**.

   1. Dopo aver specificato le immagini, fare clic su **[!UICONTROL Upload]**.

* Per selezionare le immagini da [!UICONTROL Asset Library], fare clic su **[!UICONTROL Asset Library]** e selezionare le immagini.

**[!UICONTROL Videos]:** (facoltativo) almeno uno e fino a cinque video [!DNL YouTube] di durata minima di 10 secondi. È possibile immettere gli URL o selezionarli da [!UICONTROL Asset Library], ma non entrambi nella stessa operazione.

* Per immettere gli URL:

   1. Nella scheda [!UICONTROL Enter Video Url] immettere un URL.

   1. (Facoltativo) Per aggiungere un altro URL, fare clic su **[!UICONTROL + Add]** e immettere l&#39;URL.

* Per selezionare i video da [!UICONTROL Asset Library], fare clic su **[!UICONTROL Asset Library]** e selezionare i video.

**[!UICONTROL Headlines]:** Almeno tre e fino a cinque titoli brevi con un massimo di 30 caratteri ciascuno. Almeno un titolo deve contenere al massimo 15 caratteri. Se l&#39;opzione a livello di campagna per abilitare l&#39;espansione dell&#39;URL finale è impostata in [!DNL Google Ads], [!DNL Google Ads] sostituisce questo valore con un titolo personalizzato in base al contenuto della pagina di destinazione.

È possibile immettere testo o selezionare risorse da [!UICONTROL Asset Library], ma non entrambi nella stessa operazione.

* Per immettere il testo:

   1. Nella scheda [!UICONTROL Enter Text] immettere il testo.

   1. (Facoltativo) Per aggiungere un&#39;altra stringa di testo, fare clic su **[!UICONTROL + Add]** e immettere la stringa.

* Per selezionare le risorse da [!UICONTROL Asset Library], fai clic su **[!UICONTROL Asset Library]** e seleziona le risorse.

**[!UICONTROL Long Headlines]:** Almeno uno e fino a cinque titoli lunghi con un massimo di 90 caratteri ciascuno. È possibile immettere testo o selezionare risorse da [!UICONTROL Asset Library], ma non entrambi nella stessa operazione.

* Per immettere il testo:

   1. Nella scheda [!UICONTROL Enter Text] immettere il testo.

   1. (Facoltativo) Per aggiungere un&#39;altra stringa di testo, fare clic su **[!UICONTROL + Add]** e immettere la stringa.

* Per selezionare le risorse da [!UICONTROL Asset Library], fai clic su **[!UICONTROL Asset Library]** e seleziona le risorse.

**[!UICONTROL Descriptions]:** almeno due descrizioni e fino a quattro descrizioni con un massimo di 90 caratteri ciascuna. Almeno una descrizione deve contenere al massimo 30 caratteri. È possibile immettere testo o selezionare risorse da [!UICONTROL Asset Library], ma non entrambi nella stessa operazione.

* Per immettere il testo:

   1. Nella scheda [!UICONTROL Enter Text] immettere il testo.

   1. (Facoltativo) Per aggiungere un&#39;altra stringa di testo, fare clic su **[!UICONTROL + Add]** e immettere la stringa.

* Per selezionare le risorse da [!UICONTROL Asset Library], fai clic su **[!UICONTROL Asset Library]** e seleziona le risorse.

**[!UICONTROL Call to Action]:** il call to action da includere nell&#39;annuncio. Per impostazione predefinita, *[!UICONTROL Automated]* è selezionato e [!DNL Google Ads] seleziona il call to action. Facoltativamente, puoi scegliere un’azione diversa.

**[!UICONTROL Business Name]:** Nome aziendale, con un massimo di 25 caratteri.

**[!UICONTROL Audience Signal]:** (facoltativo) [!DNL Google Ads] tipi di pubblico da utilizzare come segnali di pubblico per la campagna. I modelli di apprendimento automatico di [!DNL Google Ads] utilizzano i tipi di pubblico per trovare surfisti web simili a target e possono anche mostrare annunci a tipi di pubblico non specificati come segnali per aiutarti a raggiungere gli obiettivi prestazionali. Scegli i tipi di pubblico che hanno più probabilità di essere convertiti.

>[!NOTE]
>I segnali di pubblico sono diversi dai [target di pubblico a livello di campagna e di gruppo di annunci](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md).

**[!UICONTROL Primary Status]:** (campo di sola lettura per i gruppi di risorse esistenti nelle campagne con prestazione massima) Perché il gruppo di risorse è o non è a piena capacità. Tiene conto dello stato del gruppo di attività nonché di altri segnali, come le approvazioni di politiche e di qualità. I valori possono includere *IDONEI,* *LIMITATI,* *NON_IDONEI,* *IN PAUSA,* *IN SOSPESO,* *RIMOSSI,* *SCONOSCIUTI,* o *NON SPECIFICATI.*<!-- GGL also has a Primary Status field for campaigns; if we ever sync that, then we'll need to distinguish between them. -->

**[!UICONTROL Primary Status Reason]:** (campo di sola lettura per i gruppi di risorse esistenti nelle campagne con prestazione massima) Dettagli aggiuntivi sullo stato principale del gruppo di risorse. I valori possono includere *ASSET_GROUP_DISAPPROVED,* *ASSET_GROUP_LIMITED,* *ASSET_GROUP_PAUSED,* *ASSET_GROUP_REMOVED,* *ASSET_GROUP_UNDER_REVIEW,* *CAMPAIGN_ENDED,* *CAMPAIGN_PAUSED,* *CAMPAIGN_PENDING,* *CAMPAIGN_REMOVED,* *UNKNOWN,* o *NON SPECIFICATO.*

## [!UICONTROL Conversion Goals]

**[!UICONTROL Conversion Goal]:** Se *[!UICONTROL Use account conversion goals for this campaign]* (impostazione predefinita) o *[!UICONTROL Use campaign specific conversion goals]*. Se scegli di specificare gli obiettivi di conversione per la campagna, seleziona gli obiettivi standard e/o crea un obiettivo personalizzato per la campagna.

Gli obiettivi vengono sincronizzati ogni giorno, pertanto gli obiettivi esistenti creati nelle 24 ore precedenti potrebbero non essere elencati. Per aggiornare l&#39;elenco, [sincronizzare manualmente i dati della rete di annunci](/help/search-social-commerce/campaign-management/campaigns/sync-network.md).

Per creare un obiettivo di conversione personalizzato, fare clic su **[!UICONTROL + Add custom goal]**, immettere il nome dell&#39;obiettivo personalizzato, selezionare le [azioni di conversione](https://support.google.com/google-ads/answer/6032150) da includere nell&#39;obiettivo personalizzato, quindi fare clic su **[!UICONTROL Save]**. **Nota:** ogni campagna può avere un solo obiettivo personalizzato.

>[!TIP]
>
>Se la campagna fa parte di un portfolio ibrido, la best practice consiste nell’utilizzare obiettivi a livello di campagna che corrispondono agli obiettivi di conversione nell’obiettivo del portfolio; l’inclusione di obiettivi di conversione aggiuntivi può influire sulle prestazioni del portfolio.
>
>Tuttavia, per le campagne in portfolio ibridi per le quali [carichi gli obiettivi nella rete di annunci](/help/search-social-commerce/tools/objective-upload-to-networks.md), effettua le seguenti operazioni nell&#39;editor della rete di annunci invece che qui: a) aggiungi la metrica di obiettivo del portfolio Search, Social e Commerce caricata (che inizia con &quot;O_ACS_OBJ&quot;) come azione di conversione per la campagna; e b) aggiungi eventuali obiettivi della campagna che includono [!DNL Google] conversioni tracciate, perché le metriche tracciate nella rete di annunci non vengono caricate nella rete di annunci con l&#39;obiettivo.

>[!MORELIKETHIS]
>
>* [Gestisci campagne](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
