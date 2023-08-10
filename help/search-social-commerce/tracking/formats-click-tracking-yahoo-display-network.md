---
title: Formati di tracciamento dei clic per [!DNL Yahoo! Display Network]
description: Scopri i formati di tracciamento dei clic per [!DNL Yahoo! Display Network] account.
exl-id: 62ea592c-9138-4a8e-9616-c8f2475fea26
feature: Search Tracking
source-git-commit: f80d05aa40fd4114e9585220fe747ca7d36a19bb
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---

# Formati di tracciamento dei clic per annunci sponsorizzati su [!DNL Yahoo! Display Network]

Il seguente formato URL di destinazione di base si applica agli annunci sponsorizzati:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=86&ev_cl={ef_uniqueid}&url=<the landing page>`

Esempio:

`http://pixel.everesttech.net/1234/cq?ev_sid=86&ev_cl=258e27dcec70156a667f2229020e488&url=http%3A//www.example.com`

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
>* [Formati per il codice di tracciamento AMO ID](skwcid-tracking-parameter.md)
