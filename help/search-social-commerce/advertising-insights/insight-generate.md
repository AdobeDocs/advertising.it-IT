---
title: Genera un [!DNL Advertising Insight]
description: Scopri come creare un  [!DNL Advertising Insight].
exl-id: e6b692be-189e-4c6c-a536-e6c78801853d
feature: Search Advertising Insights
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 0%

---

# Genera un [!DNL Advertising Insight]

1. Nel menu principale, fare clic su **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Advertising Insights]**.

2. Fai clic sull’insight da generare.

3. Specifica le impostazioni di insight:

   1. (Alcuni rapporti; facoltativo) Specifica gli intervalli di date per insight.

   2. (Maggior numero di approfondimenti) Seleziona il portfolio da analizzare.

      In generale, sono disponibili tutti i portfolio ottimizzati e attivi che contengono campagne attive. Per alcuni approfondimenti, puoi filtrare l&#39;elenco dei portfolio per includere **[!UICONTROL Only Optimized Portfolios]**.

      Per [!UICONTROL Day of Week] approfondimenti, sono disponibili solo i portfolio che hanno una spesa sufficiente e che sono stati utilizzati anche per il targeting negli ultimi due giorni.

   3. ([!UICONTROL Event Path Beta] solo insight) Effettuare le seguenti operazioni:

      1. Selezionare **[!UICONTROL Operation]**: *[!UICONTROL Extract events]* (per caricare un [!UICONTROL Channel Assist Report] o [!UICONTROL Campaign Assist Report] e classificare gli eventi utente in gruppi distinti per l&#39;analisi) o *[!UICONTROL Analyze classified events]* (per caricare gruppi di eventi e utilizzarli per generare insight).

      1. Fare clic su **[!UICONTROL Select]** per individuare un file in formato XLSX e ZIP (XLSX compresso), quindi fare clic su **[!UICONTROL Upload]**.

   4. ([!UICONTROL Google Account Audit] solo insight) Effettuare le seguenti operazioni:

      1. Immettere **[!UICONTROL Advertiser Name]** e **[!UICONTROL Account Name]**.

      1. Selezionare **[!UICONTROL Account Currency]**, **[!UICONTROL File Format Region]** (*[!UICONTROL United States]* o *[!UICONTROL United Kingdom]*) e **[!UICONTROL Output Language]** (*[!UICONTROL English (USA)]*, *[!UICONTROL French]* o *[!UICONTROL German]*).

      1. Fare clic su **[!UICONTROL Select]** per individuare i report di campagne, parole chiave e cronologia modifiche scaricati per l&#39;account dall&#39;interfaccia utente Web di [!DNL Google Ads] e un file di bulksheet scaricato per l&#39;account dall&#39;applicazione di [!DNL Google Ads Editor]. Quindi fare clic su **[!UICONTROL Upload]**.

         Tutti i file devono essere in formato CSV, TSV, TXT o ZIP (CSV, TSV o TXT compresso).

   5. ([!UICONTROL Location Target Performance] solo insight; facoltativo) Per aggregare i dati ogni giorno anziché come riepilogo, selezionare **[!UICONTROL Time Aggregation]** di *[!UICONTROL Daily]*.

   6. ([!UICONTROL Normalized Sim (Combined)] solo insight) Effettuare le seguenti operazioni:

      1. Nel campo **[!UICONTROL Step]**, specificare il numero di livelli di spesa target, o passaggi, da includere nell&#39;insight. Il valore può essere compreso tra 3 e 100.

      1. Nel campo **[!UICONTROL Type]**, selezionare il tipo di simulazione:

         * *[!UICONTROL Optimized Multi-portfolio]*: genera una singola simulazione in più portfolio con lo stesso obiettivo e la stessa valuta.

         * *[!UICONTROL Individual Normalized]*: genera una singola simulazione per ogni portfolio selezionato. I portafogli possono avere obiettivi e valute diversi.

   7. ([!UICONTROL Portfolio Launch] solo insight; facoltativo) Per specificare una data di avvio futura, specificare una data nel campo **[!UICONTROL Optional Date]**.

   8. ([!UICONTROL Quality Score] solo insight) Seleziona la rete di annunci applicabile.

   9. ([!UICONTROL Query Cross Matching] solo insight) Nel menu **[!UICONTROL Google Accounts]**, seleziona l&#39;account.

4. Fare clic su **[!UICONTROL Generate Insight]**.

   Ricevi una notifica quando il processo viene completato o non riesce in base alle [impostazioni di notifica configurate](/help/search-social-commerce/notifications/notification-edit.md) per [!UICONTROL Advertising Insights].

>[!MORELIKETHIS]
>
>* [Informazioni su [!UICONTROL Advertising Insights]](insight-about.md)
>* [Visualizza o salva un [!DNL Advertising Insight]](insight-view-save.md)
>* [Elimina un [!DNL Advertising Insight]](insight-delete.md)
