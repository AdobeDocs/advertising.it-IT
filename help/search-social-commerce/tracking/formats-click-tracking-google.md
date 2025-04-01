---
title: Formati di tracciamento dei clic per  [!DNL Google Ads]
description: Scopri i formati di tracciamento dei clic per  [!DNL Google Ads]  account.
exl-id: d09c3b4e-1274-45fb-abb6-dddfe60f1477
feature: Search Tracking
source-git-commit: 70629247a18a78b12a7fc8b166a0272764bb20b8
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---

# Formati di tracciamento dei clic per [!DNL Google Ads]

Di seguito sono riportati i formati di suffisso del modello di tracciamento di base e della pagina di destinazione (suffisso URL finale) richiesti da Search, Social e Commerce per [!DNL Google Ads].

## Tracciamento dei formati dei modelli

### Rete di ricerca/visualizzazione, compresi i sitelink

Il seguente formato si applica a tutti i tipi di annunci tracciabili su reti di ricerca e visualizzazione e per i sitelink.

`https://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=3&ev_ln={keyword}&ev_lx={targetid}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={_evltx}&ev_pl={placement}&ev_pos={adposition}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={<Google ValueTrack parameter for the final URL>}`

Esempio:

`https://pixel.everesttech.net/1234/cq?ev_sid=3&ev_ln={keyword}&ev_lx={targetid}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={_evltx}&ev_pl={placement}&ev_pos={adposition}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` è una variabile per l&#39;ID univoco dell&#39;inserzionista all&#39;interno di Adobe Advertising.
>
>* Questo formato indica che il passaggio del token è abilitato per la campagna (impostazione predefinita). Se il passaggio del token è disabilitato, sostituire `cq?` dopo `<advertiser_ID>` con `c?`.
>
>* I parametri [!DNL ValueTrack] per indicare gli URL finali nei modelli di tracciamento devono essere `{lpurl}` o `!{unescapedurl}`.
>
>* (Annunci di testo) Quando fai un&#39;offerta per parola chiave, il parametro `ev_pl` (per i posizionamenti) non ha alcun valore. Quando fai un&#39;offerta per posizionamento, `ev_ln` (per parole chiave) non ha valore. Quando fai un&#39;offerta per gruppo di annunci o per qualsiasi altra dimensione, sia `ev_ln` che `ev_pl` non hanno valori.
>
>* (Annunci di ricerca dinamica) `{keyword}` indica l&#39;espressione di destinazione della ricerca dinamica, ad esempio `_cat:[VALUE]` o `_url:[VALUE]`.
>
>* (Annunci di ricerca dinamica) [!DNL Google Ads] determina dinamicamente l&#39;URL finale, pertanto non è necessario immetterne uno.
>
>* (Sitelink) Puoi vedere quali conversioni sono risultate da un clic su un sitelink generando un [!UICONTROL Transaction Report]. Il valore della colonna [!UICONTROL Link Type] per un sitelink è `sl:<Sitelink text>`, ad esempio `sl:See Current Offers`.

### Rete acquisti

Il seguente formato si applica agli annunci e ai gruppi di prodotti nelle reti di acquisto. Puoi specificare un modello di tracciamento a livello di account, campagna, gruppo di annunci o gruppo di prodotti.

`https://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=3&ev_lx={targetid}&ev_ln={keyword}&ev_pl={placement}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={adtype}&ev_plx={product_id}&ev_ptid={product_partition_id}&ev_mid={merchant_id}&ev_cty={product_country}&ev_lan={product_language}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={<Google ValueTrack parameter for the final URL>}`

Esempio:

`https://pixel.everesttech.net/1234/cq?ev_sid=3&ev_lx={targetid}&ev_ln={keyword}&ev_pl={placement}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={adtype}&ev_plx={product_id}&ev_ptid={product_partition_id}&ev_mid={merchant_id}&ev_cty={product_country}&ev_lan={product_language}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` è una variabile per l&#39;ID univoco dell&#39;inserzionista all&#39;interno di Adobe Advertising.
>
>* Questo formato indica che il passaggio del token è abilitato per la campagna (impostazione predefinita). Se il passaggio del token è disabilitato, sostituire `cq?` dopo `<advertiser_ID>` con `c?`.
>
>* I parametri [!DNL ValueTrack] per indicare gli URL finali nei modelli di tracciamento devono essere `{lpurl}` o `!{unescapedurl}`.
>
>* [!DNL Google Ads] utilizza gli URL del prodotto nel feed del Centro commerciale Google come URL finali, pertanto non è necessario immettere gli URL finali per i dati o i gruppi di prodotti.
>
>* Puoi vedere quali conversioni sono risultate da un clic su un annuncio commerciale generando un [!UICONTROL Transaction Report]. Il valore della colonna [!UICONTROL Link Type] per un annuncio di prodotto è pla:`<product ID>`, ad esempio `pla:8525822`.

## Formati del suffisso della pagina di destinazione (suffisso URL finale)

Gli account che utilizzano il monitoraggio delle conversioni di Adobe Advertising devono includere nel suffisso l&#39;identificatore di clic (`gclid` per [!DNL Google Ads]) della rete di annunci:

* Quando l&#39;inserzionista ha un&#39;integrazione Adobe Analytics, il suffisso deve includere uno dei seguenti elementi:

   * [!DNL Google Ads] account che utilizzano il formato [AMO ID](/help/integrations/analytics/ids.md#amo-id-formats) più recente (a partire da `s_kwcid`), che supporta il reporting a livello di campagna e gruppo di annunci per campagne, bozze ed esperimenti con prestazione massima:

     `ef_id={gclid}:G:s&s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

     Se l&#39;account dispone di un&#39;implementazione AMO ID lato server e l&#39;impostazione account o campagna &quot;[!UICONTROL Auto Upload]&quot; è abilitata, il parametro viene aggiunto automaticamente. In caso contrario, è necessario aggiungerlo manualmente. Vedi &quot;[ID Adobe Advertising utilizzati da [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id-implement).&quot;

   * Tutti gli altri account [!DNL Google Ads]:

     `ef_id={gclid}:G:s&s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

* Se l&#39;inserzionista non dispone di un&#39;integrazione Adobe Analytics, il suffisso deve includere quanto segue:

  `&ev_efid={gclid}:G:s`

>[!NOTE]
>
>* I suffissi della pagina di destinazione ai livelli inferiori sovrascrivono il suffisso a livello di account. Per una manutenzione più semplice, utilizza solo il suffisso a livello di account, a meno che non sia necessario un tracciamento diverso per i singoli componenti dell’account. Per configurare un suffisso a livello di gruppo di annunci o inferiore, utilizza l’editor della rete di annunci.
>
>* (Annunci di ricerca dinamica; inserzionisti con Adobe Analytics e senza tracciamento lato server) Quando desideri includere il tracciamento per il feed inverso da Adobe Advertising ad Analytics, aggiungi il codice di tracciamento AMO ID alla fine del suffisso della pagina di destinazione a livello di account.

>[!MORELIKETHIS]
>
>* [Informazioni sui formati degli URL di tracciamento dei clic per il servizio di tracciamento conversione di Adobe Advertising](formats-click-tracking-about.md)
>* [Formati AMO ID](/help/integrations/analytics/ids.md#amo-id-formats)
