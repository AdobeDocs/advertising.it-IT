---
title: Impostazioni creative dinamiche
description: Fai riferimento alle impostazioni per i contenuti creativi dinamici.
feature: Creative Dynamic Creatives
exl-id: 9dcd7245-fa02-4082-9abb-8c0792322a68
source-git-commit: 164ee92f85c0e649dc2bd6c0224a531eb72d1962
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---

# Impostazioni creative dinamiche

<!-- add a description -->

## Impostazioni annuncio dinamico<!-- for dynamic HTML5 ads {#dynamic-ad-settings-dynamic-html5}-->

<!-- add a description -->

### Dettagli di base

**[!UICONTROL Creative Type]:** se la creatività è un annuncio *[!UICONTROL Display]* (HTML5) o un annuncio *[!UICONTROL Video]*.

**[!UICONTROL Dynamic Display Ad Name]** o **[!UICONTROL Dynamic Video Ad Name]:** Nome univoco per il contenuto creativo.

**[!UICONTROL Advertiser]:** Inserzionista per il quale creare gli annunci. Se crei gli annunci da [!UICONTROL Creatives] > [!UICONTROL Creative Libraries], l&#39;inserzionista è già selezionato e di sola lettura.

**[!UICONTROL Library]:** Libreria creativa in cui creare gli annunci. Se crei gli annunci da [!UICONTROL Creatives] > [!UICONTROL Creative Libraries], il nome della libreria è già selezionato e di sola lettura.

## Modello annuncio

**[!UICONTROL Ad Template]:** il modello di annuncio da cui creare gli annunci. Seleziona un modello di annuncio esistente o carica un nuovo modello di annuncio e seleziona il tipo di modello (*Statico* o *Dinamico*). Il modello deve essere in formato ZIP e contenere:<!-- Need to add more specs for templates -->

* Creatività: file HTML5 con il formato di annuncio desiderato e (solo annunci HTML5 dinamici) un file con gli attributi di annuncio (.tdf)

* Creative video: un file .scene con il formato di annuncio desiderato. Il file ZIP può essere un massimo di 512 MB.

Per continuare, scegliere **[!UICONTROL Select Ad Template]**.

**[!UICONTROL Size]:** (solo annunci di visualizzazione dinamici; sola lettura) [dimensioni annuncio](/help/creative/creative-libraries/creative-sizes.md) per il modello di annuncio selezionato, utilizzato per creare gli annunci.

**[!UICONTROL Card Count (Max 50)]:** (solo annunci visualizzati) Il numero di prodotti da visualizzare in un carosello.

**[!UICONTROL Duration]:** (solo annunci video; sola lettura) La durata del video derivata dal modello di annuncio selezionato. La durata di ogni video deve essere compresa tra 1 e 90 secondi.

## Cataloghi

**\[Cataloghi\]**: uno o più cataloghi da cui generare annunci. Seleziona un catalogo esistente o creane uno nuovo scaricando un modello di feed esistente e creando e caricando il nuovo catalogo. Fare clic su **[!UICONTROL Select Catalog]**.

I cataloghi caricati devono essere in formato ZIP e contenere quanto segue:

* (Visualizzazione dinamica e annunci video) Uno o più file di feed in formato CSV, TSV o foglio di calcolo di Microsoft Excel (XLSX). La dimensione massima del file è 512 MB.<!-- Need to add more specs for the feed files -->

* (Visualizza annunci) Risorse immagine in formato GIF, JPEG, JPG o PNG

* (Annunci video) Risorse video in formato MP4, MOV o WEBM. I modelli di annuncio supportati includono scheda iniziale, scheda finale, sovrapposizione superiore, sovrapposizione inferiore o a L. La durata di ogni video deve essere compresa tra 1 e 90 secondi.

### [!UICONTROL Attributes Mapping]

**[!UICONTROL Enable targeting]**: <!-- "targeting options/filters," but I don't think this means user targeting since that is set in the experience/ad on DSP -->Tipi di colonne nel file di feed per i quali devono essere presenti valori per creare annunci: *[!UICONTROL Profile data]*, *[!UICONTROL Geographic data], *[!UICONTROL Data pass], *[!UICONTROL Audience Segment]*.  **Nota:** queste impostazioni funzionano in modo indipendente dalle impostazioni avanzate nelle impostazioni dell&#39;esperienza pubblicitaria.<!-- Clarify what qualifies for each, and explain more -->

**[!UICONTROL Dynamic Ad Fields]** / **[!UICONTROL Maps to Catalog Labels]:**

Mappa ogni attributo (campo annuncio dinamico) nel modello di annuncio specificato su una colonna del catalogo specificato (etichetta catalogo) oppure immetti un valore statico.

>[!MORELIKETHIS]
>
>* [Aggiungere elementi creativi dinamici a una libreria creativa](creative-add-dynamic.md)
>* [Modifica di elementi creativi dinamici in una libreria creativa](creative-edit-dynamic.md)
>* [Flussi di lavoro per annunci dinamici](/help/creative/introduction/workflow-dynamic-ads.md)
