---
title: '[!DNL Google Ads] impostazioni parola chiave'
description: Fai riferimento alle impostazioni per  [!DNL Google Ads]  parole chiave.
exl-id: b2937d18-565a-43f0-ba33-d46d4c77ec07
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/XwutnbHVQrg8mfimzVjv-Px6OeUsOWzT7-347-ff2C0
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 191
ht-degree: 0%

---

# [!DNL Google Ads] impostazioni parola chiave

Puoi creare parole chiave per le campagne che utilizzano le reti di ricerca e visualizzazione.

Consulta la guida di Google Ads per [limiti di parole chiave per account](https://support.google.com/google-ads/answer/6372658).

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Le parole chiave, incluse eventuali [!DNL Google Ads], corrispondono alla sintassi per parole chiave e segnaposto. [!DNL Google Ads] account richiedono parole chiave con i seguenti attributi:

* La lunghezza massima per parola chiave è di 80 caratteri e non più di 10 parole.
* La parola chiave può contenere solo lettere, cifre e i seguenti caratteri speciali: spazio `# $ & _ - " [] ' + . / :`

È possibile immettere o incollare fino a 2.000 parole chiave. Separare più parole chiave con virgole o immetterle su righe separate.

>[!NOTE]
>
>* È possibile creare parole chiave negative dalla visualizzazione [!UICONTROL Keywords] > [!UICONTROL Negatives] e nelle impostazioni del gruppo di annunci e della campagna.
>* Se si modifica una parola chiave o un tipo di corrispondenza [!DNL Google Ads], la parola chiave esistente verrà eliminata e ne verrà creata una nuova.

**[!UICONTROL Status]:** Lo stato di visualizzazione della parola chiave: *Attivo* o *In pausa*. Il valore predefinito per le nuove parole chiave è *Active*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Segnaposto

**[!UICONTROL Param1]:** Stringa da utilizzare come valore di sostituzione se l&#39;URL di base o il modello di tracciamento contiene [la stringa di sostituzione dinamica `{param1}`](https://support.google.com/google-ads/answer/6305348).

**[!UICONTROL Param2]:** Stringa da utilizzare come valore di sostituzione se l&#39;URL di base o il modello di tracciamento contiene [la stringa di sostituzione dinamica `{param2}`](https://support.google.com/google-ads/answer/6305348).

## Opzioni URL

<!-- **[!UICONTROL Base URl]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

<!-- **[note for Base URL field]:** -->

{{$include /help/_includes/base-url-google-note.md}}

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

>[!MORELIKETHIS]
>
>* [Gestisci parole chiave](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
