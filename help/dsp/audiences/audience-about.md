---
title: Informazioni sulla gestione dell’audience in Advertising DSP
description: Scopri le funzioni di gestione dell’audience.
feature: DSP Audiences, DSP Segments
exl-id: 44cfe67e-e495-447f-b08f-d3789bd4dd09
source-git-commit: 67b59f4f066d25f323620b83b5a0cb49beb3ee04
workflow-type: tm+mt
source-wordcount: '1021'
ht-degree: 0%

---

# Informazioni sulla gestione dell’audience in Advertising DSP

In DSP, puoi creare e gestire segmenti di pubblico e set di tipi di pubblico, che puoi utilizzare come target per i posizionamenti:

* Puoi raccogliere i tuoi dati sul pubblico di prime parti creando e implementando segmenti. In seguito, puoi effettuare il retargeting degli utenti nel segmento con annunci o impedire agli utenti del segmento di ricevere annunci. Puoi creare i seguenti tipi di segmenti:

   * [Segmenti personalizzati](/help/dsp/audiences/custom-segment-create.md) per tenere traccia di a) utenti esposti agli annunci da desktop e dispositivi mobili e b) utenti che visitano specifiche pagine web.

   * [Segmenti di rifiuto del CCPA](/help/dsp/audiences/ccpa-opt-out-segment-create.md) per tenere traccia degli ID degli utenti dalle richieste di rifiuto del consumatore sul sito web, in base al California Consumer Privacy Act (CCPA). Puoi recuperare rapporti mensili sugli ID utente dalle richieste di rifiuto.

     Per ulteriori informazioni sul supporto di Adobi Advertising per richieste di rifiuto del CCPA, vedi [Adobe Advertising di supporto per il California Consumer Privacy Act: supporto per la rinuncia del consumatore](/help/privacy/ccpa/ccpa-opt-out-of-sale.md).

* Puoi creare una libreria di tipi di pubblico di [pubblico riutilizzabile](/help/dsp/audiences/reusable-audience-create.md). I tipi di pubblico salvati sono composti da uno qualsiasi dei segmenti di pubblico disponibili e da uno qualsiasi degli altri tipi di pubblico salvati. Tutte le modifiche apportate a un pubblico salvato vengono applicate automaticamente a tutti i posizionamenti mirati o esclusi dal pubblico e a tutti gli altri tipi di pubblico che includono il pubblico salvato.

  I tipi di pubblico salvati consentono ai responsabili della pianificazione dei contenuti multimediali di raggruppare i tipi di pubblico in base alle esigenze, includendo ed escludendo più segmenti utilizzando una logica booleana complessa. Le dimensioni di ogni singolo segmento e le dimensioni totali del pubblico sono indicate durante la creazione di un pubblico. I dirigenti delle campagne possono quindi semplicemente selezionare uno o più tipi di pubblico salvati come target di posizionamento, anziché configurare manualmente i target di pubblico per ciascun posizionamento.

Per il targeting del posizionamento sono disponibili anche altri tipi di pubblico.

## Importazione di segmenti di dati di prime e terze parti

DSP può importare i tuoi segmenti di dati di prime parti dalla tua piattaforma di gestione dati (DMP) e fornirli a qualsiasi gruppo di inserzionisti, in base alle esigenze.

