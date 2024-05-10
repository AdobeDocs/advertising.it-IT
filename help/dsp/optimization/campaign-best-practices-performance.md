---
title: Best practice per l’impostazione di campagne sulle prestazioni
description: Scopri le best practice per la configurazione di campagne incentrate sulle prestazioni, che includono posizionamenti ottimizzati per il CPA più basso o il ROAS più alto.
feature: DSP Optimization, DSP Best Practices
exl-id: bc297796-0c89-4d91-87aa-0668462526ae
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '1268'
ht-degree: 0%

---

# Best practice per l’impostazione di campagne sulle prestazioni

L’DSP può ottimizzare le campagne incentrate sulle prestazioni. Consulta le seguenti best practice per le campagne sulle prestazioni:

* Passaggio 1: definire l’obiettivo
* Passaggio 2: definire la strategia
* Passaggio 3: creare pacchetti
* Passaggio 4: creare la struttura di posizionamento
* Passaggio 5: utilizzare le risorse creative giuste

## Passaggio 1: definire l’obiettivo

È importante comprendere l&#39;obiettivo della campagna, ad esempio raggiungere il ROAS più alto possibile o il CPA più basso possibile. Le campagne di prestazioni presentano [obiettivi di ottimizzazione](/help/dsp/optimization/optimization-goals.md) &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"] o &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)].&quot; Per ogni pacchetto della campagna, specifica di conseguenza l’obiettivo di ottimizzazione.

![obiettivo di ottimizzazione](/help/dsp/assets/optimization-goals.png)

