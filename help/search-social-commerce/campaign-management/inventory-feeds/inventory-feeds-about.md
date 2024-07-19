---
title: Informazioni sull’automazione della gestione degli annunci tramite i feed di inventario
description: Scopri la gestione avanzata delle campagne, che consente di gestire automaticamente la struttura dell’account e di distribuire annunci dinamici in base ai dati sull’inventario di prodotti o servizi.
exl-id: 46e78f32-96ef-4a23-bbe3-f18b84309463
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '838'
ht-degree: 0%

---

# Informazioni sull’automazione della gestione degli annunci tramite i feed di inventario

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (elimina solo azioni) e [!DNL Yandex] account solo*

La vista [!UICONTROL Campaigns] > [!UICONTROL Advanced (ACM)] per la gestione avanzata delle campagne consente di creare e aggiornare automaticamente la struttura degli account di rete degli annunci e di distribuire annunci dinamici in base ai dati sull&#39;inventario dei prodotti o dei servizi. Puoi caricare nuovi file con i dati di prodotto ogni giorno o con la frequenza desiderata, oppure collegarti direttamente a un account del centro commerciale [!DNL Google] o [!DNL Microsoft]. Utilizza la funzione per:

* Crea nuove campagne da origini dati ordinate.

* Aggiorna dinamicamente il testo e gli annunci di ricerca responsive, [!DNL Google Ads] annunci di acquisto o [!DNL Microsoft Advertising] annunci di acquisto ogni volta che vengono elaborati nuovi dati, utilizzando variabili dinamiche per elementi di dati modificabili (come prezzo o quantità). Ogni volta che modifichi i dati, gli annunci esistenti vengono eliminati e quelli nuovi vengono creati.

* Metti in pausa o rimuovi automaticamente gruppi di annunci, parole chiave e annunci quando il materiale scende sotto un livello specifico, in base a una data di fine specificata, o quando un componente esistente viene omesso dai dati di feed.

Per impostare gli annunci, crea modelli di feed inventario contenenti variabili (segnaposto), quindi sostituisci le variabili con colonne di dati effettive da un file caricato o da un account [Google o Microsoft Merchant Center sincronizzato](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). Le variabili possono anche includere gruppi di modificatori impostati in un file o singole righe nel file per creare più annunci, parole chiave, campagne o gruppi di annunci per ogni riga applicabile nel file di dati. Ad esempio, se utilizzi una variabile di gruppo di modificatori in un titolo di un annuncio e il gruppo di modificatori include due modificatori (&quot;per economico&quot; e &quot;a sconto&quot;), vengono creati due annunci separati per ciascun prodotto, uno per ciascun modificatore. Per [!DNL Google Ads] e [!DNL Microsoft Advertising] annunci di ricerca dinamica, puoi anche includere valori per le personalizzazioni degli annunci.

| [!UICONTROL Ad Variation] sezione del modello | Modificatori in Search, Social e Commerce | Contenuti feed | Annunci risultanti |
|----|----|----|----|
| Titolo: Acquista il prodotto di fascia alta \{<i>Categoria di prodotto</i>\} &lt;<i>Elenco economico</i>>.<br><br>Descrizione 1: inventario di \{<i>Nome prodotto</i>\}.<br><br>Descrizione 2: disponibile con sconto di \{<i>Percentuale sconto</i>\}%. | Valori per il gruppo di modificatori &quot;CheapList&quot;:<br><br>&quot;a buon mercato&quot;<br><br>&quot;con uno sconto&quot; | Categoria prodotto,Nome prodotto,Percentuale sconto<br>elettronica,iPod,10<br><br>abbigliamento,Camicie,15<br><br><b>Nota:</b> è possibile separare i valori con virgole o tabulazioni. | <u>Acquista prodotti di elettronica di fascia alta a buon mercato.</u><br>Enorme inventario di tablet. Disponibile con uno sconto del 10%.<br><br><u>Acquista prodotti di elettronica di fascia alta con uno sconto.</u><br>Enorme inventario di tablet. Disponibile con uno sconto del 10%.<br><br><u>Acquista capi di abbigliamento di alta qualità a buon mercato.</u><br>Enorme inventario di camicie. Disponibile con uno sconto del 15%.<br><br><u>Acquista capi di abbigliamento di alta qualità con uno sconto.</u><br>Enorme inventario di camicie. Disponibile con uno sconto del 15%. |

