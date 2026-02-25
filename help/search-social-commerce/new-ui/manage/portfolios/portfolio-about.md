---
title: (Nuova interfaccia) Informazioni sui portfolio
description: Scopri i portfolio.
feature: Search Portfolios, Search Optimization
hide: true
exl-id: 8d023c22-a1dd-4608-8c72-0a61f055e7e5
source-git-commit: de3c527bd359e0d5285b90e54278983104a2a5b5
workflow-type: tm+mt
source-wordcount: '725'
ht-degree: 0%

---

# (Nuova interfaccia) Informazioni sui portfolio

*funzionalità Beta*

Puoi gestire collettivamente le campagne pubblicitarie utilizzando i portfolio (in modo simile ai portfolio di investimento). Un portfolio è un insieme di campagne pubblicitarie o set di annunci, comprese le parole chiave e gli annunci associati, ottimizzati per un singolo obiettivo aziendale. Un obiettivo può includere più conversioni ponderate e un singolo budget o obiettivo di prestazioni (ad esempio un budget mensile o un ROI target). Poiché le singole campagne/set di annunci, parole chiave e annunci possono avere prestazioni diverse tra loro (ad esempio, possono spendere importi diversi o ottenere ROI diversi), la funzionalità di ottimizzazione utilizza modelli basati sull’intelligenza artificiale per indirizzare l’intero portfolio al raggiungimento collettivo del target. Tutte le campagne in un portfolio utilizzano la stessa valuta.

Alcuni ruoli utente possono creare e configurare i portfolio. A seconda del tipo di portfolio, le impostazioni del portfolio possono includere l’obiettivo del portfolio, le campagne assegnate, la strategia di spesa, eventuali vincoli di offerta a livello di portfolio e i parametri di modellazione e ottimizzazione. Quando sei pronto a Search, Social e Commerce per iniziare l’ottimizzazione di un portfolio, modifica lo stato su &quot;ottimizzato&quot;.

Facoltativamente, puoi raggruppare i portfolio in [gruppi di portfolio](portfolio-group-manage.md) per visualizzare dati compositi per l&#39;intero gruppo.

A seconda del ruolo, è possibile generare simulazioni delle prestazioni, che utilizzano la modellazione predittiva per identificare il punto di spesa ottimale e i report dettagliati sulla precisione delle previsioni.<!-- Mention this now? In addition, all users can use the Spend Recommendation Tool to identify the optimal budget distribution across portfolios. -->

## Supporto per l’ottimizzazione tramite strategia di offerta {#optimization-by-bid-strategy}

Le campagne possono essere ottimizzate in base alla strategia di offerta della campagna o del gruppo di annunci.

>[!NOTE]
>
>Le offerte &quot;intelligenti&quot; e &quot;offerte automatizzate&quot; sono spesso utilizzate in modo intercambiabile, ma non sono la stessa cosa. Le offerte intelligenti si riferiscono solo a [!DNL Google Ads] e [!DNL Microsoft Advertising] strategie di offerte automatizzate che utilizzano le offerte al momento dell&#39;asta, il che significa che la rete di annunci ottimizza per le conversioni o i valori di conversione al momento di ogni asta.

<!-- Add "Frequency of Bidding (or other actions, like adjusting campaign budget or bid adjustment values?) -->

