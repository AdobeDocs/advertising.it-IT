---
title: Impostazioni annuncio video universale
description: Consulta le descrizioni delle impostazioni disponibili per gli annunci video universali.
feature: DSP Ads
exl-id: 51b7d632-1e73-4726-980b-07ed50447146
source-git-commit: 9d9330847c9356180928337a4a452f35e7024545
workflow-type: tm+mt
source-wordcount: '511'
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

Tutti i pixel di tracciamento degli eventi esistenti per il posizionamento vengono associati automaticamente. Puoi scollegare i pixel esistenti e crearne di nuovi, in base alle tue esigenze di tracciamento per il singolo annuncio. **Suggerimento:** per modificare i pixel di tracciamento di terze parti per più annunci in un posizionamento contemporaneamente utilizzando la visualizzazione [!UICONTROL Ad Tools], vedere &quot;[Allega pixel di tracciamento di terze parti agli annunci in un posizionamento](/help/dsp/campaign-management/ads/ad-pixel-attach-detach.md#attach-pixels-ads).&quot;

Le seguenti impostazioni si applicano a ogni pixel creato o modificato.

**[!UICONTROL Integration Event]:** l&#39;evento che attiva il pixel per l&#39;attivazione. Per questo tipo di annuncio, utilizza i pixel che attivano *[!UICONTROL Impression]* o *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Se il pixel è un *[!UICONTROL IMG URL]* (file immagine 1x1 pixel), *[!UICONTROL HTML]* o *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** URL dell&#39;immagine pixel nel formato appropriato per [!UICONTROL Pixel Type] specificato.

**[!UICONTROL Pixel Name]:** Il nome del pixel. Utilizza un nome che ti consenta di identificare facilmente il pixel.

**[!UICONTROL Pixel Provider]:** Provider pixel: *[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]* o *[!UICONTROL IAS]*.

>[!MORELIKETHIS]
>
>* [Domande frequenti sul video universale](/help/dsp/campaign-management/faq-universal-video.md)
>* [Informazioni Sulla Gestione Degli Annunci](ad-about.md)
>* [Crea un annuncio singolo](ad-create.md)
>* [Elenca i posizionamenti associati a un annuncio](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Specifiche annuncio](ad-specs.md)
>* [Macro DSP](/help/dsp/campaign-management/macros.md)
