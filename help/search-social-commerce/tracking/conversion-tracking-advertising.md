---
title: Informazioni sui tag di tracciamento delle conversioni di Adobe Advertising
description: Scopri come utilizzare gli Adobi Advertising di tag per il tracciamento delle conversioni.
exl-id: 8194d5eb-9a5d-4c4e-bb02-e578ffb84d18
feature: Search Tracking
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 0%

---

# Informazioni sui tag di tracciamento delle conversioni di Adobe Advertising

Adobe Advertising tiene traccia delle conversioni risultanti dai clic sugli annunci utilizzando i tag di tracciamento delle conversioni di Adobe Advertising inseriti nelle pagine web che si aprono quando si verifica un evento di conversione, ad esempio una pagina di &quot;successo&quot;. I tag includono informazioni incorporate per inviare i dati della transazione, insieme al cookie di Adobe Advertising dell’utente, a un server di tracciamento, dal quale la transazione viene accreditata al clic o all’impression dell’annuncio appropriato (in base alle impostazioni di attribuzione di conversione dell’inserzionista).

>[!NOTE]
>
>Se l’utente non dispone di un cookie valido, Adobe Advertising non segnala la conversione.

Per ogni set di metriche di conversione di cui desideri tenere traccia, devi creare un tag di conversione separato. Fornisci i tag all’inserzionista o all’agenzia con un elenco di pagine web in cui inserirle. Puoi generare uno dei seguenti tipi di tag di conversione. Per istruzioni, vedere &quot;[Generare un tag di conversione Adobe Advertising](/help/search-social-commerce/tools/conversion-tag-generate.md)&quot;.

* (Consigliato) Tag JavaScript (versione 3 o versione 2), che non sono visibili nelle pagine web.

* HTML tag immagine per visualizzare sulle pagine Web immagini trasparenti (pixel) da 1 pixel x 1 pixel, invisibili agli utenti finali. Utilizza i tag immagine solo quando l’azienda non può utilizzare i tag JavaScript in base a una policy.

Per ulteriori informazioni sulle differenze tra i tipi di tag, consulta &quot;[Domande frequenti sui tag di tracciamento delle conversioni di Advertising Cloud](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).&quot;

>[!NOTE]
>
>* Questa funzione non aggiunge tag immagine o JavaScript alle pagine Web dell’inserzionista. I tag devono essere aggiunti in base alla normale procedura dell’inserzionista per l’aggiornamento delle pagine web.
>* Assicurati di considerare il tempo necessario per implementare i tag. A seconda delle politiche aziendali, l&#39;implementazione può richiedere settimane o anche mesi.

## Caratteristiche degli Adobi Advertising di tag per il tracciamento delle conversioni

Il pixel di tracciamento della conversione consente ad Adobe Advertising di effettuare le seguenti operazioni:

* Tieni traccia e segnala i dati di conversione a livello di parola chiave per le campagne di ricerca.

* Monitora e genera rapporti sui dati di conversione a livello di annuncio (creativo) in tutti i canali di marketing (ricerca e visualizzazione a pagamento), facilitando così il test creativo.

* Monitora e segnala i dati di conversione a livello di transazione in tutti i canali di marketing.

* Mostra in che modo le conversioni sono distribuite tra i diversi canali di marketing, in modo da vedere quale è più efficace.

* Generare rapporti e ottimizzarli a diversi livelli di attribuzione (ad esempio, attribuire le conversioni all’ultimo evento correlato o ponderare tutti gli eventi in modo uniforme).

* Fornisci visibilità sugli assistenti di clic (parole chiave di ricerca o posizionamenti che hanno contribuito a un funnel di conversione) e sugli assistenti di canale (eventi utente che hanno contribuito a un funnel di conversione, eventualmente su più canali di marketing).

* Fornisci visibilità nella distribuzione geografica e nei domini di riferimento del traffico del sito e delle conversioni in modo da poter perfezionare il targeting geografico e del sito web.

* Analizza le tendenze giornaliere o infragiornaliere, che possono essere utilizzate per migliorare i tassi di conversione.

>[!MORELIKETHIS]
>
>* [Opzioni di tracciamento delle conversioni](conversion-tracking-about.md)
>* [Genera un tag di conversione Adobe Advertising](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Formato dei tag di tracciamento conversione di JavaScript versione 3](format-conversion-tag-jsv3.md)
>* [Formato dei tag di tracciamento conversione di JavaScript versione 2](format-conversion-tag-jsv2.md)
>* [Formato dei tag di tracciamento conversione immagine](format-conversion-tag-image.md)
>* [Domande frequenti sui tag di conversione e di tracciamento della visualizzazione della pagina](faqs-conversion-page-view-tracking-tags.md)
>* [Adobe Advertising tag di mappatura conversione JavaScript](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)
