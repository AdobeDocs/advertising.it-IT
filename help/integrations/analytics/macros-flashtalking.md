---
title: Aggiungi [!DNL Analytics for Advertising] macro ai [!DNL Flashtalking] tag annuncio
description: Scopri perché e come aggiungere [!DNL Analytics for Advertising] macro ai tuoi [!DNL Flashtalking] tag annuncio
feature: Integration with Adobe Analytics
exl-id: ce81824c-60bf-487c-8358-d18fcb3cc95f
source-git-commit: c4db5727def6125b65fb2146666b988ae3b0db27
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# Aggiungi macro [!DNL Analytics for Advertising] a [!DNL Flashtalking] tag annuncio

*Inserzionisti con una sola integrazione Adobe Advertising-Adobe Analytics*

*Organizzazioni senza una relazione diretta con [!DNL Flashtalking] solo*

*Applicabile solo ad Advertising DSP*

Se utilizzi i tag degli annunci di [!DNL Flashtalking] per gli annunci di Advertising DSP, devi aggiungere i parametri di tracciamento agli URL della pagina di destinazione. Per utilizzare la relazione di Advertising DSP con [!DNL Flashtalking], aggiungi i parametri di Analytics for Advertising agli URL della tua pagina di destinazione. I parametri registrano i parametri AMO ID (`s_kwcid`) e `ef_id` della stringa di query nell&#39;URL della pagina di destinazione, consentendo ad Adobe Advertising di inviare i dati dei clic per gli annunci ad Adobe Analytics.

>[!NOTE]
>
>Se la tua organizzazione ha una partnership diretta con [!DNL Flashtalking], questa procedura non è necessaria. Accedi invece al tuo account [!DNL Flashtalking] e segui la documentazione di supporto di [!DNL Flashtalking] per accedere alle macro dei passaggi dati in `https://support.flashtalking.com%2Fhc%2Fen-us%2Farticles%2F4409808166419-Accessing-Data-Pass-Macros`.

Usa le macro per [!DNL Flashtalking] annunci video e display per i seguenti tipi di implementazioni di [!DNL Analytics for Advertising]:

* **Inserzionisti con il codice JavaScript [!DNL Adobe] [!DNL Analytics for Advertising] implementato sui loro siti Web**: il codice JavaScript registra già i parametri della stringa di query AMO ID (`s_kwcid`) e `ef_id`. Tuttavia, l’utilizzo delle macro estende il tracciamento per includere conversioni basate su clic quando i cookie di terze parti non sono supportati. La best practice prevede l’aggiunta di macro nelle sezioni seguenti ai tag annuncio per acquisire dati di click-through aggiuntivi che non vengono acquisiti tramite il codice JavaScript.

  >[!NOTE]
  >
  >Il codice JavaScript è una soluzione per il tracciamento dei clic solo quando i cookie sono ancora disponibili. Una volta interrotti i cookie, sarà necessario implementare le macro seguenti.

* **Inserzionisti i cui siti Web non utilizzano il codice JavaScript [!DNL Analytics for Advertising] e si basano invece sull&#39;inoltro lato server [!DNL Analytics] solo per i dati click-through** (senza dati view-through): le seguenti macro sono necessarie per segnalare l&#39;attività di clic sul sito guidata dagli annunci acquistati tramite Adobe Advertising.

## Visualizzare i tag annuncio

All&#39;interno delle impostazioni dei tag annuncio di [!DNL Flashtalking], aggiungi la seguente macro alla fine dell&#39;URL di click-through nel campo `Clicktag`:

```
[ftqs:[AdobeAMO]]
```

Se si tratta della prima o unica stringa di query dopo l&#39;URL di base, separarla dall&#39;URL di base con `?`. Se l&#39;URL di base include più stringhe di query, iniziare la prima stringa con `?` e ogni stringa successiva con `&`.

Esempi:

`https://www.adobe.com/products/photoshop?[ftqs:[AdobeAMO]]`

`https://www.adobe.com/products/photoshop?cid=email&[ftqs:[AdobeAMO]]`

## Tag annuncio video

All&#39;interno delle impostazioni dei tag annuncio di [!DNL Flashtalking], aggiungi la seguente macro alla fine dell&#39;URL di click-through nel campo `Clicktag`:

```
[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]
```

Se si tratta della prima o unica stringa di query dopo l&#39;URL di base, separarla dall&#39;URL di base con `?`. Se l&#39;URL di base include più stringhe di query, iniziare la prima stringa con `?` e ogni stringa successiva con `&`.

Esempi:

`https://www.adobe.com/products/photoshop?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

`https://www.adobe.com/products/photoshop?cid=email&[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

>[!MORELIKETHIS]
>
>* [Panoramica di [!DNL Analytics for Advertising]](overview.md)
>* [ID Adobe Advertising utilizzati da [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Aggiungi [!DNL Analytics for Advertising] Macro ai [!DNL Google Campaign Manager 360] Tag annuncio](/help/integrations/analytics/macros-google-campaign-manager.md)

