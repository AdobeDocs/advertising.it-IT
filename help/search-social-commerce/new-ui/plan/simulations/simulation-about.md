---
title: Informazioni sulle simulazioni
description: Scopri le simulazioni del portfolio.
feature: Search Optimization, Search Portfolios, Search Simulations
hide: true
exl-id: 2fbefee2-f8f7-4b3d-a039-e1ca0236c61a
source-git-commit: 73528e2aa905216584d1aa294f5581d2bca88432
workflow-type: tm+mt
source-wordcount: '1182'
ht-degree: 0%

---

# Informazioni sulle simulazioni

*funzionalità Beta*

I rapporti di simulazione mostrano il valore marginale stimato del costo per obiettivo, il costo, il numero di clic e il valore obiettivo che è possibile aspettarsi per un portfolio a vari livelli di spesa (costo) e i budget giornalieri corrispondenti o altri obiettivi. Facoltativamente, è possibile [personalizzare la visualizzazione](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md) per visualizzare metriche di traffico aggiuntive, impostazioni di simulazione e solo un tipo di simulazione specifico ([!UICONTROL Weekly] o [!UICONTROL Custom]).

<!-- Not available as of 6/21/25:
When the portfolio has a daily budget, you can optionally change the portfolio's spend target to any of the spend targets listed in the simulation.
-->

## Tipi di simulazioni

* Simulazioni settimanali automatizzate

* Simulazioni personalizzate generate dall&#39;utente

### Simulazioni settimanali automatizzate

I rapporti di simulazione vengono eseguiti automaticamente ogni settimana utilizzando le impostazioni correnti del portfolio. Le simulazioni settimanali automatizzate sono disponibili solo per i periodi in cui il portfolio è [ottimizzato o attivo](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md).

#### Simulazioni settimanali scaricate

Ogni simulazione settimanale scaricata è costituita da una cartella di lavoro. Ogni cartella di lavoro include il target per ciascuno dei 20 livelli di passo e il costo previsto, i clic, i ricavi ponderati (valore obiettivo) e le metriche di conversione incluse nell&#39;obiettivo, in base al target corrispondente. Per le prime 20 righe di dati non sono stati applicati vincoli, mentre per le restanti righe di dati sono stati applicati vincoli.

#### Dettagli simulazione settimanale su schermo

I dettagli della simulazione su schermo mostrano informazioni visive e tabulari a livello di portfolio. Per i dati per campagna, gruppi di annunci, unità di offerta o dispositivo, [scarica la simulazione](simulation-download.md).

##### Vista grafico

La visualizzazione grafico mostra il valore obiettivo previsto o un&#39;altra metrica specificata ([!UICONTROL Y-Axis Metric]<!-- I see Objective Value, Cost, Clicks, the metrics in the portfolio's objective, and then a couple of other conversion metrics. Where do the other conversion metrics come from? -->) per il target di spesa per ciascuno dei 20 livelli di spesa. Il punto intermedio di destinazione viene identificato ed è possibile modificare facoltativamente il punto intermedio di destinazione per visualizzare i dati previsti utilizzando tale valore. Tenere premuto il cursore su un punto del grafico per visualizzare i dati relativi a tale punto.

È possibile visualizzare i dati con e senza vincoli applicati, con vincoli applicati e senza vincoli applicati. Quando visualizzate i dati che prendono in considerazione i vincoli, i vincoli applicati vengono identificati sopra il grafico.

##### Vista tabella

La vista a tabella mostra la spesa target per ciascuno dei 20 livelli di spesa. Include inoltre il corrispondente costo stimato, il costo marginale rispetto al valore obiettivo, i clic, il valore obiettivo e le metriche di conversione nell’obiettivo del portfolio per ogni livello di spesa. Il punto intermedio di destinazione viene identificato ed è possibile modificare facoltativamente il punto intermedio di destinazione per visualizzare i dati previsti utilizzando tale valore.

È possibile visualizzare i dati con e senza vincoli applicati, con vincoli applicati e senza vincoli applicati. Quando visualizzate i dati che prendono in considerazione i vincoli, i vincoli applicati vengono identificati sopra il grafico.

##### Impostazioni simulazione

Le impostazioni di simulazione vengono visualizzate in sola lettura sotto il grafico o la tabella.

##### Impostazioni Portfolio

Per visualizzare le impostazioni di sola lettura per il portfolio applicabile, fare clic su **[!UICONTROL Portfolio Settings]** in alto a destra.

### Simulazioni personalizzate generate dall&#39;utente

È possibile creare un report di simulazione personalizzato per un singolo portfolio [ottimizzato o attivo](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md) utilizzando le impostazioni correnti del portfolio oppure le impostazioni personalizzate del portfolio, con o senza vincoli a livello di unità di offerta applicati, per visualizzare i risultati che tali impostazioni produrrebbero senza modificarle. Ad esempio, puoi creare una simulazione personalizzata per vedere l’effetto dell’utilizzo di una strategia di spesa o di un budget di apprendimento diverso senza considerare i vincoli attivi sulle unità di offerta nel portfolio. Puoi visualizzare le prestazioni stimate a livello di portfolio, campagna, unità di offerta e dispositivo.

#### Simulazioni personalizzate scaricate

