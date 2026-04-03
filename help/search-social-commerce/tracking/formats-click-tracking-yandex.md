---
title: Formati di tracciamento dei clic per  [!DNL Yandex]
description: Scopri i formati di tracciamento dei clic per  [!DNL Yandex]  account.
exl-id: bcbd369b-b98d-491c-a921-58bf79e01744
feature: Search Tracking
TQID: https://experienceleague.adobe.com/iw-C9oApjU-LeXi3XJol3lgCJPGPegHgzFJIL-3HHSA
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 145
ht-degree: 0%

---

# Formati di tracciamento dei clic per annunci sponsorizzati su [!DNL Yandex]

Il seguente formato URL di destinazione di base si applica agli annunci sponsorizzati:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=90&ev_lx={phrase_id}&ev_crx={ad_id}&ev_ln={keyword}&ev_mt={source_type}&ev_ltx=&ev_src={source}&ev_pos={position}&ev_pt={position_type}&url=<the landing page>`

Esempio:

`http://pixel.everesttech.net/1234/cq?ev_sid=90&ev_lx={phrase_id}&amp;ev_crx={ad_id}&amp;ev_ln={keyword}&amp;ev_mt={source_type}&amp;ev_ltx=&amp;ev_src={source}&amp;ev_pos={position}&amp;ev_pt={position_type}&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` è una variabile per l&#39;ID univoco dell&#39;inserzionista all&#39;interno di Adobe Advertising.
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
>* [Informazioni sui formati degli URL di tracciamento dei clic per il servizio di tracciamento conversione di Adobe Advertising](formats-click-tracking-about.md)
>* [Formati AMO ID](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/amo-id#dimension-items)
