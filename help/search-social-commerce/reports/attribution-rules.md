---
title: Calcolo delle regole di attribuzione
description: Scopri come Adobe Advertising calcola ogni tipo di regola di attribuzione.
exl-id: 15beeadd-bb65-4efe-8c4f-34c4a48cc775
feature: Search Reports, DSP Custom Reports
source-git-commit: 513d81cf835ccbffa16581799f0dc8306681e3ad
workflow-type: tm+mt
source-wordcount: '2711'
ht-degree: 0%

---

# Calcolo delle regole di attribuzione per Adobe Advertising

*Inserzionisti con solo monitoraggio delle conversioni di Adobe Advertising*

<!-- Verify statements about cross-device events -->

La regola di attribuzione a livello di inserzionista viene utilizzata per attribuire i dati di conversione, potenzialmente tra più canali di annunci, in una serie di eventi che portano a una conversione.

Puoi anche selezionare una regola di attribuzione nelle seguenti posizioni per applicarla solo ai dati risultanti:

* DSP

   * Rapporti personalizzati con attribuzione multi-touch

* Ricerca, social e Commerce

   * Rapporti personalizzati

   * Visualizzazioni predefinite e personalizzate

   * (Alcuni ruoli utente) Simulazioni a livello di Portfolio.

>[!NOTE]
>
>* Le regole di attribuzione si applicano ai clic sugli annunci a pagamento in qualsiasi canale e alle impression sulla visualizzazione e sugli annunci social. Non si applicano alle impression per gli annunci di ricerca a pagamento, che non possono essere tracciati a livello di evento.
>* Adobe Advertising memorizza sempre i seguenti eventi per ogni web surfer prima di una conversione: a) il primo clic a pagamento; b) fino a 10 clic per ogni canale (ricerca, social o visualizzazione), incluso il primo clic; e c) fino a 10 impression di visualizzazione.<!-- But it can continue to attribute conversions to clicks and impressions for longer. -->
>* In Advertising DSP e Advertising Creative, le definizioni multi-dispositivo considerano solo il percorso dell&#39;evento dalla regola di attribuzione selezionata.<!-- cross-device attribution via LiveRamp only -->
>* Nei rapporti e nelle viste di gestione, il numero di posizioni decimali visualizzate per un valore dipende dalla valuta, ma Adobe Advertising memorizza valori più precisi.

## Ultimo evento (impostazione predefinita)

Attribuisce la conversione all&#39;ultimo clic a pagamento nella serie all&#39;interno dell&#39;[intervallo di lookback su clic](/help/search-social-commerce/glossary.md#c-d) dell&#39;inserzionista o, se non si è verificato alcun clic a pagamento, all&#39;ultima impression all&#39;interno dell&#39;[intervallo di lookback su impression](/help/search-social-commerce/glossary.md#i-j) dell&#39;inserzionista.

Quando la conversione è preceduta solo dalle impression, viene considerata una *view-through*, ponderata in base all&#39;impostazione di ponderazione [view-through](/help/search-social-commerce/glossary.md#uv) dell&#39;inserzionista o, come specificato, in base al metodo di valutazione view-through specificato nei parametri di report, visualizzazione o simulazione personalizzata.

![Percentuali di attribuzione ultimo evento](/help/search-social-commerce/assets/attribution-percent-last-event.png "Percentuali di attribuzione ultimo evento")

<!-- start examples as collapsible content -->

+++Esempi di calcoli di eventi

### Esempio con tutti i clic

Percorso evento: Click1, Click2, Click3, Conversione di 120 USD

La conversione è attribuita al Click 3 per un importo di 120 USD.

### Esempio con impression e clic

**Nota:** le impression sono applicabili solo dagli annunci display e social.

Percorso evento: impression 1, click 1, impression 2, conversione da 120 USD

La conversione è attribuita al Click 1 per un importo di 120 USD.

### Esempio con tutte le impression

**Nota:** sono applicabili solo le impression per la visualizzazione e gli annunci social.

Percorso evento: Impression 1, Impression 2, Impression 3, Conversione di 120 USD

La conversione è attribuita all’impression 3. Poiché la conversione è una view-through, viene applicato il metodo di valutazione view-through selezionato nella sezione &quot;Attribuzione conversione&quot; delle impostazioni del rapporto:

* Se il parametro report specifica un peso di visualizzazione ponderato, tale peso viene applicato al view-through. Ad esempio, se il peso view-through dell’inserzionista è 40%, allora 120 USD x 40% = 48 USD, quindi 48 USD è attribuito a Impression 3.

