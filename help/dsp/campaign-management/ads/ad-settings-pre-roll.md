---
title: Impostazioni annuncio pre-roll
description: Consulta le descrizioni delle impostazioni pubblicitarie disponibili per gli annunci pre-roll.
feature: DSP Ads
exl-id: d0ba4346-13ae-405c-92b6-a0c32dd09d0a
source-git-commit: f521cf26d9d3945bdf1abe4577bb37d732432c87
workflow-type: tm+mt
source-wordcount: '549'
ht-degree: 0%

---

# Impostazioni annuncio pre-roll

## [!UICONTROL Insert Ad Tag]

*Solo nuovi annunci*

**[!UICONTROL URL]:** L’URL del tag VAST.

**[!UICONTROL Title]:** Un titolo per il file, che si trova nel [!UICONTROL Ads] visualizzazione e rapporti.

>[!TIP]
>
> Per verificare la validità di un tag VAST, incollalo in un browser e premi **[!UICONTROL Enter]** chiave. Se il tag è valido, verrà visualizzato un file XML che include `<VAST>` vicino alla cima.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (Sola lettura) Il tipo di annuncio che stai creando, che corrisponde al tipo di posizionamento a cui l’annuncio può essere allegato.

**[!UICONTROL Ad Name]:** Il nome dell’annuncio. Il titolo della risorsa è utilizzato per impostazione predefinita, ma puoi modificarne il nome.

>[!TIP]
>
> Utilizza un nome facile da trovare quando alleghi l’annuncio a un posizionamento, nella [!UICONTROL Ads] e nei rapporti. Ad esempio, descrivi il tipo di unità e alcuni attributi chiave (come Anteprima prodotto per vacanze: preroll 30 sec&quot;).

**[!UICONTROL Width]| [!UICONTROL Ad Unit Width]:** (Solo annunci pre-roll standard e saltabili) Larghezza dell’intera unità pubblicitaria. Questa opzione può essere bloccata a seconda del tipo di unità pubblicitaria selezionato.

**[!UICONTROL Height]| [!UICONTROL Ad Unit Height]:** (Solo annunci pre-roll standard e saltabili) Altezza dell’intera unità pubblicitaria. Questa opzione può essere bloccata a seconda del tipo di unità pubblicitaria selezionato.

**[!UICONTROL Player X]:** La coordinata X dell’unità pubblicitaria. Mantenere l&#39;impostazione predefinita.

**[!UICONTROL Player Y]:** La coordinata Y dell’unità pubblicitaria. Mantenere l&#39;impostazione predefinita.

**[!UICONTROL Player Width]:** Larghezza dell’intera unità pubblicitaria. Questa opzione può essere bloccata a seconda del tipo di unità pubblicitaria selezionato.

Questo campo è uguale al campo **[!UICONTROL Width]** campo.

**[!UICONTROL Player Height]:** Altezza dell’intera unità pubblicitaria. Questa opzione può essere bloccata a seconda del tipo di unità pubblicitaria selezionato.

È lo stesso della **[!UICONTROL Height]** campo.

**[!UICONTROL Show Controls]:** Dove includere i controlli video per l’annuncio: *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]*, o *[!UICONTROL None]* (impostazione predefinita).

**[!UICONTROL Preserve Aspect Ratio]:** Specifica se mantenere le proporzioni di larghezza e altezza del video (*[!UICONTROL Yes]*) o per estendere il video in modo da riempire lo spazio disponibile (*[!UICONTROL No]*).

**[!UICONTROL VAST Tag]:** (Annunci che utilizzano solo i tag VAST; sola lettura) Il tag VAST di terze parti inserito come origine dell’annuncio.

**[!UICONTROL Final VAST Tag]:** (Annunci che utilizzano solo i tag VAST; sola lettura) Il tag VAST di terze parti inserito come origine dell’annuncio con il necessario [Pubblicità delle macro di tracciamento DSP](/help/dsp/campaign-management/macros.md) se del caso.

**[!UICONTROL Wmode]:** (Solo pre-roll interattivo) La modalità finestra: *[!UICONTROL window]*, *[!UICONTROL transparent]*, o *[!UICONTROL opaque]*.

**[!UICONTROL Video Format]:** (Solo pre-roll interattivo) Il formato del lettore dell’annuncio per il potenziale inventario: *[!UICONTROL VPAID]* o *[!UICONTROL VPAID & VAST]*. La visualizzabilità viene sempre misurata per VPAID, ma VPAID e VAST includono un inventario che non consente la misurazione della visualizzabilità. Considera questa distinzione se le metriche di visualizzabilità sono importanti per la campagna.

**[!UICONTROL Clock Number]**: (Solo pre-roll interattivo; utilizzato solo nel Regno Unito; disponibile solo per gli utenti con autorizzazione) Un identificatore univoco utilizzato per garantire che l’annuncio corretto venga trasmesso. Se questa impostazione non è applicabile, lasciarla vuota.

### [!UICONTROL Pixel]

Tutti i pixel di tracciamento degli eventi esistenti per il posizionamento vengono associati automaticamente. Puoi scollegare i pixel esistenti e crearne di nuovi, in base alle tue esigenze di tracciamento per il singolo annuncio.

Le seguenti impostazioni si applicano a ogni pixel creato o modificato.

**[!UICONTROL Integration Event]:** L’evento che attiva il pixel da attivare. Per questo tipo di annuncio, utilizza i pixel che vengono attivati sul *[!UICONTROL Impression]* o *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Se il pixel è un *[!UICONTROL IMG URL]* (file di immagine 1x1 pixel), *[!UICONTROL HTML]*, o *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** L&#39;URL dell&#39;immagine pixel nel formato appropriato per il [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** Il nome del pixel. Utilizza un nome che ti consenta di identificare facilmente il pixel.

**[!UICONTROL Pixel Provider]:** Il provider pixel: *[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]*, o *[!UICONTROL IAS]*.

>[!MORELIKETHIS]
>
>* [Informazioni sulla gestione degli annunci](ad-about.md)
>* [Creare un singolo annuncio](ad-create.md)
>* [Elencare i posizionamenti associati a un annuncio](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Specifiche annuncio](ad-specs.md)
>* [Macro per DSP](/help/dsp/campaign-management/macros.md)
