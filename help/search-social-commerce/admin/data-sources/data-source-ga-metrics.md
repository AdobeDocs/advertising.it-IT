---
title: Disponibile [!DNL Google Analytics] metriche
description: Fai riferimento a [!DNL Google Analytics] metriche disponibili per le origini dati.
role: User, Admin
exl-id: f7ac93e3-1aed-4165-ae65-7966ca192c84
feature: Search Admin, Search Data Sources
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# Appendice - Disponibile [!DNL Google Analytics] metriche

Le metriche seguenti, ad eccezione delle esclusioni annotate, sono disponibili quando sono abilitate nell’implementazione del cliente in [!DNL Google Analytics].

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
>* [Prerequisiti per la configurazione di un [!DNL Google Analytics] origine dati](data-source-prerequisites.md)
>* [Configurare un [!DNL Google Analytics] visualizzare come origine dati](data-source-configure.md)
>* [Modifica un [!DNL Google Analytics] origine dati](data-source-edit.md)
>* [Sospendere la sincronizzazione di un&#39;origine dati](data-source-pause.md)
>* [Autentica di nuovo un [!DNL Google Analytics] origine dati](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] impostazioni origine dati](data-source-settings.md)
