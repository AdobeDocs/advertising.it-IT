---
title: '''[!DNL Microsoft Advertising] keyword settings"'
description: Fai riferimento alle impostazioni per [!DNL Microsoft Advertising] parole chiave.
exl-id: 82eee01f-db4b-4d1a-ae24-1ef65f8c6953
feature: Search Campaign Management
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] impostazioni delle parole chiave

Puoi creare parole chiave per le campagne che utilizzano le reti di ricerca e visualizzazione.

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Le parole chiave, comprese quelle [!DNL Microsoft Advertising] corrispondenza sintassi e segnaposto. La lunghezza massima per parola chiave è di 100 caratteri.

È possibile immettere o incollare fino a 2.000 parole chiave. Separare più parole chiave con virgole o immetterle su righe separate.

>[!NOTE]
>
>* È possibile creare parole chiave negative dalla [!UICONTROL Keywords] > [!UICONTROL Negatives] visualizza e nelle impostazioni del gruppo di annunci e della campagna.
>* Modifica di un [!DNL Microsoft Advertising] parola chiave elimina la parola chiave esistente e ne crea una nuova con un nuovo ID. Cambiando il tipo di corrispondenza, tuttavia, non elimina la parola chiave esistente.

**[!UICONTROL Status]:** Stato di visualizzazione della parola chiave: *Attivo* o *In pausa*. Il valore predefinito per le nuove parole chiave è *Attivo*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Segnaposto

**[!UICONTROL Param2]:** Stringa da utilizzare come valore di sostituzione se l’URL di base della parola chiave o il titolo, la descrizione o l’URL di base dell’annuncio contiene [il `{Param2}` stringa di sostituzione dinamica](https://help.bingads.microsoft.com/#apex/3/en/53079/0). La lunghezza massima è di 70 caratteri, ma tieni presente la lunghezza massima degli elementi dell’annuncio in cui lo utilizzi (ad esempio, il titolo 1 e il titolo 2 combinati possono contenere un massimo di 76 caratteri).

**[!UICONTROL Param3]:** Stringa da utilizzare come valore di sostituzione se l’URL di base della parola chiave o il titolo, la descrizione o l’URL di base dell’annuncio contiene [il `{Param3}` stringa di sostituzione dinamica](https://help.bingads.microsoft.com/#apex/3/en/53079/0). La lunghezza massima è di 70 caratteri, ma tieni presente la lunghezza massima degli elementi dell’annuncio in cui lo utilizzi (ad esempio, il titolo 1 e il titolo 2 combinati possono contenere un massimo di 76 caratteri).

## Opzioni URL

<!-- **[!UICONTROL Base URl]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

Questo campo può includere facoltativamente `{Param2}` e `{Param3}` variabili di sostituzione dinamiche.

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

>[!MORELIKETHIS]
>
>* [Gestire le parole chiave](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
