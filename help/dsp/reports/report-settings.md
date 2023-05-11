---
title: Impostazioni report personalizzate
description: Consulta le descrizioni delle impostazioni dei rapporti personalizzate.
feature: DSP Custom Reports
exl-id: 0e9e4332-3c10-44b0-b315-691b22dfb3c7
source-git-commit: 2e0240ff1b342d5a0564e01ebec3ee313b488b59
workflow-type: tm+mt
source-wordcount: '1013'
ht-degree: 0%

---

# Impostazioni report personalizzate

**[!UICONTROL Name]** Nome del report. La lunghezza massima è di 180 caratteri.

**[!UICONTROL Report Type]** Tipo di rapporto: *[!UICONTROL Custom]* (che include la maggior parte delle opzioni disponibili), *[!UICONTROL Billing]*, *[!UICONTROL Conversion]*, *[!UICONTROL Device]*, *[!UICONTROL Frequency (by Impression)]*,  *[!UICONTROL Frequency (by App/Site)]*, *[!UICONTROL Geo]*, *[!UICONTROL Margin]*, *[!UICONTROL Media Performance]*,  *[!UICONTROL Segment]*, *[!UICONTROL Site]* oppure *[!UICONTROL Household]*.

## [!UICONTROL Apply Filters] Sezione

**[!UICONTROL Timezone]:** Il fuso orario per il reporting.

**[!UICONTROL Observe Daylight Savings Time]:** Considera l&#39;ora legale nei tempi indicati.

**\[Intervallo date\]:** L’intervallo di date per il quale generare i dati. Il numero di giorni disponibili varia in base al rapporto e alle dimensioni selezionate. Sceglietene uno:

* **[!UICONTROL Previous N days]:** Include dati per un numero specifico di giorni precedenti alla data odierna.

* **[!UICONTROL Custom]:** Include i dati tra date di inizio e di fine specifiche. Per segnalare i dati nel giorno precedente, seleziona **[!UICONTROL Present]**.

* **[!UICONTROL Last Calendar Month]:** Include i dati per il mese di calendario precedente.

**[!UICONTROL Add Filters]:** (Facoltativo) Dimensioni aggiuntive in base alle quali filtrare i dati, indipendentemente dal fatto che le dimensioni siano incluse o meno come colonne nel rapporto. I filtri disponibili variano a seconda del tipo di rapporto e possono includere: *[!UICONTROL Account]*\* *[!UICONTROL Ad Type]*, *[!UICONTROL Ads]*, *[!UICONTROL Advertiser]*, *[!UICONTROL Campaign]*, *[!UICONTROL Country]*, * *[!UICONTROL Package]*, *[!UICONTROL Placement]*, *[!UICONTROL Video]* e *[!UICONTROL Video Duration]*.

\* *[!UICONTROL Account]* è disponibile per i seguenti tipi di rapporto solo quando l’organizzazione è configurata per [segnalazione interaccount](report-about.md#cross-account-reporting):  [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)]e [!UICONTROL Conversion]. Contatta il team dell’account di Adobe per ulteriori informazioni sul reporting tra account diversi.

Per applicare uno o più filtri, procedi come segue:

* Seleziona una dimensione, seleziona l’operatore (*è* o *non è uguale a*), quindi seleziona il valore applicabile. Ad esempio, per restituire i dati solo per gli annunci precedenti, specifica &quot;[!UICONTROL Ad Type equals Preroll].&quot;
* (Facoltativo) Aggiungi ulteriori criteri al filtro.
* (Facoltativo) Aggiungi altri filtri, ciascuno con uno o più criteri.

## [!UICONTROL Build Your Report] Sezione

**[!UICONTROL Select To Add As Report Headers]:**  Le colonne di dati, o intestazioni, da includere nel rapporto. Per aggiungere una colonna, espandi la categoria e seleziona la casella di controllo accanto al nome della colonna. Le colonne disponibili variano a seconda del rapporto e tutte le metriche non disponibili sono disabilitate. Le categorie di dati disponibili includono:

* [!UICONTROL Dimensions]

   >[!NOTE]
   >
   > La [!UICONTROL Household] il rapporto può includere una sola dimensione.

* [!UICONTROL Metrics]

   >[!NOTE]
   >
   >La [!UICONTROL Household] può includere metriche di sovrapposizione o metriche di non sovrapposizione, ma non entrambe.

* [!UICONTROL Conversion Metrics] (ordinati per inserzionista)

* [!UICONTROL Custom Goals] (ordinati per inserzionista)

Vedere &quot;[Colonne dei rapporti disponibili](report-columns.md)&quot; per la descrizione di tutte le opzioni.

**[!UICONTROL Drag to Re-Order Report Headers Below]:** Ordine delle intestazioni di colonna. Puoi trascinare qualsiasi colonna per personalizzare l’ordine.

## [!UICONTROL Multi-Touch Conversion Options] Sezione

**[!UICONTROL Format]:** Se generare un rapporto in *[!UICONTROL CSV]* (valori separati da virgole) o *[!UICONTROL Tab]* Formato (valori separati da tabulazioni).

**[!UICONTROL Report Headers]:** Se *[!UICONTROL Include]* o *[!UICONTROL Do Not Include]* intestazioni di colonna.

**[!UICONTROL Attribution Rule Settings]:** (Tutte) [!UICONTROL Custom], [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], [!UICONTROL Segment]e [!UICONTROL Site] rapporti con [!UICONTROL Conversion Metrics] o [!UICONTROL Custom Goals] colonne; inserzionisti solo con Adobe di tracciamento della conversione pubblicitaria) All’interno del rapporto, come attribuire i dati di conversione in una serie di eventi che portano a una conversione. Puoi scegliere più di una regola per confrontare le differenze tra le regole.

