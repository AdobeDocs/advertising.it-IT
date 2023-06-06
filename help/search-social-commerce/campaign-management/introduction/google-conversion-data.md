---
title: "[!DNL Google Ads] dati di conversione"
description: Scopri i tipi di [!DNL Google Ads]-Dati di conversione tracciati disponibili in Search, Social e Commerce.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '738'
ht-degree: 0%

---

# [!DNL Google Ads] dati di conversione in Search, Social e Commerce

Sincronizzazione automatica di Search, Social e Commerce [!DNL Google Ads]-ha tracciato i dati di conversione per tutte le tue campagne sul [!DNL Google Ads] cerca e acquista reti in Search, Social e Commerce per generare rapporti e ottimizzarli. Search, Social e Commerce sincronizzano i dati per le conversioni per le quali &quot;[!DNL Include in 'Conversions']L’opzione &quot; è abilitata, richiama i dati per gli ultimi 30 giorni e quindi richiama le modifiche ai dati ogni giorno.

## Dati di conversione disponibili

Fino a tre proprietà di transazione per ogni [[!DNL Google Ads]-conversione tracciata](https://support.google.com/google-ads/answer/4677036) (configurato in [!DNL Google Ads]) sono automaticamente disponibili in Search, Social e Commerce, utilizzando i nomi di conversione configurati in [!DNL Google Ads]. Le proprietà della transazione per ogni conversione includono:

* `GGL*` — (Quando la si tiene traccia) la somma dei valori di conversione per la parola chiave, a partire dal prefisso &quot;GGL&quot; (ad esempio GGL Purchase).

* `GGL_CT*` — il numero (conteggio) di conversioni, a partire dal prefisso &quot;GGL_CT&quot; (ad esempio GGL_CT_Purchase).

* `GGL_XD_CT*` — (Se disponibile per il tipo di conversione, quando vengono tracciati) Il numero (conteggio) delle conversioni tra dispositivi, misurato da Google, a partire dal prefisso &quot;GGL_XD_CT_&quot; (ad esempio GGL_XD_CT_Purchase).

I dati sono disponibili dalla data in cui la funzione è abilitata per l’account e viene aggiornata ogni giorno entro le ore 9:00-10:00 nel fuso orario dell’inserzionista.

[!DNL Google Ads] registra ogni conversione per [unità di offerta](/help/search-social-commerce/glossary.md#a-b), dispositivo e data di clic (non data di conversione). L’attribuzione si basa sull’impostazione di attribuzione predefinita per ogni metrica in [!DNL Google Ads]; L’attribuzione Adobe Advertising non viene considerata in perché i dati a livello di evento di clic non sono disponibili. Ogni giorno, Search, Social e Commerce estrae i dati di conversione per i 30 giorni precedenti e quindi calcola eventuali conversioni incrementali dal giorno precedente, utilizzando la data di clic da [!DNL Google Ads] e la data della transazione viene indicata come giorno precedente. Di conseguenza, i dati storici possono cambiare di giorno in giorno in quanto vengono tracciate le nuove conversioni per ogni clic. Se confronti i dati in Search, Social &amp; Commerce con quelli in [!DNL Google Ads], utilizzare l&#39;opzione di visualizzazione o di report per visualizzare &quot;[!UICONTROL Conversions by: Click date]&quot; (non per data di transazione).

Tutte le metriche sono automaticamente disponibili nelle viste di gestione delle campagne e nei rapporti di base e possono essere utilizzate anche negli obiettivi di portfolio per l’ottimizzazione.

>[!NOTE]
>
>* Se disponi di più account con gli stessi nomi di conversione, è possibile che in Adobe Advertising vengano visualizzati nomi di conversione duplicati. In tal caso, [modificare il nome visualizzato](/help/search-social-commerce/admin/transaction-properties/transaction-property-edit-display-name.md) per una delle metriche duplicate in [!UICONTROL Admin] > [!UICONTROL Transaction Properties]. Il reporting non è accurato quando due metriche diverse hanno lo stesso nome.
>* I dati a livello di unità di offerta corrispondono ai dati in [!DNL Google Ads] allo stesso livello. Tuttavia, [!DNL Google Ads]I dati di conversione di &#39; per i livelli superiori possono includere conversioni aggiuntive non attribuite alle unità di offerta figlio. I dati in Search, Social e Commerce vengono sempre aggregati dal livello di unità dell’offerta, pertanto, ad esempio, un rapporto a livello di campagna potrebbe non avere gli stessi totali di un rapporto a livello di campagna in Google Ads.
>* La varianza dei dati è in genere inferiore dopo la sincronizzazione mattutina rispetto a quella più tardi nel corso della giornata, quando non sono ancora state sincronizzate conversioni aggiuntive. È consigliabile convalidare i dati al mattino.
>* Dati di conversione non disponibili per [!DNL Google Display Network], [!DNL Gmail], [!DNL Mobile App], e [!DNL YouTube] annunci. Escludi questi tipi di annunci quando confronti i dati in [!DNL Google Ads] con dati in Search, Social e Commerce.
>* Dati per [!DNL Google Ads] Le conversioni non sono disponibili a livello di pubblico o di posizione geografica e pertanto non vengono utilizzate per ottimizzare automaticamente RLSA e le regolazioni delle offerte di posizione.


## Come confrontare i dati di conversione in [!DNL Google Ads] con dati in Search, Social e Commerce

Utilizza le seguenti impostazioni per i rapporti per convalidare dati confrontabili.

### Impostazioni dei rapporti da utilizzare in [!DNL Google Ads]

1. Nella barra degli strumenti principale, seleziona **[!DNL Reports]>[!DNL Report]**.

1. Seleziona **[!DNL + Custom]>[!DNL Table]**.

1. Dal riquadro di sinistra, specifica le righe e le colonne nel rapporto:

   1. Cerca **[!DNL Day]** e trascinarlo sul [!DNL Row] sezione.

   1. Cerca **[!DNL All conv].** e trascinarlo sul [!DNL Column] sezione.

   1. Cerca **[!DNL Conversion action]** e trascinarlo sul [!DNL Column] sezione.

1. Nella barra degli strumenti delle impostazioni del rapporto, seleziona **[!DNL Filter]>[!DNL Ad status]** e quindi selezionare tutte le caselle.

1. Nella barra degli strumenti delle impostazioni del rapporto, seleziona **[!DNL Download]>[!DNL Excel .csv]**.

### Impostazioni dei rapporti da utilizzare in Search, Social &amp; Commerce

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
>* [Informazioni sulla gestione delle campagne in Search, Social e Commerce](campaign-management-about.md)
>* [Panoramica dell’implementazione di account e campagne di ad network](campaign-implemention-overview.md)
>* [Monitorare e gestire le prestazioni delle campagne ad network](monitor-performance-campaigns.md)

