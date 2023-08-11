---
title: Il parametro di tracciamento AMO ID (s_kwcid)
description: Scopri il parametro di tracciamento utilizzato per condividere i dati degli Adobi Advertising con Adobe Analytics.
exl-id: 3f739f1c-3cb7-40d0-86ab-cf66afe6a06f
feature: Search Tracking
source-git-commit: a150a55fd8d97db83cc269c787a1c67d557b7e3a
workflow-type: tm+mt
source-wordcount: '250'
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

Per i formati AMO ID per DSP e Search, Social e Commerce, vedi &quot;[ID Adobe Advertising utilizzati da [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id).&quot;

>[!MORELIKETHIS]
>
>* [Panoramica di [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md){target="_blank"}
>* [ID Adobe Advertising utilizzati da [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id){target="_blank"}
>* [Gestire gli account di rete degli annunci](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)
>* [Impostazioni campagna Baidu](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-baidu.md)
>* [Impostazioni della campagna Google Ads](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md)
>* [Impostazioni della campagna Microsoft Advertising](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-microsoft.md)
>* [Yahoo! Impostazioni campagna Japan Ads](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yahoo-japan.md)
>* [Impostazioni campagna Yandex](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yandex.md)
