---
title: Panoramica dell’integrazione tra Adobe Advertising e Adobe Customer Journey Analytics
description: Scopri le opzioni di integrazione di Adobe Advertising con Adobe Customer Journey Analytics.
feature: Integration with Adobe Customer Journey Analytics
exl-id: 57636259-f91a-404f-b972-994af67098b1
TQID: https://experienceleague.adobe.com/nxn5AcKCc-xm-k5LXOcKIquNKyoXbt3soR5nhQR0w-E
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: a93c33ee47bd1a8df137a69598b367e985def4ee
workflow-type: tm+mt
source-wordcount: 499
ht-degree: 0%

---

# Panoramica dell’integrazione tra Adobe Advertising e Customer Journey Analytics

<!-- title? If I change, change refs throughout -->

*Inserzionisti con Advertising DSP e[!DNL Advertising Search, Social, & Commerce]*

Adobe Advertising è integrato con Adobe Customer Journey Analytics per la condivisione bidirezionale dei dati e il reporting. Sono disponibili due opzioni per impostare l’integrazione:

* Gli inserzionisti con [!DNL Analytics for Advertising] e Customer Journey Analytics hanno le stesse funzionalità che hanno tramite [!DNL Analytics for Advertising], con l&#39;aggiunta di visualizzazioni in Customer Journey Analytics.

  Continuerai a tenere traccia degli eventi di click-through utilizzando Adobe Experience Platform Web SDK (`alloy.js`) o il servizio Adobe Experience Cloud Identity (`visitorAPI.js`). Gli inserzionisti con Advertising DSP continueranno a utilizzare uno snippet di JavaScript per monitorare gli eventi view-through. I dati disponibili in Customer Journey Analytics includono:

   * Dati sulle prestazioni della campagna da Adobe Advertising in Customer Journey Analytics

   * Attività del sito e conversioni monitorate da [!DNL Google Ads] e [!DNL Microsoft Advertising] in Customer Journey Analytics, aggiornato ogni giorno

   * Dati di attribuzione da [!DNL Analytics] in Adobe Advertising, dove possono essere utilizzati per l&#39;ottimizzazione e il reporting

  In questo caso d&#39;uso, è comunque possibile [raccogliere dati storici per gli AMO ID e gli EF ID da utilizzare in Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).

<!--
  In this use case, you don't need to perform any extra steps except to optionally [collect historical data for AMO IDs and EF IDs for use in Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
-->

* Gli inserzionisti con Customer Journey Analytics ma non [!DNL Analytics for Advertising] possono scambiare dati in modalità nativa tra Adobe Advertising e Customer Journey Analytics utilizzando [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=it). È possibile tenere traccia degli eventi del sito utilizzando cookie, IP con hash, ID universali ([!DNL LiveRamp RampIDs] e ID5 ID) e attribuire eventi del sito all&#39;attività multimediale a pagamento. I seguenti dati sono disponibili a livello di campagna, gruppo di annunci, pacchetto, posizionamento e parola chiave:

   * Dati sulle prestazioni della campagna da Adobe Advertising in Customer Journey Analytics

     **Nota:** i dati di [!DNL Apple] e [!DNL Tiktok] non sono disponibili.

   * Attività del sito e conversioni monitorate da [!DNL Google Ads] e [!DNL Microsoft Advertising] in Customer Journey Analytics

   * Dati di attribuzione da Customer Journey Analytics in Adobe Advertising, dove possono essere utilizzati per l’ottimizzazione e il reporting

  In questo caso d&#39;uso, utilizzare Web SDK per tenere traccia degli eventi del sito (utilizzando cookie, indirizzi IP con hash o ID universali) e attribuire gli eventi del sito all&#39;attività paid media in [!DNL Google Ads], [!DNL Microsoft Advertising] e [!DNL Meta] e Adobe DSP. Per la raccolta dei dati verrà inoltre utilizzato Adobe Experience Platform.

## Definizioni dei tipi di dati per i rapporti

* **Dati a livello di evento:** eventi con marca temporale, ad esempio sessioni, visualizzazioni di pagina, invii di moduli lead e invii di applicazioni.

* **Dati di riepilogo:** dati di reporting aggregati, ad esempio Ad Platform, Campaign, Placement, Impression, Click e Cost.

* **Dati di classificazione/dimensioni:** dimensioni di reporting, ad esempio il nome della campagna Adobe Advertising, il nome del portfolio o l&#39;ID posizionamento. Puoi cercare (filtrare) i dati a livello di evento e i dati di riepilogo per classificazione/dimensione.

## Come avviare un’integrazione nativa tra Adobe Advertising e Customer Journey Analytics {#integration-cja-initiate}

Contatta il team del tuo account Adobe, che completerà la configurazione iniziale necessaria per iniziare e ti aiuterà a pianificare l’implementazione e l’utilizzo dei dati in base alle esigenze della tua organizzazione.

>[!MORELIKETHIS]
>
>* [Prerequisiti](prerequisites.md)
>* [ID Adobe Advertising utilizzati da [!DNL Customer Journey Analytics]](ids.md)
>* [Imposta raccolta dati, trasferimento dati e reporting](set-up.md)
>* [Metriche e dimensioni di Adobe Advertising in Customer Journey Analytics](advertising-data-in-cja.md)
>* (Utenti Adobe Analytics) [Raccogli dati storici per gli AMO ID e gli EF ID da utilizzare in Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
>* [Risoluzione dei problemi](troubleshooting.md)
