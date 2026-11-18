---
title: (Nuova interfaccia) Visualizza dettagli sulle prestazioni del portfolio
description: Scopri come visualizzare le prestazioni del portfolio, i dettagli delle unità di offerta, le previsioni e la cronologia delle offerte, nonché come esportare la cronologia delle unità di offerta in Adobe Advertising Search, Social e Commerce.
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
source-git-commit: 6b779d2f91a140cd69ed4a25ac97d376dd1ed48d
workflow-type: tm+mt
source-wordcount: '1555'
ht-degree: 0%
---
# (Nuova interfaccia) Visualizza dettagli sulle prestazioni del portfolio

*funzionalità Beta*

<!-- Verify all, including why (if) the first report is for active and optimized portfolios(?), and why the other reports are for active portfolios, not optimized ones -->

La visualizzazione dei dettagli del portfolio include le seguenti informazioni su un portfolio:

* I valori effettivi e previsti per un massimo di tre metriche delle prestazioni. I rapporti includono i valori delle metriche totali per il portfolio e la suddivisione della metrica per data.<!-- Not for active portfolios only?  -->

* Dati di accuratezza del modello per i portfolio attivi, che mostrano quanto i modelli si sono discostati dalle previsioni. Il rapporto mostra la precisione complessiva dei costi giornalieri o continui di sette giorni, la precisione dei clic e la precisione del valore obiettivo.

  È possibile visualizzare i dati come grafico di tendenza (impostazione predefinita) o come tabella.

* La spesa target rispetto alla spesa effettiva per i portafogli attivi. Facoltativamente, puoi anche includere i budget totali per le campagne per il portfolio.

* Precisione delle previsioni di costo, clic o [valore obiettivo](/help/search-social-commerce/glossary.md#o-p) per i portfolio attivi per rete di annunci.<!-- Verify -->

* Impostazioni portfolio.

  Facoltativamente, puoi aprire le impostazioni del portfolio per modificarle.

* Elenchi delle reti di annunci, degli account, delle campagne, dei gruppi di annunci e delle parole chiave nel portfolio, con i dati sulle prestazioni.

  Per singole parole chiave, puoi visualizzare i dettagli dell’unità di offerta, incluse le previsioni, le informazioni cronologiche e le informazioni gerarchiche. La visualizzazione [!UICONTROL Bid Unit Details] include le previsioni, le informazioni cronologiche e le informazioni gerarchiche seguenti per l&#39;unità di offerta selezionata:

  * Scheda [!UICONTROL Forecast]: clic, costo, costo per clic, posizione e ricavi attualmente previsti per l&#39;unità di offerta a prezzi di offerta diversi. I dati vengono visualizzati per tutti i dispositivi e per ogni tipo di dispositivo ([!UICONTROL Mobile], [!UICONTROL Computer] e [!UICONTROL Tablet]).<!-- Probably no longer applicable: For portfolios using v6 of the optimization capability, both the [!UICONTROL Computers] and [!UICONTROL Tablets] tabs show the combined totals for computers and tablets. For portfolios using v7, however, all data for the [!UICONTROL Computers] and [!UICONTROL Tablets] tabs is separate. -->

    **Nota:** non sono disponibili dati di previsione per un tipo di dispositivo quando non sono disponibili dati sufficienti specifici per il dispositivo per generare modelli e impostare le regolazioni per tale tipo di dispositivo. **Nota:** per visualizzare la precisione dei costi o dei ricavi per ogni unità di offerta all&#39;interno di un portfolio che ha ricevuto un clic durante un intervallo di date specifico, vedere rispettivamente la visualizzazione dei dettagli della precisione dei costi o dei ricavi del portfolio.

  * Scheda [!UICONTROL History]: tutte le offerte negli ultimi 36 giorni, inclusi i seguenti dati per ciascuna offerta: data e ora, impression, clic, costo totale, CPC medio, posizione media e ricavi ponderati mostrati per data di clic. I dati vengono visualizzati per tutti i dispositivi e per ogni tipo di dispositivo (Mobile, Computer e Tablet).<!-- Probably no longer applicable: For portfolios using v6 of the optimization capability, both the [!UICONTROL Computers] and [!UICONTROL Tablets] tabs show the combined totals for computers and tablets. For portfolios using v7, however, all data for the [!UICONTROL Computers] and [!UICONTROL Tablets] tabs is separate. **Note:** Whenever the optimization method changes from v6 to v7 and vice-versa, the history data is reset the same day. -->

  * Scheda [!UICONTROL Details]: la parola chiave, il tipo di corrispondenza (se applicabile) e il gruppo di annunci principale, la campagna, l&#39;account di rete dell&#39;annuncio e il portfolio a cui appartiene l&#39;unità dell&#39;offerta.

## Aprire i dettagli sulle prestazioni di un portfolio

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Portfolios]**.

