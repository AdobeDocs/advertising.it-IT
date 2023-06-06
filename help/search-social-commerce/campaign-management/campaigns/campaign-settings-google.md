---
title: "[!DNL Google Ads] impostazioni della campagna"
description: Fai riferimento alle impostazioni per [!DNL Google Ads] campagne.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '1958'
ht-degree: 0%

---

# [!DNL Google Ads] impostazioni della campagna

## \[Schermata Creazione campagna\]

**[!UICONTROL Campaign Type]:** (Disponibile solo durante la creazione della campagna) Dove inserire annunci e quali tipi di annunci la campagna può contenere:

* *[!UICONTROL Search Network Only]:* Mostra gli annunci sulla rete di ricerca, che include [!DNL Google] risultati della ricerca e, facoltativamente, siti partner di ricerca. È necessario specificare le parole chiave per ogni gruppo di annunci.

* *[!UICONTROL Search with Display Select]:* Mostra gli annunci sulla rete di ricerca (che include [!DNL Google] risultati della ricerca e, facoltativamente, siti partner di ricerca) e mostra potenzialmente annunci su siti di rete visualizzati. Sulla rete del display, [!DNL Google Ads] mostra i tuoi annunci in modo selettivo mediante offerte automatizzate, indipendentemente dalla strategia di offerta della campagna. Per gli annunci di ricerca, devi specificare le parole chiave per ciascun gruppo di annunci; per gli annunci di visualizzazione, devi specificare i posizionamenti e, facoltativamente, puoi specificare le parole chiave per ciascun gruppo di annunci.

* *[!UICONTROL Shopping Network]:* Mostra annunci di prodotti, che [!DNL Google] genera automaticamente in base ai prodotti in [!DNL Google Merchant Center] il [!DNL Google Shopping], l&#39;area accanto a [!DNL Google] risultati della ricerca (separati dagli annunci di testo) e (facoltativamente) siti web dei partner di ricerca. Per ogni gruppo di annunci della campagna, puoi specificare i gruppi di prodotti da pubblicizzare.

* *[!UICONTROL Display Network Only]:* Mostra gli annunci sulla rete di visualizzazione. Per ogni gruppo di annunci, devi specificare i posizionamenti e, facoltativamente, puoi specificare le parole chiave.

* *[!UICONTROL Performance Max]:* (Funzione beta) Mostra e ottimizza le conversioni per gli annunci tra canali utilizzando [!DNL Google Ads] offerte intelligenti. Nelle impostazioni della campagna devi specificare uno o più gruppi di risorse, tra cui immagini, loghi, titoli, descrizioni, video facoltativi e segnali di pubblico. [!DNL Google Ads] combina automaticamente le risorse per distribuire gli annunci in base al canale (ad esempio [!DNL YouTube], [!DNL Gmail], o [!DNL Search]).

   **Note:**

   * Sono disponibili solo le impostazioni richieste. Per le impostazioni facoltative, accedi a [!DNL Google Ads] editor.

   * Collegamenti a [!DNL Google Merchant Center] i feed di prodotto non sono supportati.

   * Il supporto per i gruppi di voci non è disponibile. Per gestire e visualizzare i dati per l’elenco dei gruppi, accedi a [!DNL Google Ads] editor.

   * È supportata l’ottimizzazione ibrida. Gli obiettivi della strategia di offerta e i budget della campagna sono impostati a livello di campagna.

## [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]:** Un nome di campagna univoco all’interno dell’account.

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

**[!UICONTROL Audience Target Method]:**(Solo campagne Gmail esistenti e di sola lettura) Indica se:

* *[!UICONTROL Target and Bid]* Per mostrare gli annunci solo agli utenti associati ai tipi di pubblico target che soddisfano anche altri target per il gruppo di annunci.

* *[!UICONTROL Bid Only]:*  Mostrare annunci anche a persone non associate a tipi di pubblico di destinazione, purché soddisfino altri target a livello di gruppo di annunci. Tuttavia, puoi aumentare le possibilità che gli annunci vengano mostrati a tipi di pubblico specifici, impostando offerte più elevate per tali tipi di pubblico.

**[!UICONTROL Status]:** Lo stato di visualizzazione della campagna: *Attivo* o *In pausa*. L’impostazione predefinita per le nuove campagne pubblicitarie è *Attivo*.

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

