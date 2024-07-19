---
title: Gestire le visualizzazioni dati della campagna
description: Scopri come personalizzare le visualizzazioni dati per campagne, pacchetti, posizionamenti e annunci.
feature: DSP Campaign Data Views
exl-id: a22da10b-104d-4860-a23f-f2a6e59b637c
source-git-commit: 5b07096e5f07c60a3efcbf4213b3bc2f061f36a4
workflow-type: tm+mt
source-wordcount: '915'
ht-degree: 0%

---

# Gestire le visualizzazioni dati della campagna

È possibile personalizzare i dati visualizzati nelle visualizzazioni di gestione delle campagne ([!UICONTROL Campaigns], [!UICONTROL Packages], [!UICONTROL Placements] e [!UICONTROL Ads]).

## Gestire le visualizzazioni dati {#data-visualizations-manage}

Puoi modificare le metriche e la modalità grafico per tutte le visualizzazioni di dati nelle campagne o per una singola campagna. Le modifiche a una singola campagna vengono applicate a tutte le visualizzazioni dati della campagna, incluse quelle nelle viste [!UICONTROL Packages], [!UICONTROL Placements] e [!UICONTROL Ads].

### Modificare le metriche per una visualizzazione dati

1. Nell&#39;angolo superiore destro della visualizzazione dati, fai clic su ![Impostazioni](/help/dsp/assets/settings-chart.png).

1. Seleziona le metriche.

   Non puoi selezionare la stessa metrica due volte.

1. Fare clic su **[!UICONTROL Apply]**.

### Modificare la modalità di visualizzazione di una visualizzazione dati

* Nell&#39;angolo superiore destro della visualizzazione dati fare clic sull&#39;opzione [!UICONTROL Overlay] (![Interruttore di sovrapposizione](/help/dsp/assets/overlay.png)) per passare dalla modalità di sovrapposizione (tutti i grafici sovrapposti) alla modalità di grafico a trelli (tre grafici distinti) e viceversa.

## Gestire le tabelle dati {#data-tables-manage}

In tutte le visualizzazioni di gestione delle campagne ([!UICONTROL Campaigns], [!UICONTROL Packages], [!UICONTROL Placements] e [!UICONTROL Ads]), è possibile personalizzare i dati visualizzati all&#39;interno della tabella dati.

### Gestisci visualizzazioni colonne {#column-views-manage}

Ogni livello di gestione della campagna ([!UICONTROL Campaigns], [!UICONTROL Packages], [!UICONTROL Placements] e [!UICONTROL Ads]) include [!UICONTROL Pacing] e [!UICONTROL Performance] visualizzazioni incorporate che includono metriche rilevanti per l&#39;entità. Per impostazione predefinita, la visualizzazione [!UICONTROL Pacing] è visualizzata in modo da poter identificare immediatamente le campagne e i componenti della campagna con prestazioni insoddisfacenti. Facoltativamente, puoi creare e modificare set di colonne personalizzati.

![selettore vista a colonne](/help/dsp/assets/column-view-selector.png)

DSP salva la visualizzazione più recente come predefinita, in modo che, ogni volta che ritorni alla pagina, puoi sempre visualizzare le metriche pertinenti.

#### Modificare la vista a colonne {#column-view-change}

* Nel selettore Visualizza fare clic su ![freccia giù](/help/dsp/assets/chevron-down.png) e quindi fare clic sul nome della vista a colonne desiderata.

#### Creare una vista a colonne personalizzata {#column-view-create}

1. Nel selettore Visualizza fare clic su ![freccia giù](/help/dsp/assets/chevron-down.png) e quindi su **[!UICONTROL Create View]**.

