---
title: Creare un posizionamento
description: Scopri come creare un posizionamento.
feature: DSP Placements
exl-id: 28a328b1-0839-442e-a245-f586a7042f41
source-git-commit: 0afe1d9985c1451c28943aaa17c7d6f8a73a95ef
workflow-type: tm+mt
source-wordcount: '703'
ht-degree: 0%

---

# Creare un posizionamento

>[!TIP]
>
>Crea posizionamenti in base a obiettivi specifici della campagna o a esigenze di reporting.

1. Nel menu principale, fare clic su **[!UICONTROL Campaigns]**.

1. Fai clic sul nome della campagna in cui includere il posizionamento.

1. Sopra la tabella dati, fare clic su **[!UICONTROL Create]**. Nella sezione [!UICONTROL Placement Types] del menu, fai clic sul tipo di posizionamento.

   Il tipo di posizionamento determina il tipo di annuncio che il posizionamento può includere.

1. Immetti le [impostazioni di posizionamento](placement-settings.md):

   1. Specificare le impostazioni [!UICONTROL Placement Basics].

   1. Nella sezione [!UICONTROL Goals], specifica [!UICONTROL Gross Budget] e, facoltativamente, specifica obiettivi di posizionamento aggiuntivi.

      Alcuni campi dispongono di valori predefiniti che è possibile ignorare.

      Se il pacchetto a cui è assegnato il posizionamento ha una velocità a livello di pacchetto, gli obiettivi e le impostazioni di velocità riflettono le impostazioni del pacchetto.

   1. (Facoltativo) Nella sezione [!UICONTROL Geo-Targeting], restringi le posizioni incluse o escluse.

      Se non identifichi posizioni specifiche, viene eseguito il targeting per tutte le posizioni.

      >[!NOTE]
      >
      >Le posizioni Città e DMA non sono disponibili per i posizionamenti Roku.

   1. Nella sezione [!UICONTROL Inventory Targeting], restringi le origini inventario da includere o escludere.

      Per la maggior parte dei tipi di posizionamento, tutti i tipi di inventario e tutte le origini per ciascun tipo sono inclusi per impostazione predefinita. Per [!DNL Roku] posizionamenti, è necessario specificare il tipo di inventario e le origini.

   1. (Facoltativo) Nella sezione [!UICONTROL Site Targeting], restringere i siti di destinazione e specificare i siti da escludere.

   1. Nella sezione [!UICONTROL Audience Targeting] (facoltativo):

      1. Restringi il pubblico. Ciò include la selezione dei segmenti di pubblico di destinazione all’interno del posizionamento.

         Per i posizionamenti [!DNL Roku], puoi sfruttare la corrispondenza del pubblico univoco di [DSP con [!DNL Roku]](/help/dsp/inventory/roku-inventory.md) includendo uno o più segmenti di pubblico che possono essere associati al set di dati deterministico [!DNL Roku] (consenso).

         I segmenti RampID di prime parti che non sono collegati a un posizionamento attivo, pianificato o in pausa vengono messi in pausa. Nell’elenco dei segmenti, il segmento viene indicato come &quot;In pausa automatica&quot;.

      1. (Per campagne con targeting multi-dispositivo a livello di persone; facoltativo) Quando il posizionamento esegue il targeting per uno o più tipi di pubblico specifici, abilita il targeting cross-device basato sulle persone per il posizionamento.

         Il targeting multi-dispositivo basato su persone viene fornito da [!DNL LiveRamp] utilizzando solo dati statunitensi. Il servizio è disponibile per tutti gli inserzionisti al prezzo di $0,35 CPM per le impression distribuite utilizzando il grafico dei dispositivi [!DNL LiveRamp] (ovvero, per i dispositivi non trovati nei segmenti di pubblico di destinazione).

   1. (Facoltativo) Nella sezione [!DNL Brand Safety and Media Targeting], applica le restrizioni di sicurezza del brand per i posizionamenti.

   1. (Facoltativo) Nella sezione [!DNL Tracking], immetti pixel evento di terze parti o pixel di conversione per gli annunci nel posizionamento.

      >[!NOTE]
      >
      >([!DNL Roku] posizionamenti) I fornitori di pixel di terze parti approvati da [!DNL Roku] includono [!DNL Acxiom], [!DNL Comscore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk] e [!DNL Research Now].

1. Fare clic su **[!UICONTROL Create Placement]**.

