---
title: Informazioni sui tipi di pubblico
description: Scopri le opzioni per tenere traccia, creare e gestire [!DNL Google Ads] e [!DNL Microsoft Advertising] i tipi di pubblico.
exl-id: f85cbc82-ddbc-4ecd-a17b-b4cb4808cfbc
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 0%

---

# Informazioni sulla gestione dei tipi di pubblico [!DNL Google Ads] e [!DNL Microsoft Advertising] in Search, Social e Commerce

Solo *[!DNL Google Ads]e [!DNL Microsoft Advertising]*

Nella Libreria tipi di pubblico sono elencati tutti i tipi di pubblico [!DNL Google Ads] basati su dati cliente, di mercato e simili, nonché i tipi di pubblico [!DNL Microsoft Advertising] di remarketing e remarketing dinamico, personalizzati, di corrispondenza dei clienti, di mercato e simili. È possibile utilizzare uno qualsiasi dei tipi di pubblico [!DNL Google Ads] come [!DNL Google Ads] destinazioni ed esclusioni a livello di campagna e di gruppo di annunci ed è possibile utilizzare uno qualsiasi dei tipi di pubblico [!DNL Microsoft Advertising] come [!DNL Microsoft Advertising] destinazioni a livello di campagna e di gruppo di annunci ed esclusioni (solo tipi di pubblico di remarketing dinamico). Puoi aggiungere o modificare una regolazione dell’offerta per qualsiasi target di pubblico.

Puoi anche creare e gestire i tipi di pubblico utilizzando segmenti o elenchi e-mail dai tipi di pubblico esistenti di Adobe Experience Cloud e da vari tipi di dati cliente provenienti dal sistema di gestione delle relazioni con i clienti (CRM):

* **Segmenti di pubblico di Adobe:** Gli inserzionisti con account Adobe Audience Manager o Adobe Analytics che hanno prestato il consenso possono creare [!DNL Google Ads] tipi di pubblico corrispondenti ai clienti dai loro [!DNL Adobe] segmenti:

   * (Per gli inserzionisti con account [!DNL Analytics] che non dispongono di Audience Manager) Puoi creare [!DNL Google Ads] tipi di pubblico in base ai clienti utilizzando gli ID utente di [!DNL Analytics] segmenti condivisi con Adobe Experience Cloud.

   * (Inserzionisti con account Audience Manager) Puoi creare [!DNL Google Ads] tipi di pubblico in base ai clienti utilizzando gli ID utente dai segmenti Audience Manager che hanno Search, Social e Commerce come destinazione. Possono essere inclusi i segmenti di Adobe Analytics pubblicati in Adobe Experience Cloud e i segmenti creati utilizzando la Libreria tipi di pubblico di Adobe Experience Cloud.

  Per creare tipi di pubblico in base ai clienti, l&#39;account [!DNL Google Ads] dell&#39;inserzionista deve essere [idoneo per la corrispondenza personalizzata](https://support.google.com/adspolicy/answer/6299717) e ha acconsentito a [segmenti ID utente](https://support.google.com/google-ads/answer/9199250). Inoltre, l’account dell’inserzionista in Search, Social e Commerce deve essere configurato per consentire la creazione di tipi di pubblico in base ai clienti.

  [!DNL Adobe] i dati dei segmenti e i file di sincronizzazione dei cookie per i tipi di pubblico basati su dati del cliente vengono sincronizzati con [!DNL Google Ads] al giorno.

* **Elenchi e-mail di Adobe Campaign:** Il team dell&#39;account Adobe può aiutarti a configurare un flusso di lavoro per la creazione e l&#39;aggiornamento di un pubblico di [!DNL Google Ads] customer match da un elenco e-mail all&#39;interno di [!DNL Campaign].

* **Elenchi dati cliente:** Gli inserzionisti con [!DNL Google Ads] o [!DNL Microsoft Advertising] account idonei per la corrispondenza con il cliente possono creare e aggiornare un pubblico basato su dati cliente specifico per la rete di annunci &lt;!— o pubblico di remarketing dinamico — incluso nel pubblico basato sui dati del cliente, almeno per [!DNL Google Ads]? —> caricando un file CSV con identificatori primari.

* **Elenchi di remarketing dinamico:** gli inserzionisti con [!DNL Microsoft Advertising] account possono creare e gestire tipi di pubblico di remarketing dinamico, che è possibile utilizzare per il retargeting di potenziali clienti che hanno recentemente interagito con i prodotti in uno dei diversi modi (come visualizzatori di prodotti o acquirenti passati). I tipi di pubblico di remarketing dinamico richiedono l’utilizzo del tag di conversione JavaScript e tracciamento del pubblico della rete di annunci sulle pagine web. Utilizza gli elenchi di remarketing dinamico con campagne di acquisto sulle reti di ricerca e pubblico per effettuare il retargeting dei tipi di pubblico con annunci di prodotto, nonché con campagne di ricerca per effettuare il retargeting dei tipi di pubblico con annunci di testo e annunci di ricerca dinamica. <!--[For [!DNL Google Ads], these are technically included in a customer data-based audience, so word this all carefully when we add support for them.]-->

  >[!NOTE]
  >
  >I modificatori di offerte per i target del pubblico di remarketing dinamico non sono ottimizzati nei portfolio con l&#39;impostazione &quot;[!UICONTROL Auto-optimize Bid Adjustment Values]&quot;.

>[!NOTE]
>
>Search, Social e Commerce non memorizzano i dati dei clienti caricati o dei segmenti [!DNL Adobe] utilizzati per creare o modificare un pubblico [!DNL Google Ads] o [!DNL Microsoft Advertising].

>[!MORELIKETHIS]
>
>* [Crea [!DNL Google Ads] audience corrispondenti ai clienti da [!DNL Adobe] audience](google-audience-from-adobe-audience.md)
>* [Creazione di un pubblico di tipo customer match [!DNL Google Ads] da un elenco e-mail di Adobe Campaign](google-audience-from-campaign-email-list.md)
>* [Gestire i tipi di pubblico in base ai clienti utilizzando gli elenchi di dati dei clienti](audience-from-customer-data-list.md)
>* [Gestione dei tipi di pubblico di remarketing dinamico](audience-dynamic-remarketing-manage.md)
>* [Gestione dei target del pubblico per campagne e gruppi di annunci](audience-targets-manage.md)
>* [Gestire le esclusioni di pubblico per campagne e gruppi di annunci](audience-exclusions-manage.md)
