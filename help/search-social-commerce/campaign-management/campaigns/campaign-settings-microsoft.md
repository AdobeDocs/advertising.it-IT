---
title: '[!DNL Microsoft Advertising] impostazioni campagna'
description: Fai riferimento alle impostazioni per  [!DNL Microsoft Advertising]  campagne.
exl-id: f11cb61e-d627-4074-870d-e186f3e65572
feature: Search Campaign Management
source-git-commit: 096271a2e9daddc20f7f5f4e0063fda21974c8a1
workflow-type: tm+mt
source-wordcount: '2001'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] impostazioni campagna

## \[Schermata Creazione campagna\]

**[!UICONTROL Campaign Type]:** (disponibile solo durante la creazione della campagna) Dove inserire annunci e quali tipi di annunci
la campagna può contenere:

* *[!UICONTROL Search]:* mostra gli annunci di testo nella rete di ricerca.

* *[!UICONTROL Shopping Network]:* mostra gli annunci di prodotti, per i prodotti nel catalogo prodotti [!DNL Microsoft Merchant Center], sulla rete di acquisti.

* *[!UICONTROL Audience]:* mostra annunci nativi/di visualizzazione in [!DNL Microsoft Audience Network]. È possibile a) generare automaticamente annunci basati su feed collegando la campagna a un negozio di merchant center nella sezione [!UICONTROL Shopping Settings] oppure b) creare annunci reattivi con risorse di testo e immagini caricate. Entrambe le opzioni richiedono la creazione di gruppi di annunci con targeting utente.

* *[!UICONTROL Shopping Campaigns for Brands]:* promuove i prodotti tramite rivenditori collegati attraverso le reti di ricerca e pubblico. È possibile creare gruppi di annunci e gruppi di prodotti secondari (app da promuovere) e annunci di prodotti facoltativi per la campagna; [!DNL Microsoft Advertising] crea automaticamente annunci per i gruppi di prodotti. Per le campagne di acquisto dei marchi, utilizzare la strategia di offerta [!UICONTROL Manual CPC]; per le promozioni di acquisto dei marchi, utilizzare la strategia di offerta [!UICONTROL Cost per Sale].

* *[!UICONTROL Microsoft Store Ads Campaign]:* promuove le app e i giochi disponibili in [!DNL Microsoft Store]. È possibile creare gruppi di annunci secondari, gruppi di prodotti e annunci di prodotti facoltativi per la campagna; [!DNL Microsoft Advertising] crea automaticamente annunci per i gruppi di prodotti.

* *[!UICONTROL Audience CTV Video]:* mostra gli annunci video TV connessi (CTV) sulla rete del pubblico.

* *[!UICONTROL Audience Video]:* mostra gli annunci video standard sulla rete del pubblico.

* *[!UICONTROL Performance Max]:* mostra più tipi di annunci in tutte le reti utilizzando [!DNL Microsoft Advertising] offerte intelligenti. Nelle impostazioni della campagna devi specificare uno o più gruppi di risorse, che includono immagini, loghi, titoli, descrizioni, un invito all’azione facoltativo e segnali di pubblico. La rete di annunci combina automaticamente le risorse per distribuire gli annunci in base al canale.

## [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]:** Nome di campagna univoco all&#39;interno dell&#39;account. La lunghezza massima è di 128 caratteri.

**[!UICONTROL Status]:** Lo stato di visualizzazione della campagna: *Attivo* o *In pausa*. Il valore predefinito per le nuove campagne pubblicitarie è *Attivo*.

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

* *[!UICONTROL Cost per Sale]:* (solo campagne Shopping) La rete di annunci, non Search, Social e Commerce, ottimizza le offerte in base a [!UICONTROL Target CPS] (costo per vendita). Paghi solo quando un clic sull&#39;annuncio di prodotto determina una vendita entro 24 ore. **Nota:** non includere nei portfolio le campagne con questa strategia di offerta. L’ottimizzazione per Search, Social e Commerce non è disponibile per le campagne con questa strategia di offerta.

  Una volta salvata una campagna di acquisto per i marchi con questa strategia di offerta, non puoi modificare la strategia di offerta. Per altri tipi di campagne di acquisto, questa strategia è disponibile solo per le nuove campagne.

* *[!UICONTROL CPV]* (solo campagne video CTV di pubblico) utilizza il modello Costo per visualizzazione (CPV). Search, Social e Commerce non forniscono l’ottimizzazione per le campagne con questa strategia di offerta incluse nei portfolio.

