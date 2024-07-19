---
title: Duplicare un pacchetto
description: Scopri come duplicare un pacchetto.
feature: DSP Packages
exl-id: 75842776-a024-43c9-aaf8-1126c0b9d717
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---

# Duplicare un pacchetto

Duplica un pacchetto per creare un pacchetto con impostazioni simili. È possibile:

* Duplica il pacchetto all’interno dell’inserzionista e della campagna originali o in diversi
* Se necessario, duplica i posizionamenti all’interno del pacchetto
* (Per i pacchetti duplicati nelle campagne originali) Duplica facoltativamente gli annunci originali e i pixel dell’evento a livello di posizionamento
* Modifica le date di volo del nuovo pacchetto

Consulta &quot;[Elementi non duplicati](#package-not-duplicated)&quot; per un elenco delle impostazioni di posizionamento che non sono duplicate.

1. Nel menu principale, fare clic su **[!UICONTROL Campaigns]**.

1. Fare clic sul nome della campagna per aprire la visualizzazione [!UICONTROL Packages].

1. Accanto al nome del pacchetto, fare clic su **[!UICONTROL ...]** > **[!UICONTROL Duplicate]**.

1. Specificare le impostazioni del nuovo pacchetto:

   1. Immettere il nome del nuovo pacchetto.

   1. (Facoltativo) Modifica le impostazioni predefinite.

      Per impostazione predefinita:

      * Il nuovo pacchetto viene assegnato all’inserzionista e alla campagna originali.

      * Il nuovo pacchetto diventa attivo nel giorno corrente.<!-- and the flight continues for NN  days. -->

      * I posizionamenti all&#39;interno del pacchetto originale vengono copiati nel nuovo pacchetto.

      * Gli annunci e i pixel dell’evento a livello di posizionamento non vengono copiati nel nuovo pacchetto.

1. Fare clic su **[!UICONTROL Submit]**.

## Non duplicato {#package-not-duplicated}

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

>[!MORELIKETHIS]
>
>* [Informazioni sulla gestione dei pacchetti](package-about.md)
>* [Crea pacchetto](package-create.md)
>* [Modifica pacchetto](package-edit.md)
>* [Visualizza il log delle modifiche per un pacchetto](package-change-log.md)
>* [Impostazioni pacchetto](package-settings.md)
