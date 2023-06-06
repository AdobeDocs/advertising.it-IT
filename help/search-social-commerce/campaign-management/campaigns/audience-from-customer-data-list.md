---
title: Gestire i tipi di pubblico in base ai clienti utilizzando gli elenchi di dati dei clienti
description: Scopri come creare e modificare [!DNL Google Ads] e [!DNL Microsoft® Advertising] i clienti abbinano i tipi di pubblico dagli elenchi di dati cliente.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '807'
ht-degree: 0%

---

# Gestisci [!DNL Google Ads] e [!DNL Microsoft® Advertising] customer match audience utilizzando gli elenchi di dati cliente

Puoi creare [!DNL Google Ads] e [!DNL Microsoft® Advertising] i clienti abbinano i tipi di pubblico dagli elenchi di dati cliente. Puoi anche aggiornare qualsiasi [!DNL Google Ads] o [!DNL Microsoft® Advertising] audience di customer match ad eccezione di [!DNL Google Ads] tipi di pubblico creati da un [!DNL Adobe] pubblico.

## Creare un pubblico di corrispondenza cliente da un elenco di dati cliente

*[!DNL Google Ads]e [!DNL Microsoft® Advertising] account idonei solo per il confronto con i clienti*

Puoi creare una [!DNL Google Ads] o [!DNL Microsoft® Advertising] elenco basato su dati cliente da un file di dati generato dal sistema di gestione delle relazioni con i clienti (CRM).

Per [!DNL Microsoft® Advertising] account, il file può includere indirizzi e-mail. Per [!DNL Google Ads] account, il file può includere indirizzi e-mail, indirizzi postali o numeri di telefono; ID utente; o ID dispositivo mobile dal tuo CRM.

>[!NOTE]
>
>Search, Social e Commerce non memorizzano i dati dei clienti che carichi o dai [!DNL Adobe] segmenti utilizzati per creare o modificare un [!DNL Google Ads] o [!DNL Microsoft® Advertising] pubblico.

1. Genera un file con i dati del cliente nel formato richiesto.

   È necessario eseguire l’hashing di nomi e cognomi, indirizzi e-mail e numeri di telefono utilizzando l’algoritmo SHA-256. <!-- Our UI says all, but GGL docs say don't hash user IDs and device IDs. --> Per [!DNL Google Ads] tipi di pubblico, consulta la [!DNL Google Ads] documentazione su &quot;[Linee guida sulla formattazione per il caricamento di dati con hash](https://support.google.com/google-ads/answer/7476159)&quot; per un elenco dei campi e dei requisiti consentiti per le informazioni di contatto. Per [!DNL Microsoft® Advertising] tipi di pubblico, consulta la [!DNL Microsoft® Advertising] documentazione su [preparazione degli elenchi di corrispondenza cliente](https://help.ads.microsoft.com/#apex/ads/en/56921. Facoltativamente, puoi scaricare una [!DNL Microsoft® Excel] modello per informazioni di contatto.

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nei sottomenu, fare clic su **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Nella barra degli strumenti sopra la tabella dati, fai clic su ![Crea](/help/search-social-commerce/assets/add.png "Crea").

1. Seleziona la rete di annunci e il nome dell’account, quindi fai clic su **[!UICONTROL Continue]**.

