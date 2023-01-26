---
title: Impostazioni di posizionamento
description: Consulta le descrizioni delle impostazioni di posizionamento disponibili.
feature: DSP Placements
exl-id: 36097132-e589-4d49-bf86-54f61eae5b67
source-git-commit: 7055a9b9d3a68ef2f690e146128d6946e713586a
workflow-type: tm+mt
source-wordcount: '3416'
ht-degree: 0%

---

# Impostazioni di posizionamento

## [!UICONTROL Basics]

**[!UICONTROL Placement name]** Nome del posizionamento.

>[!TIP]
>Utilizza una convenzione di denominazione adatta alla tua situazione. Una convenzione di denominazione consigliata è &quot;*\&lt;campaign name=&quot;&quot;>: \&lt;ad unit=&quot;&quot;>: \&lt;duration>: \&lt;targeting>*.&quot;

**[!UICONTROL Status]:** Lo stato del posizionamento: *[!UICONTROL Active]* (impostazione predefinita) o *[!UICONTROL Paused]*.

>[!TIP]
>La best practice prevede di sospendere il posizionamento fino a quando non sei pronto per avviarlo.

**[!UICONTROL Details]:** (Sola lettura) Il tipo di annuncio applicabile, l’account che sta creando o creando il posizionamento e la campagna principale. Per visualizzare ulteriori dettagli, fai clic su **[!UICONTROL Show more]**.

**[!UICONTROL Templates]:** Apre un elenco di modelli di posizionamento esistenti. Per compilare automaticamente le impostazioni di targeting da un modello:

1. Effettua una delle seguenti operazioni:

   * Per riutilizzare tutte le destinazioni da un modello, seleziona la casella di controllo accanto al nome del modello.

   * Per riutilizzare singoli tipi di destinazione da un modello, espandi il nome del modello e seleziona la casella di controllo accanto ai tipi di destinazione che desideri riutilizzare.

1. Clic **[!UICONTROL Apply]**.

**[!UICONTROL Ad specs for forecast]:** (Solo formati di annunci video) La durata dell&#39;annuncio e/o le specifiche dell&#39;annuncio, utilizzate per calcolare la proiezione Previsione sulla destra. I campi variano in base al tipo di annuncio.

**[!UICONTROL Environment]:** (Solo per video universali e formato) Gli ambienti del dispositivo (Desktop, Mobile, Connected TV) da includere come destinazioni nel posizionamento.

**[!UICONTROL Placement tags]:** (Facoltativo) Parole chiave o soprannomi per facilitare l’individuazione di questo posizionamento.

## Obiettivi

**[!UICONTROL Package]:** (Facoltativo) Un pacchetto a cui è assegnato il posizionamento. Fai clic su ![Modifica](/help/dsp/assets/edit.png) per selezionare e creare un pacchetto esistente o crearne uno nuovo. Quando assegni il posizionamento a un pacchetto, la [!UICONTROL Goals] viene aggiornata con le date di volo, l’obiettivo di consegna e il budget del pacchetto.

**[!UICONTROL Flight Dates]:** La data di inizio e la data di fine del posizionamento. Gli annunci approvati possono essere eseguiti durante il volo quando il posizionamento è attivo e assegnato a un pacchetto o a una campagna attivi.

Per impostazione predefinita, le date del pacchetto (se applicabile) o della campagna vengono compilate automaticamente.

>[!NOTE]
>
>* Le date del volo devono essere incluse nelle date del volo della campagna e nelle date del volo del pacchetto.


### Posizionamenti assegnati ai pacchetti con imballaggio a livello di pacchetto

**[!UICONTROL Placement Funding]:** Come assegnare un budget al posizionamento:

