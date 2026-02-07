---
title: Impostazioni pacchetto
description: Consulta le descrizioni delle impostazioni disponibili per il pacchetto.
feature: DSP Packages
exl-id: 20ec5e8e-4980-4fa0-80c9-531f5b02c0f9
source-git-commit: 86d77d23fbec15b1f80f3f9c41e66aab34a46079
workflow-type: tm+mt
source-wordcount: '1086'
ht-degree: 0%

---

# Impostazioni pacchetto

## [!UICONTROL Basic Details]

**[!UICONTROL Name]:** Il nome del pacchetto. La lunghezza massima è di 60 caratteri.

**[!UICONTROL Description]:** (facoltativo) descrizione del pacchetto.

**[!UICONTROL 3rd Party Billed Fees]:** (Facoltativo) Una tariffa statica di terze parti da registrare come costo non fatturabile:

* **[!UICONTROL CPM]:** Il costo per 1000 impression (CPM).

* **[!UICONTROL Description]:** Descrizione della tariffa CPM.

>[!NOTE]
>
>Le tariffe fatturabili si riflettono nella metrica [!UICONTROL Net CPM].

Puoi ignorare l&#39;impostazione a livello di pacchetto al [livello di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md).

## [!UICONTROL Goals & Budget]

**[!UICONTROL Pacing & Capping]:** (sola lettura per i pacchetti esistenti) A quale livello posizionare e limitare i posizionamenti nel pacchetto:

* **[!UICONTROL Package level pacing]:** Questa strategia di velocità opera definendo il ritmo e la limitazione di tutti i posizionamenti inclusi come *gruppo*. Questa strategia assicura che tutti i posizionamenti all’interno di un determinato pacchetto siano ottimizzati in modo olistico, distribuendo la spesa in base alle prestazioni e alla scalabilità a specifici indicatori di prestazioni chiave (KPI, Key Performance Indicator).

* **[!UICONTROL Placement level pacing]:** Questa strategia di velocità funziona calcolando il ritmo e la limitazione di tutti i posizionamenti inclusi *singolarmente*. La best practice prevede di utilizzare questa strategia solo per eseguire transazioni garantite sul mercato privato.

**[!UICONTROL Flight Dates]:** La data di inizio e la data di fine complessive del pacchetto. Le date del volo devono essere incluse nelle date del volo della campagna.

>[!NOTE]
>
>* Le date del volo per tutti i posizionamenti assegnati a questo pacchetto devono essere incluse entro queste date.
> * Non puoi modificare la data di inizio del pacchetto quando viene attivato il riflesso personalizzato.

**[!UICONTROL Activate Custom Flighting]:** consente di creare voli di andata e ritorno non uniformi per il pacchetto nella sezione [!UICONTROL Flighting] di seguito. Una volta attivato il riflesso personalizzato e salvato il pacchetto, non è possibile disattivare il riflesso personalizzato né modificare la data di inizio del pacchetto.

**[!UICONTROL Budget]:** (solo pacchetti con velocità a livello di pacchetto) Limite di budget lordo e intervallo di budget.

Per i pacchetti con conflitti personalizzati, l&#39;intervallo di budget è sempre *[!UICONTROL All time]*. Per i pacchetti senza sfarfallio personalizzato, specificare l&#39;intervallo di budget: *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* o *[!UICONTROL Weekly]*.

**[!UICONTROL Gross Budget]:** (solo pacchetti con velocità a livello di pacchetto e gestione dei margini dinamici) Limite di budget lordo per la durata del pacchetto.

**[!UICONTROL Optimization Goal]:** (solo pacchetti con velocità a livello di pacchetto) Obiettivo di ottimizzazione per il pacchetto. Vedi le descrizioni di ciascun obiettivo di ottimizzazione in [Obiettivi di ottimizzazione e come utilizzarli](/help/dsp/optimization/optimization-goals.md).

**[!UICONTROL Link PG Placements for Incremental Reach Optimization]:** (solo pacchetti con velocità a livello di pacchetto e con obiettivi di ottimizzazione &quot;[!UICONTROL Always Max Bid & Maximize Reach]&quot; e &quot;[!UICONTROL Lowest Cost per Reach]&quot;) Utilizza i dati di portata domestica da tutti i posizionamenti programmatici garantiti nella campagna per l&#39;ottimizzazione per la portata incrementale.