**[!UICONTROL Search Partners]:** (Campagne mirate solo alla rete di ricerca, incluse le campagne di acquisto) Mostra gli annunci nelle reti di partner di ricerca della rete di annunci. Per impostazione predefinita, questa opzione è *[!UICONTROL Off]*.

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

**[!UICONTROL Bid strategy]:** La strategia di offerta per la campagna:

* *[!UICONTROL Enhanced CPC]:* (Non disponibile per prestazioni massime o esistenti, sola lettura) [!DNL Gmail] campagne pubblicitarie) Utilizza il modello avanzato di cost-per-click (eCPC) della rete di annunci, che consente alla rete di modificare automaticamente l’offerta cost-per-click (CPC) per ogni asta nel tentativo di massimizzare le conversioni, utilizzando le conversioni specificate all’interno della rete di annunci (non in Search, Social &amp; Commerce), cercando al contempo di mantenere il CPC medio al di sotto del CPC massimo.

Quando aggiungi una campagna con eCPC a un portfolio Search, Social e Commerce ottimizzato, Search, Social e Commerce ottimizzano le offerte di base e, quando &quot;[!UICONTROL Auto adjust campaign budget limits]&quot;è abilitata l’opzione&quot;: il budget della campagna. La rete di annunci ottimizza tutte le regolazioni delle offerte e può modificare le offerte generate da Search, Social e Commerce al momento della query utente in base a dati e informazioni proprietari. **Attenzione:** Utilizza le campagne eCPC nei portfolio solo quando il totale delle conversioni tracciate nella rete di annunci è in linea con l’obiettivo del portfolio. <!-- Note to self: Within the ad network UI, you specify conversion goals either a) all conversion actions you've set to be included in "Conversions" at the account level or b) one or more individual conversions to use for optimization -->

* *[!UICONTROL Manual CPC]* (impostazione predefinita): (non disponibile per campagne con prestazione massima) utilizza il modello CPC (cost-per-click). Facoltativamente, puoi consentire alla rete di annunci di modificare le offerte per la campagna:

   * **[!UICONTROL Enable Enhanced CPC]** (disattivato per impostazione predefinita): corrisponde all’utilizzo del tasto &quot;[!UICONTROL Enhanced CPC]&quot;.

* *[!UICONTROL Maximize Clicks]:* (Campagne di ricerca, visualizzazione e acquisto) La rete di annunci, anziché Search, Social e Commerce, ottimizza le offerte per massimizzare i clic. È possibile inserire un **[!UICONTROL Max CPC]** (costo per clic) per garantire che la rete di annunci non paghi più di un importo specifico per ogni clic. **Attenzione:** Quando aggiungi una campagna con questa strategia a un portfolio, le offerte si basano sul peso del clic e non sull’obiettivo del portfolio.

* *[!UICONTROL Maximize Conversion Value]:* (Campagne Search, Performance Max e Smart Shopping) La rete di annunci, non Search, Social e Commerce, ottimizza le offerte per massimizzare il valore di conversione. È possibile inserire un **[!UICONTROL Target Return on Ad Spend]** (ROAS) in percentuale. **Nota:** Utilizza questa opzione per le campagne in portfolio ibridi ma non in portfolio standard.

* *[!UICONTROL Maximize Conversions]:* (Campagne basate su ricerca, visualizzazione e prestazioni massime) La rete di annunci, anziché Search, Social e Commerce, ottimizza le offerte per massimizzare le conversioni. È possibile inserire un **[!UICONTROL Target CPA]** (costo per acquisizione). **Nota:** Utilizza questa opzione per le campagne in portfolio ibridi ma non in portfolio standard.

* *[!UICONTROL Target CPA]:* (Campagne di visualizzazione; campagne di ricerca esistenti) La rete di annunci, non Search, Social &amp; Commerce, ottimizza le offerte in base a un **[!UICONTROL Target CPA]** (costo per acquisizione), che è l’importo medio di 30 giorni che desideri pagare per un’acquisizione (conversione). **Nota:** Utilizza questa opzione per le campagne in portfolio ibridi (ma non in portfolio standard) con qualsiasi strategia di spesa a eccezione [!UICONTROL Weekly] o [!UICONTROL Google Target CPA].

   I dati relativi alla posizione media e alle offerte CPC non sono disponibili per le campagne con questa strategia di offerta.

   Per nuove campagne di ricerca, [!DNL Google Ads] ha sostituito questa strategia di offerta con il [!UICONTROL Maximize Conversions] strategia che utilizza un [!UICONTROL Target CPA] valore. Per le campagne di ricerca esistenti con questa strategia, puoi modificare solo il valore target, e così facendo cambia la strategia in [!UICONTROL Maximize Conversions] strategia che utilizza il valore specificato [!UICONTROL Target CPA] valore.

