---
title: Assegnare e annullare l’assegnazione di bundle creativi a un nodo finale in un’esperienza
description: Scopri come assegnare i creativi a ogni target nelle esperienze pubblicitarie.
feature: Creative Experiences
exl-id: 5449a760-6ade-41c0-9cab-bd92026b150b
source-git-commit: f7d5bf3193cb41ca2a0d4415998209e5a9b724ba
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 0%

---

# Assegnare e annullare l’assegnazione di bundle creativi a un nodo finale in un’esperienza

*Esperienze con targeting solo per la struttura decisionale*

Puoi assegnare bundle creativi a un nodo di destinazione al livello più basso in una struttura decisionale dell’esperienza. Per le esperienze per le quali non hai configurato i target, il livello più in basso è in &quot;All&quot; (Tutti).

Per esperienze pubblicitarie standard, puoi assegnare solo bundle creativi standard. Per le esperienze pubblicitarie dinamiche, puoi assegnare solo bundle creativi dinamici.

>[!NOTE]
>
>Se non assegni almeno un bundle creativo a ciascun nodo finale, puoi scegliere di utilizzare le creatività predefinite per ciascun nodo non assegnato quando [salvi l&#39;esperienza](experience-create-targeting.md). Per pubblicare un’esperienza, devi assegnare dei bundle o utilizzare le creatività predefinite per ciascun nodo finale.

<!-- 1. [ways to get to the decision tree] -->

1. Effettuare una delle seguenti operazioni:

   * (Nodi finali senza elementi creativi) Sotto il nodo, fare clic su ![Aggiungi](/help/creative/assets/add.png "Aggiungi"), quindi selezionare **[!UICONTROL Assign Bundles]**.

   * (Nodi con creatività esistente) Posizionare il cursore sulla casella del bundle creativo sotto il nodo di destinazione<!-- wording???? --> e fare clic su **[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]**.

1. Seleziona la casella di controllo accanto a ciascun bundle da assegnare al nodo di destinazione, quindi deseleziona la casella di controllo accanto a ciascun bundle da annullare l’assegnazione.

   Sono elencati solo i bundle del tipo di bundle pertinente per l’esperienza (standard o dinamica).

1. Fare clic su **[!UICONTROL Attach to Bundles]**.

1. (Facoltativo) [Personalizza gli URL di tracciamento per i creativi nei bundle assegnati](experience-tracking-urls-targeting.md).

1. (Facoltativo) [Personalizza l&#39;ottimizzazione creativa e la pianificazione](experience-optimization-scheduling-targeting.md) per i bundle assegnati.

<!--
1. (Optional) To save the experience, click **[!UICONTROL Save]**, and then do the following.
...

These formatted steps are inserted automatically from text in the following file in the _includes folder, which reused in multiple places.
-->

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [Aggiungere un nodo di destinazione al livello finale](experience-target-node-add-final.md)
>* [Inserire un nodo di destinazione tra i nodi](experience-target-node-add-inner.md)
>* [Aggiungere un nodo di destinazione di pari livello tra nodi](experience-target-node-add-sibling.md)
>* [Copia nodi figlio e creativi in un altro nodo allo stesso livello](experience-target-node-copy.md)
>* [Crea un&#39;esperienza con il targeting dell&#39;albero delle decisioni](experience-create-targeting.md)
>* [Modifica un&#39;esperienza con il targeting dell&#39;albero delle decisioni](experience-edit-targeting.md)
>* [Impostazioni esperienza di destinazione](experience-settings-targeting.md)
>* [Esportare e implementare un tag di esperienza annuncio per un&#39;esperienza live](experience-tag-export.md)
