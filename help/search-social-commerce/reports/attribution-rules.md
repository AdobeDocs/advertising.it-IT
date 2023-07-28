---
title: Calcolo delle regole di attribuzione
description: Scopri come Adobi Advertising calcola ogni tipo di regola di attribuzione.
exl-id: b61561fa-8c01-4989-9ef7-620d2b4c2c0b
feature: Search Reports
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '2439'
ht-degree: 0%

---

# Come vengono calcolate le regole di attribuzione, ad Adobe Advertising

*Solo per inserzionisti con tracciamento delle conversioni di Adobi Advertising*

<!-- Verify statements about cross-device events -->

La regola di attribuzione a livello di inserzionista viene utilizzata per attribuire i dati di conversione, potenzialmente tra più canali di annunci, in una serie di eventi che portano a una conversione.

Nei rapporti, nelle viste predefinite e personalizzate per le simulazioni a livello di portfolio di Advertising Search, Social e Commerce (Search, Social e Commerce) e (alcuni ruoli utente) per Search, Social e Commerce, la regola selezionata viene utilizzata solo per i dati di visualizzazione, report o simulazione. Le varie regole di attribuzione vengono applicate come segue.

>[!NOTE]
>
>* Le regole di attribuzione si applicano ai clic sugli annunci a pagamento in qualsiasi canale e alle impression sulla visualizzazione e sugli annunci social. Non si applicano alle impression per gli annunci di ricerca a pagamento, che non possono essere tracciati a livello di evento.
>* Adobe Advertising memorizza sempre i seguenti eventi per ogni web surfer prima di una conversione: a) il primo clic a pagamento; b) fino a 10 clic per ogni canale (ricerca, social o visualizzazione), incluso il primo clic; e c) fino a 10 impression di visualizzazione. <!-- But it can continue to attribute conversions to clicks and impressions for longer. -->
* In Advertising DSP e Advertising Creative, le definizioni multi-dispositivo considerano solo il percorso dell’evento dalla regola di attribuzione selezionata.<!-- cross-device attribution via LiveRamp only -->
* Nei report e nelle viste di gestione, il numero di posizioni decimali visualizzate per un valore dipende dalla valuta, ma in Adobi Advertising vengono memorizzati valori più precisi.

## Ultimo evento (impostazione predefinita)

