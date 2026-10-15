---
title: (Nuova interfaccia) Visualizza dettagli sulle prestazioni del portfolio
description: Scopri come visualizzare i dettagli delle prestazioni del portfolio, comprese le metriche effettive e previste a livello di portfolio e per ogni campagna assegnata.
feature: Search Portfolios, Search Optimization
hide: true
exl-id: b5178856-1b0e-45cf-a351-6f31c0b0ec76
TQID: 'https://experienceleague.adobe.com/5hNxKu6YjJTWI4KGEc6aaYnpgXK6k3OsN0-YfetzENw'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 893a7eac-45bd-56c2-a120-18db6d297dcc
    internal-label: Search Portfolios
  - id: ae57d55f-b168-5358-b114-c3974b1b3d77
    internal-label: Search Optimization
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: c2296997-5d79-4905-b32e-99b5aa892429
    internal-label: Search optimization
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: b001c57e58bab6809e83b6506eb0ae827bbe72e4
workflow-type: tm+mt
source-wordcount: '1080'
ht-degree: 0%
---
# (Nuova interfaccia) Visualizza dettagli sulle prestazioni del portfolio

*funzionalità Beta*

<!-- Verify all, including why (if) the first report is for active and optimized portfolios(?), and why the other reports are for active portfolios, not optimized ones -->

La visualizzazione dei dettagli del portfolio include le seguenti informazioni su un portfolio:

* I valori effettivi e previsti per un massimo di tre metriche delle prestazioni. I rapporti includono i valori delle metriche totali per il portfolio e la suddivisione della metrica per data.<!-- Not for active portfolios only?  -->

* Dati di accuratezza del modello per i portfolio attivi, che mostrano quanto i modelli si sono discostati dalle previsioni. Il rapporto mostra la precisione complessiva dei costi giornalieri o continui di sette giorni, la precisione dei clic e la precisione del valore obiettivo.

  È possibile visualizzare i dati in base alla data di clic (impostazione predefinita) o alla data della transazione. È inoltre possibile visualizzare i dati come grafico di tendenza (impostazione predefinita) o come tabella.

* La spesa target rispetto alla spesa effettiva per i portafogli attivi. Facoltativamente, puoi anche includere i budget totali per le campagne per il portfolio.

* Precisione delle previsioni di costo, clic o [valore obiettivo](/help/search-social-commerce/glossary.md#o-p) per i portfolio attivi per rete di annunci.<!-- Verify -->

* Impostazioni portfolio.

  Facoltativamente, puoi aprire le impostazioni del portfolio per modificarle.

* Elenchi delle campagne, dei gruppi di annunci e delle parole chiave nel portfolio. Per singole parole chiave, puoi visualizzare i dettagli dell’unità di offerta, incluse le previsioni, le informazioni cronologiche e le informazioni gerarchiche.

  La visualizzazione [!UICONTROL Bid Unit Details] include le previsioni, le informazioni cronologiche e le informazioni gerarchiche seguenti per l&#39;unità di offerta selezionata:

  * Scheda [!UICONTROL Forecast]: clic, costo, costo per clic, posizione e ricavi attualmente previsti per l&#39;unità di offerta a prezzi di offerta diversi. I dati vengono visualizzati per tutti i dispositivi e per ogni tipo di dispositivo ([!UICONTROL Mobile], [!UICONTROL Computer] e [!UICONTROL Tablet]).<!-- Probably no longer applicable: For portfolios using v6 of the optimization capability, both the [!UICONTROL Computers] and [!UICONTROL Tablets] tabs show the combined totals for computers and tablets. For portfolios using v7, however, all data for the [!UICONTROL Computers] and [!UICONTROL Tablets] tabs is separate. -->

    **Nota:** non sono disponibili dati di previsione per un tipo di dispositivo quando non sono disponibili dati sufficienti specifici per il dispositivo per generare modelli e impostare le regolazioni per tale tipo di dispositivo. **Nota:** per visualizzare la precisione dei costi o dei ricavi per ogni unità di offerta all&#39;interno di un portfolio che ha ricevuto un clic durante un intervallo di date specifico, vedere rispettivamente la visualizzazione dei dettagli della precisione dei costi o dei ricavi del portfolio.

  * Scheda [!UICONTROL History]: tutte le offerte negli ultimi 36 giorni, inclusi i seguenti dati per ciascuna offerta: data e ora, impression, clic, costo totale, CPC medio, posizione media e ricavi ponderati mostrati per data di clic. I dati vengono visualizzati per tutti i dispositivi e per ogni tipo di dispositivo (Mobile, Computer e Tablet).<!-- Probably no longer applicable: For portfolios using v6 of the optimization capability, both the [!UICONTROL Computers] and [!UICONTROL Tablets] tabs show the combined totals for computers and tablets. For portfolios using v7, however, all data for the [!UICONTROL Computers] and [!UICONTROL Tablets] tabs is separate. **Note:** Whenever the optimization method changes from v6 to v7 and vice-versa, the history data is reset the same day. -->

  * Scheda [!UICONTROL Detail]: il tipo di corrispondenza (se applicabile) e il gruppo di annunci principale, la campagna, l&#39;account di rete dell&#39;annuncio e il portfolio a cui appartiene l&#39;unità dell&#39;offerta.

## Aprire i dettagli sulle prestazioni di un portfolio

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Portfolios]**.

