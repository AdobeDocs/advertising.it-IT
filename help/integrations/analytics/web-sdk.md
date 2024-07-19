---
title: Utilizzo della  [!DNL Last Event Service] libreria JavaScript con [!DNL Web SDK]
description: Scopri i passaggi per passare dall'utilizzo della libreria  [!DNL Analytics] [!DNL visitorAPI] alla libreria  [!DNL Experience Platform] [!DNL Web SDK] per l'implementazione  [!DNL Analytics for Advertising] .
feature: Integration with Adobe Analytics
exl-id: 764724a2-536a-43b9-955d-28d6146db29a
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%

---

# Utilizzo della libreria JavaScript [!DNL Last Event Service] con Adobe Experience Platform [!DNL Web SDK]

*Inserzionisti con una sola integrazione Adobe Advertising-Adobe Analytics*

Se la tua organizzazione utilizza la libreria legacy di Adobe Analytics `visitorAPI.js` per la raccolta dati, puoi opzionalmente passare a utilizzare la libreria [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html) (`alloy.js`), che ti consente di interagire con i vari servizi Experience Cloud tramite [!DNL Edge Network].

La libreria JavaScript [!DNL Analytics for Advertising] [!DNL Last Event Service] registra gli eventi view-through e click-through e li unisce alle conversioni associate utilizzando un ID supplementare (`SDID`). La libreria [!DNL Web SDK], tuttavia, non fornisce [!DNL stitch ID]. Per utilizzare [!DNL Web SDK] per [!DNL Analytics for Advertising], è necessario modificare 1) il tag [!DNL Last Event Service] utilizzato nelle pagine Web e 2) i comandi [!DNL Web SDK] `sendEvent` di conseguenza.

## Passaggio 1: modifica il tag [!DNL Last Event Service] per generare un tag `[!DNL StitchID]`

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
