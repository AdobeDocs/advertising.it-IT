---
title: Informazioni sulle librerie creative
description: Scopri come gestire i creativi delle esperienze pubblicitarie.
feature: Creative Libraries, Creative Standard Creatives, Creative Dynamic Creatives
exl-id: 77dc6528-a455-4406-98b6-15e7ce529370
source-git-commit: 076dd97944b5cb74f24bee85602e3743bba16f7b
workflow-type: tm+mt
source-wordcount: '1059'
ht-degree: 0%

---

# Informazioni sulle librerie creative

*Funzione beta chiusa*

Le librerie creative ti consentono di gestire i contenuti creativi da utilizzare nelle esperienze pubblicitarie. Puoi creare più librerie, ciascuna con un set di creatività e *bundle creativi*, che sono gruppi di creatività che puoi aggiungere a un&#39;esperienza come un&#39;unica unità.

Le librerie possono includere:

* **Singoli creativi:** Puoi includere singoli creativi direttamente all&#39;interno di esperienze pubblicitarie che non hanno target utente definiti. Puoi anche utilizzare i tuoi creativi per creare bundle, che puoi includere in [esperienze annuncio](/help/creative/experiences/experience-about.md) mirate.

   * **Creative standard:** Puoi caricare e gestire creative in [vari formati](#creative-creative-formats). Per ogni contenuto creativo si specifica la lingua predefinita per ogni annuncio a cui si associa il contenuto creativo, la pagina di destinazione predefinita che si apre quando un utente fa clic su un annuncio che include il contenuto creativo e le etichette facoltative da utilizzare come filtri nelle varie visualizzazioni di [!DNL Creative].

   * **Creative dinamiche:** (solo per clienti Adobe Advertising DCO esistenti) Gli utenti amministratori possono creare creative generate dinamicamente mappando le variabili dinamiche in un modello di annuncio ai valori in un file di feed. Tutti gli utenti possono visualizzare in anteprima, duplicare ed eliminare gli annunci dinamici esistenti.

* **Pacchetti creatività:** raggruppa i creativi in bundle da utilizzare in più esperienze con target utente definiti. Puoi creare *bundle standard* costituiti da annunci standard e *bundle dinamici* costituiti da annunci generati dinamicamente.

## Formati Creative supportati {#creative-creative-formats}

### Formati per creatività standard

Puoi aggiungere e gestire i seguenti tipi di creatività nelle [dimensioni di creatività supportate](creative-sizes.md).

>[!IMPORTANT]
>
>Anche se si intende utilizzare HTML5, HTML5 flessibile o creativi di terze parti per le esperienze pubblicitarie, è necessario aggiungere anche creativi di immagini per ogni dimensione creativa utilizzata.
>
>Ogni esperienza richiede una creatività di immagine predefinita per ogni dimensione creativa assegnata all’esperienza. Le immagini creative predefinite vengono utilizzate quando un browser non è abilitato per JavaScript o quando l’ad server non può personalizzare l’annuncio a causa di ritardi.

#### HTML5 flessibile

I creativi HTML5 flessibili sono creativi HTML5 con tutte le immagini e altri attributi come tag HTML standard, che è possibile modificare direttamente in [!DNL Creative], sia all&#39;interno di una libreria creativa che all&#39;interno di una singola esperienza (che crea una variazione della creatività originale). I creativi HTML5 flessibili utilizzano lo standard del laboratorio della tecnologia Interactive Advertising Bureau (IAB) per un [portfolio di annunci](https://flexibleads.iabtechlab.com/), per il quale le dimensioni degli annunci sono flessibili (anziché fisse) e si basano sulle proporzioni e sull&#39;intervallo di dimensioni dell&#39;annuncio e per il quale gli annunci mantengono la loro risoluzione tra i dispositivi e i siti di pubblicazione.

È possibile <!-- either --> caricare creative HTML5 flessibili come file ZIP<!-- or use one of the [provided templates](flexible-html5-templates.md) as a starting point -->. Consulta le [specifiche per le creatività flessibili di HTML5](html5-creative-specification.md).

<!-- Will flattening the view be possible later?
The card view, by default, includes a card for each base flexible HTML5 creative you've uploaded, with the number of creative variations [Delete old description? : an indicator of how many variations of the creative exist]. You can optionally flatten the card view to include separate cards for each base creative and each derivation. The table view is always flattened.


[Example default card view for a flexible creative with variations]()[]add image]
  
