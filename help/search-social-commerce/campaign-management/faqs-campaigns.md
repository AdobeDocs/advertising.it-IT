---
title: Domande frequenti sulle campagne
description: Vedi le risposte alle domande sulla gestione delle campagne e sulle visualizzazioni dati delle campagne.
exl-id: 999e5aba-f556-4b34-bb92-5931d5e0dd72
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '1585'
ht-degree: 0%

---

# Domande frequenti sulla gestione delle campagne

## Informazioni generali

+++Posso spostare campagne e componenti da un account all’altro?

Non spostare o copiare una campagna o un componente della campagna con un ID univoco in un account con un ID account diverso. Questa operazione genera errori di dati.
+++

+++Quando i dati dei clic vengono aggiornati dalle reti di annunci?

Il processo di estrazione dei dati di clic del giorno precedente dai motori di ricerca inizia alle 06:00 nel fuso orario dell’inserzionista.

Inoltre, [!DNL Google Ads] le metriche delle prestazioni a livello di campagna sulla rete di ricerca per il giorno corrente vengono richiamate alle 08:00 e alle 16:00 nel fuso orario dell’inserzionista.
+++

+++Quali azioni causano la perdita di cronologia di parole chiave e annunci?

>[!NOTE]
>
>(Inserzionisti con portfolio) Le prestazioni delle nuove combinazioni di parole chiave e tipi di corrispondenza saranno volatili, mentre Search, Social e Commerce raccolgono i dati per creare modelli per loro.

**Azioni in [!UICONTROL Search] > [!UICONTROL Campaigns] visualizzazioni, nel processo di pubblicazione di bulksheet e nell’editor proprio della rete di annunci:**

La parola chiave o l’annuncio esistente viene eliminato e ne viene creato un altro quando:

* ([!DNL Baidu], [!DNL Google Ads], e [!DNL Yandex]a) È possibile modificare il nome di una parola chiave.

* ([!DNL Google Ads], [!DNL Microsoft Advertising], e [!DNL Yandex]a) È possibile modificare il tipo di corrispondenza di una parola chiave.

* Sposti una parola chiave tra gruppi di annunci.

* ([!DNL Google Ads] annunci di ricerca dinamica, [!DNL Microsoft Advertising] annunci di testo espansi e tutti i tipi di annunci su altre reti pubblicitarie supportate) Puoi modificare un annuncio copiato (titolo/titolo o descrizione) o un’immagine pubblicitaria.

* Sposti un annuncio tra gruppi di annunci.

**Eventi nel processo di registrazione dei feed inventario prodotti:**

Un annuncio o una parola chiave esistente viene eliminata e ne viene creata un’altra quando:

* Un file di feed contiene un nuovo valore per una colonna utilizzata in una variante di annuncio.

* Le impostazioni del modello per un annuncio sono state modificate dopo l’ultima propagazione.

* Un nuovo file di feed include una riga per un annuncio o una parola chiave che a) si trovava in un file precedente ma b) da allora è stato omesso ed è stato messo in pausa o eliminato in base alle impostazioni dei dati di feed.

