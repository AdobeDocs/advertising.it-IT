---
title: '[!DNL Google Ads] impostazioni parola chiave'
description: Fare riferimento alle impostazioni per le parole chiave [!DNL Google Ads].
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 3bb565d689b65ae66d6ea2094abccdff3c9e891d
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%
---
# [!DNL Google Ads] impostazioni parola chiave

Puoi creare parole chiave per le campagne che utilizzano le reti di ricerca e visualizzazione.

Consulta la guida di [!DNL Google Ads] per [limiti di parole chiave per account](https://support.google.com/google-ads/answer/6372658).

## [!UICONTROL Basic Settings]

*Solo nuove parole chiave*

**[!UICONTROL Network]:** La rete di annunci.

**[!UICONTROL Account]:** L&#39;account di rete dell&#39;annuncio.

**[!UICONTROL Campaign]:** La campagna.

**[!UICONTROL Ad Group]:** Il gruppo di annunci.

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Le parole chiave, incluse eventuali [!DNL Google Ads], corrispondono alla sintassi per parole chiave e segnaposto. [!DNL Google Ads] account richiedono parole chiave con i seguenti attributi:

* La lunghezza massima per parola chiave è di 80 caratteri e non più di 10 parole.

* La parola chiave può contenere solo lettere, cifre e i seguenti caratteri speciali: spazio `# $ & _ - " [] ' + . / :`

È possibile immettere o incollare fino a 2.000 parole chiave. Separare più parole chiave con virgole o immetterle su righe separate.

>[!NOTE]
>
>* È possibile creare parole chiave negative dalla scheda [!UICONTROL Manage] > [!UICONTROL Keywords] > [!UICONTROL Negatives] e nelle impostazioni del gruppo di annunci e della campagna.
>* Se si modifica una parola chiave o un tipo di corrispondenza [!DNL Google Ads], la parola chiave esistente verrà eliminata e ne verrà creata una nuova.

**[!UICONTROL Status]:** Lo stato di visualizzazione della parola chiave: *[!UICONTROL Active]* o *[!UICONTROL Paused]*. Il valore predefinito per le nuove parole chiave è *[!UICONTROL Active]*.

## [!UICONTROL Bids]

{{$include /help/_includes/bid-keyword.md}}

## [!UICONTROL Placeholders]

**[!UICONTROL Param1]:** Stringa da utilizzare come valore di sostituzione se l&#39;URL di base o il modello di tracciamento contiene [la stringa di sostituzione dinamica `{param1}`](https://support.google.com/google-ads/answer/6305348).

**[!UICONTROL Param2]:** Stringa da utilizzare come valore di sostituzione se l&#39;URL di base o il modello di tracciamento contiene [la stringa di sostituzione dinamica `{param2}`](https://support.google.com/google-ads/answer/6305348).

## [!UICONTROL URL Options]

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

{{$include /help/_includes/base-url-google-note.md}}

{{$include /help/_includes/tracking-template-google.md}}

>[!MORELIKETHIS]
>
>* [Gestisci parole chiave](keyword-manage.md)
