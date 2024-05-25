---
title: Gestire i moltiplicatori delle offerte per i posizionamenti
description: Scopri come creare e modificare i moltiplicatori di offerta per i target di posizionamento.
feature: DSP Placements
exl-id: fbd44960-c9df-4713-94b7-13bcdb7e2568
source-git-commit: 503b40a6b27dd41ebd63daf74d72865fdf41f528
workflow-type: tm+mt
source-wordcount: '613'
ht-degree: 2%

---

# Gestire i moltiplicatori delle offerte per i posizionamenti

Puoi creare e gestire i moltiplicatori di offerte, per i quali un&#39;offerta viene moltiplicata per aumentare o diminuire l&#39;offerta, per gli obiettivi di posizionamento esistenti di [tipi di target idonei](#bid-multiplier-by-target). Puoi modificare manualmente i valori del moltiplicatore di offerte o caricare un foglio di calcolo con i valori.

Per impostazione predefinita, il moltiplicatore di offerta per un target è 1,00, il che significa che l’offerta non viene adeguata per tale target. I valori possono essere compresi tra 0,10 e 10,00. Ad esempio, un modificatore di offerta di 0,5 riduce l&#39;offerta di 6 a 3 dollari (0,5 x 6). Quando un&#39;asta è idonea per più modificatori di offerta, tutti i modificatori di offerta applicabili vengono moltiplicati. I modificatori di offerta non aumentano mai l’offerta oltre l’offerta massima.

È possibile impostare i moltiplicatori delle offerte (con valori diversi da 1,00) per un [numero limitato di target](#bid-multiplier-limits-by-target).

Questa funzione funziona con i target di posizionamento esistenti. Per modificare le destinazioni selezionate per i posizionamenti, vedi &quot;[Modifica posizionamenti](/help/dsp/campaign-management/placements/placement-edit.md).&quot;

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

## Tipi di target idonei per i moltiplicatori di offerte {#bid-multiplier-by-target}

Puoi configurare i modificatori di offerte solo per le destinazioni incluse e non per quelle escluse.

* **Destinazioni geografiche**: area geografica (paesi, stati e città), codici postali e DMA

* **Obiettivi di inventario**: fonti e feed per l’inventario pubblico e [!UICONTROL On Demand] inventario

* **Destinazioni sito:** siti/app target (ma non esclusi), categorie di siti

* **Destinazioni pubblico:** segmenti, parti diurne e argomenti

* **destinazioni ads.txt:** (Quando si rinuncia ad ads.txt, che consente di acquistare inventario da tutti i venditori) ads.txt venditori solo, ads.txt venditori diretti e ads.txt venditori più siti senza annunci.txt <!-- bid multipliers for the different subsets of inventory; not available when the placement targets only one subset -->

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
>* [Visualizzare il log delle modifiche per un posizionamento](placement-change-log.md)
>* [Impostazioni di posizionamento](placement-settings.md)
