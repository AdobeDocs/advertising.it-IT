---
title: Gestire i vincoli per le unità di offerta di ricerca
description: Scopri i vincoli per limitare le offerte per le unità di offerta nelle campagne CPC nei portfolio legacy a livello di parola chiave.
feature: Search Campaign Management, Search Optimization
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2:
  - id: c800239a-06eb-4249-9aef-771973d24d35
source-git-commit: c074f430583e2d320eb4d47b4fc956c1822bd04a
workflow-type: tm+mt
source-wordcount: 2660
ht-degree: 0%

---

# Gestire i vincoli per le unità di offerta di ricerca

*Applicabile solo alle unità di offerta nelle campagne CPC in portfolio legacy a livello di parola chiave*

I vincoli dell&#39;unità di offerta sono regole che limitano le offerte ottimizzate per tutte le [unità di offerta](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/glossary.html) con modelli di costi e ricavi associati al vincolo.

## Informazioni sui vincoli

Ogni vincolo si applica a una valuta specifica e facoltativamente include le condizioni di attivazione che devono essere soddisfatte durante un periodo di valutazione dei dati specificato affinché la regola venga applicata. I dati da valutare possono includere tipo di canale, tipo di corrispondenza, dati di clic, dati di conversione o metriche derivate. Ad esempio, puoi limitare le offerte a uno specifico intervallo monetario, aumentare o diminuire continuamente le offerte di un determinato importo o fare offerte in base all’offerta media per il portfolio. Ogni vincolo ha una data di inizio applicabile e scade in una data specifica o viene applicato a tempo indeterminato.

Dopo aver impostato un vincolo, puoi assegnarlo a unità di offerta specifiche o a tutte le unità di offerta all’interno di specifici gruppi di annunci o campagne. Ogni unità di offerta può avere un vincolo. I vincoli vengono ereditati dalle entità figlio, ma possono essere ignorati. Un vincolo assegnato al livello più basso sovrascrive sempre un vincolo assegnato a un livello padre. Quando si assegna un vincolo a un&#39;unità di offerta, la licitazione funziona entro i vincoli specificati per tale unità di offerta, indipendentemente dal ricavo generato dall&#39;unità di offerta, quando l&#39;unità di offerta presenta modelli di costi e ricavi.

>[!CAUTION]
>
>Quando si assegnano vincoli a un&#39;unità di offerta, si ignora la decisione del sistema di ottimizzazione delle offerte e si assume personalmente la responsabilità del ROI su tale unità di offerta.