Ogni simulazione personalizzata scaricata è costituita da una cartella di lavoro. Ogni cartella di lavoro include un foglio di lavoro per ogni livello di simulazione di entità specificato (portfolio, campagne, gruppi di annunci, unità di offerta) quando i dati sono disponibili per tale livello. Quando si specificano dati a livello di dispositivo, ogni foglio di lavoro include una colonna [!UICONTROL Device]. Ogni foglio di lavoro include una riga con i dati per ogni entità applicabile e (se specificato per il rapporto) e il tipo di dispositivo per ciascuno dei 20 passaggi (ad esempio, una riga per campagna). I dati in ogni riga includono il costo marginale previsto per ricavi, costo, clic, ricavi ponderati (valore obiettivo), il tipo di dispositivo e le metriche di conversione incluse nell’obiettivo, in base al target corrispondente. Il foglio di lavoro a livello di portfolio include anche la destinazione per i livelli di fase e il foglio di lavoro a livello di entità include la rete di annunci, il conto, la campagna e (se applicabile) il gruppo di annunci.   <!-- I don't see a Bid Units tab when specified; clarify when it is and isn't included -->

#### Dettagli della simulazione personalizzata su schermo

I dettagli della simulazione su schermo mostrano informazioni visive e tabulari a livello di portfolio. Per i dati per campagna, gruppi di annunci, unità di offerta o dispositivo, [scarica la simulazione](simulation-download.md).

#### Vista grafico

La visualizzazione grafico mostra il valore obiettivo previsto o un&#39;altra metrica specificata ([!UICONTROL Y-Axis Metric]<!-- I see Objective Value, Cost, Clicks, the metrics in the portfolio's objective, and then a couple of other conversion metrics. Where do the other conversion metrics come from? -->) per il target di spesa per il numero specificato di livelli di spesa (passaggi) per la simulazione. Viene identificato il punto intermedio di destinazione. Tenere premuto il cursore su un punto del grafico per visualizzare i dati relativi a tale punto.

Quando la simulazione è stata creata prendendo in considerazione i vincoli, i vincoli applicati vengono identificati sopra il grafico.

##### Vista tabella

La vista tabella mostra la spesa target per ciascuno dei livelli di spesa specificati (passaggi) per la simulazione. Mostra anche il costo stimato corrispondente, il costo marginale rispetto al valore obiettivo, i clic, il valore obiettivo e le metriche di conversione nell’obiettivo del portfolio per ogni livello di spesa. Viene identificato il punto intermedio di destinazione.

Quando la simulazione è stata creata prendendo in considerazione i vincoli, i vincoli applicati vengono identificati sopra il grafico.

##### Impostazioni simulazione

Le impostazioni di simulazione vengono visualizzate in sola lettura sotto il grafico o la tabella.

##### Impostazioni Portfolio

Per visualizzare le impostazioni di sola lettura per il portfolio applicabile, fare clic su **[!UICONTROL Portfolio Settings]** in alto a destra.

## Visualizzazione [!UICONTROL Simulations]

Nella visualizzazione [!UICONTROL Simulations] sono elencate le simulazioni settimanali e personalizzate. L&#39;amministratore e alcuni altri tipi di utenti<!-- Verify which --> possono visualizzare simulazioni personalizzate create da altri utenti. Tutti gli altri utenti possono visualizzare solo le simulazioni personalizzate create.

La tabella di dati include l&#39;avanzamento di ogni simulazione, una colonna [!UICONTROL Target Midpoint] compilata per ogni riga e colonne per le previsioni di costo/impression/clic/valore obiettivo, i valori effettivi e la precisione. Facoltativamente, puoi aggiungere colonne personalizzate aggiuntive (comprese le metriche di incremento, ad esempio il valore obiettivo effettivo diviso per il costo).

### Azioni disponibili {#simulations-actions}

* [Personalizzare la visualizzazione](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md) per includere ulteriori metriche, incluse le impression stimate, il costo effettivo, i clic, le impression e il valore obiettivo, il valore costo-obiettivo, la precisione del costo, la precisione dei clic e la precisione del valore obiettivo e la differenza (delta) tra il valore obiettivo previsto ed effettivo e il valore costo-obiettivo. È inoltre possibile includere colonne per la maggior parte delle impostazioni di simulazione e per il tipo di simulazione ([!UICONTROL Custom] o [!UICONTROL Weekly]).

* [Generare o eseguire nuovamente una simulazione personalizzata](simulation-create.md) per un singolo portfolio. È possibile creare una nuova simulazione o rigenerare una simulazione esistente nell&#39;elenco.

* [Visualizza sullo schermo una simulazione settimanale o personalizzata](simulation-view.md).

* [Scarica simulazioni settimanali e personalizzate](simulation-download.md) come [!DNL Microsoft Excel] cartelle di lavoro in file ZIP.

* Utilizzando il pulsante [!UICONTROL Spend Planner], apri lo strumento legacy Spend Recommendation, che ti consente di identificare la distribuzione ottimale della spesa tra i portfolio.

## Best practice

Monitora i rapporti di simulazione nelle seguenti situazioni:

* Prima di avviare un portfolio per stimarne le prestazioni con le impostazioni di portfolio corrispondenti, utilizza almeno due settimane di dati. Se i risultati della simulazione indicano prestazioni inferiori a quelle previste in base ai dati storici per le campagne incluse, esamina e risolvi i problemi prima di lanciare il portfolio.

* Dopo qualsiasi modifica importante apportata a un portfolio, ad esempio l’aggiunta di una campagna o la modifica dell’obiettivo. Se apporti modifiche alla data di inizio della modellazione del portfolio, al peso di una metrica di conversione o al valore di clic di un obiettivo, attendi che dopo il giorno 17:00 PST venga eseguita la simulazione, quando saranno disponibili modelli aggiornati di costi e ricavi.

* Periodicamente per monitorare le tendenze delle prestazioni a livello di metrica di conversione.

>[!MORELIKETHIS]
>
>* [Esegui o riesegui una simulazione](simulation-create.md)
>* [Visualizza dettagli simulazione](simulation-view.md)
>* [Scarica simulazioni](simulation-download.md)
