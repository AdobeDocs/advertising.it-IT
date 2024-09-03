---
title: Implementa  [!DNL Google Ads]  campagne con prestazione massima
description: Scopri il flusso di lavoro per la configurazione di  [!DNL Google Ads]  campagne con prestazione massima.
exl-id: 4208774c-e4dd-499d-987e-933fe073c04f
feature: Search Campaign Management
source-git-commit: 283fced2b3faa64b6383b6ab2a41696cba0da06f
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# Implementa [!DNL Google Ads] campagne con prestazione massima

Nelle campagne con prestazione massima di [!DNL Google Ads], non puoi impostare gruppi di annunci, annunci o parole chiave. Nelle impostazioni della campagna puoi invece specificare uno o più gruppi di risorse, che includono titoli, descrizioni e immagini caricate, loghi e [!DNL YouTube videos]. [!DNL Google Ads] combina automaticamente le risorse per distribuire annunci in base al canale (ad esempio [!DNL YouTube], [!DNL Gmail] o [!DNL Search]).

Nella visualizzazione [!DNL Campaigns] è possibile visualizzare le campagne con prestazione massima esistenti, con i dati sulle prestazioni in formato tabella e grafico dell&#39;andamento. I dati non sono disponibili ai livelli inferiori. I dati sulle prestazioni a livello di campagna sono disponibili anche nei report e in Adobe Analytics (per gli inserzionisti con un&#39;integrazione di [Analytics](/help/integrations/analytics/overview.md). Per visualizzare i dati sulle prestazioni per le campagne con prestazione massima in [!DNL Analytics], la campagna deve utilizzare il [codice di tracciamento AMO ID aggiornato](/help/integrations/analytics/ids.md#amo-id-formats) (che tiene traccia dell&#39;ID della campagna e dell&#39;ID del gruppo di annunci).

>[!NOTE]
>
>* È necessario caricare manualmente tutti i file di immagine. I collegamenti ai feed di prodotto [!DNL Google Merchant Center] non sono supportati.
>* Sono disponibili solo le impostazioni richieste. Per le impostazioni facoltative, accedere all&#39;editor [!DNL Google Ads].
>* Il supporto per i gruppi di voci non è disponibile. Per gestire e visualizzare i dati per l&#39;elenco dei gruppi, accedere all&#39;editor [!DNL Google Ads].

## Passaggi per impostare [!DNL Google Ads] campagne con prestazione massima

Puoi impostare le campagne con prestazione massima singolarmente dalla vista [!UICONTROL Campaigns] > [!UICONTROL Campaigns].

1. [Crea una campagna](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) con tipo di campagna **[!UICONTROL Performance Max]**.

   Specificare [!UICONTROL Campaign Details], [!UICONTROL Budget Options], [!UICONTROL Campaign Targeting] e [!UICONTROL URL Options]. È possibile immettere [!UICONTROL Negative Keywords], immettere [!UICONTROL Negative Websites] e/o sostituire le opzioni [!UICONTROL Campaign Tracking].

1. Crea gruppi di risorse e carica le risorse per la campagna:

   1. Nella parte inferiore delle impostazioni della campagna, fare clic su **[!UICONTROL Manage Asset Groups]**.

   1. Specifica le impostazioni per il primo gruppo di risorse e carica immagini, logo e video facoltativi per il gruppo di risorse.

      Per informazioni sui requisiti e le specifiche, consulta le [descrizioni delle impostazioni del gruppo di risorse](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md).

   1. Se necessario, aggiungi altri gruppi di risorse.

1. Fare clic su **[!UICONTROL Post]**.

1. (Facoltativo) Aggiungi la campagna a un portfolio ibrido per l’ottimizzazione.
