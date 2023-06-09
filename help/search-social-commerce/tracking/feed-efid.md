---
title: Tracciamento delle conversioni tramite un feed EF ID
description: Scopri come utilizzare un feed EF ID per i dati di tracciamento della conversione.
source-git-commit: 46e918418bf2e5c412efa8825dda22bc1953e439
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 0%

---

# Tracciamento delle conversioni tramite un feed EF ID

Con questo metodo, Advertising Cloud raccoglie un `ef_id` ogni volta che un utente fa clic su e un annuncio e arriva alla pagina di destinazione, e l’inserzionista memorizza il `ef_id` con i dati di conversione e li invia in un feed di dati.

## Panoramica sull’implementazione

*Account manager dell’agenzia, [!DNL Adobe] solo ruoli utente amministratore e responsabile account*

1. Utilizza le opzioni di tracciamento account o campagna &quot;[!UICONTROL EF Redirect],&quot; tipo di reindirizzamento di &quot;[!UICONTROL Token],&quot; e &quot;[!UICONTROL Auto Upload]&quot; per generare automaticamente un URL di destinazione o finale con un token di Adobe Advertising (ef_id) per ogni parola chiave (per il tracciamento a livello di parola chiave) o annuncio (per il tracciamento a livello di annuncio) nell’account o nella campagna.

   >[!NOTE]
   >* Questo metodo non richiede all’inserzionista di utilizzare tag di tracciamento delle conversioni di Adobe Advertising.
   >* Se cambi il tipo di reindirizzamento per un account o una campagna esistente da [!UICONTROL Standard] a [!UICONTROL Token], o viceversa, devi rigenerare tutti gli URL di tracciamento applicabili.

   L’ef_id viene popolato e aggiunto all’URL della pagina di destinazione quando l’utente finale fa clic sull’annuncio e viene reindirizzato a un server di Adobe Advertising. L’ef_id viene quindi trasmesso all’inserzionista nell’URL di destinazione o nell’URL finale dell’annuncio o della parola chiave. Di seguito è riportato un esempio di URL di destinazione passato all&#39;inserzionista durante il reindirizzamento:

   `http://pixel.everesttech.net/1180/cq?ev_sid=3&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx=&ev_pl={placement}&url=http%3A//www.example.com&ef_id=D59Nu0u@BD0AAM1q:20110630172936:s`

1. L’inserzionista estrae l’ef_id dal reindirizzamento e lo memorizza con i dati di conversione rilevanti da includere nel file di feed. Non modificare il ef_id e non modificare le maiuscole/minuscole.

1. (Facoltativo ma consigliato) L’inserzionista può creare un ID transazione univoco per ogni transazione da includere nel file di feed.

1. L’inserzionista carica un file con [dati di conversione richiesti](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md) nel percorso del server designato.

1. Technical Services analizza i dati di conversione nei file caricati, quindi carica i dati in Adobe Advertising. Adobe Advertising tiene traccia dei dati rispetto a singole parole chiave, annunci e posizionamenti e crea una previsione dei ricavi per ciascuno di essi.

1. I servizi tecnici convalidano i dati elaborati in base ai dati del feed e verificano eventuali [transazioni orfane](/help/search-social-commerce/glossary.md#o-p).

>[!MORELIKETHIS]
>
>* [Requisiti dei file per i file di feed di conversione](feed-file-requirements.md)
>* [Requisiti in materia di dati per i feed di dati che utilizzano ID EF](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md)


