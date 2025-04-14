---
title: ID Adobe Advertising utilizzati da [!DNL Analytics]
description: ID Adobe Advertising utilizzati da [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ff20b97e-27fe-420e-bd55-8277dc791081
source-git-commit: a69bef9d249514f5c494cff8d706b9df792eaf23
workflow-type: tm+mt
source-wordcount: '1762'
ht-degree: 0%

---

# ID Adobe Advertising utilizzati da [!DNL Analytics]

*Inserzionisti con una sola integrazione Adobe Advertising-Adobe Analytics*

*Applicabile ad Advertising DSP e[!DNL Advertising Search, Social, & Commerce]*

Adobe Advertising utilizza due ID per il tracciamento delle prestazioni nel sito: *EF ID* e *AMO ID*.

Quando si verifica un’impression pubblicitaria, Adobe Advertising crea i valori AMO ID e EF ID e li memorizza. Quando un visitatore che ha visto un annuncio entra nel sito senza fare clic su un annuncio, [!DNL Analytics] chiama questi valori da Adobe Advertising tramite il codice JavaScript [!DNL Analytics for Advertising]. Per il traffico view-through, [!DNL Analytics] genera un ID supplementare (`SDID`) utilizzato per unire l&#39;ID EF e l&#39;AMO ID in [!DNL Analytics]. Per il traffico click-through, questi ID vengono inclusi nell’URL della pagina di destinazione utilizzando i parametri della stringa di query `ef_id` e `s_kwcid` (per l’AMO ID).

Adobe Advertising distingue tra una voce di click-through o di view-through per il sito web utilizzando i seguenti criteri:

* Una voce view-through viene acquisita quando un utente visita il sito dopo aver visualizzato un annuncio ma non facendo clic su di esso. [!DNL Analytics] registra un view-through se sono soddisfatte due condizioni:

   * Il visitatore non ha click-through per un annuncio [!DNL DSP] o [!DNL Search, Social, & Commerce] durante l&#39;[intervallo di lookback su clic](#lookback-a4adc).

   * Il visitatore ha visto almeno un annuncio [!DNL DSP] durante l&#39;[intervallo di lookback delle impression](#lookback-a4adc). L’ultima impression viene passata come view-through.

* Una voce di click-through viene acquisita quando un visitatore del sito fa clic su un annuncio prima di entrare nel sito. [!DNL Analytics] acquisisce un click-through quando si verifica una delle seguenti condizioni:

   * L’URL include un EF ID e un AMO ID aggiunti all’URL della pagina di destinazione da Adobe Advertising.

   * L’URL non contiene codici di tracciamento, ma il codice JavaScript di Adobe Advertising rileva un clic negli ultimi due minuti.

![Integrazione [!DNL Analytics] basata su visualizzazioni di Adobe Advertising](/help/integrations/assets/a4adc-view-through-process.png)

*Figura 1: integrazione [!DNL Analytics] basata su Adobe Advertising*

![Integrazione [!DNL Analytics] basata su URL con clic su Adobe Advertising](/help/integrations/assets/a4adc-click-through-process.png)

*Figura 2: integrazione [!DNL Analytics] basata su URL di clic di Adobe Advertising*

## ID di Adobe Advertising EF

L’ID EF è un token univoco utilizzato da Adobe Advertising per associare l’attività a un clic online o a un’esposizione pubblicitaria. L&#39;ID EF è memorizzato nella dimensione [an [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) o [!DNL rVar] (riservato [!DNL eVar]) (ID EF di Adobe Advertising) e tiene traccia di ogni clic di annuncio o esposizione a livello di singolo browser o dispositivo. Gli ID EF fungono principalmente da chiavi per l&#39;invio di dati [!DNL Analytics] ad Adobe Advertising per il reporting e l&#39;ottimizzazione delle offerte in Adobe Advertising.

### Formato ID EF

>[!NOTE]
>
>Gli ID EF fanno distinzione tra maiuscole e minuscole. Se un&#39;implementazione di [!DNL Analytics] impone il tracciamento URL in minuscolo, Adobe Advertising non riconosce l&#39;ID EF. Questo influisce sulle offerte e sul reporting di Adobe Advertising, ma non ha alcun impatto sul reporting di Adobe Advertising entro [!DNL Analytics].

#### [!DNL Google Ads] annunci di ricerca

```
{gclid}:G:s
```

dove:

* `gclid` è [!DNL Google Click ID] (GCLID).
* `s` è il tipo di rete (&quot;s&quot; per la ricerca).

#### [!DNL Microsoft Advertising] annunci di ricerca

```
{msclkid}:G:s
```

dove:

* `msclkid` è [!DNL Microsoft Click ID] (MSCLKID).
* `s` è il tipo di rete (&quot;s&quot; per la ricerca).

#### Visualizzare annunci e annunci di ricerca su altri motori di ricerca

```
<Adobe Advertising visitor ID>:<timestamp>:<channel type>
```

dove:

* &lt;*ID visitatore Adobe Advertising*> è un ID univoco per visitatore (ad esempio, UhKVaAAABCkJ0mDt). Chiamato anche *ID surfista*.

* &lt;*timestamp*> è l&#39;ora nel formato AAAAMMGGHHMMSS (ad esempio 20190821192533 per Anno 2019, Mese 08, Giorno 21, Ora 19:25:33).

* &lt;*tipo di canale*> è il tipo di canale responsabile del clic o dell&#39;esposizione:

   * `d` per un clic su un annuncio di visualizzazione di DSP (click-through di visualizzazione)
   * `i` per un&#39;impression di un annuncio di visualizzazione DSP (view-through di visualizzazione)
   * `s` per un clic su un annuncio di ricerca (click-through di ricerca).

Esempio `EF ID: WcmibgAAAHJK1RyY:1551968087687:d`

### ID EF Dimension in [!DNL Analytics]

Nei report [!DNL Analytics], è possibile trovare i dati ID EF cercando la dimensione [!UICONTROL EF ID] e utilizzando la metrica [!UICONTROL EF ID Instance].

Gli ID EF sono soggetti al limite di identificatori univoci di 500.000 in Analysis Workspace. Una volta raggiunto il valore 500k, tutti i nuovi codici di tracciamento vengono segnalati con il titolo a riga singola &quot;[!UICONTROL Low Traffic]&quot;. A causa della possibilità di mancanza di fedeltà di reporting, gli ID EF non sono classificati e non è consigliabile utilizzarli per segmenti o rapporti in [!DNL Analytics].

## ADOBE ADVERTISING AMO ID {#amo-id}

AMO ID tiene traccia di ogni combinazione di annunci univoca a un livello meno granulare e viene utilizzato per la classificazione dei dati [!DNL Analytics] e l’acquisizione di metriche pubblicitarie (ad esempio impression, clic e costi) da Adobe Advertising. L&#39;AMO ID è archiviato in una [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) o in una dimensione rVar (AMO ID) ed è utilizzato esclusivamente per il reporting in [!DNL Analytics].

L&#39;AMO ID è anche chiamato `s_kwcid`, che a volte viene pronunciato come &quot;[!DNL squid]&quot;.

### Metodi per implementare AMO ID {#amo-id-implement}

Il parametro viene aggiunto agli URL di tracciamento in uno dei seguenti modi:

* (Consigliato) Quando la funzione di inserimento lato server è implementata.

   * Clienti DSP: il pixel server aggiunge automaticamente il parametro s_kwcid ai suffissi della pagina di destinazione quando un utente finale visualizza un annuncio con pixel di Adobe Advertising.

   * Clienti Search, Social e Commerce:

      * Per gli account [!DNL Google Ads] e [!DNL Microsoft Advertising] con l&#39;impostazione [!UICONTROL Auto Upload] abilitata per l&#39;account o la campagna, il pixel server aggiunge automaticamente il parametro s_kwcid ai suffissi della pagina di destinazione quando un utente finale fa clic su un annuncio con il pixel di Adobe Advertising.

      * Per le altre reti di annunci o per gli account [!DNL Google Ads] e [!DNL Microsoft Advertising] con l&#39;impostazione [!UICONTROL Auto Upload] disabilitata, aggiungi manualmente il parametro ai [parametri di aggiunta a livello di account](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}, che lo aggiungono agli URL di base.

* Quando la funzione di inserimento lato server non è implementata:

   * Clienti DSP: il [codice JavaScript](javascript.md) registra automaticamente i click-through e i view-through. Se un browser non supporta i cookie di terze parti, puoi comunque tenere traccia delle conversioni basate su clic per i seguenti tipi di annunci:

      * Per [!DNL Flashtalking] tag annuncio, inserisci manualmente macro aggiuntive per &quot;[Aggiungi [!DNL Analytics for Advertising] Macro a [!DNL Flashtalking] Tag annuncio](/help/integrations/analytics/macros-flashtalking.md).&quot; **Nota:** questa procedura non è necessaria se l&#39;organizzazione ha una relazione diretta con [!DNL Flashtalking] e si utilizzano macro di passaggio dati per tenere traccia dei parametri di tracciamento di `s_kwcid` e `ef_id` in base alla documentazione di supporto di [!DNL Flashtalking] all&#39;indirizzo [https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros](https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros).

      * Per [!DNL Google Campaign Manager 360] tag annuncio, inserisci manualmente macro aggiuntive per &quot;[Aggiungi [!DNL Analytics for Advertising] Macro a [!DNL Google Campaign Manager 360] Tag annuncio](/help/integrations/analytics/macros-google-campaign-manager.md).&quot;

   * Clienti Search, Social e Commerce:

      * Per gli annunci ([!DNL Google Ads] e [!DNL Microsoft Advertising]), aggiungi manualmente il parametro AMO ID ai suffissi della pagina di destinazione, idealmente a [livello account](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}, a meno che non sia necessario il tracciamento diverso per i singoli componenti account.

      * Per gli annunci su tutte le altre reti pubblicitarie, aggiungi manualmente il parametro AMO ID ai [parametri di aggiunta a livello di account](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}, che lo aggiungono agli URL di base.

Per implementare la funzione di inserimento lato server o per determinare l’opzione migliore per la tua azienda, rivolgiti al team del tuo account Adobe.

### Formati AMO ID {#amo-id-formats}

#### Formato AMO ID per [!DNL DSP]

`s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}`

dove:

* `AC` indica il canale di visualizzazione.

* `{TM_AD_ID}` è la chiave dell&#39;annuncio alfanumerico generato da Adobe Advertising. Viene utilizzato un identificatore univoco per un annuncio e funge da chiave per tradurre i metadati di entità Adobe Advertising in dimensioni [!DNL Analytics] leggibili.

* `{TM_PLACEMENT_ID}` è la chiave di posizionamento alfanumerico generata da Adobe Advertising. Viene utilizzato un identificatore univoco per un posizionamento e funge da chiave per tradurre i metadati di entità Adobe Advertising in dimensioni [!DNL Analytics] leggibili.

Esempio di AMO ID: AC!iIMvXqlOa6Nia2lDvtgw!GrVv6o2oV2qQLjQiXLC7

#### Formati AMO ID per annunci Search, Social e Commerce {#amo-id-format-search}

I parametri variano in base alla rete di annunci, ma i seguenti parametri sono comuni a tutti:

* `AL` indica il canale di ricerca. <!-- what about social/Facebook, and display ads on Google (like Gmail, YouTube)? -->

* `{userid}` è un ID utente univoco assegnato all&#39;inserzionista.

* `{sid}` è sostituito dall&#39;ID numerico per l&#39;account di rete dell&#39;inserzionista: *3* per [!DNL Google Ads], *10* per [!DNL Microsoft Advertising], *45* per [!DNL Meta], *86* per [!DNL Yahoo! Display Network], *87* per [!DNL Naver], *88* per [!DNL Baidu], *90* per [!DNL Yandex], *94* per [!DNL Yahoo! Japan Ads], *105* per [!DNL Yahoo Native] (obsoleto) o *106* per [!DNL Pinterest] (obsoleto).

##### [!DNL Baidu]

`s_kwcid=AL!{userid}!88!{creative}!{placement}!{keywordid}`

dove:

* `{creative}` è l&#39;ID numerico univoco della rete di annunci per la creatività.
* `{placement}` è il sito Web sul quale è stato fatto clic sull&#39;annuncio.
* `{keywordid}` è l&#39;ID numerico univoco della rete di annunci per la parola chiave che ha attivato l&#39;annuncio.

##### [!DNL Google Ads]

Queste includono campagne di acquisto con [!DNL Google Merchant Center].

* Account che utilizzano il formato AMO ID più recente, che supporta il reporting a livello di campagna e gruppo di annunci per campagne, bozze ed esperimenti con prestazione massima:

  `s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

* Tutti gli altri account:

  `s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

dove:

<!-- VERIFY CREATIVE description. Also, are there more networks now (audience and shopping?) -->

* `{creative}` è l&#39;ID numerico univoco [!DNL Google Ads] per la creatività.
* `{matchtype}` è il tipo di corrispondenza della parola chiave che ha attivato l&#39;annuncio: `e` per exact, `p` per phrase, o `b` per broad.
* `{placement}` è il nome di dominio del sito Web in cui è stato fatto clic sull&#39;annuncio. È disponibile un valore per gli annunci nelle campagne con targeting di posizionamento e per gli annunci nelle campagne con targeting di parola chiave visualizzate sui siti di contenuto.
* `{network}` indica la rete da cui si è verificato il clic: `g` per la ricerca [!DNL Google] (solo per annunci mirati a parole chiave), `s` per un partner di ricerca (solo per annunci mirati a parole chiave) o `d` per la rete di visualizzazione (solo per annunci mirati a parole chiave o posizionamento).
* `{product_partition_id}` è l&#39;ID numerico univoco della rete di annunci per il gruppo di prodotti utilizzato con gli annunci di prodotti.
* `{keyword}` è la parola chiave specifica che ha attivato l&#39;annuncio (nei siti di ricerca) o la parola chiave più corrispondente (nei siti di contenuto).
* `{campaignid}` è l&#39;ID numerico univoco della rete di annunci per la campagna.
* `{adgroupid}` è l&#39;ID numerico univoco della rete di annunci per il gruppo di annunci.

>[!NOTE]
>
>* Per gli annunci per ricerca dinamica, {keyword} è popolato con il targeting automatico.
>* Quando si genera il tracciamento per [!DNL Google] annunci di acquisto, un parametro ID prodotto, `{adwords_producttargetid}`, viene inserito prima del parametro della parola chiave. Il parametro ID prodotto non viene visualizzato nei parametri di tracciamento a livello di account [!DNL Google Ads] e di campagna.
>* Per utilizzare il codice di tracciamento AMO ID più recente, vedi &quot;[Aggiornare il codice di tracciamento AMO ID per un account [!DNL Google Ads] account](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md).&quot; <!-- Update terminology there too. -->

<!--

##### [!DNL Meta]

`s_kwcid=AL!{userid}!45!{{ad.id}}!{{campaign.id}}!{{adset.id}}`

where:

* `{{ad.id}}` is the unique numeric ID for the ad/creative.

* `{{campaign.id}}` is the unique ID for the campaign.

* `{{adset.id}}` is the unique ID for the ad set.

-->

##### [!DNL Microsoft Advertising]

* Tutti i tipi di campagna:

  `s_kwcid=AL!{userid}!10!{AdId}!!!!{OrderItemId}!!{CampaignId}!{AdGroupId}`

dove:

* `{AdId}` è l&#39;ID numerico univoco della rete di annunci per la creatività.
* `{OrderItemId}` è l&#39;ID numerico della rete di annunci per la parola chiave.
* `{CampaignId}` è l&#39;ID numerico univoco della rete di annunci per la campagna.
* `{AdGroupId}` è l&#39;ID numerico univoco della rete di annunci per il gruppo di annunci.

>[!NOTE]
>
> Per gli account con campagne senza l&#39;opzione di tracciamento [!UICONTROL Auto Upload] di cui non è stata già eseguita la migrazione al nuovo formato, aggiorna manualmente ogni suffisso di pagina di destinazione per includere il formato precedente.
>Nel frattempo, i formati precedenti, come segue, funzionano ancora:
>* Campagne di ricerca:
>  `s_kwcid=AL!{userid}!10!{AdId}!{OrderItemId}!!{CampaignId}!{AdGroupId}`
>* Campagne di acquisto (utilizzando [!DNL Microsoft Merchant Center]):
>  `s_kwcid=AL!{userid}!10!{AdId}!{CriterionId}`
>* Campagne di Audience Network:
>  `s_kwcid=AL!{userid}!10!{AdId}`

##### [!DNL Yahoo! Japan Ads]

`s_kwcid=AL!{userid}!94!{creative}!{matchtype}!{network}!{keyword}`

dove:

* `{creative}` è l&#39;ID numerico univoco della rete di annunci per la creatività.
* `{matchtype}` è il tipo di corrispondenza della parola chiave che ha attivato l&#39;annuncio: `be` per exact, `bp` per phrase, o `bb` per broad.
* `{network}` indica la rete da cui si è verificato il clic: `n` per la rete nativa o `s` per la ricerca.
* `{keyword}` è la parola chiave che ha attivato l&#39;annuncio.

##### [!DNL Yandex]

`s_kwcid=AL!{userid}!90!{ad_id}!{source_type}!!!{phrase_id}`

dove:

* `{ad_id}` è l&#39;ID numerico univoco della rete di annunci per la creatività.
* `{source_type}` è il tipo di sito in cui è stato visualizzato l&#39;annuncio: *b* per la ricerca, *c* per il contesto (contenuto) o *ct* per la categoria.
* `{phrase_id}` è l&#39;ID numerico della rete di annunci per la parola chiave.

### AMO ID Dimension in [!DNL Analytics]

Nei rapporti di Analytics, puoi trovare i dati AMO ID cercando la dimensione [!UICONTROL AMO ID] e utilizzando la metrica [!UICONTROL AMO ID Instances]. La dimensione [!UICONTROL AMO ID] ospita tutti i valori AMO ID acquisiti, mentre la metrica [!UICONTROL AMO ID Instances] indica la frequenza con cui un valore AMO ID è stato acquisito dal sito. Ad esempio, se lo stesso annuncio di ricerca è stato fatto clic quattro volte ma Analytics ha tracciato sette voci di sito, [!UICONTROL AMO ID Instances] sarebbe sette (7) e [!UICONTROL Clicks] sarebbe quattro (4).

Per qualsiasi reporting o controllo all’interno di [!DNL Analytics], la best practice consiste nell’utilizzare l’AMO ID insieme alla relativa istanza corrispondente. Per ulteriori informazioni, vedere &quot;[Convalida dati Click-through per [!DNL Analytics for Advertising]](data-variances.md#data-validation)&quot; in &quot;Varianze di dati previste tra [!DNL Analytics] e Adobe Advertising.&quot;

## Informazioni sulle classificazioni di Analytics

In [!DNL Analytics], una [classificazione](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) è un elemento di metadati per un determinato codice di tracciamento, ad esempio Account, Campagna o Annuncio. Adobe Advertising categorizza i dati non elaborati di Adobe Advertising utilizzando le classificazioni in modo da poter visualizzare i dati in diversi modi (ad esempio per tipo di annuncio o campagna) quando si generano i rapporti. Le classificazioni costituiscono la base del reporting di Adobe Advertising in [!DNL Analytics] e possono essere utilizzate con le metriche AMO, ad esempio [!UICONTROL Adobe Advertising Cost], [!UICONTROL Adobe Advertising Impressions] e [!UICONTROL AMO Clicks], nonché con eventi nel sito personalizzati e standard come [!UICONTROL Visits], [!UICONTROL Leads], [!UICONTROL Orders] e [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [Panoramica di [!DNL Analytics for Advertising]](overview.md)
>* [Varianze di dati previste tra [!DNL Analytics] e Adobe Advertising](data-variances.md)
