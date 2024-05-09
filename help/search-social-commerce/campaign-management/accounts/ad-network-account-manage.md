---
title: Gestire gli account di rete degli annunci
description: Scopri come impostare e gestire i dettagli di un account di rete di annunci.
exl-id: 4038d03b-63e2-4953-89df-37f7b5f68652
feature: Search Campaign Management
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '2079'
ht-degree: 0%

---

# Gestire gli account di rete degli annunci

Di seguito sono riportate le istruzioni per la creazione e la modifica dei dettagli dell&#39;account di rete e per l&#39;aggiornamento di [!DNL oAuth] token per un account e disabilitazione degli account.

Per informazioni dettagliate sulle funzionalità disponibili per ciascuna rete di annunci, vedi &quot;[Inventario supportato](/help/search-social-commerce/introduction/supported-inventory.md).&quot;

## Crea dettagli account di rete dell’annuncio {#create-account}

*Solo i ruoli utente Responsabile account agenzia, Responsabile account Adobe e Amministratore*

Per abilitare la sincronizzazione o il tracciamento di un account, devi creare un record account corrispondente contenente le credenziali di accesso e le opzioni di tracciamento dell’account e con lo stato *attivo*.

>[!NOTE]
>
>* Il supporto non è disponibile per i nuovi [!DNL Baidu] account.
>* Per creare un account effettivo sulla rete di annunci, vai al sito web della rete di annunci.

1. Nel menu principale, fai clic su **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Nel sottomenu, fai clic su **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Nella barra degli strumenti sopra la tabella dati, fai clic su ![Crea](/help/search-social-commerce/assets/add.png "Crea").

