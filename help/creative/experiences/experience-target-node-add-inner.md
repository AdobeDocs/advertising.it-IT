---
title: Aggiungere un nodo di destinazione tra i nodi di un’esperienza
description: Scopri come aggiungere un nodo di destinazione tra gli elementi di destinazione in un’esperienza di annuncio.
feature: Creative Experiences
exl-id: ac9211e5-c6ed-4185-bf9c-c2689f1b2775
source-git-commit: 81cbb3cdac21f4b4899b0c07d1eb0686b7b3c7d4
workflow-type: tm+mt
source-wordcount: '849'
ht-degree: 0%

---

# Aggiungere un nodo di destinazione tra i nodi di un’esperienza

*Esperienze con targeting solo per la struttura decisionale*
*Versione beta chiusa*

Quando inserisci un nodo di destinazione tra i livelli esistenti, il nuovo nodo di destinazione mantiene tutte le destinazioni e le creatività secondarie esistenti e inizialmente il nuovo nodo è chiamato &quot;All&quot; (Tutti). Facoltativamente, puoi mantenere il nuovo nodo senza aggiungere destinazioni più specifiche.

Per definire un target specifico, aggiungi un altro nodo di destinazione di pari livello allo stesso livello, specifica il nuovo target, quindi assegna i creativi solo a tale target. L’aggiunta di un nodo di destinazione di pari livello crea il nuovo nodo di destinazione e sposta tutti gli oggetti e le creatività secondari precedentemente assegnati a &quot;All&quot; in un nuovo nodo &quot;Everything Else&quot; allo stesso livello. In questo modo, l’aggiunta della nuova destinazione non influisce sui rami figlio esistenti, perché solo il nuovo nodo di pari livello include le nuove informazioni di targeting.

