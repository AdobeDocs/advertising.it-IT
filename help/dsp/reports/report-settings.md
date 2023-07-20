---
title: Impostazioni report personalizzati
description: Consulta le descrizioni delle impostazioni del rapporto personalizzato.
feature: DSP Custom Reports
exl-id: 0e9e4332-3c10-44b0-b315-691b22dfb3c7
source-git-commit: 781b0c8874d73d060bc7133bdd55d1ceffb63435
workflow-type: tm+mt
source-wordcount: '1171'
ht-degree: 0%

---

# Impostazioni report personalizzati

**[!UICONTROL Name]** Il nome del rapporto. La lunghezza massima è di 180 caratteri.

**[!UICONTROL Report Type]** Tipo di rapporto: *[!UICONTROL Custom]* (che include la maggior parte delle opzioni disponibili), *[!UICONTROL Billing]*, *[!UICONTROL Conversion]*, *[!UICONTROL Device]*, *[!UICONTROL Frequency (by Impression)]*,  *[!UICONTROL Frequency (by App/Site)]*, *[!UICONTROL Geo]*, *[!UICONTROL Margin]*, *[!UICONTROL Media Performance]*,  *[!UICONTROL Segment]*, *[!UICONTROL Site]*, *[!UICONTROL Household Reach & Frequency]*, o *[!UICONTROL Household Conversions]*.

## [!UICONTROL Apply Filters] Sezione

**[!UICONTROL Timezone]:** Il fuso orario per il reporting.

**[!UICONTROL Observe Daylight Savings Time]:** Considera l’ora legale negli orari segnalati.

**\[Intervallo date\]:** L’intervallo di date per il quale generare i dati. Il numero di giorni disponibili varia in base al rapporto e alle dimensioni selezionate. Sceglietene uno:

* **[!UICONTROL Previous N days]:** Include i dati per un numero specifico di giorni prima di oggi.

* **[!UICONTROL Custom]:** Include i dati tra date di inizio e fine specifiche. Per segnalare i dati fino al giorno precedente, seleziona **[!UICONTROL Present]**.

* **[!UICONTROL Last Calendar Month]:** Include i dati relativi al mese di calendario precedente.

**[!UICONTROL Add Filters]:** (Facoltativo) Dimensioni aggiuntive in base alle quali filtrare i dati, indipendentemente dal fatto che le dimensioni siano incluse o meno come colonne nel rapporto. I filtri disponibili variano in base al tipo di rapporto e possono includere: *[!UICONTROL Account]*\*, *[!UICONTROL Ad Type]*, *[!UICONTROL Ads]*, *[!UICONTROL Advertiser]*, *[!UICONTROL Campaign]*, *[!UICONTROL Country]*, * *[!UICONTROL Package]*, *[!UICONTROL Placement]*, *[!UICONTROL Video]*, e *[!UICONTROL Video Duration]*.

