---
title: '''[!DNL Microsoft Advertising] dati di conversione"'
description: Scopri i tipi di [!DNL Microsoft Advertising]-Dati di conversione tracciati disponibili in Search, Social e Commerce.
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] dati di conversione in Search, Social e Commerce

Search, Social e Commerce sincronizzano automaticamente tutte le conversioni tracciate dal [Tag UET (Universal Event Tracking) di Microsoft Advertising](https://about.ads.microsoft.com/solutions/tools/universal-event-tracking) per conversioni di siti web, incluse le conversioni view-through, per reporting e ottimizzazione.

Tutte le metriche sono automaticamente disponibili nelle viste di gestione delle campagne e nei rapporti di base e possono essere utilizzate anche negli obiettivi di portfolio per l’ottimizzazione delle campagne Microsoft Advertising.

## Dati di conversione disponibili

Search, Social e Commerce sincronizzano i dati per le conversioni per le quali &quot;[!DNL Include in 'Conversions']L’opzione &quot; è abilitata, richiama i dati per gli ultimi 35 giorni e quindi richiama le modifiche ai dati ogni giorno entro il 09:00-10:00 nel fuso orario dell’inserzionista. I dati storici possono cambiare di giorno in giorno, man mano che vengono tracciate nuove conversioni per ogni clic.

Due proprietà di transazione per ogni [[!DNL Microsoft Advertising]-conversione tracciata](https://help.ads.microsoft.com/apex/index/3/en-us/n5012) (configurato in [!DNL Microsoft Advertising]) sono automaticamente disponibili in Search, Social e Commerce, utilizzando i nomi di conversione configurati in [!DNL Microsoft Advertising]. Le proprietà della transazione per ogni conversione includono:

* `<conversion-name>` — il valore di conversione per la parola chiave (ad esempio Acquisto).

  >[!TIP]
  >
  >Utilizza questo tipo di proprietà nell’obiettivo per i portfolio che includono [!DNL Microsoft Advertising] con il valore di conversione massimo e le strategie di offerta ROAS di Target.

* `CT_<conversion-name>` — Il numero (conteggio) delle conversioni, a partire dal prefisso &quot;CT_&quot; (ad esempio CT_Purchase).

  >[!TIP]
  >
  >Utilizza questo tipo di proprietà nell’obiettivo per i portfolio che includono [!DNL Microsoft Advertising] campagne con le strategie di offerta Max Conversions e Target CPA.

I dati sono disponibili in base all’ora di clic e all’ora di conversione/transazione dalla data in cui la funzione è abilitata per il conto.

[!DNL Microsoft Advertising] registra ogni conversione per [unità di offerta](/help/search-social-commerce/glossary.md#a-b), dispositivo e data di clic (non data di conversione). L’attribuzione si basa sull’impostazione di attribuzione predefinita per ogni metrica in [!DNL Microsoft Advertising]; l’attribuzione di Adobe Advertising non è inclusa perché i dati a livello di evento clic non sono disponibili.

>[!NOTE]
>
>* Se disponi di più account con gli stessi nomi di conversione, in Adobi Advertising potrebbero essere presenti nomi di conversione duplicati. In tal caso, [modificare il nome visualizzato](/help/search-social-commerce/admin/transaction-properties/transaction-property-edit-display-name.md) per una delle metriche duplicate in [!UICONTROL Admin] > [!UICONTROL Transaction Properties]. Il reporting non è accurato quando due metriche diverse hanno lo stesso nome.
>* I dati a livello di unità di offerta corrispondono ai dati nella rete di annunci allo stesso livello. Tuttavia, i dati di conversione della rete di annunci per i livelli superiori possono includere conversioni aggiuntive che non sono attribuite alle unità di offerta figlie. I dati in Search, Social e Commerce vengono sempre aggregati dal livello di unità dell’offerta, pertanto, ad esempio, un rapporto a livello di campagna potrebbe non avere gli stessi totali di un rapporto a livello di campagna nella rete di annunci.
>* La varianza dei dati è in genere inferiore dopo la sincronizzazione mattutina rispetto a quella più tardi nel corso della giornata, quando non sono ancora state sincronizzate conversioni aggiuntive. È consigliabile convalidare i dati al mattino.
>* I dati non sono disponibili a livello di pubblico o di posizione geografica e pertanto non vengono utilizzati per ottimizzare automaticamente RLSA e le regolazioni delle offerte di posizione.

## Come confrontare i dati di conversione in [!DNL Microsoft Advertising] con dati in Search, Social e Commerce

Utilizza le seguenti impostazioni per i rapporti per convalidare dati confrontabili.

### Impostazioni dei rapporti da utilizzare in [!DNL Microsoft Advertising]

Genera il rapporto per le azioni di conversione selezionate per giorno e include i dati per tutti gli stati degli annunci.

### Impostazioni dei rapporti da utilizzare in Search, Social &amp; Commerce

In Search, Social e Commerce, utilizza l’opzione di visualizzazione o di rapporto per visualizzare le conversioni in base alla data di clic (non alla data della transazione).

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**.

1. Nella barra degli strumenti sopra la tabella dati, fai clic su **[!UICONTROL Create Report]**, tenere premuto il cursore **[!UICONTROL Basic Reports]** e quindi fare clic su **[!UICONTROL Search Engine Account Report]**.

1. In [!UICONTROL Report Settings] , specificare le seguenti impostazioni di report:

   1. In **[!UICONTROL Conversions Based]** nella sezione, seleziona **[!UICONTROL Click date]**.

   1. Specifica lo stesso intervallo di date utilizzato per il [!DNL Microsoft Advertising] rapporto.

   1. In **[!UICONTROL Search/Content]** sezione, seleziona **[!UICONTROL Search Only]**.

   1. In **[!UICONTROL Search Engine Hierarchy]** , espandere la sezione [!UICONTROL Microsoft Advertising] e selezionare l&#39;account.

   1. Apri [!UICONTROL Columns] e aggiungi il [!DNL Microsoft Advertising] metriche da confrontare.

1. Clic **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Panoramica dell’implementazione di account e campagne di ad network](campaign-implemention-overview.md)
>* [Monitorare e gestire le prestazioni delle campagne ad network](monitor-performance-campaigns.md)
>* [Visualizzare le proprietà della transazione tracciate per un inserzionista](/help/search-social-commerce/admin/transaction-properties/transaction-property-view-tracked.md)