**[!UICONTROL Custom Goal for Model Learning]:** (solo pacchetti con gli obiettivi di ottimizzazione &quot;[!UICONTROL Highest Return on Ad Spend]&quot; e &quot;[!UICONTROL Lowest Cost per Acquisition]&quot;) [obiettivo personalizzato](/help/dsp/optimization/custom-goal.md) che include gli eventi di conversione o ricavi utilizzati per calcolare la metrica CPA o ROAS. L’obiettivo personalizzato deve includere eventi funnel superiori ponderati aggiuntivi (come visite alla pagina e aggiunte al carrello) da utilizzare in aggiunta alla metrica CPA o ROAS per l’ottimizzazione del pacchetto. Per ulteriori informazioni sugli obiettivi personalizzati, incluse le best practice per la creazione di obiettivi personalizzati e campagne che li utilizzano, vedere &quot;[Obiettivi personalizzati](/help/dsp/optimization/custom-goal.md)&quot; e &quot;[Best practice per l&#39;impostazione di campagne delle prestazioni](/help/dsp/optimization/campaign-best-practices-performance.md).&quot;<!-- At some point, all of the objectives will be prefixed with "ADSP_," but probably that won't show up in the Custom Goal list in the DSP UI. -->

**[!UICONTROL Consider Only Click Conversions for Model Learning]:** (Facoltativo; pacchetti con solo gli obiettivi di ottimizzazione &quot;[!UICONTROL Highest Return on Ad Spend]&quot; e &quot;[!UICONTROL Lowest Cost per Acquisition]&quot;) indica al modello di ottimizzazione di imparare solo dalle conversioni basate su clic. In caso contrario, il modello di ottimizzazione apprende sia dalle conversioni basate su clic che da quelle basate su impression.

**[!UICONTROL Conversion Metric]:** (solo pacchetti con gli obiettivi di ottimizzazione &quot;[!UICONTROL Highest Return on Ad Spend]&quot; e &quot;[!UICONTROL Lowest Cost per Acquisition]&quot;) l&#39;evento di conversione finale (ad esempio le iscrizioni) o l&#39;importo di evento di ricavo/vendita (ad esempio i valori di acquisto e di acquisto) da utilizzare per calcolare il ritorno sulla spesa pubblicitaria o il costo per acquisizione. Seleziona da un elenco di tutti gli eventi primari (&quot;metriche obiettivo&quot;) mappati all&#39;obiettivo personalizzato selezionato. Se l’elenco è vuoto, modifica l’obiettivo personalizzato in modo da includere almeno uno degli eventi sottostanti come metrica di obiettivo.

**[!UICONTROL Package Goal Type]:** (solo pacchetti con obiettivi di ottimizzazione personalizzati) Scopo del pacchetto. Questa impostazione consente di determinare come ottimizzare il pacchetto:

* *[!UICONTROL Prospecting]:* I pacchetti di prospezione si concentrano sull&#39;acquisizione di nuovi clienti.

* *[!UICONTROL Retargeting]:* i pacchetti di retargeting si concentrano sulla riesposizione di visitatori o clienti precedenti.

* *[!UICONTROL Other]:* Tutti gli altri scopi.

**[!UICONTROL Linked Package for Optimization Learnings Carryover]:** (solo pacchetti con obiettivi di ottimizzazione personalizzati) Un altro pacchetto i cui dati storici vengono utilizzati come input per l&#39;ottimizzazione del pacchetto.

**[!UICONTROL Target]:** (solo pacchetti con velocità a livello di pacchetto) L&#39;obiettivo di destinazione, utilizzato per tenere traccia delle prestazioni.

>[!NOTE]
>
>Questo campo è solo un valore di riferimento e non viene utilizzato per le decisioni.

**[!UICONTROL Frequency Cap]:** (solo pacchetti con velocità a livello di pacchetto) Il numero di volte in cui un dispositivo univoco, un ID universale o una persona (a seconda del [!UICONTROL Cross Device Level] specificato per la campagna e dell&#39;impostazione [!UICONTROL Targeting] del posizionamento) possono essere serviti annunci dal pacchetto. Le opzioni includono *[!UICONTROL Unlimited]* o un importo specifico per giorno, settimana o mese.

>[!NOTE]
>
>* Puoi impostare i limiti di frequenza a livello di campagna, pacchetto e posizionamento. DSP rispetta il limite di frequenza più rigoroso nella gerarchia delle campagne.
>* La best practice prevede di impostare limiti di frequenza sia per la ricerca di potenziali clienti che per il retargeting a livello di pacchetto.
> * Limiti di frequenza più elevati determinano una spesa e impression più elevate, ma una portata più bassa. Limiti di frequenza più bassi determinano una spesa e impression minori, ma una portata più elevata.

**[!UICONTROL Pace on]:** (solo pacchetti con velocità a livello di pacchetto) Su cosa si basa la velocità:

* *[!UICONTROL Budget]:* (predefinito) Questa opzione fornisce il maggior numero di impression possibile nel budget del pacchetto allocato.

* *[!UICONTROL Impressions]:* Questa opzione fornisce impression fino al raggiungimento di una quantità specificata entro un intervallo specificato. Quando selezioni questa opzione, specifica il numero di impression e l&#39;intervallo: *All time,* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* o *[!UICONTROL Weekly]*.

**[!UICONTROL Flight pacing]:** (solo pacchetti con velocità a livello di pacchetto) Come pianificare la consegna degli annunci sull&#39;intero volo:

* *[!UICONTROL Even]:* La consegna avviene in modo uniforme per ogni volo, con un target pari al 50% della consegna nella prima metà del volo.

* *[!UICONTROL Slightly Ahead]:* (impostazione predefinita) Accelera la consegna in modo che sia completa al 55-65% a metà della durata del volo.

* *[!UICONTROL Frontload]:* Accelera la consegna in modo che sia completa al 65-75% a metà del volo.

* *[!UICONTROL Aggressive Frontload]:* Accelera la consegna in modo che sia completa al 75-85% a metà del volo.

**[!UICONTROL Intraday pacing]:** (solo pacchetti con velocità a livello di pacchetto) Come pianificare la consegna degli annunci per ogni giorno all&#39;interno del volo:

* *[!UICONTROL Even]:* (impostazione predefinita) Ridimensiona la consegna in base alla disponibilità dell&#39;inventario. In genere, vengono consegnati più annunci all’ora di giorno, quando il volume dell’asta è più alto e vengono consegnati meno annunci al mattino e alla sera.

* *[!UICONTROL ASAP]:* accelera la consegna a una velocità doppia rispetto a *Even*.

  >[!CAUTION]
  >
  >Questa opzione può influire negativamente sulle prestazioni. Utilizzalo solo quando assegni la massima priorità alla consegna e spendi oltre l’ottimizzazione delle prestazioni.

## [!UICONTROL Flighting]

(Pacchetti con velocità a livello di pacchetto) I periodi di volo del pacchetto, inclusi eventuali periodi di volo personalizzati entro il [!UICONTROL Flight Dates] complessivo per il pacchetto. È possibile configurare voli personalizzati solo se l&#39;opzione [!UICONTROL Activate Custom Flighting] è abilitata nella sezione [!UICONTROL Goals & Budget].

**[!UICONTROL Automatically rollover remaining flight budget to next flight]:** (disponibile solo quando l&#39;opzione [!UICONTROL Activate Custom Flighting] è abilitata) Aggiunge automaticamente qualsiasi budget rimanente del volo precedente al budget esistente per il volo successivo.

Nella visualizzazione [!UICONTROL Packages] e nella visualizzazione [!DNL Package Name] > [!UICONTROL Flights], il campo [!UICONTROL Interval Goal], che mostra l&#39;obiettivo del volo corrente, include qualsiasi budget di rollover.

**[!DNL Flight N]:** (disponibile solo quando l&#39;opzione [!UICONTROL Activate Custom Flighting] è abilitata) Per ogni volo, specificare la data di inizio, la data di fine e l&#39;obiettivo di spesa target. Per aggiungere un altro volo, fare clic su **[!UICONTROL Add Flight]**.

Per i pacchetti esistenti senza l&#39;opzione &quot;[!UICONTROL Automatically rollover remaining flight budget to next flight]&quot; abilitata, è possibile riaprire le impostazioni per immettere un valore nella colonna **[!UICONTROL Rollover]** per qualsiasi volo per aggiungere un budget potenzialmente non speso al volo successivo.

>[!MORELIKETHIS]
>
>* [Informazioni sulla gestione dei pacchetti](package-about.md)
>* [Crea pacchetto](package-create.md)
>* [Modifica pacchetto](package-edit.md)
>* [Allega un posizionamento a un pacchetto](package-attach-placement.md)
>* [Visualizza il log delle modifiche per un pacchetto](package-change-log.md)
>* [Domande frequenti sulla gestione delle campagne](/help/dsp/campaign-management/faq-campaign-management.md)
