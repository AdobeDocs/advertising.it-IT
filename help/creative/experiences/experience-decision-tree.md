---
title: Layout dell’albero delle decisioni
description: Scopri il layout della struttura decisionale per le esperienze con targeting.
feature: Creative Experiences
exl-id: 1d997422-8177-4a6b-b56a-e1c742b96ad2
source-git-commit: 3c1316fa898e5773fbf1763733e388c9ed3bd389
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 0%

---

# Layout dell&#39;albero delle decisioni per [!DNL Creative] esperienze

*Versione beta chiusa*

Quando abiliti l&#39;opzione &quot;[!UICONTROL Targeting]&quot; per un&#39;esperienza, configurala utilizzando una struttura decisionale.

Inizialmente, ogni albero decisionale inizia con il livello principale, &quot;All&quot;. Puoi aggiungere uno o più nodi di destinazione e quindi assegnare bundle creativi ai nodi finali in ogni ramo della struttura decisionale. Per impostazione predefinita, l’albero delle decisioni viene visualizzato in verticale, ma è possibile visualizzare facoltativamente l’albero in orizzontale.

![Esempio di struttura decisionale verticale senza destinazioni](/help/creative/assets/experience-decision-tree-no-targets.png "Esempio di struttura decisionale verticale senza destinazioni")

![Esempio di struttura decisionale orizzontale senza destinazioni](/help/creative/assets/experience-decision-tree-no-targets-horizontal.png "Esempio di struttura decisionale orizzontale senza destinazioni")

<!--
>[!NOTE]
>
>You can optionally assign creative bundles to the root level, without targets. However, the [XXXX workflow](experience-create-no-targeting.md) XXXXX is better XXX.<!-- Explain the diff and why to choose the other option. -->
-->

## Termini

**Struttura:** La struttura decisionale complessiva come struttura ad albero con rami.

**Nodo di destinazione:** una destinazione all&#39;interno di un ramo.

**Nodo foglia:** un insieme di creatività assegnate a un nodo di destinazione finale.

## Destinazioni in un albero decisionale

Ogni albero decisionale può avere fino a cinque livelli di target. Ogni livello di destinazione può includere più rami, ciascuno con uno o più nodi con lo stesso tipo di destinazione (segmento di pubblico, tipo di posizione geografica, valori per chiavi di passaggio dati specificate, attributi per un pixel di retargeting specificato o una categoria di dispositivi). Puoi assegnare pacchetti creativi a ogni dimensione di annuncio per la quale hai specificato un&#39;immagine creativa predefinita ai nodi di destinazione di livello più basso.

![Esempio di struttura decisionale con destinazioni](/help/creative/assets/experience-decision-tree.png "Esempio di struttura decisionale con destinazioni")

Quando si aggiunge un nodo di destinazione al livello finale, si specifica la destinazione per il nuovo nodo. Un ulteriore nodo di pari livello, &quot;Tutto il resto&quot;, viene creato automaticamente per tutti coloro che non corrispondono alla destinazione specificata. È quindi possibile aggiungere altri nodi di pari livello con destinazioni diverse dello stesso tipo.

Quando si inserisce un nodo di destinazione tra i livelli esistenti, tuttavia, il primo nodo per il nuovo livello viene inizialmente assegnato a &quot;All&quot; (Tutti). Per identificare una destinazione specifica, creare un nodo di destinazione di pari livello allo stesso livello, per il quale si specifica la destinazione effettiva. Questa azione crea il nodo di destinazione e sostituisce il nodo &quot;All&quot; con un nodo &quot;Everything Else&quot; (che include tutti i bundle creativi precedentemente assegnati a All). È quindi possibile aggiungere altri nodi di pari livello con destinazioni diverse dello stesso tipo.

Per tutti i nodi principali, puoi facoltativamente copiare tutti i nodi di destinazione secondari e i bundle creativi e incollarli in un altro nodo allo stesso livello. È possibile aggiungere i nodi incollati al framework esistente o sostituirli con il framework esistente.

## Creativi in un albero decisionale

Assegna bundle creativi a ogni nodo di destinazione finale nell’esperienza.

All’interno di ogni nodo con bundle creativi, puoi facoltativamente ruotare i creativi inclusi a) in base a pesi specificati o b) algoritmicamente per ottimizzare il tasso di click-through o un obiettivo personalizzato. È inoltre possibile ruotare i creativi in una sequenza temporale specifica utilizzando le stesse opzioni.

Facoltativamente, puoi personalizzare gli URL della pagina di destinazione, degli URL di tracciamento delle impression e degli URL di tracciamento dei clic, in base alle esigenze dei singoli creativi. <!-- Not in the UI as of 1/31: For flexible HTML5 creatives, you can customize any of the flexible attributes. -->

>[!MORELIKETHIS]
>
>* [Informazioni sulle esperienze in Advertising Creative 2.0](experience-about.md)
>* [Crea un&#39;esperienza con il targeting](/help/creative/experiences/experience-create-targeting.md)
>* [Impostazioni esperienza di destinazione](/help/creative/experiences/experience-settings-targeting.md)
