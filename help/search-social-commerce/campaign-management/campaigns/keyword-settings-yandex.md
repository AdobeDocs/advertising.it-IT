---
title: '''[!DNL Yandex] keyword settings"'
description: Fai riferimento alle impostazioni per [!DNL Yandex] parole chiave.
exl-id: 276f991b-f604-445c-8dd0-481b6eaee3d2
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 0%

---

# [!DNL Yandex] impostazioni delle parole chiave

Le parole chiave Yandex vengono utilizzate sia per le reti di ricerca che per quelle di visualizzazione (contenuto).

<!-- Note to self: Yandex doesn't have separate website placements for display; users use keywords for the sites/parts of the content network on which they want to advertise. -->

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Le frasi delle parole chiave, comprese [Sintassi del tipo di corrispondenza Yandex](https://yandex.com/support/direct/keywords/symbols-and-operators.html) per parole chiave. Ogni parola chiave può avere un massimo di sette parole, escluse le parole non significative.

È possibile immettere o incollare fino a 2.000 parole chiave. Separare più parole chiave con virgole o immetterle su righe separate.

>[!NOTE]
>
>* Modifica di un [!DNL Yandex] parola chiave o tipo corrispondenza elimina la parola chiave esistente e ne crea una nuova.
>* Ogni gruppo di annunci Yandex può includere un massimo di 200 parole chiave.

**[!UICONTROL Status]:** Stato di visualizzazione della parola chiave: *Attivo* o *In pausa*. Il valore predefinito per le nuove parole chiave è *Attivo*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Segnaposto

**[!UICONTROL Param1]** **[!UICONTROL Param2]:** Il valore della proprietà `{param1}` e `{param2}` variabili di sostituzione, sostituite per qualsiasi istanza di {param1} e {param2} nell’URL di base per annunci e sitelink quando la parola chiave viene utilizzata per visualizzare l’annuncio. La lunghezza massima è di 255 byte.

I caratteri speciali vengono codificati automaticamente in UTF-8. Ad esempio, se l’annuncio associato ha un URL di base &quot;http://www.example.com/{param1} e il valore a livello di parola chiave di {param1} è &quot;shoes/flats.html&quot;, quindi l’annuncio conduce a http://www.example.com/shoes%2Fflats.html.

>[!MORELIKETHIS]
>
>* [Gestire le parole chiave](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
