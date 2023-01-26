---
title: Tecniche consigliate per l’impostazione di campagne sulle prestazioni
description: Scopri le best practice per l’impostazione di campagne incentrate sulle prestazioni, che includono posizionamenti ottimizzati per il CPA più basso o il ROAS più alto.
feature: DSP Optimization, DSP Best Practices
exl-id: fc64680d-9d1c-4f74-a8b9-2e9b670c00eb
source-git-commit: 1c13874967ec4ad264e5fa6a5e0dfeb6120f53cc
workflow-type: tm+mt
source-wordcount: '1247'
ht-degree: 0%

---

# Tecniche consigliate per l’impostazione di campagne sulle prestazioni

DSP ottimizzare le campagne incentrate sulle prestazioni per i posizionamenti con il costo per acquisizione più basso (CPA) o con il più alto ritorno sulla spesa pubblicitaria (ROAS).

Consulta le seguenti best practice per le campagne sulle prestazioni:

* Passaggio 1: definire l’obiettivo
* Passaggio 2: definire la strategia
* Passaggio 3 - Creare pacchetti
* Passaggio 4 - Creare una struttura di posizionamento
* Passaggio 5: utilizzare le risorse creative giuste

## Passaggio 1: Definire L’Obiettivo

È importante capire se l&#39;obiettivo della campagna è quello di raggiungere il ROAS più alto possibile o il CPA più basso possibile. Per ogni pacchetto della campagna, specificherai l’obiettivo di conseguenza come *[!UICONTROL Highest ROAS - Custom Goal]* o *[!UICONTROL Lowest CPA - Custom Goal]*.

![obiettivo di ottimizzazione](/help/dsp/assets/optimization-goals.png)

È inoltre necessario determinare gli eventi di successo che porteranno all’obiettivo generale e creare obiettivi personalizzati di conseguenza. Per ogni pacchetto, specifichi un obiettivo personalizzato da utilizzare con l’obiettivo di ottimizzazione generale per la generazione di rapporti e l’ottimizzazione algoritmica utilizzando [!DNL Adobe Sensei]. Per ulteriori informazioni sulla creazione di obiettivi personalizzati, consulta la sezione [Tecniche consigliate per la creazione di un obiettivo personalizzato](custom-goal-best-practices.md).

![obiettivi personalizzati](/help/dsp/assets/objective-goals.png)

## Passaggio 2: definire la strategia

### Strategie di prospettiva

I pacchetti funnel superiore includono posizionamenti con targeting molto ampio per raggiungere nuovi consumatori netti.

#### Strategie di posizionamento consigliate per la prospettiva

* Trova nuovi tipi di pubblico che è probabile convertire utilizzando le seguenti tattiche:

   * Modellazione lookalike da una piattaforma di gestione dati (DMP), come Adobe Audience Manager.
   * Targeting comportamentale tramite dati di terze parti.
   * Targeting contestuale.
   * Targeting sito/categoria.

* Utilizzare il targeting di esecuzione della rete (RON): È importante includere una serie di posizioni di rete senza targeting del pubblico e con un ampio targeting di inventario. Ciò consente di [!DNL Adobe Sensei] per trovare utenti importanti che potrebbero disporre di cookie più recenti che non sono ancora stati suddivisi in categorie in un pubblico.

### Strategie di retargeting

I pacchetti funnel inferiori includono posizionamenti destinati agli utenti che sono già stati sulla pagina web dell’inserzionista o per i quali l’inserzionista dispone di dati CRM.

#### Strategie di posizionamento consigliate per il retargeting

* Se l’inserzionista è un cliente Adobe Analytics o Adobe Audience Manager, puoi creare segmenti di prime parti (come visitatori della homepage, pagine di prodotto o utenti che abbandonano il carrello) e utilizzarli come target di posizionamento in DSP.

* Evita di assegnare troppo budget a un posizionamento mirato al pubblico. Come regola generale, il budget di 30 dollari per 1.000 utenti al mese.

## Passaggio 3 - Creare pacchetti

La best practice prevede la creazione di pacchetti separati per la prospezione di funnel superiore e per il retargeting di funnel inferiore. L’ottimizzazione si verifica a livello di pacchetto, in modo che i dati sulle prestazioni di tutti i posizionamenti all’interno di un pacchetto vengano raggruppati. Pertanto, raggruppare posizionamenti in pacchetti con prestazioni attese simili.

![esempio di pacchetti separati per la ricerca e il retargeting](/help/dsp/assets/p-r.png)

Inoltre, utilizza le seguenti impostazioni.

