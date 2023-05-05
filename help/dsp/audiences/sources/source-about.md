---
title: Informazioni sull’attivazione dei segmenti autenticati da Audience Sources
description: Scopri come acquisire segmenti di prime parti da una piattaforma dati del cliente.
feature: DSP Audiences
exl-id: ba056440-fa2b-4472-bbfd-16dd0af887f1
source-git-commit: 68095fc77659826fae43f2453d17022ef1880807
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 2%

---

# Informazioni sull’attivazione dei segmenti autenticati da Audience Sources

<!-- Doesn't specifically explain what you can do in our UI -->

DSP acquisire segmenti di prime parti formati da segnali autenticati generati all’interno di una piattaforma dati del cliente (CDP). Puoi utilizzare i segmenti acquisiti come destinazioni per i posizionamenti.

## [!DNL Adobe Real-Time Customer Data Profile]

DSP è integrato con [la [!DNL Adobe Real-Time Customer Data Profile (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=it), che fa parte del Adobe Experience Platform.

In [!DNL Real-time CDP], *destinazioni* sono connessioni a piattaforme di dati esterne che consentono l’attivazione senza soluzione di continuità dei dati. Ad esempio, puoi utilizzare le destinazioni per attivare le relazioni con i clienti note (ad esempio indirizzi e-mail con hash) per annunci pubblicitari mirati nei formati digitali supportati da DSP.

Per ulteriori informazioni sulle destinazioni, consulta l’Experience Platform [Guida alle destinazioni](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html), compresa una panoramica del prodotto, istruzioni per [creazione di aree di lavoro di destinazione](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/destinations-workspace.html) e [creazione di connessioni di destinazione](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html)e [attivazione dei dati nelle destinazioni](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-segment-streaming-destinations.html).

### Flusso di lavoro per l’utilizzo dell’integrazione DSP con [!DNL Real-time CDP] {#workflow-sources}

1. [Consentire DSP tradurre i segmenti di dati dei clienti in [!DNL LiveRamp RampIDs]](source-durable-id.md) riconoscibili in un ambiente accessibile.<!-- I don't think I need this here: This requires DSP account-level and campaign-level settings to enable segment sharing with [!DNL LiveRamp], which will translate customer data to [!DNL RampIDs] to create targetable segments. Your Adobe Account Team will perform this configuration. -->

1. [Creare una sorgente di pubblico](source-create.md) per importare i tipi di pubblico nel tuo account DSP o un account inserzionista.

1. [Configura un [!DNL Real-Time CDP] connessione di destinazione nell&#39;Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).

Per ulteriore supporto, contatta il team dell’account di Adobe o `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Attivare i segmenti autenticati dai partner ID durevoli](source-durable-id.md)
>* [Creare una sorgente di pubblico per attivare il pubblico di prime parti](source-create.md)
>* [Impostazioni origine pubblico](source-settings.md)
>* [Adobe Advertising DSP Connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [Panoramica del catalogo delle destinazioni](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [Informazioni sulla gestione dell&#39;audience](/help/dsp/audiences/audience-about.md)

