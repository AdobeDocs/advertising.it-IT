---
title: Impostazioni gruppo di annunci [!DNL Google Ads]
description: Fai riferimento alle impostazioni per  [!DNL Google Ads]  gruppi di annunci.
exl-id: def75630-19b9-4676-ad34-5d9041cc3680
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '420'
ht-degree: 0%

---

# Impostazioni gruppo di annunci [!DNL Google Ads]

## [!UICONTROL Adgroup Details]

**[!UICONTROL Ad Group Name]:** Nome di un gruppo di annunci univoco all&#39;interno della campagna. La lunghezza massima è di 255 caratteri a doppio byte.

**[!UICONTROL Status]:** Lo stato di visualizzazione del gruppo di annunci: *Attivo* o *In pausa*. Il valore predefinito per i nuovi gruppi di annunci è *Attivo*.

**[!UICONTROL Ad Group Type]:** (solo campagne pubblicitarie di ricerca dinamica espanse) Tipo di gruppo di annunci:

* *[!UICONTROL Search Standard]* (impostazione predefinita): per annunci standard.

* *[!UICONTROL Search Dynamic]:* per annunci di ricerca dinamica.

**[!UICONTROL Ad Rotation Mode]:** Con quale frequenza [!DNL Google Ads] distribuisce gli annunci attivi tra loro all&#39;interno del gruppo di annunci:

* *[!UICONTROL Optimize]:* Google Ads favorisce gli annunci che prevede di eseguire meglio di altri annunci nel gruppo di annunci. Questi annunci entrano nell’asta pubblicitaria più spesso e nel tempo viene preferito un singolo annuncio. Ciò potrebbe non essere coerente con gli obiettivi aziendali e di ottimizzazione.

* *[!UICONTROL Rotate forever]:*   Ciascuno degli annunci entra nell’asta un numero più uniforme di volte, il che consente a Search, Social e Commerce di valutare i tuoi annunci non solo sul tasso di click-through, ma anche sulle conversioni.

* *[!UICONTROL Use campaign setting]* (impostazione predefinita per i nuovi gruppi di annunci): utilizza l&#39;impostazione di rotazione degli annunci a livello di campagna esistente. **Nota:** l&#39;impostazione a livello di campagna non è visibile in Ricerca, Social e Commerce.

Se la campagna utilizza una strategia di offerta avanzata (ad esempio [!UICONTROL Target CPA], [!UICONTROL Target ROAS] o [!UICONTROL Enhanced CPC]), [!DNL Google Ads] imposta automaticamente l&#39;opzione su &quot;[!UICONTROL Optimize]&quot;.

**[!UICONTROL Custom Bid Level]:** (campagne mirate solo alla rete di visualizzazione) Come fare offerte: da *[!UICONTROL Ad Group]* (impostazione predefinita), *[!UICONTROL Age]*, *[!UICONTROL Gender]*, *[!UICONTROL Interest and List]* (interessi e remarketing in Google Ads), *[!UICONTROL Keyword]*, *[!UICONTROL Placement]* (sito Web), *[!UICONTROL Unknown]* o *[!UICONTROL Vertical]*.

>[!NOTE]
>
>* Quando fai offerte per parola chiave, crea modelli di tracciamento a livello di parola chiave. Allo stesso modo, quando fai un&#39;offerta per posizionamento, crea modelli di tracciamento a livello di posizionamento. Per tutte le altre dimensioni, crea modelli di tracciamento a livello di annuncio.
>* Quando fai un&#39;offerta per età, genere, interesse ed elenco o verticale per campagne in portfolio, la funzionalità di ottimizzazione non ottimizza le offerte per la dimensione. Inoltre, tutte le attribuzioni vengono applicate al gruppo di annunci.
>* Gli annunci sulla rete di ricerca utilizzano sempre le offerte basate su parole chiave.

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Target CPA]:** (campagne con [!UICONTROL Target CPA] offerte; facoltativo) Il costo target per acquisizione (CPA) per il gruppo di annunci. Questo valore sostituisce il target a livello di campagna.

**[!UICONTROL Target ROAS]:** (campagne con [!UICONTROL Target ROAS] offerte; facoltativo) Il ROAS (ritorno sugli annunci) di destinazione per il gruppo di annunci, in percentuale. Questo valore sostituisce il target a livello di campagna.

## [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]:** (campagne solo nella rete di ricerca e campagne [!DNL Gmail] esistenti di sola lettura nella rete di visualizzazione) Se:

* *[!UICONTROL Target and Bid]:* Per mostrare annunci solo agli utenti associati ai tipi di pubblico di destinazione che soddisfano anche altri target per il gruppo di annunci.

* *[!UICONTROL Bid Only]:* per mostrare annunci anche a persone non associate a tipi di pubblico di destinazione, purché soddisfino altri target a livello di gruppo di annunci. Tuttavia, puoi aumentare le possibilità che gli annunci vengano mostrati a tipi di pubblico specifici impostando offerte più elevate per tali tipi di pubblico.

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
>* [Gestisci gruppi di annunci](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
