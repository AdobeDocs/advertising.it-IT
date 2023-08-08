---
title: '[!DNL Analytics] Dati in Adobi Advertising'
description: '[!DNL Analytics] Dati in Adobi Advertising'
feature: Integration with Adobe Analytics
exl-id: e11b0617-44e3-4f28-a065-aa9f6cf3eb5d
source-git-commit: 73cdb171523b55f48b5ae5c5b2b4843f542336a6
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# [!DNL Analytics] Dati in Adobe Advertising

*Per gli inserzionisti con una sola integrazione Adobi Advertising-Adobe Analytics*

## Segmenti di Analytics

Tutti i segmenti creati in [!DNL Analytics] e pubblicato su Experience Cloud.

I nuovi segmenti richiedono 24-48 ore per essere visualizzati nell’Adobe Advertising. Gli aggiornamenti ai segmenti esistenti vengono sincronizzati entro circa otto ore.

<!-- I added "metric" to some of the links below, even though it looks redundant, because of syntax limitations: If you use [!DNL] or [!UICONTROL] as the sole text of a link (such as [[!UICONTROL Revenue]], the tag is included in the link text (such as "[!UICONTROL Revenue]") when it's published. -->

## Metriche di coinvolgimento sito

>[!NOTE]
>
>* [!DNL Analytics] trasmette gli eventi per l’ID EF [!DNL eVar] in Adobi Advertising.  L’integrazione predefinita non supporta l’invio di metriche calcolate o altre dimensioni ([!DNL eVars]) in Adobe Advertising. Tuttavia, se la metrica calcolata può essere acquisita completamente in un evento personalizzato, Adobi Advertising può acquisire l’evento personalizzato.
>* [!DNL Analytics] trasmette i dati ad Adobi Advertising ogni ora.

* [!UICONTROL Timespent_secs_1stvisit]: il numero di secondi trascorsi sul sito durante la prima visita del visitatore.
* [!UICONTROL Timespent_secs_total]: numero totale di secondi trascorsi sul sito in tutte le visite all’interno dell’intervallo di lookback dei clic.
* [!UICONTROL Pageviews_1stvisit]: numero di visualizzazioni di pagina sul sito durante la prima visita del visitatore.
* [!UICONTROL Pageviews_total]: numero totale di visualizzazioni di pagina sul sito in tutte le visite all’interno dell’intervallo di lookback dei clic.
* [[!UICONTROL Bounces] metrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/bounces.html)
* [[!UICONTROL Visits] metrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html)
* [!UICONTROL ef_id_instances]: il numero di volte che [!DNL Analytics] ha raccolto un [!UICONTROL EF ID].

## Metriche di conversione

[!DNL Analytics] trasmette le metriche di conversione ad Adobi Advertising ogni giorno.

### Metriche di conversione standard

* [[!UICONTROL Revenue] metrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/revenue.html)
* [[!UICONTROL Orders] metrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/orders.html)
* [[!UICONTROL Units] metrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/units.html)
* [[!UICONTROL Carts] metrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/carts.html)
* [[!UICONTROL Cart Views] metrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-views.html)
* [[!UICONTROL Checkouts] metrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/checkouts.html)
* [[!UICONTROL Cart Additions] metrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-additions.html)
* [[!UICONTROL Cart Removals] metrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-removals.html)

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
