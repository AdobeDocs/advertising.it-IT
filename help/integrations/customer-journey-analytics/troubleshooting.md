---
title: Risoluzione dei problemi dei dati di Adobe Advertising in Customer Journey Analytics
description: Scopri come risolvere i problemi relativi ai dati di Adobe Advertising in Customer Journey Analytics.
feature: Integration with Adobe Customer Journey Analytics
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
source-git-commit: d78aa2f6596190b644d9f920f51c179e43e86317
workflow-type: tm+mt
source-wordcount: 611
ht-degree: 0%

---

# Risoluzione dei problemi dei dati di Adobe Advertising in Customer Journey Analytics

Di seguito sono riportati i potenziali problemi e le relative cause.

## Reporting di riepilogo

+++ Non sono disponibili dati di reporting di riepilogo in Customer Journey Analytics per Advertising DSP o Advertising Search, Social e Commerce.

Verifica quanto segue:

* Il feed da Adobe Advertising a Customer Journey Analytics è abilitato. Rivolgiti al team del tuo account Adobe.

* Il set di dati di dimensione/classificazione/ricerca di Adobe Advertising e il set di dati di riepilogo sono inclusi nella connessione Customer Journey Analytics.

* Le dimensioni di Adobe Advertising e le metriche di riepilogo sono incluse nella visualizzazione dati di Customer Journey Analytics.

* Customer Journey Analytics Workspace fa riferimento alla visualizzazione dati corretta.

Se verifichi tutte le impostazioni precedenti ma non trovi ancora i dati di riepilogo, apri un ticket di supporto per la tua organizzazione all&#39;indirizzo [https://experienceleague.adobe.com/home?lang=it#support](https://experienceleague.adobe.com/home?lang=it&support-tab=home#support).
.

+++

+++ I dati dei rapporti di riepilogo sono disponibili in Customer Journey Analytics per l’inserzionista 1 ma non per l’inserzionista 2.

Verifica che il feed da Adobe Advertising a Customer Journey Analytics sia abilitato per l’inserzionista 2. Rivolgiti al team del tuo account Adobe.

Se il feed è abilitato per un inserzionista ma i dati di riepilogo non sono ancora visualizzati, apri un ticket di supporto per l&#39;organizzazione all&#39;indirizzo [https://experienceleague.adobe.com/home?lang=it#support](https://experienceleague.adobe.com/home?lang=it&support-tab=home#support).
.

+++

+++ (Utenti Search, Social e Commerce) In Customer Journey Analytics sono disponibili dati di riepilogo per un account [!DNL Google Ads], [!DNL Meta Ads] o [!DNL Microsoft Advertising], ma non per un altro account.

Verifica che il feed da Adobe Advertising a Customer Journey Analytics sia abilitato per l’account di rete dell’annuncio specifico. Rivolgiti al team del tuo account Adobe.

Se il feed è abilitato per un account ma non vengono ancora visualizzati i dati di riepilogo, aprire un ticket di supporto per l&#39;organizzazione all&#39;indirizzo [https://experienceleague.adobe.com/home?lang=it#support](https://experienceleague.adobe.com/home?lang=it&support-tab=home#support). Includi [!UICONTROL Account ID] per l&#39;account di rete dell&#39;annuncio.
.

+++

+++ I dati dei rapporti di riepilogo in Customer Journey Analytics Workspace sono diversi da quelli presenti in Advertising DSP o Advertising Search, Social e Commerce, oppure mancano dati di riepilogo per alcune campagne ed entità campagne.

Verifica quanto segue:

* Stai utilizzando gli stessi intervalli di date sia in [!DNL Workspace] che nel rapporto di Adobe Advertising.

* Tutti i filtri e i segmenti applicati in [!DNL Workspace] e nel report Adobe Advertising non causano differenze nei dati.

Se sei sicuro di una discrepanza di dati, apri un ticket di supporto per la tua organizzazione all&#39;indirizzo [https://experienceleague.adobe.com/home?lang=it#support](https://experienceleague.adobe.com/home?lang=it&support-tab=home#support). Includi [!UICONTROL Account ID] per l&#39;account di rete dell&#39;annuncio.
. Includi schermate e fogli di calcolo per mostrare le prove della discrepanza. Se necessario, il team del tuo account Adobe può correggere retroattivamente il feed di dati per risolvere la discrepanza.

+++

## Reporting a livello di evento

+++ Scenario: i dati di conversione (ad esempio `Page Views`) non sono disponibili per una dimensione di reporting (ad esempio `Campaign`) in CJA Customer Journey Analytics Workspace.

Verifica quanto segue, iniziando dagli articoli con il minor numero di barriere:

* Le metriche di conversione applicabili sono eventi web/online, che Adobe Advertising può attribuire alle dimensioni.

* Stai utilizzando la visualizzazione dati corretta.

* Adobe Advertising tiene traccia dei click-through e dei view-through sul sito applicabile. <!-- Link to validation instructions in the user guide -->

* Nella connessione Customer Journey Analytics per il set di dati delle classificazioni, i valori per le impostazioni [!DNL Key] e [!DNL Matching Key] sono corretti: [!DNL Key]: `Tracking Code` (_customername.adLens2.trackingCode), [!DNL Matching Key]: `Tracking Code` (event._experience.adcloud.conversionDetails.trackingCode)

* Il servizio [!DNL Adobe Advertising] è stato aggiunto allo stream di dati di Adobe Experience Platform, lo schema mappato per lo stream di dati è `XDM ExperienceEvent Schema` e il gruppo di campi `Adobe Advertising Cloud ExperienceEvent Full Extension` è stato aggiunto allo schema.

* Le impostazioni di Adobe Advertising sono configurate correttamente nell’estensione WebSDK e pubblicate.

Se verifichi tutte le impostazioni di cui sopra ma non visualizzi ancora i dati di conversione, apri un ticket di supporto per la tua organizzazione all&#39;indirizzo [https://experienceleague.adobe.com/home?lang=it#support](https://experienceleague.adobe.com/home?lang=it&support-tab=home#support). Includi [!UICONTROL Account ID] per l&#39;account di rete dell&#39;annuncio.
.

+++


<!--

+++ Question

Answer

+++

+++ Question

Answer

+++

+++ Question

Answer

+++

-->

>[!MORELIKETHIS]
>
>* [Panoramica](overview.md)
>* [ID Adobe Advertising utilizzati da [!DNL Customer Journey Analytics]](ids.md)
>* [Prerequisiti](prerequisites.md)
>* [Imposta raccolta dati, trasferimento dati e reporting](set-up.md)
>* [Metriche e dimensioni di Adobe Advertising in Customer Journey Analytics](advertising-data-in-cja.md)
>* (Utenti Adobe Analytics) [Raccogli dati storici per gli AMO ID e gli EF ID da utilizzare in Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
