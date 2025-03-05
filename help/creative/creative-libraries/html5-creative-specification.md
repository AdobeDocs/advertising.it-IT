---
title: Specifiche creative di HTML5
description: Consulta le specifiche creative di HTML5 per Advertising Creative.
feature: Creative Standard Creatives
exl-id: 06d29442-d688-4fb8-ad6f-cba0a897fde0
source-git-commit: e966058f5fe3fe9eb039f74bda8ea950f717e123
workflow-type: tm+mt
source-wordcount: '1157'
ht-degree: 0%

---

# Specifiche creative di HTML5 per Advertising Creative

Questo documento descrive i requisiti e il supporto API per i creativi HTML5 in [!DNL Creative]. L’API supporta lo sviluppo di creatività HTML5 i cui attributi possono essere configurati al momento della distribuzione creativa.

## Ambito

[!DNL Creative] supporta i banner HTML5 con creativi non rich media visualizzati all&#39;interno dei bordi impostati su una pagina. È possibile utilizzare i seguenti tipi di creatività HTML5:

<!--Remove to simplify:

* **Simple HTML5:** Supports a single landing page URL that can be configured during creative creation and trafficking.

* **Static HTML5:** Supports up to 5 landing page URLs that can be configured during creative creation and trafficking.

-->

* **HTML5:** supporta fino a 5 URL di pagina di destinazione che possono essere configurati durante la creazione creativa e il traffico.

* **HTML5 flessibile:** supporta fino a 5 URL di pagina di destinazione che possono essere configurati durante la creazione e il traffico creativi e consente inoltre di modificare gli attributi creativi durante la creazione e il traffico creativi.

## Requisiti

### Requisiti di cartella e compressione

* La creatività deve essere inserita in un file ZIP (formato .ZIP). I file ZIP nidificati non sono supportati, pertanto non includere una cartella compressa all’interno della cartella compressa esterna.

* Il file ZIP deve contenere almeno un file HTML, il file di visualizzazione principale di HTML, che include un riferimento alla libreria JavaScript [!DNL Creative]. Il file HTML principale può trovarsi nella cartella principale o in una sottocartella.

* Il file HTML principale può essere denominato qualsiasi cosa, purché non includa caratteri speciali, anche se `index.html` è consigliato.

* Tutte le risorse di supporto necessarie per il rendering del contenuto creativo finale devono trovarsi nella stessa cartella del file di visualizzazione di HTML oppure nelle sottocartelle della cartella principale.

* Non includere nella creatività alcun file a cui la creatività non fa riferimento.

### Inclusione del file JavaScript di Advertising Creative

Il file HTML principale e nessun altro file deve contenere un riferimento al file JavaScript `AMOLibrary.js`. Chiamare il file nella prima riga della sezione `<head>` utilizzando il seguente indirizzo:

`https://ads.everesttech.net/ads/static/local/AMOLibrary.js`

Questo file contiene funzioni per garantire che il test locale degli eventi di uscita avvenga senza problemi.

<!-- Remove to simplify:

### Simple HTML5 creative requirements

#### Support for click-through URLS in simple HTML5

The `<head>` section of the main HTML file must include a JavaScript variable name `clickTag` or `clickTAG`. The value of the variable should be the landing page URL. See the following example.

```
<script type=”text/javascript”>
var clickTag = “http://www.example.com”;
</script>
```

>[!NOTE]
>
>The static URL you include in the HTML5 creative is used for local testing purposes only and will be overwritten. When you upload an HTML5 creative, you'll define the default landing page for the `clickTag` variable. When you assign an uploaded HTML5 creative to an ad experience, you can optionally override the default landing page for the `clickTag` variable, and [!DNL Creative] adds click tracking to the URL when you save the experience.

-->

<!-- Renamed to simplify:
### Static HTML5 creative requirements
-->

### Requisiti creativi di HTML5

#### Supporto per gli URL di click-through in HTML statico 5

##### `amo.registerClick(clkVar, clkUrl)`

Registra gli URL di click-through e il parametro associato utilizzato per fare riferimento a ciascun URL (noto come `clickTag`). Questa API indica al server di annunci [!DNL Creative] dove aggiungere il tracciamento dei clic. Puoi utilizzare questa API per registrare fino a cinque variabili di tag di clic, ciascuna con l’URL della pagina di destinazione corrispondente.

>[!NOTE]
>
>Gli URL statici inclusi nella creatività di HTML5 vengono utilizzati solo a scopo di test locale e verranno sovrascritti. Quando carichi un contenuto creativo di HTML5, definisci la pagina di destinazione predefinita per ogni variabile `clickTag`. Quando si assegna un contenuto creativo di HTML5 caricato a un&#39;esperienza annuncio, è possibile sostituire la pagina di destinazione predefinita per ogni variabile `clickTag` e [!DNL Creative] aggiunge il tracciamento dei clic agli URL quando si salva l&#39;esperienza.

