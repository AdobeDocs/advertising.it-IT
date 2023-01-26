---
title: Impostazioni annuncio pre-roll
description: Consulta le descrizioni delle impostazioni di annunci disponibili per gli annunci pre-scorrimento.
feature: DSP Ads
exl-id: 638d5a3d-3dff-40b6-a3ba-7ab3f08282b9
source-git-commit: 1c13874967ec4ad264e5fa6a5e0dfeb6120f53cc
workflow-type: tm+mt
source-wordcount: '549'
ht-degree: 0%

---

# Impostazioni annuncio pre-roll

## [!UICONTROL Insert Ad Tag]

*Solo nuovi annunci*

**[!UICONTROL URL]:** URL del tag VAST.

**[!UICONTROL Title]:** Un titolo per il file, che si trova nella [!UICONTROL Ads] visualizza e report.

>[!TIP]
>
> Per verificare la validità di un tag VAST, incollalo in un browser e premi il pulsante **[!UICONTROL Enter]** chiave. Se il tag è valido, verrà visualizzato un file XML che include `<VAST>` vicino alla cima.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (Sola lettura) Il tipo di annuncio che stai creando, che corrisponde al tipo di posizionamento a cui l’annuncio può essere allegato.

**[!UICONTROL Ad Name]:** Nome dell&#39;annuncio. Il titolo della risorsa viene utilizzato per impostazione predefinita, ma puoi modificarlo.

>[!TIP]
>
> Utilizza un nome che sarà facile trovare quando alleghi l’annuncio a un posizionamento, nella [!UICONTROL Ads] e nei rapporti. Ad esempio, descrivi il tipo di unità e alcuni attributi chiave (ad esempio, Anteprima del prodotto in vacanza): 30 sec Preroll&quot;).

**[!UICONTROL Width]| [!UICONTROL Ad Unit Width]:** (Solo annunci pre-roll standard e scorrevoli) La larghezza dell’intera unità pubblicitaria. Questa opzione può essere bloccata a seconda del tipo di unità pubblicitaria selezionata.

**[!UICONTROL Height]| [!UICONTROL Ad Unit Height]:** (Solo annunci pre-roll standard e scorrevoli) L&#39;altezza dell&#39;intera unità pubblicitaria. Questa opzione può essere bloccata a seconda del tipo di unità pubblicitaria selezionata.

**[!UICONTROL Player X]:** La coordinata X per l&#39;unità dell&#39;annuncio. Mantieni l’impostazione predefinita.

**[!UICONTROL Player Y]:** La coordinata Y per l&#39;unità dell&#39;annuncio. Mantieni l’impostazione predefinita.

**[!UICONTROL Player Width]:** Larghezza dell&#39;intera unità pubblicitaria. Questa opzione può essere bloccata a seconda del tipo di unità pubblicitaria selezionata.

Questo campo è lo stesso della **[!UICONTROL Width]** campo .

**[!UICONTROL Player Height]:** Altezza dell&#39;intera unità pubblicitaria. Questa opzione può essere bloccata a seconda del tipo di unità pubblicitaria selezionata.

È lo stesso del **[!UICONTROL Height]** campo .

**[!UICONTROL Show Controls]:** Dove includere i controlli video per l’annuncio: *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]* oppure *[!UICONTROL None]* (impostazione predefinita).

**[!UICONTROL Preserve Aspect Ratio]:** Se mantenere le proporzioni di larghezza e altezza del video (*[!UICONTROL Yes]*) o per allungare il video per riempire lo spazio disponibile (*[!UICONTROL No]*).

**[!UICONTROL VAST Tag]:** (Annunci che utilizzano solo tag VAST; sola lettura) Il tag VAST di terze parti immesso come origine dell&#39;annuncio.

**[!UICONTROL Final VAST Tag]:** (Annunci che utilizzano solo tag VAST; di sola lettura) Il tag VAST di terze parti immesso come origine dell&#39;annuncio con il necessario [Macro per il tracciamento DSP pubblicità](/help/dsp/campaign-management/macros.md) se del caso.

**[!UICONTROL Wmode]:** (Solo pre-scorrimento interattivo) Modalità finestra: *[!UICONTROL window]*, *[!UICONTROL transparent]* oppure *[!UICONTROL opaque]*.

**[!UICONTROL Video Format]:** (Solo pre-roll interattivo) Il formato dell&#39;ad player per il potenziale inventario: *[!UICONTROL VPAID]* o *[!UICONTROL VPAID & VAST]*. La visualizzabilità viene sempre misurata per VPAID, ma VPAID e VAST include inventario che non consente la misurazione della visualizzabilità. Considera questa distinzione se le metriche di visualizzabilità sono importanti per la campagna.

**[!UICONTROL Clock Number]**: (solo prerotolo interattivo; utilizzati solo nel Regno Unito; disponibile solo per gli utenti con autorizzazione) Un identificatore univoco utilizzato per garantire la trasmissione dell&#39;annuncio corretto. Se questa impostazione non è applicabile, lasciala vuota.

### [!UICONTROL Pixel]

Tutti i pixel di tracciamento degli eventi esistenti per il posizionamento vengono automaticamente collegati. Puoi scollegare i pixel esistenti e creare nuovi pixel in base alle tue esigenze di tracciamento per il singolo annuncio.

Le seguenti impostazioni si applicano a ogni pixel creato o modificato.

**[!UICONTROL Integration Event]:** L&#39;evento che attiva il pixel da attivare. Per questo tipo di annuncio, utilizza i pixel che attivano *[!UICONTROL Impression]* o *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Se il pixel è un *[!UICONTROL IMG URL]* (file immagine da 1 pixel), *[!UICONTROL HTML]* oppure *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** L&#39;URL dell&#39;immagine pixel, nel formato appropriato per il [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** Nome del pixel. Utilizza un nome che ti aiuti a identificare facilmente il pixel.

**[!UICONTROL Pixel Provider]:** Provider di pixel: *[!UICONTROL None]*, *[!UICONTROL Nielsen]* oppure *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [Informazioni sulla gestione degli annunci](ad-about.md)
>* [Creare un singolo annuncio](ad-create.md)
>* [Elencare i posizionamenti associati a un annuncio](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Specifiche degli annunci](ad-specs.md)
>* [Macro DSP](/help/dsp/campaign-management/macros.md)

