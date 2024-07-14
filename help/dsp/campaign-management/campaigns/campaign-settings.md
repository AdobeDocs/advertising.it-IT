---
title: Impostazioni campagna
description: Consulta le descrizioni delle impostazioni disponibili per la campagna.
feature: DSP Campaigns
exl-id: 461c3f9e-ef69-46e7-8eb1-37ccc085ba1f
source-git-commit: 0fbdc7e38026d71483c2de1406a4110066690130
workflow-type: tm+mt
source-wordcount: '1064'
ht-degree: 0%

---

# Impostazioni campagna

## [!UICONTROL Basic Campaign Details]

**[!UICONTROL Name]:** Il nome della campagna.

**[!UICONTROL Advertiser]:** (sola lettura per campagne esistenti) L&#39;inserzionista (marchio) applicabile. Seleziona un inserzionista esistente o creane uno nuovo.

**[!UICONTROL Advertiser URL]:** Pagina ufficiale dell&#39;inserzionista. Questo campo accelera il processo di approvazione degli annunci con i partner di magazzino.

**[!UICONTROL Timezone]:** (sola lettura per le campagne esistenti) Il fuso orario per la creazione di rapporti e offerte.

**[!UICONTROL Customer PO]:** (facoltativo) ordine di acquisto cliente per l&#39;ordine di inserimento/ordine di acquisto.

**[Date campagna]:** Le date di inizio e di fine della campagna.

## [!UICONTROL Campaign Goals]

**[!UICONTROL Margin Management]:** Se gestire i margini per la campagna: *[!UICONTROL Yes]* o *[!UICONTROL No]* (impostazione predefinita).

Quando scegli *[!UICONTROL Yes],* specifica il tipo di margine e l&#39;importo:

* **[!UICONTROL Margin Type]:** Il tipo di margine. Una volta abilitata la gestione dei margini e salvata la campagna, non puoi modificare il tipo di margine.

   * *[!UICONTROL Fixed]:* (impostazione predefinita) Consente all&#39;DSP di calcolare automaticamente e limitare la spesa in base a una percentuale di margine fissa di [!UICONTROL Gross Budget].

   * *[!UICONTROL Dynamic]:* Consente di gestire i margini al livello di posizionamento specificando [!UICONTROL Budget Reserve %] e [!UICONTROL Gross Budget] separati per ciascun pacchetto e posizionamento nella campagna. L&#39;DSP ottimizza in base all&#39;efficienza finanziaria di ogni collocamento, senza garantire un margine specifico. Utilizzare questa opzione per gli ordini di inserimento costituiti da più voci per le quali si è concordato di consegnare un importo fisso di unità o tipi di unità a un tasso fisso.

* **[!UICONTROL Fixed Margin %]:** (solo campagne con margini fissi) Markup predefinito per ogni ordine di inserimento <!-- impression? -->, in percentuale. Questo importo viene dedotto da [!UICONTROL Gross Budget] per definire il budget netto della campagna.

* **[!UICONTROL Budget Reserve %]:** (solo campagne con margini fissi; facoltativo) riserva una percentuale specificata di [!UICONTROL Gross Budget] come misura di salvaguardia. Questo importo viene dedotto da [!UICONTROL Gross Budget] per definire il budget netto della campagna.

**[!UICONTROL Gross Budget]:** (solo campagne con gestione dei margini) Il budget lordo della campagna, prima dell&#39;applicazione degli adeguamenti marginali specificati.

Facoltativamente, puoi aggiungere un budget lordo aggiuntivo giornaliero, settimanale o mensile:

1. Fare clic su **[!UICONTROL Add an additional Gross Budget]**.

1. Immettere **[!UICONTROL Gross Budget]** e selezionare l&#39;intervallo di budget: *[!UICONTROL Daily],* *[!UICONTROL Weekly],* o *[!UICONTROL Monthly]*.

Il budget netto totale, che rappresenta il limite di spesa per la campagna, viene calcolato automaticamente in base alle impostazioni dei margini ed è indicato sotto questo valore.

**[!UICONTROL Budget]:** (campagne senza gestione dei margini) Il budget complessivo della campagna.

**[!UICONTROL Estimated Tax Withholding]:** trattiene una percentuale della spesa totale per le tariffe degli annunci, le tariffe di distribuzione degli annunci e/o le tariffe dei dati a livello di account per le imposte nazionali o locali. Le aliquote sono stime per scopi di budget e di determinazione dei prezzi, pertanto le aliquote di imposta fatturate possono variare.

Per stimare le imposte da trattenere:

1. Fare clic su **[!UICONTROL Update rates here]**.

1. Specificare **[!UICONTROL Estimated tax rate]** come percentuale.

