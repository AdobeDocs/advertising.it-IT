---
title: Tracciamento delle conversioni Adobe Analytics
description: Scopri come utilizzare il tracciamento delle conversioni di Adobe Analytics per le campagne in Adobi Advertising.
exl-id: 0ed1d059-829a-4090-950d-41cbcc27b3ac
feature: Search Tracking
source-git-commit: 73cdb171523b55f48b5ae5c5b2b4843f542336a6
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# Tracciamento delle conversioni Adobe Analytics

*Per gli inserzionisti con solo integrazione Adobi Advertising-Adobe Analytics*

Per gli inserzionisti con un’integrazione Adobi Advertising-Adobe Analytics, Advertising Cloud può collegare i clic e le impression degli annunci con le metriche di coinvolgimento e conversione del sito tracciate da [!DNL Analytics] quando utilizzi un reindirizzamento con token (`ef_id` ) negli URL di tracciamento dei clic per il [unità di offerta](/help/search-social-commerce/glossary.md#a-b). Il [!DNL Analytics] I dati vengono inviati automaticamente ad Advertising Cloud tramite un file di feed giornaliero.

Consulta &quot;[Panoramica di [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-cloud/dsp/integrations/analytics/overview.html){target="_blank"}&quot; per ulteriori informazioni sull’integrazione.

>[!PREREQUISITES]
>
> Fusi orari nell’account dell’inserzionista di Search, Social &amp; Commerce, il [!DNL Analytics] le suite di rapporti e gli account di rete dell’annuncio devono corrispondere. Se non corrispondono, esistono delle varianze di dati tra i sistemi.

## Panoramica sull’implementazione

1. In entrata [!DNL Analytics], il team di implementazione di Search, Social &amp; Commerce modifica le seguenti impostazioni di configurazione per ogni suite di rapporti:

   * Scadenza per il `ef_id` [!DNL eVar] viene modificato per corrispondere all’intervallo di lookback del clic dell’inserzionista, ad Adobe Advertising.

   * L’ID utente Adobe Advertising.

   * Eventi standard e personalizzati da utilizzare per l’ottimizzazione.

1. In Search, Social e Commerce, il team di implementazione:

   1. Sincronizza la gerarchia degli account di rete degli annunci esistenti con Search, Social e Commerce.

   1. Aggiunge reindirizzamenti con &quot;`ef_id`&quot; token che passa agli URL di tracciamento e li invia alla rete di annunci.

   Questo passaggio precede un reindirizzamento al server di tracciamento di Adobi Advertising (ad eccezione di [!DNL Google Ads] e [!DNL Microsoft Advertising] annunci nei browser che supportano il tracciamento parallelo) e aggiunge un parametro &quot;ef_id&quot; popolato dinamicamente all’URL al momento del clic dell’annuncio. Quando si applica il tracciamento parallelo, gli utenti finali vengono inviati direttamente dall’annuncio all’URL finale e l’URL del modello di tracciamento (con la misurazione dei clic) viene caricato in background.

Una volta completata l’integrazione, Search, Social e Commerce ricevono automaticamente tutti i dati dell’evento sulla pagina tracciati in [!DNL Analytics] per le suite di rapporti configurate.

>[!MORELIKETHIS]
>
>* [Opzioni di tracciamento delle conversioni](conversion-tracking-about.md)
