---
title: Generare e implementare un tag di tracciamento delle conversioni di Adobe Advertising
description: Scopri come creare un tag di conversione Adobe Advertising per tenere traccia degli eventi di conversione.
exl-id: 02492162-96a0-4a91-8896-dd0f72199f79
feature: Search Tools, Search Tracking
source-git-commit: 1113c9f6ff8446d075dc9b90441f4119eb657598
workflow-type: tm+mt
source-wordcount: '1057'
ht-degree: 0%

---

# Generare e implementare un tag di tracciamento delle conversioni di Adobe Advertising

*Inserzionisti con solo monitoraggio delle conversioni di Adobe Advertising*

Crea un tag di conversione separato per ogni set di metriche di cui desideri tenere traccia. Puoi generare i tag in Search, Social e Commerce oppure utilizzando i tag in Adobe Experience Platform (precedentemente noto come Adobe Experience Platform Launch) con l’estensione Adobe Advertising.

<!--

## (New UI) Generate and implement a conversion-tracking tag within Search, Social, & Commerce

>[!NOTE]
>
>This feature doesn't add image tags or [!DNL JavaScript] tags to the advertiser's webpages. Provide the tags to the advertiser or agency with a list of webpages on which to insert each. The tags must be added according to the advertiser's normal procedure for updating webpages.

1. In the main menu, click **[!UICONTROL Goals] > [!UICONTROL Conversions]**.

1. In the main toolbar, click **[!UICONTROL Conversion Tag]**.

1. Specify the [conversion tag settings](#conversion-tag-settings).

1. Click **[!UICONTROL Generate]**.
   
1. Click **[!UICONTROL Copy]** to copy the tag to your clipboard. Give the tag to the advertiser or agency to implement.

>[!NOTE]
>
>Each metric in the new conversion tag is automatically listed in [!UICONTROL Admin] > [!UICONTROL Conversions], even if it isn't implemented or the webpages that it's on haven't received any clicks. This behavior is different from the behavior of metrics in tags created manually or elsewhere, which aren't listed in [!UICONTROL Admin] > [!UICONTROL Conversions] until one of the webpages that it's on has received a click. In all cases, however, each metric is initially excluded from portfolio objectives, reports, and views until you explicitly make them available. Before you add the metrics to portfolio objectives, consider first making the metrics available and adding them to reports to verify when they receive clicks.

### Adobe Advertising conversion tag settings {#conversion-tag-settings}

**[!UICONTROL Tag Type]:** The type of tag to create:

* *[!UICONTROL JavaScript]:* To create a JavaScript tag.

* *[!UICONTROL Image]:* To create an image tag to display a 1-pixel x 1-pixel transparent image (pixel), which is invisible to end users, on the webpage. The best practice is to use image tags only when the site has a policy against using JavaScript tags.

For more information about the differences between the tag types, see "[FAQs about Adobe Advertising conversion and page view tracking tags](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)."

**[!UICONTROL Include unique transaction IDs]:** (Optional) Includes a transaction ID property (`ev_transid=<transid>`) in the tag. The option is selected by default.

When you select this option, the advertiser must generate a unique value for `<transid>` (for example, an actual order ID) when the transaction is complete and pass it back to Adobe Advertising, such as `ev_transid=0123`. Adobe Advertising uses the transaction ID to eliminate duplicate transactions with the same transaction ID and property value. The transaction ID can't contain ampersand symbols (`&`), which are reserved as parameter separators. The transaction ID is included in [the [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md), which you can use to validate data within Search, Social, & Commerce with the advertiser's data.

If the data doesn't include a unique ID per transaction, then Adobe Advertising still generates one based on transaction time.

>[!NOTE]
>
>If you send [transaction ID feeds](/help/search-social-commerce/tracking/feed-transaction-id.md) with conversion data for offline conversions, then you must submit the transaction ID (`ev_transid`) for the online part of the transaction in the feed data for offline parts of the transaction.

**[!UICONTROL JS Version]:** ([!DNL JavaScript] tags only) Which version of the [!DNL JavaScript] tag to create: *[!UICONTROL v2]* (the default) or *[!UICONTROL v3]*.

**[!UICONTROL Security]:** The security protocol for your website create: *[!UICONTROL Standard]* (for websites that use HTTP) or *[!UICONTROL Secure]* (for websites that use HTTPs).

**[!UICONTROL Properties]:** One or more conversion metrics to be tracked when an end user views a page containing the conversion tag. To add a metric to the list, enter the metric name in the "[!UICONTROL Property name]" field and click **[!UICONTROL Add]**.

When multiple metrics are tracked, they're joined by an ampersand (`&`) in the tag, such as `ev_Property1=<Property1>&ev_Property2=<Property2>`.

>[!NOTE]
>
>Metrics added to this list aren't saved anywhere or integrated with the client's [!UICONTROL Conversions] list on the [!UICONTROL Admin] tab. However, metrics are added to the client's [!UICONTROL Conversions] list automatically once Adobe Advertising actually gathers data for a metric, which happens when the conversion tag is implemented on a page and an end user completes a transaction that opens that page.

-->
## &#x200B;<!-- (Legacy UI) --> Generare e implementare un tag di tracciamento delle conversioni in Search, Social e Commerce

>[!NOTE]
>
>Questa funzionalità non aggiunge tag immagine o tag [!DNL JavaScript] alle pagine Web dell&#39;inserzionista. Fornisci i tag all’inserzionista o all’agenzia con un elenco di pagine web in cui inserirle. I tag devono essere aggiunti in base alla normale procedura dell’inserzionista per l’aggiornamento delle pagine web.

1. Nel menu principale, fare clic su **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Conversion Tags]**.

