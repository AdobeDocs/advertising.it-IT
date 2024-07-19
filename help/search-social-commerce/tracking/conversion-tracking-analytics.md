---
title: Tracciamento delle conversioni Adobe Analytics
description: Scopri come utilizzare il tracciamento delle conversioni di Adobe Analytics per le campagne in Adobe Advertising.
exl-id: c72cc988-5b51-4e1a-8cb6-6c3ca2a0226b
feature: Search Tracking
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# Tracciamento delle conversioni Adobe Analytics

*Inserzionisti solo con integrazione Adobe Advertising-Adobe Analytics*

Per gli inserzionisti con un&#39;integrazione Adobe Advertising-Adobe Analytics, Advertising Cloud può collegare i clic e le impression degli annunci con le metriche di coinvolgimento e conversione del sito monitorate da [!DNL Analytics] quando utilizzi un reindirizzamento con token (parametro `ef_id`) negli URL di tracciamento dei clic per le [unità offerte](/help/search-social-commerce/glossary.md#a-b). I dati di [!DNL Analytics] vengono inviati automaticamente ad Advertising Cloud tramite un file di feed giornaliero.

Per ulteriori informazioni sull&#39;integrazione, vedere &quot;[Panoramica di [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-cloud/dsp/integrations/analytics/overview.html){target="_blank"}&quot;.

>[!PREREQUISITES]
>
> I fusi orari nell&#39;account dell&#39;inserzionista Search, Social e Commerce, nelle suite di rapporti [!DNL Analytics] e negli account della rete di annunci devono corrispondere. Se non corrispondono, si verificano varianze di dati tra i sistemi.

## Panoramica sull’implementazione

1. In [!DNL Analytics], il team di implementazione di Search, Social e Commerce modifica le seguenti impostazioni di configurazione per ogni suite di rapporti:

   * La scadenza per `ef_id` [!DNL eVar] è stata modificata per corrispondere all&#39;intervallo di lookback del clic dell&#39;inserzionista, ad Adobe Advertising.

   * L’ID utente Adobe Advertising.

   * Eventi standard e personalizzati da utilizzare per l’ottimizzazione.

1. In Search, Social e Commerce, il team di implementazione:

   1. Sincronizza la gerarchia degli account di rete degli annunci esistenti con Search, Social e Commerce.

   1. Aggiunge i reindirizzamenti con token &quot;`ef_id`&quot; che passano agli URL di tracciamento e li invia alla rete di annunci.

   Questo passaggio precede un reindirizzamento al server di tracciamento di Adobe Advertising (ad eccezione degli annunci [!DNL Google Ads] e [!DNL Microsoft Advertising] nei browser che supportano il tracciamento parallelo) e aggiunge un parametro &quot;ef_id&quot; popolato dinamicamente all&#39;URL al momento del clic dell&#39;annuncio. Quando si applica il tracciamento parallelo, gli utenti finali vengono inviati direttamente dall’annuncio all’URL finale e l’URL del modello di tracciamento (con la misurazione dei clic) viene caricato in background.

Una volta completata l&#39;integrazione, Search, Social e Commerce ricevono automaticamente tutti i dati evento sulla pagina tracciati in [!DNL Analytics] per le suite di rapporti configurate.

>[!MORELIKETHIS]
>
>* [Opzioni di tracciamento delle conversioni](conversion-tracking-about.md)
