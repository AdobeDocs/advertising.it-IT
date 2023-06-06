---
title: Requisiti dei dati per le metriche di traffico e conversione per [!DNL Naver] account di solo tracciamento
description: Fai riferimento ai requisiti di caricamento dei dati per [!DNL Naver] account di solo tracciamento.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

---

# Requisiti dei dati delle metriche per [!DNL Naver] account di solo tracciamento

Di seguito sono riportati i requisiti relativi ai dati per [!DNL Naver] metriche di traffico e conversione per gli account di solo tracciamento.

I file di dati devono essere in formato TSV, CSV o TXT.

I seguenti campi di intestazione sono obbligatori e facoltativi. Ogni riga di dati deve includere un valore aggregato giornaliero per almeno un campo di metrica.

| Nome campo/colonna intestazione | Tipo | Descrizione |
| ---- | ---- | ---- |
| Periodo | DateTime | Data a cui si applicano i dati, nel formato `YYYY.MM.DD.` (ad esempio `2019.11.15.`, con un punto dopo il giorno). |
| Campagna | Stringa sensibile a maiuscole e minuscole | Il nome della campagna. |
| Adgroup (come una parola) | Stringa sensibile a maiuscole e minuscole | Il nome del gruppo di annunci. |
| Parola chiave | Stringa sensibile a maiuscole e minuscole | (Annunci per parole chiave) Parola chiave che ha generato l’annuncio. |
| [Metrica] | Intero | (Facoltativo) Il numero di [qualunque sia la metrica da misurare].</br><br>Le metriche standard includono impression, costo e clic. Puoi includere qualsiasi metrica aggiuntiva desiderata dalla rete di annunci. Includi ogni metrica in una colonna separata.<br><br><b>Note:</b><ul><li>L&#39;intestazione di colonna per Costo deve essere &quot;Costo (KRW)&quot;.</li><li>Per includere il costo (KRW) per gli annunci di marchio, dividi manualmente il costo mensile fisso per giorno a livello di gruppo di annunci.</li><li>Rimuovi tutte le virgole dai valori delle metriche standard. Ad esempio, utilizza 1000 invece di 1000.</li><li>Per i valori Null, utilizzare 0.</li></ul> |

>[!MORELIKETHIS]
>
>* [Implementare [!DNL Naver] account di solo tracciamento](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
>* [Appendice - Dati di bulksheet richiesti per [!DNL Naver] account](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md))
>* [Caricare traffico e metriche di conversione per [!DNL Naver] account di solo tracciamento](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md)

