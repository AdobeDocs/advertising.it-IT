---
title: Personalizzare gli URL di tracciamento per un’esperienza
description: Scopri come personalizzare gli URL di tracciamento per ogni creativo in un’esperienza con targeting della struttura decisionale.
feature: Creative Experiences
exl-id: ba3b15b4-116e-4caa-8ce1-4d2e488a6362
TQID: 'https://experienceleague.adobe.com/LjeF7eYU8V93W28VbV-D6NNWWwdKqywOP2BwzDwQAgo'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
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
source-wordcount: '448'
ht-degree: 0%
---
# Personalizzare gli URL di tracciamento dei creativi in un’esperienza con il targeting della struttura decisionale

*Solo nodi di destinazione con creatività esistente*

Per le esperienze con targeting basato su albero decisionale, puoi creare fino a cinque URL personalizzati di tracciamento delle impression e cinque URL personalizzati di tracciamento dei clic per ogni singolo contenuto creativo utilizzato per l’esperienza. Quando la sostituzione della pagina di destinazione è disponibile, puoi anche specificare un URL di pagina di destinazione personalizzato. Puoi personalizzare gli URL di tracciamento dall’editor della struttura decisionale.

Gli URL personalizzati vengono utilizzati solo per gli annunci creati dall&#39;esperienza e non vengono salvati nelle impostazioni creative di base in [!UICONTROL Creative Libraries].

La sostituzione della pagina di destinazione è disponibile per le esperienze standard e per i nodi che utilizzano creatività predefinite. Per i bundle dinamici assegnati, le pagine di destinazione sono determinate dal feed e la scheda della pagina di destinazione non viene visualizzata.

## Utilizzo dell’editor basato sull’intelligenza artificiale (Beta) {#ai-editor}

Durante la [creazione](experience-create-targeting.md#ai-editor) o la [modifica](experience-edit-targeting.md#ai-editor) dell&#39;esperienza, utilizza i controlli dell&#39;area di lavoro:

1. Nel nodo foglia creativa sotto il nodo di destinazione, fare clic su **[!UICONTROL ...]** > **[!UICONTROL Edit Tracking URLs]**.

1. Selezionare la scheda **[!UICONTROL Click Tracking URLs]**, **[!UICONTROL Impression Tracking URLs]** o (se disponibile) **[!UICONTROL Landing URL]**.

   I creativi sono raggruppati per bundle. Le dimensioni creative predefinite per l’esperienza determinano le dimensioni creative disponibili.

1. Espandi il contenuto creativo da modificare ed effettua una delle seguenti operazioni:

   * Per aggiungere o modificare un URL personalizzato, immetti l’URL nel campo di input.

   * Per aggiungere un altro URL di tracciamento personalizzato, fare clic su **[!UICONTROL Add URL]** e immettere l&#39;URL nel campo di input.

   * Per rimuovere un URL personalizzato, scegliere **[!UICONTROL Delete URL]**.

   Fai clic all’esterno di un campo modificato e correggi eventuali errori di convalida prima di salvare.

1. Fare clic su **[!UICONTROL Save]** nella finestra di dialogo per aggiornare la struttura di lavoro.

1. [Salva l&#39;esperienza](#save) dall&#39;intestazione della struttura.

## Utilizzo dell’editor manuale {#manual-editor}

[Aprire l&#39;editor manuale](experience-edit-targeting.md#experience-open) prima di eseguire la procedura seguente.

1. Nel nodo foglia creativa sotto il nodo di destinazione, fare clic su **[!UICONTROL ...]** > **[!UICONTROL Edit Tracking URLs]**.

1. Selezionare la scheda **[!UICONTROL Click Tracking URLs]**, **[!UICONTROL Impression Tracking URLs]** o (se disponibile) **[!UICONTROL Landing URLs]**.

   Le schede elencano i creativi nei bundle assegnati. Le dimensioni di creatività predefinite per l&#39;esperienza determinano le dimensioni di creatività disponibili.<!-- There's no distinct "Creative Sizes" setting. -->

1. Espandi il contenuto creativo da modificare ed effettua una delle seguenti operazioni:

   * Per aggiungere o modificare un URL personalizzato, immetti l’URL nel campo di input.

   * Per aggiungere un altro URL di tracciamento personalizzato, fare clic su **[!UICONTROL +]** e immettere l&#39;URL nel campo di input.

   * Per rimuovere un URL personalizzato, posizionare il cursore sulla riga della creatività e fare clic su ![Elimina](/help/creative/assets/delete.png "Elimina").

1. Fare clic su **[!UICONTROL Save]** nella finestra di dialogo per aggiornare la struttura di lavoro.

1. [Salva l&#39;esperienza](#save) dall&#39;intestazione della struttura.

## Salvare l’esperienza {#save}

I seguenti passaggi si applicano a entrambi gli editor. Il salvataggio della sola finestra di dialogo dell’URL di tracciamento non salva né pubblica l’esperienza.

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [Assegnazione e annullamento dell&#39;assegnazione di bundle creativi a un nodo finale in un&#39;esperienza](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [Personalizza gli URL di tracciamento per un&#39;esperienza senza targeting della struttura decisionale](experience-tracking-urls-no-targeting.md)
