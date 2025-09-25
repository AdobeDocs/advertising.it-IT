---
title: Impostazioni creative dinamiche
description: Fai riferimento alle impostazioni per i contenuti creativi dinamici.
feature: Creative Dynamic Creatives
source-git-commit: f0bbbfb528000babbcb2c4c6915b62e81f477bda
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 0%

---

# Impostazioni creative dinamiche

<!-- add a description -->

<!-- This looks the same for me for either HTML5 type as of 9/24:

## Dynamic ad settings for static HTML5 ads {#dynamic-ad-settings-static-html5}

### Basic Details

**[!UICONTROL Advertiser]:** The advertiser for which to create the ads.

**[!UICONTROL Library]:** The creative library in which to create the ads.

**[!UICONTROL Dynamic Ad Name]:** A unique name for the creative.

**[!UICONTROL Ad Template Size]:** The ad dimensions for the ad template from which to create the ad. If you first select a specific [!UICONTROL Ad Template], then this value is automatically selected.

**[!UICONTROL Ad Template Type]:** The type of ad template from which to create the ad: *[!UICONTROL Static HTML5]* or *[!UICONTROL Dynamic HTML5]*.  If you first select a specific [!UICONTROL Ad Template], then this value is automatically selected.

**[!UICONTROL Ad Template]:** The ad template from which to create the ad.

**[!UICONTROL clickURL]:** A valid landing page URL to which users are redirected when they click the ad.

### [!UICONTROL Attributes Details]

-->

## Impostazioni annuncio dinamico<!-- for dynamic HTML5 ads {#dynamic-ad-settings-dynamic-html5}-->

<!-- add a description -->

### Dettagli di base

**[!UICONTROL Dynamic Ad Name]:** Nome univoco per la creatività.

**[!UICONTROL Advertiser]:** Inserzionista per il quale creare gli annunci.

**[!UICONTROL Library]:** Libreria creativa in cui creare gli annunci. Se crei gli annunci da [!UICONTROL Creatives] > [!UICONTROL Creative Libraries], il nome della libreria è già selezionato e di sola lettura.

**[!UICONTROL Ad Template Size]:** le [dimensioni annuncio](/help/creative/creative-libraries/creative-sizes.md) per il modello annuncio da cui creare l&#39;annuncio. Se selezioni prima un [!UICONTROL Ad Template] specifico, questo valore viene selezionato automaticamente.

## Modello annuncio

**[!UICONTROL Ad Template]:** il modello di annuncio da cui creare gli annunci. Seleziona un modello di annuncio esistente o carica un nuovo modello di annuncio e seleziona il tipo di modello (*Statico* o *Dinamico*). Un modello caricato deve essere in formato ZIP e contenere i file HTML5 e il file di definizione del modello (template.TDF). <!-- Need to add more specs for that -->

**[!UICONTROL Number of offers (Max 50)]:** Il numero di prodotti da visualizzare in un carosello.

## Cataloghi

**[!UICONTROL Template]:** modello di feed da utilizzare per creare gli annunci.

**\[Cataloghi\]**: uno o più cataloghi da cui generare annunci. Seleziona un catalogo esistente o creane uno nuovo scaricando un modello di feed esistente e creando e caricando il nuovo catalogo.

I cataloghi caricati devono essere in formato ZIP e contenere quanto segue:

* Uno o più file di feed in formato CSV, TSV o foglio di calcolo di Microsoft Excel (XLSX).<!-- Need to add more specs for that -->

* Risorse di immagini in formato GIF, JPEG, JPG o PNG

* (Facoltativo) Risorse video in formato MP4 o WEBM

### [!UICONTROL Attributes Mapping]

**[!UICONTROL Enable targeting]**: <!-- "targeting options/filters," but I don't think this means user targeting since that is set in the experience/ad on DSP -->Tipi di colonne nel file di feed per i quali devono essere presenti valori per creare annunci: *[!UICONTROL Profile data]*, *[!UICONTROL Geographic data], *[!UICONTROL Data pass], *[!UICONTROL Audience Segment]*.  **Nota:** queste impostazioni funzionano in modo indipendente dalle impostazioni avanzate nelle impostazioni dell&#39;esperienza pubblicitaria.<!-- Clarify what qualifies for each, and explain more -->

**[!UICONTROL Dynamic Ad Fields]** / **[!UICONTROL Maps to Catalog Labels]:**

Mappa ogni attributo (campo annuncio dinamico) nel modello di annuncio specificato su una colonna del catalogo specificato (etichetta catalogo) oppure immetti un valore statico.

>[!MORELIKETHIS]
>
>* [Aggiungere elementi creativi dinamici a una libreria creativa](creative-add-dynamic.md)
>* [Modifica di elementi creativi dinamici in una libreria creativa](creative-edit-dynamic.md)
>* [Flussi di lavoro per annunci dinamici](/help/creative/introduction/workflow-dynamic-ads.md)
