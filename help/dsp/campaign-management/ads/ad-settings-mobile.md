---
title: Impostazioni annuncio mobile
description: Consulta le descrizioni delle impostazioni pubblicitarie disponibili per gli annunci per dispositivi mobili.
feature: DSP Ads
exl-id: 45e8da8c-d6a2-4c42-8932-4cf551f6f899
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '616'
ht-degree: 0%

---

# Impostazioni annuncio mobile

## [!UICONTROL Insert Ad Tag]

*Solo nuovi formati di annunci video per dispositivi mobili*

**[!UICONTROL URL]** o **[!UICONTROL Ad Tag]**: tag di annunci VAST o di altri produttori contenenti risorse creative e pixel di tracciamento

**[!UICONTROL Ad Title]** o **[!UICONTROL Title]**: nome per l’annuncio utilizzato nella [!UICONTROL Ads] visualizzazione e rapporti.

>[!TIP]
>
> Per verificare la validità di un tag VAST, incollalo in un browser e premi **[!UICONTROL Enter]** chiave. Se il tag è valido, verrà visualizzato un file XML che include `<VAST>` vicino alla cima.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]: annunci display per dispositivi mobili

**[!UICONTROL Ad Type]:** (Sola lettura) Il tipo di annuncio che stai creando, che corrisponde al tipo di posizionamento a cui l’annuncio può essere allegato.

**[!UICONTROL Ad Name]:** Il nome dell’annuncio. Il titolo della risorsa è utilizzato per impostazione predefinita, ma puoi modificarne il nome.

>[!TIP]
>
> Utilizza un nome facile da trovare quando alleghi l’annuncio a un posizionamento, nella vista Annunci e nei rapporti. Ad esempio, descrivi il tipo di unità e alcuni attributi chiave (come Anteprima prodotto per vacanze: 300x250 Gamer&quot;).

**\[Origine annuncio\]**: (sola lettura) *[!UICONTROL 3rd party]*.

**[!UICONTROL Display Code]:** URL della risorsa creativa di terze parti. Qualsiasi [timestamp] e [[timestamp]] verranno sostituiti con i valori effettivi.

**[!UICONTROL Final Display Code]:** L’URL della risorsa creativa di terze parti, con il necessario [Pubblicità delle macro di tracciamento DSP](/help/dsp/campaign-management/macros.md) se del caso.

### [!UICONTROL Basic]: Annunci video

**[!UICONTROL Ad Type]:** (Sola lettura) Il tipo di annuncio che stai creando, che corrisponde al tipo di posizionamento a cui l’annuncio può essere allegato.

**[!UICONTROL Ad Name]:** Il nome dell’annuncio. Il titolo della risorsa è utilizzato per impostazione predefinita, ma puoi modificarne il nome.

>[!TIP]
>
> Utilizza un nome facile da trovare quando alleghi l’annuncio a un posizionamento, nella vista Annunci e nei rapporti. Ad esempio, descrivi il tipo di unità e alcuni attributi chiave (ad esempio Anteprima prodotto per vacanze: preroll telefonico da 30 sec&quot;).

**[!UICONTROL Width]| [!UICONTROL Ad Unit Width]:** Larghezza dell’intera unità pubblicitaria. Questa opzione può essere bloccata a seconda del tipo di unità pubblicitaria selezionato.

**[!UICONTROL Height]| [!UICONTROL Ad Unit Height]:** Altezza dell’intera unità pubblicitaria. Questa opzione può essere bloccata a seconda del tipo di unità pubblicitaria selezionato.

**[!UICONTROL Player X]:** La coordinata X dell’unità pubblicitaria. Mantenere l&#39;impostazione predefinita.

**[!UICONTROL Player Y]:** La coordinata Y dell’unità pubblicitaria. Mantenere l&#39;impostazione predefinita.

**[!UICONTROL Player Width]:** Larghezza dell’intera unità pubblicitaria. Questa opzione può essere bloccata a seconda del tipo di unità pubblicitaria selezionato.

È lo stesso della **[!UICONTROL Width]** campo.

**[!UICONTROL Player Height]:** Altezza dell’intera unità pubblicitaria. Questa opzione può essere bloccata a seconda del tipo di unità pubblicitaria selezionato.

È lo stesso della **[!UICONTROL Height]** campo.

**[!UICONTROL Show Controls]:** Dove includere i controlli video per l’annuncio: *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]*, o *[!UICONTROL None]* (impostazione predefinita).

**[!UICONTROL Preserve Aspect Ratio]:** Specifica se mantenere le proporzioni di larghezza e altezza del video (*[!UICONTROL Yes]*) o per estendere il video in modo da riempire lo spazio disponibile (*[!UICONTROL No]*).

**[!UICONTROL Close Button Delay]:** (Alcuni tipi di annunci) Il numero di secondi per ritardare l’aspetto del pulsante di chiusura.

**[!UICONTROL VAST Tag]:** (Annunci che utilizzano solo i tag VAST; sola lettura) Il tag VAST di terze parti inserito come risorsa creativa.

**[!UICONTROL Final VAST Tag]:** (Annunci che utilizzano solo i tag VAST; sola lettura) Il tag VAST di terze parti inserito come risorsa creativa con il necessario [Pubblicità delle macro di tracciamento DSP](/help/dsp/campaign-management/macros.md) se del caso.

**[!UICONTROL Wmode]:** (Alcuni tipi di annunci) La modalità finestra: *[!UICONTROL window]*, *[!UICONTROL transparent]*, o *[!UICONTROL opaque]*.

### [!UICONTROL Pixel]

Tutti i pixel di tracciamento degli eventi esistenti per il posizionamento vengono associati automaticamente. Puoi scollegare i pixel esistenti e crearne di nuovi, in base alle tue esigenze di tracciamento per il singolo annuncio.

Le seguenti impostazioni si applicano a ogni pixel creato o modificato.

**[!UICONTROL Integration Event]:** L’evento che attiva il pixel da attivare. Per questo tipo di annuncio, utilizza i pixel che vengono attivati sul *[!UICONTROL Impression]* o *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Se il pixel è un *[!UICONTROL IMG URL]* (file di immagine 1x1 pixel), *[!UICONTROL HTML]*, o *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** L&#39;URL dell&#39;immagine pixel nel formato appropriato per il [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** Il nome del pixel. Utilizza un nome che ti consenta di identificare facilmente il pixel.

**[!UICONTROL Pixel Provider]:** Il provider pixel: *[!UICONTROL None]*, *[!UICONTROL Nielsen]*, o *[!UICONTROL Comscore]*.

### [!UICONTROL Sharing]

Obsoleto

>[!MORELIKETHIS]
>
>* [Informazioni sulla gestione degli annunci](ad-about.md)
>* [Creare un singolo annuncio](ad-create.md)
>* [Elencare i posizionamenti associati a un annuncio](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Specifiche annuncio](ad-specs.md)
>* [Macro per DSP](/help/dsp/campaign-management/macros.md)

