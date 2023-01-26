---
title: Panoramica di Campaign Management in Advertising DSP
description: Scopri la gerarchia e i componenti di gestione delle campagne.
feature: DSP Packages, DSP Placements, DSP Ads
exl-id: 8eb7b4a5-4a31-4637-858f-202392dfac98
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 0%

---

# Panoramica di Campaign Management in Advertising DSP

DSP le campagne hanno la seguente gerarchia:

* Campaign
   * Pacchetti
      * Posizionamenti
         * Annunci

<!-- Do clients think in terms of insertion orders? If yes, then work in the following info.:
In Advertising DSP, an insertion order is represented as a campaign, and line items are represented as packages. Each package will include placements, which can use different strategies and tactics to deliver the line item requirements.
-->

## [!UICONTROL Campaigns]

[Campagne](/help/dsp/campaign-management/campaigns/campaign-about.md) sono il quadro generale delle impostazioni del volo. Ogni campagna è configurata con un inserzionista, date di inizio e fine, un budget complessivo, un&#39;opzione di targeting cross-device e un limite di frequenza predefinito, e opzioni di reporting per la visualizzabilità, frode, sicurezza del marchio e verifica del pubblico. Tutte le impostazioni a livello di campagna vengono applicate automaticamente a ogni pacchetto e posizionamento all’interno della campagna.

## [!UICONTROL Packages]

Ogni campagna può contenere uno o più [pacchetti](/help/dsp/campaign-management/packages/package-about.md), ciascuno dei quali include un set di posizionamenti.

Utilizza i pacchetti per raggruppare i posizionamenti per la consegna a un budget, a un obiettivo di prestazioni e a una strategia di calcolo personalizzata impostati. DSP ottimizzare i pacchetti spostando i budget nei posizionamenti più performanti del pacchetto. È possibile organizzare i pacchetti in base al formato di posizionamento, al tipo di inventario, al provider di dati, all’utente tipo o ad altre caratteristiche distinguibili.

I pacchetti sono facoltativi ma consigliati.

## [!UICONTROL Placements]

A [placement](/help/dsp/campaign-management/placements/placement-about.md) memorizza i parametri di targeting per uno o più annunci dello stesso tipo di annuncio. Puoi creare un posizionamento per una singola campagna o pacchetto e quindi assegnargli gli annunci.

## [!UICONTROL Ads]

[Annunci](/help/dsp/campaign-management/ads/ad-about.md) includere risorse creative e URL di tracciamento. Puoi caricare i tag di terze parti per il servizio di annunci singolarmente o in blocco utilizzando i tag sheet dei partner o il modello per il tag di massa. Puoi anche creare manualmente annunci di visualizzazione nativi da distribuire DSP.

Una volta configurati i tuoi annunci, dovrai allegare ogni annuncio a un posizionamento. Puoi allegare un singolo annuncio a uno o più posizionamenti.

Tutti gli annunci attivi e approvati in un posizionamento attivo in una campagna attiva possono essere eseguiti in base ai parametri di targeting del posizionamento.

>[!MORELIKETHIS]
>
>* [Informazioni su Campaign Management](/help/dsp/campaign-management/campaigns/campaign-about.md)
>* [Informazioni sulla gestione dei pacchetti](/help/dsp/campaign-management/packages/package-about.md)
>* [Informazioni sulla gestione del posizionamento](/help/dsp/campaign-management/placements/placement-about.md)
>* [Informazioni sulla gestione degli annunci](/help/dsp/campaign-management/ads/ad-about.md)
>* [Elenco di controllo per Campaign Launch](/help/dsp/campaign-management/campaign-launch-checklist.md)
>* [Tecniche consigliate per l’impostazione di campagne sulle prestazioni](/help/dsp/optimization/campaign-best-practices-performance.md)
>* [Informazioni sui report in-Platform](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Informazioni sulle visualizzazioni dati di Campaign](/help/dsp/campaign-management/reports/campaign-data-views-about.md)
>* [Video: Struttura dell&#39;account DSP e interfaccia utente](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/ui.html)

