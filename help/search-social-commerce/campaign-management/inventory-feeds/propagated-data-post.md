---
title: Pubblicare i dati della campagna generati dai feed nelle reti di annunci
description: Scopri come pubblicare i dati generati dai feed di dati di inventario nelle reti di annunci.
exl-id: 7d66c52b-f761-4be2-a1d9-2c63887d7cb7
feature: Search Inventory Feeds
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 0%

---

# Pubblicare i dati della campagna generati dai feed nelle reti di annunci

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (elimina solo azioni) e [!DNL Yandex] account solo*

Puoi pubblicare i dati della campagna generati da un feed mentre propaghi i dati tramite i modelli associati o come processo separato. Dopo aver pubblicato i dati, tutti i dati propagati esistenti vengono rimossi dagli elenchi [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] e [!UICONTROL Ads].

Per una pubblicazione corretta, tutti i gruppi di annunci devono essere assegnati a campagne, tutte le parole chiave e gli annunci devono essere assegnati a gruppi di annunci e tutte le informazioni richieste devono essere incluse senza violazioni della lunghezza.

* Se hai utilizzato l&#39;opzione per &quot;[!UICONTROL Propagate and Preview]&quot;, [pubblica il file bulksheet generato](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-post.md) (denominato &quot;`<feed file name>_<template name>`&quot;) dalla visualizzazione [!UICONTROL Bulksheets].

  Se in precedenza non hai [convalidato le pagine di destinazione](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md), puoi farlo prima di pubblicare il file.

