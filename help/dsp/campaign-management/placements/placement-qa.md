---
title: Revisione e modifica delle impostazioni di posizionamento tramite i bulksheet
description: Scopri come rivedere e modificare le impostazioni di posizionamento chiave in blocco utilizzando i fogli di calcolo.
feature: DSP Placements
exl-id: 2de4407d-eb3b-44ff-893c-9fdf6921d4b3
source-git-commit: 8f4e694885919a8dcf7895c2f8d8aeb11249e03c
workflow-type: tm+mt
source-wordcount: '1457'
ht-degree: 0%

---

# Revisione e modifica delle impostazioni di posizionamento tramite i bulksheet

È possibile scaricare le impostazioni per uno o più posizionamenti o per tutti i posizionamenti in una campagna in formato XLSX ([!DNL Microsoft Excel] foglio di calcolo) per la revisione. Utilizza questa funzione per rivedere rapidamente dettagli quali:

* Quali tipi di pubblico sono target della campagna.
* Quando i posizionamenti iniziano a consegnare e quando terminano.
* Quali annunci vengono allegati ai posizionamenti.

Per aggiornare più impostazioni contemporaneamente, è possibile effettuare una delle seguenti operazioni:

* Apporta le modifiche necessarie per selezionare i campi, salvare il file e caricare nuovamente il file di bulksheet modificato in DSP.

* Per apportare modifiche ai posizionamenti aggiuntivi e alle impostazioni di qualsiasi pacchetto, scarica un modello di bulksheet vuoto che includa schede per ogni tipo di componente della campagna, immetti o incolla le impostazioni nuove o aggiornate nel file modello, quindi carica il file per apportare le modifiche. Per istruzioni, consulta &quot;[Rivedere e modificare le impostazioni dei componenti di Campaign utilizzando i bulksheet](/help/dsp/campaign-management/campaign-components-review-edit.md).&quot;

I campi modificabili includono nomi di posizionamento, stati, offerte, budget, strategie di velocità e limiti di frequenza.

>[!TIP]
>
>Per modificare rapidamente più campi per uno o più posizionamenti, vedi &quot;[Modifica posizionamenti](/help/dsp/campaign-management/placements/placement-edit.md)&quot;.

## Scaricare le impostazioni per tutti i posizionamenti in una campagna

1. Nel menu principale, fare clic su **[!UICONTROL Campaigns]**.

1. In alto a destra, fare clic su **[!UICONTROL ...]** > **[!UICONTROL Download Setup Excel]**.

   Un messaggio di notifica indica quando il file è disponibile per il download.

