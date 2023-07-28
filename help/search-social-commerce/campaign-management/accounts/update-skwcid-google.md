---
title: Aggiorna il codice di tracciamento s kwcid per un [!DNL Google Ads] account
description: Scopri come passare al codice di tracciamento s\_kwcid più recente per un [!DNL Google Ads] account.
exl-id: 82168ee6-43bb-4b8d-882d-5254a1abcb09
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '462'
ht-degree: 0%

---

# Aggiorna il codice di tracciamento s\_kwcid per un [!DNL Google Ads] account

*Per gli inserzionisti con solo integrazione Adobi Advertising-Adobe Analytics*

*[!DNL Google Ads]solo account*

Formato legacy per il codice di tracciamento s\_kwcid per esistente [!DNL Google Ads] account non supporta alcune funzioni di Analytics, ad esempio la generazione di rapporti a livello di campagna e di gruppo di annunci per [!DNL Google Ads] campagne con prestazione massima, bozze e campagne di sperimentazione e altri casi d’uso in cui la stessa combinazione di ad+parola chiave+tipo di corrispondenza esiste in più campagne.

Il formato più recente include i parametri per l’ID della campagna e l’ID del gruppo di annunci:

```
s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}
```

Puoi passare al nuovo formato per uno o tutti gli account esistenti, singolarmente. Se non disponi di campagne con prestazione massima o bozze e campagne di sperimentazione, la migrazione al nuovo formato è facoltativa.

Tutte le nuove [!DNL Google Ads] gli account utilizzano automaticamente il nuovo formato s\_kwcid.

>[!NOTE]
>
>Dopo la migrazione di un account, tutti i dati di clic, costo e impression vengono segnalati correttamente dopo la modifica, ma tutti i click-through che si sono verificati prima della migrazione vengono ancora attribuiti ai dati di conversione basati sul vecchio formato s\_kwcid.

1. Nel menu principale, fai clic su **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Nel sottomenu, fai clic su **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.
1. Posizionare il cursore sul nome dell&#39;account e fare clic su ![icona a discesa freccia](/help/search-social-commerce/assets/arrow-dropdown-menu.png)e quindi selezionare **[!UICONTROL Edit]**.
1. Clic **[!UICONTROL Set Account Tracking]**.
1. Inizia la migrazione:

   1. Accanto a **[!UICONTROL S_KWCID FORMAT]** , fai clic su **[!UICONTROL LEGACY S_KWCID FORMAT]**.
   1. Clic **[!UICONTROL Migrate to new s_kwcid format]**.
   1. Nel messaggio di conferma selezionare la casella di controllo e quindi fare clic su **[!UICONTROL Continue]**.
   1. Nelle impostazioni account, fai clic su **[!UICONTROL Post]**.

   I metadati delle campagne vengono aggiornati in Analytics entro pochi giorni. Il tracciamento continua senza interruzioni, quindi non viene perso alcun dato, ma il reporting potrebbe non riflettere i nuovi codici di tracciamento fino a quando Analytics non riceve tutti i metadati.

   >[!NOTE]
   >
   >Tutti i click-through che si sono verificati prima della migrazione riporteranno comunque i dati di conversione in base al formato precedente.

1. Dopo aver iniziato la migrazione, aggiorna le impostazioni del suffisso della pagina di destinazione (denominato &quot;suffisso URL finale&quot; in alcune reti pubblicitarie), secondo necessità:

   * Quando [!UICONTROL Auto Upload]La funzione &quot; è abilitata nelle impostazioni di tracciamento, Search, Social &amp; Commerce aggiorna automaticamente il codice di tracciamento nel Suffisso della pagina di destinazione per questo account e le relative campagne. Non devi fare niente.
   * Quando [!UICONTROL Auto Upload]La funzione &quot; non è abilitata e non utilizzi l’s-kwcid lato server, quindi devi aggiornare manualmente il parametro s\_kwcid nelle impostazioni Suffisso pagina di destinazione. Puoi modificare manualmente i suffissi a livello di account e campagna nelle impostazioni account e campagna o caricando le modifiche in un bulksheet. Per configurare un suffisso a livello di gruppo di annunci o inferiore, utilizza [!DNL Google Ads] editor.
   * Se includi s\_kwcid nell’impostazione URL di base per qualsiasi componente della campagna, spostalo nell’impostazione Suffisso pagina di destinazione pertinente.

1. (Consigliato) Verifica i dati per questo account in Analytics prima di eseguire la migrazione di altri account.

>[!MORELIKETHIS]
>
>* [Gestire gli account di rete degli annunci](ad-network-account-manage.md)
>* [Il parametro di tracciamento s_kwcid](/help/search-social-commerce/tracking/skwcid-tracking-parameter.md)
>* [Panoramica di [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/home.html){target="_blank"}
