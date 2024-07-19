---
title: Gestire i tipi di pubblico in base ai clienti utilizzando gli elenchi di dati dei clienti
description: Scopri come creare e modificare  [!DNL Google Ads] e [!DNL Microsoft Advertising] i tipi di pubblico in base ai clienti dagli elenchi di dati dei clienti.
exl-id: 594a7ee0-4ac9-4970-b53e-d4624fd7b70c
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '842'
ht-degree: 0%

---

# Gestisci [!DNL Google Ads] e [!DNL Microsoft Advertising] tipi di pubblico in base ai clienti utilizzando gli elenchi di dati cliente

Puoi creare [!DNL Google Ads] e [!DNL Microsoft Advertising] tipi di pubblico in base ai clienti dagli elenchi di dati dei clienti. È inoltre possibile aggiornare qualsiasi pubblico di [!DNL Google Ads] o [!DNL Microsoft Advertising] con corrispondenza cliente ad eccezione di [!DNL Google Ads] tipi di pubblico creati da un pubblico di [!DNL Adobe].

## Creare un pubblico di corrispondenza cliente da un elenco di dati cliente

Account *[!DNL Google Ads]e [!DNL Microsoft Advertising] idonei solo per la corrispondenza cliente*

È possibile creare un elenco basato su dati cliente [!DNL Google Ads] o [!DNL Microsoft Advertising] da un file di dati generato dal sistema CRM (Customer Relationship Management).

Per gli account [!DNL Microsoft Advertising], il file può includere indirizzi di posta elettronica. Per gli account [!DNL Google Ads], il file può includere indirizzi e-mail, indirizzi postali o numeri di telefono, ID utente o ID dispositivo mobile dal CRM.

>[!NOTE]
>
>Search, Social e Commerce non memorizzano i dati dei clienti caricati o dei segmenti [!DNL Adobe] utilizzati per creare o modificare un pubblico [!DNL Google Ads] o [!DNL Microsoft Advertising].

1. Genera un file con i dati del cliente nel formato richiesto.

   È necessario eseguire l’hashing di nomi e cognomi, indirizzi e-mail e numeri di telefono utilizzando l’algoritmo SHA-256. <!-- Our UI says all, but GGL docs say don't hash user IDs and device IDs. --> Per i tipi di pubblico [!DNL Google Ads], consulta la documentazione [!DNL Google Ads] su &quot;[Linee guida per la formattazione per il caricamento di dati con hash](https://support.google.com/google-ads/answer/7476159)&quot; per un elenco dei campi e dei requisiti consentiti per le informazioni di contatto. Per i tipi di pubblico [!DNL Microsoft Advertising], consulta la documentazione di [!DNL Microsoft Advertising] su [preparazione degli elenchi di corrispondenza dei clienti](https://help.ads.microsoft.com/#apex/ads/en/56921. Facoltativamente, è possibile scaricare un modello [!DNL Microsoft Excel] per informazioni di contatto.

1. Nel menu principale, fare clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nei sottomenu, fare clic su **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Nella barra degli strumenti sopra la tabella dati, fare clic su ![Crea](/help/search-social-commerce/assets/add.png "Crea").

1. Selezionare la rete di annunci e il nome account, quindi fare clic su **[!UICONTROL Continue]**.

1. Specifica le informazioni sul pubblico:

   1. Nel menu [!UICONTROL Data Source], selezionare **[!UICONTROL Customer List]**.

   1. Immettere **[!UICONTROL Audience Name]**.

   1. Carica il file:

      1. Selezionare [!UICONTROL Data Upload Type]: *[!UICONTROL Emails, Phones, and/or Mailing Addresses]*, *[!UICONTROL User IDs]* o *[!UICONTROL Mobile Device IDs]*.

         L&#39;opzione ID utente è disponibile solo per [!DNL Google Ads] inserzionisti negli Stati Uniti che hanno acconsentito a [segmenti ID utente](https://support.google.com/google-ads/answer/9199250)

      1. (Solo per elenchi di ID di dispositivi mobili) Seleziona **[!UICONTROL OS Type]** (*[!UICONTROL Android™]* o *[!UICONTROL iOS]*) e immetti **[!UICONTROL App ID]**.

         L’App ID è un identificatore univoco utilizzato dal sistema operativo mobile per consentire alla tua applicazione di connettersi all’App Store di Google Play o Apple:

         * ([!DNL Android™] app) Il nome del pacchetto [!DNL Android™] in [!DNL Google Play], identificato da &quot;`id=<package_name>`&quot;.

           Ad esempio, in https://play.google.com/store/apps/details?id=com.example.game, il nome del pacchetto è com.example.game.

         * ([!DNL iOS] app) L&#39;ID applicazione all&#39;interno di [!DNL iTunes App Store], identificato da &quot;`<idNNNNNNNNN>`&quot; alla fine dell&#39;URL. È disponibile anche in [!DNL iOS Developer Console].

           Ad esempio, in https://itunes.apple.com/us/app/id284882215, l’ID è id284882215.

         Il tuo team di sviluppo ha accesso a [!UICONTROL App ID] per la piattaforma pertinente.

      1. Nel campo [!UICONTROL Select File], fare clic su **[!UICONTROL Choose File]** e selezionare il file sulla rete o sul dispositivo.

      1. Selezionare la casella di controllo per indicare che si accettano i termini delle politiche sulla privacy di [!DNL Adobe] e della rete di annunci.

      1. (Inserzionisti che creano [!DNL Google Ads] tipi di pubblico che conducono attività commerciali nello Spazio economico europeo (SEE) o nel Regno Unito (UK); facoltativo) Se hai raccolto il consenso degli utenti di EEA e UK a caricare i loro dati a scopo pubblicitario, seleziona la casella di controllo accanto a **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

      [!DNL Google Ads] ignora eventuali dati per gli utenti di EEA e UK con uno stato di consenso non specificato. Questo può causare discrepanze di dati e problemi di prestazioni.

      1. Fare clic su **[!UICONTROL Upload File]**.

   1. Specifica il numero di **[!UICONTROL Membership Days]**, che è il numero di giorni in cui il cookie di un utente resta nel pubblico.

   Utilizza il periodo di tempo per il quale prevedi che l’annuncio sia rilevante per l’utente. Gli elenchi dei clienti scadono solo se si immette un valore.

