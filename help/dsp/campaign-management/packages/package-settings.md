---
title: Impostazioni pacchetto
description: Consulta le descrizioni delle impostazioni del pacchetto disponibili.
feature: DSP Packages
exl-id: 20ec5e8e-4980-4fa0-80c9-531f5b02c0f9
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '797'
ht-degree: 0%

---

# Impostazioni pacchetto

## [!UICONTROL Basic Details]

**[!UICONTROL Name]:** Nome del pacchetto. La lunghezza massima è di 60 caratteri.

**[!UICONTROL Description]:** (Facoltativo) Una descrizione del pacchetto.

**[!UICONTROL 3rd Party Billed Fees]:** (Facoltativo) Una tariffa statica di terze parti da tenere traccia come costo non fatturabile:

>[!NOTE]
>
>Le commissioni fatturabili sono riportate nel [!UICONTROL Net CPM] metrica.
* **[!UICONTROL CPM]:** Il costo per 1000 impression (CPM).

* **[!UICONTROL CPM Description]:** Una descrizione della tariffa CPM.

È possibile ignorare l’impostazione a livello di pacchetto nella [livello di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md).

## [!UICONTROL Goals & Budget]

**[!UICONTROL Pacing & Capping]:** (Sola lettura per i pacchetti esistenti) A quale livello applicare e fissare i posizionamenti nel pacchetto:

* **[!UICONTROL Package level pacing]:** Questa strategia di velocità funziona passando e limitando tutti i posizionamenti inclusi come *gruppo*. Questa strategia assicura che tutti i posizionamenti all’interno di un dato pacchetto siano ottimizzati in modo olistico, distribuendo la spesa in base alle prestazioni e alla scala a specifici indicatori prestazioni chiave (KPI, Key Performance Indicators).

* **[!UICONTROL Placement level pacing]:**  Questa strategia di pacing funziona impilando e limitando tutti i posizionamenti inclusi *individualmente*. La migliore pratica è quella di utilizzare questa strategia solo per eseguire offerte garantite sul mercato privato.

**[!UICONTROL Flight Dates]:** Data di inizio e data di fine del pacchetto.

Per creare facoltativamente voli non pari per il pacchetto, selezionare *[!UICONTROL *Activate Custom Flighting]** e impostare i voli personalizzati nel [!UICONTROL Flighting] di seguito. Una volta attivato il volo personalizzato e salvato il pacchetto, non è possibile disattivare il volo personalizzato.

>[!NOTE]
>
>* Le date del volo devono essere incluse nelle date del volo della campagna. Inoltre, le date di volo per tutti i posizionamenti assegnati al pacchetto devono essere incluse entro tali date.
> * Non puoi modificare la data di inizio del pacchetto quando è attivato lo scaricamento personalizzato.


**[!UICONTROL Budget]:** (Pacchetti con solo velocità a livello di pacchetto) Il tetto di budget lordo e l&#39;intervallo di budget.

Per i pacchetti con voli personalizzati, l&#39;intervallo di budget è sempre *[!UICONTROL All time]*. Per i pacchetti senza scaricamento personalizzato, specifica l&#39;intervallo di budget: *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* o *[!UICONTROL Weekly]*.

**[!UICONTROL Gross Budget]:** (Pacchetti con velocità a livello di pacchetto e gestione dinamica dei margini) Il tetto di budget lordo per la durata del pacchetto.

**[!UICONTROL Optimization Goal]:** (Pacchetti con solo velocità a livello di pacchetto) L&#39;obiettivo di ottimizzazione per il pacchetto. Vedi le descrizioni di ogni obiettivo di ottimizzazione in [Obiettivi di ottimizzazione e come utilizzarli](/help/dsp/optimization/optimization-goals.md).

**[!UICONTROL Custom Goals]:** (Solo pacchetti con obiettivi di ottimizzazione personalizzati) Il [obiettivo personalizzato](/help/dsp/optimization/custom-goal-about.md) per il pacchetto. Per ulteriori informazioni sulle best practice per gli obiettivi personalizzati e le campagne che li utilizzano, consulta  [Tecniche consigliate per la creazione di un obiettivo personalizzato](/help/dsp/optimization/custom-goal-best-practices.md) e [Tecniche consigliate per l’impostazione di campagne sulle prestazioni](/help/dsp/optimization/campaign-best-practices-performance.md).

**[!UICONTROL Package Goal Type]:** (Solo pacchetti con obiettivi di ottimizzazione personalizzati) Lo scopo del pacchetto. Questa impostazione consente di determinare come ottimizzare il pacchetto:

* *[!UICONTROL Prospecting]:* I pacchetti prospettici si concentrano sull&#39;acquisizione di nuovi clienti.

* *[!UICONTROL Retargeting]:* I pacchetti di retargeting si concentrano sulla riesposizione di visitatori o clienti precedenti.

