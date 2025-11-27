---
title: Dati bulksheet richiesti per  [!DNL Google Ads]  account
description: Fai riferimento ai campi di intestazione e ai campi dati obbligatori nei bulksheet per  [!DNL Google Ads]  account.
exl-id: 756b77fe-f95d-469f-9ae0-7424c2fad0b1
feature: Search Bulksheets
source-git-commit: 3ab2e38f6a2f70c03504363575b13dc0dc730282
workflow-type: tm+mt
source-wordcount: '7859'
ht-degree: 0%

---

# Appendice - Dati bulksheet richiesti per i conti [!DNL Google Ads]

Per creare e aggiornare in blocco i dati della campagna [!DNL Google Ads], è possibile utilizzare i file di bulksheet di Search, Social e Commerce formattati specificamente per gli account [!DNL Google Ads]. È possibile: a) [generare file di fogli collettivi per gli account esistenti](../bulksheet-download.md) nel formato di file richiesto oppure b) crearli manualmente (vedere &quot;[Formati di file di fogli collettivi supportati](bulksheet-file-formats.md)&quot; per informazioni generali sui formati di file supportati).

Ogni bulksheet deve includere i campi intestazione e i campi dati corrispondenti necessari per le [operazioni specifiche che si desidera eseguire](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-operations.md) (ad esempio la creazione di un annuncio). Quando un campo non è obbligatorio, puoi ometterlo dall’intestazione e dalle righe di dati. Tutte le colonne personalizzate vengono eliminate quando caricate il file di foglio ausiliario.

Di seguito è riportata una tabella di tutti i campi dati disponibili e le tabelle aggiuntive che indicano quali campi sono necessari per aggiungere, modificare o eliminare dati per singole entità (ad esempio campagne e parole chiave).

## Tutti i campi dati disponibili {#bulksheet-fields-all-google}

Nella tabella seguente sono descritti tutti i campi dati disponibili.

