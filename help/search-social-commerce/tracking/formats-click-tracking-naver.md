---
title: Formati di tracciamento dei clic per  [!DNL Naver]
description: Scopri i formati di tracciamento dei clic per  [!DNL Naver]  account.
exl-id: b438652e-6e98-4223-8169-2bfb37500670
feature: Search Tracking
TQID: https://experienceleague.adobe.com/c1zAy1aKgr4MRpyiitdmO4VxP7kfKfFWHzYk88lvX2w
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 90
ht-degree: 0%

---

# Formati di tracciamento dei clic per annunci sponsorizzati su [!DNL Naver]

Il seguente formato URL di destinazione di base si applica agli annunci sponsorizzati:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=87&ev_cl={ef_uniqueid}&url=<the landing page>`

Esempio:

`http://pixel.everesttech.net/1234/cq?ev_sid=87&ev_cl=258e27dcec70156a667f2229020e488&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` è una variabile per l&#39;ID univoco dell&#39;inserzionista all&#39;interno di Adobe Advertising.
>
>* Questo formato indica che il passaggio del token è abilitato per la campagna (impostazione predefinita). Se il passaggio del token è disabilitato, sostituire `cq?` dopo `<advertiser_ID>` con `c?`.
>
>* `<the landing page>` è una variabile che rappresenta l&#39;URL del sito a cui sono indirizzati gli utenti finali.

>[!MORELIKETHIS]
>
>* [Informazioni sui formati degli URL di tracciamento dei clic per il servizio di tracciamento conversione di Adobe Advertising](formats-click-tracking-about.md)
>* [Formati AMO ID](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/amo-id#dimension-items)
