---
title: Varianze di dati previste tra [!DNL Analytics] e pubblicità Adobe
description: Varianze di dati previste tra [!DNL Analytics] e pubblicità Adobe
feature: Integration with Adobe Analytics
exl-id: 66b49881-bda1-49ef-ab8a-61399b8edd0f
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '3276'
ht-degree: 0%

---

# Varianze di dati previste tra [!DNL Analytics] e pubblicità Adobe

*Inserzionisti con una sola integrazione Advertising-Adobe Analytics di Adobe*

Gli inserzionisti con [!DNL Analytics for Advertising] <!-- (A4AdC) --> pubblicità a pagamento tramite Adobe Advertising e Adobe Analytics. Quando tieni traccia dei contenuti multimediali, delle campagne e dei canali tramite più sistemi, gli stessi set di dati di diversi sistemi raramente corrispondono completamente. In questo documento viene illustrato come aspettarsi che i dati dei file multimediali oggetto di traffico tramite Adobe Advertising vengano confrontati con i dati dei diversi sistemi in cui i file multimediali vengono tracciati [!DNL Analytics].

>[!NOTE]
>
>Questo documento si concentra su Adobe Advertising e Analytics, ma molti dei punti chiave sono trasferibili anche ad altre soluzioni di tracciamento.

## Differenze di attribuzione in rapporti simili

### Finestre di lookback e modelli di attribuzione potenzialmente diversi

La [!DNL Analytics for Advertising] l&#39;integrazione utilizza due variabili (eVar o rVar \[eVar riservate]\) per acquisire il [ID EF e ID AMO](ids.md). Queste variabili sono configurate con un singolo intervallo di lookback (il tempo entro il quale vengono attribuiti click-through e view-through) e un modello di attribuzione. Se non viene specificato diversamente, le variabili sono configurate in modo che corrispondano all’intervallo di lookback a livello di inserzionista e al modello di attribuzione predefinito in Adobe Advertising.

Tuttavia, gli intervalli di lookback e i modelli di attribuzione sono configurabili sia in Analytics (tramite le eVar) che in Adobe Advertising. Inoltre, in Adobe Advertising, il modello di attribuzione è configurabile non solo a livello dell’inserzionista (per l’ottimizzazione delle offerte), ma anche all’interno di singole visualizzazioni di dati e rapporti (solo a scopo di reporting). Ad esempio, un’organizzazione può preferire utilizzare il modello di attribuzione distribuzione pari per l’ottimizzazione, ma utilizzare l’attribuzione ultimo contatto per i rapporti in Advertising DSP o [!DNL Advertising Search]. La modifica dei modelli di attribuzione modifica il numero di conversioni attribuite.

Se un intervallo di lookback per reporting o un modello di attribuzione viene modificato in un prodotto e non nell’altro, gli stessi rapporti di ogni sistema mostreranno dati distinti:

* **Esempio di discrepanze causate da diversi intervalli di lookback:**

   Supponiamo che Adobe Advertising abbia un intervallo di lookback su 60 giorni e [!DNL Analytics] ha un intervallo di lookback di 30 giorni. E supponiamo che un utente arrivi al sito tramite un annuncio pubblicitario Adobe tracciato, se ne vada, e poi ritorni il giorno 45 e si converte. Ad Adobe, la conversione verrà attribuita alla visita iniziale perché si è verificata all’interno dell’intervallo di lookback di 60 giorni. [!DNL Analytics]Tuttavia, non è possibile attribuire la conversione alla visita iniziale perché la conversione si è verificata dopo la scadenza dell’intervallo di lookback di 30 giorni. In questo esempio, Adobe Advertising segnalerebbe un numero di conversioni più elevato rispetto a [!DNL Analytics] .

   ![Esempio di conversione attribuita in pubblicità Adobe ma non [!DNL Analytics]](/help/integrations/assets/a4adc-lookback-example.png)

