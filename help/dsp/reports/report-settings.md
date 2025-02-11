---
title: Impostazioni report personalizzati
description: Consulta le descrizioni delle impostazioni del rapporto personalizzato.
feature: DSP Custom Reports
exl-id: 0e9e4332-3c10-44b0-b315-691b22dfb3c7
source-git-commit: 195e75386e64c3659d3f4db3c2508ac903e9e311
workflow-type: tm+mt
source-wordcount: '1541'
ht-degree: 0%

---

# Impostazioni report personalizzati

**[!UICONTROL Name]:** Il nome del report. La lunghezza massima è di 180 caratteri.

**[!UICONTROL Report Type]:** Tipo di report: *[!UICONTROL Custom]* (che include la maggior parte delle opzioni disponibili), *[!UICONTROL Billing]*, *[!UICONTROL Conversion]*, *[!UICONTROL Device]*, *[!UICONTROL Frequency (by Impression)]*, *[!UICONTROL Frequency (by App/Site)]*, *[!UICONTROL Geo]*, *[!UICONTROL Margin]*, *[!UICONTROL Media Performance]*, *[!UICONTROL Segment]*, *[!UICONTROL Site]*, *[!UICONTROL Household Reach & Frequency]*, *[!UICONTROL Household Conversions]*, *[!UICONTROL Path to Conversions Beta]*, *[!UICONTROL Path Length Beta]* o *[!UICONTROL Time to Conversion Beta]*.

## Sezione [!UICONTROL Report Range]

Questa sezione determina i dati inclusi nel rapporto. Per impostare le date per la pianificazione del report, vedere la sezione &quot;[!UICONTROL Report run schedule]&quot;.

**[!UICONTROL Timezone]:** Il fuso orario per il reporting.

**[!UICONTROL Observe Daylight Savings Time]:** considera l&#39;ora legale negli orari segnalati.

**Intervallo:** l&#39;intervallo di date per il quale generare i dati. Il numero di giorni disponibili varia in base al rapporto e alle dimensioni selezionate. Sceglietene uno:

* **[!UICONTROL Previous Calendar Week]:** include i dati per la settimana di calendario precedente.

* **[!UICONTROL Previous Calendar Month]:** include i dati per il mese di calendario precedente.

* **[!UICONTROL Custom Range]:** include dati tra date di inizio e fine specifiche. Per segnalare i dati relativi al giorno precedente, selezionare **[!UICONTROL Present]**.

## Sezione [!UICONTROL Report Run schedule]

Questa sezione determina le date di esecuzione del rapporto. Per impostare le date per le quali includere i dati del report, vedere la sezione &quot;[!UICONTROL Report range]&quot;.

**\[Schedule\]:** Quando generare il report:

* *[!UICONTROL Immediately]*: aggiunge immediatamente il report alla coda dei report.

  >[!NOTE]
  >
  >È inoltre possibile [eseguire un report personalizzato in qualsiasi momento](report-run-now.md) dalla visualizzazione [!UICONTROL Reports].

* *[!UICONTROL On]\&lt;Data\>:* Esegue il report in una data specificata per il completamento entro le 09:00 nel fuso orario dell&#39;account.

* *[!UICONTROL Recurring]:* Esegue il report in base a una pianificazione durante un periodo di tempo specificato.

   * **\[Pianificazione\]:** Frequenza di esecuzione del report:

      * *Giornaliero* per eseguire il report ogni N giorni. Ad esempio, per eseguire il report ogni due settimane (14 giorni), selezionare questa opzione e immettere **14**.

      * *Settimanale* per eseguire il report nei giorni della settimana specificati. Ad esempio, per eseguire il report ogni lunedì e venerdì, selezionare questa opzione e selezionare le caselle di controllo accanto a **lunedì** e **venerdì**.

      * *Mensile* per eseguire il report in un giorno numerico specifico del mese, da 1 a 30. Ad esempio, eseguire il report il primo giorno di ogni mese, selezionare questa opzione e immettere **1**.

   * **Da**: prima data in cui è possibile eseguire il report. A seconda della pianificazione specificata, la prima istanza di report può essere successiva a tale data.

   * **Fino a**: la data di scadenza del report, che può essere un massimo di quattro mesi di calendario. Prima della scadenza di un rapporto, tutte le destinazioni e-mail specificate ricevono un avviso e-mail sette giorni e un giorno prima della data di scadenza. Per mantenere il report più a lungo, modifica questa data.

