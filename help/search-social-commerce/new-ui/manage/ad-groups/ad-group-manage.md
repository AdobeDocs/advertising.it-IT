---
title: Gestire i gruppi di annunci
description: Scopri come creare e gestire i gruppi di annunci.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: d45eb490f9dbb7da89bd1270582e5548b70cbd31
workflow-type: tm+mt
source-wordcount: 1676
ht-degree: 0%

---

# Gestire i gruppi di annunci

<!-- Go through all -->

*funzionalità Beta*

Un gruppo di annunci include un set di annunci e le relative parole chiave. Un gruppo di annunci in una campagna che esegue il targeting della rete di visualizzazione può includere anche posizionamenti, ovvero posizioni nella rete di visualizzazione in cui possono essere visualizzati gli annunci. Le impostazioni dei gruppi di annunci, applicabili a tutti i componenti del gruppo di annunci, variano in base alla rete di annunci.

Dopo aver [reso accessibile un account di rete tramite una connessione API](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md) e dopo che Search, Social e Commerce hanno sincronizzato i dati dell&#39;account con la rete di annunci, puoi creare gruppi di annunci per un tipo di campagna [supportato](/help/search-social-commerce/introduction/supported-inventory.md). Puoi anche modificare e cambiare lo stato dei gruppi di annunci.

Per informazioni dettagliate sulle funzionalità disponibili per ogni rete di annunci, vedi &quot;[Inventario supportato](/help/search-social-commerce/introduction/supported-inventory.md).&quot;

## Informazioni sulla visualizzazione [!UICONTROL Ad Groups] {#ad-group-view-about}

Nella visualizzazione [!UICONTROL Manage] > [!UICONTROL Ad Groups] sono elencati tutti i gruppi di annunci nella visualizzazione filtrata per l&#39;account dell&#39;inserzionista selezionato.

### Azioni disponibili

