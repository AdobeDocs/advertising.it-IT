---
title: Panoramica della gestione delle campagne in Advertising DSP
description: Scopri la gerarchia di gestione delle campagne e i relativi componenti.
feature: DSP Packages, DSP Placements, DSP Ads
exl-id: 8eb7b4a5-4a31-4637-858f-202392dfac98
TQID: https://experienceleague.adobe.com/w7j86H42OR371vewJM--ep2YUn70XJpMWJQNT92r2CY
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: a4886037-b6d8-40e1-aeab-edeb7649d7d3
  - id: b01c7841-b9d0-4fd5-8458-a6a6f601ad3d
  - id: d9510790-d834-436d-8423-8d69cd50464a
  - id: fddd8d8f-3ba1-4a22-b714-69d0e4655be8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 335
ht-degree: 0%

---

# Panoramica della gestione delle campagne in Advertising DSP

Le campagne DSP hanno la seguente gerarchia:

* Campagna
   * Pacchetto/i
      * Posizionamento/i
         * Annunci
<!--
 Do clients think in terms of insertion orders? If yes, then work in the following info.:
In Advertising DSP, an insertion order is represented as a campaign, and line items are represented as packages. Each package includes placements, which can use different strategies and tactics to deliver the line item requirements.
-->

## [!UICONTROL Campaigns]

[Le campagne](/help/dsp/campaign-management/campaigns/campaign-about.md) sono il framework generale delle impostazioni di volo. Ogni campagna è configurata con un inserzionista, date di inizio e fine, un budget complessivo, un’opzione di targeting per più dispositivi e un limite di frequenza predefinito, e opzioni di reporting per visibilità, frode, sicurezza del brand e verifica del pubblico. Tutte le impostazioni a livello di campagna si applicano automaticamente a ciascun pacchetto e posizionamento all’interno della campagna.

## [!UICONTROL Packages]

Ogni campagna può contenere uno o più [pacchetti](/help/dsp/campaign-management/packages/package-about.md), ciascuno dei quali include un set di posizionamenti.

Utilizza i pacchetti per raggruppare i posizionamenti per la consegna a un budget impostato, un obiettivo di prestazioni e una strategia di velocità personalizzata. DSP ottimizza i pacchetti spostando i budget sui posizionamenti con le prestazioni migliori all’interno del pacchetto. Puoi organizzare i pacchetti in base al formato di posizionamento, al tipo di inventario, al provider di dati, all’utente tipo o ad altre caratteristiche distinguibili.

I pacchetti sono facoltativi ma consigliati.

## [!UICONTROL Placements]

Un [posizionamento](/help/dsp/campaign-management/placements/placement-about.md) memorizza i parametri di targeting per uno o più annunci dello stesso tipo di annuncio. Puoi creare un posizionamento per una singola campagna o pacchetto, quindi assegnare ad esso gli annunci.

## [!UICONTROL Ads]

[Gli annunci](/help/dsp/campaign-management/ads/ad-about.md) includono le risorse creative e gli URL di tracciamento. Puoi caricare i tag di terze parti per annunci, singolarmente o in blocco, utilizzando i fogli di tag dei partner o il modello di tag collettivo. Puoi anche creare manualmente annunci display nativi da distribuire in DSP.

Una volta configurati gli annunci, devi allegare ogni annuncio a un posizionamento per iniziare a eseguire l’annuncio. Puoi allegare un singolo annuncio a uno o più posizionamenti.

Tutti gli annunci attivi e approvati in un posizionamento attivo in una campagna attiva possono essere eseguiti in base ai parametri di targeting del posizionamento.

>[!MORELIKETHIS]
>
>* [Informazioni sulla gestione delle campagne in Advertising DSP](/help/dsp/campaign-management/campaigns/campaign-about.md)
>* [Informazioni sulla gestione dei pacchetti in Advertising DSP](/help/dsp/campaign-management/packages/package-about.md)
>* [Informazioni sulla gestione dei posizionamenti in Advertising DSP](/help/dsp/campaign-management/placements/placement-about.md)
>* [Informazioni sulla gestione degli annunci in Advertising DSP](/help/dsp/campaign-management/ads/ad-about.md)
>* [Elenco di controllo per l&#39;avvio di Campaign](/help/dsp/campaign-management/campaign-launch-checklist.md)
>* [Best practice per la configurazione delle campagne sulle prestazioni](/help/dsp/optimization/campaign-best-practices-performance.md)
>* [Tipi di report sulle prestazioni nelle visualizzazioni di gestione delle campagne](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Gestisci le visualizzazioni dati della campagna](/help/dsp/campaign-management/reports/campaign-data-views-manage.md)
>* [Video: struttura dell&#39;account DSP e interfaccia utente](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/ui.html)