| Strategia d&#39;offerta | Offerta intelligente? | Offerta A Livello Di Parola Chiave/Gruppo Di Prodotti? | Livello di supporto | Tipo di obiettivo | Unità di offerta | Cosa imposta Adobe? | Cosa imposta la rete di annunci? |
|---|---|---|---|---|---|---|---|
| CPC manuale (opzione solo [!DNL Google Ads]) | — | Sì | Crea, Modifica, Ottimizza | Obiettivo singolo o multiproprietà con qualsiasi valore di peso | Parola chiave + Tipo di corrispondenza + Campagna | Offerta parola chiave, budget campagna, valori di regolazione offerta | n/d |
| ECPC (Enhanced CPC) | Sì | Sì | Crea, Modifica, Ottimizza | Obiettivo singolo o multiproprietà con qualsiasi valore di peso | Parola chiave + Tipo di corrispondenza + Campagna | Offerta parola chiave, budget campagna | Regola le offerte in tempo reale |
| Ingrandisci clic[^1] | — | — | Crea, Modifica, Ottimizza | Nessuno; ottimizza solo verso i clic | Campagna | Budget della campagna | Regola le offerte in tempo reale per massimizzare i clic nel budget |
| Massimizza conversioni<br>(con o senza TCPA) | Sì | — | Crea, Modifica, Ottimizza | Finalità a proprietà singola con un fattore di ponderazione di 1 | Campagna o gruppo di annunci ([!DNL Google Ads])<br>Solo campagna ([!DNL Microsoft Advertising]) | Budget campagna, CPA destinazione se impostato<br>TCPA può essere una strategia di offerta autonoma in [!DNL Microsoft Advertising]) | Regola le offerte in tempo reale per massimizzare gli ordini e i lead all&#39;interno del budget, raggiungendo un obiettivo CPA quando il target è impostato |
| Massimizza valore conversione<br>(con o senza TROAS) | Sì | — | Crea, Modifica, Ottimizza | Obiettivo multiproprietà con qualsiasi valore di peso o obiettivo a proprietà singola con un valore di peso maggiore di 1 (per rappresentare un valore monetario) | Campagna o gruppo di annunci ([!DNL Google Ads])<br>Solo campagna ([!DNL Microsoft Advertising]) | Budget della campagna, ROAS di destinazione se impostato<br>TROAS può essere una strategia di offerta autonoma in [!DNL Microsoft Advertising]) | Regola le offerte in tempo reale per massimizzare le entrate/i profitti entro il budget, raggiungendo un obiettivo ROAS quando il target è impostato |
| Condivisione impression target | — | — | Crea, Modifica | n/d | n/d | n/d - non può essere assegnato a un portfolio | Regola le offerte in tempo reale per raggiungere un obiettivo di condivisione delle impression |

[^1]: l&#39;impostazione della strategia di offerta [!UICONTROL Maximize Clicks] nella rete di annunci non è uguale all&#39;obiettivo di ricerca, social e Commerce [!UICONTROL Maximize Clicks]. Se la strategia di offerta è [!UICONTROL Maximize Clicks], è necessario assegnarla solo a un portfolio con ottimizzazione a livello di campagna o di gruppo di annunci, non a un portfolio con ottimizzazione a livello di parola chiave.

## Stati Portfolio {#portfolio-status}

Un portfolio può avere i seguenti stati:

<!-- **Link to include file for "Portfolio status"** -->

{{$include /help/_includes/search-portfolio-status.md}}

## Visualizzazione [!UICONTROL Portfolios]

Nella visualizzazione [!UICONTROL Portfolios] sono elencati i portfolio esistenti, con dati sulle prestazioni personalizzabili. Puoi [personalizzare le colonne all&#39;interno della visualizzazione](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md) e filtrare i dati per includere portfolio specifici [dalla barra degli strumenti](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) o dall&#39;[intestazione di colonna](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md).

Sopra la tabella di dati, puoi aprire un grafico delle prestazioni con un massimo di tre metriche calcolate su tutti i portfolio nella vista per l’intervallo di date specificato.

<!-- No options yet to edit anything within the grid, view bid changes, add a portfolio to a portfolio group, edit the Target column, or import/export DOW targets. -->

### Azioni disponibili

<!-- Update with any new options -->

<!-- within row:
* [Rename a portfolio](portfolio-rename.md)

* [View the constraints for a portfolio](portfolio-view-constraint.md)

* [View the change history for a portfolio](portfolio-view-change-history.md)
-->

* [Creare un portfolio](portfolio-create.md)

* [Duplicare un portfolio](portfolio-duplicate.md)

* [Modifica impostazioni portfolio](portfolio-edit.md)

* [Modifica in blocco le impostazioni del portfolio tramite file bulksheet](portfolio-bulksheets.md)

* [Visualizzare un grafico delle prestazioni per tutti i portfolio](portfolio-view-performance-graph.md)

* [Visualizza dettagli sulle prestazioni del portfolio](portfolio-details.md)

* [Scarica i dati nella visualizzazione [!UICONTROL Portfolios]](portfolio-view-report.md)

>[!MORELIKETHIS]
>
>* [Crea un portfolio](portfolio-create.md)
>* [Duplica un portfolio](portfolio-duplicate.md)
>* [Modifica un portfolio](portfolio-edit.md)
>* [Gestisci i report della visualizzazione dati dalla visualizzazione [!UICONTROL Portfolios]](portfolio-view-report.md)
