---
title: Impostazioni origine pubblico
description: Scopri le impostazioni delle origini del pubblico.
feature: DSP Audiences
exl-id: 274ea502-ad15-4d3d-922a-17caddb87f69
source-git-commit: 6c918b387067237de5d1eae42ae8ad253884d761
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---

# Impostazioni origine pubblico

**[!UICONTROL Data Visibility Level]:** Se i segmenti sono disponibili per un singolo inserzionista con accesso all’account (*[!UICONTROL Advertiser]*) o a tutti gli inserzionisti con accesso all&#39;account *[!UICONTROL Account]*.

**[!UICONTROL Advertiser]:** (Solo visibilità a livello di inserzionista) L’inserzionista per il quale sono disponibili i segmenti. Selezionane uno dall’elenco degli inserzionisti con accesso all’account.

**[!UICONTROL Enter IMS Org Id]:** ([!DNL Real-Time CDP] solo origini) L&#39;ID organizzazione Adobe Experience Cloud per il [!DNL Adobe Experience Platform] account.

**[!UICONTROL Convert PII to the following IDs]:** ([!DNL ActionIQ] e [!DNL Tealium] solo sorgenti) Il tipo di ID in cui desideri convertire i dati personali (PII, personally identifiable information). Gli oneri per i dati sono applicati di conseguenza.

* *[!DNL RampID]:* Per convertire PII in un RampID. Se si sceglie *[!DNL RampID]*, i segmenti vengono tradotti in [!DNL RampIDs] automaticamente.

* *[!DNL Unified ID2.0]:* ([!DNL ActionIQ] solo sorgenti) Per convertire i dati PII in [ID unificato 2.0](https://unifiedid.com/).

**[!UICONTROL Source Key]:** (Sola lettura; generato automaticamente) La chiave di origine che puoi utilizzare per creare una connessione di destinazione nella piattaforma di dati del cliente per inviare pubblici a Advertising DSP. Puoi copiare il valore negli Appunti per incollarlo nelle impostazioni di connessione di destinazione o in un file.

>[!MORELIKETHIS]
>
>* [Creare un’origine di pubblico per attivare tipi di pubblico di prime parti](source-create.md)
>* [Informazioni sull’attivazione di segmenti autenticati da origini pubblico](source-about.md)
>* [Attivare segmenti autenticati dai partner Universal ID](source-universal-id.md)
>* [Connessione Adobe Advertising DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Informazioni su Gestione dell&#39;audience](/help/dsp/audiences/audience-about.md)
