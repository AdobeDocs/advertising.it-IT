---
title: Informazioni sui formati degli URL di tracciamento dei clic per il servizio di tracciamento delle conversioni di Adobe Advertising
description: Scopri i formati di tracciamento dei clic per le reti di annunci supportate.
exl-id: b6f225d5-2268-4b2a-9927-063155ba0dc5
feature: Search Tracking
TQID: https://experienceleague.adobe.com/pVSEKmf45CqsfXMbj8HGDltdgV3wUV2UsAzP94vkijg
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: a65752f7baeae4193fe55d2f8b9f7a78b126ef06
workflow-type: tm+mt
source-wordcount: 269
ht-degree: 0%

---

# Informazioni sui formati degli URL di tracciamento dei clic per il servizio di tracciamento delle conversioni di Adobe Advertising

I modelli di tracciamento, i suffissi della pagina di destinazione (suffissi URL finali) e gli URL di destinazione per gli account degli annunci e le campagne che utilizzano il servizio di tracciamento delle conversioni di Adobe Advertising hanno il seguente formato:

`http://pixel.everesttech.net/<advertiser_ID>/<token passing parameter>?ev_sid=<ad network ID>&<tracking ID>&url=<the landing page>`

dove:

* `http://pixel.everesttech.net` reindirizza l&#39;utente ai pixel server di Adobe Advertising.

* `<advertiser_ID>` è una variabile per l&#39;ID utente univoco assegnato all&#39;inserzionista in Adobe Advertising.

* `<token passing parameter>` è una variabile per uno dei seguenti elementi:

   * `cq?` o `rq` indica che il passaggio del token è abilitato.

   * `c?` o `r` indica che il passaggio del token è disabilitato.

* `<ad network ID>` è una variabile per l&#39;ID numerico per la rete di annunci specificata, ad esempio *3* per [!DNL Google Ads], *10* per [!DNL Microsoft Advertising], *45* per [!DNL Meta], *86* per [!DNL Yahoo DSP], *87* per [!DNL Naver], *88* per [!DNL Baidu], *90* per [!DNL Yandex], *94* per [!DNL LY Ads] (in precedenza [!DNL Yahoo! Japan Ads]), *105* per [!DNL Yahoo Native] (obsoleto) o *106* per [!DNL Pinterest] (obsoleto).

* `<tracking ID>` è una variabile per una stringa ID di tracciamento generata dal sistema che identifica una parola chiave, un annuncio o un posizionamento univoco nell&#39;account. La stringa varia in base alla rete di annunci.

* `<the landing page>` è una variabile che rappresenta l&#39;URL del sito a cui sono indirizzati gli utenti finali. Per gli account con URL di destinazione, questo valore è un URL. Per gli account con modelli di tracciamento, questo valore è un parametro (ad esempio `{lpurl}`) che rappresenta l&#39;URL finale.

Visualizzare le pagine separate che indicano [[!DNL Baidu] formati](formats-click-tracking-baidu.md), [[!DNL Google Ads] formati](formats-click-tracking-google.md), [[!DNL Microsoft Advertising] formati](formats-click-tracking-microsoft.md), [[!DNL Naver] formati](formats-click-tracking-naver.md), [[!DNL Yahoo DSP] formati](formats-click-tracking-yahoo-display-network.md), [[!DNL Yahoo! Japan Ads] formati](formats-click-tracking-yahoo-japan.md) e [[!DNL Yandex] formati](formats-click-tracking-yandex.md).

>[!MORELIKETHIS]
>
>* [Formati di tracciamento dei clic per annunci sponsorizzati il [!DNL Baidu]](formats-click-tracking-baidu.md)
>* [Formati di tracciamento dei clic per [!DNL Google Ads]](formats-click-tracking-google.md)
>* [Formati di tracciamento dei clic per annunci sponsorizzati il [!DNL LY Ads]](formats-click-tracking-yahoo-japan.md)
>* [Formati di tracciamento dei clic per [!DNL Microsoft Advertising]](formats-click-tracking-microsoft.md)
>* [Formati di tracciamento dei clic per annunci sponsorizzati il [!DNL Naver]](formats-click-tracking-naver.md)
>* [Formati di tracciamento dei clic per annunci sponsorizzati il [!DNL Yahoo DSP]](formats-click-tracking-yahoo-display-network.md)
>* [Formati di tracciamento dei clic per annunci sponsorizzati il [!DNL Yandex]](formats-click-tracking-yandex.md)