DSP è una destinazione integrata per [il [!DNL Adobe Real-Time Customer Data Profile (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=it), che consente di condividere segmenti autenticati di prime parti con inserzionisti e utenti approvati per l’attivazione della campagna. Per ulteriori informazioni sull’integrazione di Real-Time CDP, consulta [Sezione Sources](/help/dsp/audiences/sources/source-about.md).

DSP può anche importare segmenti di terze parti personalizzati, incluse combinazioni complesse di segmenti di terze parti. Puoi fornire i segmenti a qualsiasi gruppo di inserzionisti, in base alle esigenze.

Per ulteriori informazioni, contatta il team del tuo account di Adobe.

## Tipi di pubblico disponibili come target di posizionamento

Puoi indirizzare i posizionamenti a tutti i seguenti tipi di pubblico.

* Tutti i set di pubblico creati dall’utente e salvati in DSP.

* Tutti i segmenti di pubblico creati dall’utente e creati in DSP:

   * Segmenti personalizzati per gli utenti che hanno visitato pagine web specifiche e utenti esposti a impression di annunci specifici.

   * Segmenti di pubblico di rifiuto del CCPA per gli utenti che hanno inviato richieste di rifiuto sul sito web, in base al California Consumer Privacy Act (CCPA).

* Tutti i segmenti di dati di prime parti importati.

* Tutti i segmenti di dati di terze parti personalizzati importati.

* (Posizionamenti mirati solo agli Stati Uniti) [Tutti i segmenti di dati di terze parti disponibili per i clienti DSP di oltre 30 fornitori](/help/dsp/audiences/third-party-data-providers.md), tra cui [!DNL Acxiom], [!DNL Datalogix], [!DNL eXelate] ([!DNL Nielsen]), [!DNL Lotame], [!DNL Oracle], [!DNL Quantcast], e molti altri.

  Puoi eseguire il targeting di segmenti specifici, che eseguono il targeting degli utenti in base ai dati del pubblico (ad esempio, utenti con caratteristiche demografiche, interessi o intenti specifici e/o profili comportamentali). Puoi sfogliare per provider di dati e categoria, cercare i segmenti per nome o ID segmento oppure filtrare i risultati per provider di dati, dimensione totale del segmento, numero di browser web o numero di dispositivi.

  I segmenti di terze parti sono soggetti a commissioni aggiuntive, indicate accanto al nome di ciascun segmento.

* (Inserzionisti con Adobe Experience Platform e [!DNL Real-Time CDP], Adobe Audience Manager o Adobe Analytics che utilizzano solo tag di conversione JavaScript di Adobe Advertising) Tutti i segmenti di pubblico di prime, seconde o terze parti disponibili creati in [!DNL Real-Time CDP], creato in Audienci Manager o pubblicato su Adobe Experience Cloud da Audienci Manager o [!DNL Analytics].

  La determinazione dei prezzi per l’utilizzo dei segmenti è prenegoziata e non è visibile in DSP.

  Segmenti da [!DNL Analytics] sono disponibili circa un’ora dopo averli creati o pubblicati come tipi di pubblico Experience Cloud. Segmenti provenienti direttamente da Audienci Manager o [!DNL Real-Time CDP] sono disponibili entro 24 ore dalla condivisione.

  >[!NOTE]
  >
  >Consulta la documentazione per [Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-home.html), [Analytics](https://experienceleague.adobe.com/docs/analytics.html), e [il [!DNL Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/segmentation/segment-builder-guide.html) per informazioni sulla configurazione e la raccolta di dati per i segmenti in tali soluzioni.

## Dati dimensione pubblico

Nelle impostazioni salvate per il pubblico e per il posizionamento, puoi visualizzare dati dettagliati sulle dimensioni del pubblico:

* Vengono visualizzate le dimensioni del pubblico deduplicato totale e attivo in tutti i segmenti selezionati e i tipi di pubblico salvati; è possibile visualizzare i dettagli per tipo di dispositivo (browser, dispositivo mobile o TV connessa).

  ![la dimensione del pubblico combinato](/help/dsp/assets/audience-size.png)

* Per i singoli segmenti e i tipi di pubblico salvati, accanto al nome del segmento vengono visualizzate la dimensione totale del pubblico e il CPM (se applicabile). Puoi visualizzare ulteriori dettagli sul segmento, inclusa la dimensione per tipo di dispositivo (browser, dispositivo mobile o TV connessa). Per i tipi di pubblico salvati, la dimensione totale è il totale deduplicato.

  ![la dimensione del singolo segmento](/help/dsp/assets/audience-size-segment.png)

## Visualizzazioni di Audiences

### Visualizzazione Tutti i tipi di pubblico

In [!UICONTROL All Audiences] o Libreria tipi di pubblico, puoi salvare e gestire i tipi di pubblico riutilizzabili, che includono gruppi di segmenti di pubblico e anche altri tipi di pubblico salvati. Puoi utilizzare i tipi di pubblico come target per più posizionamenti. Il numero di posizionamenti in cui ogni pubblico viene utilizzato è indicato accanto al nome del posizionamento.

Puoi modificare, clonare, eliminare, esportare o condividere qualsiasi tipo di pubblico.

### Visualizzazione segmenti

In [!UICONTROL Segments] , tutti gli utenti possono creare altri segmenti personalizzati.

Il [!UICONTROL Segments] visualizza inoltre elenca i seguenti tipi di segmenti:

* Tutti i segmenti personalizzati creati dall’utente sono disponibili per l’utente.

  Puoi visualizzare i tag di tracciamento per qualsiasi segmento personalizzato creato e condividere tali segmenti con altri utenti. Puoi anche modificare o eliminare i segmenti personalizzati creati.

  Non puoi modificare o condividere segmenti personalizzati condivisi da altri utenti.

* Tutti i segmenti di prime parti importati disponibili per l’utente.

  Non puoi modificare o condividere segmenti di prime parti condivisi con te. Se hai la necessità di condividere segmenti di prime parti con altri utenti, contatta il team del tuo account di Adobe.

* Tutti i segmenti personalizzati di terze parti disponibili per l’utente.

  Non puoi modificare o condividere segmenti di terze parti condivisi con te. Se devi condividere segmenti di terze parti con altri utenti, contatta il tuo Account Team di Adobi.

>[!MORELIKETHIS]
>
>* [Creare un pubblico riutilizzabile](reusable-audience-create.md)
>* [Impostazioni pubblico](audience-settings.md)
>* [Sintassi della logica dei segmenti di pubblico](audience-segment-logic-syntax.md)
>* [Creare e implementare un segmento personalizzato](custom-segment-create.md)
>* [Creare e implementare un [!UICONTROL CCPA Opt-Out-of-Sale] Segmento](ccpa-opt-out-segment-create.md)
>* [Provider di dati di terze parti disponibili](third-party-data-providers.md)
>* [Impostazioni di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md)
