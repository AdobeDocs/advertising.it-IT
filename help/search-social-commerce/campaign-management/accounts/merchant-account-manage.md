---
title: Gestisci account esercente
description: Scopri come impostare e gestire i dettagli di un account per un centro commerciale.
exl-id: 7d940e45-ea49-470b-98d0-0196593228cb
feature: Search Campaign Management
source-git-commit: cb65108fcc60c11b901e3b43c292ad5a94192b9f
workflow-type: tm+mt
source-wordcount: '789'
ht-degree: 0%

---

# Gestisci account esercente

*Solo i ruoli di account manager agenzia, manager account Adobe e amministratore*

Search, Social e Commerce possono scaricare e visualizzare i dati dei prodotti ogni giorno per gli account Google Merchant Center o Microsoft Merchant Center degli inserzionisti. Inoltre, Search, Social e Commerce possono automatizzare la creazione di annunci in base al contenuto dell&#39;account esercente.Per lavorare direttamente con i dati di prodotto in Search, Social e Commerce, è necessario creare un record account corrispondente contenente le credenziali di accesso all&#39;account e con l&#39;accesso *abilitato*.

>[!NOTE]
>
>Non puoi rimuovere un record di account esercente. È possibile disabilitare l&#39;accesso a un account cambiando il tipo di account in *disabilitato*.

## Crea dettagli account esercente {#create-merchant-account}

*Solo i ruoli di account manager agenzia, manager account Adobe e amministratore*

Per visualizzare i dati di prodotto e generare modelli di tracciamento per un account esercente e per creare annunci basati sui dati, è necessario creare un record account corrispondente contenente le credenziali di accesso all&#39;account e con accesso all&#39;account *abilitato*.

>[!NOTE]
>
>Per creare un account effettivo sulla rete di esercenti, vai al sito web della rete.

1. Nel menu principale, fare clic su **[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Products]**, che consente di aprire la scheda [!UICONTROL Accounts].

1. Nella barra degli strumenti sopra la tabella dati, fare clic su **[!UICONTROL Create Account]**.

