---
title: Il parametro di tracciamento AMO ID (s_kwcid)
description: Scopri il parametro di tracciamento utilizzato per condividere i dati degli Adobi Advertising con Adobe Analytics.
exl-id: 3f739f1c-3cb7-40d0-86ab-cf66afe6a06f
feature: Search Tracking
source-git-commit: 47cb00bc456601ef943c37de14a2047220f756f1
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 0%

---

# Il parametro di tracciamento AMO ID (s_kwcid)

*Per gli inserzionisti con solo integrazione Adobi Advertising-Adobe Analytics*

<!-- This should go in the Analytics integration chapter > IDs page, under "AMO IDs."  But I'll need to update with when/where to add the code for DSP clients. -->

Un Adobe Advertising condivide i dati relativi alle campagne con Adobe Analytics utilizzando il parametro di aggiunta AMO ID, denominato anche `s_kwcid` , costituito da elementi specifici del canale pubblicitario e della rete di annunci.

<!-- add everything below to IDs page -->

Il parametro viene aggiunto agli URL di tracciamento in uno dei seguenti modi:

* (Consigliato) La funzione di inserimento lato server è implementata.

  Per [!DNL Google Ads] e [!DNL Microsoft Advertising] account con [!UICONTROL Auto Upload] se l’impostazione è abilitata per l’account o la campagna, il pixel server aggiunge automaticamente il parametro AMO ID ai suffissi della pagina di destinazione quando un utente finale fa clic su un annuncio <!-- click a search ad or views a display ad --> con il pixel Adobe Advertising.

  Per altre reti pubblicitarie, o [!DNL Google Ads] e [!DNL Microsoft Advertising] account con [!UICONTROL Auto Upload] Se l’impostazione è disabilitata, aggiungi manualmente il parametro AMO ID ai parametri di aggiunta a livello di account, che lo aggiungono agli URL di base.

* <!-- (Search, Social, & Commerce only) -->La funzione di inserimento lato server non è implementata e devi aggiungere manualmente il parametro AMO ID al ([!DNL Google Ads] e [!DNL Microsoft Advertising]) i suffissi della pagina di destinazione o (altre reti di annunci) i parametri di aggiunta a livello di account.

Per implementare la funzione di inserimento lato server o per determinare l’opzione migliore per la tua azienda, rivolgiti al team del tuo account di Adobe.

## Formato AMO ID per annunci pubblicitari DSP

`s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}`

dove:

* `AC` indica il canale di visualizzazione.

* `{TM_AD_ID}` è la chiave alfanumerica dell’annuncio.

* `{TM_PLACEMENT_ID}` è la chiave alfanumerica di posizionamento.

## Formati AMO ID per annunci Search, Social e Commerce

I parametri variano in base alla rete di annunci, ma i seguenti parametri sono comuni a tutti:

* `AL` indica il canale di ricerca. <!-- what about social/Facebook, and display ads on Google (like Gmail, YouTube)? -->

* `{userid}` è un ID utente univoco assegnato all’inserzionista.

* `{sid}` è sostituito dall’ID numerico dell’account di rete dell’inserzionista: *3* per [!DNL Google Ads], *10* per [!DNL Microsoft Advertising], *45* per [!DNL Meta], *86* per [!DNL Yahoo! Display Network], *87* per [!DNL Naver], *88* per [!DNL Baidu], *90* per [!DNL Yandex], *94* per [!DNL Yahoo! Japan Ads], *105* per [!DNL Yahoo Native] (obsoleto), oppure *106* per [!DNL Pinterest] (obsoleto).

### [!DNL Baidu]

`s_kwcid=AL!{userid}!{sid}!{creative}!{placement}!{keywordid}`

### [!DNL Google Ads]

Tra cui campagne di acquisto tramite [!DNL Google Merchant Center].

* Account che utilizzano il formato AMO ID più recente, che supporta il reporting a livello di campagna e gruppo di annunci per campagne, bozze ed esperimenti con prestazione massima:

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

* Tutti gli altri account:

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

>[!NOTE]
>
>* Per gli annunci per ricerca dinamica: {keyword} viene popolato con il targeting automatico.
>* Quando generi il tracciamento per [!DNL Google] annunci commerciali, un parametro ID prodotto, `{adwords_producttargetid}`, viene inserito prima del parametro della parola chiave. Il parametro ID prodotto non viene visualizzato nel [!DNL Google Ads] parametri di tracciamento a livello di account e di campagna.
>* Per utilizzare il codice di tracciamento AMO ID più recente, vedi &quot;[Aggiornamento del codice di tracciamento AMO ID per un [!DNL Google Ads] account](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md).&quot; <!-- Update terminology there too. -->

<!--

### [!DNL Meta]

`s_kwcid=AL!{userid}!{sid}!{{ad.id}}!{{campaign.id}}!{{adset.id}}`

where:

* `{{ad.id}}` is the unique numeric ID for the ad/creative.

* `{{campaign.id}}` is the unique ID for the campaign.

* `{{adset.id}}` is the unique ID for the ad set.

-->

### [!DNL Microsoft Advertising]

* Campagne di ricerca:

  `s_kwcid=AL!{userid}!{sid}!{AdId}!{OrderItemId}`

* Campagne commerciali (utilizzando [!DNL Microsoft Merchant Center]):

  `s_kwcid=AL!{userid}!{sid}!{AdId}!{CriterionId}`

* Campagne di Audience Network:

  `s_kwcid=AL!{userid}!{sid}!{AdId}`

### [!DNL Yahoo! Japan Ads]

`s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{network}!{keyword}`

### [!DNL Yandex]

`s_kwcid=AL!{userid}!{sid}!{ad_id}!{source_type}!!!{phrase_id}`

>[!MORELIKETHIS]
>
>* [Panoramica di [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md){target="_blank"}
>* [Gestire gli account di rete degli annunci](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)
>* [Impostazioni campagna Baidu](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-baidu.md)
>* [Impostazioni della campagna Google Ads](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md)
>* [Impostazioni della campagna Microsoft Advertising](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-microsoft.md)
>* [Yahoo! Impostazioni campagna Japan Ads](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yahoo-japan.md)
>* [Impostazioni campagna Yandex](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yandex.md)
