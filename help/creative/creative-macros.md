---
title: Macro disponibili per il tracciamento degli URL
description: Fai riferimento alle macro che puoi aggiungere agli URL della tua pagina di destinazione, agli URL di tracciamento e alle creatività di terze parti.
feature: Creative Experiences, Creative Experiences
exl-id: d0cbbb21-467d-4ed1-bc6e-ded1b045b98b
source-git-commit: f7d5bf3193cb41ca2a0d4415998209e5a9b724ba
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---

# Macro disponibili per il tracciamento degli URL

<!-- More feature metadata???  -->

Puoi includere una qualsiasi delle seguenti macro nelle creatività di terze parti, negli URL di tracciamento di terze parti per le esperienze e negli URL delle pagine di destinazione per il tuo utilizzo.

Alcune delle macro disponibili o equivalenti vengono incluse automaticamente nei tag esperienza.

<!-- Later: 

| Macro | Description | Automatically in experience tags for Advertising DSP? | Automatically in experience tags for [!DNL Google Campaign Manager 360]? |
| --- | --- | --- | --- |
| `${TM_CAMPAIGN_ID_NUM}` | Tracks and reports the campaign ID from the DSP | Yes | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%ebuy!` |
| `${TM_SITE_ID_NUM}` | Tracks and reports the site ID from the DSP | Yes | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%esid!` |
| `${TM_PLACEMENT_ID_NUM}` | Tracks and reports the placement ID from the DSP | Yes | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%epid!` |
| `${TM_AD_ID_NUM}` | Tracks and reports the ad ID from the DSP | Yes | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%eaid!` |
| `${TM_CREATIVE_ID_NUM}` | Tracks and reports the creative ID from the DSP | N/A | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%ecid!` |
| `${TM_SESSION_ID}` | Tracks and reports the impression ID from the DSP. If a value isn't returned, Advertising Creative generates one. | Yes | &mdash; |
| `${TM_ACC_EXPERIENCE_ID}` | Tracks and reports the Advertising Creative experience ID | &mdash; | &mdash; |
| `${TM_ACC_CREATIVE_ID}` | Tracks and reports the Advertising Creative creative ID | &mdash; | &mdash; |
| `${TM_RANDOM}` | A random number between 1 and 1000000 | &mdash; | &mdash; |
| `${TM_TIMESTAMP}` | The Unix Timestamp (in seconds) | &mdash; | &mdash; |
| `${TM_CLICK_URL_URLENC}` | (For third-party ads from vendors who require URL encoding) The encoded click redirect URL, which enables ad servers to track and count ad clicks. When the ad is served and the user clicks on it, the macro is activated, and the click is recorded and counted for reporting purposes. | Yes | &mdash; |

-->

| Macro | Descrizione | Automaticamente nei tag esperienza per Advertising DSP? |
| --- | --- | --- |
| `${TM_CAMPAIGN_ID_NUM}` | Tiene traccia e segnala l’ID campagna da DSP | Sì |
| `${TM_SITE_ID_NUM}` | Tiene traccia e segnala l’ID sito da DSP | Sì |
| `${TM_PLACEMENT_ID_NUM}` | Tiene traccia e segnala l’ID di posizionamento dal DSP | Sì |
| `${TM_AD_ID_NUM}` | Tiene traccia e segnala l’ID annuncio da DSP | Sì |
| `${TM_CREATIVE_ID_NUM}` | Tiene traccia e segnala l’ID creativo da DSP | N/D |
| `${TM_SESSION_ID}` | Tiene traccia e segnala l’ID di impression da DSP. Se un valore non viene restituito, Advertising Creative ne genera uno. | Sì |
| `${TM_ACC_EXPERIENCE_ID}` | Tiene traccia e segnala l’ID esperienza Advertising Creative | — |
| `${TM_ACC_CREATIVE_ID}` | Tiene traccia e segnala l’ID creativo di Advertising Creative | — |
| `${TM_RANDOM}` | Un numero casuale compreso tra 1 e 1000000 | — |
| `${TM_TIMESTAMP}` | Timestamp UNIX® (in secondi) | — |
| `${TM_CLICK_URL_URLENC}` | (Per annunci di terze parti di fornitori che richiedono la codifica URL) L’URL di reindirizzamento dei clic codificato, che consente ai server di annunci di tenere traccia e contare i clic degli annunci. Quando l’utente fa clic sull’annuncio, la macro viene attivata e il clic viene registrato e conteggiato a scopo di reporting. | Sì |

>[!MORELIKETHIS]
>
>* [Aggiungere creatività standard a una libreria creativa](/help/creative/creative-libraries/creative-add-standard.md#creative-add-third-party)
>* [Impostazioni creative standard](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-third-party)
>* [Impostazioni esperienza di destinazione](/help/creative/experiences/experience-settings-targeting.md)
>  &#x200B;>*[Impostazioni esperienza non mirate](/help/creative/experiences/experience-settings-no-targeting.md)