A seconda della [impostazioni dei dati di feed](/help/search-social-commerce/campaign-management/inventory-feeds/feed-settings-manage.md#feed-data-settings), un annuncio o una parola chiave esistente può essere eliminato quando:

* Un nuovo file di feed non include una riga per un annuncio o una parola chiave esistente.

* La data di fine pianificata per i componenti di un file di feed pubblicato si verifica.

* Il livello di stock di un elemento scende al di sotto di un minimo specificato nelle impostazioni dei dati di feed.
+++

+++([!DNL Google Ads] campagne) Modifiche ai nomi visualizzati per il mio [!DNL Google]Le conversioni tracciate da sono state ripristinate.

Se modifichi i nomi visualizzati delle metriche di conversione in Search, Social e Commerce, le modifiche vengono sovrascritte con i nomi configurati in [!DNL Google Ads]. Apporta le modifiche al nome in [!DNL Google Ads].
+++

+++(campagne Google Ads) Posso utilizzare un budget condiviso per le campagne nei portfolio?

Per risultati migliori, non aggiungere [!DNL Google Ads] campagne a un [!DNL Google Ads] budget condiviso se si trovano in portfolio ottimizzati configurati per &quot;[!UICONTROL Auto adjust campaign budget limits].&quot; In caso affermativo, [!DNL Google Ads] sostituisce i budget per campagne ottimizzati per Search, Social e Commerce, il che potrebbe causare inefficienze nelle offerte.
+++

+++([!DNL Google Ads] Campagne ) Posso inviare utenti mobili e non mobili a pagine di destinazione diverse?

È possibile utilizzare [!DNL Google Ads] [!DNL ValueTrack] parametri `{ifmobile}` e `{ifnotmobile}` per determinare il nome di dominio della pagina di destinazione in uno dei due modi seguenti, a seconda del sito:

* Includi la designazione mobile come server host utilizzando `{ifmobile:m}{ifnotmobile:www}`.

  Ad esempio: `http://{ifmobile:m}{ifnotmobile:www}.example.com` porta gli utenti mobili su m.example.com e gli utenti non mobili su www.example.com.

* Includi la designazione mobile come dominio di primo livello utilizzando `{ifmobile:mobi}{ifnotmobile:com}`.

  Ad esempio: `http://www.example.{ifmobile:mobi}{ifnotmobile:com}` porta gli utenti mobili su www.example.mobi e gli utenti non mobili su www.example.com.

In entrambi i casi, gli URL di base con tracking di Search, Social e Commerce includono il non codificato `{}` ed eventuali parametri aggiuntivi aggiunti all’URL di base.

>[!NOTE]
>
>Non utilizzare un URL completo come valore per i parametri ifnotmobile e ifmobile; utilizza solo la parte variabile dell’URL (ad esempio &quot;m&quot; rispetto a &quot;www&quot;, &quot;mobi&quot; rispetto a &quot;com&quot;).

+++

+++([!DNL Google Ads] campagne nella rete di ricerca) Per quali dati viene visualizzato oggi?

[!DNL Google Ads] le metriche delle prestazioni a livello di campagna sulla rete di ricerca per il giorno corrente vengono richiamate alle 08:00 e alle 16:00 nel fuso orario dell’inserzionista.

In [!UICONTROL Campaigns] in entrambi i [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] e [!UICONTROL Optimization] > [!UICONTROL Portfolios] visualizzazione, quando si crea un rapporto [!UICONTROL Today] Per un intervallo di date personalizzato che include il giorno corrente, i dati includono quelli sincronizzati più di recente.

>[!NOTE]
>
>I dati per clic, impression e conversioni vengono ritardati di tre ore e non sono completi fino al successivo recupero dei dati.

+++

+++Qual è la differenza tra un modello di tracciamento e un suffisso di pagina di destinazione?

Utilizza un suffisso per la pagina di destinazione solo per le reti di annunci che supportano il tracciamento parallelo. In Search, Social e Commerce, i modelli di tracciamento e i suffissi delle pagine di destinazione devono includere un identificatore di clic dalla rete dell’annuncio, ma i modelli di tracciamento includono parametri di tracciamento aggiuntivi.

Consulta le prossime domande frequenti su [supporto del tracciamento parallelo](#parallel-tracking) per ulteriori informazioni su come vengono caricati i modelli di tracciamento e i suffissi delle pagine di destinazione quando un utente fa clic su un annuncio.

+++

+++([!DNL Google Ads] e [!DNL Microsoft Advertising]) Search, Social e Commerce supportano il tracciamento parallelo per gli annunci in [!DNL Google Ads] o [!DNL Microsoft Advertising]? {#parallel-tracking}

Il tracciamento parallelo invia i clienti direttamente dall’annuncio all’URL finale, che può includere parametri aggiunti da un suffisso URL finale o &quot;suffisso pagina di destinazione&quot;. L’URL del modello di tracciamento (con parametri aggiuntivi per la misurazione dei clic) viene caricato separatamente in background; di conseguenza, la pagina di destinazione viene caricata più rapidamente.

Search, Social e Commerce supportano il tracciamento parallelo per le campagne di ricerca e shopping utilizzando l’identificatore di clic della rete di annunci (`msclkid` per [!DNL Microsoft Advertising]; `gclid` per [!DNL Google Ads]). Utilizza un [a livello account](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md#account-settings) o [a livello di campagna](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md) [!UICONTROL Landing Page Suffix] (denominato &quot;[!DNL final URL suffix]&quot; nelle reti di annunci), che viene aggiunto agli URL della pagina di destinazione per tenere traccia dei clic sugli annunci secondari dai browser che supportano il tracciamento parallelo. Consulta la [formati di suffisso richiesti per [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) e [formati di suffisso richiesti per [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

Quando un utente visualizza l’annuncio su un browser che non supporta il tracciamento parallelo, la rete di annunci utilizza invece il tracciamento sequenziale: i clienti vengono inizialmente inviati all’URL del modello di tracciamento, che può reindirizzare i clienti ai server di tracciamento intermedi prima di reindirizzarli all’URL finale (che può includere parametri aggiuntivi nel suffisso di una pagina di destinazione). Tutti i modelli di tracciamento per un account di rete di annunci devono includere lo stesso parametro dell’identificatore di clic utilizzato nella [!UICONTROL Landing Page Suffix]. Consulta la [formati dei modelli di tracciamento per [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) e [formati dei modelli di tracciamento per [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).
+++

+++Perché gli URL di tracciamento dei miei annunci includono &quot;`&EV_HASH={<hash>}`?&quot;

Quando effettui il caricamento utilizzando una [feed inventario prodotto](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) per un account con reindirizzamento pixel di Search, Social e Commerce e con tracciamento a livello di parola chiave e creatività, Search, Social e Commerce aggiungono il parametro e il valore hash al modello di tracciamento dell’annuncio o all’URL di destinazione per identificare che è stato creato utilizzando la funzione di feed inventario.
+++

## Feed inventario

+++(Feed inventario prodotti) Devo mettere in pausa o eliminare gli annunci obsoleti o relativi a un prodotto il cui livello di scorte è inferiore a un determinato minimo?

Dipende dai requisiti aziendali dell&#39;inserzionista.

Quando sospendi gli annunci, questi vengono riattivati se invii nuovamente lo stesso annuncio o se il livello delle scorte supera il minimo consentito. Questo ti consente di conservare la cronologia dell’annuncio.

Quando elimini gli annunci e li invii nuovamente, vengono creati nuovi annunci e devono essere accumulati dati storici per i nuovi annunci. Tuttavia, se non prevedi di inviare nuovamente gli annunci eliminati, non è importante disporre di dati storici.
+++

+++(Feed inventario prodotti) Se elimino un modello di annuncio e ne creo uno nuovo e identico, gli elementi mancanti nel file di feed successivo verranno messi in pausa (quando le impostazioni del file di feed sono configurate per farlo)?

Se nel file di feed successivo mancano elementi di riga e in precedenza non sono stati inseriti tali elementi di riga dal nuovo modello tramite un file di feed precedente, gli elementi di riga mancanti non vengono riconosciuti come &quot;mancanti&quot;, pertanto non vengono creati. Per evitare questo problema, propaga il file di feed precedente tramite il nuovo modello e pubblica i dati prima di propagarli e pubblicarli da un nuovo file.
+++

+++(Feed inventario prodotti) Posso aggiornare i prezzi dei miei prodotti senza influire sul punteggio di qualità di un annuncio?

Per [!DNL Google Ads] Campagne, sì: il [!DNL Google Ads] `{Param 1}` e `{Param 2}` Le variabili ti consentono di inserire in modo dinamico valori numerici in una variante di annuncio senza eliminare e ricreare l’annuncio, e quindi senza influire sul punteggio di qualità.

Per utilizzare una `{Param 1}` o `{Param 2}` variabile per i dati relativi al prezzo, mappa la colonna price nel file di dati con quella variabile nei modelli di feed appropriati, quindi includi la variabile nei modelli di variante dell’annuncio.

Ad esempio, se la colonna è denominata &quot;Prezzo&quot;, apri il modello di feed che crea gli annunci e fai clic nel campo di input accanto a **[!UICONTROL Param 1]**, quindi fare clic su **[!UICONTROL Price]** colonna nella [!UICONTROL Feeds/Available Columns] list, che inserisce `[Price]` come valore per [!UICONTROL Param 1]. Quindi, nel modello di variante dell’annuncio nella parte inferiore del modello di feed, inserisci `{param1:default text}`, dove &quot;testo predefinito&quot; è il testo da utilizzare se la colonna dei parametri nel file di feed è vuota per una riga di annuncio.

Quando si inviano i dati, i campi di dati per [!UICONTROL Param1] e [!UICONTROL Param2] le colonne possono includere fino a 25 caratteri, inclusi dati numerici, simboli di valuta e codici di valuta, e i seguenti caratteri non numerici: `, . % + - /`
+++

+++Le mie campagne generate dai feed di inventario hanno molte transazioni orfane.

Se il [impostazioni dei dati di feed](/help/search-social-commerce/campaign-management/inventory-feeds/feed-settings-manage.md#feed-data-settings) sono configurate per eliminare gli annunci in varie situazioni, quindi eventuali conversioni ritardate che si verificano dopo i clic sull’annuncio possono causare [transazioni orfane](/help/search-social-commerce/glossary.md#o-p). La best practice prevede la sospensione degli annunci invece di eliminarli. Se un annuncio non ha ancora ricevuto ricavi dopo un lungo periodo di tempo, puoi eliminarlo tramite un bulksheet o la visualizzazione di gestione degli annunci.
+++

## Problemi di prestazioni relativi all’account e alla campagna

+++Alcune delle mie campagne spendono più o meno dei budget delle campagne.

* Ciò è normale in un portfolio ottimizzato configurato con il &quot;[!UICONTROL Auto-adjust campaign budget limits]&quot;. Quando questa opzione è abilitata, puoi spendere fino a *N* volte il budget di ogni campagna, dove *N* è il valore di &quot;[!UICONTROL Multiple]&quot;. Questa opzione consente alla funzionalità di ottimizzazione di adeguare la spesa per le singole campagne in base alle esigenze, indirizzando l’intero portfolio al raggiungimento del proprio obiettivo.
* Se [!DNL Google Ads] le campagne utilizzano un budget condiviso, quindi [!DNL Google Ads] adatta la spesa per singole campagne in base alle necessità per spendere l’intero budget condiviso.
+++
