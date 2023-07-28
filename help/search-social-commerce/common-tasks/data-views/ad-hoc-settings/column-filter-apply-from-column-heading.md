---
title: Applicare filtri dati da un menu di intestazione di colonna
description: Scopri come filtrare i dati della pagina da un menu di intestazione di colonna.
exl-id: ad745599-fd98-4f34-b181-085070adb685
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---

# Applicare un filtro dati da un menu di intestazione di colonna

Puoi applicare a una colonna tutti i filtri che desideri, uno alla volta. Tutti i filtri vengono uniti utilizzando l’operatore AND. Per aggiungere più di un filtro alla volta utilizzando tutte le metriche disponibili, vedi &quot;[Applicare filtri dati dalla barra degli strumenti](column-filter-apply-from-toolbar.md).&quot;

1. A destra dell&#39;intestazione di colonna fare clic su ![Freccia giù](/help/search-social-commerce/assets/arrow-down-dropdown.png "Freccia giù")e quindi fare clic su **[!UICONTROL Add Filter]**.

1. Definisci il filtro per la colonna:

   * (Filtri senza campi di input) Selezionare le caselle di controllo accanto a ogni valore da includere e quindi fare clic su ![Aggiorna filtro](/help/search-social-commerce/assets/select.png "Aggiorna filtro").

   * (Filtri con campi di input) Seleziona un operatore dal secondo menu, immetti il valore applicabile e quindi fai clic su ![Aggiorna filtro](/help/search-social-commerce/assets/select.png "Aggiorna filtro").

     Ad esempio, se hai selezionato il pulsante &quot;[!UICONTROL Clicks]&quot; e desideri restituire solo le righe con più di 100 clic, quindi seleziona *[!UICONTROL greater than]*&quot; ed entra `100` nel campo di input A seconda del tipo di dati, gli operatori disponibili possono includere *[!UICONTROL greater than]*, *[!UICONTROL less than]*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *[!UICONTROL doesn't contain]*, *[!UICONTROL starts with]*, *[!UICONTROL ends with]*, *[!UICONTROL no value]*, *[!UICONTROL has value]*, *[!UICONTROL before]*, *[!UICONTROL after]*, o *[!UICONTROL no date].*

     >[!NOTE]
     >
     >* I valori di testo non fanno distinzione tra maiuscole e minuscole. Ad esempio, se filtri per campagne con &quot;prestito&quot; nel nome, i risultati includono &quot;Prestiti al consumo&quot; e &quot;Applicazioni prestito&quot;.
     >* Puoi applicare un solo filtro numerico semplice (ad esempio [!UICONTROL Impressions] 100) per colonna.
