---
title: Duplicare una campagna
description: Scopri come duplicare una campagna.
feature: DSP Campaigns
exl-id: 4e42bd5b-e8a9-45be-af5c-367c48d0b131
source-git-commit: 4085c1b21c0fe84653978e449321868921841367
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# Duplicare una campagna

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

Duplica una campagna per creare una nuova campagna con impostazioni simili. È possibile:

* Duplica la campagna per l&#39;inserzionista originale o per un altro
* Facoltativamente, duplicare i pacchetti e i posizionamenti originali
* Modificare le date di volo della nuova campagna

Consulta &quot;[Non duplicato](#campaign-not-duplicated)&quot; per un elenco di impostazioni di posizionamento che non sono duplicate.

1. Nel menu principale, fai clic su **[!UICONTROL Campaigns]**.

1. Accanto al nome della campagna, fai clic su **[!UICONTROL ...]** > **[!UICONTROL Duplicate]**.

1. Specifica le nuove impostazioni della campagna:

   1. Immettere il nome della nuova campagna e la data di fine del volo.

   1. (Facoltativo) Modifica le impostazioni predefinite.

      Per impostazione predefinita, la nuova campagna viene assegnata all’inserzionista originale, ha una pianificazione dei voli che inizia il giorno corrente e include i pacchetti e i posizionamenti originali.

1. Clic **[!UICONTROL Submit]**.

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
   * Livello di posizionamento [!DNL DoubleVerify Authentic Brand Safety] segmenti (che sostituiscono i segmenti a livello di inserzionista)

>[!MORELIKETHIS]
>
>* [Informazioni su Campaign Management](campaign-about.md)
>* [Creare una campagna](campaign-create.md)
>* [Modificare una campagna](campaign-edit.md)
>* [Visualizzare il registro delle modifiche per una campagna](campaign-change-log.md)
>* [Impostazioni campagna](campaign-settings.md)

