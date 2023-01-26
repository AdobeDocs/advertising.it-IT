---
title: Visualizza impostazioni annuncio
description: Consulta le descrizioni delle impostazioni di annunci disponibili per gli annunci display.
feature: DSP Ads
exl-id: ae88dfab-0b0c-42ab-9135-422b20a4b6cd
source-git-commit: 1c13874967ec4ad264e5fa6a5e0dfeb6120f53cc
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 0%

---

# Visualizza impostazioni annuncio

Le seguenti impostazioni sono per gli annunci display standard.

## [!UICONTROL Ad Options]

### Base

**[!UICONTROL Ad Type]:** (Sola lettura) Il tipo di annuncio che stai creando, che corrisponde al tipo di posizionamento a cui l’annuncio può essere allegato. Per impostazione predefinita *[!UICONTROL Display]*.

**[!UICONTROL Ad Name]:** Nome dell&#39;annuncio. Il titolo della risorsa viene utilizzato per impostazione predefinita, ma puoi modificarlo.

>[!TIP]
>
> Utilizza un nome che sarà facile trovare quando alleghi l’annuncio a un posizionamento, nella [!UICONTROL Ads] e nei rapporti. Ad esempio, descrivi il tipo di unità e alcuni attributi chiave (ad esempio, Anteprima del prodotto in vacanza): 300x250 Gamer&quot;).

**\[Origine annuncio\]**: (Sola lettura) *[!UICONTROL 3rd party]*.

**[!UICONTROL This is an expandable Banner]:** (Solo annunci di terze parti) Indica che l’annuncio è un annuncio di banner espandibile. Le impostazioni di espansione correlate determinano quale inventario acquistare, in modo che riflettano il comportamento dell’annuncio.

**[!UICONTROL Expansion Method]:** (Solo annunci banner espandibili di terze parti) Se il banner si espande *[!UICONTROL Click]* o *[!UICONTROL Rollover]*.

**[!UICONTROL Expansion Directions]:** (Solo annunci banner espandibili di terze parti) La direzione in cui l’annuncio si espande: *[!UICONTROL Up]*, *[!UICONTROL Down]*, *[!UICONTROL Left]* oppure *[!UICONTROL Right]*.

**[!UICONTROL Certified Vendors]:** (Solo annunci banner espandibili di terze parti) Il fornitore certificato per cui l’annuncio è disponibile: *[!UICONTROL DCM]* ([!DNL Google DoubleClick for Advertisers]), *[!UICONTROL Flashtalking]*, *[!UICONTROL Sizmek]* oppure *[!UICONTROL Jivox]*.

**[!UICONTROL Display Code]:** (Solo annunci di terze parti) L’URL della risorsa creativa di terze parti. Qualsiasi [timestamp] e [[timestamp]] verranno sostituiti con valori effettivi.

**[!UICONTROL Final Display Code]:** (Solo annunci di terze parti) L’URL per la risorsa creativa di terze parti, con l’opzione necessaria [Macro per il tracciamento DSP pubblicità](/help/dsp/campaign-management/macros.md) se del caso.

**[!UICONTROL Ad Size]:** Larghezza e altezza dell’annuncio. Deve essere un [dimensioni e display standard supportati](ad-specs.md). Puoi immettere manualmente la dimensione dell’annuncio prima di caricare l’annuncio o immettere un [!UICONTROL Display Code]. Se non immetti la dimensione dell’annuncio, le dimensioni dell’annuncio o del tag dell’annuncio caricato vengono automaticamente inserite come di sola lettura. L’annuncio Display non viene salvato se le dimensioni non si trovano in Visualizzazione standard come dimensioni, ad esempio 301x250 invece di 300x250 dimensioni dell’annuncio.

>[!IMPORTANT]
>
> La dimensione dell’annuncio dichiarata nei campi larghezza e altezza corrisponde alle richieste di offerta in arrivo. Potresti riscontrare problemi di consegna se le dimensioni dell’annuncio non corrispondono alle dimensioni dell’annuncio dichiarate.

### [!UICONTROL Pixel]

Tutti i pixel di tracciamento degli eventi esistenti per il posizionamento vengono automaticamente collegati. Puoi scollegare i pixel esistenti e creare nuovi pixel in base alle tue esigenze di tracciamento per il singolo annuncio.

Le seguenti impostazioni si applicano a ogni pixel creato o modificato.

**[!UICONTROL Integration Event]:** L&#39;evento che attiva il pixel da attivare. Per questo tipo di annuncio, utilizza i pixel che attivano *[!UICONTROL Impression]* o *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Se il pixel è un *[!UICONTROL IMG URL]* (file immagine da 1 pixel), *[!UICONTROL HTML]* oppure *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** L&#39;URL dell&#39;immagine pixel, nel formato appropriato per il [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** Nome del pixel. Utilizza un nome che ti aiuti a identificare facilmente il pixel.

**[!UICONTROL Pixel Provider]:** Provider di pixel: *[!UICONTROL None]*, *[!UICONTROL Nielsen]* oppure *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [Informazioni sulla gestione degli annunci](ad-about.md)
>* [Creare un singolo annuncio](ad-create.md)
>* [Elencare i posizionamenti associati a un annuncio](ad-list-placements.md)
>* [Specifiche degli annunci](ad-specs.md)
>* [Macro DSP](/help/dsp/campaign-management/macros.md)

