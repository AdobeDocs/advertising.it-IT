---
title: Gestire i rapporti personalizzati
description: Scopri come generare e gestire la cross-experience [!UICONTROL Custom Creative Report].
feature: Creative Reporting
source-git-commit: 455a63be51ca56610cc15ba498e69eeae52ffdba
workflow-type: tm+mt
source-wordcount: '1477'
ht-degree: 0%

---

# [!UICONTROL Manage custom reports]

Puoi creare, duplicare, modificare, eseguire, scaricare ed eliminare rapporti personalizzati.

## Creare un rapporto personalizzato {#report-create}

1. Nel menu principale, fare clic su **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**.

1. In alto a destra, fare clic su **[!UICONTROL Create]**.

1. Specifica le [impostazioni report](#report-settings).

1. Fare clic su **[!UICONTROL Create Custom Report]**.

## Duplicare un rapporto personalizzato

Duplica un rapporto personalizzato per creare un nuovo rapporto con impostazioni simili.

1. Nel menu principale, fare clic su **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**.

1. Accanto al nome del report, fare clic su **[!UICONTROL ...]** > **[!UICONTROL Copy]**.

1. (Facoltativo) Modifica le [impostazioni del report](#report-settings.md) in base alle esigenze.

   Il nome del report, per impostazione predefinita, è &quot;\&lt;*nome report esistente*\> \#2&quot; (o il numero successivo nella sequenza).

## Modificare un rapporto personalizzato {#report-edit}

1. Nel menu principale, fare clic su **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**.

1. Accanto al nome del report, fare clic su **[!UICONTROL ...]** > **[!UICONTROL Edit]**.

1. Modifica le [impostazioni report](#report-settings.md).

1. Fare clic su **[!UICONTROL Edit Custom Report]**.

## Eseguire un rapporto personalizzato &lbrace;report-run-now&rbrace;

Puoi eseguire qualsiasi rapporto che non è scaduto e al momento non è in esecuzione.

>[!NOTE]
>
>Puoi anche eseguire un report personalizzato quando lo [crei](#report-create) o lo [modifichi](#report-edit).

1. Nel menu principale, fare clic su **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**.

1. Accanto al nome del report, fare clic su **[!UICONTROL ...]** > **[!UICONTROL Run Now]**.

   Una volta completato, il rapporto viene inviato alle destinazioni specificate nelle impostazioni del rapporto.

## Scaricare un rapporto personalizzato

È possibile scaricare qualsiasi istanza di report completata negli ultimi quattro mesi, con stato &quot;[!UICONTROL Ready to Download]&quot; o &quot;[!UICONTROL Completed]&quot;.

1. Nel menu principale, fare clic su **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**.

1. Nella colonna [!UICONTROL Download Report] per la riga del report, eseguire le operazioni seguenti:

   * Per scaricare l&#39;istanza più recente del report, fare clic su **[!UICONTROL Download]**.

   * (Report con più istanze) Fare clic su ![freccia GIÙ](/help/dsp/assets/chevron-down.png "freccia GIÙ") accanto a [!UICONTROL Download], quindi fare clic sulla data di completamento del report che si desidera scaricare. Le istanze di report scaricabili sono indicate da un&#39;icona di download (![icona di download](/help/dsp/assets/indicator-downloadable.png "icona di download")).

     Se sono disponibili più istanze, fare clic su **[!UICONTROL Load More]** in fondo all&#39;elenco, se necessario.

     Quando un rapporto viene eseguito più volte nello stesso giorno, le istanze del rapporto per quel giorno sono elencate in ordine cronologico, con l’istanza più recente in alto.

     I processi di report non riusciti sono indicati da un&#39;icona di errore (![indicatore di errore](/help/dsp/assets/indicator-critical.png "indicatore di errore")) e non possono essere scaricati. Per una descrizione dell’errore, posiziona il cursore sull’icona.

## Eliminare un rapporto personalizzato

1. Nel menu principale, fare clic su **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**.

1. Accanto al nome del report, fare clic su **[!UICONTROL ...]** > **[!UICONTROL Delete]**.

1. Nel messaggio di conferma, fare clic su **[!UICONTROL Delete]**.

## Impostazioni dei rapporti {#report-settings}

**[!UICONTROL Name]:** Il nome del report. La lunghezza massima è di 180 caratteri.

**[!UICONTROL Report Type]:** Il tipo di report.

### Sezione [!UICONTROL Report Range]

Questa sezione determina i dati inclusi nel rapporto. Per impostare le date per la pianificazione del report, vedere la sezione &quot;[!UICONTROL Report run schedule]&quot;.

**[!UICONTROL Timezone]:** Il fuso orario per il reporting.

**[!UICONTROL Observe Daylight Savings Time]:** considera l&#39;ora legale negli orari segnalati.

**Intervallo:** l&#39;intervallo di date per il quale generare i dati. Il numero di giorni disponibili varia in base al rapporto e alle dimensioni selezionate. Sceglietene uno:

* **[!UICONTROL Previous Calendar Week]:** include i dati per la settimana di calendario precedente.

* **[!UICONTROL Previous Calendar Month]:** include i dati per il mese di calendario precedente.

* **[!UICONTROL Custom Range]:** include dati tra date di inizio e fine specifiche. Per segnalare i dati relativi al giorno precedente, selezionare **[!UICONTROL Present]**.

### Sezione [!UICONTROL Report Run schedule]

Questa sezione determina le date di esecuzione del rapporto. Per impostare le date per le quali includere i dati del report, vedere la sezione &quot;[!UICONTROL Report range]&quot;.

**\[Schedule\]:** Quando generare il report:

* *[!UICONTROL Immediately]*: aggiunge immediatamente il report alla coda dei report.

  >[!NOTE]
  >
  >È inoltre possibile [eseguire un report personalizzato in qualsiasi momento](#report-run-now) dalla visualizzazione [!UICONTROL Reports].

* *[!UICONTROL On]\&lt;Data\>:* Esegue il report in una data specificata per il completamento da parte di 09:00 nel fuso orario dell&#39;account.

* *[!UICONTROL Recurring]:* Esegue il report in base a una pianificazione durante un periodo di tempo specificato.

   * **\[Pianificazione\]:** Frequenza di esecuzione del report:

      * *Giornaliero* per eseguire il report ogni N giorni. Ad esempio, per eseguire il report ogni due settimane (14 giorni), selezionare questa opzione e immettere **14**.

      * *Settimanale* per eseguire il report nei giorni della settimana specificati. Ad esempio, per eseguire il report ogni lunedì e venerdì, selezionare questa opzione e selezionare le caselle di controllo accanto a **lunedì** e **venerdì**.

      * *Mensile* per eseguire il report in un giorno numerico specifico del mese, da 1 a 30. Ad esempio, eseguire il report il primo giorno di ogni mese, selezionare questa opzione e immettere **1**.

   * **Da**: prima data in cui è possibile eseguire il report. A seconda della pianificazione specificata, la prima istanza di report può essere successiva a tale data.

   * **Fino a**: la data di scadenza del report, che può essere un massimo di quattro mesi di calendario. Prima della scadenza di un rapporto, tutte le destinazioni e-mail specificate ricevono un avviso e-mail sette giorni e un giorno prima della data di scadenza. Per mantenere il report più a lungo, modifica questa data.

### Sezione [!UICONTROL Apply Filters]

**[!UICONTROL Filter by]:** (facoltativo) dimensioni aggiuntive in base alle quali filtrare i dati, indipendentemente dal fatto che le dimensioni siano incluse o meno come colonne nel report. I filtri disponibili variano in base al tipo di report e possono includere: *[!UICONTROL Advertiser]*, *[!UICONTROL Experience]*, *[!UICONTROL Creative Library]* e *[!UICONTROL DSP]*<!-- Clarify what this is for, Advertising DSP or whatever DSP the ads were run from? -->.

Per applicare uno o più filtri, effettuare le seguenti operazioni:

* Selezionare una dimensione, selezionare l&#39;operatore (*uguale a* o *diverso da*), quindi selezionare il valore applicabile. Ad esempio, per restituire dati solo per gli annunci preroll, specificare &quot;[!UICONTROL Ad Type equals Preroll]&quot;.
* (Facoltativo) Aggiungi criteri aggiuntivi al filtro.
* (Facoltativo) Aggiungi altri filtri, ciascuno con uno o più criteri.

### Sezione [!UICONTROL Build Your Report]

**[!UICONTROL Select To Add As Report Headers]:** le colonne di dati, o intestazioni, da includere nel report. Per aggiungere una colonna, espandere la categoria e selezionare la casella di controllo accanto al nome della colonna. Le colonne disponibili variano in base al report e tutte le metriche non disponibili sono disabilitate.<!-- Add back once I have this completed, and reconsider wording of link/anchor:  See "[Available Report Columns](#report-custom-creative-columns)" for descriptions of all options. -->

**[!UICONTROL Drag to Re-Order Report Headers Below]:** Ordine delle intestazioni di colonna. Puoi trascinare e rilasciare qualsiasi colonna per personalizzare l’ordine.

**[!UICONTROL Format]:** se generare un report in formato *[!UICONTROL CSV]* (valori separati da virgola) o *[!UICONTROL Tab]* (valori separati da tabulazione).

**[!UICONTROL Headers]:** se *[!UICONTROL Include]* o *[!UICONTROL Do Not Include]* intestazioni di colonna.

### Sezione [!UICONTROL Multi-Touch Conversion Options]

**[!UICONTROL Attribution Rule Settings]:** Le impostazioni variano in base al tipo di report:

* **\[Tipo regola\]:** (Solo per inserzionisti con tracciamento delle conversioni di Adobe Advertising) All&#39;interno del rapporto, come attribuire dati di conversione in una serie di eventi che portano a una conversione. Puoi scegliere più di una regola se desideri confrontare le differenze tra le regole.

  >[!NOTE]
  >
  >I percorsi di conversione includono eventuali impression e clic all&#39;interno degli intervalli di impression o di lookback dei clic dell&#39;inserzionista, configurati in [!DNL Advertising Search, Social, & Commerce]. Ai clic viene data la preferenza alle impression durante l’attribuzione della conversione. Tutti i clic in un percorso di conversione ricevono il pieno credito in base alla regola di attribuzione. Il merito delle impression viene attribuito solo quando nel percorso di conversione non viene tracciato alcun clic.

   * *[!UICONTROL Last Event]:* attribuisce le conversioni all&#39;ultimo clic o all&#39;ultima impression nel percorso di conversione.

   * *[!UICONTROL Weight Last More]:* attribuisce le conversioni a tutti gli eventi nel percorso di conversione, ma attribuisce il peso maggiore all&#39;ultimo evento e successivamente meno peso agli eventi precedenti.

   * *[!UICONTROL Even Distribution]:* attribuisce le conversioni in modo uguale a ogni evento nel percorso di conversione.

   * *[!UICONTROL Weight First More]:* attribuisce le conversioni a tutti gli eventi nel percorso di conversione, ma attribuisce il peso maggiore al primo evento e successivamente meno peso ai seguenti eventi.

   * *[!UICONTROL First Event]:* attribuisce le conversioni al primo clic o all&#39;impression nel percorso di conversione.

   * *[!UICONTROL U-shaped]:* attribuisce la conversione a tutti gli eventi nel percorso di conversione, ma attribuisce il maggior peso al primo e all&#39;ultimo evento, con un peso progressivamente inferiore agli eventi nel mezzo del percorso di conversione.

   * *[!UICONTROL Display Only]:* attribuisce le conversioni all&#39;ultimo clic o impression di DSP nel percorso di conversione. Ciò include video e annunci TV connessi ed esclude i clic sugli annunci [!DNL Advertising Search, Social, & Commerce].

   * *[!UICONTROL Social Only]:* Obsoleto

Vedere anche &quot;[Modalità di calcolo delle regole di attribuzione per Adobe Advertising](/help/search-social-commerce/reports/attribution-rules.md).&quot;

**[!UICONTROL Paths as Columns]:** quali tipi di conversioni segnalare quando si sono verificati eventi precedenti sullo stesso dispositivo. Puoi includere fino a tre tipi. Per ogni tipo selezionato, viene inclusa una colonna separata per ogni metrica di conversione e viene aggiunto il suffisso specificato ([!UICONTROL (tl)], [!UICONTROL (ct)] o [!UICONTROL (vt)]):

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]:* include conversioni attribuite ai clic (TC per click-through) e alle impression (VT per view-through). Le conversioni attribuite alle impression vengono moltiplicate per il peso view-through specificato. Il peso view-through predefinito è 100%, il che significa che le conversioni attribuite alle impression vengono conteggiate come il 100% del valore delle conversioni attribuite ai clic.

* *[!UICONTROL With Clicks (CT)]:* Include solo le conversioni attribuite ai clic.

* *[!UICONTROL Impressions Only (VT)]:* include solo le conversioni attribuite alle impression perché nel percorso di conversione non è stato tracciato alcun clic.

### Sezione [!UICONTROL Add Report Destinations]

**[!UICONTROL Destination Type]:** Dove recapitare i report completati e le notifiche di errore. Una volta salvato il rapporto, non puoi modificare il tipo di destinazione.

>[!NOTE]
>
>È sempre possibile scaricare i report completati dalla visualizzazione [!UICONTROL Reports] > [!UICONTROL Custom Reports].

* *[!UICONTROL None]:* Per non inviare report o notifiche.

* *[!UICONTROL S3]:* Per inviare il report completato a una o più posizioni [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3]), che è necessario selezionare nel campo **[!UICONTROL Destination Name]**.

* *[!UICONTROL sFTP]:* Per inviare il report completato a una o più posizioni SFTP, che è necessario selezionare nel campo **[!UICONTROL Destination Name]**.

* *[!UICONTROL FTP]:* Per inviare il report completato a uno o più percorsi FTP, che è necessario selezionare nel campo **[!UICONTROL Destination Name]**.

* *[!UICONTROL FTP SSL] (attualmente in Beta):* Per inviare il report completato a uno o più percorsi SSL FTP, che è necessario selezionare nel campo **[!UICONTROL Destination Name]**.

* *[!UICONTROL Email]:* Specificare gli indirizzi e-mail a cui inviare i report completati o le notifiche se il report viene annullato a causa di errori.

**[!UICONTROL Email]:** (solo tipo di destinazione e-mail) Per ogni indirizzo, immettere l&#39;indirizzo e fare clic su **+**.

**[!UICONTROL Destination Name]:** (solo tipi di destinazione S3, FTP, sFTP e FTP SSL) i nomi delle [destinazioni del report](/help/dsp/reports/report-destinations/report-destination-about.md){target="_blank"} alle quali viene inviato il report personalizzato.

* Per specificare una destinazione esistente, selezionare un nome di destinazione dall&#39;elenco. Puoi selezionare separatamente più nomi di destinazione.

* Per creare una nuova destinazione:

   1. Fare clic su **Aggiungi nuova destinazione**.

   1. Immetti le [impostazioni di destinazione del report](/help/dsp/reports/report-destinations/report-destination-settings.md){target="_blank"} e fai clic su **Salva**.

   1. Nelle impostazioni del report, fare clic su **Aggiorna nomi di destinazione.**

      La nuova destinazione è ora disponibile dall’elenco delle destinazioni esistenti e, facoltativamente, può essere aggiunta al rapporto.


<!-- This needs a lot of updating for new report:

## Available Report Columns {#report-custom-creative-columns}

|Metric Type|Subtype|Column Name|Description|
|-----------|-------|-----------|-----------|
|\[Dimension\]|[!UICONTROL Ad]|[!UICONTROL Ad Size]|The dimensions of the published ad.|
|\[Dimension\]|[!UICONTROL Ad]|[!UICONTROL Is Default]|Whether the served ad was a default image ad or video ad for the experience.|
|\[Dimension\]|[!UICONTROL Ad]|[!UICONTROL Rotation Type]| Whether ads were rotated algorithmically (*Algorithmic*), in a specified sequence (*Sequenced*), or according to relative weights (*Weighted*).|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Creative ID]| The ID that [!UICONTROL Creative] assigned to the creative.|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Creative Name]| The name of the creative.|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Creative Type]| The type of creative (such as [!UICONTROL HTML5]).|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Parent Creative ID]| The ID that [!UICONTROL Creative] assigned to the parent creative.|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Parent Creative Name]| The name of the parent creative.|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Parent Creative Type]| The type of parent creative (such as [!UICONTROL HTML5]).|
|\[Dimension\]|[!UICONTROL Click Events]|[!UICONTROL Ad Link]| The landing page URL.|
|\[Dimension\]|[!UICONTROL Click Events]|[!UICONTROL Click Type]| The specific type of user interaction.|
|\[Dimension\]|[!UICONTROL Click Events]|[!UICONTROL Direction]| The directional flow or navigation path of the user's click interaction within the creative experience. |
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 1]| The value of Attribute 1 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 2]| The value of Attribute 2 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 3]| The value of Attribute 3 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 4]| The value of Attribute 3 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 5]| The value of Attribute 5 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Device]|[!UICONTROL Device Browser]|The browser in which the ad was shown (such as [!UICONTROL Chrome] or [!UICONTROL Firefox]).|
|\[Dimension\]|[!UICONTROL Device]|[!UICONTROL Device OS]|The operating system on which the ad was shown (such as [!UICONTROL Windows]).|
|\[Dimension\]|[!UICONTROL Device]|[!UICONTROL Device Type]|The type of device on which the ad was shown (such as [!UICONTROL Desktop]).|
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Name]| The name of the DSP on which ads were run. |
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Placement ID]| The ID of the placement for which ads were run. |
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Placement Name]| The name of the placement for which ads were run. |
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Site ID]| The ID of the site on which ads were run.|
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Site Name]| The name of the site on which ads were run. |
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Ad Tag Id]|The ID that [!UICONTROL Creative] assigned to the ad experience tag.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Advertiser Name]| The name of the advertiser.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Date/Time]|The date and time of the event.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Experience ID]| The ID that [!UICONTROL Creative] assigned to the experience.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Experience Name]| The name of the experience.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Targeting Branch Value]| The specific path through the targeting decision tree that determined which creative experience variant was served to the user.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Trafficking Line]| The name of the ad tag. |
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL City]|The city to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL Country Code]|The country code for the country to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL DMA]|The Designated Market Area (DMA) to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL State Code]|The state code for the state to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL Zip Code]|The zip code to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Category ID]|(Dynamic ads) The target product category ID.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Category Name]|(Dynamic ads) The target product category name.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 1]|(Dynamic ads) The first creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 2]|(Dynamic ads) The second creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 3]|(Dynamic ads) The third creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 4]|(Dynamic ads) The fourth creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 5]|(Dynamic ads) The fifth creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Product ID]|(Dynamic ads) The target product ID.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Product Name]|(Dynamic ads) The target product name.|
|\[Dimension\]|[!UICONTROL Segment]|[!UICONTROL Matched Audience Segment ID]|The IDs for up to five user segments that matched the ad theme.|
|\[Dimension\]|[!UICONTROL Segment]|[!UICONTROL Pixel Segment ID]|The ID for a retargeting pixel to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Segment]|[!UICONTROL Pixel Segment Name]|The name of a retargeting pixel to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Segment]|[!UICONTROL Segment Values]|The attributes for an audience segment to which the reported data is attributed.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Clicks]|The sum of all clicks on an ad.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL CTR]|The click-through rate, which is the percentage of clicks divided by ad impressions.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Engagement Rate]|The percentage of impressions served that resulted in user engagements.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Engagements]|The number of interactions on a served ad.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Impressions]|The total number of ad impressions.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Media Match Rate]| The percentage of impressions with a retargeted cookie. |
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Clicks]|(Dynamic ads only) The sum of all clicks on ads for a product. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Conversion]|(Dynamic ads only) The sum of all conversions on ads for a product. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Conversion Rate]|(Dynamic ads only) The percentage of ads for a product that resulted in conversions. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product CTR]|(Dynamic ads only) The click-through rate for ads for a product, which is the percentage of clicks divided by ad impressions. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Impressions]|(Dynamic ads only) The total number of impressions for a product. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Revenue]|(Dynamic ads only) The total revenue on served ads for a product. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Revenue]|The total revenue on served ads.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 100% Completion Rate]|The percentage of views that watched the ad in its entirety.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 25% Completion Rate]|The percentage of views that watched at least one quartile of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 50% Completion Rate]|The percentage of views that watched at least two quartiles of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 75% Completion Rate]|The percentage of views that watched at least three quartiles of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 100% Completions]|The number of views that watched the ad in its entirety.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 25% Completions]|The number of views that watched at least one quartile of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 50% Completions]|The number of views that watched at least two quartiles of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 75% Completions]|The number of views that watched at least three quartiles of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Avg Percent Viewed]|The average percentage an ad was watched to completion, accounting for all views.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Play Rate]|The percentage of impressions served that resulted in video views.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Playtime per View]|The average duration of a video view, measured in seconds.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Viewed Minutes]|The total number of minutes a video ad was viewed.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Views]|The total number of video ad views.




