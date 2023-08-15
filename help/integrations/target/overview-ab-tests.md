---
title: Configurare test A/B per annunci Adobi Advertising in Adobe Target
description: Scopri come impostare un test A/B in [!DNL Target] per i tuoi annunci DSP.
exl-id: 5092e06b-eef0-43f3-ba81-6dbe7164158c
source-git-commit: 1dbe8da7122b38dd11a242c453d71a832b31eee8
workflow-type: tm+mt
source-wordcount: '1551'
ht-degree: 0%

---

# Configurare i test A/B in Adobe Target per la pubblicità degli annunci DSP

<!-- In title and Heading1:  DSP and [!DNL Advertising Search, Social, & Commerce] Ads -->

<!-- Add [!UICONTROL and [!DNL tags throughout as needed. -->

<!-- Break into sub-files, or just leave as one? -->

*Inserzionisti solo con Advertising DSP*

Adobi Advertising e Adobe Target consentono agli esperti di marketing di fornire un’esperienza personalizzata e connessa tramite contenuti multimediali a pagamento e messaggi sul sito in modo ancora più semplice. Condividendo i segnali tra i prodotti, puoi:

* Diminuire i tassi di abbandono dei siti collegando l’esposizione degli annunci dei clienti dalle campagne DSP alle loro esperienze sul sito.

* Stabilisci un test A/B rispecchiando le esperienze sul sito con i messaggi pubblicitari utilizzando i dati di esposizione di Adobe Audience Manager e i tipi di pubblico di Target con alimentazione tramite clic.

* Misura l’impatto della messaggistica unificata su un incremento oggettivo nel sito con semplici visualizzazioni in Adobe Analytics per [!DNL Target].

Consulta le sezioni seguenti per i prerequisiti e per le istruzioni su come impostare il tracciamento click-through e view-through, implementare la condivisione del segnale tra DSP e [!DNL Target] e configurare un’attività di test A/B e [!DNL Analytics] Analysis Workspace per visualizzare i dati di test.

Per ulteriori domande, contatta adcloud_support@adobe.com.

## Prerequisiti

Questo caso d’uso richiede i seguenti prodotti e integrazioni:

* [!DNL Target]

* [[!DNL Analytics] per la pubblicità](/help/integrations/analytics/overview.md) integrazione<!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics] per [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) integrazione

* Audience Manager (richiesto solo per il test view-through)

## Passaggio 1: configurare il framework di click-through {#click-through-framework}

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

![Framework di click-through](/help/integrations/assets/target-ct-framework.png)

Quando aggiungi macro DSP a un URL di click-through (l’URL visualizzato quando un utente fa clic su un annuncio e raggiunge la pagina di destinazione), l’DSP acquisisce automaticamente la chiave di posizionamento includendo `${TM_PLACEMENT_ID}` nell’URL di click-through. Questa macro acquisisce la chiave di posizionamento alfanumerica e non l’ID di posizionamento numerico.

![URL di click-through aggiunto all’URL della pagina di destinazione](/help/integrations/assets/target-ct-url.jpg)

### (Solo DSP) Aggiungi macro DSP agli URL di click-through

<!-- If we ever write instructions for ads on other ad servers (such as Sizmek ads in DCO), then work that into the following section. -->

All’interno di Flash Talk o Google Campaign Manager 360, aggiorna manualmente l’URL di click-through per ogni annuncio in modo da includere le macro necessarie per acquisire le variabili AMO ID. Le variabili AMO ID vengono utilizzate per inviare i dati dei clic ad Adobe Analytics e per condividere le chiavi di posizionamento per il test A/B. Per istruzioni, vedere le pagine seguenti:

* [Aggiungi [!DNL Analytics for Advertising] Macro per [!DNL Flashtalking] Tag annuncio](/help/integrations/analytics/macros-flashtalking.md)

* [Aggiungi [!DNL Analytics for Advertising] Macro per [!DNL Google Campaign Manager 360] Tag annuncio](/help/integrations/analytics/macros-google-campaign-manager.md)

Contatta il tuo Adobe Account Team e Advertising Solutions Group (aac-advertising-solutions-group@adobe.com) per recuperare la chiave di posizionamento richiesta e finalizzare la configurazione e per assicurarti che ogni URL di click-through sia popolato con la chiave di posizionamento.

## Passaggio 2: configurare il framework view-through utilizzando l&#39;Audience Manager {#view-through-framework}

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

![Framework view-through](/help/integrations/assets/targetr-vt-framework.png)

Aggiungendo un pixel evento di impression di Audience Manager nei tag dell’annuncio e nelle impostazioni di posizionamento, puoi creare un segmento di test per ulteriori opportunità di test view-through.

1. Implementa un pixel Audience Manager di evento di impression nei tag degli annunci e nelle impostazioni di posizionamento DSP.

   Per le istruzioni del caso, vedere &quot;[Raccogliere dati sull’esposizione multimediale dalle campagne pubblicitarie DSP](/help/integrations/audience-manager/media-data-integration/collect.md).&quot;

   Assicurati di aggiungere [Macro per DSP](/help/dsp/campaign-management/macros.md) per acquisire tutti i dati di cui vuoi che il pixel dell’evento di impression ritorni, tra cui `${TM_PLACEMENT_ID_NUM}` ID di posizionamento numerico.

   >[!NOTE]
   >
   >Gli URL di tracciamento dei clic includono `${TM_PLACEMENT_ID}` macro per la chiave di posizionamento alfanumerica, anziché `${TM_PLACEMENT_ID_NUM}` ID di posizionamento numerico.

1. Configura un segmento di Audience Manager dai dati di impression dell’DSP:

   1. Verifica che i dati del segmento siano disponibili:

      1. [Ricerca del segnale](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-signals-search.html) per [coppia chiave-valore](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-search-pairs.html) che determina il livello di raggruppamento degli utenti del segmento.

         Utilizza un [chiave supportata](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html) con un valore che corrisponde a una macro aggiunta al pixel dell’evento di impression Audience Manager.

         Ad esempio, per raggruppare gli utenti per un posizionamento particolare, utilizza `d_placement` chiave. Per il valore, utilizzare un ID di posizionamento numerico effettivo (ad esempio 2501853) acquisito dalla macro DSP `${TM_PLACEMENT_ID_NUM}`. <!-- Explain where to find the placement ID, other than in a custom report. -->

         Se i risultati della ricerca mostrano i conteggi degli utenti per la coppia chiave-valore, che indica che il pixel è stato posizionato correttamente e i dati scorrono, continua con il passaggio successivo.

   1. [Creare una caratteristica basata su regole](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) per la creazione di segmenti in Audienci Manager.

      * Denomina la caratteristica in modo che sia facilmente identificabile nelle attività di test. Memorizza la caratteristica nella cartella preferita.

      * Seleziona `Ad Cloud` come **Origine dati**.

      * Per l’espressione della caratteristica, utilizza `d_event` come **Chiave** e `imp` come **Valore**.

   1. [Impostare un segmento di test](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segment-builder.html) per la nuova caratteristica in Audience Manager, seleziona `Ad Cloud` come **Origine dati**.

      Audienci Manager suddivide automaticamente il segmento in un gruppo di controllo che riceve l’esperienza di pagina di destinazione standard e in un gruppo di test che riceve un’esperienza personalizzata nel sito.

## Passaggio 3: configurare un’attività &quot;Test A/B&quot; in Target

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

Le istruzioni seguenti evidenziano informazioni relative al caso di utilizzo dell’DSP. Per istruzioni complete, vedere &quot;&quot;.

1. [Accedere ad Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html).

1. [Creare un test A/B](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html):

   1. In **Inserisci l’URL dell’attività** , immetti l’URL della pagina di destinazione per il test.

      >[!NOTE]
      >
      >Puoi utilizzare più URL per testare la voce del sito view-through. Per ulteriori informazioni, consulta la sezione &quot;[Attività multipagina](https://experienceleague.adobe.com/docs/target/using/experiences/vec/multipage-activity.html).&quot; È possibile identificare facilmente le voci principali per URL della pagina creando un [Rapporto sulle visite al sito](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/integrations/ad-cloud/create-advertising-cloud-site-entry-reports.html) in Analytics.

   1. In **Obiettivo** , immettere la metrica di successo per il test.

      >[!NOTE]
      >
      >Assicurati che [!DNL Analytics] è abilitato come origine dati in [!DNL Target]e che sia selezionata la suite di rapporti corretta.

   1. Imposta il **Priorità** a `High` o `999` per evitare conflitti quando gli utenti nel segmento di test ricevono un’esperienza on-site errata.

   1. Entro **Impostazioni di reporting**, seleziona la **Nome dell’azienda** e **Suite di rapporti** collegato al tuo account DSP.

      Per ulteriori suggerimenti sul reporting, consulta &quot;[Best practice per il reporting e la risoluzione dei problemi](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html).&quot;

   1. In **Intervallo date** immettere le date di inizio e di fine appropriate per il test.

   1. Aggiungi tipi di pubblico all’attività:

      1. Scegli la [segmento creato in precedenza in Audienci Manager per testare il pubblico view-through](#view-through-framework).

      1. Seleziona **Pagine del sito** > **Pagina di destinazione** > **Query** e immettere la chiave di posizionamento DSP nella **Valore** per utilizzare i parametri della stringa di query di Target per i tipi di pubblico di click-through.

   1. Per **Metodo di allocazione traffico**, seleziona **Manuale (impostazione predefinita)** e dividere il pubblico 50/50.

   1. Salva l’attività.

1. Utilizzare [!DNL Target] [Compositore esperienza visivo](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html) per apportare modifiche di progettazione al modello della pagina di destinazione per i test A/B.

   * Esperienza A: non modificare perché è l’esperienza predefinita/controlla la pagina di destinazione senza personalizzazione.

   * Esperienza B: Utilizzare [!DNL Target] interfaccia utente per personalizzare il modello della pagina di destinazione in base alle risorse incluse nel test (ad esempio titoli, copia, posizionamento dei pulsanti e creatività).

   >[!NOTE]
   >
   >Ad esempio, in caso di utilizzo di test creativi, contatta il team del tuo account Adobe.

## Passaggio 4: configurare [!DNL Analytics for Target] Analysis Workspace in [!DNL Analytics]

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

[!DNL Analytics for Target] (A4T) è un’integrazione tra soluzioni che consente agli inserzionisti di creare [!DNL Target] attività basate su [!DNL Analytics] metriche di conversione e segmenti di pubblico, quindi misurare i risultati utilizzando [!DNL Analytics] come origine per la generazione di rapporti. Tutti i rapporti e le segmentazioni per tale attività si basano su [!DNL Analytics] raccolta dati.

Per ulteriori informazioni su [!DNL Analytics for Target], compreso un collegamento alle istruzioni di implementazione, consulta &quot;[Adobe Analytics come origine per la generazione di rapporti per Adobe Target (A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)&quot;.

### Configurare [!DNL Analytics for Target] Pannello

In Analysis Workspace, configura il [!DNL Analytics for Target panel] per analizzare [!DNL Target] attività ed esperienze. Tieni presente i seguenti punti importanti e le informazioni sui tuoi rapporti.

#### Metriche

* Crea un pannello all’interno dell’area di lavoro specifico per la campagna di Adobi Advertising, il pacchetto o il posizionamento per cui è stato eseguito il test. Utilizza le visualizzazioni di riepilogo per mostrare le metriche Adobi Advertising nello stesso rapporto delle prestazioni del test di Target.

* Dai priorità utilizzando le metriche nel sito (come visite e conversioni) per misurare le prestazioni.

* Scopri che le metriche dei contenuti multimediali aggregati da Adobi Advertising (come impression, clic e costi) non possono corrispondere alle metriche di Target.

#### Dimension

Le dimensioni seguenti riguardano: [!DNL Analytics for Target]:

* **Attività Target**: nome del test A/B

* **Esperienze Target**: nomi delle esperienze pagina di destinazione utilizzate nell’attività

* **Attività Target** > **Esperienza**: nome dell’attività e nome dell’esperienza nella stessa riga

### Risoluzione dei problemi di Analytics per [!DNL Target] Dati

In Analysis Workspace, se noti che i dati di attività ed esperienze sono minimi o non vengono popolati, effettua le seguenti operazioni:

* Verifica che venga utilizzato lo stesso Supplemental Data ID (SDID) sia per Target che per Analytics. Puoi verificare i valori SDID utilizzando [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html) nella pagina di destinazione a cui la campagna indirizza gli utenti.

[Valori di Supplemental Data ID (SDID) in Adobe Debugger](/help/integrations/assets/target-troubleshooting-sdid.png)

* Nella stessa pagina di destinazione, verifica che a) il nome host mostrato nell’Adobe Debugger in Soluzioni> Target corrisponda a b) il tracking server mostrato in [!DNL Target] per l’attività (in Obiettivi e impostazioni > Impostazioni di reporting).

  [!DNL Analytics For Target] richiede un [!DNL Analytics] server di tracciamento da inviare nelle chiamate da [!DNL Target] al [!DNL Modstats] server di raccolta dati per Analytics.<!-- just "to Analytics?"-->

[Valore Hostname in Adobe Debugger](/help/integrations/assets/target-troubleshooting-hostname.png)

[Valore del server di tracciamento in Target](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## Letture ulteriori

* [Integrare Target con Analytics](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html)- Spiega come impostare la generazione rapporti di Target in Analysis Workspace.
* [Panoramica sui test A/B](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html) : descrive le attività di test A/B, che puoi utilizzare con gli annunci DSP.
* [Esperienze e offerte](https://experienceleague.adobe.com/docs/target/using/experiences/experiences.html) - Spiega [!DNL Target] strumenti per determinare il contenuto nel sito a cui sono esposti gli utenti dei test DSP.
* [Segnali, caratteristiche e segmenti](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/signal-trait-segment.html) : definisce alcuni degli strumenti di Audience Manager utili per i test view-through dell’DSP.
* [Panoramica di Analytics for Advertising](/help/integrations/analytics/overview.md) - Introduce Analytics for Advertising, che consente di monitorare le interazioni click-through e view-through nel sito nelle istanze Analytics.

<!-- 
>[!MORELIKETHIS]
>
>* 
-->
