---
title: Gestire i file di feed dati di inventario
description: Scopri come configurare le impostazioni che controllano la modalità di elaborazione dei dati dei feed.
exl-id: 73d372de-2673-4190-94cf-2f07f4ce2493
feature: Search Inventory Feeds
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '1242'
ht-degree: 0%

---

# Gestire i file di feed dati di inventario

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (solo azioni di eliminazione), e [!DNL Yandex] solo account*

Se invii i tuoi dati di feed, devi caricare file contenenti i tuoi dati di prodotto per creare in modo dinamico la struttura della campagna, gli annunci e le parole chiave, in base ai dati di prodotto. Puoi quindi associarli a modelli di annunci specifici per la rete di annunci ed elaborare i dati tramite i modelli, infine pubblicare i dati nelle reti di annunci pertinenti. È possibile associare più modelli a un file di feed, ma ogni modello può essere associato a un solo file di feed.

>[!NOTE]
>
>Non caricare file se utilizzi dati direttamente da un account di un centro commerciale.

Puoi caricare ed elaborare i file di feed dati in uno dei seguenti modi:

* **Automaticamente con FTP:** È possibile caricare i file direttamente in una directory FTP; il servizio di feed verifica la presenza di nuovi file ogni due ore. Dopo aver caricato un file per la prima volta, puoi associarlo a un modello specifico per la rete di annunci. Successivamente, tutti i file caricati con lo stesso nome vengono automaticamente associati allo stesso modello. A seconda di come [configurare le impostazioni dei dati di feed](feed-settings-manage.md), Search, Social e Commerce possono propagare automaticamente i dati del feed tramite tutti i modelli applicabili e, facoltativamente, pubblicare la campagna e i dati dell’annuncio risultanti sulle reti di annunci pertinenti.

  Per impostare una directory FTP per il deposito e l’elaborazione automatica dei file di dati, contatta il team del tuo account di Adobe.

