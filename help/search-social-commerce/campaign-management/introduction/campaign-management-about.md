---
title: Informazioni sulla gestione delle campagne in Search, Social e Commerce
description: Scopri le funzioni di gestione delle campagne in Search, Social e Commerce.
exl-id: 19e36e73-fcb6-4ff3-980b-fc05042725fd
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '806'
ht-degree: 0%

---

# Informazioni sulla gestione delle campagne in Search, Social e Commerce

Search, Social e Commerce consente di monitorare e/o gestire in un’unica posizione le campagne Search, Display/Content, Social, Shopping, Audience e Performance Max. A seconda della rete e del tipo di campagna dell’annuncio, le funzionalità disponibili possono includere la sincronizzazione con le reti dell’annuncio, la creazione e la modifica di funzionalità, il tracciamento e l’attribuzione della conversione, la generazione di rapporti e l’ottimizzazione di offerte e budget. Per informazioni dettagliate sulle funzionalità disponibili per ogni rete di annunci, vedi &quot;[Inventario supportato](/help/search-social-commerce/introduction/supported-inventory.md).&quot;

Quando si aggiungono e si modificano i dati della campagna nelle visualizzazioni [!UICONTROL Campaigns], Search, Social e Commerce inviano immediatamente le modifiche dei dati alla rete di annunci. Search, Social e Commerce estraggono inoltre i dati della struttura della campagna e i dati sui clic dagli account di rete di annunci sincronizzati una volta al giorno (o più spesso quando vengono rilevate nuove campagne) e su richiesta, in base alle richieste.

## Impostazione dell’accesso agli account di rete degli annunci

Per tenere traccia delle prestazioni degli annunci nell&#39;account di rete dell&#39;inserzionista (e per presentare offerte per gli annunci), il team dell&#39;account dell&#39;Adobe [crea un record dell&#39;account corrispondente](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) in Search, Social e Commerce. Il record account include opzioni di verifica.

Per gli account sincronizzati tramite l’API della rete di annunci, il record account include anche le credenziali di accesso all’account. Una volta che l’account è abilitato, i dati dell’account vengono estratti da con la rete di annunci. Puoi quindi visualizzare i dati dell’account esistenti nonché creare e modificare la struttura della campagna e i dati dell’annuncio.

## Tracciamento dei clic per collegare i clic alle conversioni

Se utilizzi il servizio di tracciamento delle conversioni di Adobe Advertising, devi includere il codice di tracciamento dei clic di Search, Social e Commerce nel suffisso della pagina di destinazione, nei modelli di tracciamento e negli URL finale/di destinazione per annunci, parole chiave, posizionamenti, sitelink e elenchi di prodotti. Per [reti di annunci e tipi di campagne supportati](/help/search-social-commerce/introduction/supported-inventory.md) le cui impostazioni della campagna includono &quot;[!UICONTROL EF Redirect]&quot; e &quot;[!UICONTROL Auto Upload]&quot;, Search, Social e Commerce aggiungono automaticamente il proprio codice di reindirizzamento e di tracciamento quando si salva il record, pertanto non è necessario aggiungerlo manualmente. In caso contrario, devi aggiungere manualmente il codice ai modelli di tracciamento o agli URL finali.

Per ulteriori informazioni sul tracciamento, consulta il capitolo su &quot;Tracciamento&quot;.

## Automazione delle offerte e della gestione del budget

Per [reti di annunci e tipi di campagne supportati](/help/search-social-commerce/introduction/supported-inventory.md), puoi raggruppare le campagne in portfolio, ciascuno con un obiettivo di business specifico e un target di budget o prestazioni specifico. Nei portfolio standard, Search, Social e Commerce ottimizzano le offerte basate su parole chiave CPC e il budget delle campagne. I portfolio ibridi combinano tecnologie di ottimizzazione provenienti da Search, Social e Commerce con le reti di annunci.

Per ulteriori informazioni sulle opzioni di portfolio disponibili e sulla configurazione dei portfolio, vedere il capitolo della Guida all&#39;ottimizzazione relativo ai Portfoli, disponibile in Search, Social e Commerce.<!-- verify convention for referencing Optimization Guide here -->

