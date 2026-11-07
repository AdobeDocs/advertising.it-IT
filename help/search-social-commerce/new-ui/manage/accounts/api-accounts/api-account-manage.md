---
title: (Nuova interfaccia) Gestione degli account di rete degli annunci
description: Scopri come impostare e gestire i dettagli dell’account nella nuova interfaccia utente per una rete di annunci sincronizzata tramite l’API della rete di annunci.
feature: Search Campaign Management
exl-id: a50b2943-7568-401c-be5b-ff6f62629488
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
source-git-commit: b568da9300e9adb8d189811c3c8b52516dfcef6f
workflow-type: tm+mt
source-wordcount: '3141'
ht-degree: 0%
---
# (Nuova interfaccia) Gestire gli account di rete degli annunci tramite la connessione API

Queste istruzioni spiegano come gestire gli account di rete di annunci sincronizzati tramite API da Search, Social e Commerce, inclusi autenticazione, aggiornamento della connessione e controlli dello stato.

Per creare, modificare o autenticare nuovamente gli account, è necessario disporre dell&#39;autorizzazione per la modifica degli account.

Per informazioni dettagliate sulle funzionalità disponibili per ogni rete di annunci, vedi &quot;[Inventario supportato](/help/search-social-commerce/introduction/supported-inventory.md).&quot;

## Informazioni sulla visualizzazione [!UICONTROL Accounts] {#account-view-about}

Nella visualizzazione [!UICONTROL Manage] > [!UICONTROL Accounts] sono elencati tutti gli account di rete degli annunci nella visualizzazione filtrata per l&#39;account dell&#39;inserzionista selezionato. Fare clic sul nome di un account per aprire la visualizzazione [!UICONTROL Campaigns] filtrata per l&#39;account.

### Autenticazione dell’account e stato di accesso {#authentication-status}

I dettagli di autenticazione e accesso variano a seconda della rete di annunci e delle informazioni disponibili per l’account. Un account abilitato o autenticato correttamente può ancora disporre di autorizzazioni mancanti.

Le colonne seguenti mostrano lo stato dell’account, l’autenticazione e i dettagli di accesso:

* **[!UICONTROL Status]:** Lo stato operativo dell&#39;account, separato dalle autorizzazioni e dall&#39;autenticazione. Un account abilitato può sincronizzare i dati con la rete di annunci e utilizzare le funzioni di gestione e ottimizzazione dell’account supportate. Un account disabilitato interrompe l’attività in Search, Social e Commerce. La visualizzazione dello stato dell&#39;account utilizza un indicatore verde per **[!UICONTROL Enabled]**, un indicatore rosso per **[!UICONTROL Disabled]** e un indicatore giallo per **[!UICONTROL Pending]**. È possibile [abilitare o disabilitare gli account](#enable-disable-account) dalla visualizzazione o dalle impostazioni dell&#39;account.

* **[!UICONTROL Authenticated]:** se l&#39;account è autenticato:

  * **[!UICONTROL Yes]:** L&#39;account è autenticato.

  * **[!UICONTROL No]:** L&#39;account non è autenticato. Quando è disponibile un errore di autenticazione, posiziona il cursore sull’icona di avviso rossa per visualizzarlo.

  * **[!UICONTROL Not Applicable]:** L&#39;autenticazione non è applicabile perché i dati per l&#39;account vengono caricati anziché connettersi tramite un&#39;API.

  * **[!UICONTROL Expiring in N days]**, **[!UICONTROL Expiring today]** o **[!UICONTROL Expired]:** Un avviso di scadenza token sostituisce **[!UICONTROL Yes]** quando le informazioni di scadenza sono disponibili e il token scade tra 14 giorni o meno oppure è già scaduto. Fai clic sull&#39;icona di avviso per visualizzare i dettagli di accesso dell&#39;account e [autenticare di nuovo](#reauthenticate).

