---
title: Personalizzare l’ottimizzazione creativa e la pianificazione di un’esperienza
description: Scopri come configurare l’ottimizzazione e la pianificazione degli annunci per le esperienze senza targeting.
feature: Creative Experiences
exl-id: 9398df69-6a48-4b72-8c5c-a79341bf3b8a
source-git-commit: 9c7f3d2aec0952b38d2fd3097d0b3499d33bf3b8
workflow-type: tm+mt
source-wordcount: '1174'
ht-degree: 0%

---

# Personalizza l’ottimizzazione creativa e la pianificazione di un’esperienza senza il targeting della struttura decisionale

*Esperienze con solo creatività esistente*

Per impostazione predefinita, la rotazione creativa di un tag di esperienza annuncio è determinata algoritmicamente per ottimizzare il tasso di click-through complessivo e le impostazioni di ottimizzazione creativa si applicano a tutti i creativi assegnati. Puoi personalizzare la rotazione creativa per eseguire manualmente le creatività in base al peso relativo o per ottimizzare algoritmicamente per un obiettivo personalizzato Advertising DSP specifico. È inoltre possibile pianificare l&#39;esecuzione di creativi specifici durante periodi di tempo sequenziali specificati e applicare impostazioni personalizzate di rotazione creativa per ogni programma.

## Configurare l’ottimizzazione creativa senza pianificare

Quando la pianificazione creativa è disabilitata, le impostazioni di ottimizzazione creativa si applicano a tutti i creativi assegnati.

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. Effettuare una delle seguenti operazioni:

   * Nella vista a schede, fai clic su **[!UICONTROL ...]** accanto al nome dell&#39;esperienza e quindi su **[!UICONTROL Tag Manager]**.

   * Nella visualizzazione per tabella, posizionare il cursore sulla riga, fare clic su **[!UICONTROL More]** e quindi su **[!UICONTROL Tag Manager]**.

1. Posiziona il cursore sulla riga del tag annuncio applicabile e fai clic su ![Pianificazione annuncio](/help/creative/assets/edit-gray.png "Modifica URL di tracciamento") **[!UICONTROL Creative Optimization]**.&lt;!— In Tag Manager è disponibile solo la vista a elenco, ma non quella a schede, a partire da 2/2. >

1. Disabilita **[!UICONTROL Schedule]**.

1. Seleziona il tipo di rotazione creativa per le varianti di annunci nei bundle associati:

   * *[!UICONTROL Weighted]:* mostra le varianti di annunci nei bundle creativi associati in base al peso relativo. Inserire il peso di ogni fascio come percentuale. Il peso di tutti i bundle selezionati deve essere pari a 100.<!-- For example, if Bundle 1 is 60 and Bundle 2 is 40, then Bundle 1 is shown 60% of the time, and Bundle 2 is shown 40% of the time. -->

   * *[!UICONTROL Algorithmic]:* mostra più spesso le varianti più efficaci dell&#39;annuncio, in base a un obiettivo specificato.

      * Per **[!UICONTROL Optimization Goal]**, seleziona *[!UICONTROL Click Through Rate]*, (esperienze annuncio video standard) *[!UICONTROL Completion Rate]* o *[!UICONTROL Custom Objective]*.  Se selezioni *[!UICONTROL Custom Objective]*, seleziona un [obiettivo personalizzato di Advertising DSP](/help/dsp/optimization/custom-goal.md) esistente.

   * *[!UICONTROL Sequencing]:* mostra i bundle creativi associati in un ordine specificato (con il bundle 1 servito per primo, il bundle 2 servito per secondo e così via), con un numero totale specificato di impression in ogni sequenza di bundle. Le dimensioni degli annunci offerti sono determinate dall’inventario disponibile. Potete configurare il bundle finale nella sequenza su a\) per visualizzarlo indefinitamente (impostazione predefinita) o b\) per tornare al primo bundle. Ad esempio, puoi visualizzare una qualsiasi delle varianti di annuncio nel Bundle 1 per tre (3) impression, quindi visualizzare una qualsiasi variante di annuncio nel Bundle 2 per una (1) impression, quindi visualizzare una qualsiasi delle varianti di annuncio nel Bundle 3 per due (2) impression e infine ricominciare il ciclo. In alternativa, una volta visualizzate le varianti dell’annuncio nel bundle 3, puoi continuare a visualizzare le varianti dell’annuncio nel Bundle 3 a tempo indefinito, anziché creare un loop. Quando si abilita la sequenza:

      1. Trascina e rilascia i bundle assegnati nell’ordine desiderato.

     Per impostazione predefinita, i bundle assegnati sono sequenziati nell’ordine in cui sono stati aggiunti all’esperienza.

      1. Immetti il numero di impression per ciascuna sequenza.

      1. Per l&#39;ultima sequenza, modificare se in a\) visualizzare il bundle finale nella sequenza a tempo indefinito (*[!UICONTROL Infinite]* (impostazione predefinita) o b\) tornare al primo bundle dopo la visualizzazione del bundle finale (*[!UICONTROL Keep in Loop]*).

