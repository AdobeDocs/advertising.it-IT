---
title: "[!DNL Microsoft® Ads] impostazioni dei modelli di annunci commerciali per i feed inventario"
description: Fai riferimento alle impostazioni per [!DNL Microsoft® Ads] modelli di annunci commerciali per i feed di inventario.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '507'
ht-degree: 0%

---

# [!DNL Microsoft® Ads] impostazioni del modello di annuncio acquisti per i feed inventario

Utilizza i modelli di annunci di acquisto per configurare gli annunci di acquisto.

>[!NOTE]
>
>* I seguenti caratteri sono riservati per la designazione di nomi di colonna e nomi di modificatori nel modello e pertanto non sono consentiti come testo in tutti i campi attributo:  `[ ] < > `



## \[Sopra tutte le schede\]

<!-- **Template Name:** -->

{{$include /help/_includes/inventory-feed-template-name.md}}

<!-- **Status:** -->

{{$include /help/_includes/inventory-feed-template-status.md}}

<!-- **Account:** -->

{{$include /help/_includes/inventory-feed-template-account.md}}

## \[Pannello sinistro\]

<!-- **[!UICONTROL Feed &amp; Columns]:** -->

{{$include /help/_includes/inventory-feed-template-feed-and-columns.md}}

<!-- **[!UICONTROL Modifiers]:** -->

{{$include /help/_includes/inventory-feed-template-modifiers.md}}

## [!UICONTROL Campaigns]

<!-- **[!UICONTROL Campaign]:** -->

{{$include /help/_includes/inventory-feed-template-campaign.md}}

<!-- **[!UICONTROL Campaign Map Only]:** -->

{{$include /help/_includes/inventory-feed-template-shopping-campaign-map-only.md}}

<!-- **[!UICONTROL Campaign Map Method]:** -->

{{$include /help/_includes/inventory-feed-template-shopping-campaign-map-method.md}}

**[!UICONTROL Campaign Tracking Template]:** (Facoltativo per i modelli per i file di feed client) Il modello di tracciamento a livello di campagna, che specifica tutti i reindirizzamenti del dominio di destinazione e i parametri di tracciamento e incorpora l’URL finale in un parametro. Questo valore sovrascrive l’impostazione a livello di account, ma i modelli di tracciamento a livelli più granulari (con la parola chiave come più granulare) sovrascrivono questo valore.

* Ad Adobe, il tracciamento della conversione di Advertising, applicato quando le impostazioni della campagna includono &quot;[!UICONTROL EF Redirect]&quot; e &quot;[!UICONTROL Auto Upload],&quot; eseguire una delle operazioni seguenti&quot;:

   * (Consigliato) Utilizza il [formato del modello di tracciamento per le campagne di acquisto Microsoft®](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md). Se l’intero account è dedicato agli annunci commerciali, puoi invece definire un modello di tracciamento a livello di account.

   * Se invece includi un valore per ciascun prodotto nel feed utilizzando il comando &quot;[!DNL bingads_redirect]&quot; (utilizzando la [formato corretto](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md)), quindi inserisci il parametro `{lpurl}`. Facoltativamente, puoi aggiungere reindirizzamenti di terze parti e il tracciamento al `{lpurl}` parametro.

* Per reindirizzamenti e tracciamento di terze parti, inserisci un valore.

<!-- **[!UICONTROL Campaign Final URL Suffix]:** -->

{{$include /help/_includes/final-url-suffix.md}}

**[!UICONTROL Merchant ID]:** ID cliente dell’account esercente i cui prodotti vengono utilizzati per la campagna.

**[!UICONTROL Sales Country]:** Il paese in cui vengono venduti i prodotti della campagna. Poiché i prodotti sono associati ai paesi di destinazione, questa impostazione determina quali prodotti vengono pubblicizzati nella campagna.

<!-- **[!UICONTROL Stock Level]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-stock-level.md}}

<!-- **[!UICONTROL This column has non-numeric values]:** -->

{{$include /help/_includes/inventory-feed-template-nonnumeric-values.md}}

### [!UICONTROL Campaign Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-campaign-negative-keywords.md}}

### [!UICONTROL Manage Settings for NEW Campaigns]

<!-- Flag/check box **[!UICONTROL Manage Settings for NEW Campaigns]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-manage-settings-new-campaigns.md}}

<!-- **[!UICONTROL Initial Budget]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-initial-budget.md}}

