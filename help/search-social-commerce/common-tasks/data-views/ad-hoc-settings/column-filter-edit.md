---
title: Modificare i filtri di colonna
description: Scopri come modificare i filtri di colonna.
exl-id: 68f816ea-cde2-4df0-b46c-f47fa20a2727
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 0%

---

# Modificare i filtri di colonna

## Modificare un set di filtri

1. Fai clic su ![Filtro](/help/search-social-commerce/assets/filter.png "Filtro") nella barra degli strumenti.

1. Nelle impostazioni del filtro eseguire una delle operazioni seguenti:

   * Per aggiungere un filtro, fare clic su ![Aggiungi filtro](/help/search-social-commerce/assets/add.png "Aggiungi filtro") **[!UICONTROL ADD FILTER]** e quindi eseguire le operazioni seguenti:

      1. (Facoltativo) Per filtrare i nomi delle colonne in base alla stringa di testo, immettere la stringa di ricerca nel campo di input **[!UICONTROL ADD FILTER]**.

      1. Selezionare un nome di colonna dal menu colonna.

      1. Definisci il filtro per la colonna:

         * (Filtri senza campi di input) Fare clic su ![Freccia giù](/help/search-social-commerce/assets/arrow-down-expand.png "Freccia giù") accanto al secondo menu, selezionare le caselle di controllo accanto a ogni valore da includere e quindi fare clic su ![Aggiorna filtro](/help/search-social-commerce/assets/select.png "Aggiorna filtro").

         * (Filtri con campi di input) Selezionare un operatore dal secondo menu, immettere il valore applicabile e quindi fare clic su ![Aggiorna filtro](/help/search-social-commerce/assets/select.png "Aggiorna filtro").

           Ad esempio, se hai selezionato la colonna &quot;[!UICONTROL Clicks]&quot; e desideri restituire solo le righe con più di 100 clic, seleziona *[!UICONTROL greater than]*&quot; e immetti `100` nel campo di input.

           A seconda del tipo di dati, gli operatori disponibili possono includere *[!UICONTROL greater than]*, *[!UICONTROL less than]*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *[!UICONTROL doesn't contain]*, *[!UICONTROL starts with]*, *[!UICONTROL ends with]*, *[!UICONTROL no value]* o *[!UICONTROL has value]*, *[!UICONTROL before]*, *[!UICONTROL after]* o *[!UICONTROL no date].*

           **Nota:** i valori di testo non fanno distinzione tra maiuscole e minuscole. Ad esempio, se cerchi campagne con &quot;prestito&quot; nel nome, i risultati includono &quot;Prestiti al consumo&quot; e &quot;richieste di prestito&quot;.

   * Per modificare un filtro esistente, fare clic sul filtro, modificare la definizione del filtro e quindi fare clic su ![Aggiorna filtro](/help/search-social-commerce/assets/select.png "Aggiorna filtro").

   * Per rimuovere un filtro esistente, fare clic su **[!UICONTROL X]** accanto alla definizione del filtro.

1. ([!UICONTROL Keywords] solo visualizzazione; facoltativo) Selezionare o deselezionare l&#39;impostazione su &quot;[!UICONTROL Include rows with no performance data]&quot;.&quot;

   >[!WARNING]
   >
   >Selezionando questa opzione si aumenta il tempo di caricamento della pagina.

1. Fare clic su **[!UICONTROL Apply]**.

## Modificare un singolo filtro

1. (Se necessario) Nel set di filtri sopra la tabella di dati, fare clic su ![Altro](/help/search-social-commerce/assets/more-filters.png "Altro") per espandere il set di filtri.

1. Sopra la tabella dati, fai clic sulla definizione del filtro.

1. Modifica i filtri da applicare:

   1. (Facoltativo) Modifica il nome della colonna dal menu colonna.

   1. (Facoltativo) Ridefinisci il filtro nella colonna:

      * (Filtri senza campi di input) Fare clic su ![Freccia giù](/help/search-social-commerce/assets/arrow-down-expand.png "Freccia giù") accanto al secondo menu, selezionare le caselle di controllo accanto a ogni valore da includere e quindi fare clic su ![Aggiorna filtro](/help/search-social-commerce/assets/select.png "Aggiorna filtro").

      * (Filtri con campi di input) Selezionare un operatore dal secondo menu, immettere il valore applicabile e quindi fare clic su ![Aggiorna filtro](/help/search-social-commerce/assets/select.png "Aggiorna filtro").

        Ad esempio, se hai selezionato la colonna &quot;[!UICONTROL Clicks]&quot; e desideri restituire solo le righe con più di 100 clic, seleziona *[!UICONTROL greater than]*&quot; e immetti `100` nel campo di input

        A seconda del tipo di dati, gli operatori disponibili possono includere *[!UICONTROL greater than]*, *minore di*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *non contiene* o *inizia con.*

        **Nota:** i valori di testo non fanno distinzione tra maiuscole e minuscole. Ad esempio, se cerchi campagne con &quot;prestito&quot; nel nome, i risultati includono &quot;Prestiti al consumo&quot; e &quot;richieste di prestito&quot;.
