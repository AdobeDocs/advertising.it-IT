---
title: Visualizza avvisi
description: Scopri come visualizzare gli avvisi e le risoluzioni consigliate per le campagne e i componenti della campagna.
feature: DSP Campaigns, DSP Packages, DSP Placements, DSP Ads, DSP Campaign Data Views
exl-id: 667bf1c3-3bad-4a1a-b907-0c9bfe5362a9
source-git-commit: 9ab8d3345659f48d1d131c3c6c1e1b87f0b0a0e6
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 0%

---

# Visualizza avvisi

DSP ti consente di identificare quando uno qualsiasi dei componenti delle campagne o della campagna presenta dei problemi. Per ogni problema, DSP crea un avviso con una marca temporale e l’azione consigliata per risolverlo. I motivi per gli avvisi includono problemi di configurazione (ad esempio, quando non vengono allegati annunci a un posizionamento o quando un’offerta non è configurata correttamente), rifiuto di annunci e problemi di integrità della campagna (come consegna di annunci scadente o prestazioni insoddisfacenti). Gli avvisi sono disponibili a livello di campagna, pacchetto, posizionamento, annuncio e offerta.

Gli avvisi sono disponibili nelle seguenti posizioni:

* Un&#39;icona [!UICONTROL Pulse Panel] nelle visualizzazioni [!UICONTROL Campaigns], [!UICONTROL Packages] e dei dettagli del pacchetto, [!UICONTROL Placements] e [!UICONTROL Ads] indica se sono disponibili avvisi per gli elementi in tale visualizzazione. Se l&#39;icona è blu (![Icona Pannello impulsi quando sono disponibili avvisi](/help/dsp/assets/alerts-panel.png "Icona Pannello impulsi quando sono disponibili avvisi")), gli avvisi sono disponibili. Se non è visibile alcun punto (![Icona del pannello Pulse quando non sono disponibili avvisi](/help/dsp/assets/alerts-panel-empty.png "Icona del pannello Pulse quando non sono disponibili avvisi")), non sono disponibili avvisi.

* Le tabelle dati nelle stesse visualizzazioni includono una colonna &quot;[!UICONTROL Alerts]&quot; che indica quando l&#39;elemento o i relativi componenti presentano un problema. Gli indicatori di avviso includono &quot;Critico&quot; (![Critico](/help/dsp/assets/indicator-critical.png "Critico")), &quot;Avviso&quot; (![Avvertenza](/help/dsp/assets/indicator-warning.png "Avvertenza")) e &quot;Informazioni&quot; (![Informazioni](/help/dsp/assets/indicator-information.png "Informazioni")).

Puoi aprire la relativa vista di gestione delle campagne per qualsiasi avviso, in modo da poter modificare le impostazioni in base alle esigenze per risolvere il problema.

È inoltre possibile scegliere di ignorare un singolo avviso, rimuovendolo dal pannello [!UICONTROL Pulse].

Gli avvisi e gli indicatori di avviso scompaiono automaticamente quando vengono risolti i problemi sottostanti.

## Visualizza avvisi in [!UICONTROL Pulse Panel]

1. Nel menu principale, fare clic su **[!UICONTROL Campaigns]**.

1. Effettua una delle seguenti operazioni:

   * (Per tutti gli avvisi applicabili alla visualizzazione) A destra della barra degli strumenti in qualsiasi visualizzazione di gestione delle campagne, fai clic sull&#39;icona ![Pannello Pulse quando gli avvisi sono disponibili](/help/dsp/assets/alerts-panel.png "Pannello Pulse quando gli avvisi sono disponibili").

   * (Per tutti gli avvisi per una campagna specifica) Fare clic sull&#39;indicatore di avviso per una riga della campagna, quindi fare clic su **[!UICONTROL View in Pulse panel]**.

   * (Per tutti gli avvisi per un pacchetto, posizionamento o annuncio specifico) Effettua le seguenti operazioni:

      1. Fai clic sul nome della campagna.

      1. Nel sottomenu, fare clic su **[!UICONTROL Packages]**, **[!UICONTROL Placements]** o **[!UICONTROL Ads]** per aprire la visualizzazione del componente della campagna pertinente.

      1. Fare clic sull&#39;indicatore di avviso per un pacchetto, un posizionamento o una riga di annuncio e quindi fare clic su **[!UICONTROL View in Pulse Panel]**.

   Sono elencati tutti gli avvisi associati alla campagna e ai suoi componenti, comprese le offerte mirate. Per impostazione predefinita, gli avvisi critici vengono elencati per primi.

1. (Inserzionisti con Advertising Creative; facoltativo) Fai clic sulla scheda **[!UICONTROL Creative]** per visualizzare gli avvisi per i posizionamenti che includono esperienze Advertising Creative.

1. (Facoltativo) Per raggruppare gli avvisi in base alla loro prima data di rilevamento, o per filtrarli in base allo stato, allo stato, al tipo di componente o al nome di una campagna specifica, fare clic sul pulsante ![Filtro](/help/dsp/assets/filter.png) in alto a destra del pannello, selezionare le opzioni di filtro e quindi fare clic su **[!UICONTROL Apply]**.

1. Per visualizzare un elenco di tutti i componenti della campagna interessati per un tipo di avviso specifico, fare clic sul nome dell&#39;avviso, ad esempio &quot;[!UICONTROL Package: No Active Placement (*N*)]&quot;. Per visualizzare i dettagli di ogni componente interessato, inclusa l&#39;azione consigliata, fare clic su [!UICONTROL EXPAND ALL] o sul nome del componente. Per aprire la visualizzazione di gestione delle campagne relativa a qualsiasi componente interessato in modo da poter apportare le modifiche consigliate, posizionare il cursore sul nome del componente e fare clic su ![Vai alla visualizzazione](/help/dsp/assets/go-to-view.png "Vai alla visualizzazione").

1. (Facoltativo) Per ignorare (nascondere) un avviso, posizionare il cursore sul nome del componente e fare clic su ![Ignora](/help/dsp/assets/alert-ignore.png "Ignora"), quindi fare clic su **[!UICONTROL Ignore alert till next check]**, **[!UICONTROL Ignore alert for 3 days]** o **[!UICONTROL Ignore indefinitely]**.

Hai qualche secondo per annullare l’azione, dopo aver ignorato un avviso. Una volta chiuso il messaggio di opzione, non puoi annullare l’azione.

1. (Facoltativo) Per recuperare gli avvisi ignorati, filtrare gli avvisi per visualizzare un [!UICONTROL Alert Status] di &quot;[!UICONTROL All]&quot; o &quot;[!UICONTROL Ignored]&quot;.&quot; Per annullare l&#39;eliminazione di un avviso, posizionare il cursore sul nome del componente e fare clic su ![Annulla ignora](/help/dsp/assets/alert-un-ignore.png "Annulla ignora").

## Chiudi [!UICONTROL Pulse Panel]

* A destra della barra degli strumenti, fare clic su ![Icona Pulse Panel quando sono disponibili avvisi](/help/dsp/assets/alerts-panel.png "Icona Pulse Panel quando sono disponibili avvisi") o ![Icona del pannello Pulse quando non sono disponibili avvisi](/help/dsp/assets/alerts-panel-empty.png "Icona del pannello Pulse quando non sono disponibili avvisi").

>[!MORELIKETHIS]
>
>* [Tipi di rapporti sulle prestazioni nelle visualizzazioni di gestione delle campagne](campaign-reports-about.md)
