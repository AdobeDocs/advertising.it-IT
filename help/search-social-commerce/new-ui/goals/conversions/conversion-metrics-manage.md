---
title: Gestire le metriche di conversione di un inserzionista
description: Scopri come utilizzare le metriche di conversione tracciate da Adobe Advertising per un inserzionista.
feature: Conversions
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
  - id: e6916c1b-e939-4e0b-99f5-768e83e1e99f
subfeature_v2:
  - id: d068b149-b9d1-421c-9033-a51495366ddc
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 9af7fb2602fa64f7785ff67fc6af27c59b8a678a
workflow-type: tm+mt
source-wordcount: 937
ht-degree: 0%

---

# (Nuova interfaccia utente) Gestione e visualizzazione dei dati sulle prestazioni per le metriche di conversione di un inserzionista

*funzionalità Beta*

Le metriche di [conversione](/help/search-social-commerce/glossary.md#c-d) di un inserzionista vengono utilizzate in Adobe Advertising:

* In Search, Social e Commerce i dati per le metriche di conversione possono essere visualizzati in colonne nelle viste Campagna, Portfolio e Gestione obiettivi, nonché nei rapporti. Gli utenti con privilegi di accesso sufficienti possono inoltre utilizzare metriche di conversione per creare obiettivi, utilizzati per ottimizzare i portfolio.

* (Per gli inserzionisti che fanno uso di Advertising DSP) In DSP puoi includere le metriche di conversione nelle visualizzazioni di gestione delle campagne, negli obiettivi personalizzati e nei rapporti personalizzati. È inoltre possibile utilizzare le metriche di conversione per creare [obiettivi personalizzati](/help/dsp/admin/custom-objectives-manage.md), utilizzati per ottimizzare i pacchetti.

Le metriche disponibili includono:

* Metriche di conversione di cui Adobe Advertising tiene traccia per un inserzionista.

* [Metriche di conversione e coinvolgimento sito sincronizzate da Adobe Analytics](/help/integrations/analytics/analytics-data-in-advertising.md).

* [Eventi del sito sincronizzati da Adobe Customer Journey Analytics](/help/integrations/customer-journey-analytics/overview.md).

* Conversioni tracciate da [!DNL Google Ads] e conversioni tracciate da [!DNL Microsoft Advertising] tag di tracciamento eventi universali.

* (Quando [hai configurato una specifica [!DNL Google Analytics] combinazione di account, proprietà e visualizzazione come origine dati](/help/search-social-commerce/admin/data-sources/data-source-about.md) per Search, Social e Commerce) Le conversioni sono monitorate da [!DNL Google Analytics].

* Conversioni da feed personalizzati.

Dall’elenco delle metriche di conversione disponibili, ogni utente con accesso ai dati dell’inserzionista può personalizzare le metriche visualizzate disponibili per le visualizzazioni e i rapporti di gestione, includendo o omettendo metriche specifiche a propria scelta. Puoi utilizzare un nome di metrica esattamente come è scritto nei dati recuperati oppure modificare il nome visualizzato nelle intestazioni di colonna per migliorarne la leggibilità.

>[!IMPORTANT]
>
>Per impostazione predefinita, nessuna delle metriche di conversione di un inserzionista, ad eccezione delle conversioni monitorate da [!DNL Google Ads], [!DNL Google Analytics] e [!DNL Microsoft Advertising] tag di tracciamento eventi universali, è disponibile per l&#39;inclusione nelle visualizzazioni, negli obiettivi e nei report di gestione delle campagne e dei portfolio. Per rendere disponibile una metrica di conversione, devi renderla esplicitamente disponibile.
>
>Le nuove conversioni tracciate dai tag di tracciamento degli eventi universali [!DNL Google Ads], [!DNL Google Analytics] e [!DNL Microsoft Advertising] sono sempre disponibili automaticamente.

>[!TIP]
>
>Quando l&#39;inserzionista (o la rete di annunci) interrompe la raccolta di una metrica di conversione, [nasconderla dalle visualizzazioni di gestione e dai report](#conversion-metrics-change-available) a meno che non si desideri utilizzarla per visualizzare i dati storici.

## Visualizzare le metriche di conversione tracciate per un inserzionista

* Nel menu principale, fare clic su **[!UICONTROL Goals]>[!UICONTROL Conversions]**.

Sono elencate tutte le metriche di conversione raccolte per l’inserzionista e tutti i diversi nomi visualizzati assegnati. Ogni riga di metrica include l’origine della metrica.

## Modificare il nome visualizzato di una metrica di conversione

Se ad esempio si raccolgono i dati di registrazione utilizzando una metrica di conversione denominata *reg*, è possibile modificare il nome visualizzato in modo che venga visualizzato come &quot;Registrazioni&quot;.

Impossibile eliminare un nome visualizzato esistente.

>[!NOTE]
>
>Per [metriche da [!DNL Google Analytics]](/help/search-social-commerce/admin/data-sources/data-source-about.md), eventuali modifiche manuali al nome visualizzato vengono sovrascritte se si aggiorna o si autentica nuovamente l&#39;integrazione. Analogamente, qualsiasi modifica del nome in [!DNL Google Analytics] viene ignorata a meno che non si [aggiorni](/help/search-social-commerce/admin/data-sources/data-source-edit.md) o [riautentichi](/help/search-social-commerce/admin/data-sources/data-source-reauthenticate.md) l&#39;integrazione.

1. Nel menu principale, fare clic su **[!UICONTROL Goals]>[!UICONTROL Conversions]**.

1. Filtra l&#39;elenco [dalla barra degli strumenti](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) o da un&#39;intestazione [colonna](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md).

1. Nella colonna **[!UICONTROL Conversion Display Name]** per la metrica, posizionare il cursore sul nome della metrica e fare clic su **...** > **[!UICONTROL Rename]**.

1. Immettere il nome da visualizzare, quindi fare clic su **[!UICONTROL Apply]**.

   I nomi visualizzati devono essere univoci e non possono includere i seguenti caratteri speciali: `\"<'>&`

## Modificare le metriche di conversione disponibili nelle visualizzazioni di gestione, negli obiettivi e nei rapporti {#conversion-metrics-change-available}

>[!NOTE]
>
>Quando nascondi una metrica di conversione precedentemente disponibile, questa viene rimossa da tutte le metriche derivate che la contengono.

1. Nel menu principale, fare clic su **[!UICONTROL Goals]>[!UICONTROL Conversions]**.

   Sono elencate tutte le metriche di conversione raccolte per l’inserzionista e tutti i nomi diversi specificati per la visualizzazione.

1. (Facoltativo) Filtra l&#39;elenco [dalla barra degli strumenti](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) o da un&#39;intestazione [colonna](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md).

1. Modificare le metriche di conversione disponibili per le visualizzazioni e i rapporti di gestione:

   * Per mostrare o nascondere una singola metrica, fare clic sull&#39;opzione nella colonna **[!UICONTROL Visibility]** per modificare l&#39;impostazione.

   * Per mostrare o nascondere più metriche, effettua le seguenti operazioni:

      1. Seleziona la casella di controllo accanto a ciascuna metrica di conversione.

         Per suggerimenti sulla selezione di più righe, vedere &quot;[Selezionare più righe](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

      1. Nella barra degli strumenti delle azioni in blocco, fai clic su ![Visibilità](/help/search-social-commerce/assets/visible.png "Visibilità") per visualizzare le metriche oppure su ![Visibilità disattivata](/help/search-social-commerce/assets/visibility-off.png "Visibilità disattivata") per nasconderle.

      1. (Per nascondere le metriche) Nel messaggio di conferma, fare clic su **[!UICONTROL Confirm]** per nascondere le metriche, inclusa la loro rimozione da qualsiasi metrica derivata che contiene le metriche.

## Gestire i rapporti sui dati delle prestazioni per le conversioni

Puoi scaricare le seguenti informazioni sulle conversioni tracciate: il nome della metrica sincronizzata, il nome visualizzato per la metrica nelle viste e nei rapporti di gestione di Ricerca, Social e Commerce, se la metrica è visibile nelle viste e nei rapporti di gestione, l’ID conversione e l’origine della metrica. Scaricare i dati in un file in formato cartella di lavoro [!DNL Microsoft Excel] (file XLSX).

### Generare un rapporto con le righe di dati filtrate

1. Nel menu principale, fare clic su **[!UICONTROL Goals]>[!UICONTROL Conversions]**.

1. Specifica le conversioni di cui desideri scaricare i dati:

   * Per scaricare i dati per righe specifiche, selezionare le caselle di controllo accanto alle righe.

   * Per scaricare i dati per tutte le righe, non è necessario selezionare alcuna casella di controllo. Tutte le righe sono incluse per impostazione predefinita.

1. Nella barra degli strumenti sopra la tabella dati, fare clic su ![Scarica report](/help/search-social-commerce/assets/download.png "Scarica report") **[!UICONTROL Reports]**.

1. Nelle impostazioni di [!UICONTROL Grid Reports], immettere un nome di report univoco, quindi fare clic su **[!UICONTROL Generate]**.

   Per impostazione predefinita, il file è denominato &quot;conversionsReport_YYYYMMDD_NNNN&quot;, dove &quot;NNNN&quot; è il numero del processo sequenziale (ad esempio &quot;conversionsReport_20260402_1326).

   Il file viene aggiunto all&#39;elenco [!UICONTROL Recently Generated].

1. (Facoltativo) Per scaricare il file una volta completato, fai clic su ![Scarica](/help/search-social-commerce/assets/download.png "Scarica") accanto al nome del file.

   Il file viene scaricato in base alla normale procedura del browser.

### Scaricare un rapporto completato

1. Nel menu principale, fare clic su **[!UICONTROL Goals]>[!UICONTROL Conversions]**.

1. Nella barra degli strumenti sopra la tabella dati, fare clic su ![Scarica report](/help/search-social-commerce/assets/download.png "Scarica report") **[!UICONTROL Reports]**.

1. Nell&#39;elenco [!UICONTROL Recently Generated] della finestra di dialogo [!UICONTROL Grid Reports], fare clic su ![Scarica](/help/search-social-commerce/assets/download.png "Scarica") accanto al nome del file.

   Il file viene scaricato in base alla normale procedura del browser.

### Eliminare un rapporto completato

1. Nel menu principale, fare clic su **[!UICONTROL Goals]>[!UICONTROL Conversions]**.

1. Nella barra degli strumenti sopra la tabella dati, fai clic su ![Scarica](/help/search-social-commerce/assets/download.png "Scarica") **[!UICONTROL Reports]**.

1. Nell&#39;elenco [!UICONTROL Recently Generated] della finestra di dialogo [!UICONTROL Grid Reports], fare clic su ![Elimina](/help/search-social-commerce/assets/delete-new.png "Elimina") accanto al nome del file.

<!--
>[!MORELIKETHIS]
>
>* 
-->
