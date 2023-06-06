---
title: Formati di file di bulksheet supportati
description: Fare riferimento ai requisiti generali del file per i bulksheet.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '411'
ht-degree: 0%

---

# Formati di file di bulksheet supportati

## Formati di file

Puoi scaricare, caricare e pubblicare file di bulksheet per le reti di annunci supportate in uno dei seguenti formati:

* CSV (valori separati da virgole)
* TSV (valori separati da tabulazioni)
* TXT (testo Unicode), delimitato da virgole o schede
* ZIP (compresso) contenente un file in formato CSV, TSV o TXT delimitato da virgole o tabulazioni

Quando si crea o si scarica un bulksheet, questo viene creato nel formato di file specificato con tutti i dati rilevanti inclusi nel file. Utilizza le seguenti informazioni per modificare i dati nel file o per creare manualmente un bulksheet personalizzato.

## Contenuto di base di un bulksheet

Il primo record (riga) di un file bulksheet contiene un set di nomi di colonna specifici, noti collettivamente come <i>intestazione</i>. I nomi delle colonne nell’intestazione sono in un ordine specificato e corrispondono a ciascuno dei campi nei record di dati successivi. I nomi delle colonne richiesti nell’intestazione variano in base alla rete di annunci.

Ogni record successivo (riga) contiene dati, con campi contenenti valori (o nessun valore) per ogni colonna nell’intestazione.

## Dimensione massima file

I file di bulksheet possono essere fino a 2,5 GB, ovvero circa 2,5 milioni di righe.

>[!NOTE]
>
>Quando generi un bulksheet per più campagne e i dati combinati sono costituiti da più di 500.000 righe, i dati vengono suddivisi per campagna in due o più file, denominati `<bulksheet name>_1.tsv`, `<bulksheet name>_2.tsv`e così via.

## Requisiti di formattazione per diversi tipi di file

I campi dati delimitati da tabulazioni e virgole richiedono una formattazione diversa.

### File TSV e file TXT delimitati da schede

I campi dati nei file TSV e nei file TXT delimitati da tabulazioni devono essere formattati come segue:

* I campi di ogni record sono separati da caratteri di tabulazione. Per omettere un valore per un campo, utilizzare solo il carattere di tabulazione.

   Esempio: `Cruises<TAB>5000<TAB>Caribbean<TAB><TAB><TAB>`

* I campi non possono contenere caratteri di tabulazione incorporati.

### File CSV e file TXT delimitati da virgole

I campi dati nei file CSV e nei file TXT delimitati da virgole devono essere formattati come segue:

* I campi di un record sono separati da virgole. Per omettere un valore per un campo, utilizza solo la virgola.

   Esempio: `Cruises,5000,Caribbean,,,`

* Eventuali campi possono essere facoltativamente racchiusi tra virgolette doppie (`""`).

   Esempio:  `"Cruises","5000","Caribbean",`

* I campi con virgole incorporate devono essere racchiusi tra virgolette (`""`).

   Esempio: `Cruises,5000,Caribbean,"Luxurious, spacious cabins",`

* I campi con virgolette doppie incorporate devono essere racchiusi tra virgolette (`""`).

   Esempio: `Cruises,5000,Caribbean,"Customers say ""We wish we could stay forever."",`

* I campi con spazi iniziali o finali devono essere racchiusi tra virgolette doppie (`""`).

   Esempio: `Cruises,5000,Caribbean,"  Come see what we mean.  ",`

>[!MORELIKETHIS]
>
>* [Informazioni sulla gestione dei dati della campagna tramite bulksheet](../bulksheet-about.md)
>* [Operazioni eseguibili nei bulksheet](bulksheet-operations.md)
>* [Appendice - Errori di bulksheet](../bulksheet-errors.md)
>* [Scaricare/creare un file bulksheet](../bulksheet-download.md)

