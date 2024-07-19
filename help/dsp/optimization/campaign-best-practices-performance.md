---
title: Best practice per l’impostazione di campagne sulle prestazioni
description: Scopri le best practice per la configurazione di campagne incentrate sulle prestazioni, che includono posizionamenti ottimizzati per il CPA più basso o il ROAS più alto.
feature: DSP Optimization, DSP Best Practices
exl-id: bc297796-0c89-4d91-87aa-0668462526ae
source-git-commit: 802c75920bb11f262cbe0d76d2554971aaf35831
workflow-type: tm+mt
source-wordcount: '1263'
ht-degree: 0%

---

# Best practice per l’impostazione di campagne sulle prestazioni

L’DSP può ottimizzare le campagne incentrate sulle prestazioni. Consulta le seguenti best practice per le campagne sulle prestazioni:

* Passaggio 1: definire l’obiettivo
* Passaggio 2: definire la strategia
* Passaggio 3: creare pacchetti
* Passaggio 4: creare la struttura di posizionamento
* Passaggio 5: utilizzare il giusto Assets creativo

## Passaggio 1: definire l’obiettivo

È importante comprendere l&#39;obiettivo della campagna, ad esempio raggiungere il ROAS più alto possibile o il CPA più basso possibile. Le campagne di prestazioni hanno gli [obiettivi di ottimizzazione](/help/dsp/optimization/optimization-goals.md) &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"] o &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot;.&quot; Per ogni pacchetto della campagna, specifica di conseguenza l’obiettivo di ottimizzazione.

![obiettivo di ottimizzazione](/help/dsp/assets/optimization-goals.png)

È inoltre necessario determinare gli eventi di successo che conducono all’obiettivo generale e creare obiettivi personalizzati di conseguenza. Per ogni pacchetto, specifica un obiettivo personalizzato da utilizzare con l&#39;obiettivo di ottimizzazione generale per il reporting e l&#39;ottimizzazione algoritmica utilizzando [!DNL Adobe Sensei]. Per ulteriori informazioni sulla creazione di obiettivi personalizzati, incluse le best practice, vedere [Obiettivi personalizzati](custom-goal.md).

## Passaggio 2: definire la strategia

### Strategie di prospezione

I pacchetti funnel superiori includono posizionamenti con targeting molto ampio per raggiungere nuovi consumatori.

#### Strategie di posizionamento consigliate per la ricerca

* Trova nuovi tipi di pubblico che potrebbero essere convertiti utilizzando le seguenti tattiche:

   * Modellazione lookalike da una piattaforma di gestione dati (DMP, Data Management Platform), ad esempio Adobe Audience Manager.
   * Targeting comportamentale con dati di terze parti.
   * Targeting contestuale.
   * Targeting di siti/categorie.

* Utilizzo del targeting di rete (RON): è importante includere un’esecuzione del posizionamento di rete senza targeting di pubblico e con targeting di inventario ampio. Questo consente all&#39;algoritmo [!DNL Adobe Sensei] di trovare utenti importanti che potrebbero disporre di cookie più recenti che non sono ancora stati categorizzati in un pubblico.

### Strategie di retargeting

I pacchetti funnel inferiori includono posizionamenti che eseguono il targeting di utenti che sono già stati sulla pagina web dell’inserzionista o per i quali l’inserzionista dispone di dati CRM.

#### Strategie di posizionamento consigliate per il retargeting

* Se l’inserzionista è un cliente di Adobe Analytics o Adobe Audience Manager, puoi creare segmenti di prime parti (come visitatori di homepage, pagine di prodotti o abbandonatori di carrello) e utilizzarli come target di posizionamento in DSP.

* Evita di assegnare troppo budget a un posizionamento mirato al pubblico. Come regola generale, preventivare $30 per 1.000 utenti al mese.

## Passaggio 3: creare pacchetti

