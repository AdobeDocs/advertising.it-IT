---
title: Visualizza avvisi
description: Scopri come visualizzare gli avvisi e le risoluzioni consigliate per le campagne e i componenti della campagna.
feature: DSP Campaigns, DSP Packages, DSP Placements, DSP Ads, DSP Campaign Data Views
source-git-commit: 70592355207ba43341eb208750dcd3fc00db51c1
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 0%

---

# Visualizza avvisi

*Funzione beta*

L’DSP ti aiuta a identificare quando uno qualsiasi dei componenti delle campagne o della campagna presenta dei problemi. Per ogni problema, l’DSP crea un avviso con una marca temporale e l’azione consigliata per risolverlo. I motivi per gli avvisi includono problemi di configurazione (ad esempio, quando non vengono allegati annunci a un posizionamento o quando un’offerta non è configurata correttamente), rifiuto di annunci e problemi di integrità della campagna (come consegna di annunci scadente o prestazioni insoddisfacenti). Gli avvisi sono disponibili a livello di campagna, pacchetto, posizionamento, annuncio e offerta.

Gli avvisi sono disponibili nelle seguenti posizioni:

* A [!UICONTROL Pulse Panel] icona in [!UICONTROL Campaigns], [!UICONTROL Packages] e i dettagli dei colli, [!UICONTROL Placements], e [!UICONTROL Ads] visualizzazioni indica se sono disponibili avvisi per gli elementi della visualizzazione. Quando l’icona è contrassegnata da un punto blu (![Icona del pannello Pulse quando sono disponibili gli avvisi](/help/dsp/assets/alerts-panel.png "Icona del pannello Pulse quando sono disponibili gli avvisi")), gli avvisi sono disponibili. Se non è visibile alcun punto (![Icona del pannello Pulse quando non sono disponibili avvisi](/help/dsp/assets/alerts-panel-empty.png "Icona del pannello Pulse quando non sono disponibili avvisi")), non sono disponibili avvisi.

* Le tabelle di dati nelle stesse visualizzazioni includono un &quot;[!UICONTROL Alerts]&quot;che indica quando un elemento (o i suoi componenti) presenta un problema. Gli indicatori di avviso includono &quot;Critico&quot; (![Critico](/help/dsp/assets/indicator-critical.png "Critico")), &quot;Attenzione&quot; (![Avvertenza](/help/dsp/assets/indicator-warning.png "Avvertenza")), e &quot;Information&quot; (![Informazioni](/help/dsp/assets/indicator-information.png "Informazioni")).

Puoi aprire la relativa vista di gestione delle campagne per qualsiasi avviso, in modo da poter modificare le impostazioni in base alle esigenze per risolvere il problema.

È inoltre possibile scegliere di ignorare un singolo avviso, rimuovendolo dal [!UICONTROL Pulse] pannello.

Gli avvisi e gli indicatori di avviso scompaiono automaticamente quando vengono risolti i problemi sottostanti.

## Visualizzare gli avvisi in [!UICONTROL Pulse Panel]

1. Nel menu principale, fai clic su **[!UICONTROL Campaigns]**.

1. Effettua una delle seguenti operazioni:

   * (Per tutti gli avvisi applicabili alla visualizzazione) A destra della barra degli strumenti in qualsiasi visualizzazione di gestione delle campagne, fai clic su ![Icona del pannello Pulse quando sono disponibili gli avvisi](/help/dsp/assets/alerts-panel.png "Icona del pannello Pulse quando sono disponibili gli avvisi").

   * (Per tutti gli avvisi per una campagna specifica) Fare clic sull&#39;indicatore di avviso per una riga della campagna, quindi fare clic su **[!UICONTROL View in Pulse panel]**.

   * (Per tutti gli avvisi per un pacchetto, posizionamento o annuncio specifico) Effettua le seguenti operazioni:

      1. Fai clic sul nome della campagna.

      1. Nel sottomenu, fai clic su **[!UICONTROL Packages]**, **[!UICONTROL Placements]**, o **[!UICONTROL Ads]** per aprire la vista del componente campaign rilevante.

      1. Fare clic sull&#39;indicatore di avviso per una raccolta, un posizionamento o una riga di annuncio e quindi fare clic su **[!UICONTROL View in Pulse Panel]**.

   Sono elencati tutti gli avvisi associati alla campagna e ai suoi componenti, comprese le offerte mirate. Per impostazione predefinita, gli avvisi critici vengono elencati per primi.

1. (Facoltativo) Per raggruppare gli avvisi in base alla loro prima data di rilevamento, oppure per filtrarli in base allo stato, allo stato, al tipo o al nome di una specifica campagna, fai clic su ![Pulsante Filtro](/help/dsp/assets/filter.png) nell’angolo superiore destro del pannello, seleziona le opzioni di filtro e fai clic su **[!UICONTROL Apply]**.

1. Per visualizzare un elenco di tutti i componenti della campagna interessati per un tipo di avviso specifico, fai clic sul nome dell’avviso, ad esempio &quot;[!UICONTROL Package: No Active Placement (*N*)]&quot;. Per visualizzare i dettagli di ciascun componente interessato, inclusa l’azione consigliata, fai clic su [!UICONTROL EXPAND ALL] oppure fai clic sul nome del componente. Per aprire la vista di gestione delle campagne relativa a qualsiasi componente interessato in modo da poter apportare le modifiche consigliate, posiziona il cursore sul nome del componente e fai clic su ![Vai alla visualizzazione](/help/dsp/assets/go-to-view.png "Vai alla visualizzazione").

1. (Facoltativo) Per ignorare (nascondere) un avviso, posiziona il cursore sul nome del componente e fai clic su ![Ignora](/help/dsp/assets/alert-ignore.png "Ignora")e quindi fare clic su **[!UICONTROL Ignore indefinitely]**.  <!-- **[!UICONTROL Ignore alert for three days]**, **[!UICONTROL Ignore alert until next check]**, or **[!UICONTROL Ignore indefinitely] -->

Hai qualche secondo per annullare l’azione, dopo aver ignorato un avviso. Una volta chiuso il messaggio di opzione, non puoi annullare l’azione.

1. (Facoltativo) Per recuperare gli avvisi ignorati, filtra gli avvisi in modo da visualizzare un’ [!UICONTROL Alert Status] di &quot;[!UICONTROL All]&quot; o &quot;[!UICONTROL Ignored].&quot; Per non ignorare un avviso, posiziona il cursore sul nome del componente e fai clic su ![Annulla ignora](/help/dsp/assets/alert-un-ignore.png "Annulla ignora").

## Chiudi [!UICONTROL Pulse Panel]

* A destra della barra degli strumenti, fai clic su ![Icona del pannello Pulse quando sono disponibili gli avvisi](/help/dsp/assets/alerts-panel.png "Icona del pannello Pulse quando sono disponibili gli avvisi") o ![Icona del pannello Pulse quando non sono disponibili avvisi](/help/dsp/assets/alerts-panel-empty.png "Icona del pannello Pulse quando non sono disponibili avvisi").

>[!MORELIKETHIS]
>
>* [Tipi di rapporti sulle prestazioni nelle visualizzazioni di Campaign Management](campaign-reports-about.md)
