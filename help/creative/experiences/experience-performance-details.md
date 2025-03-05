---
title: Rapporti sulle prestazioni a livello di esperienza
description: Scopri come visualizzare i rapporti sulle prestazioni a livello di esperienza.
feature: Creative Experiences
exl-id: 5e7c4c9d-b992-460a-9765-4276027f9a61
source-git-commit: 8d88a46e82a17ce5d2debf93ea0652f35a734d7a
workflow-type: tm+mt
source-wordcount: '744'
ht-degree: 0%

---

# Rapporti sulle prestazioni a livello di esperienza

*Versione beta chiusa*

Puoi visualizzare dati dettagliati sulle prestazioni per qualsiasi esperienza.

## Dati nei rapporti sulle prestazioni a livello di esperienza

La visualizzazione Report include i dati seguenti:

* **Panoramica** scheda: panoramica delle prestazioni per l&#39;intera esperienza, inclusi:

   * **Prestazioni generali** sezione:

   * **Prestazioni generali**: impression totali; clic; tasso di click-through (CTR); conversioni view-through e click-through per una singola metrica di conversione. <!-- Just one, or can you select multiple? And I don't see this as of 2/8:  You can optionally combine two metrics at a time into a single chart. -->

     <!--
     ![Overall performance](/help/creative/assets/experience-report-overall-performance.png "Overall performance"){width="100" zoomable="yes"}
          -->

   * **Percentuale predefinita**: (solo esperienze con targeting di albero delle decisioni) il numero di impression risultanti da creativi di destinazione, da creativi generici senza target o destinati a &quot;Tutti gli altri&quot; e dalla creatività predefinita per l&#39;esperienza.

     <!--
     ![Default rate](/help/creative/assets/experience-report-default-rate.png "Default rate"){width="100" zoomable="yes"} 
     -->

   * **Sezione Performance Breakdown**:

      * **Prestazioni regionali:*: singole metriche per posizione geografica.

        <!-- You can optionally do the following:
    
      * Click a metric name (such as [!UICONTROL Impressions]) to view that metric.

      * Select the region in the **[!UICONTROL Region]** menu.
      
      -->

        <!--   
      ![Regional performance](/help/creative/assets/experience-report-regional-performance.png "Regional performance"){width="100" zoomable="yes"}
      -->

      * **Prestazioni dispositivo:** singole metriche per tipo di dispositivo, sistema operativo e browser. Se necessario, fai clic sul valore per qualsiasi categoria di dispositivi per visualizzare un elenco delle prime <!-- NN --> creative distribuite con tale criterio.

        <!--    
      ![Device performance](/help/creative/assets/experience-report-device-performance.png "Device performance"){width="100" zoomable="yes"}
      -->

