---
title: Converti ID utente da [!DNL Optimizely] agli ID universali
description: Scopri come consentire all’DSP di acquisire [!DNL Optimizely] segmenti di prime parti.
feature: DSP Audiences
source-git-commit: 295cc610a7e5e811fe555db69373a8bf5b4012f7
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 0%

---

# Converti ID utente da [!DNL Optimizely] agli ID universali

Utilizzare l’integrazione DSP con [!DNL Optimizely] customer data platform per convertire gli indirizzi e-mail con hash di prime parti della tua organizzazione in ID universali per annunci pubblicitari mirati.

1. (Per convertire gli indirizzi e-mail in [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; inserzionisti con [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Configura il tracciamento per abilitare [!DNL Analytics] misurazione](#analytics-tracking).

1. [Creare un’origine di pubblico in DSP](#source-create).

1. [Preparare e inviare i dati del segmento in [!DNL Optimizely Data Platform]](#push-data).

1. [Confrontare il numero di ID universali con il numero di indirizzi e-mail con hash](#compare-id-count).

I segmenti devono essere disponibili nell’DSP entro 24 ore e devono essere aggiornati ogni 24 ore. **[Vero o aspettative diverse per Optimizely?]**

## Passaggio 1: configurare il tracciamento per [!DNL Analytics] misurazione {#analytics-tracking}

*Inserzionisti con [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

Per convertire gli indirizzi e-mail in [!DNL RampIDs] o [!DNL ID5] ID, devi effettuare le seguenti operazioni:

1. (Se non lo hai già fatto) Completa tutto [prerequisiti per l&#39;implementazione [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) e assicurarsi che il [AMO ID e EF ID](/help/integrations/analytics/ids.md) vengono inseriti negli URL di tracciamento.

1. Registrati con il partner ID universale e implementa sulle tue pagine web un codice ID universale che corrisponda alle conversioni dagli ID sui browser Web per desktop e dispositivi mobili (ma non sulle app mobili) ai view-through:

   * **Per [!DNL RampIDs]:** Devi distribuire un tag JavaScript aggiuntivo sulle pagine web per far corrispondere le conversioni dagli ID sui browser web desktop e mobili (ma non sulle app mobili) alle view-through. Contatta il tuo Account Team di Adobi, che ti fornirà le istruzioni per registrarti a un [!DNL LiveRamp] [!DNL LaunchPad] tag da [!DNL LiveRamp] Soluzioni per il traffico di autenticazione. La registrazione è gratuita, ma è necessario firmare un accordo. Dopo la registrazione, il team dell’account Adobe genererà e fornirà un tag univoco per l’organizzazione da implementare sulle pagine web.

## Passaggio 2: creare un’origine di pubblico nell’DSP {#source-create}

1. [Creare un’origine di pubblico](source-create.md) per importare tipi di pubblico sul tuo account DSP o su un account inserzionista. Puoi scegliere di convertire gli identificatori utente in uno qualsiasi dei [formati ID universali disponibili](source-about.md).

   Le impostazioni di origine includono una chiave di origine generata automaticamente, che utilizzerai per inviare i dati del segmento.

1. Dopo aver creato l&#39;origine del pubblico, condividi la chiave del codice sorgente con [!DNL Optimizely] utente.

## Passaggio 3: preparare e inviare i dati del segmento {#push-data}

L’inserzionista deve preparare e inviare i dati entro [!DNL Optimizely Data Platform].  **[Utilizzano Optimizely Data Platform?]**  <!-- Data Platform? -->

1. Effettua l&#39;hashing degli ID e-mail per il pubblico dell&#39;inserzionista utilizzando l&#39;algoritmo SHA-256.

1. Invia il segmento all’DSP, inclusi i seguenti campi:

   **[Utilizzano i servizi web di Data Platform, un altro tipo di API o un’interfaccia utente? Aggiungi un collegamento alle istruzioni. E dove immetteranno questi campi?]**  <!-- Are they using the Data Platform web services or what? Add a link to instructions. And where will they input these fields?  -->

   * **Chiave di origine:** Chiave sorgente creata in [Passaggio 2](#source-create).

   * **Codice account:** Questo è il codice alfanumerico dell&#39;account DSP, che puoi trovare all&#39;interno dell&#39;DSP all&#39;indirizzo [!UICONTROL Settings] > [!UICONTROL Account].

## Passaggio 4: confrontare il numero di ID universali con il numero di indirizzi e-mail con hash {#compare-id-count}

Dopo aver completato tutti i passaggi, verifica nella libreria del pubblico (disponibile quando crei o modifichi un pubblico da [!UICONTROL Audiences] > [!UICONTROL All Audiences] o nelle impostazioni di posizionamento) che il segmento è disponibile e si popola entro 24 ore. Confronta il numero di ID universali con il numero di indirizzi e-mail con hash originali.

Il tasso di conversione degli indirizzi e-mail con hash in ID universali deve essere superiore al 90%. Ad esempio, se invii 100 indirizzi e-mail con hash dalla piattaforma dati del cliente, questi devono essere tradotti in più di 90 ID universali. Un tasso di traduzione pari o inferiore al 90% è un problema. Per ulteriori informazioni sulle possibili variazioni dei conteggi dei segmenti, consulta la sezione &quot;[Cause delle varianze di dati tra ID e-mail e ID universali](#universal-ids-data-variances).&quot;

I segmenti vengono aggiornati ogni 24 ore. Tuttavia, l’inclusione in un segmento scade dopo 30 giorni per garantire la conformità in materia di privacy, in modo da aggiornare i tipi di pubblico inviandoli nuovamente da [!DNL Optimizely] ogni 30 giorni o meno.

Per assistenza nella risoluzione dei problemi, contatta il team del tuo account di Adobe oppure `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Informazioni sulle origini del pubblico di prime parti](/help/dsp/audiences/sources/source-about.md)
>* [Gestire le origini del pubblico per attivare i tipi di pubblico con ID universale](source-manage.md)
>* [Impostazioni origine pubblico](source-settings.md)
>* [Converti ID utente da [!DNL Adobe Real-Time CDP] agli ID universali](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Converti ID utente da [!DNL Tealium] agli ID universali](/help/dsp/audiences/sources/source-tealium.md)
>* [Informazioni su Gestione dell&#39;audience](/help/dsp/audiences/audience-about.md)
