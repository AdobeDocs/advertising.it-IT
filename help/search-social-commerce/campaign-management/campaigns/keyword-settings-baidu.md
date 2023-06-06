---
title: "[!DNL Baidu] keyword settings"
description: Fai riferimento alle impostazioni per [!DNL Baidu] parole chiave.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# [!DNL Baidu] impostazioni delle parole chiave

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Le parole chiave. La lunghezza massima per parola chiave è di 30 caratteri a byte singolo o 15 caratteri a byte doppio

È possibile immettere o incollare fino a 2.000 parole chiave. Separare più parole chiave con virgole o immetterle su righe separate. Utilizza la seguente sintassi:

* `keyword` per corrispondenza ampia
* `"keyword"` per corrispondenza frasi
* `[keyword]` per corrispondenza esatta

>[!NOTE]
>
>* [!DNL Baidu] consente un solo tipo di corrispondenza per parola chiave per gruppo di annunci. Ad esempio, il gruppo di annunci 1 non può includere entrambi `"keyword"` e `[keyword]`.
>* È possibile creare parole chiave negative dalla [!UICONTROL Keywords] > [!UICONTROL Negatives] visualizza e nelle impostazioni del gruppo di annunci e della campagna.
>* Modifica di un [!DNL Baidu] parola chiave elimina la parola chiave esistente e ne crea una nuova con un nuovo ID. Cambiando il tipo di corrispondenza, tuttavia, non elimina la parola chiave esistente.


**[!UICONTROL Status]:** Stato di visualizzazione della parola chiave: *Attivo* o *In pausa*. Il valore predefinito per le nuove parole chiave è *Attivo*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Opzioni URL

**[!UICONTROL Base URL]:** (Solo campagne con tracciamento a livello di parola chiave; facoltativo) URL della pagina di destinazione in cui vengono indirizzati gli utenti quando fanno clic sull’annuncio. Può includere codice di reindirizzamento e tracciamento di terze parti. Se inserisci un valore, questo sovrascrive l’URL di base dell’annuncio.

Dopo aver salvato il record, l’URL di base include tutti i parametri di aggiunta configurati per la campagna o l’account.

Se utilizzi il servizio di tracciamento delle conversioni di Adobe Advertising e le impostazioni della campagna includono l’utilizzo di [!UICONTROL EF Redirect] e aggiungendo il tracciamento a livello di parola chiave, Search, Social e Commerce aggiunge automaticamente il proprio codice di tracciamento dei clic.

>[!MORELIKETHIS]
>
>* [Gestire le parole chiave](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)

