---
title: Gestire i moltiplicatori delle offerte per i posizionamenti
description: Scopri come creare e modificare i moltiplicatori di offerta per i target di posizionamento.
feature: DSP Placements
exl-id: fbd44960-c9df-4713-94b7-13bcdb7e2568
source-git-commit: 18c68edec80a80d236df138c05fba8d857c9ed9e
workflow-type: tm+mt
source-wordcount: '907'
ht-degree: 1%

---

# Gestire i moltiplicatori delle offerte per i posizionamenti

Puoi creare e gestire i moltiplicatori di offerte, per i quali viene moltiplicata un&#39;offerta calcolata in modo algoritmico per aumentare o diminuire l&#39;offerta, per i tuoi obiettivi di posizionamento esistenti di [tipi di target idonei](#bid-multiplier-by-target). Puoi modificare manualmente i valori del moltiplicatore di offerte per un posizionamento o caricare un foglio di calcolo con valori per uno o più posizionamenti.

Per impostazione predefinita, il moltiplicatore di offerta per un target è 1,00, il che significa che l’offerta non viene adeguata per tale target. I valori possono essere compresi tra 0,10 e 10,00. Ad esempio, un moltiplicatore di offerta di 0,5 riduce un&#39;offerta di 6 USD a 3 USD (0,5 x 6). Quando un&#39;asta è idonea per più modificatori di offerta, tutti i moltiplicatori di offerta applicabili vengono moltiplicati. Ad esempio, se la California ha un moltiplicatore di offerta pari a 2 e San Francisco ha un moltiplicatore di offerta pari a 3, il moltiplicatore di offerta finale per gli annunci che vengono eseguiti a San Francisco è 6.

>[!NOTE]
>
>I moltiplicatori di offerte non aumentano mai l’offerta oltre l’offerta massima.

Puoi impostare i moltiplicatori di offerte (con valori diversi da 1,00) per un [numero limitato di destinazioni](#bid-multiplier-limits-by-target).

Questa funzione funziona con i target di posizionamento esistenti. Per modificare le destinazioni selezionate per i posizionamenti, vedi &quot;[Modifica posizionamenti](/help/dsp/campaign-management/placements/placement-edit.md).&quot;

## Gestire i moltiplicatori delle offerte per un singolo posizionamento

Puoi modificare manualmente i valori o caricare un foglio di calcolo per un singolo posizionamento.

1. Nel menu principale, fare clic su **[!UICONTROL Campaigns]**.

1. Fai clic sul nome della campagna.

1. Nel sottomenu fare clic su **[!UICONTROL Placements]**.

1. Accanto al nome del posizionamento, fare clic su **[!UICONTROL ...]** > **[!UICONTROL Edit]** > **[!UICONTROL Bid Multiplier]**.

1. Regola i moltiplicatori di offerta per gli obiettivi idonei:

   * Per regolare manualmente i valori del moltiplicatore di offerte, passa a ogni [scheda specifica per la destinazione](#bid-multiplier-by-target) ([!UICONTROL Geo], [!UICONTROL Inventory], [!UICONTROL Sites], [!UICONTROL Audience] e [!UICONTROL Brand Safety]) e modifica i valori esistenti per le destinazioni di posizionamento.

     La maggior parte delle categorie target elenca le sottocategorie a sinistra. Fai clic su una sottocategoria per gestire i moltiplicatori di offerte per quella sottocategoria, a seconda dei casi.

   * Per caricare un file CSV con valori del moltiplicatore di offerta in modo da sovrascrivere tutti i valori esistenti:

      1. Fai clic su **[!UICONTROL CSV File Edit]** in alto a destra.

      1. A) fare clic su **[!UICONTROL Download Template]** e modificare il file oppure b) modificare un modello scaricato in precedenza. Salvare il file modificato sul dispositivo o sulla rete.

         I fogli di calcolo scaricati includono un foglio per ogni tipo di oggetto (ad esempio Paese, Origini e Categoria sito). Sono inclusi solo i moltiplicatori di offerte esistenti con valori &lt; 1,0 o > 1,0.

         * Per aggiungere un moltiplicatore di offerta per una destinazione esistente, inserisci la destinazione utilizzando la stessa sintassi visibile nell’interfaccia utente e il corrispondente valore del moltiplicatore di offerta.

         * Per rimuovere un modificatore di offerta, imposta il valore del moltiplicatore di offerta su 1,0 oppure elimina tutte le informazioni relative alla riga.

         ![Riga di esempio in un file del foglio di calcolo del moltiplicatore di offerte](/help/dsp/assets/bid-multiplier-spreadsheet.png "Riga di esempio in un file del foglio di calcolo del moltiplicatore di offerte")

      1. Fare clic su **[!UICONTROL Next]** per passare alla sezione [!UICONTROL Upload File] e a) trascinare il file modificato nella casella oppure b) fare clic all&#39;interno della casella per selezionare il file dal dispositivo o dalla rete.

      1. Verificare i dati caricati nella sezione [!UICONTROL Review & Submit], quindi fare clic su **[!UICONTROL Save]**.

