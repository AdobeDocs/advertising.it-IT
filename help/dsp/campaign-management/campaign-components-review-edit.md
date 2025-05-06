---
title: Rivedere e modificare le impostazioni dei componenti di Campaign utilizzando i bulksheet
description: Scopri come rivedere e modificare in blocco le impostazioni del pacchetto chiave, del posizionamento e degli annunci utilizzando i fogli di calcolo.
feature: DSP Placements
exl-id: 1ec8362a-d37b-4fd7-becd-3a5b4f0c9504
source-git-commit: 7af6788f2aae3a2fb9e2048676dbe1955c2e56d9
workflow-type: tm+mt
source-wordcount: '533'
ht-degree: 0%

---

# Rivedere e modificare le impostazioni dei componenti di Campaign utilizzando i bulksheet

È possibile scaricare le impostazioni per pacchetti, posizionamenti e annunci in una singola campagna in formato XLSX ([!DNL Microsoft Excel] spreadsheet) per rivedere e modificare le impostazioni. Per impostazione predefinita, il file scaricato, denominato *bulksheet,* include schede separate per le impostazioni del pacchetto, le informazioni sul volo del pacchetto, le impostazioni di posizionamento e le pianificazioni degli annunci di posizionamento. Facoltativamente, puoi escludere le impostazioni per alcuni tipi di componenti della campagna.

Per aggiornare più impostazioni contemporaneamente, carica un file bulksheet valido con le modifiche. Per creare il bulksheet, modificare un bulksheet scaricato con le impostazioni esistenti. I campi modificabili includono la maggior parte delle impostazioni normalmente modificabili. I campi per le impostazioni non utilizzati contengono valori vuoti.

>[!NOTE]
>
>Puoi anche scaricare e modificare le impostazioni solo per pacchetti e posizionamenti specifici. Consulta &quot;[Rivedere e modificare le impostazioni dei pacchetti utilizzando i bulksheet](/help/dsp/campaign-management/packages/package-qa.md)&quot; e &quot;[Rivedere e modificare le impostazioni di posizionamento utilizzando i bulksheet](/help/dsp/campaign-management/placements/placement-qa.md).&quot;

## Scaricare le impostazioni per pacchetti, posizionamenti e annunci in una campagna {#download-bulksheet-campaign}

1. Nel menu principale, fare clic su **[!UICONTROL Campaigns]**.

