---
title: Gestire le origini del pubblico per attivare i tipi di pubblico con ID universale
description: Scopri come creare e gestire un’origine per importare i tipi di pubblico dalla piattaforma di dati dei clienti e convertirli in segmenti contenenti ID universali.
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
source-git-commit: 3a641db6b145e67e6e1f1daca271dd524973e075
workflow-type: tm+mt
source-wordcount: '759'
ht-degree: 0%

---

# Gestire le origini del pubblico per attivare i tipi di pubblico con ID universale

*funzionalità Beta*

Crea un’origine in DSP per ogni pubblico di prime parti nella piattaforma di dati cliente che desideri convertire in segmenti contenenti tipi di ID universali specificati. Puoi importare i segmenti nell’account DSP della tua organizzazione o in un account inserzionista. Gli addebiti per i dati vengono applicati in base ai tipi di ID universali selezionati. Dopo aver creato una sorgente, sono necessari passaggi aggiuntivi per acquisire i tipi di pubblico da ogni piattaforma di dati cliente. Vedere la nota alla fine della procedura per creare un&#39;origine.

In seguito, puoi modificare i tipi di ID universali in cui viene tradotto il pubblico di origine e visualizzare un registro delle modifiche.

È inoltre possibile eliminare un&#39;origine.

## Creazione di un Audience Source

<!-- Not sure about this

You can create one source for each combination of universal ID partner and data visibility level.

-->

1. Nel menu principale, fare clic su **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Fare clic su **[!UICONTROL Add Source]**.

1. Nel menu [!UICONTROL Select a Type], seleziona la [piattaforma dati cliente](source-about.md):

   * *[!UICONTROL RT-CDP]*: [!DNL Adobe Real-Time CDP].

   * *[!UICONTROL ActionIQ]*: piattaforma dati cliente [!DNL ActionIQ].

   * *[!UICONTROL Amperity]*: piattaforma dati cliente [!DNL Amperity].

   * *[!UICONTROL Optimizely]*: piattaforma dati cliente [!DNL Optimizely].

   * *[!UICONTROL Tealium CDP]*: (solo utenti configurati) la piattaforma dati del cliente [!DNL Tealium].