* *[!UICONTROL Enhanced CPC]:* (campagne sulle reti di pubblico, ricerca e shopping) Utilizza il modello avanzato di eCPC (cost-per-click) della rete di annunci, che consente alla rete di annunci di modificare automaticamente l&#39;offerta CPC (cost-per-click) per ogni asta nel tentativo di massimizzare le conversioni, utilizzando le conversioni specificate all&#39;interno della rete di annunci (non in Search, Social e Commerce), cercando al contempo di mantenere il CPC medio al di sotto del CPC massimo.

  Quando aggiungi una campagna con eCPC a un portfolio ottimizzato di Search, Social e Commerce, Search, Social e Commerce ottimizzano le offerte di base e, se l&#39;opzione &quot;[!UICONTROL Auto adjust campaign budget limits]&quot; è abilitata, il budget della campagna. La rete di annunci ottimizza tutte le regolazioni delle offerte e può modificare le offerte generate da Search, Social e Commerce al momento della query utente in base a dati e informazioni proprietari. **Attenzione:** utilizza le campagne eCPC nei portfolio solo quando il totale delle conversioni tracciate nella rete di annunci è allineato con l&#39;obiettivo del portfolio.

* *[!UICONTROL Manual CPC]*: (campagne acquisti per marchi; [!DNL Microsoft Store Ads] campagne; obsoleto per altri tipi di campagne) usa il modello CPC (costo per clic). Per alcuni tipi di annunci, puoi facoltativamente consentire alla rete di annunci di modificare le offerte per la campagna:

   * **[!UICONTROL Enable Enhanced CPC]** (disabilitato per impostazione predefinita): questa opzione è uguale a quella utilizzata per l&#39;opzione &quot;[!UICONTROL Enhanced CPC]&quot;.

* *[!UICONTROL Manual CPA]:* ([!DNL Microsoft Store Ads] campagne) Utilizza il modello di costo per acquisizione (CPA).

* *[!UICONTROL Manual CPM]* (solo campagne pubblico e campagne video di pubblico) Utilizza il modello CPM (cost-per-millemila-impressions), per il quale si specifica quanto si desidera spendere per 1.000 impression visualizzate. Le campagne con questa strategia di offerta non sono ottimizzate quando sono incluse nei portfolio.

* *[!UICONTROL Maximize Clicks]:* (campagne Search&amp;Shopping) La rete di annunci, non Search, Social e Commerce, ottimizza le offerte per massimizzare i clic. Facoltativamente, immetti un **[!UICONTROL Max CPC]** (costo per clic) per garantire che la rete di annunci non paghi più di un importo specifico per ogni clic. **Attenzione:** quando aggiungi una campagna con questa strategia a un portfolio, il peso del clic (non l&#39;obiettivo del portfolio) guida le offerte.

* *[!UICONTROL Maximize Conversion Value]:* (reti Search and Shopping/Smart Shopping, campagne con prestazioni massime) La rete di annunci, non Search, Social e Commerce, ottimizza le offerte per massimizzare il valore di conversione. È possibile immettere un valore di **[!UICONTROL Target Return on Ad Spend]** (ROAS) come percentuale. **Nota:** utilizza questa opzione per le campagne in portfolio ibridi ma non in portfolio standard.

* *[!UICONTROL Maximize Conversions]:* (campagne e campagne con prestazioni massime sulla rete di ricerca o sulla rete di pubblico (ma non video di pubblico o TV connessa)) La rete di annunci, non Search, Social e Commerce, ottimizza le offerte per massimizzare le conversioni. Facoltativamente, immettere **[!UICONTROL Target CPC]** (costo per clic). Per le campagne per il pubblico, puoi anche immettere un valore facoltativo **[!UICONTROL Target CPA]** (costo per acquisizione). **Nota:** utilizza questa opzione per le campagne in portfolio ibridi ma non in portfolio standard.

* *[!UICONTROL Target CPA]:* (campagne nella rete di ricerca) La rete di annunci, non Search, Social e Commerce, ottimizza le offerte in base a un **[!UICONTROL Target CPA]** facoltativo (costo per acquisizione), che è l&#39;importo medio di 30 giorni che si desidera pagare per un&#39;acquisizione (conversione). **Nota:** utilizza questa opzione per le campagne in portfolio ibridi (ma non in portfolio standard) con qualsiasi strategia di spesa eccetto [!UICONTROL Weekly] o [!UICONTROL Google Target CPA].

  I dati relativi alla posizione media e alle offerte CPC non sono disponibili per le campagne con questa strategia di offerta.

* *[!UICONTROL Target Impression Share]:* (campagne nella rete di ricerca) La rete di annunci, non Search, Social e Commerce, ottimizza le offerte per ottenere una quota di impression target e una posizione di annunci. Facoltativamente, immettere un **[!UICONTROL Target Impression Share]** come percentuale, il **[!UICONTROL Target Ad Position]** e un **[!UICONTROL Max CPC]** (costo per clic). **Nota:** questa opzione non è supportata nei portfolio ibridi.

* *[!UICONTROL Target Return on Ad Spend]:* (campagne nelle reti di ricerca e shopping) La rete di annunci, non Search, Social e Commerce, ottimizza le offerte in base a **[!UICONTROL Target ROAS]** (ritorno sulla spesa pubblicitaria), specificato come percentuale. Facoltativamente, immetti un **[!UICONTROL Max CPC]** (costo per clic) per garantire che la rete di annunci non paghi più di un importo specifico per ogni clic. **Nota:** utilizza questa opzione per le campagne in portfolio ibridi (ma non in portfolio standard) con qualsiasi strategia di spesa eccetto [!UICONTROL Weekly] o [!UICONTROL Google Target ROAS].

  I dati relativi alla posizione media e alle offerte CPC non sono disponibili per le campagne con questa strategia di offerta.

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]:** (solo campagne Shopping; sola lettura per campagne esistenti) Il paese in cui
i prodotti della campagna sono venduti. Poiché i prodotti sono associati ai paesi di destinazione, questa impostazione determina quali prodotti vengono pubblicizzati nella campagna.

