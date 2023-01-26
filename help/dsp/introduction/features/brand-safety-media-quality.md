---
title: Sicurezza del marchio e qualità dei supporti
description: Ulteriori informazioni sulla sicurezza del marchio e sulle funzioni di qualità dei supporti.
feature: DSP Introduction
exl-id: 8cdfd517-4cdb-4dbc-aae5-a8bda1e4e95e
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '1350'
ht-degree: 0%

---

# Sicurezza del marchio e qualità dei supporti

<!-- Check on logo sizes in staging environment -- I made them all 100 pixels high except for DoubleVerify, which is 150 (harder to see at 100), but some instances look larger in VS Code. -->

Advertising DSP fornisce una suite di funzioni di protezione del marchio per garantire che ogni campagna raggiunga utenti reali in un ambiente sicuro per il marchio.

Il nostro team per la sorveglianza delle frodi collabora strettamente con partner leader del settore, come [!DNL Interactive Advertising Bureau], [!DNL Trust and Accountability Group] [!DNL (TAG)]e [!DNL WhiteOps], per curare attentamente l&#39;inventario sulla nostra piattaforma. Attraverso una gestione proattiva della nostra offerta, DSP garantisce che tutti gli inserzionisti della piattaforma siano protetti dal traffico non umano (bot, crawler, traffico datacenter e frode) e consegnati solo in contesti sicuri per il marchio.

Oltre a fornire una gestione centralizzata della qualità, crediamo nell&#39;autorizzare gli inserzionisti a progettare i controlli che si allineano con il loro marchio. DSP offre integrazioni con [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], [!DNL Oracle Data Cloud]e [!DNL Peer39], assicurando che ogni inserzionista possa scegliere il livello desiderato di protezione dalle frodi, filtro contestuale e targeting tramite parole chiave.

## Iniziative per la qualità

### Verifica dell&#39;inventario con [!DNL Ads.txt] Supporto

