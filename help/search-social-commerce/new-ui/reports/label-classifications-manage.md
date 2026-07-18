---
title: Gestire le classificazioni delle etichette
description: Scopri come utilizzare le classificazioni delle etichette per raggruppare i componenti dell’account.
feature: Search Label Classifications
source-git-commit: 44f83bcf32d671ad96a420827d16d8f1ec39049e
workflow-type: tm+mt
source-wordcount: '1514'
ht-degree: 0%

---

# Gestire le classificazioni delle etichette

Le classificazioni delle etichette consentono di raggruppare i componenti dell’account in set significativi. Ad esempio, puoi creare una classificazione dell&#39;etichetta principale denominata &quot;Geo&quot;, creare un valore di etichetta diverso per ogni area geografica (ad esempio &quot;Regno Unito&quot; e &quot;Giappone&quot;) all&#39;interno della classificazione, quindi assegnare i valori dell&#39;etichetta alle tue [unità di offerta](/help/search-social-commerce/glossary.md#a-b) o campagne principali. Puoi quindi includere qualsiasi valore di etichetta come colonna separata nelle viste e nei rapporti, e suddividere i rapporti in base a gruppi di classificazione e valori diversi.

## Componenti delle classificazioni delle etichette

### Classificazioni delle etichette

Ogni inserzionista può avere fino a 30 classificazioni di etichette, che sono categorie di livello principale. Dopo aver creato una classificazione di etichetta, puoi creare valori di etichetta specifici per la classificazione.

### Valori etichetta