###### Parametri

* `clkVar` — Nome della variabile di clic (in genere &quot;clickTag&quot;), racchiuso tra virgolette.

* `clkUrl` — URL della pagina di destinazione per questa variabile di clic, racchiuso tra virgolette doppie.

###### Utilizzo

Chiamare `amo.registerClick()` nella sezione `<head>` del file HTML principale.

###### Esempio

`amo.registerClick("clickTag","http://www.example.com")`

##### `amo.onAdClick(clk, event)`

Attiva l&#39;evento di uscita, che reindirizza l&#39;utente alla pagina di destinazione configurata per `clickTag`. Durante il test locale, questa funzione avvisa gli sviluppatori se l’URL passato alla funzione è stato registrato.

###### Parametri

* `clkTag` — Nome della variabile di clic utilizzata per assegnare l&#39;URL della pagina di destinazione utilizzando la funzione `amo.registerClick()`, racchiusa tra virgolette singole.

* `event` — (Facoltativo) L&#39;oggetto evento &quot;click&quot; di JavaScript. Registra le coordinate dei clic, che possono essere utilizzate ulteriormente per analizzare le prestazioni creative.

###### Utilizzo

Chiamare `amo.onAdClick()` nella sezione `<body>` del file HTML principale.

###### Esempi

`amo.onAdClick('clickTag')` O `amo.onAdClick('clickTag',clickEvt)`

### Requisiti creativi flessibili per HTML5

#### Supporto per gli URL di click-through in HTML5 flessibile

##### `amo.registerClick(clkVar, clkUrl)`

Registra gli URL di click-through e il parametro associato utilizzato per fare riferimento a ciascun URL (noto come `clickTag`). Questa API indica al server di annunci [!DNL Creative] dove aggiungere il tracciamento dei clic. Puoi utilizzare questa API per registrare fino a cinque variabili di tag di clic, ciascuna con l’URL della pagina di destinazione corrispondente.

>[!NOTE]
>
>Gli URL statici inclusi nella creatività di HTML5 vengono utilizzati solo a scopo di test locale e verranno sovrascritti. Quando carichi un contenuto creativo di HTML5, definisci la pagina di destinazione predefinita per ogni variabile `clickTag`. Quando si assegna un contenuto creativo di HTML5 caricato a un&#39;esperienza annuncio, è possibile sostituire la pagina di destinazione predefinita per ogni variabile `clickTag` e [!DNL Creative] aggiunge il tracciamento dei clic agli URL quando si salva l&#39;esperienza.

###### Parametri

* `clkVar` — Nome della variabile di clic (in genere &quot;clickTag&quot;), racchiuso tra virgolette.

* `clkUrl` — URL della pagina di destinazione per questa variabile di clic, racchiuso tra virgolette doppie.

###### Utilizzo

Chiamare `amo.registerClick()` nella sezione `<head>` del file HTML principale.

###### Esempio

`amo.registerClick("clickTag","http://www.example.com")`

##### `amo.onAdClick(clk, event)`

Attiva l&#39;evento di uscita, che reindirizza l&#39;utente alla pagina di destinazione configurata per `clickTag`. Durante il test locale, questa funzione avvisa gli sviluppatori se l’URL passato alla funzione è stato registrato.

###### Parametri

* `clkTag` — Nome della variabile di clic utilizzata per assegnare l&#39;URL della pagina di destinazione utilizzando la funzione `amo.registerClick()`, racchiusa tra virgolette singole.

* `event` — (Facoltativo) L&#39;oggetto evento &quot;click&quot; di JavaScript. Registra le coordinate dei clic, che possono essere utilizzate ulteriormente per analizzare le prestazioni creative.

###### Utilizzo

Chiamare `amo.onAdClick()` nella sezione `<body>` del file HTML principale.

###### Esempi

`amo.onAdClick('clickTag')` O `amo.onAdClick('clickTag',clickEvt)`

#### Supporto per gli attributi creativi in HTML5 flessibile

##### `amo.registerAttribute(key, type, value)`

Definisce gli attributi dei creativi che possono essere modificati al momento della creazione di creatività o esperienza. Puoi definire fino a 20 attributi creativi che possono essere configurati al momento della creazione creativa o dell’esperienza.

>[!NOTE]
>
>I valori definiti in questo metodo vengono utilizzati solo per lo sviluppo locale e non vengono utilizzati in Live Ad Server.

###### Parametri

* `key` — Nome alfanumerico dell&#39;attributo. Deve iniziare con un carattere alfabetico.

* `type` — Tipo di attributo (`TEXT` o `IMAGE`).

