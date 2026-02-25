---
title: Assegnare valori di classificazione ai componenti account dalle viste di gestione delle campagne
description: Scopri come assegnare i valori di classificazione ai componenti dell’account.
exl-id: 5a3cb059-9cff-4a2e-b8aa-be8626774377
feature: Search Label Classifications
source-git-commit: d68107b04762ea149dd74fb30ab7ea9d8850915f
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 0%

---

# Assegnare valori di classificazione ai componenti account dalle viste di gestione delle campagne

Puoi assegnare e rimuovere i valori di classificazione per le seguenti entità di ricerca dalle viste di gestione della campagna: campagna, gruppo di annunci, parola chiave, annuncio, posizionamento, gruppo di prodotti a livello di unità e destinazione di ricerca dinamica. Se necessario, è possibile creare classificazioni e valori di classificazione durante il processo di assegnazione. Ogni classificazione di etichetta può avere fino a 2000 valori.

Ogni entità può avere un valore di etichetta per classificazione. Ad esempio, Shoes_Campaign può avere un valore Color di &quot;rosso&quot; e un valore Geo di &quot;Los Angeles&quot;, ma non può avere più valori Color o Geo.

I valori delle etichette vengono ereditati dalle entità figlio, pertanto non immettere valori per le entità figlio a meno che non si desideri sostituire i valori ereditati.

>[!NOTE]
>
>Le parole chiave e la copia dell&#39;annuncio per alcune reti di annunci e tipi di campagne sono [non modificabili](/help/search-social-commerce/campaign-management/faqs-campaigns.md), il che significa che la loro modifica elimina l&#39;entità esistente e ne crea una nuova. Quando un’entità esistente viene eliminata in questo modo, la classificazione dell’etichetta non viene assegnata alla nuova entità.

## (Nuova interfaccia) Assegnare i valori di classificazione ai componenti dell’account

Puoi assegnare i valori di classificazione a tutti i componenti account applicabili disponibili nella nuova interfaccia utente.

1. Aprire la visualizzazione entità dal menu **[!UICONTROL Manage]** o **[!UICONTROL Target]**.

