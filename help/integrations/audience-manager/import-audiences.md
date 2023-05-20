---
title: Importare segmenti Adobe Audience Manager per il targeting di annunci
description: Scopri come importare il [!DNL Adobe] tipi di pubblico per Advertising DSP e Search via Adobe Audience Manager
feature: Integration with Adobe Audience Manager
exl-id: 6ff80699-9554-4b39-a019-d8055d68c174
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '763'
ht-degree: 0%

---

# Importare segmenti Adobe Audience Manager per il targeting di annunci

Advertising DSP e [!DNL Advertising Search, Social, & Commerce] ognuno può estrarre metadati, dati gerarchici e dati di pubblico univoci per tutti gli inserzionisti o le agenzie di [!DNL Adobe] audience<!-- segments or audiences? Standardize terms per AAM's docs -->. Ciò include i dati per:

* Segmenti Adobe Audience Manager

* Segmenti Adobe Analytics pubblicati in Adobe Experience Cloud

* Segmenti creati con Adobe Experience Cloud [!DNL Audience Library]

* Segmenti creati in Adobe Experience Platform e inviati ad Adobe Advertising tramite Audience Manager

Per accedere [!DNL Adobe] pubblico in DSP o [!DNL Creative], è necessario importare i tipi di pubblico in DSP. Per accedere [!DNL Adobe] tipi di pubblico in [!DNL Search, Social, & Commerce], è necessario importare i tipi di pubblico in [!DNL Search, Social, & Commerce].

## Prerequisiti

* L&#39;inserzionista deve implementare [il [!DNL Adobe Experience Cloud Identity (ECID) Service]](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) versione 2.0 o successiva. Il [!DNL Identity Service] fornisce un ID universale e costante che identifica i visitatori in tutte le soluzioni di Experience Cloud.

   L’implementazione include l’aggiunta di [!DNL Identity service] codice per ogni pagina web sui siti dell’inserzionista.

* L’organizzazione deve essere [abilitato per i servizi Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/services/core-services.html) e avere un Experience Cloud [!DNL Organization ID] (precedentemente denominato [!DNL IMS org ID]).

   Il [!UICONTROL Organization ID] consente alle organizzazioni con più prodotti Adobe Experience Cloud di condividere i dati tra alcuni di essi.

* (Per gli inserzionisti che [!DNL Analytics]) L&#39;inserzionista deve [implementare [!DNL Analytics] utilizzo `appMeasurement.js`](https://experienceleague.adobe.com/docs/analytics/implementation/js/overview.html) versione 1.6.4 o successiva.

* I visitatori del sito Web dell&#39;inserzionista non includono un volume elevato di [!DNL Apple Safari] utenti.

* (Consigliato quando l’inserzionista utilizza sia l’Audience Manager che [!DNL Analytics]) Per ridurre le chiamate a ogni pagina web, rimuovi l’Audience Manager esistente [!DNL Data Integration Library] codice per la raccolta dei dati e attivazione dell&#39;inoltro lato server per ogni [!DNL Analytics] suite di rapporti. Per ulteriori informazioni, consulta la sezione &quot;[Panoramica sull&#39;inoltro lato server](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html).

* (Consigliato) Per percentuali di corrispondenza più alte, invia solo i dati del sito web di prime parti ad Adobe Advertising. Se l’inserzionista unisce dati di terze parti o dati offline da un sistema di gestione delle relazioni con i clienti, la perdita di dati può ridurre le percentuali di corrispondenza.

## Importare tipi di pubblico Audience Manager nell’DSP

### Passaggi per importare tipi di pubblico in DSP

Il [!DNL Adobe] i team delle operazioni di account e dati eseguiranno i seguenti passaggi.

1. Il team dell’account Adobe deve configurare l’impostazione a livello di inserzionista &quot;[!UICONTROL Adobe Analytics Cloud].&quot;

1. Il team dell’account Adobe deve inviare una richiesta<!-- Submit a request as a JIRA task? --> al team operazioni dati<!-- implementation team? --> per importare i segmenti di Audience Manager dell’organizzazione utilizzando l’integrazione API nativa di Advertising DSP.

### Quali modifiche si traducono in Audience Manager?

L’API automaticamente:

* Crea due destinazioni DSP in Audience Manager:

   * **[!UICONTROL Adobe Ad Cloud Cross-Channel (real-time)]**

   * **[!UICONTROL Adobe AdCloud Cross-Channel (batch)])**

* Mappa le due destinazioni su tutti i segmenti Audience Manager, consentendo all’Audience Manager di condividere i segmenti con l’account dell’inserzionista DSP associato allo stesso Experience Cloud [!DNL Organization ID] utilizzato ad Audience Manager. <!-- Verify -->

   Facoltativamente, l’organizzazione può rimuovere i segmenti non necessari dalle destinazioni all’interno di Audience Manager.