1. Effettuare una delle seguenti operazioni:

   * Accanto alla campagna, fare clic su **[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**.

   * Fai clic sul nome della campagna. In alto a destra, fare clic su **[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**.

1. Nella finestra di dialogo [!UICONTROL Bulksheet Download] deselezionare i componenti di Campaign di cui si desidera escludere le impostazioni dal file scaricato e quindi fare clic su **[!UICONTROL Download]**.

Per impostazione predefinita, sono selezionate le impostazioni per tutti i componenti della campagna.

Un messaggio di notifica indica quando il file è disponibile per il download.

1. Per scaricare il file, effettuare una delle seguenti operazioni:

   * Nel messaggio di notifica, fare clic su **[!UICONTROL Download].**

   * Nella parte destra della barra dei menu superiore, fai clic su ![Processi](/help/dsp/assets/downloads.png). Fare clic su **[!UICONTROL Download]** accanto al processo.

     Il file è stato salvato nella cartella Download del browser.<!-- See "[Placement Columns in Downloaded/Uploaded Spreadsheets](#qa-sheet-columns)" for a list of the included columns. -->

     Per modificare le impostazioni, modifica direttamente il file e carica le modifiche. Tutte le colonne modificabili sono evidenziate in blu. Per utilizzare il formato corretto per un campo, selezionate e copiate il valore dall&#39;impostazione del pacchetto o del posizionamento pertinente. Per alcune impostazioni di destinazione, come la ripartizione giornaliera, gli obiettivi personalizzati e le metriche di conversione, è disponibile un’opzione di copia all’interno dell’impostazione.

## Caricare un bulksheet con le impostazioni per pacchetti, posizionamenti e annunci per una campagna{#upload-bulksheet-campaign-components}

Carica le impostazioni per pacchetti, posizionamenti e annunci in una singola campagna contemporaneamente in un bulksheet popolato.

1. Nel menu principale, fare clic su **[!UICONTROL Campaigns]**.

1. Effettuare una delle seguenti operazioni:

   * Accanto alla campagna, fare clic su **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**.

   * Fai clic sul nome della campagna. In alto a destra, fare clic su **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**.

1. Nella finestra di dialogo [!UICONTROL Upload Bulksheet]:

   1. Trascinare e rilasciare un file nella casella oppure fare clic all&#39;interno della casella per selezionare un file dal dispositivo o dalla rete.

   1. Fare clic su **[!UICONTROL Upload]**.

1. (Facoltativo) Per verificare che gli aggiornamenti siano stati elaborati, fai clic su ![Processi](/help/dsp/assets/downloads.png) a destra della barra dei menu superiore.

Quando un aggiornamento delle impostazioni non riesce, puoi scaricare un file di errore bulksheet con codifica a colori per mostrare quali impostazioni (righe) sono state salvate e quali non sono riuscite, con il motivo di ogni errore. Puoi quindi risolvere i problemi all’interno dello stesso file e caricarlo di nuovo per elaborare le informazioni corrette.


<!--
## Placement Setting Columns in Downloaded/Uploaded Spreadsheets{#qa-sheet-columns}

>[!TIP]
>
> In a downloaded spreadsheet, all editable columns are highlighted in blue.

### Campaign-level Spreadsheets

| Section | Column | Description | Editable? |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic] | [!UICONTROL Placement ID] | The numeric ID of the placement. | &mdash; |
| [!UICONTROL Basic] | [!UICONTROL Placement Name] | The name of the placement. | Yes |
| [!UICONTROL Basic] | [!UICONTROL Labels] | Any applied labels, for reporting. | &mdash; |
| [!UICONTROL Basic] | [!UICONTROL Edit Link] | A link to open the placement in Edit mode. | &mdash; |
| [!UICONTROL Basic] | [!UICONTROL Status] | The placement status: *[!UICONTROL active]* or *[!UICONTROL inactive]*. | Yes |
| [!UICONTROL Basic] | [!UICONTROL Placement Type] | The placement type. | &mdash; |
| [!UICONTROL Basic] | [!UICONTROL Package Name] | The name of the parent package, when applicable. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Start Date] | The start date of the placement. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL End Date] | The end date of the placement. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Day parting] | Whether dayparting is *[!UICONTROL ON]* or *[!UICONTROL OFF]*.<br><b>Note:</b> To check the actual dayparting schedule, open the placement settings in DSP. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Budget] | The placement budget, if there is one. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Budget Interval] | The budget interval: <i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*, or *[!UICONTROL All Time]*. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Optimization Goal] | The objective of the package. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Optimization Target] | The target value of the goal. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Pace on] | Whether the placement is pacing towards the *[!UICONTROL Budget]* or *[!UICONTROL Impressions]*. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Max Bid] | The maximum bid for the placement. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Flight Pacing] | The flight pacing strategy for the placement: *[!UICONTROL Even]*, *[!UICONTROL slightly ahead]*, *[!UICONTROL frontload]*, or *[!UICONTROL aggressive frontload]*. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Intraday Pacing] | The intraday pacing strategy for the placement: *[!UICONTROL Even]* or *[!UICONTROL ASAP]*. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Pre-Bid Filters] | Any pre-bid filter criteria to be applied. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Bidding Rules] | Whether bidding rules (deprecated) are *[!UICONTROL ON]* or *[!UICONTROL OFF]*. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap] | The primary frequency cap for the placement during the specified [!UICONTROL Frequency Cap Interval]. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap Interval] | The interval for the primary frequency cap: *[!UICONTROL Day]*, *[!UICONTROL Week]*, or *[!UICONTROL Month]*. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap] | The secondary frequency cap for the placement during the specified [!UICONTROL Secondary Frequency Cap Interval] | Yes |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval] | The type of interval for the secondary frequency cap: *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]*, or *[!UICONTROL Minute]*. The applicable number of weeks, days, hours, or minutes is indicated by the [!UICONTROL Secondary Frequency Cap Interval Value]. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval Value] | The number of weeks, days, hours, or minutes for which the [!UICONTROL Secondary Frequency Cap] applies. For example, if the secondary cap is three impressions per six hours, then the value here would be `6`. | Yes |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included #] | The number of targeted geographical locations, *[!UICONTROL All]*, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included] | The targeted geographical locations, separated by semi-colons,or *[!UICONTROL All Locations]*. | &mdash; |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded #] | The number of excluded geographical locations or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded] | The excluded geographical locations, separated by semi-colons,  or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Included #] | The number of targeted public inventory deals, if any are specified, *[!UICONTROL All]*, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Excluded #] | The number of excluded public inventory deals, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Included #] | The number of targeted private inventory deals, if any are specified, *[!UICONTROL All]*, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Excluded #] | The number of excluded private inventory deals, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Included #] | The number of targeted [!UICONTROL On-Demand Inventory] deals, if any are specified, *[!UICONTROL All]*, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Excluded #] | The number of excluded On-Demand Inventory deals, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Traffic Type] | The targeted type of traffic: *[!UICONTROL Website]* and/or *[!UICONTROL Apps]* | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Exclude out-stream] | Whether the Inventory Targeting option to exclude outstream traffic is <i[!UICONTROL >ON]* or *[!UICONTROL OFF]*.<br>Outstream ads usually appear over the content as a pop-up or stuffed into content (in the native experience), rather than as regular video ads in a video player. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Site Tier] | The quality of the sites to target: *[!UICONTROL Tier 1]*, *[!UICONTROL Tier 2]*, *[!UICONTROL Tier 3]*, or *[!UICONTROL All Sites]*. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Categories - Included #] | The number of targeted site categories, if any are specified, or *[!UICONTROL All]*. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Categories - Excluded #] | The number of excluded site categories, if any are specified, or *[!UICONTROL All]*. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Excluded Sites] | The excluded sites, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Language] | The targeted site languages. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Allow unscreened sites] | (Standard display placements only) Whether or not to allow ad delivery on non-audited sites: *[!UICONTROL ON]* or *[!UICONTROL OFF]*. When the placement targets private inventory, this option may deliver ads on blocked sites. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Targeted Sites] | The number of targeted sites, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Included] | The targeted audiences, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Excluded] | The excluded audiences, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Demographic booster] | Whether or not [!DNL Comscore] demographic segments are enabled for the placement (and other placements in the campaign): *[!UICONTROL ON]* or *[!UICONTROL OFF]*. This feature may be enabled only for campaigns for which the [!DNL Audience Verification] feature is enabled for [!DNL Nielsen] and/or [!DNL Comscore].  It incurs additional fees.  | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Extend across screens] | Whether or not to extend the ad targeting across devices: *[!UICONTROL ON]* or *[!UICONTROL OFF]*. Cross-device targeting extends your targeting across all of a person's known device, per the device graph specified in the campaign settings. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting] - Included # | The number of targeted topic codes, if any are specified, or *[!UICONTROL All]*.   | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting - Excluded #] | The number of excluded topic codes, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Included #] | The number of targeted device targets, if any are specified, or *[!UICONTROL All]*. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Excluded #] | The number of excluded device targets, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Included #] | The number of targeted ISP providers, if any are specified, or *[!UICONTROL All]/i>. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Excluded #] | The number of excluded ISP providers, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Contextual Filtering #] | The number of brand safety filters applied, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Fraud blocking #] | The number of pre-bid fraud blocking filters applied, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Viewability #] | The number of pre-bid viewability filters applied, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Brand Safety] | [!UICONTROL Site Safety Block] | Whether or not Site Safety Block is enabled: *[!UICONTROL ON]* or *[!UICONTROL OFF]*.[Whether or not the advertiser-level setting Enable Site Safety Block is enabled: *ON* or *OFF*.I don’t see this option at the placement level. Should there be one?] | &mdash; |
| [!UICONTROL Tracking] | [!UICONTROL Tracking Pixels #] | The number of third-party  event-tracking pixels attached to the placement, or *[!UICONTROL None]*.| &mdash; |
| [!UICONTROL Tracking] | [!UICONTROL Conversion Pixels #] | The number of conversion tracking pixels attached to the placement, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Tracking] | [!UICONTROL 3rd-party fees] | A static, third-party fee rate to be tracked as a non-billable cost per 1000 impressions, if applicable. | &mdash; |
| [!UICONTROL Ads] | [!UICONTROL # of Ads Attached] | The number of ads attached to the placement, if any are attached, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Ads] | [!UICONTROL Ad Names] | The names of any ads attached to the placement, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Ads] | [!UICONTROL Attached Ad ID] | The unique DSP-generated Ad IDs of any ads attached to the placement, separated by semi-colons. To download a list of ad names and associated Ad IDs from the [!UICONTROL Ads] view, create a custom view that includes the [!UICONTROL Ad ID] metric, and then [export the data](/help/dsp/campaign-management/reports/campaign-export-data.md). | Yes |
-->

>[!MORELIKETHIS]
>
>* [Verifica e modifica impostazioni pacchetto tramite bulksheet](/help/dsp/campaign-management/packages/package-qa.md)
>* [Impostazioni pacchetto](/help/dsp/campaign-management/packages/package-settings.md)
>* [Rivedi e modifica le impostazioni di posizionamento utilizzando i bulksheet](/help/dsp/campaign-management/placements/placement-qa.md)
>* [Impostazioni posizionamento](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Impostazioni annuncio audio](/help/dsp/campaign-management/ads/ad-settings-audio.md)
>* [Impostazioni TV collegate](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md)
>* [Impostazioni annuncio visualizzato](/help/dsp/campaign-management/ads/ad-settings-display.md)
>* [Impostazioni annuncio mobile](/help/dsp/campaign-management/ads/ad-settings-mobile.md)
>* [Impostazioni annuncio visualizzazione nativo](/help/dsp/campaign-management/ads/ad-settings-native.md)
>* [Impostazioni annuncio pre-roll](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)
>* [Impostazioni annuncio video universale](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)
