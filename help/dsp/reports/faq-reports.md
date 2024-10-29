---
title: Domande frequenti sui rapporti personalizzati
description: Ulteriori informazioni sui rapporti personalizzati, inclusi i rapporti sulla famiglia e i rapporti di analisi del percorso di conversione.
exl-id: 3ffd178e-de41-4663-b85f-bd8ce3eb0dad
source-git-commit: 0ecceaf30ce135dd0083e34dd5c8c5bafb5a3c16
workflow-type: tm+mt
source-wordcount: '1183'
ht-degree: 0%

---

# Domande frequenti sui rapporti personalizzati

## Rapporti famiglia

### Il report [!UICONTROL Household Reach & Frequency]

#### Quali sono le differenze tra i report [!UICONTROL Household Reach & Frequency] e gli altri report personalizzati?

Il report [!UICONTROL Household Reach & Frequency] misura portata, impression e frequenza tra varie dimensioni a livello di famiglia in base all&#39;indirizzo IP. Gli altri rapporti personalizzati vengono generati a livello di dispositivo o cookie.

Ad esempio, anche se un’impression viene trasmessa a tre dispositivi all’interno di una famiglia, la metrica Raggiunto in famiglia univoca è pari a uno.

##### Dimension supportati

Il report [!UICONTROL Household Reach & Frequency] supporta le [dimensioni seguenti](/help/dsp/reports/report-columns.md): &quot;[!UICONTROL Campaign],&quot; &quot;[!UICONTROL Package],&quot; &quot;[!UICONTROL Placement],&quot; &quot;[!UICONTROL Site/Apps]&quot; (che non fornisce l&#39;accesso alle metriche di sovrapposizione), &quot;[!UICONTROL Media Type],&quot; &quot;[!UICONTROL Feed Type],&quot; &quot;[!UICONTROL Device],&quot; &quot;[!UICONTROL Publisher],&quot; &quot;[!UICONTROL Audience],&quot; &quot;[!UICONTROL Creative Length]&quot; e il posizionamento creato dall&#39;utente &quot;[!UICONTROL Tags].&quot; |

##### Metriche supportate

Le [metriche disponibili](/help/dsp/reports/report-columns.md) includono:

* Metriche di sovrapposizione: [!UICONTROL Frequency Overlap], [!UICONTROL Measurable Impressions (Overlap)] e [!UICONTROL Unique Household (Overlap)].

  Le metriche di sovrapposizione sono i valori che si verificano solo per la dimensione o la combinazione di dimensioni segnalata e non per altre dimensioni. <!-- For example, it might show the ?? -->

* Metriche non di sovrapposizione: [!UICONTROL Frequency], [!UICONTROL Incremental Household Reached], [!UICONTROL % Incremental Household Reached], [!UICONTROL Impressions], [!UICONTROL Measurable Impressions] e [!UICONTROL Unique Household Reached]

Le metriche di conversione e gli obiettivi personalizzati non sono supportati.

#### Qual è la differenza tra le metriche di sovrapposizione e non di sovrapposizione?

La figura seguente mostra tre metriche (Famiglia univoca raggiunta, Famiglia incrementale raggiunta e Famiglia incrementale (Sovrapposizione)) per tre campagne (A, B e C).

![Illustrazione delle metriche di sovrapposizione famiglia](/help/dsp/assets/household-overlap-metrics-illustration.png "Illustrazione delle metriche di sovrapposizione famiglia")

* Famiglia univoca raggiunta (totale) fornisce la famiglia univoca raggiunta da ciascuna campagna o l’area totale di ciascun cerchio. Nella figura, Famiglia univoca raggiunta da A = Famiglia incrementale raggiunta da A + (A+B) + (A+C) + (A+B+C)

* La famiglia incrementale raggiunta è la famiglia unica raggiunta solo da una campagna. Nella figura, la famiglia incrementale raggiunta da A, B, C è la famiglia incrementale raggiunta rispettivamente da A, B, C.

* Famiglia incrementale (sovrapposizione) è la famiglia univoca raggiunta dalla campagna o dalla combinazione di campagne. Nella figura, la famiglia incrementale raggiunta da A, C è A+C.

#### Flusso di lavoro

Segui i normali passaggi per [creare un rapporto personalizzato](report-create.md).

Il report [!UICONTROL Household Reach & Frequency] può includere una sola dimensione. Può anche includere a) metriche di sovrapposizione per qualsiasi dimensione ad eccezione di Sito/App o b) metriche non di sovrapposizione, ma non entrambe.