* Aggiunge il seguente pixel di sincronizzazione dei cookie di exchange al contenitore Audience Manager dell’organizzazione per migliorare la portata delle campagne dei clienti:

   * Adobe AdCloud: 411 (standard e automatico come parte di [!DNL Identity Service] versione 2.0. Organizzazioni [!DNL Identity Service] le versioni successive alla versione 2.0 devono aggiungere questo pixel al contenitore di Audience Manager.

## Importa tipi di pubblico Audience Manager in [!DNL Search, Social, & Commerce]

### Passaggi per importare tipi di pubblico in [!DNL Search, Social, & Commerce]

[!DNL Adobe] Il personale eseguirà la maggior parte o tutti i seguenti passaggi.

1. Il team dell’account Adobe deve inviare una richiesta al team delle operazioni sui dati per configurare un’integrazione tra [!DNL Search, Social, & Commerce] e Audience Manager. Includi i nomi dei segmenti di Audience Manager in cui desideri esportare [!DNL Search, Social, & Commerce].

1. In Audience Manager, configura le destinazioni per [!DNL Search, Social, & Commerce]:

   1. Crea due nuove destinazioni: `[!UICONTROL Adobe Media Optimizer (HTTP)]` e `[!UICONTROL Adobe Media Optimizer Batch Destination]`.

      [!DNL Media Optimizer] è un nome precedente per [!DNL Search, Social, & Commerce].

   1. Specifica i segmenti per ciascuna destinazione.

      Con il [!UICONTROL Automatically map all current and future segments] , tutti i segmenti vengono mappati e sincronizzati ogni giorno.

      Il [!UICONTROL Manually map segments] consente di mappare manualmente i segmenti da sincronizzare con la destinazione batch (`[!UICONTROL Adobe Media Optimizer Batch Destination]`). Non è necessario mappare manualmente alcun segmento alla destinazione HTTP.

1. Entro [!DNL Search, Social, & Commerce], il [!DNL Search, Social, & Commerce] il team di implementazione o un utente con il ruolo direct access client manager deve avviare l’importazione da [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Audience Manager Setup].

   Inserisci l’Experience Cloud dell’organizzazione [!DNL Organization ID] ([!DNL IMS org ID]). L’ID deve essere lo stesso utilizzato per l’account di Audience Manager dell’organizzazione.

### Quali modifiche si traducono in Audience Manager?

L’organizzazione ne vedrà due [!DNL Search, Social, & Commerce] destinazioni in Audience Manager:

* **[!UICONTROL Adobe Media Optimizer (HTTP)]**
* **[!UICONTROL Adobe Media Optimizer Batch Destination])**

## Sincronizzazione dati

L’importazione iniziale richiede circa 24 ore. Dopo l’importazione iniziale, i dati vengono sincronizzati in tempo reale, con un ritardo di uno o due secondi.

<!--
### How DSP Syncs the Data

DSP syncs the data automatically using the [!DNL Adobe Experience Cloud Identity (ECID) Service]. During synchronization, the [!DNL ECID Service] calls Adobe Advertising at [!DNL cm.eversttech.net]. Because Adobe Advertising is a trusted domain, ID syncs take place from parent pages rather than within the destination publishing iframes, as they do with most third-party activation partners. Audience Manager identifies unique users by device IDs, using the [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html#global-device-ids), also called the [!DNL Device ID].

![Synchronization of [!DNL Adobe] audiences in DSP](/help/integrations/assets/audience-manager-sync.png)

### How Search Syncs the Data
-->

<!-- 
Segment membership data is sent only after one of the following events occurs:

* (Advertisers with DSP):

  * The segment is targeted in an Adobe Advertising display ad.

  * The segment is added to the [!DNL Adobe AdCloud Cross-Channel] batch and real-time destinations within the Audience Manager user interface.

* (Advertisers with [!DNL Search, Social, & Commerce]):

  * The segment is targeted in an Adobe Advertising search ad.

  * The segment is added to the [!DNL Adobe Media Optimizer] batch and HTTP destinations within the Audience Manager user interface.
 -->
<!-- Is membership data/whatever available in Creative? If so, does it show the same as DSP? -->

## Dove trovare i segmenti sincronizzati

### Nell&#39;DSP

In DSP, i nomi dei segmenti sono organizzati in base alla tassonomia Audience Manager e sono disponibili con i conteggi di appartenenza ai segmenti corrispondenti in:

* [Impostazioni di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md#audience-targeting): al [!UICONTROL Adobe Segments] scheda di [!UICONTROL Audience Targeting] sezione.

* In entrata [impostazioni pubblico](/help/dsp/audiences/audience-settings.md): al [!UICONTROL Adobe Segments] scheda.

### In Advertising Creative

In entrata [!DNL Creative], i segmenti sono disponibili nelle impostazioni di esperienza per i nodi di destinazione.

### In entrata [!DNL Advertising Search, Social, & Commerce]

In entrata [!DNL Search, Social, & Commerce], i segmenti sono disponibili quando crei una [!DNL Google] pubblico che utilizza [!UICONTROL Data Source] &quot;[!UICONTROL Adobe Audience]&quot; da [!UICONTROL Campaigns] > [!UICONTROL Audiences] > [!UICONTROL Library].

Per ogni [!DNL Google] pubblico che hai creato, [!DNL Google] fornisce la dimensione del pubblico.

>[!MORELIKETHIS]
>
>* [Integrazioni di Adobe Advertising con Adobe Audience Manager](/help/integrations/audience-manager/overview.md)