* **Esempio di discrepanze causate da diversi modelli di attribuzione:**

   Supponiamo che un utente interagisca con tre diversi annunci pubblicitari di Adobe prima della conversione, con i ricavi come tipo di conversione. Se un rapporto Pubblicitario di Adobe utilizza un modello di distribuzione uniforme per l’attribuzione, attribuirà i ricavi in modo uniforme in tutti gli annunci. Se [!DNL Analytics] utilizza il modello di attribuzione ultimo contatto, tuttavia, attribuirà i ricavi all’ultimo annuncio. Nell’esempio seguente, Adobe Advertising attribuisce un valore pari a 10 USD dei 30 USD di ricavi acquisiti per ciascuno dei tre annunci, mentre [!DNL Analytics] attribuisce tutti i 30 USD dei ricavi all’ultimo annuncio visualizzato dall’utente. Quando confronti rapporti da pubblicità Adobe e [!DNL Analytics], noterai l’impatto della differenza di attribuzione.

   ![Entrate diverse attribuite alla pubblicità Adobe e [!DNL Analytics] basato su diversi modelli di attribuzione](/help/integrations/assets/a4adc-attribution-example.png)

>[!IMPORTANT]
>
>La best practice prevede l’utilizzo degli stessi intervalli di lookback e dello stesso modello di attribuzione in Adobe Advertising e [!DNL Analytics]. Lavora con il tuo [!DNL Adobe] il team dell&#39;account, se necessario, per identificare le impostazioni correnti e mantenere le configurazioni sincronizzate.

Questi stessi concetti si applicano a qualsiasi altro tipo di canale che utilizza diversi intervalli di lookback o modelli di attribuzione.

#### Diverse finestre di lookback per il tracciamento view-through {#impression-lookback}

Ad Adobe, nella pubblicità l’attribuzione è basata su clic e impression e puoi configurare diverse finestre di lookback per clic e impression. In [!DNL Analytics], tuttavia, l’attribuzione si basa su click-through e view-through e non è possibile impostare finestre di attribuzione diverse per click-through e view-through; il tracciamento per ogni inizia dalla visita iniziale del sito. Un’impression può verificarsi lo stesso giorno o più giorni prima dell’esecuzione di una visualizzazione-through, e questo può avere un impatto sul punto in cui inizia la finestra di attribuzione in ciascun sistema.

In genere, la maggior parte delle conversioni view-through avviene abbastanza rapidamente che entrambi i sistemi attribuiscono credito. Tuttavia, alcune conversioni possono verificarsi al di fuori dell’intervallo di lookback Adobe Advertising impression ma all’interno del [!DNL Analytics] intervallo di lookback; tali conversioni sono attribuite al view-through in [!DNL Analytics] ma non all&#39;impressione in pubblicità Adobe.

Nell’esempio seguente, supponiamo che a un visitatore sia stato servito un annuncio il Giorno 1, abbia effettuato una visita di visualizzazione (ovvero, abbia visitato la pagina di destinazione dell’annuncio senza prima fare clic sull’annuncio) il Giorno 2 e che abbia effettuato una conversione il Giorno 45. In questo caso, Adobe Advertising tiene traccia dell’utente dai giorni 1-14 (utilizzando un lookback di 14 giorni), [!DNL Analytics] tiene traccia dell’utente dai giorni 2-61 (utilizzando un lookback di 60 giorni) e la conversione dal giorno 45 viene attribuita all’annuncio all’interno di [!DNL Analytics] ma non all&#39;interno di Adobe Advertising.

![Esempio di conversione view-through attribuita in [!DNL Analytics] ma non pubblicità Adobe](/help/integrations/assets/a4adc-viewthrough-example.png)

Un&#39;altra causa di discrepanze è che, ad Adobe la pubblicità, puoi assegnare le conversioni view-through a un&#39;impostazione personalizzata *ponderazione view-through* relativo al peso attribuito a una conversione basata su clic. Il peso predefinito della visualizzazione passante è pari al 40%, il che significa che una conversione di visualizzazione through viene conteggiata come il 40% del valore di una conversione basata su clic. [!DNL Analytics] non fornisce alcuna ponderazione di questo tipo per le conversioni view-through. Quindi, per esempio, un ordine di 100 dollari di ricavi registrato in [!DNL Analytics] Sarà scontato a 40 USD in Adobe Advertising se utilizzi il peso predefinito della vista-through — una differenza di 60 USD.

Considera queste differenze quando confronti le conversioni view-through tra Adobe Advertising e [!DNL Analytics] rapporti.

#### Modelli di attribuzione disponibili

