---
title: Utilizzo della libreria  [!DNL Last Event Service] JavaScript con [!DNL Web SDK]
description: Scopri i passaggi per passare dall'utilizzo della libreria  [!DNL Analytics] [!DNL visitorAPI] alla libreria  [!DNL Experience Platform] [!DNL Web SDK] per l'implementazione  [!DNL Analytics for Advertising] .
feature: Integration with Adobe Analytics
exl-id: 764724a2-536a-43b9-955d-28d6146db29a
TQID: https://experienceleague.adobe.com/zT1lQV1yotCfJJdzTBGzSspsNEKQEB5ulxYE0qyWa9Q
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 202
ht-degree: 0%

---

# Utilizzo della libreria JavaScript [!DNL Last Event Service] con Adobe Experience Platform [!DNL Web SDK]

*Inserzionisti con una sola integrazione Adobe Advertising-Adobe Analytics*

Se la tua organizzazione utilizza la libreria legacy di Adobe Analytics `visitorAPI.js` per la raccolta dati, puoi opzionalmente passare a utilizzare la libreria [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=it) (`alloy.js`), che ti consente di interagire con i vari servizi Adobe CX Enterprise tramite [!DNL Edge Network].

La libreria JavaScript [!DNL Analytics for Advertising] [!DNL Last Event Service] registra gli eventi view-through e click-through e li unisce alle conversioni associate utilizzando un ID supplementare (`SDID`). La libreria [!DNL Web SDK], tuttavia, non fornisce [!DNL stitch ID]. Per utilizzare [!DNL Web SDK] per [!DNL Analytics for Advertising], è necessario modificare 1) il tag [!DNL Last Event Service] utilizzato nelle pagine Web e 2) i comandi [!DNL Web SDK] `sendEvent` di conseguenza.

## Passaggio 1: modifica il tag [!DNL Last Event Service] per generare un `[!DNL StitchID]`

Nel tag [!DNL Analytics for Advertising] [!DNL Last Event Service] utilizzato nelle pagine Web, aggiungi il codice per generare `[!DNL StitchID]` utilizzando il generatore di ID casuale incluso nella libreria.

**Tag legacy:**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id','rsid');
</script>
```

**Nuovo tag:**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id','rsid').generateRandomId();
</script>
```

## Passaggio 2: utilizzare [!DNL Web SDK] per inviare [!DNL StitchID] come dati XDM per [!DNL Analytics]

Inserire la seguente proprietà nel comando [!DNL Web SDK] `sendEvent` per inviare [!DNL StitchID] a [!DNL Experience Edge] come dati [!DNL Experience Data Model] (XDM) per [!DNL Analytics].<!-- The library sends the StitchID to [!DNL Experience Edge] as `[_adcloud.advertisingStitchID](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/adcloud/stitch.schema.md)`. --> [!DNL Analytics] utilizza il valore come `SDID`.

**Proprietà da aggiungere:**

```
     "_adcloud": {
       "advertisingStitchID": stitchId
     }
```

**Esempio:**

```
<script>
  alloy("sendEvent", {
    "xdm": {
      "commerce": {
        "order": {
                ………
        }
     },
     "_adcloud": {
       "advertisingStitchID": stitchId
     }
    }
  });
</script>
```

>[!MORELIKETHIS]
>
>* [Panoramica di [!DNL Analytics for Advertising]](overview.md)
>* [Codice JavaScript per [!DNL Analytics for Advertising]](/help/integrations/analytics/javascript.md)
