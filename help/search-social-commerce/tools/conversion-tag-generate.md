---
title: Genera un Adobe Advertising di tag di tracciamento delle conversioni
description: Scopri come creare un tag di conversione di Adobe Advertising per tenere traccia degli eventi di conversione.
exl-id: 617cd808-c4ba-4413-89e4-0f52cb44f44b
feature: Search Tools, Search Tracking
source-git-commit: 5141c332fc00e9eae62ef507d215dd435e86e8ba
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 0%

---

# Genera un Adobe Advertising di tag di tracciamento delle conversioni

*Solo per inserzionisti con tracciamento delle conversioni di Adobi Advertising*

Crea un tag di conversione separato per ogni set di metriche di cui desideri tenere traccia e fornisci all’inserzionista o all’agenzia un elenco di pagine web in cui inserirle.

>[!NOTE]
>
>Questa funzione non aggiunge tag immagine o [!DNL JavaScript] alle pagine Web dell&#39;inserzionista. I tag devono essere aggiunti in base alla normale procedura dell’inserzionista per l’aggiornamento delle pagine web.

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Tags]**.

1. Specifica la [impostazioni tag di conversione](#conversion-tag-settings).

1. Genera il tag:

   * Se il sito web utilizza HTTP, fai clic su **[!UICONTROL Generate Conversion Tag]**.

   * Se il sito web viene eseguito su un server protetto (HTTPS), fai clic su **[!UICONTROL Generate Secure Conversion Tag]**.

1. Copiare il tag dalla finestra di dialogo e incollarlo nelle pagine Web appropriate in base alle esigenze.

>[!NOTE]
>
>Ogni metrica nel nuovo tag di conversione viene elencata automaticamente in [!UICONTROL Admin] > [!UICONTROL Conversions], anche se non è implementato o se le pagine web in cui si trova non hanno ricevuto alcun clic. Questo comportamento è diverso da quello delle metriche nei tag creati manualmente o altrove, che non sono elencati in [!UICONTROL Admin] > [!UICONTROL Conversions] fino a quando una delle pagine web in cui si trova non ha ricevuto un clic. In tutti i casi, tuttavia, ogni metrica viene inizialmente esclusa dagli obiettivi del portfolio, dai rapporti e dalle visualizzazioni fino a quando non li rendi esplicitamente disponibili. Tuttavia, prima di aggiungere le metriche agli obiettivi del portfolio, considera innanzitutto di rendere le metriche disponibili e di aggiungerle ai rapporti per verificare quando ricevono i clic.

## Adobe Advertising di impostazioni dei tag di conversione {#conversion-tag-settings}

**[!UICONTROL Tag Type]:** Tipo di tag da creare:

* *[!UICONTROL Image]:* Creare un tag immagine per visualizzare un&#39;immagine trasparente (pixel) di 1 pixel x 1 pixel, invisibile agli utenti finali, sulla pagina Web. La best practice prevede l’utilizzo di tag immagine solo quando il sito dispone di criteri che impediscono l’utilizzo di tag JavaScript.

* *[!UICONTROL JavaScript]:* Per creare un tag JavaScript.

Per ulteriori informazioni sulle differenze tra i tipi di tag, vedi &quot;[Domande frequenti sulla conversione degli Adobi Advertising e sui tag di tracciamento della visualizzazione della pagina](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).&quot;

**[!UICONTROL Tag Properties]:** Una o più metriche di conversione da tracciare quando un utente finale visualizza una pagina contenente il tag di conversione. Per aggiungere una metrica all’elenco, inserisci il nome della metrica nella sezione &quot;[!UICONTROL Add new property]&quot; e fai clic su **[!UICONTROL Add]**.

Quando si tiene traccia di più metriche, queste vengono collegate da una e commerciale (`&`) nel tag, ad esempio `ev_Property1=<Property1>&ev_Property2=<Property2>`.

>[!NOTE]
>
>Le metriche aggiunte a questo elenco non vengono salvate da nessuna parte né integrate con quelle del client [!UICONTROL Conversions] elenco sul [!UICONTROL Admin] scheda. Tuttavia, le metriche vengono aggiunte al [!UICONTROL Conversions] elenca automaticamente una volta che Adobi Advertising raccoglie effettivamente i dati per una metrica, il che accade quando il tag di conversione viene implementato in una pagina e un utente finale completa una transazione che apre tale pagina.

**[!UICONTROL Include unique transaction IDs]:** (Facoltativo) Include una proprietà ID transazione (`ev_transid=<transid>`) nel tag. L’opzione è selezionata per impostazione predefinita.

Quando selezioni questa opzione, l’inserzionista deve generare un valore univoco per `<transid>` (ad esempio, un ID ordine effettivo) quando la transazione è completa e la ritrasferisce ad Adobi Advertising, ad esempio `ev_transid=0123`. Adobi Advertising utilizza l’ID transazione per eliminare le transazioni duplicate con lo stesso ID transazione e lo stesso valore della proprietà. L&#39;ID transazione non può contenere simboli di e commerciale (`&`), riservati come separatori di parametri. L’ID transazione è incluso in [il [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md), che puoi utilizzare per convalidare i dati in Search, Social e Commerce con i dati dell’inserzionista.

Se i dati non includono un ID univoco per transazione, Adobi Advertising ne genera comunque uno in base al tempo della transazione.

>[!NOTE]
>
>Se invii [feed ID transazione](/help/search-social-commerce/tracking/feed-transaction-id.md) con i dati di conversione per le conversioni offline, devi inviare l’ID transazione (`ev_transid`) per la parte online della transazione nei dati di feed per le parti offline della transazione.

**[!UICONTROL Page is inside FB app]:** Obsoleto

**[!UICONTROL Segment users]:** Obsoleto

**[!UICONTROL JS Version]:** ([!DNL JavaScript] solo tag) Quale versione del [!DNL JavaScript] tag da creare: *[!UICONTROL v2]* (impostazione predefinita) oppure *[!UICONTROL v3]*.

Consulta &quot;[Domande frequenti sulla conversione degli Adobi Advertising e sui tag di tracciamento della visualizzazione della pagina](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).&quot; per ulteriori informazioni sulle differenze.

>[!MORELIKETHIS]
>
>* [Informazioni sui tag di tracciamento delle conversioni di Adobe Advertising](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Informazioni sugli strumenti per creare e decodificare i tag di tracciamento](tracking-tools-about.md)
>* [Domande frequenti sui tag di conversione e di tracciamento della visualizzazione pagina](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [Formato dei tag di tracciamento della conversione JavaScript versione 3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [Formato dei tag di tracciamento della conversione JavaScript versione 2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)
>* [Formato dei tag di tracciamento conversione immagine](/help/search-social-commerce/tracking/format-conversion-tag-image.md)
>* [Adobe Advertising di tag di mappatura della conversione JavaScript](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)
>* [Informazioni sulla gestione delle metriche di conversione di un inserzionista](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