| Attribuzione pubblicitaria Adobe | [!DNL Analytics] Attribuzione | Allocazione eVar/Var |
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
>Per l&#39;allocazione lineare, [!DNL Analytics] attribuisce gli eventi di successo in modo uniforme a tutti i valori eVar all’interno di una singola visita, quindi utilizza l’allocazione lineare con una scadenza eVar di &quot;Visita&quot;. Per la pubblicità, tuttavia, l’utilizzo dell’attribuzione lineare porta a un’allocazione non realmente lineare e a una generazione di rapporti meno ideali. Ad esempio, se un visitatore interagisce con tre annunci prima di effettuare la conversione in tre visite separate, alla conversione viene attribuito solo l’annuncio visualizzato nell’ultima visita, non tutti e tre gli annunci.
>
>Inoltre, il passaggio dall’allocazione di conversione a o da &quot;Lineare&quot; impedisce la visualizzazione dei dati storici, il che può portare a dati erronei nei rapporti. Ad esempio, l’allocazione lineare potrebbe dividere i ricavi in un numero di diversi valori eVar. Se modifichi l’allocazione in &quot;Più recente&quot;, il 100% di tali ricavi viene associato al valore singolo più recente. Questa associazione può portarti a conclusioni errate.
>
>Per evitare confusione, [!DNL Analytics] rende i dati storici non disponibili nell’interfaccia di reporting. È possibile visualizzare i dati storici se si modifica l&#39;eVar di nuovo all&#39;impostazione di allocazione iniziale, anche se non è necessario modificare le impostazioni di allocazione di eVar semplicemente per accedere ai dati storici. Adobe consiglia di utilizzare un nuovo eVar quando si desidera applicare una nuova impostazione di allocazione per i dati già registrati, anziché modificare le impostazioni di allocazione per un eVar che dispone già di una quantità significativa di dati storici.

Visualizza un elenco di [!DNL Analytics] modelli di attribuzione e relative definizioni in [https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html).

Se hai effettuato l’accesso [!DNL Search], puoi trovare un elenco di modelli di attribuzione in
[https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm](https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm).

#### Attribuzione della data dell’evento in Adobe Advertising

Ad Adobe, nella pubblicità puoi segnalare i dati di conversione in base alla data di clic/evento associata (la data dell’evento di clic o impression) o in base alla data della transazione (data di conversione). Il concetto di generazione rapporti data clic/evento non esiste in [!DNL Analytics]; tutte le conversioni rilevate [!DNL Analytics] sono segnalati per data della transazione. Di conseguenza, la stessa conversione può essere segnalata con date diverse in Pubblicità Adobe e [!DNL Analytics]. Ad esempio, considera un utente che fa clic su un annuncio il 1° gennaio e si converte il 5 gennaio. Se visualizzi i dati di conversione per data evento in Adobe Advertising, la conversione verrà segnalata il 1° gennaio, quando si è verificato il clic. In [!DNL Analytics], la stessa conversione verrebbe segnalata il 5 gennaio.

![Esempio di conversione attribuita a date diverse](/help/integrations/assets/a4adc-conversions-based-on.png)

## Attribuzione in [!DNL Analytics Marketing Channels]

[[!DNL Analytics Marketing Channels] reporting](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html) ti consente di configurare regole per identificare diversi canali di marketing in base a aspetti distinti delle informazioni sugli hit. Puoi tenere traccia dei canali tracciati dalla pubblicità di Adobe ([!UICONTROL Display Click Through], [!UICONTROL Display View Through]e [!UICONTROL Paid Search]) come [!DNL Marketing Channels] utilizzando `ef_id` parametro della stringa di interrogazione per identificare il canale. <!-- Move most of the above text to "Marketing Channels" chapter once it's created, and add link here. --> Tuttavia, anche se [!DNL Marketing Channels] I rapporti possono tenere traccia dei canali di pubblicità di Adobe, i dati potrebbero non corrispondere ai rapporti di pubblicità di Adobe per diversi motivi. Per ulteriori informazioni, consulta le sezioni seguenti.

>[!NOTE]
>
> I seguenti concetti di base si applicano anche a qualsiasi tracciamento multicanale che coinvolge campagne non tracciate in Adobe Advertising, come [`campaign`](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/campaign.html) (noto anche come Dimension &quot;Tracking Code&quot; (Codice di tracciamento) o &quot;eVar 0&quot;) e monitoraggio eVar personalizzato.

### Modelli di attribuzione potenzialmente diversi in [!DNL Marketing Channels]