* *[!UICONTROL Target Impression Share]:* (Campagne di ricerca) La rete di annunci, non Search, Social e Commerce, ottimizza le offerte per raggiungere una quota di impression target e una posizione pubblicitaria. È possibile inserire un **[!UICONTROL Target Impression Share]** in percentuale, il valore **[!UICONTROL Target Ad Position]**, e un **[!UICONTROL Max CPC]** (costo per clic). **Nota:** Questa opzione non è supportata nei portfolio.

* *[!UICONTROL Target Return on Ad Spend]:*  (Campagne di visualizzazione e di acquisto; campagne di ricerca esistenti) La rete di annunci, non Search, Social e Commerce, ottimizza le offerte in base a un dato **[!UICONTROL Target ROAS]** (ritorno sulla spesa pubblicitaria), specificato come percentuale. **Nota:** Utilizza questa opzione per le campagne in portfolio ibridi (ma non in portfolio standard) con qualsiasi strategia di spesa a eccezione [!UICONTROL Weekly] o [!UICONTROL Google Target ROAS].

   I dati relativi alla posizione media e alle offerte CPC non sono disponibili per le campagne con questa strategia di offerta.

   Per nuove campagne di ricerca, [!DNL Google Ads] ha sostituito questa strategia di offerta con il [!UICONTROL Maximize Conversion Value] strategia che utilizza un [!UICONTROL Target Return on Ad Spend value]. Per le campagne di ricerca esistenti con questa strategia, puoi modificare solo il valore target, e così facendo cambia la strategia in [!UICONTROL Maximize Conversion Value] strategia che utilizza il valore specificato [!UICONTROL Target Return on Ad Spend] valore.

* *[!UICONTROL Viewable CPM]:* (Esistente, sola lettura [!DNL Gmail] solo campagne pubblicitarie) La rete di annunci pubblicitari, non Search, Social &amp; Commerce (Ricerca, Social &amp; Commerce), fa offerte solo sugli annunci misurati come visualizzabili. **Nota:** L&#39;ottimizzazione per questa strategia non è supportata in alcun tipo di portfolio.

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]:** (Solo campagne commerciali; sola lettura per le campagne esistenti) Il paese in cui vengono venduti i prodotti della campagna. Poiché i prodotti sono associati ai paesi di destinazione, questa impostazione determina quali prodotti vengono pubblicizzati nella campagna.

<!-- **[!UICONTROL Campaign Priority]:** -->

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}

