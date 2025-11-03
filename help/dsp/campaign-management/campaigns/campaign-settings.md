---
title: Impostazioni campagna
description: Consulta le descrizioni delle impostazioni disponibili per la campagna.
feature: DSP Campaigns
exl-id: 461c3f9e-ef69-46e7-8eb1-37ccc085ba1f
source-git-commit: 9d26e097f007b570c0f0e3b7f02c683a84d5e647
workflow-type: tm+mt
source-wordcount: '1434'
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

**[!UICONTROL Margin Management]:** (account self-service gestiti dalle agenzie tramite margini) Opzioni per la gestione dei margini:

* **[!UICONTROL Would you like to manage margins for this campaign?]:** Se gestire i margini per la campagna: *[!UICONTROL Yes]* o *[!UICONTROL No]* (impostazione predefinita). Quando scegli *[!UICONTROL Yes],* specifica le impostazioni aggiuntive. Dopo aver abilitato la gestione dei margini e salvato la campagna, non è possibile disabilitare la gestione dei margini.

* **[!UICONTROL How would you like to compute agency fees?]:** (solo campagne con gestione dei margini) Come calcolare le spese di agenzia, ovvero la parte del budget lordo della campagna che viene trattenuta e non inclusa nella spesa netta:

   * *[!UICONTROL Margin % of Total Budget]:* (impostazione predefinita) Calcola le commissioni come percentuale della spesa lorda. Specificare [!UICONTROL Agency Fee Type] (fisso o composito) e [!UICONTROL Margin %] o [!UICONTROL Composite Margin %].

   * *[!UICONTROL Apply Markup % on top of individual cost components]:* Calcola le tariffe come percentuale specificata dei costi dei contenuti multimediali, dei dati e di altri costi e/o [!DNL Adobe] le tariffe tecniche. Specificare [!UICONTROL Markup %] e selezionare i componenti ai quali applicare il markup.

* **[!UICONTROL Agency Fee Type]:** (campagne che utilizzano [!UICONTROL Margin % of Total Budget]) Il tipo di tariffa dell&#39;agenzia.

   * *[!UICONTROL Fixed]:* (impostazione predefinita) Consente a DSP di trattenere una percentuale fissa della spesa lorda come spese di agenzia. Specificare [!UICONTROL Margin %].

   * *[!UICONTROL Composite]:* consente a DSP di trattenere una percentuale della spesa lorda per contabilizzare sia le spese di agenzia che le [!DNL Adobe] spese tecniche. Specificare [!UICONTROL Composite Margin %].

* **[!UICONTROL Margin %]:** (campagne che utilizzano [!UICONTROL Margin % of Total Budget] con margini fissi) La percentuale della spesa lorda da trattenere come spese di agenzia. Eventuali modifiche al valore del margine vengono applicate solo alla spesa lorda futura e non alla spesa lorda storica per la campagna. Il valore [!UICONTROL Estimated Tax Withholding] è escluso dalla spesa lorda prima dell&#39;applicazione del margine. Consulta gli esempi seguenti, che presuppongono che la campagna non sia sovracspesa o sottospesa.

   * Esempio 1: si supponga che [!UICONTROL Gross Budget] sia `100 USD` e che [!UICONTROL Margin %] sia `5%` per tutto il volo. Al termine del volo della campagna, le tariffe dell&#39;agenzia vengono calcolate come `5 USD` (ovvero `5% of 100 USD`) e la spesa netta è `95 USD` (ovvero `campaign budget [100 USD] - agency fees [5 USD]`).

   * Esempio 2 con modifiche al margine: per la stessa campagna, si supponga che [!UICONTROL Margin %] sia stato modificato da `5%` a `10%` quando la spesa lorda era `40 USD`. Per il periodo precedente alla modifica, le tariffe di agenzia vengono calcolate come `2 USD` (ovvero `5% of 40 USD`); per il periodo successivo alla modifica, le tariffe di agenzia vengono calcolate come `6 USD` (ovvero `10% of 60 USD`). Le tariffe totali dell&#39;agenzia vengono calcolate come `8 USD` (ovvero `2 USD + 6 USD`) e la spesa netta è `92 USD` (ovvero `campaign budget [100 USD] - total agency fees [8 USD]`).

   * Esempio 3 con ritenuta fiscale: si supponga che [!UICONTROL Gross Budget] sia `100 USD`, che [!UICONTROL Estimated Tax Withholding] alla fine del volo della campagna sia `10 USD` e che [!UICONTROL Margin %] sia `5%` durante il volo. Al termine del volo della campagna, le tariffe dell&#39;agenzia vengono calcolate come `4.5 USD` (ovvero `5% of (campaign budget [100 USD] - tax withholding [USD 10])`) e la spesa netta è `85.5 USD` (ovvero `campaign budget [100 USD] - agency fees [4.5 USD] - tax withholding [10 USD]`).

