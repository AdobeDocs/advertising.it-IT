---
title: Requisiti dei dati per i feed di dati che utilizzano un ID transazione
description: Fai riferimento ai requisiti di dati per i feed di dati utilizzando un ID transazione.
exl-id: 055b1417-3185-4081-83f0-9f4798058c04
feature: Search Tracking
TQID: https://experienceleague.adobe.com/TONScPVaJyxsORRD-sOrYXwEzO9rsa6ERPUo8oSRono
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 299
ht-degree: 0%

---

# Requisiti dei dati per i feed di dati che utilizzano un ID transazione

Di seguito sono riportati i campi di intestazione e i campi di dati corrispondenti necessari per ogni tipo di file di feed.

>[!NOTE]
>* Le intestazioni possono essere in qualsiasi ordine purché i dati nelle righe successive seguano lo stesso ordine. Se non includi un’intestazione, l’ordine delle righe di dati deve essere coerente con ciascun file di feed.
>* Ogni riga del file di feed deve contenere dati per una transazione e la transazione deve essere identificata da un ID transazione.

| Nome campo/colonna intestazione | Tipo | Descrizione |
| ---- | ---- | ---- |
| ID transazione (ev_transid) | Stringa sensibile a maiuscole e minuscole | L’identificatore generato dall’inserzionista associato alla transazione. Poiché il tag di tracciamento conversione di Adobe Advertising viene utilizzato per le parti online della transazione, questo deve essere lo stesso ID transazione (ev_transid) fornito da Adobe Advertising per la parte precedente della transazione. Ciò significa che il tag di conversione per la parte online della transazione deve includere una metrica di conversione per un ID transazione univoco.<br><br>**Nota:** Adobe Advertising utilizza l&#39;ID per individuare i dati della transazione precedenti e aggiornarli in base a una modalità di inserimento concordata (ad esempio, per sostituire i dati esistenti o per aumentarli con i nuovi dati). |
| Data transazione | DateTime | Data della transazione. Il formato deve essere coerente per ogni transazione. |
| Conversione specifica del client | Stringa | Una conversione che viene tracciata (ad esempio il tipo o l’importo della transazione). Discuti delle conversioni da includere con il team di implementazione di Adobe Advertising prima di avviare il feed. |

## Esempio

Il seguente file di esempio include i dati per due metriche di conversione (Prodotto e Ricavi).

```
Transaction ID,Transaction Date,Product,Revenue
12345,2010-02-17,Coffee,15.00
12346,2010-02-17,Tea,42.00
12347,2010-02-17,Coffee,22.00
```

>[!MORELIKETHIS]
>
>* [Requisiti dei file per i file del feed di conversione](feed-file-requirements.md)
>* [Tracciamento delle conversioni tramite un feed ID transazione](/help/search-social-commerce/tracking/feed-transaction-id.md)
