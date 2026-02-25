---
title: (Nuova interfaccia) Gestisci [!DNL Naver] account solo per il tracciamento
description: Scopri come impostare e gestire i dettagli dell’account nella nuova interfaccia utente per un account  [!DNL Naver] .
feature: Search Campaign Management
source-git-commit: 0de2a01905727314ca6c0792c5efaf6450548293
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 0%

---

# (Nuova interfaccia) Gestisci [!DNL Naver] account solo per il tracciamento

*funzionalità Beta*

Di seguito sono riportate le istruzioni per la gestione di [[!DNL Naver] account](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md) per monitorare, creare rapporti e visualizzare le prestazioni per gli annunci acquistati direttamente dalla rete di annunci. Search, Social e Commerce non sincronizzano i dati con la rete di annunci, non forniscono offerte automatizzate né forniscono alcun tipo di ottimizzazione o simulazione.

Per informazioni dettagliate sulle funzionalità disponibili, vedere &quot;[Inventario supportato](/help/search-social-commerce/introduction/supported-inventory.md).&quot;

## Crea dettagli account di rete dell’annuncio {#create-account}

Per abilitare il tracciamento di un account, devi creare un record account corrispondente contenente le credenziali di accesso all&#39;account e con lo stato *abilitato*.

>[!NOTE]
>
>Per creare un account effettivo sulla rete di annunci, vai al sito web della rete di annunci.

1. Nel menu principale, fare clic su **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Fare clic su **[!UICONTROL Create Account]**.

1. Fare clic sul nome della rete di annunci e quindi su **[!UICONTROL Next]**.

1. Specificare le [impostazioni account](#account-settings-naver):

   1. Nella scheda **[!UICONTROL Enter Account Details]** specificare le impostazioni generali dell&#39;account.

   1. (Inserzionisti con un&#39;integrazione [[!DNL Adobe Analytics for Advertising] 1}) Fai clic sulla scheda ](/help/integrations/analytics/overview.md) e seleziona tutte le **[!UICONTROL Set up Adobe Analytics]** suite di rapporti da utilizzare per il tracciamento e il reporting dell&#39;attività della campagna.[!DNL Analytics]

1. Fare clic su **[!UICONTROL Save]**.

## Modifica i dettagli dell’account di rete dell’annuncio {#edit-account}

Per modificare il nome dell&#39;account, cambiare lo stato dell&#39;account o modificare le suite di rapporti [!DNL Analytics] da utilizzare per il tracciamento e il reporting, modificare i dettagli dell&#39;account.

>[!NOTE]
>
>Per modificare un account effettivo sulla rete di annunci, vai al sito web della rete di annunci.

1. Nel menu principale, fare clic su **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Selezionare l&#39;account in uno dei modi seguenti:

   * Selezionare la casella di controllo accanto al nome dell&#39;account, quindi fare clic su **[!UICONTROL Edit]** nella barra degli strumenti Azioni collettive.

   * Posizionare il cursore sul nome dell&#39;account, fare clic su **...** e quindi su **[!UICONTROL Edit]**.

1. Modifica le [impostazioni account](#account-settings-api):

   1. (Facoltativo) Nella scheda **[!UICONTROL Account Details]**, modificare i dettagli dell&#39;account.

   1. (Facoltativo; inserzionisti con un&#39;integrazione [[!DNL Adobe Analytics for Advertising] 1}) Fai clic sulla scheda ](/help/integrations/analytics/overview.md) e modifica le suite di rapporti **[!UICONTROL Set up Adobe Analytics]** da utilizzare per il tracciamento e il reporting dell&#39;attività della campagna.[!DNL Analytics]

   <!-- What are the repercussions of changing the suites? Timing of updated data? -->

1. Fare clic su **[!UICONTROL Save]**.

<!-- What does this do?

## Enable or disable ad network accounts {#enable-disable-account}

When you enable an ad network account, Search, Social, & Commerce synchronizes campaign data with the account (when supported) and pushes automated bids and/or campaign budgets for campaigns in portfolios. When you disable an ad network account, Search, Social, & Commerce stops all activity on the account. Data collected while the account was active is still stored, but the campaign management views and reports don't include data for the time period in which the account is disabled. You can later re-enable the account to resume activity with the account.

1. In the main menu, click **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Do either of the following:

   * (From the [!UICONTROL Accounts] view):

     * (To enable the account) Select the check box next to the account name, and then click **[!UICONTROL Activate]** in the bulk actions toolbar.

     * (To disable the account) Select the check box next to the account name, and then click **[!UICONTROL Pause]** in the bulk actions toolbar.

   * (From the account settings):
   
     1. Select the account in either of the following ways:
     
        * Hold the cursor over the account name, click **...**, and then click **[!UICONTROL Edit]**.
        
        * Select the check box next to the account name, and then click **[!UICONTROL Edit]** in the bulk actions toolbar.
        
     1. On the **[!UICONTROL Account Details]** tab, turn off **[!UICONTROL Account enabled]**.

     1. Click **[!UICONTROL Save]**.

-->

## Impostazioni dell’account di rete dell’annuncio {#account-settings-api}

### Scheda [!UICONTROL Account Details]

#### [!UICONTROL Enter Account Details]/[!UICONTROL Account Details]

**[!UICONTROL Account Name]:** nome da visualizzare per l&#39;account in Search, Social e Commerce.

>[!NOTE]
>
>Se hai un’integrazione Search, Social e Commerce-Adobe Analytics e modifichi il nome dell’account di ricerca, chiedi al team del tuo account Adobe di aggiornare la mappatura.

**[!UICONTROL Network Account ID]:** L&#39;ID account assegnato dalla rete di annunci.

**[!UICONTROL Currency]:** abbreviazione della valuta utilizzata per l&#39;account.

**[!UICONTROL Time Zone]:** Fuso orario dell&#39;inserzionista.

**[!UICONTROL Account Synchronization and Management]> [!UICONTROL Account Enabled]:** Search, Social e Commerce sincronizzano i dati della campagna con l&#39;account (se supportato) e inviano offerte automatizzate e/o budget delle campagne nei portfolio.

## Scheda [!UICONTROL Setup Analytics]

**[!UICONTROL Adobe Analytics Report Suite]:** (inserzionisti con un&#39;integrazione [[!DNL Adobe Analytics for Advertising] integration](/help/integrations/analytics/overview.md); opzionale) Una o più suite di rapporti di Analytics a cui Search, Social e Commerce invia i dati caricati per la rete di annunci, incluse le classificazioni delle entità e i dati di clic per l&#39;account.

Affinché i dati vengano visualizzati nelle suite di rapporti, (a) la funzione AMO ID lato server deve essere configurata per l’account oppure (b) l’impostazione a livello di inserzionista su &quot;[!UICONTROL Enable Advertising reporting in Analytics]&quot; deve essere abilitata. Inoltre, l&#39;account [!DNL Analytics] dell&#39;inserzionista deve essere configurato per ricevere dati da Search, Social e Commerce. Per ulteriori informazioni, contatta il team del tuo account Adobe.

>[!MORELIKETHIS]
>
>* [Implementa [!DNL Naver] account di sola verifica](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
>* [Informazioni sugli account di rete di annunci](/help/search-social-commerce/new-ui/set-up/accounts/ad-network-account-about.md)
