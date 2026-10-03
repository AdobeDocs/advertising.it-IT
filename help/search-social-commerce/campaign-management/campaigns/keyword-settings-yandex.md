---
title: '[!DNL Yandex] impostazioni parola chiave'
description: Fare riferimento alle impostazioni per le parole chiave [!DNL Yandex].
exl-id: 973be0df-9b3c-4f33-b48b-ef1db4ab35da
feature: Search Campaign Management
TQID: 'https://experienceleague.adobe.com/-PRiQ9myH0XNYF8pc2OVBuLOK-8BpxzqruOP2hzPW0I'
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
source-git-commit: 6d95caf72d11c404d866e8d091e1ffa89814ae73
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%
---
# [!DNL Yandex] impostazioni parola chiave

Le parole chiave Yandex vengono utilizzate sia per le reti di ricerca che per quelle di visualizzazione (contenuto).

<!-- Note to self: Yandex doesn't have separate website placements for display; users use keywords for the sites/parts of the content network on which they want to advertise. -->

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Le frasi delle parole chiave, inclusa qualsiasi sintassi di tipo [Yandex](https://yandex.com/support/direct/keywords/symbols-and-operators.html) per le parole chiave. Ogni parola chiave può avere un massimo di sette parole, escluse le parole non significative.

È possibile immettere o incollare fino a 2.000 parole chiave. Separare più parole chiave con virgole o immetterle su righe separate.

>[!NOTE]
>
>* Se si modifica una parola chiave o un tipo di corrispondenza [!DNL Yandex], la parola chiave esistente verrà eliminata e ne verrà creata una nuova.
>* Ogni gruppo di annunci Yandex può includere un massimo di 200 parole chiave.

**[!UICONTROL Status]:** Lo stato di visualizzazione della parola chiave: *Attivo* o *In pausa*. Il valore predefinito per le nuove parole chiave è *Active*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Segnaposto

**[!UICONTROL Param1]** **[!UICONTROL Param2]:** Il valore delle variabili di sostituzione `{param1}` e `{param2}`, che vengono sostituite per eventuali istanze di {param1} e {param2} nell&#39;URL di base per annunci e sitelink quando la parola chiave viene utilizzata per visualizzare l&#39;annuncio. La lunghezza massima è di 255 byte.

I caratteri speciali vengono codificati automaticamente in UTF-8. Ad esempio, se l&#39;annuncio associato ha un URL di base &quot;http://www.example.com/{param1} e il valore a livello di parola chiave {param1} è &quot;shoes/flats.html&quot;, l&#39;annuncio conduce a http://www.example.com/shoes%2Fflats.html.

>[!MORELIKETHIS]
>
>* [Gestisci parole chiave](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
