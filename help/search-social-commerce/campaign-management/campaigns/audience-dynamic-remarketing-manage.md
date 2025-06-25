---
title: Gestisci [!DNL Microsoft Advertising] tipi di pubblico di remarketing dinamico
description: Scopri come creare e gestire [!DNL Microsoft Advertising] tipi di pubblico di remarketing dinamico.
exl-id: 52faab75-e723-4e59-aac6-b4d0c4c1cf60
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 0%

---

# Gestisci [!DNL Microsoft Advertising] tipi di pubblico di remarketing dinamico

Solo *[!DNL Microsoft Advertising]account*

Puoi creare un pubblico di remarketing dinamico [!DNL Microsoft Advertising] quando utilizzi il tag di conversione e tracciamento del pubblico di JavaScript del motore di ricerca sulle tue pagine Web. Ogni pubblico viene creato utilizzando un tag specificato incluso nelle pagine web di cui fanno parte gli utenti. Puoi creare più tipi di pubblico con lo stesso tag di tracciamento. Puoi anche modificare il nome e l’origine dati dei tipi di pubblico esistenti o eliminare tipi di pubblico esistenti.

I tipi di pubblico di remarketing dinamico hanno il tipo di pubblico &quot;[!UICONTROL Dynamic Remarketing] \&lt;Tipo visitatore\>&quot; (ad esempio &quot;Acquirenti passati per il remarketing dinamico&quot;).

Per ulteriori informazioni sul remarketing dinamico e su come implementare il tag JavaScript richiesto, consulta la [[!DNL Microsoft Advertising] documentazione sul remarketing dinamico](https://help.ads.microsoft.com/#apex/ads/en/56910).

## Creare un pubblico di remarketing dinamico

>[!NOTE]
>
>Per gli account [!DNL Microsoft Advertising], il tag JavaScript deve includere [l&#39;ID prodotto e i parametri del tipo di pagina](https://help.ads.microsoft.com/#apex/ads/en/56910/1/#exp85).

1. Identifica il nome del tag di tracciamento evento universale (UET) [!DNL Microsoft Advertising] incluso nelle pagine Web da cui verrà creato il pubblico.

   Il nome del tag sarà necessario in un passaggio successivo.

1. Nel menu principale, fare clic su **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nei sottomenu, fare clic su **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Nella barra degli strumenti sopra la tabella dati, fare clic su ![Crea](/help/search-social-commerce/assets/add.png "Crea").

1. Selezionare la rete di annunci e il nome account, quindi fare clic su **[!UICONTROL Continue]**.

1. Specifica le informazioni sul pubblico:

   1. Nel menu **[!UICONTROL Data Source]**, selezionare **[!UICONTROL Dynamic Remarketing List]**.

   1. Immettere **[!UICONTROL Audience Name]**.

   1. Da un elenco di tutti i tag disponibili per l&#39;account del motore di ricerca, selezionare il nome del tag UET [!DNL Microsoft Advertising] incluso nelle pagine Web i cui utenti costituiscono il pubblico.

   1. Selezionare il tipo di visitatore per il pubblico, basato sulle azioni del visitatore nelle pagine Web pertinenti: *[!UICONTROL General Visitors]*, *[!UICONTROL Product Searchers]*, *[!UICONTROL Product Viewers]*, *[!UICONTROL Past Buyers]* o *[!UICONTROL Shopping Cart Abandoners]*.

   1. Specifica il numero di **[!UICONTROL Membership Days]**, che è il numero di giorni in cui il cookie di un utente resta nel pubblico. I valori possono essere compresi tra uno (1) e 180.

      Utilizza il periodo di tempo per il quale prevedi che l’annuncio sia rilevante per l’utente.

1. Fare clic su **[!UICONTROL Post]**.

>[!NOTE]
>
>Gli elenchi di remarketing dinamico di [!DNL Microsoft Advertising] sono idonei per il targeting una volta che includono almeno 300 utenti.

## Modificare un pubblico di remarketing dinamico

È possibile modificare il nome e l&#39;origine dati per un pubblico di remarketing dinamico [!DNL Microsoft Advertising]. Impossibile modificare il valore dell&#39;impostazione [!UICONTROL Membership Days].

1. Nel menu principale, fare clic su **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nei sottomenu, fare clic su **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Seleziona la casella di controllo accanto al pubblico da modificare.

1. Nella barra degli strumenti sopra la tabella dati, fare clic su ![Modifica](/help/search-social-commerce/assets/edit.png "Modifica").

1. Modifica le informazioni sul pubblico:

   1. Nella sezione **[!UICONTROL Data Source]**, fai clic su ![Modifica](/help/search-social-commerce/assets/edit.png "Modifica").

   1. (Facoltativo) Modificare **[!UICONTROL Audience Name]**.

   1. (Facoltativo) Da un elenco di tutti i tag disponibili per l&#39;account di rete dell&#39;annuncio, modificare il nome del tag UET [!DNL Microsoft Advertising] incluso nelle pagine Web i cui utenti costituiscono il pubblico.

   1. (Facoltativo) Modifica il tipo di visitatore per il pubblico, che si basa sulle azioni del visitatore nelle pagine Web pertinenti: *[!UICONTROL General Visitors]*, *[!UICONTROL Product Searchers]*, *[!UICONTROL Product Viewers]*, *[!UICONTROL Past Buyers]* o *[!UICONTROL Shopping Cart Abandoners]*.

   1. Fare clic su **[!UICONTROL Post]**.

## Eliminare un pubblico di remarketing dinamico

1. Nel menu principale, fare clic su **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nei sottomenu, fare clic su **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. (Facoltativo) Filtra l’elenco per includere tipi di pubblico specifici.

1. Seleziona la casella di controllo accanto a ciascun pubblico da eliminare.

   Per suggerimenti sulla selezione di più righe, vedere &quot;[Selezionare più righe](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Nel messaggio di conferma, fare clic su **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Informazioni sui tipi di pubblico](audience-about.md)
>* [Crea [!DNL Google Ads] audience corrispondenti ai clienti da [!DNL Adobe] audience](google-audience-from-adobe-audience.md)
>* [Creazione di un pubblico di tipo customer match [!DNL Google Ads] da un elenco e-mail di Adobe Campaign](google-audience-from-campaign-email-list.md)
>* [Gestire i tipi di pubblico in base ai clienti utilizzando gli elenchi di dati dei clienti](audience-from-customer-data-list.md)
