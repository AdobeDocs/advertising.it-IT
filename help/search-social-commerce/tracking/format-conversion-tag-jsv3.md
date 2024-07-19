---
title: Formato dei tag di tracciamento delle conversioni di JavaScript versione 3
description: Fai riferimento al formato dei tag di tracciamento delle conversioni di JavaScript versione 3.
exl-id: 9fc6bb15-d880-4353-a8c5-260b7932ab34
feature: Search Tracking
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 0%

---

# Formato dei tag di tracciamento delle conversioni di JavaScript versione 3

Il seguente formato è per i siti che utilizzano HTTPS. Per i siti che utilizzano HTTP, gli URL devono iniziare con &quot;http&quot;.

>[!NOTE]
>
>Per informazioni su quando utilizzare la versione 2 rispetto alla versione 3, consulta le [domande frequenti sui tag di tracciamento](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

```
<script type='text/javascript'>
    (function() {
        var f = function() {
              EF.init({ eventType: "transaction",
                        transactionProperties : "ev_property=<property name>&ev_transid=<transid>",
                        segment : "",
                        searchSegment : "",
                        sku : "",
                        userid : "ef-userid",
                        pixelHost : "pixel.everesttech.net"
                        
                        , allow3rdPartyPixels: 1});
              EF.main();
        };
        window.EF = window.EF || {};
        if (window.EF.main) {
            f();
            return;
        }
        window.EF.onloadCallbacks = window.EF.onloadCallbacks || [];
        window.EF.onloadCallbacks[window.EF.onloadCallbacks.length] = f;
        if (!window.EF.jsTagAdded) {
            var efjs = document.createElement('script'); efjs.type = 'text/javascript'; efjs.async = true;
            efjs.src = 'https://www.everestjs.net/static/st.v3.js';
            var s = document.getElementsByTagName('script')[0]; s.parentNode.insertBefore(efjs, s);
            window.EF.jsTagAdded=1;
        }
    })();
</script>
<noscript><img src="https://pixel.everesttech.net/<ef-userid>/t?ev_property=<property name>&ev_transid=<transid>" width="1" height="1"/></noscript>
```

dove:

* `<ef-userid>` è un ID utente numerico univoco assegnato da Search, Social e Commerce all&#39;inserzionista.

* `<propertyname>` è la conversione da tenere traccia. Ad esempio, se tieni traccia di una conversione denominata &quot;registration&quot;, il tag includerà il parametro `ev_registration=<registration>` e dovrai trasmettere i ricavi effettivi per ogni transazione (ad esempio `ev_registration=1`). Quando si tiene traccia di più proprietà, queste vengono collegate da una e commerciale (`&`), ad esempio `ev_registration=<registration>&ev_sale=<sale>` (ad esempio `ev_registration=1&ev_sale=12.99`). **Nota:** il nome della proprietà non può includere caratteri speciali.

* `<transid>` è un ID transazione univoco (ad esempio un ID ordine effettivo) generato e passato dall&#39;inserzionista per identificare una transazione. È incluso solo quando è selezionata l&#39;opzione &quot;[!UICONTROL Include unique transaction IDs]&quot;.

  Search, Social e Commerce utilizzano l&#39;ID transazione per eliminare le transazioni duplicate con lo stesso ID transazione e lo stesso valore di proprietà. L&#39;ID transazione è incluso in [!UICONTROL Transaction Report], che è possibile utilizzare per convalidare i dati in Adobe Advertising con i dati dell&#39;inserzionista. **Nota:** se i dati dell&#39;inserzionista non includono un ID univoco per transazione, Search, Social e Commerce ne generano ancora uno in base al tempo della transazione.

<!-- add more links -->

>[!MORELIKETHIS]
>
>* [Informazioni su Adobi Advertising di tag per il tracciamento delle conversioni](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Genera un tag di conversione Adobe Advertising](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Domande frequenti sui tag di conversione e di tracciamento della visualizzazione della pagina](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [Formato dei tag di tracciamento conversione di JavaScript versione 2](format-conversion-tag-jsv2.md)
>* [Formato dei tag di tracciamento conversione immagine](format-conversion-tag-image.md)
