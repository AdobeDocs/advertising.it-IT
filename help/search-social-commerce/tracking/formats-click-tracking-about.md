---
title: Informazioni sui formati degli URL di tracciamento dei clic per il servizio di tracciamento delle conversioni di Adobe Advertising
description: Scopri i formati di tracciamento dei clic per le reti di annunci supportate.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 0%

---

# Informazioni sui formati degli URL di tracciamento dei clic per il servizio di tracciamento delle conversioni di Adobe Advertising

I modelli di tracciamento, i suffissi delle pagine di destinazione (suffissi URL finali) e gli URL di destinazione per gli account e le campagne di annunci che utilizzano il servizio di tracciamento delle conversioni di Advertising di Adobe hanno il seguente formato:

`http://pixel.everesttech.net/<advertiser_ID>/<token passing parameter>?ev_sid=<ad network ID>&<tracking ID>&url=<the landing page>`

dove:

* `http://pixel.everesttech.net` reindirizza l’utente ai pixel server di Adobe Advertising.

* `<advertiser_ID>` è una variabile per l’ID utente univoco assegnato all’inserzionista all’interno di Adobe Advertising.

* `<token passing parameter>` è una variabile per uno dei seguenti elementi:

   * `cq?` o `rq` indica che il passaggio del token è abilitato.

   * `c?` o `r` indica che il passaggio del token è disabilitato.

* `<ad network ID>` è una variabile per l’ID numerico della rete di annunci specificata, ad esempio *3* per [!DNL Google Ads], *10* per [!DNL Microsoft Advertising], *45* per [!DNL Meta], *86* per [!DNL Yahoo! Display Network], *87* per [!DNL Naver], *88* per [!DNL Baidu], *90* per [!DNL Yandex], *94* per [!DNL Yahoo! Japan Ads], *105* per [!DNL Yahoo Native] (obsoleto), oppure *106* per [!DNL Pinterest] (obsoleto).

* `<tracking ID>` è una variabile per una stringa dell’ID di tracciamento generato dal sistema che identifica una parola chiave, un annuncio o un posizionamento univoco nell’account. La stringa varia in base alla rete di annunci.

* `<the landing page>` è una variabile che rappresenta l’URL sul sito a cui vengono indirizzati gli utenti finali. Per gli account con URL di destinazione, questo valore è un URL. Per gli account con modelli di tracciamento, questo valore è un parametro (ad esempio `{lpurl}`) che rappresenta l’URL finale.

Vedere le pagine separate che indicano [[!DNL Baidu] formati](formats-click-tracking-baidu.md), [[!DNL Google Ads] formati](formats-click-tracking-google.md), [[!DNL Microsoft Advertising] formati](formats-click-tracking-microsoft.md), [[!DNL Naver] formati](formats-click-tracking-naver.md), [[!DNL Yahoo! Display Network] formati](formats-click-tracking-yahoo-display-network.md), [[!DNL Yahoo! Japan Ads] formati](formats-click-tracking-yahoo-japan.md), e [[!DNL Yandex] formati](formats-click-tracking-yandex.md).

>[!MORELIKETHIS]
>
>* [Formati di tracciamento dei clic per annunci sponsorizzati su [!DNL Baidu]](formats-click-tracking-baidu.md)
>* [Formati di tracciamento dei clic per [!DNL Google Ads]](formats-click-tracking-google.md)
>* [Formati di tracciamento dei clic per [!DNL Microsoft Advertising]](formats-click-tracking-microsoft.md)
>* [Formati di tracciamento dei clic per annunci sponsorizzati su [!DNL Naver]](formats-click-tracking-naver.md)
>* [Formati di tracciamento dei clic per annunci sponsorizzati su [!DNL Yahoo! Japan Ads]](formats-click-tracking-yahoo-japan.md)
>* [Formati di tracciamento dei clic per annunci sponsorizzati su [!DNL Yahoo! Display Network]](formats-click-tracking-yahoo-display-network.md)
>* [Formati di tracciamento dei clic per annunci sponsorizzati su [!DNL Yandex]](formats-click-tracking-yandex.md)

