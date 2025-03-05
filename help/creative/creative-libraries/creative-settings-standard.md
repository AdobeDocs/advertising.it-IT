---
title: Impostazioni creative
description: Informazioni su xxxx.
feature: Creative Standard Creatives
exl-id: 8eb66310-4860-4ca0-9678-a9e33639c529
source-git-commit: 8d88a46e82a17ce5d2debf93ea0652f35a734d7a
workflow-type: tm+mt
source-wordcount: '1810'
ht-degree: 0%

---

# Impostazioni creative

*Versione beta chiusa*

Le impostazioni variano in base al tipo di creatività.

Quando si modificano più contenuti creativi contemporaneamente:

* È possibile modificare le impostazioni di ogni creativo contemporaneamente o singolarmente. Per impostazione predefinita, vengono selezionati tutti i creativi selezionati e le impostazioni specificate vengono applicate a tutti i creativi selezionati. Per modificare le impostazioni per creativi specifici, deseleziona ogni creativo inapplicabile prima di modificare i campi; se necessario, ripeti l’operazione per ulteriori creativi.

* Alcune impostazioni vengono applicate a tutti i creativi selezionati.

## Impostazioni creative flessibili per HTML5 {#creative-settings-flexible-html5}

### Scheda Dettagli

**Nome Creative:** il nome della creatività. Il nome del modello o del file caricato è utilizzato per impostazione predefinita, ma puoi modificarlo. Per più creativi, puoi modificare i singoli nomi creativi. **Suggerimento:** includere la dimensione dell&#39;annuncio nel nome della creatività e utilizzare un nome che risulti facile da trovare quando si include la creatività in un&#39;esperienza.

**Lingua:** lingua predefinita per ogni annuncio a cui si associano i creativi. Quando carichi o modifichi più creativi, lo stesso valore viene applicato a ciascun creativo selezionato.

**Dimensione creativa:** (sola lettura per i creativi esistenti) Dimensioni del creativo. Se le immagini incluse nel contenuto creativo sono più grandi delle dimensioni specificate, vengono ridimensionate di conseguenza.

**[!UICONTROL Click Tags]:** Le variabili che consentono i reindirizzamenti di tracciamento dei clic dagli annunci banner inclusi. I nomi delle variabili e gli URL della pagina di destinazione corrispondenti vengono compilati dall’unità creativa caricata, ma puoi modificare gli URL predefiniti. Per più creativi, puoi modificare i singoli tag di clic.

<!-- I don't see this as of 1/30. I do see the option to create one custom LP per creative (for any creative type), not one per click tag for flexible HTML5 creatives.
>[!NOTE]
>
>When you include the creative in an experience, you can replace the default value for any of the click tags with a custom landing page URL to generate a derivation of the base creative.
-->

**Etichetta:** (facoltativo) qualsiasi etichetta da applicare a tutti i creativi selezionati. È possibile filtrare i creativi per etichetta in varie visualizzazioni in [!DNL Creative].

* Per selezionare le etichette esistenti, fare clic su ![Giù](/help/creative/assets/chevron-down.png "Giù") e selezionare la casella di controllo accanto a ogni etichetta da applicare.

* Per cercare le etichette esistenti, inizia a immettere una stringa di testo all’interno del nome dell’etichetta.

* Per creare una nuova etichetta da applicare ai creativi, aprire l&#39;elenco, fare clic su **+ Aggiungi etichetta**, immettere un nuovo nome etichetta nel campo [!UICONTROL Label] e quindi fare clic su **Crea**.

* Per rimuovere un&#39;etichetta, deselezionare la casella di controllo accanto al nome.

### Scheda Attributi

**\[Tutti gli attributi di contenuto predefiniti applicabili al contenuto creativo\]:** I nomi e i valori degli attributi predefiniti vengono compilati dall&#39;unità creativa flessibile, ma è possibile modificare facoltativamente i valori.