* Se il parametro del report specifica l&#39;utilizzo di valori non elaborati per le visite, non viene applicato alcun peso di visualizzazione e l&#39;intero valore di 120 USD viene attribuito all&#39;impression 3.

+++

<!-- end examples as collapsible content -->

## Primo evento

Attribuisce la conversione al primo clic a pagamento della serie nell&#39;intervallo di lookback [click](/help/search-social-commerce/glossary.md#c-d) dell&#39;inserzionista o, se non si è verificato alcun clic a pagamento, alla prima impression nell&#39;[intervallo di lookback impression](/help/search-social-commerce/glossary.md#i-j) dell&#39;inserzionista. Questa regola è disponibile solo per gli eventi su singoli dispositivi.

Quando la conversione è preceduta solo dalle impression, viene considerata una *view-through*, ponderata in base all&#39;impostazione di ponderazione [view-through](/help/search-social-commerce/glossary.md#uv) dell&#39;inserzionista o, come specificato, in base al metodo di valutazione view-through specificato nei parametri di report, visualizzazione o simulazione personalizzata.

![Percentuali di attribuzione primo evento](/help/search-social-commerce/assets/attribution-percent-first-event.png "Percentuali di attribuzione primo evento")

<!-- start examples as collapsible content -->

+++Esempi di calcoli di eventi

### Esempio con tutti i clic

Percorso evento: Click 1, Click 2, Click 3, Conversione di 120 USD

La conversione è attribuita al Click 1 per un importo di 120 USD.

### Esempio con impression e clic

**Nota:** le impression sono applicabili solo dagli annunci display e social.

Percorso evento: impression 1, click 1, impression 2, conversione da 120 USD

La conversione è attribuita al Click 1 per un importo di 120 USD.

### Esempio con tutte le impression

**Nota:** sono applicabili solo le impression per la visualizzazione e gli annunci social.

Percorso evento: Impression 1, Impression 2, Impression 3, Conversione di 120 USD

La conversione è attribuita all’impression 1. Poiché la conversione è una view-through, il metodo di valutazione view-through selezionato in &quot;Conversione (campagne di visualizzazione)&quot;
Viene applicata la sezione &quot;Attribution&quot; delle impostazioni del rapporto:

* Se il parametro report specifica un peso di visualizzazione ponderato, tale peso viene applicato al view-through. Ad esempio, se il peso view-through dell’inserzionista è 40%, allora 120 x 40% = 48 USD, quindi 48 USD è attribuito a Impression 1.

* Se il parametro del report specifica l&#39;utilizzo di valori non elaborati per le visite, non viene applicato alcun peso di visualizzazione e l&#39;intero valore di 120 USD viene attribuito all&#39;impression 1.

+++

<!-- end examples as collapsible content -->

## Spessore primo evento Altro

Attribuisce la conversione a tutti gli eventi della serie che si sono verificati nell&#39;[intervallo di lookback su clic](/help/search-social-commerce/glossary.md#c-d) e nell&#39;[intervallo di lookback su impression](/help/search-social-commerce/glossary.md#i-j) dell&#39;inserzionista, ma attribuisce maggior peso al primo evento e successivamente meno peso ai seguenti eventi. Questa regola è disponibile solo per gli eventi su singoli dispositivi.

Quando la conversione è preceduta solo dalle impression, viene considerata una *view-through*, ponderata in base all&#39;impostazione di ponderazione [view-through](/help/search-social-commerce/glossary.md#uv) dell&#39;inserzionista o, come specificato, in base al metodo di valutazione view-through specificato nei parametri di report, visualizzazione o simulazione personalizzata.

Quando il percorso di conversione include sia clic che impression a pagamento, queste vengono trattate in modo diverso dai diversi prodotti Adobe Advertising:

* In Search, Social e Commerce, il peso di sostituzione [impression](/help/search-social-commerce/glossary.md#i-j), specificato nell&#39;impostazione del peso di sostituzione impression dell&#39;inserzionista e nei parametri di report, visualizzazione o simulazione personalizzata, viene applicato per la prima volta alle impression.

* In DSP, le impression vengono ignorate e vengono ponderati solo i clic. DSP non prende in considerazione i pesi di override delle impression per l’attribuzione.

![Peso del primo evento più percentuali di attribuzione](/help/search-social-commerce/assets/attribution-percent-weight-first-more.png "Peso del primo evento più percentuali di attribuzione")

<!-- start examples as collapsible content -->

+++Esempi di calcoli di eventi

### Esempio con tutti i clic

Percorso evento: Click 1, Click 2, Click 3, Conversione di 120 USD

Attribuzione: Click 1 = 60 USD, Click 2 = 40 USD, Click 3 = 20 USD (120 USD in totale)

### Esempi con impression e clic

**Nota:** le impression sono applicabili solo dagli annunci display e social.

Percorso evento: Impression 1, Click 1, Impression 2, Click 2, Conversione di 120 USD

#### (Solo per ricerca, social network e Commerce) Con &quot;Peso sostituzione impression&quot; predefinito del 10%

Poiché la serie di eventi includeva sia impression che clic, il peso di esclusione delle impression si applica alle impression.

Attribuzione: Impression 1 = 8 USD, Click 1 = 72 USD, Impression 2 = 4 USD, Click 2 = 36 USD (120 USD in totale)

#### Utilizzo (solo DSP) di No Impression Override Weight o (solo Search, Social &amp; Commerce) di un &quot;Impression Override Weight&quot; dello 0%

Poiché la serie di eventi includeva sia impression che clic, le impression vengono ignorate.

Attribuzione: Impression 1 = 0 USD, Click 1 = 80 USD, Impression 2 = 0 USD, Click 2 = 40 USD (120 USD in totale)

### Esempio con tutte le impression

**Nota:** sono applicabili solo le impression per gli annunci di visualizzazione.

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

Attribuisce la conversione in modo uguale a ogni evento della serie che si è verificato all&#39;interno dell&#39;[intervallo di lookback su clic](/help/search-social-commerce/glossary.md#c-d) e dell&#39;[intervallo di lookback su impression](/help/search-social-commerce/glossary.md#i-j) dell&#39;inserzionista.

Quando la conversione è preceduta solo dalle impression, viene considerata una *view-through*, ponderata in base all&#39;impostazione di ponderazione [view-through](/help/search-social-commerce/glossary.md#uv) dell&#39;inserzionista o, come specificato, in base al metodo di valutazione view-through specificato nei parametri di report, visualizzazione o simulazione personalizzata.

Quando il percorso di conversione include sia clic che impression a pagamento, queste vengono trattate in modo diverso dai diversi prodotti Adobe Advertising:

* In Search, Social e Commerce, il peso di sostituzione [impression](/help/search-social-commerce/glossary.md#i-j), specificato nell&#39;impostazione del peso di sostituzione impression dell&#39;inserzionista e nei parametri di report, visualizzazione o simulazione personalizzata, viene applicato per la prima volta alle impression.

* In DSP, le impression vengono ignorate e vengono ponderati solo i clic. DSP non prende in considerazione i pesi di override delle impression per l’attribuzione.

![Percentuali di attribuzione pari](/help/search-social-commerce/assets/attribution-percent-even.png "Percentuali di attribuzione pari")

<!-- start examples as collapsible content -->

+++Esempi di calcoli di eventi

### Esempio con tutti i clic

Percorso evento: Click 1, Click 2, Click 3, conversione di 120 USD

Nessuna impression ha portato alla conversione, pertanto il peso di sostituzione dell’impression non è applicabile e la conversione è suddivisa equamente tra i tre clic:

Attribuzione: Click 1 = 40 USD, Click 2 = 40 USD, Click 3 = 40 USD (120 USD in totale)

### Esempi con impression e clic

**Nota:** le impression sono applicabili solo dagli annunci display e social.

Percorso evento: Impression 1, Click 1, Impression 2, Click 2, Conversione di 120 USD

#### (Solo per ricerca, social network e Commerce) Con &quot;Peso sostituzione impression&quot; predefinito del 10%

Poiché la serie di eventi includeva sia impression che clic, il peso di esclusione delle impression si applica alle impression.

Attribuzione: Impression 1 = 6 USD, Click 1 = 54 USD, Impression 2 = 6 USD, Click 2 = 54 USD (120 USD in totale)

#### Utilizzo (solo Adobe Advertising DSP) di No Impression Override Weight (Peso di sostituzione impression) o (solo Search, Social &amp; Commerce) di un &quot;Impression Override Weight&quot; dello 0%

Poiché la serie di eventi includeva sia impression che clic, le impression vengono ignorate.

Attribuzione: Impression 1 = 0 USD, Click 1 = 60 USD, Impression 2 = 0 USD, Click 2 = 60 USD (120 USD in totale)

## Esempio con tutte le impression

**Nota:** sono applicabili solo le impression per gli annunci di visualizzazione.

Percorso evento: Impression 1, Impression 2, Impression 3, Conversione di 120 USD

Poiché la conversione è una view-through, per determinare il valore di ciascuna impression viene applicato il metodo di valutazione view-through, anziché il peso di override dell’impression:

* Se il parametro del report specifica un peso view-through ponderato, tale peso viene applicato ai valori delle impression. Ad esempio, se il peso view-through è 40%, allora Impression 1 = 16 USD, Impression 2 = 16 USD, Impression 3 = 16 USD (48 USD totali)

* Se il parametro del rapporto specifica l&#39;utilizzo di valori non elaborati per le visualizzazioni, all&#39;impression non viene applicato alcun peso view-through e l&#39;intero valore di 120 USD viene diviso tra le tre impression: Impression 1 = 40 USD, Impression 2 = 40 USD, Impression 3 = 40 USD (120 USD in totale)

+++

<!-- end examples as collapsible content -->

## Spessore ultimo evento Altro

Attribuisce la conversione a tutti gli eventi della serie che si sono verificati nell&#39;[intervallo di lookback su clic](/help/search-social-commerce/glossary.md#c-d) e nell&#39;[intervallo di lookback su impression](/help/search-social-commerce/glossary.md#i-j) dell&#39;inserzionista, ma attribuisce il massimo peso all&#39;ultimo evento e successivamente meno peso agli eventi precedenti.

Quando la conversione è preceduta solo dalle impression, viene considerata una *view-through*, ponderata in base all&#39;impostazione di ponderazione [view-through](/help/search-social-commerce/glossary.md#uv) dell&#39;inserzionista o, come specificato, in base al metodo di valutazione view-through specificato nei parametri di report, visualizzazione o simulazione personalizzata.

Quando il percorso di conversione include sia clic che impression a pagamento, queste vengono trattate in modo diverso dai diversi prodotti Adobe Advertising:

* In Search, Social e Commerce, il peso di sostituzione [impression](/help/search-social-commerce/glossary.md#i-j), specificato nell&#39;impostazione del peso di sostituzione impression dell&#39;inserzionista e nei parametri di report, visualizzazione o simulazione personalizzata, viene applicato per la prima volta alle impression.

* In DSP, le impression vengono ignorate e vengono ponderati solo i clic. DSP non prende in considerazione i pesi di override delle impression per l’attribuzione.

![Peso dell&#39;ultimo evento più percentuali di attribuzione](/help/search-social-commerce/assets/attribution-percent-weight-last-more.png "Peso dell&#39;ultimo evento più percentuali di attribuzione")

<!-- start examples as collapsible content -->

+++Esempi di calcoli di eventi

### Esempio con tutti i clic

Percorso evento: Click 1, Click 2, Click 3, Conversione di 120 USD

Attribuzione: Click 3 = 60 USD, Click 2 = 40 USD, Click 1 = 20 USD (120 USD in totale)

### Esempi con impression e clic

**Nota:** le impression sono applicabili solo dagli annunci display e social.

Percorso evento: Impression 1, Click 1, Impression 2, Click 2, Conversione di 120 USD

#### (Solo per ricerca, social network e Commerce) Con &quot;Peso sostituzione impression&quot; predefinito del 10%

Poiché la serie di eventi includeva sia impression che clic, il peso di esclusione delle impression si applica alle impression.

Attribuzione: Impression 1 = 4 USD, Click 1 = 36 USD, Impression 2 = 8 USD, Click 2 = 72 USD (120 USD in totale)

#### Utilizzo (solo DSP) di No Impression Override Weight o (solo Search, Social &amp; Commerce) di un &quot;Impression Override Weight&quot; dello 0%

Poiché la serie di eventi includeva sia impression che clic, le impression vengono ignorate.

Attribuzione: Impression 1 = 0 USD, Click 1 = 40 USD, Impression 2 = 0 USD, Click 2 = 80 USD (120 USD in totale)

### Esempio con tutte le impression

**Nota:** le impression sono applicabili solo dagli annunci display e social.

Percorso evento: Impression 1, Impression 2, Impression 3, Conversione di 120 USD

Poiché la conversione è una view-through, per determinare il valore di ciascuna impression viene applicato il metodo di valutazione view-through, anziché il peso di override dell’impression:

* Se il parametro del report specifica un peso view-through ponderato, tale peso viene applicato ai valori delle impression. Ad esempio, se il peso view-through è 40%, moltiplica ogni valore nell’esempio con tutti i clic per 40%: Impressione 3 = 24 USD, Impressione 2 = 16 USD, Impressione 1 = 8 USD (48 USD totali)

* Se il parametro del rapporto specifica l’utilizzo di valori non elaborati per le visite, l’intero importo di 120 USD viene diviso tra le impression: Impressione 3 = 60 USD, Impressione 2 = 40 USD, Impressione 1 = 20 USD (120 USD in totale)

+++

<!-- end examples as collapsible content -->

## A forma di U

Attribuisce la conversione a tutti gli eventi della serie che si sono verificati nell&#39;[intervallo di lookback su clic](/help/search-social-commerce/glossary.md#c-d) e nell&#39;[intervallo di lookback su impression](/help/search-social-commerce/glossary.md#i-j) dell&#39;inserzionista, ma attribuisce il massimo peso al primo evento e agli ultimi eventi, con un peso progressivamente inferiore agli eventi che si sono verificati al centro del percorso di conversione.

Quando la conversione è preceduta solo dalle impression, viene considerata una *view-through*, ponderata in base all&#39;impostazione di ponderazione [view-through](/help/search-social-commerce/glossary.md#uv) dell&#39;inserzionista o, come specificato, in base al metodo di valutazione view-through specificato nei parametri di report, visualizzazione o simulazione personalizzata.

Quando il percorso di conversione include sia clic che impression a pagamento, queste vengono trattate in modo diverso dai diversi prodotti Adobe Advertising:

* In Search, Social e Commerce, il peso di sostituzione [impression](/help/search-social-commerce/glossary.md#i-j), specificato nell&#39;impostazione del peso di sostituzione impression dell&#39;inserzionista e nei parametri di report, visualizzazione o simulazione personalizzata, viene applicato per la prima volta alle impression.

* In DSP, le impression vengono ignorate e vengono ponderati solo i clic. DSP non prende in considerazione i pesi di override delle impression per l’attribuzione.

![U percentuali di attribuzione](/help/search-social-commerce/assets/attribution-percent-u-shaped.png "U percentuali di attribuzione")

<!-- start examples as collapsible content -->

+++Esempi di calcoli di eventi

### Esempio con tutti i clic

Percorso evento: Click 1, Click 2, Click 3, Click 4, Conversione di 120 USD

Attribuzione: Click 1 = 36 USD, Click 2 = 24 USD, Click 3 = 24 USD, Click 4 = 36 USD (120 USD in totale)

### Esempi con impression e clic

**Nota:** le impression sono applicabili solo dagli annunci display e social.

Percorso evento: Impression 1, Click 1, Impression 2, Click 2, Conversione di 120 USD

#### (Solo per ricerca, social network e Commerce) Con &quot;Peso sostituzione impression&quot; predefinito del 10%

Poiché la serie di eventi includeva sia impression che clic, il peso di esclusione delle impression si applica alle impression.

Attribuzione: Impression 1 = 6 USD, Click 1 = 54 USD, Impression 2 = 6 USD, Click 2 = 54 USD (120 USD in totale)

#### Utilizzo di (solo DSP) senza sovrapposizione impression o (solo Search, Social e Commerce) un &quot;Peso di sostituzione impression&quot; dello 0%

Poiché la serie di eventi includeva sia impression che clic, le impression vengono ignorate.

Attribuzione: Impression 1 = 0 USD, Click 1 = 60 USD, Impression 2 = 0 USD, Click 2 = 60 USD (120 USD in totale)

### Esempio con tutte le impression

**Nota:** sono applicabili solo le impression per gli annunci di visualizzazione.

Percorso evento: Impression 1, Impression 2, Impression 3, Impression 4, Conversione di 120 USD

Poiché la conversione è una view-through, per determinare il valore di ciascuna impression viene applicato il metodo di valutazione view-through, anziché il peso di override dell’impression:

* Se il parametro del report specifica un peso view-through ponderato, tale peso viene applicato ai valori delle impression. Ad esempio, se il peso view-through è 40%, fare clic su 1 = 14,40 USD, fare clic su 2 = 9,60 USD, fare clic su 3 = 9,60 USD, fare clic su 4 = 14,40 USD (48 USD totali)

* Se il parametro del rapporto specifica l&#39;utilizzo di valori non elaborati per le visite, l&#39;intero valore di 120 USD viene diviso tra le impression: Fare clic su 1 = 36 USD, Fare clic su 2 = 24 USD, Fare clic su 3 = 24 USD, Fare clic su 4 = 36 USD (120 USD in totale)

+++

<!-- end examples as collapsible content -->
