---
title: Impostazioni annuncio mobile
description: Consulta le descrizioni delle impostazioni pubblicitarie disponibili per gli annunci per dispositivi mobili.
feature: DSP Ads
exl-id: 45e8da8c-d6a2-4c42-8932-4cf551f6f899
source-git-commit: 863bf7a4d8304e42b7004742de59b9e1a09f81b7
workflow-type: tm+mt
source-wordcount: '513'
ht-degree: 0%

---

# Impostazioni annuncio mobile

## [!UICONTROL Insert Ad Tag]

*Solo i nuovi formati di annunci video per dispositivi mobili*

**[!UICONTROL URL]** o **[!UICONTROL Ad Tag]**: tag annuncio o tag annuncio VAST di terze parti contenente risorse creative e pixel di tracciamento

**[!UICONTROL Ad Title]** o **[!UICONTROL Title]**: nome per l&#39;annuncio utilizzato nella visualizzazione e nei report [!UICONTROL Ads].

>[!TIP]
>
> Per verificare la validità di un tag VAST, incollarlo in un browser e premere il tasto **[!UICONTROL Enter]**. Se il tag è valido, verrà visualizzato un file XML che include `<VAST>` nella parte superiore.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]: annunci display per dispositivi mobili

**[!UICONTROL Ad Type]:** (sola lettura) Il tipo di annuncio che stai creando, che corrisponde al tipo di posizionamento a cui l&#39;annuncio può essere allegato.

**[!UICONTROL Ad Name]:** Il nome dell&#39;annuncio. Il titolo della risorsa è utilizzato per impostazione predefinita, ma puoi modificarne il nome.

>[!TIP]
>
> Utilizza un nome facile da trovare quando alleghi l’annuncio a un posizionamento, nella vista Annunci e nei rapporti. Ad esempio, descrivi il tipo di unità e alcuni attributi chiave (come Anteprima prodotto per vacanze: 300x250 Gamer&quot;).

**\[Ad Source\]**: (sola lettura) *[!UICONTROL 3rd party]*.

**[!UICONTROL Display Code]:** URL della risorsa creativa di terze parti. Tutti i parametri [timestamp] e [[timestamp]] vengono sostituiti con i valori effettivi.

**[!UICONTROL Final Display Code]:** URL per la risorsa creativa di terze parti, con le [macro di tracciamento Advertising DSP](/help/dsp/campaign-management/macros.md) inserite, se applicabile.

### [!UICONTROL Basic]: Annunci video

**[!UICONTROL Ad Type]:** (sola lettura) Il tipo di annuncio che stai creando, che corrisponde al tipo di posizionamento a cui l&#39;annuncio può essere allegato.

**[!UICONTROL Ad Name]:** Il nome dell&#39;annuncio. Il titolo della risorsa è utilizzato per impostazione predefinita, ma puoi modificarne il nome.

>[!TIP]
>
> Utilizza un nome facile da trovare quando alleghi l’annuncio a un posizionamento, nella vista Annunci e nei rapporti. Ad esempio, descrivi il tipo di unità e alcuni attributi chiave (ad esempio Anteprima prodotto per vacanze: preroll telefonico da 30 sec&quot;).

**[!UICONTROL Width]| [!UICONTROL Ad Unit Width]:** Larghezza dell&#39;intera unità pubblicitaria. Questa opzione può essere bloccata a seconda del tipo di unità pubblicitaria selezionato.

**[!UICONTROL Height]| [!UICONTROL Ad Unit Height]:** Altezza dell&#39;intera unità pubblicitaria. Questa opzione può essere bloccata a seconda del tipo di unità pubblicitaria selezionato.

**[!UICONTROL Player X]:** La coordinata X per l&#39;unità annuncio. Mantenere l&#39;impostazione predefinita.

**[!UICONTROL Player Y]:** La coordinata Y dell&#39;unità annuncio. Mantenere l&#39;impostazione predefinita.

**[!UICONTROL Player Width]:** la larghezza dell&#39;intera unità pubblicitaria. Questa opzione può essere bloccata a seconda del tipo di unità pubblicitaria selezionato.

È lo stesso del campo **[!UICONTROL Width]**.

**[!UICONTROL Player Height]:** altezza dell&#39;intera unità pubblicitaria. Questa opzione può essere bloccata a seconda del tipo di unità pubblicitaria selezionato.

È lo stesso del campo **[!UICONTROL Height]**.

**[!UICONTROL Show Controls]:** Dove includere i controlli video per l&#39;annuncio: *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]* o *[!UICONTROL None]* (impostazione predefinita).

**[!UICONTROL Preserve Aspect Ratio]:** se mantenere le proporzioni di larghezza e altezza del video (*[!UICONTROL Yes]*) o allungare il video per riempire lo spazio disponibile (*[!UICONTROL No]*).

**[!UICONTROL Close Button Delay]:** (alcuni tipi di annunci) Il numero di secondi per ritardare l&#39;aspetto del pulsante di chiusura.

**[!UICONTROL VAST Tag]:** (annunci che utilizzano solo tag VAST; sola lettura) Il tag VAST di terze parti immesso come risorsa creativa.

**[!UICONTROL Final VAST Tag]:** (annunci che utilizzano solo tag VAST; sola lettura) Il tag VAST di terze parti immesso come risorsa creativa con le [macro di tracciamento Advertising DSP](/help/dsp/campaign-management/macros.md) inserite, se applicabili.

**[!UICONTROL Wmode]:** (alcuni tipi di annunci) Modalità finestra: *[!UICONTROL window]*, *[!UICONTROL transparent]* o *[!UICONTROL opaque]*.

### [!UICONTROL Pixel]

<!-- **[!UICONTROL Pixel]:** -->

{{$include /help/_includes/dsp-ad-pixel.md}}

### [!UICONTROL Sharing]

Obsoleto

>[!MORELIKETHIS]
>
>* [Informazioni Sulla Gestione Degli Annunci](ad-about.md)
>* [Crea un annuncio singolo](ad-create.md)
>* [Elenca i posizionamenti associati a un annuncio](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Specifiche annuncio](ad-specs.md)
>* [Macro DSP](/help/dsp/campaign-management/macros.md)
