---
title: Replica  [!DNL Google Ads] campagne in [!DNL Microsoft Advertising]
description: Scopri come esportare le campagne sincronizzate in un account  [!DNL Google Ads] direttamente in un account [!DNL Microsoft Advertising] sincronizzato.
exl-id: e7714d3d-4a8e-44ef-a3a7-e5198c091660
feature: Search Tools
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '942'
ht-degree: 0%

---

# Replica [!DNL Google Ads] campagne in [!DNL Microsoft Advertising]

È possibile esportare le campagne sincronizzate in un account [!DNL Google Ads] direttamente in un account [!DNL Microsoft Advertising] sincronizzato come campagne eCPC (Enhanced CPC). Le offerte e i budget delle campagne esistenti vengono scalati. Il tracciamento di ricerche, social network e Commerce esistente non viene importato.

Puoi replicare i seguenti tipi di campagne e la relativa struttura:

* [!DNL Google Ads] campagne Search&amp;Display in [!DNL Microsoft Advertising] campagne Search&amp;Display.

* [!DNL Google Display Network] campagne, incluse le immagini pubblicitarie, in [!DNL Microsoft Advertising] campagne per il pubblico su Microsoft Audience Network.

  Se si desidera replicare le campagne di visualizzazione basate su feed acquisti, replicare innanzitutto le offerte di prodotti [!DNL Google Merchant Center] in [!DNL Microsoft Merchant Center]. Quando replichi le campagne, seleziona l&#39;archivio [!DNL Microsoft Merchant Center] nelle Opzioni di importazione per collegare l&#39;archivio alle campagne per il pubblico basate su feed.

* [!DNL Google Ads] campagne con prestazione massima, inclusi annunci di inventario locali, in [!DNL Microsoft Advertising] campagne con prestazione massima.

Puoi scegliere di aggiornare le campagne una volta, ogni giorno, ogni settimana o ogni mese oppure in base alla pianificazione consigliata da [!DNL Microsoft Advertising]. Facoltativamente, puoi configurare le notifiche ogni volta che viene eseguito un processo di importazione o quando si verificano errori o modifiche. Dopo aver importato le campagne in [!DNL Microsoft Advertising], puoi controllare lo stato del processo di importazione, esaminare tutti i registri di errori, eseguire manualmente un processo di importazione e modificare, mettere in pausa, abilitare o eliminare la pianificazione delle importazioni.

