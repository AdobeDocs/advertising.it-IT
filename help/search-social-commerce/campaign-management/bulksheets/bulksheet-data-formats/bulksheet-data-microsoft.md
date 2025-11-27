---
title: Dati bulksheet richiesti per  [!DNL Microsoft Advertising]  account
description: Fai riferimento ai campi di intestazione e ai campi dati obbligatori nei bulksheet per  [!DNL Microsoft Advertising]  account.
exl-id: 2a5f0e7b-f020-4cca-9b77-807c2ee5c273
feature: Search Bulksheets
source-git-commit: 3ab2e38f6a2f70c03504363575b13dc0dc730282
workflow-type: tm+mt
source-wordcount: '6928'
ht-degree: 0%

---

# Appendice - Dati bulksheet richiesti per i conti [!DNL Microsoft Advertising]

Per creare e aggiornare in blocco i dati della campagna [!DNL Microsoft Advertising], è possibile utilizzare i file di bulksheet di Search, Social e Commerce formattati specificamente per gli account [!DNL Microsoft Advertising]. È possibile: a) [generare file di fogli collettivi per gli account esistenti](../bulksheet-download.md) nel formato di file richiesto oppure b) crearli manualmente (vedere &quot;[Formati di file di fogli collettivi supportati](bulksheet-file-formats.md)&quot; per informazioni generali sui formati di file supportati).

Ogni bulksheet deve includere i campi intestazione e i campi dati corrispondenti necessari per le [operazioni specifiche che si desidera eseguire](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-operations.md) (ad esempio la creazione di un annuncio). Quando un campo non è obbligatorio, puoi ometterlo dall’intestazione e dalle righe di dati. Tutte le colonne personalizzate vengono eliminate quando caricate il file di foglio ausiliario.

Di seguito è riportata una tabella di tutti i campi dati disponibili e le tabelle aggiuntive che indicano quali campi sono necessari per aggiungere, modificare o eliminare dati per singole entità (ad esempio campagne e parole chiave).

## Tutti i campi dati disponibili {#bulksheet-fields-all-microsoft}

Nella tabella seguente sono descritti tutti i campi dati disponibili.

