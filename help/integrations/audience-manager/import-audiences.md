---
title: Importare segmenti Adobe Audience Manager per il targeting degli annunci
description: Scopri come importare il tuo [!DNL Adobe] tipi di pubblico in Advertising DSP e Search utilizzando Adobe Audience Manager
feature: Integration with Adobe Audience Manager
exl-id: 6ff80699-9554-4b39-a019-d8055d68c174
source-git-commit: 0b5e60f033d623bb6d342c6b56cb98f0bfcde916
workflow-type: tm+mt
source-wordcount: '763'
ht-degree: 0%

---

# Importare segmenti Adobe Audience Manager per il targeting degli annunci

DSP pubblicitarie e [!DNL Advertising Search] è possibile inserire metadati, dati gerarchici e dati di pubblico univoci per tutti gli inserzionisti o gli agenti [!DNL Adobe] pubblico<!-- segments or audiences? Standardize terms per AAM's docs -->. Sono inclusi i dati per:

* Segmenti Adobe Audience Manager

* Segmenti Adobe Analytics pubblicati in Adobe Experience Cloud

* Segmenti creati con Adobe Experience Cloud [!DNL Audience Library]

* Segmenti creati in Adobe Experience Platform e inviati ad Adobe Advertising tramite Audience Manager

Per accedere [!DNL Adobe] tipi di pubblico in DSP o [!DNL Creative], è necessario importare i tipi di pubblico in DSP. Per accedere [!DNL Adobe] tipi di pubblico in [!DNL [!DNL Search]], è necessario importare i tipi di pubblico in [!DNL Search]].

## Prerequisiti

* L’inserzionista deve implementare [la [!DNL Adobe Experience Cloud Identity (ECID) Service]](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) versione 2.0 o successiva. La [!DNL Identity Service] fornisce un ID universale e costante che identifica i visitatori in tutte le soluzioni di Experience Cloud.

   L&#39;implementazione include l&#39;aggiunta di [!DNL Identity service] a ogni pagina web sui siti dell&#39;inserzionista.

* L&#39;organizzazione deve essere [abilitato per i servizi di Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/services/core-services.html) e hanno un Experience Cloud [!DNL Organization ID] (precedentemente denominato [!DNL IMS org ID]).

   La [!UICONTROL Organization ID] consente alle organizzazioni con più prodotti Adobe Experience Cloud di condividere i dati tra alcuni dei prodotti.

* (Inserzionisti con [!DNL Analytics]) L&#39;inserzionista deve [implementare [!DNL Analytics] utilizzo `appMeasurement.js`](https://experienceleague.adobe.com/docs/analytics/implementation/js/overview.html) versione 1.6.4 o successiva.

* I visitatori del sito web dell&#39;inserzionista non includono un volume elevato di [!DNL Apple Safari] utenti.

* (consigliato quando l’inserzionista utilizza sia Audience Manager che [!DNL Analytics]) Per ridurre le chiamate a ogni pagina web, rimuovi l&#39;Audience Manager esistente [!DNL Data Integration Library] codice per la raccolta dati e abilitazione dell&#39;inoltro lato server per ogni [!DNL Analytics] suite di rapporti. Per ulteriori informazioni, consulta &quot;[Panoramica sull&#39;inoltro lato server](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html).

* (consigliato) Per percentuali di corrispondenza più elevate, invia solo dati di siti web di prime parti ad Adobe Advertising. Se l’inserzionista effettua il bundle di dati di terze parti o offline da un sistema di gestione delle relazioni con i clienti, la perdita di dati può ridurre le percentuali di corrispondenza.

## Importazione di tipi di pubblico di Audience Manager in DSP

### Passaggi per importare i tipi di pubblico in DSP

La [!DNL Adobe] i team per le operazioni sull’account e sui dati eseguiranno i seguenti passaggi.

1. La [!DNL Adobe] il team dell&#39;account deve configurare l&#39;impostazione a livello di inserzionista &quot;[!UICONTROL Adobe Analytics Cloud].&quot;

1. La [!DNL Adobe] il team dell&#39;account deve inviare una richiesta<!-- Submit a request as a JIRA task? --> al team delle operazioni di dati<!-- implementation team? --> importare i segmenti di Audience Manager dell’organizzazione utilizzando l’integrazione API nativa di Advertising DSP.

### Quali modifiche producono Audience Manager?

L’API automaticamente:

* Crea due destinazioni DSP in Audience Manager:

   * **[!UICONTROL Adobe Ad Cloud Cross-Channel (real-time)]**

   * **[!UICONTROL Adobe AdCloud Cross-Channel (batch)])**

