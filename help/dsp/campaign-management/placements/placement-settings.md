---
title: Impostazioni di posizionamento
description: Consulta le descrizioni delle impostazioni di posizionamento disponibili.
feature: DSP Placements
exl-id: 5b2574be-5d08-4cf7-910e-deac48d7e035
source-git-commit: 0836206b41789749a92bd9557a984896e710ec3a
workflow-type: tm+mt
source-wordcount: '3433'
ht-degree: 0%

---

# Impostazioni di posizionamento

## [!UICONTROL Basics]

**[!UICONTROL Placement name]** Il nome del posizionamento.

>[!TIP]
>Utilizza una convenzione di denominazione appropriata per la tua situazione. Una convenzione di denominazione suggerita è &quot;*\&lt;campaign name=&quot;&quot;>: \&lt;ad unit=&quot;&quot;>: \&lt;duration>: \&lt;targeting>*.&quot;

**[!UICONTROL Status]:** Lo stato del posizionamento: *[!UICONTROL Active]* (impostazione predefinita) oppure *[!UICONTROL Paused]*.

>[!TIP]
>La best practice prevede di mettere in pausa il posizionamento fino a quando non sei pronto per avviarlo.

**[!UICONTROL Details]:** (Sola lettura) Il tipo di annuncio applicabile, l’account che sta creando o creando il posizionamento e la campagna principale. Per visualizzare ulteriori dettagli, fai clic su **[!UICONTROL Show more]**.

**[!UICONTROL Templates]:** Apre un elenco di modelli di posizionamento esistenti. Per popolare automaticamente le impostazioni di targeting da un modello:

1. Effettuare una delle seguenti operazioni:

   * Per riutilizzare tutti gli oggetti di un modello, selezionare la casella di controllo accanto al nome del modello.

   * Per riutilizzare singoli tipi di oggetto da un modello, espandere il nome del modello e selezionare la casella di controllo accanto ai tipi di oggetto che si desidera riutilizzare.

1. Clic **[!UICONTROL Apply]**.

**[!UICONTROL Ad specs for forecast]:** (Solo per formati di annunci video) La durata e/o le specifiche dell’annuncio, utilizzate per calcolare la proiezione di previsione a destra. I campi variano in base al tipo di annuncio.

**[!UICONTROL Environment]:** (Solo per formato annuncio video universale) Gli ambienti del dispositivo (Desktop, Dispositivi mobili, TV connessa) da includere come destinazioni nel posizionamento. Specificane almeno uno.

Nei rapporti personalizzati, la dimensione a livello di posizionamento &quot;Ambiente dispositivo&quot; indica l’ambiente di destinazione.

**[!UICONTROL Placement tags]:** (Facoltativo) Parole chiave o nomi alternativi per individuare questo posizionamento.

## Obiettivi

**[!UICONTROL Package]:** (Facoltativo) Un pacchetto a cui è assegnato il posizionamento. Clic ![Modifica](/help/dsp/assets/edit.png) per selezionare un pacchetto esistente o crearne uno nuovo. Quando si assegna il posizionamento a un pacchetto, [!UICONTROL Goals] La sezione viene aggiornata con le date di volo, l’obiettivo di consegna e il budget del pacchetto.

**[!UICONTROL Flight Dates]:** La data di inizio e la data di fine del posizionamento. Gli annunci approvati possono essere eseguiti durante il volo quando il posizionamento è attivo e assegnato a un pacchetto o a una campagna attiva.

Le date del pacchetto (se applicabile) o della campagna vengono compilate automaticamente per impostazione predefinita.

>[!NOTE]
>
>* Le date di volo devono essere incluse nelle date di volo della campagna e nelle date di volo del pacchetto.


### Posizionamenti assegnati a pacchetti con velocità a livello di pacchetto

**[!UICONTROL Placement Funding]:** Come preventivare il posizionamento:

