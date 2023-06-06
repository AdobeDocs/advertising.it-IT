---
title: Informazioni sull’automazione della gestione degli annunci tramite i feed di inventario
description: Scopri la gestione avanzata delle campagne, che consente di gestire automaticamente la struttura dell’account e di distribuire annunci dinamici in base ai dati sull’inventario di prodotti o servizi.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 0%

---

# Informazioni sull’automazione della gestione degli annunci tramite i feed di inventario

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (solo azioni di eliminazione), e [!DNL Yandex] solo account*

Il [!UICONTROL Campaigns] > [!UICONTROL Advanced (ACM)] view for advanced campaign management (visualizza per la gestione avanzata delle campagne) consente di creare e aggiornare automaticamente la struttura degli account di rete degli annunci e di distribuire annunci dinamici in base ai dati sull’inventario di prodotti o servizi. Puoi caricare nuovi file con dati di prodotto ogni giorno o con la frequenza desiderata, oppure puoi collegarti direttamente a un [!DNL Google] o [!DNL Microsoft®] account del centro commerciale. Utilizza la funzione per:

* Crea nuove campagne da origini dati ordinate.

* Aggiornare dinamicamente il testo e gli annunci adattabili della ricerca, [!DNL Google Ads] acquisti pubblicitari, oppure [!DNL Microsoft® Advertising] annunci commerciali ogni volta che vengono elaborati nuovi dati, utilizzando variabili dinamiche per elementi di dati modificabili (come prezzo o quantità). Ogni volta che modifichi i dati, gli annunci esistenti vengono eliminati e quelli nuovi vengono creati.

* Metti in pausa o rimuovi automaticamente gruppi di annunci, parole chiave e annunci quando il materiale scende sotto un livello specifico, in base a una data di fine specificata, o quando un componente esistente viene omesso dai dati di feed.

Per impostare gli annunci, crea modelli di feed inventario contenenti variabili (segnaposto), quindi sostituisci le variabili con colonne di dati effettive da un file caricato o da un [Account Google o Microsoft® merchant center sincronizzato](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). Le variabili possono anche includere gruppi di modificatori impostati in un file o singole righe nel file per creare più annunci, parole chiave, campagne o gruppi di annunci per ogni riga applicabile nel file di dati. Ad esempio, se utilizzi una variabile di gruppo di modificatori in un titolo di un annuncio e il gruppo di modificatori include due modificatori (&quot;per economico&quot; e &quot;a sconto&quot;), vengono creati due annunci separati per ciascun prodotto, uno per ciascun modificatore. Per [!DNL Google Ads] e [!DNL Microsoft® Advertising] annunci di ricerca dinamica, puoi anche includere valori per le personalizzazioni degli annunci.

| [!UICONTROL Ad Variation] Sezione del modello | Modificatori in Search, Social e Commerce | Contenuti feed | Annunci risultanti |
|----|----|----|----|
| Titolo: Buy high-end \{<i>Categoria di prodotto</i>\} &lt;<i>CheapList</i>>.<br><br>Descrizione 1: Inventario enorme di \{<i>Nome prodotto</i>\}.<br><br>Descrizione 2: disponibile in \{<i>Percentuale sconto</i>\}% sconto. | Valori per il gruppo di modificatori &quot;CheapList&quot;:<br><br>&quot;a buon mercato&quot;<br><br>&quot;con uno sconto&quot; | Categoria prodotto,Nome prodotto,Percentuale sconto<br>elettronica,iPod,10<br><br>abbigliamento,camicie,15<br><br><b>Nota:</b> È possibile separare i valori con virgole o schede. | <u>Comprare elettronica di fascia alta a buon mercato.</u><br>Enorme inventario di compresse. Disponibile con uno sconto del 10%.<br><br><u>Acquista prodotti di elettronica di fascia alta a prezzi scontati.</u><br>Enorme inventario di compresse. Disponibile con uno sconto del 10%.<br><br><u>Comprare abbigliamento di fascia alta a buon mercato.</u><br>Enorme inventario di camicie. Disponibile con uno sconto del 15%.<br><br><u>Compra abbigliamento di fascia alta a prezzi scontati.</u><br>Enorme inventario di camicie. Disponibile con uno sconto del 15%. |

Una volta generati gli annunci, puoi facoltativamente rivederli e quindi pubblicarli nella rete di annunci.

>[!NOTE]
>Per creare o modificare in blocco i dati della campagna utilizzando i file dei fogli di calcolo, vedi &quot;[Informazioni sulla gestione dei dati della campagna tramite bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).&quot;

>[!MORELIKETHIS]
>
>* [Flusso di lavoro per la gestione dei dati della campagna tramite i feed di inventario](inventory-feeds-workflow.md)
>* [Quando vengono creati o eliminati i componenti del conto dai feed di inventario?](when-are-components-created-deleted.md)

