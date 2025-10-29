---
title: Impostazioni annuncio video universale
description: Consulta le descrizioni delle impostazioni disponibili per gli annunci video universali.
feature: DSP Ads
exl-id: 51b7d632-1e73-4726-980b-07ed50447146
source-git-commit: 863bf7a4d8304e42b7004742de59b9e1a09f81b7
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# Impostazioni annuncio video universale

>[!NOTE]
>
>Gli annunci video universali possono essere collegati solo ai posizionamenti video universali.

## [!UICONTROL Insert Ad Tag]

*Solo nuovi annunci*

**[!UICONTROL URL]:** L&#39;URL del tag VAST.

**[!UICONTROL Title]:** Titolo per il file, che si trova nella visualizzazione e nei report [!UICONTROL Ads].

>[!TIP]
>
> Per verificare la validità di un tag VAST, incollarlo in un browser e premere il tasto **[!UICONTROL Enter]**. Se il tag è valido, verrà visualizzato un file XML che include `<VAST>` nella parte superiore.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (sola lettura) Il tipo di annuncio che stai creando, che corrisponde al tipo di posizionamento a cui l&#39;annuncio può essere allegato.

**[!UICONTROL Ad Name]:** Il nome dell&#39;annuncio. Il titolo della risorsa è utilizzato per impostazione predefinita, ma puoi modificarne il nome.

>[!TIP]
>
> Utilizzare un nome facilmente individuabile quando si allega l&#39;annuncio a un posizionamento, nella visualizzazione [!UICONTROL Ads] e nei report. Ad esempio, descrivi il tipo di unità e alcuni attributi chiave (come Anteprima prodotto per vacanze: Video universale da 30 sec&quot;).

**[!UICONTROL Show Controls]:** Dove includere i controlli video per l&#39;annuncio: *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]* o *[!UICONTROL None]* (impostazione predefinita).

**[!UICONTROL Preserve Aspect Ratio]:** se mantenere le proporzioni di larghezza e altezza del video (*[!UICONTROL Yes]*) o allungare il video per riempire lo spazio disponibile (*[!UICONTROL No]*).

**[!UICONTROL VAST Tag]:** (annunci che utilizzano solo tag VAST; sola lettura) Il tag VAST di terze parti immesso come origine dell&#39;annuncio.

**[!UICONTROL Final VAST Tag]:** (annunci che utilizzano solo tag VAST; sola lettura) Il tag VAST di terze parti immesso come origine dell&#39;annuncio con le [macro di tracciamento Advertising DSP](/help/dsp/campaign-management/macros.md) inserite, se applicabili.

**[!UICONTROL Wmode]:** Modalità finestra: *[!UICONTROL window]*, *[!UICONTROL transparent]* o *[!UICONTROL opaque]*. Se questa impostazione non è applicabile, lasciarla vuota.

**[!UICONTROL Video Format]:** Il formato del lettore di annunci per il potenziale inventario: *[!UICONTROL VPAID]*, *[!UICONTROL VPAID & VAST]* o *[!UICONTROL VAST]*. La visualizzabilità viene sempre misurata per [!UICONTROL VPAID], ma [!UICONTROL VPAID & VAST] include un inventario che non consente la misurazione della visualizzabilità. Considera questa distinzione se le metriche di visualizzabilità sono importanti per la campagna.

Utilizzare [!UICONTROL VAST], che non consente la misurazione della visualizzabilità, quando si esegue il targeting di un televisore connesso o di un inventario che richiede solo il formato VAST (in genere da fonti di fornitura come Google Ad Manager, Appnexus, SpotX e Freewheel). Utilizza questa opzione anche per l’inventario precedentemente compatibile con i posizionamenti/annunci Pre-roll standard (VAST) o Phone + Tablet Standard (VAST).

**[!UICONTROL Clock Number]**: (utilizzato solo nel Regno Unito; disponibile solo per gli utenti autorizzati) Identificatore univoco utilizzato per garantire che l&#39;annuncio corretto venga trasmesso. Se questa impostazione non è applicabile, lasciarla vuota.

### [!UICONTROL Pixel]

<!-- **[!UICONTROL Pixel]:** -->

{{$include /help/_includes/dsp-ad-pixel.md}}

>[!MORELIKETHIS]
>
>* [Domande frequenti sul video universale](/help/dsp/campaign-management/faq-universal-video.md)
>* [Informazioni Sulla Gestione Degli Annunci](ad-about.md)
>* [Crea un annuncio singolo](ad-create.md)
>* [Elenca i posizionamenti associati a un annuncio](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Specifiche annuncio](ad-specs.md)
>* [Macro DSP](/help/dsp/campaign-management/macros.md)
