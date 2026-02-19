---
title: Gestire i cataloghi dei feed
description: Scopri come gestire i cataloghi di feed.
feature: Creative Dynamic Creatives
exl-id: d3ee20ba-5359-4dbe-bc76-269dc800843c
source-git-commit: ad7d2b02103b5a45dadcd51b60621c31e9db0d29
workflow-type: tm+mt
source-wordcount: '462'
ht-degree: 0%

---

# Gestire i cataloghi dei feed

I cataloghi di feed elaborati sono insiemi di potenziali varianti di annunci creati da un file di feed specificato e da un modello di feed specificato. Gli annunci HTML5 e video dinamici, ma non gli annunci HTML5 statici, richiedono un catalogo per creare annunci dinamici.

Prima di poter creare varianti di annunci e [aggiungere annunci dinamici a una libreria creativa](/help/creative/creative-libraries/creative-add-dynamic.md), elabora il catalogo. In seguito sarà possibile aggiornare il file di feed e rielaborare il catalogo per creare un nuovo set di varianti di annunci.<!-- I should list somewhere what happens when you add, update, or remove: I don't think we rewrite existing ads in the creative library, but only add to them. -->

Ogni file di feed può elaborare fino a 500 righe con risorse video.

>[!TIP]
>
>Per tutti gli account con video dinamici, la best practice consiste nel [scaricare il modello di feed universale [!UICONTROL Adobe Creative Template]](feed-template-manage.md), mappare ogni campo nel file di risorse su un campo nel backend di Advertising Creative, quindi rinominare e caricare il modello di feed. Per creare un catalogo, utilizza il nuovo modello di feed insieme al file di risorsa.

## Creare un catalogo {#feed-catalog-create}

>[!NOTE]
>
>Puoi anche caricare direttamente un catalogo quando [aggiungi creatività dinamica a una libreria creativa](/help/creative/creative-libraries/creative-add-dynamic.md). Tutti i cataloghi creati diventano disponibili nella visualizzazione [!UICONTROL Catalogs] per utilizzi futuri.

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Fare clic sulla scheda **[!UICONTROL Catalog]**.

1. In alto a destra, fare clic su **[!UICONTROL Create]** > **[!UICONTROL Template]**.

1. Specifica le [impostazioni catalogo](#catalog-settings) in base alle esigenze.

1. Fare clic su **[!UICONTROL Next]**.

1. Esamina le potenziali varianti di annuncio che possono essere create per il catalogo.

1. Fare clic su **[!UICONTROL Save]**.

## Modificare un catalogo

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Fare clic sulla scheda **[!UICONTROL Catalog]**.

1. Posizionare il cursore sulla riga del modello e fare clic su **[!UICONTROL Edit]**.

1. Modifica le [impostazioni catalogo](#catalog-settings) in base alle esigenze.

1. Esamina le potenziali varianti di annuncio che possono essere create per il catalogo.

1. Fare clic su **[!UICONTROL Save]**.

## Elaborare un catalogo {#feed-catalog-process}

L’elaborazione di un catalogo rende disponibili le varianti dell’annuncio per creare annunci HTML5 dinamici.

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Fare clic sulla scheda **[!UICONTROL Catalog]**.

1. Posizionare il cursore sulla riga del modello e fare clic su **[!UICONTROL Run Now]**.

## Metti in pausa un catalogo attivo

Sospendere un catalogo per renderlo inattivo.<!-- Can you Activate it again? -->

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Fare clic sulla scheda **[!UICONTROL Templates]**.

1. Posizionare il cursore sulla riga del modello e fare clic su **[!UICONTROL Pause]**.

<!-- Verify if this is available:  1. In the confirmation message, click **[!UICONTROL Pause]**. -->

## Attivare un catalogo in pausa

<!-- Verify if this is available. -->

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Fare clic sulla scheda **[!UICONTROL Templates]**.

1. Posizionare il cursore sulla riga del modello e fare clic su **[!UICONTROL Activate]**.

## Archiviare un catalogo

Archivia un catalogo per eliminarlo.

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Fare clic sulla scheda **[!UICONTROL Templates]**.

1. Posizionare il cursore sulla riga del modello e fare clic su **[!UICONTROL Archive]**.

1. Nel messaggio di conferma, fare clic su **[!UICONTROL Archive]**.

## Impostazioni catalogo {#catalog-settings}

**[!UICONTROL Advertiser]:** Inserzionista che può utilizzare il catalogo.

**[!UICONTROL Asset]:** Il file di feed da utilizzare come input per il catalogo.

**[!UICONTROL Catalog Name]:** Nome di catalogo univoco per l&#39;inserzionista specificato. Per impostazione predefinita, viene utilizzato il nome del file di feed, inclusa l&#39;estensione, che è la best practice per l&#39;identificazione.<!-- must it have a file extension? -->

**[!UICONTROL Template]:** modello di feed da utilizzare per la mappatura dei campi nel file di feed/risorsa specificato ai campi nel backend di Advertising Creative.

>[!MORELIKETHIS]
>
>* [Monitora lo stato dei processi di elaborazione catalogo](/help/creative/feeds/job-status-track.md)
>* [Flussi di lavoro per annunci dinamici](/help/creative/introduction/workflow-dynamic-ads.md)
>* [Gestione file risorse](/help/creative/feeds/asset-manage.md)
>* [Gestisci modelli di feed](/help/creative/feeds/feed-template-manage.md)
>* [Gestisci modelli di annunci dinamici](/help/creative/ad-templates/ad-template-manage.md)
>* [Aggiungere elementi creativi dinamici a una libreria creativa](/help/creative/creative-libraries/creative-add-dynamic.md)
