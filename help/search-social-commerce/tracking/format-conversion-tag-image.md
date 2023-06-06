---
title: Formato dei tag di tracciamento conversione immagine
description: Fai riferimento al formato dei tag di tracciamento della conversione delle immagini.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# Formato dei tag di tracciamento conversione immagine

>[!NOTE]
>
>Per informazioni su quando utilizzare i tag immagine rispetto ai tag JavaScript, vedi [Domande frequenti sul tracciamento dei tag](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

* Tag non sicuri per siti con HTTP:

   ```
   <img src="http://pixel.everesttech.net/px2/<ef-userid>?px_evt=s&s=<segmentid>&px_evt=t&ev_propertyname=<propertyname>&ev_transid=<transid>" width="1" height="1"/>
   ```

* Tag protetti per i siti con HTTPS:

   ```
   <img src="https://pixel.everesttech.net/px2/<ef-userid>?px_evt=s&s=<segmentid>&px_evt=t&ev_propertyname=<propertyname>&ev_transid=<transid>" width="1" height="1"/>
   ```

dove:

* `<ef-userid>` è un ID utente univoco e numerico che Search, Social &amp; Commerce assegna all’inserzionista.

* `<propertyname>` è la conversione che verrà tracciata. Ad esempio, se tieni traccia di una conversione denominata &quot;registration&quot;, il tag includerà il parametro `ev_registration=<registration>`e dovrai trasferire i ricavi effettivi per ogni transazione (ad esempio `ev_registration=1`). Quando si tiene traccia di più proprietà, queste vengono collegate da una e commerciale (`&`), come `ev_registration=<registration>&ev_sale=<sale>` (ad esempio, `ev_registration=1&ev_sale=12.99`). **Nota:**  Il nome della proprietà non può contenere caratteri speciali.

* `<transid>` è un ID transazione univoco (ad esempio un ID ordine effettivo) generato e passato dall&#39;inserzionista per identificare una transazione. È incluso solo quando &quot;[!UICONTROL Include unique transaction IDs]&quot; è selezionata.

   Search, Social e Commerce utilizzano l’ID transazione per eliminare le transazioni duplicate con lo stesso ID transazione e lo stesso valore della proprietà. L’ID transazione è incluso nel [!UICONTROL Transaction Report], che puoi utilizzare per convalidare i dati all’interno di Adobe Advertising con i dati dell’inserzionista. **Nota:** Se i dati dell’inserzionista non includono un ID univoco per transazione, Search, Social e Commerce ne generano ancora uno in base al tempo della transazione.

<!-- add more links -->

>[!MORELIKETHIS]
>
>* [Informazioni sui tag di tracciamento delle conversioni di Adobe Advertising](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Genera un tag di conversione Adobe Advertising](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Domande frequenti sui tag di conversione e di tracciamento della visualizzazione pagina](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [Formato dei tag di tracciamento della conversione JavaScript versione 2](format-conversion-tag-jsv2.md)
>* [Formato dei tag di tracciamento della conversione JavaScript versione 3](format-conversion-tag-jsv3.md)

