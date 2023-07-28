---
title: Implementare [!DNL Google Ads] campagne di acquisto
description: Scopri il flusso di lavoro per la configurazione di [!DNL Google Ads] campagne di acquisto.
exl-id: aab61d94-861f-4072-b044-f9ae6759e028
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---

# Implementare [!DNL Google Ads] campagne di acquisto

Gli annunci nelle campagne di acquisto utilizzano i dati sui prodotti nel tuo [!DNL Google Merchant Center] feed di prodotto, anziché parole chiave, per decidere come e dove visualizzare gli annunci.

[!DNL Google Ads] possono eseguire il targeting delle campagne [!DNL Google Shopping Network] utilizzando [!UICONTROL Campaign Type] &quot;[!UICONTROL Shopping Network].&quot; Le impostazioni per [!DNL Google Shopping] le campagne includono una priorità ([!UICONTROL High], [!UICONTROL Medium], o [!UICONTROL Low]). Facoltativamente, puoi visualizzare le informazioni sull’inventario locale negli annunci di acquisto utilizzando un’impostazione a livello di campagna.

Puoi controllare quali prodotti vengono visualizzati con gli annunci commerciali impostando l’opzione a più livelli *[gruppi di prodotti](/help/search-social-commerce/campaign-management/campaigns/product-group-about.md)* a livello di gruppo di annunci. I gruppi di prodotti si basano su qualsiasi attributo di prodotto (categoria, tipo di prodotto, marchio, condizione, ID prodotto ed etichette personalizzate) e puoi creare fino a sette livelli di gruppi di prodotti da includere o escludere dalla gara. Puoi impostare le offerte al livello più basso dei gruppi di prodotti, utilizzando la stessa offerta per tutti i prodotti corrispondenti. Se lo stesso prodotto è incluso in più campagne, [!DNL Google Ads] utilizza prima la priorità a livello di campagna per determinare quale campagna (e l’offerta associata) è idonea per l’asta pubblicitaria. Se tutte le campagne hanno la stessa priorità, la campagna con l’offerta più elevata è idonea.

## Passaggi per impostare [!DNL Google Ads] campagne di acquisto

Puoi impostare le campagne di acquisto utilizzando [modelli di feed inventario](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) per [!DNL Google Shopping], utilizzando [bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md), o singolarmente. Le istruzioni seguenti includono collegamenti alla creazione di singole entità.

1. Configurare [!DNL Google Merchant Center] e compilarlo con i dati di prodotto.

1. [Consenti a Search, Social e Commerce di scaricare dati da [!DNL Google Merchant Center] account](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

1. [Creare una campagna](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) sulla rete commerciale.

1. [Creare un gruppo di annunci](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) all’interno della campagna e imposta l’offerta predefinita per tutti gli annunci.

Puoi sovrascrivere l’offerta predefinita per i singoli gruppi di prodotti.

1. Crea gruppi di prodotti per il gruppo di annunci:

   1. [Creare un gruppo di prodotti &quot;Tutti i prodotti&quot;](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. (Facoltativo) [Creare gruppi di prodotti secondari](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   >[!NOTE]
   >Non è necessario creare annunci commerciali. Anche se il gruppo di annunci non include entità annuncio, [!DNL Google Ads] visualizza comunque gli annunci per i prodotti.

1. (Facoltativo) Per tenere traccia dei clic sull’annuncio, [generare un URL di tracciamento utilizzando lo strumento URL di tracciamento](/help/search-social-commerce/tools/click-tracking-url-generate.md), quindi aggiungerlo alle impostazioni dell’account, della campagna o del gruppo di prodotti.

1. Monitorare le prestazioni tramite [generazione di [!UICONTROL AdWords Shopping Performance Report]](/help/search-social-commerce/reports/management/specialty/specialty-report-generate.md) e [il [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md).

1. Se necessario:

   1. [Modificare le impostazioni della campagna](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) per modificare il budget della campagna.

      Se la campagna fa parte di un portfolio, l’impostazione del portfolio &quot;[!UICONTROL Auto adjust campaign budget limits]&quot; consente a Search, Social e Commerce di ottimizzare i budget per tutte le campagne del portfolio.

   1. [Regola l&#39;offerta massima per i gruppi di prodotti esistenti](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md), [elimina gruppi di prodotti](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md) per la quale non desideri più creare annunci o aggiungere una [nuovo gruppo di prodotti &quot;all products&quot;](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md)) o [nuovi gruppi di prodotti secondari](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md) per creare annunci per prodotti aggiuntivi.

>[!NOTE]
>
>* Visualizza i campi obbligatori per la gestione [!DNL Google Shopping] campagne e gruppi di prodotti tramite [bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md) e [modelli di feed inventario](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-google-shopping.md).
>* Per ulteriori informazioni su [!DNL Google Shopping] campagne, consulta [[!DNL Google Ads] documentazione](https://support.google.com/google-ads/answer/2454022).
