---
title: Varianze di dati previste tra [!DNL Analytics] e ADOBE ADVERTISING
description: Varianze di dati previste tra [!DNL Analytics] e ADOBE ADVERTISING
feature: Integration with Adobe Analytics
exl-id: 66b49881-bda1-49ef-ab8a-61399b8edd0f
source-git-commit: fb0634643e40b67e50461823f976a93129e2f038
workflow-type: tm+mt
source-wordcount: '3217'
ht-degree: 0%

---

# Varianze di dati previste tra [!DNL Analytics] e ADOBE ADVERTISING

*Per gli inserzionisti con una sola integrazione Adobi Advertising-Adobe Analytics*

Per gli inserzionisti con [!DNL Analytics for Advertising] <!-- (A4AdC) --> integration track pubblicità a pagamento tramite Adobi Advertising e Adobe Analytics. Quando si tiene traccia di contenuti multimediali, campagne e canali tramite più sistemi, raramente gli stessi set di dati di sistemi diversi corrispondono completamente. Questo documento spiega come aspettarsi che i dati dei media oggetto di traffico attraverso gli Adobi Advertising vengano confrontati con i dati dei diversi sistemi in cui i media vengono tracciati [!DNL Analytics].

>[!NOTE]
>
>Questo documento si concentra su Adobi Advertising e Analytics, ma molti dei punti chiave sono trasferibili anche ad altre soluzioni di tracciamento.

## Differenze di attribuzione in rapporti simili

### Finestre di lookback e modelli di attribuzione potenzialmente diversi

Il [!DNL Analytics for Advertising] l’integrazione utilizza due variabili ([!DNL eVars] o [!DNL rVars] \[riservato [!DNL eVars]]\) per acquisire [ID EF e AMO ID](ids.md). Queste variabili sono configurate con un singolo intervallo di lookback (il tempo entro il quale vengono attribuiti i click-through e le view-through) e un modello di attribuzione. Se non diversamente specificato, le variabili sono configurate per corrispondere all’intervallo di lookback dei clic e al modello di attribuzione predefiniti a livello di inserzionista in Adobi Advertising.

Tuttavia, gli intervalli di lookback e i modelli di attribuzione sono configurabili sia in Analytics (tramite il [!DNL eVars]) e in Adobe Advertising. Inoltre, ad Adobe Advertising, il modello di attribuzione è configurabile non solo a livello di inserzionista (per l’ottimizzazione delle offerte), ma anche all’interno di singole visualizzazioni di dati e rapporti (solo a scopo di reporting). Ad esempio, un’organizzazione potrebbe preferire il modello di attribuzione distribuzione uniforme per l’ottimizzazione, ma utilizzare l’attribuzione ultimo contatto per i rapporti in Advertising DSP o [!DNL Advertising Search, Social, & Commerce]. La modifica dei modelli di attribuzione cambia il numero di conversioni attribuite.

Se un intervallo di lookback o un modello di attribuzione viene modificato in un prodotto e non nell’altro, gli stessi rapporti di ciascun sistema mostreranno dati distinti:

* **Esempio di discrepanze causate da diversi intervalli di lookback:**

  Supponiamo che Adobi Advertising abbia un intervallo di lookback di clic di 60 giorni e [!DNL Analytics] ha un intervallo di lookback di 30 giorni. E supponiamo che un utente arrivi al sito tramite un annuncio tracciato dagli Adobi Advertising, se ne vada, quindi ritorni al giorno 45 e converta. Adobi Advertising attribuirà la conversione alla visita iniziale perché la conversione si è verificata all’interno dell’intervallo di lookback di 60 giorni. [!DNL Analytics]Tuttavia, non può attribuire la conversione alla visita iniziale perché la conversione si è verificata dopo la scadenza dell’intervallo di lookback di 30 giorni. In questo esempio, l’Adobe Advertising segnala un numero di conversioni maggiore di [!DNL Analytics] sì.

  ![Esempio di conversione attribuita in Adobi Advertising ma non [!DNL Analytics]](/help/integrations/assets/a4adc-lookback-example.png)