1. Specifica le [impostazioni account esercente](#merchant-account-settings):

   1. Nel menu [!UICONTROL Product Source], selezionare il centro commerciale.

   <!--

   1. ([!DNL Meta Ads] accounts only) Log in to the [!DNL Meta Ads] account.

   And are there additional steps just for Meta? If so, create a separate procedure for it.
   
   -->

   1. (Obbligatorio per gli account [!DNL Google Ads]; facoltativo per gli account [!DNL Microsoft Advertising]) Consenti a Search, Social e Commerce di accedere all&#39;account utilizzando il [[!DNL OAuth] protocollo di autorizzazione](https://oauth.net/2/):

      1. ([!DNL Microsoft Advertising] solo account) Seleziona **[!UICONTROL oAuth]**.

      1. Fare clic su **[!UICONTROL Enable Connection]**.

      1. (Se non hai effettuato l&#39;accesso all&#39;account dell&#39;inserzionista) Accedi all&#39;account dell&#39;inserzionista. La best practice prevede l’utilizzo delle credenziali per l’accesso API ai contenuti all’account del centro commerciale.

      1. Nella schermata di richiesta di accesso/autorizzazione, fai clic sul pulsante per confermare l’autorizzazione.

      1. Copiare la stringa di autenticazione nella finestra popup visualizzata e incollarla nel campo **[!UICONTROL oAuth Token]**.

      1. Specificare le altre impostazioni account.

1. Fare clic su **[!UICONTROL Save]**.

   I dati degli attributi per tutti i prodotti nell’account sono disponibili in Search, Social e Commerce dopo il successivo processo di sincronizzazione giornaliero (circa alle 06:00 nel fuso orario locale dell’utente). Puoi quindi utilizzare i dati del prodotto per automatizzare la creazione di annunci utilizzando i feed di inventario.

## Modifica dettagli account esercente {#edit-merchant-account}

*Solo i ruoli di account manager agenzia, manager account Adobe e amministratore*

Se le credenziali dell’account cambiano o desideri interrompere il recupero e l’utilizzo dei dati per un account esercente, modifica i dettagli dell’account.

>[!NOTE]
>
>Per modificare un account effettivo sulla rete di esercenti, visitare il sito Web della rete.

1. Nel menu principale, fare clic su **[!UICONTROL Search]\> [!UICONTROL Campaigns] \>[!UICONTROL Products]**, che consente di aprire la scheda [!UICONTROL Accounts].

1. Accanto al nome dell&#39;account, fare clic su ![Visualizza/modifica impostazioni](/help/search-social-commerce/assets/settings.png "Visualizza/modifica impostazioni").

1. Modifica le [impostazioni account esercente](#merchant-account-settings).

1. Fare clic su **[!UICONTROL Save]**.

>[!NOTE]
>
>Search, Social e Commerce devono sincronizzare i nuovi dati dell&#39;account con quelli presenti nella rete di esercenti. Questo accade automaticamente una volta al giorno alle 06:00 circa nel fuso orario locale dell’utente.

## Disabilita l’accesso a un account esercente {#disable-merchant-account}

*Solo i ruoli di account manager agenzia, manager account Adobe e amministratore*

Quando disattivi un account esercente, Search, Social e Commerce non vi accedono e di conseguenza non recupera i dati di prodotto aggiornati. I dati raccolti mentre l’account era abilitato vengono comunque memorizzati e gli annunci esistenti creati utilizzando i dati del prodotto non vengono aggiornati, messi in pausa o eliminati in base al modello di feed e alle impostazioni dei dati di feed.

1. Nel menu principale, fare clic su **[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Products]** , che apre alla scheda [!UICONTROL Accounts].

1. Accanto al nome dell&#39;account, fare clic su ![Visualizza/modifica impostazioni](/help/search-social-commerce/assets/settings.png "Visualizza/modifica impostazioni").

1. Cambia [!UICONTROL EF Account Type] in **[!UICONTROL Disabled]**.

1. Fare clic su **[!UICONTROL Save]**.

## Impostazioni account esercente {#merchant-account-settings}

>[!NOTE]
>
>Solo il manager dell&#39;account dell&#39;agenzia, il manager dell&#39;account [!DNL Adobe] e i ruoli utente amministratore possono configurare le impostazioni dell&#39;account esercente.

**[!UICONTROL Product Source]:** Rete di esercenti. Non puoi modificare il valore di un account esistente.

**[!UICONTROL OAuth Token]:** ([!DNL Google Merchant Center] account) Il token dell&#39;account per autorizzare gli accessi tramite il [[!DNL OAuth] protocollo di autorizzazione](https://oauth.net/2/).

**[!UICONTROL Auth Type]:** ([!DNL Microsoft Advertising]/[!DNL Microsoft Merchant Center] solo) Se autorizzare gli accessi all&#39;account utilizzando:

* *[!UICONTROL Client login]:* Per utilizzare l&#39;accesso del client.

* *[!UICONTROL oAuth]* (impostazione predefinita): per utilizzare il [[!DNL OAuth] protocollo di autorizzazione](https://oauth.net/2/).

**[!UICONTROL Access Key]:** ([!DNL Microsoft Merchant Center] solo) Chiave di accesso per l&#39;account sviluppatore da utilizzare.

**[!UICONTROL Account Name]:** nome visualizzato per l&#39;account in Search, Social e Commerce.

**[!UICONTROL Login]:** Nome o ID di accesso per l&#39;account.

**[!UICONTROL Password]:** La password per l&#39;account.

**[!UICONTROL Confirm Password]:** La password per l&#39;account.

**[!UICONTROL EF Account Type]:** se Search, Social e Commerce accedono all&#39;account:

* *[!UICONTROL Enabled]* (impostazione predefinita): Search, Social e Commerce possono accedere all&#39;account per recuperare i dati del prodotto.

* *[!UICONTROL Disabled]:* Search, Social e Commerce non accedono all&#39;account e pertanto non recuperano i dati di prodotto aggiornati. I dati raccolti mentre l’account era abilitato vengono comunque memorizzati e gli annunci esistenti creati utilizzando i dati del prodotto non vengono aggiornati, messi in pausa o eliminati in base al modello di feed e alle impostazioni dei dati di feed.

**[!UICONTROL Account ID]:** ID dell&#39;account esercente. Se disponi di un solo account con le informazioni di accesso specificate, questo valore è facoltativo.

**[!UICONTROL Time Zone]:** Fuso orario dell&#39;inserzionista. Utilizza lo stesso fuso orario configurato per le informazioni dell’account Search, Social e Commerce dell’inserzionista (impostato al momento della creazione dell’account). Non puoi modificare il valore di un account esistente.

>[!MORELIKETHIS]
>
>* [Informazioni sugli account di rete di annunci](ad-network-account-about.md)
>* [Gestione account di rete pubblicitaria](ad-network-account-manage.md)
