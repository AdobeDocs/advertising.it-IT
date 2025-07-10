---
title: Specifiche annuncio
description: Fai riferimento a specifiche pubblicitarie generali e specifiche per l’editore.
feature: DSP Ads
exl-id: 133dfc0d-d839-4e06-a819-21e3e630830c
source-git-commit: 10e85f9ec0b7b867828cc9ac154af6f4982c44d2
workflow-type: tm+mt
source-wordcount: '870'
ht-degree: 0%

---

# Specifiche per i tipi di annunci supportati

## Annunci video (pre-roll, CTV e video universali)

### Screens supportato

Gli annunci vengono consegnati per impostazione predefinita su dispositivi desktop, mobili e TV collegati. Per regolare la consegna è disponibile il targeting del dispositivo.

### Server di annunci di terze parti supportati

È possibile utilizzare i fogli tag di [!DNL DCM], [!DNL Flashtalking], [!DNL Innovid] e [!DNL Sizmek]. Per un elenco completo dei fornitori supportati, consulta &quot;[Certified Ad Serving Partners](certified-ad-servers.md)&quot;.

### Requisiti per Assets video ad alta definizione

**Tipo di tag video:** VPAID 2.0 JavaScript o VAST (CTV). Tutte le unità di annunci VPAID devono rispettare la specifica [VPAID 2.0](https://iabtechlab.com/wp-content/uploads/2016/04/VPAID_2_0_Final_04-10-2012.pdf) definita da Interactive Advertising Bureau (IAB).

**Codec video:** MP4/H.264

**Risoluzione:** 1280x720 per 720p, 1920x1080 per 1080p

**Bitrate:** 1500-2500 kbps per 720p, 2500-3500 kbps per 1080p

**Profilo/livello H.264:** Profilo/livello alto, livello 3.1 per 720p; Profilo alto, livello 4.0 per 1080p

**Frequenza fotogrammi video:** 29,970 fps (30 fps) per i paesi NTSC, 25 fps per i paesi PAL, 23,976 fps (24 fps) per i contenuti cinematografici

**Spazio colore video:** 4:2:0 sottocampionamento YUV Chroma

**Interlacciamento video:** Scansione progressiva, ovvero non interlacciata. Nessun movimento all&#39;interno del campo (fusione di fotogrammi) o interlacciamento.

**Leader (Slate):** Non consentito

**Codec audio:** AAC-LC o HE-AACv1

**Bitrate audio:** 128-192 kbps per AAC-LC, 64-128 kbps per HE-AACv1

**Canale audio:** mix stereo a 2 canali

**Frequenza di campionamento audio:** 44,1 kHz o 48 kHz, in base al materiale sorgente

**Livelli audio:** 24 LKFS (+/- 2,0 dB) negli Stati Uniti come da ATSC A/85; 23 LUFS (+/- 1,0) nell&#39;UE come da EBU R128

#### Requisiti aggiuntivi dell&#39;editore per gli annunci TV collegati

* **Rete A+E:** Consulta le [specifiche annuncio](/help/dsp/assets/a-e-networks-tve-video-ad-specs.pdf) di A+E Network

* **Individuazione:** Vedere le [specifiche annuncio](/help/dsp/assets/discovery-networks-ad-specs.pdf) di individuazione.

* **Disney (incluso Hulu):** Consulta le [specifiche degli annunci Disney](https://hulu.disneyadsales.com/ad-products/video-commercial/).

* **HBO Max:** Vedi le [specifiche annuncio](/help/dsp/assets/hbo-max-ad-specs-2022.xlsx) di HBO Max.

* **NBCUniversale:**

   * [Video digitale](https://together.nbcuni.com/nbcu-creative-guidelines/digital-video/)

   * [Livestream](https://together.nbcuni.com/nbcu-creative-guidelines/livestream/)

   * [Pavone](https://together.nbcuni.com/nbcu-creative-guidelines/peacock/)

* **Paramount:** Consulta le [specifiche degli annunci](https://www.paramount.com/digital-ads) di Paramount.

## Annunci visualizzati

### Screens supportato

Gli annunci vengono consegnati per impostazione predefinita su desktop e dispositivi mobili. Per regolare la consegna è disponibile il targeting del dispositivo.

### Tipi di file supportati

**Immagine:** GIF, JPG/JPEG, PNG

**HTML5:** tipi di file immagine: GIF, JPG/JPEG, PNG, SVG

### Requisiti di Image Assets

È supportata la visualizzazione universale.

**Dimensioni annuncio consigliate:** 120x60, 160x600, 180x150, 300x50, 300x100, 300x1050, 300x250, 300x600, 320x50, 320x480, 480x60, 640x480, 88x31, 728x90, 970x250, 970x90

**Server di annunci di terze parti supportati:** È possibile utilizzare fogli di tag di [!DNL DCM], [!DNL Flashtalking], [!DNL Innovid] e [!DNL Sizmek]. Per un elenco completo dei fornitori supportati, consulta &quot;[Certified Ad Serving Partners](certified-ad-servers.md)&quot;.

## Annunci audio

### Screens supportato

Desktop, dispositivi mobili, tablet, altoparlanti avanzati e TV collegata

### Server di annunci di terze parti supportati

È possibile utilizzare i fogli tag di [!DNL DCM], [!DNL Flashtalking], [!DNL Innovid] e [!DNL Sizmek]. Per un elenco completo dei fornitori supportati, consulta &quot;[Certified Ad Serving Partners](certified-ad-servers.md)&quot;.

### Requisiti per Audio Assets

**Tipo file:** MP3, OGG, AAC

**Leader (slate):** Non consentito

**Dimensione massima file:** 2 MB

**Bitrate:** 128

**Lunghezza file:** 0-60s

#### Requisiti aggiuntivi per editori

* **[!DNL iHeartRadio]**
   * Lunghezza: 5, 15, 30 o 60 secondi
   * Tipo di file: MP3
   * Dimensione massima del file: 320 kbps
   * Volume: 44,1 kHz

* **[!DNL Pandora]**
   * Lunghezza: 15 o 30 secondi
   * Tipo di file: MP4 (in-app), MP3 (desktop)
   * Dimensione massima file: 2,2 MB

* **[!DNL SoundCloud]**
   * Lunghezza: 6, 15 o 30 secondi
   * Tipo di file: MP3
   * Dimensione massima file: 5 MB

* **[!DNL Spotify]**
   * Lunghezza: fino a 30 secondi
   * Tipo di file: OGG
   * Dimensione massima del file: 500 MB
   * Volume: RMS normalizzato a-14; picco dBFS normalizzato a-0,2 dBFS

* **[!DNL TargetSpot]**
   * Lunghezza: 15, 30 o 60 secondi
   * Tipo di file: MP3

* **[!DNL TuneIn]**
   * Lunghezza: 10, 15 o 30 secondi
   * Tipo di file: MP3, OGG
   * Volume: 44,1 kHz

### Requisiti per gli annunci banner aziendali (facoltativo)

**Dimensioni supportate:** 300x250, 500x500, 640x640, 1024x1024

#### Requisiti aggiuntivi per editori

* **[!DNL iHeartRadio]:**
   * Tipo di file: JPEG, JPG, PNG, GIF, SWF, HTML
   * Dimensione massima file: 2,2 MB
   * Dimensioni: 300x250

* **[!DNL Pandora]:**
   * Tipo di file: JPEG, GIF
   * Dimensione massima file: Dimensione: 100 KB
   * Dimensioni: 300x250 (mobile o desktop) o 500x500 (desktop)

* **[!DNL SoundCloud]:**
   * Tipo di file: Static JPG, PNG
   * Dimensione massima file: meno di 400 KB
   * Dimensioni: 1024x1024

* **[!DNL Spotify]:**
   * Tipo di file: Static JPG, PNG
   * Dimensione massima file: 200 KB
   * Dimensioni: 300x250

* **[!DNL TuneIn]:**
   * Tipo di file: JPEG, JPG, PNG, GIF, HTML
   * Dimensione massima file: 2 MB
   * Dimensioni: 300x250

## Annunci display nativi

Ogni annuncio può contenere un&#39;immagine fissa o un GIF in movimento (cinemagraph).

### Screens supportato

Gli annunci vengono consegnati per impostazione predefinita su desktop e dispositivi mobili. Per regolare la consegna è disponibile il targeting del dispositivo.

### Assets richiesto per tutti i formati di feed interni

#### Risorsa immagine

**Risoluzione:** Minimo 600x600px; Minimo consigliato di 1200x627px

**Tipo di file:** JPEG (annuncio pubblicitario immagine o immagine di copertina annuncio video), GIF (cinemografo)

**Dimensioni file:** Meno di 1 MB (l&#39;immagine deve essere priva di testo).

#### Logo inserzionista

**Risoluzione:** Minimo 80x80px; Minimo consigliato di 300x300px

**Tipo di file:** JPEG o PNG.

**Proporzioni:** 1x1

>[!NOTE]
>
>A seconda dell’immagine su cui verrà sovrapposta, scegli tra le risorse di logo chiare o scure.

#### Testo/Copia

**Titolo:** Massimo 200 caratteri; consigliati 25 caratteri

**Didascalia:** Massimo 200 caratteri; consigliati 100 caratteri

**Sponsorizzato da:** Massimo 200 caratteri; consigliati 30 caratteri

**Call to action (solo MoPub):** massimo 15 caratteri

>[!NOTE]
>
>Il layout finale viene definito dall’editore in fase di esecuzione. Se un annuncio supera il numero di caratteri consigliato, è possibile che alcuni provider di inventario non inviino l’annuncio oppure che l’editore o il provider di servizi condivisi troncino il testo.

#### URL della pagina di destinazione

L’URL di click-through con tracker di clic opzionali.

Requisiti per i tracciatori di clic:

* Pixel di tracciamento delle impression di terze parti: solo formato URL immagine 1x1

* Visualizzabilità Tracciatori JavaScript: supportati solo per IAS; immagini 1x1 solo in formato JS.append

* Pixel di tracciamento dei clic di terze parti: deve essere reindirizzato alla pagina di destinazione incorporata nell’URL (reindirizzamento HTTP 302)

* I tracciatori di clic della piattaforma di gestione dati (DMP) con 200 o più risposte non sono supportati.

>[!MORELIKETHIS]
>
>* [Informazioni Sulla Gestione Degli Annunci](ad-about.md)
>* [Crea un annuncio singolo](ad-create.md)
>* [Creazione di più annunci di terze parti](ad-create-multiple.md)
>* [Modifica un annuncio](ad-edit.md)