|[!UICONTROL Metrics]|[!UICONTROL Viewability]|[!UICONTROL 100% Viewable Completion (%)]| .|
|[!UICONTROL Metrics]|[!UICONTROL Viewability]|[!UICONTROL 50% Viewable Completion (%)]| .|
|[!UICONTROL Metrics]|[!UICONTROL Viewability]|[!UICONTROL Viewability Rate (%)]|The percentage of viewable impressions out of all measurable impressions, calculated as <code>[!UICONTROL Viewable Impressions] / [!UICONTROL Measurable Impressions]</code>.|
|[!UICONTROL Metrics]|[!UICONTROL Viewability]|[!UICONTROL Viewable Impressions]|The number of ad impressions considered viewable.|
|[!UICONTROL Conversion Metrics]|[Grouped by advertiser in report settings]|[Advertiser-specific conversion]| The total for a specified advertiser-specific conversion metric or Adobe Analytics event.|
|[!UICONTROL Custom Goals]|[Grouped by advertiser in report settings]|[Advertiser-specific custom goal]|(Advertisers with Advertising DSP) The weighted sum of all conversions that are included in the specified [Advertising DSP custom goal](/help/dsp/optimization/custom-goal.md).|

{style="table-layout:auto"}

-->

>[!MORELIKETHIS]
>
>* [Rapporti sulle prestazioni a livello di esperienza](/help/creative/experiences/experience-performance-details.md)
>* [Informazioni sui report personalizzati di DSP](/help/dsp/reports/report-about.md){target="_blank"}
>* [Informazioni su [!UICONTROL report destinations]](/help/dsp/reports/report-destinations/report-destination-about.md){target="_blank"}
