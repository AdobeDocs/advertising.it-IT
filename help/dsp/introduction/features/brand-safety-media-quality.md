---
title: Sicurezza del marchio e qualità dei contenuti multimediali
description: Ulteriori informazioni sulle funzioni di sicurezza del brand e qualità dei contenuti multimediali.
feature: DSP Introduction
exl-id: 8cdfd517-4cdb-4dbc-aae5-a8bda1e4e95e
source-git-commit: 7ee798e11375863e776ac3e802efc9112280e750
workflow-type: tm+mt
source-wordcount: '1402'
ht-degree: 0%

---

# Sicurezza del marchio e qualità dei contenuti multimediali

<!-- Check on logo sizes in staging environment -- I made them all 100 pixels high except for DoubleVerify, which is 150 (harder to see at 100), but some instances look larger in VS Code. -->

Advertising DSP fornisce una suite di funzioni per la protezione del brand per garantire che ogni campagna raggiunga gli utenti reali in un ambiente sicuro per il brand.

Il nostro team di sorveglianza antifrode collabora a stretto contatto con partner leader del settore, come [!DNL Interactive Advertising Bureau], [!DNL Trust and Accountability Group] [!DNL (TAG)] e [!DNL WhiteOps], per curare attentamente l&#39;inventario sulla nostra piattaforma. Attraverso la gestione proattiva della nostra offerta, l&#39;DSP garantisce che tutti gli inserzionisti sulla piattaforma siano protetti dal traffico non umano (bot, crawler, traffico del centro dati e frodi) e consegnino solo in contesti sicuri per il marchio.

Oltre a fornire una gestione centralizzata della qualità, crediamo nell’offrire agli inserzionisti la possibilità di progettare i controlli in linea con il proprio marchio. DSP offre integrazioni con [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science] e [!DNL Peer39], garantendo che ogni inserzionista possa scegliere il livello desiderato di protezione dalle frodi, filtraggio contestuale e targeting delle parole chiave.

## Iniziative per la qualità

### Verifica dell&#39;inventario con supporto [!DNL Ads.txt]

