---
title: Metriche pubblicitarie di Adobe in Analysis Workspace
description: Metriche pubblicitarie di Adobe in Analysis Workspace
feature: Integration with Adobe Analytics
exl-id: d740bd19-c643-4917-9cfd-f9cf0affd07e
source-git-commit: 3fd9323e6b6a525392aff67cc116bd649f2936b1
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 0%

---

# Metriche pubblicitarie di Adobe in Analysis Workspace

*Inserzionisti con una sola integrazione Advertising-Adobe Analytics di Adobe*

>[!NOTE]
>
>* Adobe Advertising trasmette le metriche e le dimensioni del traffico a [!DNL Analytics] ogni giorno.
>* [!DNL Analytics] acquisisce i click-through e le visualizzazioni di Adobe Advertising in tempo reale.


## Metriche del traffico da Adobe Advertising

>[!NOTE]
>
>Tutte le metriche del traffico pubblicitario di Adobe in [!DNL Analytics] inizia con &quot;AMO&quot;.

| Metrica del traffico | Descrizione |
| -------------- | ----------- |
| [!UICONTROL AMO Impressions] | Numero di impression pubblicitarie Adobi. |
| [!UICONTROL AMO Clicks] | Il numero totale di clic su Advertising in Adobe. |
| [!UICONTROL AMO Cost] | La spesa pubblicitaria Adobe nella valuta della suite di rapporti. |
| [!UICONTROL AMO ID Instance] | Il numero di volte in cui l’ID pubblicitario Adobe è impostato. |
| [!UICONTROL AMO Minutes Viewed] | Il numero di minuti in cui è stato visualizzato un video pubblicitario Adobe. |
| [!UICONTROL AMO Views] | Il numero di visualizzazioni di un annuncio. Una visualizzazione viene conteggiata quando il visualizzatore avvia il video Adobe Advertising. |
| [!UICONTROL AMO Views 25% Complete] | Il numero di visualizzazioni per le quali è stato guardato almeno il 25% di un video pubblicitario Adobe. |
| [!UICONTROL AMO Views 50% Complete] | Il numero di visualizzazioni per le quali è stato guardato almeno il 50% di un video pubblicitario Adobe. |
| [!UICONTROL AMO Views 75% Complete] | Il numero di visualizzazioni per le quali è stato guardato almeno il 75% di un video pubblicitario Adobe. |
| [!UICONTROL AMO Views 100% Complete] | Il numero di visualizzazioni per le quali è stato guardato il 100% di un video pubblicitario Adobe. |
| [!UICONTROL AMO Viewable Impressions] | Il numero di impression misurate per essere visualizzabili in base alla configurazione di posizionamento. |
| [!UICONTROL AMO Not Viewable Impressions] | Il numero di impression determinate non visualizzabili. Questo valore viene calcolato come ([!UICONTROL AMO Measurable Impressions] - [!UICONTROL AMO Viewable]). |
| [!UICONTROL AMO Measurable Impressions] | Numero di impression per le quali è stata inizializzata correttamente la strumentazione di visualizzabilità. Questo valore è calcolato come (impression strumentate - il numero di impression non misurabili). |

## Metriche calcolate personalizzate utili per Adobe la pubblicità

Prendi in considerazione la creazione delle seguenti metriche per i tuoi dati pubblicitari di Adobe.

* Clic sull’istanza della pagina di destinazione ([!UICONTROL AMO ID Instances] / [!UICONTROL AMO Clicks]): È la percentuale di persone che hanno fatto clic sull’annuncio e lo hanno fatto sulla pagina di destinazione.
* Tasso misurabile ([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Impressions] * 100)
* Tasso di impression visualizzabile ([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Measureable Impressions] * 100)
* Costo per visualizzazione ([!UICONTROL AMO Cost] / [!UICONTROL AMO Views])
* Costo per clic ([!UICONTROL AMO Cost] / [!UICONTROL AMO Clicks])

## Dimension di pubblicità Adobe

>[!NOTE]
>
>Tutte le dimensioni pubblicitarie Adobe in [!DNL Analytics] sono seguite da &quot;(AMO ID)&quot;.

| Dimension | Dati pubblicitari Adobe applicabili | Descrizione |
| ----------- | ---------- | ---------- |
| [!UICONTROL Ad Platform (AMO ID)] | [!DNL DSP] e [!DNL Search] dati | DSP pubblicitaria o nome del motore di ricerca |
| [!UICONTROL Account (AMO ID] | [!DNL DSP] e [!DNL Search] dati | Nome account. |
| [!UICONTROL Network (AMO ID)] | [!DNL DSP] e [!DNL Search] dati | RTB ([!DNL DSP]) o il nome della rete pubblicitaria ([!DNL Search]) |
| [!UICONTROL Campaign (AMO ID)] | [!DNL DSP] e [!DNL Search] dati | Nome della campagna. |
| [!UICONTROL Optimization (AMO ID)] | [!DNL DSP] e [!DNL Search] dati | Il pacchetto ([!DNL DSP]) o portafoglio ([!DNL Search]). |
| [!UICONTROL Placement (AMO ID)] | [!DNL DSP] dati | Nome del posizionamento. |
| [!UICONTROL Ad Group (AMO ID)] | [!DNL Search] dati | Nome del gruppo di annunci. |
| [!UICONTROL Keyword (AMO ID)] | [!DNL Search] dati | Parola chiave. |
| [!UICONTROL Match Type (AMO ID)] | [!DNL Search] dati | Tipo di corrispondenza della ricerca. |
| [!UICONTROL Keyword Match Type (AMO ID)] | [!DNL Search] dati | Parola chiave e tipo di corrispondenza. |
| [!UICONTROL Ad Type (AMO ID)] | [!DNL DSP] e [!DNL Search] dati | Il tipo di annuncio, ad esempio `text`, `video`, `display`oppure `native`. |
| [!UICONTROL Ad Title (AMO ID)] | [!DNL DSP] e [!DNL Search] dati | Il tipo di annuncio ([!DNL DSP]) o titolo dell&#39;annuncio ([!DNL Search]). |
| [!UICONTROL Ad Description (AMO ID)] | [!DNL DSP] e [!DNL Search] dati | La descrizione dell&#39;annuncio ([!DNL DSP]) o corpo dell&#39;annuncio ([!DNL Search]). |
| [!UICONTROL Ad Display URL (AMO ID)] | [!DNL Search] dati | L’URL visualizzato nell’annuncio. |
| [!UICONTROL Ad Destination URL (AMO ID)] | [!DNL Search] dati | L&#39;URL di destinazione dell&#39;annuncio. |
| [!UICONTROL Landing Type (AMO ID)] | [!DNL DSP] e [!DNL Search] dati | Se la voce della pagina di destinazione è una visualizzazione passante o un click-through. |
| [!UICONTROL Product Target (AMO ID)] | [!DNL Search] dati | Destinazione del prodotto per un annuncio di elenco prodotti. |

>[!MORELIKETHIS]
>
>* [Panoramica [!DNL Analytics for Advertising]](overview.md)
>* [[!DNL Analytics] Dati in Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)

