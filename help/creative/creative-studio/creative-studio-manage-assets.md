---
title: Gestire le risorse in Creative Studio
description: Scopri come caricare, sfogliare e gestire le risorse nella scheda Creative Studio Assets in Adobe Advertising Creative.
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 24e27656edda50f29292cb75823ef6cacdb685fe
workflow-type: tm+mt
source-wordcount: 292
ht-degree: 0%

---

# Gestisci risorse in [!UICONTROL Creative Studio]

*funzionalità Beta*

Carica immagini, video, audio e risorse font da usare come riferimento nei modelli di annunci e allega ai messaggi chat dell’agente AI durante le sessioni di generazione di annunci.

## Visualizzazione [!UICONTROL Creative Studio] > [!UICONTROL Assets]

Nella scheda **[!UICONTROL Assets]** sono elencate le risorse esistenti in una vista a schede.

### Azioni disponibili

<!--  * [Browse and search assets](#assets-search) -->

* [Caricare le risorse](#assets-upload)

* [Rinominare una risorsa](#assets-rename)

* [Scaricare una risorsa](#assets-download)

* [Eliminare una risorsa](#assets-delete)

<!--

Should be in "Common Tasks" chapter

## Browse and search assets {#assets-search}

* Use the **[!UICONTROL Search assets]** field to find assets by name. Enter at least three characters to trigger a search; shorter queries don't filter results.
* Click **[!UICONTROL Filter]** to filter the asset library by type or other attributes.

-->

## Caricare le risorse {#assets-upload}

1. Nel menu principale, fare clic su **[!UICONTROL Creative Studio].**

1. Fare clic sulla scheda **[!UICONTROL Assets]**.

1. Fare clic su **[!UICONTROL Upload Assets]**.

1. Selezionare uno o più file dal computer o dalla rete.

   Sono supportati i seguenti tipi di file:

   <!-- Verified 2026-07-09 against creative-api TemplateMediaValidator.java (IMAGE_EXTENSIONS, VIDEO_EXTENSIONS, AUDIO_EXTENSIONS), which backs the /v1/creative/template-medias upload/initiate endpoint used by this tab. The Assets tab file input has no client-side accept restriction (TemplateBrowser.tsx) and relies entirely on this backend validator, so it is authoritative. -->

   | Tipo | Formati supportati | Dimensione massima file |
   | --- | --- | --- |
   | Immagini | JPG/JPEG, PNG, GIF, WebP, SVG | 10 MB |
   | Video | MP4, MOV, AVI, WebM | 512 MB |
   | Audio | MP3, WAV, AAC, OGG | 50 MB |

   I file vuoti e i tipi di file non supportati vengono rifiutati con una notifica di errore.

   Il nome della risorsa viene salvato come nome del file caricato senza la relativa estensione. Gli spazi e i caratteri non ASCII nel nome file vengono sostituiti da caratteri di sottolineatura (ad esempio, il caricamento di `My Logo.png` crea una risorsa denominata `My_Logo`). Successivamente puoi rinominare la risorsa.

<!--

maybe later:

   | Fonts | TTF, OTF, WOFF, WOFF2 | 5 MB |
   
-->

## Modificare il nome di una risorsa {#asset-rename}

1. Nel menu principale, fare clic su **[!UICONTROL Creative Studio].**

1. Fare clic sulla scheda **[!UICONTROL Assets]**.

1. Posizionare il cursore sulla scheda delle risorse e fare clic su **[!UICONTROL ...]** > **[!UICONTROL Edit name]**.

1. Aggiorna il nome della risorsa.

   I nomi delle risorse possono contenere fino a 512 caratteri.

1. Fare clic su **[!UICONTROL Update]**.

## Scaricare una risorsa {#asset-download}

1. Nel menu principale, fare clic su **[!UICONTROL Creative Studio].**

1. Fare clic sulla scheda **[!UICONTROL Assets]**.

1. Posizionare il cursore sulla scheda delle risorse e fare clic su **[!UICONTROL ...]** > **[!UICONTROL Download]**.

   La risorsa viene scaricata in base alla normale procedura del browser.

## Eliminare una risorsa {#asset-delete}

>[!NOTE]
>
>Non puoi riattivare una risorsa eliminata.

1. Nel menu principale, fare clic su **[!UICONTROL Creative Studio].**

1. Fare clic sulla scheda **[!UICONTROL Assets]**.

1. Posizionare il cursore sulla scheda delle risorse e fare clic su **[!UICONTROL ...]** > **[!UICONTROL Delete]**.

1. Nel messaggio di conferma, fare clic su **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Informazioni su Creative Studio in Advertising Creative](creative-studio-about.md)
>* [Gestione dei modelli in Creative Studio](creative-studio-manage-templates.md)
>* [Genera annunci standard in Creative Studio](creative-studio-manage-standard-ads.md)