* *[!UICONTROL Optimize based on performance]:* Controlla il budget a livello di pacchetto.
* *[!UICONTROL Set a fixed budget cap]:* Consente di impostare un budget per il posizionamento giornaliero, settimanale, mensile o completo. Immetti un valore e una durata (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

**[!UICONTROL Max Bid]:** Massimo per 1000 impression.

**[!UICONTROL Placement Pre-bid Filters]:** È necessario rispettare fino a cinque soglie KPI (ad esempio una metrica di visualizzabilità minima o un tasso di click-through) per l’esecuzione delle offerte. Puoi utilizzare i filtri pre-bid come tattiche di ottimizzazione, ma comprendere che ogni regola può limitare le opportunità su cui questo posizionamento può offrire. Per aggiungere o modificare filtri:

1. Fai clic su ![Modifica](/help/dsp/assets/edit.png).
1. Effettua una delle seguenti operazioni:
   * Per aggiungere un filtro:
      1. Clic **[!UICONTROL Add Filter]**.
      1. Accanto a **[!UICONTROL Only bid if]**, seleziona una metrica, quindi immetti un valore.
   * Per rimuovere un filtro, fai clic su **[!UICONTROL X]** nella riga filtro.
1. Clic **[!UICONTROL Save]**.

Consulta le descrizioni di ciascun filtro pre-bid in &quot;[Filtri di pre-offerta a livello di posizionamento e modalità di utilizzo](/help/dsp/optimization/optimization-pre-bid-filters.md).&quot;

### Tutti gli altri posizionamenti

**[!UICONTROL Budget Goal]:** Il massimale lordo di bilancio e l&#39;intervallo di bilancio (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

**[!UICONTROL Gross Budget Goal]:** (Posizionamenti solo nelle campagne con gestione dei margini) Il tetto di budget lordo e l&#39;intervallo di budget (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

**[!UICONTROL Optimization Goal]:**  L&#39;obiettivo di ottimizzazione per il pacchetto. Vedi le descrizioni di ogni obiettivo di ottimizzazione in &quot;[Obiettivi di ottimizzazione e come utilizzarli](/help/dsp/optimization/optimization-goals.md)&quot;.

**[!UICONTROL Target Goal]:** L&#39;obiettivo di destinazione, che viene utilizzato per monitorare le prestazioni.

>[!NOTE]
>
>Questo campo è solo un punto di riferimento e non viene utilizzato per le decisioni.

**[!UICONTROL Pace on]:** Su quale percorso si baserà:

* **[!UICONTROL Budget goal]:** (Impostazione predefinita) Questa opzione consente di ottenere il maggior numero possibile di impression nel budget allocato.

* **[!UICONTROL Impressions]:** Questa opzione consente di distribuire le impression finché non viene raggiunta una quantità specifica entro un intervallo specificato. Quando selezioni questa opzione, specifica il numero di impression e l’intervallo: *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* o *[!UICONTROL Weekly]*.

**[!UICONTROL Max Bid]:** Massimo per 1000 impression.

**[!UICONTROL Flight pacing]:** (Posizionamenti con solo velocità a livello di posizionamento) Come impostare la consegna degli annunci:

* *[!UICONTROL Even]:* (L&#39;impostazione predefinita) Posiziona la consegna uniformemente in ciascun volo, con un obiettivo del 50% della consegna nella prima metà del volo.

* *[!UICONTROL Slightly Ahead]:* (L’impostazione predefinita) Accelera la consegna in modo che sia completa a metà strada nel periodo di volo dal 55 al 65%.

* *[!UICONTROL Frontload]:* Accelera la consegna in modo che sia completa a metà del volo dal 65 al 75%.

* *[!UICONTROL Aggressive Frontload]:* Accelera la consegna in modo che sia completa a metà del volo il 75-85%.

**[!UICONTROL Intraday pacing]:** (Posizionamenti con solo velocità a livello di posizionamento) Come effettuare la consegna degli annunci in ogni giorno all’interno del volo:

* *[!UICONTROL Even]:* (L’impostazione predefinita) Consente di ridimensionare la consegna in base alla disponibilità dell’inventario. Generalmente, vengono consegnati più annunci all&#39;ora diurna, quando il volume dell&#39;asta è più alto e vengono consegnati meno annunci la mattina e la sera.

* *[!UICONTROL ASAP]:* (Il valore predefinito) Accelera la consegna a una velocità doppia rispetto alla *Pari*.

   >[!CAUTION]
   >
   >Questa opzione può influire negativamente sulle prestazioni. Utilizzalo solo quando stai dando priorità assoluta alla consegna e spendi più dell’ottimizzazione delle prestazioni.

**[!UICONTROL Placement Pre-bid Filters]:** (Facoltativo) È necessario soddisfare fino a cinque filtri per le offerte. Puoi utilizzare i filtri pre-bid come tattiche di ottimizzazione, ma ricorda che ogni regola può limitare le opportunità per cui questo posizionamento può offrire. Per aggiungere o modificare filtri:

1. Fai clic su ![Modifica](/help/dsp/assets/edit.png).
1. Effettua una delle seguenti operazioni:
   * Per aggiungere un filtro:
      1. Clic **[!UICONTROL Add Filter]**.
      1. Accanto a **[!UICONTROL Only bid if]**, seleziona una metrica, quindi immetti un valore.
   * Per rimuovere un filtro, fai clic su **[!UICONTROL X]** nella riga filtro.
1. Clic **[!UICONTROL Save]**.

## [!UICONTROL Geo-Targeting]

**[!UICONTROL Audience Location]:** (Facoltativo) Posizioni specifiche in cui includere o escludere gli annunci nel posizionamento. Se non specifichi alcuna posizione, tutte le posizioni sono oggetto di targeting.

>[!NOTE]
>
>Le posizioni Città e DMA non sono disponibili per i posizionamenti Roku.

Per specificare le posizioni:

1. Fai clic su ![Modifica](/help/dsp/assets/edit.png).
1. Effettua una delle seguenti operazioni:
   * Per includere o escludere un Paese, Stato, Città, DMA, Distretto Legislativo Federale o Distretto Legislativo Statale:
      1. Seleziona il tipo di posizione nella colonna a sinistra.
      1. Se necessario, fai clic su una posizione per espanderla.
      1. Accanto alla posizione, fai clic su *[!UICONTROL Include]* per includerlo come target o *[!UICONTROL Exclude]* per escluderlo come target.
   * Per cercare un codice postale e includere o escludere tutti i risultati selezionati:
      1. Clic **[!UICONTROL Search Postal Code]**.
      1. Selezionare il paese.
      1. Immettere il nome della città, quindi fare clic su ![Modifica](/help/dsp/assets/search.png).
      1. Fai clic sul risultato di ricerca corretto.
      1. Fai clic su *[!UICONTROL Include All]* per includere tutte le posizioni come destinazioni o *[!UICONTROL Exclude All]* per escludere tutte le posizioni come destinazioni.
   * Per inserire o incollare i codici postali e includerli o escluderli tutti:
      1. Clic **[!UICONTROL Paste Postal Code]**.
      1. Selezionare il paese.
      1. Immettere o incollare fino a 1000 codici postali.
Includi un codice postale per riga o inserisci più valori separati da virgole o tabulazioni.
      1. Fai clic su *[!UICONTROL Include All]* per includere tutte le posizioni come destinazioni o *[!UICONTROL Exclude All]* per escludere tutte le posizioni come destinazioni.
   * Per rimuovere una posizione dalla [!UICONTROL Included] o [!UICONTROL Excluded] elenco, fai clic su **[!UICONTROL X]** accanto alla posizione nella colonna a destra.
1. Clic **[!UICONTROL Done]**.

>[!NOTE]
>
>* Non tutti i paesi dispongono di posizioni relative a Stato, Città o Codice postale.
>* DMA (area di mercato designata), i distretti legislativi federali e i distretti legislativi statali sono disponibili solo per le posizioni statunitensi.


## [!UICONTROL Inventory Targeting]

**[!UICONTROL Inventory Sources]:** Origini di magazzino da includere o escludere come target. Per la maggior parte dei tipi di posizionamento, tutti i tipi di inventario e tutte le origini per ciascun tipo sono inclusi per impostazione predefinita. Per [!DNL Roku] posizionamenti, è necessario specificare il tipo di inventario e le origini. È possibile scegliere tra i seguenti tipi di inventario:

* [!UICONTROL Public]: (Tutti i tipi di posizionamento ad eccezione di Roku) Tutto l&#39;inventario di scambio aperto a cui DSP ha accesso. È possibile includere ed escludere l’inventario pubblico.

   È possibile visualizzare l’elenco in base all’origine o al feed. Quando visualizzate l’elenco per feed, potete eseguire ricerche per nome feed, chiave di feed o tag caratteristici selezionati.

* [!UICONTROL Private] | [!UICONTROL Roku Private]: Offerte private esistenti (o private esistenti) [!DNL Roku] offerte [!DNL Roku] posizionamenti) con editori configurati in DSP. È possibile includere, ma non escludere, l’inventario pubblico.

   Puoi cercare l’elenco per parola chiave, chiave, ID offerta o tag personalizzati.

* [!UICONTROL On Demand] | [!UICONTROL Roku On Demand]: Tutto [premio, non garantito [!UICONTROL On Demand] inventario](/help/dsp/inventory/on-demand-inventory-about.md) o [!UICONTROL On Demand] [!DNL Roku] offerte [!DNL Roku] posizionamenti) a cui ti sei iscritto [!DNL DSP]. Puoi includere ed escludere [!UICONTROL On Demand] inventario.

   È possibile visualizzare l’elenco in base all’origine o al feed. Quando visualizzi l’elenco per feed, puoi eseguire ricerche per nome feed, chiave di feed o per un’area di pubblicazione, un tag categoria o un tag caratteristico selezionati.

