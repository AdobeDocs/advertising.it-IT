---
title: (Nuova interfaccia) Informazioni su Advertising
description: Scopri come configurare e visualizzare le dashboard di insight per annunci pubblicitari per migliorare la precisione, le prestazioni, le simulazioni, i limiti di budget e le conversioni dei modelli.
feature: Search Advertising Insights
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: bc8b5578-58f6-5342-a640-fce94e5ff4a7
    internal-label: Search Advertising Insights
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: 54920f5e0e08c1bf6f960b4d96aa4161dfa11143
workflow-type: tm+mt
source-wordcount: '1217'
ht-degree: 0%
---
# (Nuova interfaccia) Informazioni su Advertising

Advertising Insights presenta dati visivi e fruibili per aiutarti a valutare le prestazioni del portfolio, identificare i problemi di ottimizzazione e confrontare i dati di conversione. Ogni insight viene generato su richiesta e visualizzato come dashboard su schermo.

La visualizzazione **[!UICONTROL Reports]>[!UICONTROL Insights]** visualizza le informazioni disponibili in **[!UICONTROL Dashboards]**. Intestazione pagina: **[!UICONTROL Advertising Insights]**.

>[!NOTE]
>
>Questa pagina descrive le dashboard di insight nella nuova interfaccia utente beta. La disponibilità dipende dal tuo accesso e dalle informazioni disponibili per l’inserzionista selezionato. Le [informazioni legacy su Advertising](/help/search-social-commerce/advertising-insights/insight-about.md) includono un diverso set di analisi e procedure per i file generati.

## Tipi di informazioni {#insight-types}

| Insight | Descrizione |
| --- | --- |
| [!UICONTROL Model Accuracy] | Identifica come Search, Social e Commerce consentono di prevedere costi e ricavi per un portfolio. Puoi esaminare la precisione del modello a livello di portfolio, rete di annunci e campagna. |
| [!UICONTROL Performance Insights] | Confronta le prestazioni del portfolio prima e dopo una modifica dello stato di ottimizzazione, una modifica obiettivo o una data specificata. Il dashboard include riepiloghi delle prestazioni, un controllo delle modifiche che influiscono sull’ottimizzazione, confronti tra campagne, tendenze e analisi del valore obiettivo. |
| [!UICONTROL Portfolio Simulation Analysis] | Confronta una simulazione personalizzata esistente con le prestazioni effettive. Puoi esaminare i dati del portfolio e della campagna, analizzare la precisione della simulazione ed esplorare le prestazioni stimate a diversi livelli di spesa target. |
| [!UICONTROL Campaign Budget Cap Analysis] | Indica se la spesa di un portfolio era limitata dai limiti di budget della campagna. La dashboard include spese limitate, campagne interessate, impression perse stimate, tendenze giornaliere e giornaliere della settimana e consigli per le impostazioni del portfolio. |
| [!UICONTROL Modeled Conversions] | Confronta i valori di conversione di Adobe con i valori riportati dalla rete di annunci, inclusi i dati modellati. Puoi analizzare account, portfolio o campagne e confrontare i valori misurati e modellati da Adobe e Adobe con i valori riportati dall’editore. |
| [!UICONTROL Delayed Revenue Analysis] | Misura il ritardo di conversione (il tempo trascorso tra un clic su un annuncio o una visualizzazione view-through e una conversione successiva) e ne mostra l’impatto sul valore obiettivo, sul ritorno sull’investimento (ROI) e sulla precisione del modello. L’analisi è disponibile solo per i portfolio con attribuzione di ricavi basata su clic o view-through. |

## Generare un insight {#insight-generate}

1. Nel menu principale, fare clic su **[!UICONTROL Reports]>[!UICONTROL Insights]**.

1. Fai clic sull’insight da generare.