Più [!DNL Marketing Channels] i rapporti sono configurati con [!UICONTROL Last Touch] all’attribuzione, per la quale l’ultimo canale di marketing rilevato viene assegnato il 100% del valore di conversione. Utilizzo di diversi modelli di attribuzione per [!DNL Marketing Channels] rapporti e rapporti sulla pubblicità di Adobe porteranno a discrepanze nelle conversioni attribuite.

### Un intervallo di lookback potenzialmente diverso in [!DNL Marketing Channels]

Intervallo di lookback per [!DNL Marketing Channels] possono essere personalizzati. In Adobe Advertising, l’intervallo di lookback su clic è configurabile, anche se una finestra fissa di 60 giorni è comune. Se i due prodotti utilizzano finestre di lookback diverse, si possono verificare discrepanze nei dati.

### Attribuzione di canale diversa in [!DNL Marketing Channels]

I report pubblicitari di Adobe catturano solo i media a pagamento trafficati attraverso la pubblicità di Adobe (ricerca a pagamento per [!DNL Advertising Search] annunci e display per annunci pubblicitari DSP), [!DNL Marketing Channels] i rapporti possono tenere traccia di tutti i canali digitali. Questo può causare una discrepanza nel canale per il quale viene attribuita una conversione.

Ad esempio, i canali di ricerca a pagamento e naturali hanno spesso una relazione simbiotica, in cui ogni canale aiuta l&#39;altro. La [!DNL Marketing Channels] report attribuirà alcune conversioni alla ricerca naturale che Adobe Advertising non vuole perché non tiene traccia della ricerca naturale.

Considera anche un cliente che visualizza un annuncio visualizzato, fa clic su un annuncio di ricerca a pagamento, fa clic all’interno di un messaggio e-mail e quindi inserisce un ordine di 30 USD. Anche se Adobe Advertising e [!DNL Marketing Channels] entrambi utilizzano il modello di attribuzione dell’ultimo contatto, la conversione viene comunque attribuita in modo diverso a ciascuno di essi. Adobe Advertising non ha accesso al [!UICONTROL Email] quindi accrediterebbe la ricerca a pagamento per la conversione. [!DNL Marketing Channels], tuttavia, dispone dell&#39;accesso a tutti e tre i canali, in modo da accreditare [!UICONTROL Email] per la conversione.

![Esempio di attribuzione della conversione diversa in Adobe Advertising rispetto a [!DNL Analytics Marketing Channels]](/help/integrations/assets/a4adc-channel-example.png)

Per ulteriori spiegazioni sul perché le metriche possono variare, vedi &quot;[Perché i dati del canale possono variare tra la pubblicità Adobe e [!DNL Marketing Channels]](marketing-channels/mc-data-variances.md).&quot;

## Differenze di dati in Adobe Analytics [!DNL Paid Search Detection]

La [legacy [!DNL Paid Search Detection]](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/paid-search-detection/paid-search-detection.html) in [!DNL Analytics] consente alle aziende di [definire regole per monitorare il traffico di ricerca a pagamento e organico](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/t-paid-search-detection.html) per motori di ricerca specifici. La [!DNL Paid Search Detection] le regole utilizzano sia una stringa di query che il dominio di riferimento per identificare il traffico di ricerca a pagamento e naturale. La [!DNL Paid Search Detection] i report fanno parte del gruppo più ampio di [Metodi di ricerca](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/finding-methods.html) rapporti, che scadono quando si verifica un evento specifico (ad esempio un checkout del carrello) o quando la visita termina.

Di seguito è riportata l’interfaccia per la creazione di un [!DNL Paid Search Detection] set di regole:

![Esempio di regola di rilevamento di ricerca a pagamento impostata in [!DNL Analytics]](/help/integrations/assets/a4adc-paid-search-detection.png)

Il risultato [!DNL Paid Search Detection] i rapporti includono [!UICONTROL Paid Search Engine], [!UICONTROL Paid Search Keywords], [!UICONTROL Natural Search Engine]e [!UICONTROL Natural Search Keywords] rapporti.

Tieni presente le due limitazioni seguenti per i dati in [!DNL Paid Search Detection] rapporti:

* La [!UICONTROL Paid Search Keywords] e [!UICONTROL Natural Search Keywords] i rapporti mostrano le query di ricerca identificate dagli URL di riferimento, non le parole chiave su cui gli utenti fanno offerte. Pubblicità Adobe e [!DNL Analytics] i rapporti mostrano le parole chiave effettive, pertanto non aspettarti che siano allineate con [!DNL Paid Search Detection] rapporti sulle parole chiave.

