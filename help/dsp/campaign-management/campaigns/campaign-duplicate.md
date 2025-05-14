---
title: Duplicare una campagna
description: Scopri come duplicare una campagna.
feature: DSP Campaigns
exl-id: 4e42bd5b-e8a9-45be-af5c-367c48d0b131
source-git-commit: 051658d822253e5d0cac56e3d59e99386c68fb71
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 0%

---

# Duplicare una campagna

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

Duplica una campagna per creare una nuova campagna con impostazioni simili. È possibile:

* Duplica la campagna per l&#39;inserzionista originale o per un altro

* Facoltativamente, duplicare i pacchetti e i posizionamenti originali

* Modificare le date di volo della nuova campagna

Consulta &quot;[Elementi non duplicati](#campaign-not-duplicated)&quot; per un elenco delle impostazioni di posizionamento che non sono duplicate.

1. Nel menu principale, fare clic su **[!UICONTROL Campaigns]**.

1. Accanto al nome della campagna, fare clic su **[!UICONTROL ...]** > **[!UICONTROL Duplicate]**.

1. Specifica le nuove impostazioni della campagna:

   1. Immettere il nome della nuova campagna e la data di fine del volo.

   1. (Facoltativo) Modifica le impostazioni predefinite.

      Per impostazione predefinita, la nuova campagna viene assegnata all’inserzionista originale, ha una pianificazione dei voli che inizia il giorno corrente e include i pacchetti e i posizionamenti originali.

1. Fare clic su **[!UICONTROL Submit]**.

## Non duplicato {#campaign-not-duplicated}

Tutte le impostazioni dei posizionamenti originali vengono duplicate, tranne:

* Impostazioni esperimento
* (Se modifichi le date del volo) Personalizzazione della pianificazione degli annunci
* (Se non alleghi annunci) Ponderazione e pianificazione degli annunci personalizzati
* Posizionamenti predefiniti per offerte programmatiche garantite (PG) e posizionamenti per [!UICONTROL Simple Ad Serving] offerte
* (Se copi i posizionamenti in un’altra campagna):
   * Destinazioni geografiche
   * Pixel evento
   * Annunci
   * Segmenti [!DNL DoubleVerify Authentic Brand Safety] a livello di posizionamento (che sostituiscono i segmenti a livello di inserzionista)

## Best practice per configurare la nuova campagna

>[!TIP]
>
>* Utilizza i bulksheet per [apportare modifiche a più componenti della campagna contemporaneamente](/help/dsp/campaign-management/campaign-components-review-edit.md).
>* Utilizza i fogli di tag degli annunci per [caricare più annunci di terze parti](/help/dsp/campaign-management/ads/ad-create-multiple.md).

* Sospendi la nuova campagna fino a quando non sei pronto ad attivarla.

* Considera quanto segue e modifica le nuove impostazioni della campagna in base alle esigenze:

   * L&#39;account dispone di fondi sufficienti per il nuovo budget della campagna?

   * La nuova campagna ha bisogno di un budget diverso rispetto alla campagna precedente?

   * Carica le creatività, inclusa la ponderazione e la pianificazione personalizzate necessarie, e allegale ai posizionamenti.

   * Allega i pixel dell’evento necessari ai posizionamenti e agli annunci.

   * Includi destinazioni geografiche e segmenti [!DNL DoubleVerify Authentic Brand Safety] a livello di posizionamento in base alle esigenze per i posizionamenti.

   * Per le offerte garantite programmatiche, utilizza i nuovi ID offerta e crea posizionamenti predefiniti.

   * Crea nuovi posizionamenti per offerte [!UICONTROL Simple Ad Serving] in base alle esigenze.

* Per le campagne di prestazioni (ovvero le campagne con pacchetti che utilizzano obiettivi di ottimizzazione personalizzati), utilizzare l&#39;impostazione [[!UICONTROL Linked Package for Optimization Learnings Carryover]](/help/dsp/campaign-management/packages/package-settings.md) per ogni pacchetto per utilizzare i dati storici della campagna precedente come input per l&#39;ottimizzazione del pacchetto.

>[!MORELIKETHIS]
>
>* [Informazioni sulla gestione delle campagne](campaign-about.md)
>* [Crea una campagna](campaign-create.md)
>* [Modifica una campagna](campaign-edit.md)
>* [Visualizza il log delle modifiche per una campagna](campaign-change-log.md)
>* [Impostazioni campagna](campaign-settings.md)
