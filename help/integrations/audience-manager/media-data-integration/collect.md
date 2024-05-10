---
title: Raccogliere dati di clic e impression dalle campagne Advertising DSP
description: Scopri come acquisire impression basate su cookie e eventi di clic dagli annunci Advertising DSP utilizzando pixel di Audience Manager
feature: Integration with Adobe Audience Manager
exl-id: d827fbb8-b61a-4601-a42a-1ea60e4f36b7
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '997'
ht-degree: 0%

---

# Raccogliere dati sull’esposizione multimediale dalle campagne pubblicitarie DSP

*Inserzionisti solo con Advertising DSP*

*Per gli inserzionisti con una sola integrazione Adobi Advertising-Adobe Audience Manager*

Questo documento spiega come assegnare i tag agli annunci DSP di Advertising per acquisire impression basate su cookie e eventi di clic utilizzando pixel Audienci Manager, e altre attività necessarie per utilizzare i dati.

I pixel dell’evento non acquisiscono gli eventi che si verificano in ambienti senza cookie, come le app mobili e la TV collegata (CTV).

## Passaggio 1: configurare un’origine dati in Audienci Manager {#set-up-data-source}

Ad Audience Manager, crea un’ [origine dati](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/datasources-list-and-settings.html) per i dati relativi alle impression e ai clic dell’DSP. Includi ID origine dati [in ogni tag evento](#implement-dsp-pixels) in modo che tutti gli eventi tracciati vengano attribuiti all’origine dati.

>[!NOTE]
> È possibile raccogliere tutti i dati sulle impression e sui clic per campagne pubblicitarie eseguite su più DSP all’interno di un’unica sorgente di dati.

## Passaggio 2: implementare i pixel dell’evento Impression and Click sulle pagine web {#implement-dsp-pixels}

Gli inserzionisti possono creare e implementare tag evento per i propri marchi. Se necessario, contatta il tuo consulente Adobe Audience Manager o il team dell’account Adobe per richiedere assistenza.

>[!NOTE]
>
>Se l’organizzazione utilizza [!DNL Analytics] tracciamento, potrebbe non essere necessario il tracciamento dei clic di Audience Manager. Adobe Analytics acquisisce i segnali di clic e può inviarli agli Audienci Manager tramite [inoltro lato server](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html).

### Sintassi pixel

I pixel dell’evento devono includere i seguenti parametri.

**Pixel di tracciamento dell’impression:**

`[Audience Manager customer domain].demdex.net/event?d_event=imp&d_src=[source id]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

con [parametri aggiuntivi facoltativi](#parameters) con prefisso `&`

**pixel di tracciamento dei clic:**

`[Audience Manager customer domain].demdex.net/event?d_event=click&d_src=[source id]&d_rd=[redirect URL]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

con [parametri aggiuntivi facoltativi](#parameters) con prefisso `&`

Dove:

* `[Audience Manager customer domain]` è il nome di dominio che invierà gli eventi impression o clic a [!DNL Adobe].

* `[source id]` è l’ID per [origine dati](#set-up-data-source) in cui tieni traccia delle impression dell’DSP e fai clic sui dati.

* `[redirect URL]` è l’URL di reindirizzamento con doppia codifica. Se utilizzi uno strumento di codifica online, ad esempio www.urlencoder.org, esegui la stringa attraverso il codificatore e codifica nuovamente il risultato.

* `${TM_CAMPAIGN_ID_NUM}` è l’ID numerico della campagna nell’DSP. Se desideri codificare un singolo ID campagna invece di utilizzare la macro DSP, individualo nelle impostazioni della campagna.

* Ogni [parametro](#key-value-pairs) ha il prefisso `&` ed è nel formato `d_parameter=parameter_id`, dove `parameter` viene sostituito dalla coppia chiave-valore per il nuovo campo. Esempio: `&d_placement=${TM_PLACEMENT_ID_NUM}`

### Parametri come coppie chiave-valore {#parameters}

**Formato:**  `d_parameter=parameter_id`

    dove:
    
    * il parametro ha il prefisso &quot;&amp;&quot;
    
    * &quot;parameter&quot; è sostituito dalla coppia chiave-valore per il nuovo campo
    
    Esempio: `&amp;d_placement=${TM_PLACEMENT_ID_NUM}`

Entrambi i tipi di pixel possono contenere parametri aggiuntivi, come *coppie chiave-valore* per raccogliere caratteristiche o fornire metadati della campagna (come un nome di posizionamento o un nome di campagna) per altri rapporti. Una coppia chiave-valore è costituita da due elementi correlati: *chiave*, costante che definisce il set di dati e una costante *valore*, che è una variabile appartenente al set.

Nella coppia chiave-valore, la variabile valore può essere un ID hardcoded o un *macro*, è una piccola unità di codice autonomo che viene sostituito dinamicamente con i valori corrispondenti quando il tag dell’annuncio viene caricato per il tracciamento della campagna e dell’utente. Per i parametri relativi alla campagna, puoi utilizzare [Macro per DSP](/help/dsp/campaign-management/macros.md) invece di macro di Audience Manager per inviare attributi di campaign con l’impression corrispondente o dati di clic per l’Audience Manager, utilizzando un singolo pixel in tutti gli annunci. Le macro dell’DSP inserite nei pixel dell’evento devono essere valori appropriati per le coppie chiave-valore incluse all’interno dei pixel. Ad esempio, per `d_placement` chiave, si utilizza la macro DSP `${TM_PLACEMENT_ID_NUM}` come valore per acquisire gli ID di posizionamento generati dalla macro Adobi Advertising.

Per un elenco delle macro supportate da Audienci Manager per i pixel dell’evento di impression, vedi &quot;[Acquisizione dei dati di impression delle campagne attraverso chiamate pixel](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html#supported-key-value-pairs).&quot;

Per un elenco delle macro supportate da Audienci Manager per i pixel dell&#39;evento clic, vedere &quot;[Acquisizione dei dati di clic delle campagne tramite chiamate pixel](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/click-data-pixels.html).&quot;

>[!TIP]
>
>* La best practice prevede l’inclusione degli ID della campagna, del posizionamento, della creatività (annuncio) e del sito, in modo da poter utilizzare gli attributi della campagna per creare caratteristiche Audienci Manager.
>* Per creare rapporti Audienci Optimization, sono necessari parametri aggiuntivi.
>* Nelle coppie chiave-valore, sostituisci i valori con i pertinenti [Macro per DSP](/help/dsp/campaign-management/macros.md) in modo da poter utilizzare un singolo pixel in tutti gli annunci di tutte le campagne. Ad esempio, modifica `d_campaign=[%campaignID%]`a `d_campaign=${TM_CAMPAIGN_ID_NUM}` per acquisire gli ID campagna generati dalla macro Adobi Advertising.
>* Se necessario, puoi creare parametri personalizzati con valori hardcoded. Esempio: `d_DSP=AdCloud`

Esempio di un pixel evento di impression:

`http://acme.demdex.net/event?d_event=imp&d_src=1052880&d_site=${TM_SITE_ID_NUM}&d_creative=${TM_AD_ID_NUM}&d_placement=${TM_FEED_ID_NUM}&d_campaign=${TM_CAMPAIGN_ID_NUM}&d_DSP=AdCloud&d_bust=${TM_RANDOM}`

### Dove aggiungere i pixel

#### Pixel di tracciamento dell&#39;impression

Allega un pixel di tracciamento degli eventi di impression a tutti gli annunci nel tuo [!DNL DSP] campagne. Puoi eseguire questa operazione in una delle seguenti posizioni:

* Al livello di posizionamento, che applica il pixel per impostazione predefinita a tutti gli annunci nel posizionamento. Nella sezione Tracciamento delle impostazioni di posizionamento, aggiungi il pixel nel [[!UICONTROL Event pixels] campo](/help/dsp/campaign-management/placements/placement-settings.md).

* A livello di annuncio, che sostituisce tutti i pixel evento a livello di posizionamento. Nelle impostazioni annuncio, [creare un pixel evento sul [!UICONTROL Pixel] scheda](/help/dsp/campaign-management/ads/ad-edit.md).

* (Per annunci su un server di annunci di terze parti) A livello di annuncio all’interno del server di annunci.

#### Pixel tracciamento clic

All’interno dell’ad server, inserisci il pixel dell’evento clic (con l’URL codificato aggiunto) ovunque inserisci normalmente l’URL di click-through dell’annuncio.

## Passaggio 3: attività successive all’implementazione

Una volta implementati i tag evento, i dati fluiscono nei server di raccolta dati di Audienci Manager. Completa le seguenti attività prima di poter utilizzare i dati nei rapporti.

### Creare un [!DNL Amazon S3] Bucket e origine dati

Una volta che i dati si trovano sui server Audienci Manager, è necessario creare un’ [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3]) e quindi un&#39;origine dati alla quale vengono inviati tutti i dati in pixel. Contatta il tuo consulente Audienci Manager o [Assistenza clienti](https://experienceleague.adobe.com/docs/audience-manager/user-guide/help-and-legal/help-legal-contact.html) se hai bisogno di supporto.

### Creazione di segmenti e caratteristiche Audienci Manager

I dati dell’evento fluiscono in Audienci Manager come [segnali non utilizzati](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/interactive-and-overlap-reports/unused-signals.html). Crea manualmente [caratteristiche basate su regole](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) dai dati acquisiti, quindi crea [segmenti](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segments-purpose.html) utilizzando tali caratteristiche, prima di poter utilizzare i dati nei rapporti.

Caratteristica di esempio che popola i dati a livello di utente per gli utenti esposti a un contenuto creativo specifico nell’DSP:

1. Identifica l’evento come `d_event = imp`.
1. Identifica l’ID creativo all’interno della campagna DSP e quindi mappalo sulla caratteristica come `d_creative=[Creative ID]`.

![Schermata di creazione delle caratteristiche](/help/dsp/assets/aa-trait.png)

>[!MORELIKETHIS]
>
>* [Macro per DSP](/help/dsp/campaign-management/macros.md)
>* [Panoramica dell’invio dei dati sull’esposizione ai contenuti multimediali dell’DSP a Adobe Audience Manager](overview.md)
>* [Casi d’uso](use-cases.md)
