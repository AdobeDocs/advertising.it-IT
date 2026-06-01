---
title: (Nuova interfaccia) Informazioni sui rapporti pianificati
description: Scopri i rapporti sulle prestazioni pianificati, compresi i diversi tipi di rapporti disponibili e come automatizzare i rapporti.
feature: Search Reports
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2:
  - id: e246c273-d720-4ece-b29b-7aaba7d50169
  - id: c916feea-e212-4773-b673-4daed287b8a3
  - id: adcb1be7-7ed0-464d-a8d4-c905c9d47742
  - id: ff99aaef-142d-4c93-a88c-011e979e3843
  - id: fa0141e5-dc99-4fbd-9c0e-40aff66de606
  - id: b36a77b1-3c8f-4e1c-8b0b-6e0ba3fb2664
source-git-commit: bd4246ec79684167254a153d2f3d0b917a493096
workflow-type: tm+mt
source-wordcount: 857
ht-degree: 0%

---

# (Nuova interfaccia) Informazioni sui rapporti pianificati

I rapporti sulle prestazioni pianificati consentono di tenere traccia e gestire le prestazioni di portfolio, reti di annunci ed entità account di rete di annunci a un livello di granularità ottimale. La maggior parte dei rapporti fornisce una visibilità completa sul modo in cui gli annunci in ciascun canale di marketing contribuiscono al tasso di conversione complessivo.

I dati di un report vengono compilati in modo dinamico ogni volta che si esegue il report. Facoltativamente, è possibile generare un nuovo rapporto da un rapporto esistente. I parametri del rapporto disponibili variano in base al tipo di rapporto. Per la maggior parte dei rapporti, è possibile visualizzare in anteprima le prime 50 righe invece di generare l’intero rapporto. Quando si genera un report, è possibile inviare una notifica con collegamenti di download a uno o più indirizzi di posta elettronica quando un report viene completato e i destinatari possono [gestire le notifiche in [!UICONTROL Notification Center]](/help/search-social-commerce/new-ui/notifications-manage.md).

Tutti i report completati sono disponibili nella sezione [!UICONTROL Latest Reports] della visualizzazione [!UICONTROL Reports] ed è possibile visualizzarli in formato tabella nella finestra del browser oppure aprirli o scaricarli come file.

## Categorie di rapporti disponibili

Le seguenti categorie di report sono disponibili dalla visualizzazione [!UICONTROL Scheduled Reports]. Potresti non avere accesso a tutti; i rapporti disponibili e i dati che generano sono determinati dal tuo ruolo e dalla configurazione del tuo account cliente.

| Categoria rapporto | Descrizione |
| ----| ---- |
| [!UICONTROL Basic Reports] | [Report di base](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-about.md), disponibili per tutti gli utenti, mostrano il costo effettivo e i dati di clic per portfolio, account di rete di annunci, account di rete di annunci specifici, campagne, gruppi di annunci, annunci, parole chiave, gruppi di prodotti, classificazioni di etichette e valori di etichette, vincoli di unità di offerta e vincoli di rete. Si basano sui clic fatturati dalle reti di annunci applicabili e, facoltativamente, possono includere dati di conversione o altre metriche create. |
| [!UICONTROL Advanced Reports] | I [report avanzati](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-about.md) forniscono ulteriore insight nella configurazione pubblicitaria, aiutandoti a identificare i vantaggi della modifica del targeting geografico o delle impostazioni di rete. Possono anche aiutarti a convalidare i dati di conversione nelle viste e nei rapporti di gestione della campagna e del portfolio in base ai dati di tracciamento delle conversioni interne dell’inserzionista. |
| [!UICONTROL Assist Reports] | [I report di assistenza](/help/search-social-commerce/new-ui/reports/management/assist/assist-report-about.md) forniscono informazioni approfondite sui percorsi di conversione per tutte le parole chiave e gli annunci di un inserzionista. Utilizzano dati acquisiti tramite il servizio di tracciamento delle conversioni di Adobe Advertising e possono essere generati solo per gli inserzionisti che utilizzano tale servizio. |
| [!UICONTROL Specialty Reports] | [I report speciali](/help/search-social-commerce/new-ui/reports/management/specialty/specialty-report-about.md) sono costituiti da dati raccolti dalle reti di annunci (anziché dal tracciamento di Adobe Advertising). |
| [!UICONTROL Model Accuracy Reports] | [I rapporti sulla precisione del modello](/help/search-social-commerce/new-ui/reports/management/model-accuracy/model-accuracy-report-about.md) indicano la precisione dei modelli di costi e ricavi utilizzati per ottimizzare le offerte, il budget delle campagne e gli obiettivi di strategia delle offerte per un portfolio. |

## Automazione dei rapporti

Pianifica la generazione automatica dei rapporti personalizzati in uno o entrambi i seguenti modi:

* Genera automaticamente report ogni giorno oppure in un giorno specifico della settimana o del mese, utilizzando [modelli di report](/help/search-social-commerce/new-ui/reports/report-templates-manage.md).

  Facoltativamente puoi impostare [la consegna FTP di rapporti di base e avanzati](/help/search-social-commerce/new-ui/reports/ftp-reports.md) che utilizzano un modello.

