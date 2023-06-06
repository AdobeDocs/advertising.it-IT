---
title: Assegnare valori di classificazione ai componenti conto utilizzando i bulksheet
description: Scopri come utilizzare i bulksheet per assegnare valori di classificazione ai componenti dell’account.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 7%

---

# Assegnare valori di classificazione ai componenti conto utilizzando i bulksheet

È possibile associare le classificazioni delle etichette ai valori per le seguenti entità di ricerca utilizzando i bulksheet: campagna, gruppo di annunci, parola chiave, annuncio, posizionamento, gruppo di prodotti a livello di unità e destinazione di ricerca dinamica. Ogni classificazione di etichetta può avere fino a 2000 valori.

Ogni entità può avere un valore di etichetta per classificazione. Ad esempio, Shoes_Campaign può avere un valore Color di &quot;rosso&quot; e un valore Geo di &quot;Los Angeles&quot;, ma non può avere più valori Color o Geo.

I valori delle etichette vengono ereditati dalle entità figlio, pertanto non immettere valori per le entità figlio a meno che non si desideri sostituire i valori ereditati.

>[!NOTE]
>
>Le parole chiave e la copia dell’annuncio per alcune reti e tipi di campagne pubblicitarie sono [non modificabile](/help/search-social-commerce/campaign-management/faqs-campaigns.md), il che significa che la loro modifica elimina l’entità esistente e ne crea una nuova. Quando un’entità esistente viene eliminata in questo modo, la classificazione dell’etichetta non viene assegnata alla nuova entità.

1. [Scaricare un bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) che include le entità a cui desideri assegnare i valori di classificazione delle etichette:

   * Il giorno [!UICONTROL Rows and Columns] , espandere la scheda [!UICONTROL Campaign] elenco in [!UICONTROL Bulksheet Columns] riquadro.

   * Espandi [!UICONTROL Label Classification] elenco.

   * Seleziona ogni classificazione per la quale desideri includere una colonna nel file del bulksheet.

      Ad esempio, se includi le classificazioni delle etichette &quot;Colore&quot; e &quot;Geo&quot;, il bulksheet includerà le colonne &quot;Colore&quot; e &quot;Geo&quot;.

1. Apri il file in un editor e aggiungi i valori delle etichette alle colonne di classificazione delle etichette per le entità a cui associarli. La lunghezza massima di ogni valore è di 100 caratteri e può includere caratteri ASCII e non ASCII.

   Vedi gli esempi di valori nella sezione successiva.

   Oltre ad aggiungere valori, puoi anche eliminare i valori esistenti rimuovendoli dalle righe pertinenti. Per rimuovere i valori sia da un&#39;entità padre che dalle relative entità figlio, a) includere solo la riga dell&#39;entità padre e rimuovere il valore di classificazione esistente oppure b) includere sia l&#39;entità padre che le relative entità figlio e rimuovere il valore di classificazione esistente da tutte le righe padre e figlio.

1. [Carica il file](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md) per creare le associazioni.

I valori delle etichette caricate sono visibili nelle visualizzazioni delle entità pertinenti.

## Esempio di valori di classificazione delle etichette da caricare nei bulksheet

Questo esempio include colonne per le classificazioni di etichette &quot;Colore&quot; e &quot;Geo&quot;. Per i bulksheet personalizzati, sostituisci le colonne con i nomi delle classificazioni delle etichette.

| Account | Campagna | Gruppo di annunci | Parola chiave | Annuncio | Posizionamento | Etichette | Colore | Geo |
|---|---|---|---|---|---|---|---|---|
| Acct1 | C1 |  |  |  |  |  | Verde |  |
| Acct1 | C1 | AG1 |  |  |  |  |  |  |
| Acct1 | C1 | AG1 | K1 |  |  |  |  | Regno Unito |
| Acct1 | C1 | AG1 | K2 |  |  |  | Rosso | AU |
| Acct1 | C1 | AG1 | K3 |  |  |  | Blu | DE |
| Acct1 | C1 | AG1 |  | A1 |  |  |  |  |
| Acct1 | C1 | AG1 |  | A1 |  |  | Rosso |  |
| Acct1 | C1 | AG1 |  |  | P1 |  | Rosso | AU |
| Acct1 | C1 | AG1 |  |  | P2 |  | Blu | DE |

>[!MORELIKETHIS]
>
>* [Informazioni sulle classificazioni delle etichette](classification-about.md)
>* [Creare una classificazione di etichette](classification-create.md)
>* [Assegnare valori di classificazione ai componenti account dalle viste di gestione delle campagne](classification-values-assign-campaign-management.md)
>* [Rimuovere i valori di classificazione delle etichette dai componenti dell’account](classification-values-remove.md)
>* [Elimina valori di classificazione delle etichette](classification-values-delete.md)
>* [Eliminare le classificazioni delle etichette](classification-delete.md)