* **[!UICONTROL Manager Account for Cross-Account Conversions]:** ([!DNL Google Ads] account) L&#39;ID dell&#39;account manager associato utilizzato per i caricamenti di conversione tra account. Quando è disponibile un errore per l’account manager, accanto all’ID viene visualizzata un’icona di avviso. Per visualizzare l’errore, posiziona il cursore sull’icona. Le credenziali dell&#39;account manager sono separate dalle credenziali dell&#39;account di rete dell&#39;annuncio. Per aggiungere o aggiornare le credenziali dell&#39;account manager, utilizzare **[!UICONTROL Setup]** > **[!UICONTROL Manager Accounts]**. Consulta &quot;[Gestire gli account manager](/help/search-social-commerce/new-ui/set-up/manager-account-manage.md).&quot;

* **[!UICONTROL Access Level]:** Il livello di accesso dell&#39;account segnalato, ad esempio **[!UICONTROL Full]**, **[!UICONTROL Limited]**, **[!UICONTROL None]** o **[!UICONTROL Not Applicable]** quando non è disponibile alcun valore del livello di accesso.

  Se mancano le autorizzazioni, fai clic sull’icona di avviso per visualizzare i dettagli di accesso dell’account. Nella sezione **[!UICONTROL Access]** le autorizzazioni sono elencate come **[!UICONTROL Granted]** o **[!UICONTROL Missing]**. Quando i dettagli sull&#39;impatto sono disponibili, la sezione **[!UICONTROL Not working]** elenca le funzionalità interessate. Per [autenticare nuovamente](#reauthenticate) e aggiornare le autorizzazioni, fare clic su **[!UICONTROL Update Access]**.

### Azioni disponibili

Le azioni disponibili dipendono dalle autorizzazioni e dal tipo di account.

