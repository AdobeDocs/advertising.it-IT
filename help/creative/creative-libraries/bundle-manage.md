---
title: Gestire i bundle creativi
description: Informazioni su xxxx.
feature: Creative Bundles
exl-id: a9ed4e8f-db93-46d5-9231-2b3bb0aa072a
source-git-commit: de2a2a097802cc4a7b5ac63bee2eb326895e70f1
workflow-type: tm+mt
source-wordcount: '1462'
ht-degree: 0%

---

# Gestire i bundle creativi

<!--
**I'll probably split this up into multiple pages since the creative-related topics are separate**
-->

I bundle sono gruppi di creativi che puoi aggiungere a un’esperienza come un’unica unità. Dopo aver creato un contenitore di bundle, puoi allegare dei creativi al bundle. I bundle di visualizzazione standard possono contenere solo annunci di visualizzazione standard, i bundle video standard possono contenere solo annunci video standard e i bundle di visualizzazione dinamica possono contenere solo annunci di visualizzazione dinamici. Puoi sovrascrivere le pagine di destinazione, i tag di tracciamento delle impression e i tag di tracciamento dei clic per tutti i creativi all’interno di un bundle assegnato a un’esperienza dall’interno della struttura decisionale dell’esperienza, senza influire sui creativi di base.

[!DNL Creative] ruota tra le creatività nel bundle come specificato per ogni esperienza a cui è assegnato il bundle. Facoltativamente, puoi consentire a [!DNL Creative] di ottimizzare gli elementi dell&#39;annuncio per qualsiasi esperienza in base alle prestazioni utilizzando la rotazione algoritmica degli annunci, basata su [!DNL Adobe AI].

Per abilitare l’ottimizzazione degli elementi dell’annuncio tra i bundle in un’esperienza pubblicitaria, ogni bundle può includere solo una di ogni combinazione di \[dimensione creativa o durata + lingua\]. Ad esempio, se un bundle include un contenuto creativo 250x250 con la lingua predefinita &quot;Francese&quot;, non puoi aggiungere un secondo contenuto creativo 250x250 con la lingua predefinita &quot;Francese&quot;. Se hai più creativi della stessa dimensione nella stessa lingua, aggiungili separatamente all’esperienza.

Le creatività collegate ai bundle sono ancora disponibili come singole creatività. Puoi aggiungere un singolo contenuto creativo a più bundle. Se modificate le impostazioni per un contenuto creativo associato a un bundle, le modifiche vengono propagate al bundle. Tuttavia, per l’esperienza vengono sempre utilizzati eventuali pagine di destinazione personalizzate, tag di tracciamento delle impression e tag di tracciamento dei clic configurati per la creatività all’interno di un’esperienza.

<!-- multiselect only to duplicate and delete -->

## Creare un bundle per una libreria creativa

Puoi allegare un contenuto creativo a più bundle.

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Fai clic sul nome della libreria.

1. Fare clic sulla scheda **[!UICONTROL Bundles]**.

1. In alto a destra, fare clic su **[!UICONTROL Create]** > **[!UICONTROL Bundles]** > **[!UICONTROL Bundle]**.

1. Immetti un **[!UICONTROL Bundle Name]** univoco e il **[!UICONTROL Bundle Type]:** *Visualizzazione standard* (per le creatività di visualizzazione standard), *Visualizzazione dinamica* (per le creatività di visualizzazione dinamica), *Video standard* (per le creatività di video standard).

1. Fare clic su **[!UICONTROL Create]**.

## Elencare i creativi in un pacchetto

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Facoltativo) [Personalizzare la visualizzazione](/help/creative/introduction/customize-data-views.md) per includere librerie specifiche.

1. Fai clic sul nome della libreria.

1. Fare clic sulla scheda **[!UICONTROL Bundles]**.

1. Fai clic sulla scheda o sulla riga del bundle per visualizzare tutti i creativi presenti nel bundle.

## Bundle duplicati

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Facoltativo) [Personalizzare la visualizzazione](/help/creative/introduction/customize-data-views.md) per includere librerie specifiche.

1. Fai clic sul nome della libreria.

1. Fare clic sulla scheda **[!UICONTROL Bundles]**.

