---
title: Crea [!DNL Google Ads] audience corrispondenti ai clienti da [!DNL Adobe] audience
description: Scopri come creare  [!DNL Google Ads] tipi di pubblico in base ai clienti, partendo dai tipi di pubblico esistenti di Adobe Analytics e Audience Manager.
exl-id: 7de95ebb-24b0-459f-83c0-7b85b0c0576d
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '566'
ht-degree: 0%

---

# Crea [!DNL Google Ads] tipi di pubblico in base ai clienti da Adobe Analytics e Audience Manager

*[!DNL Google Ads]account idonei solo per la corrispondenza cliente*

*Inserzionisti solo con integrazione Adobe Advertising-Adobe Audience Manager o Adobe Advertising-Adobe Analytics*

Gli inserzionisti che hanno prestato il consenso possono creare [!DNL Google Ads] tipi di pubblico in base ai clienti, utilizzando gli ID utente di a) [!DNL Analytics] segmenti condivisi con Adobe Experience Cloud e b) segmenti di Audience Manager con Search, Social e Commerce come destinazione, inclusi [!DNL Analytics] segmenti pubblicati in Adobe Experience Cloud e segmenti creati utilizzando la Libreria tipi di pubblico di Adobe Experience Cloud. Search, Social e Commerce inviano automaticamente un URL di tracciamento [!DNL Google] a ciascun segmento di [!DNL Analytics] o Audience Manager in modo che [!DNL Google] possa tracciare il pubblico.

Ogni pubblico [!DNL Adobe] può essere utilizzato per un solo pubblico [!DNL Google].

Ogni nuovo pubblico [!DNL Google] ha lo stesso nome del pubblico [!DNL Adobe] originale. [!DNL Google] determina la dimensione del pubblico per poter essere targetizzato.

>[!TIP]
>
>Per la segmentazione in tempo reale, utilizza tipi di pubblico creati da Audience Manager. I segmenti creati in [!DNL Analytics] e sincronizzati con Adobe Experience Cloud possono avere popolazioni più piccole perché vengono sincronizzati solo ogni giorno; un surfista idoneo per un segmento non può essere incluso nel segmento fino al giorno successivo. I segmenti da [!DNL Analytics] hanno un&#39;origine dati &quot;suite di rapporti - .&quot;

>[!NOTE]
>
>Search, Social e Commerce non memorizzano i dati dei clienti dei tuoi segmenti [!DNL Adobe] utilizzati per creare o modificare un pubblico [!DNL Google].

1. Completa i prerequisiti in base alle esigenze:

   1. (Per creare tipi di pubblico per l&#39;elenco di remarketing degli ID utente) Un utente amministratore o un account manager [!DNL Adobe] deve selezionare l&#39;impostazione a livello di inserzionista per abilitare i tipi di pubblico per la corrispondenza dei clienti.

   1. Implementare il [servizio Adobe Experience Platform Identity](https://experienceleague.adobe.com/docs/id-service/using/home.html) versione 2.0 o successiva.

   1. Distribuisci il seguente tag il più in alto possibile sulle pagine web dell’inserzionista da cui monitorare il pubblico

      `<script src="//pixel.everesttech.net/rlsa/<Advertising_Cloud_UserID>" type="text/javascript"> </script>`

      dove `Advertising_Cloud_UserID` è l&#39;ID utente numerico univoco assegnato all&#39;inserzionista.

      Esempio: `<script src="//pixel.everesttech.net/rlsa/1234" type="text/javascript"> </script>`

   1. (Se non è già stato completato) Un utente autorizzato deve configurare l&#39;account dell&#39;inserzionista per [sincronizzarlo con l&#39;account organizzazione dell&#39;inserzionista in Adobe Experience Cloud](/help/search-social-commerce/admin/sync-adobe-audiences.md).

1. Nel menu principale, fare clic su **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nei sottomenu, fare clic su **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Nella barra degli strumenti sopra la tabella dati, fare clic su ![Crea](/help/search-social-commerce/assets/add.png "Crea").

1. Selezionare la rete di annunci e il nome account, quindi fare clic su **[!UICONTROL Continue]**.

1. Specifica le informazioni sul pubblico:

   1. Nel menu **[!UICONTROL Data Source]**, selezionare **[!UICONTROL Adobe Audience]**.

   1. Selezionare [!UICONTROL Adobe Audience] su cui basare il pubblico [!DNL Google].

      >[!NOTE]
      >
      >[!DNL Adobe] tipi di pubblico già utilizzati per un altro pubblico [!DNL Google] non sono disponibili.

      Facoltativamente, puoi cercare tipi di pubblico che contengono una stringa di testo specifica con un minimo di tre caratteri. Per qualsiasi pubblico corrispondente, fare clic su **[!UICONTROL Include]** per selezionarlo.

      Se selezioni più tipi di pubblico [!DNL Adobe], viene creato un pubblico [!DNL Google] separato per ciascuno di essi.

   1. Selezionare **[!UICONTROL Audience Type]** da creare: **[!UICONTROL Customer List_User ID]**.

      L&#39;account [!DNL Google Ads] dell&#39;inserzionista deve essere [idoneo per la corrispondenza personalizzata](https://support.google.com/adspolicy/answer/6299717) e ha acconsentito alla [remarketing ID utente](https://support.google.com/google-ads/answer/9199250).

   1. Selezionare la casella di controllo per indicare che si accettano i termini delle politiche sulla privacy di [!DNL Adobe] e della rete di annunci.

   1. Specifica il numero di **[!UICONTROL Membership Days]**, che è il numero di giorni in cui il cookie di un utente resta nel pubblico.

      Utilizza il periodo di tempo per il quale prevedi che l’annuncio sia rilevante per l’utente. Gli elenchi per il remarketing hanno una durata massima di 540 giorni. Gli elenchi dei clienti non hanno una durata massima; per indicare che il cookie non scade, immetti 10000.

   1. Fare clic su **[!UICONTROL Post]**.

>[!NOTE]
>
>* [!DNL Google] potrebbe richiedere fino a 24 ore per elaborare il file.
>
>* Consulta la [[!DNL Google Ads] documentazione sul funzionamento e le limitazioni della corrispondenza con i clienti](https://support.google.com/displayvideo/answer/9539301).

>[!MORELIKETHIS]
>
>* [Informazioni sui tipi di pubblico](audience-about.md)
>* [Creazione di un pubblico di tipo customer match [!DNL Google Ads] da un elenco e-mail di Adobe Campaign](google-audience-from-campaign-email-list.md)
>* [Gestire i tipi di pubblico in base ai clienti utilizzando gli elenchi di dati dei clienti](audience-from-customer-data-list.md)
>* [Gestione dei tipi di pubblico di remarketing dinamico](audience-dynamic-remarketing-manage.md)
