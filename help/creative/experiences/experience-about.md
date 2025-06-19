---
title: Informazioni sulle esperienze in Advertising Creative
description: Scopri come configurare esperienze pubblicitarie personalizzate e ottimizzare gli elementi pubblicitari in base alle prestazioni.
feature: Creative Experiences
exl-id: 91d4b4e5-c646-4485-8149-89f41dc9c3e6
source-git-commit: 75d774a53521f1035c9f3a4f17b523ed1b68fec8
workflow-type: tm+mt
source-wordcount: '1076'
ht-degree: 0%

---

# Informazioni sulle esperienze in Advertising Creative 2.0

*Versione beta chiusa*

[!DNL Advertising Creative 2.0] fornisce due diverse strutture di esperienza per gli annunci in un&#39;unica libreria creativa.

* **Esperienze con targeting di struttura decisionale:** [!DNL Creative] ti consente di configurare esperienze pubblicitarie personalizzate in tutto il percorso di clienti utilizzando un modello di struttura decisionale. Puoi personalizzare tutti gli elementi dell’annuncio (immagini, titoli, offerte e pagine di destinazione) in base al pubblico di destinazione.

  Ad esempio, puoi specificare lo stesso pacchetto creativo per le persone di Chicago e New York che si trovano in un segmento di pubblico specifico di Adobe Analytics ma inviano le persone di Chicago a pagine di destinazione diverse rispetto ai newyorkesi. Puoi anche specificare un bundle diverso per le persone del segmento che vivono in un luogo qualsiasi eccetto Chicago e New York City, e un terzo bundle per altre persone che non fanno parte del segmento.

  Le opzioni di targeting includono:

   * I segmenti di pubblico primario da Adobe Audience Manager, Adobe Analytics e Advertising Cloud DSP

   * Posizioni geografiche specifiche, tra cui paesi, stati, DMA negli Stati Uniti, città e codici postali

   * Visualizzatori per i quali specifiche coppie chiave-valore (destinazioni del passaggio dati) vengono passate da DSP, publisher o partner (ad esempio SKU=01234567890123 o Cart=empty)

   * [!DNL Creative] pixel di retargeting e valori di attributo specificati

   * Tipi di dispositivi, sistemi operativi e browser specifici

  Dopo aver creato un ramo di pubblico target nella struttura decisionale, puoi associare il pubblico target con potenziali creativi assegnando al ramo dei bundle creativi. Per ogni esperienza, puoi personalizzare l&#39;ottimizzazione e la pianificazione per i bundle creativi e modificare le pagine di destinazione e gli URL di tracciamento predefiniti<!-- later: and any flexible attributes --> per i singoli creativi in ogni bundle.

* **Esperienze senza targeting della struttura decisionale:** [!DNL Creative] ottimizza gli elementi dell&#39;annuncio per l&#39;esperienza dell&#39;annuncio senza restringere il pubblico. Per ogni esperienza, puoi specificare le date di inizio e di fine e alcune impostazioni predefinite, ma gran parte del flusso di lavoro non si trova direttamente all’interno dell’esperienza. Invece di aggiungere creativi direttamente all&#39;esperienza, utilizza [!UICONTROL Tag Manager] per creare un tag annuncio per ogni dimensione dell&#39;esperienza e quindi aggiungervi creativi, configurare l&#39;ottimizzazione e la pianificazione creativa e personalizzare le pagine di destinazione e gli URL di tracciamento<!-- later: and any flexible attributes -->.

>[!NOTE]
>
> Poiché i due tipi di esperienze hanno flussi di lavoro diversi, non puoi trasformare un’esperienza non di destinazione in un’esperienza di destinazione né viceversa.

## Ad serving e ottimizzazione degli annunci

<!-- MORE -->
<!-- When multiple ad variants qualify for an impression -->

[!DNL Creative] fornisce annunci di prime parti e attiva annunci di terze parti per l&#39;esperienza in base al targeting specificato (se applicabile), alla pianificazione, alla rotazione degli annunci e alle opzioni degli obiettivi di ottimizzazione, nonché all&#39;inventario degli annunci disponibili.

* **Pianificazione:** (facoltativo) pianifica l&#39;esecuzione di creative specifiche durante periodi di tempo sequenziali specificati.

* **Rotazione annuncio:** Ruota le creatività manualmente in base al peso relativo o algoritmicamente in base all&#39;obiettivo di ottimizzazione specificato.

* **Obiettivo di ottimizzazione:** Ottimizzare gli elementi dell&#39;annuncio per il miglior tasso di click-through o per un [obiettivo personalizzato Advertising DSP](/help/dsp/optimization/custom-goal.md) esistente

  [!DNL Creative] ottimizza le esperienze pubblicitarie fornendo una condivisione delle impression alle risorse con le migliori prestazioni nell&#39;esperienza. Per le esperienze mirate a tipi di pubblico specifici, gli annunci possono essere ottimizzati in base alle prestazioni dei singoli elementi annuncio per i set di pubblico target. Per le esperienze senza target di pubblico specifici, gli elementi annuncio vengono ottimizzati in base esclusivamente alle prestazioni dei singoli elementi annuncio.

Ad esempio, puoi pianificare l’esecuzione di Creative 1 nelle prime due settimane per ottimizzare il tasso di click-through e di Creative 2 nelle due settimane successive per ottimizzare un obiettivo personalizzato specifico.

