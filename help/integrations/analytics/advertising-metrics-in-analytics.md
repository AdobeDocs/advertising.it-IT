---
title: Metriche pubblicitarie per Adobi in Analysis Workspace
description: Metriche pubblicitarie per Adobi in Analysis Workspace
feature: Integration with Adobe Analytics
exl-id: da5e5704-4504-4fc5-93d2-db7d28f0c349
source-git-commit: 5dd3772de945660e76321dac935de5ebcab5979a
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 0%

---

# Metriche pubblicitarie per Adobi in Analysis Workspace

*Inserzionisti con un Adobe di integrazione Advertising-Adobe Analytics Only*

>[!NOTE]
>
>* Adobe Advertising trasmette le metriche e le dimensioni del traffico a [!DNL Analytics] ogni giorno.
>* [!DNL Analytics] acquisisce click-through e view-through di Adobe Advertising in tempo reale.
   > Per [!DNL Search, Social, & Commerce], questa funzione è supportata per la maggior parte delle reti di annunci e dei tipi di campagne. Consulta &quot;Inventario supportato&quot; in [!DNL Search, Social, & Commerce] per ulteriori informazioni.<!-- add link when that's published in ExL -->


## Metriche di traffico da Adobe Advertising

>[!NOTE]
>
>Tutti gli Adobi di metriche del traffico per Advertising in [!DNL Analytics] inizia con &quot;AMO&quot;.

| Metrica traffico | Descrizione |
| -------------- | ----------- |
| [!UICONTROL AMO Impressions] | Il numero di impression pubblicitarie Adobi. |
| [!UICONTROL AMO Clicks] | Il numero totale di clic pubblicitari di Adobe. |
| [!UICONTROL AMO Cost] | L’Adobe della spesa pubblicitaria nella valuta della suite di rapporti. |
| [!UICONTROL AMO ID Instance] | Il numero di volte in cui è impostato l’ID Adobe Advertising. |
| [!UICONTROL AMO Minutes Viewed] | Il numero di minuti in cui è stato visualizzato un video di Adobe Advertising. |
| [!UICONTROL AMO Views] | Il numero di visualizzazioni in un annuncio. Una visualizzazione viene conteggiata quando il visualizzatore avvia il video Adobe Advertising. |
| [!UICONTROL AMO Views 25% Complete] | Il numero di visualizzazioni per le quali è stato guardato almeno il 25% di un video di Adobe Advertising. |
| [!UICONTROL AMO Views 50% Complete] | Il numero di visualizzazioni per le quali è stato guardato almeno il 50% di un video di Adobe Advertising. |
| [!UICONTROL AMO Views 75% Complete] | Il numero di visualizzazioni per le quali è stato guardato almeno il 75% di un video di Adobe Advertising. |
| [!UICONTROL AMO Views 100% Complete] | Il numero di visualizzazioni per le quali è stato guardato il 100% di un video di Adobe Advertising. |
| [!UICONTROL AMO Viewable Impressions] | Il numero di impression misurate per essere visualizzabili in base alla configurazione di posizionamento. |
| [!UICONTROL AMO Not Viewable Impressions] | Il numero di impression che sono state determinate come non visualizzabili. Questo valore viene calcolato come ([!UICONTROL AMO Measurable Impressions] - [!UICONTROL AMO Viewable]). |
| [!UICONTROL AMO Measurable Impressions] | Numero di impression servite per le quali la strumentazione di visualizzabilità è stata inizializzata correttamente. Questo valore viene calcolato come (impression instrumentate: il numero di impression non misurabili). |

## Dimension pubblicitari Adobe

>[!NOTE]
>
>Tutte le dimensioni di Adobe Advertising in [!DNL Analytics] sono seguiti da &quot;(AMO ID)&quot;.

