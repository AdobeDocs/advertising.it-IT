---
title: (Nuova interfaccia) Sincronizzazione manuale dei dati di rete degli annunci
description: Scopri come attivare manualmente la sincronizzazione della struttura della campagna e delle entità della campagna per le reti di annunci supportate dalla nuova interfaccia utente.
feature: Search Campaign Management
source-git-commit: 5e384445a35f81275eefeac660b31c1acdc785f3
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# (Nuova interfaccia utente) Sincronizzare manualmente i dati di rete degli annunci tramite la connessione API

<!-- EDIT ALL -- FROM LEGACY UI -->

Solo *[!DNL Google Ads], [!DNL Microsoft Advertising] (in precedenza [!DNL Bing Ads]), [!DNL Yahoo! Japan Ads], [!DNL Yandex] e [!DNL Baidu] account esistenti*

La sincronizzazione è il processo tramite il quale Search, Social e Commerce raccolgono informazioni aggiornate per gli account di rete pubblicitaria connessi di ogni inserzionista su [reti pubblicitarie supportate](/help/search-social-commerce/introduction/supported-inventory.md). Questi dati includono la struttura della campagna dell’inserzionista e le entità della campagna, inclusa la maggior parte dei loro attributi gestiti o segnalati in Search, Social e Commerce. Non include i dati sui clic, né le offerte e i modificatori di offerte immessi all’esterno di Search, Social e Commerce, che vengono raccolti separatamente.

Search, Social e Commerce si sincronizzano (sincronizzano) automaticamente con gli account della rete di annunci una volta al giorno e ogni volta che rilevano una nuova campagna su una delle reti di annunci. Inoltre, invia immediatamente alla rete di annunci tutte le modifiche apportate ai dati della campagna dall’interno di Search, Social e Commerce.

È possibile richiedere manualmente la sincronizzazione di tutte le campagne attive e in pausa negli account specificati<!--Not available as of 2/23:  or in specific active and paused campaigns -->. Questa attività raccoglie le entità sulla rete di annunci che sono nuove o modificate.

Per le campagne con l&#39;opzione &quot;[!UICONTROL Auto Update]&quot;, anche l&#39;operazione di sincronizzazione genera e invia codici di tracciamento mancanti o che devono essere modificati nei modelli di tracciamento o negli URL di destinazione. Gli URL vengono generati in base ai parametri nelle impostazioni di tracciamento per le impostazioni account o la campagna. Se esistono URL di tracciamento per gli elementi rilevanti, questi non vengono rigenerati a meno che non siano necessari nuovi URL (ad esempio se il tipo di corrispondenza della parola chiave, il testo creativo o i parametri di tracciamento dell’account sono cambiati).

>[!NOTE]
>
>Ogni volta che si [crea un bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md), è possibile eseguire la sincronizzazione con la rete di annunci prima della creazione del bulksheet.

## Sincronizzare le campagne in un account di rete di annunci

1. Nel menu principale, fare clic su **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Selezionare la casella di controllo accanto al nome dell&#39;account.

   <!-- As of 2/23, you can sync only one acct at a time:  Select the check box next to each account or campaign that you want to sync. You can sync up to 50 campaigns at a time. If you sync more than five accounts at a time, the job is broken into batches of up to five accounts each. -->

1. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL ... More Actions]** > **[!UICONTROL Sync]**.

   * Posizionare il cursore sul nome dell&#39;account, fare clic su **...** e quindi su **[!UICONTROL Edit]**.

È possibile seguire lo stato del processo di sincronizzazione nella visualizzazione [!UICONTROL Workspace]. Il processo può richiedere
un&#39;ora o più per la visualizzazione.

>[!MORELIKETHIS]
>
>* [Scaricare/creare un file bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)
