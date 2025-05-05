---
title: Perché i dati del canale possono variare tra Adobe Advertising e  [!DNL Marketing Channels]
description: Scopri perché i dati dei canali tracciati dall’AMO ID possono variare rispetto ai dati dei canali tracciati da [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 72e3aa1e-85ed-485a-b93f-5e67dd0140ce
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 0%

---

# Perché i dati del canale possono variare tra Adobe Advertising e [!DNL Marketing Channels]

*Inserzionisti con una sola integrazione Adobe Advertising-Adobe Analytics*

Una domanda comune da parte degli utenti che vengono a conoscenza dell’integrazione dei set di dati Adobe Advertising e [!DNL Marketing Channels] è &quot;Cosa causa la varianza nei dati tra AMO ID e [!DNL Marketing Channels]?&quot; Oppure, a volte, &quot;Perché i dati non funzionano? Ho bisogno che tutte le metriche corrispondano tra i rapporti.&quot; Fortunatamente, le discrepanze non indicano che i dati sono &quot;interrotti&quot;, e le discrepanze sono previste e anche desiderate. Vediamo perché l’integrazione è stata progettata in questo modo.

I due set di dati hanno casi d’uso principali diversi:

* [!DNL Marketing Channels]: il caso d&#39;uso principale per [!DNL Marketing Channels] consiste nel confrontare i dati su più canali con un modello di attribuzione comune. Gli analisti possono utilizzare la dimensione [!UICONTROL Marketing Channel] per ottenere informazioni più approfondite sul modo in cui i canali interagiscono tra loro. Questa informazione può aiutare ad alimentare le decisioni a livello macro su come investire in ciascun canale e può portare a informazioni su come i visitatori di ciascun canale interagiscono con il sito web.

  La dimensione [!DNL Analytics] [!UICONTROL Marketing Channel] è pertanto configurata per acquisire e tenere traccia di tutti i canali. [!DNL Marketing Channels] può anche essere configurato per acquisire view-through e click-through di Advertising DSP, e lo fa in relazione agli altri canali di marketing.

* AMO ID Adobe Advertising: il caso d’uso principale dei dati AMO ID Adobe Advertising è quello di alimentare gli algoritmi di offerta avanzati basati su [!DNL Adobe Sensei]. Gli algoritmi eseguono automaticamente migliaia di decisioni di offerta a livello micro ogni giorno per massimizzare la spesa pubblicitaria e raggiungere gli obiettivi della campagna [!DNL DSP] o del portfolio [!DNL Search, Social, & Commerce]. Maggiore è il numero di dati di conversione a cui gli algoritmi possono collegare le campagne, migliore è il numero di decisioni di offerta che gli algoritmi possono prendere.

  Per raccogliere questi dati, l’integrazione di [!DNL Analytics for Advertising] trasmette degli AMO ID non elaborati che possono essere tradotti come codici di tracciamento click-through e view-through nella dimensione AMO ID di Adobe Analytics, memorizzata come variabile personalizzata (eVar) o come variabile riservata (rVar). I click-through per altri canali non sono impostati nella dimensione AMO ID, pertanto la dimensione AMO ID non è in grado di tenere traccia dell’ingresso da questi altri canali. Il risultato è che l’AMO ID persiste attraverso [!DNL Marketing Channels] punti di ingresso.

Per ulteriori informazioni sulle possibili varianze di dati tra dati tracciati da Adobe Advertising e dati tracciati da [!DNL Analytics], vedere &quot;[Varianze di dati previste tra [!DNL Analytics] e Adobe Advertising](../data-variances.md).&quot;

>[!MORELIKETHIS]
>
>* [Varianze di dati previste tra [!DNL Analytics] e Adobe Advertising](/help/integrations/analytics/data-variances.md)
>* [Nozioni di base di [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Utilizzo degli ID Adobe Advertising per la creazione [!DNL Marketing Channels] Regole di elaborazione](mc-ids.md)
>* [Utilizzo di [!DNL Analytics Marketing Channels] con dati Adobe Advertising](mc-ac-data.md)
>* [Video: utilizzo di [!DNL Marketing Channels] per Adobe Advertising di reporting](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html?lang=it)
