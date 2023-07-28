---
title: Configurare le impostazioni dei dati dei feed
description: Scopri come configurare le impostazioni che controllano la modalità di elaborazione dei dati dei feed.
exl-id: fc72d1bc-aac7-4280-80c6-4fc53a96a49f
feature: Search Inventory Feeds
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '1147'
ht-degree: 0%

---

# Configurare le impostazioni dei dati dei feed

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (solo azioni di eliminazione), e [!DNL Yandex] solo account*

Puoi configurare la gestione dei gruppi di annunci, delle parole chiave e degli annunci nei file di dati dei feed e la modalità di elaborazione dei dati in specifici file FTP, tramite le impostazioni dei feed.

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Nella barra degli strumenti sopra la tabella dati, fai clic su **[!UICONTROL Settings]**.

1. Specifica la [impostazioni dei dati di feed](#feed-data-settings):

   1. In [!UICONTROL Obsolete Item Auto-Processing] , seleziona le informazioni nei campi.

   1. (Gli inserzionisti caricano i dati tramite FTP o tramite un collegamento diretto a un account di un centro commerciale) Nel [!UICONTROL FTP/GMC Account Auto-Processing] , seleziona le informazioni nei campi.

   1. In [!UICONTROL Miscellaneous Auto-Processing] , seleziona le informazioni nei campi.

1. Clic **[!UICONTROL Save]**.

## Impostazioni dei dati dei feed {#feed-data-settings}

**[!UICONTROL Enable obsolete item auto-processing for]:** Applica tutte le [!UICONTROL Obsolete Item Auto-processing] impostazioni per:

* *[!UICONTROL Ad Groups Only]:* Solo gruppi di annunci obsoleti.

* *[!UICONTROL Keywords Only]:* Solo parole chiave e gruppi di prodotti obsoleti.

* *[!UICONTROL Ad Variations Only]* (impostazione predefinita): solo annunci obsoleti.

* *[!UICONTROL Keywords and Ad Variations]:* Sia parole chiave obsolete/target di prodotto/gruppi di prodotti che annunci obsoleti.

>[!NOTE]
>
>* Per [!DNL Google Ads] per gli annunci commerciali, è interessato solo il gruppo di prodotti di livello più basso.
>* Per [!DNL Yandex] account, le attività obsolete di elaborazione automatica degli elementi vengono sempre eseguite sulle varianti di annuncio, indipendentemente da questa impostazione.

**[!UICONTROL When the Scheduled End Date is reached]:** (Solo dati pubblicati manualmente) Cosa fare con gli elementi riga in un file di feed pubblicato con una data e un’ora di fine specificate una volta arrivata l’ora di fine:

* *[!UICONTROL Delete]* (impostazione predefinita): elimina tutti i componenti rilevanti quando arriva l’ora di fine specificata. Non puoi annullare questa operazione.

* *[!UICONTROL Pause]:* Sospendi tutti i componenti rilevanti quando arriva l’ora di fine specificata. Se necessario, puoi riattivare i componenti in un secondo momento.

* *[!UICONTROL None]:* Non modificare lo stato dei componenti rilevanti.

**[!UICONTROL Missing line items in a manually uploaded feed]:** Cosa fare con gli elementi esistenti quando non sono inclusi in un nuovo file di feed caricato manualmente o quando non sono mappati su campagne o gruppi di annunci esistenti in base alle impostazioni Mappa solo nel modello:

* *[!UICONTROL Delete]:* Elimina i componenti esistenti.

* *[!UICONTROL Pause]:* Metti in pausa i componenti esistenti. Vengono riattivati se un nuovo file di feed contiene gli stessi elementi di riga e conservano la cronologia e i punteggi di qualità. **Nota:** Se mancano tutti i gruppi di prodotti figlio per un gruppo di prodotti padre, il gruppo di prodotti padre viene eliminato perché non è possibile mettere in pausa i gruppi di prodotti.

* *[!UICONTROL None]* (impostazione predefinita): non modificare i componenti esistenti.

**[!UICONTROL Missing line items in an FTP feed/GMC account]:** Cosa fare con gli elementi esistenti quando 1) non sono inclusi a) in un nuovo file di feed caricato in una directory FTP o b) in un account di un centro commerciale la volta successiva che Search, Social e Commerce si sincronizzano con esso, o 2) quando non vengono mappati su campagne o gruppi di annunci esistenti per il [!UICONTROL Map Only] impostazioni nel modello.

* *[!UICONTROL Delete]:* Elimina i componenti esistenti.

* *[!UICONTROL Pause]:* Metti in pausa i componenti esistenti. Vengono riattivati se i nuovi dati contengono uno degli stessi elementi e mantengono la cronologia e il punteggio di qualità. **Nota:** Se mancano tutti i gruppi di prodotti figlio per un gruppo di prodotti padre, il gruppo di prodotti padre viene eliminato perché non è possibile mettere in pausa i gruppi di prodotti.

* *[!UICONTROL None]* (impostazione predefinita): non modificare i componenti esistenti.

**[!UICONTROL When a numeric stock level reaches N units, or where a text-based value is 'out of stock']:** Operazioni da eseguire con gli articoli di linea che includono un livello di scorte quando:

* (Per i feed con valori di stock solo numerici nella colonna specificata) Il livello di stock è pari o inferiore a una quantità specificata. La quantità predefinita è zero (0).

