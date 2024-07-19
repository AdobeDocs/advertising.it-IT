---
title: Dati del bulksheet per  [!DNL Yahoo! Display Network]  account
description: Fai riferimento ai campi di intestazione e ai campi dati nei bulksheet scaricati per  [!DNL Yahoo! Display Network]  account.
exl-id: 8d938009-6edc-4420-8863-21ed241616f8
feature: Search Bulksheets
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 0%

---

# Appendice - Dati bulksheet per account [!DNL Yahoo! Display Network]

<!-- 
[Re-add "Required" to title, file name, and TOC if you add the ability to create/edit campaigns using YDN bulksheets. Then will also need to add more text below, like for the other SEs.]
-->

È possibile scaricare i dati per gli account [!DNL Yahoo! Display Network] in blocco, ma non caricare o pubblicare i bulksheet nella rete di annunci.

<!-- Hiding because this is probably too long a list to be useful.

## Available header fields

The following example shows data in comma-delimited values. If you're using tab-separated values, then the data looks different.

Platform,Acct Name,Campaign Name,Ad Group Name,Ad Name, Ad Title,Description Line 1,Description Line 2,Base URL/Final URL,Destination URL,[Advertiser-specific Label Classification],Bid Rules,Constraints,Campaign Status,Ad Group Status,Ad Status,Campaign ID,Ad Group ID,Ad ID,AMO ID,EF Error Message

-->

## Campi dati disponibili

| Campo | Campagna | Gruppo di annunci | Annuncio | Descrizione |
|----|----|----|----|----|
| [!UICONTROL Platform] | n/d | n/d | n/d | (Incluso nei bulksheet generati a scopo informativo) La piattaforma pubblicitaria. |
| [!UICONTROL Acct  Name] | Se incluso | Se incluso | Se incluso | Nome univoco che identifica un account di rete di annunci. |
| [!UICONTROL Campaign Name] | Se incluso | Se incluso | Se incluso | Il nome univoco che identifica una campagna per un account. |
| [!UICONTROL Ad Group Name] | n/d | Se incluso | Se incluso | Nome univoco che identifica un gruppo di annunci. |
| [!UICONTROL Ad Name] | n/d | n/d | Se incluso | Nome univoco che identifica l’annuncio all’interno di un gruppo di annunci. La lunghezza massima è di 50 caratteri. |
| [!UICONTROL Ad Title] | n/d | n/d | Se incluso | Titolo di un annuncio. |
| [!UICONTROL Description Line 1] | n/d | n/d | Se incluso | La prima riga del corpo di un annuncio. |
| [!UICONTROL Description Line 2] | n/d | n/d | Se incluso | Seconda riga del corpo di un annuncio. |
| [!UICONTROL Base URL/Final URL] | n/d | n/d | Se incluso | L’URL della pagina di destinazione a cui vengono indirizzati gli utenti finali quando fanno clic sull’annuncio, inclusi eventuali parametri di aggiunta configurati per la campagna o l’account. Gli URL di base/finali a livello di parola chiave sostituiscono gli URL a livello di annuncio e superiore. |
| [!UICONTROL Destination URL] | n/d | n/d | n/d | (Incluso nei bulksheet generati a scopo informativo; non pubblicato nella rete di annunci) Per gli account con URL di destinazione, questo valore è l’URL che collega un annuncio a un URL/pagina di destinazione di base sul sito web dell’inserzionista (a volte tramite un altro sito che tiene traccia del clic e quindi reindirizza l’utente alla pagina di destinazione). Include tutti i parametri di aggiunta configurati per la campagna o l’account Search, Social e Commerce. Se hai generato URL di tracciamento, questo valore si basa sui parametri di tracciamento riportati nelle impostazioni dell’account e della campagna. Se hai aggiunto dei parametri specifici per un annuncio, questi possono essere sostituiti con parametri equivalenti per Search, Social e Commerce. |
| \[Classificazione etichetta specifica dell’inserzionista\] | Se incluso | Se incluso | Se incluso | (Nome per una classificazione di etichetta specifica dell’inserzionista, ad esempio &quot;Colore&quot; per una classificazione di etichetta denominata Colore) Valore per la classificazione specificata associata all’entità. |
| [!UICONTROL Constraints] | Se incluso | Se incluso | n/d | Vincolo assegnato all&#39;entità. |
| [!UICONTROL Campaign Status] | Se incluso | n/d | n/d | Stato di visualizzazione della campagna: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> o <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Ad Group Status] | n/d | Se incluso | n/d | Stato di visualizzazione del gruppo di annunci: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> o <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Keyword Status] | n/d | n/d | Se incluso | Stato di visualizzazione della parola chiave: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> o <i>[!UICONTROL Deleted]</i> (solo parole chiave esistenti). |
| [!UICONTROL Campaign ID] | Se incluso | Se incluso | Se incluso | L’ID univoco che identifica una campagna esistente. |
| [!UICONTROL Ad Group ID] | n/d | Se incluso | Se incluso | L’ID univoco che identifica un gruppo di annunci esistente. |
| [!UICONTROL Keyword ID] | n/d | n/d | Se incluso | ID univoco che identifica una parola chiave esistente. |
| [!UICONTROL AMO ID] | n/d | n/d | n/d | (Nei bulksheet generati) Identificatore univoco generato da Adobe per un’entità sincronizzata. |
| [!UICONTROL EF Error Message] | n/d | n/d | n/d | (Incluso nei bulksheet generati a scopo informativo) Segnaposto per la visualizzazione dei messaggi di errore di Search, Social e Commerce relativi ai dati nella riga. I messaggi di errore sono inclusi nei file [!UICONTROL EF Errors]. |

>[!MORELIKETHIS]
>
>* [Scaricare/creare un file bulksheet](../bulksheet-download.md)