Per specificare il targeting di inventario:

* Per escludere un tipo di inventario, deselezionare la casella di controllo accanto al nome.
* Per eseguire il targeting di un tipo di inventario:
   1. Selezionare la casella di controllo accanto al nome del tipo di inventario.
   1. (Facoltativo) Modifica le origini in modo da includere:
      1. Fai clic su ![Modifica](/help/dsp/assets/edit.png).
      1. ([!UICONTROL Public] e [!UICONTROL On Demand] inventario) Fai clic su **[!UICONTROL View by Source]** o **[!UICONTROL View by Feed]** per modificare l&#39;elenco delle origini.
      1. (Se applicabile) Filtrare l’inventario in base alle esigenze.
      1. Specifica le origini da includere ed escludere:
         * Per includere un [!UICONTROL Public] o [!UICONTROL On Demand] sorgente, fai clic su **[!UICONTROL Include]** accanto al nome di origine.
         * Per includere [!UICONTROL Private] fonti:
            * Per includere tutto l&#39;inventario in un&#39;offerta, fai clic su **[!UICONTROL Include all]** accanto al nome dell&#39;offerta.
            * Per includere una singola origine di magazzino, espandere il nome dell&#39;offerta e quindi fare clic sulla casella di controllo accanto al nome dell&#39;origine.
         * Per escludere un [!UICONTROL Public] o [!UICONTROL On source], fai clic su **[!UICONTROL Exclude]** accanto al nome di origine.
   1. (Facoltativo) Per scaricare un file CSV con le informazioni di targeting nella posizione Download del browser, fai clic su **[!UICONTROL Save & Export]**.
   1. Clic **[!UICONTROL Save]**.

