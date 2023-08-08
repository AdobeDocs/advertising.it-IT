---
title: ID Adobe Advertising utilizzati da [!DNL Analytics]
description: ID Adobe Advertising utilizzati da [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ff20b97e-27fe-420e-bd55-8277dc791081
source-git-commit: 73cdb171523b55f48b5ae5c5b2b4843f542336a6
workflow-type: tm+mt
source-wordcount: '1180'
ht-degree: 0%

---

# ID Adobe Advertising utilizzati da [!DNL Analytics]

*Per gli inserzionisti con una sola integrazione Adobi Advertising-Adobe Analytics*

*Applicabile alla pubblicità DSP e[!DNL Advertising Search, Social, & Commerce]*

Adobi Advertising utilizza due ID per il tracciamento delle prestazioni nel sito: *ID EF* e *AMO ID*.

Quando si verifica un’impression pubblicitaria, Adobi Advertising crea e memorizza i valori AMO ID e EF ID. Quando un visitatore che ha visto un annuncio entra nel sito senza fare clic su un annuncio, [!DNL Analytics] richiama questi valori da Adobi Advertising tramite [!DNL Analytics for Advertising] Codice JavaScript. Per il traffico view-through: [!DNL Analytics] genera un ID supplementare (`SDID`), utilizzato per unire l’ID EF e AMO ID in [!DNL Analytics]. Per il traffico click-through, questi ID vengono inclusi nell’URL della pagina di destinazione utilizzando `s_kwcid` e `ef_id` parametri della stringa di query.

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

#### Microsoft Advertising Search Ads

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

## Adobe Advertising di AMO ID

AMO ID tiene traccia di ogni combinazione di annunci univoca a un livello meno granulare e viene utilizzato per [!DNL Analytics] classificazione dei dati e acquisizione di metriche pubblicitarie (come impression, clic e costi) da Adobi Advertising. L’AMO ID è memorizzato in un [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) o la dimensione rVar (AMO ID) e viene utilizzata esclusivamente per la generazione di rapporti in [!DNL Analytics].

L’AMO ID è anche denominato `s_kwcid`, che a volte viene pronunciato come &quot;[!DNL the squid].&quot;

### Formato AMO ID per [!DNL DSP]

```
<Channel ID>!<Ad ID>!<Placement ID>
```

dove:

* &lt;*ID canale*> può essere:

   * `AC` = pubblicità DSP
   * `AL` per [!DNL Advertising Search, Social, & Commerce]

* &lt;*ID annuncio*> viene utilizzato un identificatore univoco generato da un Adobe Advertising per un annuncio. Funge da chiave per tradurre i metadati di entità Adobi Advertising in caratteri leggibili [!DNL Analytics] dimensioni.

* &lt;*ID posizionamento*> è un identificatore univoco generato da un Adobe Advertising per un posizionamento. Funge da chiave per tradurre i metadati di entità Adobi Advertising in caratteri leggibili [!DNL Analytics] dimensioni.

Esempio di AMO ID: AC!iIMvXqlOa6Nia2lDvtgw!GrVv6o2oV2qQLjQiXLC7

### Formato AMO ID per [!DNL Search, Social, & Commerce]

AMO ID per [!DNL Search, Social, & Commerce] segui un formato distinto per ogni motore di ricerca. Il formato di tutti i motori di ricerca inizia con quanto segue:

```
AL!{userid}!{sid}
```

dove:

* `AL` è l’ID canale per la rete di annunci.
* `{userid}` è l’ID utente numerico univoco che Adobi Advertising assegna all’inserzionista.
* `{sid}` è l&#39;ID numerico utilizzato da Adobi Advertising per la rete di annunci specificata, ad esempio `3` per [!DNL Google Ads] o `10` per [!DNL Microsoft Advertising].

Di seguito sono riportati i formati AMO ID completi per un paio di reti di annunci. Per i formati AMO ID per altre reti pubblicitarie, contatta il team del tuo account di Adobe.

Formato AMO ID per [!DNL Google Ads]:

```
AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}
```

dove:

* `{creative}` è il [!DNL Google Ads] ID numerico univoco per la creatività.
* `{matchtype}` è il tipo di corrispondenza della parola chiave che ha attivato l’annuncio: `e` ad esempio, `p` per la frase, oppure `b` per le donne.
* `{placement}` è il nome di dominio del sito web in cui è stato fatto clic sull’annuncio. È disponibile un valore per gli annunci nelle campagne con targeting di posizionamento e per gli annunci nelle campagne con targeting di parola chiave visualizzate sui siti di contenuto.
* `{network}` indica la rete da cui si è verificato il clic:  `g` per [!DNL Google] ricerca (solo per annunci mirati alle parole chiave), `s` per un partner di ricerca (solo per annunci mirati a parole chiave), oppure `d` per la rete di visualizzazione (per annunci mirati a parole chiave o al posizionamento).
* `{keyword}` è la parola chiave specifica che ha attivato l’annuncio (sui siti di ricerca) o la parola chiave con la migliore corrispondenza (sui siti di contenuto).

Formato AMO ID per [!DNL Microsoft Advertising]:

```
AL!{userid}!{sid}!{AdId}!{OrderItemId}
```

dove:

* `{AdId}` è il [!DNL Microsoft Advertising] ID numerico univoco per la creatività.
* `{OrderItemId}` è il [!DNL Microsoft Advertising] ID numerico della parola chiave.

### DIMENSION AMO ID in [!DNL Analytics]

Nei rapporti di Analytics, puoi trovare i dati AMO ID cercando il [!UICONTROL AMO ID] e utilizzando la [!UICONTROL AMO ID Instance] metrica. Il [!UICONTROL AMO ID] , contiene tutti i valori AMO ID acquisiti, mentre [!UICONTROL AMO ID Instance] La metrica indica la frequenza con cui un valore AMO ID è stato acquisito dal sito. Ad esempio, se lo stesso annuncio di ricerca è stato fatto clic quattro volte ma Analytics ha tracciato sette voci di sito, [!UICONTROL AMO ID Instance] sarebbe di sette (7) e [!UICONTROL Clicks] sarebbero quattro (4).

Per qualsiasi reporting o auditing in [!DNL Analytics], la best practice consiste nell’utilizzare l’AMO ID insieme alla relativa istanza. Per ulteriori informazioni, consulta la sezione &quot;[Convalida dati per [!DNL Analytics for Advertising]](data-variances.md#data-validation)&quot; in &quot;Varianze di dati previste tra [!DNL Analytics] e Adobe Advertising.&quot;

## Informazioni sulle classificazioni di Analytics

In entrata [!DNL Analytics], a [classificazione](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) è una parte di metadati per un dato codice di tracciamento, ad esempio Account, Campagna o Annuncio. L’Adobe Advertising categorizza i dati grezzi dell’Adobe Advertising utilizzando le classificazioni in modo da poter visualizzare i dati in diversi modi (ad esempio per tipo di annuncio o campagna) quando si generano i rapporti. Le classificazioni costituiscono la base per la generazione di rapporti di Adobe Advertising in [!DNL Analytics] e possono essere utilizzati con le metriche AMO, ad esempio [!UICONTROL AMO Cost], [!UICONTROL AMO Impressions], e [!UICONTROL AMO Clicks], nonché con eventi nel sito personalizzati e standard come [!UICONTROL Visits], [!UICONTROL Leads], [!UICONTROL Orders], e [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [Panoramica di [!DNL Analytics for Advertising]](overview.md)
>* [Varianze di dati previste tra [!DNL Analytics] e ADOBE ADVERTISING](data-variances.md)
