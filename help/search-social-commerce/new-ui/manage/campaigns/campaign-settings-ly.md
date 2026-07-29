---
title: '[!DNL LY Ads] impostazioni campagna'
description: Fai riferimento alle impostazioni per  [!DNL LY Ads]  campagne.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: d45eb490f9dbb7da89bd1270582e5548b70cbd31
workflow-type: tm+mt
source-wordcount: 190
ht-degree: 0%

---

# [!DNL LY Ads] impostazioni campagna

## \[Inizio pagina]

**[!UICONTROL Campaign Name]:** Nome di campagna univoco all&#39;interno dell&#39;account.

**[!UICONTROL Status]:** Lo stato di visualizzazione della campagna: *Attivo* o *In pausa*. Il valore predefinito per le nuove campagne pubblicitarie è *Attivo*.

## Scheda [!UICONTROL Basic Settings]

*Solo nuove campagne*

**[!UICONTROL Network]:** La rete di annunci.

**[!UICONTROL Account]:** L&#39;account di rete dell&#39;annuncio.

**[!UICONTROL Campaign Type]:** Dove inserire annunci: l&#39;unica opzione è *[!UICONTROL Search Network Only]* per visualizzare annunci di testo nella rete di ricerca.

## Scheda [!UICONTROL Campaign Details]

<!-- **[!UICONTROL Start date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End date]:** -->

{{$include /help/_includes/end-date.md}}

## [!UICONTROL Budget Options]

**[!UICONTROL Budget]:** Il budget, ovvero l&#39;importo che si desidera spendere in media ogni giorno. Il budget minimo giornaliero è di 100 JPY.

Se si assegna questa campagna a un portfolio per il quale i limiti di budget delle campagne vengono adeguati automaticamente, a seconda delle condizioni di ricerca, è possibile spendere effettivamente più o meno del budget specificato in un dato periodo.

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

## [!UICONTROL Campaign Targeting]

<!-- **[!UICONTROL Location Targets]:** -->

{{$include /help/_includes/location-targets.md}}

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-yahoo-japan.md}}

## Scheda [!UICONTROL Additional Campaign Information]

### [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Campaign Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Campaign Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-yahoo-japan.md}}

### [!UICONTROL Campaign Tracking]

<!-- **[!UICONTROL Override Account Tracking]:** -->

{{$include /help/_includes/override-account-tracking.md}}

<!-- **[!UICONTROL Tracking Type]:** -->

{{$include /help/_includes/tracking-type.md}}

<!-- **[!UICONTROL Redirect Type]:** -->

{{$include /help/_includes/redirect-type.md}}

**[!UICONTROL Tracking Level]:** (solo per [!UICONTROL EF Redirect]) Il livello a cui devono essere tracciati i clic e i ricavi aggiungendo un reindirizzamento (se pertinente) e aggiungendo parametri agli URL rilevanti:

* *[!UICONTROL Keyword]:* Per tenere traccia dei dati solo a livello di parola chiave.

* *[!UICONTROL Creative]:* Per tenere traccia dei dati solo a livello di annuncio (creativo).

* *[!UICONTROL Creative and Keyword]:* Per tenere traccia dei dati a livello di annuncio (creativo) e di parola chiave.

**[!UICONTROL Enable conversion reporting in Adobe Analytics]:** aggiunge un parametro URL agli annunci nell&#39;account o nella campagna per il tracciamento delle conversioni.

<!-- **[!UICONTROL Encode Base URL]:** -->

{{$include /help/_includes/encode-base-url.md}}

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

<!--

Not there as of 7/22 -- what's going on here? If we're removing it, then I need to update many references throughout the whole doc:

[               **[!UICONTROL Auto Upload]:**      ]

{{$include /help/_includes/auto-upload.md}}

-->

>[!MORELIKETHIS]
>
>* [Gestisci campagne](/help/search-social-commerce/new-ui/manage/campaigns/campaign-manage.md)
