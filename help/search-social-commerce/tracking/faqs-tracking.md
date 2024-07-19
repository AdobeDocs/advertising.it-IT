---
title: Domande frequenti sul tracciamento
description: Scopri le risposte alle domande comuni sul tracciamento, inclusa la risoluzione dei problemi.
exl-id: e5302c09-0b40-47ae-bc88-9299e6bd3044
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '1190'
ht-degree: 0%

---

# Domande frequenti sul tracciamento

## Funzioni di tracciamento

+++Posso tenere traccia di campagne che Adobe Advertising non gestisce?

Sì. Se Search, Social e Commerce sincronizzano uno degli account della rete di annunci, tiene traccia dei dati dei clic della rete di annunci per tutti i [tipi di campagna supportati](/help/search-social-commerce/introduction/supported-inventory.md) in tale account. Inoltre, tiene traccia dei dati di conversione se hai aggiunto il reindirizzamento Search, Social e Commerce agli URL di destinazione dell’annuncio e/o della parola chiave o ai modelli di tracciamento e hai implementato il tracciamento della conversione nelle pagine di conversione. Chiarisci con il tuo Account Team Adobe quali campagne desideri semplicemente monitorare in Search, Social e Commerce e quali desideri che gestiscano.
+++

+++Come si ottiene l’attribuzione multi-evento?

Per gli inserzionisti che utilizzano i tag di tracciamento delle conversioni di Search, Social e Commerce o Adobe Analytics, in Adobe Advertising sono disponibili diverse opzioni per l’attribuzione dei dati di conversione a una serie di eventi che portano a una conversione. Un’impostazione a livello di inserzionista determina come attribuire i dati di conversione tra gli eventi, anche quando si verificano tra più canali pubblicitari, purché i canali consentano il tracciamento delle impression a livello di evento. Per impostazione predefinita, le conversioni sono attribuite all’ultimo evento (più recente), ma l’impostazione può essere configurata in modo diverso, ad esempio per attribuire le conversioni al primo evento o per ponderare tutti gli eventi in modo uniforme. La modifica della regola di attribuzione influisce sul calcolo delle offerte future.

Gli inserzionisti che forniscono tutti i dati di conversione in un file di feed devono attribuire la conversione agli eventi di transazione correlati.

>[!NOTE]
>
>Nelle viste, nei rapporti e nelle simulazioni personalizzate (disponibili per alcuni utenti) di gestione delle campagne e del portfolio, puoi modificare la regola utilizzata per attribuire i dati di conversione all’interno delle viste e dei risultati dei rapporti, senza influire sul calcolo delle offerte future.

+++

+++In che modo Adobe Advertising identifica le transazioni duplicate?

Le transazioni duplicate possono verificarsi quando un utente aggiorna la pagina di conferma dopo aver completato una transazione. Adobe Advertising utilizza l&#39;attributo `ev_transid` per eliminare le transazioni duplicate con lo stesso ID transazione e lo stesso valore di proprietà.

Di seguito è riportata la logica di deduplicazione di Adobe Advertising:

* **Quando un client invia un valore per l&#39;attributo `ev_transid`:** Le successive richieste di pixel vengono considerate duplicati del precedente se i seguenti sono tutti uguali: `ev_transid`; l&#39;ID di tracciamento per la stessa parola chiave, annuncio o posizionamento; e il valore per una metrica di conversione specifica.

  Ad esempio, se più richieste di prestito hanno lo stesso ID applicazione e lo stesso importo prestito per la stessa parola chiave su una rete di annunci specifica, vengono considerate duplicati e viene conteggiata solo la prima richiesta di prestito.

* **Quando un client non invia un valore per l&#39;attributo `ev_transid`:** Le transazioni successive sono considerate duplicati di quelle precedenti se condividono un ID di tracciamento per la stessa parola chiave, annuncio o posizionamento e lo stesso valore per una metrica di conversione specifica.

  Ad esempio, se più richieste di prestito hanno lo stesso ID parola chiave e lo stesso importo del prestito, vengono considerate duplicati e viene conteggiata solo la prima richiesta di prestito.
+++

## Tipi di implementazione del tracciamento

+++Voglio interrompere l’utilizzo del servizio di tracciamento delle conversioni di Adobe Advertising per una o più campagne o account. Come posso rimuovere rapidamente il codice di tracciamento dagli URL di tracciamento?

Per prima cosa, rivolgiti al team del tuo account Adobe per comprendere le implicazioni della rimozione degli URL di tracciamento.

Nell&#39;account o nella campagna, modifica il metodo di tracciamento in &quot;[!UICONTROL No EF Redirect]&quot;. Quindi creare un bulksheet utilizzando l&#39;opzione &quot;[!UICONTROL Generate Tracking URLs]&quot; e pubblicarlo nella rete di annunci. Vengono sostituiti tutti gli URL di tracciamento o di destinazione esistenti.
+++

## Domande sui dati

