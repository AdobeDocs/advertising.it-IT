---
title: Posizionamenti duplicati
description: Scopri come duplicare uno o più posizionamenti.
feature: DSP Placements
exl-id: 41021f5b-13d1-419f-af03-c5507f9fed4d
TQID: https://experienceleague.adobe.com/1QHdooPh2tr6pfbnRsPbe-P5o-lZLgX-NQIUNG2ulHM
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: a4886037-b6d8-40e1-aeab-edeb7649d7d3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: fdc899fcc763a963e5878b2fcf313174b8f5a74b
workflow-type: tm+mt
source-wordcount: 445
ht-degree: 0%

---

# Posizionamenti duplicati

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

Duplica uno o più posizionamenti per creare posizionamenti con impostazioni simili. È possibile:

* Creare più duplicati di posizionamenti
* Posizionamenti duplicati negli inserzionisti e nelle campagne originali o in diversi
* (Per i posizionamenti duplicati all’interno delle campagne originali) Duplica facoltativamente gli annunci originali
* Modificare lo stato e le date del volo dei nuovi posizionamenti

Per un elenco delle impostazioni di posizionamento non duplicate, vedere &quot;[Elementi non duplicati](#placement-not-duplicated)&quot;.

1. Nel menu principale, fare clic su **[!UICONTROL Campaigns]**.

1. Fai clic sul nome della campagna.

1. Nel sottomenu fare clic su **[!UICONTROL Placements]**.

1. Effettuare una delle seguenti operazioni:

   * Per duplicare un posizionamento, fare clic su **[!UICONTROL ...]** > **[!UICONTROL Duplicate]** accanto al nome del pacchetto.

   * Per duplicare più posizionamenti:

      1. Selezionate la casella di controllo accanto a ciascun posizionamento da duplicare.

      1. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL Duplicate]**.

1. Specificare le nuove impostazioni di posizionamento:

   1. (Posizionamenti singoli) Inserisci il nuovo nome del posizionamento.

   1. Nel menu **[!UICONTROL Choose Package (Required)]**, selezionare il pacchetto padre o **[!UICONTROL No package]*.

   1. (Facoltativo) Modifica le impostazioni predefinite.

   Le impostazioni vengono applicate a tutti i posizionamenti selezionati.

   Per impostazione predefinita, i nuovi posizionamenti sono per il tipo di annuncio originale, sono assegnati agli inserzionisti e alle campagne originali, hanno programmi di volo che iniziano il giorno corrente, sono sospesi e non includono gli annunci originali.

   Quando crei più posizionamenti, ai nuovi nomi di posizionamento viene aggiunto un numero, in sequenza, utilizzando la convenzione &lt;*original_placement_name #N*>, ad esempio &quot;My Placement #2.&quot;

1. Fare clic su **[!UICONTROL Submit]**.

## Cosa non è duplicato {#placement-not-duplicated}

Tutte le impostazioni dei posizionamenti originali vengono duplicate, tranne:

* Impostazioni esperimento
* Budget minimi a livello di posizionamento
* (Se modifichi le date del volo) Personalizzazione della pianificazione degli annunci
* (Se non alleghi annunci) Ponderazione e pianificazione degli annunci personalizzati
* Posizionamenti predefiniti per offerte programmatiche garantite (PG) e posizionamenti per [!UICONTROL Simple Ad Serving] offerte
* (Se copi i posizionamenti in un’altra campagna):
   * Destinazioni geografiche
   * Pixel evento
   * Annunci
   * Segmenti [!DNL DoubleVerify Authentic Brand Suitability] a livello di posizionamento (che sostituiscono i segmenti a livello di inserzionista)

## Best practice per configurare i nuovi posizionamenti

>[!TIP]
>
>* Utilizza i bulksheet per [apportare modifiche a più componenti della campagna contemporaneamente](/help/dsp/campaign-management/campaign-components-review-edit.md).
>* Utilizza i fogli di tag degli annunci per [caricare più annunci di terze parti](/help/dsp/campaign-management/ads/ad-create-multiple.md).

* Metti in pausa i nuovi posizionamenti fino a quando non sei pronto ad attivarli.

* Considera quanto segue e modifica i nuovi posizionamenti in base alle esigenze:

   * L’account dispone di fondi sufficienti per accogliere i nuovi budget di collocamento?

   * I nuovi posizionamenti richiedono budget diversi rispetto ai posizionamenti precedenti? Sono necessari budget minimi?

   * Carica le creatività, inclusa la ponderazione e la pianificazione personalizzate necessarie, e allegale ai posizionamenti.

   * Allega i pixel dell’evento necessari ai posizionamenti e agli annunci.

   * Includi destinazioni geografiche e segmenti [!DNL DoubleVerify Authentic Brand Suitability] a livello di posizionamento in base alle esigenze per i posizionamenti.

   * Per le offerte garantite programmatiche, utilizza i nuovi ID offerta e crea posizionamenti predefiniti.

   * Crea nuovi posizionamenti per offerte [!UICONTROL Simple Ad Serving] in base alle esigenze.

>[!MORELIKETHIS]
>
>* [Informazioni sulla gestione dei posizionamenti in Advertising DSP](placement-about.md)
>* [Crea un posizionamento](placement-create.md)
>* [Modifica posizionamenti](placement-edit.md)
>* [Visualizza il log delle modifiche per un posizionamento](placement-change-log.md)
>* [Impostazioni posizionamento](placement-settings.md)
