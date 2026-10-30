---
title: Personalizzare l’ottimizzazione creativa e la pianificazione di un’esperienza
description: Scopri come configurare l’ottimizzazione e la pianificazione degli annunci per esperienze mirate.
feature: Creative Experiences
exl-id: 47d1a249-decd-4c3b-ac88-260488d5bcd2
TQID: 'https://experienceleague.adobe.com/gDBTQn7F0ZNeiEylTDA9HNgDockR6FHE3MSvr0bJaDM'
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
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 8a75f4a164b25ed8e73816c3d853d9650f470118
workflow-type: tm+mt
source-wordcount: '1244'
ht-degree: 0%
---
# Personalizza l’ottimizzazione creativa e la pianificazione per un’esperienza con il targeting della struttura decisionale

*Solo nodi di destinazione con creatività esistente*

Per impostazione predefinita, un’esperienza ottimizza la rotazione creativa per il tasso di click-through complessivo in tutti i bundle assegnati. È possibile personalizzare le impostazioni di rotazione o pianificare bundle specifici da eseguire durante i periodi di tempo sequenziali, con impostazioni di rotazione separate per ogni pianificazione.

>[!NOTE]
>
>Queste funzioni non sono disponibili per i nodi che utilizzano le creatività predefinite anziché quelle assegnate.

