---
title: Informazioni sul tracciamento per Search, Social e Commerce
description: Scopri le opzioni di tracciamento per Search, Social e Commerce.
exl-id: f0fd367a-dd5a-46ec-a3d6-9b491860aae8
feature: Search Tracking
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '756'
ht-degree: 0%

---

# Informazioni sul tracciamento per Search, Social e Commerce

Per tenere traccia delle prestazioni degli annunci, Search, Social e Commerce necessitano di dati di tipo impression, clic, costo e conversione (transazione) per i tuoi annunci. Search, Social e Commerce utilizzano questi dati per creare i modelli di previsione dei dati necessari per ottimizzare i portfolio di annunci.

## Dati su costi, clic e impression

Search, Social e Commerce recuperano ogni giorno i dati su impression, clic e costi direttamente dalle [reti di annunci supportate](/help/search-social-commerce/introduction/supported-inventory.md). Inoltre, Search, Social e Commerce possono aggiungere nei modelli di tracciamento e negli URL di destinazione un codice di tracciamento dei clic univoco (che include un reindirizzamento a un server di tracciamento) per monitorare impression, clic e costi della visualizzazione o del contenuto e per collegare successivamente gli eventi alle conversioni.

Se desideri tenere traccia delle campagne su reti pubblicitarie con cui Search, Social e Commerce non sincronizzano i dati, devi fornire i dati per tali campagne inviando un file di feed giornaliero con i dati su impression, clic e costo.

### Tag di tracciamento dei clic

Il team di implementazione di Search, Social e Commerce configura il tracciamento dei clic aggiornando i modelli di tracciamento e gli URL di destinazione per annunci, parole chiave, posizionamenti, gruppi di prodotti ed estensioni sitelink nelle campagne pubblicitarie sincronizzate, in modo da includere una stringa di ID tracciamento univoca e un Adobe Advertising di reindirizzamento. Aggiungono inoltre il tracciamento ai suffissi della pagina Web (suffissi URL finali) per gli account e le campagne [!DNL Google Ads] e [!DNL Microsoft Advertising].

I parametri di tracciamento consentono all’Adobe Advertising di tenere traccia dei clic a livello di singola parola chiave (campagne di ricerca) o a livello di variante dell’annuncio (campagne di ricerca con targeting di contenuto o sito, campagne di visualizzazione e campagne social). Ogni volta che un utente visualizza un annuncio di visualizzazione/contenuto o fa clic su uno degli annunci, la rete di annunci invia l’evento ai server pixel Adobi Advertising utilizzando un tag di tracciamento dei clic associato alla parola chiave o all’annuncio. Per i clic:

* Per gli annunci di [!DNL Google Ads] e [!DNL Microsoft Advertising] nei browser che supportano il tracciamento parallelo, la rete di annunci invia prima il clic al sito Web e quindi ai server pixel Adobi Advertising, che inseriscono quindi un cookie nel computer dell&#39;utente, se non ne esiste già uno.

* In tutti gli altri casi, la rete pubblicitaria invia il clic direttamente ai server pixel Adobi Advertising. Il pixel server inserisce un cookie nel computer dell’utente (se non ne esiste già uno) e quindi reindirizza l’utente all’URL appropriato sul sito web. L’esperienza complessiva per l’utente finale è la stessa che si avrebbe senza un reindirizzamento.

Il cookie è impostato nel dominio [!DNL Adobe] (`everesttech.net`) come cookie di prime parti. Dopo un reindirizzamento, l’utente si trova nel dominio dell’inserzionista e il cookie viene quindi trattato come un cookie di terze parti. Per ulteriori informazioni sui cookie Adobe Advertising, vedere &quot;[Cookie Adobe Advertising](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-advertising-cloud.html?lang=it).&quot;

## Dati di conversione

Quando un cliente fa clic su un annuncio o visualizza un annuncio di visualizzazione o social, Search, Social e Commerce devono mappare ogni conversione risultante sul clic o sulla visualizzazione o sull’impression social di origine.

L’inserzionista svolge un ruolo nella fornitura dei dati di conversione per tutti i clic e le impression display/social. I dati di conversione possono includere informazioni su qualsiasi tipo di evento che si verifica su un sito web e che può essere utilizzato per l’ottimizzazione delle offerte. Puoi fornire i dati di conversione implementando il codice di tracciamento della conversione nelle pagine di conversione dell’inserzionista (ad esempio la pagina &quot;operazione riuscita&quot; visualizzata dopo che un cliente ha completato una transazione) o inviando un file di feed giornaliero con dati di conversione acquisiti da un altro metodo.

### Tag di tracciamento delle conversioni

Puoi utilizzare [tag di conversione di vari fornitori](/help/search-social-commerce/tracking/conversion-tracking-about.md).

Quando utilizzi un tag di conversione di Adobe Advertising e un utente completa una transazione riuscita e arriva a una pagina &quot;riuscita&quot;, il server pixel di Adobe Advertising controlla l’esistenza del cookie sul computer dell’utente, impostato al momento del reindirizzamento del clic. Quando trova un cookie, le informazioni sull’evento della transazione vengono trasmesse utilizzando il parametro ef_transid e la transazione viene riconosciuta come conversione e accreditata all’impression di clic o visualizzazione precedente.

Se l’utente ha fatto clic su più annunci, Adobe Advertising attribuisce la transazione al clic finale dell’annuncio o (per campagne di visualizzazione o video) all’impression finale dell’annuncio, a meno che non venga specificato diversamente. L&#39;[intervallo di lookback su clic](/help/search-social-commerce/glossary.md#c-d) e l&#39;[intervallo di lookback su impression](/help/search-social-commerce/glossary.md#i-j) determinano il numero di giorni dopo i clic a pagamento o le impression (rispettivamente) di visualizzazione o video in cui l&#39;evento può essere attribuito a una conversione.

Il team di implementazione di Adobe Advertising collabora con l’inserzionista per determinare il formato dei tag di conversione che l’inserzionista deve implementare, identificare le pagine web in cui ogni tag di conversione deve essere inserito e quindi fornire i tag di conversione da implementare.
