---
title: Informazioni sulla gestione dell'audience in Advertising DSP
description: Scopri le funzioni di gestione dell’audience.
feature: DSP Audiences, DSP Segments
exl-id: 44cfe67e-e495-447f-b08f-d3789bd4dd09
source-git-commit: 31f20bcfb79265326f515218a02d8a4fa3efd586
workflow-type: tm+mt
source-wordcount: '1324'
ht-degree: 0%

---

# Informazioni sulla gestione dell&#39;audience in Advertising DSP

In DSP, puoi creare e gestire segmenti di pubblico e set di tipi di pubblico, che puoi utilizzare come target per i posizionamenti:

* Raccogli i tuoi dati di pubblico di prime parti creando e implementando segmenti DSP. In seguito, puoi effettuare il retargeting degli utenti nel segmento con annunci o impedire agli utenti del segmento di ricevere annunci. Puoi creare i seguenti tipi di segmenti:

   * [Segmenti personalizzati](/help/dsp/audiences/custom-segment-create.md) per tenere traccia di a) utenti esposti ad annunci da dispositivi desktop e mobili e b) utenti che visitano pagine Web specifiche. Il tag di tracciamento può tenere traccia degli utenti basati su cookie o degli utenti associati agli ID universali ID5.

   * [Segmenti di rifiuto del CCPA](/help/dsp/audiences/ccpa-opt-out-segment-create.md) per tenere traccia degli ID degli utenti dalle richieste di rifiuto del consumatore sul sito Web, in base al California Consumer Privacy Act (CCPA). Puoi recuperare rapporti mensili sugli ID utente dalle richieste di rifiuto.

     Per ulteriori informazioni sul supporto di Adobi Advertising per richieste di rifiuto del CCPA, vedere [Supporto di Adobi Advertising per il California Consumer Privacy Act: Consumer Opt-out Support](/help/privacy/ccpa/ccpa-opt-out-of-sale.md).

* (funzionalità Beta) [Ottieni e utilizza ID universali per il targeting senza cookie](/help/dsp/audiences/universal-ids.md):

   * Invia manualmente i segmenti [!DNL LiveRamp] [!DNL RampID] autenticati direttamente all&#39;DSP.

   * Consenti all’DSP di importare segmenti di prime parti dalla piattaforma di dati del cliente e tradurli in tipi di ID universali supportati.

   * Includi segmenti di terze parti che contengono ID universali nei target di posizionamento senza passaggi aggiuntivi.

* Crea una libreria di pubblico di [tipi di pubblico riutilizzabili](/help/dsp/audiences/reusable-audience-create.md). I tipi di pubblico salvati sono composti da uno qualsiasi dei segmenti di pubblico disponibili e da uno qualsiasi degli altri tipi di pubblico salvati. Tutte le modifiche apportate a un pubblico salvato vengono applicate automaticamente a tutti i posizionamenti mirati o esclusi dal pubblico e a tutti gli altri tipi di pubblico che includono il pubblico salvato.

  I tipi di pubblico salvati consentono ai responsabili della pianificazione dei contenuti multimediali di raggruppare i tipi di pubblico in base alle esigenze, includendo ed escludendo più segmenti utilizzando una logica booleana complessa. Le dimensioni di ogni singolo segmento e le dimensioni totali del pubblico sono indicate durante la creazione di un pubblico. I dirigenti delle campagne possono quindi semplicemente selezionare uno o più tipi di pubblico salvati come target di posizionamento, anziché configurare manualmente i target di pubblico per ciascun posizionamento.

Per il targeting del posizionamento sono disponibili anche altri tipi di pubblico.

## Importazione di segmenti di dati di prime e terze parti

Sono disponibili molte opzioni per importare segmenti di dati di prime e terze parti in DSP, utilizzando l’interfaccia utente dell’DSP e/o tramite servizi di importazione personalizzati.

* L&#39;DSP può richiamare il tuo Adobe Audience Manager e altri tipi di pubblico di [!DNL Adobe] per il targeting. Per i prerequisiti e le istruzioni, consulta &quot;[Importare segmenti di Adobe Audience Manager per l&#39;Ad Targeting](/help/integrations/audience-manager/import-audiences.md).

* L&#39;DSP può tradurre i segmenti di dati di prime parti dalle piattaforme dati dei clienti supportate in segmenti con ID universali utilizzando la funzionalità [Origini](/help/dsp/audiences/sources/source-about.md). Puoi anche [inviare manualmente i segmenti autenticati [!DNL LiveRamp] [!DNL RampID] direttamente all&#39;DSP](/help/dsp/audiences/sources/source-import-liveramp-segments.md).

