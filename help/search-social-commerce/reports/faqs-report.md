---
title: Domande frequenti sui rapporti personalizzati
description: Scopri le risposte alle domande comuni sui rapporti sulle prestazioni, inclusa la risoluzione dei problemi relativi ai dati.
exl-id: 1232efce-25eb-48d8-a3fb-f57711fa14e5
feature: Search Reports
source-git-commit: 01fe9264fee43ed29f6cee022dadeb29fbd26f45
workflow-type: tm+mt
source-wordcount: '3922'
ht-degree: 0%

---

# Domande frequenti sui rapporti personalizzati

## Domande generali

+++Cosa succede se l’intervallo di date per il rapporto inizia prima che i dati del rapporto siano disponibili?
Il rapporto viene generato, ma include solo i dati per le date per le quali i dati sono disponibili. Per ulteriori informazioni sulla disponibilità dei dati per ogni tipo di report, vedere &quot;[I dati utilizzati per i report](data-used-for-reports.md).&quot;
+++

+++Qual è la differenza tra i rapporti basati sulla data di clic e quelli basati sulla data della transazione?
Quando si segnalano le conversioni per data transazione, i dati includono le transazioni la cui data transazione si è verificata durante il periodo di tempo specificato. Questa opzione è l’impostazione predefinita nei rapporti di base e nei rapporti avanzati e mostra l’importo dei ricavi ottenuti nel periodo di tempo specificato.

Quando si segnalano le conversioni per data di clic, i dati includono le transazioni risultanti da un clic che si è verificato durante il periodo di tempo specificato. Quando un portfolio presenta ritardi significativi tra clic e transazioni, questo tipo di reporting mostra i ricavi storici per clic per il portfolio, fornendo un’idea dei comportamenti di ricavo da prevedere nel tempo.

![Rapporto per data clic rispetto a rapporto per data transazione](/help/search-social-commerce/assets/click-date-vs-txn-date.png "Rapporto per data clic rispetto a rapporto per data transazione")
+++

+++Cosa succede se modifico l’intervallo di lookback su clic o l’intervallo di lookback su impression?
(Solo per gli inserzionisti con il servizio di tracciamento delle conversioni basato su pixel di Advertising) I dati per gli eventi risultanti dal clic iniziale vengono raccolti per un periodo più lungo o più breve.

L&#39;[intervallo di lookback su clic](/help/search-social-commerce/glossary.md#c-d) e l&#39;[intervallo di lookback su impression](/help/search-social-commerce/glossary.md#i-j) di un inserzionista determinano il numero di giorni dopo i quali si verifica un clic o un&#39;impression di visualizzazione (rispettivamente) in cui l&#39;evento può essere attribuito a una conversione. La modifica di un valore in un periodo più lungo o più breve può essere importante per gli inserzionisti con periodi di click-to-revenue o di impression-to-revenue particolarmente brevi o lunghi.

**Best practice:** assicurati che gli intervalli di lookback siano più lunghi dei tempi di click-to-revenue e di visualizzazione impression-to-revenue per la maggior parte delle parole chiave o degli annunci. Quando sono più brevi, alcune conversioni non sono associate al clic o all’impression iniziale.
+++

+++Come posso sapere quali conversioni sono risultate da un&#39;estensione pubblicitaria o da un elenco di prodotti di [!DNL Google Ads]?
Puoi vedere quali conversioni sono risultate da un clic su un&#39;estensione dell&#39;annuncio [!DNL Google Ads] (anziché sull&#39;annuncio stesso) o su un elenco di prodotti generando un [!UICONTROL Transaction Report]. Il valore della colonna [!UICONTROL Link Type] mostra il tipo e il titolo di un collegamento su cui è stato fatto clic:

* Gli elenchi prodotti sono elencati come `pla:<product ID>`, ad esempio `pla:8525822`.

* I sitelink sono elencati come `sl:<Sitelink text>`, ad esempio `sl:See Current Offers`.

  È inoltre possibile identificare un sitelink se si include la colonna [!UICONTROL Tracking URL] nel report. [!UICONTROL Tracking URL] per un sitelink include l&#39;attributo `&ev_ltx=sl:<link-name>`.

>[!NOTE]
>
>Le conversioni da [!DNL Google Ads] posizioni ed estensioni telefoniche sono incluse nei dati degli annunci che accompagnano. Non vengono segnalati separatamente.

