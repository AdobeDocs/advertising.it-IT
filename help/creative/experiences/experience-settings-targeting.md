---
title: Impostazioni delle esperienze mirate
description: Vedi le descrizioni di tutte le impostazioni per le esperienze annuncio mirate.
feature: Creative Experiences
exl-id: cb6fd855-6534-4eac-b34b-323073d186be
source-git-commit: 4b780760e5a7a0c3d370054fce8b1c15fbc6802d
workflow-type: tm+mt
source-wordcount: '1133'
ht-degree: 0%

---

# Impostazioni delle esperienze annuncio di destinazione

*Versione beta chiusa*

## [!UICONTROL Experience basics] sezione

**[!UICONTROL Ad Type]:** (sola lettura per le esperienze esistenti) Il tipo di annunci inclusi nell&#39;esperienza: *[!UICONTROL Standard Display]*, *[!UICONTROL Dynamic Display]* o *[!UICONTROL Video]*. Una volta salvata l’esperienza, non puoi modificare il tipo di annuncio.

**[!UICONTROL Advertiser]:** (sola lettura per le esperienze esistenti) L&#39;inserzionista che farà offerte sulle combinazioni creativa e di destinazione incluse nell&#39;esperienza. Una volta salvata l&#39;esperienza, non è possibile modificare l&#39;inserzionista.

**[!UICONTROL Experience Name]:** Nome univoco per l&#39;esperienza. **Suggerimento:** utilizza un nome facilmente reperibile quando utilizzi l&#39;esperienza come annuncio in Advertising DSP o in un altro DSP.

**[!UICONTROL Creative Library]:** (sola lettura per le esperienze esistenti) Un&#39;unica libreria creativa da utilizzare per l&#39;esperienza. Una volta salvata l&#39;esperienza, non puoi modificare la libreria.

## [!UICONTROL Default creatives] sezione

**\[Creatività predefinita specificata\]:** Creatività predefinita da utilizzare quando un browser non è in grado di visualizzare le creatività assegnate all&#39;esperienza, ad esempio quando il browser non è abilitato per JavaScript o l&#39;ad server non può personalizzare l&#39;annuncio a causa di ritardi. Per le esperienze di visualizzazione standard, includi un&#39;immagine creativa per ogni dimensione dell&#39;annuncio a cui si applica l&#39;esperienza. Per le esperienze video standard, includi una creatività video per annuncio e per dimensione a cui si applica l’esperienza. Le tue scelte determinano le dimensioni creative che possono essere utilizzate per l&#39;esperienza.

Per le esperienze con targeting di alberi delle decisioni, è possibile sostituire le creatività predefinite con bundle creativi che contengono creatività delle stesse dimensioni dall&#39;interno dell&#39;albero delle decisioni.<!-- verify -->

* Per aggiungere un contenuto creativo predefinito con dimensioni diverse, fare clic su **[!UICONTROL + Add Sizes]**, selezionare la casella di controllo accanto a ogni contenuto creativo da aggiungere nel riquadro di destra, quindi fare clic su **[!UICONTROL Add Creatives]**.

* Per eliminare un contenuto creativo predefinito, posizionare il cursore sulla miniatura e fare clic su ![Elimina](/help/creative/assets/delete.png "Elimina").

* Per eliminare tutti i creativi predefiniti, fare clic su ![Elimina](/help/creative/assets/delete.png "Elimina") **[!UICONTROL Delete all]**.

* Per mostrare o nascondere il riquadro Creative a destra, fare clic su ![Mostra/Nascondi](/help/creative/assets/hide-show-creatives.png "Mostra/Nascondi") in alto a destra.

## [!UICONTROL Targeting] sezione

**[!UICONTROL Targeting]:** (sola lettura per le esperienze esistenti) Abilita il targeting creativo utilizzando una struttura decisionale e la creazione automatica di tag. Una volta salvata l&#39;esperienza, non puoi modificare questa impostazione.

**[!UICONTROL Language Targeting]:** (solo esperienze con annunci standard; facoltativo; sola lettura per esperienze esistenti) Controlla le impostazioni della lingua del browser dell&#39;utente e visualizza un contenuto creativo nella lingua specificata quando è disponibile un contenuto creativo in tale lingua. Quando un contenuto creativo nella lingua specificata dal browser non è disponibile, viene utilizzata l&#39;impostazione [!UICONTROL Preferred language].

Una volta salvata l&#39;esperienza, non puoi modificare questa impostazione.

**[!UICONTROL Preferred language]:** (solo esperienze con annunci standard; sola lettura per esperienze esistenti) La lingua per tutti gli annunci creati dall&#39;esperienza, tranne quando [!UICONTROL Language Targeting] è abilitato. Una volta salvata l&#39;esperienza, non puoi modificare questa impostazione.

## [!UICONTROL Advanced] sezione

**Passaggio dati:** (sola lettura per le esperienze esistenti; facoltativo) per eseguire il targeting degli utenti in base a coppie chiave-valore specifiche passate in tempo reale da DSP, publisher o partner su impression (ad esempio SKU=01234567890123 o Cart=empty). Puoi specificare fino a cinque chiavi predefinite per il passaggio dei dati (parametri). Quando imposti il targeting all’interno della struttura decisionale, puoi includere un livello di nodi di destinazione del passaggio dei dati, personalizzare facoltativamente le chiavi e specificare i valori di destinazione per ciascun nodo. Se non specifichi alcuna chiave in questo campo quando crei l’esperienza, puoi comunque specificarla all’interno della struttura decisionale.

A ogni chiave viene aggiunta una macro nel tag esperienza annuncio, che puoi generare per implementare come annuncio nel DSP.

