---
title: Creare un posizionamento
description: Scopri come creare un posizionamento.
feature: DSP Placements
exl-id: 28a328b1-0839-442e-a245-f586a7042f41
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '651'
ht-degree: 1%

---

# Creare un posizionamento

>[!TIP]
>
>Crea posizionamenti in base a obiettivi di campagna specifici o a esigenze di reporting.

1. Nel menu principale, fai clic su **[!UICONTROL Campaigns]**.

1. Fai clic sul nome della campagna in cui verrà incluso il posizionamento.

1. Sopra la tabella dati, fai clic su **[!UICONTROL Create]**. In [!UICONTROL Placement Types] nel menu fare clic sul tipo di posizionamento.

   Il tipo di posizionamento determina il tipo di annuncio che il posizionamento può includere.

1. Inserisci il [impostazioni di posizionamento](placement-settings.md):

   1. Specifica la [!UICONTROL Basics] impostazioni.

   1. In [!UICONTROL Goals] specifica la sezione [!UICONTROL Gross Budget] e, facoltativamente, specifica ulteriori obiettivi di posizionamento.

      Alcuni campi presentano valori predefiniti che è possibile ignorare.

      Se il pacchetto a cui è assegnato il posizionamento ha una velocità a livello di pacchetto, le impostazioni relative a obiettivi e velocità rifletteranno le impostazioni del pacchetto.

   1. (Facoltativo) In [!UICONTROL Geo-Targeting] restringere le posizioni incluse o escluse.

      Se non identifichi posizioni specifiche, tutte le posizioni sono oggetto di targeting.

      >[!NOTE]
      >
      >Le posizioni Città e DMA non sono disponibili per i posizionamenti Roku.

   1. In [!UICONTROL Inventory Targeting] restringere le origini di inventario da includere o escludere.

      Per la maggior parte dei tipi di posizionamento, tutti i tipi di inventario e tutte le origini per ciascun tipo sono inclusi per impostazione predefinita. Per [!DNL Roku] posizionamenti, è necessario specificare il tipo di inventario e le origini.

   1. (Facoltativo) In [!UICONTROL Site Targeting] restringere i siti di cui si desidera eseguire il targeting e specificare eventuali siti da escludere.

   1. (Facoltativo) In [!UICONTROL Audience Targeting] sezione:

      1. Restringi il pubblico. Ciò include la selezione dei segmenti di pubblico di cui eseguire il targeting all’interno del posizionamento.

         Per [!DNL Roku] posizionamenti, puoi sfruttare [Corrispondenza del pubblico univoco di DSP con [!DNL Roku]](/help/dsp/inventory/roku-inventory.md) includendo uno o più segmenti di pubblico a cui è possibile associare il [!DNL Roku] Set di dati deterministici (Opted-in).
   1. (Per campagne con targeting su più dispositivi a livello di persone; opzionale) Quando il posizionamento esegue il targeting di uno o più tipi di pubblico specifici, abilita il targeting per il posizionamento basato su persone su dispositivi diversi.

      Il targeting cross-device basato sulle persone è fornito da [!DNL LiveRamp] utilizzando solo dati statunitensi. Il servizio è disponibile per tutti gli inserzionisti a $ 0,35 CPM per le impression consegnate utilizzando il [!DNL LiveRamp] grafico dei dispositivi (ovvero, per dispositivi non trovati all’interno dei segmenti di pubblico target).

   1. (Facoltativo) In [!DNL Brand Safety and Media Targeting] , applica restrizioni di sicurezza del marchio per i posizionamenti.

   1. (Facoltativo) In [!DNL Tracking] , immetti pixel evento di terze parti o pixel di conversione per gli annunci nel posizionamento .

      >[!NOTE]
      >
      >([!DNL Roku] posizionamenti) Fornitori di pixel di terze parti approvati da [!DNL Roku] include [!DNL Acxiom], [!DNL comScore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk]e [!DNL Research Now].


1. Clic **[!UICONTROL Create Placement]**.