* DSP può importare gli altri segmenti di dati di prime parti direttamente dalla piattaforma di gestione dati (DMP, data management platform) e fornirli a qualsiasi gruppo di inserzionisti, in base alle esigenze.

* DSP può importare segmenti di terze parti personalizzati, incluse combinazioni complesse di segmenti di terze parti. Puoi fornire i segmenti a qualsiasi gruppo di inserzionisti, in base alle esigenze.

Per ulteriori informazioni, contatta il team del tuo account di Adobe.

## Tipi di pubblico disponibili come target di posizionamento

Puoi indirizzare i posizionamenti a tutti i seguenti tipi di pubblico.

* Tutti i set di pubblico creati dall’utente e salvati in DSP.

* Tutti i segmenti di pubblico creati dall’utente e creati in DSP:

   * Segmenti personalizzati per gli utenti che hanno visitato pagine web specifiche e utenti esposti a impression di annunci specifici.

     Non viene applicata alcuna tariffa per le impression consegnate agli ID universali.

   * Segmenti di pubblico di rifiuto del CCPA per gli utenti che hanno inviato richieste di rifiuto sul sito web, in base al California Consumer Privacy Act (CCPA).

* Tutti i segmenti di dati di prime parti importati, inclusi i segmenti convertiti in ID universali.

  Vengono addebitati costi aggiuntivi per le impression consegnate agli ID universali. Consulta &quot;[Informazioni sulle origini del pubblico di prime parti](/help/dsp/audiences/sources/source-about.md)&quot; per le tariffe.

* Tutti i segmenti di dati di terze parti personalizzati importati.

* (Posizionamenti destinati solo agli Stati Uniti) [Tutti i segmenti di dati di terze parti disponibili per i clienti DSP da oltre 30 provider](/help/dsp/audiences/third-party-data-providers.md), inclusi [!DNL eXelate], ([!DNL Eyeota]), ([!DNL LiveRamp]),[!DNL Lotame], [!DNL Neustar] e molti altri.

  Puoi eseguire il targeting di segmenti specifici, che eseguono il targeting degli utenti in base ai dati del pubblico (ad esempio, utenti con caratteristiche demografiche, interessi o intenti specifici e/o profili comportamentali). Puoi sfogliare per provider di dati e categoria, cercare i segmenti per nome o ID segmento oppure filtrare i risultati per provider di dati, dimensione totale del segmento, numero di browser web o numero di dispositivi.

  I segmenti di terze parti sono soggetti a commissioni aggiuntive, indicate accanto al nome di ciascun segmento.