* *[!UICONTROL Other]:* Tutti gli altri scopi.

**[!UICONTROL Linked Package for Optimization Learnings Carryover]:** (Solo pacchetti con obiettivi di ottimizzazione personalizzati) Un altro pacchetto i cui dati storici vengono utilizzati come input per l&#39;ottimizzazione del pacchetto.

**[!UICONTROL Target]:** (Pacchetti con solo velocità a livello di pacchetto) L&#39;obiettivo di destinazione, che viene utilizzato per monitorare le prestazioni.

>[!NOTE]
>
>Questo campo è solo un punto di riferimento e non viene utilizzato per le decisioni.

**[!UICONTROL Frequency Cap]:** (Pacchetti solo a livello di pacchetto) Il numero di volte in cui un dispositivo o una persona univoca (a seconda del valore specificato) [!UICONTROL Cross Device Level] per la campagna) possono essere serviti gli annunci dal pacchetto. Le opzioni includono *[!UICONTROL Unlimited]* o un importo specifico per giorno, settimana o mese.

>[!NOTE]
>
>* Puoi impostare i limiti di frequenza a livello di campagna, pacchetto e posizionamento. DSP rispetta il limite di frequenza più rigoroso nella gerarchia delle campagne.
>* La migliore pratica è quella di impostare limiti di frequenza sia per la ricerca che per il retargeting a livello di pacchetto.
> * I limiti di frequenza più alti determinano una spesa e impression più elevate, ma una portata più bassa. I limiti di frequenza più bassi si traducono in una riduzione della spesa e delle impression ma in una maggiore portata.


**[!UICONTROL Pace on]:** (Pacchetti solo a livello di pacchetto) Su cosa si basa il pacchetto:

* *[!UICONTROL Budget]:* (Impostazione predefinita) Questa opzione offre il maggior numero possibile di impression nel budget del pacchetto allocato.

* *[!UICONTROL Impressions]:* Questa opzione consente di distribuire le impression finché non viene raggiunta una quantità specifica entro un intervallo specificato. Quando selezioni questa opzione, specifica il numero di impression e l’intervallo: *Tutto il tempo,* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* o *[!UICONTROL Weekly]*.

**[!UICONTROL Flight pacing]:** (Pacchetti solo a livello di pacchetto) Come effettuare la consegna degli annunci durante l&#39;intero volo:

* *[!UICONTROL Even]:* Paces delivery uniformemente in ogni volo, con un obiettivo del 50% della consegna nella prima metà del volo.

* *[!UICONTROL Slightly Ahead]:* (L’impostazione predefinita) Accelera la consegna in modo che sia completa a metà strada nel periodo di volo dal 55 al 65%.

* *[!UICONTROL Frontload]:* Accelera la consegna in modo che sia completa a metà del volo dal 65 al 75%.

* *[!UICONTROL Aggressive Frontload]:* Accelera la consegna in modo che sia completa a metà del volo dal 75 all&#39;85%.

**[!UICONTROL Intraday pacing]:** (Pacchetti solo a livello di pacchetto) Come effettuare la consegna degli annunci in ogni giorno all&#39;interno del volo:

* *[!UICONTROL Even]:* (L’impostazione predefinita) Consente di ridimensionare la consegna in base alla disponibilità dell’inventario. Generalmente, vengono consegnati più annunci all&#39;ora diurna, quando il volume dell&#39;asta è più alto e vengono consegnati meno annunci la mattina e la sera.

* *[!UICONTROL ASAP]:* Accelerazione della consegna a una velocità doppia rispetto alla *Pari*.

   >[!CAUTION]
   >
   >Questa opzione può influire negativamente sulle prestazioni. Utilizzalo solo quando stai dando priorità assoluta alla consegna e spendi più dell’ottimizzazione delle prestazioni.

## [!UICONTROL Flighting]

(Pacchetti con velocità a livello di pacchetto e con &quot;[!UICONTROL Activate Custom Flighting]&quot; abilitato) Periodi di volo personalizzati nel complesso [!UICONTROL Flight Dates] specificato nel [!UICONTROL Goals & Budget] sezione .

Per ogni volo, immetti la data di inizio, la data di fine e il numero di impression target. Per aggiungere un altro volo, fai clic su **[!UICONTROL Add Flight]**.

>[!MORELIKETHIS]
>
>* [Informazioni sulla gestione dei pacchetti](package-about.md)
>* [Creare un pacchetto](package-create.md)
>* [Modificare un pacchetto](package-edit.md)
>* [Allegare un posizionamento a un pacchetto](package-attach-placement.md)
>* [Visualizza il registro delle modifiche per un pacchetto](package-change-log.md)
>* [Domande frequenti su Campaign Management](/help/dsp/campaign-management/campaign-management-faq.md)