<!-- **[!UICONTROL Campaign Priority]:** -->

**[!UICONTROL Link with Microsoft Merchant Center]:** (solo campagne pubblico; facoltativo) collega la campagna con un archivio merchant specifico per annunci basati su feed automatizzati anziché annunci reattivi. Quando si seleziona questa opzione, specificare [!UICONTROL Merchant ID] e [!UICONTROL Products]. Devi creare gruppi di annunci per la campagna, ma non è necessario creare annunci.

Una volta collegata la campagna a un negozio e salvate le impostazioni, non puoi modificare questa opzione.

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}

**[!UICONTROL Products]:** (solo campagne del pubblico collegate a un negozio di centri commerciali) I prodotti da pubblicizzare. Per impostazione predefinita, è selezionato *[!UICONTROL All products]*. Per pubblicizzare solo i prodotti con attributi specifici, selezionare *[!UICONTROL Filter products]* e specificare fino a sette combinazioni di dimensioni e attributi del prodotto su cui filtrare i prodotti. Tutti i valori specificati devono essere applicabili affinché gli annunci vengano visualizzati per il prodotto. Ad esempio, per visualizzare annunci per forniture per animali Acme, puoi creare i filtri `Custom Label 1=animals`, `Category=pet supplies` e `Brand=Acme Pet Supplies`.

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## [!UICONTROL Campaign Targeting]

**[!UICONTROL Languages]:** (solo campagne con prestazione massima) La lingua dell&#39;annuncio, che deve corrispondere alla lingua dei siti in cui l&#39;annuncio può essere visualizzato. [!DNL Microsoft Advertising] determina la lingua di un utente da vari segnali, tra cui la query dell&#39;utente, il paese dell&#39;editore e l&#39;impostazione della lingua dell&#39;utente.

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

**[!UICONTROL Negative Websites]:** (solo campagne nella rete di visualizzazione/nativa; facoltativo) Siti nella rete di visualizzazione in cui non si desidera visualizzare gli annunci. Immetti un URL valido, ad esempio www.example.com. Per specificare più stringhe, separarle con virgole o immetterle su righe separate.

