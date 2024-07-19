---
title: Implementa  [!DNL Microsoft Advertising]  campagne acquisti
description: Scopri il flusso di lavoro per la configurazione di  [!DNL Microsoft Advertising]  campagne di acquisto.
exl-id: fd10237b-864d-4808-8644-3fcb18edebde
feature: Search Campaign Management
source-git-commit: d5d4dee4356d941ea9cae74b9385add00e0480c3
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# Implementa [!DNL Microsoft Advertising] campagne acquisti

Gli annunci nelle campagne di acquisto utilizzano i dati sui prodotti nel feed di prodotto [!DNL Microsoft Merchant Center] esistente, invece delle parole chiave, per decidere come e dove visualizzare gli annunci.

[!DNL Microsoft] campagne di acquisto hanno come target [!DNL Microsoft Advertising Shopping Network]. Le impostazioni per le campagne di acquisto includono un paese specificato in cui i prodotti vengono venduti e una priorità ([!DNL High], [!DNL Medium] o [!DNL Low]). Facoltativamente, puoi filtrare l’inventario per pubblicizzare i prodotti con attributi specifici e individuare o escludere posizioni e tipi di dispositivi specifici.

Puoi controllare quali prodotti vengono visualizzati con gli annunci di acquisto configurando *[gruppi di prodotti](/help/search-social-commerce/campaign-management/campaigns/product-group-about.md)* a livello di gruppo di annunci. I gruppi di prodotti si basano su qualsiasi attributo di prodotto (categoria, tipo di prodotto, marchio, condizione, ID prodotto ed etichette personalizzate) ed è possibile creare fino a sette livelli di gruppi di prodotti da includere o escludere dalla gara, escluso &quot;[!DNL Add Products]&quot;. Puoi impostare le offerte al livello più basso dei gruppi di prodotti, utilizzando la stessa offerta per tutti i prodotti corrispondenti. Se lo stesso prodotto è incluso in più campagne, [!DNL Microsoft Advertising] utilizza prima la priorità a livello di campagna per determinare quale campagna (e l&#39;offerta associata) è idonea per l&#39;asta di annunci. Se tutte le campagne hanno la stessa priorità, la campagna con l’offerta più elevata è idonea.

## Passaggi per configurare [!DNL Microsoft Advertising] campagne di acquisto

Puoi impostare le campagne acquisti utilizzando [modelli di feed inventario](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) per [!DNL Microsoft Advertising], [bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) o singolarmente. Le istruzioni seguenti includono collegamenti alla creazione di singole entità.

1. Configura il tuo account [!DNL Microsoft Merchant Center] e compilalo con i dati di prodotto.

1. [Consenti a Search, Social e Commerce di scaricare dati dall&#39;account [!DNL Microsoft Merchant Center] ](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

1. [Crea una campagna](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) sulla rete di acquisti.

1. [Crea un gruppo di annunci](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) all&#39;interno della campagna e imposta l&#39;offerta predefinita per tutti gli annunci.

   Puoi sovrascrivere l’offerta predefinita per i singoli gruppi di prodotti.

1. Crea gruppi di prodotti per il gruppo di annunci:

   1. [Crea un gruppo di prodotti &quot;Tutti i prodotti&quot;](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. (Facoltativo) [Crea gruppi di prodotti secondari](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. Crea [annunci di prodotto](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) con [righe di promozione da includere potenzialmente in ogni annuncio di acquisto](/help/search-social-commerce/campaign-management/campaigns/product-group-settings-microsoft.md) all&#39;interno del gruppo di annunci.

      Microsoft Advertising genera in modo dinamico la copia dell’annuncio e l’URL della pagina di destinazione per ogni annuncio.

      >[!NOTE]
      >
      >Anche se il gruppo di annunci non include entità pubblicitarie, [!DNL Microsoft Advertising] visualizza comunque gli annunci per i prodotti.

1. (Facoltativo) Per tenere traccia dei clic sull&#39;annuncio, [genera un URL di tracciamento utilizzando lo strumento URL di tracciamento](/help/search-social-commerce/tools/click-tracking-url-generate.md). La procedura consigliata consiste nell&#39;aggiungere l&#39;URL di tracciamento al campo [!UICONTROL Tracking Template] nelle impostazioni dell&#39;account, della campagna o del gruppo di prodotti. Per semplificare la manutenzione, aggiungilo al livello più alto possibile.

   In alternativa, è possibile aggiungere l&#39;URL di tracciamento ai dati di prodotto nell&#39;account [!DNL Microsoft Merchant Center]. A questo scopo, includi l&#39;URL di tracciamento, insieme al valore nel campo &quot;link&quot; o &quot;mobile_link&quot;, a seconda dei casi, in una colonna personalizzata &quot;[bingads_redirect](https://help.ads.microsoft.com/#apex/3/en/51084)&quot; all&#39;interno del feed del prodotto. Il valore nel campo &quot;bingads_redirect&quot; sostituisce i valori nei campi &quot;link&quot; e &quot;mobile_link&quot;. Gli URL generati con questo metodo non includono parametri di tracciamento specificati nelle impostazioni dell’account o della campagna Search, Social e Commerce.

1. Monitora le prestazioni [generando [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md).

1. Se necessario:

   1. [Modifica le impostazioni della campagna](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) per regolare il budget della campagna.

      Se la campagna fa parte di un portfolio, l&#39;impostazione del portfolio &quot;[!UICONTROL Auto adjust campaign budget limits]&quot; consente a Search, Social e Commerce di ottimizzare i budget per tutte le campagne del portfolio.

   1. Modifica l’offerta massima per i gruppi di prodotti esistenti, elimina i gruppi di prodotti per i quali non desideri più creare annunci, oppure aggiungi un nuovo gruppo di prodotti &quot;tutti i prodotti&quot; o nuovi gruppi di prodotti secondari per creare annunci per prodotti aggiuntivi.

>[!NOTE]
>
>* Vedi i campi obbligatori per la gestione di [!DNL Microsoft Shopping] campagne e gruppi di prodotti utilizzando [bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md) e [modelli di feed inventario](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-microsoft-shopping.md).
>* Per ulteriori informazioni sulle campagne [!DNL Microsoft Shopping], consulta la [[!DNL Microsoft Advertising] documentazione](https://help.ads.microsoft.com/#apex/3/en/50903).
