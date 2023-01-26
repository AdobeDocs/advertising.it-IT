---
title: Impostazioni degli annunci TV collegati
description: Vedi le descrizioni delle impostazioni degli annunci disponibili per gli annunci TV collegati.
feature: DSP Ads
exl-id: d8e47f7e-7480-400f-8ffa-ecf41ce2ebfb
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '495'
ht-degree: 0%

---

# Impostazioni degli annunci TV collegati

## [!UICONTROL Insert Ad Tag]

*Solo nuovi annunci*

**[!UICONTROL URL]**: URL del tag VAST.

**[!UICONTROL Title]**: Nome del file che verrà utilizzato nella visualizzazione Annunci e nei rapporti.

>[!TIP]
>
> Per verificare la validità di un tag VAST, incollalo in un browser e premi il pulsante **[!UICONTROL Enter]** chiave. Se il tag è valido, verrà visualizzato un file XML che include `<VAST>` vicino alla cima.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (Sola lettura) Il tipo di annuncio che stai creando, che corrisponde al tipo di posizionamento a cui l’annuncio può essere allegato.

**[!UICONTROL Ad Name]:** Nome dell&#39;annuncio. Il titolo della risorsa viene utilizzato per impostazione predefinita, ma puoi modificarlo.

>[!TIP]
>
> Utilizza un nome che sarà facile trovare quando alleghi l’annuncio a un posizionamento, nella [!UICONTROL Ads] e nei rapporti. Ad esempio, descrivi il tipo di unità e alcuni attributi chiave (ad esempio, Anteprima del prodotto in vacanza): 30 sec CTV&quot;).

**[!UICONTROL Width | Ad Unit Width]:** Larghezza dell&#39;intera unità pubblicitaria. Questa opzione può essere bloccata a seconda del tipo di unità pubblicitaria selezionata.

**[!UICONTROL Height | Ad Unit Height]:** Altezza dell&#39;intera unità pubblicitaria. Questa opzione può essere bloccata a seconda del tipo di unità pubblicitaria selezionata.

**[!UICONTROL Player X]:** La coordinata X per l&#39;unità dell&#39;annuncio. Mantieni l’impostazione predefinita.

**[!UICONTROL Player Y]:** La coordinata Y per l&#39;unità dell&#39;annuncio. Mantieni l’impostazione predefinita.

**[!UICONTROL Player Width]:** Larghezza dell&#39;intera unità pubblicitaria. Questa opzione può essere bloccata a seconda del tipo di unità pubblicitaria selezionata.

È lo stesso del **[!UICONTROL Width]** campo .

**[!UICONTROL Player Height]:** Altezza dell&#39;intera unità pubblicitaria. Questa opzione può essere bloccata a seconda del tipo di unità pubblicitaria selezionata.

È lo stesso del **[!UICONTROL Height]** campo .

**[!UICONTROL Show Controls]:** Dove includere i controlli video per l’annuncio: *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]* oppure *[!UICONTROL None]* (impostazione predefinita).

**[!UICONTROL Preserve Aspect Ratio]:** Se mantenere le proporzioni di larghezza e altezza del video (*[!UICONTROL Yes]*) o per allungare il video per riempire lo spazio disponibile (*[!UICONTROL No]*).

**[!UICONTROL VAST Tag]:** (Annunci che utilizzano solo tag VAST; sola lettura) Il tag VAST di terze parti immesso come origine dell&#39;annuncio.

**[!UICONTROL Final VAST Tag]:** (Annunci che utilizzano solo tag VAST; di sola lettura) Il tag VAST di terze parti immesso come origine dell&#39;annuncio con il necessario [Macro per il tracciamento DSP pubblicità](/help/dsp/campaign-management/macros.md) se del caso.

**[!UICONTROL Clock Number]**: (Utilizzato solo nel Regno Unito; disponibile solo per gli utenti con autorizzazione) Un identificatore univoco utilizzato per garantire la trasmissione dell&#39;annuncio corretto. Se questa impostazione non è applicabile, lasciala vuota.

### [!UICONTROL Pixel]

Tutti i pixel di tracciamento degli eventi esistenti per il posizionamento vengono automaticamente collegati. Puoi scollegare i pixel esistenti e creare nuovi pixel in base alle tue esigenze di tracciamento per il singolo annuncio.

Le seguenti impostazioni si applicano a ogni pixel creato o modificato.

**[!UICONTROL Integration Event]:** L&#39;evento che attiva il pixel da attivare. Per questo tipo di annuncio, utilizza i pixel che attivano *[!UICONTROL Impression]* o *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Se il pixel è un *[!UICONTROL IMG URL]* (file immagine da 1 pixel), *[!UICONTROL HTML]* oppure *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** L&#39;URL dell&#39;immagine pixel, nel formato appropriato per il tipo di pixel specificato.

**[!UICONTROL Pixel Name]:** Nome del pixel. Utilizza un nome che ti aiuti a identificare facilmente il pixel.

**[!UICONTROL Pixel Provider]:** Provider di pixel: *[!UICONTROL None]*, *[!UICONTROL Nielsen]* oppure *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [Informazioni sulla gestione degli annunci](ad-about.md)
>* [Creare un singolo annuncio](ad-create.md)
>* [Elencare i posizionamenti associati a un annuncio](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Specifiche degli annunci](ad-specs.md)
>* [Macro DSP](/help/dsp/campaign-management/macros.md)

