---
title: Formato dei tag di tracciamento delle conversioni di JavaScript versione 2
description: Fai riferimento al formato dei tag di tracciamento delle conversioni di JavaScript versione 2.
exl-id: 75e96f97-a3f0-4f5b-8bbb-4b1e8986f01a
feature: Search Tracking
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# Formato dei tag di tracciamento delle conversioni di JavaScript versione 2

Il seguente formato è per i siti che utilizzano HTTPS. Per i siti che utilizzano HTTP, gli URL devono iniziare con &quot;http&quot;.

>[!NOTE]
>
>Per informazioni su quando utilizzare la versione 2 rispetto alla versione 3, consulta le [domande frequenti sui tag di tracciamento](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

```
<script language="javascript" src="https://www.everestjs.net/static/st.v2.js"></script>
<script language="javascript">
var ef_event_type="transaction";
var ef_transaction_properties = "ev_property name=<property name>&ev_transid=<transid>";
/*
 * Do not modify below this line
 */
var ef_segment = "";
var ef_search_segment = "";
var ef_userid="ef-userid";
var ef_pixel_host="pixel.everesttech.net";
var ef_fb_is_app = 0;
var ef_allow_3rd_party_pixels = 1;
effp();
</script>
<noscript><img src="https://pixel.everesttech.net/<ef-userid>/t?ev_property name=<property name>&ev_transid=<transid>" width="1" height="1"/></noscript>
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
>* [Formato dei tag di tracciamento conversione di JavaScript versione 3](format-conversion-tag-jsv3.md)
>* [Formato dei tag di tracciamento conversione immagine](format-conversion-tag-image.md)
