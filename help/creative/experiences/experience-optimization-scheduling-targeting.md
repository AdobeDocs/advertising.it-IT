---
title: Personalizzare l’ottimizzazione creativa e la pianificazione di un’esperienza
description: Scopri come
feature: Creative Experiences
exl-id: 47d1a249-decd-4c3b-ac88-260488d5bcd2
source-git-commit: a271589a2cb51ec50c37a52254fd8d1b535f279a
workflow-type: tm+mt
source-wordcount: '1073'
ht-degree: 0%

---

# Personalizza l’ottimizzazione creativa e la pianificazione per un’esperienza con il targeting della struttura decisionale

*Solo nodi di destinazione con creatività esistente*

Per impostazione predefinita, la rotazione creativa di un’esperienza viene determinata algoritmicamente per ottimizzare il tasso di click-through complessivo e le impostazioni di ottimizzazione creativa si applicano a tutti i bundle assegnati. Puoi personalizzare la rotazione creativa per eseguire manualmente le creatività in ciascun bundle per ottimizzare in modo algoritmico per un obiettivo personalizzato Advertising DSP specificato; in base a una sequenza di bundle specificata, con un numero specificato di impression in ogni sequenza di bundle; o in base a pesi relativi. Puoi anche pianificare l’esecuzione di specifici bundle creativi durante specifici periodi di tempo sequenziali e applicare impostazioni personalizzate di rotazione creativa per ogni pianificazione.

>[!NOTE]
>
>Queste funzioni non sono disponibili per i nodi che utilizzano le creatività predefinite anziché quelle assegnate.

## Configurare l’ottimizzazione creativa senza pianificare

Quando la pianificazione creativa è disabilitata, le impostazioni di ottimizzazione creativa si applicano a tutti i creativi assegnati.

1. Tenere premuto il cursore sul nodo foglia creativa sotto il nodo di destinazione e fare clic su **[!UICONTROL ...]** > **[!UICONTROL Creative Optimization]**.

1. Disabilita **[!UICONTROL Schedule]**.

1. Seleziona il tipo di rotazione creativa:

   * *[!UICONTROL Weighted]:* Ruota manualmente le creatività in ogni bundle in base al peso relativo. Inserire il peso di ogni fascio come percentuale. La somma dei pesi di tutti i bundle deve essere 100.

   * *[!UICONTROL Algorithmic]:* ruota le creatività in ciascun bundle in modo algoritmico in base a un obiettivo di ottimizzazione specificato.

      * Per **[!UICONTROL Optimization Goal]**, seleziona *[!UICONTROL Click Through Rate]*, (esperienze annuncio video standard) *[!UICONTROL Completion Rate]* o *[!UICONTROL Custom Objective]*.  Se selezioni *[!UICONTROL Custom Objective]*, seleziona un [obiettivo personalizzato di Advertising DSP](/help/dsp/optimization/custom-goal.md) esistente.

   * *[!UICONTROL Sequencing]:* ruota i bundle creativi associati in un ordine specificato (con il bundle 1 servito per primo, il bundle 2 servito per secondo e così via), con un numero totale specificato di impression in ogni sequenza di bundle. Le dimensioni degli annunci offerti sono determinate dall’inventario disponibile. Potete configurare il bundle finale nella sequenza su a\) per visualizzarlo indefinitamente (impostazione predefinita) o b\) per tornare al primo bundle. Ad esempio, puoi mostrare qualsiasi creativo nel Bundle 1 per tre (3) impression, poi mostrare qualsiasi creativo nel Bundle 2 per una (1) impression, quindi mostrare qualsiasi creativo nel Bundle 3 per due (2) impression, e infine ricominciare il ciclo continuo. In alternativa, una volta che i creativi nel Bundle 3 sono visualizzati, è possibile continuare a mostrare i creativi nel Bundle 3 indefinitamente, piuttosto che creare un loop. Quando si abilita la sequenza:

      1. Trascina e rilascia i bundle assegnati nell’ordine desiderato.

     Per impostazione predefinita, i bundle assegnati sono sequenziati nell’ordine in cui sono stati aggiunti all’esperienza.

      1. Immetti il numero di impression per ciascuna sequenza.

      1. Per l&#39;ultima sequenza, modificare se in a\) visualizzare il bundle finale nella sequenza a tempo indefinito (*[!UICONTROL Infinite]* (impostazione predefinita) o b\) tornare al primo bundle dopo la visualizzazione del bundle finale (*[!UICONTROL Keep in Loop]*).

1. Fare clic su **[!UICONTROL Save]**.

## Configurare l’ottimizzazione creativa con la programmazione creativa

Facoltativamente, puoi pianificare l’esecuzione di specifici bundle creativi durante specifici periodi di tempo sequenziali tra le date di inizio e di fine dell’esperienza e applicare impostazioni di rotazione creativa personalizzate per ogni pianificazione. Ad esempio, puoi pianificare l’esecuzione del bundle 1 nelle prime due settimane per ottimizzare il tasso di click-through, e del bundle 2 nelle due settimane successive per ottimizzare un obiettivo personalizzato specifico.

Quando si utilizza la pianificazione, è necessario pianificare i bundle per tutta la durata dell’esperienza.

