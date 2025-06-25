---
title: Propagazione dei dati di feed inventario tramite modelli
description: Scopri come propagare i dati dai feed di inventario tramite modelli di annunci per gestire la struttura dei conti e distribuire annunci dinamici.
exl-id: 9660af19-a517-4593-9a99-da600a0285a5
feature: Search Inventory Feeds
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '876'
ht-degree: 0%

---

# Propagazione dei dati di feed inventario tramite modelli

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (elimina solo azioni) e [!DNL Yandex] account solo*

Dopo aver creato un modello di feed specifico per la rete di annunci e aver associato a esso un file di feed o un account del centro commerciale [!DNL Google] o [!DNL Microsoft], puoi creare annunci propagando i dati di feed tramite il modello in base alle [impostazioni dei dati di feed](feed-settings-manage.md). Durante la propagazione, i nomi delle colonne nel modello vengono sostituiti dai valori dei dati nel feed e le campagne generate e i relativi componenti dispongono delle impostazioni predefinite, a meno che il modello non specifichi diversamente. A seconda delle opzioni del modello, Cerca, Social e Commerce creano una nuova struttura dell’account (campagne, gruppi di annunci, parole chiave) per gli annunci o mappano gli annunci alla struttura dell’account esistente.

Quando i nuovi dati del feed contengono nuovi valori di dati per un elemento o il modello è stato modificato, gli annunci esistenti vengono eliminati e ne vengono creati di nuovi. Se l&#39;unica modifica è la designazione di [!DNL Google Ads] Param 1 e Param 2, verranno aggiornati solo questi valori. Gli annunci duplicati (la stessa copia e pagina di destinazione dell’annuncio) non vengono mai creati.

Quando propaghi i dati, puoi facoltativamente visualizzare in anteprima i dati generati all’interno di una vista gerarchica della campagna, generare un file bulksheet per la revisione o generare un file bulksheet per la pubblicazione immediata nella rete di annunci. Al termine di ogni azione di propagazione, nella scheda Propagazioni viene aggiunto un riepilogo di propagazione che indica il numero di ogni tipo di entità che è stato o sarebbe stato creato, messo in pausa o eliminato in base alla propagazione. Se non pubblichi i dati immediatamente, puoi visualizzarli in anteprima e pubblicarli in un secondo momento.

## Propagare i file di feed dalla scheda [!UICONTROL Templates]

1. Nel menu principale, fare clic su **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, che consente di aprire la scheda [!UICONTROL Templates].

1. Selezionare la casella di controllo accanto ai modelli da propagare.

1. Nella barra degli strumenti fare clic su **[!UICONTROL Propagate]** e quindi selezionare una delle opzioni seguenti:

   * **[!UICONTROL Propagate Only]:** Per visualizzare i dati propagati nelle schede [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] e [!UICONTROL Ads]. È comunque possibile pubblicare i dati per qualsiasi componente e i relativi sottocomponenti in un secondo momento dalla scheda [!UICONTROL Templates].

   * **[!UICONTROL Propagate and Preview]:** Per creare un file bulksheet (denominato &quot;`<feed file name>_<template name>`&quot;), disponibile nella visualizzazione [!UICONTROL Bulksheets] per la revisione (ma non nelle schede [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] e [!UICONTROL Ads]). In seguito sarà possibile pubblicare il file bulksheet dalla visualizzazione [!UICONTROL Bulksheets].

     Quando il file di bulksheet risultante è superiore a 2 MB, il file è in formato ZIP. Non è necessario decomprimere il file per pubblicarlo.

   * **[!UICONTROL Propagate and Post to SE]:** Per creare un file di bulksheet (denominato &quot;`<feed file name>_<template name>`&quot;) che viene immediatamente inserito nella coda per la pubblicazione nella rete di annunci. Il file del bulksheet è disponibile nella visualizzazione [!UICONTROL Bulksheets], ma non nelle schede [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] e [!UICONTROL Ads].

     Quando il file di bulksheet risultante è superiore a 2 MB, il file è in formato ZIP.

   L&#39;&quot;Ultimo Prop. La colonna &quot;Stato&quot; mostra lo stato del processo per i modelli applicabili.

   Al termine di ogni azione di propagazione, alla scheda [!UICONTROL Propagations] viene aggiunto un riepilogo della propagazione che indica il numero di ogni tipo di entità che è stato o sarebbe stato creato, messo in pausa o eliminato in base alla propagazione. La stima non include le modifiche apportate dall’editor pubblicitario proprio della rete di annunci.

