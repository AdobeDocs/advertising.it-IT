---
title: Gestisci [!DNL ChatGPT Ads] account di annunci conversazionali
description: Scopri come creare e gestire gli account per gli annunci tramite chat card di [!DNL ChatGPT Ads], una funzione beta che inserisce gli annunci all'interno delle conversazioni dell'assistente AI.
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: cb25ab04e8fef5d00935e5325a897b1de97e2674
workflow-type: tm+mt
source-wordcount: '898'
ht-degree: 0%
---
# Gestisci [!DNL ChatGPT Ads] account di annunci conversazionali

*funzionalità Beta*

Tramite l&#39;integrazione di Adobe DSP con [!DNL OpenAI Ads], puoi eseguire [!DNL ChatGPT Ads] annunci tramite chat card, visualizzati all&#39;interno di [!DNL ChatGPT] conversazioni. Per questa funzione, DSP crea un account di annuncio conversazionale e acquista contenuti multimediali per conto della tua organizzazione. Non potrai accedere all’account dell’annuncio da ads.openai.com. Utilizzare questa funzionalità per testare i supporti AI senza stabilire una relazione diretta con [!DNL ChatGPT Ads].

Gli account degli annunci conversazionali di [!DNL ChatGPT Ads], inclusi campagne, gruppi di annunci e annunci, verranno gestiti separatamente dalle normali campagne DSP, strutturate in modo diverso. [visualizzerai inoltre i dati sulle prestazioni per  [!DNL ChatGPT Ads] campagne, gruppi di annunci e annunci](campaign-manage.md#campaign-views-about) separatamente dalle campagne DSP.

## Idoneità

Di seguito è riportata l&#39;idoneità per questa funzione:

* **Clienti [!DNL Search, Social, & Commerce] esistenti:** Se l&#39;inserzionista utilizza già [!DNL Search, Social, & Commerce], [crea e gestisci le campagne  [!DNL ChatGPT Ads]  in Search, Social e Commerce](/help/search-social-commerce/new-ui/manage/campaigns/campaign-manage.md) anziché in DSP.

* **Settori con restrizioni:** Gli inserzionisti che rientrano in categorie con restrizioni (ad esempio, settore finanziario o sanitario) non possono creare account o campagne pubblicitarie di tipo conversational.

Se l&#39;inserzionista selezionato non è idoneo, il motivo è indicato nelle schede [!UICONTROL Accounts] e [!UICONTROL Campaigns]. Puoi comunque passare a un altro inserzionista utilizzando il selettore degli inserzionisti.

Per utilizzare questa funzione, contatta il team del tuo account Adobe per iniziare il processo di onboarding.

## Fatturazione

L&#39;utilizzo di [!DNL ChatGPT Ads] alla fine del mese viene fatturato con le altre fatture, utilizzando la valuta di fatturazione e il fuso orario di fatturazione per l&#39;account DSP (indipendentemente dalla [valuta e dal fuso orario utilizzati per l&#39;account [!DNL ChatGPT Ads] account](#account-settings)). Per domande sulla fatturazione, contatta il team del tuo account Adobe.

## Visualizzazione [!UICONTROL Conversational Ads Beta] > [!UICONTROL Accounts] {#accounts-view}

Nella scheda [!UICONTROL Conversational Ads Beta] > [!UICONTROL Accounts] sono elencati gli account [!DNL OpenAI] per l&#39;inserzionista selezionato. Le informazioni relative a ciascun account includono:

**[!UICONTROL Status]:** Se l&#39;account sta attualmente distribuendo annunci: *Attivo* o *In pausa*. Non puoi modificare lo stato di un account; se desideri sospendere o riattivare un account, contatta il team del tuo account di Adobe.

**[!UICONTROL Review status]:** Lo stato di revisione [!DNL OpenAI]: *In revisione*, *Approvato* o *Disapprovato*. Posizionare il cursore sullo stato del motivo, se disponibile.

**[!UICONTROL Active campaigns]:** Il numero di campagne attualmente attive nell&#39;account.

**[!UICONTROL Cost]:** La spesa totale dell&#39;account.

### Azioni disponibili

* [Visualizza limiti account](#account-limits)

<!-- * [Refresh information about your accounts](#refresh) -- Add topic below. -->

* [Creare un account](#account-create)

* [Modificare un account](#account-edit)

* [Aggiorna l&#39;elenco degli account](#account-refresh)

* [Torna al menu principale di DSP](#return-to-menu)

## Gestisci account

### Visualizza limiti account {#account-limits}

Un limite di account limita la spesa totale di un account in un intervallo di date specifico. Puoi visualizzare i limiti di un account, ma solo il team dell’account Adobe può crearli, modificarli o rimuoverli.

1. Nel menu principale, fare clic su **[!UICONTROL Conversational Ads Beta]**.

1. Nella visualizzazione **[!UICONTROL Accounts]**, posizionare il cursore sulla riga dell&#39;account e fare clic su **[!UICONTROL ...]>[!UICONTROL View account limit]**.

Nella pagina [!UICONTROL Account limits] sono elencati tutti i limiti per l&#39;account:

**[!UICONTROL Name]:** Il nome del limite.

**[!UICONTROL Amount]:** Il limite di spesa totale per il periodo limite.

**[!UICONTROL Period]:** L&#39;intervallo di date a cui si applica il limite.

**[!UICONTROL Status]:** *Attivo*, *In arrivo* o *Completato*.

**[!UICONTROL Spent]:** L&#39;importo speso finora entro il periodo limite.

>[!NOTE]
>
>Non puoi modificare o rimuovere i limiti completati e i periodi limite per lo stesso account non possono sovrapporsi.

### Crea un account annuncio conversazionale [!DNL ChatGPT Ads] {#account-create}

Per creare più di due account [!DNL ChatGPT Ads] per un inserzionista, contatta il team del tuo account Adobe.

1. Nel menu principale, fare clic su **[!UICONTROL Conversational Ads Beta]**.

1. Effettuare una delle seguenti operazioni:

   * (Solo il tuo primo account) Nella schermata di benvenuto, fai clic su **[!UICONTROL Create an Account]**.

   * Nella visualizzazione **[!UICONTROL Accounts]**, selezionare un inserzionista e quindi fare clic su **[!UICONTROL Create Account]**.

1. Specificare le [impostazioni account](#account-settings).

1. Selezionare la casella di controllo **[!UICONTROL I agree to the Terms and Conditions]**.

1. Fare clic su **[!UICONTROL Create account]**.

I nuovi account vengono creati in stato di pausa mentre [!DNL OpenAI] li esamina. DSP attiva l’account una volta approvato.

### Modifica un account annuncio conversazionale [!DNL ChatGPT Ads] {#account-edit}

Puoi modificare la ragione sociale e il sito web legali di un account dopo averlo creato.

1. Nel menu principale, fare clic su **[!UICONTROL Conversational Ads Beta]**.

1. Nella visualizzazione **[!UICONTROL Accounts]**, posizionare il cursore sulla riga dell&#39;account e fare clic su **[!UICONTROL ...]>[!UICONTROL Edit account]**.

1. Modificare **[!UICONTROL Legal Business Name]** e/o **[!UICONTROL Advertiser Website]**. Per ulteriori informazioni sui campi, vedere &quot;[Impostazioni account](#account-settings).&quot;

1. Fare clic su **[!UICONTROL Save changes]**.

>[!IMPORTANT]
>
>Il salvataggio delle modifiche riavvia la revisione di [!DNL OpenAI] per l&#39;account. L’account non distribuirà più annunci fino a quando non verrà nuovamente approvato.

### Aggiorna l&#39;elenco degli account {#account-refresh}

Visualizzare di nuovo l&#39;elenco degli account quando altri utenti possono aver apportato modifiche o aggiunte.

1. Nel menu principale, fare clic su **[!UICONTROL Conversational Ads Beta]**.

1. Nella visualizzazione **[!UICONTROL Accounts]**, fare clic su **[!UICONTROL Refresh]** sopra l&#39;elenco degli account.

### Torna al menu principale di DSP {#return-to-menu}

* Sopra il menu principale, fare clic su **[!UICONTROL Back to DSP]**.

### [!DNL ChatGPT Ads] impostazioni account annuncio conversazionale {#account-settings}

**[!UICONTROL Legal Business Name]:** La ragione sociale registrata dell&#39;organizzazione.

**[!UICONTROL Advertiser Website]:** URL del sito Web dell&#39;inserzionista, a partire da `http://` o `https://`.

**[!UICONTROL Country]:** Il paese in cui l&#39;organizzazione è legalmente registrata (non il paese in cui verranno eseguiti gli annunci). Deve essere lo stesso paese utilizzato per il contratto DSP dell&#39;organizzazione. Non puoi modificare questo valore dopo aver salvato l’account.

**[!UICONTROL Currency]:** (sola lettura) la valuta impostata dal team dell&#39;account Adobe per l&#39;account [!DNL ChatGPT Ads]. Potrebbe essere diversa dalla valuta per il tuo account DSP, che è visibile altrove in DSP. **Nota:** Indipendentemente da questo valore, tutte le fatture di utilizzo saranno nella *valuta di fatturazione* utilizzata per l&#39;account DSP.

**[!UICONTROL Timezone]:** (sola lettura) Il fuso orario configurato dal team dell&#39;account Adobe per l&#39;account [!DNL ChatGPT Ads]. Può essere diverso dal fuso orario utilizzato per l’account DSP, visibile altrove in DSP. **Nota:** indipendentemente da questo valore, tutte le fatture di utilizzo rappresenteranno il *fuso orario di fatturazione* utilizzato per l&#39;account DSP.

**[!UICONTROL Favicon]:** File di immagine da utilizzare come favicon del sito Web per l&#39;account.<!-- How is this used within this context? --> Il browser visualizza il favicon in varie posizioni, ad esempio la barra degli indirizzi, la scheda o i segnalibri. Il file deve essere in formato JPG, PNG o WEBP e un minimo di 256x256 pixel.

Per caricare un&#39;icona, fare clic su **[!UICONTROL Upload favicon]**, quindi individuare e selezionare un file nel dispositivo o nella rete.

**[!UICONTROL I agree to the Terms and Conditions]:** Casella di controllo per indicare che si accettano tutte le condizioni legali. Selezionare la casella di controllo per creare un account o aggiornare le impostazioni dell&#39;account.

>[!MORELIKETHIS]
>
>* [Gestione campagne pubblicitarie conversazionali](campaign-manage.md)
