---
title: Gestire i posizionamenti
description: Scopri come creare e gestire posizionamenti Google Ads e posizionamenti negativi e assegnare vincoli ai posizionamenti.
feature: Search Optimization, Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: ae57d55f-b168-5358-b114-c3974b1b3d77
    internal-label: Search Optimization
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
    internal-label: Campaign management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 3bb565d689b65ae66d6ea2094abccdff3c9e891d
workflow-type: tm+mt
source-wordcount: '1383'
ht-degree: 0%
---
# Gestire i posizionamenti

*funzionalità Beta*

Solo *[!DNL Google Ads]account*

I posizionamenti sono posizioni sulla rete di visualizzazione in cui possono essere visualizzati gli annunci. Le impostazioni di posizionamento includono l’offerta massima e i parametri di tracciamento facoltativi. Le impostazioni a livello di posizionamento sostituiscono le impostazioni del gruppo di annunci o della campagna. I posizionamenti negativi impediscono la visualizzazione degli annunci su siti specifici.

Dopo aver [reso accessibile un account di rete tramite una connessione API](/help/search-social-commerce/new-ui/manage/accounts/api-accounts/api-account-manage.md) e dopo che Search, Social e Commerce hanno sincronizzato i dati dell&#39;account con la rete di annunci, puoi creare posizionamenti per gruppi di annunci in [tipi di campagne supportati](/help/search-social-commerce/introduction/supported-inventory.md) destinati alla rete di visualizzazione. È inoltre possibile modificare e modificare lo stato dei posizionamenti, nonché creare ed eliminare posizionamenti negativi.

>[!NOTE]
>
>[!DNL Google Ads] non fornisce dati sulle prestazioni a livello di annuncio per i posizionamenti.

## Informazioni sulla visualizzazione [!UICONTROL Placements] {#placement-view-about}

La visualizzazione [!UICONTROL Targeting] > [!UICONTROL Placements] include due schede per l&#39;account dell&#39;inserzionista selezionato:

* Nella scheda [!UICONTROL Placements] sono elencati tutti i posizionamenti che è possibile fare offerte nella visualizzazione filtrata.

* Nella scheda [!UICONTROL Negatives] sono elencati tutti i posizionamenti negativi nella visualizzazione filtrata.

La visualizzazione della pagina richiede l&#39;autorizzazione [!UICONTROL View Placements]. La creazione di posizionamenti o posizionamenti negativi, la modifica di posizionamenti, la modifica dello stato di posizionamento e l&#39;eliminazione di posizionamenti o posizionamenti negativi richiede l&#39;autorizzazione [!UICONTROL Edit Placements].

### Azioni disponibili

