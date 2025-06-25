---
title: Gestire i gruppi di prodotti
description: Scopri come creare e gestire i gruppi di prodotti per lo shopping nelle campagne di acquisto.
exl-id: cf818b87-ee4b-4cf5-a4e8-0b9a7fc32182
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '720'
ht-degree: 0%

---

# Gestire i gruppi di prodotti

Solo *[!DNL Google Ads]e [!DNL Microsoft Advertising] campagne acquisti*

È possibile creare e modificare i gruppi di prodotti ed eliminare i gruppi di prodotti e i relativi gruppi di prodotti figlio nella visualizzazione [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups].

## Crea un gruppo di prodotti [!UICONTROL All Products]

Prima di poter creare gruppi di prodotti con attributi specifici, è necessario creare un gruppo di prodotti completo denominato &quot;[!UICONTROL All Products]&quot;. Ogni gruppo di annunci può avere un solo gruppo &quot;[!UICONTROL All Products]&quot;.

>[!TIP]
>
>Per creare più componenti account contemporaneamente, utilizza [bulksheet campagna](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Nel menu principale, fare clic su **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nel sottomenu, fare clic su **[!UICONTROL Live]>[!UICONTROL Product Groups]**.

1. Nella barra degli strumenti sopra la tabella dati, fare clic su ![Crea](/help/search-social-commerce/assets/add.png "Crea").

1. Selezionare la rete di annunci, l&#39;account, la campagna e il gruppo di annunci, quindi fare clic su **[!UICONTROL Continue]**.

1. Specifica le [[!DNL Google Ads] impostazioni gruppo di prodotti](product-group-settings-google.md) o [[!DNL Microsoft Advertising] impostazioni gruppo di prodotti](product-group-settings-microsoft.md).

1. Fare clic su **[!UICONTROL Post]**.

## Creare un nodo gruppo di prodotti figlio in un gruppo di prodotti esistente

Dopo aver creato almeno un gruppo &quot;[!UICONTROL All Products]&quot; completo per un gruppo di annunci, è possibile creare nodi gruppo di prodotti figlio per sottoinsiemi di prodotti da includere o escludere dalla gara, con uno o più gruppi di prodotti che hanno come target lo stesso attributo in ogni livello (ad esempio, [!UICONTROL Brand]=Acme per un gruppo di prodotti e [!UICONTROL Brand]=AcmePlus per un altro allo stesso livello. È possibile creare fino a sette livelli di nodi del gruppo di prodotti figlio, escluso &quot;[!UICONTROL All Products]&quot;.

>[!NOTE]
>
>Impossibile creare un gruppo di prodotti figlio per un gruppo di prodotti &quot;[!UICONTROL Everything Else]&quot;.

>[!TIP]
>
>Per creare più componenti account contemporaneamente, utilizza [bulksheet campagna](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Nel menu principale, fare clic su **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nel sottomenu, fare clic su **[!UICONTROL Live]>[!UICONTROL Product Groups]**.

1. (Facoltativo) Per visualizzare un gruppo di prodotti e i relativi nodi figlio del gruppo di prodotti nella visualizzazione Struttura, posizionare il cursore sul nome del gruppo di prodotti, fare clic sull&#39;![icona Menu](/help/search-social-commerce/assets/arrow-dropdown-menu.png "icona Menu"), quindi selezionare **[!UICONTROL Tree View]**.

1. Posizionare il cursore sul nome del gruppo di prodotti, fare clic su ![Menu a discesa freccia](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Menu a discesa freccia"), quindi selezionare **[!UICONTROL + Add Node]**.

1. Specifica le [[!DNL Google Ads] impostazioni gruppo di prodotti](product-group-settings-google.md) o [[!DNL Microsoft Advertising] impostazioni gruppo di prodotti](product-group-settings-microsoft.md), inclusi la dimensione e l&#39;attributo del prodotto.

1. Fare clic su **[!UICONTROL Post]**.

## Modifica impostazioni nodo gruppo di prodotti

Puoi modificare il modello di offerta e tracciamento per i nodi del gruppo di prodotti di unità (gruppi di prodotti senza nodi del gruppo di prodotti figlio) inclusi per un gruppo di annunci. Non è possibile modificare alcuna informazione per i gruppi di prodotti di unità esclusi o per i nodi di suddivisione inclusi o esclusi, che sono gruppi di prodotti con nodi di gruppi di prodotti figlio.

1. Nel menu principale, fare clic su **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nel sottomenu, fare clic su **[!UICONTROL Live]>[!UICONTROL Product Groups]**.

1. (Facoltativo) Per visualizzare un gruppo di prodotti e i relativi nodi figlio del gruppo di prodotti nella visualizzazione Struttura, posizionare il cursore sul nome del gruppo di prodotti, fare clic sull&#39;![icona Menu](/help/search-social-commerce/assets/arrow-dropdown-menu.png "icona Menu"), quindi selezionare **[!UICONTROL Tree View]**.

1. Effettuare una delle seguenti operazioni:

   1. Per modificare le impostazioni per un singolo nodo gruppo di prodotti, posizionare il cursore sul nome del gruppo di prodotti, fare clic sull&#39;icona ![Menu](/help/search-social-commerce/assets/arrow-dropdown-menu.png "icona Menu"), quindi selezionare **[!UICONTROL + Edit Node]**.

   1. (Per modificare le impostazioni per uno o più gruppi di annunci) Effettua le seguenti operazioni:

      1. Selezionare la casella di controllo accanto a ogni nodo.

         Per suggerimenti sulla selezione di più righe, vedere &quot;[Selezionare più righe](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

      1. Nella barra degli strumenti sopra la tabella dati, fare clic su ![Modifica](/help/search-social-commerce/assets/edit.png "Modifica").

1. Modifica le [[!DNL Google Ads] impostazioni gruppo di prodotti](product-group-settings-google.md) o [[!DNL Microsoft Advertising] impostazioni gruppo di prodotti](product-group-settings-microsoft.md).

   Per più nodi, le modifiche vengono applicate a tutti i nodi selezionati. Per il campo [!UICONTROL Bid], sono disponibili opzioni per modificare i valori esistenti in un valore specificato o per aumentare o diminuire l&#39;importo di una percentuale o importo monetario specificato, con un limite. Per il campo [!UICONTROL Tracking Template] è possibile modificare i valori esistenti in un valore specificato, sostituire una stringa esistente con una stringa specificata, aggiungere un prefisso specificato all&#39;inizio di ogni valore oppure aggiungere un suffisso alla fine di ogni valore.

1. (Facoltativo) Fare clic su **[!UICONTROL Additional Details]** e, facoltativamente, immettere un nome e una descrizione per il progetto.

1. Fare clic su **[!UICONTROL Post]**.

## Eliminare i nodi del gruppo di prodotti

Puoi eliminare qualsiasi gruppo di prodotti, ad eccezione di un gruppo &quot;Tutto il resto&quot; quando esistono altri gruppi di prodotti allo stesso livello, utilizzato per determinare quali prodotti nell’account del centro commerciale sono inclusi negli annunci commerciali per il gruppo di annunci. Se si elimina un gruppo di prodotti, vengono eliminati anche tutti i gruppi di prodotti secondari.

1. Nel menu principale, fare clic su **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nel sottomenu, fare clic su **[!UICONTROL Live]>[!UICONTROL Product Groups]**.

1. (Facoltativo) Filtra l’elenco per includere specifici gruppi di prodotti.

1. Effettuare una delle seguenti operazioni:

   * Per eliminare un gruppo di prodotti, fare clic nella colonna **[!UICONTROL Status]** e selezionare **[!UICONTROL Delete]**.

   * Per eliminare uno o più gruppi di prodotti, eseguire le operazioni seguenti:

      1. Selezionare la casella di controllo accanto a ogni gruppo di prodotti che si desidera eliminare.

         Per suggerimenti sulla selezione di più righe, vedere &quot;[Selezionare più righe](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

      1. Nella barra degli strumenti, fare clic su ![Altro](/help/search-social-commerce/assets/more.png "Altro") e selezionare **[!UICONTROL Delete]**.

      1. Nel messaggio di conferma, fare clic su **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Informazioni sull&#39;acquisto di gruppi di prodotti](product-group-about.md)
>* [[!DNL Google Ads] impostazioni gruppo di prodotti](product-group-settings-google.md)
>* [[!DNL Microsoft Advertising] impostazioni gruppo di prodotti](product-group-settings-microsoft.md)