1. Seleziona i bundle da duplicare:

   * Per duplicare un singolo bundle:

      * Nella vista a schede, fai clic su **[!UICONTROL ...]** accanto al nome del bundle, quindi su **[!UICONTROL Duplicate]**.

      * Nella vista tabella, tenere il cursore sulla riga e fare clic su **[!UICONTROL Duplicate]**.

   * Per duplicare uno o più bundle, seleziona la casella di controllo di ciascun bundle che desideri duplicare. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL Duplicate].**

     Per selezionare tutte le righe, selezionare la casella di controllo globale in alto a sinistra.

   I nuovi bundle sono denominati `<original name> (copy) # 1` (o il numero successivo nella sequenza). Ad esempio, se effettui due duplicati di &quot;Bundle di prova&quot;, i duplicati vengono denominati &quot;Bundle di prova (copia) # 1&quot; e &quot;Bundle di prova (copia) # 2&quot;.

## Modificare un nome bundle

Le modifiche al nome di un bundle vengono propagate tra tutte le esperienze associate.

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Fai clic sul nome della libreria.

1. Fare clic sulla scheda **[!UICONTROL Bundles]**.

1. Seleziona il bundle:

   * Nella vista a schede, fare clic su **[!UICONTROL ...]** accanto al nome della libreria, quindi fare clic su **[!UICONTROL Edit]**.

   * Nella vista tabella, tenere il cursore sulla riga e fare clic su **[!UICONTROL Edit]**.

1. Modifica **[!UICONTROL Bundle Name]**.

   [!UICONTROL Bundle Name] deve essere univoco.

1. Fare clic su **[!UICONTROL Update]**.<!-- inconsistent with "Edit" for creative libraries and creatives -->

## Associa creatività a un bundle

È possibile allegare le creatività di visualizzazione standard esistenti a un bundle di visualizzazione standard, le creatività di video standard a bundle video standard e le creatività di visualizzazione dinamiche a un bundle dinamico. Associando un contenuto creativo a un bundle, il contenuto creativo è disponibile in tutte le esperienze a cui è assegnato il bundle. Ogni bundle può includere solo una di ogni combinazione di \[creative size or duration + language\].

>[!NOTE]
>
>Puoi anche [allegare contenuti creativi ai bundle dalle visualizzazioni Annunci standard e Annunci dinamici](creative-attach-detach-bundles.md).

### Associa creatività a un bundle dall’elenco Bundle

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Facoltativo) [Personalizzare la visualizzazione](/help/creative/introduction/customize-data-views.md) per includere librerie specifiche.

1. Fai clic sul nome della libreria.

1. Fare clic sulla scheda **[!UICONTROL Bundles]**.

1. Seleziona il bundle:

   * Nella vista a schede, fai clic su **[!UICONTROL ...]** accanto al nome del bundle, quindi su **[!UICONTROL Attach Creatives]**.

   * Nella vista tabella, tenere il cursore sulla riga e fare clic su **[!UICONTROL Attach Creatives]**.

   Ogni creatività idonea al tipo di bundle viene elencata nel frame corretto. Le creatività già collegate al bundle sono elencate ma non selezionabili.

1. (Facoltativo) Passa dalla vista tabella predefinita a una vista a schede dei bundle disponibili facendo clic su ![Vista a schede](/help/creative/assets/card-view-button.png "Vista a schede") per aprire la vista a schede o su ![Vista a tabella/elenco](/help/creative/assets/table-view-button.png "Vista tabella") per tornare alla vista a tabella.

1. Nel frame di destra selezionare la casella di controllo accanto a ogni elemento creativo da allegare al bundle e quindi fare clic su **[!UICONTROL Attach Creative to Bundle]**.

### Allega i creativi a un bundle dall&#39;elenco creativo del bundle

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Facoltativo) [Personalizzare la visualizzazione](/help/creative/introduction/customize-data-views.md) per includere librerie specifiche.

1. Fai clic sul nome della libreria.

1. Fare clic sulla scheda **[!UICONTROL Bundles]**.

1. Fai clic sulla scheda o sulla riga del bundle per visualizzare tutti i creativi presenti nel bundle.

1. In alto a destra, fare clic su **[!UICONTROL Attach Creatives]**.

