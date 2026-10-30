---
title: Creare un’esperienza con il targeting dell’albero decisionale
description: Scopri come creare un’esperienza pubblicitaria mirata utilizzando l’editor di strutture decisionali manuale o basato sull’intelligenza artificiale.
feature: Creative Experiences
exl-id: 825fd9af-ca7a-4b44-8e4b-1a6f34edac9e
TQID: 'https://experienceleague.adobe.com/nxegtoNEqfAk7LUyb-3qD6YJYaGfx3M3QdrLx-q5y14'
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
source-wordcount: '715'
ht-degree: 0%
---
# Creare un’esperienza con il targeting dell’albero decisionale

Crea un’esperienza pubblicitaria mirata utilizzando una struttura decisionale. Ogni esperienza utilizza annunci provenienti da una singola libreria creativa.

Per impostazione predefinita, viene aperto l’editor basato sull’intelligenza artificiale (Beta). Puoi configurare la struttura tramite l’agente di intelligenza artificiale o modificarne direttamente l’area di lavoro. Puoi anche passare all’editor manuale esistente.

>[!NOTE]
>
>* Dopo aver creato un’esperienza con targeting, non puoi modificarla in un’esperienza non con targeting, che utilizza un flusso di lavoro diverso.
>* Assicurati che le esperienze dell’annuncio includano un targeting compatibile con le campagne in cui lo implementerai. Il comportamento di targeting gerarchico può variare a seconda di DSP. Quando carichi un tag di esperienza di annuncio in Advertising DSP e lo alleghi a un posizionamento, il targeting a livello di annuncio viene applicato sul targeting a livello di posizionamento (non al suo posto). Ad esempio, se un posizionamento ha come target gli utenti in Australia e un annuncio ha come target gli utenti in Giappone, l’annuncio avrà come target il ramo &quot;Tutti gli altri&quot;.

## Creare l’esperienza

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. Fare clic su **[!UICONTROL Create New Experience]**.