1. Specificare le [impostazioni tag di conversione](#conversion-tag-settings).

1. Genera il tag:

   * Se il sito Web utilizza HTTP, fare clic su **[!UICONTROL Generate Conversion Tag]**.

   * Se il sito Web viene eseguito su un server protetto (HTTPS), fare clic su **[!UICONTROL Generate Secure Conversion Tag]**.

1. Copiare il tag dalla finestra di dialogo e incollarlo nelle pagine Web appropriate in base alle esigenze.

>[!NOTE]
>
>Ogni metrica nel nuovo tag di conversione viene elencata automaticamente in [!UICONTROL Admin] > [!UICONTROL Conversions], anche se non è implementata o se le pagine Web in cui si trova non hanno ricevuto clic. Questo comportamento è diverso da quello delle metriche nei tag creati manualmente o altrove, che non sono elencati in [!UICONTROL Admin] > [!UICONTROL Conversions] finché una delle pagine Web in cui si trova non ha ricevuto un clic. In tutti i casi, tuttavia, ogni metrica viene inizialmente esclusa dagli obiettivi del portfolio, dai rapporti e dalle visualizzazioni fino a quando non li rendi esplicitamente disponibili. Tuttavia, prima di aggiungere le metriche agli obiettivi del portfolio, considera innanzitutto di rendere le metriche disponibili e di aggiungerle ai rapporti per verificare quando ricevono i clic.

### Impostazioni dei tag di conversione Adobe Advertising {#conversion-tag-settings}

**[!UICONTROL Tag Type]:** Tipo di tag da creare:

* *[!UICONTROL Image]:* Per creare un tag immagine per visualizzare nella pagina Web un&#39;immagine trasparente (pixel) di 1 pixel x 1 pixel, invisibile agli utenti finali. La best practice prevede l’utilizzo di tag immagine solo quando il sito non prevede l’utilizzo di tag JavaScript.

* *[!UICONTROL JavaScript]:* Per creare un tag JavaScript.

Per ulteriori informazioni sulle differenze tra i tipi di tag, consulta &quot;[Domande frequenti sui tag di conversione Adobe Advertising e di tracciamento della visualizzazione della pagina](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).&quot;

**[!UICONTROL Tag Properties]:** Una o più metriche di conversione da monitorare quando un utente finale visualizza una pagina contenente il tag di conversione. Per aggiungere una metrica all&#39;elenco, immettere il nome della metrica nel campo &quot;[!UICONTROL Add new property]&quot; e fare clic su **[!UICONTROL Add]**.

Quando si tiene traccia di più metriche, queste vengono collegate da una e commerciale (`&`) nel tag, ad esempio `ev_Property1=<Property1>&ev_Property2=<Property2>`.

>[!NOTE]
>
>Le metriche aggiunte all&#39;elenco non vengono salvate in alcun punto o integrate con l&#39;elenco [!UICONTROL Conversions] del client nella scheda [!UICONTROL Admin]. Tuttavia, le metriche vengono aggiunte automaticamente all&#39;elenco [!UICONTROL Conversions] del client una volta che Adobe Advertising raccoglie effettivamente i dati per una metrica, il che si verifica quando il tag di conversione viene implementato in una pagina e un utente finale completa una transazione che apre tale pagina.

**[!UICONTROL Include unique transaction IDs]:** (facoltativo) include una proprietà ID transazione (`ev_transid=<transid>`) nel tag. L’opzione è selezionata per impostazione predefinita.

Quando si seleziona questa opzione, l&#39;inserzionista deve generare un valore univoco per `<transid>` (ad esempio, un ID ordine effettivo) al termine della transazione e restituirlo ad Adobe Advertising, ad esempio `ev_transid=0123`. Adobe Advertising utilizza l’ID transazione per eliminare le transazioni duplicate con lo stesso ID transazione e lo stesso valore della proprietà. L&#39;ID transazione non può contenere simboli di e commerciale (`&`), che sono riservati come separatori di parametri. L&#39;ID transazione è incluso in [[!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md), che è possibile utilizzare per convalidare i dati di Search, Social e Commerce con i dati dell&#39;inserzionista.

Se i dati non includono un ID univoco per transazione, Adobe Advertising ne genera comunque uno in base al tempo della transazione.

>[!NOTE]
>
>Se si inviano [feed ID transazione](/help/search-social-commerce/tracking/feed-transaction-id.md) con dati di conversione per conversioni offline, è necessario inviare l&#39;ID transazione (`ev_transid`) per la parte online della transazione nei dati di feed per le parti offline della transazione.

**[!UICONTROL Page is inside FB app]:** Obsoleto

**[!UICONTROL Segment users]:** Obsoleto

**[!UICONTROL JS Version]:** ([!DNL JavaScript] solo tag) Quale versione del tag [!DNL JavaScript] creare: *[!UICONTROL v2]* (impostazione predefinita) o *[!UICONTROL v3]*.

Consulta &quot;[Domande frequenti sui tag di conversione e tracciamento delle visualizzazioni di pagina di Adobe Advertising](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).&quot; per ulteriori informazioni sulle differenze.

## Implementare i tag di tracciamento delle conversioni utilizzando i tag di Adobe Experience Platform e l’estensione Adobe Advertising

Puoi impostare il tracciamento delle conversioni per Ricerca, Social e Commerce utilizzando i tag in Adobe Experience Platform. I tag sono disponibili per i clienti Adobe CX Enterprise come funzionalità inclusa a valore aggiunto.

Per configurare i tag di tracciamento della conversione per Search, Social e Commerce dall’interfaccia utente di Experience Platform o da quella di Experience Platform Data Collection, sono necessarie le seguenti attività. Per informazioni e istruzioni complete sulla configurazione dei tag, consulta la Guida ai tag di Experience Platform, a partire da &quot;[Panoramica sui tag](https://experienceleague.adobe.com/it/docs/experience-platform/tags/home)&quot; e &quot;[Guida rapida](https://experienceleague.adobe.com/it/docs/experience-platform/tags/get-started/quick-start)&quot;.

>[!PREREQUISITES]
>
>Per installare l&#39;estensione tag richiesta, chiedi all&#39;amministratore dell&#39;organizzazione di accedere alle funzioni di raccolta dati nell&#39;interfaccia utente, inclusa l&#39;autorizzazione `manage_properties`.

1. Dall&#39;[interfaccia utente di Data Collection](https://experience.adobe.com/#/data-collection/), installa l&#39;estensione [Adobe Advertising](https://experienceleague.adobe.com/it/docs/experience-platform/tags/ui/extensions/overview):

   1. Dalla proprietà applicabile, apri il catalogo delle estensioni e seleziona **Adobe Advertising**.

   1. Dal menu a discesa, selezionare **SSC** (per Ricerca, Social e Commerce).

   1. Nel campo **SSC UserID**, immetti l&#39;ID utente numerico per l&#39;account Search, Social e Commerce della tua organizzazione.

      Se non conosci il tuo ID utente, contatta il team del tuo account Adobe.

   1. Fai clic su **Salva**.

1. Crea una nuova regola (ad esempio, &quot;form_completes&quot;) per attivare il tag di conversione Ricerca, Social e Commerce:

   1. Nella sezione Configurazione evento:

      1. Selezionare i valori seguenti:

         **Estensione:** `Core`

         **Tipo evento:** `Library Loaded (Page Top)`

      1. Fai clic su **Mantieni modifiche**.

   1. Nella sezione Configurazione condizione:

      1. Specifica i seguenti valori:

         **Tipo di logica:** `Regular`

         **Estensione:** `Core`

         **Tipo di condizione:** `Path Without Query String`

         **Restituisce true se il percorso è uguale a:** Il percorso in cui deve essere tracciata la conversione (ad esempio, `/form_complete`).

      1. Fai clic su **Mantieni modifiche**.

   1. Nella sezione Configurazione azione:

      1. Specifica i seguenti valori:

         **Estensione:** `Adobe Advertising`

         **Tipo azione:** `AMO Measurement`

         **Nome proprietà di conversione:** Nome della proprietà di conversione, ad esempio `form_completes`.

         **Valore:** Il valore numerico della proprietà di conversione (ad esempio `1` per tenere traccia di form_completes) oppure scegliere un [elemento dati](https://experienceleague.adobe.com/it/docs/experience-platform/tags/ui/data-elements) esistente.

      1. Fai clic su **Mantieni modifiche**.

   1. Salva la regola.

1. Pubblica le modifiche.

>[!MORELIKETHIS]
>
>* [Informazioni sui tag di tracciamento delle conversioni di Adobe Advertising](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Informazioni sugli strumenti per creare e decodificare i tag di tracciamento](tracking-tools-about.md)
>* [Domande frequenti sui tag di conversione e di tracciamento della visualizzazione della pagina](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [Formato dei tag di tracciamento conversione di JavaScript versione 3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [Formato dei tag di tracciamento conversione di JavaScript versione 2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)
>* [Formato dei tag di tracciamento conversione immagine](/help/search-social-commerce/tracking/format-conversion-tag-image.md)
>* [Tag di mappatura conversione Adobe Advertising JavaScript](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)
>* [Informazioni sulla gestione delle metriche di conversione di un inserzionista](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
