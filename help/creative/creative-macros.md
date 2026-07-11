---
title: Macro disponibili per il tracciamento degli URL
description: Fai riferimento alle macro che puoi aggiungere agli URL della tua pagina di destinazione, agli URL di tracciamento e alle creatività di terze parti.
feature: Creative Experiences, Creative Experiences
exl-id: d0cbbb21-467d-4ed1-bc6e-ded1b045b98b
TQID: https://experienceleague.adobe.com/J5jfIECrL29NngVOulEgHKZBHYqBmoz4680HzEzhIng
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: e1ce403e53ed6da4b16f5d7e4bfbbc50e1317ea8
workflow-type: tm+mt
source-wordcount: 312
ht-degree: 0%

---

# Macro disponibili per il tracciamento degli URL

<!-- More feature metadata???  -->

Puoi includere una qualsiasi delle seguenti macro nelle creatività di terze parti, negli URL di tracciamento di terze parti per le esperienze e negli URL delle pagine di destinazione per il tuo utilizzo.

Alcune delle macro disponibili o equivalenti vengono incluse automaticamente nei tag esperienza.

<!--
 Later: 

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
| `${TC_1}` | Custom tracking code 1. | &mdash; | &mdash; |
| `${TC_2}` | Custom tracking code 2. | &mdash; | &mdash; |
| `${TC_3}` | Custom tracking code 3. | &mdash; | &mdash; |
| `${TC_4}` | Custom tracking code 4. | &mdash; | &mdash; |
| `${TC_5}` | Custom tracking code 5. | &mdash; | &mdash; |
| `${GDPR_ENFORCED}` | Whether GDPR enforcement is required for the bid request. Values: **1** = GDPR should be enforced, **0** = GDPR should not be enforced. | &mdash; | &mdash; |
| `${GDPR_CONSENT}` | The GDPR consent value received from the supply partner in the bid request. Typically: **1** = consent provided, **0** = no consent provided. | &mdash; | &mdash; |
-->

| Macro | Descrizione | Automaticamente nei tag esperienza per Advertising DSP? |
| --- | --- | --- |
| `${TM_CAMPAIGN_ID_NUM}` | Tiene traccia e segnala l’ID campagna da DSP | Sì |
| `${TM_SITE_ID_NUM}` | Tiene traccia e segnala l’ID sito da DSP | Sì |
| `${TM_PLACEMENT_ID_NUM}` | Tiene traccia e segnala l’ID di posizionamento dal DSP | Sì |
| `${TM_AD_ID_NUM}` | Tiene traccia e segnala l’ID annuncio da DSP | Sì |
| `${TM_CREATIVE_ID_NUM}` | Tiene traccia e segnala l’ID creativo da DSP | N/D |
| `${TM_SESSION_ID}` | Tiene traccia e segnala l’ID sessione associato alla richiesta dell’annuncio. Se non viene restituito un valore, Advertising Creative ne genera uno. | Sì |
| `${TM_ACC_EXPERIENCE_ID}` | Tiene traccia e segnala l’ID esperienza Advertising Creative | — |
| `${TM_ACC_CREATIVE_ID}` | Tiene traccia e segnala l’ID creativo di Advertising Creative | — |
| `${TM_RANDOM}` | Numero casuale compreso tra 1 e 1.000.000. Comunemente utilizzato per svuotare la cache. | — |
| `${TM_TIMESTAMP}` | Timestamp UNIX® (in secondi) | — |
| `${TM_CLICK_URL_URLENC}` | (Per annunci di terze parti di fornitori che richiedono la codifica URL) L’URL di reindirizzamento dei clic codificato, che consente ai server di annunci di tenere traccia e contare i clic degli annunci. Quando un utente fa clic sull’annuncio, la macro viene attivata e il clic viene registrato e conteggiato a scopo di reporting. | Sì |
| `${TC_1}` | Codice di tracciamento personalizzato 1. | — |
| `${TC_2}` | Codice di tracciamento personalizzato 2. | — |
| `${TC_3}` | Codice di tracciamento personalizzato 3. | — |
| `${TC_4}` | Codice di tracciamento personalizzato 4. | — |
| `${TC_5}` | Codice di tracciamento personalizzato 5. | — |
| `${GDPR_ENFORCED}` | Se è necessaria l’applicazione del RGPD per la richiesta di offerta. Valori: **1** = il RGPD deve essere applicato, **0** = il RGPD non deve essere applicato. | — |
| `${GDPR_CONSENT}` | Il valore del consenso RGPD ricevuto dal partner di fornitura nella richiesta di offerta. In genere: **1** = consenso fornito, **0** = nessun consenso fornito. | — |

>[!MORELIKETHIS]
>
>* [Aggiungere creatività standard a una libreria creativa](/help/creative/creative-libraries/creative-add-standard.md#creative-add-third-party)
>* [Impostazioni creative standard](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-third-party)
>* [Impostazioni esperienza di destinazione](/help/creative/experiences/experience-settings-targeting.md)
>* [Impostazioni esperienza non mirate](/help/creative/experiences/experience-settings-no-targeting.md)