1. Selezionare la casella di controllo accanto a ogni tipo di commissione per cui si desidera trattenere le imposte. I tipi di commissione includono:

   * *[!UICONTROL Include estimated tax - ads fee]:* Si applica a tutte le spese dei supporti Advertising DSP, incluse le imposte sulle spese di gestione delle campagne.

   * *[!UICONTROL Include estimated tax - ad serving fee]:* Si applica a tutte le spese in Advertising DSP ad eccezione di file multimediali e dati. Sono escluse le tasse per le commissioni di gestione delle campagne

   * *[!UICONTROL Include estimated tax - data fee]:* Si applica a tutte le spese di dati in Advertising DSP.

1. Fare clic su **[!UICONTROL Submit]**.

>[!NOTE]
>
>* Negli Stati Uniti, gli stati possono variare per quanto riguarda l&#39;inclusione delle tasse tra annunci, pubblicità e dati. Per le organizzazioni in altri paesi, includere tutte e tre le categorie di imposte per contabilizzare l&#39;IVA.
>
>* È inoltre possibile configurare questi valori nelle impostazioni relative alle tariffe dell&#39;account.<!--[fee settings](/help/dsp/admin/tax-withholdings.md). -->

**[!UICONTROL Cross Device Level]:** (Sola lettura per le campagne esistenti create dal 22 giugno 2020; non disponibile per le campagne create prima del 22 giugno 2020) Livello al quale l&#39;DSP esegue il targeting degli annunci e applica limiti di frequenza: *Stesso dispositivo* per eseguire il targeting di un dispositivo o *Persone* per eseguire il targeting di una persona su tutti i dispositivi noti. **Nota:** il supporto tra dispositivi non è disponibile per i posizionamenti che hanno come destinazione gli ID universali.

**[!UICONTROL Device Graph]:** (sola lettura per campagne esistenti; campagne con targeting multidispositivo basato sulle persone) Il grafico dei dispositivi da utilizzare per il targeting multidispositivo e la gestione della frequenza:

