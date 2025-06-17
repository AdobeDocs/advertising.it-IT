---
title: Rapporti sulle prestazioni a livello di esperienza
description: Scopri come visualizzare i rapporti sulle prestazioni a livello di esperienza.
feature: Creative Experiences
exl-id: 5e7c4c9d-b992-460a-9765-4276027f9a61
source-git-commit: 1718a7f5a7e3bbfeed336b195a2575275c8fd753
workflow-type: tm+mt
source-wordcount: '776'
ht-degree: 0%

---

# Rapporti sulle prestazioni a livello di esperienza

*Versione beta chiusa*

Puoi visualizzare dati dettagliati sulle prestazioni per qualsiasi esperienza.

## Dati nei rapporti sulle prestazioni a livello di esperienza

La visualizzazione Report include i dati seguenti:

* **Panoramica** scheda: panoramica delle prestazioni in tutte le metriche di conversione per l&#39;intera esperienza<!-- Currently, the only metric in the settings list at the top of this main tab is "Select All." -->, inclusi:

   * **Prestazioni generali** sezione:

      * **Prestazioni complessive**: impression totali; clic; tasso di click-through (CTR); conversioni view-through e click-through.

     <!--
     ![Overall performance](/help/creative/assets/experience-report-overall-performance.png "Overall performance"){width="100" zoomable="yes"}
          -->

      * **Percentuale predefinita**: (solo esperienze con targeting di albero delle decisioni) il numero di impression risultanti da creativi di destinazione, da creativi generici senza target o indirizzati a &quot;Tutti gli altri&quot; e dalla creatività predefinita per l&#39;esperienza.

     <!--
     ![Default rate](/help/creative/assets/experience-report-default-rate.png "Default rate"){width="100" zoomable="yes"} 
     -->

   * **Sezione Performance Breakdown**:

      * **Prestazioni regionali:*: singole metriche per posizione geografica.

        <!--   
      ![Regional performance](/help/creative/assets/experience-report-regional-performance.png "Regional performance"){width="100" zoomable="yes"}
      -->

      * **Prestazioni dispositivo:** singole metriche per tipo di dispositivo, sistema operativo e browser. Facoltativamente, fai clic sul valore per qualsiasi categoria di dispositivi per visualizzare un elenco delle prime 10 creatività distribuite con tale criterio.

        <!--    
      ![Device performance](/help/creative/assets/experience-report-device-performance.png "Device performance"){width="100" zoomable="yes"}
      -->