1. Per scaricare il file, effettuare una delle seguenti operazioni:

   * Nel messaggio di notifica, fare clic su **[!UICONTROL Download].**

   * Nella parte destra della barra dei menu superiore, fai clic su ![Processi](/help/dsp/assets/downloads.png). Fare clic su **[!UICONTROL Download]** accanto al processo.

   Il file viene salvato nella cartella Download del browser. Per un elenco delle colonne incluse, vedere &quot;[Colonne di posizionamento nei fogli di calcolo scaricati/caricati](#qa-sheet-columns)&quot;.

## Scarica impostazioni per uno o più posizionamenti

1. Nel menu principale, fare clic su **[!UICONTROL Campaigns]**.

1. Fai clic sul nome della campagna.

1. Nel sottomenu fare clic su **[!UICONTROL Placements]**.

1. Seleziona la casella di controllo accanto a ciascun posizionamento di cui desideri scaricare le impostazioni.

1. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**.

   Un messaggio di notifica indica quando il file bulksheet è disponibile per il download.

1. Per scaricare il bulksheet, effettuare una delle seguenti operazioni:

   * Nel messaggio di notifica, fare clic su **[!UICONTROL Download].**

   * Nella parte destra della barra dei menu superiore, fai clic su ![Processi](/help/dsp/assets/downloads.png). Fare clic su **[!UICONTROL Download]** accanto al processo.

   Il file viene salvato nella cartella Download del browser. Per un elenco delle colonne incluse, vedere &quot;[Colonne di posizionamento nei fogli di calcolo scaricati/caricati](#qa-sheet-columns)&quot;.


<!-- I don't think I need this here

## Download a Bulksheet Template {#download-template}

Download a blank bulksheet template that includes tabs for each type of campaign component. You can later add rows to any tab on the template and [upload the edited file](##upload-bulksheet-package) to make changes. 

1. Click the name of the campaign.

1.  In the upper right, click **[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**.

   The file is saved to the browser's Downloads folder. See "[Placement Columns in Downloaded/Uploaded Spreadsheets](#qa-sheet-columns)" for a list of the included columns.

-->

## Caricare un bulksheet con le impostazioni di posizionamento {#upload-bulksheet-placement}

Puoi caricare le impostazioni per i posizionamenti e per gli annunci e i pacchetti associati ai posizionamenti in un file bulksheet.

1. Nel menu principale, fare clic su **[!UICONTROL Campaigns]**.

1. Fai clic sul nome della campagna.

1. In alto a destra, fare clic su **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**.

1. Nella finestra di dialogo [!UICONTROL Upload Bulksheet]:

   1. Trascinare e rilasciare un file nella casella oppure fare clic all&#39;interno della casella per selezionare un file dal dispositivo o dalla rete.

   1. Fare clic su **[!UICONTROL Upload]**.

1. (Facoltativo) Per verificare che gli aggiornamenti siano stati elaborati, fai clic su ![Processi](/help/dsp/assets/downloads.png) a destra della barra dei menu superiore.

## Colonne delle impostazioni di posizionamento nei fogli di calcolo scaricati/caricati{#qa-sheet-columns}

>[!TIP]
>
> In un foglio di calcolo scaricato, tutte le colonne modificabili sono evidenziate in blu.

### Fogli di calcolo a livello di campagna

<!-- 
Check on Brand Safety - Contextual Filtering # with new DV feature/fct change.
-->

| Sezione | Colonna | Descrizione | Modificabile? |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic] | [!UICONTROL Placement ID] | ID numerico del posizionamento. | — |
| [!UICONTROL Basic] | [!UICONTROL Placement Name] | Nome del posizionamento. | Sì |
| [!UICONTROL Basic] | [!UICONTROL Labels] | Eventuali etichette applicate, per la generazione di rapporti. | — |
| [!UICONTROL Basic] | [!UICONTROL Edit Link] | Un collegamento per aprire il posizionamento in modalità Modifica. | — |
| [!UICONTROL Basic] | [!UICONTROL Status] | Stato del posizionamento: *[!UICONTROL active]* o *[!UICONTROL inactive]*. | Sì |
| [!UICONTROL Basic] | [!UICONTROL Placement Type] | Il tipo di posizionamento. | — |
| [!UICONTROL Basic] | [!UICONTROL Package Name] | Nome del pacchetto principale, se applicabile. | — |
| [!UICONTROL Goals] | [!UICONTROL Start Date] | Data di inizio del posizionamento. | — |
| [!UICONTROL Goals] | [!UICONTROL End Date] | Data di fine del posizionamento. | — |
| [!UICONTROL Goals] | [!UICONTROL Day parting] | Indica se dayparting è *[!UICONTROL ON]* o *[!UICONTROL OFF]*.<br><b>Nota:</b> Per verificare la pianificazione effettiva di dayparting, aprire le impostazioni di posizionamento in DSP. | — |
| [!UICONTROL Goals] | [!UICONTROL Budget] | Il budget di posizionamento, se presente. | Sì |
| [!UICONTROL Goals] | [!UICONTROL Budget Interval] | Intervallo di budget: &lt;i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]* o *[!UICONTROL All Time]*. | Sì |
| [!UICONTROL Goals] | [!UICONTROL Optimization Goal] | Obiettivo del pacchetto. | — |
| [!UICONTROL Goals] | [!UICONTROL Optimization Target] | Il valore target dell’obiettivo. | — |
| [!UICONTROL Goals] | [!UICONTROL Pace on] | Indica se il posizionamento sta avanzando verso *[!UICONTROL Budget]* o *[!UICONTROL Impressions]*. | — |
| [!UICONTROL Goals] | [!UICONTROL Max Bid] | Offerta massima per il posizionamento. | Sì |
| [!UICONTROL Goals] | [!UICONTROL Flight Pacing] | Strategia di andamento del volo per il posizionamento: *[!UICONTROL Even]*, *[!UICONTROL slightly ahead]*, *[!UICONTROL frontload]* o *[!UICONTROL aggressive frontload]*. | Sì |
| [!UICONTROL Goals] | [!UICONTROL Intraday Pacing] | Strategia di velocità infragiornaliera per il posizionamento: *[!UICONTROL Even]* o *[!UICONTROL ASAP]*. | Sì |
| [!UICONTROL Goals] | [!UICONTROL Pre-Bid Filters] | Eventuali criteri di filtro pre-offerta da applicare. | — |
| [!UICONTROL Goals] | [!UICONTROL Bidding Rules] | Indica se le regole di offerta (obsolete) sono *[!UICONTROL ON]* o *[!UICONTROL OFF]*. | — |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap] | Il limite di frequenza principale per il posizionamento durante il [!UICONTROL Frequency Cap Interval] specificato. | Sì |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap Interval] | Intervallo per il limite di frequenza primario: *[!UICONTROL Day]*, *[!UICONTROL Week]* o *[!UICONTROL Month]*. | Sì |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap] | Limite di frequenza secondario per il posizionamento durante [!UICONTROL Secondary Frequency Cap Interval] specificato | Sì |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval] | Tipo di intervallo per il limite di frequenza secondario: *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]* o *[!UICONTROL Minute]*. Il numero applicabile di settimane, giorni, ore o minuti è indicato da [!UICONTROL Secondary Frequency Cap Interval Value]. | Sì |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval Value] | Il numero di settimane, giorni, ore o minuti a cui si applica [!UICONTROL Secondary Frequency Cap]. Ad esempio, se il limite secondario è di tre impression per sei ore, il valore qui sarà `6`. | Sì |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included #] | Il numero di posizioni geografiche di destinazione, *[!UICONTROL All]* o *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included] | Le posizioni geografiche di destinazione, separate da punti e virgola, o *[!UICONTROL All Locations]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded #] | Numero di posizioni geografiche escluse o *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded] | Le località geografiche escluse, separate da punti e virgola, oppure *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Included #] | Numero di offerte di inventario pubblico di destinazione, se specificate, *[!UICONTROL All]* o *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Excluded #] | Numero di offerte di inventario pubblico escluse, se specificate, oppure *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Included #] | Numero di offerte di inventario private, se specificate, *[!UICONTROL All]* o *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Excluded #] | Il numero di offerte di inventario private escluse, se specificate, o *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Included #] | Numero di [!UICONTROL On-Demand Inventory] offerte, se presenti, specificate *[!UICONTROL All]* o *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Excluded #] | Il numero di offerte di inventario su richiesta escluse, se specificate, o *[!UICONTROL None]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Traffic Type] | Tipo di traffico di destinazione: *[!UICONTROL Website]* e/o *[!UICONTROL Apps]* | — |
| [!UICONTROL Sites] | [!UICONTROL Exclude out-stream] | Indica se l&#39;opzione di targeting del magazzino per escludere il traffico in uscita è &lt;i[!UICONTROL >ON]* o *[!UICONTROL OFF]*.<br>Gli annunci in uscita vengono in genere visualizzati sopra il contenuto come popup o inseriti nel contenuto (nell&#39;esperienza nativa), anziché come normali annunci video in un lettore video. | — |
| [!UICONTROL Sites] | [!UICONTROL Site Tier] | Qualità dei siti di destinazione: *[!UICONTROL Tier 1]*, *[!UICONTROL Tier 2]*, *[!UICONTROL Tier 3]* o *[!UICONTROL All Sites]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Included #] | Il numero di categorie del sito di destinazione, se specificate, oppure *[!UICONTROL All]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Excluded #] | Il numero di categorie di sito escluse, se specificate, oppure *[!UICONTROL All]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Excluded Sites] | I siti esclusi, se presenti, sono specificati oppure *[!UICONTROL None]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Language] | Lingue del sito di destinazione. | — |
| [!UICONTROL Sites] | [!UICONTROL Allow unscreened sites] | (Solo posizionamenti di visualizzazione standard) Se consentire o meno la consegna di annunci su siti non controllati: *[!UICONTROL ON]* o *[!UICONTROL OFF]*. Quando il posizionamento ha come target l’inventario privato, questa opzione può distribuire annunci sui siti bloccati. | — |
| [!UICONTROL Sites] | [!UICONTROL Targeted Sites] | Il numero di siti di destinazione, se specificati, o *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Included] | I tipi di pubblico di destinazione, se presenti, oppure *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Excluded] | Sono specificati i tipi di pubblico esclusi, se presenti, oppure *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Demographic booster] | Indica se [!DNL Comscore] segmenti demografici sono abilitati o meno per il posizionamento (e altri posizionamenti nella campagna): *[!UICONTROL ON]* o *[!UICONTROL OFF]*. Questa funzionalità può essere abilitata solo per le campagne per le quali la funzionalità [!DNL Audience Verification] è abilitata per [!DNL Nielsen] e/o [!DNL Comscore].  Esso è soggetto a spese supplementari. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Extend across screens] | Se estendere o meno il targeting dell&#39;annuncio tra i dispositivi: *[!UICONTROL ON]* o *[!UICONTROL OFF]*. Il targeting tra dispositivi estende il targeting su tutti i dispositivi noti di una persona, in base al grafico dei dispositivi specificato nelle impostazioni della campagna. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting] - N. incluso | Numero di codici argomento di destinazione, se presenti, oppure *[!UICONTROL All]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting - Excluded #] | Numero di codici argomento esclusi, se presenti, oppure *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Included #] | Il numero di destinazioni dispositivo di destinazione, se specificate, o *[!UICONTROL All]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Excluded #] | Numero di destinazioni dispositivo escluse, se specificate, oppure *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Included #] | Numero di provider ISP di destinazione, se specificati, oppure *[!UICONTROL All]/i>. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Excluded #] | Numero di provider ISP esclusi, se specificati, oppure *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Contextual Filtering #] | Numero di filtri di sicurezza del brand applicati, se presenti, oppure *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Fraud blocking #] | Numero di filtri di blocco delle frodi pre-offerta applicati, se presenti, oppure *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Viewability #] | Numero di filtri di visibilità pre-offerta applicati, se presenti, oppure *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Site Safety Block] | Indica se il blocco di sicurezza del sito è abilitato o meno: *[!UICONTROL ON]* o *[!UICONTROL OFF]*.<!-- Whether or not the advertiser-level setting Enable Site Safety Block is enabled: *ON* or *OFF*.I don’t see this option at the placement level. Should there be one? --> | — |
| [!UICONTROL Tracking] | [!UICONTROL Tracking Pixels #] | Il numero di pixel di terze parti per il tracciamento degli eventi associati al posizionamento o *[!UICONTROL None]*. | — |
| [!UICONTROL Tracking] | [!UICONTROL Conversion Pixels #] | Il numero di pixel di tracciamento della conversione associati al posizionamento, o *[!UICONTROL None]*. | — |
| [!UICONTROL Tracking] | [!UICONTROL 3rd-party fees] | Tariffa statica di terze parti da registrare come costo non fatturabile per 1000 impression, se applicabile. | — |
| [!UICONTROL Ads] | [!UICONTROL # of Ads Attached] | Il numero di annunci allegati al posizionamento, se presenti, o *[!UICONTROL None]*. | — |
| [!UICONTROL Ads] | [!UICONTROL Ad Names] | I nomi degli annunci allegati al posizionamento o *[!UICONTROL None]*. | — |
| [!UICONTROL Ads] | [!UICONTROL Attached Ad ID] | Gli ID univoci degli annunci generati da DSP di tutti gli annunci associati al posizionamento, separati da punto e virgola. Per scaricare un elenco di nomi di annunci e ID di annunci associati dalla visualizzazione [!UICONTROL Ads], crea una visualizzazione personalizzata che includa la metrica [!UICONTROL Ad ID], quindi [esporta i dati](/help/dsp/campaign-management/reports/campaign-export-data.md). | Sì |

### Bulksheet a livello di posizionamento

| Colonna | Descrizione | Modificabile? |
|--------|-------------|-----------|
| [!UICONTROL Placement ID] | ID numerico del posizionamento. | — |
| [!UICONTROL Placement Name] | Nome del posizionamento. | Sì |
| [!UICONTROL Package Name] | Nome del pacchetto principale, se applicabile. | — |
| [!UICONTROL Start Date] | Data di inizio del posizionamento. | — |
| [!UICONTROL End Date] | Data di fine del posizionamento. | — |
| [!UICONTROL Status] | Stato del posizionamento: *[!UICONTROL active]* o *[!UICONTROL inactive]*. | — |
| [!UICONTROL Max Bid] | Offerta massima per il posizionamento. | Sì |
| [!UICONTROL Budget] | Il budget di posizionamento, se presente. | Sì |
| [!UICONTROL Budget Interval] | Intervallo di budget: &lt;i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]* o *[!UICONTROL All Time]*. | Sì |
| [!UICONTROL Primary Frequency Cap] | Il limite di frequenza principale per il posizionamento durante il [!UICONTROL Primary Frequency Cap Interval] specificato. | Sì |
| [!UICONTROL Primary Frequency Cap Interval] | Intervallo per il limite di frequenza primario: *[!UICONTROL Day]*, *[!UICONTROL Week]* o *[!UICONTROL Month]*. | Sì |
| [!UICONTROL Secondary Frequency Cap] | Limite di frequenza secondario per il posizionamento durante [!UICONTROL Secondary Frequency Cap Interval] specificato | Sì |
| [!UICONTROL Secondary Frequency Cap Interval] | Tipo di intervallo per il limite di frequenza secondario: *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]* o *[!UICONTROL Minute]*. Il numero applicabile di settimane, giorni, ore o minuti è indicato da [!UICONTROL Secondary Frequency Cap Interval Value]. | Sì |
| [!UICONTROL Secondary Frequency Cap Interval Value] | Il numero di settimane, giorni, ore o minuti a cui si applica [!UICONTROL Secondary Frequency Cap]. Ad esempio, se il limite secondario è di tre impression per sei ore, il valore qui sarà `6`. | Sì |
| [!UICONTROL Attached Ad ID] | Gli ID univoci degli annunci generati da DSP di tutti gli annunci associati al posizionamento, separati da punto e virgola. Per scaricare un elenco di nomi di annunci e ID di annunci associati dalla visualizzazione [!UICONTROL Ads], crea una visualizzazione personalizzata che includa la metrica [!UICONTROL Ad ID], quindi [esporta i dati](/help/dsp/campaign-management/reports/campaign-export-data.md). | Sì |


<!-- LOTS MORE THAN I HAD ORIGINALLY DOCUMENTED -- BELOW ARE THE LAST, BUT NOT ALL:

Brand Safety - Contextual Filtering #								"		

| Brand Safety | Brand Safety - Contextual Filtering # |  |  |
| Brand Safety | Brand Safety - Pre-Bid Fraud blocking # |  |  |
| Brand Safety | Brand Safety - Pre-Bid Viewability # |  |  |
| Brand Safety | Site Safety Block |  |  |
| Tracking | Tracking Pixels # |  |  |
| Tracking | Conversion Pixels # |  |  |
| Tracking | 3rd-party fees |  |  |
| # of Ads Attached |  |  |
| Ads |  Ad Names |  |  |
| Ads | Attached Ad ID |  |  |
| Environment | Environment |  |  |
-->


>[!MORELIKETHIS]
>
>* [Verifica e modifica le impostazioni dei componenti della campagna tramite bulksheet](/help/dsp/campaign-management/campaign-components-review-edit.md)
>* [Modifica posizionamenti](/help/dsp/campaign-management/placements/placement-edit.md)
>* [Impostazioni posizionamento](/help/dsp/campaign-management/placements/placement-settings.md)
