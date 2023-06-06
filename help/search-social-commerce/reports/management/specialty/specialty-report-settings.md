---
title: Impostazioni report speciali
description: Scopri le impostazioni obbligatorie e facoltative per i rapporti speciali.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '2995'
ht-degree: 0%

---

# Impostazioni report speciali

| Linguetta | Parametro | Descrizione |
|----|----|----|
| n/d | [!UICONTROL Name] | (Facoltativo) Un nome per il rapporto e per il modello (se si salva il rapporto come modello). Se si applica un modello esistente, il nome del modello viene compilato per impostazione predefinita. Se non si applica un modello o non si immette un nome, il report viene denominato `<client name>-<date and time>-<report type>` (come &quot;acme - 3 aprile 2009 11:25:19 AM PDT - Parola chiave&quot;).<br><br>Facoltativamente, puoi immettere un nome personalizzato, ma non utilizzare un’estensione di file.<br><br>Se stai creando un modello per [inviare rapporti a una directory FTP](/help/search-social-commerce/reports/automation/ftp-reports.md), è quindi possibile includere &quot;CSV&quot; (in lettere maiuscole) in qualsiasi punto del nome del file per creare i file in formato CSV, anziché in formato TSV predefinito. Consulta [requisiti del nome file per i rapporti inviati a una directory FTP](/help/search-social-commerce/reports/automation/ftp-reports.md). |
|  | [!UICONTROL Save as template] | (Facoltativo a meno che non si desideri eseguire il report in base a una pianificazione) Salva le impostazioni del report come modello, disponibile nella [!UICONTROL Reports] > [!UICONTROL Report Templates] e possono essere riutilizzati per creare nuovi rapporti. Per salvare il report come modello, selezionare la casella di controllo.<br><br>Per eseguire il rapporto in base a una pianificazione, è necessario salvare le impostazioni come modello.<br><br><b>Nota:</b> È possibile salvare il set di parametri corrente come nuovo modello anche se è basato su un modello esistente. |
|  | [!UICONTROL Type] | Tipo di report da generare. |
| [!UICONTROL Basic  Settings] | [!UICONTROL Template] | (Facoltativo) Un modello di rapporto da applicare, che precompila le opzioni del rapporto in base al modello. Vengono elencati tutti i modelli salvati per il tipo di report e disponibili.<br><br>Se si seleziona un modello, è comunque possibile modificare le opzioni del rapporto e salvare il rapporto come nuovo modello. |
|  | [!UICONTROL Data Aggregation] | ([!UICONTROL Forecast Accuracy Report only]) L&#39;unità di tempo che deve essere rappresentata su ogni riga del report: <i>[!UICONTROL Summary (the default)]</i>, <i>[!UICONTROL Daily]</i>, <i>[!UICONTROL Weekly]</i> (e poi specifica il primo giorno della settimana), <i>[!UICONTROL Monthly]</i>, <i>[!UICONTROL Quarterly]</i>, <i>[!UICONTROL Yearly]</i>, o <i>[!UICONTROL Day of Week]</i> (solo rapporti di base).<br><br>Il rapporto mostra una riga per ogni parola chiave o altro elemento per ogni unità di tempo nell’intervallo di date specificato. Ad esempio, se selezioni <i>[!UICONTROL Summary]</i> e un intervallo di date di <i>[!UICONTROL Last 7 Days]</i> per un rapporto di parole chiave, il rapporto include una riga per ogni parola chiave, ciascuna delle quali riepiloga i totali e le medie nei sette giorni. Lo stesso rapporto con <i>[!UICONTROL Daily]</i> l’aggregazione dei dati include una riga per ogni parola chiave per ciascuno degli ultimi sette giorni (sette righe per parola chiave).<br><br><b>Note:</b><ul><li>Quando aggreghi i dati su base oraria utilizzando il tasto &quot;[!UICONTROL Hourly]&quot; o &quot;[!UICONTROL Day of Week (Hourly)]&quot; aggregazione:</li><ul><li>Puoi visualizzare fino agli ultimi 14 giorni di dati. Il rapporto mostra i dati per ora in un orologio da 24 ore. &quot;[!UICONTROL 0]&quot; include 00:01-00:59 (12):01-12:59.00) e &quot;[!UICONTROL 23]&quot; include 23:01-23:59 (11):01-11:59) nel fuso orario dell&#39;inserzionista.</li><li>La &quot;[!UICONTROL Device]La colonna &quot; non è supportata.</li><li>Per [!UICONTROL Ad Group Report], il &quot;[!UICONTROL Data Based On]&quot;opzione&quot;[!UICONTROL Portfolio Configuration During the Specified Dates]&quot; non è supportato.</li><li>Per [!UICONTROL Ad Group Report], è possibile basare i dati orari solo sulla configurazione del portfolio corrente (utilizzando il tasto &quot;[!UICONTROL Data Based On]&quot;opzione&quot;[!UICONTROL Current Portfolio Configuration]&quot;), non la configurazione del portfolio nelle date specificate.</li></ul></ul> |
|  | [!UICONTROL Conversions Based on] | ([!UICONTROL AdWords Shopping Performance Report], [!UICONTROL Campaign Daily Impression Share Report], e [!UICONTROL Keyword Daily Impression Share Report] Solo per ) Come segnalare i dati di conversione:<ul><li><i>[!UICONTROL Transaction date]</i> (impostazione predefinita): consente di visualizzare le transazioni la cui data di transazione si è verificata nel periodo di tempo specificato. Questa opzione mostra l’importo dei ricavi ottenuti nel periodo di tempo specificato.</li><li><i>[!UICONTROL Click date]:</i> Per visualizzare le transazioni risultanti da un clic nel periodo di tempo specificato. Quando un portfolio presenta un ritardo significativo tra clic e transazioni, questa opzione è utile per calcolare il ricavo storico per clic per il portfolio, che indica i comportamenti di ricavo da prevedere nel tempo.</li></ul> |
|  | [!UICONTROL Date Range] | L’intervallo di date per il quale generare i dati:<ul><li><i>[Intervallo predefinito]:</i> Elenco di incrementi di tempo comuni, compresi <i>[!UICONTROL Today]</i> a <i>[!UICONTROL Last 180 Days]</i>. Il valore predefinito è <i>[!UICONTROL Last 7 Days]</i>, che riporta gli ultimi sette giorni per i quali i dati sono disponibili. <b>Nota:</b> <i>[!UICONTROL Last Month]</i>, <i>[!UICONTROL Last 3 Months]</i>, e <i>[!UICONTROL Last 6 Months]</i> mostra i dati per i mesi di calendario precedenti.</li><li><i>[!UICONTROL Custom Date Range]:</i> Specifica la data di inizio e la data di fine. Immettere le date nel formato MM/GG/AAAA o M/G/AAAA oppure fare clic su ![Calendario](/help/search-social-commerce/assets/calendar.png "Calendario") accanto a un campo e seleziona una data.</li></ul> |
|  | [!UICONTROL Compare With] | Confronta i dati per l’intervallo di date specificato con i dati per un secondo intervallo di date. Quando selezioni questa opzione, vengono aggiunte due colonne aggiuntive per ogni colonna di dati regolare. Ad esempio, invece di includere una sola colonna per &quot;Impression&quot;, il rapporto include colonne per &quot;[!UICONTROL Impressions Range 1],&quot; &quot;[!UICONTROL Impressions Range 2],&quot; e &quot;[!UICONTROL Impressions Difference].&quot;<br><br><b>Note:</b><ul><li>La colonna delle differenze non viene visualizzata per le metriche personalizzate/derivate.</li><li>La generazione di rapporti che confrontano intervalli di date di grandi dimensioni richiede più tempo.</li></ul> |
|  | [!UICONTROL Show Comparison Data as] | (Quando &quot;[!UICONTROL Compare With]&quot; è selezionato) Come esprimere la differenza tra i dati nei due intervalli di date selezionati nel &quot;[Campo dati] [!UICONTROL Difference]Colonna &quot;:<ul><li><i>[!UICONTROL Variance]</i> (impostazione predefinita): mostra la differenza come valore numerico.</li><li><i>[!UICONTROL % Change]:</i> Mostra la differenza come percentuale.</li></ul> |
|  | [!UICONTROL Filter By] | ([!UICONTROL RSA Asset Report], [!UICONTROL Campaign Daily Impression Share Report], e [!UICONTROL Keyword Daily Impression Share Report] solo) Se segnalare i dati per portfolio specifici o per reti di annunci specifiche:<ul><li><i>[!UICONTROL Portfolio]</i> (impostazione predefinita): per includere i dati per le campagne in uno o più portfolio.</li><li><i>[!UICONTROL Search Engine]:</i> Per includere i dati per le campagne in una o più reti di annunci, in base al tipo di rapporto. |
|  | \[Filtri primari\] | I componenti dati da includere. Se non effettui una selezione, i dati per tutti i portfolio (se applicabile) o per tutte le reti pubblicitarie applicabili e i relativi sottocomponenti vengono inclusi nel rapporto. Facoltativamente, puoi limitare i dati da segnalare specificando singoli componenti e sottocomponenti. A seconda del tipo di rapporto e (se applicabile) del fatto che si stia filtrando per portfolio o rete di annunci, indica i componenti da includere:<ul><li><i>[!UICONTROL Portfolio]:</i> Uno o più portfolio o relativi sottocomponenti (campagne o gruppi di annunci). Per selezionare un componente e tutti i relativi sottocomponenti, selezionare la casella di controllo accanto al nome del componente. Per selezionare un sottocomponente, seleziona la casella di controllo accanto al nome del sottocomponente, quindi fai clic su >> per spostarlo nel [!UICONTROL Selected Filters] colonna. Ad esempio, per ottenere i dati per il Portfolio 1 e tutte le relative campagne e gruppi di annunci, seleziona la casella di controllo accanto al Portfolio 1. Per ottenere i dati quando si è verificato almeno un evento nella campagna 1 del Portfolio 1, espandi il Portfolio 1 e seleziona solo la casella di controllo accanto a Campagna 1.</li><li><i>[!UICONTROL Search Engine]:</i> Una o più reti di annunci o i relativi sottocomponenti (account, campagne o gruppi di annunci). Per selezionare un componente e tutti i suoi sottocomponenti, seleziona la casella di controllo accanto al nome del componente, quindi fai clic su >> per spostarlo in [!UICONTROL Selected Filters] colonna. Per selezionare un sottocomponente, seleziona la casella di controllo accanto al nome del sottocomponente, quindi fai clic su >> per spostarlo nel [!UICONTROL Selected Filters] colonna. Ad esempio, per ottenere dati quando si è verificato almeno un evento in una [!DNL Google Ads] account, campagna e gruppo di annunci, seleziona la casella accanto a [!DNL Google AdWords]. Per ottenere i dati solo per la campagna 1 in [!DNL Google Ads] Account 1, espandi [!DNL Google Ads] quindi Account 1 e selezionare solo la casella di controllo accanto a Campaign 1.</li></ul><b>Note:</b><ul><li>Per espandere un componente nell’elenco (ad esempio, per elencare gli account su una rete di annunci), fai clic su ![icona freccia destra](/help/search-social-commerce/assets/compressed-item.png "icona freccia destra") accanto al componente.</li><li>Per visualizzare il tipo di componente di un elemento, posizionare il cursore su di esso.</li><li>Per impostazione predefinita, sono elencati solo a) i portfolio attivi e ottimizzati e i relativi componenti attivi o b) gli account di rete, le campagne e i relativi componenti attivi attivi e attivi. Per visualizzare i componenti in pausa ed eliminati, fai clic su ![freccia giù](/help/search-social-commerce/assets/arrow-down-expand.png "freccia giù") accanto a **[!UICONTROL Show]** e seleziona **[!UICONTROL All]**.</li><li>Quando generi un rapporto avanzato per portfolio, i dati risultanti sono per le campagne attualmente mappate sui portfolio specificati. Il rapporto non include i dati per le campagne presenti nei portfolio durante l’intervallo di date, ma che non sono ancora presenti.</li></ul> |
| [!UICONTROL Columns] | \[Colonne report\] | Le colonne di dati visualizzate nel rapporto e il loro ordine:<ul><li>Per aggiungere una colonna, fai clic sul nome della metrica nella colonna a sinistra, quindi fai clic su ![Freccia destra](/help/search-social-commerce/assets/arrow-right-customize.png "Freccia destra").</li><li>Per rimuovere una colonna, fai clic sul nome della metrica nella colonna di destra, quindi fai clic su ![Freccia sinistra](/help/search-social-commerce/assets/arrow-left-customize.png "Freccia sinistra").</li><li>Per spostare una colonna a sinistra all’interno del rapporto, fai clic sul nome della metrica nella colonna di destra, quindi fai clic su ![Freccia su](/help/search-social-commerce/assets/arrow-up-customize.png "Freccia su").</li><li>Per spostare una colonna a destra all’interno del rapporto, fai clic sul nome della metrica nella colonna di destra, quindi fai clic su ![Freccia giù](/help/search-social-commerce/assets/arrow-down-customize.png "Freccia giù").</li></ul><b>Note:</b><ul><li>Per elencare solo un tipo specifico di dati, fare clic su una delle icone sopra l&#39;elenco:<ul><li>![Proprietà](/help/search-social-commerce/assets/property-columns.png "Proprietà") per nomi di proprietà e ID per componenti di portfolio o account di ad network, ad esempio [!UICONTROL Campaign Status]&lt;.li<li>![Metriche traffico](/help/search-social-commerce/assets//traffic-metric-columns.png "Metriche traffico") per le metriche di traffico standard, come impression e clic</li><li>![Metriche dei ricavi](/help/search-social-commerce/assets/revenue-metric-columns.png "Metriche dei ricavi") per le metriche di ricavo/proprietà di transazione tracciate per l’inserzionista, comprese le metriche di conversione e di coinvolgimento del sito sincronizzate da Adobe Analytics</li><li>![Metriche derivate](/help/search-social-commerce/assets/derived-metric-columns.png "Metriche derivate") per le metriche derivate personalizzate create dall’inserzionista</li><li>![Classificazioni etichette](/help/search-social-commerce/assets/label-classification-columns.png "Classificazioni etichette") solo per le classificazioni delle etichette nei rapporti Campagna, Gruppo di annunci, Variazione annuncio, Parola chiave e Gruppo di prodotti</li></ul></li></li><li>Per impostazione predefinita, tutti i dati monetari nei rapporti vengono visualizzati nel formato del dollaro statunitense (ad esempio 1.000,00). Per visualizzare il valore nel formato di valuta corretto (ma senza simboli di valuta nei formati CSV e TSV), aggiungi &quot;[!UICONTROL Currency]&quot; al rapporto. Se il rapporto include dati per conti con valute diverse, qualsiasi &quot;[!UICONTROL Total]&quot;i valori monetari sono semplicemente la somma di tutti i numeri nella colonna, indipendentemente dalla valuta.</li><li>La generazione di rapporti che includono molte proprietà di transazione o metriche derivate personalizzate che includono molte proprietà di transazione può richiedere più tempo.</li><li>Per aggiungere, creare o modificare nuove metriche, vedi &quot;[Creare una metrica personalizzata](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-create.md),&quot; &quot;[Modificare una metrica personalizzata](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-edit.md),&quot; e &quot;[Eliminare una metrica personalizzata](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-delete.md).&quot;</li><li>Per una descrizione di tutte le colonne disponibili, vedi &quot;[Colonne report di base e avanzate](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-columns.md).&quot;</li></ul> |
|  | [!UICONTROL Order Results/Limit Rows by] | Ordina il report in base a un massimo di due colonne incluse nel report. I valori predefiniti sono diversi per ogni tipo di rapporto. Per personalizzare l&#39;ordinamento, selezionare una colonna di report, quindi selezionare <i>[!UICONTROL Ascending]</i> (per visualizzare i risultati da A a Z o da 1 a 100) o <i>[!UICONTROL Descending]</i> (per visualizzare i risultati da Z ad A o da 100 a 1). Specificare almeno una colonna in base alla quale eseguire l&#39;ordinamento. Se si ordina in base a due colonne, il rapporto viene ordinato prima in base alla prima colonna specificata e quindi in base alla seconda colonna specificata. |
|  | [!UICONTROL Include assets with no performance data, except for assets with zero lifetime data] | ([!UICONTROL RSA Asset Report only]) Include le righe per le quali non sono disponibili dati sulle prestazioni per le date specificate, inserendo valori pari a zero (0) per i dati mancanti. Per impostazione predefinita, questa opzione non è selezionata e le righe vengono visualizzate solo quando i dati (qualsiasi sia il valore) sono disponibili.<br><br>Quando questa opzione è selezionata, i rapporti includono dati sulle prestazioni per account di rete di annunci senza campagne e per campagne senza parole chiave attive, nonché per componenti disabilitati, messi in pausa ed eliminati durante l’intero intervallo di dati. Inoltre, il rapporto RSA Asset (RSA Asset Report) mostra le righe per tutte le risorse, ad eccezione di quelle con dati a vita pari a zero.<br><br><b>Avvertenza:</b> Se selezioni questa opzione e crei un rapporto per un intervallo di date ampio per molti sottocomponenti che non hanno dati, la generazione del rapporto potrebbe richiedere molto tempo. |
|  | [!UICONTROL Share with others] | Consente ad altri utenti con accesso ai dati dello stesso inserzionista di visualizzare i report generati e, se si salva il report come modello, di utilizzare il modello senza modificarlo o eliminarlo. Per impostazione predefinita, questa opzione non è selezionata. <b>Nota:</b> Indipendentemente da questa impostazione, i rapporti e i modelli sono sempre visibili a tutti gli utenti con ruoli superiori (amministratore) e a tutti i membri del Team account Adobi assegnati. |
| [!UICONTROL Advanced Filters] | \[Filtri avanzati\] | Restituisce le righe solo quando il valore di una metrica soddisfa i criteri specificati; non è necessario includere la metrica come colonna nel rapporto. L’elenco delle metriche disponibili varia in base al tipo di rapporto, ma può includere metriche derivate personalizzate per l’inserzionista, gli ID e i nomi delle proprietà per ogni rete di annunci e componente portfolio (ad esempio [!UICONTROL Campaign ID] e [!UICONTROL Campaign Status]), le metriche dei ricavi (proprietà della transazione) per l’inserzionista e le metriche relative ai clic provenienti dalle reti di annunci. Gli operatori disponibili includono <i>[!UICONTROL contains]</i>, <i>[!UICONTROL starts with]</i>, <i>[!UICONTROL equals]</i>, <i>[!UICONTROL is greater than]</i>, <i>[!UICONTROL is greater than or equal to]</i>, <i>[!UICONTROL is less than]</i>, <i>[!UICONTROL is less than or equal to]</i>, o <i>[!UICONTROL isn't equal to]</i>.<br><br>Per applicare uno o più filtri, effettuare le seguenti operazioni:<ul><li>Seleziona una metrica e un operatore, quindi inserisci il valore applicabile. Ad esempio, per restituire solo parole chiave con più di 100 clic, seleziona [!UICONTROL Clicks], seleziona [!UICONTROL >]e quindi immettere 100 nel campo di immissione.</li><li>(Per applicare altri filtri) Per ogni filtro aggiuntivo, fai clic su **[!UICONTROL +Add Filter]**, seleziona **[!UICONTROL AND]** o **[!UICONTROL OR]**, seleziona una metrica e un operatore, quindi inserisci il valore applicabile.</li></ul> |
| [!UICONTROL Attribution] | [!UICONTROL Rule] | (Solo per gli inserzionisti con il servizio di tracciamento delle conversioni basato su pixel di Adobe Advertising; [!UICONTROL AdWords Shopping Performance Report], [!UICONTROL Campaign Daily Impression Share Report], e [!UICONTROL Keyword Daily Impression Share Report] solo) ) All’interno del rapporto, come attribuire i dati di conversione mdash; potenzialmente su più canali di annunci e portfolio mdash; in una serie di eventi che portano a una conversione:<ul><li><i>[!UICONTROL First Event]:</i> Attribuisce la conversione al primo clic a pagamento della serie all’interno della [fai clic sull’intervallo di lookback](/help/search-social-commerce/glossary.md#c-d) o, se non si è verificato alcun clic a pagamento, all’ultima impression nel file dell’inserzionista [intervallo di lookback delle impression](/help/search-social-commerce/glossary.md#i-j).</li><li><i>[!UICONTROL Weight First Event More]:</i> Attribuisce la conversione a tutti gli eventi della serie che si sono verificati all&#39;interno del [fai clic sull’intervallo di lookback](/help/search-social-commerce/glossary.md#c-d) e [intervallo di lookback delle impression](/help/search-social-commerce/glossary.md#i-j), ma attribuisce il maggior peso al primo evento e successivamente meno peso ai seguenti eventi. Quando la conversione è preceduta sia da clic che da impression a pagamento, il peso di override delle impression specificato viene ulteriormente applicato alle impression. Quando la conversione è preceduta solo dalle impression, le impression vengono ponderate in base al peso view-through dell’inserzionista anziché al peso override dell’impression.</li><li><i>[!UICONTROL Even Distribution]:</li> Attribuisce la conversione in modo uniforme a ogni evento della serie in base al peso view-through dell&#39;inserzionista anziché al peso di override dell&#39;impression.</li><li><i>[!UICONTROL Weight Last Event More]:</i> Attribuisce la conversione a tutti gli eventi della serie che si sono verificati all&#39;interno del [fai clic sull’intervallo di lookback](/help/search-social-commerce/glossary.md#c-d) e [intervallo di lookback delle impression](/help/search-social-commerce/glossary.md#i-j), ma attribuisce il maggior peso all’ultimo evento e successivamente meno peso agli eventi precedenti. Quando la conversione è preceduta sia da clic che da impression a pagamento, il peso di override delle impression specificato viene ulteriormente applicato alle impression. Quando la conversione è preceduta solo dalle impression, le impression vengono ponderate in base al peso view-through dell’inserzionista anziché al peso override dell’impression.</li><li><i>[!UICONTROL Last Event]</i> (impostazione predefinita): attribuisce la conversione all’ultimo clic a pagamento della serie all’interno dell’inserzionista [fai clic sull’intervallo di lookback](/help/search-social-commerce/glossary.md#c-d) o, se non si è verificato alcun clic a pagamento, all’ultima impression nel file dell’inserzionista [intervallo di lookback delle impression](/help/search-social-commerce/glossary.md#i-j).</li><li><i>A U:</i> Attribuisce la conversione a tutti gli eventi della serie che si sono verificati all&#39;interno del [fai clic sull’intervallo di lookback](/help/search-social-commerce/glossary.md#c-d) e [intervallo di lookback delle impression](/help/search-social-commerce/glossary.md#i-j), ma attribuisce il maggior peso al primo evento e agli ultimi eventi, con un peso progressivamente inferiore agli eventi che si trovano nel mezzo del percorso di conversione. Quando la conversione è preceduta sia da clic che da impression a pagamento, il peso di override delle impression specificato viene ulteriormente applicato alle impression. Quando la conversione è preceduta solo dalle impression, le impression vengono ponderate in base al peso view-through dell’inserzionista anziché al peso override dell’impression.</li></ul><b>Note:</b><ul><li>Tutte le regole di attribuzione tranne [!UICONTROL Last Event] sono disponibili solo per gli inserzionisti con tracciamento dei clic di Adobe Advertising e con tracciamento delle conversioni da Adobe Advertising o Adobe Analytics (con un’integrazione Adobe Analytics).</li><li>Le regole di attribuzione si applicano alle impression sugli annunci display e ai clic sugli annunci a pagamento in qualsiasi canale. Non si applicano alle impression per ricerca a pagamento o annunci social, che non possono essere tracciate a livello di evento.</li><li>Quando riporti i dati di conversione utilizzando una regola di attribuzione diversa da una delle &quot;[!UICONTROL Last Event]&quot;, gli eventi che portano alla conversione possono verificarsi in più portfolio. Quando gli eventi si verificano in più portfolio, il rapporto include i dati per la conversione solo quando gli annunci o le parole chiave in tali portfolio sono inclusi nel rapporto.</li><li>([!UICONTROL Transaction Report]) Quando si segnalano le transazioni utilizzando qualsiasi regola di attribuzione eccetto &quot;[!UICONTROL Last Event]&quot; o &quot;[!UICONTROL First Event],&quot; il rapporto include una riga per ogni evento nel percorso della transazione.</li></ul> |
|  | [!UICONTROL Impression Override Weight] | (per tutte le regole di attribuzione tranne [!UICONTROL Last Event] o [!UICONTROL First Event]) Quando la conversione è preceduta sia da clic che da impression a pagamento, attribuisce la percentuale specificata di un valore di conversione alle impression che si sono verificate all’interno dell’inserzionista [intervallo di lookback delle impression](/help/search-social-commerce/glossary.md#i-j). Per impostazione predefinita, questo valore è 10%; è possibile modificare il valore in qualsiasi numero intero da 0 a 100. Questo valore viene utilizzato solo all’interno del rapporto.<br><br>Quando una conversione è preceduta solo da impression, l’operatore [ponderazione view-through](/help/search-social-commerce/glossary.md#u-v)Alle impression viene applicato il peso di override dell’impression, anziché il peso di override. |
|  | [!UICONTROL Conversion Attribution] | (Applicabile solo alle campagne di visualizzazione; [!UICONTROL AdWords Shopping Performance Report] solo) Quali tipi di conversioni segnalare quando si sono verificati eventi precedenti:<ul><li><i>[!UICONTROL Clicks]:</i> Per segnalare solo le conversioni risultanti da clic. A ogni nome di conversione viene aggiunto &quot;[!UICONTROL (CT)].&quot;</li><li><i>[!UICONTROL View-throughs Only]:</i> Per segnalare solo le conversioni risultanti da view-through. A ogni nome di conversione viene aggiunto &quot;[!UICONTROL (VT)].&quot; Quando selezioni questa opzione, scegli il valore da assegnare a ogni conversione. Nella casella Metodo di valutazione view-through selezionare un&#39;opzione:<ul><li><i>[!UICONTROL Raw]:</i> Per riportare le conversioni senza applicare un peso.</li>li><i>[!UICONTROL Weighted]</i> (impostazione predefinita): per ponderare ogni conversione in base al peso view-through specificato per l&#39;inserzionista.</li></ul></li><li><i>[!UICONTROL Clicks + View-throughs]:</i> Per segnalare tutte le conversioni. Per impostazione predefinita, a ogni nome di conversione viene aggiunto &quot;[!UICONTROL (CT+VT)].&quot; Questo tipo di attribuzione di conversione include due opzioni aggiuntive:<ul><li>[!UICONTROL Discreet columns for click & view-through conversions] — Include tre colonne separate per ogni tipo di conversione incluso: una per ogni 1) conversioni click-through, seguite da &quot;[!UICONTROL (CT)]&quot;, 2) conversioni view-through, seguite da &quot;[!UICONTROL (VT)]&quot;, 3) e tutte le conversioni, aggiunte con &quot;[!UICONTROL (CT+VT)].&quot; Quando scegli questa opzione, seleziona una delle tre colonne da utilizzare per filtrare e ordinare dal menu &quot;[!UICONTROL Filter & sort using]Elenco &quot;: <i>[!UICONTROL click]</i> (impostazione predefinita), <i>[!UICONTROL view-through]</i>, o <i>[!UICONTROL click + view-through]</i>.<br><br><b>Nota:</b> Le conversioni per le campagne di ricerca vengono visualizzate nelle colonne dei click-through, ma non nella colonna delle conversioni view-through.</li><li>[!UICONTROL View-through valuation method]: quale valore assegnare a ogni conversione derivante da una view-through:</li><ul><i>[!UICONTROL Weighted]</i> (impostazione predefinita): per ponderare ogni conversione in base al peso view-through specificato per l&#39;inserzionista.</li><li><i>[!UICONTROL Raw]:</i> Per riportare le conversioni senza applicare un peso.</li></ul></li></ul> |
|  | [!UICONTROL Conversion Attribution] > [!UICONTROL Discrete columns for cross device conversions] | Obsoleto |  |
| [!UICONTROL Scheduling and Delivery] | [!UICONTROL Report Schedule] | (Facoltativo; disponibile solo quando &quot;[!UICONTROL Save as template]&quot;) Quando eseguire il rapporto: <i>[!UICONTROL Now]</i> (per eseguire il report una sola volta; impostazione predefinita), <i>[!UICONTROL Daily]</i>, <i>[!UICONTROL Weekly on] [Giorno della settimana]</i>, o <i>[!UICONTROL Every Month] [Giorno del mese]</i>. Per tutti i periodi di tempo tranne <i>[!UICONTROL Now]</i>, seleziona l’ora nel fuso orario dell’inserzionista, a partire dalle 09:00. |
|  | [!UICONTROL Email Recipients] | <b>Nota:</b>  Questa impostazione viene utilizzata solo quando si inviano notifiche e-mail per [!UICONTROL Reports] sono [abilitato in [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-edit.md).<br><br>Indirizzi e-mail degli utenti registrati di Search, Social e Commerce a cui inviare notifiche quando il report viene completato o annullato a causa di errori. Per impostazione predefinita, viene immesso l’indirizzo dell’account utente. Per specificare più indirizzi, separali con virgole, spazi o nuove righe. Quando è pianificata l’esecuzione ripetuta del rapporto, viene inviata una notifica ogni volta che viene completato un rapporto. |
|  | [!UICONTROL Email Notification] | <b>Nota:</b>  Questa impostazione viene utilizzata solo quando si inviano notifiche e-mail per [!UICONTROL Reports] sono [abilitato in [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-edit.md).<br><br>(Quando [!UICONTROL Email Recipients] sono specificati) Cosa includere nelle notifiche e-mail a qualsiasi indirizzo specificato:<ul><li><i>[!UICONTROL Notification Only]</i> (impostazione predefinita): per inviare solo una notifica del completamento o dell&#39;errore del report, senza allegati. La notifica include collegamenti temporanei per il download di tutti i formati di rapporto.</li><li><i>[!UICONTROL XLS Attachment]:</i> Includere una copia del report completato in formato XLS se il file è inferiore a circa 10 MB. File superiori a 1 MB compressi.</li><li><i>[!UICONTROL TSV Attachment]:</i> Includere una copia del rapporto completato in formato TSV se il file è inferiore a circa 10 MB. File superiori a 1 MB compressi.</li><li><i>[!UICONTROL CSV Attachment]:</i> Includere una copia del rapporto completato in formato CSV se il file è inferiore a circa 10 MB. File superiori a 1 MB compressi. |

<table style="table-layout:auto">

>[!MORELIKETHIS]
>
>* [Informazioni sui report speciali](/help/search-social-commerce/reports/management/specialty/specialty-report-about.md)
>* [Generare un rapporto speciale](/help/search-social-commerce/reports/management/specialty/specialty-report-generate.md)
>* [Impostazioni report speciali](/help/search-social-commerce/reports/management/specialty/specialty-report-settings.md)
>* [Colonne report per report speciali](/help/search-social-commerce/reports/management/specialty/specialty-report-columns.md)
