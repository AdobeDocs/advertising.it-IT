---
title: Gestire i gruppi di prodotti
description: Scopri come creare, modificare ed eliminare i gruppi di prodotti per lo shopping e fai riferimento alle impostazioni del gruppo di prodotti per Google Ads e Microsoft Advertising.
feature: Search Campaign Management
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: c074f430583e2d320eb4d47b4fc956c1822bd04a
workflow-type: tm+mt
source-wordcount: 2337
ht-degree: 0%

---


# Gestire i gruppi di prodotti

Solo *[!DNL Google Ads]e [!DNL Microsoft Advertising] campagne acquisti*

È possibile creare e gestire gruppi di prodotti nella visualizzazione [!UICONTROL Product Groups] in [!UICONTROL Assets] > [!UICONTROL Shopping].

Puoi visualizzare i dati sui gruppi di prodotti in [ il [!UICONTROL Product Group Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/product-group-report.md).

## Cosa sono i gruppi di prodotti?

Nelle campagne di acquisto, i gruppi di prodotti, non le parole chiave, determinano i prodotti nell’account del centro commerciale per cui vengono visualizzati gli annunci di acquisto. Ogni gruppo di prodotti è basato su un singolo attributo di prodotto (ad esempio categoria, tipo di prodotto, marchio, condizione, ID prodotto o etichette personalizzate) e utilizza la stessa offerta per tutti i prodotti corrispondenti. Puoi includere o escludere offerte per i prodotti di ogni gruppo.

Puoi configurare i gruppi di prodotti a livello di gruppo di annunci per determinare quali prodotti negli account del centro commerciale vengono visualizzati negli annunci commerciali per il gruppo di annunci. Anche se il gruppo di annunci non include entità pubblicitarie, la rete pubblicitaria visualizza comunque gli annunci per i prodotti.

Se lo stesso prodotto è incluso in più campagne, il network pubblicitario utilizza innanzitutto la priorità della campagna per determinare quale campagna (e l’offerta associata) è idonea per l’asta degli annunci. Se tutte le campagne hanno la stessa priorità, la campagna con l’offerta più elevata è idonea.

Per ulteriori informazioni sulle [!DNL Google] campagne e annunci di acquisto, consulta &quot;[Implementare [!DNL Google Ads] campagne di acquisto](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)&quot; e la [documentazione di Google Ads](https://support.google.com/google-ads/answer/3455481?visit_id=638205553638977410-2592024034&rd=1). Per ulteriori informazioni sulle [!DNL Microsoft] campagne di acquisto, consulta &quot;[Implementare [!DNL Microsoft Advertising] campagne acquisti](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)&quot; e la [[!DNL Microsoft Advertising] documentazione](https://help.bingads.microsoft.com/#apex/3/en/50903/1-500).

>[!NOTE]
>
>Il supporto non è disponibile per [!DNL Google Ads] gruppi di elenchi nelle campagne con prestazione massima. Per gestire e visualizzare i dati per l&#39;elenco dei gruppi, utilizzare l&#39;editor [!DNL Google Ads].

### Gerarchia dei gruppi di prodotti

Prima di poter creare gruppi di prodotti con attributi specifici per un gruppo di annunci, è necessario creare un gruppo di prodotti completo denominato &quot;[!UICONTROL All Products]&quot;. Da questo gruppo di prodotti principale, è possibile creare gruppi di prodotti secondari per sottoinsiemi di prodotti e i nipoti dai gruppi di prodotti secondari. Dopo aver creato il primo gruppo di prodotti figlio per un gruppo di annunci, viene creato automaticamente un altro gruppo di prodotti denominato &quot;[!UICONTROL Everything Else]&quot; utilizzando l&#39;offerta del gruppo di annunci predefinito. Quando si aggiungono altri gruppi di prodotti, il gruppo &quot;[!UICONTROL Everything Else]&quot; viene regolato di conseguenza in modo che costituisca tutti i prodotti che non fanno parte di un altro gruppo di prodotti.

All&#39;interno di un gruppo di annunci, è possibile creare fino a sette livelli di gruppi di prodotti (escluso &quot;[!UICONTROL All Products]&quot;) per includere o escludere la partecipazione, con uno o più gruppi di prodotti che utilizzano lo stesso attributo in ogni livello (ad esempio, [!UICONTROL Brand]=Acme per un gruppo di prodotti e [!UICONTROL Brand]=AcmePlus per un altro allo stesso livello). I gruppi di prodotti padre sono denominati suddivisioni e il livello di suddivisione più basso è denominato unità. Puoi impostare le offerte e i modelli di tracciamento, o escludere completamente le offerte, a livello di unità. L’intero set di gruppi di prodotti attivi per un gruppo di annunci viene applicato in modo gerarchico per determinare i prodotti idonei. Ad esempio, se si suddivide [!UICONTROL All Products] in [!UICONTROL Brand]=AcmeBasic e [!UICONTROL Brand]=AcmePlus e poi si suddivide ulteriormente ciascuno di questi gruppi di prodotti in [!UICONTROL Condition]=nuovi e si impostano le offerte, solo i nuovi prodotti con i marchi AcmeBasic e AcmePlus possono essere pubblicizzati o esclusi dagli annunci.

![Esempio di set di gruppi di prodotti](/help/search-social-commerce/assets/product-group-list-new.png "Esempio di set di gruppi di prodotti")

![Gerarchia di gruppi di prodotti di esempio](/help/search-social-commerce/assets/product-group-tree-new.png "Gerarchia di gruppi di prodotti di esempio")

### Filtri di prodotto {#product-filters}

<!-- I should be able to point to help in GGL and MS -->

Vedere anche la Guida di [!DNL Google Ads] &quot;[Gestire una campagna acquisti con gruppi di prodotti](https://support.google.com/google-ads/answer/6275317)&quot; e la Guida di [!DNL Microsoft Advertising] &quot;[Comprendere e utilizzare i gruppi di prodotti](https://help.ads.microsoft.com/#apex/bae/en/56782).&quot;

| Rete acquisti | Dimension del prodotto | Attributi | Note |
|----|----|----|----|
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!DNL Google Ads]: [!UICONTROL Category=]<br><br>Microsoft: da [!UICONTROL Category 1=] a [!UICONTROL Category 5=] | \[ID categoria\] | — |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!UICONTROL Brand=] | \[Il marchio\] | — |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!UICONTROL Item ID=] | \[ID elemento\] | — |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!UICONTROL Condition] | [!UICONTROL New], [!UICONTROL Used], [!UICONTROL Refurbished], [!UICONTROL Unknown] | — |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!DNL Google Ads]: da [!UICONTROL Product Type (1st level)=] a [!UICONTROL Product Type (5th level)=]<br><br>[!DNL Microsoft]: [!UICONTROL Product Type=] | \[Il tipo di prodotto\] | — |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | Da [!UICONTROL Custom Label 0=] a [!UICONTROL Custom Label 4=] | \[Attributo per l&#39;etichetta personalizzata\] | — |
| [!DNL Google Ads] | Channel= Canale | [!UICONTROL Local], [!UICONTROL Online] | Per visualizzare gli annunci solo per i prodotti locali o online.<br><br><b>Nota:</b> Per creare annunci per i prodotti locali, è necessario attivare l&#39;opzione &quot;Annunci inventario locali&quot; e partecipare al programma di acquisto locale con [!DNL Google Merchant Center]. |
| [!DNL Google Ads] | [!UICONTROL ChannelExclusivity=] | [!UICONTROL SingleChannel], [!UICONTROL MultiChannel] | Indica se mostrare gli annunci per i prodotti disponibili solo per un singolo canale (solo locale o solo online) o per più canali (sia locali che online). |

## Visualizzazione [!UICONTROL Product Groups]

La visualizzazione [!UICONTROL Product Groups] in [!UICONTROL Assets] > [!UICONTROL Shopping] elenca tutti i gruppi di prodotti nella visualizzazione filtrata per l&#39;account dell&#39;inserzionista selezionato. Puoi anche creare e gestire gruppi di prodotti.

### Azioni disponibili <!-- Go through all -->

* [Crea un gruppo di prodotti [!UICONTROL All Products]](#product-group-create-all-products)

* [Creare un nodo gruppo di prodotti figlio in un gruppo di prodotti esistente](#node-add)

* Modificare le impostazioni per un nodo gruppo di prodotti:

  * [Modifica eventuali impostazioni](#node-edit)

  * [Modifica solo [!UICONTROL Tracking Template]](#node-edit-tracking-template)

  * [Modifica solo [!UICONTROL Max CPC]](#node-edit-maxcpc)

* [Eliminare un nodo gruppo di prodotti](#node-delete)

* [Assegna vincoli](#constraint-assign) ai gruppi di prodotti e [rimuovi vincoli](#constraint-unassign) dai gruppi di prodotti

* [Assegna classificazioni etichette](#classification-values-assign) ai gruppi di prodotti e [rimuovi classificazioni etichette](#classification-values-remove) dai gruppi di prodotti

>[!NOTE]
>
>Puoi creare e modificare grandi quantità di dati sui gruppi di prodotti (comprese etichette e assegnazioni di vincoli) contemporaneamente caricando [file bulksheet](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md) e pubblicandoli sulla rete di annunci.

## Crea un gruppo di prodotti [!UICONTROL All Products] {#product-group-create-all-products}

Prima di poter creare gruppi di prodotti con attributi specifici, è necessario creare un gruppo di prodotti completo denominato &quot;[!UICONTROL All Products]&quot;. Ogni gruppo di annunci può avere un solo gruppo &quot;[!UICONTROL All Products]&quot;.

>[!TIP]
>
>Per creare più componenti account contemporaneamente, utilizza [bulksheet campagna](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Nel menu principale, fare clic su **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. Nella barra degli strumenti sopra la tabella dati, fare clic su **[!UICONTROL Create Product Group]**.

1. Selezionare la rete di annunci, l&#39;account, la campagna e il gruppo di annunci, quindi fare clic su **[!UICONTROL Continue]**.

1. Specifica le [impostazioni del gruppo di prodotti Google Ads](#google-ads-product-group-settings) o [impostazioni del gruppo di prodotti Microsoft Advertising](#microsoft-advertising-product-group-settings).

1. Fare clic su **[!UICONTROL Review and Save]**.

1. Se necessario, fai clic su ![Modifica](/help/search-social-commerce/assets/edit-new.png "Modifica") e modifica le [impostazioni del gruppo di prodotti Google Ads](#google-ads-product-group-settings) o le [impostazioni del gruppo di prodotti Microsoft Advertising](#microsoft-advertising-product-group-settings).

1. Fare clic su **[!UICONTROL Create]**.

## Creare un nodo gruppo di prodotti figlio in un gruppo di prodotti esistente {#product-group-create-child}

Dopo aver creato almeno un gruppo &quot;[!UICONTROL All Products]&quot; completo per un gruppo di annunci, è possibile creare nodi gruppo di prodotti figlio per sottoinsiemi di prodotti da includere o escludere dalla gara, con uno o più gruppi di prodotti che hanno come target lo stesso attributo in ogni livello (ad esempio, [!UICONTROL Brand]=Acme per un gruppo di prodotti e [!UICONTROL Brand]=AcmePlus per un altro allo stesso livello. È possibile creare fino a sette livelli di nodi del gruppo di prodotti figlio, escluso &quot;[!UICONTROL All Products]&quot;.

>[!NOTE]
>
>Impossibile creare un gruppo di prodotti figlio per un gruppo di prodotti &quot;[!UICONTROL Everything Else]&quot;.

1. Nel menu principale, fare clic su **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. (Facoltativo) Per visualizzare un gruppo di prodotti e i relativi nodi figlio nella visualizzazione Struttura, posizionare il cursore sul nome del gruppo di prodotti e fare clic su **[!UICONTROL ...]>[!UICONTROL Tree View]**.

1. Posizionare il cursore sul nome del gruppo di prodotti e fare clic su **[!UICONTROL ...]>[!UICONTROL + Add Node]**.

1. Specifica le [impostazioni del gruppo di prodotti Google Ads](#google-ads-product-group-settings) o [impostazioni del gruppo di prodotti Microsoft Advertising](#microsoft-advertising-product-group-settings).

1. Fare clic su **[!UICONTROL Center]**.

## Modificare le impostazioni per un nodo gruppo di prodotti {#node-edit}

Puoi modificare il modello di offerta e tracciamento per i nodi del gruppo di prodotti di unità (gruppi di prodotti senza nodi del gruppo di prodotti figlio) inclusi per un gruppo di annunci. Non è possibile modificare alcuna informazione per i gruppi di prodotti di unità esclusi o per i nodi di suddivisione inclusi o esclusi, che sono gruppi di prodotti con nodi di gruppi di prodotti figlio.

1. Nel menu principale, fare clic su **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. (Facoltativo) Per visualizzare un gruppo di prodotti e i relativi nodi figlio nella visualizzazione Struttura, posizionare il cursore sul nome del gruppo di prodotti e fare clic su **[!UICONTROL ...]>[!UICONTROL Tree View]**.

1. Posizionare il cursore sul nome del gruppo di prodotti e fare clic su **[!UICONTROL ...]>[!UICONTROL + Edit Node]**.

1. Modifica le [impostazioni del gruppo di prodotti Google Ads](#google-ads-product-group-settings) o [impostazioni del gruppo di prodotti Microsoft Advertising](#microsoft-advertising-product-group-settings).

1. Fare clic su **[!UICONTROL Update]**.

## Modifica solo [!UICONTROL Tracking Template] per un nodo gruppo di prodotti {#node-edit-tracking-template}

1. Nel menu principale, fare clic su **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. Posizionare il cursore sul nome del gruppo di prodotti e fare clic su **[!UICONTROL ...]>[!UICONTROL Tree View]** per visualizzare il gruppo di prodotti e i relativi nodi figlio nella visualizzazione Struttura.

1. Nella colonna **[!UICONTROL Tracking Template]** fare clic su ![Modifica](/help/search-social-commerce/assets/edit-new.png "Modifica").

1. Modificare il valore **[!UICONTROL Tracking Template]**, quindi fare clic su **[!UICONTROL Save]**.

## Modifica solo [!UICONTROL Max CPC] per un nodo gruppo di prodotti {#node-edit-maxcpc}

1. Nel menu principale, fare clic su **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. Posizionare il cursore sul nome del gruppo di prodotti e fare clic su **[!UICONTROL ...]>[!UICONTROL Tree View]** per visualizzare il gruppo di prodotti e i relativi nodi figlio nella visualizzazione Struttura.

1. Nella colonna **[!UICONTROL Max CPC]** fare clic su ![Modifica](/help/search-social-commerce/assets/edit-new.png "Modifica").

1. Modificare il valore **[!UICONTROL Max CPC]**, quindi fare clic su **[!UICONTROL Save]**.

## Eliminare un nodo gruppo di prodotti {#node-delete}

Puoi eliminare qualsiasi gruppo di prodotti, ad eccezione di un gruppo &quot;Tutto il resto&quot; quando esistono altri gruppi di prodotti allo stesso livello, utilizzato per determinare quali prodotti nell’account del centro commerciale sono inclusi negli annunci commerciali per il gruppo di annunci. Se si elimina un gruppo di prodotti, vengono eliminati anche tutti i gruppi di prodotti secondari.

1. Nel menu principale, fare clic su **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. Posizionare il cursore sul nome del gruppo di prodotti e fare clic su **[!UICONTROL ...]>[!UICONTROL Tree View]** per visualizzare il gruppo di prodotti e i relativi nodi figlio nella visualizzazione Struttura.

1. Fare clic nella colonna **[!UICONTROL Status]** e selezionare **[!UICONTROL Delete]**.

1. Nel messaggio di conferma, fare clic su **[!UICONTROL Delete]**.

## Assegnare un vincolo ai gruppi di prodotti selezionati {#constraint-assign}

1. Nel menu principale, fare clic su **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. Selezionare la casella di controllo accanto a ogni gruppo di prodotti a cui assegnare un singolo vincolo.

1. Nella barra degli strumenti delle azioni in blocco, fare clic su **+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Selezionate il vincolo.

1. Fare clic su **[!UICONTROL Assign Now]**.

## Rimuovi vincoli dai gruppi di prodotti selezionati {#constraint-unassign}

1. Nel menu principale, fare clic su **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. Selezionare la casella di controllo accanto a ciascun gruppo di prodotti da cui si desidera annullare l&#39;assegnazione dei vincoli.

1. Nella barra degli strumenti Azioni in blocco fare clic su **-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Fare clic su **[!UICONTROL Confirm]**.

## Assegnare valori di classificazione ai gruppi di prodotti {#classification-values-assign}

>[!NOTE]
>
>I valori delle etichette vengono ereditati dalle entità figlio, pertanto non immettere valori per le entità figlio a meno che non si desideri sostituire i valori ereditati.

1. Nel menu principale, fare clic su **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. Selezionare la casella di controllo accanto a ogni gruppo di prodotti a cui assegnare un valore di etichetta.

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

## Rimuovi i valori di classificazione delle etichette dai gruppi di prodotti {#classification-values-remove}

Se si rimuove un valore di classificazione, viene rimossa l’associazione con il componente account e tutti i suoi componenti figlio. I dati del rapporto per il valore di classificazione non sono più disponibili per tali componenti. La rimozione di un valore di classificazione non comporta l’eliminazione del valore né dei componenti dell’account.

1. Nel menu principale, fare clic su **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. Selezionare la casella di controllo accanto a ogni gruppo di prodotti da cui si rimuoverà un valore di etichetta.

   Per suggerimenti sulla selezione di più righe, vedere &quot;[Selezionare più righe](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**.

1. Seleziona la casella di controllo accanto a ciascun valore di classificazione da rimuovere dalle entità selezionate.

   Per selezionare tutti i valori assegnati, scegliere **[!UICONTROL Select All]**. Per deselezionare tutti i valori assegnati, scegliere **[!UICONTROL Deselect All]**.

1. Fare clic su **[!UICONTROL Unassign Selected]**.

## Impostazioni gruppo di prodotti [!DNL Google Ads] {#google-ads-product-group-settings}

### Gruppi di prodotti &quot;Tutti i prodotti&quot;

**[!UICONTROL Network]:** (solo nuovi gruppi di prodotti) La rete di annunci.

**[!UICONTROL Account]:** (solo per nuovi gruppi di prodotti) Il nome dell&#39;account di rete dell&#39;annuncio.

**[!UICONTROL Campaign]:** (solo nuovi gruppi di prodotti) La campagna.

**[!UICONTROL Ad Group]:** (solo nuovi gruppi di prodotti) Il gruppo di annunci.

**[!UICONTROL Condition]** o **[!UICONTROL Condition Type]:** (sola lettura) tutti i prodotti

**[!UICONTROL Condition Value]:** (solo gruppi di prodotti esistenti)  

**[!UICONTROL Bid]** o **[!UICONTROL Max CPC]:** (solo per gruppi di prodotti inclusi) Il costo massimo per clic (CPC), che è l&#39;importo più alto da pagare per un clic dell&#39;annuncio. Questo valore viene utilizzato solo per le unità senza gruppi di prodotti secondari e viene utilizzato al posto del valore a livello di gruppo di annunci.

{{$include /help/_includes/tracking-template-google.md}}

Questo modello sostituisce i modelli di livello superiore e viene utilizzato solo per le unità senza gruppi di prodotti secondari. Eventuali parametri di accodamento specificati per l’account o la campagna non sono inclusi. Eventuali parametri di accodamento specificati per l’account o la campagna non sono inclusi.

### Tutti gli altri gruppi di prodotti

**[!UICONTROL Condition Type]** e **[!UICONTROL Condition Value]:** (sola lettura per gruppi di prodotti esistenti) dimensioni prodotto di destinazione. Per i nuovi gruppi di prodotti, inserisci la dimensione in base alla quale eseguire il targeting dei prodotti e l’attributo qualificante per la categoria di informazioni selezionata (ad esempio &quot;Acme&quot; quando esegui il targeting per marchio o &quot;Nuovo&quot; quando esegui il targeting per condizione).

Dopo aver creato un gruppo di prodotti per specifiche dimensioni di prodotto (ovvero, non &quot;Tutti i prodotti&quot;), in Ricerca, Social e Commerce viene automaticamente creato un gruppo di prodotti per &quot;Tutto il resto&quot;.

Per un elenco delle dimensioni prodotto disponibili, vedi &quot;[Filtri prodotto](#product-filters)&quot;. L&#39;elenco delle dimensioni potrebbe essere limitato in base all&#39;impostazione [!UICONTROL Inventory Filter] della campagna.

**[!UICONTROL Excluded]:** (facoltativo per i nuovi gruppi di prodotti; sola lettura per i gruppi di prodotti esistenti) Esclude le offerte sugli annunci per i prodotti corrispondenti.

**[!UICONTROL Max CPC]:** (solo per gruppi di prodotti inclusi) Il costo massimo per clic (CPC), che è l&#39;importo più alto da pagare per un clic dell&#39;annuncio. Questo valore viene utilizzato solo per le unità senza gruppi di prodotti secondari e viene utilizzato al posto del valore a livello di gruppo di annunci.

<!--
 ExL can't handle the same include twice in the same file, so using a snippet for the second occurrence.

{{$include /help/_includes/tracking-template-google.md}}
-->

{{tracking-template-google}}

Questo modello sostituisce i modelli di livello superiore e viene utilizzato solo per le unità senza gruppi di prodotti secondari.

## Impostazioni gruppo di prodotti [!DNL Microsoft Advertising] {#microsoft-advertising-product-group-settings}

### Gruppi di prodotti &quot;Tutti i prodotti&quot;

**[!UICONTROL Network]:** (solo nuovi gruppi di prodotti) La rete di annunci.

**[!UICONTROL Account]:** (solo per nuovi gruppi di prodotti) Il nome dell&#39;account di rete dell&#39;annuncio.

**[!UICONTROL Campaign]:** (solo nuovi gruppi di prodotti) La campagna.

**[!UICONTROL Ad Group]:** (solo nuovi gruppi di prodotti) Il gruppo di annunci.

**[!UICONTROL Condition]** o **[!UICONTROL Condition Type]:** (sola lettura) tutti i prodotti

**[!UICONTROL Condition Value]:** (solo gruppi di prodotti esistenti)  

**[!UICONTROL Bid]** o **[!UICONTROL Max CPC]:** (solo per gruppi di prodotti inclusi) Il costo massimo per clic (CPC), che è l&#39;importo più alto da pagare per un clic dell&#39;annuncio. Questo valore viene utilizzato solo per le unità senza gruppi di prodotti secondari e viene utilizzato al posto del valore a livello di gruppo di annunci.

**[!UICONTROL Base URL]:** (solo nuovi gruppi di prodotti) Non utilizzato<!-- Not sure this is supposed to be there; it's not showing for an existing product group: {{$include /help/_includes/base-url-keyword-ad-sitelink.md}} -->

{{$include /help/_includes/tracking-template-microsoft.md}}

Questo modello sostituisce i modelli di livello superiore e viene utilizzato solo per le unità senza gruppi di prodotti secondari.

### Tutti gli altri gruppi di prodotti

**[!UICONTROL Condition Type]** e **[!UICONTROL Condition Value]:** (sola lettura per gruppi di prodotti esistenti) dimensioni prodotto di destinazione. Per i nuovi gruppi di prodotti, immetti la dimensione in base alla quale eseguire il targeting dei prodotti e l’attributo idoneo per la categoria di informazioni selezionata (ad esempio &quot;Acme&quot; quando esegui il targeting per marchio o &quot;Nuovo&quot; quando esegui il targeting per condizione).

Dopo aver creato un gruppo di prodotti per specifiche dimensioni di prodotto (ovvero, non &quot;Tutti i prodotti&quot;), in Ricerca, Social e Commerce viene automaticamente creato un gruppo di prodotti per &quot;Tutto il resto&quot;.

Per un elenco delle dimensioni prodotto disponibili, vedi &quot;[Filtri prodotto](#product-filters)&quot;. L&#39;elenco delle dimensioni potrebbe essere limitato in base all&#39;impostazione [!UICONTROL Inventory Filter] della campagna.

**[!UICONTROL Excluded]:** (facoltativo per i nuovi gruppi di prodotti; sola lettura per i gruppi di prodotti esistenti) Esclude le offerte sugli annunci per i prodotti corrispondenti.

**[!UICONTROL Max CPC]:** (solo per gruppi di prodotti inclusi) Il costo massimo per clic (CPC), che è l&#39;importo più alto da pagare per un clic dell&#39;annuncio. Questo valore viene utilizzato solo per le unità senza gruppi di prodotti secondari e viene utilizzato al posto del valore a livello di gruppo di annunci.

<!--
 ExL can't handle the same include twice in the same file, so using a snippet for the second occurrence.

{{$include /help/_includes/tracking-template-microsoft.md}}
-->

{{tracking-template-microsoft}}

Questo modello sostituisce i modelli di livello superiore e viene utilizzato solo per le unità senza gruppi di prodotti secondari.

>[!MORELIKETHIS]
>
>* [Implementa [!DNL Google Ads] campagne acquisti](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)
>* [Implementa [!DNL Microsoft Advertising] campagne acquisti](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)
>* [I [!UICONTROL Product Group Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/product-group-report.md)
