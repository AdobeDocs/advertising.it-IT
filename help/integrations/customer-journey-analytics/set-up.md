---
title: Impostare la raccolta dati, il trasferimento dati e il reporting
description: Scopri come impostare la raccolta dati, il trasferimento dati e il reporting.
feature: Integration with Adobe Customer Journey Analytics
exl-id: a955e2b0-ea1b-4b5c-937b-f8c66603cd36
TQID: https://experienceleague.adobe.com/u6xL6FuW-TwqAkse3VTS3zcyt-10Cv-ADTZLJTiWWT8
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: e208432cf19b2661fbce58a898a123bb1224c32b
workflow-type: tm+mt
source-wordcount: 1789
ht-degree: 0%

---

# Impostare la raccolta dati, il trasferimento dati e il reporting

*Inserzionisti con Advertising DSP e[!DNL Advertising Search, Social, & Commerce]*

*Inserzionisti senza solo [!DNL Analytics for Advertising]*

Le seguenti attività sono necessarie per lo scambio nativo di dati tra Adobe Advertising e Customer Journey Analytics utilizzando [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html). Il trasferimento e l’attribuzione dei dati iniziano dopo il lancio; non vengono inclusi dati storici.

Queste attività non sono necessarie per gli inserzionisti con [!DNL Analytics for Advertising].

