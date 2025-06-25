---
title: Importare segmenti Adobe Audience Manager per il targeting di annunci
description: Scopri come importare i tipi di pubblico di  [!DNL Adobe]  in Advertising DSP e eseguire ricerche con Adobe Audience Manager
feature: Integration with Adobe Audience Manager
exl-id: 6ff80699-9554-4b39-a019-d8055d68c174
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '920'
ht-degree: 0%

---

# Importare segmenti Adobe Audience Manager per il targeting di annunci

Advertising DSP e [!DNL Advertising Search, Social, & Commerce] possono richiamare metadati, dati gerarchici e dati di pubblico univoci per tutti i tipi di pubblico [!DNL Adobe] dell&#39;inserzionista o dell&#39;agenzia<!-- segments or audiences? Standardize terms per AAM's docs -->, inclusi:

* Segmenti Adobe Audience Manager

* Segmenti Adobe Analytics pubblicati in Adobe Experience Cloud

* Segmenti creati con Adobe Experience Cloud [!DNL Audience Library]

* Segmenti creati in Adobe Experience Platform e inviati ad Adobe Advertising tramite Audience Manager

Per accedere a [!DNL Adobe] tipi di pubblico in DSP o [!DNL Creative], è necessario importare tali tipi di pubblico in DSP. Per accedere a [!DNL Adobe] tipi di pubblico in [!DNL Search, Social, & Commerce], è necessario importare i tipi di pubblico in [!DNL Search, Social, & Commerce].

## Prerequisiti

* L&#39;inserzionista deve implementare [la [!DNL Adobe Experience Cloud Identity (ECID) Service]](https://experienceleague.adobe.com/en/docs/id-service/using/intro/overview) versione 2.0 o successiva. [!DNL Identity Service] fornisce un ID universale e costante che identifica i visitatori in tutte le soluzioni di Experience Cloud.

  L&#39;implementazione include l&#39;aggiunta del codice [!DNL Identity service] a ogni pagina Web dei siti dell&#39;inserzionista.

* L&#39;organizzazione deve essere [abilitata per i servizi Experience Cloud](https://experienceleague.adobe.com/en/docs/core-services/interface/services/overview) e avere un Experience Cloud [!DNL Organization ID] (precedentemente denominato [!DNL IMS org ID]).

  [!UICONTROL Organization ID] consente alle organizzazioni con più prodotti Adobe Experience Cloud di condividere i dati tra alcuni di essi.

* (Inserzionisti con [!DNL Analytics]) L&#39;inserzionista deve [implementare [!DNL Analytics] utilizzando `appMeasurement.js`](https://experienceleague.adobe.com/en/docs/analytics/implementation/js/overview) versione 1.6.4 o successiva.

* I visitatori del sito Web dell&#39;inserzionista non includono un numero elevato di [!DNL Apple Safari] utenti.

