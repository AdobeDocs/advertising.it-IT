---
title: Impostazioni di Campaign
description: Consulta le descrizioni delle impostazioni della campagna disponibili.
feature: DSP Campaigns
exl-id: 461c3f9e-ef69-46e7-8eb1-37ccc085ba1f
source-git-commit: 4085c1b21c0fe84653978e449321868921841367
workflow-type: tm+mt
source-wordcount: '928'
ht-degree: 0%

---

# Impostazioni di Campaign

## [!UICONTROL Basic Campaign Details]

**[!UICONTROL Name]:** Nome della campagna.

**[!UICONTROL Advertiser]:** (Sola lettura per le campagne esistenti) L’inserzionista (marchio) applicabile. Seleziona un inserzionista esistente o creane uno nuovo.

**[!UICONTROL Advertiser URL]:** La pagina ufficiale dell’inserzionista. Questo campo velocizza il processo di approvazione degli annunci con i partner di inventario.

**[!UICONTROL Timezone]:** (Solo lettura per le campagne esistenti) Il fuso orario per la generazione di rapporti e le offerte.

**[!UICONTROL Customer PO]:** (Facoltativo) Ordine di acquisto cliente per l&#39;ordine di inserimento/ordine di acquisto.

**[Date campagna]:** Le date di inizio e di fine della campagna.

## [!UICONTROL Campaign Goals]

**[!UICONTROL Margin Management]:** Se gestire i margini per la campagna: *[!UICONTROL Yes]* o *[!UICONTROL No]* (impostazione predefinita).

Quando scegli *[!UICONTROL Yes],* specificare il tipo di margine e l&#39;importo:

* **[!UICONTROL Margin Type]:** Tipo di margine. Non è possibile modificare il tipo di margine dopo aver abilitato la gestione dei margini e salvato la campagna.

   * *[!UICONTROL Fixed]:* (impostazione predefinita) Consente DSP di calcolare automaticamente e di limitare la spesa in base a una percentuale di margine fissa del [!UICONTROL Gross Budget].

   * *[!UICONTROL Dynamic]:* Consente di gestire i margini verso il basso fino al livello di posizionamento specificando un valore separato [!UICONTROL Budget Reserve %] e [!UICONTROL Gross Budget] per ogni pacchetto e posizionamento nella campagna. DSP ottimizza in base all&#39;efficienza finanziaria di ciascun posizionamento, senza garantire un margine specifico. Utilizzare questa opzione per gli ordini di inserimento costituiti da più elementi di riga per i quali si è deciso di fornire un importo fisso di unità o tipi di unità a un tasso fisso.

* **[!UICONTROL Fixed Margin %]:** (Solo campagne con margini fissi) Marcatura predefinita per ogni ordine di inserimento <!-- impression? -->, come percentuale. Tale importo è dedotto dal [!UICONTROL Gross Budget] definire il bilancio netto della campagna.

