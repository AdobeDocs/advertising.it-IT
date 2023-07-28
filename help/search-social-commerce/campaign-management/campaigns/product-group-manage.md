---
title: Gestire i gruppi di prodotti
description: Scopri come creare e gestire i gruppi di prodotti per lo shopping nelle campagne di acquisto.
exl-id: 25912abd-1ddb-443f-a16d-7efe57093677
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '720'
ht-degree: 0%

---

# Gestire i gruppi di prodotti

*[!DNL Google Ads]e [!DNL Microsoft Advertising] solo campagne di acquisto*

È possibile creare e modificare gruppi di prodotti ed eliminare gruppi di prodotti e i relativi gruppi di prodotti figlio nel [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups] visualizzazione.

## Crea un’&quot;[!UICONTROL All Products]&quot; gruppo di prodotti

Prima di poter creare gruppi di prodotti con attributi specifici, devi creare un gruppo di prodotti completo denominato &quot;[!UICONTROL All Products].&quot; Ogni gruppo di annunci può averne solo uno &quot;[!UICONTROL All Products]&quot;.

>[!TIP]
>
>Per creare più componenti account contemporaneamente, utilizza [bulksheet delle campagne](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nel sottomenu, fai clic su **[!UICONTROL Live]>[!UICONTROL Product Groups]**.

1. Nella barra degli strumenti sopra la tabella dati, fai clic su ![Crea](/help/search-social-commerce/assets/add.png "Crea").

1. Seleziona la rete di annunci, l’account, la campagna e il gruppo di annunci, quindi fai clic su **[!UICONTROL Continue]**.

1. Specifica la [[!DNL Google Ads] impostazioni gruppo di prodotti](product-group-settings-google.md) o [[!DNL Microsoft Advertising] impostazioni gruppo di prodotti](product-group-settings-microsoft.md).

1. Clic **[!UICONTROL Post]**.

## Creare un nodo gruppo di prodotti figlio in un gruppo di prodotti esistente

Dopo aver creato almeno un’&quot;All-inclusive&quot;[!UICONTROL All Products]&quot; per un gruppo di annunci, puoi creare nodi figlio per un gruppo di prodotti per sottoinsiemi di prodotti da includere o escludere dalla gara, con uno o più gruppi di prodotti che hanno come target lo stesso attributo in ogni livello (ad esempio, [!UICONTROL Brand]=Acme per un gruppo di prodotti e [!UICONTROL Brand]=AcmePlus per un altro allo stesso livello. Puoi creare fino a sette livelli di nodi di gruppi di prodotti secondari, escluso &quot;[!UICONTROL All Products]&quot;.

>[!NOTE]
>
>Non puoi creare un gruppo di prodotti secondario per un’&quot;[!UICONTROL Everything Else]&quot; gruppo di prodotti.

>[!TIP]
>
>Per creare più componenti account contemporaneamente, utilizza [bulksheet delle campagne](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nel sottomenu, fai clic su **[!UICONTROL Live]>[!UICONTROL Product Groups]**.

1. (Facoltativo) Per visualizzare un gruppo di prodotti e i relativi nodi figlio nella visualizzazione Struttura, posizionare il cursore sul nome del gruppo di prodotti e fare clic su ![Icona menu](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Icona menu")e quindi selezionare **[!UICONTROL Tree View]**.

1. Posizionare il cursore sul nome del gruppo di prodotti e fare clic su ![Menu a discesa Freccia](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Menu a discesa Freccia")e quindi selezionare **[!UICONTROL + Add Node]**.

1. Specifica la [[!DNL Google Ads] impostazioni gruppo di prodotti](product-group-settings-google.md) o [[!DNL Microsoft Advertising] impostazioni gruppo di prodotti](product-group-settings-microsoft.md), inclusi la dimensione e l’attributo del prodotto.

1. Clic **[!UICONTROL Post]**.

## Modifica impostazioni nodo gruppo di prodotti

Puoi modificare il modello di offerta e tracciamento per i nodi del gruppo di prodotti di unità (gruppi di prodotti senza nodi del gruppo di prodotti figlio) inclusi per un gruppo di annunci. Non è possibile modificare alcuna informazione per i gruppi di prodotti di unità esclusi o per i nodi di suddivisione inclusi o esclusi, che sono gruppi di prodotti con nodi di gruppi di prodotti figlio.

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nel sottomenu, fai clic su **[!UICONTROL Live]>[!UICONTROL Product Groups]**.

1. (Facoltativo) Per visualizzare un gruppo di prodotti e i relativi nodi figlio nella visualizzazione Struttura, posizionare il cursore sul nome del gruppo di prodotti e fare clic su ![Icona menu](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Icona menu")e quindi selezionare **[!UICONTROL Tree View]**.

1. Effettuare una delle seguenti operazioni:

   1. Per modificare le impostazioni per un singolo nodo gruppo di prodotti, posiziona il cursore sul nome del gruppo di prodotti e fai clic su ![Icona menu](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Icona menu")e quindi selezionare **[!UICONTROL + Edit Node]**.

   1. (Per modificare le impostazioni per uno o più gruppi di annunci) Effettua le seguenti operazioni:

      1. Selezionare la casella di controllo accanto a ogni nodo.

         Per suggerimenti sulla selezione di più righe, vedere &quot;[Seleziona più righe](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      1. Nella barra degli strumenti sopra la tabella dati, fai clic su ![Modifica](/help/search-social-commerce/assets/edit.png "Modifica").

1. Modifica il [[!DNL Google Ads] impostazioni gruppo di prodotti](product-group-settings-google.md) o [[!DNL Microsoft Advertising] impostazioni gruppo di prodotti](product-group-settings-microsoft.md).

   Per più nodi, le modifiche vengono applicate a tutti i nodi selezionati. Per [!UICONTROL Bid] , sono disponibili opzioni per modificare i valori esistenti in un valore specificato o per aumentare o diminuire l&#39;importo di una percentuale o di un importo monetario specificato, con un limite. Per [!UICONTROL Tracking Template] , è possibile modificare i valori esistenti in un valore specificato, sostituire una stringa esistente con una stringa specificata, aggiungere un prefisso specificato all&#39;inizio di ogni valore o aggiungere un suffisso alla fine di ogni valore.

1. (Facoltativo) Fai clic su **[!UICONTROL Additional Details]** e facoltativamente inserire il nome e la descrizione del progetto.

1. Clic **[!UICONTROL Post]**.

## Eliminare i nodi del gruppo di prodotti

Puoi eliminare qualsiasi gruppo di prodotti, ad eccezione di un gruppo &quot;Tutto il resto&quot; quando esistono altri gruppi di prodotti allo stesso livello, utilizzato per determinare quali prodotti nell’account del centro commerciale sono inclusi negli annunci commerciali per il gruppo di annunci. Se si elimina un gruppo di prodotti, vengono eliminati anche tutti i gruppi di prodotti secondari.

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nel sottomenu, fai clic su **[!UICONTROL Live]>[!UICONTROL Product Groups]**.

1. (Facoltativo) Filtra l’elenco per includere specifici gruppi di prodotti.

1. Effettuare una delle seguenti operazioni:

   * Per eliminare un gruppo di prodotti, fai clic su nella **[!UICONTROL Status]** e seleziona **[!UICONTROL Delete]**.

   * Per eliminare uno o più gruppi di prodotti, eseguire le operazioni seguenti:

      1. Selezionare la casella di controllo accanto a ogni gruppo di prodotti che si desidera eliminare.

         Per suggerimenti sulla selezione di più righe, vedere &quot;[Seleziona più righe](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      1. Nella barra degli strumenti, fai clic su ![Altro](/help/search-social-commerce/assets/more.png "Altro") e seleziona **[!UICONTROL Delete]**.

      1. Nel messaggio di conferma, fai clic su **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Informazioni sui gruppi di prodotti di acquisto](product-group-about.md)
>* [[!DNL Google Ads] impostazioni gruppo di prodotti](product-group-settings-google.md)
>* [[!DNL Microsoft Advertising] impostazioni gruppo di prodotti](product-group-settings-microsoft.md)
