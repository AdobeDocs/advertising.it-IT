---
title: Enable uploading of objectives to ad networks
description: Learn how to upload objectives for your hybrid portfolios to [!DNL Google Ads] e [!DNL Microsoft Advertising].
exl-id: 09ab0b7a-b6ea-45ad-a82c-2c40d518d2e7
feature: Search Tools
source-git-commit: 803f1ad2ad5be005b7dab467efbeb1c4ceaa7559
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 0%

---

# Enable uploading of objectives to ad networks

*Inserzionisti con [!DNL Google Ads] e [!DNL Microsoft Advertising] solo account*

*Inserzionisti abilitati solo per l&#39;ottimizzazione ibrida*

Search, Social &amp; Commerce può caricare gli obiettivi per i portafogli di un inserzionista account e [!DNL Google Ads] [!DNL Microsoft Advertising] quindi utilizzarli per l&#39;ottimizzazione ibrida. Gli obiettivi caricati sono disponibili come azioni di conversione per obiettivi di conversione personalizzati a livello di account e di campagna.

L&#39;attivazione di questa opzione attiva automaticamente il caricamento di obiettivi nei portfolio che contengono campagne con strategie di offerta intelligente. Search, Social &amp; Commerce crea una conversione sul network pubblicitario per ogni obiettivo applicabile. La conversione rappresenta tutte le metriche di conversione ponderate nell&#39;obiettivo. Ogni conversione ha uno dei seguenti nomi:

* `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`

  dove `<network_ID>` è l&#39;ID numerico che Search, Social &amp; Commerce utilizza per il network pubblicitario, `<objective_id>` è l&#39;ID obiettivo numerico e `<network_account_ID>` è l&#39;ID numerico per il network pubblicitario account o il gestore account.

* (Old format that will be deprecated in the future) `ACS_OBJ_SID_<portfolio_id>_<se_acctid/conversion_manager_se_acctid>`

  where `<portfolio_id>` is the numeric portfolio ID and `<se_acctid/conversion_manager_se_acctid>` is the numeric ID for the ad network account or manager account.

  Your Adobe Account Team will work with you to migrate your existing conversion action names within the ad network before the old format is deprecated. During the migration period, both the old and new format uploads will run in parallel. Modelling and optimization aren&#39;t affected because the new conversion actions initially appear with &quot;secondary&quot; (not optimized) status and with 90 days of backfill data.

I caricamenti devono avvenire tutti i [!DNL Google Ads] giorni alle 06:00 nella zona di fuso orario dell&#39;inserzionista. I caricamenti devono avvenire tutti i [!DNL Microsoft Advertising] giorni alle 09:00 nella zona di fuso orario dell&#39;inserzionista.

>[!IMPORTANT]
>
>Le conversioni monitorate da Google Ads e dall&#39;tag Microsoft Advertising Universal Event Tracking (UET) non vengono ricaricate sulle reti annuncio. Se li includi in un obiettivo, aggiungili agli obiettivi della campagna entro il editor del network pubblicitario.

<!--
>[!IMPORTANT]
>
>Objectives for hybrid portfolios may include conversion goals from multiple ad networks and other types of conversion metrics. However, the individual campaigns in the portfolio can't include conversion goals that aren't included in the portfolio's objective; using additional conversion goals may impact portfolio performance.
-->

<!-- Can conversions from events triggered on other ad networks be included in the portfolio (and just be ignored)? -->

1. Nel menu principale, fare clic su **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. Selezionare la casella di controllo accanto a **[!UICONTROL Enable Objective Upload]**.

1. (Inserzionisti con [!DNL Google Ads] account che operano nello Spazio economico europeo (EEA) o nel Regno Unito (UK); facoltativo) Se hai raccolto il consenso degli utenti EEA e del Regno Unito per caricare i loro dati per scopi pubblicitari, seleziona la casella di controllo accanto a **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. Fare clic su **[!UICONTROL Save]**.

1. (If your conversions are tracked at a manager account level) [Add credentials for your manager account](/help/search-social-commerce/admin/manager-accounts.md) at **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. Verify that each objective — named `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>` — appears within two days on the ad network.

   In [!DNL Google Ads] editor, look up your [conversion actions](https://support.google.com/google-ads/answer/11461796). In [!DNL Microsoft Advertising] editor, look up your [conversion goals](https://help.ads.microsoft.com/#apex/ads/en/56709).

   Se necessario, aggiorna l&#39;intervallo di date per includere la data di caricamento.

## Risoluzione dei problemi relativi agli obiettivi mancanti

Se l&#39;obiettivo, denominato `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>` , per uno dei tuoi portafogli non viene visualizzato nella network pubblicitario, controlla quanto segue:

* ([!DNL Google Ads]) Controlla se le conversioni devono essere caricate a livello di account o di manager. Se devono essere caricati a livello di manager:

   * Verificare se le credenziali per il [!DNL Google Ads] account di gestione sono fornite in > **[!UICONTROL Search][!UICONTROL Admin] >[!UICONTROL Manager Accounts]**. Se necessario, [aggiungere le credenziali per il gestore account](/help/search-social-commerce/admin/manager-accounts.md).

   * Controlla se il network pubblicitario account include già lo stesso nome della metrica. If it does, then rename the metric so that the correct manager-level property can be created.

* Check that the portfolio&#39;s &quot;hybrid&quot; option is selected and that the objective has valid revenue.

>[!MORELIKETHIS]
>
>* [About managing an advertiser&#39;s conversion metrics](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [Upload conversion metrics to [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
