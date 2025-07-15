---
title: Informazioni sulle simulazioni
description: Scopri le simulazioni del portfolio.
feature: Search Optimization, Search Portfolios, Search Simulations
hide: true
source-git-commit: 62de95d7e3d21ae6c7f0a6f40e97352af71411e1
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 0%

---

# Informazioni sulle simulazioni

*funzionalità Beta*

I rapporti di simulazione mostrano il valore marginale stimato del costo per obiettivo, il costo, il numero di clic e il valore obiettivo che è possibile aspettarsi per un portfolio a vari livelli di spesa (costo) e i budget giornalieri corrispondenti o altri obiettivi. Facoltativamente, è possibile personalizzare la visualizzazione <!-- add link --> per visualizzare metriche di traffico aggiuntive, impostazioni di simulazione e solo un tipo di simulazione specifico ([!UICONTROL Weekly] o [!UICONTROL Custom]).

<!-- Not available as of 6/21/25:
When the portfolio has a daily budget, you can optionally change the portfolio's spend target to any of the spend targets listed in the simulation.
-->

## Tipi di simulazioni

* **Simulazioni settimanali automatizzate:** I report di simulazione vengono eseguiti automaticamente ogni settimana utilizzando le impostazioni di portfolio correnti. Le simulazioni settimanali automatizzate sono disponibili solo per i periodi in cui il portfolio è [ottimizzato o attivo](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md).

  Ogni simulazione settimanale scaricata è costituita da una cartella di lavoro. Ogni cartella di lavoro include il target per ciascuno dei 20 livelli di passo e il costo previsto, i clic, i ricavi ponderati (valore obiettivo) e le metriche di conversione incluse nell&#39;obiettivo, in base al target corrispondente. Per le prime 20 righe di dati non sono stati applicati vincoli, mentre per le restanti righe di dati sono stati applicati vincoli.

* **Simulazioni personalizzate generate dall&#39;utente:** È possibile creare un report di simulazione personalizzato per un singolo portfolio [ottimizzato o attivo](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md) utilizzando le impostazioni correnti del portfolio oppure le impostazioni personalizzate del portfolio per visualizzare i risultati che tali impostazioni produrrebbero senza modificarle. Ad esempio, puoi creare una simulazione personalizzata per vedere l&#39;effetto dell&#39;utilizzo di una strategia di spesa o di un budget di apprendimento diverso<!-- Not available yet:  , or without considering active constraints on bid units in the portfolio-->. Puoi visualizzare le prestazioni stimate a livello di portfolio, campagna, unità di offerta e dispositivo. Le simulazioni personalizzate ereditano l’impostazione dei vincoli di spesa dal portfolio.

  >[!NOTE]
  >
  > Il nuovo modulo di simulazione personalizzato utilizza le stesse impostazioni del modulo legacy, con la differenza che eredita le informazioni sui vincoli di unità di offerta dalle impostazioni del portfolio. Non puoi ignorare i vincoli di unità di offerta, come invece hai fatto nella precedente pagina delle impostazioni di simulazione personalizzata.

  Ogni simulazione personalizzata scaricata è costituita da una cartella di lavoro. Ogni cartella di lavoro include un foglio di lavoro per ogni livello di simulazione di entità specificato (portfolio, campagne, gruppi di annunci, unità di offerta) quando i dati sono disponibili per tale livello. Quando si specificano dati a livello di dispositivo, ogni foglio di lavoro include una colonna [!UICONTROL Device]. Ogni foglio di lavoro include una riga con i dati per ogni entità applicabile e (se specificato per il rapporto) e il tipo di dispositivo per ciascuno dei 20 passaggi (ad esempio, una riga per campagna). I dati in ogni riga includono il costo marginale previsto per ricavi, costo, clic, ricavi ponderati (valore obiettivo), il tipo di dispositivo e le metriche di conversione incluse nell’obiettivo, in base al target corrispondente. Il foglio di lavoro a livello di portfolio include anche la destinazione per i livelli di fase e il foglio di lavoro a livello di entità include la rete di annunci, il conto, la campagna e (se applicabile) il gruppo di annunci.   <!-- I don't see a Bid Units tab when specified; clarify when it is and isn't included -->

## Visualizzazione [!UICONTROL Simulations]

Nella visualizzazione [!UICONTROL Simulations] sono elencate le simulazioni settimanali e personalizzate. L&#39;amministratore e alcuni altri tipi di utenti<!-- Verify which --> possono visualizzare simulazioni personalizzate create da altri utenti. Tutti gli altri utenti possono visualizzare solo le simulazioni personalizzate create.

La tabella di dati include l&#39;avanzamento di ogni simulazione, una colonna [!UICONTROL Target Midpoint] compilata per ogni riga e colonne per le previsioni di costo/impression/clic/valore obiettivo, i valori effettivi e la precisione. Facoltativamente, puoi aggiungere colonne personalizzate aggiuntive (comprese le metriche di incremento, ad esempio il valore obiettivo effettivo diviso per il costo).

### Azioni disponibili {#simulations-actions}

* [Personalizzare la visualizzazione](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md) per includere ulteriori metriche, incluse le impression stimate, il costo effettivo, i clic, le impression e il valore obiettivo, il valore costo-obiettivo, la precisione del costo, la precisione dei clic e la precisione del valore obiettivo e la differenza (delta) tra il valore obiettivo previsto ed effettivo e il valore costo-obiettivo. È inoltre possibile includere colonne per la maggior parte delle impostazioni di simulazione e per il tipo di simulazione ([!UICONTROL Custom] o [!UICONTROL Weekly]).

* [Generare o eseguire nuovamente una simulazione personalizzata](simulation-create.md) per un singolo portfolio. È possibile creare una nuova simulazione o rigenerare una simulazione esistente nell&#39;elenco.

* [Scarica simulazioni settimanali e personalizzate](simulation-download.md) come [!DNL Microsoft Excel] cartelle di lavoro in file ZIP.

* Utilizzando il pulsante [!UICONTROL Spend Planner], apri lo strumento legacy Spend Recommendation, che ti consente di identificare la distribuzione ottimale della spesa tra i portfolio.

## Best practice

Monitora i rapporti di simulazione nelle seguenti situazioni:

* Prima di avviare un portfolio per stimarne le prestazioni con le impostazioni di portfolio corrispondenti, utilizza almeno due settimane di dati. Se i risultati della simulazione indicano prestazioni inferiori a quelle previste in base ai dati storici per le campagne incluse, esamina e risolvi i problemi prima di lanciare il portfolio.

* Dopo qualsiasi modifica importante apportata a un portfolio, ad esempio l’aggiunta di una campagna o la modifica dell’obiettivo. Se apporti modifiche alla data di inizio della modellazione del portfolio, al peso di una metrica di conversione o al valore di clic di un obiettivo, attendi fino alle 17:00 PST del giorno successivo per eseguire la simulazione, quando sono disponibili modelli aggiornati di costi e ricavi.

* Periodicamente per monitorare le tendenze delle prestazioni a livello di metrica di conversione.

>[!MORELIKETHIS]
>
>* [Esegui o riesegui una simulazione](simulation-create.md)
>* [Scarica simulazioni](simulation-download.md)
