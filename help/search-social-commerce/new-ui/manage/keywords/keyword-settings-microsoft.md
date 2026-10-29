---
title: '[!DNL Microsoft Advertising] impostazioni parola chiave'
description: Fare riferimento alle impostazioni per le parole chiave [!DNL Microsoft Advertising].
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
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 3bb565d689b65ae66d6ea2094abccdff3c9e891d
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 0%
---
# [!DNL Microsoft Advertising] impostazioni parola chiave

Puoi creare parole chiave per le campagne che utilizzano le reti di ricerca e visualizzazione.

## [!UICONTROL Basic Settings]

*Solo nuove parole chiave*

**[!UICONTROL Network]:** La rete di annunci.

**[!UICONTROL Account]:** L&#39;account di rete dell&#39;annuncio.

**[!UICONTROL Campaign]:** La campagna.

**[!UICONTROL Ad Group]:** Il gruppo di annunci.

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Le parole chiave, incluse eventuali [!DNL Microsoft Advertising] corrispondano alla sintassi e ai segnaposto. La lunghezza massima per parola chiave è di 100 caratteri.

È possibile immettere o incollare fino a 2.000 parole chiave. Separare più parole chiave con virgole o immetterle su righe separate.

>[!NOTE]
>
>* È possibile creare parole chiave negative dalla scheda [!UICONTROL Manage] > [!UICONTROL Keywords] > [!UICONTROL Negatives] e nelle impostazioni del gruppo di annunci e della campagna.
>* La modifica di una parola chiave [!DNL Microsoft Advertising] comporta l&#39;eliminazione della parola chiave esistente e la creazione di una nuova parola chiave con un nuovo ID. Cambiando il tipo di corrispondenza, tuttavia, non elimina la parola chiave esistente.

**[!UICONTROL Status]:** Lo stato di visualizzazione della parola chiave: *[!UICONTROL Active]* o *[!UICONTROL Paused]*. Il valore predefinito per le nuove parole chiave è *[!UICONTROL Active]*.

## [!UICONTROL Bids]

{{$include /help/_includes/bid-keyword.md}}

## [!UICONTROL Placeholders]

**[!UICONTROL Param1]:** La stringa da utilizzare come valore di sostituzione se l&#39;URL di base della parola chiave o il titolo, la descrizione o l&#39;URL di base dell&#39;annuncio contiene [la stringa di sostituzione dinamica `{Param1}`](https://help.bingads.microsoft.com/#apex/3/en/53079/0). La lunghezza massima è di 70 caratteri, ma tieni presente la lunghezza massima degli elementi dell’annuncio in cui lo utilizzi (ad esempio, il titolo 1 e il titolo 2 combinati possono contenere un massimo di 76 caratteri).

**[!UICONTROL Param2]:** La stringa da utilizzare come valore di sostituzione se l&#39;URL di base della parola chiave o il titolo, la descrizione o l&#39;URL di base dell&#39;annuncio contiene [la stringa di sostituzione dinamica `{Param2}`](https://help.bingads.microsoft.com/#apex/3/en/53079/0). La lunghezza massima è di 70 caratteri, ma tieni presente la lunghezza massima degli elementi dell’annuncio in cui lo utilizzi (ad esempio, il titolo 1 e il titolo 2 combinati possono contenere un massimo di 76 caratteri).

## [!UICONTROL URL Options]

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

Questo campo può includere facoltativamente le variabili di sostituzione dinamica `{Param1}` e `{Param2}`.

{{$include /help/_includes/tracking-template-microsoft.md}}

>[!MORELIKETHIS]
>
>* [Gestisci parole chiave](keyword-manage.md)
