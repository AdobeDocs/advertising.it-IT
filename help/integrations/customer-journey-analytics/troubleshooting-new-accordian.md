---
title: Risoluzione dei problemi dei dati di Adobe Advertising in Customer Journey Analytics
description: Scopri come risolvere i problemi relativi ai dati di Adobe Advertising in Customer Journey Analytics.
feature: Integration with Adobe Customer Journey Analytics
hide: true
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: b3b90fc7d453a9450f5858e47ae4c05243808a03
workflow-type: tm+mt
source-wordcount: 3018
ht-degree: 0%

---

# Risoluzione dei problemi dei dati di Adobe Advertising in Customer Journey Analytics

Di seguito sono riportati i potenziali problemi, le loro possibili cause e le soluzioni.

## Elenco di tutti i potenziali sintomi

| Sintomo | Ulteriori informazioni |
| ------- | ---------------- |
| Nessuna chiamata alloy() visibile nella scheda di rete del browser | Consulta la sezione &quot;[Problemi di installazione e configurazione](#issues-installation-setup)&quot; > &quot;[L&#39;estensione WebSDK non viene inizializzata](#websdk-extension-doesn't-initialize)&quot; |
| Errore della console: la lega non è definita | Vedi &quot;[Problemi di installazione e configurazione](#issues-installation-setup)&quot; > &quot;[L&#39;estensione WebSDK non viene inizializzata](#websdk-extension-doesn't-initialize)&quot; |
| Nessuna richiesta di interazione o raccolta a edge.adobedc.net | Vedi &quot;[Problemi di installazione e configurazione](#issues-installation-setup)&quot; > &quot;[L&#39;estensione WebSDK non viene inizializzata](#websdk-extension-doesn't-initialize)&quot; |
| Le richieste arrivano al server Edge ma restituiscono errori 400 o 500 | Consulta la sezione &quot;[Problemi di installazione e configurazione](#issues-installation-setup)&quot; > &quot;[Datastream non configurato o non configurato correttamente](#datastream-not-configured-or-misconfigured)&quot; |
| Nei rapporti di Adobe Analytics o Adobe Advertising non viene visualizzato alcun dato | Consulta la sezione &quot;[Problemi di installazione e configurazione](#issues-installation-setup)&quot; > &quot;[Datastream non configurato o non configurato correttamente](#datastream-not-configured-or-misconfigured)&quot; |
| Errore nella risposta di rete: &quot;datastream non trovato&quot; | Consulta la sezione &quot;[Problemi di installazione e configurazione](#issues-installation-setup)&quot; > &quot;[Datastream non configurato o non configurato correttamente](#datastream-not-configured-or-misconfigured)&quot; |
| L&#39;ID visitatore cambia da pagina a pagina | Consulta la sezione &quot;[Problemi di installazione e configurazione](#issues-installation-setup)&quot; > &quot;[Problemi di identità e ECID](#identity-and-ecid-issues)&quot; |
| I segmenti di pubblico di Advertising non corrispondono | Consulta la sezione &quot;[Problemi di installazione e configurazione](#issues-installation-setup)&quot; > &quot;[Problemi di identità e ECID](#identity-and-ecid-issues)&quot; |
| Il debugger mostra che le condizioni della regola non sono soddisfatte | Consulta la sezione &quot;[Problemi di installazione e configurazione](#issues-installation-setup)&quot; > &quot;[Le regole o gli eventi non vengono attivati](#rules-or-events-aren't-firing)&quot; |
| L&#39;azione [!UICONTROL Send Event] non viene mai eseguita | Consulta la sezione &quot;[Problemi di installazione e configurazione](#issues-installation-setup)&quot; > &quot;[Le regole o gli eventi non vengono attivati](#rules-or-events-aren't-firing)&quot; |
| Le modifiche apportate in [!DNL Tags] non si riflettono sul sito live | Consulta la sezione &quot;[Problemi di installazione e configurazione](#issues-installation-setup)&quot; > &quot;[Problemi di compilazione e pubblicazione della libreria](#library-build-and-publishing-issues)&quot; |
| È stato applicato un aggiornamento dell’estensione, ma il comportamento precedente persiste | Consulta la sezione &quot;[Problemi di installazione e configurazione](#issues-installation-setup)&quot; > &quot;[Problemi di compilazione e pubblicazione della libreria](#library-build-and-publishing-issues)&quot; |
| La chiamata dell&#39;evento di invio `alloy()` ha esito positivo (con una risposta 200), ma i dati di conversione di Adobe Advertising non sono presenti nei rapporti | Consulta la sezione &quot;[Problemi di installazione e configurazione](#issues-installation-setup)&quot; > &quot;[Problemi di convalida dello schema per i campi di Advertising](#schema-validation-for-advertising-fields)&quot; |
| Il payload XDM nel debugger non mostra alcun oggetto `_experience.adcloud` | Consulta la sezione &quot;[Problemi di installazione e configurazione](#issues-installation-setup)&quot; > &quot;[Problemi di convalida dello schema per i campi di Advertising](#schema-validation-for-advertising-fields)&quot; |
| Non vengono registrate conversioni view-through o click-through per la pagina web | Consulta la sezione &quot;[Problemi di configurazione dell&#39;estensione Advertising](#advertising-extension-setup-issues)&quot; |
| Manca `_experience.adcloud` nel payload Experience Data Model (XDM) per i click-through | Consulta la sezione &quot;[Problemi di configurazione dell&#39;estensione Advertising](#advertising-extension-setup-issues)&quot; |
| Le conversioni vengono confermate in uno strumento di debug ma non vengono visualizzate nei rapporti di Adobe Advertising | Consulta la sezione &quot;[Problemi di configurazione dell&#39;estensione Advertising](#advertising-extension-setup-issues)&quot; |

## Problemi di installazione e configurazione {#issues-installation-setup}

### L’estensione WebSDK non inizializza {#websdk-extension-doesn-initialize}

Sintomi:

* Nessuna chiamata alloy() visibile nella scheda di rete del browser
* Errore della console: la lega non è definita
* Nessuna richiesta di interazione o raccolta a edge.adobedc.net

+++ Libreria non pubblicata o in stato di bozza

Vai a [Flusso di pubblicazione](https://experienceleague.adobe.com/it/docs/experience-platform/tags/publish/publishing-flow) e assicurati che la libreria che contiene l&#39;estensione WebSDK sia nello stato approvato/pubblicato.

+++

+++ Codice di incorporamento mancante o ambiente errato

Verificare che il codice di incorporamento [!DNL Tags] nella pagina Web faccia riferimento all&#39;ambiente corretto (Dev/Stage/Prod). Cercare l&#39;ambiente nel tag `<head>` per il tag di script `//assets.adobedtm.com/...`.

+++

+++ Conflitto tra carico asincrono e carico sincrono

Verificare che sia presente un solo codice di incorporamento [!DNL Tags] per pagina Web. I codici di incorporamento duplicati causano race condition.

+++

+++ Blocco di Content Security Policy (CSP)

Aggiungi `edge.adobedc.net` e `assets.adobedtm.com` al tuo CSP `connect-src` e `script-src` direttive.

+++

### Stream di dati non configurato o non configurato correttamente {#datastream-not-configured-or-misconfigured}

Sintomi:

* Le richieste arrivano al server Edge ma restituiscono errori 400 o 500
* Nessun dato visualizzato nei report di Adobe Analytics o Adobe Advertising<!-- It's not useful to organize this info by cause, not symptom -->
* Errore nella risposta di rete: &quot;datastream non trovato&quot;

+++ L’ID dello stream di dati per la proprietà tag è mancante o non corretto

1. In [!DNL Tags], apri le [impostazioni di configurazione dello stream di dati](https://experienceleague.adobe.com/it/docs/experience-platform/tags/extensions/client/web-sdk/configure/datastreams) per la proprietà tag.
1. Verificare che il campo [!UICONTROL Datastream] punti allo stream di dati corretto per ogni ambiente (sviluppo, staging e produzione), nonché allo schema e al set di dati corretti.

   Ogni ambiente deve avere un proprio stream di dati, a meno che tu non condivida esplicitamente un solo stream di dati in tutti e tre gli ambienti.

+++

+++ I servizi stream di dati non sono abilitati per la proprietà tag

[Aprire le impostazioni dello stream di dati](https://experienceleague.adobe.com/it/docs/experience-platform/datastreams/configure) e verificare che i servizi seguenti siano abilitati:

* Adobe Advertising (per conversione/sincronizzazione pubblico)
* Adobe Experience Platform (per l’acquisizione del profilo)

+++

+++ Sandbox non corrispondente

Assicurati che lo stream di dati appartenga alla stessa sandbox di Adobe Experience Platform dello schema e del set di dati. Un errore comune è la creazione di un flusso di dati nella sandbox di produzione, ma il fatto di puntare gli schemi alla sandbox di sviluppo.

+++

### Problemi relativi a identità ed ECID {#identity-and-ecid-issues}

Sintomi:

* L&#39;ID visitatore cambia da pagina a pagina
* I segmenti di pubblico di Advertising non corrispondono

+++ I cookie di terze parti sono bloccati

Esegui la migrazione alla raccolta dati CNAME di prime parti configurando un dominio di prime parti nella configurazione Edge dello stream di dati.

+++

+++ `idMigrationEnabled` è impostato su `false` mentre è presente un cookie `s_ecid` legacy

Impostare `idMigrationEnabled: true` nella configurazione di base WebSDK per migrare l&#39;ECID esistente dai cookie `s_ecid` o `AMCV_`.

+++

### Le regole o gli eventi non attivano {#rules-or-events-aren-firing}

Sintomi:

* Il debugger mostra che le condizioni della regola non sono soddisfatte
* L&#39;azione [!UICONTROL Send Event] non viene mai eseguita

Verifica quanto segue:

* La regola viene salvata e inclusa nella build della libreria attiva.
* Il tipo di evento corrisponde al comportamento effettivo della pagina (ad esempio [!UICONTROL Library Loaded] rispetto a [!UICONTROL DOM Ready] rispetto a [!UICONTROL Window Loaded]).
* Le condizioni della regola non sono troppo restrittive. Esegui il test rimuovendo temporaneamente le condizioni per isolare il problema.
* Ordine delle regole corretto. Se più regole condividono lo stesso evento, controlla l’ordine delle regole.
* Nessun errore JavaScript precedente nella pagina sta interrompendo l’esecuzione. Controlla la console del browser per informazioni sulle eccezioni non rilevate.

### Problemi di build e pubblicazione della libreria {#library-build-and-publishing-issues}

Sintomi:

* Le modifiche apportate in [!DNL Tags] non si riflettono sul sito live
* È stato applicato un aggiornamento dell’estensione, ma il comportamento precedente persiste

+++ Le modifiche non sono state aggiunte a una libreria

In [!UICONTROL Publishing Flow], confermare che le modifiche sono state aggiunte a una libreria nell&#39;ambiente di sviluppo. Vai a [!UICONTROL Libraries], apri la libreria di lavoro, seleziona **Aggiungi tutte le risorse modificate**, quindi seleziona **Salva e genera**.

+++

+++ Il browser sta memorizzando nella cache una libreria precedente

Eseguire un aggiornamento rapido (Ctrl+Maiusc+R o Comando+Maiusc+R) o aprire la pagina in una finestra in incognito/privata. Se il problema persiste, cancella completamente la cache del browser.

+++

+++ Il codice di incorporamento è per l’ambiente sbagliato

Conferma che il codice da incorporare nella pagina sia il codice da incorporare di produzione, se stai testando il comportamento di produzione.

+++

+++ Compilazione della libreria non riuscita in modo invisibile all&#39;utente

Vai a [!UICONTROL Publishing Flow] e controlla se la libreria mostra uno stato [!UICONTROL Build Failed]. Apri la libreria e controlla il registro di build; le cause più comuni sono configurazioni di regole non valide o conflitti di versioni dell’estensione.

+++

### Problemi di convalida dello schema per i campi Advertising {#schema-validation-for-advertising-fields}

Sintomi:

* La chiamata dell&#39;evento di invio `alloy()` ha esito positivo (con una risposta 200), ma i dati di conversione di Adobe Advertising non sono presenti nei rapporti
* Il payload XDM nel debugger non mostra alcun oggetto `_experience.adcloud`

#### Passaggio 1: confermare che il gruppo di campi [!UICONTROL Advertising] sia aggiunto allo schema

1. Vai a Adobe Experience Platform > [!UICONTROL Data Management] > [!UICONTROL Schemas].
1. Apri lo schema utilizzato dallo stream di dati.
1. Nel pannello [!UICONTROL Field Groups], verifica che sia elencata l&#39;**estensione completa Adobe Advertising Cloud ExperienceEvent**.
1. Se manca, seleziona **Aggiungi**, cerca **Adobe Advertising Cloud**, seleziona **Estensione completa Adobe Advertising Cloud ExperienceEvent**, quindi seleziona **Salva**.

>[!NOTE]
>La ripubblicazione della libreria [!DNL Tags] non è necessaria solo per le modifiche dello schema, ma se sono stati aggiunti nuovi campi è necessario mappare nuovamente l&#39;elemento dati XDM in [!DNL Tags].

#### Passaggio 2: verificare che i campi Adobe Advertising richiesti siano presenti nello schema in `_experience.adcloud.conversionDetails`

| Percorso campo | Tipo | Descrizione |
| ----- | --- | --- |
| `_experience.adcloud.conversionDetails.trackingCode` | Stringa | Mappa la conversione sull’annuncio di origine e fai clic su. Compilato dal parametro di query `s_kwcid` nell&#39;URL della pagina di destinazione. |
| `_experience.adcloud.conversionDetails.trackingIdentity` | Stringa | Memorizza l’identità univoca e altri dettagli per l’evento di conversione view-through o click-through tracciato. Compilato dal parametro di query `ef_id` nell&#39;URL della pagina di destinazione. |

Se manca uno dei due campi, verifica che il gruppo di campi **Estensione completa Adobe Advertising Cloud ExperienceEvent** sia stato salvato nello schema, quindi aggiorna l’editor schema.

#### Passaggio 3: verifica che l’URL della pagina di destinazione includa i parametri di query

In un click-through di un annuncio, l’URL della pagina di destinazione deve contenere entrambi i parametri di query, ad esempio:

`https://www.example.com/landing-page?s_kwcid=AL!12345!3!abc123&ef_id=abc123xyz:G:s`

| Parametro mancante | Probabile causa |
| ----- | --- |
| `s_kwcid` | L’assegnazione tag automatica non è abilitata nelle impostazioni della campagna Adobe Advertising Search o DSP. |
| `ef_id` | L’URL della pagina di destinazione non utilizza un reindirizzamento tracciato da Adobe Advertising oppure la aggiunta dell’ID EF non è abilitata nelle impostazioni della campagna. |

#### Passaggio 4: convalidare il payload XDM in uscita

Apri AEP Debugger o la scheda del browser [!UICONTROL Network], filtra `edge.adobedc.net` e controlla il corpo della richiesta di interazione. Un payload click-through valido ha un aspetto simile al seguente:

```json
{
  "events": [{
    "xdm": {
      "eventType": "advertising.clicks",
      "_experience": {
        "adcloud": {
          "conversionDetails": {
            "trackingCode": "AL!12345!3!abc123",
            "trackingIdentity": "abc123xyz:G:s"
          }
        }
      }
    }
  }]
}
```

Se `trackingCode` o `trackingIdentity` sono vuoti o mancanti:

* Il parametro di query non era presente nella pagina quando la regola è stata attivata. Controlla l’URL e la tempistica degli eventi della regola.
* Gruppo di campi mancante nello schema. Rivedi i passaggi dello schema indicati sopra.

## [!UICONTROL Advertising] problemi di configurazione dell&#39;estensione {#advertising-extension-setup-issues}

Sintomi:

* Non vengono registrate conversioni view-through o click-through per la pagina web.

  Per verificare se le conversioni sono registrate:

  1. Apri la pagina Web con `ef_id=test&s_kwcid=test` aggiunto all&#39;URL.
  1. Apri lo strumento di ispezione del codice del browser (spesso denominato [!DNL Inspect]), apri la scheda [!DNL Network] e cerca una chiamata interattiva per event_type=&quot;advertising.arricchment_ct&quot; da Adobe Experience Platform.
  1. Nell&#39;interfaccia di Data Collection, [aprire la definizione dello schema](https://experienceleague.adobe.com/it/docs/platform-learn/implement-web-sdk/initial-configuration/configure-schemas) per i dati del sito Web che si desidera raccogliere e confermare che `xdm->_experience->adcloud->conversionDetails->trackingCode` e `trackingIdentities` contengono `ef_id` e `s_kwcid`.

* Manca `_experience.adcloud` nel payload Experience Data Model (XDM) per i click-through.

* Le conversioni vengono confermate in uno strumento di debug ma non vengono visualizzate nei rapporti di Adobe Advertising

+++ Il servizio `Adobe Advertising` non è abilitato per lo stream di dati

1. In [!DNL Tags], apri le [impostazioni di configurazione dello stream di dati](https://experienceleague.adobe.com/it/docs/experience-platform/tags/extensions/client/web-sdk/configure/datastreams) per la proprietà tag.
1. Abilita i seguenti servizi e salva le impostazioni:
   * Adobe Advertising (per conversione/sincronizzazione pubblico)
   * Adobe Experience Platform (per l’acquisizione del profilo)

+++

+++ Il componente `Adobe Advertising` non è abilitato per l&#39;estensione [!UICONTROL WebSDK]

Il componente `Adobe Advertising` all&#39;interno dell&#39;estensione WebSDK è disabilitato per impostazione predefinita e deve essere abilitato in modo esplicito prima che qualsiasi tracciamento per i click-through o le view-through di Adobe Advertising funzioni, indipendentemente dalla configurazione dello schema o delle regole XDM.

1. In [!DNL Tags], apri le [opzioni di compilazione per la proprietà nelle impostazioni di configurazione di Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/it/docs/experience-platform/tags/extensions/client/web-sdk/configure/custom-build-components).
1. Abilita il componente **Advertising** e salva le impostazioni.
1. Rigenera e ripubblica la libreria.

+++

+++ Vengono registrate solo le conversioni click-through; le conversioni view-through non vengono mai visualizzate

Questo è il comportamento predefinito previsto. Una volta abilitato il componente `Adobe Advertising`, il tracciamento dei click-through viene attivato automaticamente utilizzando i parametri di query URL `s_kwcid` e `ef_id`. Il tracciamento view-through è disattivato per impostazione predefinita e richiede una configurazione aggiuntiva. Vedere l&#39;elemento successivo.

+++

+++ Il tracciamento view-through non è abilitato o configurato

1. Abilita il servizio Adobe Advertising per lo stream di dati:
   1. Vai a [!UICONTROL Data Collection] > [!UICONTROL Datastreams] in Adobe Experience Platform e apri lo stream di dati utilizzato dalla proprietà [!DNL Tags].
   1. Seleziona **Aggiungi servizio**, seleziona **Adobe Advertising** e **Adobe Experience Platform**, quindi seleziona **Salva**.
1. Configurare gli inserzionisti in Adobe Advertising DSP:
   1. In [!DNL Tags], vai a [!UICONTROL Extensions] > [!UICONTROL Installed] > **Adobe Experience Platform Web SDK** > [!UICONTROL Configure].
   1. Nella sezione [!UICONTROL Advertiser], seleziona un inserzionista dal menu a discesa e abilitalo. Per configurare più inserzionisti, selezionare **Aggiungi inserzionista**.
1. Verifica che i pixel di conversione view-through si attivino:
   1. Nel debugger di AEP, verifica che la chiamata di interazione includa `stitchId` nel campo `xdm.query`.
   1. Confermare nella scheda [!UICONTROL Network] del browser che un evento con tipo `advertising.enrichment` è stato attivato e include `stitchId` in `xdm.query`.

Le conversioni view-through vengono attivate solo ogni 30 minuti, indipendentemente dal numero di visite. Se non vedi una chiamata di interazione, cancella la cache del browser e riprova.

+++

+++ (Se non si verifica alcun evento view-through in Experience Platform dopo l’attivazione della chiamata di interazione Viewthrough) L’inserzionista è stato digitato manualmente invece di essere selezionato dal menu a discesa

Riselezionare l&#39;inserzionista dal menu a discesa [!UICONTROL Advertiser] invece di immetterlo manualmente.

+++

+++ (Se non si verificano eventi view-through in Experience Platform dopo l’attivazione della chiamata di interazione view-through) Non viene inviato alcun ID inserzionista con la chiamata di interazione view-through

Conferma che un inserzionista sia configurato e abilitato nella sezione [!UICONTROL Advertiser] della configurazione dell&#39;estensione WebSDK, quindi rigenera e ripubblica la libreria.

+++

Prima di aprire un ticket di supporto per [!UICONTROL Advertising] problemi di configurazione dell&#39;estensione, verifica quanto segue:

* I servizi **Adobe Advertising** e **Adobe Experience Platform** sono stati aggiunti allo stream di dati.
* Il componente **Adobe Advertising** è abilitato nella configurazione dell&#39;estensione WebSDK.
* La libreria è stata ricreata e ripubblicata dopo l’abilitazione del componente.
* Per il tracciamento dei click-through, l&#39;URL della pagina di destinazione contiene `s_kwcid` e `ef_id` al clic dell&#39;annuncio.
* Per il tracciamento view-through, in Adobe Advertising DSP viene configurato un inserzionista con l’ID inserzionista corretto.
* La versione dell&#39;estensione WebSDK è 2.36.0 o successiva.

## Segnalazione dei problemi

### Reporting di riepilogo

+++ Non sono disponibili dati di reporting di riepilogo in Customer Journey Analytics per Advertising DSP o Advertising Search, Social e Commerce.

Verifica quanto segue:

* Customer Journey Analytics Workspace fa riferimento alla visualizzazione dati corretta.

* Il feed da Adobe Advertising a Customer Journey Analytics è abilitato. Rivolgiti al team del tuo account Adobe.

* Il set di dati di dimensione/classificazione/ricerca di Adobe Advertising e il set di dati di riepilogo sono inclusi nella connessione Customer Journey Analytics.

* Le dimensioni di Adobe Advertising e le metriche di riepilogo sono incluse nella visualizzazione dati di Customer Journey Analytics.

Se verifichi tutte le impostazioni precedenti ma non trovi ancora i dati di riepilogo, apri un ticket di supporto per la tua organizzazione all&#39;indirizzo [https://experienceleague.adobe.com/home?lang=it#support](https://experienceleague.adobe.com/home?lang=it&support-tab=home#support).

+++

+++ I dati dei rapporti di riepilogo sono disponibili in Customer Journey Analytics per l’inserzionista 1 ma non per l’inserzionista 2.

Verifica quanto segue:

* Il feed da Adobe Advertising a Customer Journey Analytics è abilitato per l’inserzionista 2. Rivolgiti al team del tuo account Adobe.

* L&#39;impostazione &quot;[!UICONTROL Backfill all existing data]&quot; è abilitata per i tre set di dati (dimensione/classificazione/ricerca, riepilogo ed eventi) nella connessione Customer Journey Analytics.

Se verifichi tutte le condizioni di cui sopra ma non visualizzi ancora i dati di riepilogo, apri un ticket di supporto per la tua organizzazione all&#39;indirizzo [https://experienceleague.adobe.com/home?lang=it#support](https://experienceleague.adobe.com/home?lang=it&support-tab=home#support).

+++

+++ (Utenti Search, Social e Commerce) In Customer Journey Analytics sono disponibili dati di riepilogo per un account [!DNL Google Ads], [!DNL Meta Ads] o [!DNL Microsoft Advertising], ma non per un altro account.

Verifica che il feed da Adobe Advertising a Customer Journey Analytics sia abilitato per l’account di rete dell’annuncio specifico. Rivolgiti al team del tuo account Adobe.

Se il feed è abilitato per un account ma non vengono ancora visualizzati i dati di riepilogo, aprire un ticket di supporto per l&#39;organizzazione all&#39;indirizzo [https://experienceleague.adobe.com/home?lang=it#support](https://experienceleague.adobe.com/home?lang=it&support-tab=home#support). Includi [!UICONTROL Account ID] per l&#39;account di rete dell&#39;annuncio.

+++

+++ I dati dei rapporti di riepilogo in Customer Journey Analytics Workspace sono diversi da quelli presenti in Advertising DSP o Advertising Search, Social e Commerce, oppure mancano dati di riepilogo per alcune campagne ed entità campagna.

Verifica quanto segue:

* Stai utilizzando gli stessi intervalli di date sia in [!DNL Workspace] che nel rapporto di Adobe Advertising.

* Tutti i filtri e i segmenti applicati in [!DNL Workspace] e nel report Adobe Advertising non causano differenze nei dati.

* [!UICONTROL Time Zone] per la visualizzazione dati di Customer Journey Analytics corrisponde a [[!UICONTROL Default Timezone] per il tuo account Advertising DSP](/help/dsp/admin/user-own-profile-edit.md).

* L&#39;impostazione &quot;[!UICONTROL Backfill all existing data]&quot; è abilitata per i tre set di dati (dimensione/classificazione/ricerca, riepilogo ed eventi) nella connessione Customer Journey Analytics.

Se sei sicuro di una discrepanza di dati, apri un ticket di supporto per la tua organizzazione all&#39;indirizzo [https://experienceleague.adobe.com/home?lang=it#support](https://experienceleague.adobe.com/home?lang=it&support-tab=home#support). Includi [!UICONTROL Account ID] per l&#39;account di rete dell&#39;annuncio. Per mostrare le prove della discrepanza, includi schermate e fogli di calcolo. Se necessario, il team del tuo account Adobe può correggere retroattivamente il feed di dati per risolvere la discrepanza.

+++

### Reporting a livello di evento

+++ I dati di conversione (ad esempio `Page Views`) non sono disponibili per una dimensione di reporting (ad esempio `Campaign`) in CJA Customer Journey Analytics Workspace.

Verificare quanto segue, iniziando dagli elementi con il minor numero di barriere di verifica:

* Stai utilizzando la visualizzazione dati corretta.

* Le metriche di conversione applicabili sono eventi web/online, che Adobe Advertising può attribuire alle dimensioni.

* Adobe Advertising tiene traccia dei click-through e dei view-through sul sito applicabile. <!-- Link to validation instructions in the user guide -->

* Nella connessione Customer Journey Analytics per il set di dati delle classificazioni, i valori per le impostazioni [!DNL Key] e [!DNL Matching Key] sono corretti: [!DNL Key]: `Tracking Code` (_customername.adLens2.trackingCode), [!DNL Matching Key]: `Tracking Code` (event._experience.adcloud.conversionDetails.trackingCode)

* Il servizio [!DNL Adobe Advertising] è stato aggiunto allo stream di dati di Adobe Experience Platform, lo schema mappato per lo stream di dati è `XDM ExperienceEvent Schema` e il gruppo di campi `Adobe Advertising Cloud ExperienceEvent Full Extension` è stato aggiunto allo schema `XDM ExperienceEvent`.

* Le impostazioni di Adobe Advertising sono configurate correttamente nell’estensione WebSDK e pubblicate.

Se verifichi tutte le impostazioni di cui sopra ma non visualizzi ancora i dati di conversione, apri un ticket di supporto per la tua organizzazione all&#39;indirizzo [https://experienceleague.adobe.com/home?lang=it#support](https://experienceleague.adobe.com/home?lang=it&support-tab=home#support). Includi [!UICONTROL Account ID] per l&#39;account di rete dell&#39;annuncio.

+++

<!--

+++ Question

Answer

+++

+++ Question

Answer

+++

+++ Question

Answer

+++

-->

## Strumenti di convalida e debug

### Adobe Experience Platform Debugger

Installa l&#39;estensione [!DNL Adobe Experience Platform Debugger] per [!DNL Chrome]. Esso prevede:

* Visualizzazione in tempo reale di tutte le chiamate WebSDK `alloy()`
* Convalida dell’ID dello stream di dati e dell’ambiente
* Ispezione del payload XDM
* Dettagli delle richieste e delle risposte di Edge Network

Controlli chiave nel debugger:

| Linguetta | Cosa controllare |
| ----- | --- |
| [!UICONTROL Summary] | Conferma che WebSDK viene rilevato e mostra la versione installata. |
| [!UICONTROL AEP Web SDK] | Mostra ogni evento attivato, il payload XDM completo e la risposta Edge. |
| [!UICONTROL Adobe Advertising] | Conferma l’acquisizione di AMO ID e la chiamata di interazione XDM con il tipo di evento `advertising.enrichment`. |

### Scheda Rete del browser

Filtra per `edge.adobedc.net` per esaminare le richieste edge non elaborate:

* URL richiesta: `https://[org-id].data.adobedc.net/ee/v2/interact`
* Metodo: `POST`
* Stato: `200` (integro), `400` (payload non valido) o `500` (errore del server o dello stream di dati)

Controlla il payload della richiesta per:

* `dataStreamId` corretto
* Presenza di un oggetto `xdm` con i campi previsti
* `identityMap` con ECID popolato

### Convalida della console

Verifica la versione di Web SDK installata:

```js
window.alloy.version
```

Attiva manualmente un evento di test:

```js
alloy("sendEvent", {
  xdm: {
    eventType: "web.webpagedetails.pageViews",
    web: {
      webPageDetails: { name: "Test Page", URL: window.location.href }
    }
  }
}).then(result => console.log("Edge response:", result))
  .catch(err => console.error("Send event error:", err));
```

## Elenco di controllo per riferimenti rapidi

Verifica quanto segue prima di aprire un ticket di supporto:

* L&#39;estensione WebSDK è nella versione più recente.
* La libreria viene pubblicata e il codice di incorporamento è corretto per l’ambiente.
* L’ID dello stream di dati viene impostato correttamente per lo sviluppo, la gestione temporanea e la produzione.
* Tutti i servizi dello stream di dati richiesti sono abilitati.
* Il componente [!UICONTROL Advertising] è abilitato nella configurazione dell&#39;estensione WebSDK ed è configurato un ID inserzionista DSP.
* Lo schema XDM include il gruppo di campi [!UICONTROL Advertising].
* La regola [!UICONTROL Send Event] include una mappa di identità e viene attivata sull&#39;evento corretto.
* Nessuna impostazione CSP o della privacy del browser blocca le richieste edge.
* AEP Debugger conferma che gli eventi stanno raggiungendo il limite.
* Nessun errore JavaScript nella console del browser interrompe l’esecuzione.
* Il gruppo di campi **Estensione completa Adobe Advertising Cloud ExperienceEvent** è stato aggiunto allo schema.
* `_experience.adcloud.conversionDetails.trackingCode` è presente nello schema.
* `_experience.adcloud.conversionDetails.trackingIdentity` è presente nello schema.
* L&#39;URL della pagina di destinazione contiene sia `s_kwcid` che `ef_id` al click-through.
* AEP Debugger conferma che `conversionDetails` è popolato nel payload in uscita.

## Quando effettuare l’escalation

Inoltra al tuo Adobe Account Team o al tuo team di progettazione se:

* Le richieste di Edge restituiscono `500` errori persistenti dopo la convalida dello stream di dati.
* [!UICONTROL Advertising] conversioni sono confermate nel debugger ma non vengono visualizzate nei rapporti dopo 24-48 ore.
* Un aggiornamento della versione di WebSDK introduce una regressione che non era presente nella versione precedente. Includi i numeri di versione specifici nel ticket di supporto.

>[!MORELIKETHIS]
>
>* [Panoramica](overview.md)
>* [ID Adobe Advertising utilizzati da [!DNL Customer Journey Analytics]](ids.md)
>* [Prerequisiti](prerequisites.md)
>* [Imposta raccolta dati, trasferimento dati e reporting](set-up.md)
>* [Metriche e dimensioni di Adobe Advertising in Customer Journey Analytics](advertising-data-in-cja.md)
>* (Utenti Adobe Analytics) [Raccogli dati storici per gli AMO ID e gli EF ID da utilizzare in Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
