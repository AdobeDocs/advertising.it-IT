---
title: Gestire le parole chiave
description: Scopri come creare e gestire parole chiave che possono essere offerte o negative e assegnare vincoli alle parole chiave.
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
source-git-commit: 3bb565d689b65ae66d6ea2094abccdff3c9e891d
workflow-type: tm+mt
source-wordcount: '1265'
ht-degree: 0%
---
# Gestire le parole chiave

*funzionalità Beta*

Solo *[!DNL Google Ads], [!DNL LY Ads], [!DNL Microsoft Advertising], [!DNL Yandex] e [!DNL Baidu] account esistenti*

Una parola chiave è una parola o una frase associata a un annuncio. Le impostazioni delle parole chiave includono il tipo di corrispondenza delle parole chiave, il numero massimo di offerte da utilizzare quando l’annuncio viene attivato dalla parola chiave e (per alcune reti di annunci) i parametri di tracciamento facoltativi. Le impostazioni a livello di parola chiave prevalgono sulle impostazioni del gruppo di annunci o della campagna. Le parole chiave negative impediscono la visualizzazione degli annunci per le ricerche corrispondenti.

Dopo aver [reso accessibile un account di rete tramite una connessione API](/help/search-social-commerce/new-ui/manage/accounts/api-accounts/api-account-manage.md) e dopo che Search, Social e Commerce hanno sincronizzato i dati dell&#39;account con la rete di annunci, puoi creare parole chiave per i gruppi di annunci di ricerca in [tipi di campagne supportati](/help/search-social-commerce/introduction/supported-inventory.md). È inoltre possibile modificare e modificare lo stato delle parole chiave, nonché creare ed eliminare le parole chiave negative.

Per informazioni dettagliate sulle funzionalità disponibili per ogni rete di annunci, vedi &quot;[Inventario supportato](/help/search-social-commerce/introduction/supported-inventory.md).&quot;

## Informazioni sulla visualizzazione [!UICONTROL Keywords] {#keyword-view-about}

La visualizzazione [!UICONTROL Manage] > [!UICONTROL Keywords] include due schede per l&#39;account dell&#39;inserzionista selezionato:

* Nella scheda [!UICONTROL Keywords] sono elencate tutte le parole chiave che possono essere offerte nella visualizzazione filtrata.

* Nella scheda [!UICONTROL Negatives] sono elencate tutte le parole chiave negative nella visualizzazione filtrata.

### Azioni disponibili

