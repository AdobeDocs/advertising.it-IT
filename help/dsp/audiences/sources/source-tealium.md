---
title: Converti ID utente da [!DNL Tealium] agli ID universali
description: Scopri come consentire all’DSP di acquisire [!DNL Tealium] segmenti di prime parti.
feature: DSP Audiences
exl-id: 100abbe7-e228-4eb6-a5b9-bf74e83b3aa2
source-git-commit: 2d045640b5bdf8dfba70d0f7da3ac012fd86e82e
workflow-type: tm+mt
source-wordcount: '1098'
ht-degree: 0%

---

# Converti ID utente da [!DNL Tealium] agli ID universali

*Funzione beta*

Utilizzare l’integrazione DSP con [!DNL Tealium] customer data platform per convertire gli indirizzi e-mail con hash di prime parti della tua organizzazione in ID universali per annunci pubblicitari mirati. Il processo utilizza [!DNL Amazon Web Services] (AWS) connettore per il tubo di alimentazione. Per condividere i dati da Tealium con l’DSP, segui la procedura riportata di seguito:

1. (Per convertire gli indirizzi e-mail in [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; inserzionisti con [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Configura il tracciamento per abilitare [!DNL Analytics] misurazione](#analytics-tracking).

1. [Creare un’origine di pubblico in DSP](#source-create).

1. [Preparare e condividere i dati di mappatura dei segmenti](#map-data).

1. [Creare connettori in [!DNL Tealium] per condividere i dati dei segmenti](#tealium-connector).

1. [Duplica il connettore esistente in [!DNL Tealium] per continuare a condividere i segmenti](#duplicate-connector).

1. [Confrontare il numero di ID universali con il numero di indirizzi e-mail con hash](#compare-id-count).

## Passaggio 1: configurare il tracciamento per [!DNL Analytics] misurazione {#analytics-tracking}

*Inserzionisti con [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

Per convertire gli indirizzi e-mail in [!DNL RampIDs] o [!DNL ID5] ID, devi effettuare le seguenti operazioni:

1. (Se non lo hai già fatto) Completa tutto [prerequisiti per l&#39;implementazione [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) e assicurarsi che il [AMO ID e EF ID](/help/integrations/analytics/ids.md) vengono inseriti negli URL di tracciamento.

1. Registrati con il partner ID universale e implementa sulle tue pagine web un codice ID universale che corrisponda alle conversioni dagli ID sui browser Web per desktop e dispositivi mobili (ma non sulle app mobili) ai view-through:

   * **Per [!DNL RampIDs]:** Devi distribuire un tag JavaScript aggiuntivo sulle pagine web per far corrispondere le conversioni dagli ID sui browser web desktop e mobili (ma non sulle app mobili) alle view-through. Contatta il tuo Account Team di Adobi, che ti fornirà le istruzioni per registrarti a un [!DNL LiveRamp] [!DNL LaunchPad] tag da [!DNL LiveRamp] Soluzioni per il traffico di autenticazione. La registrazione è gratuita, ma è necessario firmare un accordo. Dopo la registrazione, il team dell’account Adobe genererà e fornirà un tag univoco per l’organizzazione da implementare sulle pagine web.

## Passaggio 2: creare un’origine di pubblico nell’DSP {#source-create}

1. [Creare un’origine di pubblico](source-manage.md) per importare tipi di pubblico sul tuo account DSP o su un account inserzionista. Puoi scegliere di convertire gli identificatori utente in uno qualsiasi dei [formati ID universali disponibili](source-about.md).

   Le impostazioni di origine includono una chiave di origine generata automaticamente, che utilizzerai per preparare i dati di mappatura dei segmenti.

1. Dopo aver creato l&#39;origine del pubblico, condividi la chiave del codice sorgente con [!DNL Tealium] utente.

## Passaggio 3: preparare e condividere i dati di mappatura dei segmenti {#map-data}

L’inserzionista deve preparare e condividere i dati di mappatura dei segmenti.

1. L&#39;inserzionista deve preparare i dati entro [!DNL Tealium]:

   1. Effettua l&#39;hashing degli ID e-mail per il pubblico dell&#39;inserzionista utilizzando l&#39;algoritmo SHA-256.

   1. Mappa la colonna contenente gli ID e-mail con hash all’attributo del tipo di ID visitatore.

   1. Creare il pubblico con `Tealium_visitor_id` attributo. Applica il giusto arricchimento per attivare il pubblico. Consulta la [[!DNL Tealium] documentazione sugli attributi ID visitatore](https://docs.tealium.com/server-side/visitor-stitching/visitor-id-attribute/).

1. L’inserzionista deve fornire i dati di mappatura dei segmenti all’Account Team Adobe per creare i segmenti nell’DSP. Utilizza i seguenti nomi e valori di colonna in un file di valori separati da virgola:

   * **Chiave segmento esterna:** Il tasto del segmento esterno, che verrà successivamente specificato nelle impostazioni delle azioni per il connettore in [!DNL Tealium]. La convenzione di denominazione consigliata è &quot;`<DSP source key>_<Tealium segment name>`,&quot; ad esempio &quot;57bf424dc10_coffee-drink&quot;. Per il codice sorgente dell’DSP, utilizza [!UICONTROL Source Key] dalle impostazioni di origine del pubblico dell’DSP.

   * **Nome segmento:** Il nome del segmento.

   * **Descrizione segmento:** Lo scopo o la regola del segmento, o entrambi.

   * **ID principale:** Mantieni vuoto

   * **Video CPM:** 0

   * **Visualizza CPM:** 0

   * **Finestra segmento:** Il time-to-live del segmento.

## Passaggio 4: creare i connettori in [!DNL Tealium] per condividere i dati dei segmenti {#tealium-connector}

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

            1. Nell&#39;opzione per la creazione di un campo personalizzato, nel [!DNL Source Key] , immettere il [!UICONTROL External Segment Key] incluso nel [dati di mappatura dei segmenti](#map-data) nella procedura precedente.

               L’DSP utilizzerà questa chiave per popolare il segmento.

            1. (Consigliato) Crea un’azione di aggiornamento per mantenere fresco il segmento.

## Passaggio 5: duplicare il connettore esistente in [!DNL Tealium] per continuare a condividere i segmenti {#duplicate-connector}

Puoi avere un solo connettore per segmento e un solo segmento per connettore.

1. In entrata [!DNL Tealium], duplica il segmento per il quale vuoi creare un altro segmento e rinomina il nuovo segmento.

1. In entrata [!DNL Tealium], duplicato [il connettore creato](#tealium-connector) nella procedura precedente e rinominare il nuovo connettore da &quot;`<original name>-copy`&quot; al nuovo nome del segmento.

## Passaggio 6: confrontare il numero di ID universali con il numero di indirizzi e-mail con hash {#compare-id-count}

Dopo aver completato tutti i passaggi, i segmenti devono essere disponibili nell’DSP entro 24 ore. Verifica nella libreria del pubblico (disponibile quando crei o modifichi un pubblico da ) [!UICONTROL Audiences] > [!UICONTROL All Audiences] o nelle impostazioni di posizionamento) che il segmento viene popolato entro 24 ore. Confronta il numero di ID universali con il numero di indirizzi e-mail con hash originali.

Il tasso di conversione degli indirizzi e-mail con hash in ID universali deve essere superiore al 90%. Ad esempio, se invii 100 indirizzi e-mail con hash dalla piattaforma dati del cliente, questi devono essere tradotti in più di 90 ID universali. Un tasso di traduzione pari o inferiore al 90% è un problema. Per ulteriori informazioni sulle possibili variazioni dei conteggi dei segmenti, consulta la sezione &quot;[Cause delle varianze di dati tra ID e-mail e ID universali](#universal-ids-data-variances).&quot;

I segmenti vengono aggiornati ogni 24 ore. Tuttavia, l’inclusione in un segmento scade dopo 30 giorni per garantire la conformità in materia di privacy, in modo da aggiornare i tipi di pubblico inviandoli nuovamente da [!DNL Tealium] ogni 30 giorni o meno.

Per assistenza nella risoluzione dei problemi, contatta il team del tuo account di Adobe oppure `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Informazioni sulle origini del pubblico di prime parti](/help/dsp/audiences/sources/source-about.md)
>* [Gestire le origini del pubblico per attivare i tipi di pubblico con ID universale](source-manage.md)
>* [Supporto per l’attivazione di ID universali](/help/dsp/audiences/universal-ids.md)
>* [Informazioni su Gestione dell&#39;audience](/help/dsp/audiences/audience-about.md)
