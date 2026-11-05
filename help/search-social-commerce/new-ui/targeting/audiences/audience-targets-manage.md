---
title: Gestire i target di pubblico per campagne e gruppi di annunci
description: Scopri come gestire i target di pubblico e le relative regolazioni delle offerte per Google Ads e Microsoft Advertising.
feature: Search Campaign Management
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
source-git-commit: 7e7dcde9fb195e04025a1a8d89e792ff562b053f
workflow-type: tm+mt
source-wordcount: '562'
ht-degree: 0%
---
# Gestire i target di pubblico per campagne e gruppi di annunci

Solo *[!DNL Google Ads]e [!DNL Microsoft Advertising] account*

[!DNL Google Ads] campagne e gruppi di annunci e [!DNL Microsoft Advertising] gruppi di annunci possono eseguire il targeting di [tipi di pubblico](audience-manage.md) specifici dalla stessa rete di annunci. La rete di annunci determina la dimensione del pubblico che deve essere targetizzabile.

Un target di pubblico associa un pubblico esistente a una campagna o a un gruppo di annunci. Puoi modificare la regolazione dell’offerta e lo stato delle destinazioni esistenti.

>[!NOTE]
>
>[Le esclusioni di pubblico](audience-exclusions.md) sovrascrivono sempre le destinazioni.

## Informazioni sulla visualizzazione [!UICONTROL Targets] {#audience-targets-view-about}

Nella vista [!UICONTROL Targeting] > [!UICONTROL Audiences] > [!UICONTROL Targets] sono elencati i target del pubblico nella vista filtrata per l&#39;inserzionista selezionato.

La visualizzazione dei dati richiede l&#39;autorizzazione [!UICONTROL View Audiences]. Per modificare, modificare lo stato e eliminare le destinazioni è necessaria l&#39;autorizzazione [!UICONTROL Edit Audience Targets].

### Azioni disponibili

<!--
Restricted to internal beta users:

* [Configure audience targets](#audience-targets-create)
-->

* [Modifica regolazioni e stato dell’offerta di destinazione del pubblico](#audience-targets-edit)

* [Modificare lo stato o eliminare i target di pubblico](#audience-targets-status)

* [Copia tutti i dati nelle righe selezionate negli Appunti](#copy-to-clipboard)

<!--
Restricted to internal beta users: audience target creation.

## Configure audience targets {#audience-targets-create}

Creating targets requires the [!UICONTROL Edit Audience Targets] permission in addition to internal beta access.

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Targets]** tab.

1. Click **[!UICONTROL Create Target]**.

1. In **[!UICONTROL Basic Settings]**, select the ad network and account.

1. Select one or more audiences from the account. You can search the list.

   [!DNL Google Ads] customer match audiences are available only for search and shopping campaigns.

1. Select the campaigns or ad groups to target:

   * Select each applicable campaign or ad group for inclusion.

   * To view a campaign's ad groups, expand the campaign.

   * Use the list's search controls to find specific campaigns or ad groups.

   You can't configure a target for both a parent campaign and a child ad group that automatically uses the target.

1. Click **[!UICONTROL Review and Save]**.

1. Review the selections. To make changes, click **[!UICONTROL Edit]** in the applicable section.

1. Click **[!UICONTROL Create]**.

1. (Optional) [Set a bid adjustment](#audience-targets-edit) for the new targets.
-->

## Modifica regolazioni e stato dell’offerta di destinazione del pubblico {#audience-targets-edit}

Puoi modificare uno o più target di pubblico alla volta. Le modifiche vengono applicate a tutte le destinazioni selezionate.

>[!NOTE]
>
>Search, Social e Commerce ottimizzano automaticamente il modificatore di offerta quando la campagna principale utilizza la strategia di offerta CPC ed è in un portfolio configurato per ottimizzare automaticamente i valori di regolazione delle offerte per i target di pubblico. I modificatori di offerte per [!DNL Microsoft Advertising] target del pubblico di remarketing dinamico non sono ottimizzati.

1. Nel menu principale fare clic su **[!UICONTROL Targeting]>[!UICONTROL Audiences]** e quindi sulla scheda **[!UICONTROL Targets]**.

1. Selezionare la casella di controllo accanto a ogni destinazione da modificare.

   Per suggerimenti sulla selezione di più righe, vedere &quot;[Selezionare più righe](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL Edit]**.

1. Modificare **[!UICONTROL Bid Modifier]** o **[!UICONTROL Status]** o entrambi. Consulta le [impostazioni di modifica](#audience-targets-edit-settings).

   Lascia un campo invariato per mantenere il valore esistente.

1. (Facoltativo) Espandere **[!UICONTROL ADDITIONAL DETAILS]** e immettere **[!UICONTROL Project Name]** e **[!UICONTROL Description]**.

1. Fare clic su **[!UICONTROL Save]**.

È inoltre possibile modificare la regolazione dell&#39;offerta di un singolo target direttamente nella tabella di dati facendo clic sul relativo valore nella colonna **[!UICONTROL Bid Adjustment]**.

## Modificare lo stato o eliminare i target di pubblico {#audience-targets-status}

Puoi mettere in pausa un target di pubblico attivo per disabilitare l’offerta per tale target e successivamente riprendere l’offerta attivandola. È inoltre possibile eliminare le destinazioni attive o in pausa.

1. Nel menu principale fare clic su **[!UICONTROL Targeting]>[!UICONTROL Audiences]** e quindi sulla scheda **[!UICONTROL Targets]**.

1. (Facoltativo) Filtra l’elenco per includere target di pubblico specifici.

1. Selezionare la casella di controllo accanto a ogni oggetto di cui si desidera modificare lo stato.

1. Nella barra degli strumenti Azioni in blocco, fare clic su una delle opzioni seguenti:

   * **[!UICONTROL Activate]** per attivare le destinazioni selezionate.

   * **[!UICONTROL Pause]** per sospendere le destinazioni selezionate.

   * **[!UICONTROL Delete]** per eliminare le destinazioni selezionate.

1. Nel messaggio di conferma, fare clic su **[!UICONTROL Confirm]**.

## Copia tutti i dati nelle righe selezionate negli Appunti {#copy-to-clipboard}

Copiare le informazioni visibili nelle righe selezionate, in base ai filtri applicati e alle colonne visibili nella vista. Le informazioni vengono salvate come valori separati da tabulazioni (TSV).

1. Selezionare la casella di controllo accanto a ogni riga di cui si desidera copiare i dati.

1. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL Copy]**.

## Impostazioni di modifica di Audience Target {#audience-targets-edit-settings}

**[!UICONTROL Bid Modifier]:** Come modificare la regolazione dell&#39;offerta di pubblico:

* *[!UICONTROL Set To]:* Sostituisci l&#39;adeguamento dell&#39;offerta esistente con la percentuale specificata.

* *[!UICONTROL Increase]:* Aumentare il valore esistente della percentuale specificata.

* *[!UICONTROL Decrease]:* Diminuire il valore esistente della percentuale specificata.

Per [!UICONTROL Increase] e [!UICONTROL Decrease], immettere un valore non negativo.

Per un valore impostato, 0% non regola l&#39;offerta. Gli altri valori supportati sono compresi tra -90% e 900%. Ad esempio, se l’offerta a livello di parola chiave è 1 USD e la regolazione dell’offerta del pubblico è del 50%, l’offerta per quel pubblico aumenta a 1,50 USD.

**[!UICONTROL Status]:** Seleziona **[!UICONTROL Active]** per abilitare l&#39;offerta o **[!UICONTROL Paused]** per disabilitare l&#39;offerta per la destinazione.

>[!MORELIKETHIS]
>
>* [Gestione tipi di pubblico](audience-manage.md)
>* [Gestire le esclusioni di pubblico per campagne e gruppi di annunci](audience-exclusions.md)
