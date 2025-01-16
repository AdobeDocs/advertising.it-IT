---
title: Impostazioni di posizionamento
description: Consulta le descrizioni delle impostazioni di posizionamento disponibili.
feature: DSP Placements
exl-id: 5b2574be-5d08-4cf7-910e-deac48d7e035
source-git-commit: 17d2f802e77709636ef9654ad154e14c5d53c477
workflow-type: tm+mt
source-wordcount: '3966'
ht-degree: 0%

---

# Impostazioni di posizionamento

## [!UICONTROL Basics]

**[!UICONTROL Placement name]** Il nome del posizionamento.

>[!TIP]
>Utilizza una convenzione di denominazione appropriata per la tua situazione. Una convenzione di denominazione suggerita è &quot;*\&lt;Nome campagna\>: \&lt;Unità annuncio\>: \&lt;Durata\>: \&lt;Targeting\>*.&quot;

**[!UICONTROL Status]:** Lo stato del posizionamento: *[!UICONTROL Active]* (impostazione predefinita) o *[!UICONTROL Paused]*.

>[!TIP]
>La best practice prevede di mettere in pausa il posizionamento fino a quando non sei pronto per avviarlo.

**[!UICONTROL Details]:** (sola lettura) Il tipo di annuncio applicabile, l&#39;account che sta creando o creando il posizionamento e la campagna principale. Per visualizzare ulteriori dettagli, fare clic su **[!UICONTROL Show more]**.

**[!UICONTROL Templates]:** Apre un elenco di modelli di posizionamento esistenti. Per popolare automaticamente le impostazioni di targeting da un modello:

1. Effettuare una delle seguenti operazioni:

   * Per riutilizzare tutti gli oggetti di un modello, selezionare la casella di controllo accanto al nome del modello.

   * Per riutilizzare singoli tipi di oggetto da un modello, espandere il nome del modello e selezionare la casella di controllo accanto ai tipi di oggetto che si desidera riutilizzare.

1. Fare clic su **[!UICONTROL Apply]**.

**[!UICONTROL Ad specs for forecast]:** (solo formati di annunci video) La durata e/o le specifiche dell&#39;annuncio, utilizzate per calcolare la proiezione di previsione a destra. I campi variano in base al tipo di annuncio.

**[!UICONTROL Environment]:** (solo formato annuncio video universale) Gli ambienti del dispositivo (desktop, mobile, TV connessa) da includere come destinazioni nel posizionamento. Specificane almeno uno.

Nei rapporti personalizzati, la dimensione a livello di posizionamento &quot;Ambiente dispositivo&quot; indica l’ambiente di destinazione.

**[!UICONTROL Placement tags]:** (facoltativo) Parole chiave o nomi alternativi per individuare questo posizionamento.

## Obiettivi

**[!UICONTROL Package]:** (facoltativo) pacchetto a cui è assegnato il posizionamento. Fai clic su ![Modifica](/help/dsp/assets/edit.png) per selezionare un pacchetto esistente o crearne uno. Quando si assegna il posizionamento a un pacchetto, la sezione [!UICONTROL Goals] viene aggiornata con le date di volo, l&#39;obiettivo di consegna e il budget del pacchetto.

**[!UICONTROL Flight Dates]:** La data di inizio e la data di fine del posizionamento. Gli annunci approvati possono essere eseguiti durante il volo quando il posizionamento è attivo e assegnato a un pacchetto o a una campagna attiva.

Le date del pacchetto (se applicabile) o della campagna vengono compilate automaticamente per impostazione predefinita.

>[!NOTE]
>
>* Le date di volo devono essere incluse nelle date di volo della campagna e nelle date di volo del pacchetto.

### Posizionamenti assegnati a pacchetti con velocità a livello di pacchetto

**[!UICONTROL Placement Funding]:** Come preventivare il posizionamento:

* *[!UICONTROL Optimize based on performance]:* Controlla il budget a livello di pacchetto.
* *[!UICONTROL Set a Fixed Minimum or Maximum Budget]:* Consente di impostare un budget di posizionamento minimo e/o massimo. Specificare almeno un tipo di budget:

   * *[!UICONTROL Maximum Budget]*: immettere un valore e la durata (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

   * *[!UICONTROL Minimum Budget]*: il budget minimo come percentuale del budget del pacchetto. Quando viene specificato un limite di intervallo, il valore di budget minimo viene sempre calcolato come percentuale del limite di intervallo. In caso contrario, viene calcolata come percentuale del budget del pacchetto.

**[!UICONTROL Max Bid]:** Il massimo da pagare per 1000 impression.

**[!UICONTROL Placement Pre-bid Filters]:** Fino a cinque soglie KPI (ad esempio una metrica minima di visualizzabilità o un tasso di click-through) che devono essere soddisfatte affinché la licitazione avvenga. Puoi utilizzare i filtri di pre-offerta come tattiche di ottimizzazione, ma assicurati che ogni regola possa limitare le opportunità su cui questo posizionamento può fare offerte. Per aggiungere o modificare i filtri:

1. Fai clic su ![Modifica](/help/dsp/assets/edit.png).
1. Effettuare una delle seguenti operazioni:
   * Per aggiungere un filtro:
      1. Fare clic su **[!UICONTROL Add Filter]**.
      1. Accanto a **[!UICONTROL Only bid if]**, selezionare una metrica, quindi immettere un valore.
   * Per rimuovere un filtro, fare clic su **[!UICONTROL X]** nella riga del filtro.
1. Fare clic su **[!UICONTROL Save]**.

Vedi le descrizioni di ciascun filtro pre-offerta in &quot;[Filtri pre-offerta a livello di posizionamento e come utilizzarli](/help/dsp/optimization/optimization-pre-bid-filters.md).&quot;

### Tutti gli altri posizionamenti

**[!UICONTROL Budget Goal]:** Limite di budget lordo e intervallo di budget (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

**[!UICONTROL Gross Budget Goal]:** (Posizionamenti solo in campagne con gestione margini) Limite di budget lordo e intervallo di budget (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

**[!UICONTROL Optimization Goal]:** L&#39;obiettivo di ottimizzazione per il pacchetto. Vedi le descrizioni di ogni obiettivo di ottimizzazione in &quot;[Obiettivi di ottimizzazione e come utilizzarli](/help/dsp/optimization/optimization-goals.md)&quot;.

**[!UICONTROL Target Goal]:** L&#39;obiettivo di destinazione, utilizzato per tenere traccia delle prestazioni.

>[!NOTE]
>
>Questo campo è solo un valore di riferimento e non viene utilizzato per le decisioni.

**[!UICONTROL Pace on]:** La base per il ritmo:

* **[!UICONTROL Budget goal]:** (predefinito) Questa opzione fornisce il maggior numero di impression possibile nel budget allocato.

* **[!UICONTROL Impressions]:** Questa opzione fornisce impression fino al raggiungimento di una quantità specificata entro un intervallo specificato. Quando si seleziona questa opzione, specificare il numero di impression e l&#39;intervallo: *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* o *[!UICONTROL Weekly]*.

**[!UICONTROL Max Bid]:** Il massimo da pagare per 1000 impression.

**[!UICONTROL Flight pacing]:** (solo posizionamenti con velocità a livello di posizionamento) Come pianificare la consegna degli annunci:

* *[!UICONTROL Even]:* (impostazione predefinita) La consegna avviene in modo uniforme per ogni volo, con un target pari al 50% della consegna nella prima metà del volo.

* *[!UICONTROL Slightly Ahead]:* (impostazione predefinita) Accelera la consegna in modo che sia completa al 55-65% a metà della durata del volo.

* *[!UICONTROL Frontload]:* Accelera la consegna in modo che sia completa al 65-75% a metà del volo.

* *[!UICONTROL Aggressive Frontload]:* Accelera la consegna in modo che sia completa al 75-85% a metà del volo.

**[!UICONTROL Intraday pacing]:** (solo posizionamenti con velocità a livello di posizionamento) Come pianificare la consegna di annunci in ogni giorno all&#39;interno del volo:

* *[!UICONTROL Even]:* (impostazione predefinita) Ridimensiona la consegna in base alla disponibilità dell&#39;inventario. In genere, vengono consegnati più annunci all’ora di giorno, quando il volume dell’asta è più alto e vengono consegnati meno annunci al mattino e alla sera.

* *[!UICONTROL ASAP]:* (impostazione predefinita) Accelera la consegna a una velocità doppia rispetto a *Even*.

  >[!CAUTION]
  >
  >Questa opzione può influire negativamente sulle prestazioni. Utilizzalo solo quando assegni la massima priorità alla consegna e spendi oltre l’ottimizzazione delle prestazioni.

**[!UICONTROL Placement Pre-bid Filters]:** (facoltativo) fino a cinque filtri che devono essere soddisfatti perché l&#39;offerta si verifichi. Puoi utilizzare i filtri di pre-offerta come tattiche di ottimizzazione, ma tieni presente che ogni regola può limitare le opportunità su cui questo posizionamento può fare offerte. Per aggiungere o modificare i filtri:

1. Fai clic su ![Modifica](/help/dsp/assets/edit.png).
1. Effettuare una delle seguenti operazioni:
   * Per aggiungere un filtro:
      1. Fare clic su **[!UICONTROL Add Filter]**.
      1. Accanto a **[!UICONTROL Only bid if]**, selezionare una metrica, quindi immettere un valore.
   * Per rimuovere un filtro, fare clic su **[!UICONTROL X]** nella riga del filtro.
1. Fare clic su **[!UICONTROL Save]**.

## [!UICONTROL Geo-Targeting]

**[!UICONTROL Audience Location]:** (facoltativo) posizioni specifiche in cui includere o escludere annunci nel posizionamento. Se non specifichi alcuna posizione, viene eseguito il targeting di tutte le posizioni.

>[!NOTE]
>
>Le posizioni Città e DMA non sono disponibili per i posizionamenti Roku.

Per specificare le posizioni:

1. Fai clic su ![Modifica](/help/dsp/assets/edit.png).
1. Effettua una delle seguenti operazioni:
   * Per includere o escludere un paese, uno stato, una città, un DMA, un distretto legislativo federale o un distretto legislativo statale:
      1. Seleziona il tipo di posizione nella colonna a sinistra.
      1. (Se necessario) Fai clic su una posizione per espanderla.
      1. Accanto al percorso, fare clic su *[!UICONTROL Include]* per includerlo come destinazione o su *[!UICONTROL Exclude]* per escluderlo come destinazione.
   * Per cercare un codice postale e includere o escludere tutti i risultati selezionati:
      1. Fare clic su **[!UICONTROL Search Postal Code]**.
      1. Seleziona il paese.
      1. Immettere il nome della città, quindi fare clic su ![Modifica](/help/dsp/assets/search.png).
      1. Fare clic sul risultato di ricerca corretto.
      1. Fare clic su *[!UICONTROL Include All]* per includere tutte le posizioni come destinazioni o su *[!UICONTROL Exclude All]* per escludere tutte le posizioni come destinazioni.
   * Per inserire o incollare codici postali e includerli o escluderli tutti:
      1. Fare clic su **[!UICONTROL Paste Postal Code]**.
      1. Seleziona il paese.
      1. Inserisci o incolla fino a 1000 codici postali.
Includere un codice postale per riga oppure immettere più valori separati da virgole o tabulazioni.
      1. Fare clic su *[!UICONTROL Include All]* per includere tutte le posizioni come destinazioni o su *[!UICONTROL Exclude All]* per escludere tutte le posizioni come destinazioni.
   * Per rimuovere un percorso dall&#39;elenco [!UICONTROL Included] o [!UICONTROL Excluded], fare clic su **[!UICONTROL X]** accanto al percorso nella colonna di destra.
1. Fare clic su **[!UICONTROL Done]**.

>[!NOTE]
>
>* Non tutti i paesi dispongono di località con codice postale, Stato o Città.
>* DMA (area di mercato designata), Federal Legislative Districts e State Legislative Districts sono disponibili solo per le sedi degli Stati Uniti.

## [!UICONTROL Inventory Targeting]

**[!UICONTROL Inventory Sources]:** origini inventario da includere o escludere come destinazioni. Per la maggior parte dei tipi di posizionamento, tutti i tipi di inventario e tutte le origini per ciascun tipo sono inclusi per impostazione predefinita. Per [!DNL Roku] posizionamenti, è necessario specificare il tipo di inventario e le origini. È possibile scegliere tra i seguenti tipi di inventario:

* [!UICONTROL Public]: (tutti i tipi di posizionamento ad eccezione di Roku) Tutti gli inventari a cambio aperto a cui l&#39;DSP ha accesso. Puoi includere ed escludere l’inventario pubblico.

  È possibile visualizzare l’elenco in base all’origine o al feed. Quando visualizzi l’elenco per feed, puoi eseguire ricerche per nome di feed, chiave di feed o un tag di caratteristica selezionato.

* [!UICONTROL Private] | [!UICONTROL Roku Private]: le tue offerte private esistenti (o offerte private [!DNL Roku] esistenti per [!DNL Roku] posizionamenti) con editori che hai impostato in DSP. È possibile includere ma non escludere l&#39;inventario pubblico.

  Puoi cercare l’elenco per parola chiave, chiave, ID offerta o tag personalizzato.

   * *[!UICONTROL Ensure Fixed or Floor Price for the bid]*: (Facoltativo) Sostituisce l&#39;algoritmo del prezzo dell&#39;offerta per offrire almeno i prezzi fissi e minimi per le offerte.

* [!UICONTROL On Demand] | [!UICONTROL Roku On Demand]: tutte le [offerte premium, [!UICONTROL On Demand] inventory](/help/dsp/inventory/on-demand-inventory-about.md) non garantite (o [!UICONTROL On Demand] [!DNL Roku] offerte per [!DNL Roku] posizionamenti) alle quali ti sei iscritto in [!DNL DSP]. È possibile includere ed escludere [!UICONTROL On Demand] inventario.

  È possibile visualizzare l’elenco in base all’origine o al feed. Quando l&#39;elenco viene visualizzato per feed, è possibile eseguire ricerche per nome di feed, chiave di feed oppure per l&#39;area dell&#39;editore selezionata, il tag categoria o il tag caratteristica.

   * *[!UICONTROL Ensure Fixed or Floor Price for the bid]*: (Facoltativo) Sostituisce l&#39;algoritmo del prezzo dell&#39;offerta per offrire almeno i prezzi fissi e minimi per le offerte.

Per specificare il targeting dell&#39;inventario:

* Per escludere un tipo di inventario, deselezionare la casella di controllo accanto al nome.
* Per eseguire il targeting di un tipo di inventario:
   1. Selezionare la casella di controllo accanto al nome del tipo di inventario.
   1. (Facoltativo) Modifica le origini per includere:
      1. Fai clic su ![Modifica](/help/dsp/assets/edit.png).
      1. ([!UICONTROL Public] e [!UICONTROL On Demand] inventario) Fare clic su **[!UICONTROL View by Source]** o **[!UICONTROL View by Feed]** per modificare l&#39;elenco delle origini.
      1. (Se applicabile) Filtra l’inventario in base alle esigenze.
      1. Specificare le origini da includere ed escludere:
         * Per includere un&#39;origine [!UICONTROL Public] o [!UICONTROL On Demand], fare clic su **[!UICONTROL Include]** accanto al nome dell&#39;origine.
         * Per includere [!UICONTROL Private] origini:
            * Per includere tutte le scorte in un&#39;offerta, fare clic su **[!UICONTROL Include all]** accanto al nome dell&#39;offerta.
            * Per includere una singola origine di magazzino, espandere il nome dell&#39;offerta e quindi fare clic sulla casella di controllo accanto al nome dell&#39;origine.
         * Per escludere [!UICONTROL Public] o [!UICONTROL On source], fare clic su **[!UICONTROL Exclude]** accanto al nome di origine.
   1. (Facoltativo) Per scaricare un file CSV con le informazioni di targeting nel percorso Download del browser, fai clic su **[!UICONTROL Save & Export]**.
   1. Fare clic su **[!UICONTROL Save]**.

>[!TIP]
>
>Se ti sei iscritto al magazzino [!UICONTROL On Demand] ma non riesci a individuare gli editori o le offerte di destinazione, controlla lo stato delle offerte. Per ulteriori informazioni sugli stati, vedere [Informazioni su [!DNL On Demand] Inventario Premium](/help/dsp/inventory/on-demand-inventory-about.md).

**[!UICONTROL Exclude out-stream]:** (solo posizionamenti video) Esclude il traffico in uscita.

Gli annunci in uscita vengono solitamente visualizzati sul contenuto come pop-up o inseriti nel contenuto (nell’esperienza nativa), anziché come annunci video regolari in un lettore video.

## [!UICONTROL Site and App Targeting]

**[!UICONTROL Traffic type]:** i tipi di traffico da destinare. Le opzioni includono **[!UICONTROL Websites]** e **[!UICONTROL Apps]**.

**[!UICONTROL Tier]:** (disponibile quando **[!UICONTROL Paste list of targeted sites]** è *[!UICONTROL Off]*) Qualità del traffico di destinazione. I livelli 1-3 sono tutti brand safe e sono stati approvati dal team di mappatura DSP.

* *[!UICONTROL Tier 1]:* siti e applicazioni Premium riconoscibili a livello nazionale.

* *[!UICONTROL Tier 2]:* destinazioni Livello 1 nonché siti e applicazioni di qualità meno conosciuti rispetto al Livello 1.

* *[!UICONTROL Tier 3]:* ha come target i livelli 1-2, oltre a siti e applicazioni legittimi e sicuri per il brand adatti a un pubblico di nicchia. Utilizza il livello 3 per le compravendite con targeting di dati o portata.

* *[!UICONTROL All Sites or Apps]:* ha come target i livelli 1-3 e il nuovo inventario che non è stato né schermato né categorizzato, che puoi utilizzare per la portata.

>[!NOTE]
>
>L’inventario è specifico per le unità pubblicitarie nel posizionamento.

>[!TIP]
>
>Per le campagne sulle prestazioni, la best practice prevede di selezionare *[!UICONTROL All Sites]*.

**[!UICONTROL Site or App Categories]:** (Facoltativo; disponibile quando **[!UICONTROL Paste list of targeted sites]** è *[!UICONTROL Off]*) Categorie di siti all&#39;interno dei livelli di sito selezionati da includere o escludere (ma non entrambi) come destinazioni. Scegli da elenchi di siti verticali che l&#39;DSP ha mappato in base all&#39;oggetto:

1. Fai clic su ![Modifica](/help/dsp/assets/edit.png).
1. Specificare le categorie del sito da includere o escludere:
   * Per includere le categorie del sito:
      1. Fare clic su **[!UICONTROL Include categories]**.
      1. Selezionare la casella di controllo accanto a ogni categoria di destinazione.
   * Per escludere le categorie di siti:
      1. Fare clic su **[!UICONTROL Exclude categories]**.
      1. Selezionare la casella di controllo accanto a ogni categoria da escludere.
1. (Facoltativo) Per scaricare un file CSV con le informazioni di targeting nel percorso Download del browser, fai clic su **[!UICONTROL Export]**.
1. Fare clic su **[!UICONTROL Save]**.

**[!UICONTROL Exclude Sites or Apps]:** (facoltativo; disponibile quando **[!UICONTROL Paste list of targeted sites]** è *[!UICONTROL Off]*) Siti da escludere. È possibile cercare e selezionare i siti oppure immettere o incollare i nomi di dominio:

1. Fai clic su ![Modifica](/help/dsp/assets/edit.png).
1. Specificare i siti:
   * Per cercare un sito:
      1. Fare clic su **[!UICONTROL Search]**.
      1. Immettere una parola chiave, selezionare un livello del sito e/o selezionare una categoria del sito.
      1. Nei risultati della ricerca, seleziona i siti da escludere:
         * Per escludere un singolo sito, selezionare la casella di controllo adiacente.
         * (Quando sono disponibili più di 50 risultati) Per escludere i primi 50 risultati, fare clic su **[!UICONTROL Exclude these 50]**. Per escludere tutti i risultati della ricerca, fare clic su **[!UICONTROL Exclude these \<*NN *\>]**.
   * Per immettere i nomi di dominio:
      1. Fare clic su **[!UICONTROL Paste]**.
      1. Immetti uno o più nomi di dominio su righe separate.
      1. Fare clic su **[!UICONTROL Exclude All]**.
1. Al termine, fai clic su **[!UICONTROL Done]**.

>[!NOTE]
>
>* Vengono applicati anche elenchi di siti bloccati a livello di account e inserzionista, oltre all&#39;elenco di siti bloccati ](/help/dsp/introduction/features/brand-safety-media-quality.md) dell&#39;DSP [globally blocked, che include siti ritenuti non sicuri per gli annunci.
>* Gli elenchi di siti bloccati sostituiscono sempre gli elenchi di siti di destinazione. Se un posizionamento esclude e include lo stesso target per un annuncio, il target viene escluso.

**[!UICONTROL Language]:** (Facoltativo) Una singola lingua di destinazione.

**[!UICONTROL Site or App List Preview]:** (sola lettura) Tutti i siti di destinazione e bloccati per il posizionamento.

Facoltativamente, puoi esportare l’elenco dei siti di destinazione e dei siti bloccati come file con valori separati da virgola (CSV). Per esportare l&#39;elenco, fare clic su **[!UICONTROL Export full site list]**, quindi aprire o salvare il file in base alla normale procedura del browser.

**[!UICONTROL Allow unscreened sites]:** (solo posizionamenti di visualizzazione standard) Abilita la consegna di annunci su siti non controllati. Quando il posizionamento ha come target l’inventario privato, questa opzione può distribuire annunci sui siti bloccati.

**[!UICONTROL Paste list of targeted sites]:** consente di eseguire il targeting solo di siti specifici. Quando si attiva questa opzione, le altre opzioni di targeting del sito vengono disattivate.

**[!UICONTROL Sites]:** (disponibile quando **[!UICONTROL Paste list of targeted sites]** è *[!UICONTROL On]*) Siti di destinazione. È possibile cercare e selezionare i siti oppure immettere o incollare i nomi di dominio:

1. Fai clic su ![Modifica](/help/dsp/assets/edit.png).
1. Specificare i siti:
   * Per cercare un sito:
      1. Fare clic su **[!UICONTROL Search]**.
      1. Immettere una parola chiave, selezionare un livello del sito e/o selezionare una categoria del sito.
      1. Nei risultati della ricerca, selezionare i siti da includere:
         * Per escludere un singolo sito, selezionare la casella di controllo adiacente.
         * (Quando sono disponibili più di 50 risultati) Per includere i primi 50 risultati, fare clic su **[!UICONTROL Include these 50]**. Per includere tutti i risultati della ricerca, fare clic su **[!UICONTROL Include these \<*NN *\>]**.
   * Per immettere i nomi di dominio:
      1. fare clic su **[!UICONTROL Paste]**.
      1. Immetti uno o più nomi di dominio su righe separate.
      1. Fare clic su **[!UICONTROL Include All]**.
1. Fare clic su **[!UICONTROL Done]**.

## [!UICONTROL Audience Targeting]

**[!UICONTROL Included Audiences]:** Qualsiasi destinazione di pubblico per il posizionamento, inclusi [segmenti di terze parti, segmenti di prime parti, segmenti di Adobe, segmenti personalizzati e tipi di pubblico salvati](/help/dsp/audiences/audience-settings.md). Vengono visualizzate anche le dimensioni del pubblico deduplicato totale e attivo per tutti i segmenti selezionati e i tipi di pubblico salvati. Puoi selezionare un pubblico esistente, crearne uno da riutilizzare in un secondo momento o selezionare segmenti di pubblico specifici:

* Per selezionare un pubblico esistente, fare clic su ![Seleziona](/help/dsp/assets/chevron-down.png) accanto a [!UICONTROL Included Audiences], quindi selezionare il pubblico.
* Per creare un pubblico, fai clic su ![Seleziona](/help/dsp/assets/chevron-down.png) accanto a [!UICONTROL Included Audiences], quindi seleziona **[!UICONTROL + Create Audience]**. Per istruzioni, vedere [Creare un pubblico riutilizzabile](/help/dsp/audiences/reusable-audience-create.md), a partire dal passaggio 3.
* Per selezionare segmenti di pubblico specifici, fare clic su **[!UICONTROL Select segments for this placement only]**. Selezionare la logica del segmento; per istruzioni, vedere il passaggio 6 in &quot;[Creare un pubblico riutilizzabile](/help/dsp/audiences/reusable-audience-create.md).&quot; Al termine, fai clic su **Salva**.

**[!UICONTROL Excluded Audiences]:** Qualsiasi pubblico da escludere per il posizionamento, inclusi i tipi di pubblico con [segmenti di terze parti, segmenti di prime parti, segmenti di Adobe, segmenti personalizzati e tipi di pubblico salvati](/help/dsp/audiences/audience-settings.md). Viene visualizzata anche la dimensione totale e attiva del pubblico deduplicato in tutti i tipi di pubblico esclusi. Puoi selezionare un pubblico esistente o crearne uno nuovo da riutilizzare in un secondo momento:

* Per selezionare un pubblico esistente, fare clic su ![Seleziona](/help/dsp/assets/chevron-down.png) accanto a [!UICONTROL Excluded Audiences], quindi selezionare il pubblico.

* Per creare un pubblico, fai clic su ![Seleziona](/help/dsp/assets/chevron-down.png) accanto a [!UICONTROL Excluded Audiences], quindi seleziona **+ Crea pubblico**. Per istruzioni, vedere [Creare un pubblico riutilizzabile](/help/dsp/audiences/reusable-audience-create.md), a partire dal passaggio 3.

**[!UICONTROL Targeting]:** i tipi di ID utente di destinazione. Non puoi modificare questa impostazione dopo che il posizionamento è attivo (cioè, dopo che il volo è iniziato).

Quando selezioni sia ID legacy che ID universali, viene data la preferenza di offerta agli ID universali.

* *[!UICONTROL Legacy IDs (Cookies, MAIDS, CTV)]*: (impostazione predefinita) esegue il targeting degli utenti in base ai cookie, agli ID mobile advertising o agli ID connected TV (CTV). Gli ID vengono selezionati in base all’inventario del browser, in-app o CTV.

* *[!UICONTROL Universal ID Beta]*: esegue il targeting degli ID incentrati sulla privacy dell&#39;utente; seleziona un tipo di ID. Le opzioni disponibili sono determinate dai target geografici selezionati nella sezione [!UICONTROL Geo-Targeting]. Usare con [[!DNL RampID] segmenti importati direttamente in DSP](/help/dsp/audiences/sources/source-import-liveramp-segments.md), [segmenti per i quali DSP converte i dati PII in ID universali](/help/dsp/audiences/sources/source-about.md) o [segmenti personalizzati che tengono traccia degli ID universali](/help/dsp/audiences/custom-segment-create.md).

   * *[!UICONTROL ID5]*: destinazioni [!DNL ID5] ID creati con probabilità da indirizzi e-mail e altri segnali.<!-- What countries/geos are these available for? Everywhere?--> ID5 sono disponibili gratuitamente. **Nota:** i segmenti di terze parti di [!DNL Eyeota] possono includere ID5.

   * *[!UICONTROL RampID]*: destinazioni [!DNL LiveRamp] [!DNL RampIDs] di utenti connessi al sito tramite i relativi indirizzi e-mail.<!-- Verify --> [!DNL RampIDs] sono disponibili per gli utenti in Nord America, Australia e Nuova Zelanda.

   * *[!UICONTROL Unified ID2.0]*: Target [!DNL Unified ID2.0] (UID2) ID degli utenti connessi al sito utilizzando i loro indirizzi e-mail.<!-- Verify -->[!DNL UID2 IDs] non sono disponibili per gli utenti nello Spazio economico europeo e in alcuni altri paesi. Vedi l&#39;[elenco dei paesi vietati](/help/policies/universal-id-policy.md#prohibited-countries-uid2).

  **[!UICONTROL Terms of service]**: i termini del contratto di servizio per l&#39;utilizzo degli ID universali. Prima di poter convertire i dati in un nuovo tipo di ID, tu o un altro utente dell’account DSP dovete accettare i termini una volta. Per i clienti con contratti di assistenza gestiti, il team dell’account Adobe riceverà il consenso e accetterà le condizioni per conto della tua organizzazione. Per leggere i termini, fare clic su **>**. Per accettare i termini, scorrere fino alla fine dei termini e fare clic su **[!UICONTROL Accept]**.

**[!UICONTROL Cross Device Targeting]:** (disponibile quando la [campagna è configurata per il targeting multidispositivo basato sulle persone](/help/dsp/campaign-management/campaigns/campaign-settings.md), esegui il targeting solo degli ID legacy (non degli ID universali) e selezioni almeno un segmento o un pubblico. Consente di estendere il targeting su tutti i dispositivi noti di una persona (in base al grafico dei dispositivi specificato nelle impostazioni della campagna), anche su dispositivi che non si trovano nei segmenti specificati. Le tariffe possono essere applicate a seconda del grafico specificato per la campagna. I dati del grafico dei dispositivi sono disponibili solo in Nord America.

**[!UICONTROL Placement Cap]:** (Facoltativo) Il numero di volte in cui un dispositivo univoco, un ID universale o una persona (a seconda del [!UICONTROL Cross Device Level] specificato per la campagna e dell&#39;impostazione [!UICONTROL Targeting] del posizionamento) possono essere serviti annunci dal posizionamento. Le opzioni includono *[!UICONTROL Unlimited]* o un importo specifico per giorno, settimana o mese.

>[!NOTE]
>
> Puoi impostare i limiti di frequenza a livello di campagna, pacchetto e posizionamento. L’DSP rispetta il limite di frequenza più severo nella gerarchia delle campagne.

**[!UICONTROL Secondary Cap]:** (Facoltativo; disponibile quando si include un numero [!UICONTROL Placement Cap]) Limitazione aggiuntiva entro i limiti del limite di posizionamento primario. Seleziona il numero di impression e il periodo di tempo (ad esempio 3 ogni 12 ore).

**[!UICONTROL Day Parting]:** (facoltativo) giorni specifici della settimana e dell&#39;ora del giorno in cui possono essere eseguiti gli annunci. Per specificare gli intervalli di partenze diurne:

1. Fai clic su ![Modifica](/help/dsp/assets/edit.png).
1. Seleziona il fuso orario applicabile.
1. Specifica gli intervalli:
   * Per selezionare un intervallo predefinito, fare clic su uno dei pulsanti di intervallo. Le opzioni includono *[!UICONTROL Weekends]**, *[!UICONTROL Weekdays]*, *[!UICONTROL Morning]*, *[!UICONTROL Lunch]*, *[!UICONTROL Dinner]* o *[!UICONTROL Prime]* (primetime).
   * Per selezionare manualmente un intervallo, fare clic all&#39;interno di una cella e, facoltativamente, trascinare per selezionare l&#39;intervallo.
1. Fare clic su **[!UICONTROL Save]**.

**[!UICONTROL Topic Targeting]:** (Facoltativo; disponibile per gli inserzionisti configurati con [!DNL Proximic by Comscore] segmenti) Nomi di segmenti o ID di segmenti specifici da [!DNL Proximic by Comscore] da includere come destinazioni. Per questa funzione potrebbero essere applicati costi aggiuntivi. Per attivare questa funzione e configurare i segmenti di argomento, contatta il team del tuo account Adobe.

Per specificare il targeting degli argomenti:

1. Fai clic su ![Modifica](/help/dsp/assets/edit.png).
1. Specifica i segmenti di destinazione:
   1. Nella colonna sinistra, selezionare il partner: (*[!UICONTROL Comscore]*.
   1. Nel campo di immissione, inserisci i nomi o gli ID del segmento.
1. (Facoltativo) Per scaricare un file CSV con le informazioni dell&#39;argomento nel percorso Download del browser, fare clic su **[!UICONTROL Export]**.
1. Fare clic su **[!UICONTROL Save]**.

>[!TIP]
>
>* Il targeting degli argomenti limita l’inventario su cui il posizionamento può fare offerte, quindi utilizza il targeting degli argomenti solo per una piccola percentuale dell’acquisto complessivo.
>
>* Imposta eventuali targeting negativi all&#39;interno del segmento su [!DNL Proximic by Comscore].

**[!UICONTROL Device Targeting]:** (facoltativo) informazioni specifiche sul dispositivo, inclusi tipi di dispositivo, produttori, sistemi operativi, browser e tipi di connettività, da includere ed escludere come destinazioni. I tipi variano in base al tipo di posizionamento. Per specificare il targeting del dispositivo:

1. Fai clic su ![Modifica](/help/dsp/assets/edit.png).
1. Specifica i dettagli del dispositivo da includere ed escludere:
   1. Nella colonna sinistra selezionare la categoria.
   1. Specifica destinazione:
      * Per includere un valore, fare clic su **[!UICONTROL Include]** accanto al nome del valore.
      * Per escludere un valore, fare clic su **[!UICONTROL Exclude]** accanto al nome del valore.
1. (Facoltativo) Per scaricare un file CSV con le informazioni di targeting del dispositivo nella posizione Download del browser, fai clic su **[!UICONTROL Export]**.
1. Fare clic su **[!UICONTROL Save]**.

**[!UICONTROL ISP Targeting]:** (facoltativo) provider di servizi Internet (ISP) specifici da includere o escludere (ma non entrambi) come destinazioni. Per specificare il targeting ISP:

1. Fai clic su ![Modifica](/help/dsp/assets/edit.png).
1. Specifica gli ISP da includere o escludere:
   * Per includere gli ISP:
      1. Fare clic su **[!UICONTROL Include ISPs]**.
      1. (Facoltativo) Filtra l’elenco per parola chiave.
      1. Selezionare la casella di controllo accanto a ogni ISP di destinazione.
   * Per escludere gli ISP:
      1. Fare clic su **[!UICONTROL Exclude ISPs]**.
      1. (Facoltativo) Filtra l’elenco per parola chiave.
      1. Selezionare la casella di controllo accanto a ogni ISP da escludere.
1. (Facoltativo) Per scaricare un file CSV con le informazioni di targeting dell&#39;ISP nel percorso Download del browser, fai clic su **[!UICONTROL Export]**.
1. Fare clic su **[!UICONTROL Save]**.

## [!UICONTROL Brand Safety and Media Quality]

**[!UICONTROL DoubleVerify ABS segment ID]:** (Facoltativo; solo [!DNL DoubleVerify] clienti; disponibile solo per la visualizzazione pre-roll desktop, standard e click-to-play e per i posizionamenti di video e visualizzazioni nativi; non supportato per [posizionamenti programmatici predefiniti garantiti per offerte](/help/dsp/inventory/programmatic-guaranteed-about.md)) Un ID segmento [!DNL DoubleVerify Authentic Brand Safety] associato all&#39;account [!DNL DoubleVerify] dell&#39;organizzazione da utilizzare per il posizionamento. La specifica di un ID blocca le impression dopo l’offerta utilizzando le regole di sicurezza del brand personalizzate configurate per l’ID segmento specificato. L’DSP fattura il tuo account per l’utilizzo dell’ID segmento.

L’ID deve iniziare con &quot;51&quot; e consistere di otto cifre. Per impostazione predefinita, se nelle impostazioni dell’account dell’inserzionista è specificato un ID di segmento, viene inserito l’ID a livello dell’inserzionista, ma puoi modificarlo per utilizzare un segmento diverso o eliminare l’ID per disabilitare la funzione.

**[!UICONTROL Contextual filtering]:** tipi di filtri contestuali [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science] e [!DNL Peer39] da applicare. Le impostazioni predefinite a livello di inserzionista vengono selezionate per i nuovi posizionamenti, ma è possibile modificare le impostazioni:

<!-- Looks like we didn't rename this:
**[!UICONTROL Brand Safety categories]:** Types of [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], and [!DNL Peer39] brand safety category filters to apply. The advertiser-level defaults are selected for new placements, but you can change the settings:
-->

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block sites that are]:** (facoltativo) Uno o più tipi di contesto di inventario da bloccare per impostazione predefinita. Possono essere applicate tariffe aggiuntive.

* [!UICONTROL Peer 39]:

   * **Siti di destinazione che sono:** (facoltativo) Uno o più tipi di attributi di inventario per destinazione per impostazione predefinita. Possono essere applicate tariffe aggiuntive.

* [!UICONTROL ComScore]:

   * **Blocca siti:** (facoltativo) Uno o più tipi di attributi di inventario da bloccare per impostazione predefinita. Possono essere applicate tariffe aggiuntive.

* [!UICONTROL Integral Ad Science]

   * **[!UICONTROL Adult Content]:** (Facoltativo) Il livello di contenuto per adulti per il quale bloccare gli annunci per impostazione predefinita: *[!UICONTROL Do Not Block]* (impostazione predefinita), *[!UICONTROL Standard]* o *[!UICONTROL Strict]*. Possono essere applicate tariffe aggiuntive.

   * **[!UICONTROL Alcohol Content]:** (Facoltativo) Il grado di contenuto alcolico per il quale bloccare gli annunci per impostazione predefinita: *[!UICONTROL Do Not Block]* (impostazione predefinita), *[!UICONTROL Standard]* o *[!UICONTROL Strict]*. Possono essere applicate tariffe aggiuntive.

**[!UICONTROL Pre-bid fraud blocking]:** tipi di siti da bloccare in base al traffico fraudolento e alle attività sospette misurate tramite [!DNL DoubleVerify], [!DNL Integral Ad Science] e [!DNL Peer39]. Le impostazioni predefinite a livello di inserzionista vengono selezionate per i nuovi posizionamenti, ma è possibile modificare le impostazioni:

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** Per impostazione predefinita, blocca tutto il traffico non valido al 100%, incluso il traffico su dispositivi dirottati, per i nuovi posizionamenti. Possono essere applicate tariffe aggiuntive.

   * **[!UICONTROL Also block sites with]:** (Facoltativo) Livello aggiuntivo di frode e traffico non valido che causa il blocco predefinito degli annunci da parte dell&#39;DSP: *[!UICONTROL None]* (impostazione predefinita, che non blocca il traffico aggiuntivo), *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*, *[!UICONTROL >4% Average Fraud/IVT levels]*, *[!UICONTROL >6% Average Fraud/IVT levels]*, *[!UICONTROL >10% Average Fraud/IVT levels]* o *[!UICONTROL >25% Average Fraud/IVT levels]*. Possono essere applicate tariffe aggiuntive.

* [!UICONTROL Peer 39]:

   * **[!UICONTROL Block sites that are]:** (facoltativo) Uno o più tipi di frode che causano il blocco predefinito degli annunci da parte del DSP: *[!UICONTROL Fraud]* (che blocca tutti i siti con frode), *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]* e/o *[!UICONTROL Fraud: Zero Ads]*. Possono essere applicate tariffe aggiuntive.

* [!UICONTROL Integral Ad Science]:

   * **[!UICONTROL Block sites that are]:** (Facoltativo) Tipo di attività sospetta del sito Web o dell&#39;app che induce l&#39;DSP a bloccare gli annunci per impostazione predefinita: *[!UICONTROL None]* (impostazione predefinita, che non blocca gli annunci basati su attività sospette), *[!UICONTROL Suspicious Activity - High Risk]* o *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. Possono essere applicate tariffe aggiuntive.

**[!UICONTROL Pre-bid viewability]:**

Quali filtri di visibilità pre-offerta vengono filtrati da [!DNL DoubleVerify] e [!DNL Integral Ad Science] da applicare per il posizionamento. Le impostazioni predefinite a livello di inserzionista vengono selezionate per i nuovi posizionamenti, ma è possibile modificarle. Possono essere applicate tariffe aggiuntive.

**[!UICONTROL Ads.txt filtering]:**

Quale livello di filtro pre-offerta di [Ads.txt](https://iabtechlab.com/ads-txt-about/) utilizzare applicando l&#39;elenco di venditori digitali autorizzati di ogni editore. Il valore predefinito a livello di inserzionista viene selezionato per i nuovi posizionamenti, ma è possibile modificare le impostazioni:

* *[!UICONTROL Opt out of ads.txt (default)]*: per acquistare le scorte da tutti i venditori.
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*: per dare priorità all&#39;acquisto di scorte dai venditori diretti e dai rivenditori autorizzati di un dominio.
* *[!UICONTROL Ads.txt sellers only]*: per acquistare le scorte solo dai venditori diretti e dai rivenditori autorizzati di un dominio.
* *[!UICONTROL Ads.txt sellers only]*: per acquistare le scorte solo dai venditori diretti autorizzati di un dominio.

**[!UICONTROL Attention Targeting]:** (visualizzazione, video e posizionamenti TV connessi standard) Destinazioni [!DNL Adelaide] segmenti pre-offerta con un livello di attenzione specifico (alto, medio o basso) in base al sito, al formato e alle dimensioni dell&#39;annuncio specificati. I segmenti vengono aggiornati settimanalmente. **Nota:** l&#39;utilizzo di [!DNL Adelaide] segmenti per il targeting comporta una tariffa CPM per ogni impression distribuita con [!DNL Adelaide] targeting di attenzione; questa tariffa è separata dalle tariffe per [misurazione dell&#39;attenzione](/help/dsp/campaign-management/campaigns/campaign-settings.md). Per i posizionamenti pre-roll interattivi, il costo viene addebitato solo per le impressioni VAST.

## [!UICONTROL Tracking] {#placement-tracking}

>[!NOTE]
>
>([!DNL Roku] posizionamenti) I fornitori di tracciamento di terze parti approvati da [!DNL Roku] includono [!DNL Acxiom], [!DNL Comscore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk] e [!DNL Research Now].

**[!UICONTROL Event Pixels]:** (facoltativo) pixel di tracciamento eventi di terze parti da allegare per impostazione predefinita a tutti i nuovi annunci nel posizionamento. Per specificare i pixel dell&#39;evento:

1. Fai clic su ![Modifica](/help/dsp/assets/edit.png).
1. Effettua una delle seguenti operazioni:
   * Per selezionare un pixel esistente, selezionare la casella di controllo nella riga dei pixel.
   * Per creare un pixel:
      1. Fare clic su **[!UICONTROL Create]**.
      1. Immettere le seguenti informazioni:
         * **[!UICONTROL Pixel name]:** Il nome del pixel; la lunghezza massima è di 500 caratteri. Utilizza un nome che ti consenta di identificare facilmente il pixel.
         * **[!UICONTROL Pixel event fires on]:** l&#39;evento che attiva il pixel per l&#39;attivazione. Gli eventi disponibili variano in base al tipo di annuncio.
         * **[!UICONTROL Pixel type]:** Se il pixel è un *[!UICONTROL IMG URL]* (file immagine 1x1 pixel), *[!UICONTROL HTML]* o *[!UICONTROL JavaScript URL]*.
         * **[!UICONTROL Pixel URL]:** URL dell&#39;immagine pixel.
      1. Fare clic su **[!UICONTROL Create and attach]**.
   1. Fare clic su **[!UICONTROL Save]**.

**[!UICONTROL Conversion Pixels]:** (facoltativo) pixel di tracciamento conversione da allegare per impostazione predefinita a tutti i nuovi annunci nel posizionamento. Per specificare i pixel di conversione:

1. Fai clic su ![Modifica](/help/dsp/assets/edit.png).
1. Effettua una delle seguenti operazioni:
   * Per selezionare un pixel esistente, selezionare la casella di controllo nella riga dei pixel.
   * Per creare un pixel:
      1. Fare clic su **[!UICONTROL Create]**.
      1. Immettere le seguenti informazioni:
         * **[!UICONTROL Conversion pixel name]:** Il nome del pixel; la lunghezza massima è di 500 caratteri. Utilizza un nome che ti consenta di identificare facilmente il pixel.
         * **[!UICONTROL Conversion category]:** Il tipo di conversione.
         * **[!UICONTROL Impression conversion window]:** il numero di giorni dopo i quali si verifica un&#39;impression pubblicitaria, in cui l&#39;impression può essere attribuita a una conversione. Il valore predefinito è 30 giorni.
         * **[!UICONTROL Click conversion window]:** il numero di giorni dopo i quali si è verificato un clic su un annuncio in cui il clic può essere attribuito a una conversione. Il valore predefinito è 30 giorni.
         * **[!UICONTROL Notes]:** (facoltativo) descrizione o altre informazioni sul pixel.
      1. Fare clic su **[!UICONTROL Create and attach]**.
      1. Implementa il pixel di conversione sulle pagine web pertinenti:
         1. Nel menu principale, vai a **[!UICONTROL Resources]** > **[!UICONTROL Conversion pixels]**.
         1. Nella riga pixel, fare clic su **[!UICONTROL edit]**.
         1. Copiare i valori nei campi [!UICONTROL HTML Tag] e [!UICONTROL Flash Tag], in base alle esigenze, da fornire all&#39;inserzionista o al contatto del sito Web.

            Il reparto IT dell’inserzionista o un altro gruppo potrebbe dover pianificare la distribuzione dei tag o esserne informato.
   1. Fare clic su **[!UICONTROL Save]**.

**[!UICONTROL 3rd-party Fees]:** (facoltativo) tariffa statica di terze parti da registrare come costo non fatturabile per 1000 impression. Il valore predefinito a livello di pacchetto viene applicato automaticamente per i nuovi posizionamenti, se applicabile, a meno che non si immetta un valore diverso.

>[!NOTE]
>
>Le tariffe fatturabili si riflettono nella metrica [!UICONTROL Net CPM].

>[!MORELIKETHIS]
>
>* [Informazioni sulla gestione del posizionamento](placement-about.md)
>* [Crea un posizionamento](placement-create.md)
>* [Modifica posizionamenti](placement-edit.md)
>* [Gestire i moltiplicatori delle offerte per i posizionamenti](placement-manage-bid-multipliers.md)
>* [Visualizza il log delle modifiche per un posizionamento](placement-change-log.md)
>* [Scelte rapide da tastiera](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [Domande frequenti su Campaign Management](/help/dsp/campaign-management/faq-campaign-management.md)