\* *[!UICONTROL Account]* è disponibile per i seguenti tipi di rapporto solo quando l’organizzazione è configurata per [reporting tra account](report-about.md#cross-account-reporting):  [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)], e [!UICONTROL Conversion]. Per ulteriori informazioni sul reporting tra account, contatta il team dell’account di Adobe.

Per applicare uno o più filtri, effettuare le seguenti operazioni:

* Selezionare una dimensione, quindi selezionare l&#39;operatore (*è uguale a* o *diverso da*), quindi selezionare il valore applicabile. Ad esempio, per restituire dati solo per gli annunci preroll, specifica &quot;[!UICONTROL Ad Type equals Preroll].&quot;
* (Facoltativo) Aggiungi criteri aggiuntivi al filtro.
* (Facoltativo) Aggiungi altri filtri, ciascuno con uno o più criteri.

## [!UICONTROL Build Your Report] Sezione

**[!UICONTROL Select To Add As Report Headers]:**  Le colonne di dati, o intestazioni, da includere nel rapporto. Per aggiungere una colonna, espandere la categoria e selezionare la casella di controllo accanto al nome della colonna. Le colonne disponibili variano a seconda del rapporto e tutte le metriche non disponibili sono disabilitate. Le categorie di dati disponibili includono:

* [!UICONTROL Dimensions]

  >[!NOTE]
  >
  > Il [!UICONTROL Household Reach & Frequency] il rapporto può includere una sola dimensione.

* [!UICONTROL Metrics]

  >[!NOTE]
  >
  >Il [!UICONTROL Household Reach & Frequency] Il rapporto può includere metriche di sovrapposizione o metriche non di sovrapposizione, ma non entrambe.

* [!UICONTROL Conversion Metrics] (ordinato per inserzionista)

* [!UICONTROL Custom Goals] (ordinato per inserzionista)

Consulta &quot;[Colonne report disponibili](report-columns.md)&quot; per le descrizioni di tutte le opzioni.

**[!UICONTROL Drag to Re-Order Report Headers Below]:** Ordine delle intestazioni di colonna. Puoi trascinare e rilasciare qualsiasi colonna per personalizzare l’ordine.

**[!UICONTROL Format]:** Se generare un rapporto in *[!UICONTROL CSV]* (valori separati da virgole) o *[!UICONTROL Tab]* (valori separati da tabulazioni).

**[!UICONTROL Headers]:** Se a *[!UICONTROL Include]* o *[!UICONTROL Do Not Include]* intestazioni di colonna.

## [!UICONTROL Multi-Touch Conversion Options] Sezione

**[!UICONTROL Attribution Rule Settings]** Le impostazioni variano in base al tipo di rapporto:

* **\[Tipo di attribuzione\]:** ([!UICONTROL Household Conversion] rapporti con [!UICONTROL Conversion Metrics] o [!UICONTROL Custom Goals] colonne; solo per gli inserzionisti con tracciamento conversione Adobe Advertising) All’interno del rapporto, come attribuire i dati di conversione in una serie di eventi che portano a una conversione:

   * *[!UICONTROL Unique]:* (Impostazione predefinita) Conta il numero di volte in cui un valore di dimensione (ad esempio un dispositivo o un posizionamento) si trovava sul percorso di conversione.

   * *[!UICONTROL Multi-Touch Attribution (MTA)]:*  Distribuisce il credito di ogni conversione in base alla frequenza di occorrenza del valore di dimensione (ad esempio un dispositivo o un posizionamento) nel percorso di conversione. Ad esempio, se il totale delle impression prima della conversione era 10, con 8 su CTV e 2 su Mobile, l&#39;80% del credito (0,8) viene assegnato agli schermi CTV e 0,2 a Mobile.

* **\[Tipo di regola\]:** (Tutti [!UICONTROL Custom], [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], [!UICONTROL Segment], e [!UICONTROL Site] rapporti con [!UICONTROL Conversion Metrics] o [!UICONTROL Custom Goals] colonne; solo per gli inserzionisti con tracciamento delle conversioni di Adobi Advertising) All’interno del rapporto, come attribuire i dati di conversione in una serie di eventi che portano a una conversione. Puoi scegliere più di una regola se desideri confrontare le differenze tra le regole.

  >[!NOTE]
  >
  >I percorsi di conversione includono eventuali impression e clic all’interno degli intervalli di impression o lookback di clic dell’inserzionista, configurati in [!DNL Advertising Search, Social, & Commerce]. Ai clic viene data la preferenza alle impression durante l’attribuzione della conversione. Tutti i clic in un percorso di conversione ricevono il pieno credito in base alla regola di attribuzione. Il merito delle impression viene attribuito solo quando nel percorso di conversione non vengono tracciati clic.

   * *[!UICONTROL Last Event]:* Attribuisce le conversioni all’ultimo clic o impression nel percorso di conversione.

   * *[!UICONTROL Weight Last More]:* Attribuisce le conversioni a tutti gli eventi nel percorso di conversione, ma attribuisce il maggior peso all’ultimo evento e successivamente meno peso agli eventi precedenti.

   * *[!UICONTROL Even Distribution]:* Attribuisce le conversioni in modo uguale a ciascun evento nel percorso di conversione.

   * *[!UICONTROL Weight First More]:* Attribuisce le conversioni a tutti gli eventi nel percorso di conversione, ma attribuisce il maggior peso al primo evento e successivamente meno peso ai seguenti eventi.

   * *[!UICONTROL First Event]:* Attribuisce le conversioni al primo clic o impression nel percorso di conversione.

   * *[!UICONTROL U-shaped]:* Attribuisce la conversione a tutti gli eventi nel percorso di conversione, ma attribuisce il maggior peso al primo e all’ultimo evento, con un peso progressivamente inferiore agli eventi nel mezzo del percorso di conversione.

   * *[!UICONTROL Display Only]:*  Attribuisce le conversioni all’ultimo clic o impression DSP nel percorso di conversione. Ciò include video e annunci TV collegati ed esclude i clic su [!DNL Advertising Search, Social, & Commerce] annunci.

   * *[!UICONTROL Social Only]:* Obsoleto

  <!-- See also [How Attribution Rules Are Calculated for Adobe Advertising](). -->

* **Lookback** ([!UICONTROL Household Conversion] rapporti con [!UICONTROL Conversion Metrics] o [!UICONTROL Custom Goals] colonne; solo per gli inserzionisti con tracciamento delle conversioni di Adobi Advertising) All’interno del rapporto, il numero massimo di giorni dopo un evento di impression in cui è possibile attribuirgli un evento di conversione. Il valore predefinito è *[!UICONTROL 30 days]* e il massimo è 92 giorni.

**[!UICONTROL Paths as Columns]:**  (Tutti [!UICONTROL Custom], [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], [!UICONTROL Segment], e [!UICONTROL Site] rapporti con [!UICONTROL Conversion Metrics] o [!UICONTROL Custom Goals] colonne) Quali tipi di conversioni segnalare quando si sono verificati eventi precedenti sullo stesso dispositivo. Puoi includere fino a tre tipi. Per ogni tipo selezionato, viene inclusa una colonna separata per ogni metrica di conversione e viene aggiunta una colonna con il suffisso specificato ([!UICONTROL (tl)], [!UICONTROL (ct)], o [!UICONTROL (vt)]):

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]:* Include le conversioni attribuite ai clic (TC per click-through) e alle impression (VT per view-through). Le conversioni attribuite alle impression vengono moltiplicate per il peso view-through specificato. Il peso view-through predefinito è 100%, il che significa che le conversioni attribuite alle impression vengono conteggiate come il 100% del valore delle conversioni attribuite ai clic.

