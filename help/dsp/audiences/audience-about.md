---
title: Gestione dell'audience in Advertising DSP
description: Scopri le funzioni di gestione dell’audience.
feature: DSP Audiences, DSP Segments
exl-id: 624d2211-59a2-4791-b8f1-a9a5cecd0b8e
source-git-commit: 1c13874967ec4ad264e5fa6a5e0dfeb6120f53cc
workflow-type: tm+mt
source-wordcount: '1036'
ht-degree: 0%

---

# Gestione dell&#39;audience in Advertising DSP

In DSP puoi creare e gestire segmenti di pubblico e set di pubblico, che puoi utilizzare come target per i posizionamenti:

* Puoi raccogliere i tuoi dati di pubblico di prime parti creando e implementando i segmenti. In seguito puoi effettuare il retargeting degli utenti nel segmento con gli annunci o impedire agli utenti nel segmento di ricevere gli annunci. Puoi creare i seguenti tipi di segmenti:

   * [Segmenti personalizzati](/help/dsp/audiences/custom-segment-create.md) per tenere traccia di a) utenti esposti ad annunci da desktop, dispositivi mobili e dispositivi CTV e b) utenti che visitano specifiche pagine web.

   * [Segmenti di rifiuto del CCPA](/help/dsp/audiences/ccpa-opt-out-segment-create.md) per tenere traccia degli ID utente dalle richieste di rifiuto del consumatore sul tuo sito web, in conformità al California Consumer Privacy Act (CCPA). Puoi recuperare rapporti mensili sugli ID utente dalle richieste di rinuncia alla vendita.

      Per ulteriori informazioni sull’Adobe del supporto pubblicitario per le richieste di rifiuto del CCPA, consulta [Adobe di supporto per la pubblicità per il California Consumer Privacy Act: Supporto per rinuncia del consumatore](/help/privacy/ccpa-opt-out-of-sale.md).

* Puoi creare una libreria di tipi di pubblico [tipi di pubblico riutilizzabili](/help/dsp/audiences/reusable-audience-create.md). I tipi di pubblico salvati sono composti da uno qualsiasi dei segmenti di pubblico disponibili e da qualsiasi altro pubblico salvato. Tutte le modifiche apportate a un pubblico salvato vengono applicate automaticamente a tutti i posizionamenti che eseguono il targeting o escludono il pubblico e a tutti gli altri tipi di pubblico che includono il pubblico salvato.

   I tipi di pubblico salvati consentono ai pianificatori multimediali di raggruppare i tipi di pubblico in base alle esigenze, includendo ed escludendo più segmenti utilizzando una logica booleana complessa. Le dimensioni di ciascun segmento e le dimensioni totali del pubblico vengono indicate durante la creazione di un pubblico. I dirigenti di Campaign possono quindi semplicemente selezionare uno o più tipi di pubblico salvati come destinazioni di posizionamento anziché configurare manualmente i target di pubblico per ciascun posizionamento.

Sono disponibili anche tipi di pubblico aggiuntivi per il targeting del posizionamento.

## Importazione di segmenti di dati di prime e terze parti

DSP importare i tuoi segmenti di dati di prime parti dalla piattaforma di gestione dati (DMP, data management platform) e fornirli a qualsiasi gruppo di inserzionisti, in base alle esigenze.