* **Scheda Prestazioni di Creative***: panoramica delle prestazioni in base al contenuto creativo e al bundle o al tag dell&#39;annuncio, inclusi:

   * Scheda secondaria **Creativi**: numero totale di impression, clic e CTR per ogni creatività nell&#39;esperienza.<!-- No breakdown yet for the individual ad elements and/or the served ads. -->

   * Scheda secondaria **Bundle/Tag**: numero totale di impression, clic e CTR per i singoli bundle (esperienze con targeting dell&#39;albero delle decisioni) o tag di annunci (esperienze senza targeting dell&#39;albero delle decisioni) nell&#39;esperienza.

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

      * Per specificare un intervallo di date personalizzato, immettere la data di inizio e la data di fine oppure fare clic sull&#39;![icona calendario](/help/search-social-commerce/assets/calendar.png) accanto a un campo e selezionare una data.

   * (Facoltativo) Per modificare la regola utilizzata per attribuire i dati di conversione in una serie di eventi che portano a una conversione, fare clic su ![Impostazioni](/help/creative/assets/settings.png) e modificare **[!UICONTROL Attribution Rule]**.

     Per ulteriori informazioni sulle regole di attribuzione, vedere &quot;[Modalità di calcolo delle regole di attribuzione](/help/search-social-commerce/reports/attribution-rules.md).&quot;

   * (Facoltativo) Per modificare le conversioni segnalate, fare clic su ![Impostazioni](/help/creative/assets/settings.png) e selezionare i nomi delle conversioni nel menu **[!UICONTROL Conversions]**. Attualmente, l’unica metrica disponibile è &quot;Seleziona tutto&quot; per includere tutte le metriche di conversione.

     Le colonne di conversione disponibili includono le conversioni disponibili in Advertising Search, Social e Commerce, indipendentemente dal fatto che tu sia un cliente di Search, Social e Commerce. L&#39;elenco può includere le metriche di conversione e di coinvolgimento del sito sincronizzate da Adobe Analytics quando l&#39;inserzionista ha [un [!DNL Adobe Analytics for Advertising] integrazione](/help/integrations/analytics/overview.md). [!DNL Analytics] metriche calcolate e metriche calcolate avanzate non sono disponibili. Per ulteriori informazioni sull&#39;inclusione delle conversioni raccolte nei report, vedere l&#39;argomento &quot;[Informazioni sulla gestione delle metriche di conversione di un inserzionista](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)&quot; nella Guida di Search, Social e Commerce.

1. Nella scheda [!UICONTROL Overview]:

   * (Facoltativo) Nella sezione [!UICONTROL Overall Regional Performance], tenere premuto il cursore su un punto del grafico per visualizzare i dati relativi a tale punto.

   * (Facoltativo) Nella sezione [!UICONTROL Regional Performance] eseguire una delle operazioni seguenti:

      * Fare clic sul nome di una metrica, ad esempio [!UICONTROL Impressions], per visualizzarla.

      * Selezionare l&#39;area nel menu [!UICONTROL Region].

      * Posizionare il cursore su un paese o uno stato per visualizzare i dati relativi a tale area.

   * (Facoltativo) Nella sezione [!UICONTROL Device Performance] eseguire una delle operazioni seguenti:

      * Tenere premuto il cursore sul valore di qualsiasi categoria di dispositivi per visualizzare i dati relativi a tali criteri.

      * Fai clic sul valore per qualsiasi categoria di dispositivi per visualizzare un elenco delle prime<!-- NN--> creative distribuite con tali criteri.

1. (Facoltativo) Per visualizzare i dati per creatività e per bundle o tag annuncio, fare clic sulla scheda **[!UICONTROL Creative Performance]**.

   * Nella scheda secondaria [!UICONTROL Creatives] è possibile eseguire una delle operazioni seguenti:

      * (Facoltativo) Per passare dalla visualizzazione grafico alla visualizzazione griglia e viceversa, fare clic rispettivamente su ![Grafico](/help/creative/assets/chart-view-button.png "Grafico") e ![Griglia](/help/creative/assets/table-view-button.png "Griglia").

      * (Facoltativo) Nella vista grafico, posizionare il cursore su un punto del grafico per visualizzare i dati relativi a tale punto.

      * (Esperienze con solo targeting della struttura decisionale; facoltativo) Per suddividere le prestazioni per ogni destinazione annuncio applicata, abilita **[!UICONTROL Split targeting]**.

1. Per visualizzare i dati per bundle (esperienze con targeting di struttura decisionale) o tag annuncio (esperienze senza targeting di struttura decisionale), fai clic sulla scheda secondaria **[!UICONTROL Bundles]**. È possibile effettuare una delle seguenti operazioni:

   * (Facoltativo) Per passare dalla visualizzazione grafico alla visualizzazione griglia e viceversa, fare clic rispettivamente su ![Grafico](/help/creative/assets/chart-view-button.png "Grafico") e ![Griglia](/help/creative/assets/table-view-button.png "Griglia").

   * (Facoltativo) Nella vista grafico, posizionare il cursore su un punto del grafico per visualizzare i dati relativi a tale punto.

   * (Esperienze con solo targeting della struttura decisionale; facoltativo) Per suddividere le prestazioni per ogni destinazione annuncio applicata, abilita **[!UICONTROL Split targeting]**.

## Scaricare rapporti sulle prestazioni per un’esperienza

* Nella barra degli strumenti nella parte superiore dei report sulle prestazioni, fai clic su ![Scarica](/help/creative/assets/download.png "Scarica").

  Il file viene scaricato in un file [!DNL Microsoft Excel] in formato foglio di calcolo (XLSX), in base alla normale procedura del browser.

>[!MORELIKETHIS]
>
>* [Report Creative personalizzato](/help/creative/report-custom-creative.md)
>* [Scarica tutte le esperienze nella visualizzazione](/help/creative/experiences/experience-download-view.md)
>* [Informazioni sulle esperienze in Advertising Creative](/help/creative/experiences/experience-about.md)