* **[!UICONTROL Composite Margin %]:** (campagne che utilizzano [!UICONTROL Margin % of Total Budget] con margini compositi) La percentuale della spesa lorda che, da trattenere sotto forma di [!DNL Adobe] spese tecniche e di agenzia combinate. Le tariffe di agenzia vengono calcolate sottraendo le tariffe tecniche di Adobe dall’importo del margine composito. Eventuali modifiche al valore del margine composito vengono applicate solo alla spesa lorda futura e non alla spesa lorda storica per la campagna. Il valore [!UICONTROL Estimated Tax Withholding] è escluso dalla spesa lorda prima dell&#39;applicazione del margine composito.

  Si supponga, ad esempio, che [!UICONTROL Gross Budget] sia `100 USD`, che le [!DNL Adobe] tariffe tecniche alla fine del volo della campagna siano `10 USD` e che [!UICONTROL Composite Margin %] sia `17%` per tutto il volo. Al termine del volo della campagna (supponendo che la campagna non sia sottoutilizzata o sovracspesa), le tariffe di agenzia vengono calcolate come `7 USD` (ovvero `(17% of 100 USD) - 10`) e la spesa netta è `93 USD` (ovvero `campaign budget [100 USD] - agency fees [7 USD]`).

* **[!UICONTROL Markup %]:** (campagne che utilizzano [!UICONTROL Apply Markup % on top of individual cost components]) Percentuale da applicare ai componenti di costo specificati per calcolare le spese di agenzia. Eventuali modifiche al valore di markup vengono applicate solo ai costi futuri e non ai costi storici della campagna.

