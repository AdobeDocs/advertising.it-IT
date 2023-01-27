---
title: Specifiche degli annunci
description: Riferimento alle specifiche generali e specifiche dell'editore.
feature: DSP Ads
exl-id: 133dfc0d-d839-4e06-a819-21e3e630830c
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 0%

---

# Specifiche per i tipi di annunci supportati

## Annunci video (pre-roll, CTV e video universale)

### Schermi supportati

Gli annunci vengono consegnati per impostazione predefinita su dispositivi TV desktop, mobili e collegati. Il targeting dei dispositivi è disponibile per regolare la consegna.

### Server di annunci di terze parti supportati

È possibile utilizzare i tag sheet da [!DNL DCM], [!DNL Flashtalking], [!DNL Innovid]e [!DNL Sizmek]. Per un elenco completo dei fornitori supportati, vedi &quot;[Partner certificati di Ad Serving](certified-ad-servers.md).&quot;

### Requisiti per le risorse video ad alta definizione (richiesto)

**Tipo di tag video:** VPAID 2.0 JavaScript o VAST (CTV). Tutte le unità pubblicitarie VPAID devono rispettare [Specifica VPAID 2.0](https://iabtechlab.com/wp-content/uploads/2016/04/VPAID_2_0_Final_04-10-2012.pdf) come definito da Interactive Advertising Bureau (IAB).

**Codec video:** MP4/H.264

**Risoluzione:** 1280x720 per 720p, 1920x1080 per 1080p

**Bitrate:** 1500-2500 kbps per 720p, 2500-3500 kbps per 1080p

**Profilo/Livello H.264:** profilo alto, livello 3.1 per 720p; Profilo elevato, livello 4.0 per 1080p

**Frame rate video:** 29,970 fps (comunemente denominati 30 fps) per paesi NTSC, 25 fps per paesi PAL, 23,976 fps (comunemente denominati 24 fps) per contenuti di aspetto cinematografico

**Spazio colore video:** 4:2:0 Sottocampionamento per crominanza YUV

**Interlacciamento video:** Scansione progressiva, cioè non interlacciata. Nessun movimento all&#39;interno del campo (frame di fusione) o interlacciamento.

**Leader (ardesia):** Non consentito

**Codec audio:** AAC-LC o HE-AACv1

**Bitrate audio:** 128-192 kbps per AAC-LC, 64-128 kbps per HE-AACv1

**Canale audio:** mix stereo a 2 canali

**Frequenza di campionamento audio:** 44,1 kHz o 48 kHz, come per materiale sorgente

**Livelli audio:** 24 LKFS (+/- 2,0 dB) negli USA secondo ATSC A/85; 23 LUFS (+/- 1.0) nell&#39;UE secondo EBU R128

#### Requisiti aggiuntivi dell&#39;editore per annunci TV collegati

* **Rete A+E:** Consulta Network A+E [specifiche](/help/dsp/assets/a-e-networks-tve-video-ad-specs.pdf)

* **Scoperta:** Vedere Discovery [specifiche](/help/dsp/assets/discovery-networks-ad-specs.pdf).

* **Disney (incl. Hulu):** Vedi Disney&#39;s [specifiche](https://hulu.disneyadsales.com/ad-products/video-commercial/).

* **HBO Max:** Vedere HBO Max&#39;s [specifiche](/help/dsp/assets/hbo-max-ad-specs-2022.xlsx).

* **NBCUniversal:**

   * [Video digitale](https://together.nbcuni.com/nbcu-creative-guidelines/digital-video/)

   * [Livestream](https://together.nbcuni.com/nbcu-creative-guidelines/livestream/)

   * [Peacock](https://together.nbcuni.com/nbcu-creative-guidelines/peacock/)

* **Importo:** Vedere Paramount&#39;s [specifiche](https://www.paramount.com/digital-ads).

## Annunci visualizzati

### Schermi supportati

Gli annunci vengono consegnati per impostazione predefinita su desktop e dispositivi mobili. Il targeting dei dispositivi è disponibile per regolare la consegna.

### Tipi di file supportati

**Immagine:** GIF, JPG/JPEG, PNG

**HTML5:** Tipi di file immagine: GIF, JPG/JPEG, PNG, SVG

### Requisiti per le risorse immagine (obbligatorio)

Supporto della visualizzazione universale.

**Dimensioni annunci consigliate:** 120x60, 160x600, 180x150, 300x50, 300x100, 300x1050, 300x250, 300x60 0, 320x50, 320x480, 480x60, 640x480, 88x31, 728x90, 970x250, 970x90

**Server di annunci di terze parti supportati:** È possibile utilizzare i tag sheet da [!DNL DCM], [!DNL Flashtalking], [!DNL Innovid]e [!DNL Sizmek]. Per un elenco completo dei fornitori supportati, vedi &quot;[Partner certificati di Ad Serving](certified-ad-servers.md).&quot;

## Annunci audio

### Schermi supportati

Desktop, Mobile, Tablet, altoparlanti avanzati e TV connessa

### Server di annunci di terze parti supportati

È possibile utilizzare i tag sheet da [!DNL DCM], [!DNL Flashtalking], [!DNL Innovid]e [!DNL Sizmek]. Per un elenco completo dei fornitori supportati, vedi &quot;[Partner certificati di Ad Serving](certified-ad-servers.md).&quot;

### Requisiti per risorse audio (obbligatorio)

**Tipo di file:** MP3, OGG, AAC

**Leader (ardesia):**  Non consentito

**Dimensione massima del file:** 2 MB

**Bitrate:** 128

**Lunghezza file:** 0-60

#### Requisiti aggiuntivi per gli editori

* **[!DNL iHeartRadio]**
   * Lunghezza: 5, 15, 30 o 60 secondi
   * Tipo di file: MP3
   * Dimensione massima del file: 320 kbps
   * Volume: 44,1 kHz

* **[!DNL Pandora]**
   * Lunghezza: 15 o 30 secondi
   * Tipo di file: MP4 (in-app), MP3 (desktop)
   * Dimensione massima del file: 2,2 MB

* **[!DNL SoundCloud]**
   * Lunghezza: 6, 15 o 30 secondi
   * Tipo di file: MP3
   * Dimensione massima del file: 5 MB

* **[!DNL Spotify]**
   * Lunghezza: Fino a 30 secondi
   * Tipo di file: OGG
   * Dimensione massima del file: 500 MB
   * Volume: RMS normalizzato a -14; picco dBFS normalizzato a -0,2 dBFS

* **[!DNL TargetSpot]**
   * Lunghezza: 15, 30 o 60 secondi
   * Tipo di file: MP3

* **[!DNL TuneIn]**
   * Lunghezza: 10, 15 o 30 secondi
   * Tipo di file: MP3, OGG
   * Volume: 44,1 kHz

### Requisiti per annunci banner Companion (facoltativo)

**Dimensioni supportate:** 300x250, 500x500, 640x640, 1024x1024

#### Requisiti aggiuntivi per gli editori

* **[!DNL iHeartRadio]:**
   * Tipo di file: JPEG, JPG, PNG, GIF, SWF, HTML
   * Dimensione massima del file: 2,2 MB
   * Dimension: 300 x 250

* **[!DNL Pandora]:**
   * Tipo di file: JPEG, GIF
   * Dimensione massima del file: Dimensioni: 100 KB
   * Dimension: 300x250 (mobile o desktop) o 500x500 (desktop)

* **[!DNL SoundCloud]:**
   * Tipo di file: JPG statico, PNG
   * Dimensione massima del file: Meno di 400 KB
   * Dimension: 1024x1024

* **[!DNL Spotify]:**
   * Tipo di file: JPG statico, PNG
   * Dimensione massima del file: 200 KB
   * Dimension: 300 x 250

* **[!DNL TuneIn]:**
   * Tipo di file: JPEG, JPG, PNG, GIF, HTML
   * Dimensione massima del file: 2 MB
   * Dimension: 300 x 250

## Annunci di visualizzazione nativi

Ogni annuncio può includere un&#39;immagine fissa o un GIF in movimento (cinema).

### Schermi supportati

Gli annunci vengono consegnati per impostazione predefinita su desktop e dispositivi mobili. Il targeting dei dispositivi è disponibile per regolare la consegna.

### Risorse necessarie per tutti i formati nativi in feed

#### Risorsa immagine

**Risoluzione:** minimo 600x600px; Minimo consigliato di 1200x627px

**Tipo di file:** JPEG (immagine annuncio video o immagine copertina annuncio video), GIF (cinemograph)

**Dimensione file:** Meno di 1 MB (l&#39;immagine dovrebbe essere priva di testo).

#### Logo dell’inserzionista

**Risoluzione:** almeno 80x80px; Minimo consigliato di 300x300px

**Tipo di file:** JPEG o PNG.

**Rapporto di formato:**  Rapporto 1x1

>[!NOTE]
>
>A seconda dell’immagine su cui verrà sovrapposto, scegli tra le risorse del logo chiaro o scuro.

#### Testo/Copia

**Titolo:** massimo 200 caratteri; 25 caratteri consigliati

**Didascalia:** massimo 200 caratteri; 100 caratteri consigliati

**Sponsorizzato da:** massimo 200 caratteri; 30 caratteri consigliati

**Invito all&#39;azione (solo MoPub):** Massimo 15 caratteri

>[!NOTE]
>
>Il layout finale viene definito dall&#39;editore in fase di esecuzione. Se un annuncio supera il numero di caratteri consigliato, alcuni fornitori di inventario potrebbero non consegnare l&#39;annuncio, oppure l&#39;editore o la SSP potrebbe troncare il testo.

#### URL della pagina di destinazione

L’URL di click-through con tracciatori di clic facoltativi.

Requisiti per i tracciatori di clic:

* Pixel di tracciamento delle impression di terze parti: Solo formato URL immagine 1x1

* Tracciatori JavaScript di visualizzabilità: Supportato solo per IAS; 1x1 immagini solo in formato JS.append

* Pixel di tracciamento dei clic di terze parti: Deve essere reindirizzato alla pagina di destinazione incorporata nell’URL (reindirizzamento HTTP 302)

* Non sono supportati i tracciatori di clic di Data Management Platform (DMP) con 200 o più risposte.

>[!MORELIKETHIS]
>
>* [Informazioni sulla gestione degli annunci](ad-about.md)
>* [Creare un singolo annuncio](ad-create.md)
>* [Creare più annunci di terze parti](ad-create-multiple.md)
>* [Modificare un annuncio](ad-edit.md)

