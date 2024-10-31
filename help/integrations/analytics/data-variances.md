---
title: Varianze di dati previste tra  [!DNL Analytics]  e Adobe Advertising
description: Varianze di dati previste tra  [!DNL Analytics]  e Adobe Advertising
feature: Integration with Adobe Analytics
exl-id: 66b49881-bda1-49ef-ab8a-61399b8edd0f
source-git-commit: 6470ed471c60477bf19cf9b125f0250136f31511
workflow-type: tm+mt
source-wordcount: '3358'
ht-degree: 0%

---

# Varianze di dati previste tra [!DNL Analytics] e Adobe Advertising

*Inserzionisti con una sola integrazione Adobe Advertising-Adobe Analytics*

Gli inserzionisti con l&#39;integrazione [!DNL Analytics for Advertising] <!-- (A4AdC) --> registrano gli annunci a pagamento tramite Adobe Advertising e Adobe Analytics. Quando si tiene traccia di contenuti multimediali, campagne e canali tramite più sistemi, raramente gli stessi set di dati di sistemi diversi corrispondono completamente. In questo documento viene illustrato come si prevede che i dati dei file multimediali oggetto di traffico tramite Adobe Advertising vengano confrontati con i dati dei diversi sistemi in cui i file multimediali vengono tracciati in [!DNL Analytics].

>[!NOTE]
>
>Questo documento si concentra su Adobe Advertising e Analytics, ma molti dei punti chiave sono trasferibili anche ad altre soluzioni di tracciamento.

## Differenze di attribuzione in rapporti simili

### Finestre di lookback e modelli di attribuzione potenzialmente diversi

L&#39;integrazione di [!DNL Analytics for Advertising] utilizza due variabili ([!DNL eVars] o [!DNL rVars] \[riservato [!DNL eVars]]\) per acquisire l&#39;ID [EF e l&#39;AMO ID](ids.md). Queste variabili sono configurate con un singolo intervallo di lookback (il tempo entro il quale vengono attribuiti i click-through e le view-through) e un modello di attribuzione. Se non diversamente specificato, le variabili sono configurate per corrispondere all’intervallo di lookback dei clic e al modello di attribuzione predefiniti a livello di inserzionista in Adobe Advertising.

Tuttavia, gli intervalli di lookback e i modelli di attribuzione sono configurabili sia in Analytics (tramite [!DNL eVars]) che in Adobe Advertising. Inoltre, ad Adobe Advertising, il modello di attribuzione è configurabile non solo a livello di inserzionista (per l’ottimizzazione delle offerte), ma anche all’interno di singole visualizzazioni di dati e rapporti (solo a scopo di reporting). Ad esempio, un&#39;organizzazione potrebbe preferire il modello di attribuzione distribuzione uniforme per l&#39;ottimizzazione, ma utilizzare l&#39;attribuzione ultimo contatto per i rapporti in Advertising DSP o [!DNL Advertising Search, Social, & Commerce]. La modifica dei modelli di attribuzione cambia il numero di conversioni attribuite.

Se un intervallo di lookback o un modello di attribuzione viene modificato in un prodotto e non nell’altro, gli stessi rapporti di ciascun sistema mostrano dati distinti:

* **Esempio di discrepanze causate da diversi intervalli di lookback:**

  Supponiamo che l&#39;Adobe Advertising abbia un intervallo di lookback di 60 giorni e che [!DNL Analytics] abbia un intervallo di lookback di 30 giorni. E supponiamo che un utente arrivi al sito tramite un annuncio tracciato dagli Adobi Advertising, se ne vada, quindi ritorni al giorno 45 e converta. Adobe Advertising attribuisce la conversione alla visita iniziale perché la conversione si è verificata all’interno dell’intervallo di lookback di 60 giorni. [!DNL Analytics], tuttavia, non può attribuire la conversione alla visita iniziale perché la conversione si è verificata dopo la scadenza dell&#39;intervallo di lookback di 30 giorni. In questo Adobe Advertising viene segnalato un numero di conversioni maggiore rispetto a [!DNL Analytics].

  ![Esempio di conversione attribuita in Adobe Advertising ma non [!DNL Analytics]](/help/integrations/assets/a4adc-lookback-example.png)