1. (Facoltativo) Allega annunci al posizionamento:

   1. Fare clic su **[!UICONTROL Attach an ad]**.

   1. Effettuare una delle seguenti operazioni:

      * Per creare un nuovo annuncio:

         1. Fare clic su **[!UICONTROL Create a New Ad].**

         1. Specifica le impostazioni degli annunci per [annunci audio](/help/dsp/campaign-management/ads/ad-settings-audio.md), [TV connessa](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md), [annunci di visualizzazione](/help/dsp/campaign-management/ads/ad-settings-display.md), [annunci per dispositivi mobili](/help/dsp/campaign-management/ads/ad-settings-mobile.md), [annunci nativi](/help/dsp/campaign-management/ads/ad-settings-native.md), [annunci pre-roll](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md) o [annunci video universali](/help/dsp/campaign-management/ads/ad-settings-universal-video.md).

        >[!NOTE]
        >
        >I posizionamenti di video universali possono contenere solo annunci video universali.

         1. Fare clic su **[!UICONTROL Save & Submit for Review]**.

         1. (Facoltativo) Per ogni annuncio aggiuntivo che desideri creare per il posizionamento, fai clic su **[!UICONTROL Attach Another Ad]**, quindi ripeti i passaggi da 1 a 3.

         1. Se non si desidera allegare annunci esistenti, fare clic su **[!UICONTROL I'm done for now]**.

      * Per allegare gli annunci esistenti nella campagna:

      1. Fare clic su **[!UICONTROL Select an Ad]**.

      1. Effettuare una delle seguenti operazioni:

         * Per aggiungere un annuncio alla volta:

            1. Accanto al nome dell&#39;annuncio, fare clic su **[!UICONTROL Select].**

            1. (Facoltativo) Per ogni annuncio aggiuntivo che si desidera allegare, fare clic su **[!UICONTROL Attach Another Ad]** e quindi ripetere la procedura.

         * Per aggiungere fino a 20 annunci alla volta:

            1. Seleziona la casella di controllo sopra l’elenco degli annunci.

            1. Seleziona la casella di controllo accanto a ogni annuncio da aggiungere.

            1. Fare clic su **[!UICONTROL Attach]**.

            1. Accanto al nome dell&#39;annuncio, fare clic su **[!UICONTROL Select]**.

      1. (Facoltativo) Per sostituire il periodo di volo predefinito e la rotazione degli annunci per annunci specifici nel posizionamento:

         1. Fare clic su **[!UICONTROL Custom Schedule Ads]**.

         1. Effettua una delle seguenti operazioni:

            * Per aggiungere un volo, fare clic su **[!UICONTROL Add Flight]** e quindi specificare la data di inizio e la data di fine.

            * Per aggiungere un volo esistente a un annuncio, fare clic su **[!UICONTROL +]** nella riga annuncio per la colonna volo.

            * Per rimuovere un volo esistente da un annuncio, fare clic su **[!UICONTROL x]** nella riga annuncio per la colonna volo.

            * (Quando più annunci hanno lo stesso volo) Per ruotare gli annunci in modo non uniforme, fare clic su **[!UICONTROL Even Rotation]** nelle informazioni sul volo, quindi immettere il peso relativo in base al quale ruotare ogni annuncio, come percentuale.

              Il peso totale deve essere uguale a 100.

         1. In alto a destra, fare clic su **[!UICONTROL Continue]**.

         1. Rivedere i dettagli del volo, quindi fare clic su **[!UICONTROL Save & Finish]**.

>[!MORELIKETHIS]
>
>* [Informazioni sulla gestione del posizionamento](placement-about.md)
>* [Modifica posizionamenti](placement-edit.md)
>* [Gestire i moltiplicatori delle offerte per i posizionamenti](placement-manage-bid-multipliers.md)
>* [Modifica gli Schedules per i posizionamenti](placement-edit-ad-schedule.md)
>* [Sospendi o attiva un posizionamento](placement-pause-activate.md)
>* [Visualizza il log delle modifiche per un posizionamento](placement-change-log.md)
>* [Impostazioni posizionamento](placement-settings.md)
>* [Visualizza il rapporto Previsione posizionamento](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [Domande frequenti sul video universale](/help/dsp/campaign-management/faq-universal-video.md)
>* [Scelte rapide da tastiera](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [Risoluzione dei problemi relativi alle prestazioni](/help/dsp/optimization/troubleshooting-performance.md)
>* [Video: come creare un posizionamento display standard](https://video.tv.adobe.com/v/345000?captions=ita)
