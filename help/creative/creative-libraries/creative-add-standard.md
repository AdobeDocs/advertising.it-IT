---
title: Aggiungere creatività standard a una libreria creativa
description: Scopri come aggiungere creatività standard (non dinamica) a una libreria creativa.
feature: Creative Standard Creatives
exl-id: e6f1265b-9d05-4b3d-9dc6-300dbd9eb52d
TQID: 'https://experienceleague.adobe.com/mgUcE-E6LAIFFU8S5WrUceCQ6ZMSGF9tFkqEfnuKKSQ'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
subfeature_v2:
  - id: d06c1576-7039-4934-b256-7366e138fbb6
    internal-label: Creative Standard Creatives
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: a2a6d94329df17c332a140de428bb44fb892c97a
workflow-type: tm+mt
source-wordcount: '2018'
ht-degree: 0%
---
# Aggiungere creatività standard a una libreria creativa

Aggiungi creatività standard alle [librerie creative](creative-library-manage.md) da utilizzare con [esperienze annuncio](/help/creative/experiences/experience-about.md) standard.

>[!NOTE]
>
> Puoi includere singoli creativi direttamente all’interno di esperienze pubblicitarie che non hanno target utente definiti. Puoi anche raggruppare i tuoi creativi in [bundle](bundle-manage.md), che puoi includere nelle esperienze di annunci mirati.

## Aggiungere annunci HTML flessibili a una libreria creativa {#flexible-creative-add}

È possibile effettuare una delle seguenti operazioni:

* Carica le tue creatività flessibili nei file ZIP.

* Utilizza uno dei modelli di creatività flessibili predefiniti caricati sul tuo account come punto di partenza per la tua creatività flessibile.

### Carica le tue creatività flessibili {#flexible-creative-upload}

È possibile caricare più unità creative flessibili. Le creatività flessibili devono essere in formato ZIP e possono essere fino a 2 MB. Per i requisiti dei file, vedere la [specifica creativa di HTML5](html5-creative-specification.md).

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Fai clic sul nome della libreria.

1. Nella scheda **[!UICONTROL Creatives]**, fare clic su **[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL Flexible]**.

1. Fare clic su **[!UICONTROL Upload New]**.

