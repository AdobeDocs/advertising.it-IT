---
title: Impostazioni account inserzionista
description: Consulta le descrizioni delle impostazioni pubblicitarie disponibili.
role: User, Admin
source-git-commit: a7751041b75f4258ce8e57629262c4cb30eccc95
workflow-type: tm+mt
source-wordcount: '927'
ht-degree: 0%

---

# Impostazioni account inserzionista

*Non disponibile per utenti di sola lettura*

<!-- Not published -->

## Impostazioni [!UICONTROL General]

**[!UICONTROL Advertiser Name]:** Il nome dell&#39;inserzionista.

**[!UICONTROL Category]:** La categoria in cui opera l&#39;azienda dell&#39;inserzionista. La categoria viene comunicata agli editori quando si effettua un&#39;offerta in magazzino. Assicurati di scegliere una categoria che sia allineata ai tuoi annunci, altrimenti gli editori potrebbero rifiutare gli annunci.

>[!NOTE]
>
>Se si seleziona *[!UICONTROL Other]*, l&#39;inserzionista non può accedere a DSP [!DNL On Demand Inventory].

**[!UICONTROL Advertiser URL]:** URL della home page o del sito Web principale dell&#39;inserzionista (a partire da `http://` o `https://`).

**[!UICONTROL Share all private exchange feeds into this advertiser]:** (solo nuovi account inserzionista) Rende disponibili all&#39;inserzionista tutti i feed di scambio privati configurati per l&#39;account DSP dell&#39;organizzazione.

### [!UICONTROL Adobe IMS IDs]

Gli inserzionisti che utilizzano altri prodotti Adobe Experience Cloud possono condividere i dati tra alcuni prodotti utilizzando, ad Experience Cloud, l’ID univoco dell’organizzazione. È possibile configurare integrazioni di prodotto specifiche nella sezione [!UICONTROL Integrations].

**[!UICONTROL Account IMS org and ID]:** (inserzionisti con prodotti di Experience Cloud aggiuntivi concessi in licenza tramite un account di Experience Cloud con più inserzionisti; facoltativo) ID organizzazione di Experience Cloud dell&#39;inserzionista.

**[!UICONTROL Advertiser IMS org and ID]:** (inserzionisti con licenze dirette per altri prodotti di Experience Cloud; facoltativo) ID organizzazione Experience Cloud dell&#39;inserzionista.

### [!UICONTROL Integrations]

(Facoltativo) Prodotti di Experience Cloud aggiuntivi collegati al conto DSP. I prodotti devono essere associati allo stesso ID organizzazione Experience Cloud fornito nella sezione [!UICONTROL Adobe IMS IDs].

**[!UICONTROL Attribution services]** > **[!UICONTROL Adobe Media Optimizer]:** (inserzionisti con [!DNL Advertising Search, Social, & Commerce] o che utilizzano pixel di conversione Adobi Advertising) Un account [!DNL Search, Social, & Commerce] con cui l&#39;DSP scambia i dati di attribuzione.

**[!UICONTROL Report suites]** > **[!UICONTROL Adobe Analytics]:** (inserzionisti con Adobe Analytics; facoltativo; applicabile solo ai dati raccolti utilizzando i tag di tracciamento delle conversioni di Adobe Advertising che includono [!DNL EF Redirect] e solo token) Una o più suite di rapporti [!DNL Analytics] a cui l&#39;DSP invia i dati raccolti dagli editori e dai partner lato fornitura. Analytics invia anche i dati raccolti dal sito del cliente all’DSP.

Affinché i dati vengano visualizzati nelle suite di rapporti, è necessario abilitare l&#39;impostazione appropriata a livello di inserzionista [!DNL Search, Social, & Commerce]. Inoltre, l&#39;account [!DNL Analytics] dell&#39;inserzionista deve essere configurato per ricevere dati da Adobe Advertising.

>[!WARNING]
>
>Se rimuovi una suite di rapporti precedentemente collegata, l’DSP non scambia più dati con tale suite. Ci si aspetta di vedere le fluttuazioni dei dati.

Per ulteriori informazioni sull&#39;integrazione con [!DNL Analytics], vedere &quot;[Panoramica di [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)&quot;.

**[!UICONTROL Audiences]** > **[!UICONTROL Adobe Analytics Cloud]:** (inserzionisti con Adobe Audience Manager o Adobe Analytics; facoltativo) un account Audience Manager o [!DNL Analytics] da cui DSP richiama i metadati del segmento, i dati della gerarchia e i dati di pubblico univoci per tutti i tipi di pubblico Adobe dell&#39;inserzionista. Ciò include i dati per:

* Segmenti di Audience Manager
* [!DNL Analytics] segmenti pubblicati in Adobe Experience Cloud
* Segmenti creati con Adobe Experience Cloud [!DNL Audience Library]
* Segmenti creati in Adobe Experience Platform e inviati ad Adobe Advertising tramite Audience Manager

La sincronizzazione iniziale richiede circa 24 ore. Successivamente, i dati vengono sincronizzati in tempo reale, con un ritardo di uno o due secondi.
<!-- I don't think this is true anymore:
Segment membership data is sent to Adobe Advertising only after one of the following:

* The segment is targeted in an Adobe Advertising placement or audience library
* The segment is added to the Adobe Advertising batch and real-time destinations within the Audience Manager user interface
-->

## Impostazioni [!UICONTROL Targeting]

Facoltativamente, puoi configurare le destinazioni predefinite per i nuovi posizionamenti dell’inserzionista. Gli utenti possono sovrascrivere le destinazioni predefinite per qualsiasi nuovo posizionamento.

### [!UICONTROL Geo-targeting]

**[!UICONTROL Countries]:** Il paese predefinito per il geotargeting di ogni posizionamento. Gli utenti possono cambiare il paese e configurare un geotargeting più specifico per ogni posizionamento.

### [!UICONTROL Audience Targeting]

**[!UICONTROL Audiences to exclude]:** Qualsiasi pubblico o segmento da eliminare per impostazione predefinita. Gli utenti possono modificare le esclusioni per ogni posizionamento.

### [!UICONTROL Media Quality]

#### [!UICONTROL Contextual Filtering]

Tipi di filtri contestuali [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science] e [!DNL Peer39] da applicare. Puoi ignorare le impostazioni a livello di inserzionista al [livello di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-context}

**[!UICONTROL Block sites that are]:** (facoltativo) Uno o più tipi di contesto di inventario da bloccare per impostazione predefinita. Possono essere applicate tariffe aggiuntive.

##### [!UICONTROL Peer 39] {#peer39-context}

**[!UICONTROL Target sites that are]:** (Facoltativo) Uno o più tipi di attributi di inventario da impostare come destinazione per impostazione predefinita. Possono essere applicate tariffe aggiuntive.

##### [!UICONTROL ComScore]

**[!UICONTROL Block sites that are]:** (facoltativo) uno o più tipi di attributi di inventario da bloccare per impostazione predefinita. Possono essere applicate tariffe aggiuntive.

##### [!UICONTROL Integral Ad Science] {#ias-context}

**[!UICONTROL Adult Content]:** (Facoltativo) Il livello di contenuto per adulti per il quale bloccare gli annunci per impostazione predefinita: *[!UICONTROL Do Not Block]* (impostazione predefinita), *[!UICONTROL Standard]* o *[!UICONTROL Strict]*. Possono essere applicate tariffe aggiuntive.

**[!UICONTROL Alcohol Content]:** (Facoltativo) Il grado di contenuto alcolico per il quale bloccare gli annunci per impostazione predefinita: *[!UICONTROL Do Not Block]* (impostazione predefinita), *[!UICONTROL Standard]* o *[!UICONTROL Strict]*. Possono essere applicate tariffe aggiuntive.

#### [!UICONTROL Pre-Bid Fraud Blocking]

Tipi di siti da bloccare in base al traffico fraudolento e alle attività sospette misurate tramite [!DNL DoubleVerify], [!DNL Integral Ad Science] e [!DNL Peer39]. Puoi ignorare le impostazioni a livello di inserzionista al [livello di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-fraud}

**[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** Per impostazione predefinita, blocca tutto il traffico non valido al 100%, incluso il traffico su dispositivi dirottati, per i nuovi posizionamenti. Possono essere applicate tariffe aggiuntive.

**[!UICONTROL Also block sites with]:** (Facoltativo) Livello aggiuntivo di frode e traffico non valido che causa il blocco predefinito degli annunci da parte dell&#39;DSP: *[!UICONTROL None]* (impostazione predefinita, che non blocca il traffico aggiuntivo), *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*, *[!UICONTROL >4% Average Fraud/IVT levels]*, *[!UICONTROL >6% Average Fraud/IVT levels]*, *[!UICONTROL >10% Average Fraud/IVT levels]* o *[!UICONTROL >25% Average Fraud/IVT levels]*. Possono essere applicate tariffe aggiuntive.

##### [!UICONTROL Peer 39] {#peer-39-fraud}

**[!UICONTROL Block sites that are]:** (facoltativo) Uno o più tipi di frode che causano il blocco predefinito degli annunci da parte del DSP: *[!UICONTROL Fraud]* (che blocca tutti i siti con frode), *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]* e/o *[!UICONTROL Fraud: Zero Ads]*. Possono essere applicate tariffe aggiuntive.