Una volta generati gli annunci, puoi facoltativamente rivederli e quindi pubblicarli nella rete di annunci.

>[!NOTE]
>Per creare o modificare i dati della campagna in blocco utilizzando i file del foglio di calcolo, vedere &quot;[Informazioni sulla gestione dei dati della campagna tramite i bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).&quot;

## Flusso di lavoro per la gestione dei dati della campagna tramite i feed di inventario

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (elimina solo azioni) e [!DNL Yandex] account solo*

Inizialmente, eseguire il test di almeno un file di feed o un account, quindi automatizzare completamente il processo o continuare a controllarlo in ogni passaggio:

1. (Facoltativo) Contatta il team dell’account Adobe per impostare una directory FTP per il deposito dei file di dati.

   Se si utilizza la directory FTP, il servizio di feed verifica la presenza di nuovi file ogni due ore.

   In caso contrario, è possibile caricare manualmente i file nella visualizzazione [!UICONTROL Advanced (ACM)].

1. Imposta [parametri per l&#39;elaborazione dei dati di feed](feed-settings-manage.md#feed-data-settings).

   Se utilizzi l’FTP, non inviare automaticamente i dati alle reti di annunci inizialmente. Dopo aver verificato l’output del primo file e aver ottenuto i risultati desiderati, puoi modificare le impostazioni.

1. Caricare un file di dati nella directory FTP, [caricare manualmente un file di dati](feed-files-manage.md) in [!UICONTROL Advanced (ACM) view] o [abilitare l&#39;accesso a un account Google o Microsoft Merchant Center](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

Per caricare manualmente i file, puoi attendere finché non crei un modello che utilizza il file di dati.

1. (Facoltativo) Crea gruppi di [modificatori](modifiers-manage.md) da utilizzare come variabili in vari campi di dati nei modelli di dati dei feed.

1. [Crea uno o più modelli](ad-templates/ad-template-manage.md) che utilizzano le colonne di dati per creare campagne, gruppi di annunci, parole chiave e/o copie di annunci per un account di rete di annunci specifico.

1. [Propagare i dati di feed tramite i modelli](feed-data-propagate.md), che sostituiscono i nomi delle colonne nel modello con i dati nel file o nell&#39;account. A seconda delle opzioni del modello, Cerca, Social e Commerce creano una nuova struttura dell’account (campagne, gruppi di annunci, parole chiave) per gli annunci utilizzando le impostazioni predefinite oppure mappano gli annunci alla struttura dell’account esistente.

1. (Facoltativo) [Visualizzare l&#39;anteprima dell&#39;output](propagated-data-view.md) nelle visualizzazioni [!UICONTROL Advanced (ACM)] e, facoltativamente, visualizzare un riepilogo delle modifiche apportate ai dati nella scheda [!UICONTROL Propagations].

1. [Pubblica i dati](propagated-data-post.md) negli account di rete degli annunci pertinenti.

1. (Se usi l&#39;FTP o un account del centro commerciale per caricare i dati; facoltativo) Dopo aver convalidato l&#39;output dal primo file di feed, [modifica i parametri](feed-settings-manage.md#feed-data-settings) per propagare automaticamente i dati successivi tramite i modelli associati e inviarli alle reti di annunci pertinenti.

1. (Quando disponi di nuovi file di dati) Se necessario, carica nuovi file, propaga i dati tramite modelli e invia i dati alla rete di annunci pertinente. Facoltativamente, puoi propagare e pubblicare i dati in un unico passaggio.

>[!MORELIKETHIS]
>
>* [Quando vengono creati o eliminati i componenti dell&#39;account dai feed di inventario?](when-are-components-created-deleted.md)
