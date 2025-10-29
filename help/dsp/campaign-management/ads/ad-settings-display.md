---
title: Visualizza impostazioni annuncio
description: Consulta le descrizioni delle impostazioni pubblicitarie disponibili per gli annunci display.
feature: DSP Ads
exl-id: cff65a48-486f-401e-9759-2bb63871448f
source-git-commit: 863bf7a4d8304e42b7004742de59b9e1a09f81b7
workflow-type: tm+mt
source-wordcount: '314'
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

<!-- **[!UICONTROL Pixel]:** -->

{{$include /help/_includes/dsp-ad-pixel.md}}

>[!MORELIKETHIS]
>
>* [Informazioni Sulla Gestione Degli Annunci](ad-about.md)
>* [Crea un annuncio singolo](ad-create.md)
>* [Elenca i posizionamenti associati a un annuncio](ad-list-placements.md)
>* [Specifiche annuncio](ad-specs.md)
>* [Macro DSP](/help/dsp/campaign-management/macros.md)
