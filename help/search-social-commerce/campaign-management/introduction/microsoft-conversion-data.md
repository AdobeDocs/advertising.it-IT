---
title: '[!DNL Microsoft Advertising] dati di conversione'
description: Scopri i tipi di dati di conversione tracciati da  [!DNL Microsoft Advertising] disponibili in Search, Social e Commerce.
feature: Search Campaign Management, Conversions
exl-id: 0ebc70a0-1fb7-48db-b45d-7409e8bb6f64
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] dati di conversione in Search, Social e Commerce

Search, Social e Commerce sincronizzano automaticamente tutte le conversioni tracciate dai [[!DNL Microsoft Advertising] tag UET (Universal Event Tracking)](https://help.ads.microsoft.com/#apex/ads/en/53056) per le conversioni di siti Web, incluse le conversioni view-through, per il reporting e l&#39;ottimizzazione.

Tutte le metriche sono automaticamente disponibili nelle viste di gestione delle campagne e nei report di base e possono essere utilizzate anche negli obiettivi di portfolio per l&#39;ottimizzazione di [!DNL Microsoft Advertising] campagne.

## Dati di conversione disponibili

Cerca, Social e Commerce sincronizzano i dati per le conversioni per le quali è abilitata l&#39;opzione &quot;[!DNL Include in 'Conversions']&quot;, estraendo i dati per gli ultimi 35 giorni e quindi estraendo le modifiche ai dati ogni giorno entro le 09:00-10:00 nel fuso orario dell&#39;inserzionista. I dati storici possono cambiare di giorno in giorno, man mano che vengono tracciate nuove conversioni per ogni clic.

Due metriche per ogni conversione [[!DNL Microsoft Advertising] monitorata](https://help.ads.microsoft.com/apex/index/3/en-us/n5012) (configurata in [!DNL Microsoft Advertising]) sono automaticamente disponibili in Search, Social e Commerce, utilizzando i nomi di conversione configurati in [!DNL Microsoft Advertising]. Le metriche di ciascuna conversione includono:

* `<conversion-name>` — Valore di conversione per la parola chiave (ad esempio Acquisto).

  >[!TIP]
  >
  >Utilizzare questo tipo di metrica di conversione nell&#39;obiettivo per i portfolio che includono campagne [!DNL Microsoft Advertising] con il valore di conversione massimo e le strategie di offerta ROAS di destinazione.

* `CT_<conversion-name>` — Numero (conteggio) di conversioni, a partire dal prefisso &quot;CT_&quot; (ad esempio CT_Purchase).

  >[!TIP]
  >
  >Utilizzare questo tipo di metrica di conversione nell&#39;obiettivo per i portfolio che includono campagne [!DNL Microsoft Advertising] con le strategie di offerta Max Conversions e Target CPA.

I dati sono disponibili in base all’ora di clic e all’ora di conversione/transazione dalla data in cui la funzione è abilitata per il conto.

[!DNL Microsoft Advertising] registra ogni conversione per [unità offerta](/help/search-social-commerce/glossary.md#a-b), dispositivo e data di clic (non data di conversione). L&#39;attribuzione si basa sull&#39;impostazione di attribuzione predefinita per ogni metrica in [!DNL Microsoft Advertising]. L&#39;attribuzione Adobe Advertising non è inclusa perché i dati a livello di evento di clic non sono disponibili.

>[!NOTE]
>
>* Se disponi di più account con gli stessi nomi di conversione, è possibile che vengano visualizzati nomi di conversione duplicati in Adobe Advertising. In questo caso, [modificare il nome visualizzato](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md) per una delle metriche duplicate in [!UICONTROL Admin] > [!UICONTROL Conversions]. Il reporting non è accurato quando due metriche diverse hanno lo stesso nome.
>* I dati a livello di unità di offerta corrispondono ai dati nella rete di annunci allo stesso livello. Tuttavia, i dati di conversione della rete di annunci per i livelli superiori possono includere conversioni aggiuntive che non sono attribuite alle unità di offerta figlie. I dati in Search, Social e Commerce vengono sempre aggregati dal livello di unità dell’offerta, pertanto, ad esempio, un rapporto a livello di campagna potrebbe non avere gli stessi totali di un rapporto a livello di campagna nella rete di annunci.
>* La varianza dei dati è in genere inferiore dopo la sincronizzazione mattutina rispetto a quella più tardi nel corso della giornata, quando non sono ancora state sincronizzate conversioni aggiuntive. È consigliabile convalidare i dati al mattino.
>* I dati non sono disponibili a livello di pubblico o di posizione geografica e pertanto non vengono utilizzati per ottimizzare automaticamente RLSA e le regolazioni delle offerte di posizione.

## Come confrontare i dati di conversione in [!DNL Microsoft Advertising] con i dati di Search, Social e Commerce

Utilizza le seguenti impostazioni per i rapporti per convalidare dati confrontabili.

### Impostazioni dei report da utilizzare in [!DNL Microsoft Advertising]

Genera il rapporto per le azioni di conversione selezionate per giorno e include i dati per tutti gli stati degli annunci.

### Impostazioni dei rapporti da utilizzare in Search, Social e Commerce

In Ricerca, Social e Commerce, utilizza l’opzione di visualizzazione o di rapporto per visualizzare le conversioni in base alla data di clic (non alla data della transazione).

1. Nel menu principale, fare clic su **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**.

1. Nella barra degli strumenti sopra la tabella dati fare clic su **[!UICONTROL Create Report]**, tenere premuto il cursore su **[!UICONTROL Basic Reports]** e quindi fare clic su **[!UICONTROL Search Engine Account Report]**.

1. Nella finestra [!UICONTROL Report Settings], specificare le impostazioni di report seguenti:

   1. Nella sezione **[!UICONTROL Conversions Based]** su, selezionare **[!UICONTROL Click date]**.

   1. Specificare lo stesso intervallo di date utilizzato per il report [!DNL Microsoft Advertising].

   1. Nella sezione **[!UICONTROL Search/Content]**, selezionare **[!UICONTROL Search Only]**.

   1. Nella sezione **[!UICONTROL Search Engine Hierarchy]**, espandi la sezione [!UICONTROL Microsoft Advertising] e seleziona l&#39;account.

   1. Aprire la scheda [!UICONTROL Columns] e aggiungere le metriche [!DNL Microsoft Advertising] che si desidera confrontare.

1. Fare clic su **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Panoramica sull&#39;implementazione di account e campagne di ad network](campaign-implemention-overview.md)
>* [Monitora e gestisci le prestazioni delle campagne della rete di annunci](monitor-performance-campaigns.md)
>* [Visualizza le metriche di conversione rilevate per un inserzionista](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