* Quando il [!DNL Paid Search Detection] La funzionalità è stata creata originariamente, la query di ricerca di origine (la stringa di caratteri immessa dall’utente nella barra di ricerca nel motore di ricerca) era più facilmente disponibile agli inserzionisti tramite l’URL di riferimento. Oggi, i motori di ricerca offuscano ampiamente la query di ricerca e il [!DNL Paid Search Detection] i rapporti sulle parole chiave hanno un valore limitato perché la maggior parte dei dati delle query rientrano in &quot;non specificato&quot;.

   Con [!DNL Analytics for Advertising], gli inserzionisti possono ancora tenere traccia delle parole chiave a pagamento in [!DNL Analytics]. Il dominio di riferimento informa il motore che indica quale motore di ricerca ha guidato il traffico. Poiché le informazioni dell’account specifiche dell’inserzionista non sono legate al dominio di riferimento, tutto il traffico è elencato nel motore di ricerca. Gli inserzionisti con più account nello stesso motore di ricerca devono fare riferimento ad Adobe Advertising o [!DNL Analytics] generazione di rapporti per rapporti specifici per account.

### Perché configurare [!DNL Paid Search Detection]?

La [!DNL Paid Search Detection] i rapporti ti consentono di identificare il traffico di ricerca naturale nel [[!DNL Analytics Marketing Channels] rapporti](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html). Separare il traffico di ricerca a pagamento rispetto al traffico di ricerca naturale è un ottimo modo per comprendere il valore che la ricerca naturale porta al pieno ecosistema di marketing.

## Convalida dei dati click-through per [!DNL Analytics for Advertising] {#data-validation}

Per l’integrazione, devi convalidare i dati di click-through per assicurarti che tutte le pagine del sito stiano tracciando correttamente i click-through.

In [!DNL Analytics], uno dei modi più semplici per convalidare [!DNL Analytics for Advertising] il tracciamento serve a confrontare i clic con le istanze utilizzando la metrica calcolata &quot;Clic su istanze AMO ID&quot;, calcolata come segue:

```
Clicks to AMO ID Instances = (AMO ID Instances / AMO Clicks)
```

[!UICONTROL AMO ID Instances] rappresenta il numero di volte in cui gli ID AMO (`s_kwcid` ) sono tracciati sul sito. Ogni volta che si fa clic su un annuncio, un `s_kwcid` viene aggiunto all’URL della pagina di destinazione. Numero di [!UICONTROL AMO ID Instances], quindi, è analogo al numero di clic e può essere convalidato rispetto ai clic effettivi degli annunci. Generalmente vediamo un tasso di corrispondenza dell’80% per [!DNL Search] e un tasso di corrispondenza del 30% per [!DNL DSP] traffico (se filtrato per includere solo il click-through) [!UICONTROL AMO ID Instances]). La differenza nelle aspettative tra ricerca e visualizzazione può essere spiegata dal comportamento previsto del traffico. La ricerca acquisisce l’intento e, come tale, gli utenti in genere hanno intenzione di fare clic sui risultati della ricerca dalla query. Tuttavia, gli utenti che visualizzano un video o un annuncio video online hanno più probabilità di fare clic sull’annuncio in modo non intenzionale e quindi di rimbalzare dal sito o abbandonare la nuova finestra che viene caricata prima che l’attività della pagina venga tracciata.

In Adobe Advertising Reports (Rapporti sulla pubblicità), puoi confrontare in modo simile i clic con le istanze utilizzando &quot;[!UICONTROL ef_id_instances]&quot; metrica anziché [!UICONTROL AMO ID Instances]:

```
Clicks to [EF ID Instances = (ef_id_instances / Clicks)
```

Anche se ti dovresti aspettare un tasso di corrispondenza elevato tra l’AMO ID e l’EF ID, non aspettarti una parità del 100% perché AMO ID e EF ID registrano in modo fondamentale dati diversi, e questa differenza può portare a lievi differenze nel totale [!UICONTROL AMO ID Instances] e [!UICONTROL EF ID Instances]. Se il totale [!UICONTROL AMO ID Instances] in [!DNL Analytics] differisci da [!UICONTROL EF ID Instances] in Adobe Advertising di oltre l’1%, tuttavia, contatta il tuo [!DNL Adobe] per assistenza.

