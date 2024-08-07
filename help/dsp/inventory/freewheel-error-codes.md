---
title: Codici di errore per  [!DNL FreeWheel] invii di annunci
description: Fai riferimento ai codici di errore restituiti per l'invio di annunci a  [!DNL FreeWheel].
feature: DSP Private Inventory, DSP Deal IDs
exl-id: e48937c2-ced9-4107-9e1d-65a3bac51fff
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 3%

---

# Codici di errore per [!DNL FreeWheel] invii di annunci

I messaggi di errore per gli invii di annunci non riusciti possono provenire da Advertising DSP o da [!DNL FreeWheel]. I messaggi di errore vengono visualizzati nella colonna [!UICONTROL API Response] della finestra di dialogo [[!UICONTROL Freewheel Status]](freewheel-check-status.md).

## Errori interni di Advertising DSP

| Messaggio di errore | Descrizione | Passaggi successivi |
|--- |--- |--- |
| [!DNL Awaiting status response from [!DNL FreeWheel]] | [!DNL FreeWheel] non ha ancora risposto che l&#39;invio è riuscito o non è riuscito. | Controlla di nuovo lo stato tra 10 minuti. |
| [!DNL The submitted ad does not have a clock number assigned.] | [!DNL FreeWheel] non accetta annunci nel Regno Unito senza numeri di orologio assegnati. | Assegna un numero di orologio all’annuncio, quindi invia nuovamente l’annuncio. |
| [!DNL The ad you are attempting to submit has not yet finished transcoding. Please wait ten minutes then try again.] | Il transcodificatore non ha terminato la trascodifica dell’annuncio quando hai tentato di inviarlo. | Attendi dieci minuti, quindi invia nuovamente l’annuncio. |
| [!DNL The deal id you input is not setup as a guaranteed feed. Please submit guaranteed deals only.] | L&#39;offerta presentata non è impostata come offerta programmatica garantita. [!DNL FreeWheel] accetta solo offerte garantite. | Imposta l’ID offerta come offerta programmatica garantita. L&#39;annuncio viene inviato automaticamente a [!DNL FreeWheel] quando si salva il posizionamento predefinito programmatico garantito al termine del flusso di lavoro ID offerta. |
| [!DNL Invalid external_deal_id:] \&lt;deal_id\> | L’ID offerta inviato non esiste o non è attivo alla fine dell’Adobe. | Assicurati che l’offerta sia attiva, quindi invia nuovamente l’annuncio. |
| [!DNL \[public_id=]\&lt;offerta\>] non esiste | L&#39;ID offerta inviato non esiste alla fine di [!DNL FreeWheel]. | Contatta il tuo rappresentante [!DNL FreeWheel] per confermare l&#39;ID offerta. |
| [!DNL Ad with identifier] \&lt;*nome annuncio*\> [!DNL was not found.] | La chiave dell’annuncio inviata non esiste o non è attiva alla fine dell’Adobe. | Trova la chiave dell’annuncio corretta, quindi invia nuovamente l’annuncio. |
| [!DNL Pending Submission] | L&#39;invio è ancora in sospeso. | Aggiorna la pagina. |

{style="table-layout:auto"}

## [!DNL Freewheel] errori API

| Codice | Significato | Descrizione | Passaggi successivi |
|--- |--- |--- |--- |
| 401 | Non autorizzato | Credenziali di accesso errate, mancanti o non valide. | Contatta il team del tuo account Adobe. |
| 403 | Non consentito | Il server ha compreso la richiesta ma rifiuta di autorizzarla. | Contatta il team del tuo account Adobe. |
| 404 | Non trovato | La risorsa richiesta non è disponibile. Se l’ID creativo non viene trovato nell’operazione PUT, viene restituito un 404. | Contatta il team del tuo account Adobe. |
| 405 | Metodo non consentito | È stata effettuata una richiesta di una risorsa utilizzando un metodo di richiesta non supportato da tale risorsa (ad esempio, utilizzando GET su un metodo che richiede l’invio di dati da parte di POST o utilizzando PUT su una risorsa di sola lettura). | Contatta il team del tuo account Adobe. |
| 408 | Timeout richiesta | Timeout durante l&#39;elaborazione della richiesta. I timeout sono in genere causati da richieste simultanee di accesso esclusivo a determinate risorse. | Invia nuovamente la richiesta quando ricevi questo stato. Se il problema persiste, contatta il team del tuo account Adobe. |
| 422 | Entità non elaborabile | Risorsa non valida. Questo errore si verifica quando il corpo della richiesta non è valido o la risorsa creata/aggiornata non è valida (ad esempio, se l’ID offerta non è stato trovato). Per ulteriori informazioni, vedere [Errori API FreeWheel 422](#freewheel-422-errors). | Contatta il team del tuo account Adobe. |
| 500 | Errore interno del server | Errore di sistema API. | Contatta il team del tuo account Adobe. |

{style="table-layout:auto"}

## [!DNL Freewheel] errori API 422 {#freewheel-422-errors}

| Codice | Codice HTTP | Descrizione |
|--- |--- |--- |
| DATA_UNMARSHALL_FAILURE | 422 | I dati della richiesta sono in formato JSON non valido. Per informazioni dettagliate, consulta il messaggio di errore. |
| DATA_VALIDATION_FAILURE | 422 | I dati della richiesta non contengono campi obbligatori o hanno un tipo di dati non valido. Per informazioni dettagliate, consulta il messaggio di errore. |
| DATA_DEAL_INVALID | 422 | L’offerta non è configurata correttamente o non esiste. Per informazioni dettagliate, consulta il messaggio di errore. |
| DATA_DEAL_GET_FAILURE | 422 | L&#39;offerta non è stata trovata o la sua configurazione presenta un problema. Per informazioni dettagliate, consulta il messaggio di errore. |
| DATA_CREATIVE_INGEST_FAILURE | 422 | L’URL della creatività non è valido. Per informazioni dettagliate, consulta il messaggio di errore. |
| DATA_CREATIVE_LINK_FAILURE | 422 | Il contenuto creativo non era collegato ai nodi dell’unità pubblicitaria dell’offerta. Per informazioni dettagliate, consulta il messaggio di errore. |
| DATA_CREATIVE_UPDATE_FAILURE | 422 | La creatività non è stata aggiornata. Per informazioni dettagliate, consulta il messaggio di errore. |
| DATA_DSP_GET_FAILURE | 422 | L&#39;DSP non esiste nel sistema. |
| DATA_CREATIVE_UNLINK_FAILURE | 422 | La creatività non è stata scollegata dalle unità pubblicitarie. |
| DATA_CREATIVE_DELETE_FAILURE | 422 | Il contenuto creativo non è stato eliminato. |
| DATA_CREATIVE_DETECTION_FAILURE | 422 | L&#39;URL non è stato rilevato. |
| DATA_ENTITY_NOT_FOUND | 422 | Il creativo non esiste. |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [Panoramica sulla configurazione di offerte garantite a livello di programmazione in [!DNL Freewheel]](/help/dsp/inventory/freewheel-overview.md)
>* [Accetta un&#39;offerta nella casella in entrata dell&#39;ID offerta](deal-id-inbox-accept.md)
>* [Invia un annuncio per un&#39;offerta programmatica garantita a [!DNL Freewheel]](/help/dsp/inventory/freewheel-submit.md)
>* [Verifica lo stato degli annunci per [!DNL FreeWheel] Offerte garantite a livello di programmazione](/help/dsp/inventory/freewheel-check-status.md)
