---
title: Impostazioni campagna
description: Consulta le descrizioni delle impostazioni disponibili per la campagna.
feature: DSP Campaigns
exl-id: 461c3f9e-ef69-46e7-8eb1-37ccc085ba1f
source-git-commit: d572a406be9271c6ca14d35740f04d15ddbf7364
workflow-type: tm+mt
source-wordcount: '1050'
ht-degree: 0%

---

# Impostazioni campagna

## [!UICONTROL Basic Campaign Details]

**[!UICONTROL Name]:** Il nome della campagna.

**[!UICONTROL Advertiser]:** (Sola lettura per le campagne esistenti) L’inserzionista (marchio) applicabile. Seleziona un inserzionista esistente o creane uno nuovo.

**[!UICONTROL Advertiser URL]:** Pagina ufficiale dell’inserzionista. Questo campo accelera il processo di approvazione degli annunci con i partner di magazzino.

**[!UICONTROL Timezone]:** (Sola lettura per le campagne esistenti) Il fuso orario per i rapporti e le offerte.

**[!UICONTROL Customer PO]:** (Facoltativo) Un ordine fornitore cliente per l&#39;ordine di inserimento/ordine fornitore.

**[Date campagna]:** Le date di inizio e fine della campagna.

## [!UICONTROL Campaign Goals]

**[!UICONTROL Margin Management]:** Specifica se gestire i margini per la campagna: *[!UICONTROL Yes]* o *[!UICONTROL No]* (impostazione predefinita).

Quando scegli *[!UICONTROL Yes],* specificare il tipo e l&#39;importo del margine:

* **[!UICONTROL Margin Type]:** Tipo di margine. Una volta abilitata la gestione dei margini e salvata la campagna, non puoi modificare il tipo di margine.

   * *[!UICONTROL Fixed]:* (impostazione predefinita) Consente all&#39;DSP di calcolare automaticamente e limitare la spesa in base a una percentuale di margine fissa del [!UICONTROL Gross Budget].

   * *[!UICONTROL Dynamic]:* Consente di gestire i margini fino al livello di posizionamento specificando un [!UICONTROL Budget Reserve %] e [!UICONTROL Gross Budget] per ogni pacchetto e posizionamento nella campagna. L&#39;DSP ottimizza in base all&#39;efficienza finanziaria di ogni collocamento, senza garantire un margine specifico. Utilizzare questa opzione per gli ordini di inserimento costituiti da più voci per le quali si è concordato di consegnare un importo fisso di unità o tipi di unità a un tasso fisso.

* **[!UICONTROL Fixed Margin %]:** (Solo campagne con margini fissi) Il markup predefinito per ogni ordine di inserimento <!-- impression? -->, in percentuale. Tale importo è dedotto dal [!UICONTROL Gross Budget] per definire il budget netto della campagna.

* **[!UICONTROL Budget Reserve %]:** (Solo campagne con margini fissi; facoltativo) Riserva una percentuale specificata del [!UICONTROL Gross Budget] come salvaguardia. Tale importo è dedotto dal [!UICONTROL Gross Budget] per definire il budget netto della campagna.

**[!UICONTROL Gross Budget]:** (Solo campagne con gestione dei margini) Il budget lordo della campagna, prima dell&#39;applicazione degli adeguamenti marginali specificati.

Facoltativamente, puoi aggiungere un budget lordo aggiuntivo giornaliero, settimanale o mensile:

1. Clic **[!UICONTROL Add an additional Gross Budget]**.

1. Inserisci il **[!UICONTROL Gross Budget]** e selezionare l&#39;intervallo di budget: *[!UICONTROL Daily],* *[!UICONTROL Weekly],* o *[!UICONTROL Monthly]*.

Il budget netto totale, che rappresenta il limite di spesa per la campagna, viene calcolato automaticamente in base alle impostazioni dei margini ed è indicato sotto questo valore.

**[!UICONTROL Budget]:** (Campagne senza gestione dei margini) Il budget complessivo della campagna.

**[!UICONTROL Estimated Tax Withholding]:** Trattiene una percentuale della spesa totale per le tariffe degli annunci, le tariffe di distribuzione degli annunci e/o le tariffe dei dati a livello di conto per le imposte nazionali o locali. Le aliquote sono stime per scopi di budget e di determinazione dei prezzi, pertanto le aliquote di imposta fatturate possono variare.

Per stimare le imposte da trattenere:

1. Clic **[!UICONTROL Update rates here]**.

1. Specifica la **[!UICONTROL Estimated tax rate]**, in percentuale.

