---
title: Eseguire e scaricare simulazioni dalla visualizzazione [!UICONTROL Portfolios]
description: Scopri come eseguire una simulazione personalizzata e scaricare simulazioni settimanali dalla vista Portfolio.
feature: Search Optimization, Search Portfolios, Search Simulations
hide: true
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
source-git-commit: 3e70998ad9547cecc0f3581d6cfd917051d549db
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 0%
---
# Eseguire e scaricare simulazioni dalla visualizzazione [!UICONTROL Portfolios]

*funzionalità Beta*

Puoi eseguire una simulazione personalizzata per un singolo portfolio [ottimizzato o attivo](portfolio-about.md#portfolio-status) e scaricare simulazioni settimanali automatizzate per un massimo di 100 portfolio dalla visualizzazione [!UICONTROL Portfolios].

L&#39;esecuzione di una simulazione personalizzata richiede l&#39;autorizzazione [!UICONTROL Create Simulation]. Il download di simulazioni settimanali richiede l&#39;autorizzazione [!UICONTROL View Simulation].

>[!NOTE]
>
>È inoltre possibile [creare o eseguire nuovamente una simulazione personalizzata dalla visualizzazione [!UICONTROL Simulations]](/help/search-social-commerce/new-ui/plan/simulations/simulation-create.md).

## Eseguire una simulazione personalizzata {#run-simulation}

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Portfolios]**.

1. Effettuare una delle seguenti operazioni:

   * Posizionare il cursore sulla riga portfolio. Accanto al nome del portfolio, fare clic su **[!UICONTROL ...]** > **[!UICONTROL Run Simulation]**.

   * Seleziona la casella di controllo accanto al portfolio. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL More]>[!UICONTROL Run Simulation]**.

1. Specificare le [impostazioni di simulazione personalizzate](#custom-simulation-settings):

   1. Nella scheda **[!UICONTROL Basic Settings]**, immettere un **[!UICONTROL Simulation Name]** univoco e modificare i parametri di base in base alle esigenze.

   1. (Facoltativo) Nella scheda **[!UICONTROL Advanced Settings]**, modifica i parametri avanzati.

   Le impostazioni correnti del portfolio selezionato vengono utilizzate come impostazioni predefinite. La modifica delle impostazioni di simulazione non modifica le impostazioni del portfolio.

1. Fare clic su **[!UICONTROL Next]**.

1. Rivedi le impostazioni e apporta le modifiche necessarie.

1. Fare clic su **[!UICONTROL Submit & Run]**.

La richiesta viene inviata e viene aperta la visualizzazione [!UICONTROL Simulations]. È possibile [scaricare la simulazione](/help/search-social-commerce/new-ui/plan/simulations/simulation-download.md) dopo averla completata correttamente.

## Scarica simulazioni settimanali {#download-simulations}

È possibile scaricare simulazioni settimanali per una data di esecuzione alla volta come cartella di lavoro [!DNL Microsoft Excel] (file XLSX). Sono inclusi solo i portfolio attivi e ottimizzati con i rapporti di simulazione disponibili per tale data.

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Portfolios]**.

1. Seleziona la casella di controllo accanto a ciascun portfolio di cui desideri scaricare la simulazione settimanale. Seleziona fino a 100 portfolio.

1. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL More]>[!UICONTROL Download Simulation]**.

1. In **[!UICONTROL Weekly Simulation]**, selezionare una data di esecuzione.

   La data disponibile più recente è selezionata per impostazione predefinita. Se i rapporti non sono disponibili per alcuni portfolio selezionati, la finestra di dialogo mostra quanti portfolio verranno esclusi. Se necessario, seleziona un’altra data. Non puoi scaricare un rapporto se per nessun portfolio selezionato è disponibile una simulazione per quella data.

1. Fare clic sul pulsante di download, la cui etichetta include il numero di portfolio con i report disponibili (ad esempio, **[!UICONTROL Download 2 portfolios]**).

   Il file viene scaricato in base alla normale procedura del browser. Il messaggio di completamento indica quanti portfolio sono stati inclusi.

Per scaricare simulazioni personalizzate o selezionare singole simulazioni settimanali, utilizzare la visualizzazione [[!UICONTROL Simulations]](/help/search-social-commerce/new-ui/plan/simulations/simulation-download.md).

## Impostazioni di simulazione personalizzate {#custom-simulation-settings}

Per ulteriori informazioni sulle impostazioni di simulazione personalizzate, consulta la Guida all’ottimizzazione, disponibile in Search, Social e Commerce.

>[!MORELIKETHIS]
>
>* [(Nuova interfaccia) Visualizza dettagli prestazioni portfolio](portfolio-details.md)
>* [Informazioni sui portfolio](portfolio-about.md)
>* [Esegui o riesegui una simulazione personalizzata](/help/search-social-commerce/new-ui/plan/simulations/simulation-create.md)
>* [Scarica simulazioni](/help/search-social-commerce/new-ui/plan/simulations/simulation-download.md)