La best practice prevede la creazione di pacchetti separati per la ricerca del funnel superiore e per il retargeting del funnel inferiore. L’ottimizzazione viene eseguita a livello di pacchetto, in modo che i dati delle prestazioni provenienti da tutti i posizionamenti all’interno di un pacchetto vengano aggregati. Raggruppa quindi i posizionamenti in pacchetti con prestazioni previste simili.

![esempio di pacchetti separati per l&#39;individuazione e il retargeting](/help/dsp/assets/p-r.png)

Inoltre, utilizza le seguenti impostazioni.

### Obiettivi e budget

* **Velocità e limite:** Per selezionare un obiettivo di ottimizzazione CPA o ROAS, il pacchetto deve utilizzare la velocità a livello di pacchetto. In questo modo tutti i posizionamenti all’interno del pacchetto vengono ottimizzati per distribuire la spesa in base alle prestazioni e alla scalabilità per gli obiettivi selezionati.

* **Date di volo:** (individuazione pacchetti) Quando la campagna dura più di 25 giorni, utilizza la funzionalità [!UICONTROL Activate Custom Flighting]. In primo luogo, impostare un volo personalizzato per i primi 10 giorni a circa il 75% del budget giornaliero necessario per ridurre la spesa durante la *fase di apprendimento*. Quindi imposta un secondo volo personalizzato per il resto del budget.

  Ad esempio, se hai $ 100.000 da spendere in 30 giorni, imposta il budget per il volo 1 (giorni 1-10) su $ 25.000 (75% x $ 100.000/30 giorni = $ 2.500 al giorno). Utilizza il budget rimanente di $ 75.000 per il volo 2 (giorni 11-30).

* **Budget:** l&#39;DSP tenta sempre di allocare il 100% del budget del pacchetto in modo uniforme tra tutti i posizionamenti in un pacchetto. Se un posizionamento ha una spesa bassa o nessuna spesa, si consiglia di limitare il budget al posizionamento per consentire di allocare una maggiore parte del budget a posizionamenti con scala. Consenti 24-48 ore per la calibrazione delle modifiche di budget.

* **Obiettivi di ottimizzazione:** Utilizzare uno dei due obiettivi di ottimizzazione delle prestazioni, *[!UICONTROL Highest Return on Ad Spend]* o *[!UICONTROL Lowest Cost per Acquisition]*, a seconda dell&#39;obiettivo del pacchetto. Questi obiettivi ottimizzano automaticamente il pacchetto rispettivamente verso i posizionamenti ROAS più elevati o CPA più bassi.

* **Obiettivi personalizzati:**
   * Se un nuovo pacchetto ha lo stesso obiettivo di un pacchetto esistente, puoi facoltativamente collegare il pacchetto esistente in modo che l’algoritmo possa utilizzare i dati di apprendimento automatico esistenti.
   * Immettere il [!UICONTROL Target CPA] o il [!UICONTROL Target ROAS] appropriato.

* **Andamento di volo e Andamento infragiornaliero:** Per entrambi i tipi di andamento, selezionare *[!UICONTROL Even]* per massimizzare gli obiettivi prestazionali eseguendo un andamento uniforme durante ogni giorno e per l&#39;intero volo.

  >[!CAUTION]
  >
  >Utilizza *[!UICONTROL FrontLoad]* e *[!UICONTROL Aggressive Front Load]* per l&#39;andamento del volo e *[!UICONTROL ASAP]* per l&#39;andamento infragiornaliero solo quando assegni la massima priorità alla consegna e spendi oltre l&#39;ottimizzazione delle prestazioni, perché queste strategie possono influire negativamente sui KPI delle prestazioni desiderati.

## Passaggio 4: creare la struttura di posizionamento

Meno è di più. Se puoi impostare meno di sei posizionamenti per pacchetto, il budget disponibile può essere spostato dinamicamente verso i posizionamenti con le prestazioni migliori più facilmente.

Inoltre, assicurarsi di aggiungere ogni posizionamento a un pacchetto con un tipo di obiettivo del pacchetto di *[!UICONTROL Prospecting]* o *[!UICONTROL Retargeting]*, come appropriato.

Di seguito sono riportate le impostazioni di posizionamento consigliate per le campagne di prestazioni.

### Obiettivi

È necessario configurare l’ottimizzazione CPA o ROAS a livello di pacchetto (vedere Passaggio 3 - Creare pacchetti), ma è possibile aggiungere ulteriori impostazioni a livello di posizionamento.

* **Offerta massima:**
   * Per la ricerca di posizionamenti, utilizza un&#39;offerta massima bassa ($ 5).
   * Per i posizionamenti di retargeting, utilizza un’offerta massima elevata ($ 12).

* **Filtri pre-offerta:** Riduci al minimo o evita idealmente di impostare filtri pre-offerta aggressivi che impediscono al posizionamento di raggiungere la scalabilità. Le best practice includono:

   * Utilizza un (1) filtro di pre-offerta per posizionamento. L’utilizzo di più filtri pre-offerta richiede il rispetto di entrambi, il che riduce la scalabilità.

   * Prendi in considerazione l’impostazione di filtri pre-offerta meno rigidi nei casi in cui viene applicato un targeting aggiuntivo (come targeting di pubblico, geografico e del sito).

Consulta le descrizioni di quando utilizzare ogni filtro di pre-offerta a [Filtri di pre-offerta a livello di posizionamento e Come utilizzarli](/help/dsp/optimization/optimization-pre-bid-filters.md).

### Inventario

Per ottimizzare la scalabilità, utilizzare [!UICONTROL Public] (Open Exchange) e [!UICONTROL On Demand] inventario.

### Targeting del sito

* **[!UICONTROL Traffic Type]**: solo [!UICONTROL Websites]
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
   * Includi [!UICONTROL Computer], [!UICONTROL Mobile] e [!UICONTROL Tablet].
   * Non eseguire il targeting di [!UICONTROL Firefox] e [!UICONTROL Safari] a causa di limitazioni di targeting e misurazione. Contattare il team dell&#39;account Adobe per ulteriori dettagli sul supporto di [!DNL Adobe] per [!DNL Safari ITP].
   * Se esegui il targeting del traffico web per dispositivi mobili, disabilita tutti i browser mobili eccetto [!UICONTROL Chrome] e [!UICONTROL Edge].

### Sicurezza del marchio e qualità dei contenuti multimediali

L&#39;utilizzo del filtro contestuale, del blocco antifrode pre-offerta e/o del filtro [!UICONTROL Ads.txt] limita la scala dei posizionamenti, ma utilizzali se necessario.

## Passaggio 5: utilizzare il giusto Assets creativo

* La best practice prevede di includere quante più dimensioni di annuncio univoche possibili per massimizzare la portata. Il modello di visualizzazione universale ti consente di caricare qualsiasi dimensione di annuncio display standard.
* Assicurati che tutti i posizionamenti contengano *almeno* tutte le dimensioni degli annunci display primari (300x250, 728x90, 160x600, 300x600, 320x50 e 300x50).
* Aggiorna spesso le creatività per evitare l’eccesso di creatività.

>[!MORELIKETHIS]
>
>* [Impostazioni pacchetto](/help/dsp/campaign-management/packages/package-settings.md)
>* [Impostazioni posizionamento](/help/dsp/campaign-management/placements/placement-settings.md)
> * [Come DSP Ottimizza Le Campagne](optimization-how-dsp-optimizes-campaigns.md)
>* [Obiettivi di ottimizzazione e modalità di utilizzo](optimization-goals.md)
>* [Filtri pre-offerta a livello di posizionamento e modalità di utilizzo](optimization-pre-bid-filters.md)
>* [Elenco di controllo per il lancio di Campaign](/help/dsp/campaign-management/campaign-launch-checklist.md)