* [Creare parole chiave](#keyword-create)

* [Creare parole chiave negative](#keyword-negative-create)

* [Modifica impostazioni parole chiave](#keyword-edit)

* [Modificare o eliminare lo stato delle parole chiave e delle parole chiave negative](#keyword-status)

* [Copia tutti i dati nelle righe selezionate negli Appunti](#copy-to-clipboard)

* [Assegnare vincoli alle parole chiave e annullare l&#39;assegnazione di vincoli alle parole chiave](#keyword-constraints)

* [Assegna classificazioni etichette](/help/search-social-commerce/new-ui/set-up/label-classifications-manage.md) alle parole chiave

## Creare parole chiave {#keyword-create}

>[!TIP]
>
>Per creare un numero elevato di parole chiave contemporaneamente, utilizzare [bulksheet campagna](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Keywords]**.

1. Nella scheda **[!UICONTROL Keywords]**, fare clic su **[!UICONTROL Create Keywords]**.

1. Nel passaggio **[!UICONTROL Basic Settings]**, seleziona la rete, l&#39;account, la campagna e il gruppo di annunci.

1. Immettere le [[!DNL Baidu] impostazioni per le parole chiave](keyword-settings-baidu.md), [[!DNL Google Ads] impostazioni per le parole chiave](keyword-settings-google.md), [[!DNL LY Ads] impostazioni per le parole chiave](keyword-settings-yahoo-japan.md), [[!DNL Microsoft Advertising] impostazioni per le parole chiave](keyword-settings-microsoft.md) o [[!DNL Yandex] impostazioni per le parole chiave](keyword-settings-yandex.md).

   È possibile immettere o incollare fino a 2.000 parole chiave in un&#39;unica operazione. Separare più parole chiave con virgole o immetterle su righe separate.

   >[!NOTE]
   >
   >Se le impostazioni dell’account o della campagna specificano il tracciamento solo a livello di annuncio, Search, Social e Commerce non generano il tracciamento per le parole chiave.

1. Fare clic su **[!UICONTROL Review and Save]**.

1. Se necessario, fare clic su ![Modifica](/help/search-social-commerce/assets/edit-new.png "Modifica") **[!UICONTROL Edit]** e modificare le impostazioni di entità e/o parole chiave.

1. Fare clic su **[!UICONTROL Create]**.

## Modifica impostazioni parole chiave {#keyword-edit}

Modificando il testo della parola chiave o il tipo di corrispondenza è possibile eliminare la parola chiave esistente e crearne una nuova, a seconda della rete dell’annuncio. Per ulteriori informazioni, consulta le impostazioni delle parole chiave per la tua rete di annunci.

>[!TIP]
>
>Per modificare una grande quantità di dati di parole chiave contemporaneamente, incluse parole chiave su reti di annunci diverse, utilizza [bulksheet campagna](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Keywords]**.

1. Nella scheda **[!UICONTROL Keywords]** selezionare la casella di controllo accanto a ogni parola chiave da modificare.

1. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL Edit]**.

1. Modificare le [[!DNL Baidu] impostazioni delle parole chiave](keyword-settings-baidu.md), [[!DNL Google Ads] impostazioni delle parole chiave](keyword-settings-google.md), [[!DNL LY Ads] impostazioni delle parole chiave](keyword-settings-yahoo-japan.md), [[!DNL Microsoft Advertising] impostazioni delle parole chiave](keyword-settings-microsoft.md) o [[!DNL Yandex] impostazioni delle parole chiave](keyword-settings-yandex.md).

   Per più parole chiave, è possibile modificare solo i campi comuni a tutte le parole chiave selezionate e le modifiche apportate vengono applicate a tutte le parole chiave selezionate. Per alcuni campi alfanumerici è possibile modificare i valori esistenti in un valore specificato, sostituire una stringa esistente con una stringa specificata, aggiungere un prefisso o aggiungere un suffisso. Per alcuni campi monetari, è possibile modificare i valori esistenti in un valore specificato o aumentare o diminuire l&#39;importo di una percentuale o importo monetario specificato, con un limite.

1. Fare clic su **[!UICONTROL Review and Save]**.

1. Se necessario, fare clic su ![Modifica](/help/search-social-commerce/assets/edit-new.png "Modifica") **[!UICONTROL Edit]** e modificare le impostazioni delle parole chiave.

1. Fare clic su **[!UICONTROL Update]**.

## Creare parole chiave negative {#keyword-negative-create}

Solo *[!DNL Google Ads], [!DNL LY Ads], [!DNL Microsoft Advertising] e [!DNL Baidu] account esistenti*

È possibile creare parole chiave negative per un gruppo di annunci di ricerca o una campagna che esegue il targeting della ricerca o della rete di visualizzazione/nativa.

>[!NOTE]
>
>È inoltre possibile creare e modificare le parole chiave negative nelle [impostazioni gruppo di annunci](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-manage.md) e [impostazioni campagna](/help/search-social-commerce/new-ui/manage/campaigns/campaign-manage.md).

>[!TIP]
>
>Per creare un numero elevato di parole chiave negative contemporaneamente, utilizzare [bulksheet campagna](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Keywords]**.

1. Nella scheda **[!UICONTROL Negatives]** fare clic su **[!UICONTROL Create Negatives]** e quindi su **[!UICONTROL Campaign Negative Keyword]** o **[!UICONTROL Ad Group Negative Keyword]**.

1. Seleziona la rete, l’account, la campagna e, per le parole chiave negative a livello di gruppo di annunci, il gruppo di annunci.

1. Immettete le parole chiave negative. Utilizzare la seguente sintassi, senza il segno meno (`-`):

   * Corrispondenza ampia negativa: `keyword` (non supportata da [!DNL Microsoft Advertising])

   * Corrispondenza frase negativa: `"keyword"`

   * Corrispondenza esatta negativa: `[keyword]`

   Separare più valori con virgole o immetterli su righe separate. È possibile immettere o incollare fino a 2.000 parole chiave negative in un&#39;unica operazione. Si applicano i seguenti requisiti e restrizioni:

   * Lunghezza massima dei caratteri: [!DNL Baidu]: 30 byte singolo o 15 byte doppio; [!DNL Microsoft Advertising]: 100 byte singolo o 50 byte doppio; [!DNL Google Ads] e [!DNL LY Ads]: 80 byte singolo o 40 byte doppio.

   * [!DNL Baidu] consente un solo tipo di corrispondenza per parola chiave per gruppo di annunci. Ad esempio, il gruppo di annunci 1 non può includere sia `"keyword"` che `[keyword]`.

   * [!DNL Google Ads]: ogni parola chiave può essere costituita da un massimo di 10 parole e può includere solo lettere, cifre e i seguenti caratteri speciali: spazio `# $ & _ - " [ ] ' + . / :`

1. Fare clic su **[!UICONTROL Review and Save]**.

1. Se necessario, fare clic su ![Modifica](/help/search-social-commerce/assets/edit-new.png "Modifica") **[!UICONTROL Edit]** e modificare l&#39;entità e/o le parole chiave negative.

1. Fare clic su **[!UICONTROL Create]**.

## Modificare lo stato delle parole chiave e delle parole chiave negative {#keyword-status}

Puoi mettere in pausa una parola chiave di ricerca attiva e selezionabile per disabilitare l’offerta su di essa. In seguito puoi riprendere l’offerta riportando lo stato attivo.

È inoltre possibile eliminare parole chiave di ricerca attive o in pausa o parole chiave negative. Le parole chiave eliminate vengono eliminate dalla rete di annunci. Sono ancora visibili quando li includi nel filtro dati, ma non puoi modificarli.

### Attivare o sospendere le parole chiave

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Keywords]**.

1. Nella scheda **[!UICONTROL Keywords]** filtrare l&#39;elenco e quindi selezionare la casella di controllo accanto a ogni parola chiave di cui si desidera modificare lo stato.

1. Nella barra degli strumenti delle azioni in blocco, modifica lo stato:

   * Per attivare le parole chiave in pausa, fare clic su **[!UICONTROL Activate]**.

   * Per sospendere le parole chiave attive, fare clic su **[!UICONTROL Pause]**.

### Elimina parole chiave o parole chiave negative

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Keywords]**.

1. Nella scheda **[!UICONTROL Keywords]** o **[!UICONTROL Negatives]** filtrare l&#39;elenco, se lo si desidera, e quindi selezionare la casella di controllo accanto a ogni parola chiave o parola chiave negativa da eliminare.

1. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL Delete]**.

1. Nel messaggio di conferma, fare clic su **[!UICONTROL Confirm]**.

## Copia tutti i dati nelle righe selezionate negli Appunti {#copy-to-clipboard}

Copiare le informazioni visibili nelle righe selezionate, in base ai filtri applicati e alle colonne visibili nella vista. Le informazioni vengono salvate come valori separati da tabulazioni (TSV).

1. Selezionare la casella di controllo accanto a ogni riga di cui si desidera copiare i dati.

1. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL Copy]**.

## Gestire le assegnazioni di vincoli per le parole chiave {#keyword-constraints}

Puoi assegnare e rimuovere i vincoli di offerta per campagne, gruppi di annunci, parole chiave, posizionamenti, gruppi di prodotti a livello di unità e target di ricerca dinamica. Ogni entità può avere un solo vincolo.

I vincoli vengono ereditati dalle entità figlio, pertanto non è necessario assegnare vincoli alle entità figlio a meno che non si desideri sostituire i valori ereditati.

L’annullamento dell’assegnazione di un vincolo rimuove l’associazione con i componenti conto e tutti i relativi componenti figlio e i dati del rapporto relativi al vincolo non sono più disponibili per tali componenti. L’annullamento dell’assegnazione di un vincolo non comporta l’eliminazione del vincolo o dei componenti del conto stessi.

>[!NOTE]
>
>* Se successivamente modificate una parola chiave o la copia dell&#39;annuncio per un annuncio non modificabile, creando in tal modo una nuova parola chiave o un nuovo annuncio, il vincolo non viene assegnato alla nuova entità.
>* I vincoli attivi limitano le offerte solo per le unità di offerta assegnate nei portfolio legacy ottimizzati a livello di parola chiave. Vengono ignorate per le unità di offerta presenti in portafogli attivi, in portafogli ibridi o che non appartengono a portafogli.

### Assegnare un vincolo alle parole chiave {#keyword-constraint-assign}

È possibile assegnare un singolo vincolo a una o più parole chiave.

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Keywords]**.

