---
title: Configurare test A/B per Adobe annunci pubblicitari in Adobe Target
description: Scopri come impostare un test A/B in [!DNL Target] per il tuo DSP e [!DNL Search, Social, & Commerce] annunci pubblicitari.
exl-id: 5092e06b-eef0-43f3-ba81-6dbe7164158c
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '1642'
ht-degree: 0%

---

# Configurare test A/B in Adobe Target per DSP pubblicitarie e [!DNL Advertising Search, Social, & Commerce] Annunci

<!-- Add [!UICONTROL and [!DNL tags throughout as needed. -->

<!-- Break into sub-files, or just leave as one? -->

*Advertising DSP solo*

Adobe Advertising e Adobe Target semplificano ulteriormente gli addetti al marketing per offrire un’esperienza personalizzata e connessa su supporti a pagamento e messaggi on-site. La condivisione di segnali tra i prodotti consente di:

* Riduce i tassi di abbandono del sito collegando l’esposizione degli annunci dei clienti dalle campagne DSP alle loro esperienze sul sito.

* Stabilisci test A/B eseguendo il mirroring delle esperienze sul sito con messaggi pubblicitari utilizzando i dati di esposizione di Adobe Audience Manager e i tipi di pubblico di Target con clic-to-feed.

* Misura l’impatto della messaggistica unificata su un incremento degli obiettivi in sito con visualizzazioni semplici in Adobe Analytics per [!DNL Target].

Consulta le sezioni seguenti per i prerequisiti e per le istruzioni su come impostare il tracciamento click-through e view-through, implementare la condivisione del segnale tra DSP e [!DNL Target] e configura un&#39;attività di test A/B e configura [!DNL Analytics] Analysis Workspace per visualizzare i dati del test.

Per ulteriori domande, contatta adcloud_support@adobe.com.

## Prerequisiti

Questo caso d’uso richiede i seguenti prodotti e integrazioni:

* [!DNL Target]

* [[!DNL Analytics] per la pubblicità](/help/integrations/analytics/overview.md) integrazione<!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics] per [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) integrazione

* Audience Manager (richiesto solo per il test view-through)

## Passaggio 1: Configurare il framework di click-through {#click-through-framework}

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

![Framework Click-through](/help/integrations/assets/target-ct-framework.png)

Quando si aggiungono DSP macro a un URL click-through (l&#39;URL visualizzato quando un utente fa clic su un annuncio e raggiunge la pagina di destinazione), DSP acquisisce automaticamente la chiave di posizionamento includendo `${TM_PLACEMENT_ID}` nell’URL di click-through. Questa macro acquisisce il tasto di posizionamento alfanumerico e non l’ID di posizionamento numerico.

![URL di click-through aggiunto all’URL della pagina di destinazione](/help/integrations/assets/target-ct-url.jpg)

### (Solo DSP) Aggiungi macro DSP agli URL Click-through

<!-- If we ever write instructions for ads on other ad servers (such as Sizmek ads in DCO), then work that into the following section. -->

Nell’ambito di Flash Talk o di Google Campaign Manager 360, aggiorna manualmente l’URL di click-through per ciascun annuncio, in modo da includere le macro necessarie per acquisire le variabili AMO ID. Le variabili AMO ID vengono utilizzate per inviare dati di clic ad Adobe Analytics e per condividere le chiavi di posizionamento per il test A/B. Per istruzioni, consulta le pagine seguenti:

* [Aggiungi [!DNL Analytics for Advertising] Macro a [!DNL Flashtalking] Tag ad](/help/integrations/analytics/macros-flashtalking.md)

* [Aggiungi [!DNL Analytics for Advertising] Macro a [!DNL Google Campaign Manager 360] Tag ad](/help/integrations/analytics/macros-google-campaign-manager.md)

Contatta il tuo Adobe Account Team e il Advertising Solutions Group (aac-advertising-solutions-group@adobe.com) per recuperare la chiave di posizionamento richiesta e finalizzare la configurazione, e per fare in modo che ogni URL click-through sia compilato con la chiave di posizionamento.

## Passaggio 2: Impostare il framework View-through utilizzando l&#39;Audience Manager {#view-through-framework}

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

![Framework view-through](/help/integrations/assets/targetr-vt-framework.png)

Aggiungendo un pixel evento di impression Audience Manager nei tag degli annunci e nelle impostazioni di posizionamento, puoi creare un segmento di test per ulteriori opportunità di test view-through.

1. Implementa un pixel evento di impression Audience Manager nei tag degli annunci e nelle impostazioni di posizionamento DSP.

   Per istruzioni, vedi &quot;[Raccolta di dati sull’esposizione dei contenuti multimediali da campagne pubblicitarie DSP](/help/integrations/audience-manager/media-data-integration/collect.md).&quot;

   Assicurati di aggiungere [Macro DSP](/help/dsp/campaign-management/macros.md) per acquisire tutti i dati che si desidera trasmettere al pixel dell’evento impression, tra cui `${TM_PLACEMENT_ID_NUM}` per l’ID di posizionamento numerico.

   >[!NOTE]
   >
   >Gli URL di tracciamento dei clic includono `${TM_PLACEMENT_ID}` macro per il tasto di posizionamento alfanumerico, anziché `${TM_PLACEMENT_ID_NUM}` per l’ID di posizionamento numerico.

1. Configura un segmento di Audience Manager dai dati di impression DSP:

   1. Vai a **Audience Manager** > **Dati sul pubblico** > **Segnali**, quindi seleziona la **Ricerca** in alto a sinistra.

   1. Inserisci il **Chiave** e **Valore** per il segnale che determina a quale livello vengono raggruppati gli utenti del segmento. Utilizza un [chiave supportata](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html?lang=en) con un valore che corrisponde a una macro aggiunta al pixel evento di impression Audience Manager.

      Ad esempio, per raggruppare gli utenti per un particolare posizionamento, utilizza il `d_placement` chiave. Per il valore , utilizza un ID di posizionamento numerico effettivo (ad esempio 2501853 nella schermata di cui sopra) acquisito dalla macro DSP `${TM_PLACEMENT_ID_NUM}`. <!-- Explain where to find the placement ID, other than in a custom report. -->

      Se il campo Conteggio totale mostra i conteggi degli utenti per la coppia chiave-valore, che indica che il pixel è stato inserito correttamente e che i dati sono in flusso, puoi continuare con il passaggio successivo.
   ![Segnali di ricerca](/help/integrations/assets/target-am-signals.png)

1. [Creare un tratto basato su regole](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) per la creazione di segmenti in Audience Manager.

   1. Denomina la caratteristica in modo che sia facilmente identificabile nelle attività di test. Memorizza la caratteristica in qualsiasi cartella preferita.

   1. Da **Origine dati** menu a discesa, seleziona **Ad Cloud**.

   1. Nel generatore di espressioni, aggiungi `d_event` nel campo Chiave e `imp` in **Valore** campo , seleziona **Aggiungi regola**, quindi salva la caratteristica.

   ![Schermata di una caratteristica basata su regole](/help/integrations/assets/target-am-trait.png)

1. Imposta un segmento di test in Audience Manager:

   1. Nella parte superiore della pagina, vai a **Dati sul pubblico** > **Caratteristiche** e cerca il nome completo della caratteristica. Seleziona la casella di controllo accanto al nome della caratteristica, quindi fai clic su **Crea segmento**.

   1. Assegna un nome al segmento, seleziona `Ad Cloud` come **Origine dati**, quindi salva il segmento.

      Ad Audience Manager, divide automaticamente il segmento in un gruppo di controllo che riceve l’esperienza standard di una pagina di destinazione e un gruppo di test che ha ricevuto un’esperienza personalizzata in loco.
   ![Schermata di un segmento di prova](/help/integrations/assets/target-am-segment.png)

## Passaggio 3: Configurare un’attività &quot;Test A/B&quot; in Target

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

Le seguenti istruzioni evidenziano informazioni relative al caso d’uso DSP. Per istruzioni complete, vedi &quot;[Creare un test A/B](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html)&quot;.

1. [Accedere ad Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html).

1. Da **Attività** elenco, fai clic su **Crea attività** > **Test A/B**.

   ![Creare un’attività Test A/B](/help/integrations/assets/target-create-ab.png)

1. In **Inserisci URL attività*** campo , immetti l’URL della pagina di destinazione per il test.

   ![Inserisci il campo URL attività](/help/integrations/assets/target-create-ab-url.png)

   >[!NOTE]
   >
   >Puoi utilizzare più URL per testare l’accesso al sito tramite visualizzazione. Per ulteriori informazioni, consulta &quot;[Attività multipagina](https://experienceleague.adobe.com/docs/target/using/experiences/vec/multipage-activity.html).&quot; È possibile identificare facilmente le voci principali in base all’URL della pagina creando un [Rapporto voce sito](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/integrations/ad-cloud/create-advertising-cloud-site-entry-reports.html) in Analytics.

1. In **Obiettivo** , immetti la metrica di successo per il test.

   >[!NOTE]
   >
   >Assicurati che [!DNL Analytics] è abilitato come origine dati in [!DNL Target]e che sia selezionata la suite di rapporti corretta.

1. Imposta la **Priorità** a `High` o `999` per evitare conflitti quando gli utenti del segmento di test ricevono un’esperienza sul sito non corretta.

1. Within **Impostazioni reporting**, seleziona **Nome dell&#39;azienda** e **Suite di rapporti** connesso al tuo account DSP.

   Per ulteriori suggerimenti, consulta &quot;[Best practice e risoluzione dei problemi di reporting](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html).&quot;

1. In **Intervallo date** immettere le date di inizio e di fine appropriate per il test.

1. Aggiungi tipi di pubblico all’attività:

   1. Scegli la [segmento creato in precedenza in Audience Manager per testare i tipi di pubblico view-through](#view-through-framework).

      ![Aggiungere tipi di pubblico all’attività](/help/integrations/assets/target-create-ab-audiences.png)

   1. Seleziona **Pagine del sito** > **Pagina di destinazione** > **Query** e immetti la chiave di posizionamento DSP nel **Valore** campo per utilizzare i parametri della stringa di query di Target per i tipi di pubblico click-through.

      ![Schermata di un pubblico di clic di destinazione](/help/integrations/assets/target-click-audience.jpg)

1. Per **Metodo di allocazione traffico**, seleziona **Manuale (predefinito)** e dividi il pubblico 50/50.

1. Salva l’attività.

1. Utilizzo [!DNL Target] [Compositore esperienza visivo](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html) per apportare modifiche di progettazione al modello di pagina di destinazione del test A/B.

   * Esperienza A: Non modificare perché è l’esperienza predefinita/di controllo della pagina di destinazione senza personalizzazione.

   * Esperienza B: Utilizza la [!DNL Target] interfaccia utente per personalizzare il modello della pagina di destinazione in base alle risorse incluse nel test (ad esempio titoli, copia, posizionamento dei pulsanti e contenuti creativi).
   >[!NOTE]
   >
   >Ad esempio, i casi d’uso di test creativi, contatta il team dell’account di Adobe.

## Passaggio 4: Imposta il tuo [!DNL Analytics for Target] Analysis Workspace in [!DNL Analytics]

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

[!DNL Analytics for Target] (A4T) è un’integrazione tra più soluzioni che consente agli inserzionisti di creare [!DNL Target] attività basate su [!DNL Analytics] metriche di conversione e segmenti di pubblico, quindi misurare i risultati utilizzando [!DNL Analytics] come origine per la generazione di rapporti. Tutti i rapporti e la segmentazione per quell’attività si basano su [!DNL Analytics] raccolta dati.

Per ulteriori informazioni [!DNL Analytics for Target], compreso un collegamento alle istruzioni di implementazione, vedi &quot;[Adobe Analytics come origine per la generazione di rapporti per Adobe Target (A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)&quot;.

### Imposta la [!DNL Analytics for Target] Pannello

In Analysis Workspace, configura il [!DNL Analytics for Target panel] per analizzare [!DNL Target] attività ed esperienze. Tieni presente i seguenti punti importanti e informazioni sui tuoi rapporti.

#### Metriche

* Crea un pannello all’interno dell’area di lavoro specifico per la campagna, il pacchetto o il posizionamento Adobe Advertising per cui è stato eseguito il test. Utilizza le visualizzazioni di riepilogo per mostrare metriche pubblicitarie di Adobe nello stesso rapporto delle prestazioni del test di Target.

* Dai priorità all’utilizzo di metriche sul sito (come visite e conversioni) per misurare le prestazioni.

* Le metriche dei contenuti multimediali aggregati derivanti dalla pubblicità per Adobi (come impression, clic e costi) non possono essere abbinate alle metriche di Target.

#### Dimension

Le seguenti dimensioni riguardano [!DNL Analytics for Target]:

* **Attività di Target**: Nome del test A/B

* **Esperienze Target**: Nomi delle esperienze della pagina di destinazione utilizzate nell’attività

* **Attività Target** > **Esperienza**: Nome dell’attività e nome dell’esperienza nella stessa riga

### Risoluzione dei problemi di Analytics per [!DNL Target] Dati

In Analysis Workspace, se noti che i dati di attività ed esperienze sono minimi o non vengono popolati, procedi come segue:

* Verifica che lo stesso Supplemental Data ID (SDID) sia utilizzato sia per Target che per Analytics. Puoi verificare i valori SDID utilizzando il [Debugger Adobe Experience Cloud](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html) nella pagina di destinazione alla quale la campagna sta guidando gli utenti.

[Valori SDID (Supplemental Data ID) in Adobe Debugger](/help/integrations/assets/target-troubleshooting-sdid.png)

* Nella stessa pagina di destinazione, verifica che a) il nome host mostrato nel debugger di Adobe in Soluzioni> Target corrisponda a b) il server di tracciamento mostrato in [!DNL Target] per l&#39;attività (in Obiettivi e impostazioni > Impostazioni reporting).

   [!DNL Analytics For Target] richiede un [!DNL Analytics] server di tracciamento da inviare nelle chiamate da [!DNL Target] al [!DNL Modstats] server di raccolta dati per Analytics.<!-- just "to Analytics?"-->

[Valore del nome host in Adobe Debugger](/help/integrations/assets/target-troubleshooting-hostname.png)

[Valore del server di tracciamento in Target](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## Ulteriori letture

* [Integrare Target con Analytics](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html)- Spiega come impostare il reporting di Target in Analysis Workspace.
* [Panoramica del test A/B](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html) - Descrive le attività di test A/B, che puoi utilizzare con gli annunci DSP.
* [Esperienze e offerte](https://experienceleague.adobe.com/docs/target/using/experiences/experiences.html) - Spiega [!DNL Target] strumenti per determinare il contenuto sul sito a cui sono esposti gli utenti DSP test.
* [Segnali, caratteristiche e segmenti](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/signal-trait-segment.html) - Definisce alcuni degli strumenti di Audience Manager che possono essere utili con DSP test view-through.
* [Panoramica di Analytics per la pubblicità](/help/integrations/analytics/overview.md) - Introduce Analytics for Advertising, che consente di monitorare le interazioni del sito click-through e view-through nelle istanze di Analytics.

<!-- 
>[!MORELIKETHIS]
>
>* 
-->
