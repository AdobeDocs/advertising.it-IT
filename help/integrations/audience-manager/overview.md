---
title: Integrazioni di Adobe Advertising con Adobe Audience Manager
description: Scopri i diversi modi in cui Adobe Advertising può scambiare dati con Adobe Audience Manager.
feature: Integration with Adobe Audience Manager
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: 7fa058da06edadf9b98aa49b0e5a1110ea68808c
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 0%

---

# Integrazioni di Adobe Advertising con Adobe Audience Manager

È possibile integrare Adobe Advertising con Audience Manager nei seguenti modi.

## Sincronizza Audience Manager e altri [!DNL Adobe] segmenti per il targeting degli annunci

[!DNL Search, Social, & Commerce] e DSP possono richiamare metadati, dati gerarchici e dati di pubblico univoci per tutti i tipi di pubblico di Audience Manager e di altri tipi di pubblico di [!DNL Adobe] dell&#39;inserzionista o dell&#39;agenzia. Questa connessione univoca è disponibile solo per gli esperti di marketing che utilizzano Adobe Advertising. Consulta &quot;[Importare segmenti Adobe Audience Manager per il targeting degli annunci](/help/integrations/audience-manager/import-audiences.md).&quot;

### Utilizza Audience Manager e altri segmenti [!DNL Adobe] per creare [!DNL Google Ads] tipi di pubblico {#audience-manager-google-audiences}

*Inserzionisti con consenso con [!DNL Advertising Search, Social, & Commerce] solo*

In [!DNL Search, Social, & Commerce], puoi creare [!DNL Google Ads] tipi di pubblico in base ai clienti dagli ID utente utilizzando i tuoi segmenti esistenti di Audience Manager che hanno [!UICONTROL Adobe Media Optimizer (HTTP)] e [!UICONTROL Adobe Media Optimizer Batch Destination] come destinazioni. ([!DNL Media Optimizer] è un nome precedente per [!DNL Search, Social, & Commerce].) Sono inclusi i segmenti di Adobe Analytics pubblicati in Adobe Experience Cloud e i segmenti creati con Adobe Experience Cloud [!DNL Audience Library]. Per ulteriori informazioni, consulta &quot;[Creare [!DNL Google Ads] tipi di pubblico corrispondenti ai clienti di [!DNL Adobe] tipi di pubblico](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md).&quot;

[I tipi di pubblico corrispondenti ai clienti degli ID utente](https://support.google.com/google-ads/answer/9199250) funzionano come i tipi di pubblico basati su tag del sito Web, ma un ID non PII viene assegnato ai membri del pubblico univoci per offrire vantaggi distinti rispetto ai tipi di pubblico standard basati su tag dei clienti e dei siti Web.

Per creare gli ID utente necessari, devi utilizzare un tag JavaScript di Adobe Advertising <!-- with a user ID parameter --> sui tuoi siti web. Per ulteriori informazioni, contatta il team del tuo account di Adobe.

![processo di creazione segmento](/help/integrations/assets/ad_search_user_id_pic.png)

Dopo aver creato i tipi di pubblico, puoi utilizzarli nelle campagne [!DNL Google Ads] come [destinazioni o esclusioni a livello di campagna o di gruppo di annunci](#audience-manager-targets).

### Utilizza Audience Manager e altri segmenti [!DNL Adobe] per eseguire il targeting o escludere gli annunci {#audience-manager-targets}

* (Inserzionisti con consenso con [!DNL Search, Social, & Commerce]) Puoi utilizzare qualsiasi pubblico [!DNL Google Ads] creato [utilizzando [!DNL Adobe] segmenti](#audience-manager-google-audiences) come target o esclusioni a livello di campagna o di gruppo di annunci nelle campagne [!DNL Google Ads].

* (Inserzionisti con DSP) Puoi utilizzare i segmenti [!DNL Adobe] esistenti come destinazioni per i posizionamenti di annunci. Facoltativamente, puoi includere i segmenti in tipi di pubblico riutilizzabili, che puoi utilizzare come target o esclusioni per più posizionamenti.

* (Inserzionisti con Advertising Creative) Puoi utilizzare i segmenti [!DNL Adobe] esistenti come target per creativi specifici nelle esperienze pubblicitarie.

>[!NOTE]
>
>Per ulteriori informazioni su come creare tipi di pubblico nelle interfacce Audience Manager e Experience Cloud [!DNL Audience Library] e casi d&#39;uso comuni per diversi tipi di pubblico, vedi &quot;[Opzioni di creazione pubblico](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html)&quot;.

## Inviare dati sull’esposizione dei contenuti multimediali DSP ad Audience Manager

*Inserzionisti con solo DSP*

I clienti di DSP con Adobe Audience Manager possono acquisire dati dalle campagne pubblicitarie utilizzando chiamate pixel ad Audience Manager. Puoi quindi utilizzare i dati della campagna per creare caratteristiche basate su regole, da utilizzare per definire nuovi segmenti per abilitare vari casi d’uso di DSP, ad esempio segmentazione più avanzata, gestione della frequenza, analisi di marketing e informazioni sul reporting.

Per ulteriori informazioni, vedere &quot;[Panoramica dell&#39;invio dei dati di esposizione dei supporti DSP a Adobe Audience Manager](/help/integrations/audience-manager/media-data-integration/overview.md)&quot;.

## Ottieni informazioni più approfondite sull’attività del sito con Audience Analytics

I clienti Adobe Advertising con [[!DNL Adobe Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) possono inviare sia dati tracciati da Adobe Advertising che segmenti Audience Manager a [!DNL Analytics] per ottenere informazioni approfondite sull&#39;attività del sito.

Per ulteriori informazioni, vedere &quot;[[!DNL Adobe Audience Analytics] per i clienti Adobe Advertising](/help/integrations/audience-manager/audience-analytics.md).&quot;
