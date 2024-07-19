---
title: '[!DNL Adobe] [!DNL Audience Analytics] per Adobe Advertising Clienti'
description: Scopri come utilizzare  [!DNL Adobe] [!DNL Audience Analytics] per i casi d'uso pubblicitari
feature: Integration with Adobe Audience Manager
exl-id: 457d4335-2762-4aab-94b8-12f8a79d109b
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# [!DNL Adobe] [!DNL Audience Analytics] per Adobi Advertising di clienti

[[!DNL Adobe] [!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) è un&#39;integrazione tra Adobe Audience Manager e Adobe Analytics che consente ai clienti Audience Manager di inviare segmenti a [!DNL Analytics] per ottenere informazioni approfondite sull&#39;attività del sito.

I clienti Adobe Advertising possono trarre vantaggio utilizzando [!DNL Audience Analytics]. L’integrazione di consente di:

* Invia i dati di esposizione degli Adobi Advertising direttamente a [!DNL Analytics] per determinare l&#39;impatto dell&#39;attività del funnel superiore sull&#39;attività del sito a valle.

* Determina i canali di marketing e i punti di ingresso al sito dagli annunci di esposizione del funnel superiore.

* Crea un livello di integrazione con [!DNL Analytics for Advertising] per incorporare segmenti demografici di terze parti da [Audience Manager [!DNL Audience Marketplace]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/audience-marketplace/audience-marketplace.html) con dati di [!DNL Analytics for Advertising] per ulteriori informazioni sui profili utente.

  [!DNL Audience Marketplace] fornisce l&#39;accesso ai feed di dati di terze parti con modelli di abbonamento &quot;Activation&quot;, che consentono agli acquirenti di inviare dati a una destinazione. Se i dati vengono utilizzati all&#39;interno di una destinazione [!DNL Analytics], le tariffe di attivazione non vengono applicate.

* (Inserzionisti con Advertising DSP) Aggiungi altri segmenti di esposizione per informazioni olistiche sulla gestione dei percorsi.

  Advertising DSP può inviare i dati di esposizione ad Audience Manager come segnali actionable tramite l’implementazione di pixel di tracciamento delle impression Adobe Experience Platform o Audience Manager. L&#39;inoltro degli stessi dati a [!DNL Analytics] consente l&#39;analisi avanzata dei dati. Per ulteriori informazioni, vedere &quot;[Panoramica sull&#39;integrazione dei dati multimediali Adobe Advertising con Adobe Audience Manager](/help/integrations/audience-manager/media-data-integration/overview.md)&quot;.

Per ulteriori informazioni su [!DNL Audience Analytics], inclusi i prerequisiti e il flusso di lavoro, vedere &quot;[Panoramica Audience Analytics](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html)&quot;.

## Esempi di come utilizzare i dati di [!DNL Audience Analytics] con i dati Adobe Advertising

Di seguito sono riportati alcuni esempi di utilizzo dei dati combinati in [!DNL Analytics] [!DNL Analysis Workspace].

### Scopri l’impatto dell’attività upper funnel sull’attività downstream

Utilizza i segmenti di esposizione di Audience Manager per vedere l’impatto dell’attività del sito funnel superiore sull’attività del sito a valle. Includi ID macro di Adobe Advertising o di terze parti nei pixel di tracciamento per monitorare l’impatto su un livello dettagliato, dal livello della campagna a quello del sito su cui l’utente è stato esposto.

Vantaggi principali:

* Monitora l&#39;esposizione in base ai tipi di funnel/annunci e utilizza [!DNL Audience Analytics] per determinare le percentuali di ingresso e la sovrapposizione con la fase successiva del percorso di clienti.

* Determina l’impatto dell’attività upper funnel sull’attività downstream del sito.

* Connettere i dati [!DNL Analytics for Advertising]<!-- which doesn't include the last exposure event --> e [!DNL Audience Analytics] <!-- (which includes the user's last exposure event) --> per determinare un percorso olistico al sito.

Di seguito sono riportati alcuni esempi di report che è possibile creare in [!DNL Analysis Workspace].

![Scopri l&#39;impatto dell&#39;attività upper funnel sull&#39;attività downstream del sito](/help/integrations/assets/audience-analytics-upper-funnel-exposure.png)

### Usa i dati dei segmenti di terze parti [!DNL Audience Analytics] per l&#39;analisi del profilo utente

Utilizza segmenti di Audienci Manager di terze parti per un’analisi più completa del modo in cui gli utenti interagiscono con il tuo sito. Puoi utilizzare le informazioni per determinare nuovi tipi di pubblico di terze parti per i quali attivare i contenuti multimediali, in base al modo in cui i profili dei segmenti di terze parti interagiscono con gli indicatori di prestazioni chiave per i siti delle campagne multimediali.

>[!TIP]
> Utilizzare le dimensioni Audience Manager `Audiences ID` e `Audiences Name` in [!DNL Analytics], come qualsiasi altra dimensione raccolta da [!DNL Analytics].

Di seguito sono riportati alcuni esempi di report che è possibile creare in [!DNL Analysis Workspace].

![Utilizzo di segmenti di terze parti per arricchire l&#39;analisi del profilo utente](/help/integrations/assets/audience-analytics-third-party-report.png)

>[!MORELIKETHIS]
>
>* [Integrazioni Adobe Advertising con Adobe Audience Manager](/help/integrations/audience-manager/overview.md)
