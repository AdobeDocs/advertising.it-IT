---
title: Integrazioni di Adobe Advertising con Adobe Analytics
description: Scopri come Adobe Advertising può scambiare dati con Adobe Analytics e come utilizzarli in Search, Social & Commerce.
feature: Integration with Adobe Analytics
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: 06996ee9eb635fe204c0c3938e6937e8871c8a90
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Integrazioni di Adobe Advertising con Adobe Analytics

È possibile integrare Adobe Advertising con Analytics nei seguenti modi.

## Scambia dati tra [!DNL Analytics] e pubblicità Adobe

### Pull [!DNL Analytics] Dati nella pubblicità Adobe

Con [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md),[!DNL Search, Social, & Commerce] e DSP interviene:

* **[!DNL Analytics]segmenti:**  Metadati, dati gerarchici e dati di pubblico univoci per tutti i segmenti dell’inserzionista o agenzia creati in [!DNL Analytics] e pubblicato su Experience Cloud.

* **[!DNL Analytics]metriche di coinvolgimento del sito**

* **[!DNL Analytics]metriche standard, personalizzate e riservate**

### Inviare dati pubblicitari di Adobi a [!DNL Analytics]

* **Metriche di traffico da Adobe Advertising**

* **Dimension dalla pubblicità Adobe**

>[!NOTE]
>
>Per [!DNL Search, Social, & Commerce], questa funzione è supportata per la maggior parte delle reti di annunci e dei tipi di campagne. Consulta &quot;Inventario supportato&quot; in [!DNL Search, Social, & Commerce] per ulteriori informazioni.<!-- add link when that's published in ExL -->

### Utilizzare [!DNL Analytics] Segmenti da creare [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*Inserzionisti con consenso con [!DNL Advertising Search, Social, & Commerce] solo*

<!-- Verify all -->

Entro [!DNL Search, Social, & Commerce], è possibile creare [!DNL Google Ads] I clienti di Google abbinano i tipi di pubblico degli ID utente utilizzando il tuo [!DNL Analytics] segmenti. Sono inclusi i segmenti di Adobe Analytics pubblicati in Adobe Experience Cloud e i segmenti creati utilizzando Adobe Experience Cloud [!DNL Audience Library]. Per ulteriori informazioni, consulta la guida interna al prodotto all’interno di [!DNL Search, Social, & Commerce].

[I clienti abbinano i tipi di pubblico dagli ID utente](https://support.google.com/google-ads/answer/9199250) funziona come un pubblico basato su tag del sito web, ma un ID non PII viene assegnato a membri del pubblico univoci per offrire vantaggi distinti rispetto ai tipi di pubblico standard basati su tag del cliente e del sito web.

Per creare gli ID utente necessari, devi utilizzare un tag JavaScript di Adobe Advertising <!-- with a user ID parameter -->sui tuoi siti web. Per ulteriori informazioni, contatta il team del tuo account di Adobe.

![processo di creazione del segmento](/help/integrations/assets/ad_search_user_id_pic.png)

Una volta creati i tipi di pubblico, puoi utilizzarli in [!DNL Google Ads] campagne come [target o esclusioni a livello di campagna o di gruppo di annunci](#audience-manager-targets).

### Utilizzare [!DNL Analytics] Segmenti per Target o annunci esclusi {#analytics-targets}

* (inserzionisti con consenso con [!DNL Search, Social, & Commerce]) È possibile utilizzare qualsiasi [!DNL Google Ads] tipi di pubblico che erano [creato con [!DNL Analytics] segmenti](#audience-manager-google-audiences) come target o esclusioni a livello di campagna o di gruppo di annunci nel tuo [!DNL Google Ads] campagne.

* (Inserzionisti con DSP) Puoi utilizzare il tuo [!DNL Analytics] segmenti come destinazioni per i posizionamenti di annunci. Facoltativamente, puoi includere i segmenti in tipi di pubblico riutilizzabili, che puoi utilizzare come target o esclusioni per più posizionamenti.

* (Inserzionisti con Advertising Creative) Puoi utilizzare il tuo [!DNL Analytics] segmenti come target per creativi specifici nelle esperienze pubblicitarie.
