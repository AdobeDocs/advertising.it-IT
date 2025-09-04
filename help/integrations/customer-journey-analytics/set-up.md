---
title: Impostare la raccolta dati, il trasferimento dati e il reporting
description: Scopri come impostare la raccolta dati, il trasferimento dati e il reporting.
feature: Integration with Adobe Customer Journey Analytics
source-git-commit: 2d6cba8d5a3d966b272c5048404ac8fdf0185b74
workflow-type: tm+mt
source-wordcount: '1236'
ht-degree: 0%

---

# Impostare la raccolta dati, il trasferimento dati e il reporting

*funzionalità Beta*

Per visualizzare i dati di Advertising Cloud in Customer Journey Analytics sono necessarie le seguenti attività.

1. (Web Analyst della tua organizzazione; facoltativo) [Raccogli dati storici per gli AMO ID e gli EF ID](/help/integrations/analytics/rvars-to-evars.md){target="_blank"}.

   Questo passaggio è applicabile solo agli inserzionisti con [!DNL Analytics for Advertising].

1. (Amministratore del sito della tua organizzazione per Adobe Experience Platform) [Configura la raccolta dati in Experience Platform e implementa i tag per il monitoraggio delle conversioni](#data-collection).

1. (Amministratore del sito della tua organizzazione per Customer Journey Analytics) [Crea una connessione ai set di dati di Experience Platform in Customer Journey Analytics](#dataset-connection).

1. (Web Analyst della tua organizzazione) [Imposta le visualizzazioni dati in Customer Journey Analytics](#cja-data-views).

1. (Web Analyst della tua organizzazione) [Imposta rapporti e visualizzazioni in Customer Journey Analytics Workspace](#cja-reports).

Nelle sezioni seguenti sono incluse le procedure dettagliate, che includono le attività e le impostazioni necessarie per l’integrazione, ma non spiegano tutte le funzioni disponibili all’interno dei flussi di lavoro. Per informazioni complete, consulta le risorse collegate.

## Configurare la raccolta dati in Adobe Experience Platform e sul sito web {#data-collection}

Per impostare la raccolta dati in Experience Platform e implementare i tag di tracciamento della conversione sono necessarie le seguenti attività. L’amministratore del sito della tua organizzazione per Experience Platform può eseguire queste attività, ma il reparto IT dell’organizzazione potrebbe dover fornire assistenza per la distribuzione dei tag di tracciamento.

1. Raccogli e invia dati da Adobe Advertising ad Experience Platform Edge Network come set di dati:

   1. In Experience Platform, [definisci uno schema manuale](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/resources/schemas) per i dati da raccogliere utilizzando Experience Data Model (XDM).

      * In [!UICONTROL Schema Details], selezionare **[!UICONTROL Experience Event]** come classe base per lo schema per acquisire eventi del sito. Assegna un nome allo schema e fai clic su **[!UICONTROL Finish]**.

      * Nel pannello a sinistra, aggiungi il gruppo di campi `Adobe Advertising Cloud ExperienceEvent Full Extension` per aggiungere campi specifici ad Adobe Advertising.<!-- Add link once published --> Includere almeno l&#39;oggetto conversionDetails con le proprietà `trackingCode` e `trackingIdentities`, che includono [AMO ID e EF ID](ids.html). Gli altri campi sono facoltativi.

      * (Facoltativo) Aggiungi altri gruppi di campi in base alle esigenze per collegare campi di dati aggiuntivi ai dati di Adobe Advertising.

      **Nota:** è possibile creare più schemi, ma è possibile utilizzare un solo schema per set di dati e per flusso di dati, che verrà creato nei passaggi seguenti.

   1. [Crea un set di dati](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/create) basato sullo schema per archiviare e gestire la raccolta di dati evento.

      * Scegliere l&#39;opzione per **[!UICONTROL Create dataset from schema]** e selezionare lo schema.

        Adobe Advertising crea set di dati aggiuntivi per i dati delle metriche di riepilogo correlate (come i valori di conversione) e i dati di ricerca (dimensioni/metadati di classificazione, come il nome della campagna Adobe Advertising) in base al set di dati dell’evento. I dati per i set di dati vengono compilati quotidianamente in Experience Platform.

   1. [Crea uno stream di dati](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure) per lo schema.

      * Per l&#39;impostazione [!UICONTROL Mapping schema], selezionare lo schema.

      * Aggiungere e abilitare i servizi `Adobe Advertising` e `Adobe Experience Platform` allo stream di dati.

        Questi servizi consentono ad Edge Network di memorizzare il set di dati e di inviarlo ad Adobe Advertising.

      * Per l&#39;impostazione [!UICONTROL Event dataset], seleziona il set di dati.

        Ogni flusso di dati può inserire dati in un solo set di dati.

1. Invia i dati del sito web della tua organizzazione al flusso di dati di Experience Platform:

   1. Utilizza i [tag](https://experienceleague.adobe.com/en/docs/experience-platform/tags/home) di Experience Platform (noti in precedenza come [!DNL Launch]) per generare un tag JavaScript per inviare i dati del sito Web della tua organizzazione allo stream di dati.

      * Crea una proprietà tag, che è il contenitore per la configurazione tag.

      * Per la tua proprietà, [installa l&#39;estensione &quot;Adobe Experience Platform Web SDK&quot;](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration) dal catalogo delle estensioni.

        Questa estensione invia i dati dalle proprietà web ad Experience Cloud tramite Experience Platform Edge Network.

        Non utilizzare l&#39;estensione Adobe Advertising.

      * Creazione di una build Web SDK personalizzata:

         * Nella sezione [!UICONTROL Custom build components], abilita il componente **Advertising**.

           Questo componente include tutto il codice JavaScript necessario per Adobe Advertising nel tag. Aggiunge inoltre un’impostazione &quot;Advertising&quot; nelle regole dei tag (facoltative) per definire il modo in cui i dati pubblicitari vengono utilizzati per la misurazione dell’attribuzione.

           Facoltativamente, puoi abilitare altri componenti in base alle esigenze.

         * Nella sezione [!UICONTROL SDK Instances]:

            * Nelle impostazioni [!UICONTROL Datastreams], seleziona lo stream di dati da utilizzare per ciascuno degli ambienti web (produzione, staging, sviluppo).

            * (Solo organizzazioni con Adobe Advertising DSP) Nelle impostazioni [!UICONTROL Adobe Advertising]:

               * Abilitare l&#39;impostazione **[!UICONTROL Adobe Advertising DSP]** per abilitare il tracciamento view-through.

               * Specifica gli inserzionisti per i quali abilitare il tracciamento view-through.

               * (Facoltativo) Immetti l&#39;ID partner ID5 della tua organizzazione per raccogliere gli ID.

               * (Facoltativo) Immetti il percorso per il codice JavaScript [!DNL LiveRamp RampID] della tua organizzazione (ats.js) per raccogliere gli ID.

            * Salva la build.

      * (Facoltativo) [Crea regole](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/rules) per determinare quando Web SDK deve inviare dati ad Edge Network.

         * Per l&#39;impostazione [!UICONTROL Advertising], definisci il modo in cui i dati pubblicitari vengono utilizzati per la misurazione dell&#39;attribuzione. Questa impostazione è utile quando la regola include una sequenza di più azioni ed è disponibile solo quando è stato selezionato il componente &quot;[!UICONTROL Advertising]&quot; per il componente di compilazione personalizzato. Le opzioni includono:

           *Automatico:* consente l&#39;utilizzo di dati pubblicitari per la misurazione dell&#39;attribuzione di annunci sull&#39;azione `sendEvent` corrente in base ai dati presenti nella cache. In questo caso, l’evento di esposizione dell’annuncio viene attivato quando se ne presenta l’opportunità e potrebbe non essere disponibile per l’evento corrente. Ad esempio, se attivi un evento di pagamento dell’acquisto e nella cache non sono disponibili dati sull’esposizione dell’annuncio, l’evento di pagamento non viene attribuito all’esposizione dell’annuncio.

           *Attendi:* ritarda l&#39;esecuzione della chiamata fino al completamento del recupero e della risoluzione dei dati pubblicitari dal server, in modo da garantire una misurazione accurata dell&#39;attribuzione. Ad esempio, potresti voler attendere la risoluzione dell’evento di esposizione dell’annuncio prima di attivare un evento di pagamento dell’acquisto. **Nota:** gli ID di risoluzione potrebbero richiedere alcuni secondi a seconda del browser e del tipo di ID. Utilizzare questa opzione se l&#39;azione `sendEvent` corrente può contenere alcuni secondi di ritardo.

           *Disabilitato:* (impostazione predefinita) esclude i dati pubblicitari dalla richiesta che si sta attivando, rendendoli non disponibili per l&#39;attribuzione o il tracciamento correlato.

           *Fornisci un elemento dati:* Utilizza un elemento dati per includere o escludere dati pubblicitari durante il caricamento della pagina. I valori risolti per l&#39;elemento dati possono includere `automatic`, `wait` e `disabled`. Vedere il passaggio successivo.

        Se non utilizzi una regola per configurare un&#39;azione `sendEvent`, i dati pubblicitari vengono inviati come evento di arricchimento dell&#39;annuncio separato.

      * Crea [elementi dati](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/data-elements) necessari per mappare le variabili sul tuo sito Web alla struttura dello schema XDM creato in precedenza.

   1. [Pubblica il tag](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow) in un ambiente di test in cui puoi eseguire iterazioni sullo sviluppo dei tag.

   1. Convalida la distribuzione dei set di dati, quindi [pubblica il tag nell&#39;ambiente di produzione live](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow).

      Il reparto IT della tua organizzazione o un altro gruppo potrebbe dover pianificare l’implementazione dei tag o esserne informato.

## Creare una connessione ai set di dati di Experience Platform in Customer Journey Analytics {#dataset-connection}

Segui questi passaggi per estrarre i dati di Adobe Advertising dai set di dati di Experience Platform in Customer Journey Analytics. L’amministratore del sito della tua organizzazione per Customer Journey Analytics può eseguire queste attività.

*In arrivo*

## Configurare le visualizzazioni dati in Customer Journey Analytics {#cja-data-views}

In Customer Journey Analytics, crea una o più visualizzazioni dati per definire le metriche e le dimensioni per il reporting. Un analista web può eseguire queste attività.

*In arrivo*

## Configurare rapporti e visualizzazioni in Customer Journey Analytics Workspace {#cja-reports}

In Customer Journey Analytics Workspace, segui questi passaggi per configurare rapporti e visualizzazioni. Un analista web può eseguire queste attività.

1. [Crea un progetto](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/build-workspace-project/create-projects) in Workspace per creare rapporti e visualizzazioni in base alle dimensioni e alle metriche configurate nella visualizzazione dati.

1. (Se si dispone di dati di [!DNL Google Ads] o [!DNL Microsoft Advertising]) Creare un report delle conversioni tracciate dall&#39;editore utilizzando i campi per le metriche specifiche della rete di annunci, raggruppati come `googleConversions` e `microsoftConversions`.

>[!MORELIKETHIS]
>
>* [Panoramica](overview.md)
>* [Prerequisiti](prerequisites.md)
>* [ID Adobe Advertising utilizzati da [!DNL Customer Journey Analytics]](ids.md)
>* [Metriche e dimensioni di Adobe Advertising in Customer Journey Analytics](advertising-data-in-cja.md)
>* [Raccogliere dati cronologici per gli ID AMO e gli ID EF da utilizzare in Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
>* [Guida di Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-landing)
>* Guida utente di Customer Journey Analytics [per gli utenti di Adobe Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/compare-aa-cja/aa-to-cja-user)