* Continua ad aggiornare i tuoi modelli di foglio di calcolo personalizzati con i dati sulle prestazioni giornaliere utilizzando [feed di foglio di calcolo](/help/search-social-commerce/new-ui/reports/spreadsheet-feeds-manage.md).

## Visualizzazione [!UICONTROL Scheduled Reports]

La visualizzazione [!UICONTROL Reports] > [!UICONTROL Scheduled Reports] consente di creare e gestire report, modelli e feed di fogli di calcolo. La vista include due schede:

* La scheda **[!UICONTROL Latest Reports]** elenca tutti i report disponibili che sono stati richiesti negli ultimi sette giorni, ad eccezione di quelli eliminati manualmente, con il report più recente nella parte superiore per impostazione predefinita. Le informazioni visualizzate per ogni report includono la pianificazione in base alla quale viene eseguito (se applicabile), le date di inizio e fine per le quali i dati sono stati o saranno generati e lo stato del report (*[!UICONTROL Finished]*, *[!UICONTROL In Progress]* o *[!UICONTROL Error]*).

  I collegamenti accanto a ogni rapporto consentono di visualizzare il rapporto nel browser Web oppure di aprirlo o salvarlo come file di cartella di lavoro [!DNL Microsoft Excel] (XLS) o TSV (valori separati da tabulazioni). Alcuni tipi di rapporto possono essere salvati anche come [!UICONTROL Excel] cartelle di lavoro con un foglio di lavoro separato per ogni campagna applicabile.

  Da questa scheda è inoltre possibile creare un nuovo report (che può essere utilizzato facoltativamente come modello), creare un nuovo report basato sulle impostazioni per un report esistente, annullare i report in corso disponibili eliminandoli ed eliminare tutti i report completati disponibili. I rapporti più vecchi di sette giorni vengono eliminati automaticamente.

* Nella scheda **[!UICONTROL Templates]** sono elencati tutti i modelli di report di base e avanzati salvati disponibili, incluse le informazioni sulle pianificazioni associate. Per impostazione predefinita, il modello più recente si trova nella parte superiore.

  Da questa scheda è possibile creare un nuovo modello, modificare qualsiasi modello creato, ad esempio aggiungendo, modificando o rimuovendo la pianificazione, generare un report da un modello ed eliminare qualsiasi modello disponibile.

## Come utilizzare i rapporti

| Finalità | Report |
| ---- | ---- |
| Monitoraggio delle prestazioni | <ul><li>[I [!UICONTROL Portfolio Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/portfolio-report.md)</li><li>[I [!UICONTROL Search Engine Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/search-engine-report.md)</li><li>[I [!UICONTROL Search Engine Account Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/search-engine-account-report.md)</li><li>[I [!UICONTROL Campaign Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/campaign-report.md)</li><li>[I [!UICONTROL Ad Group Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/ad-group-report.md)</li><li>[I [!UICONTROL Forecast Accuracy Report]](/help/search-social-commerce/new-ui/reports/management/model-accuracy/forecast-accuracy-report.md)</li></ul> |
| Risoluzione dei problemi relativi alle prestazioni e analisi delle tendenze | <ul><li>[I [!UICONTROL Keyword Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/keyword-report.md)</li><li>[I [!UICONTROL Ad Variation Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/ad-variation-report.md)</li><li>[I [!UICONTROL Transaction Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/transaction-report.md)</li><li>[I [!UICONTROL RSA Asset Report]](/help/search-social-commerce/new-ui/reports/management/specialty/rsa-asset-report.md)</li><li>[I [!UICONTROL Keyword Daily Impression Share Report]](/help/search-social-commerce/new-ui/reports/management/specialty/keyword-daily-impression-share-report.md) e [I [!UICONTROL Campaign Daily Impression Share Report]](/help/search-social-commerce/new-ui/reports/management/specialty/campaign-daily-impression-share-report.md)</li><li>Qualsiasi report di base che confronta due finestre temporali utilizzando la funzionalità &quot;[!UICONTROL Compare with]&quot;</li></ul> |
| Identificazione delle opportunità di crescita del business | <ul><li>(Solo per gli inserzionisti con tracciamento delle conversioni di Adobe Advertising) [The [!UICONTROL Geo Distribution Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/geo-distribution-report.md)</li><li>(Solo per gli inserzionisti con tracciamento delle conversioni di Adobe Advertising) [The [!UICONTROL Domain Referral Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/domain-referral-report.md)</li><li>(Inserzionisti con [Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)) Rapporti personalizzati in Adobe Analytics Analysis Workspace</li></ul> |
| Analytics | <ul><li>(Solo per gli inserzionisti con tracciamento delle conversioni di Adobe Advertising) [The [!UICONTROL Channel Assist Report]](/help/search-social-commerce/new-ui/reports/management/assist/channel-assist-report.md)</li><li>(Inserzionisti con [Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)) Rapporti personalizzati in Adobe Analytics Analysis Workspace</li></ul> |

>[!MORELIKETHIS]
>
>* [Attività di installazione iniziali per i report](initial-setup.md)
>* [Dati utilizzati per i report](data-used-for-reports.md)
>* [Gestisci report pianificati](/help/search-social-commerce/new-ui/reports/management/report-manage.md)
