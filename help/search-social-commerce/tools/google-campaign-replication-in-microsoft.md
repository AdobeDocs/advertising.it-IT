---
title: Replica [!DNL Google Ads] campagne in [!DNL Microsoft® Advertising]
description: Scopri come esportare le campagne sincronizzate in una [!DNL Google Ads] account direttamente in un file sincronizzato [!DNL Microsoft® Advertising] account.
exl-id: 1bb0d915-bf33-4c50-88a5-268d4de5ccff
source-git-commit: 8d062e5c74c8f873ab5f2491659a32be47bb2afb
workflow-type: tm+mt
source-wordcount: '962'
ht-degree: 0%

---

# Replica [!DNL Google Ads] campagne in [!DNL Microsoft® Advertising]

Puoi esportare le campagne sincronizzate in una [!DNL Google Ads] account direttamente in un file sincronizzato [!DNL Microsoft® Advertising] account come campagne CPC (eCPC) avanzate. Le offerte e i budget delle campagne esistenti vengono scalati. Il tracciamento di ricerche, social e e commerce esistente non viene importato.

Puoi replicare i seguenti tipi di campagne e la relativa struttura:

* [!DNL Google Ads] campagne di ricerca e visualizzazione in [!DNL Microsoft® Advertising] campagne di ricerca e visualizzazione.

* [!DNL Google Display Network] campagne, incluse le immagini pubblicitarie, in [!DNL Microsoft® Advertising] campagne per il pubblico su Microsoft® Audience Network.

  Se desideri replicare le campagne di visualizzazione basate su feed di acquisto, devi prima replicare le [!DNL Google Merchant Center] offerte di prodotti a [!DNL Microsoft® Merchant Center]. Quando replichi le campagne, seleziona la [!DNL Microsoft® Merchant Center] archivia nelle Opzioni di importazione per collegare lo store alle campagne per il pubblico basate su feed.

* [!DNL Google Ads] le campagne con le massime prestazioni, inclusi gli annunci di inventario locali, in [!DNL Microsoft® Advertising] campagne di acquisto intelligenti.

Puoi scegliere di aggiornare le campagne una volta, ogni giorno, settimanalmente o mensilmente oppure in base a [!DNL Microsoft® Advertising]la pianificazione consigliata di. Facoltativamente, puoi configurare le notifiche ogni volta che viene eseguito un processo di importazione o quando si verificano errori o modifiche. Dopo aver importato le campagne in [!DNL Microsoft® Advertising], è possibile controllare lo stato del processo di importazione, esaminare tutti i registri di errori, eseguire manualmente un processo di importazione e modificare, mettere in pausa, abilitare o eliminare la pianificazione delle importazioni.

