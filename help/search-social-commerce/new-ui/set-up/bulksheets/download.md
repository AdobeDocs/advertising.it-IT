---
title: (Nuova interfaccia) Scaricare/creare un file bulksheet
description: Scopri come creare file di bulksheet scaricando i dati dell’account per le reti di annunci nella nuova interfaccia utente di Search, Social e Commerce.
feature: Search Bulksheets
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2:
  - id: e58024d1-d6da-420c-80af-6be211808316
  - id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 47de92fd6d4b1d481380a58f75ec4735d95fca73
workflow-type: tm+mt
source-wordcount: 1637
ht-degree: 0%

---

# (Nuova interfaccia) Scaricare/creare un file bulksheet

Puoi creare i bulksheet utilizzando le impostazioni personalizzate per uno o più account su una o più [reti di annunci supportate](about.md#bulksheet-functionality-by-network). I bulksheet includono dati in Search, Social e Commerce.

Per le campagne sincronizzate, puoi facoltativamente sincronizzarti con la rete pubblicitaria prima di scaricare i dati per garantire che siano incluse le modifiche recenti dei dati sul lato rete pubblicitaria. Per tutte le reti di annunci, puoi facoltativamente generare nuovi URL di tracciamento dei clic da includere nel file.

1. Nel menu principale, fare clic su **[!UICONTROL Setup]** \> **[!UICONTROL Bulksheets]**.

1. Nella barra degli strumenti fare clic su **[!UICONTROL Bulk Operations]** \> **[!UICONTROL Download Bulksheet]**.

1. Specificare le [impostazioni per il bulksheet](#bulksheet-settings):

   1. Nella scheda **[!UICONTROL Selections]**, seleziona gli account, le campagne o i gruppi di annunci da includere e configurare le opzioni del bulksheet.

   1. (Facoltativo) Fare clic sulla scheda **[!UICONTROL Rows and Columns]**, specificare i componenti conto e gli stati dei componenti per i quali includere righe nel bulksheet, quindi specificare le colonne da includere per ogni componente selezionato.

      Per un elenco delle righe di bulksheet disponibili, vedi &quot;[Righe di bulksheet per rete di annunci](#bulksheet-rows-by-ad-network).&quot;

   1. (Facoltativo) Fai clic sulla scheda **[!UICONTROL Filters]**, quindi specifica i criteri per le campagne, i gruppi di annunci, gli annunci/creativi, le parole chiave, i posizionamenti e altre entità da includere nel bulksheet.

1. Fare clic su **[!UICONTROL Download]**.

All&#39;inizio dell&#39;attività, la finestra visualizza una notifica ma rimane aperta in modo da poter continuare a creare altri bulksheet, se necessario. Al momento della creazione del file, si riceve una notifica e-mail con un collegamento al file. A seconda della quantità di dati compilati, la notifica potrebbe richiedere alcuni minuti o più. Se la generazione del file non riesce, nella vista Bulksheet viene visualizzato un file di errore e viene inviata una notifica e-mail con un collegamento al file di errore.

## Impostazioni bulksheet {#bulksheet-settings}

### Scheda Selezioni {#bulksheet-selections-settings}

**\[Selezione account, campagna e gruppo di annunci\]**

Espandi la gerarchia di rete e account, quindi seleziona la casella di controllo accanto a ogni account, campagna o gruppo di annunci i cui dati da includere nel bulksheet:

* Per includere tutte le campagne e i gruppi di annunci di un account, seleziona la casella di controllo accanto al nome dell’account.

* Per includere campagne specifiche, espandi l’account e seleziona la casella di controllo accanto a ciascuna campagna da includere. Per includere gruppi di annunci specifici, espandi ulteriormente una campagna e seleziona la casella di controllo accanto a ciascun gruppo di annunci.

>[!NOTE]
>
>* Un singolo bulksheet può essere applicato a più account all’interno di più reti di annunci. Le colonne specifiche della rete di annunci sono etichettate in bulksheet con il nome della rete di annunci (ad esempio &quot;Operatori mobili (Google Ads)&quot;).
>* Per visualizzare il tipo di componente di un elemento, posizionare il cursore su di esso.
>* Per impostazione predefinita, sono elencati solo gli account attivi e abilitati e i relativi componenti attivi.

**[!UICONTROL Generate Tracking URLs]:** (facoltativo) include modelli di tracciamento e suffissi di pagina di destinazione (per reti di annunci applicabili) in account con modelli di tracciamento o URL di destinazione con codici di tracciamento incorporati in account con URL di destinazione, per parole chiave, annunci, posizionamenti, sitelink e [!DNL Google Ads] gruppi di prodotti nel bulksheet. Per impostazione predefinita, questa opzione è selezionata.

Quando questa opzione è selezionata, gli URL vengono generati in base ai parametri nella sezione [!UICONTROL Campaign Tracking] delle impostazioni account o delle impostazioni della campagna. Per impostazione predefinita, se gli URL di tracciamento esistono già, non vengono rigenerati a meno che non siano necessari nuovi URL (ad esempio se il tipo di corrispondenza della parola chiave, il testo dell’annuncio o i parametri di tracciamento dell’account sono cambiati).

>[!NOTE]
>
>* Se l’inserzionista utilizza il tracciamento delle conversioni di Adobe Advertising e l’account rilevante non è configurato per generare e caricare automaticamente gli URL di tracciamento, devi generare nuovi URL di tracciamento quando gli URL di base sono cambiati.
>* Se non selezioni questa opzione, puoi comunque generare gli URL di tracciamento in un secondo momento quando carichi o pubblichi il file.

**[!UICONTROL Perform pre-sync]:** (facoltativo) indica a Search, Social e Commerce di sincronizzare i file con le campagne specificate per garantire che tutti i dati siano uguali. Per impostazione predefinita, questa opzione non è selezionata.

>[!NOTE]
>
>Search, Social e Commerce si sincronizzano automaticamente con la rete di annunci una volta al giorno, ogni volta che rileva una nuova campagna sulla rete di annunci e ogni volta che modifichi i dati della campagna da Search, Social e Commerce. Seleziona questa opzione se pensi che le modifiche recenti ai dati della campagna o dell’account siano state apportate direttamente nella rete di annunci o utilizzando l’editor desktop della rete di annunci. La creazione di un bulksheet richiede più tempo quando si seleziona questa opzione.

**[!UICONTROL Bulksheet Name]:** Nome del nuovo bulksheet e tipo di file. Per impostazione predefinita, il file viene creato in formato con valori separati da tabulazioni ed è denominato in uno dei seguenti modi:

* (Per tutti gli account per una rete di annunci) `<search_engine name>_<creation date in the format MMDDYYYY>.tsv`
* (per un singolo account) `<account name>_<search_engine name>_<creation date in the format MMDDYYYY>.tsv`
* (per più account) `MultipleAccounts_<search_engine name>_<creation date in the format MMDDYYYY>.tsv`

È possibile rinominare il file. Il nome non può includere i seguenti caratteri: `# % & * | \ : " < > . ? /`

È possibile modificare il tipo di file. Le opzioni includono *[!UICONTROL .tsv]* (per valori separati da tabulazioni), *[!UICONTROL .txt (unicode)]* (per testo ASCII conforme a Unicode), *[!UICONTROL .csv]* (per valori separati da virgola) o *[!UICONTROL .zip]* (per il formato ZIP compresso, che si decomprime in un file TSV).

>[!TIP]
>
>Per i bulksheet che includono caratteri internazionali, utilizza il formato TSV o TXT.

### Scheda Righe e colonne {#bulksheet-rows-columns-settings}

**[!UICONTROL Bulksheet Rows]:** le entità e i relativi stati da includere come righe di dati nel bulksheet, con una riga per voce. Ad esempio, se includi campagne attive, il bulksheet include una riga per campagna attiva. Sono incluse solo le entità selezionate con gli stati selezionati. I valori predefiniti sono preselezionati in base alla rete di annunci specificata. Per impostazione predefinita, vengono incluse solo le istanze attive delle entità selezionate.

Per aggiungere o rimuovere entità, selezionare o deselezionare le caselle di controllo accanto alle entità. Per aggiungere o rimuovere stati per un&#39;entità, fate clic sul menu di stato accanto all&#39;entità, quindi selezionate o deselezionate le caselle di controllo relative agli stati applicabili.

Per un elenco delle righe disponibili per rete di annunci, vedi &quot;[Righe bulksheet per rete di annunci](#bulksheet-rows-by-ad-network).&quot;

**[!UICONTROL Cascading Status Hierarchy]:** Filtra le entità figlio in base a quelle con gli stati di entità padre specificati, utilizzando un&#39;operazione AND. Ad esempio, se selezioni &quot;Campagna attiva&quot;, &quot;Gruppo attivo&quot; e &quot;Parola chiave attiva&quot;, il bulksheet include solo le parole chiave attive nei gruppi di annunci attivi nelle campagne attive.

Se non selezioni questa opzione, lo stato principale non viene considerato e il filtro utilizza un’operazione OR. Ad esempio, se selezioni &quot;Campagna attiva&quot;, &quot;Gruppo attivo&quot; e &quot;Parola chiave attiva&quot;, il bulksheet include tutte le campagne attive, tutti i gruppi di annunci attivi indipendentemente dallo stato della campagna principale e tutte le parole chiave attive indipendentemente dallo stato della campagna principale e del gruppo di annunci.

**[!UICONTROL Bulksheet Columns]:** Le colonne da includere nel file di bulksheet scaricato:

* *[!UICONTROL AMO ID]:* (obbligatorio se &quot;[!UICONTROL SE ID]&quot; non è selezionato) Include un identificatore univoco generato da [!DNL Adobe] per ogni entità/riga. Search, Social e Commerce utilizzano il valore per determinare l’identità corretta da modificare, ma non lo pubblicano sulla rete di annunci. In seguito, è possibile modificare i dati per l&#39;entità utilizzando [!UICONTROL AMO ID] come identificatore, anziché l&#39;ID entità e gli ID entità padre.

* *[!UICONTROL SE ID]:* (obbligatorio se &quot;[!UICONTROL AMO ID]&quot; non è selezionato) Include l&#39;identificatore univoco della rete di annunci per ogni colonna inclusa e le relative entità padre. In seguito, se si modificano i dati per qualsiasi entità utilizzando [!UICONTROL SE ID] come identificatore, è necessario includere anche le righe per le entità padre (inclusi i relativi valori [!UICONTROL SE ID]).

* *[!UICONTROL Platform]:* Include una colonna [!UICONTROL Platform] all&#39;inizio di ogni riga per indicare la piattaforma pubblicitaria (ad esempio &quot;Baidu&quot;).

* *[!UICONTROL Acct Name]:* (obbligatorio se &quot;[!UICONTROL AMO ID]&quot; non è selezionato) Include il nome dell&#39;account di rete dell&#39;annuncio per ogni entità/riga.

* \[Colonne specifiche dell&#39;entità\]: per includere tutte le colonne, nessuna o solo le colonne selezionate rilevanti per ogni entità selezionata in [!UICONTROL Bulksheet Rows], fare clic su ![Punta freccia destra](/help/search-social-commerce/assets/compressed-item.png "Punta freccia destra") accanto al nome dell&#39;entità per espanderla, quindi selezionare o deselezionare le caselle di controllo per le singole colonne. Per impostazione predefinita, tutte le colonne pertinenti sono incluse per ogni riga di entità selezionata.

>[!TIP]
>
>Accertati di includere colonne adeguate per identificare l’elemento in ogni riga del file bulksheet. Ad esempio, se includi righe di parole chiave per il selettore [!UICONTROL Bulksheet Rows] ma escludi tutte le colonne relative alle parole chiave, il bulksheet risultante includerà una riga per ogni istanza di parola chiave senza modo di identificare quale istanza di parola chiave appartiene a una riga specifica. In questo caso, non puoi utilizzare il bulksheet per aggiornare i dati a meno che non aggiungi manualmente la colonna ID e i valori appropriati.

### Scheda Filtri {#bulksheet-filters-settings}

Criteri per campagne, gruppi di annunci, annunci/creativi, parole chiave e/o posizionamenti specifici da includere nel bulksheet:

1. Selezionate un parametro (nome o ID entità o qualsiasi elemento di un contenuto creativo, di una parola chiave o di un posizionamento), selezionate un operatore e quindi immettete il valore applicabile.

   Ad esempio, per restituire solo gli annunci con &quot;scarpe&quot; nel titolo di un account [!DNL Google Ads], selezionare *[!UICONTROL Headline]*, selezionare *[!UICONTROL contains]*, quindi immettere `shoes` nel campo di input.

1. (Per applicare ulteriori filtri) Per ogni filtro aggiuntivo, fare clic su **[!UICONTROL +Add Filter]**, selezionare **[!UICONTROL AND]** o **[!UICONTROL OR]**, selezionare un elemento annuncio o una parola chiave e un operatore, quindi immettere il valore applicabile.

## Righe bulksheet per rete di annunci {#bulksheet-rows-by-ad-network}

| Riga bulksheet | [!DNL Baidu] | [!DNL Google Ads] | [!DNL LY Ads] | [!DNL Microsoft Advertising] | [!DNL Naver] | [!DNL Pinterest] | [!DNL Yahoo! Display Network] | [!DNL Yahoo Native] | [!DNL Yandex] | Note |
|----|----|----|----|-------|----|----|----|----|----|----|
| [!UICONTROL Campaign] | Sì | Sì | Sì | Sì | Sì | Sì | Sì | Sì | Sì | — |
| [!UICONTROL Adgroup] | Sì | Sì | Sì | Sì | Sì | Sì | Sì | Sì | Sì | — |
| [!UICONTROL Creative] *o* [!UICONTROL Creative (except RSA)] | Sì | Sì | Sì | Sì | — | — | Sì | Sì | Sì | ([!DNL Google Ads]) Utilizzare per tutti i tipi di annunci ad eccezione degli annunci di ricerca responsive, disponibili nella riga [!UICONTROL Responsive Search Ad]. |
| [!UICONTROL Responsive Search Ad] | — | Sì | — | Sì | — | — | — | — | — | — |
| [!UICONTROL Keyword] | Sì | Sì | Sì | Sì | Sì | Sì | — | Sì | Sì | Da utilizzare solo per parole chiave non negative. Per visualizzare le parole chiave negative create a livello di campagna o di gruppo di annunci, utilizza la riga [!UICONTROL Campaign Negative Keyword] o [!UICONTROL Adgroup Negative Keyword] quando disponibile. |
| [!UICONTROL Promoted Pin] | — | — | — | — | — | Sì | — | — | — | — |
| [!UICONTROL Placement] | — | Sì | — | — | — | — | — | — | — | — |
| [!UICONTROL Auto Target] | — | Sì | — | Sì | — | — | — | — | — | Utilizza per destinazioni di ricerca dinamica per un gruppo di annunci. |
| [!UICONTROL Shopping Product Group] | — | Sì | — | Sì | — | — | — | — | — | — |
| [!UICONTROL Campaign Site Link] | — | Sì | — | Sì | — | — | — | Sì | — | — |
| [!UICONTROL Campaign Negative Keyword] | Sì | Sì | Sì | Sì | — | — | — | Sì | — | Da utilizzare solo per parole chiave negative create a livello di campagna o di gruppo di annunci. Per visualizzare le parole chiave non negative, utilizzare la riga [!UICONTROL Keyword] quando disponibile. |
| [!UICONTROL Campaign Negative Website] | — | Sì | — | Sì | — | — | — | Sì | — | — |
| [!UICONTROL Adgroup Site Link] | — | Sì | — | — | — | — | — | Sì | — | — |
| [!UICONTROL Creative Site Link] | — | — | — | — | — | — | — | — | Sì | — |
| [!UICONTROL Adgroup Negative Keyword] | Sì | Sì | Sì | Sì | — | — | — | Sì | — | — |
| [!UICONTROL Adgroup Negative Website] | — | Sì | — | Sì | — | — | — | — | — | — |
| [!UICONTROL Campaign Location Target] | Sì | Sì | Sì | Sì | — | — | — | Sì | — | — |
| [!UICONTROL Adgroup Location Target] | — | — | — | Sì | — | — | — | Sì | — | — |
| [!UICONTROL Campaign Device Target] | — | Sì | — | Sì | — | — | — | Sì | — | — |
| [!UICONTROL Adgroup Device Target] | — | Sì | — | Sì | — | — | — | Sì | — | — |
| [!UICONTROL Campaign RLSA Target] | — | Sì | — | Sì | — | — | — | — | — | — |
| [!UICONTROL Adgroup RLSA Target] | — | Sì | — | Sì | — | — | — | — | — | — |
| [!UICONTROL Campaign RLSA Negative] | — | Sì | — | — | — | — | — | — | — | — |
| [!UICONTROL Adgroup RLSA Negative] | — | Sì | — | — | — | — | — | — | — | — |

Per informazioni dettagliate sulle colonne obbligatorie e facoltative per ciascuna rete di annunci, consulta gli articoli sul formato dei dati del bulksheet specifico per la rete di annunci:

* [Dati dei bulksheet obbligatori e facoltativi per  [!DNL Baidu]  account](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-baidu.md)
* [Dati dei bulksheet obbligatori e facoltativi per  [!DNL Google Ads]  account](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md)
* [Dati dei bulksheet obbligatori e facoltativi per  [!DNL LY Ads]  account](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-japan.md)
* [Dati dei bulksheet obbligatori e facoltativi per  [!DNL Microsoft Advertising]  account](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md)
* [Dati dei bulksheet obbligatori e facoltativi per  [!DNL Naver]  account](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md)
* [Dati dei bulksheet obbligatori e facoltativi per  [!DNL Yahoo! Display Network]  account](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-display-network.md)
* [Dati dei bulksheet obbligatori e facoltativi per  [!DNL Yandex]  account](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yandex.md)

>[!MORELIKETHIS]
>
>* [(Nuova interfaccia) Informazioni sulla gestione dei dati della campagna tramite bulksheet](about.md)
>* [(Nuova interfaccia) Carica un bulksheet o un file di errore corretto](upload.md)
>* [(Nuova interfaccia) Pubblica i bulksheet o correggi i file di errore](post.md)
>* [(Nuova interfaccia) Convalida pagine di destinazione in file bulksheet](validate-landing-pages.md)