## Implementazione e gestione delle esperienze

Dopo aver creato un&#39;esperienza live (con tutti gli elementi annuncio richiesti), puoi [generare un tag JavaScript o iframe per l&#39;intera esperienza](experience-tag-export.md). Puoi caricare il tag esperienza come annuncio in una campagna in Adobe Advertising DSP o implementarlo come annuncio in un DSP di terze parti.

>[!NOTE]
>
>Il comportamento di targeting gerarchico può variare a seconda di DSP. Advertising DSP applica il targeting a livello di annuncio oltre al targeting a livello di posizionamento.

## Dati sulle prestazioni per le esperienze

Sono disponibili i seguenti dati sulle prestazioni:

* Quando abiliti l&#39;opzione [!UICONTROL Metrics] nella visualizzazione [!UICONTROL Creative] > [!UICONTROL Experiences], ogni scheda o riga di esperienza indica il numero di impression e clic ricevuti dall&#39;esperienza.

  ![Opzione metriche](/help/creative/assets/metrics-option.png "Opzione metriche")

* Puoi [visualizzare dati dettagliati sulle prestazioni per qualsiasi esperienza](experience-performance-details.md) dalla vista [!UICONTROL Experiences].

* Per monitorare le prestazioni nelle esperienze, crea un [report Creative personalizzato](/help/creative/report-custom-creative.md).

## Stati dell’esperienza {#experience-statuses}

Lo stato di un&#39;esperienza viene impostato automaticamente, tranne *Eliminato,* che viene impostato manualmente.

| Stato | Descrizione |
| ------ | ----------- |
| [!UICONTROL Live] | L’esperienza include tutti gli elementi necessari per generare un tag di esperienza da implementare come annuncio in un DSP. L’inizio di un’esperienza live potrebbe essere programmato per il futuro. |
| [!UICONTROL Draft] | A tutti i rami dell’esperienza non vengono assegnati dei creativi, pertanto l’esperienza è incompleta e non puoi generare un tag esperienza. |
| [!UICONTROL Processing] | Un&#39;esperienza live precedente è stata modificata ma è ora incompleta. Non puoi generare un tag esperienza per esso. **Nota:** se hai già implementato un tag di esperienza per l&#39;esperienza, è comunque possibile distribuire la versione live precedente. Se successivamente completi l’esperienza e la attivi di nuovo, la nuova versione può essere distribuita utilizzando l’implementazione di tag esistente. |
| [!UICONTROL Deleted] | L&#39;esperienza è stata eliminata da [!DNL Creative] e non è più visibile nelle visualizzazioni di [!UICONTROL Experiences]. |

>[!NOTE]
>
>È possibile modificare lo stato di un annuncio in un DSP senza influire sullo stato dell&#39;esperienza in [!DNL Creative].

## Visualizzazione [!UICONTROL Experiences]

La visualizzazione [!UICONTROL Experiences] mostra tutte le esperienze con e senza targeting. Puoi visualizzare i nomi delle esperienze, lo stato, le date di inizio e fine, il numero e le dimensioni dei creativi o dei bundle creativi assegnati e se l’esperienza include annunci dinamici. Quando abiliti l&#39;opzione [!UICONTROL Metrics] nella visualizzazione [!UICONTROL Experiences], ogni scheda o riga di esperienza indica il numero di impression e clic ricevuti dall&#39;esperienza. Quando sei in modalità scheda, puoi scorrere tra i creativi in un’esperienza con più creativi utilizzando i pulsanti &lt; e >.

Puoi creare e gestire le esperienze, nonché creare e rinominare i tag di esperienza e esportare i tag nei formati JavaScript e iframe per l’implementazione sulle DSP. Gli inserzionisti con Advertising DSP possono facoltativamente caricare tag direttamente in una campagna Advertising DSP.

### Azioni disponibili

Di seguito sono riportate le azioni chiave disponibili. Per un elenco completo, consulta il sommario del capitolo Creatività > Esperienze.

* [Scaricare i dati all’interno della visualizzazione](experience-download-view.md)

* [Crea](/help/creative/experiences/experience-create-targeting.md) e [modifica](/help/creative/experiences/experience-edit-targeting.md) un&#39;esperienza con il targeting

* [Crea](/help/creative/experiences/experience-create-no-targeting.md), [modifica](/help/creative/experiences/experience-edit-no-targeting.md) e [crea manualmente un tag annuncio](/help/creative/experiences/experience-tag-create-manually.md) per un&#39;esperienza senza targeting

* [Clona](experience-clone.md) un&#39;esperienza

* [Anteprima](experience-preview.md) di un&#39;esperienza

* [Condividi un URL demo](experience-share-demo-url.md) per un&#39;esperienza

* [Esporta tag annuncio per un&#39;esperienza](experience-tag-export.md), incluso il caricamento facoltativo di tag annuncio direttamente in una campagna Advertising DSP

* [Elimina](experience-delete.md) un&#39;esperienza

>[!MORELIKETHIS]
>
>* [Crea un&#39;esperienza con il targeting dell&#39;albero delle decisioni](experience-create-targeting.md)
>* [Crea un&#39;esperienza senza targeting](experience-create-no-targeting.md)