#### Quali sono alcune limitazioni del report [!UICONTROL Household Reach & Frequency]?

Report con intersezioni di output di metriche di sovrapposizione fino a tre valori. Ad esempio, se utilizzi la metrica [!UICONTROL Unique Household (Overlap)] per 10 posizionamenti, puoi vedere le famiglie univoche raggiunte dai posizionamenti individuali, le famiglie comuni raggiunte da una combinazione di due posizionamenti qualsiasi e le famiglie comuni raggiunte da combinazioni di tre posizionamenti qualsiasi. Non si possono vedere famiglie comuni raggiunte da quattro o più posizionamenti.

Per dimensioni diverse da campagna, pacchetto o posizionamento, il rapporto supporta fino a 10 valori in ogni dimensione. Ad esempio, per generare un report [!UICONTROL Unique Household Reached] per la dimensione [!UICONTROL Audience], il numero di tipi di pubblico univoci deve essere minore o uguale a 10. Se includi più di 10 tipi di pubblico univoci, viene generato un rapporto vuoto.

#### Perché la frequenza e i valori univoci di portata sono diversi tra i miei rapporti [!UICONTROL Custom] e il rapporto [!UICONTROL Household Reach & Frequency]?

Queste metriche nei report [!UICONTROL Household] vengono calcolate utilizzando il conteggio effettivo degli indirizzi IP, mentre le metriche nel report [!UICONTROL Custom] utilizzano i numeri stimati calcolati utilizzando i modelli. Tuttavia, la discrepanza dovrebbe essere inferiore al 10%.

#### Come si configura il report per la dimensione [!UICONTROL Placement Tags]?

Per creare i tag per il posizionamento, [apri le impostazioni di posizionamento](/help/dsp/campaign-management/placements/placement-edit.md) e immetti i valori nel campo [Tag di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md).

Quando un posizionamento include più tag, il rapporto considera l’intera stringa come un unico tag. Il rapporto include una riga per ogni stringa univoca.

### Il report [!UICONTROL Household Conversions]

#### Quali metodi di attribuzione sono supportati nel report [!UICONTROL Household Conversions]?

Sono supportati due tipi di metodi di attribuzione:

* [!UICONTROL Unique]: conta il numero di volte in cui un valore di dimensione (ad esempio un dispositivo o un posizionamento) si trovava nel percorso di conversione.

* [!UICONTROL Multi-Touch Attribution (MTA)]: distribuisce il credito di ogni conversione in base alla frequenza di occorrenza del valore di dimensione (ad esempio un dispositivo o un posizionamento) nel percorso di conversione. Ad esempio, se il totale delle impression prima della conversione era 10, con 8 su CTV e 2 su Mobile, l&#39;80% del credito (0,8) viene assegnato agli schermi CTV e 0,2 a Mobile.

#### In che modo i rapporti sulle conversioni domestiche differiscono dai rapporti view-through CTV in Adobe Analytics?

I dati view-through CTV in [!DNL Analytics] sono alimentati dal monitoraggio di [!DNL Analytics] e i dati di conversione della famiglia utilizzano i dati raccolti mediante il monitoraggio delle conversioni Adobe Advertising. Inoltre, la logica di attribuzione DSP in [!DNL Analytics] utilizza solo l&#39;ultimo evento, ma il reporting di conversione delle famiglie supporta due diversi metodi di attribuzione: Univoco e MTA.

#### È possibile visualizzare i dati view-through CTV sia in [!DNL Analytics for Advertising] che nei report personalizzati?

Gli inserzionisti senza [!DNL Analytics for Advertising] possono utilizzare solo il Report conversione famiglia per i report di conversione famiglia.

Se la tua organizzazione dispone di [!DNL Analytics for Advertising], utilizza entrambi i tipi di reporting insieme. Mentre il reporting view-through CTV è adatto all&#39;analisi ad ampio canale, al comportamento del sito e così via, i rapporti personalizzati forniscono una visualizzazione granulare (con dati suddivisi per tipo di media, editori e così via) per indicare i fattori che determinano i tassi di conversione.

### [!UICONTROL Household Reach & Frequency] e [!UICONTROL Household Conversions] rapporti e dati da [!DNL Advanced Measurement Services]

