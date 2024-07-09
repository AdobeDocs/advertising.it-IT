---
title: Converti ID utente da [!DNL Amperity] agli ID universali
description: Scopri come consentire all’DSP di acquisire [!DNL Amperity] segmenti di prime parti.
feature: DSP Audiences
exl-id: c751709a-5ad2-43fa-ba3a-fc7a9683da3f
source-git-commit: 8a8f19c7db95c0eda05a3262eeaf4c8a0aeaaa64
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 0%

---

# Converti ID utente da [!DNL Amperity] agli ID universali

*Funzione Beta*

Utilizzare l’integrazione DSP con [!DNL Amperity] customer data platform per convertire gli indirizzi e-mail con hash di prime parti della tua organizzazione in ID universali per annunci pubblicitari mirati.

1. (Per convertire gli indirizzi e-mail in [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; inserzionisti con [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Configura il tracciamento per abilitare [!DNL Analytics] misurazione](#analytics-tracking).

1. [Creare un’origine di pubblico in DSP](#source-create).

1. [Preparare e condividere i dati di mappatura dei segmenti](#map-data).

1. [Richiedi un push dati da [!DNL Amperity] all’DSP](#push-data).

1. [Confrontare il numero di ID universali con il numero di indirizzi e-mail con hash](#compare-id-count).

## Passaggio 1: configurare il tracciamento per [!DNL Analytics] misurazione {#analytics-tracking}

*Inserzionisti con [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

Per convertire gli indirizzi e-mail in [!DNL RampIDs] o [!DNL ID5] ID, devi effettuare le seguenti operazioni:

1. (Se non lo hai già fatto) Completa tutto [prerequisiti per l&#39;implementazione [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) e assicurarsi che il [AMO ID e EF ID](/help/integrations/analytics/ids.md) vengono inseriti negli URL di tracciamento.

1. Registrati con il partner ID universale e implementa sulle tue pagine web un codice ID universale che corrisponda alle conversioni dagli ID sui browser Web per desktop e dispositivi mobili (ma non sulle app mobili) ai view-through:

   * **Per [!DNL RampIDs]:** Devi distribuire un tag JavaScript aggiuntivo sulle tue pagine web per far corrispondere le conversioni dagli ID sui browser web desktop e mobili (ma non sulle app mobili) alle view-through. Contatta il tuo Account Team di Adobi, che ti fornirà le istruzioni per registrarti a un [!DNL LiveRamp] [!DNL LaunchPad] tag da [!DNL LiveRamp] Soluzioni per il traffico di autenticazione. La registrazione è gratuita, ma è necessario firmare un accordo. Dopo la registrazione, il team dell’account Adobe genererà e fornirà un tag univoco per l’organizzazione da implementare sulle pagine web.

## Passaggio 2: creare un’origine di pubblico nell’DSP {#source-create}

1. [Creare un’origine di pubblico](source-manage.md) per importare tipi di pubblico sul tuo account DSP o su un account inserzionista. Puoi scegliere di convertire gli identificatori utente in uno qualsiasi dei [formati ID universali disponibili](source-about.md).

   Le impostazioni di origine includono una chiave di origine generata automaticamente, che utilizzerai per inviare i dati del segmento.

1. Dopo aver creato l&#39;origine del pubblico, condividi la chiave del codice sorgente con [!DNL Amperity] utente.

## Passaggio 3: preparare e condividere i dati di mappatura dei segmenti {#map-data}

L’inserzionista deve preparare e condividere i dati di mappatura dei segmenti.

1. Entro [!DNL Amperity], esegue l’hashing degli ID e-mail per il pubblico utilizzando l’algoritmo SHA-256.

1. L’inserzionista deve fornire i dati di mappatura dei segmenti all’Account Team Adobe per creare i segmenti nell’DSP. Utilizza i seguenti nomi e valori di colonna in un file di valori separati da virgola:

   * **Chiave segmento esterna:** Il [!DNL Amperity] chiave del segmento associata al segmento.

   * **Nome segmento:** Il nome del segmento.

   * **Descrizione segmento:** Lo scopo o la regola del segmento, o entrambi.

   * **ID principale:** Mantieni vuoto

   * **Video CPM:** 0

   * **Visualizza CPM:** 0

   * **Finestra segmento:** Il time-to-live del segmento.

## Passaggio 4: richiedere un push dati da [!DNL Amperity] all’DSP {#push-data}

1. Dopo aver mappato il segmento all’interno dell’DSP, l’inserzionista deve lavorare con il proprio [!DNL Amperity] rappresentativo per la distribuzione dei dati dei segmenti all’DSP.

1. L’inserzionista deve quindi confermare con l’Account Team Adobe che i dati del segmento sono stati ricevuti.

I segmenti devono essere disponibili nell’DSP entro 24 ore. Verifica nella libreria del pubblico (disponibile quando crei o modifichi un pubblico da ) [!UICONTROL Audiences] > [!UICONTROL All Audiences] o nelle impostazioni di posizionamento) che il segmento è disponibile e si sta popolando.

I segmenti verranno aggiornati in base alla configurazione per l’inserzionista in [!DNL Amperity]. Indipendentemente dalla frequenza con cui il segmento viene aggiornato, l’inclusione in un segmento scade dopo 30 giorni per impostazione predefinita o dopo un periodo di scadenza specificato dal cliente. Aggiorna i segmenti inviandoli di nuovo da [!DNL Amperity] prima della scadenza. Per richiedere la scadenza di un segmento personalizzato, contatta il team dell’account Adobe.

## Passaggio 5: confrontare il numero di ID universali con il numero di indirizzi e-mail con hash {#compare-id-count}

Dopo che l’DSP ha ricevuto i dati del segmento, il conteggio del pubblico dovrebbe essere visibile entro nove (9) ore. Nella libreria del pubblico (disponibile quando crei o modifichi un pubblico da ) [!UICONTROL Audiences] > [!UICONTROL All Audiences] o nelle impostazioni di posizionamento) confrontano il numero di ID universali con il numero di indirizzi e-mail con hash originali.

Per informazioni sui tassi accettabili di traduzione degli ID e sul perché i conteggi dei segmenti possono variare, consulta la sezione &quot;[Varianze di dati tra ID e-mail e ID universali](#universal-ids-data-variances).&quot;

Per assistenza nella risoluzione dei problemi, contatta il team del tuo account di Adobe oppure `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Informazioni sulle origini del pubblico di prime parti](/help/dsp/audiences/sources/source-about.md)
>* [Gestire le origini del pubblico per attivare i tipi di pubblico con ID universale](source-manage.md)
>* [Supporto per l’attivazione di ID universali](/help/dsp/audiences/universal-ids.md)
>* [Informazioni su Gestione dell&#39;audience](/help/dsp/audiences/audience-about.md)