* **[!UICONTROL Budget Reserve %]:** (solo campagne con margini fissi; (facoltativo) Riserva una determinata percentuale del [!UICONTROL Gross Budget] come salvaguardia. Tale importo è dedotto dal [!UICONTROL Gross Budget] definire il bilancio netto della campagna.

**[!UICONTROL Gross Budget]:** (Campagne con gestione dei margini) Il bilancio lordo della campagna, prima dell&#39;applicazione degli aggiustamenti marginali specificati.

Facoltativamente, puoi aggiungere un budget lordo giornaliero, settimanale o mensile aggiuntivo:

1. Clic **[!UICONTROL Add an additional Gross Budget]**.

1. Inserisci il **[!UICONTROL Gross Budget]** e selezionare l&#39;intervallo di budget: *[!UICONTROL Daily],* *[!UICONTROL Weekly],* o *[!UICONTROL Monthly]*.

Il budget netto totale, che è il limite di spesa per la campagna, viene calcolato automaticamente in base alle impostazioni del margine ed è indicato al di sotto di questo valore.

**[!UICONTROL Budget]:** (Campagne senza gestione dei margini) Il bilancio complessivo della campagna.

**[!UICONTROL Estimated Tax Withholding]:** Consente di trattenere una percentuale della spesa totale per le tariffe degli annunci, le tariffe di servizio degli annunci e/o le tariffe dei dati a livello di account per le imposte nazionali o locali. I tassi sono stime a scopo di budget e di calcolo, pertanto le aliquote fiscali fatturate possono variare.

Per stimare le imposte da trattenere:

1. Clic **[!UICONTROL Update rates here]**.

1. Specifica la **[!UICONTROL Estimated tax rate]**, come percentuale.

1. Selezionare la casella di controllo accanto a ogni tipo di commissione per la quale trattenere le imposte. I tipi di commissione includono:

   * *[!UICONTROL Include estimated tax - ads fee]:* Si applica a tutte le spese pubblicitarie DSP media, incluse le tasse sulle commissioni di gestione delle campagne.

   * *[!UICONTROL Include estimated tax - ad serving fee]:* Si applica a tutte le spese per i DSP pubblicitari, ad eccezione dei media e dei dati. Sono escluse le tasse per le commissioni di gestione delle campagne

   * *[!UICONTROL Include estimated tax - data fee]:* Si applica a tutte le spese di dati per la DSP pubblicitaria.

1. Clic **[!UICONTROL Submit]**.

>[!NOTE]
>
>* Negli Stati Uniti, gli stati possono variare nella loro inclusione di tasse tra annunci, ad serving, e dati. Per le organizzazioni di altri paesi, includere tutte e tre le categorie di tasse per contabilizzare l&#39;IVA.
>
>* Puoi anche configurare questi valori nelle impostazioni delle tariffe dell&#39;account.<!--[fee settings](/help/dsp/admin/tax-withholdings.md). -->


**[!UICONTROL Cross Device Level]:** (sola lettura per le campagne esistenti create dal 22 giugno 2020; non disponibile per le campagne create prima del 22 giugno 2020) Livello a cui DSP indirizzare gli annunci e applicare limiti di frequenza: *Stesso dispositivo* per eseguire il targeting di un dispositivo o *Persone* per eseguire il targeting di una persona su tutti i suoi dispositivi noti.

**[!UICONTROL Device Graph]:** (sola lettura per le campagne esistenti; campagne con targeting su più dispositivi basato solo sulle persone) Il grafico dei dispositivi da utilizzare per il targeting su più dispositivi e la gestione della frequenza:

* *[!UICONTROL LiveRamp - U.S. only]:* Disponibile per tutti gli inserzionisti per il targeting tra dispositivi a $ 0,35 CPM per le impression consegnate utilizzando il [!DNL LiveRamp] grafico dei dispositivi (ovvero, per dispositivi non trovati all’interno dei segmenti di pubblico target). Puoi impostare il targeting tra dispositivi a livello di posizionamento.

   Questa opzione è disponibile anche per tutti gli inserzionisti, senza alcun costo, per la gestione della frequenza e la misurazione dell’attribuzione.

**[!UICONTROL Frequency Cap]:** (Facoltativo) Il numero di volte in cui una persona o un dispositivo univoco (a seconda del valore specificato) [!UICONTROL Cross Device Level]verranno serviti gli annunci dalla campagna. Le opzioni includono *[!UICONTROL Unlimited]* o un importo specifico per giorno, settimana o mese.

>[!NOTE]
>
> Puoi impostare i limiti di frequenza a livello di campagna, pacchetto e posizionamento. DSP rispettare il limite di frequenza più rigoroso nella gerarchia delle campagne.

**[!UICONTROL Packages]:** La [pacchetti](/help/dsp/campaign-management/packages/package-about.md) da includere nella campagna. Seleziona i pacchetti esistenti e/o crea i pacchetti da includere. Se crei pacchetti, consulta le descrizioni [impostazioni del pacchetto](/help/dsp/campaign-management/packages/package-settings.md) per ulteriori informazioni.

## [!UICONTROL Campaign Measurement]

>[!NOTE]
>
>Le seguenti impostazioni consentono solo funzionalità di misurazione e reporting. L’ottimizzazione delle prestazioni viene eseguita solo a livello di pacchetto e posizionamento.

### [!UICONTROL 3rd Party Metrics]

#### [!UICONTROL Viewability, Fraud, & Brand Safety]

**[!UICONTROL IAS]:** (Facoltativo) Abilita [!DNL IAS] misurazione e reporting di visualizzabilità, frode, sicurezza del marchio e verifica del pubblico, utilizzando le impostazioni specificate. Sono previsti costi aggiuntivi.

* **[!UICONTROL Measure On]:** L&#39;inventario su cui misurare: *[!UICONTROL Display and VPAID video inventory]* (impostazione predefinita) o *[!UICONTROL Display, VPAID & VAST video inventory]*.

   >[!NOTE]
   >
   >La visualizzabilità video è misurabile solo su inventario VPAID.

* **[!UICONTROL IAS Account ID (AnID)]:** (inserzionisti con le proprie [!DNL IAS] conti; facoltativo) l&#39;organizzazione [!DNL IAS] ID account, quale [!DNL IAS] fatturerà direttamente per uso.

* **[!UICONTROL IAS Team ID]:** (inserzionisti con le proprie [!DNL IAS] conti; facoltativo) l&#39;ID del team per [!DNL IAS] che [!DNL IAS] fatturerà direttamente per uso. <!-- verify -->

**[!UICONTROL MOAT]:** (Facoltativo) Abilita [!DNL MOAT] misurazione e reporting di visualizzabilità, frode, sicurezza del marchio e verifica del pubblico. Sono previsti costi aggiuntivi.

#### Verifica del pubblico

**[!UICONTROL Nielsen]:** (Facoltativo) Abilita [!DNL Nielsen] misurazione e reporting della verifica del pubblico, utilizzando le impostazioni specificate. Sono previsti costi aggiuntivi.

* **[!UICONTROL Target Gender]:** Il genere da indirizzare: *[!UICONTROL Both]* (impostazione predefinita), *[!UICONTROL Male]* oppure *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** Intervallo di età da utilizzare. Utilizza i cursori sinistro e destro per ridurre l’intervallo in base alle esigenze.

* **[!UICONTROL Target Country]:** (Facoltativo) Un paese a cui rivolgersi. [!DNL Nielsen] misurerà le impression servite solo nei paesi supportati.

**[!UICONTROL comScore vCE]:** (Facoltativo) Abilita [!DNL Comscore validated Campaign Essentials (vCE)] misurazione e reporting della verifica del pubblico, utilizzando le impostazioni specificate. Sono previsti costi aggiuntivi.

* **[!UICONTROL Target Gender]:** Il genere da indirizzare: *[!UICONTROL Both]* (impostazione predefinita), *[!UICONTROL Male]* oppure *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** Intervallo di età da utilizzare. Utilizza i cursori sinistro e destro per ridurre l’intervallo in base alle esigenze.

* **[!UICONTROL Target Country]:** (Facoltativo) Un paese a cui rivolgersi. [!DNL Comscore] misurerà le impression servite solo nei paesi supportati.

### [!UICONTROL 1st Party Metrics]

**[!UICONTROL Viewability sensitivity]:** Abilita la misurazione e il reporting di prima parte della visualizzabilità utilizzando [!DNL IAB Open Video Viewability (OpenVV)] in base al livello di sensibilità specificato:

* *[!UICONTROL Standard (50% of ad in view for two consecutive seconds)]*

* *[!UICONTROL Strict (100% of ad in view and audio on for 50% duration)]*

>[!MORELIKETHIS]
>
>* [Informazioni su Campaign Management](campaign-about.md)
>* [Creare una campagna](campaign-create.md)
>* [Modificare una campagna](campaign-edit.md)
>* [Visualizza il registro delle modifiche per una campagna](campaign-change-log.md)

