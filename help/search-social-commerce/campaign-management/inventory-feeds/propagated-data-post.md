---
title: Pubblicare i dati della campagna generati dai feed nelle reti di annunci
description: Scopri come pubblicare i dati generati dai feed di dati di inventario nelle reti di annunci.
exl-id: 7d66c52b-f761-4be2-a1d9-2c63887d7cb7
feature: Search Inventory Feeds
source-git-commit: c27665b979ad8e37fd4f92385bb7339af4354d5f
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 0%

---

# Pubblicare i dati della campagna generati dai feed nelle reti di annunci

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (solo azioni di eliminazione), e [!DNL Yandex] solo account*

Puoi pubblicare i dati della campagna generati da un feed mentre propaghi i dati tramite i modelli associati o come processo separato. Dopo aver pubblicato i dati, tutti i dati propagati esistenti vengono rimossi da [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], e [!UICONTROL Ads] elenchi.

Per una pubblicazione corretta, tutti i gruppi di annunci devono essere assegnati a campagne, tutte le parole chiave e gli annunci devono essere assegnati a gruppi di annunci e tutte le informazioni richieste devono essere incluse senza violazioni della lunghezza.

* Se hai utilizzato l’opzione per &quot;[!UICONTROL Propagate and Preview],&quot; then [pubblica il file di bulksheet generato](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-post.md) (denominato &quot;`<feed file name>_<template name>`&quot;) dal [!UICONTROL Bulksheets] visualizzazione.

  Se non lo hai fatto in precedenza [convalidare le pagine di destinazione](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md), quindi puoi farlo prima di pubblicare il file.

