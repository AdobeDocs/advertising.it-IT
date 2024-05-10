---
title: Scaricare/creare un file bulksheet
description: Scopri come creare file di bulksheet scaricando i dati dell’account per le reti di annunci.
exl-id: a3fcef52-3d36-462e-a975-c741d003326e
feature: Search Bulksheets
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '1759'
ht-degree: 0%

---

# Scaricare/creare un file bulksheet

È possibile creare i bulksheet utilizzando le impostazioni personalizzate per uno o più account su uno o più [reti pubblicitarie supportate](bulksheet-about.md#bulksheet-functionality-by-network). I bulksheet includono dati in Search, Social e Commerce.

Per le campagne sincronizzate, puoi facoltativamente sincronizzarti con la rete pubblicitaria prima di scaricare i dati per garantire che siano incluse le modifiche recenti dei dati sul lato rete pubblicitaria. Per tutte le reti di annunci, puoi facoltativamente generare nuovi URL di tracciamento dei clic da includere nel file.

>[!NOTE]
>
>È inoltre possibile [creare un file di bulksheet basato sulle colonne visibili in una vista gestione campagne](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md).

1. Nel menu principale, fai clic su **[!UICONTROL Search]** > **[!UICONTROL Campaigns]** > **[!UICONTROL Bulksheets]**.

1. Nella barra degli strumenti, fai clic su **[!UICONTROL Download Bulksheet]**.

1. Specifica la [impostazioni bulksheet](#bulksheet-download-settings):

1. Il giorno **[!UICONTROL Selections]** , immettere o selezionare le informazioni nei campi.

1. (Facoltativo) Fai clic su **[!UICONTROL Rows and Columns]** , specificare i componenti conto e gli stati dei componenti per i quali includere righe nel bulksheet, quindi specificare le colonne da includere per ciascun componente selezionato.

   Per un elenco delle righe di bulksheet disponibili, vedi &quot;[Righe bulksheet per rete di annunci](#bulksheet-rows-by-ad-network).&quot;

1. (Facoltativo) Fai clic su **[!UICONTROL Filters]** e quindi indicare i criteri per campagne, gruppi di annunci, annunci/creativi, parole chiave, posizionamenti e altre entità specifici da includere nel bulksheet:

   1. Seleziona un parametro (nome o ID entità; o qualsiasi elemento di un annuncio, parola chiave o posizionamento), seleziona un operatore e quindi inserisci il valore applicabile. Ad esempio, per restituire solo gli annunci il cui titolo contiene &quot;scarpe&quot; per un [!DNL Google Ads] account, seleziona *Titolo*, seleziona *[!UICONTROL contains]*, quindi immettere `shoes` nel campo di input.

   1. (Per applicare altri filtri) Per ogni filtro aggiuntivo, fai clic su **[!UICONTROL +Add Filter]**, seleziona **[!UICONTROL AND]** o **[!UICONTROL OR]**, seleziona un elemento annuncio o una parola chiave e un operatore, quindi inserisci il valore applicabile.

1. Clic **[!UICONTROL Download]**.

Quando l&#39;attività ha inizio, la finestra visualizza una notifica ma rimane aperta, in modo da poter continuare a creare ulteriori bulksheet, se lo si desidera. Eventuali filtri ed esclusioni specificati applicabili a qualsiasi nuovo account selezionato vengono mantenuti. All&#39;inizio dell&#39;attività, il file viene elencato nella visualizzazione Bulksheet. Al momento della creazione del file, si riceve una notifica e-mail con un collegamento al file. A seconda della quantità di dati compilati, la notifica potrebbe richiedere alcuni minuti o più. Se tuttavia la generazione del file non riesce, nella vista Bulksheet viene visualizzato un file di errore e viene inviata una notifica e-mail con un collegamento al file di errore.

## Impostazioni download bulksheet {#bulksheet-download-settings}

| Linguetta | Parametro | Descrizione |
|----|----|----|
| [!UICONTROL Selections] | [!UICONTROL SE Accounts] | Account, campagne o gruppi di annunci in cui caricare i dati:<ul><li>Per selezionare un account e tutte le relative campagne e gruppi di annunci, seleziona la casella di controllo accanto al nome dell’account, quindi fai clic su >> per spostarlo in [!UICONTROL Selected Filters] colonna.</li><li>Per selezionare singole campagne o gruppi di annunci, fai clic su accanto all’account per espanderlo, (se necessario) fai clic su accanto alla campagna per espanderla, seleziona la casella di controllo accanto al nome della campagna o del gruppo di annunci, quindi fai clic su >> per spostarlo in [!UICONTROL Selected Filters] colonna. Ad esempio, per ottenere i dati solo per la campagna 1 nell’account 1, espandi l’account 1, seleziona la casella di controllo accanto a Campagna 1, quindi spostalo nell’area [!UICONTROL Selected Filters] colonna.</li></ul><b>Note:</b><ul><li>Un singolo bulksheet può essere applicato a più account all’interno di più reti di annunci. Le colonne specifiche della rete di annunci sono etichettate in bulksheet con il nome della rete di annunci (ad esempio &quot;Operatori mobili (Google Ads)&quot;).</li><li>Per visualizzare il tipo di componente di un elemento, posizionare il cursore su di esso.</li><li>Per le campagne, la prima lettera del nome della rete di annunci è tra parentesi dopo il nome dell’account (ad esempio &quot;Acme Realty (G)&quot; per un [!DNL Google Ads] account).</li><li>Per impostazione predefinita, sono elencati solo gli account attivi e abilitati e i relativi componenti attivi. Per visualizzare i componenti in pausa ed eliminati, fai clic su ![Freccia giù](/help/search-social-commerce/assets/arrow-down-expand.png "Freccia giù") accanto a [!UICONTROL Show] e seleziona **[!UICONTROL All]. |
| | [!UICONTROL Generate Tracking URLs] | (Facoltativo) Include modelli di tracciamento e suffissi di pagina di destinazione (per reti di annunci applicabili) in account con modelli di tracciamento, oppure URL di destinazione con codici di tracciamento incorporati in account con URL di destinazione, per parole chiave, annunci, posizionamenti, sitelink e [!DNL Google Ads] gruppi di prodotti nel bulksheet. Per impostazione predefinita, questa opzione è selezionata.<br><br>Quando questa opzione è selezionata, gli URL vengono generati in base ai parametri nella sezione [!UICONTROL Campaign Tracking] sezione delle impostazioni account o delle impostazioni campagna. Per impostazione predefinita, se gli URL di tracciamento esistono già, non vengono rigenerati a meno che non siano necessari nuovi URL (ad esempio se il tipo di corrispondenza della parola chiave, il testo dell’annuncio o i parametri di tracciamento dell’account sono cambiati).<br><br><b>Note:</b><ul><li>Se l’inserzionista utilizza il tracciamento delle conversioni di Adobi Advertising e l’account rilevante non è configurato per generare e caricare automaticamente gli URL di tracciamento, devi generare nuovi URL di tracciamento quando gli URL di base sono cambiati.</li><li>Se non selezioni questa opzione, puoi comunque generare gli URL di tracciamento in un secondo momento quando carichi o pubblichi il file.</li></ul> |
| | [!UICONTROL Perform Pre-sync] | (Facoltativo) Indica a Search, Social e Commerce di sincronizzare i relativi file con le campagne specificate per garantire che tutti i dati siano uguali. Per impostazione predefinita, questa opzione non è selezionata.<br><b>Nota:</b> Search, Social e Commerce si sincronizzano automaticamente con la rete di annunci una volta al giorno, ogni volta che rileva una nuova campagna sulla rete di annunci e ogni volta che modifichi i dati della campagna da Search, Social e Commerce. Seleziona questa opzione se pensi che le modifiche recenti ai dati della campagna o dell’account siano state apportate direttamente nella rete di annunci o utilizzando l’editor desktop della rete di annunci. La creazione di un bulksheet richiede più tempo quando si seleziona questa opzione. |
| | [!UICONTROL Bulksheet Name] | Nome del nuovo bulksheet e tipo di file. Per impostazione predefinita, il file viene creato in formato con valori separati da tabulazioni ed è denominato in uno dei seguenti modi:<ul><li>(per tutti gli account della rete di annunci) `&lt;search_engine name&gt;_&lt;creation date in the format MMDDYYYY&gt;.tsv`</li><li>(per account singoli) `&lt;account name&gt;_&lt;search_engine name&gt;_&lt;creation date in the format MMDDYYYY&gt;.tsv`</li><li>(per più account) `MultipleAccounts_&lt;search_engine name&gt;_&lt;creation date in the format MMDDYYYY&gt;.tsv`.</li></ul>È possibile rinominare il file. Il nome non può includere i seguenti caratteri: `# % &amp; * | \ : &quot; &lt; &gt; . ? or /`.<br><br>È possibile modificare il tipo di file. Le opzioni includono *[!UICONTROL .tsv]* (per valori separati da tabulazioni), *[!UICONTROL .txt]* (per testo ASCII conforme a Unicode), *[!UICONTROL .csv]* (per valori separati da virgola), oppure *[!UICONTROL .zip]* (per il formato ZIP compresso, che si decomprime in un file TSV).<br><br><b>Suggerimento</b> Per i bulksheet che includono caratteri internazionali, utilizza il formato TSV o TXT. |
| [!UICONTROL Rows and Columns] | [!UICONTROL Bulksheet Rows] | Entità e stati corrispondenti da includere nel bulksheet, con una riga di dati per voce. Ad esempio, se includi campagne attive, il bulksheet include una riga per campagna attiva. Sono incluse solo le entità selezionate con gli stati selezionati. I valori predefiniti sono preselezionati in base alla rete di annunci specificata. Per impostazione predefinita, vengono incluse solo le istanze attive delle entità selezionate. Per un elenco delle righe di bulksheet disponibili, vedi &quot;[Righe bulksheet per rete di annunci](#bulksheet-rows-by-ad-network).&quot;<br><br>Per aggiungere o rimuovere entità, selezionate o deselezionate rispettivamente le caselle di controllo accanto alle entità. Per aggiungere o rimuovere stati per un&#39;entità, fare clic su accanto al menu di stato, quindi selezionare o deselezionare rispettivamente le caselle di controllo accanto alle entità. |
| | [!UICONTROL Cascading Status Hierarchy] | Filtra l&#39;ambito delle entità figlio in base a quelli con gli stati di entità padre specificati, utilizzando un&#39;operazione AND. Ad esempio, se selezioni &quot;Campagna attiva&quot;, &quot;Gruppo attivo&quot; e &quot;Parola chiave attiva&quot;, il bulksheet include solo le parole chiave attive nei gruppi di annunci attivi nelle campagne attive.<br><br>Se non selezioni questa opzione, lo stato principale non viene considerato e il filtro utilizza un’operazione OR. Ad esempio, se selezioni &quot;Campagna attiva&quot;, &quot;Gruppo attivo&quot; e &quot;Parola chiave attiva&quot;, il bulksheet include tutte le campagne attive, tutti i gruppi di annunci attivi, indipendentemente dallo stato della campagna principale e tutte le parole chiave attive, indipendentemente dallo stato della campagna principale e del gruppo di annunci. |
| | [!UICONTROL Bulksheet Columns] | Colonne da includere nel file di bulksheet scaricato:<ul><li>*[!UICONTROL AMO ID]*: (obbligatorio se &quot;[!UICONTROL SE ID]&quot; non è selezionato) Include un [!DNL Adobe]Identificatore univoco generato da, per ogni entità/riga. Search, Social e Commerce utilizzano il valore per determinare l’identità corretta da modificare, ma non lo pubblicano sulla rete di annunci. In seguito, puoi modificare i dati per l’entità utilizzando [!UICONTROL AMO ID] come identificatore, anziché come ID entità e ID entità padre.</li><li>*[!UICONTROL SE ID]*: (obbligatorio se &quot;[!UICONTROL AMO ID]&quot;non è selezionato) Include l’identificatore univoco della rete di annunci per ogni colonna inclusa e le relative entità principali. In seguito, se modifichi i dati per qualsiasi entità utilizzando [!UICONTROL SE ID] come identificatore, è necessario includere anche le righe per le entità padre (incluse le relative [!UICONTROL SE ID] valori).</li><li>*[!UICONTROL Platform]*: include una [!UICONTROL Platform column] all’inizio di ogni riga per indicare la piattaforma dell’annuncio (ad esempio &quot;Baidu&quot;).</li><li>*[!UICONTROL Acct Name]*: (obbligatorio se &quot;[!UICONTROL AMO ID]&quot; non è selezionato) Include il nome dell’account di rete dell’annuncio per ogni entità/riga.</li><li>\[Colonne da includere\]: per includere tutte, nessuna o solo le colonne selezionate rilevanti per ogni entità selezionata nel [!UICONTROL Bulksheet Rows] sezione. Per visualizzare le singole colonne relative a un’entità, fai clic su ![Freccia destra](/help/search-social-commerce/assets/compressed-item.png "Freccia destra") accanto al nome dell’entità. Per impostazione predefinita, tutte le colonne pertinenti sono incluse per ogni riga di entità selezionata. Deseleziona la casella di controllo accanto a un’entità o a una singola colonna per escluderla dal bulksheet.</li></ul><br><br><b>Suggerimento</b> Accertati di includere colonne adeguate per identificare l’elemento in ogni riga del file bulksheet. Ad esempio, supponiamo che tu includa righe di parole chiave per il [!UICONTROL Bulksheet Rows] ma sono escluse tutte le colonne relative alle parole chiave. Il bulksheet risultante include una riga per ogni istanza di parola chiave. Tuttavia, poiché non sono incluse colonne relative alle parole chiave, nemmeno l’AMO ID o l’SE ID, non è possibile identificare quale istanza della parola chiave si riferisce a una riga specifica e non è possibile utilizzare il bulksheet per aggiornare i dati, a meno che non si aggiungano manualmente la colonna ID e i valori appropriati. |
| [!UICONTROL Filters] | | Criteri per campagne, gruppi di annunci, annunci/creativi, parole chiave e/o posizionamenti specifici da includere nel bulksheet:<ol><li>Selezionate un parametro (nome o ID entità o qualsiasi elemento di un contenuto creativo, di una parola chiave o di un posizionamento), selezionate un operatore e quindi immettete il valore applicabile.<br>Ad esempio, per restituire solo gli annunci il cui titolo contiene &quot;scarpe&quot; per un [!DNL Google Ads] account, seleziona *[!UICONTROL Headline]*, seleziona *[!UICONTROL contains]*, quindi immettere `shoes` nel campo di input.</li><li>(Per applicare altri filtri) Per ogni filtro aggiuntivo, fai clic su **[!UICONTROL +Add Filter]**, seleziona **[!UICONTROL AND]** o **[!UICONTROL OR]**, seleziona un elemento annuncio o una parola chiave e un operatore, quindi inserisci il valore applicabile.</li></ul> |

## Righe bulksheet per rete di annunci {#bulksheet-rows-by-ad-network}

| Riga bulksheet | [!DNL Baidu] | [!DNL Google Ads] | [!DNL Microsoft Advertising] | [!DNL Naver] | [!DNL Pinterest] | [!DNL Yahoo! Display Network] | [!DNL Yahoo! Japan Ads] | [!DNL Yahoo Native] | Yandex | Note |
|----|----|----|----|-------|----|----|----|----|----|----|
| [!UICONTROL Campaign] | Sì | Sì | Sì | Sì | Sì | Sì | Sì | Sì | Sì | — |
| [!UICONTROL Adgroup] | Sì | Sì | Sì | Sì | Sì | Sì | Sì | Sì | Sì | — |
| [!UICONTROL Creative] *o* [!UICONTROL Creative (except RSA)] | Sì | Sì | Sì | — | — | Sì | Sì | Sì | Sì | ([!DNL Google  Ads]) Utilizzare per tutti i tipi di annunci ad eccezione degli annunci di ricerca responsive, che sono disponibili nel [!UICONTROL Responsive Search Ad] riga. |
| [!UICONTROL Responsive Search Ad] | — | Sì | Sì | — | — | — | — | — | — | — |
| [!UICONTROL Keyword] | Sì | Sì | Sì | Sì | Sì | — | Sì | Sì | Sì | Da utilizzare solo per parole chiave non negative. Per visualizzare le parole chiave negative create a livello di campagna o di gruppo di annunci, utilizza [!UICONTROL Campaign Negative Keyword] o [!UICONTROL Adgroup Negative Keyword] riga quando disponibile. |
| [!UICONTROL Promoted Pin] | — | — | — | — | Sì | — | — | — | — | — |
| [!UICONTROL Placement] | — | Sì | — | — | — | — | — | — | — | — |
| [!UICONTROL Auto Target] | — | Sì | Sì | — | — | — | — | — | — | Utilizza per destinazioni di ricerca dinamica per un gruppo di annunci. |
| [!UICONTROL Shopping Product Group] | — | Sì | Sì | — | — | — | — | — | — | — |
| [!UICONTROL Campaign Site Link] | — | Sì | Sì | — | — | — | — | Sì | — | — |
| [!UICONTROL Campaign Negative Keyword] | Sì | Sì | Sì | — | — | — | Sì | Sì | — | Da utilizzare solo per parole chiave negative create a livello di campagna o di gruppo di annunci. Per visualizzare le parole chiave non negative, utilizzare [!UICONTROL Keyword] riga quando disponibile. |
| [!UICONTROL Campaign Negative Website] | — | Sì | Sì | — | — | — | — | Sì | — | — |
| [!UICONTROL Adgroup Site Link] | — | Sì | — | — | — | — | — | Sì | — | — |
| [!UICONTROL Creative Site Link] | — | — | — | — | — | — | — | — | Sì | — |
| [!UICONTROL Adgroup Negative Keyword] | Sì | Sì | Sì | — | — | — | Sì | Sì | — | — |
| [!UICONTROL Adgroup Negative Website] | — | Sì | Sì | — | — | — | — | — | — | — |
| [!UICONTROL Campaign Location Target] | Sì | Sì | Sì | — | — | — | Sì | Sì | — | — |
| [!UICONTROL Adgroup Location Target] | — | — | Sì | — | — | — | — | Sì | — | — |
| [!UICONTROL Campaign Device Target] | — | Sì | Sì | — | — | — | — | Sì | — | — |
| [!UICONTROL Adgroup Device Target] | — | Sì | Sì | — | — | — | — | Sì | — | — |
| [!UICONTROL Campaign RLSA Target] | — | Sì | Sì | — | — | — | — | — | — | — |
| [!UICONTROL Adgroup RLSA Target] | — | Sì | Sì | — | — | — | — | — | — | — |
| [!UICONTROL Campaign RLSA Negative] | — | Sì | — | — | — | — | — | — | — | — |
| [!UICONTROL Adgroup RLSA Negative] | — | Sì | — | — | — | — | — | — | — | — |

>[!MORELIKETHIS]
>
>* [Informazioni sulla gestione dei dati della campagna tramite bulksheet](bulksheet-about.md)
>* [Pubblica i bulksheet o i file di errore corretti](bulksheet-post.md)
>* [Convalidare le pagine di destinazione in file bulksheet](bulksheet-validate-landing-pages.md)
>* [Esportare un file bulksheet generato o caricato](bulksheet-export.md)
