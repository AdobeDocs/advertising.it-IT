---
title: Aggiungere un nodo di destinazione di pari livello tra i nodi di un’esperienza
description: Scopri come aggiungere un nodo di pari livello a qualsiasi nodo che ha una destinazione o si trova allo stesso livello di un nodo con una destinazione.
feature: Creative Experiences
exl-id: 915fd399-1c55-49af-94ed-cf49a4154a53
source-git-commit: 05bcaa63779856cfea2f9cd3a0ab5d5e9d3d472a
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 0%

---

# Aggiungere un nodo di destinazione di pari livello tra i nodi di un’esperienza

*Esperienze con targeting solo per la struttura decisionale*
*Versione beta chiusa*

È possibile aggiungere un nodo di pari livello a qualsiasi nodo che ha una destinazione o si trova allo stesso livello di un nodo con una destinazione.

<!-- 1. Open the decision tree:


In a new experience


In an existing experience,
 -->

1. Sopra il nodo a cui si desidera aggiungere il nodo di pari livello, fare clic su ![Aggiungi](/help/creative/assets/add.png "Aggiungi"), quindi selezionare **[!UICONTROL Insert Sibling Target]**.

1. Specificare le destinazioni:

   * Per le destinazioni Adobe Audience, effettua le seguenti operazioni:

      1. Fare clic su **[!UICONTROL Click to Browse]** per aprire le opzioni [!UICONTROL Audience Targeting], aprire la scheda **[!UICONTROL Adobe Segments]**, specificare una o più destinazioni del pubblico [!DNL Adobe] dell&#39;inserzionista e quindi fare clic su **[!UICONTROL Save]**.

      1. (Facoltativo) Per creare più nodi di destinazione quando sono specificati più tipi di pubblico, selezionare **[!UICONTROL Split targets to create nodes]**.

         Questa funzione crea un nodo di destinazione separato (con bundle creativi separati) per ogni pubblico specificato. Se non si dividono le destinazioni, l&#39;utente deve appartenere a tutti i tipi di pubblico specificati (un&#39;istruzione [!DNL Boolean] `AND`).

      1. Fare clic su **[!UICONTROL Apply]**.

   * Per i target geografici, effettuare le seguenti operazioni:

      1. Fare clic su **[!UICONTROL Click to Browse]** per aprire le opzioni [!UICONTROL Geo Targeting], specificare una o più destinazioni geografiche e quindi fare clic su **[!UICONTROL Save]**.

         Le destinazioni di codici postali dispongono di opzioni di modifica in blocco. Per incollare più codici postali, fare clic sulla scheda **[!UICONTROL Paste postal codes]**, selezionare il paese, incollare o immettere codici postali separati da virgole o su righe separate, quindi fare clic su **[!UICONTROL Include All]**. Per rimuovere una destinazione di CAP inclusa, posizionare il cursore sulla destinazione e fare clic su ![Rimuovi](/help/creative/assets/delete.png "Rimuovi") **[!UICONTROL Remove]**.

      1. (Facoltativo) Per creare più nodi di destinazione quando sono specificate più destinazioni geografiche, selezionare **[!UICONTROL Split targets to create nodes]**.

         Questa funzione crea un nodo di destinazione separato (con bundle creativi separati) per ogni destinazione geografica specificata. Se non si dividono le destinazioni, l&#39;utente deve appartenere a tutte le posizioni specificate (un&#39;istruzione [!DNL Boolean] `AND`).

      1. Fare clic su **[!UICONTROL Apply]**.

   * Per gli oggetti passaggio dati, personalizzare facoltativamente la chiave passaggio dati, immettere un singolo valore passaggio dati e quindi fare clic su **[!UICONTROL Apply]**.

     Un valore predefinito per la chiave nella coppia chiave-valore è già impostato nel campo **[!UICONTROL Data Pass]** nella sezione [!UICONTROL Advanced] delle [impostazioni esperienza](experience-settings-targeting.md). Facoltativamente, puoi personalizzare la chiave.

   * Per il retargeting delle destinazioni pixel, seleziona il pixel di retargeting da utilizzare e i valori richiesti per qualsiasi attributo del pixel che deve essere presente per mostrare le creatività. Quindi fare clic su **[!UICONTROL Apply]**.

     Gli attributi per il pixel di retargeting sono configurati nelle [impostazioni pixel di retargeting](/help/creative/pixels/retargeting-pixel-manage.md).

   * Per i dispositivi di destinazione, effettuare le seguenti operazioni:

      1. Seleziona le destinazioni.

      1. (Facoltativo) Per creare più nodi di destinazione quando sono specificate più destinazioni geografiche, selezionare **[!UICONTROL Split targets to create nodes]**.

         Questa funzione crea un nodo di destinazione separato (con bundle creativi separati) per ogni destinazione geografica specificata. Se non si dividono le destinazioni, l&#39;utente deve appartenere a tutte le posizioni specificate (un&#39;istruzione [!DNL Boolean] `AND`).

      1. Fare clic su **[!UICONTROL Apply]**.

1. Effettua una delle seguenti operazioni:

   * (Facoltativo) [Assegna creatività](experience-assign-creative-bundles.md) al nuovo nodo di destinazione.

   * (Facoltativo) Per salvare l&#39;esperienza:

      1. Fare clic su **[!UICONTROL Save]** e quindi su **[!UICONTROL OK]**.

      1. (Se ogni nodo al livello più basso non include almeno un elemento creativo): effettua una delle seguenti operazioni:

         * Per salvare l&#39;esperienza senza tutti i bundle creativi richiesti, fare clic su **[!UICONTROL Save as Draft]**.

           Non puoi creare un tag annuncio per una bozza di esperienza.

         * Per assegnare la creatività predefinita a ogni destinazione a cui non è già stato assegnato un bundle creativo, fare clic su **[!UICONTROL Assign Default Creatives]**. Dopo aver esaminato la struttura aggiornata con i creativi predefiniti assegnati, fare clic su **[!UICONTROL Save]** e **[!UICONTROL OK]**.

         * Per continuare a modificare la struttura decisionale, fare clic su **[!UICONTROL Continue Edit]**.

>[!MORELIKETHIS]
>
>* [Aggiungere un nodo di destinazione al livello finale](experience-target-node-add-final.md)
>* [Inserire un nodo di destinazione tra i nodi](experience-target-node-add-inner.md)
>* [Copia nodi figlio e creativi in un altro nodo allo stesso livello](experience-target-node-copy.md)
>* [Assegna creatività a un nodo finale](experience-assign-creative-bundles.md)
>* [Eliminare un nodo di destinazione o un nodo foglia creativo](/help/creative/experiences/experience-target-node-delete.md)
>* [Crea un&#39;esperienza con il targeting dell&#39;albero delle decisioni](experience-create-targeting.md)
>* [Modifica un&#39;esperienza con il targeting dell&#39;albero delle decisioni](experience-edit-targeting.md)
>* [Impostazioni esperienza di destinazione](experience-settings-targeting.md)
