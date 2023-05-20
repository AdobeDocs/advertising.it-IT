---
title: Domande frequenti su [!UICONTROL Household] Report
description: Ulteriori informazioni su [!UICONTROL Household] rapporto, incluse le differenze rispetto ad altri rapporti e la risoluzione dei problemi.
source-git-commit: 95f81dafbe13f40487bad47f7dd41a6c80c589ee
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 0%

---

# Domande frequenti su [!UICONTROL Household] Report

## Come sono [!UICONTROL Household] rapporti su portata e frequenza diversi da altri rapporti personalizzati?

Il [!UICONTROL Household] il rapporto misura portata, impression e frequenza tra varie dimensioni a livello di famiglia in base all’indirizzo IP. Gli altri rapporti personalizzati vengono generati a livello di dispositivo o cookie.

Ad esempio, anche se un’impression viene trasmessa a tre dispositivi all’interno di una famiglia, la metrica Raggiunto in famiglia univoca è pari a uno.

### Dimension supportati

Il [!UICONTROL Household] Il report supporta [dimensioni seguenti](/help/dsp/reports/report-columns.md): &quot;[!UICONTROL Campaign],&quot; &quot;[!UICONTROL Package],&quot; &quot;[!UICONTROL Placement],&quot; &quot;[!UICONTROL Site/Apps]&quot; (che non fornisce l’accesso alle metriche di sovrapposizione), &quot;[!UICONTROL Media Type],&quot; &quot;[!UICONTROL Feed Type],&quot; &quot;[!UICONTROL Device],&quot; &quot;[!UICONTROL Publisher],&quot; &quot;[!UICONTROL Audience],&quot; &quot;[!UICONTROL Creative Length],&quot; e posizionamento creato dall’utente &quot;[!UICONTROL Tags].&quot; |

### Metriche supportate

Il [metriche disponibili](/help/dsp/reports/report-columns.md) include:

* Metriche di sovrapposizione: [!UICONTROL Frequency Overlap], [!UICONTROL Measurable Impressions (Overlap)], e [!UICONTROL Unique Household (Overlap)].

   Le metriche di sovrapposizione sono i valori che si verificano solo per la dimensione o la combinazione di dimensioni segnalata e non per altre dimensioni. <!-- For example, it might show the ?? -->

* Metriche non di sovrapposizione: [!UICONTROL Frequency], [!UICONTROL Incremental Household Reached], [!UICONTROL % Incremental Household Reached], [!UICONTROL Impressions], [!UICONTROL Measurable Impressions], e [!UICONTROL Unique Household Reached]

Le metriche di conversione e gli obiettivi personalizzati non sono supportati.

## Qual è la differenza tra le metriche di sovrapposizione e non di sovrapposizione?

La figura seguente mostra tre metriche (Famiglia univoca raggiunta, Famiglia incrementale raggiunta e Famiglia incrementale (Sovrapposizione)) per tre campagne (A, B e C).

![Illustrazione delle metriche di sovrapposizione delle famiglie](/help/dsp/assets/household-overlap-metrics-illustration.png "Illustrazione delle metriche di sovrapposizione delle famiglie")

* Famiglia univoca raggiunta (totale) fornisce la famiglia univoca raggiunta da ciascuna campagna o l’area totale di ciascun cerchio. Nella figura, Famiglia univoca raggiunta da A = Famiglia incrementale raggiunta da A + (A+B) + (A+C) + (A+B+C)

* La famiglia incrementale raggiunta è la famiglia unica raggiunta solo da una campagna. Nella figura, la famiglia incrementale raggiunta da A, B, C è la famiglia incrementale raggiunta rispettivamente da A, B, C.

* Famiglia incrementale (sovrapposizione) è la famiglia univoca raggiunta dalla campagna o dalla combinazione di campagne. Nella figura, la famiglia incrementale raggiunta da A, C è A+C.

## Flusso di lavoro

Seguire i passaggi normali per [creare un rapporto personalizzato](report-create.md).

