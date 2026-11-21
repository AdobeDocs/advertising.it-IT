---
title: Informazioni sulla gestione di campagne e portfolio
description: Scopri come gli account di rete e le campagne, il tracciamento e l’ottimizzazione del portfolio funzionano insieme e come monitorare e migliorare le prestazioni.
feature: Search Campaign Management, Search Portfolios
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
  - id: 893a7eac-45bd-56c2-a120-18db6d297dcc
    internal-label: Search Portfolios
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 76a8d8b448441e4d7380ebc4f007aa8b5a2ab5f5
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 0%
---
# Informazioni sulla gestione di campagne e portfolio

*funzionalità Beta*

Search, Social e Commerce riuniscono in un&#39;unica interfaccia la gestione delle campagne, il reporting sulle prestazioni e l&#39;ottimizzazione del portafoglio. A seconda della rete di annunci e del tipo di campagna, puoi sincronizzare i dati della campagna, creare e modificare i componenti della campagna, tenere traccia delle conversioni e ottimizzare le offerte, i budget o gli obiettivi della strategia di offerta. Consulta [inventario supportato](/help/search-social-commerce/introduction/supported-inventory.md) per le funzionalità disponibili per ogni rete di annunci.

Il menu [!UICONTROL Manage] consente di accedere agli account, alle campagne, ai gruppi di annunci, agli annunci, alle parole chiave, ai gruppi di prodotti e ai portfolio. Le autorizzazioni dell&#39;utente determinano le visualizzazioni e le azioni disponibili. Per l&#39;organizzazione completa dei menu, vedere &quot;[Organizzazione dell&#39;interfaccia utente](/help/search-social-commerce/getting-started/user-interface.md).&quot;

## Integrazione di account, campagne e portfolio

* **Account di rete di annunci** connetti i dati dell&#39;inserzionista a Search, Social e Commerce. [I tipi di account](/help/search-social-commerce/manage/accounts/ad-network-account-about.md) includono gli account sincronizzati tramite una connessione API, gli account per i quali si caricano i dati e gli account di solo tracciamento basati su modelli. Il tipo di account determina se è possibile sincronizzare i dati, gestire le campagne o utilizzare l’ottimizzazione del portfolio.

* **Le campagne** contengono gli annunci e altri componenti utilizzati per distribuire la pubblicità. Per i tipi di campagna supportati, puoi [creare e gestire campagne](/help/search-social-commerce/manage/campaigns/campaign-manage.md) e i relativi componenti dalle visualizzazioni [!UICONTROL Manage]. È inoltre possibile utilizzare [bulksheet](/help/search-social-commerce/set-up/bulksheets/about.md) per operazioni di massa supportate.

* **I portfolio** raggruppano le campagne idonee per ottimizzarle in base a un obiettivo di business e un target di budget o prestazioni comuni. Una campagna può appartenere a un solo portfolio e tutte le campagne in un portfolio devono utilizzare la stessa valuta. Consulta &quot;[Informazioni sui portfolio](/help/search-social-commerce/manage/portfolios/portfolio-about.md).&quot;

L&#39;assegnazione di Portfolio è facoltativa. Puoi tenere traccia delle campagne e generare rapporti sulle stesse senza assegnarle a un portfolio. Non tutte le reti di annunci, i tipi di campagne o le strategie di offerta supportano l’ottimizzazione del portafoglio.

## Sincronizzare i dati della campagna

Per gli account connessi tramite un’API, Search, Social e Commerce recuperano la struttura della campagna supportata e i dati sulle prestazioni dalla rete di annunci. Le modifiche apportate ai componenti di Campaign supportati in Search, Social e Commerce vengono inviate alla rete di annunci.

