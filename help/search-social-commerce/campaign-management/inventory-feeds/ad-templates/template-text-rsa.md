---
title: Impostazioni di annunci di testo e modelli di annunci di ricerca responsive per i feed di inventario
description: Fai riferimento alle impostazioni per annunci di testo e modelli di annunci di ricerca responsive per feed di inventario.
exl-id: bf57fbb5-b7b0-4bd6-9dd2-def3825a1da6
feature: Search Inventory Feeds
source-git-commit: c5739a7c3564f84c57500b54f17ca25591e09a43
workflow-type: tm+mt
source-wordcount: '3360'
ht-degree: 0%

---

# Impostazioni di annunci di testo e modelli di annunci di ricerca responsive per i feed di inventario

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (elimina solo azioni) e [!DNL Yandex] account solo*

>[!NOTE]
>
>* I caratteri seguenti sono riservati per la designazione di nomi di colonna e nomi di modificatori nel modello e pertanto non sono consentiti come testo in tutti i campi attributo: `[ ] < > `
>* In [!DNL Yandex templates] è possibile utilizzare i parametri dinamici `{param1}` e `{param2}` solo negli URL e non è possibile utilizzare l&#39;inserimento dinamico dei prezzi nelle descrizioni degli annunci.

## \[Sopra tutte le schede\]

<!-- **Template Name:** -->

{{$include /help/_includes/inventory-feed-template-name.md}}

<!-- **Status:** -->

{{$include /help/_includes/inventory-feed-template-status.md}}

<!-- **Account:** -->

{{$include /help/_includes/inventory-feed-template-account.md}}

## \[Pannello sinistro\]

<!-- **[!UICONTROL Feed &amp; Columns]:** -->

{{$include /help/_includes/inventory-feed-template-feed-and-columns.md}}

<!-- **[!UICONTROL Modifiers]:** -->

{{$include /help/_includes/inventory-feed-template-modifiers.md}}

## [!UICONTROL Campaigns]

<!-- **[!UICONTROL Campaign]:** -->

{{$include /help/_includes/inventory-feed-template-campaign.md}}

**[!UICONTROL Map Only]:** (facoltativo) esegue il mapping di tutti i nuovi gruppi di annunci (non disponibile per [!DNL Yandex]), parole chiave e annunci alle campagne esistenti, anziché creare campagne. Se abiliti questa opzione, seleziona il metodo di mappatura.

L&#39;utilizzo di [!UICONTROL Map Only] a livello di campagna richiede una struttura di account esistente strettamente correlata alla tassonomia del prodotto e facilmente mappabile al feed di dati.

**[!UICONTROL Map Method]:** (quando [!UICONTROL Map Only] è abilitato per la campagna) Il metodo con cui i nuovi gruppi di annunci (non disponibili per [!DNL Yandex]), le parole chiave e gli annunci vengono mappati alle campagne esistenti:

* *[!UICONTROL Contains Anywhere]:* aggiunge dati a una campagna esistente il cui nome include la stringa specificata, se esistente.

* *[!UICONTROL Contains Exactly]:* aggiunge dati a una campagna esistente il cui nome include la stringa specificata, se esistente.

* *[!UICONTROL Exactly Matches]* (impostazione predefinita): aggiunge dati a una campagna esistente con lo stesso nome, se esistente.

Se non viene trovata alcuna corrispondenza, tutti i dati della campagna vengono ignorati. Se vengono trovate più corrispondenze della campagna, le parole chiave e gli annunci vengono mappati su tutti.

**[!UICONTROL Campaign Tracking Template]:** (solo account con URL finali/avanzati; facoltativo) Il modello di tracciamento a livello di campagna, che specifica tutti i reindirizzamenti del dominio di destinazione e i parametri di tracciamento e incorpora l&#39;URL finale in un parametro. Questo valore sovrascrive l’impostazione a livello di account, ma i modelli di tracciamento a livelli più granulari (con la parola chiave come più granulare) sovrascrivono questo valore.

* Per il tracciamento delle conversioni di Adobe Advertising, applicato quando le impostazioni della campagna includono &quot;[!UICONTROL EF Redirect]&quot; e &quot;[!UICONTROL Auto Upload]&quot;, Search, Social e Commerce aggiungono automaticamente il codice di reindirizzamento e tracciamento quando si salva il record.

