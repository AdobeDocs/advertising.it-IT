---
title: Panoramica sull’implementazione di Search, Social e Commerce
description: Scopri
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '819'
ht-degree: 0%

---

# Panoramica sull’implementazione di Search, Social e Commerce

[!DNL Adobe] o una delle sue agenzie affiliate collabora con ogni inserzionista per lanciare i suoi portfolio di pubblicità online e per tenere traccia di eventuali campagne pubblicitarie aggiuntive. Dopo il lancio iniziale, ulteriori attività continuative garantiscono che gli obiettivi dell&#39;inserzionista continueranno a essere raggiunti.

Di seguito è riportato il flusso di lavoro generale per l’implementazione e l’utilizzo di Search, Social e Commerce.

## Lancio iniziale

[!DNL Adobe] e/o l’agenzia collabora con l’utente per eseguire le seguenti operazioni:

1. Valuta i tuoi obiettivi aziendali di alto livello e progetta strategie per raggiungerli:

   1. Identifica il tuo modello di business e gli obiettivi di marketing.

   1. Identificare i requisiti di tracciamento delle conversioni

   1. Analizza le strutture degli annunci pubblicitari online esistenti.

   1. Identifica le metriche per l’ottimizzazione e il reporting del portfolio.

1. (Utenti amministratori o account manager) Impostare account amministrativi:

   1. Configura l&#39;account dell&#39;inserzionista. Se un&#39;agenzia gestisce i dati dell&#39;inserzionista, l&#39;account dell&#39;inserzionista deve essere associato all&#39;account dell&#39;agenzia.

   1. Se necessario, crea account utente per l’inserzionista per visualizzare e gestire i dati della campagna e generare rapporti.

   Per informazioni dettagliate sulla configurazione degli account, consulta il capitolo della guida su &quot;Amministratore&quot;.

1. Sincronizza con, o crea, campagne per ciascuno dei tuoi account di rete degli annunci:

   * Effettua la sincronizzazione con l’account a) creando un record dell’account corrispondente in Search, Social &amp; Commerce che contiene le credenziali di accesso e le opzioni di tracciamento dell’account e b) impostando lo stato dell’account su abilitato.

   * Se gli account non contengono già dati della campagna, aggiungi campagne, gruppi di annunci, parole chiave, annunci e posizionamenti da Search, Social e Commerce o dall’interno della rete di annunci.

      Per informazioni dettagliate sulla configurazione delle campagne di ricerca, consulta il capitolo della guida su &quot;Campaign Management&quot;.

1. Imposta il tracciamento per tutti gli annunci per i quali desideri che Adobe Advertising tenga traccia delle conversioni:

   1. (Se necessario) Imposta il tracciamento dei clic per gli annunci e, facoltativamente, per le parole chiave, [!DNL Google Ads] posizionamenti e [!DNL Google Ads] mediante la generazione e il caricamento di URL di tracciamento dei clic.

      Gli URL di tracciamento dei clic per gli inserzionisti con il servizio di tracciamento delle conversioni basato su pixel di Adobe Advertising includono un reindirizzamento a [!DNL Adobe] server.

   1. Imposta il tracciamento delle conversioni. A seconda dell’implementazione, potrebbe essere necessario aggiungere tag di tracciamento delle conversioni alle pagine web appropriate e/o impostare un rilascio di feed giornaliero per i dati di conversione raccolti utilizzando un metodo personalizzato.

      Per informazioni dettagliate sulla configurazione del tracciamento, consulta il capitolo della guida su &quot;Tracciamento&quot;.

1. Configurare le integrazioni con prodotti aggiuntivi:

   1. (Per gli inserzionisti che fanno uso di Adobe Analytics e/o Adobe Audience Manager) Configura integrazioni tra i vari account in modo che Adobe Advertising possa scambiare dati con essi.

      Consulta la guida su &quot;[Integrazioni con Experience Cloud](/help/integrations/home.md).&quot;

   1. (Per gli inserzionisti che [!DNL Google Analytics]a) Sincronizzare le metriche di conversione per un [!DNL Google Analytics] combinazione di account, proprietà e visualizzazione per l&#39;ottimizzazione e il reporting.

      Consulta il sottocapitolo della guida &quot;Amministratore&quot; > &quot;[Configurazione delle origini dati](/help/search-social-commerce/admin/data-sources/data-source-about.md).&quot;

