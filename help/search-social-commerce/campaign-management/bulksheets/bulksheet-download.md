---
title: Scaricare/creare un file bulksheet
description: Scopri come creare file di bulksheet scaricando i dati dell’account per le reti di annunci.
exl-id: a3fcef52-3d36-462e-a975-c741d003326e
feature: Search Bulksheets
source-git-commit: cb65108fcc60c11b901e3b43c292ad5a94192b9f
workflow-type: tm+mt
source-wordcount: '1759'
ht-degree: 0%

---

# Scaricare/creare un file bulksheet

Puoi creare i bulksheet utilizzando le impostazioni personalizzate per uno o più account su una o più [reti di annunci supportate](bulksheet-about.md#bulksheet-functionality-by-network). I bulksheet includono dati in Search, Social e Commerce.

Per le campagne sincronizzate, puoi facoltativamente sincronizzarti con la rete pubblicitaria prima di scaricare i dati per garantire che siano incluse le modifiche recenti dei dati sul lato rete pubblicitaria. Per tutte le reti di annunci, puoi facoltativamente generare nuovi URL di tracciamento dei clic da includere nel file.

>[!NOTE]
>
>Puoi anche [creare un file bulksheet basato sulle colonne visibili in una visualizzazione di gestione campagne](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md).

1. Nel menu principale, fare clic su **[!UICONTROL Search, Social, & Commerce]** > **[!UICONTROL Campaigns]** > **[!UICONTROL Bulksheets]**.

1. Nella barra degli strumenti fare clic su **[!UICONTROL Download Bulksheet]**.

1. Specificare le [impostazioni per il bulksheet](#bulksheet-download-settings):

1. Nella scheda **[!UICONTROL Selections]** immettere o selezionare le informazioni nei campi.

1. (Facoltativo) Fare clic sulla scheda **[!UICONTROL Rows and Columns]**, specificare i componenti conto e gli stati dei componenti per i quali includere righe nel bulksheet, quindi specificare le colonne da includere per ogni componente selezionato.

   Per un elenco delle righe di bulksheet disponibili, vedi &quot;[Righe di bulksheet per rete di annunci](#bulksheet-rows-by-ad-network).&quot;

1. (Facoltativo) Fai clic sulla scheda **[!UICONTROL Filters]**, quindi indica i criteri per campagne, gruppi di annunci, annunci/creativi, parole chiave, posizionamenti e altre entità specifici da includere nel bulksheet:

   1. Seleziona un parametro (nome o ID entità; o qualsiasi elemento di un annuncio, parola chiave o posizionamento), seleziona un operatore e quindi inserisci il valore applicabile. Ad esempio, per restituire solo gli annunci con &quot;scarpe&quot; nel titolo di un account [!DNL Google Ads], selezionare *Titolo*, selezionare *[!UICONTROL contains]*, quindi immettere `shoes` nel campo di input.

   1. (Per applicare ulteriori filtri) Per ogni filtro aggiuntivo, fare clic su **[!UICONTROL +Add Filter]**, selezionare **[!UICONTROL AND]** o **[!UICONTROL OR]**, selezionare un elemento annuncio o una parola chiave e un operatore, quindi immettere il valore applicabile.

1. Fare clic su **[!UICONTROL Download]**.

Quando l&#39;attività ha inizio, la finestra visualizza una notifica ma rimane aperta, in modo da poter continuare a creare ulteriori bulksheet, se lo si desidera. Eventuali filtri ed esclusioni specificati applicabili a qualsiasi nuovo account selezionato vengono mantenuti. All&#39;inizio dell&#39;attività, il file viene elencato nella visualizzazione Bulksheet. Al momento della creazione del file, si riceve una notifica e-mail con un collegamento al file. A seconda della quantità di dati compilati, la notifica potrebbe richiedere alcuni minuti o più. Se tuttavia la generazione del file non riesce, nella vista Bulksheet viene visualizzato un file di errore e viene inviata una notifica e-mail con un collegamento al file di errore.

## Impostazioni download bulksheet {#bulksheet-download-settings}

| Linguetta | Parametro | Descrizione |
|----|----|----|
| [!UICONTROL Selections] | [!UICONTROL SE Accounts] | Account, campagne o gruppi di annunci in cui caricare i dati:<ul><li>Per selezionare un account e tutte le relative campagne e gruppi di annunci, selezionare la casella di controllo accanto al nome dell&#39;account, quindi fare clic su >> per spostarlo nella colonna [!UICONTROL Selected Filters].</li><li>Per selezionare singole campagne o gruppi di annunci, fai clic su accanto all’account per espanderlo, (se necessario) fai clic su accanto alla campagna per espanderla, seleziona la casella di controllo accanto al nome della campagna o del gruppo di annunci, quindi fai clic su >> per spostarlo nella colonna [!UICONTROL Selected Filters]. Ad esempio, per ottenere i dati solo per la campagna 1 nell&#39;account 1, espandere Account 1, selezionare la casella di controllo accanto a Campaign 1, quindi spostarlo nella colonna [!UICONTROL Selected Filters].</li></ul><b>Note:</b><ul><li>Un singolo bulksheet può essere applicato a più account all’interno di più reti di annunci. Le colonne specifiche della rete di annunci sono etichettate in bulksheet con il nome della rete di annunci (ad esempio &quot;Operatori mobili (Google Ads)&quot;).</li><li>Per visualizzare il tipo di componente di un elemento, posizionare il cursore su di esso.</li><li>Per le campagne, la prima lettera del nome della rete di annunci è tra parentesi dopo il nome dell&#39;account, ad esempio &quot;Acme Realty (G)&quot; per un account [!DNL Google Ads].</li><li>Per impostazione predefinita, sono elencati solo gli account attivi e abilitati e i relativi componenti attivi. Per visualizzare i componenti in pausa ed eliminati, fare clic su ![freccia giù](/help/search-social-commerce/assets/arrow-down-expand.png "freccia giù") accanto a [!UICONTROL Show] e selezionare **[!UICONTROL All]. |
| | [!UICONTROL Generate Tracking URLs] | (Facoltativo) Include modelli di tracciamento e suffissi di pagina di destinazione (per reti di annunci applicabili) in account con modelli di tracciamento, oppure URL di destinazione con codici di tracciamento incorporati in account con URL di destinazione, per parole chiave, annunci, posizionamenti, sitelink e [!DNL Google Ads] gruppi di prodotti nel bulksheet. Per impostazione predefinita, questa opzione è selezionata.<br><br>Quando questa opzione è selezionata, gli URL vengono generati in base ai parametri nella sezione [!UICONTROL Campaign Tracking] delle impostazioni account o delle impostazioni della campagna. Per impostazione predefinita, se gli URL di tracciamento esistono già, non vengono rigenerati a meno che non siano necessari nuovi URL (ad esempio se il tipo di corrispondenza della parola chiave, il testo dell’annuncio o i parametri di tracciamento dell’account sono cambiati).<br><br><b>Note:</b><ul><li>Se l’inserzionista utilizza il tracciamento delle conversioni di Adobe Advertising e l’account rilevante non è configurato per generare e caricare automaticamente gli URL di tracciamento, devi generare nuovi URL di tracciamento quando gli URL di base sono cambiati.</li><li>Se non selezioni questa opzione, puoi comunque generare gli URL di tracciamento in un secondo momento quando carichi o pubblichi il file.</li></ul> |
| | [!UICONTROL Perform Pre-sync] | (Facoltativo) Indica a Search, Social e Commerce di sincronizzare i relativi file con le campagne specificate per garantire che tutti i dati siano uguali. Per impostazione predefinita, questa opzione non è selezionata.<br><b>Nota:</b> Search, Social e Commerce si sincronizzano automaticamente con la rete pubblicitaria una volta al giorno, ogni volta che rileva una nuova campagna nella rete pubblicitaria e ogni volta che si modificano i dati della campagna dall&#39;interno di Search, Social e Commerce. Seleziona questa opzione se pensi che le modifiche recenti ai dati della campagna o dell’account siano state apportate direttamente nella rete di annunci o utilizzando l’editor desktop della rete di annunci. La creazione di un bulksheet richiede più tempo quando si seleziona questa opzione. |
| | [!UICONTROL Bulksheet Name] | Nome del nuovo bulksheet e tipo di file. Per impostazione predefinita, il file viene creato in formato con valori separati da tabulazioni ed è denominato in uno dei seguenti modi:<ul><li>(per tutti gli account della rete di annunci) `&lt;search_engine name&gt;_&lt;creation date in the format MMDDYYYY&gt;.tsv`</li><li>(per account singoli) `&lt;account name&gt;_&lt;search_engine name&gt;_&lt;creation date in the format MMDDYYYY&gt;.tsv`</li><li>(per più account) `MultipleAccounts_&lt;search_engine name&gt;_&lt;creation date in the format MMDDYYYY&gt;.tsv`.</li></ul>È possibile rinominare il file. Il nome non può includere i seguenti caratteri: `# % &amp; * | \ : &quot; &lt; &gt; . ? or /`.<br><br>È possibile modificare il tipo di file. Le opzioni includono *[!UICONTROL .tsv]* (per valori separati da tabulazioni), *[!UICONTROL .txt]* (per testo ASCII conforme a Unicode), *[!UICONTROL .csv]* (per valori separati da virgola) o *[!UICONTROL .zip]* (per il formato ZIP compresso, che si decomprime in un file TSV).<br><br><b>Suggerimento:</b> Per i bulksheet che includono caratteri internazionali, utilizza il formato TSV o TXT. |
| [!UICONTROL Rows and Columns] | [!UICONTROL Bulksheet Rows] | Entità e stati corrispondenti da includere nel bulksheet, con una riga di dati per voce. Ad esempio, se includi campagne attive, il bulksheet include una riga per campagna attiva. Sono incluse solo le entità selezionate con gli stati selezionati. I valori predefiniti sono preselezionati in base alla rete di annunci specificata. Per impostazione predefinita, vengono incluse solo le istanze attive delle entità selezionate. Per un elenco delle righe di bulksheet disponibili, vedi &quot;[Righe di bulksheet per rete di annunci](#bulksheet-rows-by-ad-network).&quot;<br><br>Per aggiungere o rimuovere entità, selezionare o deselezionare rispettivamente le caselle di controllo accanto alle entità. Per aggiungere o rimuovere stati per un&#39;entità, fare clic su accanto al menu di stato, quindi selezionare o deselezionare rispettivamente le caselle di controllo accanto alle entità. |
| | [!UICONTROL Cascading Status Hierarchy] | Filtra l&#39;ambito delle entità figlio in base a quelli con gli stati di entità padre specificati, utilizzando un&#39;operazione AND. Ad esempio, se selezioni &quot;Campagna attiva&quot;, &quot;Gruppo attivo&quot; e &quot;Parola chiave attiva&quot;, il bulksheet include solo le parole chiave attive nei gruppi di annunci attivi nelle campagne attive.<br><br>Se non si seleziona questa opzione, lo stato padre non viene considerato e il filtro utilizza un&#39;operazione OR. Ad esempio, se selezioni &quot;Campagna attiva&quot;, &quot;Gruppo attivo&quot; e &quot;Parola chiave attiva&quot;, il bulksheet include tutte le campagne attive, tutti i gruppi di annunci attivi, indipendentemente dallo stato della campagna principale e tutte le parole chiave attive, indipendentemente dallo stato della campagna principale e del gruppo di annunci. |
| | [!UICONTROL Bulksheet Columns] | Colonne da includere nel file di bulksheet scaricato:<ul><li>*[!UICONTROL AMO ID]*: (obbligatorio se &quot;[!UICONTROL SE ID]&quot; non è selezionato) Include un identificatore univoco generato da [!DNL Adobe] per ogni entità/riga. Search, Social e Commerce utilizzano il valore per determinare l’identità corretta da modificare, ma non lo pubblicano sulla rete di annunci. In seguito, è possibile modificare i dati per l&#39;entità utilizzando [!UICONTROL AMO ID] come identificatore, anziché l&#39;ID entità e gli ID entità padre.</li><li>*[!UICONTROL SE ID]*: (obbligatorio se &quot;[!UICONTROL AMO ID]&quot; non è selezionato) Include l&#39;identificatore univoco della rete di annunci per ogni colonna inclusa e le relative entità padre. In seguito, se si modificano i dati per qualsiasi entità utilizzando [!UICONTROL SE ID] come identificatore, è necessario includere anche le righe per le entità padre (inclusi i relativi valori [!UICONTROL SE ID]).</li><li>*[!UICONTROL Platform]*: include un [!UICONTROL Platform column] all&#39;inizio di ogni riga per indicare la piattaforma pubblicitaria (ad esempio &quot;Baidu&quot;).</li><li>*[!UICONTROL Acct Name]*: (obbligatorio se &quot;[!UICONTROL AMO ID]&quot; non è selezionato) Include il nome dell&#39;account di rete dell&#39;annuncio per ogni entità/riga.</li><li>\[Colonne da includere\]: per includere tutte, nessuna o solo le colonne selezionate rilevanti per ogni entità selezionata nella sezione [!UICONTROL Bulksheet Rows]. Per visualizzare le singole colonne relative a un&#39;entità, fare clic su ![Freccia destra](/help/search-social-commerce/assets/compressed-item.png "Freccia destra") accanto al nome dell&#39;entità. Per impostazione predefinita, tutte le colonne pertinenti sono incluse per ogni riga di entità selezionata. Deseleziona la casella di controllo accanto a un’entità o a una singola colonna per escluderla dal bulksheet.</li></ul><br><br><b>Suggerimento:</b> Assicurarsi di includere colonne adeguate per identificare l&#39;elemento in ogni riga del file bulksheet. Si supponga, ad esempio, di includere righe di parole chiave per il selettore [!UICONTROL Bulksheet Rows], ma di escludere tutte le colonne relative alle parole chiave. Il bulksheet risultante include una riga per ogni istanza di parola chiave. Tuttavia, poiché non sono incluse colonne relative alle parole chiave, nemmeno l’AMO ID o l’SE ID, non è possibile identificare quale istanza della parola chiave si riferisce a una riga specifica e non è possibile utilizzare il bulksheet per aggiornare i dati, a meno che non si aggiungano manualmente la colonna ID e i valori appropriati. |
| [!UICONTROL Filters] | | Criteri per campagne, gruppi di annunci, annunci/creativi, parole chiave e/o posizionamenti specifici da includere nel bulksheet:<ol><li>Selezionate un parametro (nome o ID entità o qualsiasi elemento di un contenuto creativo, di una parola chiave o di un posizionamento), selezionate un operatore e quindi immettete il valore applicabile.<br>Ad esempio, per restituire solo gli annunci con &quot;scarpe&quot; nel titolo di un account [!DNL Google Ads], selezionare *[!UICONTROL Headline]*, selezionare *[!UICONTROL contains]*, quindi immettere `shoes` nel campo di input.</li><li>(Per applicare ulteriori filtri) Per ogni filtro aggiuntivo, fare clic su **[!UICONTROL +Add Filter]**, selezionare **[!UICONTROL AND]** o **[!UICONTROL OR]**, selezionare un elemento annuncio o una parola chiave e un operatore, quindi immettere il valore applicabile.</li></ul> |

## Righe bulksheet per rete di annunci {#bulksheet-rows-by-ad-network}

| Riga bulksheet | [!DNL Baidu] | [!DNL Google Ads] | [!DNL Microsoft Advertising] | [!DNL Naver] | [!DNL Pinterest] | [!DNL Yahoo! Display Network] | [!DNL Yahoo! Japan Ads] | [!DNL Yahoo Native] | Yandex | Note |
|----|----|----|----|-------|----|----|----|----|----|----|
| [!UICONTROL Campaign] | Sì | Sì | Sì | Sì | Sì | Sì | Sì | Sì | Sì | — |
| [!UICONTROL Adgroup] | Sì | Sì | Sì | Sì | Sì | Sì | Sì | Sì | Sì | — |
| [!UICONTROL Creative] *o* [!UICONTROL Creative (except RSA)] | Sì | Sì | Sì | — | — | Sì | Sì | Sì | Sì | ([!DNL Google  Ads]) Utilizzare per tutti i tipi di annunci ad eccezione degli annunci di ricerca responsive, disponibili nella riga [!UICONTROL Responsive Search Ad]. |
| [!UICONTROL Responsive Search Ad] | — | Sì | Sì | — | — | — | — | — | — | — |
| [!UICONTROL Keyword] | Sì | Sì | Sì | Sì | Sì | — | Sì | Sì | Sì | Da utilizzare solo per parole chiave non negative. Per visualizzare le parole chiave negative create a livello di campagna o di gruppo di annunci, utilizza la riga [!UICONTROL Campaign Negative Keyword] o [!UICONTROL Adgroup Negative Keyword] quando disponibile. |
| [!UICONTROL Promoted Pin] | — | — | — | — | Sì | — | — | — | — | — |
| [!UICONTROL Placement] | — | Sì | — | — | — | — | — | — | — | — |
| [!UICONTROL Auto Target] | — | Sì | Sì | — | — | — | — | — | — | Utilizza per destinazioni di ricerca dinamica per un gruppo di annunci. |
| [!UICONTROL Shopping Product Group] | — | Sì | Sì | — | — | — | — | — | — | — |
| [!UICONTROL Campaign Site Link] | — | Sì | Sì | — | — | — | — | Sì | — | — |
| [!UICONTROL Campaign Negative Keyword] | Sì | Sì | Sì | — | — | — | Sì | Sì | — | Da utilizzare solo per parole chiave negative create a livello di campagna o di gruppo di annunci. Per visualizzare le parole chiave non negative, utilizzare la riga [!UICONTROL Keyword] quando disponibile. |
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
>* [Pubblica bulksheet o file di errore corretti](bulksheet-post.md)
>* [Convalida pagine di destinazione in file bulksheet](bulksheet-validate-landing-pages.md)
>* [Esporta un file bulksheet generato o caricato](bulksheet-export.md)
