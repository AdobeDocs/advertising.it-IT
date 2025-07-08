---
title: Applicare filtri dati da un menu di intestazione di colonna
description: Scopri come filtrare i dati della pagina da un menu di intestazione di colonna.
exl-id: 508f254a-d859-4155-9bbd-84e0442f01d5
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: a438e0c24f9ff83941710f890c55c94b74d4d0f3
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---

# Applicare un filtro dati da un menu di intestazione di colonna

<!-- The same in new UI and legacy CM views -->

<!-- Doesn't include instructions for legacy Portfolios or Reports views -->

Puoi applicare a una colonna tutti i filtri che desideri, uno alla volta.<!-- True only for entity names, I think: All filters are joined using the AND operator. --> Per aggiungere più di un filtro alla volta utilizzando tutte le metriche disponibili, vedere &quot;[Applicare filtri dati dalla barra degli strumenti](column-filter-apply-from-toolbar.md).&quot;

1. Sul lato destro dell&#39;intestazione di colonna fare clic su ![Freccia giù](/help/search-social-commerce/assets/arrow-down-dropdown.png "Freccia giù") e quindi su **[!UICONTROL Add Filter]**.

1. Definisci il filtro per la colonna:

   * (Filtri senza campi di input) Selezionare le caselle di controllo accanto a ogni valore da includere, quindi fare clic su ![Aggiorna filtro](/help/search-social-commerce/assets/select.png "Aggiungi").

   * (Filtri con campi di input) Seleziona un operatore dal secondo menu, immetti il valore applicabile, quindi fai clic su ![Aggiorna filtro](/help/search-social-commerce/assets/select.png "Aggiungi").

     Ad esempio, se hai selezionato la colonna &quot;[!UICONTROL Clicks]&quot; e desideri restituire solo righe con più di 100 clic, seleziona *[!UICONTROL greater than]*&quot; e immetti `100` nel campo di input A seconda del tipo di dati, gli operatori disponibili possono includere *[!UICONTROL greater than]*, *[!UICONTROL less than]*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *[!UICONTROL doesn't contain]*, *[!UICONTROL starts with]*, *[!UICONTROL ends with]*, *[!UICONTROL no value]*, *[!UICONTROL has value]*, *[!UICONTROL before]*, *[!UICONTROL after]* o *[!UICONTROL no date].*

     >[!NOTE]
     >
     >* I valori di testo non fanno distinzione tra maiuscole e minuscole. Ad esempio, se filtri per campagne con &quot;prestito&quot; nel nome, i risultati includono &quot;Prestiti al consumo&quot; e &quot;Applicazioni prestito&quot;.
     >* È possibile applicare un solo filtro numerico semplice (ad esempio [!UICONTROL Impressions] \> 100) per colonna.

>[!MORELIKETHIS]
>
>* [Applica filtri dati dalla barra degli strumenti](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md)
>* [Modifica filtri colonne](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-edit.md)
>* [Rimuovere un filtro colonna]&#x200B;(/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/
