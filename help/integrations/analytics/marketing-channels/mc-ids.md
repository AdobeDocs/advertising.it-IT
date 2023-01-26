---
title: Utilizzo degli ID pubblicitari di Adobe per creare [!DNL Marketing Channels] Regole
description: Scopri come utilizzare Adobe Advertising IDs per creare regole di elaborazione per [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 525761b4-607f-4b03-9020-8051009a13c6
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 0%

---

# Utilizzo degli ID pubblicitari di Adobe per creare [!DNL Marketing Channels] Regole di elaborazione

*Inserzionisti con una sola integrazione Advertising-Adobe Analytics di Adobe*

Puoi utilizzare Adobe Advertising ID ([ID AMO e ID EF](../ids.md)) per configurare [!DNL Marketing Channels] regole di elaborazione in Adobe Analytics. Utilizza Adobe Advertising IDs per le regole specifiche delle campagne pubblicitarie Adobi.

## ID AMO nelle regole di elaborazione

L’AMO ID è il codice di tracciamento principale utilizzato per segnalare i dati pubblicitari di Adobe all’interno di [!DNL Analytics]. L’AMO ID è una concatenazione di valori dinamici gestiti da Adobe per fornire rapporti granulari all’interno di [!DNL Analytics]. Viene memorizzato in un [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) o dimensione rVar (AMO ID). L’AMO ID può essere impostato in [!DNL Analytics] in due modi:

* Tracciamento Click-through: Adobe Advertising imposta il `s_kwcid` parametro della stringa di interrogazione in un collegamento e [!DNL Analytics] rileva il parametro dall’URL della pagina di destinazione quando si verifica un click-through.
* Tracking view-through ([!DNL DSP] Solo): Il servizio Ultimo evento rileva una visualizzazione nel lato server e invia l’ID AMO a [!DNL Analytics]. In questo caso, l’URL non contiene un `s_kwcid` parametro .

I valori dinamici all’interno degli AMO ID indicano il canale di marketing monitorato:

* Il prefisso nell’AMO ID può essere utilizzato per identificare il canale di livello principale all’interno di [!DNL Marketing Channels].

* Le frasi di carattere nel corpo dell’AMO ID indicano un tipo di campagna più specifico.

* Il suffisso &quot;vt&quot; è presente per [!DNL DSP] traffico view-through e può essere utilizzato per creare click-through e view-through separati [!DNL DSP] canali.

Il resto dell’AMO ID può essere ignorato.

| ID AMO | Canale | Logica regola |
|--------|---------|--------------------|
| AL! (prefisso) | [!UICONTROL Paid Search] | Inizia con |
| AC! (prefisso) | [!UICONTROL DSP] | Inizia con |
| !g! (corpo) | [!UICONTROL Google Search] | Contiene |
| !s! (corpo) | [!UICONTROL Search Partner] | Contiene |
| !d! (corpo) | [!UICONTROL Display Network] | Contiene |
| !u! (corpo) | [!UICONTROL Smart Shopping Campaign] | Contiene |
| !tv! (corpo) | [!UICONTROL YouTube Video Ad] | Contiene |
| !yts! (corpo) | [!UICONTROL YouTube Search Ad] | Contiene |
| !vp! (corpo) | [!UICONTROL Google Video Partners] | Contiene |
| !vt (suffisso) | [!UICONTROL DSP View-through] | Termina con |

### Esempi di regole di elaborazione che utilizzano l’AMO ID

La [!DNL Marketing Channels] regola di elaborazione per [!UICONTROL Paid Search] il canale potrebbe essere simile al seguente:

![Esempio di [!UICONTROL Paid Search] regola](/help/integrations/assets/a4adc-mc-rule-paidsearch.png)

La [!DNL Marketing Channels] regola di elaborazione per [!UICONTROL YouTube Video Ads] il canale potrebbe essere simile al seguente:

![Esempio di [!UICONTROL YouTube Video Ads] regola](/help/integrations/assets/a4adc-mc-rule-youtube-video.png)

>[!IMPORTANT]
>
> Assicurati di eseguire le regole in ordine di specificità. Se le due regole di cui sopra sono state eseguite in ordine, il [!DNL YouTube] il traffico video e pubblicitario rientra completamente nella [!UICONTROL Paid Search] canale perché l’AMO ID inizia entrambi con &quot;AL!&quot; e contengono &quot;!ytv!&quot;.

## ID EF nelle regole di elaborazione

L’AMO EF ID (EF ID) è il secondo codice di tracciamento utilizzato nel [!DNL Analytics for Advertising] integrazione. Il suo scopo principale è quello di monitorare e trasmettere [!DNL Analytics] dati evento in Adobe Advertising. Ogni volta che si verifica un click-through o una visualizzazione, viene generato un ID EF univoco, anche se è lo stesso annuncio per lo stesso visitatore. L’ID EF non viene utilizzato nel [!DNL Analytics] interfaccia utente per la generazione di rapporti perché in genere supera i valori univoci di 500.000 per limite di variabili in [!DNL Analytics], rendendolo inutilizzabile per i rapporti. Le metriche e i metadati della pubblicità di Adobe non vengono applicati all’ID EF; sono applicati solo all’AMO ID. La granularità aggiunta del tracciamento è necessaria per l’ottimizzazione delle campagne in Adobe Advertising, quindi sono necessari entrambi gli ID.

Anche se la dimensione ID EF non viene utilizzata direttamente in [!DNL Analytics] l’ID EF può essere utile per la creazione di canali di marketing. Il suffisso EF ID indica il canale (visualizzazione o ricerca) e se la visita è stata guidata da un click-through o da una visualizzazione-through. Il carattere di delimitazione nell’ID EF è un punto a due punti anziché il punto esclamativo nell’ID AMO.

| Suffisso ID EF | Canale |
|-------|---------|
| :s | [!UICONTROL Paid Search] |
| :d | [!UICONTROL Display Click-through] |
| :i | [!UICONTROL Display View-through] |

### Esempi di regole di elaborazione che utilizzano l’ID EF

#### Visualizza regola di click-through

Crea un canale di marketing click-through di visualizzazione acquisendo solo i click-through. Poiché l’AMO ID è lo stesso per i click-through e le visualizzazioni-through, questa regola utilizza la variabile EF ID e la variabile `ef_id` parametro della stringa query.

A volte i click-through vengono tracciati attraverso l&#39;URL (impostazione predefinita). In altri casi, i click-through vengono tracciati attraverso il servizio Ultimo evento sul lato server, e pertanto l&#39;URL non contiene il `ef_id` parametro . La regola pertanto verifica le condizioni in cui la variabile ID EF o `ef_id` il parametro della stringa query termina con &quot;:d&quot;. Utilizza il &quot;`Any`&quot; perché desideri attivare questa regola per entrambe le condizioni.

![Esempio di regola di click-through della visualizzazione](/help/integrations/assets/a4adc-mc-rule-display-ct.png)

#### Visualizza regola view-through

Per creare un canale view-through di visualizzazione, creare una regola in cui l’ID EF termina con &quot;:i&quot;. Poiché il visitatore non ha fatto clic sull’annuncio, il tracciamento della visualizzazione tramite non include il `ef_id` o `s_kwcid` nell’URL, quindi la regola richiede una sola condizione.

![Esempio di regola di visualizzazione view-through](/help/integrations/assets/a4adc-mc-rule-display-vt.png)

>[!MORELIKETHIS]
>
>* [Nozioni fondamentali di [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Perché i dati del canale possono variare tra la pubblicità Adobe e [!DNL Marketing Channels]](mc-data-variances.md)
>* [Utilizzo [!DNL Analytics Marketing Channels] con i dati pubblicitari di Adobe](mc-ac-data.md)
>* [Video: Utilizzo [!DNL Marketing Channels] ad Adobe Advertising Reporting](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [ID pubblicitari di Adobe utilizzati da [!DNL Analytics]](/help/integrations/analytics/ids.md)

