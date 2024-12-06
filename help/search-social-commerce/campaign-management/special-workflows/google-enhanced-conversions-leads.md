---
title: Implementa [!DNL Google Ads] conversioni avanzate per i lead
description: Scopri il flusso di lavoro per impostare [!DNL Google Ads] conversioni avanzate per i lead.
feature: Search Campaign Management, Conversions
exl-id: b708c9f2-2962-45d9-8780-4e96ef2ae8f7
source-git-commit: e0b1a65e3eddc41bed73817dabb6e38b1ef881b5
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 0%

---

# Implementa [!DNL Google Ads] conversioni avanzate per i lead

Solo *[!DNL Google Ads]account*

[[!DNL Google Ads] le conversioni avanzate per i lead](https://support.google.com/google-ads/answer/9888656) ti consentono di mappare gli utenti alle conversioni offline utilizzando i dati di conversione di prime parti. Utilizza le conversioni avanzate per i lead in ambienti in cui gli ID clic non sono disponibili, ad esempio per monitorare le vendite tramite telefono o e-mail derivanti dai lead del sito web.

In Search, Social e Commerce puoi effettuare le seguenti operazioni:

* Visualizza le conversioni avanzate esistenti per i lead.

  Search, Social e Commerce sincronizzano le conversioni avanzate esistenti per i lead ogni giorno alle 05:00 nel fuso orario dell&#39;inserzionista.

* Creare conversioni avanzate per i lead.

* Carica dati di conversione offline di prime parti da mappare sulle conversioni avanzate per i lead.

* Includi le conversioni avanzate per i lead come metriche nei rapporti e come metriche ponderate negli obiettivi per l’ottimizzazione.

Per utilizzare questa funzione, completa i passaggi seguenti. I passaggi per creare i tag di tracciamento delle conversioni e per creare azioni di conversione possono facoltativamente essere annullati.

1. Entro [!DNL Google Ads], acconsentire alle conversioni avanzate per i lead:

   1. Apri le impostazioni di conversione dell’account.

   1. Selezionare l&#39;opzione per le conversioni avanzate per i lead e accettare i termini di servizio.

   1. Selezionare se utilizzare un tag [!DNL Google] o [!DNL Google Tag Manager] per creare il tag di conversione.

1. Configura e implementa un tag per tenere traccia dell’azione di conversione.

   Per istruzioni, vedere la Guida di [!DNL Google Ads] per creare tag per conversioni avanzate per lead [che utilizzano un  [!DNL Google] tag](https://support.google.com/google-ads/answer/11021502) o [che utilizzano [!DNL Google Tag Manager]](https://support.google.com/google-ads/answer/11347292).

1. Crea un&#39;azione di conversione per la conversione avanzata per i lead in [Search, Social e Commerce](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md) o [Google Ads](https://support.google.com/google-ads/answer/12216226).

   Se crei l&#39;azione di conversione in Search, Social e Commerce, specifica il **Tipo di conversione** come *Importa conversione* o *Importa.*

1. Se necessario, carica dati di prime parti, inclusi indirizzi e-mail con hash o numeri di telefono, per attribuire la conversione a un account specificato. Puoi completare questo passaggio da [Search, Social e Commerce](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md) o utilizzando [!DNL Google Data Manager].

   * In Search, Social e Commerce è possibile scaricare un modello in formato [!DNL Microsoft Excel], immettere i dati di conversione e salvare il file localmente, quindi caricare il file modificato. Il modello include colonne per indicare se è stato fornito il consenso dell&#39;utente per il caricamento di dati in [!DNL Google] a scopo pubblicitario e di personalizzazione degli annunci.

     Tutti i dati caricati vengono sincronizzati in tempo reale in [!DNL Google Ads].

   * Per ulteriori informazioni sul caricamento di dati tramite [!DNL Google Data Manager], vedere &quot;[Informazioni sul gestore dati](https://support.google.com/google-ads/answer/14639041)&quot;.

>[!MORELIKETHIS]
>
>* [Crea un&#39;azione di conversione per  [!DNL Google Ads] conversione avanzata per lead](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)
>* [Carica dati di conversione offline per conversioni avanzate](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
