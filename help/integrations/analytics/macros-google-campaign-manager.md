---
title: Aggiungi [!DNL Analytics for Advertising] Macro a [!DNL Google Campaign Manager 360] Tag ad
description: Scopri perché e come aggiungere [!DNL Analytics for Advertising] macro [!DNL Google Campaign Manager 360] tag ad
feature: Integration with Adobe Analytics
exl-id: 05084a85-5890-4a82-b3eb-4520f44f9d66
source-git-commit: 1c13874967ec4ad264e5fa6a5e0dfeb6120f53cc
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 0%

---

# Aggiungi [!DNL Analytics for Advertising] Macro a [!DNL Google Campaign Manager 360] Tag ad

*Inserzionisti con una sola integrazione Advertising-Adobe Analytics di Adobe*

*Applicabile solo alla DSP pubblicitaria*

Se utilizzi tag di annunci da [!DNL Google Campaign Manager 360] per i tuoi annunci pubblicitari DSP aggiungi [!DNL Analytics for Advertising] agli URL della pagina di destinazione utilizzando [`%p` macro](https://support.google.com/campaignmanager/table/6096962). Record dei parametri `s_kwcid` e `ef_id` parametri della stringa di query nell’URL della pagina di destinazione, consentendo ad Adobe Advertising di inviare dati di clic per gli annunci ad Adobe Analytics.

Usa macro per [!DNL Campaign Manager 360] annunci video e display per i seguenti tipi di [!DNL Analytics for Advertising] implementazioni:

* **Gli inserzionisti con [!DNL Adobe] [!DNL Analytics for Advertising] Codice JavaScript implementato sui loro siti web**: Il codice JavaScript registra già il `s_kwcid` e `ef_id` parametri della stringa di query. Tuttavia, l’utilizzo delle macro estende il tracciamento per includere le conversioni basate su clic quando i cookie di terze parti non sono supportati. La procedura consigliata consiste nell’aggiungere le macro nelle sezioni seguenti ai tag degli annunci per acquisire dati di click-through aggiuntivi non acquisiti tramite il codice JavaScript.

>[!NOTE]
>
>Il codice JavaScript è una soluzione per il tracciamento dei clic solo mentre i cookie sono ancora disponibili. Quando i cookie vengono interrotti, sarà necessario implementare le seguenti macro.

* **Inserzionisti i cui siti web non utilizzano [!DNL Analytics for Advertising] Codice JavaScript e utilizza [!DNL Analytics] inoltro lato server solo per i dati click-through** (senza dati view-through): Le seguenti macro sono necessarie per segnalare l&#39;attività di clic sul sito gestita dagli annunci acquistati tramite Adobe Advertising.

## Aggiungi le macro al tuo [!DNL Google Campaign Manager 360] Annunci

Within [!DNL Google Campaign Manager 360], aggiungi il seguente parametro all’URL della pagina di destinazione per ciascuno dei tuoi annunci video e di visualizzazione: `%pamo=!;`

Puoi specificare l’URL della pagina di destinazione in diversi modi. Le istruzioni per ciascuna opzione sono incluse nelle sottosezioni seguenti.

Di seguito è riportato un esempio dell’URL della pagina di destinazione formattato con il suffisso .

```
https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;
```

>[!NOTE]
>
>
>* Se l’URL della pagina di destinazione include un simbolo hash (#) che non è comune, inserisci il `amo` prima del simbolo hash.
>* Se non sono inclusi altri parametri dopo il `amo` quindi aggiungi un parametro (ad esempio, &amp;a=b) dopo di esso. Esempio:`https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;&a=b#login`


### Configurare il suffisso URL della pagina di destinazione a livello di inserzionista

1. Consulta la sezione [istruzioni per aprire le proprietà dell’inserzionista](https://support.google.com/campaignmanager/answer/2829344).
1. In [!UICONTROL Landing page URL suffix] impostazioni, include `%pamo!;` in [!UICONTROL URL suffix] campo .

### Configurare il suffisso URL della pagina di destinazione a livello di campagna

1. Consulta la sezione [istruzioni per aprire le proprietà della campagna](https://support.google.com/campaignmanager/answer/2838056#set).
1. In [!UICONTROL Landing page URL suffix] impostazioni, include `%pamo!;` in [!UICONTROL URL suffix] campo .

### Configurare il suffisso URL della pagina di destinazione a livello creativo

1. Apri le proprietà creative.
1. In [!UICONTROL Click tags] impostazione, includere `%pamo!;` in [!UICONTROL Landing page] per il tag di clic.

## Come [!DNL Analytics for Advertising] Le macro sono espanse in DSP

In DSP, quando crei un annuncio che include [!DNL Analytics for Advertising] parametro (`amo`), `ef_id` e `s_kwcid` le macro vengono aggiunte automaticamente all&#39;URL di clic. La procedura consigliata consiste nel controllare il tag in DSP per garantire che la `ef_id` e `s_kwcid` sono presenti macro.

Di seguito è riportato un esempio di [!DNL Google Campaign Manager 360] [tag ins](https://support.google.com/campaignmanager/answer/6080468) come appare in DSP.

```
<ins class='dcmads' style='display:inline-block;width:160px;height:600px'
data-dcm-placement='N6482.2155306TUBEMOGUL/B23486129.261313631'
data-dcm-rendering-mode='iframe'
data-dcm-https-only
data-dcm-resettable-device-id=''
data-dcm-app-id='' data-dcm-click-tracker='${TM_CLICK_URL}'
data-dcm-param-amo='ef_id=${TM_USER_ID}:${TM_DATETIME}:d&s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}'>
<script src='https://www.googletagservices.com/dcm/dcmads.js'></script>
</ins>
```

Quando un utente fa clic sull&#39;annuncio, [!DNL Google Campaign Manager 360] vede `%pamo` nel suffisso URL e inserisce in modo dinamico il valore del `amo` nell&#39;URL.

>[!MORELIKETHIS]
>
>* [Panoramica [!DNL Analytics for Advertising]](overview.md)
>* [ID pubblicitari di Adobe utilizzati da [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Aggiungi [!DNL Analytics for Advertising] Macro a [!DNL Flashtalking] Tag ad](macros-flashtalking.md)

