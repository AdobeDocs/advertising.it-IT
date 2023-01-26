---
title: Duplicare una campagna
description: Scopri come duplicare una campagna.
feature: DSP Campaigns
exl-id: 4e42bd5b-e8a9-45be-af5c-367c48d0b131
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 0%

---

# Duplicare una campagna

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

Duplica una campagna per creare una nuova campagna con impostazioni simili. Puoi:

* Duplica la campagna per l’inserzionista originale o per un altro
* Facoltativamente duplicare i pacchetti e i posizionamenti originali
* Modificare le date di volo della nuova campagna

Vedere &quot;[Non duplicato](#campaign-not-duplicated)&quot; per un elenco di impostazioni di posizionamento non duplicate.

1. Nel menu principale, fai clic su **[!UICONTROL Campaigns]**.

1. Accanto al nome della campagna, fai clic su **... >[!UICONTROL Duplicate]**.

1. Specifica le nuove impostazioni della campagna:

   1. Immetti il nome della nuova campagna e la data di fine del volo.

   1. (Facoltativo) Modificare le impostazioni predefinite.

      Per impostazione predefinita, la nuova campagna viene assegnata all’inserzionista originale, dispone di un programma di volo che inizia il giorno corrente e include i pacchetti e i posizionamenti originali.

1. Clic **[!UICONTROL Submit]**.

## Non duplicato {#campaign-not-duplicated}

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
>* [Informazioni su Campaign Management](campaign-about.md)
>* [Creare una campagna](campaign-create.md)
>* [Modificare una campagna](campaign-edit.md)
>* [Impostazioni di Campaign](campaign-settings.md)

