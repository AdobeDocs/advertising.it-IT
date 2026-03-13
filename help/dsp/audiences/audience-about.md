---
title: Informazioni sulla gestione del pubblico in Advertising DSP
description: Scopri le funzionalità di gestione del pubblico.
feature: DSP Audiences, DSP Segments
exl-id: 44cfe67e-e495-447f-b08f-d3789bd4dd09
source-git-commit: ddd55586ed895962b8f6da0390a3d76fe43ca1ca
workflow-type: tm+mt
source-wordcount: '1322'
ht-degree: 0%

---

# Informazioni sulla gestione dell&#39;audience in Advertising DSP

In DSP, puoi creare e gestire segmenti di pubblico e set di tipi di pubblico, che puoi utilizzare come target per i posizionamenti:

* Raccogli i tuoi dati di pubblico di prime parti creando e implementando segmenti di DSP. È possibile riassegnare gli utenti nel segmento con annunci o impedire agli utenti nel segmento di ricevere annunci. Potete creare i seguenti tipi di segmenti:

   * [Segmenti personalizzati](/help/dsp/audiences/custom-segment-create.md) per tenere traccia di a) utenti esposti agli annunci da desktop e dispositivi mobili e b) utenti che visitano pagine Web specifiche. Il tag di tracciamento può tenere traccia degli utenti basati su cookie o degli utenti associati agli ID universali ID5.

   * [Segmenti di annullamento della vendita del servizio di assistenza clienti](/help/dsp/audiences/ccpa-opt-out-segment-create.md) per tenere traccia degli ID degli utenti dalle richieste di annullamento della vendita dei prodotti sul sito Web, in base al California Consumer Privacy Act (CCPA). Puoi recuperare i report mensili degli ID utente dalle richieste di rinuncia alla vendita.

     Per ulteriori informazioni sull&#39;Adobe Advertising di supporto per le richieste di rinuncia alla vendita di CCPA, vedere [Supporto Adobe Advertising per il California Consumer Privacy Act: Consumer Opt-out Support](/help/privacy/ccpa/ccpa-opt-out-of-sale.md).

* (Funzione Beta) [Ottenere e utilizzare ID universali per destinazioni senza cookie](/help/dsp/audiences/universal-ids.md):

   * Invia manualmente i [!DNL LiveRamp] [!DNL RampID] segmenti autenticati direttamente all&#39;DSP.

   * Consenti all&#39;DSP di importare segmenti di terze parti dalla piattaforma dati del cliente e di tradurli in tipi di ID universali supportati.

   * Includete i segmenti di terze parti che contengono ID universali nelle destinazioni di posizionamento senza ulteriori passaggi.

* Crea una libreria di gruppi di destinatari di [gruppi di destinatari riutilizzabili](/help/dsp/audiences/reusable-audience-create.md). I tipi di pubblico salvati sono composti da uno qualsiasi dei segmenti di pubblico disponibili e da uno qualsiasi degli altri tipi di pubblico salvati. Tutte le modifiche apportate a un pubblico salvato vengono applicate automaticamente a tutti i posizionamenti mirati o esclusi dal pubblico e a tutti gli altri tipi di pubblico che includono il pubblico salvato.

  I tipi di pubblico salvati consentono ai responsabili della pianificazione dei contenuti multimediali di raggruppare i tipi di pubblico in base alle esigenze, includendo ed escludendo più segmenti utilizzando una logica booleana complessa. Le dimensioni (mirabili) di ogni singolo segmento e le dimensioni complessive del pubblico attivo sono indicate durante la creazione di un pubblico. I dirigenti delle campagne possono quindi semplicemente selezionare uno o più tipi di pubblico salvati come target di posizionamento, anziché configurare manualmente i target di pubblico per ciascun posizionamento.

Per il targeting del posizionamento sono disponibili anche altri tipi di pubblico.

## Importazione di segmenti di dati di prime e terze parti