* Se hai utilizzato l’opzione per &quot;[!UICONTROL Propagate only],&quot; quindi puoi pubblicare i dati generati per i componenti con il [[!UICONTROL New] stato](propagated-data-status.md) all’interno di una visualizzazione gerarchia di campagne dalla [!UICONTROL Templates] scheda.

  >[!NOTE]
  >
  >I componenti attivi o eliminati possono includere sottocomponenti nuovi e, se i dati sono validi, i sottocomponenti possono essere inseriti.

  >[!TIP]
  >
  >Se in precedenza non hai convalidato le pagine di destinazione e desideri farlo, [propagare i dati e visualizzarli in anteprima](feed-data-propagate.md) dal [!UICONTROL Bulksheets] visualizzare invece di pubblicarlo sulla rete di annunci. Potrai quindi [convalidare gli URL](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md) prima di inviare manualmente il file alla rete di annunci.

   1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, che apre a [!UICONTROL Templates] scheda.

   1. Selezionare la casella di controllo accanto al modello.

   1. Nella barra degli strumenti, fai clic su **[!UICONTROL Post]**.

   1. Nelle impostazioni di registrazione immettere o selezionare le informazioni nei campi, quindi fare clic su **[!UICONTROL Post]**.

      * **[!UICONTROL Selection]:** Quali componenti conto vengono registrati.

      * **[!UICONTROL Scheduling]:** Quando pubblicare il file:

         * *[!UICONTROL Post to search engine now]* (impostazione predefinita): crea un file di foglio bulk dai dati di feed propagati e inizia a contabilizzarlo immediatamente.

         * *[!UICONTROL Post to search engine on these start/end times (in America/Los_Angeles time)]:* Crea un file bulksheet e lo pubblica in un secondo momento. Specifica quanto segue:

            * **[!UICONTROL Start Time]:** Una data e un’ora future in cui il file bulksheet deve essere inviato alla rete di annunci. Per impostazione predefinita, il file viene inviato alle 00:00 (12:00) del giorno successivo. **Nota:** Per i file di grandi dimensioni che richiedono un’elaborazione più lunga, i dati pubblicati non sono immediatamente disponibili nelle visualizzazioni di gestione delle campagne o nell’Ad Manager della rete.

            * **[!UICONTROL End Time]:** Una data e un’ora future in cui gli annunci pubblicati possono essere messi in pausa o eliminati in base al [impostazione dei dati di feed](feed-settings-manage.md#feed-data-settings) per &quot;[!UICONTROL When the Scheduled End Date is reached].&quot; Per impostazione predefinita, l’ora di fine è alle 00:00 (12:00) 30 giorni a partire da oggi. Seleziona **[!UICONTROL None]** per mantenere i dati attivi indefinitamente (o fino a quando non si propagano nuovi dati per il modello) o specificare una data e un&#39;ora.

              Per specificare una data, utilizzare il formato GG/MM/AAAA o GG/M/AAAA oppure fare clic su ![Calendario](/help/search-social-commerce/assets/calendar.png "Calendario") per aprire il calendario e [seleziona una data](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md). Per modificare un&#39;ora, immettere l&#39;ora nel formato di 24 ore HH/MM o H/M oppure selezionare un&#39;ora (in intervalli di 30 minuti) dall&#39;elenco.

         * **[!UICONTROL Preview in Bulksheet Management Area only, post later]:** Crea un file di foglio ausiliario disponibile dal [!UICONTROL Search] > [!UICONTROL Bulksheets] visualizzazione. Facoltativamente, puoi pubblicare il file da lì.

           Quando il file di bulksheet risultante è superiore a 2 MB, il file è in formato ZIP. Non è necessario decomprimere il file per pubblicarlo.

      * **[!UICONTROL Generate Tracking URLs]:** Se includere gli URL di tracciamento per parole chiave e varianti di annunci nel file di bulksheet: *[!UICONTROL Yes]* (impostazione predefinita) oppure *[!UICONTROL No]*.

        Se si seleziona *[!UICONTROL Yes]*, quindi gli URL vengono generati dagli URL di base per le parole chiave e gli annunci in base al [!UICONTROL Tracking Methods] parametri in [impostazioni account](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) oppure, se mappi dati su campagne esistenti, su [!UICONTROL Tracking Methods] parametri nella [impostazioni della campagna](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md).

        Se esistono URL di tracciamento per gli elementi rilevanti, questi non vengono rigenerati a meno che non siano necessari nuovi URL (ad esempio se il tipo di corrispondenza delle parole chiave, il testo creativo o i parametri di tracciamento dell’account sono cambiati).

      * **[!UICONTROL Bulksheet Name]:** Nome del file di bulksheet da creare dai dati di feed propagati. Per impostazione predefinita, il file è denominato `<feed file name_file extension>_<feed template name>_<creation date in the format YYYYMMDDHHMMSS>.txt`. Puoi rinominare il file come preferisci, ma deve terminare con una delle seguenti estensioni: `.tsv` (per valori separati da tabulazioni), `.txt` (per testo ASCII), `.csv` (per valori separati da virgola), oppure `.zip` (per un file TSV compresso). Per i dati che includono caratteri internazionali, utilizza il formato TSV o TXT.

        Il file pubblicato è disponibile nel [!UICONTROL Bulksheets] visualizzare per 30 giorni, indipendentemente dal fatto che lo si pubblichi o meno sulla rete di annunci.

La &quot;[!UICONTROL Last Prop. Status]La colonna &quot;mostra lo stato del processo per i modelli applicabili.

Quando il bulksheet viene creato, viene elencato nella sezione [!UICONTROL Bulksheets] visualizzazione. Quando il file viene pubblicato, viene inviata una notifica e-mail con un collegamento al file. Tuttavia, se non è possibile pubblicare tutti i dati o parte di essi, nella sezione viene elencato un file di errore [!UICONTROL Bulksheets] e viene inviata una notifica e-mail con un collegamento al file di errore.

>[!NOTE]
>
>* Indipendentemente dall&#39;opzione di pianificazione selezionata, i dati specificati vengono rimossi dal [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], e [!UICONTROL Ads] elenchi.
>* L’elaborazione di grandi quantità di dati richiede più tempo. Puoi seguire l’avanzamento del file durante il processo.
>* Tutti i dati pubblicati sono soggetti al processo editoriale della rete.
>* Prima della pubblicazione di un file di bulksheet, puoi [annulla la registrazione](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-stop-job.md).

>[!MORELIKETHIS]
>
>* [Informazioni sui feed di inventario](inventory-feeds-about.md)
>* [Visualizzare i dati generati dai feed](propagated-data-view.md)
>* [Modificare i dati generati dai feed](propagated-data-edit.md)
>* [Interrompere un processo di registrazione per i dati di feed inventario](stop-job.md)
>* [Stati dei dati generati dai feed](propagated-data-status.md)
