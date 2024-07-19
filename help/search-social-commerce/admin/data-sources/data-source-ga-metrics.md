---
title: Metriche [!DNL Google Analytics]  disponibili
description: Fai riferimento alle  [!DNL Google Analytics] metriche disponibili per le origini dati.
role: User, Admin
exl-id: 434c569d-7869-4874-90a5-5af18bc8157e
feature: Search Admin, Search Data Sources
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# Appendice - Metriche [!DNL Google Analytics] disponibili

Le metriche seguenti, ad eccezione delle esclusioni annotate, sono disponibili quando sono abilitate nell&#39;implementazione del cliente in [!DNL Google Analytics].

<!-- Notes as FYI to self:
>[!NOTE]
>
>* For some of these metrics, [!DNL Google] assigns the friendly name, and the name is consistent. For some metrics, the advertiser assigns the friendly name in [!DNL Google Analytics], and the name has a dynamic value.
>* Some metrics are assigned at the property level, and others are assigned at the view level.
-->

| Categoria | Escluso | Commenti |
| ---- | ---- | ---- |
| \[Tutti\] | Metriche con tipo di dati &quot;PERCENT&quot; | Le metriche presentate come percentuale sono sempre escluse. |
| Utente | ga:1dayUsers, ga:7dayUsers, ga:14dayUsers, ga:28dayUsers, ga:sessionPerUser | — |
| Sessione | ga:uniqueDimensionCombinations | — |
| Conversioni obiettivo | — | — |
| Tracciamento pagina | ga:entrate, ga:timeOnPage, ga:uscite | — |
| Ricerca interna | — | I nomi descrittivi di tutte le metriche da Ricerca interna sono preceduti dal valore &quot;InternalSearch: &quot; |
| Tracciamento degli eventi | — | — |
| E-commerce | — | — |
| Interazioni social | — | — |
| Eccezioni | — | — |
| Variabili o colonne personalizzate | ga:calcMetric_* | Le metriche calcolate sono sempre escluse. |

>[!MORELIKETHIS]
>
>* [Informazioni sulla sincronizzazione [!DNL Google Analytics] metriche di conversione](data-source-about.md)
>* [Prerequisiti per la configurazione di un&#39;origine dati [!DNL Google Analytics] ](data-source-prerequisites.md)
>* [Configurare una visualizzazione  [!DNL Google Analytics] come origine dati](data-source-configure.md)
>* [Modifica origine dati [!DNL Google Analytics] ](data-source-edit.md)
>* [Sospendi la sincronizzazione di un&#39;origine dati](data-source-pause.md)
>* [Autentica nuovamente un&#39;origine dati [!DNL Google Analytics] ](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] impostazioni origine dati](data-source-settings.md)
