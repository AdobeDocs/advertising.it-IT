---
title: Gestire i target di pubblico per campagne e gruppi di annunci
description: Scopri come configurare e gestire i target del pubblico per le campagne e i gruppi di annunci  [!DNL Google Ads] e [!DNL Microsoft Advertising] .
exl-id: 9a496d15-082d-44e1-a0a3-71356e24b932
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '771'
ht-degree: 0%

---

# Gestisci i target del pubblico per le campagne e i gruppi di annunci [!DNL Google Ads] e [!DNL Microsoft Advertising]

Solo *[!DNL Google Ads]e [!DNL Microsoft Advertising]*

[!DNL Google Ads] campagne e gruppi di annunci e [!DNL Microsoft Advertising] gruppi di annunci possono eseguire il targeting di tipi di pubblico specifici dalla stessa rete di annunci. La rete di annunci determina la dimensione del pubblico che deve essere targetizzabile.

>[!NOTE]
>
>Le esclusioni sovrascrivono sempre le inclusioni/destinazioni.

Puoi configurare i target del pubblico, modificare i modificatori di offerte per i target del pubblico e modificare lo stato dei target del pubblico.

## Configurare i target del pubblico

1. Nel menu principale, fare clic su **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nei sottomenu, fare clic su **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]**.

1. Nella barra degli strumenti sopra la tabella dati, fare clic su ![Crea](/help/search-social-commerce/assets/add.png "Crea").

1. Selezionare la rete di annunci e il nome account, quindi fare clic su **[!UICONTROL Continue]**.

1. Configura i target del pubblico per campagne e gruppi di annunci specifici:

   1. Seleziona i tipi di pubblico applicabili per la rete di annunci specificata.

      Facoltativamente, puoi cercare tipi di pubblico che contengono una stringa di testo specifica con un minimo di tre caratteri. Per qualsiasi pubblico corrispondente, fare clic su **[!UICONTROL Include]** per selezionarlo.

      I tipi di pubblico di [!DNL Google Ads] customer match sono disponibili solo per le campagne di ricerca e shopping.

   1. Specificare le destinazioni:

      1. (Facoltativo) Per espandere una campagna e i relativi gruppi di annunci secondari, fai clic sul nome della campagna.

      1. (Facoltativo) Per filtrare un elenco di campagne o un elenco di gruppi di annunci in base a una stringa di testo inclusa nel nome, fai clic su ![Filtro](/help/search-social-commerce/assets/filter.png "Filtro") , immetti o incolla la stringa di testo nel campo di input, quindi premi il tasto **[!UICONTROL Enter]**.

      1. Specifica ogni campagna e destinazione gruppo di annunci per la rete di annunci specificata facendo clic sul cerchio vuoto adiacente in modo da visualizzare un segno di spunta blu (![Seleziona](/help/search-social-commerce/assets/include.png "Seleziona")).

      Non puoi configurare una destinazione sia per una campagna principale che per un gruppo di annunci secondario (che utilizza automaticamente la destinazione).

1. Fare clic su **[!UICONTROL Post]**.

1. (Facoltativo) Impostare un adeguamento dell&#39;offerta per l&#39;obiettivo in uno dei seguenti modi dalla vista [!UICONTROL Targets]:

   * Fare clic nella colonna **[!UICONTROL Bid Adjustment]** e immettere un valore.

   * Selezionare la casella di controllo accanto alla riga di destinazione. Nella barra degli strumenti fare clic su ![Modifica](/help/search-social-commerce/assets/edit.png "Modifica"), immettere il modificatore di offerta e quindi fare clic su **[!UICONTROL Post]**.

   I valori possono includere:

   * *0%:* per non regolare le offerte per gli annunci per questo pubblico.

   * /[*Altri valori da -90% a 900%*/]: per aumentare o diminuire l&#39;offerta per gli annunci per questo pubblico. Ad esempio, se l’offerta a livello di parola chiave è 1 USD e la regolazione dell’offerta per un target di pubblico specifico è del 50%, l’offerta per quel pubblico aumenta a 1,50 USD.

