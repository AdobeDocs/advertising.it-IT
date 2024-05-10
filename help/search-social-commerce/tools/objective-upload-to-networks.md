---
title: Abilita il caricamento degli obiettivi nelle reti di annunci
description: Scopri come caricare gli obiettivi per i portfolio ibridi in [!DNL Google Ads] e [!DNL Microsoft® Advertising].
exl-id: 09ab0b7a-b6ea-45ad-a82c-2c40d518d2e7
feature: Search Tools
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---

# Abilita il caricamento degli obiettivi nelle reti di annunci

*Inserzionisti con [!DNL Google Ads] e [!DNL Microsoft® Advertising] solo account*

*Inserzionisti abilitati solo per l’ottimizzazione ibrida*

Search, Social e Commerce possono caricare gli obiettivi per i portfolio di un account inserzionista in [!DNL Google Ads] e [!DNL Microsoft® Advertising] in modo da poterle utilizzare per l’ottimizzazione ibrida. Gli obiettivi caricati sono disponibili come azioni di conversione per gli obiettivi di conversione personalizzati a livello di account e di campagna.

L’abilitazione di questa opzione attiva automaticamente un caricamento per gli obiettivi nei portfolio che contengono campagne con strategie di offerta intelligenti. Search, Social e Commerce creano una conversione sulla rete di annunci per ogni obiettivo applicabile. La conversione rappresenta tutte le metriche di conversione ponderate nell’obiettivo. Ciascuna conversione ha uno dei seguenti nomi:

* `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`

  dove `<network_ID>` è l’ID numerico utilizzato da Search, Social e Commerce per la rete di annunci, `<objective_id>` è l&#39;ID obiettivo numerico, e `<network_account_ID>` è l&#39;ID numerico dell&#39;account di ad network o dell&#39;account manager.

* (Vecchio formato che in futuro diventerà obsoleto) `ACS_OBJ_SID_<portfolio_id>_<se_acctid/conversion_manager_se_acctid>`

  dove `<portfolio_id>` è l’ID numerico del portfolio e `<se_acctid/conversion_manager_se_acctid>` è l&#39;ID numerico dell&#39;account di ad network o dell&#39;account manager.

  Il team dell’account Adobe collaborerà con te per migrare i nomi delle azioni di conversione esistenti all’interno della rete di annunci prima che il vecchio formato venga dichiarato obsoleto. Durante il periodo di migrazione, i caricamenti del vecchio e del nuovo formato verranno eseguiti in parallelo. La modellazione e l’ottimizzazione non sono interessate, perché le nuove azioni di conversione appaiono inizialmente con lo stato &quot;secondario&quot; (non ottimizzato) e con 90 giorni di dati di retrocompilazione.

Carica in [!DNL Google Ads] si verifica ogni giorno alle 06:00 nel fuso orario dell&#39;inserzionista. Carica in [!DNL Microsoft® Advertising] si verifica ogni giorno alle 09:00 nel fuso orario dell&#39;inserzionista.

>[!IMPORTANT]
>
>Le conversioni tracciate da Google Ads e dal tag UET (Universal Event Tracking) di Microsoft Advertising non vengono ricaricate nelle reti di annunci. Se li includi all’interno di un obiettivo, aggiungili agli obiettivi della campagna nell’editor della rete di annunci.

<!--
>[!IMPORTANT]
>
>Objectives for hybrid portfolios may include conversion goals from multiple ad networks and other types of conversion metrics. However, the individual campaigns in the portfolio can't include conversion goals that aren't included in the portfolio's objective; using additional conversion goals may impact portfolio performance.
-->

<!-- Can conversions from events triggered on other ad networks be included in the portfolio (and just be ignored)? -->

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. Seleziona la casella di controllo accanto a **[!UICONTROL Enable Objective Upload]**.

1. (Per gli inserzionisti che [!DNL Google Ads] account che svolgono attività commerciali nello Spazio economico europeo (SEE) o nel Regno Unito (UK); facoltativo) Se hai raccolto il consenso degli utenti di EEA e UK a caricare i loro dati a scopo pubblicitario, seleziona la casella di controllo accanto a **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. Clic **[!UICONTROL Save]**.

1. (Se le conversioni vengono tracciate a livello di account manager) [Aggiungi le credenziali per l’account manager](/help/search-social-commerce/admin/manager-accounts.md) a **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

Al termine del caricamento giornaliero, puoi verificare che le azioni di conversione vengano visualizzate nella rete di annunci.

>[!MORELIKETHIS]
>
>* [Informazioni sulla gestione delle metriche di conversione di un inserzionista](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [Carica metriche di conversione in [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
