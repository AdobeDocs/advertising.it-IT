---
title: Panoramica dell’integrazione tra Adobe Advertising e Adobe Customer Journey Analytics
description: Scopri le opzioni di integrazione di Adobe Advertising con Adobe Customer Journey Analytics.
feature: Integration with Adobe Customer Journey Analytics
exl-id: 57636259-f91a-404f-b972-994af67098b1
source-git-commit: ca039c91a976d79ed732ad7e0435566d58f3f843
workflow-type: tm+mt
source-wordcount: '403'
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

* (Prossima funzionalità beta) Gli inserzionisti con Customer Journey Analytics ma non con [!DNL Analytics for Advertising] possono scambiare dati in modo nativo tra Adobe Advertising e Customer Journey Analytics utilizzando [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=it). È possibile tenere traccia degli eventi del sito utilizzando cookie, IP con hash, ID universali ([!DNL LiveRamp RampIDs] e ID5 ID) e attribuire eventi del sito all&#39;attività multimediale a pagamento. I seguenti dati sono disponibili a livello di campagna, gruppo di annunci, pacchetto, posizionamento e parola chiave:

   * Dati sulle prestazioni della campagna da Adobe Advertising in Customer Journey Analytics

     **Nota:** i dati di [!DNL Apple] e [!DNL Tiktok] non sono disponibili.

   * Attività del sito e conversioni monitorate da [!DNL Google Ads] e [!DNL Microsoft Advertising] in Customer Journey Analytics

   * Dati di attribuzione da Customer Journey Analytics in Adobe Advertising, dove possono essere utilizzati per l’ottimizzazione e il reporting

  In questo caso d&#39;uso, utilizzare Web SDK per tenere traccia degli eventi del sito (utilizzando cookie, indirizzi IP con hash o ID universali) e attribuire gli eventi del sito all&#39;attività paid media in [!DNL Google Ads], [!DNL Microsoft Advertising] e [!DNL Meta] e Adobe DSP. Per la raccolta dei dati verrà inoltre utilizzato Adobe Experience Platform.

## Come avviare un’integrazione nativa tra Adobe Advertising e Customer Journey Analytics

Contatta il team del tuo account Adobe, che completerà la configurazione iniziale necessaria per iniziare e ti aiuterà a pianificare l’implementazione e l’utilizzo dei dati in base alle esigenze della tua organizzazione.

>[!MORELIKETHIS]
>
>* [Prerequisiti](prerequisites.md)
>* (Utenti Adobe Analytics) [Raccogli i dati storici per gli AMO ID e gli EF ID da utilizzare in Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
