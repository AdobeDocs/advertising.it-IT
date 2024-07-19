---
title: Applicare filtri dati da un menu di intestazione di colonna
description: Scopri come filtrare i dati della pagina da un menu di intestazione di colonna.
exl-id: 508f254a-d859-4155-9bbd-84e0442f01d5
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%

---

# Applicare un filtro dati da un menu di intestazione di colonna

Puoi applicare a una colonna tutti i filtri che desideri, uno alla volta. Tutti i filtri vengono uniti utilizzando l’operatore AND. Per aggiungere più di un filtro alla volta utilizzando tutte le metriche disponibili, vedere &quot;[Applicare filtri dati dalla barra degli strumenti](column-filter-apply-from-toolbar.md).&quot;

1. Sul lato destro dell&#39;intestazione di colonna fare clic su ![Freccia giù](/help/search-social-commerce/assets/arrow-down-dropdown.png "Freccia giù") e quindi su **[!UICONTROL Add Filter]**.

1. Definisci il filtro per la colonna:

   * (Filtri senza campi di input) Selezionare le caselle di controllo accanto a ogni valore da includere, quindi fare clic su ![Aggiorna filtro](/help/search-social-commerce/assets/select.png "Aggiorna filtro").

   * (Filtri con campi di input) Selezionare un operatore dal secondo menu, immettere il valore applicabile e quindi fare clic su ![Aggiorna filtro](/help/search-social-commerce/assets/select.png "Aggiorna filtro").

     Ad esempio, se hai selezionato la colonna &quot;[!UICONTROL Clicks]&quot; e desideri restituire solo righe con più di 100 clic, seleziona *[!UICONTROL greater than]*&quot; e immetti `100` nel campo di input A seconda del tipo di dati, gli operatori disponibili possono includere *[!UICONTROL greater than]*, *[!UICONTROL less than]*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *[!UICONTROL doesn't contain]*, *[!UICONTROL starts with]*, *[!UICONTROL ends with]*, *[!UICONTROL no value]*, *[!UICONTROL has value]*, *[!UICONTROL before]*, *[!UICONTROL after]* o *[!UICONTROL no date].*

     >[!NOTE]
     >
     >* I valori di testo non fanno distinzione tra maiuscole e minuscole. Ad esempio, se filtri per campagne con &quot;prestito&quot; nel nome, i risultati includono &quot;Prestiti al consumo&quot; e &quot;Applicazioni prestito&quot;.
     >* È possibile applicare un solo filtro numerico semplice (ad esempio [!UICONTROL Impressions] \> 100) per colonna.
