---
title: Formati di tracciamento dei clic per [!DNL Baidu]
description: Scopri i formati di tracciamento dei clic per [!DNL Baidu] account.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---

# Formati di tracciamento dei clic per annunci sponsorizzati su [!DNL Baidu]

Il seguente formato URL di destinazione di base si applica agli annunci sponsorizzati:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_cmpid=<campaignID>&&ev_lx={keywordid}&ev_crx={creative}&ev_pl={placement}&url=<the landing page>`

Esempio:

`http://pixel.everesttech.net/1234/cq?ev_sid=88&ev_cmpid=800577124&&ev_lx={keywordid}&ev_crx={creative}&ev_pl={placement}&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` è una variabile per l’ID univoco dell’inserzionista in Adobe Advertising.
>
>* Questo formato indica che il passaggio del token è abilitato per la campagna (impostazione predefinita). Se il passaggio del token è disabilitato, sostituire `cq?` dopo `<advertiser_ID>` con `c?`.
>
>* `<campaignID>` è una variabile per l’ID numerico della campagna.
>
>* `<the landing page>` è una variabile che rappresenta l’URL sul sito a cui vengono indirizzati gli utenti finali.


>[!MORELIKETHIS]
>
>* [Informazioni sui formati degli URL di tracciamento dei clic per il servizio di tracciamento delle conversioni di Adobe Advertising](formats-click-tracking-about.md)
>* [Formati per il codice di tracciamento s\_kwcid](skwcid-tracking-parameter.md)

