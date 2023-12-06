---
title: Impostazioni per i piani di copertura TV collegati
description: Vedere le descrizioni delle impostazioni per i piani di copertura TV collegati.
feature: DSP Planner
source-git-commit: 72ee396019d5a444bd326fe659ce68eb3490a439
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 0%

---

# Impostazioni per i piani di copertura TV collegati

*Funzione beta*

| Parametro | Descrizione | Obbligatorio |
| --- | --- | --- |
| Nome | Nome per identificare il piano. | Sì |
| Inserzionista | L’inserzionista specifico nell’account per cui viene creato il piano. | Sì |
| Tipo di file multimediale | Tipo di supporto da includere nel piano.<br><br>Attualmente, solo [!UICONTROL Connected TV] è disponibile. | Sì |
| Intervallo date | Le date di inizio e di fine del piano.<br><br>La data di inizio non può essere precedente alla data corrente. L’intervallo di date non può essere superiore a 90 giorni. | Sì |
| Tipo di obiettivo | Il tipo di obiettivo (ad esempio [!UICONTROL Budget]) da considerare per il piano.<br><br>Attualmente, solo [!UICONTROL Budget] è disponibile. | Sì |
| Valore obiettivo | Valore obiettivo per la previsione. Per ottenere risultati di previsione più precisi, utilizzare un valore > 5000 USD. | Sì |
| Offerta massima | L’importo massimo da pagare per 1000 impression. Se il [!UICONTROL Connected TV] tipo di file multimediale selezionato, inserisci un valore di almeno 10 USD. | Sì |
| Limite di frequenza | Il numero di volte in cui a una famiglia univoca devono essere serviti gli annunci.<br><br>Quando implementi un piano e devi creare più posizionamenti, applica l’impostazione del limite di frequenza a livello di pacchetto, non a livello di posizionamento, per garantire la consegna corretta. | Sì |
| Geo-Targeting | Posizioni da includere o escludere come destinazioni. | Sì |
| Targeting inventario | Origini di magazzino da includere o escludere come destinazioni. Seleziona almeno un feed o un’origine. | Sì |
| Targeting del pubblico | Tipi di pubblico da includere o escludere come target. | No |
| Durata annuncio | La durata degli annunci da considerare per il piano. | No |

>[!MORELIKETHIS]
>
>* [Informazioni sullo strumento DSP Planner](planner-about.md)
>* [Creazione di un piano di copertura TV collegata](planner-create.md)
>* [Duplicare un piano di portata TV collegato](planner-duplicate.md)
>* [Modifica di un piano di copertura TV collegato](planner-edit.md)
>* [Esportazione di un piano di copertura TV collegato](planner-export.md)
>* [Rigenerare la previsione per un piano di copertura TV collegato](planner-forecast.md)
>* [Archiviare un piano di portata TV collegato](planner-archive.md)