1. Nel pannello a destra, seleziona la casella di controllo per ogni contenuto creativo che desideri allegare.

1. Fare clic su **[!UICONTROL Attach Creatives to Bundle]**.

## Scollegare i creativi da un pacchetto {#bundle-detach-creatives}

Se si stacca un contenuto creativo da un bundle, viene rimossa l’associazione tra i due elementi, pertanto il contenuto creativo non viene più utilizzato per le esperienze che hanno come target il bundle.

Staccando un contenuto creativo dal bundle, il contenuto non viene eliminato dalla scheda Creativi della libreria creativa.

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Facoltativo) [Personalizzare la visualizzazione](/help/creative/introduction/customize-data-views.md) per includere librerie specifiche.

1. Fai clic sul nome della libreria.

1. Fare clic sulla scheda **[!UICONTROL Bundles]**.

1. Fai clic sulla scheda o sulla riga del bundle per visualizzare tutti i creativi presenti nel bundle.

1. Seleziona le creatività da scollegare dal bundle:

   * Per scollegare un singolo contenuto creativo:

      * Nella visualizzazione a schede, fare clic su **[!UICONTROL ...]** accanto al nome della creatività e quindi su **[!UICONTROL Detach]**.

      * Nella vista tabella, tenere il cursore sulla riga e fare clic su **[!UICONTROL Detach]**.

   * Per scollegare uno o più creativi, selezionare la casella di controllo relativa a ogni creativo che si desidera scollegare. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL Detach]**.

     Per selezionare tutte le righe, selezionare la casella di controllo globale in alto a sinistra.

## Visualizzare in anteprima un singolo contenuto creativo in un bundle

Puoi visualizzare in anteprima un contenuto creativo così come verrà visualizzato dagli utenti, compresi i collegamenti ipertestuali.

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Facoltativo) [Personalizzare la visualizzazione](/help/creative/introduction/customize-data-views.md) per includere librerie specifiche.

1. Fai clic sul nome della libreria.

1. Fare clic sulla scheda **[!UICONTROL Bundles]**.

1. Fai clic sulla scheda o sulla riga del bundle per visualizzare tutti i creativi presenti nel bundle.

1. Seleziona il contenuto creativo:

   * Nella visualizzazione a schede, fare clic su **[!UICONTROL ...]** accanto al nome della creatività e quindi su **[!UICONTROL Preview]**.

   * Nella vista tabella, tenere il cursore sulla riga e fare clic su **[!UICONTROL Preview]**.

1. (Facoltativo) Per ridimensionare l&#39;immagine nello schermo, selezionare un&#39;opzione nell&#39;elenco **[!UICONTROL Zoom]**, dal 10% al 100% delle dimensioni dell&#39;immagine.

<!-- Not there as of 1/22/24:  1. (Flexible HTML5 creatives; optional) To show all frames for the creative, select **Show frames**. -->

1. (Facoltativo) Per aprire la pagina di destinazione del contenuto creativo, fai clic sul contenuto.

<!-- Verify:  Will the creative click be tracked like a regular ad click but not linked to a publisher and placement? Explain effect/consequences. -->

1. (Facoltativo) Per scaricare la creatività, fai clic su ![Scarica](/help/creative/assets/download.png "Scarica").

   Il file viene scaricato in base alla normale procedura del browser.

## Anteprima di tutti i creativi in un bundle

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Fai clic sul nome della libreria.

1. Fare clic sulla scheda **[!UICONTROL Bundles]**.

1. Seleziona il bundle:

   * Nella vista a schede, fai clic su **[!UICONTROL ...]** accanto al nome del bundle, quindi su **[!UICONTROL Preview]**.

   * Nella vista tabella, tenere il cursore sulla riga e fare clic su **[!UICONTROL Preview]**.

1. (Facoltativo) Per filtrare i creativi per lingua, selezionare un&#39;opzione nell&#39;elenco **[!UICONTROL Language]**, quindi fare clic su **[!UICONTROL Preview]** in alto a destra nell&#39;anteprima.

1. (Facoltativo) Per filtrare i creativi in base alle dimensioni, selezionare un&#39;opzione nell&#39;elenco **[!UICONTROL Size]**, quindi fare clic su **[!UICONTROL Preview]** in alto a destra nell&#39;anteprima.

