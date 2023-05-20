---
title: Impostazioni annuncio video universale
description: Consulta le descrizioni delle impostazioni disponibili per gli annunci video universali.
feature: DSP Ads
exl-id: 51b7d632-1e73-4726-980b-07ed50447146
source-git-commit: 0c9e9c8d2a3444c623568d25262421be53c0c846
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---

# Impostazioni annuncio video universale

*Funzione open beta*

>[!NOTE]
>
>Gli annunci video universali possono essere collegati solo ai posizionamenti video universali.

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
> Utilizza un nome facile da trovare quando alleghi l’annuncio a un posizionamento, nella [!UICONTROL Ads] e nei rapporti. Ad esempio, descrivi il tipo di unità e alcuni attributi chiave (come Anteprima prodotto per vacanze: Video universale da 30 sec&quot;).

**[!UICONTROL Show Controls]:** Dove includere i controlli video per l’annuncio: *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]*, o *[!UICONTROL None]* (impostazione predefinita).

**[!UICONTROL Preserve Aspect Ratio]:** Specifica se mantenere le proporzioni di larghezza e altezza del video (*[!UICONTROL Yes]*) o per estendere il video in modo da riempire lo spazio disponibile (*[!UICONTROL No]*).

**[!UICONTROL VAST Tag]:** (Annunci che utilizzano solo i tag VAST; sola lettura) Il tag VAST di terze parti inserito come origine dell’annuncio.

**[!UICONTROL Final VAST Tag]:** (Annunci che utilizzano solo i tag VAST; sola lettura) Il tag VAST di terze parti inserito come origine dell’annuncio con il necessario [Pubblicità delle macro di tracciamento DSP](/help/dsp/campaign-management/macros.md) se del caso.

**[!UICONTROL Wmode]:** Modalità finestra: *[!UICONTROL window]*, *[!UICONTROL transparent]*, o *[!UICONTROL opaque]*. Se questa impostazione non è applicabile, lasciarla vuota.

**[!UICONTROL Video Format]:** Il formato del lettore dell’annuncio per il potenziale inventario: *[!UICONTROL VPAID]*, *[!UICONTROL VPAID & VAST]*, o *[!UICONTROL VAST]*. La visibilità viene sempre misurata per [!UICONTROL VPAID], ma [!UICONTROL VPAID & VAST] include un inventario che non consente la misurazione della visualizzabilità. Considera questa distinzione se le metriche di visualizzabilità sono importanti per la campagna.

Utilizzare [!UICONTROL VAST], che non consente la misurazione della visualizzabilità, quando si esegue il targeting di un televisore collegato o di un inventario che richiede esclusivamente il formato VAST (in genere da fonti di fornitura come Google Ad Manager, Appnexus, SpotX e Freewheel). Utilizza questa opzione anche per l’inventario precedentemente compatibile con i posizionamenti/annunci Pre-roll standard (VAST) o Phone + Tablet Standard (VAST).

**[!UICONTROL Clock Number]**: (Utilizzato solo nel Regno Unito; disponibile solo per gli utenti autorizzati) Un identificatore univoco utilizzato per garantire che l’annuncio corretto venga trasmesso. Se questa impostazione non è applicabile, lasciarla vuota.

### [!UICONTROL Pixel]

Tutti i pixel di tracciamento degli eventi esistenti per il posizionamento vengono associati automaticamente. Puoi scollegare i pixel esistenti e crearne di nuovi, in base alle tue esigenze di tracciamento per il singolo annuncio.

Le seguenti impostazioni si applicano a ogni pixel creato o modificato.

**[!UICONTROL Integration Event]:** L’evento che attiva il pixel da attivare. Per questo tipo di annuncio, utilizza i pixel che vengono attivati sul *[!UICONTROL Impression]* o *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Se il pixel è un *[!UICONTROL IMG URL]* (file di immagine 1x1 pixel), *[!UICONTROL HTML]*, o *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** L&#39;URL dell&#39;immagine pixel nel formato appropriato per il [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** Il nome del pixel. Utilizza un nome che ti consenta di identificare facilmente il pixel.

**[!UICONTROL Pixel Provider]:** Il provider pixel: *[!UICONTROL None]*, *[!UICONTROL Nielsen]*, o *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [Domande frequenti sui video universali](/help/dsp/campaign-management/faq-universal-video.md)
>* [Informazioni sulla gestione degli annunci](ad-about.md)
>* [Creare un singolo annuncio](ad-create.md)
>* [Elencare i posizionamenti associati a un annuncio](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Specifiche annuncio](ad-specs.md)
>* [Macro per DSP](/help/dsp/campaign-management/macros.md)