* Per incorporare l’URL finale:

   * ([!DNL Google Ads] e solo [!DNL Microsoft Advertising]) Per un elenco di parametri per indicare gli URL finali nei modelli di tracciamento, vedere ([!DNL Microsoft Advertising] only) [[!DNL Microsoft Advertising] documentation](https://help.ads.microsoft.com/#apex/3/en/56799/2) o ([!DNL Google Ads] only) i parametri &quot;Tracking template only&quot; nella sezione su &quot;Available [!DNL ValueTrack] Parameters&quot; nella [[!DNL Google Ads] documentation](https://support.google.com/google-ads/answer/6305348).

   * ([!DNL Yahoo! Japan Ads] solo) Utilizzare il parametro `!{unescapedurl}` per indicare l&#39;URL della pagina di destinazione.

   * Facoltativamente, puoi includere i parametri URL ed eventuali parametri personalizzati definiti per la campagna, separati da e commerciali (&amp;), ad esempio `{lpurl}?matchtype={matchtype}&device={device}`.

* Per reindirizzamenti e tracciamento di terze parti, inserisci un valore.

<!-- **[!UICONTROL Campaign Final URL Suffix]:** -->

{{$include /help/_includes/final-url-suffix.md}}

<!-- **[!UICONTROL Stock Level]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-stock-level.md}}

<!-- **[!UICONTROL This column has non-numeric values]:** -->

{{$include /help/_includes/inventory-feed-template-nonnumeric-values.md}}

### [!UICONTROL Campaign Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-campaign-negative-keywords.md}}

### [!UICONTROL Manage Settings for NEW Campaigns]

<!-- Flag/check box **[!UICONTROL Manage Settings for NEW Campaigns]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-manage-settings-new-campaigns.md}}

<!-- **[!UICONTROL Initial Budget]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-initial-budget.md}}

**[!UICONTROL Networks]:** (nelle impostazioni delle campagne [!DNL Google Ads] e [!DNL Yandex]) Le reti in cui inserire gli annunci:

* *[!UICONTROL Search]:* Per inviare offerte per inserzioni di ricerca sponsorizzate.

  ([!DNL Google Ads] campagne) Per includere le offerte sulle inserzioni per i partner di ricerca [!DNL Google Ads], seleziona la casella di controllo accanto a **[!UICONTROL Search partners]**.

* *[!UICONTROL Content]:* per inserire offerte per posizionamenti su contenuto (visualizzazione) elenchi di rete. **Nota:** non è possibile creare posizionamenti utilizzando il modello. Quando selezioni questa opzione, crea posizionamenti per ogni gruppo di annunci e specifica le pagine della rete di visualizzazione da targetizzare per ogni gruppo di annunci utilizzando i bulksheet <!-- insert link --> o le impostazioni del gruppo di annunci <!-- insert links --> e del posizionamento nelle viste [!UICONTROL Search] > [!UICONTROL Campaigns].

**[!UICONTROL Languages]:** ([!DNL Google Ads] cerca e visualizza solo le reti) Una o più lingue di destinazione per gli annunci nella campagna.

[!DNL Google Ads] determina la lingua di un utente dall&#39;impostazione della lingua [!DNL Google] dell&#39;utente o dalla lingua della query di ricerca, dalla pagina corrente o dalle pagine visualizzate di recente in [!DNL Google Display Network].

<!-- **[!UICONTROL Locations]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-locations.md}}

**[!UICONTROL Has EU Political Ads]:**([!DNL Google Ads] e [!DNL Microsoft Advertising] solo campagne; applicabile alle campagne destinate a tipi di pubblico nell&#39;Unione europea (UE)) Se la campagna contiene o meno pubblicità politica in base ai requisiti per gli annunci serviti nell&#39;Unione europea ai sensi del Regolamento (UE) 2024/90: *[!UICONTROL Yes]* o *[!UICONTROL No]*.

## [!UICONTROL Ad Groups]

<!-- **[!UICONTROL Ad Group]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group.md}}

<!-- **[!UICONTROL Map Only]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-only.md}}

<!-- **[!UICONTROL Map Method]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-method.md }}

**[!UICONTROL Ad Group Tracking Template]:** (solo account con URL finali/avanzati) Il modello di tracciamento a livello di gruppo di annunci, che specifica tutti i reindirizzamenti del dominio di destinazione e i parametri di tracciamento e incorpora l&#39;URL finale in un parametro.

Per il tracciamento delle conversioni di Adobe Advertising, applicato quando le impostazioni della campagna includono &quot;[!UICONTROL EF Redirect]&quot; e &quot;[!UICONTROL Auto Upload]&quot;, Search, Social e Commerce aggiungono automaticamente il codice di reindirizzamento e tracciamento quando si salva il record.

