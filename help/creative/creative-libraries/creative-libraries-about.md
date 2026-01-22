---
title: Informazioni sul tuo creativo librerie
description: Scopri sulla gestione delle creatività per le tue esperienze annuncio.
feature: Creative Libraries, Creative Standard Creatives, Creative Dynamic Creatives
exl-id: 77dc6528-a455-4406-98b6-15e7ce529370
source-git-commit: 8d549853be10ebfbb71b14e013b04178466e87fe
workflow-type: tm+mt
source-wordcount: '1529'
ht-degree: 0%

---

# Informazioni sulle librerie creative

Il tuo creativo librerie ti consente di gestire le creatività che utilizzerai nelle tue esperienze annuncio. Puoi creare più librerie, ciascuno con un set di creatività e *creativo bundle*, ovvero gruppi di creatività che puoi aggiungere a un&#39;esperienza come un&#39;unica unità.

Il librerie può includere:

* **Creatività individuali:** puoi includere le singole creatività direttamente all&#39;interno annuncio esperienze che non hanno target utente definiti. Puoi anche usare le tue creatività per creare pacchetti, che puoi includere in esperienze[ annuncio mirate](/help/creative/experiences/experience-about.md).

   * **Creatività standard:** puoi caricare e gestire creatività in [vari formati](#creative-creative-formats). Per ogni creativo, specificate la lingua predefinita per ogni annuncio a cui associate il creativo e la pagina di destinazione predefinita che viene aperta quando un utente fa clic su un annuncio che include la creativo. Facoltativamente, è possibile specificare etichette da utilizzare come filtri all&#39;interno di varie viste all&#39;interno [!DNL Creative] e come valori di colonna nel quando si include l&#39;uso [!UICONTROL Custom Creative Report] della [!UICONTROL Creative Label] dimensione.

   * **Creatività dinamiche:** puoi creare creatività generate dinamicamente mappando le variabili dinamiche in un modello annuncio ai valori in un file feed. Tutti gli utenti possono visualizzare in anteprima, duplicare ed eliminare le inserzioni dinamiche esistenti.

* **Pacchetti creatività:** raggruppa le creatività in pacchetti da utilizzare in più esperienze con target utente definiti. Puoi creare *pacchetti* display standard costituiti da annunci display standard, *pacchetti video* standard costituiti da annunci video standard e *pacchetti* display dinamici costituiti da annunci display generati dinamicamente.

## Formati di Creative supportati {#creative-creative-formats}

### Formati per creatività standard

È possibile aggiungere e gestire i seguenti tipi di creativo nelle [dimensioni](creative-sizes.md) di creativo supportate.

>[!IMPORTANT]
>
>* Anche se intendi utilizzare HTML5, HTML5 flessibile o creatività di terze parti per le tue esperienze di visualizzazione annuncio standard, devi aggiungere anche creatività di immagini per ogni dimensione creativo utilizzata.
>* Ogni esperienza di visualizzazione standard richiede un creativo predefinito dell&#39;immagine per ogni dimensione creativo assegnata all&#39;esperienza. Le creatività immagini predefinite vengono utilizzate quando un browser non è abilitato per JavaScript o quando il ad server non può personalizzare il annuncio a causa di ritardi.
>* Ogni esperienza video standard richiede un creativo video predefinito per ogni creativo durata assegnata all&#39;esperienza.<!-- when is it used? -->

#### HTML5 flessibile

I creativi HTML5 flessibili sono creativi HTML5 con tutte le immagini e altri attributi come tag HTML standard, che è possibile modificare direttamente in [!DNL Creative], sia all&#39;interno di una libreria creativa che all&#39;interno di una singola esperienza (che crea una variazione della creatività originale). In DSP, i creativi flessibili di HTML5 sono per una singola dimensione di annuncio specifica (in pixel). Facoltativamente, è possibile modificare i valori predefiniti degli attributi specificati in una creatività flessibile di HTML5. In seguito, puoi specificare valori personalizzati per gli attributi all’interno di un’esperienza specifica, creando una variante della creatività principale.

Puoi caricare creativi flessibili HTML5 come file ZIP o utilizzare uno dei modelli disponibili per il tuo account come punto di partenza. Consulta le [specifiche per le creatività flessibili di HTML5](html5-creative-specification.md).

#### Creatività del display standard

Gli annunci display standard includono:

* Creative HTML5 caricate localmente o da Adobe GenStudio for Performance Marketing.
* File di immagine caricati localmente o da Adobe Experience Manager.

##### Creatività di HTML5

* **Esperienze GenStudio:** è possibile importare tutte le varianti di annunci da una [esperienza di visualizzazione](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/create/display-ad-experiences) in [GenStudio for Performance Marketing](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/home) come contenuto creativo di HTML5. I collegamenti esterni vengono convertiti in riferimenti locali. Il contenuto del HTML può essere fino a 20 MB e le singole immagini fino a 50 MB.

  Dopo aver importato un’esperienza GenStudio, puoi modificare i metadati (nome, lingua, tag) per la creatività importata, ma non per il contenuto creativo. Se si modifica l&#39;esperienza GenStudio in GenStudio, reimportare l&#39;esperienza in [!DNL Creative] per utilizzare la versione più recente.

  >[!NOTE]
  >
  >Per utilizzare questa funzione, sia l’account GenStudio che l’account Advertising Creative devono utilizzare lo stesso ID organizzazione e l’utente deve disporre delle autorizzazioni per accedere a GenStudio.

* **File caricati:** È inoltre possibile caricare creative HTML5 semplici o statiche, con tutti gli attributi e le immagini specificati, come file ZIP. Non è possibile modificare attributi o aggiungere immagini, ma caricare un nuovo file ZIP per aggiungere una nuova creatività. Consulta le [specifiche per creative HTML5 semplici e statiche](html5-creative-specification.md).

##### Creatività delle immagini

Puoi includere creativi di immagini in formato GIF, JPEG, JPG o PNG. Puoi caricare immagini approvate dagli account Adobe Experience Manager o immagini dal dispositivo o dalla rete.

Ogni esperienza di visualizzazione e annuncio standard richiede una creatività di immagine predefinita per ogni dimensione creativa assegnata all’esperienza.

#### Creatività di terze parti

Immetti i tag di tracciamento di JavaScript per i creativi in hosting su server di annunci di terze parti. Lo script varia in base ad server; Di seguito è riportato un esempio:

```
<SCRIPT language='JavaScript1.1' SRC="https://ad.doubleclick.net/ddm/adj/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp];dc_lat=;dc_rdid=;tag_for_child_directed_treatment=?"></SCRIPT> <NOSCRIPT> <A HREF="https://ad.doubleclick.net/ddm/jump/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp]?"><IMG SRC="https://ad.doubleclick.net/ddm/ad/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp];dc_lat=;dc_rdid=;tag_for_child_directed_treatment=?"BORDER=0 WIDTH=300 HEIGHT=250 ALT="Advertisement"></A></NOSCRIPT>
```

#### Video creatività {#creative-video-specs}

Puoi caricare creatività video di prime parti per TV web, dispositivi mobili o connessi dal tuo dispositivo o dalla tua rete. Ogni esperienza di annuncio video standard richiede un creativo video predefinito per ogni durata creativo assegnata all&#39;esperienza. DSP transcodifica automaticamente tutte le creatività video come tag VAST 2.0 in modo da poterle visualizzare in anteprima. In [!UICONTROL Tag Manager], potete applicare facoltativamente [la transcodifica](/help/creative/experiences/experience-tag-video-transcoding.md) DSP specifica a qualsiasi video annuncio esperienza tag.

Consulta il seguente video creativo requisiti. **Nota:** se carichi esperienze video in Advertising DSP, consulta anche i requisiti di [DSP per la Assets](https://experienceleague.adobe.com/en/docs/advertising/dsp/campaign-management/ads/ad-specs#requirements-for-high-definition-video-assets) di Video ad alta definizione, che potrebbero essere più limitati.

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

**Audio Frequenza** di campionamento: 44100-48000 Hz

**Frequenza Audio:** 44,1 kHz o 48 kHz

**Audio Altro:** il file caricato deve essere non interlacciato, misto e contenere una traccia audio. Potrebbe non essere presente alcun suono, ma nel file video deve essere inclusa una traccia audio.

### Formato per gli annunci dinamici

Puoi generare dinamicamente creatività in formato HTML5 statico e HTML5 dinamico mappando le variabili dinamiche in un modello annuncio ai valori in un file feed. Le creatività dinamiche possono includere creatività di cui è stata eseguita la migrazione dalle esperienze precedenti di Adobe Systems Advertising Dynamic Creative Optimization (DCO).

## I [!UICONTROL Creative Libraries] panorami

Per ulteriori informazioni sulla personalizzazione di ciascuna visualizzazione, consulta &quot;[Personalizzare le visualizzazioni](/help/creative/introduction/customize-data-views.md) di dati&quot;.

### La [!UICONTROL Creative Libraries] vista principale

La [!UICONTROL Creative Libraries] vista principale mostra tutte le librerie creativo. I dati per ogni libreria includono il numero di esperienze a cui sono assegnati i bundle del libreria, il numero di bundle, il numero di creatività, il numero di creativo dimensioni, il numero di target linguistici predefiniti, la data di creazione e la data di ultima modifica per qualsiasi elemento del libreria. La modalità tabella include anche una colonna per l&#39;inserzionista.

Quando sei in modalità scheda, puoi scorrere le immagini in un libreria con più creatività utilizzando i &lt; and > pulsanti.

#### Azioni disponibili

* [Crea una nuova libreria](/help/creative/creative-libraries/creative-library-manage.md#create-a-creative-library)

* Per ogni creativo libreria:

   * [Modifica un nome libreria](/help/creative/creative-libraries/creative-library-manage.md#edit-the-name-of-a-creative-library)

   * [Apri un libreria per visualizzare le creatività e i bundle assegnati al libreria](/help/creative/creative-libraries/creative-library-manage.md#open-a-creative-library)

   * [Elimina librerie](/help/creative/creative-libraries/creative-library-manage.md#delete-creative-libraries)

### Il [!UICONTROL Creative Libraries] > [!UICONTROL Creatives] viste

#### [!UICONTROL Standard Ads]

Il [!UICONTROL Standard Ads] scheda mostra tutte le creatività standard che hai creato. I dati per ogni creativo includono le dimensioni del creativo, il tipo di creativo e la data di creazione. La modalità tabella include anche colonne per la lingua predefinita e la pagina di destinazione predefinita.

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

La scheda [!UICONTROL Dynamic Ads] mostra tutte le creatività dinamiche create dinamicamente per i cataloghi creativi, ad eccezione delle creatività dinamiche [eliminate manualmente](creative-delete.md) dalla scheda [!UICONTROL Dynamic Ads]. Se [hai duplicato manualmente](creative-duplicate.md) qualsiasi creatività dinamica<!-- I don't think existing ads are deletd via feeds, so this probably isn't true: since a catalog was last processed -->, l&#39;elenco delle creatività per quel catalogo include anche le creatività duplicate.

I dati per ogni creatività includono il tipo di creatività, la dimensione della creatività, il numero di cataloghi a cui appartiene la creatività e la data di creazione. La modalità tabella include anche le colonne per il modello di annuncio attraverso il quale è stata generata la creatività e il conteggio delle offerte.

>[!NOTE]
>
>Ogni volta che un catalogo viene elaborato, i dati vengono aggiornati per le creatività dinamiche esistenti per tale catalogo.<!-- Verify this!!! And is there anything more to say w/regard to  -->

##### Azioni disponibili

* [Aggiungere elementi creativi dinamici a una libreria](creative-add-dynamic.md)

* [Modificare una creatività dinamica](creative-edit-dynamic.md)

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