Per ulteriori informazioni sull’AMO ID e sull’EF ID, vedi [ID pubblicitari di Adobe utilizzati da Analytics](ids.md).

Di seguito è riportato un esempio di un’area di lavoro per tenere traccia dei clic sulle istanze.

![Esempio di un’area di lavoro per tenere traccia dei clic sulle istanze](/help/integrations/assets/a4adc-clicks-to-instances-example.png)

## Confronto di set di dati in [!DNL Analytics for Advertising] Contro la pubblicità Adobe

La [ID AMO](ids.md) (parametro della stringa di query s_kwcid) viene utilizzato per il reporting in [!DNL Analytics]e [ID EF](ids.md) viene utilizzato per i rapporti in Adobe Advertising. Poiché sono valori distinti, è possibile che un valore sia danneggiato o non aggiunto alla pagina di destinazione.

Ad esempio, supponiamo di avere la seguente pagina di destinazione:

```
www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id
```

dove l’ID EF è &quot;`test_ef_id`&quot; e l&#39;AMO ID è &quot;`test_amo_id`.&quot;

Se si verifica un reindirizzamento lato sito, l&#39;URL potrebbe finire così:

```
www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id#redirectAnchorTag
```

dove l’ID EF è &quot;`test_ef_id`&quot; e l&#39;AMO ID è &quot;`test_amo_id#redirectAnchorTag`.&quot;

In questo esempio, l’aggiunta del tag di ancoraggio aggiunge caratteri imprevisti all’AMO ID, dando luogo a un valore che Analytics non riconosce. Questo AMO ID non verrebbe classificato e le conversioni ad esso associate rientrano in &quot;[!UICONTROL unspecified]&quot; o &quot;[!UICONTROL none]&quot; [!DNL Analytics] rapporti.

Fortunatamente, anche se problemi come questo sono comuni, di solito non si traducono in un&#39;alta percentuale di discrepanza. Tuttavia, se noti una grande discrepanza tra gli AMO ID in [!DNL Analytics] e gli ID EF in Adobe Advertising, contatta il tuo [!DNL Adobe] per assistenza.

## Altre considerazioni sulle metriche

### Differenza tra clic e visite {#clicks-vs-visits}

Sembrano simili, ma clic e visite rappresentano dati diversi:

* **Fai clic su:** [!DNL DSP] o il motore di ricerca registra un clic quando un visitatore fa clic su un annuncio sul sito web di un editore.

* **Visita:** [!DNL Analytics] definisce un [visita](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html) come serie di visualizzazioni di pagina effettuate da un utente, che terminano in base a uno dei vari criteri, ad esempio 30 minuti di inattività.

Per definizione, un clic può portare a più visite.

Prendi in considerazione l’esempio seguente: L&#39;utente 1 e l&#39;utente 2 accedono a un sito facendo clic su un annuncio pubblicitario Adobe. L’utente 1 visualizza quattro pagine e poi parte per il giorno, quindi il clic iniziale risulta in una visita. L&#39;utente 2 visualizza due pagine, parte per un pranzo di 45 minuti, ritorna, visualizza altre due pagine e poi parte; in questo caso, il clic iniziale si traduce in due visite.

![Esempio della differenza tra clic e visite](/help/integrations/assets/a4adc-visits-example.png)

### Differenza tra clic e clic

<!-- Rob to let me know if we should remove this and add more info. to the section on AMO Instances etc. -->

I clic e i click-through sono due metriche diverse:

* **Fai clic su:** [!DNL DSP] o il motore di ricerca registra un clic quando un visitatore fa clic su un annuncio sul sito web di un editore.

* **Click-through:** [!DNL Analytics] registra un click-through quando il visitatore arriva sul sito web di destinazione, carica la pagina di destinazione e [!DNL Analytics] La richiesta nella parte inferiore della pagina invia i dati a [!DNL Analytics].

I clic e i click-through possono variare notevolmente a causa di clic accidentali di annunci. Abbiamo osservato che la maggior parte dei clic sugli annunci visualizzati sono clic accidentali e questi visitatori accidentali hanno premuto il pulsante Indietro prima del caricamento della pagina di destinazione, quindi [!DNL Analytics] Impossibile registrare un click-through. Ciò è particolarmente vero per gli annunci per i quali è più probabile un clic accidentale, come annunci mobile, annunci video e annunci che riempiono lo schermo e devono essere chiusi prima che l’utente possa visualizzare la pagina.