1. Specificare [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* o *[!UICONTROL Account]*.

1. Immettere le [impostazioni di origine rimanenti](#source-settings).

   Mantieni una copia di [!UICONTROL Source Key] generata. Il valore ti servirà più tardi.

1. Fare clic su **[!UICONTROL Save]**.

>[!NOTE]
>
>Dopo aver creato un’origine per la piattaforma di dati cliente, dovrai completare ulteriori passaggi per importare il pubblico. Visualizza il [flusso di lavoro per [!DNL Adobe] [!DNL Real-time CDP]](source-adobe-rtcdp.md),<!-- the [workflow for [!DNL ActionIQ]](source-actioniq.md), --> il [flusso di lavoro per [!DNL Amperity]](source-amperity.md), il [flusso di lavoro per [!DNL Optimizely]](source-optimizely.md) e il [flusso di lavoro per [!DNL Tealium]](source-tealium.md).

## Modificare i tipi di ID per Audience Source

<!-- Clarify this:
All changes to universal IDs translated from the source are applied after you save the the source record. For example, if a new ID is added, any hashed email addresses shared before making the changes aren't converted. Similarly, if an ID is removed, we don't delete any historical data from the segments shared through the source.

OR 

All changes to universal IDs translated from the source are applied after you save the the source record. For example, if you add a new ID type, then we convert hashed email addresses shared before making the changes to the new ID type. Similarly, if you remove an ID type, then we delete any historical IDs of that type from the segments shared through the source.

-->

1. Nel menu principale, fare clic su **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Posizionare il cursore sulla riga di origine e fare clic su **[!UICONTROL Edit]**.

1. Cambia [ID selezionati per l&#39;origine](#source-settings).

1. Fare clic su **[!UICONTROL Save]**.

## Eliminare un Audience Source

L&#39;eliminazione di un&#39;origine rimuove i segmenti tradotti attraverso l&#39;origine.<!-- Will performance data for the segment still be available in any types of reports?  If yes, which? -->

1. Nel menu principale, fare clic su **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Posizionare il cursore sulla riga di origine e fare clic su **[!UICONTROL Delete]**.

1. Nel messaggio di conferma, fare clic su **[!UICONTROL Delete]**.

## Visualizzare il registro delle modifiche per un Audience Source

Puoi visualizzare i dettagli sulle modifiche apportate a un record di origine del pubblico e, facoltativamente, allegare note al registro.

1. Nel menu principale, fare clic su **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Posizionare il cursore sulla riga di origine e fare clic su **[!UICONTROL Change log]**.

1. (Facoltativo) Per allegare una nota al log delle modifiche:

   1. Posizionare il cursore sulla riga di origine e fare clic su **[!UICONTROL Add Notes]**.

   1. Immettere la nota, quindi fare clic su **[!UICONTROL Save]**.

      La lunghezza massima è di 256 caratteri.

1. (Facoltativo) Per aprire il registro in una schermata di dettaglio più grande, posizionare il cursore sulla riga di origine e fare clic su **[!UICONTROL View Details]**.

## Impostazioni Audience Source {#source-settings}

**[!UICONTROL Data Visibility Level]:** se i segmenti sono disponibili per un singolo inserzionista con accesso all&#39;account (*[!UICONTROL Advertiser]*) o per tutti gli inserzionisti con accesso all&#39;account *[!UICONTROL Account]*.

**[!UICONTROL Advertiser]:** (solo visibilità a livello di inserzionista) L&#39;inserzionista per il quale sono disponibili i segmenti. Selezionane uno dall’elenco degli inserzionisti con accesso all’account.

**[!UICONTROL Enter IMS Org Id]:** ([!DNL Real-Time CDP] solo origini) ID organizzazione Adobe Experience Cloud per l&#39;account [!DNL Adobe Experience Platform].

**[!UICONTROL Convert PII to the following IDs]:** i tipi di ID in cui verranno convertite le informazioni personali (PII, personally identifiable information). Se selezioni più tipi, il segmento generato viene compilato con valori per ciascun tipo di ID selezionato (ad esempio [!DNL RampID] e [!DNL Unified ID2.0] per ciascun indirizzo e-mail). Gli oneri per i dati sono applicati di conseguenza.

Per [!DNL RampID] e [!DNL Unified ID2.0], il fornitore cerca ogni indirizzo e-mail per vedere se esiste già un ID e converte l&#39;indirizzo in un ID corrispondente quando disponibile. Se per l&#39;indirizzo non esiste alcun ID, viene creato un nuovo ID.

>[!NOTE]
>
>Puoi eseguire il targeting per un solo tipo di ID in un singolo posizionamento. Per verificare le prestazioni in base al tipo di ID, [crea un posizionamento separato](/help/dsp/campaign-management/placements/placement-create.md) per ogni tipo di ID nel segmento.

* *[!DNL RampID]:* Per convertire PII in [!DNL RampID]. È possibile utilizzare [!DNL RampIDs] per il retargeting degli utenti che accedono e per la misurazione di [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md).

* *[!DNL Unified ID2.0](Beta):* Per convertire PII in un ID [Unified ID 2.0](https://unifiedid.com) per il retargeting degli utenti che accedono.

<!-- Later
* *[!DNL ID5] (Beta):* To convert PII to an [!DNL ID5] ID. You can use [!DNL ID5] IDs for retargeting logging-in users and for [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) measurement.

-->

**[!UICONTROL Terms of Service]:** I termini del contratto di servizio per la conversione di PII in ID universali. Prima di poter convertire i dati in un nuovo tipo di ID, tu o un altro utente dell’account DSP dovete accettare i termini una volta. Per i clienti con contratti di assistenza gestiti, il team dell’account Adobe riceverà il consenso e accetterà le condizioni per conto della tua organizzazione. Per leggere i termini, fare clic su **>**. Per accettare i termini, scorrere fino alla fine dei termini e fare clic su **[!UICONTROL Accept]**.

**[!UICONTROL Source Key]:** (sola lettura; generata automaticamente) La chiave di origine che puoi utilizzare per creare una connessione di destinazione nella piattaforma dati del cliente per inviare pubblici ad Advertising DSP. Puoi copiare il valore negli Appunti per incollarlo nelle impostazioni di connessione di destinazione o in un file.

>[!MORELIKETHIS]
>
>* [Informazioni sulle origini del pubblico di prime parti](source-about.md)
>* [Supporto per l&#39;attivazione di ID universali](/help/dsp/audiences/universal-ids.md)
>* [Converti ID utente da [!DNL Adobe Real-Time CDP] a ID universali](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Converti ID utente da [!DNL Amperity] a ID universali](/help/dsp/audiences/sources/source-amperity.md)
>* [Converti ID utente da [!DNL Optimizely] a ID universali](/help/dsp/audiences/sources/source-optimizely.md)
>* [Converti ID utente da [!DNL Tealium] a ID universali](/help/dsp/audiences/sources/source-tealium.md)
>* [Informazioni su Gestione dell&#39;audience](/help/dsp/audiences/audience-about.md)
