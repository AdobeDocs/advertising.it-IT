---
title: Formati di tracciamento dei clic per  [!DNL Yandex]
description: Scopri i formati di tracciamento dei clic per  [!DNL Yandex]  account.
exl-id: bcbd369b-b98d-491c-a921-58bf79e01744
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---

# Formati di tracciamento dei clic per annunci sponsorizzati su [!DNL Yandex]

Il seguente formato URL di destinazione di base si applica agli annunci sponsorizzati:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=90&ev_lx={phrase_id}&ev_crx={ad_id}&ev_ln={keyword}&ev_mt={source_type}&ev_ltx=&ev_src={source}&ev_pos={position}&ev_pt={position_type}&url=<the landing page>`

Esempio:

`http://pixel.everesttech.net/1234/cq?ev_sid=90&ev_lx={phrase_id}&amp;ev_crx={ad_id}&amp;ev_ln={keyword}&amp;ev_mt={source_type}&amp;ev_ltx=&amp;ev_src={source}&amp;ev_pos={position}&amp;ev_pt={position_type}&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` è una variabile per l&#39;ID univoco dell&#39;inserzionista in Adobe Advertising.
>
>* Questo formato indica che il passaggio del token è abilitato per la campagna (impostazione predefinita). Se il passaggio del token è disabilitato, sostituire `cq?` dopo `<advertiser_ID>` con `c?`.
>
>* `<the landing page>` è una variabile che rappresenta l&#39;URL del sito a cui sono indirizzati gli utenti finali.
>
>* `source_type` è il tipo di corrispondenza.
>
>* `source` indica se l&#39;annuncio è stato visualizzato su un sito basato su ricerche o contenuti.
>
>* `position` è il numero di posizione dell&#39;annuncio nel blocco. Per il traffico non di ricerca, il valore è &quot;0&quot;.
>
>* `position_type` è il blocco in cui l&#39;annuncio è stato mostrato su [!DNL Yandex]. Valori possibili: &quot;premium&quot; (blocco superiore), &quot;other&quot; (blocco destro) o &quot;none&quot; (traffico non di ricerca).

>[!MORELIKETHIS]
>
>* [Informazioni sui formati degli URL di tracciamento dei clic per il servizio di tracciamento delle conversioni di Adobe Advertising](formats-click-tracking-about.md)
>* [Formati AMO ID](/help/integrations/analytics/ids.md#amo-id-formats)