* **Esempio di discrepanze causate da diversi modelli di attribuzione:**

  Supponiamo che un utente interagisca con tre diversi annunci di Adobe Advertising prima della conversione, con i ricavi come tipo di conversione. Se un rapporto di Adobe Advertising utilizza un modello di distribuzione uniforme per l’attribuzione, i ricavi verranno attribuiti in modo uniforme a tutti gli annunci. Se [!DNL Analytics] utilizza il modello di attribuzione ultimo contatto; tuttavia, attribuirà i ricavi all’ultimo annuncio. Nell’esempio seguente, Adobi Advertising attribuisce un valore pari a 10 USD dei 30 USD di ricavi acquisiti a ciascuno dei tre annunci, mentre [!DNL Analytics] attribuisce tutti i 30 USD di ricavi all’ultimo annuncio visualizzato dall’utente. Quando confronti i rapporti di Adobi Advertising e [!DNL Analytics], puoi aspettarti di vedere l’impatto della differenza nell’attribuzione.

  ![Ricavi diversi attribuiti a Adobi Advertising e [!DNL Analytics] in base a diversi modelli di attribuzione](/help/integrations/assets/a4adc-attribution-example.png)

>[!IMPORTANT]
>
>La best practice prevede di utilizzare gli stessi intervalli di lookback e lo stesso modello di attribuzione sia nell’Adobe Advertising che nel [!DNL Analytics]. Collabora con il tuo Account Team di Adobi per identificare le impostazioni correnti e mantenere sincronizzate le configurazioni.

Questi stessi concetti si applicano a qualsiasi altro canale simile che utilizza intervalli di lookback o modelli di attribuzione diversi.

#### Diversi intervalli di lookback per il tracciamento view-through {#impression-lookback}

Ad Adobe Advertising, l’attribuzione si basa su clic e impression e puoi configurare diversi intervalli di lookback per i clic e le impression. In entrata [!DNL Analytics]Tuttavia, l’attribuzione si basa su click-through e view-through e non è possibile impostare diverse finestre di attribuzione per i click-through e i view-through; il tracciamento di ogni inizio alla visita iniziale del sito. Un’impression può verificarsi lo stesso giorno o più giorni prima che si verifichi una view-through e questo può influire sul punto in cui inizia la finestra di attribuzione in ciascun sistema.

In genere, la maggior parte delle conversioni view-through si verifica abbastanza rapidamente da attribuire credito a entrambi i sistemi. Tuttavia, alcune conversioni possono verificarsi al di fuori dell’intervallo di lookback di impression dell’Adobe Advertising, ma all’interno del [!DNL Analytics] intervallo di lookback; tali conversioni sono attribuite alla visualizzazione in [!DNL Analytics] ma non all&#39;Adobe Advertising.

Nell’esempio seguente, supponiamo che a un visitatore sia stato distribuito un annuncio il Giorno 1, che sia stata eseguita una visita view-through (cioè che abbia visitato la pagina di destinazione dell’annuncio senza fare clic in precedenza sull’annuncio) il Giorno 2 e che sia stato convertito il Giorno 45. In questo caso, Adobi Advertising tiene traccia dell’utente dai giorni 1-14 (utilizzando un lookback di 14 giorni), [!DNL Analytics] tiene traccia dell’utente dai giorni 2-61 (utilizzando un lookback di 60 giorni) e la conversione nel giorno 45 viene attribuita all’annuncio entro [!DNL Analytics] ma non nell&#39;Adobe Advertising.

![Esempio di conversione view-through attribuita a [!DNL Analytics] ma non Adobe Advertising](/help/integrations/assets/a4adc-viewthrough-example.png)

