---
title: Metriche [!DNL Google Analytics]  disponibili
description: Fai riferimento alle  [!DNL Google Analytics] metriche disponibili per le origini dati.
role: User, Admin
exl-id: 434c569d-7869-4874-90a5-5af18bc8157e
feature: Search Admin, Search Data Sources
TQID: https://experienceleague.adobe.com/hRYeNcQu4uUTCAHXcF9zaZfQm-mw6kDlqvs2AxZhED8
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: e55292b5-d4a1-4c98-9c20-2a2c5bea07fb
subfeature_v2:
  - id: e778848d-90fa-4520-b80f-e8dd7dfdcffc
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 131
ht-degree: 0%

---

# Appendice - Metriche [!DNL Google Analytics] disponibili

Le metriche seguenti, ad eccezione delle esclusioni annotate, sono disponibili quando sono abilitate nell&#39;implementazione del cliente in [!DNL Google Analytics].

<!--
 Notes as FYI to self:
>[!NOTE]
>
>* For some of these metrics, [!DNL Google] assigns the friendly name, and the name is consistent. For some metrics, the advertiser assigns the friendly name in [!DNL Google Analytics], and the name has a dynamic value.
>* Some metrics are assigned at the property level, and others are assigned at the view level.
-->

| Categoria | Escluso | Commenti |
| ---- | ---- | ---- |
| \[Tutti\] | Metriche con tipo di dati &quot;PERCENT&quot; | Le metriche presentate come percentuale sono sempre escluse. |
| Utente | ga:1dayUsers, ga:7dayUsers, ga:14dayUsers, ga:28dayUsers, ga:sessionsPerUser | — |
| Sessione | ga:uniqueDimensionCombinations | — |
| Conversioni obiettivo | — | — |
| Tracciamento pagina | ga:entrances, ga:timeOnPage, ga:exits | — |
| Ricerca interna | — | I nomi descrittivi di tutte le metriche da Ricerca interna sono preceduti dal valore &quot;InternalSearch: &quot; |
| Tracciamento degli eventi | — | — |
| E-commerce | — | — |
| Interazioni social | — | — |
| Eccezioni | — | — |
| Variabili o colonne personalizzate | ga :calcMetric_* | Le metriche calcolate sono sempre escluse. |

>[!MORELIKETHIS]
>
>* [Informazioni sulla sincronizzazione [!DNL Google Analytics] metriche di conversione](data-source-about.md)
>* [Prerequisiti per la configurazione di un&#39;origine dati [!DNL Google Analytics] &#x200B;](data-source-prerequisites.md)
>* [Configurare una visualizzazione  [!DNL Google Analytics] come origine dati](data-source-configure.md)
>* [Modifica origine dati [!DNL Google Analytics] &#x200B;](data-source-edit.md)
>* [Sospendi la sincronizzazione di un&#39;origine dati](data-source-pause.md)
>* [Autentica nuovamente un&#39;origine dati [!DNL Google Analytics] &#x200B;](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] impostazioni origine dati](data-source-settings.md)