* [Creare un gruppo di annunci](#ad-group-create)

* [Rinominare un gruppo di annunci dalla riga](#ad-group-rename)

* [Modificare le impostazioni del gruppo di annunci](#ad-group-edit)

* [Modificare lo stato o eliminare un gruppo di annunci dalla riga](#ad-group-status)

* [Visualizzare un grafico delle prestazioni nella visualizzazione [!UICONTROL Ad Groups]](#ad-group-performance-graph)

* [Assegnare vincoli di offerta ai gruppi di annunci e annullare l’assegnazione di vincoli dai gruppi di annunci](#ad-group-constraints)

* [Assegnare le classificazioni delle etichette ai gruppi di annunci e rimuovere le classificazioni delle etichette dai gruppi di annunci](#ad-group-classifications)

* [Gestisci i report di visualizzazione dati dalla visualizzazione [!UICONTROL Ad Groups]](#ad-group-reports)

## Creare un gruppo di annunci {#ad-group-create}

>[!TIP]
>
>Per creare un numero elevato di gruppi di annunci contemporaneamente, utilizza <!-- Not available in new UI as of 7/21: the [copy and paste feature](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) or--> [bulksheet campagna](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Fare clic su **[!UICONTROL Create Ad Group]**.

1. Specifica le impostazioni del gruppo di annunci [Baidu](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-baidu.md), [Google Ads](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-google.md), [LY Ads](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-ly.md), [Microsoft Advertising](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-microsoft.md) o [Yandex](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-yandex.md).

1. Fare clic su **[!UICONTROL Review and Save]**.

1. Se necessario, fai clic su ![Modifica](/help/search-social-commerce/assets/edit-new.png "Modifica") e modifica le impostazioni del gruppo di annunci.

1. Fare clic su **[!UICONTROL Create]**.

In seguito, puoi facoltativamente ignorare le offerte a livello di gruppo di annunci impostando offerte per singole parole chiave o posizionamenti nel gruppo di annunci.

## Rinominare un gruppo di annunci {#ad-group-rename}

Rinomina rapidamente un gruppo di annunci senza aprire le impostazioni complete del gruppo di annunci.

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Posizionare il cursore sulla riga del gruppo di annunci e fare clic su **[!UICONTROL ...]>[!UICONTROL Rename]**.

1. Modificare il nome e quindi fare clic su **[!UICONTROL Apply]**.

## Modificare le impostazioni del gruppo di annunci {#ad-group-edit}

Puoi modificare le impostazioni per singoli gruppi di annunci. Puoi anche modificare alcuni campi per più gruppi di annunci contemporaneamente, inclusi alcuni dettagli del gruppo di annunci, opzioni di budget e opzioni URL comuni a tutti i gruppi di annunci selezionati.

>[!TIP]
>
>È inoltre possibile modificare i dati in blocco utilizzando <!-- Not available in new UI as of 7/21: the [copy and paste feature](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) or--> [bulksheet campagna](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Effettuare una delle seguenti operazioni:

   * Tenere premuto il cursore sul nome dell&#39;entità e fare clic su **[!UICONTROL ...]>[!UICONTROL Edit]**.

   * Seleziona la casella di controllo accanto al gruppo di annunci. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL Edit]**.

1. Modifica le impostazioni del gruppo di annunci [Baidu](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-baidu.md), [Google Ads](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-google.md), [LY Ads](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-ly.md), [Microsoft Advertising](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-microsoft.md) o [Yandex](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-yandex.md).

1. Fare clic su **[!UICONTROL Review and Save]**.

1. Se necessario, fai clic su ![Modifica](/help/search-social-commerce/assets/edit-new.png "Modifica") e modifica le impostazioni del gruppo di annunci.

1. Fare clic su **[!UICONTROL Update]**.

## Modificare lo stato di un gruppo di annunci {#ad-group-status}

Cambia rapidamente lo stato di un gruppo di annunci senza aprire le impostazioni per gruppi di annunci completi.

Puoi mettere in pausa qualsiasi gruppo di annunci attivo su una rete di annunci supportata per disabilitare le offerte su di essa. In seguito puoi riprendere l’offerta riportando lo stato attivo.

Puoi anche eliminare qualsiasi gruppo di annunci attivo o in pausa. I gruppi di annunci eliminati vengono eliminati dalla rete di annunci. Sono ancora visibili quando li includi nel filtro dati, ma non puoi modificarli.

### Attivare o mettere in pausa un gruppo di annunci

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Posizionare il cursore sulla riga del gruppo di annunci e fare clic su ![Modifica](/help/search-social-commerce/assets/edit.png "Modifica") accanto alla colonna [!UICONTROL Status].

1. Modifica lo stato:

   * Per attivare un gruppo di annunci in pausa, selezionare **[!UICONTROL Active]**.

   * Per sospendere un gruppo di annunci attivo, selezionare **[!UICONTROL Paused]**.

### Eliminare un gruppo di annunci

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Effettuare una delle seguenti operazioni:

   * Posizionare il cursore sulla riga del gruppo di annunci e fare clic su **[!UICONTROL ...]>[!UICONTROL Delete]**.

   * Posizionare il cursore sulla riga del gruppo di annunci e fare clic su ![Modifica](/help/search-social-commerce/assets/edit.png "Modifica") accanto alla colonna [!UICONTROL Status]. Selezionare **[!UICONTROL Deleted]**.

## Gestire le assegnazioni dei vincoli di offerta per i gruppi di annunci {#ad-group-constraints}

Ogni entità può avere un solo vincolo. I vincoli vengono ereditati dalle entità figlio, pertanto non è necessario assegnare vincoli alle entità figlio a meno che non si desideri sostituire i valori ereditati.

L’annullamento dell’assegnazione di un vincolo rimuove l’associazione con i componenti conto e tutti i relativi componenti figlio e i dati del rapporto relativi al vincolo non sono più disponibili per tali componenti. L’annullamento dell’assegnazione di un vincolo non comporta l’eliminazione del vincolo né dei componenti dell’account.

### Assegna un vincolo di offerta ai gruppi di annunci selezionati dalla nuova visualizzazione [!UICONTROL Ad Groups]

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Selezionare la casella di controllo accanto a ogni gruppo di annunci a cui assegnare un singolo vincolo.

1. Nella barra degli strumenti delle azioni in blocco, fare clic su **+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Selezionate il vincolo.

1. Fare clic su **[!UICONTROL Assign Now]**.

### Assegna un vincolo di offerta alle unità di offerta di ricerca selezionate dalle viste legacy [!UICONTROL Campaigns]

1. In **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**, selezionare la visualizzazione del componente account.

1. Selezionare la casella di controllo accanto a ogni riga pertinente.

   Per suggerimenti sulla selezione di più righe, vedere &quot;[Selezionare più righe](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Nella barra degli strumenti sopra la tabella dati fare clic su **[!UICONTROL More]** e quindi su **[!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Selezionare il vincolo applicabile.

1. (Facoltativo) Immettere ulteriori dettagli:

   1. Accanto a [!UICONTROL Additional Details], fare clic su **[!UICONTROL Open]** per espandere i dettagli.

   1. Immettere un **[!UICONTROL Project Name]** facoltativo e/o un **[!UICONTROL Description]** facoltativo.

1. Fare clic su **[!UICONTROL Save]**.

### Rimuovi i vincoli di offerta dai gruppi di annunci selezionati dalla nuova visualizzazione [!UICONTROL Ad Groups]

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Selezionare la casella di controllo accanto a ogni gruppo di annunci da cui si desidera annullare l&#39;assegnazione dei vincoli.

1. Nella barra degli strumenti Azioni in blocco fare clic su **-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Fare clic su **[!UICONTROL Confirm]**.

### Rimuovi i vincoli di offerta dalle unità di offerta di ricerca dalle visualizzazioni legacy [!UICONTROL Campaigns]

>[!NOTE]
>
>Per eliminare un vincolo e renderlo non disponibile per utilizzi futuri, consulta &quot;Eliminare i vincoli per le unità di offerta di ricerca&quot; nel capitolo della Guida all’ottimizzazione su &quot;Vincoli di offerta&quot;, disponibile in Search, Social e Commerce.

1. In **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**, selezionare la visualizzazione del componente account.

1. Selezionare la casella di controllo accanto a ogni componente da cui si desidera rimuovere il vincolo.

   Per suggerimenti sulla selezione di più righe, vedere &quot;[Selezionare più righe](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Nella barra degli strumenti sopra la tabella dati fare clic su **[!UICONTROL More]** e quindi su **[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Nella finestra di dialogo di conferma, selezionare **[!UICONTROL Yes, Unassign]**.

## Assegnare le classificazioni delle etichette ai gruppi di annunci {#ad-group-classifications}

>[!NOTE]
>
>I valori delle etichette vengono ereditati dalle entità figlio, pertanto non immettere valori per le entità figlio a meno che non si desideri sostituire i valori ereditati.

### Assegnare valori di classificazione ai gruppi di annunci

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Seleziona la casella di controllo accanto a ciascun gruppo di annunci a cui assegnare un valore di etichetta.

   Per suggerimenti sulla selezione di più righe, vedere &quot;[Selezionare più righe](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Nella barra degli strumenti delle azioni in blocco, fare clic su **+[!UICONTROL Assign]** > **[!UICONTROL Label Classification]**.

1. Per ogni valore di classificazione applicabile, effettua le seguenti operazioni:

   1. Nella colonna **[!UICONTROL Classifications]**, specifica la classificazione:

      * Per utilizzare una classificazione esistente, fai clic sul nome della classificazione per espanderla.

      * Per creare una classificazione, fare clic su [!UICONTROL +] nell&#39;intestazione di colonna. Nel campo di input, immetti il nome della classificazione, quindi fai clic su ![Salva](/help/search-social-commerce/assets/save-checkmark.png "Salva") per salvare immediatamente la classificazione. Per utilizzare la nuova classificazione, fai clic sul nome della classificazione per espanderla.

        Il nome deve essere composto da [caratteri ASCII 32-126](https://www.asciitable.com/) e la lunghezza massima è di 27 caratteri a byte singolo.

   1. Nella colonna **[!UICONTROL Value Name]**, specifica il valore per la classificazione selezionata:

      * Per utilizzare un valore esistente, selezionate il valore.

      * Per creare un valore, fare clic su [!UICONTROL +] nell&#39;intestazione di colonna. Nel campo di input immettere il valore, quindi fare clic su ![Salva](/help/search-social-commerce/assets/save-checkmark.png "Salva") per salvare immediatamente il valore e selezionarlo per impostazione predefinita.

        La lunghezza massima è di 100 caratteri e può includere caratteri ASCII e non ASCII.

1. Fare clic su **+[!UICONTROL Assign Now]**.

### Rimuovere i valori di classificazione delle etichette dai gruppi di annunci

Se si rimuove un valore di classificazione, viene rimossa l’associazione con il componente account e tutti i suoi componenti figlio. I dati del rapporto per il valore di classificazione non sono più disponibili per tali componenti. La rimozione di un valore di classificazione non comporta l’eliminazione del valore né dei componenti dell’account.

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Seleziona la casella di controllo accanto a ciascun gruppo di annunci da cui rimuoverai un valore di etichetta.

   Per suggerimenti sulla selezione di più righe, vedere &quot;[Selezionare più righe](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**.

1. Seleziona la casella di controllo accanto a ciascun valore di classificazione da rimuovere dalle entità selezionate.

   Per selezionare tutti i valori assegnati, scegliere **[!UICONTROL Select All]**. Per deselezionare tutti i valori assegnati, scegliere **[!UICONTROL Deselect All]**.

1. Fare clic su **[!UICONTROL Unassign Selected]**.

## Visualizzare un grafico delle prestazioni nella visualizzazione [!UICONTROL Ad Groups] {#ad-group-performance-graph}

Apri e configura un grafico delle prestazioni con un massimo di tre metriche totali per tutti i gruppi di annunci nella vista per l’intervallo di date specificato.

### Visualizzare un grafico delle prestazioni

1. Sopra la tabella dati, fare clic su ![Grafici](/help/search-social-commerce/assets/charts.png "Grafici").

1. (Facoltativo) Specifica la valuta e fino a tre metriche da includere nel grafico.

### Nascondere un grafico delle prestazioni visibile

* Sopra la tabella dati, fare clic su ![Grafici](/help/search-social-commerce/assets/charts.png "Grafici").

## Gestisci i report di visualizzazione dati dalla visualizzazione [!UICONTROL Ad Groups] {#ad-group-reports}

Generare un report che includa le righe di dati per uno o più gruppi di annunci nella visualizzazione [!UICONTROL Ad Groups], quindi scaricare il report come file del foglio di lavoro di Microsoft Excel (formato XLXS). Il report include tutte le colonne visibili nella visualizzazione.

Puoi eliminare qualsiasi rapporto generato.

Vedere anche &quot;>* [(Interfaccia precedente) Scaricare dati da una visualizzazione di gestione campagne](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md)&quot; e &quot;[(Interfaccia precedente) Eliminare un report di dati sulle prestazioni o un file di bulksheet dal menu [!UICONTROL Downloads]](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md).&quot;

### Generare un rapporto con le righe di dati filtrate

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Specifica i gruppi di annunci di cui desideri scaricare i dati:

   * Per scaricare i dati per specifici gruppi di annunci, seleziona le caselle di controllo accanto ai gruppi di annunci.

   * Per scaricare i dati per tutti i gruppi di annunci, non è necessario selezionare alcuna casella di controllo. Per impostazione predefinita, sono inclusi tutti i gruppi di annunci.

1. Nella barra degli strumenti sopra la tabella dati, fare clic su ![Scarica report](/help/search-social-commerce/assets/download.png "Scarica report") **[!UICONTROL Reports]**.

1. Nelle impostazioni di [!UICONTROL Grid Reports], immettere un nome di report univoco, quindi fare clic su **[!UICONTROL Generate]**.

   Per impostazione predefinita, il file è denominato &quot;ad group_YYYYMMDD_NNNN&quot;, dove &quot;NNNN&quot; è il numero del processo sequenziale (ad esempio &quot;ad group_20250402_1326&quot;).

   Il file viene aggiunto all&#39;elenco [!UICONTROL Recently Generated].

1. (Facoltativo) Per scaricare il file una volta completato, fai clic su ![Scarica](/help/search-social-commerce/assets/download.png "Scarica") accanto al nome del file.

   Il file viene scaricato in base alla normale procedura del browser.

### Scaricare un rapporto completato

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Nella barra degli strumenti sopra la tabella dati, fare clic su ![Scarica report](/help/search-social-commerce/assets/download.png "Scarica report") **[!UICONTROL Reports]**.

1. Nell&#39;elenco [!UICONTROL Recently Generated] della finestra di dialogo [!UICONTROL Grid Reports], fare clic su ![Scarica](/help/search-social-commerce/assets/download.png "Scarica") accanto al nome del file.

   Il file viene scaricato in base alla normale procedura del browser.

### Eliminare un rapporto completato

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Nella barra degli strumenti sopra la tabella dati, fare clic su ![Scarica report](/help/search-social-commerce/assets/download.png "Scarica report") **[!UICONTROL Reports]**.

1. Nell&#39;elenco [!UICONTROL Recently Generated] della finestra di dialogo [!UICONTROL Grid Reports], fare clic su ![Elimina](/help/search-social-commerce/assets/delete-new.png "Elimina") accanto al nome del file.

>[!MORELIKETHIS]
>
>* [Gestione dei vincoli per le unità delle offerte di ricerca](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [Gestione assegnazioni vincoli per le campagne](/help/search-social-commerce/new-ui/manage/campaigns/campaign-constraint-assignments-manage.md)
>* [Gestisci assegnazioni vincoli per parole chiave](/help/search-social-commerce/new-ui/target/keywords/keyword-constraint-assignments-manage.md)
>* [Gestisci assegnazioni vincoli per posizionamenti](/help/search-social-commerce/new-ui/target/placements/placement-constraint-assignments-manage.md)
>* [(interfaccia precedente) Scarica dati da una visualizzazione di gestione campagne](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md)
>* [(Interfaccia precedente) Eliminare un report di dati sulle prestazioni o un file di bulksheet dal menu [!UICONTROL Downloads]](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)
>* [[!DNL Baidu] impostazioni gruppo di annunci](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-baidu.md)
>* [[!DNL Google Ads] impostazioni gruppo di annunci](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-google.md)
>* [[!DNL LY Ads] impostazioni gruppo di annunci](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-ly.md)
>* [[!DNL Microsoft Advertising] impostazioni gruppo di annunci](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-microsoft.md)
>* [[!DNL Yandex] impostazioni gruppo di annunci](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-yandex.md)