Un&#39;altra causa di discrepanze è che, ad Adobe Advertising, è possibile assegnare conversioni view-through a *ponderazione view-through* relativo al peso attribuito a una conversione basata su clic. Il peso predefinito della visualizzazione view-through è 40%, il che significa che una conversione view-through viene conteggiata come 40% del valore di una conversione basata su clic. [!DNL Analytics] non fornisce tale ponderazione delle conversioni view-through. Ad esempio, un ordine di ricavo da 100 USD registrato in [!DNL Analytics] sarà scontato a 40 USD in Adobe Advertising se si utilizza il peso view-through predefinito — una differenza di 60 USD.

Considera queste differenze durante il confronto delle conversioni view-through tra Adobi Advertising e [!DNL Analytics] rapporti.

#### Modelli di attribuzione disponibili

| Attribuzione Adobe Advertising | [!DNL Analytics] Attribuzione | [!DNL eVar]/[!DNL rVar] Allocazione |
|--- |--- |--- |
| [!UICONTROL Last Event] | [!UICONTROL Last Touch] | [!UICONTROL Most Recent] |
| [!UICONTROL First Event] | [!UICONTROL First Touch] | [!UICONTROL Original Value] |
| [!UICONTROL Weight First Event More] | n/d | n/d |
| [!UICONTROL Even Distribution] | [!UICONTROL Linear] | [!UICONTROL Linear]<br><br>Non utilizzare* |
| [!UICONTROL Weight Last Event More] | n/d | n/d |
| [!UICONTROL U-Shaped] | [!UICONTROL U-Shaped] | n/d |
| n/d | [!UICONTROL J-Shaped] | n/d |
| n/d | [!UICONTROL Inverse-J] | n/d |
| n/d | [!UICONTROL Custom] | n/d |
| n/d | [!UICONTROL Participation] | n/d |
| n/d | [!UICONTROL Algorithmic] | n/d |

>[!NOTE]
>
>Per l&#39;allocazione lineare: [!DNL Analytics] attribuisce gli eventi di successo in modo uniforme in tutti [!DNL eVar] valori all’interno di una singola visita, in modo da utilizzare l’allocazione lineare con un [!DNL eVar] scadenza di &quot;Visita&quot;. Per la pubblicità, tuttavia, l’utilizzo dell’attribuzione lineare porta a un’allocazione non realmente lineare e a rapporti non ideali. Ad esempio, se un visitatore interagisce con tre annunci prima di convertirli in tre visite separate, alla conversione viene attribuito solo l’annuncio visualizzato nell’ultima visita, non tutti e tre gli annunci.
>
>Inoltre, il passaggio dell’allocazione di conversione da o a &quot;Lineare&quot; impedisce la visualizzazione dei dati storici, il che può portare a dati errati nei rapporti. Ad esempio, l’allocazione lineare potrebbe dividere i ricavi in diversi [!DNL eVar] valori. Se modifichi l’allocazione in &quot;Most Recent&quot; (Più recente), il 100% di tali ricavi viene associato al singolo valore più recente. Questa associazione può portare a conclusioni errate.
>
>Per evitare confusione, [!DNL Analytics] rende i dati storici non disponibili nell’interfaccia di reporting. È possibile visualizzare i dati storici modificando la [!DNL eVar] torna all’impostazione di allocazione iniziale, anche se non devi modificarla [!DNL eVar] impostazioni di allocazione per accedere semplicemente ai dati storici. L’Adobe consiglia di utilizzare un nuovo [!DNL eVar] quando si desidera applicare una nuova impostazione di allocazione per i dati già registrati, anziché modificare le impostazioni di allocazione per un [!DNL eVar] che dispone già di una quantità significativa di dati storici.

Visualizza un elenco di [!DNL Analytics] modelli di attribuzione e relative definizioni in [https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html).

Se hai effettuato l’accesso a [!DNL Search, Social, & Commerce], è possibile trovare un elenco

* (Utenti in Nord America) [`https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm`](https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm)

