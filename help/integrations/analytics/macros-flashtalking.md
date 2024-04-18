---
title: Aggiungi [!DNL Analytics for Advertising] Macro per [!DNL Flashtalking] Tag annuncio
description: Scopri perché e come aggiungere [!DNL Analytics for Advertising] macro per [!DNL Flashtalking] tag annuncio
feature: Integration with Adobe Analytics
exl-id: ce81824c-60bf-487c-8358-d18fcb3cc95f
source-git-commit: ca8260e643f24787f7918249906f3f38f3bbef6d
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%

---

# Aggiungi [!DNL Analytics for Advertising] Macro per [!DNL Flashtalking] Tag annuncio

*Per gli inserzionisti con una sola integrazione Adobi Advertising-Adobe Analytics*

*Applicabile solo a Advertising DSP*

Se utilizzi tag di annunci da [!DNL Flashtalking] per gli annunci Advertising DSP, aggiungi i parametri Analytics for Advertising agli URL della pagina di destinazione. I parametri registrano l’AMO ID (`s_kwcid`) e `ef_id` parametri della stringa di query nell’URL della pagina di destinazione, che consentono all’Adobe Advertising di inviare i dati di clic per gli annunci ad Adobe Analytics.

Usa macro per [!DNL Flashtalking] annunci display e video per i seguenti tipi di [!DNL Analytics for Advertising] implementazioni:

* **Per gli inserzionisti con [!DNL Adobe] [!DNL Analytics for Advertising] Codice JavaScript implementato sui loro siti web**: il codice JavaScript registra già l’AMO ID (`s_kwcid`) e `ef_id` parametri della stringa di query. Tuttavia, l’utilizzo delle macro estende il tracciamento per includere conversioni basate su clic quando i cookie di terze parti non sono supportati. La best practice prevede l’aggiunta di macro nelle sezioni seguenti ai tag annuncio per acquisire dati di click-through aggiuntivi che non vengono acquisiti tramite il codice JavaScript.

>[!NOTE]
>
>Il codice JavaScript è una soluzione per il tracciamento dei clic solo quando i cookie sono ancora disponibili. Una volta interrotti i cookie, sarà necessario implementare le macro seguenti.

* **Inserzionisti i cui siti Web non utilizzano [!DNL Analytics for Advertising] codice JavaScript e si basano invece su [!DNL Analytics] inoltro lato server solo per dati click-through** (senza alcun dato view-through): le seguenti macro sono necessarie per segnalare l’attività di clic sul sito basata sugli annunci acquistati tramite Adobi Advertising.

## Visualizzare i tag annuncio

All&#39;interno del [!DNL Flashtalking] Aggiungi impostazioni tag, aggiungi la seguente macro alla fine dell’URL di click-through in `Clicktag` campo:

```
[ftqs:[AdobeAMO]]
```

Si tratta della prima o unica stringa di query dopo l’URL di base, quindi la separa dall’URL di base con un `?`. Se l’URL di base include più stringhe di query, inizia la prima stringa con un `?` e ogni stringa successiva con un `&`.

Esempi:

`https://www.adobe.com/products/photoshop?[ftqs:[AdobeAMO]]`

`https://www.adobe.com/products/photoshop?cid=email&[ftqs:[AdobeAMO]]`

## Tag annuncio video

All&#39;interno del [!DNL Flashtalking] Aggiungi impostazioni tag, aggiungi la seguente macro alla fine dell’URL di click-through in `Clicktag` campo:

```
[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]
```

Si tratta della prima o unica stringa di query dopo l’URL di base, quindi la separa dall’URL di base con un `?`. Se l’URL di base include più stringhe di query, inizia la prima stringa con un `?` e ogni stringa successiva con un `&`.

Esempi:

`https://www.adobe.com/products/photoshop?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

`https://www.adobe.com/products/photoshop?cid=email&[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

>[!MORELIKETHIS]
>
>* [Panoramica di [!DNL Analytics for Advertising]](overview.md)
>* [ID Adobe Advertising utilizzati da [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Aggiungi [!DNL Analytics for Advertising] Macro per [!DNL Google Campaign Manager 360] Tag annuncio](/help/integrations/analytics/macros-google-campaign-manager.md)
