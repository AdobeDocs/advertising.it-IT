---
title: Crea un  [!DNL Excel]  modello per un feed di report foglio di calcolo
description: Scopri come creare modelli di fogli di calcolo con formattazione speciale.
exl-id: 74bf3cdf-7d56-431a-8aff-11ed3840a7cd
feature: Search Reports
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# Creare un modello [!DNL Excel] per un feed di report di foglio di calcolo

*Solo per report di base e report di precisione modello*

Per creare feed di fogli di calcolo, è necessario innanzitutto creare modelli di fogli di calcolo [!DNL Microsoft Excel] con formattazione speciale utilizzando modelli di report standard. Facoltativamente, è possibile personalizzare il foglio di calcolo [!DNL Excel] per includere colonne e grafici aggiuntivi.

1. In **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**, generare il tipo di report desiderato utilizzando un&#39;unità [!UICONTROL Date Aggregation] di &quot;[!UICONTROL Daily]&quot; e con tutti gli altri parametri di dati desiderati, salvando il report come modello.

   >[!NOTE]
   >
   > * È possibile creare feed del foglio di calcolo per i report [!UICONTROL Portfolio], [!UICONTROL Search Engine], [!UICONTROL Search Engine Account], [!UICONTROL Campaign], [!UICONTROL Ad Group], [!UICONTROL Ad Variation], [!UICONTROL Keyword] e [!UICONTROL Forecast Accuracy]. Se utilizzi [!UICONTROL Ad Group Report], limita il numero di gruppi di annunci inclusi per ottenere risultati più rapidi.
   > * L&#39;unità [!UICONTROL Date Range] definita nel modello non viene utilizzata. Definirai le date per le quali aggiornare i dati quando configuri il feed del foglio di calcolo in un secondo momento.

1. Dopo la generazione del report, vai a **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]** ed esporta una versione TSV o XLS dell&#39;output del report in un file.

1. In [!DNL Excel], creare un modello personalizzato per il report:

   1. Aprire il file del report in [!DNL Excel].

   1. Preparare la cartella di lavoro:

      1. Elimina le righe superiori che mostrano i parametri del rapporto. Per i file XLS, eliminare anche la riga &quot;[!UICONTROL Total]&quot;. Facoltativamente è possibile eliminare alcune righe di dati, ma mantenere a) la riga dell&#39;intestazione dati con tutte le colonne nell&#39;ordine originale e b) almeno una riga di dati. Non aggiungere manualmente dati.

         >[!NOTE]
         >
         > La colonna finale deve includere valori diversi da zero.

      2. Ordinare i dati in base alla data di inizio in ordine crescente (dal meno recente al più recente).

      3. Modificare il nome della scheda del foglio di lavoro da &quot;[!UICONTROL Sheet1]&quot; a &quot;[!UICONTROL RAW]&quot;.

         Questo nome di scheda specifico consente di aggiornare i dati.

      4. (Facoltativo) Se necessario, aggiungi colonne personalizzate a destra delle colonne del modello di rapporto.

   1. (Facoltativo) In un foglio di lavoro separato, creare una tabella pivot. Al termine, fare clic con il pulsante destro del mouse in una cella della tabella pivot e selezionare **[!UICONTROL Pivot Table Options]**, fare clic sulla scheda **[!UICONTROL Data]** e quindi selezionare **[!UICONTROL Refresh data when opening the file]**.

   1. Salvare il file come foglio di calcolo [!DNL Excel] in formato .XLSX.

>[!MORELIKETHIS]
>
>* [Informazioni sui feed di report del foglio di calcolo](spreadsheet-feed-about.md)
>* [Creare un feed di report per fogli di calcolo](spreadsheet-feed-create.md)
>* [Modifica impostazioni feed report foglio di calcolo](spreadsheet-feed-edit.md)
>* [Impostazioni feed report foglio di calcolo](spreadsheet-feed-settings.md)
>* [Visualizzare o salvare un file di feed di report del foglio di calcolo](spreadsheet-feed-view-or-save.md)
>* [Aggiorna manualmente i feed dei report del foglio di calcolo](spreadsheet-feed-refresh.md)
>* [Elimina feed report foglio di calcolo](spreadsheet-feed-delete.md)
