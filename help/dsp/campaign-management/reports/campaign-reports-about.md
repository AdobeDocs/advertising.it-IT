---
title: Informazioni sui report in-Platform
description: Scopri i dati del rapporto inclusi nelle visualizzazioni di gestione delle campagne.
feature: DSP Campaign Data Views
exl-id: 7af97704-2053-4862-a851-12db009e6776
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '940'
ht-degree: 0%

---

# Informazioni sui report in-Platform

<!-- rename "About Performance Reports in Campaign Management Views?" -->
Le visualizzazioni di gestione della campagna includono dati di report completi. I rapporti disponibili ti aiutano a identificare i pacchetti e i posizionamenti che hanno buone prestazioni e quelli che richiedono la tua attenzione. I pulsanti di azione rapida consentono inoltre di aumentare la produttività.

## Visualizza tutte le campagne

La [!UICONTROL Campaigns] viene visualizzata una serie di grafici dati sulle prestazioni e un elenco di tutte le campagne all’interno dell’account.

### Vista grafico {#chart-view}

È possibile [personalizzare i grafici di tendenza delle serie temporali](campaign-data-visualization-manage.md) in tutte le campagne utilizzando tre metriche. Per impostazione predefinita, i dati per [!UICONTROL Net Spend], [!UICONTROL Impressions]e [!UICONTROL Net CPM] sono inclusi in grafici separati (grafici a linee). Facoltativamente, puoi modificare le metriche. Per abilitare i dati orari nei grafici di tendenza delle serie temporali, modifica la selezione della data in un singolo giorno ([!UICONTROL Today], [!UICONTROL Yesterday]o un giorno specifico).

![grafici di tendenze separati per tre metriche](/help/dsp/assets/trend-chart-separate.png)

Facoltativamente, puoi anche sovrapporre le tre metriche per individuare facilmente le anomalie e le aree in cui migliorare la scala o le prestazioni.

![grafico a tendenze con sovrapposizione](/help/dsp/assets/trend-chart.png)

### Vista a tabella

![Elenco campagne](/help/dsp/assets/campaigns-list.png)

Per impostazione predefinita, ogni riga della campagna include metriche di velocità e consegna. Le metriche di imballaggio includono [!UICONTROL Gross Spend (Lifetime)], che include un indicatore della spesa effettiva sul target rispetto alla spesa prevista sul target in tutti i pacchetti della campagna, in modo da identificare immediatamente le campagne con prestazioni peggiori. Facoltativamente [modificare la vista a colonne](column-view-change.md) o pari [creare una vista a colonne personalizzata](column-view-create.md).

È possibile [personalizzare le tabelle di dati](campaign-data-views-about.md) in modalità aggiuntive e [filtrare i dati visibili](campaign-data-filter.md).

Per visualizzare una campagna in modo più dettagliato, fai clic sul nome della campagna.

## Generazione di rapporti per singola campagna {#single-campaign-reporting}

All’interno di una campagna, puoi filtrare i dati in base all’entità della campagna: [!UICONTROL Packages], [!UICONTROL Placements]e [!UICONTROL Ads]. È possibile [filtrare i dati visibili](campaign-data-filter.md) per includere solo i pacchetti, i posizionamenti o gli annunci che desideri visualizzare.

![Schede entità campagna](/help/dsp/assets/campaign-subtabs.png)

### Vista grafico

Per ogni campagna, puoi [personalizzare i grafici di tendenza delle serie temporali](campaign-data-visualization-manage.md) con tre metriche, disponibili in ogni visualizzazione di entità. Le stesse metriche vengono mantenute in tutti i grafici di tendenze della campagna.