* *[!UICONTROL LiveRamp - U.S. only]:* Disponibile per tutti gli inserzionisti per il targeting multidispositivo a $ 0,35 CPM per le impression distribuite tramite il grafico dei dispositivi [!DNL LiveRamp] (ovvero, per i dispositivi non trovati all&#39;interno dei segmenti di pubblico di destinazione). Puoi impostare il targeting tra dispositivi a livello di posizionamento.

  Questa opzione è disponibile anche per tutti gli inserzionisti, senza costi aggiuntivi, per la gestione della frequenza e la misurazione dell’attribuzione.

  Il supporto tra dispositivi si applica solo ai posizionamenti che hanno come destinazione ID legacy ma non a quelli che hanno come destinazione ID universali (inclusi [!DNL LiveRamps]). Il targeting, la gestione della frequenza e l’attribuzione per gli ID universali vengono applicati solo a livello di ID.

**[!UICONTROL Frequency Cap]:** (Facoltativo) Il numero di volte in cui un dispositivo univoco, un ID universale o una persona (a seconda di [!UICONTROL Cross Device Level] specificato e dell&#39;impostazione [!UICONTROL Targeting] del posizionamento) possono essere serviti dagli annunci dalla campagna. Le opzioni includono *[!UICONTROL Unlimited]* o un importo specifico per giorno, settimana o mese.

>[!NOTE]
>
> Puoi impostare i limiti di frequenza a livello di campagna, pacchetto e posizionamento. L’DSP rispetta il limite di frequenza più severo nella gerarchia delle campagne.

**[!UICONTROL Packages]:** i [pacchetti](/help/dsp/campaign-management/packages/package-about.md) da includere nella campagna. Seleziona i pacchetti esistenti e/o crea i pacchetti da includere. Se si creano pacchetti, vedere le descrizioni relative alle [impostazioni del pacchetto](/help/dsp/campaign-management/packages/package-settings.md) per ulteriori informazioni.

## [!UICONTROL Campaign Measurement]

>[!NOTE]
>
>Le seguenti impostazioni abilitano solo le funzionalità di misurazione e reporting. L’ottimizzazione delle prestazioni viene eseguita solo a livello di pacchetto e posizionamento.

### [!UICONTROL 3rd Party Metrics]

#### [!UICONTROL Viewability, Fraud, & Brand Safety]

**[!UICONTROL IAS]:** (facoltativo) abilita la misurazione e la generazione di rapporti [!DNL IAS] di visualizzabilità, frode, sicurezza del marchio e verifica del pubblico, utilizzando le impostazioni specificate. Si applicano tariffe aggiuntive.

* **[!UICONTROL Measure On]:** Inventario su cui misurare: *[!UICONTROL Display and VPAID video inventory]* (impostazione predefinita) o *[!UICONTROL Display, VPAID & VAST video inventory]*.

  >[!NOTE]
  >
  >La visualizzabilità video è misurabile solo sull’inventario VPAID.

* **[!UICONTROL IAS Account ID (AnID)]:** (inserzionisti con i propri account [!DNL IAS]; facoltativo) l&#39;ID account [!DNL IAS] dell&#39;organizzazione, che [!DNL IAS] fatturerà direttamente per l&#39;utilizzo.

* **[!UICONTROL IAS Team ID]:** (inserzionisti con i propri account [!DNL IAS]; facoltativo) ID team per l&#39;account [!DNL IAS] dell&#39;organizzazione, che [!DNL IAS] fatturerà direttamente per l&#39;utilizzo. <!-- verify -->

**[!UICONTROL MOAT]:** (facoltativo) abilita la misurazione e il reporting di [!DNL MOAT] in termini di visualizzabilità, frode, sicurezza del marchio e verifica del pubblico. Si applicano tariffe aggiuntive. **Nota:** [!DNL Oracle] cesserà l&#39;attività pubblicitaria entro il 30 settembre 2024, inclusi tutti i servizi di [!DNL MOAT].

#### Verifica del pubblico

**[!UICONTROL Comscore Campaign Ratings]:** (Facoltativo) Abilita la misurazione [!DNL Campaign Ratings] convalidata [!DNL Comscore] e il reporting della verifica del pubblico, utilizzando le impostazioni specificate. Si applicano tariffe aggiuntive.

* **[!UICONTROL Target Gender]:** Il genere di destinazione: *[!UICONTROL Both]* (impostazione predefinita), *[!UICONTROL Male]* o *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** L&#39;intervallo di età di destinazione. Utilizza i cursori sinistro e destro per ridurre l’intervallo in base alle esigenze.

* **[!UICONTROL Target Country]:** (Facoltativo) Un paese di destinazione. [!DNL Comscore] misure impression fornite solo nei paesi supportati.

### [!UICONTROL Attention Measurement]{#attention-measurement}

**[!UICONTROL Adelaide]:** Abilita il tracciamento per la metrica [!UICONTROL Attention Score] a livello di posizionamento (la media ponderata del numero di [!DNL Adelaide] &quot;[!DNL Attention Units]&quot; tra le impression). Le metriche sono disponibili per tutti i tipi di posizionamento ad eccezione di [!DNL Roku] TV connessa, pre-roll solo VPAID e audio che non è un podcast. L&#39;DSP associa automaticamente un tag JavaScript a tutti i creativi associati e [!DNL Adelaide] tiene traccia dei dati di esposizione e li invia quotidianamente all&#39;DSP. Puoi utilizzare la data per ottimizzare manualmente la spesa per le tattiche di posizionamento con punteggi di attenzione migliori.

Il campo [!UICONTROL Attention Score] è disponibile nella sezione [!UICONTROL Metrics] dei report, nelle visualizzazioni [!UICONTROL Campaigns], [!UICONTROL Packages] e [!UICONTROL Placements] e nelle schede [!UICONTROL Sites], [!UICONTROL Ads] e [!UICONTROL Inventory] della visualizzazione [dettagli posizionamento](/help/dsp/campaign-management/reports/placement-details-view.md).

L&#39;utilizzo di [!DNL Adelaide] segmenti per la misurazione comporta una tariffa CPM per ogni impression distribuita dagli annunci con [!DNL Adelaide] tag di misurazione. Questa tariffa è separata dalle tariffe per il [targeting dell&#39;attenzione a livello di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md).

<!--
Example JavaScript tag:

`<script src="https://www.example.com/aam?asid=0123456789&ad=${TM_AD_ID_NUM}&adv=${TM_ADVERTISER_ID}&ca=${TM_CAMPAIGN_ID_NUM}&df=${NS_PLATFORM_ID}&dt=${NS_DEVICE_GROUPING}&pl=${TM_PLACEMENT_ID_NUM}&ra=${TM_RANDOM}&st=${TM_SITE_URL_URLENC}"></script>`
-->

### [!UICONTROL 1st Party Metrics]

**[!UICONTROL Viewability sensitivity]:** Abilita la misurazione di prime parti e il reporting della visualizzabilità utilizzando la tecnologia [!DNL IAB Open Video Viewability (OpenVV)], in base al livello di riservatezza specificato:

* *[!UICONTROL Standard (50% of ad in view for two consecutive seconds)]*

* *[!UICONTROL Strict (100% of ad in view and audio on for 50% duration)]*

>[!MORELIKETHIS]
>
>* [Informazioni su Campaign Management](campaign-about.md)
>* [Crea una campagna](campaign-create.md)
>* [Modifica una campagna](campaign-edit.md)
>* [Visualizza il log delle modifiche per una campagna](campaign-change-log.md)
