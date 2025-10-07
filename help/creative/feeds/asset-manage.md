---
title: Gestire i file di risorse
description: Scopri come caricare e gestire il file di risorse per un inserzionista.
feature: Creative Dynamic Creatives
source-git-commit: 0d7a7ab23173a061961c4b5c66ace5b69a746e86
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%

---

# Gestire i file di risorse

Gli annunci HTML5 dinamici richiedono sia un file di feed in formato foglio di calcolo Microsoft Excel (XLSX) sia le risorse immagine a cui si fa riferimento nel foglio di calcolo (ad eccezione dei riferimenti alle risorse Adobe Experience Manager). Gli annunci statici di HTML5 richiedono una sola risorsa immagine per annuncio.


>[!NOTE]
>
> È possibile utilizzare ogni file di feed per un solo catalogo.

## Requisiti dei file

* Annunci dinamici HTML5:

   * Un file di feed in formato CSV, TSV o foglio di calcolo Microsoft Excel (XLSX), con una riga di intestazione e una riga di dati per ogni variante di annuncio. Includere un nome immagine in ogni riga utilizzando il formato `images/image_name` (ad esempio `images/300x250_acme_logo.png`).

     I nomi dei campi specifici dell&#39;inserzionista devono corrispondere ai [campi disponibili per i file di feed di annunci dinamici](/help/creative/appendix-available-feed-fields.md).

   * Le risorse immagine associate in formato GIF, JPEG, JPG o PNG.<!-- Is this true: The maximum file size is two (2) MB. --> Visualizza le [dimensioni creative supportate](/help/creative/creative-libraries/creative-sizes.md).

   * (Facoltativo) Risorse video in formato MP4 o WEBM

  È possibile caricare un singolo file XLSX, un singolo file di immagine o video o un singolo file ZIP contenente qualsiasi combinazione di file XLSX, di immagini e di video.<!-- Check w/eng re any limitations or best practices WRT number of files and filesize allowed -->

* Annunci HTML5 statici:

   * Una risorsa immagine per annuncio in formato GIF, JPG, JPEG o PNG.

     È possibile caricare una o più immagini in un file ZIP.<!-- Check w/eng re any limitations or best practices WRT number of files and filesize allowed -->

## Caricare un file di risorse

>[!NOTE]
>
>Anziché caricare i file di risorse, puoi anche caricare direttamente un catalogo quando [aggiungi elementi creativi dinamici a una libreria creativa](/help/creative/creative-libraries/creative-add-dynamic.md). Tutti i cataloghi creati diventano disponibili nella visualizzazione [!UICONTROL Catalogs] per utilizzi futuri.

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Fare clic sulla scheda **[!UICONTROL Assets]**.

1. In alto a destra, fare clic su **[!UICONTROL Create]** > **[!UICONTROL Asset]**.

1. Configura il file di risorse:

   1. Seleziona l’inserzionista che può accedere al file della risorsa.

   1. Specificate il file della risorsa in uno dei seguenti modi:

      * Trascinare e rilasciare un file sul dispositivo o sulla rete nella casella.

      * Fare clic su **[!UICONTROL Select a file]** per individuare il file nel dispositivo o nella rete.

   1. Fare clic su **[!UICONTROL Upload]**.

Tutti i file ZIP vengono decompressi automaticamente. Quando si carica un file di foglio di calcolo, il file viene elencato nella scheda secondaria [!UICONTROL Feeds]. Quando si carica un file di immagine, il file è elencato nella scheda secondaria [!UICONTROL Images].

## Scaricare un file di risorse

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Fare clic sulla scheda **[!UICONTROL Assets]**.

1. Posizionare il cursore sulla riga della risorsa e fare clic su **[!UICONTROL Download]**.

   Il file viene scaricato in base alla normale procedura del browser.

## Eliminare un file di risorse

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Fare clic sulla scheda **[!UICONTROL Assets]**.

1. Posizionare il cursore sulla riga della risorsa e fare clic su **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Campi disponibili per i file di feed di annunci dinamici](/help/creative/appendix-available-feed-fields.md)
>* [Flussi di lavoro per annunci dinamici](/help/creative/introduction/workflow-dynamic-ads.md)
>* [Gestisci modelli di feed](/help/creative/feeds/feed-template-manage.md)
>* [Gestisci cataloghi](/help/creative/feeds/catalog-manage.md)
>* [Gestisci modelli di annunci dinamici](/help/creative/ad-templates/ad-template-manage.md)
>* [Aggiungere elementi creativi dinamici a una libreria creativa](/help/creative/creative-libraries/creative-add-dynamic.md)
