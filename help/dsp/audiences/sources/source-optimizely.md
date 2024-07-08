---
title: Converti ID utente da [!DNL Optimizely] a ID universali
description: Scopri come abilitare DSP per l'assimilazione [!DNL Optimizely] dei segmenti di prime parti.
feature: DSP Audiences
exl-id: 2c48a874-132a-4e5c-ba24-0e7ab80ac2d4
source-git-commit: 2c42e8e4b7ca7e0cfaaf7895f067e4ccf7a2a40e
workflow-type: tm+mt
source-wordcount: '625'
ht-degree: 0%

---

# Converti ID utente da [!DNL Optimizely] a ID universali

*Beta funzionalità*

Use the DSP integration with the [!DNL Optimizely] customer data platform to convert your organization&#39;s first-party hashed email addresses to universal IDs for targeted advertising.

1. (To convert email addresses to [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; advertisers with [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Set up tracking to enable [!DNL Analytics] measurement](#analytics-tracking).

1. [Create an audience source in DSP](#source-create).

1. [Prepare and push the segment data](#push-data).

1. [Compare the number of universal IDs with the number of hashed email addresses](#compare-id-count).

## Step 1: Set up tracking for [!DNL Analytics] measurement {#analytics-tracking}

*Inserzionisti con [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

Per convertire indirizzi [!DNL RampIDs] e-mail o [!DNL ID5] ID, è necessario eseguire le operazioni seguenti:

1. (Se non l&#39;hai già fatto) Tutte le applicazioni tutti i [prerequisiti per l&#39;implementazione [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) e assicurati che l&#39;AMO ID e l&#39;EF [ID](/help/integrations/analytics/ids.md) vengano compilati negli URL di monitoraggio.

1. Registrati con il partner ID universale e distribuire codice specifico dell&#39;ID universale sulle tue pagine web per abbinare le conversioni dagli ID sui browser Web desktop e mobili (ma non sulle app per dispositivi mobili) alle visualizzazioni:

   * **Per [!DNL RampIDs]:** devi distribuire un JavaScript tag aggiuntivo sulle tue pagine web per far corrispondere le conversioni dagli ID sui browser Web desktop e mobili (ma non sulle app per dispositivi mobili) alle visualizzazioni. Contact your Adobe Account Team, who will give you instructions to register for a [!DNL LiveRamp] [!DNL LaunchPad] tag from [!DNL LiveRamp] Authentication Traffic Solutions. Registration is free, but you must sign an agreement. Once you register, your Adobe Account Team will generate and provide a unique tag for your organization to implement on your webpages.

## Step 2: Create an audience source in DSP {#source-create}

1. [Create an audience source](source-manage.md) to import audiences to your DSP account or an advertiser account. You can choose to convert your user identifiers to any of the [available universal ID formats](source-about.md).

   The source settings will include an auto-generated source key, which you&#39;ll use to push the segment data.

1. After you create the audience source, share the source code key with the [!DNL Optimizely] user.

## Passaggio 3: preparare ed eseguire il push dei dati del segmento {#push-data}

L&#39;inserzionista deve preparare e inviare i dati con l&#39;aiuto del proprio [!DNL Optimizely] rappresentante.

1. All&#39;interno [!DNL Optimizely Data Platform]di , eseguire l&#39;hashing degli ID e-mail per il pubblico dell&#39;inserzionista utilizzando l&#39;algoritmo SHA -256.

1. Segui le istruzioni per [[!DNL Optimizely's] inviare il segmento a DSP](https://support.optimizely.com/hc/en-us/articles/27974930963981-Integrate-Adobe-Ads). Includi le seguenti informazioni per abilitare l&#39;integrazione:

   * **Source Key:** This is the source key created in [Step 2](#source-create).

   * **Account Code:** This is the alphanumeric DSP Account Code, which you can find within DSP at [!UICONTROL Settings] > [!UICONTROL Account].

The segments should be available in DSP within 24 hours and are refreshed as configured for the advertiser. Regardless of how frequently the segment is refreshed, inclusion in a segment expires after 30 days by default or after a customer-specified expiration period. Refresh your segments by re-pushing them from [!DNL Optimizely] prior to the expiration. To request a custom segment expiration, contact your Adobe Account Team.

## Step 4: Compare the number of universal IDs with the number of hashed email addresses {#compare-id-count}

Dopo aver completato tutti i passaggi, verifica nel tuo libreria pubblico (disponibile quando crei o modifichi un pubblico da [!UICONTROL Audiences] > [!UICONTROL All Audiences] o all&#39;interno di posizionamento impostazioni) che il segmento sia disponibile e venga compilato entro 24 ore. Compare the number of universal IDs with the number of original hashed email addresses.

Il tasso di conversione degli indirizzi e-mail con hash in ID universali deve essere superiore al 90%. Ad esempio, se invii 100 indirizzi e-mail con hash dalla piattaforma di dati dei clienti, devono essere convertiti in più di 90 ID universali. Un tasso di traduzione del 90% o inferiore è un problema. Per ulteriori informazioni su come può variare il conteggio dei segmenti](#universal-ids-data-variances), vedi &quot;[Cause delle varianze dei dati tra ID e-mail e ID universali&quot;.

Per assistenza sulla risoluzione dei problemi, contatta il team dell&#39;account Adobe Systems o `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Informazioni sulle origini di pubblico di prima parte](/help/dsp/audiences/sources/source-about.md)
>* [Manage Audience Sources to Activate Universal ID Audiences](source-manage.md)
>* [Supporto per l’attivazione di ID universali](/help/dsp/audiences/universal-ids.md)
>* [Informazioni su Gestione dell&#39;audience](/help/dsp/audiences/audience-about.md)
