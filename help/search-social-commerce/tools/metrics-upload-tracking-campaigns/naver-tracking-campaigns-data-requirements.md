---
title: Requisiti dei dati per le metriche di traffico e conversione per  [!DNL Naver] account di solo tracciamento
description: Fai riferimento ai requisiti di caricamento dei dati per  [!DNL Naver] account di solo tracciamento.
exl-id: cc8ee5de-2bf2-48fd-9fa7-28421aed673f
feature: Search Tools
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# Requisiti dei dati delle metriche per [!DNL Naver] account di solo tracciamento

Di seguito sono riportati i requisiti di dati per le metriche di traffico e conversione [!DNL Naver] per gli account di solo tracciamento.

I file di dati devono essere in formato TSV, CSV o TXT.

I seguenti campi di intestazione sono obbligatori e facoltativi. Ogni riga di dati deve includere un valore aggregato giornaliero per almeno un campo di metrica.

| Nome campo/colonna intestazione | Tipo | Descrizione |
| ---- | ---- | ---- |
| Periodo | DateTime | Data a cui si applicano i dati, nel formato `YYYY.MM.DD.` (ad esempio `2019.11.15.`, con un periodo successivo al giorno). |
| Campagna | Stringa sensibile a maiuscole e minuscole | Il nome della campagna. |
| Adgroup (come una parola) | Stringa sensibile a maiuscole e minuscole | Il nome del gruppo di annunci. |
| Parola chiave | Stringa sensibile a maiuscole e minuscole | (Annunci per parole chiave) Parola chiave che ha generato l’annuncio. |
| [Metrica] | Intero | (Facoltativo) Il numero di [qualsiasi metrica stia misurando].</br><br>Le metriche standard includono impressioni, costo e clic. Puoi includere qualsiasi metrica aggiuntiva desiderata dalla rete di annunci. Includi ogni metrica in una colonna separata.<br><br><b>Note:</b><ul><li>L&#39;intestazione di colonna per Costo deve essere &quot;Costo (KRW)&quot;.</li><li>Per includere il costo (KRW) per gli annunci di marchio, dividi manualmente il costo mensile fisso per giorno a livello di gruppo di annunci.</li><li>Rimuovi tutte le virgole dai valori delle metriche standard. Ad esempio, utilizza 1000 invece di 1000.</li><li>Per i valori Null, utilizzare 0.</li></ul> |

>[!MORELIKETHIS]
>
>* [Implementa [!DNL Naver] account di sola verifica](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
>* [Appendice - Dati bulksheet richiesti per [!DNL Naver] account](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md))
>* [Carica le metriche di traffico e conversione per [!DNL Naver] account di solo tracciamento](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md)