1. Posizionare il cursore sul nome del portfolio e fare clic su ![Panoramica di Portfolio](/help/search-social-commerce/assets/portfolio-overview.png "Panoramica di Portfolio").

1. (Facoltativo) Per modificare l&#39;intervallo di date per i dettagli del portfolio, fare clic sull&#39;intervallo di date in alto a destra, specificare l&#39;intervallo di date, quindi fare clic su **[!UICONTROL Apply]**.

1. (Facoltativo) Dal menu **[!UICONTROL Data Aggregation]**, modificare l&#39;unità di tempo dei dati inclusi in ogni riga: *[!UICONTROL Daily],* *[!UICONTROL Weekly],* o *[!UICONTROL Monthly].*

   Le opzioni disponibili dipendono dall’intervallo di date selezionato. Se l’aggregazione corrente non è disponibile per un nuovo intervallo di date, viene selezionata automaticamente un’altra aggregazione disponibile.

1. (Facoltativo) Dal menu **[!UICONTROL Conversion Based On]** nell&#39;intestazione della pagina, selezionare **[!UICONTROL Click Date]** o **[!UICONTROL Transaction Date]**.

   Questa impostazione si applica ai dati di conversione nei rapporti portfolio e negli elenchi dei componenti.

Per visualizzare i dettagli di un altro portfolio, utilizza il selettore di portfolio accanto al nome del portfolio.

## Personalizza la scheda [!UICONTROL Portfolio Overview]

* (Facoltativo) Per personalizzare i report [!UICONTROL Portfolio Performance], eseguire una delle operazioni seguenti:

  * Per modificare le metriche delle prestazioni utilizzate sia per le metriche totali che per quelle dettagliate, fare clic su **[!UICONTROL Metrics]** e selezionare fino a tre metriche.

    Le metriche predefinite sono *[!UICONTROL Cost]*, *[!UICONTROL Clicks]* e *[!UICONTROL Objective Value]*.<!-- What else is available: the advertiser's revenue metrics? Anything else from the ad networks? -->

  * Per le metriche dettagliate:

    * Spostare l&#39;opzione accanto a **[!UICONTROL Display predictions]** per mostrare o nascondere i valori delle metriche previsti.

    * Passare dalla visualizzazione grafico (![Visualizzazione grafico](/help/search-social-commerce/assets/chart-view.png "Visualizzazione grafico")) alla visualizzazione tabella (![Vista tabella](/help/search-social-commerce/assets/table-view.png "Vista tabella")).

    * (Nella visualizzazione grafico) Per visualizzare i dati relativi a un punto qualsiasi del grafico, tenere premuto il cursore su tale punto.

    * (Nella visualizzazione grafico) Per eseguire lo zoom, selezionare un&#39;area del grafico.

    * (Quando vengono visualizzati gli indicatori di modifica delle impostazioni del portfolio) Per visualizzare la cronologia delle modifiche del portfolio per una data contrassegnata, fare clic sull&#39;indicatore nel grafico. Per ulteriori informazioni sulla cronologia, vedere &quot;[Visualizzare la cronologia delle modifiche di un portfolio](portfolio-view-change-history.md#portfolio-change-history).&quot;

* (Facoltativo) Per personalizzare il grafico di tendenza [!UICONTROL Model accuracy], eseguire una delle operazioni seguenti:

  * Passare dalla visualizzazione grafico (![Visualizzazione grafico](/help/search-social-commerce/assets/chart-view.png "Visualizzazione grafico")) alla visualizzazione tabella (![Vista tabella](/help/search-social-commerce/assets/table-view.png "Vista tabella")).

  * Passare dalla visualizzazione dei dati relativi a *[!UICONTROL Daily Accuracy]* a quella di *[!UICONTROL 7 Day Rolling Accuracy]*.

    [!UICONTROL 7 Day Rolling Accuracy] è la precisione media della previsione per i sette giorni precedenti, espressa in percentuale. Ad esempio, il valore per l’8 maggio 2025 corrisponde alla precisione media per il periodo dal 1° maggio al 7 maggio 2025.

    [!UICONTROL 7 Day Rolling Accuracy] è disponibile solo quando [!UICONTROL Data Aggregation] è impostato su [!UICONTROL Daily].

  * (Nella visualizzazione grafico) Per visualizzare i dati relativi a un punto qualsiasi del grafico, tenere premuto il cursore su tale punto.