Attribuisce la conversione all’ultimo clic a pagamento nella serie all’interno dell’inserzionista [fai clic sull’intervallo di lookback](/help/search-social-commerce/glossary.md#c-d) o, se non si è verificato alcun clic a pagamento, all’ultima impression nel file dell’inserzionista [intervallo di lookback delle impression](/help/search-social-commerce/glossary.md#i-j).

Quando la conversione è preceduta solo da impression, viene considerata una *view-through*, ponderato in base al valore dell&#39;inserzionista [ponderazione view-through](/help/search-social-commerce/glossary.md#uv) oppure, come specificato, in base al metodo di valutazione view-through specificato nei parametri di report, vista o simulazione personalizzata.

![Percentuali di attribuzione dell’ultimo evento](/help/search-social-commerce/assets/attribution-percent-last-event.png "Percentuali di attribuzione dell’ultimo evento")

<!-- start examples as collapsible content -->

+++Esempi di calcolo degli eventi

### Esempio con tutti i clic

Percorso evento: Click1, Click2, Click3, Conversione di 120 USD

La conversione è attribuita al Click 3 per un importo di 120 USD.

### Esempio con impression e clic

**Nota:** Le impression sono applicabili solo dalla visualizzazione e dagli annunci social.

Percorso evento: impression 1, click 1, impression 2, conversione da 120 USD

La conversione è attribuita al Click 1 per un importo di 120 USD.

### Esempio con tutte le impression

**Nota:** Sono applicabili solo le impression per la visualizzazione e gli annunci social.

Percorso evento: Impression 1, Impression 2, Impression 3, Conversione di 120 USD

La conversione è attribuita all’impression 3. Poiché la conversione è una view-through, viene applicato il metodo di valutazione view-through selezionato nella sezione &quot;Attribuzione conversione&quot; delle impostazioni del rapporto:

* Se il parametro report specifica un peso di visualizzazione ponderato, tale peso viene applicato al view-through. Ad esempio, se il peso view-through dell’inserzionista è 40%, allora 120 USD x 40% = 48 USD, quindi 48 USD è attribuito a Impression 3.

* Se il parametro del report specifica l&#39;utilizzo di valori non elaborati per le visite, non viene applicato alcun peso di visualizzazione e l&#39;intero valore di 120 USD viene attribuito all&#39;impression 3.

+++

<!-- end examples as collapsible content -->

## Primo evento

Attribuisce la conversione al primo clic a pagamento della serie all’interno della [fai clic sull’intervallo di lookback](/help/search-social-commerce/glossary.md#c-d) o, se non si è verificato alcun clic a pagamento, alla prima impression all’interno del [intervallo di lookback delle impression](/help/search-social-commerce/glossary.md#i-j). Questa regola è disponibile solo per gli eventi su singoli dispositivi.

Quando la conversione è preceduta solo da impression, viene considerata una *view-through*, ponderato in base al valore dell&#39;inserzionista [ponderazione view-through](/help/search-social-commerce/glossary.md#uv) oppure, come specificato, in base al metodo di valutazione view-through specificato nei parametri di report, vista o simulazione personalizzata.

![Percentuali di attribuzione del primo evento](/help/search-social-commerce/assets/attribution-percent-first-event.png "Percentuali di attribuzione del primo evento")

<!-- start examples as collapsible content -->

+++Esempi di calcolo degli eventi

### Esempio con tutti i clic

Percorso evento: Click 1, Click 2, Click 3, Conversione di 120 USD

La conversione è attribuita al Click 1 per un importo di 120 USD.

### Esempio con impression e clic

**Nota:** Le impression sono applicabili solo dalla visualizzazione e dagli annunci social.

Percorso evento: impression 1, click 1, impression 2, conversione da 120 USD

La conversione è attribuita al Click 1 per un importo di 120 USD.

### Esempio con tutte le impression

**Nota:** Sono applicabili solo le impression per la visualizzazione e gli annunci social.

Percorso evento: Impression 1, Impression 2, Impression 3, Conversione di 120 USD

La conversione è attribuita all’impression 1. Poiché la conversione è una view-through, viene applicato il metodo di valutazione view-through selezionato nella sezione &quot;Attribuzione conversione (Visualizza campagne)&quot; delle impostazioni del rapporto:

* Se il parametro report specifica un peso di visualizzazione ponderato, tale peso viene applicato al view-through. Ad esempio, se il peso view-through dell’inserzionista è 40%, allora 120 x 40% = 48 USD, quindi 48 USD è attribuito a Impression 1.

* Se il parametro del report specifica l&#39;utilizzo di valori non elaborati per le visite, non viene applicato alcun peso di visualizzazione e l&#39;intero valore di 120 USD viene attribuito all&#39;impression 1.

+++

<!-- end examples as collapsible content -->

## Spessore primo evento Altro

Attribuisce la conversione a tutti gli eventi della serie che si sono verificati all&#39;interno del [fai clic sull’intervallo di lookback](/help/search-social-commerce/glossary.md#c-d) e [intervallo di lookback delle impression](/help/search-social-commerce/glossary.md#i-j), ma attribuisce il maggior peso al primo evento e successivamente meno peso ai seguenti eventi. Questa regola è disponibile solo per gli eventi su singoli dispositivi.

Quando la conversione è preceduta solo da impression, viene considerata una *view-through*, ponderato in base al valore dell&#39;inserzionista [ponderazione view-through](/help/search-social-commerce/glossary.md#uv) oppure, come specificato, in base al metodo di valutazione view-through specificato nei parametri di report, vista o simulazione personalizzata.

Quando il percorso di conversione include sia clic che impression a pagamento, queste vengono trattate in modo diverso dai diversi prodotti di Adobe Advertising:

* In Search, Social e Commerce, il [peso di override impression](/help/search-social-commerce/glossary.md#i-j) , specificato nell&#39;impostazione di peso per la sostituzione delle impression dell&#39;inserzionista e nei parametri di report, visualizzazione o simulazione personalizzata, viene applicato per la prima volta alle impression.

* In DSP, le impression vengono ignorate e solo i clic vengono ponderati. L’DSP non prende in considerazione i pesi di esclusione delle impression per l’attribuzione.

![Ponderare il primo evento più percentuali di attribuzione](/help/search-social-commerce/assets/attribution-percent-weight-first-more.png "Ponderare il primo evento più percentuali di attribuzione")

<!-- start examples as collapsible content -->

+++Esempi di calcolo degli eventi

### Esempio con tutti i clic

Percorso evento: Click 1, Click 2, Click 3, Conversione di 120 USD

Attribuzione: Click 1 = 60 USD, Click 2 = 40 USD, Click 3 = 20 USD (120 USD in totale)

### Esempi con impression e clic

**Nota:** Le impression sono applicabili solo dalla visualizzazione e dagli annunci social.

Percorso evento: Impression 1, Click 1, Impression 2, Click 2, Conversione di 120 USD

#### (Solo per ricerca, social network e commerce) Con l’impostazione predefinita &quot;Peso sostituzione impression&quot; del 10%

Poiché la serie di eventi includeva sia impression che clic, il peso di esclusione delle impression si applica alle impression.

Attribuzione: Impression 1 = 8 USD, Click 1 = 72 USD, Impression 2 = 4 USD, Click 2 = 36 USD (120 USD in totale)

#### Utilizzo (solo DSP) di No Impression Override Weight (Peso di sostituzione impression) o (solo Search, Social &amp; Commerce) di un &quot;Impression Override Weight&quot; dello 0%

Poiché la serie di eventi includeva sia impression che clic, le impression vengono ignorate.

Attribuzione: Impression 1 = 0 USD, Click 1 = 80 USD, Impression 2 = 0 USD, Click 2 = 40 USD (120 USD in totale)

### Esempio con tutte le impression

**Nota:** Sono applicabili solo le impression per gli annunci display.

Percorso evento: Impression 1, Impression 2, Impression 3, Conversione di 120 USD

Poiché la conversione è una view-through, per determinare il valore di ciascuna impression viene applicato il metodo di valutazione view-through, anziché il peso di override dell’impression:

* Se il parametro del report specifica un peso view-through ponderato, tale peso viene applicato ai valori delle impression. Ad esempio, se il peso view-through è 40%, allora Impression 1 = 24 USD, Impression 2 = 16 USD, Impression 3 = 8 USD (48 USD totali)

* Se il parametro del rapporto specifica l&#39;utilizzo di valori non elaborati per le visualizzazioni, all&#39;impression non viene applicato alcun peso view-through e l&#39;intero valore di 120 USD viene diviso tra le tre impression: Impression 1 = 60 USD, Impression 2 = 40 USD, Impression 3 = 20 USD (120 USD in totale)

+++

<!-- end examples as collapsible content -->

## Distribuzione uniforme

>[!NOTE]
>
>Questa regola è disponibile solo per gli eventi su singoli dispositivi.

Attribuisce la conversione in modo uguale a ogni evento della serie che si è verificato all&#39;interno del [fai clic sull’intervallo di lookback](/help/search-social-commerce/glossary.md#c-d) e [intervallo di lookback delle impression](/help/search-social-commerce/glossary.md#i-j).

Quando la conversione è preceduta solo da impression, viene considerata una *view-through*, ponderato in base al valore dell&#39;inserzionista [ponderazione view-through](/help/search-social-commerce/glossary.md#uv) oppure, come specificato, in base al metodo di valutazione view-through specificato nei parametri di report, vista o simulazione personalizzata.

Quando il percorso di conversione include sia clic che impression a pagamento, queste vengono trattate in modo diverso dai diversi prodotti di Adobe Advertising:

* In Search, Social e Commerce, il [peso di override impression](/help/search-social-commerce/glossary.md#i-j) , specificato nell&#39;impostazione di peso per la sostituzione delle impression dell&#39;inserzionista e nei parametri di report, visualizzazione o simulazione personalizzata, viene applicato per la prima volta alle impression.

* In DSP, le impression vengono ignorate e solo i clic vengono ponderati. L’DSP non prende in considerazione i pesi di esclusione delle impression per l’attribuzione.

![Percentuali di attribuzione pari](/help/search-social-commerce/assets/attribution-percent-even.png "Percentuali di attribuzione pari")

<!-- start examples as collapsible content -->

+++Esempi di calcolo degli eventi

### Esempio con tutti i clic

Percorso evento: Click 1, Click 2, Click 3, conversione di 120 USD

Nessuna impression ha portato alla conversione, pertanto il peso di sostituzione dell’impression non è applicabile e la conversione è suddivisa equamente tra i tre clic:

Attribuzione: Click 1 = 40 USD, Click 2 = 40 USD, Click 3 = 40 USD (120 USD in totale)

### Esempi con impression e clic

**Nota:** Le impression sono applicabili solo dalla visualizzazione e dagli annunci social.

Percorso evento: Impression 1, Click 1, Impression 2, Click 2, Conversione di 120 USD

#### (Solo per ricerca, social network e commerce) Con l’impostazione predefinita &quot;Peso sostituzione impression&quot; del 10%

Poiché la serie di eventi includeva sia impression che clic, il peso di esclusione delle impression si applica alle impression.

Attribuzione: Impression 1 = 6 USD, Click 1 = 54 USD, Impression 2 = 6 USD, Click 2 = 54 USD (120 USD in totale)

#### Utilizzo (solo per Adobe Advertising DSP) di No Impression Override Weight (Peso di sostituzione impression) o (solo per Search, Social &amp; Commerce) di un &quot;Impression Override Weight&quot; dello 0%

Poiché la serie di eventi includeva sia impression che clic, le impression vengono ignorate.

Attribuzione: Impression 1 = 0 USD, Click 1 = 60 USD, Impression 2 = 0 USD, Click 2 = 60 USD (120 USD in totale)

## Esempio con tutte le impression

**Nota:** Sono applicabili solo le impression per gli annunci display.

Percorso evento: Impression 1, Impression 2, Impression 3, Conversione di 120 USD

Poiché la conversione è una view-through, per determinare il valore di ciascuna impression viene applicato il metodo di valutazione view-through, anziché il peso di override dell’impression:

* Se il parametro del report specifica un peso view-through ponderato, tale peso viene applicato ai valori delle impression. Ad esempio, se il peso view-through è 40%, allora Impression 1 = 16 USD, Impression 2 = 16 USD, Impression 3 = 16 USD (48 USD totali)

* Se il parametro del rapporto specifica l&#39;utilizzo di valori non elaborati per le visualizzazioni, all&#39;impression non viene applicato alcun peso view-through e l&#39;intero valore di 120 USD viene diviso tra le tre impression: Impression 1 = 40 USD, Impression 2 = 40 USD, Impression 3 = 40 USD (120 USD in totale)

+++

<!-- end examples as collapsible content -->

## Spessore ultimo evento Altro

Attribuisce la conversione a tutti gli eventi della serie che si sono verificati all&#39;interno del [fai clic sull’intervallo di lookback](/help/search-social-commerce/glossary.md#c-d) e [intervallo di lookback delle impression](/help/search-social-commerce/glossary.md#i-j), ma attribuisce il maggior peso all’ultimo evento e successivamente meno peso agli eventi precedenti.

Quando la conversione è preceduta solo da impression, viene considerata una *view-through*, ponderato in base al valore dell&#39;inserzionista [ponderazione view-through](/help/search-social-commerce/glossary.md#uv) oppure, come specificato, in base al metodo di valutazione view-through specificato nei parametri di report, vista o simulazione personalizzata.

Quando il percorso di conversione include sia clic che impression a pagamento, queste vengono trattate in modo diverso dai diversi prodotti di Adobe Advertising:

* In Search, Social e Commerce, il [peso di override impression](/help/search-social-commerce/glossary.md#i-j) , specificato nell&#39;impostazione di peso per la sostituzione delle impression dell&#39;inserzionista e nei parametri di report, visualizzazione o simulazione personalizzata, viene applicato per la prima volta alle impression.

* In DSP, le impression vengono ignorate e solo i clic vengono ponderati. L’DSP non prende in considerazione i pesi di esclusione delle impression per l’attribuzione.

![Peso dell’ultimo evento più percentuali di attribuzione](/help/search-social-commerce/assets/attribution-percent-weight-last-more.png "Peso dell’ultimo evento più percentuali di attribuzione")

<!-- start examples as collapsible content -->

+++Esempi di calcolo degli eventi

### Esempio con tutti i clic

Percorso evento: Click 1, Click 2, Click 3, Conversione di 120 USD

Attribuzione: Click 3 = 60 USD, Click 2 = 40 USD, Click 1 = 20 USD (120 USD in totale)

### Esempi con impression e clic

**Nota:** Le impression sono applicabili solo dalla visualizzazione e dagli annunci social.

Percorso evento: Impression 1, Click 1, Impression 2, Click 2, Conversione di 120 USD

#### (Solo per ricerca, social network e commerce) Con l’impostazione predefinita &quot;Peso sostituzione impression&quot; del 10%

Poiché la serie di eventi includeva sia impression che clic, il peso di esclusione delle impression si applica alle impression.

Attribuzione: Impression 1 = 4 USD, Click 1 = 36 USD, Impression 2 = 8 USD, Click 2 = 72 USD (120 USD in totale)

#### Utilizzo (solo DSP) di No Impression Override Weight (Peso di sostituzione impression) o (solo Search, Social &amp; Commerce) di un &quot;Impression Override Weight&quot; dello 0%

Poiché la serie di eventi includeva sia impression che clic, le impression vengono ignorate.

Attribuzione: Impression 1 = 0 USD, Click 1 = 40 USD, Impression 2 = 0 USD, Click 2 = 80 USD (120 USD in totale)

### Esempio con tutte le impression

**Nota:** Le impression sono applicabili solo dalla visualizzazione e dagli annunci social.

Percorso evento: Impression 1, Impression 2, Impression 3, Conversione di 120 USD

Poiché la conversione è una view-through, per determinare il valore di ciascuna impression viene applicato il metodo di valutazione view-through, anziché il peso di override dell’impression:

* Se il parametro del report specifica un peso view-through ponderato, tale peso viene applicato ai valori delle impression. Ad esempio, se il peso view-through è 40%, moltiplica ogni valore nell’esempio con tutti i clic per 40%: Impressione 3 = 24 USD, Impressione 2 = 16 USD, Impressione 1 = 8 USD (48 USD totali)

* Se il parametro del rapporto specifica l’utilizzo di valori non elaborati per le visite, l’intero importo di 120 USD viene diviso tra le impression: Impressione 3 = 60 USD, Impressione 2 = 40 USD, Impressione 1 = 20 USD (120 USD in totale)

+++

<!-- end examples as collapsible content -->

## A forma di U

Attribuisce la conversione a tutti gli eventi della serie che si sono verificati all&#39;interno del [fai clic sull’intervallo di lookback](/help/search-social-commerce/glossary.md#c-d) e [intervallo di lookback delle impression](/help/search-social-commerce/glossary.md#i-j), ma attribuisce il maggior peso al primo evento e agli ultimi eventi, con un peso progressivamente inferiore agli eventi che si trovano nel mezzo del percorso di conversione.

Quando la conversione è preceduta solo da impression, viene considerata una *view-through*, ponderato in base al valore dell&#39;inserzionista [ponderazione view-through](/help/search-social-commerce/glossary.md#uv) oppure, come specificato, in base al metodo di valutazione view-through specificato nei parametri di report, vista o simulazione personalizzata.

Quando il percorso di conversione include sia clic che impression a pagamento, queste vengono trattate in modo diverso dai diversi prodotti di Adobe Advertising:

* In Search, Social e Commerce, il [peso di override impression](/help/search-social-commerce/glossary.md#i-j) , specificato nell&#39;impostazione di peso per la sostituzione delle impression dell&#39;inserzionista e nei parametri di report, visualizzazione o simulazione personalizzata, viene applicato per la prima volta alle impression.

* In DSP, le impression vengono ignorate e solo i clic vengono ponderati. L’DSP non prende in considerazione i pesi di esclusione delle impression per l’attribuzione.

![Percentuali di attribuzione a forma di U](/help/search-social-commerce/assets/attribution-percent-u-shaped.png "Percentuali di attribuzione a forma di U")

<!-- start examples as collapsible content -->

+++Esempi di calcolo degli eventi

### Esempio con tutti i clic

Percorso evento: Click 1, Click 2, Click 3, Click 4, Conversione di 120 USD

Attribuzione: Click 1 = 36 USD, Click 2 = 24 USD, Click 3 = 24 USD, Click 4 = 36 USD (120 USD in totale)

### Esempi con impression e clic

**Nota:** Le impression sono applicabili solo dalla visualizzazione e dagli annunci social.

Percorso evento: Impression 1, Click 1, Impression 2, Click 2, Conversione di 120 USD

#### (Solo per ricerca, social network e commerce) Con l’impostazione predefinita &quot;Peso sostituzione impression&quot; del 10%

Poiché la serie di eventi includeva sia impression che clic, il peso di esclusione delle impression si applica alle impression.

Attribuzione: Impression 1 = 6 USD, Click 1 = 54 USD, Impression 2 = 6 USD, Click 2 = 54 USD (120 USD in totale)

#### Utilizzo (solo DSP) di nessun peso di override delle impression o (solo per Search, Social &amp; Commerce) di un &quot;peso di override delle impression&quot; dello 0%

Poiché la serie di eventi includeva sia impression che clic, le impression vengono ignorate.

Attribuzione: Impression 1 = 0 USD, Click 1 = 60 USD, Impression 2 = 0 USD, Click 2 = 60 USD (120 USD in totale)

### Esempio con tutte le impression

**Nota:** Sono applicabili solo le impression per gli annunci display.

Percorso evento: Impression 1, Impression 2, Impression 3, Impression 4, Conversione di 120 USD

Poiché la conversione è una view-through, per determinare il valore di ciascuna impression viene applicato il metodo di valutazione view-through, anziché il peso di override dell’impression:

* Se il parametro del report specifica un peso view-through ponderato, tale peso viene applicato ai valori delle impression. Ad esempio, se il peso view-through è 40%, fare clic su 1 = 14,40 USD, fare clic su 2 = 9,60 USD, fare clic su 3 = 9,60 USD, fare clic su 4 = 14,40 USD (48 USD totali)

* Se il parametro del rapporto specifica l&#39;utilizzo di valori non elaborati per le visite, l&#39;intero valore di 120 USD viene diviso tra le impression: Fare clic su 1 = 36 USD, Fare clic su 2 = 24 USD, Fare clic su 3 = 24 USD, Fare clic su 4 = 36 USD (120 USD in totale)

+++

<!-- end examples as collapsible content -->
