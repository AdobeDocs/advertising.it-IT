---
title: Gestire le campagne
description: Scopri come creare e gestire le campagne pubblicitarie.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 6b67f3e2759ddd80300c86df610b36684b7a07e2
workflow-type: tm+mt
source-wordcount: 2285
ht-degree: 0%

---

# Gestire le campagne

*funzionalità Beta*

Una campagna è il componente principale di un account di ad network. Per la maggior parte dei tipi di campagna, è costituito da un set di gruppi di annunci o set di annunci. Le impostazioni della campagna includono parametri di budget, target di annunci e parametri di tracciamento facoltativi per tutti gli annunci della campagna. I parametri di tracciamento a livello di campagna sostituiscono i parametri a livello di account, ma possono essere sostituiti a un livello inferiore.

Dopo aver [reso accessibile un account di rete tramite una connessione API](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md) e dopo che Search, Social e Commerce hanno sincronizzato i dati dell&#39;account con la rete di annunci, puoi creare nuove campagne con [tipi di campagna supportati](/help/search-social-commerce/introduction/supported-inventory.md). Puoi anche modificare e cambiare lo stato delle campagne.

Per informazioni dettagliate sulle funzionalità disponibili per ogni rete di annunci, vedi &quot;[Inventario supportato](/help/search-social-commerce/introduction/supported-inventory.md).&quot;

## Informazioni sulla visualizzazione [!UICONTROL Campaigns] {#campaign-view-about}

Nella visualizzazione [!UICONTROL Manage] > [!UICONTROL Campaigns] sono elencate tutte le campagne nella visualizzazione filtrata per l&#39;account dell&#39;inserzionista selezionato. Puoi aprire un elenco di gruppi di annunci nella campagna facendo clic sul nome della campagna.

Quando si aggiungono e si modificano i dati della campagna nelle visualizzazioni [!UICONTROL Campaigns], Search, Social e Commerce inviano immediatamente le modifiche dei dati alla rete di annunci. Search, Social e Commerce estraggono inoltre i dati della struttura della campagna e i dati sui clic ogni giorno, o più spesso quando vengono rilevate nuove campagne. Per tutte le reti pubblicitarie sincronizzate, puoi anche sincronizzare gli account su richiesta in base alle esigenze.

Search, Social e Commerce estraggono i dati sulle prestazioni ogni ora dagli account sincronizzati [!DNL Google Ads] e [!DNL Microsoft Advertising] e ogni giorno per altri account di rete di annunci sincronizzati.

### Azioni disponibili

