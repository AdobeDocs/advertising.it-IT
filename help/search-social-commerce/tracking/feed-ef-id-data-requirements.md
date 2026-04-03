---
title: Requisiti in materia di dati per i feed di dati che utilizzano ID EF
description: Riferirsi ai requisiti in materia di dati per i feed di dati che utilizzano ID EF.
exl-id: 507ed42c-349f-4311-af61-8f7a27794162
feature: Search Tracking
TQID: https://experienceleague.adobe.com/p66X8xVlx-JwKjGgXxonJRRu78Q8F4109VkaIVtUbwU
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 256
ht-degree: 0%

---

# Requisiti in materia di dati per i feed di dati che utilizzano ID EF

Di seguito sono riportati i campi di intestazione e i campi di dati corrispondenti necessari per ogni tipo di file di feed.

>[!NOTE]
>* Le intestazioni possono essere in qualsiasi ordine purché i dati nelle righe successive seguano lo stesso ordine. Se non includi un’intestazione, l’ordine delle righe di dati deve essere coerente con ciascun file di feed.
>* Ogni riga del file di feed deve contenere dati per una transazione, che deve essere identificata da un ef_id (token) generato da Adobe Advertising.

| Nome campo/colonna intestazione | Tipo | Descrizione |
| ---- | ---- | ---- |
| ID EF | Stringa sensibile a maiuscole e minuscole | L’ef_id (token) acquisito al clic della transazione, costituito dall’ID surfista, dall’ora di clic e dal tipo di rete. Non alterare il valore. |
| ID transazione | Stringa sensibile a maiuscole e minuscole | (Facoltativo ma consigliato) ID transazione generato dall’inserzionista. La best practice prevede di includere questo valore per ogni transazione anche se l’ef_id viene utilizzato per tenere traccia della transazione al momento del reindirizzamento. |
| Data transazione | DateTime | Data della transazione. Il formato deve essere coerente per ogni transazione. |
| Conversione specifica del client | Stringa | Una conversione che viene tracciata (ad esempio il tipo o l’importo della transazione). Discuti delle conversioni da includere con il team di implementazione di Adobe Advertising prima di avviare il feed. |

## Esempio

Il seguente file di esempio include i dati per due metriche di conversione (Prodotto e Ricavi).

```
EF ID,Client Transaction ID, Transaction Date,Product,Revenue
TIl4VQqoEEQAAG8CU5EAAACY:20100217062449:s,04896325,2010-02-17,Coffee,15.00
SOl5PRKlPEILDG6CL3QYENOI:20100217065632:s,04896490,2010-02-17,Tea,42.00
TRl4BEtoTPMBEW4SU5ZUMEPIE:20100217065804:s,04896552,2010-02-17,Coffee,22.00
```

>[!MORELIKETHIS]
>
>* [Requisiti dei file per i file del feed di conversione](feed-file-requirements.md)
>* [Tracciamento delle conversioni tramite un feed EF ID](/help/search-social-commerce/tracking/feed-efid.md)
