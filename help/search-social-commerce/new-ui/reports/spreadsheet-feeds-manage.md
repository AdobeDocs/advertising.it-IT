---
title: (Nuova interfaccia) Gestione dei feed dei rapporti sui fogli di calcolo
description: Scopri come creare, configurare, aggiornare, visualizzare ed eliminare feed di rapporti di fogli di calcolo che forniscono dati sulle prestazioni giornaliere in un foglio di calcolo personalizzato.
feature: Search Reports
source-git-commit: 38ee8dfbaf82d8f1d212a931956398444e61060f
workflow-type: tm+mt
source-wordcount: '1492'
ht-degree: 0%

---

# (Nuova interfaccia) Gestione dei feed dei rapporti sui fogli di calcolo

*Solo per report di base e report di precisione modello*

<!-- Update link to notifications once available -->

I feed dei fogli di calcolo forniscono dati sulle prestazioni giornaliere per tutti i report di base e i report di precisione dei modelli in un formato di foglio di calcolo personalizzato in [!DNL Microsoft Excel] XLSX. È possibile impostare i feed del foglio di calcolo utilizzando modelli di foglio di calcolo [!DNL Excel] appositamente formattati creati da modelli di report standard. Ogni giorno, il foglio di calcolo viene aggiornato automaticamente a un’ora specificata con nuovi dati non elaborati aggregati quotidianamente. I dati non elaborati popolano le colonne e i grafici inclusi nel modello del foglio di calcolo. Quando un file di feed del foglio di calcolo è disponibile o se la generazione del file non riesce, ogni destinatario e-mail nel modello di report riceve una notifica, in base alle [impostazioni di notifica configurate dall&#39;utente per i report](/help/search-social-commerce/notifications/notification-about.md).

Puoi configurare il feed in modo che venga aggiornato fino agli ultimi 90 giorni di dati e che tutti i dati esistenti precedenti rimangano invariati.

Nella visualizzazione [!UICONTROL Reports] > [!UICONTROL Spreadsheets Feeds] sono elencati tutti i feed del foglio di calcolo creati. Da questa vista è possibile creare feed di fogli di calcolo, aggiornare manualmente un feed o eliminare un feed.

## Azioni disponibili

* [Crea un  [!DNL Excel]  modello per un feed di report foglio di calcolo](#spreadsheet-feed-create-excel-template)

* [Creare un feed di report per fogli di calcolo](#spreadsheet-feed-create)

* [Modifica impostazioni feed report foglio di calcolo](#spreadsheet-feed-edit)

* [Visualizzare o salvare un file di feed di report del foglio di calcolo](#spreadsheet-feed-view-or-save)

* [Aggiorna manualmente i feed dei rapporti del foglio di calcolo](#spreadsheet-feed-refresh)

* [Eliminare i feed dei report del foglio di calcolo](#spreadsheet-feed-delete)

## Creare un modello [!DNL Excel] per un feed di report di foglio di calcolo {#spreadsheet-feed-create-excel-template}

<!-- Add x-refs when available -->

Per creare feed di fogli di calcolo, è necessario innanzitutto creare modelli di fogli di calcolo [!DNL Microsoft Excel] con formattazione speciale utilizzando modelli di report standard. Facoltativamente, è possibile personalizzare il foglio di calcolo [!DNL Excel] per includere colonne e grafici aggiuntivi.

1. In **[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]**, generare il tipo di report desiderato utilizzando un&#39;unità [!UICONTROL Date Aggregation] di &quot;[!UICONTROL Daily]&quot; e con tutti gli altri parametri di dati desiderati, salvando il report come modello.

   >[!NOTE]
   >
   > * È possibile creare feed del foglio di calcolo per i report [!UICONTROL Portfolio], [!UICONTROL Search Engine], [!UICONTROL Search Engine Account], [!UICONTROL Campaign], [!UICONTROL Ad Group], [!UICONTROL Ad Variation], [!UICONTROL Keyword] e [!UICONTROL Forecast Accuracy]. Se utilizzi [!UICONTROL Ad Group Report], limita il numero di gruppi di annunci inclusi per ottenere risultati più rapidi.
   > * L&#39;unità [!UICONTROL Date Range] definita nel modello non viene utilizzata. Definirai le date per le quali aggiornare i dati quando configuri il feed del foglio di calcolo in un secondo momento.

1. Dopo la generazione del report, passare a **[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]** ed esportare una versione TSV o XLS dell&#39;output del report in un file.

1. In [!DNL Excel], creare un modello personalizzato per il report:

   1. Aprire il file del report in [!DNL Excel].

   1. Preparare la cartella di lavoro:

      1. Elimina le righe superiori che mostrano i parametri del rapporto. Per i file XLS, eliminare anche la riga &quot;[!UICONTROL Total]&quot;. Facoltativamente è possibile eliminare alcune righe di dati, ma mantenere a) la riga dell&#39;intestazione dati con tutte le colonne nell&#39;ordine originale e b) almeno una riga di dati. Non aggiungere manualmente dati.

         >[!NOTE]
         >
         > La colonna finale deve includere valori diversi da zero.

      1. Ordinare i dati in base alla data di inizio in ordine crescente (dal meno recente al più recente).

      1. Modificare il nome della scheda del foglio di lavoro da &quot;[!UICONTROL Sheet1]&quot; a &quot;[!UICONTROL RAW]&quot;.

         Questo nome di scheda specifico consente di aggiornare i dati.

      1. (Facoltativo) Se necessario, aggiungi colonne personalizzate a destra delle colonne del modello di rapporto.

   1. (Facoltativo) In un foglio di lavoro separato, creare una tabella pivot. Al termine, fare clic con il pulsante destro del mouse in una cella della tabella pivot e selezionare **[!UICONTROL Pivot Table Options]**, fare clic sulla scheda **[!UICONTROL Data]** e quindi selezionare **[!UICONTROL Refresh data when opening the file]**.

   1. Salvare il file come foglio di calcolo [!DNL Excel] in formato .XLSX.

## Creare un feed di report per fogli di calcolo {#spreadsheet-feed-create}

1. [Crea il  [!DNL Excel] modello da compilare con i dati del report](#spreadsheet-feed-create-excel-template).

1. Creare il feed del foglio di calcolo:

   1. Nel menu principale, fare clic su **[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**.

   1. In alto a destra, fare clic su **[!UICONTROL Create Spreadsheet]**.

   1. Nella finestra di dialogo **[!UICONTROL Create Spreadsheet Feed]**, specifica le [impostazioni feed foglio di calcolo](#spreadsheet-feed-settings).

   1. Fare clic su **[!UICONTROL Submit]**.

   1. (Facoltativo) Una volta che il feed [!UICONTROL Update Status] è *[!UICONTROL Finished]*, fai clic su **[!UICONTROL XLSX]** accanto al feed, quindi apri o salva il file in base alla normale procedura del browser.

      >[!NOTE]
      >
      >Se il modello di rapporto associato al feed viene successivamente eliminato, anche il feed viene eliminato.

      I feed del foglio di calcolo vengono aggiornati automaticamente ogni giorno al [!UICONTROL Schedule Time] configurato. Se il modello di rapporto include indirizzi per qualsiasi destinatario e-mail, tali indirizzi ricevono notifiche quando il foglio di calcolo viene aggiornato.

## Modifica impostazioni feed report foglio di calcolo {#spreadsheet-feed-edit}

>[!NOTE]
>
> Se si modificano le colonne nel modello di report o si utilizza un modello di report nuovo o aggiornato, è necessario aggiornare il modello [!DNL Excel] di conseguenza e caricarlo nuovamente.

1. (Facoltativo) Per aggiornare il modello di report o il modello [!DNL Excel] utilizzato per il feed del foglio di calcolo:

   * (Facoltativo) Per utilizzare un modello di report diverso o aggiornato per il feed, [crea un nuovo [!DNL Excel] modello per il modello di report](#spreadsheet-feed-create-excel-template).

     Nei passaggi successivi verranno caricati sia il modello di report che il nuovo file [!DNL Excel].

   * (Facoltativo) Per aggiungere semplicemente colonne personalizzate al modello [!DNL Excel], inserire le colonne a destra delle colonne dal modello di report, quindi salvare il file come foglio di calcolo [!DNL Excel] in formato XLSX. Caricare il nuovo file [!DNL Excel] nel passaggio successivo.

1. Nel menu principale, fare clic su **[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**.

1. Modificare le impostazioni del feed del foglio di calcolo:

   1. Seleziona la casella di controllo accanto al nome del feed del foglio di calcolo.

   1. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL Edit]**.

   1. Nella finestra di dialogo [!UICONTROL Create Spreadsheet Feed]<!-- sic -->, modifica le [impostazioni feed foglio di calcolo](#spreadsheet-feed-settings).

   1. Fare clic su **[!UICONTROL Submit]**.

   1. (Facoltativo) Una volta che il feed [!UICONTROL Update Status] è *[!UICONTROL Finished]*, fai clic su **[!UICONTROL XLSX]** accanto al feed, quindi apri o salva il file in base alla normale procedura del browser.

   >[!NOTE]
   >
   > Se il modello di rapporto associato al feed viene successivamente eliminato, anche il feed viene eliminato.

   I feed dei fogli di calcolo vengono aggiornati automaticamente alle ore 08:00 di ogni giorno nel fuso orario dell&#39;inserzionista. Se il modello di rapporto include indirizzi per qualsiasi destinatario e-mail, tali indirizzi ricevono notifiche quando il foglio di calcolo viene aggiornato.

## Impostazioni feed report foglio di calcolo {#spreadsheet-feed-settings}

| Campo | Descrizione |
|---|---|
| [!UICONTROL Feed Name] | Un nome per il feed del foglio di calcolo. |
| [!UICONTROL Report Template] | Il modello di report che specifica i dati del report richiesti; selezionare quello utilizzato per creare il modello [!DNL Excel]. Sono elencati tutti i modelli di report di base.<br><br><b>Nota:</b> Se si modifica il modello di report utilizzato per il report o si aggiornano le colonne nel modello, è necessario creare e caricare un nuovo modello [!DNL Excel]. |
| [!UICONTROL Excel Template] | Il modello [!DNL Excel] appositamente formattato creato in formato .XLSX, che viene applicato ai dati specificati nel modello di report. Specificare il file da caricare immettendo il percorso completo e il nome del file oppure facendo clic su <b>[!UICONTROL Browse]</b> per individuare il file nel dispositivo o nella rete. |
| [!UICONTROL Back Fill From] | Data di inizio per la quale vengono aggiornati i dati esistenti nella scheda [!UICONTROL RAW], rappresentata da un numero di giorni nel passato. Immetti un valore massimo di 90 giorni; il valore predefinito è sette (7) giorni.<br><br>Ad esempio, se il valore è 7 e oggi è 7 marzo, i dati esistenti nella scheda [!UICONTROL RAW] a partire dal 1 marzo verranno aggiornati (fino alla data di fine specificata dal parametro [!UICONTROL Back Fill Until]). Le righe di dati esistenti per le date precedenti al 1° marzo non vengono eliminate, ma non vengono aggiornate. |
| [!UICONTROL Back Fill Until] | Data di fine per la quale i dati esistenti nella scheda [!UICONTROL RAW] vengono aggiornati, rappresentata da un numero di giorni nel passato. Il valore predefinito è un (1) giorno.<br><br>Ad esempio, se il valore è 1 e oggi è 7 marzo, i dati esistenti nella scheda [!UICONTROL RAW] verranno aggiornati fino al 6 marzo e a partire dalla data di inizio specificata dal parametro [!UICONTROL Back Fill From]. Se questo valore è 1, il parametro [!UICONTROL Back Fill Until] è 7 e oggi è 7 marzo, i dati esistenti nella scheda [!UICONTROL RAW] vengono aggiornati dal 1° marzo al 6 marzo. In entrambi gli esempi, le righe di dati esistenti per le date successive al 6 marzo non vengono eliminate, ma non vengono aggiornate. |
| [!UICONTROL Email Recipients] | Indirizzi e-mail a cui inviare notifiche ogni volta che il report viene aggiornato o ogni volta che il report viene eseguito quando il modello include una pianificazione. Per impostazione predefinita, viene immesso l’indirizzo dell’account utente. Per specificare più indirizzi, separali con virgole, spazi o nuove righe. |
| [!UICONTROL Schedule Time] | Ora di aggiornamento dei feed del foglio di calcolo: alle ore 08:00 o a qualsiasi ora compresa tra le ore 10:00 e 23:00 nel fuso orario dell&#39;inserzionista. Il valore predefinito per i nuovi feed di fogli di calcolo è 10:00.<br><br><b>Nota:</b> Per motivi di prestazioni, non è possibile aggiornare i feed di fogli di calcolo a 09:00 quando vengono generati altri report. |
| [!UICONTROL Email Notification] | (Quando si specificano i destinatari e-mail) Cosa includere nelle notifiche e-mail a qualsiasi indirizzo specificato:<ul><li><i>[!UICONTROL Attach feed]</i> — Per inviare una copia del report completato in formato XLSX. Se il file supera i 10 MB, la notifica non include un allegato.</li><li><i>[!UICONTROL Notification Only]</i> (impostazione predefinita) - Per inviare solo una notifica del completamento o dell&#39;errore del report, con un collegamento al report.</li></ul> |

## Visualizzare o salvare un file di feed di report del foglio di calcolo {#spreadsheet-feed-view-or-save}

Puoi visualizzare qualsiasi feed di foglio di calcolo generato o salvarlo in un file. I file di feed del foglio di calcolo sono in formato XLSX [!DNL Microsoft Excel].

1. Nel menu principale, fare clic su **[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**.

1. Fai clic su **[!UICONTROL XLSX]** accanto al feed, quindi apri o salva il file in base alla normale procedura del browser.

## Aggiorna manualmente i feed dei rapporti del foglio di calcolo {#spreadsheet-feed-refresh}

>[!NOTE]
>
>I feed dei fogli di calcolo vengono aggiornati automaticamente alle 08:00 ogni giorno nel fuso orario locale.

1. Nel menu principale, fare clic su **[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**.

1. Selezionare la casella di controllo accanto a ogni feed da aggiornare.

1. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL Run Spreadsheet]**.

1. Nel messaggio di conferma, fare clic su **[!UICONTROL Confirm]**.

1. (Facoltativo) Quando il [!UICONTROL Update Status] di un feed è *[!UICONTROL Finished]*, fai clic su **[!UICONTROL XLSX]** accanto al feed, quindi apri o salva il file in base alla normale procedura del browser.

## Eliminare i feed dei report del foglio di calcolo {#spreadsheet-feed-delete}

>[!NOTE]
>
>Se il modello di rapporto associato a un feed viene eliminato, il feed viene eliminato automaticamente.

1. Nel menu principale, fare clic su **[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**.

1. Seleziona la casella di controllo accanto a ciascun feed da eliminare.

1. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL Delete]**.

1. Nel messaggio di conferma, fare clic su **[!UICONTROL Confirm]**.
