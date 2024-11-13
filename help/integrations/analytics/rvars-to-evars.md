---
title: Raccogliere dati storici per AMO ID e EF ID da utilizzare in Adobe Customer Journey Analytics
description: Scopri come raccogliere dati storici per le variabili riservate in Adobe Analytics per utilizzi futuri in Adobe Customer Journey Analytics
feature: Integration with Adobe Analytics
source-git-commit: 4cd58fd995b3df9fb7837077108207ce910157c1
workflow-type: tm+mt
source-wordcount: '605'
ht-degree: 0%

---

# Raccogliere dati storici per AMO ID e EF ID da utilizzare in Adobe Customer Journey Analytics

*Inserzionisti con [!DNL Analytics for Advertising] e solo Adobe Customer Journey Analytics*

Se si utilizzano variabili riservate per acquisire l&#39;AMO ID [e l&#39;EF ID](ids.md) per l&#39;integrazione di [!DNL Analytics for Advertising], è possibile prepararsi per una futura integrazione tra Adobe Advertising e [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview), che è la soluzione di Adobe [!DNL analytics] di nuova generazione, copiando al più presto le variabili riservate per l&#39;AMO ID e l&#39;EF ID in [standard [!DNL eVars]](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/evar). In questo modo sarà possibile raccogliere i dati storici per gli AMO ID e gli EF ID non appena si completa l’attività. Il team dell’account Adobe ti informerà se utilizzi variabili riservate e se devi completare questa attività.

<!-- You can also do the same for any other reserved variables you use for your [!DNL Analytics for Advertising] implementation. -->

<!-- This will allow Adobe Experience Platform, which supplies data to Customer Journey Analytics, to begin collecting historical data for your [!DNL rVars] as soon as you complete the task. -->

## Perché devo raccogliere i dati storici per il Customer Journey Analytics?

Customer Journey Analytics consente di sincronizzare i dati da Adobe Experience Platform ad Adobe Analytics Analysis Workspace. Attualmente, [!DNL Analytics Data Connector] ad Experience Platform non invia i dati per le variabili riservate da [!DNL Analytics] ad Experience Platform. Di conseguenza, i dati per gli AMO ID e gli EF ID acquisiti da variabili riservate non sono attualmente disponibili all’interno del Customer Journey Analytics. <!-- Instead, XXXXXXXXXX what exactly? -->.<!-- Does the Analytics for Advertising implementation use the Analytics Data Connector in particular (why would it use anything?), and we're planning to implement the Web SDK to do it instead in the future? -->

Adobe Advertising sta pianificando una futura implementazione con il Customer Journey Analytics. Una volta rilasciata l&#39;implementazione, per l&#39;integrazione di [!DNL Analytics for Advertising] sarà comunque necessario raccogliere i dati di click-through e i dati di view-through (utenti DSP) utilizzando il tracciamento di [!DNL Analytics]. Tuttavia, se l&#39;organizzazione dispone di entrambi i prodotti, sarà possibile visualizzare i dati sia nel Customer Journey Analytics <!-- (Analysis Workspace using data from Experience Platform)--> [!DNL Analytics] che nel gruppo <!-- (Analysis Workspace using data from [!DNL Analytics]) --> {1\). Quando la funzione viene rilasciata, Experience Platform inizierà a raccogliere i dati per l’AMO ID e l’EF ID per l’utilizzo nel Customer Journey Analytics, ma non esisteranno dati storici precedenti alla data di rilascio.

Tuttavia, puoi iniziare a raccogliere i dati per gli AMO ID e gli EF ID <!-- [!DNL rVars] --> prima creando una semplice [[!DNL Analytics] regola di elaborazione](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/processing-rules) per copiare gli AMO ID e gli EF ID <!-- [!DNL rVars] --> in [!DNL eVars] ora. Dopo aver creato la regola di elaborazione, inizierai ad accantonare i dati per gli AMO ID e gli EF ID <!-- [!DNL rVars] --> non appena tengono traccia dei nuovi eventi. I dati storici saranno quindi disponibili entro il Customer Journey Analytics una volta che l’implementazione sarà disponibile.

>[!NOTE]
>
>Le regole di elaborazione vengono applicate solo ai nuovi dati ricevuti. Non lavorano retroattivamente per raccogliere dati passati.

## Copia le variabili riservate per AMO ID e EF ID in [!DNL eVars]

Questo passaggio è manuale e deve essere completato per ogni suite di rapporti che tiene traccia degli AMO ID e degli EF ID <!-- [!DNL rVars] --> che si prevede di integrare con Adobe Advertising in futuro.

1. [Creare una regola di elaborazione](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/t-processing-rules) con le impostazioni seguenti:

   * Selezionare la suite di rapporti per la quale si desidera eseguire la migrazione dei dati dell’AMO ID e dell’EF ID <!-- [!DNL rVar] --> in Experience Platform per l’utilizzo da parte del Customer Journey Analytics.

   * Per [!UICONTROL Rule Title], utilizza un nome descrittivo, ad esempio &quot;Copy AMO ID and EF ID to eVars&quot;.

   * Nella sezione [!UICONTROL Always Execute], aggiungi due azioni per creare le nuove eVar:

      * Per `AMO ID`: ```Overwrite value of <new/unused eVar> with amo.s_kwcid(Context Data)```

      * Per `EF ID`: ```Overwrite value of <new/unused eVar> With amo.ef_id(Context Data)```

   * Per [!UICONTROL Reason for rule], utilizza una nota descrittiva, ad esempio &quot;AMO ID e EF ID verranno trasportati ad AEP tramite il connettore Adobe Analytics&quot;.

1. Convalida la regola di elaborazione salvata.

   Dopo aver salvato la regola di elaborazione, i dati per `AMO ID` e `AMO EF ID` <!-- the existing reserved variables --> devono essere identici ai dati per le due nuove eVar in cui vengono copiati.

   Se ad esempio il nuovo eVar `eVar142` è mappato a `amo.s_kwcid(Context Data)`, i dati per `eVar142` e `AMO ID` devono essere identici.

Per ulteriori informazioni sull&#39;applicazione delle regole di elaborazione, vedere &quot;[Funzionamento delle regole di elaborazione](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/processing-rules-about).&quot;

>[!MORELIKETHIS]
>
>* [Panoramica di [!DNL Analytics for Advertising]](overview.md)
