---
title: '''[!DNL Microsoft Advertising] impostazioni della campagna'
description: Fai riferimento alle impostazioni per [!DNL Microsoft Advertising] campagne.
exl-id: f11cb61e-d627-4074-870d-e186f3e65572
feature: Search Campaign Management
source-git-commit: 0f128b569f8c005c4f72a0c85ebf59e9fed53320
workflow-type: tm+mt
source-wordcount: '1963'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] impostazioni della campagna

## \[Schermata Creazione campagna\]

**[!UICONTROL Campaign Type]:** (Disponibile solo durante la creazione della campagna) Dove inserire annunci e quali tipi di annunci la campagna può contenere:

* *[!UICONTROL Search]:* Mostra gli annunci di testo nella rete di ricerca.

* *[!UICONTROL Shopping Network]:* Mostra gli annunci di prodotto: per i prodotti nel tuo [!DNL Microsoft Merchant Center] catalogo dei prodotti — sulla rete commerciale.

* *[!UICONTROL Audience]:* Mostra gli annunci nativi/display sul [!DNL Microsoft Audience Network]. Puoi: a) generare automaticamente annunci basati su feed collegando la campagna a un negozio di centri commerciali nel [!UICONTROL Shopping Settings] sezione o b) creare annunci reattivi con risorse di testo e immagini caricate. Entrambe le opzioni richiedono la creazione di gruppi di annunci con targeting utente.

* *[!UICONTROL Shopping Campaigns for Brands]:* (Funzione beta) Promuove i prodotti attraverso rivenditori collegati attraverso le reti di ricerca e pubblico. Puoi creare gruppi di annunci e gruppi di prodotti secondari (app da promuovere) e annunci di prodotti facoltativi per la campagna; [!DNL Microsoft Advertising] crea automaticamente annunci per i gruppi di prodotti. Per le campagne di acquisto dei marchi, utilizza la strategia di offerta [!UICONTROL Manual CPC]; per le promozioni commerciali per i marchi, utilizza la strategia di offerta [!UICONTROL Cost per Sale].

* *[!UICONTROL Microsoft Store Ads Campaign]:* (Funzione beta) Promuove le app e i giochi disponibili nel [!DNL Microsoft Store]. Puoi creare gruppi di annunci secondari, gruppi di prodotti e annunci di prodotti facoltativi per la campagna; [!DNL Microsoft Advertising] crea automaticamente annunci per i gruppi di prodotti.

* *[!UICONTROL Audience CTV Video]:* (Funzione beta) Mostra gli annunci video TV connessi (CTV) sulla rete del pubblico.

* *[!UICONTROL Audience Video]:* (Funzione beta) Mostra annunci video standard sulla rete del pubblico.

* *[!UICONTROL Performance Max]:* (Funzione beta) Mostra più tipi di annunci su tutte le reti utilizzando [!DNL Microsoft Advertising] offerte intelligenti. Nelle impostazioni della campagna devi specificare uno o più gruppi di risorse, che includono immagini, loghi, titoli, descrizioni, un invito all’azione facoltativo e segnali di pubblico. La rete di annunci combina automaticamente le risorse per distribuire gli annunci in base al canale.

## [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]:** Un nome di campagna univoco all’interno dell’account. La lunghezza massima è di 128 caratteri.

**[!UICONTROL Status]:** Lo stato di visualizzazione della campagna: *Attivo* o *In pausa*. L’impostazione predefinita per le nuove campagne pubblicitarie è *Attivo*.

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

**[!UICONTROL Bid strategy]:** La strategia di offerta per la campagna:

* *[!UICONTROL Cost per Sale]:* (Solo campagne Shopping) La rete di annunci, non Search, Social e Commerce, ottimizza le offerte in base al [!UICONTROL Target CPS] (costo per vendita). Paghi solo quando un clic sull&#39;annuncio di prodotto determina una vendita entro 24 ore. **Nota:** Non includere nei portfolio le campagne con questa strategia di offerta. L’ottimizzazione per Search, Social e Commerce non è disponibile per le campagne con questa strategia di offerta.

  Una volta salvata una campagna di acquisto per i marchi con questa strategia di offerta, non puoi modificare la strategia di offerta. Per altri tipi di campagne di acquisto, questa strategia è disponibile solo per le nuove campagne.

* *[!UICONTROL CPV]* (Solo campagne video di Audience CTV) Utilizza il modello Costo per visualizzazione (CPV). <!-- Campaigns with this bid strategy aren't optimized when they're included in portfolios. -->

* *[!UICONTROL Enhanced CPC]:* (Campagne sulle reti di pubblico, ricerca e shopping) Utilizza il modello avanzato cost-per-click (eCPC) della rete di annunci, che consente alla rete di annunci di modificare automaticamente l’offerta cost-per-click (CPC) per ogni asta nel tentativo di massimizzare le conversioni, utilizzando le conversioni specificate all’interno della rete di annunci (non in Search, Social e Commerce), cercando al contempo di mantenere il CPC medio al di sotto del CPC massimo.

  Quando aggiungi una campagna con eCPC a un portfolio ottimizzato di Search, Social e Commerce, Search, Social e Commerce ottimizzano le offerte di base e quando &quot;[!UICONTROL Auto adjust campaign budget limits]&quot;è abilitata l’opzione&quot;: il budget della campagna. La rete di annunci ottimizza tutte le regolazioni delle offerte e può modificare le offerte generate da Search, Social e Commerce al momento della query utente in base a dati e informazioni proprietari. **Attenzione:** Utilizza le campagne eCPC nei portfolio solo quando il totale delle conversioni tracciate nella rete di annunci è in linea con l’obiettivo del portfolio.

* *[!UICONTROL Manual CPC]*: (campagne commerciali per i marchi; [!DNL Microsoft Store Ads] campagne; obsoleto per altri tipi di campagne) Utilizza il modello CPC (cost-per-click). Per alcuni tipi di annunci, puoi facoltativamente consentire alla rete di annunci di modificare le offerte per la campagna:

   * **[!UICONTROL Enable Enhanced CPC]** (disabilitato per impostazione predefinita): questa opzione è uguale all’utilizzo del tasto &quot;[!UICONTROL Enhanced CPC]&quot;.

* *[!UICONTROL Manual CPA]:* ([!DNL Microsoft Store Ads] Campagne ) Utilizza il modello CPA (Cost per acquisition).

* *[!UICONTROL Manual CPM]* (Solo campagne per pubblico e campagne video per pubblico) Utilizza il modello CPM (cost-per-THOUSE-IMPRESSION), per il quale si specifica cosa si desidera spendere per 1.000 impression visualizzate. Le campagne con questa strategia di offerta non sono ottimizzate quando sono incluse nei portfolio.

* *[!UICONTROL Maximize Clicks]:* (Campagne di ricerca e shopping) La rete di annunci, non Search, Social e Commerce, ottimizza le offerte per massimizzare i clic. È possibile inserire un **[!UICONTROL Max CPC]** (costo per clic) per garantire che la rete di annunci non paghi più di un importo specifico per ogni clic. **Attenzione:** Quando aggiungi una campagna con questa strategia a un portfolio, il peso del clic (non l’obiettivo del portfolio) guida le offerte.

* *[!UICONTROL Maximize Conversion Value]:* (Search and shopping/reti di acquisto intelligenti, campagne con le massime prestazioni) La rete di annunci, non Search, Social e Commerce, ottimizza le offerte per massimizzare il valore di conversione. È possibile inserire un **[!UICONTROL Target Return on Ad Spend]** (ROAS) in percentuale. **Nota:** Utilizza questa opzione per le campagne in portfolio ibridi ma non in portfolio standard.

* *[!UICONTROL Maximize Conversions]:* (Campagne e campagne con prestazioni massime sulla rete di ricerca o sulla rete di pubblico (ma non su video di pubblico o TV connessa). La rete di annunci, non su Search, Social e Commerce, ottimizza le offerte per massimizzare le conversioni. È possibile inserire un **[!UICONTROL Target CPC]** (costo per clic). Per le campagne per il pubblico, puoi anche inserire un **[!UICONTROL Target CPA]** (costo per acquisizione). **Nota:** Utilizza questa opzione per le campagne in portfolio ibridi ma non in portfolio standard.

* *[!UICONTROL Target CPA]:* (Campagne nella rete di ricerca) La rete di annunci, non Search, Social e Commerce, ottimizza le offerte sulla base di un **[!UICONTROL Target CPA]** (costo per acquisizione), che è l’importo medio di 30 giorni che desideri pagare per un’acquisizione (conversione). **Nota:** Utilizza questa opzione per le campagne in portfolio ibridi (ma non in portfolio standard) con qualsiasi strategia di spesa a eccezione [!UICONTROL Weekly] o [!UICONTROL Google Target CPA].

  I dati relativi alla posizione media e alle offerte CPC non sono disponibili per le campagne con questa strategia di offerta.

* *[!UICONTROL Target Impression Share]:* (Campagne nella rete di ricerca) La rete di annunci, non Search, Social e Commerce, ottimizza le offerte per raggiungere una quota di impression target e una posizione di annunci. È possibile inserire un **[!UICONTROL Target Impression Share]** in percentuale, il valore **[!UICONTROL Target Ad Position]**, e un **[!UICONTROL Max CPC]** (costo per clic). **Nota:** Questa opzione non è supportata nei portfolio ibridi.

* *[!UICONTROL Target Return on Ad Spend]:* (Campagne sulle reti di ricerca e shopping) La rete di annunci, non Search, Social e Commerce, ottimizza le offerte in base al tuo **[!UICONTROL Target ROAS]** (ritorno sulla spesa pubblicitaria), specificato come percentuale. È possibile inserire un **[!UICONTROL Max CPC]** (costo per clic) per garantire che la rete di annunci non paghi più di un importo specifico per ogni clic. **Nota:** Utilizza questa opzione per le campagne in portfolio ibridi (ma non in portfolio standard) con qualsiasi strategia di spesa a eccezione [!UICONTROL Weekly] o [!UICONTROL Google Target ROAS].

  I dati relativi alla posizione media e alle offerte CPC non sono disponibili per le campagne con questa strategia di offerta.

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]:** (Solo campagne commerciali; sola lettura per le campagne esistenti) Il paese in cui vengono venduti i prodotti della campagna. Poiché i prodotti sono associati ai paesi di destinazione, questa impostazione determina quali prodotti vengono pubblicizzati nella campagna.

<!-- **[!UICONTROL Campaign Priority]:** -->

**[!UICONTROL Link with Microsoft Merchant Center]:** (Solo campagne di pubblico; facoltativo) collega la campagna con un negozio di centro commerciale specifico per annunci basati su feed automatizzati anziché annunci reattivi. Quando selezioni questa opzione, specifica la [!UICONTROL Merchant ID] e [!UICONTROL Products]. Devi creare gruppi di annunci per la campagna, ma non è necessario creare annunci.

Una volta collegata la campagna a un negozio e salvate le impostazioni, non puoi modificare questa opzione.

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}

**[!UICONTROL Products]:** (Campagne di pubblico collegate solo a un negozio di centri commerciali) I prodotti da pubblicizzare. Per impostazione predefinita, *[!UICONTROL All products]* è selezionato. Per pubblicizzare solo i prodotti con attributi specifici, seleziona *[!UICONTROL Filter products]* e specifica fino a sette combinazioni di dimensioni e attributi del prodotto su cui filtrare i prodotti. Tutti i valori specificati devono essere applicabili affinché gli annunci vengano visualizzati per il prodotto. Ad esempio, per visualizzare gli annunci per le forniture di animali Acme, puoi creare i filtri `Custom Label 1=animals`, `Category=pet supplies`, e `Brand=Acme Pet Supplies`.

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## [!UICONTROL Campaign Targeting]

**[!UICONTROL Languages]:** (Solo campagne con prestazione massima) La lingua dell’annuncio, che deve corrispondere alla lingua dei siti in cui l’annuncio può comparire. [!DNL Microsoft Advertising] determina la lingua di un utente da vari segnali, tra cui la query dell&#39;utente, il paese dell&#39;editore e l&#39;impostazione della lingua dell&#39;utente.

<!-- **[!UICONTROL Location Targets]:** -->

{{$include /help/_includes/location-targets.md}}

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

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

{{$include /help/_includes/negative-keyword-note-microsoft.md}}

## [!UICONTROL Negative Websites]

**[!UICONTROL Negative Websites]:** (Campagne solo sulla rete nativa/di visualizzazione; facoltativo) Siti sulla rete di visualizzazione in cui non desideri visualizzare gli annunci. Immetti un URL valido, ad esempio www.example.com. Per specificare più stringhe, separarle con virgole o immetterle su righe separate.

Per informazioni sulla disponibilità, consulta l’Aiuto di Microsoft Advertising per &quot;[Impedire la visualizzazione di annunci su siti Web specifici](https://help.ads.microsoft.com/#apex/bae/en/14061/0).&quot;

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

**[!UICONTROL Asset Group Name]:** Nome della cartella risorse (gruppo di risorse).

**[!UICONTROL Asset Group Status]:** Stato del gruppo di risorse: *[!UICONTROL Active]* o *[!UICONTROL Paused]*.

**[!UICONTROL Final URL]:** L’URL finale per tutti gli annunci creati dal gruppo di risorse.

**[!UICONTROL Images]:** Fino a 20 immagini per l’annuncio, tra cui almeno un’immagine quadrata e un’immagine orizzontale. Consulta la [[!DNL Microsoft Advertising] linee guida per le immagini](https://help.ads.microsoft.com/#apex/ads/en/60204/0). Puoi caricare le immagini o selezionarle dal tuo [!UICONTROL Asset Library] — ma non entrambi nella stessa operazione.

* Per caricare le immagini:

   1. Il giorno [!UICONTROL Upload from Device] , fare clic su **[!UICONTROL +]** e selezionare le immagini dal dispositivo o dalla rete.

   1. Per ogni immagine:

      1. Seleziona le proporzioni.

      1. Trascinate e posizionate la casella di ritaglio in base alle necessità per selezionare la parte visualizzabile dell&#39;immagine e, se possibile, ridimensionate la parte visualizzabile.

      1. (Facoltativo) Selezionate altre proporzioni e, se necessario, riposizionate e ridimensionate l&#39;immagine per ogni proporzione selezionata.

         Viene creata una risorsa per ogni proporzione selezionata.

      1. Clic **[!UICONTROL Proceed]**.

   1. Al termine della specifica delle immagini, fare clic su **[!UICONTROL Upload]**.

* Per selezionare immagini dal [!UICONTROL Asset Library], fai clic su **[!UICONTROL Asset Library]** e selezionare le immagini.

**[!UICONTROL Logos]:** Almeno un logo. Puoi includere fino a cinque. Consulta la [[!DNL Microsoft Advertising] linee guida per le risorse](https://help.ads.microsoft.com/#apex/ads/en/60204/0). Puoi caricare le immagini o selezionarle dal tuo [!UICONTROL Asset Library] — ma non entrambi nella stessa operazione.

* Per caricare le immagini:

   1. Il giorno [!UICONTROL Upload from Device] , fare clic su **[!UICONTROL +]** e selezionare le immagini dal dispositivo o dalla rete.

   1. Per ogni immagine:

      1. Seleziona le proporzioni.

      1. Trascinate e posizionate la casella di ritaglio in base alle necessità per selezionare la parte visualizzabile dell&#39;immagine e, se possibile, ridimensionate la parte visualizzabile.

      1. (Facoltativo) Selezionate altre proporzioni e, se necessario, riposizionate e ridimensionate l&#39;immagine per ogni proporzione selezionata.

         Viene creata una risorsa per ogni proporzione selezionata.

      1. Clic **[!UICONTROL Proceed]**.

   1. Al termine della specifica delle immagini, fare clic su **[!UICONTROL Upload]**.

* Per selezionare immagini dal [!UICONTROL Asset Library], fai clic su **[!UICONTROL Asset Library]** e selezionare le immagini.

**[!UICONTROL Headlines]:** Almeno tre e fino a 15 titoli brevi con un massimo di 30 caratteri ciascuno. È possibile immettere testo o selezionare risorse dal [!UICONTROL Asset Library] — ma non entrambi nella stessa operazione.

* Per immettere il testo:

   1. Il giorno [!UICONTROL Enter Text] , immettere il testo.

   1. (Facoltativo) Per aggiungere un&#39;altra stringa di testo, fare clic su **[!UICONTROL + Add]** e inserisci la stringa.

* Per selezionare le risorse dal [!UICONTROL Asset Library], fai clic su **[!UICONTROL Asset Library]** e seleziona le risorse.

**[!UICONTROL Long Headlines]:** Almeno uno e fino a cinque titoli lunghi con un massimo di 90 caratteri ciascuno. È possibile immettere testo o selezionare risorse dal [!UICONTROL Asset Library] — ma non entrambi nella stessa operazione.

* Per immettere il testo:

   1. Il giorno [!UICONTROL Enter Text] , immettere il testo.

   1. (Facoltativo) Per aggiungere un&#39;altra stringa di testo, fare clic su **[!UICONTROL + Add]** e inserisci la stringa.

* Per selezionare le risorse dal [!UICONTROL Asset Library], fai clic su **[!UICONTROL Asset Library]** e seleziona le risorse.

**[!UICONTROL Descriptions]:** Almeno due descrizioni e fino a cinque descrizioni con un massimo di 90 caratteri ciascuna. È possibile immettere testo o selezionare risorse dal [!UICONTROL Asset Library] — ma non entrambi nella stessa operazione.

* Per immettere il testo:

   1. Il giorno [!UICONTROL Enter Text] , immettere il testo.

   1. (Facoltativo) Per aggiungere un&#39;altra stringa di testo, fare clic su **[!UICONTROL + Add]** e inserisci la stringa.

* Per selezionare le risorse dal [!UICONTROL Asset Library], fai clic su **[!UICONTROL Asset Library]** e seleziona le risorse.

**[!UICONTROL Call to Action]:** Invito all’azione da includere nell’annuncio. Per impostazione predefinita, *[!UICONTROL Act Now]* è selezionato.

**[!UICONTROL Business Name]:** La ragione sociale, con un massimo di 25 caratteri. Non può contenere script, HTML o un altro linguaggio di markup.

**[!UICONTROL Audience Signal]:** (Facoltativo) [!DNL Microsoft Advertising] tipi di pubblico da utilizzare come segnali di pubblico per la campagna. [!DNL Microsoft Advertising] i modelli di apprendimento automatico utilizzano i tipi di pubblico per trovare surfisti web simili a targetizzare e possono anche mostrare annunci a tipi di pubblico che non sono specificati come segnali per aiutarti a raggiungere gli obiettivi di prestazioni. Scegli i tipi di pubblico che hanno più probabilità di essere convertiti.

>[!NOTE]
>I segnali del pubblico sono diversi da [target del pubblico a livello di gruppo di annunci](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md).

<!-- **[!UICONTROL Display Path 1]**, **[!UICONTROL Display Path 2]:** -->

{{$include /help/_includes/display-path1-2.md}}

**[!UICONTROL Add new asset group]:** Consente di specificare un altro gruppo di risorse.

## [!UICONTROL Conversion Goals]

**[!UICONTROL Conversion Goal]:** Se a *[!UICONTROL Use account conversion goals for this campaign]* (impostazione predefinita) oppure *[!UICONTROL Use campaign specific conversion goals]*. Se scegli di specificare gli obiettivi di conversione per la campagna, seleziona gli obiettivi dall’elenco di tutti gli obiettivi disponibili. **Nota:** Gli obiettivi vengono sincronizzati ogni giorno, pertanto gli obiettivi creati nelle 24 ore precedenti potrebbero non essere elencati. Per aggiornare l&#39;elenco: [sincronizzare manualmente i dati della rete di annunci](/help/search-social-commerce/campaign-management/campaigns/sync-network.md).

>[!TIP]
>
>Per i portfolio ibridi per i quali carichi gli obiettivi nella rete di annunci, la best practice è quella di utilizzare obiettivi a livello di campagna che corrispondono agli obiettivi di conversione nell’obiettivo del portfolio. Tuttavia, se gli obiettivi della campagna includono conversioni tracciate da [!DNL Microsoft Advertising] tag di tracciamento degli eventi universali (UET), quindi aggiungili all’interno del [!DNL Microsoft Advertising] perché non vengono caricati nuovamente sulla rete di annunci con l’obiettivo. Inoltre, all&#39;interno del [!DNL Microsoft Advertising] , rimuovi le azioni di conversione della campagna come obiettivi predefiniti dell’account deselezionando &quot;includi nelle conversioni&quot;.

<!-- Check on this:
>If the campaign is part of a hybrid portfolio, then use only conversion goals that are included in the portfolio's objective for the campaign. Including additional conversion goals may impact portfolio performance.
>
>The objective may include conversion goals or other conversions that aren't included for the campaign, but the campaign can't include conversion goals that aren't included in the objective.
-->

>[!MORELIKETHIS]
>
>* [Gestire le campagne](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
