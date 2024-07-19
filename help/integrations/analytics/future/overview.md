---
title: Integrazioni Adobe Advertising con Adobe Analytics
description: Scopri come Adobe Advertising può scambiare dati con Adobe Analytics e come utilizzarli in Search, Social e Commerce.
feature: Integration with Adobe Analytics
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: 78f69587771d9e72eb137f1e0866d782ed5c4d01
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# Integrazioni Adobe Advertising con Adobe Analytics

È possibile integrare Adobe Advertising con Analytics nei seguenti modi.

## Scambia dati tra [!DNL Analytics] e Adobe Advertising

### Estrai dati [!DNL Analytics] in Adobe Advertising

Con [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md),[!DNL Search, Social, & Commerce] e DSP eseguire il pull in:

* **[!DNL Analytics]segmenti:** metadati, dati gerarchici e dati di pubblico univoci per tutti i segmenti dell&#39;inserzionista o dell&#39;agenzia creati in [!DNL Analytics] e pubblicati in Experience Cloud.

* **[!DNL Analytics]metriche di coinvolgimento sito**

* **[!DNL Analytics]metriche standard, personalizzate e riservate**

### Invia dati Adobe Advertising a [!DNL Analytics]

* **Metriche traffico da Adobe Advertising**

* **Dimension dall&#39;Adobe Advertising**

>[!NOTE]
>
>Per [!DNL Search, Social, & Commerce], questa funzione è supportata per la maggior parte delle reti di annunci e dei tipi di campagne. Per ulteriori informazioni, vedere &quot;Inventario supportato&quot; nella Guida di [!DNL Search, Social, & Commerce].<!-- add link when that's published in ExL -->

### Usa [!DNL Analytics] segmenti per creare [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*Inserzionisti con consenso con [!DNL Advertising Search, Social, & Commerce] solo*

<!-- Verify all -->

All&#39;interno di [!DNL Search, Social, & Commerce], puoi creare [!DNL Google Ads] tipi di pubblico in base ai clienti di Google dagli ID utente utilizzando i tuoi segmenti [!DNL Analytics] esistenti. Sono inclusi i segmenti di Adobe Analytics pubblicati in Adobe Experience Cloud e i segmenti creati con Adobe Experience Cloud [!DNL Audience Library]. Per ulteriori informazioni, consulta &quot;[Creare [!DNL Google Ads] tipi di pubblico corrispondenti ai clienti di [!DNL Adobe] tipi di pubblico](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md).&quot;

[I tipi di pubblico corrispondenti ai clienti degli ID utente](https://support.google.com/google-ads/answer/9199250) funzionano come i tipi di pubblico basati su tag del sito Web, ma un ID non PII viene assegnato ai membri del pubblico univoci per offrire vantaggi distinti rispetto ai tipi di pubblico standard basati su tag dei clienti e dei siti Web.

Per creare gli ID utente necessari, è necessario utilizzare un tag JavaScript di Adobe Advertising <!-- with a user ID parameter --> sui siti Web. Per ulteriori informazioni, contatta il team del tuo account di Adobe.

![processo di creazione segmento](/help/integrations/assets/ad_search_user_id_pic.png)

Dopo aver creato i tipi di pubblico, puoi utilizzarli nelle campagne [!DNL Google Ads] come [destinazioni o esclusioni a livello di campagna o di gruppo di annunci](#audience-manager-targets).

### Usa [!DNL Analytics] segmenti per eseguire il targeting o escludere annunci {#analytics-targets}

* (Inserzionisti con consenso con [!DNL Search, Social, & Commerce]) Puoi utilizzare qualsiasi pubblico [!DNL Google Ads] creato [utilizzando [!DNL Analytics] segmenti](#audience-manager-google-audiences) come target o esclusioni a livello di campagna o di gruppo di annunci nelle campagne [!DNL Google Ads].

* (Inserzionisti con DSP) Puoi utilizzare i segmenti [!DNL Analytics] esistenti come destinazioni per i posizionamenti di annunci. Facoltativamente, puoi includere i segmenti in tipi di pubblico riutilizzabili, che puoi utilizzare come target o esclusioni per più posizionamenti.

* (Inserzionisti con Advertising Creative) Puoi utilizzare i segmenti [!DNL Analytics] esistenti come target per creativi specifici nelle esperienze pubblicitarie.