## Modificare il modificatore di offerta per i target di pubblico

Puoi modificare il modificatore di offerta e lo stato dei target del pubblico per tutti i tipi di pubblico ad eccezione di quelli sul mercato.

>[!NOTE]
>
>Search, Social e Commerce ottimizzano automaticamente il modificatore di offerta quando la campagna principale utilizza la strategia di offerta CPC ed è in un portfolio configurato per ottimizzare automaticamente i valori di regolazione delle offerte per i target di pubblico.

1. Nel menu principale, fare clic su **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nei sottomenu, fare clic su **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]**.

1. Effettuare una delle seguenti operazioni:

   * Per modificare un modificatore di offerta per una destinazione, fare clic nella colonna **[!UICONTROL Bid Adjustment]** e modificare la regolazione dell&#39;offerta.

   * Per modificare un modificatore di offerta per una o più destinazioni, effettuare le seguenti operazioni:

      1. Selezionare la casella di controllo accanto a ogni destinazione da modificare.

         Per suggerimenti sulla selezione di più righe, vedere &quot;[Selezionare più righe](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

      1. Nella barra degli strumenti sopra la tabella dati, fare clic su ![Modifica](/help/search-social-commerce/assets/edit.png "Modifica").

      1. Modificare i campi **[!UICONTROL Bid Modifier]** e/o **[!UICONTROL Status]**.

         Per il campo [!UICONTROL Bid Modifier], sono disponibili opzioni per modificare i valori esistenti in un valore specificato o per aumentare o diminuire l&#39;importo di una percentuale o importo monetario specificato, con un limite.

         Per un valore impostato, il valore può includere:

         * *0%:* per non regolare le offerte per gli annunci per questo pubblico.

         * /[*Altri valori da -90% a 900%*/]: per aumentare o diminuire l&#39;offerta per gli annunci per questo pubblico. Ad esempio, se l’offerta a livello di parola chiave è 1 USD e la regolazione dell’offerta per un target di pubblico specifico è del 50%, l’offerta per quel pubblico aumenta a 1,50 USD.

         Per più destinazioni, le modifiche vengono applicate a tutte le destinazioni selezionate.

      1. (Facoltativo) Fare clic su **[!UICONTROL Additional Details]** e, facoltativamente, immettere un nome e una descrizione per il progetto.

      1. Fare clic su **[!UICONTROL Post]**.

## Modificare lo stato dei target di pubblico

Puoi mettere in pausa un target di pubblico attivo per disabilitare le offerte su di esso. In seguito puoi riprendere l’offerta riportando lo stato attivo.

Puoi anche eliminare un target di pubblico di ricerca attivo o in pausa.

1. Nel menu principale, fare clic su **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nei sottomenu, fare clic su **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]**.

1. (Facoltativo) Filtra l’elenco per includere target di pubblico specifici.

1. Seleziona la casella di controllo accanto a ogni pubblico di destinazione di cui desideri modificare lo stato.

   Per suggerimenti sulla selezione di più righe, vedere &quot;[Selezionare più righe](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Nella barra degli strumenti, fai clic sul pulsante di stato:

   * Per attivare le righe, fare clic su ![Attiva](/help/search-social-commerce/assets/activate.png "Attiva").

   * Per sospendere le righe, fare clic su ![Pausa](/help/search-social-commerce/assets/pause.png "Pausa").

   * Per eliminare le righe, fare clic su ![Altre azioni](/help/search-social-commerce/assets/more.png "Altre azioni") e selezionare **[!UICONTROL Delete]**. Nel messaggio di conferma, fare clic su **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Informazioni sui tipi di pubblico](audience-about.md)
>* [Gestire le esclusioni di pubblico per campagne e gruppi di annunci](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md)
