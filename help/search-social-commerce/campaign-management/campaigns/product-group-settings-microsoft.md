---
title: '[!DNL Microsoft® Advertising] impostazioni gruppo di prodotti'
description: Fai riferimento alle impostazioni per [!DNL Microsoft® Advertising] gruppi di prodotti.
exl-id: a34511ef-f5bc-4d93-a56e-90348f670ad6
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---

# [!DNL Microsoft® Advertising] impostazioni gruppo di prodotti

## Gruppi di prodotti &quot;Tutti i prodotti&quot;

**[!UICONTROL Condition]:** (Sola lettura) Tutti i prodotti

**[!UICONTROL Bid]:** (Solo per gruppi di prodotti inclusi) Il costo massimo per clic (CPC), che è l’importo più alto da pagare per un clic dell’annuncio. Questo valore viene utilizzato solo per le unità senza gruppi di prodotti secondari e viene utilizzato al posto del valore a livello di gruppo di annunci.

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

Questo modello sostituisce i modelli di livello superiore e viene utilizzato solo per le unità senza gruppi di prodotti secondari.

## Tutti gli altri gruppi di prodotti

**[!UICONTROL Condition/Value]:** (Sola lettura per i gruppi di prodotti esistenti) Le dimensioni prodotto di cui eseguire il targeting. Per i nuovi gruppi di prodotti, immetti la dimensione in base alla quale eseguire il targeting dei prodotti e l’attributo idoneo per la categoria di informazioni selezionata (ad esempio &quot;Acme&quot; quando esegui il targeting per marchio o &quot;Nuovo&quot; quando esegui il targeting per condizione).

Dopo aver creato un gruppo di prodotti per specifiche dimensioni di prodotto (ovvero, non &quot;Tutti i prodotti&quot;), in Ricerca, Social e Commerce viene automaticamente creato un gruppo di prodotti per &quot;Tutto il resto&quot;.

Per un elenco delle dimensioni prodotto disponibili, vedi &quot;[Filtri di prodotti per campagne acquisti](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md).&quot; L’elenco delle dimensioni può essere limitato in base al valore della campagna [!UICONTROL Inventory Filter] impostazione.

**[!UICONTROL Excluded]:** (Facoltativo per i nuovi gruppi di prodotti; sola lettura per i gruppi di prodotti esistenti) Esclude le offerte sugli annunci per i prodotti corrispondenti.

**[!UICONTROL Bid]:** (Solo per gruppi di prodotti inclusi) Il costo massimo per clic (CPC), che è l’importo più alto da pagare per un clic dell’annuncio. Questo valore viene utilizzato solo per le unità senza gruppi di prodotti secondari e viene utilizzato al posto del valore a livello di gruppo di annunci.

<!-- **[!UICONTROL Tracking Template]:** -->

<!-- ExL can't handle the same include twice in the same file, so using a snippet for the second occurrence.

{{$include /help/_includes/tracking-template-microsoft.md}}
-->

{{tracking-template-microsoft}}

Questo modello sostituisce i modelli di livello superiore e viene utilizzato solo per le unità senza gruppi di prodotti secondari.

>[!MORELIKETHIS]
>
>* [Informazioni sui gruppi di prodotti di acquisto](product-group-about.md)
>* [Gestire i gruppi di prodotti](product-group-manage.md)
>* [Filtri di prodotti per campagne acquisti](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md)
>* [Implementare [!DNL Microsoft® Advertising] campagne di acquisto](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md)