>[!TIP]
>
>Se hai effettuato la sottoscrizione a [!UICONTROL On Demand] inventory ma non è possibile individuare gli editori o le offerte per il targeting, quindi controllare lo stato delle offerte. Per ulteriori informazioni sugli stati, consulta [Informazioni [!DNL On Demand] Inventario Premium](/help/dsp/inventory/on-demand-inventory-about.md).

**[!UICONTROL Exclude out-stream]:** (Solo per i posizionamenti video) Esclude il traffico outstream.

Gli annunci in uscita vengono solitamente visualizzati sopra il contenuto come pop-up o riempiti di contenuto (nell’esperienza nativa), anziché come annunci video normali in un lettore video.

## [!UICONTROL Site Targeting]

**[!UICONTROL Traffic type]:** Tipi di traffico da eseguire. Le opzioni includono **[!UICONTROL Websites]** e **[!UICONTROL Apps]**.

**[!UICONTROL Site tier]:** (Disponibile quando **[!UICONTROL Paste list of targeted sites]** è *[!UICONTROL Off]*) La qualità dei siti di destinazione. I livelli 1-3 sono tutti sicuri per il marchio e sono stati valutati e approvati dal team di mappatura DSP.

* *[!UICONTROL Tier 1]:* Siti e applicazioni Premium riconoscibili a livello nazionale.
* *[!UICONTROL Tier 2]:* Target di livello 1, nonché siti e applicazioni di qualità meno noti rispetto al livello 1.
* *[!UICONTROL Tier 3]:* Esegue il targeting dei livelli 1-2, nonché dei siti e delle applicazioni legittimi e sicuri per il marchio che soddisfano un pubblico di nicchia. Utilizza il livello 3 per gli acquisti di tipo reach o data targeting.
* *[!UICONTROL All Sites]:* Esegue il targeting dei livelli da 1 a 3 e del nuovo inventario che non è stato controllato o categorizzato, che puoi utilizzare per raggiungere.

>[!NOTE]
>
>L’inventario è specifico per le unità pubblicitarie nel posizionamento.

>[!TIP]
>
>Per le campagne sulle prestazioni, è consigliabile selezionare *[!UICONTROL All Sites]*.

**[!UICONTROL Site Categories]:** (Facoltativo; disponibile quando **[!UICONTROL Paste list of targeted sites]** è *[!UICONTROL Off]*) Categorie di siti all’interno dei livelli di sito selezionati per includere o escludere (ma non entrambi) come destinazioni. Scegli tra gli elenchi di siti verticali mappati DSP in base all&#39;oggetto del sito:

1. Fai clic su ![Modifica](/help/dsp/assets/edit.png).
1. Specifica le categorie del sito da includere o escludere:
   * Per includere le categorie del sito:
      1. Clic **[!UICONTROL Include categories]**.
      1. Seleziona la casella di controllo accanto a ogni categoria di destinazione.
   * Per escludere le categorie di siti:
      1. Clic **[!UICONTROL Exclude categories]**.
      1. Seleziona la casella di controllo accanto a ogni categoria da escludere.
1. (Facoltativo) Per scaricare un file CSV con le informazioni di targeting nella posizione Download del browser, fai clic su **[!UICONTROL Export]**.
1. Clic **[!UICONTROL Save]**.

**[!UICONTROL Exclude Sites]:** (Facoltativo; disponibile quando **[!UICONTROL Paste list of targeted sites]** è *[!UICONTROL Off]*) Siti da escludere. È possibile cercare e selezionare siti oppure immettere o incollare nomi di dominio:

1. Fai clic su ![Modifica](/help/dsp/assets/edit.png).
1. Specifica i siti:
   * Per cercare un sito:
      1. Clic **[!UICONTROL Search]**.
      1. Immettere una parola chiave, selezionare un livello del sito e/o selezionare una categoria del sito.
      1. Nei risultati della ricerca, seleziona i siti da escludere:
         * Per escludere un singolo sito, seleziona la casella di controllo accanto a esso.
         * (Quando sono disponibili più di 50 risultati) Per escludere i primi 50 risultati, fai clic su **[!UICONTROL Exclude these 50]**. Per escludere tutti i risultati della ricerca, fai clic su **[!UICONTROL Exclude these \<*NN *\>]**.
   * Per immettere i nomi di dominio:
      1. Clic **[!UICONTROL Paste]**.
      1. Immettere uno o più nomi di dominio su righe separate.
      1. Clic **[!UICONTROL Exclude All]**.
1. Fai clic su **[!UICONTROL Done]** quando hai finito.

>[!NOTE]
>
>* Vengono applicati anche elenchi di siti bloccati a livello di account e inserzionista, oltre al DSP [elenco siti bloccati a livello globale](/help/dsp/introduction/features/brand-safety-media-quality.md), che include i siti considerati non sicuri per gli annunci.
>* Gli elenchi di siti bloccati sovrascrivono sempre gli elenchi di siti di destinazione. Se un posizionamento esclude e include lo stesso target per un annuncio, il target viene escluso.


**[!UICONTROL Language]:** (Facoltativo) Una singola lingua di destinazione.

**[!UICONTROL Site List Preview]:** (Sola lettura) Tutti i siti di destinazione e bloccati per il posizionamento.