Per i campi dati relativi alle entità account, vedere &quot;[Campi necessari per creare, modificare o eliminare ogni componente account](#bulksheet-fields-per-component-microsoft).&quot;

| Campo | Descrizione |
|----|----|
| [!UICONTROL Platform] | (Incluso nei bulksheet generati a scopo informativo) La piattaforma pubblicitaria. Obbligatorio a meno che ogni riga non includa &quot;[!UICONTROL AMO ID]&quot; per l&#39;entità. |
| [!UICONTROL Acct Name] | Nome univoco che identifica un account di rete di annunci. Obbligatorio a meno che ogni riga non includa &quot;[!UICONTROL AMO ID]&quot; per l&#39;entità. |
| [!UICONTROL Campaign Name] | Il nome univoco che identifica una campagna per un account. La lunghezza massima è di 128 caratteri. |
| [!UICONTROL Campaign Budget] | Il budget giornaliero o mensile della campagna, con o senza simboli monetari e punteggiatura. Non può essere inferiore a 0,05. |
| [!UICONTROL Channel Type] | Tipo di canale di destinazione della campagna: <i>[!UICONTROL Audience]</i>, <i>[!UICONTROL DynamicSearchAds]</i>, <i>[!UICONTROL Search]</i> o <i>[!UICONTROL Shopping]</i>. |
| [!UICONTROL Delivery Method] | (Solo campagne con budget giornalieri) Quanto rapidamente vengono visualizzati gli annunci per la campagna ogni giorno:<ul><li><i>[!UICONTROL Standard (Distributed)]</i> (impostazione predefinita per le nuove campagne): per distribuire le impression pubblicitarie nell&#39;arco della giornata.</li><li><i>[!UICONTROL Accelerated]:</i> Per visualizzare gli annunci il più spesso possibile fino al raggiungimento del budget. Di conseguenza, i tuoi annunci potrebbero non essere visualizzati più avanti nella giornata.</li></ul> |
| [!UICONTROL Campaign Priority] | (Solo campagne acquisti) La priorità con cui viene utilizzata la campagna quando più campagne pubblicizzano lo stesso prodotto: <i>[!UICONTROL Low]</i> (impostazione predefinita per le nuove campagne), <i>[!UICONTROL Medium]</i> o <i>[!UICONTROL High]</i>.<br><br>Quando lo stesso prodotto è incluso in più campagne, la rete di annunci utilizza per prima cosa la priorità della campagna per determinare quale campagna (e l&#39;offerta associata) è idonea per l&#39;asta di annunci. Se tutte le campagne hanno la stessa priorità, la campagna con l’offerta più elevata è idonea. |
| [!UICONTROL Merchant ID] | (Campagne commerciali e campagne di pubblico collegate solo a un feed esercente) L’ID cliente dell’account esercente i cui prodotti vengono utilizzati per la campagna. |
| [!UICONTROL Sales Country] | (Solo campagne commerciali; sola lettura per le campagne esistenti) Il paese in cui vengono venduti i prodotti della campagna. Poiché i prodotti sono associati ai paesi di destinazione, questa impostazione determina quali prodotti vengono pubblicizzati nella campagna. |
| [!UICONTROL Product Scope Filter] | (Solo campagne che utilizzano la rete di acquisto) I prodotti nel tuo account esercente per i quali è possibile creare annunci di prodotto per la campagna. Puoi immettere fino a sette combinazioni di dimensioni e attributi di prodotto su cui filtrare i prodotti, utilizzando il formato dimension=attribute. Separa più filtri con un delimitatore &quot;>>&quot;. Per un elenco delle dimensioni di prodotto disponibili, consulta &quot;[Filtri di prodotto per campagne acquisti](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md).&quot;<br><br> Esempio: &quot;`CategoryL1==Animals & Pet Supplies>>CategoryL2=Pet Supplies>>Brand=Acme Pet Supplies`&quot;<br><br> Per eliminare i valori esistenti, utilizzare il valore `[delete]` (comprese le parentesi). |
| [!UICONTROL DSA Domain Name] | (Campagne di tipo a) &quot;<i>[!UICONTROL DynamicSearchAds]</i>&quot; o b) &quot;<i>[!UICONTROL Search]</i>&quot; quando l&#39;elemento [!DNL ExperimentId] non è impostato) Il nome di dominio del sito Web di destinazione per gli annunci di ricerca dinamica. La lunghezza massima è di 2.048 caratteri. Se il nome di dominio include `www`, verrà tagliato e non utilizzato.<br><br>Per le campagne esistenti non è possibile modificare il dominio, ma è necessario includerlo per aggiornare altre proprietà. |
| [!UICONTROL DSA Domain Language] | (Campagne di tipo a) &quot;<i>[!UICONTROL DynamicSearchAds]</i>&quot; o b) &quot;<i>[!UICONTROL Search]</i>&quot; quando l&#39;elemento [!DNL ExperimentId] non è impostato) Lingua delle pagine del sito Web da utilizzare per gli annunci di ricerca dinamica. Le lingue di dominio supportate sono [!UICONTROL Dutch], [!UICONTROL English], [!UICONTROL French], [!UICONTROL German], [!UICONTROL Italian], [!UICONTROL Spanish] e [!UICONTROL Swedish].<br><br>Per le campagne esistenti non è possibile modificare la lingua, ma è necessario includerla per aggiornare altre proprietà. |
| [!UICONTROL Ad Group Name] | Nome univoco che identifica un gruppo di annunci. La lunghezza massima è di 128 caratteri. I caratteri vuoti finali non vengono salvati (ad esempio, &quot;Gruppo di annunci 1&quot; viene salvato come &quot;Gruppo di annunci 1&quot;). |
| [!UICONTROL Ad Group Type] | (Campagne nella rete di ricerca; sola lettura per gruppi di annunci esistenti) Tipo di gruppo di annunci: <i>[!UICONTROL Audience]</i> (solo per campagne di pubblico), <i>[!UICONTROL Search Dynamic]</i> (solo per annunci di ricerca dinamica) e <i>[!UICONTROL Search Standard]</i> (solo per annunci di ricerca responsive e annunci di testo espansi esistenti). Alcuni tipi di campagne possono includere più tipi di gruppi di annunci. |
| [!UICONTROL Keyword] | (Solo campagne nella rete di ricerca) Stringa della parola chiave. La lunghezza massima è di 50 caratteri.<br><br><b>Note:</b><ul><li>Per escludere una parola chiave a livello di gruppo di annunci o di campagna, impostare [!UICONTROL Match Type] su `Negative`. Se la riga include il nome del gruppo di annunci, la parola chiave viene esclusa per il gruppo di annunci. Se la riga non include il nome del gruppo di annunci, la parola chiave viene esclusa per l’intera campagna.</li><li>La modifica di una parola chiave [!DNL Microsoft Advertising] comporta l&#39;eliminazione della parola chiave esistente e la creazione di una nuova parola chiave con un nuovo ID. Cambiando il tipo di corrispondenza, tuttavia, non elimina la parola chiave esistente.</li></ul> |
| Posizionamento | Obsoleto |
| [!UICONTROL Audience] | L’elenco di remarketing per il pubblico di destinazione degli annunci di ricerca (RLSA) per la campagna o il gruppo di annunci. |
| [!UICONTROL Target Type] | (Solo destinazioni RLSA) Tipo di destinazione: <i>[!UICONTROL Inclusion]</i> o <i>[!UICONTROL Exclusion]</i>. |
| [!UICONTROL Auto Target Expression] | Target di ricerca dinamica per il gruppo di annunci. Per tutte le destinazioni, utilizzare &quot;[!UICONTROL All Web Pages]&quot;.<br><br>Per eseguire il targeting di un massimo di tre criteri di ricerca dinamica, utilizzare il formato `<category>=<target>`, dove &lt;categoria> può includere una delle categorie seguenti. Unire più destinazioni per una singola categoria con &quot;`[blank space] and [blank space]`&quot; e unire più categorie con &quot;`[blank space] and [blank space]`&quot;.<br><ul><li><i>Categoria:</i> per visualizzare annunci di ricerca dinamici per pagine indicizzate con una categoria di contenuto Google specifica.</li><li><i>URL:</i> per visualizzare annunci di ricerca dinamica per pagine indicizzate con un URL specifico, in cui il valore può essere incluso in qualsiasi punto dell&#39;URL.</li><li><i>Titolo pagina:</i> per visualizzare annunci di ricerca dinamica per pagine indicizzate con testo specifico nel titolo della pagina.</li><li><i>Contenuto pagina:</i> per visualizzare annunci di ricerca dinamica per pagine indicizzate con contenuto specifico.</li></ul>Esempio: url=shoes.example.com e page title=footwear<br>Esempio: tutte le pagine Web |
| [!UICONTROL Location] | Una posizione geografica in cui inserire annunci per la campagna o il gruppo di annunci; i valori non fanno distinzione tra maiuscole e minuscole. Se non immetti alcun valore per la campagna o il gruppo di annunci, viene eseguito il targeting di tutte le posizioni. Per eseguire il targeting di posizioni specifiche, immettere la posizione utilizzando i formati del codice di posizione [!DNL Microsoft Advertising]. Per scaricare un elenco di percorsi, accedere al portale per sviluppatori [!DNL Microsoft Advertising] utilizzando le credenziali dell&#39;account pubblicitario [!DNL Microsoft Advertising]. <b>Nota:</b> per escludere una posizione, anteporre al codice della posizione un segno meno (`-`), ad esempio `-United States`. |
| [!UICONTROL Location Type] | Il tipo di ubicazione, ad esempio Città, Paese, Metropolitana, CAP e Stato. Per scaricare un elenco di percorsi, accedere al portale per sviluppatori [!DNL Microsoft Advertising] utilizzando le credenziali dell&#39;account pubblicitario [!DNL Microsoft Advertising]. |
| [!UICONTROL Match Type] | (Solo campagne nella rete di ricerca) Le opzioni di corrispondenza delle parole chiave. Questo può includere l’opzione di corrispondenza delle parole chiave per un target di ricerca dinamica o un gruppo di prodotti. I valori includono: <i>[!UICONTROL Broad]</i> (impostazione predefinita per le nuove parole chiave), <i>[!UICONTROL Exact]</i>, <i>[!UICONTROL Phrase]</i>, <i>[!UICONTROL Content]</i> (impostazione automatica per le parole chiave quando il gruppo di annunci esegue il targeting della rete di contenuti), <i>[!UICONTROL Negative]</i> (per escludere una parola chiave nella rete di contenuti), <i>[!UICONTROL Dynamic Ad Target]</i> (impostazione predefinita per le nuove destinazioni di ricerca dinamica), <i>[!UICONTROL Product Group]</i> (impostazione predefinita per i nuovi gruppi di prodotti) o <i>[!UICONTROL Negative Product Group]</i> (per escludere un gruppo di prodotti).  Per modificare o eliminare una parola chiave con più tipi di corrispondenza è necessario un valore per il tipo di corrispondenza o l’ID della parola chiave.<br><br>Per Broad Match Modifier, scegliere &quot;Broad&quot; e inserire un `+` prima di qualsiasi parola all&#39;interno della parola chiave richiesta (ad esempio &quot;`+red +shoes`&quot; per richiedere sia &quot;red&quot; che &quot;shoes&quot;).<br><br>La modifica del tipo di corrispondenza per una parola chiave [!DNL Microsoft Advertising] non elimina la parola chiave esistente. |
| [!UICONTROL Max CPC] | (Campagne sulla rete di ricerca) Il costo massimo per clic (CPC), che è l’importo più alto da pagare per un clic dell’annuncio in base alla parola chiave, al gruppo di prodotti o al target di ricerca dinamica, con o senza simboli monetari e punteggiatura.  Per i record esistenti relativi a parole chiave e gruppi di prodotti in portfolio ottimizzati, gli aggiornamenti sono validi per un solo giorno e vengono sovrascritti durante il successivo ciclo di ottimizzazione. <b>Nota:</b> non è possibile impostare le offerte per le parole chiave negative. |
| [!UICONTROL Max Content CPC] | (Sola lettura per le campagne CPC create prima che la rete di contenuti diventasse obsoleta solo nel 2017 ) Il costo massimo del contenuto per clic (CPC), che è l’importo più alto da pagare per un clic di un annuncio da un sito di rete di visualizzazione, con o senza simboli monetari e punteggiatura. |
| [!UICONTROL Audience Target Method] | (Gruppi di annunci di pubblico) Indica se:<ul><li><i>[!UICONTROL Target and Bid]:</i> Per mostrare annunci solo agli utenti associati ai tipi di pubblico di destinazione che soddisfano anche altri target per il gruppo di annunci.</li><li><i>[!UICONTROL Bid Only]:</i>Per mostrare annunci anche a persone non associate a tipi di pubblico di destinazione, purché soddisfino altri target a livello di gruppo di annunci.</li></ul> Tuttavia, puoi aumentare le possibilità che gli annunci vengano mostrati a tipi di pubblico specifici, impostando offerte più elevate per tali tipi di pubblico. |
| [!UICONTROL Parent Product Groupings] | Gerarchia di eventuali gruppi di prodotti padre.<br><br>Esempio: `All Products>>ProductTypeL1=a>>ProductTypeL2=b` |
| [!UICONTROL Product Grouping] | Il gruppo di prodotti (ad esempio &quot;brand=acme&quot; o &quot;All Products&quot;).<br><br><b>Note:</b><ul><li>Quando un gruppo di prodotti specificato non esiste nella gerarchia dei gruppi di prodotti principali, in Ricerca, Social e Commerce vengono create le parti della gerarchia necessarie.</li><li>Cerca, Social e Commerce crea automaticamente un gruppo &quot;[!UICONTROL All Products]&quot; ogni volta che crei un gruppo di annunci in una campagna di acquisto con un&#39;offerta predefinita impostata sull&#39;offerta predefinita del gruppo di annunci. Search, Social e Commerce creano automaticamente un gruppo &quot;[!UICONTROL Everything Else]&quot; con l&#39;offerta predefinita del gruppo di annunci a ogni livello della gerarchia dei gruppi di prodotti. Puoi comunque creare in modo esplicito questi gruppi predefiniti, escludendoli o modificandone le offerte.</li><li>Ogni gruppo di annunci può includere fino a otto livelli di gruppi di prodotti, tra cui &quot;[!UICONTROL All Products]&quot; e altri sette livelli.</li></ul> |
| [!UICONTROL Partition Type] | Il tipo di partizione per il gruppo di prodotti: <i>[!UICONTROL subdivision]</i> (se include gruppi di prodotti figlio) o <i>[!UICONTROL unit]</i> (se non include gruppi di prodotti figlio). |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 15] | (Solo annunci di testo espansi, annunci multimediali, annunci reattivi e annunci di ricerca responsive) I titoli di un annuncio. La lunghezza massima per ogni campo del titolo dell’annuncio è di 30 caratteri o 15 caratteri a doppio byte, incluso qualsiasi testo dinamico (come i valori delle parole chiave, le variabili di sostituzione dinamica `{Param2}` e `{Param3}` e i personalizzatori di annunci).<br><br> Per gli annunci di ricerca responsive, inserisci un personalizzatore di annunci utilizzando il seguente formato, dove &quot;Testo predefinito&quot; è un valore facoltativo da inserire quando il file di feed non include un valore valido: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`<br><br>Per gli annunci di testo espansi, sono richiesti Ad Title e Ad Title 2 e [!UICONTROL Ad Title 3] è facoltativo. [!DNL Microsoft Advertising] ha dichiarato obsoleti gli annunci di testo espansi ad agosto 2022 e ora puoi creare rapporti solo su ed eliminarli.<br><br>Per gli annunci multimediali, gli annunci reattivi e gli annunci di ricerca responsive, sono necessari [!UICONTROL Ad Title], [!UICONTROL Ad Title 2] e [!UICONTROL Ad Title 3] e tutti gli altri campi del titolo dell&#39;annuncio sono facoltativi.<br><br>Per eliminare il valore esistente per un campo non obbligatorio, utilizzare il valore `[delete]` (comprese le parentesi).<br><br>Per tutti i tipi di annunci ad eccezione di quelli di testo espansi, la modifica della copia dell&#39;annuncio comporta l&#39;eliminazione dell&#39;annuncio esistente e la creazione di un nuovo annuncio con le stesse proprietà. |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | (Solo per annunci di ricerca reattiva; facoltativo) Posizione in cui fissare il titolo dell&#39;annuncio corrispondente: `[null]` (nessun valore, che rende il titolo dell&#39;annuncio idoneo per tutte le posizioni), 1, 2 o 3. Ad esempio, se [!UICONTROL Ad Title Position] ha un valore pari a 1, [!UICONTROL Ad Title] può essere visualizzato solo nella posizione 1. Per impostazione predefinita, tutti i titoli degli annunci sono nulli (non hanno valori). Per eliminare il valore esistente, utilizzare il valore `[delete]` (comprese le parentesi).<br><br><b>Nota:</b> puoi fissare più titoli di annunci nella stessa posizione. La rete di annunci utilizza uno dei titoli degli annunci fissati alla posizione. I titoli fissati alla posizione 3 potrebbero non essere visualizzati con l’annuncio. |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | (Annunci di testo, annunci per ricerca dinamica, annunci multimediali, annunci reattivi, annunci per ricerca responsive e solo sitelink a livello di campagna) Il corpo di un annuncio o di un sitelink.<br><br>Per i sitelink, è possibile utilizzare sia [!UICONTROL Description Line 1] che [!UICONTROL Description Line 2] per includere testo aggiuntivo che la rete di annunci potrebbe visualizzare sotto il testo del collegamento. Ogni campo di descrizione può includere fino a 35 caratteri a byte singolo o 17 caratteri a byte doppio.<br><br>Per gli annunci, la lunghezza massima per ogni campo di descrizione è di 90 caratteri o 45 caratteri a doppio byte, incluso qualsiasi testo dinamico, ad esempio i valori delle parole chiave e degli adcustomizzatori di annunci.<br><br>Per gli annunci di ricerca responsive, inserire un personalizzatore di annunci utilizzando il seguente formato, dove Testo predefinito è un valore facoltativo da inserire quando il file di feed non include un valore valido: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`<br><br>Per gli annunci di testo e gli annunci di ricerca dinamica, la riga di descrizione 1 è obbligatoria e [!UICONTROL Description Line 2] è facoltativa.<br><br>Per gli annunci multimediali, gli annunci reattivi e gli annunci di ricerca responsive, sono necessari [!UICONTROL Description Line 1] e [!UICONTROL Description Line 2] e [!UICONTROL Description Line 3] e [!UICONTROL Description Line 4] sono facoltativi.<br><br>Per eliminare il valore esistente, utilizzare il valore `[delete]` (comprese le parentesi).<br><br><b>Note:</b><ul><li>(Annunci di testo standard) Il titolo e il testo combinati devono contenere almeno tre parole.</li><li>(Annunci di testo espansi) Questo campo può includere facoltativamente le variabili di sostituzione dinamica {Param2} e {Param3}. In tal caso, la lunghezza massima del testo dell’annuncio è di 300 caratteri a byte singolo o 150 caratteri a byte doppio. [!DNL Microsoft Advertising] ha dichiarato obsoleti gli annunci di testo espansi ad agosto 2022 e ora puoi creare rapporti solo su ed eliminarli.</li><li>(Annunci di ricerca dinamica) Il testo di sostituzione dinamica non è consentito.</li><li>Per tutti i tipi di annunci, ad eccezione degli annunci di testo espansi, la modifica di un annuncio copiato elimina l’annuncio esistente e ne crea uno nuovo.</li></ul> |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | (Solo annunci di ricerca responsive; facoltativo) Posizione in cui fissare la descrizione corrispondente: `[null]` (nessun valore, che rende la descrizione idonea per tutte le posizioni), 1, 2 o 3. Ad esempio, se [!UICONTROL Description 1 Position] ha un valore pari a 1, la Descrizione 1 può essere visualizzata solo nella Posizione 1. Per impostazione predefinita, nessuna descrizione è bloccata su una posizione.<br><br>Per eliminare il valore esistente, utilizzare il valore `[delete]` (comprese le parentesi).<br><br><b>Nota:</b> è possibile fissare più descrizioni nella stessa posizione. La rete di annunci utilizza una delle descrizioni fissate alla posizione. Le descrizioni fissate alla posizione 2 potrebbero non essere visualizzate con l’annuncio. |
| [!UICONTROL Business Name] | (Solo annunci multimediali) La ragione sociale, con un massimo di 25 caratteri. |
| [!UICONTROL Promotion Line] | (Solo per annunci di prodotti) Una linea promozionale unica da includere nell’elenco dei prodotti nei risultati di ricerca (ad esempio &quot;Spedizione gratuita ora!&quot;). La lunghezza massima è di 45 caratteri.<br><br>La linea della promozione può essere visualizzata in posizioni diverse rispetto all&#39;annuncio (ad esempio sotto l&#39;annuncio) a seconda della posizione dell&#39;annuncio sulla pagina. |
| [!UICONTROL Display URL] | L’URL incluso nell’annuncio.<br><br>Per gli annunci di ricerca dinamica espansi, la rete di annunci genera questo valore in modo dinamico dal dominio del sito Web e non è necessario immettere un valore.<br><br>Per gli annunci di testo espansi e gli annunci di ricerca responsive, non è necessario immettere un valore. L’URL di visualizzazione viene estratto automaticamente dal dominio nell’URL finale. Facoltativamente, puoi personalizzare l’URL utilizzando i campi Percorso 1 e Percorso 2.<br><br><b>Note:</b><ul><li>(Account con URL finali) I nomi di dominio nell’URL visualizzato e nell’URL finale devono corrispondere.</li><li>[!DNL Microsoft Advertising] ha dichiarato obsoleti gli annunci di testo espansi ad agosto 2022 e ora puoi creare rapporti solo su ed eliminarli.</li></ul> |
| [!UICONTROL Display Path 1] | (Solo annunci di testo espansi, annunci di ricerca dinamici e annunci di ricerca responsive) Testo aggiunto all’URL di visualizzazione ed estratto automaticamente dall’URL finale. Ogni percorso è preceduto nell’URL da una barra (/). Un percorso non può contenere barre (/) o caratteri di nuova riga (\n). La lunghezza massima per ogni percorso è di 15 caratteri o 7 caratteri a doppio byte.<br><br>Per inserire un personalizzatore di annunci, usa i seguenti formati, dove &quot;Testo predefinito&quot; è un valore facoltativo da inserire quando il file di feed non include un valore valido: `{CUSTOMIZER.Attribute name:Default text}`, ad esempio `{CUSTOMIZER.Discount:10%}`<br><br>Ad esempio, se [!UICONTROL Display Path 1] è &quot;offerte&quot;, l&#39;URL di visualizzazione sarà &lt;URL di visualizzazione>/offerte, ad esempio www.example.com/deals.<br><br>[!DNL Microsoft Advertising] ha dichiarato obsoleti gli annunci di testo espansi ad agosto 2022 e ora puoi creare rapporti solo su ed eliminarli. |
| [!UICONTROL Display Path 1] | (Solo annunci di testo espansi, annunci di ricerca dinamici e annunci di ricerca responsive) Un percorso di visualizzazione aggiuntivo. Vedere la voce per [!UICONTROL Display Path 1].<br><br>Esempio: se [!UICONTROL Display Path 1] è &quot;offerte&quot; e [!UICONTROL Display Path 2] è &quot;locale&quot;, l&#39;URL di visualizzazione sarà &lt;<i>URL di visualizzazione</i>>/offerte/locale, ad esempio www.example.com/deals/local. |
| [!UICONTROL Start Date] | (Solo sitelink avanzati) La prima data in cui è possibile fare offerte per il sitelink, nel fuso orario dell&#39;inserzionista e in uno dei seguenti formati: m/d/aaaa, m/g/aa, m-d-aaaa o m-d-aaaa. Per impostazione predefinita, i nuovi sitelink migliorati sono nel giorno corrente. <b>Nota:</b> è possibile creare nuovi sitelink avanzati solo nelle campagne con sitelink avanzati esistenti o senza sitelink. |
| [!UICONTROL End Date] | L’ultima data in cui il sitelink può essere visualizzato con gli annunci, nel fuso orario dell’inserzionista e in uno dei seguenti formati: m/d/aaaa, m/d/aaaa, m-d-aaaa o m-d-aaaa. Per un nuovo sitelink, il valore predefinito è `[blank]` (ovvero, nessuna data di fine). |
| [!UICONTROL Call To Action] | Il call to action da includere nell’annuncio. Per un elenco dei valori possibili[, vedere il riferimento API &#x200B;](https://learn.microsoft.com/en-us/advertising/campaign-management-service/calltoaction)ma immettere chiamate di più parole per l&#39;azione come più parole, ad esempio &quot;Bet Now&quot; invece di &quot;BetNow&quot;, nei bulksheet. |
| [!UICONTROL Call To Action Language] | Lingua per le opzioni di call to action. Consulta il riferimento API [per un elenco delle lingue possibili](https://learn.microsoft.com/en-us/advertising/campaign-management-service/languagename). |
| [!UICONTROL Base URL/Final URL] | L’URL della pagina di destinazione a cui vengono indirizzati gli utenti dei motori di ricerca quando fanno clic sull’annuncio, compresi eventuali parametri di aggiunta configurati per la campagna o l’account. Gli URL di base/finali a livello di parola chiave sostituiscono quelli a livello di annuncio e superiori.<br><br>Per eliminare il valore esistente, utilizzare il valore `[delete]` (comprese le parentesi). |
| [!UICONTROL Destination URL] | (Incluso nei bulksheet generati a scopo informativo; non pubblicato sul motore di ricerca) Per gli account con URL di destinazione, si tratta dell’URL che collega un annuncio a un URL/pagina di destinazione di base sul sito web dell’inserzionista (a volte tramite un altro sito che tiene traccia del clic e quindi reindirizza l’utente alla pagina di destinazione). Include tutti i parametri di aggiunta configurati per la campagna o l’account Search, Social e Commerce. Se hai generato URL di tracciamento, questo si basa sui parametri di tracciamento riportati nelle impostazioni del tuo account e nelle impostazioni della campagna. Se hai aggiunto parametri specifici per i motori di ricerca, questi possono essere sostituiti con parametri equivalenti per Search, Social e Commerce.<br><br>Per gli account con URL finali, questa colonna mostra lo stesso valore della colonna URL di base/URL finale. |
| [!UICONTROL Custom URL Param] | Dati da sostituire alla variabile dinamica `{custom_code}` quando la variabile viene inclusa nei parametri di tracciamento per le impostazioni dell&#39;account di ricerca o della campagna. Per inserire il valore personalizzato nell’URL di tracciamento, devi caricare il file del bulksheet utilizzando l’opzione Genera URL di tracciamento. |
| [!UICONTROL Creative Type] | Il formato dell&#39;annuncio: <i>[!UICONTROL Dynamic Search Ad]</i>, <i>[!UICONTROL Expanded Text Ad]</i>, <i>[!UICONTROL Expanded Dynamic Search Ad]</i>, <i>[!UICONTROL Multimedia Ad]</i>, <i>[!UICONTROL Product Ad]</i> (annunci acquisti), o <i>[!UICONTROL Responsive Search Ad]</i>, o <i>[!UICONTROL Text ad]</i>. Il valore predefinito per i nuovi annunci è <i>[!UICONTROL Text ad]</i>. |
| [!UICONTROL Ad Group Start Date] | La prima data in cui le offerte possono essere presentate per il gruppo di annunci, nel fuso orario dell’inserzionista e in uno dei seguenti formati: m/g/aaaa, m/g/aa, m-g-aaaa o m-g-aa. Per un nuovo gruppo di annunci, l’impostazione predefinita è la data corrente. |
| [!UICONTROL Ad Group End Date] | L&#39;ultima data in cui le offerte possono essere presentate per il gruppo di annunci, nel fuso orario dell&#39;inserzionista e in uno dei seguenti formati: m/d/aaaa, m/g/aa, m-d-aaaa o m-d-aaaa. Per un nuovo gruppo di annunci, l&#39;impostazione predefinita è [blank] (ovvero, nessuna data di fine). |
| [!UICONTROL Tracking Template] | (Facoltativo) Il modello di tracciamento, che specifica tutti i reindirizzamenti dei domini di destinazione e i parametri di tracciamento e incorpora l’URL finale in un parametro. Il modello di tracciamento al livello più granulare (con la parola chiave come più granulare) sostituisce i valori a tutti i livelli superiori.<br><br>Per il tracciamento delle conversioni di Adobe Advertising, applicato quando le impostazioni della campagna includono &quot;[!UICONTROL EF Redirect]&quot; e &quot;[!UICONTROL Auto Upload]&quot;, Search, Social e Commerce aggiungono automaticamente il codice di reindirizzamento e di tracciamento quando si salva il record.<br><br>Per reindirizzamenti e monitoraggio di terze parti, immettere un valore.<br><br>Per un elenco di parametri per indicare gli URL finali nei modelli di tracciamento, consulta la documentazione di [!DNL Microsoft Advertising].<br><br> Per eliminare il valore esistente, utilizzare il valore `[delete]` (comprese le parentesi). |
| [!UICONTROL Landing Page Suffix] | Eventuali parametri da aggiungere alla fine degli URL finali per tenere traccia delle informazioni. Esempio: `param2=value1&param3=value2`<br><br>Visualizza &quot;[Formati di tracciamento dei clic per [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).&quot;<br><br>I suffissi URL finali ai livelli inferiori sovrascrivono il suffisso a livello di account. Per una manutenzione più semplice, utilizza solo il suffisso a livello di account, a meno che non sia necessario un tracciamento diverso per i singoli componenti dell’account. Per configurare un suffisso a livello di gruppo di annunci o inferiore, utilizzare l&#39;editor [!DNL Microsoft Advertising]. |
| Cerca stato rete | Se inserire annunci per il gruppo di annunci su vari elementi della rete di ricerca:<ul><li><i>Tutto:</i> per inserire annunci in tutte le reti di ricerca Bing e nei partner di ricerca in syndication.</li><li><i>OwnedAndOperatedOnly:</i>Per inserire annunci solo su Bing e Yahoo! siti web.</li><li><i>SyndicatedSearchOnly:</i> Per inserire annunci solo su Bing e Yahoo. partner di ricerca in syndication.</li><li><i>Disattivato:</i> Per inserire annunci solo nella rete dei contenuti (non nella rete di ricerca).</li></ul> Per i nuovi gruppi di annunci, l’impostazione predefinita è Attivato. |
| [!UICONTROL Content Network Status] | Obsoleto |
| [!UICONTROL Languages] | Lingua di destinazione per gli annunci nel gruppo di annunci: [!UICONTROL English], [!UICONTROL French], [!UICONTROL Finnish], [!UICONTROL German], [!UICONTROL Norwegian], [!UICONTROL Spanish] o [!UICONTROL Swedish]. Il valore predefinito per le nuove campagne è [!UICONTROL English].<br><br>Questa impostazione determina i paesi e le aree geografiche in cui l&#39;annuncio può essere visualizzato. Assicurati di scegliere una lingua compatibile con i target di posizione della campagna. |
| [!UICONTROL Budget Type] | Indica se il budget è <i>[!UICONTROL Daily]</i> (impostazione predefinita) o <i>[!UICONTROL Monthly]</i>.<br><br>Nota: se assegni la campagna a un portfolio ottimizzato, questo valore viene impostato automaticamente su [!UICONTROL Daily]. |
| [!UICONTROL Device] | Tipo di dispositivo per il quale vengono apportate regolazioni delle offerte a livello di campagna o di gruppo di annunci: <i>[!UICONTROL smartphone]</i>, <i>[!UICONTROL tablet]</i> o <i>[!UICONTROL desktop]</i>. |
| [!UICONTROL Bid Adjustment] | Rettifica offerta per un tipo di destinazione specificato. Ad esempio, se l’offerta a livello di parola chiave è 1 USD e la regolazione dell’offerta per gli smartphone è del 50%, l’offerta per lo smartphone è di 1,50 USD. Per impostazione predefinita, tutte le destinazioni sono offerte a livello di parola chiave. Le percentuali valide possono includere:<ul><li>Smartphone e tablet: -100 (per non fare offerte per il tipo di dispositivo) e da -90 a 900</li><li>Desktop: da 0 a 900</li></ul> |
| [!UICONTROL Creative Preferred Devices] | Tipi di dispositivi su cui si preferisce visualizzare l&#39;annuncio o il sitelink: <i>[!UICONTROL All]</i> (impostazione predefinita) o <i>[!UICONTROL Mobile]</i>. Quando si specifica Mobile, la rete tenta di visualizzare l’annuncio o il sitelink agli utenti dei dispositivi mobili anziché agli utenti del desktop o del tablet. In caso contrario, la rete visualizza l&#39;annuncio o il sitelink su qualsiasi tipo di dispositivo. <b>Nota:</b> la rete non garantisce che l&#39;annuncio verrà visualizzato sul tipo di dispositivo preferito. |
| [!UICONTROL Param2] | Stringa da utilizzare come valore di sostituzione se l&#39;URL di base della parola chiave o il titolo, la descrizione o l&#39;URL di base dell&#39;annuncio contiene la stringa di sostituzione dinamica `{Param2}`. La lunghezza massima è di 70 caratteri, ma tieni presente la lunghezza massima degli elementi dell’annuncio in cui lo utilizzi (ad esempio, il titolo 1 e il titolo 2 combinati possono contenere un massimo di 76 caratteri). Per eliminare il valore esistente, utilizzare il valore `[delete]` (comprese le parentesi). |
| [!UICONTROL Param3] | Stringa da utilizzare come valore di sostituzione se l&#39;URL di base della parola chiave o il titolo, la descrizione o l&#39;URL di base dell&#39;annuncio contiene la stringa di sostituzione dinamica `{Param3}`. La lunghezza massima è di 70 caratteri, ma tieni presente la lunghezza massima degli elementi dell’annuncio in cui lo utilizzi (ad esempio, il titolo 1 e il titolo 2 combinati possono contenere un massimo di 76 caratteri). Per eliminare il valore esistente, utilizzare il valore `[delete]` (comprese le parentesi). |
| [!UICONTROL Link Name] | Testo del sitelink. Deve essere univoco all’interno della campagna. Se si specificano Description1 e Description2, il testo del sitelink può includere fino a 25 caratteri a byte singolo o 12 caratteri a byte doppio; in caso contrario, il testo del sitelink può includere fino a 35 caratteri a byte singolo o 17 caratteri a byte doppio.<br><br>[!DNL Microsoft Advertising] può visualizzare due, quattro o sei sitelink avanzati con descrizioni, oppure quattro o sei sitelink in una singola riga senza descrizioni, con un annuncio.<br><br>Puoi creare nuovi collegamenti di siti migliorati solo nelle campagne con collegamenti di siti migliorati esistenti o senza collegamenti di siti. |
| [!UICONTROL Campaign Status] | Stato di visualizzazione della campagna: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> o <i>[!UICONTROL Deleted]</i> (solo campagne esistenti). Il valore predefinito per le nuove campagne è [!UICONTROL Active]. Per eliminare una campagna attiva o in pausa, immettere il valore `Deleted`. |
| [!UICONTROL Ad Group Status] | Stato di visualizzazione del gruppo di annunci: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> o <i>[!UICONTROL Deleted]</i> (solo gruppi di annunci esistenti). Il valore predefinito per i nuovi gruppi di annunci è [!UICONTROL Active]. Per eliminare un gruppo di annunci attivo o in pausa, immettere il valore `Deleted`. |
| [!UICONTROL Keyword Status] | Stato di visualizzazione della parola chiave: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> o <i>[!UICONTROL Deleted]</i> (solo parole chiave esistenti). Il valore predefinito per le nuove parole chiave è [!UICONTROL Active]. Per eliminare una parola chiave attiva o in pausa, immettere il valore `Deleted`. <b>Nota:</b> se crei URL di tracciamento per una parola chiave con più tipi di corrispondenza, lo stato della parola chiave per ogni tipo di corrispondenza deve essere lo stesso. |
| [!UICONTROL Placement Status] | Obsoleto |
| [!UICONTROL Ad Status] | Stato di visualizzazione dell&#39;annuncio: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Deleted]</i> (solo annunci esistenti), <i>[!UICONTROL Disapproved]</i> (non modificabile) o <i>[!UICONTROL Paused]</i>. Il valore predefinito per i nuovi annunci è [!UICONTROL Active]. Per eliminare un annuncio attivo o in pausa, immettere il valore `Deleted`. |
| [!UICONTROL Target Status] | Stato di una destinazione di ricerca dinamica: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> o <i>[!UICONTROL Deleted]</i> (solo destinazioni esistenti). Il valore predefinito per le nuove destinazioni è [!UICONTROL Active]. Per eliminare una destinazione attiva o in pausa, immettere il valore `Deleted`. |
| [!UICONTROL Sitelink Status] | Stato di visualizzazione del sitelink: <i>[!UICONTROL Active]</i> o <i>[!UICONTROL Deleted]</i> (solo sitelink esistenti). Il valore predefinito per i nuovi sitelink è [!UICONTROL Active]. Per eliminare un sitelink attivo, immettere il valore `Deleted`. |
| [!UICONTROL Location Status] | Stato della destinazione del percorso: <i>[!UICONTROL Active]</i> o <i>[!UICONTROL Deleted]</i> (solo posizioni esistenti). Il valore predefinito per i nuovi percorsi è [!UICONTROL Active]. Per eliminare un percorso attivo, immettere il valore `Deleted`. |
| [!UICONTROL Product Group Status] | Stato di visualizzazione del gruppo di prodotti: <i>[!UICONTROL Active]</i> o <i>[!UICONTROL Deleted]</i> (solo gruppi di prodotti esistenti). Il valore predefinito per i nuovi gruppi di prodotti è [!UICONTROL Active]. Per eliminare un gruppo di prodotti attivo, immettere il valore `Deleted`. |
| [!UICONTROL Device Target Status] | Stato della destinazione del dispositivo a livello di campagna o di gruppo di annunci: <i>[!UICONTROL Active]</i> o <i>[!UICONTROL Deleted]</i>. Per le nuove campagne e i nuovi gruppi di annunci, l&#39;impostazione predefinita è [!UICONTROL Active]. |
| [!UICONTROL RLSA Target Status] | Stato della destinazione RLSA a livello di campagna o di gruppo di annunci o dell&#39;esclusione (solo Google Ads): <i>[!UICONTROL Active]</i> o <i>[!UICONTROL Deleted]</i> (solo destinazioni esistenti). Il valore predefinito per le nuove destinazioni o esclusioni è [!UICONTROL Active]. Per eliminare una destinazione attiva o un&#39;esclusione, immettere il valore `Deleted`. |
| \[Classificazione etichetta specifica dell’inserzionista\] | (Nome per una classificazione di etichetta specifica dell’inserzionista, ad esempio &quot;Colore&quot; per una classificazione di etichetta denominata Colore) Valore per la classificazione specificata associata all’entità. Puoi includere un solo valore per classificazione per entità (ad esempio &quot;rosso&quot; per la classificazione dell’etichetta &quot;Colore&quot; per la campagna A). La lunghezza massima è di 100 caratteri e il valore può includere caratteri ASCII e non ASCII.<br><br>Le classificazioni delle etichette e i relativi valori vengono applicati a tutti i componenti figlio. I nuovi componenti aggiunti in seguito vengono associati automaticamente all&#39;etichetta. Le classificazioni delle etichette per i gruppi di prodotti vengono applicate al livello di unità (più granulare).<br><br>Né il nome della classificazione né il valore della classificazione fanno distinzione tra maiuscole e minuscole. |
| [!UICONTROL Constraints] | Vincolo assegnato all&#39;entità. È possibile assegnare un solo vincolo per entità.<br><b>>I vincoli vengono ereditati dalle entità figlio, pertanto non è necessario immettere valori per le entità figlio a meno che non si desideri ignorare i valori ereditati. |
| [!UICONTROL Campaign ID] | L’ID univoco che identifica una campagna esistente. Nei file CSV e TSV deve essere preceduto da virgolette singole (&#39;).[^1] Obbligatorio solo quando si modifica il nome della campagna, a meno che la riga non includa &quot;[!UICONTROL AMO ID]&quot; per la campagna. |
| [!UICONTROL Ad Group ID] | L’ID univoco che identifica un gruppo di annunci esistente. Nei file CSV e TSV deve essere preceduto da virgolette singole (&#39;).[^1] Obbligatorio solo quando si modifica il nome della campagna, a meno che la riga non includa &quot;[!UICONTROL AMO ID]&quot; per il gruppo di annunci. |
| [!UICONTROL Placement ID] | Obsoleto |
| [!UICONTROL Keyword ID] | ID univoco che identifica una parola chiave esistente. Nei file CSV e TSV deve essere preceduto da virgolette singole (&#39;).[^1] Obbligatorio solo quando si modifica la parola chiave, a meno che la riga non includa a) colonne di proprietà sufficienti per identificare la parola chiave o b) un &quot;[!UICONTROL AMO ID]&quot;.&quot; |
| [!UICONTROL Ad ID] | <p>ID univoco che identifica un annuncio esistente. Nei file CSV e TSV deve essere preceduto da virgolette singole (&#39;).[^1] Per gli annunci di ricerca responsive, è necessario l’ID annuncio o l’AMO ID per modificare o eliminare i dati dell’annuncio. Per tutti gli altri tipi di entità, l’AMO ID è necessario solo quando si modifica lo stato dell’annuncio, a meno che la riga non includa a) colonne di proprietà dell’annuncio sufficienti per identificare l’annuncio o b) un &quot;[!UICONTROL AMO ID]&quot;.&quot; Tuttavia, se non includi né [!UICONTROL Ad ID] né [!UICONTROL AMO ID] e le colonne della proprietà dell&#39;annuncio corrispondono a più annunci, lo stato di uno solo degli annunci cambia.</p><p><b>Nota:</b> se si modificano le colonne a) delle proprietà dell&#39;annuncio ad eccezione di Stato per un annuncio esistente o b) i dati per un annuncio di ricerca responsive e non si includono né [!UICONTROL Ad ID] né [!UICONTROL AMO ID], viene creato un nuovo annuncio e l&#39;annuncio esistente non viene modificato. </p> |
| [!UICONTROL Sitelink ID] | ID univoco che identifica un sitelink esistente. Nei file CSV e TSV deve essere preceduto da virgolette singole (&#39;).[^1] Obbligatorio solo quando si modifica o si elimina il sitelink, a meno che la riga non includa a) colonne di proprietà sufficienti per identificare il sitelink o b) un &quot;[!UICONTROL AMO ID]&quot;.&quot; Tuttavia, se non includi né [!UICONTROL Sitelink ID] né [!UICONTROL AMO ID] e le colonne di proprietà corrispondono a più sitelink, lo stato di uno solo dei sitelink cambia.</p><p><b>Nota:</b> se si modificano le colonne delle proprietà del sitelink ad eccezione di Stato per un sitelink esistente e non si includono né [!UICONTROL Sitelink ID] né [!UICONTROL AMO ID], verrà creato un nuovo sitelink e il sitelink esistente non verrà modificato. |
| [!UICONTROL Product Group ID] | ID univoco che identifica un gruppo di prodotti esistente. Nei file CSV e TSV deve essere preceduto da virgolette singole (&#39;).[^1] Obbligatorio solo quando si modifica o si elimina il gruppo di prodotti, a meno che la riga non includa a) colonne di proprietà sufficienti per identificare il gruppo di prodotti o b) un &quot;[!UICONTROL AMO ID]&quot;.&quot; |
| ID posizione | L&#39;identificatore univoco [!DNL Microsoft Advertising] per la destinazione della posizione. Per scaricare un elenco di percorsi, accedere al portale per sviluppatori [!DNL Microsoft Advertising] utilizzando le credenziali dell&#39;account pubblicitario [!DNL Microsoft Advertising]. Obbligatorio solo quando si modifica o si elimina la destinazione del percorso, a meno che la riga non includa un &quot;[!UICONTROL AMO ID]&quot; per la destinazione. |
| [!UICONTROL Target ID] | ID univoco che identifica una destinazione automatica esistente. Obbligatorio solo quando si modifica o si elimina la destinazione automatica, a meno che la riga non includa &quot;[!UICONTROL AMO ID]&quot; per la destinazione. |
| [!UICONTROL RLSA Target ID] | ID univoco che identifica una destinazione RLSA a livello di campagna o di gruppo di annunci esistente. Nei file CSV e TSV deve essere preceduto da virgolette singole (&#39;).[^1] Obbligatorio solo quando si modifica o si elimina la destinazione o l&#39;esclusione, a meno che la riga non includa un &quot;[!UICONTROL AMO ID]&quot; per la destinazione. |
| [!UICONTROL AMO ID] | (Nei bulksheet generati) Identificatore univoco generato da Adobe per un’entità sincronizzata. Per gli annunci di ricerca responsive, l’AMO ID è necessario per modificare o eliminare gli annunci, a meno che tu non includa l’Ad ID. Per modificare i dati per tutti gli altri tipi di entità con un AMO ID, è necessario l’AMO ID per modificare o eliminare i dati, a meno che non si includano l’ID entità e l’ID entità principale.<br><br>Search, Social e Commerce utilizzano il valore per determinare l&#39;identità corretta da modificare, ma non pubblicano l&#39;ID sulla rete di annunci. |
| [!UICONTROL EF Error Message] | (Incluso nei bulksheet generati a scopo informativo) Segnaposto per la visualizzazione dei messaggi di errore provenienti dalla rete di annunci relativi ai dati nella riga. I messaggi di errore sono inclusi nei file [!UICONTROL EF Errors]. Questo valore non viene inviato alla rete di annunci. |
| [!UICONTROL SE Error Message] | (Incluso nei bulksheet generati a scopo informativo) Segnaposto per la visualizzazione dei messaggi di errore provenienti dalla rete di annunci relativi ai dati nella riga. I messaggi di errore sono inclusi nei file [!UICONTROL SE Errors]. Questo valore non viene inviato alla rete di annunci. |
| [!UICONTROL Exemption Request] | (Incluso nei bulksheet generati a scopo informativo) Segnaposto per la visualizzazione dei nomi e del testo di eventuali criteri pubblicitari Google violati da un annuncio. |
| [!UICONTROL Retail Hash] | (Incluso a scopo informativo nei bulksheet generati utilizzando Advanced Campaign Management) Un codice hash alfanumerico (ad esempio f9639f40cdf56524b541e5dacf55a991) che indica che l’elemento è stato generato utilizzando la vista Avanzate (ACM). |

[^1]: [!DNL Excel] converte i numeri elevati in notazione scientifica (ad esempio 2,12E+09 per 2115585666) quando apre il file. Per visualizzare le cifre nella notazione standard, selezionare una cella della colonna e fare clic all&#39;interno della barra della formula.

## Campi necessari per creare, modificare o eliminare ciascun componente conto {#bulksheet-fields-per-component-microsoft}

Nelle sezioni seguenti sono inclusi i campi relativi a entità conto specifiche.

>[!NOTE]
>
>Quando un campo non è applicabile a un’azione, qualsiasi valore inserito nel campo viene ignorato.

### Campi della campagna

Per una descrizione di ogni campo dati, vedere &quot;[Tutti i campi dati disponibili](#bulksheet-fields-all-microsoft).&quot;

| Campo | Obbligatorio |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obbligatorio a meno che ogni riga non includa &quot;[!UICONTROL AMO ID]&quot; per l&#39;entità. |
| [!UICONTROL Campaign Name] | Obbligatorio. Il nome univoco che identifica una campagna per un account. |
| [!UICONTROL Campaign Budget] | Obbligatorio per creare una campagna. Limite di spesa giornaliero per la campagna, con o senza simboli monetari e punteggiatura. Questo valore sostituisce ma non può superare il budget del conto. |
| [!UICONTROL Channel Type] | Obbligatorio per creare una campagna. |
| [!UICONTROL Delivery Method] | Facoltativo |
| [!UICONTROL Campaign Priority] | Obbligatorio per creare una campagna acquisti. |
| [!UICONTROL Merchant ID] | Obbligatorio per creare una campagna acquisti. |
| [!UICONTROL Sales Country] | Obbligatorio per creare una campagna acquisti. |
| [!UICONTROL Product Scope Filter] | (Campagne commerciali) Facoltativo |
| [!UICONTROL DSA Domain Name] | Necessario per creare una campagna di tipo a) &quot;[!UICONTROL DynamicSearchAds]&quot; o b) &quot;[!UICONTROL Search]&quot; quando l&#39;elemento [!DNL ExperimentId] non è impostato) |
| [!UICONTROL DSA Domain Language] | Necessario per creare una campagna di tipo a) &quot;[!UICONTROL DynamicSearchAds]&quot; o b) &quot;[!UICONTROL Search]&quot; quando l&#39;elemento [!DNL ExperimentId] non è impostato) |
| [!UICONTROL Tracking Template] | Facoltativo |
| [!UICONTROL Landing Page Suffix] | <p>Facoltativo |
| [!UICONTROL Budget Type] | Obbligatorio per creare una campagna. |
| [!UICONTROL Device] | Facoltativo |
| [!UICONTROL Bid Adjustment] | Facoltativo |
| [!UICONTROL Campaign Status] | Obbligatorio solo per eliminare una campagna. |
| \[Classificazione etichetta specifica dell’inserzionista\] | Facoltativo |
| [!UICONTROL Constraints] | Facoltativo |
| [!UICONTROL Campaign ID] | Obbligatorio solo quando si modifica il nome della campagna, a meno che la riga non includa &quot;[!UICONTROL AMO ID]&quot; per la campagna. |
| [!UICONTROL AMO ID] | Obbligatorio per modificare o eliminare i dati a meno che non si includano l’ID entità e l’ID entità padre.<br><br>Search, Social e Commerce utilizzano il valore per determinare l&#39;identità corretta da modificare, ma non pubblicano l&#39;ID sulla rete di annunci. |

### Campi del gruppo di annunci

Per una descrizione di ogni campo dati, vedere &quot;[Tutti i campi dati disponibili](#bulksheet-fields-all-microsoft).&quot;

| Campo | Obbligatorio |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obbligatorio a meno che ogni riga non includa &quot;[!UICONTROL AMO ID]&quot; per l&#39;entità. |
| [!UICONTROL Campaign Name] | Obbligatorio |
| [!UICONTROL Ad Group Name] | Obbligatorio |
| [!UICONTROL Ad Group Type] | Obbligatorio per creare un gruppo di annunci. |
| [!UICONTROL Audience Target Method] | Obbligatorio solo per creare gruppi di annunci di pubblico. |
| [!UICONTROL Ad Group Start Date] | Facoltativo |
| [!UICONTROL Ad Group End Date] | Facoltativo |
| [!UICONTROL Tracking Template] | Facoltativo |
| [!UICONTROL Search Network Status] | (Solo campagne nella rete di ricerca) Facoltativo |
| [!UICONTROL Languages] | Facoltativo |
| [!UICONTROL Device] | Facoltativo |
| [!UICONTROL Bid Adjustment] | Facoltativo |
| [!UICONTROL Ad Group Status] | Richiesto solo per eliminare un gruppo di annunci. |
| \[Classificazione etichetta specifica dell’inserzionista\] | Facoltativo |
| [!UICONTROL Constraints] | Facoltativo |
| [!UICONTROL Ad Group ID] | Obbligatorio solo quando si modifica il nome del gruppo di annunci, a meno che la riga non includa &quot;[!UICONTROL AMO ID]&quot; per il gruppo di annunci. |
| [!UICONTROL AMO ID] | Obbligatorio per modificare o eliminare i dati a meno che non si includano l’ID entità e l’ID entità padre.<br><br>Search, Social e Commerce utilizzano il valore per determinare l&#39;identità corretta da modificare, ma non pubblicano l&#39;ID sulla rete di annunci. |

### Campi parola chiave

Per una descrizione di ogni campo dati, vedere &quot;[Tutti i campi dati disponibili](#bulksheet-fields-all-microsoft).&quot;

| Campo | Obbligatorio |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obbligatorio a meno che ogni riga non includa &quot;[!UICONTROL AMO ID]&quot; per l&#39;entità. |
| [!UICONTROL Campaign Name] | Obbligatorio |
| [!UICONTROL Ad Group Name] | Obbligatorio |
| [!UICONTROL Keyword] | Obbligatorio |
| [!UICONTROL Match Type] | Per modificare o eliminare una parola chiave con più tipi di corrispondenza è necessario un valore per il tipo di corrispondenza o l’ID della parola chiave. |
| [!UICONTROL Max CPC] | Facoltativo |
| [!UICONTROL Base URL/Final URL] | Facoltativo |
| [!UICONTROL Custom URL Param] | Facoltativo |
| [!UICONTROL Tracking Template] | Facoltativo |
| [!UICONTROL Param1] | Facoltativo |
| [!UICONTROL Param2] | Facoltativo |
| [!UICONTROL Keyword Status] | Obbligatorio solo per eliminare una parola chiave. |
| \[Classificazione etichetta specifica dell’inserzionista\] | Facoltativo |
| [!UICONTROL Constraints] | Facoltativo |
| [!UICONTROL Campaign ID] | Facoltativo |
| [!UICONTROL Ad Group ID] | Facoltativo |
| [!UICONTROL Keyword ID] | Obbligatorio solo quando si modifica o si elimina la parola chiave, a meno che la riga non includa a) colonne di proprietà sufficienti per identificare la parola chiave o b) un &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | Obbligatorio per modificare o eliminare i dati a meno che non si includano l’ID entità e l’ID entità padre.<br><br>Search, Social e Commerce utilizzano il valore per determinare l&#39;identità corretta da modificare, ma non pubblicano l&#39;ID sulla rete di annunci. |

### Campi degli annunci per ricerca dinamica

>[!NOTE]
>
>Il supporto per la creazione non è disponibile.

Per questo tipo di annuncio, utilizzare la riga &quot;[!UICONTROL Creative (except RSA)]&quot; nella finestra di dialogo [!UICONTROL Download Bulksheet].

Per una descrizione di ogni campo dati, vedere &quot;[Tutti i campi dati disponibili](#bulksheet-fields-all-microsoft).&quot;

| Campo | Obbligatorio |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obbligatorio a meno che ogni riga non includa &quot;[!UICONTROL AMO ID]&quot; per l&#39;entità. |
| [!UICONTROL Campaign Name] | Obbligatorio |
| [!UICONTROL Ad Group Name] | Obbligatorio |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] | Obbligatorio per modificare la descrizione. <b>Nota:</b> Per questo tipo di annuncio, la modifica della copia dell&#39;annuncio elimina l&#39;annuncio esistente e ne crea uno nuovo. |
| [!UICONTROL Display Path 1] | Obbligatorio per modificare il campo. |
| [!UICONTROL Display Path 2] | Obbligatorio per modificare il campo. |
| [!UICONTROL Creative Type] | Obbligatorio per creare o modificare lo stato di un annuncio di prodotto. |
| [!UICONTROL Creative Preferred Devices] | Facoltativo |
| [!UICONTROL Ad Status] | Obbligatorio per eliminare un annuncio. |
| \[Classificazione etichetta specifica dell’inserzionista\] | Facoltativo |
| [!UICONTROL Campaign ID] | Facoltativo |
| [!UICONTROL Ad Group ID] | Facoltativo |
| [!UICONTROL Ad ID] | Obbligatorio solo quando si modifica lo stato dell&#39;annuncio, a meno che la riga non includa a&rpar; colonne di proprietà dell&#39;annuncio sufficienti per identificare l&#39;annuncio o b&rpar; e &quot;[!UICONTROL AMO ID]&quot;. Tuttavia, se non includi né [!UICONTROL Ad ID] né [!UICONTROL AMO ID] e le colonne della proprietà dell&#39;annuncio corrispondono a più annunci, lo stato di uno solo degli annunci cambia. |
| [!UICONTROL AMO ID] | Obbligatorio per modificare o eliminare i dati a meno che non si includano l’ID entità e l’ID entità padre.<br><br>Search, Social e Commerce utilizzano il valore per determinare l&#39;identità corretta da modificare, ma non pubblicano l&#39;ID sulla rete di annunci. |

### Campi annuncio prodotto (acquisti)

Per ulteriori informazioni sulla creazione di annunci per acquisti, consulta &quot;[Implementare [!DNL Microsoft Advertising] campagne acquisti](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-workflows/microsoft-shopping-campaigns.html).&quot;

Per questo tipo di annuncio, utilizzare la riga &quot;[!UICONTROL Creative (except RSA)]&quot; nella finestra di dialogo [!UICONTROL Download Bulksheet].

Per una descrizione di ogni campo dati, vedere &quot;[Tutti i campi dati disponibili](#bulksheet-fields-all-microsoft).&quot;

| Campo | Obbligatorio |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obbligatorio a meno che ogni riga non includa &quot;[!UICONTROL AMO ID]&quot; per l&#39;entità. |
| [!UICONTROL Campaign Name] | Obbligatorio |
| [!UICONTROL Ad Group Name] | Obbligatorio |
| [!UICONTROL Promotion Line] | Facoltativo |
| [!UICONTROL Base URL/Final URL] | Facoltativo |
| [!UICONTROL Custom URL Param] | Facoltativo |
| [!UICONTROL Creative Type] | Obbligatorio per creare o modificare lo stato di un annuncio di prodotto. |
| [!UICONTROL Tracking Template] | Facoltativo |
| [!UICONTROL Ad Status] | Obbligatorio per eliminare un annuncio. |
| \[Classificazione etichetta specifica dell’inserzionista\] | Facoltativo |
| [!UICONTROL Constraints] | Facoltativo |
| [!UICONTROL Campaign ID] | Facoltativo |
| [!UICONTROL Ad Group ID] | Facoltativo |
| [!UICONTROL Ad ID] | Obbligatorio solo quando si modifica lo stato dell&#39;annuncio, a meno che la riga non includa a) un numero sufficiente di colonne di proprietà dell&#39;annuncio per identificare l&#39;annuncio oppure b) un &quot;[!UICONTROL AMO ID]&quot;. Tuttavia, se non includi né [!UICONTROL Ad ID] né [!UICONTROL AMO ID] e le colonne della proprietà dell&#39;annuncio corrispondono a più annunci, lo stato di uno solo degli annunci cambia. |
| [!UICONTROL AMO ID] | Obbligatorio per modificare o eliminare i dati a meno che non si includano l’ID entità e l’ID entità padre.<br><br>Search, Social e Commerce utilizzano il valore per determinare l&#39;identità corretta da modificare, ma non pubblicano l&#39;ID sulla rete di annunci. |

### Campi pubblicitari reattivi (multimediali)

Per questo tipo di annuncio, utilizzare la riga &quot;[!UICONTROL Creative (except RSA)]&quot; nella finestra di dialogo [!UICONTROL Download Bulksheet].

Per una descrizione di ogni campo dati, vedere &quot;[Tutti i campi dati disponibili](#bulksheet-fields-all-microsoft).&quot;

| Campo | Obbligatorio |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obbligatorio a meno che ogni riga non includa &quot;[!UICONTROL AMO ID]&quot; per l&#39;entità. |
| [!UICONTROL Campaign Name] | Obbligatorio |
| [!UICONTROL Ad Group Name] | Obbligatorio |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 15] | Per gli annunci reattivi, sono necessari [!UICONTROL Ad Title], [!UICONTROL Ad Title 2] e [!UICONTROL Ad Title 3] per creare annunci e tutti gli altri campi del titolo dell&#39;annuncio sono facoltativi. Per eliminare il valore esistente per un campo non obbligatorio, utilizzare il valore `[delete]` (comprese le parentesi). <b>Nota:</b> Per questo tipo di annuncio, la modifica della copia dell&#39;annuncio elimina l&#39;annuncio esistente e ne crea uno nuovo. |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | [!UICONTROL Description Line 1] e [!UICONTROL Description Line 2] sono necessari per creare annunci e [!UICONTROL Description Line 3] e [!UICONTROL Description Line 4] sono facoltativi. <b>Nota:</b> Per questo tipo di annuncio, la modifica della copia dell&#39;annuncio elimina l&#39;annuncio esistente e ne crea uno nuovo. |
| [!UICONTROL Business Name] | Obbligatorio per creare o eliminare un annuncio. |
| [!UICONTROL Call To Action] | Obbligatorio per creare un annuncio. |
| [!UICONTROL Call To Action Language] | Obbligatorio per creare un annuncio. |
| [!UICONTROL Base URL/Final URL] | Obbligatorio per creare un annuncio. |
| [!UICONTROL Creative Type] | Facoltativo. |
| [!UICONTROL Tracking Template] | Facoltativo |
| [!UICONTROL Ad Status] | Obbligatorio per eliminare un annuncio. |
| \[Classificazione etichetta specifica dell’inserzionista\] | Facoltativo |
| [!UICONTROL Campaign ID] | Facoltativo |
| [!UICONTROL Ad Group ID] | Facoltativo |
| [!UICONTROL Ad ID] | Obbligatorio solo quando si modifica lo stato dell&#39;annuncio, a meno che la riga non includa a) un numero sufficiente di colonne di proprietà dell&#39;annuncio per identificare l&#39;annuncio oppure b) un &quot;[!UICONTROL AMO ID]&quot;. Tuttavia, se non includi né [!UICONTROL Ad ID] né [!UICONTROL AMO ID] e le colonne della proprietà dell&#39;annuncio corrispondono a più annunci, lo stato di uno solo degli annunci cambia. |
| [!UICONTROL AMO ID] | Obbligatorio per modificare o eliminare i dati a meno che non si includano l’ID entità e l’ID entità padre.<br><br>Search, Social e Commerce utilizzano il valore per determinare l&#39;identità corretta da modificare, ma non pubblicano l&#39;ID sulla rete di annunci. |

### Campi degli annunci di ricerca reattivi

Per questo tipo di annuncio, utilizzare la riga &quot;[!UICONTROL Responsive Search Ad]&quot; nella finestra di dialogo [!UICONTROL Download Bulksheet].

Per una descrizione di ogni campo dati, vedere &quot;[Tutti i campi dati disponibili](#bulksheet-fields-all-microsoft).&quot;

| Campo | Obbligatorio |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obbligatorio a meno che ogni riga non includa &quot;[!UICONTROL AMO ID]&quot; per l&#39;entità. |
| [!UICONTROL Campaign Name] | Obbligatorio |
| [!UICONTROL Ad Group Name] | Obbligatorio |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 15] | Per gli annunci di ricerca responsive, sono necessari [!UICONTROL Ad Title], [!UICONTROL Ad Title 2] e [!UICONTROL Ad Title 3] per creare un annuncio e tutti gli altri campi del titolo dell&#39;annuncio sono facoltativi. Per eliminare il valore esistente per un campo non obbligatorio, utilizzare il valore `[delete]` (comprese le parentesi). |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | Facoltativo |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | Per gli annunci di ricerca responsive, sono necessari [!UICONTROL Description Line 1] e [!UICONTROL Description Line 2] per creare un annuncio e [!UICONTROL Description Line 3] e [!UICONTROL Description Line 4] sono facoltativi. Per eliminare il valore esistente, utilizzare il valore `[delete]` (comprese le parentesi). |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | Facoltativo |
| [!UICONTROL Display Path 1] | Facoltativo |
| [!UICONTROL Display Path 2] | Facoltativo |
| [!UICONTROL Base URL/Final URL] | Obbligatorio per creare un annuncio. |
| [!UICONTROL Custom URL Param] | Facoltativo |
| [!UICONTROL Creative Type] | Facoltativo |
| [!UICONTROL Tracking Template] | Facoltativo |
| [!UICONTROL Ad Status] | Obbligatorio per eliminare un annuncio. |
| \[Classificazione etichetta specifica dell’inserzionista\] | Facoltativo |
| [!UICONTROL Campaign ID] | Facoltativo |
| [!UICONTROL Ad Group ID] | Facoltativo |
| [!UICONTROL Ad ID] | Necessario per modificare o eliminare gli annunci a meno che la riga non includa un &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | Obbligatorio per modificare o eliminare gli annunci a meno che non includa l’ID annuncio. |

### Campi di annunci di testo

Per questo tipo di annuncio, utilizzare la riga &quot;[!UICONTROL Creative (except RSA)]&quot; nella finestra di dialogo [!UICONTROL Download Bulksheet].

>[!NOTE]
>
>Gli annunci di testo espansi erano obsoleti. Puoi eliminare solo gli annunci di testo esistenti.

Per una descrizione di ogni campo dati, vedere &quot;[Tutti i campi dati disponibili](#bulksheet-fields-all-microsoft).&quot;

| Campo | Obbligatorio |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obbligatorio a meno che ogni riga non includa &quot;[!UICONTROL AMO ID]&quot; per l&#39;entità. |
| [!UICONTROL Campaign Name] | Obbligatorio |
| [!UICONTROL Ad Group Name] | Obbligatorio |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 3] | Sola lettura |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] | Sola lettura |
| [!UICONTROL Display URL] | Sola lettura |
| [!UICONTROL Display Path 1] | Sola lettura |
| [!UICONTROL Display Path 2] | Sola lettura |
| [!UICONTROL Base URL/Final URL] | Sola lettura |
| [!UICONTROL Custom URL Param] | Sola lettura |
| [!UICONTROL Creative Type] | Facoltativo |
| [!UICONTROL Tracking Template] | Sola lettura |
| [!UICONTROL Creative Preferred Devices] | Sola lettura |
| [!UICONTROL Ad Status] | Obbligatorio |
| \[Classificazione etichetta specifica dell’inserzionista\] | Facoltativo |
| [!UICONTROL Campaign ID] | Facoltativo |
| [!UICONTROL Ad Group ID] | Facoltativo |
| [!UICONTROL Ad ID] | Obbligatorio solo quando si modifica lo stato dell&#39;annuncio, a meno che la riga non includa un &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | Obbligatorio per modificare o eliminare i dati a meno che non includa l’ID annuncio.<br><br>Search, Social e Commerce utilizzano il valore per determinare l&#39;identità corretta da modificare, ma non pubblicano l&#39;ID sulla rete di annunci. |

### Campi destinazione ricerca dinamica (targeting automatico)

>[!NOTE]
>
>Il supporto per la creazione non è disponibile.

Per una descrizione di ogni campo dati, vedere &quot;[Tutti i campi dati disponibili](#bulksheet-fields-all-microsoft).&quot;

| Campo | Obbligatorio |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obbligatorio a meno che ogni riga non includa &quot;[!UICONTROL AMO ID]&quot; per l&#39;entità. |
| [!UICONTROL Campaign Name] | Obbligatorio |
| [!UICONTROL Ad Group Name] | Obbligatorio |
| [!UICONTROL Auto Target Expression] | Obbligatorio. |
| [!UICONTROL Match Type] | Facoltativo |
| [!UICONTROL Max CPC] | Facoltativo |
| [!UICONTROL Custom URL Param] | Facoltativo |
| [!UICONTROL Target Status] | Necessario per eliminare una destinazione |
| \[Classificazione etichetta specifica dell’inserzionista\] | Facoltativo |
| [!UICONTROL Constraints] | Facoltativo |
| [!UICONTROL Campaign ID] | Facoltativo |
| [!UICONTROL Ad Group ID] | Facoltativo |
| [!UICONTROL Target ID] | Obbligatorio solo quando si modifica o si elimina la destinazione automatica, a meno che la riga non includa &quot;[!UICONTROL AMO ID]&quot; per la destinazione. |
| [!UICONTROL AMO ID] | Obbligatorio per modificare o eliminare i dati a meno che non si includano l’ID entità e l’ID entità padre.<br><br>Search, Social e Commerce utilizzano il valore per determinare l&#39;identità corretta da modificare, ma non pubblicano l&#39;ID sulla rete di annunci. |

### Campi gruppo di prodotti acquisti

Per una descrizione di ogni campo dati, vedere &quot;[Tutti i campi dati disponibili](#bulksheet-fields-all-microsoft).&quot;

| Campo | Obbligatorio |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obbligatorio a meno che ogni riga non includa &quot;[!UICONTROL AMO ID]&quot; per l&#39;entità. |
| [!UICONTROL Campaign Name] | Obbligatorio |
| [!UICONTROL Ad Group Name] | Obbligatorio |
| [!UICONTROL Match Type] | Obbligatorio per creare un gruppo di prodotti. |
| [!UICONTROL Max CPC] | Obbligatorio per creare un gruppo di prodotti. |
| [!UICONTROL Parent Product Groupings] | Obbligatorio |
| [!UICONTROL Product Grouping] | Obbligatorio |
| [!UICONTROL Partition Type] | Obbligatorio per creare un gruppo di prodotti. |
| [!UICONTROL Base URL/Final URL] | Obbligatorio |
| [!UICONTROL Tracking Template] | Facoltativo |
| [!UICONTROL Product Group Status] | Obbligatorio solo per eliminare un gruppo di prodotti. |
| \[Classificazione etichetta specifica dell’inserzionista\] | Facoltativo |
| [!UICONTROL Constraints] | Facoltativo |
| [!UICONTROL Campaign ID] | Facoltativo |
| [!UICONTROL Ad Group ID] | Facoltativo |
| [!UICONTROL Product Group ID] | Obbligatorio solo quando si modifica o si elimina il gruppo di prodotti, a meno che la riga non includa a) colonne di proprietà sufficienti per identificare il gruppo di prodotti o b) un &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | Obbligatorio per modificare o eliminare i dati a meno che non si includano l’ID entità e l’ID entità padre.<br><br>Search, Social e Commerce utilizzano il valore per determinare l&#39;identità corretta da modificare, ma non pubblicano l&#39;ID sulla rete di annunci. |

### Campi sitelink a livello di campagna

Per una descrizione di ogni campo dati, vedere &quot;[Tutti i campi dati disponibili](#bulksheet-fields-all-microsoft).&quot;

| Campo | Obbligatorio |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obbligatorio a meno che ogni riga non includa &quot;[!UICONTROL AMO ID]&quot; per l&#39;entità. |
| [!UICONTROL Campaign Name] | Obbligatorio |
| Riga descrizione 1 | Facoltativo |
| [!UICONTROL Description Line 2] | Facoltativo |
| [!UICONTROL Start Date] | Facoltativo |
| [!UICONTROL End Date] | Facoltativo |
| [!UICONTROL Base URL/Final URL] | Obbligatorio |
| [!UICONTROL Custom URL Param] | Facoltativo |
| [!UICONTROL Tracking Template] | Facoltativo |
| [!UICONTROL Creative Preferred Devices] | Facoltativo |
| [!UICONTROL Link Name] | Obbligatorio |
| [!UICONTROL Sitelink Status] | Obbligatorio solo per eliminare un sitelink. |
| [!UICONTROL Campaign ID] | Facoltativo |
| [!UICONTROL Sitelink ID] | Obbligatorio solo quando si modifica o si elimina il sitelink, a meno che la riga non includa a) colonne di proprietà sufficienti per identificare il sitelink o b) un &quot;[!UICONTROL AMO ID]&quot;. Tuttavia, se non includi né [!UICONTROL Sitelink ID] né [!UICONTROL AMO ID] e le colonne di proprietà corrispondono a più sitelink, lo stato di uno solo dei sitelink cambia.<br><br><b>Nota:</b> se si modificano le colonne delle proprietà del sitelink ad eccezione di Stato per un sitelink esistente e non si includono [!UICONTROL Sitelink ID] né [!UICONTROL AMO ID], verrà creato un nuovo sitelink e il sitelink esistente non verrà modificato. |
| [!UICONTROL AMO ID] | Obbligatorio per modificare o eliminare i dati a meno che non si includano l’ID entità e l’ID entità padre.<br><br>Search, Social e Commerce utilizzano il valore per determinare l&#39;identità corretta da modificare, ma non pubblicano l&#39;ID sulla rete di annunci. |

### Campi destinazione posizione

Per una descrizione di ogni campo dati, vedere &quot;[Tutti i campi dati disponibili](#bulksheet-fields-all-microsoft).&quot;

| Campo | Obbligatorio |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obbligatorio a meno che ogni riga non includa &quot;[!UICONTROL AMO ID]&quot; per l&#39;entità. |
| [!UICONTROL Campaign Name] | Obbligatorio |
| [!UICONTROL Location] | Obbligatorio |
| [!UICONTROL Location Type] | Necessario per creare una destinazione |
| [!UICONTROL Bid Adjustment] | Facoltativo |
| [!UICONTROL Location Status] | Obbligatorio solo per eliminare una destinazione di posizione. |
| [!UICONTROL Campaign ID] | Facoltativo |
| [!UICONTROL AMO ID] | Obbligatorio per modificare o eliminare i dati a meno che non includa l’ID campagna.<br><br>Search, Social e Commerce utilizzano il valore per determinare l&#39;identità corretta da modificare, ma non pubblicano l&#39;ID sulla rete di annunci. |

### Campi di destinazione per dispositivi a livello di campagna e di gruppo di annunci

Per una descrizione di ogni campo dati, vedere &quot;[Tutti i campi dati disponibili](#bulksheet-fields-all-microsoft).&quot;

| Campo | Obbligatorio |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obbligatorio a meno che ogni riga non includa &quot;[!UICONTROL AMO ID]&quot; per l&#39;entità. |
| [!UICONTROL Campaign Name] | Obbligatorio |
| [!UICONTROL Device] | Obbligatorio per eliminare una destinazione dispositivo. |
| [!UICONTROL Bid Adjustment] | Facoltativo |
| [!UICONTROL Ad Group Name] | Obbligatorio per le destinazioni dei dispositivi a livello di gruppo di annunci. Non applicabile per i target dispositivo a livello di campagna. |
| [!UICONTROL Device Target Status] | Obbligatorio solo per eliminare una destinazione dispositivo. |
| [!UICONTROL Campaign ID] | Facoltativo |
| [!UICONTROL Ad Group ID] | Facoltativo; applicabile solo per destinazioni dispositivo a livello di gruppo di annunci. |
| [!UICONTROL AMO ID] | Necessario per modificare o eliminare i dati a meno che non includiate l&#39;ID Device Target.<br><br>Search, Social e Commerce utilizzano il valore per determinare l&#39;identità corretta da modificare, ma non pubblicano l&#39;ID sulla rete di annunci. |

### Campi di destinazione RLSA a livello di campagna e di gruppo di annunci

Per una descrizione di ogni campo dati, vedere &quot;[Tutti i campi dati disponibili](#bulksheet-fields-all-microsoft).&quot;

| Campo | Obbligatorio |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obbligatorio a meno che ogni riga non includa &quot;[!UICONTROL AMO ID]&quot; per l&#39;entità. |
| [!UICONTROL Campaign Name] | Obbligatorio |
| [!UICONTROL Ad Group Name] | Obbligatorio per i target a livello di gruppo di annunci. Non applicabile per i target a livello di campagna. |
| [!UICONTROL Audience] | Obbligatorio per creare una nuova destinazione. |
| [!UICONTROL Target Type] | Facoltativo |
| [!UICONTROL Bid Adjustment] | Facoltativo |
| [!UICONTROL RLSA Target Status] | Obbligatorio per eliminare una destinazione. |
| [!UICONTROL Campaign ID] | Facoltativo |
| [!UICONTROL Ad Group ID] | Facoltativo; applicabile solo per target a livello di gruppo di annunci. |
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
