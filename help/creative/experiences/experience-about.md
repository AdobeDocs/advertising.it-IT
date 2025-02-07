---
title: Informazioni sulle esperienze in Advertising Creative
description: Scopri come configurare esperienze pubblicitarie personalizzate e ottimizzare gli elementi pubblicitari in base alle prestazioni.
feature: Creative Experiences
source-git-commit: fbf663b38282f48facab57efaf5533892642a252
workflow-type: tm+mt
source-wordcount: '804'
ht-degree: 0%

---

# Informazioni sulle esperienze in Advertising Creative 2.0

*Versione beta chiusa*

<!-- Revisit Description metadata -->

<!-- MORE -->

[!DNL Advertising Creative 2.0] fornisce due diverse strutture di esperienza pubblicitaria per gli annunci nella libreria creativa<!-- can use a single library only -->:

* **Esperienze con targeting di struttura decisionale:** [!DNL Creative] ti consente di configurare esperienze pubblicitarie personalizzate in tutto il percorso di clienti utilizzando un modello di struttura decisionale. Puoi personalizzare tutti gli elementi dell’annuncio (immagini, titoli, offerte e pagine di destinazione) in base al pubblico di destinazione.

  Ad esempio, puoi specificare lo stesso bundle creativo per le persone di Chicago e New York che si trovano in un segmento di pubblico specifico di Adobe Analytics ma inviano persone a Chicago che si trovano nello stesso segmento a pagine di destinazione diverse rispetto ai newyorkesi. Puoi anche specificare un bundle diverso per le persone del segmento che vivono in un luogo qualsiasi eccetto Chicago e New York City, e un terzo bundle per altre persone che non fanno parte del segmento.

  Le opzioni di targeting includono i visualizzatori nei segmenti di pubblico di prime parti da Adobe Audience Manager, Adobe Analytics e Advertising Cloud DSP; i visualizzatori in posizioni geografiche specifiche, tra cui paesi, stati, DMA negli Stati Uniti, città e codici postali; i visualizzatori per i quali vengono passate coppie chiave-valore specifiche (target dei passaggi dati) dall’DSP, dall’editore o dal partner; i visualizzatori con [!DNL Creative] pixel di retargeting e valori di attributo specificati; e i visualizzatori con tipi di dispositivo, sistemi operativi e browser specifici.

  Puoi assegnare bundle creativi a ogni esperienza, personalizzando facoltativamente l&#39;ottimizzazione e la pianificazione per i bundle creativi e modificando le pagine di destinazione e gli URL di tracciamento predefiniti<!-- and any flexible attributes --> per i singoli creativi in ogni bundle.

* **Esperienze senza targeting della struttura decisionale:** [!DNL Creative] ottimizza gli elementi dell&#39;annuncio per l&#39;esperienza dell&#39;annuncio senza restringere il pubblico.<!-- For first-party creatives, [!DNL Creative] serves the ads. --> Puoi specificare le date di inizio e fine e alcune impostazioni predefinite per ogni esperienza, ma gran parte del flusso di lavoro non si trova direttamente all&#39;interno dell&#39;esperienza. Invece di aggiungere creativi direttamente all&#39;esperienza, puoi creare un tag annuncio per ogni dimensione dell&#39;esperienza, quindi aggiungervi creativi, configurare l&#39;ottimizzazione e la pianificazione creative e personalizzare le pagine di destinazione e gli URL di tracciamento dall&#39;interno di [!UICONTROL Tag Manager].

## Ottimizzazione degli annunci

<!-- MORE -->
[!DNL Creative] ottimizza gli elementi dell&#39;annuncio per qualsiasi esperienza in base alle prestazioni. Per le esperienze mirate a tipi di pubblico specifici, gli annunci possono essere ottimizzati in base alle prestazioni dei singoli elementi annuncio per i set di pubblico target. Per le esperienze senza target di pubblico specifici, gli elementi dell’annuncio vengono ottimizzati in base alle sole prestazioni dei singoli elementi dell’annuncio.

## Implementazione e gestione delle esperienze

Dopo aver creato un&#39;esperienza live (con tutti gli elementi di annuncio richiesti), puoi [generare un tag JavaScript o iframe per l&#39;intera esperienza](experience-tag-export.md), che puoi facoltativamente caricare come annuncio in una campagna in Adobe Advertising DSP o implementare come annuncio in un DSP di terze parti. [!DNL Creative] fornisce annunci per l&#39;esperienza in base alle opzioni di targeting e rotazione degli annunci e all&#39;inventario degli annunci disponibili.

## Dati sulle prestazioni per le esperienze

