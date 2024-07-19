---
title: Utilizzo di  [!DNL Roku] Inventario
description: Scopri la partnership dell'DSP con  [!DNL Roku], incluse le opzioni di inventario, i fornitori di tracciamento di terze parti approvati e le best practice per i posizionamenti specifici di  [!DNL Roku].
feature: DSP On Demand Inventory, DSP Private Inventory
exl-id: e7a1aa80-d7f0-4a4e-96b1-6b362a32106e
source-git-commit: f3099c84fe2d6b1610ddf4ca07d59b119718afee
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---

# Utilizzo dell&#39;inventario [!DNL Roku]

Advertising DSP fornisce funzionalità per la pubblicità su [!DNL Roku].

## Corrispondenza pubblico

La relazione tra [!DNL Roku] e DSP corrisponde ai tipi di pubblico di [!DNL DSP] a [!DNL Roku] ID per il targeting deterministico del pubblico 1:1 nell&#39;inventario di [!DNL Roku].

## [!DNL Roku] opzioni di inventario

È possibile a) impostare ID offerta privati direttamente con [!DNL Roku] e quindi immettere i dati ID offerta in DSP oppure b) visitare la raccolta [!DNL On Demand] per iscriversi a [!DNL Roku] profili:

>[!NOTE]
>
>L&#39;inventario [!DNL Roku] non è disponibile nei mercati aperti e negli scambi.

* Per le tue offerte private, [imposta le informazioni sugli ID offerta in DSP](/help/dsp/inventory/deal-id-create.md) e quindi esegui la destinazione &quot;[!UICONTROL Roku Network - Audience]&quot; e &quot;[!UICONTROL The Roku Channel - Audience]&quot; entro [!DNL Roku] posizionamenti.<!-- Or do you target the deal ID?? I see those strings for Roku On Demand inventory. Clarify if all Roku private deals show up as one or the other of these in Roku Private inventory in Roku placement settings. -->

* Puoi [abbonarti al seguente [!DNL Roku] inventario all&#39;interno della [!DNL On Demand] Galleria](/help/dsp/inventory/on-demand-inventory-subscribe.md), quindi eseguire il targeting delle offerte approvate entro [!DNL Roku] posizionamenti:

   * &quot;[!UICONTROL Roku Network - Audience]&quot; per l&#39;inventario nell&#39;ecosistema [!DNL Roku] con partner di contenuti premium, ad esempio [!DNL The CW], [!DNL ABC] e [!DNL ESPN].
   * &quot;[!UICONTROL The Roku Channel - Audience]&quot; per il contenuto dell&#39;app di proprietà e gestione (O&amp;O) di [!DNL Roku].

### Vantaggi della personalizzazione di Marketplace privati con [!DNL Roku]

Le offerte private ti consentono di personalizzare i parametri dell’offerta in base alle tue esigenze.

* **Prezzi negoziati:** Collabora con il team di vendita [!DNL Roku] per negoziare e strutturare un accordo che soddisfi le tue esigenze della campagna.

* **Priorità scala:** i mercati privati (PMP) ricevono priorità maggiore rispetto alle offerte sempre attive (ad esempio [!DNL On Demand] offerte).

* **Gestione frequenza:** Il limite di frequenza predefinito di [!DNL Roku] è un (1) annuncio per 30 minuti per utente, ma puoi personalizzarlo per ora, giorno, settimana, mese o intero periodo di volo.<!-- Within the DSP placement settings? NO - you negotiate this with Roku, but Christine to confirm with Amanda whether you should be able to edit this in placement. -->

* Targeting dati **[!DNL Roku]:** I tipi di pubblico [!DNL Roku] sono generati da [!DNL Roku] segnali TV e dispositivo, dati tracciati da [!DNL The Roku Channel] (ad esempio affinità per il genere TV, comportamento TV in streaming e stato di abbonamento via cavo) e dati aggiuntivi dal sistema CRM (Customer Relationship Management) [!DNL Roku].

* **[!DNL Roku]Targeting dei contenuti:** Le offerte private possono essere indirizzate alle app in base al genere, all&#39;applicazione dell&#39;app, agli eventi di elenco Bloccati, agli eventi stagionali e ai tentipoli e vengono mostrate solo in [!DNL The Roku Channel].

## [!DNL Roku] posizionamenti

Nelle campagne DSP, [crea [!DNL Roku] posizionamenti specifici](/help/dsp/campaign-management/placements/placement-create.md) utilizzando il tipo di posizionamento &quot;[!UICONTROL Connected TV (Roku)]&quot;. Includi [!DNL Roku] posizionamenti in pacchetti specifici per [!DNL Roku] con obiettivi definiti.

Ogni posizionamento [!DNL Roku] deve avere come destinazione almeno un&#39;offerta o origine [!DNL Roku]. Per utilizzare la corrispondenza del pubblico dell&#39;DSP con [!DNL Roku], includere uno o più segmenti di pubblico che possono essere associati al set di dati deterministico [!DNL Roku] (consenso).

### [!DNL Roku] fornitori di tracciamento terze parti approvati

I posizionamenti [!DNL Roku] possono includere pixel evento di terze parti e pixel di conversione dei seguenti fornitori: [!DNL Acxiom], [!DNL Comscore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk] e [!DNL Research Now].

### Best practice per strategia di posizionamento

Di seguito sono riportate le procedure consigliate per i posizionamenti specifici di [!DNL Roku].

Per massimizzare la portata incrementale:

* Elimina i tipi di pubblico esposti in [!DNL Roku O&O] escludendo quelli già raggiunti con [!DNL The Roku Channel].

* Elimina i tipi di pubblico esposti su [!DNL All Roku] escludendo quelli già raggiunti nella piattaforma [!DNL Roku].

Per la configurazione più veloce:

* Effettua il targeting delle offerte esistenti e sempre attive per [!DNL The Roku Channel] in [[!DNL On Demand] Inventario](/help/dsp/inventory/on-demand-inventory-subscribe.md) per accedere rapidamente a [!DNL Roku] inventario posseduto e gestito.
* Effettua il targeting delle offerte sempre attive per [!DNL Roku Network] in [[!DNL On Demand] Inventario](/help/dsp/inventory/on-demand-inventory-subscribe.md) per ottenere rapidamente la scalabilità nella piattaforma [!DNL Roku].

Alla scala massima:

* Personalizzare un marketplace privato [!DNL Roku] per l&#39;accesso prioritario alla fornitura [!DNL Roku] a un prezzo negoziato.

>[!MORELIKETHIS]
>
>* [Crea manualmente dettagli ID offerta](/help/dsp/inventory/deal-id-create.md)
> * [Abbonati e richiedi l&#39;accesso alle [!DNL On Demand] Offerte di magazzino Premium](/help/dsp/inventory/on-demand-inventory-subscribe.md)
>* [Crea un posizionamento](/help/dsp/campaign-management/placements/placement-create.md)
