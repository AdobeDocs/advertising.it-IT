---
title: Formati di tracciamento dei clic per [!DNL Yahoo! Japan Ads]
description: Scopri i formati di tracciamento dei clic per [!DNL Yahoo! Japan Ads] account.
exl-id: 4584f2c4-8090-4931-bd44-0df42f350755
feature: Search Tracking
source-git-commit: ca9425333731ada692c68f08b20f070265eb3409
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# Formati di tracciamento dei clic per annunci sponsorizzati su [!DNL Yahoo! Japan Ads]

I seguenti formati di modello di tracciamento di base si applicano agli annunci sponsorizzati:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=!{unescapedlpurl}`

oppure, se l’opzione di assegnazione tag automatica è impostata per l’account in [!DNL Yahoo! Japan Ads]:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=!{unescapedlpurl}/?yclid=<yclid>`

Esempio:

`http://pixel.everesttech.net/1234/cq?ev_sid=94&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=http%3A//www.example.com/?yclid=1234567890`

>[!NOTE]
>
>* `<advertiser_ID>` è una variabile per l’ID univoco dell’inserzionista in Adobi Advertising.
>
>* Questo formato indica che il passaggio del token è abilitato per la campagna (impostazione predefinita). Se il passaggio del token è disabilitato, sostituire `cq?` dopo `<advertiser_ID>` con `c?`.
>
>* `<the landing page>` è una variabile che rappresenta l’URL sul sito a cui vengono indirizzati gli utenti finali.

>[!MORELIKETHIS]
>
>* [Informazioni sui formati degli URL di tracciamento dei clic per il servizio di tracciamento delle conversioni di Adobe Advertising](formats-click-tracking-about.md)
>* [Formati per il codice di tracciamento AMO ID](amo-id-tracking-parameter.md)
