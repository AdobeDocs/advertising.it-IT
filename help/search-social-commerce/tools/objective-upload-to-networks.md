---
title: Abilita il caricamento degli obiettivi nelle reti di annunci
description: Scopri come caricare gli obiettivi per i portfolio ibridi in [!DNL Google Ads] e [!DNL Microsoft® Advertising].
exl-id: 09ab0b7a-b6ea-45ad-a82c-2c40d518d2e7
feature: Search Tools
source-git-commit: e8eabf7e4aa7c9201cd8198aae32d325b2858f2b
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# Abilita il caricamento degli obiettivi nelle reti di annunci

*Inserzionisti con [!DNL Google Ads] e [!DNL Microsoft® Advertising] solo account*

*Inserzionisti abilitati solo per l’ottimizzazione ibrida*

Se l&#39;account dell&#39;inserzionista è configurato per l&#39;utilizzo dell&#39;ottimizzazione ibrida, Adobi Advertising può facoltativamente caricare gli obiettivi per i portfolio dell&#39;account in [!DNL Google Ads] e [!DNL Microsoft® Advertising] come conversioni, in modo da poterle utilizzare per l’ottimizzazione ibrida.

L’abilitazione di questa opzione attiva automaticamente un caricamento per i portfolio che contengono campagne con strategie di offerta intelligenti. Search, Social e Commerce crea una conversione sulla rete di annunci per ogni combinazione di portfolio e obiettivo applicabile. Ogni conversione ha il nome `ACS_OBJ_SID_<portfolio_id>_<se_acctid/conversion_manager_se_acctid>`, dove `<portfolio_id>` è l’ID numerico del portfolio e `<se_acctid/conversion_manager_se_acctid>` è l&#39;ID numerico dell&#39;account di ad network o dell&#39;account manager. La conversione rappresenta tutte le metriche di conversione ponderate nell’obiettivo.

Carica in [!DNL Google Ads] si verifica ogni giorno alle 06:00 nel fuso orario dell&#39;inserzionista. Carica in [!DNL Microsoft® Advertising] si verifica ogni giorno alle 09:00 nel fuso orario dell&#39;inserzionista.

<!-- Note to self: Conversions tracked by Google Ads and by the Microsoft Advertising universal event tracking (UET) tag aren't re-uploaded to the ad networks. -->

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. Seleziona la casella di controllo accanto a **[!UICONTROL Enable Objective Upload]**.

   Questa opzione è disponibile solo se l’account dell’inserzionista è configurato per l’utilizzo dell’ottimizzazione ibrida. Per abilitare l’ottimizzazione ibrida, contatta il team del tuo account Adobe.

1. (Per gli inserzionisti che [!DNL Google Ads] account che svolgono attività commerciali nello Spazio economico europeo (SEE) o nel Regno Unito (UK); facoltativo) Se hai raccolto il consenso degli utenti di EEA e UK a caricare i loro dati a scopo pubblicitario, seleziona la casella di controllo accanto a **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. Clic **[!UICONTROL Save]**.

1. (Se le conversioni vengono tracciate a livello di account manager) [Aggiungi le credenziali per l’account manager](/help/search-social-commerce/admin/manager-accounts.md) a **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

>[!MORELIKETHIS]
>
>* [Informazioni sulla gestione delle metriche di conversione di un inserzionista](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [Carica metriche di conversione in [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