* (Inserzionisti con Adobe Experience Platform e [!DNL Real-Time CDP], Adobe Audience Manager o Adobe Analytics che utilizzano solo tag di conversione JavaScript Adobe Advertising) Tutti i segmenti di pubblico di prime, seconde o terze parti disponibili creati in [!DNL Real-Time CDP], creati in Audience Manager o pubblicati in Adobe Experience Cloud da Audience Manager o [!DNL Analytics].

  La determinazione dei prezzi per l’utilizzo dei segmenti è prenegoziata e non è visibile in DSP.

  I segmenti di [!DNL Analytics] sono disponibili circa un&#39;ora dopo la loro creazione o pubblicazione come tipi di pubblico Experience Cloud. I segmenti provenienti direttamente da Audience Manager o [!DNL Real-Time CDP] sono disponibili entro 24 ore dalla condivisione.

  >[!NOTE]
  >
  >Consulta la documentazione di [Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-home.html?lang=it), [Analytics](https://experienceleague.adobe.com/docs/analytics.html?lang=it) e [the [!DNL Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/segmentation/segment-builder-guide.html?lang=it) per informazioni sulla configurazione e la raccolta dei dati per i segmenti in queste soluzioni.

## Dati dimensione pubblico

In Audiences > All Audiences e nella sezione Audience Targeting delle impostazioni di posizionamento, puoi filtrare ogni elenco di segmenti per intervallo di dimensioni, compreso l’intervallo totale e intervalli separati per tipi di dispositivi specifici o tipi di ID universali.

![filtro per dimensione pubblico](/help/dsp/assets/audience-size-filter.png)

Puoi anche visualizzare dati dettagliati sulle dimensioni del pubblico:

* Vengono visualizzate le dimensioni del pubblico deduplicato totale e attivo in tutti i segmenti selezionati e i tipi di pubblico salvati; è possibile visualizzare i dettagli per tipo di dispositivo (browser, dispositivo mobile o TV connessa).

  ![la dimensione del pubblico combinata](/help/dsp/assets/audience-size.png)

* Per i singoli segmenti, accanto al nome del segmento vengono visualizzate la dimensione totale del pubblico e il CPM (se applicabile).

  ![dimensione segmento singolo](/help/dsp/assets/audience-size-segment.png)

* Puoi visualizzare ulteriori dettagli su un singolo segmento o un pubblico salvato, incluse le dimensioni per browser, dispositivi mobili, TV connessa e partner di tipo ID universale. Per i tipi di pubblico salvati, la dimensione totale è il totale deduplicato.

  ![dettagli del singolo segmento o del pubblico salvato](/help/dsp/assets/audience-size-segment-details.png)

## Visualizzazioni di Audiences

### Visualizzazione Tutti i tipi di pubblico

Nella visualizzazione [!UICONTROL All Audiences], o Libreria tipi di pubblico, è possibile salvare e gestire i tipi di pubblico riutilizzabili, che includono gruppi di segmenti di pubblico e anche altri tipi di pubblico salvati. Puoi utilizzare i tipi di pubblico come target per più posizionamenti. Il numero di posizionamenti in cui ogni pubblico viene utilizzato è indicato accanto al nome del posizionamento.

Puoi modificare, clonare, eliminare, esportare o condividere qualsiasi tipo di pubblico.

### Visualizzazione segmenti

Nella visualizzazione [!UICONTROL Segments], tutti gli utenti possono creare altri segmenti personalizzati.

Nella visualizzazione [!UICONTROL Segments] sono elencati anche i seguenti tipi di segmenti:

* Tutti i segmenti personalizzati creati dall’utente sono disponibili per l’utente.

  Puoi visualizzare i tag di tracciamento per qualsiasi segmento personalizzato creato e condividere tali segmenti con altri utenti. Puoi anche modificare o eliminare i segmenti personalizzati creati.

  Non puoi modificare o condividere segmenti personalizzati condivisi da altri utenti.

* Tutti i segmenti di prime parti importati così come sono disponibili per l’utente.

  Non puoi modificare o condividere segmenti di prime parti condivisi con te. Se hai la necessità di condividere segmenti di prime parti con altri utenti, contatta il team del tuo account di Adobe.

* Tutti i segmenti personalizzati di terze parti disponibili per l’utente.

  Non puoi modificare o condividere segmenti di terze parti condivisi con te. Se devi condividere segmenti di terze parti con altri utenti, contatta il tuo Account Team di Adobi.

### Visualizzazione Origini

Nella visualizzazione [!UICONTROL Sources] è possibile configurare le origini per i segmenti di prime parti nelle piattaforme dati dei clienti supportate che si desidera convertire in segmenti contenenti tipi ID universali specificati. Le impostazioni di origine includono una chiave di origine generata automaticamente, che fornirai alla piattaforma dati del cliente per stabilire la connessione.

Per ulteriori informazioni sulle piattaforme dati del cliente supportate, sui tipi di ID universali supportati e sui flussi di lavoro per impostare connessioni a ogni piattaforma dati del cliente, vedi &quot;[Informazioni sulle origini](/help/dsp/audiences/sources/source-about.md)&quot;.

I segmenti tradotti sono disponibili per l’inclusione in tipi di pubblico riutilizzabili e in impostazioni di posizionamento per il targeting senza cookie.

>[!MORELIKETHIS]
>
>* [Supporto per l&#39;attivazione di ID universali](/help/dsp/audiences/universal-ids.md)
>* [Crea un pubblico riutilizzabile](reusable-audience-create.md)
>* [Creare e implementare un segmento personalizzato](custom-segment-create.md)
>* [Crea e implementa un segmento [!UICONTROL CCPA Opt-Out-of-Sale]](ccpa-opt-out-segment-create.md)
>* [Informazioni sulle origini del pubblico di prime parti](/help/dsp/audiences/sources/source-about.md)
>* [Gestione delle origini del pubblico per attivare i tipi di pubblico con ID universale](/help/dsp/audiences/sources/source-manage.md)
>* [Importa manualmente segmenti autenticati da [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Provider di dati di terze parti disponibili](third-party-data-providers.md)
>* [Impostazioni posizionamento](/help/dsp/campaign-management/placements/placement-settings.md)
