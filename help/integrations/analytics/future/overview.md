---
title: Integrazioni di Adobe Advertising con Adobe Analytics
description: Scopri come Adobe Advertising può scambiare dati con Adobe Analytics e come utilizzarli in Search, Social e Commerce.
feature: Integration with Adobe Analytics
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: f2860a4b-f905-4545-bead-1bbc92564592
    internal-label: Advertising integrations
subfeature_v2:
  - id: cfd751d4-ee56-4323-8fd1-dc174b031709
    internal-label: Analytics integration
source-git-commit: 6d95caf72d11c404d866e8d091e1ffa89814ae73
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 0%
---
# Integrazioni di Adobe Advertising con Adobe Analytics

Puoi integrare Adobe Advertising con Analytics nei seguenti modi.

## Scambia dati tra [!DNL Analytics] e Adobe Advertising

### Estrarre dati [!DNL Analytics] in Adobe Advertising

Con [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md),[!DNL Search, Social, & Commerce] e DSP eseguire il pull in:

* **[!DNL Analytics]segmenti:** metadati, dati gerarchici e dati di pubblico univoci per tutti i segmenti dell&#39;inserzionista o dell&#39;agenzia creati in [!DNL Analytics] e pubblicati in Adobe CX Enterprise.

* **[!DNL Analytics]metriche di coinvolgimento sito**

* **[!DNL Analytics]metriche standard, personalizzate e riservate**

### Invia dati Adobe Advertising a [!DNL Analytics]

* **Metriche traffico da Adobe Advertising**

* **Dimensioni da Adobe Advertising**

>[!NOTE]
>
>Per [!DNL Search, Social, & Commerce], questa funzione è supportata per la maggior parte delle reti di annunci e dei tipi di campagne. Per ulteriori informazioni, vedere &quot;Inventario supportato&quot; nella Guida di [!DNL Search, Social, & Commerce].<!-- add link when that's published in ExL -->

### Usa [!DNL Analytics] segmenti per creare [!DNL Google Ads] tipi di pubblico {#audience-manager-google-audiences}

*Inserzionisti con consenso con [!DNL Advertising Search, Social, & Commerce] solo*

<!-- Verify all -->

All&#39;interno di [!DNL Search, Social, & Commerce], puoi creare [!DNL Google Ads] tipi di pubblico in base ai clienti di Google dagli ID utente utilizzando i tuoi segmenti [!DNL Analytics] esistenti. Sono inclusi i segmenti di Adobe Analytics pubblicati in Adobe CX Enterprise e i segmenti creati con Adobe CX Enterprise [!DNL Audience Library]. Per ulteriori informazioni, consulta &quot;[Creare [!DNL Google Ads] tipi di pubblico corrispondenti ai clienti di [!DNL Adobe] tipi di pubblico](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md).&quot;

[I tipi di pubblico corrispondenti ai clienti degli ID utente](https://support.google.com/google-ads/answer/9199250) funzionano come i tipi di pubblico basati su tag del sito Web, ma un ID non PII viene assegnato ai membri del pubblico univoci per offrire vantaggi distinti rispetto ai tipi di pubblico standard basati su tag dei clienti e dei siti Web.

Per creare gli ID utente necessari, devi utilizzare un tag JavaScript di Adobe Advertising <!-- with a user ID parameter --> sui tuoi siti web. Per ulteriori informazioni, contatta il team del tuo account di Adobe.

![processo di creazione segmento](/help/integrations/assets/ad_search_user_id_pic.png)

Dopo aver creato i tipi di pubblico, puoi utilizzarli nelle campagne [!DNL Google Ads] come [destinazioni o esclusioni a livello di campagna o di gruppo di annunci](#audience-manager-targets).

### Usa [!DNL Analytics] segmenti per eseguire il targeting o escludere gli annunci {#analytics-targets}

* (Inserzionisti con consenso con [!DNL Search, Social, & Commerce]) Puoi utilizzare qualsiasi pubblico [!DNL Google Ads] creato [utilizzando [!DNL Analytics] segmenti](#audience-manager-google-audiences) come target o esclusioni a livello di campagna o di gruppo di annunci nelle campagne [!DNL Google Ads].

* (Inserzionisti con DSP) Puoi utilizzare i segmenti [!DNL Analytics] esistenti come destinazioni per i posizionamenti di annunci. Facoltativamente, puoi includere i segmenti in tipi di pubblico riutilizzabili, che puoi utilizzare come target o esclusioni per più posizionamenti.

* (Inserzionisti con Advertising Creative) Puoi utilizzare i segmenti [!DNL Analytics] esistenti come target per creativi specifici nelle esperienze pubblicitarie.