## Sezione [!UICONTROL Apply Filters]

**[!UICONTROL Filter by]:** (facoltativo) dimensioni aggiuntive in base alle quali filtrare i dati, indipendentemente dal fatto che le dimensioni siano incluse o meno come colonne nel report. I filtri disponibili variano in base al tipo di report e possono includere: *[!UICONTROL Account]*\*, *[!UICONTROL Ad Type]*, *[!UICONTROL Ads]*, *[!UICONTROL Advertiser]*, *[!UICONTROL Campaign]*, *[!UICONTROL Country]*, * *[!UICONTROL Package]*, *[!UICONTROL Placement]*, *[!UICONTROL Video]* e *[!UICONTROL Video Duration]*.

Per applicare uno o più filtri, effettuare le seguenti operazioni:

* Selezionare una dimensione, selezionare l&#39;operatore (*uguale a* o *diverso da*), quindi selezionare il valore applicabile. Ad esempio, per restituire dati solo per gli annunci preroll, specificare &quot;[!UICONTROL Ad Type equals Preroll]&quot;.
* (Facoltativo) Aggiungi criteri aggiuntivi al filtro.
* (Facoltativo) Aggiungi altri filtri, ciascuno con uno o più criteri.

\* *[!UICONTROL Account]* è disponibile per i seguenti tipi di report solo quando l&#39;organizzazione è configurata per [rapporti tra account diversi](report-about.md#cross-account-reporting): [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)] e [!UICONTROL Conversion]. Contatta il team del tuo account Adobe per ulteriori informazioni sul reporting tra account diversi.

**[!UICONTROL Include data from Adobe Advertising SSC]:** (solo rapporti Percorso di conversione, Lunghezza percorso e Tempo di conversione) Include i dati per i clic sugli annunci di ricerca da campagne Advertising Search, Social e Commerce specificate. Quando selezioni questa opzione:

1. Seleziona l&#39;account di ricerca, social e Commerce utilizzando il filtro **Filtra per[!UICONTROL SSC Account]**.

1. Seleziona le campagne utilizzando il filtro **Filtra per[!UICONTROL SSC Campaign]**.

   Per selezionare più campagne, fare clic su **[!UICONTROL Add Criteria]** per la seconda e le campagne successive.

## Sezione [!UICONTROL Build Your Report]

**[!UICONTROL Select To Add As Report Headers]:** le colonne di dati, o intestazioni, da includere nel report. Per aggiungere una colonna, espandere la categoria e selezionare la casella di controllo accanto al nome della colonna. Le colonne disponibili variano a seconda del rapporto e tutte le metriche non disponibili sono disabilitate. Le categorie di dati disponibili possono comprendere:

* [!UICONTROL Dimensions]

  >[!NOTE]
  >
  > I report [!UICONTROL Household Reach & Frequency] e [!UICONTROL Path to Conversion] possono includere una sola dimensione.
  > I report [!UICONTROL Path Length] e [!UICONTROL Time to Conversion] non includono dimensioni.

* [!UICONTROL Metrics]

  >[!NOTE]
  >
  >Il report [!UICONTROL Household Reach & Frequency] può includere metriche di sovrapposizione o metriche non di sovrapposizione, ma non entrambe.

* [!UICONTROL Conversion Metrics] (ordinato per inserzionista)

* [!UICONTROL Custom Goals] (ordinato per inserzionista)

Per le descrizioni di tutte le opzioni, vedere &quot;[Colonne report disponibili](report-columns.md)&quot;.

**[!UICONTROL Drag to Re-Order Report Headers Below]:** Ordine delle intestazioni di colonna. Puoi trascinare e rilasciare qualsiasi colonna per personalizzare l’ordine.

**[!UICONTROL Format]:** se generare un report in formato *[!UICONTROL CSV]* (valori separati da virgola) o *[!UICONTROL Tab]* (valori separati da tabulazione).

