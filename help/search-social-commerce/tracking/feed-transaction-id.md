---
title: Tracciamento delle conversioni tramite un feed ID transazione
description: Scopri come utilizzare un feed ID transazione per i dati di tracciamento della conversione.
exl-id: 3341ac20-d435-4387-99da-7b874e53c2e7
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---

# Tracciamento delle conversioni tramite un feed ID transazione

Quando un inserzionista ha transazioni sia online che offline, può tenere traccia delle transazioni online tramite il pixel di tracciamento della conversione di Adobe Advertising Adobi Advertising e può tenere traccia delle transazioni offline utilizzando un ID transazione e consegnarle tramite un feed:

* Per le transazioni online, Adobe Advertising tiene traccia dei clic sugli annunci e delle transazioni risultanti sul sito Web.

* L&#39;inserzionista deve tenere traccia delle conversioni offline e inviare ad Adobe Advertising i file di feed a livello di transazione.

## Panoramica sull’implementazione

*Solo i ruoli di amministratore, responsabile account di [!DNL Adobe] e amministratore*

1. Utilizza le opzioni di tracciamento account o campagna &quot;[!UICONTROL EF Redirect]&quot; e &quot;[!UICONTROL Auto Upload]&quot; per generare automaticamente un URL di destinazione o finale per ogni parola chiave (per il tracciamento a livello di parola chiave) o annuncio (per il tracciamento a livello di annuncio) nell&#39;account o nella campagna.

1. Imposta il tracciamento delle conversioni di Adobe Advertising per le conversioni online. Questa procedura è la stessa utilizzata per gli inserzionisti con tracciamento delle conversioni basato su pixel di Adobe Advertising. È importante generare tag di conversione che includano un parametro per un ID transazione univoco (`ev_transid=<transid>`).

1. Per la parte offline di ciascuna transazione, l&#39;inserzionista genera lo stesso ID transazione utilizzato nella parte online della transazione da includere nel file di feed.

1. L&#39;inserzionista carica un file con i [dati di conversione richiesti](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md) nel percorso del server designato.

1. Technical Services analizza i dati di conversione nei file caricati, quindi carica i dati in Adobe Advertising. Adobe Advertising tiene traccia dei dati rispetto a singole parole chiave, annunci e posizionamenti e crea una previsione dei ricavi per ciascuno di essi.

1. I servizi tecnici convalidano i dati elaborati in base ai dati del feed e verificano la presenza di [transazioni orfane](/help/search-social-commerce/glossary.md#o-p).

>[!MORELIKETHIS]
>
>* [Requisiti dei file per i file del feed di conversione](feed-file-requirements.md)
>* [Requisiti dei dati per i feed di dati che utilizzano un ID transazione](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md)
