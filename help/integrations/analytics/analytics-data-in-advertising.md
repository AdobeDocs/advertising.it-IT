---
title: '''[!DNL Analytics] Dati in Adobe Advertising"'
description: '''[!DNL Analytics] Dati in Adobe Advertising"'
feature: Integration with Adobe Analytics
exl-id: e11b0617-44e3-4f28-a065-aa9f6cf3eb5d
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 0%

---

# [!DNL Analytics] Dati in Adobe Advertising

*Inserzionisti con una sola integrazione Advertising-Adobe Analytics di Adobe*

## Segmenti di Analytics

Tutti i segmenti creati in [!DNL Analytics] e pubblicato in Experience Cloud.

La visualizzazione dei nuovi segmenti in Adobe Advertising richiede 24-48 ore. Gli aggiornamenti ai segmenti esistenti vengono sincronizzati entro circa otto ore.

<!-- I added "metric" to some of the links below, even though it looks redundant, because of syntax limitations: If you use [!DNL] or [!UICONTROL] as the sole text of a link (such as [[!UICONTROL Revenue]], the tag is included in the link text (such as "[!UICONTROL Revenue]") when it's published. -->

## Metriche di coinvolgimento del sito

>[!NOTE]
>
>* [!DNL Analytics] trasmette gli eventi per l’eVar EF ID in Adobe Advertising.  L’integrazione predefinita non supporta l’invio di metriche calcolate o altre dimensioni (eVar) in Adobe Advertising. Tuttavia, se la metrica calcolata può essere completamente acquisita in un evento personalizzato, Adobe Advertising può acquisire l’evento personalizzato.
>* [!DNL Analytics] trasmette i dati ad Adobe Advertising ogni ora.


* [!UICONTROL Timespent_secs_1stvisit]: Il numero di secondi trascorsi sul sito durante la prima visita del visitatore.
* [!UICONTROL Timespent_secs_total]: Numero totale di secondi trascorsi sul sito in tutte le visite nell’intervallo di lookback su clic.
* [!UICONTROL Pageviews_1stvisit]: Il numero di visualizzazioni di pagina sul sito durante la prima visita del visitatore.
* [!UICONTROL Pageviews_total]: Il numero totale di visualizzazioni di pagina sul sito per tutte le visite nell’intervallo di lookback su clic.
* [[!UICONTROL Bounces] metrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/bounces.html)
* [[!UICONTROL Visits] metrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html)
* [!UICONTROL ef_id_instances]: Il numero di volte in cui [!DNL Analytics] raccolto [!UICONTROL EF ID].

## Metriche di conversione

[!DNL Analytics] trasmette le metriche di conversione ad Adobe Advertising ogni giorno.

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

Queste metriche sono specifiche per la suite di rapporti, pertanto le metriche disponibili variano per ogni cliente e suite di rapporti.

### Metriche di conversione riservate

Queste metriche sono specifiche per la suite di rapporti, pertanto le metriche disponibili variano per ogni cliente e suite di rapporti.

>[!MORELIKETHIS]
>
>* [Panoramica [!DNL Analytics for Advertising]](overview.md)
>* [Metriche pubblicitarie di Adobe in Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)

