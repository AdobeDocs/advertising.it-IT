---
title: Aggiungi [!DNL Analytics for Advertising] Macro a [!DNL Flashtalking] Tag ad
description: Scopri perché e come aggiungere [!DNL Analytics for Advertising] macro [!DNL Flashtalking] tag ad
feature: Integration with Adobe Analytics
exl-id: 4b060668-723c-4cd2-b70e-409501ec67de
source-git-commit: 1c13874967ec4ad264e5fa6a5e0dfeb6120f53cc
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 0%

---

# Aggiungi [!DNL Analytics for Advertising] Macro a [!DNL Flashtalking] Tag ad

*Inserzionisti con una sola integrazione Advertising-Adobe Analytics di Adobe*

*Applicabile solo alla DSP pubblicitaria*

Se utilizzi tag di annunci da [!DNL Flashtalking] per i tuoi annunci pubblicitari DSP aggiungi i parametri di Analytics for Advertising agli URL della pagina di destinazione. Record dei parametri `s_kwcid` e `ef_id` parametri della stringa di query nell’URL della pagina di destinazione, consentendo ad Adobe Advertising di inviare dati di clic per gli annunci ad Adobe Analytics.

Usa macro per [!DNL Flashtalking] annunci video e display per i seguenti tipi di [!DNL Analytics for Advertising] implementazioni:

* **Gli inserzionisti con [!DNL Adobe] [!DNL Analytics for Advertising] Codice JavaScript implementato sui loro siti web**: Il codice JavaScript registra già il `s_kwcid` e `ef_id` parametri della stringa di query. Tuttavia, l’utilizzo delle macro estende il tracciamento per includere le conversioni basate su clic quando i cookie di terze parti non sono supportati. La procedura consigliata consiste nell’aggiungere le macro nelle sezioni seguenti ai tag degli annunci per acquisire dati di click-through aggiuntivi non acquisiti tramite il codice JavaScript.

>[!NOTE]
>
>Il codice JavaScript è una soluzione per il tracciamento dei clic solo mentre i cookie sono ancora disponibili. Quando i cookie vengono interrotti, sarà necessario implementare le seguenti macro.

* **Inserzionisti i cui siti web non utilizzano [!DNL Analytics for Advertising] Codice JavaScript e utilizza [!DNL Analytics] inoltro lato server solo per i dati click-through** (senza dati view-through): Le seguenti macro sono necessarie per segnalare l&#39;attività di clic sul sito gestita dagli annunci acquistati tramite Adobe Advertising.

## Visualizza tag annunci

All&#39;interno di [!DNL Flashtalking] aggiungi le seguenti macro alla fine dell&#39;URL di click-through nel `Clicktag` campo:

```html
?[ftqs:[AdobeAMO]]
```

Esempio:  `https://www.adobe.com/products/photoshop?[ftqs:[AdobeAMO]]`

## Video Ad Tag

All&#39;interno di [!DNL Flashtalking] aggiungi le seguenti macro alla fine dell&#39;URL di click-through nel `Clicktag` campo:

```html
?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]
```

Esempio:  `https://www.adobe.com/products/photoshop?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

>[!MORELIKETHIS]
>
>* [Panoramica [!DNL Analytics for Advertising]](overview.md)
>* [ID pubblicitari di Adobe utilizzati da [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Aggiungi [!DNL Analytics for Advertising] Macro a [!DNL Google Campaign Manager 360] Tag ad](/help/integrations/analytics/macros-google-campaign-manager.md)