Consulta la sezione [Sezione &quot;Visualizzazione grafico&quot; sulle metriche per campagne](#chart-view) per ulteriori informazioni.

### Vista a tabella

In ogni scheda di entità, ogni riga include metriche di velocità e consegna, per impostazione predefinita, ma puoi [modificare la vista a colonne](column-view-change.md) o pari [creare una vista a colonne personalizzata](column-view-create.md) da applicare a tutte le schede secondarie della campagna. È possibile [personalizzare le tabelle di dati](campaign-data-views-about.md) in altri modi. Ogni tabella di dati include [!UICONTROL Subtotals] riga, che mostra la somma o il valore medio di ciascuna metrica in tutte le righe visibili.

### Posizionamento [!UICONTROL Inspector] {#placement-inspector}

Per ogni posizionamento, puoi [aprire una (visualizzazione dettagli [!UICONTROL Inspector])](placement-details-view.md), che include i seguenti dati approfonditi:

* **[!UICONTROL Sites]:** Tutti i siti in cui il posizionamento ha avuto impression.

   La [!UICONTROL Sites] include le funzioni di ricerca e filtro, le stesse opzioni standard e personalizzate per la vista a colonne disponibili nella pagina principale e un [!UICONTROL Exclude] in ogni riga per escludere rapidamente un sito dal posizionamento.

* **[!UICONTROL Ads]:** Tutti gli annunci nel posizionamento.

   La [!UICONTROL Ads] include le funzioni di ricerca e filtro, le stesse opzioni standard e personalizzate per la vista a colonne disponibili nella pagina principale e i pulsanti di azione rapida in ogni riga, ad esempio [!UICONTROL Pause] (in modo da mettere rapidamente in pausa un annuncio).

* **[!UICONTROL Frequency]:** Dati per ogni livello di frequenza pubblicitaria per il posizionamento, tra cui:
   * il livello di frequenza dell’annuncio (ad esempio &quot;1&quot; per tutte le istanze in cui gli utenti hanno visto un annuncio una volta)
   * il numero univoco stimato di dispositivi/browser o persone (a seconda della specifica [!UICONTROL Cross Device Level] per la campagna) che ha ricevuto impression al livello di frequenza specificato
   * il numero stimato di impression al livello di frequenza specificato
   * la frequenza media stimata per il livello di frequenza specificato. Questo valore è uguale a (Impressioni stimate)/(Uniche stimate).

* **[!UICONTROL Inventory]:** Informazioni su tutte le offerte oggetto del posizionamento.

   La [!UICONTROL Inventory] consente di risolvere rapidamente i problemi visualizzando le statistiche sulle prestazioni, ad esempio [!UICONTROL Auctions], [!UICONTROL Bids]e [!UICONTROL Win Rate]. La scheda include le funzioni di ricerca e filtro, le stesse opzioni standard e personalizzate per la vista a colonne disponibili nella pagina principale e i pulsanti di azione rapida in ogni riga, tra cui [!UICONTROL Edit], [!UICONTROL View Report]e [[!UICONTROL Auction Insights] per ulteriori informazioni](/help/dsp/inventory/private-deal-auction-insights.md).

#### Risoluzione dei problemi di inventario

| Problema | Possibile causa | Azioni da intraprendere |
| -----------| ---------- | ---------- |
| [!UICONTROL Zero Auctions] | L’editore non ha iniziato a inviare richieste di offerta. | Contatta l&#39;editore per attivare l&#39;offerta. |
|  | L&#39;operazione è stata impostata in modo errato, ad esempio immettendo un ID offerta esterno errato. | Conferma i dettagli dell&#39;offerta e modifica l&#39;offerta. |
| [!UICONTROL Auctions but no Bids] | Il targeting di posizionamento non corrisponde alle richieste di offerta in arrivo per l’offerta. <br><br> Ad esempio, un posizionamento potrebbe avere come destinazione un’area geografica non idonea all’offerta. | Modifica le destinazioni di posizionamento in base alle esigenze per evitare incongruenze nel targeting. |
|  | Il posizionamento non ha un annuncio attivo con il tipo di supporto richiesto per l’offerta. | Crea e allega un annuncio con il tipo di supporto corretto al posizionamento. |
|  | Il posizionamento non ha un budget adeguato. | Aumenta il budget di posizionamento per consentire offerte su richieste in arrivo. |
|  | Le date del volo di posizionamento non si sovrappongono alle date di consegna dell’impression per l’operazione. | Modifica le date del volo del posizionamento in base alle esigenze. |
| [!UICONTROL Low Win Rate] | L&#39;offerta massima del posizionamento (minimo o fisso) è inferiore al minimo richiesto dall&#39;offerta. | Aumenta il posizionamento [!UICONTROL Max Bid] se necessario. |
|  | Il posizionamento utilizza filtri pre-offerta che limitano le offerte. | Abbassa le soglie dei filtri pre-offerta per consentire un numero maggiore di offerte. |
|  | Il targeting del pubblico per il posizionamento è troppo restrittivo. | Controlla se i target di pubblico specificati hanno abbastanza utenti attivi ed espandi il pubblico, se possibile. |

![ispettore di posizionamento](/help/dsp/assets/placement-inspector.png)

Puoi esportare i dati nella [!UICONTROL Sites], [!UICONTROL Ads]oppure [!UICONTROL Frequency] nella cartella di download predefinita del browser come rapporto in formato XLSM.

### Altri tipi di rapporti a livello di campagna

Per altri raggruppamenti di dati, visualizza [le pagine di reporting a livello di campagna](/help/dsp/campaign-management/campaigns/campaign-view-report.md). La <!--legacy --> include sezioni su [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability]e [!UICONTROL Audience Performance] dati.

>[!MORELIKETHIS]
>
>* [Visualizzare i siti, gli annunci e i dettagli di frequenza per un posizionamento](placement-details-view.md)
>* [Informazioni sulle visualizzazioni dati di Campaign](campaign-data-views-about.md)
>* [Creare una vista a colonne personalizzata](column-view-create.md)
>* [Modificare la Vista a colonne](column-view-change.md)
>* [Gestire le visualizzazioni dati](campaign-data-visualization-manage.md)
>* [Esportare dati da una visualizzazione Campaign Management](campaign-export-data.md)
>* [Visualizzare un rapporto dettagliato per una campagna](/help/dsp/campaign-management/campaigns/campaign-view-report.md)