* **Esempio di discrepanze causate da diversi modelli di attribuzione:**

  Supponiamo che un utente interagisca con tre diversi annunci di Adobe Advertising prima della conversione, con i ricavi come tipo di conversione. Se un rapporto di Adobe Advertising utilizza un modello di distribuzione uniforme per l’attribuzione, i ricavi vengono attribuiti in modo uniforme tra tutti gli annunci. Tuttavia, se [!DNL Analytics] utilizza il modello di attribuzione ultimo contatto, attribuisce i ricavi all&#39;ultimo annuncio. Nell&#39;esempio seguente, Adobe Advertising attribuisce un valore pari a 10 USD dei 30 USD di ricavi acquisiti a ciascuno dei tre annunci, mentre [!DNL Analytics] attribuisce tutti i 30 USD di ricavi all&#39;ultimo annuncio visualizzato dall&#39;utente. Confrontando i rapporti di Adobe Advertising e [!DNL Analytics], è possibile prevedere l&#39;impatto della differenza nell&#39;attribuzione.

  ![Ricavi diversi attribuiti a Adobe Advertising e [!DNL Analytics] in base a modelli di attribuzione diversi](/help/integrations/assets/a4adc-attribution-example.png)

>[!IMPORTANT]
>
>La best practice prevede di utilizzare gli stessi intervalli di lookback e lo stesso modello di attribuzione sia nell’Adobe Advertising che in [!DNL Analytics]. Collabora con il tuo Account Team Adobe per identificare le impostazioni correnti e mantenere sincronizzate le configurazioni.

Questi stessi concetti si applicano a qualsiasi altro canale simile che utilizza intervalli di lookback o modelli di attribuzione diversi.

#### Diversi intervalli di lookback per il tracciamento view-through {#impression-lookback}

Ad Adobe Advertising, l’attribuzione si basa su clic e impression e puoi configurare diversi intervalli di lookback per i clic e le impression. In [!DNL Analytics], tuttavia, l&#39;attribuzione si basa su click-through e view-through e non è possibile impostare finestre di attribuzione diverse per i click-through e i view-through; il tracciamento di ogni inizia alla visita iniziale del sito. Un’impression può verificarsi lo stesso giorno o più giorni prima che si verifichi una view-through e la tempistica può influire sul punto in cui inizia la finestra di attribuzione in ciascun sistema.

In genere, la maggior parte delle conversioni view-through si verifica abbastanza rapidamente da attribuire credito a entrambi i sistemi. Tuttavia, alcune conversioni possono verificarsi al di fuori dell&#39;intervallo di lookback di impression Adobe Advertising ma all&#39;interno dell&#39;intervallo di lookback [!DNL Analytics]; tali conversioni sono attribuite alla view-through in [!DNL Analytics] ma non all&#39;impression in Adobe Advertising.

Nell’esempio seguente, supponiamo che a un visitatore sia stato servito un annuncio il Giorno 1, che abbia eseguito una visita view-through (ovvero abbia visitato la pagina di destinazione dell’annuncio senza fare clic in precedenza sull’annuncio) il Giorno 2 e che sia stato convertito il Giorno 45. In questo caso, Adobe Advertising tiene traccia dell’utente dai giorni 1-14 (utilizzando un lookback di 14 giorni), [!DNL Analytics] tiene traccia dell’utente dai giorni 2-61 (utilizzando un lookback di 60 giorni) e la conversione nel giorno 45 viene attribuita all’annuncio entro [!DNL Analytics] ma non all’interno di Adobe Advertising.

