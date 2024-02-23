---
title: Integrazioni Adobi Advertising con Adobe Audience Manager
description: Scopri i diversi modi in cui Adobi Advertising può scambiare dati con Adobe Audience Manager.
feature: Integration with Adobe Audience Manager
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: d0260fc3b10f1944b82cdc4c1e3b8137a695e05e
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 0%

---

# Integrazioni Adobi Advertising con Adobe Audience Manager

È possibile integrare Adobi Advertising con Audienci Manager nei seguenti modi.

## Sincronizza Audience Manager e altro [!DNL Adobe] Segmenti per Ad Targeting

[!DNL Search, Social, & Commerce] e l&#39;DSP può inserire metadati, dati gerarchici e dati di pubblico univoci per tutti gli Audienci Manager e gli altri dati dell&#39;inserzionista o dell&#39;agenzia [!DNL Adobe] pubblico. Questa connessione univoca è disponibile solo per gli esperti di marketing che utilizzano Adobi Advertising. Consulta &quot;[Importare segmenti Adobe Audience Manager per il targeting di annunci](/help/integrations/audience-manager/import-audiences.md).&quot;

### Usa Audience Manager e altro [!DNL Adobe] Segmenti da creare [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*Inserzionisti con consenso con [!DNL Advertising Search, Social, & Commerce] solo*

Entro [!DNL Search, Social, & Commerce], è possibile creare [!DNL Google Ads] i clienti abbinano i tipi di pubblico dagli ID utente utilizzando i segmenti di Audience Manager esistenti che hanno [!UICONTROL Adobe Media Optimizer (HTTP)] e [!UICONTROL Adobe Media Optimizer Batch Destination] come destinazioni. ([!DNL Media Optimizer] è un nome precedente per [!DNL Search, Social, & Commerce].) Sono inclusi i segmenti di Adobe Analytics pubblicati in Adobe Experience Cloud e i segmenti creati utilizzando Adobe Experience Cloud [!DNL Audience Library]. Per ulteriori informazioni, consulta la sezione &quot;[Crea [!DNL Google Ads] audience di corrispondenza cliente da [!DNL Adobe] audience](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md).&quot;

[I clienti abbinano i tipi di pubblico dagli ID utente](https://support.google.com/google-ads/answer/9199250) funziona come un pubblico basato su tag del sito web, ma un ID non PII viene assegnato a membri del pubblico univoci per offrire vantaggi distinti rispetto ai tipi di pubblico standard basati su tag del cliente e del sito web.

Per creare gli ID utente necessari, devi utilizzare un tag JavaScript di Adobe Advertising <!-- with a user ID parameter -->sui tuoi siti web. Per ulteriori informazioni, contatta il team del tuo account di Adobe.

![processo di creazione del segmento](/help/integrations/assets/ad_search_user_id_pic.png)

Una volta creati i tipi di pubblico, puoi utilizzarli in [!DNL Google Ads] campagne come [target o esclusioni a livello di campagna o di gruppo di annunci](#audience-manager-targets).

### Usa Audience Manager e altro [!DNL Adobe] Segmenti per Target o annunci esclusi {#audience-manager-targets}

* (inserzionisti con consenso con [!DNL Search, Social, & Commerce]) È possibile utilizzare qualsiasi [!DNL Google Ads] tipi di pubblico che erano [creato con [!DNL Adobe] segmenti](#audience-manager-google-audiences) come target o esclusioni a livello di campagna o di gruppo di annunci nel tuo [!DNL Google Ads] campagne.

* (Inserzionisti con DSP) Puoi utilizzare il tuo [!DNL Adobe] segmenti come destinazioni per i posizionamenti di annunci. Facoltativamente, puoi includere i segmenti in tipi di pubblico riutilizzabili, che puoi utilizzare come target o esclusioni per più posizionamenti.

* (Per gli inserzionisti che utilizzano Advertising Creative) Puoi utilizzare i [!DNL Adobe] segmenti come target per creativi specifici nelle esperienze pubblicitarie.

>[!NOTE]
>
>Per ulteriori informazioni su come creare tipi di pubblico, consulta l’Audience Manager e l’Experience Cloud [!DNL Audience Library] e casi d’uso comuni per tipi di pubblico diversi, consulta la sezione &quot;[Opzioni di creazione del pubblico](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html).&quot;

## Inviare dati sull’esposizione ai contenuti multimediali dell’DSP agli Audienci Manager

*Inserzionisti solo con DSP*

I clienti DSP con Adobe Audience Manager possono acquisire dati da campagne pubblicitarie utilizzando chiamate pixel per gli Audienci Manager. Puoi quindi utilizzare i dati della campagna per creare caratteristiche basate su regole, da utilizzare per definire nuovi segmenti per abilitare vari casi d’uso dell’DSP, ad esempio segmentazione più avanzata, gestione della frequenza, analisi di marketing e informazioni sul reporting.

Consulta &quot;[Panoramica dell’invio dei dati sull’esposizione ai contenuti multimediali dell’DSP a Adobe Audience Manager](/help/integrations/audience-manager/media-data-integration/overview.md)&quot; per ulteriori informazioni.

## Ottieni informazioni più approfondite sull’attività del sito con Audienci Analytics

Adobe Advertising di clienti con [[!DNL Adobe Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) può inviare sia dati tracciati dagli Adobi Advertising che segmenti di Audienci Manager a [!DNL Analytics] per ottenere informazioni approfondite sull’attività del sito.

Per ulteriori informazioni, consulta la sezione &quot;[[!DNL Adobe Audience Analytics] ad Adobe Advertising Clienti](/help/integrations/audience-manager/audience-analytics.md).&quot;
