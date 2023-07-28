---
title: Impostazioni metriche personalizzate
description: Fai riferimento alle impostazioni per le metriche personalizzate, calcolate dalle metriche standard.
exl-id: f4b8c44e-ecb3-46dc-9a68-c079188e1d75
feature: Search Common Tasks, Search Custom Metrics
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '613'
ht-degree: 0%

---

# Impostazioni metriche personalizzate

Le impostazioni delle metriche personalizzate sono leggermente diverse nelle diverse parti dell’interfaccia.

## Impostazioni delle metriche personalizzate nelle visualizzazioni di gestione delle campagne

| Parametro/Sezione | Descrizione |
|----|----|
| Nome metrica personalizzata | Il nome della metrica, visualizzato come nome della colonna. <b>Suggerimento</b> Utilizza un nome di metrica significativo, ma considera che i nomi più lunghi aumentano la larghezza della colonna. |
| Inserisci metrica | La formula matematica utilizzata per calcolare la nuova metrica (ad esempio [Costo]/[Registrazioni]:<ul><li>Per inserire una metrica dall’elenco delle metriche del traffico e delle entrate, posiziona il cursore nel punto in cui desideri inserire la metrica, quindi selezionala dall’elenco o immettila manualmente e racchiusa tra parentesi (ad esempio, `[CPC]`).</li><li>Per inserire un operatore, posizionare il cursore nel punto in cui si desidera inserire l&#39;operatore, quindi fare clic sul pulsante o immettere il simbolo manualmente. Gli operatori matematici disponibili: `+ - * / ( ) ()`</li></ul><b>Nota:</b> Il calcolo di metriche personalizzate complesse richiede più tempo e la generazione di rapporti e viste che le includono, soprattutto se includono colonne separate per le conversioni click-through e view-through, richiede più tempo. |
| Formato | Come presentare i dati per questa metrica: *[!UICONTROL Currency]* (un valore monetario), *[!UICONTROL Number to 2 Decimal Points]*, *[!UICONTROL Number to 3 Decimal Points]*, *[!UICONTROL Number w/out Decimal Points]*, o *[!UICONTROL Percentage]* (una percentuale con due punti decimali).<br><br><b>Attenzione:</b> Se crei una metrica derivata con il formato [!UICONTROL Number w/out Decimal Points] (che mostra i dati come numeri interi) e li include in una visualizzazione o in un report che utilizza una regola di attribuzione di conversione ponderata ([!UICONTROL Weight First Event More], [!UICONTROL Weight Last Event More], o [!UICONTROL Even Distribution]), l’output viene visualizzato in numeri interi, non in decimali. Di conseguenza, i singoli campi dati potrebbero essere errati, anche se i totali sono corretti. Ad esempio, se un ordine è diviso in modo uniforme tra tre eventi, a ciascuno di essi viene attribuito un ordine (anziché 0,33). Per evitare il problema, utilizza il formato metrica [!UICONTROL Number to 2 Decimal Points]. |

## Impostazioni delle metriche personalizzate nei rapporti e nei modelli di rapporto e nel [!UICONTROL Portfolios] visualizzazioni

| Parametro/Sezione | Descrizione |
|----|----|
| Nome metrica personalizzata | Il nome della metrica, visualizzato come nome della colonna. <b>Suggerimento</b> Utilizza un nome di metrica significativo, ma considera che i nomi più lunghi aumentano la larghezza della colonna. |
| Formato | Come presentare i dati per questa metrica: *[!UICONTROL Currency]* (un valore monetario), *[!UICONTROL Number to 2 Decimal Points]*, *[!UICONTROL Number to 3 Decimal Points]*, *[!UICONTROL Number w/out Decimal Points]*, o *[!UICONTROL Percentage]* (una percentuale con due punti decimali).<br><br><b>Attenzione:</b> Se crei una metrica derivata con il formato [!UICONTROL Number w/out Decimal Points] (che mostra i dati come numeri interi) e li include in una visualizzazione o in un report che utilizza una regola di attribuzione di conversione ponderata ([!UICONTROL Weight First Event More], [!UICONTROL Weight Last Event More], o [!UICONTROL Even Distribution]), l’output viene visualizzato in numeri interi, non in decimali. Di conseguenza, i singoli campi dati potrebbero essere errati, anche se i totali sono corretti. Ad esempio, se un ordine è diviso in modo uniforme tra tre eventi, a ciascuno di essi viene attribuito un ordine (anziché 0,33). Per evitare il problema, utilizza il formato metrica [!UICONTROL Number to 2 Decimal Points]. |
| Inserisci metrica | Elenco di metriche esistenti da cui è possibile creare una formula.<br><br>Per inserire una metrica nel campo di input della formula, posizionare il cursore nel punto in cui si desidera inserire la metrica, quindi selezionare la metrica dall&#39;elenco o immetterla manualmente e racchiusa tra parentesi (ad esempio, `[CPC]`). |
| Inserisci operatore | Gli operatori matematici disponibili: `+ - x / ( )`<br><br>Per inserire un operatore nel campo di inserimento della formula, posizionare il cursore nel punto in cui si desidera inserire l&#39;operatore, quindi fare clic sul pulsante o immettere il simbolo manualmente. |
| [Campo di input della formula per la metrica] | La formula matematica utilizzata per calcolare la nuova metrica in base a una o più proprietà o metriche standard esistenti (ad esempio `[Cost]/[Registrations]`. Può includere qualsiasi combinazione di metriche e operatori.<br><br><b>Nota:</b> Il calcolo di metriche personalizzate complesse richiede più tempo e la generazione di rapporti e viste che le includono, soprattutto se includono colonne separate per le conversioni click-through e view-through, richiede più tempo. |

>[!MORELIKETHIS]
>
>* [Informazioni sulle metriche personalizzate](custom-metric-about.md)
>* [Creare una metrica personalizzata](custom-metric-create.md)
>* [Modificare una metrica personalizzata](custom-metric-edit.md)
>* [Eliminare una metrica personalizzata](custom-metric-delete.md)
