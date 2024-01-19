---
title: Configurare test A/B per annunci Search, Social e Commerce in Adobi Advertising Adobe Target
description: Scopri come impostare un test A/B in [!DNL Target] per [!DNL Google Ads] e [!DNL Microsoft® Advertising] annunci in Search, Social e Commerce.
exl-id: 564c7d61-beec-40cf-ac68-83d1e87e3008
source-git-commit: b94541bf8675d535b2f19b26c05235eb56bc6c0b
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 0%

---

# Configurare i test A/B in Adobe Target per annunci pubblicitari, social e commerce

*Inserzionisti solo con Advertising Search, Social e Commerce*

*[!DNL Google Ads]e [!DNL Microsoft® Advertising] solo account*

Adobi Advertising e Adobe Target semplificano la configurazione dei test A/B di esperienza della pagina di destinazione per il traffico pubblicitario digitale [!DNL Google Ads] e [!DNL Microsoft® Advertising] a:

* Migliorare i tassi di conversione (CVR) e le misure di efficienza di acquisizione (come CPA, CPL e CAC).

* Fornisci un’esperienza di pagina di destinazione più personalizzata che sia rilevante per l’annuncio (ad esempio, abbinare l’immagine o il video creativo, la copia, la parola chiave o altro segnale pubblicitario alla pagina di destinazione).

È inoltre possibile combinare [[!DNL Analytics] per la pubblicità](/help/integrations/analytics/overview.md) e [[!DNL Analytics] per [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) dimensioni di reporting per l’integrazione integrate in Adobe Analytics per misurare e visualizzare i dati di test con [!DNL Analytics] metriche ed eventi di successo.

Consulta le sezioni seguenti per i prerequisiti e le istruzioni per impostare i test A/B in [!DNL Target] per il traffico click-through da annunci in Search, Social e Commerce e suggerimenti su come misurare e visualizzare i test in [!DNL Analytics].

## Prerequisiti

### Prodotti richiesti

* Ricerca, social e commerce
* [!DNL Target]

### Prodotti e integrazioni consigliati

* [!DNL Analytics]

* [[!DNL Analytics] per la pubblicità](/help/integrations/analytics/overview.md) integrazione<!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics] per [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) integrazione

## Passaggio 1: creare un’attività di test A/B in [!DNL Target] per Ricerca, Social e Commerce

Le istruzioni seguenti evidenziano le informazioni relative al caso d’uso Ricerca, Social e Commerce.

1. [Accedere ad Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html).

1. [Creare un test A/B](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html):

   1. In **[!UICONTROL Enter Activity URL]** , immetti l’URL della pagina di destinazione per il test.

   1. In **[!UICONTROL Goal]** , immettere la metrica di successo per il test.

      >[!NOTE]
      >
      >Assicurati che [!DNL Analytics] è abilitato come origine dati in [!DNL Target]e che sia selezionata la suite di rapporti corretta.

   1. Imposta il **[!UICONTROL Priority]** a `High` o `999` per evitare conflitti quando gli utenti nel segmento di test ricevono un’esperienza on-site errata.


   1. Entro **[!UICONTROL Reporting Settings]**, seleziona la **[!UICONTROL Company Name]** e **[!UICONTROL Report Suite]** connessi al tuo account Search, Social &amp; Commerce.

      Per ulteriori suggerimenti sul reporting, consulta &quot;[Best practice per il reporting e la risoluzione dei problemi](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html).&quot;

   1. In **[!UICONTROL Date Range]** immettere le date di inizio e di fine appropriate per il test.

   1. Seleziona **[!UICONTROL Site Pages]** > **[!UICONTROL Landing Page]** > **[!UICONTROL Query]**. In **[!UICONTROL Value]** , immettere il [!UICONTROL Network Account ID], [!UICONTROL Network Campaign ID], [!UICONTROL Network Adgroup ID], o [!UICONTROL Network Ad ID] per l’entità pertinente della rete di annunci in Search, Social &amp; Commerce. Questo consente di utilizzare il [!DNL Target] parametri della stringa di query per i tipi di pubblico di click-through per l’entità.

      Per trovare l’ID, utilizza [aggiunta della colonna ID rilevante alla vista entità](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md).

      ![[!UICONTROL Network Account ID] colonna nella [!UICONTROL Accounts] visualizza](/help/integrations/assets/target-search-id.png "[!UICONTROL Network Account ID] colonna nella [!UICONTROL Accounts] visualizza")

      Se hai bisogno di assistenza, rivolgiti al team del tuo account Adobe.

   1. Per **[!UICONTROL Traffic Allocation Method]**, seleziona **[!UICONTROL Manual (Default)]** e dividere il pubblico 50/50.

   1. Salva l’attività.