1. Fare clic su **[!UICONTROL Save]**.

## Configurare l’ottimizzazione creativa con la programmazione creativa

Facoltativamente, puoi pianificare l’esecuzione di creative specifiche utilizzate per un tag di esperienza annuncio durante periodi di tempo sequenziali specifici tra le date di inizio e di fine dell’esperienza e applicare impostazioni di rotazione creativa personalizzate per ogni pianificazione. Ad esempio, puoi pianificare l’esecuzione di Creative 1 nelle prime due settimane per ottimizzare il tasso di click-through e di Creative 2 nelle due settimane successive per ottimizzare un obiettivo personalizzato specifico.

Quando utilizzi la pianificazione, devi pianificare le creatività per tutta la durata dell’esperienza.

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. Effettuare una delle seguenti operazioni:

   * Nella vista a schede, fai clic su **[!UICONTROL ...]** accanto al nome dell&#39;esperienza e quindi su **[!UICONTROL Tag Manager]**.

   * Nella visualizzazione per tabella, posizionare il cursore sulla riga, fare clic su **[!UICONTROL More]** e quindi su **[!UICONTROL Tag Manager]**.

1. Posiziona il cursore sulla riga del tag annuncio applicabile e fai clic su ![Pianificazione annuncio](/help/creative/assets/edit-gray.png "Modifica URL di tracciamento") **[!UICONTROL Creative Optimization]**. <!-- For targeted experiences, this is "Edit Schedules" -->&lt;!— In Tag Manager è disponibile solo la vista a elenco, ma non quella a schede, a partire da 2/2. >

1. Abilita **[!UICONTROL Schedule]**.

