---
title: Utilizzo degli ID Adobe Advertising per creare  [!DNL Marketing Channels]  regole
description: Scopri come utilizzare gli Adobe Advertising ID per creare regole di elaborazione per  [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 525761b4-607f-4b03-9020-8051009a13c6
source-git-commit: 0813a8bddc1ecf238f4a62c4fcefd8584f32e152
workflow-type: tm+mt
source-wordcount: '1448'
ht-degree: 0%

---

# Utilizzo degli ID di Adobe Advertising per creare [!DNL Marketing Channels] regole di elaborazione

*Inserzionisti con una sola integrazione Adobe Advertising-Adobe Analytics*

Puoi utilizzare gli Adobe Advertising ID ([AMO ID e EF ID](../ids.md)) per configurare [!DNL Marketing Channels] regole di elaborazione in Adobe Analytics. Utilizza gli Adobe Advertising ID per le regole specifiche delle campagne Adobe Advertising. L&#39;ordine in cui si elaborano le regole determina se tutti i dati possibili vengono acquisiti correttamente.

## AMO ID nelle regole di elaborazione

AMO ID è il codice di tracciamento principale utilizzato per segnalare i dati di Adobe Advertising entro [!DNL Analytics]. AMO ID è una concatenazione di valori dinamici gestiti da Adobe per fornire rapporti granulari all’interno di [!DNL Analytics]. È memorizzato in una dimensione [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) o rVar (AMO ID). L&#39;AMO ID può essere impostato in [!DNL Analytics] in due modi:

* Tracciamento click-through: Adobe Advertising imposta il parametro della stringa di query `s_kwcid` in un collegamento e [!DNL Analytics] lo seleziona dall&#39;URL della pagina di destinazione quando si verifica un click-through.

* Tracciamento view-through ([!DNL DSP] Only): [!DNL Last Event Service] rileva una view-through sul lato server e invia l&#39;AMO ID a [!DNL Analytics]. In questo caso, l&#39;URL non contiene un parametro `s_kwcid`.

I valori dinamici all’interno degli AMO ID indicano il canale di marketing tracciato:

* Il prefisso nell’AMO ID può essere utilizzato per identificare il canale di primo livello all’interno di [!DNL Marketing Channels].

* Le frasi di carattere nel corpo dell’AMO ID indicano un tipo di campagna più specifico.

* Il suffisso &quot;vt&quot; è presente per il traffico view-through [!DNL DSP] e può essere utilizzato per creare canali [!DNL DSP] di click-through e view-through separati.

Il resto dell’AMO ID può essere ignorato.

| [!UICONTROL AMO ID] | Canale | Logica delle regole |
|--------|---------|--------------------|
| !ctv (suffisso) | [!UICONTROL DSP Connected TV ViewThrough] | Termina con |
| !d! (body) | [!UICONTROL Display Network] | Contiene |
| !g! (body) | [!UICONTROL Google Search] | Contiene |
| !s! (body) | [!UICONTROL Search Partner] | Contiene |
| !u! (body) | [!UICONTROL Smart Shopping Campaign] | Contiene |
| !ytv! (body) | [!UICONTROL YouTube Video Ad] | Contiene |
| !yts! (body) | [!UICONTROL YouTube Search Ad] | Contiene |
| !vp! (body) | [!UICONTROL Google Video Partners] | Contiene |
| !vt (suffisso) | [!UICONTROL DSP ViewThrough] | Termina con |
| AL! (prefisso) | [!UICONTROL Paid Search] | Inizia con |
| AC! (prefisso) | [!UICONTROL DSP Display] | Inizia con |

## ID EF nelle regole di elaborazione

AMO EF ID (EF ID) è il secondo codice di tracciamento utilizzato nell’integrazione [!DNL Analytics for Advertising]. Il suo scopo principale è monitorare e trasmettere i dati dell&#39;evento [!DNL Analytics] in Adobe Advertising. Ogni volta che si verifica un click-through o una view-through, viene generato un ID EF univoco, anche se si tratta esattamente dello stesso annuncio per lo stesso visitatore. L&#39;ID EF non è utilizzato nell&#39;interfaccia utente di [!DNL Analytics] per la generazione di rapporti perché in genere supera i 500.000 valori univoci per limite variabile in [!DNL Analytics], rendendolo inutilizzabile per la generazione di rapporti. Le metriche e i metadati di Adobe Advertising non vengono applicati all’ID EF, ma solo all’AMO ID. Per l’ottimizzazione delle campagne in Adobe Advertising è necessaria una maggiore granularità del tracciamento, pertanto sono necessari entrambi gli ID.

Anche se la dimensione EF ID non viene utilizzata direttamente nei rapporti di [!DNL Analytics], l&#39;EF ID può essere utile nella creazione di canali di marketing. Il suffisso EF ID indica il canale (visualizzazione o ricerca) e se la visita è stata guidata da un click-through o da una visualizzazione view-through. Il delimitatore nell’ID EF è un due punti, anziché il punto esclamativo nell’AMO ID.

| Suffisso ID EF | Canale |
|-------|---------|
| :s | [!UICONTROL Paid Search Click-through] |
| :d | [!UICONTROL Display ClickThrough] |
| :i | [!UICONTROL Display ViewThrough] |

## Esempi di regole di elaborazione per Adobe Advertising

Il seguente set di regole di esempio si concentra sulle regole per i canali pubblicitari (Paid Search, Display ClickThrough e Display ViewThrough). Vengono inoltre dimostrate la regola consigliata per il rilevamento di ricerche a pagamento (incluso il modo in cui tale regola interagisce con la logica del canale di marketing Ricerca naturale) e un aggiornamento facoltativo alla regola Domini di riferimento naturali.

**Nota:** è possibile separare la visualizzazione come due canali o unirla in un singolo canale in base alle preferenze dell&#39;inserzionista.

Nell’esempio sono inclusi altri canali per illustrare l’ordine consigliato di funzionamento dei canali pubblicitari rispetto ad altri canali in un’implementazione tipica.

>[!IMPORTANT]
>
>Consulta &quot;[Ordine delle operazioni per [!DNL Marketing Channels] regole](#rule-order)&quot; per informazioni sull&#39;ordine in cui le regole devono essere elaborate.

![Esempio di un set di regole di elaborazione](/help/integrations/assets/a4adc-mc-rule-set-example.png)

### Regola di ricerca a pagamento

La best practice prevede di includere due condizioni con l&#39;operatore &quot;Any&quot; per una regola [!UICONTROL Paid Search]:

* I dati relativi a costo/clic/impression contengono l’AMO ID, quindi includi l’AMO ID. L’AMO ID deve iniziare con &quot;AL!&quot; per allocare correttamente i dati di clic/costo/impression a [!UICONTROL Paid Search].<!-- Is this just called AMO ID there, not s_kwcid=XXX? What's the difference? -->

* Gli URL per i click-through [!UICONTROL Paid Search] includono sempre il parametro della stringa di query `s_kwcid`, quindi includilo per garantire che venga eseguita la deduplicazione corretta se il visitatore torna alla pagina di destinazione. Includi &quot;AL!&quot; prima di `s_kwcid` per allocare correttamente i dati di clic/costo/impression a [!UICONTROL Paid Search].

Non impostare il valore del canale sull’AMO ID. Impostalo su un valore simile al dominio di riferimento, al motore di ricerca + parola chiave o alla pagina. (Questo è rilevante per tutti i [!DNL Marketing Channels]).

<!-- Explain that comment about relevancy -- do I need to repeat this for each rule example?  -->

![Esempio di regola di ricerca a pagamento](/help/integrations/assets/a4adc-mc-rule-paid-search.png "Esempio di regola di ricerca a pagamento")

### Regola di ricerca naturale

Per [!UICONTROL Natural Search], assicurati che le regole di rilevamento [[!UICONTROL Paid Search]](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/paid-search-detection/t-paid-search-detection) includano i parametri della stringa di query `ef_id` e `s_kwcid`. In genere, questa configurazione viene eseguita automaticamente quando Advertising Search, Social e Commerce sono integrati in [!DNL Analytics], ma è necessario verificare che un amministratore di [!DNL Analytics] abbia modificato la logica dopo la configurazione dell&#39;integrazione.

Imposta la regola su &quot;Corrisponde alle regole di rilevamento ricerca naturale&quot; (che in genere è l’impostazione predefinita per questo canale).

![Esempio di regola di ricerca naturale](/help/integrations/assets/a4adc-mc-rule-natural-search.png "Esempio di regola di ricerca naturale")

### Visualizza #1 regola di click-through

Crea un canale di marketing ClickThrough di visualizzazione acquisendo solo i click-through. Poiché l’AMO ID è lo stesso sia per i click-through che per i view-through, questa regola utilizza la variabile EF ID e il parametro della stringa di query `ef_id`.

A volte i click-through vengono tracciati attraverso l’URL (impostazione predefinita). In altri casi, i click-through vengono tracciati tramite il servizio Last Event sul lato server e pertanto l&#39;URL non contiene il parametro `ef_id`. La regola verifica quindi le condizioni in cui la variabile EF ID o il parametro della stringa di query `ef_id` termina con &quot;:d&quot;. Utilizzare l&#39;operatore &quot;`Any`&quot; perché si desidera attivare questa regola per entrambe le condizioni.

![Esempio di prima regola di visualizzazione ClickThrough](/help/integrations/assets/a4adc-mc-rule-display-ct.png "Esempio di prima regola di visualizzazione ClickThrough")

### Regola dei domini di riferimento naturali

(Facoltativo) La best practice prevede l&#39;aggiunta di una condizione &quot;Is First Page of Visit&quot; (È la prima pagina della visita) con l&#39;operatore &quot;Any&quot; alla regola standard [!UICONTROL Natural Referring Domains]. Anche se questa regola è facoltativa, può aiutare a evitare che la distinzione tra maiuscole e minuscole dei referenti naturali venga impostata quando l’utente fa clic sul pulsante Indietro per tornare alla pagina di destinazione.

![Esempio di regola Domini di riferimento naturali](/help/integrations/assets/a4adc-mc-rule-natural-referring-domains.png "Esempio di regola Domini di riferimento naturali")

### Visualizza regola view-through CTV

Per tenere traccia delle view-through di [!DNL DSP] TV connessa (CTV), crea una regola in cui l&#39;AMO ID termina con `"!ctv"`. Poiché il visitatore non ha fatto clic sull&#39;annuncio, il tracciamento view-through non include `ef_id` o `s_kwcid` nell&#39;URL e la regola richiede una sola condizione.

![Esempio di regola ViewThrough di Visual CTV](/help/integrations/assets/a4adc-mc-rule-display-ctv-vt.png "Esempio di regola ViewThrough di Display CTV")

### Visualizza regola view-through

Per creare un canale Display ViewThrough, creare una regola in cui l&#39;ID EF termina con &quot;:i&quot;. Poiché il visitatore non ha fatto clic sull&#39;annuncio, il tracciamento view-through non include `ef_id` o `s_kwcid` nell&#39;URL e la regola richiede una sola condizione.

![Esempio di regola ViewThrough di visualizzazione](/help/integrations/assets/a4adc-mc-rule-display-vt.png "Esempio di regola ViewThrough di visualizzazione")

### Visualizza #2 regola di click-through

Per la seconda regola ClickThrough di visualizzazione, il set **AMO ID inizia con &quot;AC!&quot;**. Questa seconda regola consente di acquisire i dati di clic/costo/impression per il canale di visualizzazione che proviene direttamente da Adobe Advertising a [!DNL Analytics]. Questi dati sono attribuiti a un AMO ID ma non includono un URL con la stringa di query `ef_id`, pertanto questi hit non sono collegati a un AMO EF ID, che è ciò che acquisisce la prima regola di visualizzazione ClickThrough.

![Esempio di una seconda regola ClickThrough di visualizzazione](/help/integrations/assets/a4adc-mc-rule-display-ct2.png "Esempio di una seconda regola ClickThrough di visualizzazione")

## Ordine delle operazioni per le regole [!DNL Marketing Channels] {#rule-order}

![Ordine ideale delle operazioni per le regole relative ad Adobe Advertising](/help/integrations/assets/a4adc-mc-rule-order.png "Ordine ideale delle operazioni per le regole relative ad Adobe Advertising")

* Metti [!UICONTROL Paid Search] *prima* [!UICONTROL Natural Search]. In caso contrario, i dati di ricerca a pagamento possono essere assegnati alla ricerca naturale.

* Metti **first** [!UICONTROL Display ClickThrough] *before* [!UICONTROL Natural Referring Domains] e [!UICONTROL Natural Social].

* Quando utilizzi [!UICONTROL CTV view-throughs], inseriscilo *prima* [!UICONTROL Display ViewThroughs]. In caso contrario, le view-through CTV verranno acquisite come ViewThroughs di visualizzazione.

* Posiziona [!UICONTROL Display ViewThroughs] *dopo* altri canali ma prima di [!UICONTROL Internal] e [!UICONTROL Direct] perché è possibile che nello stesso evento di destinazione si verifichi un click-through view-through e non[!DNL Advertising]. Ad esempio, un visitatore può vedere un annuncio di Adobe Advertising, ottenere un&#39;impression e quindi visitare il sito tramite [!UICONTROL Natural Search].

  La procedura consigliata consiste nell&#39;assegnare la priorità agli altri canali (eccetto [!UICONTROL Internal] e [!UICONTROL Direct]) rispetto alle view-through.

* Alcuni inserzionisti potrebbero scegliere di dare priorità a [!UICONTROL Display ViewThroughs] rispetto a [!UICONTROL Natural Referring Domains]. A tale scopo, scambia l’ordine di elaborazione delle due regole.

* La regola **second** [!UICONTROL Display ClickThrough] è disponibile per rilevare i dati di clic/costo/impression provenienti direttamente da Adobe Advertising in [!DNL Analytics]. Poiché questi dati sono attribuiti solo a un AMO ID, questi hit non sono collegati a un AMO EF ID. Se non imposti questa regola, tutti i dati di clic/costo/impression rientrano nel canale [!UICONTROL Direct], che è il canale predefinito per tutti i dati che non corrispondono a [!DNL Marketing Channel]. Questa regola deve essere *successiva* alla regola view-through, altrimenti verrà rilevata qualsiasi view-through.

<!-- WORDING!!!!  Check on this, and if it's necessary still with the other info about order:  If you include additional marketing channels, be sure to run your rules in order of specificity. For example, say you create a processing rule for [!DNL YouTube] video ad traffic tracked by Advertising Search, Social, & Commerce. The AMO ID for video traffic starts with with "AL!" and contain "!ytv!". If you run the rule for Paid Search (for which the AMO ID starts with "AL!") and then run the rule for video traffic, the YouTube video ad traffic would all fall under the Paid Search channel. -->

>[!MORELIKETHIS]
>
>* [Nozioni di base di [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Perché i dati dei canali possono variare tra Adobe Advertising e [!DNL Marketing Channels]](mc-data-variances.md)
>* [Utilizzo di [!DNL Analytics Marketing Channels] con i dati di Adobe Advertising](mc-ac-data.md)
>* [Video: utilizzo di [!DNL Marketing Channels] per la generazione di rapporti di Adobe Advertising](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [ID Adobe Advertising utilizzati da [!DNL Analytics]](/help/integrations/analytics/ids.md)