---
title: Gestisci le metriche di conversione di un inserzionista in DSP.
description: Scopri come utilizzare le metriche di conversione tracciate da Adobe Advertising per un inserzionista DSP.
feature: Conversions
source-git-commit: e2746d58fa512f032a1e4ff851d23876cd63fc93
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 0%

---

# Gestire le metriche di conversione di un inserzionista

Le metriche di conversione di un inserzionista vengono utilizzate in Adobe Advertising:

* In Advertising DSP, puoi includere le metriche di conversione nelle viste di gestione delle campagne, negli obiettivi personalizzati e nei rapporti personalizzati. Puoi anche utilizzare le metriche di conversione di un inserzionista per creare [obiettivi personalizzati](/help/dsp/admin/custom-objectives-manage.md), utilizzati per ottimizzare i pacchetti.

* (Inserzionisti con Advertising Search, Social e Commerce) In Search, Social e Commerce, i dati per le metriche di conversione possono essere visualizzati in colonne nelle viste Campagna, Portfolio e Gestione obiettivi e nei rapporti. Gli utenti con privilegi di accesso sufficienti possono inoltre utilizzare metriche di conversione per creare obiettivi, utilizzati per ottimizzare i portfolio.

<!--
The conversion metrics that Adobe Advertising tracks for an advertiser &mdash; including [conversion and site engagement metrics synced from Adobe Analytics](/help/integrations/analytics/analytics-data-in-advertising.md), [site events synced from Adobe Customer Journey Analytics](/help/integrations/customer-journey-analytics/overview.md), and custom feeds &mdash; are used throughout Advertising DSP. You can include conversion metrics in campaign management views, custom objectives, and custom reports. You can also use conversion metrics to create [custom objectives](/help/dsp/admin/custom-objectives-manage.md), which are used to optimize packages.

By default, none of an advertiser's conversion metrics are available for campaign management views, custom objectives, and reports. They are available only when you specifically make them available. When you make a conversion metric available, you can either use the metric name exactly as it is spelled in the retrieved data or change the display name that's shown in column headings for readability.

From the list of visible metrics, each user with access to the advertiser's data can customize the metrics they see for campaign management views, objectives, and reports by including or omitting specific metrics. Users with sufficient access privileges can also optimize for specific metrics by associating them with DSP package-level custom goals.

-->

I tipi di metriche tracciate per gli utenti di DSP includono:

* Metriche di conversione di cui Adobe Advertising tiene traccia per un inserzionista.

* [Metriche di conversione e coinvolgimento sito sincronizzate da Adobe Analytics](/help/integrations/analytics/analytics-data-in-advertising.md).

* [Eventi del sito sincronizzati da Adobe Customer Journey Analytics](/help/integrations/customer-journey-analytics/overview.md).

* Conversioni da feed personalizzati.

Dall’elenco delle metriche di conversione disponibili, ogni utente con accesso ai dati dell’inserzionista può personalizzare le metriche visualizzate disponibili per le visualizzazioni e i rapporti di gestione, includendo o omettendo metriche specifiche a propria scelta. Puoi utilizzare un nome di metrica esattamente come è scritto nei dati recuperati oppure modificare il nome visualizzato nelle intestazioni di colonna per migliorarne la leggibilità.

>[!IMPORTANT]
>
>Per impostazione predefinita, nessuna delle metriche di conversione di un inserzionista è disponibile per l’inclusione nelle visualizzazioni di gestione delle campagne, negli obiettivi personalizzati e nei rapporti personalizzati. Per rendere disponibile una metrica di conversione, devi renderla esplicitamente disponibile.

>[!TIP]
>
>Quando l&#39;inserzionista (o la rete di annunci) interrompe la raccolta di una metrica di conversione, [nasconderla dalle visualizzazioni di gestione e dai report](#conversion-metrics-change-available) a meno che non si desideri utilizzarla per visualizzare i dati storici.

## Visualizzare le metriche di conversione tracciate per un inserzionista

* Nel menu principale, fare clic su **[!UICONTROL Settings]>[!UICONTROL Conversions Beta]**.

Sono elencate tutte le metriche di conversione raccolte per l’inserzionista e tutti i diversi nomi visualizzati assegnati. Ogni riga di metrica include l’origine della metrica.

## Modificare il nome visualizzato di una metrica di conversione

Se ad esempio si raccolgono i dati di registrazione utilizzando una metrica di conversione denominata *reg*, è possibile modificare il nome visualizzato in modo che venga visualizzato come &quot;Registrazioni&quot;.

Impossibile eliminare un nome visualizzato esistente.

1. Nel menu principale, fare clic su **[!UICONTROL Settings]>[!UICONTROL Conversions Beta]**.

1. Posizionare il cursore sulla riga e fare clic su **[!UICONTROL Edit Display Name]**.

1. Immettere il nome da visualizzare, quindi fare clic su **[!UICONTROL Save]**.

   I nomi visualizzati devono essere univoci e non possono includere i seguenti caratteri speciali: `\"<'>&`

## Modificare le metriche di conversione disponibili nelle visualizzazioni di gestione delle campagne, negli obiettivi personalizzati e nei rapporti personalizzati {#change-the-conversion-metrics-available-in-ui}

1. Nel menu principale, fare clic su **[!UICONTROL Settings]>[!UICONTROL Conversions]**.

   Sono elencate tutte le metriche di conversione raccolte per l’inserzionista e tutti i nomi diversi specificati per la visualizzazione.

1. (Facoltativo) Filtra l’elenco:

   1. Sopra l&#39;elenco, fare clic su ![Filtro](/help/dsp/assets/filter.png "Filtro").

   1. Specificare i filtri, quindi fare clic su **[!DNL Apply]**.

      Puoi filtrare le metriche in base all’AMO Client ID (ID client AMO), a seconda che siano visibili o nascoste nell’interfaccia utente, e in base all’origine dati.

1. Modificare le metriche di conversione disponibili per le visualizzazioni e i rapporti di gestione:

   * Per visualizzare una metrica, posizionare il cursore sulla riga e fare clic su **[!UICONTROL Show in UI and Reports]**.

   * Per nascondere una metrica, posizionare il cursore sulla riga e fare clic su **[!UICONTROL Hide in UI and Reports]**.

>[!MORELIKETHIS]
>
>* [Gestisci le visualizzazioni dati della campagna](/help/dsp/campaign-management/reports/campaign-data-views-manage.md)
>* [Gestisci obiettivi personalizzati](/help/dsp/admin/custom-objectives-manage.md)
