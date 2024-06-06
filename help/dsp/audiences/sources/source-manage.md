---
title: Gestire le origini del pubblico per attivare i tipi di pubblico con ID universale
description: Scopri come creare e gestire un’origine per importare i tipi di pubblico dalla piattaforma di dati dei clienti e convertirli in segmenti contenenti ID universali.
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
source-git-commit: 9411089703ce0b9502c1c2522cce999c3a5fafbf
workflow-type: tm+mt
source-wordcount: '724'
ht-degree: 0%

---

# Gestire le origini del pubblico per attivare i tipi di pubblico con ID universale

*Funzione beta*

Crea un’origine in DSP per ogni pubblico di prime parti nella piattaforma di dati cliente che desideri convertire in segmenti contenenti tipi di ID universali specificati. Puoi importare i segmenti nell’account DSP della tua organizzazione o in un account inserzionista. Gli addebiti per i dati vengono applicati in base ai tipi di ID universali selezionati. Dopo aver creato una sorgente, sono necessari passaggi aggiuntivi per acquisire i tipi di pubblico da ogni piattaforma di dati cliente. Vedere la nota alla fine della procedura per creare un&#39;origine.

In seguito, puoi modificare i tipi di ID universali in cui viene tradotto il pubblico di origine e visualizzare un registro delle modifiche.

È inoltre possibile eliminare un&#39;origine.

## Creare un’origine di pubblico

<!-- Not sure about this

You can create one source for each combination of universal ID partner and data visibility level.

-->

1. Nel menu principale, fai clic su **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Clic **[!UICONTROL Add Source]**.

1. In [!UICONTROL Select a Type] selezionare la piattaforma dati del cliente:

   * *[!UICONTROL RT-CDP]*: [Il [!DNL Adobe Real-Time Customer Data Platform]](source-about.md).

   * *[!UICONTROL ActionIQ]*: Il [[!DNL ActionIQ] piattaforma dati cliente](source-about.md).

   * *[!UICONTROL Tealium CDP]*: (solo utenti configurati) Il [[!DNL Tealium] piattaforma dati cliente](source-about.md).

