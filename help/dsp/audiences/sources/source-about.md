---
title: Informazioni sull’attivazione di segmenti autenticati da origini pubblico
description: Scopri come acquisire segmenti di prime parti da una piattaforma di dati cliente.
feature: DSP Audiences
exl-id: ba056440-fa2b-4472-bbfd-16dd0af887f1
source-git-commit: f6308ac9af8019987f4a2e501cba6b019cb032b6
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 0%

---

# Informazioni sull’attivazione di segmenti autenticati da origini pubblico

<!-- Doesn't specifically explain what you can do in our UI -->
*Funzione beta*

L’DSP può acquisire segmenti di prime parti composti da segnali autenticati incorporati in una piattaforma di dati cliente (CDP). Puoi utilizzare i segmenti acquisiti come destinazioni per i posizionamenti.

## [!DNL Adobe Real-Time Customer Data Profile]

L&#39;DSP è integrato con [il [!DNL Adobe Real-Time Customer Data Profile (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html), che fa parte di Adobe Experience Platform.

In entrata [!DNL Real-time CDP], *destinazioni* sono connessioni a piattaforme dati esterne che consentono l’attivazione diretta dei dati. Ad esempio, puoi utilizzare le destinazioni per attivare le relazioni con i clienti note (come gli indirizzi e-mail con hash) per la pubblicità mirata nei formati digitali supportati dall’DSP.

Per ulteriori informazioni sulle destinazioni, vedi l’Experience Platform [Guida alle destinazioni](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html), inclusa una panoramica del prodotto, istruzioni per [creazione di aree di lavoro di destinazione](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/destinations-workspace.html) e [creazione di connessioni di destinazione](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html), e [attivazione dei dati nelle destinazioni](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-segment-streaming-destinations.html).

### Flusso di lavoro per l&#39;utilizzo dell&#39;integrazione DSP con [!DNL Real-time CDP] {#workflow-sources}

<!-- Make sure that titles make the distinctions clear -- everything can't be "Activate XXX." -->

1. [Consentire all’DSP di tradurre i segmenti di dati dei clienti in [!DNL LiveRamp RampIDs]](source-durable-id.md) che sono riconoscibili in un ambiente in cui è possibile fare offerte.<!-- I don't think I need this here: This requires DSP account-level and campaign-level settings to enable segment sharing with [!DNL LiveRamp], which will translate customer data to [!DNL RampIDs] to create targetable segments. Your Adobe Account Team will perform this configuration. -->

1. [Creare un’origine di pubblico](source-create.md) per importare tipi di pubblico sul tuo account DSP o su un account inserzionista.

1. [Configurare un [!DNL Real-Time CDP] connessione di destinazione in Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).

Per ulteriore supporto, contatta il team del tuo account Adobe o `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Attivare segmenti autenticati dai partner ID resistenti](source-durable-id.md)
>* [Creare un’origine di pubblico per attivare tipi di pubblico di prime parti](source-create.md)
>* [Impostazioni origine pubblico](source-settings.md)
>* [Adobe Advertising DSP Connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [Panoramica del catalogo delle destinazioni](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [Informazioni su Gestione dell&#39;audience](/help/dsp/audiences/audience-about.md)

