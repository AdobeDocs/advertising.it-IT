---
title: '[!DNL Microsoft Advertising] impostazioni gruppo di annunci'
description: Fai riferimento alle impostazioni per  [!DNL Microsoft Advertising]  gruppi di annunci.
exl-id: 5d788e5b-ddf3-4f4e-8e8d-98e3235cb187
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '651'
ht-degree: 0%

---

# Impostazioni gruppo di annunci [!DNL Microsoft Advertising]

## [!UICONTROL Adgroup Details]

**[!UICONTROL Ad Group Name]:** Nome di un gruppo di annunci univoco all&#39;interno della campagna. La lunghezza massima è di 128 caratteri.

**[!UICONTROL Status]:** Lo stato di visualizzazione del gruppo di annunci: *Attivo* o *In pausa*. Il valore predefinito per i nuovi gruppi di annunci è *Attivo*.

**[!UICONTROL Ad Language]:** (campagne di ricerca) La lingua di destinazione per gli annunci.

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

## [!UICONTROL Networks]

**[!UICONTROL Networks]:** (Cerca annunci) Come e dove inserire annunci all&#39;interno del gruppo di annunci:

* *[!UICONTROL Only Microsoft Advertising and Yahoo! websites]* (impostazione predefinita): per inserire offerte per annunci nella rete di ricerca.

* *[!UICONTROL Only Microsoft Advertising and Yahoo! syndicated search partners]:* per inviare offerte per annunci su siti partner sindacati.

* *[!UICONTROL Content network]:* Obsoleto

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Content Bid]:** Obsoleto

## [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]:** (gruppi di annunci di pubblico) Indica se:

* *[!UICONTROL Target and Bid]:* Per mostrare annunci solo agli utenti associati ai tipi di pubblico di destinazione che soddisfano anche altri target per il gruppo di annunci.

* *[!UICONTROL Bid Only]:* per mostrare annunci anche a persone non associate a tipi di pubblico di destinazione, purché soddisfino altri target a livello di gruppo di annunci. Tuttavia, puoi aumentare le possibilità che gli annunci vengano mostrati a tipi di pubblico specifici impostando offerte più elevate per tali tipi di pubblico.

<!-- **[!UICONTROL Location Target]:** -->

{{$include /help/_includes/location-targets.md}}

Per i gruppi di annunci [!DNL Microsoft Advertising] nella rete di pubblico, i modificatori di offerte per le destinazioni di posizione non sono ottimizzati nei portfolio standard con l&#39;impostazione &quot;[!UICONTROL Auto-optimize Bid Adjustment Values]&quot;.

**[!UICONTROL Genre]:** (Gruppi di annunci in [!UICONTROL Audience CTV Video] campagne; disponibili in US, CA, BR, MX, UK, DE, ES, FR, IT, AU, MY e TH<!-- Should that go in the campaign sub-type description instead, or is this applicable for this feature only? -->) I generi di destinazione, che determinano gli spettacoli e i canali su cui vengono visualizzati gli annunci:

* *[!UICONTROL All genres]:* (impostazione predefinita) Esegue il targeting di tutti i generi.

* *[!UICONTROL Select From Below List]:* esegue il targeting dei generi selezionati. Seleziona dall&#39;elenco di tutti i generi disponibili.

