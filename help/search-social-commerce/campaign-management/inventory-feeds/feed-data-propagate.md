---
title: Propagazione dei dati di feed inventario tramite modelli
description: Scopri come propagare i dati dai feed di inventario tramite modelli di annunci per gestire la struttura dei conti e distribuire annunci dinamici.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '874'
ht-degree: 0%

---

# Propagazione dei dati di feed inventario tramite modelli

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (solo azioni di eliminazione), e [!DNL Yandex] solo account*

Dopo aver creato un modello di feed specifico per una rete di annunci e aver associato un file di feed o un [!DNL Google] o [!DNL Microsoft®] con un account di centro commerciale, puoi creare annunci in modo dinamico propagando i dati di feed attraverso il modello in base al [impostazioni dei dati di feed](feed-settings-manage.md). Durante la propagazione, i nomi delle colonne nel modello vengono sostituiti dai valori dei dati nel feed e le campagne generate e i relativi componenti dispongono delle impostazioni predefinite, a meno che il modello non specifichi diversamente. A seconda delle opzioni del modello, in Ricerca, Social e Commerce viene creata una nuova struttura di account (campagne, gruppi di annunci, parole chiave) per gli annunci o gli annunci vengono mappati sulla struttura di account esistente.

Quando i nuovi dati del feed contengono nuovi valori di dati per un elemento o il modello è stato modificato, gli annunci esistenti vengono eliminati e ne vengono creati di nuovi. Se l&#39;unica modifica riguarda la designazione di [!DNL Google Ads] Param 1 e Param 2, vengono aggiornati solo tali valori. Gli annunci duplicati (la stessa copia e pagina di destinazione dell’annuncio) non vengono mai creati.

Quando propaghi i dati, puoi facoltativamente visualizzare in anteprima i dati generati all’interno di una vista gerarchica della campagna, generare un file bulksheet per la revisione o generare un file bulksheet per la pubblicazione immediata nella rete di annunci. Al termine di ogni azione di propagazione, nella scheda Propagazioni viene aggiunto un riepilogo di propagazione che indica il numero di ogni tipo di entità che è stato o sarebbe stato creato, messo in pausa o eliminato in base alla propagazione. Se non pubblichi i dati immediatamente, puoi visualizzarli in anteprima e pubblicarli in un secondo momento.

## Propagazione dei file di feed da [!UICONTROL Templates] scheda

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, che apre a [!UICONTROL Templates] scheda.

1. Selezionare la casella di controllo accanto ai modelli da propagare.

1. Nella barra degli strumenti, fai clic su **[!UICONTROL Propagate]**, quindi selezionare una delle opzioni seguenti:

   * **[!UICONTROL Propagate Only]:** Per visualizzare i dati propagati su [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], e [!UICONTROL Ads] schede. Puoi comunque pubblicare i dati per qualsiasi componente e i relativi sottocomponenti in un secondo momento da [!UICONTROL Templates] scheda.

   * **[!UICONTROL Propagate and Preview]:** Per creare un file di bulksheet denominato &quot;`<feed file name>_<template name>`&quot;), disponibile nella [!UICONTROL Bulksheets] visualizzazione per la revisione (ma non sulla [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], e [!UICONTROL Ads] schede). In seguito, puoi pubblicare il file bulksheet da [!UICONTROL Bulksheets] visualizzazione.

      Quando il file di bulksheet risultante è superiore a 2 MB, il file è in formato ZIP. Non è necessario decomprimere il file per pubblicarlo.

   * **[!UICONTROL Propagate and Post to SE]:** Per creare un file di bulksheet denominato &quot;`<feed file name>_<template name>`&quot;) che viene immediatamente messo in coda per la pubblicazione sulla rete di annunci. Il file del bulksheet è disponibile nel [!UICONTROL Bulksheets] , ma non è disponibile nel [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], e [!UICONTROL Ads] schede.

      Quando il file di bulksheet risultante è superiore a 2 MB, il file è in formato ZIP.
   L&#39;&quot;Ultimo Prop. La colonna &quot;Stato&quot; mostra lo stato del processo per i modelli applicabili.

   Al termine di ogni azione di propagazione, viene aggiunto un riepilogo di propagazione [!UICONTROL Propagations] , che indica il numero di ciascun tipo di entità che è stato o sarebbe stato creato, messo in pausa o eliminato in base alla propagazione. La stima non include le modifiche apportate dall’editor pubblicitario proprio della rete di annunci.

