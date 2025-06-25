---
title: Panoramica di  [!DNL Analytics for Advertising]
description: Panoramica di  [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 94558478-ffa6-4b83-bc79-c7589fe0f14c
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '1223'
ht-degree: 0%

---

# Panoramica di [!DNL Analytics for Advertising]

*Inserzionisti con Advertising DSP e[!DNL Advertising Search, Social, & Commerce]*

[!DNL Analytics for Advertising] integra Adobe Analytics e Adobe Advertising per estendere e migliorare le funzionalità di ogni prodotto.

L&#39;integrazione consente agli inserzionisti di tenere traccia delle interazioni con i siti click-through e view-through nelle loro istanze [!DNL Analytics], consentendo ai brand di vedere in che modo la spesa pubblicitaria porta al coinvolgimento del sito e agli obiettivi aziendali critici.

Inoltre, Adobe Advertising può accedere ai vasti dati di prime parti che [!DNL Analytics] raccoglie utilizzando [!DNL Analytics] tag già presenti sul sito. Ciò consente una gestione più solida del percorso, attività di remarketing di prime parti e reporting sui siti a pagamento. Adobe Advertising può utilizzare ulteriormente i dati [!DNL Analytics] per l&#39;ottimizzazione delle spese e delle offerte.

Se utilizzato correttamente, [!DNL Analytics for Advertising] offusca le linee tra due ruoli tradizionali: gestione del percorso pubblicitario (l&#39;atto di inviare utenti al sito tramite annunci pubblicitari) e comprensione del coinvolgimento del sito tramite analisi Web.

Vantaggi principali:

* Invia [!DNL Analytics] segmenti direttamente ad Adobe Advertising per il remarketing del sito di prime parti.
* Utilizza [!DNL Analytics] eventi personalizzati e standard come segnali di conversione per ottimizzare la pubblicità multimediale a pagamento.
* Utilizza [!DNL Analytics] Analysis Workspace per comprendere meglio i punti di ingresso al sito e il comportamento delle visite.
* Consente una più stretta collaborazione tra gli analisti web e i team dei media a pagamento.
* Utilizzare gli ID view-through e click-through persistenti di Adobe Advertising in [!DNL Analytics] per comprendere il coinvolgimento del sito.
* Migliora i report tradizionali di paid media in Analysis Workspace con metriche personalizzate, dimensioni personalizzate e attività del sito non raggiungibili durante l’esportazione di dati o pixel verso ad server o altre DSP.
* Utilizza il codice [!DNL Analytics] già presente sul tuo sito Web per il tracciamento e l&#39;ottimizzazione in Adobe Advertising.

>[!TIP]
>
> Guarda un [video introduttivo a [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html#analytics).

## Utilizzo di Analytics per il reporting di file multimediali a pagamento

[!DNL Analytics for Advertising] migliora il reporting e insight sul modo in cui il tuo advertising determina il comportamento del sito, consentendoti di:

* Utilizzare gli ID view-through e click-through persistenti di Adobe Advertising in [!DNL Analytics] per comprendere il coinvolgimento del sito.
* Sfrutta Analysis Workspace per comprendere meglio i punti di ingresso al sito e il comportamento delle visite. Puoi accedere ai dati di eventi e dimensionali dei contenuti multimediali a pagamento, che includono i nomi delle entità di Adobe Advertising Campaign (fino a posizionamenti e annunci) e le metriche associate, come clic, impression e costi.

Per utilizzare [!DNL Analytics] come strumento di reporting per contenuti multimediali a pagamento, è necessario un accesso Experience Cloud con accesso ad Analysis Workspace. Il team di Adobe Advertising ti aiuterà a mappare i dati di Adobe Advertising sulle singole suite di rapporti in Analysis Workspace. Puoi inviare dati di Adobe Advertising a qualsiasi suite di rapporti, ma dovresti essere a conoscenza delle suite di rapporti che sono state mappate su Adobe Advertising e di quelle che non lo sono state. A seconda della suite di rapporti, questo potrebbe modificare i dati segnalati.

[Gli ID Adobe Advertising all&#39;interno di [!DNL Analytics]](ids.md) funzionano come altri [!DNL eVars], con una scadenza personalizzata e persistente. Per impostazione predefinita, l’intervallo di lookback dell’attribuzione è impostato su 60 giorni durante l’implementazione di Adobe Advertising. Per modificare questa impostazione, rivolgiti al team del tuo account Adobe.

Alle dimensioni Adobe Advertising viene aggiunto il suffisso &quot;(AMO ID)&quot; (ad esempio &quot;Ad Type (AMO ID)&quot;). Per un elenco delle dimensioni disponibili, vedere &quot;[Metriche Adobe Advertising in Analysis Workspace](advertising-metrics-in-analytics.md)&quot;.

>[!NOTE]
>
> Quando visualizzi i dati di Adobe Advertising (o qualsiasi set di dati) in [!DNL Analytics], tieni presente che le metriche e i rapporti si basano sulle regole impostate in [!DNL Analytics]. I dati potrebbero essere diversi da quelli visualizzati in altri sistemi di reporting, ad esempio report del server di annunci, report [!DNL DSP] o report del motore di ricerca. Per comprendere le differenze di dati in [!DNL Analytics], è necessario sapere quando scadono i dati di [!DNL eVar], cosa definisce una visita, cosa viene considerata attribuzione ultimo contatto rispetto all&#39;attribuzione totale persistente e altri fattori. Per ulteriori informazioni, vedere [Varianze di dati previste tra [!DNL Analytics] e Adobe Advertising](data-variances.md).

## Utilizzo di Analytics per sviluppare campagne e portfolio Adobe Advertising

Senza richiedere pixel aggiuntivi, [!DNL Analytics for Advertising] consente una migliore ottimizzazione e una più semplice segmentazione del pubblico inviando due segnali principali ad Adobe Advertising:

* Metriche di conversione da utilizzare come segnali di offerta:
   * metriche standard, ad esempio [!UICONTROL Revenue] e [!UICONTROL Cart Views].
   * le metriche di coinvolgimento del sito, come la visualizzazione pagina e le metriche di visita.
   * metriche di ricavo personalizzate.
   * metriche delle entrate riservate.
* Segmenti creati in [!DNL Analytics] e pubblicati in Experience Cloud.

  È possibile utilizzare [!DNL Analytics] segmenti per il retargeting del sito di prime parti in [!DNL DSP] e annunci di ricerca a pagamento.

  (Solo per [!DNL Search, Social, & Commerce]) Gli inserzionisti con [!DNL Analytics] ma non Audience Manager possono anche creare tipi di pubblico basati su tag (elenchi di remarketing) e tipi di pubblico con corrispondenza dei clienti (elenchi dei clienti) del sito Web Google da [!DNL Analytics] segmenti condivisi con Experience Cloud.

### Metriche di conversione del sito come segnali di offerta

Puoi utilizzare gli eventi standard e gli eventi personalizzati di [!DNL Analytics] per creare obiettivi ponderati in Adobe Advertising. Gli obiettivi sono alla base delle decisioni di offerta per i pacchetti [!DNL DSP] e i portfolio Search, Social e Commerce.

Per le campagne [!DNL Google Ads] e [!DNL Google Microsoft Advertising] nei portfolio ibridi Search, Social e Commerce, puoi facoltativamente caricare gli obiettivi, inclusi eventuali eventi [!DNL Analytics] negli obiettivi, direttamente nelle reti di annunci, dove diventano disponibili come azioni di conversione per gli obiettivi di conversione personalizzati a livello di account e di campagna.

>[!NOTE]
>
> Impossibile mappare le metriche calcolate da [!DNL Analytics] ad Adobe Advertising.

Il tuo team Adobe Advertising ti aiuterà a identificare e mappare gli eventi applicabili alle prestazioni di paid media in Adobe Advertising, dove sono elencati in [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Admin] > [!UICONTROL Conversions].

Per un elenco delle metriche disponibili, vedere &quot;[Metriche di Analytics in Adobe Advertising](analytics-data-in-advertising.md)&quot;.

### Segmenti di Analytics per il retargeting del sito

Adobe Advertising può acquisire [!DNL Analytics] segmenti a scopo di remarketing per Advertising DSP e [!DNL Search, Social, & Commerce] annunci utilizzando l&#39;integrazione nativa di Experience Cloud Audiences tra [!DNL Analytics] e Experience Cloud.

Per accedere ai segmenti [!DNL Analytics], un account inserzionista deve abilitare il [servizio Experience Cloud ID](https://experienceleague.adobe.com/docs/id-service/using/home.html). Quando il servizio ID è abilitato, tutti i segmenti di Experience Cloud (inclusi i segmenti creati in [!DNL Analytics] e pubblicati in Experience Cloud, i segmenti creati in Adobe Audience Manager, i segmenti creati in Experience Cloud utilizzando [!DNL People core service] e i segmenti creati in Adobe Experience Platform e inviati ad Adobe Advertising tramite Audience Manager) diventano disponibili in Adobe Advertising non appena vengono elaborati.

[!DNL Analytics] segmenti sono disponibili entro 24 ore e vengono aggiornati ogni giorno.

Per ulteriori informazioni sul servizio Experience Cloud Audiences, vedi [Tipi di pubblico di Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html).

## Esempi di come utilizzare l’integrazione {#integration-examples}

### Utilizzo dei dati di Adobe Advertising in Analysis Workspace

Per scoprire come utilizzare i dati di Adobe Advertising per creare report visivi in Analysis Workspace, guarda il video &quot;[Introduzione a Workspace e reporting](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html).&quot;

#### Utilizzo delle conversioni view-through di programmi TV collegati nei report

*Solo utenti Advertising DSP*

È possibile misurare l&#39;efficacia full funnel delle campagne CTV (connected TV) collegando l&#39;esposizione pubblicitaria sui dispositivi CTV alle conversioni in loco. Il nuovo filtro [!UICONTROL Landing Type] &quot;[!UICONTROL View-through (CTV)]&quot; suddivide le conversioni in righe separate per i valori [!UICONTROL Click Through], [!UICONTROL View Through] e [!UICONTROL View Through (CTV)].

Per visualizzare le metriche di conversione view-through CTV, utilizza la vista Posizionamento o la vista Canale di marketing in Analysis Workspace.

Utilizzo della vista Posizionamento:

1. Includi i posizionamenti di spesa CTV nella visualizzazione di reporting.

1. Includi le metriche desiderate, ad esempio &quot;Impression&quot;, &quot;Clic&quot; e così via.

1. Applica i seguenti filtri:

   Piattaforma annuncio: `Advertising Cloud DSP`

   Pagina di destinazione: `View-Through (CTV)`

Utilizzo della vista Canale di marketing:

1. Includere la dimensione `Marketing Channel`.

1. Includi le metriche desiderate, ad esempio &quot;Impression&quot;, &quot;Clic&quot; e così via.

1. Applica i seguenti filtri:

   Piattaforma annuncio: `Advertising Cloud DSP`

   Pagina di destinazione: `View-Through (CTV)`

### Creazione di dashboard di Adobe Advertising

Per scoprire come tenere traccia dei dati di Adobe Advertising rispetto agli obiettivi in Analysis Workspace, guarda il video &quot;[Creare dashboard di Adobe Advertising con Adobe Analytics](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-dashboards-a4adc.html).&quot;

### Utilizzo di Adobe Advertising ID per l’analisi dell’ingresso nel sito

Per scoprire come creare un report sulle visite al sito di Adobe Advertising per monitorare le influenze relative a giorno della settimana, ora del giorno, browser e aree geografiche, guarda il video &quot;[Creazione di report sulle visite al sito di Adobe Advertising](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-site-entry-a4adc.html)&quot;.

## Come avviare un&#39;implementazione di [!DNL Analytics for Advertising]

Contatta il team del tuo account Adobe, che completerà la configurazione iniziale necessaria per iniziare e ti aiuterà a pianificare l’implementazione e l’utilizzo dei dati in base alle esigenze della tua organizzazione.

>[!MORELIKETHIS]
>
>* [Video: introduzione a [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html)
>* [Prerequisiti e informazioni chiave per l&#39;implementazione [!DNL Analytics for Advertising]](prerequisites.md)
>* [ID Adobe Advertising utilizzati da Analytics](ids.md)
>* [Codice JavaScript per Advertising](/help/integrations/analytics/javascript.md)
>* [Varianze di dati previste tra [!DNL Analytics] e Adobe Advertising](data-variances.md)
>* [Metriche Adobe Advertising in Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Dati in Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