* (Tutti gli altri utenti) [`https://enterprise-intl.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm`](https://enterprise-intl.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm)

#### Attribuzione data evento in Adobe Advertising

Ad Adobe Advertising, puoi generare rapporti sui dati di conversione in base alla data di clic/data dell’evento associata (la data dell’evento di clic o di impression) o in base alla data della transazione (data di conversione). Il concetto di reporting sulle date di clic/evento non esiste in [!DNL Analytics]; tutte le conversioni tracciate in [!DNL Analytics] sono segnalati per data di transazione. Di conseguenza, la stessa conversione può essere segnalata con date diverse in Adobe Advertising e [!DNL Analytics]. Ad esempio, considera un utente che fa clic su un annuncio il 1° gennaio e converte il 5 gennaio. Se in Adobi Advertising visualizzi i dati di conversione per data evento, la conversione verrà segnalata il 1° gennaio, quando si è verificato il clic. In entrata [!DNL Analytics], la stessa conversione sarebbe segnalata il 5 gennaio.

![Esempio di conversione attribuita a date diverse](/help/integrations/assets/a4adc-conversions-based-on.png)

## Attribuzione in [!DNL Analytics Marketing Channels]

[[!DNL Analytics Marketing Channels] reportistica](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html) consente di configurare le regole per identificare diversi canali di marketing in base ad aspetti distinti delle informazioni sugli hit. Puoi tenere traccia dei canali tracciati dagli Adobi Advertising ([!UICONTROL Display Click Through], [!UICONTROL Display View Through], e [!UICONTROL Paid Search]) come [!DNL Marketing Channels] utilizzando `ef_id` parametro stringa query per identificare il canale. <!-- Move most of the above text to "Marketing Channels" chapter once it's created, and add link here. --> Tuttavia, anche se [!DNL Marketing Channels] i report possono tenere traccia dei canali di Adobe Advertising, i dati potrebbero non corrispondere ai report di Adobe Advertising per diversi motivi. Per ulteriori informazioni, consulta le sezioni seguenti.

>[!NOTE]
>
> I seguenti concetti di base si applicano anche a qualsiasi tracciamento multicanale che coinvolga campagne non tracciate in Adobe Advertising, come ad esempio [`campaign`](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/campaign.html) variabile (nota anche come dimensione &quot;Codice di tracciamento&quot; o &quot;[!DNL eVar] 0&quot;) e personalizzato [!DNL eVar] tracciamento.

### Modelli di attribuzione potenzialmente diversi in [!DNL Marketing Channels]

Più [!DNL Marketing Channels] i rapporti sono configurati con [!UICONTROL Last Touch] attribuzione, per la quale all’ultimo canale di marketing rilevato viene assegnato il 100% del valore di conversione. Utilizzo di diversi modelli di attribuzione per [!DNL Marketing Channels] rapporti e rapporti sugli Adobi Advertising condurranno a discrepanze nelle conversioni attribuite.

### Un intervallo di lookback potenzialmente diverso in [!DNL Marketing Channels]

L’intervallo di lookback per [!DNL Marketing Channels] possono essere personalizzate. Ad Adobe Advertising, l’intervallo di lookback su clic è configurabile, anche se una finestra fissa di 60 giorni è comune. Se i due prodotti utilizzano intervalli di lookback diversi, si possono verificare discrepanze di dati.

### Attribuzione canale diversa in [!DNL Marketing Channels]

I report Adobi Advertising catturano solo i media a pagamento trafficati attraverso l&#39;Adobe Advertising (ricerca a pagamento per [!DNL Advertising Search, Social, & Commerce] annunci pubblicitari e display per la pubblicità (annunci DSP), mentre [!DNL Marketing Channels] i rapporti possono tracciare tutti i canali digitali. Questo può causare una discrepanza nel canale per il quale viene attribuita una conversione.

Ad esempio, i canali di ricerca a pagamento e di ricerca naturale hanno spesso una relazione simbiotica, in cui ogni canale assiste l’altro. Il [!DNL Marketing Channels] Il rapporto attribuirà alcune conversioni alla ricerca naturale che l’Adobe Advertising non riuscirà a ottenere perché non tiene traccia della ricerca naturale.

Considera anche un cliente che visualizza un annuncio di visualizzazione, fa clic su un annuncio di ricerca a pagamento, fa clic all’interno di un messaggio e-mail e quindi effettua un ordine di 30 USD. Anche se Adobe Advertising e [!DNL Marketing Channels] entrambi utilizzano il modello di attribuzione ultimo contatto; la conversione verrebbe comunque attribuita in modo diverso a ciascuno. L’Adobe Advertising non ha accesso a [!UICONTROL Email] , in modo da accreditare la ricerca a pagamento per la conversione. [!DNL Marketing Channels], tuttavia, ha accesso a tutti e tre i canali, pertanto [!UICONTROL Email] per la conversione.

![Adobe Advertising di attribuzione di conversione diversa in [!DNL Analytics Marketing Channels]](/help/integrations/assets/a4adc-channel-example.png)

Per ulteriori spiegazioni sul motivo per cui le metriche possono variare, consulta &quot;[Perché i dati del canale possono variare tra Adobe Advertising e [!DNL Marketing Channels]](marketing-channels/mc-data-variances.md).&quot;

## Differenze nei dati in Adobe Analytics [!DNL Paid Search Detection]

Il [legacy [!DNL Paid Search Detection]](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/paid-search-detection/paid-search-detection.html) funzionalità in [!DNL Analytics] consente alle aziende di [definire regole per tenere traccia del traffico di ricerca organica e a pagamento](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/t-paid-search-detection.html) per i motori di ricerca specificati. Il [!DNL Paid Search Detection] le regole utilizzano sia una stringa di query che il dominio di riferimento per identificare il traffico di ricerca a pagamento e naturale. Il [!DNL Paid Search Detection] i rapporti fanno parte del gruppo più ampio di [Metodi di ricerca](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/finding-methods.html) rapporti, che scadono quando si verifica un evento specificato (ad esempio, il Cart Checkout) o al termine della visita.

Di seguito è riportata l’interfaccia per la creazione di un’ [!DNL Paid Search Detection] set di regole:

![Esempio di regola di rilevamento ricerca a pagamento impostata in [!DNL Analytics]](/help/integrations/assets/a4adc-paid-search-detection.png)

Il risultato [!DNL Paid Search Detection] i rapporti includono [!UICONTROL Paid Search Engine], [!UICONTROL Paid Search Keywords], [!UICONTROL Natural Search Engine], e [!UICONTROL Natural Search Keywords] rapporti.

Osserva le due limitazioni seguenti con i dati in [!DNL Paid Search Detection] rapporti:

* Il [!UICONTROL Paid Search Keywords] e [!UICONTROL Natural Search Keywords] I report mostrano le query di ricerca identificate dagli URL di riferimento, non le parole chiave sulle quali gli utenti fanno un’offerta. ADOBE ADVERTISING e [!DNL Analytics] i report mostrano le parole chiave effettive, quindi non aspettarti che si allineino con [!DNL Paid Search Detection] rapporti sulle parole chiave.

* Quando [!DNL Paid Search Detection] originariamente creata, la query di ricerca di origine (la stringa di caratteri immessa dall’utente nella barra di ricerca nel motore di ricerca) era più facilmente disponibile per gli inserzionisti tramite l’URL di riferimento. Oggi, i motori di ricerca offuscano in gran parte la query di ricerca e il [!DNL Paid Search Detection] i rapporti sulle parole chiave hanno un valore limitato perché la maggior parte dei dati delle query rientra in &quot;non specificato&quot;.

  Con [!DNL Analytics for Advertising], gli inserzionisti possono comunque tenere traccia delle parole chiave a pagamento in [!DNL Analytics]. Il dominio di riferimento informa il motore di rapporti su quale motore di ricerca ha guidato il traffico. Poiché le informazioni sull’account specifiche dell’inserzionista non sono legate al dominio di riferimento, tutto il traffico viene elencato nel motore di ricerca. Gli inserzionisti con più account nello stesso motore di ricerca devono fare riferimento a Adobe Advertising o [!DNL Analytics] generazione di rapporti per la generazione di rapporti specifici per l’account.

### Perché configurare [!DNL Paid Search Detection]?

Il [!DNL Paid Search Detection] i rapporti ti consentono di identificare il traffico di ricerca naturale nel [[!DNL Analytics Marketing Channels] rapporti](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html). La separazione del traffico di ricerca a pagamento dal traffico di ricerca naturale è un ottimo modo per comprendere il valore che la ricerca naturale apporta all’intero ecosistema di marketing.

## Convalida dei dati di click-through per [!DNL Analytics for Advertising] {#data-validation}

Ai fini dell’integrazione, è necessario convalidare i dati di click-through per assicurarsi che tutte le pagine del sito tengano correttamente traccia dei click-through.

In entrata [!DNL Analytics], uno dei modi più semplici per convalidare [!DNL Analytics for Advertising] Il tracciamento consiste nel confrontare i clic con le istanze utilizzando un pulsante &quot;Click to [!UICONTROL AMO ID Instances]&quot;metrica calcolata, calcolata come segue:

```
Clicks to [!UICONTROL AMO ID Instances] = ([!UICONTROL AMO ID Instances] / Adobe Advertising Clicks)
```

[!UICONTROL AMO ID Instances] rappresenta il numero di volte che [AMO ID](ids.md) vengono tracciati sul sito. Ogni volta che si fa clic su un annuncio, viene visualizzato un AMO ID (`s_kwcid`) all’URL della pagina di destinazione. Il numero di [!UICONTROL AMO ID Instances], pertanto, è simile al numero di clic e può essere convalidato in base ai clic effettivi sugli annunci. In genere viene visualizzata una percentuale di corrispondenza dell’80% per [!DNL Search, Social, & Commerce] e una percentuale di corrispondenza del 30% per [!DNL DSP] traffico (se filtrato per includere solo il click-through [!UICONTROL AMO ID Instances]). La differenza nelle aspettative tra ricerca e visualizzazione può essere spiegata dal comportamento di traffico previsto. La ricerca acquisisce l’intento e, come tale, gli utenti in genere intendono fare clic sui risultati della ricerca dalla propria query. Tuttavia, gli utenti che visualizzano un annuncio video display o online hanno più probabilità di fare clic sull’annuncio involontariamente e quindi di eseguire un rimbalzo dal sito o di abbandonare la nuova finestra che viene caricata prima che l’attività della pagina venga tracciata.

Nei rapporti di Adobe Advertising, puoi confrontare in modo simile i clic con le istanze utilizzando la funzione &quot;[!UICONTROL ef_id_instances]&quot; metrica invece di [!UICONTROL AMO ID Instances]:

```
Clicks to [EF ID Instances = (ef_id_instances / Clicks)
```

Anche se è previsto un tasso di corrispondenza elevato tra AMO ID e EF ID, non aspettarti una parità del 100% perché AMO ID e EF ID tengono traccia fondamentalmente di dati diversi e questa differenza può portare a lievi differenze nel totale [!UICONTROL AMO ID Instances] e [!UICONTROL EF ID Instances]. Se il totale [!UICONTROL AMO ID Instances] in [!DNL Analytics] differire da [!UICONTROL EF ID Instances] in Adobe Advertising di oltre l’1%, tuttavia, contatta il team del tuo account Adobe per assistenza.

Per ulteriori informazioni su AMO ID e EF ID, consulta [ID Adobe Advertising utilizzati da Analytics](ids.md).

Di seguito è riportato un esempio di area di lavoro per tenere traccia dei clic sulle istanze.

![Esempio di un’area di lavoro per tenere traccia dei clic sulle istanze](/help/integrations/assets/a4adc-clicks-to-instances-example.png)

## Confronto dei set di dati in [!DNL Analytics for Advertising] Rispetto all’Adobe Advertising

Il [AMO ID](ids.md) (parametro della stringa di query s_kwcid) viene utilizzato per la generazione di rapporti in [!DNL Analytics]e [ID EF](ids.md) viene utilizzato per il reporting in Adobi Advertising. Poiché si tratta di valori distinti, un valore può essere danneggiato o non aggiunto alla pagina di destinazione.

Ad esempio, supponiamo di avere la seguente pagina di destinazione:

```
www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id
```

dove l’ID EF è &quot;`test_ef_id`&quot; e l’AMO ID è &quot;`test_amo_id`.&quot;

Se si verifica un reindirizzamento lato sito, l’URL potrebbe presentarsi così:

```
www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id#redirectAnchorTag
```

dove l’ID EF è &quot;`test_ef_id`&quot; e l’AMO ID è &quot;`test_amo_id#redirectAnchorTag`.&quot;

In questo esempio, l’aggiunta del tag di ancoraggio aggiunge caratteri imprevisti all’AMO ID, causando un valore che Analytics non riconosce. Questo AMO ID non sarebbe classificato e le conversioni ad esso associate rientrerebbero in &quot;[!UICONTROL unspecified]&quot; o &quot;[!UICONTROL none]&quot; in [!DNL Analytics] rapporti.

Fortunatamente, problemi come questo sono comuni, ma in genere non causano un&#39;alta percentuale di discrepanze. Tuttavia, se noti una grande discrepanza tra gli AMO ID in [!DNL Analytics] e ID EF in Adobe Advertising, contatta il team dell’account Adobe per assistenza.

## Altre considerazioni sulle metriche

### Differenza tra clic e visite {#clicks-vs-visits}

Sembrano simili, ma i clic e le visite rappresentano dati diversi:

* **Fai clic su:** [!DNL DSP] oppure il motore di ricerca registra un clic quando un visitatore fa clic su un annuncio sul sito web di un editore.

* **Visita:** [!DNL Analytics] definisce un [visita](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html) come una serie di visualizzazioni di pagina effettuate da un utente e terminanti in base a uno dei diversi criteri, ad esempio 30 minuti di inattività.

Per definizione, un clic può portare a più visite.

Prendi in considerazione l’esempio seguente: l’utente 1 e l’utente 2 accedono entrambi a un sito facendo clic su un annuncio di Adobe Advertising. L’utente 1 visualizza quattro pagine e poi parte per la giornata, quindi il clic iniziale dà luogo a una visita. L’utente 2 visualizza due pagine, parte per un pranzo di 45 minuti, torna, visualizza altre due pagine e poi se ne va; in questo caso, il clic iniziale si traduce in due visite.

![Esempio della differenza tra clic e visite](/help/integrations/assets/a4adc-visits-example.png)

### Differenza tra clic e click-through

<!-- Rob to let me know if we should remove this and add more info. to the section on AMO Instances etc. -->

I click-through sono due metriche diverse:

* **Fai clic su:** [!DNL DSP] oppure il motore di ricerca registra un clic quando un visitatore fa clic su un annuncio sul sito web di un editore.

* **Click-through:** [!DNL Analytics] registra un click-through quando il visitatore arriva al sito web di destinazione, la pagina di destinazione viene caricata e [!DNL Analytics] nella parte inferiore della pagina invia i dati a [!DNL Analytics].

I click-through e i click-through possono variare notevolmente a causa di clic accidentali sugli annunci. Abbiamo osservato che la maggior parte dei clic sugli annunci di visualizzazione sono clic accidentali e questi visitatori accidentali hanno premuto il pulsante Indietro prima del caricamento della pagina di destinazione, quindi [!DNL Analytics] impossibile registrare un click-through. Ciò è particolarmente vero per gli annunci su cui è più probabile un clic accidentale, come gli annunci per dispositivi mobili, gli annunci video e gli annunci che riempiono lo schermo e devono essere chiusi prima che l’utente possa visualizzare la pagina.

È inoltre meno probabile che i siti caricati su dispositivi mobili generino click-through a causa di larghezze di banda inferiori o della potenza di elaborazione disponibile, con conseguenti tempi di caricamento delle pagine di destinazione più lunghi. Non è raro che il 50-70% dei clic non si traduca in click-through. Negli ambienti mobili, la differenza può arrivare fino al 90% a causa della combinazione di un browser più lento e della maggiore probabilità che l’utente faccia clic accidentalmente sull’annuncio mentre scorre la pagina o tenta di chiudere l’annuncio.

I dati dei clic possono anche essere registrati in ambienti che non possono registrare i click-through con i meccanismi di tracciamento correnti (come i clic provenienti da o in un’app mobile) o per i quali l’inserzionista ha implementato un solo approccio di tracciamento (ad esempio, con l’approccio JavaScript view-through, i browser che bloccano i cookie di terze parti tengono traccia dei clic, ma non dei click-through). Un motivo chiave per cui l’Adobe consiglia di distribuire sia l’approccio di tracciamento degli URL di clic che quello di tracciamento view-through JavaScript è quello di massimizzare la copertura dei click-through tracciabili.

### Utilizzo delle metriche del traffico Adobe Advertising per i Dimension non Adobi Advertising

Adobi Advertising fornisce ad Analytics [le metriche del traffico specifiche per la pubblicità e le dimensioni correlate da [!DNL DSP] e [!DNL Search, Social, & Commerce]](advertising-metrics-in-analytics.md). Le metriche fornite dall’Adobe Advertising sono applicabili solo alle dimensioni dell’Adobe Advertising specificate e i dati non sono disponibili per altre dimensioni in [!DNL Analytics].

Ad esempio, se visualizzi [!UICONTROL Adobe Advertising Clicks] e [!UICONTROL Adobe Advertising Cost] metriche per conto, che è una dimensione di Adobe Advertising, visualizzerai il totale [!UICONTROL Adobe Advertising Clicks] e [!UICONTROL Adobe Advertising Cost] per account.

![Esempio di metriche di Adobe Advertising in un rapporto che utilizza una dimensione di Adobe Advertising](/help/integrations/assets/a4adc-traffic-supported-dimension.png)

Tuttavia, se visualizzi il [!UICONTROL Adobe Advertising Clicks] e [!UICONTROL Adobe Advertising Cost] metriche per una dimensione su pagina (come Pagina), per la quale Adobe Advertising non fornisce dati, il valore [!UICONTROL Adobe Advertising Clicks] e [!UICONTROL Adobe Advertising Cost] per ogni pagina sarà zero (0).

![Adobe Advertising di metriche in un rapporto che utilizza una dimensione non supportata](/help/integrations/assets/a4adc-traffic-unsupported-dimension.png)

### Utilizzo di [!UICONTROL AMO ID Instances] in sostituzione dei clic con Dimension non Adobi Advertising

Poiché non è possibile utilizzare [!UICONTROL AMO Clicks] con dimensioni nel sito, potresti voler trovare un equivalente ai clic. In alternativa, potresti essere tentato di utilizzare le Visite, ma non sono l’opzione migliore, perché ogni visitatore può avere più visite. (Vedere &quot;[Differenza tra clic e visite](#clicks-vs-visits).&quot; È invece consigliabile utilizzare [!UICONTROL AMO ID Instances], che è il numero di volte in cui l’AMO ID viene acquisito. Mentre [!UICONTROL AMO ID Instances] non corrisponde [!UICONTROL AMO Clicks] esattamente, sono l&#39;opzione migliore per misurare il traffico di clic sul sito. Per ulteriori informazioni, consulta la sezione &quot;[Convalida dei dati di click-through per [!DNL Analytics for Advertising]](#data-validation).&quot;

![Esempio di [!UICONTROL AMO ID Instances] invece di [!UICONTROL Adobe Advertising Clicks] per una dimensione non supportata](/help/integrations/assets/a4adc-amo-id-instances.png)

>[!MORELIKETHIS]
>
>* [Panoramica di [!DNL Analytics for Advertising]](overview.md)
>* [ID Adobe Advertising utilizzati da [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Metriche di Adobe Advertising in Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Dati in Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
>* [Perché i dati possono variare tra Adobe Advertising e [!DNL Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md)