* [Creare i posizionamenti](#placement-create)

* [Creare posizionamenti negativi](#placement-negative-create)

* [Modificare le impostazioni di posizionamento](#placement-edit)

* [Modificare o eliminare lo stato dei posizionamenti e dei posizionamenti negativi](#placement-status)

* [Copia tutti i dati nelle righe selezionate negli Appunti](#copy-to-clipboard)

* [Assegnare vincoli ai posizionamenti e annullare l’assegnazione di vincoli dai posizionamenti](#placement-constraints)

* [Assegnare le classificazioni delle etichette ai posizionamenti](/help/search-social-commerce/new-ui/set-up/label-classifications-manage.md)

## Creare i posizionamenti {#placement-create}

>[!TIP]
>
>Per creare un numero elevato di posizionamenti contemporaneamente, utilizza [bulksheet campagna](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. Nel menu principale, fare clic su **[!UICONTROL Targeting]>[!UICONTROL Placements]**.

1. Nella scheda **[!UICONTROL Placements]**, fare clic su **[!UICONTROL Create Placement]**.

1. Nel passaggio **[!UICONTROL Basic Settings]**, seleziona la rete, l&#39;account, la campagna e il gruppo di annunci.

1. Immetti le [impostazioni di posizionamento](#placement-create-settings).

   Per creare più posizionamenti, separa gli URL del sito web con virgole.

1. Fare clic su **[!UICONTROL Review and Save]**.

1. Se necessario, fai clic su ![Modifica](/help/search-social-commerce/assets/edit-new.png "Modifica") **[!UICONTROL Edit]** e modifica l&#39;entità e/o le impostazioni di posizionamento.

1. Fare clic su **[!UICONTROL Create]**.

## Creare posizionamenti negativi {#placement-negative-create}

È possibile creare posizionamenti negativi per una campagna [!DNL Google Ads] o un gruppo di annunci destinati alla rete di visualizzazione.

>[!NOTE]
>
>È inoltre possibile creare e modificare posizionamenti negativi nelle [impostazioni gruppo di annunci](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-manage.md) e [impostazioni campagna](/help/search-social-commerce/new-ui/manage/campaigns/campaign-manage.md).

>[!TIP]
>
>Per creare un numero elevato di posizionamenti negativi contemporaneamente, utilizzare [bulksheet campagna](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. Nel menu principale, fare clic su **[!UICONTROL Targeting]>[!UICONTROL Placements]**.

1. Nella scheda **[!UICONTROL Negatives]** fare clic su **[!UICONTROL Create Negative]** e quindi su **[!UICONTROL Campaign Negative]** o **[!UICONTROL Ad Group Negative]**.

1. Nel passaggio **[!UICONTROL Basic Settings]**, seleziona la rete, l’account, la campagna e (per i posizionamenti negativi a livello di gruppo di annunci) il gruppo di annunci.

1. Nel passaggio **[!UICONTROL Manage Websites]** immettere gli URL negativi del sito Web, ad esempio `www.example.com` o `example.com/shoes`.

   Separa più URL con virgole. Questo modulo accetta gli URL del sito Web, non le stringhe di argomenti o categorie.

1. Fare clic su **[!UICONTROL Review and Save]**.

1. Se necessario, fai clic su ![Modifica](/help/search-social-commerce/assets/edit-new.png "Modifica") **[!UICONTROL Edit]** e modifica l&#39;entità e/o gli URL negativi del sito Web.

1. Fare clic su **[!UICONTROL Create]**.

## Modificare le impostazioni di posizionamento {#placement-edit}

Puoi modificare lo stato, l’offerta, l’URL di base e il modello di tracciamento per uno o più posizionamenti. Non puoi modificare l’URL del sito web di destinazione o modificare i posizionamenti eliminati.

>[!TIP]
>
>Per modificare una grande quantità di dati di posizionamento contemporaneamente, utilizza [bulksheet campagna](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. Nel menu principale, fare clic su **[!UICONTROL Targeting]>[!UICONTROL Placements]**.

1. Nella scheda **[!UICONTROL Placements]** selezionare la casella di controllo accanto a ogni posizionamento da modificare.

1. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL Edit]**.

1. Nel pannello **[!UICONTROL Edit Placements]**, modifica le [impostazioni di posizionamento](#placement-edit-settings).

   Per più posizionamenti, le modifiche vengono applicate a tutti i posizionamenti selezionati. Puoi impostare le offerte su un valore specificato oppure aumentarle o diminuirle di una percentuale o di un importo monetario specificato, con un limite. Per gli URL, puoi sostituire il valore esistente, trovare e sostituire il testo, aggiungere un prefisso o aggiungere un suffisso.

   La modifica delle offerte è disabilitata quando i posizionamenti selezionati utilizzano più valute.

1. Fare clic su **[!UICONTROL Save]**.

## Modificare lo stato dei posizionamenti e dei posizionamenti negativi {#placement-status}

Puoi mettere in pausa un posizionamento attivo e su cui fare offerte per disabilitare l’offerta. In seguito puoi riprendere l’offerta riportando lo stato attivo.

È inoltre possibile eliminare posizionamenti attivi o in pausa o posizionamenti negativi. I posizionamenti eliminati vengono eliminati dalla rete di annunci. Sono ancora visibili quando li includi nel filtro dati, ma non puoi modificarli.

### Attivare o sospendere i posizionamenti

1. Nel menu principale, fare clic su **[!UICONTROL Targeting]>[!UICONTROL Placements]**.

1. Nella scheda **[!UICONTROL Placements]**, filtrare l&#39;elenco e quindi selezionare la casella di controllo accanto a ogni posizionamento di cui si desidera modificare lo stato.

1. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL Edit]**.

1. Nella sezione **[!UICONTROL Placement Details]**, modifica **[!UICONTROL Status]**:

   * Per attivare i posizionamenti in pausa, selezionare **[!UICONTROL Active]**.

   * Per sospendere i posizionamenti attivi, selezionare **[!UICONTROL Paused]**.

1. Fare clic su **[!UICONTROL Save]**.

### Elimina posizionamenti o posizionamenti negativi

1. Nel menu principale, fare clic su **[!UICONTROL Targeting]>[!UICONTROL Placements]**.

1. Nella scheda **[!UICONTROL Placements]** o **[!UICONTROL Negatives]**, filtrare l&#39;elenco e quindi selezionare la casella di controllo accanto a ogni posizionamento o posizionamento negativo da eliminare.

1. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL Delete]**.

1. Nel messaggio di conferma, fare clic su **[!UICONTROL Confirm]**.

## Copia tutti i dati nelle righe selezionate negli Appunti {#copy-to-clipboard}

Copiare le informazioni visibili nelle righe selezionate, in base ai filtri applicati e alle colonne visibili nella vista. Le informazioni vengono salvate come valori separati da tabulazioni (TSV).

1. Selezionare la casella di controllo accanto a ogni riga di cui si desidera copiare i dati.

1. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL Copy]**.

## Gestire le assegnazioni di vincoli per i posizionamenti {#placement-constraints}

Puoi assegnare e rimuovere i vincoli di offerta per campagne, gruppi di annunci, parole chiave, posizionamenti, gruppi di prodotti a livello di unità e target di ricerca dinamica. Ogni entità può avere un solo vincolo.

I vincoli vengono ereditati dalle entità figlio, pertanto non è necessario assegnare vincoli alle entità figlio a meno che non si desideri sostituire i valori ereditati.

L’annullamento dell’assegnazione di un vincolo rimuove l’associazione con i componenti conto e tutti i relativi componenti figlio e i dati del rapporto relativi al vincolo non sono più disponibili per tali componenti. L’annullamento dell’assegnazione di un vincolo non comporta l’eliminazione del vincolo o dei componenti del conto stessi.

>[!NOTE]
>
>* Se successivamente modificate una parola chiave o la copia dell&#39;annuncio per un annuncio non modificabile, creando in tal modo una nuova parola chiave o un nuovo annuncio, il vincolo non viene assegnato alla nuova entità.
>* I vincoli attivi limitano le offerte solo per le unità di offerta assegnate nei portfolio legacy ottimizzati a livello di parola chiave. Vengono ignorate per le unità di offerta presenti in portafogli attivi, in portafogli ibridi o che non appartengono a portafogli.

### Assegnare un vincolo ai posizionamenti {#placement-constraint-assign}

È possibile assegnare un singolo vincolo a uno o più posizionamenti.

1. Nel menu principale, fare clic su **[!UICONTROL Targeting]>[!UICONTROL Placements]**.

1. Nella scheda **[!UICONTROL Placements]** selezionare la casella di controllo accanto a ogni posizione a cui assegnare un singolo vincolo.

1. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL Assign]>[!UICONTROL Bid Constraint]**.

1. Selezionate il vincolo.

1. Fare clic su **[!UICONTROL Assign Now]**.

### Annullare l’assegnazione di vincoli ai posizionamenti {#placement-constraint-unassign}

L&#39;annullamento dell&#39;assegnazione di un vincolo non ne comporta l&#39;eliminazione. Per eliminare un vincolo rendendolo non disponibile per un utilizzo futuro, vedere &quot;[Gestire i vincoli per le unità di offerta di ricerca](/help/search-social-commerce/new-ui/goals/constraints-manage.md#constraint-change-status).&quot;

1. Nel menu principale, fare clic su **[!UICONTROL Targeting]>[!UICONTROL Placements]**.

1. Nella scheda **[!UICONTROL Placements]** selezionare la casella di controllo accanto a ogni posizionamento da cui si desidera annullare l&#39;assegnazione dei vincoli.

1. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL Unassign]>[!UICONTROL Bid Constraint]**.

1. Fare clic su **[!UICONTROL Confirm]**.

## Impostazioni di posizionamento {#placement-settings}

### Impostazioni durante la creazione di posizionamenti {#placement-create-settings}

#### [!UICONTROL Basic Settings]

**[!UICONTROL Network]:** La rete di annunci. Solo [!DNL Google Ads] è supportato.

**[!UICONTROL Account]:** L&#39;account di rete dell&#39;annuncio.

**[!UICONTROL Campaign]:** La campagna.

**[!UICONTROL Ad Group]:** Il gruppo di annunci.

#### [!UICONTROL Placement Details]

**[!UICONTROL Placements]:** siti nella rete di visualizzazione in cui può essere visualizzato l&#39;annuncio. Immettere un URL del sito Web valido, ad esempio `www.example.com`, `example.com` o `example.com/shoes`. Separa più URL con virgole. L&#39;URL non può includere un punto interrogativo (`?`).

Per escludere invece i siti Web, [crea posizionamenti negativi](#placement-negative-create) dalla scheda [!UICONTROL Targeting] > [!UICONTROL Placements] > [!UICONTROL Negatives] oppure utilizza le impostazioni del gruppo di annunci e della campagna.

**[!UICONTROL Status]:** Lo stato di visualizzazione del posizionamento: *[!UICONTROL Active]* (per abilitare l&#39;offerta) o *[!UICONTROL Paused]* (per disabilitare l&#39;offerta).

#### [!UICONTROL Bids]

**[!UICONTROL Bid]:** (facoltativo) il costo massimo per clic (CPC) o il costo per mille impression visualizzabili (vCPM) per l&#39;annuncio basato sul posizionamento, a seconda della strategia di offerta della campagna. Questo valore sostituisce l&#39;offerta a livello di gruppo di annunci.

#### [!UICONTROL Tracking URLs]

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

{{$include /help/_includes/base-url-google-note.md}}

{{$include /help/_includes/tracking-template-google.md}}

>[!NOTE]
>
>Il modulo di creazione della nuova interfaccia utente richiede che l&#39;URL di base e il modello di tracciamento, se specificato, inizino con `http://` o `https://`.

### Impostazioni durante la modifica dei posizionamenti {#placement-edit-settings}

Il pannello [!UICONTROL Edit Placements] supporta le seguenti impostazioni per uno o più posizionamenti selezionati. Non puoi modificare l’URL del sito web di destinazione.

#### [!UICONTROL Placement Details]

**[!UICONTROL Status]:** *[!UICONTROL Active]* o *[!UICONTROL Paused]*.

#### [!UICONTROL Bid Details]

**[!UICONTROL Bid adjustment]:** Come modificare l&#39;offerta:

* *[!UICONTROL Set to]:* Sostituisci l&#39;offerta esistente con un valore specificato.

* *[!UICONTROL Increase]:* Aumenta l&#39;offerta esistente di un importo o di una percentuale specificata.

* *[!UICONTROL Decrease]:* Diminuisci l&#39;offerta esistente di un importo o di una percentuale specificata.

**[!UICONTROL Modifier type]:** (per aumenti o diminuzioni) Se l&#39;adeguamento utilizza *[!UICONTROL Currency]* o *[!UICONTROL Percentage]*.

**[!UICONTROL Set value]:** La nuova offerta o l&#39;importo dell&#39;adeguamento. Il valore minimo è 0,01.

**[!UICONTROL Max limit]:** (per aumenti o diminuzioni; facoltativo) Il limite per l&#39;offerta adeguata. Per un aumento, questa è l’offerta massima; per una diminuzione, questa è l’offerta minima. Il valore limite minimo è 0,01.

La modifica delle offerte è disabilitata quando i posizionamenti selezionati utilizzano più valute.

#### [!UICONTROL Tracking Urls]

**[!UICONTROL Base Url]**, **[!UICONTROL Tracking Template]:** Per ogni campo, selezionare la modalità di modifica del valore:

* *[!UICONTROL Set To]:* Sostituisci il valore. Immettere un URL del sito Web valido che inizi con `http://` o `https://`.

* *[!UICONTROL Find/Replace]:* Sostituisci il testo specificato all&#39;interno del valore. Immettere il testo da trovare e il testo sostitutivo.

* *[!UICONTROL Add Suffix]:* Aggiungi testo al valore. Immettere il testo del suffisso.

* *[!UICONTROL Add Prefix]:* Aggiungi testo all&#39;inizio del valore. Immettere il testo del prefisso.

>[!NOTE]
>
>Tutti i nuovi URL di base devono essere URL validi che iniziano con `http://` o `https://`.

>[!MORELIKETHIS]
>
>* [Gestione dei vincoli per le unità delle offerte di ricerca](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [Gestisci classificazioni etichette](/help/search-social-commerce/new-ui/set-up/label-classifications-manage.md)
