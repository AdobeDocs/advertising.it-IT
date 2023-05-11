---
title: Domande frequenti sulle [!UICONTROL Household] Rapporto
description: Ulteriori informazioni sulle [!UICONTROL Household] , compreso il modo in cui si differenzia dagli altri rapporti e la risoluzione dei problemi.
source-git-commit: 95f81dafbe13f40487bad47f7dd41a6c80c589ee
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 0%

---

# Domande frequenti sulle [!UICONTROL Household] Rapporto

## Come [!UICONTROL Household] rapporti di portata e frequenza diversi da altri rapporti personalizzati?

La [!UICONTROL Household] le misure di report raggiungono, impression e frequenza tra varie dimensioni a livello di famiglia in base all&#39;indirizzo IP. Gli altri rapporti personalizzati vengono generati a livello di dispositivo o cookie.

Ad esempio, anche se viene trasmessa un’impression a tre dispositivi all’interno di una famiglia, la metrica Raggiunto unico per famiglia è una.

### Dimension supportati

La [!UICONTROL Household] il rapporto supporta [dimensioni seguenti](/help/dsp/reports/report-columns.md): &quot;[!UICONTROL Campaign]&quot;[!UICONTROL Package]&quot;[!UICONTROL Placement]&quot;[!UICONTROL Site/Apps]&quot; (che non fornisce accesso alle metriche di sovrapposizione), &quot;[!UICONTROL Media Type]&quot;[!UICONTROL Feed Type]&quot;[!UICONTROL Device]&quot;[!UICONTROL Publisher]&quot;[!UICONTROL Audience]&quot;[!UICONTROL Creative Length],&quot; e il posizionamento creato dall&#39;utente &quot;[!UICONTROL Tags].&quot; |

### Metriche supportate

La [metriche disponibili](/help/dsp/reports/report-columns.md) include:

* Metriche di sovrapposizione: [!UICONTROL Frequency Overlap], [!UICONTROL Measurable Impressions (Overlap)]e [!UICONTROL Unique Household (Overlap)].

   Le metriche di sovrapposizione sono i valori che si verificano solo per la dimensione o la combinazione di dimensioni segnalate e non per altre dimensioni. <!-- For example, it might show the ?? -->

* Metriche non di sovrapposizione: [!UICONTROL Frequency], [!UICONTROL Incremental Household Reached], [!UICONTROL % Incremental Household Reached], [!UICONTROL Impressions], [!UICONTROL Measurable Impressions]e [!UICONTROL Unique Household Reached]

Le metriche di conversione e gli obiettivi personalizzati non sono supportati.

## Qual è la differenza tra le metriche di sovrapposizione e non di sovrapposizione?

La figura seguente mostra tre metriche (Univoco Famiglia raggiunta, Famiglia incrementale raggiunta e Famiglia incrementale (sovrapposizione)) per tre campagne (A, B e C).

![Illustrazione delle metriche di sovrapposizione delle famiglie](/help/dsp/assets/household-overlap-metrics-illustration.png "Illustrazione delle metriche di sovrapposizione delle famiglie")

* La pagina Univoco Raggiunto (Totale) fornisce la famiglia Univoca raggiunta da ciascuna campagna o l’area totale di ciascuno dei cerchi. Nella figura, Famiglia unica raggiunta da A = Famiglia incrementale raggiunta da A + (A+B) + (A+C) +(A+B+C)

* La famiglia incrementale raggiunta è la famiglia univoca raggiunta solo da una campagna. Nella figura, la famiglia incrementale raggiunta da A, B, C è la famiglia incrementale raggiunta rispettivamente da A, B e C.

* La famiglia incrementale (sovrapposizione) è la famiglia univoca raggiunta dalla campagna o dalla combinazione di campagne. Nella figura, la famiglia incrementale raggiunta da A, C è A+C.

## Flusso di lavoro

Segui i passaggi normali per [creare un rapporto personalizzato](report-create.md).

