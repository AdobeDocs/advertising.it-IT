---
title: Risoluzione dei problemi dei dati di Adobe Advertising in Customer Journey Analytics
description: Scopri come risolvere i problemi relativi ai dati di Adobe Advertising in Customer Journey Analytics.
feature: Integration with Adobe Customer Journey Analytics
hide: true
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: c3ffa88d5df4fa2ff7e52813503c10b67d7c6eb7
workflow-type: tm+mt
source-wordcount: 3290
ht-degree: 0%

---

# Risoluzione dei problemi dei dati di Adobe Advertising in Customer Journey Analytics

Di seguito sono riportati i potenziali problemi, le loro possibili cause e le soluzioni.

## Elenco di tutti i potenziali problemi

| Problema | Ulteriori informazioni |
| ------- | ---------------- |
| Nessuna chiamata alloy() visibile nella scheda [!DNL Network] dello strumento di ispezione del codice del browser | Consulta la sezione &quot;[Problemi di installazione e configurazione](#issues-installation-setup)&quot; > &quot;[L&#39;estensione WebSDK non viene inizializzata](#websdk-extension-doesn't-initialize)&quot; |
| Errore della console: la lega non è definita | Vedi &quot;[Problemi di installazione e configurazione](#issues-installation-setup)&quot; > &quot;[L&#39;estensione WebSDK non viene inizializzata](#websdk-extension-doesn't-initialize)&quot; |
| Nessuna richiesta di interazione o raccolta a edge.adobedc.net | Vedi &quot;[Problemi di installazione e configurazione](#issues-installation-setup)&quot; > &quot;[L&#39;estensione WebSDK non viene inizializzata](#websdk-extension-doesn't-initialize)&quot; |
| Le richieste raggiungono Adobe Experience Platform Edge Network ma restituiscono errori 400 o 500 | Consulta la sezione &quot;[Problemi di installazione e configurazione](#issues-installation-setup)&quot; > &quot;[Datastream non configurato o non configurato correttamente](#datastream-not-configured-or-misconfigured)&quot; |
| Nei rapporti di Adobe Analytics o Adobe Advertising non viene visualizzato alcun dato | Consulta la sezione &quot;[Problemi di installazione e configurazione](#issues-installation-setup)&quot; > &quot;[Datastream non configurato o non configurato correttamente](#datastream-not-configured-or-misconfigured)&quot; |
| Errore nella risposta di rete: &quot;datastream non trovato&quot; | Consulta la sezione &quot;[Problemi di installazione e configurazione](#issues-installation-setup)&quot; > &quot;[Datastream non configurato o non configurato correttamente](#datastream-not-configured-or-misconfigured)&quot; |
| Non vengono registrate conversioni view-through o click-through per la pagina web | Consulta la sezione &quot;[Problemi di configurazione dell&#39;estensione Advertising](#advertising-extension-setup-issues)&quot; |
| Manca `_experience.adcloud` nel payload Experience Data Model (XDM) per i click-through | Consulta la sezione &quot;[Problemi di configurazione dell&#39;estensione Advertising](#advertising-extension-setup-issues)&quot; |
| Le conversioni vengono confermate in uno strumento di debug ma non vengono visualizzate nei rapporti di Adobe Advertising | Consulta la sezione &quot;[Problemi di configurazione dell&#39;estensione Advertising](#advertising-extension-setup-issues)&quot; |
| L&#39;ID visitatore cambia da pagina a pagina | Consulta la sezione &quot;[Problemi di identità ed ECID](#identity-and-ecid-issues)&quot; |
| I segmenti di pubblico di Advertising non corrispondono | Consulta la sezione &quot;[Problemi di identità ed ECID](#identity-and-ecid-issues)&quot; |
| Il debugger mostra che le condizioni della regola non sono soddisfatte | Vedi la sezione &quot;[Le regole o gli eventi non vengono attivati](#rules-or-events-don't-fire)&quot; |
| L&#39;azione [!UICONTROL Send Event] non viene mai eseguita | Vedi la sezione &quot;[Le regole o gli eventi non vengono attivati](#rules-or-events-don't-fire)&quot; |
| Le modifiche apportate in [!DNL Tags] non si riflettono sul sito live | Consulta la sezione &quot;[Problemi di compilazione e pubblicazione della libreria](#library-build-and-publishing-issues)&quot; |
| È stato applicato un aggiornamento dell’estensione, ma il comportamento precedente persiste | Consulta la sezione &quot;[Problemi di compilazione e pubblicazione della libreria](#library-build-and-publishing-issues)&quot; |
| La chiamata dell&#39;evento di invio `alloy()` ha esito positivo (con una risposta 200), ma i dati di conversione di Adobe Advertising non sono presenti nei rapporti | Consulta la sezione &quot;[Problemi di convalida dello schema per i campi Advertising](#schema-validation-for-advertising-fields)&quot; |
| Il payload XDM nel debugger non mostra alcun oggetto `_experience.adcloud` | Consulta la sezione &quot;[Problemi di convalida dello schema per i campi Advertising](#schema-validation-for-advertising-fields)&quot; |
| Non sono disponibili dati di reporting di riepilogo in Customer Journey Analytics per Advertising DSP o Advertising Search, Social e Commerce. | Consulta la sezione &quot;[Problemi di reporting](#reporting-issues)&quot; > &quot;[Report di riepilogo](#summary-reporting)&quot; |
| I dati dei rapporti di riepilogo sono disponibili in Customer Journey Analytics per l’inserzionista 1 ma non per l’inserzionista 2. | Consulta la sezione &quot;[Problemi di reporting](#reporting-issues)&quot; > &quot;[Report di riepilogo](#summary-reporting)&quot; |
| (Utenti Search, Social e Commerce) In Customer Journey Analytics sono disponibili dati di riepilogo per un account [!DNL Google Ads], [!DNL Meta Ads] o [!DNL Microsoft Advertising], ma non per un altro account. | Consulta la sezione &quot;[Problemi di reporting](#reporting-issues)&quot; > &quot;[Report di riepilogo](#summary-reporting)&quot; |
| I dati dei rapporti di riepilogo in Customer Journey Analytics Workspace sono diversi da quelli presenti in Advertising DSP o Advertising Search, Social e Commerce, oppure mancano dati di riepilogo per alcune campagne ed entità campagna. | Consulta la sezione &quot;[Problemi di reporting](#reporting-issues)&quot; > &quot;[Report di riepilogo](#summary-reporting)&quot; |
| I dati di conversione (ad esempio `Page Views`) non sono disponibili per una dimensione di reporting (ad esempio `Campaign`) in CJA Customer Journey Analytics Workspace. | Consulta la sezione &quot;[Problemi di reporting](#reporting-issues)&quot; > &quot;[Reporting a livello di evento](#event-level-reporting)&quot; |

## Problemi di installazione e configurazione {#issues-installation-setup}

### L’estensione WebSDK non inizializza {#websdk-extension-doesn-initialize}

#### Problemi:

* Nessuna chiamata alloy() visibile nella scheda [!DNL Network] dello strumento di ispezione del codice del browser
* Errore della console: la lega non è definita
* Nessuna richiesta di interazione o raccolta a edge.adobedc.net

#### Possibili cause e verifica/risoluzione

| Causa | Correzione |
| ----- | --- |
| Libreria non pubblicata o in stato di bozza | Vai a [Flusso di pubblicazione](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow) e assicurati che la libreria che contiene l&#39;estensione WebSDK sia nello stato approvato/pubblicato. |
| Codice di incorporamento mancante o ambiente errato | Verificare che il codice di incorporamento [!DNL Tags] nella pagina Web faccia riferimento all&#39;ambiente corretto (Dev/Stage/Prod). Cercare l&#39;ambiente nel tag `<head>` per il tag di script `//assets.adobedtm.com/...`. |
| Conflitto tra carico asincrono e carico sincrono | Verificare che sia presente un solo codice di incorporamento [!DNL Tags] per pagina Web. I codici di incorporamento duplicati causano race condition. |
| Blocco di Content Security Policy (CSP) | Aggiungi `edge.adobedc.net` `and assets.adobedtm.com` al tuo CSP `connect-src` e `script-src` direttive. |

### Stream di dati non configurato o non configurato correttamente {#datastream-not-configured-or-misconfigured}

#### Problemi:

* Le richieste raggiungono Adobe Experience Platform Edge Network ma restituiscono errori 400 o 500
* Nessun dato visualizzato nei report di Adobe Analytics o Adobe Advertising<!-- It's not useful to organize this info by cause, not symptom -->
* Errore nella risposta di rete: &quot;datastream non trovato&quot;

#### Possibili cause e verifica/risoluzione

| Causa | Correzione |
| ----- | --- |
| L’ID dello stream di dati per la proprietà tag è mancante o errato. | <ol><li>In [!DNL Tags], apri le [impostazioni di configurazione dello stream di dati](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/datastreams) per la proprietà tag.</li><li>Verificare che il campo [!UICONTROL Datastream] punti allo stream di dati corretto per ogni ambiente (sviluppo, staging e produzione), nonché allo schema e al set di dati corretti.<br><br>Ogni ambiente deve avere un proprio flusso di dati, a meno che tu non condivida esplicitamente un flusso di dati in tutti e tre gli ambienti.</li></ol> |
| I servizi stream di dati non sono abilitati per la proprietà tag. | [Aprire le impostazioni dello stream di dati](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure) e verificare che i servizi seguenti siano abilitati:<ul><li>Adobe Advertising (per conversione/sincronizzazione pubblico)</li><li>Adobe Experience Platform (per l’acquisizione del profilo)</li></ul> |
| Sandbox non corrispondente | Assicurati che lo stream di dati appartenga alla stessa sandbox di Adobe Experience Platform dello schema e del set di dati. Un errore comune è la creazione di un flusso di dati nella sandbox di produzione, ma il fatto di puntare gli schemi alla sandbox di sviluppo. |

### [!UICONTROL Advertising] problemi di configurazione dell&#39;estensione {#advertising-extension-setup-issues}

#### Problemi:

* Non vengono registrate conversioni view-through o click-through per la pagina web.

  Per verificare se le conversioni sono registrate:

  1. Apri la pagina Web con `ef_id=test&s_kwcid=test` aggiunto all&#39;URL.
  1. Apri lo strumento di ispezione del codice del browser (spesso denominato [!DNL Inspect]), apri la scheda [!DNL Network] e cerca una chiamata interattiva per event_type=&quot;advertising.arricchment_ct&quot; da Adobe Experience Platform.
  1. Nell&#39;interfaccia di Data Collection, [aprire la definizione dello schema](https://experienceleague.adobe.com/en/docs/platform-learn/implement-web-sdk/initial-configuration/configure-schemas) per i dati del sito Web che si desidera raccogliere e confermare che `xdm->_experience->adcloud->conversionDetails->trackingCode` e `trackingIdentities` contengono `ef_id` e `s_kwcid`.

* Manca `_experience.adcloud` nel payload Experience Data Model (XDM) per i click-through.

* Le conversioni vengono confermate in uno strumento di debug ma non vengono visualizzate nei rapporti di Adobe Advertising

#### Possibili cause e verifica/risoluzione

| Causa | Correzione |
| ----- | --- |
| Il servizio `Adobe Advertising` non è abilitato per lo stream di dati | <ol><li>In [!DNL Tags], apri le [impostazioni di configurazione dello stream di dati](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/datastreams) per la proprietà tag.</li><li>Abilita i seguenti servizi e salva le impostazioni:<ul><li>Adobe Advertising (per conversione/sincronizzazione pubblico)</li><li>Adobe Experience Platform (per l’acquisizione del profilo)</li></ul></ol> |
| Il componente `Adobe Advertising` non è abilitato per l&#39;estensione [!UICONTROL WebSDK] | Il componente `Adobe Advertising` all&#39;interno dell&#39;estensione WebSDK è disabilitato per impostazione predefinita e deve essere abilitato in modo esplicito prima che qualsiasi tracciamento per i click-through o le view-through di Adobe Advertising funzioni, indipendentemente dalla configurazione dello schema o delle regole XDM.<ol><li>In [!DNL Tags], apri le [opzioni di compilazione per la proprietà nelle impostazioni di configurazione di Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/custom-build-components).</li><li>Abilita il componente **Advertising** e salva le impostazioni.</li><li>Rigenera e ripubblica la libreria.</li></ol> |
| Vengono registrate solo le conversioni click-through; le conversioni view-through non vengono mai visualizzate | Questo è il comportamento predefinito previsto. Una volta abilitato il componente `Adobe Advertising`, il tracciamento dei click-through viene attivato automaticamente utilizzando i parametri di query URL `s_kwcid` e `ef_id`. Il tracciamento view-through è disattivato per impostazione predefinita e richiede una configurazione aggiuntiva. Vedere la riga successiva. |
| Il tracciamento view-through non è abilitato o configurato | <ol><li>Abilitare il servizio Adobe Advertising per lo stream di dati</li><ol><li>Vai a [!UICONTROL Data Collection] > [!UICONTROL Datastreams] in Adobe Experience Platform e apri lo stream di dati utilizzato dalla proprietà [!DNL Tags].</li><li>Seleziona **Aggiungi servizio**, seleziona **Adobe Advertising** e **Adobe Experience Platform**, quindi seleziona **Salva**.</li></ol><li>Configurare gli inserzionisti in Adobe Advertising DSP</li><ol><li>In [!DNL Tags], vai a [!UICONTROL Extensions] > [!UICONTROL Installed] > **Adobe Experience Platform Web SDK** > [!UICONTROL Configure].</li><li>Nella sezione [!UICONTROL Advertiser], seleziona un inserzionista dal menu a discesa e abilitalo. Per configurare più inserzionisti, selezionare **Aggiungi inserzionista**.</li></ol><li>Verifica che i pixel di conversione view-through siano attivati</li><ol><li>In Adobe Experience Platform Debugger, confermare che la chiamata di interazione includa `stitchId` nel campo `xdm.query`.</li><li>Nella scheda [!DNL Network] dello strumento di ispezione del codice del browser, verificare che un evento con tipo `advertising.enrichment` sia stato attivato e includa `stitchId` in `xdm.query`.</li></ol></ol> Le conversioni view-through vengono attivate solo ogni 30 minuti, indipendentemente dal numero di visite. Se non vedi una chiamata di interazione, cancella la cache del browser e riprova. |
| (Se non si verifica alcun evento view-through in Experience Platform dopo l’attivazione della chiamata di interazione Viewthrough) L’inserzionista è stato digitato manualmente invece di essere selezionato dal menu a discesa | Riselezionare l&#39;inserzionista dal menu a discesa [!UICONTROL Advertiser] invece di immetterlo manualmente. |
| (Se non si verificano eventi view-through in Experience Platform dopo l’attivazione della chiamata di interazione view-through) Non viene inviato alcun ID inserzionista con la chiamata di interazione view-through | Conferma che un inserzionista sia configurato e abilitato nella sezione [!UICONTROL Advertiser] della configurazione dell&#39;estensione WebSDK, quindi rigenera e ripubblica la libreria. |

Prima di aprire un ticket di supporto per [!UICONTROL Advertising] problemi di configurazione dell&#39;estensione, verifica quanto segue:

* I servizi **Adobe Advertising** e **Adobe Experience Platform** sono stati aggiunti allo stream di dati.
* Il componente **Adobe Advertising** è abilitato nella configurazione dell&#39;estensione WebSDK.
* La libreria è stata ricreata e ripubblicata dopo l’abilitazione del componente.
* Per il tracciamento dei click-through, l&#39;URL della pagina di destinazione contiene `s_kwcid` e `ef_id` al clic dell&#39;annuncio.
* Per il tracciamento view-through, in Adobe Advertising DSP viene configurato un inserzionista con l’ID inserzionista corretto.
* La versione dell&#39;estensione WebSDK è 2.36.0 o successiva.

### Problemi relativi a identità ed ECID {#identity-and-ecid-issues}

#### Problemi:

* L&#39;ID visitatore cambia da pagina a pagina
* I segmenti di pubblico di Advertising non corrispondono

#### Possibili cause e verifica/risoluzione

| Causa | Correzione |
| ----- | --- |
| I cookie di terze parti sono bloccati | Esegui la migrazione alla raccolta dati CNAME di prime parti configurando un dominio di prime parti nella configurazione Edge Network del flusso di dati. |
| `idMigrationEnabled` è impostato su `false` mentre è presente un cookie `s_ecid` legacy | Impostare `idMigrationEnabled: true` nella configurazione di base WebSDK per migrare l&#39;ECID esistente dai cookie `s_ecid` o `AMCV_`. |

### Le regole o gli eventi non attivano {#rules-or-events-don&#39;t-fire}

#### Problemi:

* Il debugger mostra che le condizioni della regola non sono soddisfatte
* L&#39;azione [!UICONTROL Send Event] non viene mai eseguita

#### Verifica e risoluzione

Verifica quanto segue:

* La regola viene salvata e inclusa nella build della libreria attiva.
* Il tipo di evento corrisponde al comportamento effettivo della pagina (ad esempio [!UICONTROL Library Loaded] rispetto a [!UICONTROL DOM Ready] rispetto a [!UICONTROL Window Loaded]).
* Le condizioni della regola non sono troppo restrittive. Esegui il test rimuovendo temporaneamente le condizioni per isolare il problema.
* Ordine delle regole corretto. Se più regole condividono lo stesso evento, controlla l’ordine delle regole.
* Nessun errore JavaScript precedente nella pagina sta interrompendo l’esecuzione. Controlla la console del browser per informazioni sulle eccezioni non rilevate.

### Problemi di build e pubblicazione della libreria {#library-build-and-publishing-issues}

#### Problemi:

* Le modifiche apportate in [!DNL Tags] non si riflettono sul sito live
* È stato applicato un aggiornamento dell’estensione, ma il comportamento precedente persiste

#### Possibili cause e verifica/risoluzione

| Causa | Correzione |
| ----- | --- |
| Le modifiche non sono state aggiunte a una libreria | In [!UICONTROL Publishing Flow], confermare che le modifiche sono state aggiunte a una libreria nell&#39;ambiente di sviluppo. Vai a [!UICONTROL Libraries], apri la libreria di lavoro, seleziona **Aggiungi tutte le risorse modificate**, quindi seleziona **Salva e genera**. |
| Il browser sta memorizzando nella cache una libreria precedente | Eseguire un aggiornamento rapido (Ctrl+Maiusc+R o Comando+Maiusc+R) o aprire la pagina in una finestra in incognito/privata. Se il problema persiste, cancella completamente la cache del browser. |
| Il codice di incorporamento è per l’ambiente sbagliato | Conferma che il codice da incorporare nella pagina sia il codice da incorporare di produzione, se stai testando il comportamento di produzione. |
| Compilazione della libreria non riuscita in modo invisibile all&#39;utente | Vai a [!UICONTROL Publishing Flow] e controlla se la libreria mostra uno stato [!UICONTROL Build Failed]. Apri la libreria e controlla il registro di build; le cause più comuni sono configurazioni di regole non valide o conflitti di versioni dell’estensione. |

### Problemi di convalida dello schema per i campi Advertising {#schema-validation-for-advertising-fields}

#### Problemi:

* La chiamata dell&#39;evento di invio `alloy()` ha esito positivo (con una risposta 200), ma i dati di conversione di Adobe Advertising non sono presenti nei rapporti
* Il payload XDM nel debugger non mostra alcun oggetto `_experience.adcloud`

#### Possibili cause e verifica/risoluzione

| Causa | Correzione |
| ----- | --- |
| Il gruppo di campi [!UICONTROL Advertising] non è presente nello schema | <ol><li>Vai a Adobe Experience Platform > [!UICONTROL Data Management] > [!UICONTROL Schemas].</li><li>Apri lo schema utilizzato dallo stream di dati.</li><li>Nel pannello [!UICONTROL Field Groups], verifica che sia elencata l&#39;**estensione completa Adobe Advertising Cloud ExperienceEvent**.</li><li>Se manca, seleziona **Aggiungi**, cerca **Adobe Advertising Cloud**, seleziona **Estensione completa Adobe Advertising Cloud ExperienceEvent**, quindi salva le impostazioni.</li></ol>La ripubblicazione della libreria [!DNL Tags] non è necessaria solo per le modifiche dello schema, ma se sono stati aggiunti nuovi campi è necessario mappare nuovamente l&#39;elemento dati XDM in [!DNL Tags]. |
| I campi Adobe Advertising richiesti non sono presenti nello schema | Verificare che i campi Adobe Advertising richiesti siano presenti nello schema in `_experience.adcloud.conversionDetails`. Vedi &quot;[Riferimento: campi schema obbligatori](#required-schema-fields)&quot;.<br><br>Se uno dei due campi non è presente, verifica che il gruppo di campi **Estensione completa Adobe Advertising Cloud ExperienceEvent** sia stato salvato nello schema, quindi aggiorna l&#39;editor schema. |
| L’URL della pagina di destinazione non include i parametri di query richiesti | Accertati che l’URL della pagina di destinazione includa i parametri di query necessari. In un click-through di un annuncio, l&#39;URL della pagina di destinazione deve contenere entrambi i parametri di query, ad esempio `https://www.example.com/landing-page?s_kwcid=AL!12345!3!abc123&ef_id=abc123xyz:G:s`. Vedere &quot;[Riferimento: parametri di query mancanti](#missing-query-parameters)&quot; per le cause probabili. |
| Alcuni parametri nel payload XDM sono mancanti o vuoti | Per convalidare il payload XDM in uscita, apri la scheda Adobe Experience Platform Debugger o [!DNL Network] dello strumento di ispezione del codice del browser, filtra per `edge.adobedc.net` e controlla il corpo della richiesta di interazione (vedi il payload di esempio riportato di seguito).<br><br>Se `trackingCode` o `trackingIdentity` sono vuoti o mancanti: il parametro di query non era presente nella pagina quando la regola è stata attivata (controlla l&#39;URL e la tempistica degli eventi della regola) oppure il gruppo di campi non è presente nello schema (visita di nuovo la prima riga). |

##### Riferimento: campi schema obbligatori {#required-schema-fields}

| Percorso campo | Tipo | Descrizione |
| ----- | --- | --- |
| `_experience.adcloud.conversionDetails.trackingCode` | Stringa | Mappa la conversione sull’annuncio di origine e fai clic su. Compilato dal parametro di query `s_kwcid` nell&#39;URL della pagina di destinazione. |
| `_experience.adcloud.conversionDetails.trackingIdentity` | Stringa | Memorizza l’identità univoca e altri dettagli per l’evento di conversione view-through o click-through tracciato. Compilato dal parametro di query `ef_id` nell&#39;URL della pagina di destinazione. |

##### Riferimento: parametri di query mancanti {#missing-query-parameters}

| Parametro mancante | Probabile causa |
| ----- | --- |
| `s_kwcid` | L’assegnazione tag automatica non è abilitata nelle impostazioni della campagna Adobe Advertising Search o DSP. |
| `ef_id` | L’URL della pagina di destinazione non utilizza un reindirizzamento tracciato da Adobe Advertising oppure la aggiunta dell’ID EF non è abilitata nelle impostazioni della campagna. |

**Esempio di payload click-through**

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

## Segnalazione dei problemi in Customer Journey Analytics Workspace

### Reporting di riepilogo

| Problema | Verifica e risoluzione |
| ----- | --- |
| Non sono disponibili dati di reporting di riepilogo in Customer Journey Analytics per Advertising DSP o Advertising Search, Social e Commerce. | <ol><li>Verifica che Customer Journey Analytics Workspace faccia riferimento alla visualizzazione dati corretta.</li><li>Verifica che il feed da Adobe Advertising a Customer Journey Analytics sia abilitato. Rivolgiti al team del tuo account Adobe.</li><li>Conferma che il set di dati di dimensione/classificazione/ricerca di Adobe Advertising e il set di dati di riepilogo siano inclusi nella connessione Customer Journey Analytics.</li><li>Conferma che le dimensioni di Adobe Advertising e le metriche di riepilogo siano incluse nella visualizzazione dati di Customer Journey Analytics.</li></ol>Se verifichi tutte le impostazioni precedenti ma non visualizzi ancora i dati di riepilogo, apri un [ticket di supporto](https://experienceleague.adobe.com/home?support-tab=home#support) per la tua organizzazione. |
| I dati dei rapporti di riepilogo sono disponibili in Customer Journey Analytics per l’inserzionista 1 ma non per l’inserzionista 2. | <ol><li>Conferma che il feed da Adobe Advertising a Customer Journey Analytics sia abilitato per l’inserzionista 2. Rivolgiti al team del tuo account Adobe.</li><li>Conferma che l&#39;impostazione &quot;[!UICONTROL Backfill all existing data]&quot; è abilitata per i tre set di dati (dimensione/classificazione/ricerca, riepilogo ed eventi) nella connessione Customer Journey Analytics.</li></ol>Se verifichi tutte le condizioni di cui sopra ma non visualizzi ancora i dati di riepilogo, apri un [ticket di supporto](https://experienceleague.adobe.com/home?support-tab=home#support) per la tua organizzazione. |
| (Utenti Search, Social e Commerce) In Customer Journey Analytics sono disponibili dati di riepilogo per un account [!DNL Google Ads], [!DNL Meta Ads] o [!DNL Microsoft Advertising], ma non per un altro account. | Verifica che il feed da Adobe Advertising a Customer Journey Analytics sia abilitato per l’account di rete dell’annuncio specifico. Verifica con il tuo account team Adobe.<br><br>Se il feed è abilitato per un account ma non vengono ancora visualizzati i dati di riepilogo, apri un [ticket di supporto](https://experienceleague.adobe.com/home?support-tab=home#support) per la tua organizzazione. Includi [!UICONTROL Account ID] per l&#39;account di rete dell&#39;annuncio. |
| I dati dei rapporti di riepilogo in Customer Journey Analytics Workspace sono diversi da quelli presenti in Advertising DSP o Advertising Search, Social e Commerce, oppure mancano dati di riepilogo per alcune campagne ed entità campagna. | <ol><li>Conferma di utilizzare gli stessi intervalli di date sia in [!DNL Workspace] che nel rapporto di Adobe Advertising.</li><li>Verificare che i filtri e i segmenti applicati in [!DNL Workspace] e nel report Adobe Advertising non causino differenze nei dati.</li><li>Conferma che [!UICONTROL Time Zone] per la visualizzazione dati di Customer Journey Analytics corrisponda a [!UICONTROL Default Timezone] per il tuo account [Advertising DSP](/help/dsp/admin/user-own-profile-edit.md).</li><li>Conferma che l&#39;impostazione &quot;[!UICONTROL Backfill all existing data]&quot; è abilitata per i tre set di dati (dimensione/classificazione/ricerca, riepilogo ed eventi) nella connessione Customer Journey Analytics.</li></ol>Se sei sicuro di una discrepanza di dati, apri un [ticket di supporto](https://experienceleague.adobe.com/home?support-tab=home#support) per la tua organizzazione. Includi [!UICONTROL Account ID] per l&#39;account di rete dell&#39;annuncio. Per mostrare le prove della discrepanza, includi schermate e fogli di calcolo. Se necessario, il team del tuo account Adobe può correggere retroattivamente il feed di dati per risolvere la discrepanza. |

### Reporting a livello di evento

| Problema | Verifica e risoluzione |
| ----- | --- |
| I dati di conversione (come `Page Views`) non sono disponibili per una dimensione di reporting (come `Campaign`) in Customer Journey Analytics Workspace. | Verificare quanto segue, iniziando dagli elementi con il minor numero di barriere di verifica:<ul><li>Verifica di utilizzare la visualizzazione dati corretta.</li><li>Conferma che le metriche di conversione applicabili siano eventi web/online, che Adobe Advertising può attribuire alle dimensioni.</li><li>Conferma che Adobe Advertising stia tenendo traccia dei click-through e delle view-through sul sito applicabile.</li><li>Nella connessione Customer Journey Analytics per il set di dati delle classificazioni, verificare che i valori per le impostazioni [!DNL Key] e [!DNL Matching Key] siano corretti: [!DNL Key]: `Tracking Code` (_customername.adLens2.trackingCode), [!DNL Matching Key]: `Tracking Code` (event._experience.adcloud.conversionDetails.trackingCode).</li><li>Verificare che il servizio [!DNL Adobe Advertising] sia aggiunto allo stream di dati di Adobe Experience Platform, che lo schema mappato per lo stream di dati sia `XDM ExperienceEvent Schema` e che il gruppo di campi `Adobe Advertising Cloud ExperienceEvent Full Extension` sia aggiunto allo schema `XDM ExperienceEvent`.</li><li>Verifica che le impostazioni di Adobe Advertising siano configurate correttamente nell&#39;estensione WebSDK e pubblicate.</li></ul>Se verifichi tutte le impostazioni precedenti ma non visualizzi ancora i dati di conversione, apri un [ticket di supporto](https://experienceleague.adobe.com/home?support-tab=home#support) per la tua organizzazione. Includi [!UICONTROL Account ID] per l&#39;account di rete dell&#39;annuncio. |

## Utili strumenti di convalida e debug

### Adobe Experience Platform Debugger

Installa l&#39;estensione [!DNL Adobe Experience Platform Debugger] per [!DNL Chrome] per:

* Visualizzazione in tempo reale di tutte le chiamate WebSDK `alloy()`
* Convalida dell’ID dello stream di dati e dell’ambiente
* Ispezione del payload XDM
* Dettagli delle richieste e delle risposte di Edge Network

Controlli chiave nel debugger:

| Linguetta | Cosa controllare |
| ----- | --- |
| [!UICONTROL Summary] | Conferma che WebSDK viene rilevato e mostra la versione installata. |
| [!UICONTROL Adobe Experience Platform WebSDK] | Mostra ogni evento attivato, il payload XDM completo e la risposta di Edge Network. |
| [!UICONTROL Adobe Advertising] | Conferma l’acquisizione di AMO ID e la chiamata di interazione XDM con il tipo di evento `advertising.enrichment`. |

### Scheda [!DNL Network] dello strumento di ispezione del codice del browser

Utilizza la scheda [!DNL Network] dello strumento di ispezione del codice del browser (spesso denominato &quot;[!DNL Inspect]&quot;) per effettuare le seguenti operazioni:

Filtra per `edge.adobedc.net` per esaminare le richieste Edge Network non elaborate:

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

## Elenco di controllo per riferimenti rapidi prima di richiedere assistenza

Verifica quanto segue prima di aprire un ticket di supporto:

* L&#39;estensione WebSDK è nella versione più recente.
* La libreria viene pubblicata e il codice di incorporamento è corretto per l’ambiente.
* L’ID dello stream di dati viene impostato correttamente per lo sviluppo, la gestione temporanea e la produzione.
* Tutti i servizi dello stream di dati richiesti sono abilitati.
* Il componente [!UICONTROL Advertising] è abilitato nella configurazione dell&#39;estensione WebSDK ed è configurato un ID inserzionista DSP.
* Lo schema XDM include il gruppo di campi [!UICONTROL Advertising].
* La regola [!UICONTROL Send Event] include una mappa di identità e viene attivata sull&#39;evento corretto.
* Nessuna impostazione di privacy CSP o browser blocca le richieste Edge Network.
* L’Adobe Experience Platform Debugger conferma che gli eventi stanno raggiungendo Edge Network.
* Nessun errore JavaScript nella console del browser interrompe l’esecuzione.
* Il gruppo di campi `Adobe Advertising Cloud ExperienceEvent Full Extension` è stato aggiunto allo schema.
* `_experience.adcloud.conversionDetails.trackingCode` è presente nello schema.
* `_experience.adcloud.conversionDetails.trackingIdentity` è presente nello schema.
* L&#39;URL della pagina di destinazione contiene sia `s_kwcid` che `ef_id` parametri al click-through.
* Adobe Experience Platform Debugger conferma che `conversionDetails` è popolato nel payload in uscita.

## Quando segnalare un problema

Contatta il team dell’account Adobe o il team di progettazione se:

* Le richieste di Edge Network restituiscono `500` errori persistenti dopo la convalida dello stream di dati.
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
