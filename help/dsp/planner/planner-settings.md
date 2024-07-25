---
title: Impostazioni per i piani di copertura TV collegati
description: Vedere le descrizioni delle impostazioni per i piani di copertura TV collegati.
feature: DSP Planner
exl-id: 65edd6f5-557c-44d1-a0ed-8cd26d8a2f6e
source-git-commit: 37b901093d7eff65d783e558f2e98c5d288a8286
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Impostazioni per i piani di copertura TV collegati

| Parametro | Descrizione | Obbligatorio |
| --- | --- | --- |
| Nome | Nome per identificare il piano. | Sì |
| Inserzionista | L’inserzionista specifico nell’account per cui viene creato il piano. | Sì |
| Tipo di file multimediale | Tipo di supporto da includere nel piano.<br><br>Al momento sono disponibili solo [!UICONTROL Connected TV]. | Sì |
| Intervallo date | Le date di inizio e di fine del piano.<br><br>La data di inizio non può essere precedente alla data corrente. L’intervallo di date non può essere superiore a 90 giorni. | Sì |
| Tipo di obiettivo | Tipo di obiettivo (ad esempio [!UICONTROL Budget]) da considerare per il piano.<br><br>Al momento sono disponibili solo [!UICONTROL Budget]. | Sì |
| Valore obiettivo | Valore obiettivo per la previsione. Per ottenere risultati di previsione più precisi, utilizzare un valore > 5000 USD. | Sì |
| Offerta massima | L’importo massimo da pagare per 1000 impression. Se il tipo di supporto [!UICONTROL Connected TV] è selezionato, immettere un valore di almeno 10 USD. | Sì |
| Limite di frequenza | Il numero di volte in cui a una famiglia univoca devono essere serviti gli annunci.<br><br>Quando si implementa un piano e si devono creare più posizionamenti, applicare l&#39;impostazione del limite di frequenza a livello di pacchetto, non a livello di posizionamento, per garantire la corretta consegna. | Sì |
| Geo-Targeting | Posizioni da includere o escludere come destinazioni. Le opzioni includono paesi, città, stati, aree di mercato designate (DMA) e codici postali (che è possibile a) incollare come valori separati da virgole per un paese specificato o b) cercare per paese e città). | Sì |
| Targeting inventario | Origini di magazzino da includere o escludere come destinazioni. Seleziona almeno un feed o un’origine. | Sì |
| Targeting sito/app | Siti Web e app da includere o escludere come destinazioni. Immettere un URL per riga, quindi fare clic su **[!UICONTROL Include All]** o **[!UICONTROL Exclude All]** sotto il campo di input. | No |
| Targeting del pubblico | Tipi di pubblico da includere o escludere come target. | No |
| Durata annuncio | La durata degli annunci da considerare per il piano. | No |

>[!MORELIKETHIS]
>
>* [Informazioni sullo strumento DSP Planner](planner-about.md)
>* [Crea un piano di copertura TV collegato](planner-create.md)
>* [Duplicare un piano di copertura TV collegata](planner-duplicate.md)
>* [Modifica un piano di copertura TV collegato](planner-edit.md)
>* [Esporta un piano di copertura TV collegato](planner-export.md)
>* [Rigenerare la previsione per un piano di copertura TV collegato](planner-forecast.md)
>* [Archivia un piano di copertura TV collegato](planner-archive.md)
