---
title: Configurare account di rete per il caricamento dei dati
description: Scopri come impostare e gestire i dettagli di un account di rete di annunci.
feature: Search Campaign Management
source-git-commit: e62eb730ec88a37cbe34e35d7b9bf99e0d4fd41d
workflow-type: tm+mt
source-wordcount: '545'
ht-degree: 0%

---

# Gestire gli account di rete degli annunci per il caricamento dei dati

<!-- Edit all, including title and metadata -->

Di seguito sono riportate le istruzioni per la gestione dei dettagli dell&#39;account per gli account di rete di annunci per i quali verranno caricati i dati dell&#39;account.

Per informazioni dettagliate sulle funzionalità disponibili per ogni rete di annunci, vedi &quot;[Inventario supportato](/help/search-social-commerce/introduction/supported-inventory.md).&quot;

>[!NOTE]
>
>Per istruzioni sulla gestione dei dettagli di un account di rete di annunci sincronizzato da Search, Social e Commerce tramite l&#39;API della rete di annunci, vedere &quot;[Gestire gli account di rete di annunci tramite la connessione API](../api-accounts/api-account-manage.md)&quot;.

## Crea dettagli account {#create-account}

1. Fare clic su **[!UICONTROL Create Account]**.

1. Fare clic sul nome della rete di annunci e quindi su **[!UICONTROL Next]**.

1. Specificare le [impostazioni account](#account-settings):

   1. Nella scheda **[!UICONTROL Account Details]**, modificare i dettagli dell&#39;account.

   1. (Inserzionisti con un&#39;integrazione [[!DNL Adobe Analytics for Advertising]] (/help/integrations/analytics/overview.md)) Fare clic sulla scheda **[!UICONTROL Set up Adobe Analytics]** e modificare le suite di rapporti [!DNL Analytics] da utilizzare per il tracciamento e il reporting dell&#39;attività della campagna.

   1. (Facoltativo) Nella scheda **[!UICONTROL Upload File]**, carica i file di dati per l&#39;account.

1. Fare clic su **[!UICONTROL Save]**.

## Modifica dettagli account {#edit-account}

1. Nel menu principale, fare clic su **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Selezionare l&#39;account in uno dei modi seguenti:

   * Selezionare la casella di controllo accanto al nome dell&#39;account, quindi fare clic su **[!UICONTROL Edit]** nella barra degli strumenti Azioni collettive.

   * Posizionare il cursore sul nome dell&#39;account, fare clic su **...** e quindi su **[!UICONTROL Edit]**.

1. Modifica le [impostazioni account](#account-settings-upload):

   1. (Facoltativo) Nella scheda **[!UICONTROL Account Details]**, modificare i dettagli dell&#39;account.

   1. (Facoltativo; inserzionisti con un&#39;integrazione [[!DNL Adobe Analytics for Advertising] 1}) Fai clic sulla scheda ](/help/integrations/analytics/overview.md) e modifica le suite di rapporti **[!UICONTROL Set up Adobe Analytics]** da utilizzare per il tracciamento e il reporting dell&#39;attività della campagna.[!DNL Analytics]

   1. (Facoltativo) Nella scheda **[!UICONTROL Upload File]**, carica i file di dati per l&#39;account.

   <!-- What are the repercussions of changing the suites? Timing of updated data? -->

1. Fare clic su **[!UICONTROL Save]**.

## Attivare o disattivare gli account di rete degli annunci {#enable-disable-account}

1. Nel menu principale, fare clic su **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Effettuare una delle seguenti operazioni:

   * (Dalla visualizzazione [!UICONTROL Accounts]):

      * (Per abilitare l&#39;account) Selezionare la casella di controllo accanto al nome dell&#39;account, quindi fare clic su **[!UICONTROL Activate]** nella barra degli strumenti Azioni collettive.

      * (Per disabilitare l&#39;account) Selezionare la casella di controllo accanto al nome dell&#39;account, quindi fare clic su **[!UICONTROL Pause]** nella barra degli strumenti Azioni collettive.

   * (dalle impostazioni account):

      1. Selezionare l&#39;account in uno dei modi seguenti:

         * Posizionare il cursore sul nome dell&#39;account, fare clic su **...** e quindi su **[!UICONTROL Edit]**.

         * Selezionare la casella di controllo accanto al nome dell&#39;account, quindi fare clic su **[!UICONTROL Edit]** nella barra degli strumenti Azioni collettive.

      1. Nella scheda **[!UICONTROL Account Details]**, disattivare **[!UICONTROL Account enabled]**.

      1. Fare clic su **[!UICONTROL Save]**.

## Impostazioni account {#account-settings-upload}

### Scheda [!UICONTROL Account Details]

**[!UICONTROL Account Name]:** nome da visualizzare per l&#39;account in Search, Social e Commerce.

>[!NOTE]
>
>Se hai un’integrazione Search, Social e Commerce-Adobe Analytics e modifichi il nome dell’account di ricerca, informa il team dell’account Adobe in modo che possa aggiornare la mappatura.

**[!UICONTROL Network Account ID]:** L&#39;ID account assegnato dalla rete di annunci. Questo ID viene utilizzato solo per il reporting. Search, Social e Commerce non si connettono direttamente all&#39;account di rete dell&#39;annuncio.

**[!UICONTROL Currency]:** (sola lettura per gli account esistenti) Abbreviazione della valuta utilizzata per l&#39;account.

**[!UICONTROL Time Zone]:** (sola lettura per gli account esistenti) Fuso orario dell&#39;inserzionista.

**[!UICONTROL Account Synchronization and Management]> [!UICONTROL Account Enabled]:** Ricerca, Social e Commerce consente il recupero automatico dei dati per un bucket S3 specificato.

## Scheda [!UICONTROL Setup Analytics]

**[!UICONTROL Adobe Analytics Report Suite]:** (inserzionisti con un&#39;integrazione [[!DNL Adobe Analytics for Advertising] integration](/help/integrations/analytics/overview.md); opzionale) Una o più suite di rapporti di Analytics a cui Search, Social e Commerce invia i dati caricati per la rete di annunci, incluse le classificazioni delle entità e i dati di clic per l&#39;account.

Affinché i dati vengano visualizzati nelle suite di rapporti, (a) la funzione AMO ID lato server deve essere configurata per l’account oppure (b) l’impostazione a livello di inserzionista su &quot;[!UICONTROL Enable Advertising reporting in Analytics]&quot; deve essere abilitata. Inoltre, l&#39;account [!DNL Analytics] dell&#39;inserzionista deve essere configurato per ricevere dati da Search, Social e Commerce. Per ulteriori informazioni, contatta il team del tuo account Adobe.

### Scheda [!UICONTROL Upload File]

(Facoltativo) Carica i file di dati per l&#39;account.<!-- For instructions, see "[Upload offline account data for reporting and simulations](upload-account-data.md)." -->
