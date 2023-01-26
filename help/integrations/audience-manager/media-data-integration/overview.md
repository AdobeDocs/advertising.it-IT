---
title: Panoramica sull’invio DSP dati di esposizione a contenuti multimediali a Adobe Audience Manager
description: Scopri come utilizzare i pixel dell’evento Audience Manager per acquisire dati a livello di impression e di clic dalle campagne Advertising DSP
feature: Integration with Adobe Audience Manager
exl-id: 916b7deb-511e-4fbf-96d9-b274a48dc748
source-git-commit: 1c13874967ec4ad264e5fa6a5e0dfeb6120f53cc
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---

# Panoramica sull’invio DSP dati di esposizione a contenuti multimediali a Adobe Audience Manager

*Advertising DSP solo*

*Inserzionisti con una sola integrazione Advertising-Adobe Audience Manager di Adobe*

I clienti Advertising DSP con Adobe Audience Manager possono utilizzare pixel evento Audienci Manager per acquisire dati a livello di impression e dati a livello di clic da campagne DSP. I pixel dell’evento inviano i dati come segnali actionable all’Audience Manager. Questi segnali consentono diversi casi di utilizzo DSP, ad esempio segmentazione più avanzata, gestione delle frequenze, analisi di marketing e informazioni sul reporting.

DSP non vi carica per inviare questi segnali ad Audience Manager. Tuttavia, paghi i costi standard di acquisizione di Audienci Manager in base alle chiamate al server, in base al contratto di Audience Manager. Audience Manager rimuove gli eventi duplicati tracciati in due modi diversi, in modo che ogni evento venga caricato una sola volta.

>[!NOTE]
>
> Audience Manager supporta anche l’acquisizione di dati dai file di registro di ad server, che offre una flessibilità inferiore. Questo processo non è trattato in questa documentazione.

## Vantaggi principali

* I dati della campagna DSP fluiscono in Audience Manager in tempo reale ed è possibile utilizzarli per creare caratteristiche basate su regole da utilizzare per definire i segmenti.

* I segmenti sono disponibili per il targeting immediatamente dopo la qualifica di caratteristiche utente e segmenti, rafforzando le attività di targeting in tempo reale.

* Puoi sfruttare i dati della campagna per casi d’uso quali il limite di frequenza tra i creativi, il retargeting degli utenti esposti a campagne precedenti e l’analisi del comportamento e dei punti di ingresso del sito a valle.

* I dati aggregati forniscono una visualizzazione unificata delle prestazioni della campagna, consentono di identificare percorsi di conversione personalizzati e possono essere utilizzati per migliorare la sequenza di eventi che portano alle conversioni tramite Audience Manager [!DNL Audience Optimization Reports] o attraverso [[!DNL Audience Analytics] Integrazione con Adobe Analytics](/help/integrations/audience-manager/audience-analytics.md).

## Tracciamento dei dati

L’impression Audience Manager e i pixel dell’evento clic sono basati su cookie. I pixel non acquisiscono gli eventi che si verificano in ambienti senza cookie, come le app mobili e la TV connessa (CTV).

### Pixel di tracciamento delle impression

Audience Manager traccia i dati sulle impression per un annuncio quando si collega all&#39;annuncio un pixel di tracciamento eventi trasparente con pixel 1xl-pixel. Il pixel dell’evento viene caricato ogni volta che l’annuncio viene servito a un utente e caricato dal browser web. Il pixel viene caricato da un sottodominio specifico del client di [`demdex.net`](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html), che è un dominio legacy, ad Audience Manager, e contiene parametri come coppie chiave-valore. La chiamata dell’evento raccoglie i dati di impression e conversione e li invia ai server di raccolta dati di Audience Manager.

### Pixel di tracciamento dei clic

Audience Manager tiene traccia dei clic in modo simile alle impression, con la differenza che non carica il pixel evento trasparente ogni volta che l’annuncio viene servito. I dati dei clic vengono invece tracciati nell’URL di click-through dell’annuncio. L’annuncio punta a un sottodominio specifico del client di [`demdex.net`](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html), un dominio legacy, ad Audience Manager, per l’elaborazione da parte dei server di raccolta dati di Audience Manager. Il server reindirizza quindi l’utente alla pagina di destinazione prevista. L’URL contiene parametri come coppie chiave-valore.

>[!NOTE]
>
>Se l&#39;organizzazione utilizza [!DNL Analytics] tracciamento, potrebbe non essere necessario un Audience Manager di tracciamento dei clic. Adobe Analytics acquisisce i segnali di clic e può inviarli ad Audience Manager attraverso [inoltro lato server](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html).

>[!MORELIKETHIS]
>
>* [Raccogliere dati di clic e impression da campagne pubblicitarie DSP](collect.md)
>* [Casi d&#39;uso](use-cases.md)

