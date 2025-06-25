---
title: '[!DNL Google Ads] dati di conversione'
description: Scopri i tipi di dati di conversione tracciati da  [!DNL Google Ads] disponibili in Search, Social e Commerce.
exl-id: a4634410-446b-4e2e-a52f-22a494f731f9
feature: Search Campaign Management, Conversions
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '661'
ht-degree: 0%

---

# [!DNL Google Ads] dati di conversione in Search, Social e Commerce

Search, Social e Commerce sincronizzano automaticamente i dati di conversione tracciati da [!DNL Google Ads] per tutte le campagne sulle reti di ricerca e shopping di [!DNL Google Ads] in Search, Social e Commerce per il reporting e l&#39;ottimizzazione.

Tutte le metriche sono automaticamente disponibili nelle viste di gestione delle campagne e nei rapporti di base e possono essere utilizzate anche negli obiettivi di portfolio per l’ottimizzazione.

## Dati di conversione disponibili

Cerca, Social e Commerce sincronizzano i dati per le conversioni per le quali è abilitata l&#39;opzione &quot;[!DNL Include in 'Conversions']&quot;, estraendo i dati per gli ultimi 35 giorni e quindi estraendo le modifiche ai dati ogni giorno entro le 09:00-10:00 nel fuso orario dell&#39;inserzionista. I dati storici possono cambiare di giorno in giorno, man mano che vengono tracciate nuove conversioni per ogni clic.

In Search, Social e Commerce sono automaticamente disponibili fino a tre metriche per ogni conversione [[!DNL Google Ads] tracciata](https://support.google.com/google-ads/answer/4677036) (configurata in [!DNL Google Ads]) utilizzando i nomi di conversione configurati in [!DNL Google Ads]. Le metriche di ciascuna conversione includono:

<!--

* `<conversion-name>` &mdash; (When you track it) The conversion value for the keyword, beginning with the "GGL" prefix (such as GGL Purchase).

`CT_<conversion-name>` &mdash; The number (count) of conversions, beginning with the "GGL_CT" prefix (such as GGL_CT_Purchase).

* `XD_<conversion-name>` &mdash; (When available for the conversion type, when you track them) The number (count) of cross-device conversions, as measured by Google, beginning with the "GGL_XD_CT_" prefix (such as GGL_XD_CT_Purchase).

-->

* `GGL*` — (quando viene tracciato) il valore di conversione per la parola chiave, a partire dal prefisso &quot;GGL&quot; (ad esempio Acquisto GGL).

* `GGL_CT*` — Numero (conteggio) di conversioni, a partire dal prefisso &quot;GGL_CT&quot; (ad esempio GGL_CT_Purchase).

* `GGL_XD_CT*` — (se disponibile per il tipo di conversione, quando vengono tracciati) Il numero (conteggio) di conversioni tra dispositivi, misurato da Google, a partire dal prefisso &quot;GGL_XD_CT_&quot; (ad esempio GGL_XD_CT_Purchase).

[!DNL Google Ads] registra ogni conversione per [unità offerta](/help/search-social-commerce/glossary.md#a-b), dispositivo e data di clic (non data di conversione). L&#39;attribuzione si basa sull&#39;impostazione di attribuzione predefinita per ogni metrica in [!DNL Google Ads]. L&#39;attribuzione Adobe Advertising non è inclusa perché i dati a livello di evento di clic non sono disponibili.

>[!NOTE]
>
>* Se disponi di più account con gli stessi nomi di conversione, è possibile che vengano visualizzati nomi di conversione duplicati in Adobe Advertising. In questo caso, [modificare il nome visualizzato](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md) per una delle metriche duplicate in [!UICONTROL Admin] > [!UICONTROL Conversions]. Il reporting non è accurato quando due metriche diverse hanno lo stesso nome.
>* I dati a livello di unità di offerta corrispondono ai dati in [!DNL Google Ads] allo stesso livello. Tuttavia, i dati di conversione di [!DNL Google Ads] per i livelli superiori possono includere conversioni aggiuntive non attribuite alle unità di offerta figlio. I dati in Search, Social e Commerce vengono sempre aggregati dal livello di unità dell’offerta, pertanto un rapporto a livello di campagna potrebbe non avere gli stessi totali di un rapporto a livello di campagna in Google Ads.
>* La varianza dei dati è in genere inferiore dopo la sincronizzazione mattutina rispetto a quella più tardi nel corso della giornata, quando non sono ancora state sincronizzate conversioni aggiuntive. È consigliabile convalidare i dati al mattino.
>* I dati di conversione non sono disponibili per [!DNL Google Display Network], [!DNL Gmail], [!DNL Mobile App] e [!DNL YouTube] annunci. Escludi questi tipi di annunci quando confronti i dati in [!DNL Google Ads] con i dati di Search, Social e Commerce.
>* I dati per le conversioni [!DNL Google Ads] non sono disponibili a livello di pubblico o di posizione geografica e pertanto non vengono utilizzati per ottimizzare automaticamente RLSA e le regolazioni delle offerte di posizione.

## Come confrontare i dati di conversione in [!DNL Google Ads] con i dati di Search, Social e Commerce

Se si confrontano i dati di Search, Social e Commerce con quelli di [!DNL Google Ads], utilizzare l&#39;opzione di visualizzazione o di report per visualizzare le conversioni in base alla data di clic (non alla data della transazione).

Utilizza le seguenti impostazioni per i rapporti per convalidare dati confrontabili.

### Impostazioni dei report da utilizzare in [!DNL Google Ads]

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

### Impostazioni dei rapporti da utilizzare in Search, Social e Commerce

In Ricerca, Social e Commerce, utilizza l’opzione di visualizzazione o di rapporto per visualizzare le conversioni in base alla data di clic (non alla data della transazione).

1. Nel menu principale, fare clic su **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**.

1. Nella barra degli strumenti sopra la tabella dati fare clic su **[!UICONTROL Create Report]**, tenere premuto il cursore su **[!UICONTROL Basic Reports]** e quindi fare clic su **[!UICONTROL Search Engine Account Report]**.

1. Nella finestra [!UICONTROL Report Settings], specificare le impostazioni di report seguenti:

   1. Nella sezione **[!UICONTROL Conversions Based]** su, selezionare **[!UICONTROL Click date]**.

   1. Specificare lo stesso intervallo di date utilizzato per il report [!DNL Google Ads].

   1. Nella sezione **[!UICONTROL Search/Content]**, selezionare **[!UICONTROL Search Only]**.

   1. Nella sezione **[!UICONTROL Search Engine Hierarchy]**, espandi la sezione [!UICONTROL Google Adwords] e seleziona l&#39;account.

   1. Apri la scheda [!UICONTROL Columns] e aggiungi le metriche [!DNL Google Ads] (a partire da &quot;GGL&quot;) che desideri confrontare.

1. Fare clic su **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Panoramica sull&#39;implementazione di account e campagne di ad network](campaign-implemention-overview.md)
>* [Monitora e gestisci le prestazioni delle campagne della rete di annunci](monitor-performance-campaigns.md)
>* [Visualizza le metriche di conversione rilevate per un inserzionista](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
>* [Crea un tag di conversione per [!DNL Google Ads]](/help/search-social-commerce/admin/conversion-metrics/conversion-tag-google.md)
>* [Carica dati di conversione offline per conversioni avanzate](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