1. Per la prima programmazione:

   1. Nella colonna sinistra, seleziona la casella di controllo accanto a ogni creatività da aggiungere alla prima pianificazione.

   1. Specifica le date di inizio e fine per la pianificazione.

   1. Seleziona il tipo di rotazione creativa:

      * *[!UICONTROL Weighted]:* Ruota manualmente i creativi in base al peso relativo. Immetti il peso di ogni creatività in percentuale. La somma dei pesi per tutti i creativi selezionati deve essere 100.

      * *[!UICONTROL Algorithmic]:* ruota le creatività in modo algoritmico in base a un obiettivo di ottimizzazione specificato.

         * Per **[!UICONTROL Optimization Goal]**, seleziona *[!UICONTROL Click Through Rate]*, (esperienze annuncio video standard) *[!UICONTROL Completion Rate]* o *[!UICONTROL Custom Objective]*.  Se selezioni *[!UICONTROL Custom Objective]*, seleziona un [obiettivo personalizzato di Advertising DSP](/help/dsp/optimization/custom-goal.md).<!-- Verify --> esistente

      * *[!UICONTROL Sequencing]:* ruota i bundle creativi associati in un ordine specificato (con il bundle 1 servito per primo, il bundle 2 servito per secondo e così via), con un numero totale specificato di impression in ogni sequenza di bundle. Le dimensioni degli annunci offerti sono determinate dall’inventario disponibile. Potete configurare il bundle finale nella sequenza su a\) per visualizzarlo indefinitamente (impostazione predefinita) o b\) per tornare al primo bundle. Ad esempio, puoi mostrare qualsiasi creativo nel Bundle 1 per tre (3) impression, poi mostrare qualsiasi creativo nel Bundle 2 per una (1) impression, quindi mostrare qualsiasi creativo nel Bundle 3 per due (2) impression, e infine ricominciare il ciclo continuo. In alternativa, una volta che i creativi nel Bundle 3 sono visualizzati, è possibile continuare a mostrare i creativi nel Bundle 3 indefinitamente, piuttosto che creare un loop. Quando si abilita la sequenza:

         1. Trascina e rilascia i bundle assegnati nell’ordine desiderato.

            Per impostazione predefinita, i bundle assegnati sono sequenziati nell’ordine in cui sono stati aggiunti all’esperienza.

         1. Immetti il numero di impression per ciascuna sequenza.

         1. Per l&#39;ultima sequenza, modificare se in a\) visualizzare il bundle finale nella sequenza a tempo indefinito (*[!UICONTROL Infinite]* (impostazione predefinita) o b\) tornare al primo bundle dopo la visualizzazione del bundle finale (*[!UICONTROL Keep in Loop]*).

1. Per ogni programma aggiuntivo:

   1. Fare clic su **[!UICONTROL + Add Schedule]**.

   1. Nella colonna sinistra, seleziona la casella di controllo accanto a ogni creatività da aggiungere alla prima pianificazione.

   1. Specifica le date di inizio e fine per la pianificazione.

   1. Seleziona il tipo di rotazione creativa:

      * *[!UICONTROL Weighted]:* Ruota manualmente i creativi in base al peso relativo. Immetti il peso di ogni creatività in percentuale. La somma dei pesi per tutti i creativi selezionati deve essere 100.

      * *[!UICONTROL Algorithmic]:* ruota le creatività in modo algoritmico in base a un obiettivo di ottimizzazione specificato.

         * Per **[!UICONTROL Optimization Goal]**, selezionare *[!UICONTROL Click Through Rate]* o *[!UICONTROL Custom Objective]*.  Se selezioni *[!UICONTROL Custom Objective]*, seleziona un [obiettivo personalizzato di Advertising DSP](/help/dsp/optimization/custom-goal.md).<!-- Verify --> esistente

      * *[!UICONTROL Sequencing]:* ruota i bundle creativi associati in un ordine specificato, con un numero totale specificato di impression in ogni sequenza di bundle. Quando si abilita la sequenza:

         1. Trascina e rilascia i bundle assegnati nell’ordine desiderato.

            Per impostazione predefinita, i bundle assegnati sono sequenziati nell’ordine in cui sono stati aggiunti all’esperienza.

         1. Immetti il numero di impression per ciascuna sequenza.

         1. Per l&#39;ultima sequenza, modificare se in a\) visualizzare il bundle finale nella sequenza a tempo indefinito (*[!UICONTROL Infinite]* (impostazione predefinita) o b\) tornare al primo bundle dopo la visualizzazione del bundle finale (*[!UICONTROL Keep in Loop]*).

1. Fare clic su **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Creare manualmente un tag annuncio per una dimensione creativa applicabile](/help/creative/experiences/experience-tag-create-manually.md)
>* [Assegna creatività a un tag annuncio per esperienze senza targeting](experience-tag-assign-creatives.md)
>* [Personalizza gli URL di tracciamento per un&#39;esperienza senza targeting della struttura decisionale](experience-tracking-urls-no-targeting.md)