1. Selezionare la casella di controllo accanto a ogni riga pertinente.

   Per suggerimenti sulla selezione di più righe, vedere &quot;[Selezionare più righe](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Nella barra degli strumenti delle azioni in blocco, fare clic su **+[!UICONTROL Assign]** > **[!UICONTROL Label Classification]**.

1. Per ogni valore di classificazione applicabile, effettua le seguenti operazioni:

   1. Nella colonna **[!UICONTROL Classifications]**, specifica la classificazione:

      * Per utilizzare una classificazione esistente, fai clic sul nome della classificazione per espanderla.

      * Per creare una classificazione, fare clic su [!UICONTROL +] nell&#39;intestazione di colonna. Nel campo di input, immetti il nome della classificazione, quindi fai clic su ![Salva](/help/search-social-commerce/assets/save-checkmark.png "Salva") per salvare immediatamente la classificazione. Per utilizzare la nuova classificazione, fai clic sul nome della classificazione per espanderla.

        Il nome deve essere composto da [caratteri ASCII 32-126](https://www.asciitable.com/) e la lunghezza massima è di 27 caratteri a byte singolo.

   1. Nella colonna **[!UICONTROL Value Name]**, specifica il valore per la classificazione selezionata:

      * Per utilizzare un valore esistente, selezionate il valore.

      * Per creare un valore, fare clic su [!UICONTROL +] nell&#39;intestazione di colonna. Nel campo di input immettere il valore, quindi fare clic su ![Salva](/help/search-social-commerce/assets/save-checkmark.png "Salva") per salvare immediatamente il valore e selezionarlo per impostazione predefinita.

        La lunghezza massima è di 100 caratteri e può includere caratteri ASCII e non ASCII.

1. Fare clic su **+[!UICONTROL Assign Now]**.

## (Interfaccia precedente) Assegna valori di classificazione ai componenti dell’account

1. Fare clic su **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**, quindi selezionare la visualizzazione del componente account.

1. Effettuare una delle seguenti operazioni:

   * (Per assegnare valori a una singola entità) Posizionare il cursore sul nome dell&#39;entità, fare clic su ![Pulsante Menu](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Pulsante Menu"), quindi selezionare **[!UICONTROL Classification]**.

   * Per assegnare valori a una o più entità, effettuare le seguenti operazioni:

      * Selezionare la casella di controllo accanto a ogni riga pertinente.

        Per suggerimenti sulla selezione di più righe, vedere &quot;[Selezionare più righe](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

      * Nella barra degli strumenti sopra la tabella dati fare clic su ![Altro](/help/search-social-commerce/assets/more.png "Altro") e quindi su **[!UICONTROL Classification]**.

1. In [!UICONTROL Assignment Details] eseguire una delle operazioni seguenti:

   * Per modificare i valori delle classificazioni esistenti in nuovi valori, selezionare **[!UICONTROL Set To]**.

     La lunghezza massima di ogni valore è di 100 caratteri e può includere caratteri ASCII e non ASCII.

   * Per assegnare i valori di classificazione specificati senza rimuovere i valori esistenti, selezionare **[!UICONTROL Assign]**.

   * Per rimuovere specifici valori di classificazione attualmente assegnati, selezionare **[!UICONTROL Remove]**.

     Quando rimuovi un valore di classificazione, i dati del rapporto relativi a tale valore non sono più disponibili per i componenti dell’account specificati.

   * Per eliminare i valori di classificazione specificati, selezionare **[!UICONTROL Delete]**.

     L’eliminazione di un valore di classificazione ne rende impossibile l’utilizzo futuro e i dati del rapporto non sono più disponibili per tale valore. Tutte le assegnazioni tra i valori e i componenti specifici dell’account vengono rimosse, ma i componenti dell’account non vengono eliminati.

1. Per ogni valore di classificazione applicabile, effettua le seguenti operazioni:

   1. Nella colonna **[!UICONTROL Classification]**, specifica il nome della classificazione:

      * Per utilizzare una classificazione esistente, fai clic sul nome della classificazione per espanderla.

      * Per creare una classificazione, fare clic su [!UICONTROL +]. Nel campo di input, immetti il nome della classificazione, quindi fai clic su ![Salva](/help/search-social-commerce/assets/select.png "Salva") per salvare immediatamente la classificazione.

        Il nome deve essere composto da [caratteri ASCII 32-126](https://www.asciitable.com/) e la lunghezza massima è di 27 caratteri a byte singolo.

   1. Nella colonna **[!UICONTROL Value Name]** specificare il nome del valore:

      * Per utilizzare un valore esistente, fai clic sul nome del valore per selezionarlo.

      * Per creare un valore, fare clic su [!UICONTROL +]. Immettere il valore nel campo di input, quindi fare clic su ![Salva](/help/search-social-commerce/assets/select.png "Salva") per salvare immediatamente il valore.

        La lunghezza massima è di 100 caratteri e può includere caratteri ASCII e non ASCII.

1. (Facoltativo) Immettere ulteriori dettagli:

   1. Accanto a **[!UICONTROL Additional Details]**, fai clic su ![Apri](/help/search-social-commerce/assets/chevron-up.png "Apri") per espandere i dettagli.

   1. Immettere un **[!UICONTROL Project Name]** facoltativo e/o un **[!UICONTROL Description]** facoltativo.

1. Fare clic su **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Informazioni sulle classificazioni delle etichette](classification-about.md)
>* [Creare una classificazione di etichette](classification-create.md)
>* [Assegna valori di classificazione ai componenti account tramite bulksheet](classification-values-assign-bulksheets.md)
>* [Rimuovere i valori di classificazione delle etichette dai componenti dell&#39;account](classification-values-remove.md)
>* [Elimina i valori di classificazione delle etichette](classification-values-delete.md)
>* [Elimina classificazioni etichette](classification-delete.md)
