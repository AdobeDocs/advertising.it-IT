---
title: '[!DNL Adobe] [!DNL Audience Analytics]  per clienti Adobe Advertising'
description: Scopri come utilizzare  [!DNL Adobe] [!DNL Audience Analytics] per i casi d'uso pubblicitari
feature: Integration with Adobe Audience Manager
exl-id: 457d4335-2762-4aab-94b8-12f8a79d109b
source-git-commit: d6416dae58543e1287b7af7df44eada4be023731
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# [!DNL Adobe] [!DNL Audience Analytics] per i clienti Adobe Advertising

[[!DNL Adobe] [!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html?lang=it) è un&#39;integrazione tra Adobe Audience Manager e Adobe Analytics che consente ai clienti Audience Manager di inviare segmenti a [!DNL Analytics] per ottenere informazioni approfondite sull&#39;attività del sito.

I clienti Adobe Advertising possono trarre vantaggio dall&#39;utilizzo di [!DNL Audience Analytics]. L’integrazione di consente di:

* Invia i dati di esposizione di Adobe Advertising direttamente a [!DNL Analytics] per determinare l&#39;impatto dell&#39;attività superiore di funnel sull&#39;attività del sito a valle.

* Determina i canali di marketing e i punti di ingresso al sito dagli annunci di esposizione funnel superiori.

* Crea un livello di integrazione con [!DNL Analytics for Advertising] per incorporare segmenti demografici di terze parti da [Audience Manager [!DNL Audience Marketplace]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/audience-marketplace/audience-marketplace.html?lang=it) con dati di [!DNL Analytics for Advertising] per ulteriori informazioni sui profili utente.

  [!DNL Audience Marketplace] fornisce l&#39;accesso ai feed di dati di terze parti con modelli di abbonamento &quot;Activation&quot;, che consentono agli acquirenti di inviare dati a una destinazione. Se i dati vengono utilizzati all&#39;interno di una destinazione [!DNL Analytics], le tariffe di attivazione non vengono applicate.

* (Inserzionisti con Advertising DSP) Aggiungi altri segmenti di esposizione per informazioni olistiche sulla gestione dei percorsi.

  Advertising DSP può inviare i dati di esposizione ad Audience Manager come segnali utilizzabili tramite l’implementazione di pixel di tracciamento delle impression di Adobe Experience Platform o Audience Manager. L&#39;inoltro degli stessi dati a [!DNL Analytics] consente l&#39;analisi avanzata dei dati. Per ulteriori informazioni, vedere &quot;[Panoramica dell&#39;invio dei dati di esposizione dei supporti DSP a Adobe Audience Manager](/help/integrations/audience-manager/media-data-integration/overview.md)&quot;.

Per ulteriori informazioni su [!DNL Audience Analytics], inclusi i prerequisiti e il flusso di lavoro, vedere &quot;[Panoramica di Audience Analytics](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html?lang=it)&quot;.

## Esempi di come utilizzare i dati di [!DNL Audience Analytics] con i dati di Adobe Advertising

Di seguito sono riportati alcuni esempi di utilizzo dei dati combinati in [!DNL Analytics] [!DNL Analysis Workspace].

### Scopri l’impatto dell’attività upper funnel sull’attività downstream

Utilizza i segmenti di esposizione di Audience Manager per visualizzare l’impatto dell’attività del sito superiore di funnel sull’attività del sito a valle. Includi ID macro di Adobe Advertising o di terze parti nei pixel di tracciamento per monitorare l’impatto su un livello dettagliato, dal livello della campagna a quello del sito su cui l’utente è stato esposto.

Vantaggi principali:

* Tenere traccia dell&#39;esposizione per tipi di funnel/annunci e utilizzare [!DNL Audience Analytics] per determinare le percentuali di ingresso e la sovrapposizione con la fase successiva del percorso di clienti.

* Determinare l’impatto dell’attività upper funnel sull’attività downstream del sito.

* Connettere i dati [!DNL Analytics for Advertising]<!-- which doesn't include the last exposure event --> e [!DNL Audience Analytics] per determinare un percorso olistico al sito.

<!-- (which includes the user's last exposure event) -->

Di seguito sono riportati alcuni esempi di report che è possibile creare in [!DNL Analysis Workspace].

![Visualizza l&#39;impatto dell&#39;attività superiore di funnel sull&#39;attività del sito a valle](/help/integrations/assets/audience-analytics-upper-funnel-exposure.png)

### Usa i dati del segmento di terze parti [!DNL Audience Analytics] per l&#39;analisi del profilo utente

Utilizza i segmenti di Audience Manager di terze parti per un’analisi più completa del modo in cui gli utenti interagiscono con il tuo sito. Puoi utilizzare le informazioni per determinare nuovi tipi di pubblico di terze parti per i quali attivare i contenuti multimediali, in base al modo in cui i profili dei segmenti di terze parti interagiscono con gli indicatori di prestazioni chiave per i siti delle campagne multimediali.

>[!TIP]
> Utilizzare le dimensioni Audience Manager `Audiences ID` e `Audiences Name` in [!DNL Analytics], come qualsiasi altra dimensione raccolta da [!DNL Analytics].

Di seguito sono riportati alcuni esempi di report che è possibile creare in [!DNL Analysis Workspace].

![Utilizzo di segmenti di terze parti per arricchire l&#39;analisi del profilo utente](/help/integrations/assets/audience-analytics-third-party-report.png)

>[!MORELIKETHIS]
>
>* [Integrazioni Adobe Advertising con Adobe Audience Manager](/help/integrations/audience-manager/overview.md)
