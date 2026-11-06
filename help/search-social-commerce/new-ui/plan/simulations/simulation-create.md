---
title: Eseguire o rieseguire una simulazione personalizzata
description: Scopri come eseguire o eseguire nuovamente una simulazione personalizzata per un portfolio.
feature: Search Optimization, Search Portfolios, Search Simulations
hide: true
exl-id: 0ee62d04-fdc4-445c-90fb-71d5a40a9ed0
TQID: 'https://experienceleague.adobe.com/DlSJEcKXOxVz6UXVpAjQqaiwDTakgJ4SS6rsQUxkQIE'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ae57d55f-b168-5358-b114-c3974b1b3d77
    internal-label: Search Optimization
  - id: 893a7eac-45bd-56c2-a120-18db6d297dcc
    internal-label: Search Portfolios
  - id: 1d0fea65-a874-543d-94c9-b4dbf9e0360a
    internal-label: Search Simulations
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: c2296997-5d79-4905-b32e-99b5aa892429
    internal-label: Search optimization
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: cb2d71e240af5ea1278cb2c00046d80040c914ce
workflow-type: tm+mt
source-wordcount: '530'
ht-degree: 0%
---
# Eseguire o rieseguire una simulazione personalizzata

*funzionalità Beta*

Puoi generare una simulazione personalizzata per un portfolio [ottimizzato o attivo](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md#portfolio-status). È inoltre possibile selezionare una simulazione nell&#39;elenco per eseguire una nuova simulazione per lo stesso portfolio oppure rieseguire le simulazioni con le impostazioni esistenti.

La creazione di una simulazione personalizzata richiede l&#39;autorizzazione [!UICONTROL Create Simulation]. La selezione di un portfolio richiede l&#39;autorizzazione [!UICONTROL View Portfolios].

<!-- You can't run sims for portfolios with legacy keyword-level optimization when they include smart bidding campaigns. Clarify all exceptions so users don't find out via error messages. -->

[!UICONTROL Admin] e [!UICONTROL Account Manager] utenti possono visualizzare le simulazioni create da altri utenti. Tutti gli altri utenti possono visualizzare solo le simulazioni personalizzate create.

## Crea una nuova simulazione {#simulation-create}

È possibile iniziare dalla visualizzazione [!UICONTROL Simulations] o [eseguire una simulazione personalizzata dalla visualizzazione [!UICONTROL Portfolios]](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-create-simulation.md#run-simulation).

1. Nel menu principale, fare clic su **[!UICONTROL Plan]>[!UICONTROL Simulations]**.

1. Cancellare le righe di simulazione selezionate, quindi fare clic su **[!UICONTROL Run Simulation]**.

1. Selezionare il portfolio:

   1. Fare clic su **[!UICONTROL Select Portfolio]**.

   1. Seleziona il portfolio.

      Per cercare i portfolio che includono una stringa di testo specifica, inizia a immettere la stringa di testo all’interno del campo di ricerca. I valori non fanno distinzione tra maiuscole e minuscole.

   1. Fare clic su **[!UICONTROL Proceed]**.

1. Specificare le [impostazioni di simulazione personalizzate](#custom-simulation-settings):

   1. (Facoltativo) Per modificare il portfolio utilizzato per la simulazione, fare clic su **[!UICONTROL Change Portfolio]** accanto al nome del portfolio, selezionare il portfolio e quindi fare clic su **[!UICONTROL Proceed]**.

   1. Nella scheda [!UICONTROL Basic Settings]:

      1. Immettere un **[!UICONTROL Simulation Name]** univoco.

      1. (Facoltativo) Modificate i parametri di base per la simulazione.

   1. (Facoltativo) Nella scheda [!UICONTROL Advanced Settings], modifica i parametri avanzati per la simulazione.

   I parametri esistenti per il portfolio selezionato sono specificati per impostazione predefinita. La modifica dei valori ti mostrerà i risultati che diversi parametri produrrebbero senza modificare i parametri esistenti del portfolio.

1. Fare clic su **[!UICONTROL Next]**.

1. Rivedi le impostazioni e modificale come necessario.

1. Fare clic su **[!UICONTROL Submit & Run]**.

La richiesta viene inviata e viene aperta la visualizzazione [!UICONTROL Simulations]. Quando il rapporto di simulazione è disponibile, tu e qualsiasi altro destinatario e-mail specificato ricevete una notifica con un collegamento per il download. È inoltre possibile [scaricare la simulazione dalla visualizzazione [!UICONTROL Simulations]](simulation-download.md).

<!-- Still true:  When the results for any report type include more than 60,000 rows, the workbook includes multiple worksheets. -->

## Rieseguire una simulazione con le impostazioni esistenti {#rerun-a-simulation-with-the-existing-settings}

Puoi eseguire nuovamente fino a 10 simulazioni alla volta con le impostazioni esistenti. Impossibile rieseguire le simulazioni con stato [!UICONTROL Queued] o [!UICONTROL In Progress]. Se la selezione include queste simulazioni, queste vengono ignorate e le simulazioni rimanenti vengono inviate.

1. Nel menu principale, fare clic su **[!UICONTROL Plan]>[!UICONTROL Simulations]**.

1. Seleziona le caselle di controllo accanto alle simulazioni da eseguire nuovamente.

1. Nella barra degli strumenti sopra la tabella dati o nella barra degli strumenti Azioni collettive, fare clic su **[!UICONTROL Re-Run Simulation]**.

La richiesta viene inviata e la visualizzazione si aggiorna.

## Eseguire una nuova simulazione per un portfolio nell’elenco {#edit-the-settings-for-an-existing-simulation-and-rerun-it}

Se si seleziona una simulazione prima di fare clic su [!UICONTROL Run Simulation], verrà selezionato il portfolio per una nuova simulazione. Il modulo utilizza le impostazioni correnti del portfolio, non le impostazioni della simulazione selezionata. Questa azione non modifica la simulazione esistente.

1. Nel menu principale, fare clic su **[!UICONTROL Plan]>[!UICONTROL Simulations]**.

1. Selezionare la casella di controllo accanto a una simulazione per il portfolio che si desidera utilizzare.

   Se selezioni più simulazioni, tutte devono utilizzare lo stesso portfolio. Il portfolio deve essere attivo o ottimizzato.

1. Sopra la tabella dati, fare clic su **[!UICONTROL Run Simulation]**.

1. Specificare le [impostazioni di simulazione personalizzate](#custom-simulation-settings), incluso un **[!UICONTROL Simulation Name]** univoco. Modificare i parametri nelle schede **[!UICONTROL Basic Settings]** e **[!UICONTROL Advanced Settings]** in base alle esigenze.

1. Fare clic su **[!UICONTROL Next]**.

1. Rivedi le impostazioni e modificale come necessario.

1. Fare clic su **[!UICONTROL Submit & Run]**.

La richiesta viene inviata e viene aperta la visualizzazione [!UICONTROL Simulations]. È possibile [scaricare la simulazione](simulation-download.md) dopo averla completata correttamente.

## Impostazioni di simulazione personalizzate {#custom-simulation-settings}

Per ulteriori informazioni sulle impostazioni di simulazione personalizzate, consulta la Guida all’ottimizzazione, disponibile in Search, Social e Commerce.

>[!MORELIKETHIS]
>
>* [Informazioni sulle simulazioni](simulation-about.md)
>* [Visualizza dettagli simulazione](simulation-view.md)
>* [Scarica simulazioni](simulation-download.md)