+++

+++La colonna &quot;[!UICONTROL Keyword]&quot; nel report include un valore &quot;(contenuto adgroup) &lt;*nome gruppo annunci*>.&quot;
Quando la riga include dati per campagne di ricerca abilitate per il contenuto, campagne di visualizzazione o campagne social, che non includono parole chiave, la colonna [!UICONTROL Keyword] mostra invece il nome del gruppo di annunci applicabile.
+++

+++A causa di cambiamenti stagionali o di mercato, i miei rapporti mostrano dati atipici. Questo influisce sulle offerte una volta che le condizioni cambiano?
La funzionalità di ottimizzazione crea quotidianamente i propri modelli di ricavo per ogni unità di offerta per garantire che identifichi e risponda immediatamente alle tendenze, e i modelli incorporano dati storici a lungo termine per aiutare a prevedere le prestazioni stagionali. L&#39;impostazione di mezza durata del modello di ricavo del portfolio<!-- add link to glossary? --> determina anche la ponderazione dei dati recenti sui ricavi. La best practice prevede di ridurre l’emivita durante un periodo di prestazioni atipiche, ma di aumentarla dopo l’adeguamento del modello di ricavo. Se hai domande sulla necessità di regolare l’emivita, contatta il team del tuo account Adobe.

Se non desideri che i dati del periodo influiscano sulle offerte future, puoi scegliere di escludere tali date dal modello. Contatta il team del tuo account Adobe per escludere le date.
+++

+++Posso creare un report su una metrica di proprietà account specifica, ad esempio [!UICONTROL Device] o [!UICONTROL Objective Name]?
Per i report di entità campagna ([!UICONTROL Campaign Report], [!UICONTROL Ad Group Report], [!UICONTROL Ad Variation Report], [!UICONTROL Keyword Report] e [!UICONTROL Product Group Report]), i dati delle metriche vengono aggregati dinamicamente dalle colonne di proprietà incluse nel report. Facoltativamente, è possibile rimuovere la colonna chiave per il rapporto e includere solo le colonne di proprietà per le quali si desidera aggregare i dati.

Ad esempio, se si genera un [!UICONTROL Keyword Report] che include le colonne Dispositivo [!UICONTROL Ad Group] e , per impostazione predefinita il report aggrega le metriche per ogni parola chiave in base al gruppo di annunci e al tipo di dispositivo. Tuttavia, se rimuovi la colonna [!UICONTROL Keyword] prima di generare il rapporto, questo genera dinamicamente le metriche per i gruppi di annunci specificati per tipo di dispositivo.

>[!NOTE]
>
>Non puoi utilizzare questa funzione per aggregare i dati in base alle classificazioni delle etichette. Eventuali colonne di classificazione delle etichette nel rapporto vengono omesse. Utilizzare invece il [report di classificazione etichette](/help/search-social-commerce/reports/management/basic-advanced/label-classification-report.md).

+++

## Problemi generali relativi ai dati

+++I rapporti generati utilizzando regole di attribuzione diverse mostrano totali diversi.
Se generi un rapporto più volte utilizzando gli stessi parametri di rapporto ma con regole di attribuzione diverse, i dati possono differire per uno dei seguenti motivi:

* I dati basati su date su clic potrebbero non rientrare nell’intervallo di date specificato.

  Se si utilizza il parametro di report &quot;[!UICONTROL Conversions based on click date]&quot;, l&#39;intervallo di date specificato viene applicato alla data del clic anziché alla data della transazione. Se il rapporto utilizza anche la regola di attribuzione &quot;Primo evento&quot; o &quot;Ultimo evento&quot;, il primo o l’ultimo evento che ha portato alla conversione potrebbe non rientrare nell’intervallo di date specificato. Ad esempio, si supponga che un utente abbia fatto clic su Parola chiave_1 il 30 aprile, su Parola chiave_2 il 20 maggio e abbia effettuato la conversione il 21 maggio. Se il report utilizza la regola di attribuzione &quot;[!UICONTROL First Event]&quot; e un intervallo di date compreso tra l&#39;1 e il 21 maggio, il primo evento (un clic su Keyword_1 il 30 aprile) non verrà incluso nel report. Se si esegue il report con lo stesso intervallo di date ma si utilizza la regola di attribuzione &quot;[!UICONTROL Last Event]&quot;, la conversione viene inclusa nel report perché l&#39;ultimo clic si è verificato all&#39;interno dell&#39;intervallo di date specificato.

