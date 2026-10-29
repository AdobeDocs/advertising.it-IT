---
title: Gestisci [!DNL Google Ads] destinazioni di ricerca dinamica
description: Scopri come creare e gestire [!DNL Google Ads] destinazioni di ricerca dinamica.
exl-id: 5ea68cab-677f-4c7e-8776-24d6546f0b15
feature: Search Campaign Management
TQID: 'https://experienceleague.adobe.com/MsSy-p-WSroc3FyiHx6kvcTohEaWOqJCzqbl91mNwK0'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
    internal-label: Campaign management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: f907f445c70ce64368dfa7e77d4cd1900ecc7113
workflow-type: tm+mt
source-wordcount: '1504'
ht-degree: 0%
---
# Gestisci [!DNL Google Ads] destinazioni di ricerca dinamica

Solo *[!DNL Google Ads]account*

È possibile creare, modificare e modificare lo stato delle destinazioni di ricerca dinamica per [!DNL Google Ads] campagne che utilizzano la rete di ricerca.

## Cosa sono le destinazioni di ricerca dinamica?

Le destinazioni di ricerca dinamica definiscono se la rete di annunci utilizza tutte o un sottoinsieme delle pagine del sito web per eseguire il targeting degli annunci di ricerca dinamica. Configurare i target di ricerca dinamica a livello di gruppo di annunci; si applicano a tutti gli annunci di ricerca dinamica nello stesso gruppo di annunci.

A seconda delle impostazioni della campagna, le destinazioni di ricerca dinamica possono essere obbligatorie o facoltative:

* È necessario creare destinazioni di ricerca dinamica quando non si specifica un dominio e una lingua del sito Web nella sezione &quot;[!UICONTROL DSA Options]&quot; della campagna.

* Facoltativamente, puoi creare destinazioni di ricerca dinamica quando specifichi un dominio del sito web e una lingua nella sezione &quot;[!UICONTROL DSA Options]&quot; della campagna.

  [!DNL Google Ads] mostra automaticamente i tuoi annunci di ricerca dinamica in base al contenuto di un sito Web specificato con queste impostazioni.

Per tenere traccia in modo ottimale delle prestazioni, configura la campagna con un gruppo di annunci per destinazione di ricerca dinamica e includi un gruppo di annunci che esegue il targeting di tutti i criteri.

Per ulteriori informazioni su [!DNL Google Ads] annunci per ricerca dinamica, vedere https://support.google.com/google-ads/answer/2471185.

## Visualizzazione [!UICONTROL Auto Targets] {#auto-target-view-about}

La vista [!UICONTROL Targeting] > [!UICONTROL Auto Targets] elenca tutte le destinazioni di ricerca dinamica nella vista filtrata per l&#39;account dell&#39;inserzionista selezionato. Puoi anche gestire i target di ricerca dinamica.

La visualizzazione dei dati richiede l&#39;autorizzazione [!UICONTROL View Auto Targets]. La creazione di destinazioni e la modifica delle relative offerte o dello stato richiede l&#39;autorizzazione [!UICONTROL Edit Auto Targets].

### Azioni disponibili

