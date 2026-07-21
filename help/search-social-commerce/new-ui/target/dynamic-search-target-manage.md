---
title: Gestisci [!DNL Google Ads] destinazioni ricerca dinamica
description: Scopri come creare e gestire  [!DNL Google Ads] destinazioni di ricerca dinamiche.
exl-id: 5ea68cab-677f-4c7e-8776-24d6546f0b15
feature: Search Campaign Management
TQID: 'https://experienceleague.adobe.com/MsSy-p-WSroc3FyiHx6kvcTohEaWOqJCzqbl91mNwK0'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: c074f430583e2d320eb4d47b4fc956c1822bd04a
workflow-type: tm+mt
source-wordcount: 702
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

## Visualizzazione [!UICONTROL Auto Targets]

La vista [!UICONTROL Target] > [!UICONTROL Auto Targets] elenca tutte le destinazioni di ricerca dinamica nella vista filtrata per l&#39;account dell&#39;inserzionista selezionato. Puoi anche gestire i target di ricerca dinamica.

### Azioni disponibili

<!--
* Create a dynamic search target

* Edit the settings for a dynamic search target

* Change the status of dynamic search targets
-->

* [Assegna vincoli](#constraint-assign) alle destinazioni di ricerca dinamica e [rimuovi vincoli](#constraint-unassign) dalle destinazioni di ricerca dinamica

* [Assegna classificazioni etichette](#classification-values-assign) alle destinazioni di ricerca dinamica e [rimuovi classificazioni etichette](#classification-values-remove) dalle destinazioni di ricerca dinamica

>[!NOTE]
>
>Puoi creare e modificare grandi quantità di dati di destinazione (comprese etichette e assegnazioni di vincoli) contemporaneamente caricando [file di bulksheet](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md) e inviandoli alla rete di annunci.

<!--
Not available yet:

## Create a [!DNL Google Ads] dynamic search target

You can create dynamic search targets to define pages in your websites (that is, the domains used in your ads' display URLs) whose content is used to target your dynamic search ads in the same ad group.

You can target all criteria or up to three individual criteria.

>[!NOTE]
>
>To best track performance, create an "[!UICONTROL All Targets]" target for only one ad group per campaign.

>[!TIP]
>
>To create many account components at once, use [campaign bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. In the main menu, click **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Auto Targets]**.

1. In the toolbar above the data table, click ![Create](/help/search-social-commerce/assets/add.png "Create").

1. Select the ad network, the account, the campaign, and the ad group, and then click **[!UICONTROL Continue]**.

1. Specify the [dynamic search target settings](#dynamic-search-target-settings).

1. Click **[!UICONTROL Post]**.

## Edit [!DNL Google Ads] dynamic search target settings

You can edit the status or maximum bid for a [!DNL Google Ads] dynamic search target. You can't change the criteria that are targeted.

>[!TIP]
>
>To edit large amounts of data at once, use [campaign bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. In the main menu, click **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Auto Targets]**.

1. Select the check box next to each row to edit.

   For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."

1. In the toolbar above the data table, click ![Edit](/help/search-social-commerce/assets/edit.png "Edit").

1. Specify the [dynamic search target settings](#dynamic-search-target-settings).

   For multiple targets, your changes are applied to all of the selected targets. For the [!UICONTROL Bid field], you have options to change existing values to a specified value or to either increase or decrease the amount by a specified percentage or monetary amount, with a limit.

1. Save the data:

   * (Single targets) Click **[!UICONTROL Post]**.
   
   * (Multiple ad groups) Click **[!UICONTROL Post Now]**.

## Change the status of [!DNL Google Ads] dynamic search targets

You can pause any active dynamic search target in a supported campaign type to stop using them for dynamic search ads in the same ad group. You can later use them as targets by changing the ad status back to active.

You can also delete any dynamic target.

1. In the main menu, click **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Auto Targets]**.

1. (Optional) Filter the list to include specific dynamic targets.

1. Do either of the following:
   
   * To change the status of one dynamic target, click in the **[!UICONTROL Status]** column and change the status.
   
   * To delete one or more dynamic targets, do the following:
   
     1.  Select the check box next to each dynamic target you want to delete.
     
        For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."
     
     1. In the toolbar, click ![More](/help/search-social-commerce/assets/more.png "More") and select **[!UICONTROL Delete]**.
     
     1. In the confirmation message, click **[!UICONTROL Delete]**.

## [!DNL Google Ads] dynamic search target settings {#dynamic-search-target-settings}

### [!UICONTROL Auto-Target Details]

**[!UICONTROL Auto-targets]:** (Required when you don't specify a website domain and language in the campaign's [!UICONTROL DSA Options] section; read-only for existing targets) Dynamic search targets for the ad group:

* *[!UICONTROL All Targets]* (the default): Targets all indexed pages.

* *\[Specific Targets\]:* Targets up to three criteria for the indexed pages. When you select this, you must specify the criteria by specifying information categories and specific values for which to target ads (for example, "URL contains shoes.example.com"). To specify more than one criteria, click **[!UICONTROL + And]**. Target criteria include:

  * *[!UICONTROL Category]:* To show ads for indexed pages with a specific [!DNL Google Ads] content category.

  * *[!UICONTROL URL]:* To show ads for indexed pages with a specific URL, where the value may be included anywhere within the URL.

  * *[!UICONTROL Page Title]:* To show ads for indexed pages with specific text in the page title.

  * *[!UICONTROL Page Content]:* To show ads for indexed pages with specific content.

**Status:** The status of the target settings:

* *[!UICONTROL Active]* (the default): Enables bidding.

* *[!UICONTROL Paused]:* Disables bidding.

* *[!UICONTROL Deleted]* (existing targets only): Deletes the target settings.

### [!UICONTROL Bids]

**[!UICONTROL Bid]:** The maximum cost per click (CPC) for an ad or cost per 1000 impressions (CPM) for an ad, as applicable for the ad network and campaign pricing model. This value overrides the ad group-level value.

>[!NOTE]
>
>If the target is in an optimized portfolio, then the specified CPC bid is applied for one day. Afterward, the optimization capability places bids according to its own calculations.

-->

## Assegna un vincolo alle destinazioni di ricerca dinamica selezionate dalla nuova visualizzazione [!UICONTROL Auto Targets] {#constraint-assign}

1. Nel menu principale, fare clic su **[!UICONTROL Target]>[!UICONTROL Auto Targets]**.

1. Selezionare la casella di controllo accanto a ogni destinazione di ricerca dinamica a cui assegnare un singolo vincolo.

1. Nella barra degli strumenti delle azioni in blocco, fare clic su **+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Selezionate il vincolo.

1. Fare clic su **[!UICONTROL Assign Now]**.

## Rimuovere i vincoli dalle destinazioni di ricerca dinamica selezionate dalla nuova visualizzazione [!UICONTROL Auto Targets] {#constraint-unassign}

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Auto Targets]**.

1. Selezionare la casella di controllo accanto a ogni destinazione di ricerca dinamica da cui si desidera annullare l&#39;assegnazione dei vincoli.

1. Nella barra degli strumenti Azioni in blocco fare clic su **-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Fare clic su **[!UICONTROL Confirm]**.

## Assegnare valori di classificazione ai target di ricerca dinamici {#classification-values-assign}

>[!NOTE]
>
>I valori delle etichette vengono ereditati dalle entità figlio, pertanto non immettere valori per le entità figlio a meno che non si desideri sostituire i valori ereditati.

1. Nel menu principale, fare clic su **[!UICONTROL Target]>[!UICONTROL Auto Targets]**.

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

## Rimuovere i valori di classificazione delle etichette dalle destinazioni di ricerca dinamica {#classification-values-remove}

Se si rimuove un valore di classificazione, viene rimossa l’associazione con il componente account e tutti i suoi componenti figlio. I dati del rapporto per il valore di classificazione non sono più disponibili per tali componenti. La rimozione di un valore di classificazione non comporta l’eliminazione del valore né dei componenti dell’account.

1. Nel menu principale, fare clic su **[!UICONTROL Target]>[!UICONTROL Auto Targets]**.

1. Selezionare la casella di controllo accanto a ogni destinazione di ricerca dinamica da cui si rimuoverà un valore di etichetta.

   Per suggerimenti sulla selezione di più righe, vedere &quot;[Selezionare più righe](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**.

1. Seleziona la casella di controllo accanto a ciascun valore di classificazione da rimuovere dalle entità selezionate.

   Per selezionare tutti i valori assegnati, scegliere **[!UICONTROL Select All]**. Per deselezionare tutti i valori assegnati, scegliere **[!UICONTROL Deselect All]**.

1. Fare clic su **[!UICONTROL Unassign Selected]**.

>[!MORELIKETHIS]
>
>* [(Nuova interfaccia) Gestione dei vincoli per le unità di offerta di ricerca](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [(Nuova interfaccia) Gestione classificazioni etichette](/help/search-social-commerce/new-ui/reports/label-classifications-manage.md)