## Propagazione dei file di feed da [!UICONTROL Feeds] list

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Nella barra degli strumenti sopra la tabella dati, fai clic su **[!UICONTROL Feeds]**.

1. Seleziona la casella di controllo accanto al file di feed.

1. Sopra la tabella dati, fai clic su **[!UICONTROL Propagate/Post Feed Data]**, quindi selezionare una delle opzioni seguenti:

   * **[!UICONTROL Propagate Only]:** Per visualizzare i dati propagati su [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], e [!UICONTROL Ads] schede. Puoi comunque pubblicare i dati per qualsiasi componente e i relativi sottocomponenti in un secondo momento da [!UICONTROL Templates] scheda.

   * **[!UICONTROL Propagate and Preview]:** Per creare un file di bulksheet denominato &quot;`<feed file name>_<template name>`&quot;), disponibile nella [!UICONTROL Bulksheets] visualizzazione per la revisione (ma non sulla [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], e [!UICONTROL Ads] schede). In seguito, puoi pubblicare il file bulksheet da [!UICONTROL Bulksheets] visualizzazione.

      Quando il file di bulksheet risultante è superiore a 2 MB, il file è in formato ZIP. Non è necessario decomprimere il file per pubblicarlo.

   * **[!UICONTROL Propagate and Post to SE]:** Per creare un file di bulksheet denominato &quot;`<feed file name>_<template name>`&quot;) che viene immediatamente messo in coda per la pubblicazione sulla rete di annunci. Il file del bulksheet è disponibile nel [!UICONTROL Bulksheets] , ma non è disponibile nel [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], e [!UICONTROL Ads] schede.

      Quando il file di bulksheet risultante è superiore a 2 MB, il file è in formato ZIP.

1. Nella finestra popup selezionare la casella di controllo accanto a ogni modello tramite il quale si desidera propagare i dati dal file di feed e quindi fare clic su **[!UICONTROL Propagate Feed]**.

   Sono elencati tutti i modelli associati al file.

Il [!UICONTROL Templates] viene visualizzata la scheda e il pulsante &quot;[!UICONTROL Last Prop. Status]La colonna &quot;mostra lo stato del processo per i modelli applicabili.

Al termine di ogni azione di propagazione, viene aggiunto un riepilogo di propagazione [!UICONTROL Propagations] , che indica il numero di ciascun tipo di entità che è stato o sarebbe stato creato, messo in pausa o eliminato in base alla propagazione. La stima non include le modifiche apportate dall’editor pubblicitario proprio della rete di annunci.

## Visualizzare un riepilogo di propagazione

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Fai clic su **[!UICONTROL Propagations]** scheda.

1. Accanto al nome del modello, fai clic su ![Icona Visualizza/Modifica impostazioni](/help/search-social-commerce/assets/settings.png "Icona Visualizza/Modifica impostazioni") .

## Interrompere un processo di propagazione

È possibile interrompere un processo di propagazione per i dati del feed di inventario mentre il processo è ancora in coda.

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, che apre a [!UICONTROL Templates] scheda.

1. Nella sezione &quot;[!UICONTROL Last Prop. Status]&quot; accanto al nome del modello, fai clic su **[!UICONTROL Cancel]**.

>[!MORELIKETHIS]
>
>* [Informazioni sui feed di inventario](inventory-feeds-about.md)
>* [Gestire i modelli di annunci per i feed di inventario](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md)
>* [Visualizzare i dati generati dai feed](propagated-data-view.md)
>* [Modificare i dati generati dai feed](propagated-data-edit.md)
>* [Pubblicare i dati della campagna generati dai feed nelle reti di annunci](propagated-data-post.md)
>* [Interrompere un processo di registrazione per i dati di feed inventario](stop-job.md)
>* [Stati dei dati generati dai feed](propagated-data-status.md)

