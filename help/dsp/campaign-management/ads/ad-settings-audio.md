---
title: Impostazioni annuncio audio
description: Consulta le descrizioni delle impostazioni pubblicitarie disponibili per gli annunci audio.
feature: DSP Ads
exl-id: 2fa1143b-6e83-4729-91cd-7a5da357509e
source-git-commit: 863bf7a4d8304e42b7004742de59b9e1a09f81b7
workflow-type: tm+mt
source-wordcount: '274'
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

<!-- **[!UICONTROL Pixel]:** -->

{{$include /help/_includes/dsp-ad-pixel.md}}

>[!MORELIKETHIS]
>
>* [Informazioni Sulla Gestione Degli Annunci](ad-about.md)
>* [Crea un annuncio singolo](ad-create.md)
>* [Elenca i posizionamenti associati a un annuncio](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Specifiche annuncio](ad-specs.md)
>* [Macro DSP](/help/dsp/campaign-management/macros.md)
