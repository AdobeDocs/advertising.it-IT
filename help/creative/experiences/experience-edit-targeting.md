---
title: Modificare un’esperienza con il targeting dell’albero decisionale
description: Scopri come modificare un’esperienza pubblicitaria mirata utilizzando l’editor di strutture decisionali manuale o basato sull’intelligenza artificiale.
feature: Creative Experiences
exl-id: 8c5e8f9b-c405-41b2-98a9-da7c5debd3e1
TQID: 'https://experienceleague.adobe.com/0mcPjfiET-DKrm2qaa1Odygv1GIgv4cR7lBRNmrYGBk'
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
source-wordcount: '655'
ht-degree: 0%
---
# Modificare un’esperienza con il targeting dell’albero decisionale

Per impostazione predefinita, viene aperto l’editor basato sull’intelligenza artificiale (Beta) per le esperienze con targeting. Puoi lavorare con l’agente di intelligenza artificiale, modificare direttamente l’area di lavoro o aprire l’editor manuale esistente.

## Apri l’esperienza {#experience-open}

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. (Facoltativo) [Personalizza la visualizzazione](/help/creative/introduction/customize-data-views.md) per includere esperienze specifiche.

1. Effettuare una delle seguenti operazioni:

   * Per aprire l’editor basato sull’intelligenza artificiale:

     * Nella vista a schede, fai clic su **[!UICONTROL ...]** accanto al nome dell&#39;esperienza e quindi su **[!UICONTROL Edit]**.

     * Nella visualizzazione per tabella, posizionare il cursore sulla riga, fare clic su **[!UICONTROL More]** e quindi su **[!UICONTROL Edit]**.

   * Per aprire l’editor manuale:

     * Nella vista a schede, fai clic su **[!UICONTROL ...]** accanto al nome dell&#39;esperienza e quindi su **[!UICONTROL Create Decision Tree Manually (Legacy)]**.

     * Nella visualizzazione per tabella, posizionare il cursore sulla riga, fare clic su **[!UICONTROL More]** e quindi su **[!UICONTROL Create Decision Tree Manually (Legacy)]**.

     * Nell’editor basato sull’intelligenza artificiale,

## Modificare utilizzando l’editor basato sull’intelligenza artificiale (Beta) {#ai-editor}