* Mappa le due destinazioni a tutti i segmenti di Audience Manager, consentendo ad Audience Manager di condividere i segmenti con l’account DSP dell’inserzionista associato allo stesso Experience Cloud [!DNL Organization ID] utilizzato ad Audience Manager. <!-- Verify -->

   Facoltativamente, l’organizzazione può rimuovere i segmenti non necessari dalle destinazioni all’interno di Audience Manager.

* Aggiunge il seguente pixel di sincronizzazione cookie di scambio al contenitore Audience Manager dell’organizzazione per migliorare la portata delle campagne dei clienti:

   * Adobe AdCloud: 411 (Questo viene fornito standard e automaticamente come parte [!DNL Identity Service] versione 2.0. Organizzazioni con [!DNL Identity Service] le versioni inferiori alla 2.0 devono aggiungere questo pixel al contenitore di Audienci Manager.

## Importa tipi di pubblico di Audience Manager in [!DNL Search]

### Passaggi per importare i tipi di pubblico in [!DNL Search]

[!DNL Adobe] il personale eseguirà la maggior parte o tutti i seguenti passaggi.

1. La [!DNL Adobe] il team dell’account deve inviare una richiesta al team delle operazioni dati per impostare un’integrazione tra [!DNL Search] e Audience Manager. Includi i nomi dei segmenti di Audience Manager in cui desideri esportare [!DNL Search].

1. In Audience Manager, configura le destinazioni per [!DNL Search]:

   1. Crea due nuove destinazioni: `[!UICONTROL Adobe Media Optimizer (HTTP)]` e `[!UICONTROL Adobe Media Optimizer Batch Destination]`.

      [!DNL Media Optimizer] è un nome precedente per [!DNL Search].

   1. Specifica i segmenti per ciascuna delle destinazioni.

      Con la [!UICONTROL Automatically map all current and future segments] Tutti i segmenti sono mappati e sincronizzati ogni giorno.

      La [!UICONTROL Manually map segments] consente di mappare manualmente i segmenti da sincronizzare con la destinazione batch (`[!UICONTROL Adobe Media Optimizer Batch Destination]`). Nessun segmento deve essere mappato manualmente alla destinazione HTTP.

1. Within [!DNL Search], oppure [!DNL Search] il team di implementazione o un utente con il ruolo di gestione client ad accesso diretto deve avviare l&#39;importazione da [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Audience Manager Setup].

   Devi inserire l’Experience Cloud dell’organizzazione [!DNL Organization ID] ([!DNL IMS org ID]). L&#39;ID deve essere lo stesso utilizzato per l&#39;account Audience Manager dell&#39;organizzazione.

### Quali modifiche producono Audience Manager?

L&#39;organizzazione ne vedrà due [!DNL Search] destinazioni nell&#39;Audience Manager:

* **[!UICONTROL Adobe Media Optimizer (HTTP)]**
* **[!UICONTROL Adobe Media Optimizer Batch Destination])**

## Sincronizzazione dati

L&#39;importazione iniziale richiede circa 24 ore. Dopo l’importazione iniziale, i dati vengono sincronizzati in tempo reale con un ritardo di uno o due secondi.

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

* (Advertisers with [!DNL Search]):

  * The segment is targeted in an Adobe Advertising search ad.

  * The segment is added to the [!DNL Adobe Media Optimizer] batch and HTTP destinations within the Audience Manager user interface.
 -->
<!-- Is membership data/whatever available in Creative? If so, does it show the same as DSP? -->

## Dove trovare i segmenti sincronizzati

### In DSP

In DSP, i nomi dei segmenti sono organizzati in base alla tassonomia Audience Manager e disponibili con i conteggi corrispondenti per l’appartenenza al segmento in:

* [Impostazioni di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md#audience-targeting): Sulla [!UICONTROL Adobe Segments] della scheda [!UICONTROL Audience Targeting] sezione .

* In [impostazioni del pubblico](/help/dsp/audiences/audience-settings.md): Sulla [!UICONTROL Adobe Segments] scheda .

### In Advertising Creative

In [!DNL Creative], i segmenti sono disponibili nelle impostazioni dell’esperienza per i nodi di destinazione.

### In [!DNL Advertising Search]

In [!DNL [!DNL Search]], i segmenti sono disponibili quando crei una [!DNL Google] utilizzando [!UICONTROL Data Source] &quot;[!UICONTROL Adobe Audience]&quot; [!UICONTROL Campaigns] > [!UICONTROL Audiences] > [!UICONTROL Library].

Per ogni [!DNL Google] pubblico creato, [!DNL Google] fornisce le dimensioni del pubblico.

>[!MORELIKETHIS]
>
>* [Integrazioni pubblicitarie di Adobe con Adobe Audience Manager](/help/integrations/audience-manager/overview.md)

