---
title: Posizionamenti duplicati
description: Scopri come duplicare uno o più posizionamenti.
feature: DSP Placements
exl-id: d22a61a8-4f1b-41ee-b4fb-3124bec81a2f
source-git-commit: 1c13874967ec4ad264e5fa6a5e0dfeb6120f53cc
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# Posizionamenti duplicati

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

Duplica uno o più posizionamenti per creare posizionamenti con impostazioni simili. Puoi:

* Creare più duplicati di posizionamenti
* Posizionamenti duplicati all’interno degli inserzionisti e delle campagne originali o all’interno di diversi
* (Per posizionamenti duplicati all’interno delle campagne originali) È possibile duplicare gli annunci originali
* Modificare lo stato e le date di volo dei nuovi posizionamenti

Vedere &quot;[Non duplicato](#placement-not-duplicated)&quot; per un elenco di impostazioni di posizionamento non duplicate.

1. Nel menu principale, fai clic su **[!UICONTROL Campaigns]**.

1. Fai clic sul nome della campagna.

1. Nel sottomenu, fai clic su **[!UICONTROL Placements]**.

1. Effettua una delle seguenti operazioni:

   * Per duplicare un posizionamento, fai clic su  **[!UICONTROL ...]>[!UICONTROL Duplicate]** accanto al nome del pacchetto.

   * Per duplicare più posizionamenti:

      1. Seleziona la casella di controllo accanto a ogni posizionamento da duplicare.

      1. Nella barra degli strumenti Azioni in blocco, fai clic su **[!UICONTROL Duplicate]**.

1. Specifica le nuove impostazioni di posizionamento:

   1. (Posizionamenti singoli) Inserisci il nuovo nome del posizionamento.

   1. In **[!UICONTROL Choose Package (Required)]** seleziona il pacchetto principale o **[!UICONTROL No package]*

   1. (Facoltativo) Modificare le impostazioni predefinite.

   Le impostazioni vengono applicate a tutti i posizionamenti selezionati.

   Per impostazione predefinita, i nuovi posizionamenti sono per il tipo di annuncio originale, sono assegnati agli inserzionisti e alle campagne originali, dispongono di pianificazioni di volo che iniziano il giorno corrente, sono in pausa e non includono gli annunci originali.

   Quando crei più posizionamenti, ai nuovi nomi di posizionamento viene aggiunto un numero, in sequenza, utilizzando la convenzione &lt;*nome_posizionamento_originale #N*>, ad esempio &quot;My Placement #2&quot;.

1. Clic **[!UICONTROL Submit]**.

## Non duplicato {#placement-not-duplicated}

Tutte le impostazioni dei posizionamenti originali vengono duplicate tranne:

* Impostazioni dell’esperimento
* (Se si modificano le date del volo) Programmazione annunci personalizzata
* (Se non alleghi annunci) Ponderazione e pianificazione degli annunci personalizzati
* Posizionamenti predefiniti per offerte e posizionamenti programmatici garantiti (PG) per [!UICONTROL Simple Ad Serving] offerte
* (Se copi dei posizionamenti in una campagna diversa):
   * Destinazioni geografiche
   * Pixel evento
   * Annunci
   * Livello di posizionamento [!DNL DoubleVerify Authentic Brand Safety] segmenti (che ignorano i segmenti a livello di inserzionista)

>[!MORELIKETHIS]
>
>* [Informazioni sulla gestione del posizionamento](placement-about.md)
>* [Creare un posizionamento](placement-create.md)
>* [Modificare un posizionamento](placement-edit.md)
>* [Visualizza il registro delle modifiche per un posizionamento](placement-change-log.md)
>* [Impostazioni di posizionamento](placement-settings.md)