1. [Apri l&#39;esperienza](#experience-open).

1. Descrivi le modifiche di targeting desiderate nella conversazione. Identifica il ramo interessato dalle sue destinazioni o, se mostrato sull’area di lavoro, dal suo ID nodo.

1. Rivedi la struttura aggiornata e descrivi eventuali ulteriori modifiche. Attendi che l’assistente finisca l’elaborazione prima di interagire con l’area di lavoro.

1. (Facoltativo) Apporta le modifiche direttamente nell’area di lavoro:

   * [Aggiungere una destinazione di livello finale](experience-target-node-add-final.md#ai-editor), [inserire un livello di destinazione](experience-target-node-add-inner.md#ai-editor) o [aggiungere una destinazione di pari livello](experience-target-node-add-sibling.md#ai-editor).

   * Modificare i criteri di una destinazione facendo clic su **[!UICONTROL ...]** > **[!UICONTROL Edit]** accanto alla destinazione, modificando i valori e facendo clic su **[!UICONTROL Edit Node]**.

   * [Copia nodi figlio e creativi](experience-target-node-copy.md#ai-editor) o [elimina un nodo](experience-target-node-delete.md#ai-editor).

   * [Assegna o rimuovi l&#39;assegnazione dei bundle creativi](experience-assign-creative-bundles.md#ai-editor).

   * [Personalizza l&#39;ottimizzazione e la pianificazione della creatività](experience-optimization-scheduling-targeting.md) o [gli URL di tracciamento](experience-tracking-urls-targeting.md#ai-editor).

1. [Salva l&#39;esperienza](#save).

## Modifica tramite l’editor manuale {#manual-editor}

1. [Apri l&#39;esperienza](#experience-open).

1. (Esperienze con stato `[processing](experience-about.md#experience-statuses)`) Se viene richiesto di fornire una bozza esistente non pubblicata, effettuare una delle seguenti operazioni:

   * Fai clic su **[!UICONTROL Continue editing draft]** per rivedere e continuare a modificare la bozza.

   * Fare clic su **[!UICONTROL Discard and start again]** per ignorare la bozza e iniziare dalla versione live.

   * Fare clic su **[!UICONTROL Cancel this edit]** per interrompere la modifica.

1. (Facoltativo) Regolare il cursore di zoom o fare clic su ![Visualizza come struttura verticale](/help/creative/assets/tree-vertical.png "Visualizza come struttura verticale") o ![Visualizza come albero orizzontale](/help/creative/assets/tree-horizontal.png "Visualizza come albero orizzontale") per modificare l&#39;orientamento.

   Le impostazioni di visualizzazione vengono salvate fino alla disconnessione.

1. Cambia obiettivi e creatività secondo necessità:

   * [Aggiungere una destinazione di livello finale](experience-target-node-add-final.md#manual-editor), [inserire una destinazione tra nodi](experience-target-node-add-inner.md#manual-editor) o [aggiungere una destinazione di pari livello](experience-target-node-add-sibling.md#manual-editor).

   * [Copia nodi figlio e creativi](experience-target-node-copy.md#manual-editor) o [elimina un nodo](experience-target-node-delete.md#manual-editor).

   * [Assegna o rimuovi l&#39;assegnazione dei bundle creativi](experience-assign-creative-bundles.md#manual-editor).

   * [Personalizza l&#39;ottimizzazione e la pianificazione della creatività](experience-optimization-scheduling-targeting.md) o [gli URL di tracciamento](experience-tracking-urls-targeting.md#manual-editor).

1. [Salva l&#39;esperienza](#save).

## Cambia editor o modifica le impostazioni dell&#39;esperienza {#switch-editors}

>[!IMPORTANT]
>
>Prima di uscire dall’editor basato sull’intelligenza artificiale, salva le modifiche alla struttura che desideri mantenere. Il passaggio all’editor manuale o al modulo di esperienza non trasferisce le modifiche non salvate.

* **Editor basato su IA per l&#39;editor manuale:** Fare clic su **[!UICONTROL Manual Decision Tree]**. Nella finestra di dialogo di conferma, fai clic su **[!UICONTROL Yes]** per ignorare le modifiche non salvate e aprire l&#39;editor manuale oppure su **[!UICONTROL No]** per rimanere.

* **Editor basato su IA per le impostazioni generali:** Fare clic su **[!UICONTROL Experience Form]**, quindi su **[!UICONTROL Yes]** per ignorare le modifiche alla struttura non salvate e aprire il modulo. Modificare le [impostazioni generali dell&#39;esperienza](experience-settings-targeting.md), quindi fare clic su **[!UICONTROL Save]**.

* **Editor manuale delle impostazioni generali:** Salvare le modifiche alla struttura che si desidera mantenere e quindi fare clic su **[!UICONTROL Experience Form]**. Modificare le [impostazioni generali dell&#39;esperienza](experience-settings-targeting.md), quindi fare clic su **[!UICONTROL Save]**.

* **Impostazioni generali per l&#39;editor basato su IA:** Fare clic su **[!UICONTROL Decision Tree]**. Quando si salvano le modifiche alle impostazioni generali di un’esperienza con targeting, si apre anche l’editor basato sull’intelligenza artificiale.

* **Editor manuale per l&#39;editor basato sull&#39;intelligenza artificiale:** Salva le modifiche alla struttura, torna alla visualizzazione [!UICONTROL Experiences] e seleziona **[!UICONTROL Edit]** per l&#39;esperienza.

Per uscire dall&#39;editor basato su IA senza aprire un altro editor, fare clic su **[!UICONTROL Cancel]**. Fare clic su **[!UICONTROL Yes]** per ignorare le modifiche alla struttura non salvate oppure su **[!UICONTROL No]** per continuare la modifica.

## Salvare l’esperienza {#save}

I seguenti passaggi si applicano a entrambi gli editor.

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [Impostazioni esperienza di destinazione](experience-settings-targeting.md)
>* [Aggiungere un nodo di destinazione al livello finale](experience-target-node-add-final.md)
>* [Inserire un nodo di destinazione tra i nodi](experience-target-node-add-inner.md)
>* [Aggiungere un nodo di destinazione di pari livello tra nodi](experience-target-node-add-sibling.md)
>* [Copia nodi figlio e creativi in un altro nodo allo stesso livello](experience-target-node-copy.md)
>* [Assegna creatività a un nodo finale](experience-assign-creative-bundles.md)
>* [Personalizza gli URL di tracciamento per i creativi nei bundle assegnati](experience-tracking-urls-targeting.md)
>* [Personalizzare l&#39;ottimizzazione e la pianificazione della creatività](experience-optimization-scheduling-targeting.md)
>* [Esportare e implementare un tag di esperienza annuncio per un&#39;esperienza live](/help/creative/experiences/experience-tag-export.md)
>* [Crea un&#39;esperienza con il targeting dell&#39;albero delle decisioni](experience-create-targeting.md)
>* [Visualizza il registro delle modifiche per un&#39;esperienza](/help/creative/experiences/experience-view-change-log.md)