Per reindirizzamenti e tracciamento di terze parti, inserisci un valore. Per indicare l’URL della pagina di destinazione:

* Per Yahoo! Account Japan Ads, utilizzare il parametro {lpurl}.

* Per i parametri disponibili per gli account Microsoft Advertising e Google Ads, vedi la [[!DNL Microsoft Advertising] documentazione](https://help.ads.microsoft.com/#apex/3/en/56799) o i parametri &quot;Solo modello di tracciamento&quot;nella sezione &quot;Parametri [!DNL ValueTrack] disponibili&quot; nella [[!DNL Google Ads] documentazione](https://support.google.com/google-ads/answer/6305348).

Questo valore sostituisce le impostazioni a livello di account e di campagna, ma i modelli di tracciamento a livelli più granulari (con la parola chiave come più granulare) sostituiscono questo valore.

### [!UICONTROL Ad Group Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-ad-group-negative-keywords.md}}

### [!UICONTROL Manage Settings for NEW Ad Groups]

<!-- Flag/check box **[!UICONTROL Manage Settings for NEW Ad Groups]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-manage-settings-new-ad-groups.md}}

<!-- **[!UICONTROL Languages]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-language-microsoft.md}}

## [!UICONTROL Keywords]

**[!UICONTROL Keywords]:** Parole chiave per il gruppo di annunci specificato (o la campagna per gli account [!DNL Yandex]), che possono essere costituite da qualsiasi combinazione di testo statico, colonne nel file specificato e modificatori. I nomi di colonna e i modificatori vengono sostituiti con i dati effettivi quando il file di feed specificato viene propagato attraverso il modello.

Per inserire un nome di colonna o un gruppo di modificatori come parametro dinamico, fare clic nel campo di input e quindi fare clic su un nome di colonna nell&#39;elenco delle colonne o su un nome di [modificatore](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) nell&#39;elenco dei modificatori. Per specificare più parole chiave o più tipi di corrispondenza per la stessa parola chiave, immetterle su righe separate. Per specificare il tipo di corrispondenza della parola chiave, utilizzare la sintassi seguente intorno al nome della colonna:

* Per i modelli [!DNL Google Ads], [!DNL Microsoft Advertising] e [!DNL Yahoo! Japan Ads]:

   * Per i parametri dinamici: Corrispondenza ampia = `[keyword]`, Modificatore corrispondenza ampia per il primo termine nella colonna [!UICONTROL Keyword] (ad esempio +scarpe blu in camoscio) = `+[keyword]`, Modificatore corrispondenza ampia per ogni termine nella colonna Parola chiave (ad esempio +blu +camoscio +scarpe) = `+[keyword]+`, Corrispondenza frase = `"[keyword]"`, Corrispondenza esatta = `[[keyword]]`

   * Per le parole chiave statiche: Corrispondenza ampia = `keyword`, Modificatore corrispondenza ampia = `+keyword` o Corrispondenza frase = `"keyword"`

     Non è possibile immettere parole chiave statiche con corrispondenza esatta e sintassi di corrispondenza standard perché sono racchiuse tra parentesi quadre (`[]`), come lo sono i parametri dinamici.

