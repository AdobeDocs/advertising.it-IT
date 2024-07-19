---
title: Assegnare valori di classificazione ai componenti conto utilizzando i bulksheet
description: Scopri come utilizzare i bulksheet per assegnare valori di classificazione ai componenti dell’account.
exl-id: b2dfd487-097c-45f8-a6a5-24395fdb2b85
feature: Search Label Classifications
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 0%

---

# Assegnare valori di classificazione ai componenti conto utilizzando i bulksheet

È possibile associare le classificazioni delle etichette ai valori per le seguenti entità di ricerca utilizzando i bulksheet: campagna, gruppo di annunci, parola chiave, annuncio, posizionamento, gruppo di prodotti a livello di unità e destinazione di ricerca dinamica. Ogni classificazione di etichetta può avere fino a 2000 valori.

Ogni entità può avere un valore di etichetta per classificazione. Ad esempio, Shoes_Campaign può avere un valore Color di &quot;rosso&quot; e un valore Geo di &quot;Los Angeles&quot;, ma non può avere più valori Color o Geo.

I valori delle etichette vengono ereditati dalle entità figlio, pertanto non immettere valori per le entità figlio a meno che non si desideri sostituire i valori ereditati.

>[!NOTE]
>
>Le parole chiave e la copia dell&#39;annuncio per alcune reti di annunci e tipi di campagne sono [non modificabili](/help/search-social-commerce/campaign-management/faqs-campaigns.md), il che significa che la loro modifica elimina l&#39;entità esistente e ne crea una nuova. Quando un’entità esistente viene eliminata in questo modo, la classificazione dell’etichetta non viene assegnata alla nuova entità.

1. [Scaricare un bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) che include le entità alle quali si desidera assegnare i valori di classificazione delle etichette:

   * Nella scheda [!UICONTROL Rows and Columns], espandere l&#39;elenco [!UICONTROL Campaign] nel riquadro [!UICONTROL Bulksheet Columns].

   * Espandere l&#39;elenco [!UICONTROL Label Classification].

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
| Att1 | C1 | | | | | | Verde | |
| Att1 | C1 | AG1 | | | | | | |
| Att1 | C1 | AG1 | K1 | | | | | Regno Unito |
| Att1 | C1 | AG1 | K2 | | | | Rosso | AU |
| Att1 | C1 | AG1 | K3 | | | | Blu | DE |
| Att1 | C1 | AG1 | | A1 | | | | |
| Att1 | C1 | AG1 | | A1 | | | Rosso | |
| Att1 | C1 | AG1 | | | P1 | | Rosso | AU |
| Att1 | C1 | AG1 | | | P2 | | Blu | DE |

>[!MORELIKETHIS]
>
>* [Informazioni sulle classificazioni delle etichette](classification-about.md)
>* [Creare una classificazione di etichette](classification-create.md)
>* [Assegna valori di classificazione ai componenti account dalle visualizzazioni di gestione campagne](classification-values-assign-campaign-management.md)
>* [Rimuovere i valori di classificazione delle etichette dai componenti dell&#39;account](classification-values-remove.md)
>* [Elimina i valori di classificazione delle etichette](classification-values-delete.md)
>* [Elimina classificazioni etichette](classification-delete.md)
