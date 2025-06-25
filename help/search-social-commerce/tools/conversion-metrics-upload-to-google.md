---
title: Carica metriche di conversione tracciate da Ricerca, Social e Commerce in [!DNL Google Ads]
description: Scopri come caricare in  [!DNL Google Ads] le metriche di conversione tracciate da Search, Social e Commerce.
exl-id: 976792ae-135c-4790-82cf-9503edb93fb1
feature: Search Tools
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# Carica metriche di conversione di ricerca, social e Commerce in [!DNL Google Ads]

*Inserzionisti con [!DNL Google Ads] account e solo il monitoraggio delle conversioni di Adobe Advertising*

Search, Social e Commerce possono facoltativamente caricare in [!DNL Google Ads] tutte le metriche di conversione di cui tiene traccia per le campagne [!DNL Google Ads] che utilizzano il servizio di tracciamento delle conversioni di Adobe Advertising. Questa opzione non rende le conversioni disponibili per l’ottimizzazione ibrida. Se desideri utilizzare le conversioni Adobe per l&#39;ottimizzazione ibrida, consulta &quot;[Abilitare il caricamento di obiettivi nelle reti di annunci](objective-upload-to-networks.md).&quot;

Gli upload giornalieri includono il valore `gclid` tracciato, il valore di conversione definito utilizzando il modello di attribuzione a livello di inserzionista e la marca temporale. Se il modello di attribuzione viene aggiornato, il caricamento successivo utilizza il nuovo modello, ma i dati passati non vengono aggiornati per l’utilizzo del nuovo modello.

>[!NOTE]
>
>I caricamenti non includono le metriche di conversione caricate su Adobe Advertising dai file di feed.

1. Nel menu principale, fare clic su **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. Selezionare la casella di controllo accanto a **[!UICONTROL Upload Conversions to Google Ads]**.

1. (Inserzionisti che svolgono attività commerciali nello Spazio economico europeo (SEE) o nel Regno Unito (UK); facoltativo) Se hai raccolto il consenso degli utenti di EEA e UK a caricare i loro dati a scopo pubblicitario, seleziona la casella di controllo accanto a **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. Fare clic su **[!UICONTROL Save]**.

1. (Se le conversioni vengono tracciate a livello di account manager) [Aggiungi le credenziali per l&#39;account manager](/help/search-social-commerce/admin/manager-accounts.md) alle **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

>[!MORELIKETHIS]
>
>* [Abilita il caricamento degli obiettivi nelle reti di annunci](objective-upload-to-networks.md)
