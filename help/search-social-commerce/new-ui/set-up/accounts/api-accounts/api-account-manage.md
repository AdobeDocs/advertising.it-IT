---
title: (Nuova interfaccia) Gestione degli account di rete degli annunci
description: Scopri come impostare e gestire i dettagli dell’account nella nuova interfaccia utente per una rete di annunci sincronizzata tramite l’API della rete di annunci.
feature: Search Campaign Management
source-git-commit: e62eb730ec88a37cbe34e35d7b9bf99e0d4fd41d
workflow-type: tm+mt
source-wordcount: '2129'
ht-degree: 0%

---

# (Nuova interfaccia) Gestire gli account di rete degli annunci tramite la connessione API

<!-- Besides just logging into an account, do you have to make any other choices once you're logged in (such as to give speciic permissions to SSC?  And what about oAuth tokens -- do we still use them? -->

*funzionalità Beta*

<!-- Move out info about Naver into a separate page -->

Di seguito sono riportate le istruzioni per la gestione degli account di rete di annunci sincronizzati da Search, Social e Commerce tramite l’API della rete di annunci.

<!-- Move out info about Naver into a separate page -->

Per informazioni dettagliate sulle funzionalità disponibili per ogni rete di annunci, vedi &quot;[Inventario supportato](/help/search-social-commerce/introduction/supported-inventory.md).&quot;

## Crea dettagli account di rete dell’annuncio {#create-account}

Per abilitare la sincronizzazione di un account, è necessario creare un record account corrispondente contenente le credenziali di accesso e le opzioni di verifica dell&#39;account e con lo stato *abilitato*.

>[!NOTE]
>
>Per creare un account effettivo sulla rete di annunci, vai al sito web della rete di annunci.

1. Nel menu principale, fare clic su **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Fare clic su **[!UICONTROL Create Account]**.

1. Fare clic sul nome della rete di annunci e quindi su **[!UICONTROL Next]**.

1. (Tutte le reti di annunci tranne [!DNL Yandex]) Accedi alla rete di annunci utilizzando le credenziali dell&#39;inserzionista. Selezionare l&#39;opzione &quot;Registrazione account per questo account&quot;. Quindi, in alto a destra, fare clic su **[!UICONTROL Next]**.

