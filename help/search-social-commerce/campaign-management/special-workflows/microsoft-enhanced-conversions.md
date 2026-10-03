---
title: Implementa [!DNL Microsoft Advertising] conversioni avanzate per conversioni offline
description: Scopri il flusso di lavoro per la configurazione di [!DNL Microsoft Advertising] conversioni avanzate per conversioni offline.
feature: Search Campaign Management, Conversions
exl-id: 44937db7-9e80-4a5d-85c7-5bd5febc3b96
TQID: 'https://experienceleague.adobe.com/GLFczqDqV8HE5hUZt8ORAlQMNy4OqQTtMdaHoYoN10U'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
  - id: e6916c1b-e939-4e0b-99f5-768e83e1e99f
    internal-label: Conversion tracking
subfeature_v2:
  - id: d068b149-b9d1-421c-9033-a51495366ddc
    internal-label: Conversions
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 6d95caf72d11c404d866e8d091e1ffa89814ae73
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%
---
# Implementa [!DNL Microsoft Advertising] conversioni avanzate per conversioni offline

Solo *[!DNL Microsoft Advertising]account*

[[!DNL Microsoft Advertising] conversioni avanzate](https://help.ads.microsoft.com/#apex/ads/en/60178) ti consentono di mappare gli utenti alle conversioni offline utilizzando i dati di conversione di prime parti. Utilizza le conversioni avanzate in ambienti in cui gli ID clic non sono disponibili, ad esempio per monitorare le vendite tramite telefono o e-mail derivanti dai lead del sito web.

In Search, Social e Commerce puoi effettuare le seguenti operazioni:

* Visualizza le conversioni avanzate esistenti per le conversioni offline.

  Search, Social e Commerce sincronizzano le conversioni avanzate esistenti ogni giorno alle 05:00 nel fuso orario dell’inserzionista.

* Carica dati di conversione offline di prime parti da mappare sugli obiettivi di conversione avanzati esistenti.

* Includi le conversioni avanzate come metriche nei rapporti e come metriche ponderate negli obiettivi per l’ottimizzazione.

Per utilizzare questa funzione, completa i passaggi seguenti.

1. Segui tutti i prerequisiti nella Guida di [!DNL Microsoft Advertising] su &quot;[Conversioni avanzate](https://help.ads.microsoft.com/#apex/ads/en/60178).&quot;

1. [Configura un obiettivo di conversione avanzato entro [!DNL Microsoft Advertising]](https://help.ads.microsoft.com/#apex/ads/en/60178).

1. Se necessario, carica dati di prime parti, inclusi indirizzi e-mail con hash o numeri di telefono, per attribuire la conversione a un account specificato. Puoi completare questo passaggio da [Search, Social e Commerce](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md) o da [!DNL Microsoft Advertising].

   * In Search, Social e Commerce è possibile scaricare un modello in formato [!DNL Microsoft Excel], immettere i dati di conversione e salvare il file localmente, quindi caricare il file modificato.

     Tutti i dati caricati vengono sincronizzati in tempo reale in [!DNL Microsoft Advertising].

   * Per ulteriori informazioni sul caricamento di dati in [!DNL Microsoft Advertising], vedere la sezione &quot;Configurare conversioni avanzate per conversioni offline&quot; nella Guida di [!DNL Microsoft Advertising] in &quot;[Conversioni avanzate](https://help.ads.microsoft.com/#apex/ads/en/60178)&quot;.

>[!MORELIKETHIS]
>
>* [Carica dati di conversione offline per conversioni avanzate](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
