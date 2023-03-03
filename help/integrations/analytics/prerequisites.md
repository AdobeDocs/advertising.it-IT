---
title: Prerequisiti e informazioni chiave per l’implementazione [!DNL Analytics for Advertising]
description: Prerequisiti e informazioni chiave per l’implementazione [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 7c477900-ebb0-4c0e-811a-ab8bc6069599
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '842'
ht-degree: 0%

---

# Prerequisiti e informazioni chiave per l’implementazione [!DNL Analytics for Advertising]

*Inserzionisti con Advertising DSP e[!DNL Advertising Search]*

Leggi le seguenti informazioni prima di integrare Adobe Advertising con Adobe Analytics.

## Requisiti per il reporting di dati pubblicitari di Adobi in [!DNL Analytics]

* una delle seguenti situazioni:
   * Adobe Experience Platform Web SDK: `alloy.js`
   * Servizio Experience Cloud Identity: `visitorAPI.js` versione 2.0 o successiva
* Qualsiasi versione di Adobe Analytics (incluso [!DNL Prime], [!DNL Premium], o [!DNL Ultimate])
* Adobe Analytics: `appMeasurement.js` versione 2.1 o successiva

>[!TIP]
>
>Per migliorare la fedeltà dei dati, utilizza la versione più recente di ciascuna libreria.

## Requisiti per la condivisione dei segmenti di Analytics con Adobe Advertising

* Servizio Experience Cloud Identity: `visitorAPI.js` versione 2.1 o successiva
* Adobe Analytics: `appMeasurement.js` versione 1.8 o successiva

## Requisiti per la comunicazione [!DNL Analytics] Dati in Adobe Advertising

Fornisci al team di implementazione di Advertising di Adobe quanto segue:

* Il [!DNL Analytics] ID suite di rapporti che verrà utilizzato per generare rapporti sull’attività dei media a pagamento e per alimentare l’attività del sito ai fini di ottimizzazione e reporting in Adobe Advertising
* L’ID organizzazione Experience Cloud (ID organizzazione) della società.

Puoi trovare entrambi questi ID sulla [Scheda Riepilogo di Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html).

![Schermata Riepilogo Experience Cloud Debugger](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Dati in Adobe Advertising {#lookback-a4adc}

Perché [!DNL Analytics] I dati vengono inviati ad Adobe Advertising per il reporting e l’ottimizzazione. I dati sono soggetti alle regole di attribuzione, inclusi gli intervalli di lookback di impression e clic, configurati per l’inserzionista in Adobe Advertising.

![impostazioni dell’intervallo di lookback a livello di inserzionista in Adobe Advertising](/help/integrations/assets/a4adc-lookbacks.png)

* Adobe Intervallo di lookback dell’attribuzione di Advertising: numero di giorni dopo il primo clic in cui il clic può essere attribuito a una conversione. Per impostazione predefinita, questo valore è 60 giorni; il massimo è 90 giorni
* Adobe di intervallo di lookback dell’impression di attribuzione di Advertising: numero di giorni dopo i quali si verifica un’impression pubblicitaria, in cui l’impression può essere attribuita a una conversione. Per impostazione predefinita, questo valore è 14 giorni; il massimo è 30 giorni

   >[!NOTE]
   >
   > L’intervallo di lookback dell’impression è specifico per Adobe Advertising, non [!DNL Analytics for Advertising], reporting.

Il [!DNL Analytics for Advertising] JavaScript utilizza queste impostazioni per determinare quanto indietro nel tempo considera valida una voce view-through o una voce click-through nel sito. Per ulteriori informazioni su come vengono determinate le visite e i click-through, vedi &quot;[Adobe di ID pubblicitari utilizzati da Analytics](ids.md).&quot;

## Adobe di dati pubblicitari in [!DNL Analytics]

[!DNL Analytics] imposta gli ID Adobe Advertising ID (AMO ID) all’interno dell’hit Analytics, in base all’impostazione di persistenza degli eVar dell’inserzionista, che si applica sia ai click-through che alle visualizzazioni. L’impostazione di persistenza è configurata nel back-end Adobe Advertising e il team dell’account Adobe può modificarla.

* [!DNL Analytics for Advertising] Scadenza eVar: 60 giorni per impostazione predefinita per gli AMO ID

>[!NOTE]
>
>Per segmentare i dati per un arco temporale diverso, puoi [impostare segmenti personalizzati](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) con diversi intervalli di lookback all’interno di Analysis Workspace.

## Ambienti pubblicitari supportati

* Ricerca
* Visualizzazione
* Video
* Video online
* Nativa

Contatta il tuo account team di Adobi per conoscere gli ambienti di annunci supportati più di recente in ciascun canale.

## Aspetti da considerare prima dell’implementazione

* Il team di implementazione di Adobe Advertising configurerà l’integrazione.

* Questa integrazione non comporta costi aggiuntivi e le chiamate al server non generano costi aggiuntivi [!DNL Analytics] o Adobe Spese pubblicitarie.

* [!DNL Analytics for Advertising] è indipendente dal server di annunci: è possibile che si verifichi un view-through o un click-through da qualsiasi server di annunci e che gli ID appropriati vengano generati all’ingresso del sito.

* Solo i passaggi dell’integrazione [!DNL Analytics] eventi standard e personalizzati per Adobe Advertising per l’ottimizzazione delle offerte di media a pagamento e attività pubblicitarie successive. Non passa [!DNL Analytics] segmenti, metriche calcolate ed eVar per Adobe Advertising per l’ottimizzazione delle offerte.

* Adobe Advertising crea ID persistenti in [!DNL Analytics] in base all’ultimo annuncio pubblicitario fatto clic o visualizzato prima che l’utente entri nel sito, in base al [finestre di lookback click-through e view-through](#lookback-a4adc) configurato in Adobe Advertising. Se un visitatore del sito dispone di entrambi i tipi di interazioni di accesso al sito nel proprio profilo e il clic rientra nel periodo di lookback, l’ID di click-through del visitatore sovrascriverebbe l’ID di view-through per il reporting sul sito.

* [!DNL Analytics for Advertising] il tracciamento delle conversioni in Adobe Analytics utilizza un intervallo di lookback configurabile (60 giorni per impostazione predefinita). Adobe I rapporti sulla pubblicità riflettono le conversioni e il coinvolgimento del sito fino alla fine di questo intervallo di lookback.

* Sono supportati tutti i tipi di annunci. Tuttavia, non tutti gli ambienti di annunci sono supportati.

   Ad esempio, gli annunci TV connessi (CTV) non vengono tracciati perché non si verificano clic in CTV e non possono verificarsi conversioni sullo stesso dispositivo. Tuttavia, se l’annuncio viene visualizzato in un ambiente desktop, è possibile tenere traccia di alcuni dati di accesso al sito view-through.

* [!DNL Analytics] le conversioni sono attualmente tracciate e attribuite solo a un visitatore sullo stesso dispositivo.

* [!DNL Analytics for Advertising] non supporta le conversioni view-through in-app.

* Il tracciamento view-through non è supportato per gli inserzionisti che utilizzano un’implementazione lato server di [!DNL Analytics].

### ID supplementare

Una volta implementato il servizio Experience Cloud Identity per un sito, gli hit che contengono i dati di [!DNL Analytics] o Adobe Advertising contengono un ID supplementare.

Esempio: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

Per un’integrazione accurata dei dati, tutte le chiamate Adobe Advertising utilizzate da un [!DNL Analytics for Advertising] attività per consegnare contenuti o registrare la metrica di obiettivo deve avere un valore [!DNL Analytics] hit che condivide lo stesso ID supplementare.

Durante la risoluzione dei problemi in [!DNL Analytics], assicurati di confermare che l’ID supplementare sia presente per [!DNL Analytics] hit. In [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html), puoi visualizzare questo ID nella scheda Pubblicità Adobe come `sdid` parametro.

>[!NOTE]
>
> Questa implementazione funziona in modo simile al [!DNL Analytics for Target] integrazione.

>[!MORELIKETHIS]
>
>* [Panoramica di [!DNL Analytics for Advertising]](overview.md)
>* [Codice JavaScript per Analytics per Advertising](/help/integrations/analytics/javascript.md)

