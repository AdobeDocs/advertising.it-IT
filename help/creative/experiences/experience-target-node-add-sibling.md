---
title: Aggiungere un nodo di destinazione di pari livello tra i nodi di un’esperienza
description: Scopri come aggiungere un nodo di pari livello a qualsiasi nodo che ha una destinazione o si trova allo stesso livello di un nodo con una destinazione.
feature: Creative Experiences
exl-id: 915fd399-1c55-49af-94ed-cf49a4154a53
TQID: 'https://experienceleague.adobe.com/fRdbFmlTUBzHHkmrfonZ0COJ7-1x6t2HRczwlcVb99o'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
subfeature_v2:
  - id: f1a0ef49-c5d6-4fdf-b0dc-ae6685afe30b
    internal-label: Creative experiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 8a75f4a164b25ed8e73816c3d853d9650f470118
workflow-type: tm+mt
source-wordcount: '1151'
ht-degree: 0%
---
# Aggiungere un nodo di destinazione di pari livello tra i nodi di un’esperienza

*Esperienze con targeting solo per la struttura decisionale*

È possibile aggiungere un nodo di pari livello a qualsiasi nodo che ha una destinazione o si trova allo stesso livello di un nodo con una destinazione.

## Utilizzo dell’editor basato sull’intelligenza artificiale (Beta) {#ai-editor}

