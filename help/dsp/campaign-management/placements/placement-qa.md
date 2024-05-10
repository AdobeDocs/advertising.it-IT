---
title: Revisione e modifica delle impostazioni di posizionamento tramite i fogli di calcolo
description: Scopri come rivedere e modificare le impostazioni di posizionamento chiave utilizzando i fogli di calcolo.
feature: DSP Placements
exl-id: 2de4407d-eb3b-44ff-893c-9fdf6921d4b3
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '1432'
ht-degree: 0%

---

# Revisione e modifica delle impostazioni di posizionamento tramite i fogli di calcolo

Puoi scaricare le impostazioni per uno o più posizionamenti, o per tutti i posizionamenti in una campagna, in formato XLSX (foglio di calcolo Excel) per la revisione. Utilizza questa funzione per rivedere rapidamente dettagli quali:

* Quali tipi di pubblico sono target della campagna.
* Quando i posizionamenti iniziano a consegnare e quando terminano.
* Quali annunci vengono allegati ai posizionamenti.

Puoi quindi apportare modifiche a determinati campi e caricarli nuovamente in DSP in una sola volta. I campi modificabili includono nomi di posizionamento, stati, offerte, budget, strategie di velocità e limiti di frequenza.

>[!TIP]
>
>Per modificare più campi per uno o più posizionamenti, vedi &quot;[Modifica posizionamenti](/help/dsp/campaign-management/placements/placement-edit.md).&quot;

## Scaricare le impostazioni per tutti i posizionamenti in una campagna

1. Nel menu principale, fai clic su **[!UICONTROL Campaigns]**.

1. Effettuare una delle seguenti operazioni:

   * Accanto al nome della campagna, fai clic su **[!UICONTROL ...]** > **[!UICONTROL Download Excel QA sheet]**.

   * Fai clic sul nome della campagna per visualizzarne i dettagli. In alto a destra, fai clic su **[!UICONTROL ...]** > **[!UICONTROL Download Excel QA sheet]**.

   Un messaggio di notifica indica quando il file è disponibile per il download.

