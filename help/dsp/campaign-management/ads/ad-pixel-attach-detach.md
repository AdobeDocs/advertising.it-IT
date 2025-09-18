---
title: Allega e rimuovi pixel dagli annunci
description: Scopri come allegare e rimuovere i pixel di tracciamento di terze parti dagli annunci.
feature: DSP Ads
source-git-commit: a3bd04da6c6f428fdb6e1f05187ea3de0174c9d7
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 0%

---

# Allega e rimuovi pixel dagli annunci

Puoi collegare e scollegare dagli annunci i pixel di tracciamento di terze parti.

## Apri la visualizzazione [!UICONTROL Ad Tools] {#ad-tools-open}

1. Nel menu principale, fare clic su **[!UICONTROL Campaigns]**.

1. Fai clic sul nome della campagna.

1. Aprire la visualizzazione [!UICONTROL Ad Tools] in uno dei modi seguenti:

   * Nella visualizzazione [!UICONTROL Campaigns] accanto al nome della campagna, fare clic su **[!UICONTROL ...]** > **[!UICONTROL Ad Tools].**

   * (Dalla visualizzazione [!UICONTROL Packages] , [!UICONTROL Placements] o [!UICONTROL Ads]) In alto a destra, fare clic su **[!UICONTROL ...]** > **[!UICONTROL Ad Tools]**.

## Allegare pixel di tracciamento di terze parti agli annunci in un posizionamento {#attach-pixels-ads}

1. [Aprire la visualizzazione [!UICONTROL Ad Tools]](#ad-tools-open).

   Verrà aperta la scheda **[!UICONTROL Attach Pixels]**.

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

   Verrà aperta la scheda **[!UICONTROL Attach Pixels]**.

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

   Verrà aperta la scheda **[!UICONTROL Attach Pixels]**.

1. Passa all&#39;opzione **[!UICONTROL View]** in alto a destra.

1. (Facoltativo) Individua annunci e pixel di terze parti in base alle esigenze:

   * Sopra la tabella sinistra, fare clic su ![Filtro](/help/dsp/assets/filter.png) e filtrare gli elenchi in base allo stato dell&#39;annuncio, al tipo di annuncio, all&#39;evento di integrazione dei pixel o al tipo di pixel.

   * Sopra le tabelle di destra e di sinistra, cerca stringhe di testo specifiche nei nomi degli annunci e nei nomi dei pixel.

1. Fai clic su una riga di annunci nella tabella a sinistra per visualizzare i pixel associati nella tabella a destra.

1. (Facoltativo) Per allegare altri pixel agli annunci, passa alla visualizzazione **[!UICONTROL Edit]** in alto a destra. Per istruzioni, vedere il passaggio 3 della procedura precedente &quot;[Allega pixel di tracciamento di terze parti agli annunci in un posizionamento](#attach-pixels-ads)&quot;.

>[!MORELIKETHIS]
>
>* [Informazioni Sulla Gestione Degli Annunci](ad-about.md)
>* [Allega annunci ai posizionamenti](/help/dsp/campaign-management/ads/ad-attach-to-placement.md)
>* [Crea un annuncio singolo](ad-create.md)
>* [Creazione di più annunci di terze parti](ad-create-multiple.md)
>* [Modifica un annuncio](ad-edit.md)
>* [Elenca i posizionamenti associati a un annuncio](ad-list-placements.md)
>* [Modifica gli Schedules per i posizionamenti](/help/dsp/campaign-management/placements/placement-edit-ad-schedule.md)
>* [Domande frequenti sul video universale](/help/dsp/campaign-management/faq-universal-video.md)