>[!NOTE]
>
>* I vincoli attivi limitano le offerte solo per le unità di offerta assegnate nei portfolio legacy ottimizzati a livello di parola chiave. Vengono ignorate per le unità di offerta che si trovano in portafogli ibridi, in portafogli attivi o che non si trovano in portfolio. **Suggerimento:** nelle impostazioni del portfolio, attiva l&#39;opzione portfolio su &quot;Regola automaticamente i limiti di budget delle campagne&quot;. Il valore &quot;Multiple&quot; consigliato è &quot;1&quot;.
>* I vincoli di offerta vengono ignorati per le unità di offerta prive di dati sufficienti per generare modelli di costi e ricavi.
>* (Campagne con una strategia di offerta CPC o eCPC) Quando un vincolo di offerta è in conflitto con un limite di offerta a livello di portafoglio, il vincolo sostituisce il limite a livello di portafoglio. Ad esempio, se l’offerta minima di un portfolio è di 5 USD ma si limita un’unità di offerta nel portfolio a un’offerta minima di 3 USD, l’unità di offerta è pari o superiore a 3 USD. La spesa complessiva per le unità di offerta vincolate, tuttavia, è determinata dal parametro [&quot;Spend Around Constraints&quot; del portfolio](#spend-around-constraints).
>* I vincoli operano sull’offerta di base. Qualsiasi tipo di regolazione dell’offerta rispetto all’offerta di base (ad esempio l’aumento dell’offerta per gli utenti finali sui dispositivi mobili) può spostare l’offerta al di fuori dell’intervallo consentito per il vincolo. Ad esempio, se il vincolo richiede un CPC massimo di 6 USD, l’offerta di base è già di 6 USD e il portfolio ottimizza automaticamente le regolazioni delle offerte per i dispositivi mobili al 50%-60%, il CPC massimo è di 9,00-9.60 USD — non di 6 USD.

### Tipi di vincoli {#constraint-types}

* **[!UICONTROL Bid]:** limita le offerte a un intervallo monetario.

* **[!UICONTROL Bid Shift]:** modifica continuamente le offerte ottimizzate per tutte le unità di offerta associate di un importo specificato, entro i limiti di offerta. Un cambiamento di offerta fa sì che i portfolio rilevanti sovrastino o sottoutilizzino l&#39;importo totale causato dal cambiamento di offerta, indipendentemente dall&#39;impostazione del portfolio &quot;Spend Around Constraints&quot; (Spendi in base ai vincoli). Nota: se l’offerta CPC corrente è già uguale o maggiore dell’offerta massima o uguale o inferiore all’offerta minima, il vincolo viene ignorato e l’offerta non viene modificata. Inoltre, i vincoli di spostamento delle offerte non vengono applicati alle unità di offerta prive di dati sufficienti per generare modelli di costi e ricavi.

* **[!UICONTROL Incremental Bidding]:** (applicabile solo alle parole chiave senza impression) Aumenta o diminuisce l&#39;offerta in modo incrementale a una velocità specificata fino a quando l&#39;offerta non raggiunge una destinazione designata.

* **[!UICONTROL Search Engine Min Bid]:** ([!DNL Google Ads] account) Utilizza le offerte CPC minime determinate dal motore di ricerca come offerte minime. Poiché il motore di ricerca cambia le offerte minime, l&#39;offerta cambia di conseguenza. Facoltativamente, puoi specificare limiti di offerta aggiuntivi per tutte le unità di offerta associate.

* **[!UICONTROL Impression Share]:** ([!DNL Google Ads] e [!DNL Microsoft Advertising] campagne CPC con solo corrispondenza esatta) Limita le offerte a un intervallo monetario quando gli annunci sono tra una quota di impression minima e massima. **Nota:** quando il vincolo non è conveniente, la funzionalità di ottimizzazione potrebbe sostituirlo.

### Quando applicare i vincoli

Alcuni motivi per limitare le unità di offerta sono i seguenti:

* Per esporre rapidamente parole chiave e annunci non testati.

* Per ridurre i rischi per nuovi portfolio, account, campagne e gruppi di annunci. Ad esempio, prima di lanciare un portfolio, puoi impostare le offerte massime per le unità di offerta a traffico elevato e quindi aumentare gradualmente i valori ogni giorno. Ciò consente al modello di offerta di adeguarsi ogni giorno senza il rischio di un aumento consistente delle offerte.

* Per assicurarti che le parole chiave di coda con tassi di conversione elevati non vengano riproposte.

* Per offrire termini specifici che sono fondamentali per il tuo marchio o durante le promozioni.

### Dove visualizzare informazioni sui vincoli nell’interfaccia utente

Oltre ad aprire la visualizzazione [[!UICONTROL Constraints]](#constraints-view), è possibile visualizzare le informazioni relative ai vincoli nei modi seguenti:

* Tutti i vincoli sono valori di etichetta per una singola [classificazione di etichetta](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/label-classifications/classification-about.html) denominata &quot;[!UICONTROL Constraints]&quot;.

  * &quot;[!UICONTROL Constraints]&quot; è incluso nell&#39;elenco &quot;[!UICONTROL Classifications]&quot; nelle impostazioni di visualizzazione predefinite e personalizzate e nei report pianificati. È possibile aggiungere la colonna in qualsiasi punto si desideri visualizzare i vincoli assegnati alle entità rilevanti.

  * Quando si scarica un bulksheet, &quot;[!UICONTROL Constraints]&quot; è elencato nella colonna &quot;[!UICONTROL Classifications]&quot; per le entità applicabili nella finestra di dialogo [!UICONTROL Download Bulksheet]. Quando si include la colonna, il bulksheet scaricato include tutti i vincoli assegnati alle entità rilevanti.

  La classificazione [!UICONTROL Constraints] non è inclusa nella visualizzazione [!UICONTROL Label Classifications]. La visualizzazione [!UICONTROL Constraints] è separata. Anche la classificazione [!UICONTROL Constraints] non è inclusa nel limite di classificazione delle 30 etichette.

* [Il [!UICONTROL Constraint Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/constraint-report.md) include i dati di costo, clic e (facoltativamente) conversione per i vincoli che utilizzano l&#39;architettura di classificazione delle etichette.

### Visualizzazione [!UICONTROL Constraints] {#constraints-view}

Nella vista [!UICONTROL Goals] > [!UICONTROL Constraints] sono elencati tutti i vincoli. Le colonne disponibili includono lo stato del vincolo, il tipo di vincolo, le date di inizio e fine, il numero di campagne, gruppi di annunci, parole chiave, annunci, posizionamenti, destinazioni automatiche e gruppi di prodotti a cui è associato il vincolo, impression, clic e dati sui costi e i dati sui ricavi per tutte le metriche di conversione visibili.<!-- Clarify why "Ads" is listed, unless it's to identify the relevant ads -->

>[!IMPORTANT]
>
>I dati sulle prestazioni per una riga nella visualizzazione [!UICONTROL Constraints] potrebbero non corrispondere ai dati sulle prestazioni per l&#39;entità di livello superiore a cui è assegnato il vincolo. Poiché un vincolo assegnato al livello più basso sovrascrive sempre un vincolo assegnato a un livello padre, è possibile che un vincolo assegnato a una campagna o a un gruppo di annunci non rimanga assegnato ai gruppi di annunci e alle parole chiave figlio. Ad esempio, se alla campagna A viene assegnato il vincolo A, tutti i gruppi di annunci e le parole chiave della campagna A ereditano automaticamente il vincolo A. Tuttavia, tali gruppi di annunci e parole chiave potrebbero in seguito essere assegnati ad altri vincoli, come il vincolo B, perdendo così la loro associazione con il vincolo A.

>[!NOTE]
>
>Assegnare vincoli alle unità di offerta e annullarne l&#39;assegnazione dalla vista di gestione delle entità pertinente (ad esempio dalla vista [!UICONTROL Campaigns] per i vincoli a livello di campagna).

#### Azioni disponibili

* [Crea un vincolo](#constraint-create).

* [Modifica impostazioni vincolo](#constraint-edit).

* [Modifica lo stato dei vincoli](#constraint-change-status).

## Creare un vincolo {#constraint-create}

1. Nel menu principale, fare clic su **[!UICONTROL Goals]>[!UICONTROL Constraints]**.

1. Nella barra degli strumenti superiore destra sopra la tabella dati, fare clic su **[!UICONTROL Create Constraint]**.

1. Immetti le [impostazioni vincolo](#constraint-settings).

   Per spostarsi tra la scheda [!UICONTROL Constraint Type] e la scheda [!UICONTROL Conditions], fare clic sulla scheda che si desidera aprire oppure sui pulsanti [!UICONTROL Next] e [!UICONTROL Back].

1. Fare clic su **[!UICONTROL Review and Save]** per rivedere le impostazioni.

1. Fare clic su **[!UICONTROL Save]**.

Dopo aver creato un vincolo, puoi [assegnarlo](#constraint-assign) a campagne, gruppi di annunci, parole chiave, posizionamenti e gruppi di prodotti a livello di unità.

## Modifica impostazioni vincolo {#constraint-edit}

È possibile modificare le impostazioni di un vincolo alla volta.

1. Nel menu principale, fare clic su **[!UICONTROL Goals]>[!UICONTROL Constraints]**.

1. (Facoltativo) Filtra l&#39;elenco [dalla barra degli strumenti](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) o da un&#39;intestazione [colonna](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md).

1. Selezionare la casella di controllo accanto al vincolo da modificare.

1. Nella barra degli strumenti Azioni in blocco, fare clic su ![Modifica](/help/search-social-commerce/assets/edit-new.png "Modifica").

1. Modifica le [impostazioni vincolo](#constraint-settings).

   Per spostarsi tra la scheda [!UICONTROL Constraint Type] e la scheda [!UICONTROL Conditions], fare clic sulla scheda che si desidera aprire oppure sui pulsanti [!UICONTROL Next] e [!UICONTROL Back].

1. Fare clic su **[!UICONTROL Review and Save]** per rivedere le impostazioni.

1. Fare clic su **[!UICONTROL Save]**.

## Modificare lo stato dei vincoli {#constraint-change-status}

È possibile sospendere qualsiasi vincolo attivo per disattivarlo. In seguito potrai abilitarlo modificando lo stato in *attivo*.

È inoltre possibile eliminare un vincolo che rimuove tutte le associazioni con i componenti conto e rende il vincolo non disponibile per utilizzi futuri. I dati del rapporto per il vincolo non sono più disponibili. **Nota:** Per dissociare semplicemente un vincolo da un componente account, vedi &quot;[Rimuovere i vincoli dalle unità di offerta di ricerca](#constraints-unassign).&quot;

1. Nel menu principale, fare clic su **[!UICONTROL Goals]>[!UICONTROL Constraints]**.

1. (Facoltativo) Filtra l&#39;elenco [dalla barra degli strumenti](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) o da un&#39;intestazione [colonna](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md).

1. Selezionare la casella di controllo accanto a ogni vincolo di cui si desidera modificare lo stato.

   Per suggerimenti sulla selezione di più righe, vedere &quot;[Selezionare più righe](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Nella barra degli strumenti delle azioni in blocco, fai clic sul pulsante di stato:

   * Per attivare tutte le righe selezionate, fare clic su ![Attiva](/help/search-social-commerce/assets/activate-new.png "Attiva").

   * Per sospendere tutte le righe selezionate, fare clic su ![Pausa](/help/search-social-commerce/assets/pause-new.png "Pausa").

   * Per eliminare tutte le righe selezionate, fare clic su ![Elimina](/help/search-social-commerce/assets/delete-new.png "Elimina").

1. Nel messaggio di conferma, fare clic su **[!UICONTROL Confirm]**.

## Impostazioni dei vincoli {#constraint-settings}

| Linguetta | Parametro | Descrizione |
|---|---|---|
| \[Informazioni di base\] | [!UICONTROL Constraint Name] | Un nome univoco per il vincolo. |
| | [!UICONTROL Currency] | La valuta in cui sono presentate le unità di offerta applicabili. Le unità di offerta per le quali viene utilizzata una valuta diversa vengono ignorate. |
| | [!UICONTROL Status] | Stato del vincolo:<ul><li>**Attivo:** (impostazione predefinita) Il vincolo viene applicato durante le condizioni e l&#39;intervallo di date specificati.</li><li>**Sospeso:** Il vincolo non è applicato.</li></ul> |
| [!UICONTROL Constraint Type] | [!UICONTROL Constraint Type] | Tipo di vincolo. Per le descrizioni dei tipi di vincolo e delle reti pubblicitarie idonee per ciascuno di essi, vedere &quot;[Tipi di vincolo](#constraint-types).&quot; |
| | [!UICONTROL Start Date] | Primo giorno in cui il vincolo ha effetto. Il valore predefinito è il giorno corrente. Per modificare la data, immettere una data o fare clic su ![Calendario](/help/search-social-commerce/assets/calendar-new.png "Calendario") per aprire il calendario e selezionare una data. |
| | [Data di fine] | Indica se il vincolo diventerà inefficace in una data specifica. Per applicare il vincolo a tempo indeterminato, ad esempio quando l’unità di offerta è fondamentale per il marchio dell’azienda, lascia vuoto il campo. Per terminare il vincolo in una data specifica, immettere una data o fare clic su ![Calendario](/help/search-social-commerce/assets/calendar-new.png "Calendario") per aprire il calendario e selezionare una data. **Nota:** il vincolo non può scadere prima di domani. |
| | [!UICONTROL Set constraint options for Bid] | ([!UICONTROL Bid] solo vincoli) Le impostazioni includono:<ul><li>**[!UICONTROL Min Bid]:** Offerta base minima per le unità di offerta associate.</li><li>**[!UICONTROL Max Bid]:** L&#39;offerta di base massima per le unità di offerta associate.</li></ul> |
| | [!UICONTROL Set constraint options for Bid Shift] | ([!UICONTROL Bid Shift] solo vincoli) Il tipo e l&#39;importo del turno di offerta da applicare continuamente all&#39;offerta di base:<ul><li>*[!UICONTROL Increases]:* Aumenta le offerte di un valore percentuale o valuta specificato. Immettere l&#39;importo da modificare, quindi selezionare *$* o *%*. Immettere inoltre **[!UICONTROL Max Limit]**, che è l&#39;offerta massima possibile quando viene applicato il vincolo. **Nota:** se l&#39;offerta CPC corrente è già uguale o maggiore di [!UICONTROL Max Limit], il vincolo viene ignorato e l&#39;offerta non viene modificata.</li><li>*[!UICONTROL Decreases]:* riduce le offerte di un valore percentuale o valuta specificato. Immettere l&#39;importo da modificare, quindi selezionare *$ o %*. Immettere anche **[!UICONTROL Min Limit]**, che è l&#39;offerta minima possibile (soglia minima) quando viene applicato il vincolo. **Nota:** se l&#39;offerta CPC corrente è già uguale o inferiore a [!UICONTROL Min Limit], il vincolo viene ignorato e l&#39;offerta non viene modificata.</li></ul>**Note:**<ul><li>Un cambiamento di offerta causerà una sovraspesa o una sottospesa dei portafogli rilevanti dell&#39;importo totale causato dal cambiamento di offerta, indipendentemente dall&#39;impostazione del portfolio per &quot;[!UICONTROL Spend Around Constraints]&quot;.</li><li>Se specifichi una data di fine per il vincolo e la funzionalità di ottimizzazione adegua automaticamente i limiti di spesa per le campagne nel portfolio, le offerte non si limitano a ripristinare gli importi originali dopo la data di fine, ma vengono adeguate in modo ottimale.</li><li>I cambiamenti di offerta non vengono applicati alle unità di offerta senza dati sufficienti per generare modelli di costi e ricavi.</li></ul> |
| | [!UICONTROL Set constraint options for Incremental Bidding] | ([!UICONTROL Incremental Bidding] solo vincoli) Un target di offerta e quanto e con quale frequenza aumentare o diminuire l&#39;offerta in modo incrementale fino a raggiungere il target:<ul><li>**[!UICONTROL Bid target]:** L&#39;importo dell&#39;offerta target.</li><li>**[!UICONTROL Incrementally change bids by]** e **[Tipo]:** Quanto aumentare o diminuire in modo incrementale le offerte e se modificare le offerte in base a un valore di valuta (**$**) o a una percentuale (*%*).</li><li>**[!UICONTROL Every __ days]:** con quale frequenza incrementare le offerte.</li></ul>Ad esempio, supponiamo che l&#39;offerta corrente per una delle parole chiave sia 100 centesimi e che si desideri modificare l&#39;offerta del 10% ogni giorno fino a raggiungere un obiettivo di offerta di 500 centesimi. Il Giorno 1, dopo l’impostazione del vincolo, l’offerta per tale parola chiave è 110 centesimi (offerta corrente + 10%). Il giorno 2, l&#39;offerta è di 120 centesimi (offerta corrente per il giorno 1 + 20%) e così via. Tuttavia, se l’obiettivo dell’offerta è di 50 centesimi e gli altri parametri sono gli stessi, le offerte diminuiscono in modo incrementale fino a raggiungere i 50 centesimi. |
| | [!UICONTROL Set constraint options for Search Engine Min Bid] | ([!UICONTROL Search Engine Min Bid] vincoli) Utilizza l&#39;offerta minima richiesta per mostrare un&#39;unità di offerta nella prima pagina dei risultati di ricerca in Google ([!UICONTROL Google First Page CPC]). Facoltativamente, inserisci un valore **[!UICONTROL Min Bid]** e/o un valore **[!UICONTROL Max Bid]** per definire l&#39;intervallo di offerte idonee per il vincolo. Ad esempio, se specifichi un [!UICONTROL Min Bid] di 2,50 USD e un [!UICONTROL Max Bid] di 4 USD, non farai un&#39;offerta sull&#39;unità di offerta se la prima offerta della pagina [!DNL Google Ads] è inferiore a 2,50 USD o superiore a 4 USD. |
| | [!UICONTROL Set constraint options for Impression Share] | ([!UICONTROL Impression Share] solo vincoli) Le impostazioni includono:<ul><li>**[!UICONTROL Min Bid]** (facoltativo) l&#39;offerta base minima per le unità di offerta associate.</li><li>**[!UICONTROL Max Bid]:** (facoltativo) l&#39;offerta di base massima per le unità di offerta associate.</li><li>**[!UICONTROL Min Impression Share]:** La quota di impression più bassa, in percentuale, che attiverà il vincolo per le unità di offerta applicabili. Deve essere compreso tra 10 e 90. **Nota:** quando il vincolo non è conveniente, la funzionalità di ottimizzazione potrebbe sostituirlo.</li><li>**[!UICONTROL Max Impression Share]:** la quota di impression più elevata, in percentuale, che attiverà il vincolo per le unità di offerta applicabili. Deve essere compreso tra 10 e 90.**Nota:** Se il vincolo non è conveniente, la funzionalità di ottimizzazione potrebbe sostituirlo.</li></ul>> |
| [!UICONTROL Conditions] | [!UICONTROL Condition Type] | Se applicare condizioni al vincolo:<ul><li>*[!UICONTROL No Condition]:* (impostazione predefinita) Il vincolo viene applicato incondizionatamente durante l&#39;intervallo di date specificato.</li><li>*[!UICONTROL Satisfy]:* Il vincolo viene applicato solo quando vengono soddisfatte le condizioni specificate durante un periodo di valutazione dei dati specificato.</li></ul> |
| | [!UICONTROL Data Evaluation Period] | (Quando sono impostate le condizioni) Il periodo di tempo per il quale valutare i dati per i criteri specificati. Se si seleziona *[!UICONTROL Custom date range],**&#x200B; specificare &#x200B;** [!UICONTROL Start Date] **&#x200B; e &#x200B;** [!UICONTROL End Date]** immettendo ogni data nel formato `MM-DD-YYYY` (ad esempio 03-29-2026 per il 29 marzo 2026) o facendo clic su ![Pulsante Calendario](/help/search-social-commerce/assets/calendar-new.png "Pulsante Calendario") per aprire il calendario e selezionare ogni data. |
| | [!UICONTROL When to Apply Constraints] | (Quando sono impostate le condizioni) Quante condizioni del filtro devono essere soddisfatte per applicare il vincolo:<ul><li>*[!UICONTROL Match All Filters]:* Applica il vincolo quando viene soddisfatta ogni condizione di filtro specificata.</li><li>*[!UICONTROL Match Any Filters]:* Applica il vincolo quando viene soddisfatta almeno una delle condizioni di filtro specificate.</li></ul> |
| | [!UICONTROL Filters] | (Quando le condizioni sono impostate) Uno o più criteri che devono essere soddisfatti. Per creare un filtro, seleziona una proprietà o una metrica dall’elenco. Per le proprietà (ad esempio [!UICONTROL Channel Type]), selezionare i valori applicabili nell&#39;elenco. Per le metriche (ad esempio [!UICONTROL Clicks]), selezionare un operatore, quindi immettere il valore applicabile. Ad esempio, per restituire solo unità di offerta con più di 100 clic, seleziona **Clic**, seleziona **maggiore di**, quindi immetti `100` nel campo di input.</li></ul> |

## Assegna vincoli alle unità di offerta di ricerca {#constraint-assign}

Puoi applicare vincoli di unità di offerta a qualsiasi campagna, gruppo di annunci, parola chiave, posizionamento o destinazione di ricerca dinamica (destinazione automatica).

Ogni entità può avere un solo vincolo. Potete assegnare un singolo vincolo a una o più entità contemporaneamente.

>[!NOTE]
>
>* Se successivamente modificate una parola chiave o la copia dell&#39;annuncio per un annuncio, creando in tal modo una nuova parola chiave o un nuovo annuncio, il vincolo non viene assegnato alla nuova entità.
>* Vedere le stesse istruzioni nella visualizzazione [[!UICONTROL Campaigns]](/help/search-social-commerce/new-ui/manage/campaigns/campaign-constraint-assignments-manage.md), [[!UICONTROL Ad Groups]](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-constraint-assignments-manage.md), [[!UICONTROL Keywords]](/help/search-social-commerce/new-ui/target/keywords/keyword-constraint-assignments-manage.md) o [[!UICONTROL Placements]](/help/search-social-commerce/new-ui/target/placements/placement-constraint-assignments-manage.md). <!-- ADD LINK WHEN AVAILABLE for dynamic search targets (auto targets). -->

1. Dal menu principale, apri la relativa vista di gestione.

   Ad esempio, per assegnare vincoli a livello di campagna, passa a [!UICONTROL Manage] > [!UICONTROL Campaigns].

1. (Facoltativo) Filtra l&#39;elenco [dalla barra degli strumenti](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) o da un&#39;intestazione [colonna](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md).

1. Selezionare la casella di controllo accanto a ogni entità a cui assegnare un singolo vincolo.

1. Nella barra degli strumenti delle azioni in blocco, fare clic su **+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Selezionate il vincolo.

1. Fare clic su **[!UICONTROL Assign Now]**.

## Annulla l’assegnazione dei vincoli dalle unità di offerta di ricerca {#constraints-unassign}

>[!NOTE]
>
>* Per eliminare un vincolo rendendolo non disponibile per un utilizzo futuro, vedere &quot;[Modificare lo stato dei vincoli](#constraint-change-status).&quot;
>* Vedere le stesse istruzioni nella visualizzazione [[!UICONTROL Campaigns]](/help/search-social-commerce/new-ui/manage/campaigns/campaign-constraint-assignments-manage.md), [[!UICONTROL Ad Groups]](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-constraint-assignments-manage.md), [[!UICONTROL Keywords]](/help/search-social-commerce/new-ui/target/keywords/keyword-constraint-assignments-manage.md) o [[!UICONTROL Placements]](/help/search-social-commerce/new-ui/target/placements/placement-constraint-assignments-manage.md). <!-- ADD LINK WHEN AVAILABLE for dynamic search targets (auto targets). -->

1. Nel menu principale, apri la vista di gestione pertinente.

   Ad esempio, per annullare l&#39;assegnazione dei vincoli a livello di campagna, passa a [!UICONTROL Manage] > [!UICONTROL Campaigns].

1. Selezionare la casella di controllo accanto a ogni entità da cui si desidera annullare l&#39;assegnazione dei vincoli.

1. Nella barra degli strumenti Azioni in blocco fare clic su **-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Fare clic su **[!UICONTROL Confirm]**.

>[!MORELIKETHIS]
>
>* [Gestione assegnazioni vincoli per le campagne](/help/search-social-commerce/new-ui/manage/campaigns/campaign-constraint-assignments-manage.md)
>* [Gestisci assegnazioni vincoli per gruppi di annunci](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-constraint-assignments-manage.md)
>* [Gestisci assegnazioni vincoli per parole chiave](/help/search-social-commerce/new-ui/target/keywords/keyword-constraint-assignments-manage.md)
>* [Gestisci assegnazioni vincoli per posizionamenti](/help/search-social-commerce/new-ui/target/placements/placement-constraint-assignments-manage.md)
>* [I [!UICONTROL Constraint Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/constraint-report.md)
