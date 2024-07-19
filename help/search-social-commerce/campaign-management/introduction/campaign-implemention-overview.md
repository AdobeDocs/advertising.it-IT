---
title: Panoramica dell’implementazione di account e campagne di ad network
description: Scopri le attività necessarie per configurare, sincronizzare e gestire gli account di rete degli annunci.
exl-id: 36307e65-81f8-4794-8a75-a37623b294ed
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '966'
ht-degree: 0%

---

# Panoramica dell’implementazione di account e campagne di ad network

Adobe collabora con ogni inserzionista per configurare i suoi account e le sue campagne di rete pubblicitaria. Ciò include la configurazione di Search, Social e Commerce per la connessione e la sincronizzazione con gli account dell’inserzionista, la creazione di nuove campagne e componenti della campagna in base alle esigenze, l’impostazione del tracciamento per gli annunci dei componenti, l’aggiunta facoltativa delle campagne ai portfolio per consentire a Search, Social e Commerce di ottimizzare l’offerta sugli annunci e la convalida dei dati iniziali su costo, clic e ricavo.

Dopo l’attivazione di una campagna e l’eventuale aggiunta a un portfolio, il team di gestione dell’account Adobe, il team dell’agenzia o l’inserzionista (a seconda dei termini del contratto del livello di servizio) dovranno monitorare ogni campagna e modificare i componenti e le impostazioni rilevanti in base alle necessità per soddisfare gli obiettivi dell’inserzionista.

Questa pagina include informazioni su tutti i tipi di account, inclusa la modalità di impostazione della struttura delle campagne per gli account sincronizzati. Per ulteriori istruzioni sulla configurazione di account di sola verifica per [!DNL Naver], vedere &quot;[Implementare [!DNL Naver] account di sola verifica](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md).&quot;

## Attività di configurazione iniziali per account e campagne

[!DNL Adobe] e/o la tua agenzia collaboreranno con te per eseguire le seguenti operazioni:

1. (Nuovi account inserzionista) Imposta account amministrativi:

   1. Configura l&#39;account dell&#39;inserzionista.

   1. Se necessario, crea account utente per l’inserzionista per visualizzare e gestire i dati della campagna e generare rapporti.

1. (Alcune reti di annunci) Ottieni l’autorizzazione Search, Social e Commerce per accedere a ciascun account utilizzando l’API della rete di annunci e l’interfaccia utente Search, Social e Commerce.

