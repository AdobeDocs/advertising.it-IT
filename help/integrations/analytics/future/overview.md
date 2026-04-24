---
title: Adobe Advertising integrations with Adobe Analytics
description: Learn about how Adobe Advertising can exchange data with Adobe Analytics and how you can use the data within Search, Social, & Commerce.
feature: Integration with Adobe Analytics
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 0%

---

# Adobe Advertising integrations with Adobe Analytics

You can integrate Adobe Advertising with Analytics in the following ways.

## Exchange data between [!DNL Analytics] and Adobe Advertising

### Pull [!DNL Analytics] data into Adobe Advertising

With [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md),[!DNL Search, Social, & Commerce] and DSP pull in:

* **[!DNL Analytics]segments:**  Metadata, hierarchy data, and unique audience data for all of an advertiser&#39;s or agency&#39;s segments created in [!DNL Analytics] and published to Adobe CX Enterprise.

* **[!DNL Analytics]site engagement metrics**

* **[!DNL Analytics]standard, custom, and reserved metrics**

### Send Adobe Advertising data to [!DNL Analytics]

* **Traffic metrics from Adobe Advertising**

* **Dimensions from Adobe Advertising**

>[!NOTE]
>
>For [!DNL Search, Social, & Commerce], this feature is supported for most ad networks and campaign types. See &quot;Supported Inventory&quot; in the [!DNL Search, Social, & Commerce] Guide for more information.<!-- add link when that's published in ExL -->

### Use [!DNL Analytics] segments to create [!DNL Google Ads] audiences {#audience-manager-google-audiences}

*Inserzionisti con consenso con [!DNL Advertising Search, Social, & Commerce] solo*

<!-- Verify all -->

Within [!DNL Search, Social, & Commerce], you can create [!DNL Google Ads] Google customer match audiences from user IDs using your existing [!DNL Analytics] segments. Sono inclusi i segmenti di Adobe Analytics pubblicati in Adobe CX Enterprise e i segmenti creati con Adobe CX Enterprise [!DNL Audience Library]. Per ulteriori informazioni, consulta &quot;[Creare [!DNL Google Ads] tipi di pubblico corrispondenti ai clienti di [!DNL Adobe] tipi di pubblico](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md).&quot;

[I tipi di pubblico corrispondenti ai clienti degli ID utente](https://support.google.com/google-ads/answer/9199250) funzionano come i tipi di pubblico basati su tag del sito Web, ma un ID non PII viene assegnato ai membri del pubblico univoci per offrire vantaggi distinti rispetto ai tipi di pubblico standard basati su tag dei clienti e dei siti Web.

Per creare gli ID utente necessari, devi utilizzare un tag JavaScript di Adobe Advertising <!-- with a user ID parameter --> sui tuoi siti web. Per ulteriori informazioni, contatta il team del tuo account di Adobe.

![processo di creazione segmento](/help/integrations/assets/ad_search_user_id_pic.png)

Dopo aver creato i tipi di pubblico, puoi utilizzarli nelle campagne [!DNL Google Ads] come [destinazioni o esclusioni a livello di campagna o di gruppo di annunci](#audience-manager-targets).

### Use [!DNL Analytics] segments to target or exclude ads {#analytics-targets}

* (Inserzionisti con consenso con [!DNL Search, Social, & Commerce]) Puoi utilizzare qualsiasi pubblico [!DNL Google Ads] creato [utilizzando [!DNL Analytics] segmenti](#audience-manager-google-audiences) come target o esclusioni a livello di campagna o di gruppo di annunci nelle campagne [!DNL Google Ads].

* (Inserzionisti con DSP) Puoi utilizzare i segmenti [!DNL Analytics] esistenti come destinazioni per i posizionamenti di annunci. Facoltativamente, puoi includere i segmenti in tipi di pubblico riutilizzabili, che puoi utilizzare come target o esclusioni per più posizionamenti.

* (Inserzionisti con Advertising Creative) Puoi utilizzare i segmenti [!DNL Analytics] esistenti come target per creativi specifici nelle esperienze pubblicitarie.
