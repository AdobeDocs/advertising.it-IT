---
title: Gestire i moltiplicatori delle offerte per i posizionamenti
description: Scopri come creare e modificare i moltiplicatori di offerta per i target di posizionamento specificati.
feature: DSP Placements
exl-id: fbd44960-c9df-4713-94b7-13bcdb7e2568
source-git-commit: ae1a58bd0aed430cd2914146dfb2850bc8125025
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 3%

---

# Gestire i moltiplicatori delle offerte per i posizionamenti

Utilizzando questa funzione puoi modificare i moltiplicatori di offerta per i target di posizionamento esistenti. Puoi gestire i moltiplicatori delle offerte per un posizionamento alla volta.<!-- remove that line once we can edit multiple -->

Per modificare le destinazioni selezionate per i posizionamenti, vedi &quot;[Modifica posizionamenti](/help/dsp/campaign-management/placements/placement-edit.md).&quot;

<!-- 
## Manage the Bid Multipliers for a Single Placement
-->

1. Nel menu principale, fai clic su **[!UICONTROL Campaigns]**.

1. Fai clic sul nome della campagna.

1. Nel sottomenu, fai clic su **[!UICONTROL Placements]**.

1. Accanto al nome del posizionamento, fate clic su  **[!UICONTROL ...]** > **[!UICONTROL Bid Multiplier]**.

1. Sposta in ogni [scheda specifica del target](#bid-multiplier-by-target) ([!UICONTROL Geo], [!UICONTROL Inventory], [!UICONTROL Sites], [!UICONTROL Audience], e [!UICONTROL Brand Safety]) e modificare i valori esistenti per le destinazioni di posizionamento. La maggior parte delle categorie target elenca le sottocategorie a sinistra. Fai clic su una sottocategoria per gestire i moltiplicatori di offerte per quella sottocategoria, se applicabile.

   Per impostazione predefinita, il moltiplicatore di offerta per un target è 1,00, il che significa che l’offerta non viene adeguata per tale target. I valori possono essere compresi tra 0,10 e 10,00. Ad esempio, un modificatore di offerta di 0,5 riduce l&#39;offerta di 6 a 3 dollari (0,5 x 6). I modificatori di offerta non aumentano mai l’offerta oltre l’offerta massima.

   Quando un&#39;asta è idonea per più modificatori di offerta, tutti i modificatori di offerta applicabili vengono moltiplicati.

   È possibile impostare i moltiplicatori delle offerte (con valori diversi da 1,00) per un [numero limitato di target](#bid-multiplier-limits-by-target).

1. In alto a destra, fai clic su **[!UICONTROL Save]**.

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