1. Specifica le metriche da includere nella visualizzazione:

   1. Nell’elenco delle metriche disponibili, seleziona la casella di controllo accanto a ciascuna metrica da includere.

      Tutte le metriche sono alfabetiche per categoria: [!UICONTROL Settings], [!UICONTROL Spend], [!UICONTROL Pacing], [!UICONTROL Reporting] (metriche standard monitorate da DSP), [!UICONTROL Viewability] e [!UICONTROL Conversions]. Le metriche alle quali è stato aggiunto &quot;([!UICONTROL Lifetime])&quot; restituiscono valori dall&#39;inizio della campagna, indipendentemente dall&#39;intervallo di date selezionato nella pagina.

   1. Se necessario, modifica l’ordine delle colonne facendo clic sui nomi delle colonne nel pannello di destra e trascinandoli nelle posizioni desiderate.

   Alcune colonne hanno posizioni fisse e non possono essere spostate o rimosse.

1. Applica o salva le impostazioni:

   * Per applicare temporaneamente le impostazioni senza salvarle nella visualizzazione, fare clic su **[!UICONTROL Apply].**

   * Per salvare le impostazioni in una nuova vista a colonne personalizzata, fare clic su **[!UICONTROL Save As]**. Nella finestra [!UICONTROL Save View] immettere il nome della nuova visualizzazione e quindi fare clic su **[!UICONTROL Save]**.

#### Modificare una vista a colonne {#column-view-edit}

>[!NOTE]
>
>Non è possibile salvare le modifiche apportate a una vista a colonne standard (predefinita), ma è possibile applicarle temporaneamente o salvarle in una nuova vista personalizzata.

1. Nel selettore Visualizza fare clic su ![freccia giù](/help/dsp/assets/chevron-down.png) e quindi sul nome della vista a colonne esistente.

1. Nel selettore Visualizza fare clic su ![freccia giù](/help/dsp/assets/chevron-down.png) e quindi su **[!UICONTROL Edit View]**.

1. Modifica le metriche da includere nella visualizzazione:

   1. Nell’elenco delle metriche disponibili, seleziona la casella di controllo accanto a ciascuna metrica da includere e deseleziona la casella di controllo accanto a ciascuna metrica da escludere.

      Tutte le metriche sono alfabetiche per categoria: [!UICONTROL Settings], [!UICONTROL Spend], [!UICONTROL Pacing], [!UICONTROL Reporting] (metriche standard monitorate da DSP), [!UICONTROL Viewability] e [!UICONTROL Conversions]. Le metriche alle quali è stato aggiunto &quot;([!UICONTROL Lifetime])&quot; restituiscono valori dall&#39;inizio della campagna, indipendentemente dall&#39;intervallo di date selezionato nella pagina.

   1. Se necessario, modifica l’ordine delle colonne facendo clic sui nomi delle colonne nel pannello di destra e trascinandoli nelle posizioni desiderate.

   Alcune colonne hanno posizioni fisse e non possono essere spostate o rimosse.

1. Applica o salva le impostazioni:

   * (Solo visualizzazioni personalizzate) Per salvare le impostazioni, fare clic su **[!UICONTROL Save]**.

   * Per applicare temporaneamente le impostazioni senza salvarle nella visualizzazione, fare clic su **[!UICONTROL Apply].**

   * Per salvare le impostazioni in una nuova vista a colonne personalizzata, fare clic su **[!UICONTROL Save As]**. Nella finestra [!UICONTROL Save View] immettere il nome della nuova visualizzazione e quindi fare clic su **[!UICONTROL Save]**.

### Filtrare i dati della campagna {#filter-data-tables}

I filtri modificano i dati visualizzati nella scheda corrente. I filtri disponibili variano in base al tipo di entità, ma possono includere il nome dell’entità, lo stato e colonne di proprietà aggiuntive.

1. Nella barra degli strumenti principale, fare clic su ![Pulsante Filtro](/help/dsp/assets/filter.png).
1. Per ogni filtro che si desidera applicare, fare clic sul nome del filtro nella colonna sinistra e quindi specificare il valore del filtro.
1. Fare clic su **[!UICONTROL Apply]**.

#### Filtri disponibili

Sono disponibili i seguenti filtri per le viste [!UICONTROL Campaigns], [!UICONTROL Packages] e [!UICONTROL Placements]:

