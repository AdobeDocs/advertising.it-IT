---
title: Sicurezza del marchio e qualità dei contenuti multimediali
description: Ulteriori informazioni sulle funzioni di sicurezza del brand e qualità dei contenuti multimediali.
feature: DSP Introduction
exl-id: 8cdfd517-4cdb-4dbc-aae5-a8bda1e4e95e
source-git-commit: e8cb734e313b6aecfb75dfcbf70347efe83254a5
workflow-type: tm+mt
source-wordcount: '1423'
ht-degree: 0%

---

# Sicurezza del marchio e qualità dei contenuti multimediali

<!-- Check on logo sizes in staging environment -- I made them all 100 pixels high except for DoubleVerify, which is 150 (harder to see at 100), but some instances look larger in VS Code. -->

Advertising DSP offre una suite di funzioni per la protezione del brand per garantire che ogni campagna raggiunga gli utenti reali in un ambiente sicuro per il brand.

Il nostro team di sorveglianza antifrode collabora con partner leader del settore, quali [!DNL Interactive Advertising Bureau], [!DNL Trust and Accountability Group] [!DNL (TAG)], e [!DNL WhiteOps], per curare attentamente l’inventario sulla nostra piattaforma. Attraverso la gestione proattiva della nostra offerta, l&#39;DSP garantisce che tutti gli inserzionisti sulla piattaforma siano protetti dal traffico non umano (bot, crawler, traffico del centro dati e frodi) e consegnino solo in contesti sicuri per il marchio.

Oltre a fornire una gestione centralizzata della qualità, crediamo nell’offrire agli inserzionisti la possibilità di progettare i controlli in linea con il proprio marchio. DSP offre integrazioni con [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], [!DNL Oracle Data Cloud], e [!DNL Peer39], assicurando che ogni inserzionista possa scegliere il livello desiderato di protezione dalle frodi, filtraggio contestuale e targeting delle parole chiave.

## Iniziative per la qualità

### Verifica magazzino con [!DNL Ads.txt] Supporto

