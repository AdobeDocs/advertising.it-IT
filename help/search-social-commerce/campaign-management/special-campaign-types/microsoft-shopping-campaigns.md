---
title: Implementare [!DNL Microsoft® Advertising] campagne di acquisto
description: Scopri il flusso di lavoro per la configurazione di [!DNL Microsoft® Advertising] campagne di acquisto.
exl-id: 3fb19b92-5bc0-414e-9234-68310082d0ed
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 0%

---

# Implementare [!DNL Microsoft® Advertising] campagne di acquisto

Gli annunci nelle campagne di acquisto utilizzano i dati sui prodotti nel tuo [!DNL Microsoft® Merchant Center] feed di prodotto, anziché parole chiave, per decidere come e dove visualizzare gli annunci.

[!DNL Microsoft®] campagne di acquisto mirate a [!DNL Microsoft® Advertising Shopping Network]. Le impostazioni per le campagne di acquisto includono un paese specifico in cui i prodotti vengono venduti e una priorità ([!DNL High], [!DNL Medium], o [!DNL Low]). Facoltativamente, puoi filtrare l’inventario per pubblicizzare i prodotti con attributi specifici e individuare o escludere posizioni e tipi di dispositivi specifici.

Puoi controllare quali prodotti vengono visualizzati con gli annunci commerciali impostando l’opzione a più livelli *[gruppi di prodotti](/help/search-social-commerce/campaign-management/campaigns/product-group-about.md)* a livello di gruppo di annunci. I gruppi di prodotti si basano su qualsiasi attributo di prodotto (categoria, tipo di prodotto, marchio, condizione, ID prodotto ed etichette personalizzate) e puoi creare fino a sette livelli di gruppi di prodotti per includere o escludere dalla gara d’appalto, escluso &quot;[!DNL Add Products].&quot; Puoi impostare le offerte al livello più basso dei gruppi di prodotti, utilizzando la stessa offerta per tutti i prodotti corrispondenti. Se lo stesso prodotto è incluso in più campagne, [!DNL Microsoft® Advertising] utilizza prima la priorità a livello di campagna per determinare quale campagna (e l’offerta associata) è idonea per l’asta pubblicitaria. Se tutte le campagne hanno la stessa priorità, la campagna con l’offerta più elevata è idonea.

## Passaggi per impostare [!DNL Microsoft® Advertising] campagne di acquisto

Puoi impostare le campagne di acquisto utilizzando [modelli di feed inventario](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) per [!DNL Microsoft® Advertising], utilizzando [bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md), o singolarmente. Le istruzioni seguenti includono collegamenti alla creazione di singole entità.

1. Configurare [!DNL Microsoft® Merchant Center] e compilarlo con i dati di prodotto.

1. [Consenti a Search, Social e Commerce di scaricare dati da [!DNL Microsoft® Merchant Center] account](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

1. [Creare una campagna](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) sulla rete commerciale.

1. [Creare un gruppo di annunci](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) all’interno della campagna e imposta l’offerta predefinita per tutti gli annunci.

Puoi sovrascrivere l’offerta predefinita per i singoli gruppi di prodotti.

1. Crea gruppi di prodotti per il gruppo di annunci:

   1. [Creare un gruppo di prodotti &quot;Tutti i prodotti&quot;](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. (Facoltativo) [Creare gruppi di prodotti secondari](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. Crea [annunci di prodotti](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) con [linee di promozione da includere potenzialmente in ogni annuncio di acquisto](/help/search-social-commerce/campaign-management/campaigns/product-group-settings-microsoft.md) all’interno del gruppo di annunci.

      Microsoft® Advertising genera in modo dinamico la copia dell’annuncio e l’URL della pagina di destinazione per ogni annuncio.

      >[!NOTE]
      >
      >Anche se il gruppo di annunci non include entità annuncio, [!DNL Microsoft® Advertising] visualizza comunque gli annunci per i prodotti.

1. (Facoltativo) Per tenere traccia dei clic sull’annuncio, [generare un URL di tracciamento utilizzando lo strumento URL di tracciamento](/help/search-social-commerce/tools/click-tracking-url-generate.md). La best practice prevede l’aggiunta dell’URL di tracciamento al [!UICONTROL Tracking Template] nelle impostazioni account, campagna o gruppo di prodotti. Per semplificare la manutenzione, aggiungilo al livello più alto possibile.

   In alternativa, puoi aggiungere l’URL di tracciamento ai dati di prodotto all’interno di [!DNL Microsoft® Merchant Center] account. A tal fine, includi l’URL di tracciamento, insieme al valore nel campo &quot;link&quot; o &quot;mobile_link&quot;, a seconda dei casi, in una colonna personalizzata&quot;[bingads_redirect](https://help.ads.microsoft.com/#apex/3/en/51084)&quot; nel feed del prodotto. Il valore nel campo &quot;bingads_redirect&quot; sostituisce i valori nei campi &quot;link&quot; e &quot;mobile_link&quot;. Gli URL generati con questo metodo non includono parametri di tracciamento specificati nelle impostazioni dell’account Search, Social e Commerce o nella campagna.

1. Monitorare le prestazioni tramite [generazione di [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md).

1. Se necessario:

   1. [Modificare le impostazioni della campagna](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) per modificare il budget della campagna.

      Se la campagna fa parte di un portfolio, l’impostazione del portfolio &quot;[!UICONTROL Auto adjust campaign budget limits]&quot; consente a Search, Social e Commerce di ottimizzare i budget per tutte le campagne del portfolio.

   1. Modifica l’offerta massima per i gruppi di prodotti esistenti, elimina i gruppi di prodotti per i quali non desideri più creare annunci, oppure aggiungi un nuovo gruppo di prodotti &quot;tutti i prodotti&quot; o nuovi gruppi di prodotti secondari per creare annunci per prodotti aggiuntivi.

>[!NOTE]
>
>* Visualizza i campi obbligatori per la gestione [!DNL Microsoft® Shopping] campagne e gruppi di prodotti tramite [bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md) e [modelli di feed inventario](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-microsoft-shopping.md).
>* Per ulteriori informazioni su [!DNL Microsoft® Shopping] campagne, consulta [[!DNL Microsoft® Advertising] documentazione](https://help.ads.microsoft.com/#apex/3/en/50903).
