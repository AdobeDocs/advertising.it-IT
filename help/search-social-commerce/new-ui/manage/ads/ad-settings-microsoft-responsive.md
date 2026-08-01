---
title: '[!DNL Microsoft Advertising] impostazioni degli annunci reattivi'
description: Fai riferimento alle impostazioni per  [!DNL Microsoft Advertising] annunci reattivi.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 730b474b83ae4df47c18f93adfec62b1dc9b8a16
workflow-type: tm+mt
source-wordcount: 243
ht-degree: 0%

---

# Impostazioni degli annunci reattivi (pubblico) di [!DNL Microsoft Advertising]

Il formato degli annunci reattivi è disponibile per gli annunci di pubblico basati su immagini, video e video TV connessi in [!DNL Microsoft Audience Network]. La rete di annunci assembla dinamicamente gli annunci reattivi utilizzando le combinazioni più efficaci di elementi pubblicitari.

## [!UICONTROL Basic Settings]

*Solo nuovi annunci*

**[!UICONTROL Network]:** La rete di annunci.

**[!UICONTROL Account]:** L&#39;account di rete dell&#39;annuncio.

**[!UICONTROL Campaign]:** La campagna.

**[!UICONTROL Ad Group]:** Il gruppo di annunci.

## [!UICONTROL Audience CTV Video Ad Details]

<!-- I can't find a video ad -- this same header is used for image ads. Need to verify the video ad settings and when you'll get them -->

### Annunci video

**[!UICONTROL Videos]:** URL di un annuncio video.

**[!UICONTROL Status]:** Stato annuncio: *[!UICONTROL Active]* o *[!UICONTROL Paused]*.

### Annunci immagine)

>[!NOTE]
>
>La rete di annunci crea automaticamente annunci per le campagne per il pubblico collegate a un negozio di centri commerciali utilizzando le informazioni sui prodotti del negozio e il targeting degli utenti a livello di gruppo di annunci. Non è necessario creare manualmente annunci.

**[!UICONTROL Images]:** Fino a 15 immagini JPEG o PNG per l&#39;annuncio. Includere almeno un&#39;immagine con proporzioni 1.91:1. Visualizza le proporzioni e dimensioni consentite per [immagini annuncio pubblico](https://help.ads.microsoft.com/#apex/ads/en/56912/0).

Per gli annunci di pubblico, [!DNL Microsoft Advertising] ritaglia automaticamente questa immagine per tutte le possibili proporzioni.

<!-- Instructions -->

{{$include /help/_includes/images-ms-multimedia-responsive-ad.md}}

**[!UICONTROL Business Name]:** Nome aziendale, con un massimo di 25 caratteri. Può essere utilizzato nei formati di annuncio di sola chiamata.

**[!UICONTROL Short Headlines]:** Almeno tre e fino a 15 titoli brevi con almeno una parola e un massimo di 30 caratteri ciascuno.

**[!UICONTROL Long Headlines]:** Almeno tre e fino a cinque titoli lunghi con un massimo di 90 caratteri ciascuno.

**[!UICONTROL Ad Text]:** almeno due descrizioni e fino a quattro descrizioni contenenti almeno una parola e un massimo di 90 caratteri ciascuna.

**[!UICONTROL Status]:** Stato annuncio: *[!UICONTROL Active]* o *[!UICONTROL Paused]*.

## [!UICONTROL Tracking URLs]

<!-- **[!UICONTROL Base URl]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

>[!MORELIKETHIS]
>
>* [Gestione annunci](/help/search-social-commerce/new-ui/manage/ads/ad-manage.md)
