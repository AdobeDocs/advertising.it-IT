---
title: Sincronizzare manualmente i dati di rete degli annunci
description: Scopri come attivare manualmente la sincronizzazione della struttura della campagna e delle entità della campagna per le reti di annunci supportate.
exl-id: 185c6a01-c2e8-4bbb-a9dd-0a8200eb4792
feature: Search Campaign Management
source-git-commit: c2a1ce841a9dc99c57239f817dbd2065b91cdfb9
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# Sincronizzare manualmente i dati di rete degli annunci

*[!DNL Google Ads], [!DNL Microsoft® Advertising] (in precedenza [!DNL Bing Ads]), [!DNL Yahoo! Japan Ads], [!DNL Yandex], ed esistenti [!DNL Baidu] solo account*

La sincronizzazione è il processo tramite il quale Search, Social e Commerce raccoglie informazioni aggiornate per gli account di rete degli annunci collegati di ogni inserzionista su [reti pubblicitarie supportate](/help/search-social-commerce/introduction/supported-inventory.md). Questi dati includono la struttura della campagna dell’inserzionista e le entità della campagna, inclusa la maggior parte dei loro attributi gestiti o segnalati in Search, Social e Commerce. Non include i dati di clic, né le offerte e i modificatori di offerte immessi al di fuori di Search, Social e Commerce, che vengono raccolti separatamente.

Search, Social e Commerce sincronizzano automaticamente (sincronizzano) con gli account della rete di annunci una volta al giorno e anche ogni volta che rileva una nuova campagna su una delle reti di annunci. Inoltre, invia immediatamente alla rete di annunci tutte le modifiche apportate ai dati della campagna da Search, Social e Commerce.

Puoi richiedere manualmente la sincronizzazione di tutte le campagne attive e in pausa in account specifici o in campagne attive e in pausa specifiche. Questa attività raccoglie le entità sulla rete di annunci che sono nuove o modificate.

Per campagne con &quot;[!UICONTROL Auto Upload]&quot;, l’operazione di sincronizzazione genera e invia anche codici di tracciamento mancanti o che devono essere modificati nei modelli di tracciamento o negli URL di destinazione. Gli URL vengono generati in base ai parametri nelle impostazioni di tracciamento per le impostazioni account o la campagna. Se esistono URL di tracciamento per gli elementi rilevanti, questi non vengono rigenerati a meno che non siano necessari nuovi URL (ad esempio se il tipo di corrispondenza della parola chiave, il testo creativo o i parametri di tracciamento dell’account sono cambiati).

>[!NOTE]
>
>In qualsiasi momento [creare un bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md), è possibile eseguire la sincronizzazione con la rete dell’annuncio prima di creare il bulksheet.

1. Nel menu principale, fai clic su **[!UICONTROL Search]>[!UICONTROL Campaigns]**. Nel sottomenu, seleziona **[!UICONTROL Accounts]** per sincronizzare tutte le campagne in account specifici oppure **[!UICONTROL Campaigns]** per sincronizzare campagne specifiche.

1. (Facoltativo) Filtra l’elenco per includere account o campagne specifici.

1. Seleziona la casella di controllo accanto a ogni account o campagna da sincronizzare. Puoi sincronizzare fino a 50 campagne alla volta. Se si sincronizzano più di cinque account alla volta, il processo viene suddiviso in batch contenenti fino a cinque account ciascuno.

1. Clic **![Altro](/help/search-social-commerce/assets/more.png "Altro")** nella barra degli strumenti, quindi seleziona **[!UICONTROL Sync]**.

È possibile seguire lo stato del processo di sincronizzazione in [!UICONTROL Workspace] visualizzazione. La visualizzazione del processo potrebbe richiedere un&#39;ora o più.

>[!MORELIKETHIS]
>
>* [Scaricare/creare un file bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)
