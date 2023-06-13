---
title: Utilizzo degli ID Adobe Advertising per la creazione [!DNL Marketing Channels] Regole
description: Scopri come utilizzare gli ID Adobe Advertising per creare regole di elaborazione per [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 525761b4-607f-4b03-9020-8051009a13c6
source-git-commit: a59b477a6f8a616851d85bf89b58434d4d56cd83
workflow-type: tm+mt
source-wordcount: '766'
ht-degree: 0%

---

# Utilizzo degli ID Adobe Advertising per la creazione [!DNL Marketing Channels] Regole di elaborazione

*Inserzionisti con un Adobe di integrazione Advertising-Adobe Analytics Only*

Puoi utilizzare gli ID Adobe Advertising ([AMO ID e EF ID](../ids.md)) per configurare [!DNL Marketing Channels] regole di elaborazione in Adobe Analytics. Utilizza gli ID Adobe Advertising per le regole specifiche delle campagne di Adobe Advertising.

## AMO ID nelle regole di elaborazione

AMO ID è il codice di tracciamento principale utilizzato per segnalare i dati di Adobe Advertising in [!DNL Analytics]. L’AMO ID è una concatenazione di valori dinamici gestiti da Adobe per fornire rapporti granulari in [!DNL Analytics]. È memorizzato in un [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) o dimensione rVar (AMO ID). L’AMO ID può essere impostato in [!DNL Analytics] in due modi:

* Tracciamento click-through: Adobe Advertising imposta il `s_kwcid` parametro della stringa di query in un collegamento e [!DNL Analytics] recupera il parametro dall’URL della pagina di destinazione quando si verifica un click-through.
* Tracciamento view-through ([!DNL DSP] Solo per ): il servizio Last Event rileva una view-through sul lato server e invia l’AMO ID a [!DNL Analytics]. In questo caso, l’URL non contiene un `s_kwcid` parametro.

I valori dinamici all’interno degli AMO ID indicano il canale di marketing tracciato:

* Il prefisso nell’AMO ID può essere utilizzato per identificare il canale di livello superiore in [!DNL Marketing Channels].

* Le frasi di carattere nel corpo dell’AMO ID indicano un tipo di campagna più specifico.

* Il suffisso &quot;vt&quot; è presente per [!DNL DSP] e può essere utilizzato per creare un click-through e un view-through separati [!DNL DSP] canali.

Il resto dell’AMO ID può essere ignorato.

| [!UICONTROL AMO ID] | Canale | Logica delle regole |
|--------|---------|--------------------|
| AL! (prefisso) | [!UICONTROL Paid Search] | Inizia con |
| AC! (prefisso) | [!UICONTROL DSP] | Inizia con |
| !g! (body) | [!UICONTROL Google Search] | Contiene |
| !s! (body) | [!UICONTROL Search Partner] | Contiene |
| !d! (body) | [!UICONTROL Display Network] | Contiene |
| !u! (body) | [!UICONTROL Smart Shopping Campaign] | Contiene |
| !ytv! (body) | [!UICONTROL YouTube Video Ad] | Contiene |
| !yts! (body) | [!UICONTROL YouTube Search Ad] | Contiene |
| !vp! (body) | [!UICONTROL Google Video Partners] | Contiene |
| !vt (suffisso) | [!UICONTROL DSP View-through] | Termina con |

### Esempi di regole di elaborazione che utilizzano l’AMO ID

Il [!DNL Marketing Channels] regola di elaborazione per [!UICONTROL Paid Search] il canale potrebbe essere simile al seguente:

![Esempio di [!UICONTROL Paid Search] regola](/help/integrations/assets/a4adc-mc-rule-paidsearch.png)

Il [!DNL Marketing Channels] regola di elaborazione per [!UICONTROL YouTube Video Ads] il canale potrebbe essere simile al seguente:

![Esempio di [!UICONTROL YouTube Video Ads] regola](/help/integrations/assets/a4adc-mc-rule-youtube-video.png)

>[!IMPORTANT]
>
> Assicurati di eseguire le regole in ordine di specificità. Se le due regole precedenti sono state eseguite in ordine, il [!DNL YouTube] il traffico di annunci video rientra nel [!UICONTROL Paid Search] perché l’AMO ID inizierebbe entrambe con &quot;AL!&quot; e contengono &quot;!ytv!&quot;.

## ID EF nelle regole di elaborazione

L’AMO EF ID (EF ID) è il secondo codice di tracciamento utilizzato nel [!DNL Analytics for Advertising] integrazione. Il suo scopo principale è tracciare e superare [!DNL Analytics] dati dell’evento in Adobe Advertising. Ogni volta che si verifica un click-through o una view-through, viene generato un ID EF univoco, anche se si tratta esattamente dello stesso annuncio per lo stesso visitatore. L’ID EF non viene utilizzato nel [!DNL Analytics] interfaccia utente di reporting, perché in genere supera i 500.000 valori univoci per limite variabile in [!DNL Analytics], rendendolo inutilizzabile per il reporting. Le metriche e i metadati dell’Adobe Advertising non vengono applicati all’ID EF, ma solo all’AMO ID. Per l’ottimizzazione della campagna in Adobe Advertising è necessaria una maggiore granularità del tracciamento, pertanto sono necessari entrambi gli ID.

Anche se la dimensione ID EF non viene utilizzata direttamente in [!DNL Analytics] nella generazione di rapporti, l’ID EF può essere utile nella creazione di canali di marketing. Il suffisso EF ID indica il canale (visualizzazione o ricerca) e se la visita è stata guidata da un click-through o da una visualizzazione view-through. Il delimitatore nell’ID EF è un due punti, anziché il punto esclamativo nell’AMO ID.

| Suffisso ID EF | Canale |
|-------|---------|
| :s | [!UICONTROL Paid Search] |
| :d | [!UICONTROL Display Click-through] |
| :i | [!UICONTROL Display View-through] |

### Esempi di regole di elaborazione che utilizzano l’ID EF

#### Visualizza regola di click-through

Crea un canale di marketing click-through di visualizzazione acquisendo solo i click-through. Poiché l’AMO ID è lo stesso sia per i click-through che per i view-through, questa regola utilizza la variabile EF ID e `ef_id` parametro stringa query.

A volte i click-through vengono tracciati attraverso l’URL (impostazione predefinita). In altri casi, i click-through vengono tracciati attraverso il servizio Last Event sul lato server, e pertanto l’URL non contiene `ef_id` parametro. La regola verifica pertanto le condizioni in cui la variabile EF ID o il `ef_id` il parametro della stringa di query termina con &quot;:d&quot;. Utilizza la &quot;`Any`&quot; perché desideri che questa regola venga attivata per una delle due condizioni.

![Esempio di regola di click-through di visualizzazione](/help/integrations/assets/a4adc-mc-rule-display-ct.png)

#### Visualizza regola view-through

Per creare un canale view-through di visualizzazione, crea una regola in cui l’ID EF termina con &quot;:i&quot;. Poiché il visitatore non ha fatto clic sull’annuncio, il tracciamento view-through non include il `ef_id` o `s_kwcid` nell’URL, quindi la regola richiede una sola condizione.

![Esempio di regola di visualizzazione view-through](/help/integrations/assets/a4adc-mc-rule-display-vt.png)

>[!MORELIKETHIS]
>
>* [Nozioni di base di [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Perché i dati dei canali possono variare tra la pubblicità Adobe e [!DNL Marketing Channels]](mc-data-variances.md)
>* [Utilizzo di [!DNL Analytics Marketing Channels] con dati Adobe Advertising](mc-ac-data.md)
>* [Video: Utilizzo [!DNL Marketing Channels] ad Adobe Advertising Reporting](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Adobe di ID pubblicitari utilizzati da [!DNL Analytics]](/help/integrations/analytics/ids.md)
