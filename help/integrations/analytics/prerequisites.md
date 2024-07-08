---
title: Prerequisiti e informazioni chiave per l'implementazione [!DNL Analytics for Advertising]
description: Prerequisiti e informazioni chiave per l'implementazione [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 7c477900-ebb0-4c0e-811a-ab8bc6069599
source-git-commit: 8481227a8ccb1f1e6e715e34e14732967110c168
workflow-type: tm+mt
source-wordcount: '802'
ht-degree: 0%

---

# Prerequisiti e informazioni chiave per l&#39;implementazione [!DNL Analytics for Advertising]

*Inserzionisti con DSP pubblicitari e[!DNL Advertising Search, Social, & Commerce]*

Prima di integrare Adobe Systems Advertising con Adobe Analytics, consulta le seguenti informazioni.

## Requisiti per la generazione di rapporti Adobe Systems dati pubblicitari in [!DNL Analytics]

* Una delle seguenti operazioni:
   * Adobe Experience Platform Web SDK: `alloy.js`
   * Experience Cloud Identity Service: `visitorAPI.js` versione 2.0 o successiva
* Qualsiasi versione di Adobe Analytics (inclusi [!DNL Prime], [!DNL Premium], o [!DNL Ultimate])
* Adobe Analytics: `appMeasurement.js` versione 2.1 o successiva
* (Pubblicità DSP clienti) Uno [snippet di DSP JavaScript](javascript.md) pubblicitario distribuito nelle tue pagine web per tenere traccia delle visite di visualizzazione.

>[!TIP]
>
>Per migliorare la fedeltà dei dati, utilizza la versione più recente di ogni libreria.

## Requisiti per la condivisione di segmenti Analytics con Adobe Systems Advertising

* Experience Cloud Identity Service: `visitorAPI.js` versione 2.1 o successiva
* Adobe Analytics: `appMeasurement.js` versione 1.8 o successiva

## Requisiti per la segnalazione [!DNL Analytics] dei dati in Adobe Systems Advertising

Fornisci all&#39;implementazione team di Adobe Systems Advertising quanto segue:

* ID suite [!DNL Analytics] di rapporti da utilizzare per generare rapporti sull&#39;attività paid media e per alimentare le attività del sito per l&#39;ottimizzazione e la creazione di report in Adobe Systems Advertising
* ID organizzazione (ID organizzazione) Experience Cloud della società.

È possibile trovare entrambi questi ID nella [scheda di riepilogo di Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html).