* (Facoltativo) Per personalizzare il grafico di tendenza [!UICONTROL Target vs actual spend], eseguire una delle operazioni seguenti:

  * Sposta il parametro accanto a **[!UICONTROL Display budget]** per mostrare o nascondere il budget totale della campagna per ogni data.

  * Per visualizzare i dati relativi a un punto qualsiasi del grafico, posizionare il cursore su tale punto.

* (Facoltativo) Per personalizzare il grafico di tendenza [!UICONTROL Network Accuracy], eseguire una delle operazioni seguenti:

  * Modificare la metrica riportata in *[!UICONTROL Cost]*, *[!UICONTROL Clicks]* o *[!UICONTROL Objective Value]*.

  * Quando i dati sono disponibili per più reti, selezionare la rete dal menu accanto al menu delle metriche.

  * Per visualizzare i dati relativi a un punto qualsiasi del grafico, posizionare il cursore su tale punto.

  * Per eseguire lo zoom, selezionate un&#39;area nel grafico.

## Personalizzare gli elenchi dei componenti del portfolio

Le schede [!UICONTROL Networks], [!UICONTROL Accounts], [!UICONTROL Campaigns], [!UICONTROL Ad Groups] e [!UICONTROL Keywords] includono i seguenti controlli:

* Per eseguire la ricerca per nome, immettere il testo nel campo di ricerca sopra la tabella e sottomettere la ricerca.

* Per [filtrare i dati](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md), fare clic su ![Filtro](/help/search-social-commerce/assets/filter-new.png "Filtro"). Puoi modificare o rimuovere i filtri applicati utilizzando i controlli filtro sopra la tabella.

* Per visualizzare i componenti di una rete, un account, una campagna o un gruppo di annunci nella scheda successiva, fai clic sul nome corrispondente. Il padre selezionato viene visualizzato nel breadcrumb sopra la tabella e i filtri applicabili vengono riportati durante il drilling verso il basso. Le selezioni padre possono continuare a limitare l&#39;elenco quando si passa da una scheda all&#39;altra.

  Per rimuovere una selezione di espansione (ad esempio un nome di rete o di account), fare clic su **[!UICONTROL X]** accanto al nome del componente nella breadcrumb sopra la tabella. Le selezioni padre di livello superiore possono rimanere attive. Per tornare a tutti i componenti nel portfolio, rimuovi le selezioni principali rimanenti ed eventuali altri filtri.

* Per aggiornare i dati, fare clic su ![Aggiorna](/help/search-social-commerce/assets/refresh-new.png "Aggiorna").

* ([!UICONTROL Accounts], [!UICONTROL Campaigns], [!UICONTROL Ad Groups] e [!UICONTROL Keywords] solo schede) Per modificare le colonne visualizzate o l&#39;ordinamento, fare clic su ![Colonne personalizzate](/help/search-social-commerce/assets/custom-columns-new.png "Colonne personalizzate") e [modificare il set di colonne e le opzioni di ordinamento](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-sort-icon.md).


## Elencare le reti di annunci nel portfolio

* Fare clic sulla scheda **[!UICONTROL Networks]**.

## Elencare i conti nel portfolio

* Per visualizzare tutti gli account nel portfolio, fare clic sulla scheda **[!UICONTROL Accounts]**.

* Per visualizzare gli account per una rete specifica nel portfolio, fare clic sulla scheda **[!UICONTROL Networks]** e quindi sul nome della rete.

## Elencare le campagne nel portfolio

I dettagli di ciascuna campagna includono la strategia di offerta, il costo effettivo e previsto, i clic e il valore obiettivo, nonché la precisione di costo, clic e valore obiettivo.

* Per visualizzare tutte le campagne nel portfolio, fare clic sulla scheda **[!UICONTROL Campaigns]**.

* Per visualizzare le campagne per un account specifico nel portfolio, fare clic sulla scheda **[!UICONTROL Accounts]** e quindi sul nome dell&#39;account.

## Elencare i gruppi di annunci nel portfolio

I dettagli su ciascun gruppo di annunci includono la rete, l’offerta predefinita, i costi, i clic, il CPC, le impression, il valore obiettivo e le metriche di conversione utilizzate nell’obiettivo del portfolio.

* Per visualizzare tutti i gruppi di annunci nel portfolio, fare clic sulla scheda **[!UICONTROL Ad Groups]**.

* Per visualizzare tutti i gruppi di annunci di una campagna all&#39;interno del portfolio, fare clic sulla scheda **[!UICONTROL Campaigns]** e quindi sul nome della campagna.