Se necessario, è possibile [richiedere una sincronizzazione manuale](/help/search-social-commerce/manage/accounts/api-accounts/sync-api-accounts.md). Se un account smette di sincronizzarsi, rivederne [l&#39;autenticazione e lo stato di accesso](/help/search-social-commerce/manage/accounts/api-accounts/api-account-manage.md#authentication-status).

Gli account di caricamento dati e gli account di solo tracciamento non vengono sincronizzati con la rete di annunci. Segui il flusso di lavoro per il tipo di account [](/help/search-social-commerce/manage/accounts/ad-network-account-about.md) per fornire dati sulla campagna e sulle prestazioni.

## Configurare il tracciamento e l’ottimizzazione

[Il tracciamento](/help/search-social-commerce/tracking/tracking-about.md) collega l&#39;attività della campagna alle conversioni rilevanti per la tua azienda. A seconda dell’implementazione, i dati di conversione possono provenire dai tag di Adobe Advertising, da un’integrazione di Adobe Analytics, dal tracciamento della rete di annunci o dai feed di dati. Configura il tracciamento dei clic e il tracciamento delle conversioni in base alle esigenze della tua implementazione e convalida i dati prima di utilizzarli per l’ottimizzazione.

In [!UICONTROL Goals] > [!UICONTROL Conversions], puoi [rivedere le metriche di conversione tracciate per l&#39;inserzionista e controllarne la visibilità](/help/search-social-commerce/goals/conversions/conversion-metrics-manage.md). Utilizza le metriche appropriate nei tuoi [obiettivi](/help/search-social-commerce/goals/objectives/objective-about.md).

Per abilitare l&#39;ottimizzazione del portfolio, [crea un portfolio](/help/search-social-commerce/manage/portfolios/portfolio-create.md), assegna una campagna obiettiva e idonea e configurane le impostazioni di spesa e ottimizzazione. Un portfolio attivo raccoglie e modella i dati sulle prestazioni. Quando i dati e le impostazioni sono pronti, [imposta lo stato del portfolio su ottimizzato](/help/search-social-commerce/manage/portfolios/portfolio-change-status.md) per iniziare l&#39;ottimizzazione. Le azioni eseguite dipendono dal tipo di portfolio e dalle [strategie di offerta della campagna](/help/search-social-commerce/manage/portfolios/portfolio-about.md#optimization-by-bid-strategy).

Per informazioni dettagliate sulla sequenza di installazione, vedere &quot;[Configurare account e campagne di ad network](/help/search-social-commerce/getting-started/campaign-implementation-overview.md).&quot;

## Monitorare le prestazioni di campagne e portfolio {#monitor-performance}

Il team dell&#39;account, l&#39;agenzia o l&#39;inserzionista è responsabile del monitoraggio delle prestazioni e dell&#39;esecuzione delle modifiche in base ai termini del contratto di assistenza. Di routine:

* Verificare le prestazioni della campagna e dell&#39;account nelle visualizzazioni [!UICONTROL Manage]. [Personalizza colonne, filtri e intervalli di date](/help/search-social-commerce/common-tasks/data-views/data-views-about.md) per concentrarti sulle metriche e sulle entità rilevanti.

* Utilizza [!UICONTROL Dashboard] > [!UICONTROL Overview] per [monitorare le tendenze del portfolio e le modifiche nelle prestazioni](/help/search-social-commerce/dashboard/dashboard-overview.md).

* Rivedi [avvisi personalizzati](/help/search-social-commerce/common-tasks/alerts-manage.md) per le condizioni che richiedono un&#39;indagine.

* [Genera report](/help/search-social-commerce/reports/management/report-manage.md) per le prestazioni di campagne, parole chiave, annunci pubblicitari e portfolio. Per i portfolio, [controlla i dettagli delle prestazioni](/help/search-social-commerce/manage/portfolios/portfolio-details.md), incluse le prestazioni effettive e la precisione del modello.

* Utilizza [simulazioni](/help/search-social-commerce/plan/simulations/simulation-about.md), se disponibili, per valutare gli effetti previsti di diversi livelli di spesa.

* Esamina le differenze tra le conversioni riportate e i dati di origine. Consulta le linee guida per i dati di conversione [!DNL Google Ads] e [!DNL Microsoft Advertising] nei collegamenti correlati.

## Regolare campagne e portfolio

In base alle prestazioni e ai cambiamenti negli obiettivi aziendali, potrebbe essere necessario:

* Modifica le impostazioni della campagna, crea o sospendi i componenti della campagna, perfeziona i set di parole chiave o testa diversi annunci. Le azioni disponibili dipendono dalla rete di annunci e dal tipo di campagna.

* Rivedi il targeting geografico, di pubblico e di posizionamento utilizzando le visualizzazioni e i rapporti di gestione pertinenti.

* [Modifica le assegnazioni della campagna](/help/search-social-commerce/manage/campaigns/campaign-manage.md#campaign-portfolio) quando una campagna deve essere ottimizzata con un portfolio diverso. L’assegnazione di una campagna a un altro portfolio la rimuove dal portfolio precedente.

* [Modifica le impostazioni del portfolio](/help/search-social-commerce/manage/portfolios/portfolio-edit.md), inclusi i controlli di obiettivo, strategia di spesa, vincoli o ottimizzazione consentiti dal tuo profilo di prodotto.

* Rivedi [cronologia modifiche](/help/search-social-commerce/reports/history-logs.md) durante l&#39;analisi delle modifiche delle prestazioni.

>[!MORELIKETHIS]
>
>* [Configurare account e campagne di rete di annunci](/help/search-social-commerce/getting-started/campaign-implementation-overview.md)
>* [Inventario supportato](/help/search-social-commerce/introduction/supported-inventory.md)
>* [[!DNL Google Ads] dati di conversione in Search, Social e Commerce](/help/search-social-commerce/tracking/google-conversion-data.md)
>* [[!DNL Microsoft Advertising] dati di conversione in Search, Social e Commerce](/help/search-social-commerce/tracking/microsoft-conversion-data.md)