Ogni classificazione di etichetta può avere fino a 2000 valori. Dopo aver creato valori di etichetta specifici per una classificazione, puoi assegnarli a campagne, gruppi di annunci, parole chiave, annunci, posizionamenti e gruppi di prodotti [ dalle viste gestione campagne](#classification-values-assign-campaign-management) o [utilizzando i bulksheet](#classification-values-assign-bulksheets).

Ogni entità idonea può avere valori di etichetta per più classificazioni, ma un solo valore di etichetta per classificazione. I valori delle etichette vengono ereditati dalle entità figlio, ma possono essere ignorati. Il valore assegnato al livello più basso sostituisce sempre i valori assegnati ai livelli padre.

## Visualizzazione Classificazioni etichette

La visualizzazione [!UICONTROL Reports] > [!UICONTROL Labels Classifications] include [!UICONTROL Classifications] e [!UICONTROL Label Values] sottoviste. Per impostazione predefinita, i dati vengono visualizzati per le classificazioni e i valori delle etichette a livello di parola chiave, ma è possibile visualizzare facoltativamente i dati per le classificazioni e i valori a livello di annuncio.

## Azioni disponibili

* Visualizza i dati per le classificazioni delle etichette.

* Visualizza i dati per i valori di classificazione delle etichette.

* [Crea una classificazione di etichette](#classification-create).

* Assegna valori di classificazione ai componenti account [dalle visualizzazioni di gestione campagne](#classification-values-assign-campaign-management) o [utilizzando i bulksheet](#classification-values-assign-bulksheets).

* [Rimuovere i valori di classificazione delle etichette dai componenti account](#classification-values-remove).

* [Elimina i valori di classificazione delle etichette](#classification-values-delete).

* [Elimina classificazioni etichette](#classification-delete).

## Creare una classificazione di etichette {#classification-create}

<!-- Update links to bulksheet columns once I have new files/paths -->

1. Fare clic su **[!UICONTROL Reports]>[!UICONTROL Label Classifications]**.

1. In alto a destra, fare clic su **[!UICONTROL Create Classification]**.

1. Immettere un nome di classificazione di etichetta univoco, quindi fare clic su **[!UICONTROL Create]**.

   Il nome deve essere univoco per l&#39;account dell&#39;inserzionista e deve essere costituito da [caratteri ASCII da 32 a 126](https://www.asciitable.com/) e la lunghezza massima è di 27 caratteri a byte singolo. Il nome non può essere identico al nome di una colonna di report o di una colonna di bulksheet esistente. Vedi i nomi delle colonne dei bulksheet per [Baidu](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-baidu.md), [Google Ads](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md), [LY Ads](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-japan.md), [Microsoft Advertising](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md), [Naver](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md), [Yahoo! Visualizza rete](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-display-network.md) e [Yandex](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yandex.md).

## Assegnare valori di classificazione ai componenti account dalle viste di gestione delle campagne {#classification-values-assign-campaign-management}

Puoi assegnare e rimuovere i valori di classificazione per le seguenti entità di ricerca dalle viste di gestione della campagna: campagna, gruppo di annunci, parola chiave, annuncio, posizionamento, gruppo di prodotti a livello di unità e destinazione di ricerca dinamica. Se necessario, è possibile creare classificazioni e valori di classificazione durante il processo di assegnazione. Ogni classificazione di etichetta può avere fino a 2000 valori.

Ogni entità può avere un valore di etichetta per classificazione. Ad esempio, Shoes_Campaign può avere un valore Color di &quot;rosso&quot; e un valore Geo di &quot;Los Angeles&quot;, ma non può avere più valori Color o Geo.

I valori delle etichette vengono ereditati dalle entità figlio, pertanto non immettere valori per le entità figlio a meno che non si desideri sostituire i valori ereditati.

>[!NOTE]
>
>Le parole chiave e la copia dell&#39;annuncio per alcune reti di annunci e tipi di campagne sono [non modificabili](/help/search-social-commerce/campaign-management/faqs-campaigns.md), il che significa che la loro modifica elimina l&#39;entità esistente e ne crea una nuova. Quando un’entità esistente viene eliminata in questo modo, la classificazione dell’etichetta non viene assegnata alla nuova entità.

1. Aprire la visualizzazione entità dal menu **[!UICONTROL Manage]** o **[!UICONTROL Target]**.

1. Selezionare la casella di controllo accanto a ogni riga pertinente.

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

## Assegnare valori di classificazione ai componenti conto utilizzando i bulksheet {#classification-values-assign-bulksheets}

<!-- Update bulksheet references to ones in new UI -->

È possibile associare le classificazioni delle etichette ai valori per le seguenti entità di ricerca utilizzando i bulksheet: campagna, gruppo di annunci, parola chiave, annuncio, posizionamento, gruppo di prodotti a livello di unità e destinazione di ricerca dinamica. Ogni classificazione di etichetta può avere fino a 2000 valori.

Ogni entità può avere un valore di etichetta per classificazione. Ad esempio, Shoes_Campaign può avere un valore Color di &quot;rosso&quot; e un valore Geo di &quot;Los Angeles&quot;, ma non può avere più valori Color o Geo.

I valori delle etichette vengono ereditati dalle entità figlio, pertanto non immettere valori per le entità figlio a meno che non si desideri sostituire i valori ereditati.

>[!NOTE]
>
>Le parole chiave e la copia dell&#39;annuncio per alcune reti di annunci e tipi di campagne sono [non modificabili](/help/search-social-commerce/campaign-management/faqs-campaigns.md), il che significa che la loro modifica elimina l&#39;entità esistente e ne crea una nuova. Quando un’entità esistente viene eliminata in questo modo, la classificazione dell’etichetta non viene assegnata alla nuova entità.

1. [Scaricare un bulksheet](/help/search-social-commerce/new-ui/set-up/bulksheets/download.md) che include le entità alle quali si desidera assegnare i valori di classificazione delle etichette:

   * Nella scheda [!UICONTROL Rows and Columns], espandere l&#39;elenco [!UICONTROL Campaign] nel riquadro [!UICONTROL Bulksheet Columns].

   * Espandere l&#39;elenco [!UICONTROL Label Classification].

   * Seleziona ogni classificazione per la quale desideri includere una colonna nel file del bulksheet.

     Ad esempio, se includi le classificazioni delle etichette &quot;Colore&quot; e &quot;Geo&quot;, il bulksheet includerà le colonne &quot;Colore&quot; e &quot;Geo&quot;.

1. Apri il file in un editor e aggiungi i valori delle etichette alle colonne di classificazione delle etichette per le entità a cui associarli. La lunghezza massima di ogni valore è di 100 caratteri e può includere caratteri ASCII e non ASCII.

   Vedi gli esempi di valori nella sezione successiva.

   Oltre ad aggiungere valori, puoi anche eliminare i valori esistenti rimuovendoli dalle righe pertinenti. Per rimuovere i valori sia da un&#39;entità padre che dalle relative entità figlio, a) includere solo la riga dell&#39;entità padre e rimuovere il valore di classificazione esistente oppure b) includere sia l&#39;entità padre che le relative entità figlio e rimuovere il valore di classificazione esistente da tutte le righe padre e figlio.

1. [Carica il file](/help/search-social-commerce/new-ui/set-up/bulksheets/upload.md) per creare le associazioni.

I valori delle etichette caricate sono visibili nelle visualizzazioni delle entità pertinenti.

### Esempio di valori di classificazione delle etichette da caricare nei bulksheet

Questo esempio include colonne per le classificazioni di etichette &quot;Colore&quot; e &quot;Geo&quot;. Per i bulksheet personalizzati, sostituisci le colonne con i nomi delle classificazioni delle etichette.

| Account | Campagna | Gruppo di annunci | Parola chiave | Annuncio | Posizionamento | Etichette | Colore | Geo |
|---|---|---|---|---|---|---|---|---|
| Att1 | C1 | | | | | | Verde | |
| Att1 | C1 | AG1 | | | | | | |
| Att1 | C1 | AG1 | K1 | | | | | Regno Unito |
| Att1 | C1 | AG1 | K2 | | | | Rosso | AU |
| Att1 | C1 | AG1 | K3 | | | | Blu | DE |
| Att1 | C1 | AG1 | | A1 | | | | |
| Att1 | C1 | AG1 | | A1 | | | Rosso | |
| Att1 | C1 | AG1 | | | P1 | | Rosso | AU |
| Att1 | C1 | AG1 | | | P2 | | Blu | DE |

## Rimuovere i valori di classificazione delle etichette dai componenti dell’account {#classification-values-remove}

Se si rimuove un valore di classificazione, viene rimossa l’associazione con il componente account e tutti i suoi componenti figlio. I dati del rapporto per il valore di classificazione non sono più disponibili per tali componenti. La rimozione di un valore di classificazione non comporta l’eliminazione del valore né dei componenti dell’account.

>[!NOTE]
>
>Per eliminare un valore da una classificazione etichetta, vedere &quot;[Eliminare i valori di classificazione etichetta](#classification-values-delete).&quot;

1. Aprire la visualizzazione entità dal menu **[!UICONTROL Manage]** o **[!UICONTROL Target]**.

1. Selezionare la casella di controllo accanto a ogni riga pertinente.

   Per suggerimenti sulla selezione di più righe, vedere &quot;[Selezionare più righe](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**.

1. Selezionare la casella di controllo accanto a ogni valore di classificazione da rimuovere dalle entità selezionate.<!-- As of 2/24/26, no way to tell which entity each value is assigned to -->

   Per selezionare tutti i valori assegnati, scegliere **[!UICONTROL Select All]**. Per deselezionare tutti i valori assegnati, scegliere **[!UICONTROL Deselect All]**.

1. Fare clic su **[!UICONTROL Unassign Selected]**.

## Elimina valori di classificazione delle etichette {#classification-values-delete}

L’eliminazione dei valori di classificazione delle etichette ne rende impossibile l’utilizzo futuro e i dati del rapporto non sono più disponibili per tali valori. Tutte le assegnazioni tra i valori e le relative classificazioni dell’etichetta principale e specifici componenti dell’account vengono rimosse, ma le classificazioni dell’etichetta principale e i componenti della campagna non vengono eliminati.

>[!NOTE]
>
>Per dissociare semplicemente un valore di classificazione da un componente account, vedere &quot;[Rimuovere i valori di classificazione delle etichette dai componenti account](#classification-values-remove).&quot;

1. Fare clic su **[!UICONTROL Reports]>[!UICONTROL Label Classifications]**.

1. Fare clic sulla scheda **[!UICONTROL Label Values]**.

1. (Facoltativo) Filtra l’elenco per includere valori di etichetta specifici.

1. Selezionare la casella di controllo accanto a ogni valore di etichetta da eliminare.

   Puoi eliminare fino a 200 righe alla volta.

   Per suggerimenti sulla selezione di più righe, vedere &quot;[Selezionare più righe](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Nella barra degli strumenti Azioni in blocco, fare clic su ![Elimina](/help/search-social-commerce/assets/delete.png "Elimina").

1. Nel messaggio di conferma, fare clic su **[!UICONTROL Confirm]**.

## Eliminare le classificazioni delle etichette

L’eliminazione di una classificazione rimuove tutte le associazioni tra i relativi valori figlio e i componenti conto. Una classificazione eliminata e i relativi valori non sono disponibili per un utilizzo futuro. I dati del rapporto per i valori di classificazione non sono più disponibili.

>[!NOTE]
>
>Per dissociare semplicemente un valore di classificazione da un componente account, vedere &quot;[Rimuovere i valori di classificazione delle etichette dai componenti account](#classification-values-remove).&quot;

1. Fare clic su **[!UICONTROL Reports]>[!UICONTROL Label Classifications]**.

1. (Facoltativo) Filtra l’elenco per includere specifiche classificazioni di etichette.

1. Selezionare la casella di controllo accanto a ogni classificazione di etichetta da eliminare.

   Puoi eliminare fino a 200 righe alla volta.

   Per suggerimenti sulla selezione di più righe, vedere &quot;[Selezionare più righe](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Nella barra degli strumenti Azioni in blocco, fare clic su ![Elimina](/help/search-social-commerce/assets/delete.png "Elimina").

1. Nel messaggio di conferma, fare clic su **[!UICONTROL Confirm]**.