Facoltativamente, puoi esportare l’elenco dei siti di destinazione e bloccati come file con valori delimitati da virgole. Per esportare l’elenco, fai clic su **[!UICONTROL Export full site list]**, quindi apri o salva il file in base alla normale procedura del browser.

**[!UICONTROL Allow unscreened sites]:** (Solo posizionamenti di visualizzazione standard) Abilita la consegna di annunci su siti non controllati. Quando il posizionamento esegue il targeting dell’inventario privato, questa opzione può distribuire annunci sui siti bloccati.

**[!UICONTROL Paste list of targeted sites]:** Consente di eseguire il targeting solo per siti specifici. Quando abiliti questa opzione, le altre opzioni di targeting del sito sono disabilitate.

**[!UICONTROL Sites]:** (Disponibile quando **[!UICONTROL Paste list of targeted sites]** è *[!UICONTROL On]*) Siti di destinazione. È possibile cercare e selezionare siti oppure immettere o incollare nomi di dominio:

1. Fai clic su ![Modifica](/help/dsp/assets/edit.png).
1. Specifica i siti:
   * Per cercare un sito:
      1. Clic **[!UICONTROL Search]**.
      1. Immettere una parola chiave, selezionare un livello del sito e/o selezionare una categoria del sito.
      1. Nei risultati della ricerca, seleziona i siti da includere:
         * Per escludere un singolo sito, seleziona la casella di controllo accanto a esso.
         * (Quando sono disponibili più di 50 risultati) Per includere i primi 50 risultati, fai clic su **[!UICONTROL Include these 50]**. Per includere tutti i risultati della ricerca, fai clic su **[!UICONTROL Include these \<*NN *\>]**.
   * Per immettere i nomi di dominio:
      1. click **[!UICONTROL Paste]**.
      1. Immettere uno o più nomi di dominio su righe separate.
      1. Clic **[!UICONTROL Include All]**.
1. Clic **[!UICONTROL Done]**.

## [!UICONTROL Audience Targeting]

**[!UICONTROL Included Audiences]:** Qualsiasi target di pubblico per il posizionamento, tra cui [segmenti di terze parti, segmenti di prime parti, segmenti di Adobe, segmenti personalizzati e tipi di pubblico salvati](/help/dsp/audiences/audience-settings.md). Viene inoltre visualizzata la dimensione totale e attiva del pubblico deduplicato per tutti i segmenti selezionati e i tipi di pubblico salvati. Puoi selezionare un pubblico esistente, crearne uno nuovo da riutilizzare in un secondo momento o selezionare segmenti di pubblico specifici:

* Per selezionare un pubblico esistente, fai clic su ![Seleziona](/help/dsp/assets/chevron-down.png) accanto a [!UICONTROL Included Audiences], quindi seleziona il pubblico.
* Per creare un nuovo pubblico, fai clic su ![Seleziona](/help/dsp/assets/chevron-down.png) accanto a [!UICONTROL Included Audiences], quindi seleziona **[!UICONTROL + Create Audience]**. Per istruzioni, consulta [Creare un pubblico riutilizzabile](/help/dsp/audiences/reusable-audience-create.md), a partire dal passaggio 3.
* Per selezionare segmenti di pubblico specifici, fai clic su **[!UICONTROL Select segments for this placement only]**. Seleziona la logica del segmento; per istruzioni, vedi il passaggio 6 in &quot;[Creare un pubblico riutilizzabile](/help/dsp/audiences/reusable-audience-create.md).&quot; Al termine, fai clic su **Salva**.

**[!UICONTROL Excluded Audiences]:** Qualsiasi pubblico da escludere per il posizionamento, compresi i tipi di pubblico con [segmenti di terze parti, segmenti di prime parti, segmenti di Adobe, segmenti personalizzati e tipi di pubblico salvati](/help/dsp/audiences/audience-settings.md). Viene inoltre visualizzata la dimensione totale e attiva del pubblico deduplicato per tutti i tipi di pubblico esclusi. Puoi selezionare un pubblico esistente o crearne uno nuovo da riutilizzare in un secondo momento:

* Per selezionare un pubblico esistente, fai clic su ![Seleziona](/help/dsp/assets/chevron-down.png) accanto a [!UICONTROL Excluded Audiences], quindi seleziona il pubblico.
* Per creare un nuovo pubblico, fai clic su ![Seleziona](/help/dsp/assets/chevron-down.png) accanto a [!UICONTROL Excluded Audiences], quindi seleziona **+ Crea pubblico**. Per istruzioni, consulta [Creare un pubblico riutilizzabile](/help/dsp/audiences/reusable-audience-create.md), a partire dal passaggio 3.

