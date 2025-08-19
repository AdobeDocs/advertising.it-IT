---
title: '[!UICONTROL Custom Creative Report]'
description: Scopri come generare la cross-experience [!UICONTROL Custom Creative Report].
feature: Creative Reporting
exl-id: 13687d9d-6283-40ac-86a2-bb88b9fdfcc3
source-git-commit: bf969c1b3cc57e2ef83087952a9bac530b276916
workflow-type: tm+mt
source-wordcount: '2021'
ht-degree: 0%

---

# [!UICONTROL Custom Creative Report]

*funzionalità Beta*

[!UICONTROL Custom Creative Report] ti consente di personalizzare il contenuto e la distribuzione dei dati dei rapporti per tutte le esperienze pubblicitarie.

Puoi generare i rapporti una volta o pianificarli ogni giorno, ogni settimana o ogni mese alle ore 03:00 nel fuso orario specificato in base a criteri specifici, ad esempio ogni 15 giorni o il 1° di ogni mese. Una volta generato un report, puoi scaricarlo da [!UICONTROL Reports] > [!UICONTROL Custom Reports] o da [destinazioni report](/help/dsp/reports/report-destinations/report-destination-about.md) collegate dei seguenti tipi:

* [!DNL Amazon Simple Storage Service] ([!DNL S3])
* FTP
* SSL FTP <!-- (in beta) -->
* SFTP

## Crea un [!UICONTROL Custom Creative Report]

1. Nel menu principale, fare clic su **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**.

1. In alto a destra, fare clic su **[!UICONTROL Create]**.

