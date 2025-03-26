---
title: Rivedere e modificare le impostazioni dei pacchetti utilizzando i bulksheet
description: Scopri come rivedere e modificare le impostazioni dei pacchetti chiave in blocco utilizzando i fogli di calcolo.
feature: DSP Packages
exl-id: bf52de27-db48-40e2-bb55-a2c27a1924ad
source-git-commit: c482f476de5b79ee9a363791d62ba8c2ada12cbc
workflow-type: tm+mt
source-wordcount: '715'
ht-degree: 0%

---

# Rivedere e modificare le impostazioni dei pacchetti utilizzando i bulksheet

È possibile scaricare le impostazioni per uno o più pacchetti in formato XLSX ([!DNL Microsoft Excel] spreadsheet) per la revisione. Il file *bulksheet* include una scheda separata con le informazioni sul volo.

Per aggiornare più impostazioni contemporaneamente, è possibile effettuare una delle seguenti operazioni:

* Apporta le modifiche necessarie per selezionare i campi, salvare il file e caricare di nuovo il file del bulksheet modificato in DSP.

* Per apportare modifiche ad altri pacchetti, posizionamenti o annunci nella campagna, scarica un bulksheet per la campagna. Immetti o incolla le impostazioni aggiornate nel file, quindi carica il file per apportare le modifiche. Per istruzioni, consulta &quot;[Rivedere e modificare le impostazioni dei componenti di Campaign utilizzando i bulksheet](/help/dsp/campaign-management/campaign-components-review-edit.md).&quot;

I campi modificabili includono la maggior parte delle impostazioni normalmente modificabili.

>[!TIP]
>
>Per modificare rapidamente più campi per uno o più pacchetti, vedere &quot;[Modifica pacchetti](/help/dsp/campaign-management/packages/package-edit.md)&quot;.

## Scaricare le impostazioni per tutti i pacchetti in una campagna

Quando scarichi le impostazioni per tutti i pacchetti di una campagna, il bulksheet include schede separate per le impostazioni del pacchetto e per le informazioni sul volo. Facoltativamente, puoi includere le impostazioni per i posizionamenti e gli annunci associati ai pacchetti; vengono incluse schede aggiuntive per le impostazioni di posizionamento e annunci.

1. Nel menu principale, fare clic su **[!UICONTROL Campaigns]**.