1. Configurare e avviare i portfolio:

   1. Imposta i portfolio configurati per raggiungere l’obiettivo e gli obiettivi aziendali con le campagne appropriate. Il team di implementazione raccoglie e convalida i dati dei clic e dei ricavi per almeno 14 giorni e convalida le impostazioni del portfolio.

      >[!NOTE]
      >
      >Search, Social e Commerce tiene comunque traccia dei dati e li segnala per le campagne non assegnate a portfolio, ma non ottimizza le offerte per esse.

   1. Una volta che i dati sono sufficienti per creare una linea di base, il team può avviare il portfolio, consentendo a Search, Social e Commerce di ottimizzare offerte e/o budget per il portfolio, in base al tipo di ottimizzazione.
   Per informazioni dettagliate sulla configurazione e sul lancio dei portfolio, consulta la guida in linea di &quot;Ottimizzazione&quot;, accessibile dal [!UICONTROL Help] menu (![Menu Aiuto](/help/search-social-commerce/assets/help-main-menu.png "Menu Aiuto")) in alto a destra nelle pagine di Search, Social e Commerce.

1. Monitora le prestazioni dei portfolio:

   1. Genera informazioni sulla pubblicità, ossia dati visivi e actionable sui portfolio ottimizzati e attivi.

   1. Imposta e potenzialmente automatizza rapporti personalizzati per il monitoraggio delle prestazioni.

   Per informazioni dettagliate sull’esecuzione di informazioni sulla pubblicità e sulla configurazione dei rapporti, consulta il capitolo della guida su &quot;Approfondimenti e rapporti&quot;.

1. (Facoltativo) Configura il [visualizzazioni dati delle prestazioni](/help/search-social-commerce/common-tasks/data-views/data-views-about.md) per visualizzare i dati che si desidera visualizzare.

## Attività in corso

Dopo il lancio iniziale, sono necessarie le seguenti attività in corso. A seconda dei termini del tuo contratto, [!DNL Adobe], un&#39;agenzia affiliata o l&#39;inserzionista svolge i seguenti compiti:

* Continua a monitorare e analizzare le prestazioni di ciascun portfolio visualizzando avvisi, dati sulle prestazioni per ciascun portfolio e le relative campagne dei componenti, rapporti personalizzabili e simulazioni (alcuni ruoli).

* Regola le varie strategie e impostazioni utilizzate per gestire il set di portfolio, se necessario, in base alle prestazioni effettive e previste del portfolio e alle opportunità di crescita:

   * Regola i budget del portfolio, gli obiettivi e altre impostazioni.

   * Modifica le strutture account/campagne per adattarle ai cambiamenti nella strategia di marketing.

   * Aggiungere, mettere in pausa ed eliminare componenti della campagna. Questo può includere l’espansione dei set di parole chiave basati sull’analisi dei termini di ricerca e la verifica delle pagine di destinazione e di copia degli annunci.

   * Aggiornare le strategie di targeting geografico e del sito in base a rapporti sulle prestazioni avanzati.

   * (Facoltativo) Aggiungi vincoli di offerta alle singole parole chiave di ricerca o a tutte le parole chiave in un gruppo di annunci, una campagna o un portfolio.

   * Aggiungere nuovi portfolio.

Per istruzioni sul monitoraggio dei portfolio e sull&#39;adeguamento delle strategie di portfolio, vedere il sottocapitolo della guida &quot;Ottimizzazione&quot; > &quot;Gestione dei Portfoli&quot; > &quot;Monitoraggio e gestione delle prestazioni&quot;, disponibile nella [!UICONTROL Help] menu (![Menu Aiuto](/help/search-social-commerce/assets/help-main-menu.png "Menu Aiuto")) in alto a destra nelle pagine di Search, Social e Commerce.
