---
title: Formati di tracciamento dei clic per [!DNL Yandex]
description: Scopri i formati di tracciamento dei clic per [!DNL Yandex] account.
exl-id: cf1d6c4b-9bcd-4b82-919f-c14dbaff9a76
feature: Search Tracking
source-git-commit: ca9425333731ada692c68f08b20f070265eb3409
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---

# Formati di tracciamento dei clic per annunci sponsorizzati su [!DNL Yandex]

Il seguente formato URL di destinazione di base si applica agli annunci sponsorizzati:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=90&ev_lx={phrase_id}&ev_crx={ad_id}&ev_ln={keyword}&ev_mt={source_type}&ev_ltx=&ev_src={source}&ev_pos={position}&ev_pt={position_type}&url=<the landing page>`

Esempio:

`http://pixel.everesttech.net/1234/cq?ev_sid=90&ev_lx={phrase_id}&amp;ev_crx={ad_id}&amp;ev_ln={keyword}&amp;ev_mt={source_type}&amp;ev_ltx=&amp;ev_src={source}&amp;ev_pos={position}&amp;ev_pt={position_type}&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` è una variabile per l’ID univoco dell’inserzionista in Adobi Advertising.
>
>* Questo formato indica che il passaggio del token è abilitato per la campagna (impostazione predefinita). Se il passaggio del token è disabilitato, sostituire `cq?` dopo `<advertiser_ID>` con `c?`.
>
>* `<the landing page>` è una variabile che rappresenta l’URL sul sito a cui vengono indirizzati gli utenti finali.
>
>* `source_type`  è il tipo di corrispondenza.
>
>* `source` indica se l’annuncio è stato visualizzato su un sito basato su ricerche o contenuti.
>
>* `position` è il numero di posizione dell’annuncio nel blocco. Per il traffico non di ricerca, il valore è &quot;0&quot;.
>
>* `position_type` è il blocco in cui l’annuncio è stato mostrato [!DNL Yandex]. Valori possibili: &quot;premium&quot; (blocco superiore), &quot;other&quot; (blocco destro) o &quot;none&quot; (traffico non di ricerca).

>[!MORELIKETHIS]
>
>* [Informazioni sui formati degli URL di tracciamento dei clic per il servizio di tracciamento delle conversioni di Adobe Advertising](formats-click-tracking-about.md)
>* [Formati per il codice di tracciamento AMO ID](amo-id-tracking-parameter.md)