1. Nel pannello **[!UICONTROL Configure]**, specifica le [impostazioni insight](#insight-settings).

1. Fare clic su **[!UICONTROL Generate Insight]**.

   Il pannello di configurazione si chiude e nel quadro comandi viene visualizzata l&#39;analisi.

1. Rivedi i [risultati insight](#insight-results).

Per modificare le impostazioni, fare clic su **[!UICONTROL Configure]**, modificare i valori e fare di nuovo clic su **[!UICONTROL Generate Insight]**. Per tornare all&#39;elenco di insight, fare clic su **[!UICONTROL Analysis List]** nella breadcrumb.

## Impostazioni di Insight {#insight-settings}

### Precisione del modello {#model-accuracy-settings}

* **[!UICONTROL Portfolios]:** Selezionare un portfolio.

* **[!UICONTROL Choose Revenue Type]:** Selezionare **[!UICONTROL Actual Revenue]** (impostazione predefinita) o **[!UICONTROL Delayed Revenue]**.

* **[!UICONTROL Date Range]:** Selezionare le date da analizzare. Vedi [Impostazioni intervallo di date](#date-range-settings).

### Informazioni sulle prestazioni {#performance-insights-settings}

* **[!UICONTROL Portfolios]:** Selezionare un portfolio.

* **[!UICONTROL Revenue Type]:** Selezionare **[!UICONTROL Actual Revenue]** (impostazione predefinita) o **[!UICONTROL Delayed Revenue]**.

* **Data evento:** Selezionare il tipo di data in base al quale confrontare le prestazioni:

  * **[!UICONTROL Optimization Status Change (last 90 days)]** (impostazione predefinita): selezionare una data di modifica dello stato di ottimizzazione disponibile per il portfolio.

  * **[!UICONTROL Objective Change Date (last 90 days)]:** Selezionare una data di modifica obiettivo disponibile per il portfolio.

  * **[!UICONTROL Specific Date]:** Specificare una data utilizzando la selezione data.

  Seleziona la data dell’evento prima di configurare i periodi di confronto. Se non sono disponibili date evento per il portfolio selezionato, è possibile utilizzare **[!UICONTROL Specific Date]**.

* **[!UICONTROL Pre Days]:** Specificare il periodo precedente alla data dell&#39;evento:

  * Selezionare **[!UICONTROL 7]** (impostazione predefinita), **[!UICONTROL 14]** o **[!UICONTROL 30]**.

  * Selezionare **[!UICONTROL Pre Start Date]** e specificare **[!UICONTROL Custom Pre Date]**.

  * Selezionare **[!UICONTROL Custom Pre Days]** e immettere un numero positivo di giorni.

* **[!UICONTROL Post Days]:** Specificare il periodo successivo alla data dell&#39;evento:

  * Selezionare **[!UICONTROL 7]** (impostazione predefinita), **[!UICONTROL 14]** o **[!UICONTROL 30]**.

  * Selezionare **[!UICONTROL Post End Date]** e specificare **[!UICONTROL Custom Post Date]**.

  * Selezionare **[!UICONTROL Custom Post Days]** e immettere un numero positivo di giorni.

  La data dell’evento non è inclusa in nessuno dei periodi di confronto.

* **[!UICONTROL Date Exclusion]:** (Facoltativo) Escludere le date dall&#39;analisi:

  1. Fare clic su **[!UICONTROL Select Dates]**.

  1. Seleziona le date da escludere:

     * Fai clic su singole date per selezionarle o deselezionarle.

     * Tenere premuto **[!UICONTROL Shift]** durante la selezione di un intervallo.

     * Per rimuovere tutte le esclusioni, fare clic su **[!UICONTROL Clear All]**.

  1. Al termine, fai clic su **[!UICONTROL Done]**.

### Analisi simulazione Portfolio {#simulation-settings}

* **[!UICONTROL Portfolios]:** Selezionare un portfolio con una simulazione personalizzata esistente.

* **[!UICONTROL Simulation Date]:** Selezionare la data della simulazione da analizzare. Se per tale data sono disponibili più simulazioni, selezionare anche la simulazione per nome.

  Se non sono disponibili simulazioni personalizzate, [genera una simulazione personalizzata](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-create-simulation.md) prima di utilizzare questa insight.

* **[!UICONTROL Actual Days]:** Selezionare **[!UICONTROL 7]** (impostazione predefinita), **[!UICONTROL 14]** o **[!UICONTROL 30]** giorni di dati delle prestazioni effettive. Per specificare un altro numero, selezionare **[!UICONTROL Enter Actual Days]** e immettere un valore compreso tra 1 e 90.

* **[!UICONTROL Type]:** Seleziona **[!UICONTROL Transaction Date]** (impostazione predefinita) o **[!UICONTROL Click Date]** per l&#39;attribuzione di conversione.

### Analisi del tetto del budget della campagna {#budget-cap-settings}

* **[!UICONTROL Portfolio]:** Selezionare un portfolio.

* **[!UICONTROL Date Range]:** Selezionare le date da analizzare. Vedi [Impostazioni intervallo di date](#date-range-settings).

### Conversioni modellate {#modeled-conversions-settings}

* **[!UICONTROL Analysis Level]:** Selezionare **[!UICONTROL Account]**, **[!UICONTROL Portfolio]** (impostazione predefinita) o **[!UICONTROL Campaign]**.

* **[!UICONTROL Accounts]**, **[!UICONTROL Portfolios]** o **[!UICONTROL Campaigns]:** Selezionare le entità applicabili per il livello di analisi. Potete selezionare più entità.

* **[!UICONTROL Date Range]:** Selezionare le date da analizzare. Vedi [Impostazioni intervallo di date](#date-range-settings).

* **[!UICONTROL Adobe Conversion]:** Seleziona la proprietà di conversione Adobe da confrontare.

* **[!UICONTROL Publisher Conversion]:** Selezionare la proprietà di conversione dell&#39;editore da confrontare.

  Le proprietà di conversione disponibili dipendono dal livello di analisi, dalle entità selezionate e dall&#39;intervallo di date. Per il confronto sono necessarie entrambe le proprietà di conversione.

### Analisi dei ricavi ritardati {#delayed-revenue-settings}

* **[!UICONTROL Portfolios]:** Seleziona un portfolio con attribuzione di ricavi basata su clic o view-through.

* **[!UICONTROL Date Range]:** Selezionare le date da analizzare. Vedi [Impostazioni intervallo di date](#date-range-settings).

### Impostazioni intervallo di date {#date-range-settings}

Per informazioni dettagliate con un&#39;impostazione **[!UICONTROL Date Range]**, selezionare **[!UICONTROL Last 7 days]** (impostazione predefinita), **[!UICONTROL Last 14 days]** o **[!UICONTROL Last 30 days]**.

Per specificare un altro periodo, selezionare **[!UICONTROL Custom Date]** e immettere **[!UICONTROL Start Date]** e **[!UICONTROL End Date]**. Puoi selezionare le date negli ultimi 90 giorni, fino alla data corrente.

## Visualizza risultati insight {#insight-results}

### Precisione del modello {#model-accuracy-results}

Rivedi i dettagli del portfolio e utilizza le seguenti schede:

* **[!UICONTROL Portfolio]:** Verificare la precisione del modello a livello di portfolio e i confronti di budget.

* **[!UICONTROL Ad Network]:** Verifica la precisione del modello e i confronti del budget per rete di annunci.

* **[!UICONTROL Campaigns]:** Verificare la precisione del modello a livello di campagna e il target rispetto alle prestazioni effettive.

* **[!UICONTROL Playground Beta]:** Confronta la precisione del modello per più campagne.

Per i grafici di precisione delle campagne, selezionare **[!UICONTROL Comparison Options]** e **[!UICONTROL Campaign]**. In **[!UICONTROL Playground Beta]** è possibile selezionare più campagne. Fare clic su **[!UICONTROL Table View]** per passare da un grafico ai dati sottostanti.

### Informazioni sulle prestazioni {#performance-insights-results}

Il dashboard mostra **[!UICONTROL Pre Period]** e **[!UICONTROL Post Period]**, le metriche delle prestazioni aggregate per entrambi i periodi e i dettagli del portfolio.

**[!UICONTROL Audit Trail]** riepiloga le modifiche ai fattori che influiscono sull&#39;ottimizzazione, inclusi il budget del portfolio, la strategia di spesa, la spesa minima per la campagna e il limite di spesa multiplo. Quando i dettagli delle modifiche sono disponibili, fare clic su **[!UICONTROL View Details]** per esaminarli.

Utilizza le schede **[!UICONTROL Comparative Overview]**, **[!UICONTROL Campaigns Comparison]**, **[!UICONTROL Trends & Patterns]**, **[!UICONTROL Deep Analysis]** e **[!UICONTROL Objective Value And Analysis]** per esplorare il confronto.

### Analisi simulazione Portfolio {#simulation-results}

Rivedi i dettagli della simulazione e utilizza le seguenti schede:

* **[!UICONTROL Portfolio]:** Esaminare i dati di simulazione a livello di portfolio. All’interno di questa scheda:

  * **[!UICONTROL Simulation Data]** mostra le metriche di simulazione e le prestazioni della spesa di destinazione.

  * **[!UICONTROL Simulation Vs Actual]** confronta le prestazioni simulate con quelle effettive.

  * **[!UICONTROL Try New Target]** consente di immettere una spesa target in **[!UICONTROL Explore Target Spend]** per visualizzare i clic stimati, i costi e i ricavi. Si tratta di un’analisi delle prestazioni stimate che non modifica l’obiettivo di spesa del portafoglio.

* **[!UICONTROL Campaigns]:** Verificare i confronti di simulazione a livello di campagna.

* **[!UICONTROL Accuracy Analysis]:** Verificare la precisione della simulazione.

### Analisi del tetto del budget della campagna {#budget-cap-results}

Rivedi i dettagli del portfolio e le metriche di riepilogo:

* **[!UICONTROL Total Capped Spend]:** La percentuale di spesa nei giorni in cui sono stati raggiunti i budget delle campagne.

* **[!UICONTROL Capped Campaigns]:** Numero di campagne che hanno raggiunto il budget almeno una volta.

* **[!UICONTROL Est. Lost Impressions]:** impression stimate mancate a causa di limiti di budget.

* **[!UICONTROL Peak Capping Day]:** Il giorno della settimana con la spesa più limitata.

I grafici **[!UICONTROL Spend on Capped Campaigns by Day]** e **[!UICONTROL Capped Spend by Weekday]** mostrano le tendenze relative ai limiti. Rivedi **[!UICONTROL Capped Campaign Performance]** per i dettagli della campagna e **[!UICONTROL Portfolio Settings Recommendations]** per le modifiche alle impostazioni suggerite.

### Conversioni modellate {#modeled-conversions-results}

Esamina le tabelle seguenti per le entità e l’intervallo di date selezionati:

* **[!UICONTROL Adobe Measured vs Publisher Conversions]:** confronta i valori di conversione misurati direttamente da Adobe con i valori riportati dall&#39;editore, che includono dati misurati e modellati.

* **[!UICONTROL Adobe Modeled vs Publisher Conversions]:** confronta i valori di conversione misurati e modellati da Adobe con i valori segnalati da publisher.

Entrambe le tabelle includono il nome e l’ID dell’entità, il valore Adobe, il valore riportato dall’editore, la differenza assoluta e la differenza percentuale.

Se non sono disponibili dati, verifica di aver selezionato sia le proprietà di conversione che i dati per le entità e l’intervallo di date selezionati.

### Analisi dei ricavi ritardati {#delayed-revenue-results}

**[!UICONTROL Key Insights Summary]** mostra i ricavi ponderati previsti (ora denominati &quot;[valore obiettivo](/help/search-social-commerce/glossary.md#o-p)&quot;), il ROI e le informazioni sulla precisione del modello.

La sezione **[!UICONTROL Conversion Lag Breakdown by Revenue Property]** mostra la percentuale di conversioni realizzate il giorno 0 e entro i giorni 3, 7, 14 e 28 per ogni proprietà di ricavo.

In **[!UICONTROL Performance Over Time]**, selezionare **[!UICONTROL Objective Value]**, **[!UICONTROL ROI]** o **[!UICONTROL Model Accuracy]** per confrontare le prestazioni previste, la data della transazione e la data di clic. Fare clic su **[!UICONTROL Table View]** per passare dal grafico ai dati sottostanti.

In **[!UICONTROL Metrics Definitions]**, fare clic su **[!UICONTROL Show]** per informazioni sulle date e le metriche utilizzate nell&#39;analisi oppure su **[!UICONTROL Hide]** per comprimerle.

Se l’analisi non è applicabile, seleziona un portfolio con attribuzione di ricavi basata su clic o view-through. Se non sono disponibili dati, verifica che siano presenti dati per il portfolio e l’intervallo di date selezionati.