**[!UICONTROL Cross Device Targeting]:** (Disponibile quando selezioni almeno un segmento o un pubblico e [campaign è configurato per il targeting cross-device basato su persone](/help/dsp/campaign-management/campaigns/campaign-settings.md). Consente di estendere il targeting su tutti i dispositivi noti di una persona (in base al grafico dei dispositivi specificato nelle impostazioni della campagna), anche sui dispositivi che non si trovano nei segmenti specificati. Le tariffe possono essere applicate a seconda del grafico specificato per la campagna. I dati del grafico dei dispositivi sono attualmente disponibili solo in Nord America.

**[!UICONTROL Placement Cap]:** (Facoltativo) Il numero di volte in cui una persona o un dispositivo univoco (a seconda del valore specificato) [!UICONTROL Cross Device Level] per la campagna) verranno serviti gli annunci dal posizionamento. Le opzioni includono *[!UICONTROL Unlimited]* o un importo specifico per giorno, settimana o mese.

>[!NOTE]
>
> Puoi impostare i limiti di frequenza a livello di campagna, pacchetto e posizionamento. DSP rispettare il limite di frequenza più rigoroso nella gerarchia delle campagne.

**[!UICONTROL Secondary Cap]:** (Facoltativo; disponibile quando si include un valore numerico [!UICONTROL Placement Cap]) Limitazione aggiuntiva entro i limiti del tappo di posizionamento principale. Seleziona il numero di impression e il periodo di tempo (ad esempio 3 per 12 ore).

**[!UICONTROL Day Parting]:** (Facoltativo) Giorni specifici della settimana e dell’ora del giorno in cui gli annunci possono essere eseguiti. Per specificare gli intervalli di ripartizione giornaliera:

1. Fai clic su ![Modifica](/help/dsp/assets/edit.png).
1. Selezionare il fuso orario applicabile.
1. Specifica gli intervalli:
   * Per selezionare un intervallo preimpostato, fare clic su uno dei pulsanti di intervallo. Le opzioni includono *[!UICONTROL Weekends]**, *[!UICONTROL Weekdays]*, *[!UICONTROL Morning]*, *[!UICONTROL Lunch]*, *[!UICONTROL Dinner]* oppure *[!UICONTROL Prime]* (primetime).
   * Per selezionare manualmente un intervallo, fare clic all’interno di una cella e, facoltativamente, trascinare per selezionare l’intervallo.
1. Clic **[!UICONTROL Save]**.

**[!UICONTROL Topic Targeting]:** (Facoltativo; disponibili per gli inserzionisti configurati con [!DNL Comscore] e [!DNL Grapeshot] segmenti) Nomi di segmento o ID specifici da [!DNL Comscore] e [!DNL Grapeshot] da includere come target. Per questa funzione possono essere applicati costi aggiuntivi. Per attivare questa funzione e impostare i segmenti degli argomenti, contatta il tuo [!DNL Adobe] team di account.

Per specificare il targeting per gli argomenti:

1. Fai clic su ![Modifica](/help/dsp/assets/edit.png).
1. Specifica i segmenti di destinazione:
   1. Nella colonna a sinistra, seleziona il partner (*[!UICONTROL Comscore]* o *[!UICONTROL Grapeshot]*).
   1. Nel campo di input, immetti i nomi dei segmenti o gli ID dei segmenti.
1. (Facoltativo) Per scaricare un file CSV con le informazioni sull&#39;argomento nella posizione Download del browser, fai clic su **[!UICONTROL Export]**.
1. Clic **[!UICONTROL Save]**.

>[!TIP]
>
>* Il targeting dell’argomento limita l’inventario su cui il posizionamento può fare offerte, quindi utilizza il targeting dell’argomento solo per una piccola percentuale dell’acquisto complessivo.
>
>* Imposta qualsiasi targeting negativo all’interno del segmento su [!DNL Comscore] o [!DNL Grapeshot].


**[!UICONTROL Device Targeting]:** (Facoltativo) Informazioni specifiche sui dispositivi, inclusi tipi di dispositivi, produttori, sistemi operativi, browser e tipi di connettività, da includere ed escludere come target. Per specificare il targeting del dispositivo:

1. Fai clic su ![Modifica](/help/dsp/assets/edit.png).
1. Specifica i dettagli del dispositivo da includere ed escludere:
   1. Nella colonna a sinistra, seleziona la categoria .
   1. Specifica il targeting:
      * Per includere un valore, fai clic su **[!UICONTROL Include]** accanto al nome del valore.
      * Per escludere un valore, fai clic su **[!UICONTROL Exclude]** accanto al nome del valore.
1. (Facoltativo) Per scaricare un file CSV con le informazioni di targeting del dispositivo nella posizione Download del browser, fai clic su **[!UICONTROL Export]**.
1. Clic **[!UICONTROL Save]**.

**[!UICONTROL ISP Targeting]:** (Facoltativo) Specifici provider di servizi Internet (ISP) per includere o escludere (ma non entrambi) come target. Per specificare il targeting dell&#39;ISP:

1. Fai clic su ![Modifica](/help/dsp/assets/edit.png).
1. Specifica gli ISP da includere o escludere:
   * Per includere gli ISP:
      1. Clic **[!UICONTROL Include ISPs]**.
      1. (Facoltativo) Filtrare l’elenco per parola chiave.
      1. Seleziona la casella di controllo accanto a ogni ISP da indirizzare.
   * Per escludere gli ISP:
      1. Clic **[!UICONTROL Exclude ISPs]**.
      1. (Facoltativo) Filtrare l’elenco per parola chiave.
      1. Seleziona la casella di controllo accanto a ogni ISP da escludere.
