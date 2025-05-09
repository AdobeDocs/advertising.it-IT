---
title: Configurare test A/B per Adobe Advertising Search, Social e Commerce Ads in Adobe Target
description: Scopri come impostare un test A/B in [!DNL Target] per [!DNL Google Ads] e [!DNL Microsoft Advertising] annunci in Search, Social e Commerce.
exl-id: 564c7d61-beec-40cf-ac68-83d1e87e3008
source-git-commit: 26a4451fb09f2a42ac60ba123ddf0cf38323312d
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 0%

---

# Configurare i test A/B in Adobe Target per Advertising Search, Social e Commerce Ads

*Inserzionisti solo con Advertising Search, Social e Commerce*

Solo *[!DNL Google Ads]e [!DNL Microsoft Advertising] account*

Adobe Advertising e Adobe Target semplificano la configurazione dei test A/B di esperienza pagina di destinazione per il traffico pubblicitario digitale [!DNL Google Ads] e [!DNL Microsoft Advertising] in:

* Migliorare i tassi di conversione (CVR) e le misure di efficienza di acquisizione (come CPA, CPL e CAC).

* Fornisci un’esperienza di pagina di destinazione più personalizzata che sia rilevante per l’annuncio (ad esempio, abbinare l’immagine o il video creativo, la copia, la parola chiave o altro segnale pubblicitario alla pagina di destinazione).

