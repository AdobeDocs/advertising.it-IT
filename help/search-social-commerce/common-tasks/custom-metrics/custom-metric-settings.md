---
title: Impostazioni metriche personalizzate
description: Fai riferimento alle impostazioni per le metriche personalizzate, calcolate dalle metriche standard.
exl-id: b9e8434d-5ea2-47cd-9d63-705a6337c34c
feature: Search Common Tasks, Search Custom Metrics
TQID: https://experienceleague.adobe.com/yyXHbc4ll8-Y4v3v0p3zMKi6zQVYXQr3bYApBEGGN-s
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 616
ht-degree: 0%

---

# Impostazioni metriche personalizzate

Le impostazioni delle metriche personalizzate sono leggermente diverse nelle diverse parti dell’interfaccia.

## Impostazioni delle metriche personalizzate nella maggior parte delle visualizzazioni di gestione

| Parametro/Sezione | Descrizione |
|----|----|
| Nome metrica personalizzata | Il nome della metrica, visualizzato come nome della colonna. <b>Suggerimento:</b> utilizzare un nome di metrica significativo, ma considerare che nomi più lunghi aumentano la larghezza della colonna. |
| Inserisci metrica | La formula matematica utilizzata per calcolare la nuova metrica (ad esempio [Costo]/[Registrazioni]:<ul><li>Per inserire una metrica dall&#39;elenco delle metriche di traffico e ricavi, posizionare il cursore nel punto in cui si desidera inserire la metrica, quindi selezionarla dall&#39;elenco o immetterla manualmente e racchiusa tra parentesi (ad esempio, `[CPC]`).</li><li>Per inserire un operatore, posizionare il cursore nel punto in cui si desidera inserire l&#39;operatore, quindi fare clic sul pulsante o immettere il simbolo manualmente. Operatori matematici disponibili: `+ - * / ( ) ()`</li></ul><b>Nota:</b> il calcolo delle metriche personalizzate complesse richiede più tempo e la generazione dei report e delle visualizzazioni che le includono, in particolare quando includono colonne separate per le conversioni click-through e view-through, richiede più tempo. |
| Formato | Come presentare i dati per questa metrica: *[!UICONTROL Currency]* (valore monetario), *[!UICONTROL Number to 2 Decimal Points]*, *[!UICONTROL Number to 3 Decimal Points]*, *[!UICONTROL Number w/out Decimal Points]* o *[!UICONTROL Percentage]* (percentuale con due punti decimali).<br><br><b>Attenzione:</b> se si crea una metrica derivata con il formato [!UICONTROL Number w/out Decimal Points] (che mostra i dati come numeri interi) e li si include in una visualizzazione o in un report che utilizza una regola di attribuzione di conversione ponderata ([!UICONTROL Weight First Event More], [!UICONTROL Weight Last Event More] o [!UICONTROL Even Distribution]), l&#39;output verrà visualizzato in numeri interi e non in decimali. Di conseguenza, i singoli campi dati potrebbero essere errati, anche se i totali sono corretti. Ad esempio, se un ordine è diviso in modo uniforme tra tre eventi, a ciascuno di essi viene attribuito un ordine (anziché 0,33). Per evitare il problema, utilizzare il formato di metrica [!UICONTROL Number to 2 Decimal Points]. |

## Impostazioni delle metriche personalizzate nei report e nei modelli di report e nelle [!UICONTROL Portfolios] visualizzazioni legacy

| Parametro/Sezione | Descrizione |
|----|----|
| Nome metrica personalizzata | Il nome della metrica, visualizzato come nome della colonna. <b>Suggerimento:</b> utilizzare un nome di metrica significativo, ma considerare che nomi più lunghi aumentano la larghezza della colonna. |
| Formato | Come presentare i dati per questa metrica: *[!UICONTROL Currency]* (valore monetario), *[!UICONTROL Number to 2 Decimal Points]*, *[!UICONTROL Number to 3 Decimal Points]*, *[!UICONTROL Number w/out Decimal Points]* o *[!UICONTROL Percentage]* (percentuale con due punti decimali).<br><br><b>Attenzione:</b> se si crea una metrica derivata con il formato [!UICONTROL Number w/out Decimal Points] (che mostra i dati come numeri interi) e li si include in una visualizzazione o in un report che utilizza una regola di attribuzione di conversione ponderata ([!UICONTROL Weight First Event More], [!UICONTROL Weight Last Event More] o [!UICONTROL Even Distribution]), l&#39;output verrà visualizzato in numeri interi e non in decimali. Di conseguenza, i singoli campi dati potrebbero essere errati, anche se i totali sono corretti. Ad esempio, se un ordine è diviso in modo uniforme tra tre eventi, a ciascuno di essi viene attribuito un ordine (anziché 0,33). Per evitare il problema, utilizzare il formato di metrica [!UICONTROL Number to 2 Decimal Points]. |
| Inserisci metrica | Elenco di metriche esistenti da cui è possibile creare una formula.<br><br>Per inserire una metrica nel campo di input della formula, posizionare il cursore nel punto in cui si desidera inserire la metrica, quindi selezionare la metrica dall&#39;elenco oppure immetterla manualmente e racchiusa tra parentesi (ad esempio, `[CPC]`). |
| Inserisci operatore | Operatori matematici disponibili: `+ - x / ( )`<br><br>Per inserire un operatore nel campo di input della formula, posizionare il cursore nel punto in cui si desidera inserire l&#39;operatore, quindi fare clic sul pulsante o immettere il simbolo manualmente. |
| [Campo di input formula per la metrica] | Formula matematica utilizzata per calcolare la nuova metrica in base a una o più proprietà esistenti o metriche standard, ad esempio `[Cost]/[Registrations]`. Può includere qualsiasi combinazione di metriche e operatori.<br><br><b>Nota:</b> il calcolo delle metriche personalizzate complesse richiede più tempo e la generazione dei report e delle visualizzazioni che le includono, in particolare quando includono colonne separate per le conversioni click-through e view-through, richiede più tempo. |

>[!MORELIKETHIS]
>
>* [Informazioni sulle metriche personalizzate](custom-metric-about.md)
>* [Creare una metrica personalizzata](custom-metric-create.md)
>* [Modificare una metrica personalizzata](custom-metric-edit.md)
>* [Eliminare una metrica personalizzata](custom-metric-delete.md)
