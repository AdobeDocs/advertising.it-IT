---
title: Impostazioni degli annunci mobili
description: Consulta le descrizioni delle impostazioni di annunci disponibili per gli annunci mobili.
feature: DSP Ads
exl-id: 45e8da8c-d6a2-4c42-8932-4cf551f6f899
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '616'
ht-degree: 0%

---

# Impostazioni degli annunci mobili

## [!UICONTROL Insert Ad Tag]

*Solo nuovi formati di annunci video per dispositivi mobili*

**[!UICONTROL URL]** o **[!UICONTROL Ad Tag]**: Un tag ad o tag di terze parti VAST che contiene risorse creative e pixel di tracciamento

**[!UICONTROL Ad Title]** o **[!UICONTROL Title]**: Un nome per l’annuncio utilizzato nella [!UICONTROL Ads] visualizza e report.

>[!TIP]
>
> Per verificare la validità di un tag VAST, incollalo in un browser e premi il pulsante **[!UICONTROL Enter]** chiave. Se il tag è valido, verrà visualizzato un file XML che include `<VAST>` vicino alla cima.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]: Annunci display per dispositivi mobili

**[!UICONTROL Ad Type]:** (Sola lettura) Il tipo di annuncio che stai creando, che corrisponde al tipo di posizionamento a cui l’annuncio può essere allegato.

**[!UICONTROL Ad Name]:** Nome dell&#39;annuncio. Il titolo della risorsa viene utilizzato per impostazione predefinita, ma puoi modificarlo.

>[!TIP]
>
> Utilizza un nome che sarà facile trovare quando alleghi l’annuncio a un posizionamento, nella visualizzazione Annunci e nei rapporti. Ad esempio, descrivi il tipo di unità e alcuni attributi chiave (ad esempio, Anteprima del prodotto in vacanza): 300x250 Gamer&quot;).

**\[Origine annuncio\]**: (Sola lettura) *[!UICONTROL 3rd party]*.

**[!UICONTROL Display Code]:** URL della risorsa creativa di terze parti. Qualsiasi [timestamp] e [[timestamp]] verranno sostituiti con valori effettivi.

**[!UICONTROL Final Display Code]:** L’URL della risorsa creativa di terze parti, con l’URL necessario [Macro per il tracciamento DSP pubblicità](/help/dsp/campaign-management/macros.md) se del caso.

### [!UICONTROL Basic]: Annunci video

**[!UICONTROL Ad Type]:** (Sola lettura) Il tipo di annuncio che stai creando, che corrisponde al tipo di posizionamento a cui l’annuncio può essere allegato.

**[!UICONTROL Ad Name]:** Nome dell&#39;annuncio. Il titolo della risorsa viene utilizzato per impostazione predefinita, ma puoi modificarlo.

>[!TIP]
>
> Utilizza un nome che sarà facile trovare quando alleghi l’annuncio a un posizionamento, nella visualizzazione Annunci e nei rapporti. Ad esempio, descrivi il tipo di unità e alcuni attributi chiave (ad esempio, Anteprima del prodotto in vacanza): 30 sec Preroll&quot;).

**[!UICONTROL Width]| [!UICONTROL Ad Unit Width]:** Larghezza dell&#39;intera unità pubblicitaria. Questa opzione può essere bloccata a seconda del tipo di unità pubblicitaria selezionata.

**[!UICONTROL Height]| [!UICONTROL Ad Unit Height]:** Altezza dell&#39;intera unità pubblicitaria. Questa opzione può essere bloccata a seconda del tipo di unità pubblicitaria selezionata.

**[!UICONTROL Player X]:** La coordinata X per l&#39;unità dell&#39;annuncio. Mantieni l’impostazione predefinita.

**[!UICONTROL Player Y]:** La coordinata Y per l&#39;unità dell&#39;annuncio. Mantieni l’impostazione predefinita.

**[!UICONTROL Player Width]:** Larghezza dell&#39;intera unità pubblicitaria. Questa opzione può essere bloccata a seconda del tipo di unità pubblicitaria selezionata.

È lo stesso del **[!UICONTROL Width]** campo .

**[!UICONTROL Player Height]:** Altezza dell&#39;intera unità pubblicitaria. Questa opzione può essere bloccata a seconda del tipo di unità pubblicitaria selezionata.

È lo stesso del **[!UICONTROL Height]** campo .

**[!UICONTROL Show Controls]:** Dove includere i controlli video per l’annuncio: *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]* oppure *[!UICONTROL None]* (impostazione predefinita).

**[!UICONTROL Preserve Aspect Ratio]:** Se mantenere le proporzioni di larghezza e altezza del video (*[!UICONTROL Yes]*) o per allungare il video per riempire lo spazio disponibile (*[!UICONTROL No]*).

**[!UICONTROL Close Button Delay]:** (Alcuni tipi di annuncio) Il numero di secondi necessari per ritardare l&#39;aspetto del pulsante di chiusura.

**[!UICONTROL VAST Tag]:** (Annunci che utilizzano solo tag VAST; di sola lettura) Il tag VAST di terze parti inserito come risorsa creativa.

**[!UICONTROL Final VAST Tag]:** (Annunci che utilizzano solo tag VAST; di sola lettura) Il tag VAST di terze parti inserito come risorsa creativa con il necessario [Macro per il tracciamento DSP pubblicità](/help/dsp/campaign-management/macros.md) se del caso.

**[!UICONTROL Wmode]:** (Alcuni tipi di annunci) La modalità finestra: *[!UICONTROL window]*, *[!UICONTROL transparent]* oppure *[!UICONTROL opaque]*.

### [!UICONTROL Pixel]

Tutti i pixel di tracciamento degli eventi esistenti per il posizionamento vengono automaticamente collegati. Puoi scollegare i pixel esistenti e creare nuovi pixel in base alle tue esigenze di tracciamento per il singolo annuncio.

Le seguenti impostazioni si applicano a ogni pixel creato o modificato.

**[!UICONTROL Integration Event]:** L&#39;evento che attiva il pixel da attivare. Per questo tipo di annuncio, utilizza i pixel che attivano *[!UICONTROL Impression]* o *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Se il pixel è un *[!UICONTROL IMG URL]* (file immagine da 1 pixel), *[!UICONTROL HTML]* oppure *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** L&#39;URL dell&#39;immagine pixel, nel formato appropriato per il [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** Nome del pixel. Utilizza un nome che ti aiuti a identificare facilmente il pixel.

**[!UICONTROL Pixel Provider]:** Provider di pixel: *[!UICONTROL None]*, *[!UICONTROL Nielsen]* oppure *[!UICONTROL Comscore]*.

### [!UICONTROL Sharing]

Obsoleto

>[!MORELIKETHIS]
>
>* [Informazioni sulla gestione degli annunci](ad-about.md)
>* [Creare un singolo annuncio](ad-create.md)
>* [Elencare i posizionamenti associati a un annuncio](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Specifiche degli annunci](ad-specs.md)
>* [Macro DSP](/help/dsp/campaign-management/macros.md)

