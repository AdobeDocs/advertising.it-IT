---
title: Gestire gli account di rete degli annunci
description: Scopri come impostare e gestire i dettagli di un account di rete di annunci.
exl-id: 4038d03b-63e2-4953-89df-37f7b5f68652
feature: Search Campaign Management
source-git-commit: 304b3589109fe9ddf4d2f0df84c7fa45aa3726d2
workflow-type: tm+mt
source-wordcount: '2078'
ht-degree: 0%

---

# Gestire gli account di rete degli annunci

<!-- Probably need to change the page title. If I update the filename, get B. to create a redirect to the new URL. -->

Di seguito sono riportate le istruzioni per la creazione e la modifica dei dettagli dell&#39;account di rete, l&#39;aggiornamento del token [!DNL oAuth] per un account e la disattivazione degli account.

<!-- Move out info about Naver?  Then change to the following:  Following are instructions for creating and editing account details for an ad network account that Search, Social, & Commerce will sync using the ad network's API; refreshing the [!DNL oAuth] token for an account; and disabling accounts. -->

<!-- Also update Description metadata to "Learn how to set up and manage account details for an ad network account synced via the ad network API." -->

Per informazioni dettagliate sulle funzionalità disponibili per ogni rete di annunci, vedi &quot;[Inventario supportato](/help/search-social-commerce/introduction/supported-inventory.md).&quot;

## Crea dettagli account di rete dell’annuncio {#create-account}

*Solo i ruoli di account manager agenzia, manager account Adobe e amministratore*

Per abilitare la sincronizzazione o il tracciamento di un account, è necessario creare un record account corrispondente contenente le credenziali di accesso e le opzioni di tracciamento dell&#39;account e con lo stato *attivo*.

>[!NOTE]
>
>* Supporto non disponibile per i nuovi account [!DNL Baidu].
>* Per creare un account effettivo sulla rete di annunci, vai al sito web della rete di annunci.

