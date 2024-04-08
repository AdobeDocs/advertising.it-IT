---
title: Impostazioni pacchetto
description: Consulta le descrizioni delle impostazioni disponibili per il pacchetto.
feature: DSP Packages
exl-id: 20ec5e8e-4980-4fa0-80c9-531f5b02c0f9
source-git-commit: 54e8dec0f31d1f18931d12d868ba162879a7acfb
workflow-type: tm+mt
source-wordcount: '959'
ht-degree: 0%

---

# Impostazioni pacchetto

## [!UICONTROL Basic Details]

**[!UICONTROL Name]:** Il nome del pacchetto. La lunghezza massima è di 60 caratteri.

**[!UICONTROL Description]:** (Facoltativo) Una descrizione del pacchetto.

**[!UICONTROL 3rd Party Billed Fees]:** (Facoltativo) Una tariffa statica di terze parti da tracciare come costo non fatturabile:

>[!NOTE]
>
>Le tariffe fatturabili vengono riportate nel [!UICONTROL Net CPM] metrica.
>
* **[!UICONTROL CPM]:** Il costo per 1000 impression (CPM).

* **[!UICONTROL CPM Description]:** Descrizione della tariffa CPM.

È possibile sovrascrivere l’impostazione a livello di pacchetto in corrispondenza di [livello di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md).

## [!UICONTROL Goals & Budget]

**[!UICONTROL Pacing & Capping]:** (Sola lettura per i pacchetti esistenti) A quale livello posizionare e limitare i posizionamenti nel pacchetto:

* **[!UICONTROL Package level pacing]:** Questa strategia di andamento funziona calcolando il ritmo e riducendo tutti i posizionamenti inclusi come una *gruppo*. Questa strategia assicura che tutti i posizionamenti all’interno di un determinato pacchetto siano ottimizzati in modo olistico, distribuendo la spesa in base alle prestazioni e alla scalabilità a specifici indicatori di prestazioni chiave (KPI, Key Performance Indicator).

* **[!UICONTROL Placement level pacing]:**  Questa strategia di velocità funziona calcolando il ritmo e riducendo tutti i posizionamenti inclusi *singolarmente*. La best practice prevede di utilizzare questa strategia solo per eseguire transazioni garantite sul mercato privato.

**[!UICONTROL Flight Dates]:** La data di inizio e la data di fine del pacchetto.

Per creare voli non uniformi per il pacchetto, selezionare *[!UICONTROL *Activate Custom Flighting]** e impostare i voli personalizzati nel [!UICONTROL Flighting] sezione successiva. Una volta attivato il riflesso personalizzato e salvato il pacchetto, non è possibile disattivare il riflesso personalizzato.

>[!NOTE]
>
>* Le date del volo devono essere incluse nelle date del volo della campagna. Inoltre, le date di volo per tutti i posizionamenti assegnati a questo pacchetto devono essere incluse entro tali date.
> * Non puoi modificare la data di inizio del pacchetto quando viene attivato il riflesso personalizzato.

**[!UICONTROL Budget]:** (Solo pacchetti con velocità a livello di pacchetto) Limite di budget lordo e intervallo di budget.

Per i pacchetti con conflitti personalizzati, l&#39;intervallo di budget è sempre *[!UICONTROL All time]*. Per i pacchetti senza conflitti personalizzati, specifica l’intervallo di budget: *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* o *[!UICONTROL Weekly]*.

**[!UICONTROL Gross Budget]:** (Solo pacchetti con velocità a livello di pacchetto e gestione dinamica dei margini) Limite di budget lordo per la durata del pacchetto.

**[!UICONTROL Optimization Goal]:** (Solo pacchetti con velocità a livello di pacchetto) Obiettivo di ottimizzazione per il pacchetto. Vedi le descrizioni di ciascun obiettivo di ottimizzazione in [Obiettivi di ottimizzazione e modalità di utilizzo](/help/dsp/optimization/optimization-goals.md).

