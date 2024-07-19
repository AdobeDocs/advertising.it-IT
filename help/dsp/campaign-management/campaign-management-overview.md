---
title: Panoramica di Campaign Management in Advertising DSP
description: Scopri la gerarchia di gestione delle campagne e i relativi componenti.
feature: DSP Packages, DSP Placements, DSP Ads
exl-id: 8eb7b4a5-4a31-4637-858f-202392dfac98
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 0%

---

# Panoramica di Campaign Management in Advertising DSP

Le campagne DSP hanno la seguente gerarchia:

* Campagna
   * Pacchetto/i
      * Posizionamento/i
         * Annunci
<!-- Do clients think in terms of insertion orders? If yes, then work in the following info.:
In Advertising DSP, an insertion order is represented as a campaign, and line items are represented as packages. Each package includes placements, which can use different strategies and tactics to deliver the line item requirements.
-->

## [!UICONTROL Campaigns]

[Le campagne](/help/dsp/campaign-management/campaigns/campaign-about.md) sono il framework generale delle impostazioni di volo. Ogni campagna è configurata con un inserzionista, date di inizio e fine, un budget complessivo, un’opzione di targeting per più dispositivi e un limite di frequenza predefinito, e opzioni di reporting per visibilità, frode, sicurezza del brand e verifica del pubblico. Tutte le impostazioni a livello di campagna si applicano automaticamente a ciascun pacchetto e posizionamento all’interno della campagna.

## [!UICONTROL Packages]

Ogni campagna può contenere uno o più [pacchetti](/help/dsp/campaign-management/packages/package-about.md), ciascuno dei quali include un set di posizionamenti.

Utilizza i pacchetti per raggruppare i posizionamenti per la consegna a un budget impostato, un obiettivo di prestazioni e una strategia di velocità personalizzata. L’DSP ottimizza i pacchetti spostando i budget sui posizionamenti con le prestazioni migliori all’interno del pacchetto. Puoi organizzare i pacchetti in base al formato di posizionamento, al tipo di inventario, al provider di dati, all’utente tipo o ad altre caratteristiche distinguibili.

I pacchetti sono facoltativi ma consigliati.

## [!UICONTROL Placements]

Un [posizionamento](/help/dsp/campaign-management/placements/placement-about.md) memorizza i parametri di targeting per uno o più annunci dello stesso tipo di annuncio. Puoi creare un posizionamento per una singola campagna o pacchetto, quindi assegnare ad esso gli annunci.

## [!UICONTROL Ads]

[Gli annunci](/help/dsp/campaign-management/ads/ad-about.md) includono le risorse creative e gli URL di tracciamento. Puoi caricare i tag di terze parti per annunci, singolarmente o in blocco, utilizzando i fogli di tag dei partner o il modello di tag collettivo. Puoi anche creare manualmente annunci display nativi da distribuire tramite DSP.

Una volta configurati gli annunci, devi allegare ogni annuncio a un posizionamento per iniziare a eseguire l’annuncio. Puoi allegare un singolo annuncio a uno o più posizionamenti.

Tutti gli annunci attivi e approvati in un posizionamento attivo in una campagna attiva possono essere eseguiti in base ai parametri di targeting del posizionamento.

>[!MORELIKETHIS]
>
>* [Informazioni su Campaign Management](/help/dsp/campaign-management/campaigns/campaign-about.md)
>* [Informazioni sulla gestione dei pacchetti](/help/dsp/campaign-management/packages/package-about.md)
>* [Informazioni sulla gestione del posizionamento](/help/dsp/campaign-management/placements/placement-about.md)
>* [Informazioni Sulla Gestione Degli Annunci](/help/dsp/campaign-management/ads/ad-about.md)
>* [Elenco di controllo per il lancio di Campaign](/help/dsp/campaign-management/campaign-launch-checklist.md)
>* [Procedure consigliate per l&#39;impostazione di campagne sulle prestazioni](/help/dsp/optimization/campaign-best-practices-performance.md)
>* [Tipi di report sulle prestazioni nelle visualizzazioni di Campaign Management](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Gestione Delle Visualizzazioni Dati Della Campagna](/help/dsp/campaign-management/reports/campaign-data-views-manage.md)
>* [Video: struttura dell&#39;account DSP e interfaccia utente](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/ui.html)
