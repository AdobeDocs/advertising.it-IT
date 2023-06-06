---
title: Tracciamento delle conversioni tramite un feed ID transazione
description: Scopri come utilizzare un feed ID transazione per i dati di tracciamento della conversione.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---

# Tracciamento delle conversioni tramite un feed ID transazione

Quando un inserzionista ha transazioni sia online che offline, Adobe Advertising può tracciare le transazioni online tramite il pixel di tracciamento delle conversioni di Adobe Advertising e l’inserzionista può tracciare le transazioni offline utilizzando un ID transazione e consegnarle tramite un feed:

* Per le transazioni online, Adobe Advertising tiene traccia dei clic sugli annunci e delle transazioni risultanti sul sito web.

* L’inserzionista deve tenere traccia delle conversioni offline e inviare file di feed a livello di transazione ad Adobe Advertising.

## Panoramica sull’implementazione

*Account manager dell’agenzia, [!DNL Adobe] solo ruoli utente amministratore e responsabile account*

1. Utilizza le opzioni di tracciamento account o campagna &quot;[!UICONTROL EF Redirect]&quot; e &quot;[!UICONTROL Auto Upload]&quot; per generare automaticamente un URL di destinazione o finale per ogni parola chiave (per il tracciamento a livello di parola chiave) o annuncio (per il tracciamento a livello di annuncio) nell’account o nella campagna.

1. Imposta il tracciamento delle conversioni Adobe Advertising per le conversioni online. Questa procedura è la stessa utilizzata per gli inserzionisti con tracciamento delle conversioni basato su pixel per Adobe Advertising. È importante generare tag di conversione che includano un parametro per un ID transazione univoco (`ev_transid=<transid>`).

1. Per la parte offline di ciascuna transazione, l&#39;inserzionista genera lo stesso ID transazione utilizzato nella parte online della transazione da includere nel file di feed.

1. L’inserzionista carica un file con [dati di conversione richiesti](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md) nel percorso del server designato.

1. Technical Services analizza i dati di conversione nei file caricati, quindi carica i dati in Adobe Advertising. Adobe Advertising tiene traccia dei dati rispetto a singole parole chiave, annunci e posizionamenti e crea una previsione dei ricavi per ciascuno di essi.

1. I servizi tecnici convalidano i dati elaborati in base ai dati del feed e verificano eventuali [transazioni orfane](/help/search-social-commerce/glossary.md#o-p).

>[!MORELIKETHIS]
>
>* [Requisiti dei file per i file di feed di conversione](feed-file-requirements.md)
>* [Requisiti dei dati per i feed di dati che utilizzano un ID transazione](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md)

