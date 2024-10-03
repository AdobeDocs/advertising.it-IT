---
title: Tipi di rapporti sulle prestazioni nelle visualizzazioni di Campaign Management
description: Scopri i dati del rapporto inclusi nelle visualizzazioni di gestione della campagna.
feature: DSP Campaign Data Views
exl-id: 7af97704-2053-4862-a851-12db009e6776
source-git-commit: eba8e9813f8daea58b30f7890ac2dca2498f326f
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 0%

---

# Tipi di rapporti sulle prestazioni nelle visualizzazioni di Campaign Management

Le visualizzazioni di gestione della campagna includono dati di rapporto completi. I rapporti disponibili ti aiutano a identificare i pacchetti e i posizionamenti che stanno ottenendo buoni risultati e quelli che richiedono la tua attenzione. I pulsanti di azione rapida consentono inoltre di migliorare la produttività.

## Visualizzazione di tutte le campagne

La visualizzazione [!UICONTROL Campaigns] si apre con un set di grafici dei dati sulle prestazioni e un elenco di tutte le campagne all&#39;interno del tuo account.

### Vista grafico {#chart-view}

È possibile [personalizzare i grafici delle tendenze delle serie temporali](campaign-data-views-manage.md#data-visualizations-manage) in tutte le campagne utilizzando tre metriche. Per impostazione predefinita, i dati per [!UICONTROL Net Spend], [!UICONTROL Impressions] e [!UICONTROL Net CPM] sono inclusi in grafici a trelli separati. Facoltativamente, puoi modificare le metriche. Per abilitare i dati orari nei grafici di andamento delle serie temporali, modificare la selezione della data in un singolo giorno ([!UICONTROL Today], [!UICONTROL Yesterday] o un giorno specifico).

![grafici di tendenza separati per tre metriche](/help/dsp/assets/trend-chart-separate.png)

Facoltativamente, puoi anche sovrapporre le tre metriche per rilevare facilmente le anomalie e le aree in cui migliorare la scalabilità o le prestazioni.

![grafico di tendenza con sovrapposizione](/help/dsp/assets/trend-chart.png)

### Vista tabella

![Elenco campagne](/help/dsp/assets/campaigns-list.png)

Per impostazione predefinita, ogni riga della campagna include metriche di velocità e consegna. Le metriche di velocità includono [!UICONTROL Gross Spend (Lifetime)], che include un indicatore della spesa effettiva nel target rispetto alla spesa prevista nel target in tutti i pacchetti della campagna, in modo da identificare immediatamente le campagne con prestazioni insoddisfacenti. È possibile [modificare la vista a colonne](campaign-data-views-manage.md#column-view-change) o anche [creare una vista a colonne personalizzata](campaign-data-views-manage.md#column-view-create).

Puoi [personalizzare ulteriormente le tabelle dati](campaign-data-views-manage.md#data-tables-manage) in altri modi e [filtrare i dati visibili](campaign-data-views-manage.md#filter-data-tables).

Per visualizzare una campagna più dettagliatamente, fai clic sul nome della campagna.

#### Indicatori di avviso

Una colonna &quot;[!UICONTROL Alerts]&quot; indica quando una campagna, o qualsiasi entità secondaria al suo interno, presenta un problema. Un&#39;icona [!UICONTROL Pulse Panel] a destra della barra degli strumenti indica anche se sono disponibili avvisi per le entità elencate. Per ulteriori informazioni, vedere &quot;[Visualizza avvisi](campaign-alerts.md)&quot;.

## Reporting per singola campagna {#single-campaign-reporting}

All&#39;interno di una campagna, è possibile filtrare i dati in base all&#39;entità della campagna: [!UICONTROL Packages], [!UICONTROL Placements] e [!UICONTROL Ads]. Puoi [filtrare ulteriormente i dati visibili](campaign-data-views-manage.md#filter-data-tables) per includere solo i pacchetti, i posizionamenti o gli annunci che desideri visualizzare.

![Schede entità campagna](/help/dsp/assets/campaign-subtabs.png)

### Vista grafico

Per ogni campagna, puoi [personalizzare i grafici di tendenza delle serie temporali](campaign-data-views-manage.md#data-visualizations-manage) con tre metriche, disponibili in ogni vista di entità. Le stesse metriche vengono mantenute in tutti i grafici di tendenza per la campagna.

Per ulteriori informazioni, consulta la sezione [&quot;Visualizzazione grafico&quot; sulle metriche per più campagne](#chart-view).

### Vista tabella

In ogni scheda entità, ogni riga include le metriche di velocità e consegna per impostazione predefinita, ma puoi [modificare la vista a colonne](campaign-data-views-manage.md#column-view-change) o anche [creare una vista a colonne personalizzata](campaign-data-views-manage.md#column-view-create) da applicare in tutte le schede secondarie della campagna. È possibile [personalizzare ulteriormente le tabelle dati](campaign-data-views-manage.md#data-tables-manage) in altri modi. Ogni tabella di dati include una riga [!UICONTROL Subtotals] che mostra la somma o il valore medio di ogni metrica in tutte le righe visibili.

#### Indicatori di avviso

Una colonna &quot;[!UICONTROL Alerts]&quot; indica quando un pacchetto, un posizionamento o un annuncio, o qualsiasi entità figlio in un pacchetto o in un posizionamento, presenta un problema. Una colonna &quot;[!UICONTROL Alerts]&quot; indica quando una campagna, o qualsiasi entità secondaria al suo interno, presenta un problema. Un&#39;icona [!UICONTROL Pulse Panel] a destra della barra degli strumenti indica anche se sono disponibili avvisi per le entità elencate. Per ulteriori informazioni, vedere &quot;[Visualizza avvisi](campaign-alerts.md)&quot;.

### Altri tipi di reporting a livello di campagna

Per altre suddivisioni dei dati, visualizza [le pagine di reporting a livello di campagna](/help/dsp/campaign-management/campaigns/campaign-view-report.md). Il report include sezioni sui dati [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability] e [!UICONTROL Audience Performance].

### Altri tipi di reporting a livello di posizionamento

Per altre suddivisioni dei dati, visualizza [le pagine di reporting a livello di posizionamento](/help/dsp/campaign-management/placements/placement-view-report.md). Il report include sezioni sui dati [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability], [!UICONTROL Audience Performance], [!UICONTROL Notifications] e [!UICONTROL Ads].

Inoltre, potete visualizzare i seguenti dati nelle impostazioni di posizionamento:

* [A (visualizzazione dettagli [!UICONTROL Inspector])](placement-details-view.md), che mostra tutti i siti target, gli annunci, i dati sulla frequenza e le offerte per un posizionamento.

* Un report di [previsione di posizionamento](/help/dsp/campaign-management/reports/placement-forecast.md).

* [Report diagnostici posizionamento](/help/dsp/campaign-management/reports/placement-diagnostics.md).


### Altri tipi di reporting a livello di annuncio

Per altre suddivisioni dei dati, visualizza [le pagine di reporting a livello di annuncio](/help/dsp/campaign-management/ads/ad-view-report.md). Il report include [!UICONTROL Overview], [!UICONTROL Geography] e [!UICONTROL Viewability] dati.

>[!MORELIKETHIS]
>
>* [Visualizza i dettagli di siti, annunci e frequenza per un posizionamento](placement-details-view.md)
>* [Gestione Delle Visualizzazioni Dati Della Campagna](campaign-data-views-manage.md)
>* [Esporta dati da una visualizzazione Campaign Management](campaign-export-data.md)
>* [Visualizza un report dettagliato per una campagna](/help/dsp/campaign-management/campaigns/campaign-view-report.md)
>* [Visualizza avvisi](campaign-alerts.md)
