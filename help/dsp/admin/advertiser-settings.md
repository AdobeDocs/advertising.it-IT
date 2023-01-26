---
title: Impostazioni account inserzionista
description: Consulta le descrizioni delle impostazioni dell’inserzionista disponibili.
source-git-commit: 1a98b3ba7c37a768825e9e48db7d847f12daa9a0
workflow-type: tm+mt
source-wordcount: '871'
ht-degree: 0%

---

# Impostazioni account inserzionista

*Non disponibile per utenti di sola lettura*

## [!UICONTROL General] Impostazioni

**[!UICONTROL Advertiser Name]:** Nome dell&#39;inserzionista.

**[!UICONTROL Category]:** La categoria in cui opera l&#39;inserzionista. La categoria viene comunicata agli editori quando fai un&#39;offerta su inventory. Assicurati di scegliere una categoria che si allinea ai tuoi annunci, o gli editori possono rifiutare i tuoi annunci.

>[!NOTE]
>
>Se si seleziona *[!UICONTROL Other]*, quindi l&#39;inserzionista non sarà in grado di accedere DSP [!DNL On Demand Inventory].

**[!UICONTROL Advertiser URL]:** La homepage dell&#39;inserzionista o l&#39;URL principale del sito web (a partire da `http://` o `https://`).

**[!UICONTROL Share all private exchange feeds into this advertiser]:** (Solo per i nuovi account pubblicitari) Rende disponibili all’inserzionista tutti i feed di scambio privati configurati per l’account di DSP dell’organizzazione.

### [!UICONTROL Adobe IMS IDs]

Gli inserzionisti con prodotti Adobe Experience Cloud aggiuntivi possono condividere dati tra alcuni prodotti utilizzando ad Experience Cloud l’ID univoco dell’organizzazione. Puoi configurare integrazioni di prodotti specifiche nella sezione [!UICONTROL Integrations] sezione .

**[!UICONTROL Account IMS org and ID]:** (inserzionisti con prodotti di Experience Cloud aggiuntivi concessi in licenza tramite un account di Experience Cloud con più inserzionisti; facoltativo) l&#39;ID organizzazione Experience Cloud dell&#39;inserzionista.

**[!UICONTROL Advertiser IMS org and ID]:** (inserzionisti con licenze dirette per prodotti di Experience Cloud aggiuntivi; facoltativo) l&#39;ID organizzazione Experience Cloud dell&#39;inserzionista.

### [!UICONTROL Integrations]

(Facoltativo) Prodotti di Experience Cloud aggiuntivi collegati all’account DSP. I prodotti devono essere associati allo stesso ID organizzazione Experience Cloud fornito nel [!UICONTROL Adobe IMS IDs] sezione .

**[!UICONTROL Attribution services]** > **[!UICONTROL Adobe Media Optimizer]:** (Inserzionisti con [!DNL Adobe Advertising Search] o che utilizzano pixel di conversione della pubblicità di Adobe) A [!DNL Search] account con cui DSP scambiare i dati di attribuzione.

**[!UICONTROL Report suites]** > **[!UICONTROL Adobe Analytics]:** (inserzionisti con Adobe Analytics; facoltativo; applicabile solo ai dati raccolti utilizzando tag di monitoraggio delle conversioni di Adobe Advertising che includono [!DNL EF Redirect] e solo token) Uno o più [!DNL Analytics] suite di rapporti a cui DSP invierà i dati raccolti dagli editori e dai partner lato offerta. Analytics invierà inoltre i dati raccolti dal sito del cliente a DSP.

Affinché i dati vengano visualizzati nelle suite di rapporti, la [!DNL Search] impostazione a livello di inserzionista su &quot;[!UICONTROL Enable tracking for SAINT feeds]&quot; deve essere abilitato. Inoltre, l&#39;inserzionista [!DNL Analytics] l’account deve essere configurato per ricevere dati da Adobe Advertising.

>[!WARNING]
>
>Se rimuovi una suite di rapporti precedentemente collegata, DSP non scambierà più dati con tale suite. Ci si aspetta di vedere le fluttuazioni dei dati.

