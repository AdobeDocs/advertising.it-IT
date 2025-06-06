---
title: Panoramica dell’invio dei dati sull’esposizione ai contenuti multimediali dell’DSP a Adobe Audience Manager
description: Scopri come utilizzare i pixel evento di Audience Manager per acquisire dati a livello di impression e di clic dalle campagne Advertising DSP
feature: Integration with Adobe Audience Manager
exl-id: c299cdf0-a83e-4026-8b8b-22ce08af0cc4
source-git-commit: c204955ec48826d00a5f78e5be4849f53d09e224
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 0%

---

# Panoramica dell’invio dei dati sull’esposizione ai contenuti multimediali dell’DSP a Adobe Audience Manager

*Inserzionisti con solo Advertising DSP*

*Inserzionisti con una sola integrazione Adobe Advertising-Adobe Audience Manager*

I clienti di Advertising DSP con Adobe Audience Manager possono utilizzare pixel evento di Audience Manager per acquisire dati a livello di impression e di clic dalle campagne DSP. I pixel dell’evento inviano i dati all’Audience Manager come segnali utilizzabili. Questi segnali consentono diversi casi di utilizzo dell’DSP, ad esempio segmentazione più avanzata, gestione della frequenza, analisi di marketing e informazioni sul reporting.

L&#39;DSP non ti fa pagare per inviare questi segnali agli Audienci Manager. Tuttavia, in base al tuo contratto di Audienci Manager Audience Manager, paghi i costi standard di acquisizione in base alle chiamate al server. Audience Manager rimuove gli eventi duplicati tracciati in due modi diversi, in modo che ogni evento venga caricato una sola volta.

>[!NOTE]
>
> Audience Manager supporta inoltre l’acquisizione di dati da file di registro di ad server, offrendo meno flessibilità. Tale processo non è trattato in questa documentazione.

## Vantaggi principali

* I dati della campagna DSP fluiscono in Audience Manager in tempo reale e possono essere utilizzati per creare caratteristiche basate su regole da utilizzare per definire i segmenti.

* I segmenti sono disponibili per il targeting immediatamente dopo la qualificazione delle caratteristiche dell’utente e dei segmenti, a supporto delle attività di targeting in tempo reale.

* Puoi sfruttare i dati della campagna per casi d’uso quali il limite di frequenza tra i creativi, il retargeting degli utenti che sono stati esposti a campagne precedenti e l’analisi del comportamento del sito a valle e dei punti di ingresso.

* I dati aggregati forniscono una visualizzazione unificata delle prestazioni della campagna, consentono di identificare percorsi di conversione personalizzati e possono essere utilizzati per migliorare la sequenza di eventi che portano a conversioni tramite l&#39;Audience Manager [!DNL Audience Optimization Reports] o un&#39;integrazione [[!DNL Audience Analytics] con Adobe Analytics](/help/integrations/audience-manager/audience-analytics.md).

## Tracciamento dei dati

I pixel dell’evento di impression e clic dell’Audience Manager sono basati su cookie. I pixel non acquisiscono gli eventi che si verificano in ambienti senza cookie, ad esempio app mobili e TV connessa (CTV).<!-- 6/24: CTV inventory isn't clickable, and impression tracking would be lost when we convert users from IP to cookies. -->

### Pixel di tracciamento dell&#39;impression

Audience Manager tiene traccia dei dati di impression per un annuncio quando alleghi all’annuncio un pixel trasparente per il tracciamento degli eventi di 1xl-pixel. Il pixel dell’evento viene caricato ogni volta che l’annuncio viene servito a un utente e caricato dal browser web. Il pixel viene caricato da un sottodominio specifico del client di [`demdex.net`](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html?lang=it), che è un dominio legacy ad Audience Manager e contiene parametri come coppie chiave-valore. La chiamata dell&#39;evento raccoglie i dati sulle impression e di conversione e li invia ai server di raccolta dati di Audience Manager.

### Pixel tracciamento clic

L’Audience Manager tiene traccia dei clic in modo simile alle impression, con la differenza che non carica il pixel dell’evento trasparente ogni volta che l’annuncio viene distribuito. Piuttosto, i dati di clic vengono tracciati nell’URL di click-through dell’annuncio. L&#39;annuncio punta a un sottodominio specifico del client di [`demdex.net`](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html?lang=it), che è un dominio legacy ad Audience Manager, per l&#39;elaborazione da parte dei server di raccolta dati Audience Manager. Il server reindirizza quindi l’utente alla pagina di destinazione prevista. L’URL contiene parametri come coppie chiave-valore.

>[!NOTE]
>
>Se la tua organizzazione utilizza il tracciamento di [!DNL Analytics], potrebbe non essere necessario il tracciamento dei clic di Audience Manager. Adobe Analytics acquisisce i segnali di clic e può inviarli all&#39;Audience Manager tramite [inoltro lato server](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html?lang=it).

>[!MORELIKETHIS]
>
>* [Raccogli dati di clic e impression dalle campagne Advertising DSP](collect.md)
>* [Casi d&#39;uso](use-cases.md)