>[!NOTE]
>
>I percorsi di conversione includono qualsiasi impression e clic all’interno delle finestre di lookback dell’inserzionista sull’impression o sul clic, configurate in [!DNL Advertising Search, Social, & Commerce]. I clic hanno la preferenza sulle impression durante l’attribuzione della conversione. Tutti i clic in un percorso di conversione ricevono il credito completo in base alla regola di attribuzione. Le impressioni ricevono credito solo quando non viene tracciato alcun clic nel percorso di conversione.

* *[!UICONTROL Last Event]:* Attribuisce conversioni all’ultimo clic o impression nel percorso di conversione.

* *[!UICONTROL Weight Last More]:* Attribuisce conversioni a tutti gli eventi nel percorso di conversione, ma attribuisce il maggior peso all’ultimo evento e in modo successivo minor peso agli eventi precedenti.

* *[!UICONTROL Even Distribution]:* Attribuisce conversioni uguali a ogni evento nel percorso di conversione.

* *[!UICONTROL Weight First More]:* Attribuisce conversioni a tutti gli eventi nel percorso di conversione, ma dà il massimo peso al primo evento e in modo sequenziale meno peso agli eventi seguenti.

* *[!UICONTROL First Event]:* Attribuisce conversioni al primo clic o impression nel percorso di conversione.

* *[!UICONTROL U-shaped]:* Attribuisce la conversione a tutti gli eventi nel percorso di conversione, ma dà il massimo peso al primo e all’ultimo evento, con un peso progressivamente inferiore rispetto agli eventi nel mezzo del percorso di conversione.

* *[!UICONTROL Display Only]:*  Attribuisce conversioni all’ultimo clic o impression DSP nel percorso di conversione. Questo include annunci video e TV connessi ed esclude i clic su [!DNL Advertising Search, Social, & Commerce] annunci pubblicitari.

* *[!UICONTROL Social Only]:* Obsoleto

<!-- See also [How Attribution Rules Are Calculated for Adobe Advertising](). -->

**[!UICONTROL Paths as Columns]:**  (Tutte) [!UICONTROL Custom], [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], [!UICONTROL Segment]e [!UICONTROL Site] rapporti con [!UICONTROL Conversion Metrics] o [!UICONTROL Custom Goals] Colonne) Quali tipi di conversioni segnalare quando si sono verificati eventi precedenti sullo stesso dispositivo. Puoi includere fino a tre tipi. Per ogni tipo selezionato, viene inclusa una colonna separata per ogni metrica di conversione e viene aggiunta con il suffisso specificato ([!UICONTROL (tl)], [!UICONTROL (ct)]oppure [!UICONTROL (vt)]):

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]:* Include le conversioni attribuite ai clic (CT per click-through) e alle impression (VT per view-through). Le conversioni attribuite alle impression vengono moltiplicate per il peso di visualizzazione specificato. Il peso predefinito della visualizzazione passante è 100%, il che significa che le conversioni attribuite alle impression vengono conteggiate come il 100% del valore delle conversioni attribuite ai clic.

