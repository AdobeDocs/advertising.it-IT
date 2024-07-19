---
title: '[!DNL Google Ads] impostazioni annuncio di sola chiamata'
description: Fai riferimento alle impostazioni per  [!DNL Google Ads] annunci di sola chiamata.
exl-id: 10672771-53fd-4ce9-9d67-6b1f8f5a41b8
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 0%

---

# [!DNL Google Ads] impostazioni annuncio di sola chiamata

Puoi creare annunci di testo di sola chiamata per le campagne che utilizzano la rete di ricerca.

Search, Social e Commerce tengono traccia degli annunci di sola chiamata utilizzando il suffisso della pagina di destinazione a livello di account e il modello di tracciamento, ma è possibile ignorare il tracciamento a livello di account a livello di annuncio in [!DNL Google Ads] Manager.

Consulta la guida di [!DNL Google Ads] per [limiti di annunci per account](https://support.google.com/google-ads/answer/6372658?hl=en).

<!-- ## Call-only Ad -->

<!-- hiding section header since there's only one section -->

**[!UICONTROL Business Name]:** Il nome dell&#39;azienda. La lunghezza massima è di 25 caratteri o 12 caratteri a doppio byte.

**[!UICONTROL Country]:** (Facoltativo) Il paese in cui si trova l&#39;azienda.

**[!UICONTROL Phone Number]:** Il numero di telefono dell&#39;azienda. Esempi: (124) 123-4567, 12345678901, +441234567890.

**[!UICONTROL Description 1], [!UICONTROL Description 2]:** Prima e seconda riga del corpo dell&#39;annuncio. La lunghezza massima per ogni riga è di 35 caratteri o 17 caratteri a doppio byte.

La sintassi di sostituzione delle parole chiave non viene conteggiata per la lunghezza massima consentita. Ad esempio, &quot;`{Description1: Free Account Analysis!}`&quot; è trattato come 22 caratteri (solo la parte &quot;Analisi account gratuito\!&quot;).

>[!NOTE]
>
>I campi di descrizione non possono includere numeri di telefono.

**[!UICONTROL Display URL]:** URL visualizzato nell&#39;annuncio. L’URL di visualizzazione deve corrispondere a un dominio associato alla tua azienda, ma l’annuncio non invia persone a una pagina di destinazione.

La lunghezza massima è di 35 caratteri a byte singolo o 17 caratteri a byte doppio. La sintassi di sostituzione delle parole chiave non viene conteggiata per la lunghezza massima consentita. Ad esempio, &quot;`{DisplayURL: example.com}`&quot; viene trattato come 11 caratteri (solo la parte &quot;example.com&quot;).

**[!UICONTROL Verification URL]:** (Facoltativo) Pagina Web in cui il numero di telefono dell&#39;annuncio viene visualizzato come testo, in modo che [!DNL Google Ads] possa verificare che il numero di telefono sia valido. Deve avere lo stesso dominio dell’URL di visualizzazione dell’annuncio.

**[!UICONTROL Is Tracked]:** Abilita il tracciamento delle chiamate e le conversioni di sola chiamata.

**[!UICONTROL Count calls as phone call conversions]:** (quando &quot;[!UICONTROL Is Tracked]&quot; è selezionato; facoltativo) attribuisce tutte le chiamate risultanti dall&#39;annuncio a un tipo specifico di conversione di chiamata, quando ne è specificato uno. In caso contrario, [!DNL Google Ads] crea un&#39;azione di conversione predefinita denominata &quot;[!UICONTROL Calls from ads]&quot; una volta che registra almeno una conversione dai numeri di inoltro e quindi attribuisce le chiamate ad essa.

**[!UICONTROL Count Action]:** (Quando &quot;[!UICONTROL Count calls as phone call conversions]&quot; è selezionato; facoltativo) Azione di conversione esistente a cui vengono attribuite le chiamate.

È possibile creare e gestire azioni di conversione in [!DNL Google Ads].

<!-- **[!UICONTROL Status]:** -->

{{$include /help/_includes/status-ad.md}}

>[!MORELIKETHIS]
>
>* [Informazioni sugli annunci](ad-about.md)
>* [Gestione annunci](ad-manage.md)
>* [[!DNL Google Ads] impostazioni annuncio ricerca dinamica espansa](ad-settings-google-dsa.md)
>* [[!DNL Google Ads] impostazioni degli annunci di ricerca responsive](ad-settings-google-rsa.md)
