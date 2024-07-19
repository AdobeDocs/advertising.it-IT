---
title: '[!UICONTROL Forecast Accuracy Report]'
description: Scopri il rapporto Precisione previsione, comprese le colonne di dati.
exl-id: f0c42323-eb0d-461a-ab09-440fd1bfc960
feature: Search Reports, Search Model Accuracy Reports
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 0%

---

# [!UICONTROL Forecast Accuracy Report]

Il rapporto mostra la precisione dei modelli di costi e ricavi per giorno per portafogli specifici. Per impostazione predefinita, per ogni portfolio sono inclusi i ricavi, i costi e i clic previsti ed effettivi su base giornaliera, nonché l&#39;accuratezza delle previsioni. Include i dati delle campagne attualmente mappate sui portfolio.

Puoi visualizzare i dati relativi ai 18 mesi precedenti.

>[!NOTE]
>
>* Questo report fornisce gli stessi dati del livello di portfolio [!UICONTROL Model Accuracy Report], con la differenza che è possibile eseguirlo in più portfolio e modificare la regola di attribuzione. È inoltre possibile eseguire e pianificare il report utilizzando parametri personalizzati e utilizzarlo per creare feed di fogli di calcolo.
>
>* La best practice prevede di visualizzare [!UICONTROL Forecast Accuracy Report] per almeno gli ultimi sette giorni perché, indipendentemente dalla strategia di spesa del portfolio, la maggior parte dei portfolio presenta un trend intrinseco del giorno della settimana. La funzionalità di ottimizzazione prende in considerazione questa tendenza e alloca la spesa di conseguenza.
>
>* Per le previsioni di costo, una deviazione del 10% negli ultimi sette giorni è considerata accettabile, pertanto la spesa effettiva compresa tra il 90% e il 110% della spesa prevista va bene. Per le previsioni di entrate, una deviazione del 15% negli ultimi sette giorni è considerata accettabile, quindi un reddito effettivo compreso tra l’85% e il 115% della spesa prevista va bene. Si dovrebbero esaminare le previsioni con scostamenti più elevati.
>
>* Quando le parole chiave nel portfolio sono associate a vincoli di spostamento dell’offerta, il portfolio sovrascrive o sottoutilizza l’importo totale causato dallo spostamento dell’offerta. Di conseguenza, le colonne dei costi previsti si discostano dalla spesa target per l’aumento o la riduzione della spesa.

## Colonne disponibili

Di seguito sono riportate le colonne disponibili per ogni rapporto. Le colonne predefinite vengono incluse automaticamente per impostazione predefinita. È possibile aggiungere le colonne personalizzate disponibili dalla sezione [!UICONTROL Columns] delle impostazioni del report.

| Colonna | Predefinito? | Descrizione |
|----|----|----|
| [!UICONTROL Portfolio] | Predefinito | Il portfolio. |
| [!UICONTROL Day of Week] | Predefinito | Giorno della settimana segnalato: <i>[!UICONTROL Sunday]</i>, <i>[!UICONTROL Monday]</i>, <i>[!UICONTROL Tuesday]</i>, <i>[!UICONTROL Wednesday]</i>, <i>[!UICONTROL Thursday]</i>, <i>[!UICONTROL Friday]</i> o <i>[!UICONTROL Saturday]</i>. |
| [!UICONTROL Start Date] | Predefinito | Primo giorno indicato. |
| [!UICONTROL End Date] | Predefinito | Ultimo giorno indicato. |
| [!UICONTROL Predicted Revenue] | Predefinito | Ricavi previsti per il portfolio. |
| [!UICONTROL Revenue] | Predefinito | Ricavi effettivi per il portfolio. |
| [!UICONTROL Revenue Accuracy] | Predefinito | Precisione della previsione dei ricavi, espressa in percentuale. |
| [!UICONTROL Predicted Cost] | Predefinito | Il costo previsto per il portfolio. |
| [!UICONTROL Cost] | Predefinito | Il costo effettivo del portfolio. |
| [!UICONTROL Cost Accuracy] | Predefinito | Precisione della previsione dei costi, espressa in percentuale. |
| [!UICONTROL Predicted Clicks] | Predefinito | Numero di clic previsto per il portfolio. |
| [!UICONTROL Clicks] | Predefinito | Il numero effettivo di clic per il portfolio. |
| [!UICONTROL Click Accuracy] | Predefinito | Precisione della previsione di clic, espressa in percentuale. |
| [!UICONTROL EF Portfolio Group ID] | Predefinito | L’ID numerico del gruppo di portfolio a cui appartiene il portfolio. |
| [!UICONTROL Portfolio Group Name] | Predefinito | Il nome del gruppo di portfolio a cui appartiene il portfolio. |
| [!UICONTROL Portfolio ID] | Predefinito | L’ID numerico del portfolio. |

>[!MORELIKETHIS]
>
>* [Informazioni sui report di precisione del modello](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md)
>* [I [!UICONTROL Forecast Accuracy (Actuals) Report]](forecast-accuracy-actuals-report.md)
>* [Genera un report di precisione modello](model-accuracy-report-generate.md)
>* [Impostazioni report precisione modello](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-settings.md)