1. Tenere premuto il cursore sul nodo foglia creativa sotto il nodo di destinazione e fare clic su **[!UICONTROL ...]** > **[!UICONTROL Creative Optimization]**.

1. Abilita **[!UICONTROL Schedule]**.

1. Per la prima programmazione:

   1. Nella colonna a sinistra, seleziona la casella di controllo accanto a ciascun bundle creativo da aggiungere alla prima pianificazione.

   1. Specifica le date di inizio e fine per la pianificazione.

   1. Seleziona il tipo di rotazione creativa:

      * *[!UICONTROL Weighted]:* Ruota manualmente le creatività in ogni bundle in base al peso relativo. Inserire il peso di ogni fascio come percentuale. La somma dei pesi di tutti i bundle selezionati deve essere pari a 100.

      * *[!UICONTROL Algorithmic]:* ruota le creatività in ciascun bundle in modo algoritmico in base a un obiettivo di ottimizzazione specificato.

         * Per **[!UICONTROL Optimization Goal]**, seleziona *[!UICONTROL Click Through Rate]*, (esperienze annuncio video standard) *[!UICONTROL Completion Rate]* o *[!UICONTROL Custom Objective]*.  Se selezioni *[!UICONTROL Custom Objective]*, seleziona un [obiettivo personalizzato di Advertising DSP](/help/dsp/optimization/custom-goal.md) esistente.

      * *[!UICONTROL Sequencing]:* ruota i bundle creativi associati in un ordine specificato (con il bundle 1 servito per primo, il bundle 2 servito per secondo e così via), con un numero totale specificato di impression in ogni sequenza di bundle. Le dimensioni degli annunci offerti sono determinate dall’inventario disponibile. Potete configurare il bundle finale nella sequenza su a\) per visualizzarlo indefinitamente (impostazione predefinita) o b\) per tornare al primo bundle. Ad esempio, puoi mostrare qualsiasi creativo nel Bundle 1 per tre (3) impression, poi mostrare qualsiasi creativo nel Bundle 2 per una (1) impression, quindi mostrare qualsiasi creativo nel Bundle 3 per due (2) impression, e infine ricominciare il ciclo continuo. In alternativa, una volta che i creativi nel Bundle 3 sono visualizzati, è possibile continuare a mostrare i creativi nel Bundle 3 indefinitamente, piuttosto che creare un loop. Quando si abilita la sequenza:

         1. Trascina e rilascia i bundle assegnati nell’ordine desiderato.

            Per impostazione predefinita, i bundle assegnati sono sequenziati nell’ordine in cui sono stati aggiunti all’esperienza.

         1. Immetti il numero di impression per ciascuna sequenza.

         1. Per l&#39;ultima sequenza, modificare se in a\) visualizzare il bundle finale nella sequenza a tempo indefinito (*[!UICONTROL Infinite]* (impostazione predefinita) o b\) tornare al primo bundle dopo la visualizzazione del bundle finale (*[!UICONTROL Keep in Loop]*).

1. Per ogni programma aggiuntivo:

   1. Fare clic su **[!UICONTROL + Add Schedule]**.

   1. Nella colonna a sinistra, seleziona la casella di controllo accanto a ciascun bundle creativo da aggiungere alla prima pianificazione.

   1. Specifica le date di inizio e fine per la pianificazione.

   1. Seleziona il tipo di rotazione creativa:

      * *[!UICONTROL Weighted]:* Ruota manualmente le creatività in ogni bundle in base al peso relativo. Inserire il peso di ogni fascio come percentuale. La somma dei pesi di tutti i bundle selezionati deve essere pari a 100.

      * *[!UICONTROL Algorithmic]:* ruota le creatività in ciascun bundle in modo algoritmico in base a un obiettivo di ottimizzazione specificato.

         * Per **[!UICONTROL Optimization Goal]**, selezionare *[!UICONTROL Click Through Rate]* o *[!UICONTROL Custom Objective]*.  Se selezioni *[!UICONTROL Custom Objective]*, seleziona un [obiettivo personalizzato di Advertising DSP](/help/dsp/optimization/custom-goal.md) esistente.

      * *[!UICONTROL Sequencing]:* ruota i bundle creativi associati in un ordine specificato, con un numero totale specificato di impression in ogni sequenza di bundle. Quando si abilita la sequenza:

         1. Trascina e rilascia i bundle assegnati nell’ordine desiderato.

            Per impostazione predefinita, i bundle assegnati sono sequenziati nell’ordine in cui sono stati aggiunti all’esperienza.

         1. Immetti il numero di impression per ciascuna sequenza.

         1. Per l&#39;ultima sequenza, modificare se in a\) visualizzare il bundle finale nella sequenza a tempo indefinito (*[!UICONTROL Infinite]* (impostazione predefinita) o b\) tornare al primo bundle dopo la visualizzazione del bundle finale (*[!UICONTROL Keep in Loop]*).

1. Fare clic su **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Assegnazione e annullamento dell&#39;assegnazione di bundle creativi a un nodo finale in un&#39;esperienza](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [Personalizza gli URL di tracciamento per i creativi](/help/creative/experiences/experience-tracking-urls-targeting.md)
