---
title: Assegnare valori di classificazione ai componenti account dalle viste di gestione delle campagne
description: Scopri come assegnare i valori di classificazione ai componenti dell’account.
exl-id: 7e55d7d8-5e12-409b-ad5d-c53cbf24c7c9
feature: Search Label Classifications
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---

# Assegnare valori di classificazione ai componenti account dalle viste di gestione delle campagne

Puoi assegnare e rimuovere i valori di classificazione per le seguenti entità di ricerca dalle viste di gestione della campagna: campagna, gruppo di annunci, parola chiave, annuncio, posizionamento, gruppo di prodotti a livello di unità e destinazione di ricerca dinamica. Se necessario, è possibile creare classificazioni e valori di classificazione durante il processo di assegnazione. Ogni classificazione di etichetta può avere fino a 2000 valori.

Ogni entità può avere un valore di etichetta per classificazione. Ad esempio, Shoes_Campaign può avere un valore Color di &quot;rosso&quot; e un valore Geo di &quot;Los Angeles&quot;, ma non può avere più valori Color o Geo.

I valori delle etichette vengono ereditati dalle entità figlio, pertanto non immettere valori per le entità figlio a meno che non si desideri sostituire i valori ereditati.

>[!NOTE]
>
>Le parole chiave e la copia dell’annuncio per alcune reti e tipi di campagne pubblicitarie sono [non modificabile](/help/search-social-commerce/campaign-management/faqs-campaigns.md), il che significa che la loro modifica elimina l’entità esistente e ne crea una nuova. Quando un’entità esistente viene eliminata in questo modo, la classificazione dell’etichetta non viene assegnata alla nuova entità.

1. Clic **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** e quindi selezionare la vista del componente conto.

1. Effettuare una delle seguenti operazioni:

   * Per assegnare valori a una singola entità, posizionate il cursore sul nome dell&#39;entità e fate clic su ![Pulsante Menu](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Pulsante Menu")e quindi selezionare **[!UICONTROL Classification]**.

   * Per assegnare valori a una o più entità, effettuare le seguenti operazioni:

      * Selezionare la casella di controllo accanto a ogni riga pertinente.

        Per suggerimenti sulla selezione di più righe, vedere &quot;[Seleziona più righe](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      * Nella barra degli strumenti sopra la tabella dati, fai clic su ![Altro](/help/search-social-commerce/assets/more.png "Altro")e quindi fare clic su **[!UICONTROL Classification]**.

1. In [!UICONTROL Assignment Details], eseguire una delle operazioni seguenti:

   * Per modificare i valori delle classificazioni esistenti in nuovi valori, seleziona **[!UICONTROL Set To]**.

     La lunghezza massima di ogni valore è di 100 caratteri e può includere caratteri ASCII e non ASCII.

   * Per assegnare i valori di classificazione specificati senza rimuovere i valori esistenti, seleziona **[!UICONTROL Assign]**.

   * Per rimuovere specifici valori di classificazione attualmente assegnati, seleziona **[!UICONTROL Remove]**.

     Quando rimuovi un valore di classificazione, i dati del rapporto relativi a tale valore non sono più disponibili per i componenti dell’account specificati.

   * Per eliminare i valori di classificazione specificati, seleziona **[!UICONTROL Delete]**.

     L’eliminazione di un valore di classificazione ne rende impossibile l’utilizzo futuro e i dati del rapporto non sono più disponibili per tale valore. Tutte le assegnazioni tra i valori e i componenti specifici dell’account vengono rimosse, ma i componenti dell’account non vengono eliminati.

1. Per ogni valore di classificazione applicabile, effettua le seguenti operazioni:

   1. In **[!UICONTROL Classification]** , specifica il nome della classificazione:

      * Per utilizzare una classificazione esistente, fai clic sul nome della classificazione per espanderla.

      * Per creare una classificazione, fai clic su [!UICONTROL +]. Nel campo di input, inserisci il nome della classificazione, quindi fai clic su ![Salva](/help/search-social-commerce/assets/select.png "Salva") per salvare immediatamente la classificazione.

        Il nome deve essere costituito da [Caratteri ASCII: 32-126](https://www.asciitable.com/), e la lunghezza massima è di 27 caratteri a byte singolo.

   1. In **[!UICONTROL Value Name]** , specifica il nome del valore:

      * Per utilizzare un valore esistente, fai clic sul nome del valore per selezionarlo.

      * Per creare un valore, fai clic su [!UICONTROL +]. Nel campo di immissione immettere il valore e quindi fare clic su ![Salva](/help/search-social-commerce/assets/select.png "Salva") per salvare immediatamente il valore.

        La lunghezza massima è di 100 caratteri e può includere caratteri ASCII e non ASCII.

1. (Facoltativo) Immettere ulteriori dettagli:

   1. Accanto a **[!UICONTROL Additional Details]**, fai clic su ![Apri](/help/search-social-commerce/assets/chevron-up.png "Apri") per espandere i dettagli.

   1. Immetti un valore facoltativo **[!UICONTROL Project Name]** e/o opzionale **[!UICONTROL Description]**.

1. Clic **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Informazioni sulle classificazioni delle etichette](classification-about.md)
>* [Creare una classificazione di etichette](classification-create.md)
>* [Assegnare valori di classificazione ai componenti conto utilizzando i bulksheet](classification-values-assign-bulksheets.md)
>* [Rimuovi i valori di classificazione delle etichette dai componenti dell’account](classification-values-remove.md)
>* [Elimina valori di classificazione delle etichette](classification-values-delete.md)
>* [Eliminare le classificazioni delle etichette](classification-delete.md)