È inoltre meno probabile che i siti caricati su dispositivi mobili si traducano in click-through a causa di larghezze di banda inferiori o potenza di elaborazione disponibile, il che causa un rallentamento del caricamento delle pagine di destinazione. Non è raro che il 50-70% dei clic non si traduca in click-through. Negli ambienti mobili, la differenza può raggiungere il 90% a causa della combinazione di un browser più lento e della maggiore probabilità che l’utente faccia accidentalmente clic sull’annuncio mentre scorre la pagina o cerca di chiudere l’annuncio.

I dati dei clic possono anche essere registrati in ambienti che non possono registrare i click-through con i meccanismi di tracciamento correnti (come i clic che entrano o provengono da un’app mobile) o per i quali l’inserzionista ha implementato un solo approccio di tracciamento (ad esempio, con l’approccio JavaScript di visualizzazione, i browser che bloccano i cookie di terze parti monitoreranno i clic, ma non i click-through). Un motivo chiave per cui l’Adobe consiglia di implementare sia il tracciamento degli URL di clic che l’approccio di tracciamento di visualizzazione tramite JavaScript è quello di massimizzare la copertura dei click-through tracciabili.

### Utilizzo delle metriche del traffico pubblicitario di Adobe per Dimension pubblicitari non Adobi

Adobe Advertising fornisce ad Analytics [le metriche del traffico specifiche per la pubblicità e le relative dimensioni da [!DNL DSP] e [!DNL Search]](advertising-metrics-in-analytics.md). Le metriche fornite da Adobe Advertising sono applicabili solo alle dimensioni pubblicitarie di Adobe specificate e i dati non sono disponibili per altre dimensioni in [!DNL Analytics].

Ad esempio, se visualizzi il [!UICONTROL AMO Clicks] e [!UICONTROL AMO Cost] metriche per account, che è un Adobe di dimensione Advertising, vedrai il totale [!UICONTROL AMO Clicks] e [!UICONTROL AMO Cost] per conto.

![Esempio di metriche pubblicitarie di Adobe in un rapporto utilizzando una dimensione pubblicitaria di Adobe](/help/integrations/assets/a4adc-traffic-supported-dimension.png)

Tuttavia, se visualizzi il [!UICONTROL AMO Clicks] e [!UICONTROL AMO Cost] metriche in base a una dimensione su pagina (ad esempio Pagina), per la quale Adobe Advertising non fornisce dati, quindi il [!UICONTROL AMO Clicks] e [!UICONTROL AMO Cost] per ogni pagina sarà zero (0).

![Esempio di metriche pubblicitarie di Adobe in un rapporto utilizzando una dimensione non supportata](/help/integrations/assets/a4adc-traffic-unsupported-dimension.png)

### Utilizzo [!UICONTROL AMO ID Instances] come sostituto dei clic con Dimension pubblicitari non Adobi

Poiché non puoi utilizzare [!UICONTROL AMO Clicks] con le dimensioni sul sito, potresti voler trovare un equivalente ai clic. Puoi essere tentato di utilizzare le visite come sostituto, ma non sono l’opzione migliore perché ogni visitatore può avere più visite. (Vedi &quot;[Differenza tra clic e visite](#clicks-vs-visits).&quot; Consigliamo invece di utilizzare [!UICONTROL AMO ID Instances]: il numero di volte in cui l’AMO ID viene acquisito. Quando [!UICONTROL AMO ID Instances] non corrisponderà [!UICONTROL AMO Clicks] esattamente, sono l&#39;opzione migliore per misurare il traffico di clic sul sito. Per ulteriori informazioni, consulta &quot;[Convalida dei dati per [!DNL Analytics for Advertising]](#data-validation).&quot;

![Esempio di [!UICONTROL AMO ID Instances] anziché [!UICONTROL AMO Clicks] per una dimensione non supportata](/help/integrations/assets/a4adc-amo-id-instances.png)

>[!MORELIKETHIS]
>
>* [Panoramica [!DNL Analytics for Advertising]](overview.md)
>* [ID pubblicitari di Adobe utilizzati da [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Metriche pubblicitarie di Adobe in Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Dati in Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
>* [Perché i dati possono variare tra la pubblicità Adobe e [!DNL Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md)

