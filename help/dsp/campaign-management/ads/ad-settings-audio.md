---
title: Impostazioni annuncio audio
description: Consulta le descrizioni delle impostazioni pubblicitarie disponibili per gli annunci audio.
feature: DSP Ads
exl-id: 2fa1143b-6e83-4729-91cd-7a5da357509e
TQID: https://experienceleague.adobe.com/rP0SJspXvqzivctnNqe7b35mbL-ARZlGzC3cLAS-uwA
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: d9510790-d834-436d-8423-8d69cd50464a
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 277
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
>* [Informazioni sulla gestione degli annunci in Advertising DSP](ad-about.md)
>* [Crea un singolo annuncio](ad-create.md)
>* [Elencare i posizionamenti associati a un annuncio](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Specifiche annuncio](ad-specs.md)
>* [Macro di DSP](/help/dsp/campaign-management/macros.md)