Il [!UICONTROL Household] il rapporto può includere una sola dimensione. Può anche includere a) metriche di sovrapposizione per qualsiasi dimensione ad eccezione di Sito/App o b) metriche non di sovrapposizione, ma non entrambe.

## Quali sono alcuni limiti della [!UICONTROL Household] rapporto? 

Report con intersezioni di output di metriche di sovrapposizione fino a tre valori. Ad esempio, utilizzando la metrica [!UICONTROL Unique Household (Overlap)] per 10 posizionamenti, si possono vedere le famiglie uniche raggiunte dai posizionamenti individuali, le famiglie comuni raggiunte da una combinazione di due posizionamenti qualsiasi e le famiglie comuni raggiunte da combinazioni di tre posizionamenti qualsiasi. Non si possono vedere famiglie comuni raggiunte da quattro o più posizionamenti.

Per dimensioni diverse da campagna, pacchetto o posizionamento, il rapporto supporta fino a 10 valori in ogni dimensione. Ad esempio, per generare un [!UICONTROL Unique Household Reached] rapporto per [!UICONTROL Audience] il numero di tipi di pubblico univoci deve essere inferiore o uguale a 10. Se includi più di 10 tipi di pubblico univoci, viene generato un rapporto vuoto.

## Perché i valori di frequenza e portata univoci sono diversi tra i miei [!UICONTROL Custom] rapporti e [!UICONTROL Household] rapporto?

Queste metriche in [!UICONTROL Household] I rapporti di vengono calcolati utilizzando il conteggio effettivo degli indirizzi IP, mentre le metriche in [!UICONTROL Custom] nel rapporto vengono utilizzati numeri stimati calcolati utilizzando modelli. Tuttavia, la discrepanza dovrebbe essere inferiore al 10%.

## Come si configura il rapporto per [!UICONTROL Placement Tags] dimensione?

Per creare i tag per il posizionamento: [apri le impostazioni di posizionamento](/help/dsp/campaign-management/placements/placement-edit.md) e immettere i valori nel [Campo Tag di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md).
 
Quando un posizionamento include più tag, il rapporto considera l’intera stringa come un unico tag. Il rapporto include una riga per ogni stringa univoca.

## [!UICONTROL Household] Rapporto e dati da [!DNL Advanced Measurement Services]

Per la generazione avanzata di rapporti sulla portata e sulla frequenza basati sulle famiglie, il [[!DNL Strategic Advertising Consulting] team](/help/dsp/introduction/advanced-measurement-services.md) può fornire rapporti altamente personalizzabili insieme a consigli strategici olistici. Per ulteriori informazioni su [!DNL Advanced Measurement Services], contatta il team del tuo account Adobe.

### Se utilizzo già [!DNL Advanced Measurement Services], perché utilizzare il [!UICONTROL Household] rapporto?

Il [!UICONTROL Household] il rapporto consente ai clienti di richiamare autonomamente in tempo reale le metriche di portata e frequenza a livello di famiglia.

### Posso utilizzare entrambi i [!UICONTROL Household] rapporto e [!DNL Advanced Measurement Services]? 

Il caso d’uso ideale consiste nell’utilizzare sia [!UICONTROL Household] rapporto e [!DNL Advanced Measurement Services] servizi di reporting e consulenza. Considera [!UICONTROL Household] generare rapporti come transazionali, intesi a informare le ottimizzazioni quotidiane, e [!DNL Advanced Measurement Services] in quanto più strategico, destinato a informare apprendimenti e soluzioni olistiche legati a obiettivi aziendali generali.

>[!MORELIKETHIS]
>
>* [Informazioni sui report personalizzati](/help/dsp/reports/report-about.md)
>* [Creare un rapporto personalizzato](/help/dsp/reports/report-create.md)
>* [Modificare un rapporto personalizzato](/help/dsp/reports/report-edit.md)
>* [Impostazioni report personalizzati](/help/dsp/reports/report-settings.md)
>* [Colonne report disponibili](/help/dsp/reports/report-columns.md)

