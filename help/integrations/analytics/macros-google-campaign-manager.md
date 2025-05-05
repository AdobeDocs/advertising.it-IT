---
title: Aggiungi [!DNL Analytics for Advertising] macro ai [!DNL Google Campaign Manager 360] tag annuncio
description: Scopri perché e come aggiungere [!DNL Analytics for Advertising] macro ai tuoi [!DNL Google Campaign Manager 360] tag annuncio
feature: Integration with Adobe Analytics
exl-id: 89cd4e1d-277a-4a43-9c38-ae6641302e09
source-git-commit: aa41ba08ba83bfacbc2541c0f0d90336b3c36305
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 0%

---

# Aggiungi macro [!DNL Analytics for Advertising] a [!DNL Google Campaign Manager 360] tag annuncio

*Inserzionisti con una sola integrazione Adobe Advertising-Adobe Analytics*

*Applicabile solo ad Advertising DSP*

Se utilizzi i tag degli annunci di [!DNL Google Campaign Manager 360] per gli annunci di Advertising DSP, aggiungi [!DNL Analytics for Advertising] parametri agli URL della pagina di destinazione utilizzando la macro [`%p`](https://support.google.com/campaignmanager/table/6096962). I parametri registrano i parametri AMO ID (`s_kwcid`) e `ef_id` della stringa di query nell&#39;URL della pagina di destinazione, consentendo ad Adobe Advertising di inviare i dati dei clic per gli annunci ad Adobe Analytics.

Usa le macro per [!DNL Campaign Manager 360] annunci video e display per i seguenti tipi di implementazioni di [!DNL Analytics for Advertising]:

* **Inserzionisti con il codice JavaScript [!DNL Adobe] [!DNL Analytics for Advertising] implementato sui loro siti Web**: il codice JavaScript registra già i parametri della stringa di query AMO ID (`s_kwcid`) e `ef_id`. Tuttavia, l’utilizzo delle macro estende il tracciamento per includere conversioni basate su clic quando i cookie di terze parti non sono supportati. La best practice prevede l’aggiunta di macro nelle sezioni seguenti ai tag annuncio per acquisire dati di click-through aggiuntivi che non vengono acquisiti tramite il codice JavaScript.

>[!NOTE]
>
>Il codice JavaScript è una soluzione per il tracciamento dei clic solo quando i cookie sono ancora disponibili. Una volta interrotti i cookie, sarà necessario implementare le macro seguenti.

* **Inserzionisti i cui siti Web non utilizzano il codice JavaScript [!DNL Analytics for Advertising] e si basano invece sull&#39;inoltro lato server [!DNL Analytics] solo per i dati click-through** (senza dati view-through): le seguenti macro sono necessarie per segnalare l&#39;attività di clic sul sito guidata dagli annunci acquistati tramite Adobe Advertising.

## Aggiungi le macro agli annunci di [!DNL Google Campaign Manager 360]

Entro [!DNL Google Campaign Manager 360], aggiungi il seguente parametro all&#39;URL della pagina di destinazione per ciascuno degli annunci video e di visualizzazione: `%pamo=!;`

Puoi specificare l’URL della pagina di destinazione in diversi modi. Le istruzioni per ciascuna opzione sono incluse nelle seguenti sottosezioni.

Di seguito è riportato un esempio dell’URL della pagina di destinazione formattato con il suffisso.

```
https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;
```

>[!NOTE]
>
>&#x200B;>* Se l&#39;URL della pagina di destinazione include un simbolo hash (#), che non è comune, inserire il parametro `amo` prima del simbolo hash.
>* Se dopo il parametro `amo` non sono inclusi altri parametri, aggiungere un parametro, ad esempio &amp;a=b. Esempio: `https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;&a=b#login`

### Configurare il suffisso URL della pagina di destinazione a livello di inserzionista

1. Consulta le [istruzioni per aprire le proprietà dell&#39;inserzionista](https://support.google.com/campaignmanager/answer/2829344).
1. Nelle impostazioni [!UICONTROL Landing page URL suffix], includere `%pamo!;` nel campo [!UICONTROL URL suffix].

### Configurare il suffisso URL per la pagina di destinazione a livello di campagna

1. Consulta le [istruzioni per aprire le proprietà della campagna](https://support.google.com/campaignmanager/answer/2838056#set).
1. Nelle impostazioni [!UICONTROL Landing page URL suffix], includere `%pamo!;` nel campo [!UICONTROL URL suffix].

### Configurare il suffisso URL per la pagina di destinazione a livello creativo

1. Apri le proprietà creative.
1. Nell&#39;impostazione [!UICONTROL Click tags], includere `%pamo!;` nella colonna [!UICONTROL Landing page] per il tag click.

## Espansione di [!DNL Analytics for Advertising] macro in DSP

In DSP, quando si crea un annuncio che include il parametro [!DNL Analytics for Advertising] (`amo`), le macro `ef_id` e `s_kwcid` vengono aggiunte automaticamente all&#39;URL di clic. La procedura consigliata consiste nel controllare il tag in DSP per verificare che siano presenti le macro `ef_id` e `s_kwcid`.

Di seguito è riportato un esempio di tag [!DNL Google Campaign Manager 360] [ins](https://support.google.com/campaignmanager/answer/6080468) come visualizzato in DSP.

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

Quando un utente fa clic sull&#39;annuncio, [!DNL Google Campaign Manager 360] visualizza `%pamo` nel suffisso URL e inserisce dinamicamente il valore del parametro `amo` nell&#39;URL.

>[!MORELIKETHIS]
>
>* [Panoramica di [!DNL Analytics for Advertising]](overview.md)
>* [ID Adobe Advertising utilizzati da [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Aggiungi [!DNL Analytics for Advertising] Macro ai [!DNL Flashtalking] Tag annuncio](macros-flashtalking.md)
