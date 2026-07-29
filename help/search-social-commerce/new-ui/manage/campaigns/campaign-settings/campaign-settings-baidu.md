---
title: '[!DNL Baidu] impostazioni campagna'
description: Fai riferimento alle impostazioni per  [!DNL Baidu]  campagne.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 3a5c2507f3acb08419e143ba906cf55df2496d0f
workflow-type: tm+mt
source-wordcount: 309
ht-degree: 0%

---

# [!DNL Baidu] impostazioni campagna

## \[Inizio pagina]

**[!UICONTROL Campaign Name]:** Nome di campagna univoco all&#39;interno dell&#39;account.

**[!UICONTROL Status]:** Lo stato di visualizzazione della campagna: *Attivo* o *In pausa*. Il valore predefinito per le nuove campagne pubblicitarie è *Attivo*.

## Scheda [!UICONTROL Basic Settings]

*Solo nuove campagne*

**[!UICONTROL Network]:** La rete di annunci.

**[!UICONTROL Account]:** L&#39;account di rete dell&#39;annuncio.

**[!UICONTROL Campaign Type]:** Dove inserire annunci e quali tipi di annunci può contenere la campagna. L&#39;unica opzione è *Cerca solo rete*.

## Scheda [!UICONTROL Campaign Details]

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

**[!UICONTROL Contains EU Political Ads]:**(Applicabile alle campagne indirizzate a tipi di pubblico nell&#39;Unione europea) Indica se la campagna contiene o meno pubblicità politica in base ai requisiti per gli annunci pubblicati nell&#39;Unione europea ai sensi del Regolamento UE 2024/90: *[!UICONTROL Yes]* o *[!UICONTROL No]*.

## Scheda [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

<!--VERIFY OPTIMIZATION BEHAVIOR -->**[!UICONTROL Bid strategy]:** La strategia di offerta per la campagna:

* *[!UICONTROL Maximize Conversions]:* La rete di annunci, non Search, Social e Commerce, ottimizza le offerte per massimizzare le conversioni. È possibile immettere un valore **[!UICONTROL Target CPA]** (costo per acquisizione). **Nota:** utilizza questa opzione per le campagne nei portfolio con ottimizzazione a livello di campagna. Nei portfolio con ottimizzazione a livello di campagna, Search, Social e Commerce ottimizzano il CPA di Target.

* *[!UICONTROL Maximize Conversion Value]:* La rete di annunci, non Search, Social e Commerce, ottimizza le offerte per massimizzare il valore di conversione. È possibile immettere un valore di **[!UICONTROL Target Return on Ad Spend]** (ROAS) come percentuale. **Nota:** utilizza questa opzione per le campagne nei portfolio con ottimizzazione a livello di campagna. Nei portfolio con ottimizzazione a livello di campagna, Search, Social e Commerce ottimizzano il ROAS di Target.

## Scheda [!UICONTROL Campaign Targeting]

**[!UICONTROL Languages]:** lingua dell&#39;annuncio, che deve corrispondere alla lingua dei siti in cui l&#39;annuncio può essere visualizzato. La rete di annunci determina la lingua di un utente da vari segnali, tra cui la query dell’utente, il paese dell’editore e l’impostazione della lingua dell’utente.

<!-- **[!UICONTROL Location Targets]:** -->

{{$include /help/_includes/location-targets.md}}

## Scheda [!UICONTROL Additional Campaign Information]

### [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Campaign Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Campaign Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-baidu.md}}

### Scheda [!UICONTROL Campaign Tracking]

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