È inoltre necessario determinare gli eventi di successo che conducono all’obiettivo generale e creare obiettivi personalizzati di conseguenza. Per ogni pacchetto, specifica un obiettivo personalizzato da utilizzare con l’obiettivo di ottimizzazione generale per il reporting e l’ottimizzazione algoritmica utilizzando [!DNL Adobe Sensei]. Per ulteriori informazioni sulla creazione di obiettivi personalizzati, vedi [Best practice per la creazione di un obiettivo personalizzato](custom-goal.md#custom-goal-best-practices).

![obiettivi personalizzati](/help/dsp/assets/objective-goals.png)

## Passaggio 2: definire la strategia

### Strategie di prospezione

I pacchetti funnel superiori includono posizionamenti con targeting molto ampio per raggiungere nuovi consumatori.

#### Strategie di posizionamento consigliate per la ricerca

* Trova nuovi tipi di pubblico che potrebbero essere convertiti utilizzando le seguenti tattiche:

   * Modellazione lookalike da una piattaforma di gestione dati (DMP, Data Management Platform), ad esempio Adobe Audience Manager.
   * Targeting comportamentale con dati di terze parti.
   * Targeting contestuale.
   * Targeting di siti/categorie.

* Utilizzo del targeting di rete (RON): è importante includere un’esecuzione del posizionamento di rete senza targeting di pubblico e con targeting di inventario ampio. Ciò consente [!DNL Adobe Sensei] algoritmo per trovare utenti importanti che potrebbero disporre di cookie più recenti non ancora categorizzati in un pubblico.

### Strategie di retargeting

I pacchetti funnel inferiori includono posizionamenti che eseguono il targeting di utenti che sono già stati sulla pagina web dell’inserzionista o per i quali l’inserzionista dispone di dati CRM.

#### Strategie di posizionamento consigliate per il retargeting

* Se l’inserzionista è un cliente di Adobe Analytics o Adobe Audience Manager, puoi creare segmenti di prime parti (come visitatori di homepage, pagine di prodotti o abbandonatori di carrello) e utilizzarli come target di posizionamento in DSP.

* Evita di assegnare troppo budget a un posizionamento mirato al pubblico. Come regola generale, preventivare $30 per 1.000 utenti al mese.

## Passaggio 3: creare pacchetti

La best practice prevede la creazione di pacchetti separati per la ricerca del funnel superiore e per il retargeting del funnel inferiore. L’ottimizzazione viene eseguita a livello di pacchetto, in modo che i dati delle prestazioni provenienti da tutti i posizionamenti all’interno di un pacchetto vengano aggregati. Raggruppa quindi i posizionamenti in pacchetti con prestazioni previste simili.

![esempio di pacchetti separati per la ricerca e il retargeting](/help/dsp/assets/p-r.png)

Inoltre, utilizza le seguenti impostazioni.

### Obiettivi e budget

* **Ritmo e limite:** Per selezionare un obiettivo di ottimizzazione CPA o ROAS, il pacchetto deve utilizzare la velocità a livello di pacchetto. In questo modo tutti i posizionamenti all’interno del pacchetto vengono ottimizzati per distribuire la spesa in base alle prestazioni e alla scalabilità per gli obiettivi selezionati.

* **Date di volo:** (Ricerca di pacchetti) Quando la campagna è in esecuzione per più di 25 giorni, utilizza [!UICONTROL Activate Custom Flighting] funzionalità. In primo luogo, impostare un volo personalizzato per i primi 10 giorni a circa il 75% del budget giornaliero necessario per ridurre la spesa durante il *fase di apprendimento*. Quindi imposta un secondo volo personalizzato per il resto del budget.

  Ad esempio, se hai $ 100.000 da spendere in 30 giorni, imposta il budget per il volo 1 (giorni 1-10) su $ 25.000 (75% x $ 100.000/30 giorni = $ 2.500 al giorno). Utilizza il budget rimanente di $ 75.000 per il volo 2 (giorni 11-30).

* **Budget:** L&#39;DSP cerca sempre di allocare il 100% del budget del pacchetto in modo uniforme tra tutti i posizionamenti all&#39;interno di un pacchetto. Se un posizionamento ha una spesa bassa o nessuna spesa, si consiglia di limitare il budget al posizionamento per consentire di allocare una maggiore parte del budget a posizionamenti con scala. Consenti 24-48 ore per la calibrazione delle modifiche di budget.

* **Obiettivi di ottimizzazione:** Utilizzare uno dei due obiettivi di ottimizzazione delle prestazioni, *[!UICONTROL Highest Return on Ad Spend]* o *[!UICONTROL Lowest Cost per Acquisition]*, a seconda dell’obiettivo del pacchetto. Questi obiettivi ottimizzano automaticamente il pacchetto rispettivamente verso i posizionamenti ROAS più elevati o CPA più bassi.

* **Obiettivi personalizzati:**
   * Se un nuovo pacchetto ha lo stesso obiettivo di un pacchetto esistente, puoi facoltativamente collegare il pacchetto esistente in modo che l’algoritmo possa utilizzare i dati di apprendimento automatico esistenti.
   * Immetti il valore appropriato [!UICONTROL Target CPA] o [!UICONTROL Target ROAS].

* **Andamento del volo e andamento infragiornaliero:** Per entrambi i tipi di velocità, selezionare *[!UICONTROL Even]* massimizzare gli obiettivi prestazionali con un ritmo uniforme durante tutto il giorno e per l&#39;intero volo.

  >[!CAUTION]
  >
  >Utilizzare *[!UICONTROL FrontLoad]* e *[!UICONTROL Aggressive Front Load]* per l&#39;andamento dei voli e *[!UICONTROL ASAP]* ritmo per il ritmo infragiornaliero solo quando si assegnano priorità complete alla consegna e si spende rispetto all’ottimizzazione delle prestazioni, perché tali strategie possono influire negativamente sui KPI delle prestazioni desiderati.

## Passaggio 4: creare la struttura di posizionamento

Meno è di più. Se puoi impostare meno di sei posizionamenti per pacchetto, il budget disponibile può essere spostato dinamicamente verso i posizionamenti con le prestazioni migliori più facilmente.

Inoltre, assicurati di aggiungere ogni posizionamento a un pacchetto con un obiettivo del pacchetto di tipo *[!UICONTROL Prospecting]* o *[!UICONTROL Retargeting]*, a seconda dei casi.

Di seguito sono riportate le impostazioni di posizionamento consigliate per le campagne di prestazioni.

### Obiettivi

È necessario configurare l’ottimizzazione CPA o ROAS a livello di pacchetto (vedere Passaggio 3 - Creare pacchetti), ma è possibile aggiungere ulteriori impostazioni a livello di posizionamento.

* **Offerta massima:**
   * Per la ricerca di posizionamenti, utilizza un&#39;offerta massima bassa ($ 5).
   * Per i posizionamenti di retargeting, utilizza un’offerta massima elevata ($ 12).

* **Filtri pre-offerta:** Riduci al minimo o evita idealmente di impostare filtri aggressivi pre-offerta, che impediscono al posizionamento di raggiungere la scala. Le best practice includono:

   * Utilizza un (1) filtro di pre-offerta per posizionamento. L’utilizzo di più filtri pre-offerta richiede il rispetto di entrambi, il che riduce la scalabilità.

   * Prendi in considerazione l’impostazione di filtri pre-offerta meno rigidi nei casi in cui viene applicato un targeting aggiuntivo (come targeting di pubblico, geografico e del sito).

Consulta le descrizioni di quando utilizzare ciascun filtro di pre-offerta all’indirizzo [Filtri pre-offerta a livello di posizionamento e come utilizzarli](/help/dsp/optimization/optimization-pre-bid-filters.md).

### Inventario

Per massimizzare la scala, utilizza [!UICONTROL Public] (Open Exchange) e [!UICONTROL On Demand] inventario.

### Targeting del sito

* **[!UICONTROL Traffic Type]**: [!UICONTROL Websites] solo
* **[!UICONTROL Site Tier]**: [!UICONTROL All sites]

### Targeting del pubblico

<!-- Say something about limiting unnecessary constraints/limitations, including dayparting, which limit your chances for ad exposure. Use only when it's required for your audience. -->

* **[!UICONTROL Included Audiences]:**
   * Per la ricerca di posizionamenti, raggruppa categorie di pubblico simili e dimensioni di pubblico simili in un unico posizionamento. Quindi, in base alle prestazioni, eseguire una delle operazioni seguenti:
      * Rimuovi i tipi di pubblico con prestazioni meno soddisfacenti dai posizionamenti esistenti.
      * Sposta i tipi di pubblico con prestazioni migliori in un posizionamento separato per controllare meglio i budget.
   * Per i posizionamenti di retargeting, è consigliabile includere un segmento di pubblico per posizionamento per controllare facilmente le offerte e il budget.

>[!NOTE]
>
>I tuoi annunci funzionano meglio se un utente può essere raggiunto da un solo posizionamento. Una significativa sovrapposizione degli utenti tra i posizionamenti può causare concorrenza, che si traduce in un ciclo di offerte in continuo aumento, aumentando il costo per utente. Pertanto, se includi più tipi di pubblico, assicurati che non siano composti da utenti/membri del pubblico sovrapposti.
>
> È possibile evitare la sovrapposizione dei tipi di pubblico creando i tipi di pubblico in livelli in modo da poter eliminare i livelli più alti e più inclusivi dai posizionamenti in base alle esigenze.

* **[!UICONTROL Frequency Capping]:**
   * Per la ricerca di posizionamenti, utilizza limiti di frequenza stretti (un’impression al giorno).
   * Per i posizionamenti di retargeting, imposta il limite di posizionamento principale su 6-10 impression al giorno e il limite secondario su un’impression all’ora.

* **[!UICONTROL Device Targeting]**:
   * Includi [!UICONTROL Computer], [!UICONTROL Mobile], e [!UICONTROL Tablet].
   * Non mirare [!UICONTROL Firefox] e [!UICONTROL Safari] a causa di limiti di targeting e misurazione. Contatta il team del tuo account Adobe per maggiori dettagli su [!DNL Adobe] supporto per [!DNL Safari ITP].
   * Se esegui il targeting del traffico web per dispositivi mobili, disattiva tutti i browser mobili eccetto [!UICONTROL Chrome] e [!UICONTROL Edge].

### Sicurezza del marchio e qualità dei contenuti multimediali

Utilizzo del filtro contestuale, del blocco preventivo delle frodi e/o [!UICONTROL Ads.txt] il filtro limita la scala dei posizionamenti, ma utilizzali se necessario.

## Passaggio 5: utilizzare le risorse creative giuste

* La best practice prevede di includere quante più dimensioni di annuncio univoche possibili per massimizzare la portata. Il modello di visualizzazione universale ti consente di caricare qualsiasi dimensione di annuncio display standard.
* Assicurati che tutti i posizionamenti contengano *almeno* tutte le dimensioni principali degli annunci display (300x250, 728x90, 160x600, 300x600, 320x50 e 300x50).
* Aggiorna spesso le creatività per evitare l’eccesso di creatività.

>[!MORELIKETHIS]
>
>* [Impostazioni pacchetto](/help/dsp/campaign-management/packages/package-settings.md)
>* [Impostazioni di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md)
> * [Come l’DSP ottimizza le campagne](optimization-how-dsp-optimizes-campaigns.md)
>* [Obiettivi di ottimizzazione e modalità di utilizzo](optimization-goals.md)
>* [Filtri pre-offerta a livello di posizionamento e come utilizzarli](optimization-pre-bid-filters.md)
>* [Elenco di controllo per il lancio di Campaign](/help/dsp/campaign-management/campaign-launch-checklist.md)
