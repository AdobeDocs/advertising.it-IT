---
title: Configurare account e campagne di ad network
description: Segui il flusso di lavoro di configurazione per connessioni di rete di annunci, campagne, tracciamento, metriche di conversione e ottimizzazione del portfolio facoltativa.
feature: Search Getting Started, Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: 54967645-9f46-5896-8af7-b943b426aadf
    internal-label: Search Getting Started
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 76a8d8b448441e4d7380ebc4f007aa8b5a2ab5f5
workflow-type: tm+mt
source-wordcount: '650'
ht-degree: 0%
---
# Configurare account e campagne di ad network

*funzionalità Beta*

[!DNL Adobe] e la tua agenzia collaborano con te per collegare i tuoi account di rete degli annunci, preparare campagne, configurare il tracciamento e convalidare i dati sulle prestazioni. Se desideri ottimizzare le campagne idonee tramite Search, Social e Commerce, il flusso di lavoro include anche la configurazione del portfolio.

Questo elenco di controllo fornisce i dettagli dell&#39;account e della campagna per il [flusso di lavoro di implementazione](implemention-overview.md) più ampio. Le attività che puoi eseguire dipendono dalle tue autorizzazioni e dalla funzionalità [supportata per ogni rete di annunci e tipo di campagna](/help/search-social-commerce/introduction/supported-inventory.md).

## Imposta flusso di lavoro

1. **Conferma i requisiti di accesso e account.**

   Rivolgiti al tuo amministratore per confermare l’accesso all’inserzionista appropriato e le autorizzazioni necessarie per le tue attività. Consulta &quot;[Amministrazione utenti per Search, Social e Commerce](/help/search-social-commerce/user-administration.md).&quot;

   Se necessario, crea l’account effettivo della rete di annunci sul sito web della rete di annunci. La creazione di un record di account in Search, Social e Commerce non comporta la creazione di un account sulla rete di annunci.