[[!DNL Ads.txt], che sta per [!DNL Authorized Digital Sellers]](https://iabtechlab.com/ads-txt) è un&#39;iniziativa lanciata da [!DNL Interactive Advertising Bureau] ([!DNL IAB]) nel giugno 2017 per facilitare la corretta rappresentazione degli inventari sul mercato aperto, contrastando in tal modo le fonti illegittime di traffico e di spoofing dei domini. Gli editori e i distributori partecipanti dichiarano pubblicamente le società autorizzate a vendere il loro inventario digitale e la natura di tali relazioni, mantenendo un `ads.txt` pagina al livello principale del dominio (ad esempio `example.com/ads.txt`).

Supporto DSP [!DNL ads.txt] leggendo i `ads.txt` e offrendoti la possibilità di acquistare solo da verificato [!DNL ads.txt] venditori. Ad esempio, confrontando i venditori che vediamo accedere a `nytimes.com` al New York Times&quot; `ads.txt` file, possiamo identificare quali sono legittimi e quali non lo sono, e bloccheremo i trasgressori se il posizionamento è configurato per l&#39;acquisto solo da venditori verificati. <!-- can we actually mention NY Times? -->

È possibile impostare impostazioni predefinite [!DNL ads.txt] controlli per ogni inserzionista<!-- [default ads.txt controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->, quindi facoltativamente [personalizzare le impostazioni per ciascun posizionamento](/help/dsp/campaign-management/placements/placement-settings.md) a:

* acquista l&#39;inventario solo dai venditori diretti autorizzati di un dominio

* acquistare le scorte solo dai venditori diretti e dai rivenditori autorizzati di un dominio

* dare priorità all&#39;acquisto di scorte dai venditori diretti e dai rivenditori autorizzati di un dominio

* acquista l&#39;inventario da tutti i venditori

### Sorveglianza delle frodi della piattaforma

L&#39;DSP ha creato solidi strumenti e sistemi interni per gestire le frodi su tutta la nostra piattaforma, collaborando con i principali fornitori del settore come [!DNL Whiteops] e [!DNL Integral Ad Science].

Inoltre, Adobe lavora a stretto contatto con [!DNL IAB] e [!DNL TAG] per garantire un blocco delle frodi solido e conforme agli standard di settore per proteggere i nostri inserzionisti, utilizzando strumenti come [!DNL ads.txt] (vedere la sezione precedente), [!DNL IAB] Elenco di bot e ragni e [!DNL TAG] Elenco IP del centro dati.

Grazie al nostro approccio multidimensionale alla qualità, il nostro team monitora le anomalie e i pattern di traffico non validi, garantendo meno del 3% di traffico non valido nell’inventario protetto. Qualsiasi inventario sospetto, incluso quello relativo a domini specifici o proveniente da editori o venditori specifici, viene immediatamente bloccato sulla piattaforma.

### Mappatura inventario, suddivisione in livelli e categorizzazione

La mappatura dell’inventario è il processo dettagliato di revisione e onboarding necessario per tutti i nuovi inventari prima che vengano aggiunti alla nostra piattaforma. Tale processo è inteso a garantire la sicurezza e la qualità di tutti i dati di inventario relativi all&#39;DSP.

* **Mappatura:** Il nostro team di inventario esamina attentamente ogni dominio, valutando aspetti quali:

   * Sicurezza del brand

   * Verifica del tipo di annuncio

   * Contenuto generico, domini duplicati e servizi di annunci falsi

* **Livelli:** Esamina olisticamente la presenza del marchio nell’ecosistema complessivo per classificare l’inventario tra i diversi livelli. È possibile [eseguire il targeting dei posizionamenti](/help/dsp/campaign-management/placements/placement-settings.md) a questi livelli per il livello di portata desiderato:

   * **[!UICONTROL T1]** — Nome del marchio, siti riconosciuti a livello internazionale

   * **[!UICONTROL T2]** siti di grande impatto visivo, aggiornati, senza contenuti generati dagli utenti e solitamente privi di riconoscimento globale

   * **[!UICONTROL T3]** — Contenuti generati dagli utenti e contenuti di nicchia

* **Categorizzazione del sito:** Per facilitare il targeting e il blocco dei contenuti, a ogni proprietà viene assegnato un tag con una categoria di sito definita dall’DSP in base al contenuto della proprietà. È possibile [includi o escludi queste categorie del sito per ogni posizionamento](/help/dsp/campaign-management/placements/placement-settings.md) in base agli obiettivi di posizionamento.

### Supporto completo per il blocco del sito

L&#39;DSP fornisce sia un elenco di siti bloccati a livello globale sia l&#39;opzione per creare elenchi di siti bloccati personalizzati per gli inserzionisti e gli account.

#### Elenco siti bloccati a livello globale DSP {#global-blocked-sites}

L’DSP mantiene un elenco di siti bloccati a livello globale per i quali l’esecuzione di annunci è considerata non sicura. Questo elenco contiene siti con contenuti sgradevoli (come odio o terrore) e siti infetti da bot, pre-roll falso, domini non corrispondenti e altre attività fraudolente.

Come parte della nostra iniziativa Brand Safety per eliminare le attività che frodano gli inserzionisti, tutti i siti vengono controllati utilizzando le misure nell’elenco dei siti bloccati del grafico. Tutti i siti che non superano i controlli di sicurezza del marchio vengono aggiunti all’elenco dei siti bloccati a livello globale. Poiché l’DSP gestisce questo elenco in modo dinamico, i siti possono spostarsi in qualsiasi momento dall’elenco o viceversa, in base all’analisi più recente sulla sicurezza del marchio.

Quando si include un sito nell&#39;elenco dei siti bloccati a livello globale come destinazione di posizionamento, il sito viene contrassegnato con un punto esclamativo rosso (!). Ciò indica che gli annunci non vengono eseguiti sul sito contrassegnato.

>[!NOTE]
>
>Facoltativamente, puoi ignorare l’elenco globale dei siti bloccati per gli annunci display standard allegati a un’offerta privata attendibile abilitando l’opzione &quot;[!UICONTROL Allow unscreened sites]Opzione &quot; in [impostazioni di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md). Se necessario, il team dell’account Adobe può anche disattivare facoltativamente il blocco del sito per un’offerta pubblica (a livello di asta) nelle impostazioni dell’editore per l’offerta.

#### Elenchi di siti bloccati a livello di account e inserzionista

Gli utenti possono inoltre gestire elenchi di siti bloccati a livello di account e di inserzionista<!-- [account-level and advertiser-level blocked sites lists](/help/dsp/admin/blocked-sites-list-edit.md) -->, utilizzati automaticamente per tutti i posizionamenti. L&#39;elenco dei siti bloccati di livello inferiore viene applicato in aggiunta all&#39;elenco dei siti bloccati a livello globale.

## Integrazioni di terze parti

### Filtro contestuale

Il filtro contestuale consente di eseguire il targeting o bloccare le opportunità pubblicitarie in base al contesto della pagina a cui l’annuncio verrebbe distribuito. Adobe fornisce un filtro contestuale tramite integrazioni con i principali fornitori del settore: [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], e [!DNL Peer39]. Esempi di filtri correnti includono [!UICONTROL Adult Content], [!UICONTROL Natural Disasters], [!UICONTROL Legal Drinking Age], [!UICONTROL MANGA], [!UICONTROL Epidemics], e [!UICONTROL G-rated Sites].

È possibile impostare i controlli di filtro contestuali predefiniti per ogni inserzionista<!-- [default contextual filter controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->, quindi facoltativamente [personalizzare le impostazioni per ciascun posizionamento](/help/dsp/campaign-management/placements/placement-settings.md). Quando si utilizza questa funzione, è possibile che vengano applicate tariffe aggiuntive.

![Logo Comscore](/help/dsp/assets/comscore-logo.png) ![Logo DoubleVerify](/help/dsp/assets/doubleverify-logo.png) ![Logo Ad Science integrale](/help/dsp/assets/ias-logo.png) ![Logo Peer39](/help/dsp/assets/peer39-logo.png)

### Blocco di frodi pre-offerta

Sfruttare le integrazioni di terze parti con [!DNL DoubleVerify], [!DNL Integral Ad Science], e [!DNL Peer39] per bloccare il traffico non umano dalle campagne. Queste integrazioni forniscono funzionalità di blocco pre-offerta leader di settore per ridurre al minimo il traffico non valido generale e sofisticato (GIVT e SIVT) nelle campagne.

Puoi impostare i controlli di blocco delle frodi pre-offerta predefiniti per ogni inserzionista<!-- [default pre-bid fraud blocking controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->, quindi facoltativamente [personalizzare le impostazioni per ciascun posizionamento](/help/dsp/campaign-management/placements/placement-settings.md). Quando si utilizza questa funzione, è possibile che vengano applicate tariffe aggiuntive.

Per ulteriori informazioni sulle funzionalità, contatta direttamente il fornitore preferenziale o contatta il team del tuo account Adobe.

![Logo DoubleVerify](/help/dsp/assets/doubleverify-logo.png) ![Logo Ad Science integrale](/help/dsp/assets/ias-logo.png) ![Logo Peer39](/help/dsp/assets/peer39-logo.png)

### Visibilità pre-offerta {#pre-bid-viewability}

Filtri di visibilità pre-offerta forniti dai nostri partner leader del settore [!DNL DoubleVerify], [!DNL Oracle Advertising] ([!DNL Moat]), e [!DNL Integral Ad Science] consente agli inserzionisti di garantire che le campagne raggiungano gli obiettivi di prestazioni di visualizzabilità desiderati per l’intero inventario di video e display.

Puoi impostare filtri di visualizzabilità predefiniti per ogni inserzionista<!-- [default pre-viewability filters for each advertiser](/help/dsp/admin/advertiser-settings.md) -->, quindi facoltativamente [personalizzare le impostazioni per ciascun posizionamento](/help/dsp/campaign-management/placements/placement-settings.md). Quando si utilizza questa funzione, è possibile che vengano applicate tariffe aggiuntive.

![Logo DoubleVerify](/help/dsp/assets/doubleverify-logo.png) ![Logo Oracle Advertising](/help/dsp/assets/oracle-advertising-logo.png) ![Logo Ad Science integrale](/help/dsp/assets/ias-logo.png)

### Targeting e misurazione dell’attenzione

[!DNL Adobe's] partnership con [!DNL Adelaide] fornisce agli inserzionisti supporto per la metrica Adelaide &quot;.[!DNL Attention Units],&quot; che misura la qualità dei contenuti multimediali in base ai dati di tracciamento oculare, esposizione e risultato.

[Destinazione dell’attenzione pre-offerta a livello di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md) consente agli inserzionisti di mirare a livelli di attenzione specifici per migliorare il coinvolgimento dei clienti.

Inoltre, gli inserzionisti possono abilitare [tracciamento per il livello di posizionamento [!UICONTROL Attention Score] metrica](/help/dsp/campaign-management/campaigns/campaign-settings.md#attention-measurement) (il numero medio ponderato di [!DNL Attention Units] per tutte le campagne per capire quali tattiche di posizionamento producono i migliori risultati di business.

Per ogni funzione separata vengono applicate tariffe aggiuntive.

### Targeting argomento

Il targeting degli argomenti dell’DSP consente di eseguire il targeting o bloccare gli elenchi di parole chiave sfruttando i nostri partner contestuali leader di settore [!DNL Comscore] e [!DNL Oracle Data Cloud] (in precedenza [!DNL Grapeshot]). Il targeting degli argomenti ti aiuta a garantire che gli annunci vengano sempre serviti in un ambiente in linea con il tuo marchio, sia che si tratti di bloccare contenuti dannosi o di garantire la spesa in un contesto che garantisce un risultato maggiore.

Il targeting degli argomenti richiede di creare segmenti di argomenti personalizzati direttamente con la piattaforma partner. Una volta creati i segmenti, puoi [target o escludere un ID segmento nel [!UICONTROL Audience Targeting] sezione per ciascun posizionamento](/help/dsp/campaign-management/placements/placement-settings.md). Per questa funzione potrebbero essere applicati costi aggiuntivi.

Per creare segmenti di argomenti personalizzati:

* Per creare un [!DNL Comscore] e creare segmenti personalizzati, puoi richiedere un accesso per [!DNL Activation Segment Manager] a [https://agents.comscore.com](https://agents.comscore.com). Consulta la [[!DNL Comscore] centro risorse](https://comscoreactivation.zendesk.com/hc/) per istruzioni complete sulla configurazione di segmenti personalizzati. Le tariffe per i segmenti personalizzati sono visibili in [!DNL Segment Manager] durante la creazione.

* Per iniziare a utilizzare [!DNL Oracle Data Cloud], contatto [!DNL Oracle Data Cloud] o il tuo Account Team Adobe.

![Logo Comscore](/help/dsp/assets/comscore-logo.png) ![Logo Grapeshot](/help/dsp/assets/oracle-grapeshot-logo.png)

### [!DNL DoubleVerify Authentic Brand Safety]

L&#39;DSP ha collaborato con [!DNL DoubleVerify] per offrire i propri [!DNL Authentic Brand Safety] soluzione di targeting, che consente di creare un set centralizzato di requisiti di sicurezza del marchio da indirizzare a tutte le piattaforme di acquisto per coerenza.

Dopo aver creato un [!DNL DoubleVerify] con il targeting necessario, puoi utilizzarlo all’interno dell’DSP per replicare le regole del blocco post-offerta con pre-offerta in ambienti web.

È possibile specificare un [!DNL DoubleVerify] ID segmento per ogni inserzionista<!-- [specify a DoubleVerify segment ID for each advertiser](/help/dsp/admin/advertiser-settings.md) -->, quindi facoltativamente [abilitare o disabilitare [!UICONTROL Authentic Brand Safety] per ogni posizionamento](/help/dsp/campaign-management/placements/placement-settings.md). L’DSP fattura il tuo account per l’utilizzo dell’ID segmento.

Per ulteriori informazioni sulle funzionalità, contatta [!DNL DoubleVerify] direttamente o contatta il tuo Account Team Adobe.

![Logo DoubleVerify](/help/dsp/assets/doubleverify-logo.png)

>[!MORELIKETHIS]
>
>* [Impostazioni di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md)
<!-- >* [Advertiser Account Settings](/help/dsp/admin/advertiser-settings.md) -->