1. Fare clic su **[!UICONTROL Post]**.

>[!NOTE]
>
>* L’elaborazione del file da parte della rete di annunci potrebbe richiedere fino a 24 ore.
>* Consulta la [[!DNL Google Ads] documentazione sul funzionamento e le limitazioni della corrispondenza con i clienti](https://support.google.com/displayvideo/answer/9539301).

## Modificare un pubblico con Customer Match utilizzando un elenco di dati cliente

È possibile aggiornare qualsiasi pubblico di tipo [!DNL Google Ads] o [!DNL Microsoft Advertising] con corrispondenza cliente ad eccezione di [!DNL Google Ads] tipi di pubblico creati da un pubblico [!DNL Adobe]. Puoi caricare dati per aggiungere, eliminare o sostituire tutti i dati esistenti per il pubblico.

I dati devono essere dello stesso tipo dell’elenco clienti originale (indirizzi e-mail, indirizzi postali, numeri di telefono, ID utente o ID dispositivo mobile per un’app specifica su un sistema operativo mobile specifico).

1. Genera un file con i dati del cliente nel formato richiesto per il tipo di dati esistente.

È necessario eseguire l’hashing di nomi e cognomi, indirizzi e-mail e numeri di telefono utilizzando l’algoritmo SHA-256. <!-- Our UI says all, but GGL docs say don't hash user IDs and device IDs. --> Per i tipi di pubblico [!DNL Google Ads], consulta la documentazione [!DNL Google Ads] su &quot;[Linee guida per la formattazione per il caricamento di dati con hash](https://support.google.com/google-ads/answer/7476159)&quot; per un elenco dei campi e dei requisiti consentiti per le informazioni di contatto. Per i tipi di pubblico [!DNL Microsoft Advertising], consulta la documentazione di [!DNL Microsoft Advertising] su [preparazione degli elenchi di corrispondenza dei clienti](https://help.ads.microsoft.com/#apex/ads/en/56921. Facoltativamente, è possibile scaricare un modello [!DNL Microsoft Excel] per informazioni di contatto.

1. Nel menu principale, fare clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nei sottomenu, fare clic su **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Seleziona la casella di controllo accanto al pubblico da modificare.

1. Nella barra degli strumenti sopra la tabella dati, fare clic su ![Modifica](/help/search-social-commerce/assets/edit.png).

1. Selezionare l&#39;azione: *[!UICONTROL Add]* (per aggiungere i dati caricati ai dati esistenti, a meno che non esistano già), *[!UICONTROL Delete]* (per eliminare i dati caricati dai dati esistenti, quando esistono già) o *[!UICONTROL Replace]* (per eliminare tutti i dati esistenti e sostituirli con i dati caricati).

1. Carica il file:

   1. Nel campo [!UICONTROL Select File], fare clic su **[!UICONTROL Choose File]** e selezionare il file sulla rete o sul dispositivo.

   1. Selezionare la casella di controllo per indicare che si accettano i termini delle politiche sulla privacy di [!DNL Adobe] e della rete di annunci.

   1. Fare clic su **[!UICONTROL Upload File]**.

1. Fare clic su **[!UICONTROL Post]**.

>[!NOTE]
>
>L’elaborazione degli aggiornamenti a un pubblico da parte della rete di annunci potrebbe richiedere del tempo.

>[!MORELIKETHIS]
>
>* [Informazioni sui tipi di pubblico](audience-about.md)
>* [Crea [!DNL Google Ads] audience corrispondenti ai clienti da [!DNL Adobe] audience](google-audience-from-adobe-audience.md)
>* [Creazione di un pubblico di tipo customer match [!DNL Google Ads] da un elenco e-mail di Adobe Campaign](google-audience-from-campaign-email-list.md)
>* [Gestione dei tipi di pubblico di remarketing dinamico](audience-dynamic-remarketing-manage.md)