* Per [!DNL Yandex] modelli:

   * Per i parametri dinamici: inserire il nome della colonna, ad esempio `[keyword]`. Per indicare il tipo di corrispondenza, utilizzare la sintassi specifica di [[!DNL Yandex]](https://yandex.com/support/direct/keywords/symbols-and-operators.html). **Nota:** Per i termini di corrispondenza generici, utilizzare la sintassi seguente: Broad Match Modifier per il primo termine nella colonna Keyword (ad esempio +blue suede shoes) = `+[keyword]`, Broad Match Modifier per ogni termine nella colonna Keyword (ad esempio +blue +suede +shoes) = `+[keyword]+`

   * Per le parole chiave statiche: sono supportate solo le parole chiave di ricerca. Utilizza la sintassi specifica di [[!DNL Yandex]](https://yandex.com/support/direct/keywords/symbols-and-operators.html) per la parola chiave. Le parentesi quadre (`[]`) per indicare l&#39;ordine delle parole non sono supportate.

>[!NOTE]
>
>* È possibile includere manualmente più valori di modificatore nel campo Parole chiave racchiudendo i valori separati da virgola tra parentesi prima o dopo un parametro di parola chiave (ma non in entrambe le posizioni). Ad esempio, `(cheap, discount, affordable)[product]` genera tre annunci separati per ciascun prodotto.
>* Se non si specifica un tipo di corrispondenza, viene utilizzato il tipo di corrispondenza predefinito &quot;broad&quot;.
>* I risultati negativi non sono supportati.
>* I modificatori di corrispondenza ampia di Google ora hanno lo stesso comportamento di corrispondenza della corrispondenza della frase per alcune lingue e non è possibile creare nuove parole chiave di modificatore di corrispondenza ampia. Per ulteriori informazioni, consulta la [[!DNL Google Ads] documentazione](https://support.google.com/google-ads/answer/10286719).

**[!UICONTROL Map Only]:** Aggiunge nuovi annunci ai gruppi di annunci (o alle campagne per gli account [!DNL Yandex]) in cui vengono trovate le parole chiave specificate, anziché creare nuove parole chiave. Per attivare questa opzione, selezionare la casella di controllo. Quando questa opzione è attivata, tutte le variabili Param 1 e Param 2 nelle parole chiave specificate non vengono applicate perché le parole chiave esistono.

**[!UICONTROL Keyword Final URL]:** (account con URL finali/avanzati; facoltativo) l&#39;URL della pagina di destinazione a cui vengono indirizzati gli utenti della rete pubblicitaria quando fanno clic sull&#39;annuncio. Deve includere lo stesso dominio dell’URL di visualizzazione e tutti i parametri nell’URL finale devono corrispondere a quelli nell’URL della pagina di destinazione dopo il clic dell’annuncio. Può contenere reindirizzamenti all’interno del dominio o del sottodominio della pagina di destinazione, ma non reindirizzamenti all’esterno del dominio della pagina di destinazione.

Se si utilizza un feed [!DNL Google Merchant Center] e si include questo valore nella colonna &quot;[!DNL Link]&quot;, inserire tale colonna in questo campo.

>[!NOTE]
>
>* Se generi URL di tracciamento quando pubblichi dati propagati tramite il modello, i parametri di tracciamento vengono aggiunti a questo valore in base alle impostazioni di tracciamento dell’account.
>* ([!DNL Google Ads] account) Evita di utilizzare macro, che non vengono sostituite dai clic provenienti da origini che abilitano il tracciamento parallelo. Se l’inserzionista deve utilizzare delle macro, il team dell’account di Adobe deve collaborare con l’Assistenza clienti o con il team di implementazione per aggiungerle.

**[!UICONTROL Keyword Tracking Template]:** (account con URL finali/avanzati; facoltativo) Il modello di tracciamento, che specifica tutti i reindirizzamenti del dominio di destinazione e i parametri di tracciamento e incorpora l&#39;URL finale in un parametro. Il modello di tracciamento al livello più granulare (con la parola chiave come valore più granulare) sostituisce i valori a tutti gli altri livelli.

* Per il tracciamento delle conversioni di Adobe Advertising, applicato quando le impostazioni della campagna includono &quot;[!UICONTROL EF Redirect]&quot; e &quot;[!UICONTROL Auto Upload]&quot;, Search, Social e Commerce aggiungono automaticamente il codice di reindirizzamento e tracciamento quando si salva il record.

* Facoltativamente, puoi inserire reindirizzamenti e tracciamento di terze parti.

* Per indicare l’URL della pagina di destinazione:

   * ([!DNL Google Ads] e solo [!DNL Microsoft Advertising]) Per un elenco di parametri per indicare gli URL finali nei modelli di tracciamento, vedere ([!DNL Microsoft Advertising] only) [[!DNL Microsoft Advertising] documentation](https://help.ads.microsoft.com/#apex/3/en/56799) o ([!DNL Google Ads] only) i parametri &quot;Tracking template only&quot; nella sezione su &quot;Available [!DNL ValueTrack] Parameters&quot; nella [[!DNL Google Ads] documentation](https://support.google.com/google-ads/answer/6305348).

   * ([!DNL Yahoo! Japan Ads] solo) Utilizzare il parametro `!{lpurl}` per indicare l&#39;URL della pagina di destinazione.

**[!UICONTROL Param 1]**, **[!UICONTROL Param 2]\[[!DNL Google Ads] modelli\]:** ([!DNL Google Ads] solo modelli) Colonna nel file specificato che rappresenta la variabile [!DNL Google Ads] `{param1}` o `{param2}`, che è possibile includere nella copia dell&#39;annuncio o nell&#39;URL di visualizzazione per qualsiasi annuncio creato dal modello. Per inserire il parametro dinamico, fare clic nel campo di input, quindi selezionare il nome di una colonna nell&#39;elenco delle colonne. Quando il file di feed viene propagato attraverso il modello, il nome della colonna viene sostituito con i dati effettivi.

Se si utilizza uno di questi parametri, è possibile applicarlo solo alle nuove parole chiave oppure aggiornare anche i valori delle parole chiave esistenti che non sono state create dal modello:

* **[!UICONTROL Do Not Apply to Existing Keywords]** (impostazione predefinita): inserisce semplicemente il valore del parametro per le nuove parole chiave create utilizzando il modello.

* **[!UICONTROL Apply to Existing Keywords: Constant]:** Oltre a creare nuove parole chiave dal feed, Search, Social e Commerce aggiorna anche il valore del parametro per tutte le parole chiave esistenti nel gruppo di annunci che non sono state create utilizzando il modello. Immettere un singolo valore numerico da utilizzare per tutte le parole chiave. Il modello deve contenere almeno una parola chiave.

* **[!UICONTROL Apply to Existing Keywords: Min]:** Oltre a creare nuove parole chiave dal feed, Search, Social e Commerce aggiorna anche il valore del parametro per tutte le parole chiave esistenti nel gruppo di annunci che non sono state create utilizzando il modello, purché il file di feed contenga valori numerici per il parametro, con un massimo di un punto decimale ma senza virgole, simboli o codici di valuta o qualsiasi altro carattere. Il valore minimo per il parametro nel file di feed viene utilizzato per tutte le parole chiave esistenti. Ad esempio, se il file di feed ha [!UICONTROL Param1] valori di 21500 e 22000, i valori [!UICONTROL Param1] per le parole chiave esistenti vengono modificati in 21500. Il modello deve contenere almeno una parola chiave. **Suggerimento:** utilizza questa opzione solo quando i gruppi di annunci sono a tema stretto, in modo che le parole chiave abbiano lo stesso valore.

I campi dati nel file di feed possono contenere un massimo di 25 caratteri e possono essere costituiti solo da dati numerici con i seguenti caratteri non numerici:

* (Quando si utilizza il parametro &quot;[!UICONTROL Apply to Existing Keywords: Min]&quot;) Solo fino a un punto decimale.

* Se non si utilizza il parametro &quot;[!UICONTROL Apply to Existing Keywords: Min]&quot;:

   * Il valore può essere preceduto o accodato con un simbolo di valuta o un codice. Ad esempio, sono valide £ 2.000,00 e 2000GBP.

   * Il valore può includere una virgola (,) o un punto (.) come separatore, con un punto facoltativo (.) o una virgola (,) per i valori frazionari. Ad esempio, sono validi 1.000,00 e 2.000,10.

   * Il valore può essere preceduto o accodato da un segno di percentuale (%), un segno più (+) o un segno meno (-). Ad esempio, 20%, 208+ e -42.32 sono validi.

   * È possibile incorporare due numeri con una barra. Ad esempio, sono validi 4/1 e 0,95/0,45.

**[!UICONTROL Param 2]\[[!DNL Microsoft Advertising] modelli\]:** ([!DNL Microsoft Advertising] solo modelli) Stringa da utilizzare come valore di sostituzione in un annuncio se il titolo, il testo, l&#39;URL di visualizzazione o l&#39;URL finale contiene la stringa di sostituzione dinamica `{Param2}`. La lunghezza massima è di 70 caratteri, ma tieni presente la lunghezza massima degli elementi dell’annuncio in cui lo utilizzi (ad esempio, un titolo dell’annuncio può includere fino a 25 caratteri).

**[!UICONTROL Param 3]:** ([!DNL Microsoft Advertising] solo modelli) Stringa da utilizzare come valore di sostituzione in un annuncio se il titolo, il testo, l&#39;URL di visualizzazione o l&#39;URL finale contiene la stringa di sostituzione dinamica `{Param3}`. La lunghezza massima è di 70 caratteri, ma tieni presente la lunghezza massima degli elementi dell’annuncio in cui lo utilizzi (ad esempio, un titolo dell’annuncio può includere fino a 25 caratteri).

**[!UICONTROL Initial Bid (<Match Type or Ad Type>)]:** L&#39;offerta iniziale per ogni parola chiave con il tipo di corrispondenza o di annuncio specificato.

## [!UICONTROL Ads]

**[!UICONTROL Ad Type]:** ([!DNL Google Ads] e [!DNL Microsoft Advertising] solo campagne) Tipo di annunci: *[!UICONTROL Expanded Search Ads]* o *[!UICONTROL Responsive Search Ads]*.

**[!UICONTROL Prefill]:** (Facoltativo) Precompila tutti i campi di copia degli annunci alternativi con il testo dei campi di copia degli annunci originali.

### [!UICONTROL Headlines]

**[!UICONTROL Pin]:** (solo annunci di ricerca responsive) La posizione dell&#39;annuncio in cui deve essere incluso il titolo/titolo (ad esempio &quot;[!UICONTROL Pinned at position 1]&quot;). Il valore predefinito è [!UICONTROL Unpinned].

Per ogni posizione deve essere disponibile almeno un titolo. Se si fissano più titoli nella stessa posizione, l&#39;annuncio finale includerà sempre uno di questi titoli nella posizione specificata. I titoli fissati alla posizione 3 potrebbero non essere visualizzati con l’annuncio.

**[!UICONTROL Headline 1]**, **[!UICONTROL Headline 2]**, **[!UICONTROL Headline 3]:** (solo annunci di ricerca responsive) I titoli degli annunci (titoli). Ogni variante di annuncio deve includere almeno tre titoli di annuncio, fino a un massimo di 15. La rete di annunci visualizza gli annunci con un massimo di tre titoli. La lunghezza massima per ogni titolo è di 30 caratteri, incluso qualsiasi testo dinamico (come i valori delle parole chiave e delle personalizzazioni di annunci).

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-ad-customizer}}

**[!UICONTROL Ad Title]:** (solo annunci di testo standard Microsoft Advertising esistenti; sola lettura) titolo o prima riga di un annuncio. Microsoft Advertising ha dichiarato obsolete la creazione e la modifica di annunci di testo standard.

**[!UICONTROL Headline 1]**, **[!UICONTROL Headline 2]:** ([!DNL Google Ads] e [!DNL Yahoo! Japan Ads] solo modelli di annunci di testo espansi/estesi) Titolo di un annuncio. La lunghezza massima per ogni riga (dopo la sostituzione di eventuali parametri dinamici) è di 30 caratteri o 15 caratteri a doppio byte.

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Headline 3]:** ([!DNL Google Ads] solo modelli di annunci di testo espansi; facoltativo) Un terzo titolo per un annuncio. La lunghezza massima (dopo la sostituzione di eventuali parametri dinamici) è di 30 caratteri o 15 caratteri a doppio byte.

**[!UICONTROL Title]:** ([!DNL Yandex] only) Titolo o prima riga di un annuncio. Il massimo è di 33 caratteri.

**[!UICONTROL Title Part 1]**, **[!UICONTROL Title Part 2]:** (solo annunci di testo espansi di Microsoft Advertising) Titolo di un annuncio. La lunghezza massima per ogni riga (dopo la sostituzione di eventuali parametri dinamici) è di 30 caratteri o 15 caratteri a doppio byte.

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Ad Text]:** (solo annunci di testo espansi di Microsoft Advertising) Corpo di un annuncio. La lunghezza massima (dopo la sostituzione di eventuali parametri dinamici) è di 80 caratteri o 40 caratteri a doppio byte (come cinese, giapponese e coreano).

