---
title: Layout dell’albero delle decisioni
description: Scopri gli editor di alberi decisionali manuali e basati sull’intelligenza artificiale per le esperienze con il targeting.
feature: Creative Experiences
exl-id: 1d997422-8177-4a6b-b56a-e1c742b96ad2
TQID: 'https://experienceleague.adobe.com/JFrcVBHxv90Fchk-VfkmxAITQJswboszNMFOfaAQlL4'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
subfeature_v2:
  - id: f1a0ef49-c5d6-4fdf-b0dc-ae6685afe30b
    internal-label: Creative experiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 8a75f4a164b25ed8e73816c3d853d9650f470118
workflow-type: tm+mt
source-wordcount: '807'
ht-degree: 0%
---
# Layout dell&#39;albero delle decisioni per [!DNL Creative] esperienze

Quando abiliti l&#39;opzione &quot;[!UICONTROL Targeting]&quot; per un&#39;esperienza, configurala utilizzando una struttura decisionale.

Inizialmente, ogni albero decisionale inizia con il livello principale, &quot;All&quot;. Puoi aggiungere uno o più nodi di destinazione e quindi assegnare bundle creativi ai nodi finali in ogni ramo della struttura decisionale.

## Editor basato sull’intelligenza artificiale (Beta) {#ai-editor}

L’editor basato sull’intelligenza artificiale si apre per impostazione predefinita quando crei o modifichi un’esperienza con il targeting. Combina una conversazione con l’agente di intelligenza artificiale e un’area di lavoro interattiva dell’albero decisionale.

* Descrivi la struttura di targeting o le modifiche desiderate nella conversazione e controlla la struttura risultante prima di salvarla.

* Modifica l’area di lavoro direttamente per aggiungere livelli e nodi di destinazione, assegnare bundle e configurare URL di ottimizzazione creativa e tracciamento. Non è necessario passare all&#39;editor manuale per utilizzare questi controlli.

* Visualizza il nome dell’esperienza, lo stato e l’inserzionista nell’intestazione e, se disponibile, utilizza gli ID nodo per identificare i nodi di destinazione quando descrivi le modifiche.

* Utilizza **[!UICONTROL Zoom in]**, **[!UICONTROL Zoom out]** e **[!UICONTROL Change orientation]** per modificare la visualizzazione. **[!UICONTROL Reset tree]** cancella la struttura dopo la conferma; non reimposta solo lo zoom.

Durante l&#39;elaborazione di una modifica da parte dell&#39;assistente, l&#39;area di lavoro e il relativo pulsante **[!UICONTROL Save]** sono temporaneamente disabilitati. Attendi il completamento dell’elaborazione prima di apportare un’altra modifica all’area di lavoro.

## Editor manuale {#manual-editor}

Per aprire l&#39;editor manuale esistente dall&#39;editor basato su IA, fare clic su **[!UICONTROL Manual Decision Tree]**. È inoltre possibile selezionare **[!UICONTROL Create Decision Tree Manually (Legacy)]** dalle azioni dell&#39;esperienza nella visualizzazione [!UICONTROL Experiences]. Consulta [Cambiare editor o modificare le impostazioni dell&#39;esperienza](experience-edit-targeting.md#switch-editors).

Nell&#39;editor manuale, la struttura viene visualizzata in verticale per impostazione predefinita. È possibile passare a una vista orizzontale e regolare lo zoom con un dispositivo di scorrimento. Le impostazioni di visualizzazione vengono salvate fino alla disconnessione.

Gli esempi seguenti mostrano l’editor manuale:

![Esempio di struttura decisionale verticale senza destinazioni](/help/creative/assets/experience-decision-tree-no-targets.png "Esempio di struttura decisionale verticale senza destinazioni")

![Esempio di struttura decisionale orizzontale senza destinazioni](/help/creative/assets/experience-decision-tree-no-targets-horizontal.png "Esempio di struttura decisionale orizzontale senza destinazioni")