* Se hai utilizzato l&#39;opzione per &quot;[!UICONTROL Propagate only]&quot;, puoi pubblicare i dati generati per i componenti con lo stato [[!UICONTROL New]](propagated-data-status.md) all&#39;interno di una vista gerarchia campagne dalla scheda [!UICONTROL Templates].

  >[!NOTE]
  >
  >I componenti attivi o eliminati possono includere sottocomponenti nuovi e, se i dati sono validi, i sottocomponenti possono essere inseriti.

  >[!TIP]
  >
  >Se in precedenza non hai convalidato le pagine di destinazione e desideri farlo, [propaga i dati e visualizzali in anteprima](feed-data-propagate.md) dalla visualizzazione [!UICONTROL Bulksheets] invece di pubblicarli nella rete di annunci. Puoi quindi [convalidare gli URL](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md) prima di inviare manualmente il file alla rete di annunci.

   1. Nel menu principale, fare clic su **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, che consente di aprire la scheda [!UICONTROL Templates].

   1. Selezionare la casella di controllo accanto al modello.

   1. Nella barra degli strumenti fare clic su **[!UICONTROL Post]**.

   1. Nelle impostazioni di registrazione immettere o selezionare le informazioni nei campi, quindi fare clic su **[!UICONTROL Post]**.

      * **[!UICONTROL Selection]:** quali componenti account sono registrati.

      * **[!UICONTROL Scheduling]:** Quando pubblicare il file:

         * *[!UICONTROL Post to search engine now]* (impostazione predefinita): crea un file di foglio ausiliario dai dati del feed propagato e inizia a pubblicarlo immediatamente.

         * *[!UICONTROL Post to search engine on these start/end times (in America/Los_Angeles time)]:* crea un file bulksheet e lo pubblica in un secondo momento. Specifica quanto segue:

            * **[!UICONTROL Start Time]:** Una data e un&#39;ora future in cui il file del bulksheet deve essere inviato alla rete di annunci. Per impostazione predefinita, il file viene inviato alle 00:00 (12:00) del giorno successivo. **Nota:** per i file di grandi dimensioni che richiedono un&#39;elaborazione più lunga, i dati pubblicati non sono immediatamente disponibili nelle visualizzazioni di gestione delle campagne o nell&#39;ad manager della rete.

            * **[!UICONTROL End Time]:** Una data e un&#39;ora future in cui gli annunci pubblicati potranno essere sospesi o eliminati in base all&#39;[impostazione dei dati di feed](feed-settings-manage.md#feed-data-settings) per &quot;[!UICONTROL When the Scheduled End Date is reached]&quot;. Per impostazione predefinita, l’ora di fine è alle 00:00 (12:00) 30 giorni a partire da oggi. Selezionare **[!UICONTROL None]** per mantenere i dati attivi indefinitamente (o fino a quando non si propagano nuovi dati per il modello) o specificare una data e un&#39;ora.

              Per specificare una data, utilizzare il formato GG/MM/AAAA o GG/M/AAAA oppure fare clic su ![Calendario](/help/search-social-commerce/assets/calendar.png "Calendario") per aprire il calendario e [selezionare una data](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md). Per modificare un&#39;ora, immettere l&#39;ora nel formato di 24 ore HH/MM o H/M oppure selezionare un&#39;ora (in intervalli di 30 minuti) dall&#39;elenco.

         * **[!UICONTROL Preview in Bulksheet Management Area only, post later]:** Crea un file di foglio bulk disponibile dalla vista [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Bulksheets]. Facoltativamente, puoi pubblicare il file da lì.

           Quando il file di bulksheet risultante è superiore a 2 MB, il file è in formato ZIP. Non è necessario decomprimere il file per pubblicarlo.

      * **[!UICONTROL Generate Tracking URLs]:** se includere gli URL di tracciamento per le parole chiave e le varianti di annunci nel file di bulksheet: *[!UICONTROL Yes]* (impostazione predefinita) o *[!UICONTROL No]*.

        Se si seleziona *[!UICONTROL Yes]*, gli URL vengono generati dagli URL di base per le parole chiave e gli annunci in base ai parametri [!UICONTROL Tracking Methods] nelle [impostazioni account](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) o, se si mappano i dati alle campagne esistenti, ai parametri [!UICONTROL Tracking Methods] nelle [impostazioni campagna](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) esistenti.

        Se esistono URL di tracciamento per gli elementi rilevanti, questi non vengono rigenerati a meno che non siano necessari nuovi URL (ad esempio se il tipo di corrispondenza delle parole chiave, il testo creativo o i parametri di tracciamento dell’account sono cambiati).

      * **[!UICONTROL Bulksheet Name]:** nome del file di bulksheet da creare dai dati di feed propagati. Per impostazione predefinita, il file è denominato `<feed file name_file extension>_<feed template name>_<creation date in the format YYYYMMDDHHMMSS>.txt`. È possibile rinominare il file come desiderato, ma deve terminare con una delle seguenti estensioni di file: `.tsv` (per valori separati da tabulazioni), `.txt` (per testo ASCII), `.csv` (per valori separati da virgola) o `.zip` (per un file TSV compresso). Per i dati che includono caratteri internazionali, utilizza il formato TSV o TXT.

        Il file pubblicato è disponibile nella visualizzazione [!UICONTROL Bulksheets] per 30 giorni, indipendentemente dal fatto che venga pubblicato o meno nella rete di annunci.

La colonna &quot;[!UICONTROL Last Prop. Status]&quot; mostra lo stato del processo per i modelli applicabili.

Al momento della creazione, il bulksheet viene elencato nella visualizzazione [!UICONTROL Bulksheets]. Quando il file viene pubblicato, viene inviata una notifica e-mail con un collegamento al file. Tuttavia, se non è possibile pubblicare tutti i dati o parte di essi, nella visualizzazione [!UICONTROL Bulksheets] viene elencato un file di errore e viene inviata una notifica e-mail con un collegamento al file di errore.

>[!NOTE]
>
>* Indipendentemente dall&#39;opzione di pianificazione selezionata, i dati specificati vengono rimossi dagli elenchi [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] e [!UICONTROL Ads].
>* L’elaborazione di grandi quantità di dati richiede più tempo. Puoi seguire l’avanzamento del file durante il processo.
>* Tutti i dati pubblicati sono soggetti al processo editoriale della rete.
>* Prima della pubblicazione di un file di bulksheet, puoi [annullare la pubblicazione](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-stop-job.md).

>[!MORELIKETHIS]
>
>* [Informazioni sui feed inventario](inventory-feeds-about.md)
>* [Visualizza dati generati dai feed](propagated-data-view.md)
>* [Modifica dati generati dai feed](propagated-data-edit.md)
>* [Interrompere un processo di registrazione per i dati del feed inventario](stop-job.md)
>* [Stati dei dati generati dai feed](propagated-data-status.md)
