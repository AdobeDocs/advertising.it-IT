---
title: Allega annunci ai posizionamenti
description: Scopri come allegare gli annunci ai posizionamenti.
feature: DSP Ads
exl-id: bca590c9-e0d0-41e6-96b1-26ea5b2f842f
source-git-commit: 86acfaecdf761adc7c6585a49dbcdf4490290a8c
workflow-type: tm+mt
source-wordcount: '901'
ht-degree: 0%

---

# Allega annunci ai posizionamenti

Utilizza la visualizzazione [!UICONTROL Ad Tools] per allegare annunci ai posizionamenti, allegare pixel di tracciamento di terze parti agli annunci e scollegare dagli annunci i pixel di tracciamento di terze parti esistenti.

>[!NOTE]
>
>Gli annunci video universali possono essere collegati solo ai posizionamenti video universali.

## Apri la visualizzazione [!UICONTROL Ad Tools] {#ad-tools-open}

1. Nel menu principale, fare clic su **[!UICONTROL Campaigns]**.

1. Fai clic sul nome della campagna.

1. Aprire la visualizzazione [!UICONTROL Ad Tools] in uno dei modi seguenti:

   * (Dalla visualizzazione [!UICONTROL Packages] , [!UICONTROL Placements] o [!UICONTROL Ads]) In alto a destra, fare clic su **[!UICONTROL ...]** > **[!UICONTROL Ad Tools]**.

   * Nella visualizzazione [!UICONTROL Placements] accanto al nome del posizionamento, fare clic su **[!UICONTROL ...]** > **[!UICONTROL Attach Ads].**

   * Nella visualizzazione [!UICONTROL Ads] accanto al nome dell&#39;annuncio, fare clic su **[!UICONTROL ...]** > **[!UICONTROL Add to Placements]**.

   La scheda [!UICONTROL Attach Ads] è selezionata per impostazione predefinita.

## Allega annunci ai posizionamenti {#attach-ads-campaign}

