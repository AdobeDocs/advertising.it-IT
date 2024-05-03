---
title: Posizionamenti duplicati
description: Scopri come duplicare uno o più posizionamenti.
feature: DSP Placements
exl-id: 41021f5b-13d1-419f-af03-c5507f9fed4d
source-git-commit: ae1a58bd0aed430cd2914146dfb2850bc8125025
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 0%

---

# Posizionamenti duplicati

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

Duplica uno o più posizionamenti per creare posizionamenti con impostazioni simili. È possibile:

* Creare più duplicati di posizionamenti
* Posizionamenti duplicati negli inserzionisti e nelle campagne originali o in diversi
* (Per i posizionamenti duplicati all’interno delle campagne originali) Duplica facoltativamente gli annunci originali
* Modificare lo stato e le date del volo dei nuovi posizionamenti

Consulta &quot;[Non duplicato](#placement-not-duplicated)&quot; per un elenco di impostazioni di posizionamento che non sono duplicate.

1. Nel menu principale, fai clic su **[!UICONTROL Campaigns]**.

1. Fai clic sul nome della campagna.

1. Nel sottomenu, fai clic su **[!UICONTROL Placements]**.

1. Effettuare una delle seguenti operazioni:

   * Per duplicare un posizionamento, fate clic su  **[!UICONTROL ...]** > **[!UICONTROL Duplicate]** accanto al nome del pacchetto.

   * Per duplicare più posizionamenti:

      1. Selezionate la casella di controllo accanto a ciascun posizionamento da duplicare.

      1. Nella barra degli strumenti Azioni in blocco, fai clic su **[!UICONTROL Duplicate]**.

1. Specificare le nuove impostazioni di posizionamento:

   1. (Posizionamenti singoli) Inserisci il nuovo nome del posizionamento.

   1. In **[!UICONTROL Choose Package (Required)]** selezionare il pacchetto principale o il **[!UICONTROL No package]*.

   1. (Facoltativo) Modifica le impostazioni predefinite.

   Le impostazioni vengono applicate a tutti i posizionamenti selezionati.

   Per impostazione predefinita, i nuovi posizionamenti sono per il tipo di annuncio originale, sono assegnati agli inserzionisti e alle campagne originali, hanno programmi di volo che iniziano il giorno corrente, sono sospesi e non includono gli annunci originali.

   Quando si creano più posizionamenti, ai nuovi nomi di posizionamento viene aggiunto un numero, in sequenza, utilizzando la convenzione &lt;*#N original_placement_name*>, ad esempio &quot;My Placement #2.&quot; (Il mio posizionamento)

1. Clic **[!UICONTROL Submit]**.

## Non duplicato {#placement-not-duplicated}

Tutte le impostazioni dei posizionamenti originali vengono duplicate, tranne:

* Impostazioni esperimento
* (Se modifichi le date del volo) Personalizzazione della pianificazione degli annunci
* (Se non alleghi annunci) Ponderazione e pianificazione degli annunci personalizzati
* Posizionamenti predefiniti per offerte programmatiche garantite (PG) e posizionamenti per [!UICONTROL Simple Ad Serving] offerte
* (Se copi i posizionamenti in un’altra campagna):
   * Destinazioni geografiche
   * Pixel evento
   * Annunci
   * Livello di posizionamento [!DNL DoubleVerify Authentic Brand Safety] segmenti (che sostituiscono i segmenti a livello di inserzionista)

>[!MORELIKETHIS]
>
>* [Informazioni sulla gestione del posizionamento](placement-about.md)
>* [Creare un posizionamento](placement-create.md)
>* [Modifica posizionamenti](placement-edit.md)
>* [Visualizzare il log delle modifiche per un posizionamento](placement-change-log.md)
>* [Impostazioni di posizionamento](placement-settings.md)