Per informazioni sulla disponibilità, vedere la Guida di Microsoft Advertising per &quot;[impedire la visualizzazione di annunci su siti Web specifici](https://help.ads.microsoft.com/#apex/bae/en/14061/0).&quot;

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

**[!UICONTROL Asset Group Name]:** Nome della cartella risorse (gruppo di risorse).

**[!UICONTROL Asset Group Status]:** Lo stato del gruppo di risorse: *[!UICONTROL Active]* o *[!UICONTROL Paused]*.

**[!UICONTROL Final URL]:** URL finale per tutti gli annunci creati dal gruppo di risorse.

**[!UICONTROL Images]:** Fino a 20 immagini per l&#39;annuncio, tra cui almeno un&#39;immagine quadrata e un&#39;immagine orizzontale. Consulta le [[!DNL Microsoft Advertising] linee guida per le immagini](https://help.ads.microsoft.com/#apex/ads/en/60204/0). È possibile caricare immagini o selezionarle da [!UICONTROL Asset Library], ma non entrambe nella stessa operazione.

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

**[!UICONTROL Logos]:** Almeno un logo. Puoi includere fino a cinque. Consulta le [[!DNL Microsoft Advertising] linee guida per le risorse](https://help.ads.microsoft.com/#apex/ads/en/60204/0). È possibile caricare immagini o selezionarle da [!UICONTROL Asset Library], ma non entrambe nella stessa operazione.

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

**[!UICONTROL Headlines]:** Almeno tre e fino a 15 titoli brevi con un massimo di 30 caratteri ciascuno. È possibile immettere testo o selezionare risorse da [!UICONTROL Asset Library], ma non entrambi nella stessa operazione.

* Per immettere il testo:

   1. Nella scheda [!UICONTROL Enter Text] immettere il testo.

   1. (Facoltativo) Per aggiungere un&#39;altra stringa di testo, fare clic su **[!UICONTROL + Add]** e immettere la stringa.

* Per selezionare le risorse da [!UICONTROL Asset Library], fai clic su **[!UICONTROL Asset Library]** e seleziona le risorse.

**[!UICONTROL Long Headlines]:** Almeno uno e fino a cinque titoli lunghi con un massimo di 90 caratteri ciascuno. È possibile immettere testo o selezionare risorse da [!UICONTROL Asset Library], ma non entrambi nella stessa operazione.

* Per immettere il testo:

   1. Nella scheda [!UICONTROL Enter Text] immettere il testo.

   1. (Facoltativo) Per aggiungere un&#39;altra stringa di testo, fare clic su **[!UICONTROL + Add]** e immettere la stringa.

* Per selezionare le risorse da [!UICONTROL Asset Library], fai clic su **[!UICONTROL Asset Library]** e seleziona le risorse.

**[!UICONTROL Descriptions]:** almeno due descrizioni e fino a cinque descrizioni con un massimo di 90 caratteri ciascuna. È possibile immettere testo o selezionare risorse da [!UICONTROL Asset Library], ma non entrambi nella stessa operazione.

* Per immettere il testo:

   1. Nella scheda [!UICONTROL Enter Text] immettere il testo.

   1. (Facoltativo) Per aggiungere un&#39;altra stringa di testo, fare clic su **[!UICONTROL + Add]** e immettere la stringa.

* Per selezionare le risorse da [!UICONTROL Asset Library], fai clic su **[!UICONTROL Asset Library]** e seleziona le risorse.

**[!UICONTROL Call to Action]:** Invito all&#39;azione da includere nell&#39;annuncio. Per impostazione predefinita, è selezionato *[!UICONTROL Act Now]*.

**[!UICONTROL Business Name]:** Nome aziendale, con un massimo di 25 caratteri. Non può contenere script, HTML o un altro linguaggio di markup.

**[!UICONTROL Audience Signal]:** (facoltativo) [!DNL Microsoft Advertising] tipi di pubblico da utilizzare come segnali di pubblico per la campagna. I modelli di apprendimento automatico di [!DNL Microsoft Advertising] utilizzano i tipi di pubblico per trovare surfisti web simili a target e possono anche mostrare annunci a tipi di pubblico non specificati come segnali per aiutarti a raggiungere gli obiettivi prestazionali. Scegli i tipi di pubblico che hanno più probabilità di essere convertiti.

>[!NOTE]
>I segnali di pubblico sono diversi dalle [destinazioni di pubblico a livello di gruppo di annunci](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md).

<!-- **[!UICONTROL Display Path 1]**, **[!UICONTROL Display Path 2]:** -->

{{$include /help/_includes/display-path1-2.md}}

**[!UICONTROL Add new asset group]:** Consente di specificare un altro gruppo di risorse.

## [!UICONTROL Conversion Goals]

**[!UICONTROL Conversion Goal]:** Se *[!UICONTROL Use account conversion goals for this campaign]* (impostazione predefinita) o *[!UICONTROL Use campaign specific conversion goals]*. Se scegli di specificare gli obiettivi di conversione per la campagna, seleziona gli obiettivi dall’elenco di tutti gli obiettivi disponibili. **Nota:** gli obiettivi vengono sincronizzati ogni giorno, pertanto gli obiettivi creati nelle 24 ore precedenti potrebbero non essere elencati. Per aggiornare l&#39;elenco, [sincronizzare manualmente i dati della rete di annunci](/help/search-social-commerce/campaign-management/campaigns/sync-network.md).

>[!TIP]
>
>Se la campagna fa parte di un portfolio ibrido, la best practice consiste nell’utilizzare obiettivi a livello di campagna che corrispondono agli obiettivi di conversione nell’obiettivo del portfolio; l’inclusione di obiettivi di conversione aggiuntivi può influire sulle prestazioni del portfolio.
>
> Tuttavia, per le campagne in portfolio ibridi per le quali [carichi gli obiettivi nella rete di annunci](/help/search-social-commerce/tools/objective-upload-to-networks.md), effettua le seguenti operazioni nell&#39;editor della rete di annunci invece che qui: a) aggiungi la metrica di obiettivo del portfolio Search, Social e Commerce caricato (che inizia con &quot;O_ACS_OBJ&quot;) come obiettivo di conversione per la campagna; e b) aggiungi tutti gli obiettivi della campagna che includono le conversioni tracciate dal tag UET (Universal Event Tracking) di [!DNL Microsoft Advertising], perché le metriche tracciate nella rete di annunci non vengono caricate nella rete di annunci con l&#39;obiettivo.

>[!MORELIKETHIS]
>
>* [Gestisci campagne](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
