---
title: Configurare test A/B per Adobe Advertising DSP Ads in Adobe Target
description: Scopri come impostare un test A/B in [!DNL Target] per i tuoi annunci DSP.
exl-id: 5092e06b-eef0-43f3-ba81-6dbe7164158c
source-git-commit: 26a4451fb09f2a42ac60ba123ddf0cf38323312d
workflow-type: tm+mt
source-wordcount: '1413'
ht-degree: 0%

---

# Configurare i test A/B in Adobe Target per Advertising DSP Ads

*Inserzionisti con solo Advertising DSP*

Adobe Advertising e Adobe Target consentono agli esperti di marketing di fornire un’esperienza personalizzata e connessa tramite contenuti multimediali a pagamento e messaggi sul sito in modo ancora più semplice. Condividendo i segnali tra i prodotti, puoi:

* Diminuire i tassi di abbandono dei siti collegando l’esposizione degli annunci dei clienti dalle campagne DSP alle loro esperienze sul sito.

* Stabilisci un test A/B rispecchiando le esperienze sul sito con i messaggi pubblicitari utilizzando i dati di esposizione di Adobe Audience Manager e i tipi di pubblico [!DNL Target] con alimentazione tramite clic.

* Misura l&#39;impatto della messaggistica unificata su un incremento oggettivo nel sito con semplici visualizzazioni in Adobe Analytics per [!DNL Target].

Vedere le sezioni seguenti per i prerequisiti e per le istruzioni su come impostare il tracciamento dei click-through e del view-through, implementare la condivisione del segnale tra DSP e [!DNL Target], impostare un&#39;attività di test A/B e configurare [!DNL Analytics] Analysis Workspace per visualizzare i dati di test.

Per ulteriori domande, contatta adcloud_support@adobe.com.

## Prerequisiti

Questo caso d’uso richiede i seguenti prodotti e integrazioni:

* [!DNL Target]

