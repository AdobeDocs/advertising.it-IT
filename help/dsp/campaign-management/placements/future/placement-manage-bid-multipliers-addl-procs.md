---
title: Gestire i moltiplicatori delle offerte per i posizionamenti
description: Scopri come creare e modificare i moltiplicatori di offerta per i target di posizionamento specificati.
feature: DSP Placements
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 0%

---

# Gestire i moltiplicatori delle offerte per i posizionamenti


<!--

See if any of these procedures are implemented; may need to be edited and/or re-worded based on functionality/UI

-->

Utilizzando questa funzione puoi modificare i moltiplicatori di offerta per i target di posizionamento esistenti.

Per modificare le destinazioni selezionate per i posizionamenti, vedi &quot;[Modifica posizionamenti](/help/dsp/campaign-management/placements/placement-edit.md).&quot;

## Gestire i moltiplicatori delle offerte per uno o più posizionamenti

Per tutti i posizionamenti selezionati, puoi modificare manualmente i valori o caricare un foglio di calcolo con i valori.

1. Nel menu principale, fai clic su **[!UICONTROL Campaigns]**.

1. Fai clic sul nome della campagna.

1. Nel sottomenu, fai clic su **[!UICONTROL Placements]**.

1. Seleziona la casella di controllo accanto a ciascun posizionamento di cui desideri gestire i moltiplicatori di offerta.

1. Nella barra degli strumenti Azioni in blocco, fai clic su **[!UICONTROL ...]** > **[!UICONTROL Bid Multiplier]**.

1. Regola manualmente i moltiplicatori delle offerte per il target idoneo o caricando un file CSV con i valori target:

   * Per regolare manualmente i valori del moltiplicatore di offerta, passa a ogni scheda specifica per l’oggetto ([!UICONTROL Geo], [!UICONTROL Inventory], [!UICONTROL Sites], [!UICONTROL Audience], e[!UICONTROL Brand Safety]) e modificare i valori esistenti per le destinazioni di posizionamento.

   Le stesse modifiche si applicano a tutti i posizionamenti selezionati.

   * Per caricare un file CSV con valori del moltiplicatore di offerta che sovrascrivono i valori esistenti:

     >[!NOTE]
     >
     >Se lasci vuoto un campo, vengono eliminati tutti i valori per quel tipo di destinazione.<!-- Verify and re-word if needed. I'm not sure if you'll be able to have multiple data rows (one per placement) or if there will be only one data row applicable for all. -->

      1. Clic **[!UICONTROL CSV Edit]** in alto a destra.

      1. A) fare clic su **[!UICONTROL Download Template]** e modificare i valori del moltiplicatore di offerta o b) modificare un modello scaricato in precedenza. Salvare il file modificato sul dispositivo o sulla rete.

      1. A) trascinare e rilasciare il file modificato nella casella o b) fare clic all&#39;interno della casella per selezionare il file dal dispositivo o dalla rete.

   1. Clic **[!UICONTROL Upload]**.

   Per impostazione predefinita, il moltiplicatore di offerta per un target è 1,00, il che significa che l’offerta non viene adeguata per tale target. I valori possono essere compresi tra 0,10 e 10,00. Ad esempio, un modificatore di offerta di 0,5 riduce l&#39;offerta di 6 a 3 dollari (0,5 x 6). È possibile impostare i moltiplicatori delle offerte (con valori diversi da 1,00) per un [numero limitato di target](#bid-multiplier-limits-by-target).

   Quando un&#39;asta è idonea per più modificatori di offerta, tutti i modificatori di offerta applicabili vengono moltiplicati.

   I modificatori di offerta non aumentano mai l’offerta oltre l’offerta massima.

1. Clic **[!UICONTROL Save]**.

-->

## Carica un foglio di calcolo per gestire i moltiplicatori di offerte per un singolo posizionamento<!-- Is this still going to exist independently, or will you just do this via the "Bid Multiplier" option in the main context menu for placements? If both options, then reword headings for distinction -->

Le modifiche nel file caricato sovrascrivono i valori del moltiplicatore di offerta esistente.<!-- what if you delete a row? -->

1. Nel menu principale, fai clic su **[!UICONTROL Campaigns]**.

1. Fai clic sul nome della campagna.

1. Nel sottomenu, fai clic su **[!UICONTROL Placements]**.

1. Accanto al nome del posizionamento, fate clic su  **[!UICONTROL ...]** > **[!UICONTROL Upload Bid Multiplier Excel Sheet]**.

1. 
   <!-- Verify the rest of these steps. -->

1. A) fare clic su **[!UICONTROL Download Template]** e modificare i valori del moltiplicatore di offerta o b) modificare un modello scaricato in precedenza. Salvare il file modificato sul dispositivo o sulla rete.

   Per impostazione predefinita, il moltiplicatore di offerta per un target è 1,00, il che significa che l’offerta non viene adeguata per tale target. I valori possono essere compresi tra 0,10 e 10,00. Ad esempio, un modificatore di offerta di 0,5 riduce l&#39;offerta di 6 a 3 dollari (0,5 x 6). È possibile impostare i moltiplicatori delle offerte (con valori diversi da 1,00) per un [numero limitato di target](#bid-multiplier-limits-by-target).

   Quando un&#39;asta è idonea per più modificatori di offerta, tutti i modificatori di offerta applicabili vengono moltiplicati.

   I modificatori di offerta non aumentano mai l’offerta oltre l’offerta massima.

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