* *[!UICONTROL With Clicks (CT)]:* Include solo le conversioni attribuite ai clic.

* *[!UICONTROL Impressions Only (VT)]:* Include solo le conversioni attribuite alle impression perché non sono stati tracciati clic nel percorso di conversione.

**[!UICONTROL Conversion Reporting Based On]:**  Come segnalare i dati di conversione:

* *[!UICONTROL Conversion Timestamp]:* (L’impostazione predefinita) Le conversioni saranno associate alla data di conversione.

* *[!UICONTROL Event Timestamp]:* Le conversioni verranno riportate in base alla data dell&#39;impression o del clic che ha causato la conversione, come determinato dal [!UICONTROL Attribution Rule Settings].

## [!UICONTROL Add Report Destinations] Sezione

**[!UICONTROL Destination Type]:** Scegliere uno dei seguenti tipi di destinazione:

* *[!UICONTROL S3]:* Per inviare il rapporto completato a uno o più [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3]), che verranno specificate nella **[!UICONTROL Destination Name]** campo .
* *[!UICONTROL sFTP]:* Per inviare il rapporto completato a una o più posizioni SFTP, specificate nella **[!UICONTROL Destination Name]** campo .
* *[!UICONTROL FTP]:* Per inviare il rapporto completato a una o più posizioni FTP, specificate nella **[!UICONTROL Destination Name]** campo .
* *[!UICONTROL FTP SSL](attualmente in versione beta):* Per inviare il rapporto completato a una o più posizioni SSL FTP, specificate nella **[!UICONTROL Destination Name]** campo .
* *[!UICONTROL Email]:* Specifica degli indirizzi e-mail a cui inviare i rapporti o le notifiche completati se il rapporto viene annullato a causa di errori. Per specificare più indirizzi, separali con virgole o spazi.

>[!NOTE]
>
> Non è possibile modificare il tipo di destinazione una volta salvato il rapporto.

**[!UICONTROL Destination Name]:** (Solo tipi di destinazione SSL S3, FTP, sFTP e FTP) I nomi delle destinazioni del rapporto a cui verrà inviato il rapporto personalizzato.

* Per specificare una destinazione esistente, selezionarne uno dall’elenco. È possibile selezionare separatamente più nomi di destinazione.

* Per creare una nuova destinazione:

   1. Fai clic su **Aggiungi nuova destinazione**.

   1. Inserisci il [impostazioni di destinazione del report](/help/dsp/reports/report-destinations/report-destination-settings.md)e fai clic su **Salva**.

   1. Nelle impostazioni del rapporto, fai clic su **Aggiorna nomi di destinazione.**

      La nuova destinazione è ora disponibile dall’elenco delle destinazioni esistenti ed è possibile aggiungerla facoltativamente al rapporto.

**[!UICONTROL Frequency]:** (Per ciascuno [!UICONTROL Destination Name] Con quale frequenza inviare il rapporto alla destinazione: *[!UICONTROL Once]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]* oppure *[!UICONTROL Monthly]*.

## [!UICONTROL Save Report] Sezione

**[!UICONTROL Send & Save]:** Quando inviare il rapporto: *[!UICONTROL On Schedule]* o *[!UICONTROL Run Now]*. I rapporti pianificati verranno consegnati entro le 09:00 nel fuso orario dell’account.

>[!NOTE]
>
>È possibile [eseguire un rapporto personalizzato in qualsiasi momento](report-run-now.md) dal [!UICONTROL Reports] visualizza.

>[!MORELIKETHIS]
>
>* [Informazioni sui report personalizzati](/help/dsp/reports/report-about.md)
>* [Creare un rapporto personalizzato](/help/dsp/reports/report-create.md)
>* [Duplicare un rapporto personalizzato](/help/dsp/reports/report-copy.md)
>* [Modificare un rapporto personalizzato](/help/dsp/reports/report-edit.md)
>* [Eseguire un rapporto personalizzato](/help/dsp/reports/report-run-now.md)
>* [Impostazioni report personalizzate](/help/dsp/reports/report-settings.md)
>* [Informazioni sulle destinazioni dei rapporti](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [Colonne dei rapporti disponibili](/help/dsp/reports/report-columns.md)