* [Crea dettagli account di rete dell’annuncio](#create-account)

* [Modifica i dettagli dell’account di rete dell’annuncio](#edit-account)

* [Autenticazione di un account di rete di annunci](#reauthenticate)

* [Attivare o disattivare gli account di rete degli annunci](#enable-disable-account)

* [Sincronizzare i dati dell’account con la rete dell’annuncio](sync-api-accounts.md)

* [Visualizzare un grafico delle prestazioni nella visualizzazione [!UICONTROL Accounts]](#account-performance-graph)

* [Gestisci i report di visualizzazione dati dalla visualizzazione [!UICONTROL Accounts]](#account-reports)

## Crea dettagli account di rete dell’annuncio {#create-account}

Per abilitare la sincronizzazione di un account, è necessario creare un record account corrispondente contenente le credenziali di accesso e le opzioni di verifica dell&#39;account e con lo stato *abilitato*.

>[!NOTE]
>
>Per creare un account effettivo sulla rete di annunci, vai al sito web della rete di annunci.

1. Nel menu principale, fare clic su **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. Fare clic su **[!UICONTROL Create Account]**.

1. Fai clic sul nome della rete di annunci per aprire la configurazione dell’account.

1. (Tutte le reti di annunci tranne [!DNL ChatGPT Ads] e [!DNL Yandex]) Nella scheda **[!UICONTROL Authenticate]**, completa l&#39;accesso nella finestra popup utilizzando le credenziali dell&#39;inserzionista e concedi l&#39;accesso all&#39;account richiesto.

   La schermata di installazione si aggiorna automaticamente e visualizza **[!UICONTROL Authentication Successful]** quando l&#39;autenticazione ha esito positivo. Per riaprire la finestra di accesso, fare clic su **[!UICONTROL Open login again]**. Se il browser blocca la finestra, modifica le impostazioni del browser per consentire la visualizzazione di popup per il sito.

   Per [!DNL Meta Ads], un avviso identifica eventuali autorizzazioni mancanti e il loro impatto. Autenticazione riuscita non significa necessariamente che tutte le autorizzazioni richieste siano state concesse.

   Fare clic su **[!UICONTROL Next]** per continuare.

1. Specifica le [impostazioni account](#account-settings-api) in ogni scheda disponibile. Per gli account autenticati in un popup, selezionare l&#39;account da sincronizzare da **[!UICONTROL Linked Ad Accounts]** nella scheda **[!UICONTROL Select Accounts]**.

1. Fare clic su **[!UICONTROL Save]**.

   I dati recenti relativi ai costi e ai clic per tutte le campagne nell’account vengono aggiornati nelle ore di Search, Social e Commerce. Per impostazione predefinita, i dati sono disponibili per gli ultimi 5-10 giorni, a seconda della rete di annunci. Quando necessario, tuttavia, il team di avvio del progetto può recuperare i dati per un massimo di 60 giorni.

## Modifica i dettagli dell’account di rete dell’annuncio {#edit-account}

Per abilitare o disabilitare l&#39;attività su un account, modificare i parametri di tracciamento predefiniti in un account o modificare le suite di rapporti [!DNL Analytics] da utilizzare per il tracciamento e il reporting, modificare i dettagli dell&#39;account. Per aggiornare la connessione o le autorizzazioni di aggiornamento, è possibile [autenticare nuovamente l&#39;account](#reauthenticate) dalle impostazioni dell&#39;account o dalla visualizzazione [!UICONTROL Accounts].

>[!NOTE]
>
>Per modificare un account effettivo sulla rete di annunci, vai al sito web della rete di annunci.

1. Nel menu principale, fare clic su **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. Selezionare l&#39;account in uno dei modi seguenti:

   * Selezionare la casella di controllo accanto al nome dell&#39;account, quindi fare clic su **[!UICONTROL Edit]** nella barra degli strumenti Azioni collettive.

   * Posizionare il cursore sul nome dell&#39;account, fare clic su **...** e quindi su **[!UICONTROL Edit]**.

1. Modifica le [impostazioni account](#account-settings-api) nelle schede disponibili.

1. Fare clic su **[!UICONTROL Save]**.

   >[!NOTE]
   >
   >Search, Social e Commerce devono sincronizzare i nuovi dati dell&#39;account con quelli della rete pubblicitaria. Questo accade automaticamente una volta al giorno, o più spesso quando Search, Social &amp; Commerce rileva le modifiche sulla rete di annunci.

## Autenticazione di un account di rete di annunci {#reauthenticate}

*Per gli account che utilizzano l&#39;autenticazione popup; non applicabile a [!DNL ChatGPT Ads] o [!DNL Yandex] account*

Per aggiornare la connessione di rete dell’annuncio o le autorizzazioni di aggiornamento per l’account, autentica nuovamente l’account.

1. (Se hai effettuato l’accesso a un altro account per la stessa rete di annunci nella stessa applicazione del browser) Esci da qualsiasi account diverso da quello dell’inserzionista.

1. Nel menu principale, fare clic su **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. Apri l’autenticazione in uno dei seguenti modi:

   * (Quando il valore **[!UICONTROL Authenticated]** dell&#39;account è **[!UICONTROL No]**) Posizionare il cursore sul nome dell&#39;account, fare clic su **...**, quindi fare clic su **[!UICONTROL Re authenticate]**, se disponibile.

   * (Quando viene visualizzato un avviso di scadenza del token) Fare clic sull&#39;icona di avviso nella colonna **[!UICONTROL Authenticated]**, quindi fare clic su **[!UICONTROL Reauthenticate]**.

   * (Se mancano le autorizzazioni) Fare clic sull&#39;icona di avviso nella colonna **[!UICONTROL Access Level]**, quindi fare clic su **[!UICONTROL Update Access]**.

   * (Dalle impostazioni dell&#39;account) Selezionare la casella di controllo accanto al nome dell&#39;account e fare clic su **[!UICONTROL Edit]** nella barra degli strumenti Azioni in blocco oppure posizionare il cursore sul nome dell&#39;account, fare clic su **...** e quindi su **[!UICONTROL Edit]**. Nella scheda **[!UICONTROL Account Details]** in **[!UICONTROL Account Authentication]** fare clic su **[!UICONTROL Re authenticate]**.

1. Completa l’accesso nella finestra a comparsa utilizzando le credenziali dell’inserzionista e concedi l’accesso all’account richiesto.

   Il nuovo token di accesso viene salvato automaticamente al completamento della nuova autenticazione. Se si modificano anche altre impostazioni dell&#39;account, fare clic su **[!UICONTROL Save]** per salvare le modifiche.

   Per [!DNL Meta Ads], un messaggio informativo identifica le autorizzazioni ancora mancanti dopo la riautenticazione riuscita. Per identificare la funzionalità interessata, esaminare i [dettagli di accesso](#authentication-status).

## Attivare o disattivare gli account di rete degli annunci {#enable-disable-account}

Quando abiliti un account di ad network, Search, Social e Commerce sincronizzano i dati della campagna con l’account (se supportato) e inviano offerte automatizzate e/o budget delle campagne nei portfolio. Quando disattivi un account di rete di annunci, Search, Social e Commerce interrompe tutte le attività sull’account. I dati raccolti mentre l’account era attivo vengono comunque memorizzati, ma le visualizzazioni e i rapporti di gestione delle campagne non includono i dati per il periodo di tempo in cui l’account è disabilitato. In seguito, potrai riabilitare l’account per riprendere l’attività con l’account.

1. Nel menu principale, fare clic su **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. Effettuare una delle seguenti operazioni:

   * (Dalla visualizzazione [!UICONTROL Accounts]):

     * (Per abilitare l&#39;account) Selezionare la casella di controllo accanto al nome dell&#39;account, quindi fare clic su **[!UICONTROL Enable]** nella barra degli strumenti Azioni collettive.

     * (Per disabilitare l&#39;account) Selezionare la casella di controllo accanto al nome dell&#39;account, quindi fare clic su **[!UICONTROL Disable]** nella barra degli strumenti Azioni collettive.

   * (dalle impostazioni account):

     1. Selezionare l&#39;account in uno dei modi seguenti:

        * Posizionare il cursore sul nome dell&#39;account, fare clic su **...** e quindi su **[!UICONTROL Edit]**.

        * Selezionare la casella di controllo accanto al nome dell&#39;account, quindi fare clic su **[!UICONTROL Edit]** nella barra degli strumenti Azioni collettive.

     1. Nella scheda **[!UICONTROL Account Details]**, attivare **[!UICONTROL Account Enabled]** per abilitare l&#39;account o disattivarlo per disabilitarlo.

     1. Fare clic su **[!UICONTROL Save]**.

## Visualizzare un grafico delle prestazioni nella visualizzazione [!UICONTROL Accounts] {#account-performance-graph}

Apri e configura un grafico delle prestazioni con un massimo di tre metriche calcolate sugli account nella vista filtrata per l’intervallo di date e la valuta specificati.

### Visualizzare un grafico delle prestazioni

1. Nel menu principale, fare clic su **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. Specifica l’intervallo di date e applica eventuali filtri per gli account di cui desideri visualizzare le prestazioni.

1. Sopra la tabella dati, fare clic su ![Grafici](/help/search-social-commerce/assets/charts.png "Grafici").

1. (Facoltativo) Utilizzare **[!UICONTROL Currency]** e **[!UICONTROL Metrics]** per specificare la valuta e fino a tre metriche da includere nel grafico.

### Nascondere un grafico delle prestazioni visibile

* Sopra la tabella dati, fare clic su ![Grafici](/help/search-social-commerce/assets/charts.png "Grafici").

## Gestisci i report di visualizzazione dati dalla visualizzazione [!UICONTROL Accounts] {#account-reports}

Generare un report che includa le righe di dati per uno o più account nella visualizzazione [!UICONTROL Accounts], quindi scaricare il report come file del foglio di lavoro di Microsoft Excel (formato XLSX). Il rapporto include le colonne visibili nella vista per l’intervallo di date specificato.

Puoi eliminare i rapporti completati e quelli non generati.

### Generare un rapporto con le righe di dati filtrate

1. Nel menu principale, fare clic su **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. Specifica l’intervallo di date e applica eventuali filtri per i dati da scaricare.

1. Specificare gli account di cui si desidera scaricare i dati:

   * Per scaricare i dati per account specifici, seleziona le caselle di controllo accanto agli account.

   * Per scaricare i dati per tutti gli account nella visualizzazione filtrata, lasciare deselezionate tutte le caselle di controllo.

1. Nella barra degli strumenti sopra la tabella dati, fare clic su ![Scarica report](/help/search-social-commerce/assets/download.png "Scarica report") **[!UICONTROL Reports]**.

1. Nella finestra di dialogo [!UICONTROL Grid Reports], mantieni **[!UICONTROL Report Name]** predefinito o immetti un altro nome, quindi fai clic su **[!UICONTROL Generate]**.

   Il report viene aggiunto all&#39;elenco **[!UICONTROL Recently Generated]**.

1. (Facoltativo) Per scaricare il file una volta completato, fai clic su ![Scarica](/help/search-social-commerce/assets/download.png "Scarica") accanto al nome del file.

   Il file viene scaricato in base alla normale procedura del browser.

### Scaricare un rapporto completato

1. Nel menu principale, fare clic su **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. Nella barra degli strumenti sopra la tabella dati, fare clic su ![Scarica report](/help/search-social-commerce/assets/download.png "Scarica report") **[!UICONTROL Reports]**.

1. Nell&#39;elenco **[!UICONTROL Recently Generated]** della finestra di dialogo [!UICONTROL Grid Reports], fare clic su ![Scarica](/help/search-social-commerce/assets/download.png "Scarica") accanto al nome del file.

   Il file viene scaricato in base alla normale procedura del browser.

### Eliminare un rapporto

1. Nel menu principale, fare clic su **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. Nella barra degli strumenti sopra la tabella dati, fare clic su ![Scarica report](/help/search-social-commerce/assets/download.png "Scarica report") **[!UICONTROL Reports]**.

1. Nell&#39;elenco **[!UICONTROL Recently Generated]** della finestra di dialogo [!UICONTROL Grid Reports], fare clic su ![Elimina](/help/search-social-commerce/assets/delete-new.png "Elimina") accanto al nome di un report completato o di un report che non è stato generato.

1. Conferma l’eliminazione.

## Impostazioni dell’account di rete dell’annuncio {#account-settings-api}

Le impostazioni dell’account variano a seconda della rete di annunci. Potresti non visualizzare tutte le impostazioni qui sotto.

### Scheda [!UICONTROL Authenticate]

(Visibile durante la creazione di un account che utilizza l’autenticazione a comparsa) Connettiti alla rete di annunci utilizzando le credenziali dell’inserzionista. La scheda visualizza lo stato della connessione e include **[!UICONTROL Open login again]** per riaprire il popup di accesso.

### Scheda [!UICONTROL Select Accounts]/[!UICONTROL Account Details]

**[!UICONTROL Account Name]:** nome da visualizzare per l&#39;account in Search, Social e Commerce.

>[!NOTE]
>
>Se hai un’integrazione Search, Social e Commerce-Adobe Analytics e modifichi il nome dell’account di ricerca, chiedi al team del tuo account Adobe di aggiornare la mappatura.

**[!UICONTROL Linked Ad Accounts]:** (visibile durante la creazione di un account che utilizza l&#39;autenticazione popup) L&#39;account di rete dell&#39;annuncio da sincronizzare. Scegli tra gli account annuncio collegati all’accesso alla rete.

**[Dettagli di accesso]:** ([!DNL Yandex] account) Le credenziali dell&#39;account da utilizzare:

* **[!UICONTROL Login]:** Nome o ID di accesso per abilitare l&#39;accesso API all&#39;account.

* **[!UICONTROL Password]:** La password per l&#39;account.

* **[!UICONTROL Access Key]:** Chiave di accesso per l&#39;account sviluppatore da utilizzare.

* **[!UICONTROL Application ID]:** Token sviluppatore da utilizzare per l&#39;account. Lo stesso token viene utilizzato per tutti gli account [!DNL Yandex].

* **[!UICONTROL Purse Campaign ID]:** ([!DNL Yandex] account con l&#39;impostazione Account condiviso disabilitato solo; facoltativo) ID numerico per la campagna utilizzato per pagare tutte le campagne pubblicitarie nell&#39;account.

* **[!UICONTROL Finance Token]:** ([!DNL Yandex] account con l&#39;impostazione Account condiviso disabilitato solo; facoltativo) Il token sviluppatore per le chiamate API relative ai dati finanziari, ad esempio la riallocazione di denaro tra le campagne pubblicitarie per l&#39;ottimizzazione del portfolio.

**[!UICONTROL Currency]:** (sola lettura) L&#39;abbreviazione della valuta utilizzata per l&#39;account. Questo valore viene compilato automaticamente con la valuta configurata per l’account sulla rete di annunci una volta salvato il record.

**[!UICONTROL Time Zone]:** Fuso orario dell&#39;inserzionista. Questo valore viene compilato automaticamente con il fuso orario configurato per l&#39;account Search, Social e Commerce dell&#39;inserzionista una volta salvato il record.

**[!UICONTROL Login]:** (sola lettura) Account utente utilizzato per accedere all&#39;account.

**[!UICONTROL Account Synchronization and Management]> [!UICONTROL Account Enabled]:** Search, Social e Commerce sincronizzano i dati della campagna con l&#39;account (se supportato) e inviano offerte automatizzate e/o budget delle campagne nei portfolio.

**[!UICONTROL Account Authentication]> [!UICONTROL Re authenticate]:** (visibile durante la modifica di un account che utilizza l&#39;autenticazione popup) Aggiorna le autorizzazioni della connessione o dell&#39;account. Il nuovo token di accesso viene salvato automaticamente al completamento della nuova autenticazione.

## Scheda [!UICONTROL Setup Tracking]

<!-- This should be the name of the whole left side of options -- they're all enabled/disabled depending on whether you enable our tracking -->

**[!UICONTROL Search, Social, & Commerce Tracking]:** se abilitare o meno il tracciamento utilizzando il servizio di tracciamento delle conversioni di Adobe Advertising. Questo metodo genera ID univoci di tracciamento dei clic e reindirizza gli utenti al server Adobe Advertising a scopo di tracciamento prima di inviarli alla pagina di destinazione del client. Questo metodo dispone di opzioni di tracciamento predefinite che puoi personalizzare facoltativamente e che puoi anche specificare parametri da aggiungere a ogni URL.

Per abilitare questa funzionalità, attivare **[Abilita tracciamento]**.

>[!NOTE]
>
>* Se modifichi questa impostazione, devi rigenerare gli URL di tracciamento per l’account.
>* Le opzioni di tracciamento a livello di campagna sostituiscono le impostazioni a livello di account.

**[!UICONTROL Tracking Type]:** (quando il tracciamento di Search, Social e Commerce è abilitato) Il metodo di reindirizzamento degli utenti finali all&#39;URL finale o all&#39;URL di destinazione. L’opzione selezionata è applicabile a tutte le unità di offerta nell’account o nella campagna. L&#39;impostazione predefinita a livello di account viene ereditata dalle impostazioni di tracciamento dell&#39;inserzionista e l&#39;impostazione predefinita a livello di campagna viene ereditata dalle impostazioni dell&#39;account.

* *[!UICONTROL Standard]:* Per reindirizzare l&#39;utente finale all&#39;URL specificato.

* *[!UICONTROL Token]:* Per reindirizzare l&#39;utente finale all&#39;URL e registrare anche l&#39;ID Search, Social e Commerce per il clic (`ef_id`) come parametro della stringa di query, utilizzato come token. Scegliere questa opzione se si desidera creare rapporti sulle transazioni non in linea, se si desidera che Search, Social e Commerce scambino dati con Adobe Analytics o se si desidera tenere traccia di tutte le conversioni che si verificano nei browser [!DNL Apple Safari].

>[!NOTE]
>
>* Se passi da [!UICONTROL Standard] a [!UICONTROL Token] o viceversa, devi rigenerare gli URL di tracciamento per l&#39;account.
>* Puoi sovrascrivere l’impostazione a livello di account a livello di campagna.

**[!UICONTROL Auto Update]:** (quando il tracciamento di Ricerca, Social e Commerce è abilitato) Standardizza gli URL di tracciamento per verificarne la compatibilità tra browser e server. Search, Social e Commerce caricano automaticamente i seguenti elementi nella rete di annunci durante la successiva sincronizzazione: (a) parametri di tracciamento di Search, Social e Commerce per i modelli di tracciamento e gli stessi parametri aggiunti agli URL finali; (b) nuovi URL di destinazione incorporati con il codice di tracciamento di Search, Social e Commerce. Per gli inserzionisti con un&#39;integrazione [Adobe Advertising-Adobe Analytics](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) e una configurazione AMO ID (s_kwcid) lato server, il caricamento include anche [parametri AMO ID](/help/integrations/analytics/ids.md#amo-id) per i tuoi account [!DNL Google Ads] e [!DNL Microsoft Advertising]. L&#39;impostazione predefinita a livello di account viene ereditata dalle impostazioni di tracciamento dell&#39;inserzionista. Puoi sovrascrivere l’impostazione a livello di account a livello di campagna.

Gli URL di tracciamento vengono aggiornati ogni giorno solo per le entità non sincronizzate, ovvero nuove entità aggiunte ed entità esistenti le cui proprietà sono state modificate. Pertanto, se modifichi questa impostazione da disabilitato a abilitato per un inserzionista/account/campagna esistente, gli URL di tracciamento non vengono aggiornati per le entità esistenti già sincronizzate. Per aggiungere il tracciamento agli URL delle entità sincronizzate esistenti, contatta il team dell’account Adobe e richiedi un processo di sincronizzazione manuale una tantum. Il processo di caricamento automatico gestisce le modifiche future.

**[!UICONTROL URL Encoding]:** (quando il monitoraggio di Search, Social e Commerce è abilitato; account con solo URL di destinazione) Codifica l&#39;URL di base nella barra degli indirizzi del browser dell&#39;utente finale (ad esempio `%3D` anziché `=`):

**[!UICONTROL Tracking Level]:** (quando il tracciamento di Ricerca, Social e Commerce è abilitato; disponibile a livello di account e campagna; non applicabile alle reti di annunci abilitate per il tracciamento parallelo) Il livello a cui tenere traccia di clic e ricavi aggiungendo un reindirizzamento e aggiungendo parametri agli URL rilevanti:

* *[!UICONTROL Keyword]:* Per tenere traccia dei dati solo a livello di parola chiave. Non disponibile per [!DNL Yandex].

* *[!UICONTROL Ad]:* Per tenere traccia dei dati solo a livello di annuncio. Non disponibile per [!DNL Naver].

* *[!UICONTROL Keyword and Ad]:* Per tenere traccia dei dati a livello di parola chiave e di annuncio. Non disponibile per [!DNL Naver] e [!DNL Yandex].

**[!UICONTROL Landing Page Suffix]** (solo account [!DNL Google Ads] e [!DNL Microsoft Advertising]; facoltativo) Qualsiasi parametro da aggiungere alla fine degli URL finali per tenere traccia delle informazioni; include tutti i parametri che l&#39;azienda deve monitorare.

Esempio: `param1=value1&param2=value2`

Gli account che utilizzano il tracciamento dei clic di Adobe Advertising devono includere nel suffisso l&#39;identificatore di clic della rete di annunci (`msclkid` per [!DNL Microsoft Advertising]; `gclid` per Google). Gli account con un’integrazione Adobe Analytics devono utilizzare il parametro AMO ID (a partire da `s_kwcid`). Se l’account dispone di un’implementazione AMO ID lato server, il parametro viene aggiunto automaticamente quando un utente fa clic su un annuncio; in caso contrario, devi aggiungerlo manualmente qui. Vedere i [formati di suffisso richiesti per [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) e [formati di suffisso richiesti per [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

>[!NOTE]
>
>* Questo campo non è aggiornato dall&#39;impostazione di tracciamento [!UICONTROL Auto Update].
>* I suffissi URL finali ai livelli inferiori sovrascrivono il suffisso a livello di account. Per una manutenzione più semplice, utilizza solo il suffisso a livello di account, a meno che non sia necessario un tracciamento diverso per i singoli componenti dell’account. Per configurare un suffisso a livello di gruppo di annunci o inferiore, utilizza l’editor della rete di annunci.

**URL di tracciamento account**: ([!DNL Google Ads], [!DNL LY Ads] e [!DNL Microsoft Advertising] account solo; facoltativo) Il modello di tracciamento predefinito per l&#39;account, che specifica tutti i reindirizzamenti del dominio di destinazione e i parametri di tracciamento e incorpora anche l&#39;URL della pagina finale/di destinazione in un parametro. Esempio: `{lpurl}?source={network}&id=5` o `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` per includere un reindirizzamento.

* Per incorporare l’URL finale:

  * ([!DNL Google Ads] e solo [!DNL Microsoft Advertising]) Per un elenco di parametri per indicare gli URL finali nei modelli di tracciamento, vedere ([!DNL Microsoft Advertising] only) [[!DNL Microsoft Advertising] documentation](https://help.ads.microsoft.com/#apex/3/en/56799) o ([!DNL Google Ads] only) i parametri &quot;Tracking template only&quot; nella sezione su &quot;Available [!DNL ValueTrack] Parameters&quot; nella [[!DNL Google Ads] documentation](https://support.google.com/google-ads/answer/6305348).

  * ([!DNL LY Ads] solo) Utilizzare il parametro `!{lpurl}` per indicare l&#39;URL della pagina di destinazione.

* Facoltativamente, puoi includere i parametri URL ed eventuali parametri personalizzati definiti per la campagna, separati da e commerciali (&amp;), ad esempio `{lpurl}?matchtype={matchtype}&device={device}`.

* Facoltativamente, puoi aggiungere reindirizzamenti e tracciamento di terze parti.

* Quando le impostazioni della campagna includono &quot;[!UICONTROL EF Redirect]&quot; e &quot;[!UICONTROL Auto Upload]&quot;, Search, Social e Commerce applicano automaticamente i prefissi al proprio codice di reindirizzamento e di tracciamento quando si salva il record.

>[!NOTE]
>
>* Per [!DNL Google Ads], evitare l&#39;utilizzo di macro, che non vengono sostituite dai clic provenienti da origini che abilitano il tracciamento parallelo. Se l’inserzionista deve utilizzare delle macro, l’Account Team di Adobe collabora con l’Assistenza clienti o con il team di implementazione per aggiungerle.
>* Il modello di tracciamento al livello più granulare sostituisce i valori a tutti i livelli superiori. Ad esempio, se entrambe le impostazioni account e parola chiave includono un valore, tale valore viene applicato.
>* Se aggiorni un modello di tracciamento a livello di annuncio, sitelink o parola chiave, gli annunci pertinenti vengono nuovamente inviati per la revisione. Puoi aggiornare i modelli di tracciamento a livello di account, campagna o gruppo di annunci senza inviare nuovamente gli annunci per l’approvazione.

## Scheda [!UICONTROL Set up Adobe Analytics]

Queste impostazioni sono disponibili per gli inserzionisti con un&#39;integrazione [[!DNL Adobe Analytics for Advertising] 1&rbrace;.](/help/integrations/analytics/overview.md)

**[!UICONTROL Adobe Analytics Report Suite]:** (Facoltativo) Una o più suite di rapporti di Analytics a cui Search, Social e Commerce invia i dati che raccoglie dalla rete di annunci, incluse le classificazioni delle entità e i dati di clic per l&#39;account. Questa funzionalità è disponibile solo per le reti di annunci supportate.<!-- What are the repercussions of changing the suites? Timing of updated data? -->

Affinché i dati vengano visualizzati nelle suite di rapporti, (a) la funzione AMO ID lato server deve essere configurata per l’account oppure (b) l’impostazione a livello di inserzionista su &quot;[!UICONTROL Enable Advertising reporting in Analytics]&quot; deve essere abilitata. Inoltre, l&#39;account [!DNL Analytics] dell&#39;inserzionista deve essere configurato per ricevere dati da Search, Social e Commerce. Per ulteriori informazioni, contatta il team del tuo account Adobe.

**[!UICONTROL Adobe Analytics Conversion Reporting]: [!UICONTROL Enable conversion reporting in Adobe Analytics]:** ([!DNL Meta Ads] account; facoltativo) aggiunge il parametro di tracciamento [AMO ID (s_kwcid)](/help/search-social-commerce/tracking/amo-id-tracking-parameter.md) a tutti gli annunci della campagna. Il parametro consente ad Adobe Analytics di associare le conversioni alle campagne Meta Ads nella suite di rapporti specificata, insieme alle classificazioni delle entità e ai dati sui clic.

>[!MORELIKETHIS]
>
>* [Informazioni sugli account di rete di annunci](../ad-network-account-about.md)
>* [Gestione account centro esercenti](/help/search-social-commerce/new-ui/set-up/manager-account-manage.md)
>* [Aggiorna il codice di tracciamento s_kwcid per a [!DNL Google Ads] account](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md)