## Propagare i file di feed dall&#39;elenco [!UICONTROL Feeds]

1. Nel menu principale, fare clic su **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Nella barra degli strumenti sopra la tabella dati, fare clic su **[!UICONTROL Feeds]**.

1. Seleziona la casella di controllo accanto al file di feed.

1. Sopra la tabella dati fare clic su **[!UICONTROL Propagate/Post Feed Data]** e quindi selezionare una delle opzioni seguenti:

   * **[!UICONTROL Propagate Only]:** Per visualizzare i dati propagati nelle schede [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] e [!UICONTROL Ads]. È comunque possibile pubblicare i dati per qualsiasi componente e i relativi sottocomponenti in un secondo momento dalla scheda [!UICONTROL Templates].

   * **[!UICONTROL Propagate and Preview]:** Per creare un file bulksheet (denominato &quot;`<feed file name>_<template name>`&quot;), disponibile nella visualizzazione [!UICONTROL Bulksheets] per la revisione (ma non nelle schede [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] e [!UICONTROL Ads]). In seguito sarà possibile pubblicare il file bulksheet dalla visualizzazione [!UICONTROL Bulksheets].

     Quando il file di bulksheet risultante è superiore a 2 MB, il file è in formato ZIP. Non è necessario decomprimere il file per pubblicarlo.

   * **[!UICONTROL Propagate and Post to SE]:** Per creare un file di bulksheet (denominato &quot;`<feed file name>_<template name>`&quot;) che viene immediatamente inserito nella coda per la pubblicazione nella rete di annunci. Il file del bulksheet è disponibile nella visualizzazione [!UICONTROL Bulksheets], ma non nelle schede [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] e [!UICONTROL Ads].

     Quando il file di bulksheet risultante è superiore a 2 MB, il file è in formato ZIP.

1. Nella finestra popup selezionare la casella di controllo accanto a ogni modello tramite il quale si desidera propagare i dati dal file di feed e quindi fare clic su **[!UICONTROL Propagate Feed]**.

   Sono elencati tutti i modelli associati al file.

Viene visualizzata la scheda [!UICONTROL Templates] e la colonna &quot;[!UICONTROL Last Prop. Status]&quot; mostra lo stato del processo per i modelli applicabili.

Al termine di ogni azione di propagazione, alla scheda [!UICONTROL Propagations] viene aggiunto un riepilogo della propagazione che indica il numero di ogni tipo di entità che è stato o sarebbe stato creato, messo in pausa o eliminato in base alla propagazione. La stima non include le modifiche apportate dall’editor pubblicitario proprio della rete di annunci.

## Visualizzare un riepilogo di propagazione

1. Nel menu principale, fare clic su **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Fare clic sulla scheda **[!UICONTROL Propagations]**.

1. Accanto al nome del modello, fare clic su ![Icona Visualizza/Modifica impostazioni](/help/search-social-commerce/assets/settings.png "Icona Visualizza/Modifica impostazioni").

## Interrompere un processo di propagazione

È possibile interrompere un processo di propagazione per i dati del feed di inventario mentre il processo è ancora in coda.

1. Nel menu principale, fare clic su **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, che consente di aprire la scheda [!UICONTROL Templates].

1. Nella colonna &quot;[!UICONTROL Last Prop. Status]&quot; accanto al nome del modello, fare clic su **[!UICONTROL Cancel]**.

>[!MORELIKETHIS]
>
>* [Informazioni sui feed inventario](inventory-feeds-about.md)
>* [Gestione dei modelli di annunci per i feed inventario](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md)
>* [Visualizza dati generati dai feed](propagated-data-view.md)
>* [Modifica dati generati dai feed](propagated-data-edit.md)
>* [Pubblica i dati della campagna generati dai feed alle reti di annunci](propagated-data-post.md)
>* [Interrompere un processo di registrazione per i dati del feed inventario](stop-job.md)
>* [Stati dei dati generati dai feed](propagated-data-status.md)