1. Selezionare la casella di controllo accanto a ogni tipo di commissione per cui si desidera trattenere le imposte. I tipi di commissione includono:

   * *[!UICONTROL Include estimated tax - ads fee]:* Si applica a tutte le spese pubblicitarie dei media DSP, comprese le tasse sulle spese di gestione delle campagne.

   * *[!UICONTROL Include estimated tax - ad serving fee]:* Si applica a tutte le spese per Advertising DSP tranne che per i media e i dati. Sono escluse le tasse per le commissioni di gestione delle campagne

   * *[!UICONTROL Include estimated tax - data fee]:* Si applica a tutta la spesa di dati su Advertising DSP.

1. Clic **[!UICONTROL Submit]**.

>[!NOTE]
>
>* Negli Stati Uniti, gli stati possono variare per quanto riguarda l&#39;inclusione delle tasse tra annunci, pubblicità e dati. Per le organizzazioni in altri paesi, includere tutte e tre le categorie di imposte per contabilizzare l&#39;IVA.
>
>* Puoi anche configurare questi valori nelle impostazioni delle tariffe dell’account.<!--[fee settings](/help/dsp/admin/tax-withholdings.md). -->

**[!UICONTROL Cross Device Level]:** (Sola lettura per le campagne esistenti create dal 22 giugno 2020; non disponibile per le campagne create prima del 22 giugno 2020) Livello al quale l’DSP esegue il targeting degli annunci e applica limiti di frequenza: *Stesso dispositivo* per eseguire il targeting di un dispositivo o *Persone* per eseguire il targeting di una persona su tutti i suoi dispositivi noti. **Nota:** Il supporto tra dispositivi non è disponibile per i posizionamenti mirati agli ID universali.

**[!UICONTROL Device Graph]:** (Sola lettura per le campagne esistenti; campagne con targeting multi-dispositivo basato sulle persone) Il grafico dei dispositivi da utilizzare per il targeting multi-dispositivo e la gestione della frequenza:

* *[!UICONTROL LiveRamp - U.S. only]:* Disponibile per tutti gli inserzionisti per il targeting tra dispositivi a $ 0,35 CPM per le impression distribuite utilizzando [!DNL LiveRamp] device graph (ossia, per dispositivi non trovati all’interno dei segmenti di pubblico target). Puoi impostare il targeting tra dispositivi a livello di posizionamento.

  Questa opzione è disponibile anche per tutti gli inserzionisti, senza costi aggiuntivi, per la gestione della frequenza e la misurazione dell’attribuzione.

  Il supporto tra dispositivi si applica solo ai posizionamenti che hanno come target ID legacy ma non a quelli che hanno come target ID universali (inclusi [!DNL LiveRamps]). Il targeting, la gestione della frequenza e l’attribuzione per gli ID universali vengono applicati solo a livello di ID.

**[!UICONTROL Frequency Cap]:** (Facoltativo) Il numero di volte in cui un dispositivo univoco, un ID universale o una persona (a seconda del [!UICONTROL Cross Device Level] e del posizionamento [!UICONTROL Targeting] impostazione ) possono essere serviti annunci dalla campagna. Le opzioni includono *[!UICONTROL Unlimited]* o un importo specifico per giorno, settimana o mese.

>[!NOTE]
>
> Puoi impostare i limiti di frequenza a livello di campagna, pacchetto e posizionamento. L’DSP rispetta il limite di frequenza più severo nella gerarchia delle campagne.

**[!UICONTROL Packages]:** Il [pacchetti](/help/dsp/campaign-management/packages/package-about.md) da includere nella campagna. Seleziona i pacchetti esistenti e/o crea i pacchetti da includere. Se crei pacchetti, consulta le descrizioni di [impostazioni pacchetto](/help/dsp/campaign-management/packages/package-settings.md) per ulteriori informazioni.

## [!UICONTROL Campaign Measurement]

>[!NOTE]
>
>Le seguenti impostazioni abilitano solo le funzionalità di misurazione e reporting. L’ottimizzazione delle prestazioni viene eseguita solo a livello di pacchetto e posizionamento.

### [!UICONTROL 3rd Party Metrics]

#### [!UICONTROL Viewability, Fraud, & Brand Safety]

**[!UICONTROL IAS]:** (Facoltativo) Abilita [!DNL IAS] misurazione e reporting di visualizzabilità, frode, sicurezza del brand e verifica del pubblico, utilizzando le impostazioni specificate. Si applicano tariffe aggiuntive.

* **[!UICONTROL Measure On]:** Inventario su cui misurare: *[!UICONTROL Display and VPAID video inventory]* (impostazione predefinita) oppure *[!UICONTROL Display, VPAID & VAST video inventory]*.

  >[!NOTE]
  >
  >La visualizzabilità video è misurabile solo sull’inventario VPAID.

