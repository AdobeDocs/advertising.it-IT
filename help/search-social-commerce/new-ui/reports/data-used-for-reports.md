---
title: (Nuova interfaccia) Dati utilizzati per i rapporti
description: Scopri i diversi tipi di dati disponibili nelle visualizzazioni dati e nei rapporti personalizzati.
feature: Search Reports
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: ff99aaef-142d-4c93-a88c-011e979e3843id: c916feea-e212-4773-b673-4daed287b8a3id: adcb1be7-7ed0-464d-a8d4-c905c9d47742id: fa0141e5-dc99-4fbd-9c0e-40aff66de606id: b36a77b1-3c8f-4e1c-8b0b-6e0ba3fb2664id: e246c273-d720-4ece-b29b-7aaba7d50169
source-git-commit: 18f4c5afafd63a6ae9421bf80b4e5b5fd424ed86
workflow-type: tm+mt
source-wordcount: 604
ht-degree: 0%

---

# (Nuova interfaccia) Dati utilizzati per i rapporti

Search, Social e Commerce includono un set completo di rapporti sulle prestazioni basati sui dati di clic e conversione. È possibile visualizzare i dati delle prestazioni di base per i vari componenti di un portfolio o di un account annuncio dalle visualizzazioni [!UICONTROL Portfolios] e [!UICONTROL Campaigns] nonché generando vari rapporti di base e avanzati.

Gli inserzionisti che utilizzano il servizio di monitoraggio delle conversioni di Adobe Advertising possono inoltre identificare il numero di clic per una posizione geografica o un nome di dominio di un sito Web di provenienza, il modo in cui gli annunci in ciascun canale e i vari eventi che portano a una conversione contribuiscono al tasso di conversione complessivo e la distribuzione delle conversioni per una singola [metrica di conversione](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) per canale di marketing. I rapporti disponibili variano in base al tipo di account utente. Il team dell’account di Adobe ha accesso a tutti i rapporti.

La maggior parte dei rapporti può essere personalizzata in modo da visualizzare solo le informazioni desiderate. Le metriche standard seguenti sono disponibili nella maggior parte dei rapporti e vengono calcolate a livello di annuncio:

* **Metriche delle prestazioni standard:**

   * **[!UICONTROL Impressions]:** Il numero totale di volte in cui l&#39;annuncio è stato inserito.

   * **[!UICONTROL Clicks]:** Il numero totale di volte in cui è stato fatto clic su un collegamento nell&#39;annuncio.

   * **[!UICONTROL Cost]:** Il costo totale dell&#39;annuncio. Il costo per la pubblicità pay-per-click (PPC) è sempre il numero di clic moltiplicato per il costo per clic.

   * **[!UICONTROL Cost per Click]:** Il costo medio di un clic per un annuncio, che è il costo dell&#39;annuncio diviso per il numero totale di clic per l&#39;annuncio. Ad esempio, se spendi 100 USD per un’impression pubblicitaria e l’annuncio genera 10 clic, il costo per clic è di 100 USD/10=10 USD per clic.

   * **[!UICONTROL Average Position]:** (se applicabile) La posizione media di un annuncio che è stato inserito, ponderata dal numero di impression.

   * **[!UICONTROL Estimated Clicks]:** (incluso nei report avanzati solo per gli inserzionisti con il servizio di monitoraggio delle conversioni di Adobe Advertising) Il numero totale di clic stimati per una città o un nome di dominio di un sito Web di provenienza. Ciò può includere dati per reti pubblicitarie per le quali un inserzionista non ha un account pubblicitario.

* **Metriche di conversione:** il numero totale di conversioni per ciascuna delle metriche di conversione dell&#39;inserzionista o i dati delle transazioni tracciati verso una metrica di conversione. Possono essere incluse le metriche di conversione e di coinvolgimento del sito, ma non le metriche calcolate e le metriche calcolate avanzate, che sono sincronizzate da Adobe Analytics.

  Possono essere incluse anche [[!DNL Google Ads] conversioni tracciate](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md) e [[!DNL Google Analytics] conversioni tracciate](/help/search-social-commerce/admin/data-sources/data-source-about.md) sincronizzate per l&#39;account dell&#39;inserzionista.

* **Metriche personalizzate:** Le metriche personalizzate derivate dalla creazione di formule basate su metriche esistenti, ad esempio il costo per ordine.

## Disponibilità dei dati

Quando si generano i rapporti, è possibile scegliere come attribuire i dati di conversione in una serie di eventi che portano a una conversione. Ad esempio, puoi scegliere di attribuire l’intera conversione all’ultimo evento o di ponderare l’ultimo evento più degli altri. Per impostazione predefinita, le conversioni sono attribuite all’ultimo evento.

A seconda della regola di attribuzione specificata per il rapporto, i dati per ciascun tipo di rapporto sono disponibili per le date seguenti.

| Gruppo di rapporti | Report | Date per le quali sono disponibili i dati |
| --- | --- | --- |
| [!UICONTROL Basic Reports] | [!UICONTROL Campaign Hourly Report] | A partire dal 15 maggio 2021.<br><br><b>Eccezione:</b> i dati delle metriche di prominenza sono disponibili a partire dall&#39;8 settembre 2022. |
| | Tutti gli altri [!UICONTROL Basic Reports] | I 36 mesi precedenti.<br><br><b>Eccezione:</b> I dati delle metriche di prominenza sono disponibili a partire dall&#39;8 settembre 2022. |
| [!UICONTROL Advanced Reports] | [!UICONTROL Transaction Report] | I 45 giorni precedenti. |
| | [!UICONTROL Domain Referral Report], [!UICONTROL Geo Distribution Report] | I due (2) mesi precedenti più il mese corrente. |
| [!UICONTROL Assist Reports] | Tutti | I 18 mesi precedenti. |
| [!UICONTROL Specialty Reports] | [!UICONTROL AdWords Audience Target Report] | L&#39;anno precedente. |
| | [!UICONTROL Google Asset Group Performance Report] | Nessuna limitazione |
| | [!UICONTROL MSA Ad Extension by Ad Report], [!UICONTROL MSA Ad Extension by Keyword Report], [!UICONTROL MSA Ad Extension Detail Report], [!UICONTROL MSA Network Impression Share Report], [!UICONTROL MSA Network Performance Report] | Ultimi 180 giorni. |
| | [!UICONTROL RSA Assets Report] | A decorrere dal 10 agosto 2022. |
| | Tutti gli altri [!UICONTROL Specialty Reports] | I due (2) mesi precedenti. |
| [!UICONTROL Model Accuracy Reports] | [!UICONTROL Forecast Accuracy Report] | I 18 mesi precedenti. |
| [!UICONTROL Change History Report] | — | I 31 giorni precedenti. |

>[!MORELIKETHIS]
>
>* [Informazioni sui report](report-about.md)
>* [Attività di installazione iniziali per i report](initial-setup.md)
