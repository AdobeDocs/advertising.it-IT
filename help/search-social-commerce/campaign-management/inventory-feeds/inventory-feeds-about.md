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

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (solo azioni di eliminazione), e [!DNL Yandex] solo account*

Il [!UICONTROL Campaigns] > [!UICONTROL Advanced (ACM)] view for advanced campaign management (visualizza per la gestione avanzata delle campagne) consente di creare e aggiornare automaticamente la struttura degli account di rete degli annunci e di distribuire annunci dinamici in base ai dati sull’inventario di prodotti o servizi. Puoi caricare nuovi file con dati di prodotto ogni giorno o con la frequenza desiderata, oppure puoi collegarti direttamente a un [!DNL Google] o [!DNL Microsoft] account del centro commerciale. Utilizza la funzione per:

* Crea nuove campagne da origini dati ordinate.

* Aggiornare dinamicamente il testo e gli annunci adattabili della ricerca, [!DNL Google Ads] acquisti pubblicitari, oppure [!DNL Microsoft Advertising] annunci commerciali ogni volta che vengono elaborati nuovi dati, utilizzando variabili dinamiche per elementi di dati modificabili (come prezzo o quantità). Ogni volta che modifichi i dati, gli annunci esistenti vengono eliminati e quelli nuovi vengono creati.

* Metti in pausa o rimuovi automaticamente gruppi di annunci, parole chiave e annunci quando il materiale scende sotto un livello specifico, in base a una data di fine specificata, o quando un componente esistente viene omesso dai dati di feed.

Per impostare gli annunci, crea modelli di feed inventario contenenti variabili (segnaposto), quindi sostituisci le variabili con colonne di dati effettive da un file caricato o da un [Account Google o Microsoft Merchant Center sincronizzato](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). Le variabili possono anche includere gruppi di modificatori impostati in un file o singole righe nel file per creare più annunci, parole chiave, campagne o gruppi di annunci per ogni riga applicabile nel file di dati. Ad esempio, se utilizzi una variabile di gruppo di modificatori in un titolo di un annuncio e il gruppo di modificatori include due modificatori (&quot;per economico&quot; e &quot;a sconto&quot;), vengono creati due annunci separati per ciascun prodotto, uno per ciascun modificatore. Per [!DNL Google Ads] e [!DNL Microsoft Advertising] annunci di ricerca dinamica, puoi anche includere valori per le personalizzazioni degli annunci.

| [!UICONTROL Ad Variation] Sezione del modello | Modificatori in Search, Social e Commerce | Contenuti feed | Annunci risultanti |
|----|----|----|----|
| Titolo: Buy high-end \{<i>Categoria di prodotto</i>\} &lt;<i>CheapList</i>>.<br><br>Descrizione 1: Inventario enorme di \{<i>Nome prodotto</i>\}.<br><br>Descrizione 2: disponibile in \{<i>Percentuale sconto</i>\}% sconto. | Valori per il gruppo di modificatori &quot;CheapList&quot;:<br><br>&quot;a buon mercato&quot;<br><br>&quot;con uno sconto&quot; | Categoria prodotto,Nome prodotto,Percentuale sconto<br>elettronica,iPod,10<br><br>abbigliamento,camicie,15<br><br><b>Nota:</b> È possibile separare i valori con virgole o schede. | <u>Comprare elettronica di fascia alta a buon mercato.</u><br>Enorme inventario di compresse. Disponibile con uno sconto del 10%.<br><br><u>Acquista prodotti di elettronica di fascia alta a prezzi scontati.</u><br>Enorme inventario di compresse. Disponibile con uno sconto del 10%.<br><br><u>Comprare abbigliamento di fascia alta a buon mercato.</u><br>Enorme inventario di camicie. Disponibile con uno sconto del 15%.<br><br><u>Compra abbigliamento di fascia alta a prezzi scontati.</u><br>Enorme inventario di camicie. Disponibile con uno sconto del 15%. |

Una volta generati gli annunci, puoi facoltativamente rivederli e quindi pubblicarli nella rete di annunci.

>[!NOTE]
>Per creare o modificare in blocco i dati della campagna utilizzando i file dei fogli di calcolo, vedi &quot;[Informazioni sulla gestione dei dati della campagna tramite bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).&quot;

## Flusso di lavoro per la gestione dei dati della campagna tramite i feed di inventario

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (solo azioni di eliminazione), e [!DNL Yandex] solo account*

Inizialmente, eseguire il test di almeno un file di feed o un account, quindi automatizzare completamente il processo o continuare a controllarlo in ogni passaggio:

1. (Facoltativo) Contatta il team dell’account Adobe per impostare una directory FTP per il deposito dei file di dati.

   Se si utilizza la directory FTP, il servizio di feed verifica la presenza di nuovi file ogni due ore.

   In caso contrario, puoi caricare manualmente i file nel [!UICONTROL Advanced (ACM)] visualizzazione.

1. Imposta [parametri per l’elaborazione dei dati di feed](feed-settings-manage.md#feed-data-settings).

   Se utilizzi l’FTP, non inviare automaticamente i dati alle reti di annunci inizialmente. Dopo aver verificato l’output del primo file e aver ottenuto i risultati desiderati, puoi modificare le impostazioni.

1. Caricare un file di dati nella directory FTP, [caricare manualmente un file di dati](feed-files-manage.md) nel [!UICONTROL Advanced (ACM) view], o [abilitare l’accesso a un account Google o Microsoft merchant center](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

Per caricare manualmente i file, puoi attendere finché non crei un modello che utilizza il file di dati.

1. (Facoltativo) Crea gruppi di [modificatori](modifiers-manage.md) da utilizzare come variabili in vari campi di dati nei modelli di dati dei feed.

1. [Creare uno o più modelli](ad-templates/ad-template-manage.md) che utilizzano le colonne di dati per creare campagne, gruppi di annunci, parole chiave e/o copie di annunci per un account di rete di annunci specifico.

1. [Propagazione dei dati di feed tramite i modelli](feed-data-propagate.md), che sostituisce i nomi delle colonne nel modello con i dati nel file o nel conto. A seconda delle opzioni del modello, Cerca, Social e Commerce creano una nuova struttura dell’account (campagne, gruppi di annunci, parole chiave) per gli annunci utilizzando le impostazioni predefinite oppure mappano gli annunci alla struttura dell’account esistente.

1. (Facoltativo) [Anteprima dell’output](propagated-data-view.md) nel [!UICONTROL Advanced (ACM)] e, se lo si desidera, visualizzare un riepilogo delle modifiche apportate ai dati [!UICONTROL Propagations] scheda.

1. [Pubblica i dati](propagated-data-post.md) ai pertinenti account di rete pubblicitaria.

1. (Se per caricare i dati utilizzi l’FTP o un account del centro commerciale, facoltativo) Dopo aver convalidato l’output del primo file di feed, [modificare i parametri](feed-settings-manage.md#feed-data-settings) per propagare automaticamente i dati successivi tramite i modelli associati e inviarli alle reti di annunci pertinenti.

1. (Quando disponi di nuovi file di dati) Se necessario, carica nuovi file, propaga i dati tramite modelli e invia i dati alla rete di annunci pertinente. Facoltativamente, puoi propagare e pubblicare i dati in un unico passaggio.

>[!MORELIKETHIS]
>
>* [Quando vengono creati o eliminati i componenti del conto dai feed di inventario?](when-are-components-created-deleted.md)
