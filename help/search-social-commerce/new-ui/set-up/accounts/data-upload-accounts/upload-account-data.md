---
title: Carica dati account offline per reporting e simulazioni
description: Scopri come caricare manualmente i dati dell’account offline o in un bucket  [!DNL Amazon] [!DNL S3] per il supporto di reporting e simulazione. I file di registro tengono traccia dell’avanzamento dei processi di caricamento.
source-git-commit: bfa5403ff66bed73797fc4c7115b8c043856745d
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 0%

---

# Carica dati account offline per reporting e simulazioni

*Inserzionisti abilitati per il caricamento dei dati dell&#39;account*

Carica il contenuto della campagna e i dati di costo, clic e conversione offline per un account senza supporto API per reporting e simulazioni delle prestazioni.

Puoi tenere traccia dell&#39;avanzamento dei processi di caricamento utilizzando la funzionalità [!UICONTROL Upload Logs]:

* Visualizza un elenco di ogni file caricato per l’account. Le informazioni su ciascun processo di caricamento file includono il nome del file, il canale di caricamento (*[!UICONTROL Cloud Storage]* o *[!UICONTROL Drag & Drop]*), la data e lo stato di sincronizzazione e i motivi per i caricamenti incompleti.

* Scarica un file con le entità account e le metriche correlate che sono state caricate per qualsiasi processo. I file sono in formato CSV (Virgola Separated Values).

## Caricare i dati dell’account manualmente

Puoi popolare un account con contenuti e costi della campagna, clic e dati di conversione caricando manualmente i dati in un file.

<!--
See "XXX" for information about supported ad networks and account structures.

[supported ad networks and campaign types](/help/search-social-commerce/introduction/supported-inventory.md)
-->

1. Nel menu principale, fare clic su **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Effettuare una delle seguenti operazioni:

   * (Dalla visualizzazione [!UICONTROL Accounts]):

      1. Selezionare la casella di controllo accanto al nome dell&#39;account, quindi fare clic su **[!UICONTROL Upload]** nella barra degli strumenti Azioni collettive.

      1. Trascinare un file nella casella o fare clic su **[!UICONTROL Browse Files]** e scegliere un file dal dispositivo o dalla rete.

      1. Fare clic su **[!UICONTROL Upload Files]**.

   * (dalle impostazioni account):

      1. Selezionare l&#39;account in uno dei modi seguenti:

         * Posizionare il cursore sul nome dell&#39;account, fare clic su **...** e quindi su **[!UICONTROL Edit]**.

         * Selezionare la casella di controllo accanto al nome dell&#39;account, quindi fare clic su **[!UICONTROL Edit]** nella barra degli strumenti Azioni collettive.

      1. Fare clic sulla scheda **[!UICONTROL Upload File]**.

      1. Trascinare un file nella casella o fare clic su **[!UICONTROL Browse Files]** e scegliere un file dal dispositivo o dalla rete.

      1. Fare clic su **[!UICONTROL Save]**.

# Carica dati account in un bucket [!DNL Amazon] [!DNL S3] {#data-upload-s3}

È possibile popolare un account con il contenuto e i costi della campagna, i clic e i dati di conversione caricando i dati in una cartella assegnata a Search, Social e Commerce in un bucket [!DNL Amazon Web Services] (AWS) [!DNL Simple Storage Service] ([!DNL S3]).

<!--
See "XXX" for information about supported ad networks and account structures.

[supported ad networks and campaign types](/help/search-social-commerce/introduction/supported-inventory.md)
-->

>[!PREREQUISITES]
>
>* Contatta il team del tuo account Adobe per abilitare il caricamento dei dati dell’account dell’inserzionista Search, Social e Commerce. Il team semplificherà la creazione di una cartella specifica dell&#39;organizzazione in un bucket [!DNL S3] e ti informerà al termine.<!-- Add more context about the bucket we'll use here or in the intro. Do we have one bucket (potentially with multiple folders) per client, or do we share them (if so, do we need to state how in docs? -->
>* Recupera il percorso di archiviazione cloud [!DNL S3], l&#39;ID della chiave di accesso e la chiave di accesso segreta per il tuo account. Gli stessi ID chiave di accesso e chiave di accesso segreta vengono utilizzati per tutti gli account <!-- naming convention?--> di caricamento dati dell&#39;organizzazione.

