---
title: Dati bulksheet richiesti per  [!DNL Naver]  account
description: Fai riferimento ai campi di intestazione e ai campi dati obbligatori nei bulksheet per  [!DNL Naver]  account.
exl-id: 1bfcdbb6-8026-4230-ab6b-b7c79b0d185a
feature: Search Bulksheets
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '998'
ht-degree: 0%

---

# Appendice - Dati bulksheet richiesti per i conti [!DNL Naver]

Compilare gli account [!DNL Naver] in Search, Social e Commerce generando un file bulksheet in [!DNL Naver] e caricandolo in Search, Social e Commerce.

{{$include /help/_includes/bulksheet-appendices-intro.md}}

<!-- Hiding because this is probably too long a list to be useful.

## Available header fields

Platform,Acct Name,Campaign Name,Ad Group Name,Keyword,Base URL,Destination URL,[Advertiser-specific Label Classification],Constraints,Campaign Status,Ad Group Status,Keyword Status,Campaign ID,Ad Group ID,Keyword ID,AMO ID,Error Message

{{$include /help/_includes/bulksheet-headers-note.md}}

-->

## Campi dati disponibili

{{$include /help/_includes/bulksheet-appendices-intro-required-data.md}}

| Campo | Campagna | Gruppo di annunci | Parola chiave | Descrizione |
|----|----|----|----|----|
| [!UICONTROL Platform] | n/d | n/d | n/d | (Incluso nei bulksheet generati a scopo informativo) La piattaforma pubblicitaria. Obbligatorio a meno che ogni riga non includa un AMO ID per l’entità. |
| [!UICONTROL Acct Name] | Obbligatorio/facoltativo | Obbligatorio/facoltativo | Obbligatorio/facoltativo | Nome univoco che identifica un account di rete di annunci. Obbligatorio a meno che ogni riga non includa un AMO ID per l’entità. |
| [!UICONTROL Campaign Name] | Obbligatorio | Obbligatorio | Obbligatorio | Il nome univoco che identifica una campagna per un account. |
| [!UICONTROL Ad Group Name] | n/d | Obbligatorio | Obbligatorio | Nome univoco che identifica un gruppo di annunci. |
| [!UICONTROL Keyword] | n/d | n/d | Obbligatorio | La stringa della parola chiave. |
| [!UICONTROL Base URL] | n/d | n/d | Facoltativo | L’URL della pagina di destinazione a cui vengono indirizzati gli utenti finali quando fanno clic sull’annuncio, inclusi eventuali parametri di aggiunta configurati per la campagna o l’account.<br><br>Gli URL di base/finali a livello di parola chiave sostituiscono gli URL a livello di annuncio e superiore. |
| [!UICONTROL Destination URL] | n/d | n/d | n/d | (Incluso nei bulksheet generati a scopo informativo; non pubblicato nella rete di annunci) Per gli account con URL di destinazione, questo valore è l’URL che collega un annuncio a un URL/pagina di destinazione di base sul sito web dell’inserzionista (a volte tramite un altro sito che tiene traccia del clic e quindi reindirizza l’utente alla pagina di destinazione). Include tutti i parametri di aggiunta configurati per la campagna o l’account Search, Social e Commerce. Se hai generato URL di tracciamento, questo valore si basa sui parametri di tracciamento riportati nelle impostazioni dell’account e della campagna. Se hai aggiunto parametri specifici per un annuncio, questi possono essere sostituiti con parametri equivalenti per Search, Social e Commerce.<br><br>Per gli account con URL finali, questa colonna mostra lo stesso valore di [!UICONTROL Base URL/Final URL column]. |
| \[Classificazione etichetta specifica dell’inserzionista\] | Facoltativo | Facoltativo | Facoltativo | (Nome per una classificazione di etichetta specifica dell’inserzionista, ad esempio &quot;Colore&quot; per una classificazione di etichetta denominata Colore) Valore per la classificazione specificata associata all’entità. Puoi includere un solo valore per classificazione per entità (ad esempio &quot;rosso&quot; per la classificazione dell’etichetta &quot;Colore&quot; per la campagna A). La lunghezza massima è di 100 caratteri e il valore può includere caratteri ASCII e non ASCII.<br><br>Le classificazioni delle etichette e i relativi valori vengono applicati a tutti i componenti figlio. I nuovi componenti aggiunti in seguito vengono associati automaticamente all&#39;etichetta. Le classificazioni delle etichette per i gruppi di prodotti vengono applicate al livello di unità (più granulare).<br><br>Il nome della classificazione e il valore della classificazione non fanno distinzione tra maiuscole e minuscole. |
| [!UICONTROL Constraints] | Facoltativo | Facoltativo | Facoltativo | Vincolo assegnato all&#39;entità. È possibile assegnare un solo vincolo per entità.<br><br>I vincoli vengono ereditati dalle entità figlio, pertanto non è necessario immettere valori per le entità figlio a meno che non si desideri ignorare i valori ereditati. |
| [!UICONTROL Campaign Status] | Facoltativo: Crea o modifica<br>Obbligatorio: elimina | n/d | n/d | Stato di visualizzazione della campagna: *[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> o <i>[!UICONTROL Deleted]</i> (solo campagne esistenti). Il valore predefinito per le nuove campagne è <i>[!UICONTROL Active]</i>. Per eliminare una campagna attiva o in pausa, immettere il valore &quot;[!UICONTROL Deleted]&quot;. |
| [!UICONTROL Ad Group Status] | n/d | Facoltativo: Crea o modifica<br>Obbligatorio: elimina | n/d | Stato di visualizzazione del gruppo di annunci: *[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> o <i>[!UICONTROL Deleted]</i> (solo gruppi di annunci esistenti). Il valore predefinito per i nuovi gruppi di annunci è <i>[!UICONTROL Active]</i>. Per eliminare un gruppo di annunci attivo o in pausa, immettere il valore &quot;[!UICONTROL Deleted]&quot;. |
| [!UICONTROL Keyword Status] | n/d | n/d | Facoltativo: Crea o modifica<br>Obbligatorio: elimina | Stato di visualizzazione della parola chiave: *[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> o <i>[!UICONTROL Deleted]</i> (solo parole chiave esistenti). Il valore predefinito per le nuove parole chiave è <i>[!UICONTROL Active]</i>. Per eliminare una parola chiave attiva o in pausa, immettere il valore &quot;[!UICONTROL Deleted]&quot;. |
| [!UICONTROL Campaign ID] | n/d: Create<br>Obbligatorio/Facoltativo: Edit or delete | Facoltativo | Facoltativo | L’ID univoco che identifica una campagna esistente. Nei file CSV e TSV deve essere preceduto da virgolette singole (&#39;).[^1] Richiesto solo quando si modifica il nome della campagna, a meno che la riga non includa un AMO ID per la campagna. |
| [!UICONTROL Ad Group ID] | n/d | n/d: Create<br>Obbligatorio/Facoltativo: Edit or delete | Facoltativo | L’ID univoco che identifica un gruppo di annunci esistente. Nei file CSV e TSV deve essere preceduto da virgolette singole (&#39;).[^1] Richiesto solo quando si modifica il nome del gruppo di annunci, a meno che la riga non includa un AMO ID per il gruppo di annunci. |
| [!UICONTROL Keyword ID] | n/d | n/d | n/d: Create<br>Obbligatorio/Facoltativo: Edit<br>Obbligatorio: Delete | ID univoco che identifica una parola chiave esistente. Nei file CSV e TSV deve essere preceduto da virgolette singole (&#39;).[^1] Obbligatorio solo quando si modifica il nome della parola chiave, a meno che la riga non includa a) colonne di proprietà sufficienti per identificare la parola chiave o b) un AMO ID. |
| [!UICONTROL AMO ID] | n/d: Create<br>Facoltativo: Edit or delete | n/d: Create<br>Facoltativo: Edit or delete | n/d: Create<br>Facoltativo: Edit or delete | (Nei bulksheet generati) Identificatore univoco generato da [!DNL Adobe] per un&#39;entità sincronizzata. Per gli annunci di ricerca responsive, è necessario l’AMO ID per modificare o eliminare gli annunci a meno che non includa [!UICONTROL Ad ID]. Per modificare i dati per tutti gli altri tipi di entità con un AMO ID, è necessario l’AMO ID per modificare o eliminare i dati, a meno che non si includano l’ID entità e l’ID entità principale.<br><br>Search, Social e Commerce utilizzano il valore per determinare l&#39;identità corretta da modificare, ma non pubblicano l&#39;ID sulla rete di annunci. |
| [!UICONTROL EF Error Message] | n/d | n/d | n/d | (Incluso nei bulksheet generati a scopo informativo) Segnaposto per la visualizzazione dei messaggi di errore di Search, Social e Commerce relativi ai dati nella riga. I messaggi di errore sono inclusi nei file [!UICONTROL EF Errors]. Questo valore non viene inviato alla rete di annunci. |
| [!UICONTROL SE Error Message] | n/d | n/d | n/d | (Incluso nei bulksheet generati a scopo informativo) Segnaposto per la visualizzazione dei messaggi di errore provenienti dalla rete di annunci relativi ai dati nella riga. I messaggi di errore sono inclusi nei file [!UICONTROL SE Errors]. Questo valore non viene inviato alla rete di annunci. |

[^1]: all&#39;apertura del file, i numeri elevati vengono convertiti in notazione scientifica, ad esempio 2,12E+09 per 2115585666. Per visualizzare le cifre nella notazione standard, selezionare una cella della colonna e fare clic all&#39;interno della barra della formula.

>[!MORELIKETHIS]
>
>* [Appendice - Errori bulksheet](../bulksheet-errors.md)
>* [Operazioni eseguibili nei bulksheet](bulksheet-operations.md)
>* [Formati di file di bulksheet supportati](bulksheet-file-formats.md)
>* [Scaricare/creare un file bulksheet](../bulksheet-download.md)
>* [Formati di tracciamento dei clic per [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [Caricare un file di bulksheet o un file di errore corretto](../bulksheet-upload.md)
>* [Implementa [!DNL Naver] account di sola verifica](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