* (Per i feed con valori di testo nella colonna specificata) Il valore per [!UICONTROL Availability] è &quot;[!UICONTROL out of stock]&quot;; il valore non fa distinzione tra maiuscole e minuscole. **Nota:** **Nei modelli di feed, indica le colonne a livello di stock basate su testo utilizzando la casella di controllo per &quot;[!UICONTROL This column has non-numeric values].&quot;

Seleziona l’azione per entrambi i casi:

* *[!UICONTROL Delete]* (impostazione predefinita) Elimina i componenti.

* *[!UICONTROL Pause]:* Metti in pausa i componenti. Quando i dati vengono aggiornati, i componenti vengono riattivati se i valori numerici delle scorte superano la quantità specificata o se [!UICONTROL Availability] è &quot;[!UICONTROL in stock]&quot; o &quot;[!UICONTROL preorder]&quot;. I componenti mantengono la cronologia e il punteggio di qualità.

Il livello di magazzino per ogni riga proviene da una colonna nel file di feed, come specificato in &quot;[!UICONTROL Stock Level]&quot; per ciascun modello.

>[!TIP]
>
>* Per i prodotti o i servizi per i quali si prevede di effettuare il riassortimento o aumentare la disponibilità, è consigliabile sospendere i gruppi di annunci, le parole chiave e gli annunci anziché eliminarli e ricrearli. La messa in pausa consente di mantenere i punteggi di qualità.
>* Se abiliti l’elaborazione automatica obsoleta per i gruppi di annunci e i nuovi dati includono un livello di stock per il gruppo di annunci, è significativo eliminare o mettere in pausa il gruppo di annunci solo quando il livello di stock specificato è a livello di categoria anziché a livello di marchio/articolo. Ad esempio, se hai un gruppo di annunci &quot;convertibili&quot;, il livello di stock per il gruppo di annunci deve essere il totale di tutti i singoli modelli convertibili rappresentati nel gruppo di annunci.

**[!UICONTROL Propagate feed data through all applicable templates]:** (Gli inserzionisti che caricano file di dati tramite FTP o un account di un centro commerciale) propaga automaticamente i nuovi dati tramite i modelli applicabili. L’opzione è selezionata per impostazione predefinita. Se disattivi l’opzione, puoi comunque propagare manualmente i dati per qualsiasi file di feed, account o modello.

>[!NOTE]
>
>* Per i file FTP, il servizio di feed verifica la presenza di aggiornamenti nella directory FTP ogni due ore (ore pari nel fuso orario PST). Questa opzione elabora tutti i file caricati dall’ultimo controllo.
>* Per gli account del centro commerciale, Search, Social e Commerce si sincronizzano con l’account ogni giorno alle 06:00 circa nel fuso orario dell’inserzionista. Questa opzione elabora tutti i dati aggiornati dall&#39;ultima sincronizzazione.
>* I dati propagati sono disponibili da [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], e [!UICONTROL Ads] fino a quando i dati non vengono inviati alla rete di annunci o al [!UICONTROL Bulksheets] visualizzazione.

**[!UICONTROL Post to the SE]:** (Gli inserzionisti caricano i file di dati tramite FTP o un account del centro commerciale) Crea automaticamente i file dei bulksheet nei formati corretti per le reti pubblicitarie pertinenti dopo che i nuovi dati vengono propagati tramite i modelli applicabili. Questa opzione rimuove anche i dati da [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], e [!UICONTROL Ads] , a meno che non si verifichino errori in uno dei sottocomponenti.

Questa opzione è disabilitata per impostazione predefinita. Per abilitare questa opzione, selezionare la casella di controllo e quindi specificare se inviare i file di bulksheet alle reti di annunci:

* *[!UICONTROL Immediately]* (impostazione predefinita): pubblica i file dei fogli collettivi nelle reti pubblicitarie pertinenti dopo che i dati sono stati propagati tramite i modelli. I file dei bulksheet rimangono disponibili in [!UICONTROL Bulksheets] 30 giorni.

* *[!UICONTROL Preview in Bulksheet Management area only, post later]:** Non pubblica i file dei bulksheet sulle reti pubblicitarie pertinenti, ma li elenca nel [!UICONTROL Bulksheets] , da cui puoi pubblicarli in un secondo momento. I file dei bulksheet rimangono disponibili in [!UICONTROL Bulksheets] 30 giorni. Quando il file bulksheet è superiore a 10 MB ma inferiore a 2 GB, il file è in formato ZIP; non è necessario decomprimere il file per pubblicarlo. **Suggerimento** Se non hai convalidato in precedenza le pagine di destinazione, utilizza questa opzione per convalidarle dalla sezione [!UICONTROL Bulksheets] prima di pubblicare i dati sulla rete di annunci.

**[!UICONTROL Exclude keywords from posting when keyword length is greater than]:** Impedisce la pubblicazione di frasi di parole chiave con più di un numero specificato di parole nella rete di annunci. Quando questa opzione è selezionata, le frasi delle parole chiave con un numero di parole superiore al numero massimo vengono propagate ed elencate nel [!UICONTROL Keywords] , ma non vengono pubblicate quando tenti di pubblicare i dati.

Questa opzione è disattivata per impostazione predefinita, in modo che vengano pubblicate tutte le parole chiave, indipendentemente dal numero di parole incluse nella frase. Se si seleziona questa opzione, selezionare il numero massimo di parole da inserire (da 3 a 10).

>[!MORELIKETHIS]
>
>* [Informazioni sui feed di inventario](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [Propagazione dei dati di feed tramite modelli](/help/search-social-commerce/campaign-management/inventory-feeds/feed-data-propagate.md)
>* [Pubblicare i dati della campagna generati dai feed nelle reti di annunci](propagated-data-post.md)
