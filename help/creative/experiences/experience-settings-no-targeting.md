---
title: Impostazioni per esperienze non di destinazione
description: Vedi le descrizioni di tutte le impostazioni per le esperienze pubblicitarie senza targeting della struttura decisionale.
feature: Creative Experiences
exl-id: aeeca035-8ae2-4173-827a-b8690d228549
source-git-commit: 5d8b511708008c77e817ccdb00ae02c158dfe63e
workflow-type: tm+mt
source-wordcount: '1123'
ht-degree: 0%

---

# Impostazioni per esperienze non di destinazione

*Versione beta chiusa*

## [!UICONTROL Experience basics] sezione

**[!UICONTROL Advertiser]:** (sola lettura per le esperienze esistenti) L&#39;inserzionista che farà offerte sui creativi inclusi nell&#39;esperienza. Una volta salvata l&#39;esperienza, non è possibile modificare l&#39;inserzionista.

**[!UICONTROL Experience Name]:** Nome univoco per l&#39;esperienza. **Suggerimento:** utilizza un nome facilmente reperibile quando utilizzi l&#39;esperienza come annuncio in Advertising DSP o in un altro DSP.

**[!UICONTROL Creative Library]:** (sola lettura per le esperienze esistenti) Un&#39;unica libreria creativa da utilizzare per l&#39;esperienza. Una volta salvata l&#39;esperienza, non puoi modificare la libreria.

## [!UICONTROL Default creatives] sezione

**\[Creatività predefinita specificata\]:** Creatività immagine predefinita da utilizzare quando un browser non è in grado di visualizzare i creativi assegnati all&#39;esperienza, ad esempio quando il browser non è abilitato per JavaScript o l&#39;ad server non può personalizzare l&#39;annuncio a causa di ritardi. Includi un&#39;immagine creativa per ogni dimensione dell&#39;annuncio a cui si applica l&#39;esperienza. Le tue scelte determinano le dimensioni creative che possono essere utilizzate per l&#39;esperienza. <!-- In the legacy product, you selected the ad sizes for the experience, and then selected default images for each of those ad sizes. -->

Per le esperienze senza il targeting della struttura decisionale, è possibile sostituire le creatività predefinite con creative della stessa dimensione entro [!UICONTROL Tag Manager].

* Per aggiungere un contenuto creativo predefinito con dimensioni diverse, fare clic su **[!UICONTROL + Add Sizes]**, selezionare la casella di controllo accanto a ogni contenuto creativo da aggiungere nel riquadro di destra, quindi fare clic su **[!UICONTROL Add Creatives]**.

* Per eliminare un contenuto creativo predefinito, posizionare il cursore sulla miniatura e fare clic su ![Elimina](/help/creative/assets/delete.png "Elimina").

* Per eliminare tutti i creativi predefiniti, fare clic su ![Elimina](/help/creative/assets/delete.png "Elimina") **[!UICONTROL Delete all]**.

* Per mostrare o nascondere il riquadro Creative a destra, fare clic su ![Mostra/Nascondi](/help/creative/assets/hide-show-creatives.png "Mostra/Nascondi") in alto a destra.

## [!UICONTROL Targeting] sezione

**[!UICONTROL Targeting]:** (sola lettura per esperienze esistenti) Non applicabile se non si abilita il targeting utilizzando una struttura decisionale; mantenere questa opzione disabilitata.

**[!UICONTROL Dynamic ads]:** (sola lettura per le esperienze esistenti) indica che l&#39;esperienza include annunci dinamici. **Nota:** un&#39;esperienza può includere tutti gli annunci standard o tutti gli annunci dinamici.

**[!UICONTROL Language Targeting]:** (solo esperienze con annunci standard; facoltativo; sola lettura per esperienze esistenti) Controlla le impostazioni della lingua del browser dell&#39;utente e visualizza un contenuto creativo nella lingua specificata quando è disponibile un contenuto creativo in tale lingua. Quando un contenuto creativo nella lingua specificata dal browser non è disponibile, viene utilizzata l&#39;impostazione [!UICONTROL Preferred language]. Una volta salvata l&#39;esperienza, non puoi modificare questa impostazione.

**[!UICONTROL Preferred language]:** (solo esperienze con annunci standard; sola lettura per esperienze esistenti) La lingua per tutti gli annunci creati dall&#39;esperienza, tranne quando [!UICONTROL Language Targeting] è abilitato. Una volta salvata l&#39;esperienza, non puoi modificare questa impostazione.

## [!UICONTROL Advanced] sezione

**Passaggio dati:** (solo esperienze con annunci dinamici; facoltativo) per indirizzare gli utenti in base a coppie chiave-valore specifiche passate in tempo reale su impression da DSP, publisher o partner. È possibile specificare fino a cinque chiavi di trasferimento dati (parametri).<!-- May move this to just within the decision tree. -->

Quando crei un tag di esperienza annuncio per una dimensione creativa specifica, a ogni chiave specificata in questo campo viene aggiunta una macro nel tag. Immetti il valore di ogni coppia chiave-valore all’interno del tag prima di implementare il tag come annuncio nel DSP.

**Raggio:** (solo esperienze con annunci dinamici; facoltativo) Un raggio da un CAP degli Stati Uniti specificato nel file di feed per il target; seleziona un raggio da 0 miglia a 200 miglia. Il file di feed utilizzato per creare gli annunci dinamici per l&#39;esperienza deve includere una colonna [!UICONTROL ZIP]<!-- or a user-named column mapped to a ZIP column --> con un valore per ogni riga prodotto nel file. Ad esempio, per un raggio di 10 miglia, un annuncio per un prodotto disponibile in 95110 può essere visualizzato agli utenti entro 10 miglia da 95110 (determinato dall’indirizzo IP dell’utente).

