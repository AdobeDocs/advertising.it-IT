---
title: Prerequisiti per l’integrazione di Adobe Advertising con Customer Journey Analytics
description: Prerequisiti per l’integrazione di Adobe Advertising con Customer Journey Analytics
feature: Integration with Adobe Customer Journey Analytics
exl-id: 4bd14178-5003-4da6-9034-d070c57f0e9b
source-git-commit: ba23ab97c916f829cf9d640669423dd8e72949c0
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%

---

# Prerequisiti per l’integrazione di Adobe Advertising con Customer Journey Analytics

*Inserzionisti con Advertising DSP e[!DNL Advertising Search, Social, & Commerce]*

Leggi le seguenti informazioni prima di integrare Adobe Advertising con Adobe Customer Journey Analytics.

## Requisiti per la generazione di rapporti sui dati di Adobe Advertising in Customer Journey Analytics

* Inserzionisti con [!DNL Analytics for Advertising] e Customer Journey Analytics:

   * Adobe Customer Journey Analytics<!-- any specific version? -->

   * [Tutti gli altri prerequisiti per [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md).

* Inserzionisti con Customer Journey Analytics ma non [!DNL Analytics for Advertising]:

   * Libreria Adobe Experience Platform Web SDK: `alloy.js`

     [!DNL Org ID] utilizzato per Web SDK e per l&#39;account dell&#39;inserzionista Adobe Advertising deve essere lo stesso. Puoi trovare questo ID nella scheda [Riepilogo di Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html?lang=it).

     ![Schermata Riepilogo di Experience Cloud Debugger](/help/integrations/assets/a4adc-debugger-summary.png)

     Per creare uno stream di dati Experience Platform e uno schema XDM è necessario l’assistenza dell’amministratore del sito Experience Platform.

   * Adobe Customer Journey Analytics<!-- any specific version? -->

     Per impostare una connessione al set di dati e configurare la generazione rapporti è necessario il supporto dell’analista web interno.

>[!TIP]
>
>Per migliorare la fedeltà dei dati, utilizza la versione più recente di ciascuna libreria.

>[!MORELIKETHIS]
>
>* [Panoramica](overview.md)
>* (Utenti Adobe Analytics) [Raccogli i dati storici per gli AMO ID e gli EF ID da utilizzare in Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
