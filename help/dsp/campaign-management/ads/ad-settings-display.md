---
title: Visualizza impostazioni annuncio
description: Consulta le descrizioni delle impostazioni pubblicitarie disponibili per gli annunci display.
feature: DSP Ads
exl-id: cff65a48-486f-401e-9759-2bb63871448f
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 0%

---

# Visualizza impostazioni annuncio

Le seguenti impostazioni sono per gli annunci display standard.

## [!UICONTROL Ad Options]

### Base

**[!UICONTROL Ad Type]:** (Sola lettura) Il tipo di annuncio che stai creando, che corrisponde al tipo di posizionamento a cui l’annuncio può essere allegato. Il valore predefinito è *[!UICONTROL Display]*.

**[!UICONTROL Ad Name]:** Il nome dell’annuncio. Il titolo della risorsa è utilizzato per impostazione predefinita, ma puoi modificarne il nome.

>[!TIP]
>
> Utilizza un nome facile da trovare quando alleghi l’annuncio a un posizionamento, nella [!UICONTROL Ads] e nei rapporti. Ad esempio, descrivi il tipo di unità e alcuni attributi chiave (come Anteprima prodotto per vacanze: 300x250 Gamer&quot;).

**\[Origine annuncio\]**: (sola lettura) *[!UICONTROL 3rd party]*.

**[!UICONTROL This is an expandable Banner]:** (Solo annunci di terze parti) Indica che l’annuncio è un annuncio banner espandibile. Le impostazioni di espansione correlate determinano quale inventario acquistare, quindi assicurati che riflettano il comportamento dell’annuncio.

**[!UICONTROL Expansion Method]:** (Solo banner pubblicitari espandibili di terze parti) Se il banner si espande *[!UICONTROL Click]* o *[!UICONTROL Rollover]*.

**[!UICONTROL Expansion Directions]:** (Solo per banner pubblicitari espandibili di terze parti) La direzione in cui l’annuncio si espande: *[!UICONTROL Up]*, *[!UICONTROL Down]*, *[!UICONTROL Left]*, o *[!UICONTROL Right]*.

**[!UICONTROL Certified Vendors]:** (Solo banner pubblicitari espandibili di terze parti) Il fornitore certificato per il quale l’annuncio è disponibile: *[!UICONTROL DCM]* ([!DNL Google DoubleClick for Advertisers]), *[!UICONTROL Flashtalking]*, *[!UICONTROL Sizmek]*, o *[!UICONTROL Jivox]*.

**[!UICONTROL Display Code]:** (Solo per annunci di terze parti) L’URL della risorsa creativa di terze parti. Qualsiasi [timestamp] e [[timestamp]] vengono sostituiti con i valori effettivi.

**[!UICONTROL Final Display Code]:** (Solo per annunci di terze parti) L’URL della risorsa creativa di terze parti, con il necessario [Pubblicità delle macro di tracciamento DSP](/help/dsp/campaign-management/macros.md) se del caso.

**[!UICONTROL Ad Size]:** Larghezza e altezza dell’annuncio. Deve essere un [dimensioni annuncio display standard supportate](ad-specs.md). Puoi immettere manualmente le dimensioni dell’annuncio prima di caricarlo o immettere un [!UICONTROL Display Code]. Se non immetti la dimensione dell’annuncio, le dimensioni del caricamento o del tag dell’annuncio vengono immesse automaticamente come di sola lettura. L’annuncio di visualizzazione non viene salvato se le dimensioni non rientrano nel display standard come dimensioni, ad esempio 301x250 invece delle dimensioni dell’annuncio 300x250.

>[!IMPORTANT]
>
> Le dimensioni dell’annuncio dichiarate nei campi di larghezza e altezza corrispondono alle richieste di offerta in arrivo. Potresti riscontrare problemi di consegna se le dimensioni dell’annuncio non corrispondono a quelle dichiarate.

### [!UICONTROL Pixel]

Tutti i pixel di tracciamento degli eventi esistenti per il posizionamento vengono associati automaticamente. Puoi scollegare i pixel esistenti e crearne di nuovi, in base alle tue esigenze di tracciamento per il singolo annuncio. **Suggerimento** Per modificare i pixel di tracciamento di terze parti per più annunci in un posizionamento contemporaneamente utilizzando [!UICONTROL Ad Tools] visualizzare, vedere &quot;[Allegare pixel di tracciamento di terze parti agli annunci in un posizionamento](/help/dsp/campaign-management/ads/ad-attach-to-placement.md#attach-pixels-ads).&quot;

Le seguenti impostazioni si applicano a ogni pixel creato o modificato.

**[!UICONTROL Integration Event]:** L’evento che attiva il pixel da attivare. Per questo tipo di annuncio, utilizza i pixel che vengono attivati sul *[!UICONTROL Impression]* o *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Se il pixel è un *[!UICONTROL IMG URL]* (file di immagine 1x1 pixel), *[!UICONTROL HTML]*, o *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** L&#39;URL dell&#39;immagine pixel nel formato appropriato per il [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** Il nome del pixel. Utilizza un nome che ti consenta di identificare facilmente il pixel.

**[!UICONTROL Pixel Provider]:** Il provider pixel: *[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]*, o *[!UICONTROL IAS]*.

>[!MORELIKETHIS]
>
>* [Informazioni sulla gestione degli annunci](ad-about.md)
>* [Creare un singolo annuncio](ad-create.md)
>* [Elencare i posizionamenti associati a un annuncio](ad-list-placements.md)
>* [Specifiche annuncio](ad-specs.md)
>* [Macro per DSP](/help/dsp/campaign-management/macros.md)
