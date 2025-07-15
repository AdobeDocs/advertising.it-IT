---
title: (Nuova interfaccia) Visualizza dettagli sulle prestazioni del portfolio
description: Scopri come visualizzare i dettagli delle prestazioni del portfolio, comprese le metriche effettive e previste a livello di portfolio e per ogni campagna assegnata.
feature: Search Portfolios, Search Optimization
hide: true
source-git-commit: 62de95d7e3d21ae6c7f0a6f40e97352af71411e1
workflow-type: tm+mt
source-wordcount: '638'
ht-degree: 0%

---

# (Nuova interfaccia) Visualizza dettagli sulle prestazioni del portfolio

*funzionalità Beta*

<!-- Verify all, including why (if) the first report is for active and optimized portfolios(?), and why the other reports are for active portfolios, not optimized ones -->

La visualizzazione dei dettagli del portfolio include le seguenti informazioni su un portfolio:

* I valori effettivi e previsti per un massimo di tre metriche delle prestazioni. I rapporti includono i valori delle metriche totali per il portfolio e la suddivisione della metrica per data.<!-- Not for active portfolios only?  -->

* Dati di accuratezza del modello per i portfolio attivi, che mostrano quanto i modelli si sono discostati dalle previsioni. Il rapporto mostra la precisione complessiva dei costi giornalieri o continui di sette giorni, la precisione dei clic e la precisione del valore obiettivo.

  È possibile visualizzare i dati in base alla data di clic (impostazione predefinita) o alla data della transazione.   È inoltre possibile visualizzare i dati come grafico di tendenza (impostazione predefinita) o come tabella.

* La spesa target rispetto alla spesa effettiva per i portafogli attivi. Facoltativamente, puoi anche includere i budget totali per le campagne per il portfolio.

* Precisione delle previsioni di costo, clic o [valore obiettivo](/help/search-social-commerce/glossary.md#o-p) per i portfolio attivi per rete di annunci.<!-- Verify -->

* Impostazioni portfolio.

  Facoltativamente, puoi aprire le impostazioni del portfolio per modificarle.

## Aprire i dettagli sulle prestazioni di un portfolio

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Portfolios]**.

1. Fai clic sul nome del portfolio.

1. (Facoltativo) Dal menu **[!UICONTROL Granularity]**, modificare la granularità dei dati tra *[!UICONTROL Daily],* *[!UICONTROL Weekly],* o *[!UICONTROL Monthly].*

1. (Facoltativo) Per modificare l&#39;intervallo di date per i dettagli del portfolio, fare clic sull&#39;intervallo di date in alto a destra, specificare l&#39;intervallo di date, quindi fare clic su **[!UICONTROL Apply]**.

## Personalizza la scheda [!UICONTROL Portfolio Overview]

* (Facoltativo) Per personalizzare i report [!UICONTROL Portfolio Performance], eseguire una delle operazioni seguenti:

   * Per modificare le metriche delle prestazioni utilizzate sia per le metriche totali che per quelle dettagliate, fare clic su **[!UICONTROL Metrics]** e selezionare fino a tre metriche.

     Le metriche predefinite sono *[!UICONTROL Cost]*, *[!UICONTROL Clicks]* e *[!UICONTROL Objective Value]*.<!-- What else is available: the advertiser's revenue metrics? Anything else from the ad networks? -->

   * Per le metriche dettagliate:

      * Spostare l&#39;opzione accanto a **[!UICONTROL Display predictions]** per mostrare o nascondere i valori delle metriche previsti.

      * Passare dalla visualizzazione grafico (![Visualizzazione grafico](/help/search-social-commerce/assets/chart-view.png "Visualizzazione grafico")) alla visualizzazione tabella (![Vista tabella](/help/search-social-commerce/assets/table-view.png "Vista tabella")).

      * (Nella visualizzazione grafico) Per visualizzare i dati relativi a un punto qualsiasi del grafico, tenere premuto il cursore su tale punto.

* (Facoltativo) Per personalizzare il grafico di tendenza [!UICONTROL Model accuracy], eseguire una delle operazioni seguenti:

   * Passare dalla visualizzazione grafico (![Visualizzazione grafico](/help/search-social-commerce/assets/chart-view.png "Visualizzazione grafico")) alla visualizzazione tabella (![Vista tabella](/help/search-social-commerce/assets/table-view.png "Vista tabella")).

   * Passare dalla visualizzazione dei dati di *[!UICONTROL Click Date]* a quella di *[!UICONTROL Transaction Date]*.

   * Passare dalla visualizzazione dei dati relativi a *[!UICONTROL Daily Accuracy]* a quella di *[!UICONTROL 7 Day Rolling Accuracy]*.

     [!UICONTROL 7 Day Rolling Accuracy] è la precisione media della previsione per i sette giorni precedenti, espressa in percentuale. Ad esempio, il valore per l’8 maggio 2025 corrisponde alla precisione media per il periodo dal 1° maggio al 7 maggio 2025.

   * (Nella visualizzazione grafico) Per visualizzare i dati relativi a un punto qualsiasi del grafico, tenere premuto il cursore su tale punto.

* (Facoltativo) Per personalizzare il grafico di tendenza [!UICONTROL Target vs actual spend], eseguire una delle operazioni seguenti:

   * Sposta il parametro accanto a **[!UICONTROL Display budget]** per mostrare o nascondere il budget totale della campagna per ogni data.

   * Per visualizzare i dati relativi a un punto qualsiasi del grafico, posizionare il cursore su tale punto.

* (Facoltativo) Per personalizzare il grafico di tendenza [!UICONTROL Network Accuracy], eseguire una delle operazioni seguenti:

   * Modificare la metrica riportata in *[!UICONTROL Cost]*, *[!UICONTROL Clicks]* o *[!UICONTROL Objective Value]*.

   * Per visualizzare i dati relativi a un punto qualsiasi del grafico, posizionare il cursore su tale punto.

## Elencare le campagne nel portfolio

* Fare clic sulla scheda **[!UICONTROL Campaigns]**.

## Elencare i gruppi di annunci nel portfolio

* Per visualizzare tutti i gruppi di annunci di una campagna all&#39;interno del portfolio, fare clic sulla scheda **[!UICONTROL Campaigns]** e quindi sul nome della campagna.

## Elencare le parole chiave nel portfolio

* Per visualizzare tutte le parole chiave nel portfolio, fare clic sulla scheda **[!UICONTROL Keywords]**.

* Per visualizzare tutte le parole chiave di un gruppo di annunci all&#39;interno del portfolio, fare clic sulla scheda **[!UICONTROL Ad Groups]** e quindi sul nome del gruppo di annunci.

## Visualizzare e modificare le impostazioni del portfolio

* Per visualizzare o nascondere le impostazioni del portfolio, fare clic su **[!UICONTROL Portfolio Settings]**.

   * Per modificare le impostazioni del portfolio visibili, fai clic su ![Modifica](/help/search-social-commerce/assets/edit.png "Modifica") accanto alla sezione delle impostazioni e [modifica le impostazioni del portfolio](portfolio-edit.md).

Per ulteriori informazioni sulle impostazioni del portfolio, consulta la Guida all’ottimizzazione, disponibile in Search, Social e Commerce.

>[!MORELIKETHIS]
>
>* [(Nuova interfaccia) Informazioni sui portfolio](portfolio-about.md)
>* [(Nuova interfaccia) Modifica un portfolio](portfolio-edit.md)
>* [(Nuova interfaccia) Scarica i dati nella visualizzazione [!UICONTROL Portfolios]](portfolio-view-report.md)
