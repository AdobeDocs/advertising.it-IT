---
title: Gestire le esclusioni di pubblico per campagne e gruppi di annunci
description: Scopri le esclusioni di pubblico di Google Ads e Microsoft Advertising, tra cui come eliminare le esclusioni di Google Ads.
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
source-wordcount: '269'
ht-degree: 0%
---
# Gestire le esclusioni di pubblico per campagne e gruppi di annunci

Solo *[!DNL Google Ads]e [!DNL Microsoft Advertising] account*

Un&#39;esclusione di pubblico impedisce che gli annunci in una campagna o in un gruppo di annunci vengano mostrati agli utenti di un [pubblico](audience-manage.md) specifico.

Per gli account [!DNL Google Ads], è possibile escludere qualsiasi tipo di pubblico. Per gli account [!DNL Microsoft Advertising], è possibile escludere solo i tipi di pubblico di remarketing dinamico.

>[!NOTE]
>
>Le esclusioni sostituiscono sempre [destinazioni pubblico](audience-targets-manage.md).

## Informazioni sulla visualizzazione [!UICONTROL Exclusions] {#audience-exclusions-view-about}

Nella visualizzazione [!UICONTROL Targeting] > [!UICONTROL Audiences] > [!UICONTROL Exclusions] sono elencate le esclusioni di pubblico nella visualizzazione filtrata per l&#39;inserzionista selezionato.

La visualizzazione dei dati richiede l&#39;autorizzazione [!UICONTROL View Audiences]. La selezione delle righe e l&#39;eliminazione delle esclusioni supportate richiede l&#39;autorizzazione [!UICONTROL Edit Audience Exclusions].

### Azioni disponibili

<!--
Restricted to internal beta users:

* [Configure audience exclusions](#audience-exclusions-create)
-->

* [Eliminare le esclusioni di pubblico](#audience-exclusions-delete)

* [Copia tutti i dati nelle righe selezionate negli Appunti](#copy-to-clipboard)

<!--
Restricted to internal beta users: audience exclusion creation.

## Configure audience exclusions {#audience-exclusions-create}

Creating exclusions requires the [!UICONTROL Edit Audience Exclusions] permission in addition to internal beta access.

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Exclusions]** tab.

1. Click **[!UICONTROL Create Exclusion]**.

1. In **[!UICONTROL Basic Settings]**, select the ad network and account.

1. Select one or more audiences from the account. You can search the list.

   [!DNL Google Ads] customer match audiences are available only for search and shopping campaigns.

1. Select the campaigns or ad groups from which to exclude the audiences:

   * Select each applicable campaign or ad group for exclusion.

   * To view a campaign's ad groups, expand the campaign.

   * Use the list's search controls to find specific campaigns or ad groups.

1. Click **[!UICONTROL Review and Save]**.

1. Review the selections. To make changes, click **[!UICONTROL Edit]** in the applicable section.

1. Click **[!UICONTROL Create]**.
-->

## Eliminare le esclusioni di pubblico {#audience-exclusions-delete}

*[!DNL Google Ads]esclusioni solo*

Puoi eliminare una o più esclusioni di pubblico [!DNL Google Ads]. L&#39;eliminazione di [!DNL Microsoft Advertising] esclusioni non è supportata in questa visualizzazione.

1. Nel menu principale fare clic su **[!UICONTROL Targeting]>[!UICONTROL Audiences]** e quindi sulla scheda **[!UICONTROL Exclusions]**.

1. (Facoltativo) Filtra l’elenco per includere specifiche esclusioni di pubblico.

1. Selezionare la casella di controllo accanto a ogni esclusione di [!DNL Google Ads] da eliminare. Non includere nella selezione le esclusioni da un altro network pubblicitario.

   Per suggerimenti sulla selezione di più righe, vedere &quot;[Selezionare più righe](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL Delete]**.

1. Nel messaggio di conferma, fare clic su **[!UICONTROL Confirm]**.

## Copia tutti i dati nelle righe selezionate negli Appunti {#copy-to-clipboard}

Copiare le informazioni visibili nelle righe selezionate, in base ai filtri applicati e alle colonne visibili nella vista. Le informazioni vengono salvate come valori separati da tabulazioni (TSV).

1. Selezionare la casella di controllo accanto a ogni riga di cui si desidera copiare i dati.

1. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL Copy]**.

>[!MORELIKETHIS]
>
>* [Gestione tipi di pubblico](audience-manage.md)
>* [Gestione dei target del pubblico per campagne e gruppi di annunci](audience-targets-manage.md)
