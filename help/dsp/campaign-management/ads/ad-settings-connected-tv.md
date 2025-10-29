---
title: Impostazioni annuncio TV collegato
description: Vedere le descrizioni delle impostazioni disponibili per gli annunci TV connessi.
feature: DSP Ads
exl-id: d8e47f7e-7480-400f-8ffa-ecf41ce2ebfb
source-git-commit: 863bf7a4d8304e42b7004742de59b9e1a09f81b7
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---

# Impostazioni annuncio TV collegato

## [!UICONTROL Insert Ad Tag]

*Solo nuovi annunci*

**[!UICONTROL URL]**: URL del tag VAST.

**[!UICONTROL Title]**: nome per il file, utilizzato nella visualizzazione Annunci e nei report.

>[!TIP]
>
> Per verificare la validità di un tag VAST, incollarlo in un browser e premere il tasto **[!UICONTROL Enter]**. Se il tag è valido, verrà visualizzato un file XML che include `<VAST>` nella parte superiore.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (sola lettura) Il tipo di annuncio che stai creando, che corrisponde al tipo di posizionamento a cui l&#39;annuncio può essere allegato.

**[!UICONTROL Ad Name]:** Il nome dell&#39;annuncio. Il titolo della risorsa è utilizzato per impostazione predefinita, ma puoi modificarne il nome.

>[!TIP]
>
> Utilizzare un nome facilmente individuabile quando si allega l&#39;annuncio a un posizionamento, nella visualizzazione [!UICONTROL Ads] e nei report. Ad esempio, descrivi il tipo di unità e alcuni attributi chiave (come Anteprima prodotto per vacanze: 30sec CTV&quot;).

**[!UICONTROL Width | Ad Unit Width]:** la larghezza dell&#39;intera unità pubblicitaria. Questa opzione può essere bloccata a seconda del tipo di unità pubblicitaria selezionato.

**[!UICONTROL Height | Ad Unit Height]:** altezza dell&#39;intera unità pubblicitaria. Questa opzione può essere bloccata a seconda del tipo di unità pubblicitaria selezionato.

**[!UICONTROL Player X]:** La coordinata X per l&#39;unità annuncio. Mantenere l&#39;impostazione predefinita.

**[!UICONTROL Player Y]:** La coordinata Y dell&#39;unità annuncio. Mantenere l&#39;impostazione predefinita.

**[!UICONTROL Player Width]:** la larghezza dell&#39;intera unità pubblicitaria. Questa opzione può essere bloccata a seconda del tipo di unità pubblicitaria selezionato.

È lo stesso del campo **[!UICONTROL Width]**.

**[!UICONTROL Player Height]:** altezza dell&#39;intera unità pubblicitaria. Questa opzione può essere bloccata a seconda del tipo di unità pubblicitaria selezionato.

È lo stesso del campo **[!UICONTROL Height]**.

**[!UICONTROL Show Controls]:** Dove includere i controlli video per l&#39;annuncio: *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]* o *[!UICONTROL None]* (impostazione predefinita).

**[!UICONTROL Preserve Aspect Ratio]:** se mantenere le proporzioni di larghezza e altezza del video (*[!UICONTROL Yes]*) o allungare il video per riempire lo spazio disponibile (*[!UICONTROL No]*).

**[!UICONTROL VAST Tag]:** (annunci che utilizzano solo tag VAST; sola lettura) Il tag VAST di terze parti immesso come origine dell&#39;annuncio.

**[!UICONTROL Final VAST Tag]:** (annunci che utilizzano solo tag VAST; sola lettura) Il tag VAST di terze parti immesso come origine dell&#39;annuncio con le [macro di tracciamento Advertising DSP](/help/dsp/campaign-management/macros.md) inserite, se applicabili.

**[!UICONTROL Clock Number]**: (utilizzato solo nel Regno Unito; disponibile solo per gli utenti autorizzati) Identificatore univoco utilizzato per garantire che l&#39;annuncio corretto venga trasmesso. Se questa impostazione non è applicabile, lasciarla vuota.

### [!UICONTROL Pixel]

<!-- **[!UICONTROL Pixel]:** -->

{{$include /help/_includes/dsp-ad-pixel.md}}

>[!MORELIKETHIS]
>
>* [Informazioni Sulla Gestione Degli Annunci](ad-about.md)
>* [Crea un annuncio singolo](ad-create.md)
>* [Elenca i posizionamenti associati a un annuncio](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Specifiche annuncio](ad-specs.md)
>* [Macro DSP](/help/dsp/campaign-management/macros.md)
