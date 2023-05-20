---
title: Informazioni Sui Rapporti In-Platform
description: Scopri i dati del rapporto inclusi nelle visualizzazioni di gestione della campagna.
feature: DSP Campaign Data Views
exl-id: 7af97704-2053-4862-a851-12db009e6776
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '940'
ht-degree: 0%

---

# Informazioni Sui Rapporti In-Platform

<!-- rename "About Performance Reports in Campaign Management Views?" -->
Le visualizzazioni di gestione della campagna includono dati di rapporto completi. I rapporti disponibili ti aiutano a identificare i pacchetti e i posizionamenti che stanno ottenendo buoni risultati e quelli che richiedono la tua attenzione. I pulsanti di azione rapida consentono inoltre di migliorare la produttività.

## Visualizzazione di tutte le campagne

Il [!UICONTROL Campaigns] visualizza consente di aprire un set di grafici dei dati sulle prestazioni e un elenco di tutte le campagne all’interno del tuo account.

### Vista grafico {#chart-view}

È possibile [personalizzare i grafici di tendenza delle serie temporali](campaign-data-visualization-manage.md) in tutte le campagne utilizzando tre metriche. Per impostazione predefinita, i dati per [!UICONTROL Net Spend], [!UICONTROL Impressions], e [!UICONTROL Net CPM] sono inclusi in grafici separati (grafici a tre linee). Facoltativamente, puoi modificare le metriche. Per abilitare i dati orari nei grafici di andamento delle serie temporali, modificare la selezione della data in un singolo giorno ([!UICONTROL Today], [!UICONTROL Yesterday]o un giorno specifico).

![grafici di tendenza separati per tre metriche](/help/dsp/assets/trend-chart-separate.png)

Facoltativamente, puoi anche sovrapporre le tre metriche per rilevare facilmente le anomalie e le aree in cui migliorare la scalabilità o le prestazioni.

![grafico di tendenza con sovrapposizione](/help/dsp/assets/trend-chart.png)

### Vista tabella

![Elenco campagne](/help/dsp/assets/campaigns-list.png)

Per impostazione predefinita, ogni riga della campagna include metriche di velocità e consegna. Le metriche del ritmo includono [!UICONTROL Gross Spend (Lifetime)], che include un indicatore della spesa effettiva nel target rispetto alla spesa prevista nel target in tutti i pacchetti della campagna, in modo da identificare immediatamente le campagne con prestazioni insoddisfacenti. Facoltativamente puoi [modificare la vista a colonne](column-view-change.md) o pari [creare una vista a colonne personalizzata](column-view-create.md).

Ulteriori informazioni [personalizzare le tabelle dati](campaign-data-views-about.md) in altri modi e [filtrare i dati visibili](campaign-data-filter.md).

Per visualizzare una campagna più dettagliatamente, fai clic sul nome della campagna.

## Reporting per singola campagna {#single-campaign-reporting}

All’interno di una campagna, puoi filtrare i dati in base all’entità della campagna: [!UICONTROL Packages], [!UICONTROL Placements], e [!UICONTROL Ads]. Ulteriori informazioni [filtrare i dati visibili](campaign-data-filter.md) per includere solo i pacchetti, i posizionamenti o gli annunci che desideri visualizzare.

![Schede entità campagna](/help/dsp/assets/campaign-subtabs.png)

### Vista grafico

Per ogni campagna, puoi [personalizzare i grafici di tendenza delle serie temporali](campaign-data-visualization-manage.md) con tre metriche, disponibili in ogni vista di entità. Le stesse metriche vengono mantenute in tutti i grafici di tendenza per la campagna.

Consulta la [Sezione &quot;Vista grafico&quot; sulle metriche per più campagne](#chart-view) per ulteriori informazioni.

### Vista tabella

In ogni scheda di entità, ogni riga include le metriche di velocità e consegna per impostazione predefinita, ma puoi [modificare la vista a colonne](column-view-change.md) o pari [creare una vista a colonne personalizzata](column-view-create.md) da applicare a tutte le schede secondarie della campagna. Ulteriori informazioni [personalizzare le tabelle dati](campaign-data-views-about.md) in altri modi. Ogni tabella di dati include [!UICONTROL Subtotals] riga, che mostra la somma o il valore medio di ciascuna metrica su tutte le righe visibili.

### Posizionamento [!UICONTROL Inspector] {#placement-inspector}

Per ogni posizionamento, puoi [apri una (visualizzazione dettagli) [!UICONTROL Inspector])](placement-details-view.md), che include i seguenti dati approfonditi:

* **[!UICONTROL Sites]:** Tutti i siti su cui il posizionamento ha avuto impressioni.

   Il [!UICONTROL Sites] Questa scheda include le funzioni di ricerca e filtro, le stesse opzioni di visualizzazione delle colonne standard e personalizzate disponibili nella pagina principale e una [!UICONTROL Exclude] in ogni riga, in modo da poter escludere rapidamente un sito dal posizionamento.

