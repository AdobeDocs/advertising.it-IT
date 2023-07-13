---
title: Panoramica di [!DNL Analytics for Advertising]
description: Panoramica di [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 94558478-ffa6-4b83-bc79-c7589fe0f14c
source-git-commit: d4306553d4ad7379672be5bff1bc5cc6f74f70bf
workflow-type: tm+mt
source-wordcount: '1185'
ht-degree: 0%

---

# Panoramica di [!DNL Analytics for Advertising]

*Inserzionisti con Advertising DSP e[!DNL Advertising Search, Social, & Commerce]*

[!DNL Analytics for Advertising] integra Adobe Analytics e Adobe Advertising per estendere e migliorare le funzionalità di ciascun prodotto.

L’integrazione consente agli inserzionisti di tenere traccia delle interazioni con i siti click-through e view-through nei loro [!DNL Analytics] consentendo ai brand di vedere in che modo la spesa pubblicitaria porta al coinvolgimento del sito e agli obiettivi aziendali critici.

Inoltre, Adobe Advertising può accedere ai vasti dati di prime parti che [!DNL Analytics] raccoglie tramite [!DNL Analytics] tag già presenti nel sito. Ciò consente una gestione più solida del percorso, attività di remarketing di prime parti e reporting sui siti a pagamento. L’Adobe Advertising può ulteriormente utilizzare [!DNL Analytics] dati per l’ottimizzazione della spesa e delle offerte.

Se correttamente impiegati, [!DNL Analytics for Advertising] sfoca le linee di confine tra due ruoli tradizionali: gestione del percorso pubblicitario (l’atto di inviare utenti al sito tramite annunci pubblicitari) e comprensione del coinvolgimento del sito tramite analisi web.

Vantaggi principali:

* Invia [!DNL Analytics] segmenti direttamente in Adobe Advertising per il remarketing del sito di prime parti.
* Utilizzare [!DNL Analytics] eventi personalizzati e standard come segnali di conversione per ottimizzare la pubblicità a pagamento.
* Sfruttare [!DNL Analytics] Analysis Workspace per comprendere meglio i punti di ingresso al sito e il comportamento delle visite.
* Consente una più stretta collaborazione tra gli analisti web e i team dei media a pagamento.
* Utilizzare gli ID view-through e click-through Adobi Advertising persistenti in [!DNL Analytics] per comprendere il coinvolgimento del sito.
* Migliora i report tradizionali di paid media in Analysis Workspace con metriche personalizzate, dimensioni personalizzate e attività del sito non raggiungibili durante l’esportazione di dati o pixel verso ad server o altri DSP.
* Sfruttare [!DNL Analytics] codice già presente sul sito web per il tracciamento e l’ottimizzazione in Adobe Advertising.

>[!TIP]
>
> Osserva un [video introduttivo a [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html#analytics).

## Utilizzo di Analytics per il reporting di file multimediali a pagamento

[!DNL Analytics for Advertising] consente di migliorare la generazione di rapporti e informazioni approfondite sul modo in cui la pubblicità guida il comportamento del sito, consentendoti di:

* Utilizzare gli ID view-through e click-through Adobi Advertising persistenti in [!DNL Analytics] per comprendere il coinvolgimento del sito.
* Sfrutta Analysis Workspace per comprendere meglio i punti di ingresso al sito e il comportamento delle visite. Puoi accedere ai dati di eventi e dimensionali a pagamento per contenuti multimediali, che includono nomi di entità di campagna di Adobe Advertising (fino a posizionamenti e annunci) e le relative metriche associate, come clic, impression e costi.

Da utilizzare [!DNL Analytics] come strumento di reporting per contenuti multimediali a pagamento, la tua organizzazione ha bisogno di un accesso Experience Cloud con accesso ad Analysis Workspace. Il team Advertising del tuo Adobe ti aiuterà a mappare i dati di Advertising dell’Adobe sulle singole suite di rapporti in Analysis Workspace. Puoi inviare dati di Adobe Advertising a qualsiasi suite di rapporti, ma dovresti essere a conoscenza delle suite di rapporti mappate su Adobe Advertising e di quelle che non lo sono state. A seconda della suite di rapporti, questo potrebbe modificare i dati segnalati.

[ID Adobe Advertising in [!DNL Analytics]](ids.md) funziona come altre eVar, con una scadenza personalizzata e persistente. Per impostazione predefinita, l’intervallo di lookback dell’attribuzione è impostato su 60 giorni durante l’implementazione di Adobe Advertising. Per modificare questa impostazione, rivolgiti al team del tuo account Adobe.

Alle dimensioni di Adobe Advertising viene aggiunto il suffisso &quot;(AMO ID)&quot; (ad esempio &quot;Ad Type (AMO ID)&quot;). Consulta &quot;[Metriche di Adobe Advertising in Analysis Workspace](advertising-metrics-in-analytics.md)&quot; per un elenco delle dimensioni disponibili.

>[!NOTE]
>
> Quando visualizzi i dati di Adobe Advertising (o qualsiasi set di dati) in [!DNL Analytics], le metriche e i rapporti si basano sulle regole impostate in [!DNL Analytics]. I dati potrebbero essere diversi da quelli visualizzati all’interno di altri sistemi di reporting, ad esempio i rapporti sui server di annunci, [!DNL DSP] rapporti o rapporti dei motori di ricerca. Per comprendere le differenze di dati in [!DNL Analytics], è necessario sapere quando scadono i dati eVar, cosa definisce una visita, cosa viene considerata attribuzione ultimo contatto rispetto all’attribuzione persistente totale e altri fattori. Per ulteriori informazioni, consulta [Varianze di dati previste tra [!DNL Analytics] e ADOBE ADVERTISING](data-variances.md).

## Utilizzo di Analytics per potenziare campagne e Portfoli pubblicitari Adobe

Senza richiedere pixel aggiuntivi, [!DNL Analytics for Advertising] consente di ottimizzare e segmentare più facilmente il pubblico inviando all’Adobe Advertising due segnali principali:

* Metriche di conversione da utilizzare come segnali di offerta:
   * metriche standard, come [!UICONTROL Revenue] e [!UICONTROL Cart Views].
   * le metriche di coinvolgimento del sito, come la visualizzazione pagina e le metriche di visita.
   * metriche di ricavo personalizzate.
   * metriche delle entrate riservate.
* Segmenti creati in [!DNL Analytics] e pubblicato su Experience Cloud.

  È possibile utilizzare [!DNL Analytics] segmenti per il retargeting del sito di prime parti in [!DNL DSP] e annunci di ricerca a pagamento.

  ([!DNL Search, Social, & Commerce] solo) Per gli inserzionisti con [!DNL Analytics] ma non è un Audience Manager di può anche creare tipi di pubblico basati su tag (elenchi di remarketing) e tipi di pubblico con corrispondenza dei clienti (elenchi di clienti) da Google [!DNL Analytics] segmenti condivisi con Experience Cloud.

### Metriche di conversione del sito come segnali di offerta

Puoi utilizzare gli eventi standard e gli eventi personalizzati da [!DNL Analytics] per creare obiettivi ponderati in Adobe Advertising. Gli obiettivi informano le decisioni di offerta per il tuo [!DNL DSP] pacchetti e portafogli di ricerca.

>[!NOTE]
>
> Impossibile mappare le metriche calcolate da [!DNL Analytics] in Adobe Advertising.

Il team di Adobe Advertising ti aiuterà a identificare e mappare gli eventi applicabili alle prestazioni dei contenuti multimediali a pagamento in Adobe Advertising, dove verranno visualizzati in [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Transaction Properties].

Consulta &quot;[Metriche di Analytics in Adobe Advertising](analytics-data-in-advertising.md)&quot; per un elenco delle metriche disponibili.

### Segmenti di Analytics per il retargeting del sito

L’Adobe Advertising può acquisire [!DNL Analytics] segmenti a scopo di remarketing per Advertising DSP e [!DNL Search, Social, & Commerce] annunci tramite l’integrazione nativa Experience Cloud Audiences tra [!DNL Analytics] e Experience Cloud.

Per accedere al [!DNL Analytics] segmenti, un account dell&#39;inserzionista deve avere [Servizio ID Experience Cloud](https://experienceleague.adobe.com/docs/id-service/using/home.html) abilitato. Quando il servizio ID è abilitato, tutti i segmenti Experience Cloud (inclusi quelli creati in [!DNL Analytics] e pubblicati in Experience Cloud, segmenti creati in Adobe Audience Manager, segmenti creati in Experience Cloud utilizzando [!DNL People core service]I segmenti, e creati in Adobe Experience Platform e inviati ad Adobe Advertising tramite Audience Manager diventano disponibili all’interno di Adobe Advertising non appena vengono elaborati.

[!DNL Analytics] I segmenti sono disponibili entro 24 ore e vengono aggiornati ogni giorno.

Per ulteriori informazioni sul servizio Audiences di Experience Cloud, consulta [Tipi di pubblico di Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html).

## Esempi di come utilizzare l’integrazione {#integration-examples}

### Utilizzo dei dati Adobe Advertising in Analysis Workspace

Per scoprire come utilizzare i dati pubblicitari di Adobe per creare rapporti visivi in Analysis Workspace, guarda il video &quot;[Introduzione a Workspace e Generazione rapporti](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html).&quot;

#### Utilizzo delle conversioni view-through di programmi TV collegati nei report

*Pubblicità solo per gli utenti DSP*

È possibile misurare l&#39;efficacia full funnel delle campagne CTV (connected TV) collegando l&#39;esposizione pubblicitaria sui dispositivi CTV alle conversioni in loco. Per visualizzare le metriche di conversione view-through CTV, utilizza la vista Posizionamento o la vista Canale di marketing in Analysis Workspace.

Utilizzo della vista Posizionamento:

1. Includi i posizionamenti di spesa CTV nella visualizzazione di reporting.

1. Includi le metriche desiderate, ad esempio &quot;Impression&quot;, &quot;Clic&quot; e così via.

1. Applica i seguenti filtri:

   Piattaforma annuncio: `Advertising Cloud DSP`

   Pagina di destinazione: `View-Through (CTV)`

Utilizzo della vista Canale di marketing:

1. Includi la dimensione `Marketing Channel`.

1. Includi le metriche desiderate, ad esempio &quot;Impression&quot;, &quot;Clic&quot; e così via.

1. Applica i seguenti filtri:

   Piattaforma annuncio: `Advertising Cloud DSP`

   Pagina di destinazione: `View-Through (CTV)`

### Creazione di dashboard di Adobe Advertising

Per scoprire come tracciare i dati Adobi Advertising rispetto agli obiettivi in Analysis Workspace, guarda il video &quot;[Creare dashboard di Adobe Advertising con Adobe Analytics](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-dashboards-a4adc.html).&quot;

### Utilizzo dell’ID Adobe Advertising per l’analisi dell’ingresso nel sito

Per scoprire come creare un rapporto sulle visite al sito di un Adobe Advertising per monitorare le influenze geografiche, giornaliere e relative all’ora del giorno, guarda il video &quot;[Creare rapporti sulle visite al sito per annunci Adobe](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-site-entry-a4adc.html).&quot;

>[!MORELIKETHIS]
>
>* [Video: Introduzione a [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html)
>* [Prerequisiti e informazioni chiave per l’implementazione [!DNL Analytics for Advertising]](prerequisites.md)
>* [Adobe di ID pubblicitari utilizzati da Analytics](ids.md)
>* [Codice JavaScript per Analytics per Advertising](/help/integrations/analytics/javascript.md)
>* [Varianze di dati previste tra [!DNL Analytics] e pubblicità Adobe](data-variances.md)
>* [Metriche di Adobe Advertising in Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Dati in Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