* La selezione del filtro portfolio esclude alcuni degli eventi che portano alla conversione.

  Se esegui un rapporto su un sottoinsieme di portfolio, è possibile che non includa le campagne che includevano l’evento a cui è stata attribuita la conversione in una delle regole di attribuzione. Si supponga, ad esempio, che un utente faccia clic su Parola chiave_1 da Portfolio_1, su Parola chiave_2 da Portfolio_2 e quindi esegua la conversione. Se il report utilizza la regola di attribuzione &quot;[!UICONTROL First Event]&quot;, è necessario includere Portfolio_1 affinché la conversione possa essere inclusa nel report. Tuttavia, se il rapporto utilizza la regola di attribuzione &quot;Last Event&quot; (Ultimo evento), deve essere incluso Portfolio_2.

>[!TIP]
>
>Se si desidera confrontare i totali di conversione in diverse regole di attribuzione, eseguire i report utilizzando il parametro di report &quot;[!UICONTROL Conversions based on transaction date]&quot; e selezionare tutte le reti di annunci o tutti i portfolio. Se non imposti altri filtri, i totali di conversione devono corrispondere.

+++

+++I singoli campi dati non sono corretti, anche se i totali sono corretti.
Questa situazione può verificarsi quando i formati della metrica utilizzano numeri interi:

* Se si crea una [metrica personalizzata](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-about.md) con il formato *Numero con punti decimali* (che mostra i dati come numeri interi) e li si include in una visualizzazione o in un report che utilizza una regola di attribuzione di conversione ponderata ([!UICONTROL Weight First Event More], [!UICONTROL Weight Last Event More] o [!UICONTROL Even Distribution]), l&#39;output verrà visualizzato in numeri interi e non in decimali. In questo caso, i singoli campi dati potrebbero essere errati, anche se i totali sono corretti. Ad esempio, se un ordine è diviso in modo uniforme tra tre eventi, a ciascuno di essi viene attribuito un ordine (anziché 0,33). Per risolvere il problema, [modifica il formato della metrica](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-edit.md) in *Numero con 2 punti decimali*.

* Analogamente, se disponi di una metrica di ricavo inviata come numero intero, si verifica lo stesso problema. Il formato dei ricavi è controllato dal tag di conversione che invia i dati. Per risolvere il problema, [crea una metrica personalizzata](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-create.md) costituita esclusivamente dalla metrica Ricavi e con il formato *Numero a 2 punti decimali* e includila nelle visualizzazioni e nei report anziché nella metrica originale.
+++

+++Quando mancano i dati di clic o i ricavi, come posso evitare che influiscano sulle offerte future?
Si verificano problemi di dati di clic quando Search, Social e Commerce non sono sincronizzati con la rete di annunci. Contatta il team del tuo account Adobe per sincronizzare manualmente l’account. Se mancano i dati di clic per un’intera giornata, chiedi al team del tuo account Adobe di escludere tale giorno dai modelli di costo.

I problemi relativi ai dati dei ricavi possono verificarsi a causa di un problema di tracciamento o di un file di feed. Contatta il team del tuo account Adobe per indagare sul problema. Se mancano dati sui ricavi per un giorno intero, chiedi al team del tuo account Adobe di escludere tale giorno dai modelli di ricavi.
+++

+++I dati monetari sono visualizzati in un formato errato.
Per impostazione predefinita, tutti i dati monetari nei rapporti vengono visualizzati nel formato del dollaro statunitense (ad esempio 1.000,00). Per visualizzare il valore nel formato di valuta corretto (ma senza simboli di valuta nei formati CSV e TSV), aggiungere la colonna &quot;[!UICONTROL Currency]&quot; al rapporto. Se il report include dati per conti con valute diverse, tutti i valori monetari &quot;[!UICONTROL Total]&quot; sono semplicemente la somma di tutti i numeri nella colonna, indipendentemente dalla valuta.
+++

+++Perché trovo valori decimali per una metrica di conversione che deve essere un numero naturale (1, 2 e così via)?
È possibile che vengano visualizzati valori decimali nei seguenti casi:

* Se il report è stato eseguito utilizzando un parametro della regola di attribuzione di conversione diverso da [!UICONTROL Last Event] o [!UICONTROL First Event], i ricavi possono essere suddivisi tra più eventi nel percorso di conversione.

