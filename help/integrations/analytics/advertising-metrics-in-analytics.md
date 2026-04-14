---
title: Metriche di Adobe Advertising in Analysis Workspace
description: Metriche e classificazioni di Adobe Advertising in Analysis Workspace
feature: Integration with Adobe Analytics
exl-id: da5e5704-4504-4fc5-93d2-db7d28f0c349
TQID: https://experienceleague.adobe.com/CLPeE8g0Mix4Scq90qCd-s-tCUuBmkTBrkBWT1aPEhw
autotag-review: '2026-04-13T23:29:38.865Z'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: f2860a4b-f905-4545-bead-1bbc92564592
subfeature_v2:
  - id: cfd751d4-ee56-4323-8fd1-dc174b031709
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 05f5454a520027b33ebe4e2fe8583569cb19e5df
workflow-type: tm+mt
source-wordcount: 190
ht-degree: 0%

---

# Metriche di Adobe Advertising in Analysis Workspace

*Inserzionisti con una sola integrazione Adobe Advertising-Adobe Analytics*

>[!NOTE]
>
>* Adobe Advertising trasmette ogni giorno le metriche e le classificazioni del traffico a [!DNL Analytics].
>* [!DNL Analytics] acquisisce i click-through e i view-through di Adobe Advertising in tempo reale.
>* Per [!DNL Search, Social, & Commerce], questa funzione è supportata per la maggior parte delle reti di annunci e dei tipi di campagne. Per ulteriori informazioni, vedere &quot;[Inventario supportato](/help/search-social-commerce/introduction/supported-inventory.md)&quot; nella Guida di [!DNL Search, Social, & Commerce].

## Metriche del traffico da Adobe Advertising

Le metriche del traffico di Adobe Advertising in [!DNL Analytics] in genere iniziano con &quot;Adobe Advertising&quot;, ad eccezione di &quot;[!UICONTROL AMO ID Instances]&quot;. Tuttavia, per i clienti a lungo termine che hanno utilizzato un evento personalizzato (anziché un evento riservato) per creare originariamente metriche per clic, costi e impression, tali metriche iniziano ancora con &quot;AMO&quot;.

Per l&#39;elenco, vedere &quot;[Metriche Adobe Advertising](https://experienceleague.adobe.com/en/docs/analytics/components/metrics/amo-metrics)&quot;.

<!--

| Traffic Metric | Description |
| -------------- | ----------- |
| [!UICONTROL Adobe Advertising Clicks] or (some legacy customers) [!UICONTROL AMO Clicks] | The number of total Adobe Advertising clicks. |
| [!UICONTROL Adobe Advertising Cost] or (some legacy customers) [!UICONTROL AMO Cost] | The Adobe Advertising spend in the currency of the report suite. |
| [!UICONTROL Adobe Advertising Impressions] or (some legacy customers) [!UICONTROL AMO Impressions] | The number of Adobe Advertising impressions. |
| [!UICONTROL Adobe Advertising Measurable Impressions] | The number of impressions that were served for which viewability instrumentation successfully initialized. This value is calculated as (instrumented impressions - the number of unmeasurable impressions). |
| [!UICONTROL Adobe Advertising Minutes Viewed] | The number of minutes an Adobe Advertising video was viewed. |
| [!UICONTROL Adobe Advertising Not Viewable Impressions] | The number of impressions that were determined to be not viewable. This value is calculated as ([!UICONTROL Adobe Advertising Measurable Impressions] - [!UICONTROL Adobe Advertising Viewable]). |
| [!UICONTROL Adobe Advertising Viewable Impressions] | The number of impressions that were measured to be viewable according to the placement configuration. |
| [!UICONTROL Adobe Advertising Views] | The number of views on an ad. A view is counted when the viewer initiates the Adobe Advertising video. |
| [!UICONTROL Adobe Advertising Views 25% Complete] | The number of views for which at least 25% of an Adobe Advertising video was watched. |
| [!UICONTROL Adobe Advertising Views 50% Complete] | The number of views for which at least 50% of an Adobe Advertising video was watched. |
| [!UICONTROL Adobe Advertising Views 75% Complete] | The number of views for which at least 75% of an Adobe Advertising video was watched. |
| [!UICONTROL Adobe Advertising Views 100% Complete] | The number of views for which 100% of an Adobe Advertising video was watched. |
| [!UICONTROL AMO ID Instances] | The number of times the [!UICONTROL AMO ID] is set. |

