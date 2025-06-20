---
title: Informazioni su Adobe Advertising Creative
description: Informazioni su  [!DNL Creative].
feature: Creative Introduction
source-git-commit: 72a6c3de183aa47cecc2ec4d0fab30ff91d4bb05
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 0%

---

# Informazioni su Adobe Advertising Creative 2.0

*Versione beta chiusa*

<!-- verify all and rewrite to include new stuff -->

Come parte di Adobe Advertising, Advertising Creative è una piattaforma self-service per automatizzare esperienze pubblicitarie personalizzate in tempo reale e, facoltativamente, ottimizzare gli annunci a livello di elemento creativo.<!-- Verify --> Puoi implementare le esperienze pubblicitarie come annunci in qualsiasi DSP, incluso Adobe Advertising DSP.

## Librerie creative personalizzate di creativi riutilizzabili

Le librerie Creative ti consentono di gestire i contenuti creativi da utilizzare nelle esperienze pubblicitarie. Puoi creare più librerie, ciascuna con singoli creativi e gruppi creativi (denominati *bundle*, che allegherai alle esperienze).

### [!DNL Adobe] integrazioni risorse

[!DNL Creative] è direttamente integrato con Adobe Experience Manager e consente di caricare facilmente le risorse immagine [!DNL Adobe] create e approvate dal team di progettazione e quindi utilizzarle per la creazione di storyboard e la modifica in tempo reale di esperienze pubblicitarie.

## Esperienze basate su regole e non mirate

* **Esperienze mirate e basate su regole:** crea storie utilizzando un modello di struttura decisionale basato su regole, distribuendo una stringa coreografica di annunci personalizzati in tempo reale in base a ciò che sai sul tuo pubblico. Ad esempio, le storie possono cambiare in base al comportamento del cliente, all&#39;area geografica, alla demografia, al retargeting, alla posizione nel percorso di clienti e altro ancora.

* **Esperienze non di destinazione:** pianifica e ottimizza gli elementi dell&#39;annuncio senza restringere il pubblico.

### [!DNL Adobe] integrazioni dati

Puoi utilizzare i segmenti di pubblico di prime parti da Adobe Audience Manager e Adobe Analytics, nonché i segmenti di pubblico personalizzati creati in Advertising DSP e i pixel di retargeting creati con [!DNL Creative], come target per creativi specifici in un&#39;esperienza pubblicitaria. <!-- Advertiser should be able to target all segments that are available in DSP for targeting -->

### Implementazione di esperienze come annunci

Dopo aver creato un&#39;esperienza, puoi generarne un tag JavaScript o iframe e implementarlo come annuncio di visualizzazione standard di terze parti in una campagna Advertising DSP o in qualsiasi altro DSP.<!-- Will add video and other ad formats; not sure if they'll be available for both standard and dynamic ads. -->

### Ottimizzazione degli elementi dell’annuncio

Facoltativamente, puoi consentire a [!DNL Creative] di ottimizzare gli elementi dell&#39;annuncio per qualsiasi esperienza in base alle prestazioni, indipendentemente dal fatto che tu definisca o meno target di pubblico specifici, utilizzando una rotazione dell&#39;annuncio ottimizzata e ponderata, basata su Adobe Sensei.

<!--
[!DNL Creative] serves first-party ads and triggers third-party ads for the experience based on the specified targeting (when applicable), scheduling, ad rotation, and optimization goal options 
-->

## Pixel di retargeting

Puoi creare pixel di retargeting da utilizzare come target per i creativi all’interno di un’esperienza pubblicitaria. Le destinazioni mostrano annunci solo per gli utenti con attributi specificati che hanno visitato in precedenza pagine web specifiche.

## Tracciamento di impression, clic e conversione

[!DNL Creative] tiene traccia automaticamente di tutte le impression e i clic per gli annunci serviti da un&#39;esperienza. Facoltativamente, puoi anche aggiungere URL di tracciamento delle impression e dei clic di terze parti ai creativi nelle librerie Creative, nonché URL di tracciamento personalizzati in un’esperienza.

[!DNL Creative] tiene traccia anche delle conversioni dagli annunci serviti creati dalle tue esperienze pubblicitarie.<!-- Verify wording; anything important to add here? We do track them for all users, right? Or is it optional?  -->

<!--
 [Don't need to mention] When an ad is served, the DSP that buys the ad first tracks the impression, and then passes the impression information to [!DNL Creative]. [!DNL Creative] first tracks a click on an ad, and it then passes the click information
to the DSP.
-->

## Generazione di rapporti sulle prestazioni

Puoi visualizzare rapporti sulle prestazioni dettagliati a livello di esperienza in Creativi > Esperienze.

Puoi anche creare rapporti Creative personalizzati in Rapporti > Rapporti personalizzati per monitorare le prestazioni a livello di esperienza nelle esperienze. Se utilizzi le tue esperienze [!DNL Creative] come annunci nelle campagne DSP, i dati sulle prestazioni per tali annunci sono disponibili in report personalizzati aggiuntivi, proprio come i dati per gli altri annunci DSP. <!-- Verify that [!DNL Creative] users have access to ALL other reports. -->

Facoltativamente, puoi recapitare i rapporti personalizzati alle [destinazioni dei rapporti](/help/dsp/reports/report-destinations/report-destination-about.md) specificate.

<!--
>* [Overview of implementing Adobe Advertising Creative](/help/creative/introduction/implementation-overview.md)
>* [How the user interface is organized](/help/creative/introduction/ui.md)
-->

>[!MORELIKETHIS]
>
>* [Informazioni sulle librerie creative](/help/creative/creative-libraries/creative-libraries-about.md)
>* [Informazioni sulle esperienze in Advertising Creative](/help/creative/experiences/experience-about.md)