* **Elaborazione manuale:** Puoi eseguire manualmente [carica file di feed](#feed-file-upload) dal [!UICONTROL Advanced] (ACM). Dopo aver associato un file di feed a uno o più annunci specifici della rete [modelli](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md), puoi generare dati di campagne e annunci tramite [propagazione dei dati del feed tramite i modelli](feed-data-propagate.md) in base al [impostazioni dei dati di feed](feed-settings-manage.md). Facoltativamente, puoi visualizzare in anteprima i dati generati nelle viste gerarchiche della campagna, generare un file bulksheet per la revisione o generare un file bulksheet per la pubblicazione immediata nella rete di annunci. Se non pubblichi i dati immediatamente, puoi [anteprima](propagated-data-view.md) e [pubblicarlo](propagated-data-post.md) più tardi. Potrai farlo in seguito [sostituisci il file di feed esistente con un nuovo file](#feed-file-replace) senza perdere le associazioni di modelli esistenti.

## Requisiti del file di feed

Non sono necessari campi di dati specifici in un singolo file, ma per ogni file sono necessari i seguenti elementi:

* La prima riga del file deve contenere nomi di colonna (denominati anche *intestazioni*), che corrispondono ai parametri dinamici nei modelli associati. Le righe rimanenti devono includere dati corrispondenti ai nomi delle colonne. Ogni riga di dati deve riferirsi a un solo componente account, ad esempio una campagna o un annuncio. I valori su tutte le righe devono essere separati da tabulazioni o virgole. Consulta la [File di esempio CSV](#example-csv-feed-file) e [File di esempio TSV](#example-tsv-feed-file) di seguito.

* Il file può essere di qualsiasi dimensione ma deve avere una delle seguenti estensioni: `.tsv` (per valori separati da tabulazioni), `.txt` (per [!DNL Unicode]testo ASCII conforme), `.csv` (per valori separati da virgola), oppure `.zip` (per un singolo file in formato ZIP compresso, che si decomprime in un file TSV).

* Il nome del file fa distinzione tra maiuscole e minuscole e non può includere i seguenti caratteri: `# % & * | \ : " < > . ? /`

* Se si depositano file in una directory FTP, è necessario utilizzare lo stesso nome per ogni versione del file.

* ([!DNL Google Ads] solo modelli) Se il modello utilizza il parametro di annuncio Param2 o Param2 negli annunci di testo, i campi di dati corrispondenti nel file di feed devono includere dati numerici, senza simboli monetari.

* Per aggiornare i componenti account esistenti, includi il nome della campagna esistente (e i relativi componenti, se pertinenti). Se la struttura esistente non è specificata, vengono creati nuovi componenti.

### Esempio di un file di feed separato da virgole {#example-csv-feed-file}

```
Product Category,Product Name,Discount Percentage
electronics,iPods,10
apparel,Shirts,15
shoes,Clarks,20
```

### Esempio di un file di feed separato da tabulazioni {#example-tsv-feed-file}

```
Product Category<TAB>Product Name<TAB>Discount Percentage
electronics<TAB>iPods<TAB>10
apparel<TAB>Shirts<TAB>15
shoes<TAB>Clarks<TAB>20
```

## Best practice

* Per i dati che includono caratteri internazionali, utilizza i file in formato TSV o TXT.

* Per ottenere un processo ripetibile con revisione o modifica manuale limitata, imposta i file di feed e i relativi dati della struttura dell’account come segue:

   * Includi colonne e righe contenenti dati sufficienti per creare una struttura di conto o eseguire il mapping alla struttura di conto esistente. Idealmente, utilizza una struttura dei conti esistente che sia strettamente legata alla tassonomia dei prodotti e alla quale i dati dei feed possano essere facilmente mappati.

   * Includi descrizioni sufficientemente brevi da poter essere utilizzate nella copia dell’annuncio.

   * Utilizza pattern di dati e convenzioni di denominazione coerenti tra le righe di prodotto.

   * Rimuovere tutti gli spazi precedenti e finali.

   * Rimuovi eventuali caratteri illeggibili.

## Visualizzare o scaricare un file di feed

Puoi aprire o scaricare qualsiasi file di feed caricato manualmente o utilizzando l’FTP.

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, che apre a [!UICONTROL Templates] scheda.

1. Individua il file di feed:

1. Nell&#39;elenco dei modelli individuare un modello che utilizza il file di feed.

1. Nella barra degli strumenti sopra la tabella dati, fai clic su **[!UICONTROL Feeds]** per aprire un elenco di tutti i file di feed.

1. Fai clic sul nome del file di feed.

1. Apri o salva il file in base alla normale procedura del browser.

Per ulteriori informazioni, consulta la guida in linea del browser.

## Caricare manualmente un file di feed {#feed-file-upload}

>[!NOTE]
> Se si associa un modello a un file caricato manualmente, ma in seguito si carica tramite FTP un altro file con lo stesso nome, estensione e maiuscole/minuscole, il file FTP viene utilizzato quando si propagano i dati tramite il modello. Ad esempio, myfile.csv sostituisce myfile.csv, mentre Myfile.CSV no.

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, che apre a [!UICONTROL Templates] scheda.

1. Nella barra degli strumenti sopra la tabella dati, fai clic su **[!UICONTROL Feeds]**.

1. Sopra la tabella dati, fai clic su **[!UICONTROL Upload]**.

1. Specificare il file da caricare immettendo il percorso completo e il nome del file oppure facendo clic su **[!UICONTROL Browse]** per individuare il file sul dispositivo o sulla rete.

1. Clic **[!UICONTROL Upload].

Tutti i campi nel file vengono convalidati. Non puoi pubblicare elementi con lunghezze di campo non valide in un secondo momento finché non correggi i valori. Tutti i nomi di colonna nel file diventano disponibili nei modelli come parametri dinamici.

## Sostituire un file di feed {#feed-file-replace}

Quando sostituite un file di feed, anche se il nuovo file ha un nome o un&#39;estensione diversa, tutte le associazioni di modelli esistenti vengono mantenute. Il nuovo file viene utilizzato quando si propagano i dati tramite tutti i modelli originariamente associati al file precedente.

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, che apre a [!UICONTROL Templates] scheda.

1. Effettuare una delle seguenti operazioni:

   * In [!UICONTROL Feed] per qualsiasi modello applicabile, fai clic su ![Altre opzioni](/help/search-social-commerce/assets/options.png "Altre opzioni") e seleziona **[!UICONTROL Re-upload]**.

   * Nella barra degli strumenti sopra la tabella dati, fai clic su **[!UICONTROL Feeds]**. Nell&#39;elenco dei file di feed selezionare la casella di controllo accanto al nome del file esistente. Sopra la tabella dati, fai clic su **[!UICONTROL Upload]**.

   >[!NOTE]
   >
   >Origine del file di feed (&quot;[!UICONTROL FTP]&quot; o &quot;&amp;mdash&quot; per i file caricati manualmente) è incluso nel [!UICONTROL Source] colonna.

1. Specificare il file da caricare immettendo il percorso completo e il nome del file oppure facendo clic su **[!UICONTROL Browse]** per individuare il file sul dispositivo o sulla rete.

Anche se il nuovo file ha un nome o un&#39;estensione diversa, il file esistente viene sovrascritto con il nuovo file.

1. Clic **[!UICONTROL Re-Upload]**.

Tutti i campi nel file vengono convalidati. Non puoi pubblicare elementi con lunghezze di campo non valide in un secondo momento finché non correggi i valori. Tutti i nomi di colonna nel file diventano disponibili nei modelli come parametri dinamici.

## Elimina file di feed

Puoi eliminare qualsiasi file di feed caricato manualmente o tramite FTP. Quando si elimina un file di feed, questo non viene più associato ad alcun modello.

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, che apre a [!UICONTROL Templates] scheda.

1. Nella barra degli strumenti sopra la tabella dati, fai clic su **[!UICONTROL Feeds]**.

1. Selezionare la casella di controllo accanto a ogni file che si desidera eliminare.

1. Sopra la tabella dati, fai clic su **[!UICONTROL Delete]**.

1. Nel messaggio di conferma, fai clic su **[!UICONTROL Yes]**.

>[!MORELIKETHIS]
>
>* [Informazioni sui feed di inventario](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [Propagazione dei dati di feed tramite modelli](feed-data-propagate.md)
>* [Visualizzare i dati generati dai feed](propagated-data-view.md)
>* [Modificare i dati generati dai feed](propagated-data-edit.md)
>* [Pubblicare i dati della campagna generati dai feed nelle reti di annunci](propagated-data-post.md)
>* [Interrompere un processo di registrazione per i dati di feed inventario](stop-job.md)
>* [Stati dei dati generati dai feed](propagated-data-status.md)
