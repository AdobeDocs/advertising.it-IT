---
title: Codici di errore per [!DNL FreeWheel] Invii annunci
description: Fai riferimento ai codici di errore restituiti per l’invio di annunci a [!DNL FreeWheel].
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 2eb93971-ba82-4de8-96c5-48524d628b70
source-git-commit: 1c13874967ec4ad264e5fa6a5e0dfeb6120f53cc
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 2%

---

# Codici di errore per [!DNL FreeWheel] Invii annunci

I messaggi di errore per gli annunci inviati non riusciti possono provenire da Advertising DSP o da [!DNL FreeWheel]. I messaggi di errore vengono visualizzati nella [!UICONTROL API Response] nella colonna [[!UICONTROL Freewheel Status] dialogo](freewheel-check-status.md).

## Pubblicità DSP errori interni

| Messaggio di errore | Descrizione | Passaggi successivi |
|--- |--- |--- |
| [!DNL Awaiting status response from [!DNL FreeWheel]] | [!DNL FreeWheel] non ha ancora risposto che l&#39;invio è stato eseguito correttamente o non è riuscito. | Controlla di nuovo lo stato in 10 minuti. |
| [!DNL The submitted ad does not have a clock number assigned.] | [!DNL FreeWheel] non accetta gli annunci britannici senza i numeri di orologio assegnati. | Assegna un numero di orologio all’annuncio, quindi invia nuovamente l’annuncio. |
| [!DNL The ad you are attempting to submit has not yet finished transcoding. Please wait ten minutes then try again.] | Il transcoder non aveva completato la transcodifica dell’annuncio quando si tentava di inviarlo. | Attendi dieci minuti, quindi invia nuovamente l’annuncio. |
| [!DNL The deal id you input is not setup as a guaranteed feed. Please submit guaranteed deals only.] | L&#39;accordo presentato non è impostato come accordo programmatico garantito. [!DNL FreeWheel] accetta solo offerte garantite. | Imposta l&#39;ID offerta come offerta programmatica garantita. L’annuncio viene inviato automaticamente a [!DNL FreeWheel] quando salvi il posizionamento predefinito programmatico garantito al termine del flusso di lavoro ID offerta. |
| [!DNL Invalid external_deal_id:] \&lt;deal_id> | L&#39;ID offerta inviato non esiste o non è attivo al termine dell&#39;Adobe. | Assicurati che l&#39;offerta sia attiva, quindi invia nuovamente l&#39;annuncio. |
| [!DNL \[public_id=]\&lt;deal>] non esiste | L&#39;ID offerta inviato non esiste nel [!DNL FreeWheel] fine. | Contatta il tuo [!DNL FreeWheel] per confermare l&#39;ID dell&#39;offerta. |
| [!DNL Ad with identifier] \&lt;*nome annuncio*\> [!DNL was not found.] | La chiave dell&#39;annuncio inviata non esiste o non è attiva al termine dell&#39;Adobe. | Trova il codice pubblicitario corretto e quindi invia nuovamente l’annuncio. |
| [!DNL Pending Submission] | La presentazione è ancora in sospeso. | Aggiorna la pagina. |

{style=&quot;table-layout:auto&quot;}

## [!DNL Freewheel] Errori API

| Codice | Significato | Descrizione | Passaggi successivi |
|--- |--- |--- |--- |
| 401 | Non autorizzato | Credenziali di accesso errate, mancanti o non valide. | Contatta il tuo [!DNL Adobe] team di account. |
| 403 | Proibito | Il server ha capito la richiesta ma rifiuta di autorizzarla. | Contatta il tuo [!DNL Adobe] team di account. |
| 404 | Non trovato | La risorsa richiesta non è disponibile. Se l’ID creativo non viene trovato nell’operazione PUT, viene restituito un 404. | Contatta il tuo [!DNL Adobe] team di account. |
| 405 | Metodo non consentito | È stata effettuata una richiesta di una risorsa utilizzando un metodo di richiesta non supportato da tale risorsa (ad esempio, utilizzando GET su un metodo che richiede l’invio di dati da parte di POST o utilizzando PUT su una risorsa di sola lettura). | Contatta il tuo [!DNL Adobe] team di account. |
| 408 | Timeout richiesta | Timeout durante l&#39;elaborazione della richiesta. I timeout di solito sono causati da richieste simultanee di accesso esclusivo a determinate risorse. | Invia nuovamente la richiesta quando ricevi questo stato. Se il problema persiste, contatta il tuo [!DNL Adobe] team di account. |
| 422 | Entità non processabile | Risorsa non valida. Questo errore si verifica quando il corpo della richiesta non è valido o la risorsa creata/aggiornata non è valida (ad esempio, se l’ID offerta non è stato trovato). Vedi [Errori API 422 FreeWheel](#freewheel-422-errors) per ulteriori informazioni. | Contatta il tuo [!DNL Adobe] team di account. |
| 500 | Errore interno del server | Errore di sistema API. | Contatta il tuo [!DNL Adobe] team di account. |

{style=&quot;table-layout:auto&quot;}

## [!DNL Freewheel] Errori API 422 {#freewheel-422-errors}

| Codice | Codice HTTP | Descrizione |
|--- |--- |--- |
| DATA_UNMARHER_FAILURE | 422 | Il formato json della richiesta non è valido. Per ulteriori informazioni, guarda il messaggio di errore. |
| DATA_VALIDATION_FAILURE | 422 | I dati della richiesta non contengono campi obbligatori o presentano un tipo di dati non valido. Per ulteriori informazioni, guarda il messaggio di errore. |
| DATA_DEAL_INVALID | 422 | L&#39;offerta è configurata in modo errato o non esiste. Per ulteriori informazioni, guarda il messaggio di errore. |
| DATA_DEAL_GET_FAILURE | 422 | L&#39;accordo non è stato trovato o la sua configurazione ha un problema. Per ulteriori informazioni, guarda il messaggio di errore. |
| DATA_CREATIVE_INGEST_FAILURE | 422 | L&#39;URL creativo non è valido. Per ulteriori informazioni, guarda il messaggio di errore. |
| DATA_CREATIVE_LINK_FAILURE | 422 | Il contenuto creativo non era collegato ai nodi dell&#39;unità dell&#39;offerta. Per ulteriori informazioni, guarda il messaggio di errore. |
| DATA_CREATIVE_UPDATE_FAILURE | 422 | Il creativo non è stato aggiornato. Per ulteriori informazioni, guarda il messaggio di errore. |
| DATA_DSP_GET_FAILURE | 422 | Il DSP non esiste all&#39;interno del sistema. |
| DATA_CREATIVE_UNLINK_FAILURE | 422 | Il creativo non era scollegato dalle unità pubblicitarie. |
| DATA_CREATIVE_DELETE_FAILURE | 422 | Il creativo non è stato cancellato. |
| DATA_CREATIVE_DETECTION_FAILURE | 422 | L&#39;URL non è stato rilevato. |
| DATA_ENTITY_NOT_FOUND | 422 | Il creativo non esiste. |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [Panoramica sull&#39;impostazione di offerte garantite programmatiche in [!DNL Freewheel]](/help/dsp/inventory/freewheel-overview.md)
>* [Accettare un accordo nella casella in entrata dell’ID offerta](deal-id-inbox-accept.md)
>* [Invia un annuncio per un&#39;offerta garantita a livello di programmazione a [!DNL Freewheel]](/help/dsp/inventory/freewheel-submit.md)
>* [Controlla lo stato degli annunci per [!DNL FreeWheel] Offerte garantite programmatiche](/help/dsp/inventory/freewheel-check-status.md)

