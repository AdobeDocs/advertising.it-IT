---
title: Tag Adobe Advertising di mappatura della conversione
description: Scopri il tag di mappatura della conversione basato su JavaScript per ITP 2.2, che consente ad Adobe Advertising di tenere traccia di un evento di conversione che si verifica su una pagina che non è la pagina di destinazione.
exl-id: cbeaf3cd-f1ab-419d-bba8-58a1c8215352
feature: Search Tracking
source-git-commit: 2c755eaa01f5bc7606074bb0fc276901c21ef807
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 0%

---

# Tag di mappatura della conversione JavaScript di Adobe Advertising

*Inserzionisti con solo monitoraggio delle conversioni di Adobe Advertising*

Il tag di mappatura della conversione basato su JavaScript Adobe Advertising, se utilizzato in aggiunta al tag di tracciamento della conversione v2 o v3 Adobe Advertising JavaScript, consente ad Adobe Advertising di tenere traccia di un evento di conversione che si verifica su una pagina che non è la pagina di destinazione. La soluzione ITP 2.2 memorizza il cookie di un utente nell’archivio locale in un iFrame di proprietà dell’inserzionista. L’archiviazione locale può quindi rendere persistente il valore del cookie dal clic a valle alla pagina di conversione.

Utilizza il tag di mappatura della conversione per garantire che Adobe Advertising possa tracciare tutte le conversioni che si verificano all’interno dei browser Apple Safari e Mozilla Firefox, che limitano la persistenza dei cookie di prime parti. <!-- For all requirements to track conversions from Safari, see "Track Conversions from Apple Safari Browsers." -->

Per utilizzare il tag di mappatura della conversione:

1. [Distribuire il tag di mappatura della conversione](#deploy-conversion-mapping-tag).

1. Se la tua organizzazione utilizza più ID organizzazione del servizio Adobe Experience Cloud Identity (precedentemente denominati ID organizzazione IMS), [aggiorna i tag di conversione](#update-conversion-tags) per includere l&#39;ID organizzazione.

1. [Convalida la distribuzione tag](#validate-conversion-mapping).

## Distribuire il tag di mappatura della conversione JavaScript per ITP 2.2 {#deploy-conversion-mapping-tag}

>[!NOTE]
>
>Se si utilizza il tag di mappatura della conversione JavaScript per ITP 2.0, sostituire il tag esistente in tutte le pagine di conversione con uno dei seguenti tag.<!-- any other instructions, too? Point them to the other page on Track Conversions from Safari...." -->

* Se la tua organizzazione utilizza un singolo ID organizzazione, utilizzato per il tuo account Search, Social e Commerce, utilizza il seguente tag:

  `<script src="//www.everestjs.net/static/amo-conversion-mapper.js" userid="{AMO User ID}"></script>`

  dove sostituisci `{AMO User ID}` con l&#39;ID utente univoco per il tuo account Search, Social e Commerce.

* Se la tua organizzazione utilizza più ID organizzazione, utilizza il seguente tag:

  `<script src="//www.everestjs.net/static/amo-conversion-mapper.js" imsorgid="{xxxxxx@AdobeOrg}" userid="{AMO User ID}"></script>`

  dove:

   * si sostituisce il valore `{xxxxxx@AdobeOrg}` con l&#39;ID organizzazione per il quale vengono tracciate le conversioni della pagina. Utilizza lo stesso ID organizzazione per tutte le pagine di conversione.

   * sostituisci `{AMO User ID}` con l&#39;ID utente univoco per il tuo account Search, Social e Commerce.

* Se si utilizza un sistema di gestione dei tag che non supporta l&#39;aggiunta della variabile `imsorgid` al tag script, utilizzare il codice seguente:

  *Se la tua organizzazione utilizza un singolo ID organizzazione:

  ```
  <script>
  window.ad_cloud = window.ad_cloud || {};
  window.ad_cloud.userid = "{AMO User ID}"
  </script>
  <script src="//www.everestjs.net/static/amo-conversionmapper.js"></script>
  ```

  dove sostituisci `{AMO User ID}` con l&#39;ID utente univoco per il tuo account Search, Social e Commerce.

   * Se la tua organizzazione utilizza più ID organizzazione:

     ```
     <script>
     window.ad_cloud = window.ad_cloud || {};
     window.ad_cloud.imsorgid = "{xxxxxx@AdobeOrg}"
     window.ad_cloud.userid = "{AMO User ID}"
     </script>
     <script src="//www.everestjs.net/static/amo-conversionmapper.js"></script>
     ```

     dove:

      * si sostituisce il valore `{xxxxxx@AdobeOrg}` con l&#39;ID organizzazione per il quale vengono tracciate le conversioni della pagina. Utilizza lo stesso ID organizzazione per tutte le pagine di conversione.

      * sostituisci `{AMO User ID}` con l&#39;ID utente univoco per il tuo account Search, Social e Commerce.

Se non conosci il valore del tuo ID organizzazione o dell&#39;ID utente di Search, Social e Commerce, chiedi al team del tuo account Adobe.

### Esempi

```
<script src="//www.everestjs.net/static/amo-conversion-mapper.js" imsorgid="abc12345@AdobeOrg" userid="99999"></script>`
```

```
<script>
window.ad_cloud = window.ad_cloud || {};
window.ad_cloud.imsorgid = "abc12345@AdobeOrg"
window.ad_cloud.userid = "99999"
</script>
<script src="//www.everestjs.net/static/amo-conversion-mapper.js"></script>
```

### Dove aggiungere il tag

Aggiungi il tag in qualsiasi pagina che potrebbe essere una pagina di destinazione da un clic di ricerca (idealmente, su tutte le pagine, poiché le pagine di destinazione possono cambiare nel tempo). Deve essere caricato prima del tag di tracciamento della conversione v3 di Adobe Advertising JavaScript.

Se si trova all’interno di un iframe o di un tag contenitore,:

* L’iframe deve trovarsi sullo stesso livello del dominio di primo livello.

* Il tag di mappatura della conversione deve trovarsi a un solo (1) livello sotto il dominio di primo livello.

## Aggiornare i tag di conversione JavaScript {#update-conversion-tags}

Se la tua organizzazione utilizza più ID organizzazione, aggiungi l’ID organizzazione per il quale vengono tracciate le conversioni di una pagina ai tag di conversione JavaScript esistenti.

Se la tua organizzazione utilizza un ID organizzazione, questo passaggio non è necessario.

### Tag di JavaScript V2

Aggiungi la seguente stringa all’inizio del tag dello script di conversione:

`ef_imsorgid="{xxxxxx@AdobeOrg}";`

in cui si sostituisce il valore `{xxxxxx@AdobeOrg}` con l&#39;ID organizzazione per il quale vengono tracciate le conversioni della pagina.

Esempio:

```
<script language="javascript" src="https://www.everestjs.net/static/st.v2.js"></script>
<script language="javascript">
ef_imsorgid = "abc12345@AdobeOrg";
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

### Tag JavaScript V3

Dopo aver definito `window.EF`, aggiungere la seguente stringa:

`window.EF.imsorgid = "{xxxxxx@AdobeOrg}";`

in cui si sostituisce il valore `{xxxxxx@AdobeOrg}` con l&#39;ID organizzazione per il quale vengono tracciate le conversioni della pagina.

Esempio:

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
        window.EF.imsorgid ="abc12345@AdobeOrg";
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

## Convalidare la distribuzione dei tag {#validate-conversion-mapping}

Chiedi al tuo Account Team Adobe di aiutarti con la convalida del tag di mappatura della conversione e del tag di conversione regolare (se lo hai aggiornato).
