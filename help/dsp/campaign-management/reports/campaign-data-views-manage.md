---
title: Gestire le visualizzazioni dati della campagna
description: Scopri come personalizzare le visualizzazioni dati per campagne, pacchetti, posizionamenti e annunci.
feature: DSP Campaign Data Views
source-git-commit: 61ca25565e09bbce505d6f5cb0e5e8b7214eb1e0
workflow-type: tm+mt
source-wordcount: '914'
ht-degree: 0%

---

# Gestire le visualizzazioni dati della campagna

Puoi personalizzare i dati visualizzati nelle visualizzazioni di gestione delle campagne ([!UICONTROL Campaigns], [!UICONTROL Packages], [!UICONTROL Placements], e [!UICONTROL Ads]).

## Gestire le visualizzazioni dati {#data-visualizations-manage}

Puoi modificare le metriche e la modalità grafico per tutte le visualizzazioni di dati nelle campagne o per una singola campagna. Le modifiche apportate a una singola campagna vengono applicate a tutte le visualizzazioni di dati della campagna, incluse quelle in [!UICONTROL Packages], [!UICONTROL Placements], e [!UICONTROL Ads] visualizzazioni.

### Modificare le metriche per una visualizzazione dati

1. In alto a destra nella visualizzazione dati, fai clic su ![Impostazioni](/help/dsp/assets/settings-chart.png).

1. Seleziona le metriche.

   Non puoi selezionare la stessa metrica due volte.

1. Clic **[!UICONTROL Apply]**.

### Modificare la modalità di visualizzazione di una visualizzazione dati

* In alto a destra nella visualizzazione dati, fai clic su [!UICONTROL Overlay] switch (![Interruttore di sovrapposizione](/help/dsp/assets/overlay.png)) per passare dalla modalità di sovrapposizione (tutti i grafici sovrapposti) alla modalità grafico a traliccio (tre grafici separati).

## Gestire le tabelle dati {#data-tables-manage}

In tutte le visualizzazioni di gestione delle campagne ([!UICONTROL Campaigns], [!UICONTROL Packages], [!UICONTROL Placements], e [!UICONTROL Ads]), è possibile personalizzare i dati visualizzati all&#39;interno della tabella dati.

### Gestisci visualizzazioni colonne {#column-views-manage}

Ogni livello di gestione della campagna ([!UICONTROL Campaigns], [!UICONTROL Packages], [!UICONTROL Placements], e [!UICONTROL Ads]) include [!UICONTROL Pacing] e [!UICONTROL Performance] visualizzazioni che includono metriche rilevanti per tale entità. Per impostazione predefinita, il [!UICONTROL Pacing] viene mostrata in modo da poter identificare immediatamente le campagne e i componenti della campagna con prestazioni meno soddisfacenti. Facoltativamente, puoi creare e modificare set di colonne personalizzati.

![selettore vista a colonne](/help/dsp/assets/column-view-selector.png)

DSP salva la visualizzazione più recente come predefinita, in modo che, ogni volta che ritorni alla pagina, puoi sempre visualizzare le metriche pertinenti.

#### Modificare la vista a colonne {#column-view-change}

* Nel selettore Visualizza, fai clic su ![freccia giù](/help/dsp/assets/chevron-down.png), quindi fare clic sul nome della vista a colonne desiderata.

#### Creare una vista a colonne personalizzata {#column-view-create}

1. Nel selettore Visualizza, fai clic su ![freccia giù](/help/dsp/assets/chevron-down.png)e quindi fare clic su **[!UICONTROL Create View]**.

1. Specifica le metriche da includere nella visualizzazione:

   1. Nell’elenco delle metriche disponibili, seleziona la casella di controllo accanto a ciascuna metrica da includere.

      Tutte le metriche sono alfabetiche per categoria: [!UICONTROL Settings], [!UICONTROL Spend], [!UICONTROL Pacing], [!UICONTROL Reporting] (metriche standard monitorate dall’DSP), [!UICONTROL Viewability], e [!UICONTROL Conversions]. Metriche aggiunte con &quot;([!UICONTROL Lifetime])&quot; restituiscono i valori dall&#39;inizio della campagna, indipendentemente dall&#39;intervallo di date selezionato nella pagina.

   1. Se necessario, modifica l’ordine delle colonne facendo clic sui nomi delle colonne nel pannello di destra e trascinandoli nelle posizioni desiderate.

   Alcune colonne hanno posizioni fisse e non possono essere spostate o rimosse.

1. Applica o salva le impostazioni:

   * Per applicare temporaneamente le impostazioni senza salvarle nella visualizzazione, fare clic su **[!UICONTROL Apply].**

   * Per salvare le impostazioni in una nuova vista a colonne personalizzata, fai clic su **[!UICONTROL Save As]**. In [!UICONTROL Save View] , immettere il nome della nuova visualizzazione e quindi fare clic su **[!UICONTROL Save]**.

#### Modificare una vista a colonne {#column-view-edit}

>[!NOTE]
>
>Non è possibile salvare le modifiche apportate a una vista a colonne standard (predefinita), ma è possibile applicarle temporaneamente o salvarle in una nuova vista personalizzata.

1. Nel selettore Visualizza, fai clic su ![freccia giù](/help/dsp/assets/chevron-down.png), quindi fare clic sul nome della vista a colonne esistente.

1. Nel selettore Visualizza, fai clic su ![freccia giù](/help/dsp/assets/chevron-down.png)e quindi fare clic su **[!UICONTROL Edit View]**.