1. Effettuare una delle seguenti operazioni:

   * Accanto alla campagna, fare clic su **[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**.

   * Fai clic sul nome della campagna. In alto a destra, fare clic su **[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**.

1. Nella finestra di dialogo [!UICONTROL Bulksheet Download] deselezionare i componenti di Campaign di cui si desidera escludere le impostazioni dal file scaricato e quindi fare clic su **[!UICONTROL Download]**.

Per impostazione predefinita, sono selezionate le impostazioni per tutti i posizionamenti e gli annunci associati ai pacchetti.

Un messaggio di notifica indica quando il file è disponibile per il download.

1. Per scaricare il file, effettuare una delle seguenti operazioni:

   * Nel messaggio di notifica, fare clic su **[!UICONTROL Download].**

   * Nella parte destra della barra dei menu superiore, fai clic su ![Processi](/help/dsp/assets/downloads.png). Fare clic su **[!UICONTROL Download]** accanto al processo.

     Il file è stato salvato nella cartella Download del browser.<!-- See "[Placement Columns in Downloaded/Uploaded Spreadsheets](#qa-sheet-columns)" for a list of the included columns. -->

     Per modificare le impostazioni, modifica direttamente il file e carica le modifiche. Tutte le colonne modificabili sono evidenziate in blu.

## Impostazioni di download per pacchetti specifici

Quando si scaricano le impostazioni per pacchetti specifici, il file del bulksheet include schede separate per le impostazioni del pacchetto e per le informazioni sul volo e il file è modificabile.

1. Nel menu principale, fare clic su **[!UICONTROL Campaigns]**.

1. Fai clic sul nome della campagna.

1. Nel sottomenu fare clic su **[!UICONTROL Packages]**.

1. Selezionare le caselle di controllo relative ai pacchetti di cui si desidera scaricare le impostazioni.

1. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**.

   Un messaggio di notifica indica quando il file bulksheet è disponibile per il download.

1. Per scaricare il bulksheet, effettuare una delle seguenti operazioni:

   * Nel messaggio di notifica, fare clic su **[!UICONTROL Download].**

   * Nella parte destra della barra dei menu superiore, fai clic su ![Processi](/help/dsp/assets/downloads.png). Fare clic su **[!UICONTROL Download]** accanto al processo.

     Il file viene salvato nella cartella Download del browser. Per un elenco delle colonne incluse, consulta &quot;[Colonne di posizionamento nei bulksheet scaricati/caricati](#qa-sheet-columns)&quot;.

     Per modificare le impostazioni, modifica direttamente il file e carica le modifiche. Tutte le colonne modificabili sono evidenziate in blu. Per utilizzare il formato corretto per un campo, selezionate e copiate il valore dall&#39;impostazione del pacchetto o del posizionamento pertinente. Per alcune impostazioni di destinazione, come la ripartizione giornaliera, gli obiettivi personalizzati e le metriche di conversione, è disponibile un’opzione di copia all’interno dell’impostazione.

## Caricare un bulksheet con le impostazioni del pacchetto {#upload-bulksheet-package}

Puoi caricare le impostazioni dei pacchetti, inclusi i posizionamenti e gli annunci associati ai pacchetti, in un file bulksheet.

1. Nel menu principale, fare clic su **[!UICONTROL Campaigns]**.

1. Effettua una delle seguenti operazioni:

   * Accanto alla campagna principale, fare clic su **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**.

   * Fai clic sul nome della campagna. In alto a destra, fare clic su **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**.

     Questa opzione è disponibile nella scheda [!UICONTROL Packages], [!UICONTROL Placements] o [!UICONTROL Ads].

   * Nel sottomenu, fare clic su **[!UICONTROL Packages]** e selezionare la casella di controllo per qualsiasi pacchetto. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**.

1. Nella finestra di dialogo [!UICONTROL Upload Bulksheet]:

   1. Trascinare e rilasciare un file nella casella oppure fare clic all&#39;interno della casella per selezionare un file dal dispositivo o dalla rete.

   1. Fare clic su **[!UICONTROL Upload]**.

1. (Facoltativo) Per verificare che gli aggiornamenti siano stati elaborati, fai clic su ![Processi](/help/dsp/assets/downloads.png) a destra della barra dei menu superiore.

Quando un aggiornamento delle impostazioni non riesce, puoi scaricare un file di errore bulksheet con codifica a colori per mostrare quali impostazioni (righe) sono state salvate e quali non sono riuscite, con il motivo di ogni errore. Puoi quindi risolvere i problemi all’interno dello stesso file e caricarlo di nuovo per elaborare le informazioni corrette.

<!--
## Package Setting Columns in Downloaded/Uploaded Bulksheets{#qa-sheet-columns-packages}

>[!TIP]
>
> In a downloaded bulksheet file, all editable columns are highlighted in blue.

### [!UICONTROL Package] Tab

| Section | Column | Description | Editable? |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic details] | [!UICONTROL Package ID] | The numeric ID of the package. | &mdash; |
| [!UICONTROL Basic details] | [!UICONTROL Package Name] | The name of the package. | Yes |
| [!UICONTROL Basic details] | [!UICONTROL Status] | The package status: *[!UICONTROL active]* or *[!UICONTROL inactive]*. | Yes |
| [!UICONTROL Basic details] | [!UICONTROL Description] | An optional description of the package. | Yes |
| [!UICONTROL Basic details] | [!UICONTROL 3rd-party fees - CPM] | A static, third-party fee rate to be tracked as a non-billable cost per 1000 impressions, if applicable. | Yes |
| [!UICONTROL Basic details] | [!UICONTROL 3rd-party fees - description] | An optional description of the third-party fee rate, if applicable. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package Start Date] | The start date of the package. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package End Date] | The end date of the package. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Pacing Level] | At which level to pace and cap placements in the package: *[!UICONTROL Package]* or *[!UICONTROL Placement]*. | &mdash; |
| [!UICONTROL Goals & Budget] | [!UICONTROL Budget] | The package budget. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Budget Interval] | The budget interval: <i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*, or *[!UICONTROL All Time]*. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Interval Cap] | An optional budget interval cap. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Interval Cap Period] | The interval for the optional budget interval cap: <i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*, or *[!UICONTROL All Time]*. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Optimization Goal] | The objective of the package. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Optimization Target] | The target value of the goal. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Custom Goal Name] | (Packages with the "[!UICONTROL Highest Return on Ad Spend]" and "[!UICONTROL Lowest Cost per Acquisition]" optimization goals only)A [custom goal](/help/dsp/optimization/custom-goal.md) that includes the revenue or conversion events used to calculate the CPA or ROAS metric. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Conversion Metric Name] | (Optional; packages with the "[!UICONTROL Highest Return on Ad Spend]" and "[!UICONTROL Lowest Cost per Acquisition]" optimization goals only) The final conversion event or revenue event/sale amount to use for computing the return on ad spend or the cost per acquisition. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package Goal Type] | (Packages with custom optimization goals only) The purpose of the package, which helps determine how to optimize the package: *[!UICONTROL Prospecting]*, *[!UICONTROL Retargeting]*, or *[!UICONTROL Other]* . | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Linked Package id for learning carryover] | (Packages with custom optimization goals only) The package ID for another package whose historic data is used as input for optimizing the package. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Linked Package Name for learning carryover] | (Packages with custom optimization goals only) Another package whose historic data is used as input for optimizing the package. | &mdash; |
| [!UICONTROL Goals & Budget] | [!UICONTROL Pace on] | Whether the package is pacing towards the *[!UICONTROL budget]* or *[!UICONTROL primary_goal]* (for impressions). | &mdash; |
| [!UICONTROL Goals & Budget] | [!UICONTROL Primary Goal Amount] | (When you pace the package on impressions) The target number of impressions during the specified time interval. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Primary Goal Interval] | (When you pace the package on impressions) The time interval for the target number of impressions. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Flight Pacing] | The flight pacing strategy for the package: *[!UICONTROL Even]*, *[!UICONTROL slightly ahead]*, *[!UICONTROL frontload]*, or *[!UICONTROL aggressive frontload]*. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Intraday Pacing] | The intraday pacing strategy for the package: *[!UICONTROL Even]* or *[!UICONTROL ASAP]*. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap] | The primary frequency cap for the package during the specified [!UICONTROL Frequency Cap Interval]. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap Interval] | The interval for the primary frequency cap: *[!UICONTROL Day]*, *[!UICONTROL Week]*, or *[!UICONTROL Month]*. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap Interval Value] | The number of weeks, days, hours, or minutes for which the primary [!UICONTROL Frequency Cap] applies. For example, if the primary cap is 12 impressions per month, then the value here would be `12`. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap] | The secondary frequency cap for the package during the specified [!UICONTROL Secondary Frequency Cap Interval] | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap Interval] | The type of interval for the secondary frequency cap: *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]*, or *[!UICONTROL Minute]*. The applicable number of weeks, days, hours, or minutes is indicated by the [!UICONTROL Secondary Frequency Cap Interval Value]. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap Interval Value] | The number of weeks, days, hours, or minutes for which the [!UICONTROL Secondary Frequency Cap] applies. For example, if the secondary cap is three impressions per six hours, then the value here would be `6`. | Yes |
| [!UICONTROL Custom Flights] | [!UICONTROL Activate Custom Flights] | Whether or not to create non-even pacing flights for the package*T* (true) or *F* (false). Once you enable custom flighting and save the package, you can't disable custom flighting nor edit the package start date. | &mdash; |
| [!UICONTROL Custom Flights] | [!UICONTROL Automatic Budget Rollover] | (Available only when the [!UICONTROL Activate Custom Flighting] option is enabled) Whether or not to automatically add any remaining budget from the previous flight to the existing budget for the next flight: *T* (true) or *F* (false). | Yes |
| [!UICONTROL Error] | [!UICONTROL Error] | Any relevant errors. | &mdash; |