### [!UICONTROL Descriptions]

**[!UICONTROL Description]:** Il corpo dell&#39;annuncio.

* (Modelli di annunci di testo espansi di Google Ads) La lunghezza massima (dopo la sostituzione di eventuali parametri dinamici) è di 90 caratteri o 45 caratteri a doppio byte.

* (Yahoo! Modelli Japan Ads) La lunghezza massima (dopo la sostituzione di eventuali parametri dinamici) è di 80 caratteri o 40 caratteri a doppio byte.

* (Modelli Yandex) La lunghezza massima (dopo la sostituzione di eventuali parametri dinamici) è di 75 caratteri e una singola parola non può superare i 22 caratteri.

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Pin]:** (solo annunci di ricerca responsive) La posizione dell&#39;annuncio in cui deve essere inclusa la descrizione (ad esempio &quot;[!UICONTROL Pinned at position 1]&quot;). Il valore predefinito è [!UICONTROL Unpinned]. Per ogni posizione deve essere disponibile almeno una descrizione.

Se si fissano più descrizioni alla stessa posizione, l&#39;annuncio finale include sempre una di queste descrizioni nella posizione specificata. Le descrizioni fissate alla posizione 2 potrebbero non essere visualizzate con l’annuncio.

**[!UICONTROL Description 1]**, **[!UICONTROL Description 2]:** (solo annunci di ricerca responsive) Descrizioni annuncio. Ogni variante di annuncio deve includere almeno due descrizioni di annunci, fino a un massimo di quattro. La rete di annunci visualizza annunci con un massimo di due descrizioni; immetti almeno due. La lunghezza massima per ogni descrizione è di 90 caratteri, incluso qualsiasi testo dinamico (come i valori delle parole chiave e delle personalizzazioni di annunci).

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-ad-customizer}}

