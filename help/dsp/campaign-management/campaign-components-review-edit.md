---
title: Rivedere e modificare le impostazioni dei componenti di Campaign utilizzando i bulksheet
description: Scopri come rivedere e modificare in blocco le impostazioni del pacchetto chiave, del posizionamento e degli annunci utilizzando i fogli di calcolo.
feature: DSP Placements
source-git-commit: fa4cee46135c85849daa7faa4059c77fc753c2c8
workflow-type: tm+mt
source-wordcount: '1349'
ht-degree: 0%

---

# Rivedere e modificare le impostazioni dei componenti di Campaign utilizzando i bulksheet

<!-- Update headers as needed once the original download become editable and we call everything bulksheets. -->

È possibile scaricare le impostazioni per pacchetti, posizionamenti e annunci in una singola campagna in formato XLSX ([!DNL Microsoft Excel] foglio di calcolo) per la revisione. Per impostazione predefinita, il file scaricato include schede separate per le impostazioni del pacchetto, le informazioni sul volo del pacchetto, le impostazioni di posizionamento e le pianificazioni degli annunci di posizionamento. Facoltativamente, puoi escludere le impostazioni per alcuni tipi di componenti della campagna.

Per aggiornare più impostazioni contemporaneamente, carica un file bulksheet valido con le modifiche. Per creare il bulksheet, puoi scaricare un modello di bulksheet vuoto che include schede per ciascun tipo di componente della campagna, inserire o incollare impostazioni nuove o aggiornate nel file modello, quindi salvare il file per caricarlo. I campi modificabili includono la maggior parte delle impostazioni normalmente modificabili.

>[!NOTE]
>
>Puoi anche scaricare e modificare le impostazioni solo per pacchetti e posizionamenti specifici. Consulta &quot;[Rivedere e modificare le impostazioni dei pacchetti utilizzando i bulksheet](/help/dsp/campaign-management/packages/package-qa.md)&quot; e &quot;[Rivedere e modificare le impostazioni di posizionamento utilizzando i bulksheet](/help/dsp/campaign-management/placements/placement-qa.md).&quot;

## Scaricare le impostazioni per pacchetti, posizionamenti e annunci in una campagna

1. Nel menu principale, fare clic su **[!UICONTROL Campaigns]**.

1. In alto a destra, fare clic su **[!UICONTROL ...]** > **[!UICONTROL Download QA sheet]**.

1. Nella finestra di dialogo [!UICONTROL QA Sheet Download] deselezionare i componenti di Campaign di cui si desidera escludere le impostazioni dal file scaricato e quindi fare clic su **[!UICONTROL Download]**.

Per impostazione predefinita, sono selezionate le impostazioni per tutti i componenti della campagna.

Un messaggio di notifica indica quando il file è disponibile per il download.

1. Per scaricare il file, effettuare una delle seguenti operazioni:

   * Nel messaggio di notifica, fare clic su **[!UICONTROL Download].**

   * Nella parte destra della barra dei menu superiore, fai clic su ![Processi](/help/dsp/assets/downloads.png). Fare clic su **[!UICONTROL Download]** accanto al processo.

     Il file viene salvato nella cartella Download del browser. Per un elenco delle colonne incluse, vedere &quot;[Colonne di posizionamento nei fogli di calcolo scaricati/caricati](#qa-sheet-columns)&quot;.

>[!NOTE]
>
>Non puoi modificare e ricaricare i file di controllo qualità a livello di campagna. Per apportare modifiche alle impostazioni del componente Campaign in questi file, [scarica un file modello impostazioni separato (file di installazione)](#download-template), immetti o incolla righe dal file di controllo qualità nel modello e salva il file, quindi [carica il file modello popolato](#upload-bulksheet-campaign-components).

## Scaricare un modello di bulksheet per una campagna {#download-template}

Scarica un modello bulksheet vuoto che include schede per ogni tipo di componente della campagna. In seguito puoi aggiungere righe a qualsiasi scheda del modello e [caricare il file modificato](##upload-bulksheet-campaign-components) per apportare modifiche ai componenti della campagna.

1. Fai clic sul nome della campagna.

1. In alto a destra, fare clic su **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**.

1. Nella finestra di dialogo [!UICONTROL Upload Bulksheet], fare clic su **[!UICONTROL Bulksheet Template].**

   Il file viene salvato nella cartella Download del browser. Per un elenco delle colonne incluse, vedere &quot;[Colonne di posizionamento nei fogli di calcolo scaricati/caricati](#qa-sheet-columns)&quot;.

## Caricare un bulksheet con le impostazioni per pacchetti, posizionamenti e annunci per una campagna{#upload-bulksheet-campaign-components}

Carica le impostazioni per pacchetti, posizionamenti e annunci in una singola campagna contemporaneamente in un bulksheet popolato.

1. [Scaricare un modello di bulksheet](#download-template) se necessario, immettere o incollare le impostazioni relative a pacchetti, posizionamento e/o annunci nelle schede pertinenti di un modello di bulksheet, quindi salvare il file nel dispositivo o nella rete.

   Consulta le impostazioni disponibili di seguito.

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

>[!MORELIKETHIS]
>
>* [Verifica e modifica impostazioni pacchetto tramite bulksheet](/help/dsp/campaign-management/packages/package-qa.md)
>* [Rivedi e modifica le impostazioni di posizionamento utilizzando i bulksheet](/help/dsp/campaign-management/placements/placement-qa.md)