![Schermata Riepilogo debugger Experience Cloud](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Dati in Adobe Systems Advertising {#lookback-a4adc}

Poiché [!DNL Analytics] i dati vengono inviati a Adobe Systems Advertising per la creazione di rapporti e l&#39;ottimizzazione, i dati sono soggetti alle regole attribuzione, tra cui gli intervalli di lookback di impression e di click, configurate per l&#39;inserzionista in Adobe Systems Advertising.

![Impostazioni della finestra di lookback a livello di inserzionista in Adobe Systems Advertising](/help/integrations/assets/a4adc-lookbacks.png)

* Intervallo di lookback di attribuzione di Adobe Systems Advertising: il numero di giorni successivi al primo clic in cui il clic può essere attribuito a una conversione. Per impostazione predefinita, questo valore è di 60 giorni; il massimo è di 90 giorni
* Intervallo di lookback di attribuzione impression di Adobe Systems Advertising: il numero di giorni successivi a un ad impression in cui il impression può essere attribuito a una conversione. Per impostazione predefinita, questo valore è di 14 giorni; il massimo è di 30 giorni

  >[!NOTE]
  >
  > L&#39;intervallo di lookback di impression è specifico per Adobe Systems Pubblicità, non [!DNL Analytics for Advertising]per i rapporti.

Il [!DNL Analytics for Advertising] JavaScript utilizza queste impostazioni per determinare fino a che punto considerare valida una voce di view-through o una voce click-through al sito. Per ulteriori informazioni su come vengono determinate le visualizzazioni e i click-through, consulta &quot;[Adobe Systems ID pubblicitari utilizzati dai Analytics](ids.md)&quot;.

## Adobe Systems dati pubblicitari in [!DNL Analytics]

[!DNL Analytics] imposta Adobe Systems ID pubblicità (AMO ID) all&#39;interno dell&#39;hit Analytics, in base all&#39;impostazione di persistenza dell&#39;inserzionista [!DNL eVar] , che si applica sia ai click-through che alle visualizzazioni. L&#39;impostazione di persistenza è configurata nel back-end di Adobe Systems Advertising e il team dell&#39;account Adobe Systems può modificarla.

* [!DNL Analytics for Advertising][!DNL eVar] scadenza: 60 giorni per impostazione predefinita per gli ID AMO

>[!NOTE]
>
>Per segmentare i dati per un arco temporale diverso, puoi [impostare segmenti](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) personalizzati con diverse finestre di lookback all&#39;interno di Analysis Workspace.

## Ambienti pubblicitari supportati

* Ricerca
* Esporre
* Video
* Online Video
* Connessione TV
* Nativo

Contatta il team dell&#39;account Adobe Systems per gli ambienti annuncio supportati più recenti in ciascun canale.

## Aspetti da considerare prima dell&#39;implementazione

* Il implementazione team di Adobe Systems Advertising imposta l&#39;integrazione.

* Non vengono addebitati costi aggiuntivi per questa integrazione, né le chiamate al server comportano costi pubblicitari aggiuntivi [!DNL Analytics] o Adobe Systems.

* [!DNL Analytics for Advertising] è indipendente dal ad server: da qualsiasi ad server può verificarsi un view-through o un click-through e gli ID corretti vengono generati al momento dell&#39;ingresso nel sito.

* L&#39;integrazione passa solo [!DNL Analytics] gli eventi standard e personalizzati a Adobe Systems Advertising per offerta ottimizzazione delle successive attività paid media e pubblicitarie. Non passa [!DNL Analytics] segmenti, metriche calcolate e [!DNL eVars] a Adobe Systems Advertising per ottimizzare offerta.

* Adobe Systems Advertising crea ID permanenti all&#39;interno [!DNL Analytics] in base all&#39;ultimo annuncio pubblicitario cliccato o visualizzato prima che l&#39;utente entri nel sito, in base alle [finestre](#lookback-a4adc) di lookback di clic e visualizzazione configurate in Adobe Systems Advertising. Se un visitatore del sito ha entrambi i tipi di interazioni di immissione sul sito all&#39;interno del suo profilo e il clic è all&#39;interno del periodo di lookback, l&#39;ID click-through del visitatore sostituisce l&#39;ID di visualizzazione per la creazione di rapporti sul sito.

* [!DNL Analytics for Advertising] Il monitoraggio delle conversioni in Adobe Analytics utilizza una finestra di lookback di monitoraggio configurabile (60 giorni per impostazione predefinita). Adobe Systems rapporti pubblicitari riflettono le conversioni e il coinvolgimento del sito fino alla fine di questa finestra di lookback di monitoraggio.

* Sono supportati tutti i tipi di annuncio. Tuttavia, non tutti gli ambienti annuncio sono supportati.

* [!DNL Analytics] Le conversioni sono attualmente tracciate e attribuite solo a un visitatore sullo stesso dispositivo.

* [!DNL Analytics for Advertising] non supporta le conversioni view-through in-app.

* Il monitoraggio Visualizza-through non è supportato per gli inserzionisti che utilizzano un implementazione di inoltro lato server di [!DNL Analytics].

### ID supplementare

Una volta implementato il servizio Experience Cloud Identity per un sito, i risultati che contengono dati provenienti da [!DNL Analytics] o Adobe Systems Advertising includono un ID supplementare.

Esempio: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

Per un&#39;integrazione accurata dei dati, tutte le chiamate pubblicitarie Adobe Systems utilizzate da un&#39;attività [!DNL Analytics for Advertising] per inviare contenuto o registrare la metrica obiettivo devono avere un hit corrispondente [!DNL Analytics] che condivida lo stesso ID supplementare.

Durante la risoluzione dei problemi in [!DNL Analytics], assicurati di confermare che l&#39;ID supplementare sia presente per [!DNL Analytics] gli hit. In Adobe Experience Cloud [Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html) è possibile visualizzare questo ID nel scheda di Adobe Systems Advertising come `sdid` parametro.

>[!NOTE]
>
> Questo implementazione funziona in modo simile all&#39;integrazione [!DNL Analytics for Target] .

>[!MORELIKETHIS]
>
>* [Panoramica di [!DNL Analytics for Advertising]](overview.md)
>* [JavaScript Code for Analytics for Advertising](/help/integrations/analytics/javascript.md)
