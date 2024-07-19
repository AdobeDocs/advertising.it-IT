---
title: Configurare le impostazioni dei dati dei feed
description: Scopri come configurare le impostazioni che controllano la modalità di elaborazione dei dati dei feed.
exl-id: 7eaac751-ecdf-4e73-9eae-a961bd9b7360
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '1155'
ht-degree: 0%

---

# Configurare le impostazioni dei dati dei feed

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (elimina solo azioni) e [!DNL Yandex] account solo*

Puoi configurare la gestione dei gruppi di annunci, delle parole chiave e degli annunci nei file di dati dei feed e la modalità di elaborazione dei dati in specifici file FTP, tramite le impostazioni dei feed.

1. Nel menu principale, fare clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Nella barra degli strumenti sopra la tabella dati, fare clic su **[!UICONTROL Settings]**.

1. Specificare le [impostazioni dei dati di feed](#feed-data-settings):

   1. Nella sezione [!UICONTROL Obsolete Item Auto-Processing], seleziona le informazioni nei campi.

   1. (Inserzionisti che caricano dati tramite FTP o tramite un collegamento diretto a un account di un centro commerciale) Nella sezione [!UICONTROL FTP/GMC Account Auto-Processing], seleziona le informazioni nei campi.

   1. Nella sezione [!UICONTROL Miscellaneous Auto-Processing], seleziona le informazioni nei campi.

1. Fare clic su **[!UICONTROL Save]**.

## Impostazioni dei dati dei feed {#feed-data-settings}

**[!UICONTROL Enable obsolete item auto-processing for]:** Applica tutte le impostazioni [!UICONTROL Obsolete Item Auto-processing] a:

* *[!UICONTROL Ad Groups Only]:* solo gruppi di annunci obsoleti.

* *[!UICONTROL Keywords Only]:* Solo parole chiave e gruppi di prodotti obsoleti.

* *[!UICONTROL Ad Variations Only]* (impostazione predefinita): solo annunci obsoleti.

* *[!UICONTROL Keywords and Ad Variations]:* sia parole chiave obsolete/target di prodotto/gruppi di prodotti che annunci obsoleti.

>[!NOTE]
>
>* Per [!DNL Google Ads] annunci di acquisto, è interessato solo il gruppo di prodotti di livello più basso.
>* Per gli account [!DNL Yandex], le attività di elaborazione automatica degli elementi obsolete vengono sempre eseguite sulle varianti degli annunci, indipendentemente da questa impostazione.

**[!UICONTROL When the Scheduled End Date is reached]:** (solo dati pubblicati manualmente) Cosa fare con gli elementi di riga in un file di feed pubblicato con una data e un&#39;ora di fine specificate una volta arrivata l&#39;ora di fine:

* *[!UICONTROL Delete]* (impostazione predefinita): elimina tutti i componenti rilevanti quando arriva l&#39;ora di fine specificata. Non puoi annullare questa operazione.

* *[!UICONTROL Pause]:* Sospendi tutti i componenti rilevanti quando arriva l&#39;ora di fine specificata. Se necessario, puoi riattivare i componenti in un secondo momento.

* *[!UICONTROL None]:* Non modificare lo stato dei componenti rilevanti.

**[!UICONTROL Missing line items in a manually uploaded feed]:** Cosa fare con gli elementi esistenti quando non sono inclusi in un nuovo file di feed caricato manualmente o quando non sono mappati su campagne o gruppi di annunci esistenti in base alle impostazioni Solo mappa nel modello:

* *[!UICONTROL Delete]:* Eliminare i componenti esistenti.

* *[!UICONTROL Pause]:* Sospendere i componenti esistenti. Vengono riattivati se un nuovo file di feed contiene gli stessi elementi di riga e conservano la cronologia e i punteggi di qualità. **Nota:** se mancano tutti i gruppi di prodotti figlio per un gruppo di prodotti padre, il gruppo di prodotti padre viene eliminato perché non è possibile sospendere i gruppi di prodotti.

* *[!UICONTROL None]* (impostazione predefinita): non modificare i componenti esistenti.

**[!UICONTROL Missing line items in an FTP feed/GMC account]:** Operazioni con gli elementi esistenti quando 1) non sono inclusi a) in un nuovo file di feed caricato in una directory FTP o b) in un account di un centro commerciale alla successiva sincronizzazione di Search, Social e Commerce con esso oppure 2) quando non sono mappati su campagne o gruppi di annunci esistenti in base alle impostazioni [!UICONTROL Map Only] nel modello.

* *[!UICONTROL Delete]:* Eliminare i componenti esistenti.

* *[!UICONTROL Pause]:* Sospendere i componenti esistenti. Vengono riattivati se i nuovi dati contengono uno degli stessi elementi e mantengono la cronologia e il punteggio di qualità. **Nota:** se mancano tutti i gruppi di prodotti figlio per un gruppo di prodotti padre, il gruppo di prodotti padre viene eliminato perché non è possibile sospendere i gruppi di prodotti.

* *[!UICONTROL None]* (impostazione predefinita): non modificare i componenti esistenti.

**[!UICONTROL When a numeric stock level reaches N units, or where a text-based value is 'out of stock']:** Cosa fare con gli elementi di riga che includono un livello di stock quando:

* (Per i feed con valori di stock solo numerici nella colonna specificata) Il livello di stock è pari o inferiore a una quantità specificata. La quantità predefinita è zero (0).

