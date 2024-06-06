---
title: Creare e gestire le origini del pubblico per attivare i tipi di pubblico con ID universale
description: Scopri come creare e gestire un’origine per importare i tipi di pubblico dalla piattaforma di dati dei clienti e convertirli in segmenti contenenti ID universali.
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
source-git-commit: 295cc610a7e5e811fe555db69373a8bf5b4012f7
workflow-type: tm+mt
source-wordcount: '369'
ht-degree: 0%

---

# Creare un’origine di pubblico per attivare i tipi di pubblico con ID universale

*Funzione beta*

Crea un’origine in DSP per ogni pubblico di prime parti nella piattaforma di dati cliente che desideri convertire in segmenti contenenti tipi di ID universali specificati. Puoi importare i segmenti nell’account DSP della tua organizzazione o in un account inserzionista. Gli addebiti per i dati vengono applicati in base ai tipi di ID universali selezionati.

Sono necessari passaggi aggiuntivi per acquisire i tipi di pubblico da ogni piattaforma di dati cliente. Vedere la nota alla fine della procedura.

## Creare un’origine di pubblico

1. Nel menu principale, fai clic su **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Clic **[!UICONTROL Add Source]**.

1. In [!UICONTROL Select a Type] selezionare la piattaforma dati del cliente:

   * *[!UICONTROL RT-CDP]*: [Il [!DNL Adobe Real-Time Customer Data Platform]](source-about.md).

   * *[!UICONTROL ActionIQ]*: Il [[!DNL ActionIQ] piattaforma dati cliente](source-about.md).

   * *[!UICONTROL Tealium CDP]*: (solo utenti configurati) Il [[!DNL Tealium] piattaforma dati cliente](source-about.md).

1. Specifica la [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* o *[!UICONTROL Account]*.

1. Inserisci il valore rimanente [impostazioni di origine](source-settings.md).

   Mantieni una copia di [!UICONTROL Source Key] che viene generato. Il valore ti servirà più tardi.

1. Clic **[!UICONTROL Save]**.

>[!NOTE]
>
>Dopo aver creato un’origine per la piattaforma di dati cliente, dovrai completare ulteriori passaggi. Consulta la [flusso di lavoro per importare tipi di pubblico da [!DNL Adobe] [!DNL Real-time CDP]](source-adobe-rtcdp.md)<!-- the [activation workflow for [!DNL ActionIQ]](source-actioniq.md), --> e [flusso di lavoro per importare tipi di pubblico da [!DNL Tealium]](source-tealium.md).

## Modificare i tipi di ID per un’origine pubblico

1. Nel menu principale, fai clic su **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Tenere premuto il cursore sulla riga di origine e fare clic su **[!UICONTROL Edit]**.

1. Modificare il [ID selezionati per l’origine](source-settings.md).

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

>[!MORELIKETHIS]
>
>* [Impostazioni origine pubblico](source-settings.md)
>* [Informazioni sulle origini del pubblico di prime parti](source-about.md)
>* [Connessione Adobe Advertising Cloud DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Informazioni su Gestione dell&#39;audience](/help/dsp/audiences/audience-about.md)
