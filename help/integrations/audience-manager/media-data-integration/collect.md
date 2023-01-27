---
title: Raccogliere dati di clic e impression da campagne pubblicitarie DSP
description: Scopri come acquisire le impression basate su cookie e gli eventi di clic dagli annunci pubblicitari DSP utilizzando i pixel di Audience Manager
feature: Integration with Adobe Audience Manager
exl-id: d827fbb8-b61a-4601-a42a-1ea60e4f36b7
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '1055'
ht-degree: 0%

---

# Raccolta di dati sull’esposizione dei contenuti multimediali da campagne pubblicitarie DSP

*Advertising DSP solo*

*Inserzionisti con una sola integrazione Advertising-Adobe Audience Manager di Adobe*

Questo documento spiega come assegnare tag DSP annunci pubblicitari per acquisire eventi basati su cookie e clic utilizzando pixel di Audience Manager e attività aggiuntive necessarie per utilizzare i dati.

I pixel dell’evento non acquisiscono gli eventi che si verificano in ambienti senza cookie, come le app mobili e la TV connessa (CTV).

## Passaggio 1: Impostare un’origine dati nell’Audience Manager {#set-up-data-source}

Ad Audience Manager, crea un [sorgente dati](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/datasources-list-and-settings.html) per l’impression DSP e fare clic sui dati. Includere l’ID dell’origine dati [in ciascun tag evento](#implement-dsp-pixels) in modo che tutti gli eventi tracciati siano attribuiti all&#39;origine dati.

>[!NOTE]
> È possibile raccogliere tutte le impression e fare clic sui dati per le campagne pubblicitarie in esecuzione su più DSP all’interno di una singola origine dati.

## Passaggio 2: Implementare i pixel dell’evento Impression e Clic sulle pagine web {#implement-dsp-pixels}

Gli inserzionisti possono creare e implementare tag evento per i propri marchi. Se necessario, contatta il tuo consulente Adobe Audience Manager o il tuo [!DNL Adobe] account manager per il supporto.

>[!NOTE]
>
>Se l&#39;organizzazione utilizza [!DNL Analytics] tracciamento, potrebbe non essere necessario un Audience Manager di tracciamento dei clic. Adobe Analytics acquisisce i segnali di clic e può inviarli ad Audience Manager attraverso [inoltro lato server](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html).

### Sintassi dei pixel

I pixel dell’evento devono includere i seguenti parametri.

**Pixel di tracciamento delle impression:**

`[Audience Manager customer domain].demdex.net/event?d_event=imp&d_src=[source id]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

con [parametri aggiuntivi facoltativi](#parameters) con prefisso `&`

**Pixel di tracciamento dei clic:**

`[Audience Manager customer domain].demdex.net/event?d_event=click&d_src=[source id]&d_rd=[redirect URL]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

con [parametri aggiuntivi facoltativi](#parameters) con prefisso `&`

Dove:

* `[Audience Manager customer domain]` è il nome di dominio a cui invieranno gli eventi impression o click [!DNL Adobe].

* `[source id]` è l&#39;ID per [sorgente dati](#set-up-data-source) in cui potrai tenere traccia DSP impression e fare clic sui dati.

* `[redirect URL]` è l&#39;URL di reindirizzamento con doppia codifica. Se utilizzi uno strumento di codifica online, ad esempio www.urlencoder.org, esegui la stringa attraverso il codificatore e codifica nuovamente il risultato.

* `${TM_CAMPAIGN_ID_NUM}` è l&#39;ID numerico della campagna in DSP. Se desideri codificare un singolo ID campagna invece di utilizzare la macro DSP, individua l&#39;ID nelle impostazioni della campagna.

* Ogni [parameter](#key-value-pairs) è preceduto da `&` ed è nel formato `d_parameter=parameter_id`, dove `parameter` viene sostituito dalla coppia chiave-valore per il nuovo campo. Esempio: `&d_placement=${TM_PLACEMENT_ID_NUM}`

### Parametri come coppie chiave-valore {#parameters}

**Formato:**  `d_parameter=parameter_id`

    dove:
    
    * Il parametro ha il prefisso `&amp;`
    
    * `parameter` viene sostituito dalla coppia chiave-valore per il nuovo campo
    
    Esempio: `&amp;d_placement=${TM_PLACEMENT_ID_NUM}`

Entrambi i tipi di pixel possono contenere parametri aggiuntivi, come *coppie chiave-valore* raccogliere le caratteristiche o fornire i metadati della campagna (ad esempio un nome di posizionamento o una campagna) per altri rapporti. Una coppia chiave-valore è costituita da due elementi correlati: a *key*, che è una costante che definisce il set di dati, e un *value*, che è una variabile che appartiene al set.

Nella coppia chiave-valore, la variabile valore può essere un ID hardcoded o un *macro*, che è una piccola unità di codice indipendente che viene sostituita dinamicamente con i valori corrispondenti quando il tag dell’annuncio viene caricato per la campagna e il tracciamento degli utenti. Per i parametri relativi alla campagna, puoi utilizzare [Macro DSP](/help/dsp/campaign-management/macros.md) anziché utilizzare le macro di Audience Manager per inviare gli attributi della campagna insieme all’impression corrispondente o fare clic sui dati per Audience Manager, utilizzando un singolo pixel in tutti gli annunci. Le macro DSP inserite nei pixel dell’evento devono essere valori appropriati per le coppie chiave-valore incluse nei pixel. Ad esempio, per `d_placement` chiave, si utilizzerebbe la macro DSP `${TM_PLACEMENT_ID_NUM}` come valore per acquisire gli ID di posizionamento generati dalla macro Adobe Advertising.

Per un elenco delle macro supportate, ad Audience Manager, dai pixel dell’evento impression, vedere &quot;[Acquisizione dei dati di impression delle campagne tramite chiamate pixel](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html#supported-key-value-pairs).&quot;

Per un elenco delle macro supportate ad Audience Manager per i pixel dell&#39;evento click, vedere &quot;[Acquisizione dei dati di clic delle campagne tramite chiamate pixel](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/click-data-pixels.html).&quot;

>[!TIP]
>
>* La procedura consigliata consiste nell’includere la campagna, il posizionamento, la creatività (ad) e gli ID del sito, in modo da poter utilizzare gli attributi della campagna per creare caratteristiche di Audience Manager.
>* Per creare rapporti di Audience Optimization, sono necessari parametri aggiuntivi.
>* Nelle coppie chiave-valore, sostituisci i valori con i valori pertinenti [Macro DSP](/help/dsp/campaign-management/macros.md) puoi quindi utilizzare un singolo pixel in tutti gli annunci in tutte le campagne. Ad esempio, modifica `d_campaign=[%campaignID%]`a `d_campaign=${TM_CAMPAIGN_ID_NUM}` per acquisire gli ID della campagna generati dalla macro Adobe Advertising.
>* Se necessario, puoi creare parametri personalizzati con valori hardcoded. Esempio: `d_DSP=AdCloud`


Esempio di pixel evento impression:

`http://acme.demdex.net/event?d_event=imp&d_src=1052880&d_site=${TM_SITE_ID_NUM}&d_creative=${TM_AD_ID_NUM}&d_placement=${TM_FEED_ID_NUM}&d_campaign=${TM_CAMPAIGN_ID_NUM}&d_DSP=AdCloud&d_bust=${TM_RANDOM}`

### Dove aggiungere i pixel

#### Pixel di tracciamento delle impression

Allega un pixel di tracciamento degli eventi di impression a tutti gli annunci nel tuo [!DNL DSP] campagne. Puoi eseguire questa operazione in uno dei seguenti punti:

* A livello di posizionamento, che applica il pixel per impostazione predefinita a tutti gli annunci nella posizione. Nella sezione Tracking delle impostazioni di posizionamento , aggiungi il pixel nel [[!UICONTROL Event pixels] field](/help/dsp/campaign-management/placements/placement-settings.md).

* A livello di annuncio, che esclude qualsiasi pixel evento a livello di posizionamento. Nelle impostazioni dell’annuncio, [crea un pixel evento sul [!UICONTROL Pixel] scheda](/help/dsp/campaign-management/ads/ad-edit.md).

* (Per annunci su un server di annunci di terze parti) A livello di annuncio all&#39;interno del server di annunci.

#### Pixel di tracciamento dei clic

All&#39;interno del server di annunci, inserisci il pixel dell&#39;evento click (con l&#39;URL codificato aggiunto) ovunque normalmente si inserisca l&#39;URL di click-through dell&#39;annuncio.

## Passaggio 3: Attività post-implementazione

Una volta implementati i tag evento, i dati vengono riversati nei server di raccolta dati di Audience Manager. Completa le seguenti attività prima di poter utilizzare i dati nei rapporti.

### Crea un [!DNL Amazon S3] Intervallo e origine dati

Una volta che i dati sono presenti sui server di Audience Manager, devi creare un [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3]), e quindi un’origine dati, a cui verranno inviati tutti i dati pixel. Contatta il tuo consulente Audience Manager o [Assistenza clienti](https://experienceleague.adobe.com/docs/audience-manager/user-guide/help-and-legal/help-legal-contact.html) se hai bisogno di supporto.

### Creare caratteristiche e segmenti di Audience Manager

I dati dell’evento fluiranno in Audience Manager come [segnali non utilizzati](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/interactive-and-overlap-reports/unused-signals.html). Creare manualmente [caratteristiche basate su regole](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) dai dati acquisiti, quindi crea [segmenti](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segments-purpose.html) utilizzare queste caratteristiche, prima di poter utilizzare i dati nei rapporti.

Caratteristica di esempio che popola i dati a livello di utente per gli utenti esposti a un creativo specifico in DSP:

1. Identifica l’evento come `d_event = imp`.
1. Identifica l’ID creativo all’interno della campagna di DSP, quindi mappalo sulla caratteristica come `d_creative=[Creative ID]`.

![Schermata di creazione delle caratteristiche](/help/dsp/assets/aa-trait.png)

>[!MORELIKETHIS]
>
>* [Macro DSP](/help/dsp/campaign-management/macros.md)
>* [Panoramica sull’invio DSP dati di esposizione a contenuti multimediali a Adobe Audience Manager](overview.md)
>* [Casi d&#39;uso](use-cases.md)

