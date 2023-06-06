---
title: "[!DNL Google Ads] impostazioni del gruppo di annunci"
description: Fai riferimento alle impostazioni per [!DNL Google Ads] gruppi di annunci.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 0%

---

# [!DNL Google Ads] impostazioni gruppo di annunci

## [!UICONTROL Adgroup Details]

**[!UICONTROL Ad Group Name]:** Un nome di gruppo di annunci univoco all’interno della campagna. La lunghezza massima è di 255 caratteri a doppio byte.

**[!UICONTROL Status]:** Lo stato di visualizzazione del gruppo di annunci: *Attivo* o *In pausa*. Il valore predefinito per i nuovi gruppi di annunci è *Attivo*.

**[!UICONTROL Ad Group Type]:** (Solo campagne pubblicitarie di ricerca dinamica espanse) Il tipo di gruppo di annunci:

* *[!UICONTROL Search Standard]* (impostazione predefinita): per annunci standard.

* *[!UICONTROL Search Dynamic]:* Per annunci di ricerca dinamica.

**[!UICONTROL Ad Rotation Mode]:** Con quale frequenza [!DNL Google Ads] distribuisce gli annunci attivi in relazione tra loro all’interno del gruppo di annunci:

* *[!UICONTROL Optimize]:* Google Ads favorisce gli annunci che si aspetta di fare meglio di altri annunci nel gruppo di annunci. Questi annunci entrano nell’asta pubblicitaria più spesso e nel tempo viene preferito un singolo annuncio. Ciò potrebbe non essere coerente con gli obiettivi aziendali e di ottimizzazione.

* *[!UICONTROL Rotate forever]:*   Ciascuno degli annunci entra nell’asta un numero più uniforme di volte, il che consente a Search, Social e Commerce di valutare i tuoi annunci non solo sul tasso di click-through, ma anche sulle conversioni.

* *[!UICONTROL Use campaign setting]*(impostazione predefinita per i nuovi gruppi di annunci): utilizza l’impostazione di rotazione degli annunci a livello di campagna esistente. **Nota:** L’impostazione a livello di campagna non è visibile in Search, Social &amp; Commerce.

Se la campagna utilizza una strategia di offerta avanzata (ad esempio [!UICONTROL Target CPA], [!UICONTROL Target ROAS], o [!UICONTROL Enhanced CPC]), quindi [!DNL Google Ads] imposta automaticamente l&#39;opzione su &quot;[!UICONTROL Optimize].&quot;

**[!UICONTROL Custom Bid Level]:** (Campagne mirate solo alla rete di visualizzazione) Procedura: *[!UICONTROL Ad Group]* (impostazione predefinita), *[!UICONTROL Age]*, *[!UICONTROL Gender]*, *[!UICONTROL Interest and List]* (Interessi e remarketing in Google Ads), *[!UICONTROL Keyword]*, *[!UICONTROL Placement]* (sito web), *[!UICONTROL Unknown]*, o *[!UICONTROL Vertical]*.

>[!NOTE]
>
>* Quando fai offerte per parola chiave, crea modelli di tracciamento a livello di parola chiave. Allo stesso modo, quando fai un&#39;offerta per posizionamento, crea modelli di tracciamento a livello di posizionamento. Per tutte le altre dimensioni, crea modelli di tracciamento a livello di annuncio.
>* Quando fai un&#39;offerta per età, genere, interesse ed elenco o verticale per campagne in portfolio, la funzionalità di ottimizzazione non ottimizza le offerte per la dimensione. Inoltre, tutte le attribuzioni vengono applicate al gruppo di annunci.
>* Gli annunci sulla rete di ricerca utilizzano sempre le offerte basate su parole chiave.


## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Target CPA]:** (Campagne con [!UICONTROL Target CPA] offerte; facoltativo) il costo target per acquisizione (CPA) per il gruppo di annunci. Questo valore sostituisce il target a livello di campagna.

**[!UICONTROL Target ROAS]:** (Campagne con [!UICONTROL Target ROAS] offerte; facoltativo) il ritorno previsto sulla spesa pubblicitaria (ROAS) per il gruppo di annunci, in percentuale. Questo valore sostituisce il target a livello di campagna.

## [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]:** (Campagne solo sulla rete di ricerca ed esistenti, di sola lettura) [!DNL Gmail] sulla rete di visualizzazione) Se:

* *[!UICONTROL Target and Bid]:* Per mostrare gli annunci solo agli utenti associati ai tipi di pubblico target che soddisfano anche altri target per il gruppo di annunci.

* *[!UICONTROL Bid Only]:* Mostrare annunci anche a persone non associate a tipi di pubblico di destinazione, purché soddisfino altri target a livello di gruppo di annunci. Tuttavia, puoi aumentare le possibilità che gli annunci vengano mostrati a tipi di pubblico specifici impostando offerte più elevate per tali tipi di pubblico.

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-google.md}}

## [!UICONTROL Negative Websites]

<!-- **[!UICONTROL Negative Websites]:** -->

{{$include /help/_includes/negative-websites-google.md}}

>[!MORELIKETHIS]
>
>* [Gestire i gruppi di annunci](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)

