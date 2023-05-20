---
title: '''[!DNL Adobe] [!DNL Audience Analytics] ad Adobe, Clienti di Advertising'
description: Scopri come utilizzare [!DNL Adobe] [!DNL Audience Analytics] per casi d’uso pubblicitari
feature: Integration with Adobe Audience Manager
exl-id: 457d4335-2762-4aab-94b8-12f8a79d109b
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---

# [!DNL Adobe] [!DNL Audience Analytics] ad Adobe Clienti Advertising

[[!DNL Adobe] [!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) è un’integrazione tra Adobe Audience Manager e Adobe Analytics che consente ai clienti Audience Manager di inviare segmenti a [!DNL Analytics] per ottenere informazioni approfondite sull’attività del sito.

I clienti di Adobe Advertising possono trarre vantaggio dall’utilizzo di [!DNL Audience Analytics]. L’integrazione di consente di:

* Invia i dati sull’esposizione di Adobe Advertising direttamente a [!DNL Analytics] per determinare l’impatto dell’attività upper funnel sull’attività downstream del sito.

* Determina i canali di marketing e i punti di ingresso al sito dagli annunci di esposizione del funnel superiore.

* Livellare l’integrazione con [!DNL Analytics for Advertising] per incorporare segmenti demografici di terze parti da [Audience Manager [!DNL Audience Marketplace]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/audience-marketplace/audience-marketplace.html) con [!DNL Analytics for Advertising] per ulteriori informazioni sui profili utente.

   [!DNL Audience Marketplace] fornisce l’accesso a feed di dati di terze parti con modelli di abbonamento &quot;Activation&quot;, che consentono agli acquirenti di inviare dati a una destinazione. Se i dati vengono utilizzati in un [!DNL Analytics] destinazione, quindi le tariffe di attivazione non vengono applicate.

* (Inserzionisti con Advertising DSP) Aggiungi altri segmenti di esposizione per informazioni olistiche sulla gestione del percorso.

   Advertising DSP può inviare i dati di esposizione ad Audience Manager come segnali actionable attraverso l&#39;implementazione di Adobe Experience Platform o Audience Manager impression-tracking pixel. Inoltro degli stessi dati a [!DNL Analytics] consente l’analisi avanzata dei dati. Consulta &quot;[Panoramica dell’integrazione dei dati Adobe Advertising Media con Adobe Audience Manager](/help/integrations/audience-manager/media-data-integration/overview.md)&quot; per ulteriori informazioni.

Per ulteriori informazioni su [!DNL Audience Analytics], inclusi i relativi prerequisiti e flusso di lavoro, consulta &quot;[Panoramica Audience Analytics](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html).&quot;

## Esempi di utilizzo [!DNL Audience Analytics] Dati con dati pubblicitari Adobe

Di seguito sono riportati alcuni esempi di come utilizzare i dati combinati in [!DNL Analytics] [!DNL Analysis Workspace].

### Scopri l’impatto dell’attività upper funnel sull’attività downstream

Utilizza i segmenti di esposizione di Audience Manager per vedere l’impatto dell’attività del sito funnel superiore sull’attività del sito a valle. Includi Adobe Advertising o ID macro di terze parti nei pixel di tracciamento per monitorare l’impatto su un livello dettagliato, dal livello della campagna a quello del sito su cui l’utente è stato esposto.

Vantaggi principali:

* Tracciare l’esposizione in base ai tipi di funnel/annunci e all’utilizzo [!DNL Audience Analytics] per determinare i tassi di ingresso e la sovrapposizione con la fase successiva del percorso di clienti.

* Determina l’impatto dell’attività upper funnel sull’attività downstream del sito.

* Connetti [!DNL Analytics for Advertising]<!-- which doesn't include the last exposure event --> e [!DNL Audience Analytics] dati <!-- (which includes the user's last exposure event) --> per determinare un percorso olistico al sito.

Di seguito sono riportati alcuni esempi di report che è possibile creare in [!DNL Analysis Workspace].

![Scopri l’impatto dell’attività upper funnel sull’attività downstream del sito](/help/integrations/assets/audience-analytics-upper-funnel-exposure.png)

### Utilizzare [!DNL Audience Analytics] Dati di segmenti di terze parti per l’analisi del profilo utente

Utilizza segmenti di Audienci Manager di terze parti per un’analisi più completa del modo in cui gli utenti interagiscono con il tuo sito. Puoi utilizzare le informazioni per determinare nuovi tipi di pubblico di terze parti per i quali attivare i contenuti multimediali, in base al modo in cui i profili dei segmenti di terze parti interagiscono con gli indicatori di prestazioni chiave per i siti delle campagne multimediali.

>[!TIP]
> Utilizza l’Audience Manager `Audiences ID` e `Audiences Name` dimensioni in [!DNL Analytics], come qualsiasi altra dimensione che [!DNL Analytics] raccoglie.

Di seguito sono riportati alcuni esempi di report che è possibile creare in [!DNL Analysis Workspace].

![Utilizzo di segmenti di terze parti per arricchire l’analisi del profilo utente](/help/integrations/assets/audience-analytics-third-party-report.png)

>[!MORELIKETHIS]
>
>* [Integrazioni di Adobe Advertising con Adobe Audience Manager](/help/integrations/audience-manager/overview.md)