1. (Facoltativo) Per scaricare un file CSV con le informazioni di targeting dell&#39;ISP nella posizione Download del browser, fai clic su **[!UICONTROL Export]**.
1. Clic **[!UICONTROL Save]**.

## [!UICONTROL Brand Safety and Media Targeting]

**[!UICONTROL Contextual filtering]:** Tipi di [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science]e [!DNL Peer39] filtri contestuali da applicare. Le impostazioni predefinite a livello dell’inserzionista vengono selezionate per i nuovi posizionamenti, ma è possibile modificare le impostazioni:

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block sites that are]:** (Facoltativo) Per impostazione predefinita, uno o più tipi di contesto di inventario da bloccare. Possono essere applicati costi aggiuntivi.

* [!UICONTROL Peer 39]:

   * **Siti di destinazione:** (Facoltativo) Per impostazione predefinita, è necessario eseguire il targeting di uno o più tipi di attributi di inventario. Possono essere applicati costi aggiuntivi.

* [!UICONTROL ComScore]:

   * **Blocca siti che sono:** (Facoltativo) Per impostazione predefinita, uno o più tipi di attributi di inventario da bloccare. Possono essere applicati costi aggiuntivi.

* [!UICONTROL Integral Ad Science]

   * **[!UICONTROL Adult Content]:** (Facoltativo) Il grado di contenuto per adulti per cui bloccare gli annunci per impostazione predefinita: *[!UICONTROL Do Not Block]* (impostazione predefinita), *[!UICONTROL Standard]* oppure *[!UICONTROL Strict]*. Possono essere applicati costi aggiuntivi.

   * **[!UICONTROL Alcohol Content]:** (Facoltativo) Il grado di contenuto alcolico per il quale bloccare gli annunci per impostazione predefinita: *[!UICONTROL Do Not Block]* (impostazione predefinita), *[!UICONTROL Standard]* oppure *[!UICONTROL Strict]*. Possono essere applicati costi aggiuntivi.

**[!UICONTROL Pre-bid fraud blocking]:** Tipi di siti da bloccare in base al traffico fraudolento e alle attività sospette misurate attraverso [!DNL DoubleVerify], [!DNL Integral Ad Science]e [!DNL Peer39]. Le impostazioni predefinite a livello dell’inserzionista vengono selezionate per i nuovi posizionamenti, ma è possibile modificare le impostazioni:

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** Per impostazione predefinita, blocca tutto il traffico non valido al 100%, incluso il traffico su dispositivi con collegamenti elevati, per i nuovi posizionamenti. Possono essere applicati costi aggiuntivi.

   * **[!UICONTROL Also block sites with]:** (Facoltativo) Un ulteriore livello di frode e traffico non valido che causerà il blocco degli annunci da parte di DSP per impostazione predefinita:  *[!UICONTROL None]* (l’impostazione predefinita, che non blocca il traffico aggiuntivo), *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*, *[!UICONTROL >4% Average Fraud/IVT levels]*, *[!UICONTROL >6% Average Fraud/IVT levels]*, *[!UICONTROL >10% Average Fraud/IVT levels]* oppure *[!UICONTROL >25% Average Fraud/IVT levels]*. Possono essere applicati costi aggiuntivi.

* [!UICONTROL Peer 39]:

   * **[!UICONTROL Block sites that are]:** (Facoltativo) Per impostazione predefinita, uno o più tipi di frode che DSP bloccare gli annunci: *[!UICONTROL Fraud]* (che blocca tutti i siti con frode), *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]* e/o *[!UICONTROL Fraud: Zero Ads]*. Possono essere applicati costi aggiuntivi.

* [!UICONTROL Integral Ad Science]:

   * **[!UICONTROL Block sites that are]:** (Facoltativo) Un tipo di attività sospetta sul sito web o sull&#39;app che DSP bloccare gli annunci per impostazione predefinita: *[!UICONTROL None]* (l’impostazione predefinita, che non blocca gli annunci in base a attività sospette), *[!UICONTROL Suspicious Activity - High Risk]* oppure *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. Possono essere applicati costi aggiuntivi.

**[!UICONTROL Ads.txt filtering]:**