1. Nel menu principale, fare clic su **[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Nel sottomenu, fare clic su **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Nella barra degli strumenti sopra la tabella dati, fare clic su ![Crea](/help/search-social-commerce/assets/add.png "Crea").

1. Specificare le [impostazioni account](#account-settings):

   1. Fare clic sul nome della rete di annunci e quindi su **[!UICONTROL Next]**.

   1. Nella sezione **[!UICONTROL Account Details]** immettere i dettagli dell&#39;account.

      Per le reti di annunci che utilizzano il tipo di autorizzazione di accesso &quot;[!UICONTROL oAuth]&quot;, consenti a Search, Social e Commerce di accedere all&#39;account utilizzando il [protocollo di autorizzazione OAuth](https://oauth.net/2/):

      1. Immettere il valore **[!UICONTROL Login]** per l&#39;account, immettere facoltativamente la password e quindi fare clic su **[!UICONTROL Authenticate]**.

         La best practice prevede l’utilizzo dell’accesso API all’account. Immetti la password quando desideri crittografarla e salvarla, in modo che il team dell’account Adobe possa aggiornare i token in base alle esigenze.

      1. (Se non hai effettuato l’accesso all’account dell’inserzionista) Accedi all’account dell’inserzionista. La best practice prevede l’utilizzo delle credenziali per l’accesso API all’account.

      1. Nella schermata di richiesta di autorizzazione/accesso, fai clic sul pulsante per confermare l’autorizzazione.

      1. Copiare la stringa di autenticazione nella finestra popup visualizzata e incollarla nel campo **[!UICONTROL oAuth Token]**.

      1. Specificare i dettagli dell&#39;account rimanenti.

   1. Fare clic su **[!UICONTROL Set Account Tracking]** e immettere le impostazioni di verifica.

1. Fare clic su **[!UICONTROL Post]**.

   I dati recenti relativi ai costi e ai clic per tutte le campagne nell’account sono disponibili in Search, Social e Commerce in circa 24 ore. Per impostazione predefinita, i dati sono disponibili per gli ultimi 5-10 giorni, a seconda della rete di annunci. Quando necessario, tuttavia, il team di avvio del progetto può recuperare i dati per un massimo di 60 giorni.

## Modifica i dettagli dell’account di rete dell’annuncio {#edit-account}

*Solo i ruoli di account manager agenzia, manager account Adobe e amministratore*

Se le credenziali dell’account cambiano, vuoi modificare i parametri di tracciamento predefiniti in un account, oppure vuoi abilitare o disabilitare l’attività su un account, quindi modificare i dettagli dell’account.

>[!NOTE]
>
>Per modificare un account effettivo sulla rete di annunci, vai al sito web della rete di annunci.

1. Nel menu principale, fare clic su **[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Nel sottomenu, fare clic su **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Posizionare il cursore sul nome dell&#39;account, fare clic su ![Altro](/help/search-social-commerce/assets/more-filters.png "Altro"), quindi selezionare **[!UICONTROL Edit]**.

1. Modifica le [impostazioni account](#account-settings):

   1. (Facoltativo) Modifica i dettagli dell’account.

   1. (Facoltativo) Fare clic su **[!UICONTROL Set Account Tracking]** e modificare le impostazioni di tracciamento.

1. Fare clic su **[!UICONTROL Post]**.

   >[!NOTE]
   >
   >Search, Social e Commerce devono sincronizzare i nuovi dati dell&#39;account con quelli della rete pubblicitaria. Questo accade automaticamente una volta al giorno, o più spesso quando Search, Social &amp; Commerce rileva le modifiche sulla rete di annunci.

## Aggiorna i token di accesso OAuth per gli account di ricerca {#refresh-oauth-tokens}

*Solo i ruoli di account manager agenzia, manager account Adobe e amministratore*

Se Search, Social e Commerce accedono all&#39;account utilizzando il protocollo di autorizzazione [OAuth](https://oauth.net/2/) e le credenziali dell&#39;account cambiano, oppure se è necessario un accesso aggiuntivo per supportare nuove funzionalità in Search, Social e Commerce, è necessario ottenere un nuovo token di accesso per l&#39;account.

Il team del tuo account Adobe ti informerà se nuove funzioni richiedono un nuovo token.

1. (Se hai effettuato l’accesso a un altro account per la stessa rete di annunci nella stessa applicazione del browser) Esci da qualsiasi account diverso da quello dell’inserzionista.

1. Nel menu principale, fare clic su **[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Nel sottomenu, fare clic su **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Posizionare il cursore sul nome dell&#39;account, fare clic su ![Altro](/help/search-social-commerce/assets/more-filters.png "Altro"), quindi selezionare **[!UICONTROL Edit]**.

1. Ottieni un nuovo token di accesso:

   1. Fare clic su **[!UICONTROL Get oAuth Token]**.

   1. (Se non hai effettuato l’accesso all’account dell’inserzionista) Accedi all’account dell’inserzionista. La best practice prevede l’utilizzo delle credenziali per l’accesso API all’account.

   1. Nella schermata di richiesta di autorizzazione/accesso, fai clic sul pulsante per confermare l’autorizzazione.

   1. Copiare la stringa di autenticazione nella finestra popup visualizzata e incollarla nel campo **[!UICONTROL oAuth Token]**.

1. Fare clic su **[!UICONTROL Post]**.

## Attivare o disattivare gli account di rete degli annunci {#enable-disable-account}

*Solo i ruoli di account manager agenzia, manager account Adobe e amministratore*

Quando abiliti un account di ad network, Search, Social e Commerce sincronizzano i dati della campagna con l’account (se supportato) e inviano offerte automatizzate e/o budget delle campagne nei portfolio. Quando disattivi un account di rete di annunci, Search, Social e Commerce interrompe tutte le attività sull’account. I dati raccolti mentre l’account era attivo vengono comunque memorizzati, ma le visualizzazioni e i rapporti di gestione delle campagne non includono i dati per il periodo di tempo in cui l’account è disabilitato. In seguito, potrai riabilitare l’account per riprendere l’attività con l’account.

1. Nel menu principale, fare clic su **[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Nel sottomenu, fare clic su **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Effettuare una delle seguenti operazioni:

   * Per modificare lo stato di un singolo account, posizionare il cursore sul nome dell&#39;account, fare clic su ![Altro](/help/search-social-commerce/assets/more-filters.png "Altro") e quindi selezionare **[!UICONTROL Edit]**. Modificare **[!UICONTROL Status]** in *Enabled* o *Disabled*, quindi fare clic su **[!UICONTROL Post]**.

   * Per modificare lo stato di uno o più account, effettuare le seguenti operazioni:

      1. Seleziona la casella di controllo accanto a ciascun account.

         Per suggerimenti sulla selezione di più righe, vedere &quot;[Selezionare più righe](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

      1. Nella barra degli strumenti sopra la tabella dati, fare clic su ![Icona Attiva](/help/search-social-commerce/assets/activate.png "Icona Attiva") per abilitare l&#39;account o su ![Icona Disattiva](/help/search-social-commerce/assets/disable.png "Icona Disattiva") per disabilitarlo.

## Impostazioni dell’account di rete dell’annuncio {#account-settings}

>[!NOTE]
>
>Solo gli utenti dell&#39;account manager, dell&#39;account manager di [!DNL Adobe] e dell&#39;amministratore possono configurare le impostazioni dell&#39;account.

### Dettagli account

**[!UICONTROL SE Account ID]:** (tutti gli account tranne [!DNL Naver] e [!DNL Yandex]; modificabile solo per i nuovi account) L&#39;ID account assegnato dalla rete di annunci.

>[!NOTE]
>
>Gli account del gestore della rete di annunci non sono supportati qui. Per identificare un account manager per [!DNL Microsoft Advertising] o [!DNL Yandex], utilizzare rispettivamente il campo ID account principale o Account MCC. Per [configurare le credenziali per un account di manager [!DNL Google Ads] &#x200B;](/help/search-social-commerce/admin/manager-accounts.md), passare a [!UICONTROL Admin] \> [!UICONTROL Manager Accounts].

**[!UICONTROL Account Name]:** nome da visualizzare per l&#39;account in Search, Social e Commerce.

>[!NOTE]
>
>Se hai un’integrazione Search, Social e Commerce-Adobe Analytics e modifichi il nome dell’account di ricerca, chiedi al team del tuo account Adobe di aggiornare la mappatura.

**[!UICONTROL Login Details]: \[Tipo di accesso\]** - ([!DNL Microsoft Advertising]/[!DNL Microsoft Merchant Center] only) Autorizzare gli accessi all&#39;account utilizzando:

* *[!UICONTROL oAuth]* (impostazione predefinita): per utilizzare il [[!DNL OAuth] protocollo di autorizzazione](https://oauth.net/2/).

* *[!UICONTROL Password]:* Per utilizzare la password del client.

Per gli account [!DNL Microsoft Advertising], è possibile utilizzare solo gli accessi autorizzati da [!DNL oAuth].

**[!UICONTROL Login Details]: [!UICONTROL Login]:** (tutte le reti di annunci tranne [!DNL Naver]) Nome o ID di accesso per abilitare l&#39;accesso API all&#39;account.

**[!UICONTROL Login Details]: [!UICONTROL OAuth Token]:** ([!DNL Microsoft Advertising] [!DNL oAuth]-enabled e tutte le altre reti tranne [!DNL Meta] e [!DNL Yandex]) Il token dell&#39;account per autorizzare gli accessi utilizzando il [[!DNL OAuth] protocollo di autorizzazione](https://oauth.net/2/).

**[!UICONTROL Login Details]: [!UICONTROL Password]:** (tutte le reti di annunci tranne [!DNL Naver]) La password per l&#39;account. Per gli account abilitati per le password in [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] e [!DNL Yandex], questo campo è obbligatorio. Per gli account abilitati per [!DNL oAuth], questo campo è facoltativo. Utilizzarlo quando si desidera crittografare e salvare la password in modo che l&#39;account manager possa aggiornare i token in base alle esigenze.

**[!UICONTROL Login Details]: [!UICONTROL Access Key]:** (solo account [!DNL Yandex]) Chiave di accesso per l&#39;account sviluppatore da utilizzare.

**[!UICONTROL Currency]:** abbreviazione della valuta utilizzata per l&#39;account. Questo campo è modificabile per i nuovi account [!DNL Naver]. Per tutte le altre reti di ricerca, il valore viene compilato automaticamente con la valuta configurata per l’account sulla rete di annunci dopo il salvataggio del record.

**[!UICONTROL Landing Page Suffix]** (solo account [!DNL Google Ads] e [!DNL Microsoft Advertising]; facoltativo) Qualsiasi parametro da aggiungere alla fine degli URL finali per tenere traccia delle informazioni; include tutti i parametri che l&#39;azienda deve monitorare.

Esempio: `param1=value1&param2=value2`

Gli account che utilizzano il tracciamento dei clic di Adobe Advertising devono includere nel suffisso l&#39;identificatore di clic della rete di annunci (`msclkid` per [!DNL Microsoft Advertising]; `gclid` per Google). Gli account con un’integrazione Adobe Analytics devono utilizzare il parametro AMO ID (a partire da `s_kwcid`). Se l’account dispone di un’implementazione AMO ID lato server, il parametro viene aggiunto automaticamente quando un utente fa clic su un annuncio; in caso contrario, devi aggiungerlo manualmente qui. Vedere i [formati di suffisso richiesti per [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) e [formati di suffisso richiesti per [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

>[!NOTE]
>
>* Questo campo non è aggiornato dall&#39;impostazione di tracciamento [!UICONTROL Auto Upload].
>* I suffissi URL finali ai livelli inferiori sovrascrivono il suffisso a livello di account. Per una manutenzione più semplice, utilizza solo il suffisso a livello di account, a meno che non sia necessario un tracciamento diverso per i singoli componenti dell’account. Per configurare un suffisso a livello di gruppo di annunci o inferiore, utilizza l’editor della rete di annunci.

**Fuso orario:** (tutte le reti di annunci tranne [!DNL Baidu] e [!DNL Yahoo! Display Network]) Fuso orario dell&#39;inserzionista. Questo campo è modificabile e facoltativo per i nuovi account [!DNL Naver]. Per tutte le altre reti di ricerca, il valore viene compilato automaticamente con il fuso orario configurato per l&#39;account Search, Social e Commerce dell&#39;inserzionista una volta salvato il record.

**Stato:** lo stato dell&#39;account in Search, Social e Commerce:

* *Abilitato:* Search, Social e Commerce sincronizza i dati della campagna con l&#39;account (se supportato) e invia offerte automatizzate e/o budget delle campagne nei portfolio.
* *Disabilitata:* Ricerca, Social e Commerce interrompe tutte le attività sull&#39;account. I dati raccolti mentre l’account era attivo vengono comunque memorizzati, ma le visualizzazioni e i rapporti di gestione delle campagne non includono i dati per il periodo di tempo in cui l’account viene messo in pausa. Successivamente puoi riattivare l’account per riprendere l’attività con l’account.

**Modello di tracciamento** - ([!DNL Google Ads], [!DNL Microsoft Advertising] e [!DNL Yahoo! Japan Ads] account solo; facoltativo) Il modello di tracciamento predefinito per l&#39;account, che specifica tutti i reindirizzamenti e i parametri di tracciamento del dominio di destinazione e incorpora anche l&#39;URL della pagina finale/di destinazione in un parametro. Esempio: `{lpurl}?source={network}&id=5` o `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` per includere un reindirizzamento.

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

**[!UICONTROL Master Account ID]:** ([!DNL Microsoft Advertising] account solo) ID per un account agenzia/gestione associato all&#39;account.

**[!UICONTROL MCC Account]:** ([!DNL Yandex] account solo; facoltativo) un account agenzia/gestione associato all&#39;account. Per rimuovere un&#39;associazione esistente, selezionare &quot;[!UICONTROL No MCC Account]&quot;.

**[!UICONTROL Application ID]:** (solo account [!DNL Yandex]) Token sviluppatore da utilizzare per l&#39;account. Lo stesso token viene utilizzato per tutti gli account [!DNL Yandex].

**[!UICONTROL Purse Campaign ID]:** ([!DNL Yandex] account con l&#39;impostazione Account condiviso disabilitato solo; facoltativo) ID numerico per la campagna utilizzato per pagare tutte le campagne pubblicitarie nell&#39;account.

**[!UICONTROL Finance Token]:** ([!DNL Yandex] account con l&#39;impostazione Account condiviso disabilitato solo; facoltativo) Token sviluppatore da utilizzare per le chiamate API relative ai dati finanziari, ad esempio per riallocare denaro dal wallet tra le campagne dell&#39;inserzionista in base alle esigenze di ottimizzazione del portfolio.

### Tracciamento account

<!-- **[!UICONTROL Tracking Type]:** -->

{{$include /help/_includes/tracking-type.md}}

<!-- **[!UICONTROL Redirect Type]:** -->

{{$include /help/_includes/redirect-type.md}}

<!-- **[!UICONTROL Auto Upload]:** -->

{{$include /help/_includes/auto-upload.md}}

<!-- **[!UICONTROL Encode Base URL]:** -->

{{$include /help/_includes/encode-base-url.md}}

<!-- **[!UICONTROL Tracking Level]:** -->

{{$include /help/_includes/tracking-level.md}}

**[!UICONTROL Track Product Group]:** (solo per [!UICONTROL EF Redirect]) Non implementato

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

* **Formato S_kwcid:** (Account [!DNL Google Ads] esistenti per gli inserzionisti con un&#39;integrazione Adobe Advertising-Adobe Analytics e per i quali non è già stata eseguita la migrazione dell&#39;AMO ID (s_kwcid))

Questo account utilizza il formato legacy per il codice di tracciamento AMO ID, che consente ad Adobe Advertising di condividere i dati sull’account con Adobe Analytics. Il [formato più recente](/help/integrations/analytics/ids.md#amo-id-formats) include i parametri per l&#39;ID della campagna e l&#39;ID del gruppo di annunci, necessari per creare report accurati a livello di campagna e di gruppo di annunci per le campagne con prestazione massima [!DNL Google Ads], nonché per le bozze e gli esperimenti in Analytics:

`s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

Se l&#39;account deve creare un rapporto a livello di campagna e gruppo di annunci, fare clic sull&#39;icona [!UICONTROL Edit] (matita) e quindi **[!UICONTROL Migrate to new s_kwcid format]** per passare al nuovo formato. Per gli account che non includono questi tipi di campagna, la migrazione al nuovo formato è facoltativa ma consigliata.

Per istruzioni complete, consulta &quot;[Aggiornare il codice di tracciamento AMO ID per un [!DNL Google Ads] account](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md).&quot;

**Nomi suite di rapporti:** (solo per reindirizzamento EF con token; inserzionisti con un&#39;integrazione Adobe Advertising-Adobe Analytics; facoltativo) Una o più suite di rapporti Analytics a cui Search, Social e Commerce invia i dati che raccoglie dalla rete di annunci, incluse le classificazioni delle entità e i dati di clic per l&#39;account. Questa funzione è disponibile solo per le reti di annunci supportate.

Affinché i dati vengano visualizzati nelle suite di rapporti, (a) la funzione AMO ID lato server deve essere configurata per l’account oppure (b) l’impostazione a livello di inserzionista su &quot;[!UICONTROL Enable Advertising reporting in Analytics]&quot; deve essere abilitata. Inoltre, l’account Analytics dell’inserzionista deve essere configurato per ricevere dati da Search, Social e Commerce. Per ulteriori informazioni, contatta il team del tuo account Adobe.

>[!MORELIKETHIS]
>
>* [Informazioni sugli account di rete di annunci](ad-network-account-about.md)
>* [Gestione account centro esercenti](merchant-account-manage.md)
>* [Aggiorna il codice di tracciamento s_kwcid per a [!DNL Google Ads] account](update-amo-id-google.md)
