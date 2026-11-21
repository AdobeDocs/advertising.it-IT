---
title: Panoramica dell’implementazione di Search, Social e Commerce
description: Scopri il flusso di lavoro generale per avviare e gestire un portfolio.
exl-id: c99dc029-81e4-4416-89b1-7cf8d66658b2
feature: Search Getting Started
TQID: 'https://experienceleague.adobe.com/AFMTue1YGuFjAJF04HTHEimfd2JC8ZxSkYCRDu8wDFY'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 54967645-9f46-5896-8af7-b943b426aadf
    internal-label: Search Getting Started
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: 76a8d8b448441e4d7380ebc4f007aa8b5a2ab5f5
workflow-type: tm+mt
source-wordcount: '886'
ht-degree: 0%
---
# Panoramica dell’implementazione di Search, Social e Commerce

[!DNL Adobe] o una delle sue agenzie affiliate collabora con ogni inserzionista per lanciare i suoi portfolio di pubblicità online e per tenere traccia di eventuali campagne pubblicitarie aggiuntive. Dopo il lancio iniziale, ulteriori attività continuative garantiscono che gli obiettivi dell&#39;inserzionista continueranno a essere raggiunti.

Di seguito è riportato il flusso di lavoro generale per l’implementazione e l’utilizzo di Search, Social e Commerce.

## Lancio iniziale

[!DNL Adobe] e/o l&#39;agenzia di lavoro dell&#39;utente eseguono le seguenti operazioni:

1. Valuta i tuoi obiettivi aziendali di alto livello e progetta strategie per raggiungerli:

   1. Identifica il tuo modello di business e gli obiettivi di marketing.

   1. Identificare i requisiti di tracciamento delle conversioni

   1. Analizza le strutture degli annunci pubblicitari online esistenti.

   1. Identifica le metriche per l’ottimizzazione e il reporting del portfolio.

1. (Utenti amministratori o account manager) Impostare account amministrativi:

   1. Configura l&#39;account dell&#39;inserzionista. Se un&#39;agenzia gestisce i dati dell&#39;inserzionista, l&#39;account dell&#39;inserzionista deve essere associato all&#39;account dell&#39;agenzia.

   1. Se necessario, crea account utente per l’inserzionista per visualizzare e gestire i dati della campagna e generare rapporti.

   Rivolgiti al tuo amministratore per configurare l’accesso utilizzando Adobe Admin Console e i profili di prodotto appropriati. Consulta &quot;[Amministrazione utenti per Search, Social e Commerce](/help/search-social-commerce/user-administration.md).&quot;

1. Sincronizza con, o crea, campagne per ciascuno dei tuoi account di rete degli annunci:

   * Per gli account connessi all&#39;API, [crea i dettagli dell&#39;account](/help/search-social-commerce/manage/accounts/api-accounts/api-account-manage.md#create-account) in [!UICONTROL Manage] > [!UICONTROL Accounts], completa l&#39;autenticazione specifica della rete, configura le opzioni di tracciamento e abilita l&#39;account.

   * Per gli account senza supporto API, segui il flusso di lavoro [Caricamento dati](/help/search-social-commerce/manage/accounts/data-upload-accounts/data-upload-account-manage.md) o [Account di solo tracciamento](/help/search-social-commerce/manage/accounts/template-account-manage.md), a seconda dei casi. Questi account non vengono sincronizzati con la rete di annunci o non supportano l’ottimizzazione del portfolio.

   * Se gli account non contengono già dati della campagna, aggiungi campagne, gruppi di annunci, parole chiave, annunci e posizionamenti da Search, Social e Commerce o dall’interno della rete di annunci.

     Per l&#39;elenco di controllo dettagliato, vedere &quot;[Configurare account e campagne di ad network](campaign-implementation-overview.md).&quot; Per i tipi di campagna supportati, utilizzare [!UICONTROL Manage] > [!UICONTROL Campaigns] per [creare e gestire campagne](/help/search-social-commerce/manage/campaigns/campaign-manage.md).

1. Imposta il tracciamento per tutti gli annunci per i quali desideri che Adobe Advertising tenga traccia delle conversioni:

   1. (Se necessario) [Configura il tracciamento dei clic](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md) per gli annunci e, facoltativamente, per le parole chiave, [!DNL Google Ads] posizionamenti e [!DNL Google Ads] estensioni generando e caricando gli URL di tracciamento dei clic.

      Gli URL di tracciamento dei clic per gli inserzionisti con il servizio di tracciamento delle conversioni basato su pixel di Adobe Advertising includono un reindirizzamento ai server [!DNL Adobe].

   1. [Configura il tracciamento delle conversioni](/help/search-social-commerce/tracking/conversion-tracking-about.md). A seconda dell’implementazione, potrebbe essere necessario aggiungere tag di tracciamento delle conversioni alle pagine web appropriate e/o impostare un rilascio di feed giornaliero per i dati di conversione raccolti utilizzando un metodo personalizzato. Puoi [generare tag di tracciamento delle conversioni di Adobe Advertising](/help/search-social-commerce/goals/conversions/conversion-tag-generate.md) da [!UICONTROL Goals] > [!UICONTROL Conversions].

      Per ulteriori informazioni, vedere &quot;[Informazioni sul tracciamento per Search, Social e Commerce](/help/search-social-commerce/tracking/tracking-about.md).&quot;