Non tutte le informazioni sulla campagna sono replicate e potresti dover aggiungere alcune informazioni al tuo [!DNL Microsoft® Advertising] campagne. Per ulteriori informazioni sui dati importati, consulta [!DNL Microsoft® Advertising] guida di &quot;[Cosa viene importato da [!DNL Google Ads]](https://help.ads.microsoft.com/#apex/ads/en/50851).&quot; Poiché il tracciamento di Ricerca, Social e Commerce non è importato, è necessario aggiungere il tracciamento anche all’interno di [account](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md), [campagna](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md), [gruppo di annunci](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md), o [annuncio](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) impostazioni.

## Replica [!DNL Google Ads] campagne

>[!NOTE]
>
>Se desideri replicare le campagne di visualizzazione basate su feed di acquisto, [replicare [!DNL Google Merchant Center] offerte di prodotti in [!DNL Microsoft® Merchant Center]](https://help.ads.microsoft.com/apex/index/3/en/56870). Quando replichi le campagne, seleziona la [!DNL Microsoft® Merchant Center] archivia nelle opzioni di importazione per collegare lo store alle campagne per il pubblico basate su feed.

Consulta [da cosa viene importato [!DNL Google Ads] campagne](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500).

1. Nel menu principale di Ricerca, Social e Commerce, fai clic su **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Clic **[!UICONTROL +Import]**.

1. Specifica la [impostazioni di importazione](#campaign-import-settings):

   1. In **[!UICONTROL Select accounts]** sezione:

      1. Selezionare gli account di origine e di destinazione.

      1. Clic **[!UICONTROL Get Credential Id from MSA]**.

      1. Accedi alla destinazione [!DNL Microsoft Advertising] , copiare l&#39;ID delle credenziali visualizzato e incollare il valore in **[!UICONTROL Credential ID]** campo.

   1. In **[!UICONTROL Select campaigns & ad groups]** , specifica le campagne e i gruppi di annunci da importare.

   1. In **[!UICONTROL Customize your import]** , specificare i tipi di elemento da importare.

   1. In **[!UICONTROL Set schedule]** , specificare quando eseguire il processo di importazione.

1. Clic **[!UICONTROL Post]**.

1. (Facoltativo) Aggiungi il tracciamento di ricerca, social e commerce all’interno del [account](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md), [campagna](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md), [gruppo di annunci](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md), o [annuncio](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) impostazioni.

## Modificare le impostazioni di pianificazione per un processo di importazione campagne

Consulta [da cosa viene importato [!DNL Google Ads] campagne](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500).

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Selezionare la casella di controllo accanto al processo di importazione e quindi fare clic su ![Modifica](/help/search-social-commerce/assets/edit.png "Modifica").

1. In **[!UICONTROL Set schedule]** , specificare [impostazioni di pianificazione](#campaign-import-settings).

1. Clic **[!UICONTROL Post]**.

## Visualizzare i processi di importazione delle campagne

Puoi elencare tutti i processi di importazione, inclusa l’origine [!DNL Google Ads] account, il target [!DNL Microsoft® Advertising] l&#39;account, l&#39;ora o la pianificazione dell&#39;importazione e l&#39;utente che ha creato il processo. Quando si esegue un processo di importazione più volte, anche durante importazioni pianificate regolarmente, ogni occorrenza viene elencata come un processo separato.

* Effettuare una delle seguenti operazioni:

   * Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

     Per impostazione predefinita, la vista si apre su [!UICONTROL List of Import Jobs] scheda.

   * Dalla sezione [[!UICONTROL Import Logs] scheda](#campaign-import-log), fare clic su **[!UICONTROL List of Import Jobs]** scheda.

## Eseguire un processo di importazione campagna

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Selezionare la casella di controllo accanto al processo di importazione.

1. Clic ![Esegui ora](/help/search-social-commerce/assets/run.png "Esegui ora").

## Visualizzare i registri per i processi di importazione delle campagne {#campaign-import-log}

Puoi elencare tutti i processi di importazione completati o non riusciti, inclusa l’ora di inizio e l’origine [!DNL Google Ads] account, il target [!DNL Microsoft® Advertising] account, l&#39;utente che ha creato il processo, il numero di operazioni riuscite e non riuscite ed eventuali indirizzi e-mail che hanno ricevuto notifiche per ciascun processo. Puoi visualizzare ulteriori dettagli sulle modifiche apportate al target [!DNL Microsoft® Advertising] account che si è verificato per ogni processo, incluso il numero di elementi aggiunti, sincronizzati, eliminati e che hanno prodotto errori per ogni livello di entità (ad esempio campagna o parola chiave) nell’account.

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Fai clic su **[!UICONTROL Import Logs]** scheda.

1. (Facoltativo) Per visualizzare i dettagli di qualsiasi processo di importazione, fai clic sul valore in [!UICONTROL Summary] colonna.

## Impostazioni del processo di importazione di Campaign {#campaign-import-settings}

### [!UICONTROL Select accounts]

**[!UICONTROL Source Google Ads account]:** Il [!DNL Google Ads] account da cui vengono esportati i dati della campagna.

**[!UICONTROL Credential ID]:** Un ID che [!DNL Microsoft® Advertising] utilizza per rappresentare il [!DNL Google Ads] credenziali.

Generazione automatica di [!DNL Microsoft® Advertising] credenziali per l&#39;importazione non disponibili a causa di [!DNL Microsoft® Advertising] limitazioni. Contatta il supporto tecnico Adobe o il team dell’account Adobe, che genererà le credenziali e ti fornirà l’ID.

**[!UICONTROL Target Microsoft® Ads account]:** Il [!DNL Microsoft® Advertising] account in cui vengono importati i dati della campagna.

### [!UICONTROL Select campaigns & ad groups]

**\[Dati da importare\]:** Specificare i dati da importare:

* *[!UICONTROL Import all new and existing campaigns]:* Per importare dati per tutte le campagne già esistenti e per le campagne che non esistono in [!DNL Microsoft® Advertising].

* *[!UICONTROL Import specific campaigns and adgroups]:* Per selezionare campagne e gruppi di annunci specifici.

   * Per espandere una campagna nei gruppi di annunci figlio, fai clic su **[!UICONTROL >]** dopo il nome della campagna.

   * Per selezionare una campagna o un gruppo di annunci, seleziona l’elemento in modo che venga visualizzato un segno di spunta.

   * Per rimuovere una campagna o un gruppo di annunci:

      * In [!UICONTROL Campaigns] o [!UICONTROL Adgroups] deseleziona la campagna o il gruppo di annunci in modo che il segno di spunta non sia più visibile.

      * In [!UICONTROL Selected] , fare clic su ![Elimina](/help/search-social-commerce/assets/delete.png "Elimina").

### [!UICONTROL Customize your import]

**[!UICONTROL Choose specific import options]:** Consente di specificare cosa importare, le offerte, i budget e altre opzioni.

**[!UICONTROL What to import]:** Definisce gli elementi da importare. Le opzioni di importazione delle categorie di articoli sono selezionate per impostazione predefinita, con tutti i tipi di elementi selezionati. Per includere solo tipi di elementi specifici, fare clic su **[!UICONTROL Show advanced options]** e modificare i tipi di elemento da includere.

**[!UICONTROL Bids and budgets]:** Definisce le impostazioni di offerta e budget da importare, aggiornare e personalizzare.

**[!UICONTROL Other options]:** Definisce come gestire gli URL importati della pagina di destinazione, i modelli di tracciamento e altre opzioni di campagna, annuncio e targeting.

### [!UICONTROL Set schedule]

**[!UICONTROL Import name]:** Nome del processo di importazione.

**[!UICONTROL When]:** Quando importare le campagne specificate: *Automatico* (per consentire [!DNL Microsoft® Advertising] impostare una pianificazione per ottimizzare al meglio le campagne), *[!UICONTROL Now]* (per eseguire il processo quando si inseriscono le impostazioni del processo), *[!UICONTROL Once]* a un’ora determinata, *[!UICONTROL Daily]* a un’ora determinata, *[!UICONTROL Weekly]* in un momento determinato, oppure *[!UICONTROL Monthly]* a un’ora specificata.

**[!UICONTROL Receive email notifications]:** Se e quando inviare notifiche e-mail sui processi di importazione agli indirizzi e-mail nel campo Send reports to (Invia rapporti a).

**[!UICONTROL Send reports to]:** Indirizzi e-mail per ricevere notifiche sui processi di importazione. Separa più indirizzi con virgole (`,`).
