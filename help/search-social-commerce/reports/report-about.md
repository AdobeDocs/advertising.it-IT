---
title: Informazioni sui report
description: Scopri i rapporti sulle prestazioni, compresi i diversi tipi di rapporti disponibili e come automatizzare i rapporti.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '853'
ht-degree: 0%

---

# Informazioni sui report

I rapporti sulle prestazioni consentono di tenere traccia e gestire le prestazioni di portfolio, reti di annunci ed entità account di rete di annunci con la granularità desiderata. La maggior parte dei rapporti fornisce una visibilità completa sul modo in cui gli annunci in ciascun canale di marketing contribuiscono al tasso di conversione complessivo.

I dati di un report vengono compilati in modo dinamico ogni volta che si esegue il report. Facoltativamente, è possibile generare un nuovo rapporto da un rapporto esistente. I parametri del rapporto disponibili variano in base al tipo di rapporto. Per la maggior parte dei rapporti, è possibile visualizzare in anteprima le prime 50 righe invece di generare l’intero rapporto. Quando generi un rapporto, puoi inviare una notifica con collegamenti di download a uno o più indirizzi e-mail al termine di un rapporto, in modo che i destinatari possano [gestire le notifiche in [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

Tutti i report completati sono disponibili nel [!UICONTROL Latest Reports] sezione del [!UICONTROL Reports] ed è possibile visualizzarli in formato tabella nella finestra del browser oppure aprirli o scaricarli come file.

## Categorie di rapporti disponibili

Le seguenti categorie di rapporti sono disponibili dal [!UICONTROL Reports] visualizzazione. Potresti non avere accesso a tutti; i rapporti disponibili e i dati che generano sono determinati dal tuo ruolo e dalla configurazione del tuo account cliente.

| Categoria rapporto | Descrizione |
| ----| ---- |
| [!UICONTROL Basic Reports] | [Rapporti di base](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md), disponibili per tutti gli utenti, mostrano il costo effettivo e i dati di clic per portfolio, account di rete di annunci, account di rete di annunci specifici, campagne, gruppi di annunci, annunci, parole chiave, gruppi di prodotti, classificazioni di etichette e valori di etichette, vincoli di unità di offerta e vincoli di rete. Si basano sui clic fatturati dalle reti di annunci applicabili e, facoltativamente, possono includere dati di conversione o altre metriche create. |
| [!UICONTROL Advanced Reports] | [Rapporti avanzati](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md) fornisci informazioni aggiuntive sulla configurazione dei messaggi pubblicitari, per aiutarti a identificare i vantaggi che trarresti dalla modifica del targeting geografico o delle impostazioni di rete. Possono anche aiutarti a convalidare i dati di conversione nelle viste e nei rapporti di gestione della campagna e del portfolio in base ai dati di tracciamento delle conversioni interne dell’inserzionista. |
| [!UICONTROL Assist Reports] | [Rapporti di assistenza](/help/search-social-commerce/reports/management/assist/assist-report-about.md) fornisce informazioni sui percorsi di conversione per tutte le parole chiave e gli annunci di un inserzionista. Utilizzano dati acquisiti tramite il servizio di tracciamento delle conversioni di Adobe Advertising e possono essere generati solo per gli inserzionisti che utilizzano il servizio. |
| [!UICONTROL Specialty Reports] | [Rapporti speciali](/help/search-social-commerce/reports/management/specialty/specialty-report-about.md) sono dati raccolti dalle reti di annunci (anziché dal tracciamento di Adobe Advertising). |
| [!UICONTROL Model Accuracy Reports] | [Report di precisione modello](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md) indica l’accuratezza dei modelli di costi e ricavi utilizzati per ottimizzare le offerte. |

## Automazione dei rapporti

Pianifica la generazione automatica dei rapporti personalizzati in uno o entrambi i seguenti modi:

* Genera automaticamente rapporti ogni giorno, o in un giorno specifico della settimana o del mese, utilizzando [modelli di rapporto](/help/search-social-commerce/reports/automation/templates/template-about.md).

   Facoltativamente, puoi impostare [Distribuzione FTP di rapporti di base e avanzati](/help/search-social-commerce/reports/automation/ftp-reports.md) che utilizzano un modello.

* Aggiornamento continuo dei modelli di foglio di calcolo personalizzati con dati sulle prestazioni giornaliere tramite [feed di fogli di calcolo](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md).

## Visualizzazioni dei report

Il [!UICONTROL Reports] visualizzazioni a [!UICONTROL Search] > [!UICONTROL Insights & Reports] > [!UICONTROL Reports] consente di creare e gestire rapporti, modelli e feed di fogli di calcolo. La vista include due schede:

* Il **[!UICONTROL Latest Reports]** La scheda elenca tutti i rapporti disponibili che sono stati richiesti negli ultimi sette giorni, ad eccezione di quelli eliminati manualmente, con il rapporto più recente nella parte superiore per impostazione predefinita. Le informazioni visualizzate per ciascun rapporto includono la pianificazione in base alla quale viene eseguito (se applicabile), le date di inizio e di fine per le quali i dati sono stati o saranno generati e lo stato del rapporto (*[!UICONTROL Finished]*, *[!UICONTROL In Progress]*, o *[!UICONTROL Error]*).

   I collegamenti accanto a ciascun rapporto consentono di visualizzarlo nel browser oppure di aprirlo o salvarlo come [!DNL Microsoft Excel] file della cartella di lavoro (XLS) o valori separati da tabulazioni (TSV); alcuni tipi di rapporto possono anche essere salvati come [!UICONTROL Excel] cartelle di lavoro con un foglio di lavoro separato per ogni campagna applicabile.

   Da questa scheda è inoltre possibile creare un nuovo report (che può essere utilizzato facoltativamente come modello), creare un nuovo report basato sulle impostazioni per un report esistente, annullare i report in corso disponibili eliminandoli ed eliminare tutti i report completati disponibili. I rapporti più vecchi di sette giorni vengono eliminati automaticamente.

* Il **[!UICONTROL Templates]** La scheda elenca tutti i modelli di report di base e avanzati salvati disponibili, incluse le informazioni su eventuali pianificazioni associate. Per impostazione predefinita, il modello più recente si trova nella parte superiore.

   Da questa scheda è possibile creare un nuovo modello, modificare qualsiasi modello creato, ad esempio aggiungendo, modificando o rimuovendo la pianificazione, generare un report da un modello ed eliminare qualsiasi modello disponibile.

## Come utilizzare i rapporti

| Finalità | Report |
| ---- | ---- |
| Monitoraggio delle prestazioni | <ul><li>[Il [!UICONTROL Portfolio Report]](/help/search-social-commerce/reports/management/basic-advanced/portfolio-report.md)</li><li>[Il [!UICONTROL Search Engine Report]](/help/search-social-commerce/reports/management/basic-advanced/search-engine-report.md)</li><li>[Il [!UICONTROL Search Engine Account Report]](/help/search-social-commerce/reports/management/basic-advanced/search-engine-account-report.md)</li><li>[Il [!UICONTROL Campaign Report]](/help/search-social-commerce/reports/management/basic-advanced/campaign-report.md)</li><li>[Il [!UICONTROL Ad Group Report]](/help/search-social-commerce/reports/management/basic-advanced/ad-group-report.md)</li><li>[Il [!UICONTROL Forecast Accuracy Report]](/help/search-social-commerce/reports/management/model-accuracy/forecast-accuracy-report.md)</li></ul> |
| Risoluzione dei problemi relativi alle prestazioni e analisi delle tendenze | <ul><li>[Il [!UICONTROL Keyword Report]](/help/search-social-commerce/reports/management/basic-advanced/keyword-report.md)</li><li>[Il [!UICONTROL Ad Variation Report]](/help/search-social-commerce/reports/management/basic-advanced/ad-variation-report.md)</li><li>[Il [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md)</li><li>[Il [!UICONTROL RSA Asset Report]](/help/search-social-commerce/reports/management/specialty/rsa-asset-report.md)</li><li>[Il [!UICONTROL Keyword Daily Impression Share Report]](/help/search-social-commerce/reports/management/specialty/keyword-daily-impression-share-report.md) e [Il [!UICONTROL Campaign Daily Impression Share Report]](/help/search-social-commerce/reports/management/specialty/campaign-daily-impression-share-report.md)</li><li>Qualsiasi report di base che confronta due finestre temporali utilizzando il tasto &quot;[!UICONTROL Compare with]&quot; funzione</li></ul> |
| Identificazione delle opportunità di crescita del business | <ul><li>(Solo per gli inserzionisti con Adobe Advertising conversion tracking) [Il [!UICONTROL Geo Distribution Report]](/help/search-social-commerce/reports/management/basic-advanced/geo-distribution-report.md)</li><li>(Solo per gli inserzionisti con Adobe Advertising conversion tracking) [Il [!UICONTROL Domain Referral Report]](/help/search-social-commerce/reports/management/basic-advanced/domain-referral-report.md)</li><li>(Per gli inserzionisti che [Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)) Rapporti personalizzati in Adobe Analytics Analysis Workspace</li></ul> |
| Analytics | <ul><li>(Solo per gli inserzionisti con Adobe Advertising conversion tracking) [Il [!UICONTROL Channel Assist Report]](/help/search-social-commerce/reports/management/assist/channel-assist-report.md)</li><li>(Per gli inserzionisti che [Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)) Rapporti personalizzati in Adobe Analytics Analysis Workspace</li></ul> |

>[!MORELIKETHIS]
>
>* [Dati utilizzati per i rapporti](data-used-for-reports.md)
>* [Attività di configurazione iniziali per i rapporti](initial-setup.md)
>* [Generare un rapporto di base o avanzato](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md)
>* [Generare un report di precisione del modello](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-generate.md)
>* [Generare un rapporto speciale](/help/search-social-commerce/reports/management/specialty/specialty-report-generate.md)
>* [Generare un rapporto di assistenza](/help/search-social-commerce/reports/management/assist/assist-report-generate.md)

