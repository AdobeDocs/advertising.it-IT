---
title: Integrazioni pubblicitarie di Adobe con Adobe Audience Manager
description: Scopri i diversi modi in cui Adobe Advertising può scambiare dati con Adobe Audience Manager.
feature: Integration with Adobe Audience Manager
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: 0b5e60f033d623bb6d342c6b56cb98f0bfcde916
workflow-type: tm+mt
source-wordcount: '502'
ht-degree: 0%

---

# Integrazioni pubblicitarie di Adobe con Adobe Audience Manager

Puoi integrare Adobe Advertising con Audience Manager nei seguenti modi.

## Sincronizza Audience Manager e altro [!DNL Adobe] Segmenti per il targeting degli annunci

[!DNL Search] e DSP inserire metadati, dati gerarchici e dati di audience univoci per tutti gli Audienci Manager di un inserzionista o di un&#39;agenzia e per altri [!DNL Adobe] pubblico. Questa connessione univoca è disponibile solo per gli addetti al marketing che utilizzano Adobe Advertising. Vedere &quot;[Importare segmenti Adobe Audience Manager per il targeting degli annunci](/help/integrations/audience-manager/import-audiences.md).&quot;

### Usa Audience Manager e altro [!DNL Adobe] Segmenti da creare [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*Inserzionisti con consenso con [!DNL Advertising Search] only*

Entro [!DNL [!DNL Search]], puoi creare [!DNL Google Ads] I tipi di pubblico dei clienti Google corrispondono a quelli degli ID utente utilizzando i segmenti di Audience Manager esistenti che hanno [!UICONTROL Adobe Media Optimizer (HTTP)] e [!UICONTROL Adobe Media Optimizer Batch Destination] come destinazioni. ([!DNL Media Optimizer] è un nome precedente per [!DNL [!DNL Search]]. Ciò include i segmenti Adobe Analytics pubblicati in Adobe Experience Cloud e i segmenti creati utilizzando Adobe Experience Cloud [!DNL Audience Library]. Per ulteriori informazioni, consulta la guida interna al prodotto in [!DNL [!DNL Search]].

[Corrispondenza cliente ai tipi di pubblico dagli ID utente](https://support.google.com/google-ads/answer/9199250) funziona come un pubblico basato su tag del sito web, ma un ID non PII viene assegnato a membri di pubblico univoci per vantaggi distinti rispetto ai tipi di pubblico standard basati sulla corrispondenza del cliente e a quelli basati su tag del sito web.

Per creare gli ID utente necessari, devi utilizzare un tag JavaScript di pubblicità di Adobe <!-- with a user ID parameter -->sui siti web. Contatta [!DNL [!DNL Search]] per ulteriori informazioni.

![processo di creazione dei segmenti](/help/integrations/assets/ad_search_user_id_pic.png)

Una volta creati i tipi di pubblico, puoi utilizzarli in [!DNL Google Ads] campagne come [target o esclusioni a livello di campagna o di gruppo di annunci](#audience-manager-targets).

### Utilizzare Audience Manager e altri [!DNL Adobe] Segmenti in Target o Annunci esclusi {#audience-manager-targets}

* (Annunci Opted-in con [!DNL [!DNL Search]]) È possibile utilizzare qualsiasi [!DNL Google Ads] tipi di pubblico che erano [creato utilizzando [!DNL Adobe] segmenti](#audience-manager-google-audiences) come target o esclusioni a livello di campagna o di gruppo di annunci nel tuo [!DNL Google Ads] campagne.

* (Inserzionisti con DSP) Puoi utilizzare il tuo esistente [!DNL Adobe] come target per i posizionamenti degli annunci. Facoltativamente, puoi includere i segmenti nei tipi di pubblico riutilizzabili, che puoi utilizzare come target o esclusioni per più posizionamenti.

* (Inserzionisti con Advertising Creative) Puoi utilizzare il tuo esistente [!DNL Adobe] segmenti come target per creativi specifici nelle esperienze pubblicitarie.

>[!NOTE]
>
>Per ulteriori informazioni su come creare tipi di pubblico nell’Audience Manager e nell’Experience Cloud [!DNL Audience Library] interfacce e casi d’uso comuni per tipi di pubblico diversi, consulta &quot;[Opzioni di creazione del pubblico](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html).&quot;

## Inviare DSP dati di esposizione a contenuti multimediali ad Audience Manager

*Inserzionisti con solo DSP*

DSP clienti con Adobe Audience Manager possono acquisire dati da campagne pubblicitarie utilizzando chiamate pixel ad Audience Manager. Puoi quindi utilizzare i dati della campagna per creare caratteristiche basate su regole, che puoi utilizzare per definire nuovi segmenti per abilitare vari casi di utilizzo DSP, come segmentazione più avanzata, gestione delle frequenze, analisi di marketing e informazioni sul reporting.

Vedere &quot;[Panoramica sull’invio DSP dati di esposizione a contenuti multimediali a Adobe Audience Manager](/help/integrations/audience-manager/media-data-integration/overview.md)&quot; per ulteriori informazioni.

## Approfondimenti più approfonditi sulle attività del sito con Audience Analytics

Adobe Advertising Customer con [[!DNL Adobe][!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) può inviare sia dati tracciati dalla pubblicità di Adobe che segmenti di Audience Manager a [!DNL Analytics] per informazioni approfondite sull’attività del sito.

Per ulteriori informazioni, consulta &quot;[[!DNL Adobe][!DNL Audience Analytics] ad Adobe i clienti della pubblicità](/help/integrations/audience-manager/audience-analytics.md).&quot;
