---
source-git-commit: 2b719e00418010b1f8e21b8956ad55b2ffc7dee1
workflow-type: tm+mt
source-wordcount: '697'
ht-degree: 0%

---
# ADOBE ADVERTISING AMO ID

## ADOBE ADVERTISING AMO ID {#amo-id}

AMO ID tiene traccia di ogni combinazione di annunci univoca a un livello meno granulare e viene utilizzato per la classificazione dei dati di [!DNL Analytics] e Customer Journey Analytics e l’acquisizione di metriche pubblicitarie (ad esempio impression, clic e costi) da Adobe Advertising.

Per [!DNL Analytics], l&#39;AMO ID è archiviato in una dimensione [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html?lang=it) o rVar (AMO ID).

Per Customer Journey Analytics, l’AMO ID è archiviato nella proprietà `trackingCode` dell’oggetto `conversionDetails`, che fa parte di [!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension].

L&#39;AMO ID è anche chiamato `s_kwcid`, che a volte viene pronunciato come &quot;[!DNL squid]&quot;.

### Formati AMO ID {#amo-id-formats}

#### Formato AMO ID per [!DNL DSP]

`s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}`

dove:

* `AC` indica il canale di visualizzazione.

* `{TM_AD_ID}` è la chiave dell&#39;annuncio alfanumerico generato da Adobe Advertising. Viene utilizzato un identificatore univoco per un annuncio e funge da chiave per tradurre i metadati di entità Adobe Advertising in dimensioni leggibili [!DNL Analytics] e Customer Journey Analytics.

* `{TM_PLACEMENT_ID}` è la chiave di posizionamento alfanumerico generata da Adobe Advertising. Viene utilizzato un identificatore univoco per un posizionamento e funge da chiave per tradurre i metadati di entità Adobe Advertising in dimensioni leggibili [!DNL Analytics] e Customer Journey Analytics.

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
> &#x200B;>Nel frattempo, i formati precedenti, come segue, funzionano ancora:
>* Campagne di ricerca:
>  &#x200B;>  `s_kwcid=AL!{userid}!10!{AdId}!{OrderItemId}!!{CampaignId}!{AdGroupId}`
>* Campagne di acquisto (utilizzando [!DNL Microsoft Merchant Center]):
>  &#x200B;>  `s_kwcid=AL!{userid}!10!{AdId}!{CriterionId}`
>* Campagne di Audience Network:
>  &#x200B;>  `s_kwcid=AL!{userid}!10!{AdId}`

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