Durante la [creazione](experience-create-targeting.md#ai-editor) o la [modifica](experience-edit-targeting.md#ai-editor) dell&#39;esperienza, puoi descrivere la nuova destinazione di pari livello all&#39;agente di intelligenza artificiale. Identifica il ramo padre e i valori di destinazione, quindi rivedi il risultato. Per aggiungere il pari livello direttamente nell’area di lavoro:

1. Posizionare il cursore sul padre dei nodi nel livello in cui si desidera creare un altro elemento di pari livello e fare clic su **[!UICONTROL +]**.

   La categoria di destinazione è determinata dal livello esistente e il selettore di valori viene aperto per tale categoria.

1. Specifica i valori target per la categoria:

   * Per i target di pubblico:

     * Per aggiungere il primo segmento, individua e seleziona il segmento di pubblico.

     * Per aggiungere segmenti a un gruppo di segmenti esistente:

       1. Seleziona il gruppo di segmenti.

       1. (Facoltativo) Modificare la logica del gruppo in **[!UICONTROL Include Any]**, **[!UICONTROL Include All]** o **[!UICONTROL Exclude All]**, in base alle esigenze.

          **[!UICONTROL Include Any]** corrisponde agli utenti in almeno un segmento selezionato; **[!UICONTROL Include All]** richiede l&#39;appartenenza in tutti i segmenti selezionati.

          **[!UICONTROL Exclude All]** non è disponibile per il primo gruppo di segmenti. Per un pubblico che include solo esclusioni, crea il pubblico utilizzando **[!UICONTROL Include Any]**, quindi escludilo quando lo aggiungi a un posizionamento all&#39;interno del DSP.

       1. Individua e seleziona i segmenti aggiuntivi.

     * Per aggiungere un nuovo gruppo di segmenti:

       1. Aggiungi un gruppo.

       1. (Facoltativo) Modificare la logica tra il gruppo precedente e il nuovo gruppo in **[!UICONTROL And]** o **[!UICONTROL Or]**, in base alle esigenze.

          **[!UICONTROL And]** richiede che gli utenti soddisfino le condizioni di entrambi i gruppi; **[!UICONTROL Or]** richiede che soddisfino almeno le condizioni di un gruppo.

       1. Individua e seleziona i segmenti per il nuovo gruppo.

       1. (Facoltativo) Modificare la logica del gruppo in **[!UICONTROL Include Any]**, **[!UICONTROL Include All]** o **[!UICONTROL Exclude All]**, in base alle esigenze.

   * Per gli obiettivi geografici:

     * Seleziona le posizioni all’interno della categoria geografica al livello esistente, ad esempio paesi, regioni o città.

     * Per gli oggetti di codice postale, seleziona il paese e inserisci i codici postali da includere. Per inserire più codici postali in blocco, separali con virgole o inseriscili in una riga separata.

   * Per le destinazioni di passaggio dati, immetti la chiave e il valore da rilevare.

     La chiave predefinita del passaggio dati è configurata nel campo **[!UICONTROL Data Pass]** nella sezione **[!UICONTROL Advanced]** delle [impostazioni generali dell&#39;esperienza](experience-settings-targeting.md). Se necessario, personalizza la chiave per la destinazione.

   * Per il retargeting delle destinazioni di pixel, seleziona il pixel di retargeting e specifica i valori per gli attributi di pixel necessari per mostrare le creatività.

     Gli attributi disponibili sono configurati nelle [impostazioni pixel di retargeting](/help/creative/pixels/retargeting-pixel-manage.md).

   * Per i dispositivi di destinazione, seleziona i valori all’interno della categoria di dispositivi al livello esistente: tipi di dispositivi, sistemi operativi o browser.

1. (Se disponibile; facoltativo) Seleziona **[!UICONTROL Split Nodes]** per creare un nodo di destinazione separato per ogni valore selezionato, con le proprie assegnazioni del bundle creativo. In caso contrario, i valori selezionati vengono raggruppati in un nodo di destinazione.

1. Fare clic su **[!UICONTROL Add Node]**.

1. (Facoltativo) Per rinominare il nuovo nodo, fare clic su **[!UICONTROL ...]** > **[!UICONTROL Edit Name]**, immettere **[!UICONTROL Node Name]**, quindi fare clic su **[!UICONTROL Save]**.

1. [Assegna bundle creativi](experience-assign-creative-bundles.md#ai-editor) se il nuovo nodo è un nodo finale, quindi [salva l&#39;esperienza](#save).

## Utilizzo dell’editor manuale {#manual-editor}

[Aprire l&#39;editor manuale](experience-edit-targeting.md#experience-open) prima di eseguire la procedura seguente.

1. Sopra il nodo a cui si desidera aggiungere il nodo di pari livello, fare clic su ![Aggiungi](/help/creative/assets/add.png "Aggiungi"), quindi selezionare **[!UICONTROL Insert Sibling Target]**.

1. Specifica i valori target per la categoria:

   * Per i target di pubblico:

     1. Fare clic su **[!UICONTROL Click to Browse]** per aprire le opzioni **[!UICONTROL Audience Targeting]**.

     1. Configura i segmenti e i gruppi di pubblico:

        * Per aggiungere il primo segmento, individualo nel pannello a sinistra e seleziona la casella di controllo accanto al nome del segmento.

        * Per aggiungere segmenti a un gruppo di segmenti esistente:

          1. Fai clic sul gruppo di segmenti nel pannello di destra.

          1. (Facoltativo) Modificare la logica del gruppo in **[!UICONTROL Include Any]**, **[!UICONTROL Include All]** o **[!UICONTROL Exclude All]**, in base alle esigenze.

             **[!UICONTROL Include Any]** corrisponde agli utenti in almeno un segmento selezionato; **[!UICONTROL Include All]** richiede l&#39;appartenenza in tutti i segmenti selezionati.

             **[!UICONTROL Exclude All]** non è disponibile per il primo gruppo di segmenti. Per un pubblico che include solo esclusioni, crea il pubblico utilizzando **[!UICONTROL Include Any]**, quindi escludilo quando lo aggiungi a un posizionamento all&#39;interno del DSP.

          1. Individua il nuovo segmento nel pannello a sinistra e seleziona la casella di controllo accanto al nome del segmento. Ripeti per ogni segmento aggiuntivo.

             Il gruppo di segmenti viene aggiornato automaticamente con i nuovi segmenti.

        * Per aggiungere un nuovo gruppo di segmenti:

          1. Fai clic su **[!UICONTROL + New Group]** nel pannello di destra.

          1. (Facoltativo) Modificare la logica tra il gruppo precedente e il nuovo gruppo in **[!UICONTROL And]** o **[!UICONTROL Or]**, in base alle esigenze.

             **[!UICONTROL And]** richiede che gli utenti soddisfino le condizioni di entrambi i gruppi; **[!UICONTROL Or]** richiede che soddisfino almeno le condizioni di un gruppo.

          1. Individuate i segmenti per il nuovo gruppo nel pannello a sinistra e selezionate le caselle di controllo accanto ai nomi dei segmenti.

          1. (Facoltativo) Modificare la logica del gruppo in **[!UICONTROL Include Any]**, **[!UICONTROL Include All]** o **[!UICONTROL Exclude All]**, in base alle esigenze.

     1. Fare clic su **[!UICONTROL Create]**.

     1. Fare clic su **[!UICONTROL Apply]**.

   * Per i target geografici, effettuare le seguenti operazioni:

     1. Fare clic su **[!UICONTROL Click to Browse]** per aprire le opzioni [!UICONTROL Geo Targeting], specificare una o più destinazioni geografiche e quindi fare clic su **[!UICONTROL Save]**.

        Le destinazioni di codici postali dispongono di opzioni di modifica in blocco. Per incollare più codici postali, fare clic sulla scheda **[!UICONTROL Paste postal codes]**, selezionare il paese, incollare o immettere codici postali separati da virgole o su righe separate, quindi fare clic su **[!UICONTROL Include All]**. Per rimuovere una destinazione di CAP inclusa, posizionare il cursore sulla destinazione e fare clic su ![Rimuovi](/help/creative/assets/delete.png "Rimuovi") **[!UICONTROL Remove]**.

     1. (Facoltativo) Per creare più nodi di destinazione quando sono specificate più destinazioni geografiche, selezionare **[!UICONTROL Split targets to create nodes]**.

        Questa funzione crea un nodo di destinazione separato (con bundle creativi separati) per ogni destinazione geografica specificata. Se non si dividono le destinazioni, l&#39;utente deve appartenere a tutte le posizioni specificate (un&#39;istruzione [!DNL Boolean] `AND`).

     1. Fare clic su **[!UICONTROL Apply]**.

   * Per gli oggetti passaggio dati, personalizzare facoltativamente la chiave passaggio dati, immettere un singolo valore passaggio dati e quindi fare clic su **[!UICONTROL Apply]**.

     La chiave predefinita del passaggio dati è configurata nel campo **[!UICONTROL Data Pass]** nella sezione **[!UICONTROL Advanced]** delle [impostazioni generali dell&#39;esperienza](experience-settings-targeting.md). Se necessario, personalizza la chiave per la destinazione.

   * Per il retargeting delle destinazioni pixel, seleziona il pixel di retargeting da utilizzare e i valori richiesti per qualsiasi attributo del pixel che deve essere presente per mostrare le creatività. Quindi fare clic su **[!UICONTROL Apply]**.

     Gli attributi disponibili sono configurati nelle [impostazioni pixel di retargeting](/help/creative/pixels/retargeting-pixel-manage.md).

   * Per i dispositivi di destinazione, effettuare le seguenti operazioni:

     1. Seleziona le destinazioni.

     1. (Facoltativo) Per creare più nodi di destinazione quando sono specificate più destinazioni geografiche, selezionare **[!UICONTROL Split targets to create nodes]**.

        Questa funzione crea un nodo di destinazione separato (con bundle creativi separati) per ogni destinazione geografica specificata. Se non si dividono le destinazioni, l&#39;utente deve appartenere a tutte le posizioni specificate (un&#39;istruzione [!DNL Boolean] `AND`).

     1. Fare clic su **[!UICONTROL Apply]**.

1. (Facoltativo) Specifica un nome di ramo personalizzato per un ramo definito dall&#39;utente.

   Per impostazione predefinita, i rami definiti dall’utente sono etichettati con le destinazioni applicate.

   Non puoi creare un nome di ramo personalizzato per un ramo &quot;Tutti&quot; o &quot;Tutti gli altri&quot;.

   1. Tenere premuto il cursore sul nodo di destinazione e fare clic su **[!UICONTROL ...]** > **[!UICONTROL Edit Name]**.

   1. Immettere **[!UICONTROL Node Name]**, quindi fare clic su **[!UICONTROL Save]**.

1. (Facoltativo) [Assegna bundle creativi](experience-assign-creative-bundles.md#manual-editor) al nuovo nodo di destinazione.

## Salvare l’esperienza {#save}

I seguenti passaggi si applicano a entrambi gli editor.

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [Aggiungere un nodo di destinazione al livello finale](experience-target-node-add-final.md)
>* [Inserire un nodo di destinazione tra i nodi](experience-target-node-add-inner.md)
>* [Copia nodi figlio e creativi in un altro nodo allo stesso livello](experience-target-node-copy.md)
>* [Assegna creatività a un nodo finale](experience-assign-creative-bundles.md)
>* [Eliminare un nodo di destinazione o un nodo foglia creativo](/help/creative/experiences/experience-target-node-delete.md)
>* [Crea un&#39;esperienza con il targeting dell&#39;albero delle decisioni](experience-create-targeting.md)
>* [Modifica un&#39;esperienza con il targeting dell&#39;albero delle decisioni](experience-edit-targeting.md)
>* [Impostazioni esperienza di destinazione](experience-settings-targeting.md)