La [!UICONTROL Household] il rapporto può includere una sola dimensione. Può anche includere a) metriche di sovrapposizione per qualsiasi dimensione ad eccezione di Sito/App o b) metriche di non sovrapposizione, ma non entrambe.

## Quali sono alcune limitazioni del [!UICONTROL Household] rapporto? 

I rapporti con metriche di sovrapposizione presentano intersezioni di output fino a tre valori. Ad esempio, se utilizzi la metrica [!UICONTROL Unique Household (Overlap)] per 10 collocamenti, si possono vedere le famiglie uniche raggiunte dai singoli collocamenti, le famiglie comuni raggiunte da una combinazione di due posizionamenti, e le famiglie comuni raggiunte da combinazioni di tre posizionamenti. Non si possono vedere famiglie comuni raggiunte da quattro o più posizionamenti.

Per dimensioni diverse da campagna, pacchetto o posizionamento, il rapporto supporta fino a 10 valori in ogni dimensione. Ad esempio, per generare un [!UICONTROL Unique Household Reached] rapporto per [!UICONTROL Audience] Il numero di tipi di pubblico univoci deve essere minore o uguale a 10. Se includi più di 10 tipi di pubblico univoci, viene generato un rapporto vuoto.

## Perché la frequenza e i valori di portata univoci sono diversi tra i [!UICONTROL Custom] le relazioni e [!UICONTROL Household] rapporto?

Queste metriche in [!UICONTROL Household] i rapporti vengono calcolati utilizzando il conteggio effettivo degli indirizzi IP, mentre le metriche nel [!UICONTROL Custom] i rapporti utilizzano numeri stimati calcolati utilizzando i modelli. Tuttavia, la discrepanza dovrebbe essere inferiore al 10%.

## Come si configura il rapporto per il [!UICONTROL Placement Tags] dimensione?

Per creare tag per il posizionamento, [apri le impostazioni di posizionamento](/help/dsp/campaign-management/placements/placement-edit.md) e immetti i valori nella [Campo Tag posizionamento](/help/dsp/campaign-management/placements/placement-settings.md).
 
Quando un posizionamento include più tag, il rapporto considera l’intera stringa come un tag. Il rapporto include una riga per ogni stringa univoca.

## [!UICONTROL Household] Rapporto e dati da [!DNL Advanced Measurement Services]

Per la generazione avanzata di rapporti sulla portata e la frequenza basate sulle famiglie, la [[!DNL Strategic Advertising Consulting] team](/help/dsp/introduction/advanced-measurement-services.md) può fornire rapporti altamente personalizzabili insieme a raccomandazioni strategiche olistiche. Per ulteriori informazioni [!DNL Advanced Measurement Services], contatta il team dell’account Adobe.

### Se sto già utilizzando [!DNL Advanced Measurement Services], perché dovrei usare [!UICONTROL Household] rapporto?

La [!UICONTROL Household] consente ai clienti di richiamare autonomamente in tempo reale le metriche di portata e frequenza a livello di famiglia.

### Posso utilizzare entrambi i [!UICONTROL Household] e [!DNL Advanced Measurement Services]? 

Il caso d&#39;uso ideale è quello di utilizzare entrambi i [!UICONTROL Household] la relazione e [!DNL Advanced Measurement Services] servizi di reporting e consulenza in comune. Considera la [!UICONTROL Household] rapporti come transazionali, intesi a informare le ottimizzazioni quotidiane, e [!DNL Advanced Measurement Services] come più strategico, inteso per informare gli insegnamenti olistici e le acquisizioni legate agli obiettivi aziendali generali.

>[!MORELIKETHIS]
>
>* [Informazioni sui report personalizzati](/help/dsp/reports/report-about.md)
>* [Creare un rapporto personalizzato](/help/dsp/reports/report-create.md)
>* [Modificare un rapporto personalizzato](/help/dsp/reports/report-edit.md)
>* [Impostazioni report personalizzate](/help/dsp/reports/report-settings.md)
>* [Colonne dei rapporti disponibili](/help/dsp/reports/report-columns.md)