### Obiettivi e budget

* **Imballaggio e maschiatura:** Per selezionare un obiettivo di ottimizzazione CPA o ROAS, il pacchetto deve utilizzare la velocità a livello di pacchetto. In questo modo, tutti i posizionamenti all’interno del pacchetto vengono ottimizzati per distribuire la spesa in base alle prestazioni e alla scala fino agli obiettivi selezionati.

* **Date di volo:** (Pacchetti di profilazione) Quando la campagna viene eseguita per più di 25 giorni, utilizza il [!UICONTROL Activate Custom Flighting] funzionalità. Innanzitutto, imposta un volo personalizzato per i primi 10 giorni a circa il 75% del budget giornaliero necessario per ridurre la spesa durante il *fase di apprendimento*. Quindi impostare un secondo volo personalizzato per il resto del budget.

   Ad esempio, se hai 100.000 $ da spendere in 30 giorni, imposta il budget per il volo 1 (giorni 1-10) a 25.000 $ (75% x $ 100.000/30 giorni = $ 2.500 al giorno). Utilizza il budget rimanente di $75.000 per il volo 2 (Giorni 11-30).

* **Bilancio:** DSP sempre cercare di allocare il 100% del budget del pacchetto in modo uniforme tra tutti i posizionamenti in un pacchetto. Se un posizionamento ha una spesa bassa o nessuna spesa, si consiglia di limitare il budget al posizionamento per consentire a più budget di essere allocato a posizionamenti con scala. Consente di calibrare 24-48 ore per le modifiche al budget.

* **Obiettivi di ottimizzazione:** Utilizzare uno dei due obiettivi di ottimizzazione delle prestazioni, *[!UICONTROL Highest ROAS]* o *[!UICONTROL Lowest CPA]*, a seconda dell’obiettivo del pacchetto. Questi obiettivi ottimizzano automaticamente il pacchetto verso i posizionamenti di ROAS più alti o CPA più bassi, rispettivamente.

* **Obiettivi personalizzati:**
   * Se un nuovo pacchetto ha lo stesso obiettivo di un pacchetto esistente, puoi facoltativamente collegare il pacchetto esistente in modo che l&#39;algoritmo possa utilizzare i dati di apprendimento automatico esistenti.
   * Inserire il valore appropriato [!UICONTROL Target CPA] o [!UICONTROL Target ROAS].

* **Imballaggio dei voli e imballaggio infragiornaliero:** Per entrambi i tipi di riempimento, seleziona *[!UICONTROL Even]* per massimizzare i tuoi obiettivi prestazionali, effettuando un passo uniforme durante tutto il giorno e per tutto il volo.

   >[!CAUTION]
   >
   >Utilizzo *[!UICONTROL FrontLoad]* e *[!UICONTROL Aggressive Front Load]* per voli in volo e *[!UICONTROL ASAP]* valutazione dei percorsi infragiornalieri solo quando si assegna priorità complete alla consegna e alla spesa rispetto all’ottimizzazione delle prestazioni, in quanto tali strategie possono influire negativamente sui KPI delle prestazioni desiderati.

## Passaggio 4 - Creare una struttura di posizionamento

Meno è di più. Se è possibile impostare meno di sei posizionamenti per pacchetto, il budget disponibile può passare in modo dinamico ai posizionamenti con le prestazioni migliori più facilmente.

Inoltre, assicurati di aggiungere ogni posizionamento a un pacchetto con un tipo di obiettivo del pacchetto di *[!UICONTROL Prospecting]* o *[!UICONTROL Retargeting]*, se del caso.

Di seguito sono riportate le impostazioni di posizionamento consigliate per le campagne sulle prestazioni.

### Obiettivi

Puoi configurare l’ottimizzazione CPA o ROAS a livello di pacchetto (consulta il Passaggio 3 - Creazione di pacchetti), ma puoi aggiungere impostazioni aggiuntive a livello di posizionamento.

* **Offerta massima:**
   * Per la ricerca di posizionamenti, utilizza un&#39;offerta massima bassa ($5).
   * Per i posizionamenti di retargeting, utilizza un’offerta massima elevata ($12).

* **Filtri pre-offerta:** Riduci al minimo o evita idealmente l’impostazione di filtri preventivi aggressivi che impediscono al posizionamento di raggiungere una scala. Le best practice includono:

   * Utilizza un filtro (1) pre-bid per posizionamento. Per poter utilizzare più filtri prebid, è necessario che entrambi siano soddisfatti, il che riduce la scala.

   * Prendi in considerazione l’impostazione di filtri pre-bid meno rigorosi nei casi in cui viene applicato un targeting aggiuntivo (ad esempio pubblico, geo e targeting del sito).

