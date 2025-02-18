---
title: Personalizzare l’ottimizzazione creativa e la pianificazione di un’esperienza
description: Scopri come
feature: Creative Experiences
exl-id: 9398df69-6a48-4b72-8c5c-a79341bf3b8a
source-git-commit: f6da629fdb81af4393bac9a81050111aded3ee3a
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 0%

---

# Personalizza l’ottimizzazione creativa e la pianificazione di un’esperienza senza il targeting della struttura decisionale

*Esperienze con solo creatività esistente*
*Versione beta chiusa*

Per impostazione predefinita, la rotazione creativa di un tag di esperienza annuncio è determinata algoritmicamente per ottimizzare il tasso di click-through complessivo e le impostazioni di ottimizzazione creativa si applicano a tutti i creativi assegnati. Puoi personalizzare la rotazione creativa per eseguire manualmente le creatività in base al peso relativo o per ottimizzare algoritmicamente per un obiettivo personalizzato Advertising DSP specifico. <!-- verify --> È inoltre possibile pianificare l&#39;esecuzione di creativi specifici durante periodi di tempo sequenziali specificati e applicare impostazioni personalizzate di rotazione creativa per ogni pianificazione.

## Configurare l’ottimizzazione creativa senza pianificare

Quando la pianificazione creativa è disabilitata, le impostazioni di ottimizzazione creativa si applicano a tutti i creativi assegnati.

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. Effettuare una delle seguenti operazioni:

   * Nella vista a schede, fai clic su **[!UICONTROL ...]** accanto al nome dell&#39;esperienza e quindi su **[!UICONTROL Tag Manager]**.

   * Nella visualizzazione per tabella, posizionare il cursore sulla riga, fare clic su **[!UICONTROL More]** e quindi su **[!UICONTROL Tag Manager]**

1. Posiziona il cursore sulla riga del tag annuncio applicabile e fai clic su ![Pianificazione annuncio](/help/creative/assets/edit-gray.png "Modifica URL di tracciamento") **[!UICONTROL Ad Schedule]**. <!-- For targeted experiences, this is "Edit Schedules" -->&lt;!— In Tag Manager è disponibile solo la vista a elenco, ma non quella a schede, a partire da 2/2. >

1. Disabilita **[!UICONTROL Schedule]**.

1. Seleziona il tipo di rotazione creativa:

   * *[!UICONTROL Weighted]:* Ruota manualmente i creativi in base al peso relativo. Immetti il peso di ogni creatività in percentuale. La somma dei pesi per tutti i creativi selezionati deve essere 100.

   * *[!UICONTROL Algorithmic]:* ruota le creatività in modo algoritmico in base a un obiettivo di ottimizzazione specificato.

      * Per **[!UICONTROL Optimization Goal]**, selezionare *[!UICONTROL Click Through Rate]* o *[!UICONTROL Custom Objective]*.  Se selezioni *[!UICONTROL Custom Objective]*, seleziona un [obiettivo personalizzato di Advertising DSP](/help/dsp/optimization/custom-goal.md).<!-- Verify --> esistente

1. Fare clic su **[!UICONTROL Save]**.

## Configurare l’ottimizzazione creativa con la programmazione creativa

Facoltativamente, puoi pianificare l’esecuzione di creative specifiche utilizzate per un tag di esperienza annuncio durante periodi di tempo sequenziali specifici tra le date di inizio e di fine dell’esperienza e applicare impostazioni di rotazione creativa personalizzate per ogni pianificazione. Ad esempio, puoi pianificare l’esecuzione di Creative 1 nelle prime due settimane in modo da ottimizzare il tasso di click-through e Creative 2 nelle due settimane successive in modo da ottimizzare un obiettivo personalizzato specifico.

Quando utilizzi la pianificazione, devi pianificare le creatività per tutta la durata dell’esperienza.

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. Effettuare una delle seguenti operazioni:

   * Nella vista a schede, fai clic su **[!UICONTROL ...]** accanto al nome dell&#39;esperienza e quindi su **[!UICONTROL Tag Manager]**.

   * Nella visualizzazione per tabella, posizionare il cursore sulla riga, fare clic su **[!UICONTROL More]** e quindi su **[!UICONTROL Tag Manager]**

1. Posiziona il cursore sulla riga del tag annuncio applicabile e fai clic su ![Pianificazione annuncio](/help/creative/assets/edit-gray.png "Modifica URL di tracciamento") **[!UICONTROL Ad Schedule]**. <!-- For targeted experiences, this is "Edit Schedules" -->&lt;!— In Tag Manager è disponibile solo la vista a elenco, ma non quella a schede, a partire da 2/2. >

1. Abilita **[!UICONTROL Schedule]**.

1. Per la prima programmazione:

   1. Nella colonna sinistra, seleziona la casella di controllo accanto a ogni creatività da aggiungere alla prima pianificazione.

   1. Specifica le date di inizio e fine per la pianificazione.

   1. Seleziona il tipo di rotazione creativa:

      * *[!UICONTROL Weighted]:* Ruota manualmente i creativi in base al peso relativo. Immetti il peso di ogni creatività in percentuale. La somma dei pesi per tutti i creativi selezionati deve essere 100.

      * *[!UICONTROL Algorithmic]:* ruota le creatività in modo algoritmico in base a un obiettivo di ottimizzazione specificato.

         * Per **[!UICONTROL Optimization Goal]**, selezionare *[!UICONTROL Click Through Rate]* o *[!UICONTROL Custom Objective]*.  Se selezioni *[!UICONTROL Custom Objective]*, seleziona un [obiettivo personalizzato di Advertising DSP](/help/dsp/optimization/custom-goal.md).<!-- Verify --> esistente

1. Per ogni programma aggiuntivo:

   1. Fare clic su **[!UICONTROL + Add Schedule]**.

   1. Nella colonna sinistra, seleziona la casella di controllo accanto a ogni creatività da aggiungere alla prima pianificazione.

   1. Specifica le date di inizio e fine per la pianificazione.

   1. Seleziona il tipo di rotazione creativa:

      * *[!UICONTROL Weighted]:* Ruota manualmente i creativi in base al peso relativo. Immetti il peso di ogni creatività in percentuale. La somma dei pesi per tutti i creativi selezionati deve essere 100.

      * *[!UICONTROL Algorithmic]:* ruota le creatività in modo algoritmico in base a un obiettivo di ottimizzazione specificato.

         * Per **[!UICONTROL Optimization Goal]**, selezionare *[!UICONTROL Click Through Rate]* o *[!UICONTROL Custom Objective]*.  Se selezioni *[!UICONTROL Custom Objective]*, seleziona un [obiettivo personalizzato di Advertising DSP](/help/dsp/optimization/custom-goal.md).<!-- Verify --> esistente

1. Fare clic su **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Creare manualmente un tag annuncio per una dimensione creativa applicabile](/help/creative/experiences/experience-tag-create-manually.md)
>* [Assegna creatività a un tag annuncio per esperienze senza targeting](experience-tag-assign-creatives.md)
>* [Personalizza gli URL di tracciamento per un&#39;esperienza senza targeting della struttura decisionale](experience-tracking-urls-no-targeting.md)
