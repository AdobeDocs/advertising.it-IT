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

Utilizza il [!UICONTROL Ad Tools] visualizzazione per allegare annunci ai posizionamenti, allegare pixel di tracciamento di terze parti agli annunci e scollegare dagli annunci i pixel di tracciamento di terze parti esistenti.

>[!NOTE]
>
>Gli annunci video universali possono essere collegati solo ai posizionamenti video universali.

## Apri [!UICONTROL Ad Tools] Visualizza {#ad-tools-open}

1. Nel menu principale, fai clic su **[!UICONTROL Campaigns]**.

1. Fai clic sul nome della campagna.

1. Apri [!UICONTROL Ad Tools] visualizzare in uno dei modi seguenti:

   * (Da [!UICONTROL Packages] , [!UICONTROL Placements], o [!UICONTROL Ads] in alto a destra, fai clic su **[!UICONTROL ...]** > **[!UICONTROL Ad Tools]**.

   * (Da [!UICONTROL Placements] (vista) Accanto al nome del posizionamento, fate clic su **[!UICONTROL ...]** > **[!UICONTROL Attach Ads].**

   * (Da [!UICONTROL Ads] ) Accanto al nome dell’annuncio, fai clic su  **[!UICONTROL ...]** > **[!UICONTROL Add to Placements]**.

   Il [!UICONTROL Attach Ads] è selezionata per impostazione predefinita.

## Allega annunci ai posizionamenti {#attach-ads-campaign}

1. [Apri [!UICONTROL Ad Tools] visualizza](#ad-tools-open).

1. In [!UICONTROL Edit] visualizzazione secondaria, eseguire le operazioni seguenti per ogni gruppo di annunci che si desidera allegare ai posizionamenti:

   1. (Facoltativo) Individua posizionamenti e annunci specifici in uno dei seguenti modi:

      * Sopra la tabella a sinistra, fai clic su ![Filtro](/help/dsp/assets/filter.png) e filtrare gli elenchi per pacchetto, tipo di posizionamento, stato posizionamento, tipo di annuncio o stato annuncio.

      * Sopra le tabelle di destra e di sinistra, cerca stringhe di testo specifiche nel posizionamento e nei nomi degli annunci.

   1. Nella tabella a sinistra, seleziona la casella di controllo accanto a ciascun posizionamento a cui allegare gli annunci.

   1. Nella tabella a destra, seleziona la casella di controllo accanto a ogni annuncio che desideri allegare ai posizionamenti selezionati.

      Sono selezionabili solo gli annunci applicabili per il tipo di posizionamento e che non sono già allegati ai posizionamenti selezionati.

   1. In basso a destra, fai clic su **[!UICONTROL Attach]**.

1. (Facoltativo) Per tornare alle visualizzazioni dei dettagli della campagna, fai clic su ![Torna alla cartella](/help/dsp/assets/breadcrumb-return.png "Torna alla cartella") a sinistra di [!UICONTROL Ad Tools] e seleziona il nome della campagna.

## Visualizza annunci allegati ai posizionamenti {#view-ads-campaign}

<!-- should be a separate page, combined with "List the Placements Associated with an Ad" (although that pertains to a single ad only), or maybe just rename this topic -->

1. [Apri [!UICONTROL Ad Tools] visualizza](#ad-tools-open).

1. Passa a **[!UICONTROL View]** in alto a destra.

1. (Facoltativo) Individua posizionamenti e annunci specifici in base alle esigenze:

   * Sopra la tabella a sinistra, fai clic su ![Filtro](/help/dsp/assets/filter.png) e filtrare gli elenchi per pacchetto, tipo di posizionamento, stato posizionamento, tipo di annuncio o stato annuncio.

   * Nelle tabelle di destra e di sinistra, cerca stringhe di testo specifiche nel posizionamento o nel nome dell’annuncio.

1. Fai clic su una riga di posizionamento nella tabella a sinistra per visualizzare gli annunci allegati nella tabella a destra.

1. (Facoltativo) Per allegare più annunci ai posizionamenti della campagna, passa alla **[!UICONTROL Edit]** in alto a destra. Si veda il punto 2 della procedura precedente, &quot;[Allega annunci ai posizionamenti](#attach-ads-campaign),&quot; per le istruzioni.

## Allegare pixel di tracciamento di terze parti agli annunci in un posizionamento {#attach-pixels-ads}

1. [Apri [!UICONTROL Ad Tools] visualizza](#ad-tools-open).

1. Fai clic su **[!UICONTROL Attach Pixels]** scheda.

1. In [!UICONTROL Edit] visualizzazione secondaria:

   1. (Facoltativo) Individua annunci e pixel di terze parti in uno dei seguenti modi:

      * Sopra la tabella a sinistra, fai clic su ![Filtro](/help/dsp/assets/filter.png) e filtra gli elenchi in base allo stato dell’annuncio, al tipo di annuncio, all’evento di integrazione pixel o al tipo di pixel.

      * Sopra le tabelle di destra e di sinistra, cerca stringhe di testo specifiche nei nomi degli annunci e nei nomi dei pixel.

   1. (Se per la campagna non esistono pixel di tracciamento di terze parti) Crea un pixel:

      1. Nella tabella a destra, fai clic su **[!UICONTROL Create pixel]**.

      1. Specificare le impostazioni:

         **[!UICONTROL Integration Event]:** L’evento che attiva il pixel da attivare, ad esempio *[!UICONTROL Impression]* o *[!UICONTROL Click-through]*.

         **[!UICONTROL Pixel Type]:** Se il pixel è un *[!UICONTROL IMG URL]* (file di immagine 1x1 pixel), *[!UICONTROL HTML]*, o *[!UICONTROL JavaScript URL]*.

         **[!UICONTROL Pixel URL or Code]:** URL dell&#39;immagine pixel nel formato appropriato per il tipo di pixel specificato.

         **[!UICONTROL Pixel Name]:** Il nome del pixel. Utilizza un nome che ti consenta di identificare facilmente il pixel.

         **[!UICONTROL Pixel Provider]:** Il provider pixel: *[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]*, o *[!UICONTROL IAS]*.

      1. Clic **[!UICONTROL Save]**.

   1. Nella tabella a sinistra, seleziona la casella di controllo accanto a ogni annuncio per il quale desideri allegare pixel di tracciamento di terze parti.

   1. Nella tabella a destra, seleziona la casella di controllo accanto a ciascun pixel di tracciamento di terze parti che desideri allegare agli annunci selezionati.

      È possibile selezionare solo i pixel che non sono già allegati agli annunci selezionati.

   1. In basso a destra, fai clic su **[!UICONTROL Attach]**.

1. (Facoltativo) Per tornare alle visualizzazioni dei dettagli della campagna, fai clic su ![Torna alla cartella](/help/dsp/assets/breadcrumb-return.png "Torna alla cartella") a sinistra di [!UICONTROL Ad Tools] e seleziona il nome della campagna.

## Staccare i pixel di tracciamento di terze parti dagli annunci in un posizionamento {#detach-pixels-ads}

1. [Apri [!UICONTROL Ad Tools] visualizza](#ad-tools-open).

1. Fai clic su **[!UICONTROL Attach Pixels]** scheda.

1. In [!UICONTROL Edit] visualizzazione secondaria:

   1. (Facoltativo) Individua annunci e pixel di terze parti in uno dei seguenti modi:

      * Sopra la tabella a sinistra, fai clic su ![Filtro](/help/dsp/assets/filter.png) e filtra gli elenchi in base allo stato dell’annuncio, al tipo di annuncio, all’evento di integrazione pixel o al tipo di pixel.

      * Sopra le tabelle di destra e di sinistra, cerca stringhe di testo specifiche nei nomi degli annunci e nei nomi dei pixel.

   1. Nella tabella a sinistra, seleziona la casella di controllo accanto a ogni annuncio da cui desideri scollegare i pixel di tracciamento di terze parti.

   1. Nella tabella a destra, seleziona la casella di controllo accanto a ciascun pixel di tracciamento di terze parti che desideri staccare dagli annunci selezionati.

      Sono selezionabili solo i pixel allegati a tutti gli annunci selezionati.

   1. In basso a destra, fai clic su **[!UICONTROL Detach]**.

1. (Facoltativo) Per tornare alle visualizzazioni dei dettagli della campagna, fai clic su ![Torna alla cartella](/help/dsp/assets/breadcrumb-return.png "Torna alla cartella") a sinistra di [!UICONTROL Ad Tools] e seleziona il nome della campagna.

## Pixel di visualizzazione allegati agli annunci {#view-pixels-ads}

1. [Apri [!UICONTROL Ad Tools] visualizza](#ad-tools-open).

1. Fai clic su **[!UICONTROL Attach Pixels]** scheda.

1. Passa a **[!UICONTROL View]** in alto a destra.

1. (Facoltativo) Individua annunci e pixel di terze parti in base alle esigenze:

   * Sopra la tabella a sinistra, fai clic su ![Filtro](/help/dsp/assets/filter.png) e filtra gli elenchi in base allo stato dell’annuncio, al tipo di annuncio, all’evento di integrazione pixel o al tipo di pixel.

   * Sopra le tabelle di destra e di sinistra, cerca stringhe di testo specifiche nei nomi degli annunci e nei nomi dei pixel.

1. Fai clic su una riga di annunci nella tabella a sinistra per visualizzare i pixel associati nella tabella a destra.

1. Per allegare più pixel agli annunci, passa alla **[!UICONTROL Edit]** in alto a destra. Si veda il Passaggio 3 della procedura precedente, &quot;[Allegare pixel di tracciamento di terze parti agli annunci in un posizionamento](#attach-pixels-ads),&quot; per le istruzioni.

>[!MORELIKETHIS]
>
>* [Informazioni sulla gestione degli annunci](ad-about.md)
>* [Creare un singolo annuncio](ad-create.md)
>* [Creare più annunci di terze parti](ad-create-multiple.md)
>* [Modificare un annuncio](ad-edit.md)
>* [Elencare i posizionamenti associati a un annuncio](ad-list-placements.md)
>* [Modificare gli Schedules degli annunci per i posizionamenti](/help/dsp/campaign-management/placements/placement-edit-ad-schedule.md)
>* [Domande frequenti sui video universali](/help/dsp/campaign-management/faq-universal-video.md)
