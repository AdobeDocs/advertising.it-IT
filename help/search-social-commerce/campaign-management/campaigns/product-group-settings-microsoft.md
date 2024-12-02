---
title: Impostazioni gruppo di prodotti [!DNL Microsoft Advertising]
description: Fai riferimento alle impostazioni per  [!DNL Microsoft Advertising] gruppi di prodotti acquisti.
exl-id: ea3a4137-1396-430f-9d6c-8e1e1f1f52c2
feature: Search Campaign Management
source-git-commit: 7e4d2aa502f26b480a5fd76d68411586c24f68b2
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---

# Impostazioni gruppo di prodotti [!DNL Microsoft Advertising]

## Gruppi di prodotti &quot;Tutti i prodotti&quot;

**[!UICONTROL Condition]:** (sola lettura) tutti i prodotti

**[!UICONTROL Bid]:** (solo per gruppi di prodotti inclusi) Il costo massimo per clic (CPC), che è l&#39;importo più alto da pagare per un clic dell&#39;annuncio. Questo valore viene utilizzato solo per le unità senza gruppi di prodotti secondari e viene utilizzato al posto del valore a livello di gruppo di annunci.

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

Questo modello sostituisce i modelli di livello superiore e viene utilizzato solo per le unità senza gruppi di prodotti secondari.

## Tutti gli altri gruppi di prodotti

**[!UICONTROL Condition/Value]:** (sola lettura per gruppi di prodotti esistenti) dimensioni prodotto di destinazione. Per i nuovi gruppi di prodotti, immetti la dimensione in base alla quale eseguire il targeting dei prodotti e l’attributo idoneo per la categoria di informazioni selezionata (ad esempio &quot;Acme&quot; quando esegui il targeting per marchio o &quot;Nuovo&quot; quando esegui il targeting per condizione).

Dopo aver creato un gruppo di prodotti per specifiche dimensioni di prodotto (ovvero, non &quot;Tutti i prodotti&quot;), in Ricerca, Social e Commerce viene automaticamente creato un gruppo di prodotti per &quot;Tutto il resto&quot;.

Per un elenco delle dimensioni di prodotto disponibili, consulta &quot;[Filtri di prodotto per campagne acquisti](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md).&quot; L&#39;elenco delle dimensioni potrebbe essere limitato in base all&#39;impostazione [!UICONTROL Inventory Filter] della campagna.

**[!UICONTROL Excluded]:** (facoltativo per i nuovi gruppi di prodotti; sola lettura per i gruppi di prodotti esistenti) Esclude le offerte sugli annunci per i prodotti corrispondenti.

**[!UICONTROL Bid]:** (solo per gruppi di prodotti inclusi) Il costo massimo per clic (CPC), che è l&#39;importo più alto da pagare per un clic dell&#39;annuncio. Questo valore viene utilizzato solo per le unità senza gruppi di prodotti secondari e viene utilizzato al posto del valore a livello di gruppo di annunci.

<!-- **[!UICONTROL Tracking Template]:** -->

<!-- ExL can't handle the same include twice in the same file, so using a snippet for the second occurrence.

{{$include /help/_includes/tracking-template-microsoft.md}}
-->

{{tracking-template-microsoft}}

Questo modello sostituisce i modelli di livello superiore e viene utilizzato solo per le unità senza gruppi di prodotti secondari.

>[!MORELIKETHIS]
>
>* [Informazioni sull&#39;acquisto di gruppi di prodotti](product-group-about.md)
>* [Gestione dei gruppi di prodotti](product-group-manage.md)
>* [Filtri prodotti campagna acquisti](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md)
>* [Implementa [!DNL Microsoft Advertising] campagne acquisti](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)