**Pixel RT:** (solo esperienze con annunci dinamici; facoltativo) Un pixel di retargeting [!UICONTROL Creative] per il potenziale target. Quando imposti il targeting all’interno dell’albero decisionale, puoi includere un livello di nodi di destinazione di pixel RT. Per ogni nodo, specificherai il pixel di destinazione e i valori per gli attributi del pixel necessari per mostrare i creativi nei bundle creativi assegnati. Se non specifichi un pixel in questo campo, puoi comunque specificarne uno all’interno dell’albero decisionale.&lt;!— Da R: &quot;il Pixel RT dovrebbe essere tramite la selezione del contenuto nella Dynamic Ad Setup&quot; — chiarimento. Nelle impostazioni degli annunci dinamici viene visualizzato &quot;Datapass&quot; (una parola), ma non sono sicuro di come funzionino insieme questa impostazione e questo livello di esperienza. —>

**[!UICONTROL Label]:**<!-- should be "Labels" --> (facoltativo) qualsiasi etichetta specifica di [!DNL Creative] da applicare all&#39;esperienza. È possibile filtrare le esperienze per etichetta nella visualizzazione Esperienze<!-- sic -->.

* Per selezionare le etichette esistenti, fare clic su ![Giù](/help/creative/assets/chevron-down.png "Giù") e selezionare la casella di controllo accanto a ogni etichetta da applicare.

* Per cercare le etichette esistenti, inizia a immettere una stringa di testo all’interno del nome dell’etichetta.

* Per creare una nuova etichetta da applicare, aprire l&#39;elenco, fare clic su **+ Aggiungi etichetta**, immettere un nuovo nome etichetta nel campo [!UICONTROL Label] e quindi fare clic su **Crea**.

* Per rimuovere un&#39;etichetta, deselezionare la casella di controllo accanto al nome.

**[!UICONTROL Impression Tracking URL]:** (facoltativo) URL di tracciamento delle impression di terze parti da aggiungere all&#39;URL della pagina di destinazione per qualsiasi annuncio creato dall&#39;esperienza. Puoi includere fino a cinque URL. Per aggiungere un URL aggiuntivo, fai clic su ![icona](/help/creative/assets/create.png) **[!UICONTROL Add More] e immetti l&#39;URL.

Dopo aver immesso un URL, tutte le [macro disponibili](/help/creative/creative-macros.md) e i dati con cui vengono sostituite sono elencati più in basso nella pagina. Per inserire una delle macro nell&#39;URL, posizionare il cursore sulla descrizione della macro e fare clic su ![Copia negli Appunti](/help/creative/assets/copy-to-clipboard.png "Copia negli Appunti"), quindi incollare la macro nel campo URL.

>[!NOTE]
>
>* [!DNL Creative] aggiunge automaticamente i propri tag di tracciamento delle impression all&#39;URL della pagina di destinazione.
>* Puoi sovrascrivere questo URL per qualsiasi contenuto creativo nell’esperienza.
>* È inoltre possibile immettere codice di tracciamento delle impression JavaScript di terze parti nel campo [!UICONTROL Client JS]

**[!UICONTROL Click Tracking URL]:** (facoltativo) (facoltativo) un URL di tracciamento dei clic di terze parti da aggiungere all&#39;URL della pagina di destinazione. Puoi includere fino a cinque URL. Per aggiungere un URL aggiuntivo, fare clic su ![icona](/help/creative/assets/create.png) **[!UICONTROL Add More]** e immettere l&#39;URL.

Dopo aver immesso un URL, tutte le [macro disponibili](/help/creative/creative-macros.md) e i dati con cui vengono sostituite sono elencati più in basso nella pagina. Per inserire una delle macro nell&#39;URL, posizionare il cursore sulla descrizione della macro e fare clic su ![Copia negli Appunti](/help/creative/assets/copy-to-clipboard.png "Copia negli Appunti"), quindi incollare la macro nel campo URL.

>[!NOTE]
>
>* [!DNL Creative] aggiunge automaticamente i propri tag di tracciamento delle impression all&#39;URL della pagina di destinazione.
>* Puoi sovrascrivere questo URL per qualsiasi <!-- creative bundle for targeted experiences --> creativo nell&#39;esperienza.

**[!UICONTROL Client JS]:** (Facoltativo):

* (Quando l’inserzionista utilizza un fornitore di conformità OBA per gli annunci) Codice JavaScript che punta alla sovrapposizione dell’annuncio che consente agli utenti di rinunciare al targeting comportamentale online (OBA).

* Eventuale codice di tracciamento delle impression JavaScript di terze parti da aggiungere alla pagina di destinazione. **Nota:** Puoi anche immettere un URL di tracciamento delle impression di terze parti nel campo [!UICONTROL Impression Tracking URL].

>[!MORELIKETHIS]
>
>* [Crea un&#39;esperienza senza il targeting dell&#39;albero delle decisioni](experience-create-no-targeting.md)
>* [Modificare un&#39;esperienza senza il targeting dell&#39;albero delle decisioni](experience-edit-no-targeting.md)
>* [Macro disponibili per il tracciamento degli URL](/help/creative/creative-macros.md)
>* [Creare manualmente un tag annuncio per una dimensione creativa applicabile](experience-tag-create-manually.md)
>* [Assegna creatività a un tag annuncio per esperienze senza targeting](experience-tag-assign-creatives.md)
>* [Personalizza gli URL di tracciamento per un&#39;esperienza senza targeting](experience-tracking-urls-no-targeting.md)
>* [Personalizza l&#39;ottimizzazione creativa e la pianificazione per un&#39;esperienza senza targeting](experience-optimization-scheduling-no-targeting.md)
