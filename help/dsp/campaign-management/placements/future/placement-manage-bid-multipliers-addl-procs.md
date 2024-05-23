---
title: Gestire i moltiplicatori delle offerte per i posizionamenti
description: Informazioni xxx
feature: DSP Placements
source-git-commit: c0dd18a3ce8759214813b7303c590a28febf1b37
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 0%

---

# XXX

## Gestire i moltiplicatori delle offerte per un singolo posizionamento

1. Nel menu principale, fai clic su **[!UICONTROL Campaigns]**.

1. Fai clic sul nome della campagna.

1. Nel sottomenu, fai clic su **[!UICONTROL Placements]**.

1. Accanto al nome del posizionamento, fate clic su  **[!UICONTROL ...]** > **[!UICONTROL Bid Multiplier]**.

1. Regola i moltiplicatori di offerta per gli obiettivi idonei:

   * Per regolare manualmente i valori del moltiplicatore di offerta, passa a ciascuno [scheda specifica del target](#bid-multiplier-by-target) ([!UICONTROL Geo], [!UICONTROL Inventory], [!UICONTROL Sites], [!UICONTROL Audience], e [!UICONTROL Brand Safety]) e modificare i valori esistenti per le destinazioni di posizionamento.

     La maggior parte delle categorie target elenca le sottocategorie a sinistra. Fai clic su una sottocategoria per gestire i moltiplicatori di offerte per quella sottocategoria, a seconda dei casi.

   * Per caricare un file CSV con valori del moltiplicatore di offerta in modo da sovrascrivere tutti i valori esistenti:

      1. Clic **[!UICONTROL CSV File Edit]** in alto a destra.

      1. A) fare clic su **[!UICONTROL Download Template]** e modificare il file o b) modificare un modello scaricato in precedenza. Salvare il file modificato sul dispositivo o sulla rete.

         I fogli di calcolo scaricati includono un foglio per ogni tipo di oggetto (ad esempio Paese, Origini e Categoria sito). Sono inclusi solo i moltiplicatori di offerte esistenti con valori &lt; 1,0 o > 1,0.

         * Per aggiungere un moltiplicatore di offerta per una destinazione esistente, inserisci la destinazione utilizzando la stessa sintassi visibile nell’interfaccia utente e il corrispondente valore del moltiplicatore di offerta.

         * Per rimuovere un modificatore di offerta, imposta il valore del moltiplicatore di offerta su 1,0 oppure elimina tutte le informazioni relative alla riga.

         ![Riga di esempio in un file di foglio di calcolo del moltiplicatore di offerte](/help/dsp/assets/bid-multiplier-spreadsheet.png "Riga di esempio in un file di foglio di calcolo del moltiplicatore di offerte")

      1. Clic **[!UICONTROL Next]** per passare al [!UICONTROL Upload File] e a) trascinare e rilasciare il file modificato nella casella oppure b) fare clic all&#39;interno della casella per selezionare il file dal dispositivo o dalla rete.

      1. Verifica i dati caricati in [!UICONTROL Review & Submit] e quindi fare clic su **[!UICONTROL Save]**.

## Gestire i moltiplicatori delle offerte per uno o più posizionamenti

<!-- verify all and edit accordingly -->

1. Nel menu principale, fai clic su **[!UICONTROL Campaigns]**.

1. Fai clic sul nome della campagna.

1. Nel sottomenu, fai clic su **[!UICONTROL Placements]**.

1. Seleziona la casella di controllo accanto a ciascun posizionamento di cui desideri gestire i moltiplicatori di offerta.

1. Nella barra degli strumenti Azioni in blocco, fai clic su **[!UICONTROL ...]** > **[!UICONTROL Upload Bid Multiplier Excel Sheet]**.

<!-- Check the following this functionality when available in UAT -->

1. Regola i moltiplicatori di offerta per gli obiettivi idonei:

   * Per regolare manualmente i valori del moltiplicatore di offerta, passa a ogni scheda specifica per l’oggetto ([!UICONTROL Geo], [!UICONTROL Inventory], [!UICONTROL Sites], [!UICONTROL Audience], e[!UICONTROL Brand Safety]) e modificare i valori esistenti per le destinazioni di posizionamento.

   Le stesse modifiche si applicano a tutti i posizionamenti selezionati.

* Per caricare un file CSV con valori del moltiplicatore di offerta in modo da sovrascrivere tutti i valori esistenti:

   1. Clic **[!UICONTROL CSV File Edit]** in alto a destra.

   1. A) fare clic su **[!UICONTROL Download Template]** e modificare il file o b) modificare un modello scaricato in precedenza. Salvare il file modificato sul dispositivo o sulla rete.

      I fogli di calcolo scaricati includono un foglio per ogni tipo di oggetto (ad esempio Paese, Origini e Categoria sito). Sono inclusi solo i moltiplicatori di offerte esistenti con valori &lt; 1,0 o > 1,0.

      * Per aggiungere un moltiplicatore di offerta per una destinazione esistente, inserisci la destinazione utilizzando la stessa sintassi visibile nell’interfaccia utente e il corrispondente valore del moltiplicatore di offerta.

      * Per rimuovere un modificatore di offerta, imposta il valore del moltiplicatore di offerta su 1,0 oppure elimina tutte le informazioni relative alla riga.

      ![Riga di esempio in un file di foglio di calcolo del moltiplicatore di offerte](/help/dsp/assets/bid-multiplier-spreadsheet.png "Riga di esempio in un file di foglio di calcolo del moltiplicatore di offerte")

   1. Clic **[!UICONTROL CSV Edit]** in alto a destra.

   1. A) fare clic su **[!UICONTROL Download Template]** e modificare i valori del moltiplicatore di offerta o b) modificare un modello scaricato in precedenza. Salvare il file modificato sul dispositivo o sulla rete.

   1. A) trascinare e rilasciare il file modificato nella casella o b) fare clic all&#39;interno della casella per selezionare il file dal dispositivo o dalla rete.

   1. Clic **[!UICONTROL Upload]**.

1. Clic **[!UICONTROL Save]**.

## Tipi di target idonei per i moltiplicatori di offerte {#bid-multiplier-by-target}

non copiato qui

## Numero massimo di moltiplicatori di offerte per tipo di destinazione {#bid-multiplier-limits-by-target}

non copiato qui

<!--

>[!MORELIKETHIS]
>
>* [About Placement Management](placement-about.md)
>* [Edit Placements](placement-edit.md)
>* [View the Change Log for a Placement](placement-change-log.md)
>* [Placement Settings](placement-settings.md)
 -->