**[!UICONTROL Headers]:** se *[!UICONTROL Include]* o *[!UICONTROL Do Not Include]* intestazioni di colonna.

## Sezione [!UICONTROL Multi-Touch Conversion Options]

**[!UICONTROL Attribution Rule Settings]:** Le impostazioni variano in base al tipo di report:

* **\[Tipo di attribuzione\]:** ([!UICONTROL Household Conversion] report con [!UICONTROL Conversion Metrics] o [!UICONTROL Custom Goals] colonne; solo per gli inserzionisti con Adobe Advertising di tracciamento delle conversioni) All&#39;interno del report, come attribuire i dati di conversione in una serie di eventi che portano a una conversione:

   * *[!UICONTROL Unique]:* (impostazione predefinita) Conta il numero di volte in cui un valore di dimensione (ad esempio un dispositivo o un posizionamento) si trovava nel percorso di conversione.

   * *[!UICONTROL Multi-Touch Attribution (MTA)]:* distribuisce il credito di ogni conversione in base alla frequenza di occorrenza del valore di dimensione (ad esempio un dispositivo o un posizionamento) nel percorso di conversione. Ad esempio, se il totale delle impression prima della conversione era 10, con 8 su CTV e 2 su Mobile, l&#39;80% del credito (0,8) viene assegnato agli schermi CTV e 0,2 a Mobile.

* **\[Tipo di regola\]:** (tutti i report [!UICONTROL Custom], [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], [!UICONTROL Segment] e [!UICONTROL Site] con [!UICONTROL Conversion Metrics] o [!UICONTROL Custom Goals] colonne; solo per gli inserzionisti con Adobe Advertising di tracciamento delle conversioni) All&#39;interno del report, come attribuire i dati di conversione in una serie di eventi che portano a una conversione. Puoi scegliere più di una regola se desideri confrontare le differenze tra le regole.

  >[!NOTE]
  >
  >I percorsi di conversione includono eventuali impression e clic all&#39;interno degli intervalli di impression o di lookback dei clic dell&#39;inserzionista, configurati in [!DNL Advertising Search, Social, & Commerce]. Ai clic viene data la preferenza alle impression durante l’attribuzione della conversione. Tutti i clic in un percorso di conversione ricevono il pieno credito in base alla regola di attribuzione. Il merito delle impression viene attribuito solo quando nel percorso di conversione non viene tracciato alcun clic.

   * *[!UICONTROL Last Event]:* attribuisce le conversioni all&#39;ultimo clic o all&#39;ultima impression nel percorso di conversione.

   * *[!UICONTROL Weight Last More]:* attribuisce le conversioni a tutti gli eventi nel percorso di conversione, ma attribuisce il peso maggiore all&#39;ultimo evento e successivamente meno peso agli eventi precedenti.

   * *[!UICONTROL Even Distribution]:* attribuisce le conversioni in modo uguale a ogni evento nel percorso di conversione.

   * *[!UICONTROL Weight First More]:* attribuisce le conversioni a tutti gli eventi nel percorso di conversione, ma attribuisce il peso maggiore al primo evento e successivamente meno peso ai seguenti eventi.

   * *[!UICONTROL First Event]:* attribuisce le conversioni al primo clic o all&#39;impression nel percorso di conversione.

   * *[!UICONTROL U-shaped]:* attribuisce la conversione a tutti gli eventi nel percorso di conversione, ma attribuisce il maggior peso al primo e all&#39;ultimo evento, con un peso progressivamente inferiore agli eventi nel mezzo del percorso di conversione.

   * *[!UICONTROL Display Only]:* attribuisce le conversioni all&#39;ultimo clic o impression DSP nel percorso di conversione. Ciò include video e annunci TV connessi ed esclude i clic sugli annunci [!DNL Advertising Search, Social, & Commerce].

   * *[!UICONTROL Social Only]:* Obsoleto

Vedi anche &quot;[Modalità di calcolo delle regole di attribuzione, ad Adobe Advertising](/help/search-social-commerce/reports/attribution-rules.md).&quot;

