---
title: Implementare [!DNL Naver] account di solo tracciamento
description: Scopri come impostare campagne di tracciamento per il tuo [!DNL Naver] account in modo da poter tracciare, creare rapporti e visualizzare le prestazioni per gli annunci acquistati direttamente dalla rete di annunci.
source-git-commit: c4848da6c5489a5128a0424eef6a12f2c51caa12
workflow-type: tm+mt
source-wordcount: '686'
ht-degree: 0%

---

# Implementare [!DNL Naver] account di solo tracciamento

*[!DNL Naver]solo account*

Puoi creare campagne di tracciamento per il tuo [!DNL Naver] account in modo da poter tracciare, creare rapporti e visualizzare le prestazioni per gli annunci acquistati direttamente dalla rete di annunci. Search, Social e Commerce non sincronizzano i dati con la rete di annunci, non caricano automaticamente il tracciamento e non fanno offerte per l’account.

Le campagne di tracciamento replicano campagne, gruppi di annunci e parole chiave esistenti. Dopo aver creato la struttura dell’account in Search, Social e Commerce e aggiunto il tracciamento alle campagne originali all’interno della rete di annunci, puoi caricare le metriche del traffico di rete giornaliero per le parole chiave o gli annunci. Search, Social e Commerce possono quindi attribuire le conversioni agli annunci e alle parole chiave.

Puoi tenere traccia delle metriche delle prestazioni in tutte le campagne e per ogni singola campagna, gruppo di annunci o parola chiave/annuncio. Puoi anche includere informazioni su di loro nella maggior parte dei rapporti di base, avanzati e di assistenza, insieme ai dati per le altre reti di annunci. Il supporto per l’esportazione delle metriche in Adobe Analytics non è disponibile, ma Search, Social &amp; Commerce può essere sincronizzato [metriche in cui stai tracciando [!DNL Analytics]](/help/integrations/analytics/analytics-data-in-advertising.md) in Search, Social e Commerce.

>[!NOTE]
>
>Non puoi aggiungere campagne di tracciamento a un portfolio per l’ottimizzazione.

1. Crea campagne di tracciamento in Search, Social &amp; Commerce:

   1. Crea [dettagli account di rete fittizio](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md). Se in una singola rete di annunci sono presenti più account, consolidarli in un unico account in [!UICONTROL Accounts] visualizzazione.

      [!DNL Naver] non fornisce il supporto API per caricare i parametri di tracciamento nella rete di annunci. Tuttavia, puoi generare parametri di tracciamento utilizzando i bulksheet e aggiungerli manualmente all’interno della rete di annunci (per il passaggio 2). Per generare i parametri di tracciamento, devi utilizzare il &quot;[!UICONTROL EF Redirect]&quot; metodo di tracciamento. Facoltativamente, puoi aggiungere i parametri di accodamento desiderati.

      Search, Social e Commerce includono automaticamente il parametro `ev_cl={ef_uniqueid}` in qualsiasi URL di tracciamento generato all’interno di bulksheet per l’account. Questo ID univoco viene utilizzato per far corrispondere i dati della campagna con qualsiasi costo e i dati dei clic caricati.

   1. Configura le campagne per il tracciamento:

      1. All’interno della rete di annunci, crea un file bulksheet contenente tutte le entità, e le relative entità principali, che desideri che Search, Social e Commerce tengano traccia dell’account.

         Puoi includere dati sulle parole chiave, incluse le campagne principali e i gruppi di annunci.

      1. Se necessario, modifica il file del bulksheet in modo che segua le istruzioni Search, Social e Commerce. [formato di bulksheet richiesto per [!DNL Naver] account](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md).

      1. In Ricerca, Social E Commerce, [carica il file bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md).

         >[!NOTE]
         >
         >Nota: Search, Social e Commerce non pubblicano i dati sull’account di rete dell’annuncio.

1. Configura il tracciamento per le campagne:

   1. In Ricerca, Social E Commerce, [scarica un nuovo file bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) utilizzo dell’opzione per &quot;[!UICONTROL Generate Tracking URLs].&quot;
   Utilizzo di &quot;[!UICONTROL Generate Tracking URLs]L’opzione &quot; compila il [!UICONTROL Destination URL] per ogni parola chiave con il codice di tracciamento di Search, Social e Commerce preceduto dal prefisso [!UICONTROL Base URL] valore.

   Di seguito è riportato un esempio dell’URL di destinazione con tracciamento:

   ```http://pixel.everesttech.net/1234/cq?ev_sid=87&ev_cl=258e27dcec70156a667f2229020e488&url=http%3A//www.example.com```

   1. Copia il [!UICONTROL Destination URL] i valori nel file di bulksheet scaricato alle relative impostazioni delle parole chiave della rete.

      Puoi aggiungere gli URL alle entità rilevanti caricando il file nella rete all’interno dell’editor della rete di annunci. In tal caso, potrebbe essere necessario rimuovere alcune colonne, in base ai requisiti di dati della rete. In caso contrario, è necessario immettere manualmente gli URL nella rete.


1. Scarica periodicamente i dati su clic e i costi aggregati quotidianamente dalla rete di annunci per le parole chiave o gli annunci pubblicitari a livello di gruppo di annunci che stai tracciando, quindi [carica i dati di clic e costo](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md) per eseguire ricerche, social e commerce in [formato richiesto](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-data-requirements.md).

   Includi la gerarchia completa dell’account ed eventuali metriche da includere. Search, Social e Commerce confrontano i dati caricati con i dati delle campagne esistenti.

1. (Facoltativo) Se utilizzi i tag del servizio di tracciamento delle conversioni di Adobe Advertising nelle tue pagine web per tracciare le conversioni che non vengono tracciate sulla rete di annunci, invia file di feed contenenti dati di conversione aggregati su base giornaliera da aggiungere alle campagne di tracciamento.

   Per ulteriori informazioni, contatta il team del tuo account Adobe.

Tutti i dati di tracciamento caricati sono disponibili da [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] all&#39;interno del [!UICONTROL Accounts], [!UICONTROL Campaigns], [!UICONTROL Ad Groups], e [!UICONTROL Keywords] visualizzazioni. È disponibile anche per i report in [!UICONTROL Insights & Reports] visualizzazione.

>[!MORELIKETHIS]
>
>* [Appendice - Dati di bulksheet richiesti per [!DNL Naver] account](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md)
>* [Caricare traffico e metriche di conversione per [!DNL Naver] account di solo tracciamento](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md)
>* [Requisiti dei dati delle metriche per [!DNL Naver] account di solo tracciamento](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-data-requirements.md)
>* [Formati di tracciamento dei clic per [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)

