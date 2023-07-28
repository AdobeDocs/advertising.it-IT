---
title: Implementare [!DNL Google Ads] campagne con prestazione massima
description: Scopri il flusso di lavoro per la configurazione di [!DNL Google Ads] numero massimo di campagne con prestazioni.
exl-id: afad96b2-d4a6-41ee-ad84-38aa1306d73e
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# Implementare [!DNL Google Ads] campagne con prestazione massima

In entrata [!DNL Google Ads] con il numero massimo di campagne, non puoi impostare gruppi di annunci, annunci o parole chiave. Nelle impostazioni della campagna puoi invece specificare uno o più gruppi di risorse, che includono titoli, descrizioni e immagini caricate, loghi e [!DNL YouTube videos]. [!DNL Google Ads] combina automaticamente le risorse per distribuire gli annunci in base al canale (ad esempio [!DNL YouTube], [!DNL Gmail], o [!DNL Search]).

Puoi visualizzare le campagne con prestazione massima esistenti, con i dati sulle prestazioni in formato tabella e grafico dell’andamento, nel [!DNL Campaigns] vista; i dati non sono disponibili ai livelli inferiori. I dati sulle prestazioni a livello di campagna sono disponibili anche nei rapporti e in Adobe Analytics (per gli inserzionisti con un’ [Integrazione di Analytics](/help/integrations/analytics/overview.md). Per visualizzare i dati sulle prestazioni per le campagne con prestazione massima in [!DNL Analytics], la campagna deve utilizzare [codice di tracciamento s_kwcid aggiornato](/help/search-social-commerce/tracking/skwcid-tracking-parameter.md) (che tiene traccia dell’ID della campagna e dell’ID del gruppo di annunci).

>[!NOTE]
>
>* È necessario caricare manualmente tutti i file di immagine. Collegamenti a [!DNL Google Merchant Center] i feed di prodotto non sono supportati.
>* Sono disponibili solo le impostazioni richieste. Per le impostazioni facoltative, accedi a [!DNL Google Ads] editor.
>* Il supporto per i gruppi di voci non è disponibile. Per gestire e visualizzare i dati per l’elenco dei gruppi, accedi a [!DNL Google Ads] editor.

## Passaggi per impostare [!DNL Google Ads] campagne con prestazione massima

Puoi impostare le campagne con prestazione massima singolarmente dalla [!UICONTROL Campaigns] > [!UICONTROL Campaigns] visualizzazione.

1. [Creare una campagna](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) con tipo di campagna **[!UICONTROL Performance Max]**.

   Specifica la [!UICONTROL Campaign Details], [!UICONTROL Budget Options], [!UICONTROL Campaign Targeting], e [!UICONTROL URL Options]. È possibile inserire [!UICONTROL Negative Keywords], immetti [!UICONTROL Negative Websites], e/o sovrascrivere [!UICONTROL Campaign Tracking] opzioni.

1. Crea gruppi di risorse e carica le risorse per la campagna:

   1. Nella parte inferiore delle impostazioni della campagna, fai clic su **[!UICONTROL Manage Asset Groups]**.

   1. Specifica le impostazioni per il primo gruppo di risorse e carica immagini, logo e video facoltativi per il gruppo di risorse.

      Consulta [descrizioni delle impostazioni del gruppo di risorse](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md) per comprendere i requisiti e le specifiche.

   1. Se necessario, aggiungi altri gruppi di risorse.

1. Clic **[!UICONTROL Post]**.

1. (Facoltativo) Aggiungi la campagna a un portfolio ibrido per l’ottimizzazione.
