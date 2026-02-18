---
title: Flussi di lavoro per gli annunci dinamici
description: Scopri i flussi di lavoro per la gestione degli annunci dinamici.
feature: Creative Dynamic Creatives
exl-id: eb1cdfbc-9514-4530-a50a-3ae6f6247662
source-git-commit: 4e809ac18720f22f636b2df2ad4a5b1db355e729
workflow-type: tm+mt
source-wordcount: '640'
ht-degree: 0%

---

# Flussi di lavoro per gli annunci dinamici

*Utenti autorizzati a creare annunci dinamici*

Puoi impostare gli annunci dinamici in due modi:

* Flusso di lavoro 1: carica un modello di annuncio e un catalogo delle varianti di annunci direttamente nelle impostazioni degli annunci dinamici quando aggiungi annunci dinamici a una libreria creativa. Puoi scaricare un modello di feed esistente per creare il catalogo.

  Utilizza questo flusso di lavoro quando una stessa persona può fornire tutte le informazioni (ad eccezione del modello di feed) per creare gli annunci. I file caricati rimangono disponibili per utilizzi futuri.

* Flusso di lavoro 2: configura un modello di annuncio e cataloghi di varianti di annunci in viste separate, quindi aggiungi separatamente annunci dinamici a un contenuto creativo utilizzando il modello di annuncio e i cataloghi già disponibili.

  Utilizzare questo flusso di lavoro quando persone diverse completeranno attività diverse o quando si desidera completare una sola attività alla volta.

## Flusso di lavoro 1

>[!PREREQUISITES]
>
>* Modelli di annuncio: un modello di annuncio display (un file ZIP con file HTML5) o un modello di annuncio video (un file ZIP con un file scene)
>* Cataloghi di prodotti in formato CSV, TSV o foglio di calcolo Microsoft Excel (XLSX)

1. [Crea creatività dinamica](/help/creative/creative-libraries/creative-add-dynamic.md) per una libreria creativa. Per gli annunci HTML5 e video dinamici, carica o seleziona un modello di annuncio e un catalogo esistenti.

1. Utilizza le creatività dinamiche per le esperienze pubblicitarie:

   1. [Crea bundle di annunci dinamici](/help/creative/creative-libraries/bundle-manage.md) che puoi allegare tutti in una sola volta a un&#39;esperienza pubblicitaria.

   1. Crea esperienze annuncio dinamiche [con targeting](/help/creative/experiences/experience-create-targeting.md) o [senza targeting](/help/creative/experiences/experience-create-no-targeting.md) e [assegna i bundle creativi alle esperienze](/help/creative/experiences/experience-assign-creative-bundles.md).

   1. [Genera e implementa tag esperienza annuncio](/help/creative/experiences/experience-tag-export.md) per eseguirli come annunci nel tuo DSP.

      Per utilizzare un’esperienza di annuncio come annuncio in Adobe Advertising DSP, carica il tag esperienza di annuncio in una campagna Advertising DSP. Per utilizzare un’esperienza annuncio come annuncio in un DSP diverso, implementa il tag di esperienza annuncio in tale DSP.

## Flusso di lavoro 2

1. [Crea un modello di annuncio](/help/creative/ad-templates/ad-template-manage.md) per gli annunci dinamici in base alle risorse disponibili. Il modello dell&#39;annuncio deve essere in formato ZIP e contenere:<!-- Need to add more specs for templates -->

* Creatività: file HTML5 con il formato di annuncio desiderato e (solo annunci HTML5 dinamici) un file con gli attributi di annuncio (.tdf)

* Creative video: un file .scene con il formato di annuncio desiderato e un file con gli attributi di annuncio (.tdf)

1. Configura gli elementi annuncio:

   * (Per singoli annunci statici di HTML5) Raccogli e [carica le risorse immagine](/help/creative/feeds/asset-manage.md) per i tuoi annunci.

   * (Per annunci HTML5 e video dinamici) Crea cataloghi degli elementi dell’annuncio:

      1. Crea un file di feed in formato foglio di calcolo Microsoft Excel (XLSX), con una riga per ogni variante di annuncio. Includi un nome immagine o video in ogni riga. Raccogli separatamente le risorse immagine e video associate.

      1. [Carica il file di feed e le risorse](/help/creative/feeds/asset-manage.md).

      1. [Crea un modello di feed](/help/creative/feeds/feed-template-manage.md) per mappare i campi nel file di feed (foglio di calcolo) ai campi nel backend di Advertising Creative. Facoltativamente, puoi scaricare e popolare i modelli di feed principali con campi relativi a retail<!-- and what is the creative template?-->.

      1. [Creare un catalogo](/help/creative/feeds/catalog-manage.md#feed-catalog-create) da un file di feed specificato e da un modello di feed specificato, quindi [elaborare il catalogo](/help/creative/feeds/catalog-manage.md#feed-catalog-process) per visualizzare le varianti di annuncio che è possibile creare da esso.

         È possibile utilizzare ogni file di feed per un solo catalogo.

         È possibile [tenere traccia dello stato dei processi di elaborazione del catalogo](/help/creative/feeds/job-status-track.md) nella scheda [!UICONTROL Creative] > [!UICONTROL Feeds] > [!UICONTROL Job Status].

1. [Crea creatività dinamica](/help/creative/creative-libraries/creative-add-dynamic.md) per una libreria creativa. Per gli annunci HTML5 dinamici, utilizza un modello di annuncio specificato e cataloghi specificati.

1. Utilizza le creatività dinamiche per le esperienze pubblicitarie:

   1. [Crea bundle di annunci dinamici](/help/creative/creative-libraries/bundle-manage.md) che puoi allegare tutti in una sola volta a un&#39;esperienza pubblicitaria.

   1. Crea esperienze annuncio dinamiche [con targeting](/help/creative/experiences/experience-create-targeting.md) o [senza targeting](/help/creative/experiences/experience-create-no-targeting.md) e [assegna i bundle creativi alle esperienze](/help/creative/experiences/experience-assign-creative-bundles.md).

   1. [Genera e implementa tag esperienza annuncio](/help/creative/experiences/experience-tag-export.md) per eseguirli come annunci nel tuo DSP.

      Per utilizzare un’esperienza di annuncio come annuncio in Adobe Advertising DSP, carica il tag esperienza di annuncio in una campagna Advertising DSP. Per utilizzare un’esperienza annuncio come annuncio in un DSP diverso, implementa il tag di esperienza annuncio in tale DSP.