Quando abiliti l&#39;opzione [!UICONTROL Metrics] nella visualizzazione [!UICONTROL Experiences], ogni scheda o riga di esperienza indica il numero di impression e clic ricevuti dall&#39;esperienza.

![Opzione metriche](/help/creative/assets/metrics-option.png "Opzione metriche")

<!-- insert screen shot of Metrics option?  If not, then add instructions elsewhere -->

<!-- I don't see this as of 1/9; why only in the table view?   You can also add conversion columns in the table view. -->

È possibile visualizzare dati dettagliati sulle prestazioni per qualsiasi esperienza dalla vista [!UICONTROL Creative] > [!UICONTROL Experiences]. Per monitorare le prestazioni nelle esperienze, creare un [!UICONTROL Custom Creative Report].

<!--
You can [view detailed performance data for any experience](experience-view-report.md) from the Creative > Experiences view. To monitor performance across your experiences, [create custom reports](/help/dsp/reports/report-create.md).
-->

## Stati dell’esperienza {#experience-statuses}

<!-- verify that these are all still the same -->

Lo stato di un&#39;esperienza viene impostato automaticamente, ad eccezione di *eliminato,* impostato manualmente.

*Live:* L&#39;esperienza include tutti gli elementi necessari, quindi puoi generare un tag esperienza da implementare come annuncio in un DSP. <!-- A live experience may be scheduled to start in the future -->

*Bozza:* a tutti i rami dell&#39;esperienza non vengono assegnati creativi, pertanto l&#39;esperienza è incompleta e non puoi generare un tag esperienza.

*Elaborazione:* Un&#39;esperienza live in precedenza è stata modificata ma è ora incompleta. Non puoi generare un tag esperienza per esso. **Nota:** se hai già implementato un tag di esperienza per l&#39;esperienza, la versione live precedente verrà comunque distribuita. Se in un secondo momento completi l’esperienza, riattivandola, la nuova versione verrà distribuita utilizzando l’implementazione di tag esistente.

*Eliminata:* L&#39;esperienza è stata eliminata da [!DNL Creative] e non è più visibile nelle visualizzazioni di [!UICONTROL Experiences].

>[!NOTE]
>
>È possibile modificare lo stato di un annuncio in un DSP senza influire sullo stato dell&#39;esperienza in [!DNL Creative].

## Visualizzazione [!UICONTROL Experiences]

La visualizzazione [!UICONTROL Experiences] mostra tutte le esperienze con e senza targeting. Puoi visualizzare i nomi delle esperienze, lo stato, le date di inizio e fine, il numero e le dimensioni dei creativi o dei bundle creativi assegnati e se l’esperienza include annunci dinamici. Quando abiliti l&#39;opzione [!UICONTROL Metrics] nella visualizzazione [!UICONTROL Experiences], ogni scheda o riga di esperienza indica il numero di impression e clic ricevuti dall&#39;esperienza.

Puoi creare e gestire le tue esperienze, tra cui l’ottimizzazione e l’assegnazione di creativi e bundle creativi alle tue esperienze. Puoi anche creare e rinominare i tag di esperienza degli annunci ed esportare i tag in formati JavaScript e iframe per l’implementazione nell’DSP. Gli inserzionisti con Advertising DSP possono facoltativamente caricare tag direttamente in una campagna Advertising DSP come annunci.

<!--
### Available actions

* [Download data within the view](experience-download-view.md)

        + [Assign and unassign creative bundles to a final node](/help/creative/experiences/experience-assign-creative-bundles.md)
* Experiences with decision tree targeting: [Create](/help/creative/experiences/experience-create-targeting.md) and [edit](/help/creative/experiences/experience-edit-targeting.md) experiences, [assign and unassign creative bundles](/help/creative/experiences/experience-assign-creative-bundles.md), [customize creative optimization and scheduling](/help/creative/experiences/experience-optimization-scheduling-targeting.md), and [customize the tracking URLs for creatives](/help/creative/experiences/experience-tracking-urls-targeting.md)

* Experiences without decision tree targeting: [Create](experience-create-no-targeting.md) and [edit](/help/creative/experiences/experience-edit-no-targeting.md)

* [Clone](experience-clone.md) an experience

* [Preview](experience-preview.md) an experience

* [Share a demo URL](experience-share-demo-url.md) for an experience

* [Export ad tags for an experience](experience-tag-export.md)

* [Delete](experience-delete.md) an experience

-->

<!-- You can add or remove labels for your experiences.-->

<!-- Add links to workflows once they're done -->

>[!MORELIKETHIS]
>
>* [Crea un&#39;esperienza con il targeting dell&#39;albero delle decisioni](experience-create-targeting.md)
>* [Crea un&#39;esperienza senza targeting](experience-create-no-targeting.md)
