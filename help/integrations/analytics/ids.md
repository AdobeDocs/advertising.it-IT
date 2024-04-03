---
title: ID Adobe Advertising utilizzati da [!DNL Analytics]
description: ID Adobe Advertising utilizzati da [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ff20b97e-27fe-420e-bd55-8277dc791081
source-git-commit: 9374f5ef6aaff1f638022bc878c7af190e31888f
workflow-type: tm+mt
source-wordcount: '1686'
ht-degree: 0%

---

# ID Adobe Advertising utilizzati da [!DNL Analytics]

*Per gli inserzionisti con una sola integrazione Adobi Advertising-Adobe Analytics*

*Applicabile alla pubblicità DSP e[!DNL Advertising Search, Social, & Commerce]*

Adobi Advertising utilizza due ID per il tracciamento delle prestazioni nel sito: *ID EF* e *AMO ID*.

Quando si verifica un’impression pubblicitaria, Adobi Advertising crea e memorizza i valori AMO ID e EF ID. Quando un visitatore che ha visto un annuncio entra nel sito senza fare clic su un annuncio, [!DNL Analytics] richiama questi valori da Adobi Advertising tramite [!DNL Analytics for Advertising] Codice JavaScript. Per il traffico view-through: [!DNL Analytics] genera un ID supplementare (`SDID`), utilizzato per unire l’ID EF e AMO ID in [!DNL Analytics]. Per il traffico click-through, questi ID vengono inclusi nell’URL della pagina di destinazione utilizzando `ef_id` e `s_kwcid` (per AMO ID) parametri della stringa di query.

L’Adobe Advertising distingue tra una voce di click-through o di view-through per il sito web utilizzando i seguenti criteri:

* Una voce view-through viene acquisita quando un utente visita il sito dopo aver visualizzato un annuncio ma non facendo clic su di esso. [!DNL Analytics] registra una visualizzazione view-through se sono soddisfatte due condizioni:

   * Il visitatore non ha click-through per un [!DNL DSP] o [!DNL Search, Social, & Commerce] annuncio durante [fai clic sull’intervallo di lookback](#lookback-a4adc).

   * Il visitatore ne ha visto almeno uno [!DNL DSP] annuncio durante [intervallo di lookback delle impression](#lookback-a4adc). L’ultima impression viene passata come view-through.

* Una voce di click-through viene acquisita quando un visitatore del sito fa clic su un annuncio prima di entrare nel sito. [!DNL Analytics] acquisisce un click-through quando si verifica una delle seguenti condizioni:

   * L’URL include un ID EF e un AMO ID aggiunti all’URL della pagina di destinazione per Adobe Advertising.

   * L’URL non contiene codici di tracciamento, ma il codice JavaScript di Adobe Advertising rileva un clic negli ultimi due minuti.

![Adobe Advertising basato sulla visualizzazione [!DNL Analytics] integrazione](/help/integrations/assets/a4adc-view-through-process.png)

*Figura 1: Adobe Advertising basato sulla visualizzazione [!DNL Analytics] integrazione*

![Adobe Advertising di clic basato su URL [!DNL Analytics] integrazione](/help/integrations/assets/a4adc-click-through-process.png)

*Figura 2: clic Adobe Advertising basato su URL [!DNL Analytics] integrazione*

## ADOBE ADVERTISING ID EF

L’ID EF è un token univoco utilizzato da Adobi Advertising per associare l’attività a un clic online o a un’esposizione pubblicitaria. L’ID EF è memorizzato in [un [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) o [!DNL rVar] (riservato) [!DNL eVar]) (ID EF di Adobe Advertising) e tiene traccia di ogni clic di annuncio o esposizione a livello di singolo browser o dispositivo. Gli ID EF fungono principalmente da chiavi per l’invio [!DNL Analytics] dati da inserire nell’Adobe Advertising per la generazione di rapporti e l’ottimizzazione delle offerte in Adobi Advertising.

### Formato ID EF

>[!NOTE]
>
>Gli ID EF fanno distinzione tra maiuscole e minuscole. Se un [!DNL Analytics] L’implementazione forza il tracciamento URL in lettere minuscole, quindi Adobi Advertising non riconoscerà l’ID EF. Questo influirà sulle offerte e sui rapporti di Adobi Advertising, ma non ha alcun impatto sulla generazione di rapporti di Adobi Advertising in [!DNL Analytics].

#### [!DNL Google Ads] annunci di ricerca

```
{gclid}:G:s
```

dove:

* `gclid` è il [!DNL Google Click ID] (GCLID)
* `s` è il tipo di rete (&quot;s&quot; per la ricerca).

#### [!DNL Microsoft Advertising] annunci di ricerca

```
{msclkid}:G:s
```

dove:

* `msclkid` è il [!DNL Microsoft Click ID] (MSCLKID)
* `s` è il tipo di rete (&quot;s&quot; per la ricerca).

#### Visualizzare annunci e annunci di ricerca su altri motori di ricerca

```
<Adobe Advertising visitor ID>:<timestamp>:<channel type>
```

dove:

* &lt;*ID visitatore Adobe Advertising*> è un ID univoco per visitatore (ad esempio UhKVaAAABCkJ0mDt). Denominato anche *ID surfista*.

* &lt;*timestamp*> è l’ora nel formato YYYYMMDDHMMSS (ad esempio 20190821192533 per l’anno 2019, mese 08, giorno 21, ora 19:25:33 ).

* &lt;*tipo di canale*> è il tipo di canale responsabile del clic o dell’esposizione:

   * `d` per fare clic su un annuncio di visualizzazione DSP (click-through di visualizzazione)
   * `i` per una rappresentazione di un annuncio di visualizzazione dell’DSP (view-through del display)
   * `s` per fare clic su un annuncio di ricerca (click-through di ricerca).

Esempio `EF ID: WcmibgAAAHJK1RyY:1551968087687:d`

### Il Dimension EF ID in [!DNL Analytics]

In entrata [!DNL Analytics] report, è possibile trovare i dati ID EF ricercando il [!UICONTROL EF ID] e utilizzando la [!UICONTROL EF ID Instance] metrica.

Gli ID EF sono soggetti al limite di identificatori univoci di 500.000 in Analysis Workspace. Una volta raggiunto il valore di 500k, tutti i nuovi codici di tracciamento sono segnalati sotto il titolo di una riga &quot;[!UICONTROL Low Traffic].&quot; A causa della possibilità di mancanza di fedeltà di reporting, gli ID EF non sono classificati e non è consigliabile utilizzarli per i segmenti o il reporting in [!DNL Analytics].

## Adobe Advertising di AMO ID {#amo-id}

AMO ID tiene traccia di ogni combinazione di annunci univoca a un livello meno granulare e viene utilizzato per [!DNL Analytics] classificazione dei dati e acquisizione di metriche pubblicitarie (come impression, clic e costi) da Adobi Advertising. L’AMO ID è memorizzato in un [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) o la dimensione rVar (AMO ID) e viene utilizzata esclusivamente per la generazione di rapporti in [!DNL Analytics].

L’AMO ID è anche denominato `s_kwcid`, che a volte viene pronunciato come &quot;[!DNL the squid].&quot;

### Metodi per implementare AMO ID {#amo-id-implement}

Il parametro viene aggiunto agli URL di tracciamento in uno dei seguenti modi:

* (Consigliato) Quando la funzione di inserimento lato server è implementata.

   * Clienti DSP: il pixel server aggiunge automaticamente il parametro s_kwcid ai suffissi della pagina di destinazione quando un utente finale visualizza un annuncio con il pixel di Adobe Advertising.

   * Clienti Search, Social e Commerce:

      * Per [!DNL Google Ads] e [!DNL Microsoft® Advertising] account con [!UICONTROL Auto Upload] se l’impostazione è abilitata per l’account o la campagna, il pixel server aggiunge automaticamente il parametro s_kwcid ai suffissi della pagina di destinazione quando un utente finale fa clic su un annuncio con il pixel di Adobe Advertising.

      * Per altre reti pubblicitarie, o [!DNL Google Ads] e [!DNL Microsoft® Advertising] account con [!UICONTROL Auto Upload] disabilitata, aggiungi manualmente il parametro al tuo [parametri di accodamento a livello di account](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}, che lo aggiungono agli URL di base.

* Quando la funzione di inserimento lato server non è implementata:

   * Clienti DSP: il [Codice JavaScript](javascript.md) registra automaticamente i click-through e i view-through. Se un browser non supporta i cookie di terze parti, puoi comunque tenere traccia delle conversioni basate su clic per i seguenti tipi di annunci:

      * Per [!DNL Flashtalking] Aggiungi tag, inserisci manualmente macro aggiuntive per &quot;[Aggiungi [!DNL Analytics for Advertising] Macro per [!DNL Flashtalking] Tag annuncio](/help/integrations/analytics/macros-flashtalking.md).&quot;

      * Per [!DNL Google Campaign Manager 360] Aggiungi tag, inserisci manualmente macro aggiuntive per &quot;[Aggiungi [!DNL Analytics for Advertising] Macro per [!DNL Google Campaign Manager 360] Tag annuncio](/help/integrations/analytics/macros-google-campaign-manager.md).&quot;

   * Clienti Search, Social e Commerce:

      * Per ([!DNL Google Ads] e [!DNL Microsoft® Advertising]), aggiungi manualmente il parametro AMO ID ai suffissi della pagina di destinazione, idealmente in corrispondenza del [livello account](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"} a meno che non sia necessario un tracciamento diverso per i singoli componenti del conto.

      * Per gli annunci su tutte le altre reti di annunci, aggiungi manualmente il parametro AMO ID al tuo [parametri di accodamento a livello di account](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}, che lo aggiungono agli URL di base.

Per implementare la funzione di inserimento lato server o per determinare l’opzione migliore per la tua azienda, rivolgiti al team del tuo account di Adobe.

### Formati AMO ID {#amo-id-formats}

#### Formato AMO ID per [!DNL DSP]

`s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}`

dove:

* `AC` indica il canale di visualizzazione.

* `{TM_AD_ID}` è la chiave dell’annuncio alfanumerico generata dall’Adobe Advertising. Viene utilizzato un identificatore univoco per un annuncio e funge da chiave per tradurre i metadati di entità Adobi Advertising in caratteri leggibili [!DNL Analytics] dimensioni.

* `{TM_PLACEMENT_ID}` è la chiave di posizionamento alfanumerico generata da Adobi Advertising. Viene utilizzato un identificatore univoco per un posizionamento e funge da chiave per tradurre i metadati di entità Adobi Advertising in caratteri leggibili [!DNL Analytics] dimensioni.

Esempio di AMO ID: AC!iIMvXqlOa6Nia2lDvtgw!GrVv6o2oV2qQLjQiXLC7

#### Formati AMO ID per annunci Search, Social e Commerce {#amo-id-format-search}

I parametri variano in base alla rete di annunci, ma i seguenti parametri sono comuni a tutti:

* `AL` indica il canale di ricerca. <!-- what about social/Facebook, and display ads on Google (like Gmail, YouTube)? -->

* `{userid}` è un ID utente univoco assegnato all’inserzionista.

* `{sid}` è sostituito dall’ID numerico dell’account di rete dell’inserzionista: *3* per [!DNL Google Ads], *10* per [!DNL Microsoft Advertising], *45* per [!DNL Meta], *86* per [!DNL Yahoo! Display Network], *87* per [!DNL Naver], *88* per [!DNL Baidu], *90* per [!DNL Yandex], *94* per [!DNL Yahoo! Japan Ads], *105* per [!DNL Yahoo Native] (obsoleto), oppure *106* per [!DNL Pinterest] (obsoleto).

##### [!DNL Baidu]

`s_kwcid=AL!{userid}!{sid}!{creative}!{placement}!{keywordid}`

dove:

* `{creative}` è l’ID numerico univoco della rete di annunci per il contenuto creativo.
* `{placement}` è il sito web su cui è stato fatto clic sull’annuncio.
* `{keywordid}` è l’ID numerico univoco della rete di annunci per la parola chiave che ha attivato l’annuncio.

##### [!DNL Google Ads]

Tra cui campagne di acquisto tramite [!DNL Google Merchant Center].

* Account che utilizzano il formato AMO ID più recente, che supporta il reporting a livello di campagna e gruppo di annunci per campagne, bozze ed esperimenti con prestazione massima:

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

* Tutti gli altri account:

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

dove:

<!-- VERIFY CREATIVE description. Also, are there more networks now (audience and shopping?) -->

* `{creative}` è il [!DNL Google Ads] ID numerico univoco per la creatività.
* `{matchtype}` è il tipo di corrispondenza della parola chiave che ha attivato l’annuncio: `e` ad esempio, `p` per la frase, oppure `b` per le donne.
* `{placement}` è il nome di dominio del sito web in cui è stato fatto clic sull’annuncio. È disponibile un valore per gli annunci nelle campagne con targeting di posizionamento e per gli annunci nelle campagne con targeting di parola chiave visualizzate sui siti di contenuto.
* `{network}` indica la rete da cui si è verificato il clic: `g` per [!DNL Google] ricerca (solo per annunci mirati alle parole chiave), `s` per un partner di ricerca (solo per annunci mirati a parole chiave), oppure `d` per la rete di visualizzazione (per annunci mirati a parole chiave o al posizionamento).
* `{product_partition_id}` è l’ID numerico univoco della rete di annunci per il gruppo di prodotti utilizzato con gli annunci di prodotti.
* `{keyword}` è la parola chiave specifica che ha attivato l’annuncio (sui siti di ricerca) o la parola chiave con la migliore corrispondenza (sui siti di contenuto).
* `{campaignid}` è l’ID numerico univoco della rete di annunci per la campagna.
* `{adgroupid}` è l’ID numerico univoco della rete di annunci per il gruppo di annunci.

>[!NOTE]
>
>* Per gli annunci per ricerca dinamica: {keyword} viene popolato con il targeting automatico.
>* Quando generi il tracciamento per [!DNL Google] annunci commerciali, un parametro ID prodotto, `{adwords_producttargetid}`, viene inserito prima del parametro della parola chiave. Il parametro ID prodotto non viene visualizzato nel [!DNL Google Ads] parametri di tracciamento a livello di account e di campagna.
>* Per utilizzare il codice di tracciamento AMO ID più recente, vedi &quot;[Aggiornamento del codice di tracciamento AMO ID per un [!DNL Google Ads] account](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md).&quot; <!-- Update terminology there too. -->

<!--

##### [!DNL Meta]

`s_kwcid=AL!{userid}!{sid}!{{ad.id}}!{{campaign.id}}!{{adset.id}}`

where:

* `{{ad.id}}` is the unique numeric ID for the ad/creative.

* `{{campaign.id}}` is the unique ID for the campaign.

* `{{adset.id}}` is the unique ID for the ad set.

-->

##### [!DNL Microsoft Advertising]

* Campagne di ricerca:

  `s_kwcid=AL!{userid}!{sid}!{AdId}!{OrderItemId}`

* Campagne commerciali (utilizzando [!DNL Microsoft Merchant Center]):

  `s_kwcid=AL!{userid}!{sid}!{AdId}!{CriterionId}`

* Campagne di Audience Network:

  `s_kwcid=AL!{userid}!{sid}!{AdId}`

dove:

* `{AdId}` è l’ID numerico univoco della rete di annunci per il contenuto creativo.
* `{OrderItemId}` è l’ID numerico della rete di annunci per la parola chiave.
* `{CriterionId}` è l’ID numerico della rete di annunci per il gruppo di prodotti utilizzato con gli annunci di prodotti.

##### [!DNL Yahoo! Japan Ads]

`s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{network}!{keyword}`

dove:

* `{creative}` è l’ID numerico univoco della rete di annunci per il contenuto creativo.
* `{matchtype}` è il tipo di corrispondenza della parola chiave che ha attivato l’annuncio: `be` ad esempio, `bp` per la frase, oppure `bb` per le donne.
* `{network}` indica la rete da cui si è verificato il clic: `n` per nativo o `s` per la ricerca.
* `{keyword}` è la parola chiave che ha attivato l’annuncio.

##### [!DNL Yandex]

`s_kwcid=AL!{userid}!{sid}!{ad_id}!{source_type}!!!{phrase_id}`

dove:

* `{ad_id}` è l’ID numerico univoco della rete di annunci per il contenuto creativo.
* `{source_type}` è il tipo di sito in cui è stato visualizzato l’annuncio: *b* per la ricerca, *c* per contesto (contenuto), oppure *ct* per categoria.
* `{phrase_id}` è l’ID numerico della rete di annunci per la parola chiave.

### DIMENSION AMO ID in [!DNL Analytics]

Nei rapporti di Analytics, puoi trovare i dati AMO ID cercando il [!UICONTROL AMO ID] e utilizzando la [!UICONTROL AMO ID Instances] metrica. Il [!UICONTROL AMO ID] , contiene tutti i valori AMO ID acquisiti, mentre [!UICONTROL AMO ID Instances] La metrica indica la frequenza con cui un valore AMO ID è stato acquisito dal sito. Ad esempio, se lo stesso annuncio di ricerca è stato fatto clic quattro volte ma Analytics ha tracciato sette voci di sito, [!UICONTROL AMO ID Instances] sarebbe di sette (7) e [!UICONTROL Clicks] sarebbero quattro (4).

Per qualsiasi reporting o auditing in [!DNL Analytics], la best practice consiste nell’utilizzare l’AMO ID insieme alla relativa istanza. Per ulteriori informazioni, consulta la sezione &quot;[Convalida dei dati di click-through per [!DNL Analytics for Advertising]](data-variances.md#data-validation)&quot; in &quot;Varianze di dati previste tra [!DNL Analytics] e Adobe Advertising.&quot;

## Informazioni sulle classificazioni di Analytics

In entrata [!DNL Analytics], a [classificazione](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) è una parte di metadati per un dato codice di tracciamento, ad esempio Account, Campagna o Annuncio. L’Adobe Advertising categorizza i dati grezzi dell’Adobe Advertising utilizzando le classificazioni in modo da poter visualizzare i dati in diversi modi (ad esempio per tipo di annuncio o campagna) quando si generano i rapporti. Le classificazioni costituiscono la base per la generazione di rapporti di Adobe Advertising in [!DNL Analytics] e possono essere utilizzati con le metriche AMO, ad esempio [!UICONTROL Adobe Advertising Cost], [!UICONTROL Adobe Advertising Impressions], e [!UICONTROL AMO Clicks], nonché con eventi nel sito personalizzati e standard come [!UICONTROL Visits], [!UICONTROL Leads], [!UICONTROL Orders], e [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [Panoramica di [!DNL Analytics for Advertising]](overview.md)
>* [Varianze di dati previste tra [!DNL Analytics] e ADOBE ADVERTISING](data-variances.md)