* **[!UICONTROL Ads]:** Tutti gli annunci nel posizionamento.

   Il [!UICONTROL Ads] Questa scheda include le funzioni di ricerca e filtro, le stesse opzioni di visualizzazione delle colonne standard e personalizzate disponibili nella pagina principale e i pulsanti di azione rapida in ogni riga, ad esempio [!UICONTROL Pause] (in modo da poter mettere in pausa rapidamente un annuncio).

* **[!UICONTROL Frequency]:** Dati per ciascun livello di frequenza dell’annuncio per il posizionamento, tra cui:
   * il livello di frequenza dell’annuncio (ad esempio &quot;1&quot; per tutte le istanze in cui gli utenti hanno visto un annuncio una volta)
   * il numero univoco stimato di dispositivi/browser o persone (a seconda del [!UICONTROL Cross Device Level] per la campagna) che ha ricevuto impression al livello di frequenza specificato
   * il numero stimato di impression al livello di frequenza specificato
   * la frequenza media stimata per il livello di frequenza specificato. Questo valore è uguale a (Impression stimate)/(Valori univoci stimati).

* **[!UICONTROL Inventory]:** Informazioni su tutte le offerte target del posizionamento.

   Il [!UICONTROL Inventory] consente di risolvere rapidamente i problemi visualizzando le statistiche sulle prestazioni, ad esempio [!UICONTROL Auctions], [!UICONTROL Bids], e [!UICONTROL Win Rate]. La scheda include le funzioni di ricerca e filtro, le stesse opzioni di visualizzazione delle colonne standard e personalizzate disponibili nella pagina principale e i pulsanti di azione rapida in ogni riga, tra cui [!UICONTROL Edit], [!UICONTROL View Report], e [[!UICONTROL Auction Insights] per ulteriori informazioni sulla risoluzione dei problemi](/help/dsp/inventory/private-deal-auction-insights.md).

#### Risoluzione dei problemi di inventario

| Problema | Possibile causa | Azioni da intraprendere |
| -----------| ---------- | ---------- |
| [!UICONTROL Zero Auctions] | L&#39;editore non ha iniziato a inviare richieste di offerta. | Contatta l’editore per attivare l’offerta. |
|  | L’offerta è stata impostata in modo errato, ad esempio inserendo un ID offerta esterno errato. | Conferma i dettagli dell’offerta e modifica l’offerta. |
| [!UICONTROL Auctions but no Bids] | Il targeting del posizionamento non corrisponde alle richieste di offerta in arrivo per l’offerta. <br><br> Ad esempio, un posizionamento potrebbe essere indirizzato a una geografia che non è idonea per l’operazione. | Modifica le destinazioni di posizionamento in base alle esigenze per evitare incongruenze di targeting. |
|  | Il posizionamento non ha un annuncio attivo con il tipo di file multimediale richiesto per l’offerta. | Crea e allega al posizionamento un annuncio con il tipo di file multimediale corretto. |
|  | Il posizionamento non dispone di un budget adeguato. | Aumenta il budget di posizionamento per consentire le offerte sulle richieste in arrivo. |
|  | Le date del volo di posizionamento non si sovrappongono alle date di consegna delle impression per l’offerta. | Modifica le date di volo del posizionamento in base alle esigenze. |
| [!UICONTROL Low Win Rate] | L&#39;offerta massima del posizionamento (minima o fissa) è inferiore al minimo richiesto dalla trattativa. | Aumentare il [!UICONTROL Max Bid] secondo necessità. |
|  | Il posizionamento utilizza filtri pre-offerta che limitano le offerte. | Abbassa le soglie dei filtri pre-offerta per consentire un maggior numero di offerte. |
|  | Il targeting del pubblico per il posizionamento è troppo restrittivo. | Verifica se le destinazioni del pubblico specificato hanno un numero sufficiente di utenti attivi e, se possibile, espandi il pubblico. |

![posizionamento Ispettore](/help/dsp/assets/placement-inspector.png)

È possibile esportare i dati in [!UICONTROL Sites], [!UICONTROL Ads], o [!UICONTROL Frequency] nella cartella di download predefinita del browser come rapporto in formato XLSM.

### Altri tipi di reporting a livello di campagna

Per altre suddivisioni dei dati, visualizza [le pagine di reporting a livello di campagna](/help/dsp/campaign-management/campaigns/campaign-view-report.md). Il <!--legacy --> Il rapporto include sezioni su [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability], e [!UICONTROL Audience Performance] dati.

>[!MORELIKETHIS]
>
>* [Visualizzare i dettagli di Siti, Annunci e Frequenza per un posizionamento](placement-details-view.md)
>* [Informazioni sulle visualizzazioni dati di Campaign](campaign-data-views-about.md)
>* [Creare una vista a colonne personalizzata](column-view-create.md)
>* [Modificare la vista a colonne](column-view-change.md)
>* [Gestire le visualizzazioni dati](campaign-data-visualization-manage.md)
>* [Esportare dati da una vista Campaign Management](campaign-export-data.md)
>* [Visualizzare un rapporto dettagliato per una campagna](/help/dsp/campaign-management/campaigns/campaign-view-report.md)

