---
title: Errori di bulksheet
description: Fai riferimento ai potenziali motivi di ogni errore di bulksheet.
exl-id: dc3559b0-05c0-4896-b9e9-67084f56ab80
feature: Search Bulksheets
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '1137'
ht-degree: 0%

---

# Errori di bulksheet

Search, Social e Commerce genera due tipi di file di errore durante le operazioni dei bulksheet:

* **Errori SE:** Quando un file viene pubblicato ma la rete di annunci non accetta tutti i dati, viene creato un file di errore denominato `<uploaded file name>_se_errors.<extension used for the bulksheet>`. Quando sono state accettate alcune righe ma non tutte, il file di errore mostra le righe non pubblicate e una spiegazione di ogni errore in modo da poterlo correggere. Gli errori sono inclusi nella colonna &quot;[!UICONTROL SE Error Message]&quot;.

>[!NOTE]
>
>Se si pubblicano [!DNL Google Ads] annunci che violano le politiche pubblicitarie della rete di annunci ma possono essere ammessi alle esenzioni, tali annunci vengono automaticamente ripubblicati con le richieste di esenzione. Se la richiesta di esenzione ha esito negativo, le informazioni sulla violazione vengono incluse nel file di errore.

* **Errori EF:** Quando l&#39;operazione di bulksheet non è in grado di caricare o elaborare un file o singole righe nel file, viene creato un file di errore denominato `<uploaded file name>_ef_errors.<extension used for the bulksheet>`. Se il problema riguarda singole righe, queste righe vengono incluse,
con una spiegazione di ogni errore in modo da poterlo correggere. Gli errori sono inclusi nella colonna &quot;[!UICONTROL EF Error Message]&quot;.

## [!UICONTROL SE Error] messaggi

Gli errori nella colonna [!UICONTROL SE Error] provengono direttamente dalla rete di annunci.

## [!UICONTROL EF Error] messaggi

I seguenti errori possono essere inclusi nella colonna [!UICONTROL EF Error] nei file [!UICONTROL EF Errors].

### Errori di download/creazione

| Categoria | Messaggio | Descrizione |
|----|----|----|
| Generale | [!UICONTROL Internal Error: Please Try Creating the bulksheet Again. If Problem Persists Contact Technical Support] | Operazione non riuscita a causa di un errore non categorizzato o non gestito. Se il problema persiste, contatta il team dell’account Adobe per indagare sulla causa. |
| | [!UICONTROL Pre-Sync Failed. Please Try Creating the bulksheet Again. If Problem Persists Contact Technical Support] | Non è stato possibile sincronizzare Ricerca, Social e Commerce con la rete di annunci prima di creare il bulksheet, quindi non è stato creato alcun bulksheet. Se il problema persiste, contatta il team del tuo account Adobe. |

### Errori di caricamento