* **[!UICONTROL Select cost components on which markup will be applied]:** (campagne che utilizzano [!UICONTROL Apply Markup % on top of individual cost components]) I componenti di costo per i quali è applicato [!UICONTROL Markup %]. Selezionare tutti i componenti applicabili: *[!UICONTROL Media cost]*, *[!UICONTROL Data and Other costs]* e/o *[!UICONTROL Adobe tech fees]*. Eventuali modifiche alla selezione dei componenti vengono applicate solo ai costi futuri e non ai costi storici della campagna.

  Ad esempio, [!UICONTROL Markup %] è `10%` per &quot;[!UICONTROL Media cost]&quot; e &quot;[!UICONTROL Data and Other costs]. Se, in qualsiasi momento del volo della campagna, il costo dei supporti è `20 USD`, i dati e gli altri costi sono `5 USD` e le spese tecniche [!DNL Adobe] sono `2 USD`, le spese di agenzia vengono calcolate come `2.50 USD` (ovvero `10% of (20 USD + 5 USD)` e la spesa lorda è `29.50 USD` (ovvero `media cost [20 USD] + data and other costs [5 USD] + [!DNL Adobe] tech fees [2 USD] + agency fees [2.50 USD]`).

**[!UICONTROL Gross Budget]:** (solo campagne con gestione dei margini) Il budget lordo della campagna, prima dell&#39;applicazione degli adeguamenti marginali specificati.

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

**[!UICONTROL Cross Device Level]:** (sola lettura per le campagne esistenti create dal 22 giugno 2020; non disponibile per le campagne create prima del 22 giugno 2020) Livello al quale DSP esegue il targeting degli annunci e applica limiti di frequenza: *Stesso dispositivo* per eseguire il targeting di un dispositivo o *Persone* per eseguire il targeting di una persona su tutti i dispositivi noti. **Nota:** il supporto tra dispositivi non è disponibile per i posizionamenti che hanno come destinazione gli ID universali.

**[!UICONTROL Device Graph]:** (sola lettura per campagne esistenti; campagne con targeting multidispositivo basato sulle persone) Il grafico dei dispositivi da utilizzare per il targeting multidispositivo e la gestione della frequenza:

* *[!UICONTROL LiveRamp - U.S. only]:* Disponibile per tutti gli inserzionisti per il targeting multidispositivo a $0,35 CPM per le impression distribuite tramite il grafico dei dispositivi [!DNL LiveRamp] (ovvero, per i dispositivi non trovati all&#39;interno dei segmenti di pubblico target). Puoi impostare il targeting tra dispositivi a livello di posizionamento.

  Questa opzione è disponibile anche per tutti gli inserzionisti, senza costi aggiuntivi, per la gestione della frequenza e la misurazione dell’attribuzione.

  Il supporto tra dispositivi si applica solo ai posizionamenti che hanno come destinazione ID legacy ma non a quelli che hanno come destinazione ID universali (inclusi [!DNL LiveRamps]). Il targeting, la gestione della frequenza e l’attribuzione per gli ID universali vengono applicati solo a livello di ID.

**[!UICONTROL Frequency Cap]:** (Facoltativo) Il numero di volte in cui un dispositivo univoco, un ID universale o una persona (a seconda di [!UICONTROL Cross Device Level] specificato e dell&#39;impostazione [!UICONTROL Targeting] del posizionamento) possono essere serviti dagli annunci dalla campagna. Le opzioni includono *[!UICONTROL Unlimited]* o un importo specifico per giorno, settimana o mese.

>[!NOTE]
>
> Puoi impostare i limiti di frequenza a livello di campagna, pacchetto e posizionamento. DSP rispetta il limite di frequenza più rigoroso nella gerarchia delle campagne.

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

#### Verifica del pubblico

**[!UICONTROL Comscore Campaign Ratings]:** (Facoltativo) Abilita la misurazione [!DNL Comscore] convalidata [!DNL Campaign Ratings] e il reporting della verifica del pubblico, utilizzando le impostazioni specificate. Si applicano tariffe aggiuntive.

* **[!UICONTROL Target Gender]:** Il genere di destinazione: *[!UICONTROL Both]* (impostazione predefinita), *[!UICONTROL Male]* o *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** L&#39;intervallo di età di destinazione. Utilizza i cursori sinistro e destro per ridurre l’intervallo in base alle esigenze.

* **[!UICONTROL Target Country]:** (Facoltativo) Un paese di destinazione. [!DNL Comscore] misure impression fornite solo nei paesi supportati.

### [!UICONTROL Attention Measurement]{#attention-measurement}

**[!UICONTROL Adelaide]:** Abilita il tracciamento per la metrica [!UICONTROL Attention Score] a livello di posizionamento (la media ponderata del numero di [!DNL Adelaide] &quot;[!DNL Attention Units]&quot; tra le impression). Le metriche sono disponibili per tutti i tipi di posizionamento ad eccezione di [!DNL Roku] TV connessa, pre-roll solo VPAID e audio che non è un podcast. DSP allega automaticamente un tag JavaScript a tutti i creativi associati e [!DNL Adelaide] tiene traccia dei dati di esposizione e li invia quotidianamente a DSP. Puoi utilizzare la data per ottimizzare manualmente la spesa per le tattiche di posizionamento con punteggi di attenzione migliori.

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
>* [Informazioni sulla gestione delle campagne](campaign-about.md)
>* [Crea una campagna](campaign-create.md)
>* [Modifica una campagna](campaign-edit.md)
>* [Visualizza il log delle modifiche per una campagna](campaign-change-log.md)