1. (Amministratore del sito della tua organizzazione per Adobe Experience Platform) [Configura la raccolta dati in Experience Platform e implementa i tag per il monitoraggio delle conversioni](#data-collection).

1. (Amministratore del sito della tua organizzazione per Customer Journey Analytics) [Crea una connessione ai set di dati di Experience Platform in Customer Journey Analytics](#dataset-connection).

1. (Web Analyst della tua organizzazione) [Imposta le visualizzazioni dati in Customer Journey Analytics](#cja-data-views).

1. (Web Analyst della tua organizzazione) [Imposta rapporti e visualizzazioni in Customer Journey Analytics Workspace](#cja-reports).

Nelle sezioni seguenti sono incluse le procedure dettagliate, che includono le attività e le impostazioni necessarie per l’integrazione, ma non spiegano tutte le funzioni disponibili all’interno dei flussi di lavoro. Per informazioni complete, consulta le risorse collegate.

## Configurare la raccolta dati in Adobe Experience Platform e sul sito web {#data-collection}

Per impostare la raccolta dati in Experience Platform e implementare i tag di tracciamento della conversione sono necessarie le seguenti attività. L’amministratore del sito della tua organizzazione per Experience Platform può eseguire queste attività, ma il reparto IT dell’organizzazione potrebbe dover fornire assistenza per la distribuzione dei tag di tracciamento.

### Raccogliere e inviare dati da Adobe Advertising ad Experience Platform Edge Network come set di dati

Questa procedura include la creazione di uno schema. Facoltativamente, puoi invece modificare uno schema esistente; in tal caso, non è necessario creare un set di dati o uno stream di dati.

1. In Experience Platform, [definisci uno schema manuale](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/resources/schemas) per i dati da raccogliere utilizzando Experience Data Model (XDM).

   * In [!UICONTROL Schema Details], selezionare **[!UICONTROL Experience Event]** come classe base per lo schema per acquisire eventi del sito. Assegna un nome allo schema e fai clic su **[!UICONTROL Finish]**.

   * Nel pannello a sinistra, aggiungi il gruppo di campi [Estensione completa Adobe Advertising Cloud ExperienceEvent](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/field-groups/event/advertising-full-extension) per aggiungere campi specifici ad Adobe Advertising. Includi almeno l&#39;oggetto conversionDetails con le proprietà `trackingCode` e `trackingIdentities`, che includono l&#39;ID [AMO e l&#39;ID EF](ids.md). Gli altri campi sono facoltativi.

   * (Facoltativo) Aggiungi altri gruppi di campi in base alle esigenze per collegare campi di dati aggiuntivi ai dati di Adobe Advertising.

   **Nota:** è possibile creare più schemi, ma è possibile utilizzare un solo schema per set di dati e per flusso di dati, che verrà creato nei passaggi seguenti.

1. [Crea un set di dati](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/create) basato sullo schema per archiviare e gestire la raccolta di dati evento. Questo sarà il *set di dati evento*. Se stai modificando uno schema esistente con un set di dati, puoi saltare questo passaggio.

   * Scegliere l&#39;opzione per **[!UICONTROL Create dataset from schema]** e selezionare lo schema.

     In base al set di dati dell&#39;evento, Adobe Advertising crea due set di dati aggiuntivi: 1\) un *set di dati di riepilogo* con i relativi dati di riepilogo (come clic e impression) e 2\) un *set di dati di ricerca* (con dimensioni/metadati di classificazione, come il nome della campagna Adobe Advertising). I dati per i set di dati vengono compilati quotidianamente in Experience Platform.

   >[!TIP]
   >
   >Crea prima un set di dati evento fittizio per convalidare il flusso di dati prima di utilizzare un set di dati di produzione.

1. [Crea un flusso di dati](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure) per specificare dove inviare dati dal sito Web o dall&#39;app e come gestire i dati in arrivo.

   * Per l&#39;impostazione [!UICONTROL Mapping schema], selezionare lo schema.

   * Aggiungere e abilitare i servizi `Adobe Advertising` e `Adobe Experience Platform` allo stream di dati.

     Il servizio [!UICONTROL Adobe Advertising] consente di associare le esposizioni degli annunci al payload, mentre il servizio [!UICONTROL Adobe Experience Platform] consente ad Edge Network di memorizzare il set di dati e di indirizzarlo ad Adobe Advertising.

   * Per l&#39;impostazione [!UICONTROL Event dataset], seleziona il set di dati evento.

     Ogni flusso di dati può inserire dati in un solo set di dati.

### Invia i dati del sito web della tua organizzazione al flusso di dati di Experience Platform

Utilizza l’estensione Adobe Experience Platform Web SDK nei tag Adobe per inviare i dati del sito web della tua organizzazione al flusso di dati di Experience Platform.

>[!NOTE]
>
>Sono supportati solo i tag di Adobe. Il supporto non è disponibile per Experience Platform Web SDK (`alloy.js`) standalone o per i gestori di tag di terze parti.

1. Utilizza i [tag](https://experienceleague.adobe.com/en/docs/experience-platform/tags/home) di Experience Platform (noti in precedenza come [!DNL Launch]) per generare un tag JavaScript per inviare i dati del sito Web della tua organizzazione allo stream di dati.

   * Crea una proprietà tag, che è il contenitore per la configurazione tag.

   * Per la tua proprietà, [installa l&#39;estensione &quot;Adobe Experience Platform Web SDK&quot;](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration) dal catalogo delle estensioni.

     Questa estensione invia i dati dalle proprietà web ad Adobe CX Enterprise tramite Experience Platform Edge Network.

     Non utilizzare l&#39;estensione Adobe Advertising.

   * Creazione di una [build Web SDK personalizzata](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration#custom-build):

      * Nella sezione [!UICONTROL Custom build components], abilita il componente **Advertising**.

        Questo componente include tutto il codice JavaScript necessario per Adobe Advertising nel tag ed è richiesto per i clienti Advertising DSP e Advertising Search, Social e Commerce. Il componente aggiunge anche un’impostazione &quot;Advertising&quot; nelle regole dei tag (facoltative) per definire il modo in cui i dati pubblicitari vengono utilizzati per la misurazione dell’attribuzione.

        Facoltativamente, puoi abilitare altri componenti in base alle esigenze.

      * Nella sezione [!UICONTROL SDK Instances]:

         * Nelle impostazioni [!UICONTROL Datastreams], seleziona lo stream di dati da utilizzare per ciascuno degli ambienti web (produzione, staging, sviluppo).

         * (Solo organizzazioni con Adobe Advertising DSP) Nelle impostazioni [[!UICONTROL Adobe Advertising]](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/advertising), abilita **[!UICONTROL Adobe Advertising DSP]** per consentire il tracciamento view-through e specifica gli inserzionisti per i quali abilitare il tracciamento view-through. Facoltativamente, puoi raccogliere gli ID dagli ID universali aggiungendo l&#39;ID partner ID5 della tua organizzazione e/o il percorso al codice JavaScript [!DNL LiveRamp RampID] della tua organizzazione (ats.js).

           Se gli inserzionisti non sono elencati, inserisci l&#39;ID inserzionista per ogni inserzionista. Se necessario, chiedi gli ID al tuo account team di Adobe.

         * Salva la build.

   * (Facoltativo) [Crea regole](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/rules) per determinare quando Web SDK deve inviare dati ad Edge Network.

      * Per le azioni `[sendEvent](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/actions/send-event)`, utilizza l&#39;impostazione [[!UICONTROL Advertising]](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/action-types#advertising) per definire il modo in cui i dati pubblicitari vengono utilizzati per la misurazione dell&#39;attribuzione. Questa impostazione è utile quando la regola include una sequenza di più azioni ed è disponibile solo quando è stato selezionato il componente &quot;[!UICONTROL Advertising]&quot; per il componente di compilazione personalizzato.

   * Crea [elementi dati](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/data-elements) necessari per mappare le variabili sul tuo sito Web alla struttura dello schema XDM creato in precedenza.

1. [Pubblica il tag](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow) in un ambiente di test in cui puoi eseguire iterazioni sullo sviluppo dei tag.

1. [Controlla l&#39;attività per ciascuno dei tuoi tre set di dati](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/user-guide#view-datasets) per convalidare la consegna.

1. [Pubblica il tag nell&#39;ambiente di produzione live](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow).

   Il reparto IT della tua organizzazione o un altro gruppo potrebbe dover pianificare l’implementazione dei tag o esserne informato.

## Creare una connessione ai set di dati di Experience Platform in Customer Journey Analytics {#dataset-connection}

Segui questi passaggi per estrarre i dati di Adobe Advertising dai set di dati di Experience Platform in Customer Journey Analytics. L’amministratore del sito della tua organizzazione per Customer Journey Analytics può eseguire queste attività.

Facoltativamente, puoi anche modificare una connessione esistente con le stesse informazioni.

1. In Customer Journey Analytics, [crea o modifica una connessione](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-connections/create-connection) che include i set di dati e lo schema di Experience Platform.

   <!-- **Note:** You must send data for all DSP and Search, Social, & Commerce accounts to a single Experience Platform instance and sandbox.  -->

   * Verifica che sia selezionata la sandbox corretta.

   * Calcola il numero medio di eventi giornalieri (meno di 1 milione per la maggior parte delle organizzazioni).

   * Aggiungi il set di dati delle metriche degli eventi di Experience Platform (tipo: `Event`), il set di dati delle metriche di riepilogo degli eventi <!-- Adobe Advertising --> (tipo: `Event`) e il set di dati delle dimensioni (classificazioni/metadati) <!-- Adobe Advertising --> (tipo: `Lookup`).

     Il team ha creato il set di dati dell’evento, mentre Adobe Advertising ha creato i set di dati di riepilogo e le dimensioni in base al set di dati dell’evento.

     Facoltativamente, puoi includere set di dati aggiuntivi in base alle esigenze.

   * Configura le impostazioni del set di dati:

      * Per le impostazioni [!UICONTROL Event Dataset]:

         * **[!UICONTROL Person ID]:** `Identity Map`

         * **[!UICONTROL Use primary identity namespace]:** Abilita impostazione

         * **[!UICONTROL Data Source Type]:** `Web Data > Others` <!-- I don't see "Others" in the screen shot example -->

         * **[!UICONTROL Import all new data]:** Abilitare l&#39;impostazione

      * Per le impostazioni [!UICONTROL Lookup Dataset], mappa il set di dati delle dimensioni al set di dati degli eventi:

         * **[!UICONTROL Key]** (campo da utilizzare come chiave per il set di dati delle dimensioni): `Tracking Code` (che corrisponde al campo `trackingCode` nello schema).

         * **[!UICONTROL Matching key]** (campo da utilizzare come chiave corrispondente per il set di dati degli eventi): `Tracking Code (Event datasets)`.<!-- verify this Later, you'll also map the events dataset to the summary dataset when you set up your data view(#cja-data-views).  -->

         * **[!UICONTROL Import all new data]:** Abilitare l&#39;impostazione

      * Per le impostazioni [!UICONTROL Metrics Dataset]:

         * **[!UICONTROL Person ID]:** `Identity Map`

         * **[!UICONTROL Timestamp]:** Conferma il valore

         * **[!UICONTROL Import all new data]:** Abilitare l&#39;impostazione

1. Entro tre ore, verifica che i dati siano disponibili in Customer Journey Analytics.

   1. In Customer Journey Analytics, vai a **[!UICONTROL Connections]** e seleziona la tua connessione.

   2. Nell&#39;elenco dei set di dati visualizzati, verificare che il report &quot;[!UICONTROL Number of Records]&quot; indichi che i dati sono stati aggiunti.

## Configurare le visualizzazioni dati in Customer Journey Analytics {#cja-data-views}

In Customer Journey Analytics, crea una o più visualizzazioni dati per definire le metriche e le dimensioni per il reporting. Un analista web può eseguire queste attività.

1. In Customer Journey Analytics, [crea una visualizzazione dati](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/create-dataview).

1. Configura la visualizzazione in modo da includere le seguenti informazioni.

   * Se si dispone di un account Adobe Analytics, utilizzare [!UICONTROL Time Zone] per l&#39;account [!DNL Analytics] nella sezione [!UICONTROL Calendar] della scheda [!UICONTROL Configure].

   * Nella scheda [!UICONTROL Components]:

      * Aggiungi il set di dati di ricerca (con dimensioni/dati di classificazione), il set di dati evento (con i dati a livello di evento) e il set di dati di riepilogo (con le altre metriche, come i clic).

      * Scegli le metriche dal set di dati evento e dal set di dati di ricerca da includere nella visualizzazione dati.

      * Cerca &quot;[!UICONTROL Tracking Code]&quot; (che fa parte del set di dati evento con percorso schema `_experience.adcloud.conversionDetails.trackingCode`). <!-- and do what with it? Add it? Or is that what you --> Imposta **[!UICONTROL Persistence]** su *[!UICONTROL Most Recent]*.

<!--

Seems to not be necessary now:


       You already joined these two datasets in the connection that you created in the [last procedure](#dataset-connection).
     
     *  Join the events dataset to the summary dataset, which isn't yet joined to anything:
     
       * For each dimension with summary data that you want to be available in Customer Journey Analytics, [create a derived field](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/derived-fields).

         For example, to view summary data for campaigns, create a derived field for the dimension `Adobe Advertising Campaign`.
         
         You'll link the two datasets using the matching key `trackingCode` (which is the schema field for the Adobe Advertising ID).
       
         * In the [!UICONTROL Lookup] section of the derived rule builder:
         
           * For the **[!UICONTROL Value]** field, select "[!UICONTROL Tracking Code]" from the metrics summary dataset.

           * For the **[!UICONTROL Lookup dataset]** field, select the dimensions dataset (such as "Adobe Advertising Classification").

           * For the **[!UICONTROL Matching Key]** field, select "[!UICONTROL Tracking Code]" from the classification dataset.

           * For the **[!UICONTROL Values to return]** field, select the dimension (such as "[!UICONTROL Adobe Advertising Campaign]")" from the classification dataset.
         
         The derived field name is appended with "(DF)", such as `Adobe Advertising Campaign(DF)`. 
         
       * For each derived field:
       
         * In the [!UICONTROL Included components] section, add the derived field.
         
           Two names are now listed for the same dimension (for example, "Adobe Advertising Campaign(DF)" (the derived field) and "Adobe Advertising Campaign" (the field in the summary dataset)).

         * Select the dimension in the summary dataset (such as "Adobe Advertising Campaign") and edit the settings for the dataset.

           The settings open on the right.

           * In the the Summary Data Group section, select the option to **[!UICONTROL Create grouping]**.

           * For the **[!UICONTROL Dimension]** field, select the derived field (which is appended with "(DF)," such as "Adobe Advertising Campaign(DF)").
         
           * Select the option to **[!UICONTROL Hide in reporting]**, which hides the derived field name in Workspace.

-->

## Configurare rapporti e visualizzazioni in Customer Journey Analytics Workspace {#cja-reports}

In Customer Journey Analytics Workspace, segui questi passaggi per configurare rapporti e visualizzazioni. Un analista web può eseguire queste attività.

1. [Crea un progetto](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/build-workspace-project/create-projects) in Workspace per creare rapporti e visualizzazioni in base alle dimensioni e alle metriche configurate nella visualizzazione dati.

Puoi classificare sia le metriche di riepilogo che i dati evento utilizzando la stessa dimensione in una tabella a forma libera.

1. (Se si dispone di dati di [!DNL Google Ads] o [!DNL Microsoft Advertising]) Creare un report delle conversioni tracciate dall&#39;editore utilizzando i campi per le metriche specifiche della rete di annunci, raggruppati come `googleConversions` e `microsoftConversions`.

>[!TIP]
>
>Gli eventi di riepilogo in genere aggiungono una piccola quantità di dati aggiuntivi ai rapporti, ad esempio alcuni eventi aggiuntivi, una sessione aggiuntiva al giorno o una persona in più per rapporto. Queste aggiunte sono trascurabili rispetto agli eventi web standard. Tuttavia, è possibile filtrare questi dati di evento di riepilogo aggiuntivi escludendo i dati per l&#39;ID persona fittizio `00000000-0000-0000-0000-000000000000`.
>![Esempio di esclusione di dati tramite un ID persona](/help/integrations/assets/cja-report-with-person-id.png "Esempio di esclusione di dati tramite un ID persona")

![Visualizzazione dei set di dati in Customer Journey Analytics](/help/integrations/assets/cja-report-example.png "Visualizzazione dei set di dati in Customer Journey Analytics")

>[!MORELIKETHIS]
>
>* [Panoramica](overview.md)
>* [Prerequisiti](prerequisites.md)
>* [ID Adobe Advertising utilizzati da [!DNL Customer Journey Analytics]](ids.md)
>* [Metriche e dimensioni di Adobe Advertising in Customer Journey Analytics](advertising-data-in-cja.md)
>* [Raccogliere dati storici per gli ID AMO e gli ID EF da utilizzare in Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
>* [Guida di Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-landing)
>* Guida utente di Customer Journey Analytics [per gli utenti di Adobe Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/compare-aa-cja/aa-to-cja-user)