![Esempio di conversione view-through attribuita in [!DNL Analytics] ma non nell&#39;Adobe Advertising](/help/integrations/assets/a4adc-viewthrough-example.png)

Un&#39;ulteriore causa di discrepanze è che, ad Adobe Advertising, è possibile assegnare alle conversioni view-through un *peso view-through* personalizzato relativo al peso attribuito a una conversione basata su clic. Il peso predefinito della visualizzazione view-through è 40%, il che significa che una conversione view-through viene conteggiata come 40% del valore di una conversione basata su clic. [!DNL Analytics] non fornisce una tale ponderazione delle conversioni view-through. Ad Adobe Advertising, un ordine di ricavi da 100 USD acquisito in [!DNL Analytics] viene scontato a 40 USD se si utilizza il peso view-through predefinito, una differenza di 60 USD.

Considerare queste differenze durante il confronto delle conversioni view-through tra i report Adobe Advertising e [!DNL Analytics].

#### Modelli di attribuzione disponibili

| Attribuzione Adobe Advertising | Attribuzione [!DNL Analytics] | Allocazione [!DNL eVar]/[!DNL rVar] |
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
>Per l&#39;allocazione lineare, [!DNL Analytics] attribuisce gli eventi di successo in modo uniforme tra tutti i valori [!DNL eVar] all&#39;interno di una singola visita, quindi utilizza l&#39;allocazione lineare con una scadenza [!DNL eVar] di &quot;Visita&quot;. Per la pubblicità, tuttavia, l’utilizzo dell’attribuzione lineare porta a un’allocazione non realmente lineare e a rapporti non ideali. Ad esempio, se un visitatore interagisce con tre annunci prima di convertirli in tre visite separate, alla conversione viene attribuito solo l’annuncio visualizzato nell’ultima visita, non tutti e tre gli annunci.
>
>Inoltre, il passaggio dell’allocazione di conversione da o a &quot;Lineare&quot; impedisce la visualizzazione dei dati storici, il che può portare a dati errati nei rapporti. Ad esempio, l&#39;allocazione lineare potrebbe dividere i ricavi in diversi valori di [!DNL eVar]. Se modifichi l’allocazione in &quot;Most Recent&quot; (Più recente), il 100% di tali ricavi viene associato al singolo valore più recente. Questa associazione può portare a conclusioni errate.
>
>Per evitare confusione, [!DNL Analytics] rende i dati cronologici non disponibili nell&#39;interfaccia di reporting. È possibile visualizzare i dati storici se si ripristina l&#39;impostazione di allocazione iniziale di [!DNL eVar], anche se non è consigliabile modificare le impostazioni di allocazione di [!DNL eVar] per accedere semplicemente ai dati storici. Adobe consiglia di utilizzare un nuovo [!DNL eVar] quando si desidera applicare una nuova impostazione di allocazione per i dati già registrati, anziché modificare le impostazioni di allocazione per un [!DNL eVar] che dispone già di una quantità significativa di dati storici.

Consulta un elenco dei modelli di attribuzione [!DNL Analytics] e delle relative definizioni in [https://experienceleague.adobe.com/en/docs/analytics/analyze/analysis-workspace/attribution/models](https://experienceleague.adobe.com/en/docs/analytics/analyze/analysis-workspace/attribution/models).

Se hai effettuato l&#39;accesso a [!DNL Search, Social, & Commerce], puoi trovare un elenco

* (Utenti in Nord America) [`https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm`](https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm)

* (Tutti gli altri utenti) [`https://enterprise-intl.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm`](https://enterprise-intl.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm)

#### Attribuzione data evento in Adobe Advertising

Ad Adobe Advertising, puoi generare rapporti sui dati di conversione in base alla data di clic/data dell’evento associata (la data dell’evento di clic o di impression) o in base alla data della transazione (data di conversione). Il concetto di reporting sulla data di clic/evento non esiste in [!DNL Analytics]; tutte le conversioni tracciate in [!DNL Analytics] sono segnalate per data di transazione. Di conseguenza, la stessa conversione può essere segnalata con date diverse in Adobe Advertising e [!DNL Analytics]. Ad esempio, considera un utente che fa clic su un annuncio il 1° gennaio e converte il 5 gennaio. Se in Adobe Advertising visualizzi i dati di conversione per data evento, la conversione viene segnalata il 1° gennaio, quando si è verificato il clic. In [!DNL Analytics], la stessa conversione viene segnalata il 5 gennaio.

![Esempio di conversione attribuita a date diverse](/help/integrations/assets/a4adc-conversions-based-on.png)

## Attribuzione in [!DNL Analytics Marketing Channels]

[[!DNL Analytics Marketing Channels] generazione rapporti](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html) consente di configurare le regole per identificare diversi canali di marketing in base ad aspetti distinti delle informazioni sugli hit. È possibile tenere traccia dei canali tracciati dagli Adobi Advertising ([!UICONTROL Display Click Through], [!UICONTROL Display View Through] e [!UICONTROL Paid Search]) come [!DNL Marketing Channels] utilizzando il parametro della stringa di query `ef_id` per identificare il canale. <!-- Move most of the above text to "Marketing Channels" chapter once it's created, and add link here. --> Tuttavia, anche se i report [!DNL Marketing Channels] possono tenere traccia dei canali di Adobe Advertising, i dati potrebbero non corrispondere ai report di Adobe Advertising per diversi motivi. Per ulteriori informazioni, consulta le sezioni seguenti.

>[!NOTE]
>
> I seguenti concetti di base si applicano anche a qualsiasi tracciamento multicanale che coinvolge campagne non tracciate in Adobe Advertising, come la variabile [`campaign`](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/campaign.html) (nota anche come dimensione &quot;Codice di tracciamento&quot; o &quot;[!DNL eVar] 0&quot;) e il tracciamento personalizzato [!DNL eVar].

### Modelli di attribuzione potenzialmente diversi in [!DNL Marketing Channels]

La maggior parte dei rapporti [!DNL Marketing Channels] è configurata con attribuzione [!UICONTROL Last Touch], a cui è assegnato il 100% del valore di conversione dell&#39;ultimo canale di marketing rilevato. L&#39;utilizzo di diversi modelli di attribuzione per i report [!DNL Marketing Channels] e i report di Adobe Advertising genera discrepanze nelle conversioni attribuite.

### Un intervallo di lookback potenzialmente diverso in [!DNL Marketing Channels]

L&#39;intervallo di lookback per [!DNL Marketing Channels] può essere personalizzato. Ad Adobe Advertising, l’intervallo di lookback su clic è configurabile, anche se una finestra fissa di 60 giorni è comune. Se i due prodotti utilizzano intervalli di lookback diversi, si possono verificare discrepanze di dati.

### Attribuzione canale diversa in [!DNL Marketing Channels]

I report Adobe Advertising acquisiscono solo contenuti multimediali a pagamento oggetto di traffico tramite Adobe Advertising (ricerca a pagamento per [!DNL Advertising Search, Social, & Commerce] annunci e visualizzazione per annunci Advertising DSP), mentre i report [!DNL Marketing Channels] possono tenere traccia di tutti i canali digitali. Questo può causare una discrepanza nel canale per il quale viene attribuita una conversione.

Ad esempio, i canali di ricerca a pagamento e di ricerca naturale hanno spesso una relazione simbiotica, in cui ogni canale assiste l’altro. Il report [!DNL Marketing Channels] attribuisce alcune conversioni alla ricerca naturale che l&#39;Adobe Advertising non ha perché non tiene traccia della ricerca naturale.

Considera anche un cliente che visualizza un annuncio di visualizzazione, fa clic su un annuncio di ricerca a pagamento, fa clic all’interno di un messaggio e-mail e quindi effettua un ordine di 30 USD. Anche se sia Adobe Advertising che [!DNL Marketing Channels] utilizzano il modello di attribuzione ultimo contatto, la conversione verrebbe comunque attribuita in modo diverso a ciascuno di essi. L&#39;Adobe Advertising non ha accesso al canale [!UICONTROL Email], pertanto accrediterebbe la ricerca a pagamento per la conversione. [!DNL Marketing Channels], tuttavia, ha accesso a tutti e tre i canali, pertanto attribuirebbe il merito a [!UICONTROL Email] per la conversione.

![Esempio di attribuzione di conversione diversa in Adobe Advertising rispetto a [!DNL Analytics Marketing Channels]](/help/integrations/assets/a4adc-channel-example.png)

Per ulteriori spiegazioni sul motivo per cui le metriche possono variare, vedere &quot;[Why Channel Data Can Vary Between Adobe Advertising and [!DNL Marketing Channels]](marketing-channels/mc-data-variances.md)&quot; (Perché i dati del canale possono variare da un  all&#39;altro).

## Differenze di dati in Adobe Analytics [!DNL Paid Search Detection]

La funzionalità [legacy [!DNL Paid Search Detection]](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/paid-search-detection/paid-search-detection.html) in [!DNL Analytics] consente alle aziende di [definire regole per il monitoraggio del traffico di ricerca organico e a pagamento](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/t-paid-search-detection.html) per i motori di ricerca specificati. Le regole [!DNL Paid Search Detection] utilizzano sia una stringa di query che il dominio di riferimento per identificare il traffico di ricerca a pagamento e naturale. I report [!DNL Paid Search Detection] fanno parte del gruppo più ampio di report [Metodi di ricerca](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/finding-methods.html), che scadono quando si verifica un evento specificato, ad esempio il Check-Out del carrello, oppure al termine della visita.

Di seguito è riportata l&#39;interfaccia per la creazione di un set di regole [!DNL Paid Search Detection]:

![Esempio di regola di rilevamento ricerca a pagamento impostata in [!DNL Analytics]](/help/integrations/assets/a4adc-paid-search-detection.png)

I report [!DNL Paid Search Detection] risultanti includono [!UICONTROL Paid Search Engine], [!UICONTROL Paid Search Keywords], [!UICONTROL Natural Search Engine] e [!UICONTROL Natural Search Keywords].

Tenere presente le due limitazioni seguenti con i dati nei report [!DNL Paid Search Detection]:

* I report [!UICONTROL Paid Search Keywords] e [!UICONTROL Natural Search Keywords] mostrano le query di ricerca identificate dagli URL di riferimento, non le parole chiave su cui gli utenti fanno un&#39;offerta. I report Adobe Advertising e [!DNL Analytics] visualizzano le parole chiave effettive, quindi non aspettarti che si allineino con i report [!DNL Paid Search Detection] per parole chiave.

* Al momento della creazione della funzionalità [!DNL Paid Search Detection], la query di ricerca di origine (la stringa di caratteri immessa dall&#39;utente nella barra di ricerca nel motore di ricerca) era più facilmente disponibile per gli inserzionisti tramite l&#39;URL di riferimento. Attualmente, i motori di ricerca offuscano in gran parte la query di ricerca e i report per parole chiave [!DNL Paid Search Detection] hanno un valore limitato perché la maggior parte dei dati della query rientra in &quot;non specificato&quot;.

  Con [!DNL Analytics for Advertising], gli inserzionisti possono ancora tenere traccia delle parole chiave a pagamento in [!DNL Analytics]. Il dominio di riferimento informa il motore di rapporti su quale motore di ricerca ha guidato il traffico. Poiché le informazioni sull’account specifiche dell’inserzionista non sono legate al dominio di riferimento, tutto il traffico viene elencato nel motore di ricerca. Gli inserzionisti con più account nello stesso motore di ricerca devono fare riferimento al reporting di Adobe Advertising o [!DNL Analytics] per il reporting specifico dell&#39;account.

### Perché configurare [!DNL Paid Search Detection]?

I report [!DNL Paid Search Detection] ti consentono di identificare il traffico di ricerca naturale nei [[!DNL Analytics Marketing Channels] report](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html). La separazione del traffico di ricerca a pagamento dal traffico di ricerca naturale è un ottimo modo per comprendere il valore che la ricerca naturale apporta all’intero ecosistema di marketing.

## Convalida dei dati di click-through per [!DNL Analytics for Advertising] {#data-validation}

Ai fini dell’integrazione, è necessario convalidare i dati di click-through per assicurarsi che tutte le pagine del sito tengano correttamente traccia dei click-through.

In [!DNL Analytics], uno dei modi più semplici per convalidare il tracciamento di [!DNL Analytics for Advertising] consiste nel confrontare le istanze con i clic utilizzando una metrica calcolata &quot;Istanze AMO ID per clic&quot;, calcolata come segue:

```
AMO ID Instances to Clicks = ([!UICONTROL AMO ID Instances] / [!UICONTROL Adobe Advertising Clicks])
```

[!UICONTROL AMO ID Instances] rappresenta il numero di volte in cui [AMO ID](ids.md) sono tracciati sul sito. Ogni volta che si fa clic su un annuncio, viene aggiunto un parametro AMO ID (`s_kwcid`) all&#39;URL della pagina di destinazione. Il numero di [!UICONTROL AMO ID Instances] è quindi analogo al numero di clic e può essere convalidato in base ai clic effettivi sugli annunci. In genere viene visualizzata una percentuale di corrispondenza dell&#39;85% per [!DNL Search, Social, & Commerce] e una percentuale di corrispondenza del 30% per il traffico [!DNL DSP] (quando filtrato per includere solo il click-through [!UICONTROL AMO ID Instances]). La differenza nelle aspettative tra ricerca e visualizzazione può essere spiegata dal comportamento di traffico previsto. La ricerca acquisisce l’intento e, come tale, gli utenti in genere intendono fare clic sui risultati della ricerca dalla propria query. Tuttavia, gli utenti che visualizzano un annuncio video display o online hanno più probabilità di fare clic sull’annuncio involontariamente e quindi di eseguire un rimbalzo dal sito o di abbandonare la nuova finestra che viene caricata prima che l’attività della pagina venga tracciata.

Nei rapporti di Adobe Advertising, è possibile confrontare in modo simile le istanze con i clic utilizzando la metrica &quot;[!UICONTROL EF ID Instances]&quot; invece di [!UICONTROL AMO ID Instances]:

```
EF ID Instances to Clicks = ([!UICONTROL EF ID Instances] / [!UICONTROL Adobe Advertising Clicks])
```

Anche se è previsto un tasso di corrispondenza elevato tra AMO ID e EF ID, non si prevede una parità del 100% perché AMO ID e EF ID tengono traccia fondamentalmente di dati diversi e questa differenza può portare a lievi differenze nel totale di [!UICONTROL AMO ID Instances] e [!UICONTROL EF ID Instances]. Se il totale di [!UICONTROL AMO ID Instances] in [!DNL Analytics] differisce da [!UICONTROL EF ID Instances] in Adobe Advertising di oltre l&#39;1%, tuttavia, contatta il team dell&#39;account Adobe per assistenza.

Per ulteriori informazioni sull&#39;AMO ID e sull&#39;EF ID, vedi [ID Adobi Advertising utilizzati da Analytics](ids.md).

<!--  Need to create a new report to show tracking instances to clicks, instead of clicks to instances as shown, and replace this screenshot.

The following is an example of a workspace to track clicks to instances.

![Example of a workspace to track clicks to instances to clicks](/help/integrations/assets/a4adc-clicks-to-instances-example.png)
-->

### Risoluzione dei problemi di disparità tra clic e istanze

Se il rapporto tra [!UICONTROL EF ID Instances] e clic è inferiore all&#39;85%, verifica quanto segue:

* Ti manca il tracciamento dei clic per l’account o a qualsiasi livello secondario, oppure è presente il tracciamento dei clic duplicato (ad esempio, a livello di account e di campagna)?

  In Search, Social e Commerce, [scarica un bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) per consentire all&#39;account di controllare gli URL di tracciamento.

  Inoltre, in [!DNL Analytics], è possibile verificare se l’AMO ID e l’EF IF sono aggiunti in modo coerente utilizzando una metrica calcolata da &quot;[!DNL AMO ID] a [!DNL EF ID]&quot;, calcolata come segue:

  ```
  [!DNL AMO ID] to [!DNL EF ID] = ([!UICONTROL AMO ID] / [!DNL EF ID])
  ```

  Un valore superiore al 100% indica che mancano più ID EF rispetto agli AMO ID.

* La pagina di destinazione presenta un problema di caricamento che impedisce l’acquisizione dell’AMO ID e dell’EF?

* L’URL della pagina di destinazione viene reindirizzato in modo da perdere l’AMO ID e l’EF ID?

* Tutte le pagine di destinazione utilizzano la suite di rapporti configurata?

>[!NOTE]
>
>In teoria, è possibile che una istanza abbia più clic. Assicurati di verificare la presenza di clic su diversi dispositivi (ad esempio desktop, dispositivi mobili e tablet).

## Confronto dei set di dati in [!DNL Analytics for Advertising] rispetto a Adobe Advertising

Il [AMO ID](ids.md) (parametro della stringa di query s_kwcid) è utilizzato per il reporting in [!DNL Analytics] e il [EF ID](ids.md) (parametro della stringa di query ef_id) è utilizzato per il reporting in Adobe Advertising. Poiché si tratta di valori distinti, un valore può essere danneggiato o non aggiunto alla pagina di destinazione.

Ad esempio, supponiamo di avere la seguente pagina di destinazione:

```
www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id
```

dove l&#39;ID EF è &quot;`test_ef_id`&quot; e l&#39;AMO ID è &quot;`test_amo_id`&quot;.

Se si verifica un reindirizzamento lato sito, l’URL potrebbe presentarsi così:

```
www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id#redirectAnchorTag
```

dove l&#39;ID EF è &quot;`test_ef_id`&quot; e l&#39;AMO ID è &quot;`test_amo_id#redirectAnchorTag`&quot;.

In questo esempio, l’aggiunta del tag di ancoraggio aggiunge caratteri imprevisti all’AMO ID, causando un valore che Analytics non riconosce. Questo AMO ID non sarebbe classificato e le conversioni associate ad esso rientrerebbero in &quot;[!UICONTROL unspecified]&quot; o &quot;[!UICONTROL none]&quot; nei report [!DNL Analytics].

Fortunatamente, problemi come questo sono comuni, ma in genere non causano un&#39;alta percentuale di discrepanze. Tuttavia, se noti una grande discrepanza tra gli AMO ID in [!DNL Analytics] e gli EF ID in Adobe Advertising, contatta il team dell’account Adobe per assistenza.

## Altre considerazioni sulle metriche

### Differenza tra clic e visite {#clicks-vs-visits}

Sembrano simili, ma i clic e le visite rappresentano dati diversi:

* **Clic:** [!DNL DSP] o il motore di ricerca registra un clic quando un visitatore fa clic su un annuncio sul sito Web di un editore.

* **Visita:** [!DNL Analytics] definisce una [visita](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html) come una serie di visualizzazioni di pagina da parte di un utente, che termina in base a uno dei diversi criteri, ad esempio 30 minuti di inattività.

Per definizione, un clic può portare a più visite.

Prendi in considerazione l’esempio seguente: l’utente 1 e l’utente 2 accedono entrambi a un sito facendo clic su un annuncio di Adobe Advertising. L’utente 1 visualizza quattro pagine e poi parte per la giornata, quindi il clic iniziale dà luogo a una visita. L’utente 2 visualizza due pagine, parte per un pranzo di 45 minuti, torna, visualizza altre due pagine e poi se ne va; in questo caso, il clic iniziale si traduce in due visite.

![Esempio della differenza tra clic e visite](/help/integrations/assets/a4adc-visits-example.png)

### Differenza tra clic e click-through

<!-- Rob to let me know if we should remove this and add more info. to the section on AMO Instances etc. -->

I click-through sono due metriche diverse:

* **Clic:** [!DNL DSP] o il motore di ricerca registra un clic quando un visitatore fa clic su un annuncio sul sito Web di un editore.

* **Click-through:** [!DNL Analytics] registra un click-through quando il visitatore arriva al sito Web di destinazione, la pagina di destinazione viene caricata e la richiesta [!DNL Analytics] nella parte inferiore della pagina invia i dati a [!DNL Analytics].

I click-through e i click-through possono variare notevolmente a causa di clic accidentali sugli annunci. Abbiamo notato che la maggior parte dei clic sugli annunci di visualizzazione sono clic accidentali e questi visitatori accidentali hanno premuto il pulsante Indietro prima del caricamento della pagina di destinazione, pertanto [!DNL Analytics] non può registrare un click-through. Ciò è particolarmente vero per gli annunci su cui è più probabile un clic accidentale, come gli annunci per dispositivi mobili, gli annunci video e gli annunci che riempiono lo schermo e devono essere chiusi prima che l’utente possa visualizzare la pagina.

È inoltre meno probabile che i siti caricati su dispositivi mobili generino click-through a causa di larghezze di banda inferiori o della potenza di elaborazione disponibile, con conseguenti tempi di caricamento delle pagine di destinazione più lunghi. Non è raro che il 50-70% dei clic non si traduca in click-through. Negli ambienti mobili, la differenza può arrivare fino al 90% a causa della combinazione di un browser più lento e della maggiore probabilità che l’utente faccia clic accidentalmente sull’annuncio mentre scorre la pagina o tenta di chiudere l’annuncio.

I dati dei clic possono anche essere registrati in ambienti che non possono registrare i click-through con i meccanismi di tracciamento correnti (come i clic che entrano in o provengono da un’app mobile) o per i quali l’inserzionista ha implementato un solo approccio di tracciamento (ad esempio, con l’approccio JavaScript view-through, i browser che bloccano i cookie di terze parti tengono traccia dei clic, ma non dei click-through). Un motivo chiave per cui Adobe consiglia di distribuire sia l’approccio di tracciamento URL di clic che quello di tracciamento view-through di JavaScript è quello di massimizzare la copertura dei click-through tracciabili.

### Utilizzo delle metriche del traffico Adobe Advertising per i Dimension non Adobi Advertising

L&#39;Adobe Advertising fornisce ad Analytics [metriche di traffico specifiche per la pubblicità e le dimensioni correlate da [!DNL DSP] e [!DNL Search, Social, & Commerce]](advertising-metrics-in-analytics.md). Le metriche fornite dall&#39;Adobe Advertising sono applicabili solo alle dimensioni dell&#39;Adobe Advertising specificate e i dati non sono disponibili per altre dimensioni in [!DNL Analytics].

Se ad esempio si visualizzano le metriche [!UICONTROL Adobe Advertising Clicks] e [!UICONTROL Adobe Advertising Cost] per conto, che è una dimensione di Adobe Advertising, il totale di [!UICONTROL Adobe Advertising Clicks] e [!UICONTROL Adobe Advertising Cost] verrà visualizzato per conto.

![Esempio di metriche di Adobe Advertising in un report che utilizza una dimensione di Adobe Advertising](/help/integrations/assets/a4adc-traffic-supported-dimension.png)

Tuttavia, se visualizzi le metriche [!UICONTROL Adobe Advertising Clicks] e [!UICONTROL Adobe Advertising Cost] per una dimensione su pagina (come Pagina), per la quale Adobe Advertising non fornisce dati, allora i [!UICONTROL Adobe Advertising Clicks] e i [!UICONTROL Adobe Advertising Cost] per ogni pagina sono zero (0).

![Esempio di metriche di Adobe Advertising in un report che utilizza una dimensione non supportata](/help/integrations/assets/a4adc-traffic-unsupported-dimension.png)

### Utilizzo di [!UICONTROL AMO ID Instances] come sostituto dei clic con Dimension non Adobi Advertising

Poiché non è possibile utilizzare [!UICONTROL AMO Clicks] con dimensioni nel sito, potrebbe essere utile trovare un equivalente ai clic. In alternativa, potresti essere tentato di utilizzare le Visite, ma non sono l’opzione migliore, perché ogni visitatore può avere più visite. (Vedi &quot;[La differenza tra clic e visite](#clicks-vs-visits).&quot; È invece consigliabile utilizzare [!UICONTROL AMO ID Instances], che è il numero di volte in cui l’AMO ID viene acquisito. Anche se [!UICONTROL AMO ID Instances] non corrisponde esattamente a [!UICONTROL AMO Clicks], è l&#39;opzione migliore per misurare il traffico dei clic sul sito. Per ulteriori informazioni, vedere &quot;[Convalida dati Click-through per [!DNL Analytics for Advertising]](#data-validation)&quot;.

![Esempio di [!UICONTROL AMO ID Instances] invece di [!UICONTROL Adobe Advertising Clicks] per una dimensione non supportata](/help/integrations/assets/a4adc-amo-id-instances.png)

>[!MORELIKETHIS]
>
>* [Panoramica di [!DNL Analytics for Advertising]](overview.md)
>* [ID Adobe Advertising utilizzati da [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Metriche di Adobe Advertising in Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Dati in Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
>* [Perché i dati possono variare tra Adobe Advertising e [!DNL Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md)
