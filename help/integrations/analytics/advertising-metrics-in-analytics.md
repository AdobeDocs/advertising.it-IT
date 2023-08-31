---
title: Metriche di Adobe Advertising in Analysis Workspace
description: Metriche di Adobe Advertising in Analysis Workspace
feature: Integration with Adobe Analytics
exl-id: da5e5704-4504-4fc5-93d2-db7d28f0c349
source-git-commit: da69280679a4e0c5ce04f55ee94ce984745395ff
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 0%

---

# Metriche di Adobe Advertising in Analysis Workspace

*Per gli inserzionisti con una sola integrazione Adobi Advertising-Adobe Analytics*

>[!NOTE]
>
>* Adobe Advertising trasmette le metriche e le dimensioni del traffico a [!DNL Analytics] ogni giorno.
>* [!DNL Analytics] acquisisce in tempo reale i click-through e i view-through di Adobe Advertising.
>* Per [!DNL Search, Social, & Commerce], questa funzione è supportata per la maggior parte delle reti di annunci e dei tipi di campagne. Consulta &quot;[Inventario supportato](/help/search-social-commerce/introduction/supported-inventory.md)&quot; in [!DNL Search, Social, & Commerce] per ulteriori informazioni.

## Metriche traffico da Adobi Advertising

Adobe Advertising delle metriche del traffico in [!DNL Analytics] in genere inizia con &quot;Adobe Advertising&quot;, ad eccezione di &quot;[!UICONTROL AMO ID Instances].&quot; Tuttavia, per i clienti a lungo termine che hanno utilizzato un evento personalizzato (anziché un evento riservato) per creare originariamente metriche per clic, costi e impression, tali metriche iniziano ancora con &quot;AMO&quot;.

| Metrica traffico | Descrizione |
| -------------- | ----------- |
| [!UICONTROL Adobe Advertising Clicks] o (alcuni clienti legacy) [!UICONTROL AMO Clicks] | Il numero totale di clic Adobe Advertising. |
| [!UICONTROL Adobe Advertising Cost] o (alcuni clienti legacy) [!UICONTROL AMO Cost] | L’Adobe Advertising di spesa nella valuta della suite di rapporti. |
| [!UICONTROL Adobe Advertising Impressions] o (alcuni clienti legacy) [!UICONTROL AMO Impressions] | Il numero di impression Adobi Advertising. |
| [!UICONTROL Adobe Advertising Measurable Impressions] | Numero di impression servite per le quali la strumentazione di visualizzabilità è stata inizializzata correttamente. Questo valore viene calcolato come (impression instrumentate: il numero di impression non misurabili). |
| [!UICONTROL Adobe Advertising Minutes Viewed] | Il numero di minuti in cui è stato visualizzato un video di Adobe Advertising. |
| [!UICONTROL Adobe Advertising Not Viewable Impressions] | Il numero di impression che sono state determinate come non visualizzabili. Questo valore viene calcolato come ([!UICONTROL Adobe Advertising Measurable Impressions] - [!UICONTROL Adobe Advertising Viewable]). |
| [!UICONTROL Adobe Advertising Viewable Impressions] | Il numero di impression misurate per essere visualizzabili in base alla configurazione di posizionamento. |
| [!UICONTROL Adobe Advertising Views] | Il numero di visualizzazioni in un annuncio. Una vista viene conteggiata quando il visualizzatore avvia il video di Adobe Advertising. |
| [!UICONTROL Adobe Advertising Views 25% Complete] | Il numero di visualizzazioni per le quali è stato guardato almeno il 25% di un video di Adobe Advertising. |
| [!UICONTROL Adobe Advertising Views 50% Complete] | Il numero di visualizzazioni per le quali è stato guardato almeno il 50% di un video di Adobe Advertising. |
| [!UICONTROL Adobe Advertising Views 75% Complete] | Il numero di visualizzazioni per le quali è stato guardato almeno il 75% di un video di Adobe Advertising. |
| [!UICONTROL Adobe Advertising Views 100% Complete] | Il numero di visualizzazioni per le quali è stato guardato il 100% di un video di Adobe Advertising. |
| [!UICONTROL AMO ID Instances] | Il numero di volte in cui [!UICONTROL AMO ID] è impostato. |

## Dimension Adobe Advertising

>[!NOTE]
>
>Tutte le dimensioni di Adobe Advertising in [!DNL Analytics] sono seguiti da &quot;[!DNL (AMO ID)].&quot;

| Dimensione | Dati Adobe Advertising applicabili | Descrizione |
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

* Clic sull’istanza della pagina di destinazione ([!UICONTROL AMO ID Instances] / [!UICONTROL Adobe Advertising Clicks]): corrisponde alla percentuale di persone che hanno fatto clic sull’annuncio e l’hanno fatto sulla pagina di destinazione.
* Tasso misurabile ([!UICONTROL Adobe Advertising Viewable Impressions] / [!UICONTROL Adobe Advertising Impressions] * 100)
* Tasso di impression visualizzabile ([!UICONTROL Adobe Advertising Viewable Impressions] / [!UICONTROL Adobe Advertising Measureable Impressions] * 100)
* Costo per visualizzazione ([!UICONTROL Adobe Advertising Cost] / [!UICONTROL Adobe Advertising Views])
* Costo per clic ([!UICONTROL Adobe Advertising Cost] / [!UICONTROL Adobe Advertising Clicks])

>[!MORELIKETHIS]
>
>* [Panoramica di [!DNL Analytics for Advertising]](overview.md)
>* [[!DNL Analytics] Dati in Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