1. (Facoltativo) Per ridimensionare le immagini nello schermo, selezionare un&#39;opzione nell&#39;elenco **[!UICONTROL Zoom]**, dal 10% al 100% delle dimensioni dell&#39;immagine.

1. (Facoltativo) Per aprire la pagina di destinazione di un contenuto creativo, fai clic sul contenuto creativo.

<!-- Verify:  Will the creative click be tracked like a regular ad click but not linked to a publisher and placement? Explain effect/consequences. -->

1. (Facoltativo) Per condividere un URL demo in modo che altre persone senza un accesso a [!DNL Creative] possano visualizzare l&#39;anteprima dei creativi:

   1. Fai clic su ![Condividi](/help/creative/assets/share.png "Condividi") in alto a destra nell&#39;anteprima.

   1. Nella finestra di dialogo [!UICONTROL Share Demo URL], fai clic su **[!UICONTROL Copy]** per copiare l&#39;URL negli Appunti e condividerlo con un altro utente.

<!-- Not there as of 1/22/25:

## Edit the landing page and tracking tags for the creatives in a standard creative bundle

*Standard creative bundles only*

[Verify and edit all this, including the command names and where they're available. This is supposed to be a single and bulk action from within the right frame when you've open bundle details for a single bundle -- not from the Bundles table view.]

This procedure customizes the landing page, impression-tracking tags, and click-tracking tags for the creatives only within the context of the bundle. It doesn't change the settings for the base creative in [!UICONTROL Creative Libraries].

The custom URL and tags are applied to a creative when the bundle is assigned to an experience and the creative is served for the experience.

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Optional) [Customize the view](/help/creative/introduction/customize-data-views.md) to include specific libraries.

1. Click the library name.

1. Click the **[!UICONTROL Bundles]** tab.

1. Click the bundle name.

1. In the right pane, XXXXXXXXXXXX.

1. 

1. Edit any of the following settings: **[!UICONTROL Landing Page]**, **[!UICONTROL Click Tags]**, **[!UICONTROL Impression Tags]**.[Verify, and is can you do this for only one creative or is multiselect available?]

1.

 -->

## Elimina bundle

Puoi eliminare i bundle non assegnati a un&#39;esperienza [live](/help/creative/experiences/experience-about.md#experience-statuses-experience-statuses). Se un bundle è assegnato a un&#39;esperienza live, [rimuovi il bundle dalla struttura decisionale](/help/creative/experiences/experience-target-node-delete.md) per l&#39;esperienza prima di continuare.

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Facoltativo) [Personalizzare la visualizzazione](/help/creative/introduction/customize-data-views.md) per includere librerie specifiche.

1. Fai clic sul nome della libreria.

1. Fare clic sulla scheda **[!UICONTROL Bundles]**.

1. Seleziona i bundle da eliminare:

   * Per eliminare un singolo bundle:

      * Nella vista a schede, fai clic su **[!UICONTROL ...]** accanto al nome del bundle, quindi su **[!UICONTROL Delete]**.

      * Nella vista tabella, tenere il cursore sulla riga e fare clic su **[!UICONTROL Delete]**.

   * Per eliminare uno o più bundle, seleziona la casella di controllo relativa a ciascun bundle che desideri eliminare. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL Delete].**

     Per selezionare tutte le righe, selezionare la casella di controllo globale in alto a sinistra.

1. Nel messaggio di conferma, fare clic su **[!UICONTROL Delete].**

<!--
>* [Overview of implementing Adobe Advertising Creative](/help/creative/introduction/implementation-overview.md)
>* [How the user interface is organized](/help/creative/introduction/ui.md)
-->

>[!MORELIKETHIS]
>
>* [Assegnazione e annullamento dell&#39;assegnazione di bundle creativi a un nodo finale in un&#39;esperienza](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [Anteprima di un contenuto creativo](/help/creative/creative-libraries/creative-preview.md)
>* [Aggiungere creatività standard a una libreria creativa](/help/creative/creative-libraries/creative-add-standard.md)
>* [Gestisci librerie creative](/help/creative/creative-libraries/creative-library-manage.md)
>* [Informazioni sulle librerie creative](/help/creative/creative-libraries/creative-libraries-about.md)