-->

## Classificazioni Adobe Advertising

Consulta le [classificazioni per la dimensione AMO ID](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/amo-id#classifications).
<!--

>[!NOTE]
>
>All Adobe Advertising dimensions in [!DNL Analytics] are followed by "[!DNL (AMO ID)]."

| Dimension | Applicable Adobe Advertising Data  | Description |
| ----------- | ---------- | ---------- |
| [!UICONTROL Ad Platform (AMO ID)] | [!DNL DSP] and [!DNL Search, Social, & Commerce] data | Advertising DSP or the search engine name |
| [!UICONTROL Account (AMO ID] | [!DNL DSP] and [!DNL Search, Social, & Commerce] data | The account name. |
| [!UICONTROL Network (AMO ID)] | [!DNL DSP] and [!DNL Search, Social, & Commerce] data | RTB ([!DNL DSP]) or the ad network name ([!DNL Search, Social, & Commerce]) |
| [!UICONTROL Campaign (AMO ID)] | [!DNL DSP] and [!DNL Search, Social, & Commerce] data | The campaign name. |
| [!UICONTROL Optimization (AMO ID)] | [!DNL DSP] and [!DNL Search, Social, & Commerce] data | The package ([!DNL DSP]) or portfolio ([!DNL Search, Social, & Commerce]) name. |
| [!UICONTROL Placement (AMO ID)] | [!DNL DSP] data | The placement name. |
| [!UICONTROL Ad Group (AMO ID)] | [!DNL Search, Social, & Commerce] data | The ad group name. |
| [!UICONTROL Keyword (AMO ID)] | [!DNL Search, Social, & Commerce] data | The keyword. |
| [!UICONTROL Match Type (AMO ID)] | [!DNL Search, Social, & Commerce] data | The search match type. |
| [!UICONTROL Keyword Match Type (AMO ID)] | [!DNL Search, Social, & Commerce] data | The keyword and match type. |
| [!UICONTROL Ad Type (AMO ID)] | [!DNL DSP] and [!DNL Search, Social, & Commerce] data | The ad type, such as `text`, `video`, `display`, or `native`. |
| [!UICONTROL Ad Title (AMO ID)] | [!DNL DSP] and [!DNL Search, Social, & Commerce] data |The ad type ([!DNL DSP]) or ad title ([!DNL Search, Social, & Commerce]). |
| [!UICONTROL Ad Description (AMO ID)] | [!DNL DSP] and [!DNL Search, Social, & Commerce] data | The ad description ([!DNL DSP]) or ad body ([!DNL Search, Social, & Commerce]). |
| [!UICONTROL Ad Display URL (AMO ID)] | [!DNL Search, Social, & Commerce] data | The URL displayed in the ad. |
| [!UICONTROL Ad Destination URL (AMO ID)] | [!DNL Search, Social, & Commerce] data | The destination URL for the ad. |
| [!UICONTROL Landing Type (AMO ID)] | [!DNL DSP] and [!DNL Search, Social, & Commerce] data | Whether the landing page entry was a view-through or a click-through. |
| [!UICONTROL Product Target (AMO ID)] | [!DNL Search, Social, & Commerce] data | The product target for a product listing ad. |

-->

## Utili metriche calcolate personalizzate per Adobe Advertising

Prendi in considerazione la creazione delle metriche seguenti per i dati di Adobe Advertising.

* Clic sull&#39;istanza della pagina di destinazione ([!UICONTROL AMO ID Instances] / [!UICONTROL Adobe Advertising Clicks]): questa è la percentuale di persone che hanno fatto clic sull&#39;annuncio e l&#39;hanno fatto sulla pagina di destinazione.
* Tasso misurabile ([!UICONTROL Adobe Advertising Viewable Impressions] / [!UICONTROL Adobe Advertising Impressions] * 100)
* Percentuale di impression visualizzabili ([!UICONTROL Adobe Advertising Viewable Impressions] / [!UICONTROL Adobe Advertising Measureable Impressions] * 100)
* Costo per visualizzazione ([!UICONTROL Adobe Advertising Cost] / [!UICONTROL Adobe Advertising Views])
* Costo per clic ([!UICONTROL Adobe Advertising Cost] / [!UICONTROL Adobe Advertising Clicks])

>[!MORELIKETHIS]
>
>* [Panoramica di [!DNL Analytics for Advertising]](overview.md)
>* [[!DNL Analytics] Dati in Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