* *[!UICONTROL With Clicks (CT)]:* Include solo le conversioni attribuite ai clic.

* *[!UICONTROL Impressions Only (VT)]:* Include solo le conversioni attribuite alle impression perché non è stato tracciato alcun clic nel percorso di conversione.

**[!UICONTROL Conversion Reporting Based On]:**  Come segnalare i dati di conversione:

* *[!UICONTROL Conversion Timestamp]:* (Impostazione predefinita) Le conversioni verranno associate alla data di conversione.

* *[!UICONTROL Event Timestamp]:* Le conversioni verranno segnalate in base alla data dell’impression o del clic che ha causato la conversione, come determinato dal valore specificato [!UICONTROL Attribution Rule Settings].

## [!UICONTROL Add Report Destinations] Sezione

**[!UICONTROL Destination Type]:** Scegliere uno dei seguenti tipi di destinazione:

* *[!UICONTROL S3]:* Per inviare il report completato a uno o più [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3]), che verranno specificate nella sezione **[!UICONTROL Destination Name]** campo.
* *[!UICONTROL sFTP]:* Per inviare il rapporto completato a una o più posizioni SFTP, che specificherai nella **[!UICONTROL Destination Name]** campo.
* *[!UICONTROL FTP]:* Per inviare il report completato a una o più posizioni FTP, che verranno specificate nella **[!UICONTROL Destination Name]** campo.
* *[!UICONTROL FTP SSL](attualmente in versione beta):* Per inviare il report completato a una o più posizioni FTP SSL, che verranno specificate nella **[!UICONTROL Destination Name]** campo.
* *[!UICONTROL Email]:* Per specificare gli indirizzi e-mail a cui inviare i report completati o le notifiche se il report viene annullato a causa di errori. Per specificare più indirizzi, separali con virgole o spazi.

>[!NOTE]
>
> Una volta salvato il rapporto, non puoi modificare il tipo di destinazione.

**[!UICONTROL Destination Name]:** (Solo per i tipi di destinazione S3, FTP, sFTP e FTP SSL) I nomi delle destinazioni dei rapporti a cui verrà inviato il rapporto personalizzato.

* Per specificare una destinazione esistente, selezionare un nome di destinazione dall&#39;elenco. Puoi selezionare separatamente più nomi di destinazione.

* Per creare una nuova destinazione:

   1. Clic **Aggiungi nuova destinazione**.

   1. Inserisci il [impostazioni di destinazione del rapporto](/help/dsp/reports/report-destinations/report-destination-settings.md)e fai clic su **Salva**.

   1. Nelle impostazioni del rapporto, fai clic su **Aggiorna i nomi delle destinazioni.**

      La nuova destinazione è ora disponibile dall’elenco delle destinazioni esistenti e, facoltativamente, può essere aggiunta al rapporto.

**[!UICONTROL Frequency]:** (Per ogni [!UICONTROL Destination Name] Con quale frequenza inviare il rapporto alla destinazione: *[!UICONTROL Once]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, o *[!UICONTROL Monthly]*.

## [!UICONTROL Save Report] Sezione

**[!UICONTROL Send & Save]:** Quando inviare il rapporto: *[!UICONTROL On Schedule]* o *[!UICONTROL Run Now]*. I report pianificati verranno consegnati entro le 09:00 nel fuso orario dell’account.

>[!NOTE]
>
>È possibile [eseguire un rapporto personalizzato in qualsiasi momento](report-run-now.md) dal [!UICONTROL Reports] visualizzazione.

>[!MORELIKETHIS]
>
>* [Informazioni sui report personalizzati](/help/dsp/reports/report-about.md)
>* [Creare un rapporto personalizzato](/help/dsp/reports/report-create.md)
>* [Duplicare un rapporto personalizzato](/help/dsp/reports/report-copy.md)
>* [Modificare un rapporto personalizzato](/help/dsp/reports/report-edit.md)
>* [Eseguire un rapporto personalizzato](/help/dsp/reports/report-run-now.md)
>* [Impostazioni report personalizzati](/help/dsp/reports/report-settings.md)
>* [Informazioni sulle destinazioni dei rapporti](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [Colonne report disponibili](/help/dsp/reports/report-columns.md)
