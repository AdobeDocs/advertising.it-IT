---
title: Formati di tracciamento dei clic per  [!DNL Microsoft Advertising]
description: Scopri i formati di tracciamento dei clic per  [!DNL Microsoft Advertising]  account.
exl-id: 4970ac33-4978-4768-8701-6fdd3252bbd1
feature: Search Tracking
source-git-commit: 70629247a18a78b12a7fc8b166a0272764bb20b8
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 0%

---

# Formati di tracciamento dei clic per [!DNL Microsoft Advertising]

Di seguito sono riportati i formati di suffisso del modello di tracciamento di base e della pagina di destinazione (suffisso URL finale) richiesti da Search, Social e Commerce per [!DNL Microsoft Advertising].

## Tracciamento dei formati dei modelli

### Reti di ricerca e pubblico (tranne i sitelink)

Il seguente formato si applica a tutti i tipi di annunci tracciabili sulle reti di ricerca e pubblico.

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

Esempio:

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` è una variabile per l&#39;ID univoco dell&#39;inserzionista all&#39;interno di Adobe Advertising.
>
>* Questo formato indica che il passaggio del token è abilitato per la campagna (impostazione predefinita). Se il passaggio del token è disabilitato, sostituire `cq?` dopo `<advertiser_ID>` con `c?`.
>
>* `{TargetId}` rappresenta l&#39;ID di a) la parola chiave o b) la parola chiave e l&#39;elenco di remarketing (pubblico) che hanno attivato l&#39;annuncio (ad esempio, &quot;kwd-123:aud-456&quot; sia per una parola chiave che per un elenco di remarketing o &quot;kwd-123&quot; solo per parola chiave).

### Sitelink

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

Esempio:

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` è una variabile per l&#39;ID univoco dell&#39;inserzionista all&#39;interno di Adobe Advertising.
>
>* Questo formato indica che il passaggio del token è abilitato per la campagna (impostazione predefinita). Se il passaggio del token è disabilitato, sostituire `cq?` dopo `<advertiser_ID>` con `c?`.
>
>* `{TargetId}` rappresenta l&#39;ID di a) la parola chiave o b) la parola chiave e l&#39;elenco di remarketing (pubblico) che hanno attivato l&#39;annuncio (ad esempio, &quot;kwd-123:aud-456&quot; sia per una parola chiave che per un elenco di remarketing o &quot;kwd-123&quot; solo per parola chiave).
>
>* `{adextensionid}` non utilizzato.
>
>* (Sitelink) Puoi vedere quali conversioni sono risultate da un clic su un sitelink generando un [!UICONTROL Transaction Report]. Il valore della colonna [!UICONTROL Link Type] per un sitelink è `sl:<Sitelink text>`, ad esempio `sl:See Current Offers`.

### Rete acquisti

I seguenti formati si applicano agli annunci di acquisto nelle reti di acquisto. Puoi specificare un modello di tracciamento a livello di account, campagna, gruppo di annunci o gruppo di prodotti.

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_plx={ProductId}&ev_ptid={CriterionId}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_ex={feeditemid}&ev_efid={msclkid}:G:s&url={lpurl}`

Esempio:

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_plx={ProductId}&ev_ptid={CriterionId}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_ex={feeditemid}&ev_efid={msclkid}:G:s&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` è una variabile per l&#39;ID univoco dell&#39;inserzionista all&#39;interno di Adobe Advertising.
>
>* Questo formato indica che il passaggio del token è abilitato per la campagna (impostazione predefinita). Se il passaggio del token è disabilitato, sostituire `cq?` dopo `<advertiser_ID>` con `c?`.
>
>* `{TargetId}` rappresenta l&#39;ID di a) la parola chiave o b) la parola chiave e l&#39;elenco di remarketing (pubblico) che hanno attivato l&#39;annuncio (ad esempio, &quot;kwd-123:aud-456&quot; sia per una parola chiave che per un elenco di remarketing o &quot;kwd-123&quot; solo per parola chiave).
>
>* (Facoltativo) Anziché immettere modelli di tracciamento a livello di account, campagna, gruppo di annunci o gruppo di prodotti, è possibile aggiungere l&#39;URL di tracciamento ai dati di prodotto nell&#39;account [!DNL Microsoft Merchant Center]. A questo scopo, includi l&#39;URL di tracciamento, insieme al valore nel campo &quot;`link`&quot; o &quot;`mobile_link`&quot;, a seconda dei casi, in una colonna personalizzata &quot;[bingads_redirect](https://help.bingads.microsoft.com/#apex/3/en/51084/0)&quot; all&#39;interno del feed del prodotto. Il valore nel campo &quot;`bingads_redirect`&quot; sostituisce i valori nei campi &quot;`link`&quot; e &quot;`mobile_link`&quot;. Gli URL generati con questo metodo non includono parametri di tracciamento specificati nelle impostazioni dell’account o della campagna Search, Social e Commerce.

## Formati del suffisso della pagina di destinazione (suffisso URL finale)

>[!NOTE]
>
>I suffissi della pagina di destinazione ai livelli inferiori sovrascrivono il suffisso a livello di account. Per una manutenzione più semplice, utilizza solo il suffisso a livello di account, a meno che non sia necessario un tracciamento diverso per i singoli componenti dell’account. Per configurare un suffisso a livello di gruppo di annunci o inferiore, utilizza l’editor della rete di annunci.

### Ricerca e audience network

Gli account che utilizzano il monitoraggio delle conversioni di Adobe Advertising devono includere nel suffisso l&#39;identificatore di clic (`msclkid` per [!DNL Microsoft Advertising]) della rete di annunci:

* Quando l&#39;inserzionista ha un&#39;integrazione Adobe Analytics, il suffisso deve includere quanto segue:

  `ef_id={msclkid}:G:s&s_kwcid=AL!{userid}!10!{AdId}!{OrderItemId}`

* Se l&#39;inserzionista non dispone di un&#39;integrazione Adobe Analytics, il suffisso deve includere quanto segue:

  `&ev_efid={msclkid}:G:s`

### Rete acquisti

Gli account che utilizzano il monitoraggio delle conversioni di Adobe Advertising devono includere nel suffisso l&#39;identificatore di clic (`msclkid` per [!DNL Microsoft Advertising]) della rete di annunci:

* Quando l&#39;inserzionista ha un&#39;integrazione Adobe Analytics, il suffisso deve includere quanto segue:

  `ef_id={msclkid}:G:s&s_kwcid=AL!{userid}!10!{AdId}!{CriterionId}`

* Se l&#39;inserzionista non dispone di un&#39;integrazione Adobe Analytics, il suffisso deve includere quanto segue:

  `&ev_efid={msclkid}:G:s`

>[!MORELIKETHIS]
>
>* [Informazioni sui formati degli URL di tracciamento dei clic per il servizio di tracciamento conversione di Adobe Advertising](formats-click-tracking-about.md)
>* [Formati AMO ID](/help/integrations/analytics/ids.md#amo-id-formats)
