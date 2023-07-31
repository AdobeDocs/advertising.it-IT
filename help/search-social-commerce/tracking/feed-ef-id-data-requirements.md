---
title: Requisiti in materia di dati per i feed di dati che utilizzano ID EF
description: Riferirsi ai requisiti in materia di dati per i feed di dati che utilizzano ID EF.
exl-id: 15e76f3a-c376-4e7b-b3c8-ca76fd427002
feature: Search Tracking
source-git-commit: f21283731d7a1830af585cec43805c54c81c72ff
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 0%

---

# Requisiti in materia di dati per i feed di dati che utilizzano ID EF

Di seguito sono riportati i campi di intestazione e i campi di dati corrispondenti necessari per ogni tipo di file di feed.

>[!NOTE]
>* Le intestazioni possono essere in qualsiasi ordine purché i dati nelle righe successive seguano lo stesso ordine. Se non includi un’intestazione, l’ordine delle righe di dati deve essere coerente con ciascun file di feed.
>* Ogni riga del file di feed deve contenere dati per una transazione, che deve essere identificata da un ef_id (token) generato da un Adobe Advertising.

| Nome campo/colonna intestazione | Tipo | Descrizione |
| ---- | ---- | ---- |
| ID EF | Stringa sensibile a maiuscole e minuscole | L’ef_id (token) acquisito al clic della transazione, costituito dall’ID surfista, dall’ora di clic e dal tipo di rete. Non alterare il valore. |
| ID transazione | Stringa sensibile a maiuscole e minuscole | (Facoltativo ma consigliato) ID transazione generato dall’inserzionista. La best practice prevede di includere questo valore per ogni transazione anche se l’ef_id viene utilizzato per tenere traccia della transazione al momento del reindirizzamento. |
| Data transazione | DateTime | Data della transazione. Il formato deve essere coerente per ogni transazione. |
| Conversione specifica del client | Stringa | Una conversione che viene tracciata (ad esempio il tipo o l’importo della transazione). Discuti delle conversioni da includere con il team di implementazione di Adobi Advertising prima di avviare il feed. |

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
>* [Requisiti dei file per i file di feed di conversione](feed-file-requirements.md)
>* [Tracciamento delle conversioni tramite un feed EF ID](/help/search-social-commerce/tracking/feed-efid.md)
