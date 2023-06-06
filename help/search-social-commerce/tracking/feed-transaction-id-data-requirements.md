---
title: Requisiti dei dati per i feed di dati che utilizzano un ID transazione
description: Fai riferimento ai requisiti di dati per i feed di dati utilizzando un ID transazione.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# Requisiti dei dati per i feed di dati che utilizzano un ID transazione

Di seguito sono riportati i campi di intestazione e i corrispondenti campi di dati richiesti per ogni tipo di file di feed.

>[!NOTE]
>* Le intestazioni possono essere in qualsiasi ordine purché i dati nelle righe successive seguano lo stesso ordine. Se non includi un’intestazione, l’ordine delle righe di dati deve essere coerente con ciascun file di feed.
>* Ogni riga del file di feed deve contenere dati per una transazione e la transazione deve essere identificata da un ID transazione.


| Nome campo/colonna intestazione | Tipo | Descrizione |
| ---- | ---- | ---- |
| ID transazione (ev_transid) | Stringa sensibile a maiuscole e minuscole | L’identificatore generato dall’inserzionista associato alla transazione. Poiché il tag di tracciamento conversione di Adobe Advertising viene utilizzato per le parti online della transazione, questo deve essere lo stesso ID della transazione (ev_transid) fornito da Adobe Advertising per la parte precedente della transazione. Ciò significa che il tag di conversione per la parte online della transazione deve includere una proprietà per un ID transazione univoco.<br><br>**Nota:** Adobe Advertising utilizza l’ID per individuare i vecchi dati della transazione e aggiornarli in base a una modalità di inserimento concordata (ad esempio, per sostituire i dati esistenti o per aumentarli con i nuovi dati). |
| Data transazione | DateTime | Data della transazione. Il formato deve essere coerente per ogni transazione. |
| Conversione specifica del client | Stringa | Una conversione che viene tracciata (ad esempio il tipo o l’importo della transazione). Discuti delle conversioni da includere con il team di implementazione di Adobe Advertising prima di avviare il feed. |

## Esempio

Il seguente file di esempio include i dati per due proprietà di transazione (Prodotto e Ricavi).

```
Transaction ID,Transaction Date,Product,Revenue
12345,2010-02-17,Coffee,15.00
12346,2010-02-17,Tea,42.00
12347,2010-02-17,Coffee,22.00
```

>[!MORELIKETHIS]
>
>* [Requisiti dei file per i file di feed di conversione](feed-file-requirements.md)
>* [Tracciamento delle conversioni tramite un feed ID transazione](/help/search-social-commerce/tracking/feed-transaction-id.md)