1. Immetti le [impostazioni generali dell&#39;esperienza](experience-settings-targeting.md), con **[!UICONTROL Targeting]** abilitato.

1. Fare clic su **[!UICONTROL Create]**.

   Per la nuova esperienza viene aperto l’editor della struttura decisionale basato sull’intelligenza artificiale.

1. Configurare la struttura utilizzando una delle procedure seguenti.

## Configurare la struttura utilizzando l’editor basato sull’intelligenza artificiale (Beta) {#ai-editor}

1. Nella conversazione, descrivi la struttura di targeting desiderata, inclusi i criteri per ogni ramo e come gestire i visualizzatori che non corrispondono a un target specificato.

1. Rivedi la struttura nell’area di lavoro. Per richiedere modifiche, descrivetele nella conversazione. Attendi che l’assistente finisca l’elaborazione prima di interagire con l’area di lavoro.

1. (Facoltativo) Affina la struttura direttamente nell’area di lavoro:

   * [Aggiungere una destinazione di livello finale](experience-target-node-add-final.md#ai-editor), [inserire un livello di destinazione](experience-target-node-add-inner.md#ai-editor) o [aggiungere una destinazione di pari livello](experience-target-node-add-sibling.md#ai-editor).

   * [Copia nodi figlio e creativi](experience-target-node-copy.md#ai-editor) o [elimina un nodo](experience-target-node-delete.md#ai-editor).

1. [Assegna bundle creativi ai nodi finali](experience-assign-creative-bundles.md#ai-editor) e, facoltativamente, [personalizza l&#39;ottimizzazione e la pianificazione creative](experience-optimization-scheduling-targeting.md) e [gli URL di tracciamento](experience-tracking-urls-targeting.md#ai-editor).

   Per pubblicare l’esperienza, devi assegnare dei bundle a ciascun nodo finale o utilizzare le creatività predefinite dell’esperienza. È possibile assegnare valori predefiniti a nodi non assegnati al momento del salvataggio.

1. (Facoltativo) Modifica le impostazioni di esperienza generale:

   1. Per salvare le modifiche alla struttura da mantenere, fare clic su **[!UICONTROL Save]**.

   1. Fare clic su **[!UICONTROL Experience Form]**, quindi su **[!UICONTROL Yes]** per ignorare le modifiche alla struttura non salvate e aprire il modulo.

   1. Modificare le [impostazioni generali dell&#39;esperienza](experience-settings-targeting.md), quindi fare clic su **[!UICONTROL Save]**.

      Viene aperto l’editor basato sull’intelligenza artificiale.

1. [Salva l&#39;esperienza](#save).

## Configurare la struttura utilizzando l’editor manuale {#manual-editor}

1. Nell&#39;editor basato su IA fare clic su **[!UICONTROL Manual Decision Tree]** e quindi su **[!UICONTROL Yes]** per uscire dall&#39;editor basato su IA.

   Salva eventuali modifiche all’editor AI che desideri mantenere prima di cambiare. Confermando lo switch, vengono eliminate le modifiche alla struttura non salvate.

1. (Facoltativo) Modificare le impostazioni di visualizzazione:

   * Ingrandire o ridurre spostando il dispositivo di scorrimento.

   * Passare dalla visualizzazione verticale alla visualizzazione orizzontale facendo clic su ![Visualizza come struttura verticale](/help/creative/assets/tree-vertical.png "Visualizza come struttura verticale") o ![Visualizza come albero orizzontale](/help/creative/assets/tree-horizontal.png "Visualizza come albero orizzontale").

   Le impostazioni di visualizzazione vengono salvate fino alla disconnessione.

1. Configura i target dell’annuncio e le creatività corrispondenti:

   * [Aggiungere una destinazione di livello finale](experience-target-node-add-final.md#manual-editor), [inserire una destinazione tra nodi](experience-target-node-add-inner.md#manual-editor) o [aggiungere una destinazione di pari livello](experience-target-node-add-sibling.md#manual-editor).

   * [Copia nodi figlio e creativi](experience-target-node-copy.md#manual-editor) o [elimina un nodo](experience-target-node-delete.md#manual-editor).

   * [Assegna bundle creativi](experience-assign-creative-bundles.md#manual-editor) e, facoltativamente, [personalizza l&#39;ottimizzazione e la pianificazione creative](experience-optimization-scheduling-targeting.md) e [gli URL di tracciamento](experience-tracking-urls-targeting.md#manual-editor).

1. (Facoltativo) Per modificare le impostazioni generali dell&#39;esperienza, fare clic su **[!UICONTROL Experience Form]** e modificare le [impostazioni generali dell&#39;esperienza](experience-settings-targeting.md).

1. [Salva l&#39;esperienza](#save).

## Salvare l’esperienza {#save}

I seguenti passaggi si applicano a entrambi gli editor.

{{$include /help/_includes/experience-save.md}}

## Tag di annunci e transcodifica video per esperienze salvate

Quando l&#39;esperienza è in diretta, [!DNL Creative] crea automaticamente un tag annuncio per ogni dimensione creativa o durata video applicabile. È quindi possibile [esportare un tag annuncio e implementarlo in un DSP](/help/creative/experiences/experience-tag-export.md).

Per le esperienze di annunci video, i creativi video vengono transcodificati automaticamente da Adobe Advertising DSP come tag VAST 2.0, in modo da poterli visualizzare in anteprima. Facoltativamente, puoi [applicare la transcodifica per un DSP](experience-tag-video-transcoding.md) diverso a qualsiasi tag esperienza annuncio video.

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
>* [Modifica un&#39;esperienza con il targeting dell&#39;albero delle decisioni](experience-edit-targeting.md)
>* [Visualizza il registro delle modifiche per un&#39;esperienza](/help/creative/experiences/experience-view-change-log.md)