Non tutte le informazioni sulla campagna sono state replicate e potrebbe essere necessario aggiungere alcune informazioni alle campagne [!DNL Microsoft Advertising]. Per ulteriori informazioni sui dati importati, vedere la Guida di [!DNL Microsoft Advertising] in &quot;[What gets imported from [!DNL Google Ads]](https://help.ads.microsoft.com/#apex/ads/en/50851).&quot; Poiché il monitoraggio di Search, Social e Commerce non è importato, è necessario aggiungere il monitoraggio anche nelle impostazioni [account](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md), [campagna](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md), [gruppo di annunci](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) o [ad](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md).

## Replica [!DNL Google Ads] campagne

>[!NOTE]
>
>Se desideri replicare le campagne di visualizzazione basate su feed acquisti, [replica le  [!DNL Google Merchant Center] offerte di prodotti in [!DNL Microsoft Merchant Center]](https://help.ads.microsoft.com/apex/index/3/en/56870). Quando replichi le campagne, seleziona l&#39;archivio [!DNL Microsoft Merchant Center] nelle opzioni di importazione per collegare l&#39;archivio alle campagne per il pubblico basate su feed.

Vedi [ciò che è stato importato da [!DNL Google Ads] campagne](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500).

1. Nel menu principale di Ricerca, Social e Commerce, fare clic su **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Fare clic su **[!UICONTROL +Import]**.

1. Specificare le [impostazioni di importazione](#campaign-import-settings):

   1. Nella sezione **[!UICONTROL Select accounts]**:

      1. Selezionare gli account di origine e di destinazione.

      1. Fare clic su **[!UICONTROL Get Credential Id from MSA]**.

      1. Accedere all&#39;account [!DNL Microsoft Advertising] di destinazione, copiare l&#39;ID credenziali visualizzato e incollare il valore nel campo **[!UICONTROL Credential ID]**.

   1. Nella sezione **[!UICONTROL Select campaigns & ad groups]**, specifica le campagne e i gruppi di annunci da importare.

   1. Nella sezione **[!UICONTROL Customize your import]** specificare i tipi di elemento da importare.

   1. Nella sezione **[!UICONTROL Set schedule]** specificare quando eseguire il processo di importazione.

1. Fare clic su **[!UICONTROL Post]**.

1. (Facoltativo) Aggiungi il tracciamento di ricerca, social e Commerce nelle impostazioni [account](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md), [campagna](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md), [gruppo di annunci](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) o [ad](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md).

## Modificare le impostazioni di pianificazione per un processo di importazione campagne

Vedi [ciò che è stato importato da [!DNL Google Ads] campagne](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500).

1. Nel menu principale, fare clic su **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Selezionare la casella di controllo accanto al processo di importazione, quindi fare clic su ![Modifica](/help/search-social-commerce/assets/edit.png "Modifica").

1. Nella sezione **[!UICONTROL Set schedule]**, specifica le [impostazioni di pianificazione](#campaign-import-settings).

1. Fare clic su **[!UICONTROL Post]**.

## Visualizzare i processi di importazione delle campagne

È possibile elencare tutti i processi di importazione, inclusi l&#39;account di origine [!DNL Google Ads], l&#39;account di destinazione [!DNL Microsoft Advertising], l&#39;ora o la pianificazione dell&#39;importazione e l&#39;utente che ha creato il processo. Quando si esegue un processo di importazione più volte, anche durante importazioni pianificate regolarmente, ogni occorrenza viene elencata come un processo separato.

* Effettuare una delle seguenti operazioni:

   * Nel menu principale, fare clic su **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

     Per impostazione predefinita, la visualizzazione si apre sulla scheda [!UICONTROL List of Import Jobs].

   * Dalla scheda [[!UICONTROL Import Logs]](#campaign-import-log), fare clic sulla scheda **[!UICONTROL List of Import Jobs]**.

## Eseguire un processo di importazione campagna

1. Nel menu principale, fare clic su **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Selezionare la casella di controllo accanto al processo di importazione.

1. Fai clic su ![Esegui ora](/help/search-social-commerce/assets/run.png "Esegui ora").

## Visualizzare i registri per i processi di importazione delle campagne {#campaign-import-log}

È possibile elencare tutti i processi di importazione completati o non riusciti, inclusi l&#39;ora di inizio, l&#39;account di origine [!DNL Google Ads], l&#39;account di destinazione [!DNL Microsoft Advertising], l&#39;utente che ha creato il processo, il numero di operazioni riuscite e non riuscite e qualsiasi indirizzo di posta elettronica che ha ricevuto notifiche per ogni processo. È possibile visualizzare ulteriori dettagli sulle modifiche all&#39;account [!DNL Microsoft Advertising] di destinazione che si sono verificate per ogni processo, incluso il numero di elementi aggiunti, sincronizzati, eliminati e che hanno prodotto errori per ogni livello di entità (ad esempio campagna o parola chiave) nell&#39;account.

1. Nel menu principale, fare clic su **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Fare clic sulla scheda **[!UICONTROL Import Logs]**.

1. (Facoltativo) Per visualizzare i dettagli di qualsiasi processo di importazione, fare clic sul valore nella colonna [!UICONTROL Summary].

## Impostazioni del processo di importazione di Campaign {#campaign-import-settings}

### [!UICONTROL Select accounts]

**[!UICONTROL Source Google Ads account]:** Account [!DNL Google Ads] sincronizzato da cui vengono esportati i dati della campagna.

**[!UICONTROL Credential ID]:** ID utilizzato da [!DNL Microsoft Advertising] per rappresentare le credenziali di [!DNL Google Ads].

Generazione automatica delle credenziali [!DNL Microsoft Advertising] per l&#39;importazione non disponibile a causa di limitazioni [!DNL Microsoft Advertising]. Contatta il tuo Account Team di Adobi, che genererà le credenziali e ti fornirà l’ID.

**[!UICONTROL Target Microsoft Ads account]:** Account [!DNL Microsoft Advertising] sincronizzato in cui vengono importati i dati della campagna.

### [!UICONTROL Select campaigns & ad groups]

**\[Dati da importare\]:** Specificare i dati da importare:

* *[!UICONTROL Import all new and existing campaigns]:* Per importare i dati per tutte le campagne già esistenti e le campagne che non esistono in [!DNL Microsoft Advertising].

* *[!UICONTROL Import specific campaigns and adgroups]:* Per selezionare campagne e gruppi di annunci specifici.

   * Per espandere una campagna nei gruppi di annunci figlio, fare clic su **[!UICONTROL >]** dopo il nome della campagna.

   * Per selezionare una campagna o un gruppo di annunci, seleziona l’elemento in modo che venga visualizzato un segno di spunta.

   * Per rimuovere una campagna o un gruppo di annunci:

      * Nella colonna [!UICONTROL Campaigns] o [!UICONTROL Adgroups], deseleziona la campagna o il gruppo di annunci in modo che il segno di spunta scompaia.

      * Nella colonna [!UICONTROL Selected] fare clic su ![Elimina](/help/search-social-commerce/assets/delete.png "Elimina").

### [!UICONTROL Customize your import]

**[!UICONTROL Choose specific import options]:** consente di specificare gli elementi da importare, le offerte e i budget e altre opzioni.

**[!UICONTROL What to import]:** Definisce gli elementi da importare. Le opzioni di importazione delle categorie di articoli sono selezionate per impostazione predefinita, con tutti i tipi di elementi selezionati. Per includere solo tipi di elemento specifici, fare clic su **[!UICONTROL Show advanced options]** e modificare i tipi di elemento in modo che includano.

**[!UICONTROL Bids and budgets]:** definisce le impostazioni di offerta e budget da importare, aggiornare e personalizzare.

**[!UICONTROL Other options]:** Definisce come gestire gli URL importati della pagina di destinazione, i modelli di tracciamento e altre opzioni di campagna, annuncio e targeting.

### [!UICONTROL Set schedule]

**[!UICONTROL Import name]:** Nome del processo di importazione.

**[!UICONTROL When]:** Quando importare le campagne specificate: *Automatico* (per consentire a [!DNL Microsoft Advertising] di impostare una pianificazione per ottimizzare al meglio le campagne), *[!UICONTROL Now]* (per eseguire il processo quando si inseriscono le impostazioni del processo), *[!UICONTROL Once]* a un&#39;ora specificata, *[!UICONTROL Daily]* a un&#39;ora specificata, *[!UICONTROL Weekly]* a un&#39;ora specificata o *[!UICONTROL Monthly]* a un&#39;ora specificata.

**[!UICONTROL Receive email notifications]:** se e quando inviare notifiche e-mail sui processi di importazione agli indirizzi e-mail nel campo Send reports to (Invia rapporti a).

**[!UICONTROL Send reports to]:** Indirizzi e-mail per ricevere notifiche sui processi di importazione. Separare più indirizzi con virgole (`,`).