[Example card for a flexible creative with one variation]() [add image]

 -->

Facoltativamente, è possibile modificare i valori predefiniti degli attributi specificati in una creatività flessibile di HTML5. In seguito, puoi specificare valori personalizzati per gli attributi all’interno di un’esperienza specifica, creando una variante della creatività principale.

#### Creatività di HTML5

È possibile caricare creative HTML5 semplici o statiche, con tutti gli attributi e le immagini specificati, come file ZIP. Non è possibile modificare attributi o aggiungere immagini, ma caricare un nuovo file ZIP per aggiungere una nuova creatività. Consulta le [specifiche per creative HTML5 semplici e statiche](html5-creative-specification.md).

#### Creatività delle immagini

Puoi includere creativi di immagini in formato GIF, JPEG, JPG o PNG. È possibile caricare <!--LATER:   images from your Adobe Experience Manager accounts or --> immagini dal dispositivo o dalla rete.

Ogni esperienza pubblicitaria richiede una creatività di immagine predefinita per ogni dimensione creativa assegnata all’esperienza.

#### Creatività di terze parti

Immetti i tag di tracciamento di JavaScript per i creativi in hosting su server di annunci di terze parti. Lo script varia in base al server di annunci; di seguito è riportato un esempio:

```
<SCRIPT language='JavaScript1.1' SRC="https://ad.doubleclick.net/ddm/adj/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp];dc_lat=;dc_rdid=;tag_for_child_directed_treatment=?"></SCRIPT> <NOSCRIPT> <A HREF="https://ad.doubleclick.net/ddm/jump/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp]?"><IMG SRC="https://ad.doubleclick.net/ddm/ad/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp];dc_lat=;dc_rdid=;tag_for_child_directed_treatment=?"BORDER=0 WIDTH=300 HEIGHT=250 ALT="Advertisement"></A></NOSCRIPT>
```

### Formato per annunci dinamici

Gli utenti amministratori possono generare dinamicamente creatività in formato HTML5 statico e HTML5 dinamico mappando le variabili dinamiche in un modello di annuncio ai valori in un file di feed. I contenuti creativi dinamici possono includere quelli delle precedenti esperienze Adobe Advertising Dynamic Creative Optimization (DCO).

## Le visualizzazioni [!UICONTROL Creative Libraries]

Per ulteriori informazioni sulla personalizzazione di ogni visualizzazione, vedere &quot;[Personalizza le visualizzazioni dati](/help/creative/introduction/customize-data-views.md)&quot;.

### Visualizzazione principale di [!UICONTROL Creative Libraries]

La visualizzazione principale di [!UICONTROL Creative Libraries] mostra tutte le librerie creative. I dati di ciascuna libreria includono il numero di esperienze a cui vengono assegnati i bundle della libreria, il numero di bundle, il numero di creativi, il numero di dimensioni di creatività, il numero di destinazioni della lingua predefinite, la data di creazione e la data dell’ultima modifica di qualsiasi elemento della libreria. La modalità tabella include anche una colonna per l’inserzionista.

#### Azioni disponibili

* Creare nuove librerie

* Per ogni libreria creativa:

   * Modifica il nome della libreria

   * Apri la libreria per visualizzare le creatività e i bundle assegnati alla libreria

   * Eliminare la libreria