Per ulteriori informazioni sull’integrazione con [!DNL Analytics], vedi &quot;[Panoramica [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md).&quot;

**[!UICONTROL Audiences]** > **[!UICONTROL Adobe Analytics Cloud]:** (inserzionisti con Adobe Audience Manager o Adobe Analytics; facoltativo) un Audience Manager o [!DNL Analytics] account da cui DSP i metadati del segmento, i dati gerarchici e i dati di audience univoci per tutti i tipi di pubblico Adobi dell’inserzionista. Sono inclusi i dati per:

* Segmenti di Audience Manager
* [!DNL Analytics] segmenti pubblicati in Adobe Experience Cloud
* Segmenti creati in Adobe Experience Cloud utilizzando [!DNL People core service]
* Segmenti creati in Adobe Experience Platform e inviati ad Adobe Advertising tramite Audience Manager

La sincronizzazione iniziale richiede circa 24 ore. Dopo di che, i dati vengono sincronizzati in tempo reale, con un ritardo da uno a due secondi.
<!-- I don't think this is true anymore:
Segment membership data is sent to Adobe Advertising only after one of the following:

* The segment is targeted in an Adobe Advertising placement or audience library
* The segment is added to the Adobe Advertising batch and real-time destinations within the Audience Manager user interface
-->

## [!UICONTROL Targeting] Impostazioni

Facoltativamente, puoi configurare le destinazioni predefinite per i nuovi posizionamenti dell’inserzionista. Gli utenti possono ignorare le destinazioni predefinite per qualsiasi nuovo posizionamento.

### [!UICONTROL Geo-targeting]

**[!UICONTROL Countries]:** Il paese predefinito per il geotargeting di ogni posizionamento. Gli utenti possono modificare il paese e configurare un geotargeting più specifico per ogni posizionamento.

### [!UICONTROL Audience Targeting]

**[!UICONTROL Audiences to exclude]:** Qualsiasi pubblico o segmento da sopprimere per impostazione predefinita. Gli utenti possono modificare le esclusioni per ogni posizionamento.

### [!UICONTROL Media Quality]

#### [!UICONTROL Contextual Filtering]

Tipi di [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science]e [!DNL Peer39] filtri contestuali da applicare. È possibile ignorare le impostazioni a livello di inserzionista nella [livello di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-context}

**[!UICONTROL Block sites that are]:** (Facoltativo) Per impostazione predefinita, uno o più tipi di contesto di inventario da bloccare. Possono essere applicati costi aggiuntivi.

##### [!UICONTROL Peer 39] {#peer39-context}

**[!UICONTROL Target sites that are]:** (Facoltativo) Per impostazione predefinita, è necessario eseguire il targeting di uno o più tipi di attributi di inventario. Possono essere applicati costi aggiuntivi.

##### [!UICONTROL ComScore]

**[!UICONTROL Block sites that are]:** (Facoltativo) Per impostazione predefinita, uno o più tipi di attributi di inventario da bloccare. Possono essere applicati costi aggiuntivi.

##### [!UICONTROL Integral Ad Science] {#ias-context}

**[!UICONTROL Adult Content]:** (Facoltativo) Il grado di contenuto per adulti per cui bloccare gli annunci per impostazione predefinita: *[!UICONTROL Do Not Block]* (impostazione predefinita), *[!UICONTROL Standard]* oppure *[!UICONTROL Strict]*. Possono essere applicati costi aggiuntivi.

**[!UICONTROL Alcohol Content]:** (Facoltativo) Il grado di contenuto alcolico per il quale bloccare gli annunci per impostazione predefinita: *[!UICONTROL Do Not Block]* (impostazione predefinita), *[!UICONTROL Standard]* oppure *[!UICONTROL Strict]*. Possono essere applicati costi aggiuntivi.

#### [!UICONTROL Pre-Bid Fraud Blocking]

Tipi di siti da bloccare in base al traffico fraudolento e alle attività sospette misurate attraverso [!DNL DoubleVerify], [!DNL Integral Ad Science]e [!DNL Peer39]. È possibile ignorare le impostazioni a livello di inserzionista nella [livello di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-fraud}

**[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** Per impostazione predefinita, blocca tutto il traffico non valido al 100%, incluso il traffico su dispositivi in hijacked, per i nuovi posizionamenti. Possono essere applicati costi aggiuntivi.

**[!UICONTROL Also block sites with]:** (Facoltativo) Un ulteriore livello di frode e traffico non valido che causerà il blocco degli annunci da parte di DSP per impostazione predefinita:  *[!UICONTROL None]* (l’impostazione predefinita, che non blocca il traffico aggiuntivo), *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*, *[!UICONTROL >4% Average Fraud/IVT levels]*, *[!UICONTROL >6% Average Fraud/IVT levels]*, *[!UICONTROL >10% Average Fraud/IVT levels]* oppure *[!UICONTROL >25% Average Fraud/IVT levels]*. Possono essere applicati costi aggiuntivi.

##### [!UICONTROL Peer 39] {#peer-39-fraud}

**[!UICONTROL Block sites that are]:** (Facoltativo) Per impostazione predefinita, uno o più tipi di frode che DSP bloccare gli annunci: *[!UICONTROL Fraud]* (che blocca tutti i siti con frode), *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]* e/o *[!UICONTROL Fraud: Zero Ads]*. Possono essere applicati costi aggiuntivi.

##### [!UICONTROL Integral Ad Science] {#ias-fraud}

**[!UICONTROL Block sites that are]:** (Facoltativo) Un tipo di attività sospetta sul sito web o sull&#39;app che DSP bloccare gli annunci per impostazione predefinita: *[!UICONTROL None]* (l’impostazione predefinita, che non blocca gli annunci in base a attività sospette), *[!UICONTROL Suspicious Activity - High Risk]* oppure *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. Possono essere applicati costi aggiuntivi.

#### [!UICONTROL Ads.text]

**[!UICONTROL Ads.txt Filtering]:** Per impostazione predefinita, quale livello [[!DNL Ads.txt] filtro pre-offerta](https://iabtechlab.com/ads-txt-about/) da utilizzare sfruttando i [!DNL Authorized Digital Sellers] elenco:
* *[!UICONTROL Opt out of ads.txt (default)]*: Comprare l&#39;inventario da tutti i venditori.
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*: Per assegnare priorità all’acquisto di inventario da venditori e rivenditori diretti autorizzati di un dominio.
* *[!UICONTROL Ads.txt sellers only]*: Acquistare scorte solo da venditori e rivenditori diretti autorizzati di un dominio.
* *[!UICONTROL Ads.txt sellers only]*: Acquistare scorte solo da venditori diretti autorizzati di un dominio.

È possibile ignorare l’impostazione a livello di inserzionista nella [livello di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md).

#### [!UICONTROL Safe Site Block]

**[!UICONTROL Enable Site Safety Block]:** Per impostazione predefinita, abilita un filtro post-offerta in tempo reale per garantire che gli annunci servano sui siti di destinazione dell’inserzionista. <!-- Can remove this: Users can enable or disable the feature for each placement. I don't see this option, but I should probably verify. If this can't be edited at placement level, then remove "By default." If it can, say that you can override at placement level. -->

#### [!UICONTROL DoubleVerify Authentic Brand Safety]

**[!UICONTROL DoubleVerify Account]:** ([!DNL DoubleVerify] esclusivamente clienti; facoltativo) l&#39;ID del segmento di sicurezza del marchio associato al [!DNL DoubleVerify] conto.

**[!UICONTROL Enable Authentic Brand Safety]:** (Facoltativo) Per impostazione predefinita, abilita [!DNL DoubleVerify] Authentic Brand Safety, che blocca le impression dopo l’offerta utilizzando le regole di sicurezza del marchio personalizzate configurate per l’ID segmento specificato. DSP effettua la fatturazione dell’utilizzo del tuo account per l’ID del segmento.

È possibile ignorare l’impostazione a livello di inserzionista a livello di posizionamento.

>[!MORELIKETHIS]
>
>* [Creare un account inserzionista](/help/dsp/admin/advertiser-create.md)


<!-- >* [View the Advertiser List for the Account](/help/dsp/admin/advertiser-view.md) -->