* `value` — Valore dell&#39;attributo per il test. Per gli attributi di tipo `IMAGE`, il valore deve essere il percorso relativo del file di immagine.

###### Utilizzo

Chiamare `amo.registerAttribute()` per registrare un attributo creativo, un tipo e un valore durante il test in modalità locale. Tutti i file di immagine utilizzati come valori di esempio devono essere inclusi nel file ZIP insieme al pacchetto caricato.

##### `amo.attributes`

Un oggetto JSON per eseguire una query sui nomi e i valori delle variabili dell’attributo creativo. Le chiavi oggetto sono i nomi degli attributi e i valori sono i valori di tali attributi.

Nella modalità di test locale, le coppie chiave-valore sono quelle registrate dall&#39;API `amo.registerAttribute`. Per la produzione, i nomi e i valori delle variabili dell’attributo creativo devono essere configurati al momento della creazione creativa e del traffico.

### Requisiti dei contenuti Creative

La maggior parte degli scambi di display disponibili in Advertising DSP hanno i seguenti requisiti creativi:

* Un bordo solido deve circondare tutte le immagini dell’annuncio.

* Non è consentito espandere gli annunci.

* La pagina di destinazione deve aprirsi in una nuova finestra.

* Il dominio della pagina di destinazione e i relativi sottodomini non possono superare i 35 caratteri. **Nota:** gli URL della pagina di destinazione finale sono definiti in DSP e non nelle risorse HTML5 stesse.

* Eventuali clausole di esclusione della responsabilità relative all’offerta di un annuncio devono essere incluse nell’annuncio stesso e non solo nella pagina di destinazione.

<!-- * (Dynamic HTML5 creatives) Do not use `window.open` to handle clicks in your code. Always use `amo.onDynAdClick` to handle click-throughs. -->

## Contenuto di esempio come oggetto e array JSON

### Esempio di contenuto come oggetto JSON

<!-- Should I update these to current/real URLs? Sent email to Apoorva 1/22. -->

```
{
"name": "Adobe Creative",
"description": "Creative",
"picture_url": "http://wwwimages.adobe.com/content/dam/acom/en/products/creativecloud/max2016/images/cc-overview-assets-720x472.png",
"product_url": "http://www.adobe.com/creativecloud.html?promoid=ZP46FD38&mv=other"
}
```

### Contenuto di esempio come array JSON

<!-- Should I update these to current/real URLs? Sent email to Apoorva 1/22. -->

```
[{
"name": "Adobe Creative",
"description": "Creative",
"picture_url": "http://wwwimages.adobe.com/content/dam/acom/en/products/creativecloud/max2016/images/cc-overview-assets-720x472.png",
"product_url": "http://www.adobe.com/creativecloud.html?promoid=ZP46FD38&mv=other"
},

{
"name": "Adobe Creative",
"description": "Creative",
"picture_url": "http://wwwimages.adobe.com/content/dam/acom/en/products/creativecloud/max2016/images/cc-overview-mobile-720x520.png",
"product_url": "http://adobe.com/"
}

]
```

## Esempio di creatività di HTML5

### Esempio di struttura delle cartelle (dopo la decompressione)

* index.html

* /assets (cartella)

   * bg.jpg (immagine JPG, PNG, SVG o GIF)

### Esempio di file HTML (index.html) per semplici creative HTML5

```
<!DOCTYPE html>
<html>
<head>
  <script type="text/javascript" src="https://ads.everesttech.net/ads/static/local/AMOLibrary.js"></script>
  <script type="text/javascript">
  amo.registerClick("clickTag","http://www.example.com");
  </script>
</head>
<body>
  <a href="javascript:amo.onAdClick('clickTag')">
  <img src="assets/bg.jpg" width="300" height="250" style="position:absolute;top:0px;left:0px;">
  </a>
</body>
</html>
```

### Esempio di file HTML (index.html) per le creatività statiche di HTML5

```
<!DOCTYPE html>
<html>
<head>
  <script type="text/javascript" src="https://ads.everesttech.net/ads/static/local/AMOLibrary.js"></script>
  <script type="text/javascript">
  amo.registerClick("clickTag","http://www.example.com");
  amo.registerClick("clickTag2","http://www.example2.com");
  amo.registerClick("clickTag3","http://www.example3.com");
  amo.registerClick("clickTag4","http://www.example4.com");
  amo.registerClick("clickTag5","http://www.example5.com");
  </script>
</head>
<body>
  <a href="javascript:amo.onAdClick('clickTag')">
  <img src="assets/bg.jpg" width="300" height="250" style="position:absolute;top:0px;left:0px;">
  </a>
</body>
</html>
```

>[!MORELIKETHIS]
>
>* [Aggiungere creatività standard a una libreria creativa](/help/creative/creative-libraries/creative-add-standard.md)