**[!UICONTROL Custom Goal for Model Learning]:** (Pacchetti con &quot;[!UICONTROL Highest Return on Ad Spend]&quot; e &quot;[!UICONTROL Lowest Cost per Acquisition]&quot; solo obiettivi di ottimizzazione) A [obiettivo personalizzato](/help/dsp/optimization/custom-goal.md) che include i ricavi o gli eventi di conversione utilizzati per calcolare la metrica CPA o ROAS. L’obiettivo personalizzato può facoltativamente includere eventi upper funnel ponderati aggiuntivi (come visite della pagina e aggiunte al carrello) da utilizzare in aggiunta alla metrica CPA o ROAS per l’ottimizzazione del pacchetto. Per ulteriori informazioni sulle best practice per obiettivi personalizzati e campagne che li utilizzano, consulta [Best practice per la creazione di un obiettivo personalizzato](/help/dsp/optimization/custom-goal.md#custom-goal-best-practices) e [Best practice per l’impostazione di campagne sulle prestazioni](/help/dsp/optimization/campaign-best-practices-performance.md).

**[!UICONTROL Consider Only Click Conversions for Model Learning]:** (Facoltativo; pacchetti con &quot;[!UICONTROL Highest Return on Ad Spend]&quot; e &quot;[!UICONTROL Lowest Cost per Acquisition]&quot;Solo obiettivi di ottimizzazione&quot; indica al modello di ottimizzazione di imparare solo dalle conversioni basate su clic. In caso contrario, il modello di ottimizzazione apprende sia dalle conversioni basate su clic che da quelle basate su impression.

**[!UICONTROL Conversion Metric]:** (Facoltativo; pacchetti con &quot;[!UICONTROL Highest Return on Ad Spend]&quot; e &quot;[!UICONTROL Lowest Cost per Acquisition]&quot;Solo obiettivi di ottimizzazione&quot;: l’evento di conversione finale (ad esempio le iscrizioni) o l’importo di evento di ricavo/vendita (ad esempio i valori di acquisto e di acquisto) da utilizzare per calcolare il ritorno sulla spesa pubblicitaria o il costo per acquisizione. Seleziona da un elenco di tutti gli eventi primari (&quot;metriche obiettivo&quot;) mappati all&#39;obiettivo personalizzato selezionato. Se l’elenco è vuoto, modifica l’obiettivo personalizzato in modo da includere almeno uno degli eventi sottostanti come metrica di obiettivo.

**[!UICONTROL Package Goal Type]:** (Solo pacchetti con obiettivi di ottimizzazione personalizzati) Scopo del pacchetto. Questa impostazione consente di determinare come ottimizzare il pacchetto:

* *[!UICONTROL Prospecting]:* I pacchetti di ricerca si concentrano sull&#39;acquisizione di nuovi clienti.

* *[!UICONTROL Retargeting]:* I pacchetti di retargeting si concentrano sulla riesposizione di visitatori o clienti precedenti.

* *[!UICONTROL Other]:* Tutti gli altri scopi.

**[!UICONTROL Linked Package for Optimization Learnings Carryover]:** (Solo pacchetti con obiettivi di ottimizzazione personalizzati) Un altro pacchetto i cui dati storici vengono utilizzati come input per l’ottimizzazione del pacchetto.

**[!UICONTROL Target]:** (Solo pacchetti con velocità a livello di pacchetto) L’obiettivo di destinazione, utilizzato per monitorare le prestazioni.

>[!NOTE]
>
>Questo campo è solo un valore di riferimento e non viene utilizzato per le decisioni.

**[!UICONTROL Frequency Cap]:** (Solo pacchetti con velocità a livello di pacchetto) Il numero di volte in cui un dispositivo o una persona univoca (a seconda della [!UICONTROL Cross Device Level] per la campagna) possono essere serviti annunci dal pacchetto. Le opzioni includono *[!UICONTROL Unlimited]* o un importo specifico per giorno, settimana o mese.

>[!NOTE]
>
>* Puoi impostare i limiti di frequenza a livello di campagna, pacchetto e posizionamento. L’DSP rispetta il limite di frequenza più severo nella gerarchia delle campagne.
>* La best practice prevede di impostare limiti di frequenza sia per la ricerca di potenziali clienti che per il retargeting a livello di pacchetto.
> * Limiti di frequenza più elevati determinano una spesa e impression più elevate, ma una portata più bassa. Limiti di frequenza più bassi determinano una spesa e impression minori, ma una portata più elevata.

**[!UICONTROL Pace on]:** (Solo pacchetti con velocità a livello di pacchetto) Su cosa si basa la velocità:

* *[!UICONTROL Budget]:* Impostazione predefinita. Questa opzione fornisce il maggior numero di impression possibile nel budget del pacchetto allocato.

* *[!UICONTROL Impressions]:* Questa opzione fornisce le impression fino al raggiungimento di una quantità specificata entro un intervallo specificato. Quando selezioni questa opzione, specifica il numero di impression e l’intervallo: *Sempre,* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* o *[!UICONTROL Weekly]*.

**[!UICONTROL Flight pacing]:** (Solo pacchetti con velocità a livello di pacchetto) Come organizzare e recapitare i messaggi durante l&#39;intero volo:

* *[!UICONTROL Even]:* La consegna avviene in modo uniforme su ogni volo, con un obiettivo del 50% della consegna nella prima metà del volo.

* *[!UICONTROL Slightly Ahead]:* (Impostazione predefinita) Accelera la consegna in modo che sia completa al 55-65% a metà della durata del volo.

* *[!UICONTROL Frontload]:* Accelera la consegna in modo che sia completa al 65-75% a metà del volo.

* *[!UICONTROL Aggressive Frontload]:* Accelera la consegna in modo che sia completa al 75-85% a metà del volo.

**[!UICONTROL Intraday pacing]:** (Solo pacchetti con velocità a livello di pacchetto) Come organizzare e consegnare ogni giorno all’interno del volo:

* *[!UICONTROL Even]:* (Impostazione predefinita) Ridimensiona la consegna in base alla disponibilità dell’inventario. In genere, vengono consegnati più annunci all’ora di giorno, quando il volume dell’asta è più alto e vengono consegnati meno annunci al mattino e alla sera.

* *[!UICONTROL ASAP]:* Accelera la consegna a una velocità doppia rispetto a *Uniforme*.

  >[!CAUTION]
  >
  >Questa opzione può influire negativamente sulle prestazioni. Utilizzalo solo quando assegni la massima priorità alla consegna e spendi oltre l’ottimizzazione delle prestazioni.

## [!UICONTROL Flighting]

(Pacchetti con velocità a livello di pacchetto e con &quot;[!UICONTROL Activate Custom Flighting]&quot; abilitato) Periodi di volo personalizzati entro il [!UICONTROL Flight Dates] specificato in [!UICONTROL Goals & Budget] sezione.

Per ogni volo, inserisci la data di inizio, la data di fine e il numero di impression previsto. Per aggiungere un altro volo, fai clic su **[!UICONTROL Add Flight]**.

>[!MORELIKETHIS]
>
>* [Informazioni sulla gestione dei pacchetti](package-about.md)
>* [Creare un pacchetto](package-create.md)
>* [Modificare un pacchetto](package-edit.md)
>* [Allegare un posizionamento a un pacchetto](package-attach-placement.md)
>* [Visualizzare il registro delle modifiche di un pacchetto](package-change-log.md)
>* [Domande frequenti su Campaign Management](/help/dsp/campaign-management/faq-campaign-management.md)
