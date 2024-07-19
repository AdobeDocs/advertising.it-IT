---
title: Implementa  [!DNL Google Ads]  campagne acquisti
description: Scopri il flusso di lavoro per la configurazione di  [!DNL Google Ads]  campagne di acquisto.
exl-id: d80370d9-534d-4854-b7d3-1384a84320ad
feature: Search Campaign Management
source-git-commit: 3c702a01df1186e74c4f329a08199ce829be0827
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# Implementa [!DNL Google Ads] campagne acquisti

Gli annunci nelle campagne di acquisto utilizzano i dati sui prodotti nel feed di prodotto [!DNL Google Merchant Center] esistente, invece delle parole chiave, per decidere come e dove visualizzare gli annunci.

[!DNL Google Ads] campagne possono eseguire il targeting di [!DNL Google Shopping Network] utilizzando [!UICONTROL Campaign Type] &quot;[!UICONTROL Shopping Network].&quot; Le impostazioni per le campagne [!DNL Google Shopping] includono una priorità ([!UICONTROL High], [!UICONTROL Medium] o [!UICONTROL Low]). Facoltativamente, puoi visualizzare le informazioni sull’inventario locale negli annunci di acquisto utilizzando un’impostazione a livello di campagna.

Puoi controllare quali prodotti vengono visualizzati con gli annunci di acquisto configurando *[gruppi di prodotti](/help/search-social-commerce/campaign-management/campaigns/product-group-about.md)* a livello di gruppo di annunci. I gruppi di prodotti si basano su qualsiasi attributo di prodotto (categoria, tipo di prodotto, marchio, condizione, ID prodotto ed etichette personalizzate) e puoi creare fino a sette livelli di gruppi di prodotti da includere o escludere dalla gara. Puoi impostare le offerte al livello più basso dei gruppi di prodotti, utilizzando la stessa offerta per tutti i prodotti corrispondenti. Se lo stesso prodotto è incluso in più campagne, [!DNL Google Ads] utilizza prima la priorità a livello di campagna per determinare quale campagna (e l&#39;offerta associata) è idonea per l&#39;asta di annunci. Se tutte le campagne hanno la stessa priorità, la campagna con l’offerta più elevata è idonea.

## Passaggi per configurare [!DNL Google Ads] campagne di acquisto

Puoi impostare le campagne acquisti utilizzando [modelli di feed inventario](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) per [!DNL Google Shopping], [bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) o singolarmente. Le istruzioni seguenti includono collegamenti alla creazione di singole entità.

1. Configura il tuo account [!DNL Google Merchant Center] e compilalo con i dati di prodotto.

1. [Consenti a Search, Social e Commerce di scaricare dati dall&#39;account [!DNL Google Merchant Center] ](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

1. [Crea una campagna](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) sulla rete di acquisti.

1. [Crea un gruppo di annunci](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) all&#39;interno della campagna e imposta l&#39;offerta predefinita per tutti gli annunci.

   Puoi sovrascrivere l’offerta predefinita per i singoli gruppi di prodotti.

1. Crea gruppi di prodotti per il gruppo di annunci:

   1. [Crea un gruppo di prodotti &quot;Tutti i prodotti&quot;](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. (Facoltativo) [Crea gruppi di prodotti secondari](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   >[!NOTE]
   >Non è necessario creare annunci commerciali. Anche se il gruppo di annunci non include entità pubblicitarie, [!DNL Google Ads] visualizza comunque gli annunci per i prodotti.

1. (Facoltativo) Per tenere traccia dei clic sull&#39;annuncio, [genera un URL di tracciamento utilizzando lo strumento URL di tracciamento](/help/search-social-commerce/tools/click-tracking-url-generate.md), quindi aggiungilo alle impostazioni dell&#39;account, della campagna o del gruppo di prodotti.

1. Monitora le prestazioni [generando [!UICONTROL AdWords Shopping Performance Report]](/help/search-social-commerce/reports/management/specialty/specialty-report-generate.md) e [[!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md).

1. Se necessario:

   1. [Modifica le impostazioni della campagna](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) per regolare il budget della campagna.

      Se la campagna fa parte di un portfolio, l&#39;impostazione del portfolio &quot;[!UICONTROL Auto adjust campaign budget limits]&quot; consente a Search, Social e Commerce di ottimizzare i budget per tutte le campagne del portfolio.

   1. [Modifica l&#39;offerta massima per i gruppi di prodotti esistenti](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md), [elimina i gruppi di prodotti](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md) per i quali non desideri più creare annunci, oppure aggiungi [un nuovo gruppo di prodotti &quot;tutti i prodotti&quot;](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md)) o [nuovi gruppi di prodotti secondari](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md) per creare annunci per altri prodotti.

>[!NOTE]
>
>* Vedi i campi obbligatori per la gestione di [!DNL Google Shopping] campagne e gruppi di prodotti utilizzando [bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md) e [modelli di feed inventario](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-google-shopping.md).
>* Per ulteriori informazioni sulle campagne [!DNL Google Shopping], consulta la [[!DNL Google Ads] documentazione](https://support.google.com/google-ads/answer/2454022).