1. Per ogni account di rete di annunci:

   1. Se necessario, imposta l’account sulla rete di annunci.

   1. Integrare con l&#39;account [creando un record dell&#39;account corrispondente](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md#create-account) in Search, Social e Commerce contenente le credenziali di accesso e le opzioni di verifica dell&#39;account e impostare lo stato dell&#39;account su abilitato.

      Search, Social e Commerce si sincronizzano quindi con la rete di annunci. Se l’account contiene già dati della campagna, i dati sono disponibili in circa 24 ore.

   1. ([Tipi di annuncio che è possibile creare/modificare](/help/search-social-commerce/introduction/supported-inventory.md) in Search, Social e Commerce) Se l&#39;account non contiene già dati della campagna, creare la struttura della campagna e i componenti della campagna da Search, Social e Commerce utilizzando uno dei metodi seguenti disponibili per il tipo di annuncio:

      * (Google Ads, Microsoft Advertising, Yahoo! Solo annunci e account Yandex) Imposta un [processo automatizzato per creare annunci dinamici e parole chiave mirati a ogni elemento nel tuo inventario](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) in base a un modello di annunci specifico per la rete di annunci creato e al contenuto dei file di dati di inventario caricati in un percorso FTP.

      * (Baidu, Google Ads, Microsoft Advertising, Yahoo! Japan Ads e solo account Yandex) Carica [file di bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) contenenti la quantità di dati desiderata per un account e poi li invia alle reti di annunci.

      * (Baidu, Google Ads, Microsoft Advertising, Yahoo! Japan Ads e (solo per gli account Yandex). Immetti i dati per i singoli componenti direttamente nell’interfaccia. Per la maggior parte delle campagne e dei tipi di annunci, puoi creare dati a livello di campagna, di gruppo di annunci e a livello di singola parola chiave, posizionamento e annuncio.

      Alcuni tipi di campagne e annunci, tuttavia, richiedono flussi di lavoro univoci. Consulta le istruzioni per la configurazione di [[!DNL Microsoft Advertising] campagne acquisti](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md), [[!DNL Google Ads] annunci ricerca dinamica](/help/search-social-commerce/campaign-management/special-campaign-types/google-dynamic-search-ads.md), [[!DNL Google Ads] campagne prestazioni massime](/help/search-social-commerce/campaign-management/special-campaign-types/google-performance-max-campaigns.md) e [[!DNL Google Ads] campagne acquisti](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md).

   1. ([!DNL Naver] solo account di sola verifica) Carica [file bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) con dati per replicare campagne, gruppi di annunci e parole chiave esistenti in Search, Social e Commerce senza pubblicarli in [!DNL Naver].

1. Imposta il tracciamento per tutti gli annunci per i quali l’Adobe Advertising terrà traccia delle conversioni:

   1. (Per gli inserzionisti con il servizio di monitoraggio delle conversioni di Adobe Advertising) Se necessario, [imposta il monitoraggio dei clic](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md) per gli annunci e, facoltativamente, per parole chiave, posizionamenti ed estensioni di annunci, generando e caricando URL di monitoraggio dei clic di Search, Social e Commerce.

      Per [!DNL Google Ads] campagne con prestazione massima, imposta tutto il tracciamento nelle [impostazioni di tracciamento della campagna](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md).

1. Per le campagne di solo tracciamento, devi invece generare gli URL di destinazione utilizzando i bulksheet, quindi aggiungere gli URL di destinazione generati alle entità pertinenti utilizzando l’editor nativo della rete di annunci.

   1. Imposta il tracciamento delle conversioni. A seconda dell’implementazione, ciò può comportare l’aggiunta di tag di tracciamento della conversione alle pagine web dell’inserzionista e/o l’impostazione di un rilascio giornaliero di feed per i dati di conversione raccolti separatamente dall’inserzionista.

      Se utilizzi il servizio di monitoraggio delle conversioni di Adobe Advertising, puoi generare i tag di monitoraggio delle conversioni [in Search, Social e Commerce](/help/search-social-commerce/tools/conversion-tag-generate.md) o [utilizzando Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud.html).

   1. Convalida i dati tracciati.

   Per ulteriori dettagli sulla configurazione del tracciamento, consulta il capitolo su &quot;Tracciamento&quot;.

1. (Inserzionisti con Adobe Analytics) [Integra Adobe Advertising e Analytics](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) in modo che possano scambiare dati.

1. (Per consentire a Search, Social e Commerce di ottimizzare le offerte e/o i budget delle campagne; solo [tipi di campagna supportati](/help/search-social-commerce/introduction/supported-inventory.md)) [Assegna la campagna a un portfolio](/help/search-social-commerce/campaign-management/campaign-assign-to-portfolio.md).

   Se il portfolio non è già stato avviato (ottimizzazione di offerte e/o budget), lascia che la funzionalità di ottimizzazione raccolga dati sufficienti per creare modelli di costi e ricavi in modo da poter stabilire le prestazioni linea di base per il portfolio prima di avviarlo.

   Se il portfolio è già stato avviato, abilita l’apprendimento per il portfolio. Per ulteriori informazioni, vedere &quot;Regolazione delle strategie di portfolio&quot;. Dopo l’aggiunta di nuove campagne, il portfolio sarà volatile, mentre la funzionalità di ottimizzazione raccoglie i dati sulle unità di offerta della campagna. L&#39;offerta si regola automaticamente entro una o tre settimane.

   Per ulteriori informazioni sui portfolio, vedere la Guida all&#39;ottimizzazione, disponibile in Search, Social e Commerce.<!-- verify convention for referencing Optimization Guide here -->

1. (Se verranno tracciate nuove conversioni per l&#39;inserzionista) [Rendere disponibili le conversioni](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) per report, visualizzazioni di gestione campagne e obiettivi di portfolio.

1. Per ogni campagna, verifica che Search, Social e Commerce ricevano i dati relativi ai clic e ai costi dalla rete di annunci e convalida i dati sui ricavi mostrati in Search, Social e Commerce con i dati sui ricavi dell’inserzionista.

1. (Facoltativo) Automatizza la generazione di rapporti configurando modelli di rapporti, feed di fogli di calcolo e distribuzione FTP di rapporti pianificati.

   Per istruzioni, consulta il capitolo su &quot;Rapporti&quot;.

>[!MORELIKETHIS]
>
>* [Informazioni sulla gestione delle campagne in Search, Social e Commerce](campaign-management-about.md)
>* [Monitora e gestisci le prestazioni delle campagne della rete di annunci](monitor-performance-campaigns.md)
>* [Dati di conversione di Google Ads in Search, Social e Commerce](google-conversion-data.md)
>* [Inventario supportato](/help/search-social-commerce/introduction/supported-inventory.md)