[[!DNL Ads.txt], che rappresenta [!DNL Authorized Digital Sellers]](https://iabtechlab.com/ads-txt) è un&#39;iniziativa lanciata dalla [!DNL Interactive Advertising Bureau] ([!DNL IAB]) nel giugno 2017 per facilitare la corretta rappresentazione dell&#39;inventario sul mercato aperto, combattendo in tal modo le fonti illegali di traffico e lo spoofing del dominio. Gli editori e i distributori partecipanti dichiarano pubblicamente le società autorizzate a vendere il loro inventario digitale e la natura di tali relazioni, mantenendo un `ads.txt` al livello superiore del dominio (ad esempio `example.com/ads.txt`).

Supporti DSP [!DNL ads.txt] leggendo i `ads.txt` e ti offre la possibilità di acquistare solo da verificato [!DNL ads.txt] venditori. Ad esempio, confrontando i venditori, vediamo l&#39;accesso `nytimes.com` al New York Times&quot; `ads.txt` file, possiamo identificare quali sono legittimi e quali no, e bloccheremo i trasgressori se il posizionamento è configurato per l&#39;acquisto solo da venditori verificati. <!-- can we actually mention NY Times? -->

È possibile impostare il valore predefinito [!DNL ads.txt] controlli per ogni inserzionista<!-- [default ads.txt controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->, e quindi facoltativamente [personalizzare le impostazioni per ogni posizionamento](/help/dsp/campaign-management/placements/placement-settings.md) a:

* acquista inventario solo da venditori diretti autorizzati di un dominio

* acquista inventario solo da rivenditori e venditori diretti autorizzati di un dominio

* priorità all&#39;acquisto di inventario da venditori e rivenditori diretti autorizzati di un dominio

* acquista inventario da tutti i venditori

### Sorveglianza delle frodi su piattaforma

DSP ha creato potenti strumenti e sistemi interni per gestire le frodi su tutta la nostra piattaforma, collaborando con i principali fornitori del settore come [!DNL Whiteops] e [!DNL Integral Ad Science].

Inoltre, Adobe collabora strettamente con [!DNL IAB] e [!DNL TAG] per garantire un blocco solido e standard del settore delle frodi per proteggere i nostri inserzionisti, sfruttando strumenti come [!DNL ads.txt] (vedi la sezione precedente), [!DNL IAB] Elenco dei bot e dei ragni e [!DNL TAG] Elenco IP del centro dati.

Attraverso il nostro approccio multidimensionale alla qualità, il nostro team monitora le anomalie e i pattern di traffico non validi, garantendo meno del 3% di traffico non valido sull’inventario protetto. Qualsiasi inventario sospetto, compreso l&#39;inventario su domini specifici o presso editori o venditori specifici, viene immediatamente bloccato in tutta la piattaforma.

### Mappatura dell’inventario, suddivisione in più livelli e categorizzazione

La mappatura dell’inventario è il processo dettagliato di revisione e onboarding richiesto per tutto il nuovo inventario prima che venga aggiunto alla nostra piattaforma. Questo processo è progettato per garantire la sicurezza e la qualità di tutto l&#39;inventario su DSP.

* **Mappatura:** Il nostro team di Inventory esamina attentamente ogni dominio, valutando aspetti quali:

   * Sicurezza del marchio

   * Verifica del tipo di annuncio

   * Contenuto generico, domini duplicati e servizio annunci falsi

* **Livelli:** Esamina olisticamente la presenza del marchio nell&#39;ecosistema complessivo per classificare l&#39;inventario su diversi livelli. È possibile [eseguire il targeting dei posizionamenti](/help/dsp/campaign-management/placements/placement-settings.md) a questi livelli per il livello di portata desiderato:

   * **[!UICONTROL T1]** - Marca, siti riconoscibili a livello internazionale

   * **[!UICONTROL T2]** - Grandi siti aggiornati, privi di contenuti generati dagli utenti e generalmente privi di riconoscimento globale

   * **[!UICONTROL T3]** - Contenuti generati dall&#39;utente e contenuti di nicchia

* **Classificazione del sito:** Per facilitare il targeting e il blocco dei contenuti, taggiamo ogni proprietà con una categoria di sito definita DSP in base al contenuto della proprietà. È possibile [eseguire il targeting o escludere queste categorie di siti per ogni posizionamento](/help/dsp/campaign-management/placements/placement-settings.md) in base agli obiettivi di posizionamento.

### Supporto completo per il blocco del sito

DSP fornisce sia un elenco di siti bloccati a livello globale che l&#39;opzione per creare elenchi di siti bloccati personalizzati per gli inserzionisti e gli account.

#### DSP elenco dei siti bloccati a livello globale {#global-blocked-sites}

DSP mantiene un elenco di siti bloccati a livello globale di siti ritenuti non sicuri per eseguire annunci su. Questo elenco contiene siti con contenuti discutibili (come odio o terrore) e siti infettati da bot, falsi pre-roll, domini non corrispondenti e altre attività fraudolente.

Come parte della nostra iniziativa Brand Safety per eliminare le attività che truffano gli inserzionisti, tutti i siti vengono controllati utilizzando le misure nella lista dei siti bloccati del grafico. Tutti i siti che non superano i controlli di sicurezza del marchio vengono aggiunti all’elenco dei siti bloccati a livello globale. Poiché DSP gestire questo elenco in modo dinamico, i siti possono passare o uscire dall’elenco in qualsiasi momento, in base all’ultima analisi sulla sicurezza del marchio.

Quando includi un sito nell’elenco dei siti bloccati a livello globale come destinazione di posizionamento, il sito viene contrassegnato con un punto esclamativo rosso (!). Questo indica che gli annunci non verranno eseguiti sul sito contrassegnato.

>[!NOTE]
>
>Facoltativamente, puoi ignorare l&#39;elenco dei siti bloccati globali per gli annunci display standard allegati a un&#39;offerta privata attendibile abilitando &quot;[!UICONTROL Allow unscreened sites]&quot; nella [impostazioni di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md). Se necessario, il [!DNL Adobe] il team dell&#39;account può anche disattivare il blocco del sito per un&#39;offerta pubblica (a livello di asta) nelle impostazioni dell&#39;editore per l&#39;offerta.

#### Elenchi di siti bloccati a livello di account e di inserzionista

Gli utenti possono inoltre mantenere elenchi di siti bloccati a livello di account e di inserzionista<!-- [account-level and advertiser-level blocked sites lists](/help/dsp/admin/blocked-sites-list-edit.md) -->, che vengono utilizzati automaticamente per tutti i posizionamenti. L&#39;elenco dei siti bloccati di livello inferiore viene applicato in aggiunta all&#39;elenco dei siti bloccati a livello globale.

## Integrazioni di terze parti

### Filtro contestuale

Il filtro contestuale consente di eseguire il targeting o bloccare le opportunità pubblicitarie in base al contesto della pagina in cui l’annuncio verrebbe servito. Adobe fornisce filtri contestuali tramite integrazioni con i principali fornitori del settore: [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science]e [!DNL Peer39]. Esempi di filtri correnti includono [!UICONTROL Adult Content], [!UICONTROL Natural Disasters], [!UICONTROL Legal Drinking Age], [!UICONTROL MANGA], [!UICONTROL Epidemics]e [!UICONTROL G-rated Sites].

Puoi impostare i controlli del filtro contestuale predefiniti per ogni inserzionista<!-- [default contextual filter controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->, e quindi facoltativamente [personalizzare le impostazioni per ogni posizionamento](/help/dsp/campaign-management/placements/placement-settings.md). È possibile applicare tariffe aggiuntive quando si utilizza questa funzione.

![Logo Comscore](/help/dsp/assets/comscore-logo.png) ![Logo DoubleVerify](/help/dsp/assets/doubleverify-logo.png) ![Logo Integral Ad Science](/help/dsp/assets/ias-logo.png) ![Logo Peer39](/help/dsp/assets/peer39-logo.png)

### Blocco di frodi pre-offerta

Sfrutta le integrazioni di terze parti con [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science]e [!DNL Peer39] per bloccare il traffico non umano dalle campagne. Queste integrazioni forniscono funzionalità di blocco pre-bid leader di settore per ridurre al minimo il traffico generico e sofisticato non valido (GIVT e SIVT) nelle campagne.

Puoi impostare i controlli predefiniti di blocco della frode pre-offerta per ogni inserzionista<!-- [default pre-bid fraud blocking controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->, e quindi facoltativamente [personalizzare le impostazioni per ogni posizionamento](/help/dsp/campaign-management/placements/placement-settings.md). È possibile applicare tariffe aggiuntive quando si utilizza questa funzione.

Per ulteriori informazioni sulle funzionalità, contatta direttamente il tuo fornitore preferito o contatta il tuo [!DNL Adobe] team di account.

![Logo Comscore](/help/dsp/assets/comscore-logo.png) ![Logo DoubleVerify](/help/dsp/assets/doubleverify-logo.png) ![Logo Integral Ad Science](/help/dsp/assets/ias-logo.png) ![Logo Peer39](/help/dsp/assets/peer39-logo.png)

### Visualizzazione pre-offerta {#pre-bid-viewability}

Filtri di visualizzabilità pre-offerta gestiti dai nostri partner leader del settore [!DNL DoubleVerify], [!DNL Oracle Advertising] ([!DNL Moat]) e [!DNL Integral Ad Science] consentono agli inserzionisti di garantire che le loro campagne soddisfino i loro obiettivi di prestazioni di visualizzazione desiderati in tutto l’inventario video e display.

È possibile impostare filtri di visualizzazione predefiniti per ogni inserzionista<!-- [default pre-viewability filters for each advertiser](/help/dsp/admin/advertiser-settings.md) -->, e quindi facoltativamente [personalizzare le impostazioni per ogni posizionamento](/help/dsp/campaign-management/placements/placement-settings.md). È possibile applicare tariffe aggiuntive quando si utilizza questa funzione.

![Logo DoubleVerify](/help/dsp/assets/doubleverify-logo.png) ![Logo Oracle Advertising](/help/dsp/assets/oracle-advertising-logo.png) ![Logo Integral Ad Science](/help/dsp/assets/ias-logo.png)

### Targeting dell&#39;argomento

DSP targeting degli argomenti ti consente di eseguire il targeting o bloccare elenchi di parole chiave sfruttando i nostri partner contestuali leader del settore [!DNL Comscore] e [!DNL Oracle Data Cloud] ([!DNL Grapeshot]). Il targeting degli argomenti ti consente di garantire che gli annunci vengano sempre serviti in un ambiente che si allinea al tuo marchio, che includa il blocco dei contenuti dannosi o la garanzia della spesa in un contesto che garantisca un risultato migliore.

Per il targeting degli argomenti è necessario creare segmenti di argomenti personalizzati direttamente con [!DNL Comscore] o [!DNL Grapeshot] (utilizzando [!DNL Oracle Data Cloud]). Una volta creati nella piattaforma partner, puoi [eseguire il targeting o escludere un ID segmento nel [!UICONTROL Audience Targeting] sezione per ogni posizionamento](/help/dsp/campaign-management/placements/placement-settings.md). Per questa funzione possono essere applicati costi aggiuntivi.

Per creare segmenti di argomento personalizzati:

* Per creare una [!DNL Comscore] e crea segmenti personalizzati, puoi richiedere un accesso per [!DNL Activation Segment Manager] a [https://agents.comscore.com](https://agents.comscore.com). Consulta la sezione [[!DNL Comscore] centro di assistenza](https://comscoreactivation.zendesk.com/hc/) per istruzioni complete sulla configurazione di segmenti personalizzati. Le tariffe per i segmenti personalizzati sono visibili in [!DNL Segment Manager] quando le crei.

* Per iniziare a utilizzare [!DNL Oracle Data Cloud], contatto [!DNL Oracle Data Cloud] o [!DNL Adobe] team di account.

![Logo Comscore](/help/dsp/assets/comscore-logo.png) ![Logo della Grappa](/help/dsp/assets/oracle-grapeshot-logo.png)

### [!DNL DoubleVerify Authentic Brand Safety]

DSP ha collaborato con [!DNL DoubleVerify] offrire [!DNL Authentic Brand Safety] soluzione di targeting, che ti consente di creare un set centralizzato di requisiti di sicurezza del brand da indirizzare a tutte le piattaforme di acquisto per coerenza.

Una volta costruito un [!DNL DoubleVerify] segmento di sicurezza del brand con il targeting necessario, puoi utilizzarlo in DSP per replicare le regole di blocco post-bid con pre-bid in ambienti web.

Puoi specificare un [!DNL DoubleVerify] ID segmento per ogni inserzionista<!-- [specify a DoubleVerify segment ID for each advertiser](/help/dsp/admin/advertiser-settings.md) -->, e quindi facoltativamente [abilitare o disabilitare [!UICONTROL Authentic Brand Safety] per ogni posizionamento](/help/dsp/campaign-management/placements/placement-settings.md). DSP effettua la fatturazione dell’utilizzo del tuo account per l’ID del segmento.

Per ulteriori informazioni sulle funzionalità, contatta [!DNL DoubleVerify] direttamente o contattate il vostro [!DNL Adobe] team di account.

![Logo DoubleVerify](/help/dsp/assets/doubleverify-logo.png)

>[!MORELIKETHIS]
>
>* [Impostazioni di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md)

<!-- >* [Advertiser Account Settings](/help/dsp/admin/advertiser-settings.md) -->