Per i campi dati relativi alle entità account, vedere &quot;[Campi necessari per creare, modificare o eliminare ogni componente account](#bulksheet-fields-per-component-google).&quot;

>[!NOTE]
>
>* I valori in tutte le colonne di testo fanno distinzione tra maiuscole e minuscole.
>* Quando si crea un nuovo record e non si includono valori per tutti i campi dati obbligatori, ad alcuni di questi campi vengono assegnati i valori predefiniti specificati.
>* Per i campi che non sono specificati di seguito, viene utilizzato il valore predefinito per la rete di annunci.
>* Per un elenco delle righe di bulksheet disponibili nella finestra di dialogo [!UICONTROL Download Bulksheet], vedere &quot;[Righe di bulksheet per rete di annunci](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md#bulksheet-rows-by-ad-network).&quot;

| Campo | Descrizione |
| ---- | ---- |
| [!UICONTROL Platform] | (Incluso nei bulksheet generati a scopo informativo) La piattaforma pubblicitaria. Obbligatorio a meno che ogni riga non includa &quot;[!UICONTROL AMO ID]&quot; per l&#39;entità. |
| [!UICONTROL Acct Name] | Nome univoco che identifica un account di rete di annunci. Obbligatorio a meno che ogni riga non includa &quot;[!UICONTROL AMO ID]&quot; per l&#39;entità. |
| [!UICONTROL Campaign Name] | Il nome univoco che identifica una campagna per un account. |
| [!UICONTROL Campaign Budget] | Limite di spesa giornaliero per la campagna, con o senza simboli monetari e punteggiatura. Questo valore sostituisce ma non può superare il budget del conto. |
| [!UICONTROL Delivery Method] | <p>Velocità di visualizzazione degli annunci per la campagna ogni giorno:</p><ul><li><p><i>[!UICONTROL Standard (Distributed)]</i> (impostazione predefinita per le nuove campagne): per distribuire le impression pubblicitarie nell&#39;arco della giornata.</p></li><li><p><i>[!UICONTROL Accelerated]:</i> (obsoleto a ottobre 2019) Per visualizzare gli annunci il più spesso possibile fino al raggiungimento del budget. Di conseguenza, i tuoi annunci potrebbero non essere visualizzati più avanti nella giornata.</p></li></ul> |
| [!UICONTROL Channel Type] | <p>Canali su cui inserire gli annunci. Specifica una o più opzioni:</p><ul><li><p><i>[!UICONTROL Search]</i> (impostazione predefinita per le nuove campagne): per inserire annunci nella rete di ricerca [!DNL Google Ads] (inclusi i siti Web dei partner di ricerca [!DNL Google Ads]) e facoltativamente anche nella rete di visualizzazione [!DNL Google Ads]. <b>Nota:</b> non è possibile aggiungere a un portfolio per l&#39;ottimizzazione delle offerte le campagne che hanno come destinazione sia la rete di ricerca che la rete di visualizzazione.</p></li><li><p><i>[!UICONTROL Display]</i>: per inserire annunci solo nella rete di visualizzazione [!DNL Google Ads].</p></li><li><p><i>[!UICONTROL Shopping]</i>: per inserire annunci di acquisto nella rete di acquisto [!DNL Google Ads] (in alcuni paesi) e nella rete di ricerca [!DNL Google Ads] (inclusi [!DNL Google Ads] siti Web partner di ricerca e ricerca). Per creare annunci per acquisti, è necessario disporre di prodotti in un account [!DNL Google Merchant Center] e [consentire a Search, Social e Commerce di scaricare dati dall&#39;account](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). Consulta &quot;[Implementare [!DNL Google Ads] campagne acquisti](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)&quot; per ulteriori informazioni sul processo di creazione di annunci acquisti.</p></li></ul> |
| [!UICONTROL Networks] | <p>Dove inserire gli annunci. Specifica una o più opzioni:</p><ul><li><p><i>[!UICONTROL Google Search]</i>: elenchi di ricerca sponsorizzati solo in Google Search Network.</p></li><li><p><i>[!UICONTROL Search Partners]</i>: elenchi di ricerca sponsorizzati sui partner di ricerca di Google.</p></li><li><p><i>[!UICONTROL Content]</i>: per fare offerte per le inserzioni in rete visualizzate.</p></li><li><p><i>[!UICONTROL All]</i> (impostazione predefinita per le nuove campagne): ha come target Google Search, Search Partners e Content.</p></li></ul> |
| [!UICONTROL DSA Domain Name] | <p>(Solo rete di ricerca; applicabile solo agli annunci di ricerca dinamica espansi) Il dominio principale (ad esempio example.com) o il sottodominio (ad esempio shoes.example.com) del sito web il cui contenuto viene utilizzato dalla rete di annunci per eseguire il targeting degli annunci di ricerca dinamica.<br><br><b>Note:</b></p><ul><li><p>Gli annunci per ricerca dinamica espansi hanno come target il contenuto del sito web, anziché le parole chiave.</p></li><li><p>Per eseguire il targeting, il dominio deve essere indicizzato in base all’indice di ricerca organica della rete di annunci.</p></li><li><p>Se non specifichi un dominio, devi creare destinazioni di ricerca dinamica, che eseguano il targeting di tutte le pagine del sito web o di un sottoinsieme di esse, per ogni gruppo di annunci.</p></li></ul> |
| [!UICONTROL DSA Domain Language] | (Solo rete di ricerca; applicabile solo agli annunci di ricerca dinamica espansi) La lingua per il dominio del sito Web specificato. <b>Nota:</b> se il dominio contiene pagine in più lingue e desideri eseguirne il targeting per tutte, crea una campagna separata per ogni lingua. |
| [!UICONTROL GDN Custom Bid Level] | (Campagne mirate solo alla rete di visualizzazione) Come fare offerte: da <i>[!UICONTROL Ad Group]</i> (impostazione predefinita), <i>[!UICONTROL Keyword]</i>, <i>[!UICONTROL Placement]</i> (sito Web) o <i>[!UICONTROL None]</i> (per reimpostare il valore esistente). Altre dimensioni (<i>Età</i>, <i>Genere</i>, <i>Interesse ed Elenco</i>, <i>Argomento</i> e <i>Verticale</i>) sono disponibili dall&#39;interfaccia [!DNL Google Ads]. Se è stata utilizzata l&#39;interfaccia [!DNL Google Ads] per configurare l&#39;offerta per un&#39;altra dimensione, il valore viene visualizzato, ma non è possibile selezionare o immettere le dimensioni qui.</p><p><b>Nota:</b></p><ul><li><p>Quando fai offerte per parola chiave, crea modelli di tracciamento a livello di parola chiave. Allo stesso modo, quando fai un&#39;offerta per posizionamento, crea modelli di tracciamento a livello di posizionamento. Per tutte le altre dimensioni, crea modelli di tracciamento a livello di annuncio.</p></li><li><p>Quando fai un&#39;offerta per una dimensione non supportata (Età, Genere, Interesse ed Elenco o Argomento), Ricerca, Social e Commerce non ottimizzano le offerte per la dimensione e tutta l&#39;attribuzione viene applicata al gruppo di annunci.</p></li><li><p>Gli annunci sulla rete di ricerca utilizzano sempre le offerte basate su parole chiave.</p></li></ul> |
| [!UICONTROL Campaign Priority] | <p>(Solo campagne acquisti) La priorità con cui viene utilizzata la campagna quando più campagne pubblicizzano lo stesso prodotto: <i>[!UICONTROL Low]</i> (impostazione predefinita per le nuove campagne), <i>[!UICONTROL Medium]</i> o <i>[!UICONTROL High]</i>.</p><p>Se lo stesso prodotto è incluso in più campagne, il network pubblicitario utilizza per prima cosa la priorità della campagna per determinare quale campagna (e l’offerta associata) è idonea per l’asta degli annunci. Se tutte le campagne hanno la stessa priorità, la campagna con l’offerta più elevata è idonea. |
| [!UICONTROL Merchant ID] | (Campagne commerciali e campagne di pubblico collegate solo a un feed esercente) L’ID cliente dell’account esercente i cui prodotti vengono utilizzati per la campagna. |
| [!UICONTROL Sales Country] | (Solo campagne commerciali; sola lettura per le campagne esistenti) Il paese in cui vengono venduti i prodotti della campagna. Poiché i prodotti sono associati ai paesi di destinazione, questa impostazione determina quali prodotti vengono pubblicizzati nella campagna. |
| [!UICONTROL Product Scope Filter] | (Solo campagne che utilizzano la rete di acquisto [!DNL Google Ads]) I prodotti nel tuo account [!DNL Google Merchant Center] per i quali è possibile creare annunci per la campagna. Puoi immettere fino a sette combinazioni di dimensioni e attributi di prodotto su cui filtrare i prodotti, utilizzando il formato dimension=attribute. Separa più filtri con un delimitatore &quot;>>&quot;. Per un elenco delle dimensioni di prodotto disponibili, consulta &quot;[Filtri di prodotto per campagne acquisti](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md).&quot;</p><p>Esempio: &quot;CategoryL1=animal>>CategoryL2=pet supply>>Brand=Acme Pet Supplies&quot;</p><p>Per eliminare i valori esistenti, utilizzare il valore <code>[delete]</code> (comprese le parentesi).</p> |
| [!UICONTROL Languages] | <p>(Solo reti di ricerca e visualizzazione) Le lingue di destinazione per gli annunci nella campagna.</p><p>Se non immetti un valore per questo campo o per il campo [!UICONTROL Geo Targeting] di una nuova campagna, la valuta specificata per l&#39;account determina le lingue predefinite, tranne per il fatto che le campagne con valute non mappate a lingue specifiche (ad esempio, EUR) sono indirizzate a tutte le lingue. Se non si immette un valore per questo campo ma si immette un valore nel campo [!UICONTROL Geo Targeting] per una nuova campagna, il valore predefinito sarà <i>[!UICONTROL All]</i>. Se lasci vuoto questo campo per una campagna esistente, il valore esistente viene mantenuto.</p><p>Per eseguire il targeting per tutte le lingue, immetti <span style="font-style: italic;">&lt;i[!UICONTROL >All]</i></span>. Per eseguire il targeting di lingue specifiche, immettere valori separati da punti e virgola utilizzando <a href="https://developers.google.com/adwords/api/docs/appendix/codes-formats?csw=1#languages" target="_blank">[!DNL Google Ads] nomi di lingua</a> (ad esempio <i>Inglese;Giapponese</i>, che vengono sostituiti con i codici numerici corretti) o codici numerici (ad esempio <i>1000;1005</i>). I valori non fanno distinzione tra maiuscole e minuscole.</p> |
| [!UICONTROL Location] | Una posizione geografica in cui inserire annunci o per la quale escludere annunci per la campagna. Se non si immettono valori per questo campo o per il campo Lingue di una nuova campagna, le posizioni predefinite verranno determinate dalla valuta specificata per il conto, tranne per il fatto che le campagne con valute non mappate a posizioni specifiche (ad esempio, EUR) sono indirizzate a tutte le posizioni. Se non si immette un valore per questo campo ma si immette un valore nel campo [!UICONTROL Languages] per una nuova campagna, il valore predefinito sarà <i>[!UICONTROL All]</i>. Se lasci vuoto questo campo per una campagna esistente, il valore esistente viene mantenuto.</p><p>Per individuare una posizione specifica, utilizzare uno dei [[!DNL Google Ads] nomi di posizione](https://developers.google.com/adwords/api/docs/appendix/geotargeting) (sostituiti con il codice numerico corretto) o i codici di posizione:</p><ul><li><p>Paesi/territori: immettere i nomi dei paesi/territori (ad esempio <i>Stati Uniti;Giappone</i>) o i codici numerici (ad esempio <i>2840;2392</i>).</p></li><li><p>Stati/province/regioni: immettere i nomi di stato/provincia/regione con le abbreviazioni di paese/territorio correlate (ad esempio <i>Tokyo, JP;New York, US</i>) o i codici numerici (ad esempio <i>20636;21167</i>).</p></li><li><p>Città non USA: immettere il nome della città, lo stato/provincia/regione e le abbreviazioni del paese/territorio (ad esempio <i>Adachi, Tokyo, JP;Kita, Tokyo, JP</i>) oppure i codici numerici (ad esempio <i>1028850;1009293</i>)</p></li><li><p>Aree metropolitane USA: immettere i nomi delle città, degli stati e le abbreviazioni dei paesi (ad esempio <i>Buffalo NY, US;New York NY, US</i>) o i codici numerici (ad esempio <i>514;501</i>).</p></li></ul><p>Per escludere una posizione, anteporre al nome o al codice della posizione un segno meno (`-`), ad esempio <i>-Giappone</i>.</p><p><b>Nota:</b> i valori non fanno distinzione tra maiuscole e minuscole.</p> |
| [!UICONTROL Location Type] | (Quando includi una posizione) Il [tipo di posizione](https://developers.google.com/google-ads/api/data/geotargets). |
| [!UICONTROL Device] | Tipo di dispositivo per il quale vengono apportate regolazioni delle offerte a livello di campagna o di gruppo di annunci: <i>[!UICONTROL smartphone]</i>, <i>[!UICONTROL tablet]</i> o <i>[!UICONTROL desktop]</i>. |
| [!UICONTROL Bid Adjustment] | <p>(Quando includi una destinazione [!UICONTROL Location], [!UICONTROL Device] o [!UICONTROL RLSA]) Se regolare le offerte per gli annunci in una posizione specifica, su un tipo di dispositivo specifico o con una destinazione di pubblico specifica:</p><ul><li><p>Per utilizzare l&#39;offerta a livello di parola chiave (differenza 0%), immetti 0. Per i nuovi target, puoi anche lasciare vuoto questo campo.</p></li><li><p>Per utilizzare un&#39;offerta diversa per questo target, immettere la percentuale di aumento o di diminuzione delle offerte.</p></li><ul><li><p>Per le destinazioni RLSA e posizione, le percentuali valide includono da -90 a 900.</p></li><li><p>Per le regolazioni delle offerte dei dispositivi, le percentuali valide includono:</p></li><ul><li><p>(Campagne)-100 (per non fare offerte per annunci sul tipo di dispositivo) o da -90 a 900.</p></li><li><p>(Gruppi di annunci) -100 per smartphone e tablet (per non fare offerte per il tipo di dispositivo) e da -90 a 900 per tutti i tipi di dispositivo.</p></li></ul></ul><li><p>(Campagne e gruppi di annunci esistenti) Per utilizzare la regolazione dell’offerta esistente, lascia vuoto questo campo.</p></li></ul> |
| [!UICONTROL Adobe Rec Bid Adjustment] | (Incluso nei bulksheet generati a scopo informativo) La regolazione dell’offerta di sola lettura consigliata da Adobe per il target di posizione a livello di campagna o un RLSA. Viene calcolato solo quando la campagna si trova in un portfolio con un obiettivo che utilizza metriche di conversione ponderate (non l&#39;obiettivo [!UICONTROL Maximize Clicks]) e la campagna contiene almeno due target di posizione o RLSA con almeno cinque clic o 5 USD di costo negli ultimi 90 giorni.</p><p>Se si desidera modificare manualmente una destinazione di posizione o RLSA per utilizzare il valore consigliato, attendere almeno due settimane dopo aver creato la destinazione di posizione o RLSA per consentire una raccolta dati sufficiente e non modificare il valore più di una volta alla settimana. |
| [!UICONTROL Device Targets] | <p>(Solo tipi di campagna legacy) I dispositivi su cui può essere visualizzato l’annuncio: <i>[!UICONTROL All]</i>, <i>[!UICONTROL Computers]</i>, <i>[!UICONTROL Smartphones]</i> o <i>[!UICONTROL Tablets]</i>. Per le nuove campagne, il valore predefinito è <i>[!UICONTROL All]</i>.</p> |
| [!UICONTROL Device OS Targets (Google Adwords)] | (Solo tipi di campagna legacy; applicabile quando le destinazioni dispositivo includono &quot;Smartphone&quot; o &quot;Tablet&quot;) I sistemi operativi in cui l&#39;annuncio può essere visualizzato: <i>[!UICONTROL All]</i>, <i>[!UICONTROL Android]</i>, <i>[!UICONTROL iOS]</i> o <i>[!UICONTROL Palm]</i>. Per le nuove campagne, il valore predefinito è <i>[!UICONTROL All]</i>.</p> |
| [!UICONTROL Mobile Carriers (Google Adwords)] | <p>(Solo tipi di campagna legacy; applicabile quando [!UICONTROL Device Targets] includono &quot;[!UICONTROL All]&quot; o &quot;[!UICONTROL Smartphones]&quot;) gestori di telefonia mobile a cui gli smartphone possono essere connessi: <i>[!UICONTROL All]</i>, o uno o più gestori indicati da &lt;c<i>codice gestore</i>>,&lt;<i>codice paese</i>> (ad esempio T-Mobile,US) utilizzando l&#39;elenco di <a href="https://developers.google.com/adwords/api/docs/appendix/codes-formats?csw=1#mobile-carriers" target="_blank">gestori e codici disponibili per [!DNL Google Ads]</a>. Separa più gestori con punti e virgola ( ad esempio T-Mobile,US;T-Mobile,GB). Per le nuove campagne, il valore predefinito è <i>[!UICONTROL All]</i>.</p> |
| [!UICONTROL Ad Group Name] | <p>Nome univoco che identifica un gruppo di annunci. La lunghezza massima è di 255 caratteri; i caratteri vuoti finali non vengono salvati (ad esempio, &quot;Gruppo di annunci 1&quot; viene salvato come &quot;Gruppo di annunci 1&quot;). Questo campo non è applicabile per sitelink a livello di campagna o target di dispositivi a livello di campagna.</p> |
| [!UICONTROL Ad Group Type] | <p>Tipo di gruppo di annunci: <i>[!UICONTROL Demand Gen]</i> (solo per campagne demand gen), <i>[!UICONTROL Display]</i> (per campagne display), <i>[!UICONTROL Search Dynamic]</i> (per annunci di ricerca dinamica espansi), <i>[!UICONTROL Search Standard]</i> (per annunci search), <i>[!UICONTROL Shopping Product]</i> (per annunci shopping di prodotti), <i>[!UICONTROL Shopping Showcase]</i> (creazione e modifica non supportate) o <i>[!UICONTROL Unknown]</i>.</p> |
| [!UICONTROL Max CPC] | <p>(Solo campagne CPC) Il costo massimo per clic (CPC), che è l’importo più alto da pagare per un clic sull’annuncio sulla rete di annunci, con o senza simboli monetari e punteggiatura. Puoi impostare i valori per gruppi di annunci, parole chiave, gruppi di prodotti e destinazioni di ricerca dinamica. Il valore predefinito per una nuova parola chiave viene ereditato dal livello del gruppo di annunci. Per i gruppi di prodotti, è possibile impostare i valori per il livello più basso del gruppo di prodotti; il valore predefinito per un nuovo livello viene ereditato dal livello padre.</p><p>Per i gruppi di prodotti esistenti e i target di ricerca dinamica in portfolio ottimizzati, gli aggiornamenti sono validi per un solo giorno e vengono sovrascritti durante il successivo ciclo di ottimizzazione.</p> |
| [!UICONTROL Max Content CPC] | <p>(Solo campagne CPC) Il costo massimo del contenuto per clic (CPC), che è l’importo più alto da pagare per un clic di un annuncio da un sito di rete di visualizzazione, con o senza simboli monetari e punteggiatura. Puoi impostare e modificare i valori a livello di gruppo di annunci nelle campagne per le quali non è stato eseguito il targeting del posizionamento.</p> |
| [!UICONTROL Audience Target Method] | <p>(Campagne solo nella rete di ricerca e campagne [!DNL Gmail] di sola lettura esistenti nella rete di visualizzazione) Procedura:</p><ul><li><p><i>[!UICONTROL Target and Bid]</i>: per mostrare annunci solo agli utenti associati ai tipi di pubblico di destinazione che soddisfano anche altri target per il gruppo di annunci.</p></li><li><p><i>[!UICONTROL Bid Only]</i>: per mostrare annunci anche a persone non associate a tipi di pubblico di destinazione, purché soddisfino altri target a livello di gruppo di annunci.</p><p>Tuttavia, puoi aumentare le possibilità che gli annunci vengano mostrati a tipi di pubblico specifici, impostando offerte più elevate per tali tipi di pubblico.</p></li></ul> |
| [!UICONTROL Keyword] | La stringa della parola chiave. La lunghezza massima è di 80 caratteri e non può superare le 10 parole e può includere solo lettere, cifre e i seguenti caratteri speciali: spazio `# $ & _ - " [ ] ' + . / :`</p><p><b>Nota:</b></p><ul><li><p>Per escludere una parola chiave a livello di gruppo di annunci o di campagna, impostare [!UICONTROL Match Type] su <i>[!UICONTROL Negative]</i>. Se la riga include il nome del gruppo di annunci, la parola chiave viene esclusa per il gruppo di annunci. Se la riga non include il nome del gruppo di annunci, la parola chiave viene esclusa per l’intera campagna.</p></li><li><p>Se si modifica una parola chiave o un tipo di corrispondenza [!DNL Google Ads], la parola chiave esistente verrà eliminata e ne verrà creata una nuova.</p></li></ul> |
| [!UICONTROL Placement] | (Solo campagne che utilizzano contenuti corrispondenti) Posizione nella rete di visualizzazione in cui possono essere visualizzati gli annunci. Specificare una delle seguenti opzioni:</p><ul><li><p>Sito Web: immettere un URL valido. Può essere un dominio di primo livello, un sottodominio di primo livello o un dominio con un singolo nome di directory. L&#39;URL non può includere un punto interrogativo (?). Esempi:<code><br />www.example.com<br />example.com<br />autos.example.com<br />example.com/widgets</code></p></li><li><p>Una posizione annuncio su una pagina specifica: utilizza il formato `<URL> >> <location,sublocation>` (ad esempio `finance.google.com >> Company pages,Top right`).</p></li><li><p>Categoria argomento: utilizzare la sintassi `<category::<category> > <subcategory>` e così via (ad esempio `category::Industries > Energy & Utilities > Oil & Gas`).</p></li></ul><p><b>Nota:</b> Per escludere un posizionamento a livello di gruppo di annunci o di campagna, imposta [!UICONTROL Match Type] su <i>[!UICONTROL Negative]</i>. Se la riga include il nome del gruppo di annunci, il posizionamento viene escluso per il gruppo di annunci. Se la riga non include il nome del gruppo di annunci, il posizionamento viene escluso per l’intera campagna.</p> |
| [!UICONTROL Auto Target Expression] | <p>(Obbligatorio quando l&#39;impostazione della campagna su &quot;[!UICONTROL Use my website contents to target my ads]&quot; non è abilitata; facoltativo altrimenti) Destinazioni di ricerca dinamica per il gruppo di annunci.</p><p>Per tutte le destinazioni, utilizzare un asterisco (*).</p><p>Per eseguire il targeting di un massimo di tre criteri di ricerca dinamica, utilizzare il formato `<category>=<target>`, dove `<category>` può includere una qualsiasi delle categorie seguenti. Unisci più destinazioni per una singola categoria con &quot;\[spazio vuoto\] e \[spazio vuoto\]&quot; e unisci più categorie con &quot;[spazio vuoto] e [spazio vuoto]&quot;.</p><ul><li><p><i>[!UICONTROL Category]</i>: per visualizzare annunci di ricerca dinamica espansi per pagine indicizzate con una categoria di contenuto [!DNL Google Ads] specifica.</p></li><li><p><i>[!UICONTROL URL]</i>: per visualizzare annunci di ricerca dinamica espansi per pagine indicizzate con un URL specifico, in cui il valore può essere incluso in qualsiasi punto dell&#39;URL.</p></li><li><p><i>[!UICONTROL Page Title]</i>: per visualizzare annunci di ricerca dinamica espansi per pagine indicizzate con testo specifico nel titolo della pagina.</p></li><li><p><i>[!UICONTROL Page Content]</i>: per visualizzare annunci di ricerca dinamica espansi per pagine indicizzate con contenuto specifico.</p></li></ul><p>Esempio: url=shoes.example.com e page title=footwear</p> |
| [!UICONTROL Parent Product Groupings] | Gerarchia di eventuali gruppi di prodotti padre.<br><br>Esempio: `All Products>>ProductTypeL1=a>>ProductTypeL2=b` |
| [!UICONTROL Product Grouping] | <p>Il gruppo di prodotti (ad esempio &quot;brand=acme&quot; o &quot;All Products&quot;).</p><p><b>Nota:</b></p><ul><li><p>Quando un gruppo di prodotti specificato non esiste nella gerarchia [!UICONTROL Parent Product Groupings], in Ricerca, Social e Commerce vengono create le parti della gerarchia necessarie.</p></li><li><p>Search, Social e Commerce creano automaticamente un gruppo &quot;[!UICONTROL All Products]&quot; quando si crea un gruppo di annunci in una campagna acquisti [!DNL Google Ads] con un&#39;offerta predefinita impostata sull&#39;offerta predefinita del gruppo di annunci. Search, Social e Commerce creano automaticamente un gruppo &quot;[!UICONTROL Everything Else]&quot; con l&#39;offerta predefinita del gruppo di annunci a ogni livello della gerarchia del gruppo di prodotti. Puoi comunque creare in modo esplicito questi gruppi predefiniti, escludendoli o modificandone le offerte.</p></li><li><p>Ogni gruppo di annunci può includere fino a otto livelli di gruppi di prodotti, tra cui &quot;[!UICONTROL All Products]&quot; e altri sette livelli.</p></li></ul> |
| [!UICONTROL Partition Type] | Il tipo di partizione per il gruppo di prodotti: <i>sottodivisione</i> (se include gruppi di prodotti figlio) o <i>unità</i> (se non include gruppi di prodotti figlio). |
| [!UICONTROL Match Type] | <p>Per il target di ricerca dinamica o i gruppi di prodotti: Opzione di corrispondenza delle parole chiave per il target di ricerca dinamica o il gruppo di prodotti: <i>[!UICONTROL Dynamic Ad Target]</i> (impostazione predefinita per i nuovi target di ricerca dinamica), <i>[!UICONTROL Product Group]</i> (impostazione predefinita per i nuovi gruppi di prodotti) o <i>[!UICONTROL Negative Product Group]</i> (per escludere un gruppo di prodotti).</p><p>Per le parole chiave: l&#39;opzione di corrispondenza delle parole chiave per la parola chiave: <i>[!UICONTROL Broad]</i>, <i>[!UICONTROL Phrase]</i>, <i>[!UICONTROL Exact]</i> o <i>[!UICONTROL Negative]</i> (per escludere una parola chiave o un posizionamento nella rete di visualizzazione); i gruppi di prodotti utilizzati con gli annunci di acquisto hanno un tipo di corrispondenza <i>[!UICONTROL Product Group]</i>. Se utilizzi <i>[!UICONTROL Negative]</i>, devi includere anche il tipo di corrispondenza da escludere (ad esempio, &quot;Frase negativa&quot;).</p><p>Per le nuove parole chiave, il valore predefinito è <i>[!UICONTROL Broad]</i>. Un valore per il tipo di corrispondenza o per l’ID della parola chiave è necessario solo per modificare una parola chiave con più tipi di corrispondenza.</p><p><b>Nota:</b></p><ul><li><p>I tipi di corrispondenza non sono applicabili agli annunci di ricerca dinamica espansi, che non utilizzano parole chiave.</p></li><li><p>Se si modifica il tipo di corrispondenza per una parola chiave [!DNL Google Ads], la parola chiave esistente verrà eliminata e ne verrà creata una nuova.</p></li><li><p>Per il Broad Match Modifier, scegliete &quot;Broad&quot; e inserite un + prima di qualsiasi parola all&#39;interno della parola chiave per la quale sono richieste varianti di chiusura (ad esempio &quot;+red +shoes&quot; per richiedere varianti di chiusura sia di &quot;red&quot; che di &quot;shoes&quot;). <b>Nota:</b> i modificatori di corrispondenza ampia hanno ora lo stesso comportamento di corrispondenza della corrispondenza della frase per alcune lingue e non è possibile creare nuove parole chiave del modificatore di corrispondenza ampia da luglio 2021. Per ulteriori informazioni, consulta la [[!DNL Google Ads] documentazione](https://support.google.com/google-ads/answer/7042511).</p> |
| [!UICONTROL First Page Bid] | (Inclusa nei bulksheet generati a scopo informativo) L’offerta necessaria per inserire un annuncio sulla prima pagina dei risultati della ricerca. Questo valore non viene inviato alla rete di annunci. |
| [!UICONTROL Quality Score] | (incluso nei bulksheet generati a scopo informativo) Il punteggio di qualità corrente assegnato dal motore di ricerca alla parola chiave. Questo valore non viene inviato alla rete pubblicitaria.) |
| [!UICONTROL Creative Preferred Devices] | (Annunci di testo, annunci di ricerca dinamica espansi e sitelink avanzati; facoltativo) Tipi di dispositivi su cui si preferisce visualizzare l&#39;annuncio: <i>[!UICONTROL All]</i> (impostazione predefinita) o <i>[!UICONTROL Mobile]</i>. Quando si specifica <i>[!UICONTROL Mobile]</i>, la rete tenta di visualizzare l&#39;annuncio agli utenti di dispositivi mobili anziché agli utenti di desktop o tablet. In caso contrario, l’annuncio verrà visualizzato in rete su qualsiasi tipo di dispositivo.</p><p><b>Nota:</b></p><ul><li><p>Solo l&#39;amministratore e gli utenti del gestore account [!DNL Adobe] possono modificare questa impostazione.</p></li><li><p>La rete non garantisce la visualizzazione dell&#39;annuncio sul tipo di dispositivo preferito.</p></li><li><p>È possibile creare nuovi sitelink avanzati solo nelle campagne con sitelink avanzati esistenti o senza sitelink.</p></li></ul> |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-15 | (Solo annunci di testo espansi e annunci di ricerca responsive) I titoli di un annuncio, ciascuno separato da una barra verticale (&vert;). La lunghezza massima per ciascun campo del titolo dell’annuncio è di 30 caratteri o 15 caratteri a doppio byte, incluso qualsiasi testo dinamico (come i valori delle parole chiave e degli ad customizer).</p><p>Per gli annunci di ricerca responsive, sono necessari [!UICONTROL Ad Title], [!UICONTROL Ad Title 2] e [!UICONTROL Ad Title 3] e tutti gli altri campi del titolo dell&#39;annuncio sono facoltativi. Per eliminare il valore esistente per un campo non obbligatorio, utilizzare il valore <code>[delete]</code> (comprese le parentesi).</p><p>Per gli annunci di ricerca responsive, inserire un personalizzatore di annunci utilizzando il seguente formato: <code>{CUSTOMIZER.AdCustomizerName:DefaultText}</code>, ad esempio <code>{CUSTOMIZER.Discount:10%}</code></p><p>Non puoi creare o modificare, ma puoi eliminare gli annunci di testo espansi, che [!DNL Google Ads] ha dichiarato obsoleti a giugno 2022. |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | <p>(Solo annunci di ricerca reattiva; facoltativo) Posizione in cui fissare il titolo dell&#39;annuncio corrispondente: `[null]` (nessun valore, che rende il titolo dell&#39;annuncio idoneo per tutte le posizioni), <i>1</i>, <i>2</i> o <i>3</i>. Ad esempio, se [!UICONTROL Ad Title Position] ha un valore pari a 1, Titolo annuncio verrà visualizzato solo nella posizione 1. Per impostazione predefinita, tutti i titoli degli annunci sono nulli (non hanno valori).</p><p>Per eliminare il valore esistente, utilizzare il valore <code>[delete]</code> (comprese le parentesi).</p><p><b>Nota:</b> puoi fissare più titoli di annunci nella stessa posizione. La rete di annunci utilizza uno dei titoli degli annunci fissati alla posizione. I titoli fissati alla posizione 3 potrebbero non essere visualizzati con l’annuncio.</p> |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | <p>(Solo annunci di ricerca dinamica espansi, annunci di testo espansi e annunci di ricerca responsive) Il corpo di un annuncio. La lunghezza massima per ciascun campo di descrizione è di 90 caratteri o 45 caratteri a doppio byte, incluso qualsiasi testo dinamico (come i valori delle parole chiave e degli ad customizer).</p><p>Per gli annunci di ricerca responsive, inserire un personalizzatore di annunci utilizzando il seguente formato: `{CUSTOMIZER.AdCustomizerName:DefaultText}`, ad esempio `{CUSTOMIZER.Discount:10%}`</p><p>Per gli annunci di ricerca dinamica espansi, utilizzare solo [!UICONTROL Description Line 1] e [!UICONTROL Description Line 2]. <b>Nota:</b> Per questo tipo di annuncio, la modifica della copia dell&#39;annuncio elimina l&#39;annuncio esistente e ne crea uno nuovo.</p><p>Non puoi creare o modificare, ma puoi eliminare gli annunci di testo espansi, che [!DNL Google Ads] ha dichiarato obsoleti a giugno 2022.</p><p>Per gli annunci di ricerca responsive, sono necessari [!UICONTROL Description Line 1] e [!UICONTROL Description Line 2] e [!UICONTROL Description Line 3] e [!UICONTROL Description Line 4] sono facoltativi. Per eliminare il valore esistente, utilizzare il valore <code>[delete]</code> (comprese le parentesi).</p> |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | (Solo annunci di ricerca reattiva; facoltativo) Posizione in cui fissare la descrizione corrispondente: `[null]` (nessun valore, che rende la descrizione idonea per tutte le posizioni), <i>1</i>, <i>2</i> o <i>3</i>. Ad esempio, se [!UICONTROL Description 1 Position] ha un valore pari a 1, [!UICONTROL Description 1] viene visualizzato solo nella posizione 1. Per impostazione predefinita, nessuna descrizione è bloccata su una posizione.</p><p>Per eliminare il valore esistente, utilizzare il valore `[delete]` (comprese le parentesi).</p><p><b>Nota:</b> è possibile fissare più descrizioni nella stessa posizione. La rete di annunci utilizza una delle descrizioni fissate alla posizione. Le descrizioni fissate alla posizione 2 potrebbero non essere visualizzate con l’annuncio. |
| [!UICONTROL Display URL] | L’URL incluso nell’annuncio.<br><br>Per gli annunci di ricerca dinamica espansi, [!DNL Google Ads] genera questo valore in modo dinamico dal dominio del sito Web e non è necessario immettere un valore.<br><br>Per gli annunci di ricerca responsive, non è necessario immettere un valore. L’URL di visualizzazione viene estratto automaticamente dal dominio nell’URL finale. Facoltativamente, puoi personalizzare l’URL utilizzando i campi Percorso 1 e Percorso 2.<br><br>Non puoi creare o modificare, ma puoi eliminare gli annunci di testo espansi, che [!DNL Google Ads] ha dichiarato obsoleti a giugno 2022.<br><br><b>Nota:</b> (account con URL finali) i nomi di dominio nell&#39;URL di visualizzazione e nell&#39;URL finale devono corrispondere.</p> |
| [!UICONTROL Display Path 1] | <p>(Solo annunci di testo espansi<span> e annunci di ricerca responsive</span>)</p><p>(Facoltativo) Testo aggiunto all&#39;URL di visualizzazione che viene estratto automaticamente dall&#39;URL finale. È preceduta nell’URL da una barra (/). Un percorso non può contenere barre (/) o caratteri di nuova riga (\n). La lunghezza massima è di 15 caratteri o 7 caratteri a doppio byte.</p><p>Per inserire un personalizzatore di annunci, usa i seguenti formati, dove `Default text` è un valore facoltativo da inserire quando il file di feed non include un valore valido:&lt; `{CUSTOMIZER.AdCustomizerName:Default text}`, ad esempio `{CUSTOMIZER.Discount:10%}`</p><p>Ad esempio, se [!UICONTROL Display Path 1] è &quot;offerte&quot;, l&#39;URL di visualizzazione è &lt;<i>URL di visualizzazione</i>>/offerte, ad esempio www.example.com/deals.</p><p>Non puoi creare o modificare, ma puoi eliminare gli annunci di testo espansi, che [!DNL Google Ads] ha dichiarato obsoleti a giugno 2022.</p> |
| [!UICONTROL Display Path 2] | Un secondo percorso di visualizzazione; vedere la voce per [!UICONTROL Display Path 1].<br><br>Esempio: se [!UICONTROL Display Path 1] è &quot;offerte&quot; e [!UICONTROL Display Path 2] è &quot;locale&quot;, l&#39;URL di visualizzazione è &lt;<i>URL di visualizzazione</i>>/offerte/locale, ad esempio www.example.com/deals/local.</p><p>Non puoi creare o modificare, ma puoi eliminare gli annunci di testo espansi, che [!DNL Google Ads] ha dichiarato obsoleti a giugno 2022.</p> |
| [!UICONTROL Promotion Line] | (Solo annunci di inserzioni di prodotti) Una linea promozionale opzionale da includere nell’elenco dei prodotti nei risultati di ricerca. La lunghezza massima è di 45 caratteri.</p><p>La linea della promozione può apparire in posizioni diverse rispetto all&#39;annuncio (ad esempio sotto l&#39;annuncio) a seconda di dove l&#39;annuncio viene visualizzato sulla pagina. |
| [!UICONTROL Link Name] | <p>Testo del sitelink. Può contenere fino a 25 caratteri.</p><p>Per i nuovi sitelink, devi includere il nome della campagna nella riga del sitelink. Per i sitelink a livello di gruppo di annunci, devi includere anche il nome del gruppo di annunci.</p><p><b>Nota:</b> il testo esistente di 35 caratteri viene ancora visualizzato negli annunci su desktop e tablet ma non su dispositivi mobili.</p> |
| [!UICONTROL Mobile App Platform (Google Adwords)] | (Solo annunci di installazione app esistenti) Sistema operativo in cui viene eseguita l&#39;applicazione mobile: <i>Android™</i> o <i>ios</i>. |
| [!UICONTROL Mobile App ID (Google Adwords)] | (Solo annunci di installazione app esistenti) <p>ID dell’applicazione o nome del pacchetto. |
| [!UICONTROL Mobile App Name (Google Adwords)] | (Solo annunci di installazione app esistenti) Il nome dell’applicazione. |
| [!UICONTROL Start Date] | <p>(Solo sitelink avanzati) La prima data in cui è possibile fare offerte per il sitelink, nel fuso orario dell&#39;inserzionista e in uno dei seguenti formati: <i>m/g/aaaa</i>, <i>m/g/aa</i>, <i>m-g-aaaa</i> o <i>m-g-aa</i>. Per impostazione predefinita, i nuovi sitelink migliorati sono nel giorno corrente.</p><p><b>Nota:</b> è possibile creare nuovi sitelink avanzati solo nelle campagne con sitelink avanzati esistenti o senza sitelink.</p> |
| [!UICONTROL End Date] | <p>(Solo sitelink avanzati) L&#39;ultima data in cui è possibile fare offerte per il sitelink, nel fuso orario dell&#39;inserzionista e in uno dei seguenti formati:  <i>m/g/aaaa</i>, <i>m/g/aaaa</i>, <i>m-g-aaaa</i>, o <i>m-g-aaaa</i>. Il valore predefinito è none (nessuna data di fine).</p><p><b>Nota:</b> è possibile creare nuovi sitelink avanzati solo nelle campagne con sitelink avanzati esistenti o senza sitelink.</p> |
| [!UICONTROL Exclude Tablet (Google Adwords)] | (Solo annunci di installazione app esistenti)</p><p>(Facoltativo) Impedisce a [!DNL Google Ads] di visualizzare l&#39;annuncio agli utenti del tablet. I valori possono includere <i>yes</i> e <i>no</i>. |
| [!UICONTROL Landing Page Suffix] | Eventuali parametri da aggiungere alla fine degli URL finali per tenere traccia delle informazioni. Esempio: `param2=value1&param3=value2`<br><br>Visualizza &quot;[Formati di tracciamento dei clic per [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md).&quot;<br><br>I suffissi URL finali ai livelli inferiori sovrascrivono il suffisso a livello di account. Per una manutenzione più semplice, utilizza solo il suffisso a livello di account, a meno che non sia necessario un tracciamento diverso per i singoli componenti dell’account. Per configurare un suffisso a livello di gruppo di annunci o inferiore, utilizzare l&#39;editor [!DNL Google Ads]. |
| [!UICONTROL Tracking Template] | Il modello di tracciamento, che specifica tutti i reindirizzamenti del dominio di destinazione e i parametri di tracciamento e incorpora l&#39;URL finale in un parametro [!DNL ValueTrack]. Il modello di tracciamento al livello più granulare (con la parola chiave come più granulare) sostituisce i valori a tutti i livelli superiori.<br><br>Per il monitoraggio delle conversioni di Adobe Advertising, applicato quando le impostazioni della campagna includono &quot;[!UICONTROL EF Redirect]&quot; e &quot;[!UICONTROL Auto Upload]&quot;, Search, Social e Commerce aggiungono automaticamente il proprio codice di reindirizzamento e di tracciamento quando si salva il record.<br><br>Per reindirizzamenti e monitoraggio di terze parti, immettere un valore. Per un elenco di [!DNL ValueTrack] parametri per indicare gli URL finali nei modelli di tracciamento, vedere i parametri &quot;Solo modello di tracciamento&quot; nella sezione &quot;Parametri [!DNL ValueTrack] disponibili&quot; nella [[!DNL Google Ads] documentazione](https://support.google.com/google-ads/answer/2375447).<br><br>Per eliminare il valore esistente, utilizzare il valore `[delete]` (comprese le parentesi). |
| [!UICONTROL Base URL/Final URL] | L’URL della pagina di destinazione a cui vengono indirizzati gli utenti dei motori di ricerca quando fanno clic sull’annuncio, compresi eventuali parametri di aggiunta configurati per la campagna o l’account. Gli URL di base/finali a livello di parola chiave sostituiscono quelli a livello di annuncio e superiori.<br><br>Per eliminare il valore esistente, utilizzare il valore `[delete]` (comprese le parentesi). |
| [!UICONTROL Destination URL] | (Incluso nei bulksheet generati a scopo informativo; non pubblicato sul motore di ricerca) Per gli account con URL di destinazione, si tratta dell’URL che collega un annuncio a un URL/pagina di destinazione di base sul sito web dell’inserzionista (a volte tramite un altro sito che tiene traccia del clic e quindi reindirizza l’utente alla pagina di destinazione). Include tutti i parametri di aggiunta configurati per la campagna o l’account Search, Social e Commerce. Se hai generato URL di tracciamento, questo si basa sui parametri di tracciamento riportati nelle impostazioni del tuo account e nelle impostazioni della campagna. Se hai aggiunto parametri specifici per i motori di ricerca, questi possono essere sostituiti con parametri equivalenti per Search, Social e Commerce.<br><br>Per gli account con URL finali, questa colonna mostra lo stesso valore della colonna URL di base/URL finale. |
| [!UICONTROL Custom URL Param] | Dati da sostituire alla variabile dinamica `{custom_code}` quando la variabile viene inclusa nei parametri di tracciamento per le impostazioni dell&#39;account di ricerca o della campagna. Per inserire il valore personalizzato nell’URL di tracciamento, devi caricare il file del bulksheet utilizzando l’opzione Genera URL di tracciamento. |
| [!UICONTROL Creative Type] | Formato annuncio: <i>[!UICONTROL Text ad]</i>, <i>[!UICONTROL Expanded text ad]</i>, <i>[!UICONTROL Demand Gen Carousel Ad]</i> (annunci carosello con più immagini), <i>[!UICONTROL Demand Gen Image Ad (single-image ads)]</i>, <i>[!UICONTROL Demand Gen Product Ad]</i> e <i>[!UICONTROL Demand Gen Video Ad]</i>, <i>[!UICONTROL Dynamic search ad]</i> (tipo annuncio obsoleto), <i>[!UICONTROL Expanded Dynamic Search ad]</i>, &lt;[!UICONTROL i>Display ad]</i>, <i>[!UICONTROL App Install ad]</i> (obsoleto), <i>[!UICONTROL Image]</i>, <i>[!UICONTROL Product ad<]/i> (annunci per acquisti) o <i>[!UICONTROL Responsive search ad]</i>. Il valore predefinito per i nuovi annunci è <i>[!UICONTROL Text ad]</i>.<br><br>Necessario per creare o modificare lo stato di un annuncio di prodotto. |
| [!UICONTROL Param1] | <p>Il valore numerico del parametro dell&#39;annuncio `{param1}`, che può essere incluso nella copia dell&#39;annuncio o nell&#39;URL di visualizzazione per qualsiasi annuncio nel file di bulksheet. La lunghezza massima è di 25 caratteri. È possibile includere i seguenti caratteri non numerici:</p><ul><li><p>Il valore può essere preceduto o accodato con un simbolo di valuta o un codice. Ad esempio, `£2.000,00` e `2000GBP` sono validi.</p></li><li><p>Il valore può includere una virgola (`,`) o un punto (`.`) come separatore, con un punto facoltativo (`.`) o una virgola (`,`) per i valori frazionari. Ad esempio, `1,000.00` e `2.000,10` sono validi.</p></li><li><p>Il valore può essere preceduto o aggiunto da un segno di percentuale (`%`), un segno più (`+`) o un segno meno (`- `). Ad esempio, `20%`, `208+` e `-42.32` sono validi.</p></li><li><p>È possibile incorporare due numeri con una barra. Ad esempio, `4/1` e `0.95/0.45` sono validi.</p></li></ul><p>Per eliminare il valore esistente, utilizzare il valore `[delete]` (comprese le parentesi).</p> |
| [!UICONTROL Param2] | Il valore numerico del parametro dell&#39;annuncio `{param2}`, che può essere incluso nella copia dell&#39;annuncio o nell&#39;URL di visualizzazione per qualsiasi annuncio nel file di bulksheet. Per ulteriori informazioni, vedere la voce relativa a Param1. |
| [!UICONTROL Audience] | L’elenco di remarketing per il pubblico di destinazione degli annunci di ricerca (RLSA) o il pubblico escluso per la campagna o il gruppo di annunci. Specifica se si tratta di una destinazione o di un’esclusione nel campo &quot;Tipo di destinazione&quot;. |
| [!UICONTROL Target Type] | (Quando viene specificato un pubblico) Indica se il pubblico specificato è un <i>Inclusione</i> (destinazione) o <i>Esclusione</i>. |
| [!UICONTROL Campaign Status] | Stato di visualizzazione della campagna: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, <i>[!UICONTROL Ended]</i> (non modificabile) o <i>[!UICONTROL Deleted]</i> (solo campagne esistenti). Il valore predefinito per le nuove campagne è <i>[!UICONTROL Active]</i>. Per eliminare una campagna attiva o in pausa, immettere il valore <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Ad Group Status] | Stato di visualizzazione del gruppo di annunci: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> o <i>[!UICONTROL Deleted]</i> (solo gruppi di annunci esistenti). Il valore predefinito per i nuovi gruppi di annunci è [!UICONTROL Active]. Per eliminare un gruppo di annunci attivo o in pausa, immettere il valore `Deleted`. |
| [!UICONTROL Keyword Status] | Stato di visualizzazione della parola chiave: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> o <i>[!UICONTROL Deleted]</i> (solo parole chiave esistenti). Il valore predefinito per le nuove parole chiave è [!UICONTROL Active]. Per eliminare una parola chiave attiva o in pausa, immettere il valore <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Ad Status] | Stato di visualizzazione dell&#39;annuncio: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Deleted]</i> (solo annunci esistenti), <i>[!UICONTROL Disapproved]</i> (non modificabile) o <i>[!UICONTROL Paused]</i>. Il valore predefinito per i nuovi annunci è [!UICONTROL Active]. Per eliminare un annuncio attivo o in pausa, immettere il valore <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Placement Status] | Stato del posizionamento del sito Web: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> o <i>[!UICONTROL Deleted]</i> (solo annunci esistenti). Il valore predefinito per i nuovi siti Web è <i>Attivo.</i> Per eliminare un posizionamento attivo o sospeso, immettere il valore <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Target Status] | Stato di una destinazione di ricerca dinamica: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> o <i>[!UICONTROL Deleted]</i> (solo destinazioni esistenti). Il valore predefinito per le nuove destinazioni è <i>Attivo.</i> Per eliminare una destinazione attiva o in pausa, immettere il valore <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Product Group Status] | Stato di visualizzazione del gruppo di prodotti: <i>[!UICONTROL Active]</i> <span>or</span> <i>[!UICONTROL Deleted]</i> (solo gruppi di prodotti esistenti). Il valore predefinito per i nuovi gruppi di prodotti è <i>[!UICONTROL Active]</i>. Per eliminare un gruppo di prodotti attivo, immettere il valore <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Sitelink Status] | Stato di visualizzazione del sitelink: <i>Attivo o Eliminato</i> (solo sitelink esistenti). Il valore predefinito per i nuovi sitelink è <i>[!UICONTROL Active]</i>. Per eliminare un sitelink attivo, immettere il valore <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Location Status] | Stato della destinazione del percorso: <i>[!UICONTROL Active]</i> o <i>[!UICONTROL Deleted]</i> (solo posizioni esistenti). Il valore predefinito per i nuovi percorsi è [!UICONTROL Active]. Per eliminare un percorso attivo, immettere il valore <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL RLSA Target Status] | Stato della destinazione o esclusione RLSA a livello di campagna o di gruppo di annunci: <i>[!UICONTROL Active]</i> o [!UICONTROL Deleted]</i> (solo destinazioni esistenti). Il valore predefinito per le nuove destinazioni o esclusioni è <i>[!UICONTROL Active]</i>. Per eliminare una destinazione attiva o un&#39;esclusione, immettere il valore <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Device Target Status] | <p>Stato della destinazione del dispositivo a livello di campagna o di gruppo di annunci: <i>[!UICONTROL Active]</i> o <i>[!UICONTROL Deleted]</i>. Per le nuove campagne e i nuovi gruppi di annunci, l&#39;impostazione predefinita è <i>[!UICONTROL Active]</i>.</p> |
| \[Classificazione etichetta specifica dell’inserzionista\] | (Nome per una classificazione di etichetta specifica dell’inserzionista, ad esempio &quot;Colore&quot; per una classificazione di etichetta denominata Colore) Valore per la classificazione specificata associata all’entità. Puoi includere un solo valore per classificazione per entità (ad esempio &quot;rosso&quot; per la classificazione dell’etichetta &quot;Colore&quot; per la campagna A). La lunghezza massima è di 100 caratteri e il valore può includere caratteri ASCII e non ASCII.<br><br>Le classificazioni delle etichette e i relativi valori vengono applicati a tutti i componenti figlio. I nuovi componenti aggiunti in seguito vengono associati automaticamente all&#39;etichetta. Le classificazioni delle etichette per i gruppi di prodotti vengono applicate al livello di unità (più granulare).<br><br>Né il nome della classificazione né il valore della classificazione fanno distinzione tra maiuscole e minuscole. |
| [!UICONTROL Constraints] | Vincolo assegnato all&#39;entità. È possibile assegnare un solo vincolo per entità.<br><b>>I vincoli vengono ereditati dalle entità figlio, pertanto non è necessario immettere valori per le entità figlio a meno che non si desideri ignorare i valori ereditati. |
| [!UICONTROL Campaign ID] | L’ID univoco che identifica una campagna esistente. Nei file CSV e TSV deve essere preceduto da virgolette singole (&#39;).[^1] Obbligatorio solo quando si modifica il nome della campagna, a meno che la riga non includa &quot;[!UICONTROL AMO ID]&quot; per la campagna. |
| [!UICONTROL Ad Group ID] | L’ID univoco che identifica un gruppo di annunci esistente. Nei file CSV e TSV deve essere preceduto da virgolette singole (&#39;).[^1] Obbligatorio solo quando si modifica il nome della campagna, a meno che la riga non includa &quot;[!UICONTROL AMO ID]&quot; per il gruppo di annunci. |
| [!UICONTROL Keyword ID] | ID univoco che identifica una parola chiave esistente. Nei file CSV e TSV deve essere preceduto da virgolette singole (&#39;).[^1] Obbligatorio solo quando si modifica la parola chiave, a meno che la riga non includa a) colonne di proprietà sufficienti per identificare la parola chiave o b) un &quot;[!UICONTROL AMO ID]&quot;.&quot; |
| [!UICONTROL Ad ID] | <p>ID univoco che identifica un annuncio esistente. Nei file CSV e TSV deve essere preceduto da virgolette singole (&#39;).[^1] Per gli annunci di ricerca responsive, è necessario l’ID annuncio o l’AMO ID per modificare o eliminare i dati dell’annuncio. Per tutti gli altri tipi di entità, l&#39;ID annuncio è richiesto solo quando si modifica lo stato dell&#39;annuncio, a meno che la riga non includa a) colonne di proprietà dell&#39;annuncio sufficienti per identificare l&#39;annuncio o b) un &quot;[!UICONTROL AMO ID]&quot;.&quot; Tuttavia, se non includi né [!UICONTROL Ad ID] né [!UICONTROL AMO ID] e le colonne della proprietà dell&#39;annuncio corrispondono a più annunci, lo stato di uno solo degli annunci cambia.</p><p><b>Nota:</b> se si modificano le colonne a) delle proprietà dell&#39;annuncio ad eccezione di Stato per un annuncio esistente o b) i dati per un annuncio di ricerca responsive e non si includono né [!UICONTROL Ad ID] né [!UICONTROL AMO ID], viene creato un nuovo annuncio e l&#39;annuncio esistente non viene modificato.</p> |
| [!UICONTROL Placement ID] | L’ID univoco che identifica il posizionamento di un sito web. Obbligatorio solo quando si modifica o si elimina il posizionamento, a meno che la riga non includa a) colonne di proprietà sufficienti per identificare il posizionamento o b) un &quot;[!UICONTROL AMO ID]&quot;.&quot; |
| [!UICONTROL Target ID] | ID univoco che identifica una destinazione automatica esistente. Obbligatorio solo quando si modifica o si elimina la destinazione automatica, a meno che la riga non includa &quot;[!UICONTROL AMO ID]&quot; per la destinazione. |
| [!UICONTROL Product Group ID] | ID univoco che identifica un gruppo di prodotti esistente. Nei file CSV e TSV deve essere preceduto da virgolette singole (&#39;).[^1] Obbligatorio solo quando si modifica o si elimina il gruppo di prodotti, a meno che la riga non includa a) colonne di proprietà sufficienti per identificare il gruppo di prodotti o b) un &quot;[!UICONTROL AMO ID]&quot;.&quot; |
| [!UICONTROL Sitelink ID] | ID univoco che identifica un sitelink esistente. Nei file CSV e TSV deve essere preceduto da virgolette singole (&#39;).[^1] Obbligatorio solo quando si modifica o si elimina il sitelink, a meno che la riga non includa a) colonne di proprietà sufficienti per identificare il sitelink o b) un &quot;[!UICONTROL AMO ID]&quot;.&quot; Tuttavia, se non includi né [!UICONTROL Sitelink ID] né [!UICONTROL AMO ID] e le colonne di proprietà corrispondono a più sitelink, lo stato di uno solo dei sitelink cambia.</p><p><b>Nota:</b> se si modificano le colonne delle proprietà del sitelink ad eccezione di Stato per un sitelink esistente e non si includono né [!UICONTROL Sitelink ID] né [!UICONTROL AMO ID], verrà creato un nuovo sitelink e il sitelink esistente non verrà modificato. |
| [!UICONTROL RLSA Target ID] | ID univoco che identifica una destinazione o un’esclusione RLSA a livello di campagna o di gruppo di annunci esistente. Nei file CSV e TSV deve essere preceduto da virgolette singole (&#39;).[^1] Obbligatorio solo quando si modifica o si elimina la destinazione o l&#39;esclusione, a meno che la riga non includa un &quot;[!UICONTROL AMO ID]&quot; per la destinazione. |
| [!UICONTROL Device Target ID] | <p>ID univoco che identifica una destinazione o un’esclusione dispositivo a livello di campagna o di gruppo di annunci esistente. Nei file CSV e TSV deve essere preceduto da virgolette singole (&#39;).[^1] Obbligatorio solo quando si modifica o si elimina la destinazione, a meno che la riga non includa un &quot;[!UICONTROL AMO ID]&quot; per la destinazione.</p> |
| [!UICONTROL AMO ID] | (Nei bulksheet generati) Identificatore univoco generato da Adobe per un’entità sincronizzata. Per gli annunci di ricerca responsive, l’AMO ID è necessario per modificare o eliminare gli annunci, a meno che tu non includa l’Ad ID. Per modificare i dati per tutti gli altri tipi di entità con un AMO ID, è necessario l’AMO ID per modificare o eliminare i dati, a meno che non si includano l’ID entità e l’ID entità principale.<br><br>Search, Social e Commerce utilizzano il valore per determinare l&#39;identità corretta da modificare, ma non pubblicano l&#39;ID sulla rete di annunci. |
| [!UICONTROL EF Error Message] | (Incluso nei bulksheet generati a scopo informativo) Segnaposto per la visualizzazione dei messaggi di errore provenienti dalla rete di annunci relativi ai dati nella riga. I messaggi di errore sono inclusi nei file [!UICONTROL EF Errors]. Questo valore non viene inviato alla rete di annunci. |
| [!UICONTROL SE Error Message] | (Incluso nei bulksheet generati a scopo informativo) Segnaposto per la visualizzazione dei messaggi di errore provenienti dalla rete di annunci relativi ai dati nella riga. I messaggi di errore sono inclusi nei file [!UICONTROL SE Errors]. Questo valore non viene inviato alla rete di annunci. |
| [!UICONTROL Exemption Request] | (Incluso nei bulksheet generati a scopo informativo) Segnaposto per la visualizzazione dei nomi e del testo di eventuali criteri pubblicitari [!DNL Google Ads] violati da un annuncio. |
| [!UICONTROL Retail Hash] | (Incluso a scopo informativo nei bulksheet generati utilizzando Advanced Campaign Management) Un codice hash alfanumerico (ad esempio f9639f40cdf56524b541e5dacf55a991) che indica che l’elemento è stato generato utilizzando la vista Avanzate (ACM). |

[^1]: [!DNL Excel] converte i numeri elevati in notazione scientifica (ad esempio 2,12E+09 per 2115585666) quando apre il file. Per visualizzare le cifre nella notazione standard, selezionare una cella della colonna e fare clic all&#39;interno della barra della formula.

## Campi necessari per creare, modificare o eliminare ciascun componente conto {#bulksheet-fields-per-component-google}

Nelle sezioni seguenti sono inclusi i campi relativi a entità conto specifiche.

>[!NOTE]
>
>Quando un campo non è applicabile a un’azione, qualsiasi valore inserito nel campo viene ignorato.

### Campi della campagna

Per una descrizione di ogni campo dati, vedere &quot;[Tutti i campi dati disponibili](#bulksheet-fields-all-google).&quot;

| Campo | Obbligatorio |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obbligatorio a meno che ogni riga non includa &quot;[!UICONTROL AMO ID]&quot; per l&#39;entità. |
| [!UICONTROL Campaign Name] | Obbligatorio |
| [!UICONTROL Campaign Budget] | Obbligatorio per creare una campagna. |
| [!UICONTROL Delivery Method] | Obbligatorio per creare una campagna. |
| [!UICONTROL Channel Type] | Obbligatorio per creare una campagna. |
| [!UICONTROL Networks] | Obbligatorio per creare una campagna. |
| [!UICONTROL DSA Domain Name] | Necessario per creare una campagna con annunci di ricerca dinamici sulla rete di ricerca. |
| [!UICONTROL DSA Domain Language] | Necessario per creare una campagna con annunci di ricerca dinamici sulla rete di ricerca. |
| [!UICONTROL Campaign Priority] | Obbligatorio per creare una campagna acquisti. |
| [!UICONTROL Merchant ID] | Obbligatorio per creare una campagna acquisti. |
| [!UICONTROL Sales Country] | Obbligatorio per creare una campagna acquisti. |
| [!UICONTROL Product Scope Filter] | (Campagne commerciali) Facoltativo |
| [!UICONTROL Languages] | Facoltativo |
| [!UICONTROL Device Targets] | Facoltativo |
| [!UICONTROL Device Targets (Google Adwords)] | Facoltativo |
| [!UICONTROL Mobile Carriers (Google Adwords)] | Facoltativo |
| [!UICONTROL Audience Target Method] | n/d |
| [!UICONTROL Landing Page Suffix] | Facoltativo |
| [!UICONTROL Tracking Template] | Facoltativo |
| [!UICONTROL Campaign Status] | Obbligatorio solo per eliminare una campagna. |
| \[Classificazione etichetta specifica dell’inserzionista\] | Facoltativo |
| [!UICONTROL Constraints] | Facoltativo |
| [!UICONTROL Campaign ID] | Obbligatorio solo quando si modifica il nome della campagna, a meno che la riga non includa &quot;[!UICONTROL AMO ID]&quot; per la campagna. |
| [!UICONTROL AMO ID] | Obbligatorio per modificare o eliminare i dati a meno che non si includano l’ID entità e l’ID entità padre.<br><br>Search, Social e Commerce utilizzano il valore per determinare l&#39;identità corretta da modificare, ma non pubblicano l&#39;ID sulla rete di annunci. |

### Campi del gruppo di annunci

Per una descrizione di ogni campo dati, vedere &quot;[Tutti i campi dati disponibili](#bulksheet-fields-all-google).&quot;

| Campo | Obbligatorio |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obbligatorio a meno che ogni riga non includa &quot;[!UICONTROL AMO ID]&quot; per l&#39;entità. |
| [!UICONTROL Campaign Name] | Obbligatorio |
| [!UICONTROL Networks] | n/d |
| [!UICONTROL GDN Custom Bid Level] | Facoltativo |
| [!UICONTROL Ad Group Name] | Obbligatorio |
| [!UICONTROL Ad Group Type] | Obbligatorio per creare un gruppo di annunci. |
| [!UICONTROL Max CPC] | Facoltativo |
| [!UICONTROL Max Content CPC] | Facoltativo |
| [!UICONTROL Audience Target Method] | Obbligatorio |
| [!UICONTROL Tracking Template] | Facoltativo |
| [!UICONTROL Ad Group Status] | Richiesto solo per eliminare un gruppo di annunci. |
| \[Classificazione etichetta specifica dell’inserzionista\] | Facoltativo |
| [!UICONTROL Constraints] | Facoltativo |
| [!UICONTROL Ad Group ID] | Obbligatorio solo quando si modifica il nome del gruppo di annunci, a meno che la riga non includa &quot;[!UICONTROL AMO ID]&quot; per il gruppo di annunci. |
| [!UICONTROL AMO ID] | Obbligatorio per modificare o eliminare i dati a meno che non si includano l’ID entità e l’ID entità padre.<br><br>Search, Social e Commerce utilizzano il valore per determinare l&#39;identità corretta da modificare, ma non pubblicano l&#39;ID sulla rete di annunci. |

### Campi parola chiave

Per una descrizione di ogni campo dati, vedere &quot;[Tutti i campi dati disponibili](#bulksheet-fields-all-google).&quot;

| Campo | Obbligatorio |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obbligatorio a meno che ogni riga non includa &quot;[!UICONTROL AMO ID]&quot; per l&#39;entità. |
| [!UICONTROL Campaign Name] | Obbligatorio |
| [!UICONTROL Ad Group Name] | Obbligatorio |
| [!UICONTROL Max CPC] | Facoltativo |
| [!UICONTROL Keyword] | Obbligatorio |
| [!UICONTROL Match Type] | Per modificare o eliminare una parola chiave con più tipi di corrispondenza è necessario un valore per il tipo di corrispondenza o l’ID della parola chiave. |
| [!UICONTROL Tracking Template] | Facoltativo |
| [!UICONTROL Base URL/Final URL] | Facoltativo |
| [!UICONTROL Custom URL Param] | Facoltativo |
| [!UICONTROL Param1] | Facoltativo |
| [!UICONTROL Param2] | Facoltativo |
| [!UICONTROL Keyword Status] | Obbligatorio solo per eliminare una parola chiave. |
| \[Classificazione etichetta specifica dell’inserzionista\] | Facoltativo |
| [!UICONTROL Constraints] | Facoltativo |
| [!UICONTROL Campaign ID] | Facoltativo |
| [!UICONTROL Ad Group ID] | Facoltativo |
| [!UICONTROL Keyword ID] | Obbligatorio solo quando si modifica o si elimina la parola chiave, a meno che la riga non includa a) colonne di proprietà sufficienti per identificare la parola chiave o b) un &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | Obbligatorio per modificare o eliminare i dati a meno che non si includano l’ID entità e l’ID entità padre.<br><br>Search, Social e Commerce utilizzano il valore per determinare l&#39;identità corretta da modificare, ma non pubblicano l&#39;ID sulla rete di annunci. |

### Campi di posizionamento

Per una descrizione di ogni campo dati, vedere &quot;[Tutti i campi dati disponibili](#bulksheet-fields-all-google).&quot;

| Campo | Obbligatorio |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obbligatorio a meno che ogni riga non includa &quot;[!UICONTROL AMO ID]&quot; per l&#39;entità. |
| [!UICONTROL Campaign Name] | Obbligatorio |
| [!UICONTROL Ad Group Name] | Obbligatorio |
| [!UICONTROL Max Placement CPC (Google Adwords)] | Facoltativo |
| [!UICONTROL Max Placement CPM (Google Adwords)] | Facoltativo |
| [!UICONTROL Placement] | Obbligatorio |
| [!UICONTROL Match Type] | Obbligatorio |
| [!UICONTROL Tracking Template] | Facoltativo |
| [!UICONTROL Base URL/Final URL] | Facoltativo |
| [!UICONTROL Custom URL Param] | Facoltativo |
| [!UICONTROL Placement Status] | Obbligatorio solo per eliminare un posizionamento. |
| \[Classificazione etichetta specifica dell’inserzionista\] | Facoltativo |
| [!UICONTROL Constraints] | Facoltativo |
| [!UICONTROL Campaign ID] | Facoltativo |
| [!UICONTROL Ad Group ID] | Facoltativo |
| [!UICONTROL Placement ID] | Obbligatorio solo quando si modifica o si elimina il posizionamento, a meno che la riga non includa a) colonne di proprietà sufficienti per identificare il posizionamento o b) un &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | Obbligatorio per modificare o eliminare i dati a meno che non si includano l’ID entità e l’ID entità padre.<br><br>Search, Social e Commerce utilizzano il valore per determinare l&#39;identità corretta da modificare, ma non pubblicano l&#39;ID sulla rete di annunci. |

### Annuncio per ricerca dinamica espanso

Questo tipo di annuncio è ora denominato &quot;annuncio di ricerca dinamica&quot; in [!DNL Google Ads]. Per ulteriori informazioni sulla creazione di annunci per ricerca dinamica, vedi &quot;[Implementare [!DNL Google Ads] annunci per ricerca dinamica](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-workflows/google-dynamic-search-ads.html?lang=it).&quot;

Per questo tipo di annuncio, utilizzare la riga &quot;[!UICONTROL Creative (except RSA)]&quot; nella finestra di dialogo [!UICONTROL Download Bulksheet].

Per una descrizione di ogni campo dati, vedere &quot;[Tutti i campi dati disponibili](#bulksheet-fields-all-google).&quot;

| Campo | Obbligatorio |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obbligatorio a meno che ogni riga non includa &quot;[!UICONTROL AMO ID]&quot; per l&#39;entità. |
| [!UICONTROL Campaign Name] | Obbligatorio |
| [!UICONTROL Ad Group Name] | Obbligatorio |
| [!UICONTROL Creative Preferred Devices] | Facoltativo |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] | Obbligatorio per creare un annuncio o modificare la descrizione. <b>Nota:</b> Per questo tipo di annuncio, la modifica della copia dell&#39;annuncio elimina l&#39;annuncio esistente e ne crea uno nuovo. |
| [!UICONTROL Display URL] | Obbligatorio |
| [!UICONTROL Tracking Template] | Facoltativo |
| [!UICONTROL Creative Type] | Obbligatorio per creare o modificare lo stato di un annuncio di prodotto. |
| [!UICONTROL Ad Status] | Obbligatorio per eliminare un annuncio. |
| \[Classificazione etichetta specifica dell’inserzionista\] | Facoltativo |
| [!UICONTROL Campaign ID] | Facoltativo |
| [!UICONTROL Ad Group ID] | Facoltativo |
| [!UICONTROL Ad ID] | Obbligatorio solo quando si modifica lo stato dell&#39;annuncio, a meno che la riga non includa a) un numero sufficiente di colonne di proprietà dell&#39;annuncio per identificare l&#39;annuncio oppure b) un &quot;[!UICONTROL AMO ID]&quot;. Tuttavia, se non includi né [!UICONTROL Ad ID] né [!UICONTROL AMO ID] e le colonne della proprietà dell&#39;annuncio corrispondono a più annunci, lo stato di uno solo degli annunci cambia. |
| [!UICONTROL AMO ID] | Obbligatorio per modificare o eliminare i dati a meno che non si includano l’ID entità e l’ID entità padre.<br><br>Search, Social e Commerce utilizzano il valore per determinare l&#39;identità corretta da modificare, ma non pubblicano l&#39;ID sulla rete di annunci. |

### Campi per annunci di acquisto/elenco prodotti

Per ulteriori informazioni sulla creazione di annunci per acquisti, consulta &quot;[Implementare [!DNL Google Ads] campagne acquisti](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-workflows/google-shopping-campaigns.html?lang=it).&quot;

Per questo tipo di annuncio, utilizzare la riga &quot;[!UICONTROL Creative (except RSA)]&quot; nella finestra di dialogo [!UICONTROL Download Bulksheet].

Per una descrizione di ogni campo dati, vedere &quot;[Tutti i campi dati disponibili](#bulksheet-fields-all-google).&quot;

| Campo | Obbligatorio |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obbligatorio a meno che ogni riga non includa &quot;[!UICONTROL AMO ID]&quot; per l&#39;entità. |
| [!UICONTROL Campaign Name] | Obbligatorio |
| [!UICONTROL Ad Group Name] | Obbligatorio |
| [!UICONTROL Promotion Line] | Facoltativo |
| [!UICONTROL Tracking Template] | Facoltativo |
| [!UICONTROL Base URL/Final URL] | Facoltativo |
| [!UICONTROL Custom URL Param] | Facoltativo |
| [!UICONTROL Creative Type] | Obbligatorio per creare o modificare lo stato di un annuncio di prodotto. |
| [!UICONTROL Ad Status] | Obbligatorio per eliminare un annuncio. |
| \[Classificazione etichetta specifica dell’inserzionista\] | Facoltativo |
| [!UICONTROL Constraints] | Facoltativo |
| [!UICONTROL Campaign ID] | Facoltativo |
| [!UICONTROL Ad Group ID] | Facoltativo |
| [!UICONTROL Ad ID] | Obbligatorio solo quando si modifica lo stato dell&#39;annuncio, a meno che la riga non includa a) un numero sufficiente di colonne di proprietà dell&#39;annuncio per identificare l&#39;annuncio oppure b) un &quot;[!UICONTROL AMO ID]&quot;. Tuttavia, se non includi né [!UICONTROL Ad ID] né [!UICONTROL AMO ID] e le colonne della proprietà dell&#39;annuncio corrispondono a più annunci, lo stato di uno solo degli annunci cambia. |
| [!UICONTROL AMO ID] | Obbligatorio per modificare o eliminare i dati a meno che non si includano l’ID entità e l’ID entità padre.<br><br>Search, Social e Commerce utilizzano il valore per determinare l&#39;identità corretta da modificare, ma non pubblicano l&#39;ID sulla rete di annunci. |

### Campi degli annunci di ricerca reattivi

Per questo tipo di annuncio, utilizzare la riga &quot;[!UICONTROL Responsive Search Ad]&quot; nella finestra di dialogo [!UICONTROL Download Bulksheet].

Per una descrizione di ogni campo dati, vedere &quot;[Tutti i campi dati disponibili](#bulksheet-fields-all-google).&quot;

| Campo | Obbligatorio |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obbligatorio a meno che ogni riga non includa &quot;[!UICONTROL AMO ID]&quot; per l&#39;entità. |
| [!UICONTROL Campaign Name] | Obbligatorio |
| [!UICONTROL Ad Group Name] | Obbligatorio |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-15 | Per gli annunci di ricerca responsive, sono necessari [!UICONTROL Ad Title], [!UICONTROL Ad Title 2] e [!UICONTROL Ad Title 3] per creare un annuncio e tutti gli altri campi del titolo dell&#39;annuncio sono facoltativi. Per eliminare il valore esistente per un campo non obbligatorio, utilizzare il valore `[delete]` (comprese le parentesi). |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | Facoltativo |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | Per gli annunci di ricerca responsive, sono necessari [!UICONTROL Description Line 1] e [!UICONTROL Description Line 2] per creare un annuncio e [!UICONTROL Description Line 3] e [!UICONTROL Description Line 4] sono facoltativi. Per eliminare il valore esistente, utilizzare il valore `[delete]` (comprese le parentesi). |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | Facoltativo |
| [!UICONTROL Display Path 1] | Facoltativo |
| [!UICONTROL Display Path 2] | Facoltativo |
| [!UICONTROL Tracking Template] | Facoltativo |
| [!UICONTROL Base URL/Final URL] | Obbligatorio per creare un annuncio. |
| [!UICONTROL Custom URL Param] | Facoltativo |
| [!UICONTROL Creative Type] | Facoltativo |
| [!UICONTROL Ad Status] | Obbligatorio per eliminare un annuncio. |
| \[Classificazione etichetta specifica dell’inserzionista\] | Facoltativo |
| [!UICONTROL Campaign ID] | Facoltativo |
| [!UICONTROL Ad Group ID] | Facoltativo |
| [!UICONTROL Ad ID] | Necessario per modificare o eliminare gli annunci a meno che la riga non includa un &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | Obbligatorio per modificare o eliminare gli annunci a meno che non includa l’ID annuncio. |

### Campi di annunci di testo

Per questo tipo di annuncio, utilizzare la riga &quot;[!UICONTROL Creative (except RSA)]&quot; nella finestra di dialogo [!UICONTROL Download Bulksheet].

Per una descrizione di ogni campo dati, vedere &quot;[Tutti i campi dati disponibili](#bulksheet-fields-all-google).&quot;

>[!NOTE]
>
>Gli annunci di testo espansi sono stati dichiarati obsoleti a giugno 2022. Puoi eliminare solo gli annunci di testo esistenti.

| Campo | Obbligatorio |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obbligatorio a meno che ogni riga non includa &quot;[!UICONTROL AMO ID]&quot; per l&#39;entità. |
| [!UICONTROL Campaign Name] | Obbligatorio |
| [!UICONTROL Ad Group Name] | Obbligatorio |
| [!UICONTROL Creative Preferred Devices] | Sola lettura |
| [!UICONTROL Ad Title], Titolo annuncio 2-3 | Sola lettura |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] | Sola lettura |
| [!UICONTROL Display URL] | Sola lettura |
| [!UICONTROL Display Path 1] | Sola lettura |
| [!UICONTROL Display Path 2] | Sola lettura |
| [!UICONTROL Tracking Template] | Sola lettura |
| [!UICONTROL Base URL/Final URL] | Sola lettura |
| [!UICONTROL Custom URL Param] | Sola lettura |
| [!UICONTROL Creative Type] | Facoltativo |
| [!UICONTROL Ad Status] | Obbligatorio |
| \[Classificazione etichetta specifica dell’inserzionista\] | Facoltativo |
| [!UICONTROL Campaign ID] | Facoltativo |
| [!UICONTROL Ad Group ID] | Facoltativo |
| [!UICONTROL Ad ID] | Obbligatorio solo quando si modifica lo stato dell&#39;annuncio, a meno che la riga non includa a&rpar; colonne di proprietà dell&#39;annuncio sufficienti per identificare l&#39;annuncio o b&rpar; e &quot;[!UICONTROL AMO ID]&quot;. Tuttavia, se non includi né [!UICONTROL Ad ID] né [!UICONTROL AMO ID] e le colonne della proprietà dell&#39;annuncio corrispondono a più annunci, lo stato di uno solo degli annunci cambia. |
| [!UICONTROL AMO ID] | Obbligatorio per modificare o eliminare i dati a meno che non si includano l’ID entità e l’ID entità padre.<br><br>Search, Social e Commerce utilizzano il valore per determinare l&#39;identità corretta da modificare, ma non pubblicano l&#39;ID sulla rete di annunci. |

### Campi destinazione ricerca dinamica (targeting automatico)

Per una descrizione di ogni campo dati, vedere &quot;[Tutti i campi dati disponibili](#bulksheet-fields-all-google).&quot;

| Campo | Obbligatorio |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obbligatorio a meno che ogni riga non includa &quot;[!UICONTROL AMO ID]&quot; per l&#39;entità. |
| [!UICONTROL Campaign Name] | Obbligatorio |
| [!UICONTROL Ad Group Name] | Obbligatorio |
| [!UICONTROL Max CPC] | Facoltativo |
| [!UICONTROL Auto Target Expression] | Obbligatorio solo quando l&#39;impostazione della campagna su &quot;[!UICONTROL Use my website contents to target my ads]&quot; non è abilitata. |
| [!UICONTROL Match Type] | Facoltativo |
| [!UICONTROL Target Status] | Necessario per eliminare una destinazione |
| \[Classificazione etichetta specifica dell’inserzionista\] | Facoltativo |
| [!UICONTROL Constraints] | Facoltativo |
| [!UICONTROL Campaign ID] | Facoltativo |
| [!UICONTROL Ad Group ID] | Facoltativo |
| [!UICONTROL Target ID] | Obbligatorio solo quando si modifica o si elimina la destinazione automatica, a meno che la riga non includa &quot;[!UICONTROL AMO ID]&quot; per la destinazione. |
| [!UICONTROL AMO ID] | Obbligatorio per modificare o eliminare i dati a meno che non si includano l’ID entità e l’ID entità padre.<br><br>Search, Social e Commerce utilizzano il valore per determinare l&#39;identità corretta da modificare, ma non pubblicano l&#39;ID sulla rete di annunci. |

### Campi gruppo di prodotti acquisti

Per una descrizione di ogni campo dati, vedere &quot;[Tutti i campi dati disponibili](#bulksheet-fields-all-google).&quot;

| Campo | Obbligatorio |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obbligatorio a meno che ogni riga non includa &quot;[!UICONTROL AMO ID]&quot; per l&#39;entità. |
| [!UICONTROL Campaign Name] | Obbligatorio |
| [!UICONTROL Ad Group Name] | Obbligatorio |
| [!UICONTROL Max CPC] | Obbligatorio per creare un gruppo di prodotti. |
| [!UICONTROL Parent Product Groupings] | Obbligatorio |
| [!UICONTROL Product Grouping] | Obbligatorio |
| [!UICONTROL Partition Type] | Obbligatorio per creare un gruppo di prodotti. |
| [!UICONTROL Match Type] | Facoltativo |
| [!UICONTROL Tracking Template] | Facoltativo |
| [!UICONTROL Base URL/Final URL] | Obbligatorio |
| [!UICONTROL Product Group Status] | Obbligatorio solo per eliminare un gruppo di prodotti. |
| \[Classificazione etichetta specifica dell’inserzionista\] | Facoltativo |
| [!UICONTROL Constraints] | Facoltativo |
| [!UICONTROL Campaign ID] | Facoltativo |
| [!UICONTROL Ad Group ID] | Facoltativo |
| [!UICONTROL Product Group ID] | Obbligatorio solo quando si modifica o si elimina il gruppo di prodotti, a meno che la riga non includa a) colonne di proprietà sufficienti per identificare il gruppo di prodotti o b) un &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | Obbligatorio per modificare o eliminare i dati a meno che non si includano l’ID entità e l’ID entità padre.<br><br>Search, Social e Commerce utilizzano il valore per determinare l&#39;identità corretta da modificare, ma non pubblicano l&#39;ID sulla rete di annunci. |

### Campi sitelink a livello di campagna e di gruppo di annunci

Per una descrizione di ogni campo dati, vedere &quot;[Tutti i campi dati disponibili](#bulksheet-fields-all-google).&quot;

| Campo | Obbligatorio |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obbligatorio a meno che ogni riga non includa &quot;[!UICONTROL AMO ID]&quot; per l&#39;entità. |
| [!UICONTROL Campaign Name] | Obbligatorio |
| [!UICONTROL Ad Group Name] | Obbligatorio per i sitelink a livello di gruppo di annunci. Non applicabile per i sitelink a livello di campagna. |
| [!UICONTROL Creative Preferred Devices] | Facoltativo |
| [!UICONTROL Link Name] | Obbligatorio |
| [!UICONTROL Start Date] | Facoltativo |
| [!UICONTROL End Date] | Facoltativo |
| [!UICONTROL Tracking Template] | Facoltativo |
| [!UICONTROL Base URL/Final URL] | Obbligatorio |
| [!UICONTROL Sitelink Status] | Obbligatorio solo per eliminare un sitelink. |
| [!UICONTROL Campaign ID] | Facoltativo |
| [!UICONTROL Ad Group ID] | Facoltativo |
| [!UICONTROL Sitelink ID] | Obbligatorio solo quando si modifica o si elimina il sitelink, a meno che la riga non includa a) colonne di proprietà sufficienti per identificare il sitelink o b) un &quot;[!UICONTROL AMO ID]&quot;. Tuttavia, se non includi né [!UICONTROL Sitelink ID] né [!UICONTROL AMO ID] e le colonne di proprietà corrispondono a più sitelink, lo stato di uno solo dei sitelink cambia.<br><br><b>Nota:</b> se si modificano le colonne delle proprietà del sitelink ad eccezione di [!UICONTROL Status] per un sitelink esistente e non si includono [!UICONTROL Sitelink ID] né [!UICONTROL AMO ID], verrà creato un nuovo sitelink e il sitelink esistente non verrà modificato. |
| [!UICONTROL AMO ID] | Obbligatorio per modificare o eliminare i dati a meno che non si includano l’ID entità e l’ID entità padre.<br><br>Search, Social e Commerce utilizzano il valore per determinare l&#39;identità corretta da modificare, ma non pubblicano l&#39;ID sulla rete di annunci. |

### Destinazione posizione

Per una descrizione di ogni campo dati, vedere &quot;[Tutti i campi dati disponibili](#bulksheet-fields-all-google).&quot;

| Campo | Obbligatorio |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obbligatorio a meno che ogni riga non includa &quot;[!UICONTROL AMO ID]&quot; per l&#39;entità. |
| [!UICONTROL Campaign Name] | Obbligatorio |
| [!UICONTROL Location] | Obbligatorio |
| [!UICONTROL Location Type] | Facoltativo |
| [!UICONTROL Bid Adjustment] | Facoltativo |
| [!UICONTROL Location Status] | Obbligatorio solo per eliminare una destinazione di posizione. |
| [!UICONTROL Campaign ID] | Facoltativo |
| [!UICONTROL AMO ID] | Necessario per modificare o eliminare i dati a meno che non si includa [!UICONTROL Campaign ID].<br><br>Search, Social e Commerce utilizzano il valore per determinare l&#39;identità corretta da modificare, ma non pubblicano l&#39;ID sulla rete di annunci. |

### Campi di destinazione per dispositivi a livello di campagna e di gruppo di annunci

Per una descrizione di ogni campo dati, vedere &quot;[Tutti i campi dati disponibili](#bulksheet-fields-all-google).&quot;

| Campo | Obbligatorio |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obbligatorio a meno che ogni riga non includa &quot;[!UICONTROL AMO ID]&quot; per l&#39;entità. |
| [!UICONTROL Campaign Name] | Obbligatorio |
| [!UICONTROL Device] | Necessario per creare o modificare una destinazione dispositivo. |
| [!UICONTROL Bid Adjustment] | Facoltativo |
| [!UICONTROL Ad Group Name] | Obbligatorio per le destinazioni dei dispositivi a livello di gruppo di annunci. Non applicabile per i target dispositivo a livello di campagna. |
| [!UICONTROL Device Target Status] | Obbligatorio solo per eliminare una destinazione dispositivo. |
| [!UICONTROL Campaign ID] | Facoltativo |
| [!UICONTROL Ad Group ID] | Facoltativo; applicabile solo per destinazioni dispositivo a livello di gruppo di annunci. |
| [!UICONTROL Device Target ID] | Obbligatorio solo quando si modifica o si elimina la destinazione, a meno che la riga non includa &quot;[!UICONTROL AMO ID]&quot; per la destinazione. |
| [!UICONTROL AMO ID] | Necessario per modificare o eliminare i dati a meno che non includiate l&#39;ID Device Target.<br><br>Search, Social e Commerce utilizzano il valore per determinare l&#39;identità corretta da modificare, ma non pubblicano l&#39;ID sulla rete di annunci. |

### Campi di destinazione/esclusione RLSA a livello di campagna e di gruppo di annunci

Per una descrizione di ogni campo dati, vedere &quot;[Tutti i campi dati disponibili](#bulksheet-fields-all-google).&quot;

| Campo | Obbligatorio |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obbligatorio a meno che ogni riga non includa &quot;[!UICONTROL AMO ID]&quot; per l&#39;entità. |
| [!UICONTROL Campaign Name] | Obbligatorio |
| [!UICONTROL Bid Adjustment] | Facoltativo |
| [!UICONTROL Ad Group Name] | Obbligatorio per destinazioni ed esclusioni a livello di gruppo di annunci. Non applicabile per target ed esclusioni a livello di campagna. |
| [!UICONTROL Audience] | Obbligatorio per creare una nuova destinazione o esclusione. |
| [!UICONTROL Target Type] | Obbligatorio per creare una nuova destinazione o esclusione. |
| [!UICONTROL RLSA Target Status] | Obbligatorio solo per eliminare una destinazione o un’esclusione. |
| [!UICONTROL Campaign ID] | Facoltativo |
| [!UICONTROL Ad Group ID] | Facoltativo; applicabile solo per target ed esclusioni a livello di gruppo di annunci. |
| [!UICONTROL RLSA Target ID] | Obbligatorio solo quando si modifica o si elimina la destinazione, a meno che la riga non includa &quot;[!UICONTROL AMO ID]&quot; per la destinazione. |
| [!UICONTROL AMO ID] | Necessario per modificare o eliminare i dati a meno che non si includa l&#39;ID destinazione RLSA.<br><br>Search, Social e Commerce utilizzano il valore per determinare l&#39;identità corretta da modificare, ma non pubblicano l&#39;ID sulla rete di annunci. |

>[!MORELIKETHIS]
>
>* [Appendice - Errori bulksheet](../bulksheet-errors.md)
>* [Operazioni eseguibili nei bulksheet](bulksheet-operations.md)
>* [Formati di file di bulksheet supportati](bulksheet-file-formats.md)
>* [Scaricare/creare un file bulksheet](../bulksheet-download.md)
>* [Formati di tracciamento dei clic per [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [Caricare un file di bulksheet o un file di errore corretto](../bulksheet-upload.md)
