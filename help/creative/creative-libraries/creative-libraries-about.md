---
title: Informazioni sulle librerie creative
description: Scopri come gestire i creativi delle esperienze pubblicitarie.
feature: Creative Libraries, Creative Standard Creatives, Creative Dynamic Creatives
exl-id: 77dc6528-a455-4406-98b6-15e7ce529370
source-git-commit: 2d794d0c4e6ce708412742f6ba6178b61116b41d
workflow-type: tm+mt
source-wordcount: '1409'
ht-degree: 0%

---

# Informazioni sulle librerie creative

*Funzione beta chiusa*

Le librerie creative ti consentono di gestire i contenuti creativi da utilizzare nelle esperienze pubblicitarie. Puoi creare più librerie, ciascuna con un set di creatività e *bundle creativi*, che sono gruppi di creatività che puoi aggiungere a un&#39;esperienza come un&#39;unica unità.

Le librerie possono includere:

* **Singoli creativi:** Puoi includere singoli creativi direttamente all&#39;interno di esperienze pubblicitarie che non hanno target utente definiti. Puoi anche utilizzare i tuoi creativi per creare bundle, che puoi includere in [esperienze annuncio](/help/creative/experiences/experience-about.md) mirate.

   * **Creative standard:** Puoi caricare e gestire creative in [vari formati](#creative-creative-formats). Per ogni contenuto creativo, specifica la lingua predefinita per ogni annuncio a cui associ il contenuto creativo e la pagina di destinazione predefinita che si apre quando un utente fa clic su un annuncio che include il contenuto creativo. Facoltativamente, è possibile specificare le etichette da utilizzare come filtri in varie visualizzazioni all&#39;interno di [!DNL Creative] e come valori di colonna in [!UICONTROL Custom Creative Report] quando si include l&#39;utilizzo della dimensione [!UICONTROL Creative Label].

   * **Creative dinamiche:** (solo per clienti Adobe Advertising DCO esistenti) Gli utenti amministratori possono creare creative generate dinamicamente mappando le variabili dinamiche in un modello di annuncio ai valori in un file di feed. Tutti gli utenti possono visualizzare in anteprima, duplicare ed eliminare gli annunci dinamici esistenti.

* **Pacchetti creatività:** raggruppa i creativi in bundle da utilizzare in più esperienze con target utente definiti. Puoi creare *bundle di visualizzazione standard* costituiti da annunci di visualizzazione standard, *bundle video standard* costituiti da annunci video standard e *bundle di visualizzazione dinamici* costituiti da annunci di visualizzazione generati dinamicamente.

## Formati Creative supportati {#creative-creative-formats}

### Formati per creatività standard

Puoi aggiungere e gestire i seguenti tipi di creatività nelle [dimensioni di creatività supportate](creative-sizes.md).

>[!IMPORTANT]
>
>* Anche se si intende utilizzare HTML5, HTML5 flessibile o creativi di terze parti per le esperienze di visualizzazione standard, è necessario aggiungere anche creativi di immagini per ogni dimensione creativa utilizzata.
>* Ogni esperienza di visualizzazione standard richiede una creatività di immagine predefinita per ogni dimensione creativa assegnata all’esperienza. Le immagini creative predefinite vengono utilizzate quando un browser non è abilitato per JavaScript o quando l’ad server non può personalizzare l’annuncio a causa di ritardi.
>* Ogni esperienza video standard richiede una creatività video predefinita per ogni durata creativa assegnata all&#39;esperienza.<!-- when is it used? -->

#### HTML5 flessibile

I creativi HTML5 flessibili sono creativi HTML5 con tutte le immagini e altri attributi come tag HTML standard, che è possibile modificare direttamente in [!DNL Creative], sia all&#39;interno di una libreria creativa che all&#39;interno di una singola esperienza (che crea una variazione della creatività originale). In DSP, i creativi flessibili di HTML5 sono per una singola dimensione di annuncio specifica (in pixel). Facoltativamente, è possibile modificare i valori predefiniti degli attributi specificati in una creatività flessibile di HTML5. In seguito, puoi specificare valori personalizzati per gli attributi all’interno di un’esperienza specifica, creando una variante della creatività principale.

Puoi caricare creativi flessibili HTML5 come file ZIP o utilizzare uno dei modelli disponibili per il tuo account come punto di partenza. Consulta le [specifiche per le creatività flessibili di HTML5](html5-creative-specification.md).

#### Creatività di HTML5

È possibile caricare creative HTML5 semplici o statiche, con tutti gli attributi e le immagini specificati, come file ZIP. Non è possibile modificare attributi o aggiungere immagini, ma caricare un nuovo file ZIP per aggiungere una nuova creatività. Consulta le [specifiche per creative HTML5 semplici e statiche](html5-creative-specification.md).

#### Creatività delle immagini

Puoi includere creativi di immagini in formato GIF, JPEG, JPG o PNG. Puoi caricare immagini approvate dagli account Adobe Experience Manager o immagini dal dispositivo o dalla rete.

Ogni esperienza di visualizzazione e annuncio standard richiede una creatività di immagine predefinita per ogni dimensione creativa assegnata all’esperienza.

#### Creatività di terze parti

Immetti i tag di tracciamento di JavaScript per i creativi in hosting su server di annunci di terze parti. Lo script varia in base al server di annunci; di seguito è riportato un esempio:

```
<SCRIPT language='JavaScript1.1' SRC="https://ad.doubleclick.net/ddm/adj/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp];dc_lat=;dc_rdid=;tag_for_child_directed_treatment=?"></SCRIPT> <NOSCRIPT> <A HREF="https://ad.doubleclick.net/ddm/jump/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp]?"><IMG SRC="https://ad.doubleclick.net/ddm/ad/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp];dc_lat=;dc_rdid=;tag_for_child_directed_treatment=?"BORDER=0 WIDTH=300 HEIGHT=250 ALT="Advertisement"></A></NOSCRIPT>
```

#### Creativi video {#creative-video-specs}

È possibile caricare creativi video di prime parti per il Web, i dispositivi mobili o la TV connessa dal dispositivo o dalla rete. Ogni esperienza di annuncio video standard richiede una creatività video predefinita per ogni durata creativa assegnata all’esperienza. Tutti i video creativi vengono transcodificati automaticamente da DSP come tag VAST 2.0 per consentirti di visualizzarli in anteprima. In [!UICONTROL Tag Manager], puoi facoltativamente [applicare la transcodifica specifica di DSP](/help/creative/experiences/experience-tag-video-transcoding.md) a qualsiasi tag esperienza annuncio video.

Consulta i seguenti requisiti creativi per il video. **Nota:** per il caricamento di esperienze video in Advertising DSP, vedi anche [Requisiti DSP per Assets video ad alta definizione](https://experienceleague.adobe.com/en/docs/advertising/dsp/campaign-management/ads/ad-specs#requirements-for-high-definition-video-assets), che potrebbero essere più limitati.

**Tipo file:** .mov, .mp4, .webm

**Dimensione file:** massimo di 512 MB

**Proporzioni video:** 16:9, 4:3

**Risoluzione video:** 640x360 per 360p, 1280x720 per 720p, 1920x1080 per 1080p

**Lunghezza video:** massimo di 90 secondi

**Bitrate:** 600-1200 kbps per 360p, 1500-2500 kbps per 720p, 3000-5000+ kbps per 1080p

**Frame rate video:** 23,98 FPS. Possono essere accettati frame rate aggiuntivi in base a requisiti regionali o di pubblicazione

**Codec video:** H.264 (standard di settore), AV1, H.265

**Formato audio:** ACC (standard di settore/MP4), Opus (WebM/AV1)

**Bitrate audio:** 16-512 kbps

**Frequenza di campionamento audio:** 44100-48000 Hz

**Frequenza audio:** 44,1 kHz o 48 kHz

**Altro audio:** il file caricato deve essere non interlacciato, misto e contenere una traccia audio. Potrebbe non essere presente alcun suono, ma nel file video deve essere inclusa una traccia audio.

### Formato per annunci dinamici

Gli utenti amministratori possono generare dinamicamente creatività in formato HTML5 statico e HTML5 dinamico mappando le variabili dinamiche in un modello di annuncio ai valori in un file di feed. I contenuti creativi dinamici possono includere quelli delle precedenti esperienze Adobe Advertising Dynamic Creative Optimization (DCO).

## Le visualizzazioni [!UICONTROL Creative Libraries]

Per ulteriori informazioni sulla personalizzazione di ogni visualizzazione, vedere &quot;[Personalizza le visualizzazioni dati](/help/creative/introduction/customize-data-views.md)&quot;.

### Visualizzazione principale di [!UICONTROL Creative Libraries]

La visualizzazione principale di [!UICONTROL Creative Libraries] mostra tutte le librerie creative. I dati di ciascuna libreria includono il numero di esperienze a cui vengono assegnati i bundle della libreria, il numero di bundle, il numero di creativi, il numero di dimensioni di creatività, il numero di destinazioni della lingua predefinite, la data di creazione e la data dell’ultima modifica di qualsiasi elemento della libreria. La modalità tabella include anche una colonna per l’inserzionista.

Quando sei in modalità scheda, puoi scorrere le immagini in una libreria con più elementi creativi utilizzando i pulsanti &lt; e >.

#### Azioni disponibili

* [Crea una nuova libreria](/help/creative/creative-libraries/creative-library-manage.md#create-a-creative-library)

* Per ogni libreria creativa:

   * [Modificare il nome di una libreria](/help/creative/creative-libraries/creative-library-manage.md#edit-the-name-of-a-creative-library)

   * [Apri una libreria per visualizzare le creatività e i bundle assegnati alla libreria](/help/creative/creative-libraries/creative-library-manage.md#open-a-creative-library)

   * [Elimina librerie](/help/creative/creative-libraries/creative-library-manage.md#delete-creative-libraries)

### Visualizzazioni [!UICONTROL Creative Libraries] > [!UICONTROL Creatives]

#### [!UICONTROL Standard Ads]

La scheda [!UICONTROL Standard Ads] mostra tutte le creatività standard create dall&#39;utente. I dati per ogni creatività includono la dimensione della creatività, il tipo di creatività e la data di creazione. La modalità tabella include anche le colonne per la lingua predefinita e la pagina di destinazione predefinita.

##### Azioni disponibili

* [Aggiungere creatività standard a una libreria](creative-add-standard.md)

* [Modificare un contenuto creativo standard](creative-edit-standard.md)

* [Visualizzare l’anteprima di un contenuto creativo standard](creative-preview.md)

* [Aggiungi creatività standard ai bundle di visualizzazione standard e rimuovi creatività standard da un bundle di visualizzazione standard](creative-attach-detach-bundles.md)

* [Aggiungere creatività video ai bundle video standard e rimuovere creatività video da un bundle video standard](creative-attach-detach-bundles.md)

* [Duplicare le creatività standard](creative-duplicate.md)

* [Scarica creatività standard](creative-download.md)

* [Elimina creatività standard](creative-delete.md)

#### [!UICONTROL Dynamic Ads]

La scheda [!UICONTROL Dynamic Ads] mostra tutte le creatività dinamiche create dinamicamente per i cataloghi creativi, ad eccezione delle creatività dinamiche [eliminate manualmente](creative-delete.md) dalla scheda [!UICONTROL Dynamic Ads]. Se [hai duplicato manualmente](creative-duplicate.md) le creatività dinamiche dall&#39;ultima elaborazione di un catalogo, l&#39;elenco delle creatività per tale catalogo include anche le creatività duplicate.

I dati per ogni creatività includono il tipo di creatività, la dimensione della creatività, il numero di cataloghi a cui appartiene la creatività e la data di creazione. La modalità tabella include anche le colonne per il modello attraverso il quale è stata generata la creatività e il conteggio delle offerte.

>[!NOTE]
>
>Ogni volta che un catalogo viene elaborato, i dati vengono aggiornati per le creatività dinamiche esistenti per tale catalogo.

##### Azioni disponibili

La possibilità di creare e modificare contenuti creativi dinamici è attualmente disponibile solo per l’Account Team di Adobe. Tuttavia, tutti gli utenti possono:

* [Anteprima di elementi creativi dinamici](creative-preview.md)

* [Aggiungi creatività dinamica ai bundle di visualizzazione dinamica e rimuovi creatività dinamica da un bundle di visualizzazione dinamica](creative-attach-detach-bundles.md)

* [Duplicare elementi creativi dinamici](creative-duplicate.md)

* [Eliminare le creatività dinamiche](creative-delete.md)

<!-- Later:  Dynamic creatives are generated automatically when you save a catalog, but can regenerate the catalog using the contents of an updated asset file [using the Run Now option]. -->

### Visualizzazione [!UICONTROL Creative Libraries] > [!UICONTROL Bundles]

La visualizzazione [!UICONTROL Bundles] mostra tutti i contenitori di bundle standard e dinamici. Puoi vedere i nomi creativi, le dimensioni creative e i linguaggi dei creativi inclusi in ogni pacchetto. In modalità scheda, è possibile scorrere le immagini in un pacchetto con più elementi creativi utilizzando i pulsanti &lt; e >.

#### Azioni disponibili

* Aggiungi bundle di visualizzazione standard, video standard e dinamica a una libreria

* Elencare e visualizzare in anteprima i creativi in un bundle

* Modificare un nome bundle

* Aggiungi creatività di visualizzazione standard ai bundle di visualizzazione standard e rimuovi creatività di visualizzazione standard da un bundle di visualizzazione standard

* Aggiunta di video creativi standard ai bundle video standard e rimozione di video creativi standard da un bundle video standard

* Bundle duplicati

* Elimina bundle

>[!MORELIKETHIS]
>
>* [Gestisci librerie creative](/help/creative/creative-libraries/creative-library-manage.md)
>* [Aggiungere creatività standard a una libreria creativa](creative-add-standard.md)
>* [Gestione dei bundle creativi](bundle-manage.md)
>* [Personalizza le visualizzazioni dati](/help/creative/introduction/customize-data-views.md)