### Visualizzazioni [!UICONTROL Creative Libraries] > [!UICONTROL Creatives]

#### [!UICONTROL Standard Ads]

La scheda [!UICONTROL Standard Ads] mostra tutte le creatività standard create dall&#39;utente. I dati per ogni creatività includono la dimensione della creatività, il tipo di creatività e la data di creazione. La modalità tabella include anche le colonne per la lingua predefinita e la pagina di destinazione predefinita.

##### Azioni disponibili

* [Aggiungere creatività standard a una libreria](creative-add-standard.md)

* [Modificare un contenuto creativo standard](creative-edit-standard.md)

* [Visualizzare l’anteprima di un contenuto creativo standard](creative-preview.md)

* [Aggiungere creatività standard ai bundle standard e rimuovere le creatività standard da un bundle standard](creative-attach-detach-bundles.md)

* [Duplicare le creatività standard](creative-duplicate.md)

* [Scarica creatività standard](creative-download.md)

* [Elimina creatività standard](creative-delete.md)

<!-- Add in as separate actions?

add or remove labels, regenerate thumbnails for your creatives. When a creative has child creative variations, you can view the variations within the Card view.

-->

#### [!UICONTROL Dynamic Ads]

La scheda [!UICONTROL Dynamic Ads] mostra tutte le creatività dinamiche create dinamicamente per i cataloghi creativi, ad eccezione delle creatività dinamiche [eliminate manualmente](creative-delete.md) dalla scheda [!UICONTROL Dynamic Ads]. Se [hai duplicato manualmente](creative-duplicate.md) le creatività dinamiche dall&#39;ultima elaborazione di un catalogo, l&#39;elenco delle creatività per tale catalogo include anche le creatività duplicate.

I dati per ogni creatività includono il tipo di creatività, la dimensione della creatività, il numero di cataloghi a cui appartiene la creatività e la data di creazione. La modalità tabella include anche le colonne per il modello attraverso il quale è stata generata la creatività e il conteggio delle offerte.

>[!NOTE]
>
>Ogni volta che un catalogo viene elaborato, i dati vengono aggiornati per le creatività dinamiche esistenti per tale catalogo.

##### Azioni disponibili

La possibilità di creare e modificare contenuti creativi dinamici è attualmente disponibile solo per l’Account Team di Adobe. Tuttavia, tutti gli utenti possono:

* [Anteprima di elementi creativi dinamici](creative-preview.md)

* [Aggiungere creatività dinamica ai bundle dinamici e rimuovere creatività dinamica da un bundle dinamico](creative-attach-detach-bundles.md)

* [Duplicare elementi creativi dinamici](creative-duplicate.md)

* [Eliminare le creatività dinamiche](creative-delete.md)

<!-- Later:  Dynamic creatives are generated automatically when you save a catalog, but can regenerate the catalog using the contents of an updated asset file [using the Run Now option]. -->

### Visualizzazione [!UICONTROL Creative Libraries] > [!UICONTROL Bundles]

La visualizzazione [!UICONTROL Bundles] mostra tutti i contenitori di bundle standard e dinamici. Puoi vedere i nomi creativi, le dimensioni creative e i linguaggi dei creativi inclusi in ogni pacchetto.

#### Azioni disponibili

* Aggiungere bundle standard e dinamici a una libreria

* Elencare e visualizzare in anteprima i creativi in un bundle

* Modificare un nome bundle

* Aggiungere creatività standard ai bundle standard e rimuovere le creatività standard da un bundle standard

* Bundle duplicati

* Elimina bundle

>[!MORELIKETHIS]
>
>* [Gestisci librerie creative](/help/creative/creative-libraries/creative-library-manage.md)
>* [Aggiungere creatività standard a una libreria creativa](creative-add-standard.md)
>* [Gestione dei bundle creativi](bundle-manage.md)
>* [Personalizza le visualizzazioni dati](/help/creative/introduction/customize-data-views.md)
