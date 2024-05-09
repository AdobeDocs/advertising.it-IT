---
title: Come l’DSP ottimizza le campagne
description: Scopri come l’DSP ottimizza i pacchetti nelle campagne.
feature: DSP Optimization
exl-id: 92d411cf-4307-4449-97b4-da3817f2a0b4
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '679'
ht-degree: 0%

---

# Come Advertising DSP ottimizza le campagne

Questa pagina illustra come il motore di ottimizzazione DSP, basato su [!DNL Adobe Sensei], ottimizza i pacchetti nelle campagne. Per suggerimenti su come ottimizzare manualmente le campagne, contatta il team del tuo account Adobe. <!-- add link to trading playbook if we add it to help -->

Gli obiettivi di ottimizzazione dei pacchetti funzionano a due livelli:

* Per ogni pacchetto: l’DSP alloca il budget a ogni posizionamento all’interno del pacchetto in base alle prestazioni del posizionamento rispetto all’indicatore KPI selezionato.

* Per ogni posizionamento/asta nel pacchetto: l’DSP calcola il valore dell’indicatore KPI economico in tempo reale per ogni posizionamento e quindi utilizza questo valore per determinare l’offerta.

  >[!NOTE]
  >
  >Il valore economico può essere pesantemente ponderato in base a quanto bene un collocamento è spesa. Se un posizionamento è dietro il suo obiettivo di spesa, allora è permesso acquistare aste di qualità inferiore. Se un posizionamento soddisfa facilmente il suo obiettivo di spesa, allora l&#39;attenzione si sposta su aste di qualità più elevata.

## Ottimizzazione dei pacchetti

L’DSP può ottimizzare la distribuzione in due modi fondamentali, con 20 varianti disponibili per allinearsi all’obiettivo di prestazioni specifico. Puoi scegliere di:

* Assegnare la priorità al tasso di prestazioni

* Stabilire priorità per il bilanciamento dell&#39;efficienza dei costi con il tasso di prestazioni

Consulta [Obiettivi di ottimizzazione e modalità di utilizzo](optimization-goals.md) per determinare quale obiettivo di ottimizzazione ti aiuterà a raggiungere i tuoi KPI.

### Pacchetti che assegnano priorità al tasso di prestazioni

Per gli obiettivi di ottimizzazione che danno priorità al tasso di prestazioni, l’DSP prevede le prestazioni di ogni asta e fa sempre offerte all’Offerta massima. Esempi di obiettivi di ottimizzazione applicabili includono [!UICONTROL Highest Viewability Rate], [!UICONTROL Highest Clickthrough Rate]e così via.

Questa modalità di ottimizzazione funziona correttamente se:

* Conosci già il livello CPM effettivo/accettabile (ad esempio, un benchmark storico).

* Sei disposto a regolare manualmente il [!UICONTROL Max Bid] per ogni posizionamento se si verificano problemi con la scalabilità.

* Stai dando priorità alla scalabilità rispetto all&#39;efficienza.

#### Logica di andamento {#pacing-logic-performance}

* Se la spesa è a ritmo sostenuto, le offerte diventano più selettive, in modo da fare offerte solo sulle aste che si prevede abbiano tassi di prestazioni elevati.

* Se la spesa è in ritardo, le offerte diventano meno selettive, in modo da fare offerte sulle aste che si prevede abbiano tassi di prestazioni inferiori per raggiungere l&#39;obiettivo di ritmo.

#### Cancellazione dell&#39;ombreggiatura del prezzo/offerta {#clearing-price-performance}

Dopo aver eseguito la logica di andamento, l&#39;DSP esegue l&#39;offerta proposta attraverso un modello di previsione del prezzo di compensazione. Se la previsione indica che l’offerta può essere ridotta con una riduzione minima al tasso di vincita, l’offerta viene diminuita in base alla previsione.

### Pacchetti che danno priorità al bilanciamento dell&#39;efficienza dei costi con il tasso di prestazioni

Per alcuni obiettivi di ottimizzazione, l’DSP prevede le prestazioni di ogni asta e regola automaticamente i prezzi delle offerte, senza mai superare i [!UICONTROL Max Bid]. Esempi di obiettivi di ottimizzazione applicabili includono [!UICONTROL Lowest CPM], [!UICONTROL Lowest CPA], [!UICONTROL Lowest Cost per View], [!UICONTROL Lowest Cost per Click]e così via.

#### Logica di andamento {#pacing-logic-balanced}

* Se la spesa è a ritmo sostenuto, l&#39;DSP diventa più sensibile ai prezzi, facendo offerte inferiori per scambiare il tasso di vincita con il piano di ritmo.

* Se viene bilanciata anche una metrica delle prestazioni (tutti gli obiettivi tranne [!UICONTROL Lowest CPM]), il KPI previsto viene miscelato nell&#39;importo che è l&#39;offerta. Di conseguenza, le offerte per le aste che si prevede saranno più performanti in base al &quot;costo per&quot; sono più alte.

* Se la spesa è in ritardo, l&#39;DSP diventa meno sensibile ai prezzi e presenta offerte più elevate, fino al [!UICONTROL Max Bid], per scambiare il tasso di vincita con il piano di velocità.

#### Cancellazione dell&#39;ombreggiatura del prezzo/offerta {#clearing-price-balanced}

Dopo aver eseguito la logica di andamento, l&#39;DSP esegue l&#39;offerta proposta attraverso un modello di previsione del prezzo di compensazione. Se la previsione indica che l’offerta può essere ridotta con una riduzione minima al tasso di vincita, l’offerta viene diminuita in base alla previsione.

## Ottimizzazione del posizionamento

I filtri pre-offerta di posizionamento sono il modo più rigido per garantire prestazioni elevate. L’DSP utilizza i filtri pre-offerta in modo strategico tra diversi tipi di annunci per raggiungere gli obiettivi di prestazioni per i posizionamenti all’interno di ciascun pacchetto. Puoi utilizzare i filtri di pre-offerta in concomitanza con l’ottimizzazione a livello di pacchetto o in modo indipendente.

>[!NOTE]
>
>I filtri di pre-offerta disponibili variano a seconda del tipo di annuncio. Ad esempio, per un posizionamento di visualizzazione standard, puoi filtrare in base al tasso di click-through e alla visualizzabilità, ma non in base al tasso di completamento.

Consulta [Filtri pre-offerta a livello di posizionamento e come utilizzarli](optimization-pre-bid-filters.md) per determinare quale filtro di pre-offerta ti aiuterà a ottenere i tuoi KPI.

>[!MORELIKETHIS]
>
>* [Impostazioni pacchetto](/help/dsp/campaign-management/packages/package-settings.md)
>* [Impostazioni di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Obiettivi di ottimizzazione e modalità di utilizzo](optimization-goals.md)
>* [Filtri pre-offerta a livello di posizionamento e come utilizzarli](optimization-pre-bid-filters.md)
>* [Risoluzione dei problemi relativi alle prestazioni](/help/dsp/optimization/troubleshooting-performance.md)