1. Specifica la [impostazioni account](#account-settings):

   1. Fai clic sul nome della rete di annunci, quindi fai clic su **[!UICONTROL Next]**.

   1. In **[!UICONTROL Account Details]** , immettere i dettagli dell&#39;account.

      Per le reti di annunci che utilizzano il tipo di autorizzazione di accesso &quot;[!UICONTROL oAuth],&quot; consente a Search, Social e Commerce di accedere all’account utilizzando [Protocollo di autorizzazione OAuth](https://oauth.net/2/):

      1. Inserisci il **[!UICONTROL Login]** per l&#39;account, immettere facoltativamente la password e quindi fare clic su **[!UICONTROL Authenticate]**.

         La best practice prevede l’utilizzo dell’accesso API all’account. Inserisci la password quando desideri crittografarla e salvarla, in modo che il team dell’account Adobe possa aggiornare i token in base alle esigenze.

      1. (Se non hai effettuato l’accesso all’account dell’inserzionista) Accedi all’account dell’inserzionista. La best practice prevede l’utilizzo delle credenziali per l’accesso API all’account.

      1. Nella schermata di richiesta di autorizzazione/accesso, fai clic sul pulsante per confermare l’autorizzazione.

      1. Copia la stringa di autenticazione nella finestra pop-up che si apre e incolla la stringa nella **[!UICONTROL oAuth Token]** campo.

      1. Specificare i dettagli dell&#39;account rimanenti.

   1. Clic **[!UICONTROL Set Account Tracking]** e immetti le impostazioni di tracciamento.

1. Clic **[!UICONTROL Post]**.

   I dati recenti relativi ai costi e ai clic per tutte le campagne nell’account sono disponibili in Search, Social e Commerce in circa 24 ore. Per impostazione predefinita, i dati sono disponibili per gli ultimi 5-10 giorni, a seconda della rete di annunci. Quando necessario, tuttavia, il team di avvio del progetto può recuperare i dati per un massimo di 60 giorni.

## Modifica i dettagli dell’account di rete dell’annuncio {#edit-account}

*Solo i ruoli utente Responsabile account agenzia, Responsabile account Adobe e Amministratore*

Se le credenziali dell’account cambiano, vuoi modificare i parametri di tracciamento predefiniti in un account, oppure vuoi abilitare o disabilitare l’attività su un account, quindi modificare i dettagli dell’account.

>[!NOTE]
>
>Per modificare un account effettivo sulla rete di annunci, vai al sito web della rete di annunci.

1. Nel menu principale, fai clic su **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Nel sottomenu, fai clic su **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Posizionare il cursore sul nome dell&#39;account e fare clic su ![Altro](/help/search-social-commerce/assets/more-filters.png "Altro")e quindi selezionare **[!UICONTROL Edit]**.

1. Modifica il [impostazioni account](#account-settings):

   1. (Facoltativo) Modifica i dettagli dell’account.

   1. (Facoltativo) Fai clic su **[!UICONTROL Set Account Tracking]** e modificare le impostazioni di tracciamento.

1. Clic **[!UICONTROL Post]**.

   >[!NOTE]
   >
   >Search, Social e Commerce devono sincronizzare i nuovi dati dell&#39;account con quelli della rete pubblicitaria. Questo accade automaticamente una volta al giorno, o più spesso quando Search, Social &amp; Commerce rileva le modifiche sulla rete di annunci.

## Aggiorna i token di accesso OAuth per gli account di ricerca {#refresh-oauth-tokens}

*Solo i ruoli utente Responsabile account agenzia, Responsabile account Adobe e Amministratore*

Se Search, Social e Commerce accedono all&#39;account utilizzando [Protocollo di autorizzazione OAuth](https://oauth.net/2/) e le credenziali dell’account cambiano, oppure se è necessario un accesso aggiuntivo per supportare nuove funzioni in Search, Social e Commerce, devi ottenere un nuovo token di accesso per l’account.

Se nuove funzionalità richiedono un nuovo token, il team del tuo account Adobe ti informerà.

1. (Se hai effettuato l’accesso a un altro account per la stessa rete di annunci nella stessa applicazione del browser) Esci da qualsiasi account diverso da quello dell’inserzionista.

1. Nel menu principale, fai clic su **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Nel sottomenu, fai clic su **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Posizionare il cursore sul nome dell&#39;account e fare clic su ![Altro](/help/search-social-commerce/assets/more-filters.png "Altro")e quindi selezionare **[!UICONTROL Edit]**.

1. Ottieni un nuovo token di accesso:

   1. Clic **[!UICONTROL Get oAuth Token]**.

   1. (Se non hai effettuato l’accesso all’account dell’inserzionista) Accedi all’account dell’inserzionista. La best practice prevede l’utilizzo delle credenziali per l’accesso API all’account.

   1. Nella schermata di richiesta di autorizzazione/accesso, fai clic sul pulsante per confermare l’autorizzazione.

   1. Copia la stringa di autenticazione nella finestra pop-up che si apre e incolla la stringa nella **[!UICONTROL oAuth Token]** campo.

1. Clic **[!UICONTROL Post]**.

## Attivare o disattivare gli account di rete degli annunci {#enable-disable-account}

*Solo i ruoli utente Responsabile account agenzia, Responsabile account Adobe e Amministratore*

Quando si abilita un account di ad network, Search, Social e Commerce sincronizzano i dati della campagna con l&#39;account (se supportato) e inviano offerte automatizzate e/o budget delle campagne nei portfolio.Quando si disabilita un account di ad network, Search, Social e Commerce interrompe tutte le attività sull&#39;account. I dati raccolti mentre l’account era attivo vengono comunque memorizzati, ma le visualizzazioni e i rapporti di gestione delle campagne non includono i dati per il periodo di tempo in cui l’account è disabilitato. In seguito, potrai riabilitare l’account per riprendere l’attività con l’account.

1. Nel menu principale, fai clic su **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Nel sottomenu, fai clic su **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Effettuare una delle seguenti operazioni:

   * Per modificare lo stato di un singolo account, posizionare il cursore sul nome dell&#39;account e fare clic su ![Altro](/help/search-social-commerce/assets/more-filters.png "Altro")e quindi selezionare **[!UICONTROL Edit]**. Modificare il **[!UICONTROL Status]** a *Abilitato* o *Disabilitato* e quindi fare clic su **[!UICONTROL Post]**.

   * Per modificare lo stato di uno o più account, effettuare le seguenti operazioni:

      1. Seleziona la casella di controllo accanto a ciascun account.

         Per suggerimenti sulla selezione di più righe, vedere &quot;[Seleziona più righe](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      1. Nella barra degli strumenti sopra la tabella dati, fai clic su ![Icona Attiva](/help/search-social-commerce/assets/activate.png "Icona Attiva") per abilitare l’account o ![Icona Disattiva](/help/search-social-commerce/assets/disable.png "Icona Disattiva") per disabilitare l&#39;account.

## Impostazioni dell’account di rete dell’annuncio {#account-settings}

>[!NOTE]
>
>Solo responsabile del conto di agenzia, [!DNL Adobe] gli utenti di account manager e amministratore possono configurare le impostazioni dell’account.

### Dettagli account

**[!UICONTROL SE Account ID]:** (Tutti gli account tranne [!DNL Naver] e [!DNL Yandex] account; modificabile solo per i nuovi account) L’ID account assegnato dalla rete di annunci.

>[!NOTE]
>
>Gli account del gestore della rete di annunci non sono supportati qui. Per identificare un account manager per [!DNL Microsoft Advertising] o [!DNL Yandex], utilizzare rispettivamente il campo ID account principale o Account MCC. A [impostare le credenziali per un [!DNL Google Ads] account manager](/help/search-social-commerce/admin/manager-accounts.md), vai a [!UICONTROL Admin] \> [!UICONTROL Manager Accounts].

**[!UICONTROL Account Name]:** Il nome da visualizzare per l’account in Search, Social &amp; Commerce.

>[!NOTE]
>
>Se hai un’integrazione Search, Social e Commerce-Adobe Analytics e modifichi il nome dell’account di ricerca, informa il team dell’account Adobe in modo che possa aggiornare la mappatura.

**[!UICONTROL Login Details]: \[Tipo di accesso\]** - ([!DNL Microsoft Advertising]/[!DNL Microsoft Merchant Center] solo) Se autorizzare gli accessi all’account utilizzando:

* *[!UICONTROL oAuth]* (impostazione predefinita): per utilizzare [[!DNL OAuth] protocollo di autorizzazione](https://oauth.net/2/).

* *[!UICONTROL Password]:* Per utilizzare la password del client.

Per [!DNL Microsoft Advertising] account, solo [!DNL oAuth]-è possibile utilizzare gli accessi autorizzati.

**[!UICONTROL Login Details]: [!UICONTROL Login]:** (Tutte le reti pubblicitarie tranne [!DNL Naver]) Il nome o l’ID di accesso per abilitare l’accesso API all’account.

**[!UICONTROL Login Details]: [!UICONTROL OAuth Token]:** ([!DNL Microsoft Advertising] [!DNL oAuth]-abilitato e tutte le altre reti tranne [!DNL Meta] e [!DNL Yandex]) Token dell&#39;account per autorizzare gli accessi tramite [[!DNL OAuth] protocollo di autorizzazione](https://oauth.net/2/).

**[!UICONTROL Login Details]: [!UICONTROL Password]:** (Tutte le reti pubblicitarie tranne [!DNL Naver]) La password dell&#39;account. Per gli account abilitati per le password su [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads], e [!DNL Yandex], questo campo è obbligatorio. Per [!DNL oAuth]-enabled account, questo campo è facoltativo; utilizzalo quando desideri crittografare e salvare la password in modo che l’account manager possa aggiornare i token in base alle esigenze.

**[!UICONTROL Login Details]: [!UICONTROL Access Key]:** ([!DNL Yandex] solo account) Chiave di accesso per l&#39;account sviluppatore da utilizzare.

**[!UICONTROL Currency]:** Abbreviazione della valuta utilizzata per il conto. Questo campo è modificabile per il nuovo [!DNL Naver] account. Per tutte le altre reti di ricerca, il valore viene compilato automaticamente con la valuta configurata per l’account sulla rete di annunci dopo il salvataggio del record.

**[!UICONTROL Landing Page Suffix]** ([!DNL Google Ads] e [!DNL Microsoft Advertising] solo account; facoltativo) qualsiasi parametro da aggiungere alla fine degli URL finali per tenere traccia delle informazioni; include tutti i parametri che l’azienda deve monitorare.

Esempio: `param1=value1&param2=value2`

Gli account che utilizzano il tracciamento dei clic di Adobe Advertising devono includere l’identificatore di clic della rete di annunci (`msclkid` per [!DNL Microsoft Advertising]; `gclid` per Google) nel suffisso. Gli account con un’integrazione Adobe Analytics devono utilizzare il parametro AMO ID (che inizia con `s_kwcid`). Se l’account dispone di un’implementazione AMO ID lato server, il parametro viene aggiunto automaticamente quando un utente fa clic su un annuncio; in caso contrario, devi aggiungerlo manualmente qui. Consulta la [formati di suffisso richiesti per [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) e [formati di suffisso richiesti per [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

>[!NOTE]
>
>* Questo campo non viene aggiornato da [!UICONTROL Auto Upload] impostazione di tracciamento.
>* I suffissi URL finali ai livelli inferiori sovrascrivono il suffisso a livello di account. Per una manutenzione più semplice, utilizza solo il suffisso a livello di account, a meno che non sia necessario un tracciamento diverso per i singoli componenti dell’account. Per configurare un suffisso a livello di gruppo di annunci o inferiore, utilizza l’editor della rete di annunci.

**Fuso orario:** (Tutte le reti di annunci tranne [!DNL Baidu] e [!DNL Yahoo! Display Network]) Il fuso orario dell&#39;inserzionista. Questo campo è modificabile e facoltativo per i nuovi [!DNL Naver] account. Per tutte le altre reti di ricerca, il valore viene compilato automaticamente con il fuso orario configurato per l&#39;account Search, Social e Commerce dell&#39;inserzionista una volta salvato il record.

**Stato:** Lo stato dell’account in Search, Social e Commerce:

* *Attivato:* Search, Social e Commerce sincronizzano i dati della campagna con l&#39;account (se supportato) e inviano offerte automatizzate e/o budget delle campagne nei portfolio.
* *Disattivato:* Search, Social e Commerce interrompe tutte le attività sull&#39;account. I dati raccolti mentre l’account era attivo vengono comunque memorizzati, ma le visualizzazioni e i rapporti di gestione delle campagne non includono i dati per il periodo di tempo in cui l’account viene messo in pausa. Successivamente puoi riattivare l’account per riprendere l’attività con l’account.

**Modello di tracciamento** - ([!DNL Google Ads], [!DNL Microsoft Advertising], e [!DNL Yahoo! Japan Ads] solo account; facoltativo) Il modello di tracciamento predefinito per l’account, che specifica tutti i reindirizzamenti e i parametri di tracciamento del dominio di destinazione finale e incorpora anche l’URL della pagina di destinazione finale in un parametro. Esempio: `{lpurl}?source={network}&id=5` o `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` per includere un reindirizzamento.

* Per incorporare l’URL finale:

   * ([!DNL Google Ads] e [!DNL Microsoft Advertising] solo ) Per un elenco di parametri che indicano gli URL finali nei modelli di tracciamento, vedi ([!DNL Microsoft Advertising] solo ) [[!DNL Microsoft Advertising] documentazione](https://help.ads.microsoft.com/#apex/3/en/56799) o ([!DNL Google Ads] solo) i parametri &quot;Solo modello di tracciamento&quot; nella sezione su &quot;Disponibile [!DNL ValueTrack] Parameters&quot; nella sezione [[!DNL Google Ads] documentazione](https://support.google.com/google-ads/answer/6305348).

   * ([!DNL Yahoo! Japan Ads] solo) Usa il parametro `!{lpurl}` per indicare l’URL della pagina di destinazione.

* Facoltativamente, puoi includere i parametri URL ed eventuali parametri personalizzati definiti per la campagna, separati da e commerciali (&amp;), ad esempio `{lpurl}?matchtype={matchtype}&device={device}`.

* Facoltativamente, puoi aggiungere reindirizzamenti e tracciamento di terze parti.

* Quando le impostazioni della campagna includono &quot;[!UICONTROL EF Redirect]&quot; e &quot;[!UICONTROL Auto Upload],&quot; Search, Social e Commerce applicano automaticamente i prefissi al proprio codice di reindirizzamento e di tracciamento quando si salva il record.

>[!NOTE]
>
>* Per [!DNL Google Ads], evita di utilizzare macro che non vengono sostituite dai clic provenienti da origini che abilitano il tracciamento parallelo. Se l’inserzionista deve utilizzare delle macro, l’Account Team Adobe deve collaborare con l’Assistenza clienti o con il team di implementazione per aggiungerle.
>* Il modello di tracciamento al livello più granulare sostituisce i valori a tutti i livelli superiori. Ad esempio, se entrambe le impostazioni account e parola chiave includono un valore, tale valore viene applicato.
>* Se aggiorni un modello di tracciamento a livello di annuncio, sitelink o parola chiave, gli annunci pertinenti vengono nuovamente inviati per la revisione. Puoi aggiornare i modelli di tracciamento a livello di account, campagna o gruppo di annunci senza inviare nuovamente gli annunci per l’approvazione.

**[!UICONTROL Master Account ID]:** ([!DNL Microsoft Advertising] solo account) ID di un account agenzia/gestione associato all’account.

**[!UICONTROL MCC Account]:** ([!DNL Yandex] solo account; facoltativo) Un account di agenzia/gestione associato all’account. Per rimuovere un’associazione esistente, seleziona &quot;[!UICONTROL No MCC Account].&quot;

**[!UICONTROL Application ID]:** ([!DNL Yandex] solo account) Token sviluppatore da utilizzare per l’account. Lo stesso token viene utilizzato per tutti [!DNL Yandex] account.

**[!UICONTROL Purse Campaign ID]:** ([!DNL Yandex] account con l&#39;impostazione Account condiviso disabilitata; facoltativo) l&#39;ID numerico per la campagna utilizzato per pagare tutte le campagne pubblicitarie nell&#39;account.

**[!UICONTROL Finance Token]:** ([!DNL Yandex] account con l’impostazione Account condiviso disabilitata; facoltativo) Il token sviluppatore da utilizzare per le chiamate API relative ai finanziamenti, ad esempio per riallocare denaro dal wallet tra le campagne dell’inserzionista in base alle necessità per l’ottimizzazione del portfolio.

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

**[!UICONTROL Track Product Group]:** (Per [!UICONTROL EF Redirect] solo) Non implementato

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

* **Formato S_kwcid** - (Esistente [!DNL Google Ads] account per gli inserzionisti con un’integrazione Adobi Advertising-Adobe Analytics e per i quali non è già stata eseguita la migrazione dell’AMO ID (s_kwcid)

Questo account utilizza il formato legacy per il codice di tracciamento AMO ID, che consente ad Adobi Advertising di condividere i dati sull’account con Adobe Analytics. Il [formato più recente](/help/integrations/analytics/ids.md#amo-id-formats) include i parametri per l’ID della campagna e l’ID del gruppo di annunci, necessari per creare rapporti accurati a livello di campagna e di gruppo di annunci per [!DNL Google Ads] campagne di prestazioni massime, bozze ed esperimenti in Analytics:

`s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

Se questo account deve generare rapporti a livello di campagna e di gruppo di annunci, fai clic su [!UICONTROL Edit] (matita) e quindi **[!UICONTROL Migrate to new s_kwcid format]** al nuovo formato. Per gli account che non includono questi tipi di campagna, la migrazione al nuovo formato è facoltativa ma consigliata.

Per istruzioni complete, consulta &quot;[Aggiornamento del codice di tracciamento AMO ID per un [!DNL Google Ads] account](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md).&quot;

**Nomi suite di rapporti** - (Solo per reindirizzamento EF con token; inserzionisti con integrazione Adobi Advertising-Adobe Analytics; facoltativo) Una o più suite di rapporti Analytics a cui Search, Social e Commerce invia i dati che raccoglie dalla rete di annunci, incluse le classificazioni delle entità e i dati di clic per l’account. Questa funzione è disponibile solo per le reti di annunci supportate.

Affinché i dati vengano visualizzati nelle suite di rapporti, a) la funzione AMO ID lato server deve essere configurata per l’account o b) l’impostazione a livello di inserzionista su &quot;[!UICONTROL Enable tracking for SAINT feeds]&quot; deve essere abilitato. Inoltre, l’account Analytics dell’inserzionista deve essere configurato per ricevere dati da Search, Social e Commerce. Per ulteriori informazioni, contatta il tuo Adobe Account Manager.

>[!MORELIKETHIS]
>
>* [Informazioni sugli account di rete degli annunci](ad-network-account-about.md)
>* [Gestisci account centro esercenti](merchant-account-manage.md)
>* [Aggiorna il codice di tracciamento s_kwcid per un [!DNL Google Ads] account](update-amo-id-google.md)
