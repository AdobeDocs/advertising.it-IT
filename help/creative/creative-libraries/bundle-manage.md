---
title: Gestire i bundle creativi
description: Informazioni su xxxx.
feature: Creative Bundles
exl-id: a9ed4e8f-db93-46d5-9231-2b3bb0aa072a
source-git-commit: 97e0f562153983202a2f3641e17dd682ff3d00ea
workflow-type: tm+mt
source-wordcount: '1118'
ht-degree: 0%

---

# Gestire i bundle creativi

*Versione beta chiusa*

<!--
**I'll probably split this up into multiple pages since the creative-related topics are separate**
-->

I bundle sono gruppi di creativi che puoi aggiungere a un’esperienza come un’unica unità. Dopo aver creato un contenitore di bundle, puoi allegare dei creativi al bundle. I bundle standard possono contenere solo annunci standard, mentre i bundle dinamici possono contenere solo annunci dinamici. Puoi sovrascrivere le pagine di destinazione, i tag di tracciamento delle impression e i tag di tracciamento dei clic per tutti i creativi all’interno di un bundle assegnato a un’esperienza dall’interno della struttura decisionale dell’esperienza, senza influire sui creativi di base.

[!DNL Creative] ruota tra le creatività nel bundle come specificato per ogni esperienza a cui è assegnato il bundle. Facoltativamente, puoi consentire a [!DNL Creative] di ottimizzare gli elementi dell&#39;annuncio per qualsiasi esperienza in base alle prestazioni utilizzando la rotazione algoritmica degli annunci, basata su Adobe Sensei.

Per abilitare l’ottimizzazione degli elementi tra i bundle in un’esperienza pubblicitaria, ogni bundle può includere solo una di ogni combinazione \[creative size + language\]. Ad esempio, se un bundle include un contenuto creativo 250x250 con la lingua predefinita &quot;Francese&quot;, non puoi aggiungere un secondo contenuto creativo 250x250 con la lingua predefinita &quot;Francese&quot;. Se hai più creativi della stessa dimensione nella stessa lingua, aggiungili separatamente all’esperienza.

Le creatività collegate ai bundle sono ancora disponibili come singole creatività. Puoi aggiungere un singolo contenuto creativo a più bundle. Se modificate le impostazioni per un contenuto creativo associato a un bundle, le modifiche vengono propagate al bundle. Tuttavia, per l’esperienza vengono sempre utilizzati eventuali pagine di destinazione personalizzate, tag di tracciamento delle impression e tag di tracciamento dei clic configurati per la creatività all’interno di un’esperienza.

<!-- multiselect only to duplicate and delete -->

## Creare un bundle per una libreria creativa

Puoi allegare un contenuto creativo a più bundle.

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Fai clic sul nome della libreria.

1. Fare clic sulla scheda **[!UICONTROL Bundles]**.

1. In alto a destra, fare clic su **[!UICONTROL Create]** > **[!UICONTROL Bundles]** > **[!UICONTROL Bundle]**.

1. Immetti un **[!UICONTROL Bundle Name]** univoco e il **[!UICONTROL Bundle Type]:** *Standard* (per creativi standard) o *Dynamic* (per creativi dinamici.

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

Puoi allegare [creatività standard esistente](/help/creative/creative-libraries/creative-libraries-about.md) a un bundle standard e allegare creatività dinamica esistente<!-- [existing dynamic creatives](creative-dynamic-manage.md) --> a un bundle dinamico. Associando un contenuto creativo a un bundle, il contenuto creativo è disponibile in tutte le esperienze a cui è assegnato il bundle. Ogni bundle può includere solo una di ogni combinazione di \[creative size + language\].

<!--
>[!NOTE]
>
>You can also [attach creatives to bundles from the Standard Ads and Dynamic Ads views](creative-attach-detach-bundles.md).
-->

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Facoltativo) [Personalizzare la visualizzazione](/help/creative/introduction/customize-data-views.md) per includere librerie specifiche.

1. Fai clic sul nome della libreria.

1. Fare clic sulla scheda **[!UICONTROL Bundles]**.

1. Seleziona il bundle:

   * Nella vista a schede, fai clic su **[!UICONTROL ...]** accanto al nome del bundle, quindi su **[!UICONTROL Attach Creatives]**.

   * Nella vista tabella, tenere il cursore sulla riga e fare clic su **[!UICONTROL Attach Creatives]**.

   Ogni creatività idonea al tipo di bundle viene elencata nel frame corretto. Le creatività già collegate al bundle sono elencate ma non selezionabili.

1. Nel frame di destra selezionare la casella di controllo accanto a ogni elemento creativo da allegare al bundle e quindi fare clic su **[!UICONTROL Attach Creative to Bundle]**.

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

## Visualizzare in anteprima un contenuto creativo in un bundle

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

1. (Facoltativo) Per scaricare la creatività, fai clic su ![Scarica](/help/creative/assets/download.png "Scarica").

   Il file viene scaricato in base alla normale procedura del browser.


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
>* [Aggiungere creatività standard a una libreria creativa](/help/creative/creative-libraries/creative-add-standard.md)
>* [Gestisci librerie creative](/help/creative/creative-libraries/creative-library-manage.md)
>* [Informazioni sulle librerie creative](/help/creative/creative-libraries/creative-libraries-about.md)
