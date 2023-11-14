---
title: Utilizzo di [!DNL Last Event Service] Libreria JavaScript con [!DNL Web SDK]
description: Scopri come passare da utilizzando [!DNL Analytics] [!DNL visitorAPI] libreria a [!DNL Experience Platform] [!DNL Web SDK] libreria per [!DNL Analytics for Advertising] implementazione.
feature: Integration with Adobe Analytics
exl-id: 764724a2-536a-43b9-955d-28d6146db29a
source-git-commit: 7501c1f8f6477a4ee6de64c64d52b1aafaf16994
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---

# Utilizzo di [!DNL Last Event Service] Libreria JavaScript con Adobe Experience Platform [!DNL Web SDK]

*Per gli inserzionisti con una sola integrazione Adobi Advertising-Adobe Analytics*

Se la tua organizzazione utilizza il precedente Adobe Analytics `visitorAPI.js` per la raccolta dei dati, puoi facoltativamente passare all’utilizzo della [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html) libreria (`alloy.js`), che consente di interagire con i vari servizi di Experience Cloud tramite il [!DNL Edge Network].

Il [!DNL Analytics for Advertising] [!DNL Last Event Service] La libreria JavaScript registra gli eventi view-through e click-through e li unisce alle conversioni associate utilizzando un ID supplementare (`SDID`). Il [!DNL Web SDK] libreria, tuttavia, non fornisce un [!DNL stitch ID]. Per utilizzare [!DNL Web SDK] per [!DNL Analytics for Advertising], sarà necessario modificare 1) il [!DNL Last Event Service] tag utilizzati nelle pagine Web e 2) il [!DNL Web SDK] `sendEvent` comandi di conseguenza.

## Passaggio 1: modificare [!DNL Last Event Service] Tag per generare un `[!DNL StitchID]`

In [!DNL Analytics for Advertising] [!DNL Last Event Service] utilizzato nelle pagine Web, aggiungi il codice per generare il `[!DNL StitchID]` utilizzando il generatore di ID casuale fornito in bundle con la libreria.

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

Inserisci la seguente proprietà all’interno del [!DNL Web SDK] `sendEvent` comando per inviare [!DNL StitchID] a [!DNL Experience Edge] as [!DNL Experience Data Model] Dati (XDM) per [!DNL Analytics].<!-- The library will send the StitchID to [!DNL Experience Edge] as `[_adcloud.advertisingStitchID](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/adcloud/stitch.schema.md)`. --> [!DNL Analytics] utilizzerà il valore come `SDID`.

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
