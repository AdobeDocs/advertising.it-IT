---
title: Prerequisiti e informazioni chiave per l'implementazione  [!DNL Analytics for Advertising]
description: Prerequisiti e informazioni chiave per l'implementazione  [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 7c477900-ebb0-4c0e-811a-ab8bc6069599
source-git-commit: 1559c2cb83e32d90f4b2fe959d07c4e588d9becf
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 0%

---

# Prerequisiti e informazioni chiave per l&#39;implementazione di [!DNL Analytics for Advertising]

*Inserzionisti con Advertising DSP e[!DNL Advertising Search, Social, & Commerce]*

Leggi le seguenti informazioni prima di integrare Adobe Advertising con Adobe Analytics.

## Requisiti per i dati dell&#39;Adobe Advertising di reporting in [!DNL Analytics]

* una delle seguenti situazioni:
   * Adobe Experience Platform Web SDK: `alloy.js`
   * Servizio Experience Cloud Identity: `visitorAPI.js` versione 2.0 o successiva
* Qualsiasi versione di Adobe Analytics (inclusi [!DNL Prime], [!DNL Premium] o [!DNL Ultimate])
* Adobe Analytics: `appMeasurement.js` versione 2.1 o successiva
* (Clienti Advertising DSP) Un [frammento di codice JavaScript di Advertising DSP](javascript.md) distribuito nelle pagine Web per tenere traccia delle visite view-through.

>[!TIP]
>
>Per migliorare la fedeltà dei dati, utilizza la versione più recente di ciascuna libreria.

## Requisiti per la condivisione dei segmenti di Analytics con Adobe Advertising

* Servizio Experience Cloud Identity: `visitorAPI.js` versione 2.1 o successiva
* Adobe Analytics: `appMeasurement.js` versione 1.8 o successiva

## Requisiti per il reporting dei dati [!DNL Analytics] in Adobe Advertising

Fornisci al team di implementazione di Adobe Advertising quanto segue:

* ID suite di rapporti [!DNL Analytics] da utilizzare per la generazione di rapporti sulle attività a pagamento e per il feed delle attività del sito per l&#39;ottimizzazione e il reporting in Adobe Advertising
* L’ID organizzazione Experience Cloud (ID organizzazione) della società.

Entrambi gli ID sono disponibili nella scheda [Riepilogo di Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html).