1. [Aprire la visualizzazione [!UICONTROL Ad Tools]](#ad-tools-open).

1. Nella visualizzazione secondaria [!UICONTROL Edit], eseguire le operazioni seguenti per ogni gruppo di annunci che si desidera allegare ai posizionamenti:

   1. (Facoltativo) Individua posizionamenti e annunci specifici in uno dei seguenti modi:

      * Sopra la tabella sinistra, fare clic su ![Filtro](/help/dsp/assets/filter.png) e filtrare gli elenchi in base al pacchetto, al tipo di posizionamento, allo stato del posizionamento, al tipo di annuncio o allo stato dell&#39;annuncio.

      * Sopra le tabelle di destra e di sinistra, cerca stringhe di testo specifiche nel posizionamento e nei nomi degli annunci.

   1. Nella tabella a sinistra, seleziona la casella di controllo accanto a ciascun posizionamento a cui allegare gli annunci.

   1. Nella tabella a destra, seleziona la casella di controllo accanto a ogni annuncio che desideri allegare ai posizionamenti selezionati.

      Sono selezionabili solo gli annunci applicabili per il tipo di posizionamento e che non sono già allegati ai posizionamenti selezionati.

   1. In basso a destra, fare clic su **[!UICONTROL Attach]**.

1. (Facoltativo) Per tornare alle visualizzazioni dettagli campagna, fai clic su ![Torna alla cartella](/help/dsp/assets/breadcrumb-return.png "Torna alla cartella") a sinistra di [!UICONTROL Ad Tools] e seleziona il nome della campagna.

## Visualizza annunci allegati ai posizionamenti {#view-ads-campaign}

<!-- should be a separate page, combined with "List the Placements Associated with an Ad" (although that pertains to a single ad only), or maybe just rename this topic -->

1. [Aprire la visualizzazione [!UICONTROL Ad Tools]](#ad-tools-open).

1. Passa all&#39;opzione **[!UICONTROL View]** in alto a destra.

1. (Facoltativo) Individua posizionamenti e annunci specifici in base alle esigenze:

   * Sopra la tabella sinistra, fare clic su ![Filtro](/help/dsp/assets/filter.png) e filtrare gli elenchi in base al pacchetto, al tipo di posizionamento, allo stato del posizionamento, al tipo di annuncio o allo stato dell&#39;annuncio.

   * Nelle tabelle di destra e di sinistra, cerca stringhe di testo specifiche nel posizionamento o nel nome dell’annuncio.

1. Fai clic su una riga di posizionamento nella tabella a sinistra per visualizzare gli annunci allegati nella tabella a destra.

1. (Facoltativo) Per allegare altri annunci ai posizionamenti della campagna, passa alla vista **[!UICONTROL Edit]** in alto a destra. Per istruzioni, vedi il passaggio 2 della procedura precedente, &quot;[Allega annunci ai posizionamenti](#attach-ads-campaign)&quot;.

## Allegare pixel di tracciamento di terze parti agli annunci in un posizionamento {#attach-pixels-ads}

1. [Aprire la visualizzazione [!UICONTROL Ad Tools]](#ad-tools-open).

1. Fare clic sulla scheda **[!UICONTROL Attach Pixels]**.

1. Nella visualizzazione secondaria [!UICONTROL Edit]:

   1. (Facoltativo) Individua annunci e pixel di terze parti in uno dei seguenti modi:

      * Sopra la tabella sinistra, fare clic su ![Filtro](/help/dsp/assets/filter.png) e filtrare gli elenchi in base allo stato dell&#39;annuncio, al tipo di annuncio, all&#39;evento di integrazione dei pixel o al tipo di pixel.

      * Sopra le tabelle di destra e di sinistra, cerca stringhe di testo specifiche nei nomi degli annunci e nei nomi dei pixel.

   1. (Se per la campagna non esistono pixel di tracciamento di terze parti) Crea un pixel:

      1. Nella tabella a destra, fare clic su **[!UICONTROL Create pixel]**.

      1. Specificare le impostazioni:

         **[!UICONTROL Integration Event]:** L&#39;evento che attiva il pixel da attivare, ad esempio *[!UICONTROL Impression]* o *[!UICONTROL Click-through]*.

         **[!UICONTROL Pixel Type]:** Se il pixel è un *[!UICONTROL IMG URL]* (file immagine 1x1 pixel), *[!UICONTROL HTML]* o *[!UICONTROL JavaScript URL]*.

         **[!UICONTROL Pixel URL or Code]:** URL dell&#39;immagine pixel nel formato appropriato per il tipo di pixel specificato.

         **[!UICONTROL Pixel Name]:** Il nome del pixel. Utilizza un nome che ti consenta di identificare facilmente il pixel.

         **[!UICONTROL Pixel Provider]:** Provider pixel: *[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]* o *[!UICONTROL IAS]*.

      1. Fare clic su **[!UICONTROL Save]**.

   1. Nella tabella a sinistra, seleziona la casella di controllo accanto a ogni annuncio per il quale desideri allegare pixel di tracciamento di terze parti.

   1. Nella tabella a destra, seleziona la casella di controllo accanto a ciascun pixel di tracciamento di terze parti che desideri allegare agli annunci selezionati.

      È possibile selezionare solo i pixel che non sono già allegati agli annunci selezionati.

   1. In basso a destra, fare clic su **[!UICONTROL Attach]**.

1. (Facoltativo) Per tornare alle visualizzazioni dettagli campagna, fai clic su ![Torna alla cartella](/help/dsp/assets/breadcrumb-return.png "Torna alla cartella") a sinistra di [!UICONTROL Ad Tools] e seleziona il nome della campagna.

## Staccare i pixel di tracciamento di terze parti dagli annunci in un posizionamento {#detach-pixels-ads}

1. [Aprire la visualizzazione [!UICONTROL Ad Tools]](#ad-tools-open).

1. Fare clic sulla scheda **[!UICONTROL Attach Pixels]**.

1. Nella visualizzazione secondaria [!UICONTROL Edit]:

   1. (Facoltativo) Individua annunci e pixel di terze parti in uno dei seguenti modi:

      * Sopra la tabella sinistra, fare clic su ![Filtro](/help/dsp/assets/filter.png) e filtrare gli elenchi in base allo stato dell&#39;annuncio, al tipo di annuncio, all&#39;evento di integrazione dei pixel o al tipo di pixel.

      * Sopra le tabelle di destra e di sinistra, cerca stringhe di testo specifiche nei nomi degli annunci e nei nomi dei pixel.

   1. Nella tabella a sinistra, seleziona la casella di controllo accanto a ogni annuncio da cui desideri scollegare i pixel di tracciamento di terze parti.

   1. Nella tabella a destra, seleziona la casella di controllo accanto a ciascun pixel di tracciamento di terze parti che desideri staccare dagli annunci selezionati.

      Sono selezionabili solo i pixel allegati a tutti gli annunci selezionati.

   1. In basso a destra, fare clic su **[!UICONTROL Detach]**.

1. (Facoltativo) Per tornare alle visualizzazioni dettagli campagna, fai clic su ![Torna alla cartella](/help/dsp/assets/breadcrumb-return.png "Torna alla cartella") a sinistra di [!UICONTROL Ad Tools] e seleziona il nome della campagna.

## Pixel di visualizzazione allegati agli annunci {#view-pixels-ads}

1. [Aprire la visualizzazione [!UICONTROL Ad Tools]](#ad-tools-open).

1. Fare clic sulla scheda **[!UICONTROL Attach Pixels]**.

1. Passa all&#39;opzione **[!UICONTROL View]** in alto a destra.

1. (Facoltativo) Individua annunci e pixel di terze parti in base alle esigenze:

   * Sopra la tabella sinistra, fare clic su ![Filtro](/help/dsp/assets/filter.png) e filtrare gli elenchi in base allo stato dell&#39;annuncio, al tipo di annuncio, all&#39;evento di integrazione dei pixel o al tipo di pixel.

   * Sopra le tabelle di destra e di sinistra, cerca stringhe di testo specifiche nei nomi degli annunci e nei nomi dei pixel.

1. Fai clic su una riga di annunci nella tabella a sinistra per visualizzare i pixel associati nella tabella a destra.

1. (Facoltativo) Per allegare altri pixel agli annunci, passa alla visualizzazione **[!UICONTROL Edit]** in alto a destra. Per istruzioni, vedere il passaggio 3 della procedura precedente &quot;[Allega pixel di tracciamento di terze parti agli annunci in un posizionamento](#attach-pixels-ads)&quot;.

>[!MORELIKETHIS]
>
>* [Informazioni Sulla Gestione Degli Annunci](ad-about.md)
>* [Crea un annuncio singolo](ad-create.md)
>* [Creazione di più annunci di terze parti](ad-create-multiple.md)
>* [Modifica un annuncio](ad-edit.md)
>* [Elenca i posizionamenti associati a un annuncio](ad-list-placements.md)
>* [Modifica gli Schedules per i posizionamenti](/help/dsp/campaign-management/placements/placement-edit-ad-schedule.md)
>* [Domande frequenti sul video universale](/help/dsp/campaign-management/faq-universal-video.md)