| Categoria | Messaggio | Descrizione |
|----|----|----|
| Generale | [!UICONTROL Internal Error: Please Try Uploading the bulksheet Again. If Problem Persists Contact Customer Care] | Operazione non riuscita. Se il problema persiste, contatta il team del tuo account Adobe. |
| Tutte le entità | [!UICONTROL Invalid Fields.] \[campi non validi ed errore\] | Dati specificati mancanti o non validi. |
|  | [!UICONTROL Invalid Reference Given] | L’ID dell’entità sulla rete di annunci o l’ID di un’entità principale (ad esempio l’ID account) non corrisponde a un’entità in Search, Social e Commerce. Ciò può verificarsi quando hai modificato l’ID nel bulksheet. |
|  | [!UICONTROL &lt;Entity> is deleted or expired] | L’entità è scaduta o è stata eliminata e non è possibile modificarne le proprietà. L’entità può essere eliminata quando qualcuno modifica manualmente lo stato. |
|  | [!UICONTROL &lt;Entity> status should be Active or Paused] | (Nuove entità) Una nuova entità può essere solo &quot;Attiva&quot; o &quot;In pausa&quot;. |
|  | [!UICONTROL Duplicate Entries are present] | Sono incluse più righe per la stessa entità, con attributi diversi in ogni riga. Consolida le modifiche in una riga. |
|  | [!UICONTROL Invalid AMO ID given] | L’AMO ID per la riga non esiste. Ciò può verificarsi se hai modificato l’ID nel bulksheet. |
|  | [!UICONTROL Invalid row given] | La riga non include informazioni sufficienti per determinare il tipo di entità. Modifica la riga per includere tutti i campi obbligatori per il tipo di entità. |
| Account | [!UICONTROL Provide Valid Account Details] | (Bulksheet per più account) Gli identificatori dell’account non sono inclusi in tutte le righe. Immettere i valori per una delle seguenti combinazioni di colonne per ogni riga: a) &quot;[!UICONTROL AMO ID]&quot; o b) &quot;[!UICONTROL Account Name]&quot; e &quot;[!UICONTROL Platform]&quot;.&quot; |
|  | [!UICONTROL Account is disabled. Disabled Accounts cannot be processed] | Search, Social e Commerce non hanno accesso all&#39;account di rete dell&#39;annuncio, pertanto non puoi creare o modificare i dati della campagna. Verificare che le credenziali per l&#39;account di ricerca siano corrette e che l&#39;account sia abilitato. |
| Campagna | [!UICONTROL Invalid Shopping Country specified] | (Campagne commerciali) Il valore nel campo &quot;[!UICONTROL Sales Country]&quot; non è valido. Visualizza un elenco di paesi validi [per [!DNL Google Ads]](https://support.google.com/merchants/answer/160637#countrytable) e [per [!DNL Microsoft Advertising]](https://help.ads.microsoft.com/#apex/3/en/51083). |
| Tutti i componenti della campagna | [!UICONTROL Campaign creation failed] | La campagna principale non è stata creata, quindi questa entità non è stata creata. Assicurarsi che tutte le entità padre contengano tutti i campi obbligatori. |
| Gruppo di annunci | [!UICONTROL Campaign Row missing] | La campagna principale specificata non esiste, pertanto il gruppo di annunci non è stato creato. Crea la campagna principale in una nuova riga. |
|  | [!UICONTROL New adgroup has both keywords and placement] | Un gruppo di annunci può contenere parole chiave o posizionamenti, ma non entrambi. Crea gruppi di annunci separati per parole chiave e posizionamenti. |
|  | [!UICONTROL No corresponding keyword for Adgroup] | ([!DNL Yandex]) Il gruppo di annunci non è stato creato perché non include almeno una parola chiave. |
|  | [!UICONTROL No corresponding creative for Adgroup] | ([!DNL Yandex]) Il gruppo di annunci non è stato creato perché non include almeno un annuncio. |
|  | [!UICONTROL Creative Row Missing] | ([!DNL Yandex]) Il gruppo di annunci non è stato creato perché non include almeno un annuncio. |
| Tutti i componenti del gruppo di annunci | [!UICONTROL Adgroup creation failed] | Il gruppo di annunci principale non è stato creato, pertanto non è stato possibile creare questa entità. Ciò potrebbe essere dovuto a un errore nei campi del gruppo di annunci o a una campagna principale non riuscita. Assicurarsi che tutte le entità padre contengano tutti i campi obbligatori. |
|  | [!UICONTROL Adgroup Row Missing] | Il gruppo di annunci principale specificato non esiste, pertanto non è stato possibile creare l’entità. Crea il gruppo di annunci principale in una nuova riga. |
|  | [!UICONTROL Cannot modify Tracking Template at Keyword / Creative / Site Link level until Account has been migrated to use Upgraded URLs. Please retry after migration] | Il campo &quot;[!UICONTROL Tracking Template]&quot; è solo per gli account che utilizzano URL finali/avanzati. Rimuovi il valore finché non esegui la migrazione dell’account per utilizzare gli URL finali/avanzati. |
| Annuncio | [!UICONTROL Cannot modify attributes other than status code and url for &lt;ad type>] | (Tipi di annunci diversi da testo, testo espanso, prodotto, installazione app e ricerca dinamica) Puoi modificare solo lo stato e l’URL per questo tipo di annuncio. |
|  | [!UICONTROL The number of creatives under an AdGroup should not exceed 50] | Ogni gruppo di annunci può includere fino a 50 annunci e questo bulksheet ne include più di 50. Riduci il numero di annunci. |
|  | [!UICONTROL Cannot modify an ad which is either deleted/expired or under an deleted/expired campaign] | L’annuncio si trova in un’entità padre scaduta o eliminata, quindi non puoi modificarlo. |
| Parola chiave | [!UICONTROL Cannot modify a keyword/website/product which is under deleted Adgroup or Campaign] | La campagna principale o il gruppo di annunci è eliminato o scaduto, quindi non puoi modificare l’entità. |
| Posizionamento | [!UICONTROL Cannot modify a keyword/website/product which is under deleted Adgroup or Campaign] | La campagna principale o il gruppo di annunci è eliminato o scaduto, quindi non puoi modificare l’entità. |
|  | [!UICONTROL Cannot specify placement bids for websites under Display Select enabled Campaign with Search and Display Networks] | (Google Ads) Puoi fare offerte sui posizionamenti solo nelle campagne sulla sola rete di ricerca o solo sulla rete di contenuti, ma non nelle campagne mirate sia alla rete di ricerca che a quella di contenuti. |
| Gruppo di prodotti acquisti | [!UICONTROL Cannot delete Everything Else manually. It will be deleted automatically when all Product Group Conditions under the same parent are removed] | Ogni livello di gruppo di prodotti deve includere un gruppo &quot;[!UICONTROL Everything Else]&quot;. Non è possibile eliminare manualmente un gruppo &quot;[!UICONTROL Everything Else]&quot;, poiché viene eliminato automaticamente quando si eliminano tutti gli altri gruppi di prodotti allo stesso livello. |
|  | [!UICONTROL Cannot modify a keyword/website/product which is under deleted Adgroup or Campaign] | La campagna principale o il gruppo di annunci è eliminato o scaduto, quindi non puoi modificare l’entità. |
| Sitelink | [!UICONTROL Sitelinks Cannot update more than 10 site links per campaign] | ([!DNL Yandex] solo) Il messaggio non è accurato. Ogni campagna può includere fino a quattro (non 10) sitelink e questo bulksheet ne include più di quattro. Rimuovi alcuni sitelink. |
|  | [!UICONTROL Cannot update sitelinks under deleted/expired campaign] | La campagna principale è scaduta o è stata eliminata, pertanto non puoi modificare il sitelink. |
|  | [!UICONTROL Creative creation failed] | ([!DNL Yandex]) Impossibile creare il sitelink perché l&#39;annuncio non è stato creato. |
| Destinazione posizione | [!UICONTROL Cannot modify locations under deleted campaigns or adgroups] | La campagna principale o il gruppo di annunci è eliminato o scaduto, quindi non puoi modificare le destinazioni delle posizioni. |
| Esclusioni | [!UICONTROL Other than status is modified] | È possibile modificare solo lo stato di un&#39;esclusione (&quot;[!UICONTROL Active]&quot; o &quot;[!UICONTROL Deleted]&quot;). |
| Destinazioni/tipi di pubblico degli elenchi di remarketing Google | [!UICONTROL Invalid Audience given] | (Solo campagne [!DNL Google Ads]) La destinazione RLSA non corrisponde a un pubblico RLSA esistente. Correggere i valori nelle colonne &quot;[!UICONTROL Audience]&quot; e &quot;[!UICONTROL RLSA Target]&quot;. |

### Pubblica errori

I seguenti errori si verificano solo in [!UICONTROL EF Errors] file. La maggior parte degli errori di pubblicazione proviene dalla rete di annunci e sono inclusi in un file SE Errors.

| Categoria | Messaggio | Descrizione |
|----|----|----|
| Generale | [!UICONTROL Internal Error: Please Try Posting the bulksheet Again. If Problem Persists Contact Customer Care] | Operazione non riuscita. Se il problema persiste, contatta il team del tuo account Adobe. |
| Tutte le entità | [!UICONTROL Entity] è pubblicato in ad network | L’entità è stata pubblicata sul network pubblicitario, ma non è stata sincronizzata su Search, Social e Commerce contemporaneamente, pertanto i dati dell’entità non sono immediatamente disponibili in Search, Social e Commerce. Il processo di sincronizzazione viene ora attivato automaticamente.<br><br>Quando vengono sincronizzate grandi quantità di dati, i dati potrebbero non essere disponibili in Search, Social e Commerce per diverse ore o più. |
| | [!UICONTROL Skipping &lt;ENTITY> creation since &lt;PARENT ENTITY> creation failed.] | Non è stato possibile creare l&#39;entità padre, quindi questa entità figlio non è stata creata. |

>[!MORELIKETHIS]
>
>* [Informazioni sulla gestione dei dati della campagna tramite bulksheet](bulksheet-about.md)
>* [Scaricare/creare un file bulksheet](bulksheet-download.md)
>* [Convalida pagine di destinazione in file bulksheet](bulksheet-validate-landing-pages.md)
>* [Caricare un file di bulksheet o un file di errore corretto](bulksheet-upload.md)
>* [Pubblica bulksheet o file di errore corretti](bulksheet-post.md)