### [!UICONTROL Package_Flights] Tab {#qa-sheet-columns-package-flights}

| Section | Column | Description | Editable? |
|---------|--------|-------------|-----------|
| [!UICONTROL Flight Details] | [!UICONTROL Package ID] | The numeric ID of the package. | &mdash; |
| [!UICONTROL Flight details] | [!UICONTROL Flight ID] | The numeric ID of the flight. | &mdash; |
| [!UICONTROL Flight details] | [!UICONTROL Flight Start Date] |The first date of the flight. | Yes |
| [!UICONTROL Flight details] | [!UICONTROL Flight End Date] | The final date of the flight. | Yes |
| [!UICONTROL Flight details] | [!UICONTROL Flight Budget] | The target spend goal for the flight. | Yes |
| [!UICONTROL Flight details] | [!UICONTROL Rollover] | (Existing packages without the "[!UICONTROL Automatically rollover remaining flight budget to next flight]" option enabled) An amount of potentially unspent budget to add to the next flight. | Yes |
-->

>[!MORELIKETHIS]
>
>* [Verifica e modifica le impostazioni dei componenti della campagna tramite bulksheet](/help/dsp/campaign-management/campaign-components-review-edit.md)
>* [Modifica pacchetti](/help/dsp/campaign-management/packages/package-edit.md)
>* [Impostazioni pacchetto](/help/dsp/campaign-management/packages/package-settings.md)