**Raggio:** (solo esperienze con annunci dinamici; facoltativo) Un raggio da un CAP degli Stati Uniti specificato nel file di feed per il target; seleziona un raggio da 0 miglia a 200 miglia. Il file di feed utilizzato per creare gli annunci dinamici per l&#39;esperienza deve includere una colonna [!UICONTROL ZIP]<!-- or a user-named column mapped to a ZIP column --> con un valore per ogni riga prodotto nel file. Ad esempio, per un raggio di 10 miglia, un annuncio per un prodotto disponibile in 95110 può essere visualizzato agli utenti entro 10 miglia da 95110 (determinato dall’indirizzo IP dell’utente).

**Pixel RT:** (sola lettura per le esperienze esistenti; facoltativo) Un pixel di retargeting [!UICONTROL Creative] per la destinazione potenziale. Quando imposti il targeting all’interno dell’albero decisionale, puoi includere un livello di nodi di destinazione di pixel RT. Per ogni nodo, specificherai il pixel di destinazione e i valori per gli attributi del pixel necessari per mostrare i creativi nei bundle creativi assegnati. Se non specifichi un pixel in questo campo quando crei l&#39;esperienza, puoi comunque specificarne uno all&#39;interno dell&#39;albero decisionale.<!-- May move this to just within the decision tree. -->

**Etichetta:**<!-- should be "Labels" --> (Facoltativo) Qualsiasi etichetta specifica di [!DNL Creative] da applicare all&#39;esperienza. È possibile filtrare le esperienze per etichetta nella visualizzazione Esperienze e includere la dimensione [!UICONTROL Experience Label] in [!UICONTROL Custom Creative Report].

* Per selezionare le etichette esistenti, fare clic su ![Giù](/help/creative/assets/chevron-down.png "Giù") e selezionare la casella di controllo accanto a ogni etichetta da applicare.

* Per cercare le etichette esistenti, inizia a immettere una stringa di testo all’interno del nome dell’etichetta.

* Per creare una nuova etichetta da applicare, aprire l&#39;elenco, fare clic su **+ Aggiungi etichetta**, immettere un nuovo nome etichetta nel campo [!UICONTROL Label] e quindi fare clic su **Crea**.

* Per rimuovere un&#39;etichetta, deselezionare la casella di controllo accanto al nome.

**URL di tracciamento impression:** (facoltativo) URL di tracciamento delle impression di terze parti da aggiungere all&#39;URL della pagina di destinazione per qualsiasi annuncio creato dall&#39;esperienza. Puoi includere fino a cinque URL. Per aggiungere un URL aggiuntivo, fai clic su ![icona](/help/creative/assets/create.png) **[!UICONTROL Add More] e immetti l&#39;URL.

Dopo aver immesso un URL, tutte le [macro disponibili](/help/creative/creative-macros.md) e i dati con cui vengono sostituite sono elencati più in basso nella pagina. Per inserire una delle macro nell&#39;URL, posizionare il cursore sulla descrizione della macro e fare clic su ![Copia negli Appunti](/help/creative/assets/copy-to-clipboard.png "Copia negli Appunti"), quindi incollare la macro nel campo URL.

>[!NOTE]
>
>* [!DNL Creative] aggiunge automaticamente i propri tag di tracciamento delle impression all&#39;URL della pagina di destinazione.
>* Puoi [ignorare questo URL per qualsiasi contenuto creativo nell&#39;esperienza](experience-tracking-urls-targeting.md).
>* È inoltre possibile immettere codice di tracciamento delle impression JavaScript di terze parti nel campo [!UICONTROL Client JS]

**URL di tracciamento dei clic:** (facoltativo) (facoltativo) un URL di tracciamento dei clic di terze parti da aggiungere all&#39;URL della pagina di destinazione. Puoi includere fino a cinque URL. Per aggiungere un URL aggiuntivo, fai clic su ![icona](/help/creative/assets/create.png) **[!UICONTROL Add More] e immetti l&#39;URL.

Dopo aver immesso un URL, tutte le [macro disponibili](/help/creative/creative-macros.md) e i dati con cui vengono sostituite sono elencati più in basso nella pagina. Per inserire una delle macro nell&#39;URL, posizionare il cursore sulla descrizione della macro e fare clic su ![Copia negli Appunti](/help/creative/assets/copy-to-clipboard.png "Copia negli Appunti"), quindi incollare la macro nel campo URL.

>[!NOTE]
>
>* [!DNL Creative] aggiunge automaticamente i propri tag di tracciamento delle impression all&#39;URL della pagina di destinazione.
>* Puoi [ignorare questo URL per qualsiasi contenuto creativo nell&#39;esperienza](experience-tracking-urls-targeting.md).

**JS client:** (facoltativo):

* (Quando l’inserzionista utilizza un fornitore di conformità OBA per gli annunci) Codice JavaScript che punta alla sovrapposizione dell’annuncio che consente agli utenti di rinunciare al targeting comportamentale online (OBA).

* Eventuale codice di tracciamento delle impression JavaScript di terze parti da aggiungere alla pagina di destinazione. **Nota:** Puoi anche immettere un URL di tracciamento delle impression di terze parti nel campo [!UICONTROL Impression Tracking URL].

>[!MORELIKETHIS]
>
>* [Crea un&#39;esperienza con il targeting dell&#39;albero delle decisioni](experience-create-targeting.md)
>* [Modifica un&#39;esperienza con il targeting dell&#39;albero delle decisioni](experience-edit-targeting.md)
>* [Macro disponibili per il tracciamento degli URL](/help/creative/creative-macros.md)