1. Specificare le [impostazioni account](#account-settings-api):

   1. Nella scheda **[!UICONTROL Select Accounts]** specificare le impostazioni generali dell&#39;account. Per gli account [!DNL Yandex], specificare le credenziali account.

   1. Fare clic sulla scheda **[!UICONTROL Setup Tracking]** e immettere le impostazioni di verifica.

   1. (Inserzionisti con un&#39;integrazione [[!DNL Adobe Analytics for Advertising] 1&rbrace;) Fai clic sulla scheda &#x200B;](/help/integrations/analytics/overview.md) e seleziona tutte le **[!UICONTROL Set up Adobe Analytics]** suite di rapporti da utilizzare per il tracciamento e il reporting dell&#39;attività della campagna.[!DNL Analytics]

1. Fare clic su **[!UICONTROL Save]**.

   I dati recenti relativi ai costi e ai clic per tutte le campagne nell’account vengono aggiornati nelle ore di Search, Social e Commerce. Per impostazione predefinita, i dati sono disponibili per gli ultimi 5-10 giorni, a seconda della rete di annunci. Quando necessario, tuttavia, il team di avvio del progetto può recuperare i dati per un massimo di 60 giorni.

## Modifica i dettagli dell’account di rete dell’annuncio {#edit-account}

Per autenticare nuovamente le impostazioni dell&#39;account per aggiornare la connessione o le autorizzazioni di aggiornamento, abilitare o disabilitare l&#39;attività su un account, modificare i parametri di tracciamento predefiniti in un account o modificare le suite di rapporti [!DNL Analytics] da utilizzare per il tracciamento e il reporting, quindi modificare i dettagli dell&#39;account.

>[!NOTE]
>
>Per modificare un account effettivo sulla rete di annunci, vai al sito web della rete di annunci.

1. Nel menu principale, fare clic su **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Selezionare l&#39;account in uno dei modi seguenti:

   * Selezionare la casella di controllo accanto al nome dell&#39;account, quindi fare clic su **[!UICONTROL Edit]** nella barra degli strumenti Azioni collettive.

   * Posizionare il cursore sul nome dell&#39;account, fare clic su **...** e quindi su **[!UICONTROL Edit]**.

1. Modifica le [impostazioni account](#account-settings-api):

   1. (Facoltativo) Nella scheda **[!UICONTROL Account Details]**, modificare i dettagli dell&#39;account.

   1. (Facoltativo) Fare clic sulla scheda **[!UICONTROL Setup Tracking]** e modificare le impostazioni di tracciamento.

   1. (Facoltativo; inserzionisti con un&#39;integrazione [[!DNL Adobe Analytics for Advertising] 1&rbrace;) Fai clic sulla scheda &#x200B;](/help/integrations/analytics/overview.md) e modifica le suite di rapporti **[!UICONTROL Set up Adobe Analytics]** da utilizzare per il tracciamento e il reporting dell&#39;attività della campagna.[!DNL Analytics]

   <!-- What are the repercussions of changing the suites? Timing of updated data? -->

1. Fare clic su **[!UICONTROL Save]**.

   >[!NOTE]
   >
   >Search, Social e Commerce devono sincronizzare i nuovi dati dell&#39;account con quelli della rete pubblicitaria. Questo accade automaticamente una volta al giorno, o più spesso quando Search, Social &amp; Commerce rileva le modifiche sulla rete di annunci.

## Autenticazione di un account di rete di annunci {#reauthenticate}

Per aggiornare la connessione di rete dell’annuncio o le autorizzazioni di aggiornamento per l’account, autentica nuovamente l’account.

1. (Se hai effettuato l’accesso a un altro account per la stessa rete di annunci nella stessa applicazione del browser) Esci da qualsiasi account diverso da quello dell’inserzionista.

1. Nel menu principale, fare clic su **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

<!-- For Bing and Yandex, the right-click menu includes "Re authenticate." Clarify why just those types -->

1. Selezionare l&#39;account in uno dei modi seguenti:

   * Selezionare la casella di controllo accanto al nome dell&#39;account, quindi fare clic su **[!UICONTROL Edit]** nella barra degli strumenti Azioni collettive.

   * Posizionare il cursore sul nome dell&#39;account, fare clic su **...** e quindi su **[!UICONTROL Edit]**.

1. Nella scheda **[!UICONTROL Account Details]**, fare clic su **[!UICONTROL Re authenticate]** e accedere alla rete di annunci utilizzando le credenziali dell&#39;inserzionista.

1. Fare clic su **[!UICONTROL Save]**.

## Attivare o disattivare gli account di rete degli annunci {#enable-disable-account}

Quando abiliti un account di ad network, Search, Social e Commerce sincronizzano i dati della campagna con l’account (se supportato) e inviano offerte automatizzate e/o budget delle campagne nei portfolio. Quando disattivi un account di rete di annunci, Search, Social e Commerce interrompe tutte le attività sull’account. I dati raccolti mentre l’account era attivo vengono comunque memorizzati, ma le visualizzazioni e i rapporti di gestione delle campagne non includono i dati per il periodo di tempo in cui l’account è disabilitato. In seguito, potrai riabilitare l’account per riprendere l’attività con l’account.

1. Nel menu principale, fare clic su **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Effettuare una delle seguenti operazioni:

   * (Dalla visualizzazione [!UICONTROL Accounts]):

      * (Per abilitare l&#39;account) Selezionare la casella di controllo accanto al nome dell&#39;account, quindi fare clic su **[!UICONTROL Activate]** nella barra degli strumenti Azioni collettive.

      * (Per disabilitare l&#39;account) Selezionare la casella di controllo accanto al nome dell&#39;account, quindi fare clic su **[!UICONTROL Pause]** nella barra degli strumenti Azioni collettive.

   * (dalle impostazioni account):

      1. Selezionare l&#39;account in uno dei modi seguenti:

         * Posizionare il cursore sul nome dell&#39;account, fare clic su **...** e quindi su **[!UICONTROL Edit]**.

         * Selezionare la casella di controllo accanto al nome dell&#39;account, quindi fare clic su **[!UICONTROL Edit]** nella barra degli strumenti Azioni collettive.

      1. Nella scheda **[!UICONTROL Account Details]**, disattivare **[!UICONTROL Account enabled]**.

      1. Fare clic su **[!UICONTROL Save]**.

## Impostazioni dell’account di rete dell’annuncio {#account-settings-api}

Le impostazioni dell’account variano a seconda della rete di annunci. Potresti non visualizzare tutte le impostazioni qui sotto.

<!-- When you're creating new accounts only; not sure that you'll have anything to do here once you've authenticated

### Authenticate tab

-->

### Scheda [!UICONTROL Select Accounts]/[!UICONTROL Account Details]

**[!UICONTROL Account Name]:** nome da visualizzare per l&#39;account in Search, Social e Commerce.

>[!NOTE]
>
>Se hai un’integrazione Search, Social e Commerce-Adobe Analytics e modifichi il nome dell’account di ricerca, chiedi al team del tuo account Adobe di aggiornare la mappatura.

**[!DNL [Account di rete dell&#39;annuncio]]:** (visibile durante la creazione di un account) L&#39;account di rete dell&#39;annuncio da sincronizzare.

**[Dettagli di accesso]:** (solo account Yandex) Le credenziali dell&#39;account da utilizzare:

* **[!UICONTROL Login]:** Nome o ID di accesso per abilitare l&#39;accesso API all&#39;account.

* **[!UICONTROL Password]:** La password per l&#39;account.

* **[!UICONTROL Access Key]:** Chiave di accesso per l&#39;account sviluppatore da utilizzare.

* **[!UICONTROL Application ID]:** Token sviluppatore da utilizzare per l&#39;account. Lo stesso token viene utilizzato per tutti gli account [!DNL Yandex].

* **[!UICONTROL Purse Campaign ID]:** ([!DNL Yandex] account con l&#39;impostazione Account condiviso disabilitato solo; facoltativo) ID numerico per la campagna utilizzato per pagare tutte le campagne pubblicitarie nell&#39;account.

* **[!UICONTROL Finance Token]:** ([!DNL Yandex] account con l&#39;impostazione Account condiviso disabilitato solo; facoltativo) Token sviluppatore da utilizzare per le chiamate API relative ai dati finanziari, ad esempio per riallocare denaro dal wallet tra le campagne dell&#39;inserzionista in base alle esigenze di ottimizzazione del portfolio.

**[!UICONTROL Network Account ID]:** (tutte le reti di annunci tranne [!DNL Yandex] L&#39;ID account assegnato dalla rete di annunci.

>[!NOTE]
>
>Gli account del gestore della rete di annunci non sono supportati qui. Per identificare un account manager per [!DNL Microsoft Advertising], utilizzare rispettivamente il campo ID account principale o Account MCC. Per [configurare le credenziali per un account di manager [!DNL Google Ads] &#x200B;](/help/search-social-commerce/admin/manager-accounts.md), passare a [!UICONTROL Admin] \> [!UICONTROL Manager Accounts].

**[!UICONTROL Currency]:** (sola lettura) L&#39;abbreviazione della valuta utilizzata per l&#39;account. Questo valore viene compilato automaticamente con la valuta configurata per l’account sulla rete di annunci una volta salvato il record.

**[!UICONTROL Time Zone]:** Fuso orario dell&#39;inserzionista. Questo valore viene compilato automaticamente con il fuso orario configurato per l&#39;account Search, Social e Commerce dell&#39;inserzionista una volta salvato il record.

**[!UICONTROL Login]:** (sola lettura) Account utente utilizzato per accedere all&#39;account.

**[!UICONTROL Account Synchronization and Management]> [!UICONTROL Account Enabled]:** Search, Social e Commerce sincronizzano i dati della campagna con l&#39;account (se supportato) e inviano offerte automatizzate e/o budget delle campagne nei portfolio.

## Scheda [!UICONTROL Setup Tracking]

<!-- This should be the name of the whole left side of options -- they're all enabled/disabled depending on whether you enable our tracking -->

**[!UICONTROL Search, Social, & Commerce Tracking]:** Per abilitare o meno il tracciamento, utilizza il servizio di tracciamento delle conversioni di Adobe Advertising. Questo metodo genera ID univoci di tracciamento dei clic e reindirizza gli utenti al server Adobe Advertising a scopo di tracciamento prima di inviarli alla pagina di destinazione del client. Questo metodo dispone di opzioni di tracciamento predefinite che puoi personalizzare facoltativamente e che puoi anche specificare parametri da aggiungere a ogni URL.

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

Gli URL di tracciamento vengono aggiornati ogni giorno solo per le entità non sincronizzate, ovvero nuove entità aggiunte ed entità esistenti le cui proprietà sono state modificate. Pertanto, se modifichi questa impostazione da disabilitato a abilitato per un inserzionista/account/campagna esistente, gli URL di tracciamento non vengono aggiornati per le entità esistenti già sincronizzate. Per aggiungere il tracciamento agli URL delle entità sincronizzate esistenti, contatta il team dell’account Adobe e richiedi un processo di sincronizzazione manuale una tantum. Il processo di caricamento automatico gestirà le modifiche future.

**[!UICONTROL URL Encoding]:** (quando il monitoraggio di Search, Social e Commerce è abilitato; account con solo URL di destinazione) Codifica l&#39;URL di base nella barra degli indirizzi del browser dell&#39;utente finale (ad esempio `%3D` anziché `=`):

**[!UICONTROL Tracking Level]:** (quando il tracciamento di Ricerca, Social e Commerce è abilitato; disponibile a livello di account e campagna; non applicabile alle reti di annunci abilitate per il tracciamento parallelo) Il livello a cui devono essere tracciati i clic e i ricavi aggiungendo un reindirizzamento (se pertinente) e aggiungendo parametri agli URL rilevanti:

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

**URL di tracciamento account**: ([!DNL Google Ads], [!DNL Microsoft Advertising] e [!DNL Yahoo! Japan Ads] account solo; facoltativo) Il modello di tracciamento predefinito per l&#39;account, che specifica tutti i reindirizzamenti del dominio di destinazione e i parametri di tracciamento e incorpora anche l&#39;URL della pagina finale/di destinazione in un parametro. Esempio: `{lpurl}?source={network}&id=5` o `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` per includere un reindirizzamento.

* Per incorporare l’URL finale:

   * ([!DNL Google Ads] e solo [!DNL Microsoft Advertising]) Per un elenco di parametri per indicare gli URL finali nei modelli di tracciamento, vedere ([!DNL Microsoft Advertising] only) [[!DNL Microsoft Advertising] documentation](https://help.ads.microsoft.com/#apex/3/en/56799) o ([!DNL Google Ads] only) i parametri &quot;Tracking template only&quot; nella sezione su &quot;Available [!DNL ValueTrack] Parameters&quot; nella [[!DNL Google Ads] documentation](https://support.google.com/google-ads/answer/6305348).

   * ([!DNL Yahoo! Japan Ads] solo) Utilizzare il parametro `!{lpurl}` per indicare l&#39;URL della pagina di destinazione.

* Facoltativamente, puoi includere i parametri URL ed eventuali parametri personalizzati definiti per la campagna, separati da e commerciali (&amp;), ad esempio `{lpurl}?matchtype={matchtype}&device={device}`.

* Facoltativamente, puoi aggiungere reindirizzamenti e tracciamento di terze parti.

* Quando le impostazioni della campagna includono &quot;[!UICONTROL EF Redirect]&quot; e &quot;[!UICONTROL Auto Upload]&quot;, Search, Social e Commerce applicano automaticamente i prefissi al proprio codice di reindirizzamento e di tracciamento quando si salva il record.

>[!NOTE]
>
>* Per [!DNL Google Ads], evitare l&#39;utilizzo di macro, che non vengono sostituite dai clic provenienti da origini che abilitano il tracciamento parallelo. Se l’inserzionista deve utilizzare delle macro, il team dell’account di Adobe deve collaborare con l’Assistenza clienti o con il team di implementazione per aggiungerle.
>* Il modello di tracciamento al livello più granulare sostituisce i valori a tutti i livelli superiori. Ad esempio, se entrambe le impostazioni account e parola chiave includono un valore, tale valore viene applicato.
>* Se aggiorni un modello di tracciamento a livello di annuncio, sitelink o parola chiave, gli annunci pertinenti vengono nuovamente inviati per la revisione. Puoi aggiornare i modelli di tracciamento a livello di account, campagna o gruppo di annunci senza inviare nuovamente gli annunci per l’approvazione.

## Scheda [!UICONTROL Setup Analytics]

**[!UICONTROL Adobe Analytics Report Suite]:** (inserzionisti con un&#39;integrazione [[!DNL Adobe Analytics for Advertising] integration](/help/integrations/analytics/overview.md); facoltativo) Una o più suite di rapporti di Analytics a cui Search, Social e Commerce invia i dati che raccoglie dalla rete di annunci, incluse le classificazioni delle entità e i dati di clic per l&#39;account. Questa funzione è disponibile solo per le reti di annunci supportate.

Affinché i dati vengano visualizzati nelle suite di rapporti, (a) la funzione AMO ID lato server deve essere configurata per l’account oppure (b) l’impostazione a livello di inserzionista su &quot;[!UICONTROL Enable Advertising reporting in Analytics]&quot; deve essere abilitata. Inoltre, l&#39;account [!DNL Analytics] dell&#39;inserzionista deve essere configurato per ricevere dati da Search, Social e Commerce. Per ulteriori informazioni, contatta il team del tuo account Adobe.

>[!MORELIKETHIS]
>
>* [Informazioni sugli account di rete di annunci](../ad-network-account-about.md)
>* [Gestione account centro esercenti](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md)
>* [Aggiorna il codice di tracciamento s_kwcid per a [!DNL Google Ads] account](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md)
