---
title: Panoramica [!DNL Analytics for Advertising]
description: Panoramica [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 94558478-ffa6-4b83-bc79-c7589fe0f14c
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '1077'
ht-degree: 0%

---

# Panoramica [!DNL Analytics for Advertising]

*Inserzionisti con DSP pubblicitari e[!DNL Advertising Search, Social, & Commerce]*

[!DNL Analytics for Advertising] integra Adobe Analytics e Adobe Advertising per estendere e migliorare le funzionalità di ogni prodotto.

L’integrazione consente agli inserzionisti di monitorare le interazioni del sito click-through e view-through nelle loro [!DNL Analytics] , consentendo ai marchi di vedere in che modo la spesa pubblicitaria porta al coinvolgimento del sito e a obiettivi aziendali critici.

Inoltre, Adobe Advertising può accedere ai vasti dati di prime parti che [!DNL Analytics] raccoglie tramite [!DNL Analytics] tag già presenti sul sito. Ciò consente una gestione più affidabile dei percorsi, remarketing di prime parti e reporting di siti multimediali a pagamento. Adobe Advertising può utilizzare ulteriormente il [!DNL Analytics] dati per l’ottimizzazione di spesa e offerta.

Se correttamente impiegati, [!DNL Analytics for Advertising] sfoca le linee tra due ruoli tradizionali: gestione dei percorsi pubblicitari (atto di inviare utenti al sito tramite annunci pubblicitari) e comprensione del coinvolgimento del sito tramite analisi web.

Vantaggi principali:

* Invia [!DNL Analytics] segmenti direttamente in Adobe Advertising per il remarketing di siti di prime parti.
* Utilizzo [!DNL Analytics] eventi personalizzati e standard come segnali di conversione per l&#39;ottimizzazione della pubblicità a pagamento.
* Approfitta di [!DNL Analytics] Analysis Workspace per comprendere meglio i punti di ingresso del sito e il comportamento delle visite.
* Consente una più stretta collaborazione tra web analyst e team di media a pagamento.
* Utilizza ID costanti di visualizzazione e click-through di Adobe Advertising in [!DNL Analytics] per comprendere il coinvolgimento del sito.
* Ottimizza i report tradizionali per contenuti multimediali a pagamento in Analysis Workspace con metriche personalizzate, dimensioni personalizzate e attività del sito non raggiungibili durante l’esportazione di dati o pixel su server di annunci o altri DSP.
* Approfitta di [!DNL Analytics] codice già presente sul tuo sito web per il monitoraggio e l&#39;ottimizzazione all&#39;interno di Adobe Advertising.

>[!TIP]
>
> Guarda un [introduzione video a [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html?lang=en#analytics).

## Utilizzo di Analytics per i rapporti sui file multimediali a pagamento

[!DNL Analytics for Advertising] migliora il reporting e le informazioni sul modo in cui la pubblicità guida il comportamento del sito consentendo di:

* Utilizza ID costanti di visualizzazione e click-through di Adobe Advertising in [!DNL Analytics] per comprendere il coinvolgimento del sito.
* Utilizza Analysis Workspace per comprendere meglio i punti di ingresso del sito e il comportamento delle visite. Puoi accedere ai dati dimensionali ed evento dei file multimediali a pagamento, che includono ad Adobe i nomi delle entità delle campagne pubblicitarie (fino a posizionamenti e annunci) e le metriche associate, come clic, impression e costi.

Per utilizzare [!DNL Analytics] come strumento di reporting per file multimediali a pagamento, l’organizzazione deve disporre di un accesso Experience Cloud con accesso ad Analysis Workspace. Il team Advertising di Adobe ti aiuterà a mappare i tuoi dati Pubblicitari di Adobe alle singole suite di rapporti in Analysis Workspace. Puoi inviare dati Adobe Advertising a qualsiasi suite di rapporti, ma devi essere consapevole delle suite di rapporti che sono state mappate su Adobe Advertising e su quelle che non lo hanno fatto. A seconda della suite di rapporti, i dati segnalati potrebbero essere modificati.

[Adobe di ID pubblicitari in [!DNL Analytics]](ids.md) funziona come altre eVar, con scadenza personalizzata e persistente. Per impostazione predefinita, l’intervallo di lookback di attribuzione è impostato su 60 giorni durante l’implementazione di Adobe Advertising. Per modificare questa impostazione, collabora con il team dell&#39;account Adobe.

Ad Adobe, le dimensioni pubblicitarie vengono aggiunte con il suffisso &quot;(AMO ID)&quot; (ad esempio &quot;Tipo di annuncio (AMO ID)&quot;). Vedere &quot;[Metriche pubblicitarie di Adobe in Analysis Workspace](advertising-metrics-in-analytics.md)&quot; per un elenco delle dimensioni disponibili.

>[!NOTE]
>
> Quando visualizzi i dati di Adobe Advertising (o qualsiasi set di dati) in [!DNL Analytics], tieni presente che le metriche e i rapporti si basano sulle regole impostate in [!DNL Analytics]. I dati potrebbero essere diversi da quelli disponibili in altri sistemi di reporting, ad esempio nei report ad server, [!DNL DSP] rapporti o rapporti del motore di ricerca. Per comprendere le differenze di dati in [!DNL Analytics], è necessario sapere alla scadenza dei dati di eVar, cosa definisce una visita, cosa è considerato l’attribuzione di ultimo contatto rispetto all’attribuzione di persistenza totale e altri fattori. Per ulteriori informazioni, consulta [Varianze di dati previste tra [!DNL Analytics] e pubblicità Adobe](data-variances.md).

## Utilizzo di Analytics per alimentare campagne e Portfoli pubblicitari di Adobe

Senza richiedere pixel aggiuntivi, [!DNL Analytics for Advertising] consente una migliore ottimizzazione e una segmentazione del pubblico più semplice inviando due segnali principali ad Adobe Advertising:

* Metriche di conversione da utilizzare come segnali di offerta:
   * metriche standard, ad esempio [!UICONTROL Revenue] e [!UICONTROL Cart Views].
   * metriche di coinvolgimento del sito, come la visualizzazione della pagina e le metriche di visita.
   * metriche personalizzate dei ricavi.
   * metriche di ricavi riservati.
* Segmenti creati in [!DNL Analytics] e pubblicato in Experience Cloud.

   È possibile utilizzare [!DNL Analytics] segmenti per il retargeting di siti di prime parti in [!DNL DSP] e annunci pubblicitari a pagamento.

   ([!DNL Search, Social, & Commerce] Solo per gli inserzionisti con [!DNL Analytics] ma non Audience Manager può anche creare tipi di pubblico basati su tag del sito web Google (elenchi di remarketing) e audience di corrispondenza dei clienti (elenchi dei clienti) da [!DNL Analytics] segmenti condivisi con Experience Cloud.

### Metriche di conversione del sito come segnali di offerta

Puoi utilizzare gli eventi standard e personalizzati da [!DNL Analytics] costruire obiettivi ponderati in pubblicità Adobe. Gli obiettivi informano le decisioni di offerta per il tuo [!DNL DSP] pacchetti e portfolio di ricerca.

>[!NOTE]
>
> Non è possibile mappare le metriche calcolate da [!DNL Analytics] in Adobe Advertising.

Il team Advertising di Adobe ti aiuterà a identificare e mappare gli eventi applicabili alle prestazioni dei media a pagamento in Adobe Advertising, dove appariranno in [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Transaction Properties].

Vedere &quot;[Metriche di Analytics in Pubblicità Adobe](analytics-data-in-advertising.md)&quot; per un elenco delle metriche disponibili.

### Segmenti di Analytics per il retargeting dei siti

Adobe Advertising può acquisire [!DNL Analytics] segmenti a scopo di remarketing per DSP pubblicitari e [!DNL Search, Social, & Commerce] annunci utilizzando l’integrazione nativa di Experience Cloud Audiences tra [!DNL Analytics] e Experience Cloud.

Per accedere al [!DNL Analytics] segmenti, un account inserzionista deve avere [Servizio Experience Cloud ID](https://experienceleague.adobe.com/docs/id-service/using/home.html) abilitato. Quando il servizio ID è abilitato, tutti i segmenti di Experience Cloud (inclusi i segmenti creati in [!DNL Analytics] e pubblicati in Experience Cloud, segmenti creati in Adobe Audience Manager, segmenti creati in Experience Cloud utilizzando [!DNL People core service], e i segmenti creati in Adobe Experience Platform e inviati ad Adobe Advertising tramite Audience Manager) diventano disponibili in Adobe Advertising non appena vengono elaborati.

[!DNL Analytics] I segmenti sono disponibili entro 24 ore e vengono aggiornati quotidianamente.

Per ulteriori informazioni sul servizio pubblico di Experience Cloud, vedi [Tipi di pubblico di Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html).

## Esempi di utilizzo dell’integrazione

### Utilizzo dei dati pubblicitari di Adobe in Analysis Workspace

Per scoprire come utilizzare i dati pubblicitari di Adobe per creare rapporti visivi in Analysis Workspace, guarda il video &quot;[Introduzione a Workspace e reporting](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html).&quot;

### Creazione di dashboard di Adobe Advertising

Per scoprire come tenere traccia dei dati pubblicitari Adobi rispetto agli obiettivi in Analysis Workspace, guarda il video &quot;[Creare dashboard di Adobe Advertising con Adobe Analytics](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-dashboards-a4adc.html).&quot;

### Utilizzo dell’ID pubblicitario Adobe per l’analisi della partecipazione al sito

Per scoprire come creare un report di ingresso del sito pubblicitario di Adobe per monitorare le influenze geografiche, giorno della settimana, ora del giorno, browser e del giorno, guarda il video &quot;[Creazione di report per l&#39;immissione di siti pubblicitari di Adobe](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-site-entry-a4adc.html).&quot;

>[!MORELIKETHIS]
>
>* [Video: Introduzione a [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html)
>* [Prerequisiti e informazioni chiave per l’implementazione [!DNL Analytics for Advertising]](prerequisites.md)
>* [ID pubblicitari di Adobe utilizzati da Analytics](ids.md)
>* [Codice JavaScript per Analytics per la pubblicità](/help/integrations/analytics/javascript.md)
>* [Varianze di dati previste tra [!DNL Analytics] e pubblicità Adobe](data-variances.md)
>* [Metriche pubblicitarie di Adobe in Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Dati in Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)

