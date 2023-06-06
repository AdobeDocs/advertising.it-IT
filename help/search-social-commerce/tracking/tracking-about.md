---
title: Informazioni sul tracciamento per Ricerca, Social e Commerce
description: Scopri le opzioni di tracciamento per Search, Social e Commerce.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 0%

---

# Informazioni sul tracciamento per Ricerca, Social e Commerce

Per tenere traccia delle prestazioni degli annunci, cerca i dati sulle esigenze di Search, Social e Commerce (transazione), clic, costo e conversione per gli annunci. Search, Social e Commerce utilizza questi dati per creare i modelli di previsione dei dati necessari per ottimizzare i portfolio di annunci.

## Dati su costi, clic e impression

Search, Social e Commerce recupera i dati su impression, clic e costi direttamente da [reti pubblicitarie supportate](/help/search-social-commerce/introduction/supported-inventory.md) ogni giorno. Inoltre, Search, Social e Commerce possono aggiungere nei modelli di tracciamento e negli URL di destinazione un codice di tracciamento dei clic univoco (che include un reindirizzamento a un server di tracciamento) per monitorare impression, clic e costi di visualizzazione/contenuto e per collegare successivamente gli eventi alle conversioni.

Se desideri tenere traccia delle campagne su reti pubblicitarie con cui Search, Social e Commerce non sincronizza i dati, devi fornire i dati per tali campagne inviando un file di feed giornaliero con i dati su impression, clic e costo.

### Tag di tracciamento dei clic

Il team di implementazione di Search, Social &amp; Commerce configura il tracciamento dei clic aggiornando i modelli di tracciamento e gli URL di destinazione per annunci, parole chiave, posizionamenti, gruppi di prodotti ed estensioni sitelink nelle campagne pubblicitarie sincronizzate, in modo da includere una stringa ID di tracciamento univoca e un Adobe di reindirizzamento Advertising. Aggiungono inoltre il tracciamento ai suffissi della pagina principale (suffissi URL finali) per il tuo [!DNL Google Ads] e [!DNL Microsoft Advertising] account e campagne.

I parametri di tracciamento consentono ad Adobe Advertising di tenere traccia dei clic a livello di singola parola chiave (campagne di ricerca) o a livello di variante dell’annuncio (campagne di ricerca con targeting di contenuto o sito, campagne di visualizzazione e campagne social). Ogni volta che un utente visualizza un annuncio di visualizzazione/contenuto o fa clic su uno degli annunci, la rete di annunci invia l’evento ai pixel server di Advertising Adobe utilizzando un tag di tracciamento dei clic associato alla parola chiave o all’annuncio. Per i clic:

* Per gli annunci Google Ads e Microsoft Advertising sui browser che supportano il tracciamento parallelo, la rete di annunci invia prima il clic al sito web e poi agli Adobi pixel server di Advertising, che quindi inseriscono un cookie sul computer dell’utente, se non ne esiste già uno.

* In tutti gli altri casi, la rete pubblicitaria invia il clic direttamente ai pixel server di Adobe Advertising. Il pixel server inserisce un cookie nel computer dell’utente (se non ne esiste già uno) e quindi reindirizza l’utente all’URL appropriato sul sito web. L’esperienza complessiva per l’utente finale è la stessa che si avrebbe senza un reindirizzamento.

Il cookie è impostato in [!DNL Adobe] dominio (`everesttech.net`) come cookie di prime parti. Dopo un reindirizzamento, l’utente si trova nel dominio dell’inserzionista e il cookie viene quindi trattato come un cookie di terze parti. Per ulteriori informazioni sui cookie di Adobe Advertising, consulta la sezione &quot;[Cookie di Adobe Advertising](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-advertising-cloud.html).&quot;

## Dati di conversione

Quando un cliente fa clic su un annuncio o visualizza un annuncio di visualizzazione o social, Search, Social e Commerce deve mappare ogni conversione risultante sul clic o sulla visualizzazione o sull’impression social di origine.

L’inserzionista svolge un ruolo nella fornitura dei dati di conversione per tutti i clic e le impression display/social. I dati di conversione possono includere informazioni su qualsiasi tipo di evento che si verifica su un sito web e che può essere utilizzato per l’ottimizzazione delle offerte. Puoi fornire i dati di conversione implementando il codice di tracciamento della conversione nelle pagine di conversione dell’inserzionista (ad esempio la pagina &quot;operazione riuscita&quot; visualizzata dopo che un cliente ha completato una transazione) o inviando un file di feed giornaliero con dati di conversione acquisiti da un altro metodo.

### Tag di tracciamento delle conversioni

È possibile utilizzare [tag di conversione di vari fornitori](/help/search-social-commerce/tracking/conversion-tracking-about.md).

Quando utilizzi un tag di conversione Adobe Advertising e un utente completa una transazione riuscita e arriva a una pagina di &quot;successo&quot;, il server pixel di Adobe Advertising controlla l’esistenza del cookie sul computer dell’utente, impostato al momento del reindirizzamento del clic. Quando trova un cookie, le informazioni sull’evento della transazione vengono trasmesse utilizzando il parametro ef_transid e la transazione viene riconosciuta come conversione e accreditata all’impression di clic o visualizzazione precedente.

Se l’utente ha fatto clic su più annunci, Adobe Advertising attribuisce la transazione al clic finale dell’annuncio o (per campagne display o video) all’impression finale dell’annuncio, a meno che non venga specificato diversamente. Il tuo [fai clic sull’intervallo di lookback](/help/search-social-commerce/glossary.md#c-d) e [intervallo di lookback delle impression](/help/search-social-commerce/glossary.md#i-j) determina il numero di giorni dopo i quali si verifica un clic a pagamento o un’impression display/video (rispettivamente) in cui l’evento può essere attribuito a una conversione.

Il team di implementazione di Adobe Advertising collabora con l’inserzionista per determinare il formato dei tag di conversione che l’inserzionista deve implementare, identificare le pagine web in cui ogni tag di conversione deve essere inserito e quindi fornire i tag di conversione da implementare.