* **Scheda Prestazioni creative***: panoramica delle prestazioni per tag di annunci o bundle creativi e, tra cui:

   * Scheda secondaria **Creativi**: numero totale di impression, clic e CTR per ogni creatività nell&#39;esperienza.<!-- No breakdown yet for the individual ad elements and/or the served ads. -->

     <!--

     * *Experiences with decision tree targeting:* The total number of impressions, clicks, and CTR for each creative. You can optionally do the following:
     
       * To break out the performance for each ad target, enable **[!UICONTROL Split targeting]**.

       * To switch between the grid view and a trend chart, which includes the addition of view-through conversions and click-through conversions (using the conversions specified in the top toolbar), click ![Chart](/help/creative/assets/chart-view-button.png "Chart") and ![Grid](/help/creative/assets/table-view-button.png "Grid") above the report. [Find out about this:  ..., and total conversions for specified conversion metricsYour conversion metrics are combined into one Conversions column set unless you have made individual metric column sets available within Advertising Cloud Search.]

     * *Experiences without decision tree targeting:* The total number of impressions, clicks, and click-through rate (CTR) for each creative. You can optionally do the following:

       * To switch between the grid view and a trend chart, which includes the addition of view-through conversions and click-through conversions (using the conversions specified in the top toolbar), click ![Chart](/help/creative/assets/chart-view-button.png "Chart") and ![Grid](/help/creative/assets/table-view-button.png "Grid") above the report.

     -->

   * Scheda secondaria **Bundle/Tag**: numero totale di impression, clic e CTR per i singoli bundle (esperienze con targeting dell&#39;albero delle decisioni) o tag di annunci (esperienze senza targeting dell&#39;albero delle decisioni) nell&#39;esperienza.

     <!--
   
     * *Experiences with decision tree targeting:* The total number of impressions, clicks, and CTR for each bundle. You can optionally do the following:
     
       * To break out the performance for each ad target, enable **[!UICONTROL Split targeting]**.

       * To switch between the grid view and a trend chart, which includes the addition of view-through conversions  and click-through conversions (using on the conversions specified in the top toolbar), click ![Chart](/help/creative/assets/chart-view-button.png "Chart") and ![Grid](/help/creative/assets/table-view-button.png "Grid") above the report.

     * *Experiences without decision tree targeting:* The total number of impressions, clicks, and click-through rate (CTR) for each ad tag. You can optionally do the following:

       * To switch between the grid view and a trend chart, which includes the addition of view-through conversions and click-through conversions (using the conversions specified in the top toolbar), click ![Chart](/help/creative/assets/chart-view-button.png "Chart") and ![Grid](/help/creative/assets/table-view-button.png "Grid") above the report.

     -->

## Visualizzare i rapporti sulle prestazioni per un’esperienza

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. (Facoltativo) [Personalizza la visualizzazione](/help/creative/introduction/customize-data-views.md) per includere esperienze specifiche.

1. Seleziona l&#39;esperienza:

   * Nella vista a schede, fai clic su **[!UICONTROL ...]** accanto al nome dell&#39;esperienza e quindi su **[!UICONTROL Reports]**.

   * Nella vista tabella, tenere il cursore sulla riga e fare clic su **[!UICONTROL Reports]**.

   Verrà aperta la scheda [!UICONTROL Overview].

1. (Facoltativo) Nella barra degli strumenti in alto a destra, specifica l’intervallo di date, la regola di attribuzione della conversione e le conversioni riportate in tutti i rapporti sulle prestazioni:

   * (Facoltativo) Per modificare l&#39;intervallo di date per i dati sulle prestazioni, scegliere un&#39;opzione nel menu data:

      * Per specificare un periodo predefinito, selezionare il report: (*[!UICONTROL Last Month-to-date],* *[!UICONTROL Last 7 days],* *[!UICONTROL Last 30 days],* *[!UICONTROL Last 7 days],* *[!UICONTROL Last 30 days],* *[!UICONTROL Today],* o *[!UICONTROL Yesterday]*.

      * Per specificare un intervallo di date personalizzato, specificare la data di inizio e la data di fine <!-- in the format MM/DD/YYYY or M/D/YYYY,--> oppure fare clic sull&#39;![icona calendario](/help/search-social-commerce/assets/calendar.png) accanto a un campo e selezionare una data.

   * (Facoltativo) Per modificare la regola utilizzata per attribuire i dati di conversione in una serie di eventi che portano a una conversione, fare clic su ![Impostazioni](/help/creative/assets/settings.png) e modificare **[!UICONTROL Attribution Rule]**.

   * (Facoltativo) Per modificare le conversioni segnalate, fare clic su ![Impostazioni](/help/creative/assets/settings.png) e selezionare i nomi delle conversioni nel menu **[!UICONTROL Conversions]**.&lt;!— Solo uno o più? Verifica la visualizzazione: devo vedere un inserzionista con più conversioni già impostate —>

     Le colonne di conversione disponibili includono le conversioni disponibili in Advertising Search, Social e Commerce, indipendentemente dal fatto che tu sia un cliente di Search, Social e Commerce. Questo può includere metriche di conversione e coinvolgimento del sito sincronizzate da Adobe Analytics quando l&#39;inserzionista ha [un [!DNL Adobe Analytics for Advertising] integrazione](/help/integrations/analytics/overview.md). <!--Analytics calculated metrics and advanced calculated metrics aren't available.--> Per ulteriori informazioni sull&#39;inclusione delle conversioni raccolte nei report, vedere l&#39;argomento &quot;[Informazioni sulla gestione delle metriche di conversione di un inserzionista](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)&quot; nella Guida di Search, Social e Commerce.

1. Nella scheda [!UICONTROL Overview]:

   * (Facoltativo) Nella sezione [!UICONTROL Overall Regional Performance], tenere premuto il cursore su un punto del grafico per visualizzare i dati relativi a tale punto.

   * (Facoltativo) Nella sezione [!UICONTROL Regional Performance] eseguire una delle operazioni seguenti:

      * Fare clic sul nome di una metrica, ad esempio [!UICONTROL Impressions], per visualizzarla.

      * Selezionare l&#39;area nel menu [!UICONTROL Region].

      * Posizionare il cursore su un paese o uno stato per visualizzare i dati relativi a tale area.

   * (Facoltativo) Nella sezione [!UICONTROL Device Performance] eseguire una delle operazioni seguenti:

      * Tenere premuto il cursore sul valore per qualsiasi categoria di dispositivi per visualizzare i dati relativi a tali criteri.

      * Fai clic sul valore per qualsiasi categoria di dispositivi per visualizzare un elenco dei primi <!-- NN--> creativi serviti con quel criterio.

1. (Facoltativo) Per visualizzare i dati per creatività e per bundle o tag annuncio, fare clic sulla scheda **[!UICONTROL Creative Performance]**.

   * Nella scheda secondaria [!UICONTROL Creatives] è possibile eseguire una delle operazioni seguenti:

      * (Facoltativo) Per passare dalla visualizzazione grafico alla visualizzazione griglia e viceversa, fare clic rispettivamente su ![Grafico](/help/creative/assets/chart-view-button.png "Grafico") e ![Griglia](/help/creative/assets/table-view-button.png "Griglia").

      * (Facoltativo) Nella vista grafico, posizionare il cursore su un punto del grafico per visualizzare i dati relativi a tale punto.

      * (Esperienze con solo targeting della struttura decisionale; facoltativo) Per suddividere le prestazioni per ogni destinazione annuncio applicata, abilita **[!UICONTROL Split targeting]**.

1. Per visualizzare i dati per bundle (esperienze con targeting della struttura decisionale) o tag annuncio (esperienze senza targeting della struttura decisionale), fai clic sulla scheda secondaria **[!UICONTROL Bundles]**. È possibile effettuare una delle seguenti operazioni:

   * (Facoltativo) Per passare dalla visualizzazione grafico alla visualizzazione griglia e viceversa, fare clic rispettivamente su ![Grafico](/help/creative/assets/chart-view-button.png "Grafico") e ![Griglia](/help/creative/assets/table-view-button.png "Griglia").

   * (Facoltativo) Nella vista grafico, posizionare il cursore su un punto del grafico per visualizzare i dati relativi a tale punto.

   * (Esperienze con solo targeting della struttura decisionale; facoltativo) Per suddividere le prestazioni per ogni destinazione annuncio applicata, abilita **[!UICONTROL Split targeting]**.

1. (Facoltativo) Per scaricare i dati in un file [!DNL Microsoft Excel] in formato foglio di calcolo (XLSX), fare clic su ![Scarica](/help/creative/assets/download.png "Scarica") nella barra degli strumenti.

   Il file viene scaricato in base alla normale procedura del browser.

>[!MORELIKETHIS]
>
>* [Report Creative personalizzato](/help/creative/report-custom-creative.md)
