---
title: Creare un posizionamento
description: Scopri come creare un posizionamento.
feature: DSP Placements
exl-id: 28a328b1-0839-442e-a245-f586a7042f41
source-git-commit: 9b3d6893e004b16714bf50f1334424d50fac7c91
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 0%

---

# Creare un posizionamento

>[!TIP]
>
>Crea posizionamenti in base a obiettivi specifici della campagna o a esigenze di reporting.

1. Nel menu principale, fai clic su **[!UICONTROL Campaigns]**.

1. Fai clic sul nome della campagna in cui includere il posizionamento.

1. Sopra la tabella dati, fai clic su **[!UICONTROL Create]**. In [!UICONTROL Placement Types] del menu, fate clic sul tipo di posizionamento.

   Il tipo di posizionamento determina il tipo di annuncio che il posizionamento può includere.

1. Inserisci il [impostazioni di posizionamento](placement-settings.md):

   1. Specifica la [!UICONTROL Placement Basics] impostazioni.

   1. In [!UICONTROL Goals] , specificare [!UICONTROL Gross Budget] e, facoltativamente, specifica obiettivi di posizionamento aggiuntivi.

      Alcuni campi dispongono di valori predefiniti che è possibile ignorare.

      Se il pacchetto a cui è assegnato il posizionamento ha una velocità a livello di pacchetto, gli obiettivi e le impostazioni di velocità riflettono le impostazioni del pacchetto.

   1. (Facoltativo) In [!UICONTROL Geo-Targeting] , restringere le posizioni incluse o escluse.

      Se non identifichi posizioni specifiche, viene eseguito il targeting per tutte le posizioni.

      >[!NOTE]
      >
      >Le posizioni Città e DMA non sono disponibili per i posizionamenti Roku.

   1. In [!UICONTROL Inventory Targeting] limitare le origini di magazzino da includere o escludere.

      Per la maggior parte dei tipi di posizionamento, tutti i tipi di inventario e tutte le origini per ciascun tipo sono inclusi per impostazione predefinita. Per [!DNL Roku] posizionamenti, è necessario specificare il tipo di inventario e le origini.

   1. (Facoltativo) In [!UICONTROL Site Targeting] , limitare i siti di destinazione e specificare i siti da escludere.

   1. (Facoltativo) In [!UICONTROL Audience Targeting] sezione:

      1. Restringi il pubblico. Ciò include la selezione dei segmenti di pubblico di destinazione all’interno del posizionamento.

         Per [!DNL Roku] posizionamenti, puoi sfruttare [Corrispondenza del pubblico univoco dell’DSP con [!DNL Roku]](/help/dsp/inventory/roku-inventory.md) includendo uno o più segmenti di pubblico che possono essere confrontati con [!DNL Roku] (opt-in) set di dati deterministici.

      1. (Per campagne con targeting multi-dispositivo a livello di persone; facoltativo) Quando il posizionamento esegue il targeting per uno o più tipi di pubblico specifici, abilita il targeting cross-device basato sulle persone per il posizionamento.

         Il targeting cross-device basato su persone è fornito da [!DNL LiveRamp] utilizzando solo dati statunitensi. Il servizio è disponibile per tutti gli inserzionisti a $ 0,35 CPM per le impression distribuite utilizzando [!DNL LiveRamp] device graph (ossia, per dispositivi non trovati all’interno dei segmenti di pubblico target).

   1. (Facoltativo) In [!DNL Brand Safety and Media Targeting] , applica le restrizioni di sicurezza del marchio per i posizionamenti.

   1. (Facoltativo) In [!DNL Tracking] , inserisci i pixel dell’evento di terze parti o i pixel di conversione per gli annunci nel posizionamento.

      >[!NOTE]
      >
      >([!DNL Roku] posizionamenti) fornitori di pixel di terze parti approvati da [!DNL Roku] include [!DNL Acxiom], [!DNL Comscore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk], e [!DNL Research Now].

1. Clic **[!UICONTROL Create Placement]**.

