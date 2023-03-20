---
title: Domande frequenti sui video universali
description: Ulteriori informazioni sugli annunci video universali.
feature: DSP Placements, DSP Ads
source-git-commit: 8e0237355e834f4ae2b9ef1ed211e047b41cafe7
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# # Domande frequenti sul video universale

## Come si creano posizionamenti video universali e annunci?

I posizionamenti video universali possono contenere solo annunci video universali e gli annunci video universali possono essere collegati solo a posizionamenti video universali.

Crea in modo simile a come crei altri tipi di posizionamenti e video:

1. All&#39;interno della campagna desiderata, [creare un posizionamento video universale](/help/dsp/campaign-management/placements/placement-create.md), selezionando [!UICONTROL Placement Type] **[!UICONTROL Universal Video]**.

   È necessario specificare almeno un ambiente (Desktop, Mobile, Connected TV) da utilizzare.

1. Nella stessa campagna del posizionamento video universale, [creare un singolo annuncio video universale](/help/dsp/campaign-management/ads/ad-create.md) o [creare più annunci video universali](/help/dsp/campaign-management/ads/ad-create-multiple.md).

   Se crei più annunci, assicurati di specificare &quot;[!UICONTROL Universal Video]&quot; come [!UICONTROL Ad Type]. Per [!DNL Google] o [!DNL Flashtalking] annunci, dopo aver caricato il file, fai clic sul campo Tipo di annuncio nel &quot;[!UICONTROL Review ad types]&quot; e modificarlo. Per altri tipi di tag annuncio, specifica il tipo di annuncio all’interno del file foglio di calcolo caricato.

1. [Apri le impostazioni dell’annuncio](/help/dsp/campaign-management/ads/ad-edit.md) per ogni nuovo annuncio e seleziona il formato video applicabile:

   * **[!UICONTROL VPAID]:** La visualizzabilità viene sempre misurata.
   * **[!UICONTROL VPAID & VAST (Default)]:** Include inventario che non consente la misurazione della visualizzabilità.
   * **[!UICONTROL VAST]** - Adatto per l&#39;inventario televisivo collegato.

   Vedere &quot;[Impostazioni degli annunci video universali](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)&quot; per ulteriori informazioni.

1. [Allega i nuovi annunci video universali](/help/dsp/campaign-management/ads/ad-attach-to-placement.md) al posizionamento video universale.

## Perché alcuni obiettivi e pacchetti di ottimizzazione non sono disponibili quando l’ambiente TV connesso è selezionato per un posizionamento video universale?

Gli obiettivi incompatibili con i posizionamenti TV collegati standard, ad esempio il costo per clic più basso, non sono supportati per l&#39;ambiente TV connesso in posizionamenti video universali. Allo stesso modo, anche i pacchetti con obiettivi di ottimizzazione incompatibili non sono disponibili per la selezione.

## Quando dovrebbe essere **[!UICONTROL VAST]** il formato video può essere utilizzato per annunci video universali?

Utilizzo **[!UICONTROL VAST]** in uno dei seguenti scenari:

* Il posizionamento sarà indirizzato all&#39;inventario televisivo connesso.
* Il posizionamento eseguirà il targeting dell’inventario video da Google Ad Manager, Appnexus, SpotX o FreeWheel. Questi SSP non supportano il formato video VPAID e VAST.

## È possibile collegare più annunci video universali allo stesso posizionamento video universale?

Sì.
