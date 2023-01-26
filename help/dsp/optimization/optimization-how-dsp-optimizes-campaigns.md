---
title: Ottimizzazione DSP campagne
description: Scopri come DSP ottimizzare i pacchetti nelle campagne.
feature: DSP Optimization
exl-id: 054582ef-b677-4725-b25c-b82bf3e5b43e
source-git-commit: 1c13874967ec4ad264e5fa6a5e0dfeb6120f53cc
workflow-type: tm+mt
source-wordcount: '681'
ht-degree: 0%

---

# Come la pubblicità DSP ottimizza le campagne

Questa pagina illustra come il motore di ottimizzazione DSP, alimentato da [!DNL Adobe Sensei], ottimizza i pacchetti nelle campagne. Per suggerimenti e trucchi su come ottimizzare manualmente le campagne, contatta il tuo [!DNL Adobe] team di account. <!-- add link to trading playbook if we add it to help -->

Gli obiettivi di ottimizzazione dei pacchetti funzionano a due livelli:

* Per ogni pacchetto: DSP assegna il budget a ogni posizionamento all’interno del pacchetto in base alle prestazioni del posizionamento rispetto al KPI selezionato.

* Per ogni collocamento/asta nell&#39;imballaggio: DSP calcola il valore KPI economico in tempo reale per ogni asta per posizionamento, quindi utilizza questo valore per determinare l’offerta.

   >[!NOTE]
   >
   >Il valore economico può essere pesantemente ponderato in base a quanto bene un posizionamento è la spesa. Se un posizionamento è dietro il suo obiettivo di spesa, allora sarà permesso di acquistare aste di qualità inferiore. Se un posizionamento soddisfa facilmente il suo obiettivo di spesa, allora si concentrerà su aste di qualità più elevata.

## Ottimizzazione dei pacchetti

DSP ottimizzare la consegna in due modi fondamentali, con 20 varianti disponibili per allinearsi al tuo obiettivo di prestazioni specifico. Puoi scegliere di:

* Dare priorità al tasso di prestazioni

* Dare priorità al bilanciamento dell&#39;efficienza dei costi con il tasso di prestazioni

Vedi [Obiettivi di ottimizzazione e come utilizzarli](optimization-goals.md) per determinare quale obiettivo di ottimizzazione ti aiuterà a raggiungere i KPI.

### Pacchetti che assegnano priorità alla velocità di prestazione

Per gli obiettivi di ottimizzazione che definiscono la priorità del tasso di prestazioni, DSP prevede le prestazioni di ogni asta e sempre le offerte all&#39;offerta massima. Esempi di obiettivi di ottimizzazione applicabili includono [!UICONTROL Highest Viewability Rate], [!UICONTROL Highest Clickthrough Rate]e così via.

Questa modalità di ottimizzazione funziona bene se:

* Conoscete già il livello CPM effettivo/accettabile (ad esempio, un valore di riferimento storico).

* Sei disposto a regolare manualmente il [!UICONTROL Max Bid] per ogni posizionamento, in caso di problemi di scalabilità.

* State dando la priorità alla scala rispetto all&#39;efficienza.

#### Logica di imballaggio {#pacing-logic-performance}

* Se la spesa è al passo, le offerte diventeranno più selettive, in modo da fare solo offerte sulle aste previste per avere alti tassi di performance.

* Se la spesa è in ritardo, le offerte diventeranno meno selettive, in modo da poter fare offerte sulle aste prevedibilmente avere tassi di prestazioni inferiori al fine di raggiungere l&#39;obiettivo di pacing.

#### Ombreggiatura prezzo/offerta di compensazione {#clearing-price-performance}

Dopo aver eseguito la logica di valutazione, DSP esegue l&#39;offerta proposta attraverso un modello di previsione del prezzo di compensazione. Se la previsione indica che l&#39;offerta può essere abbassata con una diminuzione minima al tasso di vincita, allora l&#39;offerta è diminuita in base alla previsione.

### Pacchetti che attribuiscono priorità all&#39;efficienza dei costi di bilanciamento con il tasso di prestazioni

Per alcuni obiettivi di ottimizzazione, DSP prevede le prestazioni di ogni asta e regola automaticamente i prezzi delle offerte, mai superando di un posizionamento [!UICONTROL Max Bid]. Esempi di obiettivi di ottimizzazione applicabili includono [!UICONTROL Lowest CPM], [!UICONTROL Lowest CPA], [!UICONTROL Lowest Cost per View], [!UICONTROL Lowest Cost per Click]e così via.

#### Logica di imballaggio {#pacing-logic-balanced}

* Se la spesa è al passo, allora DSP diventa più sensibile al prezzo, le offerte più basse per il commercio di tasso di vincita con il piano di pacing.

* Se anche una metrica delle prestazioni viene bilanciata (tutti gli obiettivi eccetto [!UICONTROL Lowest CPM]), quindi il KPI previsto viene miscelato nell’importo dell’offerta. Pertanto, per le aste che si prevede saranno più performanti in base al &quot;costo per&quot;.

* Se la spesa è in ritardo, allora DSP diventa meno sensibile ai prezzi e le offerte più elevate, fino a [!UICONTROL Max Bid], per scambiare il tasso di vincita con il piano di pacing.

#### Ombreggiatura prezzo/offerta di compensazione {#clearing-price-balanced}

Dopo aver eseguito la logica di valutazione, DSP esegue l&#39;offerta proposta attraverso un modello di previsione del prezzo di compensazione. Se la previsione indica che l&#39;offerta può essere abbassata con una diminuzione minima al tasso di vincita, allora l&#39;offerta è diminuita in base alla previsione.

## Ottimizzazione del posizionamento

I filtri di pre-offerta di posizionamento sono il modo più rigoroso per garantire prestazioni elevate. DSP utilizza filtri pre-offerta strategicamente tra diversi tipi di annunci per raggiungere obiettivi di prestazioni tra i posizionamenti all’interno di ciascun pacchetto. Puoi utilizzare i filtri pre-bid contemporaneamente con l’ottimizzazione a livello di pacchetto o in modo indipendente.

>[!NOTE]
>
>I filtri per offerte precedenti disponibili variano a seconda del tipo di annuncio. Ad esempio, per un posizionamento standard dello schermo, è possibile filtrare in base al tasso di click-through e alla visualizzabilità ma non in base al tasso di completamento.

Vedi [Filtri di pre-offerta a livello di posizionamento e modalità di utilizzo](optimization-pre-bid-filters.md) per determinare quale filtro pre-bid ti aiuterà a raggiungere i KPI.

>[!MORELIKETHIS]
>
>* [Impostazioni pacchetto](/help/dsp/campaign-management/packages/package-settings.md)
>* [Impostazioni di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Obiettivi di ottimizzazione e come utilizzarli](optimization-goals.md)
>* [Filtri di pre-offerta a livello di posizionamento e modalità di utilizzo](optimization-pre-bid-filters.md)
>* [Risoluzione dei problemi relativi alle prestazioni](/help/dsp/optimization/troubleshooting-performance.md)