1. Configurare le integrazioni con prodotti aggiuntivi:

   1. (Per gli inserzionisti che fanno uso di Adobe Analytics e/o Adobe Audience Manager) Configura integrazioni tra i vari account in modo che Adobe Advertising possa scambiare dati con loro.

      Consulta la guida su &quot;[Integrazioni con CX Enterprise](/help/integrations/home.md)&quot;.

   1. (Inserzionisti con [!DNL Google Analytics]) Sincronizza le metriche di conversione per un account [!DNL Google Analytics], una proprietà e una combinazione di visualizzazioni per l&#39;ottimizzazione e il reporting.

      Questa configurazione utilizza l’interfaccia utente legacy. Consulta &quot;[Informazioni sulla sincronizzazione [!DNL Google Analytics] metriche di conversione](/help/search-social-commerce/legacy-ui/admin/data-sources/data-source-about.md)&quot; e, se necessario, [passa all&#39;interfaccia legacy](ui-switch.md).

1. (Facoltativo) Imposta e avvia i portfolio:

   1. In [!UICONTROL Goals] > [!UICONTROL Conversions], [controlla le metriche di conversione e rendi visibili le metriche richieste](/help/search-social-commerce/goals/conversions/conversion-metrics-manage.md#conversion-metrics-change-available). In [!UICONTROL Goals] > [!UICONTROL Objectives], [crea o seleziona un obiettivo](/help/search-social-commerce/goals/objectives/objective-about.md) per l&#39;ottimizzazione.

   1. In [!UICONTROL Manage] > [!UICONTROL Portfolios], [crea portfolio](/help/search-social-commerce/manage/portfolios/portfolio-create.md) configurati per soddisfare l&#39;obiettivo e gli obiettivi aziendali, con le [campagne idonee](/help/search-social-commerce/manage/campaigns/campaign-manage.md#campaign-portfolio) appropriate. [Attiva i portfolio](/help/search-social-commerce/manage/portfolios/portfolio-change-status.md) per raccogliere e modellare i dati. Il team di implementazione raccoglie e convalida i dati dei clic e dei ricavi per almeno 14 giorni e convalida le impostazioni del portfolio.

      >[!NOTE]
      >
      >Search, Social e Commerce tengono comunque traccia dei dati e li segnalano per le campagne che non sono assegnate a portfolio, ma che non forniscono l’ottimizzazione.

   1. Una volta disponibili dati sufficienti per creare una linea di base, il team può [cambiare lo stato del portfolio in ottimizzato](/help/search-social-commerce/manage/portfolios/portfolio-change-status.md), consentendo a Search, Social e Commerce di ottimizzare offerte, budget e/o obiettivi di strategia di offerta per il portfolio, in base al tipo di portfolio e alle strategie di offerta della campagna.

   Consulta &quot;[Informazioni sui portfolio](/help/search-social-commerce/manage/portfolios/portfolio-about.md)&quot; per informazioni sul supporto dell&#39;ottimizzazione e sugli stati dei portfolio.

1. Monitora le prestazioni dei portfolio:

   1. Utilizza [!UICONTROL Dashboard] > [!UICONTROL Overview] per [esaminare le tendenze del portfolio](/help/search-social-commerce/dashboard/dashboard-overview.md) e [visualizzare i dettagli delle prestazioni del portfolio](/help/search-social-commerce/manage/portfolios/portfolio-details.md) per analizzare i risultati e la precisione del modello.

   1. [Imposta avvisi personalizzati](/help/search-social-commerce/common-tasks/alerts-manage.md) e [genera rapporti personalizzati](/help/search-social-commerce/reports/management/report-manage.md) per il monitoraggio delle prestazioni. Quando necessario, automatizza la generazione di rapporti utilizzando [modelli di rapporti](/help/search-social-commerce/reports/report-templates-manage.md) e [feed di fogli di calcolo](/help/search-social-commerce/reports/spreadsheet-feeds-manage.md).

   Per ulteriori informazioni, consulta &quot;[Monitorare le prestazioni della campagna e del portfolio](/help/search-social-commerce/manage/manage-about.md#monitor-performance).&quot;

1. (Facoltativo) Configura le [visualizzazioni dati delle prestazioni](/help/search-social-commerce/common-tasks/data-views/data-views-about.md) per visualizzare i dati che desideri visualizzare.

## Attività in corso

Dopo il lancio iniziale, sono necessarie le seguenti attività in corso. A seconda dei termini del tuo contratto, [!DNL Adobe], un&#39;agenzia affiliata o l&#39;inserzionista esegue le seguenti attività:

* Continua a monitorare e analizzare le prestazioni di ciascun portfolio visualizzando avvisi, dati sulle prestazioni per ciascun portfolio e le relative campagne dei componenti, rapporti personalizzabili e simulazioni (alcuni ruoli).

* Regola le varie strategie e impostazioni utilizzate per gestire il set di portfolio, se necessario, in base alle prestazioni effettive e previste del portfolio e alle opportunità di crescita:

  * Regola i budget del portfolio, gli obiettivi e altre impostazioni.

  * Modifica le strutture account/campagne per adattarle ai cambiamenti nella strategia di marketing.

  * Aggiungere, mettere in pausa ed eliminare componenti della campagna. Questo può includere l’espansione dei set di parole chiave basati sull’analisi dei termini di ricerca e la verifica delle pagine di destinazione e di copia degli annunci.

  * Aggiornare le strategie di targeting geografico e del sito in base a rapporti sulle prestazioni avanzati.

  * (Facoltativo) Aggiungi vincoli di offerta alle singole parole chiave di ricerca o a tutte le parole chiave in un gruppo di annunci, una campagna o un portfolio.

  * Aggiungere nuovi portfolio.

Per istruzioni sul monitoraggio delle campagne e dei portfolio e sulla regolazione delle relative impostazioni, vedere &quot;[Informazioni sulla gestione delle campagne e dei portfolio](/help/search-social-commerce/manage/manage-about.md)&quot; e &quot;[Modifica dettagli portfolio](/help/search-social-commerce/manage/portfolios/portfolio-edit.md)&quot;.