1. Nel menu principale, fare clic su **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Effettuare una delle seguenti operazioni:

   * (Dalla visualizzazione [!UICONTROL Accounts]):

      1. Selezionare la casella di controllo accanto al nome dell&#39;account, quindi fare clic su **[!UICONTROL Upload]** nella barra degli strumenti Azioni collettive.

      1. Nella casella [!UICONTROL Cloud Storage Link] fare clic su **[!UICONTROL Go to the Link]**.

      1. Fare clic su **[!UICONTROL Show Access Key and Secret]**.

      1. Accanto al campo [!UICONTROL Storage Link], fare clic su **[!UICONTROL Copy]** per copiare il collegamento negli Appunti e archiviarlo in un luogo sicuro.

      1. Analogamente, copiare e archiviare in modo sicuro i valori [!UICONTROL Access Key] e [!UICONTROL Secret Key].

      1. Fare clic su **[!UICONTROL Done]**.

   * (dalle impostazioni account):

      1. Selezionare l&#39;account in uno dei modi seguenti:

         * Posizionare il cursore sul nome dell&#39;account, fare clic su **...** e quindi su **[!UICONTROL Edit]**.

         * Selezionare la casella di controllo accanto al nome dell&#39;account, quindi fare clic su **[!UICONTROL Edit]** nella barra degli strumenti Azioni collettive.

      1. Fare clic sulla scheda **[!UICONTROL Upload File]**.

      1. Nella casella [!UICONTROL Cloud Storage Link] fare clic su **[!UICONTROL Go to the Link]**.

      1. Fare clic su **[!UICONTROL Show Access Key and Secret]**.

      1. Accanto al campo [!UICONTROL Storage Link], fare clic su **[!UICONTROL Copy]** per copiare il collegamento negli Appunti e archiviarlo in un luogo sicuro.

      1. Analogamente, copiare e archiviare in modo sicuro i valori [!UICONTROL Access Key] e [!UICONTROL Secret Key].

      1. Fare clic su **[!UICONTROL Done]**.

      1. Fare clic su **[!UICONTROL Save]**.

1. (Una volta per organizzazione) Configura l’ambiente AWS locale:

   1. Scaricare e installare [!DNL AWS Command Line Interface] (AWS CLI) dal seguente percorso: [https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html).

   1. Configura le credenziali di AWS:

      1. Creare un file di testo normale e denominarlo `~/.aws/credentials` (senza estensione file).

      1. Apri il file in qualsiasi editor di testo e immetti l’ID della chiave di accesso e la chiave di accesso segreta dell’organizzazione nel modo seguente:

         ```
         [default]
         aws_access_key_id = <Access key copied in Step 2>
         aws_secret_access_key = <Secret key copied in Step 2>
         ```

1. Scarica il rapporto sui dati dell’account dalla rete di annunci e salvalo.

1. In AWS CLI, eseguire il comando seguente per caricare i dati dell&#39;account nel percorso cloud [!DNL S3].

   ```
   aws s3 cp <local-report-file-location <S3-cloud-location-associated-with-your-account>
   ```

   Esempio: `aws s3 cp filename.txt s3://cloud-location/`

## Visualizza un registro dei file di dati dell’account caricati

1. Nel menu principale, fare clic su **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Posizionare il cursore sul nome dell&#39;account, fare clic su **...** e quindi su **[!UICONTROL Upload Logs]**.

1. (Facoltativo) Per scaricare i dati di un file caricato, fai clic su ![Scarica](/help/search-social-commerce/assets/download.png "Scarica") nella colonna [!UICONTROL Download] e scarica il file in base alla normale procedura del browser.

## Dati richiesti

I dati devono rispettare i requisiti di dati per la rete di annunci. I campi dati per ogni entità possono variare in base alla rete di annunci.
