---
title: Flusso di lavoro per l'utilizzo dell'integrazione DSP con [!DNL Tealium]
description: Scopri come consentire all’DSP di acquisire [!DNL Tealium] segmenti di prime parti.
feature: DSP Audiences
exl-id: 100abbe7-e228-4eb6-a5b9-bf74e83b3aa2
source-git-commit: b94541bf8675d535b2f19b26c05235eb56bc6c0b
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 0%

---

# Flusso di lavoro per l&#39;utilizzo dell&#39;integrazione DSP con [!DNL Tealium]

Puoi condividere i dati di prime parti della tua organizzazione da [!DNL Tealium] customer data platform utilizzando [!DNL Amazon Web Services] (AWS) connettore per il tubo di alimentazione. Ci sono quattro passaggi per condividere i dati da Tealium con l&#39;DSP:

1. [Creare un’origine di pubblico in DSP](#source-create).

1. [Preparare e condividere i dati di mappatura dei segmenti](#map-data).

1. [Creare connettori in [!DNL Tealium] per condividere i dati dei segmenti](#tealium-connector).

1. [Duplica il connettore esistente in [!DNL Tealium] per continuare a condividere i segmenti](#duplicate-connector).

## Passaggio 1: creare un’origine di pubblico nell’DSP {#source-create}

* [Creare un’origine di pubblico](source-create.md) per importare tipi di pubblico sul tuo account DSP o su un account inserzionista e condividere la chiave del codice sorgente con [!DNL Tealium] utente.

## Passaggio 2: preparare e condividere i dati di mappatura dei segmenti {#map-data}

1. L’inserzionista deve preparare e condividere i dati di mappatura dei segmenti:

   1. L&#39;inserzionista deve preparare i dati entro [!DNL Tealium]:

      1. L&#39;hashing degli ID e-mail per il pubblico dell&#39;inserzionista deve essere eseguito utilizzando l&#39;algoritmo SHA-256.

      1. La colonna contenente gli ID e-mail con hash deve essere mappata sull&#39;attributo del tipo di ID visitatore.

      1. Il pubblico deve essere creato con `Tealium_visitor_id` attributo. Per attivare il pubblico deve essere applicato il giusto arricchimento. Consulta la [[!DNL Tealium] documentazione sugli attributi ID visitatore](https://docs.tealium.com/server-side/visitor-stitching/visitor-id-attribute/).

   1. L’inserzionista deve fornire i dati di mappatura dei segmenti all’Account Team Adobe per creare i segmenti nell’DSP. Utilizza i seguenti nomi e valori di colonna in un file di valori separati da virgola:

      * **Chiave segmento esterna:** Il tasto del segmento esterno, che verrà successivamente specificato nelle impostazioni delle azioni per il connettore in [!DNL Tealium]. La convenzione di denominazione consigliata è &quot;`<DSP source key>_<Tealium segment name>`,&quot; ad esempio &quot;57bf424dc10_coffee-drink&quot;.

      * **Nome segmento:** Il nome del segmento.

      * **Descrizione segmento:** Lo scopo o la regola del segmento, o entrambi.

      * **ID principale:** Mantieni vuoto

      * **Video CPM:** 0

      * **Visualizza CPM:** 0

      * **Finestra segmento:** Il time-to-live del segmento.

## Passaggio 3: creare i connettori in [!DNL Tealium] per condividere i dati dei segmenti {#tealium-connector}

Per ogni segmento che desideri condividere, crea un connettore separato per ogni azione che attiva le modifiche ai dati. Ad esempio, per condividere due segmenti ciascuno con due trigger, crea quattro connettori.

1. Il team dell’account di Adobe fornisce all’inserzionista le credenziali del connettore del firewall di AWS.

1. In entrata [!DNL Tealium], [aggiungi un connettore](https://docs.tealium.com/server-side/connectors/add/), utilizzando le opzioni seguenti:

   1. Seleziona la [!DNL AWS Firehose] connettore.

   1. Nelle impostazioni di origine:

      1. Seleziona il segmento di pubblico da condividere.

      1. Configurare un trigger:

         * Per il primo connettore per il segmento, seleziona il trigger `Joined Audience`. In questo modo i dati vengono condivisi con l’DSP ogni volta che un utente si unisce a un segmento.

         * Per il secondo connettore per il segmento, seleziona il trigger `Left Audience`. Questo connettore viene utilizzato per gestire tutte le rinunce e gli utenti che lasciano il segmento nell’DSP.

   1. Nelle impostazioni di configurazione, specifica il connettore del firewall AWS. Se non è ancora stato aggiunto il connettore per DSP, aggiungere un connettore utilizzando le seguenti informazioni:

      * **Nome:** Nome del connettore.

      * **Chiave di accesso:** La chiave di accesso fornita dal team dell’account Adobe.

      * **Chiave segreta:** Chiave segreta fornita dal team dell’account Adobe.

      * **Regione:** Stati Uniti orientali, Virginia settentrionale (us-east-1)

   1. Nelle impostazioni delle azioni, eseguire le operazioni seguenti:

      1. Crea un’azione &quot;Send Customer Data to Delivery Stream (Advanced)&quot; per aggiungere dati al segmento, utilizzando le seguenti informazioni:

         * **Nome azione:** Nome dell’azione.

         * **Tipo azione:** Invia dati del cliente al flusso di consegna (avanzato)

         * **Flusso di consegna:** Tealium_CDP_Connector

         * **Dati messaggio:**  Effettua le seguenti operazioni:

            1. Scegli un attributo per il segmento:

               * Per l’attributo Hashed_Email, assegna un nome al messaggio personalizzato `hashed_email`.

               * Per l’attributo Cookies, assegna un nome al messaggio personalizzato `cookies`.

            1. Nell&#39;opzione per la creazione di un campo personalizzato, nel [!DNL Source Key] , immettere il [!UICONTROL External Segment Key] incluso nei dati di mappatura dei segmenti in [Passaggio 2](#map-data).

               L’DSP utilizzerà questa chiave per popolare il segmento.

            1. (Consigliato) Crea un’azione di aggiornamento per mantenere fresco il segmento.

## Passaggio 4: duplicare il connettore esistente in [!DNL Tealium] per continuare a condividere i segmenti {#duplicate-connector}

Puoi avere un solo connettore per segmento e un solo segmento per connettore.

1. In entrata [!DNL Tealium], duplica il segmento per il quale vuoi creare un altro segmento e rinomina il nuovo segmento.

1. In entrata [!DNL Tealium], duplica il connettore creato in [Passaggio 3](#tealium-connector), e rinomina il nuovo connettore da &quot;`<original name>-copy`&quot; al nuovo nome del segmento.

>[!MORELIKETHIS]
>
>* [Informazioni sull’attivazione di segmenti autenticati da origini pubblico](/help/dsp/audiences/sources/source-about.md)
>* [Creare un’origine di pubblico per attivare tipi di pubblico di prime parti](source-create.md)
>* [Impostazioni origine pubblico](source-settings.md)
>* [Flusso di lavoro per l&#39;utilizzo dell&#39;integrazione DSP con [!DNL Adobe Real-Time CDP]](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Informazioni su Gestione dell&#39;audience](/help/dsp/audiences/audience-about.md)