1. **Connetti o registra ogni account di rete dell&#39;annuncio.**

   In [!UICONTROL Manage] > [!UICONTROL Accounts], utilizza il flusso di lavoro per il [tipo di account](/help/search-social-commerce/manage/accounts/ad-network-account-about.md):

   * **Connessione API:** [Crea i dettagli dell&#39;account](/help/search-social-commerce/manage/accounts/api-accounts/api-account-manage.md#create-account), completa l&#39;autenticazione specifica della rete, configura le opzioni di tracciamento e abilita l&#39;account. Verificare il relativo [stato di autenticazione e di accesso](/help/search-social-commerce/manage/accounts/api-accounts/api-account-manage.md#authentication-status); l&#39;autenticazione riuscita non significa necessariamente che siano state concesse tutte le autorizzazioni necessarie.

   * **Caricamento dati:** [Crea i dettagli dell&#39;account e carica i dati della campagna e delle prestazioni](/help/search-social-commerce/manage/accounts/data-upload-accounts/data-upload-account-manage.md). Questi account non vengono sincronizzati con la rete di annunci o non supportano l’ottimizzazione del portfolio.

   * **[!DNL Naver]solo tracciamento:** Segui il [flusso di lavoro account di solo tracciamento](/help/search-social-commerce/manage/accounts/template-account-manage.md). Utilizza i bulksheet per generare URL di tracciamento e applicarli nell’editor della rete di annunci; l’account non sincronizza o supporta l’ottimizzazione del portfolio.

1. **Rivedi o crea la struttura della campagna.**

   Per gli account connessi a API, controlla le campagne sincronizzate e i relativi componenti. [Richiedere una sincronizzazione manuale](/help/search-social-commerce/manage/accounts/api-accounts/sync-api-accounts.md) quando necessario.

   Per i tipi di campagna supportati, utilizzare [!UICONTROL Manage] > [!UICONTROL Campaigns] per [creare o modificare le campagne](/help/search-social-commerce/manage/campaigns/campaign-manage.md). Crea i [gruppi di annunci](/help/search-social-commerce/manage/ad-groups/ad-group-manage.md), [annunci](/help/search-social-commerce/manage/ads/ad-manage.md) richiesti e altri componenti supportati. È inoltre possibile utilizzare [bulksheet](/help/search-social-commerce/set-up/bulksheets/about.md) per operazioni di massa supportate.

   Completa tutte le impostazioni di rete richieste prima di attivare le campagne. Gestisci i componenti non supportati nell’interfaccia della rete di annunci.

1. **Configura e convalida il tracciamento prima dell&#39;avvio.**

   Seleziona il [metodo di tracciamento conversione](/help/search-social-commerce/tracking/conversion-tracking-about.md) che corrisponde alla tua implementazione. Se necessario, [genera e applica URL di tracciamento dei clic](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md) e [genera tag di tracciamento delle conversioni](/help/search-social-commerce/goals/conversions/conversion-tag-generate.md).

   Configura le [integrazioni](/help/integrations/home.md) o i [feed di conversione](/help/search-social-commerce/tracking/tracking-about.md) richiesti e verifica che le conversioni possano essere attribuite come previsto. Per le campagne di solo tracciamento, applica gli URL di tracciamento generati nell’editor della rete di annunci.

1. **Verifica le metriche di conversione.**

   In [!UICONTROL Goals] > [!UICONTROL Conversions], [rivedi le metriche tracciate e rendi visibili le metriche richieste](/help/search-social-commerce/goals/conversions/conversion-metrics-manage.md#conversion-metrics-change-available) per le visualizzazioni di gestione, i report e gli obiettivi. Se necessario, modifica i nomi visualizzati per distinguere le metriche.

1. **(Facoltativo) Preparare l&#39;ottimizzazione del portfolio.**

   Conferma che le campagne e le relative strategie di offerta sono [idonee per l&#39;ottimizzazione del portfolio](/help/search-social-commerce/manage/portfolios/portfolio-about.md#optimization-by-bid-strategy).

   [Crea o seleziona un obiettivo](/help/search-social-commerce/goals/objectives/objective-about.md) che utilizza le metriche di conversione appropriate. In [!UICONTROL Manage] > [!UICONTROL Portfolios], [crea un portfolio](/help/search-social-commerce/manage/portfolios/portfolio-create.md) o [modifica un portfolio esistente](/help/search-social-commerce/manage/portfolios/portfolio-edit.md) con le impostazioni richieste per finalità, strategia di spesa e ottimizzazione.

   [Assegna le campagne al portfolio](/help/search-social-commerce/manage/campaigns/campaign-manage.md#campaign-portfolio). Ogni campagna può appartenere a un solo portfolio e tutte le campagne in un portfolio devono utilizzare la stessa valuta.

1. **Convalidare i dati della campagna e stabilire una previsione delle prestazioni.**

   Verifica che i dati su costo, clic e conversione siano disponibili per ogni campagna. Confrontare i dati di conversione con l&#39;origine appropriata, inclusi [!DNL Google Ads] e [!DNL Microsoft Advertising], se applicabile. Quando confronti i rapporti, utilizza intervalli di date e impostazioni di attribuzione coerenti.

   Per un nuovo portfolio, [attivalo](/help/search-social-commerce/manage/portfolios/portfolio-change-status.md) per raccogliere e modellare i dati. Convalida i dati e le impostazioni del portfolio prima di abilitare l’ottimizzazione.

1. **(Facoltativo) Ottimizzazione portfolio Launch.**

   Quando il portfolio è pronto, [cambiane lo stato in ottimizzato](/help/search-social-commerce/manage/portfolios/portfolio-change-status.md), rivedendo i prerequisiti e i messaggi di conferma. Search, Social e Commerce ottimizzano quindi il portfolio in base alle sue impostazioni e alle strategie di offerta della campagna supportata.

1. **Configura monitoraggio e reporting continui.**

   [Personalizza le visualizzazioni dati](/help/search-social-commerce/common-tasks/data-views/data-views-about.md), [Configura avvisi personalizzati](/help/search-social-commerce/common-tasks/alerts-manage.md) e [genera rapporti pianificati](/help/search-social-commerce/reports/management/report-manage.md). Quando necessario, automatizza la generazione di rapporti utilizzando [modelli di rapporti](/help/search-social-commerce/reports/report-templates-manage.md) e [feed di fogli di calcolo](/help/search-social-commerce/reports/spreadsheet-feeds-manage.md).

   Continua a [monitorare e regolare campagne e portfolio](/help/search-social-commerce/manage/manage-about.md#monitor-performance) dopo il lancio.

>[!MORELIKETHIS]
>
>* [Panoramica sull&#39;implementazione di Search, Social e Commerce](implemention-overview.md)
>* [Informazioni sulla gestione di campagne e portfolio](/help/search-social-commerce/manage/manage-about.md)
>* [[!DNL Google Ads] dati di conversione in Search, Social e Commerce](/help/search-social-commerce/tracking/google-conversion-data.md)
>* [[!DNL Microsoft Advertising] dati di conversione in Search, Social e Commerce](/help/search-social-commerce/tracking/microsoft-conversion-data.md)