* **[!UICONTROL IAS Account ID (AnID)]:** (Inserzionisti con il proprio [!DNL IAS] account; facoltativo) dell&#39;organizzazione [!DNL IAS] ID account, che [!DNL IAS] verrà fatturato direttamente per l&#39;utilizzo.

* **[!UICONTROL IAS Team ID]:** (Inserzionisti con il proprio [!DNL IAS] account; facoltativo) l’ID del team dell’organizzazione [!DNL IAS] account, che [!DNL IAS] verrà fatturato direttamente per l&#39;utilizzo. <!-- verify -->

**[!UICONTROL MOAT]:** (Facoltativo) Abilita [!DNL MOAT] misurazione e reporting della visibilità, delle frodi, della sicurezza del marchio e della verifica del pubblico. Si applicano tariffe aggiuntive.

#### Verifica del pubblico

**[!UICONTROL comScore Campaign Ratings]:** (Facoltativo) Abilita [!DNL Comscore] convalidato [!DNL Campaign Ratings] misurazione e reporting della verifica del pubblico, utilizzando le impostazioni specificate. Si applicano tariffe aggiuntive.

* **[!UICONTROL Target Gender]:** Genere di destinazione: *[!UICONTROL Both]* (impostazione predefinita), *[!UICONTROL Male]*, o *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** L’intervallo di età di destinazione. Utilizza i cursori sinistro e destro per ridurre l’intervallo in base alle esigenze.

* **[!UICONTROL Target Country]:** (Facoltativo) Paese di destinazione. [!DNL Comscore] le impression relative alle misure sono servite solo nei paesi supportati.

### [!UICONTROL Attention Measurement]{#attention-measurement}

**[!UICONTROL Adelaide]:** Abilita il tracciamento per il livello di posizionamento [!UICONTROL Attention Score] metrica (il numero medio ponderato di [!DNL Adelaide] &quot;[!DNL Attention Units]&quot; tra le impression). Le metriche sono disponibili per tutti i tipi di posizionamento ad eccezione di [!DNL Roku] TV collegata, pre-roll solo VPAID e audio che non è un podcast. l’DSP associa automaticamente un tag JavaScript a tutti i creativi associati; e [!DNL Adelaide] tiene traccia dei dati di esposizione e li invia quotidianamente all’DSP. Puoi utilizzare la data per ottimizzare manualmente la spesa per le tattiche di posizionamento con punteggi di attenzione migliori.

Il [!UICONTROL Attention Score] è disponibile nel [!UICONTROL Metrics] sezione dei rapporti; all&#39;interno della sezione [!UICONTROL Campaigns], [!UICONTROL Packages], e [!UICONTROL Placements] visualizzazioni; e [!UICONTROL Sites], [!UICONTROL Ads], e [!UICONTROL Inventory] schede di [visualizzazione dettagli posizionamento](/help/dsp/campaign-management/reports/placement-details-view.md).

Utilizzo di [!DNL Adelaide] i segmenti per la misurazione sono soggetti a una tariffa CPM per ogni impression distribuita dagli annunci con [!DNL Adelaide] tag di misurazione. Questa tariffa è separata dalle tariffe per [targeting dell’attenzione a livello di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md).

<!--
Example JavaScript tag:

`<script src="https://www.example.com/aam?asid=0123456789&ad=${TM_AD_ID_NUM}&adv=${TM_ADVERTISER_ID}&ca=${TM_CAMPAIGN_ID_NUM}&df=${NS_PLATFORM_ID}&dt=${NS_DEVICE_GROUPING}&pl=${TM_PLACEMENT_ID_NUM}&ra=${TM_RANDOM}&st=${TM_SITE_URL_URLENC}"></script>`
-->

### [!UICONTROL 1st Party Metrics]

**[!UICONTROL Viewability sensitivity]:** Consente la misurazione di prime parti e il reporting della visualizzabilità utilizzando [!DNL IAB Open Video Viewability (OpenVV)] tecnologia, in base al livello di sensibilità specificato:

* *[!UICONTROL Standard (50% of ad in view for two consecutive seconds)]*

* *[!UICONTROL Strict (100% of ad in view and audio on for 50% duration)]*

>[!MORELIKETHIS]
>
>* [Informazioni su Campaign Management](campaign-about.md)
>* [Creare una campagna](campaign-create.md)
>* [Modificare una campagna](campaign-edit.md)
>* [Visualizzare il registro delle modifiche per una campagna](campaign-change-log.md)
