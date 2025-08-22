---
title: Panoramica dell’integrazione tra Adobe Advertising e Adobe Customer Journey Analytics
description: Scopri le opzioni di integrazione di Adobe Advertising con Adobe Customer Journey Analytics.
feature: Integration with Adobe Customer Journey Analytics
source-git-commit: 1e8305031b175f9bb1c52b82b6ed4913e6108349
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 0%

---

# Panoramica dell’integrazione tra Adobe Advertising e Customer Journey Analytics

<!-- title? If I change, change refs throughout -->

*Inserzionisti con Advertising DSP e[!DNL Advertising Search, Social, & Commerce]*

Adobe Advertising è integrato con Adobe Customer Journey Analytics per estendere e migliorare le funzionalità di ciascun prodotto. Sono disponibili due opzioni per impostare l’integrazione:

* Gli inserzionisti con [!DNL Analytics for Advertising] e Customer Journey Analytics hanno le stesse funzionalità che hanno tramite [!DNL Analytics for Advertising], con l&#39;aggiunta di visualizzazioni in Customer Journey Analytics.

  Continuerai a tenere traccia degli eventi di click-through utilizzando Adobe Experience Platform Web SDK (`alloy.js`) o il servizio Adobe Experience Cloud Identity (`visitorAPI.js`). Gli inserzionisti con Advertising DSP continueranno a utilizzare uno snippet di JavaScript per monitorare gli eventi view-through. I dati disponibili in Customer Journey Analytics includono:

   * Dati sulle prestazioni della campagna da Adobe Advertising

   * Attività del sito e conversioni monitorate da [!DNL Google Ads], [!DNL Microsoft Advertising] e [!DNL Meta]

   * Dati di attribuzione da [!DNL Analytics], che possono essere utilizzati per l&#39;ottimizzazione e il reporting in Adobe Advertising

  In questo caso d&#39;uso, non è necessario eseguire alcun passaggio aggiuntivo, ad eccezione dell&#39;eventuale [raccolta di dati storici per gli AMO ID e gli EF ID da utilizzare in Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).

* (Prossima funzione beta) Gli inserzionisti con Customer Journey Analytics ma non con [!DNL Analytics for Advertising] possono scambiare in modo nativo i seguenti dati tra Adobe Advertising e Customer Journey Analytics tracciando gli eventi di click-through e view-through tramite Adobe Experience Platform Web SDK (`alloy.js`). I dati sono disponibili a livello di campagna, gruppo di annunci, pacchetto, posizionamento e parola chiave.

   * Dati sulle prestazioni della campagna da Adobe Advertising

     **Nota:** i dati di [!DNL Apple] e [!DNL Tiktok] non sono disponibili.

   * Attività del sito e conversioni monitorate da [!DNL Google Ads], [!DNL Microsoft Advertising] e [!DNL Meta]

   * Dati di attribuzione da Customer Journey Analytics, che possono essere utilizzati per l’ottimizzazione e il reporting in Adobe Advertising

  **Nota:** non sono ancora disponibili dati organici.<!-- Does that belong somewhere up above? -->

  In questo caso d&#39;uso, utilizzare Web SDK per tenere traccia degli eventi del sito (utilizzando cookie, indirizzi IP con hash o ID universali) e attribuire gli eventi del sito all&#39;attività paid media in [!DNL Google Ads], [!DNL Microsoft Advertising] e [!DNL Meta] e Adobe DSP. Per la raccolta dei dati verrà inoltre utilizzato Adobe Experience Platform.

## Come avviare un’integrazione nativa tra Adobe Advertising e Customer Journey Analytics

Contatta il team del tuo account Adobe, che completerà la configurazione iniziale necessaria per iniziare e ti aiuterà a pianificare l’implementazione e l’utilizzo dei dati in base alle esigenze della tua organizzazione.

>[!MORELIKETHIS]
>
>* [Prerequisiti](prerequisites.md)
>* (Utenti Adobe Analytics) [Raccogli i dati storici per gli AMO ID e gli EF ID da utilizzare in Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