* **Lookback:** ([!UICONTROL Household Conversion] report con [!UICONTROL Conversion Metrics] o [!UICONTROL Custom Goals] colonne e [!UICONTROL Path to Conversion], [!UICONTROL Path Length] o [!UICONTROL Time to Conversion] report solo con [!UICONTROL Conversion Metrics] colonne; solo per gli inserzionisti con Adobe Advertising di tracciamento delle conversioni) All&#39;interno del report, il numero massimo di giorni dopo un evento di impression o un evento di clic (per [!UICONTROL Path to Conversion], [!UICONTROL Path Length] o [!UICONTROL Time to Conversion] report) in cui è possibile attribuire un evento di conversione. Il valore predefinito è *[!UICONTROL 30 days]* e il massimo è 92 giorni.

  >[!TIP]
  >
  >Se utilizzi [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md), utilizza lo stesso intervallo di lookback utilizzato in [!DNL Analytics].

**[!UICONTROL Paths as Columns]:** (tutti i report [!UICONTROL Custom], [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], [!UICONTROL Segment] e [!UICONTROL Site] con [!UICONTROL Conversion Metrics] o [!UICONTROL Custom Goals] colonne) Quali tipi di conversioni segnalare quando si sono verificati eventi precedenti sullo stesso dispositivo. Puoi includere fino a tre tipi. Per ogni tipo selezionato, viene inclusa una colonna separata per ogni metrica di conversione e viene aggiunto il suffisso specificato ([!UICONTROL (tl)], [!UICONTROL (ct)] o [!UICONTROL (vt)]):

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]:* include conversioni attribuite ai clic (TC per click-through) e alle impression (VT per view-through). Le conversioni attribuite alle impression vengono moltiplicate per il peso view-through specificato. Il peso view-through predefinito è 100%, il che significa che le conversioni attribuite alle impression vengono conteggiate come il 100% del valore delle conversioni attribuite ai clic.

* *[!UICONTROL With Clicks (CT)]:* Include solo le conversioni attribuite ai clic.

* *[!UICONTROL Impressions Only (VT)]:* include solo le conversioni attribuite alle impression perché nel percorso di conversione non è stato tracciato alcun clic.

**[!UICONTROL Conversion Reporting Based On]:** Come segnalare i dati di conversione:

* *[!UICONTROL Conversion Timestamp]:* (impostazione predefinita) Le conversioni sono associate alla data di conversione.

* *[!UICONTROL Event Timestamp]:* Le conversioni vengono segnalate in base alla data dell&#39;impression o del clic che ha causato la conversione, come determinato dal [!UICONTROL Attribution Rule Settings] specificato.

## Sezione [!UICONTROL Add Report Destinations]

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

**[!UICONTROL Destination Name]:** (solo tipi di destinazione S3, FTP, sFTP e FTP SSL) i nomi delle destinazioni del report a cui viene inviato il report personalizzato.

* Per specificare una destinazione esistente, selezionare un nome di destinazione dall&#39;elenco. Puoi selezionare separatamente più nomi di destinazione.

* Per creare una nuova destinazione:

   1. Fare clic su **Aggiungi nuova destinazione**.

   1. Immetti le [impostazioni di destinazione del report](/help/dsp/reports/report-destinations/report-destination-settings.md) e fai clic su **Salva**.

   1. Nelle impostazioni del report, fare clic su **Aggiorna nomi di destinazione.**

      La nuova destinazione è ora disponibile dall’elenco delle destinazioni esistenti e, facoltativamente, può essere aggiunta al rapporto.

>[!MORELIKETHIS]
>
>* [Informazioni sui report personalizzati](/help/dsp/reports/report-about.md)
>* [Crea un report personalizzato](/help/dsp/reports/report-create.md)
>* [Duplica un report personalizzato](/help/dsp/reports/report-copy.md)
>* [Modifica un report personalizzato](/help/dsp/reports/report-edit.md)
>* [Scarica un report personalizzato](/help/dsp/reports/report-download.md)
>* [Esegui un report personalizzato](/help/dsp/reports/report-run-now.md)
>* [Impostazioni report personalizzati](/help/dsp/reports/report-settings.md)
>* [Informazioni sulle destinazioni dei report](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [Colonne report disponibili](/help/dsp/reports/report-columns.md)
