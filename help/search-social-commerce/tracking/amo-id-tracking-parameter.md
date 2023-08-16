---
title: Il parametro di tracciamento AMO ID (s_kwcid)
description: Scopri il parametro di tracciamento utilizzato per condividere i dati degli Adobi Advertising con Adobe Analytics.
exl-id: 3f739f1c-3cb7-40d0-86ab-cf66afe6a06f
feature: Search Tracking
source-git-commit: 3c91d0a764397fd72192f5a522ac936176047bc2
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# Il parametro di tracciamento AMO ID (s_kwcid)

*Per gli inserzionisti con solo integrazione Adobi Advertising-Adobe Analytics*

<!-- This should go in the Analytics integration chapter > IDs page, under "AMO IDs" once I've finalized content for DSP clients.  -->

Un Adobe Advertising condivide i dati relativi alle campagne con Adobe Analytics utilizzando il parametro di aggiunta AMO ID, denominato anche `s_kwcid` , costituito da elementi specifici del canale pubblicitario e della rete di annunci.

Il parametro viene aggiunto agli URL di tracciamento in uno dei seguenti modi:

* (Consigliato) La funzione di inserimento lato server è implementata.

   * Clienti DSP: il pixel server aggiunge automaticamente il parametro s_kwcid ai suffissi della pagina di destinazione quando un utente finale visualizza un annuncio con il pixel di Adobe Advertising.

   * Clienti Search, Social e Commerce:

      * Per [!DNL Google Ads] e [!DNL Microsoft® Advertising] account con [!UICONTROL Auto Upload] se l’impostazione è abilitata per l’account o la campagna, il pixel server aggiunge automaticamente il parametro s_kwcid ai suffissi della pagina di destinazione quando un utente finale fa clic su un annuncio con il pixel di Adobe Advertising.

      * Per altre reti pubblicitarie, o [!DNL Google Ads] e [!DNL Microsoft® Advertising] account con [!UICONTROL Auto Upload] Se l’impostazione è disabilitata, aggiungi manualmente il parametro ai parametri di accodamento a livello di account, che lo aggiungono agli URL di base.

* La funzione di inserimento lato server non è implementata:

   * Clienti DSP:

      * Per [!DNL Flashtalking] Aggiungi tag, inserisci manualmente macro aggiuntive per &quot;[Aggiungi [!DNL Analytics for Advertising] Macro per [!DNL Flashtalking] Tag annuncio](/help/integrations/analytics/macros-flashtalking.md).&quot;

      * Per [!DNL Google Campaign Manager 360] Aggiungi tag, inserisci manualmente macro aggiuntive per &quot;[Aggiungi [!DNL Analytics for Advertising] Macro per [!DNL Google Campaign Manager 360] Tag annuncio](/help/integrations/analytics/macros-google-campaign-manager.md).&quot;

  <!--  * For all other ads, XXXX. -->

   * Clienti Search, Social e Commerce:

      * Per ([!DNL Google Ads] e [!DNL Microsoft® Advertising]), aggiungi manualmente il parametro AMO ID ai suffissi della pagina di destinazione.

      * Per gli annunci su tutte le altre reti di annunci, aggiungi manualmente il parametro AMO ID ai parametri di aggiunta a livello di account, che lo aggiungono agli URL di base.

Per implementare la funzione di inserimento lato server o per determinare l’opzione migliore per la tua azienda, rivolgiti al team del tuo account di Adobe.

Per i formati AMO ID per DSP e Search, Social e Commerce, vedi &quot;[ID Adobe Advertising utilizzati da [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id).&quot;

>[!MORELIKETHIS]
>
>* [Panoramica di [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md){target="_blank"}
>* [ID Adobe Advertising utilizzati da [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id){target="_blank"}
>* (Ricerca, Social e Commerce) [Gestire gli account di rete degli annunci](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)
>* (Ricerca, Social e Commerce) [Impostazioni campagna Baidu](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-baidu.md)
>* (Ricerca, Social e Commerce) [Impostazioni della campagna Google Ads](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md)
>* (Ricerca, Social e Commerce) [Impostazioni della campagna Microsoft® Advertising](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-microsoft.md)
>* (Ricerca, Social e Commerce) [Yahoo! Impostazioni campagna Japan Ads](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yahoo-japan.md)
>* (Ricerca, Social e Commerce) [Impostazioni campagna Yandex](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yandex.md)
