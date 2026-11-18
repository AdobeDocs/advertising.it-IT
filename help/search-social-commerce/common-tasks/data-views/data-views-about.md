---
title: Informazioni sulla personalizzazione dei dati nelle visualizzazioni di gestione delle campagne
description: Scopri i tipi di dati che è possibile personalizzare nelle visualizzazioni dati di Campaign.
exl-id: 89f36865-9275-494e-ac33-d41fa30faa2a
feature: Search Common Tasks, Search Custom Data Views
TQID: 'https://experienceleague.adobe.com/PnBql37yqK03DWH2OhLf8hnCBPOwFAVZxD65NNZu0VU'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: bcc57258-3285-5d02-a731-d86f57a58c47
    internal-label: Search Common Tasks
  - id: d6e2ef48-fac7-5a4a-96ff-9ac0264dc826
    internal-label: Search Custom Data Views
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 2f170883b2876ea4a7b39e814df598d337f7ca07
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 0%
---
# Informazioni sulla personalizzazione dei dati nelle visualizzazioni di gestione delle campagne

Nella maggior parte delle visualizzazioni dati di Campaign, puoi personalizzare i dati visualizzati all’interno della tabella dati. Puoi personalizzare i dati nei seguenti modi:

* [Modifica le impostazioni per l&#39;intera visualizzazione predefinita](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md##view-edit) per una visualizzazione di entità specifica (ad esempio [!UICONTROL Campaigns]) in modo da includere un ordine di colonna specifico, filtri, intervallo di date, regola di attribuzione e altro ancora. Applicare le impostazioni temporaneamente o salvarle. Puoi anche [creare altre viste personalizzate](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md#create-custom-view), [clonare viste esistenti](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md#view-clone) e [applicare le tue viste](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md#apply-a-default-or-custom-view).

* [Modificare le colonne e il relativo ordinamento](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-sort-icon.md) utilizzando il controllo [!UICONTROL Custom Columns] nella barra degli strumenti. Nella nuova interfaccia utente, se la barra degli strumenti è troppo stretta per visualizzare il controllo, fare clic su **[!UICONTROL Actions]>[!UICONTROL Custom Columns]**. Puoi anche [cambiare rapidamente solo le colonne](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-column-heading.md) da qualsiasi intestazione di colonna nella visualizzazione.

* (Solo interfaccia utente legacy) [Dal pannello di navigazione a sinistra](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/filter-using-left-panel.md), è possibile:

  * Sfoglia o cerca le entità per rete di annunci e filtra in base allo stato dell’entità e allo stato dell’account, della campagna e del gruppo di annunci o del set di annunci. Fai clic su un’entità o un gruppo di entità nel pannello per caricare una visualizzazione delle entità figlio (ad esempio, fai clic sul nome di una campagna per visualizzarne i gruppi di annunci figlio).

  * Sfoglia o cerca le campagne per portfolio o gruppo di portfolio e filtra in base allo stato dell’entità e allo stato del gruppo di portfolio, portfolio e campagna. Fai clic su un gruppo di portfolio, portfolio o campagna nel pannello per caricare i dati per il gruppo di portfolio, portfolio o campagna nella vista entità corrente.

  * Accesso, modifica e reimpostazione delle visualizzazioni predefinite, accesso, modifica ed eliminazione delle visualizzazioni personalizzate. Facendo clic sul nome di una vista, viene caricata la vista appropriata.

* Applica i filtri alle colonne di dati disponibili per modificare i dati visualizzati nella scheda corrente. È possibile creare filtri [dalle intestazioni di colonna](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md) o [da un pulsante sulla barra degli strumenti](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md). Per le viste di gestione delle campagne, i filtri vengono mantenuti applicabili quando apri le entità figlio. Ad esempio, se visualizzi le campagne con \> 100 clic e quindi apri un gruppo di annunci all’interno della campagna, vengono visualizzati solo i gruppi di annunci con \> 100 clic.

* [Modifica l&#39;intervallo di date](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/date-filter.md) utilizzato in tutte le visualizzazioni predefinite e personalizzate per le quali non sono stati salvati intervalli di date specifici.

* [Riordinare i dati](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-sort.md) in base ai valori di una colonna specifica.

* Controlla se visualizzare 25 righe, 50 righe, 100 righe, (solo interfaccia utente legacy) 200 righe o (solo interfaccia utente legacy) [!UICONTROL Continuous Scroll] nella parte inferiore di qualsiasi pagina.

<!--

## (New UI) Data table tools {#grid-controls-new-ui}

In applicable management views, the toolbar includes the following controls:

* On the left, the [!UICONTROL Filter] control appears before grid search. Where supported, the [!UICONTROL Conversion based on] selector follows search and lets you select [!UICONTROL Click Date] or [!UICONTROL Transaction Date].

* On the right, operational actions, such as [!UICONTROL Reports], appear alongside view and display controls. The available controls depend on the view and your permissions.

* When the available width is reduced, controls move into the [!UICONTROL Actions] menu. This can happen when you narrow the window or open the AI Assistant panel. If a control isn't visible in the toolbar, look for it in [!UICONTROL Actions]. In wider layouts, controls remain inline.

* Within [!UICONTROL Actions], a horizontal divider separates operational actions from view and display controls, such as the current view, [!UICONTROL Custom Columns], [!UICONTROL Compressed Mode], and [!UICONTROL Charts], where available.

* The primary create button remains outside [!UICONTROL Actions].

The [!UICONTROL Refresh] icon is beside the page title in applicable views. The date range control is in the page header. For instructions on comparing two date ranges and changing the comparison format, see "[Filter data by date range](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/date-filter.md#compare-periods-new-ui)."

### Change the grid density

* Where available, click **[!UICONTROL Compressed Mode]** in the toolbar or **[!UICONTROL Actions]** menu to turn compact grid spacing on or off.

  The toolbar button is selected when compressed mode is on. In [!UICONTROL Actions], a switch indicates the current state.

### Show or hide charts

* Where available, click **[!UICONTROL Charts]** in the toolbar or **[!UICONTROL Actions]** menu.

  The toolbar button is selected when charts are shown. In [!UICONTROL Actions], a switch indicates whether charts are shown. Click the control again to hide the charts.

-->
