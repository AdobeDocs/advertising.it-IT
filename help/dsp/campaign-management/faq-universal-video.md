---
title: Domande frequenti sui video universali
description: Ulteriori informazioni sugli annunci video universali.
feature: DSP Placements, DSP Ads
exl-id: 48c744ae-90a3-47e9-a5dc-c4e3c01b75a0
source-git-commit: 8d65069b7da5d3c33cc7713c6c80af27eb6bf227
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Domande frequenti sui video universali

[Annunci video universali](/help/dsp/campaign-management/ads/ad-about.md#ad-types) consente di eseguire il targeting dell&#39;inventario video dagli ambienti desktop, mobile e TV connessi per l&#39;inventario VPAID e VAST utilizzando un unico posizionamento video.

## Come si creano posizionamenti video e annunci universali?

I posizionamenti video universali possono contenere solo annunci video universali e gli annunci video universali possono essere collegati solo a posizionamenti video universali.

Crea posizionamenti e annunci video universali in modo simile a come si creano altri tipi di posizionamenti e video:

1. Nella campagna desiderata, [crea un posizionamento video universale](/help/dsp/campaign-management/placements/placement-create.md), selezionando [!UICONTROL Placement Type] **[!UICONTROL Universal Video]**.

   È necessario specificare almeno un ambiente (Desktop, Mobile, Connected TV) per la destinazione.

1. Nella stessa campagna del posizionamento video universale, [crea un singolo annuncio video universale](/help/dsp/campaign-management/ads/ad-create.md) o [crea più annunci video universali](/help/dsp/campaign-management/ads/ad-create-multiple.md).

   Se crei più annunci, assicurati di specificare &quot;[!UICONTROL Universal Video]&quot; come [!UICONTROL Ad Type]:

   * Per [!DNL Google] o [!DNL Flashtalking] annunci: nel passaggio &quot;[!UICONTROL Review ad types]&quot; dopo aver caricato il file, fai clic sul campo **[!UICONTROL Ad Type]** e seleziona **[!UICONTROL Universal Video]**.

   * Per altri tipi di tag annuncio: all&#39;interno del file del foglio di calcolo caricato, specifica il campo Tipo annuncio per ogni annuncio come **[!UICONTROL Universal Video]**.

1. [Apri le impostazioni dell&#39;annuncio](/help/dsp/campaign-management/ads/ad-edit.md) per ogni nuovo annuncio e seleziona il formato video applicabile:

   * **[!UICONTROL VPAID]:** La visibilità viene sempre misurata.
   * **[!UICONTROL VPAID & VAST (Default)]:** Include un inventario che non consente la misurazione della visualizzabilità.
   * **[!UICONTROL VAST]** - Adatto per l&#39;inventario TV connessa.

   Per ulteriori informazioni, consulta &quot;[Impostazioni annuncio video universale](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)&quot;.

1. [Allega i nuovi annunci video universali](/help/dsp/campaign-management/ads/ad-attach-to-placement.md) al posizionamento video universale.

## Perché alcuni obiettivi e pacchetti di ottimizzazione non sono disponibili quando l’ambiente TV collegata è selezionato per un posizionamento video universale?

Gli obiettivi incompatibili con i posizionamenti TV connessi standard, ad esempio il costo inferiore per clic, non sono supportati per l’ambiente TV connesso nei posizionamenti video universali. Analogamente, non è possibile selezionare pacchetti con obiettivi di ottimizzazione incompatibili.

## Quando utilizzare il formato video **[!UICONTROL VAST]** per gli annunci video universali?

Utilizzare **[!UICONTROL VAST]** in uno dei seguenti scenari:

* Il posizionamento è destinato all’inventario dei televisori connessi.
* Il posizionamento esegue il targeting dell’inventario video da Google Ad Manager, Appnexus, SpotX o Freewheel. Questi provider di servizi condivisi non supportano il formato video VPAID e VAST.

## È possibile allegare più annunci video universali allo stesso posizionamento video universale?

Sì.