[[!DNL Ads.txt], che sta per  [!DNL Authorized Digital Sellers]](https://iabtechlab.com/ads-txt) è un&#39;iniziativa lanciata da [!DNL Interactive Advertising Bureau] ([!DNL IAB]) nel giugno 2017 per facilitare la corretta rappresentazione dell&#39;inventario sul mercato aperto, contrastando in tal modo le fonti illegittime di traffico e spoofing dei domini. Gli editori e i distributori partecipanti dichiarano pubblicamente le società autorizzate a vendere il proprio inventario digitale e la natura di tali relazioni, mantenendo una pagina `ads.txt` al livello superiore del dominio (ad esempio `example.com/ads.txt`).

L&#39;DSP supporta [!DNL ads.txt] leggendo il file `ads.txt` di ogni editore e offrendoti la possibilità di acquistare solo da [!DNL ads.txt] venditori verificati. Ad esempio, confrontando i venditori che vediamo accedere a `nytimes.com` con il file `ads.txt` del New York Times, possiamo identificare quali sono legittimi e quali no, e bloccheremo i trasgressori se il posizionamento è configurato per l&#39;acquisto solo da venditori verificati. <!-- can we actually mention NY Times? -->

È possibile impostare [!DNL ads.txt] controlli predefiniti per ogni inserzionista<!-- [default ads.txt controls for each advertiser](/help/dsp/admin/advertiser-settings.md) --> e quindi [personalizzare le impostazioni per ogni posizionamento](/help/dsp/campaign-management/placements/placement-settings.md) in modo da:

* acquista l&#39;inventario solo dai venditori diretti autorizzati di un dominio

* acquistare le scorte solo dai venditori diretti e dai rivenditori autorizzati di un dominio

* dare priorità all&#39;acquisto di scorte dai venditori diretti e dai rivenditori autorizzati di un dominio

* acquista l&#39;inventario da tutti i venditori

### Sorveglianza delle frodi della piattaforma

DSP ha creato potenti strumenti e sistemi interni per gestire le frodi su tutta la piattaforma, collaborando con i principali fornitori del settore come [!DNL Whiteops] e [!DNL Integral Ad Science].

Inoltre, Adobe lavora a stretto contatto con [!DNL IAB] e [!DNL TAG] per garantire un blocco delle frodi solido e conforme agli standard di settore per proteggere i nostri inserzionisti, sfruttando strumenti come [!DNL ads.txt] (vedi la sezione precedente), l&#39;elenco Bot e Spiders di [!DNL IAB] e l&#39;elenco IP del data center di [!DNL TAG].

Grazie al nostro approccio multidimensionale alla qualità, il nostro team monitora le anomalie e i pattern di traffico non validi, garantendo meno del 3% di traffico non valido nell’inventario protetto. Qualsiasi inventario sospetto, incluso quello relativo a domini specifici o proveniente da editori o venditori specifici, viene immediatamente bloccato sulla piattaforma.

### Mappatura inventario, suddivisione in livelli e categorizzazione

La mappatura dell’inventario è il processo dettagliato di revisione e onboarding necessario per tutti i nuovi inventari prima che vengano aggiunti alla nostra piattaforma. Tale processo è inteso a garantire la sicurezza e la qualità di tutti i dati di inventario relativi all&#39;DSP.

* **Mappatura:** Il nostro team di inventario esamina attentamente ogni dominio, valutando aspetti quali:

   * Sicurezza del brand

   * Verifica del tipo di annuncio

   * Contenuto generico, domini duplicati e servizi di annunci falsi

* **Livelli:** Esamina olisticamente la presenza del brand nell&#39;ecosistema complessivo per classificare l&#39;inventario tra i diversi livelli. Puoi [eseguire il targeting dei posizionamenti](/help/dsp/campaign-management/placements/placement-settings.md) per questi livelli per il livello di portata desiderato:

   * **[!UICONTROL T1]** — Nome del marchio, siti riconosciuti a livello internazionale

   * **[!UICONTROL T2]** - Siti di grande impatto che sono aggiornati, senza contenuti generati dall&#39;utente e in genere privi di riconoscimento globale

   * **[!UICONTROL T3]** — Contenuto generato dall&#39;utente e contenuto di nicchia

* **Categorizzazione del sito:** Per facilitare il targeting e il blocco dei contenuti, a ogni proprietà viene applicata una categoria del sito definita dall&#39;DSP in base al contenuto della proprietà. Puoi [indirizzare o escludere queste categorie di siti per ogni posizionamento](/help/dsp/campaign-management/placements/placement-settings.md) in base agli obiettivi di posizionamento.

### Supporto completo per il blocco del sito

L&#39;DSP fornisce sia un elenco di siti bloccati a livello globale sia l&#39;opzione per creare elenchi di siti bloccati personalizzati per gli inserzionisti e gli account.

#### Elenco siti bloccati a livello globale DSP {#global-blocked-sites}

L’DSP mantiene un elenco di siti bloccati a livello globale per i quali l’esecuzione di annunci è considerata non sicura. Questo elenco contiene siti con contenuti sgradevoli (come odio o terrore) e siti infetti da bot, pre-roll falso, domini non corrispondenti e altre attività fraudolente.

Come parte della nostra iniziativa Brand Safety per eliminare le attività che frodano gli inserzionisti, tutti i siti vengono controllati utilizzando le misure nell’elenco dei siti bloccati del grafico. Tutti i siti che non superano i controlli di sicurezza del marchio vengono aggiunti all’elenco dei siti bloccati a livello globale. Poiché l’DSP gestisce questo elenco in modo dinamico, i siti possono spostarsi in qualsiasi momento dall’elenco o viceversa, in base all’analisi più recente sulla sicurezza del marchio.

Quando si include un sito nell&#39;elenco dei siti bloccati a livello globale come destinazione di posizionamento, il sito viene contrassegnato con un punto esclamativo rosso (!). Ciò indica che gli annunci non vengono eseguiti sul sito contrassegnato.

>[!NOTE]
>
>Facoltativamente, è possibile ignorare l&#39;elenco globale dei siti bloccati per gli annunci di visualizzazione standard allegati a un&#39;offerta privata attendibile abilitando l&#39;opzione &quot;[!UICONTROL Allow unscreened sites]&quot; nelle [impostazioni di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md). Se necessario, il team dell’account Adobe può anche disattivare facoltativamente il blocco del sito per un’offerta pubblica (a livello di asta) nelle impostazioni dell’editore per l’offerta.

#### Elenchi di siti bloccati a livello di account e inserzionista

Gli utenti possono inoltre gestire elenchi di siti bloccati a livello di account e di inserzionista<!-- [account-level and advertiser-level blocked sites lists](/help/dsp/admin/blocked-sites-list-edit.md) -->, che vengono utilizzati automaticamente per tutti i posizionamenti. L&#39;elenco dei siti bloccati di livello inferiore viene applicato in aggiunta all&#39;elenco dei siti bloccati a livello globale.

## Integrazioni di terze parti

### Filtro contestuale

Il filtro contestuale consente di eseguire il targeting o bloccare le opportunità pubblicitarie in base al contesto della pagina a cui l’annuncio verrebbe distribuito. Adobe fornisce un filtro contestuale tramite integrazioni con i principali fornitori del settore: [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science] e [!DNL Peer39]. Esempi di filtri correnti includono [!UICONTROL Adult Content], [!UICONTROL Natural Disasters], [!UICONTROL Legal Drinking Age], [!UICONTROL MANGA], [!UICONTROL Epidemics] e [!UICONTROL G-rated Sites].

È possibile impostare i controlli filtro contestuali predefiniti per ogni inserzionista<!-- [default contextual filter controls for each advertiser](/help/dsp/admin/advertiser-settings.md) --> e quindi [personalizzare le impostazioni per ogni posizionamento](/help/dsp/campaign-management/placements/placement-settings.md). Quando si utilizza questa funzione, è possibile che vengano applicate tariffe aggiuntive.

![Logo Comscore](/help/dsp/assets/comscore-logo.png) ![Logo DoubleVerify](/help/dsp/assets/doubleverify-logo.png) ![Logo Integral Ad Science](/help/dsp/assets/ias-logo.png) ![Logo Peer39](/help/dsp/assets/peer39-logo.png)

### Blocco di frodi pre-offerta

Sfrutta le integrazioni di terze parti con [!DNL DoubleVerify], [!DNL Integral Ad Science] e [!DNL Peer39] per bloccare il traffico non umano dalle campagne. Queste integrazioni forniscono funzionalità di blocco pre-offerta leader di settore per ridurre al minimo il traffico non valido generale e sofisticato (GIVT e SIVT) nelle campagne.

Puoi impostare i controlli di blocco delle frodi pre-offerta predefiniti per ogni inserzionista<!-- [default pre-bid fraud blocking controls for each advertiser](/help/dsp/admin/advertiser-settings.md) --> e quindi [personalizzare le impostazioni per ogni posizionamento](/help/dsp/campaign-management/placements/placement-settings.md). Quando si utilizza questa funzione, è possibile che vengano applicate tariffe aggiuntive.

Per ulteriori informazioni sulle funzionalità, contatta direttamente il fornitore preferenziale o contatta il team del tuo account Adobe.

![Logo DoubleVerify](/help/dsp/assets/doubleverify-logo.png) ![Logo Integral Ad Science](/help/dsp/assets/ias-logo.png) ![Logo Peer39](/help/dsp/assets/peer39-logo.png)

### Visibilità pre-offerta {#pre-bid-viewability}

I filtri di visibilità pre-offerta forniti dai nostri partner leader del settore [!DNL DoubleVerify] e [!DNL Integral Ad Science] consentono agli inserzionisti di garantire che le campagne raggiungano gli obiettivi di prestazioni di visualizzabilità desiderati nell&#39;inventario di video e display.

È possibile impostare filtri di visualizzabilità predefiniti per ogni inserzionista<!-- [default pre-viewability filters for each advertiser](/help/dsp/admin/advertiser-settings.md) --> e quindi [personalizzare le impostazioni per ogni posizionamento](/help/dsp/campaign-management/placements/placement-settings.md). Quando si utilizza questa funzione, è possibile che vengano applicate tariffe aggiuntive.

![Logo DoubleVerify](/help/dsp/assets/doubleverify-logo.png) ![Logo Integral Ad Science](/help/dsp/assets/ias-logo.png)

### Targeting e misurazione dell’attenzione

La partnership di [!DNL Adobe's] con [!DNL Adelaide] fornisce agli inserzionisti il supporto per la metrica di Adelaide &quot;[!DNL Attention Units]&quot;, che misura la qualità dei contenuti multimediali in base ai dati di tracciamento oculare, esposizione e risultato.

[Il targeting dell&#39;attenzione pre-offerta a livello di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md) consente agli inserzionisti di eseguire il targeting di livelli di attenzione specifici per migliorare il coinvolgimento dei clienti.

Inoltre, gli inserzionisti possono abilitare il tracciamento [&#x200B; per la metrica [!UICONTROL Attention Score] di livello posizionamento](/help/dsp/campaign-management/campaigns/campaign-settings.md#attention-measurement) (la media ponderata di [!DNL Attention Units] tra le impression) per qualsiasi campagna per capire quali tattiche di posizionamento producono i migliori risultati di business.

Per ogni funzione separata vengono applicate tariffe aggiuntive.

### Targeting argomento

Il targeting di argomenti DSP consente di eseguire il targeting o bloccare gli elenchi di parole chiave sfruttando il nostro partner contestuale leader del settore [!DNL Comscore]. Il targeting degli argomenti ti aiuta a garantire che gli annunci vengano sempre serviti in un ambiente in linea con il tuo marchio, sia che si tratti di bloccare contenuti dannosi o di garantire la spesa in un contesto che garantisce un risultato maggiore.

Il targeting degli argomenti richiede di creare segmenti di argomenti personalizzati direttamente con la piattaforma partner. Una volta creati i segmenti, puoi [individuare o escludere un ID segmento nella sezione [!UICONTROL Audience Targeting] per ogni posizionamento](/help/dsp/campaign-management/placements/placement-settings.md). Per questa funzione potrebbero essere applicati costi aggiuntivi.

Per creare un account [!DNL Comscore] e segmenti di argomenti personalizzati, è possibile richiedere l&#39;accesso per [!DNL Activation Segment Manager] all&#39;indirizzo [https://agents.comscore.com](https://agents.comscore.com). Per istruzioni complete sulla configurazione dei segmenti personalizzati, consulta il [[!DNL Comscore] Centro assistenza](https://comscoreactivation.zendesk.com/hc/). Le tariffe per i segmenti personalizzati sono visibili in [!DNL Segment Manager] durante la creazione.

![Logo Comscore](/help/dsp/assets/comscore-logo.png)

### [!DNL DoubleVerify Authentic Brand Safety]

DSP ha collaborato con [!DNL DoubleVerify] per offrire la sua soluzione di targeting [!DNL Authentic Brand Safety], che consente di creare un set centralizzato di requisiti di sicurezza del brand per eseguire il targeting su tutte le piattaforme di acquisto per coerenza.

Dopo aver creato un segmento di sicurezza del brand [!DNL DoubleVerify] con il targeting necessario, puoi utilizzarlo all&#39;interno dell&#39;DSP per replicare le regole del blocco post-offerta con pre-offerta tra gli ambienti web.

È possibile specificare un ID segmento [!DNL DoubleVerify] per ogni inserzionista<!-- [specify a DoubleVerify segment ID for each advertiser](/help/dsp/admin/advertiser-settings.md) --> e quindi, facoltativamente, [abilitare o disabilitare [!UICONTROL Authentic Brand Safety] per ogni posizionamento](/help/dsp/campaign-management/placements/placement-settings.md). L’DSP fattura il tuo account per l’utilizzo dell’ID segmento.

Per ulteriori informazioni sulle funzionalità, contattare direttamente [!DNL DoubleVerify] o il team dell&#39;account Adobe.

![Logo DoubleVerify](/help/dsp/assets/doubleverify-logo.png)

>[!MORELIKETHIS]
>
>* [Impostazioni posizionamento](/help/dsp/campaign-management/placements/placement-settings.md)
<!-- >* [Advertiser Account Settings](/help/dsp/admin/advertiser-settings.md) -->