![Schermata Riepilogo Experienci Cloud Debugger](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] dati in Adobe Advertising {#lookback-a4adc}

Poiché i dati di [!DNL Analytics] vengono inviati ad Adobe Advertising per il reporting e l&#39;ottimizzazione, i dati sono soggetti alle regole di attribuzione, inclusi gli intervalli di lookback su impression e clic, configurati per l&#39;inserzionista in Adobe Advertising.

![impostazioni dell&#39;intervallo di lookback a livello di inserzionista in Adobe Advertising](/help/integrations/assets/a4adc-lookbacks.png)

* Adobe Advertising di intervallo di lookback su clic di attribuzione: numero di giorni dopo il primo clic in cui il clic può essere attribuito a una conversione. Per impostazione predefinita, questo valore è 60 giorni; il massimo è 90 giorni
* Intervallo di lookback delle impression di attribuzione di Adobe Advertising: numero di giorni dopo i quali si verifica un’impression pubblicitaria, in cui l’impression può essere attribuita a una conversione. Per impostazione predefinita, questo valore è 14 giorni; il massimo è 30 giorni

  >[!NOTE]
  >
  > L&#39;intervallo di lookback delle impression è specifico di Adobe Advertising, non di [!DNL Analytics for Advertising], nel reporting.

Il JavaScript [!DNL Analytics for Advertising] utilizza queste impostazioni per determinare quanto indietro nel tempo considera valida una voce view-through o una voce click-through nel sito. Per ulteriori informazioni sulle modalità di determinazione delle visite e dei click-through, vedere &quot;[ID Adobi Advertising utilizzati da Analytics](ids.md).&quot;

## Adobe Advertising di dati in [!DNL Analytics]

[!DNL Analytics] imposta gli ID Adobe Advertising (AMO ID) nell&#39;hit di Analytics, in base all&#39;impostazione di persistenza [!DNL eVar] dell&#39;inserzionista, che si applica sia ai click-through che alle view-through. L’impostazione di persistenza è configurata sul back-end Adobe Advertising e il team dell’account Adobe può modificarla.

* Scadenza [!DNL Analytics for Advertising] [!DNL eVar]: 60 giorni per impostazione predefinita per gli AMO ID

>[!NOTE]
>
>Per segmentare i dati per un intervallo di tempo diverso, puoi [impostare segmenti personalizzati](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) con diversi intervalli di lookback in Analysis Workspace.

## Ambienti pubblicitari supportati

* Ricerca
* Visualizzazione
* Video
* Video online
* TV collegata
* Nativa

Contatta il tuo account team di Adobi per conoscere gli ambienti di annunci supportati più di recente in ciascun canale.

## Aspetti da considerare prima dell’implementazione

* Il team di implementazione di Adobe Advertising configura l’integrazione.

* Non vengono fatturati costi aggiuntivi per questa integrazione, né le chiamate al server determinano [!DNL Analytics] o Adobi Advertising aggiuntivi.

* [!DNL Analytics for Advertising] è indipendente dal server di annunci: è possibile che si verifichi un click-through o una visualizzazione da qualsiasi server di annunci e che gli ID appropriati vengano generati all&#39;ingresso del sito.

* L&#39;integrazione trasmette solo [!DNL Analytics] eventi standard e personalizzati a Adobe Advertising per l&#39;ottimizzazione delle offerte per le successive attività pubblicitarie e per i media a pagamento. Non trasmette [!DNL Analytics] segmenti, metriche calcolate e [!DNL eVars] all&#39;Adobe Advertising per l&#39;ottimizzazione delle offerte.

* In Adobe Advertising vengono creati ID persistenti all&#39;interno di [!DNL Analytics] in base all&#39;ultimo annuncio su cui è stato fatto clic o visualizzato prima che l&#39;utente entri nel sito, in base agli [intervalli di lookback di click e view-through](#lookback-a4adc) configurati in Adobe Advertising. Se nel profilo di un visitatore del sito sono presenti entrambi i tipi di interazioni di accesso al sito e il clic rientra nel periodo di lookback, l’ID di click-through del visitatore prevale sull’ID di view-through per i rapporti sul sito.

* Il monitoraggio delle conversioni [!DNL Analytics for Advertising] in Adobe Analytics utilizza un intervallo di lookback configurabile (60 giorni per impostazione predefinita). I rapporti di Adobe Advertising riflettono le conversioni e il coinvolgimento del sito fino alla fine di questo intervallo di lookback di tracciamento.

* Sono supportati tutti i tipi di annunci. <!--Clarify what this might include. It used to include CTV, but not anymore: However, not all ad environments are supported. -->

* [!DNL Analytics] conversioni sono attualmente tracciate e attribuite solo a un visitatore sullo stesso dispositivo.

* [!DNL Analytics for Advertising] non supporta le conversioni view-through in-app.

* Il tracciamento view-through non è supportato per gli inserzionisti che utilizzano un&#39;implementazione lato server di [!DNL Analytics].

### ID supplementare

Una volta implementato il servizio Experience Cloud Identity per un sito, gli hit che contengono i dati di [!DNL Analytics] o Adobe Advertising contengono un ID supplementare.

Esempio: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

Per un&#39;integrazione accurata dei dati, tutte le chiamate di Adobe Advertising utilizzate da un&#39;attività [!DNL Analytics for Advertising] per inviare contenuto o registrare la metrica di obiettivo devono avere un hit [!DNL Analytics] corrispondente che condivida lo stesso ID supplementare.

Durante la risoluzione dei problemi in [!DNL Analytics], assicurati di confermare che l&#39;ID supplementare sia presente per [!DNL Analytics] hit. Nel [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html), puoi visualizzare questo ID nella scheda dell&#39;Adobe Advertising come parametro `sdid`.

>[!NOTE]
>
> Questa implementazione funziona in modo simile all&#39;integrazione [!DNL Analytics for Target].

>[!MORELIKETHIS]
>
>* [Panoramica di [!DNL Analytics for Advertising]](overview.md)
>* [Codice JavaScript per Advertising](/help/integrations/analytics/javascript.md)
