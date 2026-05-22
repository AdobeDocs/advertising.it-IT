---
title: Gestire i rapporti pianificati
description: Scopri come gestire i rapporti pianificati.
feature: Search Reports, Search Basic Reports, Search Advanced Reports, Search Assist Reports, Search Model Accuracy Reports, Search Specialty Reports
source-git-commit: bfca434eacf52ec7236804c54b7740442aa12961
workflow-type: tm+mt
source-wordcount: '1571'
ht-degree: 0%

---

# Gestire i rapporti pianificati

I rapporti sulle prestazioni consentono di tenere traccia e gestire le prestazioni di portfolio, reti di annunci ed entità account di rete di annunci con la granularità desiderata. La maggior parte dei rapporti fornisce una visibilità completa sul modo in cui gli annunci in ciascun canale di marketing contribuiscono al tasso di conversione complessivo.

I dati di un report vengono compilati in modo dinamico ogni volta che si esegue il report. Facoltativamente, è possibile generare un nuovo rapporto da un rapporto esistente. I parametri del rapporto disponibili variano in base al tipo di rapporto. Per la maggior parte dei rapporti, è possibile visualizzare in anteprima le prime 50 righe invece di generare l’intero rapporto. Quando si genera un report, è possibile inviare una notifica con collegamenti di download a uno o più indirizzi di posta elettronica quando un report viene completato e i destinatari possono [gestire le notifiche in [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

Tutti i report completati sono disponibili nella sezione [!UICONTROL Latest Reports] della visualizzazione [!UICONTROL Reports] ed è possibile visualizzarli in formato tabella nella finestra del browser oppure aprirli o scaricarli come file.

## Categorie di rapporti disponibili

Le seguenti categorie di report sono disponibili dalla visualizzazione [!UICONTROL Reports]. Potresti non avere accesso a tutti; i rapporti disponibili e i dati che generano sono determinati dal tuo ruolo e dalla configurazione del tuo account cliente.

| Categoria rapporto | Descrizione |
| ----| ---- |
| [!UICONTROL Basic Reports] | [Report di base](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-about.md), disponibili per tutti gli utenti, mostrano il costo effettivo e i dati di clic per portfolio, account di rete di annunci, account di rete di annunci specifici, campagne, gruppi di annunci, annunci, parole chiave, gruppi di prodotti, classificazioni di etichette e valori di etichette, vincoli di unità di offerta e vincoli di rete. Si basano sui clic fatturati dalle reti di annunci applicabili e, facoltativamente, possono includere dati di conversione o altre metriche create. |
| [!UICONTROL Advanced Reports] | I [report avanzati](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-about.md) forniscono ulteriore insight nella configurazione pubblicitaria, aiutandoti a identificare i vantaggi della modifica del targeting geografico o delle impostazioni di rete. Possono anche aiutarti a convalidare i dati di conversione nelle viste e nei rapporti di gestione della campagna e del portfolio in base ai dati di tracciamento delle conversioni interne dell’inserzionista. |
| [!UICONTROL Assist Reports] | [I report di assistenza](/help/search-social-commerce/new-ui/reports/management/assist/assist-report-about.md) forniscono informazioni approfondite sui percorsi di conversione per tutte le parole chiave e gli annunci di un inserzionista. Utilizzano dati acquisiti tramite il servizio di tracciamento delle conversioni di Adobe Advertising e possono essere generati solo per gli inserzionisti che utilizzano tale servizio. |
| [!UICONTROL Specialty Reports] | [I report speciali](/help/search-social-commerce/new-ui/reports/management/specialty/specialty-report-about.md) sono costituiti da dati raccolti dalle reti di annunci (anziché dal tracciamento di Adobe Advertising). |
| [!UICONTROL Model Accuracy Reports] | [I rapporti sulla precisione del modello](/help/search-social-commerce/new-ui/reports/management/model-accuracy/model-accuracy-report-about.md) indicano la precisione dei modelli di costi e ricavi utilizzati per ottimizzare le offerte, il budget delle campagne e gli obiettivi di strategia delle offerte per un portfolio. |

## Automazione dei rapporti

Pianifica la generazione automatica dei rapporti personalizzati in uno o entrambi i seguenti modi:

* Genera automaticamente report ogni giorno oppure in un giorno specifico della settimana o del mese, utilizzando [modelli di report](/help/search-social-commerce/reports/automation/templates/template-about.md).

  Facoltativamente puoi impostare [la consegna FTP di rapporti di base e avanzati](/help/search-social-commerce/new-ui/reports/ftp-reports.md) che utilizzano un modello.

* Continua ad aggiornare i tuoi modelli di foglio di calcolo personalizzati con i dati sulle prestazioni giornaliere utilizzando [feed di foglio di calcolo](/help/search-social-commerce/new-ui/reports/spreadsheet-feeds-manage.md).

## Le visualizzazioni [!UICONTROL Scheduled Reports]

Le viste [!UICONTROL Reports] > [!UICONTROL Scheduled Reports] ti consentono di creare e gestire report e modelli di report:

* Nella scheda **[!UICONTROL Latest Reports]** sono elencati tutti i report disponibili<!-- Doesn't seem to be true: that were requested in the last seven days -->, ad eccezione di quelli eliminati manualmente, con il report più recente nella parte superiore per impostazione predefinita. Le informazioni visualizzate per ogni report includono la pianificazione in base alla quale viene eseguito (se applicabile), le date di inizio e fine per le quali sono stati o verranno generati i dati, chi ha creato il report e lo stato del report (*[!UICONTROL Finished]*, *[!UICONTROL In Progress]* o *[!UICONTROL Error]*).

  I collegamenti accanto a ciascun rapporto consentono di aprire o salvare il rapporto come cartella di lavoro [!DNL Microsoft Excel] (XLS), file con valori separati da tabulazioni (TSV) o file con valori separati da virgole (CSV). Alcuni tipi di report possono essere salvati anche come [!UICONTROL Excel] cartelle di lavoro con un foglio di lavoro separato per ogni campagna applicabile.

  Da questa scheda è inoltre possibile creare un nuovo report (che può essere utilizzato facoltativamente come modello), creare un nuovo report basato sulle impostazioni di un report esistente o utilizzando un modello di report, annullare i report in corso disponibili eliminandoli ed eliminare tutti i report completati disponibili.

* Nella scheda **[!UICONTROL Templates]** sono elencati tutti i modelli di report di base e avanzati salvati disponibili, incluse le informazioni sulle pianificazioni associate. Per impostazione predefinita, il modello più recente si trova nella parte superiore.

  Da questa scheda è possibile creare un nuovo modello, modificare qualsiasi modello creato, ad esempio aggiungendo, modificando o rimuovendo la pianificazione, generare un report da un modello ed eliminare qualsiasi modello disponibile.

## Come utilizzare i rapporti

| Finalità | Report |
| ---- | ---- |
| Monitoraggio delle prestazioni | <ul><li>[I [!UICONTROL Portfolio Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/portfolio-report.md)</li><li>[I [!UICONTROL Search Engine Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/search-engine-report.md)</li><li>[I [!UICONTROL Search Engine Account Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/search-engine-account-report.md)</li><li>[I [!UICONTROL Campaign Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/campaign-report.md)</li><li>[I [!UICONTROL Ad Group Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/ad-group-report.md)</li><li>[I [!UICONTROL Forecast Accuracy Report]](/help/search-social-commerce/new-ui/reports/management/model-accuracy/forecast-accuracy-report.md)</li></ul> |
| Risoluzione dei problemi relativi alle prestazioni e analisi delle tendenze | <ul><li>[I [!UICONTROL Keyword Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/keyword-report.md)</li><li>[I [!UICONTROL Ad Variation Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/ad-variation-report.md)</li><li>[I [!UICONTROL Transaction Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/transaction-report.md)</li><li>[I [!UICONTROL RSA Asset Report]](/help/search-social-commerce/new-ui/reports/management/specialty/rsa-asset-report.md)</li><li>[I [!UICONTROL Keyword Daily Impression Share Report]](/help/search-social-commerce/new-ui/reports/management/specialty/keyword-daily-impression-share-report.md) e [I [!UICONTROL Campaign Daily Impression Share Report]](/help/search-social-commerce/new-ui/reports/management/specialty/campaign-daily-impression-share-report.md)</li><li>Qualsiasi report di base che confronta due finestre temporali utilizzando la funzionalità &quot;[!UICONTROL Compare with]&quot;</li></ul> |
| Identificazione delle opportunità di crescita del business | <ul><li>(Solo per gli inserzionisti con tracciamento delle conversioni di Adobe Advertising) [The [!UICONTROL Geo Distribution Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/geo-distribution-report.md)</li><li>(Solo per gli inserzionisti con tracciamento delle conversioni di Adobe Advertising) [The [!UICONTROL Domain Referral Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/domain-referral-report.md)</li><li>(Inserzionisti con [Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html?lang=it)) Rapporti personalizzati in Adobe Analytics Analysis Workspace</li></ul> |
| Analytics | <ul><li>(Solo per gli inserzionisti con tracciamento delle conversioni di Adobe Advertising) [The [!UICONTROL Channel Assist Report]](/help/search-social-commerce/new-ui/reports/management/assist/channel-assist-report.md)</li><li>(Inserzionisti con [Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html?lang=it)) Rapporti personalizzati in Adobe Analytics Analysis Workspace</li></ul> |

## Generare rapporti

### Generare un nuovo rapporto

1. Nel menu principale, fare clic su **[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]**.

1. Fare clic su **[!UICONTROL Create Report]**, fare clic sulla categoria del report nel pannello a sinistra, quindi selezionare il tipo di report.<!-- Add link to list of report categories and report types --> Fare clic su **[!UICONTROL Proceed]**.

1. (Facoltativo) Nella finestra [!UICONTROL Create Report], modifica le impostazioni predefinite del rapporto per [rapporti di base e avanzati](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-settings.md), [rapporti assistenza](/help/search-social-commerce/new-ui/reports/management/assist/assist-report-settings.md), [rapporti accuratezza modello](/help/search-social-commerce/new-ui/reports/management/model-accuracy/model-accuracy-report-settings.md) e [rapporti speciali](/help/search-social-commerce/new-ui/reports/management/specialty/specialty-report-settings.md):

   1. (Facoltativo) Inserire un nome personalizzato per il rapporto e per il modello (se si salva il rapporto come modello).

   1. (Facoltativo) Per salvare le impostazioni del report come modello, abilitare l&#39;impostazione **[!UICONTROL Save as template]**.

   1. (Facoltativo) Selezionare un report diverso **[!UICONTROL Type]** nella stessa categoria di report.

   1. (Facoltativo) Nella scheda **[!UICONTROL Basic Settings]**, selezionare un modello di report esistente da utilizzare o modificare le impostazioni di base predefinite per il report.

   1. (Facoltativo) Fare clic sulla scheda **[!UICONTROL Columns]** e modificare le colonne predefinite nel report, incluso l&#39;ordine delle colonne.

      Per impostazione predefinita, tutti i dati monetari nei rapporti vengono visualizzati nel formato del dollaro statunitense (ad esempio 1.000,00). Per visualizzare il valore nel formato di valuta corretto (ma senza simboli di valuta nei formati CSV e TSV), aggiungere la colonna &quot;[!UICONTROL Currency]&quot; al rapporto. Se il report include dati per conti con valute diverse, tutti i valori monetari &quot;[!UICONTROL Total]&quot; sono la somma di tutti i numeri nella colonna, indipendentemente dalla valuta.

   1. (Alcuni tipi di report, facoltativo) Fare clic sulla scheda **[!UICONTROL Filters & Attribution]** o **[!UICONTROL Filters]** e aggiungere filtri dati, (alcuni tipi di report) limitare i risultati del report in modo da includere solo classificazioni di etichette specifiche e modificare le impostazioni di attribuzione di conversione e regola di attribuzione di attribuzione predefinite.

   1. (Facoltativo) Fare clic sulla scheda **[!UICONTROL Scheduling]** e modificare le opzioni di pianificazione e consegna predefinite.

1. Fare clic su **[!UICONTROL Create]**.

Se non è stata specificata una pianificazione, il report viene eseguito immediatamente; in caso contrario, viene eseguito in base alla pianificazione specificata. Il nome del report viene aggiunto alla visualizzazione [[!UICONTROL Latest Reports]](/help/search-social-commerce/reports/report-about.md). Se il report è stato salvato come modello, verrà aggiunto anche alla visualizzazione [[!UICONTROL Templates]](/help/search-social-commerce/reports/report-about.md). Una volta completato il report, il file è disponibile per l&#39;apertura o il salvataggio; i modelli sono disponibili immediatamente.

Se hai immesso indirizzi e-mail per la notifica, ogni destinatario riceve una notifica quando il processo di report viene completato o non riesce, in base alle [impostazioni di notifica configurate](/help/search-social-commerce/notifications/notification-edit.md) dell&#39;utente per i report.

### Generare un rapporto da un rapporto esistente

1. Nel menu principale, fare clic su **[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]**, che apre alla scheda **[!UICONTROL Latest Reports]**.

1. Effettuare una delle seguenti operazioni:

   * Posizionare il cursore sulla riga del report e fare clic su **...** > **[!UICONTROL Duplicate]**.

   * Seleziona la casella di controllo accanto al rapporto. Nella barra degli strumenti Azioni in blocco, fare clic su [Duplica](/help/search-social-commerce/assets/duplicate.png "Duplica").

1. Se necessario, modifica le impostazioni del rapporto.

1. Fare clic su **[!UICONTROL Create]**.

### Generare un report da un modello esistente

1. Nel menu principale, fare clic su **[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]**.

1. Fare clic sulla scheda **[!UICONTROL Templates]**.

1. Effettuare una delle seguenti operazioni:

   * Posizionare il cursore sulla riga del modello e fare clic su **...** > **[!UICONTROL Duplicate]**.

   * Selezionare la casella di controllo accanto al modello esistente. Nella barra degli strumenti Azioni in blocco, fare clic su [Duplica](/help/search-social-commerce/assets/duplicate.png) **[!UICONTROL Duplicate]**.

1. (Facoltativo) Rinomina il modello e, se necessario, modifica le impostazioni del rapporto.

   Fare clic su **[!UICONTROL Next]** per spostarsi tra le sezioni di impostazione.

1. Abilita l&#39;impostazione **[!UICONTROL Save as Template]**.

1. Fare clic su **[!UICONTROL Create]**.

## Visualizzare l’anteprima o salvare un rapporto

È possibile visualizzare l&#39;anteprima di un report nel browser Web oppure aprire o salvare i dati del report come cartella di lavoro [!DNL Microsoft Excel], file TSV, file CSV o, in alcuni casi, cartella di lavoro con schede [!DNL Microsoft Excel].

>[!NOTE]
>
>I membri del Adobe Account Team e alcuni utenti amministratori possono visualizzare i report creati dagli utenti inserzionisti e agenzie.

1. Nel menu principale, fare clic su **[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]**, che apre alla scheda **[!UICONTROL Latest Reports]**.

1. Effettuare una delle seguenti operazioni:

   * Per visualizzare un report nel browser Web, effettuare una delle seguenti operazioni:

      * Posizionare il cursore sulla riga del modello e fare clic su **...** > **[!UICONTROL Preview]**.

      * Selezionare la casella di controllo accanto al modello esistente. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL Preview]**.

   * (Per aprire o salvare i dati del report in un file) Nella colonna [!UICONTROL Export] accanto al nome del report, fare clic sul nome di un formato, quindi aprire o salvare il file in base alla normale procedura del browser:

      * **[!UICONTROL XLS]:** per una cartella di lavoro [!DNL Excel] con un singolo foglio di lavoro (formato XLSX). Il rapporto include un foglio di lavoro etichettato nella parte superiore con i parametri, con una riga per ciascun componente segnalata quando i dati per il componente sono disponibili. Le righe senza dati vengono omesse.

        I rapporti di base includono un totale per ogni colonna numerica.

      * **[!UICONTROL TSV]:** per un file TSV. Il rapporto include i parametri e una riga per ciascun componente indicato.

      * **[!UICONTROL CSV]:** per un file CSV. Il rapporto include i parametri e una riga per ciascun componente indicato.

## Eliminare i rapporti

1. Nel menu principale, fare clic su **[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]**, che apre alla scheda **[!UICONTROL Latest Reports]**.

1. Effettuare una delle seguenti operazioni:

   * Per eliminare un singolo report:

      1. Posizionare il cursore sulla riga del report e fare clic su **...** > **[!UICONTROL Run]**.

      1. Nel messaggio di conferma, fare clic su **[!UICONTROL Confirm]**.

   * Per eliminare uno o più rapporti:

      1. Selezionare la casella di controllo accanto a ogni report che si desidera eliminare.

      1. Nella barra degli strumenti Azioni in blocco, fare clic su [Elimina](/help/search-social-commerce/assets/delete-new.png "Elimina") **[!UICONTROL Delete]**.

      1. Nel messaggio di conferma, fare clic su **[!UICONTROL Confirm]**.

<!--

>[!MORELIKETHIS]
>
>* [About basic and advanced reports](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-about.md)
>* [Basic and advanced report settings](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-settings.md)
>* [Report columns for basic and advanced reports](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-columns.md)

-->
