---
title: '[!DNL Yandex] impostazioni campagna'
description: Fai riferimento alle impostazioni per  [!DNL Yandex]  campagne.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: d45eb490f9dbb7da89bd1270582e5548b70cbd31
workflow-type: tm+mt
source-wordcount: 252
ht-degree: 0%

---

# [!DNL Yandex] impostazioni campagna

## \[Inizio pagina]

**[!UICONTROL Campaign Name]:** Nome di campagna univoco all&#39;interno dell&#39;account.

**[!UICONTROL Status]:** Lo stato di visualizzazione della campagna: *Attivo* o *In pausa*. Il valore predefinito per le nuove campagne pubblicitarie è *Attivo*.

## Scheda [!UICONTROL Basic Settings]

*Solo nuove campagne*

**[!UICONTROL Network]:** La rete di annunci.

**[!UICONTROL Account]:** L&#39;account di rete dell&#39;annuncio.

**[!UICONTROL Campaign Type]:** Dove inserire gli annunci:

* *[!UICONTROL Search Network Only]:* visualizza annunci di testo nella rete di ricerca. È necessario specificare le parole chiave per ogni gruppo di annunci.

* *[!UICONTROL Search and Display Network]:* Visualizza annunci di testo nella rete di ricerca e in [!DNL Yandex Advertising Network]. Per gli annunci di ricerca, è necessario specificare le parole chiave di ricerca per ciascun gruppo di annunci. Per gli annunci display, è necessario specificare le parole chiave per i siti Web sui quali si desidera pubblicizzare per ogni gruppo di annunci.

* *[!UICONTROL Display Network Only]:* Visualizza annunci di testo in [!DNL Yandex Advertising Network]. Per ogni gruppo di annunci, è necessario specificare le parole chiave per i siti Web sui quali si desidera pubblicizzare.

## Scheda [!UICONTROL Campaign Details]

<!-- **[!UICONTROL Start date]:** -->

{{$include /help/_includes/start-date.md}}

## Scheda [!UICONTROL Budget Options]

**[!UICONTROL Budget]:** Il budget, ovvero l&#39;importo che si desidera spendere giornalmente (in media) o durante la durata della campagna, a seconda del tipo di budget dell&#39;account. Il budget minimo è di 300, 10 o 10 dollari americani.

**Note:**

* Le nuove campagne hanno la strategia di gestione delle offerte &quot;Posizione più elevata disponibile&quot;.

* A seconda delle condizioni di ricerca, se assegni questa campagna a un portfolio configurato per consentire l’adeguamento automatico dei limiti di budget della campagna, puoi spendere effettivamente più o meno del budget specificato per un dato giorno, mese o durata.

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

## Scheda [!UICONTROL Additional Campaign Information]

### [!UICONTROL Campaign Tracking]

<!-- **[!UICONTROL Override Account Tracking]:** -->

<!-- **[!UICONTROL Override Account Tracking]:** -->

{{$include /help/_includes/override-account-tracking.md}}

<!-- **[!UICONTROL Tracking Type]:** -->

{{$include /help/_includes/tracking-type.md}}

<!-- **[!UICONTROL Redirect Type]:** -->

{{$include /help/_includes/redirect-type.md}}

**[!UICONTROL Tracking Level]:** (solo per [!UICONTROL EF Redirect]; sola lettura) Livello al quale è necessario tenere traccia di clic e ricavi. Solo *[!UICONTROL Creative]* è disponibile per [!DNL Yandex]. I dati vengono tracciati solo a livello di annuncio (creativo).

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
