---
title: Utilizzo degli ID Adobe Advertising per la creazione di  [!DNL Marketing Channels]  regole
description: Scopri come utilizzare gli ID Adobe Advertising per creare regole di elaborazione per  [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 525761b4-607f-4b03-9020-8051009a13c6
source-git-commit: 96a0add168c7fb7a6d80cf1b81ef4b315fbba89f
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 0%

---

# Utilizzo degli ID Adobe Advertising per creare [!DNL Marketing Channels] regole di elaborazione

*Inserzionisti con una sola integrazione Adobe Advertising-Adobe Analytics*

È possibile utilizzare gli ID Adobe Advertising ([AMO ID e EF ID](../ids.md)) per configurare [!DNL Marketing Channels] regole di elaborazione in Adobe Analytics. Utilizza gli ID Adobe Advertising per le regole specifiche delle campagne di Adobe Advertising.

## AMO ID nelle regole di elaborazione

AMO ID è il codice di tracciamento principale utilizzato per segnalare i dati di Adobe Advertising in [!DNL Analytics]. AMO ID è una concatenazione di valori dinamici gestiti da Adobe per fornire rapporti granulari all’interno di [!DNL Analytics]. È memorizzato in una dimensione [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) o rVar (AMO ID). L&#39;AMO ID può essere impostato in [!DNL Analytics] in due modi:

* Tracciamento click-through: l&#39;Adobe Advertising imposta il parametro della stringa di query `s_kwcid` in un collegamento e [!DNL Analytics] lo seleziona dall&#39;URL della pagina di destinazione quando si verifica un click-through.
* Tracciamento view-through ([!DNL DSP] Only): Last Event Service rileva una view-through sul lato server e invia l&#39;AMO ID a [!DNL Analytics]. In questo caso, l&#39;URL non contiene un parametro `s_kwcid`.

I valori dinamici all’interno degli AMO ID indicano il canale di marketing tracciato:

* Il prefisso nell’AMO ID può essere utilizzato per identificare il canale di primo livello all’interno di [!DNL Marketing Channels].

* Le frasi di carattere nel corpo dell’AMO ID indicano un tipo di campagna più specifico.

* Il suffisso &quot;vt&quot; è presente per il traffico view-through [!DNL DSP] e può essere utilizzato per creare canali [!DNL DSP] di click-through e view-through separati.

Il resto dell’AMO ID può essere ignorato.

| [!UICONTROL AMO ID] | Canale | Logica delle regole |
|--------|---------|--------------------|
| !ctv (suffisso) | [!UICONTROL DSP Connected TV View-through] | Termina con |
| !d! (body) | [!UICONTROL Display Network] | Contiene |
| !g! (body) | [!UICONTROL Google Search] | Contiene |
| !s! (body) | [!UICONTROL Search Partner] | Contiene |
| !u! (body) | [!UICONTROL Smart Shopping Campaign] | Contiene |
| !ytv! (body) | [!UICONTROL YouTube Video Ad] | Contiene |
| !yts! (body) | [!UICONTROL YouTube Search Ad] | Contiene |
| !vp! (body) | [!UICONTROL Google Video Partners] | Contiene |
| !vt (suffisso) | [!UICONTROL DSP View-through] | Termina con |
| AL! (prefisso) | [!UICONTROL Paid Search] | Inizia con |
| AC! (prefisso) | [!UICONTROL DSP] | Inizia con |

### Esempi di regole di elaborazione che utilizzano l’AMO ID

La regola di elaborazione [!DNL Marketing Channels] per il canale [!UICONTROL Paid Search] potrebbe essere simile alla seguente:

![Esempio di regola [!UICONTROL Paid Search]](/help/integrations/assets/a4adc-mc-rule-paidsearch.png)

La regola di elaborazione [!DNL Marketing Channels] per il canale [!UICONTROL YouTube Video Ads] potrebbe essere simile alla seguente:

![Esempio di regola [!UICONTROL YouTube Video Ads]](/help/integrations/assets/a4adc-mc-rule-youtube-video.png)

>[!IMPORTANT]
>
> Assicurati di eseguire le regole in ordine di specificità. Se le due regole di cui sopra vengono eseguite in ordine, il traffico dell’annuncio video [!DNL YouTube] rientra nel canale [!UICONTROL Paid Search] perché l’AMO ID inizia entrambe con &quot;AL!&quot; e contengono &quot;!ytv!&quot;.

## ID EF nelle regole di elaborazione

AMO EF ID (EF ID) è il secondo codice di tracciamento utilizzato nell’integrazione [!DNL Analytics for Advertising]. Il suo scopo principale è monitorare e trasmettere i dati dell&#39;evento [!DNL Analytics] in Adobe Advertising. Ogni volta che si verifica un click-through o una view-through, viene generato un ID EF univoco, anche se si tratta esattamente dello stesso annuncio per lo stesso visitatore. L&#39;ID EF non è utilizzato nell&#39;interfaccia utente di [!DNL Analytics] per la generazione di rapporti perché in genere supera i 500.000 valori univoci per limite variabile in [!DNL Analytics], rendendolo inutilizzabile per la generazione di rapporti. Le metriche e i metadati dell’Adobe Advertising non vengono applicati all’ID EF, ma solo all’AMO ID. Per l’ottimizzazione della campagna in Adobe Advertising è necessaria una maggiore granularità del tracciamento, pertanto sono necessari entrambi gli ID.

Anche se la dimensione EF ID non viene utilizzata direttamente nei rapporti di [!DNL Analytics], l&#39;EF ID può essere utile nella creazione di canali di marketing. Il suffisso EF ID indica il canale (visualizzazione o ricerca) e se la visita è stata guidata da un click-through o da una visualizzazione view-through. Il delimitatore nell’ID EF è un due punti, anziché il punto esclamativo nell’AMO ID.

| Suffisso ID EF | Canale |
|-------|---------|
| :s | [!UICONTROL Paid Search] |
| :d | [!UICONTROL Display Click-through] |
| :i | [!UICONTROL Display View-through] |

### Esempi di regole di elaborazione che utilizzano l’ID EF

#### Visualizza regola di click-through

Crea un canale di marketing click-through di visualizzazione acquisendo solo i click-through. Poiché l’AMO ID è lo stesso sia per i click-through che per i view-through, questa regola utilizza la variabile EF ID e il parametro della stringa di query `ef_id`.

A volte i click-through vengono tracciati attraverso l’URL (impostazione predefinita). In altri casi, i click-through vengono tracciati tramite il servizio Last Event sul lato server e pertanto l&#39;URL non contiene il parametro `ef_id`. La regola verifica quindi le condizioni in cui la variabile EF ID o il parametro della stringa di query `ef_id` termina con &quot;:d&quot;. Utilizzare l&#39;operatore &quot;`Any`&quot; perché si desidera attivare questa regola per entrambe le condizioni.

![Esempio di regola di click-through di visualizzazione](/help/integrations/assets/a4adc-mc-rule-display-ct.png)

#### Visualizza regola view-through

Per creare un canale view-through di visualizzazione, crea una regola in cui l’ID EF termina con &quot;:i&quot;. Poiché il visitatore non ha fatto clic sull&#39;annuncio, il tracciamento view-through non include `ef_id` o `s_kwcid` nell&#39;URL, pertanto la regola richiede una sola condizione.

![Esempio di regola di visualizzazione view-through](/help/integrations/assets/a4adc-mc-rule-display-vt.png)

>[!MORELIKETHIS]
>
>* [Nozioni di base di [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Perché i dati del canale possono variare tra Adobe Advertising e [!DNL Marketing Channels]](mc-data-variances.md)
>* [Utilizzo di [!DNL Analytics Marketing Channels] con dati Adobe Advertising](mc-ac-data.md)
>* [Video: utilizzo di [!DNL Marketing Channels] per Adobe Advertising di reporting](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [ID Adobe Advertising utilizzati da [!DNL Analytics]](/help/integrations/analytics/ids.md)