Puoi anche combinare le dimensioni native [[!DNL Analytics] per Advertising](/help/integrations/analytics/overview.md) e [[!DNL Analytics] per il reporting dell&#39;integrazione  [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) integrate in Adobe Analytics per misurare e visualizzare i dati di test con [!DNL Analytics] metriche ed eventi di successo.

Vedere le sezioni seguenti per i prerequisiti, le istruzioni per impostare test A/B in [!DNL Target] per il traffico click-through da annunci in Search, Social e Commerce e i suggerimenti su come misurare e visualizzare i test in [!DNL Analytics].

## Prerequisiti

### Prodotti richiesti

* Ricerca, social e Commerce
* [!DNL Target]

### Prodotti e integrazioni consigliati

* [!DNL Analytics]

* [[!DNL Analytics] per l&#39;integrazione con Advertising](/help/integrations/analytics/overview.md)<!-- necessary for testing view-throughs, which most advertisers want to do -->

* Integrazione di [[!DNL Analytics] for [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)

## Passaggio 1: creare un&#39;attività di test A/B in [!DNL Target] per Search, Social e Commerce

Le istruzioni seguenti evidenziano le informazioni relative al caso d’uso Ricerca, Social e Commerce.

1. [Accedi ad Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html).

1. [Creare un test A/B](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html):

   1. Nel campo **[!UICONTROL Enter Activity URL]**, immetti l&#39;URL della pagina di destinazione per il test.

   1. Nel campo **[!UICONTROL Goal]**, immettere la metrica di successo per il test.

      >[!NOTE]
      >
      >Assicurarsi che [!DNL Analytics] sia abilitato come origine dati in [!DNL Target] e che sia selezionata la suite di rapporti corretta.

   1. Impostare **[!UICONTROL Priority]** su `High` o `999` per evitare conflitti quando gli utenti nel segmento di test ricevono un&#39;esperienza nel sito non corretta.


   1. In **[!UICONTROL Reporting Settings]**, seleziona **[!UICONTROL Company Name]** e **[!UICONTROL Report Suite]** connessi al tuo account Search, Social e Commerce.

      Per ulteriori suggerimenti sul reporting, consulta &quot;[Best practice per il reporting e risoluzione dei problemi](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html).&quot;

   1. Nel campo **[!UICONTROL Date Range]** immettere le date di inizio e di fine appropriate per il test.

   1. Selezionare **[!UICONTROL Site Pages]** > **[!UICONTROL Landing Page]** > **[!UICONTROL Query]**. Nel campo **[!UICONTROL Value]**, immettere [!UICONTROL Network Account ID], [!UICONTROL Network Campaign ID], [!UICONTROL Network Adgroup ID] o [!UICONTROL Network Ad ID] per l&#39;entità di rete pubblicitaria rilevante in Search, Social e Commerce. Questo consente di utilizzare i parametri della stringa di query [!DNL Target] per i tipi di pubblico di click-through per l&#39;entità.

      Per trovare l&#39;ID, [aggiungi la colonna ID pertinente alla vista entità](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md).

      Colonna ![[!UICONTROL Network Account ID] nella visualizzazione [!UICONTROL Accounts]](/help/integrations/assets/target-search-id.png "[!UICONTROL Network Account ID] nella visualizzazione [!UICONTROL Accounts]")

      Se hai bisogno di assistenza, contatta il team del tuo account Adobe.

   1. Per **[!UICONTROL Traffic Allocation Method]**, seleziona **[!UICONTROL Manual (Default)]** e suddivide il pubblico 50/50.

   1. Salva l’attività.

1. Utilizza [Compositore esperienza visivo di Target](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html) per apportare modifiche di progettazione al modello della pagina di destinazione per test A/B.

   * Esperienza A: non modificare perché è l’esperienza predefinita/controlla la pagina di destinazione senza personalizzazione.

   * Esperienza B: utilizza l&#39;interfaccia utente [!DNL Target] per personalizzare il modello della pagina di destinazione in base alle risorse incluse nel test (ad esempio titoli, copia, posizionamento dei pulsanti e creatività).

   >[!NOTE]
   >
   >Ad esempio, in caso di utilizzo di test creativi, contatta il team del tuo account Adobe.

## Passaggio 2: configurare l&#39;Analysis Workspace [!DNL Analytics for Target] in [!DNL Analytics]

[!DNL Analytics for Target] (A4T) è un&#39;integrazione tra soluzioni che consente agli inserzionisti di creare attività [!DNL Target] basate su metriche di conversione e segmenti di pubblico di [!DNL Analytics] e quindi di misurare i risultati utilizzando [!DNL Analytics] come origine per la generazione di rapporti. Tutti i report e le segmentazioni per tale attività si basano sulla raccolta dati [!DNL Analytics].

Per ulteriori informazioni su [!DNL Analytics for Target], incluso un collegamento alle istruzioni di implementazione, vedere &quot;[Adobe Analytics come origine per la generazione di rapporti per Adobe Target (A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)&quot;.

### Configura il pannello [!DNL Analytics for Target]

In Analysis Workspace, configura [!DNL Analytics for Target panel] per analizzare le attività e le esperienze [!DNL Target]. Tieni presente i seguenti punti importanti e le informazioni sui tuoi rapporti.

#### Metriche

* Crea un pannello nell&#39;area di lavoro specifico per l&#39;account Adobe Advertising, la campagna o il gruppo di annunci<!-- only applicable entities? --> per cui è stato eseguito il test. Utilizzare le visualizzazioni di riepilogo per visualizzare le metriche di Adobe Advertising nello stesso rapporto delle prestazioni del test [!DNL Target].

* Dai priorità utilizzando le metriche nel sito (come visite e conversioni) per misurare le prestazioni.

* Le metriche multimediali aggregate da Adobe Advertising (come impression, clic e costi) non possono corrispondere alle metriche [!DNL Target].

#### Dimensioni

Le dimensioni seguenti si riferiscono a [!DNL Analytics for Target]:

* **Attività Target**: nome del test A/B

* **Esperienze Target**: nomi delle esperienze di pagina di destinazione utilizzate nell&#39;attività

* **Attività Target** > **Esperienza**: nome dell&#39;attività e nome dell&#39;esperienza nella stessa riga

### Risoluzione dei problemi di Analytics per i dati [!DNL Target]

In Analysis Workspace, se noti che i dati di attività ed esperienze sono minimi o non vengono popolati, effettua le seguenti operazioni:

* Verificare che lo stesso [!UICONTROL Supplemental Data ID] (SDID) sia utilizzato per [!DNL Target] e [!DNL Analytics]. Puoi verificare i valori SDID utilizzando [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html) nella pagina di destinazione in cui la campagna guida gli utenti.

[Valori di Supplemental Data ID (SDID) in Adobe Debugger](/help/integrations/assets/target-troubleshooting-sdid.png)

* Nella stessa pagina di destinazione, verifica che a) il [!UICONTROL Hostname] visualizzato in Adobe Debugger in [!UICONTROL Solutions] > [!UICONTROL Target] corrisponda a b) il [!UICONTROL Tracking Server] visualizzato in [!DNL Target] per l&#39;attività (in [!UICONTROL Goals & Settings] > [!UICONTROL Reporting Settings]).

  [!DNL Analytics For Target] richiede l&#39;invio di un server di monitoraggio [!DNL Analytics] nelle chiamate da [!DNL Target] al server di raccolta dati [!DNL Modstats] per Analytics.<!-- just "to Analytics?"-->

[Valore Hostname in Adobe Debugger](/help/integrations/assets/target-troubleshooting-hostname.png)

[Valore del server di tracciamento in Target](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## Letture ulteriori

* [Integrare Target con Analytics](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html) - Spiega come impostare il reporting di [!DNL Target] in Analysis Workspace.
* [Panoramica test A/B](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html): descrive le attività test A/B, utilizzabili con annunci Search, Social e Commerce.
* [Panoramica di Analytics per Advertising](/help/integrations/analytics/overview.md) - Introduce Analytics per Advertising, che consente di tenere traccia delle interazioni del sito click-through e view-through nelle istanze di Analytics.

>[!MORELIKETHIS]
>
>* [Configurare i test A/B in Adobe Target per Advertising DSP Ads](ab-tests-dsp.md)
