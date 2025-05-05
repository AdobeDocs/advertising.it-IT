---
title: '[!DNL Analytics] dati in Adobe Advertising'
description: '[!DNL Analytics] dati in Adobe Advertising'
feature: Integration with Adobe Analytics
exl-id: e11b0617-44e3-4f28-a065-aa9f6cf3eb5d
source-git-commit: 73cdb171523b55f48b5ae5c5b2b4843f542336a6
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---

# [!DNL Analytics] dati in Adobe Advertising

*Inserzionisti con una sola integrazione Adobe Advertising-Adobe Analytics*

## Segmenti di Analytics

Tutti i segmenti creati in [!DNL Analytics] e pubblicati in Experience Cloud.

I nuovi segmenti richiedono 24-48 ore per essere visualizzati nell’Adobe Advertising. Gli aggiornamenti ai segmenti esistenti vengono sincronizzati entro circa otto ore.

<!-- I added "metric" to some of the links below, even though it looks redundant, because of syntax limitations: If you use [!DNL] or [!UICONTROL] as the sole text of a link (such as [[!UICONTROL Revenue]], the tag is included in the link text (such as "[!UICONTROL Revenue]") when it's published. -->

## Metriche di coinvolgimento sito

>[!NOTE]
>
>* [!DNL Analytics] trasmette gli eventi per l&#39;ID EF [!DNL eVar] in Adobe Advertising.  L&#39;integrazione predefinita non supporta l&#39;invio di metriche calcolate o altre dimensioni ([!DNL eVars]) in Adobe Advertising. Tuttavia, se la metrica calcolata può essere acquisita completamente in un evento personalizzato, Adobe Advertising può acquisire l’evento personalizzato.
>* [!DNL Analytics] trasmette i dati ad Adobe Advertising ogni ora.

* [!UICONTROL Timespent_secs_1stvisit]: numero di secondi trascorsi sul sito durante la prima visita del visitatore.
* [!UICONTROL Timespent_secs_total]: numero totale di secondi trascorsi sul sito in tutte le visite all&#39;interno dell&#39;intervallo di lookback dei clic.
* [!UICONTROL Pageviews_1stvisit]: numero di visualizzazioni di pagina sul sito durante la prima visita del visitatore.
* [!UICONTROL Pageviews_total]: numero totale di visualizzazioni di pagina sul sito per tutte le visite all&#39;interno dell&#39;intervallo di lookback dei clic.
* Metrica [[!UICONTROL Bounces]](https://experienceleague.adobe.com/docs/analytics/components/metrics/bounces.html?lang=it)
* Metrica [[!UICONTROL Visits]](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html?lang=it)
* [!UICONTROL ef_id_instances]: numero di volte che [!DNL Analytics] ha raccolto un [!UICONTROL EF ID].

## Metriche di conversione

[!DNL Analytics] passa ogni giorno le metriche di conversione agli Adobi Advertising.

### Metriche di conversione standard

* Metrica [[!UICONTROL Revenue]](https://experienceleague.adobe.com/docs/analytics/components/metrics/revenue.html?lang=it)
* Metrica [[!UICONTROL Orders]](https://experienceleague.adobe.com/docs/analytics/components/metrics/orders.html?lang=it)
* Metrica [[!UICONTROL Units]](https://experienceleague.adobe.com/docs/analytics/components/metrics/units.html?lang=it)
* Metrica [[!UICONTROL Carts]](https://experienceleague.adobe.com/docs/analytics/components/metrics/carts.html?lang=it)
* Metrica [[!UICONTROL Cart Views]](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-views.html?lang=it)
* Metrica [[!UICONTROL Checkouts]](https://experienceleague.adobe.com/docs/analytics/components/metrics/checkouts.html?lang=it)
* Metrica [[!UICONTROL Cart Additions]](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-additions.html?lang=it)
* Metrica [[!UICONTROL Cart Removals]](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-removals.html?lang=it)

### Metriche di conversione personalizzate

Queste metriche sono specifiche per la suite di rapporti, pertanto le metriche disponibili variano per ciascun cliente e suite di rapporti.

### Metriche di conversione personalizzate create da [!DNL eVars] e [!DNL Props]

Le metriche disponibili variano a seconda del cliente. Consulta &quot;[Creare metriche di conversione da Adobe Analytics [!DNL eVars] e [!DNL Props]](/help/integrations/analytics/conversion-metrics-from-evars.md).&quot;

### Metriche di conversione riservate

Queste metriche sono specifiche per la suite di rapporti, pertanto le metriche disponibili variano per ciascun cliente e suite di rapporti.

>[!MORELIKETHIS]
>
>* [Panoramica di [!DNL Analytics for Advertising]](overview.md)
>* [Metriche di Adobe Advertising in Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