Consulta le descrizioni di quando utilizzare ogni filtro pre-bid in [Filtri di pre-offerta a livello di posizionamento e modalità di utilizzo](/help/dsp/optimization/optimization-pre-bid-filters.md).

### Inventario

Per massimizzare la scala, utilizza [!UICONTROL Public] (Open Exchange) e [!UICONTROL On Demand] inventario.

### Targeting del sito

* **[!UICONTROL Traffic Type]**: [!UICONTROL Websites] only
* **[!UICONTROL Site Tier]**: [!UICONTROL All sites]

### Targeting del pubblico

<!-- Say something about limiting unnecessary constraints/limitations, including dayparting, which limit your chances for ad exposure. Use only when it's required for your audience. -->

* **[!UICONTROL Included Audiences]:**
   * Per la ricerca di posizionamenti, raggruppare categorie di pubblico simili e dimensioni di pubblico simili in un unico posizionamento. Quindi, in base alle prestazioni, effettua una delle seguenti operazioni:
      * Rimuovi i tipi di pubblico con prestazioni inferiori dai posizionamenti esistenti.
      * Sposta i tipi di pubblico con prestazioni migliori in un posizionamento separato per controllare meglio i budget.
   * Per i posizionamenti di retargeting, è consigliabile includere un segmento di pubblico per posizionamento per controllare facilmente le offerte e il budget.

>[!NOTE]
>
>I tuoi annunci avranno prestazioni migliori se un utente può essere raggiunto con un solo posizionamento. Una sovrapposizione significativa degli utenti tra i posizionamenti può causare concorrenza, che produce un ciclo di offerte in continuo aumento, aumentando il costo per utente. Pertanto, se includi più tipi di pubblico, assicurati che non siano composti da utenti/membri del pubblico sovrapposti.
>
> Puoi evitare la sovrapposizione di tipi di pubblico creando i tipi di pubblico su più livelli in modo da eliminare i livelli superiori e più inclusivi dai posizionamenti in base alle esigenze.

* **[!UICONTROL Frequency Capping]:**
   * Per la ricerca di posizionamenti, utilizzare tappi di frequenza stretti (un&#39;impression al giorno).
   * Per i posizionamenti di retargeting, imposta il limite di posizionamento primario su 6-10 impression al giorno e il limite secondario su un’impression all’ora.

* **[!UICONTROL Device Targeting]**:
   * Includi [!UICONTROL Computer], [!UICONTROL Mobile]e [!UICONTROL Tablet].
   * Non eseguire il targeting [!UICONTROL Firefox] e [!UICONTROL Safari] a causa di limitazioni di targeting e misurazione. Contatta il tuo [!DNL Adobe] team di account per ulteriori informazioni [!DNL Adobe] supporto per [!DNL Safari ITP].
   * Se esegui il targeting del traffico web mobile, disattiva tutti i browser mobili eccetto [!UICONTROL Chrome] e [!UICONTROL Edge].

### Sicurezza del marchio e qualità dei supporti

Utilizzo di filtri contestuali, blocco della frode pre-offerta e/o [!UICONTROL Ads.txt] Il filtro limiterà la scala dei posizionamenti, ma utilizzali se necessario.

## Passaggio 5: utilizzare le risorse creative giuste

* La best practice prevede di includere il maggior numero possibile di dimensioni di annunci univoci per massimizzare la portata. Il modello di visualizzazione universale ti consente di caricare qualsiasi dimensione standard di annunci display.
* Assicurati che tutti i posizionamenti contengano *almeno* tutte le dimensioni degli annunci display principali (300x250, 728x90, 160x600, 300x600, 320x50 e 300x50).
* Aggiorna spesso i creativi per evitare l&#39;affaticamento creativo.

>[!MORELIKETHIS]
>
>* [Impostazioni pacchetto](/help/dsp/campaign-management/packages/package-settings.md)
>* [Impostazioni di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md)
> * [Ottimizzazione DSP campagne](optimization-how-dsp-optimizes-campaigns.md)
>* [Obiettivi di ottimizzazione e come utilizzarli](optimization-goals.md)
>* [Filtri di pre-offerta a livello di posizionamento e modalità di utilizzo](optimization-pre-bid-filters.md)
>* [Elenco di controllo per Campaign Launch](/help/dsp/campaign-management/campaign-launch-checklist.md)

