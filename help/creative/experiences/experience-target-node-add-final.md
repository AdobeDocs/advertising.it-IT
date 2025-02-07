---
title: Aggiungere un nodo di destinazione al livello finale in un’esperienza
description: Scopri come aggiungere un nodo di destinazione al livello di destinazione finale di un’esperienza di annuncio.
feature: Creative Experiences
source-git-commit: fd925c641bef7953aea50813725252c3913757fa
workflow-type: tm+mt
source-wordcount: '641'
ht-degree: 0%

---

# Aggiungere un nodo di destinazione al livello finale in un’esperienza

*Esperienze con targeting solo per la struttura decisionale*
*Versione beta chiusa*

Quando aggiungi un nodo di destinazione al livello più basso dell’esperienza, che si tratti del nodo principale &quot;All&quot;, di un nodo specifico di destinazione o di un nodo &quot;Everything Else&quot;, puoi definire la destinazione direttamente senza dover creare un nodo di pari livello. Questo crea il nodo di destinazione e un nodo aggiuntivo &quot;Tutto il resto&quot; allo stesso livello.

>[!NOTE]
>
>Per inserire un nodo di destinazione tra i livelli esistenti di una struttura decisionale, vedere &quot;[Inserire un nodo di destinazione tra i nodi di un&#39;esperienza](experience-target-node-add-inner.md).&quot;

<!-- 1. [ways to get to the decision tree] -->

1. Nel nodo in cui si desidera inserire la destinazione, fare clic su ![Aggiungi](/help/creative/assets/add.png "Aggiungi"), quindi selezionare **[!UICONTROL Insert New Target]**.

1. Specificare le destinazioni:

   * Per Adobe Destinazioni pubblico, selezionare **[!UICONTROL Adobe Audience]**, quindi eseguire le operazioni seguenti:

      1. Fare clic su **[!UICONTROL Click to Browse]** per aprire le opzioni [!UICONTROL Audience Targeting], aprire la scheda **[!UICONTROL Adobe Segments]**, specificare una o più destinazioni del pubblico [!DNL Adobe] dell&#39;inserzionista e quindi fare clic su **[!UICONTROL Create]**.

      1. (Facoltativo) Per creare più nodi di destinazione quando sono specificati più tipi di pubblico, selezionare **[!UICONTROL Split targets to create nodes]**.

         Questo crea un nodo di destinazione separato (con bundle creativi separati) per ogni pubblico specificato. Se non dividi le destinazioni, l’utente deve appartenere a tutti i tipi di pubblico specificati.

      1. Fare clic su **[!UICONTROL Apply]**.

   * Per le destinazioni geografiche, selezionare una singola categoria geografica (ad esempio [!UICONTROL Geo: Country]), quindi eseguire le operazioni seguenti:

      1. Fare clic su **[!UICONTROL Click to Browse]** per aprire le opzioni [!UICONTROL Geo Targeting], specificare una o più destinazioni geografiche e quindi fare clic su **[!UICONTROL Save]**.

         Le destinazioni di codici postali dispongono di opzioni di modifica in blocco. Per incollare più codici postali, fare clic sulla scheda **[!UICONTROL Paste postal codes]**, selezionare il paese, incollare o immettere codici postali separati da virgole o su righe separate, quindi fare clic su **[!UICONTROL Include All]**. Per rimuovere una destinazione di CAP inclusa, posizionare il cursore sulla destinazione e fare clic su ![Rimuovi](/help/creative/assets/delete.png "Rimuovi") **[!UICONTROL Remove]**.

      1. (Facoltativo) Per creare più nodi di destinazione quando sono specificate più destinazioni geografiche, selezionare **[!UICONTROL Split targets to create nodes]**.

         Questo crea un nodo di destinazione separato (con bundle creativi separati) per ogni destinazione geografica specificata. Se non si dividono le destinazioni, l&#39;utente deve appartenere a tutte le posizioni specificate.

      1. Fare clic su **[!UICONTROL Apply]**.

   * Per una destinazione di passaggio dati, selezionare **[!UICONTROL Data Pass]**, immettere un valore di passaggio dati singolo, quindi fare clic su **[!UICONTROL Apply]**.

   La chiave per la coppia chiave-valore è già impostata nel campo **[!UICONTROL Data Pass]** nella sezione [!UICONTROL Advanced] delle [impostazioni esperienza](experience-settings-targeting.md).

   * Per un target di pixel di retargeting, selezionare **[!UICONTROL RT Pixel]**, selezionare un singolo pixel di retargeting da utilizzare e i valori richiesti per qualsiasi attributo del pixel che deve essere presente per mostrare i creativi, quindi fare clic su **[!UICONTROL Apply]**.

     Gli attributi per il pixel di retargeting sono configurati nelle [impostazioni pixel di retargeting](/help/creative/pixels/retargeting-pixel-manage.md).

   * Per i dispositivi di destinazione, effettuare le seguenti operazioni:

      1. Selezionare una singola categoria di destinazione (**[!UICONTROL Device: Type]**, **[!UICONTROL Device: OS]** o **[!UICONTROL Device: Browser]**), quindi selezionare le destinazioni.

      1. (Facoltativo) Per creare più nodi di destinazione quando sono specificate più destinazioni geografiche, selezionare **[!UICONTROL Split targets to create nodes]**.

         Questo crea un nodo di destinazione separato (con bundle creativi separati) per ogni destinazione geografica specificata. Se non si dividono le destinazioni, l&#39;utente deve appartenere a tutte le posizioni specificate.

      1. Fare clic su **[!UICONTROL Apply]**.

1. Effettua una delle seguenti operazioni:

   * (Facoltativo) [Assegna creatività](experience-assign-creative-bundles.md) al nuovo nodo di destinazione e al nodo &quot;Tutto il resto&quot;.

   * (Facoltativo) Per salvare l&#39;esperienza:

      1. Fare clic su **[!UICONTROL Save]** e quindi su **[!UICONTROL OK]**.

      1. (Se ogni nodo al livello più basso non include almeno un elemento creativo): effettua una delle seguenti operazioni:

         * Per salvare l&#39;esperienza senza tutti i bundle creativi necessari, fare clic su **[!UICONTROL Save as Draft]**.

           Non puoi creare un tag annuncio per una bozza di esperienza.

         * Per assegnare la creatività predefinita a ogni destinazione a cui non è già stato assegnato un bundle creativo, fare clic su **[!UICONTROL Assign Default Creatives]**. Dopo aver esaminato la struttura aggiornata con i creativi predefiniti assegnati, fare clic su **[!UICONTROL Save]** e **[!UICONTROL OK]**.

         * Per continuare a modificare la struttura decisionale, fare clic su **[!UICONTROL Continue Edit]**.

>[!MORELIKETHIS]
>
>* [Inserire un nodo di destinazione tra i nodi](experience-target-node-add-inner.md)
>* [Aggiungere un nodo di destinazione di pari livello tra nodi](experience-target-node-add-sibling.md)
>* [Copia nodi figlio e creativi in un altro nodo allo stesso livello](experience-target-node-copy.md)
>* [Assegna creatività a un nodo finale](experience-assign-creative-bundles.md)
>* [Eliminare un nodo di destinazione o un nodo foglia creativo](/help/creative/experiences/experience-target-node-delete.md)
>* [Crea un&#39;esperienza con il targeting dell&#39;albero delle decisioni](experience-create-targeting.md)
>* [Modifica un&#39;esperienza con il targeting dell&#39;albero delle decisioni](experience-edit-targeting.md)
>* [Impostazioni esperienza di destinazione](experience-settings-targeting.md)