+++Come faccio a sapere quale metrica di conversione proviene da un feed di dati o è tracciata dal tag di tracciamento della conversione di Adobe Advertising?

In un [!UICONTROL Transaction Report] è possibile stabilire se una metrica di conversione inclusa è stata tracciata dal pixel di tracciamento della conversione di Adobe Advertising se si include la colonna personalizzata &quot;[!UICONTROL Tracking URL]&quot;. Gli URL di tracciamento con il pixel di tracciamento Adobe Advertising iniziano con `http://pixel.everesttech.net`.
+++

+++Cosa sono le transazioni orfane?

Le transazioni orfane sono eventi di transazione che non possono essere associati a una parola chiave o a un annuncio specifico. Adobe Advertising attribuisce le transazioni/entrate a una parola chiave o a un annuncio confrontando gli ID di tracciamento ricevuti con l’evento entrate con l’ID di tracciamento univoco nell’URL di tracciamento della parola chiave o dell’annuncio.

Quando un Account Team Adobe sospetta che le transazioni orfane siano la causa di un calo dei ricavi, il team di Assistenza clienti controlla la presenza di orfani e, se ne trova qualcuno, indaga sul problema.

Gli orfani si verificano nelle seguenti situazioni.

**Implementazioni pixel**

Le transazioni orfane non si verificano quasi mai per le implementazioni pixel. Tuttavia, si sono verificati orfani nei pixel quando:

* I dati di clic non sono disponibili per la data di clic della conversione. In questo caso, i dati vengono mappati quando Search, Social e Commerce ottengono i dati dei clic dalla rete di annunci.

* I registri di clic non vengono elaborati prima dei registri di conversione.

**Implementazioni feed**

* L’ID di tracciamento inviato nel feed proviene da un account di cui Search, Social e Commerce non è a conoscenza.

* L&#39;account non è sincronizzato oppure si sono verificati errori durante il processo di sincronizzazione.

* L’ID di tracciamento è stato aggiunto e rimosso dalla rete pubblicitaria mentre Search, Social e Commerce non erano sincronizzati con la rete pubblicitaria, pertanto Search, Social e Commerce non dispongono di informazioni sull’ID. Questo problema continua a causare ricavi orfani in caso di ritardo nella ricezione dei ricavi.

* Il client ha inviato un ID di tracciamento formattato in modo errato nel feed e che non corrisponde all’ID di tracciamento nell’URL. Ciò si verifica in genere a causa di un problema di formattazione o quando gli ID di tracciamento vengono abbreviati nel feed.

* Nel file di configurazione, l’espressione regolare utilizzata per estrarre l’ID di tracciamento dagli URL non è corretta o è obsoleta. A volte l’inserzionista modifica l’ID di tracciamento nell’URL o adotta un sistema di tracciamento completamente nuovo, che richiede al team di implementazione di Search, Social e Commerce di aggiornare l’espressione regolare. In tali casi, una parte importante dei ricavi è orfana.

**Implementazioni di feed mediante un ID transazione**

Non sono disponibili transazioni online prima delle date in cui i dati sono disponibili nel feed offline.

**Implementazioni feed tramite un token (ef_id)**

Search, Social e Commerce non riescono a trovare un clic corrispondente sul loro server o sulla rete di annunci. Ciò può essere dovuto al fatto che i dati di clic non sono disponibili per la data di clic della conversione o (raramente) perché i registri di clic non sono stati elaborati prima dei registri di conversione. Quando Search, Social e Commerce ricevono i dati di clic dalla rete di annunci o i registri di clic vengono elaborati, i dati vengono mappati alla conversione.
+++

## Problemi di tracciamento dei ricavi

+++Come si correggono dati vecchi/errati da un file di feed?

Contatta l’Assistenza clienti per ricevere il file di dati corretto.
+++

+++Più parole chiave hanno gli stessi URL di tracciamento.

**Implicazioni**

Per le implementazioni di feed con più ID di tracciamento, i dati vengono segnalati in base a più parole chiave. Per altre implementazioni, le conversioni possono essere attribuite alla parola chiave sbagliata perché il sistema assegna arbitrariamente una conversione a una delle parole chiave.

**Possibile causa**

L’URL di una nuova parola chiave o di un nuovo annuncio è stato copiato da un’altra parola chiave o da un altro annuncio.

Questo non dovrebbe accadere con la visualizzazione o gli annunci social.

**Possibile soluzione o soluzione alternativa**

* Se gestisci le tue parole chiave e i tuoi annunci, crea un file bulksheet con gli URL corretti per gli URL duplicati e pubblicalo sull&#39;account appropriato utilizzando l&#39;opzione **[!UICONTROL Generate Tracking URLs]**, che rigenera gli URL per tutte le parole chiave e gli annunci.

* Se un Account Team di Adobi gestisce le parole chiave, chiedi loro di creare nuovi URL per gli URL duplicati.
+++
