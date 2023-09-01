---
title: Crea [!DNL Google Ads] audience di corrispondenza cliente da [!DNL Adobe] audience
description: Scopri come creare [!DNL Google Ads] i clienti abbinano i tipi di pubblico dei tipi di pubblico esistenti di Adobe Analytics e di Audienci Manager.
exl-id: 17cf0729-bc13-4ec3-918e-039ecdc91a41
feature: Search Campaign Management
source-git-commit: aa913130d0f611c4164ef8bdca57983d8c6c0405
workflow-type: tm+mt
source-wordcount: '576'
ht-degree: 0%

---

# Crea [!DNL Google Ads] i clienti abbinano i tipi di pubblico di Adobe Analytics e di Audienci Manager

*[!DNL Google Ads]account idonei solo per il confronto con i clienti*

*Per gli inserzionisti con un’integrazione solo Adobi Advertising-Adobe Audience Manager o Adobe Advertising-Adobe Analytics*

Gli inserzionisti con consenso possono creare [!DNL Google Ads] i clienti abbinano i tipi di pubblico utilizzando gli ID utente di a) [!DNL Analytics] segmenti condivisi con Adobe Experience Cloud e b) segmenti di Audience Manager con Search, Social e Commerce come destinazione, tra cui [!DNL Analytics] segmenti pubblicati in Adobe Experience Cloud e segmenti creati utilizzando la Libreria tipi di pubblico di Adobe Experience Cloud. Search, Social e Commerce spingono automaticamente un [!DNL Google] URL di tracciamento per ogni [!DNL Analytics] o Audience Manager segmento in modo che [!DNL Google] può tracciare il pubblico.

Ogni [!DNL Adobe] il pubblico può essere utilizzato per un solo [!DNL Google] pubblico.

Ogni nuovo [!DNL Google] il pubblico ha lo stesso nome dell’originale [!DNL Adobe] pubblico. [!DNL Google] determina le dimensioni del pubblico per poter essere targetizzato.

>[!TIP]
>
>Per la segmentazione in tempo reale, utilizza tipi di pubblico creati da Audienci Manager. Segmenti creati in [!DNL Analytics] e sincronizzati con Adobe Experience Cloud possono avere popolazioni più piccole perché vengono sincronizzati solo ogni giorno; un surfista idoneo per un segmento non può essere incluso nel segmento fino al giorno successivo. Segmenti da [!DNL Analytics] hanno un’origine dati &quot;suite di rapporti - .&quot;

>[!NOTE]
>
>Search, Social e Commerce non memorizzano i dati dei clienti provenienti dai [!DNL Adobe] segmenti utilizzati per creare o modificare un [!DNL Google] pubblico.

1. Completa i prerequisiti in base alle esigenze:

   1. (Per creare tipi di pubblico per elenchi di remarketing con ID utente) Un [!DNL Adobe] l’utente amministratore o l’account manager deve selezionare l’impostazione a livello di inserzionista per abilitare i tipi di pubblico in customer match.

   1. Implementare [Servizio Adobe Experience Platform Identity](https://experienceleague.adobe.com/docs/id-service/using/home.html) versione 2.0 o successiva.

   1. Distribuisci il seguente tag il più in alto possibile sulle pagine web dell’inserzionista da cui monitorare il pubblico

      `<script src="//pixel.everesttech.net/rlsa/<Advertising_Cloud_UserID>" type="text/javascript"> </script>`

      dove `Advertising_Cloud_UserID` è l&#39;ID utente numerico univoco assegnato all&#39;inserzionista.

      Esempio: `<script src="//pixel.everesttech.net/rlsa/1234" type="text/javascript"> </script>`

   1. (Se non è già stato completato) Un utente autorizzato deve configurare l’account dell’inserzionista su [sincronizza con l&#39;account organizzazione dell&#39;inserzionista in Adobe Experience Cloud](/help/search-social-commerce/admin/sync-adobe-audiences.md).

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nei sottomenu, fare clic su **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Nella barra degli strumenti sopra la tabella dati, fai clic su ![Crea](/help/search-social-commerce/assets/add.png "Crea").

1. Seleziona la rete di annunci e il nome dell’account, quindi fai clic su **[!UICONTROL Continue]**.

1. Specifica le informazioni sul pubblico:

   1. In **[!UICONTROL Data Source]** menu, seleziona **[!UICONTROL Adobe Audience]**.

   1. Seleziona la [!UICONTROL Adobe Audience] su cui basare [!DNL Google] pubblico.

      >[!NOTE]
      >
      >[!DNL Adobe] tipi di pubblico già utilizzati per un altro [!DNL Google] pubblico non disponibile.

      Facoltativamente, puoi cercare tipi di pubblico che contengono una stringa di testo specifica con un minimo di tre caratteri. Per qualsiasi pubblico corrispondente, fai clic su **[!UICONTROL Include]** per selezionarlo.

      Se si selezionano più [!DNL Adobe] tipi di pubblico, quindi un pubblico separato [!DNL Google] Il pubblico viene creato per ciascun pubblico.

   1. Seleziona la **[!UICONTROL Audience Type]** per creare: **[!UICONTROL Customer List_User ID]**.

      Dell&#39;inserzionista [!DNL Google Ads] l&#39;account deve essere [idoneo per la corrispondenza personalizzata](https://support.google.com/adspolicy/answer/6299717) e ha acconsentito [remarketing con ID utente](https://support.google.com/google-ads/answer/9199250).

   1. Selezionare la casella di controllo per indicare che si accettano i termini del [!DNL Adobe] e le policy sulla privacy della rete di annunci.

   1. Specifica il numero di **[!UICONTROL Membership Days]**, che è il numero di giorni in cui il cookie di un utente resta nel pubblico.

      Utilizza il periodo di tempo per il quale prevedi che l’annuncio sia rilevante per l’utente. Gli elenchi per il remarketing hanno una durata massima di 540 giorni. Gli elenchi dei clienti non hanno una durata massima; per indicare che il cookie non scade, immetti 10000.

   1. Clic **[!UICONTROL Post]**.

>[!NOTE]
>
>* [!DNL Google] potrebbero essere necessarie fino a 24 ore per elaborare il file.
>
>* Consulta [[!DNL Google Ads] documentazione su come funziona la corrispondenza con i clienti e limitazioni](https://support.google.com/displayvideo/answer/9539301).

>[!MORELIKETHIS]
>
>* [Informazioni sui tipi di pubblico](audience-about.md)
>* [Creare un [!DNL Google Ads] customer match audience da un elenco e-mail di Adobe Campaign](google-audience-from-campaign-email-list.md)
>* [Gestire i tipi di pubblico in base ai clienti utilizzando gli elenchi di dati dei clienti](audience-from-customer-data-list.md)
>* [Gestire i tipi di pubblico di remarketing dinamico](audience-dynamic-remarketing-manage.md)