* [[!DNL Analytics] per l&#39;integrazione con Advertising](/help/integrations/analytics/overview.md)<!-- necessary for testing view-throughs, which most advertisers want to do -->

* Integrazione di [[!DNL Analytics] for [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=it)

* Audience Manager (richiesto solo per il test view-through)

## Passaggio 1: configurare il framework di click-through {#click-through-framework}

![Framework click-through](/help/integrations/assets/target-ct-framework.png)

Quando aggiungi macro DSP a un URL di click-through (l&#39;URL visualizzato quando un utente fa clic su un annuncio e raggiunge la pagina di destinazione), DSP acquisisce automaticamente la chiave di posizionamento includendo `${TM_PLACEMENT_ID}` nell&#39;URL di click-through. Questa macro acquisisce la chiave di posizionamento alfanumerica e non l’ID di posizionamento numerico.

![URL click-through aggiunto all&#39;URL della pagina di destinazione](/help/integrations/assets/target-ct-url.jpg)

### (Solo DSP) Aggiungi macro DSP agli URL di click-through

<!-- If we ever write instructions for ads on other ad servers (such as Sizmek ads in DCO), then work that into the following section. -->

In [!DNL Flashtalking] o Google Campaign Manager 360, aggiorna manualmente l’URL di click-through per ogni annuncio in modo da includere le macro necessarie per acquisire le variabili AMO ID. Le variabili AMO ID vengono utilizzate per inviare i dati dei clic ad Adobe Analytics e per condividere le chiavi di posizionamento per il test A/B. Per istruzioni, vedere le pagine seguenti:

* [Aggiungi [!DNL Analytics for Advertising] Macro ai [!DNL Flashtalking] Tag annuncio](/help/integrations/analytics/macros-flashtalking.md). **Nota:** questa procedura non è necessaria se l&#39;organizzazione ha una relazione diretta con [!DNL Flashtalking] e si utilizzano macro di passaggio dati per tenere traccia dei parametri di tracciamento di `s_kwcid` e `ef_id` in base alla documentazione di supporto di [!DNL Flashtalking] all&#39;indirizzo [https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros](https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros).

* [Aggiungi [!DNL Analytics for Advertising] macro ai [!DNL Google Campaign Manager 360] tag annuncio](/help/integrations/analytics/macros-google-campaign-manager.md)

Contatta il tuo Adobe Account Team e Advertising Solutions Group (aac-advertising-solutions-group@adobe.com) per recuperare la chiave di posizionamento richiesta e finalizzare la configurazione e per assicurarti che ogni URL di click-through sia compilato con la chiave di posizionamento.

## Passaggio 2: configurare il framework view-through con Audience Manager {#view-through-framework}

![Framework di visualizzazione](/help/integrations/assets/targetr-vt-framework.png)

Aggiungendo un pixel evento di impression di Audience Manager nei tag annuncio e nelle impostazioni di posizionamento, puoi creare un segmento di test per ulteriori opportunità di test view-through.

1. Implementa un pixel evento di impression di Audience Manager nei tag pubblicitari e nelle impostazioni di posizionamento di DSP.

   Per istruzioni, consulta &quot;[Raccogliere dati sull&#39;esposizione multimediale dalle campagne Advertising DSP](/help/integrations/audience-manager/media-data-integration/collect.md).&quot;

   Accertati di aggiungere [macro DSP](/help/dsp/campaign-management/macros.md) per acquisire tutti i dati di cui vuoi che il pixel dell&#39;evento di impression ritorni, inclusi `${TM_PLACEMENT_ID_NUM}` per l&#39;ID di posizionamento numerico.

   >[!NOTE]
   >
   >Gli URL di tracciamento dei clic includono la macro `${TM_PLACEMENT_ID}` per la chiave di posizionamento alfanumerica, invece di `${TM_PLACEMENT_ID_NUM}` per l’ID di posizionamento numerico.

1. Configura un segmento di Audience Manager dai dati delle impression di DSP:

   1. Verifica che i dati del segmento siano disponibili:

      1. [Cerca il segnale](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-signals-search.html?lang=it) per la [coppia chiave-valore](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-search-pairs.html?lang=it) che determina il livello di raggruppamento degli utenti del segmento.

         Utilizza una [chiave supportata](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html?lang=it) con un valore corrispondente a una macro aggiunta al pixel dell&#39;evento di Audience Manager impression.

         Ad esempio, per raggruppare gli utenti per un particolare posizionamento, utilizza la chiave `d_placement`. Per il valore, utilizzare un ID di posizionamento numerico effettivo (ad esempio 2501853) acquisito dalla macro DSP `${TM_PLACEMENT_ID_NUM}`. <!-- Explain where to find the placement ID, other than in a custom report. -->

         Se i risultati della ricerca mostrano i conteggi degli utenti per la coppia chiave-valore, che indica che il pixel è stato posizionato correttamente e i dati scorrono, continua con il passaggio successivo.

   1. [Crea una caratteristica basata su regole](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html?lang=it) per la creazione di segmenti in Audience Manager.

      * Denomina la caratteristica in modo che sia facilmente identificabile nelle attività di test. Memorizza la caratteristica nella cartella preferita.

      * Seleziona `Ad Cloud` come **[!UICONTROL Data Source]**.

      * Per l&#39;espressione della caratteristica, utilizzare `d_event` come **[!UICONTROL Key]** e `imp` come **[!UICONTROL Value]**.

   1. [Configura un segmento di test](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segment-builder.html?lang=it) per la nuova caratteristica in Audience Manager, selezionando `Ad Cloud` come **[!UICONTROL Data Source]**.

      Audience Manager divide automaticamente il segmento in un gruppo di controllo che riceve l’esperienza della pagina di destinazione standard e in un gruppo di test che riceve un’esperienza personalizzata nel sito.

## Passaggio 3: configurare un&#39;attività test A/B in [!DNL Target] per DSP

Le istruzioni seguenti evidenziano le informazioni relative al caso di utilizzo di DSP.

1. [Accedi ad Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html?lang=it).

1. [Creare un test A/B](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html?lang=it):

   1. Nel campo **[!UICONTROL Enter Activity URL]**, immetti l&#39;URL della pagina di destinazione per il test.

      >[!NOTE]
      >
      >Puoi utilizzare più URL per testare la voce del sito view-through. Per ulteriori informazioni, vedere &quot;[Attività multipagina](https://experienceleague.adobe.com/docs/target/using/experiences/vec/multipage-activity.html?lang=it).&quot; È possibile identificare facilmente le voci principali in base all&#39;URL della pagina creando un [rapporto sulle voci del sito](https://experienceleague.adobe.com/it/docs/analytics-learn/tutorials/integrations/adobe-advertising-dsp/create-advertising-cloud-site-entry-reports) in Analytics.

   1. Nel campo **[!UICONTROL Goal]**, immettere la metrica di successo per il test.

      >[!NOTE]
      >
      >Assicurarsi che [!DNL Analytics] sia abilitato come origine dati in [!DNL Target] e che sia selezionata la suite di rapporti corretta.

   1. Impostare **[!UICONTROL Priority]** su `High` o `999` per evitare conflitti quando gli utenti nel segmento di test ricevono un&#39;esperienza nel sito non corretta.

   1. In **[!UICONTROL Reporting Settings]**, seleziona **[!UICONTROL Company Name]** e **[!UICONTROL Report Suite]** connessi al tuo account DSP.

      Per ulteriori suggerimenti sul reporting, consulta &quot;[Best practice per il reporting e risoluzione dei problemi](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html?lang=it).&quot;

   1. Nel campo **[!UICONTROL Date Range]** immettere le date di inizio e di fine appropriate per il test.

   1. Aggiungi tipi di pubblico all’attività:

      1. Scegli il [segmento creato in precedenza in Audience Manager per testare i tipi di pubblico view-through](#view-through-framework).

      1. Seleziona **[!UICONTROL Site Pages]** > **[!UICONTROL Landing Page]** > **[!UICONTROL Query]** e immetti la chiave di posizionamento DSP nel campo **[!UICONTROL Value]** per utilizzare i parametri della stringa di query Target per i tipi di pubblico di click-through.

   1. Per **[!UICONTROL Traffic Allocation Method]**, seleziona **[!UICONTROL Manual (Default)]** e suddivide il pubblico 50/50.

   1. Salva l’attività.

1. Utilizza [Compositore esperienza visivo di Target](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html?lang=it) per apportare modifiche di progettazione al modello della pagina di destinazione per test A/B.

   * Esperienza A: non modificare perché è l’esperienza predefinita/controlla la pagina di destinazione senza personalizzazione.

   * Esperienza B: utilizza l&#39;interfaccia utente [!DNL Target] per personalizzare il modello della pagina di destinazione in base alle risorse incluse nel test (ad esempio titoli, copia, posizionamento dei pulsanti e creatività).

   >[!NOTE]
   >
   >Ad esempio, in caso di utilizzo di test creativi, contatta il team del tuo account Adobe.

## Passaggio 4: configurare l&#39;Analysis Workspace [!DNL Analytics for Target] in [!DNL Analytics]

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

[!DNL Analytics for Target] (A4T) è un&#39;integrazione tra soluzioni che consente agli inserzionisti di creare attività [!DNL Target] basate su metriche di conversione e segmenti di pubblico di [!DNL Analytics] e quindi di misurare i risultati utilizzando [!DNL Analytics] come origine per la generazione di rapporti. Tutti i report e le segmentazioni per tale attività si basano sulla raccolta dati [!DNL Analytics].

Per ulteriori informazioni su [!DNL Analytics for Target], incluso un collegamento alle istruzioni di implementazione, vedere &quot;[Adobe Analytics come origine per la generazione di rapporti per Adobe Target (A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=it)&quot;.

### Configura il pannello [!DNL Analytics for Target]

In Analysis Workspace, configura [!DNL Analytics for Target panel] per analizzare le attività e le esperienze [!DNL Target]. Tieni presente i seguenti punti importanti e le informazioni sui tuoi rapporti.

#### Metriche

* Crea un pannello all’interno dell’area di lavoro specifica per la campagna, il pacchetto o il posizionamento Adobe Advertising per cui è stato eseguito il test. Utilizzare le visualizzazioni di riepilogo per visualizzare le metriche di Adobe Advertising nello stesso rapporto delle prestazioni del test [!DNL Target].

* Dai priorità utilizzando le metriche nel sito (come visite e conversioni) per misurare le prestazioni.

* Le metriche multimediali aggregate da Adobe Advertising (come impression, clic e costi) non possono corrispondere alle metriche [!DNL Target].

#### Dimensioni

Le dimensioni seguenti si riferiscono a [!DNL Analytics for Target]:

* **[!UICONTROL Target Activities]**: nome del test A/B

* **[!UICONTROL Target Experiences]**: nomi delle esperienze della pagina di destinazione utilizzate nell&#39;attività

* **[!UICONTROL Target Activity]** > **[!UICONTROL Experience]**: il nome dell&#39;attività e dell&#39;esperienza nella stessa riga

### Risoluzione dei problemi di Analytics per i dati [!DNL Target]

In Analysis Workspace, se noti che i dati di attività ed esperienze sono minimi o non vengono popolati, effettua le seguenti operazioni:

* Verificare che lo stesso [!UICONTROL Supplemental Data ID] (SDID) sia utilizzato per [!DNL Target] e [!DNL Analytics]. Puoi verificare i valori SDID utilizzando [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html?lang=it) nella pagina di destinazione in cui la campagna guida gli utenti.

[Valori di Supplemental Data ID (SDID) in Adobe Debugger](/help/integrations/assets/target-troubleshooting-sdid.png)

* Nella stessa pagina di destinazione, verifica che a) il [!UICONTROL Hostname] visualizzato in Adobe Debugger in [!UICONTROL Solutions] > [!UICONTROL Target] corrisponda a b) il [!UICONTROL Tracking Server] visualizzato in [!DNL Target] per l&#39;attività (in [!UICONTROL Goals & Settings] > [!UICONTROL Reporting Settings]).

  [!DNL Analytics For Target] richiede l&#39;invio di un server di monitoraggio [!DNL Analytics] nelle chiamate da [!DNL Target] al server di raccolta dati [!DNL Modstats] per Analytics.<!-- just "to Analytics?"-->

[Valore Hostname in Adobe Debugger](/help/integrations/assets/target-troubleshooting-hostname.png)

[Valore del server di tracciamento in Target](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## Letture ulteriori

* [Integrare Target con Analytics](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html?lang=it) - Spiega come impostare il reporting di [!DNL Target] in Analysis Workspace.
* [Panoramica test A/B](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html?lang=it): descrive le attività test A/B, utilizzabili con gli annunci DSP.
* [Esperienze e offerte](https://experienceleague.adobe.com/docs/target/using/experiences/experiences.html?lang=it) - Illustra [!DNL Target] strumenti per determinare il contenuto nel sito a cui sono esposti gli utenti di test di DSP.
* [Segnali, caratteristiche e segmenti](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/signal-trait-segment.html?lang=it): definisce alcuni degli strumenti di Audience Manager che possono essere utili per il test view-through di DSP.
* [Panoramica di Analytics per Advertising](/help/integrations/analytics/overview.md) - Introduce Analytics per Advertising, che consente di tenere traccia delle interazioni del sito click-through e view-through nelle istanze di Analytics.

>[!MORELIKETHIS]
>
>* [Configurare i test A/B in Adobe Target per Advertising Search, Social e Commerce Ads](ab-tests-search.md)