>[!NOTE]
>
>Puoi anche sostituire il valore predefinito per qualsiasi attributo creativo con un valore personalizzato quando includi il creativo in un’esperienza. La modifica degli attributi all’interno di un’esperienza crea una variante della creatività principale.

Per informazioni sugli attributi disponibili nei modelli predefiniti, vedere &quot;[Modelli creativi flessibili disponibili](#flexible-creative-templates-available).&quot;

### Scheda Modello

*Solo creatività esistente*

Il file modello HTML5 flessibile per la creatività.

Facoltativamente, è possibile sostituire il modello esistente con un nuovo modello con un layout diverso ma con lo stesso insieme di nomi di attributi del modello originale. Il nuovo modello deve essere in formato ZIP con un massimo di 2 MB. Quando la creatività si trova in un bundle, tutte le esperienze che utilizzano il bundle in seguito utilizzano il layout del nuovo modello.

Quando aggiorni il modello per un contenuto creativo principale con varianti secondarie, le varianti vengono aggiornate in base alle modifiche apportate al layout del modello, ma i valori degli attributi per la variante non vengono modificati.

Per sostituire il modello di annuncio esistente:

1. Fare clic su **Aggiorna modello**.

1. Fai clic su **Procedi**.

1. Specificare un file ZIP in uno dei modi seguenti:

   * Trascinare e rilasciare un file sul dispositivo o sulla rete nella casella.

   * Fare clic su **[!UICONTROL select a file]** per individuare il file nel dispositivo o nella rete.

   Consulta le [specifiche degli annunci flessibili](#flexible-ad-spec).

1. Modifica le nuove [impostazioni degli annunci HTML flessibili](#flexible-ad-settings) in base alle esigenze.

1. Fai clic su **[!UICONTROL Edit]**

## Impostazioni creative di HTML5 {#creative-settings-html5}

## Scheda Dettagli

Per i nuovi creativi, le seguenti impostazioni non si trovano in una scheda denominata.

**Nome Creative:** il nome della creatività. Per una nuova creatività, il nome del file viene utilizzato per impostazione predefinita, ma è possibile modificarlo. Per più creativi, puoi modificare i singoli nomi creativi. **Suggerimento:** includere la dimensione dell&#39;annuncio nel nome della creatività e utilizzare un nome che risulti facile da trovare quando si include la creatività in un&#39;esperienza.

**Lingua:** lingua predefinita per ogni annuncio a cui si associano i creativi. Quando carichi o modifichi più creativi, lo stesso valore viene applicato a ciascun creativo selezionato.

**Dimensione creativa:** (sola lettura per i creativi esistenti) Dimensioni del creativo. Se le immagini incluse nel contenuto creativo sono più grandi delle dimensioni specificate, vengono ridimensionate di conseguenza.

**[!UICONTROL Click Tags]:** (solo creatività HTML5 statica) Le variabili che consentono il reindirizzamento del tracciamento dei clic dagli annunci banner inclusi. I nomi delle variabili e gli URL della pagina di destinazione corrispondenti vengono compilati dall’unità creativa caricata, ma puoi modificare gli URL predefiniti. Per più creativi, puoi modificare i singoli tag di clic.

>[!NOTE]
>
>Quando includi il contenuto creativo in un’esperienza, puoi sostituire il valore predefinito per qualsiasi tag di clic con un URL di pagina di destinazione personalizzato per generare una derivazione del contenuto creativo di base.

**URL della pagina di destinazione:** (solo creativi HTML5 semplici con una pagina di destinazione) URL della pagina di destinazione predefinita per ogni annuncio a cui si associano i creativi. Deve essere un URL valido che inizia con http:// o https://. Può includere parametri di tracciamento di terze parti o [[!DNL Creative] macro](/help/creative/creative-macros.md) per uso personale.

Quando includi un contenuto creativo in un bundle e assegni il bundle a un’esperienza, puoi facoltativamente modificare l’URL della pagina di destinazione e aggiungere URL di tracciamento impression e clic e JavaScript per ogni contenuto creativo nel bundle. <!-- NOT SURE APPLICABLE ANYMORE: to generate a variation of the base creative. -->

**Etichetta:** (facoltativo) qualsiasi etichetta da applicare a tutti i creativi selezionati. È possibile filtrare i creativi per etichetta in varie visualizzazioni in [!DNL Creative].

* Per selezionare le etichette esistenti, fare clic su ![Giù](/help/creative/assets/chevron-down.png "Giù") e selezionare la casella di controllo accanto a ogni etichetta da applicare.

* Per cercare le etichette esistenti, inizia a immettere una stringa di testo all’interno del nome dell’etichetta.

* Per creare una nuova etichetta da applicare ai creativi, aprire l&#39;elenco, fare clic su **+ Aggiungi etichetta**, immettere un nuovo nome etichetta nel campo [!UICONTROL Label] e quindi fare clic su **Crea**.

* Per rimuovere un&#39;etichetta, deselezionare la casella di controllo accanto al nome.

### Scheda Modello

*Solo creatività HTML5 statiche esistenti*

Il file modello HTML5 per la creatività.

Facoltativamente, è possibile sostituire il modello esistente con un nuovo modello con un layout diverso ma con lo stesso insieme di nomi di attributi del modello originale. Il nuovo modello deve essere in formato ZIP con un massimo di 2 MB. Quando la creatività si trova in un bundle, tutte le esperienze che utilizzano il bundle in seguito utilizzano il layout del nuovo modello.

Quando aggiorni il modello per un contenuto creativo principale con varianti secondarie, le varianti vengono aggiornate in base alle modifiche apportate al layout del modello, ma i valori degli attributi per la variante non vengono modificati.

Per sostituire il modello di annuncio esistente:

1. Fare clic su **Aggiorna modello**.

1. Fai clic su **Procedi**.

1. Specificare un file ZIP in uno dei modi seguenti:

   * Trascinare e rilasciare un file sul dispositivo o sulla rete nella casella.

   * Fare clic su **[!UICONTROL select a file]** per individuare il file nel dispositivo o nella rete.

   Consulta le [specifiche degli annunci HTML](html5-creative-specification.md).

1. Modifica le nuove [impostazioni annuncio HTML5](#creative-settings-html5) in base alle esigenze.

1. Fai clic su **[!UICONTROL Edit]**

## Impostazioni creative immagini {#creative-settings-image}

**Nome Creative:** il nome della creatività. Per una nuova creatività, il nome del file viene utilizzato per impostazione predefinita, ma è possibile modificarlo. Per più immagini, puoi modificare i singoli nomi creativi. **Suggerimento:** utilizza un nome facile da trovare quando includi il contenuto creativo in un&#39;esperienza.

**Lingua:** lingua predefinita per ogni annuncio a cui si associano i creativi. Lo stesso valore si applica a tutte le immagini selezionate. Quando includi i creativi in un’esperienza, puoi facoltativamente personalizzare le preferenze di lingua per l’esperienza.

**Dimensione Creative:** (sola lettura) le dimensioni delle immagini caricate.

**URL della pagina di destinazione:** URL della pagina di destinazione predefinita per ogni annuncio a cui si associano i creativi. L’URL della pagina di destinazione deve essere un URL valido che inizia con http:// o https://. Può includere parametri di tracciamento di terze parti o [[!DNL Creative] macro](/help/creative/creative-macros.md) per uso personale. Lo stesso valore si applica a tutte le immagini selezionate.

Quando includi un contenuto creativo in un bundle e quindi assegni il bundle a un’esperienza, puoi facoltativamente modificare l’URL della pagina di destinazione e aggiungere URL di tracciamento di impression e clic e JavaScript per ogni contenuto creativo nel bundle. <!-- NOT SURE APPLICABLE ANYMORE: to generate a variation of the base creative. -->

**Etichetta:** (facoltativo) qualsiasi etichetta da applicare a tutti i creativi selezionati. È possibile filtrare i creativi per etichetta in varie visualizzazioni in [!DNL Creative].

* Per selezionare le etichette esistenti, fare clic su ![Giù](/help/creative/assets/chevron-down.png "Giù") e selezionare la casella di controllo accanto a ogni etichetta da applicare.

* Per cercare le etichette esistenti, inizia a immettere una stringa di testo all’interno del nome dell’etichetta.

* Per creare una nuova etichetta da applicare ai creativi, aprire l&#39;elenco, fare clic su **+ Aggiungi etichetta**, immettere un nuovo nome etichetta nel campo [!UICONTROL Label] e quindi fare clic su **Crea**.

* Per rimuovere un&#39;etichetta, deselezionare la casella di controllo accanto al nome.

## Impostazioni creative di terze parti {#creative-settings-third-party}

**Codice JavaScript:** un tag JavaScript (e facoltativamente un tag alternativo per i browser che non supportano JavaScript) che punta alla creatività sul server di annunci di terze parti. Lo script può variare a seconda del server di annunci. Quando modifichi più creativi, lo stesso valore viene applicato a ciascun creativo selezionato.

Tutte le [macro disponibili](/help/creative/creative-macros.md) e i dati con cui vengono sostituite sono elencati sotto il campo di input. Per inserire una delle macro nel tag, posizionare il cursore sulla descrizione della macro e fare clic su ![Copia negli Appunti](/help/creative/assets/copy-to-clipboard.png "Copia negli Appunti"), quindi incollare l&#39;immagine nel punto desiderato all&#39;interno del tag.

Quando includi questa creatività in un’esperienza implementata come annuncio da un DSP, DSP utilizza le informazioni contenute in questo tag per visualizzare l’annuncio e tracciare impression e clic su di esso. Il DSP quindi invia il tag allo scambio di annunci. Quando l&#39;annuncio viene visualizzato e selezionato, il server dell&#39;annuncio, il DSP e [!DNL Creative] tengono traccia degli eventi.

**[!UICONTROL Advertiser]:** (sola lettura) L&#39;inserzionista a cui è disponibile la libreria.

**Nome Creative:** il nome della creatività. **Suggerimento:** utilizza un nome facile da trovare quando includi il contenuto creativo in un&#39;esperienza.

**Dimensione Creative:** (sola lettura per annunci esistenti) le dimensioni della creatività. Per i nuovi creativi, seleziona da un elenco di dimensioni di annuncio standard.
u
**Lingua:** lingua predefinita per ogni annuncio a cui si associano i creativi.

**URL pagina di destinazione:** URL della pagina di destinazione utilizzato per convalidare ogni annuncio a cui si associano i creativi. Il server di annunci di terze parti determina la pagina di destinazione effettiva di ciascun annuncio.

**Etichetta:** (facoltativo) qualsiasi etichetta da applicare a tutti i creativi selezionati. È possibile filtrare i creativi per etichetta in varie visualizzazioni in [!DNL Creative].

* Per selezionare le etichette esistenti, fare clic su ![Giù](/help/creative/assets/chevron-down.png "Giù") e selezionare la casella di controllo accanto a ogni etichetta da applicare.

* Per cercare le etichette esistenti, inizia a immettere una stringa di testo all’interno del nome dell’etichetta.

* Per creare una nuova etichetta da applicare ai creativi, aprire l&#39;elenco, fare clic su **+ Aggiungi etichetta**, immettere un nuovo nome etichetta nel campo [!UICONTROL Label] e quindi fare clic su **Crea**.

* Per rimuovere un&#39;etichetta, deselezionare la casella di controllo accanto al nome.

>[!MORELIKETHIS]
>
>* [Aggiungere creatività standard a una libreria creativa](/help/creative/creative-libraries/creative-add-standard.md)
>* [Modifica creatività standard](/help/creative/creative-libraries/creative-edit-standard.md)
>* [Macro disponibili per il tracciamento degli URL](/help/creative/creative-macros.md)
