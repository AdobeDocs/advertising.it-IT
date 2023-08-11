---
title: Formati di tracciamento dei clic per [!DNL Microsoft Advertising]
description: Scopri i formati di tracciamento dei clic per [!DNL Microsoft Advertising] account.
exl-id: 725981db-1b9a-4c89-b95d-98d07ec99756
feature: Search Tracking
source-git-commit: 05b9a55e19c9f76060eedb35c41cdd2e11753c24
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 0%

---

# Formati di tracciamento dei clic per [!DNL Microsoft Advertising]

Di seguito sono riportati i formati di suffisso per il modello di tracciamento di base e la pagina di destinazione (suffisso URL finale) richiesti da Search, Social e Commerce per [!DNL Microsoft Advertising].

## Tracciamento dei formati dei modelli

### Reti di ricerca e pubblico (tranne i sitelink)

Il seguente formato si applica a tutti i tipi di annunci tracciabili sulle reti di ricerca e pubblico.

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

Esempio:

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` è una variabile per l’ID univoco dell’inserzionista in Adobi Advertising.
>
>* Questo formato indica che il passaggio del token è abilitato per la campagna (impostazione predefinita). Se il passaggio del token è disabilitato, sostituire `cq?` dopo `<advertiser_ID>` con `c?`.
>
>* `{TargetId}` rappresenta l’ID di a) la parola chiave o b) la parola chiave e l’elenco di remarketing (audience) che hanno attivato l’annuncio (ad esempio, &quot;kwd-123:aud-456&quot; sia per una parola chiave che per un elenco di remarketing o &quot;kwd-123&quot; solo per parola chiave).

### Sitelink

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

Esempio:

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` è una variabile per l’ID univoco dell’inserzionista in Adobi Advertising.
>
>* Questo formato indica che il passaggio del token è abilitato per la campagna (impostazione predefinita). Se il passaggio del token è disabilitato, sostituire `cq?` dopo `<advertiser_ID>` con `c?`.
>
>* `{TargetId}` rappresenta l’ID di a) la parola chiave o b) la parola chiave e l’elenco di remarketing (audience) che hanno attivato l’annuncio (ad esempio, &quot;kwd-123:aud-456&quot; sia per una parola chiave che per un elenco di remarketing o &quot;kwd-123&quot; solo per parola chiave).
>
>* `{adextensionid}` non è utilizzato.
>
>* (Sitelink) Puoi vedere quali conversioni sono risultate da un clic su un sitelink generando un [!UICONTROL Transaction Report]. Il [!UICONTROL Link Type] il valore della colonna per un sitelink è `sl:<Sitelink text>`, ad esempio `sl:See Current Offers`.

### Rete acquisti

I seguenti formati si applicano agli annunci di acquisto nelle reti di acquisto. Puoi specificare un modello di tracciamento a livello di account, campagna, gruppo di annunci o gruppo di prodotti.

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_plx={ProductId}&ev_ptid={CriterionId}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_ex={feeditemid}&ev_efid={msclkid}:G:s&url={lpurl}`

Esempio:

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_plx={ProductId}&ev_ptid={CriterionId}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_ex={feeditemid}&ev_efid={msclkid}:G:s&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` è una variabile per l’ID univoco dell’inserzionista in Adobi Advertising.
>
>* Questo formato indica che il passaggio del token è abilitato per la campagna (impostazione predefinita). Se il passaggio del token è disabilitato, sostituire `cq?` dopo `<advertiser_ID>` con `c?`.
>
>* `{TargetId}` rappresenta l’ID di a) la parola chiave o b) la parola chiave e l’elenco di remarketing (audience) che hanno attivato l’annuncio (ad esempio, &quot;kwd-123:aud-456&quot; sia per una parola chiave che per un elenco di remarketing o &quot;kwd-123&quot; solo per parola chiave).
>
>* (Facoltativo) Invece di inserire modelli di tracciamento a livello di account, campagna, gruppo di annunci o gruppo di prodotti, puoi aggiungere l’URL di tracciamento ai dati di prodotto all’interno di [!DNL Microsoft Merchant Center] account. A tal fine, includi l’URL di tracciamento, insieme al valore nella sezione &quot;`link`&quot; o &quot;`mobile_link`&quot;, a seconda dei casi, in una colonna personalizzata &quot;[bingads_redirect](https://help.bingads.microsoft.com/#apex/3/en/51084/0)&quot; nel feed del prodotto. Il valore in &quot;`bingads_redirect`&quot; sostituirà i valori nel campo &quot;`link`&quot; e &quot;`mobile_link`&quot;. Gli URL generati con questo metodo non includono parametri di tracciamento specificati nelle impostazioni dell’account Search, Social e Commerce o nella campagna.

## Formati del suffisso della pagina di destinazione (suffisso URL finale)

>[!NOTE]
>
>I suffissi della pagina di destinazione ai livelli inferiori sovrascrivono il suffisso a livello di account. Per una manutenzione più semplice, utilizza solo il suffisso a livello di account, a meno che non sia necessario un tracciamento diverso per i singoli componenti dell’account. Per configurare un suffisso a livello di gruppo di annunci o inferiore, utilizza l’editor della rete di annunci.

### Ricerca e audience network

Gli account che utilizzano il tracciamento delle conversioni di Adobi Advertising devono includere l’identificatore di clic della rete di annunci (`msclkid` per [!DNL Microsoft Advertising]) nel suffisso:

* Quando l&#39;inserzionista ha un&#39;integrazione Adobe Analytics, il suffisso deve includere quanto segue:

  `ef_id={msclkid}:G:s&s_kwcid=AL!{userid}!{sid}!{AdId}!{OrderItemId}`

* Se l&#39;inserzionista non dispone di un&#39;integrazione Adobe Analytics, il suffisso deve includere quanto segue:

  `&ev_efid={msclkid}:G:s`

### Rete acquisti

Gli account che utilizzano il tracciamento delle conversioni di Adobi Advertising devono includere l’identificatore di clic della rete di annunci (`msclkid` per [!DNL Microsoft Advertising]) nel suffisso:

* Quando l&#39;inserzionista ha un&#39;integrazione Adobe Analytics, il suffisso deve includere quanto segue:

  `ef_id={msclkid}:G:s&s_kwcid=AL!{userid}!{sid}!{AdId}!{CriterionId}`

* Se l&#39;inserzionista non dispone di un&#39;integrazione Adobe Analytics, il suffisso deve includere quanto segue:

  `&ev_efid={msclkid}:G:s`

>[!MORELIKETHIS]
>
>* [Informazioni sui formati degli URL di tracciamento dei clic per il servizio di tracciamento delle conversioni di Adobe Advertising](formats-click-tracking-about.md)
>* [Formati AMO ID](/help/integrations/analytics/ids.md#amo-id-formats)