Puoi configurare queste impostazioni direttamente nell’area di lavoro dell’editor basato sull’intelligenza artificiale (Beta) o nell’editor manuale. In entrambi gli editor, il salvataggio della finestra di dialogo del bundle aggiorna la struttura di lavoro; devi anche [salvare l&#39;esperienza](#save) dall&#39;intestazione della struttura.

## Impostazioni di rotazione {#rotation-settings}

* **[!UICONTROL Weighted]:** mostra le varianti di annunci nei bundle creativi associati in base al peso relativo.

* **[!UICONTROL Algorithmic]:** mostra più spesso le varianti di annunci più efficaci, in base a un obiettivo di ottimizzazione specificato, ad esempio il tasso di click-through o un obiettivo personalizzato di Advertising DSP.

* **[!UICONTROL Sequence] (editor basato su IA) o [!UICONTROL Sequencing] (editor manuale):** mostra i bundle creativi associati in un ordine specificato, con un numero specificato di impression per ogni bundle nella sequenza. Per impostazione predefinita, i bundle sono sequenziati nell’ordine in cui sono stati aggiunti all’esperienza. Le dimensioni degli annunci offerti sono determinate dall’inventario disponibile. Il bundle finale può essere utilizzato indefinitamente (impostazione predefinita), oppure la sequenza può tornare al primo bundle.

  Ad esempio, una sequenza può servire varianti di annunci dal bundle 1 per tre impression, dal Bundle 2 per una impression e dal Bundle 3 per due impression e quindi ripetere. Senza cicli continui, il bundle 3 continua a essere utilizzato indefinitamente.

## Configurare l’ottimizzazione creativa senza pianificare

Quando la pianificazione creativa è disabilitata, le impostazioni di ottimizzazione creativa si applicano a tutti i creativi assegnati.

### Utilizzo dell’editor basato sull’intelligenza artificiale (Beta) {#without-scheduling-ai}

1. Durante la [creazione](experience-create-targeting.md#ai-editor) o la [modifica](experience-edit-targeting.md#ai-editor) dell&#39;esperienza, fai clic su **[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]** nel nodo foglia creativa.

   Per un nodo finale senza bundle, fai clic su **[!UICONTROL Assign Bundles]** e [assegna prima i bundle](experience-assign-creative-bundles.md#ai-editor).

1. Apri la scheda **[!UICONTROL Creative optimisation]**.

1. Disabilita **[!UICONTROL Schedule]**.

1. Seleziona il tipo di rotazione creativa e configurane le impostazioni:

   * **[!UICONTROL Weighted]:** Immettere il peso relativo per ogni riga del bundle. Il totale dei pesi deve essere 100. Per distribuire equamente i pesi, fare clic su **[!UICONTROL Apply equal weight]**.

   * **[!UICONTROL Algorithmic]:** Selezionare un&#39;opzione **[!UICONTROL Optimization goals]**. Se scegli un obiettivo personalizzato, seleziona l&#39;[obiettivo personalizzato di Advertising DSP](/help/dsp/optimization/custom-goal.md) esistente in **[!UICONTROL Custom objective]**.

   * **[!UICONTROL Sequence]:** Trascina i bundle nell&#39;ordine desiderato e immetti il numero di impression per ciascuna sequenza. Consenti a **[!UICONTROL Keep in loop]** di ripetere la sequenza o lasciala disabilitata per impostare le impression dell&#39;ultimo bundle su **[!UICONTROL Infinite]**.

1. Fare clic su **[!UICONTROL Save]** nella finestra di dialogo.

1. [Salva l&#39;esperienza](#save).

### Utilizzo dell’editor manuale {#without-scheduling-manual}

[Aprire l&#39;editor manuale](experience-edit-targeting.md#experience-open) prima di eseguire la procedura seguente.

1. Mentre [crei](experience-create-targeting.md) o [modifichi](experience-edit-targeting.md) l&#39;esperienza, apri le impostazioni di ottimizzazione creativa:

   1. Tenere premuto il cursore sul nodo foglia creativo sotto il nodo di destinazione ed effettuare le seguenti operazioni:

      * Per i bundle esistenti, fare clic su **[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]**.

      * Per i nuovi bundle, fai clic su **[!UICONTROL ...]** > **[!UICONTROL Assign Bundles]** e [assegna i bundle](experience-assign-creative-bundles.md).

   1. Fare clic sulla scheda **[!UICONTROL Creative Optimization]**.

1. Disabilita **[!UICONTROL Schedule]**.

1. Seleziona il tipo di rotazione creativa per le varianti di annunci nei bundle associati:

   * *[!UICONTROL Weighted]:* Immettere il peso di ciascun bundle come percentuale. Per applicare gli stessi pesi a tutti i bundle associati, fare clic su (![Applica peso uguale](/help/creative/assets/apply-equal-weight.png "Applica peso uguale")). La somma dei pesi di tutti i bundle selezionati deve essere pari a 100.

   * *[!UICONTROL Algorithmic]:* Per **[!UICONTROL Optimization Goal]**, selezionare *[!UICONTROL Click Through Rate]*, (esperienze annuncio video standard) *[!UICONTROL Completion Rate]* o *[!UICONTROL Custom Objective]*. Se selezioni *[!UICONTROL Custom Objective]*, seleziona un [obiettivo personalizzato di Advertising DSP](/help/dsp/optimization/custom-goal.md) esistente.

   * *[!UICONTROL Sequencing]:*

     1. Trascina e rilascia i bundle assegnati nell’ordine desiderato.

     1. Immetti il numero di impression per ciascuna sequenza.

     1. Per l&#39;ultima sequenza, modificare se in a\) visualizzare il bundle finale nella sequenza a tempo indefinito (*[!UICONTROL Infinite]* (impostazione predefinita) o b\) tornare al primo bundle dopo la visualizzazione del bundle finale (*[!UICONTROL Keep in Loop]*).

1. Fare clic su **[!UICONTROL Save]**.

## Configurare l’ottimizzazione creativa con la programmazione creativa

Facoltativamente, puoi pianificare l’esecuzione di specifici bundle creativi durante specifici periodi di tempo sequenziali tra le date di inizio e di fine dell’esperienza e applicare impostazioni di rotazione creativa personalizzate per ogni pianificazione. Ad esempio, puoi pianificare l’esecuzione del bundle 1 nelle prime due settimane per ottimizzare il tasso di click-through, e del bundle 2 nelle due settimane successive per ottimizzare un obiettivo personalizzato specifico.

Quando si utilizza la pianificazione, è necessario pianificare i bundle per tutta la durata dell’esperienza.

### Utilizzo dell’editor basato sull’intelligenza artificiale (Beta) {#with-scheduling-ai}

1. Durante la [creazione](experience-create-targeting.md#ai-editor) o la [modifica](experience-edit-targeting.md#ai-editor) dell&#39;esperienza, fai clic su **[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]** nel nodo foglia creativa.

   Per un nodo finale senza bundle, fai clic su **[!UICONTROL Assign Bundles]** e [assegna prima i bundle](experience-assign-creative-bundles.md#ai-editor).

1. Aprire la scheda **[!UICONTROL Creative optimisation]** e abilitare **[!UICONTROL Schedule]**.

1. Selezionare **[!UICONTROL Timezone]** per la pianificazione.

1. Per la prima programmazione:

   1. Seleziona la casella di controllo accanto a ciascun bundle da includere nella colonna sinistra.

   1. Specifica le date e le ore di inizio e fine.

   1. Seleziona il tipo di rotazione creativa e configurane le impostazioni:

      * **[!UICONTROL Weighted]:** Immettere il peso relativo per ogni riga del bundle nella pianificazione. Il totale dei pesi deve essere 100. Per distribuire equamente i pesi, fare clic su **[!UICONTROL Apply equal weight]**.

      * **[!UICONTROL Algorithmic]:** Selezionare un&#39;opzione **[!UICONTROL Optimization goals]**. Se scegli un obiettivo personalizzato, seleziona l&#39;[obiettivo personalizzato di Advertising DSP](/help/dsp/optimization/custom-goal.md) esistente in **[!UICONTROL Custom objective]**.

      * **[!UICONTROL Sequence]:** Trascina i bundle nell&#39;ordine desiderato e immetti il numero di impression per ciascuna sequenza. Consenti a **[!UICONTROL Keep in loop]** di ripetere la sequenza o lasciala disabilitata per impostare le impression dell&#39;ultimo bundle su **[!UICONTROL Infinite]**.

1. Per ogni pianificazione aggiuntiva, fare clic su **[!UICONTROL + Add Schedule]**, selezionare la relativa scheda di pianificazione e configurarne i bundle, le date e le ore e le impostazioni di rotazione.

   Le caselle di controllo del bundle si applicano alla pianificazione selezionata, non a tutte le pianificazioni. Assicurati che le pianificazioni coprano l&#39;intera durata dell&#39;esperienza con i bundle assegnati.

1. Fare clic su **[!UICONTROL Save]** nella finestra di dialogo.

1. [Salva l&#39;esperienza](#save).

### Utilizzo dell’editor manuale {#with-scheduling-manual}

[Aprire l&#39;editor manuale](experience-edit-targeting.md#experience-open) prima di eseguire la procedura seguente.

1. Mentre [crei](experience-create-targeting.md) o [modifichi](experience-edit-targeting.md) l&#39;esperienza, apri le impostazioni di ottimizzazione creativa:

   1. Tenere premuto il cursore sul nodo foglia creativo sotto il nodo di destinazione ed effettuare le seguenti operazioni:

      * Per i bundle esistenti, fare clic su **[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]**.

      * Per i nuovi bundle, fai clic su **[!UICONTROL ...]** > **[!UICONTROL Assign Bundles]** e [assegna i bundle](experience-assign-creative-bundles.md).

   1. Fare clic sulla scheda **[!UICONTROL Creative Optimization]**.

1. Abilita **[!UICONTROL Schedule]**.

1. Per la prima programmazione:

   1. Nella colonna a sinistra, seleziona la casella di controllo accanto a ciascun bundle creativo da aggiungere alla prima pianificazione.

   1. Specifica la data e l’ora di inizio, nonché la data e l’ora di fine della pianificazione.

   1. Seleziona il tipo di rotazione creativa:

      * *[!UICONTROL Weighted]:* Immettere il peso di ciascun bundle come percentuale. Per applicare gli stessi pesi a tutti i bundle nella pianificazione, fare clic su (![Applica peso uguale](/help/creative/assets/apply-equal-weight.png "Applica peso uguale")). La somma dei pesi di tutti i bundle selezionati deve essere pari a 100.

      * *[!UICONTROL Algorithmic]:* Per **[!UICONTROL Optimization Goal]**, selezionare *[!UICONTROL Click Through Rate]*, (esperienze annuncio video standard) *[!UICONTROL Completion Rate]* o *[!UICONTROL Custom Objective]*. Se selezioni *[!UICONTROL Custom Objective]*, seleziona un [obiettivo personalizzato di Advertising DSP](/help/dsp/optimization/custom-goal.md) esistente.

      * *[!UICONTROL Sequencing]:*

        1. Trascina e rilascia i bundle assegnati nell’ordine desiderato.

        1. Immetti il numero di impression per ciascuna sequenza.

        1. Per l&#39;ultima sequenza, modificare se in a\) visualizzare il bundle finale nella sequenza a tempo indefinito (*[!UICONTROL Infinite]* (impostazione predefinita) o b\) tornare al primo bundle dopo la visualizzazione del bundle finale (*[!UICONTROL Keep in Loop]*).

1. Per ogni programma aggiuntivo:

   1. Fare clic su **[!UICONTROL + Add Schedule]**.

   1. Nella colonna a sinistra, seleziona la casella di controllo accanto a ciascun bundle creativo da aggiungere alla prima pianificazione.

   1. Specifica le date di inizio e fine per la pianificazione.

   1. Seleziona il tipo di rotazione creativa:

      * *[!UICONTROL Weighted]:* Immettere il peso di ciascun bundle come percentuale. La somma dei pesi di tutti i bundle selezionati deve essere pari a 100.

      * *[!UICONTROL Algorithmic]:* Per **[!UICONTROL Optimization Goal]**, selezionare *[!UICONTROL Click Through Rate]* o *[!UICONTROL Custom Objective]*. Se selezioni *[!UICONTROL Custom Objective]*, seleziona un [obiettivo personalizzato di Advertising DSP](/help/dsp/optimization/custom-goal.md) esistente.

      * *[!UICONTROL Sequencing]:*

        1. Trascina e rilascia i bundle assegnati nell’ordine desiderato.

        1. Immetti il numero di impression per ciascuna sequenza.

        1. Per l&#39;ultima sequenza, modificare se in a\) visualizzare il bundle finale nella sequenza a tempo indefinito (*[!UICONTROL Infinite]* (impostazione predefinita) o b\) tornare al primo bundle dopo la visualizzazione del bundle finale (*[!UICONTROL Keep in Loop]*).

1. Fare clic su **[!UICONTROL Save]**.

## Salvare l’esperienza {#save}

I seguenti passaggi si applicano a entrambi gli editor.

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [Assegnazione e annullamento dell&#39;assegnazione di bundle creativi a un nodo finale in un&#39;esperienza](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [Personalizza gli URL di tracciamento per i creativi](/help/creative/experiences/experience-tracking-urls-targeting.md)
>* [Visualizza il registro delle modifiche per un&#39;esperienza](/help/creative/experiences/experience-view-change-log.md)