| Dimension | Dati pubblicitari di Adobe applicabili | Descrizione |
| ----------- | ---------- | ---------- |
| [!UICONTROL Ad Platform (AMO ID)] | [!DNL DSP] e [!DNL Search, Social, & Commerce] dati | Advertising DSP o il nome del motore di ricerca |
| [!UICONTROL Account (AMO ID] | [!DNL DSP] e [!DNL Search, Social, & Commerce] dati | Il nome dell’account. |
| [!UICONTROL Network (AMO ID)] | [!DNL DSP] e [!DNL Search, Social, & Commerce] dati | RTB ([!DNL DSP]) o il nome della rete di annunci ([!DNL Search, Social, & Commerce]) |
| [!UICONTROL Campaign (AMO ID)] | [!DNL DSP] e [!DNL Search, Social, & Commerce] dati | Il nome della campagna. |
| [!UICONTROL Optimization (AMO ID)] | [!DNL DSP] e [!DNL Search, Social, & Commerce] dati | Il pacchetto ([!DNL DSP]) o portfolio ([!DNL Search, Social, & Commerce]). |
| [!UICONTROL Placement (AMO ID)] | [!DNL DSP] dati | Il nome del posizionamento. |
| [!UICONTROL Ad Group (AMO ID)] | [!DNL Search, Social, & Commerce] dati | Il nome del gruppo di annunci. |
| [!UICONTROL Keyword (AMO ID)] | [!DNL Search, Social, & Commerce] dati | La parola chiave. |
| [!UICONTROL Match Type (AMO ID)] | [!DNL Search, Social, & Commerce] dati | Tipo di corrispondenza della ricerca. |
| [!UICONTROL Keyword Match Type (AMO ID)] | [!DNL Search, Social, & Commerce] dati | Parola chiave e tipo di corrispondenza. |
| [!UICONTROL Ad Type (AMO ID)] | [!DNL DSP] e [!DNL Search, Social, & Commerce] dati | Il tipo di annuncio, ad esempio `text`, `video`, `display`, o `native`. |
| [!UICONTROL Ad Title (AMO ID)] | [!DNL DSP] e [!DNL Search, Social, & Commerce] dati | Tipo di annuncio ([!DNL DSP]) o titolo annuncio ([!DNL Search, Social, & Commerce]). |
| [!UICONTROL Ad Description (AMO ID)] | [!DNL DSP] e [!DNL Search, Social, & Commerce] dati | Descrizione dell’annuncio ([!DNL DSP]) o corpo dell’annuncio ([!DNL Search, Social, & Commerce]). |
| [!UICONTROL Ad Display URL (AMO ID)] | [!DNL Search, Social, & Commerce] dati | L’URL visualizzato nell’annuncio. |
| [!UICONTROL Ad Destination URL (AMO ID)] | [!DNL Search, Social, & Commerce] dati | L’URL di destinazione dell’annuncio. |
| [!UICONTROL Landing Type (AMO ID)] | [!DNL DSP] e [!DNL Search, Social, & Commerce] dati | Se la voce della pagina di destinazione era un view-through o un click-through. |
| [!UICONTROL Product Target (AMO ID)] | [!DNL Search, Social, & Commerce] dati | Il target di prodotto per un annuncio di elenco prodotti. |

## Utili metriche calcolate personalizzate per Adobe Advertising

Prendi in considerazione la creazione delle metriche seguenti per i dati di Adobe Advertising.

* Clic sull’istanza della pagina di destinazione ([!UICONTROL AMO ID Instances] / [!UICONTROL AMO Clicks]): corrisponde alla percentuale di persone che hanno fatto clic sull’annuncio e l’hanno fatto sulla pagina di destinazione.
* Tasso misurabile ([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Impressions] * 100)
* Tasso di impression visualizzabile ([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Measureable Impressions] * 100)
* Costo per visualizzazione ([!UICONTROL AMO Cost] / [!UICONTROL AMO Views])
* Costo per clic ([!UICONTROL AMO Cost] / [!UICONTROL AMO Clicks])

>[!MORELIKETHIS]
>
>* [Panoramica di [!DNL Analytics for Advertising]](overview.md)
>* [[!DNL Analytics] Dati in Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)

