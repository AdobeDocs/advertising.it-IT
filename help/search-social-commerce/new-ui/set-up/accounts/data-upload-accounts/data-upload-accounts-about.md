---
title: null
description: null
source-git-commit: f2b29c2f3a38cadc31a9b3110aa82feadd62e5cc
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 0%

---

# Informazioni sul caricamento dei dati dell’account per rapporti e simulazioni

<!-- Move all related files into one page? -->

Se utilizzi reti pubblicitarie online per le quali Search, Social e Commerce non forniscono supporto API, puoi caricare contenuti della campagna e costi offline, fare clic e dati di conversione per un account per generare rapporti e simulazioni delle prestazioni. Gli inserzionisti con un&#39;integrazione [[!DNL Adobe Analytics for Advertising] integration](/help/integrations/analytics/overview.md) possono anche visualizzare i dati dei loro account in Adobe Analytics.

Questa funzione è disponibile per le reti di annunci che seguono la struttura standard a tre livelli delle campagne (campagna, gruppo di annunci o set di annunci e unità di offerta (annuncio o parola chiave)). Per Adobe DSP, la funzione è disponibile per i pacchetti e i posizionamenti assegnati a un pacchetto, ma non per le campagne o i posizionamenti con velocità a livello di posizionamento.

Supporto predefinito disponibile per le reti seguenti:<!-- But what if you want to use something else? Is that possible currently? -->

<!-- * Adobe Demand Side Platform (Advertising DSP) [Is any data upload required, or just an initial setup of an S3 bucket and/or something else, and then DSP sends the data automatically? If so, then I may need to reframe this whole chapter accordingly.] -->
<!-- * [!DNL Reddit Ads] -->

* [!DNL Apple Search Ads]
* [!DNL LinkedIn Ads]
* [!DNL TikTok Ads]

Search, Social e Commerce Adobe Advertising non sono supportati con questa funzione.

## Funzionalità disponibili in Search, Social e Commerce

* Tracciamento e reporting:

   * Componenti di sola lettura per campagne, fino al livello di unità di offerta nelle viste di gestione delle campagne.

   * Dati sulle prestazioni fino al livello di gruppo di annunci <!-- verify the entity level --> nelle visualizzazioni di gestione delle campagne e nei rapporti personalizzati. Gli inserzionisti con [!DNL Adobe Analytics for Advertising]) ottengono inoltre dati sulle prestazioni fino al livello di gruppo di annunci <!-- verify the entity level --> all&#39;interno delle suite di rapporti di Adobe Analytics specificate per l&#39;inserzionista.&lt;!verifica se i tipi di dati sono limitati: costi, clic, impression di visualizzazione, ricavi? —>

* Simulazioni delle prestazioni quando si aggiungono campagne a un portfolio.<!-- How does this even work? Do they need to be in standard or hybrid portfolios, with active or optimized status, and can you mix these campaigns with API-synced campaigns? If so, do we just ignore these campaigns and optimize the others? -->

  Search, Social e Commerce non ottimizzano nulla, né fanno offerte, per questi tipi di campagne all’interno di un portfolio.

## Flusso di lavoro per la configurazione di account offline

<!-- subtitle wording? -->

1. [Configura un record account fittizio](/help/search-social-commerce/new-ui/set-up/accounts/data-upload-accounts/data-upload-account-manage.md).

1. Creare un file di dati per un singolo account<!--  in what file format? -->, incluso lo stato a livello di giorno per campagne, gruppi di annunci e annunci.

I dati devono rispettare i requisiti di dati per la rete di annunci, in modo che i campi di dati per ogni entità possano variare a seconda della rete di annunci.

1. <!-- For all ad networks (excluding DSP), -->Caricare i dati iniziali per un singolo account in uno dei modi seguenti:

* Caricare un file manualmente dal dispositivo o dalla rete.

* Carica i dati in una cartella di ricerca, social e Commerce assegnata in un bucket [!DNL Amazon Web Services] (AWS) [!DNL Simple Storage Service] ([!DNL S3]).

  >[!PREREQUISITES]
  >
  >* Contatta il team del tuo account Adobe per abilitare il caricamento dei dati dell’account dell’inserzionista Search, Social e Commerce. Il team semplificherà la creazione di una cartella specifica dell&#39;organizzazione in un bucket [!DNL S3] e ti informerà al termine.<!-- Add more context about the bucket we'll use here or in the intro. Do we have one bucket (potentially with multiple folders) per client, or do we share them (if so, do we need to state how in docs? -->
  >* Recupera il percorso di archiviazione cloud [!DNL S3], l&#39;ID della chiave di accesso e la chiave di accesso segreta per il tuo account. Gli stessi ID chiave di accesso e chiave di accesso segreta vengono utilizzati per tutti gli account <!-- naming convention?--> di caricamento dati dell&#39;organizzazione.

1. Continua a caricare nuovi file di dati ogni giorno.

1. Dopo aver caricato i dati per 30 giorni, puoi facoltativamente aggiungere le campagne ai portfolio <!--what type? how should we refer to them? --> e generare simulazioni.

Puoi [visualizzare un registro di ogni caricamento dati](upload-log.md) per visualizzarne lo stato. Inoltre, se avvii un caricamento ma il caricamento non ha esito positivo, riceverai una notifica di errore tramite [Centro notifiche](/help/search-social-commerce/notifications/notification-about.md), in base alle impostazioni di notifica.

<!-- Data validation, and any troubleshooting? -->

>[!MORELIKETHIS]
>
>* [Informazioni sul caricamento dei dati dell&#39;account per report e simulazioni](data-upload-accounts-about.md)
>* [Carica dati account in un bucket [!DNL Amazon] [!DNL S3]](upload-data-from-s3-bucket.md)
>* [Carica dati account manualmente](upload-data-manually.md)
>* [Visualizza un registro dei file di dati account caricati](upload-log.md)
>* [Gestire gli account di rete degli annunci per il caricamento dei dati](/help/search-social-commerce/campaign-management/accounts/data-upload-account-manage.md)
