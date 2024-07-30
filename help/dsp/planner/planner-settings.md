---
title: Impostazioni per i piani di copertura TV collegati
description: Vedere le descrizioni delle impostazioni per i piani di copertura TV collegati.
feature: DSP Planner
exl-id: 65edd6f5-557c-44d1-a0ed-8cd26d8a2f6e
source-git-commit: 5d8d981f08eaea2b0a0bc553ab06bd47f1e88ac9
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 0%

---

# Impostazioni per i piani di copertura TV collegati

<!-- Move out of table for consistency at some point. -->

| Parametro | Descrizione | Obbligatorio |
| --- | --- | --- |
| [!UICONTROL Name] | Nome per identificare il piano. | Sì |
| [!UICONTROL Advertiser] | L’inserzionista specifico nell’account per cui viene creato il piano. | Sì |
| [!UICONTROL Media Type] | Tipo di supporto da includere nel piano.<br><br>Al momento sono disponibili solo [!UICONTROL Connected TV]. | Sì |
| [!UICONTROL Date Range] | Le date di inizio e di fine del piano.<br><br>La data di inizio non può essere precedente alla data corrente. L’intervallo di date non può essere superiore a 90 giorni. | Sì |
| [!UICONTROL Goal Type] | Tipo di obiettivo (ad esempio [!UICONTROL Budget]) da considerare per il piano.<br><br>Al momento sono disponibili solo [!UICONTROL Budget]. | Sì |
| [!UICONTROL Goal Value] | Valore obiettivo per la previsione. Per ottenere risultati di previsione più precisi, utilizzare un valore > 5000 USD. | Sì |
| [!UICONTROL Max Bid] | L’importo massimo da pagare per 1000 impression. Se il tipo di supporto [!UICONTROL Connected TV] è selezionato, immettere un valore di almeno 10 USD. | Sì |
| [!UICONTROL Frequency Cap] | Il numero di volte in cui a una famiglia univoca devono essere serviti gli annunci.<br><br>Quando si implementa un piano e si devono creare più posizionamenti, applicare l&#39;impostazione del limite di frequenza a livello di pacchetto, non a livello di posizionamento, per garantire la corretta consegna. | Sì |
| [!UICONTROL Geo-Targeting] | Posizioni da includere o escludere come destinazioni. Le opzioni includono:<ul><li>Paesi, città, stati: fare clic sulla scheda **[!UICONTROL Country/State/City]**; selezionare se l&#39;area è un *Paese*, *Stato* o *Città*; facoltativamente espandere qualsiasi posizione per visualizzare i relativi sottocomponenti, quindi fare clic su **[!UICONTROL Include]** o **[!UICONTROL Exclude]** accanto alla posizione.</li><li>Aree di mercato designate (DMA) negli Stati Uniti: fare clic sulla scheda **[!UICONTROL DMA]**; facoltativamente espandere qualsiasi stato per visualizzare i relativi DMA, quindi fare clic su **[!UICONTROL Include]** o **[!UICONTROL Exclude]** accanto alla posizione.</li><li>Codici postali: puoi effettuare le seguenti operazioni:<ul><li>Fai clic sulla scheda **[!UICONTROL Search postal code]**, seleziona il paese, immetti il nome completo della città o le lettere contenute nel nome della città, quindi premi il tasto **[Invio]**, fai clic sul nome della città corretto per visualizzare tutti i codici postali della città, fai clic sul codice postale corretto e quindi su **[!UICONTROL Include]** o **[!UICONTROL Exclude]**.</li><li>Fare clic sulla scheda **[!UICONTROL Paste postal code]**, selezionare il paese, immettere o incollare valori separati da virgola e quindi fare clic su **[!UICONTROL Include All]** o **[!UICONTROL Exclude All]**.</li></ul></li></ul> | Sì |
| [!UICONTROL Inventory Targeting] | Origini di magazzino da includere o escludere come destinazioni. Seleziona almeno un feed o un’origine. | Sì |
| [!UICONTROL Site/App Targeting] | Siti Web e app da includere o escludere come destinazioni. Immettere un URL per riga, quindi fare clic su **[!UICONTROL Include All]** o **[!UICONTROL Exclude All]**. | No |
| [!UICONTROL Audience Targeting] | Tipi di pubblico da includere o escludere come target. | No |
| [!UICONTROL Ad duration] | La durata degli annunci da considerare per il piano. | No |

>[!MORELIKETHIS]
>
>* [Informazioni sullo strumento DSP Planner](planner-about.md)
>* [Crea un piano di copertura TV collegato](planner-create.md)
>* [Duplicare un piano di copertura TV collegata](planner-duplicate.md)
>* [Modifica un piano di copertura TV collegato](planner-edit.md)
>* [Esporta un piano di copertura TV collegato](planner-export.md)
>* [Rigenerare la previsione per un piano di copertura TV collegato](planner-forecast.md)
>* [Archivia un piano di copertura TV collegato](planner-archive.md)
