---
title: Copiare nodi secondari in un altro nodo di destinazione allo stesso livello
description: Scopri come copiare tutti i nodi secondari di un nodo di destinazione principale in un altro nodo di destinazione allo stesso livello
feature: Creative Experiences
exl-id: b3705689-57b6-41ce-9e00-2358bd195c93
TQID: 'https://experienceleague.adobe.com/KLKVrggOQ8V99Cd-2PcFEdwImKvLYkskSD-DPDvpwu0'
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
source-git-commit: 8a75f4a164b25ed8e73816c3d853d9650f470118
workflow-type: tm+mt
source-wordcount: '403'
ht-degree: 0%
---
# Copiare nodi secondari in un altro nodo di destinazione allo stesso livello

*Esperienze con targeting solo per la struttura decisionale*

Puoi copiare tutti i nodi secondari di un nodo di destinazione principale (inclusi tutti i target secondari e i bundle creativi loro assegnati) in un altro nodo di destinazione allo stesso livello. È possibile copiare i nodi a) aggiungendo i nodi copiati al framework esistente oppure b) sostituendo completamente il framework esistente. <!-- Give the main use case or an example to explain. -->

Questa funzionalità non influisce sulla destinazione specificata per il nodo padre, ma solo sui nodi figlio.

## Utilizzo dell’editor basato sull’intelligenza artificiale (Beta) {#ai-editor}

Durante la [creazione](experience-create-targeting.md#ai-editor) o la [modifica](experience-edit-targeting.md#ai-editor) dell&#39;esperienza, utilizza i controlli dell&#39;area di lavoro:

1. Nel nodo padre di cui si desidera copiare gli elementi figlio fare clic su **[!UICONTROL ...]** > **[!UICONTROL Copy Children]**.

1. Nel nodo di destinazione allo stesso livello, fare clic su **[!UICONTROL ...]** e quindi scegliere una delle opzioni seguenti:

   * Per aggiungere gli oggetti figlio e i creativi copiati senza rimuovere gli elementi figlio esistenti, fare clic su **[!UICONTROL Add]**.

   * Per sostituire gli oggetti e i creativi figlio esistenti con gli elementi figlio copiati, fare clic su **[!UICONTROL Replace]**.

   Un&#39;azione viene disabilitata quando la struttura ad albero non la supporta. Rivedi eventuali avvisi prima di procedere.

1. Rivedi il ramo di destinazione, quindi [salva l&#39;esperienza](#save).

## Utilizzo dell’editor manuale {#manual-editor}

[Aprire l&#39;editor manuale](experience-edit-targeting.md#experience-open) prima di eseguire la procedura seguente.

1. Fai clic sul nodo principale di cui desideri copiare gli elementi secondari, fai clic su ![Aggiungi](/help/creative/assets/add.png "Aggiungi"), quindi seleziona a\) **[!UICONTROL Copy Children ctrl+c]** o b\) immetti **[!UICONTROL Ctrl+C]** ([!DNL Microsoft Windows]) o **[!UICONTROL Command-C]** ([!DNL Apple Macintosh]) sulla tastiera.

1. Effettuare una delle seguenti operazioni:

   * Per sostituire tutti i nodi figlio e i creativi di un nodo, fare clic sul nodo in cui si desidera incollare le informazioni copiate, fare clic su **[!UICONTROL ...]**, quindi selezionare **[!UICONTROL Replace ctrl+shift+v]** o b\) immettere **[!UICONTROL Ctrl+Shift+V]** ([!DNL Microsoft Windows]) o **[!UICONTROL Command-Shift-V]** ([!DNL Apple Macintosh]) sulla tastiera.

   * (Nodi con più destinazioni secondarie, nessun nodo &quot;All&quot; e nessun solo creativo) Per aggiungere tutti i nodi secondari e i creativi a un nodo, senza eliminare quelli esistenti, fare clic sul nodo in cui si desidera incollare le informazioni copiate, fare clic su **[!UICONTROL ...]** e selezionare **[!UICONTROL Add ctrl+v]** o b\) immettere **[!UICONTROL Ctrl+V]** ([!DNL Microsoft Windows]) o **[!UICONTROL Command-V]** ([!DNL Apple Macintosh]) sulla tastiera.

## Salvare l’esperienza {#save}

I seguenti passaggi si applicano a entrambi gli editor.

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [Aggiungere un nodo di destinazione al livello finale](experience-target-node-add-final.md)
>* [Inserire un nodo di destinazione tra i nodi](experience-target-node-add-inner.md)
>* [Aggiungere un nodo di destinazione di pari livello tra nodi](experience-target-node-add-sibling.md)
>* [Assegna creatività a un nodo finale](experience-assign-creative-bundles.md)
>* [Eliminare un nodo di destinazione o un nodo foglia creativo](/help/creative/experiences/experience-target-node-delete.md)
>* [Crea un&#39;esperienza con il targeting dell&#39;albero delle decisioni](experience-create-targeting.md)
>* [Modifica un&#39;esperienza con il targeting dell&#39;albero delle decisioni](experience-edit-targeting.md)
>* [Impostazioni esperienza di destinazione](experience-settings-targeting.md)
