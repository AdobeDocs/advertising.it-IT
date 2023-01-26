---
title: Colonne nei fogli di calcolo scaricati/caricati
description: Fai riferimento alle colonne nei fogli di calcolo per la qualità di Excel scaricati e caricati.
feature: DSP Placements
exl-id: 8a8dceed-f77d-4b6b-a842-f57528125c92
source-git-commit: 1c13874967ec4ad264e5fa6a5e0dfeb6120f53cc
workflow-type: tm+mt
source-wordcount: '782'
ht-degree: 0%

---

# Colonne nei fogli di calcolo scaricati/caricati

<!-- rename -- not specific enough - I think you can download Excel files of other things too -->

<!-- see notes within the table about descriptions that need to be edited -->

>[!TIP]
>
> In un foglio di calcolo scaricato, tutte le colonne modificabili sono evidenziate in blu.

| Sezione | Colonna | Descrizione | Modificabile? |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic] | [!UICONTROL Placement ID] | ID numerico del posizionamento. | — |
| [!UICONTROL Basic] | [!UICONTROL Placement Name] | Nome del posizionamento. | Sì |
| [!UICONTROL Basic] | [!UICONTROL Labels] | Eventuali etichette applicate, per il reporting. | — |
| [!UICONTROL Basic] | [!UICONTROL Edit Link] | Collegamento per aprire il posizionamento in modalità Modifica. | — |
| [!UICONTROL Basic] | [!UICONTROL Status] | Lo stato del posizionamento: *[!UICONTROL active]* o *[!UICONTROL inactive]*. | Sì |
| [!UICONTROL Basic] | [!UICONTROL Placement Type] | Tipo di posizionamento. | — |
| [!UICONTROL Basic] | [!UICONTROL Package Name] | Nome del pacchetto principale, se applicabile. | — |
| [!UICONTROL Goals] | [!UICONTROL Start Date] | Data di inizio del posizionamento. | — |
| [!UICONTROL Goals] | [!UICONTROL End Date] | Data di fine del posizionamento. | — |
| [!UICONTROL Goals] | [!UICONTROL Day parting] | Se la dayparting è *[!UICONTROL ON]* o *[!UICONTROL OFF]*.<br><b>Nota:</b> Per controllare la pianificazione effettiva del dayparting, apri le impostazioni di posizionamento in DSP. | — |
| [!UICONTROL Goals] | [!UICONTROL Budget] | Il budget di posizionamento, se disponibile. | Sì |
| [!UICONTROL Goals] | [!UICONTROL Budget Interval] | Intervallo di budget: &lt;i span=&quot;&quot; id=&quot;0&quot; translate=&quot;no&quot; />* *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]* oppure *[!UICONTROL All Time]*.[!UICONTROL >Daily] | Sì |
| [!UICONTROL Goals] | [!UICONTROL Optimization Goal] | Obiettivo del pacchetto. | — |
| [!UICONTROL Goals] | [!UICONTROL Optimization Target] | Il valore di destinazione dell&#39;obiettivo. | — |
| [!UICONTROL Goals] | [!UICONTROL Pace on] | Se il posizionamento è in pendenza verso il *[!UICONTROL Budget]* o *[!UICONTROL Impressions]*. | — |
| [!UICONTROL Goals] | [!UICONTROL Max Bid] | L&#39;offerta massima per il posizionamento. | Sì |
| [!UICONTROL Goals] | [!UICONTROL Flight Pacing] | Strategia di volo per il posizionamento: *[!UICONTROL Even]*, *[!UICONTROL slightly ahead]*, *[!UICONTROL frontload]* oppure *[!UICONTROL aggressive frontload]*. | Sì |
| [!UICONTROL Goals] | [!UICONTROL Intraday Pacing] | La strategia di posizionamento intraday: *[!UICONTROL Even]* o *[!UICONTROL ASAP]*. | Sì |
| [!UICONTROL Goals] | [!UICONTROL  Pre-Bid Filters] | Qualsiasi criterio di filtro pre-offerta da applicare. | — |
| [!UICONTROL Goals] | [!UICONTROL Bidding Rules] | Se le regole di offerta (obsoleto) sono *[!UICONTROL ON]* o *[!UICONTROL OFF]*. | — |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap] | Il tappo di frequenza principale per il posizionamento durante il [!UICONTROL Frequency Cap Interval]. | Sì |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap Interval] | Intervallo per il limite di frequenza principale: *[!UICONTROL Day]*, *[!UICONTROL Week]* oppure *[!UICONTROL Month]*. | Sì |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap] | Il limite di frequenza secondario per il posizionamento durante il [!UICONTROL Secondary Frequency Cap Interval] | Sì |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval] | Tipo di intervallo per il limite di frequenza secondario: *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]* oppure *[!UICONTROL Minute]*. Il numero di settimane, giorni, ore o minuti applicabile è indicato dal [!UICONTROL Secondary Frequency Cap Interval Value]. | Sì |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval Value] | Il numero di settimane, giorni, ore o minuti per i quali il [!UICONTROL Secondary Frequency Cap] si applica. Ad esempio, se il limite secondario è tre impression per sei ore, il valore qui sarà <b>6&lt;/>. | Sì |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included #] | Il numero di località geografiche mirate, *[!UICONTROL All]* oppure *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included] | le posizioni geografiche di destinazione, separate da punti e virgola, o *[!UICONTROL All Locations]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded #] | il numero di località geografiche escluse o *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded] | le posizioni geografiche escluse, separate da punti e virgola, o *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Included #] | il numero di eventuali offerte mirate di inventario pubblico, *[!UICONTROL All]* oppure *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Excluded #] | il numero di eventuali offerte di inventario pubblico escluse, oppure *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Included #] | il numero di eventuali offerte di inventario privato mirate, *[!UICONTROL All]* oppure *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Excluded #] | il numero di eventuali offerte di inventario privato escluse, oppure *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Included #] | Numero di destinazioni [!UICONTROL On-Demand Inventory] offerte, se del caso, *[!UICONTROL All]* oppure *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Excluded #] | il numero di offerte On-Demand Inventory escluse, se specificato, oppure *[!UICONTROL None]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Traffic Type] | Il tipo di traffico mirato: *[!UICONTROL Website]* e/o *[!UICONTROL Apps]* | — |
| [!UICONTROL Sites] | [!UICONTROL Exclude out-stream] | Se l&#39;opzione di targeting dell&#39;inventario per escludere il traffico esterno è &lt;i span=&quot;&quot; id=&quot;0&quot; translate=&quot;no&quot; />* o *[!UICONTROL OFF]*.[!UICONTROL >ON]<br>Gli annunci in uscita vengono solitamente visualizzati sopra il contenuto come pop-up o riempiti di contenuto (nell’esperienza nativa), anziché come annunci video normali in un lettore video. | — |
| [!UICONTROL Sites] | [!UICONTROL Site Tier] | La qualità dei siti a cui rivolgersi: *[!UICONTROL Tier 1]*, *[!UICONTROL Tier 2]*, *[!UICONTROL Tier 3]* oppure *[!UICONTROL All Sites]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Included #] | il numero di eventuali categorie di siti di destinazione specificate, oppure *[!UICONTROL All]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Excluded #] | il numero di eventuali categorie di siti esclusi, oppure *[!UICONTROL All]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Excluded Sites] | i siti esclusi, se sono specificati, o *[!UICONTROL None]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Language] | Lingue del sito di destinazione. | — |
| [!UICONTROL Sites] | [!UICONTROL Allow unscreened sites] | (Solo posizionamenti di visualizzazione standard) Consentire o meno la consegna di annunci su siti non controllati: *[!UICONTROL ON]* o *[!UICONTROL OFF]*. Quando il posizionamento esegue il targeting dell’inventario privato, questa opzione può distribuire annunci sui siti bloccati. | — |
| [!UICONTROL Sites] | [!UICONTROL Targeted Sites] | il numero di siti di destinazione, se specificato, oppure *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Included] | i tipi di pubblico di destinazione, se specificati, o *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Excluded] | i tipi di pubblico esclusi, se specificati, o *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Demographic booster] | Indipendentemente o meno [!DNL Comscore] i segmenti demografici sono abilitati per il posizionamento (e altri posizionamenti nella campagna): *[!UICONTROL ON]* o *[!UICONTROL OFF]*. Questa funzione può essere abilitata solo per le campagne per le quali la [!DNL Audience Verification] è abilitata per [!DNL Nielsen] e/o [!DNL Comscore].  Incorrerà commissioni aggiuntive. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Extend across screens] | Se estendere o meno il targeting degli annunci tra i dispositivi: *[!UICONTROL ON]* o *[!UICONTROL OFF]*. Il targeting tra dispositivi estende il targeting su tutti i dispositivi noti di una persona, in base al grafico dei dispositivi specificato nelle impostazioni della campagna. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting] - Incluso # | il numero di eventuali codici di argomento di destinazione specificati, oppure *[!UICONTROL All]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting - Excluded #] | il numero di eventuali codici di argomento esclusi, oppure *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Included #] | il numero di eventuali destinazioni dei dispositivi di destinazione, oppure *[!UICONTROL All]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Excluded #] | il numero di destinazioni dei dispositivi escluse, se specificato, oppure *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Included #] | Il numero di provider ISP interessati, se specificato, o *[!UICONTROL All]/i>. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Excluded #] | il numero di provider di servizi Internet esclusi, se specificato, oppure *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Contextual Filtering #] | il numero di eventuali filtri di sicurezza del marchio applicati, oppure *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Fraud blocking #] | il numero di eventuali filtri di blocco della frode pre-offerta applicati, oppure *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Viewability #] | il numero di filtri di visualizzabilità pre-offerta applicati, se presenti, o *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Site Safety Block] | Se il blocco di sicurezza del sito è abilitato o meno: *[!UICONTROL ON]* o *[!UICONTROL OFF]*.<!-- Whether or not the advertiser-level setting Enable Site Safety Block is enabled: *ON* or *OFF*.I don’t see this option at the placement level. Should there be one? --> | — |
| [!UICONTROL Tracking] | [!UICONTROL Tracking Pixels #] | il numero di pixel di tracciamento eventi di terze parti collegati al posizionamento, o *[!UICONTROL None]*. | — |
| [!UICONTROL Tracking] | [!UICONTROL Conversion Pixels #] | Il numero di pixel di tracciamento della conversione collegati al posizionamento, o *[!UICONTROL None]*. | — |
| [!UICONTROL Tracking] | [!UICONTROL 3rd-party fees] | Tariffa fissa di terzi da rintracciare come costo non fatturabile per 1000 impression, se applicabile. | — |
| [!UICONTROL Ads] | [!UICONTROL # of Ads Attached] | il numero di annunci eventualmente allegati al posizionamento, oppure *[!UICONTROL None]*. | — |
| [!UICONTROL Ads] | [!UICONTROL Ad Names] | i nomi degli annunci eventualmente allegati al posizionamento, oppure *[!UICONTROL None]*. | — |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [Informazioni sulla correzione delle impostazioni di posizionamento per una campagna utilizzando i fogli di calcolo](qa-about.md)
>* [Scaricare le impostazioni di posizionamento per una campagna](qa-sheet-download.md)
>* [Carica le impostazioni di posizionamento per una campagna](qa-sheet-upload.md)
>* [Impostazioni di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md)

