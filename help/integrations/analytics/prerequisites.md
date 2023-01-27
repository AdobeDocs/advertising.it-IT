---
title: Prerequisiti e informazioni chiave per l’implementazione [!DNL Analytics for Advertising]
description: Prerequisiti e informazioni chiave per l’implementazione [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 7c477900-ebb0-4c0e-811a-ab8bc6069599
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 0%

---

# Prerequisiti e informazioni chiave per l’implementazione [!DNL Analytics for Advertising]

*Inserzionisti con DSP pubblicitari e[!DNL Advertising Search]*

Leggi le seguenti informazioni prima di integrare Adobe Advertising con Adobe Analytics.

## Requisiti per la segnalazione dei dati pubblicitari Adobi in [!DNL Analytics]

* Una delle seguenti opzioni:
   * Adobe Experience Platform Web SDK: `alloy.js`
   * Servizio Experience Cloud Identity: `visitorAPI.js` versione 2.0 o successiva
* Qualsiasi versione di Adobe Analytics (tra cui [!DNL Prime], [!DNL Premium]oppure [!DNL Ultimate])
* Adobe Analytics: `appMeasurement.js` versione 2.1 o successiva

>[!TIP]
>
>Per migliorare la fedeltà dei dati, utilizza la versione più recente di ciascuna libreria.

## Requisiti per la condivisione dei segmenti di Analytics con Adobe Advertising

* Servizio Experience Cloud Identity: `visitorAPI.js` versione 2.1 o successiva
* Adobe Analytics: `appMeasurement.js` versione 1.8 o successiva

## Obblighi di segnalazione [!DNL Analytics] Dati in Adobe Advertising

Fornisci al team di implementazione di Adobe Advertising i seguenti elementi:

* La [!DNL Analytics] ID suite di rapporti che verrà utilizzato per la generazione di rapporti su attività di media a pagamento e per l’alimentazione dell’attività del sito per l’ottimizzazione e il reporting in Adobe Advertising
* L&#39;ID organizzazione Experience Cloud della società (ID organizzazione).

Puoi trovare entrambi questi ID nel [Scheda Riepilogo del debugger Adobe Experience Cloud](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html).

![Schermata Riepilogo Experience Cloud Debugger](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Dati in Adobe Advertising {#lookback-a4adc}

Perché [!DNL Analytics] i dati vengono inviati ad Adobe Advertising per il reporting e l’ottimizzazione, i dati sono soggetti alle regole di attribuzione, compresi gli intervalli di lookback su impression e clic, configurati per l’inserzionista in Adobe Advertising.

![impostazioni dell’intervallo di lookback a livello di inserzionista in Adobe Advertising](/help/integrations/assets/a4adc-lookbacks.png)

* Adobe Intervallo di lookback su attribuzione pubblicitaria: Il numero di giorni successivi al primo clic in cui il clic può essere attribuito a una conversione. Per impostazione predefinita, questo valore è di 60 giorni; il massimo è 90 giorni
* Adobe intervallo di lookback dell’impression dell’attribuzione della pubblicità: Il numero di giorni dopo che si verifica un’impression pubblicitaria in cui l’impression può essere attribuita a una conversione. Per impostazione predefinita, questo valore è di 14 giorni; il massimo è 30 giorni

   >[!NOTE]
   >
   > L’intervallo di lookback su impression è specifico per Adobe Advertising, non per . [!DNL Analytics for Advertising], rapporti.

La [!DNL Analytics for Advertising] JavaScript utilizza queste impostazioni per determinare fino a che punto considerare valida una voce view-through o una voce click-through nel sito. Per ulteriori informazioni sulla determinazione delle visualizzazioni e dei click-through, consulta &quot;[ID pubblicitari di Adobe utilizzati da Analytics](ids.md).&quot;

## Adobe di dati pubblicitari in [!DNL Analytics]

[!DNL Analytics] imposta gli ID pubblicità di Adobe (AMO ID) all’interno dell’hit di Analytics, in base all’impostazione di persistenza eVar dell’inserzionista, che si applica sia ai click-through che alle visualizzazioni. L’impostazione di persistenza è configurata sul back-end Adobe Advertising e il tuo [!DNL Adobe] il team dell&#39;account può cambiarlo.

* [!DNL Analytics for Advertising] Scadenza eVar: 60 giorni per impostazione predefinita per gli ID AMO

>[!NOTE]
>
>Per segmentare i dati per un arco temporale diverso, puoi [impostare segmenti personalizzati](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) con diverse finestre di lookback in Analysis Workspace.

## Ambienti di annunci supportati

* Ricerca
* Visualizzazione
* Video
* Video online
* Nativo

Contatta il tuo [!DNL Adobe] team di account per gli ultimi ambienti di annunci supportati in ciascun canale.

## Aspetti da considerare prima dell’implementazione

* Il team di implementazione di Adobe Advertising configurerà l’integrazione.

* Non vengono fatturati costi aggiuntivi per questa integrazione, né le chiamate server generano ulteriori [!DNL Analytics] o le tariffe pubblicitarie Adobi.

* [!DNL Analytics for Advertising] è ad-server-agnostico: una visualizzazione o un click-through possono verificarsi da qualsiasi ad server e gli ID corretti vengono generati al momento dell&#39;ingresso del sito.

* L’integrazione passa solo [!DNL Analytics] eventi standard e personalizzati per Adobe Advertising per l&#39;ottimizzazione delle offerte dei successivi mezzi a pagamento e attività pubblicitarie. Non passa [!DNL Analytics] segmenti, metriche calcolate ed eVar ad Adobe Advertising per l’ottimizzazione delle offerte.

* Adobe Advertising crea ID persistenti all&#39;interno di [!DNL Analytics] in base all&#39;ultimo annuncio cliccato o visualizzato prima che l&#39;utente entri nel sito, in base alla [finestre di lookback su click e view-through](#lookback-a4adc) configurato in Adobe Advertising. Se un visitatore del sito deve avere entrambi i tipi di interazioni di accesso al sito all’interno del proprio profilo e il clic si trova entro il periodo di lookback, l’ID click-through del visitatore sovrascriverà l’ID view-through per la generazione di rapporti sul sito.

* [!DNL Analytics for Advertising] il tracciamento delle conversioni in Adobe Analytics utilizza un intervallo di lookback di tracciamento configurabile (60 giorni per impostazione predefinita). I rapporti sulla pubblicità di Adobe riflettono le conversioni e il coinvolgimento del sito attraverso la fine di questo intervallo di lookback di tracciamento.

* Sono supportati tutti i tipi di annunci. Tuttavia, non tutti gli ambienti di annunci sono supportati.

   Ad esempio, gli annunci TV collegati (CTV) non vengono tracciati perché non si verificano clic in CTV e non possono verificarsi conversioni sullo stesso dispositivo. Tuttavia, se l’annuncio viene visualizzato in un ambiente desktop, è possibile tenere traccia di alcuni dati di ingresso del sito view-through.

* [!DNL Analytics] le conversioni sono attualmente tracciate e attribuite solo a un visitatore sullo stesso dispositivo.

* [!DNL Analytics for Advertising] non supporta le conversioni in-app view-through.

* Il tracciamento view-through non è supportato per gli inserzionisti che utilizzano un’implementazione lato server di [!DNL Analytics].

### ID supplementare

Una volta implementato il servizio Experience Cloud Identity per un sito, gli hit che contengono i dati di [!DNL Analytics] o Adobe Advertising contiene un ID supplementare.

Esempio: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

Per un’integrazione accurata dei dati, tutte le chiamate pubblicitarie Adobe utilizzate da un [!DNL Analytics for Advertising] per fornire contenuto o registrare la metrica di obiettivo, è necessario che sia presente un [!DNL Analytics] hit che condivide lo stesso ID supplementare.

Quando si risolve il problema in [!DNL Analytics], assicurati di confermare che l’ID supplementare sia presente per [!DNL Analytics] hit. In [Debugger Adobe Experience Cloud](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html), puoi visualizzare questo ID nella scheda Pubblicità di Adobe come `sdid` parametro .

>[!NOTE]
>
> Questa implementazione funziona in modo simile al [!DNL Analytics for Target] integrazione.

>[!MORELIKETHIS]
>
>* [Panoramica [!DNL Analytics for Advertising]](overview.md)
>* [Codice JavaScript per Analytics per la pubblicità](/help/integrations/analytics/javascript.md)

