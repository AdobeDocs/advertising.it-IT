---
title: Perché i dati dei canali possono variare tra la pubblicità Adobe e [!DNL Marketing Channels]
description: Scopri perché i dati dei canali tracciati dall’AMO ID possono variare rispetto ai dati dei canali tracciati da [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 72e3aa1e-85ed-485a-b93f-5e67dd0140ce
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# Perché i dati dei canali possono variare tra la pubblicità Adobe e [!DNL Marketing Channels]

*Inserzionisti con un Adobe di integrazione Advertising-Adobe Analytics Only*

Una domanda comune da parte degli utenti che vengono a conoscenza dell’integrazione dell’Adobe Advertising e [!DNL Marketing Channels] I set di dati sono le cause della varianza nei dati tra l’AMO ID e [!DNL Marketing Channels]?&quot; Oppure, a volte, &quot;Perché i dati non funzionano? Ho bisogno che tutte le metriche corrispondano tra i rapporti.&quot; Fortunatamente, le discrepanze non indicano che i dati sono &quot;interrotti&quot;, e le discrepanze sono previste e anche desiderate. Vediamo perché l’integrazione è stata progettata in questo modo.

I due set di dati hanno casi d’uso principali diversi:

* [!DNL Marketing Channels]: caso di utilizzo principale per [!DNL Marketing Channels] confronta i dati tra più canali con un modello di attribuzione comune. Gli analisti possono utilizzare [!UICONTROL Marketing Channel] per ottenere informazioni più approfondite sul modo in cui i canali interagiscono tra loro. Questa informazione può aiutare ad alimentare le decisioni a livello macro su come investire in ciascun canale e può portare a informazioni su come i visitatori di ciascun canale interagiscono con il sito web.

   Il [!DNL Analytics] [!UICONTROL Marketing Channel] dimension, quindi, è configurato per acquisire e tenere traccia di tutti i canali. [!DNL Marketing Channels] può essere configurato anche per acquisire view-through e click-through di Advertising DSP, e lo fa in relazione agli altri canali di marketing.

* Adobe Advertising AMO ID: il caso d’uso principale dei dati AMO di Adobe Advertising è quello di alimentare il [!DNL Adobe Sensei]algoritmi di offerta basati su. Gli algoritmi prendono automaticamente migliaia di decisioni di offerta a livello micro prese ogni giorno per massimizzare la spesa pubblicitaria e raggiungere gli obiettivi del [!DNL DSP] campagna o [!DNL Search, Social, & Commerce] portfolio. Maggiore è il numero di dati di conversione a cui gli algoritmi possono collegare le campagne, migliore è il numero di decisioni di offerta che gli algoritmi possono prendere.

   Per raccogliere questi dati, [!DNL Analytics for Advertising] L’integrazione passa gli AMO ID non elaborati che possono essere tradotti come codici di tracciamento click-through e view-through nella dimensione AMO ID di Adobe Analytics, memorizzata come variabile personalizzata (eVar) o come variabile riservata (rVar). I click-through per altri canali non sono impostati nella dimensione AMO ID, pertanto la dimensione AMO ID non è in grado di tenere traccia dell’ingresso da questi altri canali. Il risultato è che l’AMO ID persiste attraverso [!DNL Marketing Channels] punti di ingresso.

Per ulteriori informazioni sulle possibili varianze di dati tra i dati tracciati da Adobe Advertising e [!DNL Analytics]-dati tracciati, vedere &quot;[Varianze di dati previste tra [!DNL Analytics] e pubblicità Adobe](../data-variances.md).&quot;

>[!MORELIKETHIS]
>
>* [Varianze di dati previste tra [!DNL Analytics] e pubblicità Adobe](/help/integrations/analytics/data-variances.md)
>* [Nozioni di base di [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Utilizzo degli ID Adobe Advertising per la creazione [!DNL Marketing Channels] Regole di elaborazione](mc-ids.md)
>* [Utilizzo di [!DNL Analytics Marketing Channels] con i dati pubblicitari di Adobe](mc-ac-data.md)
>* [Video: Utilizzo [!DNL Marketing Channels] ad Adobe Advertising Reporting](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)