1. Specifica le [impostazioni report](#report-settings).

1. Fare clic su **[!UICONTROL Create Custom Report]**.

## Impostazioni dei rapporti {#report-settings}

**[!UICONTROL Name]:** Il nome del report. La lunghezza massima è di 180 caratteri.

**[!UICONTROL Report Type]:** Il tipo di report: *[!UICONTROL Custom Creative Beta]*.

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
  >È inoltre possibile [eseguire un report personalizzato in qualsiasi momento](/help/dsp/reports/report-run-now.md) dalla visualizzazione [!UICONTROL Reports].

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

**[!UICONTROL Select To Add As Report Headers]:** le colonne di dati, o intestazioni, da includere nel report. Per aggiungere una colonna, espandere la categoria e selezionare la casella di controllo accanto al nome della colonna. Le colonne disponibili variano a seconda del rapporto e tutte le metriche non disponibili sono disabilitate. Per le descrizioni di tutte le opzioni, vedere &quot;[Colonne report disponibili](#report-custom-creative-columns)&quot;.

**[!UICONTROL Drag to Re-Order Report Headers Below]:** Ordine delle intestazioni di colonna. Puoi trascinare e rilasciare qualsiasi colonna per personalizzare l’ordine.

**[!UICONTROL Format]:** se generare un report in formato *[!UICONTROL CSV]* (valori separati da virgola) o *[!UICONTROL Tab]* (valori separati da tabulazione).

**[!UICONTROL Headers]:** se *[!UICONTROL Include]* o *[!UICONTROL Do Not Include]* intestazioni di colonna.

### Sezione [!UICONTROL Multi-Touch Conversion Options]

**[!UICONTROL Attribution Rule Settings]:** Le impostazioni variano in base al tipo di report:

* **\[Tipo di attribuzione\]:** (solo per inserzionisti con tracciamento delle conversioni di Adobe Advertising) All&#39;interno del rapporto, come attribuire dati di conversione in una serie di eventi che portano a una conversione:

   * *[!UICONTROL Unique]:* (impostazione predefinita) Conta il numero di volte in cui un valore di dimensione (ad esempio un dispositivo o un posizionamento) si trovava nel percorso di conversione.

   * *[!UICONTROL Multi-Touch Attribution (MTA)]:* distribuisce il credito di ogni conversione in base alla frequenza di occorrenza del valore di dimensione (ad esempio un dispositivo o un posizionamento) nel percorso di conversione. Ad esempio, se il totale delle impression prima della conversione era 10, con 8 su CTV e 2 su Mobile, l&#39;80% del credito (0,8) viene assegnato agli schermi CTV e 0,2 a Mobile.

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

* *[!UICONTROL FTP SSL](attualmente in Beta):* Per inviare il report completato a uno o più percorsi SSL FTP, che è necessario selezionare nel campo **[!UICONTROL Destination Name]**.

* *[!UICONTROL Email]:* Specificare gli indirizzi e-mail a cui inviare i report completati o le notifiche se il report viene annullato a causa di errori.

**[!UICONTROL Email]:** (solo tipo di destinazione e-mail) Per ogni indirizzo, immettere l&#39;indirizzo e fare clic su **+**.

**[!UICONTROL Destination Name]:** (solo tipi di destinazione S3, FTP, sFTP e FTP SSL) i nomi delle [destinazioni del report](/help/dsp/reports/report-destinations/report-destination-about.md){target="_blank"} alle quali viene inviato il report personalizzato.

* Per specificare una destinazione esistente, selezionare un nome di destinazione dall&#39;elenco. Puoi selezionare separatamente più nomi di destinazione.

* Per creare una nuova destinazione:

   1. Fare clic su **Aggiungi nuova destinazione**.

   1. Immetti le [impostazioni di destinazione del report](/help/dsp/reports/report-destinations/report-destination-settings.md){target="_blank"} e fai clic su **Salva**.

   1. Nelle impostazioni del report, fare clic su **Aggiorna nomi di destinazione.**

      La nuova destinazione è ora disponibile dall’elenco delle destinazioni esistenti e, facoltativamente, può essere aggiunta al rapporto.

## Colonne report disponibili {#report-custom-creative-columns}

| Tipo di metrica | Sottotipo | Nome colonna | Descrizione |
|-----------|-------|-----------|-----------|
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Ad Size] | Dimensioni dell’annuncio pubblicato. |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Is Default] | Se l&#39;annuncio fornito era un annuncio immagine o un annuncio video predefinito per l&#39;esperienza. |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Rotation Type] | Se gli annunci sono stati ruotati in base al peso relativo (*Ponderato*) o algoritmicamente (*Algoritmico*). |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Creative ID] | ID assegnato da [!UICONTROL Creative] alla creatività. |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Creative Name] | Il nome della creatività. |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Creative Type] | Il tipo di creatività (ad esempio [!UICONTROL HTML5]). |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Parent Creative ID] | L&#39;ID che [!UICONTROL Creative] ha assegnato alla creatività principale. |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Parent Creative Name] | Nome del contenuto creativo principale. |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Parent Creative Type] | Il tipo di contenuto creativo principale (ad esempio [!UICONTROL HTML5]). |
| [!UICONTROL Dimension] | [!UICONTROL Click Events] | [!UICONTROL Ad Link] | L’URL della pagina di destinazione. |
| [!UICONTROL Dimension] | [!UICONTROL Click Events] | [!UICONTROL Click Type] | Il tipo specifico di interazione dell’utente. |
| [!UICONTROL Dimension] | [!UICONTROL Click Events] | [!UICONTROL Direction] | Il flusso direzionale o il percorso di navigazione dell’interazione clic dell’utente all’interno dell’esperienza creativa. |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Device Browser] | Browser in cui è stato visualizzato l&#39;annuncio (ad esempio [!UICONTROL Chrome] o [!UICONTROL Firefox]). |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Device OS] | Sistema operativo in cui è stato visualizzato l&#39;annuncio (ad esempio [!UICONTROL Windows]). |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Device Type] | Tipo di dispositivo su cui è stato visualizzato l&#39;annuncio (ad esempio [!UICONTROL Desktop]). |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Name] | Nome del DSP su cui sono stati eseguiti gli annunci. |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Placement ID] | ID del posizionamento per il quale sono stati eseguiti gli annunci. |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Placement Name] | Nome del posizionamento per il quale sono stati eseguiti gli annunci. |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Site ID] | ID del sito su cui sono stati eseguiti gli annunci. |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Site Name] | Il nome del sito in cui sono stati eseguiti gli annunci. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Ad Tag Id] | L&#39;ID che [!UICONTROL Creative] ha assegnato al tag esperienza annuncio. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Advertiser Name] | Nome dell&#39;inserzionista. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Date/Time] | La data e l’ora dell’evento. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Experience ID] | L&#39;ID assegnato [!UICONTROL Creative] all&#39;esperienza. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Experience Name] | Nome dell’esperienza. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Targeting Branch Value] | Il percorso specifico attraverso la struttura decisionale di targeting che ha determinato quale variante di esperienza creativa è stata fornita all’utente. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Trafficking Line] | Nome del tag dell’annuncio. |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL City] | La città alla quale sono attribuiti i dati segnalati. |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL Country Code] | Il codice del paese al quale sono attribuiti i dati segnalati. |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL DMA] | L’area di mercato designata (DMA) alla quale sono attribuiti i dati segnalati. |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL State Code] | Il codice dello stato a cui sono attribuiti i dati segnalati. |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL Zip Code] | Il codice postale al quale vengono attribuiti i dati segnalati. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Category ID] | (Annunci dinamici) L’ID della categoria del prodotto di destinazione. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Category Name] | (Annunci dinamici) Il nome della categoria del prodotto di destinazione. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 1] | (Annunci dinamici) Il primo attributo creativo. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 2] | (Annunci dinamici) Il secondo attributo creativo. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 3] | (Annunci dinamici) Il terzo attributo creativo. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 4] | (Annunci dinamici) Il quarto attributo creativo. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 5] | (Annunci dinamici) Il quinto attributo creativo. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Product ID] | (Annunci dinamici) L’ID prodotto di destinazione. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Product Name] | (Annunci dinamici) Il nome del prodotto target. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Matched Audience Segment ID] | Gli ID per un massimo di cinque segmenti di utenti che corrispondono al tema dell’annuncio. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Pixel Segment ID] | ID per un pixel di retargeting a cui vengono attribuiti i dati segnalati. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Pixel Segment Name] | Il nome di un pixel di retargeting a cui vengono attribuiti i dati segnalati. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Segment Values] | Attributi per un segmento di pubblico a cui sono attribuiti i dati segnalati. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Clicks] | La somma di tutti i clic su un annuncio. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL CTR] | Il tasso di click-through, che è la percentuale di clic divisa per le impression pubblicitarie. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Engagement Rate] | Percentuale di impression distribuite che hanno portato a impegni dell’utente. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Engagements] | Il numero di interazioni su un annuncio distribuito. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Impressions] | Numero totale di ad impression. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Media Match Rate] | Percentuale di impression con un cookie retargeting. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Clicks] | (Solo per annunci dinamici) La somma di tutti i clic sugli annunci di un prodotto. Quando il prodotto è nullo, questo valore è zero (0). |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Conversion] | (Solo per annunci dinamici) La somma di tutte le conversioni sugli annunci di un prodotto. Quando il prodotto è nullo, questo valore è zero (0). |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Conversion Rate] | (Solo annunci dinamici) La percentuale di annunci per un prodotto che ha generato conversioni. Quando il prodotto è nullo, questo valore è zero (0). |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Product CTR] | (Solo per annunci dinamici) Il tasso di click-through per gli annunci di un prodotto, che è la percentuale di clic divisa per le impression degli annunci. Quando il prodotto è nullo, questo valore è zero (0). |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Impressions] | (Solo per annunci dinamici) Il numero totale di impression per un prodotto. Quando il prodotto è nullo, questo valore è zero (0). |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Revenue] | (Solo per annunci dinamici) Il ricavo totale sugli annunci serviti per un prodotto. Quando il prodotto è nullo, questo valore è zero (0). |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Revenue] | Ricavi totali sugli annunci serviti. |
| [!UICONTROL Conversion Metrics] | [Raggruppato per inserzionista nelle impostazioni del report] | [Conversione specifica per l&#39;inserzionista] | Totale per una metrica di conversione o un evento Adobe Analytics specifico per l’inserzionista. |
| [!UICONTROL Custom Goals] | [Raggruppato per inserzionista nelle impostazioni del report] | [Obiettivo personalizzato specifico per l&#39;inserzionista] | (Inserzionisti con Advertising DSP) La somma ponderata di tutte le conversioni incluse nell&#39;[obiettivo personalizzato Advertising DSP](/help/dsp/optimization/custom-goal.md) specificato. |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [Rapporti sulle prestazioni a livello di esperienza](/help/creative/experiences/experience-performance-details.md)
>* [Informazioni sui report personalizzati di DSP](/help/dsp/reports/report-about.md){target="_blank"}
>* [Informazioni su [!UICONTROL report destinations]](/help/dsp/reports/report-destinations/report-destination-about.md){target="_blank"}