* [!UICONTROL Campaigns] filtri di visualizzazione:
   * [!UICONTROL Campaign status]
   * [!UICONTROL Advertiser]
* [!UICONTROL Packages] filtri di visualizzazione:
   * [!UICONTROL Custom flights] (che esistano o meno)
   * [!UICONTROL Custom goal] (se applicabile)
   * [!UICONTROL End end date]
   * [!UICONTROL Optimization goal]
   * [!UICONTROL Flight pacing]
   * [!UICONTROL Intraday pacing]
   * [!UICONTROL Package status]
   * [!UICONTROL Start date]
* [!UICONTROL Placements] filtri di visualizzazione:
   * [!UICONTROL Custom ad scheduling]
   * [!UICONTROL Custom goal] (se applicabile)
   * [!UICONTROL End date]
   * [!UICONTROL Max bid] ([!UICONTROL less than], [!UICONTROL greater than] o [!UICONTROL equal to] un valore specificato)
   * [!UICONTROL Optimization goal]
   * [!UICONTROL Pacing on] ([!UICONTROL impressions] o [!UICONTROL spend])
   * [!UICONTROL Flight pacing]
   * [!UICONTROL Intraday pacing]
   * [!UICONTROL Package]
   * [!UICONTROL Placement status]
   * [!UICONTROL Placement type]
   * [!UICONTROL Placement sub-type]
   * [!UICONTROL Start date]
   * [!UICONTROL Creation date]
* [!UICONTROL Ads] filtri di visualizzazione:
   * [!UICONTROL Adobe ad approval status]
   * [!UICONTROL Ad ID]
   * [!UICONTROL Ad name]
   * [!UICONTROL Ad type]
   * [!UICONTROL Creation date]


### Modificare l’intervallo di date

Modifica l’intervallo di date utilizzato in tutte le visualizzazioni standard e personalizzate utilizzando il selettore dell’intervallo di date sopra qualsiasi tabella di dati.

![Selettore intervallo date](/help/dsp/assets/date-range-selector.png "Selettore intervallo date")

* Per un intervallo predefinito: selezionalo dall’elenco degli incrementi di tempo comuni. Il valore predefinito è [!UICONTROL Last 30 days]*.

* Per un intervallo specifico, effettuare una delle seguenti operazioni:

   * Fare clic su ![Calendario](/help/dsp/assets/calendar.png "Calendario"), quindi fare clic sulla data di inizio e sulla data di fine all&#39;interno del calendario.

   * Fare clic all&#39;interno dell&#39;intervallo di date, quindi immettere una data di inizio e una data di fine oppure selezionarle all&#39;interno del calendario.

     È possibile immettere valori numerici (da M-D-AA a MM-GG-AAAA) e/o nomi o abbreviazioni dei mesi (ad esempio Gen o Gennaio).

### Ordinare una colonna di dati

Puoi ordinare qualsiasi colonna di dati in ordine crescente (dalla A alla Z o da 1 a 10) o decrescente (dalla Z alla A o da 10 a 1).

* Fai clic sull’intestazione della colonna per passare dall’ordine crescente a quello decrescente.


### Specifica il numero di righe di dati

In basso a destra, accanto a **[!UICONTROL Items per page]** , selezionare *[!UICONTROL 25]*, *[!UICONTROL 50]* o *[!UICONTROL 100]*.

>[!MORELIKETHIS]
>
>* [Tipi di report sulle prestazioni nelle visualizzazioni di Campaign Management](campaign-reports-about.md)
>* [Visualizza i dettagli di siti, annunci e frequenza per un posizionamento](placement-details-view.md)
>* [Visualizza il rapporto Previsione posizionamento](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [Visualizza i report di diagnostica posizionamento](placement-diagnostics.md)
>* [Esporta dati da una visualizzazione Campaign Management](campaign-export-data.md)
>* [Video: struttura dell&#39;account DSP e interfaccia utente](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/ui.html)
