---
title: Impostazioni annuncio TV collegato
description: Vedere le descrizioni delle impostazioni disponibili per gli annunci TV connessi.
feature: DSP Ads
exl-id: d8e47f7e-7480-400f-8ffa-ecf41ce2ebfb
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '522'
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

Tutti i pixel di tracciamento degli eventi esistenti per il posizionamento vengono associati automaticamente. Puoi scollegare i pixel esistenti e crearne di nuovi, in base alle tue esigenze di tracciamento per il singolo annuncio. **Suggerimento:** per modificare i pixel di tracciamento di terze parti per più annunci in un posizionamento contemporaneamente utilizzando la visualizzazione [!UICONTROL Ad Tools], vedere &quot;[Allega pixel di tracciamento di terze parti agli annunci in un posizionamento](/help/dsp/campaign-management/ads/ad-attach-to-placement.md#attach-pixels-ads).&quot;

Le seguenti impostazioni si applicano a ogni pixel creato o modificato.

**[!UICONTROL Integration Event]:** l&#39;evento che attiva il pixel per l&#39;attivazione. Per questo tipo di annuncio, utilizza i pixel che attivano *[!UICONTROL Impression]* o *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Se il pixel è un *[!UICONTROL IMG URL]* (file immagine 1x1 pixel), *[!UICONTROL HTML]* o *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** URL dell&#39;immagine pixel nel formato appropriato per il tipo di pixel specificato.

**[!UICONTROL Pixel Name]:** Il nome del pixel. Utilizza un nome che ti consenta di identificare facilmente il pixel.

**[!UICONTROL Pixel Provider]:** Provider pixel: *[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]* o *[!UICONTROL IAS]*.

>[!MORELIKETHIS]
>
>* [Informazioni Sulla Gestione Degli Annunci](ad-about.md)
>* [Crea un annuncio singolo](ad-create.md)
>* [Elenca i posizionamenti associati a un annuncio](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Specifiche annuncio](ad-specs.md)
>* [Macro DSP](/help/dsp/campaign-management/macros.md)