* In [!UICONTROL Transaction Report], se più unità di [offerta](/help/search-social-commerce/glossary.md#a-b) con tipi di corrispondenza diversi hanno lo stesso ID transazione, i ricavi per l&#39;ID di tracciamento vengono suddivisi in base al numero di clic nella data di clic specificata.
+++

## Metriche delle prestazioni standard

+++Mancano dati di clic nei rapporti.
Di seguito sono riportati i motivi comuni della mancanza di dati di clic.

| Causa | Rilevamento/analisi | Risoluzione |
|---|---|---|
| Il processo che recupera i dati di clic dall’account dell’annuncio non è riuscito. | Non esiste un modo sistematico per rilevare questo problema, ma puoi notare che una campagna non mostra informazioni sui costi o sui clic, anche se l’account dell’annuncio ha speso denaro. | Contatta il team del tuo account Adobe.<br><br>Se i dati mancano per più di 24 ore, escludere tali date dalle previsioni di costo fino al recupero dei dati. Il team del tuo account Adobe può escludere le date. |
| Un problema di fatturazione tra l’inserzionista e la rete di annunci impedisce all’account dell’annuncio di spendere. | Non esiste un modo sistematico per rilevare questo problema, ma potresti notare che una campagna non mostra alcun costo o informazioni sui clic. | Se sai che un account dell’annuncio non è stato in grado di spendere a causa di un problema di fatturazione, escludi tali date dalle previsioni di costo. Il team del tuo account Adobe può escludere le date. |

+++

+++I dati sulle prestazioni sono diversi dai dati nell’editor della rete di annunci.
Quando la rete di annunci invia aggiornamenti ai dati precedenti (spesso perché hanno attribuito la frode dei clic ad alcuni clic), Search, Social e Commerce non aggiornano i dati a meno che non vi sia una discrepanza superiore al 5% e l’Account Team di Adobe non file una richiesta.

Inoltre, quando confronti i dati di condivisione delle impression aggregati in un intervallo di date, i dati riportati dai rapporti di Search, Social e Commerce possono differire da quelli riportati dalla rete di annunci. Questa differenza è dovuta al modo in cui i dati vengono segnalati dall’API dell’ad network, utilizzata da Search, Social e Commerce per richiamare i dati. Ad esempio, per i dati [!DNL Google Ads]:

* Per la maggior parte delle metriche di condivisione delle impression, [!DNL Google Ads] limita il limite minimo o massimo dei valori segnalati per valori inferiori al 10% o superiori al 90%. I dati sono riportati come 0,0999 per &lt;10% e 0,9001 per >90%

* In presenza di una combinazione di dati con e senza limiti di tempo all’interno dell’intervallo di date, Search, Social e Commerce aggregano i dati delle impression utilizzando i valori inviati nell’API così com’è, utilizzando 0,0999 per le righe con &lt;10% e 0,9001 per le righe con >90%. Questa aggregazione potrebbe causare una varianza dai dati preaggregati [!DNL Google Ads] perché [!DNL Google Ads] può utilizzare valori percentuali effettivi, ad esempio 7% o 97%.
+++

+++I dati delle prestazioni nei report sono diversi dai dati in [!DNL Google Analytics].
I due sistemi misurano dati diversi, pertanto è necessario che visualizzino dati diversi. Ad esempio:

* Search, Social e Commerce (e Google Ads) tengono traccia dei clic, mentre [!DNL Google Analytics] tiene traccia delle visite per sessione di 30 minuti del browser. Ad esempio, se un utente fa clic una volta sull&#39;annuncio, fa clic sul pulsante Indietro e quindi fa di nuovo clic sull&#39;annuncio, in Search, Social &amp; Commerce vengono registrati due clic, ma [!DNL Google Analytics] registra una visita.

* [!DNL Google Analytics] mostra tutti i dati sul traffico, mentre Search, Social e Commerce (e [!DNL Google Ads]) filtra i clic non validi (ad esempio i clic eccessivi e ripetuti).

* [!DNL Google Analytics] include i dati dei clic e dei ricavi per tutti i clic. Search, Social e Commerce non possono tenere traccia dei dati dei clic e dei ricavi per annunci e parole chiave con URL di tracciamento errati o mancanti.
+++

## Metriche di conversione

+++Il mio rapporto non mostra dati di conversione.
Il rapporto potrebbe non includere le metriche di conversione per le quali si sono verificate conversioni.
+++

+++Nei rapporti manca la retribuzione.

**Inserzionisti che utilizzano i tag di conversione di Adobe Advertising**

*Possibili cause:*

* Parole chiave o annunci sono stati aggiunti senza prefisso ai modelli di tracciamento o agli URL di destinazione il prefisso di tracciamento dei clic Search, Social e Commerce oppure il prefisso di tracciamento non è corretto.

* Il tag di tracciamento della conversione non è implementato correttamente in tutte le pagine web applicabili o è stato modificato.

* Le metriche di conversione tracciate da Search, Social e Commerce sono escluse dai rapporti e non sono quindi visibili.

* Il parser dei ricavi per il client non è stato implementato.

*Soluzione o soluzione alternativa possibile:*

1. Verifica che nei rapporti o nelle visualizzazioni dati siano incluse le colonne corrette. Se non sono disponibili le colonne corrette da aggiungere, tu o il tuo Adobe Account Team dovete [rendere le metriche di conversione disponibili per i report](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-available.md).

1. Verifica che i tag di tracciamento della conversione corretti siano implementati in tutte le pagine web applicabili. Se necessario, chiedi al tuo account team Adobe di creare una transazione di prova per ogni tag di tracciamento delle conversioni applicabile e di acquisire i dettagli della transazione, ad esempio `transactionid` e i dettagli dal cookie (ad esempio `trackingid`, `clickid` e così via).

1. Se l&#39;opzione [!UICONTROL Auto Upload] è disabilitata per la campagna e sono state aggiunte parole chiave o annunci, assicurati di aver generato un modello di tracciamento o un URL di destinazione che includa il tracciamento dei clic di ricerca, social e Commerce per ciascuno di essi. Il team dell’account Adobe può eseguire un rapporto interno per verificare se gli URL di tracciamento dei clic (modelli di tracciamento o URL di destinazione) sono mancanti o non validi.

   Se necessario, genera il tracciamento creando un file bulksheet con gli URL corretti e inserisci il file nell&#39;account appropriato utilizzando l&#39;opzione **Genera URL di tracciamento**.

   L&#39;URL di destinazione deve iniziare con &quot;http://pixel.everesttech.net&quot; o &quot;https://pixel.everesttech.net&quot;.

1. Se nessuno di questi passaggi risolve il problema, [contatta l&#39;Assistenza clienti](/help/search-social-commerce/get-help.md).

   Se il cliente non è stato avviato o è appena stato avviato, l’Assistenza clienti verifica se è stato configurato un parser di ricavi. Se il parser è configurato, verifica se Search, Social e Commerce ricevono conversioni di pixel e risolve il problema.

**Inserzionisti che inviano feed di dati di conversione**

*Possibili cause:*

* Il file di feed non è stato consegnato, non è stato analizzato completamente o il feed conteneva transazioni orfane.

* Le metriche di conversione pertinenti sono escluse dai rapporti e quindi non visibili.

>[!NOTE]
>
>I dati generalmente non vengono visualizzati nell’interfaccia utente fino a 2-4 ore dopo la ricezione del feed.

*Soluzione o soluzione alternativa possibile:*

1. Verifica che nei rapporti o nelle visualizzazioni dati siano incluse le colonne corrette. Se non sono disponibili le colonne corrette da aggiungere, tu o il tuo Adobe Account Team dovete [rendere le metriche di conversione disponibili per i report](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-available.md).

1. Esegui [!UICONTROL Portfolio Report]. Se è vuoto, eseguire [!UICONTROL Campaign Report] e [!UICONTROL Search Engine Report] per verificare se i ricavi sono visualizzati in tali rapporti. In caso contrario, le campagne potrebbero non essere assegnate al portfolio appropriato.

1. Verifica che il file sia stato inviato al server delle entrate e che il file segua lo stesso formato e la stessa convenzione di denominazione dei file precedenti.

   Se il formato o la convenzione di denominazione del file sono stati modificati, correggere il file e inviarlo di nuovo.

1. Se il file è stato inviato, [contatta l&#39;Assistenza clienti](/help/search-social-commerce/get-help.md).

   L’Assistenza clienti verificherà se il file è stato ricevuto e analizzato. Se il file è stato elaborato senza errori, verifica la presenza di transazioni orfane.
+++

+++Alcuni rapporti avanzati non includono i dati di conversione forniti da un feed dell’inserzionista.
[!UICONTROL Geo Distribution Report] e [!UICONTROL Domain Referral Report] utilizzano dati acquisiti tramite il servizio di monitoraggio delle conversioni di Adobe Advertising e possono essere generati solo per gli inserzionisti con il servizio. I rapporti non includono dati di conversione tracciati all’esterno del sistema di tracciamento delle conversioni di Adobe Advertising.
+++

+++I dati dei ricavi sono diversi da quelli dell’inserzionista.

**Inserzionisti che utilizzano i tag di conversione di Adobe Advertising**

*Possibili cause:*

* Search, Social e Commerce ignorano le entrate quando il cookie viene scaduto o eliminato, ma l’inserzionista potrebbe considerarlo entrate valide.

* Il traffico verso la pagina dell’inserzionista proviene da un segnalibro o da una ricerca organica, anziché da un annuncio.

* Il tag di tracciamento della conversione non è implementato correttamente in tutte le pagine web applicabili o è stato modificato.

*Soluzione o soluzione alternativa possibile:*

1. Vai a **[!UICONTROL Insights & Reports]>[!UICONTROL Reports]** e genera un [!UICONTROL Transaction Report]. Confronta le transazioni ricevute da Search, Social e Commerce con i dati dell&#39;inserzionista.

1. Se alcune transazioni non sono corrette o mancano, assicurati che il tag di tracciamento della conversione pertinente sia implementato in tutte le pagine web applicabili e non sia stato modificato a meno che il team dell’account Adobe non ti abbia consigliato di farlo. Un tag potrebbe mancare o essere stato modificato se il sito web è stato aggiornato di recente.

   Search, Social e Commerce prevedono URL ben formati (con parametri in coppie nome-valore) all&#39;interno della variabile `ef_transaction_properties` e all&#39;interno dell&#39;elemento `src` del tag `img`.

1. Se non riesci a determinare e risolvere il problema, [contatta l&#39;Assistenza clienti](/help/search-social-commerce/get-help.md).

   L’assistenza clienti cercherà di identificare le transazioni mancanti e quindi di verificare la presenza di transazioni orfane e di transazioni che non provengono da un annuncio (&quot;conversioni non correlate&quot;).

**Inserzionisti con feed di dati di conversione che utilizzano `ef_id` valori**

Consulta le possibili cause e soluzioni per le implementazioni pixel di cui sopra.

**Inserzionisti con feed di dati di conversione che utilizzano ID transazione**

*Possibili cause:*

* Search, Social e Commerce ignorano le entrate alla scadenza o alla cancellazione del cookie, ma l’inserzionista potrebbe considerarle entrate valide.

* Il traffico verso la pagina dell’inserzionista proviene da un segnalibro o da una ricerca organica, anziché da un annuncio.

* È stata segnalata una conversione offline prima di una transazione online con lo stesso ID transazione. La transazione online deve essere eseguita per prima.

*Soluzione o soluzione alternativa possibile:*

1. Vai a **[!UICONTROL Insights & Reports]>[!UICONTROL Reports]** e genera un [!UICONTROL Transaction Report]. Confronta le transazioni ricevute da Search, Social e Commerce con i dati di feed dell’inserzionista.

1. Se nel rapporto manca una transazione nel file di feed, verifica se si è verificata una transazione online con lo stesso ID transazione (tracciato tramite il pixel) prima della conversione offline.

1. Se non riesci a determinare e risolvere il problema, [contatta l&#39;Assistenza clienti](/help/search-social-commerce/get-help.md).

   L&#39;Assistenza clienti verificherà la presenza di errori di analisi dei dati e [transazioni orfane](/help/search-social-commerce/glossary.md#o-p).

**Inserzionisti con altri tipi di feed di dati di conversione**

*Possibili cause:*

* Search, Social e Commerce ignorano le entrate quando il cookie viene scaduto o eliminato, ma l’inserzionista potrebbe considerarlo entrate valide.

* Il traffico verso la pagina dell’inserzionista proviene da un segnalibro o da una ricerca organica, anziché da un annuncio.

* Sono presenti [transazioni orfane](/help/search-social-commerce/glossary.md#o-p), pertanto Search, Social e Commerce non contano tutti i ricavi che dovrebbero.

* L’inserzionista ha convalidato un rapporto Search, Social e Commerce in base a un set di dati diverso da quello inviato nel feed.

* Gli ID transazione (`ev_transid` valori) non sono stati inviati, non sono univoci o non sono corretti.

* Il file di feed contiene ID di tracciamento duplicati.

* Errori durante l&#39;analisi del file.

* La logica di deduplicazione dell’inserzionista è diversa da Ricerca, Social e Commerce.

*Soluzione o soluzione alternativa possibile:*

1. Vai a **[!UICONTROL Insights]e[!UICONTROL Reports > Reports]** e genera un [!UICONTROL Transaction Report]. Confronta le transazioni ricevute da Search, Social e Commerce con i dati dell&#39;inserzionista.

1. Se alcune transazioni non sono corrette o mancano, assicurati che a) il file di feed contenga tutti gli ID transazione richiesti e nessun ID di tracciamento duplicato e che b) gli ID transazione siano univoci e corretti.

1. Se non riesci a determinare e risolvere il problema, [contatta l&#39;Assistenza clienti](/help/search-social-commerce/get-help.md).

   L’Assistenza clienti verificherà la presenza di errori di analisi dei dati e transazioni orfane.
+++

+++I dati dei ricavi sono diversi da quelli di Adobe Analytics
Vedi [https://experienceleague.adobe.com/docs/advertising/integrations/analytics/data/data-variances.html?lang=it](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/data/data-variances.html?lang=it).<!-- change link URL to relative link -->
+++

## Rapporti specifici

+++In [!UICONTROL Portfolio Report] devono essere visualizzate le stesse cifre della visualizzazione [!UICONTROL Portfolios]?
La visualizzazione [!UICONTROL Portfolio Report] e la visualizzazione [!UICONTROL Portfolios] mostrano gli stessi dati quando tutti i filtri per la visualizzazione, i parametri del report e le colonne di dati per la visualizzazione e il report sono uguali. Ad esempio, se la visualizzazione [!UICONTROL Portfolios] mostra portfolio che sono &quot;[!UICONTROL All but inactive]&quot; per l&#39;intervallo di date &quot;[!UICONTROL Last 7 days]&quot; e con solo le colonne di dati predefinite visualizzate, un [!UICONTROL Portfolio Report] che utilizza i parametri predefiniti mostra dati identici. Se si modifica uno dei parametri del report o si utilizzano filtri diversi nella visualizzazione [!UICONTROL Portfolios], i valori dei dati potrebbero essere diversi.
+++

+++I dati in [!UICONTROL Portfolio Report] non corrispondono ai dati in [!UICONTROL Search Engine Report] o [!UICONTROL Search Engine Account Report].
[!UICONTROL Portfolio Report] mostra i dati solo per le campagne assegnate ai portfolio specificati, ma [!UICONTROL Search Engine Report] e [!UICONTROL Search Engine Account Report] possono includere anche i dati per le campagne non assegnate a un portfolio.
+++

+++In che modo [!UICONTROL Model Accuracy] > [!UICONTROL Forecast Accuracy Report] è diverso dal livello portfolio [!UICONTROL Model Accuracy Report]?
(Solo per utenti amministratori, manager account di Adobe e manager di agenzia) Il [!UICONTROL Forecast Accuracy Report] disponibile da [!UICONTROL Reports] > [!UICONTROL Model Accuracy] fornisce gli stessi dati del livello portfolio [!UICONTROL Model Accuracy Report], con la differenza che è possibile eseguirlo in più portfolio e modificare la regola di attribuzione. È inoltre possibile eseguire e pianificare il report utilizzando parametri personalizzati e utilizzarlo per creare feed di fogli di calcolo. Inoltre, [!UICONTROL Forecast Accuracy Report] è più accurato del report legacy a livello di portfolio perché valuta la precisione dei ricavi utilizzando gli obiettivi storici per il portfolio anziché l&#39;obiettivo corrente e rappresenta più accuratamente i dati per il fuso orario applicabile.
+++

+++I dati a livello di annuncio non sono disponibili per [!DNL Google Ads] campagne Dynamic Search Ad (DSA), performance max, smart shopping e [!DNL YouTube].
Le reti di annunci non forniscono l’identificatore necessario per attribuire i ricavi a un singolo annuncio per tali campagne. Di conseguenza, i dati sulle prestazioni a livello di annuncio non sono disponibili per questi tipi di campagna nella visualizzazione [!UICONTROL Ads] o in [!UICONTROL Ad Variation Report]. Sono previste discrepanze tra il totale dei dati a livello di annuncio per una campagna e il totale dei dati per la campagna.
+++

+++In [!UICONTROL Transaction Report], come posso sapere quale metrica di conversione proviene da un feed di dati o è tracciata dal pixel di tracciamento di Adobe Advertising?
In un report di transazione, puoi verificare se una metrica di conversione inclusa è stata tracciata dal pixel di tracciamento di Adobe Advertising se includi la colonna personalizzata &quot;[!UICONTROL Tracking URL]&quot;. Gli URL di tracciamento con il pixel di tracciamento di Adobe Advertising iniziano con &quot;`http://pixel.everesttech.net`&quot;.
+++

+++I dati in [!UICONTROL Transaction Report] non corrispondono ai dati in [!UICONTROL Keyword Report].
Quando si generano entrambi i rapporti per portfolio, i dati sono diversi se si genera [!UICONTROL Keyword Report] utilizzando dati storici (ovvero, in base alla configurazione del portfolio durante le date specificate) anziché i dati per le campagne correnti. Quando generi [!UICONTROL Transaction Report] per portfolio, vengono inclusi i dati per le campagne correnti nel portfolio.
+++

## Feed del foglio di calcolo

+++L’output del rapporto include una combinazione di intervalli di date.
È possibile che vengano visualizzati intervalli di date diversi se il feed aggrega dati utilizzando un livello di aggregazione dati diverso da &quot;[!UICONTROL Daily]&quot;.

Per risolvere il problema, aggiorna il feed del foglio di calcolo per includere i dati aggregati giornalmente. Questa attività include l&#39;aggiornamento del modello di report, la generazione di un report utilizzando il modello, la creazione di un modello [!DNL Microsoft Excel] personalizzato utilizzando il report e l&#39;aggiornamento delle impostazioni del feed per includere il nuovo modello di Excel. Per ulteriori informazioni, vedere &quot;[Modifica impostazioni feed report foglio di calcolo](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-edit.md).&quot;
+++

+++Un feed di foglio di calcolo genera un errore interno.
Questo errore può verificarsi se si modificano le colonne nel modello di report ma non si aggiorna il modello [!DNL Microsoft Excel] di conseguenza.

Per risolvere il problema, aggiorna il feed del foglio di calcolo in modo da includere le nuove colonne. Questa attività include l&#39;aggiornamento del modello di report, la generazione di un report utilizzando il modello, la creazione di un modello [!DNL Excel] personalizzato utilizzando il report e l&#39;aggiornamento delle impostazioni del feed per includere il nuovo modello di Excel. Per ulteriori informazioni, vedere &quot;[Modifica impostazioni feed report foglio di calcolo](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-edit.md).&quot;
+++

+++Quando si tenta di aprire un feed di foglio di calcolo in [!DNL Excel], [!DNL Excel] segnala un errore di tipo &quot;contenuto illeggibile&quot; e i dati vengono rimossi dal contenuto recuperato.
Se il modello [!DNL Microsoft Excel] non ordina i dati in base alla data di inizio in ordine crescente, il feed del foglio di calcolo potrebbe includere righe vuote. In particolare, [!DNL Excel] segnala l&#39;errore &quot;Excel ha trovato contenuto illeggibile in &#39;&lt;*nome report*>.xlsx.&#39; Ripristinare il contenuto della cartella di lavoro? Se si considera attendibile l&#39;origine della cartella di lavoro, fare clic su sì.&quot; Se si fa clic su &quot;Sì&quot;, viene visualizzato il seguente messaggio: &quot;Record rimossi: informazioni sulle celle dalla parte /xl/worksheets/sheet1.xml&quot; e il feed del foglio di calcolo include righe vuote.

Per risolvere il problema, modificare il modello [!DNL Excel] associato al feed in modo da ordinare i dati in base a [!DNL Start date in Ascending (Oldest to Newest) order], quindi caricare il modello aggiornato tramite le impostazioni del feed del foglio di calcolo. Per ulteriori informazioni, vedere &quot;[Modifica feed report foglio di calcolo](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-edit.md).&quot;
+++
