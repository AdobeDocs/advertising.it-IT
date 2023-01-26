---
title: Perché i dati del canale possono variare tra la pubblicità Adobe e [!DNL Marketing Channels]
description: Scopri perché i dati del canale tracciati dall’AMO ID possono variare dai dati del canale tracciati da [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 72e3aa1e-85ed-485a-b93f-5e67dd0140ce
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# Perché i dati del canale possono variare tra la pubblicità Adobe e [!DNL Marketing Channels]

*Inserzionisti con una sola integrazione Advertising-Adobe Analytics di Adobe*

Una domanda comune da parte degli utenti che apprendono dell&#39;integrazione della pubblicità Adobe e [!DNL Marketing Channels] set di dati è &quot;Ciò che causa la varianza nei dati tra l’AMO ID e [!DNL Marketing Channels]?&quot; O, a volte, &quot;Perché i dati sono interrotti? Ho bisogno che tutte le metriche corrispondano tra i rapporti.&quot; Fortunatamente, le discrepanze non indicano che i dati sono &quot;interrotti&quot;, e le discrepanze sono attese e anche desiderate. Scopriamo perché l’integrazione è stata progettata in questo modo.

I due set di dati hanno diversi casi d’uso principali:

* [!DNL Marketing Channels]: Il caso d’uso principale per [!DNL Marketing Channels] confronta i dati su più canali con un modello di attribuzione comune. Gli analisti possono utilizzare [!UICONTROL Marketing Channel] per ottenere informazioni più approfondite sul modo in cui i canali interagiscono tra loro. Queste informazioni possono contribuire a favorire le decisioni a livello di macro su come investire in ciascun canale e possono portare a informazioni su come i visitatori di ogni canale interagiscono con il sito web.

   La [!DNL Analytics] [!UICONTROL Marketing Channel] La dimensione , quindi, è configurata per acquisire e monitorare tutti i canali. [!DNL Marketing Channels] può anche essere configurato per acquisire visualizzazioni e click-through di DSP pubblicitaria, e lo fa in relazione agli altri canali di marketing.

* Adobe Advertising AMO ID: Il caso d’uso principale dei dati AMO di Adobe Advertising ID è quello di feed dell’ [!DNL Adobe Sensei]algoritmi di offerta basati su tecnologia. Gli algoritmi prendono automaticamente migliaia di decisioni sulle offerte a livello micro prese quotidianamente per massimizzare la spesa pubblicitaria e raggiungere gli obiettivi [!DNL DSP] o [!DNL Search] portafoglio Maggiore è il numero di dati di conversione a cui gli algoritmi possono collegare le campagne, migliore sarà il numero di decisioni di aggiudicazione.

   Per raccogliere questi dati, [!DNL Analytics for Advertising] l’integrazione passa gli AMO ID non elaborati che possono essere tradotti come codici di tracciamento click-through e view-through nella dimensione AMO ID di Adobe Analytics, che viene memorizzata come variabile personalizzata (eVar) o come variabile riservata (rVar). I click-through per altri canali non sono impostati nella dimensione AMO ID, pertanto la dimensione AMO ID non è in grado di monitorare la voce da questi altri canali. Il risultato è che l’AMO ID persiste [!DNL Marketing Channels] punti di ingresso.

Per ulteriori informazioni sulle possibili varianze di dati tra i dati tracciati da Adobe Advertising e [!DNL Analytics]- dati tracciati, vedi &quot;[Varianze di dati previste tra [!DNL Analytics] e pubblicità Adobe](../data-variances.md).&quot;

>[!MORELIKETHIS]
>
>* [Varianze di dati previste tra [!DNL Analytics] e pubblicità Adobe](/help/integrations/analytics/data-variances.md)
>* [Nozioni fondamentali di [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Utilizzo degli ID pubblicitari di Adobe per creare [!DNL Marketing Channels] Regole di elaborazione](mc-ids.md)
>* [Utilizzo [!DNL Analytics Marketing Channels] con i dati pubblicitari di Adobe](mc-ac-data.md)
>* [Video: Utilizzo [!DNL Marketing Channels] ad Adobe Advertising Reporting](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)

