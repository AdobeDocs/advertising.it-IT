---
title: Creare un [!DNL Excel] modello per un feed di report per fogli di calcolo
description: Scopri come creare modelli di fogli di calcolo con formattazione speciale.
exl-id: 74bf3cdf-7d56-431a-8aff-11ed3840a7cd
feature: Search Reports
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# Creare un [!DNL Excel] modello per un feed di report per fogli di calcolo

*Solo per report di base e report di accuratezza del modello*

Per creare feed di fogli di calcolo, è necessario innanzitutto creare un formato speciale [!DNL Microsoft Excel] modelli di fogli di calcolo che utilizzano modelli di report standard. Facoltativamente, puoi personalizzare [!DNL Excel] per includere colonne e grafici aggiuntivi.

1. In entrata **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**, genera il tipo di rapporto desiderato utilizzando un [!UICONTROL Date Aggregation] unità di &quot;[!UICONTROL Daily]&quot; e con tutti gli altri parametri di dati desiderati, salva il rapporto come modello.

   >[!NOTE]
   >
   > * È possibile creare feed di fogli di calcolo per [!UICONTROL Portfolio], [!UICONTROL Search Engine], [!UICONTROL Search Engine Account], [!UICONTROL Campaign], [!UICONTROL Ad Group], [!UICONTROL Ad Variation], [!UICONTROL Keyword], e [!UICONTROL Forecast Accuracy] rapporti. Se si utilizza [!UICONTROL Ad Group Report], limita il numero di gruppi di annunci inclusi per risultati più rapidi.
   > * Il [!UICONTROL Date Range] l&#39;unità definita nel modello non viene utilizzata. Definirai le date per le quali aggiornare i dati quando configuri il feed del foglio di calcolo in un secondo momento.

1. Dopo la generazione del rapporto, vai a **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]** ed esporta in un file una versione TSV o XLS dell’output del rapporto.

1. In entrata [!DNL Excel], crea un modello personalizzato per il rapporto:

   1. Apri il file del rapporto in [!DNL Excel].

   1. Preparare la cartella di lavoro:

      1. Elimina le righe superiori che mostrano i parametri del rapporto. Per i file XLS, elimina anche &quot;[!UICONTROL Total]&quot;. Facoltativamente è possibile eliminare alcune righe di dati, ma mantenere a) la riga dell&#39;intestazione dati con tutte le colonne nell&#39;ordine originale e b) almeno una riga di dati. Non aggiungere manualmente dati.

         >[!NOTE]
         >
         > La colonna finale deve includere valori diversi da zero.

      2. Ordinare i dati in base alla data di inizio in ordine crescente (dal meno recente al più recente).

      3. Cambia il nome della scheda del foglio di lavoro da &quot;[!UICONTROL Sheet1]&quot; a &quot;[!UICONTROL RAW].&quot;

         Questo nome di scheda specifico consente di aggiornare i dati.

      4. (Facoltativo) Se necessario, aggiungi colonne personalizzate a destra delle colonne del modello di rapporto.

   1. (Facoltativo) In un foglio di lavoro separato, creare una tabella pivot. Al termine, fare clic con il pulsante destro del mouse in una cella della tabella pivot e selezionare **[!UICONTROL Pivot Table Options]**, fare clic su **[!UICONTROL Data]** , quindi selezionare **[!UICONTROL Refresh data when opening the file]**.

   1. Salva il file come [!DNL Excel] in formato .XLSX.

>[!MORELIKETHIS]
>
>* [Informazioni sui feed di report dei fogli di calcolo](spreadsheet-feed-about.md)
>* [Creare un feed di report per fogli di calcolo](spreadsheet-feed-create.md)
>* [Modifica impostazioni feed report foglio di calcolo](spreadsheet-feed-edit.md)
>* [Impostazioni feed report foglio di calcolo](spreadsheet-feed-settings.md)
>* [Visualizzare o salvare un file di feed di report del foglio di calcolo](spreadsheet-feed-view-or-save.md)
>* [Aggiorna manualmente i feed dei rapporti del foglio di calcolo](spreadsheet-feed-refresh.md)
>* [Eliminare i feed dei report del foglio di calcolo](spreadsheet-feed-delete.md)
