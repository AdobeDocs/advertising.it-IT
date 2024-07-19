---
title: '[!DNL Baidu] impostazioni parola chiave'
description: Fai riferimento alle impostazioni per  [!DNL Baidu]  parole chiave.
exl-id: 3b3a578b-06f1-486f-9ade-9104e0a1dd5f
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 0%

---

# [!DNL Baidu] impostazioni parola chiave

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Le parole chiave. La lunghezza massima per parola chiave è di 30 caratteri a byte singolo o 15 caratteri a byte doppio

È possibile immettere o incollare fino a 2.000 parole chiave. Separare più parole chiave con virgole o immetterle su righe separate. Utilizza la seguente sintassi:

* `keyword` per corrispondenza ampia
* `"keyword"` per corrispondenza frase
* `[keyword]` per corrispondenza esatta

>[!NOTE]
>
>* [!DNL Baidu] consente un solo tipo di corrispondenza per parola chiave per gruppo di annunci. Ad esempio, il gruppo di annunci 1 non può includere sia `"keyword"` che `[keyword]`.
>* È possibile creare parole chiave negative dalla visualizzazione [!UICONTROL Keywords] > [!UICONTROL Negatives] e nelle impostazioni del gruppo di annunci e della campagna.
>* La modifica di una parola chiave [!DNL Baidu] comporta l&#39;eliminazione della parola chiave esistente e la creazione di una nuova parola chiave con un nuovo ID. Cambiando il tipo di corrispondenza, tuttavia, non elimina la parola chiave esistente.

**[!UICONTROL Status]:** Lo stato di visualizzazione della parola chiave: *Attivo* o *In pausa*. Il valore predefinito per le nuove parole chiave è *Active*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Opzioni URL

**[!UICONTROL Base URL]:** (solo campagne con tracciamento a livello di parola chiave; facoltativo) URL della pagina di destinazione utilizzato dagli utenti quando fanno clic sull&#39;annuncio. Può includere
codice di reindirizzamento e tracciamento di terze parti. Se inserisci un valore, questo sovrascrive l’URL di base dell’annuncio.

Dopo aver salvato il record, l’URL di base include tutti i parametri di aggiunta configurati per la campagna o l’account.

Se si utilizza il servizio di monitoraggio delle conversioni di Adobe Advertising e le impostazioni della campagna includono l&#39;utilizzo di [!UICONTROL EF Redirect] e l&#39;aggiunta del monitoraggio a livello di parola chiave, Search, Social e Commerce aggiungono automaticamente il proprio codice di monitoraggio dei clic.

>[!MORELIKETHIS]
>
>* [Gestisci parole chiave](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
