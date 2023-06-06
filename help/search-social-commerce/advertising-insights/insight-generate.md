---
title: Genera un [!DNL Advertising Insight]
description: Scopri come creare un [!DNL Advertising Insight].
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# Genera un [!DNL Advertising Insight]

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Advertising Insights]**.

2. Fai clic sull’informazione che desideri generare.

3. Specifica le impostazioni di approfondimento:

   1. (Alcuni rapporti; facoltativo) Specifica gli intervalli di date per l’approfondimento.

   2. (Maggior numero di approfondimenti) Seleziona il portfolio da analizzare.

      In generale, sono disponibili tutti i portfolio ottimizzati e attivi che contengono campagne attive. Per alcune informazioni, puoi filtrare l’elenco dei portfolio per includere **[!UICONTROL Only Optimized Portfolios]**.

      Per [!UICONTROL Day of Week] approfondimenti, sono disponibili solo i portfolio che hanno una spesa sufficiente e che sono stati utilizzati anche per il targeting negli ultimi due giorni.

   3. ([!UICONTROL Event Path Beta] solo approfondimenti) Effettua le seguenti operazioni:

      1. Seleziona la **[!UICONTROL Operation]**: *[!UICONTROL Extract events]* (per caricare una [!UICONTROL Channel Assist Report] o [!UICONTROL Campaign Assist Report] e classificare gli eventi utente in gruppi distinti per l&#39;analisi) o *[!UICONTROL Analyze classified events]* (per caricare gruppi di eventi e utilizzarli per generare insight).

      1. Clic **[!UICONTROL Select]** per individuare un file in formato XLSX e ZIP (XLSX compresso), quindi fare clic su **[!UICONTROL Upload]**.
   4. ([!UICONTROL Google Account Audit] solo approfondimenti) Effettua le seguenti operazioni:

      1. Inserisci il **[!UICONTROL Advertiser Name]** e **[!UICONTROL Account Name]**.

      1. Seleziona la **[!UICONTROL Account Currency]**, **[!UICONTROL File Format Region]** (*[!UICONTROL United States]* o *[!UICONTROL United Kingdom]*) e **[!UICONTROL Output Language]** (*[!UICONTROL English (USA)]*, *[!UICONTROL French]*, o *[!UICONTROL German]*).

      1. Clic **[!UICONTROL Select]** per individuare i report campagna, parola chiave e cronologia modifiche scaricati per l&#39;account da [!DNL Google Ads] l&#39;interfaccia utente web e un file di bulksheet scaricato per l&#39;account da [!DNL Google Ads Editor] applicazione. Quindi fai clic su **[!UICONTROL Upload]**.

         Tutti i file devono essere in formato CSV, TSV, TXT o ZIP (CSV, TSV o TXT compresso).
   5. ([!UICONTROL Location Target Performance] solo approfondimenti; facoltativo) Per aggregare i dati quotidianamente anziché come riepilogo, seleziona la **[!UICONTROL Time Aggregation]** di *[!UICONTROL Daily]*.

   6. ([!UICONTROL Normalized Sim (Combined)] solo approfondimenti) Effettua le seguenti operazioni:

      1. In **[!UICONTROL Step]** , specificare il numero di livelli di spesa target, o passaggi, da includere nell&#39;approfondimento. Il valore può essere compreso tra 3 e 100.

      1. In **[!UICONTROL Type]** , selezionare il tipo di simulazione:

         * *[!UICONTROL Optimized Multi-portfolio]*: genera una singola simulazione su più portfolio con lo stesso obiettivo e la stessa valuta.

         * *[!UICONTROL Individual Normalized]*: genera una singola simulazione per ciascun portfolio selezionato. I portafogli possono avere obiettivi e valute diversi.
   7. ([!UICONTROL Portfolio Launch] solo approfondimenti; facoltativo) Per specificare una data di lancio futura, specifica una data in **[!UICONTROL Optional Date]** campo.

   8. ([!UICONTROL Quality Score] solo approfondimenti) Seleziona la rete di annunci applicabile.

   9. ([!UICONTROL Query Cross Matching] solo approfondimenti) In **[!UICONTROL Google Accounts]** selezionare l&#39;account.




4. Clic **[!UICONTROL Generate Insight]**.

   Riceverai una notifica quando il processo viene completato o non riesce in base al tuo [impostazioni di notifica configurate](/help/search-social-commerce/notifications/notification-edit.md) per [!UICONTROL Advertising Insights].

>[!MORELIKETHIS]
>
>* [Informazioni su [!UICONTROL Advertising Insights]](insight-about.md)
>* [Visualizza o salva un [!DNL Advertising Insight]](insight-view-save.md)
>* [Eliminare un [!DNL Advertising Insight]](insight-delete.md)

