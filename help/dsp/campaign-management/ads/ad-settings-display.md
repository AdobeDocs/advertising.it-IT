---
title: Visualizza impostazioni annuncio
description: Consulta le descrizioni delle impostazioni pubblicitarie disponibili per gli annunci display.
feature: DSP Ads
exl-id: cff65a48-486f-401e-9759-2bb63871448f
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '444'
ht-degree: 0%

---

# Visualizza impostazioni annuncio

Le seguenti impostazioni sono per gli annunci display standard.

## [!UICONTROL Ad Options]

### Base

**[!UICONTROL Ad Type]:** (sola lettura) Il tipo di annuncio che stai creando, che corrisponde al tipo di posizionamento a cui l&#39;annuncio può essere allegato. Il valore predefinito è *[!UICONTROL Display]*.

**[!UICONTROL Ad Name]:** Il nome dell&#39;annuncio. Il titolo della risorsa è utilizzato per impostazione predefinita, ma puoi modificarne il nome.

>[!TIP]
>
> Utilizzare un nome facilmente individuabile quando si allega l&#39;annuncio a un posizionamento, nella visualizzazione [!UICONTROL Ads] e nei report. Ad esempio, descrivi il tipo di unità e alcuni attributi chiave (come Anteprima prodotto per vacanze: 300x250 Gamer&quot;).

**\[Ad Source\]**: (sola lettura) *[!UICONTROL 3rd party]*.

**[!UICONTROL This is an expandable Banner]:** (solo annunci di terze parti) indica che l&#39;annuncio è un banner pubblicitario espandibile. Le impostazioni di espansione correlate determinano quale inventario acquistare, quindi assicurati che riflettano il comportamento dell’annuncio.

**[!UICONTROL Expansion Method]:** (solo annunci banner espandibili di terze parti) Se il banner si espande su *[!UICONTROL Click]* o *[!UICONTROL Rollover]*.

**[!UICONTROL Expansion Directions]:** (solo banner pubblicitari espandibili di terze parti) La direzione di espansione dell&#39;annuncio: *[!UICONTROL Up]*, *[!UICONTROL Down]*, *[!UICONTROL Left]* o *[!UICONTROL Right]*.

**[!UICONTROL Certified Vendors]:** (solo banner pubblicitari espandibili di terze parti) Il fornitore certificato per il quale l&#39;annuncio è disponibile: *[!UICONTROL DCM]* ([!DNL Google DoubleClick for Advertisers]), *[!UICONTROL Flashtalking]*, *[!UICONTROL Sizmek]* o *[!UICONTROL Jivox]*.

**[!UICONTROL Display Code]:** (solo annunci di terze parti) URL della risorsa creativa di terze parti. Tutti i parametri [timestamp] e [[timestamp]] vengono sostituiti con i valori effettivi.

**[!UICONTROL Final Display Code]:** (solo annunci di terze parti) URL per la risorsa creativa di terze parti, con le [macro di tracciamento Advertising DSP](/help/dsp/campaign-management/macros.md) inserite, se applicabili.

**[!UICONTROL Ad Size]:** Larghezza e altezza dell&#39;annuncio. Deve essere una [dimensione annuncio visualizzazione standard supportata](ad-specs.md). Puoi immettere manualmente le dimensioni dell&#39;annuncio prima di caricarlo o immettere [!UICONTROL Display Code]. Se non immetti la dimensione dell’annuncio, le dimensioni del caricamento o del tag dell’annuncio vengono immesse automaticamente come di sola lettura.

>[!IMPORTANT]
>
> Le dimensioni dell’annuncio dichiarate nei campi di larghezza e altezza corrispondono alle richieste di offerta in arrivo. Potresti riscontrare problemi di consegna se le dimensioni dell’annuncio non corrispondono a quelle dichiarate.

### [!UICONTROL Pixel]

Tutti i pixel di tracciamento degli eventi esistenti per il posizionamento vengono associati automaticamente. Puoi scollegare i pixel esistenti e crearne di nuovi, in base alle tue esigenze di tracciamento per il singolo annuncio. **Suggerimento:** per modificare i pixel di tracciamento di terze parti per più annunci in un posizionamento contemporaneamente utilizzando la visualizzazione [!UICONTROL Ad Tools], vedere &quot;[Allega pixel di tracciamento di terze parti agli annunci in un posizionamento](/help/dsp/campaign-management/ads/ad-attach-to-placement.md#attach-pixels-ads).&quot;

Le seguenti impostazioni si applicano a ogni pixel creato o modificato.

**[!UICONTROL Integration Event]:** l&#39;evento che attiva il pixel per l&#39;attivazione. Per questo tipo di annuncio, utilizza i pixel che attivano *[!UICONTROL Impression]* o *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Se il pixel è un *[!UICONTROL IMG URL]* (file immagine 1x1 pixel), *[!UICONTROL HTML]* o *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** URL dell&#39;immagine pixel nel formato appropriato per [!UICONTROL Pixel Type] specificato.

**[!UICONTROL Pixel Name]:** Il nome del pixel. Utilizza un nome che ti consenta di identificare facilmente il pixel.

**[!UICONTROL Pixel Provider]:** Provider pixel: *[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]* o *[!UICONTROL IAS]*.

>[!MORELIKETHIS]
>
>* [Informazioni Sulla Gestione Degli Annunci](ad-about.md)
>* [Crea un annuncio singolo](ad-create.md)
>* [Elenca i posizionamenti associati a un annuncio](ad-list-placements.md)
>* [Specifiche annuncio](ad-specs.md)
>* [Macro DSP](/help/dsp/campaign-management/macros.md)