## Carica moltiplicatori di offerte per uno o più posizionamenti

Carica un foglio di calcolo per applicare gli stessi valori a tutti i posizionamenti selezionati.

1. Nel menu principale, fare clic su **[!UICONTROL Campaigns]**.

1. Fai clic sul nome della campagna.

1. Nel sottomenu fare clic su **[!UICONTROL Placements]**.

1. Seleziona la casella di controllo accanto a ciascun posizionamento di cui desideri gestire i moltiplicatori di offerta.

1. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL ...]** > **[!UICONTROL Upload Bid Multiplier Excel Sheet]**.

1. Carica un file CSV con valori del moltiplicatore di offerta per sovrascrivere tutti i valori esistenti per tutti i posizionamenti selezionati.

   1. A) fare clic su **[!UICONTROL Download Template]** e modificare il file oppure b) modificare un modello scaricato in precedenza. Salvare il file modificato sul dispositivo o sulla rete.

      I fogli di calcolo scaricati includono un foglio per ogni tipo di oggetto (ad esempio Paese, Origini e Categoria sito). Sono inclusi solo i moltiplicatori di offerte esistenti con valori &lt; 1,0 o > 1,0.

      * Per aggiungere un moltiplicatore di offerta per una destinazione esistente, inserisci la destinazione utilizzando la stessa sintassi visibile nell’interfaccia utente e il corrispondente valore del moltiplicatore di offerta.

      * Per rimuovere un modificatore di offerta, imposta il valore del moltiplicatore di offerta su 1,0 oppure elimina tutte le informazioni relative alla riga.

      ![Riga di esempio in un file del foglio di calcolo del moltiplicatore di offerte](/help/dsp/assets/bid-multiplier-spreadsheet.png "Riga di esempio in un file del foglio di calcolo del moltiplicatore di offerte")

   1. Fare clic su **[!UICONTROL Next]** per passare alla sezione [!UICONTROL Upload File] e a) trascinare il file modificato nella casella oppure b) fare clic all&#39;interno della casella per selezionare il file dal dispositivo o dalla rete.

   1. Verificare i dati caricati nella sezione [!UICONTROL Review & Submit], quindi fare clic su **[!UICONTROL Save]**.

## Tipi di target idonei per i moltiplicatori di offerte {#bid-multiplier-by-target}

Puoi configurare i modificatori di offerte solo per le destinazioni incluse e non per quelle escluse.

* **Destinazioni geografiche**: area geografica (paesi, stati e città), codici postali e DMA

* **Destinazioni inventario**: origini e feed per inventario pubblico e [!UICONTROL On Demand] inventario

* **Destinazioni del sito:** siti/app di destinazione (ma non esclusi), categorie del sito

* **Destinazioni pubblico:** segmenti, parti diurne e argomenti

* **ads.txt destinazioni:** (quando si rinuncia ad ads.txt, che consente di acquistare l&#39;inventario da tutti i venditori) ads.txt venditori solo, ads.txt venditori diretti e ads.txt venditori più siti senza annunci.txt <!-- bid multipliers for the different subsets of inventory; not available when the placement targets only one subset -->

## Numero massimo di moltiplicatori di offerte per tipo di destinazione {#bid-multiplier-limits-by-target}

Puoi impostare i moltiplicatori delle offerte (con valori diversi da 1,00) per un numero limitato di target. Ad esempio, puoi impostare i moltiplicatori di offerte per un massimo di 20 obiettivi per paese. Di seguito è elencato il numero massimo di target per ogni tipo di target che possono avere moltiplicatori di offerte.

| Categoria | Parametro | Numero massimo |
| -------- | --------- | ----- |
| Geo | Paese | 20 |
| Geo | Stato | 100 |
| Geo | Città | 100 |
| Geo | Metro | 100 |
| Geo | Codici postali | 100 |
| Inventario | Sorgenti | 100 |
| Inventario | Feed | 100 |
| Sites | Categoria sito | 100 |
| Sites | Siti/app | 100 |
| Pubblico | Segmenti | 500 |
| Pubblico | Argomenti | 100 |
| Sicurezza del marchio | Ads.txt | N/D |

>[!MORELIKETHIS]
>
>* [Informazioni sulla gestione del posizionamento](placement-about.md)
>* [Modifica posizionamenti](placement-edit.md)
>* [Visualizza il log delle modifiche per un posizionamento](placement-change-log.md)
>* [Impostazioni posizionamento](placement-settings.md)
