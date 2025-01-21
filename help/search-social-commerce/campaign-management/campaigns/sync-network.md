---
title: Sincronizzare manualmente i dati di rete degli annunci
description: Scopri come attivare manualmente la sincronizzazione della struttura della campagna e delle entità della campagna per le reti di annunci supportate.
exl-id: 185c6a01-c2e8-4bbb-a9dd-0a8200eb4792
feature: Search Campaign Management
source-git-commit: c4600e6ef41193f09722052ef9b16fe5d07bdaaf
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# Sincronizzare manualmente i dati di rete degli annunci

Solo *[!DNL Google Ads], [!DNL Microsoft Advertising] (in precedenza [!DNL Bing Ads]), [!DNL Yahoo! Japan Ads], [!DNL Yandex] e [!DNL Baidu] account esistenti*

La sincronizzazione è il processo tramite il quale Search, Social e Commerce raccolgono informazioni aggiornate per gli account di rete pubblicitaria connessi di ogni inserzionista su [reti pubblicitarie supportate](/help/search-social-commerce/introduction/supported-inventory.md). Questi dati includono la struttura della campagna dell’inserzionista e le entità della campagna, inclusa la maggior parte dei loro attributi gestiti o segnalati in Search, Social e Commerce. Non include i dati sui clic, né le offerte e i modificatori di offerte immessi all’esterno di Search, Social e Commerce, che vengono raccolti separatamente.

Search, Social e Commerce si sincronizzano (sincronizzano) automaticamente con gli account della rete di annunci una volta al giorno e ogni volta che rilevano una nuova campagna su una delle reti di annunci. Inoltre, invia immediatamente alla rete di annunci tutte le modifiche apportate ai dati della campagna dall’interno di Search, Social e Commerce.

Puoi richiedere manualmente la sincronizzazione di tutte le campagne attive e in pausa in account specifici o in campagne attive e in pausa specifiche. Questa attività raccoglie le entità sulla rete di annunci che sono nuove o modificate.

Per le campagne con l&#39;opzione &quot;[!UICONTROL Auto Upload]&quot;, anche l&#39;operazione di sincronizzazione genera e invia codici di tracciamento mancanti o che devono essere modificati nei modelli di tracciamento o negli URL di destinazione. Gli URL vengono generati in base ai parametri nelle impostazioni di tracciamento per le impostazioni account o la campagna. Se esistono URL di tracciamento per gli elementi rilevanti, questi non vengono rigenerati a meno che non siano necessari nuovi URL (ad esempio se il tipo di corrispondenza della parola chiave, il testo creativo o i parametri di tracciamento dell’account sono cambiati).

>[!NOTE]
>
>Ogni volta che si [crea un bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md), è possibile eseguire la sincronizzazione con la rete di annunci prima della creazione del bulksheet.

1. Nel menu principale, fare clic su **[!UICONTROL Search]>[!UICONTROL Campaigns]**. Nel sottomenu, selezionare **[!UICONTROL Accounts]** per sincronizzare tutte le campagne in account specifici oppure **[!UICONTROL Campaigns]** per sincronizzare campagne specifiche.

1. (Facoltativo) Filtra l’elenco per includere account o campagne specifici.

1. Seleziona la casella di controllo accanto a ogni account o campagna da sincronizzare. Puoi sincronizzare fino a 50 campagne alla volta. Se si sincronizzano più di cinque account alla volta, il processo viene suddiviso in batch contenenti fino a cinque account ciascuno.

1. Fai clic su ![**Altro**](/help/search-social-commerce/assets/more.png " Altro") nella barra degli strumenti, quindi seleziona **[!UICONTROL Sync]**.

È possibile seguire lo stato del processo di sincronizzazione nella visualizzazione [!UICONTROL Workspace]. Il processo può richiedere
un&#39;ora o più per la visualizzazione.

>[!MORELIKETHIS]
>
>* [Scaricare/creare un file bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)