Sono disponibili molte opzioni per importare segmenti di dati di prime e terze parti in DSP, utilizzando l’interfaccia utente di DSP e/o tramite servizi di importazione personalizzati.

* DSP può richiamare il tuo Adobe Audience Manager e altri tipi di pubblico di [!DNL Adobe] per il targeting. Per i prerequisiti e le istruzioni, consulta &quot;[Importare segmenti di Adobe Audience Manager per l&#39;Ad Targeting](/help/integrations/audience-manager/import-audiences.md).

* DSP può tradurre i segmenti di dati di prime parti dalle piattaforme dati dei clienti supportate in segmenti con ID universali utilizzando la funzionalità [Origini](/help/dsp/audiences/sources/source-about.md). Puoi anche [inviare manualmente i segmenti autenticati [!DNL LiveRamp] [!DNL RampID] direttamente a DSP](/help/dsp/audiences/sources/source-import-liveramp-segments.md).

* DSP può importare altri segmenti di dati di prime parti direttamente dalla piattaforma di gestione dati (DMP) e fornirli a qualsiasi gruppo di inserzionisti, in base alle esigenze.

* DSP può importare segmenti personalizzati di terze parti, incluse combinazioni complesse di segmenti di terze parti. Puoi fornire i segmenti a qualsiasi gruppo di inserzionisti, in base alle esigenze.

Per ulteriori informazioni, contatta il team del tuo account di Adobe.

## Tipi di pubblico disponibili come target di posizionamento

Puoi indirizzare i posizionamenti a tutti i seguenti tipi di pubblico.

* Tutti i gruppi di destinatari creati dall&#39;utente e salvati nell&#39;DSP.

* Tutti i segmenti di pubblico creati dall’utente e creati nell’DSP:

   * Segmenti personalizzati per utenti che visitano pagine Web specifiche e utenti esposti a impression di annunci specifici.

     Non vengono addebitate commissioni per le impressioni fornite agli ID universali.

   * Segmenti di pubblico che hanno optato per l&#39;esclusione dalla vendita per gli utenti che hanno inviato richieste di esclusione dalla vendita sul tuo sito Web, in base al California Consumer Privacy Act (CCPA).

* Tutti i segmenti di dati di prime parti importati, inclusi i segmenti convertiti in ID universali.

  Vengono addebitati costi aggiuntivi per le impression consegnate agli ID universali. Consulta &quot;[Informazioni sulle origini del pubblico di prime parti](/help/dsp/audiences/sources/source-about.md)&quot; per le tariffe.

* Tutti i segmenti di dati di terze parti personalizzati importati.

* (Posizionamenti destinati solo agli Stati Uniti) [Tutti i segmenti di dati di terze parti disponibili per i clienti DSP da oltre 30 provider](/help/dsp/audiences/third-party-data-providers.md), inclusi [!DNL eXelate], ([!DNL Eyeota]), ([!DNL LiveRamp]),[!DNL Lotame], [!DNL Neustar] e molti altri.

  Puoi eseguire il targeting di segmenti specifici, che eseguono il targeting degli utenti in base ai dati del pubblico (ad esempio, utenti con caratteristiche demografiche, interessi o intenti specifici e/o profili comportamentali). Puoi sfogliare per provider di dati e categoria, cercare i segmenti per nome o ID segmento oppure filtrare i risultati per provider di dati, dimensione del segmento attivo, numero di browser web o numero di dispositivi.

  I segmenti di terze parti prevedono costi aggiuntivi indicati accanto al nome di ciascun segmento.

* (Inserzionisti con Adobe Experience Platform e [!DNL Real-Time CDP], Adobe Audience Manager o Adobe Analytics che utilizzano solo tag di conversione JavaScript Adobe Advertising) Tutti i segmenti di pubblico disponibili di prima, seconda o terza parte creati in [!DNL Real-Time CDP], creati in Audience Manager o pubblicati in Adobe Experience Cloud da Audience Manager o [!DNL Analytics].

  I prezzi per l&#39;utilizzo dei segmenti sono stati negoziati in anticipo e non sono visibili nel DSP.

  I segmenti da [!DNL Analytics] sono disponibili circa un&#39;ora dopo la creazione o la pubblicazione come gruppi di Experienci Cloud. I segmenti provenienti direttamente da Audience Manager o [!DNL Real-Time CDP] sono disponibili entro 24 ore dalla condivisione.

  >[!NOTE]
  >
  >Per informazioni sull&#39;impostazione e la raccolta di dati per i segmenti in queste soluzioni, vedere la documentazione per [Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-home.html?lang=it), [Analisi](https://experienceleague.adobe.com/docs/analytics.html?lang=it) e [l [!DNL Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/segmentation/segment-builder-guide.html?lang=it).

## Dati dimensioni gruppo di destinatari

In Audiences > All Audiences e nella sezione Audience Targeting delle impostazioni di posizionamento, potete filtrare ciascun elenco di segmenti per intervallo di dimensioni, inclusi intervalli separati per tipi di dispositivi specifici o tipi di ID universali.

![filtro per dimensione pubblico](/help/dsp/assets/audience-size-filter.png)

Puoi anche visualizzare dati dettagliati sulle dimensioni del pubblico:

* Vengono visualizzate le dimensioni del pubblico deduplicato attivo in tutti i segmenti selezionati e in tutti i gruppi di destinatari salvati ed è possibile visualizzare i dettagli in base al tipo di dispositivo (browser, dispositivo mobile o TV connessa).

  ![la dimensione del pubblico combinata](/help/dsp/assets/audience-size.png)

* Per i singoli segmenti, accanto al nome del segmento vengono visualizzate la dimensione del pubblico attivo e CPM (se applicabile).

  ![dimensione segmento singolo](/help/dsp/assets/audience-size-segment.png)

* Puoi visualizzare ulteriori dettagli su un singolo segmento o un pubblico salvato, incluse le dimensioni per browser, dispositivi mobili, TV connessa e partner di tipo ID universale. Per i tipi di pubblico salvati, la dimensione totale del pubblico attivo corrisponde al totale deduplicato.

  ![dettagli del singolo segmento o del pubblico salvato](/help/dsp/assets/audience-size-segment-details.png)

## Visualizzazioni gruppi di destinatari

### Vista Tutti i gruppi di destinatari

Nella visualizzazione [!UICONTROL All Audiences] o nella raccolta gruppi di destinatari è possibile salvare e gestire gruppi di destinatari riutilizzabili, che includono gruppi di segmenti di pubblico e anche altri gruppi di destinatari salvati. Potete usare i gruppi di destinatari come destinazioni per più posizionamenti. Il numero di posizioni in cui ogni gruppo di destinatari viene utilizzato viene indicato accanto al nome della posizione.

Puoi modificare, clonare, eliminare, esportare o condividere qualsiasi gruppo di destinatari.

### Vista segmenti

Nella visualizzazione [!UICONTROL Segments], tutti gli utenti possono creare altri segmenti personalizzati.

Nella visualizzazione [!UICONTROL Segments] sono elencati anche i seguenti tipi di segmenti:

* Tutti i segmenti personalizzati creati dall’utente sono disponibili per l’utente.

  È possibile visualizzare i tag di tracciamento per qualsiasi segmento personalizzato creato e condividerli con altri utenti. Potete anche modificare o eliminare i segmenti personalizzati creati.

  Non è possibile modificare o condividere segmenti personalizzati condivisi da altri utenti.

* Tutti i segmenti di prima parte importati così come sono disponibili per l’utente.

  Non è possibile modificare o condividere segmenti di prima parte condivisi con te. Se devi condividere segmenti di prima parte con altri utenti, contatta il tuo Account Team Adobe.

* Tutti i segmenti personalizzati di terze parti disponibili per l’utente.

  Non potete modificare o condividere segmenti di terze parti condivisi con voi. Se devi condividere segmenti di terze parti con utenti aggiuntivi, contatta il tuo team per gli account di Adobe.

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
