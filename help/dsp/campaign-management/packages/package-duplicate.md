---
title: Duplicare un pacchetto
description: Scopri come duplicare un pacchetto.
feature: DSP Packages
exl-id: 75842776-a024-43c9-aaf8-1126c0b9d717
TQID: https://experienceleague.adobe.com/fbOXyvipyiJ7rOlCroMLHvSqCqXPIEL9FTHmqm7CQu8
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: fddd8d8f-3ba1-4a22-b714-69d0e4655be8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: fdc899fcc763a963e5878b2fcf313174b8f5a74b
workflow-type: tm+mt
source-wordcount: 420
ht-degree: 0%

---

# Duplicare un pacchetto

Duplica un pacchetto per creare un pacchetto con impostazioni simili. È possibile:

* Duplica il pacchetto all’interno dell’inserzionista e della campagna originali o in diversi

* Se necessario, duplica i posizionamenti all’interno del pacchetto

* (Per i pacchetti duplicati nelle campagne originali) Duplica facoltativamente gli annunci originali e i pixel dell’evento a livello di posizionamento

* Modifica le date di volo del nuovo pacchetto

Per un elenco delle impostazioni di posizionamento non duplicate, vedere &quot;[Elementi non duplicati](#package-not-duplicated)&quot;.

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

## Cosa non è duplicato {#package-not-duplicated}

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

## Best practice per configurare il nuovo pacchetto

>[!TIP]
>
>* Utilizza i bulksheet per [apportare modifiche a più componenti della campagna contemporaneamente](/help/dsp/campaign-management/campaign-components-review-edit.md).
>* Utilizza i fogli di tag degli annunci per [caricare più annunci di terze parti](/help/dsp/campaign-management/ads/ad-create-multiple.md).

* Metti in pausa il nuovo pacchetto fino a quando non sei pronto ad attivarlo.

* Considera quanto segue e modifica il nuovo pacchetto in base alle esigenze:

   * L&#39;account dispone di fondi sufficienti per accogliere il nuovo budget del pacchetto?

   * Il nuovo pacchetto necessita di un bilancio diverso rispetto al pacchetto precedente?

   * Sono necessari budget minimi per uno qualsiasi dei posizionamenti?

   * Carica le creatività, inclusa la ponderazione e la pianificazione personalizzate necessarie, e allegale ai posizionamenti.

   * Allega i pixel dell’evento necessari ai posizionamenti e agli annunci.

   * Includi destinazioni geografiche e segmenti [!DNL DoubleVerify Authentic Brand Suitability] a livello di posizionamento in base alle esigenze per i posizionamenti.

   * Per le offerte garantite programmatiche, utilizza i nuovi ID offerta e crea posizionamenti predefiniti.

   * Crea nuovi posizionamenti per offerte [!UICONTROL Simple Ad Serving] in base alle esigenze.

* Per i pacchetti che utilizzano obiettivi di ottimizzazione personalizzati, utilizzare l&#39;impostazione [[!UICONTROL Linked Package for Optimization Learnings Carryover]](/help/dsp/campaign-management/packages/package-settings.md) per ogni pacchetto per utilizzare i dati storici della campagna precedente come input per l&#39;ottimizzazione del pacchetto.

>[!MORELIKETHIS]
>
>* [Informazioni sulla gestione dei pacchetti in Advertising DSP](package-about.md)
>* [Crea un pacchetto](package-create.md)
>* [Modifica pacchetto](package-edit.md)
>* [Visualizza il registro delle modifiche per un pacchetto](package-change-log.md)
>* [Impostazioni pacchetto](package-settings.md)
