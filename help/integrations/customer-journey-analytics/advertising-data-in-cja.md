---
title: Metriche e dimensioni di Adobe Advertising in Customer Journey Analytics
description: Fai riferimento alle metriche e alle dimensioni di Adobe Advertising disponibili in Customer Journey Analytics.
feature: Integration with Adobe Customer Journey Analytics
exl-id: 97c89e03-ab15-4906-96fc-6bb77ea0cd7c
source-git-commit: 3ab2e38f6a2f70c03504363575b13dc0dc730282
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 0%

---

# Metriche e dimensioni di Adobe Advertising in Customer Journey Analytics

*Inserzionisti con una sola integrazione Adobe Advertising-Customer Journey Analytics*

*funzionalità Beta*

Adobe Advertising passa metriche e dimensioni del traffico a [!DNL Customer Journey Analytics] al giorno. [!DNL Web SDK] acquisisce i click-through e i view-through di Adobe Advertising in tempo reale e li trasmette a Customer Journey Analytics.

## Metriche del traffico di Adobe Advertising

<!-- Verify column names -->

Nella tabella seguente:

* &quot;Nome campo XDM&quot; è il nome del campo in Adobe Experience Platform.

* &quot;Nome visualizzato campo XDM&quot; indica il nome visualizzato in Customer Journey Analytics.

| Nome campo Adobe Advertising | Nome campo XDM | Nome visualizzato campo XDM | Source |
|------------------------------|----------------|------------------------|--------|
| Data | Data | Tutti | |
| AMO ID | skwcid | ID ADOBE ADVERTISING | Tutti |
| Impression AMO | adobe_advertising_impressions | Impression di Adobe Advertising | Tutti |
| Clic AMO | adobe_advertising_clicks | Clic su Adobe Advertising | Tutti |
| Costo AMO | adobe_advertising_cost | Costo Adobe Advertising | Tutti |
| Codice valuta | valuta | Valuta | Tutti |
| Visualizzazioni AMO | adobe_advertising_views | Visualizzazioni di Adobe Advertising | Ad Cloud DSP |
| Visualizzazioni AMO completate al 25% | adobe_advertising_views_25_pct | Visualizzazioni Adobe Advertising 25% Complete | Ad Cloud DSP |
| Visualizzazioni AMO completate al 50% | adobe_advertising_views_50_pct | Visualizzazioni Adobe Advertising 50% complete | Ad Cloud DSP |
| Visualizzazioni AMO 75% completato | adobe_advertising_views_75_pct | Visualizzazioni Adobe Advertising 75% completato | Ad Cloud DSP |
| Visualizzazioni AMO completate al 100% | adobe_advertising_views_100_pct | Visualizzazioni Adobe Advertising 100% complete | Ad Cloud DSP |
| Minuti AMO visualizzati | adobe_advertising_minutes_viewed | Minuti Adobe Advertising visualizzati | Ad Cloud DSP |
| Impression visualizzabili AMO | adobe_advertising_viewable_impressions | Impression visualizzabili in Adobe Advertising | Ad Cloud DSP |
| Impression AMO non visualizzabili | adobe_advertising_not_viewable_impressions | Impression non visualizzabili in Adobe Advertising | Ad Cloud DSP |
| Impression misurabili AMO | adobe_advertising_measurement_impressions | Impression misurabili di Adobe Advertising | Ad Cloud DSP |

<!--
| Adobe Advertising Landing Page Views | adobe_advertising_landing_page_views | Adobe Advertising Landing Page Views | Meta Only |
| Adobe Advertising App Events | adobe_advertising_app_events | Adobe Advertising App Events | Meta Only |
| Adobe Advertising Engagements | adobe_advertising_engagements | Adobe Advertising Engagements | Meta Only |
| Adobe Advertising Ad Platform Conversions | adobe_advertising_ad_platform_conversions | Adobe Advertising Ad Platform Conversions | Meta Only |
| Adobe Advertising App Installs | adobe_advertising_app_installs | Adobe Advertising App Installs | Meta Only |
| Adobe Advertising Ad Platform Conversion Value | adobe_advertising_ad_platform_conversion_value | Adobe Advertising Ad Platform Conversion Value | Meta Only |
| Adobe Advertising Ad Platform Leads | adobe_advertising_ad_platform_leads | Adobe Advertising Ad Platform Leads | Meta Only |
| Adobe Advertising Page Like | adobe_advertising_page_like | Adobe Advertising Page Like | Meta Only |
| Adobe Advertising Phone Calls | adobe_advertising_phone_calls | Adobe Advertising Phone Calls | Meta Only |
| Adobe Advertising Messages | adobe_advertising_messages | Adobe Advertising Messages | Meta Only |
-->

## Dimensioni Adobe Advertising

Nella tabella seguente:

* &quot;Nome campo XDM&quot; è il nome del campo in Adobe Experience Platform.

* &quot;Nome visualizzato campo XDM&quot; indica il nome visualizzato in Customer Journey Analytics.

| Nome campo Adobe Advertising | Nome campo XDM | Nome visualizzato campo XDM | Source |
|------------------------------|----------------|------------------------|--------|
| Chiave | skwcid | ID ADOBE ADVERTISING |  |
| Piattaforma annuncio | adobe_advertising_ad_platform | Adobe Advertising Ad Platform |  |
| Account | adobe_advertising_account | Account Adobe Advertising |  |
| Campagna | adobe_advertising_campaign | Campagna Adobe Advertising |  |
| Gruppo di annunci | adobe_advertising_ad_group | Adobe Advertising Ad Group |  |
| Parola chiave | adobe_advertising_keyword | Parola chiave Adobe Advertising |  |
| Annuncio | adobe_advertising_ad | Adobe Advertising Ad |  |
| Posizionamento | adobe_advertising_placement | Posizionamento Adobe Advertising |  |
| Tipo di corrispondenza | adobe_advertising_match_type | Tipo di corrispondenza Adobe Advertising |  |
| Titolo annuncio | adobe_advertising_ad_title | Titolo annuncio Adobe Advertising |  |
| Descrizione annuncio | adobe_advertising_ad_description | Descrizione annuncio Adobe Advertising |  |
| URL di destinazione dell’annuncio | adobe_advertising_ad_destination_url | URL di destinazione dell’annuncio Adobe Advertising |  |
| URL di visualizzazione annuncio | adobe_advertising_ad_display_url | URL di visualizzazione dell’annuncio Adobe Advertising |  |
| Dispositivo | adobe_advertising_device | Dispositivo Adobe Advertising |  |
| Keyword MatchType | adobe_advertising_keyword_matchtype | Adobe Advertising Keyword MatchType |  |
| Rete | adobe_advertising_network | Rete Adobe Advertising |  |
| Tipo di annuncio | adobe_advertising_ad_type | Tipo di annuncio Adobe Advertising |  |
| Destinazione prodotto | adobe_advertising_product_target | Target di prodotto Adobe Advertising |  |
| Tipo di destinazione | adobe_advertising_landing_type | Tipo di destinazione Adobe Advertising |  |
| Ottimizzazione | adobe_advertising_optimization | Ottimizzazione Adobe Advertising |  |

>[!MORELIKETHIS]
>
>* [Panoramica](overview.md)
>* [Prerequisiti](prerequisites.md)
>* [ID Adobe Advertising utilizzati da [!DNL Customer Journey Analytics]](ids.md)
>* [Imposta raccolta dati, trasferimento dati e reporting](set-up.md)