1. (Facoltativo) Allega annunci al posizionamento:

   1. Clic **[!UICONTROL Attach an ad]**.

   1. Effettua una delle seguenti operazioni:

      * Per creare un nuovo annuncio:

         1. Clic **[!UICONTROL Create a New Ad].**

         1. Specifica le impostazioni dell&#39;annuncio per [annunci audio](/help/dsp/campaign-management/ads/ad-settings-audio.md), [TV collegata](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md), [annunci display](/help/dsp/campaign-management/ads/ad-settings-display.md), [annunci mobile](/help/dsp/campaign-management/ads/ad-settings-mobile.md), [annunci nativi](/help/dsp/campaign-management/ads/ad-settings-native.md), [annunci pre-scorrimento](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)oppure [annunci video universali](/help/dsp/campaign-management/ads/ad-settings-universal-video.md).

         1. Clic **[!UICONTROL Save & Submit for Review]**.

         1. (Facoltativo) Per ogni annuncio aggiuntivo da creare per il posizionamento, fai clic su **[!UICONTROL Attach Another Ad]**, quindi ripetere i passaggi 1-3.

         1. Se non alleghi annunci esistenti, fai clic su **[!UICONTROL I'm done for now]**.
      * Per allegare annunci esistenti nella campagna:

         1. Clic **[!UICONTROL Select an Ad]**.

         1. Effettua una delle seguenti operazioni:

            * Per aggiungere un annuncio alla volta:

               1. Accanto al nome dell’annuncio, fai clic su **[!UICONTROL Select].**

               1. (Facoltativo) Per ogni annuncio aggiuntivo da allegare, fai clic su **[!UICONTROL Attach Another Ad]**, quindi ripetere il processo.
            * Per aggiungere fino a 20 annunci alla volta:

               1. Seleziona la casella di controllo sopra l’elenco degli annunci.

               1. Seleziona la casella di controllo accanto a ciascun annuncio da aggiungere.

               1. Clic **[!UICONTROL Attach]**.

               1. Accanto al nome dell’annuncio, fai clic su **[!UICONTROL Select]**.
         1. (Facoltativo) Per ignorare il periodo di volo predefinito e la rotazione degli annunci per annunci specifici nel posizionamento:

            1. Clic **[!UICONTROL Custom Schedule Ads]**.

            1. Effettua una delle seguenti operazioni:

               * Per aggiungere un volo, fai clic su **[!UICONTROL Add Flight]**, quindi specifica la data di inizio e la data di fine.

               * Per aggiungere un volo esistente a un annuncio, fai clic su **[!UICONTROL +]** nella riga dell’annuncio per la colonna flight.

               * Per rimuovere un volo esistente da un annuncio, fai clic su **[!UICONTROL x]** nella riga dell’annuncio per la colonna flight.

               * (Quando più annunci hanno lo stesso volo) Per ruotare gli annunci in modo non uniforme, fai clic su **[!UICONTROL Even Rotation]** nelle informazioni sul volo, quindi inserire il peso relativo in base al quale ruotare ogni annuncio, in percentuale.

                  Il peso totale deve essere uguale a 100.
            1. In alto a destra, fai clic su **[!UICONTROL Continue]**.

            1. Esamina i dettagli del volo, quindi fai clic su **[!UICONTROL Save & Finish]**.





>[!MORELIKETHIS]
>
>* [Informazioni sulla gestione del posizionamento](placement-about.md)
>* [Modificare un posizionamento](placement-edit.md)
>* [Modificare la pianificazione dell’annuncio per un posizionamento](placement-edit-ad-schedule.md)
>* [Mettere in pausa o attivare un posizionamento](placement-pause-activate.md)
>* [Visualizza il registro delle modifiche per un posizionamento](placement-change-log.md)
>* [Impostazioni di posizionamento](placement-settings.md)
>* [Scelte rapide da tastiera](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [Risoluzione dei problemi relativi alle prestazioni](/help/dsp/optimization/troubleshooting-performance.md)
>* [Video: Come creare un posizionamento di visualizzazione standard](https://video.tv.adobe.com/v/340454)