**[!UICONTROL Campaign Priority]:** La priorità con cui viene utilizzata la campagna quando più campagne pubblicizzano lo stesso prodotto: *[!UICONTROL Low]* (impostazione predefinita per le nuove campagne), *[!UICONTROL Medium]*, o *[!UICONTROL High]*. Se lo stesso prodotto è incluso in più campagne, il network pubblicitario utilizza per prima cosa la priorità della campagna per determinare quale campagna (e l’offerta associata) è idonea per l’asta degli annunci. Se tutte le campagne hanno la stessa priorità, la campagna con l’offerta più elevata è idonea.

<!-- **[!UICONTROL Locations]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-locations.md}}

## [!UICONTROL Ad Groups]

<!-- **[!UICONTROL Ad Group]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group.md}}

<!-- **[!UICONTROL Map Only]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-only.md}}

<!-- **[!UICONTROL Map Method]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-method.md }}

**[!UICONTROL Ad Group Tracking Template]:** (Facoltativo) Un modello di tracciamento a livello di gruppo di annunci, che specifica tutti i reindirizzamenti e i parametri di tracciamento del dominio di destinazione finale e incorpora l’URL finale in un parametro. Questo valore sostituisce le impostazioni a livello di account e di campagna, ma i modelli di tracciamento a livelli più granulari sostituiscono questo valore.

Ad Adobe, non è necessario immettere un valore nel tracciamento delle conversioni di Advertising. Il valore a livello di campagna è sufficiente.

Per reindirizzamenti e tracciamento di terze parti, inserisci un valore.

### [!UICONTROL Ad Group Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-ad-group-negative-keywords.md}}

### [!UICONTROL Manage Settings for NEW Ad Groups]

<!-- Flag/check box **[!UICONTROL Manage Settings for NEW Ad Groups]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-manage-settings-new-ad-groups.md}}

<!-- **[!UICONTROL Languages]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-language-microsoft.md}}

## [!UICONTROL Product Groups]

**[!UICONTROL Tier 1]:** Il gruppo di prodotti predefinito completo, &quot;[!UICONTROL All products].&quot; Non puoi eliminare questo gruppo di prodotti principale, ma viene eliminato automaticamente quando tutti i livelli inferiori non sono presenti nel feed.

<!-- **[!UICONTROL Tier 2 - Tier 8]:** -->

{{$include /help/_includes/inventory-feed-template-tier2-8.md}}

<!-- **[!UICONTROL Row Level Value]:** -->

{{$include /help/_includes/inventory-feed-template-row-level-value.md}}

**[!UICONTROL Tracking Template]:** (Unità senza gruppi di prodotti secondari; facoltativo) Il modello di tracciamento per il gruppo di prodotti, che specifica tutti i reindirizzamenti del dominio di destinazione e i parametri di tracciamento e incorpora l’URL finale in un parametro ValueTrack. Questo modello sostituisce i modelli di livello superiore.

Ad Adobe, non è necessario immettere un valore nel tracciamento delle conversioni di Advertising. Il valore a livello di campagna è sufficiente.

Per reindirizzamenti e tracciamento di terze parti, inserisci un valore.

**[!UICONTROL Initial Bid]:** L’offerta iniziale per ogni annuncio.

## [!UICONTROL Feed Filters]

<!-- **\[Feed Filter\]:** -->

{{$include /help/_includes/inventory-feed-template-feed-filter.md}}

## [!UICONTROL Label Classifications]

<!-- **\[Component\] [!UICONTROL Label Classifications] &gt; `[Label Classification and Value`]:** -->

{{$include /help/_includes/inventory-feed-template-label-classifications.md}}

>[!MORELIKETHIS]
>
>* [Informazioni sull’automazione della gestione degli annunci tramite i feed di inventario](../inventory-feeds-about.md)
>* [Flusso di lavoro per la gestione dei dati della campagna tramite i feed di inventario](../inventory-feeds-workflow.md)
>* [Gestione dei modificatori](../modifiers-manage.md)
>* [Gestione dei file di feed dati di inventario](/help/search-social-commerce/campaign-management/inventory-feeds/feed-files-manage.md)
>* [Propagazione dei dati di feed tramite modelli](../feed-data-propagate.md)
>* [Pubblicare i dati della campagna dai feed di inventario alle reti di annunci](../propagated-data-post.md)