Quale livello di [Ads.txt](https://iabtechlab.com/ads-txt-about/) filtro pre-bid da utilizzare sfruttando l’elenco dei rivenditori digitali autorizzati di ciascun editore. L’impostazione predefinita a livello di inserzionista è selezionata per i nuovi posizionamenti, ma puoi modificare le impostazioni:

* *[!UICONTROL Opt out of ads.txt (default)]*: Comprare l&#39;inventario da tutti i venditori.
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*: Per assegnare priorità all’acquisto di inventario da venditori e rivenditori diretti autorizzati di un dominio.
* *[!UICONTROL Ads.txt sellers only]*: Acquistare scorte solo da venditori e rivenditori diretti autorizzati di un dominio.
* *[!UICONTROL Ads.txt sellers only]*: Acquistare scorte solo da venditori diretti autorizzati di un dominio.

**[!UICONTROL DoubleVerify Authentic Brand Safety]:** (Gli inserzionisti configurati con [!UICONTROL DoubleVerify Authentic Brand Safety] Abilita [!DNL DoubleVerify Authentic Brand Safety], che blocca le impression dopo l’offerta utilizzando le regole di sicurezza del marchio personalizzate configurate per l’ID segmento specificato. DSP addebita al tuo account l’utilizzo dell’ID segmento specificato nelle impostazioni dell’inserzionista.

## [!UICONTROL Tracking] {#placement-tracking}

>[!NOTE]
>
>([!DNL Roku] posizionamenti) fornitori di tracciamento di terze parti approvati da [!DNL Roku] include [!DNL Acxiom], [!DNL comScore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk]e [!DNL Research Now].

**[!UICONTROL Event Pixels]:** (Facoltativo) Pixel di tracciamento eventi di terze parti che saranno allegati per impostazione predefinita a tutti i nuovi annunci nel posizionamento. Per specificare i pixel dell’evento:

1. Fai clic su ![Modifica](/help/dsp/assets/edit.png).
1. Effettua una delle seguenti operazioni:
   * Per selezionare un pixel esistente, seleziona la casella di controllo nella riga pixel.
   * Per creare un nuovo pixel:
      1. Clic **[!UICONTROL Create]**.
      1. Immetti le seguenti informazioni:
         * **[!UICONTROL Pixel name]:** Nome del pixel; la lunghezza massima è di 500 caratteri. Utilizza un nome che ti aiuti a identificare facilmente il pixel.
         * **[!UICONTROL Pixel event fires on]:** L&#39;evento che attiva il pixel da attivare. Gli eventi disponibili variano in base al tipo di annuncio.
         * **[!UICONTROL Pixel type]:** Se il pixel è un *[!UICONTROL IMG URL]* (file immagine da 1 pixel), *[!UICONTROL HTML]* oppure *[!UICONTROL JavaScript URL]*.
         * **[!UICONTROL Pixel URL]:** URL dell&#39;immagine pixel.
      1. Clic **[!UICONTROL Create and attach]**.
   1. Clic **[!UICONTROL Save]**.

**[!UICONTROL Conversion Pixels]:** (Facoltativo) Pixel di tracciamento della conversione che saranno collegati per impostazione predefinita a tutti i nuovi annunci nel posizionamento. Per specificare i pixel di conversione:

1. Fai clic su ![Modifica](/help/dsp/assets/edit.png).
1. Effettua una delle seguenti operazioni:
   * Per selezionare un pixel esistente, seleziona la casella di controllo nella riga pixel.
   * Per creare un nuovo pixel:
      1. Clic **[!UICONTROL Create]**.
      1. Immetti le seguenti informazioni:
         * **[!UICONTROL Conversion pixel name]:** Nome del pixel; la lunghezza massima è di 500 caratteri. Utilizza un nome che ti aiuti a identificare facilmente il pixel.
         * **[!UICONTROL Conversion category]:** Il tipo di conversione.
         * **[!UICONTROL Impression conversion window]:** Il numero di giorni dopo che si verifica un’impression pubblicitaria in cui l’impression può essere attribuita a una conversione. Il valore predefinito è 30 giorni.
         * **[!UICONTROL Click conversion window]:** Il numero di giorni successivi all’esecuzione di un clic annuncio in cui il clic può essere attribuito a una conversione. Il valore predefinito è 30 giorni.
         * **[!UICONTROL Notes]:** (Facoltativo) Una descrizione o altre informazioni sul pixel.
      1. Clic **[!UICONTROL Create and attach]**.
      1. Implementa il pixel di conversione sulle pagine web rilevanti:
         1. Nel menu principale, vai a **[!UICONTROL Resources]>[!UICONTROL Conversion pixels]**.
         1. Nella riga pixel, fai clic su **[!UICONTROL edit]**.
         1. Copia i valori nella [!UICONTROL HTML Tag] e [!UICONTROL Flash Tag] campi, se necessario, per fornire all&#39;inserzionista o al contatto del sito web.

            Il reparto IT dell&#39;inserzionista o un altro gruppo potrebbe dover pianificare o essere informato sulla distribuzione dei tag.
   1. Clic **[!UICONTROL Save]**.

**[!UICONTROL 3rd-party Fees]:** (Facoltativo) Un tasso di commissione statico di terze parti da tracciare come costo non fatturabile per 1000 impression. L’impostazione predefinita a livello di pacchetto viene applicata automaticamente per i nuovi posizionamenti, se applicabile, a meno che non si immetta un valore diverso.

>[!NOTE]
>
>Le commissioni fatturabili sono riportate nel [!UICONTROL Net CPM] metrica.

>[!MORELIKETHIS]
>
>* [Informazioni sulla gestione del posizionamento](placement-about.md)
>* [Creare un posizionamento](placement-create.md)
>* [Modificare un posizionamento](placement-edit.md)
>* [Visualizza il registro delle modifiche per un posizionamento](placement-change-log.md)
>* [Scelte rapide da tastiera](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [Domande frequenti su Campaign Management](/help/dsp/campaign-management/campaign-management-faq.md)

