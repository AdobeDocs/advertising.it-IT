---
title: Impostazioni annuncio audio
description: Consulta le descrizioni delle impostazioni pubblicitarie disponibili per gli annunci audio.
feature: DSP Ads
exl-id: 2fa1143b-6e83-4729-91cd-7a5da357509e
source-git-commit: 9d9330847c9356180928337a4a452f35e7024545
workflow-type: tm+mt
source-wordcount: '406'
ht-degree: 0%

---

# Impostazioni annuncio audio

## [!UICONTROL Insert Ad Tag]

*Solo nuovi annunci*

**[!UICONTROL URL]**: URL del tag VAST.

**[!UICONTROL Title]**: nome per il file, utilizzato nella visualizzazione e nei report [!UICONTROL Ads].

>[!TIP]
>
> Per verificare la validità di un tag VAST, incollarlo in un browser e premere il tasto **[!UICONTROL Enter]**. Se il tag è valido, verrà visualizzato un file XML che include `<VAST>` nella parte superiore.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (sola lettura) Il tipo di annuncio che stai creando, che corrisponde al tipo di posizionamento a cui l&#39;annuncio può essere allegato. Il valore predefinito è *[!UICONTROL Audio]*.

**[!UICONTROL Ad Name]:** Il nome dell&#39;annuncio. Il titolo della risorsa è utilizzato per impostazione predefinita, ma puoi modificarne il nome.

>[!TIP]
>
> Utilizzare un nome facilmente individuabile quando si allega l&#39;annuncio a un posizionamento, nella visualizzazione [!UICONTROL Ads] e nei report. Ad esempio, descrivi il tipo di unità e alcuni attributi chiave (come Anteprima prodotto per vacanze: 30 sec Audio&quot;).

**[!UICONTROL Ad Duration]:** La lunghezza del file audio. Viene impostato automaticamente come [!UICONTROL 15] o [!UICONTROL 30], a seconda dell&#39;unità pubblicitaria selezionata.

Questo campo può essere visualizzato o meno, a seconda delle autorizzazioni dell’account.

**[!UICONTROL VAST Tag]:** (annunci che utilizzano solo tag VAST) URL per un&#39;origine annuncio di terze parti. Assicurati che il tag VAST includa solo file multimediali audio.

**[!UICONTROL Final VAST Tag]:** (solo annunci con tag VAST) URL per l&#39;origine annunci di terze parti con le [macro di tracciamento Advertising DSP](/help/dsp/campaign-management/macros.md) inserite, se applicabili.

**[!UICONTROL Select Rate]:** (solo utenti con autorizzazione) Tariffa prenegoziata fatturata tramite Adobe o una delle tariffe negoziate e fatturate tramite il fornitore. Per aggiungere una tariffa, contatta il team del tuo account Adobe.

### [!UICONTROL Pixel]

Tutti i pixel di tracciamento degli eventi esistenti per il posizionamento vengono associati automaticamente. Puoi scollegare i pixel esistenti e crearne di nuovi, in base alle tue esigenze di tracciamento per il singolo annuncio. **Suggerimento:** per modificare i pixel di tracciamento di terze parti per più annunci in un posizionamento contemporaneamente utilizzando la visualizzazione [!UICONTROL Ad Tools], vedere &quot;[Allega pixel di tracciamento di terze parti agli annunci in un posizionamento](/help/dsp/campaign-management/ads/ad-pixel-attach-detach.md#attach-pixels-ads).&quot;

Le seguenti impostazioni si applicano a ogni pixel creato o modificato.

**[!UICONTROL Integration Event]:** l&#39;evento che attiva il pixel per l&#39;attivazione. Per questo tipo di annuncio, utilizza i pixel che attivano *[!UICONTROL Impression]* o *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Se il pixel è un *[!UICONTROL IMG URL]* (file immagine 1x1 pixel), *[!UICONTROL HTML]* o *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** URL dell&#39;immagine pixel nel formato appropriato per il tipo di pixel specificato.

**[!UICONTROL Pixel Name]:** Il nome del pixel. Utilizza un nome che ti consenta di identificare facilmente il pixel.

**[!UICONTROL Pixel Provider]:** Provider pixel:*[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]* o *[!UICONTROL IAS]*.

>[!MORELIKETHIS]
>
>* [Informazioni Sulla Gestione Degli Annunci](ad-about.md)
>* [Crea un annuncio singolo](ad-create.md)
>* [Elenca i posizionamenti associati a un annuncio](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Specifiche annuncio](ad-specs.md)
>* [Macro DSP](/help/dsp/campaign-management/macros.md)