1. Modifica le metriche da includere nella visualizzazione:

   1. Nell’elenco delle metriche disponibili, seleziona la casella di controllo accanto a ciascuna metrica da includere e deseleziona la casella di controllo accanto a ciascuna metrica da escludere.

      Tutte le metriche sono alfabetiche per categoria: [!UICONTROL Settings], [!UICONTROL Spend], [!UICONTROL Pacing], [!UICONTROL Reporting] (metriche standard monitorate dall’DSP), [!UICONTROL Viewability], e [!UICONTROL Conversions]. Metriche aggiunte con &quot;([!UICONTROL Lifetime])&quot; restituiscono i valori dall&#39;inizio della campagna, indipendentemente dall&#39;intervallo di date selezionato nella pagina.

   1. Se necessario, modifica l’ordine delle colonne facendo clic sui nomi delle colonne nel pannello di destra e trascinandoli nelle posizioni desiderate.

   Alcune colonne hanno posizioni fisse e non possono essere spostate o rimosse.

1. Applica o salva le impostazioni:

   * (Solo visualizzazioni personalizzate) Per salvare le impostazioni, fai clic su **[!UICONTROL Save]**.

   * Per applicare temporaneamente le impostazioni senza salvarle nella visualizzazione, fare clic su **[!UICONTROL Apply].**

   * Per salvare le impostazioni in una nuova vista a colonne personalizzata, fai clic su **[!UICONTROL Save As]**. In [!UICONTROL Save View] , immettere il nome della nuova visualizzazione e quindi fare clic su **[!UICONTROL Save]**.

### Filtrare i dati della campagna {#filter-data-tables}

I filtri modificano i dati visualizzati nella scheda corrente. I filtri disponibili variano in base al tipo di entità, ma possono includere il nome dell’entità, lo stato e colonne di proprietà aggiuntive.

1. Nella barra degli strumenti principale, fai clic su ![Pulsante Filtro](/help/dsp/assets/filter.png).
1. Per ogni filtro che si desidera applicare, fare clic sul nome del filtro nella colonna sinistra e quindi specificare il valore del filtro.
1. Clic **[!UICONTROL Apply]**.

#### Filtri disponibili

Sono disponibili i seguenti filtri per [!UICONTROL Campaigns], [!UICONTROL Packages], e [!UICONTROL Placements] visualizzazioni:

* [!UICONTROL Campaigns] visualizza filtri:
   * [!UICONTROL Campaign status]
   * [!UICONTROL Advertiser]
* [!UICONTROL Packages] visualizza filtri:
   * [!UICONTROL Custom flights] (che esistano o meno)
   * [!UICONTROL Custom goal] (se applicabile)
   * [!UICONTROL End end date]
   * [!UICONTROL Optimization goal]
   * [!UICONTROL Flight pacing]
   * [!UICONTROL Intraday pacing]
   * [!UICONTROL Package status]
   * [!UICONTROL Start date]
* [!UICONTROL Placements] visualizza filtri:
   * [!UICONTROL Custom ad scheduling]
   * [!UICONTROL Custom goal] (se applicabile)
   * [!UICONTROL End date]
   * [!UICONTROL Max bid] ([!UICONTROL less than], [!UICONTROL greater than], o [!UICONTROL equal to] un valore specificato)
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
* [!UICONTROL Ads] visualizza filtri:
   * [!UICONTROL Adobe ad approval status]
   * [!UICONTROL Ad ID]
   * [!UICONTROL Ad name]
   * [!UICONTROL Ad type]
   * [!UICONTROL Creation date]


### Modificare l’intervallo di date

Modifica l’intervallo di date utilizzato in tutte le visualizzazioni standard e personalizzate utilizzando il selettore dell’intervallo di date sopra qualsiasi tabella di dati.

![Selettore intervallo di date](/help/dsp/assets/date-range-selector.png "Selettore intervallo di date")

* Per un intervallo predefinito: selezionalo dall’elenco degli incrementi di tempo comuni. Il valore predefinito è [!UICONTROL Last 30 days]*.

* Per un intervallo specifico, effettuare una delle seguenti operazioni:

   * Clic ![Calendario](/help/dsp/assets/calendar.png "Calendario")e quindi fare clic sulla data di inizio e sulla data di fine all&#39;interno del calendario.

   * Fare clic all&#39;interno dell&#39;intervallo di date, quindi immettere una data di inizio e una data di fine oppure selezionarle all&#39;interno del calendario.

     È possibile immettere valori numerici (da M-D-AA a MM-GG-AAAA) e/o nomi o abbreviazioni dei mesi (ad esempio Gen o Gennaio).

### Ordinare una colonna di dati

Puoi ordinare qualsiasi colonna di dati in ordine crescente (dalla A alla Z o da 1 a 10) o decrescente (dalla Z alla A o da 10 a 1).

* Fai clic sull’intestazione della colonna per passare dall’ordine crescente a quello decrescente.


### Specifica il numero di righe di dati

In basso a destra di qualsiasi pagina, accanto a **[!UICONTROL Items per page]** , seleziona *[!UICONTROL 25]*, *[!UICONTROL 50]*, o *[!UICONTROL 100]*.

>[!MORELIKETHIS]
>
>* [Informazioni sui rapporti sulle prestazioni nelle visualizzazioni di Campaign Management](campaign-reports-about.md)
>* [Visualizzare i dettagli di Siti, Annunci e Frequenza per un posizionamento](placement-details-view.md)
>* [Visualizza il rapporto Previsione posizionamento](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [Visualizzare i rapporti di diagnostica del posizionamento](placement-diagnostics.md)
>* [Esportare dati da una vista Campaign Management](campaign-export-data.md)
>* [Video: Struttura dell&#39;account DSP e interfaccia utente](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/ui.html)
