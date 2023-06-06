---
title: Informazioni sulla gestione dei dati della campagna tramite bulksheet
description: Scopri le funzionalità dei bulksheet disponibili tramite la rete di annunci, il flusso di lavoro dei bulksheet e la gestione degli errori.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '772'
ht-degree: 0%

---

# Informazioni sulla gestione dei dati della campagna tramite bulksheet

Un bulksheet è un file che contiene i dati della campagna in un formato specifico e può essere utilizzato per creare o modificare rapidamente i dati della struttura della campagna e del gruppo di annunci e gli annunci di testo. Puoi generare (scaricare) i bulksheet con i dati per uno o più account, per campagne e gruppi di annunci specifici o anche per annunci di testo, posizionamenti e gruppi di prodotti specifici. È possibile utilizzare i bulksheet per gestire set di dati di grandi dimensioni o per apportare piccole modifiche. Ogni rete di annunci richiede diverse colonne di informazioni.

Puoi generare i bulksheet con la quantità di dati desiderata oppure, facoltativamente, crearli manualmente e caricarli (vedi il capitolo su &quot;Dati richiesti/inclusi nei bulksheet&quot;).

Dopo aver creato un bulksheet, puoi identificare le pagine di destinazione danneggiate che devono essere corrette o i dati aggiuntivi da aggiungere o modificare. Puoi quindi modificare il file e caricarlo in Search, Social e Commerce, pianificando facoltativamente che venga inviato alla rete di annunci pertinente immediatamente o in un secondo momento. Puoi anche pubblicare un bulksheet disponibile immediatamente o in un secondo momento.

Facoltativamente, puoi caricare i file bulksheet su un account FTP specificato per il recupero e la registrazione automatica. La directory viene analizzata ogni ora e i nuovi file vengono inviati alla rete di ricerca nell&#39;ordine in cui vengono ricevuti.

Tutti i bulksheet, i file di errore di convalida della pagina di destinazione e gli altri file di errore vengono eliminati automaticamente 30 giorni dopo la creazione, a meno che non vengano eliminati in precedenza.

## Funzionalità per Ad Network

* **Scarica, carica e pubblica:**  [!DNL Baidu], [!DNL Google Ads], [!DNL Microsoft® Advertising], e [!DNL Yandex] account

* **Solo download e caricamento:** [!DNL Naver] account

   Puoi caricare [!DNL Naver] dati da utilizzare in Search, Social e Commerce, ma non possono inviarli alla rete di annunci. Puoi anche scaricare i dati esistenti (non sincronizzati).

* **Scarica solo dati:**  [!DNL Pinterest], [!DNL Yahoo Native], e [!DNL Yahoo! Display Network] account

   Puoi scaricare i dati esistenti (non sincronizzati).

## Panoramica sull’utilizzo dei bulksheet

I passaggi standard per l’utilizzo dei bulksheet per gli account sincronizzati sono i seguenti:

<!-- insert image
  [EDIT/RECREATE FILE to replace "search engine"]
-->

1. [Scaricare dati per uno o più account, campagne o gruppi di annunci in un file di bulksheet](bulksheet-download.md). Facoltativamente, puoi popolare manualmente un bulksheet specifico per la rete di annunci e caricare il file.

1. [Convalidare le pagine di destinazione](bulksheet-validate-landing-pages.md) negli URL di base (finali) o di destinazione nel file.

1. Quando devi aggiungere dati o apportare correzioni:

   1. [Esportare il file](bulksheet-export.md) sul desktop e modificarlo in [!DNL Microsoft® Excel].

   1. [Carica manualmente il file modificato](bulksheet-upload.md) per effettuare ricerche, social e e commerce, oppure [carica il file su un account FTP specificato](bulksheet-ftp-account.md) per la registrazione automatica.

1. (per file caricati manualmente) [Pubblica il file](bulksheet-post.md) alla rete di annunci durante il caricamento o in un secondo momento.

1. (Se necessario) Scaricare i nuovi file di errore, correggere le righe e ripubblicare il file.

## Gestione degli errori di caricamento e registrazione dei dati della campagna

Search, Social e Commerce caricano e pubblicano tutte le righe di dati possibili da un foglio di massa di una campagna, inclusi gli URL di tracciamento generati quando necessario.

Quando si verificano errori durante l&#39;operazione di bulksheet, viene generato uno dei due tipi di file di errore seguenti:

* **[!UICONTROL EF Errors]:**  Quando non è possibile caricare o elaborare un file o singole righe nel file, viene visualizzato un file di errore denominato `<uploaded file name>_ef_errors.<extension used for the bulksheet>` viene creato. Se il problema riguarda singole righe, queste righe vengono incluse, con una spiegazione di ogni errore in modo che possa essere corretto.

* **[!UICONTROL SE Errors]:**  Quando un file viene pubblicato ma la rete di annunci non accetta alcuni o tutti i dati, viene visualizzato un file di errore denominato `<uploaded file name>_se_errors.<extension used for the bulksheet>` viene creato. Quando alcune righe, ma non tutte, sono state accettate, il file di errore mostra le righe che non sono state pubblicate e una spiegazione di ogni errore in modo che possa essere corretto. I messaggi di errore vengono visualizzati nelle ultime tre colonne di ogni riga.

>[!NOTE]
>
>Se ne pubblichi una [!DNL Google Ads] gli annunci che violano le politiche pubblicitarie della rete di annunci ma che possono essere ammessi alle esenzioni, vengono automaticamente ripubblicati con le richieste di esenzione. Se la richiesta di esenzione ha esito negativo, le informazioni sulla violazione vengono incluse nel file di errore.

Puoi scaricare entrambi i tipi di file di errore, apportare correzioni direttamente nelle righe, quindi ricaricare e pubblicare il file.

I file di errore vengono eliminati automaticamente dopo 30 giorni, a meno che non vengano eliminati in precedenza.

## Informazioni su ciascun file

Tutti i file di dati scaricati, i file caricati e i file di errore sono disponibili da [!UICONTROL Search] > [!UICONTROL Bulksheets].

Le informazioni per ciascun file includono lo stato corrente dell&#39;attività e la percentuale di completamento dell&#39;attività, la data di creazione, (se applicabile) la data in cui è stata o verrà pubblicata nella rete di annunci specificata, la data di eliminazione pianificata e il nome di accesso dell&#39;utente che ha avviato l&#39;attività.

>[!MORELIKETHIS]
>
>* [Scaricare/creare un file bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)
>* [Carica un file di bulksheet o un file di errore corretto](bulksheet-upload.md)
>* [Pubblica i bulksheet o i file di errore corretti](bulksheet-post.md)
>* [Esportare un file bulksheet generato o caricato](bulksheet-export.md)
