---
title: '''[!DNL Google Ads] dati di conversione"'
description: Scopri i tipi di [!DNL Google Ads]-Dati di conversione tracciati disponibili in Search, Social e Commerce.
exl-id: a7ee8e72-aa7d-4e90-b765-b7b01308762d
feature: Search Campaign Management, Conversions
source-git-commit: af32aea1c50edb6b22b0b15c920cb8c2dcdc37e9
workflow-type: tm+mt
source-wordcount: '668'
ht-degree: 0%

---

# [!DNL Google Ads] dati di conversione in Search, Social e Commerce

Sincronizzazione automatica di Search, Social e Commerce [!DNL Google Ads]-ha tracciato i dati di conversione per tutte le tue campagne sul [!DNL Google Ads] cerca e acquista reti in Search, Social e Commerce per generare rapporti e ottimizzarli.

Tutte le metriche sono automaticamente disponibili nelle viste di gestione delle campagne e nei rapporti di base e possono essere utilizzate anche negli obiettivi di portfolio per l’ottimizzazione.

## Dati di conversione disponibili

Search, Social e Commerce sincronizzano i dati per le conversioni per le quali &quot;[!DNL Include in 'Conversions']L’opzione &quot; è abilitata, richiama i dati per gli ultimi 35 giorni e quindi richiama le modifiche ai dati ogni giorno entro il 09:00-10:00 nel fuso orario dell’inserzionista. I dati storici possono cambiare di giorno in giorno, man mano che vengono tracciate nuove conversioni per ogni clic.

Fino a tre metriche per ciascuno [[!DNL Google Ads]-conversione tracciata](https://support.google.com/google-ads/answer/4677036) (configurato in [!DNL Google Ads]) sono automaticamente disponibili in Search, Social e Commerce, utilizzando i nomi di conversione configurati in [!DNL Google Ads]. Le metriche di ciascuna conversione includono:

<!--

* `<conversion-name>` &mdash; (When you track it) The conversion value for the keyword, beginning with the "GGL" prefix (such as GGL Purchase).

`CT_<conversion-name>` &mdash; The number (count) of conversions, beginning with the "GGL_CT" prefix (such as GGL_CT_Purchase).

* `XD_<conversion-name>` &mdash; (When available for the conversion type, when you track them) The number (count) of cross-device conversions, as measured by Google, beginning with the "GGL_XD_CT_" prefix (such as GGL_XD_CT_Purchase).

-->

* `GGL*` — (Quando viene tracciato) il valore di conversione per la parola chiave, a partire dal prefisso &quot;GGL&quot; (ad esempio Acquisto GGL).

* `GGL_CT*` — il numero (conteggio) di conversioni, a partire dal prefisso &quot;GGL_CT&quot; (ad esempio GGL_CT_Purchase).

* `GGL_XD_CT*` — (Se disponibile per il tipo di conversione, quando vengono tracciati) Il numero (conteggio) delle conversioni tra dispositivi, misurato da Google, a partire dal prefisso &quot;GGL_XD_CT_&quot; (ad esempio GGL_XD_CT_Purchase).

[!DNL Google Ads] registra ogni conversione per [unità di offerta](/help/search-social-commerce/glossary.md#a-b), dispositivo e data di clic (non data di conversione). L’attribuzione si basa sull’impostazione di attribuzione predefinita per ogni metrica in [!DNL Google Ads]; l’attribuzione di Adobe Advertising non è inclusa perché i dati a livello di evento clic non sono disponibili.

>[!NOTE]
>
>* Se disponi di più account con gli stessi nomi di conversione, è possibile che in Adobe Advertising vengano visualizzati nomi di conversione duplicati. In tal caso, [modificare il nome visualizzato](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md per una delle metriche duplicate in [!UICONTROL Admin] > [!UICONTROL Conversions]. Il reporting non è accurato quando due metriche diverse hanno lo stesso nome.
>* I dati a livello di unità di offerta corrispondono ai dati in [!DNL Google Ads] allo stesso livello. Tuttavia, [!DNL Google Ads]I dati di conversione di &#39; per i livelli superiori possono includere conversioni aggiuntive non attribuite alle unità di offerta figlio. I dati in Search, Social e Commerce vengono sempre aggregati dal livello di unità dell’offerta, pertanto, ad esempio, un rapporto a livello di campagna potrebbe non avere gli stessi totali di un rapporto a livello di campagna in Google Ads.
>* La varianza dei dati è in genere inferiore dopo la sincronizzazione mattutina rispetto a quella più tardi nel corso della giornata, quando non sono ancora state sincronizzate conversioni aggiuntive. È consigliabile convalidare i dati al mattino.
>* Dati di conversione non disponibili per [!DNL Google Display Network], [!DNL Gmail], [!DNL Mobile App], e [!DNL YouTube] annunci. Escludi questi tipi di annunci quando confronti i dati in [!DNL Google Ads] con dati in Search, Social e Commerce.
>* Dati per [!DNL Google Ads] Le conversioni non sono disponibili a livello di pubblico o di posizione geografica e pertanto non vengono utilizzate per ottimizzare automaticamente RLSA e le regolazioni delle offerte di posizione.

## Come confrontare i dati di conversione in [!DNL Google Ads] con dati in Search, Social e Commerce

Se confronti i dati in Search, Social &amp; Commerce con quelli in [!DNL Google Ads], utilizzare l&#39;opzione di visualizzazione o di report per visualizzare le conversioni in base alla data di clic (non alla data della transazione).

Utilizza le seguenti impostazioni per i rapporti per convalidare dati confrontabili.

### Impostazioni dei rapporti da utilizzare in [!DNL Google Ads]

Genera il rapporto per le azioni di conversione selezionate per giorno e include i dati per tutti gli stati degli annunci.

<!-- 

1. In the main toolbar, select **[!DNL Reports] > [!DNL Report]**.

1. Select **[!DNL + Custom] > [!DNL Table]**.

1. From the left pane, specify the rows and columns in the report:
   
   1. Search for the **[!DNL Day]** field and it drag to the [!DNL Row] section.

   1. Search for the **[!DNL All conv].** field and it drag to the [!DNL Column] section.

   1. Search for the **[!DNL Conversion action]** field and it drag to the [!DNL Column] section.

1. In the report settings toolbar, select **[!DNL Filter] > [!DNL Ad status]**, and then select all boxes.

1. In the report settings toolbar, select **[!DNL Download] > [!DNL Excel .csv]**.

-->

### Impostazioni dei rapporti da utilizzare in Search, Social &amp; Commerce

In Search, Social e Commerce, utilizza l’opzione di visualizzazione o di rapporto per visualizzare le conversioni in base alla data di clic (non alla data della transazione).

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**.

1. Nella barra degli strumenti sopra la tabella dati, fai clic su **[!UICONTROL Create Report]**, tenere premuto il cursore **[!UICONTROL Basic Reports]** e quindi fare clic su **[!UICONTROL Search Engine Account Report]**.

1. In [!UICONTROL Report Settings] , specificare le seguenti impostazioni di report:

   1. In **[!UICONTROL Conversions Based]** nella sezione, seleziona **[!UICONTROL Click date]**.

   1. Specifica lo stesso intervallo di date utilizzato per il [!DNL Google Ads] rapporto.

   1. In **[!UICONTROL Search/Content]** sezione, seleziona **[!UICONTROL Search Only]**.

   1. In **[!UICONTROL Search Engine Hierarchy]** , espandere la sezione [!UICONTROL Google Adwords] e selezionare l&#39;account.

   1. Apri [!UICONTROL Columns] e aggiungi il [!DNL Google Ads] metriche (a partire da &quot;GGL&quot;) che desideri confrontare.

1. Clic **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Panoramica dell’implementazione di account e campagne di ad network](campaign-implemention-overview.md)
>* [Monitorare e gestire le prestazioni delle campagne ad network](monitor-performance-campaigns.md)
>* [Visualizzare le metriche di conversione tracciate per un inserzionista](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
>* [Creare un tag di conversione per [!DNL Google Ads]](/help/search-social-commerce/admin/conversion-metrics/conversion-tag-google.md)
