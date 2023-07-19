---
title: Domande frequenti sui rapporti sulle famiglie
description: Ulteriori informazioni sui dati dei rapporti, tra cui come [!UICONTROL Household] i rapporti sono diversi dagli altri rapporti e dalla risoluzione dei problemi.
exl-id: aaaf6f6d-b133-4cda-8fc6-bd686b3b1ebb
source-git-commit: 05f7d9c7a120828bda46d4f79796dfb419cca242
workflow-type: tm+mt
source-wordcount: '907'
ht-degree: 0%

---

# Domande frequenti sui rapporti sulle famiglie

## Il [!UICONTROL Household Reach & Frequency] Report

### Come sono [!UICONTROL Household Reach & Frequency] rapporti diversi da altri rapporti personalizzati?

Il [!UICONTROL Household Reach & Frequency] il rapporto misura portata, impression e frequenza tra varie dimensioni a livello di famiglia in base all’indirizzo IP. Gli altri rapporti personalizzati vengono generati a livello di dispositivo o cookie.

Ad esempio, anche se un’impression viene trasmessa a tre dispositivi all’interno di una famiglia, la metrica Raggiunto in famiglia univoca è pari a uno.

#### Dimension supportati

Il [!UICONTROL Household Reach & Frequency] Il report supporta [dimensioni seguenti](/help/dsp/reports/report-columns.md): &quot;[!UICONTROL Campaign],&quot; &quot;[!UICONTROL Package],&quot; &quot;[!UICONTROL Placement],&quot; &quot;[!UICONTROL Site/Apps]&quot; (che non fornisce l’accesso alle metriche di sovrapposizione), &quot;[!UICONTROL Media Type],&quot; &quot;[!UICONTROL Feed Type],&quot; &quot;[!UICONTROL Device],&quot; &quot;[!UICONTROL Publisher],&quot; &quot;[!UICONTROL Audience],&quot; &quot;[!UICONTROL Creative Length],&quot; e posizionamento creato dall’utente &quot;[!UICONTROL Tags].&quot; |

#### Metriche supportate

Il [metriche disponibili](/help/dsp/reports/report-columns.md) include:

* Metriche di sovrapposizione: [!UICONTROL Frequency Overlap], [!UICONTROL Measurable Impressions (Overlap)], e [!UICONTROL Unique Household (Overlap)].

  Le metriche di sovrapposizione sono i valori che si verificano solo per la dimensione o la combinazione di dimensioni segnalata e non per altre dimensioni. <!-- For example, it might show the ?? -->

* Metriche non di sovrapposizione: [!UICONTROL Frequency], [!UICONTROL Incremental Household Reached], [!UICONTROL % Incremental Household Reached], [!UICONTROL Impressions], [!UICONTROL Measurable Impressions], e [!UICONTROL Unique Household Reached]

Le metriche di conversione e gli obiettivi personalizzati non sono supportati.

### Qual è la differenza tra le metriche di sovrapposizione e non di sovrapposizione?

La figura seguente mostra tre metriche (Famiglia univoca raggiunta, Famiglia incrementale raggiunta e Famiglia incrementale (Sovrapposizione)) per tre campagne (A, B e C).

![Illustrazione delle metriche di sovrapposizione delle famiglie](/help/dsp/assets/household-overlap-metrics-illustration.png "Illustrazione delle metriche di sovrapposizione delle famiglie")

* Famiglia univoca raggiunta (totale) fornisce la famiglia univoca raggiunta da ciascuna campagna o l’area totale di ciascun cerchio. Nella figura, Famiglia univoca raggiunta da A = Famiglia incrementale raggiunta da A + (A+B) + (A+C) + (A+B+C)

* La famiglia incrementale raggiunta è la famiglia unica raggiunta solo da una campagna. Nella figura, la famiglia incrementale raggiunta da A, B, C è la famiglia incrementale raggiunta rispettivamente da A, B, C.

* Famiglia incrementale (sovrapposizione) è la famiglia univoca raggiunta dalla campagna o dalla combinazione di campagne. Nella figura, la famiglia incrementale raggiunta da A, C è A+C.

### Flusso di lavoro

Seguire i passaggi normali per [creare un rapporto personalizzato](report-create.md).

Il [!UICONTROL Household Reach & Frequency] il rapporto può includere una sola dimensione. Può anche includere a) metriche di sovrapposizione per qualsiasi dimensione ad eccezione di Sito/App o b) metriche non di sovrapposizione, ma non entrambe.

### Quali sono alcuni limiti della [!UICONTROL Household Reach & Frequency] rapporto?

Report con intersezioni di output di metriche di sovrapposizione fino a tre valori. Ad esempio, utilizzando la metrica [!UICONTROL Unique Household (Overlap)] per 10 posizionamenti, si possono vedere le famiglie uniche raggiunte dai posizionamenti individuali, le famiglie comuni raggiunte da una combinazione di due posizionamenti qualsiasi e le famiglie comuni raggiunte da combinazioni di tre posizionamenti qualsiasi. Non si possono vedere famiglie comuni raggiunte da quattro o più posizionamenti.

