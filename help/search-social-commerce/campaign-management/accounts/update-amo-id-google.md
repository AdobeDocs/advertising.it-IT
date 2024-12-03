---
title: 'Aggiorna il codice di tracciamento AMO ID (s_kwcid) per un account  [!DNL Google Ads] '
description: Scopri come passare al codice di tracciamento AMO ID più recente per un account  [!DNL Google Ads] .
exl-id: 4dfd9ea6-f639-4b9a-aaa5-13f574e3961b
feature: Search Campaign Management
source-git-commit: edb46265c6977a1e2c1b352f41fedcfc3a9e3bbf
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 0%

---

# Aggiorna il codice di tracciamento AMO ID (s_kwcid) per un account [!DNL Google Ads]

*Inserzionisti solo con integrazione Adobe Advertising-Adobe Analytics*

Solo *[!DNL Google Ads]account*

Il formato legacy (precedente a ottobre 2019) per il [codice di tracciamento AMO ID](/help/integrations/analytics/ids.md#amo-id-formats) per gli account [!DNL Google Ads] esistenti non supporta alcune funzionalità in Analytics, ad esempio la generazione di rapporti a livello di campagna e di gruppo di annunci per campagne con prestazione massima [!DNL Google Ads], bozze e campagne di esperimenti e altri casi d’uso in cui la stessa combinazione di parole chiave+corrispondenza esiste in più campagne.

Il formato corrente include i parametri per l’ID della campagna e l’ID del gruppo di annunci:

```
s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}
```

Per un account esistente che utilizza il formato legacy, puoi passare al formato corrente. Se non disponi di campagne con prestazione massima o bozze e campagne di sperimentazione, la migrazione al nuovo formato è facoltativa.

Tutti i nuovi account [!DNL Google Ads] utilizzano automaticamente il formato AMO ID corrente.

>[!NOTE]
>
>Questa opzione è disponibile solo per gli account che non utilizzano il formato corrente.
>
>Dopo la migrazione di un account, tutti i dati relativi a clic, costi e impression vengono segnalati correttamente dopo la modifica, ma tutti i click-through che si sono verificati prima della migrazione vengono ancora attribuiti ai dati di conversione basati sul vecchio formato AMO ID.

1. Nel menu principale, fare clic su **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Nel sottomenu, fare clic su **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Posizionare il cursore sul nome dell&#39;account, fare clic sull&#39;icona a discesa ![freccia](/help/search-social-commerce/assets/arrow-dropdown-menu.png), quindi selezionare **[!UICONTROL Edit]**.

1. Fare clic su **[!UICONTROL Set Account Tracking]**.

1. Inizia la migrazione:

   1. Accanto a **[!UICONTROL S_KWCID FORMAT]** nelle impostazioni [!UICONTROL Account Tracking], fare clic su **[!UICONTROL LEGACY S_KWCID FORMAT]**.

   1. Fare clic su **[!UICONTROL Migrate to new s_kwcid format]**.

   1. Nel messaggio di conferma selezionare la casella di controllo e quindi fare clic su **[!UICONTROL Continue]**.

   1. Nelle impostazioni account, fare clic su **[!UICONTROL Post]**.

   I metadati per le campagne vengono aggiornati in [!DNL Analytics] entro pochi giorni. Il tracciamento continua senza interruzioni, quindi non viene perso alcun dato, ma il reporting potrebbe non riflettere i nuovi codici di tracciamento fino a quando [!DNL Analytics] non riceve tutti i metadati.

   >[!NOTE]
   >
   >Tutti i click-through che si sono verificati prima della migrazione segnalano ancora i dati di conversione in base al formato precedente.

1. Dopo aver iniziato la migrazione, aggiorna le impostazioni del suffisso della pagina di destinazione (denominato &quot;suffisso URL finale&quot; in alcune reti pubblicitarie), secondo necessità:

   * Quando la funzione [!UICONTROL Auto Upload]&quot; è abilitata nelle impostazioni di tracciamento, Search, Social e Commerce aggiornano automaticamente il codice di tracciamento nel suffisso della pagina di destinazione per questo account e le relative campagne. Non devi fare niente.

   * Se la funzione [!UICONTROL Auto Upload] non è abilitata e non utilizzi la funzione [AMO ID lato server](/help/integrations/analytics/ids.md#amo-id-formats), devi aggiornare manualmente il parametro AMO ID nelle impostazioni Suffisso pagina di destinazione. È possibile modificare manualmente i suffissi a livello di account e campagna nelle [impostazioni account](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) e [impostazioni campagna](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md) oppure [caricare le modifiche in un bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md). Per configurare un suffisso a livello di gruppo di annunci o inferiore, utilizzare l&#39;editor [!DNL Google Ads].

   * Se includi l’AMO ID nell’impostazione URL di base per qualsiasi componente della campagna, spostalo nell’impostazione Suffisso pagina di destinazione pertinente.

1. (Consigliato) Verificare i dati per questo account in [!DNL Analytics] prima di eseguire la migrazione di altri account.

>[!MORELIKETHIS]
>
>* [Gestione account di rete pubblicitaria](ad-network-account-manage.md)
>* [ID Adobe Advertising utilizzati da [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Panoramica di [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/home.html){target="_blank"}
