---
title: Modificare i contenuti originali standard in una libreria creativa
description: Scopri come modificare le impostazioni delle creatività standard (non dinamiche) in una libreria creativa.
feature: Creative Standard Creatives
exl-id: 333ab2ea-293a-44e2-89e7-06782578318f
source-git-commit: f7d5bf3193cb41ca2a0d4415998209e5a9b724ba
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# Modificare i contenuti originali standard in una libreria creativa

Puoi modificare alcune impostazioni per ogni tipo di creatività standard. È possibile modificare più creativi<!-- or creative variations --> dello stesso tipo creativo (HTML5 semplice con una sola pagina di destinazione, HTML5 statico con più pagine di destinazione, HTML5 flessibile, immagine o terze parti<!-- , or dynamic -->) solo.

Per i creativi flessibili di HTML5 e HTML5 statici, puoi caricare un nuovo file modello con un layout diverso ma con lo stesso set di nomi di attributi. Per semplici creativi HTML5, è possibile modificare qualsiasi attributo o aggiungere immagini caricando un nuovo modello con i nuovi attributi o immagini. In tutti i casi, il modello deve essere un file locale in formato ZIP con un massimo di 2 MB.

Quando modifichi un contenuto creativo<!-- or creative variation --> incluso in un bundle, le modifiche vengono applicate automaticamente a tutte le esperienze che includono il bundle, tranne per il fatto che tutte le pagine di destinazione personalizzate e gli URL di tracciamento specificati a livello di esperienza rimangono applicabili al bundle allegato a tale esperienza.

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Facoltativo) [Personalizzare la visualizzazione](/help/creative/introduction/customize-data-views.md) per includere librerie specifiche.

1. Fai clic sul nome della libreria.

1. Nella scheda **[!UICONTROL Creatives]** > **[!UICONTROL Standard Ads]**, seleziona i creativi:

   * (Facoltativo) [Personalizza la visualizzazione](/help/creative/introduction/customize-data-views.md) per includere creativi specifici.

   * Per modificare un singolo contenuto creativo:

      * Nella visualizzazione a schede, fare clic su **[!UICONTROL ...]** accanto al nome della creatività e quindi su **[!UICONTROL Edit]**.

      * Nella vista tabella, tenere il cursore sulla riga e fare clic su **[!UICONTROL Edit]**.

   * Per modificare uno o più contenuti creativi, selezionare la casella di controllo relativa a ogni contenuto creativo che si desidera modificare. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL Edit]**.

     Per selezionare tutte le righe, selezionare la casella di controllo globale in alto a sinistra.

1. Modifica le [impostazioni creative per le immagini](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-image), le [impostazioni creative per HTML5](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-html5), le [impostazioni creative flessibili per HTML5](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-flexible-html5) o le [impostazioni creative per terze parti](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-third-party). <!-- , or [dynamic creative settings](/help/creative/creative-libraries/creative-settings-dynamic.md) -->

   Quando si modificano più contenuti creativi contemporaneamente:

   * È possibile modificare le impostazioni di ogni creativo contemporaneamente o singolarmente. Per impostazione predefinita, vengono selezionati tutti i creativi selezionati e le impostazioni specificate vengono applicate a tutti i creativi selezionati. Per modificare le impostazioni per creativi specifici, deseleziona ogni creativo inapplicabile prima di modificare i campi; se necessario, ripeti l’operazione per ulteriori creativi.

   * Alcune impostazioni vengono applicate a tutti i creativi selezionati.

   >[!NOTE]
   >
   >* (Solo per creatività HTML5 flessibile) È possibile modificare gli attributi solo per singole creatività.<!-- May never be implemented: Also, when you update the template for a parent creative with child variations, the variations are updated with any changes to the template layout, but the attribute values for the variation aren't changed. -->

<!-- Not there as of 1/16/25. If we do add it, verify the applicable ad types:   
1. (Flexible HTML5 [or third-party should be possible, but not so] creatives; optional) Once you've made your changes, click ![]() to preview the new creative. 
-->

1. Fai clic su **Salva**.

<!-- Not there as of 1/16/25. If we do add it, add back in:
1. (Flexible HTML5 or third-party creatives; optional) Regenerate the thumbnail within the table view or cards view if the change isn't visible immediately.
-->

>[!MORELIKETHIS]
>
>* [Aggiungere creatività standard a una libreria creativa](creative-add-standard.md)
>* [Impostazioni creative standard](/help/creative/creative-libraries/creative-settings-standard.md)
>* [Anteprima di un contenuto creativo](/help/creative/creative-libraries/creative-preview.md)