Per dimensioni diverse da campagna, pacchetto o posizionamento, il rapporto supporta fino a 10 valori in ogni dimensione. Ad esempio, per generare un [!UICONTROL Unique Household Reached] rapporto per [!UICONTROL Audience] il numero di tipi di pubblico univoci deve essere inferiore o uguale a 10. Se includi più di 10 tipi di pubblico univoci, viene generato un rapporto vuoto.

### Perché i valori di frequenza e portata univoci sono diversi tra i miei [!UICONTROL Custom] rapporti e [!UICONTROL Household Reach & Frequency] rapporto?

Queste metriche in [!UICONTROL Household] I rapporti di vengono calcolati utilizzando il conteggio effettivo degli indirizzi IP, mentre le metriche in [!UICONTROL Custom] nel rapporto vengono utilizzati numeri stimati calcolati utilizzando modelli. Tuttavia, la discrepanza dovrebbe essere inferiore al 10%.

### Come si configura il rapporto per [!UICONTROL Placement Tags] dimensione?

Per creare i tag per il posizionamento: [apri le impostazioni di posizionamento](/help/dsp/campaign-management/placements/placement-edit.md) e immettere i valori nel [Campo Tag di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md).

Quando un posizionamento include più tag, il rapporto considera l’intera stringa come un unico tag. Il rapporto include una riga per ogni stringa univoca.

## Il [!UICONTROL Household Conversions] Report

### Quali sono i tipi di metodi di attribuzione supportati in [!UICONTROL Household Conversions] rapporto?

Sono supportati due tipi di metodi di attribuzione:

* Univoco: conta quante volte un valore di dimensione (ad esempio un dispositivo o un posizionamento) si trovava sul percorso di conversione.

* MTA (Multi-Touch Attribution): distribuisce il credito di ogni conversione in base alla frequenza di occorrenza del valore di dimensione (ad esempio un dispositivo o un posizionamento) sul percorso di conversione. Ad esempio, se il totale delle impression prima della conversione era 10, con 8 su CTV e 2 su Mobile, l&#39;80% del credito (0,8) viene assegnato agli schermi CTV e 0,2 a Mobile.

### In che modo i rapporti sulle conversioni domestiche differiscono dai rapporti view-through CTV in Adobe Analytics?

Dati view-through CTV in [!DNL Analytics] è alimentato [!DNL Analytics] e i dati di conversione della famiglia utilizzano i dati raccolti utilizzando il tracciamento delle conversioni di Adobe Advertising. Inoltre, la logica di attribuzione DSP in [!DNL Analytics] utilizza solo l’ultimo evento, ma il reporting delle conversioni domestiche supporta due diversi metodi di attribuzione: Univoco e MTA.

### È possibile visualizzare i dati view-through CTV in entrambi [!DNL Analytics for Advertising] e nei rapporti personalizzati?

Inserzionisti senza [!DNL Analytics for Advertising] Per la generazione di rapporti sulle conversioni delle famiglie è possibile utilizzare solo il Rapporto conversione famiglia.

Se la tua organizzazione ha [!DNL Analytics for Advertising], utilizza entrambi i tipi di reporting insieme. Mentre il reporting view-through CTV è adatto all&#39;analisi ad ampio canale, al comportamento del sito e così via, i rapporti personalizzati forniscono una visualizzazione granulare (con dati suddivisi per tipo di media, editori e così via) per indicare i fattori che determinano i tassi di conversione.

## [!UICONTROL Household Reach & Frequency] e [!UICONTROL Household Conversions] Rapporti e dati di [!DNL Advanced Measurement Services]

Per la generazione di rapporti avanzati su portata e frequenza basate sulle famiglie o conversioni, [[!DNL Strategic Advertising Consulting] team](/help/dsp/introduction/advanced-measurement-services.md) può fornire rapporti altamente personalizzabili insieme a consigli strategici olistici. Per ulteriori informazioni su [!DNL Advanced Measurement Services], contatta il team del tuo account Adobe.

### Se utilizzo già [!DNL Advanced Measurement Services], perché utilizzare il [!UICONTROL Household Reach & Frequency] e [!UICONTROL Household Conversions] rapporti?

Il [!UICONTROL Household Reach & Frequency] e [!UICONTROL Household Conversions] i report consentono ai clienti di richiamare autonomamente in tempo reale le metriche relative a portata, frequenza e conversione a livello di famiglia.

### Posso utilizzare entrambi i [!UICONTROL Household Reach & Frequency] e [!UICONTROL Household Conversions] rapporti e [!DNL Advanced Measurement Services]?

Il caso d’uso ideale consiste nell’utilizzare sia [!UICONTROL Household] rapporto e [!DNL Advanced Measurement Services] servizi di reporting e consulenza. Considera [!UICONTROL Household] generare rapporti come transazionali, intesi a informare le ottimizzazioni quotidiane, e [!DNL Advanced Measurement Services] in quanto più strategico, destinato a informare apprendimenti e soluzioni olistiche legati a obiettivi aziendali generali.

>[!MORELIKETHIS]
>
>* [Informazioni sui report personalizzati](/help/dsp/reports/report-about.md)
>* [Creare un rapporto personalizzato](/help/dsp/reports/report-create.md)
>* [Modificare un rapporto personalizzato](/help/dsp/reports/report-edit.md)
>* [Impostazioni report personalizzati](/help/dsp/reports/report-settings.md)
>* [Colonne report disponibili](/help/dsp/reports/report-columns.md)