1. (Facoltativo) Allega annunci al posizionamento:

   1. Clic **[!UICONTROL Attach an ad]**.

   1. Effettuare una delle seguenti operazioni:

      * Per creare un nuovo annuncio:

         1. Clic **[!UICONTROL Create a New Ad].**

         1. Specifica le impostazioni annuncio per [annunci audio](/help/dsp/campaign-management/ads/ad-settings-audio.md), [TV collegata](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md), [annunci display](/help/dsp/campaign-management/ads/ad-settings-display.md), [annunci per dispositivi mobili](/help/dsp/campaign-management/ads/ad-settings-mobile.md), [annunci nativi](/help/dsp/campaign-management/ads/ad-settings-native.md), [annunci pre-roll](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md), o [annunci video universali](/help/dsp/campaign-management/ads/ad-settings-universal-video.md).

        >[!NOTE]
        >
        >I posizionamenti di video universali possono contenere solo annunci video universali.

         1. Clic **[!UICONTROL Save & Submit for Review]**.

         1. (Facoltativo) Per ogni annuncio aggiuntivo che desideri creare per il posizionamento, fai clic su **[!UICONTROL Attach Another Ad]**, quindi ripetere i passaggi 1-3.

         1. Se non intendi allegare annunci esistenti, fai clic su **[!UICONTROL I'm done for now]**.

      * Per allegare gli annunci esistenti nella campagna:

      1. Clic **[!UICONTROL Select an Ad]**.

      1. Effettuare una delle seguenti operazioni:

         * Per aggiungere un annuncio alla volta:

            1. Accanto al nome dell’annuncio, fai clic su **[!UICONTROL Select].**

            1. (Facoltativo) Per ogni annuncio aggiuntivo che desideri allegare, fai clic su **[!UICONTROL Attach Another Ad]** e quindi ripetere il processo.

         * Per aggiungere fino a 20 annunci alla volta:

            1. Seleziona la casella di controllo sopra l’elenco degli annunci.

            1. Seleziona la casella di controllo accanto a ogni annuncio da aggiungere.

            1. Clic **[!UICONTROL Attach]**.

            1. Accanto al nome dell’annuncio, fai clic su **[!UICONTROL Select]**.

      1. (Facoltativo) Per sostituire il periodo di volo predefinito e la rotazione degli annunci per annunci specifici nel posizionamento:

         1. Clic **[!UICONTROL Custom Schedule Ads]**.

         1. Effettua una delle seguenti operazioni:

            * Per aggiungere un volo, fai clic su **[!UICONTROL Add Flight]** e quindi specificare la data di inizio e la data di fine.

            * Per aggiungere un volo esistente a un annuncio, fai clic su **[!UICONTROL +]** nella riga annuncio per la colonna volo.

            * Per rimuovere un volo esistente da un annuncio, fai clic su **[!UICONTROL x]** nella riga annuncio per la colonna volo.

            * (Quando più annunci hanno lo stesso volo) Per ruotare gli annunci in modo non uniforme, fai clic su **[!UICONTROL Even Rotation]** nelle informazioni sul volo, quindi immettere il peso relativo in base al quale ruotare ogni annuncio, come percentuale.

              Il peso totale deve essere uguale a 100.

         1. In alto a destra, fai clic su **[!UICONTROL Continue]**.

         1. Rivedi i dettagli del volo, quindi fai clic su **[!UICONTROL Save & Finish]**.

>[!MORELIKETHIS]
>
>* [Informazioni sulla gestione del posizionamento](placement-about.md)
>* [Modifica posizionamenti](placement-edit.md)
>* [Gestire i moltiplicatori delle offerte per i posizionamenti](placement-manage-bid-multipliers.md)
>* [Modificare gli Schedules degli annunci per i posizionamenti](placement-edit-ad-schedule.md)
>* [Sospendere o attivare un posizionamento](placement-pause-activate.md)
>* [Visualizzare il log delle modifiche per un posizionamento](placement-change-log.md)
>* [Impostazioni di posizionamento](placement-settings.md)
>* [Visualizza il rapporto Previsione posizionamento](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [Domande frequenti sui video universali](/help/dsp/campaign-management/faq-universal-video.md)
>* [Scelte rapide da tastiera](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [Risoluzione dei problemi relativi alle prestazioni](/help/dsp/optimization/troubleshooting-performance.md)
>* [Video: come creare un posizionamento display standard](https://video.tv.adobe.com/v/340454)