**[!UICONTROL Description 2]:** (solo modelli di annunci di testo espansi di Google; facoltativo) Una seconda riga dell&#39;annuncio. La lunghezza massima (dopo la sostituzione di eventuali parametri dinamici) è di 90 caratteri o 45 caratteri a doppio byte.

### [!UICONTROL Path]

**[!UICONTROL Display Path 1]**, **[!UICONTROL Display Path 2]:** (solo testo espanso e annunci di ricerca responsive; facoltativo) Uno o due percorsi URL da includere consecutivamente dopo l&#39;URL di base. Devono descrivere il prodotto o servizio nell’annuncio in modo più dettagliato. Ad esempio, se aggiungi [!UICONTROL Display Path 1] di &quot;Scarpe&quot; e [!UICONTROL Display Path 2] di &quot;Esterno&quot; all&#39;URL di base www.example.com, l&#39;URL è www.example.com/Shoes/Outdoor. La lunghezza massima (dopo la sostituzione di eventuali parametri dinamici) per ciascun campo è di 15 caratteri o 7 caratteri a doppio byte.

Per gli annunci di ricerca responsive, inserire un adcustomizzatore di annunci utilizzando i formati seguenti, dove `Default text` è un valore facoltativo da inserire quando il file di feed non include un valore valido:

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}`, ad esempio `{CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}`, ad esempio `{CUSTOMIZER.Discount:10%}`

**[!UICONTROL Display URL]:** (solo annunci di testo standard [!DNL Microsoft Advertising] e [!DNL Yahoo! Japan Ads] esistenti; sola lettura) URL visualizzato in un annuncio.

[!DNL Microsoft Advertising] e [!DNL Yahoo! Japan Ads] hanno dichiarato obsolete la creazione e la modifica di annunci di testo standard.

**[!UICONTROL Base URL]:** (solo account con URL di destinazione) Pagina alla quale vengono indirizzati gli utenti. Può includere codice di reindirizzamento e tracciamento di terze parti. Se utilizzi il servizio di monitoraggio delle conversioni di Adobe Advertising e le impostazioni della campagna includono l&#39;utilizzo di [!UICONTROL EF Redirect] e l&#39;aggiunta del monitoraggio a livello di annuncio, Search, Social e Commerce aggiungono automaticamente il proprio codice di reindirizzamento e tracciamento all&#39;annuncio.

Per inserire un nome di colonna o un gruppo di modificatori come parametro dinamico, fare clic nel campo di input e quindi fare clic su un nome di colonna nell&#39;elenco delle colonne o su un nome di modificatore [](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) nell&#39;elenco [!UICONTROL Modifiers].

**[!UICONTROL Final URL]:** (account con URL finali/avanzati) URL della pagina di destinazione a cui gli utenti vengono indirizzati quando fanno clic sull&#39;annuncio. Deve includere lo stesso dominio dell’URL di visualizzazione e tutti i parametri nell’URL finale devono corrispondere a quelli nell’URL della pagina di destinazione dopo il clic dell’annuncio. Può contenere reindirizzamenti all’interno del dominio o del sottodominio della pagina di destinazione, ma non reindirizzamenti all’esterno del dominio della pagina di destinazione.

Se si utilizza un feed del centro [!DNL Google Merchant] e si include questo valore nella colonna &quot;[!UICONTROL Link]&quot;, inserire tale colonna in questo campo.

>[!NOTE]
>
>* Se generi URL di tracciamento quando pubblichi dati propagati tramite il modello, i parametri di tracciamento vengono aggiunti a questo valore in base alle impostazioni di tracciamento dell’account.
>* ([!DNL Google Ads] account ) Evita l&#39;utilizzo di macro, che non vengono sostituite dai clic provenienti da origini che abilitano il tracciamento parallelo. Se l’inserzionista deve utilizzare delle macro, il team dell’account di Adobe deve collaborare con l’Assistenza clienti o con il team di implementazione per aggiungerle.

**[!UICONTROL Tracking Template]:** (account con URL finali/avanzati; facoltativo) Il modello di tracciamento, che specifica tutti i reindirizzamenti del dominio di destinazione e i parametri di tracciamento e incorpora l&#39;URL finale in un parametro. Il modello di tracciamento al livello più granulare (con la parola chiave come valore più granulare) sostituisce i valori a tutti gli altri livelli.

Per il tracciamento delle conversioni di Adobe Advertising, applicato quando le impostazioni della campagna includono &quot;[!UICONTROL EF Redirect]&quot; e &quot;[!UICONTROL Auto Upload]&quot;, Search, Social e Commerce aggiungono automaticamente il codice di reindirizzamento e tracciamento quando si salva il record.

Per reindirizzamenti e tracciamento di terze parti, inserisci un valore. Per indicare l’URL della pagina di destinazione:

* Per Yahoo! Account Japan Ads, utilizzare il parametro {lpurl}.

* Per i parametri disponibili per gli account Microsoft Advertising e Google Ads, vedi la [[!DNL Microsoft Advertising] documentazione](https://help.ads.microsoft.com/#apex/3/en/56799) o i parametri &quot;Solo modello di tracciamento&quot;nella sezione &quot;Parametri [!DNL ValueTrack] disponibili&quot; nella [[!DNL Google Ads] documentazione](https://support.google.com/google-ads/answer/6305348).

**\[Campi annuncio alternativi sotto i campi annuncio originali\]:** (facoltativo) un set alternativo di copie di annunci per un annuncio, che può essere utilizzato se una qualsiasi delle righe nella copia dell&#39;annuncio originale supera la lunghezza massima consentita una volta che i parametri dinamici vengono compilati con i dati durante la propagazione.

>[!NOTE]
>
>* Se è selezionata l&#39;opzione [!UICONTROL Prefill], i campi alternativi vengono precompilati con quelli originali e puoi modificarli in base alle esigenze.
>* Solo i campi della copia dell’annuncio che superano la lunghezza massima vengono sostituiti con il valore alternativo. Ad esempio, se solo un titolo o titolo originale è troppo lungo, la variante di annuncio generata utilizza il titolo o il titolo alternativo e le descrizioni originali. Assicurati pertanto che la copia dell’annuncio alternativa sia appropriata quando combinata con la copia dell’annuncio originale.
>* Se la copia dell’annuncio originale soddisfa i requisiti di lunghezza del motore di ricerca, la copia dell’annuncio alternativa viene eliminata.

**\[Componente\] [!UICONTROL Ad Label Classifications] > \[Classificazione e valore etichetta\]:** (facoltativo) valori per un massimo di cinque classificazioni di etichette esistenti da assegnare alle varianti di annuncio create o modificate utilizzando il modello. Per ogni componente della campagna a cui desideri assegnare le classificazioni delle etichette:

1. Fare clic sulla casella di controllo.

1. Configura i valori di classificazione delle etichette per il modello di variante dell’annuncio:

   * Per ogni classificazione e valore di etichetta da assegnare al componente, effettua le seguenti operazioni:

      1. Fare clic su **[!UICONTROL Add Label Classification]**.

      1. Selezionare la classificazione dell&#39;etichetta esistente, quindi selezionare un valore esistente o immettere un nuovo valore.

         La lunghezza massima di ogni valore è di 100 caratteri e può includere caratteri ASCII e non ASCII.

         Per inserire un nome di colonna come parametro dinamico per un valore di classificazione di etichetta, fare clic nel campo di input (il secondo campo) e quindi fare clic sul nome di una colonna nell&#39;elenco delle colonne.

         Puoi includere un solo valore per classificazione per componente della campagna. Ad esempio, una campagna può avere Color=Red ma non Color=Red e Color=Blue.

         * Per modificare un valore di classificazione delle etichette esistente, selezionare o immettere un nuovo valore.

         * Per rimuovere un valore di classificazione etichetta esistente, fare clic su **[!UICONTROL X]** accanto al valore.

## [!UICONTROL Feed Filters]

<!-- **\[Feed Filter\]:** -->

{{$include /help/_includes/inventory-feed-template-feed-filter.md}}

## [!UICONTROL Label Classifications]

<!-- **\[Component\] [!UICONTROL Label Classifications] &gt; `[Label Classification and Value`]:** -->

{{$include /help/_includes/inventory-feed-template-label-classifications.md}}

>[!MORELIKETHIS]
>
>* [Informazioni sull&#39;automazione della gestione degli annunci tramite i feed di inventario](../inventory-feeds-about.md)
>* [Gestione dei modificatori](../modifiers-manage.md)
>* [Gestione dei file di feed dei dati di inventario](/help/search-social-commerce/campaign-management/inventory-feeds/feed-files-manage.md)
>* [Propagazione dei dati di feed tramite modelli](../feed-data-propagate.md)
>* [Pubblica dati campagna dai feed di inventario alle reti di annunci](../propagated-data-post.md)