DSP è una destinazione integrata per [la [!DNL Adobe Real-Time Customer Data Profile (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html), che consente di condividere segmenti di prime parti autenticati con inserzionisti approvati e con gli utenti per l’attivazione della campagna. Per ulteriori informazioni sull’integrazione di Real-Time CDP, consulta la sezione [Sezione Origini](/help/dsp/audiences/sources/source-about.md).

DSP inoltre importare segmenti personalizzati di terze parti, incluse combinazioni complesse di segmenti di terze parti. Puoi fornire i segmenti a qualsiasi set di inserzionisti, in base alle esigenze.

Contatta il tuo [!DNL Adobe] team di account per ulteriori informazioni.

## Tipi di pubblico disponibili come target di posizionamento

Puoi eseguire il targeting dei posizionamenti per tutti i seguenti tipi di pubblico.

* Tutti i set di pubblico creati dall’utente salvati in DSP.

* Tutti i segmenti di pubblico creati dall’utente creati in DSP:

   * Segmenti personalizzati per gli utenti che hanno visitato pagine web specifiche e gli utenti esposti alle impression di annunci specifici.

   * Segmenti di pubblico con rinuncia al CCPA per gli utenti che hanno inviato richieste di rinuncia al commercio sul tuo sito web, in conformità al California Consumer Privacy Act (CCPA).

* Tutti i segmenti di dati di prime parti importati.

* Tutti i segmenti di dati di terze parti personalizzati importati.

* (Posizionamenti destinati solo agli Stati Uniti) [Tutti i segmenti di dati di terze parti disponibili per clienti DSP da oltre 30 provider](/help/dsp/audiences/third-party-data-providers.md), tra cui [!DNL Acxiom], [!DNL Datalogix], [!DNL eXelate] ([!DNL Nielsen]), [!DNL Lotame], [!DNL Oracle], [!DNL Quantcast]e molto altro ancora.

   Puoi eseguire il targeting di segmenti specifici, che si rivolgono agli utenti in base ai dati del pubblico (ad esempio, utenti con specifici profili demografici, interessi o intenti e/o comportamentali). Puoi sfogliare i dati per provider e categoria, cercare i segmenti per nome o ID segmento, o filtrare i risultati per provider di dati, dimensione totale del segmento, conteggio del browser web o conteggio dei dispositivi.

   I segmenti di terze parti devono sostenere tariffe aggiuntive, indicate accanto al nome di ciascun segmento.

* (inserzionisti con Adobe Experience Platform e [!DNL Real-Time CDP], Adobe Audience Manager o Adobe Analytics che utilizzano solo tag di conversione JavaScript per la pubblicità) Tutti i segmenti di pubblico di prime, seconde o terze parti disponibili creati in [!DNL Real-Time CDP], creato in Audience Manager o pubblicato in Adobe Experience Cloud dall&#39;Audience Manager o [!DNL Analytics].

   I prezzi per l’utilizzo dei segmenti sono prenegoziati e non sono visibili in DSP.

   Segmenti da [!DNL Analytics] sono disponibili circa un’ora dopo averli creati o pubblicati come tipi di pubblico di Experience Cloud. Segmenti provenienti direttamente dall’Audience Manager o [!DNL Real-Time CDP] sono disponibili entro 24 ore dalla loro condivisione.

   >[!NOTE]
   >
   >Consulta la documentazione per [Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-home.html), [Analytics](https://experienceleague.adobe.com/docs/analytics.html)e [la [!DNL Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/segmentation/segment-builder-guide.html) per informazioni sulla configurazione e la raccolta di dati per i segmenti in tali soluzioni.

## Dati sulle dimensioni del pubblico

Nelle impostazioni di pubblico salvate e nelle impostazioni di posizionamento, puoi visualizzare dati dettagliati sulle dimensioni del pubblico:

* Viene visualizzata la dimensione totale e attiva del pubblico deduplicato su tutti i segmenti selezionati e i tipi di pubblico salvati; puoi visualizzare i dettagli in base al tipo di dispositivo (browser, dispositivi mobili o TV connessi).

   ![dimensione del pubblico combinato](/help/dsp/assets/audience-size.png)

* Per i singoli segmenti e i tipi di pubblico salvati, accanto al nome del segmento vengono visualizzate la dimensione totale del pubblico e CPM (se applicabile). Puoi visualizzare ulteriori dettagli sul segmento, tra cui le dimensioni per tipo di dispositivo (browser, dispositivi mobili o TV connessi). Per i tipi di pubblico salvati, la dimensione totale è il totale deduplicato.

   ![la dimensione del singolo segmento](/help/dsp/assets/audience-size-segment.png)

## Visualizzazioni del pubblico

### La vista Tutti i tipi di pubblico

In [!UICONTROL All Audiences] Visualizza, o Libreria tipi di pubblico, puoi salvare e gestire tipi di pubblico riutilizzabili, che includono gruppi di segmenti di pubblico e persino altri tipi di pubblico salvati. Puoi utilizzare i tipi di pubblico come destinazioni per più posizionamenti. Il numero di posizionamenti in cui viene utilizzato ogni pubblico è indicato accanto al nome del posizionamento.

Puoi modificare, clonare, eliminare, esportare o condividere qualsiasi pubblico.

### Visualizzazione Segmenti

In [!UICONTROL Segments] visualizza , tutti gli utenti possono creare segmenti personalizzati aggiuntivi.

La [!UICONTROL Segments] visualizza inoltre un elenco dei seguenti tipi di segmenti:

* Tutti i segmenti personalizzati creati dall’utente sono disponibili per l’utente.

   Puoi visualizzare i tag di tracciamento per uno qualsiasi dei segmenti personalizzati creati e condividerli con altri utenti. Puoi anche modificare o eliminare i segmenti personalizzati creati.

   Non puoi modificare o condividere segmenti personalizzati condivisi da altri utenti con te.

* Tutti i segmenti importati di prime parti disponibili per l’utente.

   Non puoi modificare o condividere segmenti di prime parti condivisi con te. Contatta il tuo [!DNL Adobe] team dell’account per condividere segmenti di prime parti con utenti aggiuntivi.

* Tutti i segmenti personalizzati di terze parti disponibili per l’utente.

   Non puoi modificare o condividere segmenti di terze parti condivisi con te. Contatta il tuo [!DNL Adobe] team dell’account se hai bisogno di condividere segmenti di terze parti con altri utenti.

>[!MORELIKETHIS]
>
>* [Creare un pubblico riutilizzabile](reusable-audience-create.md)
>* [Impostazioni del pubblico](audience-settings.md)
>* [Sintassi per la logica del segmento di pubblico](audience-segment-logic-syntax.md)
>* [Creare e implementare un segmento personalizzato](custom-segment-create.md)
>* [Creare e implementare un [!UICONTROL CCPA Opt-Out-of-Sale] Segmento](ccpa-opt-out-segment-create.md)
>* [Fornitori di dati di terze parti disponibili](third-party-data-providers.md)
>* [Impostazioni di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md)

