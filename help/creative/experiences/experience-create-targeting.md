---
title: Creare un’esperienza con il targeting dell’albero decisionale
description: Scopri come creare un’esperienza pubblicitaria mirata utilizzando una struttura decisionale.
feature: Creative Experiences
exl-id: 825fd9af-ca7a-4b44-8e4b-1a6f34edac9e
source-git-commit: 6c75d21daba9a07f17d4f339a0edf4d0bdc06019
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 0%

---

# Creare un’esperienza con il targeting dell’albero decisionale

*Versione beta chiusa*

Crea un’esperienza pubblicitaria mirata utilizzando una struttura decisionale. Ogni esperienza utilizza annunci provenienti da una singola libreria creativa.

>[!NOTE]
>
> Dopo aver creato un’esperienza con targeting, non puoi modificarla in un’esperienza non con targeting, che utilizza un flusso di lavoro diverso.

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. Fare clic su **[!UICONTROL Create New Experience]**.

1. Immetti le [impostazioni generali per l&#39;esperienza](experience-settings-targeting.md).

1. Fare clic su **[!UICONTROL Create]**.

1. Nell’albero decisionale, effettua le seguenti operazioni:

   1. (Facoltativo) Modifica le impostazioni di visualizzazione per l’albero decisionale.

      Le impostazioni vengono salvate fino alla disconnessione.

      * Ingrandire o ridurre spostando il dispositivo di scorrimento.

      * Passare dalla visualizzazione di un elenco verticale a quella di un elenco orizzontale facendo clic su ![Visualizza come struttura verticale](/help/creative/assets/tree-vertical.png "Visualizza come struttura verticale") o ![Visualizza come albero orizzontale](/help/creative/assets/tree-horizontal.png "Visualizza come albero orizzontale").

   1. (Facoltativo) Imposta i target dell’annuncio e le creatività corrispondenti in uno dei seguenti modi:

      * Destinazioni:

        *[Aggiungi un nodo di destinazione al livello finale](experience-target-node-add-final.md) in un&#39;esperienza.

         * [Inserire un nodo di destinazione tra i nodi](experience-target-node-add-inner.md).

         * [Aggiungere un nodo di destinazione di pari livello tra i nodi](experience-target-node-add-sibling.md).

         * [Copia nodi figlio e creativi in un altro nodo allo stesso livello](experience-target-node-copy.md).

      * Pacchetti Creative:

         * [Assegnazione e annullamento dell&#39;assegnazione di creatività a un nodo finale](experience-assign-creative-bundles.md).

           Se non assegni almeno un bundle a ciascun nodo finale, puoi scegliere di utilizzare le creatività predefinite per ciascun nodo non assegnato quando salvi l’esperienza. Per pubblicare un’esperienza, devi assegnare dei bundle o utilizzare le creatività predefinite per ciascun nodo finale.

         * [Personalizza gli URL di tracciamento per i creativi nei bundle assegnati](experience-tracking-urls-targeting.md).

         * [Personalizza l&#39;ottimizzazione creativa e la pianificazione](experience-optimization-scheduling-targeting.md) per i bundle assegnati.

1. (Facoltativo) Passa dalla struttura decisionale alle impostazioni generali:

   * Per aprire le impostazioni generali dalla struttura decisionale, fare clic su **[!UICONTROL Experience Form]** in alto a destra.

   * Per aprire la struttura decisionale dalle impostazioni generali, fare clic su **[!UICONTROL Decision Tree]** in alto a destra.

1. Fare clic su **[!UICONTROL Save]** e quindi eseguire le operazioni seguenti.

   * (Se ogni nodo al livello più basso include almeno un bundle creativo) Fare clic su **[!UICONTROL OK]**.

   * (Se ogni nodo al livello più basso non include almeno un bundle creativo) Effettua una delle seguenti operazioni:

      * Per salvare l&#39;esperienza senza tutti i bundle creativi necessari, fare clic su **[!UICONTROL Save as Draft]**.

        Non puoi creare un tag annuncio per un&#39;esperienza [bozza](experience-about.md#experience-statuses).

      * Per assegnare la creatività predefinita a ogni destinazione a cui non è già stato assegnato un bundle creativo, fare clic su **[!UICONTROL Assign Default Creatives]**. Dopo aver esaminato la struttura aggiornata con i creativi predefiniti assegnati, fare clic su **[!UICONTROL Save]** e **[!UICONTROL OK]**.

      * Per continuare a modificare la struttura decisionale, fare clic su **[!UICONTROL Continue Edit]**.

Quando l&#39;esperienza è attiva, [!DNL Creative] crea automaticamente un tag annuncio per ogni dimensione creativa applicabile.

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
