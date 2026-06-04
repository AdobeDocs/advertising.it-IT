---
title: (Nuova interfaccia) Informazioni sulla gestione dei dati della campagna tramite i bulksheet
description: Scopri le funzionalità dei bulksheet disponibili tramite la rete di annunci, il flusso di lavoro dei bulksheet e la gestione degli errori nella nuova interfaccia utente di Search, Social e Commerce.
feature: Search Bulksheets
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: e58024d1-d6da-420c-80af-6be211808316id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: f916f47a40729ff39ac1456e3b3ad93e1045e9a9
workflow-type: tm+mt
source-wordcount: 773
ht-degree: 0%

---

# (Nuova interfaccia) Informazioni sulla gestione dei dati della campagna tramite i bulksheet

Un bulksheet è un file che contiene i dati della campagna in un formato specifico e può essere utilizzato per creare o modificare rapidamente i dati della struttura della campagna e del gruppo di annunci e gli annunci di testo. Puoi generare (scaricare) i bulksheet con i dati per uno o più account, per campagne e gruppi di annunci specifici o anche per annunci di testo, posizionamenti e gruppi di prodotti specifici. È possibile utilizzare i bulksheet per gestire set di dati di grandi dimensioni o per apportare piccole modifiche. Ogni rete di annunci richiede diverse colonne di informazioni.

Puoi generare i bulksheet con la quantità di dati desiderata oppure, facoltativamente, crearli manualmente e caricarli. Vedere &quot;[Dati obbligatori e inclusi nei bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-file-formats.md)&quot; per i requisiti di formato file e &quot;[Operazioni eseguibili nei bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-operations.md)&quot; per le operazioni supportate dalla rete di annunci.

Dopo aver creato un bulksheet, puoi identificare le pagine di destinazione danneggiate che devono essere corrette o i dati aggiuntivi da aggiungere o modificare. Puoi quindi modificare il file e caricarlo in Search, Social e Commerce, pianificando facoltativamente che venga inviato alla rete di annunci pertinente immediatamente o in un secondo momento. Puoi anche pubblicare un bulksheet disponibile immediatamente o in un secondo momento.

Tutti i bulksheet, i file di errore di convalida della pagina di destinazione e gli altri file di errore vengono eliminati automaticamente 30 giorni dopo la creazione, a meno che non vengano eliminati in precedenza.

## Funzionalità per rete di annunci {#bulksheet-functionality-by-network}

* **Scarica, carica e pubblica:** account [!DNL Baidu], [!DNL Google Ads], [!DNL Microsoft Advertising] e [!DNL Yandex]

* **Solo download e caricamento:** [!DNL Naver] account

  Puoi caricare [!DNL Naver] dati da utilizzare in Search, Social e Commerce, ma non puoi pubblicarli nella rete di annunci. Puoi anche scaricare i dati esistenti (non sincronizzati).

* **Scarica solo dati:** [!DNL Pinterest], [!DNL Yahoo Native] e [!DNL Yahoo! Display Network] account

  Puoi scaricare i dati esistenti (non sincronizzati).

## Panoramica sull’utilizzo dei bulksheet

I passaggi standard per l’utilizzo di bulksheet con account sincronizzati sono i seguenti:

1. [Scarica i dati per uno o più account, campagne o gruppi di annunci in un file bulksheet](download.md). Facoltativamente, puoi popolare manualmente un bulksheet specifico per la rete di annunci e caricare il file.

1. [Convalida le pagine di destinazione](validate-landing-pages.md) negli URL di base (finali) o negli URL di destinazione nel file.

1. Quando devi aggiungere dati o apportare correzioni:

   1. Esportare il file sul desktop e modificarlo in [!DNL Microsoft Excel].

   1. [Carica manualmente il file modificato](upload.md) in Search, Social e Commerce.

1. (Per i file caricati manualmente) [Pubblica il file](post.md) nella rete di annunci durante il caricamento o in un secondo momento.

1. (Se necessario) Scaricare i nuovi file di errore, correggere le righe e ripubblicare il file.

## Gestione degli errori di caricamento e registrazione dei dati della campagna

Search, Social e Commerce caricano e pubblicano tutte le righe di dati possibili da un bulksheet di una campagna, inclusi gli URL di tracciamento generati quando necessario.

Quando si verificano errori durante un&#39;operazione di bulksheet, viene generato uno dei due tipi di file di errore seguenti:

* **[!UICONTROL EF Errors]:** Quando non è possibile caricare o elaborare un file o singole righe nel file, viene creato un file di errore denominato `<uploaded file name>_ef_errors.<extension used for the bulksheet>`. Se il problema riguarda singole righe, queste righe vengono incluse, con una spiegazione di ogni errore in modo che possa essere corretto.

* **[!UICONTROL SE Errors]:** Quando un file viene pubblicato ma la rete di annunci non accetta alcuni o tutti i dati, viene creato un file di errore denominato `<uploaded file name>_se_errors.<extension used for the bulksheet>`. Quando alcune righe, ma non tutte, sono state accettate, il file di errore mostra le righe che non sono state pubblicate e una spiegazione di ogni errore in modo che possa essere corretto. I messaggi di errore vengono visualizzati nelle ultime tre colonne di ogni riga.

>[!NOTE]
>
>Se si pubblicano [!DNL Google Ads] annunci che violano le politiche pubblicitarie della rete di annunci ma possono essere ammessi alle esenzioni, tali annunci vengono automaticamente ripubblicati con le richieste di esenzione. Se la richiesta di esenzione ha esito negativo, le informazioni sulla violazione vengono incluse nel file di errore.

Puoi scaricare entrambi i tipi di file di errore, apportare correzioni direttamente nelle righe, quindi ricaricare e pubblicare il file.

I file di errore vengono eliminati automaticamente dopo 30 giorni, a meno che non vengano eliminati in precedenza.

## Informazioni su ciascun file

Tutti i file di dati scaricati, i file caricati e i file di errore sono disponibili da [!UICONTROL Setup] \> [!UICONTROL Bulksheets].

Le informazioni per ciascun file includono lo stato corrente dell&#39;attività e la percentuale di completamento dell&#39;attività, la data di creazione, (se applicabile) la data in cui è stata o verrà pubblicata nella rete di annunci specificata, la data di eliminazione pianificata e il nome di accesso dell&#39;utente che ha avviato l&#39;attività.

>[!MORELIKETHIS]
>
>* [(Nuova interfaccia) Download/creazione di un file bulksheet](download.md)
>* [(Nuova interfaccia) Carica un bulksheet o un file di errore corretto](upload.md)
>* [(Nuova interfaccia) Pubblica i bulksheet o correggi i file di errore](post.md)
>* [(Nuova interfaccia) Convalida pagine di destinazione in file bulksheet](validate-landing-pages.md)
>* [(Nuova interfaccia) Elimina i bulksheet caricati e i file di errore](delete.md)
>* [(Nuova interfaccia) Interruzione di un processo bulksheet in corso](stop-job.md)