1. Specificare i file ZIP in uno dei modi seguenti:

   * Trascinare i file sul dispositivo o sulla rete nella casella.

   * Fare clic su **[!UICONTROL Select a file]** per individuare i file nel dispositivo o nella rete.

   Consulta le [specifiche degli annunci flessibili](#flexible-ad-spec).

1. Aggiungi o rimuovi file creativi flessibili:

   * Per aggiungere un file, fai clic su ![Aggiungi](/help/creative/assets/create.png "Aggiungi") in alto a sinistra e individua il file sul tuo dispositivo o rete.

   * Per rimuovere un file, deselezionare la relativa casella di controllo.

1. (Facoltativo) Per visualizzare l&#39;anteprima di un contenuto creativo, fai clic su ![Anteprima](/help/creative/assets/preview.png "Anteprima") sopra l&#39;immagine.

1. Specificare le [impostazioni degli annunci flessibili di HTML5](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-flexible-html5).

   Per impostazione predefinita, vengono selezionati tutti i creativi appena caricati. Tutte le impostazioni con un solo valore vengono applicate a tutti i creativi selezionati; per alcune impostazioni è possibile specificare valori singoli. Per immettere le impostazioni per creativi specifici, deseleziona la casella di controllo accanto a ciascun creativo inapplicabile.

1. Fai clic su **[!UICONTROL Create]**

### Aggiungere creatività flessibili utilizzando un modello {#flexible-creative-use-template}

Puoi utilizzare uno qualsiasi dei modelli creativi flessibili caricati sul tuo account per creare annunci di una dimensione predefinita. Dopo aver selezionato un modello da utilizzare, è possibile modificare i tag e gli attributi dei clic.

<!--
Replace last sentence with this if we add the template download feature back:  You can either a\) select a template to use, and then edit the click tags and attributes; or b\) [download a template as a ZIP file](#download-flexible-creative-template), edit the contents offline to build your own creative, and then [upload the edited file as a new creative](flexible-creative-upload).
-->

<!--
 Not currently an option:
You can use any of the [predefined flexible creative templates](flexible-html5-templates.md) included with [!DNL Creative] to build 160x600, 300x250, 300x600, or 728x90 ads.

For information about the attributes available in predefined templates, see "[Available flexible creative templates](#flexible-creative-templates-available)."
-->

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Fai clic sul nome della libreria.

1. Nella scheda **[!UICONTROL Creatives]**, fare clic su **[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL Flexible]**.

1. Fare clic su **[!UICONTROL Browse System Flexible Templates]**.

1. (Facoltativo) Per visualizzare l&#39;anteprima del modello, fare clic su **[!UICONTROL ...]** accanto al nome del modello e quindi su **[!UICONTROL Preview]**.

   È possibile scaricare il modello: fare clic su **[!UICONTROL ...]** accanto al nome del modello, quindi fare clic su **[!UICONTROL Download]**.

1. Accanto al nome del modello, fare clic su **[!UICONTROL ...]** e quindi su **[!UICONTROL Use Selected]**.

1. Modifica le [impostazioni creative flessibili di HTML5](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-flexible-html5) per specificare la lingua e includere tag di clic, immagini e altri attributi personalizzati.

   La dimensione massima del file del contenuto creativo, una volta compresso, è di 2 MB.<!-- Still true? -->

1. Aggiungi o rimuovi i tuoi file creativi flessibili:

   * Per aggiungere un file dal dispositivo o dalla rete, fai clic su ![Aggiungi](/help/creative/assets/create.png "Aggiungi") in alto a sinistra e individua il file. Selezionare la casella di controllo accanto al contenuto creativo, deselezionare la casella di controllo accanto agli altri contenuti creativi e modificare le [impostazioni creative flessibili di HTML5](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-flexible-html5) per specificare la lingua e includere tag di clic, immagini e altri attributi personalizzati.

   * Per rimuovere un file, deselezionare la relativa casella di controllo.

1. (Facoltativo) Per visualizzare l&#39;anteprima di un contenuto creativo, fai clic su ![Anteprima](/help/creative/assets/preview.png "Anteprima") sopra l&#39;immagine.

1. Fare clic su **[!UICONTROL Create]**.

## Aggiungere un contenuto creativo display standard a una libreria creativa

I creativi display standard includono i creativi di immagini e HTML5, inclusi i creativi importati da Adobe Experience Manager e Adobe GenStudio for Performance Marketing.

* I creativi delle immagini possono essere in formato GIF, JPEG, JPG o PNG. La dimensione massima del file è di due (2) MB. Visualizza le [dimensioni creative supportate](/help/creative/creative-libraries/creative-sizes.md).

* È possibile aggiungere più risorse Experience Manager, più esperienze GenStudio o più creativi HTML5 locali di un singolo tipo (semplice o statico) alla volta. Per i creativi di HTML5, vedere la [specifica annuncio HTML5](/help/creative/creative-libraries/html5-creative-specification.md).

<!--
 Add in when we add this feature back:
You can optionally download a sample HTML5 creative as a ZIP file, edit the contents to build your own creative, and then add the edited file as a new creative.
-->

>[!NOTE]
>
>È inoltre possibile [aggiungere creativi HTML5 flessibili](#flexible-creative-add), ovvero creativi HTML5 con tutti i relativi attributi come tag HTML standard modificabili direttamente in [!DNL Creative].

### Dalla nuova interfaccia

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Facoltativo) [Personalizzare la visualizzazione](/help/creative/introduction/customize-data-views.md) per includere librerie specifiche.

1. Apri la libreria in uno dei seguenti modi:

   * Fai clic sul nome della libreria.

   * Accanto al nome della libreria, fare clic su **[!UICONTROL ...]** > **[!UICONTROL Open]**.

1. Nella scheda **[!UICONTROL Creatives]**, fare clic su **[!UICONTROL Create]** > **[!UICONTROL Upload]** > **[!UICONTROL Display]**.

1. Specifica i creativi:

   * Per le risorse immagine o HTML5 locali, effettua una delle seguenti operazioni:

     * Trascinare i file sul dispositivo o sulla rete nella casella.

     * Fare clic su **[!UICONTROL Select a file]** per individuare i file nel dispositivo o nella rete.

   * Per le immagini approvate in una [libreria Experience Manager connessa al tuo account DSP](/help/creative/creative-libraries/aem-assets-configure.md), effettua le seguenti operazioni:

     1. Fare clic su **[!UICONTROL AEM Asset Library]**.

     1. (Se non hai già effettuato l’accesso al tuo account Experience Manager) Accedi al tuo account Experience Manager.

     1. Individua e seleziona i file nelle visualizzazioni [!UICONTROL Assets] o [!UICONTROL Collections], quindi fai clic su **[!UICONTROL Select]** in alto a destra.

        <!-- If the existing asset has multiple quality options, [!DNL Creative] downloads the primary asset, or the asset with the highest resolution within some upper limit [verify what it is and how this works]. [If an asset is part of an image set, ... primary asset in the image set. -->

   * Per le esperienze GenStudio, effettua le seguenti operazioni:

     1. Fare clic su **[!UICONTROL GenStudio Library]**.

     1. (Se non hai già effettuato l&#39;accesso al tuo account GenStudio) Accedi al tuo account GenStudio.

        Le esperienze degli annunci visualizzati vengono visualizzate per impostazione predefinita. Se necessario, filtra le esperienze per campagna o altri attributi.

     1. Individua e seleziona le esperienze degli annunci di visualizzazione, quindi fai clic su **[!UICONTROL Select]** in alto a destra.

     Ogni variante creativa in un&#39;esperienza selezionata viene importata come creatività separata di HTML5.

1. Aggiungi o rimuovi creatività:

   * Per aggiungere un&#39;immagine, fai clic su ![Aggiungi](/help/creative/assets/create.png "Aggiungi") in alto a sinistra e individua il file sul tuo dispositivo o rete.

   * Per rimuovere un&#39;immagine, deselezionare la relativa casella di controllo.

1. Specificare le [impostazioni creative di HTML5](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-html5) o le [impostazioni creative per le immagini](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-image).

   Per impostazione predefinita, vengono selezionati tutti i creativi o le esperienze GenStudio che hai appena caricato e tutte le impostazioni specificate vengono applicate a tutti gli elementi selezionati. Qualsiasi impostazione con un solo valore si applica a tutti gli elementi selezionati. Per immettere le impostazioni per creativi o esperienze GenStudio specifiche, deseleziona ogni creativo o esperienza inapplicabile.

1. Fare clic su **[!UICONTROL Save Creative]**.

### Dall’interfaccia utente legacy

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Fare clic su **[!UICONTROL Switch to classic UI]**.

1. Fai clic sul nome della libreria.

1. Nella scheda **[!UICONTROL Creatives]**, fare clic su **[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL Standard Display]**.

1. Specifica i creativi:

   * Per le risorse immagine o HTML5 locali, effettua una delle seguenti operazioni:

     * Trascinare i file sul dispositivo o sulla rete nella casella.

     * Fare clic su **[!UICONTROL Select a file]** per individuare i file nel dispositivo o nella rete.

   * Per le immagini approvate in una [libreria Experience Manager connessa al tuo account DSP](/help/creative/creative-libraries/aem-assets-configure.md), effettua le seguenti operazioni:

     1. Fare clic su **[!UICONTROL AEM Asset Library]**.

     1. (Se non hai già effettuato l’accesso al tuo account Experience Manager) Accedi al tuo account Experience Manager.

     1. Individua e seleziona i file nelle visualizzazioni [!UICONTROL Assets] o [!UICONTROL Collections], quindi fai clic su **[!UICONTROL Select]** in alto a destra.

        <!-- If the existing asset has multiple quality options, [!DNL Creative] downloads the primary asset, or the asset with the highest resolution within some upper limit [verify what it is and how this works]. [If an asset is part of an image set, ... primary asset in the image set. -->

   * Per le esperienze GenStudio, effettua le seguenti operazioni:

     1. Fare clic su **[!UICONTROL GenStudio Library]**.

     1. (Se non hai già effettuato l&#39;accesso al tuo account GenStudio) Accedi al tuo account GenStudio.

        Le esperienze degli annunci visualizzati vengono visualizzate per impostazione predefinita. Se necessario, filtra le esperienze per campagna o altri attributi.

     1. Individua e seleziona le esperienze degli annunci di visualizzazione, quindi fai clic su **[!UICONTROL Select]** in alto a destra.

     Ogni variante creativa in un&#39;esperienza selezionata viene importata come creatività separata di HTML5.

1. Aggiungi o rimuovi creatività:

   * Per aggiungere un&#39;immagine, fai clic su ![Aggiungi](/help/creative/assets/create.png "Aggiungi") in alto a sinistra e individua il file sul tuo dispositivo o rete.

   * Per rimuovere un&#39;immagine, deselezionare la relativa casella di controllo.

1. Specificare le [impostazioni creative di HTML5](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-html5) o le [impostazioni creative per le immagini](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-image).

   Per impostazione predefinita, vengono selezionati tutti i creativi o le esperienze GenStudio che hai appena caricato e tutte le impostazioni specificate vengono applicate a tutti gli elementi selezionati. Qualsiasi impostazione con un solo valore si applica a tutti gli elementi selezionati. Per immettere le impostazioni per creativi o esperienze GenStudio specifiche, deseleziona ogni creativo o esperienza inapplicabile.

1. Fare clic su **[!UICONTROL Create]**.

## Aggiungere creatività di terze parti a una libreria creativa {#creative-add-third-party}

[!DNL Creative] supporta i tag degli annunci per i creativi di visualizzazione ospitati su server di annunci di terze parti. Nella nuova interfaccia utente, puoi importare una o più creatività da un foglio di traffico. L’interfaccia utente legacy supporta l’immissione di un tag per un singolo contenuto creativo.

### Dalla nuova interfaccia

#### Preparare la scheda di traffico {#third-party-sheet-requirements}

* Utilizzare un file Excel (`.xlsx` o `.xls`), CSV o TSV di dimensioni non superiori a 10 MB, con un massimo di 500 elementi creativi.

* Per i file di Excel, inserire le creatività nel primo foglio di lavoro. Viene importato solo il primo foglio di lavoro. I file protetti da password non sono supportati.

* Utilizzare un&#39;esportazione [!DNL Flashtalking] o [!DNL Google Campaign Manager 360] o preparare un foglio generico. Il foglio deve corrispondere al layout dell’ad server selezionato al momento del caricamento.

* Includi un nome creativo, una dimensione e un tag annuncio per ogni creatività. I nomi possono contenere fino a 255 caratteri. Specificare le dimensioni in una colonna di dimensione singola (ad esempio `300x250`) o in colonne di larghezza e altezza separate nelle esportazioni fornitore. Utilizza [dimensioni creative supportate](creative-sizes.md).

* Per un foglio generico, utilizzare le intestazioni di colonna `Creative Name`, `Size` e `Ad Tag`. Puoi scaricare un modello CSV dalla finestra di dialogo di caricamento. Sostituisci la riga di esempio con i tuoi dati creativi.

>[!IMPORTANT]
>
>* Il caricamento in blocco supporta solo i tag di visualizzazione. I tag Video e VAST non sono supportati.
>* Il caricamento in blocco memorizza i tag degli annunci forniti senza inserire macro di tracciamento o riscrivere gli URL di tracciamento durante l’importazione. Includi tutte le [macro di tracciamento](/help/creative/creative-macros.md) necessarie nei tag prima di caricare il foglio.

#### Caricare e rivedere i contenuti creativi {#third-party-bulk-upload}

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Apri la libreria in uno dei seguenti modi:

   * Fai clic sul nome della libreria.

   * Accanto al nome della libreria, fare clic su **[!UICONTROL ...]** > **[!UICONTROL Open]**.

1. Nella scheda **[!UICONTROL Creatives]**, fare clic su **[!UICONTROL Add new]** > **[!UICONTROL Upload]** > **[!UICONTROL 3rd Party]**.

   Viene visualizzata la finestra di dialogo **[!UICONTROL Bulk upload third-party tags]**.

1. Selezionare **[!UICONTROL Ad server]** corrispondente al foglio:

   * **[!UICONTROL Flashtalking]**

   * **[!UICONTROL Google CM360]**

   * **[!UICONTROL Generic]**

   Prima di caricare un file devi selezionare un ad server. L’ad server selezionato si applica a ogni contenuto creativo del foglio; non viene rilevato dai singoli tag.

1. (Facoltativo) Per preparare un foglio generico, fare clic su **[!UICONTROL Download CSV template]**, sostituire i dati di esempio con le proprie creative e salvare il file.

1. Specificare il foglio in uno dei modi seguenti:

   * Trascina e rilascia il file nella casella di caricamento.

   * Fare clic su **[!UICONTROL select a file]** per individuare il file nel dispositivo o nella rete.

   Il foglio viene caricato e analizzato. Se il layout non corrisponde al server di annunci selezionato, correggi il foglio o seleziona il server di annunci corrispondente e carica di nuovo il file.

1. In **[!UICONTROL Review third-party creatives]**, esaminare **[!UICONTROL Creative name]**, **[!UICONTROL Size]**, **[!UICONTROL Type]**, **[!UICONTROL Language]** e **[!UICONTROL Status]** per ogni riga.

   * Se il foglio include più formati di tag, selezionare la scheda della colonna di tag che si desidera importare. Il formato selezionato si applica a tutte le righe e non vengono visualizzate le righe senza tag in quella colonna. La modifica delle schede reimposta la selezione su tutte le righe importabili per quel formato.

   * Tutte le righe importabili sono selezionate per impostazione predefinita. Deseleziona la casella di controllo accanto ai contenuti creativi che non desideri importare.

   * (Facoltativo) Modificare **[!UICONTROL Language]** per i singoli creativi. L&#39;impostazione predefinita è Inglese.

   * Impossibile selezionare o importare righe con lo stato **[!UICONTROL Error]**. È possibile importare le righe valide oppure fare clic su **[!UICONTROL Cancel]**, correggere il foglio di origine e caricarlo nuovamente. Correggi i nomi, le dimensioni o i tag mancanti e rimuovi i tag video o qualsiasi carattere contrassegnato come non supportato.

1. Fai clic su **[!UICONTROL Importa <N> creatives &#x200B;]**, dove `<N>` è il numero di creatives selezionati. Per un singolo contenuto creativo, fare clic su **[!UICONTROL Import 1 creative]**.

   La finestra di dialogo si chiude e una notifica conferma l’avvio dell’importazione. Al termine dell’elaborazione, le creatività vengono visualizzate nella libreria.

Per tenere traccia dell&#39;importazione, fai clic su ![Gestione processi](/help/creative/assets/job-manager.png "Gestione processi") (**[!UICONTROL Job Manager]**) a destra della barra dei menu superiore. Se alcune righe non riescono durante l&#39;elaborazione, fare clic su **[!UICONTROL Download failed rows]** per il processo di importazione, correggere il foglio scaricato e caricarlo di nuovo.

### Dall’interfaccia utente legacy

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Fare clic su **[!UICONTROL Switch to classic UI]**.

1. (Facoltativo) [Personalizzare la visualizzazione](/help/creative/introduction/customize-data-views.md) per includere librerie specifiche.

1. Fai clic sul nome della libreria.

1. Nella scheda **[!UICONTROL Creatives]**, fare clic su **[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL 3rd Party]**.

1. Specifica il tag JavaScript e altre impostazioni per la creatività nelle [impostazioni creative di terze parti](#creative-settings-third-party).

   È possibile copiare e incollare le [macro disponibili](/help/creative/creative-macros.md) nel tag JavaScript.

1. Fare clic su **[!UICONTROL Create]**.

## Caricare un video creativo in una libreria creativa

Consulta le [specifiche creative per video](/help/creative/creative-libraries/creative-libraries-about.md#creative-video-specs) e le [dimensioni creative supportate](/help/creative/creative-libraries/creative-sizes.md).

### Dalla nuova interfaccia

Puoi caricare un video alla volta.

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Facoltativo) [Personalizzare la visualizzazione](/help/creative/introduction/customize-data-views.md) per includere librerie specifiche.

1. Apri la libreria in uno dei seguenti modi:

   * Fai clic sul nome della libreria.

   * Accanto al nome della libreria, fare clic su **[!UICONTROL ...]** > **[!UICONTROL Open]**.

1. Nella scheda **[!UICONTROL Creatives]**, fare clic su **[!UICONTROL Create]** > **[!UICONTROL Upload]** > **[!UICONTROL Video]**.

1. Specificare il file video in uno dei modi seguenti:

   * Trascinare e rilasciare un file sul dispositivo o sulla rete nella casella.

   * Fare clic su **[!UICONTROL Select a file]** per individuare un file nel dispositivo o nella rete.

1. Specifica le [impostazioni creative per il video](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-video).

1. Fare clic su **[!UICONTROL Save Creative]**.

### Dall’interfaccia utente legacy

1. Nel menu principale, fare clic su **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Fare clic su **[!UICONTROL Switch to classic UI]**.

1. Fai clic sul nome della libreria.

1. Nella scheda **[!UICONTROL Creatives]**, fare clic su **[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL Video]**.

1. Specificare i file video in uno dei modi seguenti:

   * Trascinare i file sul dispositivo o sulla rete nella casella.

   * Fare clic su **[!UICONTROL Select a file]** per individuare i file nel dispositivo o nella rete.

1. Specifica le [impostazioni creative per il video](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-video).

   Per impostazione predefinita, la creatività appena caricata è selezionata e tutte le impostazioni specificate vengono applicate alla creatività selezionata.<!-- By default, all creatives you just uploaded are selected, and any settings you specify apply to all selected creatives. Any settings with only one value apply to all selected creatives. To enter settings for specific creatives, deselect each inapplicable creative. -->

1. Fai clic su **[!UICONTROL Create]**

>[!MORELIKETHIS]
>
>* [Modifica creatività standard](/help/creative/creative-libraries/creative-edit-standard.md)
>* [Impostazioni creative standard](/help/creative/creative-libraries/creative-settings-standard.md)
>* [Visualizza il registro delle modifiche per un contenuto creativo](/help/creative/creative-libraries/creative-view-change-log.md)
>* [Macro disponibili per il tracciamento degli URL](/help/creative/creative-macros.md)
>* [Dimensioni creative supportate](/help/creative/creative-libraries/creative-sizes.md)
>* [Anteprima di un contenuto creativo](/help/creative/creative-libraries/creative-preview.md)
>* [Allega e scollega creativi dai bundle](/help/creative/creative-libraries/creative-attach-detach-bundles.md)
>* [Informazioni sulle librerie creative](/help/creative/creative-libraries/creative-libraries-about.md)
>* [Gestisci librerie creative](/help/creative/creative-libraries/creative-library-manage.md)
