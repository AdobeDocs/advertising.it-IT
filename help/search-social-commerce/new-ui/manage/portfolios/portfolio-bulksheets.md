---
title: Modifica in blocco le impostazioni del portfolio tramite file bulksheet
description: Scopri come modificare le impostazioni per più portfolio utilizzando un file bulksheet.
feature: Search Portfolios, Search Optimization
hide: true
exl-id: 20f7419d-9f5e-4477-ae8d-8b85a79b1e81
source-git-commit: 8b63f697278b5dc4ecbb720af44053fbc771273f
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 0%

---

# Modifica in blocco le impostazioni del portfolio tramite file bulksheet

*funzionalità Beta*

Un bulksheet portfolio è un file che contiene le impostazioni del portfolio in un formato specifico e può essere utilizzato per rivedere e modificare rapidamente le impostazioni. Puoi generare (scaricare) i bulksheet con le impostazioni per uno o più portfolio. Il file viene scaricato come cartella di lavoro [!DNL Excel] con due fogli di lavoro (formato XLSX). La cartella di lavoro include:

* Foglio di lavoro [!UICONTROL Instructions] di sola lettura con informazioni sulla modifica dei campi.

* Una scheda [!UICONTROL Portfolio Settings Edit], con una riga per portfolio incluso. Se necessario, puoi modificare i campi, salvare il file localmente e successivamente [caricare il file modificato](#portfolio-bulksheet-upload) in Search, Social e Commerce. I campi modificabili vengono evidenziati a colori.

## Scaricare un file bulksheet con le impostazioni del portfolio

1. (Facoltativo) Seleziona la casella di controllo accanto a ciascun portfolio da includere nel bulksheet.

   Se non selezioni portfolio specifici, puoi scaricare le impostazioni per tutti i portfolio.

1. Nella barra degli strumenti sopra la tabella dati, fai clic su:

   * (Per tutti i portfolio) **[!UICONTROL Bulk Operations]** > **[!UICONTROL Export All Portfolios]**.

   * (Per i portfolio selezionati) **[!UICONTROL Bulk Operations]** > **[!UICONTROL Export Selected Portfolios]**.

1. Immettere il nome del file del bulksheet da creare, quindi fare clic su **[!UICONTROL Export Now]**.

   Il file viene salvato nella cartella Download predefinita del browser.

## Carica un file di bulksheet con le impostazioni di portfolio aggiornate {#portfolio-bulksheet-upload}

Il file deve essere in formato XLSX.

1. Nella barra degli strumenti sopra la tabella dati, fare clic su **[!UICONTROL Bulk Operations]** > **[!UICONTROL Import Portfolio Details]**.

1. Nella finestra di dialogo [!UICONTROL Import Portfolio Details File]:

   1. Trascinare un file nella casella oppure fare clic su **[!UICONTROL Browse File]** per selezionare un file dal dispositivo o dalla rete.

   1. Fare clic su **[!UICONTROL Import]**.

Puoi controllare lo stato del caricamento dal pulsante [!UICONTROL Global Sync Status] (![Stato sincronizzazione globale](/help/search-social-commerce/assets/global-sync-status.png "Stato sincronizzazione globale")) accanto al selettore dell&#39;intervallo di date. Se una delle modifiche non ha avuto esito positivo, puoi scaricare un file di errore che mostra cosa non è riuscito.

Le notifiche vengono aggiunte anche al Centro notifiche e puoi aprire il riquadro Notifiche dall&#39;icona ![Notifiche](/help/search-social-commerce/assets/notifications-new.png "Notifiche") accanto al pulsante [!UICONTROL Global Sync Status] (![Stato sincronizzazione globale](/help/search-social-commerce/assets/global-sync-status.png "Stato sincronizzazione globale")).

## Requisiti dei dati per i file di bulksheet caricati

Tutti i file di bulksheet devono includere la colonna [!UICONTROL Portfolio ID] e ogni riga di dati deve includere un valore affinché [!UICONTROL Portfolio ID] sia actionable. Per ulteriori informazioni sui requisiti dei dati, vedere la scheda [!UICONTROL Instructions] nel file di bulksheet scaricato.

Per informazioni sulle colonne delle impostazioni del portfolio nella scheda [!UICONTROL Portfolio Settings Edit], vedere la Guida all&#39;ottimizzazione, disponibile in Search, Social e Commerce.

<!--
## Data fields on the [!UICONTROL Portfolio Settings Edit] tab

| Field | Required to import data? | Description |
| ----- | ------------------------ | ----------- |
| Portfolio ID |  |  |
| Portfolio Name |  |  |
| Status |  |  |
| Spend Strategy |  |  |
| Target |  |  |
| Hybrid |  |  |
| Auto adjust campaign budgets |  |  |
| Spend Multiple |  |  |
| Minimum Campaign Budget |  |  |
| Objective |  |  |
| Cost Half-Life |  |  |
| Revenue Half-Life |  |  |
| Min. Target CPA |  |  |
| Max. Target CPA |  |  |
| Min. Target ROAS |  |  |
| Max. Target ROAS |  |  |

-->

>[!MORELIKETHIS]
>
>* [(Nuova interfaccia) Modifica un portfolio](portfolio-edit.md)
>* [Crea un portfolio](portfolio-create.md)
>* [(Nuova interfaccia) Informazioni sui portfolio](portfolio-about.md)