1. Effettuare una delle seguenti operazioni:

   * Nel messaggio di notifica, fai clic su **[!UICONTROL Download].**

   * A destra della barra dei menu superiore, fai clic su ![Processi](/help/dsp/assets/downloads.png). Clic **[!UICONTROL Download]** accanto al processo.

   Il file viene salvato nella cartella Download del browser. Consulta &quot;[Colonne nei fogli di calcolo scaricati/caricati](#qa-sheet-columns)&quot; per un elenco delle colonne incluse.

## Scarica impostazioni per uno o più posizionamenti

1. Nel menu principale, fai clic su **[!UICONTROL Campaigns]**.

1. Fai clic sul nome della campagna.

1. Nel sottomenu, fai clic su **[!UICONTROL Placements]**.

1. Seleziona la casella di controllo accanto a ciascun posizionamento di cui desideri scaricare le impostazioni.

1. Nella barra degli strumenti Azioni in blocco, fai clic su **[!UICONTROL ...]** > **[!UICONTROL Download Edit in Excel Sheet]**.

Il file viene salvato automaticamente nella cartella Download del browser. Consulta &quot;[Colonne nei fogli di calcolo scaricati/caricati](#qa-sheet-columns)&quot; per un elenco delle colonne incluse.

## Caricare impostazioni per tutti i posizionamenti in una campagna

1. Nel menu principale, fai clic su **[!UICONTROL Campaigns]**.

1. Effettuare una delle seguenti operazioni:

   * Accanto al nome della campagna, fai clic su **[!UICONTROL ...]** > **[!UICONTROL Upload Excel QA sheet]**.

   * Fai clic sul nome della campagna per visualizzarne i dettagli. In alto a destra, fai clic su **[!UICONTROL ...]** > **[!UICONTROL Upload Excel QA sheet]**.

1. In [!UICONTROL Edit in Excel] finestra di dialogo:

   1. Trascinare e rilasciare un file nella casella oppure fare clic all&#39;interno della casella per selezionare un file dal dispositivo o dalla rete.

   1. Clic **[!UICONTROL Upload]**.

1. (Facoltativo) Per verificare che gli aggiornamenti siano stati elaborati, fai clic su ![Processi](/help/dsp/assets/downloads.png) a destra della barra dei menu superiore.

## Impostazioni di caricamento per uno o più posizionamenti

1. Nel menu principale, fai clic su **[!UICONTROL Campaigns]**.

1. Fai clic sul nome della campagna.

1. Nel sottomenu, fai clic su **[!UICONTROL Placements]**.

1. Seleziona la casella di controllo accanto a ciascun posizionamento di cui desideri caricare le impostazioni.

1. Nella barra degli strumenti Azioni in blocco, fai clic su **[!UICONTROL ...]** > **[!UICONTROL Upload Edit in Excel Sheet]**.

1. In [!UICONTROL Edit in Excel] finestra di dialogo:

   1. Trascinare e rilasciare un file nella casella oppure fare clic all&#39;interno della casella per selezionare un file dal dispositivo o dalla rete.

   1. Clic **[!UICONTROL Upload]**.

1. (Facoltativo) Per verificare che gli aggiornamenti siano stati elaborati, fai clic su ![Processi](/help/dsp/assets/downloads.png) a destra della barra dei menu superiore.

## Colonne delle impostazioni di posizionamento nei fogli di calcolo scaricati/caricati{#qa-sheet-columns}

>[!TIP]
>
> In un foglio di calcolo scaricato, tutte le colonne modificabili sono evidenziate in blu.

### Fogli di calcolo a livello di campagna

| Sezione | Colonna | Descrizione | Modificabile? |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic] | [!UICONTROL Placement ID] | ID numerico del posizionamento. | — |
| [!UICONTROL Basic] | [!UICONTROL Placement Name] | Nome del posizionamento. | Sì |
| [!UICONTROL Basic] | [!UICONTROL Labels] | Eventuali etichette applicate, per la generazione di rapporti. | — |
| [!UICONTROL Basic] | [!UICONTROL Edit Link] | Un collegamento per aprire il posizionamento in modalità Modifica. | — |
| [!UICONTROL Basic] | [!UICONTROL Status] | Lo stato del posizionamento: *[!UICONTROL active]* o *[!UICONTROL inactive]*. | Sì |
| [!UICONTROL Basic] | [!UICONTROL Placement Type] | Il tipo di posizionamento. | — |
| [!UICONTROL Basic] | [!UICONTROL Package Name] | Nome del pacchetto principale, se applicabile. | — |
| [!UICONTROL Goals] | [!UICONTROL Start Date] | Data di inizio del posizionamento. | — |
| [!UICONTROL Goals] | [!UICONTROL End Date] | Data di fine del posizionamento. | — |
| [!UICONTROL Goals] | [!UICONTROL Day parting] | Se dayparting è *[!UICONTROL ON]* o *[!UICONTROL OFF]*.<br><b>Nota:</b> Per verificare l&#39;effettivo programma di dayparting, aprire le impostazioni di posizionamento in DSP. | — |
| [!UICONTROL Goals] | [!UICONTROL Budget] | Il budget di posizionamento, se presente. | Sì |
| [!UICONTROL Goals] | [!UICONTROL Budget Interval] | Intervallo di budget: &lt;i span=&quot;&quot; id=&quot;0&quot; translate=&quot;no&quot; />*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*, o *[!UICONTROL All Time]*.[!UICONTROL >Daily] | Sì |
| [!UICONTROL Goals] | [!UICONTROL Optimization Goal] | Obiettivo del pacchetto. | — |
| [!UICONTROL Goals] | [!UICONTROL Optimization Target] | Il valore target dell’obiettivo. | — |
| [!UICONTROL Goals] | [!UICONTROL Pace on] | Se il posizionamento sta avanzando verso il *[!UICONTROL Budget]* o *[!UICONTROL Impressions]*. | — |
| [!UICONTROL Goals] | [!UICONTROL Max Bid] | Offerta massima per il posizionamento. | Sì |
| [!UICONTROL Goals] | [!UICONTROL Flight Pacing] | La strategia di andamento del volo per il posizionamento: *[!UICONTROL Even]*, *[!UICONTROL slightly ahead]*, *[!UICONTROL frontload]*, o *[!UICONTROL aggressive frontload]*. | Sì |
| [!UICONTROL Goals] | [!UICONTROL Intraday Pacing] | La strategia di andamento infragiornaliero per il posizionamento: *[!UICONTROL Even]* o *[!UICONTROL ASAP]*. | Sì |
| [!UICONTROL Goals] | [!UICONTROL Pre-Bid Filters] | Eventuali criteri di filtro pre-offerta da applicare. | — |
| [!UICONTROL Goals] | [!UICONTROL Bidding Rules] | Indica se le regole di offerta (obsolete) sono *[!UICONTROL ON]* o *[!UICONTROL OFF]*. | — |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap] | Limite di frequenza principale per il posizionamento durante il periodo specificato [!UICONTROL Frequency Cap Interval]. | Sì |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap Interval] | Intervallo per il limite di frequenza principale: *[!UICONTROL Day]*, *[!UICONTROL Week]*, o *[!UICONTROL Month]*. | Sì |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap] | Limite di frequenza secondario per il posizionamento durante il periodo specificato [!UICONTROL Secondary Frequency Cap Interval] | Sì |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval] | Il tipo di intervallo per l’elemento di copertura frequenza secondario: *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]*, o *[!UICONTROL Minute]*. Il numero applicabile di settimane, giorni, ore o minuti è indicato dal [!UICONTROL Secondary Frequency Cap Interval Value]. | Sì |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval Value] | Il numero di settimane, giorni, ore o minuti per i quali [!UICONTROL Secondary Frequency Cap] applicabile. Ad esempio, se il limite secondario è di tre impression per sei ore, il valore qui sarà `6`. | Sì |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included #] | Il numero di località geografiche interessate, *[!UICONTROL All]*, o *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included] | le località geografiche interessate, separate da punti e virgola, oppure *[!UICONTROL All Locations]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded #] | Il numero di località geografiche escluse o *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded] | le località geografiche escluse, separate da un punto e virgola, oppure *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Included #] | Il numero di eventuali operazioni mirate di inventario pubblico, se specificato; *[!UICONTROL All]*, o *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Excluded #] | Il numero di operazioni di inventario pubblico escluse, se specificate, oppure *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Included #] | Il numero di operazioni mirate di inventario privato, se specificate, *[!UICONTROL All]*, o *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Excluded #] | Il numero di operazioni di inventario privato escluse, se specificate, oppure *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Included #] | Il numero di [!UICONTROL On-Demand Inventory] le eventuali offerte, se specificate, *[!UICONTROL All]*, o *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Excluded #] | Il numero di offerte di magazzino On-Demand escluse, se specificate, oppure *[!UICONTROL None]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Traffic Type] | Il tipo di traffico di destinazione: *[!UICONTROL Website]* e/o *[!UICONTROL Apps]* | — |
| [!UICONTROL Sites] | [!UICONTROL Exclude out-stream] | Indica se l&#39;opzione Targeting scorte per escludere il traffico in uscita è &lt;i span=&quot;&quot; id=&quot;0&quot; translate=&quot;no&quot; />* o *[!UICONTROL OFF]*.[!UICONTROL >ON]<br>Gli annunci in uscita vengono solitamente visualizzati sul contenuto come pop-up o inseriti nel contenuto (nell’esperienza nativa), anziché come annunci video regolari in un lettore video. | — |
| [!UICONTROL Sites] | [!UICONTROL Site Tier] | La qualità dei siti di destinazione: *[!UICONTROL Tier 1]*, *[!UICONTROL Tier 2]*, *[!UICONTROL Tier 3]*, o *[!UICONTROL All Sites]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Included #] | Il numero di categorie di siti di destinazione, se presenti, oppure *[!UICONTROL All]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Excluded #] | Il numero di categorie di siti escluse, se presenti, oppure *[!UICONTROL All]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Excluded Sites] | I siti esclusi, se presenti, sono specificati, oppure *[!UICONTROL None]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Language] | Lingue del sito di destinazione. | — |
| [!UICONTROL Sites] | [!UICONTROL Allow unscreened sites] | (Solo posizionamenti di visualizzazione standard) Se consentire o meno la consegna di annunci su siti non controllati: *[!UICONTROL ON]* o *[!UICONTROL OFF]*. Quando il posizionamento ha come target l’inventario privato, questa opzione può distribuire annunci sui siti bloccati. | — |
| [!UICONTROL Sites] | [!UICONTROL Targeted Sites] | Il numero di siti di destinazione, se presenti, oppure *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Included] | I tipi di pubblico target, se presenti, oppure *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Excluded] | I tipi di pubblico esclusi, se presenti, oppure *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Demographic booster] | Indipendentemente dal fatto [!DNL Comscore] i segmenti demografici sono abilitati per il posizionamento (e altri posizionamenti nella campagna): *[!UICONTROL ON]* o *[!UICONTROL OFF]*. Questa funzione può essere abilitata solo per le campagne per le quali [!DNL Audience Verification] la funzione è abilitata per [!DNL Nielsen] e/o [!DNL Comscore].  Esso è soggetto a spese supplementari. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Extend across screens] | Se estendere o meno il targeting dell’annuncio tra i dispositivi: *[!UICONTROL ON]* o *[!UICONTROL OFF]*. Il targeting tra dispositivi estende il targeting su tutti i dispositivi noti di una persona, in base al grafico dei dispositivi specificato nelle impostazioni della campagna. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting] - N. incluso | Il numero di codici argomento di destinazione, se presenti, oppure *[!UICONTROL All]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting - Excluded #] | Il numero di codici argomento esclusi, se presenti, oppure *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Included #] | Il numero di destinazioni dispositivo di destinazione, se presenti, oppure *[!UICONTROL All]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Excluded #] | Il numero di destinazioni dispositivo escluse, se presenti, oppure *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Included #] | Il numero di provider ISP interessati, se presenti, oppure *[!UICONTROL All]/i>. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Excluded #] | il numero di provider ISP esclusi, se presenti, oppure *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Contextual Filtering #] | il numero di filtri di sicurezza del marchio applicati, se presenti, oppure *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Fraud blocking #] | il numero di filtri di blocco antifrode pre-offerta applicati, se presenti, oppure *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Viewability #] | il numero di filtri di visibilità pre-offerta applicati, se presenti, oppure *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Site Safety Block] | Se il blocco di sicurezza del sito è abilitato o meno: *[!UICONTROL ON]* o *[!UICONTROL OFF]*.<!-- Whether or not the advertiser-level setting Enable Site Safety Block is enabled: *ON* or *OFF*.I don’t see this option at the placement level. Should there be one? --> | — |
| [!UICONTROL Tracking] | [!UICONTROL Tracking Pixels #] | Il numero di pixel di terze parti per il tracciamento degli eventi associati al posizionamento, oppure *[!UICONTROL None]*. | — |
| [!UICONTROL Tracking] | [!UICONTROL Conversion Pixels #] | Il numero di pixel di tracciamento della conversione associati al posizionamento, oppure *[!UICONTROL None]*. | — |
| [!UICONTROL Tracking] | [!UICONTROL 3rd-party fees] | Tariffa statica di terze parti da registrare come costo non fatturabile per 1000 impression, se applicabile. | — |
| [!UICONTROL Ads] | [!UICONTROL # of Ads Attached] | Il numero di annunci allegati al posizionamento, se presenti, oppure *[!UICONTROL None]*. | — |
| [!UICONTROL Ads] | [!UICONTROL Ad Names] | I nomi di tutti gli annunci allegati al posizionamento, oppure *[!UICONTROL None]*. | — |
| [!UICONTROL Ads] | [!UICONTROL Attached Ad ID] | Gli ID univoci degli annunci generati da DSP di tutti gli annunci associati al posizionamento, separati da punto e virgola. Per scaricare un elenco di nomi di annunci e degli ID di annunci associati dal [!UICONTROL Ads] creazione di una visualizzazione personalizzata che includa [!UICONTROL Ad ID] metrica e quindi [esportare i dati](/help/dsp/campaign-management/reports/campaign-export-data.md). | Sì |

### Fogli di calcolo a livello di posizionamento

| Colonna | Descrizione | Modificabile? |
|--------|-------------|-----------|
| [!UICONTROL Placement ID] | ID numerico del posizionamento. | — |
| [!UICONTROL Placement Name] | Nome del posizionamento. | Sì |
| [!UICONTROL Package Name] | Nome del pacchetto principale, se applicabile. | — |
| [!UICONTROL Start Date] | Data di inizio del posizionamento. | — |
| [!UICONTROL End Date] | Data di fine del posizionamento. | — |
| [!UICONTROL Status] | Lo stato del posizionamento: *[!UICONTROL active]* o *[!UICONTROL inactive]*. | — |
| [!UICONTROL Max Bid] | Offerta massima per il posizionamento. | Sì |
| [!UICONTROL Budget] | Il budget di posizionamento, se presente. | Sì |
| [!UICONTROL Budget Interval] | Intervallo di budget: &lt;i span=&quot;&quot; id=&quot;0&quot; translate=&quot;no&quot; />*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*, o *[!UICONTROL All Time]*.[!UICONTROL >Daily] | Sì |
| [!UICONTROL Primary Frequency Cap] | Limite di frequenza principale per il posizionamento durante il periodo specificato [!UICONTROL Primary Frequency Cap Interval]. | Sì |
| [!UICONTROL Primary Frequency Cap Interval] | Intervallo per il limite di frequenza principale: *[!UICONTROL Day]*, *[!UICONTROL Week]*, o *[!UICONTROL Month]*. | Sì |
| [!UICONTROL Secondary Frequency Cap] | Limite di frequenza secondario per il posizionamento durante il periodo specificato [!UICONTROL Secondary Frequency Cap Interval] | Sì |
| [!UICONTROL Secondary Frequency Cap Interval] | Il tipo di intervallo per l’elemento di copertura frequenza secondario: *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]*, o *[!UICONTROL Minute]*. Il numero applicabile di settimane, giorni, ore o minuti è indicato dal [!UICONTROL Secondary Frequency Cap Interval Value]. | Sì |
| [!UICONTROL Secondary Frequency Cap Interval Value] | Il numero di settimane, giorni, ore o minuti per i quali [!UICONTROL Secondary Frequency Cap] applicabile. Ad esempio, se il limite secondario è di tre impression per sei ore, il valore qui sarà `6`. | Sì |
| [!UICONTROL Attached Ad ID] | Gli ID univoci degli annunci generati da DSP di tutti gli annunci associati al posizionamento, separati da punto e virgola. Per scaricare un elenco di nomi di annunci e degli ID di annunci associati dal [!UICONTROL Ads] creazione di una visualizzazione personalizzata che includa [!UICONTROL Ad ID] metrica e quindi [esportare i dati](/help/dsp/campaign-management/reports/campaign-export-data.md). | Sì |

>[!MORELIKETHIS]
>
>* [Modifica posizionamenti](/help/dsp/campaign-management/placements/placement-edit.md)
>* [Impostazioni di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md)