* [Creare una campagna](#campaign-create)

* [Rinominare una campagna dall’interno della riga](#campaign-rename)

* [Modificare le impostazioni della campagna](#campaign-edit)

* [Modificare lo stato o eliminare una campagna dalla riga](#campaign-status)

* [Assegnare campagne a un portfolio e rimuovere campagne da un portfolio](#campaign-portfolio)

* [Visualizzare un grafico delle prestazioni nella visualizzazione [!UICONTROL Campaigns]](#campaign-performance-graph)

* [Assegnare vincoli di offerta alle campagne e annullare l’assegnazione di vincoli alle campagne](#campaign-constraints)

* [Assegnare vincoli target alle campagne e annullare l’assegnazione di vincoli target alle campagne](#campaign-target-constraints)

* [Assegna classificazioni di etichette alle campagne e rimuovi le classificazioni di etichette dalle campagne](#campaign-classifications)

* [Gestisci i report di visualizzazione dati dalla visualizzazione [!UICONTROL Campaigns]](#campaign-reports)

## Creare una campagna {#campaign-create}

>[!NOTE]
>
>* Prima di creare una campagna, [implementa i tag di tracciamento delle conversioni](/help/search-social-commerce/tracking/conversion-tracking-about.md) nelle pagine Web dell&#39;inserzionista.
>* Per creare un numero elevato di campagne contemporaneamente, utilizzare <!-- Not available in new UI as of 7/21: the [copy and paste feature](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) or--> [bulksheet campagna](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Fare clic su **[!UICONTROL Create Campaign]**.

1. Specifica le impostazioni della campagna [Baidu](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-baidu.md), [Google Ads](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-google.md), [LY Ads](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-ly.md), [Microsoft Advertising](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-microsoft.md) o [Yandex](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-yandex.md).

1. Fare clic su **[!UICONTROL Review and Save]**.

1. Se necessario, fai clic su ![Modifica](/help/search-social-commerce/assets/edit-new.png "Modifica") e modifica le impostazioni della campagna.

1. Fare clic su **[!UICONTROL Create]**.

A seconda della rete di annunci su cui è stata creata la campagna, potrebbe essere necessario creare gruppi di annunci e annunci associati prima che la campagna venga inviata alla rete di annunci.

## Rinominare una campagna {#campaign-rename}

Rinominare rapidamente una campagna senza aprire le impostazioni complete della campagna.

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Posizionare il cursore sulla riga della campagna e fare clic su **[!UICONTROL ...]>[!UICONTROL Rename]**.

1. Modificare il nome e quindi fare clic su **[!UICONTROL Apply]**.

## Modificare le impostazioni della campagna {#campaign-edit}

Puoi modificare le impostazioni per le singole campagne. Puoi anche modificare alcuni campi per più campagne contemporaneamente, tra cui alcuni dettagli della campagna, opzioni di budget e opzioni URL comuni a tutte le campagne selezionate.

>[!TIP]
>
>È inoltre possibile modificare i dati in blocco utilizzando <!-- Not available in new UI as of 7/21: the [copy and paste feature](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) or--> [bulksheet campagna](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Effettuare una delle seguenti operazioni:

   * Tenere premuto il cursore sul nome dell&#39;entità e fare clic su **[!UICONTROL ...]>[!UICONTROL Edit]**.

   * Seleziona la casella di controllo accanto alla campagna. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL Edit]**.

1. Modifica [Baidu](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-baidu.md), [Google Ads](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-google.md), [LY Ads](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-ly.md), <!-- [Meta Ads](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-meta.md), --> [Impostazioni campagna Microsoft Advertising](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-microsoft.md) o [Yandex](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-yandex.md).

1. Fare clic su **[!UICONTROL Review and Save]**.

1. Se necessario, fai clic su ![Modifica](/help/search-social-commerce/assets/edit-new.png "Modifica") e modifica le impostazioni della campagna.

1. Fare clic su **[!UICONTROL Update]**.

A seconda della rete di annunci in cui è stata creata la campagna, potrebbe essere necessario includere gruppi di annunci e annunci prima di inviarla alla rete di annunci.

## Modificare lo stato di una campagna {#campaign-status}

Cambia rapidamente lo stato di una campagna senza aprire le impostazioni complete della campagna.

Puoi mettere in pausa qualsiasi campagna attiva su una rete di annunci supportata per disabilitare le offerte su di essa. In seguito puoi riprendere l’offerta riportando lo stato attivo.

Puoi anche eliminare qualsiasi campagna attiva o in pausa. Le campagne eliminate vengono eliminate dalla rete di annunci. Sono ancora visibili quando li includi nel filtro dati, ma non puoi modificarli.

### Attivare o mettere in pausa una campagna

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Posizionare il cursore sulla riga della campagna e fare clic su ![Modifica](/help/search-social-commerce/assets/edit.png "Modifica") accanto alla colonna [!UICONTROL Status].

1. Modifica lo stato:

   * Per attivare una campagna in pausa, selezionare **[!UICONTROL Active]**.

   * Per sospendere una campagna attiva, selezionare **[!UICONTROL Paused]**.

### Eliminare una campagna

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Effettuare una delle seguenti operazioni:

   * Posizionare il cursore sulla riga della campagna e fare clic su **[!UICONTROL ...]>[!UICONTROL Delete]**.

   * Posizionare il cursore sulla riga della campagna e fare clic su ![Modifica](/help/search-social-commerce/assets/edit.png "Modifica") accanto alla colonna [!UICONTROL Status]. Selezionare **[!UICONTROL Deleted]**.

## Assegnare campagne a un portfolio {#campaign-portfolio}

L’assegnazione di una campagna a un portfolio ottimizzato consente a Search, Social e Commerce di ottimizzare le offerte, il budget delle campagne e i target delle strategie di offerta per parole chiave e annunci nella campagna. È possibile assegnare le campagne a un portfolio dalla vista [!UICONTROL Campaigns], quando si crea il portfolio o modificandone le impostazioni.

Non tutti i tipi di campagne e le reti pubblicitarie sono idonei per l&#39;ottimizzazione. Vedere un elenco di [tipi di campagne supportati](/help/search-social-commerce/introduction/supported-inventory.md) che è possibile includere in un portfolio. Inoltre, verifica il supporto per l&#39;ottimizzazione [per ogni strategia di offerta della campagna](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md#optimization-by-bid-strategy).

>[!NOTE]
>
>Ogni campagna può essere assegnata a un solo portfolio. Se assegni una campagna già associata a un altro portfolio a un nuovo portfolio, viene rimossa dal portfolio originale.

### Assegna campagne a un portfolio esistente dalla visualizzazione [!UICONTROL Campaigns]

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Seleziona la casella di controllo accanto a ciascuna campagna da assegnare a un singolo portfolio.

1. Nella barra degli strumenti delle azioni in blocco, fare clic su **+[!UICONTROL Assign]** > **[!UICONTROL Existing Portfolio]**.

1. Seleziona il portfolio.

1. Fare clic su **[!UICONTROL Assign Now]**.

### Assegna campagne a un nuovo portfolio dalla visualizzazione [!UICONTROL Campaigns]

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Seleziona la casella di controllo accanto a ciascuna campagna per la quale desideri creare il nuovo portfolio.

1. Nella barra degli strumenti delle azioni in blocco, fare clic su **+[!UICONTROL Assign]** > **[!UICONTROL New Portfolio]**.

1. Nella schermata [!UICONTROL Create Portfolio], specificare le impostazioni del portfolio.

   Le campagne selezionate in precedenza sono già assegnate alla campagna. Facoltativamente, puoi modificare l’elenco delle campagne per il portfolio.

   Per ulteriori informazioni sulle impostazioni del portfolio, consulta la Guida all’ottimizzazione, disponibile in Search, Social e Commerce.

1. Fare clic su **[!UICONTROL Review and Save]**.

### Modificare le assegnazioni di una campagna per un portfolio dalla visualizzazione [!UICONTROL Portfolios]

Quando rimuovi una campagna da un portfolio, Search, Social e Commerce non possono ottimizzare le offerte, il budget delle campagne e i target delle strategie di offerta per tale campagna.

L’azione viene registrata nella cronologia delle modifiche del portfolio.

Per ulteriori informazioni sull’ottimizzazione, consulta la Guida all’ottimizzazione, disponibile in Search, Social e Commerce.

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Portfolios]**.

1. Seleziona la casella di controllo accanto al portfolio.

1. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL Edit]**.

1. Nelle impostazioni del portfolio, vai alla sezione [!UICONTROL Assign Campaigns] e modifica le assegnazioni della campagna.

   Per ulteriori informazioni sulle impostazioni del portfolio, consulta la Guida all’ottimizzazione, disponibile in Search, Social e Commerce.

1. Fare clic su **[!UICONTROL Review and Save]**.

1. Rivedere le impostazioni e apportare le modifiche necessarie, quindi fare clic su **[!UICONTROL Save]**.

## Gestire le assegnazioni dei vincoli di offerta per le campagne {#campaign-constraints}

Ogni entità può avere un solo vincolo. I vincoli vengono ereditati dalle entità figlio, pertanto non è necessario assegnare vincoli alle entità figlio a meno che non si desideri sostituire i valori ereditati.

L’annullamento dell’assegnazione di un vincolo rimuove l’associazione con i componenti conto e tutti i relativi componenti figlio e i dati del rapporto relativi al vincolo non sono più disponibili per tali componenti. L’annullamento dell’assegnazione di un vincolo non comporta l’eliminazione del vincolo né dei componenti dell’account.

>[!NOTE]
>
>I vincoli attivi limitano le offerte solo per le unità di offerta assegnate nei portfolio legacy ottimizzati a livello di parola chiave. Vengono ignorate per le unità di offerta presenti in portafogli attivi, in portafogli ibridi o che non appartengono a portafogli.

### Assegna un vincolo di offerta alle campagne selezionate dalla nuova visualizzazione [!UICONTROL Campaigns]

Puoi assegnare un singolo vincolo a una o più campagne.

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Seleziona la casella di controllo accanto a ciascuna campagna a cui assegnare un singolo vincolo.

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

### Rimuovi i vincoli di offerta dalle campagne selezionate dalla nuova visualizzazione [!UICONTROL Campaigns]

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Seleziona la casella di controllo accanto a ciascuna campagna da cui annullare l’assegnazione dei vincoli.

1. Nella barra degli strumenti Azioni in blocco fare clic su **-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Fare clic su **[!UICONTROL Confirm]**.

### Rimuovi i vincoli di offerta dalle unità di offerta di ricerca dalle visualizzazioni legacy [!UICONTROL Campaigns]

>[!NOTE]
>
>Per eliminare un vincolo rendendolo non disponibile per utilizzi futuri, vedere &quot;Eliminare i vincoli per le unità di offerta di ricerca&quot; nel capitolo della Guida all&#39;ottimizzazione relativo a &quot;Vincoli di offerta&quot;, disponibile all&#39;interno di Search, Social e Commerce.<!-- verify convention for referencing Optimization Guide here -->

1. In **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**, selezionare la visualizzazione del componente account.

1. Selezionare la casella di controllo accanto a ogni componente da cui si desidera rimuovere il vincolo.

   Per suggerimenti sulla selezione di più righe, vedere &quot;[Selezionare più righe](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Nella barra degli strumenti sopra la tabella dati fare clic su **[!UICONTROL More]** e quindi su **[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Nella finestra di dialogo di conferma, selezionare **[!UICONTROL Yes, Unassign]**.

## Gestire le assegnazioni dei vincoli di destinazione per le campagne {#campaign-target-constraints}

### Assegna un vincolo di destinazione alle campagne selezionate dalla nuova visualizzazione [!UICONTROL Campaigns]

Puoi assegnare un singolo vincolo di destinazione a una o più campagne.

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Seleziona la casella di controllo accanto a ciascuna campagna a cui assegnare un singolo vincolo di destinazione.

1. Nella barra degli strumenti delle azioni in blocco, fare clic su **+[!UICONTROL Assign]** > **[!UICONTROL Target Constraint]**.

1. Selezionate il vincolo.

1. Fare clic su **[!UICONTROL Assign Now]**.

### Rimuovi i vincoli di destinazione dalle campagne selezionate dalla nuova visualizzazione [!UICONTROL Campaigns]

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Seleziona la casella di controllo accanto a ciascuna campagna da cui annullerai l’assegnazione di un vincolo di destinazione.

1. Nella barra degli strumenti Azioni in blocco fare clic su **-[!UICONTROL Unassign]** > **[!UICONTROL Target Constraint]**.

1. Fare clic su **[!UICONTROL Confirm]**.

## Assegnare le classificazioni delle etichette alle campagne {#campaign-classifications}

>[!NOTE]
>
>I valori delle etichette vengono ereditati dalle entità figlio, pertanto non immettere valori per le entità figlio a meno che non si desideri sostituire i valori ereditati.

### Assegnare valori di classificazione alle campagne

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Seleziona la casella di controllo accanto a ciascuna campagna a cui assegnare un valore di etichetta.

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

### Rimuovere i valori di classificazione delle etichette dalle campagne

Se si rimuove un valore di classificazione, viene rimossa l’associazione con il componente account e tutti i suoi componenti figlio. I dati del rapporto per il valore di classificazione non sono più disponibili per tali componenti. La rimozione di un valore di classificazione non comporta l’eliminazione del valore né dei componenti dell’account.

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Seleziona la casella di controllo accanto a ciascuna campagna da cui rimuoverai un valore di etichetta.

   Per suggerimenti sulla selezione di più righe, vedere &quot;[Selezionare più righe](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**.

1. Seleziona la casella di controllo accanto a ciascun valore di classificazione da rimuovere dalle entità selezionate.

   Per selezionare tutti i valori assegnati, scegliere **[!UICONTROL Select All]**. Per deselezionare tutti i valori assegnati, scegliere **[!UICONTROL Deselect All]**.

1. Fare clic su **[!UICONTROL Unassign Selected]**.

## Visualizzare un grafico delle prestazioni nella visualizzazione [!UICONTROL Campaigns] {#campaign-performance-graph}

Apri e configura un grafico delle prestazioni con un massimo di tre metriche totali per tutte le campagne nella vista per l’intervallo di date specificato.

### Visualizzare un grafico delle prestazioni

1. Sopra la tabella dati, fare clic su ![Grafici](/help/search-social-commerce/assets/charts.png "Grafici").

1. (Facoltativo) Specifica la valuta e fino a tre metriche da includere nel grafico.

### Nascondere un grafico delle prestazioni visibile

* Sopra la tabella dati, fare clic su ![Grafici](/help/search-social-commerce/assets/charts.png "Grafici").

## Gestisci i report di visualizzazione dati dalla visualizzazione [!UICONTROL Campaigns] {#campaign-reports}

<!-- Wording??????  Filtered data reports? -->

Generare un report che includa le righe di dati per una o più campagne nella visualizzazione [!UICONTROL Campaigns], quindi scaricare il report come file del foglio di lavoro di Microsoft Excel (formato XLXS). Il report include tutte le colonne visibili nella visualizzazione.

Puoi eliminare qualsiasi rapporto generato.

Vedere anche &quot;>* [(Interfaccia precedente) Scaricare dati da una visualizzazione di gestione campagne](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md)&quot; e &quot;[(Interfaccia precedente) Eliminare un report di dati sulle prestazioni o un file di bulksheet dal menu [!UICONTROL Downloads]](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md).&quot;

### Generare un rapporto con le righe di dati filtrate

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Specifica le campagne di cui desideri scaricare i dati:

   * Per scaricare i dati per campagne specifiche, seleziona le caselle di controllo accanto alle campagne.

   * Per scaricare i dati per tutte le campagne, non è necessario selezionare alcuna casella di controllo. Tutte le campagne sono incluse per impostazione predefinita.

1. Nella barra degli strumenti sopra la tabella dati, fare clic su ![Scarica report](/help/search-social-commerce/assets/download.png "Scarica report") **[!UICONTROL Reports]**.

1. Nelle impostazioni di [!UICONTROL Grid Reports], immettere un nome di report univoco, quindi fare clic su **[!UICONTROL Generate]**.

   Per impostazione predefinita, il file è denominato &quot;campaign_YYYYMMDD_NNNN&quot;, dove &quot;NNNN&quot; è il numero del processo sequenziale (ad esempio &quot;campaign_20250402_1326&quot;).

   Il file viene aggiunto all&#39;elenco [!UICONTROL Recently Generated].

1. (Facoltativo) Per scaricare il file una volta completato, fai clic su ![Scarica](/help/search-social-commerce/assets/download.png "Scarica") accanto al nome del file.

   Il file viene scaricato in base alla normale procedura del browser.

### Scaricare un rapporto completato

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Nella barra degli strumenti sopra la tabella dati, fare clic su ![Scarica report](/help/search-social-commerce/assets/download.png "Scarica report") **[!UICONTROL Reports]**.

1. Nell&#39;elenco [!UICONTROL Recently Generated] della finestra di dialogo [!UICONTROL Grid Reports], fare clic su ![Scarica](/help/search-social-commerce/assets/download.png "Scarica") accanto al nome del file.

   Il file viene scaricato in base alla normale procedura del browser.

### Eliminare un rapporto completato

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Nella barra degli strumenti sopra la tabella dati, fare clic su ![Scarica report](/help/search-social-commerce/assets/download.png "Scarica report") **[!UICONTROL Reports]**.

1. Nell&#39;elenco [!UICONTROL Recently Generated] della finestra di dialogo [!UICONTROL Grid Reports], fare clic su ![Elimina](/help/search-social-commerce/assets/delete-new.png "Elimina") accanto al nome del file.

>[!MORELIKETHIS]
>
>* [Gestione dei vincoli per le unità delle offerte di ricerca](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [Gestisci assegnazioni vincoli per gruppi di annunci](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-constraint-assignments-manage.md)
>* [Gestisci assegnazioni vincoli per parole chiave](/help/search-social-commerce/new-ui/target/keywords/keyword-constraint-assignments-manage.md)
>* [Gestisci assegnazioni vincoli per posizionamenti](/help/search-social-commerce/new-ui/target/placements/placement-constraint-assignments-manage.md)
>* [(interfaccia precedente) Scarica dati da una visualizzazione di gestione campagne](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md)
>* [(Interfaccia precedente) Eliminare un report di dati sulle prestazioni o un file di bulksheet dal menu [!UICONTROL Downloads]](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)
>* [[!DNL Baidu] impostazioni campagna](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-baidu.md)
>* [[!DNL Google Ads] impostazioni campagna](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-google.md)
>* [[!DNL LY Ads] impostazioni campagna](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-ly.md)
>* [[!DNL Microsoft Advertising] impostazioni campagna](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-microsoft.md)
>* [[!DNL Yandex] impostazioni campagna](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-yandex.md)

<!-- >* [[!DNL Meta Ads] campaign settings](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-meta.md) -->

