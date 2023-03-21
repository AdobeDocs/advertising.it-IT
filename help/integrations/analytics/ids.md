---
title: ID pubblicitari di Adobe utilizzati da [!DNL Analytics]
description: ID pubblicitari di Adobe utilizzati da [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ff20b97e-27fe-420e-bd55-8277dc791081
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '1183'
ht-degree: 0%

---

# ID pubblicitari di Adobe utilizzati da [!DNL Analytics]

*Inserzionisti con una sola integrazione Advertising-Adobe Analytics di Adobe*

*Applicabile alle DSP pubblicitarie e[!DNL Advertising Search, Social, & Commerce]*

Adobe Advertising utilizza due ID per il tracciamento delle prestazioni in loco: la *ID EF* e *ID AMO*.

Quando si verifica un’impression pubblicitaria, Adobe Advertising crea i valori AMO ID e EF ID e li memorizza. Quando un visitatore che ha visto un annuncio entra nel sito senza fare clic su un annuncio, [!DNL Analytics] richiama questi valori da Adobe Advertising tramite [!DNL Analytics for Advertising] Codice JavaScript. Per il traffico view-through, [!DNL Analytics] genera un ID supplementare (`SDID`), che viene utilizzato per unire l’ID EF e l’ID AMO in [!DNL Analytics]. Per il traffico click-through, questi ID sono inclusi nell’URL della pagina di destinazione utilizzando `s_kwcid` e `ef_id` parametri della stringa di query.

Ad Adobe, la pubblicità distingue tra una voce click-through o view-through al sito web utilizzando i seguenti criteri:

* Una voce view-through viene acquisita quando un utente visita il sito dopo aver visualizzato un annuncio ma non lo fa clic. [!DNL Analytics] registra un view-through se sono soddisfatte due condizioni:
   * Il visitatore non dispone di click-through per un [!DNL DSP] o [!DNL Search, Social, & Commerce] annuncio durante [finestra di lookback su clic](#lookback-a4adc).
   * Il visitatore ne ha visto almeno uno [!DNL DSP] annuncio durante [intervallo di lookback su impression](#lookback-a4adc). L’ultima impression viene passata come view-through.
* Una voce click-through viene acquisita quando un visitatore del sito fa clic su un annuncio prima di accedere al sito. [!DNL Analytics] acquisisce un click-through quando si verifica una delle seguenti condizioni:
   * L’URL include un EF ID e un AMO ID come aggiunto all’URL della pagina di destinazione da Adobe Advertising.
   * L’URL non contiene codici di tracciamento, ma l’Adobe di codice JavaScript per la pubblicità rileva un clic negli ultimi due minuti.

![Adobe Advertising basato su visualizzazione [!DNL Analytics] integrazione](/help/integrations/assets/a4adc-view-through-process.png)

*Figura 1: Adobe Advertising basato su visualizzazione [!DNL Analytics] integrazione*

![Adobe Pubblicità clic basato su URL [!DNL Analytics] integrazione](/help/integrations/assets/a4adc-click-through-process.png)

*Figura 2: Adobe Pubblicità clic basato su URL [!DNL Analytics] integrazione*

## ID EF di Adobe Advertising

L’ID EF è un token univoco utilizzato da Adobe Advertising per associare l’attività a un clic o a un’esposizione online agli annunci. L’ID EF viene memorizzato in un [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) o dimensione rVar (eVar riservato) (Adobe Advertising EF ID) e tiene traccia di ogni clic o esposizione pubblicitaria a livello di singolo browser o dispositivo. Gli ID EF agiscono principalmente come chiavi per l’invio [!DNL Analytics] dati ad Adobe Advertising per la generazione di rapporti e l’ottimizzazione delle offerte nell’ambito di Adobe Advertising.

### Formato ID EF

>[!NOTE]
>
>Gli ID EF distinguono tra maiuscole e minuscole. Se [!DNL Analytics] l’implementazione forza il tracciamento degli URL in lettere minuscole, quindi Adobe Advertising non riconoscerà l’ID EF. Questo avrà un impatto sulle offerte e sui rapporti di Adobe Advertising, ma non avrà alcun impatto sui rapporti di Adobe Advertising all&#39;interno di [!DNL Analytics].

#### [!DNL Google Ads] ricerca annunci

```
{gclid}:G:s
```

dove:

* `gclid` è [!DNL Google Click ID] (GCLID).
* `s` è il tipo di rete (&quot;s&quot; per la ricerca).

#### Annunci di ricerca Microsoft Advertising

```
{msclkid}:G:s
```

dove:

* `msclkid` è [!DNL Microsoft Click ID] (MSCLKID).
* `s` è il tipo di rete (&quot;s&quot; per la ricerca).

#### Visualizza annunci e cerca annunci su altri motori di ricerca

```
<Adobe Advertising visitor ID>:<timestamp>:<channel type>
```

dove:

* &lt;*ID visitatore Adobe Advertising*> è un ID univoco per visitatore (ad esempio UhKVaAAABCkJ0mDt). Denominato anche *ID surfista*.

* &lt;*timestamp*> è il momento nel formato YYYYMMDDHHMMSS (come 20190821192533 per Anno 2019, Mese 08, Giorno 21, Ora 19:25:33).

* &lt;*tipo di canale*> è il tipo di canale responsabile del clic o dell&#39;esposizione:

   * `d` per un clic su un annuncio DSP visualizzato (visualizzazione click-through)
   * `i` per un&#39;impressione di un annuncio di visualizzazione DSP (display view-through)
   * `s` per fare clic su un annuncio di ricerca (click-through di ricerca).

Esempio `EF ID: WcmibgAAAHJK1RyY:1551968087687:d`

### Dimension EF ID in [!DNL Analytics]

In [!DNL Analytics] rapporti, puoi trovare i dati dell’ID EF cercando [!UICONTROL EF ID] e utilizzando [!UICONTROL EF ID Instance] metrica.

Gli ID EF sono soggetti al limite di identificazione univoca di 500.000 in Analysis Workspace. Una volta raggiunto il valore 500k, tutti i nuovi codici di tracciamento sono riportati sotto il titolo della voce a una riga &quot;[!UICONTROL Low Traffic].&quot; A causa della possibilità di mancanza di fedeltà nella generazione dei rapporti, gli ID EF non vengono classificati e non devono essere utilizzati per i segmenti o per la generazione di rapporti in [!DNL Analytics].

## Adobe Advertising AMO ID

L’AMO ID tiene traccia di ogni combinazione di annunci univoci a un livello meno granulare e viene utilizzato per [!DNL Analytics] classificazione dei dati e acquisizione di metriche pubblicitarie (come impression, clic e costi) da Adobe Advertising. L&#39;AMO ID viene memorizzato in un [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) o dimensione rVar (AMO ID) e viene utilizzata esclusivamente per la generazione di rapporti in [!DNL Analytics].

L’AMO ID è anche denominato `s_kwcid`, che a volte si pronuncia come &quot;[!DNL the squid].&quot;

### Formato AMO ID per [!DNL DSP]

```
<Channel ID>!<Ad ID>!<Placement ID>
```

dove:

* &lt;*ID canale*> può essere:

   * `AC` = DSP pubblicitarie
   * `AL` per [!DNL Advertising Search, Social, & Commerce]

* &lt;*ID annuncio*> è utilizzato un Adobe di identificatore univoco generato dalla pubblicità per un annuncio. Funge da chiave per tradurre i metadati dell’entità Advertising di Adobe in metadati leggibili [!DNL Analytics] dimensioni.

* &lt;*ID posizionamento*> è un Adobe di identificatore univoco generato dalla pubblicità per un posizionamento. Funge da chiave per tradurre i metadati dell’entità Advertising di Adobe in metadati leggibili [!DNL Analytics] dimensioni.

Esempio di ID AMO: AC!iIMvXqlOa6Nia2lDvtgw!GrVv6o2oV2qQLjQiXLC7

### Formato AMO ID per [!DNL Search, Social, & Commerce]

ID AMO per [!DNL Search, Social, & Commerce] segui un formato distinto per ogni motore di ricerca. Il formato per tutti i motori di ricerca inizia con quanto segue:

```
AL!{userid}!{sid}
```

dove:

* `AL` è l&#39;ID canale per la rete pubblicitaria.
* `{userid}` è l’ID utente numerico univoco che Adobe Advertising assegna all’inserzionista.
* `{sid}` è l&#39;ID numerico utilizzato da Adobe Advertising per la rete di annunci specificata, come `3` per [!DNL Google Ads] o `10` per [!DNL Microsoft Advertising].

Di seguito sono riportati i formati AMO ID completi per un paio di reti di annunci. Per i formati AMO ID per altre reti di annunci, contatta il team dell’account Adobe.

Formato AMO ID per [!DNL Google Ads]:

```
AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}
```

dove:

* `{creative}` è [!DNL Google Ads] ID numerico univoco per il creativo.
* `{matchtype}` è il tipo di corrispondenza della parola chiave che ha attivato l’annuncio: `e` esatto, `p` per frase, o `b` in generale.
* `{placement}` è il nome di dominio del sito web sul quale è stato fatto clic sull’annuncio. È disponibile un valore per gli annunci nelle campagne con targeting per il posizionamento e per gli annunci nelle campagne con targeting per parola chiave che vengono visualizzati sui siti di contenuto.
* `{network}` indica la rete da cui si è verificato il clic:  `g` per [!DNL Google] cerca (solo per annunci con targeting per parola chiave), `s` per un partner di ricerca (solo per annunci con targeting per parola chiave), o `d` per Display Network (per annunci mirati a parole chiave o con targeting per il posizionamento).
* `{keyword}` è la parola chiave specifica che ha attivato l’annuncio (sui siti di ricerca) o la parola chiave che corrisponde meglio (sui siti di contenuto).

Formato AMO ID per [!DNL Microsoft Advertising]:

```
AL!{userid}!{sid}!{AdId}!{OrderItemId}
```

dove:

* `{AdId}` è [!DNL Microsoft Advertising] ID numerico univoco per il creativo.
* `{OrderItemId}` è [!DNL Microsoft Advertising] ID numerico della parola chiave.

### Dimension AMO ID in [!DNL Analytics]

Nei rapporti di Analytics puoi trovare i dati AMO ID ricercando il [!UICONTROL AMO ID] e utilizzando [!UICONTROL AMO ID Instance] metrica. La [!UICONTROL AMO ID] la dimensione contiene tutti i valori AMO ID acquisiti, mentre la [!UICONTROL AMO ID Instance] metrica indica la frequenza con cui il sito ha acquisito un valore AMO ID. Ad esempio, se lo stesso annuncio di ricerca è stato selezionato quattro volte ma Analytics ha tracciato sette voci del sito, allora [!UICONTROL AMO ID Instance] sarebbero sette (7) e [!UICONTROL Clicks] sarebbe quattro (4).

Per qualsiasi attività di reporting o di revisione in [!DNL Analytics], la best practice prevede l’utilizzo dell’AMO ID insieme all’istanza corrispondente. Per ulteriori informazioni, consulta &quot;[Convalida dei dati per [!DNL Analytics for Advertising]](data-variances.md#data-validation)&quot; in &quot;Varianze di dati previste tra [!DNL Analytics] e Adobe Advertising.&quot;

## Informazioni sulle classificazioni di Analytics

In [!DNL Analytics], [classificazione](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) è un elemento di metadati per un dato codice di tracciamento, ad esempio Account, Campaign o Ad. Adobe Advertising classifica i dati grezzi di Adobe Advertising utilizzando le classificazioni in modo da poter visualizzare i dati in modi diversi (come per tipo di annuncio o campagna) quando generi i rapporti. Le classificazioni sono alla base della generazione di rapporti sulla pubblicità in Adobe [!DNL Analytics] e può essere utilizzato con le metriche AMO, come [!UICONTROL AMO Cost], [!UICONTROL AMO Impressions]e [!UICONTROL AMO Clicks], nonché con eventi on-site personalizzati e standard come [!UICONTROL Visits], [!UICONTROL Leads], [!UICONTROL Orders]e [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [Panoramica [!DNL Analytics for Advertising]](overview.md)
>* [Varianze di dati previste tra [!DNL Analytics] e pubblicità Adobe](data-variances.md)

