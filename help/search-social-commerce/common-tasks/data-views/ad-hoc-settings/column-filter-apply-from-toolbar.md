---
title: Applicare filtri dati dalla barra degli strumenti
description: Scopri come filtrare i dati della pagina dalla barra degli strumenti.
exl-id: fc1dca75-b0e5-48fd-90ee-f09c158e3e8b
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# Applicare filtri dati dalla barra degli strumenti

Puoi applicare a una visualizzazione tutti i filtri che desideri. Tutti i filtri vengono uniti utilizzando l’operatore AND.

1. Nella barra degli strumenti, fai clic su ![Filtro](/help/search-social-commerce/assets/filter.png "Filtro").

1. Nelle impostazioni del filtro eseguire una delle operazioni seguenti:

   * Per aggiungere un filtro, fare clic su ![Aggiungi filtro](/help/search-social-commerce/assets/add.png "Aggiungi filtro") **[!UICONTROL ADD FILTER]** e quindi eseguire le operazioni seguenti:

      1. (Facoltativo) Per filtrare i nomi delle colonne in base alla stringa di testo, immettere la stringa di ricerca nel campo di input **[!UICONTROL ADD FILTER]**.

      1. Selezionare un nome di colonna dal menu colonna.

      1. Definisci il filtro per la colonna:

         * (Filtri senza campi di input) Fare clic su ![Freccia giù](/help/search-social-commerce/assets/arrow-down-expand.png "Freccia giù") accanto al secondo menu, quindi selezionare le caselle di controllo accanto a ogni valore da includere.

         * (Filtri con campi di input) Seleziona un operatore dal secondo menu, quindi inserisci il valore applicabile.

           Ad esempio, se hai selezionato la colonna &quot;[!UICONTROL Clicks]&quot; e desideri restituire solo le righe con più di 100 clic, seleziona *[!UICONTROL greater than]*&quot; e immetti `100` nel campo di input.

           A seconda del tipo di dati, gli operatori disponibili possono includere *[!UICONTROL greater than]*, *[!UICONTROL less than]*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *[!UICONTROL doesn't contain]*, *[!UICONTROL starts with]*, *[!UICONTROL ends with]*, *[!UICONTROL no value]*, *[!UICONTROL has value]*, *[!UICONTROL before]*, *[!UICONTROL after]* o *[!UICONTROL no date].*

           **Nota:** i valori di testo non fanno distinzione tra maiuscole e minuscole. Ad esempio, se filtri per campagne con &quot;prestito&quot; nel nome, i risultati includono &quot;Prestiti al consumo&quot; e &quot;Applicazioni prestito&quot;.

         * ([!UICONTROL Ad Groups], [!UICONTROL Keywords], [!UICONTROL Product Groups], [!UICONTROL Placements] e [!UICONTROL Auto Targets] solo visualizzazioni; facoltativo) Cambia l&#39;impostazione in &quot;[!UICONTROL Include rows with performance data only].&quot;

           **Avviso:** se si deseleziona l&#39;opzione e la visualizzazione include molte entità senza dati sulle prestazioni, la visualizzazione dei dati richiede più tempo.

   * Per modificare un filtro esistente, fare clic sul filtro, modificare la definizione del filtro e quindi fare clic su ![Aggiorna filtro](/help/search-social-commerce/assets/select.png "Aggiorna filtro").

   * Per rimuovere un filtro esistente, fare clic su **[!UICONTROL X]** accanto alla definizione del filtro.

1. Fare clic su **[!UICONTROL Apply]**.
