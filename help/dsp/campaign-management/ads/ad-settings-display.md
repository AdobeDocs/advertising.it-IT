---
title: Impostazioni degli annunci di visualizzazione
description: Consulta le descrizioni delle impostazioni pubblicitarie disponibili per gli annunci display.
feature: DSP Ads
exl-id: cff65a48-486f-401e-9759-2bb63871448f
TQID: https://experienceleague.adobe.com/bcuGR2fzcwjvPcWisdQZBbU8vcaZhgW2qZPAXjV5ndM
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: d9510790-d834-436d-8423-8d69cd50464a
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 317
ht-degree: 0%

---

# Impostazioni degli annunci di visualizzazione

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
>* [Informazioni sulla gestione degli annunci in Advertising DSP](ad-about.md)
>* [Crea un singolo annuncio](ad-create.md)
>* [Elencare i posizionamenti associati a un annuncio](ad-list-placements.md)
>* [Specifiche annuncio](ad-specs.md)
>* [Macro di DSP](/help/dsp/campaign-management/macros.md)
