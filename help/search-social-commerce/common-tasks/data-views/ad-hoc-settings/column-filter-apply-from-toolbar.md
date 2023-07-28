---
title: Applicare filtri dati dalla barra degli strumenti
description: Scopri come filtrare i dati della pagina dalla barra degli strumenti.
exl-id: 922cc148-e6dc-428b-a7f3-1da3780df326
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# Applicare filtri dati dalla barra degli strumenti

Puoi applicare a una visualizzazione tutti i filtri che desideri. Tutti i filtri vengono uniti utilizzando l’operatore AND.

1. Nella barra degli strumenti, fai clic su ![Filtro](/help/search-social-commerce/assets/filter.png "Filtro").

1. Nelle impostazioni del filtro eseguire una delle operazioni seguenti:

   * Per aggiungere un filtro, fai clic su ![Aggiungi filtro](/help/search-social-commerce/assets/add.png "Aggiungi filtro") **[!UICONTROL ADD FILTER]**, quindi eseguire le operazioni seguenti:

      1. (Facoltativo) Per filtrare i nomi delle colonne in base alla stringa di testo, immetti la stringa di ricerca nel campo **[!UICONTROL ADD FILTER]** campo di input.

      1. Selezionare un nome di colonna dal menu colonna.

      1. Definisci il filtro per la colonna:

         * (Filtri senza campi di input) Fai clic su ![Freccia giù](/help/search-social-commerce/assets/arrow-down-expand.png "Freccia giù") accanto al secondo menu, quindi selezionare le caselle di controllo accanto a ogni valore da includere.

         * (Filtri con campi di input) Seleziona un operatore dal secondo menu, quindi inserisci il valore applicabile.

           Ad esempio, se hai selezionato il pulsante &quot;[!UICONTROL Clicks]&quot; e desideri restituire solo le righe con più di 100 clic, quindi seleziona *[!UICONTROL greater than]*&quot; ed entra `100` nel campo di input.

           A seconda del tipo di dati, gli operatori disponibili possono includere *[!UICONTROL greater than]*, *[!UICONTROL less than]*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *[!UICONTROL doesn't contain]*, *[!UICONTROL starts with]*, *[!UICONTROL ends with]*, *[!UICONTROL no value]*, *[!UICONTROL has value]*, *[!UICONTROL before]*, *[!UICONTROL after]*, o *[!UICONTROL no date].*

           **Nota:** I valori di testo non fanno distinzione tra maiuscole e minuscole. Ad esempio, se filtri per campagne con &quot;prestito&quot; nel nome, i risultati includeranno &quot;Prestiti al consumo&quot; e &quot;richieste di prestito&quot;.

         * ([!UICONTROL Ad Groups], [!UICONTROL Keywords], [!UICONTROL Product Groups], [!UICONTROL Placements], e [!UICONTROL Auto Targets] solo visualizzazioni; facoltativo) Cambia l’impostazione in &quot;[!UICONTROL Include rows with performance data only].&quot;

           **Avvertenza:** Se deselezioni l’opzione e la vista include molte entità senza dati sulle prestazioni, la visualizzazione dei dati richiede più tempo.

   * Per modificare un filtro esistente, fare clic sul filtro, modificare la definizione del filtro e quindi fare clic su ![Aggiorna filtro](/help/search-social-commerce/assets/select.png "Aggiorna filtro").

   * Per rimuovere un filtro esistente, fai clic su **[!UICONTROL X]** accanto alla definizione del filtro.

1. Clic **[!UICONTROL Apply]**.