1. Posizionare il cursore sul nome del portfolio e fare clic su (/help/search-social-commerce/assets/portfolio-overview.png &quot;Panoramica di Portfolio&quot;).

1. (Facoltativo) Dal menu **[!UICONTROL Data Aggregation]**, modificare l&#39;unità di tempo dei dati inclusi in ogni riga: *[!UICONTROL Daily],* *[!UICONTROL Weekly],* o *[!UICONTROL Monthly].*

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

1. Fare clic su **[!UICONTROL Download report]**.

## Elencare le campagne nel portfolio

I dettagli di ciascuna campagna includono la strategia di offerta, il costo effettivo e previsto, i clic e il valore obiettivo, nonché la precisione di costo, clic e valore obiettivo.

* Fare clic sulla scheda **[!UICONTROL Campaigns]**.

## Elencare i gruppi di annunci nel portfolio

I dettagli su ciascun gruppo di annunci includono il costo, i clic e il valore obiettivo.

* Per visualizzare tutti i gruppi di annunci nel portfolio, fare clic sulla scheda **[!UICONTROL Ad Groups]**.

* Per visualizzare tutti i gruppi di annunci di una campagna all&#39;interno del portfolio, fare clic sulla scheda **[!UICONTROL Campaigns]** e quindi sul nome della campagna.

## Elencare e visualizzare i dettagli sulle parole chiave nel portfolio

I dettagli di ciascuna parola chiave includono l&#39;ID dell&#39;unità di offerta, il tipo di corrispondenza, il costo effettivo e previsto, i clic e il valore obiettivo, nonché la differenza tra costo, clic e valore obiettivo. Puoi visualizzare i dettagli dell’unità di offerta relativi a una singola parola chiave.

1. Elencare le parole chiave:

   * Per visualizzare tutte le parole chiave nel portfolio, fare clic sulla scheda **[!UICONTROL Keywords]**.

   * Per visualizzare tutte le parole chiave di un gruppo di annunci all&#39;interno del portfolio, fare clic sulla scheda **[!UICONTROL Ad Groups]** e quindi sul nome del gruppo di annunci.

1. (Facoltativo) Per visualizzare i dettagli su un&#39;unità di offerta specifica, fare clic sul valore nella colonna **[!UICONTROL Bid Unit ID]**. Fare clic su una scheda di [!UICONTROL Bid Unit Details] per ulteriori informazioni.

## Visualizzare e modificare le impostazioni del portfolio

* Per visualizzare o nascondere le impostazioni del portfolio, fare clic su **[!UICONTROL Portfolio Settings]**.

  * Per modificare le impostazioni del portfolio visibili, fai clic su ![Modifica](/help/search-social-commerce/assets/edit.png "Modifica") accanto alla sezione delle impostazioni e [modifica le impostazioni del portfolio](portfolio-edit.md).

Per ulteriori informazioni sulle impostazioni del portfolio, consulta la Guida all’ottimizzazione, disponibile in Search, Social e Commerce.

## Scaricare i rapporti sulle prestazioni del portfolio e gli elenchi dei componenti del portfolio

* Per scaricare tutti i rapporti:

  1. Nella barra degli strumenti fare clic su **[!UICONTROL Download report]**.

  1. Selezionare la casella di controllo accanto a ogni tipo di rapporto sulle prestazioni e di componente portfolio da includere.

     Per alcuni rapporti sulle prestazioni, è possibile scegliere se scaricare i dati come grafico o tabella.

  1. Fare clic su **[!UICONTROL Download report]**.

* Per scaricare un report [!DNL model accuracy] con tipi di dati specifici:

  1. Nella barra degli strumenti del report, fare clic su **[!UICONTROL Download report]**.

  1. Seleziona la casella di controllo accanto a ciascun tipo di dati da includere e come suddividerli (per unità di offerta e/o per volume di clic).

  1. Fare clic su **[!UICONTROL Download report]**.

>[!MORELIKETHIS]
>
>* [(Nuova interfaccia) Informazioni sui portfolio](portfolio-about.md)
>* [(Nuova interfaccia) Modifica un portfolio](portfolio-edit.md)
>* [(Nuova interfaccia) Scarica i dati nella visualizzazione [!UICONTROL Portfolios]](portfolio-view-report.md)
