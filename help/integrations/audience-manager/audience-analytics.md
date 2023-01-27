---
title: '''[!DNL Adobe] [!DNL Audience Analytics] ad Adobe i clienti della pubblicità'
description: Scopri come utilizzare [!DNL Adobe] [!DNL Audience Analytics] per i casi di utilizzo pubblicitario
feature: Integration with Adobe Audience Manager
exl-id: 457d4335-2762-4aab-94b8-12f8a79d109b
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---

# [!DNL Adobe] [!DNL Audience Analytics] ad Adobe i clienti della pubblicità

[[!DNL Adobe] [!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) è un’integrazione tra Adobe Audience Manager e Adobe Analytics che consente ai clienti di Audience Manager di inviare segmenti a [!DNL Analytics] per informazioni approfondite sull’attività del sito.

I clienti Adobe Advertising possono trarre vantaggio dall’utilizzo di [!DNL Audience Analytics]. L’integrazione consente di:

* Invia i dati dell&#39;esposizione pubblicitaria di Adobe direttamente a [!DNL Analytics] determinare l’impatto dell’attività di imbuto superiore sull’attività del sito a valle.

* Determina i canali di marketing e i punti di ingresso del sito dagli annunci di esposizione funnel superiori.

* Crea un livello di integrazione con [!DNL Analytics for Advertising] incorporare segmenti demografici di terze parti [Audience Manager [!DNL Audience Marketplace]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/audience-marketplace/audience-marketplace.html) con [!DNL Analytics for Advertising] per ulteriori informazioni sui profili utente.

   [!DNL Audience Marketplace] fornisce l’accesso ai feed di dati di terze parti con modelli di abbonamento &quot;Activation&quot;, che consentono agli acquirenti di inviare dati a una destinazione. Se i dati vengono utilizzati in un [!DNL Analytics] destinazione, quindi le tariffe di attivazione non vengono applicate.

* (Inserzionisti con Advertising DSP) Aggiungi ulteriori segmenti di esposizione per informazioni sulla gestione dei percorsi olistici.

   La DSP pubblicitaria può inviare dati di esposizione ad Audienci Manager come segnali actionable attraverso l&#39;implementazione di Adobe Experience Platform o di pixel Audienci Manager di tracciamento delle impression. Inoltro degli stessi dati a [!DNL Analytics] abilita l’analisi avanzata dei dati. Vedere &quot;[Panoramica dell’integrazione dei dati di Adobe Advertising Media con Adobe Audience Manager](/help/integrations/audience-manager/media-data-integration/overview.md)&quot; per ulteriori informazioni.

Per ulteriori informazioni [!DNL Audience Analytics], compresi i prerequisiti e il flusso di lavoro, vedi &quot;[Panoramica di Audience Analytics](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html).&quot;

## Esempi di utilizzo [!DNL Audience Analytics] Dati con i dati pubblicitari di Adobe

Di seguito sono riportati alcuni esempi di utilizzo dei dati combinati all’interno di [!DNL Analytics] [!DNL Analysis Workspace].

### Vedi l&#39;impatto dell&#39;attività dell&#39;imbuto superiore sull&#39;attività a valle

Utilizza i segmenti di esposizione di Audience Manager per vedere l&#39;impatto dell&#39;attività superiore del sito funnel sull&#39;attività del sito a valle. Includi ID di pubblicità di Adobe o macro di terze parti nei pixel di tracciamento per tracciare l&#39;impatto su un livello dettagliato, dal livello della campagna al livello del sito sul quale l&#39;utente è stato esposto.

Vantaggi principali:

* Esposizione al binario per tipo di funnel/annuncio e uso [!DNL Audience Analytics] per determinare i tassi di ingresso e la sovrapposizione con la fase successiva del percorso cliente.

* Determinare l’impatto dell’attività di imbuto superiore sull’attività del sito a valle.

* Connetti [!DNL Analytics for Advertising]<!-- which doesn't include the last exposure event --> e [!DNL Audience Analytics] dati <!-- (which includes the user's last exposure event) --> per determinare un percorso olistico sul sito.

Di seguito sono riportati alcuni esempi di rapporti che puoi creare in [!DNL Analysis Workspace].

![Vedere l&#39;impatto dell&#39;attività di funnel superiore sull&#39;attività di sito a valle](/help/integrations/assets/audience-analytics-upper-funnel-exposure.png)

### Utilizzo [!DNL Audience Analytics] Dati dei segmenti di terze parti per l’analisi dei profili utente

Utilizza segmenti di Audience Manager di terze parti per un’analisi più approfondita del modo in cui gli utenti interagiscono con il tuo sito. Puoi utilizzare le informazioni per determinare nuovi tipi di pubblico di terze parti per i quali attivare i contenuti multimediali, in base al modo in cui i profili dei segmenti di terze parti interagiscono con indicatori di prestazioni chiave per i siti delle campagne multimediali.

>[!TIP]
> Utilizza l’Audience Manager `Audiences ID` e `Audiences Name` dimensioni [!DNL Analytics], come qualsiasi altra dimensione [!DNL Analytics] raccoglie.

Di seguito sono riportati alcuni esempi di rapporti che puoi creare in [!DNL Analysis Workspace].

![Utilizzo di segmenti di terze parti per arricchire l’analisi del profilo utente](/help/integrations/assets/audience-analytics-third-party-report.png)

>[!MORELIKETHIS]
>
>* [Integrazioni pubblicitarie di Adobe con Adobe Audience Manager](/help/integrations/audience-manager/overview.md)

