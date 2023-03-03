---
title: Impostazioni annuncio audio
description: Consulta le descrizioni delle impostazioni pubblicitarie disponibili per gli annunci audio.
feature: DSP Ads
exl-id: 2fa1143b-6e83-4729-91cd-7a5da357509e
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 0%

---

# Impostazioni annuncio audio

## [!UICONTROL Insert Ad Tag]

*Solo nuovi annunci*

**[!UICONTROL URL]**: URL del tag VAST.

**[!UICONTROL Title]**: nome del file, che verrà utilizzato nel [!UICONTROL Ads] visualizzazione e rapporti.

>[!TIP]
>
> Per verificare la validità di un tag VAST, incollalo in un browser e premi **[!UICONTROL Enter]** chiave. Se il tag è valido, verrà visualizzato un file XML che include `<VAST>` vicino alla cima.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (Sola lettura) Il tipo di annuncio che stai creando, che corrisponde al tipo di posizionamento a cui l’annuncio può essere allegato. Il valore predefinito è *[!UICONTROL Audio]*.

**[!UICONTROL Ad Name]:** Il nome dell’annuncio. Il titolo della risorsa è utilizzato per impostazione predefinita, ma puoi modificarne il nome.

>[!TIP]
>
> Utilizza un nome facile da trovare quando alleghi l’annuncio a un posizionamento, nella [!UICONTROL Ads] e nei rapporti. Ad esempio, descrivi il tipo di unità e alcuni attributi chiave (come Anteprima prodotto per vacanze: 30 sec Audio&quot;).

**[!UICONTROL Ad Duration]:** La lunghezza del file audio. Viene impostato automaticamente come [!UICONTROL 15] o [!UICONTROL 30], a seconda dell’unità pubblicitaria selezionata.

Questo campo può essere visualizzato o meno, a seconda delle autorizzazioni dell’account.

**[!UICONTROL VAST Tag]:** (Annunci che utilizzano solo tag VAST) URL per un’origine annuncio di terze parti. Assicurati che il tag VAST includa solo file multimediali audio.

**[!UICONTROL Final VAST Tag]:** (Solo per annunci con tag VAST) L’URL per l’origine dell’annuncio di terze parti con il necessario [Pubblicità delle macro di tracciamento DSP](/help/dsp/campaign-management/macros.md) se del caso.

**[!UICONTROL Select Rate]:** (Solo per utenti autorizzati) Tariffa prenegoziata fatturata tramite Adobe o una delle tariffe negoziate e fatturate tramite il fornitore. Per aggiungere una tariffa, contatta il team del tuo account Adobe.

### Pixel

Tutti i pixel di tracciamento degli eventi esistenti per il posizionamento vengono associati automaticamente. Puoi scollegare i pixel esistenti e crearne di nuovi, in base alle tue esigenze di tracciamento per il singolo annuncio.

Le seguenti impostazioni si applicano a ogni pixel creato o modificato.

**[!UICONTROL Integration Event]:** L’evento che attiva il pixel da attivare. Per questo tipo di annuncio, utilizza i pixel che vengono attivati sul *[!UICONTROL Impression]* o *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Se il pixel è un *[!UICONTROL IMG UR]L* (file di immagine 1x1 pixel), *[!UICONTROL HTML]*, o *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** URL dell&#39;immagine pixel nel formato appropriato per il tipo di pixel specificato.

**[!UICONTROL Pixel Name]:** Il nome del pixel. Utilizza un nome che ti consenta di identificare facilmente il pixel.

**[!UICONTROL Pixel Provider]:** Il provider pixel: *[!UICONTROL None]*, *[!UICONTROL Nielsen]*, o *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [Informazioni sulla gestione degli annunci](ad-about.md)
>* [Creare un singolo annuncio](ad-create.md)
>* [Elencare i posizionamenti associati a un annuncio](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Specifiche annuncio](ad-specs.md)
>* [Macro per DSP](/help/dsp/campaign-management/macros.md)