## Elencare e visualizzare i dettagli sulle parole chiave nel portfolio {#bid-unit-details}

I dettagli di ciascuna parola chiave includono l&#39;ID dell&#39;unità di offerta, il tipo di corrispondenza, il costo effettivo e previsto, i clic e il valore obiettivo, nonché la differenza tra costo, clic e valore obiettivo. Puoi visualizzare i dettagli dell’unità di offerta relativi a una singola parola chiave.

1. Elencare le parole chiave:

   * Per visualizzare tutte le parole chiave nel portfolio, fare clic sulla scheda **[!UICONTROL Keywords]**.

   * Per visualizzare tutte le parole chiave di un gruppo di annunci all&#39;interno del portfolio, fare clic sulla scheda **[!UICONTROL Ad Groups]** e quindi sul nome del gruppo di annunci.

1. (Facoltativo) Per visualizzare i dettagli su un&#39;unità di offerta specifica, fare clic sul valore nella colonna **[!UICONTROL Bid Unit ID]**. Fare clic su una scheda di [!UICONTROL Bid Unit Details] per ulteriori informazioni.

### Visualizzare e scaricare la cronologia di una singola unità di offerta {#bid-unit-history}

1. [Aprire i dettagli dell&#39;unità dell&#39;offerta](#bid-unit-details).

1. Fare clic sulla scheda **[!UICONTROL History]**.

1. (Facoltativo) Dal menu dei dispositivi sopra la tabella, selezionare un tipo di dispositivo per il quale visualizzare la cronologia. Per impostazione predefinita, vengono visualizzati i dati di tutti i dispositivi.

1. (Facoltativo) Quando i dati della cronologia sono disponibili, fare clic su **[!UICONTROL Export as csv]** per scaricare la cronologia visualizzata.

Il file viene scaricato in base alla normale procedura del browser.

Per visualizzare la cronologia delle offerte per l&#39;intero portfolio e modificarne l&#39;intervallo di date, vedere &quot;[Visualizzare la cronologia delle modifiche delle offerte di un portfolio](portfolio-view-change-history.md#portfolio-bid-change-history).&quot;

## Visualizzare e modificare le impostazioni del portfolio

* Per visualizzare o nascondere le impostazioni del portfolio, fare clic su **[!UICONTROL Portfolio Settings]**.

  * Per modificare le impostazioni del portfolio visibili, fai clic su ![Modifica](/help/search-social-commerce/assets/edit.png "Modifica") accanto alla sezione delle impostazioni e [modifica le impostazioni del portfolio](portfolio-edit.md).

Per ulteriori informazioni sulle impostazioni del portfolio, consulta la Guida all’ottimizzazione, disponibile in Search, Social e Commerce.

## Scarica i rapporti sulle prestazioni del portfolio e gli elenchi dei componenti del portfolio

* Per scaricare i rapporti sulle prestazioni e gli elenchi dei componenti:

  1. Nella barra degli strumenti fare clic su **[!UICONTROL Download report]**.

  1. Selezionare la casella di controllo accanto a ogni tipo di rapporto sulle prestazioni e di componente portfolio da includere.

     I componenti del portfolio disponibili sono *[!UICONTROL Campaigns table]*, *[!UICONTROL Ad groups table]* e *[!UICONTROL Keywords table]*. Le tabelle [!UICONTROL Networks] e [!UICONTROL Accounts] non sono incluse in questo download.

     Per i report sulle prestazioni con entrambe le opzioni, selezionare **[!UICONTROL As chart]**, **[!UICONTROL As table]** o entrambi. Il report [!UICONTROL Network accuracy chart] è disponibile solo come grafico.

  1. Fare clic su **[!UICONTROL Download report]**.

* Per scaricare un report [!UICONTROL Model accuracy] con tipi di dati specifici:

  1. Nella barra degli strumenti di [!UICONTROL Model accuracy], fare clic su **[!UICONTROL Download report]**.

  1. Selezionare **[!UICONTROL Cost Accuracy]**, **[!UICONTROL Objective Value Accuracy]** o entrambi.

  1. Per ogni tipo di dati selezionato, selezionare **[!UICONTROL By Bid Unit]**, **[!UICONTROL By Click Volume]** o entrambi.

  1. Fare clic su **[!UICONTROL Download report]**.

>[!MORELIKETHIS]
>
>* [(Nuova interfaccia) Informazioni sui portfolio](portfolio-about.md)
>* [(Nuova interfaccia) Modifica un portfolio](portfolio-edit.md)
>* [(Nuova interfaccia) Scarica i dati nella visualizzazione [!UICONTROL Portfolios]](portfolio-view-report.md)
