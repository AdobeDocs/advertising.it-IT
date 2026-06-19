---
title: Formati di tracciamento dei clic per  [!DNL LY Ads]
description: Scopri i formati di tracciamento dei clic per  [!DNL LY Ads]  account.
exl-id: 79e45205-5c72-4612-9b60-36538e3c48c4
feature: Search Tracking
TQID: https://experienceleague.adobe.com/ZFNzA0bfxKhlNW6fvPWMwBc4naT7rOhvym-wSpxvYXg
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 47de92fd6d4b1d481380a58f75ec4735d95fca73
workflow-type: tm+mt
source-wordcount: 115
ht-degree: 0%

---

# Formati di tracciamento dei clic per annunci sponsorizzati su [!DNL LY Ads]

I seguenti formati di modello di tracciamento di base si applicano agli annunci sponsorizzati:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=!{unescapedlpurl}`

oppure, quando l&#39;opzione di assegnazione tag automatica è impostata per l&#39;account in [!DNL LY Ads]:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=!{unescapedlpurl}/?yclid=<yclid>`

Esempio:

`http://pixel.everesttech.net/1234/cq?ev_sid=94&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=http%3A//www.example.com/?yclid=1234567890`

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
>* [Formati AMO ID](https://experienceleague.adobe.com/it/docs/analytics/components/dimensions/amo-id#dimension-items)