1. Utilizzare [Compositore esperienza visivo di Target](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html) per apportare modifiche di progettazione al modello della pagina di destinazione per i test A/B.

   * Esperienza A: non modificare perché è l’esperienza predefinita/controlla la pagina di destinazione senza personalizzazione.

   * Esperienza B: Utilizzare [!DNL Target] interfaccia utente per personalizzare il modello della pagina di destinazione in base alle risorse incluse nel test (ad esempio titoli, copia, posizionamento dei pulsanti e creatività).

   >[!NOTE]
   >
   >Ad esempio, in caso di utilizzo di test creativi, contatta il team del tuo account Adobe.

## Passaggio 2: configurare [!DNL Analytics for Target] Analysis Workspace in [!DNL Analytics]

[!DNL Analytics for Target] (A4T) è un’integrazione tra soluzioni che consente agli inserzionisti di creare [!DNL Target] attività basate su [!DNL Analytics] metriche di conversione e segmenti di pubblico, quindi misurare i risultati utilizzando [!DNL Analytics] come origine per la generazione di rapporti. Tutti i rapporti e le segmentazioni per tale attività si basano su [!DNL Analytics] raccolta dati.

Per ulteriori informazioni su [!DNL Analytics for Target], compreso un collegamento alle istruzioni di implementazione, consulta &quot;[Adobe Analytics come origine per la generazione di rapporti per Adobe Target (A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)&quot;.

### Configurare [!DNL Analytics for Target] Pannello

In Analysis Workspace, configura il [!DNL Analytics for Target panel] per analizzare [!DNL Target] attività ed esperienze. Tieni presente i seguenti punti importanti e le informazioni sui tuoi rapporti.

#### Metriche

* Crea un pannello all’interno dell’area di lavoro specifico per l’account, la campagna o il gruppo di annunci di Adobe Advertising<!-- only applicable entities? --> per il quale è stato eseguito il test. Utilizza le visualizzazioni di riepilogo per mostrare metriche Adobi Advertising nello stesso rapporto della [!DNL Target] prestazioni del test.

* Dai priorità utilizzando le metriche nel sito (come visite e conversioni) per misurare le prestazioni.

* Scopri che le metriche dei contenuti multimediali aggregati da Adobi Advertising (come impression, clic e costi) non possono corrispondere a [!DNL Target] metriche.

#### Dimension

Le dimensioni seguenti riguardano: [!DNL Analytics for Target]:

* **Attività Target**: nome del test A/B

* **Esperienze Target**: nomi delle esperienze pagina di destinazione utilizzate nell’attività

* **Attività Target** > **Esperienza**: nome dell’attività e nome dell’esperienza nella stessa riga

### Risoluzione dei problemi di Analytics per [!DNL Target] Dati

In Analysis Workspace, se noti che i dati di attività ed esperienze sono minimi o non vengono popolati, effettua le seguenti operazioni:

* Verifica che lo stesso [!UICONTROL Supplemental Data ID] (SDID) viene utilizzato per entrambi [!DNL Target] e [!DNL Analytics]. Puoi verificare i valori SDID utilizzando [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html) nella pagina di destinazione a cui la campagna indirizza gli utenti.

[Valori di Supplemental Data ID (SDID) in Adobe Debugger](/help/integrations/assets/target-troubleshooting-sdid.png)

* Nella stessa pagina di destinazione, verifica che a) il [!UICONTROL Hostname] mostrato nell’Adobe Debugger in [!UICONTROL Solutions] > [!UICONTROL Target] corrisponde a b) il [!UICONTROL Tracking Server] mostrato in [!DNL Target] per l&#39;attività (sotto [!UICONTROL Goals & Settings] > [!UICONTROL Reporting Settings]).

  [!DNL Analytics For Target] richiede un [!DNL Analytics] server di tracciamento da inviare nelle chiamate da [!DNL Target] al [!DNL Modstats] server di raccolta dati per Analytics.<!-- just "to Analytics?"-->

[Valore Hostname in Adobe Debugger](/help/integrations/assets/target-troubleshooting-hostname.png)

[Valore del server di tracciamento in Target](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## Letture ulteriori

* [Integrare Target con Analytics](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html) - Spiega come impostare [!DNL Target] reporting in Analysis Workspace.
* [Panoramica sui test A/B](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html) : descrive le attività di test A/B, che puoi utilizzare con annunci Search, Social e Commerce.
* [Panoramica di Analytics for Advertising](/help/integrations/analytics/overview.md) - Introduce Analytics for Advertising, che consente di monitorare le interazioni click-through e view-through nel sito nelle istanze Analytics.

>[!MORELIKETHIS]
>
>* [Configurare i test A/B in Adobe Target per la pubblicità degli annunci DSP](ab-tests-dsp.md)
