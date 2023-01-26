---
title: Utilizzo della [!DNL Last Event Service] Libreria JavaScript con [!DNL Web SDK]
description: Scopri i passaggi per passare dall’utilizzo di [!DNL Analytics] [!DNL visitorAPI] nella libreria [!DNL Experience Platform] [!DNL Web SDK] libreria [!DNL Analytics for Advertising] implementazione.
feature: Integration with Adobe Analytics
exl-id: 764724a2-536a-43b9-955d-28d6146db29a
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---

# Utilizzo della [!DNL Last Event Service] Libreria JavaScript con Adobe Experience Platform [!DNL Web SDK]

*Inserzionisti con una sola integrazione Advertising-Adobe Analytics di Adobe*

Se l’organizzazione utilizza Adobe Analytics legacy `visitorAPI.js` per la raccolta dati, puoi facoltativamente passare a utilizzando la [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html) libreria (`alloy.js`), che consente di interagire con i vari servizi di Experience Cloud tramite [!DNL Edge Network].

La [!DNL Analytics for Advertising] [!DNL Last Event Service] La libreria JavaScript registra gli eventi view-through e click-through e li unisce alle conversioni associate utilizzando un ID supplementare (`SDID`). La [!DNL Web SDK] la libreria, tuttavia, non fornisce un [!DNL stitch ID]. Per utilizzare [!DNL Web SDK] per [!DNL Analytics for Advertising], sarà necessario modificare 1) il [!DNL Last Event Service] alle pagine web e 2) al [!DNL Web SDK] `sendEvent` comandi di conseguenza.

## Passaggio 1: Modifica il [!DNL Last Event Service] Assegnare tag a Genera un tag `[!DNL StitchID]`

In [!DNL Analytics for Advertising] [!DNL Last Event Service] aggiungi codice per generare il tag utilizzato nelle pagine web `[!DNL StitchID]` utilizzando il generatore di ID casuale incluso nella libreria.

**Tag legacy:**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id');
</script>
```

**Nuovo tag:**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id').generateRandomId();
</script>
```

## Passaggio 2: Utilizzo [!DNL Web SDK] per inviare [!DNL StitchID] come dati XDM per [!DNL Analytics]

Inserisci la seguente proprietà all’interno della [!DNL Web SDK] `sendEvent` per inviare il comando [!DNL StitchID] a [!DNL Experience Edge] come [!DNL Experience Data Model] (XDM) dati per [!DNL Analytics].<!-- The library will send the StitchID to [!DNL Experience Edge] as `[_adcloud.advertisingStitchID](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/adcloud/stitch.schema.md)`. --> [!DNL Analytics] utilizzerà il valore come `SDID`.

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
>* [Panoramica [!DNL Analytics for Advertising]](overview.md)
>* [Codice JavaScript per [!DNL Analytics for Advertising]](/help/integrations/analytics/javascript.md)