1. Nella scheda **[!UICONTROL Keywords]** selezionare la casella di controllo accanto a ogni parola chiave a cui assegnare un singolo vincolo.

1. Nella barra degli strumenti delle azioni in blocco, fare clic su **+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Selezionate il vincolo.

1. Fare clic su **[!UICONTROL Assign Now]**.

### Annullare l&#39;assegnazione di vincoli alle parole chiave {#keyword-constraint-unassign}

L&#39;annullamento dell&#39;assegnazione di un vincolo non ne comporta l&#39;eliminazione. Per eliminare un vincolo e renderlo non disponibile per utilizzi futuri, consulta &quot;Eliminare i vincoli per le unità di offerta di ricerca&quot; nel capitolo della Guida all’ottimizzazione su &quot;Vincoli di offerta&quot;, disponibile in Search, Social e Commerce.

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Keywords]**.

1. Nella scheda **[!UICONTROL Keywords]** selezionare la casella di controllo accanto a ogni parola chiave da cui si desidera annullare l&#39;assegnazione dei vincoli.

1. Nella barra degli strumenti Azioni in blocco fare clic su **-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Fare clic su **[!UICONTROL Confirm]**.

>[!MORELIKETHIS]
>
>* [[!DNL Baidu] impostazioni parole chiave](keyword-settings-baidu.md)
>* [[!DNL Google Ads] impostazioni parole chiave](keyword-settings-google.md)
>* [[!DNL LY Ads] impostazioni parole chiave](keyword-settings-yahoo-japan.md)
>* [[!DNL Microsoft Advertising] impostazioni parole chiave](keyword-settings-microsoft.md)
>* [[!DNL Yandex] impostazioni parole chiave](keyword-settings-yandex.md)
>* [Gestione dei vincoli per le unità delle offerte di ricerca](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [Gestisci classificazioni etichette](/help/search-social-commerce/new-ui/set-up/label-classifications-manage.md)