## Visualizzazioni di gestione delle campagne

Le viste di gestione della campagna consentono di monitorare e gestire gli account di ricerca. Sono disponibili le seguenti viste:

* **[!UICONTROL Campaigns]** — Le visualizzazioni di [!UICONTROL Campaigns] mostrano i dati di ogni account di rete di annunci connesso. Puoi visualizzare i dati su costi, clic, impression e ricavi per tutti gli account di rete di annunci e per singoli account, campagne, gruppi di annunci, parole chiave, annunci, gruppi di prodotti per la spesa, posizionamenti, destinazioni automatiche (target di ricerca dinamici), tipi di pubblico e librerie di estensioni di annunci e le entità account associate. Per [tipi di campagne supportati nelle reti di annunci supportate](/help/search-social-commerce/introduction/supported-inventory.md), puoi creare e modificare i dati per le singole campagne e i singoli componenti della campagna direttamente nell&#39;interfaccia. Facoltativamente, è possibile esportare i dati nella maggior parte delle visualizzazioni secondarie in un file del foglio di calcolo.

  >[!NOTE]
  >
  >I dati a livello di annuncio non sono disponibili per [!DNL Google Ads] campagne Dynamic Search Ad (DSA), performance max, smart shopping e [!DNL YouTube].

* **[!UICONTROL Products]** — Le visualizzazioni [!UICONTROL Products] mostrano i dati per ogni account [[!DNL Google] o [!DNL Microsoft] centro commerciale sincronizzato](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). Nella visualizzazione secondaria predefinita [!UICONTROL Accounts] sono elencati tutti gli account sincronizzati. Alcuni tipi di utente possono aggiungere nuovi account da questa visualizzazione. Nella visualizzazione secondaria [!UICONTROL Products] sono elencati tutti i prodotti inclusi nell&#39;account.

* **[!UICONTROL Advanced (ACM)]** — Dalla vista [!DNL Advanced] ([!DNL AMC], per Campaign Management avanzato), è possibile impostare processi automatizzati per la creazione di [annunci dinamici e parole chiave indirizzati a ogni elemento nel proprio inventario](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) in base a un modello di annunci specifico per la rete di annunci creato e al contenuto di [!DNL Google Merchant Center] account o file di dati di inventario caricati in un percorso FTP. Le anteprime mostrano i dettagli di ogni modello di feed per l’inserzionista e di ogni campagna, gruppo di annunci, parola chiave e annuncio incluso in un feed propagato tramite un modello di feed ma non pubblicato nella rete di annunci.

* **[!UICONTROL Bulksheets]** - Utilizzare la visualizzazione [!UICONTROL Bulksheets] per creare [file bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) contenenti la quantità di dati desiderata per un account in una [rete di annunci supportata](/help/search-social-commerce/introduction/supported-inventory.md), quindi inviarli alla rete di annunci.

* **[!UICONTROL Audiences]** — [Le [!UICONTROL Audiences] visualizzazioni](/help/search-social-commerce/campaign-management/campaigns/audience-about.md) elencano tutti i tipi di pubblico [!DNL Google Ads] e [!DNL Microsoft Advertising] generati da vari tipi di elenchi di utenti. Puoi creare [!DNL Google Ads] tipi di pubblico dai tuoi tipi di pubblico di Adobe Experience Cloud esistenti e dagli elenchi e-mail dei tuoi clienti. Puoi anche visualizzare e gestire i target e le esclusioni del pubblico per gli annunci [!DNL Google Ads] e [!DNL Microsoft Advertising].

* **[!UICONTROL Label Classifications]** - Utilizzare questa visualizzazione per creare ed eliminare [classificazioni di etichette](/help/search-social-commerce/campaign-management/label-classifications/classification-about.md), che possono essere utili per raggruppare le etichette in insiemi significativi.

>[!MORELIKETHIS]
>
>* [Panoramica sull&#39;implementazione di account e campagne di ad network](campaign-implemention-overview.md)
>* [Monitora e gestisci le prestazioni delle campagne della rete di annunci](monitor-performance-campaigns.md)
>* [Dati di conversione di Google Ads in Search, Social e Commerce](google-conversion-data.md)