1. Specifica la [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* o *[!UICONTROL Account]*.

1. Inserisci il valore rimanente [impostazioni di origine](#source-settings).

   Mantieni una copia di [!UICONTROL Source Key] che viene generato. Il valore ti servirà più tardi.

1. Clic **[!UICONTROL Save]**.

>[!NOTE]
>
>Dopo aver creato un’origine per la piattaforma di dati cliente, dovrai completare ulteriori passaggi. Consulta la [flusso di lavoro per importare tipi di pubblico da [!DNL Adobe] [!DNL Real-time CDP]](source-adobe-rtcdp.md)<!-- the [activation workflow for [!DNL ActionIQ]](source-actioniq.md), --> e [flusso di lavoro per importare tipi di pubblico da [!DNL Tealium]](source-tealium.md).

## Modificare i tipi di ID per un’origine pubblico

<!-- Clarify this:
All changes to universal IDs translated from the source are applied after you save the the source record. For example, if a new ID is added, any hashed email addresses shared before making the changes aren't converted. Similarly, if an ID is removed, we don't delete any historical data from the segments shared through the source.

OR 

All changes to universal IDs translated from the source are applied after you save the the source record. For example, if you add a new ID type, then we convert hashed email addresses shared before making the changes to the new ID type. Similarly, if you remove an ID type, then we delete any historical IDs of that type from the segments shared through the source.

-->

1. Nel menu principale, fai clic su **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Tenere premuto il cursore sulla riga di origine e fare clic su **[!UICONTROL Edit]**.

1. Modificare il [ID selezionati per l’origine](#source-settings).

1. Clic **[!UICONTROL Save]**.

## Eliminare un’origine di pubblico

L’eliminazione di un’origine rimuove i segmenti tradotti attraverso l’origine.<!-- Will performance data for the segment still be available in any types of reports?  If yes, which? -->

1. Nel menu principale, fai clic su **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Tenere premuto il cursore sulla riga di origine e fare clic su **[!UICONTROL Delete]**.

1. Nel messaggio di conferma, fai clic su **[!UICONTROL Delete]**.

## Visualizzare il registro delle modifiche per un’origine pubblico

Puoi visualizzare i dettagli sulle modifiche apportate a un record di origine del pubblico e, facoltativamente, allegare note al registro.

1. Nel menu principale, fai clic su **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Tenere premuto il cursore sulla riga di origine e fare clic su **[!UICONTROL Change log]**.

1. (Facoltativo) Per allegare una nota al log delle modifiche:

   1. Tenere premuto il cursore sulla riga di origine e fare clic su **[!UICONTROL Add Notes]**.

   1. Immettere la nota, quindi fare clic su **[!UICONTROL Save]**.

      La lunghezza massima è di 256 caratteri.

1. (Facoltativo) Per aprire il registro in una schermata di dettaglio più grande, tenere premuto il cursore sulla riga di origine e fare clic su **[!UICONTROL View Details]**.

## Impostazioni origine pubblico {#source-settings}

**[!UICONTROL Data Visibility Level]:** Se i segmenti sono disponibili per un singolo inserzionista con accesso all’account (*[!UICONTROL Advertiser]*) o a tutti gli inserzionisti con accesso all&#39;account *[!UICONTROL Account]*.

**[!UICONTROL Advertiser]:** (Solo visibilità a livello di inserzionista) L’inserzionista per il quale sono disponibili i segmenti. Selezionane uno dall’elenco degli inserzionisti con accesso all’account.

**[!UICONTROL Enter IMS Org Id]:** ([!DNL Real-Time CDP] solo origini) L&#39;ID organizzazione Adobe Experience Cloud per il [!DNL Adobe Experience Platform] account.

**[!UICONTROL Convert PII to the following IDs]:** I tipi di ID in cui convertirai le tue informazioni personali identificabili (PII). Se selezioni più tipi, il segmento generato viene compilato con valori per ciascun tipo di ID selezionato (ad esempio [!DNL RampID] e un [!DNL Unified ID2.0] per ciascun indirizzo e-mail). Gli oneri per i dati sono applicati di conseguenza.

Per [!DNL RampID] e [!DNL Unified ID2.0], il fornitore cerca ogni indirizzo e-mail per vedere se esiste già un ID e traduce l’indirizzo in un ID corrispondente quando disponibile. Se per l&#39;indirizzo non esiste alcun ID, viene creato un nuovo ID.

>[!NOTE]
>
>Puoi eseguire il targeting per un solo tipo di ID in un singolo posizionamento. Per verificare le prestazioni per tipo di ID: [creare un posizionamento separato](/help/dsp/campaign-management/placements/placement-create.md) per ogni tipo di ID nel segmento.

* *[!DNL RampID]:* Per convertire i dati PII in una [!DNL RampID]. È possibile utilizzare [!DNL RampIDs] per il retargeting degli utenti che accedono e per [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) misurazione.

* *[!DNL Unified ID2.0](Beta):* Per convertire i dati PII in una [ID unificato 2.0](https://unifiedid.com) ID per il retargeting degli utenti che accedono.

<!-- Later
* *[!DNL ID5] (Beta):* To convert PII to an [!DNL ID5] ID. You can use [!DNL ID5] IDs for retargeting logging-in users and for [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) measurement.

-->

**[!UICONTROL Terms of Service]:** I termini del contratto di servizio per la conversione di PII in ID universali. Prima di poter convertire i dati in un nuovo tipo di ID, tu o un altro utente dell’account DSP dovete accettare i termini una volta. Per i clienti con contratti di assistenza gestiti, il team dell’account Adobe otterrà il consenso e accetterà i termini per conto della tua organizzazione. Per leggere i termini, fai clic su **>**. Per accettare i termini, scorri fino alla parte inferiore dei termini e fai clic su **[!UICONTROL Accept]**.

**[!UICONTROL Source Key]:** (Sola lettura; generato automaticamente) La chiave di origine che puoi utilizzare per creare una connessione di destinazione nella piattaforma di dati del cliente per inviare pubblici a Advertising DSP. Puoi copiare il valore negli Appunti per incollarlo nelle impostazioni di connessione di destinazione o in un file.

>[!MORELIKETHIS]
>
>* [Informazioni sulle origini del pubblico di prime parti](source-about.md)
>* [Importare manualmente segmenti autenticati da [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Connessione Adobe Advertising DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Informazioni su Gestione dell&#39;audience](/help/dsp/audiences/audience-about.md)
