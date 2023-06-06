---
title: Requisiti dei file per i file di feed di conversione
description: Fai riferimento ai requisiti per i file di feed di conversione.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '359'
ht-degree: 0%

---

# Requisiti dei file per i file di feed di conversione

Di seguito sono riportati i requisiti per il formato di file, i campi dati obbligatori e facoltativi, il nome del file e il protocollo di trasferimento file per i file di feed.

## Formato file

Il file di dati deve essere in formato testo normale (TXT), valori delimitati da virgole (CSV) o valori delimitati da tabulazioni (TSV). Il file può essere costituito da una riga di intestazione e da righe di dati con valori separati da tabulazioni, virgole o altri caratteri (ma non spazi):

* **Riga intestazione:** (Facoltativo) La prima riga del file è un&#39;intestazione, che specifica i nomi di campo (o di colonna) richiesti in un ordine specifico, separati da tabulazioni o virgole. I nomi delle colonne richiesti includono le proprietà della transazione che Adobe Advertising sta monitorando come conversioni.

* **Righe dati:** Ogni riga successiva include campi dati nello stesso ordine dell’intestazione e separati da tabulazioni o virgole. Se il primo record non è un&#39;intestazione, ogni riga di dati deve includere tutti i campi possibili in un ordine specificato. I valori di tutti gli ID e le proprietà della transazione devono essere alfanumerici.

   Quando più clic su uno o più annunci portano a una transazione, è necessario determinare l’ID clic e l’ID di tracciamento a cui attribuire la transazione. Poiché per ogni transazione viene segnalato un ID univoco, è possibile aggiornare le singole transazioni.

## Convenzione per la denominazione dei file

Il nome del file deve includere la data ed essere coerente. Ad esempio, se utilizzi il formato AAAAMMGG.txt, un file inviato il 15 maggio 2011 deve essere denominato 20110515.txt.

## Protocollo di trasferimento file

Invia il file tramite il protocollo di trasferimento SFTP, utilizzando la porta 22. Dovrai fornire le informazioni sulla chiave pubblica.  Il team dell’account Adobe o il team di implementazione ti fornirà la posizione del server e le credenziali necessarie per il trasferimento dei file.

>[!TIP]
>
>I feed di dati di conversione vengono elaborati più volte al giorno. Carica il feed giornaliero il prima possibile dopo le 12:00, ora locale, in modo che Adobe Advertising possa elaborare i dati e renderli disponibili nell’interfaccia utente di reporting nelle prime ore del mattino.

>[!MORELIKETHIS]
>
>* [Requisiti in materia di dati per i feed di dati che utilizzano ID EF](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md)
>* [Requisiti dei dati per i feed di dati che utilizzano un ID transazione](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md)

