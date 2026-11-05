---
title: (Nuova interfaccia) Gestire i modelli di rapporto
description: Scopri come creare, visualizzare, modificare ed eliminare modelli di rapporto riutilizzabili per rapporti pianificati e on-demand.
feature: Search Reports
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 9166e3e1-13c1-5edf-bc2a-c6e22231df68
    internal-label: Search Reports
source-git-commit: eb12699872b7c89240f5340cd3b0a251c9c08366
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 0%
---
# (Nuova interfaccia) Gestire i modelli di rapporto

I modelli di rapporto sono layout di rapporto predefiniti che è possibile riutilizzare quando si genera la maggior parte dei rapporti. L&#39;utilizzo dei modelli consente di risparmiare tempo se si desidera utilizzare parametri non predefiniti, eseguire varianti dello stesso rapporto o eseguire lo stesso rapporto in base a una pianificazione regolare. I modelli salvati sono disponibili nella scheda **[!UICONTROL Templates]** in **[!UICONTROL Reports]>[!UICONTROL Reports]**.

Puoi gestire fino a 100 modelli alla volta.

La visualizzazione dei dati richiede l&#39;autorizzazione [!UICONTROL View Scheduled Reports]. La creazione, la duplicazione, la modifica, l&#39;esecuzione e l&#39;eliminazione di modelli nonché la copia dei dati delle righe richiedono l&#39;autorizzazione [!UICONTROL Edit Scheduled Reports]. Puoi modificare solo i modelli che hai creato.

## Azioni disponibili

