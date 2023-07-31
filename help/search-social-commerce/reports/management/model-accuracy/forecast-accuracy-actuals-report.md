---
title: '[!UICONTROL Forecast Accuracy (Actuals) Report]'
description: Scopri di più su [!UICONTROL Forecast Accuracy (Actuals) Report], incluse le colonne di dati.
exl-id: ff49284a-2d13-48bf-a172-3bd461db7a3c
feature: Search Reports, Search Model Accuracy Reports
source-git-commit: 97111c6cd38098cac72b8773390afd254a017d1d
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 0%

---

# Il [!UICONTROL Forecast Accuracy (Actuals) Report]

Questo rapporto mostra i dati effettivi su impression, clic, costi e ricavi dalla rete di annunci per giorno per ciascun portfolio.

## Colonne disponibili

Di seguito sono riportate le colonne incluse automaticamente in ogni rapporto. Non puoi aggiungere altre colonne.

| Colonna | Predefinito? | Descrizione |
|----|----|----|
| [!UICONTROL Portfolio Group Name] | Predefinito | Il nome del gruppo di portfolio a cui appartiene il portfolio. |
| [!UICONTROL Portfolio ID] | Predefinito | L’ID numerico del portfolio. |
| [!UICONTROL EF Portfolio Group ID] | Predefinito | L’ID numerico del gruppo di portfolio a cui appartiene il portfolio. |
| [!UICONTROL Portfolio] | Predefinito | Il portfolio. |
| [!UICONTROL Portfolio Status] | Predefinito | Lo stato del portfolio:<ul><li><i>[!UICONTROL Optimize]:</i> La funzionalità di ottimizzazione raccoglie i dati su clic e ricavi per le campagne pertinenti, modella i dati per ottimizzare le offerte e ottimizza le offerte e/o i budget delle campagne (a seconda del tipo di ottimizzazione e delle strategie di offerta della campagna).</li><li><i>[!UICONTROL Active]:</i> La funzionalità di ottimizzazione raccoglie i dati sui clic e sui ricavi per le campagne pertinenti e modella i dati, ma non ottimizza le offerte o i budget delle campagne.</li><li><i>[!UICONTROL Inactive]:</i> La funzionalità di ottimizzazione raccoglie i dati dei clic per le campagne rilevanti a scopo di reporting, ma non si tratta di modellare i dati né di ottimizzare le offerte o i budget delle campagne. |
| [!UICONTROL Day of Week] | Predefinito | Il giorno della settimana riportato: <i>[!UICONTROL Sunday]</i>, <i>[!UICONTROL Monday]</i>, <i>[!UICONTROL Tuesday]</i>, <i>[!UICONTROL Wednesday]</i>, <i>[!UICONTROL Thursday]</i>, <i>[!UICONTROL Friday]</i>, o <i>[!UICONTROL Saturday]</i>. |
| [!UICONTROL Event Date] | Predefinito | La data riportata. |
| [!UICONTROL Device] | Predefinito | (Google Ads, Microsoft® Advertising, Yahoo! Rete di visualizzazione, Yahoo! Japan Ads e Yahoo Native campaigns) Il tipo di dispositivo su cui sono stati visualizzati gli annunci: <i>[!UICONTROL Computers]</i>, <i>[!UICONTROL Mobile]</i>, <i>[!UICONTROL Tablets]</i>, <i>[!UICONTROL Other]</i>, o <i>[!UICONTROL N/A]</i> (nessun valore). Le righe per altre reti di annunci hanno valori di <i>[!UICONTROL N/A]</i>.<br><br>Nelle campagne di ricerca, se i modelli di tracciamento o gli URL di destinazione per le parole chiave, gli annunci e/o le estensioni degli annunci includevano parametri per il tracciamento dei dati per dispositivo (<code>&amp;ev_dvc={device}&amp;ev_dvm={devicemodel}</code>) al momento in cui l’annuncio è stato fatto clic, nella riga di ogni tipo di dispositivo vengono inclusi anche i dati di conversione. In caso contrario, se i dati di conversione non possono essere attribuiti a un tipo di dispositivo, vengono aggregati in una riga separata con un &quot;[!UICONTROL Device]&quot; valore di <i>[!UICONTROL N/A]</i>. |
| [!UICONTROL Revenue] | Predefinito | Ricavi totali. |
| [!UICONTROL Impressions] | Predefinito | Il totale delle impression. |
| [!UICONTROL Clicks] | Predefinito | Il numero totale di clic. |
| [!UICONTROL Cost] | Predefinito | Il costo totale. |

>[!MORELIKETHIS]
>
>* [Informazioni sui report di precisione dei modelli](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md)
>* [Il [!UICONTROL Forecast Accuracy Report]](forecast-accuracy-report.md)
>* [Generare un report di precisione del modello](model-accuracy-report-generate.md)
>* [Impostazioni report di precisione modello](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-settings.md)