* [Creare una destinazione di ricerca dinamica](#auto-target-create)

* [Modificare le impostazioni per le destinazioni di ricerca dinamica](#auto-target-edit)

* [Modificare lo stato o eliminare le destinazioni di ricerca dinamica](#auto-target-status)

* [Copia tutti i dati nelle righe selezionate negli Appunti](#copy-to-clipboard)

* [Assegna vincoli](#constraint-assign) alle destinazioni di ricerca dinamica e [rimuovi vincoli](#constraint-unassign) dalle destinazioni di ricerca dinamica

* [Assegna classificazioni etichette](#classification-values-assign) alle destinazioni di ricerca dinamica e [rimuovi classificazioni etichette](#classification-values-remove) dalle destinazioni di ricerca dinamica

>[!NOTE]
>
>Puoi creare e modificare grandi quantità di dati di destinazione (comprese etichette e assegnazioni di vincoli) contemporaneamente caricando [file di bulksheet](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md) e inviandoli alla rete di annunci.

## Crea una destinazione di ricerca dinamica [!DNL Google Ads] {#auto-target-create}

Puoi creare destinazioni di ricerca dinamica per definire le pagine dei siti web (ovvero i domini utilizzati negli URL di visualizzazione degli annunci) il cui contenuto viene utilizzato per indirizzare gli annunci di ricerca dinamica nello stesso gruppo di annunci.

Puoi eseguire il targeting di tutte le pagine indicizzate o specificare fino a tre criteri.

>[!NOTE]
>
>Per tenere traccia in modo ottimale delle prestazioni, crea una destinazione con l&#39;opzione [!UICONTROL All] per un solo gruppo di annunci per campagna.

1. Nel menu principale, fare clic su **[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**.

1. Sopra la tabella dati, fare clic su **[!UICONTROL Create Auto Target]**.

1. In **[!UICONTROL Basic Settings]**, selezionare la rete di annunci, l&#39;account, la campagna e il gruppo di annunci.

1. Specificare le [impostazioni rimanenti per la destinazione di ricerca dinamica](#auto-target-create-settings).

1. Fare clic su **[!UICONTROL Review and Save]**.

1. Controlla le impostazioni. Per modificare le impostazioni, fare clic su ![Modifica](/help/search-social-commerce/assets/edit-new.png "Modifica") **[!UICONTROL Edit]** nella sezione applicabile e modificare le impostazioni.

1. Fare clic su **[!UICONTROL Create]**.

## Modifica impostazioni destinazione di ricerca dinamica [!DNL Google Ads] {#auto-target-edit}

Puoi modificare lo stato o l’offerta massima per una o più destinazioni di ricerca dinamica. Non puoi modificare i criteri di destinazione.

1. Nel menu principale, fare clic su **[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**.

1. Selezionare la casella di controllo accanto a ogni riga da modificare.

   Per suggerimenti sulla selezione di più righe, vedere &quot;[Selezionare più righe](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL Edit]**.

1. Nel pannello **[!UICONTROL Edit Auto Targets]**, modifica le impostazioni di [stato e offerta](#auto-target-edit-settings).

   Le modifiche vengono applicate a tutte le destinazioni selezionate. Le impostazioni che non vengono modificate mantengono i valori esistenti.

   Quando le destinazioni selezionate utilizzano più valute, la modifica delle offerte viene disabilitata. Puoi comunque modificarne lo stato.

1. Fare clic su **[!UICONTROL Save]**.

Puoi anche modificare l’offerta di un singolo target direttamente nella tabella di dati facendo clic sul valore dell’offerta.

## Modifica lo stato o elimina [!DNL Google Ads] destinazioni di ricerca dinamica {#auto-target-status}

Puoi mettere in pausa un target di ricerca dinamica attivo per interromperne l’utilizzo per gli annunci di ricerca dinamica nello stesso gruppo di annunci. In seguito, è possibile riprendere a utilizzare la destinazione riportandone lo stato attivo. Puoi anche eliminare i target di ricerca dinamica.

1. Nel menu principale, fare clic su **[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**.

1. (Facoltativo) Filtra l’elenco per includere target di ricerca dinamica specifici.

1. Effettuare una delle seguenti operazioni:

   * Per modificare lo stato di una destinazione, fare clic sul relativo valore nella colonna **[!UICONTROL Status]** e selezionare **[!UICONTROL Active]** o **[!UICONTROL Paused]**.

   * Per modificare lo stato di più destinazioni, selezionare la casella di controllo accanto a ciascuna destinazione, fare clic su **[!UICONTROL Edit]** nella barra degli strumenti Azioni in blocco, selezionare **[!UICONTROL Status]** nel pannello **[!UICONTROL Edit Auto Targets]** e quindi fare clic su **[!UICONTROL Save]**.

   * Per eliminare una o più destinazioni, selezionare la casella di controllo accanto a ciascuna destinazione, fare clic su **[!UICONTROL ...]>[!UICONTROL Delete]** nella barra degli strumenti Azioni in blocco e quindi fare clic su **[!UICONTROL Confirm]** nel messaggio di conferma.

## Copia tutti i dati nelle righe selezionate negli Appunti {#copy-to-clipboard}

Copiare le informazioni visibili nelle righe selezionate, in base ai filtri applicati e alle colonne visibili nella vista. Le informazioni vengono salvate come valori separati da tabulazioni (TSV).

1. Selezionare la casella di controllo accanto a ogni riga di cui si desidera copiare i dati.

1. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL Copy]**.

## Gestire le assegnazioni di vincoli per i target di ricerca dinamici {#constraints}

### Assegnare un vincolo ai target di ricerca dinamici {#constraint-assign}

1. Nel menu principale, fare clic su **[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**.

1. Selezionare la casella di controllo accanto a ogni destinazione di ricerca dinamica a cui assegnare un singolo vincolo.

1. Nella barra degli strumenti delle azioni in blocco, fare clic su **+[!UICONTROL Assign]** > **[!UICONTROL Bid Constraint]**.

1. Selezionate il vincolo.

1. Fare clic su **[!UICONTROL Assign Now]**.

### Rimuovere i vincoli dalle destinazioni di ricerca dinamica selezionate {#constraint-unassign}

1. Nel menu principale, fare clic su **[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**.

1. Selezionare la casella di controllo accanto a ogni destinazione di ricerca dinamica da cui si desidera annullare l&#39;assegnazione dei vincoli.

1. Nella barra degli strumenti Azioni in blocco fare clic su **-[!UICONTROL Unassign]** > **[!UICONTROL Bid Constraint]**.

1. Fare clic su **[!UICONTROL Confirm]**.

## Gestire i valori di classificazione per i target di ricerca dinamica {#classification-values}

### Assegnare valori di classificazione ai target di ricerca dinamici {#classification-values-assign}

>[!NOTE]
>
>I valori delle etichette vengono ereditati dalle entità figlio, pertanto non immettere valori per le destinazioni di ricerca dinamica a meno che non si desideri ignorare i valori ereditati.

1. Nel menu principale, fare clic su **[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**.

1. Selezionare la casella di controllo accanto a ogni destinazione di ricerca dinamica a cui assegnare un valore di etichetta.

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

### Rimuovere i valori di classificazione delle etichette dalle destinazioni di ricerca dinamica {#classification-values-remove}

Se si rimuove un valore di classificazione, viene rimossa l’associazione con il componente account e tutti i suoi componenti figlio. I dati del rapporto per il valore di classificazione non sono più disponibili per tali componenti. La rimozione di un valore di classificazione non comporta l’eliminazione del valore né dei componenti dell’account.

1. Nel menu principale, fare clic su **[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**.

1. Selezionare la casella di controllo accanto a ogni destinazione di ricerca dinamica da cui si rimuoverà un valore di etichetta.

   Per suggerimenti sulla selezione di più righe, vedere &quot;[Selezionare più righe](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**.

1. Seleziona la casella di controllo accanto a ciascun valore di classificazione da rimuovere dalle entità selezionate.

   Per selezionare tutti i valori assegnati, scegliere **[!UICONTROL Select All]**. Per deselezionare tutti i valori assegnati, scegliere **[!UICONTROL Deselect All]**.

1. Fare clic su **[!UICONTROL Unassign Selected]**.

## [!DNL Google Ads] impostazioni destinazione di ricerca dinamica {#dynamic-search-target-settings}

### Impostazioni disponibili durante la creazione {#auto-target-create-settings}

#### [!UICONTROL Auto Target Details]

**Destinazioni automatiche:** le pagine indicizzate il cui contenuto viene utilizzato per eseguire il targeting degli annunci di ricerca dinamica nel gruppo di annunci:

* *[!UICONTROL All]* (impostazione predefinita): esegue il targeting di tutte le pagine indicizzate.

* *[!UICONTROL Specific]:* esegue il targeting delle pagine che soddisfano fino a tre criteri. Selezionare un criterio e immetterne il valore. Per aggiungere un altro criterio, scegliere **[!UICONTROL And]**. I criteri sono combinati con AND, pertanto una pagina deve corrispondere a tutti i criteri specificati. Fare clic su **[!UICONTROL Reset]** per cancellare i criteri.

  * *[!UICONTROL Category]:* La categoria di contenuto [!DNL Google Ads] della pagina è uguale al valore specificato. Immetti un valore.

  * *[!UICONTROL URL]:* L&#39;URL della pagina contiene il valore specificato, ad esempio `shoes.example.com`. Immetti un URL valido.

  * *[!UICONTROL Page Title]:* Il titolo della pagina contiene il testo specificato. Immetti un valore.

  * *[!UICONTROL Page Content]:* Il contenuto della pagina contiene il testo specificato. Immetti un valore.

Non puoi modificare i criteri di destinazione dopo aver creato la destinazione.

**[!UICONTROL Status]:** Lo stato della destinazione:

* *[!UICONTROL Active]* (impostazione predefinita): abilita l&#39;offerta.

* *[!UICONTROL Paused]:* Disabilita l&#39;offerta.

**[!UICONTROL Bid]:** Il costo massimo per clic (CPC) per la destinazione. Questo valore sostituisce l&#39;offerta a livello di gruppo di annunci. Il campo è facoltativo; quando si immette un&#39;offerta, il valore minimo è 0,01 nella valuta del conto.

>[!NOTE]
>
>Se il target si trova in un portafoglio ottimizzato, l’offerta CPC specificata viene applicata per un giorno. Successivamente, la funzionalità di ottimizzazione posiziona le offerte in base ai propri calcoli.

### Impostazioni disponibili durante la modifica {#auto-target-edit-settings}

#### [!UICONTROL Auto Target Details]

**[!UICONTROL Status]:** Selezionare **[!UICONTROL Active]** o **[!UICONTROL Paused]**.

#### [!UICONTROL Bid details]

La modifica delle offerte è disabilitata quando le destinazioni selezionate utilizzano più valute.

**[!UICONTROL Bid adjustment]:** Come modificare le offerte massime:

* *[!UICONTROL Set to]:* Sostituisci ogni offerta con l&#39;importo in [!UICONTROL Set value].

* *[!UICONTROL Increase]:* Aumenta ogni offerta dell&#39;importo o della percentuale in [!UICONTROL Set value].

* *[!UICONTROL Decrease]:* riduci ogni offerta dell&#39;importo o della percentuale in [!UICONTROL Set value].

**[!UICONTROL Modifier type]:** (Per [!UICONTROL Increase] e [!UICONTROL Decrease]) Selezionare **[!UICONTROL Currency]** o **[!UICONTROL Percentage]**.

**[!UICONTROL Set value]:** La nuova offerta o l&#39;importo o la percentuale di cui modificare ogni offerta. Il valore minimo è 0,01.

**[!UICONTROL Max limit]:** (facoltativo; per [!UICONTROL Increase] e [!UICONTROL Decrease]) Un limite nella valuta dell&#39;account. Per un aumento, questa è l’offerta massima risultante. Per una riduzione, questa è l’offerta minima risultante. Quando immetti un limite, il valore minimo è 0,01.

>[!MORELIKETHIS]
>
>* [(Nuova interfaccia) Gestione dei vincoli per le unità di offerta di ricerca](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [(Nuova interfaccia) Gestione classificazioni etichette](/help/search-social-commerce/new-ui/set-up/label-classifications-manage.md)
