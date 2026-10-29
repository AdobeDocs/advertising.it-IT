---
title: '[!DNL Yandex] impostazioni parola chiave'
description: Fare riferimento alle impostazioni per le parole chiave [!DNL Yandex].
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
source-wordcount: '227'
ht-degree: 0%
---
# [!DNL Yandex] impostazioni parola chiave

[!DNL Yandex] parole chiave utilizzate sia per le reti di ricerca che per quelle di visualizzazione (contenuto).

## [!UICONTROL Basic Settings]

*Solo nuove parole chiave*

**[!UICONTROL Network]:** La rete di annunci.

**[!UICONTROL Account]:** L&#39;account di rete dell&#39;annuncio.

**[!UICONTROL Campaign]:** La campagna.

**[!UICONTROL Ad Group]:** Il gruppo di annunci.

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Le frasi delle parole chiave, inclusa qualsiasi sintassi di tipo [[!DNL Yandex] match](https://yandex.com/support/direct/keywords/symbols-and-operators.html) per le parole chiave. Ogni parola chiave può avere un massimo di sette parole, escluse le parole non significative.

È possibile immettere o incollare fino a 2.000 parole chiave. Separare più parole chiave con virgole o immetterle su righe separate.

>[!NOTE]
>
>* Se si modifica una parola chiave o un tipo di corrispondenza [!DNL Yandex], la parola chiave esistente verrà eliminata e ne verrà creata una nuova.
>* Ogni gruppo di annunci [!DNL Yandex] può includere un massimo di 200 parole chiave.

**[!UICONTROL Status]:** Lo stato di visualizzazione della parola chiave: *[!UICONTROL Active]* o *[!UICONTROL Paused]*. Il valore predefinito per le nuove parole chiave è *[!UICONTROL Active]*.

## [!UICONTROL Bids]

{{$include /help/_includes/bid-keyword.md}}

## [!UICONTROL Placeholders]

>[!NOTE]
>
>I caratteri speciali vengono codificati automaticamente in UTF-8. Ad esempio, se l&#39;annuncio associato ha un URL di base di `http://www.example.com/{param1}` e il valore a livello di parola chiave di `{param1}` è `shoes/flats.html`, l&#39;annuncio conduce a `http://www.example.com/shoes%2Fflats.html`.

**[!UICONTROL Param1]:** Stringa da utilizzare come valore di sostituzione se l&#39;URL di base contiene la stringa di sostituzione dinamica `{param1}` per annunci e sitelink quando la parola chiave viene utilizzata per visualizzare l&#39;annuncio. La lunghezza massima è di 255 byte.

**[!UICONTROL Param2]:** Stringa da utilizzare come valore di sostituzione se l&#39;URL di base contiene la stringa di sostituzione dinamica `{param2}` per annunci e sitelink quando la parola chiave viene utilizzata per visualizzare l&#39;annuncio. La lunghezza massima è di 255 byte.

>[!MORELIKETHIS]
>
>* [Gestisci parole chiave](keyword-manage.md)