##### [!UICONTROL Integral Ad Science] {#ias-fraud}

**[!UICONTROL Block sites that are]:** (Facoltativo) Tipo di attività sospetta del sito Web o dell&#39;app che induce l&#39;DSP a bloccare gli annunci per impostazione predefinita: *[!UICONTROL None]* (impostazione predefinita, che non blocca gli annunci basati su attività sospette), *[!UICONTROL Suspicious Activity - High Risk]* o *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. Possono essere applicate tariffe aggiuntive.

#### [!UICONTROL Pre-Bid Viewability]

Filtri di visibilità pre-offerta opzionali di [!DNL DoubleVerify] e [!DNL Integral Ad Science] da applicare ai posizionamenti. I valori predefiniti a livello di inserzionista vengono selezionati per i nuovi posizionamenti. Puoi ignorare le impostazioni a livello di inserzionista al [livello di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-viewability}

###### Video

** **[!UICONTROL Include URL's whose average video viewability rate is]**. Con questa opzione, seleziona i criteri.

** **[!UICONTROL Impressions with Insufficient IAB Viewability Data]**

** **[!UICONTROL Include URL's whose average completion & fully viewable rate is]**. Con questa opzione, seleziona i criteri.

** **[!UICONTROL Include URL's whose average player size composition is]**. Con questa opzione, seleziona i criteri.

** **[!UICONTROL Impressions with Insufficient Player Size Statistics]**

###### Visualizzazione

** **[!UICONTROL Only target URL's or Apps that have historically achieved a display viewability rate of]**. Con questa opzione, seleziona i criteri.

* **[!UICONTROL Impressions with Insufficient IAB Viewability Performance Data]**

* **[!UICONTROL Include Apps and URL's whose average entire creative (100% of pixels) viewable duration is]**. Con questa opzione, seleziona i criteri.

* **[!UICONTROL Impressions with Insufficient BXD Performance Data]**

##### [!UICONTROL Integral Ad Science] {#ias-viewability}

Un filtro **[!UICONTROL Video Viewability Targets]** facoltativo e un filtro **[!UICONTROL Display Viewability Targets]** facoltativo. Possono essere applicate tariffe aggiuntive.

#### [!UICONTROL Ads.text]

**[!UICONTROL Ads.txt Filtering]:** Per impostazione predefinita, quale livello di [[!DNL Ads.txt] filtro pre-offerta](https://iabtechlab.com/ads-txt-about/) utilizzare sfruttando l&#39;elenco [!DNL Authorized Digital Sellers] di ogni editore:
* *[!UICONTROL Opt out of ads.txt (default)]*: per acquistare le scorte da tutti i venditori.
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*: per dare priorità all&#39;acquisto di scorte dai venditori diretti e dai rivenditori autorizzati di un dominio.
* *[!UICONTROL Ads.txt sellers only]*: per acquistare le scorte solo dai venditori diretti e dai rivenditori autorizzati di un dominio.
* *[!UICONTROL Ads.txt sellers only]*: per acquistare le scorte solo dai venditori diretti autorizzati di un dominio.

Puoi ignorare l&#39;impostazione a livello di inserzionista al [livello di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md).

#### [!UICONTROL Safe Site Block]

**[!UICONTROL Enable Site Safety Block]:** Per impostazione predefinita, abilita un filtro post-offerta in tempo reale per garantire che gli annunci vengano distribuiti sui siti di destinazione dell&#39;inserzionista. <!-- Can remove this: Users can enable or disable the feature for each placement. I don't see this option, but I should probably verify. If this can't be edited at placement level, then remove "By default." If it can, say that you can override at placement level. -->

#### [!UICONTROL DoubleVerify Authentic Brand Suitability]

**[!UICONTROL DoubleVerify Account]:** ([!DNL DoubleVerify] solo clienti; facoltativo) l&#39;ID del segmento di sicurezza del brand associato all&#39;account [!DNL DoubleVerify] dell&#39;organizzazione.

**[!UICONTROL Enable Authentic Brand Suitability]:** (Facoltativo) Per impostazione predefinita, abilita [!DNL DoubleVerify Authentic Brand Safety], che blocca le impression post-offerta utilizzando le regole di sicurezza del brand personalizzate configurate per l&#39;ID segmento specificato. L’DSP fattura il tuo account per l’utilizzo dell’ID segmento.

Puoi ignorare l’impostazione a livello di inserzionista a livello di posizionamento.

>[!MORELIKETHIS]
>
>* [Crea un account inserzionista](/help/dsp/admin/advertiser-create.md)

<!-- >* [View the Advertiser List for the Account](/help/dsp/admin/advertiser-view.md) -->