* (Per i feed con valori di testo nella colonna specificata) Il valore per [!UICONTROL Availability] è &quot;[!UICONTROL out of stock]&quot;; il valore non fa distinzione tra maiuscole e minuscole. **Nota:** **nei modelli di feed, indicare le colonne a livello di stock basate su testo utilizzando la casella di controllo per &quot;[!UICONTROL This column has non-numeric values]&quot;.&quot;

Seleziona l’azione per entrambi i casi:

* *[!UICONTROL Delete]* (impostazione predefinita) Elimina i componenti.

* *[!UICONTROL Pause]:* Sospendere i componenti. Quando i dati vengono aggiornati, i componenti vengono riattivati se i valori numerici delle scorte superano la quantità specificata o se [!UICONTROL Availability] è &quot;[!UICONTROL in stock]&quot; o &quot;[!UICONTROL preorder]&quot;. I componenti mantengono la cronologia e il punteggio di qualità.

Il livello di magazzino per ogni riga proviene da una colonna nel file di feed, come specificato nel campo &quot;[!UICONTROL Stock Level]&quot; per ogni modello.

>[!TIP]
>
>* Per i prodotti o i servizi per i quali si prevede di effettuare il riassortimento o aumentare la disponibilità, è consigliabile sospendere i gruppi di annunci, le parole chiave e gli annunci anziché eliminarli e ricrearli. La messa in pausa consente di mantenere i punteggi di qualità.
>* Se abiliti l’elaborazione automatica obsoleta per i gruppi di annunci e i nuovi dati includono un livello di stock per il gruppo di annunci, è significativo eliminare o mettere in pausa il gruppo di annunci solo quando il livello di stock specificato è a livello di categoria anziché a livello di marchio/articolo. Ad esempio, se hai un gruppo di annunci &quot;convertibili&quot;, il livello di stock per il gruppo di annunci deve essere il totale di tutti i singoli modelli convertibili rappresentati nel gruppo di annunci.

**[!UICONTROL Propagate feed data through all applicable templates]:** (gli inserzionisti caricano i file di dati tramite FTP o un account del centro commerciale) propaga automaticamente i nuovi dati tramite i modelli applicabili. L’opzione è selezionata per impostazione predefinita. Se disattivi l’opzione, puoi comunque propagare manualmente i dati per qualsiasi file di feed, account o modello.

>[!NOTE]
>
>* Per i file FTP, il servizio di feed verifica la presenza di aggiornamenti nella directory FTP ogni due ore (ore pari nel fuso orario PST). Questa opzione elabora tutti i file caricati dall’ultimo controllo.
>* Per gli account del centro commerciale, Search, Social e Commerce si sincronizzano con l’account ogni giorno alle 06:00 circa nel fuso orario dell’inserzionista. Questa opzione elabora tutti i dati aggiornati dall&#39;ultima sincronizzazione.
>* I dati propagati sono disponibili dalle schede [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] e [!UICONTROL Ads] fino a quando non vengono inviati alla rete di annunci o alla visualizzazione [!UICONTROL Bulksheets].

**[!UICONTROL Post to the SE]:** (gli inserzionisti caricano i file di dati tramite FTP o un account del centro commerciale) crea automaticamente i file dei fogli collettivi nei formati corretti per le reti pubblicitarie pertinenti dopo che i nuovi dati sono stati propagati tramite i modelli applicabili. Questa opzione rimuove anche i dati dalle schede [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] e [!UICONTROL Ads], a meno che non si verifichino errori in eventuali sottocomponenti.

Questa opzione è disabilitata per impostazione predefinita. Per abilitare questa opzione, selezionare la casella di controllo e quindi specificare se inviare i file di bulksheet alle reti di annunci:

* *[!UICONTROL Immediately]* (impostazione predefinita): pubblica i file dei fogli collettivi nelle reti pubblicitarie pertinenti dopo che i dati sono stati propagati tramite i modelli. I file del bulksheet rimangono disponibili nella visualizzazione [!UICONTROL Bulksheets] per 30 giorni.

* *[!UICONTROL Preview in Bulksheet Management area only, post later]:** Non pubblica i file dei fogli collettivi nelle reti di annunci pertinenti, ma li elenca nella visualizzazione [!UICONTROL Bulksheets], da cui puoi pubblicarli in un secondo momento. I file del bulksheet rimangono disponibili nella visualizzazione [!UICONTROL Bulksheets] per 30 giorni. Quando il file bulksheet è superiore a 10 MB ma inferiore a 2 GB, il file è in formato ZIP; non è necessario decomprimere il file per pubblicarlo. **Suggerimento:** se non hai convalidato in precedenza le pagine di destinazione, utilizza questa opzione per convalidarle dalla visualizzazione [!UICONTROL Bulksheets] prima di pubblicare i dati nella rete di annunci.

**[!UICONTROL Exclude keywords from posting when keyword length is greater than]:** impedisce la pubblicazione di frasi di parole chiave con più di un numero specificato di parole nella rete di annunci. Quando questa opzione è selezionata, le frasi delle parole chiave con un numero di parole superiore al massimo vengono propagate ed elencate nella scheda [!UICONTROL Keywords], ma non vengono pubblicate quando si tenta di pubblicare i dati.

Questa opzione è disattivata per impostazione predefinita, in modo che vengano pubblicate tutte le parole chiave, indipendentemente dal numero di parole incluse nella frase. Se si seleziona questa opzione, selezionare il numero massimo di parole da inserire (da 3 a 10).

>[!MORELIKETHIS]
>
>* [Informazioni sui feed inventario](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [Propagazione dei dati di feed tramite modelli](/help/search-social-commerce/campaign-management/inventory-feeds/feed-data-propagate.md)
>* [Pubblica i dati della campagna generati dai feed alle reti di annunci](propagated-data-post.md)
