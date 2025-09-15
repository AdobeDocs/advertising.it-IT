---
title: Novità
description: Scopri gli aggiornamenti alle integrazioni tra Adobe Advertising e altri prodotti e servizi in Adobe Experience Cloud.
cloud: Experience Cloud
product: advertising cloud
index: true
exl-id: e5874077-d2a8-43bb-ad4e-55547442c8a4
source-git-commit: db3e843ecb5ec7a21dca4d15ce2a98448b32f307
workflow-type: tm+mt
source-wordcount: '827'
ht-degree: 0%

---

# Novità

Le seguenti funzioni sono nuove o modificate di recente.

| Data | Funzionalità | Descrizione | Per Ulteriori Informazioni |
| ---- | ------- | ----------- | -------------------- |
| 8 settembre 2025 | Integrazione con Customer Journey Analytics | (funzionalità Beta) Gli inserzionisti con Customer Journey Analytics ma non con [!DNL Analytics for Advertising] possono ora scambiare dati in modalità nativa tra Adobe Advertising e Customer Journey Analytics utilizzando [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=it). | Vedi &quot;[Panoramica](/help/integrations/customer-journey-analytics/overview.md).&quot; |
| 26 marzo 2025 | [!DNL Adobe Analytics for Advertising] | (Inserzionisti con account Search, Social e Commerce; [!DNL Microsoft Advertising] e [!DNL Adobe Analytics for Advertising]) Per gli account con l’opzione di tracciamento [!UICONTROL Auto Upload], il formato del parametro AMO ID nei suffissi della pagina di destinazione per tutti i tipi di campagna è stato aggiornato al formato più recente. In precedenza, le campagne con prestazione massima per la maggior parte degli account venivano migrate al nuovo formato.<br><br>Per gli account senza l&#39;opzione di tracciamento [!UICONTROL Auto Upload] che non sono già stati migrati al nuovo formato, è tuttavia necessario aggiornare manualmente ogni suffisso di pagina di destinazione per includere il nuovo formato AMO ID.<br><br>Formato corrente: `s_kwcid=AL!{userid}!10!{AdId}!!!!{OrderItemId}!!{CampaignId}!{AdGroupId}` | Consulta &quot;[Panoramica di [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)&quot; e dei [formati AMO ID](/help/integrations/analytics/ids.md#amo-id-formats).&quot; |
| 13 novembre 2024 | [!DNL Analytics for Advertising] | (Inserzionisti con [!DNL Analytics for Advertising] e Adobe Customer Journey Analytics) Se utilizzi variabili riservate per acquisire gli AMO ID e gli EF ID, puoi prepararti per una futura integrazione tra Adobe Advertising e Adobe Customer Journey Analytics copiando al più presto le variabili riservate per l’AMO ID e l’EF ID nello standard [!DNL eVars]. In questo modo sarà possibile raccogliere i dati storici per gli AMO ID e gli EF ID non appena si completa l’attività e i dati storici saranno disponibili per utilizzi futuri. Il team del tuo account Adobe ti informerà se utilizzi variabili riservate e se devi completare questa attività. | Consulta &quot;[Raccogliere dati storici per gli ID AMO e gli ID EF da utilizzare in Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).&quot; |
| Rilasciato il 29 ottobre 2024 | [!DNL Adobe Analytics for Advertising] | (Inserzionisti con [!DNL Adobe Analytics for Advertising] e [!DNL Microsoft Advertising] campagne con prestazione massima) I dati a livello di gruppo di risorse per le campagne con prestazione massima sono ora disponibili in Adobe Analytics quando si implementa un nuovo parametro AMO ID ([!DNL s_kwcid]) negli URL di tracciamento per le campagne con prestazione massima, che non includono annunci e parole chiave. Il tracciamento della maggior parte degli account con campagne di prestazione massima è già stato migrato al nuovo formato. Per gli account con campagne con prestazione massima senza l’opzione di tracciamento [!UICONTROL Auto Upload] che non sono già stati migrati al nuovo formato, tuttavia, è necessario aggiornare manualmente ogni suffisso di pagina di destinazione per includere il nuovo formato AMO ID.<br><br>I dati di Adobe Analytics per le campagne con prestazione massima sono disponibili anche in Search, Social e Commerce. | Consulta il nuovo [formato AMO ID](/help/integrations/analytics/ids.md#amo-id-formats) e [quando e come aggiungere il parametro agli URL di tracciamento](/help/integrations/analytics/ids.md#amo-id-implement). |
| 16 dicembre 2023 | Aiuto | Un nuovo documento spiega come impostare test A/B in [!DNL Target] per il traffico click-through da annunci in Search, Social e Commerce, nonché suggerimenti su come misurare e visualizzare i test in [!DNL Analytics]. | Consulta &quot;[Configurare i test A/B in Adobe Target per Search, Social e Commerce Ads](/help/integrations/target/ab-tests-search.md).&quot; |
| 8 agosto 2023 | [!DNL Analytics for Advertising] | Alcune metriche degli eventi di successo di [!DNL Analytics], tra cui le metriche di conversione standard, personalizzate e riservate e le metriche del traffico, sono automaticamente disponibili in DSP e in Search, Social e Commerce. Ora puoi anche configurare le metriche di successo personalizzate in base ai tuoi [!DNL Analytics] [!DNL eVars] e [!DNL props] esistenti incanalando i dati di livello [!DNL eVar] e [!DNL prop] in un evento di successo personalizzato. | Consulta &quot;[Creare metriche di conversione da Adobe Analytics [!DNL eVars] e [!DNL Props]](/help/integrations/analytics/conversion-metrics-from-evars.md).&quot; |
| 13 luglio 2023 | Generazione rapporti | (Utenti DSP con [!DNL Analytics for Advertising]) Le conversioni view-through per i posizionamenti CTV (Connection TV) sono ora incluse nei dati di conversione disponibili in Adobe Analytics. | Vedere la sezione su &quot;Esempi di utilizzo dell&#39;integrazione&quot; in &quot;[Panoramica di [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md#integration-examples).&quot; |
| novembre 2022 | Aiuto | Un nuovo documento spiega come implementare la condivisione dei segnali di click-through e view-through tra Advertising DSP e Adobe Target, impostare un&#39;attività di test A/B in [!DNL Target] per gli annunci DSP e configurare Adobe Analytics Analysis Workspace per visualizzare i dati di test. | Consulta &quot;[Configurare i test A/B in Adobe Target per Advertising DSP Ads](/help/integrations/target/ab-tests-dsp.md).&quot; |
| 17 agosto 2022 | Aiuto | Un nuovo capitolo spiega tutti i modi in cui Adobe Advertising è integrato con Adobe Audience Manager. | Consulta il capitolo su &quot;Integrazione con Adobe Audience Manager&quot;, inclusa una panoramica di &quot;[Integrazioni Adobe Advertising con Adobe Audience Manager](/help/integrations/audience-manager/overview.md)&quot;. |
| 27 aprile 2021 | [!DNL Analytics for Advertising] | Scopri perché e come aggiungere [!DNL Analytics for Advertising] macro ai tuoi tag annuncio di [!DNL Google Campaign Manager 360] per inviare dati di clic ad Adobe Analytics. | Vedi &quot;[Aggiungi [!DNL Analytics for Advertising] Macro ai [!DNL Google Campaign Manager 360] Tag annuncio](/help/integrations/analytics/macros-google-campaign-manager.md).&quot; |
| 19 aprile 2021 | [!DNL Analytics for Advertising] | Scopri perché e come aggiungere macro ai tag annuncio di [!DNL Flashtalking] per inviare dati di clic ad Adobe Analytics. | Vedi &quot;[Aggiungi [!DNL Analytics for Advertising] Macro ai [!DNL Flashtalking] Tag annuncio](/help/integrations/analytics/macros-flashtalking.md).&quot; |
| 27 ottobre 2021 | [!DNL Analytics for Advertising] | Se l&#39;organizzazione desidera passare dall&#39;utilizzo della libreria legacy di Adobe Analytics `visitorAPI.js` alla libreria [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=it) (`alloy.js`) per la raccolta dati, è necessario apportare alcune modifiche per abilitare la combinazione degli ID. | Vedi &quot;[Utilizzo della [!DNL Last Event Service] libreria JavaScript con Adobe Experience Platform [!DNL Web SDK]](/help/integrations/analytics/web-sdk.md).&quot; |
| 26 maggio 2021 | Aiuto | Il capitolo &quot;[!DNL Analytics for Advertising]&quot; ora include un sottocapitolo su &quot;Lavorare in [!DNL Analytics Marketing Channels]&quot;. | Consulta: &quot;[Nozioni di base dei canali di marketing](/help/integrations/analytics/marketing-channels/mc-overview.md)&quot;, &quot;[Utilizzo degli ID di Adobe Advertising per creare [!DNL Analytics Marketing Channels] Regole di elaborazione](/help/integrations/analytics/marketing-channels/mc-ids.md)&quot;, &quot;[Utilizzo di [!DNL Analytics Marketing Channels] con i dati di Adobe Advertising](/help/integrations/analytics/marketing-channels/mc-ac-data.md)&quot; e &quot;[Perché i dati dei canali possono variare tra Adobe Advertising e [!DNL Analytics Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md).&quot; |
| 26 maggio 2021 | Aiuto | È stato aggiunto un collegamento a tutte le esercitazioni video su [!DNL Analytics for Advertising]. | Consulta: &quot;[Esercitazioni video sulle integrazioni Adobe Advertising](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/overview.html?lang=it).&quot; |

{style="table-layout:auto"}

<!-- At some point, just make this an overview page instead?

Adobe Advertising is integrated with the following Adobe Experience Cloud products:

* [Adobe Analytics](/help/integrations/analytics/overview.md)

* Adobe Audience Manager

* Adobe Campaign (Adobe Advertising Search only)

 -->
