---
title: Duplicare un pacchetto
description: Scopri come duplicare un pacchetto.
feature: DSP Packages
exl-id: 75842776-a024-43c9-aaf8-1126c0b9d717
source-git-commit: 1a98b3ba7c37a768825e9e48db7d847f12daa9a0
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---

# Duplicare un pacchetto

Duplica un pacchetto per creare un pacchetto con impostazioni simili. Puoi:

* Duplica il pacchetto all’interno dell’inserzionista e della campagna originali o all’interno di diversi
* Facoltativamente, duplica i posizionamenti all’interno del pacchetto
* (Per i pacchetti duplicati all’interno delle campagne originali) Facoltativamente duplica gli annunci originali e i pixel dell’evento a livello di posizionamento
* Modificare le date di volo del nuovo pacchetto

Vedere &quot;[Non duplicato](#package-not-duplicated)&quot; per un elenco di impostazioni di posizionamento non duplicate.

1. Nel menu principale, fai clic su **[!UICONTROL Campaigns]**.

1. Fai clic sul nome della campagna per aprire la [!UICONTROL Packages] visualizza.

1. Accanto al nome del pacchetto, fai clic su  **[!UICONTROL ...]** > **[!UICONTROL Duplicate]**.

1. Specifica le nuove impostazioni del pacchetto:

   1. Immetti il nuovo nome del pacchetto.

   1. (Facoltativo) Modificare le impostazioni predefinite.

      Per impostazione predefinita:

      * Il nuovo pacchetto viene assegnato all’inserzionista e alla campagna originali.

      * Il nuovo pacchetto diventa attivo il giorno corrente.<!-- and the flight continues for NN  days. -->

      * I posizionamenti all&#39;interno del pacchetto originale vengono copiati nel nuovo pacchetto.

      * Gli annunci e i pixel dell’evento a livello di posizionamento non vengono copiati nel nuovo pacchetto.

1. Clic **[!UICONTROL Submit]**.

## Non duplicato {#package-not-duplicated}

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
>* [Informazioni sulla gestione dei pacchetti](package-about.md)
>* [Creare un pacchetto](package-create.md)
>* [Modificare un pacchetto](package-edit.md)
>* [Visualizza il registro delle modifiche per un pacchetto](package-change-log.md)
>* [Impostazioni pacchetto](package-settings.md)