>[!IMPORTANT]
>
>Salva le modifiche da mantenere prima di uscire dall’editor basato sull’intelligenza artificiale. Facendo clic su **[!UICONTROL Manual Decision Tree]**, **[!UICONTROL Experience Form]** o **[!UICONTROL Cancel]** viene aperta una finestra di dialogo di conferma. Se si fa clic su **[!UICONTROL Yes]**, le modifiche alla struttura non salvate vengono ignorate; se si fa clic su **[!UICONTROL No]**, l&#39;utente rimane nell&#39;editor.

## Termini

**Struttura:** La struttura decisionale complessiva come struttura ad albero con rami.

**Nodo di destinazione:** una destinazione all&#39;interno di un ramo.

**Nodo foglia:** un insieme di creatività assegnate a un nodo di destinazione finale.

## Destinazioni in un albero decisionale

Ogni albero decisionale può avere fino a cinque livelli di target. I target a livello di esperienza vengono applicati insieme alle opzioni di targeting del tuo DSP; il comportamento di targeting gerarchico può variare a seconda di DSP. Assicurati che le esperienze dell’annuncio includano un targeting compatibile con le campagne in cui lo implementerai.

Ogni livello di destinazione può includere più rami, ciascuno con uno o più nodi con lo stesso tipo di destinazione (segmento di pubblico, tipo di posizione geografica, valori per chiavi di passaggio dati specificate, attributi per un pixel di retargeting specificato o una categoria di dispositivi). Puoi assegnare ai nodi di destinazione di livello inferiore dei bundle creativi in ogni dimensione dell’annuncio per la quale hai specificato un’immagine creativa o creativa video predefinita.

<!-- Add a screen shot of the AI editor -->L’esempio seguente mostra le destinazioni nell’editor manuale:

![Esempio di struttura decisionale con destinazioni](/help/creative/assets/experience-decision-tree.png "Esempio di struttura decisionale con destinazioni")

Quando si aggiunge un nodo di destinazione al livello finale, si specifica la destinazione per il nuovo nodo. Un ulteriore nodo di pari livello, &quot;Tutto il resto&quot;, viene creato automaticamente per tutti coloro che non corrispondono alla destinazione specificata. È quindi possibile aggiungere altri nodi di pari livello con destinazioni diverse dello stesso tipo.

Quando si inserisce un nodo di destinazione tra i livelli esistenti, tuttavia, il primo nodo per il nuovo livello viene inizialmente assegnato a &quot;All&quot; (Tutti). Per identificare una destinazione specifica, creare un nodo di destinazione di pari livello allo stesso livello, per il quale si specifica la destinazione effettiva. Questa azione crea il nodo di destinazione e sostituisce il nodo &quot;All&quot; con un nodo &quot;Everything Else&quot; (che include tutti i bundle creativi precedentemente assegnati a All). È quindi possibile aggiungere altri nodi di pari livello con destinazioni diverse dello stesso tipo.

Per tutti i nodi principali, puoi facoltativamente copiare tutti i nodi di destinazione secondari e i bundle creativi e incollarli in un altro nodo allo stesso livello. È possibile aggiungere i nodi incollati al framework esistente o sostituirli con il framework esistente.

## Creativi in un albero decisionale

Assegna bundle creativi a ogni nodo di destinazione finale nell’esperienza.

All’interno di ogni nodo con bundle creativi, puoi facoltativamente ruotare i creativi inclusi a) algoritmicamente per ottimizzare il tasso di click-through o un obiettivo personalizzato, b) in base a pesi specifici, o c) in una sequenza specifica. Facoltativamente, è anche possibile ruotare i creativi in una sequenza temporale specifica o in una combinazione delle stesse opzioni.

Facoltativamente, puoi personalizzare gli URL della pagina di destinazione, degli URL di tracciamento delle impression e degli URL di tracciamento dei clic, in base alle esigenze dei singoli creativi. <!-- Not in the UI as of 1/31: For flexible HTML5 creatives, you can customize any of the flexible attributes. -->

>[!MORELIKETHIS]
>
>* [Informazioni sulle esperienze in Advertising Creative 2.0](experience-about.md)
>* [Crea un&#39;esperienza con il targeting](/help/creative/experiences/experience-create-targeting.md)
>* [Impostazioni esperienza di destinazione](/help/creative/experiences/experience-settings-targeting.md)