* *[!UICONTROL Optimize based on performance]:* Controlla il budget a livello di pacchetto.
* *[!UICONTROL Set a fixed budget cap]:* Consente di impostare un budget di posizionamento giornaliero, settimanale, mensile o all-time. Immetti un valore e la durata (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

**[!UICONTROL Max Bid]:** Il massimo per pagare 1000 impression.

**[!UICONTROL Placement Pre-bid Filters]:** Fino a cinque soglie per i KPI (ad esempio una metrica minima di visualizzabilità o un tasso di click-through) che devono essere raggiunte affinché l’offerta si verifichi. Puoi utilizzare i filtri di pre-offerta come tattiche di ottimizzazione, ma assicurati che ogni regola possa limitare le opportunità su cui questo posizionamento può fare offerte. Per aggiungere o modificare i filtri:

1. Clic ![Modifica](/help/dsp/assets/edit.png).
1. Effettuare una delle seguenti operazioni:
   * Per aggiungere un filtro:
      1. Clic **[!UICONTROL Add Filter]**.
      1. Accanto a **[!UICONTROL Only bid if]**, seleziona una metrica e quindi inserisci un valore.
   * Per rimuovere un filtro, fai clic su **[!UICONTROL X]** nella riga del filtro.
1. Clic **[!UICONTROL Save]**.

Vedi le descrizioni di ciascun filtro pre-offerta all’indirizzo &quot;[Filtri pre-offerta a livello di posizionamento e come utilizzarli](/help/dsp/optimization/optimization-pre-bid-filters.md).&quot;

### Tutti gli altri posizionamenti

**[!UICONTROL Budget Goal]:** Limite di budget lordo e intervallo di budget (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

**[!UICONTROL Gross Budget Goal]:** (Posizionamenti solo in campagne con gestione dei margini) Limite di budget lordo e intervallo di budget (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

**[!UICONTROL Optimization Goal]:**  L’obiettivo di ottimizzazione per il pacchetto. Vedi la descrizione di ciascun obiettivo di ottimizzazione in &quot;[Obiettivi di ottimizzazione e modalità di utilizzo](/help/dsp/optimization/optimization-goals.md)&quot;.

**[!UICONTROL Target Goal]:** L’obiettivo target, che viene utilizzato per monitorare le prestazioni.

>[!NOTE]
>
>Questo campo è solo un valore di riferimento e non viene utilizzato per le decisioni.

**[!UICONTROL Pace on]:** Su quale ritmo si baserà:

* **[!UICONTROL Budget goal]:** Impostazione predefinita. Questa opzione fornisce il maggior numero di impression possibile nel budget assegnato.

* **[!UICONTROL Impressions]:** Questa opzione fornisce le impression fino al raggiungimento di una quantità specificata entro un intervallo specificato. Quando selezioni questa opzione, specifica il numero di impression e l’intervallo: *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* o *[!UICONTROL Weekly]*.

**[!UICONTROL Max Bid]:** Il massimo per pagare 1000 impression.

**[!UICONTROL Flight pacing]:** (Solo posizionamenti con velocità a livello di posizionamento) Come regolare il ritmo di distribuzione degli annunci:

* *[!UICONTROL Even]:* (Impostazione predefinita) La consegna avviene in modo uniforme per ogni volo, con un obiettivo del 50% della consegna nella prima metà del volo.

* *[!UICONTROL Slightly Ahead]:* (Impostazione predefinita) Accelera la consegna in modo che sia completa al 55-65% a metà della durata del volo.

* *[!UICONTROL Frontload]:* Accelera la consegna in modo che sia completa al 65-75% a metà del volo.

* *[!UICONTROL Aggressive Frontload]:* Accelera la consegna in modo che sia completa al 75-85% a metà del volo.

**[!UICONTROL Intraday pacing]:** (Solo posizionamenti con velocità a livello di posizionamento) Come pianificare e consegnare ogni giorno all’interno del volo:

* *[!UICONTROL Even]:* (Impostazione predefinita) Ridimensiona la consegna in base alla disponibilità dell’inventario. In genere, vengono consegnati più annunci all’ora di giorno, quando il volume dell’asta è più alto e vengono consegnati meno annunci al mattino e alla sera.

* *[!UICONTROL ASAP]:* (Impostazione predefinita) Accelera la consegna a una velocità doppia rispetto a *Uniforme*.

   >[!CAUTION]
   >
   >Questa opzione può influire negativamente sulle prestazioni. Utilizzalo solo quando assegni la massima priorità alla consegna e spendi oltre l’ottimizzazione delle prestazioni.

**[!UICONTROL Placement Pre-bid Filters]:** (Facoltativo) Fino a cinque filtri che devono essere soddisfatti perché l’offerta si verifichi. Puoi utilizzare i filtri di pre-offerta come tattiche di ottimizzazione, ma tieni presente che ogni regola può limitare le opportunità su cui questo posizionamento può fare offerte. Per aggiungere o modificare i filtri:

1. Clic ![Modifica](/help/dsp/assets/edit.png).
1. Effettuare una delle seguenti operazioni:
   * Per aggiungere un filtro:
      1. Clic **[!UICONTROL Add Filter]**.
      1. Accanto a **[!UICONTROL Only bid if]**, seleziona una metrica e quindi inserisci un valore.
   * Per rimuovere un filtro, fai clic su **[!UICONTROL X]** nella riga del filtro.
1. Clic **[!UICONTROL Save]**.

## [!UICONTROL Geo-Targeting]

**[!UICONTROL Audience Location]:** (Facoltativo) Posizioni specifiche in cui includere o escludere annunci nel posizionamento. Se non specifichi alcuna posizione, viene eseguito il targeting di tutte le posizioni.

>[!NOTE]
>
>Le posizioni Città e DMA non sono disponibili per i posizionamenti Roku.

Per specificare le posizioni:

1. Clic ![Modifica](/help/dsp/assets/edit.png).
1. Effettua una delle seguenti operazioni:
   * Per includere o escludere un paese, uno stato, una città, un DMA, un distretto legislativo federale o un distretto legislativo statale:
      1. Seleziona il tipo di posizione nella colonna a sinistra.
      1. (Se necessario) Fai clic su una posizione per espanderla.
      1. Accanto alla posizione, fai clic su *[!UICONTROL Include]* per includerlo come destinazione o *[!UICONTROL Exclude]* per escluderlo come destinazione.
   * Per cercare un codice postale e includere o escludere tutti i risultati selezionati:
      1. Clic **[!UICONTROL Search Postal Code]**.
      1. Seleziona il paese.
      1. Immettere il nome della città, quindi fare clic su ![Modifica](/help/dsp/assets/search.png).
      1. Fare clic sul risultato di ricerca corretto.
      1. Clic *[!UICONTROL Include All]* per includere tutte le posizioni come destinazioni o *[!UICONTROL Exclude All]* per escludere tutte le posizioni come destinazioni.
   * Per inserire o incollare codici postali e includerli o escluderli tutti:
      1. Clic **[!UICONTROL Paste Postal Code]**.
      1. Seleziona il paese.
      1. Inserisci o incolla fino a 1000 codici postali.
Includere un codice postale per riga oppure immettere più valori separati da virgole o tabulazioni.
      1. Clic *[!UICONTROL Include All]* per includere tutte le posizioni come destinazioni o *[!UICONTROL Exclude All]* per escludere tutte le posizioni come destinazioni.
   * Per rimuovere una posizione dal [!UICONTROL Included] o [!UICONTROL Excluded] , fare clic su **[!UICONTROL X]** accanto alla posizione nella colonna di destra.
1. Clic **[!UICONTROL Done]**.

>[!NOTE]
>
>* Non tutti i paesi dispongono di località con codice postale, Stato o Città.
>* DMA (area di mercato designata), Federal Legislative Districts e State Legislative Districts sono disponibili solo per le sedi degli Stati Uniti.


## [!UICONTROL Inventory Targeting]

**[!UICONTROL Inventory Sources]:** Origini di magazzino da includere o escludere come destinazioni. Per la maggior parte dei tipi di posizionamento, tutti i tipi di inventario e tutte le origini per ciascun tipo sono inclusi per impostazione predefinita. Per [!DNL Roku] posizionamenti, è necessario specificare il tipo di inventario e le origini. È possibile scegliere tra i seguenti tipi di inventario:

* [!UICONTROL Public]: (Tutti i tipi di posizionamento ad eccezione di Roku) Tutti gli inventari a cambio aperto a cui l’DSP ha accesso. Puoi includere ed escludere l’inventario pubblico.

   È possibile visualizzare l’elenco in base all’origine o al feed. Quando visualizzi l’elenco per feed, puoi eseguire ricerche per nome di feed, chiave di feed o un tag di caratteristica selezionato.

* [!UICONTROL Private] | [!UICONTROL Roku Private]: le offerte private esistenti (o private esistenti [!DNL Roku] offerte per [!DNL Roku] posizionamenti) con gli editori configurati in DSP. È possibile includere ma non escludere l&#39;inventario pubblico.

   Puoi cercare l’elenco per parola chiave, chiave, ID offerta o tag personalizzato.

* [!UICONTROL On Demand] | [!UICONTROL Roku On Demand]: tutto [premium, non garantito [!UICONTROL On Demand] inventario](/help/dsp/inventory/on-demand-inventory-about.md) (o [!UICONTROL On Demand] [!DNL Roku] offerte per [!DNL Roku] ai quali ti sei iscritto/a [!DNL DSP]. Puoi includere ed escludere [!UICONTROL On Demand] inventario.

   È possibile visualizzare l’elenco in base all’origine o al feed. Quando l&#39;elenco viene visualizzato per feed, è possibile eseguire ricerche per nome di feed, chiave di feed oppure per l&#39;area dell&#39;editore selezionata, il tag categoria o il tag caratteristica.

Per specificare il targeting dell&#39;inventario:

* Per escludere un tipo di inventario, deselezionare la casella di controllo accanto al nome.
* Per eseguire il targeting di un tipo di inventario:
   1. Selezionare la casella di controllo accanto al nome del tipo di inventario.
   1. (Facoltativo) Modifica le origini per includere:
      1. Clic ![Modifica](/help/dsp/assets/edit.png).
      1. ([!UICONTROL Public] e [!UICONTROL On Demand] inventory) Fai clic su **[!UICONTROL View by Source]** o **[!UICONTROL View by Feed]** per modificare l&#39;elenco delle origini.
      1. (Se applicabile) Filtra l’inventario in base alle esigenze.
      1. Specificare le origini da includere ed escludere:
         * Per includere una [!UICONTROL Public] o [!UICONTROL On Demand] sorgente, fai clic su **[!UICONTROL Include]** accanto al nome dell&#39;origine.
         * Da includere [!UICONTROL Private] origini:
            * Per includere tutte le scorte in un&#39;offerta, fare clic su **[!UICONTROL Include all]** accanto al nome dell’offerta.
            * Per includere una singola origine di magazzino, espandere il nome dell&#39;offerta e quindi fare clic sulla casella di controllo accanto al nome dell&#39;origine.
         * Per escludere un [!UICONTROL Public] o [!UICONTROL On source], fai clic su **[!UICONTROL Exclude]** accanto al nome dell&#39;origine.
   1. (Facoltativo) Per scaricare un file CSV con le informazioni di targeting nella posizione Download del browser, fai clic su **[!UICONTROL Save & Export]**.
   1. Clic **[!UICONTROL Save]**.

>[!TIP]
>
>Se ti sei iscritto a [!UICONTROL On Demand] inventario ma non è possibile individuare gli editori o le offerte di destinazione, quindi controllare lo stato delle offerte. Per ulteriori informazioni sugli stati, consulta [Informazioni su [!DNL On Demand] Magazzino Premium](/help/dsp/inventory/on-demand-inventory-about.md).

**[!UICONTROL Exclude out-stream]:** (Solo posizionamenti video) Esclude il traffico in uscita.

Gli annunci in uscita vengono solitamente visualizzati sul contenuto come pop-up o inseriti nel contenuto (nell’esperienza nativa), anziché come annunci video regolari in un lettore video.

## [!UICONTROL Site Targeting]

**[!UICONTROL Traffic type]:** Tipi di traffico di destinazione. Le opzioni includono **[!UICONTROL Websites]** e **[!UICONTROL Apps]**.

**[!UICONTROL Site tier]:** (disponibile quando **[!UICONTROL Paste list of targeted sites]** è *[!UICONTROL Off]*) La qualità dei siti di destinazione. I livelli 1-3 sono tutti brand safe e sono stati esaminati e approvati dal team di mappatura DSP.

* *[!UICONTROL Tier 1]:* Siti e applicazioni Premium riconoscibili a livello nazionale.
* *[!UICONTROL Tier 2]:* Obiettivi Tier 1 e siti e applicazioni di qualità meno conosciuti rispetto al Tier 1.
* *[!UICONTROL Tier 3]:* Targeting dei livelli 1-2 e dei siti e delle applicazioni legittimi e sicuri per il brand adatti a un pubblico di nicchia. Utilizza il livello 3 per le compravendite con targeting di dati o portata.
* *[!UICONTROL All Sites]:* Target Livelli 1-3 e nuovo inventario che non è stato selezionato o classificato, che puoi utilizzare per la portata.

>[!NOTE]
>
>L’inventario è specifico per le unità pubblicitarie nel posizionamento.

>[!TIP]
>
>Per le campagne sulle prestazioni, la best practice prevede di selezionare *[!UICONTROL All Sites]*.

**[!UICONTROL Site Categories]:** (Facoltativo; disponibile quando **[!UICONTROL Paste list of targeted sites]** è *[!UICONTROL Off]*) Le categorie del sito all&#39;interno dei livelli del sito selezionati da includere o escludere (ma non entrambi) come destinazioni. Scegli da elenchi di siti verticali che l&#39;DSP ha mappato in base all&#39;oggetto del sito:

1. Clic ![Modifica](/help/dsp/assets/edit.png).
1. Specificare le categorie del sito da includere o escludere:
   * Per includere le categorie del sito:
      1. Clic **[!UICONTROL Include categories]**.
      1. Selezionare la casella di controllo accanto a ogni categoria di destinazione.
   * Per escludere le categorie di siti:
      1. Clic **[!UICONTROL Exclude categories]**.
      1. Selezionare la casella di controllo accanto a ogni categoria da escludere.
1. (Facoltativo) Per scaricare un file CSV con le informazioni di targeting nella posizione Download del browser, fai clic su **[!UICONTROL Export]**.
1. Clic **[!UICONTROL Save]**.

**[!UICONTROL Exclude Sites]:** (Facoltativo; disponibile quando **[!UICONTROL Paste list of targeted sites]** è *[!UICONTROL Off]*) Siti da escludere. È possibile cercare e selezionare i siti oppure immettere o incollare i nomi di dominio:

1. Clic ![Modifica](/help/dsp/assets/edit.png).
1. Specificare i siti:
   * Per cercare un sito:
      1. Clic **[!UICONTROL Search]**.
      1. Immettere una parola chiave, selezionare un livello del sito e/o selezionare una categoria del sito.
      1. Nei risultati della ricerca, seleziona i siti da escludere:
         * Per escludere un singolo sito, selezionare la relativa casella di controllo.
         * (Quando sono disponibili più di 50 risultati) Per escludere i primi 50 risultati, fai clic su **[!UICONTROL Exclude these 50]**. Per escludere tutti i risultati della ricerca, fare clic su **[!UICONTROL Exclude these \<*NN *\>]**.
   * Per immettere i nomi di dominio:
      1. Clic **[!UICONTROL Paste]**.
      1. Immetti uno o più nomi di dominio su righe separate.
      1. Clic **[!UICONTROL Exclude All]**.
1. Clic **[!UICONTROL Done]** quando hai finito.

>[!NOTE]
>
>* Oltre all’DSP, vengono applicati anche elenchi di siti bloccati a livello di account e di inserzionista [elenco siti bloccati a livello globale](/help/dsp/introduction/features/brand-safety-media-quality.md), che include i siti ritenuti non sicuri per gli annunci.
>* Gli elenchi Siti bloccati sostituiscono sempre gli elenchi Siti di destinazione. Se un posizionamento esclude e include lo stesso target per un annuncio, il target viene escluso.


**[!UICONTROL Language]:** (Facoltativo) Una singola lingua per il targeting.

**[!UICONTROL Site List Preview]:** (Sola lettura) Tutti i siti di destinazione e bloccati per il posizionamento.

Facoltativamente, puoi esportare l’elenco dei siti di destinazione e dei siti bloccati come file con valori separati da virgola (CSV). Per esportare l’elenco, fai clic su **[!UICONTROL Export full site list]**, quindi aprire o salvare il file in base alla normale procedura del browser.

**[!UICONTROL Allow unscreened sites]:** (Solo posizionamenti di visualizzazione standard) Abilita la consegna di annunci su siti non controllati. Quando il posizionamento ha come target l’inventario privato, questa opzione può distribuire annunci sui siti bloccati.

**[!UICONTROL Paste list of targeted sites]:** Consente di eseguire il targeting solo di siti specifici. Quando si attiva questa opzione, le altre opzioni di targeting del sito vengono disattivate.

**[!UICONTROL Sites]:** (disponibile quando **[!UICONTROL Paste list of targeted sites]** è *[!UICONTROL On]* a) Siti di destinazione. È possibile cercare e selezionare i siti oppure immettere o incollare i nomi di dominio:

1. Clic ![Modifica](/help/dsp/assets/edit.png).
1. Specificare i siti:
   * Per cercare un sito:
      1. Clic **[!UICONTROL Search]**.
      1. Immettere una parola chiave, selezionare un livello del sito e/o selezionare una categoria del sito.
      1. Nei risultati della ricerca, selezionare i siti da includere:
         * Per escludere un singolo sito, selezionare la relativa casella di controllo.
         * (Quando sono disponibili più di 50 risultati) Per includere i primi 50 risultati, fai clic su **[!UICONTROL Include these 50]**. Per includere tutti i risultati della ricerca, fare clic su **[!UICONTROL Include these \<*NN *\>]**.
   * Per immettere i nomi di dominio:
      1. click **[!UICONTROL Paste]**.
      1. Immetti uno o più nomi di dominio su righe separate.
      1. Clic **[!UICONTROL Include All]**.
1. Clic **[!UICONTROL Done]**.

## [!UICONTROL Audience Targeting]

**[!UICONTROL Included Audiences]:** Qualsiasi target di pubblico per il posizionamento, tra cui [segmenti di terze parti, segmenti di prime parti, segmenti di Adobe, segmenti personalizzati e tipi di pubblico salvati](/help/dsp/audiences/audience-settings.md). Vengono visualizzate anche le dimensioni del pubblico deduplicato totale e attivo per tutti i segmenti selezionati e i tipi di pubblico salvati. Puoi selezionare un pubblico esistente, crearne uno nuovo da riutilizzare in un secondo momento o selezionare segmenti di pubblico specifici:

* Per selezionare un pubblico esistente, fai clic su ![Seleziona](/help/dsp/assets/chevron-down.png) accanto a [!UICONTROL Included Audiences], quindi seleziona il pubblico.
* Per creare un nuovo pubblico, fai clic su ![Seleziona](/help/dsp/assets/chevron-down.png) accanto a [!UICONTROL Included Audiences], quindi selezionare **[!UICONTROL + Create Audience]**. Per istruzioni, consulta [Creare un pubblico riutilizzabile](/help/dsp/audiences/reusable-audience-create.md), a partire dal passaggio 3.
* Per selezionare segmenti di pubblico specifici, fai clic su **[!UICONTROL Select segments for this placement only]**. Seleziona la logica del segmento; per le istruzioni consulta il passaggio 6 in &quot;[Creare un pubblico riutilizzabile](/help/dsp/audiences/reusable-audience-create.md).&quot; Al termine, fai clic su **Salva**.

**[!UICONTROL Excluded Audiences]:** Qualsiasi pubblico da escludere per il posizionamento, compresi i tipi di pubblico con [segmenti di terze parti, segmenti di prime parti, segmenti di Adobe, segmenti personalizzati e tipi di pubblico salvati](/help/dsp/audiences/audience-settings.md). Viene visualizzata anche la dimensione totale e attiva del pubblico deduplicato in tutti i tipi di pubblico esclusi. Puoi selezionare un pubblico esistente o crearne uno nuovo da riutilizzare in un secondo momento:

* Per selezionare un pubblico esistente, fai clic su ![Seleziona](/help/dsp/assets/chevron-down.png) accanto a [!UICONTROL Excluded Audiences], quindi seleziona il pubblico.
* Per creare un nuovo pubblico, fai clic su ![Seleziona](/help/dsp/assets/chevron-down.png) accanto a [!UICONTROL Excluded Audiences], quindi selezionare **+ Crea pubblico**. Per istruzioni, consulta [Creare un pubblico riutilizzabile](/help/dsp/audiences/reusable-audience-create.md), a partire dal passaggio 3.

**[!UICONTROL Cross Device Targeting]:** (Disponibile quando selezioni almeno un segmento o un pubblico e il [campaign è configurato per il targeting multi-dispositivo basato sulle persone](/help/dsp/campaign-management/campaigns/campaign-settings.md). Consente di estendere il targeting su tutti i dispositivi noti di una persona (in base al grafico dei dispositivi specificato nelle impostazioni della campagna), anche su dispositivi che non si trovano nei segmenti specificati. Le tariffe possono essere applicate a seconda del grafico specificato per la campagna. I dati del grafico dei dispositivi sono attualmente disponibili solo in Nord America.

**[!UICONTROL Placement Cap]:** (Facoltativo) Il numero di volte in cui un dispositivo o una persona univoca (a seconda del [!UICONTROL Cross Device Level] per la campagna) verranno serviti annunci dal posizionamento. Le opzioni includono *[!UICONTROL Unlimited]* o un importo specifico per giorno, settimana o mese.

>[!NOTE]
>
> Puoi impostare i limiti di frequenza a livello di campagna, pacchetto e posizionamento. L’DSP rispetterà il limite di frequenza più rigoroso nella gerarchia della campagna.

**[!UICONTROL Secondary Cap]:** (Facoltativo; disponibile quando si include un valore numerico [!UICONTROL Placement Cap]) Limitazione aggiuntiva entro i limiti del cappuccio di posizionamento principale. Seleziona il numero di impression e il periodo di tempo (ad esempio 3 ogni 12 ore).

**[!UICONTROL Day Parting]:** (Facoltativo) Giorni specifici della settimana e ora del giorno in cui gli annunci possono essere eseguiti. Per specificare gli intervalli di partenze diurne:

1. Clic ![Modifica](/help/dsp/assets/edit.png).
1. Seleziona il fuso orario applicabile.
1. Specifica gli intervalli:
   * Per selezionare un intervallo predefinito, fare clic su uno dei pulsanti di intervallo. Le opzioni includono *[!UICONTROL Weekends]**, *[!UICONTROL Weekdays]*, *[!UICONTROL Morning]*, *[!UICONTROL Lunch]*, *[!UICONTROL Dinner]*, o *[!UICONTROL Prime]* (primetime).
   * Per selezionare manualmente un intervallo, fare clic all&#39;interno di una cella e, facoltativamente, trascinare per selezionare l&#39;intervallo.
1. Clic **[!UICONTROL Save]**.

**[!UICONTROL Topic Targeting]:** (Facoltativo; disponibile per gli inserzionisti configurati con [!DNL Comscore] e [!DNL Grapeshot] segmenti) Nomi di segmenti specifici o ID da [!DNL Comscore] e [!DNL Grapeshot] da includere come target. Per questa funzione potrebbero essere applicati costi aggiuntivi. Per attivare questa funzione e impostare i segmenti di argomento, contatta il team dell’account di Adobe.

Per specificare il targeting degli argomenti:

1. Clic ![Modifica](/help/dsp/assets/edit.png).
1. Specifica i segmenti di destinazione:
   1. Nella colonna sinistra, seleziona il partner (*[!UICONTROL Comscore]* o *[!UICONTROL Grapeshot]*).
   1. Nel campo di immissione, inserisci i nomi o gli ID del segmento.
1. (Facoltativo) Per scaricare un file CSV con le informazioni dell&#39;argomento nella posizione Download del browser, fai clic su **[!UICONTROL Export]**.
1. Clic **[!UICONTROL Save]**.

>[!TIP]
>
>* Il targeting degli argomenti limita l’inventario su cui il posizionamento può fare offerte, quindi utilizza il targeting degli argomenti solo per una piccola percentuale dell’acquisto complessivo.
>
>* Imposta eventuali targeting negativi all’interno del segmento su [!DNL Comscore] o [!DNL Grapeshot].


**[!UICONTROL Device Targeting]:** (Facoltativo) Informazioni specifiche sul dispositivo, inclusi tipi di dispositivo, produttori, sistemi operativi, browser e tipi di connettività, da includere ed escludere come destinazioni. Per specificare il targeting del dispositivo:

1. Clic ![Modifica](/help/dsp/assets/edit.png).
1. Specifica i dettagli del dispositivo da includere ed escludere:
   1. Nella colonna sinistra selezionare la categoria.
   1. Specifica destinazione:
      * Per includere un valore, fai clic su **[!UICONTROL Include]** accanto al nome del valore.
      * Per escludere un valore, fai clic su **[!UICONTROL Exclude]** accanto al nome del valore.
1. (Facoltativo) Per scaricare un file CSV con le informazioni di targeting del dispositivo nella posizione Download del browser, fai clic su **[!UICONTROL Export]**.
1. Clic **[!UICONTROL Save]**.

**[!UICONTROL ISP Targeting]:** (Facoltativo) Specifici fornitori di servizi Internet (ISP) da includere o escludere (ma non entrambi) come destinatari. Per specificare il targeting ISP:

1. Clic ![Modifica](/help/dsp/assets/edit.png).
1. Specifica gli ISP da includere o escludere:
   * Per includere gli ISP:
      1. Clic **[!UICONTROL Include ISPs]**.
      1. (Facoltativo) Filtra l’elenco per parola chiave.
      1. Selezionare la casella di controllo accanto a ogni ISP di destinazione.
   * Per escludere gli ISP:
      1. Clic **[!UICONTROL Exclude ISPs]**.
      1. (Facoltativo) Filtra l’elenco per parola chiave.
      1. Selezionare la casella di controllo accanto a ogni ISP da escludere.
1. (Facoltativo) Per scaricare un file CSV con le informazioni di targeting dell&#39;ISP nella posizione Download del browser in uso, fai clic su **[!UICONTROL Export]**.
1. Clic **[!UICONTROL Save]**.

## [!UICONTROL Brand Safety and Media Targeting]

**[!UICONTROL Contextual filtering]:** Tipi di [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], e [!DNL Peer39] filtri contestuali da applicare. Le impostazioni predefinite a livello di inserzionista vengono selezionate per i nuovi posizionamenti, ma è possibile modificare le impostazioni:

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block sites that are]:** (Facoltativo) Uno o più tipi di contesto di magazzino da bloccare per impostazione predefinita. Possono essere applicate tariffe aggiuntive.

* [!UICONTROL Peer 39]:

   * **Siti target che sono:** (Facoltativo) Uno o più tipi di attributi di inventario da impostare come destinazione per impostazione predefinita. Possono essere applicate tariffe aggiuntive.

* [!UICONTROL ComScore]:

   * **Blocca siti:** (Facoltativo) Uno o più tipi di attributi di inventario da bloccare per impostazione predefinita. Possono essere applicate tariffe aggiuntive.

* [!UICONTROL Integral Ad Science]

   * **[!UICONTROL Adult Content]:** (Facoltativo) Il grado di contenuto per adulti per cui bloccare gli annunci per impostazione predefinita: *[!UICONTROL Do Not Block]* (impostazione predefinita), *[!UICONTROL Standard]*, o *[!UICONTROL Strict]*. Possono essere applicate tariffe aggiuntive.

   * **[!UICONTROL Alcohol Content]:** (Facoltativo) Il grado di contenuto alcolico per il quale bloccare gli annunci per impostazione predefinita: *[!UICONTROL Do Not Block]* (impostazione predefinita), *[!UICONTROL Standard]*, o *[!UICONTROL Strict]*. Possono essere applicate tariffe aggiuntive.

**[!UICONTROL Pre-bid fraud blocking]:** Tipi di siti da bloccare in base al traffico fraudolento e alle attività sospette misurate tramite [!DNL DoubleVerify], [!DNL Integral Ad Science], e [!DNL Peer39]. Le impostazioni predefinite a livello di inserzionista vengono selezionate per i nuovi posizionamenti, ma è possibile modificare le impostazioni:

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** Per impostazione predefinita, blocca tutto il traffico non valido al 100%, incluso il traffico sui dispositivi con evidenziazione, per i nuovi posizionamenti. Possono essere applicate tariffe aggiuntive.

   * **[!UICONTROL Also block sites with]:** (Facoltativo) Un livello aggiuntivo di frode e traffico non valido che causerà il blocco predefinito degli annunci da parte dell’DSP:  *[!UICONTROL None]* (impostazione predefinita, che non blocca il traffico aggiuntivo), *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*, *[!UICONTROL >4% Average Fraud/IVT levels]*, *[!UICONTROL >6% Average Fraud/IVT levels]*, *[!UICONTROL >10% Average Fraud/IVT levels]*, o *[!UICONTROL >25% Average Fraud/IVT levels]*. Possono essere applicate tariffe aggiuntive.

* [!UICONTROL Peer 39]:

   * **[!UICONTROL Block sites that are]:** (Facoltativo) Uno o più tipi di frode che causeranno il blocco predefinito degli annunci da parte dell’DSP: *[!UICONTROL Fraud]* (che blocca tutti i siti con frodi), *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]*, e/o *[!UICONTROL Fraud: Zero Ads]*. Possono essere applicate tariffe aggiuntive.

* [!UICONTROL Integral Ad Science]:

   * **[!UICONTROL Block sites that are]:** (Facoltativo) Un tipo di attività sospetta su siti web o app che causerà il blocco predefinito degli annunci da parte dell’DSP: *[!UICONTROL None]* (impostazione predefinita, che non blocca gli annunci basati su attività sospette), *[!UICONTROL Suspicious Activity - High Risk]*, o *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. Possono essere applicate tariffe aggiuntive.

**[!UICONTROL Ads.txt filtering]:**

Quale livello di [Ads.txt](https://iabtechlab.com/ads-txt-about/) filtro pre-offerta da utilizzare sfruttando l’elenco di venditori digitali autorizzati di ogni editore. Il valore predefinito a livello di inserzionista viene selezionato per i nuovi posizionamenti, ma è possibile modificare le impostazioni:

* *[!UICONTROL Opt out of ads.txt (default)]*: per acquistare le scorte da tutti i venditori.
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*: per dare la priorità all’acquisto delle scorte dai venditori e rivenditori diretti autorizzati di un dominio.
* *[!UICONTROL Ads.txt sellers only]*: per acquistare le scorte solo dai venditori e rivenditori diretti autorizzati di un dominio.
* *[!UICONTROL Ads.txt sellers only]*: per acquistare le scorte solo dai venditori diretti autorizzati di un dominio.

**[!UICONTROL DoubleVerify Authentic Brand Safety]:** (Per gli inserzionisti configurati con [!UICONTROL DoubleVerify Authentic Brand Safety] opzione) Abilita [!DNL DoubleVerify Authentic Brand Safety], che blocca le impression dopo l’offerta utilizzando le regole di sicurezza del brand personalizzate configurate per l’ID segmento specificato. L’DSP fattura il tuo account per l’utilizzo dell’ID segmento specificato nelle impostazioni dell’inserzionista.

## [!UICONTROL Tracking] {#placement-tracking}

>[!NOTE]
>
>([!DNL Roku] posizionamenti) Fornitori di tracciamento di terze parti approvati da [!DNL Roku] include [!DNL Acxiom], [!DNL comScore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk], e [!DNL Research Now].

**[!UICONTROL Event Pixels]:** (Facoltativo) Pixel di tracciamento degli eventi di terze parti che verranno allegati per impostazione predefinita a tutti i nuovi annunci nel posizionamento. Per specificare i pixel dell&#39;evento:

1. Clic ![Modifica](/help/dsp/assets/edit.png).
1. Effettua una delle seguenti operazioni:
   * Per selezionare un pixel esistente, selezionare la casella di controllo nella riga dei pixel.
   * Per creare un nuovo pixel:
      1. Clic **[!UICONTROL Create]**.
      1. Immettere le seguenti informazioni:
         * **[!UICONTROL Pixel name]:** Nome del pixel; la lunghezza massima è di 500 caratteri. Utilizza un nome che ti consenta di identificare facilmente il pixel.
         * **[!UICONTROL Pixel event fires on]:** L’evento che attiva il pixel da attivare. Gli eventi disponibili variano in base al tipo di annuncio.
         * **[!UICONTROL Pixel type]:** Se il pixel è un *[!UICONTROL IMG URL]* (file di immagine 1x1 pixel), *[!UICONTROL HTML]*, o *[!UICONTROL JavaScript URL]*.
         * **[!UICONTROL Pixel URL]:** URL dell&#39;immagine pixel.
      1. Clic **[!UICONTROL Create and attach]**.
   1. Clic **[!UICONTROL Save]**.

**[!UICONTROL Conversion Pixels]:** (Facoltativo) I pixel di tracciamento della conversione che verranno allegati per impostazione predefinita a tutti i nuovi annunci nel posizionamento. Per specificare i pixel di conversione:

1. Clic ![Modifica](/help/dsp/assets/edit.png).
1. Effettua una delle seguenti operazioni:
   * Per selezionare un pixel esistente, selezionare la casella di controllo nella riga dei pixel.
   * Per creare un nuovo pixel:
      1. Clic **[!UICONTROL Create]**.
      1. Immettere le seguenti informazioni:
         * **[!UICONTROL Conversion pixel name]:** Nome del pixel; la lunghezza massima è di 500 caratteri. Utilizza un nome che ti consenta di identificare facilmente il pixel.
         * **[!UICONTROL Conversion category]:** Tipo di conversione.
         * **[!UICONTROL Impression conversion window]:** Il numero di giorni dopo i quali si verifica un’impression pubblicitaria, in cui l’impression può essere attribuita a una conversione. Il valore predefinito è 30 giorni.
         * **[!UICONTROL Click conversion window]:** Il numero di giorni dopo i quali si verifica un clic su un annuncio in cui il clic può essere attribuito a una conversione. Il valore predefinito è 30 giorni.
         * **[!UICONTROL Notes]:** (Facoltativo) Una descrizione o altre informazioni sul pixel.
      1. Clic **[!UICONTROL Create and attach]**.
      1. Implementa il pixel di conversione sulle pagine web pertinenti:
         1. Nel menu principale, vai a **[!UICONTROL Resources]** > **[!UICONTROL Conversion pixels]**.
         1. Nella riga pixel, fai clic su **[!UICONTROL edit]**.
         1. Copia i valori in [!UICONTROL HTML Tag] e [!UICONTROL Flash Tag] campi, se necessario, da fornire all’inserzionista o al contatto con il sito web.

            Il reparto IT dell’inserzionista o un altro gruppo potrebbe dover pianificare la distribuzione dei tag o esserne informato.
   1. Clic **[!UICONTROL Save]**.

**[!UICONTROL 3rd-party Fees]:** (Facoltativo) Tariffa statica di terze parti da tracciare come costo non fatturabile per 1000 impression. Il valore predefinito a livello di pacchetto viene applicato automaticamente per i nuovi posizionamenti, se applicabile, a meno che non si immetta un valore diverso.

>[!NOTE]
>
>Le tariffe fatturabili vengono riportate nel [!UICONTROL Net CPM] metrica.

>[!MORELIKETHIS]
>
>* [Informazioni sulla gestione del posizionamento](placement-about.md)
>* [Creare un posizionamento](placement-create.md)
>* [Modificare un posizionamento](placement-edit.md)
>* [Visualizzare il log delle modifiche per un posizionamento](placement-change-log.md)
>* [Scelte rapide da tastiera](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [Domande frequenti su Campaign Management](/help/dsp/campaign-management/faq-campaign-management.md)

