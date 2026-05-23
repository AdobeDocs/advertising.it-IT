---
title: (Nuova interfaccia) Gestire gli avvisi personalizzati
description: Scopri come creare, configurare, mettere in pausa, attivare, eliminare, visualizzare ed esportare avvisi personalizzati e modelli di avvisi.
feature: Search Alerts
source-git-commit: 0fddeb8f01bd7c310544973ae2aff78339eb2144
workflow-type: tm+mt
source-wordcount: '1065'
ht-degree: 0%

---

# (Nuova interfaccia) Gestire gli avvisi personalizzati

Crea modelli di avviso per identificare quando un portfolio, una campagna o un gruppo di annunci soddisfa condizioni specifiche, ad esempio una metrica di prestazioni, durante un periodo specificato, quindi genera un avviso. Gli avvisi sono disponibili per un singolo inserzionista. Gli avvisi includono tutte le colonne nella vista predefinita pertinente. Ad esempio, gli avvisi a livello di campagna includono tutte le colonne nella visualizzazione predefinita [!UICONTROL Campaigns].

È possibile creare modelli di avviso dalla scheda [!UICONTROL Alert Templates] nel pannello [!UICONTROL Custom Alerts] o dalla parte superiore di qualsiasi pagina.

Quando viene attivata un&#39;istanza di avviso per un modello di avviso:

* I destinatari specificati ricevono una notifica e-mail. Quando l&#39;avviso contiene fino a 1000 record, l&#39;avviso e-mail include un file [CSV](/help/search-social-commerce/glossary.md#c-d) con i dati dell&#39;avviso, inclusi i dati per tutte le entità che hanno attivato l&#39;avviso.

* L&#39;avviso è elencato nella scheda [!UICONTROL Triggered Alerts] nel pannello [!UICONTROL Custom Alert Templates].<!-- Not available as of 5/22 for alerts triggered the day before:  A downloadable report is available for ten days after the alert is triggered. -->

<!-- This doesn't seem to be true as of 5/22 -- check on this behavior:    * The alert is listed in the [!UICONTROL Notifications] center in the applicable entity view, which is available from the right toolbar. Notifications remain in the [!UICONTROL Notifications] center unless you delete them or mark them as read. -->

## Visualizzazione [!UICONTROL Custom Alerts]

Per aprire il pannello [!UICONTROL Custom Alerts], fai clic su ![Avviso personalizzato](/help/search-social-commerce/assets/custom-alert.png "Avviso personalizzato") in alto a destra.

Il pannello [!UICONTROL Custom Alerts] include la visualizzazione [!UICONTROL Alert Templates], che elenca tutti i modelli di avviso creati per l&#39;account e da cui è possibile creare, modificare, mettere in pausa, riattivare ed eliminare i modelli di avviso. Nella visualizzazione [!UICONTROL Triggered Alerts] sono elencate le istanze di avviso generate.

## Azioni disponibili

