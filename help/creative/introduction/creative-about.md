---
title: Informazioni sull’Adobe Advertising Creative
description: Informazioni su  [!DNL Creative].
feature: Creative Introduction
source-git-commit: fd925c641bef7953aea50813725252c3913757fa
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---

# Informazioni sull’Adobe Advertising Creative 2.0

*Versione beta chiusa*

<!-- verify all and rewrite to include new stuff -->

Come parte di Adobe Advertising, Advertising Creative è una piattaforma self-service per automatizzare esperienze pubblicitarie personalizzate in tempo reale e, facoltativamente, ottimizzare gli annunci a livello di elemento creativo.

## Librerie creative personalizzate di creativi riutilizzabili

Le tue Creative Libraries ti consentono di gestire tutte le creatività che utilizzerai nelle esperienze pubblicitarie. Puoi creare più librerie, ciascuna con singoli creativi e gruppi creativi (denominati *bundle*). Aggiungerai bundle creativi alle esperienze annuncio.

## Esperienze basate su regole

Con [!DNL Creative], è possibile creare storie utilizzando un modello di struttura decisionale basato su regole, distribuendo una serie coreografica di annunci personalizzati in tempo reale in base a ciò che sai sul tuo pubblico e che seguono i tuoi clienti anche quando passano a siti Web diversi<!-- verify if that's true without Adobe CDP -->. Ad esempio, le storie possono cambiare in base al comportamento del cliente, all&#39;area geografica, alla demografia, al retargeting, alla posizione nel percorso di clienti e altro ancora.

### Implementazione di esperienze come annunci

Dopo aver creato un&#39;esperienza, puoi generarne un tag JavaScript o iframe e implementarlo come annuncio di terze parti in Advertising DSP o in qualsiasi altro DSP.<!-- Add any more info about integration with DSP? -->

<!-- Maybe add a subsection "Audience targeting options" with info about types of creative-level REtargeting and placement-level targeting within your DSP.  Need to clarify if any placement-level targeting might contradict/override creative-level targeting, or if they're completely different.

Advertiser should be able to target all segments which are available in DSP for targeting
-->

### Ottimizzazione degli elementi dell’annuncio

Facoltativamente, puoi consentire a [!DNL Creative] di ottimizzare gli elementi dell&#39;annuncio per qualsiasi esperienza in base alle prestazioni, indipendentemente dal fatto che tu definisca o meno target di pubblico specifici, utilizzando una rotazione dell&#39;annuncio ottimizzata e ponderata, basata su Adobe Sensei.

## Pixel di retargeting

Puoi creare pixel di retargeting da utilizzare come target per i creativi all’interno di un’esperienza pubblicitaria, in modo da mostrare gli annunci solo agli utenti con attributi specifici che hanno visitato in precedenza pagine web specifiche.

## Tracciamento di impression, clic e conversione

[!DNL Creative] tiene traccia automaticamente di tutte le impression e i clic per gli annunci serviti da un&#39;esperienza. Facoltativamente, puoi anche aggiungere URL di tracciamento delle impression e dei clic di terze parti ai creativi in Creative Libraries, nonché URL di tracciamento personalizzati in un’esperienza.

[!DNL Creative] tiene traccia anche delle conversioni dagli annunci serviti creati dalle tue esperienze pubblicitarie.<!-- Verify wording; anything important to add here? We do track them for all users, right? Or is it optoinal?  -->

<!--
 [Don't need to mention] When an ad is served, the DSP that buys the ad first tracks the impression, and then passes the impression information to [!DNL Creative]. [!DNL Creative] first tracks a click on an ad, and it then passes the click information
to the DSP.
-->

## Generazione di rapporti sulle prestazioni

Puoi visualizzare rapporti sulle prestazioni dettagliati a livello di esperienza in Creativi > Esperienze.

Puoi anche creare rapporti creativi personalizzati in Rapporti > Rapporti personalizzati per monitorare le prestazioni a livello di esperienza nelle esperienze. Se utilizzi le tue esperienze [!DNL Creative] come annunci nelle campagne DSP, i dati sulle prestazioni per tali annunci sono disponibili in report personalizzati aggiuntivi, proprio come i dati per gli altri annunci DSP. <!-- Verify that [!DNL Creative] users have access to ALL other reports, and if I can completely duplicate the report help for both help sets. -->

Facoltativamente, puoi recapitare i rapporti personalizzati alle [destinazioni dei rapporti](/help/dsp/reports/report-destinations/report-destination-about.md) specificate.

<!--
>* [Overview of implementing Adobe Advertising Creative](/help/creative/introduction/implementation-overview.md)
>* [How the user interface is organized](/help/creative/introduction/ui.md)
-->

>[!MORELIKETHIS]
>
>* [Informazioni sulle librerie creative](/help/creative/creative-libraries/creative-libraries-about.md)
>* [Informazioni sulle esperienze in Advertising Creative](/help/creative/experiences/experience-about.md)