>[!NOTE]
>
>Per aggiungere un nodo di destinazione al livello inferiore di una struttura decisionale, vedere &quot;[Aggiungere un nodo di destinazione al livello finale in un&#39;esperienza](experience-target-node-add-final.md).&quot;

<!-- 1. [ways to get to the decision tree] -->

1. Nel nodo in cui si desidera inserire la destinazione, fare clic su ![Aggiungi](/help/creative/assets/add.png "Aggiungi"), quindi selezionare **[!UICONTROL Insert New Target]**.

1. Effettuare una delle seguenti operazioni:

   * Se i nodi di pari livello non esistono già, eseguire le operazioni seguenti:

      1. Selezionare il tipo di destinazione, quindi fare clic su **[!UICONTROL Apply]**:

         * Per le destinazioni Adobe Audience, selezionare **[!UICONTROL Adobe Audience]**.

         * Per le destinazioni geografiche, selezionare una singola categoria geografica (ad esempio [!UICONTROL Geo: Country]).

         * Per le destinazioni del passaggio dati, selezionare **[!UICONTROL Data Pass]**.

         * Per il retargeting delle destinazioni pixel, selezionare **[!UICONTROL RT Pixel].

         * Per le destinazioni dispositivo, selezionare una singola categoria di destinazione (**[!UICONTROL Device: Type]**, **[!UICONTROL Device: OS]** o **[!UICONTROL Device: Browser]**).

   * Se i nodi di pari livello esistono già, eseguire le operazioni seguenti:

      * Per le destinazioni Adobe Audience, effettua le seguenti operazioni:

         1. Fare clic su **[!UICONTROL Click to Browse]** per aprire le opzioni [!UICONTROL Audience Targeting], aprire la scheda **[!UICONTROL Adobe Segments]**, specificare una o più destinazioni del pubblico [!DNL Adobe] dell&#39;inserzionista e quindi fare clic su **[!UICONTROL Create]**<!-- Why not "Save" like for the other node types/use cases? -->.

         1. (Facoltativo) Per creare più nodi di destinazione quando sono specificati più tipi di pubblico, selezionare **[!UICONTROL Split targets to create nodes]**.

            Questa funzione crea un nodo di destinazione separato (con bundle creativi separati) per ogni pubblico specificato. Se non si dividono le destinazioni, l&#39;utente deve appartenere a tutti i tipi di pubblico specificati (un&#39;istruzione [!DNL Boolean] `AND`).

         1. Fare clic su **[!UICONTROL Apply]**.

      * Per i target geografici, effettuare le seguenti operazioni:

         1. Fare clic su **[!UICONTROL Click to Browse]** per aprire le opzioni [!UICONTROL Geo Targeting], specificare una o più destinazioni geografiche e quindi fare clic su **[!UICONTROL Save]**.

            Le destinazioni di codici postali dispongono di opzioni di modifica in blocco. Per incollare più codici postali, fare clic sulla scheda **[!UICONTROL Paste postal codes]**, selezionare il paese, incollare o immettere codici postali separati da virgole o su righe separate, quindi fare clic su **[!UICONTROL Include All]**. Per rimuovere una destinazione di CAP inclusa, posizionare il cursore sulla destinazione e fare clic su ![Rimuovi](/help/creative/assets/delete.png "Rimuovi") **[!UICONTROL Remove]**.

         1. (Facoltativo) Per creare più nodi di destinazione quando sono specificate più destinazioni geografiche, selezionare **[!UICONTROL Split targets to create nodes]**.

            Questa funzione crea un nodo di destinazione separato (con bundle creativi separati) per ogni destinazione geografica specificata. Se non si dividono le destinazioni, l&#39;utente deve appartenere a tutte le posizioni specificate (un&#39;istruzione [!DNL Boolean] `AND`).

         1. Fare clic su **[!UICONTROL Apply]**.

      * Per una destinazione di passaggio dati, personalizzare facoltativamente la chiave di passaggio dati, immettere un singolo valore di passaggio dati e quindi fare clic su **[!UICONTROL Apply]**.

        Un valore predefinito per la chiave nella coppia chiave-valore è già impostato nel campo **[!UICONTROL Data Pass]** nella sezione [!UICONTROL Advanced] delle [impostazioni esperienza](experience-settings-targeting.md). Facoltativamente, puoi personalizzare la chiave.

      * Per un target di pixel di retargeting, selezionare un singolo pixel di retargeting da utilizzare e i valori per gli attributi del pixel necessari per mostrare i creativi, quindi fare clic su **[!UICONTROL Apply]**.

        Gli attributi per il pixel di retargeting sono configurati nelle [impostazioni pixel di retargeting](/help/creative/pixels/retargeting-pixel-manage.md).

      * Per i dispositivi di destinazione, effettuare le seguenti operazioni:

         1. Seleziona le destinazioni.

         1. (Facoltativo) Per creare più nodi di destinazione quando sono specificate più destinazioni geografiche, selezionare **[!UICONTROL Split targets to create nodes]**.

            Questa funzione crea un nodo di destinazione separato (con bundle creativi separati) per ogni destinazione geografica specificata. Se non si dividono le destinazioni, l&#39;utente deve appartenere a tutte le posizioni specificate (un&#39;istruzione [!DNL Boolean] `AND`).

         1. (Facoltativo) Per creare più nodi di destinazione quando sono specificate più destinazioni geografiche, selezionare **[!UICONTROL Split targets to create nodes]**.

         1. Fare clic su **[!UICONTROL Apply]**.

1. (Facoltativo) Specifica un nome di ramo personalizzato per un ramo definito dall&#39;utente.

   Per impostazione predefinita, i rami definiti dall’utente sono etichettati con le destinazioni applicate.

   Non puoi creare un nome di ramo personalizzato per un ramo &quot;Tutti&quot; o &quot;Tutti gli altri&quot;.

   1. Tenere premuto il cursore sul nodo di destinazione e fare clic su **[!UICONTROL ...]** > **[!UICONTROL Edit Name]**.

   1. Immettere **[!UICONTROL Node Name]**, quindi fare clic su **[!UICONTROL Save]**.

1. Effettua una delle seguenti operazioni:

   * (Facoltativo) [Assegna creatività](experience-assign-creative-bundles.md) al nuovo nodo di destinazione e al nodo &quot;Tutto il resto&quot;.

   * (Facoltativo) [Aggiungere un nodo di destinazione di pari livello](experience-target-node-add-sibling.md) del tipo di destinazione specificato.

   * (Facoltativo) Per salvare l&#39;esperienza:

      1. Fare clic su **[!UICONTROL Save]** e quindi su **[!UICONTROL OK]**.

      1. (Se ogni nodo al livello più basso non include almeno un elemento creativo): effettua una delle seguenti operazioni:

         * Per salvare l&#39;esperienza senza tutti i bundle creativi necessari, fare clic su **[!UICONTROL Save as Draft]**.

           Non puoi creare un tag annuncio per una bozza di esperienza.

         * Per assegnare la creatività predefinita a ogni destinazione a cui non è già stato assegnato un bundle creativo, fare clic su **[!UICONTROL Assign Default Creatives]**. Dopo aver esaminato la struttura aggiornata con i creativi predefiniti assegnati, fare clic su **[!UICONTROL Save]** e **[!UICONTROL OK]**.

         * Per continuare a modificare la struttura decisionale, fare clic su **[!UICONTROL Continue Edit]**.

>[!MORELIKETHIS]
>
>* [Aggiungere un nodo di destinazione al livello finale](experience-target-node-add-final.md)
>* [Aggiungere un nodo di destinazione di pari livello tra nodi](experience-target-node-add-sibling.md)
>* [Copia nodi figlio e creativi in un altro nodo allo stesso livello](experience-target-node-copy.md)
>* [Assegna creatività a un nodo finale](experience-assign-creative-bundles.md)
>* [Eliminare un nodo di destinazione o un nodo foglia creativo](/help/creative/experiences/experience-target-node-delete.md)
>* [Crea un&#39;esperienza con il targeting dell&#39;albero delle decisioni](experience-create-targeting.md)
>* [Modifica un&#39;esperienza con il targeting dell&#39;albero delle decisioni](experience-edit-targeting.md)
>* [Impostazioni esperienza di destinazione](experience-settings-targeting.md)
