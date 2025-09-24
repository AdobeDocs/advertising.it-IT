---
title: Gestire i modelli di annunci dinamici
description: Informazioni su xxxx.
feature: Creative Templates
source-git-commit: 5828fada55ba9506589df6088ea58b896084700c
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 0%

---

# Gestire i modelli di annunci dinamici

Crea un modello di annuncio separato per ogni combinazione di tipo di annuncio (HTML5 statico o HTML5 dinamico) e dimensioni dell’annuncio caricando un file HTML5 compresso con il formato di annuncio desiderato. Per gli annunci HTML5 dinamici, puoi anche caricare un file contenente gli attributi dell&#39;annuncio<!-- more clarification? -->.

<!-- add this where/how?: You can use the same feed template for multiple ad templates. -->

<!-- EXPLAIN MORE:  Is this like repropagating a feed file through a template, or can you just change some things? Is generating an ad template a one-time thing, using the existing feed file, but you might later update the file and re-propagation doesn't happen automatically? Clarify the use cases for each.-->

## Creare un modello di annuncio dinamico

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**.

1. In alto a destra, fai clic su **[!UICONTROL Create Ad Template]**

1. Specifica le [impostazioni del modello di annuncio](#ad-template-settings)

1. Fare clic su **[!UICONTROL Create]**.

## Modificare un modello di annuncio dinamico

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**.

1. Posizionare il cursore sulla riga del modello di annuncio e fare clic su **[!UICONTROL Edit]**.

1. Modifica le [impostazioni del modello di annuncio](#ad-template-settings).

1. Fare clic su **[!UICONTROL Save]**.

## Scaricare un modello di annuncio dinamico

<!-- Explain more about what this contains and the format:  Downloaded ad templates are compressed (zipped) files that include XXX as TDF files and the uploaded HTML5 (and attributes?) data. You can open the TDF file in a text editor. -->

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**.

1. Posizionare il cursore sulla riga del modello di annuncio e fare clic su **[!UICONTROL Download]**.

   Il file viene scaricato in base alla normale procedura del browser.

## Eliminare un modello di annuncio dinamico

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**.

1. Posizionare il cursore sulla riga del modello di annuncio e fare clic su **[!UICONTROL Delete]**.

1. Nel messaggio di conferma, fare clic su **[!UICONTROL Delete]**.<!-- Confirm -->

## Creare annunci dinamici da un modello di annuncio

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**.

1. Posizionare il cursore sulla riga del modello di annuncio e fare clic su **[!UICONTROL Create Dynamic Ad]**.

   Nella schermata [!UICONTROL New Dynamic Ad], i campi [!UICONTROL Ad Template Size], [!UICONTROL Ad Template Type] e [!UICONTROL Ad Template] vengono selezionati automaticamente e sono di sola lettura.

1. Specificare le impostazioni degli annunci dinamici per [creare gli annunci dinamici](/help/creative/creative-libraries/creative-add-dynamic.md).

## Impostazioni del modello di annuncio {#ad-template-settings}

### Dettagli del modello di annuncio

**[!UICONTROL Advertiser]**: (sola lettura per i modelli esistenti) l&#39;inserzionista per il quale verranno generati gli annunci.

**[!UICONTROL Ad Template Name]**: nome univoco del modello di annuncio per l&#39;inserzionista.

**[!UICONTROL Ad Template Type]**: (sola lettura per i modelli esistenti) Il formato del modello di annuncio: *HTML5* statico o *Dynamic HTML5*.

**[!UICONTROL Ad Template Size]**: (sola lettura per i modelli esistenti) le dimensioni degli annunci creati dal modello.

**[!UICONTROL Description]**: (facoltativo) informazioni utili per chiunque utilizzi il modello di annuncio.

<!-- I don't see this on 9/24:

### (Static HTML5 ad templates) Click Tags

**\[Click Tag Parameter\]**: The click tag parameters to allow click-tracking redirects from ads created using the ad template. To add a parameter, click **[!UICONTROL + Add More]** and enter an additional parameter. You can include up to five parameters.

-->

### zip HTML5

Un file HTML5 compresso con il formato di annuncio desiderato. Se hai già caricato un file, viene elencato il nome del file.

Consulta la [specifica creativa di HTML5](/help/creative/creative-libraries/html5-creative-specification.md).

Per caricare un file:

1. Fare clic su **[!UICONTROL Upload HTML5 zip]**.

1. Individuare il file sul dispositivo o sulla rete.

### (Modelli di annunci Dynamic HTML5) File di attributi

<!-- EXPLAIN -->Un file che contiene gli attributi per il modello di annuncio. Se hai già caricato un file, viene elencato il nome del file.

<!-- Add specs for this file type -->

Per caricare un file:

1. Fare clic su **[!UICONTROL Upload Attributes File]**.

1. Individuare il file sul dispositivo o sulla rete.

>[!MORELIKETHIS]
>
>* [Flusso di lavoro per annunci dinamici](/help/creative/introduction/workflow-dynamic-ads.md)
>* [Gestione file risorse](/help/creative/feeds/asset-manage.md)
>* [Gestisci modelli di feed](/help/creative/feeds/feed-template-manage.md)
>* [Gestisci cataloghi](/help/creative/feeds/catalog-manage.md)
>* [Aggiungere elementi creativi dinamici a una libreria creativa](/help/creative/creative-libraries/creative-add-dynamic.md)

