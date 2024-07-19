---
title: Converti ID utente da [!DNL Tealium] a ID universali
description: Scopri come consentire all’DSP di acquisire i  [!DNL Tealium]  segmenti di prime parti.
feature: DSP Audiences
exl-id: 100abbe7-e228-4eb6-a5b9-bf74e83b3aa2
source-git-commit: 91b08bf54f067666c9c27949ff740639738887d0
workflow-type: tm+mt
source-wordcount: '1092'
ht-degree: 0%

---

# Converti ID utente da [!DNL Tealium] in ID universali

*funzionalità Beta*

Utilizza l&#39;integrazione DSP con la piattaforma dati cliente [!DNL Tealium] per convertire gli indirizzi e-mail con hash di prime parti della tua organizzazione in ID universali per pubblicità mirata. Il processo utilizza il connettore firewall [!DNL Amazon Web Services] (AWS). Per condividere i dati da Tealium con l’DSP, segui la procedura riportata di seguito:

1. (Per convertire gli indirizzi e-mail in [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; inserzionisti con [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Configura il tracciamento per abilitare [!DNL Analytics] la misurazione](#analytics-tracking).

1. [Crea un&#39;origine pubblico in DSP](#source-create).

1. [Preparare e condividere i dati di mappatura dei segmenti](#map-data).

1. [Crea connettori in [!DNL Tealium] per condividere i dati dei segmenti](#tealium-connector).

1. [Duplica il connettore esistente in [!DNL Tealium] per continuare a condividere i segmenti](#duplicate-connector).

1. [Confrontare il numero di ID universali con il numero di indirizzi e-mail con hash](#compare-id-count).

## Passaggio 1: configurare il tracciamento per la misurazione [!DNL Analytics] {#analytics-tracking}

*Inserzionisti con [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

Per convertire gli indirizzi e-mail in [!DNL RampIDs] o [!DNL ID5] ID, è necessario effettuare le seguenti operazioni:

1. (Se non lo hai già fatto) Completa tutti i [prerequisiti per l&#39;implementazione [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) e assicurati che [AMO ID e EF ID](/help/integrations/analytics/ids.md) siano inseriti negli URL di tracciamento.

1. Registrati con il partner ID universale e implementa sulle tue pagine web un codice ID universale che corrisponda alle conversioni dagli ID sui browser Web per desktop e dispositivi mobili (ma non sulle app mobili) ai view-through:

   * **Per [!DNL RampIDs]:** è necessario distribuire un tag JavaScript aggiuntivo nelle pagine Web per far corrispondere le conversioni dagli ID nei browser Web desktop e mobile (ma non nelle app mobili) alle view-through. Contatta il team dell&#39;account Adobe, che ti fornirà le istruzioni per registrarti a un tag [!DNL LiveRamp] [!DNL LaunchPad] da [!DNL LiveRamp] soluzioni traffico autenticazione. La registrazione è gratuita, ma è necessario firmare un accordo. Dopo la registrazione, il team dell’account Adobe genererà e fornirà un tag univoco per l’organizzazione da implementare sulle pagine web.

## Passaggio 2: creare un’origine di pubblico nell’DSP {#source-create}

1. [Crea un&#39;origine di pubblico](source-manage.md) per importare i tipi di pubblico nel tuo account DSP o in un account inserzionista. Puoi scegliere di convertire gli identificatori utente in uno qualsiasi dei [formati ID universali disponibili](source-about.md).

   Le impostazioni di origine includono una chiave di origine generata automaticamente, che utilizzerai per preparare i dati di mappatura dei segmenti.

1. Dopo aver creato l&#39;origine del pubblico, condividere la chiave del codice sorgente con l&#39;utente [!DNL Tealium].

## Passaggio 3: preparare e condividere i dati di mappatura dei segmenti {#map-data}

L’inserzionista deve preparare e condividere i dati di mappatura dei segmenti.

1. L&#39;inserzionista deve preparare i dati entro [!DNL Tealium]:

   1. Effettua l&#39;hashing degli ID e-mail per il pubblico dell&#39;inserzionista utilizzando l&#39;algoritmo SHA-256.

   1. Mappa la colonna contenente gli ID e-mail con hash all’attributo del tipo di ID visitatore.

   1. Crea il pubblico con l&#39;attributo `Tealium_visitor_id`. Applica il giusto arricchimento per attivare il pubblico. Consulta la [[!DNL Tealium] documentazione sugli attributi dell&#39;ID visitatore](https://docs.tealium.com/server-side/visitor-stitching/visitor-id-attribute/).

1. L’inserzionista deve fornire i dati di mappatura dei segmenti all’Account Team Adobe per creare i segmenti nell’DSP. Utilizza i seguenti nomi e valori di colonna in un file di valori separati da virgola:

   * **Chiave segmento esterna:** Chiave segmento esterna, che verrà specificata in seguito nelle impostazioni azione per il connettore in [!DNL Tealium]. La convenzione di denominazione consigliata è &quot;`<DSP source key>_<Tealium segment name>`&quot;, ad esempio &quot;57bf424dc10_coffee-drink.&quot; Per la chiave di origine DSP, utilizzare [!UICONTROL Source Key] dalle impostazioni di origine del pubblico DSP.

   * **Nome segmento:** Nome segmento.

   * **Descrizione segmento:** lo scopo o la regola del segmento o entrambi.

   * **ID padre:** Mantieni vuoto

   * **Video CPM:** 0

   * **Visualizza CPM:** 0

   * **Finestra del segmento:** Il time-to-live del segmento.

## Passaggio 4: creare connettori in [!DNL Tealium] per condividere i dati dei segmenti {#tealium-connector}

Per ogni segmento che desideri condividere, crea un connettore separato per ogni azione che attiva le modifiche ai dati. Ad esempio, per condividere due segmenti ciascuno con due trigger, crea quattro connettori.

1. Il team dell’account di Adobe fornisce all’inserzionista le credenziali del connettore del firewall di AWS.

1. In [!DNL Tealium], [aggiungere un connettore](https://docs.tealium.com/server-side/connectors/add/), utilizzando le opzioni seguenti:

   1. Selezionare il connettore [!DNL AWS Firehose].

   1. Nelle impostazioni di origine:

      1. Seleziona il segmento di pubblico da condividere.

      1. Configurare un trigger:

         * Per il primo connettore per il segmento, selezionare il trigger `Joined Audience`. In questo modo i dati vengono condivisi con l’DSP ogni volta che un utente si unisce a un segmento.

         * Per il secondo connettore per il segmento, selezionare il trigger `Left Audience`. Questo connettore viene utilizzato per gestire tutte le rinunce e gli utenti che lasciano il segmento nell’DSP.

   1. Nelle impostazioni di configurazione, specifica il connettore del firewall AWS. Se non è ancora stato aggiunto il connettore per DSP, aggiungere un connettore utilizzando le seguenti informazioni:

      * **Nome:** Il nome del connettore.

      * **Chiave di accesso:** La chiave di accesso fornita dal team dell&#39;account Adobe.

      * **Chiave segreta:** La chiave segreta fornita dal team dell&#39;account Adobe.

      * **Regione:** Stati Uniti orientali della Virginia settentrionale (us-east-1)

   1. Nelle impostazioni delle azioni, eseguire le operazioni seguenti:

      1. Crea un’azione &quot;Send Customer Data to Delivery Stream (Advanced)&quot; per aggiungere dati al segmento, utilizzando le seguenti informazioni:

         * **Nome azione:** Nome dell&#39;azione.

         * **Tipo azione:** Invia dati del cliente al flusso di consegna (avanzata)

         * **Flusso di consegna:** Tealium_CDP_Connector

         * **Dati messaggio:** Effettuare le operazioni seguenti:

            1. Scegli un attributo per il segmento:

               * Per l&#39;attributo Hashed_Email, denominare il messaggio personalizzato `hashed_email`.

               * Per l&#39;attributo Cookies, denominare il messaggio personalizzato `cookies`.

            1. Nell&#39;opzione per la creazione di un campo personalizzato, nel campo [!DNL Source Key], immettere [!UICONTROL External Segment Key] incluso nei [dati di mappatura segmenti](#map-data) nella procedura precedente.

               L’DSP utilizzerà questa chiave per popolare il segmento.

            1. (Consigliato) Crea un’azione di aggiornamento per mantenere fresco il segmento.

## Passaggio 5: duplica il connettore esistente in [!DNL Tealium] per continuare a condividere i segmenti {#duplicate-connector}

Puoi avere un solo connettore per segmento e un solo segmento per connettore.

1. In [!DNL Tealium], duplicare il segmento per il quale si desidera creare un altro segmento e rinominare il nuovo segmento.

1. In [!DNL Tealium], duplicare [il connettore creato](#tealium-connector) nella procedura precedente e rinominare il nuovo connettore da &quot;`<original name>-copy`&quot; al nuovo nome del segmento.

## Passaggio 6: confrontare il numero di ID universali con il numero di indirizzi e-mail con hash {#compare-id-count}

I segmenti devono essere disponibili nell’DSP entro 24 ore. Dopo che l’DSP ha ricevuto i dati del segmento, il conteggio del pubblico dovrebbe essere visibile entro nove (9) ore.

Verifica nella libreria del pubblico (disponibile quando crei o modifichi un pubblico da [!UICONTROL Audiences] > [!UICONTROL All Audiences] o nelle impostazioni di posizionamento) che il segmento si stia popolando e confronta il numero di ID universali con il numero di indirizzi e-mail con hash originali. Per informazioni sulle percentuali di traduzione degli ID accettabili e sul motivo per cui i conteggi dei segmenti possono variare, consulta &quot;[Varianze di dati tra ID e-mail e ID universali](#universal-ids-data-variances).&quot;

I segmenti vengono aggiornati ogni 24 ore. Tuttavia, l’inclusione in un segmento scade dopo 30 giorni per impostazione predefinita o dopo un periodo di scadenza specificato dal cliente. Aggiorna i segmenti inviandoli di nuovo da [!DNL Tealium] prima della scadenza. Per richiedere la scadenza di un segmento personalizzato, contatta il team dell’account Adobe.

## Risoluzione dei problemi

Per risolvere i problemi relativi al tasso di traduzione e al conteggio degli utenti, consulta &quot;[Supporto per l&#39;attivazione degli ID universali](/help/dsp/audiences/universal-ids.md).&quot;

Per risolvere i problemi relativi alla procedura di conversione, contatta il team dell&#39;account Adobe o `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Informazioni sulle origini del pubblico di prime parti](/help/dsp/audiences/sources/source-about.md)
>* [Gestione delle origini del pubblico per attivare i tipi di pubblico con ID universale](source-manage.md)
>* [Supporto per l&#39;attivazione di ID universali](/help/dsp/audiences/universal-ids.md)
>* [Informazioni su Gestione dell&#39;audience](/help/dsp/audiences/audience-about.md)