* [Creare un modello di report](#template-create) come nuovo modello o basato su un modello esistente.

* [Visualizzare le impostazioni di un modello di report senza modificare l&#39;originale](#template-view).

* [Modifica un modello di report](#template-edit), inclusa la pianificazione.

* [Esegui report su richiesta per i modelli specificati](#template-run).

* [Elimina modelli di report](#template-delete).

* [Copia tutti i dati nelle righe selezionate negli Appunti](#copy-to-clipboard).

## Creare un modello di rapporto {#template-create}

1. Nel menu principale, fare clic su **[!UICONTROL Reports]>[!UICONTROL Reports]**.

1. Fare clic sulla scheda **[!UICONTROL Templates]**.

1. Effettuare una delle seguenti operazioni:

   * Per creare un nuovo modello, fare clic su **[!UICONTROL Create Template]**. Nel pannello **[!UICONTROL Create a New Template]**, selezionare la categoria e il tipo di report, quindi fare clic su **[!UICONTROL Proceed]**.

   * Per creare un modello basato su un modello esistente, posizionare il cursore sulla riga del modello e fare clic su ![Impostazioni modello](/help/search-social-commerce/assets/settings-new.png "Impostazioni modello") **[!UICONTROL Template Settings]** o **[!UICONTROL ...]>[!UICONTROL Duplicate]**.

1. Immettere un **[!UICONTROL Report Name]** univoco per il modello e verificare che **[!UICONTROL Save as Template]** sia abilitato.

   L&#39;impostazione è attivata per impostazione predefinita quando si inizia con **[!UICONTROL Create Template]**. Se viene disattivata, l&#39;azione finale diventa **[!UICONTROL Run Report]**, che genera un report invece di salvare un modello.

1. Configura le impostazioni del report per [report di base e avanzati](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-settings.md), [report assistenza](/help/search-social-commerce/new-ui/reports/management/assist/assist-report-settings.md), [report accuratezza modello](/help/search-social-commerce/new-ui/reports/management/model-accuracy/model-accuracy-report-settings.md) o [report speciali](/help/search-social-commerce/new-ui/reports/management/specialty/specialty-report-settings.md).

   Fare clic su **[!UICONTROL Next]** per spostarsi tra le sezioni delle impostazioni.

1. (Facoltativo) Per generare automaticamente i report, configurare **[!UICONTROL Frequency]** e le impostazioni di consegna in **[!UICONTROL Scheduling]**.

1. Fare clic su **[!UICONTROL Create]**.

È inoltre possibile salvare un modello durante la [creazione di un report dalla scheda Ultimi report](/help/search-social-commerce/new-ui/reports/management/report-manage.md) abilitando **[!UICONTROL Save as Template]** prima di inviare le impostazioni del report.

## Visualizzare le impostazioni di un modello di report {#template-view}

Per verificare le impostazioni senza modificare il modello originale, aprire un duplicato. È necessaria l&#39;autorizzazione [!UICONTROL Edit Scheduled Reports]. L&#39;apertura del duplicato non comporta il salvataggio di un nuovo modello.

1. Nel menu principale, fare clic su **[!UICONTROL Reports]>[!UICONTROL Reports]**.

1. Fare clic sulla scheda **[!UICONTROL Templates]**.

1. Posizionare il cursore sulla riga del modello e fare clic su ![Impostazioni modello](/help/search-social-commerce/assets/settings-new.png "Impostazioni modello") **[!UICONTROL Template Settings]**.

1. Rivedi le impostazioni del rapporto.

1. Al termine, fai clic su **[!UICONTROL Cancel]**. Se viene richiesto di eliminare la configurazione, fare clic su **[!UICONTROL Discard]**.

Per salvare una copia, seguire la [procedura di creazione del modello](#template-create).

## Modificare un modello di rapporto {#template-edit}

È possibile modificare le impostazioni e la pianificazione di qualsiasi modello creato. Le modifiche vengono applicate ai rapporti generati dal modello in futuro.

1. Nel menu principale, fare clic su **[!UICONTROL Reports]>[!UICONTROL Reports]**.

1. Fare clic sulla scheda **[!UICONTROL Templates]**.

1. Selezionare la casella di controllo accanto a un modello creato.

1. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL Edit]**.

   [!UICONTROL Edit] non è disponibile se sono selezionati più modelli o se il modello selezionato è stato creato da un altro utente.

1. Modifica le impostazioni del rapporto. Per aggiungere, modificare o rimuovere una pianificazione, modificare **[!UICONTROL Frequency]** in **[!UICONTROL Scheduling]**.

   Seleziona una frequenza giornaliera, settimanale o mensile per i rapporti pianificati. Per rimuovere una pianificazione ricorrente, selezionare **[!UICONTROL Now]**.

   **[!UICONTROL Save as Template]** e **[!UICONTROL Type]** sono di sola lettura quando si modifica un modello esistente. Non è necessario abilitare di nuovo [!UICONTROL Save as Template].

1. Fare clic su **[!UICONTROL Save]**.

## Eseguire report su richiesta per i modelli specificati {#template-run}

Puoi eseguire rapporti per uno o più modelli in qualsiasi momento.

1. Nel menu principale, fare clic su **[!UICONTROL Reports]>[!UICONTROL Reports]**.

1. Fare clic sulla scheda **[!UICONTROL Templates]**.

1. Effettuare una delle seguenti operazioni:

   * Per eseguire un singolo modello:

     1. Aprire il menu della riga del modello e selezionare **[!UICONTROL Run]**.

     1. Nel messaggio di conferma, fare clic su **[!UICONTROL Confirm]**.

   * Per eseguire uno o più modelli:

     1. Selezionare la casella di controllo accanto a ogni modello che si desidera eseguire.

     1. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL Run]**.

     1. Nel messaggio di conferma, fare clic su **[!UICONTROL Confirm]**.

È inoltre possibile eseguire un modello durante la modifica facendo clic su **[!UICONTROL Run Report]** e quindi su **[!UICONTROL Confirm]**. Salva prima le modifiche; questa azione esegue il modello salvato.

## Eliminare i modelli di rapporto {#template-delete}

Puoi eliminare qualsiasi modello di rapporto disponibile. Quando elimini un modello che include una pianificazione, tale rapporto non viene generato in futuro.

1. Nel menu principale, fare clic su **[!UICONTROL Reports]>[!UICONTROL Reports]**.

1. Fare clic sulla scheda **[!UICONTROL Templates]**.

1. Effettuare una delle seguenti operazioni:

   * Per eliminare un singolo modello:

     1. Aprire il menu della riga del modello e selezionare **[!UICONTROL Delete]**.

     1. Nel messaggio di conferma, fare clic su **[!UICONTROL Confirm]**.

   * Per eliminare uno o più modelli:

     1. Selezionare la casella di controllo accanto a ogni modello che si desidera eliminare.

     1. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL Delete]**.

     1. Nel messaggio di conferma, fare clic su **[!UICONTROL Confirm]**.

## Copia tutti i dati nelle righe selezionate negli Appunti {#copy-to-clipboard}

Copiare le informazioni visibili nelle righe selezionate, in base ai filtri applicati e alle colonne visibili nella vista. Le informazioni vengono salvate come valori separati da tabulazioni (TSV).

1. Selezionare la casella di controllo accanto a ogni riga di cui si desidera copiare i dati.

1. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL Copy]**.

1. Nel messaggio di conferma, fare clic su **[!UICONTROL Confirm]**.