**[!UICONTROL Local Inventory Ads]:** (Solo campagne di acquisto; inserzionisti che già partecipano al programma di acquisto locale con [!DNL Google Merchant Center] negli Stati Uniti, nel Regno Unito, in Germania, in Francia, in Giappone e all&#39;estero (facoltativo) consente [!DNL Google Ads] per aggiungere automaticamente le informazioni sull’inventario locale agli annunci di acquisto su Google.com.

**Suggerimento** Se utilizzi questa impostazione, non escludere gli annunci locali nel [!UICONTROL Inventory Filter] impostazione.

**Nota:** Gli annunci di inventario locali richiedono due feed aggiuntivi per [!DNL Google Merchant Center] — uno con i dati dei prodotti locali e l&#39;altro con l&#39;inventario dei prodotti locali. Consulta la [!DNL Google Ads] per ulteriori informazioni su [annunci per acquisti locali](https://www.google.com/retail/local-inventory-ads/).

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## [!UICONTROL Campaign Targeting]

**[!UICONTROL Languages]:** (Solo reti di ricerca e visualizzazione) Una o più lingue di destinazione per gli annunci nella campagna.

[!DNL Google Ads] determina la lingua di un utente dal [!DNL Google] impostazioni della lingua o lingua della query di ricerca, della pagina corrente o delle pagine visualizzate di recente nella [!DNL Google Display Network].

**[!UICONTROL Location Targets]:** Posizioni geografiche specifiche dell’utente da includere o escludere come target. Per impostazione predefinita, tutte le posizioni sono impostate come destinazione. Puoi includere ed escludere utenti in qualsiasi combinazione di posizioni. Le esclusioni sostituiscono sempre le inclusioni.

* Per eseguire il targeting di tutte le posizioni, non selezionare alcuna posizione.

* Per eseguire il targeting o escludere posizioni specifiche:

   * (Paesi, stati, aree metropolitane o città) Fai clic su **[!UICONTROL Location Target]** (![Destinazione posizione](/help/search-social-commerce/assets/location-target.png "Destinazione posizione")) e individuare le posizioni da includere ed escludere:

      * Per includere una posizione e le relative posizioni figlio, fare clic sul cerchio accanto a essa una volta in modo che un segno di spunta blu (![Includi](/help/search-social-commerce/assets/include.png "Includi")).

      * Per escludere una posizione, fare clic due volte sul cerchio accanto ad essa in modo che un segno di spunta rosso (![Escludi](/help/search-social-commerce/assets/exclude.png "Escludi")).

      * Per espandere una posizione nei relativi sottocomponenti, ad esempio gli stati, le aree metropolitane o le città negli Stati Uniti, fare clic sul nome della posizione.

      * Per cercare una posizione, immetti o incolla almeno i primi tre caratteri della posizione nel campo di input. Nei risultati della ricerca, fai clic su **[!UICONTROL Include]** accanto a una posizione da includere o **[!UICONTROL Exclude]** accanto a una posizione da escludere.
   * (Posizioni vicino a un indirizzo; solo destinazioni incluse) Fai clic su **[!UICONTROL Radius Target]** (![Destinazione raggio](/help/search-social-commerce/assets/radius-target.png "Destinazione raggio")), quindi fare clic su **[!UICONTROL Address]**. Immettere l&#39;indirizzo e il raggio in miglia o chilometri intorno all&#39;indirizzo desiderato, quindi fare clic su **[!UICONTROL Add]**.

   * (Posizioni vicine alle coordinate geografiche; solo destinazioni incluse) Fai clic su **[!UICONTROL Radius Target]** (![Destinazione raggio](/help/search-social-commerce/assets/radius-target.png "Destinazione raggio")), quindi fare clic su **[!UICONTROL Coordinate]**. Immettere la latitudine e la longitudine e il raggio in miglia o chilometri intorno alla posizione di destinazione, quindi fare clic su **[!UICONTROL Add]**.

   * (Posizioni vicino al tuo [!DNL My Business] posizioni disponibili come estensioni di posizione; solo destinazioni incluse) Fare clic su **[!UICONTROL Location Group Target]** (![Gruppo di posizioni](/help/search-social-commerce/assets/location-group.png "Gruppo di posizioni")); è possibile inserire un paese, uno stato, un&#39;area metropolitana o una città per visualizzare l&#39;elenco delle posizioni disponibili e quindi selezionare una o più posizioni dall&#39;elenco di [!DNL Google My Business] posizioni. Specifica il raggio in miglia o chilometri intorno alle posizioni di destinazione, quindi fai clic su **[!UICONTROL Add]**.


* Per aggiungere un adeguamento offerta per un&#39;ubicazione di destinazione inclusa, immettere un valore di adeguamento offerta:

* 0%: per non regolare le offerte per gli annunci in questa posizione.

* \[Altri valori da -90% a 300%\]: per aumentare o diminuire l&#39;offerta per gli annunci in questa posizione.

**Nota:**

* Search, Social e Commerce non forniscono regolazioni delle offerte regolate automaticamente per i seguenti target di posizione a causa di limitazioni nei dati che [!DNL Google Ads] fornisce la mappatura delle ubicazioni di surfer agli obiettivi di ubicazione:

   * Destinazioni del raggio.

   * Alcune località al di sotto del livello di stato/provincia/regione/contea/prefettura per le quali [!DNL Google Ads] non invia una posizione padre nell&#39;URL del surfista, inclusi gli aeroporti e i distretti del Congresso degli Stati Uniti.

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## [!UICONTROL Advanced Device Options]

**[!UICONTROL Mobile Carriers]:** (Visualizza solo rete) Specifici gestori di telefonia mobile da indirizzare; i gestori sono ordinati per paese. Se non ne selezioni alcuna, viene eseguito il targeting di tutti.

**[!UICONTROL Mobile Carriers]:** (Visualizza solo rete) Sistemi operativi specifici per il targeting. Se non ne selezioni alcuna, viene eseguito il targeting di tutti.

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

**[!UICONTROL Track Product Group]:** (Per [!UICONTROL EF Redirect] solo) Non implementato

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

## [!UICONTROL Asset Groups] (per gruppo di risorse)

**[!UICONTROL Asset Group Name]:** Nome del gruppo di risorse. Collegamenti a [!DNL Google Merchant Center] i feed di prodotto non sono supportati.

**[!UICONTROL Asset Group Status]:** Stato del gruppo di risorse: *[!UICONTROL Active]* o *[!UICONTROL Paused]*.

**[!UICONTROL Final URL]:** L’URL finale per tutti gli annunci creati dal gruppo di risorse. <!-- For campaigns created within Search, Social, & Commerce, final URL expansion is automatically enabled for the campaign, and Google Ads replaces this value with a more relevant landing page based on the user's search query and intent, and also customizes the headline based on the landing page content. You can disable final URL expansion, or exclude specific URLs from expansion, from within the [!DNL Google Ads] editor. -->

**[!UICONTROL Images]:** Fino a quindici immagini per l’annuncio, incluse le seguenti dimensioni: 1) almeno tre immagini quadrate, 2) almeno tre immagini panoramiche e 3) almeno un’immagine verticale. Consulta la [[!DNL Google Ads] specifiche dell&#39;immagine](https://support.google.com/google-ads/answer/10724492?hl=en&amp;ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications). Per caricare le immagini:

1. Per ogni immagine:

   1. Clic **[!UICONTROL +]** e selezionare un&#39;immagine dal dispositivo o dalla rete.

   1. Seleziona le proporzioni.

   1. Trascina e posiziona la casella di ritaglio in base alle esigenze per selezionare la parte visualizzabile dell’immagine, quindi fai clic su **[!UICONTROL Proceed]**.

1. Al termine della specifica delle immagini, fare clic su **[!UICONTROL Upload]**.

**[!UICONTROL Logos]:** Almeno un logo quadrato (1:1) e un logo orizzontale (4:1). Puoi includere fino a cinque di ogni dimensione. Consulta la [[!DNL Google Ads] specifiche del logo](https://support.google.com/google-ads/answer/10724492?hl=en&amp;ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications). Per caricare le immagini:

1. Per ogni immagine:

   1. Clic **[!UICONTROL +]** e selezionare un&#39;immagine dal dispositivo o dalla rete.

   1. Trascina e posiziona la casella di ritaglio in base alle esigenze per selezionare la parte visualizzabile dell’immagine, quindi fai clic su **[!UICONTROL Proceed]**.

1. Al termine della specifica delle immagini, fare clic su **[!UICONTROL Upload]**.

**[!UICONTROL Videos]:** (Facoltativo) L’URL per almeno uno e fino a cinque, [!DNL YouTube] video di durata superiore a 10 secondi.

**[!UICONTROL Headlines]:** Almeno tre e fino a cinque titoli brevi con un massimo di 30 caratteri ciascuno. Almeno un titolo deve contenere al massimo 15 caratteri. Se l’opzione a livello di campagna per abilitare l’espansione finale dell’URL è impostata in [!DNL Google Ads], quindi [!DNL Google Ads] sostituisce questo valore con un titolo personalizzato in base al contenuto della pagina di destinazione.

**[!UICONTROL Long Headlines]:** Almeno uno e fino a cinque titoli lunghi con un massimo di 90 caratteri ciascuno.

**[!UICONTROL Descriptions]:** Almeno due descrizioni e fino a quattro descrizioni con un massimo di 90 caratteri ciascuna. Almeno una descrizione deve contenere al massimo 30 caratteri.

**[!UICONTROL Call to Action]:** Invito all’azione da includere nell’annuncio. Per impostazione predefinita, *[!UICONTROL Automated]* è selezionato, e [!DNL Google Ads] seleziona l&#39;invito all&#39;azione. Facoltativamente, puoi scegliere un’azione diversa.

**[!UICONTROL Business Name]:** La ragione sociale, con un massimo di 25 caratteri.

**[!UICONTROL Add new asset group]:** Consente di specificare un gruppo di risorse aggiuntivo.

>[!MORELIKETHIS]
>
>* [Gestire le campagne](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