Il posizionamento degli annunci TV collegata (CTV) dipende dalla qualità video e dalla quantità di offerte. Consulta i [requisiti tecnici per gli annunci CTV](https://help.ads.microsoft.com/#apex/ads/en/60102/0/#TechnicalRequirements).

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

**[!UICONTROL Gender]:** (gruppi di annunci di pubblico; facoltativo) Tipi specifici da includere o escludere come destinazioni: *[!UICONTROL Male]*, *[!UICONTROL Female]* e *[!UICONTROL Unknown]*. Per impostazione predefinita, il targeting viene applicato a tutti i generi. Le esclusioni sostituiscono sempre le inclusioni.

* Per impostare come destinazione tutti i valori, non selezionare alcun valore.

* Per includere un valore, fare clic una volta sul cerchio adiacente in modo che venga visualizzato un segno di spunta blu (![Includi](/help/search-social-commerce/assets/include.png "Includi")). Puoi facoltativamente aumentare o diminuire le offerte di una percentuale specificata per ogni genere target.

* Per escludere un valore, fare clic due volte sul cerchio adiacente in modo che venga visualizzato un segno di spunta rosso (![Escludi](/help/search-social-commerce/assets/exclude.png "Escludi")).

**[!UICONTROL Age]:** (gruppi di annunci di pubblico; facoltativo) Categorie di età specifiche da includere o escludere come destinazioni: *[!UICONTROL 18-24]*, *[!UICONTROL 25-34]*, *[!UICONTROL 35-49]*, *[!UICONTROL 50-64]*, *[!UICONTROL 65+]* e *[!UICONTROL Unknown]*. Per impostazione predefinita, è impostato il targeting per tutte le età. Le esclusioni sostituiscono sempre le inclusioni.

* Per impostare come destinazione tutti i valori, non selezionare alcun valore.

* Per includere un valore, fare clic una volta sul cerchio adiacente in modo che venga visualizzato un segno di spunta blu (![Includi](/help/search-social-commerce/assets/include.png "Includi")). Puoi facoltativamente aumentare o diminuire le offerte di una percentuale specificata per ogni età target.

* Per escludere un valore, fare clic due volte sul cerchio adiacente in modo che venga visualizzato un segno di spunta rosso (![Escludi](/help/search-social-commerce/assets/exclude.png "Escludi")).

**[!UICONTROL Industry]:** (gruppi di annunci di pubblico; facoltativo) Settori specifici da includere o escludere come target. Per impostazione predefinita, tutti i settori sono target. Le esclusioni sostituiscono sempre le inclusioni.

* Per impostare come destinazione tutti i valori, non selezionare alcun valore.

* Per includere un valore, fare clic una volta sul cerchio adiacente in modo che venga visualizzato un segno di spunta blu (![Includi](/help/search-social-commerce/assets/include.png "Includi")). Facoltativamente, puoi aumentare o diminuire le offerte di una percentuale specifica per ogni settore di destinazione.

* Per escludere un valore, fare clic due volte sul cerchio adiacente in modo che venga visualizzato un segno di spunta rosso (![Escludi](/help/search-social-commerce/assets/exclude.png "Escludi")).

**[!UICONTROL Job Function Targets]:** (gruppi di annunci di pubblico; facoltativo) Funzioni processo specifiche da includere o escludere come destinazioni. Per impostazione predefinita, tutte le funzioni lavorative sono impostate come destinazione. Le esclusioni sostituiscono sempre le inclusioni.

* Per impostare come destinazione tutti i valori, non selezionare alcun valore.

* Per includere un valore, fare clic una volta sul cerchio adiacente in modo che venga visualizzato un segno di spunta blu (![Includi](/help/search-social-commerce/assets/include.png "Includi")). Facoltativamente, puoi aumentare o diminuire le offerte di una percentuale specificata per ogni funzione lavorativa target.

* Per escludere un valore, fare clic due volte sul cerchio adiacente in modo che venga visualizzato un segno di spunta rosso (![Escludi](/help/search-social-commerce/assets/exclude.png "Escludi")).

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

<!-- **[!UICONTROL Custom Parameters]:** -->

{{$include /help/_includes/custom-parameters.md}}

**[!UICONTROL Adgroup Frequency Cap Settings]:** (Facoltativo) Il numero di volte in cui un cliente può ricevere annunci dal gruppo di annunci. Immettere un valore e selezionare l&#39;unità di tempo (*[!UICONTROL Hour]*, *[!UICONTROL Day]* o *[!UICONTROL Week]*).

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-microsoft.md}}

## [!UICONTROL Negative Websites]

**[!UICONTROL Negative Websites]:** (solo campagne nella rete di visualizzazione/nativa; facoltativo) Siti nella rete di visualizzazione in cui non si desidera visualizzare gli annunci. Immetti un URL valido, ad esempio www.example.com. Per specificare più stringhe, separarle con virgole o immetterle su righe separate.

Per informazioni sulla disponibilità, vedere la Guida di [!DNL Microsoft Advertising] per &quot;[impedire la visualizzazione di annunci su siti Web specifici](https://help.ads.microsoft.com/#apex/bae/en/14061/0).&quot;

>[!MORELIKETHIS]
>
>* [Gestisci gruppi di annunci](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