Per rapporti avanzati su portata e frequenza o conversioni basate su famiglia, il [[!DNL Strategic Advertising Consulting] team](/help/dsp/introduction/advanced-measurement-services.md) può fornire rapporti altamente personalizzabili insieme a consigli strategici olistici. Per ulteriori informazioni su [!DNL Advanced Measurement Services], contatta il team del tuo account Adobe.

#### Se utilizzo già [!DNL Advanced Measurement Services], perché dovrei usare i report [!UICONTROL Household Reach & Frequency] e [!UICONTROL Household Conversions]?

I report [!UICONTROL Household Reach & Frequency] e [!UICONTROL Household Conversions] consentono ai client di richiamare autonomamente in tempo reale le metriche relative alla portata, alla frequenza e alla conversione a livello di famiglia.

#### Posso utilizzare sia i report [!UICONTROL Household Reach & Frequency] che [!UICONTROL Household Conversions] e [!DNL Advanced Measurement Services]?

Il caso d&#39;uso ideale consiste nell&#39;utilizzare insieme il report [!UICONTROL Household] e i servizi di reporting e consulenza [!DNL Advanced Measurement Services]. Considera il rapporto [!UICONTROL Household] come transazionale, concepito per informare le ottimizzazioni quotidiane, e [!DNL Advanced Measurement Services] come più strategico, concepito per informare gli apprendimenti olistici e i tentativi legati agli obiettivi di business generali.

## Rapporti di analisi del percorso di conversione

### Confronto tra il rapporto Percorso di conversione e i rapporti creati da [!DNL Advanced Measurement Services] e Adobe Analytics

| | Percorso del rapporto di conversione | Effetto alone servizi di misurazione avanzati sui report di ricerca | Rapporti di Adobe Analytics Workspace |
| --- | --- | --- |---|
| Valore per il cliente | Genera un rapporto personalizzato self-service per capire quali percorsi del percorso di annunci hanno portato a più conversioni per aumentare l’ottimizzazione | Comprendere l&#39;influenza delle tattiche di TV collegata (CTV) sui clic di ricerca | Comprendi l’influenza del tuo investimento Adobe Advertising olistico, insieme ad altri canali di marketing, sui clic di ricerca |
| Livello familiare | Sì | Sì | No |
| CTV è supportato? | Sì | Sì | Sì |
| Metodologia di attribuzione | L’ultimo evento di contatto (impression o clic) deve trovarsi nella finestra del lookbook. | Univoci | Ultimo contatto |
| | Per il percorso di conversione vengono considerati i punti di interazione che precedono di oltre 30 giorni l’evento di ultimo contatto. | (Il CTV riceve credito, indipendentemente da dove si verifica l&#39;esposizione al CTV nel percorso del clic dell&#39;utente) | (CTV ottiene credito se l&#39;impression è l&#39;ultimo evento nell&#39;intervallo di lookback E non c&#39;è alcun click a pagamento da altri formati prima o dopo l&#39;esposizione CTV) |
| Livello di reporting | Granulare | Granulare | Ampia |
| | (Tipo Di Canale, Creativo/Annuncio, Parola Chiave, Percorsi, Lunghezza, Tempo Di Conversione) | (CTV Tactic, app CTV/editore) | (Adobe Advertising e altri canali di marketing) |
| Canali di marketing | DSP + Cerca (da Ricerca, Social e Commerce) | DSP + Cerca (da Ricerca, Social e Commerce) | Canali di marketing non tracciati dall’ID EF di click-through dell’Adobe Advertising (ad esempio, Ricerca organica, Social organico, E-mail e Affiliate) |
| Metriche di conversione supportate | Metriche tracciate utilizzando il pixel evento Adobe Advertising (AMO ID) e il tracciamento di Adobe Analytics | Clic (nessuna conversione) | Metriche tracciate con il tracciamento di Adobe Analytics |

Per ulteriori informazioni sull&#39;effetto Halo Advanced Measurement Services sui report di ricerca, vedere &quot;[Advanced Measurement Services](/help/dsp/introduction/advanced-measurement-services.md).&quot;

>[!MORELIKETHIS]
>
>* [Informazioni sui report personalizzati](/help/dsp/reports/report-about.md)
>* [Crea un report personalizzato](/help/dsp/reports/report-create.md)
>* [Modifica un report personalizzato](/help/dsp/reports/report-edit.md)
>* [Impostazioni report personalizzati](/help/dsp/reports/report-settings.md)
>* [Colonne report disponibili](/help/dsp/reports/report-columns.md)
