---
title: Integrazioni pubblicitarie di Adobe con Adobe Analytics
description: Scopri come Adobe Advertising può scambiare dati con Adobe Analytics e come utilizzare i dati in Search, Social e Commerce.
feature: Integration with Adobe Analytics
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: def6a3a8d1de1f9f80dee6ecd1a18667afc79fd3
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 0%

---

# Integrazioni pubblicitarie di Adobe con Adobe Analytics

Puoi integrare Adobe Advertising con Analytics nei seguenti modi.

## Dati di Exchange tra [!Aanalisi] e pubblicità Adobe

### Pull [!Aanalisi] Dati in Adobe Advertising

Con [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md),[!DNL Search, Social, & Commerce] e DSP tirare in:

* **[!DNL Analytics]segmenti:**  Metadati, dati gerarchici e dati di pubblico univoci per tutti i segmenti di un inserzionista o di un’agenzia creati in [!DNL Analytics] e pubblicato in Experience Cloud.

* **[!DNL Analytics]metriche di coinvolgimento del sito**

* **[!DNL Analytics]Metriche standard, personalizzate e riservate**

### Invia dati pubblicitari di Adobe a [!Aanalisi]

* **Metriche del traffico da Adobe Advertising**

* **Dimension da Adobe Advertising**

>[!NOTE]
>
>Per [!DNL Search, Social, & Commerce], questa funzione è supportata per la maggior parte delle reti di annunci e dei tipi di campagne. Consulta &quot;Inventario supportato&quot; in [!DNL Search, Social, & Commerce] Guida per ulteriori informazioni.<!-- add link when that's published in ExL -->

### Utilizzo [!DNL Analytics] Segmenti da creare [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*Inserzionisti con consenso con [!DNL Advertising Search, Social, & Commerce] only*

<!-- Verify all -->

Within [!DNL Search, Social, & Commerce], puoi creare [!DNL Google Ads] I tipi di pubblico di corrispondenza dei clienti Google dagli ID utente utilizzano i tipi di pubblico esistenti [!DNL Analytics] segmenti. Ciò include i segmenti Adobe Analytics pubblicati in Adobe Experience Cloud e i segmenti creati utilizzando Adobe Experience Cloud [!DNL Audience Library]. Per ulteriori informazioni, consulta la guida interna al prodotto in [!DNL Search, Social, & Commerce].

[Corrispondenza cliente ai tipi di pubblico dagli ID utente](https://support.google.com/google-ads/answer/9199250) funziona come un pubblico basato su tag del sito web, ma un ID non PII viene assegnato a membri di pubblico univoci per vantaggi distinti rispetto ai tipi di pubblico standard basati sulla corrispondenza del cliente e a quelli basati su tag del sito web.

Per creare gli ID utente necessari, devi utilizzare un tag JavaScript di pubblicità di Adobe <!-- with a user ID parameter -->sui siti web. Per ulteriori informazioni, contatta il team dell’account Adobe.

![processo di creazione dei segmenti](/help/integrations/assets/ad_search_user_id_pic.png)

Una volta creati i tipi di pubblico, puoi utilizzarli in [!DNL Google Ads] campagne come [target o esclusioni a livello di campagna o di gruppo di annunci](#audience-manager-targets).

### Utilizzo [!DNL Analytics] Segmenti in Target o Annunci esclusi {#analytics-targets}

* (Annunci Opted-in con [!DNL Search, Social, & Commerce]) Puoi utilizzare qualsiasi [!DNL Google Ads] tipi di pubblico che erano [creato utilizzando [!DNL Analytics] segmenti](#audience-manager-google-audiences) come target o esclusioni a livello di campagna o di gruppo di annunci nel tuo [!DNL Google Ads] campagne.

* (Inserzionisti con DSP) Puoi utilizzare il tuo esistente [!DNL Analytics] come target per i posizionamenti degli annunci. Facoltativamente, puoi includere i segmenti nei tipi di pubblico riutilizzabili, che puoi utilizzare come target o esclusioni per più posizionamenti.

* (Inserzionisti con Advertising Creative) Puoi utilizzare il tuo esistente [!DNL Analytics] segmenti come target per creativi specifici nelle esperienze pubblicitarie.