* (Consigliato quando l&#39;inserzionista utilizza sia Audience Manager che [!DNL Analytics]) Per ridurre le chiamate a ogni pagina web, rimuovi il codice Audience Manager [!DNL Data Integration Library] esistente per la raccolta dati e abilita l&#39;inoltro lato server per ogni suite di rapporti [!DNL Analytics]. Per ulteriori informazioni, vedere &quot;[Panoramica sull&#39;inoltro lato server](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/server-side-forwarding/ssf).

* (Consigliato) Per percentuali di corrispondenza più alte, invia solo i dati del sito web di prime parti ad Adobe Advertising. Se l’inserzionista unisce dati di terze parti o dati offline da un sistema di gestione delle relazioni con i clienti, la perdita di dati può ridurre le percentuali di corrispondenza.

## Importare tipi di pubblico di Audience Manager in DSP

### Passaggi per importare tipi di pubblico in DSP

I team delle operazioni per l&#39;account e i dati di [!DNL Adobe] eseguono i passaggi seguenti.

1. Il team dell&#39;account Adobe deve configurare l&#39;impostazione a livello di inserzionista &quot;[!UICONTROL Adobe Analytics Cloud]&quot;.&quot;

1. Il team account di Adobe deve inviare una richiesta al team operazioni dati per importare i segmenti Audience Manager dell’organizzazione utilizzando l’integrazione API nativa di Advertising DSP.

### Quali modifiche risultano in Audience Manager?

L’API automaticamente:

* Crea due destinazioni DSP in Audience Manager:

   * **[!UICONTROL Adobe AdCloud Cross-Channel (real-time)]**

   * **[!UICONTROL Adobe AdCloud Cross-Channel (batch)]**

* Mappa le due destinazioni su tutti i segmenti di Audience Manager, consentendo ad Audience Manager di condividere i segmenti con l&#39;account dell&#39;inserzionista DSP associato allo stesso Experience Cloud [!DNL Organization ID] utilizzato per Audience Manager.

  Facoltativamente, l’organizzazione può rimuovere i segmenti non necessari dalle destinazioni all’interno di Audience Manager.

* Aggiunge il seguente pixel di sincronizzazione dei cookie di exchange al contenitore Audience Manager dell’organizzazione per migliorare la portata delle campagne dei clienti:

   * Adobe AdCloud: 411 (questo pixel è standard e automaticamente come parte della versione 2.0 di [!DNL Identity Service]. Le organizzazioni con [!DNL Identity Service] versioni precedenti alla 2.0 devono aggiungere questo pixel al proprio contenitore Audience Manager.

## Importa tipi di pubblico di Audience Manager in [!DNL Search, Social, & Commerce]

### Passaggi per importare tipi di pubblico in [!DNL Search, Social, & Commerce]

Il personale [!DNL Adobe] esegue la maggior parte o tutti i passaggi seguenti.

1. Il team dell&#39;account di Adobe deve inviare una richiesta al team delle operazioni sui dati per configurare un&#39;integrazione tra [!DNL Search, Social, & Commerce] e Audience Manager. Includere i nomi dei segmenti Audience Manager che si desidera esportare in [!DNL Search, Social, & Commerce].

1. In Audience Manager, configura le destinazioni per [!DNL Search, Social, & Commerce]:

   1. Creare due nuove destinazioni: `[!UICONTROL Adobe Media Optimizer (HTTP)]` e `[!UICONTROL Adobe Media Optimizer Batch Destination]`.

      [!DNL Media Optimizer] è un nome precedente per [!DNL Search, Social, & Commerce].

   1. Specifica i segmenti per ciascuna destinazione.

      Con l&#39;opzione [!UICONTROL Automatically map all current and future segments], tutti i segmenti vengono mappati e sincronizzati ogni giorno.

      L&#39;opzione [!UICONTROL Manually map segments] consente di mappare manualmente i segmenti da sincronizzare con la destinazione batch (`[!UICONTROL Adobe Media Optimizer Batch Destination]`). Non è necessario mappare manualmente alcun segmento alla destinazione HTTP.

1. In [!DNL Search, Social, & Commerce], il team di implementazione di [!DNL Search, Social, & Commerce] o un utente con ruolo di responsabile client di accesso diretto deve avviare l&#39;importazione da [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Admin] > [!UICONTROL Audience Manager Setup].

   Experience Cloud [!DNL Organization ID] ([!DNL IMS org ID]) dell&#39;organizzazione è obbligatorio. L’ID deve essere lo stesso utilizzato per l’account Audience Manager dell’organizzazione.

### Quali modifiche risultano in Audience Manager?

Due destinazioni [!DNL Search, Social, & Commerce] diventano disponibili per l&#39;organizzazione in Audience Manager:

* **[!UICONTROL Adobe Media Optimizer (HTTP)]**
* **[!UICONTROL Adobe Media Optimizer Batch Destination]**

## Sincronizzazione dati

L’importazione iniziale richiede circa 24 ore. Dopo l’importazione iniziale, i dati vengono sincronizzati in tempo reale, con un ritardo di uno o due secondi.

I dati di iscrizione al segmento vengono inviati solo dopo che si è verificato uno dei seguenti eventi:

* (Inserzionisti con DSP):

   * Il segmento è destinato a un annuncio visivo Adobe Advertising.

   * Il segmento viene aggiunto al batch [!DNL Adobe AdCloud Cross-Channel] e alle destinazioni in tempo reale nell&#39;interfaccia utente di Audience Manager.

* (Inserzionisti con [!DNL Search, Social, & Commerce]):

   * Il segmento è indicato come destinazione in un annuncio di ricerca Adobe Advertising.

   * Il segmento viene aggiunto al batch [!DNL Adobe Media Optimizer] e alle destinazioni HTTP nell&#39;interfaccia utente di Audience Manager.

<!-- Is membership data/whatever available in Creative? If so, does it show the same as DSP? -->

### Sincronizzazione dei dati in DSP

DSP sincronizza automaticamente i dati utilizzando [!DNL Adobe Experience Cloud Identity (ECID) Service]. Durante la sincronizzazione, [!DNL ECID Service] chiama Adobe Advertising in [!DNL cm.everesttech.net]. Poiché Adobe Advertising è un dominio fidato, le sincronizzazioni ID hanno luogo dalle pagine padre invece che all’interno degli iframe di pubblicazione di destinazione, come fanno con la maggior parte dei partner di attivazione di terze parti. Audience Manager identifica gli utenti univoci in base agli ID dispositivo, utilizzando [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/reference/ids-in-aam), chiamato anche [!DNL Device ID].

<!--
![Synchronization of [!DNL Adobe] audiences in DSP](/help/integrations/assets/audience-manager-sync.png)
-->

### Sincronizzazione dei dati con Search, Social e Commerce

Search, Social e Commerce sincronizzano automaticamente i dati utilizzando [!DNL Adobe Experience Cloud Identity (ECID) Service]. Durante la sincronizzazione, [!DNL ECID Service] chiama Adobe Advertising in [!DNL cm.everesttech.net], che è un dominio trusted che appartiene ad Adobe Advertising. Audience Manager identifica gli utenti univoci in base agli ID dispositivo, utilizzando [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/reference/ids-in-aam), chiamato anche [!DNL Device ID].

## Dove trovare i segmenti sincronizzati

### In DSP

DSP organizza i nomi dei segmenti in base alla tassonomia di Audience Manager e include i conteggi di appartenenza ai segmenti corrispondenti in:

* [Impostazioni posizionamento](/help/dsp/campaign-management/placements/placement-settings.md#audience-targeting): nella scheda [!UICONTROL Adobe Segments] della sezione [!UICONTROL Audience Targeting].

* In [impostazioni pubblico](/help/dsp/audiences/audience-settings.md): nella scheda [!UICONTROL Adobe Segments].

### In Advertising Creative

In [!DNL Creative], i segmenti sono disponibili nelle impostazioni esperienza per i nodi di destinazione.

### In [!DNL Advertising Search, Social, & Commerce]

In [!DNL Search, Social, & Commerce], i segmenti sono disponibili quando si crea un pubblico [!DNL Google] utilizzando [!UICONTROL Data Source] &quot;[!UICONTROL Adobe Audience]&quot; da [!UICONTROL Campaigns] > [!UICONTROL Audiences] > [!UICONTROL Library].

Per ogni pubblico di [!DNL Google] creato, [!DNL Google] fornisce la dimensione del pubblico.

>[!MORELIKETHIS]
>
>* [Integrazioni Adobe Advertising con Adobe Audience Manager](/help/integrations/audience-manager/overview.md)
