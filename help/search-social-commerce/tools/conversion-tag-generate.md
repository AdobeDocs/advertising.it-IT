---
title: Genera un Adobe Advertising di tag di tracciamento delle conversioni
description: Scopri come creare un tag di conversione di Adobe Advertising per tenere traccia degli eventi di conversione.
exl-id: 02492162-96a0-4a91-8896-dd0f72199f79
feature: Search Tools, Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '674'
ht-degree: 0%

---

# Genera un Adobe Advertising di tag di tracciamento delle conversioni

*Inserzionisti con solo monitoraggio delle conversioni di Adobe Advertising*

Crea un tag di conversione separato per ogni set di metriche di cui desideri tenere traccia e fornisci all’inserzionista o all’agenzia un elenco di pagine web in cui inserirle.

>[!NOTE]
>
>Questa funzionalità non aggiunge tag immagine o tag [!DNL JavaScript] alle pagine Web dell&#39;inserzionista. I tag devono essere aggiunti in base alla normale procedura dell’inserzionista per l’aggiornamento delle pagine web.

1. Nel menu principale, fare clic su **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Tags]**.

1. Specificare le [impostazioni tag di conversione](#conversion-tag-settings).

1. Genera il tag:

   * Se il sito Web utilizza HTTP, fare clic su **[!UICONTROL Generate Conversion Tag]**.

   * Se il sito Web viene eseguito su un server protetto (HTTPS), fare clic su **[!UICONTROL Generate Secure Conversion Tag]**.

1. Copiare il tag dalla finestra di dialogo e incollarlo nelle pagine Web appropriate in base alle esigenze.

>[!NOTE]
>
>Ogni metrica nel nuovo tag di conversione viene elencata automaticamente in [!UICONTROL Admin] > [!UICONTROL Conversions], anche se non è implementata o se le pagine Web in cui si trova non hanno ricevuto clic. Questo comportamento è diverso da quello delle metriche nei tag creati manualmente o altrove, che non sono elencati in [!UICONTROL Admin] > [!UICONTROL Conversions] finché una delle pagine Web in cui si trova non ha ricevuto un clic. In tutti i casi, tuttavia, ogni metrica viene inizialmente esclusa dagli obiettivi del portfolio, dai rapporti e dalle visualizzazioni fino a quando non li rendi esplicitamente disponibili. Tuttavia, prima di aggiungere le metriche agli obiettivi del portfolio, considera innanzitutto di rendere le metriche disponibili e di aggiungerle ai rapporti per verificare quando ricevono i clic.

## Adobe Advertising di impostazioni dei tag di conversione {#conversion-tag-settings}

**[!UICONTROL Tag Type]:** Tipo di tag da creare:

* *[!UICONTROL Image]:* Per creare un tag immagine per visualizzare nella pagina Web un&#39;immagine trasparente (pixel) di 1 pixel x 1 pixel, invisibile agli utenti finali. La best practice prevede l’utilizzo di tag immagine solo quando il sito non prevede l’utilizzo di tag JavaScript.

* *[!UICONTROL JavaScript]:* Per creare un tag JavaScript.

Per ulteriori informazioni sulle differenze tra i tipi di tag, consulta &quot;[Domande frequenti sui tag di conversione di Adobe Advertising e di tracciamento della visualizzazione della pagina](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).&quot;

**[!UICONTROL Tag Properties]:** Una o più metriche di conversione da monitorare quando un utente finale visualizza una pagina contenente il tag di conversione. Per aggiungere una metrica all&#39;elenco, immettere il nome della metrica nel campo &quot;[!UICONTROL Add new property]&quot; e fare clic su **[!UICONTROL Add]**.

Quando si tiene traccia di più metriche, queste vengono collegate da una e commerciale (`&`) nel tag, ad esempio `ev_Property1=<Property1>&ev_Property2=<Property2>`.

>[!NOTE]
>
>Le metriche aggiunte all&#39;elenco non vengono salvate in alcun punto o integrate con l&#39;elenco [!UICONTROL Conversions] del client nella scheda [!UICONTROL Admin]. Tuttavia, le metriche vengono aggiunte automaticamente all&#39;elenco [!UICONTROL Conversions] del client una volta che Adobe Advertising raccoglie effettivamente i dati per una metrica, il che si verifica quando il tag di conversione viene implementato in una pagina e un utente finale completa una transazione che apre tale pagina.

**[!UICONTROL Include unique transaction IDs]:** (facoltativo) include una proprietà ID transazione (`ev_transid=<transid>`) nel tag. L’opzione è selezionata per impostazione predefinita.

Quando si seleziona questa opzione, l&#39;inserzionista deve generare un valore univoco per `<transid>` (ad esempio, un ID ordine effettivo) al termine della transazione e restituirlo all&#39;Adobe Advertising, ad esempio `ev_transid=0123`. Adobe Advertising utilizza l’ID transazione per eliminare le transazioni duplicate con lo stesso ID transazione e lo stesso valore della proprietà. L&#39;ID transazione non può contenere simboli di e commerciale (`&`), che sono riservati come separatori di parametri. L&#39;ID transazione è incluso in [[!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md), che è possibile utilizzare per convalidare i dati di Search, Social e Commerce con i dati dell&#39;inserzionista.

Se i dati non includono un ID univoco per transazione, Adobe Advertising ne genera comunque uno in base al tempo della transazione.

>[!NOTE]
>
>Se si inviano [feed ID transazione](/help/search-social-commerce/tracking/feed-transaction-id.md) con dati di conversione per conversioni offline, è necessario inviare l&#39;ID transazione (`ev_transid`) per la parte online della transazione nei dati di feed per le parti offline della transazione.

**[!UICONTROL Page is inside FB app]:** Obsoleto

**[!UICONTROL Segment users]:** Obsoleto

**[!UICONTROL JS Version]:** ([!DNL JavaScript] solo tag) Quale versione del tag [!DNL JavaScript] creare: *[!UICONTROL v2]* (impostazione predefinita) o *[!UICONTROL v3]*.

Consulta &quot;[Domande frequenti sulla conversione degli Adobi Advertising e sui tag di tracciamento della visualizzazione della pagina](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).&quot; per ulteriori informazioni sulle differenze.

>[!MORELIKETHIS]
>
>* [Informazioni su Adobi Advertising di tag per il tracciamento delle conversioni](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Informazioni sugli strumenti per creare e decodificare i tag di tracciamento](tracking-tools-about.md)
>* [Domande frequenti sui tag di conversione e di tracciamento della visualizzazione della pagina](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [Formato dei tag di tracciamento conversione di JavaScript versione 3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [Formato dei tag di tracciamento conversione di JavaScript versione 2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)
>* [Formato dei tag di tracciamento conversione immagine](/help/search-social-commerce/tracking/format-conversion-tag-image.md)
>* [Adobe Advertising tag di mappatura conversione JavaScript](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)
>* [Informazioni sulla gestione delle metriche di conversione di un inserzionista](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