1. Specifica le informazioni sul pubblico:

   1. In [!UICONTROL Data Source] menu, seleziona **[!UICONTROL Customer List]**.

   1. Inserisci il **[!UICONTROL Audience Name]**.

   1. Carica il file:

      1. Seleziona la [!UICONTROL Data Upload Type]: *[!UICONTROL Emails, Phones, and/or Mailing Addresses]*, *[!UICONTROL User IDs]*, o *[!UICONTROL Mobile Device IDs]*.

         L’opzione ID utente è disponibile solo per [!DNL Google Ads] inserzionisti negli Stati Uniti che hanno acconsentito [segmenti ID utente](https://support.google.com/google-ads/answer/9199250)

      1. (Solo per elenchi di ID di dispositivi mobili) Seleziona il **[!UICONTROL OS Type]** (*[!UICONTROL Android™]* o *[!UICONTROL iOS]*) e immettere il **[!UICONTROL App ID]**.

         L’App ID è un identificatore univoco utilizzato dal sistema operativo mobile per consentire alla tua applicazione di connettersi all’App Store di Google Play o Apple:

         * ([!DNL Android™] app) Il [!DNL Android™] nome pacchetto in [!DNL Google Play], identificato da &quot;`id=<package_name>`.&quot;

            Ad esempio, in https://play.google.com/store/apps/details?id=com.example.game, il nome del pacchetto è com.example.game.

         * ([!DNL iOS] app) L&#39;ID applicazione all&#39;interno del [!DNL iTunes App Store], identificato da &quot;`<idNNNNNNNNN>`&quot; alla fine dell’URL. È disponibile anche nel [!DNL iOS Developer Console].

            Ad esempio, in https://itunes.apple.com/us/app/id284882215, l’ID è id284882215.
         Il tuo team di sviluppo ha accesso a [!UICONTROL App ID] per la piattaforma pertinente.

      1. In [!UICONTROL Select File] , fare clic su **[!UICONTROL Choose File]** e selezionare il file sulla rete o sul dispositivo.

      1. Selezionare la casella di controllo per indicare che si accettano i termini del [!DNL Adobe] e le policy sulla privacy della rete di annunci.

      1. Clic **[!UICONTROL Upload File]**.
   1. Specifica il numero di **[!UICONTROL Membership Days]**, che è il numero di giorni in cui il cookie di un utente resta nel pubblico.

   Utilizza il periodo di tempo per il quale prevedi che l’annuncio sia rilevante per l’utente. Gli elenchi dei clienti scadono solo se si immette un valore.

1. Clic **[!UICONTROL Post]**.

>[!NOTE]
>
>* L’elaborazione del file da parte della rete di annunci potrebbe richiedere fino a 24 ore.
>* Consulta [[!DNL Google Ads] documentazione su come funziona la corrispondenza con i clienti e limitazioni](https://support.google.com/displayvideo/answer/9539301).


## Modificare un pubblico con Customer Match utilizzando un elenco di dati cliente

È possibile aggiornare qualsiasi [!DNL Google Ads] o [!DNL Microsoft® Advertising] audience di customer match ad eccezione di [!DNL Google Ads] tipi di pubblico creati da un [!DNL Adobe] pubblico. Puoi caricare dati per aggiungere, eliminare o sostituire tutti i dati esistenti per il pubblico.

I dati devono essere dello stesso tipo dell’elenco clienti originale (indirizzi e-mail, indirizzi postali, numeri di telefono, ID utente o ID dispositivo mobile per un’app specifica su un sistema operativo mobile specifico).

1. Genera un file con i dati del cliente nel formato richiesto per il tipo di dati esistente.

È necessario eseguire l’hashing di nomi e cognomi, indirizzi e-mail e numeri di telefono utilizzando l’algoritmo SHA-256. <!-- Our UI says all, but GGL docs say don't hash user IDs and device IDs. --> Per [!DNL Google Ads] tipi di pubblico, consulta la [!DNL Google Ads] documentazione su &quot;[Linee guida sulla formattazione per il caricamento di dati con hash](https://support.google.com/google-ads/answer/7476159)&quot; per un elenco dei campi e dei requisiti consentiti per le informazioni di contatto. Per [!DNL Microsoft® Advertising] tipi di pubblico, consulta la [!DNL Microsoft® Advertising] documentazione su [preparazione degli elenchi di corrispondenza cliente](https://help.ads.microsoft.com/#apex/ads/en/56921. Facoltativamente, puoi scaricare una [!DNL Microsoft® Excel] modello per informazioni di contatto.

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nei sottomenu, fare clic su **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Seleziona la casella di controllo accanto al pubblico da modificare.

1. Nella barra degli strumenti sopra la tabella dati, fai clic su ![Modifica](/help/search-social-commerce/assets/edit.png).

1. Seleziona l’azione: *[!UICONTROL Add]* (per aggiungere i dati caricati ai dati esistenti, a meno che non esistano già), *[!UICONTROL Delete]* (per eliminare i dati caricati dai dati esistenti, se già esistenti), oppure *[!UICONTROL Replace]* per eliminare tutti i dati esistenti e sostituirli con i dati caricati.

1. Carica il file:

   1. In [!UICONTROL Select File] , fare clic su **[!UICONTROL Choose File]** e selezionare il file sulla rete o sul dispositivo.

   1. Selezionare la casella di controllo per indicare che si accettano i termini del [!DNL Adobe] e le policy sulla privacy della rete di annunci.

   1. Clic **[!UICONTROL Upload File]**.

1. Clic **[!UICONTROL Post]**.

>[!NOTE]
>
>L’elaborazione degli aggiornamenti a un pubblico da parte della rete di annunci potrebbe richiedere del tempo.

>[!MORELIKETHIS]
>
>* [Informazioni sui tipi di pubblico](audience-about.md)
>* [Crea [!DNL Google Ads] audience di corrispondenza cliente da [!DNL Adobe] audience](google-audience-from-adobe-audience.md)
>* [Creare un [!DNL Google Ads] customer match audience da un elenco e-mail di Adobe Campaign](google-audience-from-campaign-email-list.md)
>* [Gestire i tipi di pubblico di remarketing dinamico](audience-dynamic-remarketing-manage.md)