* [Visualizza avvisi attivati](#alert-view)

* [Visualizzare modelli di avvisi personalizzati](#alert-template-view)

* [Creare un modello di avviso personalizzato](#alert-template-create)

* [Modificare un modello di avviso personalizzato](#alert-template-edit)

* [Mettere in pausa un modello di avviso personalizzato](#alert-template-pause)

* [Attivare un modello di avviso personalizzato](#alert-template-activate)

* [Eliminare un modello di avviso personalizzato](#alert-template-delete)

<!-- Not available as of 5/22:  * [Export data for triggered alerts](#alert-export-data) -->

## Visualizza avvisi attivati {#alert-view}

1. In alto a destra, fare clic su ![Avviso personalizzato](/help/search-social-commerce/assets/custom-alert.png "Avviso personalizzato").

1. Fare clic sulla scheda **[!UICONTROL Triggered Alerts]**.

1. (Facoltativo) Filtra l’elenco per includere avvisi per un tipo di entità specifico o cerca una stringa di testo all’interno del nome del modello. Nelle query di ricerca non viene fatta distinzione tra maiuscole e minuscole.

## Visualizzare modelli di avvisi personalizzati {#alert-template-view}

1. Nell&#39;angolo superiore destro di qualsiasi pagina, fare clic su ![Avviso personalizzato](/help/search-social-commerce/assets/custom-alert.png "Avviso personalizzato"), che si apre nella scheda [!UICONTROL Alert Templates].

1. (Facoltativo) Filtra l’elenco per includere avvisi per un tipo di entità specifico o cerca una stringa di testo all’interno del nome del modello. Nelle query di ricerca non viene fatta distinzione tra maiuscole e minuscole.

1. (Facoltativo) Per visualizzare tutti i criteri per un modello di avviso, fare clic sul numero di criteri (ad esempio ![Pulsante Criteri di avviso personalizzati di esempio](/help/search-social-commerce/assets/custom-alert-criteria.png "Pulsante Criteri di avviso personalizzati di esempio").

## Creare un modello di avviso personalizzato {#alert-template-create}

I nuovi modelli di avviso hanno lo stato &quot;[!UICONTROL Active]&quot;.

1. Effettuare una delle seguenti operazioni:

   * In alto a destra, fare clic su ![Avviso personalizzato](/help/search-social-commerce/assets/custom-alert.png "Avviso personalizzato") > **[!UICONTROL Create Custom Alert]**.

   In alto a destra, fare clic su ![Avviso personalizzato](/help/search-social-commerce/assets/custom-alert.png "Avviso personalizzato") > **[!UICONTROL View Custom Alerts]**, che consente di aprire la scheda [!UICONTROL Alert Templates]. Fare clic su **[!UICONTROL Create Alert]**.

1. Specificare le [impostazioni degli avvisi](#alert-template-settings) nelle schede **[!UICONTROL Entity]**, **[!UICONTROL Date Range]**, **[!UICONTROL Filters]** e **[!UICONTROL Scheduling and Delivery]**.

   Puoi spostarti tra le schede facendo clic sul nome della scheda (ad esempio, &quot;Filtri&quot;) o facendo clic su **[!UICONTROL Next]** in basso a destra.

1. Nella scheda [!UICONTROL Summary], fare clic su **[!UICONTROL Create Alert]**.

## Modificare un modello di avviso personalizzato {#alert-template-edit}

1. In alto a destra, fai clic su ![Avviso personalizzato](/help/search-social-commerce/assets/custom-alert.png "Avviso personalizzato") > **[!UICONTROL View Custom Alerts]**, che si apre sulla scheda [!UICONTROL Alert Templates].

1. (Facoltativo) Filtra l’elenco per includere avvisi per un tipo di entità specifico o cerca una stringa di testo all’interno del nome del modello. Nelle query di ricerca non viene fatta distinzione tra maiuscole e minuscole.

1. Accanto al nome del modello, fare clic su ![Modifica](/help/search-social-commerce/assets/edit-new.png "Modifica").

1. Nella finestra [!UICONTROL Edit Custom Alert], modificare le [impostazioni degli avvisi](#alert-template-settings) nelle schede **[!UICONTROL Date Range]**, **[!UICONTROL Filters]** e **[!UICONTROL Scheduling and Delivery]**.

   Puoi spostarti tra le schede facendo clic sul nome della scheda (ad esempio, &quot;Filtri&quot;) o facendo clic su **[!UICONTROL Next]** in basso a destra.

1. Nella scheda [!UICONTROL Summary], fare clic su **[!UICONTROL Update Alert]**.

## Mettere in pausa un modello di avviso personalizzato {#alert-template-pause}

1. In alto a destra, fai clic su ![Avviso personalizzato](/help/search-social-commerce/assets/custom-alert.png "Avviso personalizzato") > **[!UICONTROL View Custom Alerts]**, che si apre sulla scheda [!UICONTROL Alert Templates].

1. (Facoltativo) Filtra l’elenco per includere avvisi per un tipo di entità specifico o cerca una stringa di testo all’interno del nome del modello. Nelle query di ricerca non viene fatta distinzione tra maiuscole e minuscole.

1. Nella riga del modello, selezionare *[!UICONTROL Paused]*.

## Attivare un modello di avviso personalizzato {#alert-template-activate}

1. In alto a destra, fai clic su ![Avviso personalizzato](/help/search-social-commerce/assets/custom-alert.png "Avviso personalizzato") > **[!UICONTROL View Custom Alerts]**, che si apre sulla scheda [!UICONTROL Alert Templates].

1. (Facoltativo) Filtra l’elenco per includere avvisi per un tipo di entità specifico o cerca una stringa di testo all’interno del nome del modello. Nelle query di ricerca non viene fatta distinzione tra maiuscole e minuscole.

1. Nella riga del modello, selezionare *[!UICONTROL Active]*.

## Eliminare un modello di avviso personalizzato {#alert-template-delete}

È possibile eliminare solo i modelli di avviso creati.

1. In alto a destra, fai clic su ![Avviso personalizzato](/help/search-social-commerce/assets/custom-alert.png "Avviso personalizzato") > **[!UICONTROL View Custom Alerts]**, che si apre sulla scheda [!UICONTROL Alert Templates].

1. (Facoltativo) Filtra l’elenco per includere avvisi per un tipo di entità specifico o cerca una stringa di testo all’interno del nome del modello. Nelle query di ricerca non viene fatta distinzione tra maiuscole e minuscole.

1. Nella riga del modello, fai clic su ![Elimina](/help/search-social-commerce/assets/delete-new.png "Elimina").

1. Nella finestra del messaggio di conferma, fare clic su **[!UICONTROL Delete]**.

## Impostazioni del modello di avviso personalizzato {#alert-template-settings}

| Linguetta | Parametro | Descrizione |
|--- |--- |--- |
|  | [!UICONTROL Name] | Il nome dell’avviso. Deve contenere almeno cinque caratteri. |
| [!UICONTROL Date Range] | [!UICONTROL Select Entity] | Tipo di entità da valutare: <i>[!UICONTROL Portfolio]</i>, <i>[!UICONTROL Campaign]</i> o <i>[!UICONTROL Ad Group]</i>. |
| [!UICONTROL Date Range] | [!UICONTROL Period] | L’intervallo di date per il quale valutare le condizioni per l’avviso. Le metriche vengono valutate in forma aggregata nell’intervallo di date. Le opzioni variano da *[!UICONTROL Yesterday]* a *[!UICONTROL Last 180 Days]*. |
| [!UICONTROL Filters] | \[Filtri definiti\] | Condizioni per l&#39;attivazione dell&#39;avviso all&#39;ora specificata nella scheda [!UICONTROL Scheduling and Delivery]. Le colonne disponibili variano in base al tipo di entità. Tutti i filtri vengono uniti utilizzando la funzione booleana AND, che significa che devono essere soddisfatte tutte le condizioni specificate.<ul><li><p>Per aggiungere un filtro, eseguire le operazioni seguenti:<p><ol><li><p>(Facoltativo) Per filtrare i nomi delle colonne in base alla stringa di testo, immettere la stringa di ricerca nel campo di input [!UICONTROL ADD FILTER].</p></li><li><p>Nell&#39;elenco delle colonne selezionare un nome di colonna.</p></li><li><p>Definisci il filtro per la colonna:</p></li><ul><li><p>(Filtri senza campi di input) Fare clic su ![Freccia giù](/help/search-social-commerce/assets/arrow-down-expand.png "Freccia giù") accanto al secondo menu, quindi selezionare le caselle di controllo accanto a ogni valore da includere.</p></li><li><p>(Tutti gli altri filtri con campi di input) Seleziona un operatore dal secondo menu, quindi inserisci il valore applicabile.</p><p>Ad esempio, se hai selezionato la colonna &quot;Clic&quot; e desideri restituire solo le righe con più di 100 clic, seleziona &quot;maggiore di&quot; e immetti 100 nel campo di input.</p><p>A seconda del tipo di dati, gli operatori disponibili possono includere <i>maggiore di</i>, <i>minore di</i>, <i>uguale a</i>, <i>contiene</i>, <i>non contiene</i>, <i>inizia con</i>, <i>termina con</i>, <i>nessun valore</i>, <i>ha valore</i>, <i>prima</i>, <i>dopo</i> o <i>nessuna data</i>.</p><p>**Nota:** i valori di testo non fanno distinzione tra maiuscole e minuscole. Ad esempio, se si filtra per campagne con &quot;prestito&quot; nel nome, i risultati potrebbero includere &quot;Prestiti al consumo&quot; e &quot;Applicazioni prestito&quot;.</p></li></ol><li><p>Per rimuovere un filtro, fare clic su ![Elimina](/help/search-social-commerce/assets/delete.png "Elimina") accanto alla definizione del filtro.</p></li></ul> |
| [!UICONTROL Scheduling and Delivery] | [!UICONTROL Trigger this Alert] \[quando\] | Con quale frequenza l’avviso controlla i filtri delle condizioni specificate e, quando vengono soddisfatte tutte le condizioni, invia notifiche e-mail:<ul><li><p>[!UICONTROL Daily at <*NN*> `[AM\|PM]`]</p></li><li><p>[!UICONTROL Weekly on <*Giorno della settimana*> alle &lt;*NN*> `[AM\|PM]`]</p></li><li><p>[!UICONTROL Every month on <*Giorno NN*> alle &lt;*NN*> `[AM\|PM]`]</p></li></ul>**Nota:** questo valore non influisce sul periodo di valutazione. |
|  | [!UICONTROL Email Recipients] | (Modificabile solo dal creatore del modello di avviso; sola lettura per tutti gli altri utenti) Utenti di ricerca, social network e Commerce registrati a cui inviare notifiche quando viene attivato un avviso. Per impostazione predefinita, viene selezionato il nome dell’account utente. Facoltativamente, aggiungi o rimuovi utenti con accesso ai dati dell’inserzionista.<br><br>Se l&#39;avviso include fino a 1000 record, al messaggio di posta elettronica viene allegata una versione CSV dell&#39;avviso. |

<!--

Not available as of 5/22:

## Export data for triggered alerts {#alert-export-data}

You can export data for a triggered alert or data for the most recently triggered alert for an alert template as a [!DNL Microsoft Excel] workbook ([XLS](/help/search-social-commerce/glossary.md#w-x) file), a tab-separated values ([TSV](/help/search-social-commerce/glossary.md#s-t)) file, or a comma-separated values ([CSV](/help/search-social-commerce/glossary.md#c-d)) file. Downloadable reports are available for ten days after the alert is triggered and are then automatically deleted.

1. Do either of the following:

   * (To export data for the most recently triggered alert for an alert template) In the upper right, click ![Custom Alert](/help/search-social-commerce/assets/custom-alert.png "Custom Alert") > **[!UICONTROL View Custom Alerts]**, which opens to the [!UICONTROL Alert Templates] tab.

   * (To export data for a specific triggered alert) In the upper right, click ![Custom Alert](/help/search-social-commerce/assets/custom-alert.png "Custom Alert"). Click **[!UICONTROL Triggered Alerts]**.

1. In the [!UICONTROL Export] column next to the template or report name, click the name of a format, and then open or save the file according to your browser's normal procedure:

   * **[!UICONTROL XLS]:** For an [!DNL Excel] workbook with a single worksheet (XLS). The report includes one worksheet, labeled at the top with the parameters, with one row for each included component when data for the component is available. Rows with no data are omitted. Basic reports include a total for each numeric column.

   * **[!UICONTROL TSV]:** For a TSV file. The report includes the parameters and one row for each included component.

   * **[!UICONTROL CSV]:** For a CSV file. The report includes the parameters and one row for each included component.

-->
