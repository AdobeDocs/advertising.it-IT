---
title: Aggiungi [!DNL Analytics for Advertising] Macro per [!DNL Google Campaign Manager 360] Tag annuncio
description: Scopri perché e come aggiungere [!DNL Analytics for Advertising] macro per [!DNL Google Campaign Manager 360] tag annuncio
feature: Integration with Adobe Analytics
exl-id: 89cd4e1d-277a-4a43-9c38-ae6641302e09
source-git-commit: 703cda43e96dfa9d80bbce2d64192fc461d5dbae
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 0%

---

# Aggiungi [!DNL Analytics for Advertising] Macro per [!DNL Google Campaign Manager 360] Tag annuncio

*Per gli inserzionisti con una sola integrazione Adobi Advertising-Adobe Analytics*

*Applicabile solo a Advertising DSP*

Se utilizzi tag di annunci da [!DNL Google Campaign Manager 360] per gli annunci Advertising DSP, aggiungi [!DNL Analytics for Advertising] parametri degli URL della pagina di destinazione utilizzando [`%p` macro](https://support.google.com/campaignmanager/table/6096962). I parametri registrano l’AMO ID (`s_kwcid`) e `ef_id` parametri della stringa di query nell’URL della pagina di destinazione, che consentono all’Adobe Advertising di inviare i dati di clic per gli annunci ad Adobe Analytics.

Usa macro per [!DNL Campaign Manager 360] annunci display e video per i seguenti tipi di [!DNL Analytics for Advertising] implementazioni:

* **Per gli inserzionisti con [!DNL Adobe] [!DNL Analytics for Advertising] Codice JavaScript implementato sui loro siti web**: il codice JavaScript registra già l’AMO ID (`s_kwcid`) e `ef_id` parametri della stringa di query. Tuttavia, l’utilizzo delle macro estende il tracciamento per includere conversioni basate su clic quando i cookie di terze parti non sono supportati. La best practice prevede l’aggiunta di macro nelle sezioni seguenti ai tag annuncio per acquisire dati di click-through aggiuntivi che non vengono acquisiti tramite il codice JavaScript.

>[!NOTE]
>
>Il codice JavaScript è una soluzione per il tracciamento dei clic solo quando i cookie sono ancora disponibili. Una volta interrotti i cookie, sarà necessario implementare le macro seguenti.

* **Inserzionisti i cui siti Web non utilizzano [!DNL Analytics for Advertising] codice JavaScript e si basano invece su [!DNL Analytics] inoltro lato server solo per dati click-through** (senza alcun dato view-through): le seguenti macro sono necessarie per segnalare l’attività di clic sul sito basata sugli annunci acquistati tramite Adobi Advertising.

## Aggiungere le macro al [!DNL Google Campaign Manager 360] Annunci

Entro [!DNL Google Campaign Manager 360], aggiungi al seguente parametro all’URL della pagina di destinazione per ciascuno degli annunci video e di visualizzazione: `%pamo=!;`

Puoi specificare l’URL della pagina di destinazione in diversi modi. Le istruzioni per ciascuna opzione sono incluse nelle seguenti sottosezioni.

Di seguito è riportato un esempio dell’URL della pagina di destinazione formattato con il suffisso.

```
https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;
```

>[!NOTE]
>
>>* Se l’URL della pagina di destinazione include un simbolo hash (#), che non è comune, inserisci il `amo` prima del simbolo hash.
>* Se non sono inclusi altri parametri dopo il `amo` , quindi aggiungi un parametro (ad esempio, &amp;a=b) dopo di esso. Esempio:`https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;&a=b#login`

### Configurare il suffisso URL della pagina di destinazione a livello di inserzionista

1. Consulta la [istruzioni per aprire le proprietà dell&#39;inserzionista](https://support.google.com/campaignmanager/answer/2829344).
1. In [!UICONTROL Landing page URL suffix] impostazioni, includi `%pamo!;` nel [!UICONTROL URL suffix] campo.

### Configurare il suffisso URL per la pagina di destinazione a livello di campagna

1. Consulta la [istruzioni per aprire le proprietà della campagna](https://support.google.com/campaignmanager/answer/2838056#set).
1. In [!UICONTROL Landing page URL suffix] impostazioni, includi `%pamo!;` nel [!UICONTROL URL suffix] campo.

### Configurare il suffisso URL per la pagina di destinazione a livello creativo

1. Apri le proprietà creative.
1. In [!UICONTROL Click tags] impostazione, includi `%pamo!;` nel [!UICONTROL Landing page] per il tag click.

## Come [!DNL Analytics for Advertising] Le macro vengono estese nell’DSP

In DSP, quando crei un annuncio che include [!DNL Analytics for Advertising] parametro (`amo`), il `ef_id` e `s_kwcid` Le macro vengono aggiunte automaticamente all&#39;URL di clic. La best practice consiste nel controllare il tag in DSP per garantire che `ef_id` e `s_kwcid` macro presenti.

Di seguito è riportato un esempio di [!DNL Google Campaign Manager 360] [tag ins](https://support.google.com/campaignmanager/answer/6080468) come appare nell’DSP.

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

Quando un utente fa clic sull’annuncio, [!DNL Google Campaign Manager 360] vede `%pamo` nel suffisso URL e inserisce dinamicamente il valore del `amo` nell&#39;URL.

>[!MORELIKETHIS]
>
>* [Panoramica di [!DNL Analytics for Advertising]](overview.md)
>* [ID Adobe Advertising utilizzati da [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Aggiungi [!DNL Analytics for Advertising] Macro per [!DNL Flashtalking] Tag annuncio](macros-flashtalking.md)
