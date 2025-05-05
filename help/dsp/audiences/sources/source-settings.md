---
title: Impostazioni Audience Source
description: Scopri le impostazioni delle origini del pubblico.
feature: DSP Audiences
exl-id: 274ea502-ad15-4d3d-922a-17caddb87f69
source-git-commit: 295cc610a7e5e811fe555db69373a8bf5b4012f7
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 0%

---

# Impostazioni Audience Source

*funzionalità Beta*

**[!UICONTROL Data Visibility Level]:** se i segmenti sono disponibili per un singolo inserzionista con accesso all&#39;account (*[!UICONTROL Advertiser]*) o per tutti gli inserzionisti con accesso all&#39;account *[!UICONTROL Account]*.

**[!UICONTROL Advertiser]:** (solo visibilità a livello di inserzionista) L&#39;inserzionista per il quale sono disponibili i segmenti. Selezionane uno dall’elenco degli inserzionisti con accesso all’account.

**[!UICONTROL Enter IMS Org Id]:** ([!DNL Real-Time CDP] solo origini) ID organizzazione Adobe Experience Cloud per l&#39;account [!DNL Adobe Experience Platform].

**[!UICONTROL Convert PII to the following IDs]:** i tipi di ID in cui verranno convertite le informazioni personali (PII, personally identifiable information). Se selezioni più tipi, il segmento generato viene compilato con valori per ciascun tipo di ID selezionato (ad esempio [!DNL RampID] e [!DNL Unified ID2.0] per ciascun indirizzo e-mail). Gli oneri per i dati sono applicati di conseguenza.

Per [!DNL RampID] e [!DNL Unified ID2.0], il fornitore cerca ogni indirizzo e-mail per vedere se esiste già un ID e converte l&#39;indirizzo in un ID corrispondente quando disponibile. Se per l&#39;indirizzo non esiste alcun ID, viene creato un nuovo ID.

>[!NOTE]
>
>Puoi eseguire il targeting per un solo tipo di ID in un singolo posizionamento. Per verificare le prestazioni in base al tipo di ID, [crea un posizionamento separato](/help/dsp/campaign-management/placements/placement-create.md) per ogni tipo di ID nel segmento.

* *[!DNL RampID]:* Per convertire PII in [!DNL RampID]. È possibile utilizzare [!DNL RampIDs] per il retargeting degli utenti che accedono e per la misurazione di [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md).

* *[!DNL Unified ID2.0] (Beta):* Per convertire PII in un ID [Unified ID 2.0](https://unifiedid.com) per il retargeting degli utenti che accedono.

<!-- Later
* *[!DNL ID5] (Beta):* To convert PII to an [!DNL ID5] ID. You can use [!DNL ID5] IDs for retargeting logging-in users and for [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) measurement.

-->

**[!UICONTROL Terms of Service]:** I termini del contratto di servizio per la conversione di PII in ID universali. Prima di poter convertire i dati in un nuovo tipo di ID, tu o un altro utente dell’account DSP dovete accettare i termini una volta. Per i clienti con contratti di assistenza gestiti, il team dell’account Adobe otterrà il consenso e accetterà i termini per conto della tua organizzazione. Per leggere i termini, fare clic su **>**. Per accettare i termini, scorrere fino alla fine dei termini e fare clic su **[!UICONTROL Accept]**.

**[!UICONTROL Source Key]:** (sola lettura; generata automaticamente) La chiave di origine che puoi utilizzare per creare una connessione di destinazione nella piattaforma dati del cliente per inviare pubblici ad Advertising DSP. Puoi copiare il valore negli Appunti per incollarlo nelle impostazioni di connessione di destinazione o in un file.

>[!MORELIKETHIS]
>
>* [Gestione delle origini del pubblico per attivare i tipi di pubblico con ID universale](source-manage.md)
>* [Informazioni sulle origini del pubblico di prime parti](source-about.md)
>* [Importa manualmente segmenti autenticati da [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Connessione Adobe Advertising DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Informazioni su Gestione dell&#39;audience](/help/dsp/audiences/audience-about.md)
