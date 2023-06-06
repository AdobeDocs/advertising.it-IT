---
title: Gestisci [!DNL Microsoft Advertising] tipi di pubblico di remarketing dinamico
description: Scopri come creare e gestire [!DNL Microsoft Advertising] tipi di pubblico di remarketing dinamico.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 0%

---

# Gestisci [!DNL Microsoft Advertising] tipi di pubblico di remarketing dinamico

*[!DNL Microsoft Advertising]solo account*

Puoi creare una [!DNL Microsoft Advertising] pubblico di remarketing dinamico quando utilizzi il tag di conversione JavaScript e tracciamento del pubblico del motore di ricerca sulle pagine web. Ogni pubblico viene creato utilizzando un tag specificato incluso nelle pagine Web di cui gli utenti faranno parte. Puoi creare più tipi di pubblico con lo stesso tag di tracciamento. Puoi anche modificare il nome e l’origine dati dei tipi di pubblico esistenti o eliminare tipi di pubblico esistenti.

I tipi di pubblico di remarketing dinamico hanno il tipo di pubblico &quot;[!UICONTROL Dynamic Remarketing] \&lt;visitor type=&quot;&quot;>&quot; (ad esempio &quot;Acquirenti passati per il remarketing dinamico&quot;).

Per ulteriori informazioni sul remarketing dinamico e su come implementare il tag JavaScript richiesto, consulta la [[!DNL Microsoft Advertising] documentazione sul remarketing dinamico](https://help.ads.microsoft.com/#apex/ads/en/56910).

## Creare un pubblico di remarketing dinamico

>[!NOTE]
>
>Per [!DNL Microsoft Advertising] account, il tag JavaScript deve includere [parametri di tipo pagina e ID prodotto](https://help.ads.microsoft.com/#apex/ads/en/56910/1/#exp85).

1. Identifica il nome del [!DNL Microsoft Advertising] tag di tracciamento degli eventi universali (UET) incluso nelle pagine web da cui verrà creato il pubblico.

   Il nome del tag sarà necessario in un passaggio successivo.

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nei sottomenu, fare clic su **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Nella barra degli strumenti sopra la tabella dati, fai clic su ![Crea](/help/search-social-commerce/assets/add.png "Crea").

1. Seleziona la rete di annunci e il nome dell’account, quindi fai clic su **[!UICONTROL Continue]**.

1. Specifica le informazioni sul pubblico:

   1. In **[!UICONTROL Data Source]** menu, seleziona **[!UICONTROL Dynamic Remarketing List]**.

   1. Inserisci il **[!UICONTROL Audience Name]**.

   1. Dall’elenco di tutti i tag disponibili per l’account del motore di ricerca, seleziona il nome [!DNL Microsoft Advertising] Tag UET incluso nelle pagine Web i cui utenti costituiranno il pubblico.

   1. Seleziona il tipo di visitatore per il pubblico, in base alle azioni del visitatore sulle pagine web pertinenti: *[!UICONTROL General Visitors]*, *[!UICONTROL Product Searchers]*, *[!UICONTROL Product Viewers]*, *[!UICONTROL Past Buyers]*, o *[!UICONTROL Shopping Cart Abandoners]*.

   1. Specifica il numero di **[!UICONTROL Membership Days]**, che è il numero di giorni in cui il cookie di un utente resta nel pubblico. I valori possono essere compresi tra uno (1) e 180.

      Utilizza il periodo di tempo per il quale prevedi che l’annuncio sia rilevante per l’utente.

1. Clic **[!UICONTROL Post]**.

>[!NOTE]
>
>Il tuo [!DNL Microsoft Advertising] gli elenchi di remarketing dinamico sono idonei per il targeting una volta che includono almeno 300 utenti.

## Modificare un pubblico di remarketing dinamico

È possibile modificare il nome e l&#39;origine dati di un [!DNL Microsoft Advertising] pubblico di remarketing dinamico. Impossibile modificare il valore di [!UICONTROL Membership Days] impostazione.

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nei sottomenu, fare clic su **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Seleziona la casella di controllo accanto al pubblico da modificare.

1. Nella barra degli strumenti sopra la tabella dati, fai clic su ![Modifica](/help/search-social-commerce/assets/edit.png "Modifica").

1. Modifica le informazioni sul pubblico:

   1. In **[!UICONTROL Data Source]** , fare clic su ![Modifica](/help/search-social-commerce/assets/edit.png "Modifica").

   1. (Facoltativo) Modifica il **[!UICONTROL Audience Name]**.

   1. (Facoltativo) Da un elenco di tutti i tag disponibili per l’account di rete dell’annuncio, modifica il nome del [!DNL Microsoft Advertising] Tag UET incluso nelle pagine Web i cui utenti costituiranno il pubblico.

   1. (Facoltativo) Modifica il tipo di visitatore per il pubblico, che si basa sulle azioni del visitatore sulle pagine web pertinenti: *[!UICONTROL General Visitors]*, *[!UICONTROL Product Searchers]*, *[!UICONTROL Product Viewers]*, *[!UICONTROL Past Buyers]*, o *[!UICONTROL Shopping Cart Abandoners]*.

   1. Clic **[!UICONTROL Post]**.

## Eliminare un pubblico di remarketing dinamico

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nei sottomenu, fare clic su **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. (Facoltativo) Filtra l’elenco per includere tipi di pubblico specifici.

1. Seleziona la casella di controllo accanto a ciascun pubblico da eliminare.

   Per suggerimenti sulla selezione di più righe, vedere &quot;[Seleziona più righe](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

1. Nel messaggio di conferma, fai clic su **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Informazioni sui tipi di pubblico](audience-about.md)
>* [Crea [!DNL Google Ads] audience di corrispondenza cliente da [!DNL Adobe] audience](google-audience-from-adobe-audience.md)
>* [Creare un [!DNL Google Ads] customer match audience da un elenco e-mail di Adobe Campaign](google-audience-from-campaign-email-list.md)
>* [Gestire i tipi di pubblico in base ai clienti utilizzando gli elenchi di dati dei clienti](audience-from-customer-data-list.md)

