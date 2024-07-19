---
title: Converti ID utente da [!DNL Optimizely] a ID universali
description: Scopri come consentire all’DSP di acquisire i  [!DNL Optimizely]  segmenti di prime parti.
feature: DSP Audiences
exl-id: 2c48a874-132a-4e5c-ba24-0e7ab80ac2d4
source-git-commit: 91b08bf54f067666c9c27949ff740639738887d0
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 0%

---

# Converti ID utente da [!DNL Optimizely] in ID universali

*funzionalità Beta*

Utilizza l&#39;integrazione DSP con la piattaforma dati cliente [!DNL Optimizely] per convertire gli indirizzi e-mail con hash di prime parti della tua organizzazione in ID universali per pubblicità mirata.

1. (Per convertire gli indirizzi e-mail in [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; inserzionisti con [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Configura il tracciamento per abilitare [!DNL Analytics] la misurazione](#analytics-tracking).

1. [Crea un&#39;origine pubblico in DSP](#source-create).

1. [Prepara e invia i dati del segmento](#push-data).

1. [Confrontare il numero di ID universali con il numero di indirizzi e-mail con hash](#compare-id-count).

## Passaggio 1: configurare il tracciamento per la misurazione [!DNL Analytics] {#analytics-tracking}

*Inserzionisti con [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

Per convertire gli indirizzi e-mail in [!DNL RampIDs] o [!DNL ID5] ID, è necessario effettuare le seguenti operazioni:

1. (Se non lo hai già fatto) Completa tutti i [prerequisiti per l&#39;implementazione [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) e assicurati che [AMO ID e EF ID](/help/integrations/analytics/ids.md) siano inseriti negli URL di tracciamento.

1. Registrati con il partner ID universale e implementa sulle tue pagine web un codice ID universale che corrisponda alle conversioni dagli ID sui browser Web per desktop e dispositivi mobili (ma non sulle app mobili) ai view-through:

   * **Per [!DNL RampIDs]:** è necessario distribuire un tag JavaScript aggiuntivo nelle pagine Web per far corrispondere le conversioni dagli ID nei browser Web desktop e mobile (ma non nelle app mobili) alle view-through. Contatta il team dell&#39;account Adobe, che ti fornirà le istruzioni per registrarti a un tag [!DNL LiveRamp] [!DNL LaunchPad] da [!DNL LiveRamp] soluzioni traffico autenticazione. La registrazione è gratuita, ma è necessario firmare un accordo. Dopo la registrazione, il team dell’account Adobe genererà e fornirà un tag univoco per l’organizzazione da implementare sulle pagine web.

## Passaggio 2: creare un’origine di pubblico nell’DSP {#source-create}

1. [Crea un&#39;origine di pubblico](source-manage.md) per importare i tipi di pubblico nel tuo account DSP o in un account inserzionista. Puoi scegliere di convertire gli identificatori utente in uno qualsiasi dei [formati ID universali disponibili](source-about.md).

   Le impostazioni di origine includono una chiave di origine generata automaticamente, che utilizzerai per inviare i dati del segmento.

1. Dopo aver creato l&#39;origine del pubblico, condividere la chiave del codice sorgente con l&#39;utente [!DNL Optimizely].

## Passaggio 3: preparare e inviare i dati del segmento {#push-data}

L&#39;inserzionista deve preparare e inviare i dati utilizzando [!DNL Optimizely Data Platform]. Per qualsiasi domanda sul processo, contatta il tuo rappresentante [!DNL Optimizely].

1. In [!DNL Optimizely Data Platform], esegui l&#39;hash degli ID e-mail per il pubblico utilizzando l&#39;algoritmo SHA-256.

1. Segui le [[!DNL Optimizely's] istruzioni per inviare il segmento a DSP](https://support.optimizely.com/hc/en-us/articles/27974930963981-Integrate-Adobe-Ads). Includi le seguenti informazioni per abilitare l’integrazione:

   * **Chiave Source:** Chiave di origine creata in [Passaggio 2](#source-create).

   * **Codice account:** Questo è il codice alfanumerico dell&#39;account DSP, che puoi trovare all&#39;interno dell&#39;DSP in [!UICONTROL Settings] > [!UICONTROL Account].

I segmenti verranno aggiornati in base alla configurazione per l’inserzionista. Indipendentemente dalla frequenza con cui il segmento viene aggiornato, l’inclusione in un segmento scade dopo 30 giorni per impostazione predefinita o dopo un periodo di scadenza specificato dal cliente. Aggiorna i segmenti inviandoli di nuovo da [!DNL Optimizely] prima della scadenza. Per richiedere la scadenza di un segmento personalizzato, contatta il team dell’account Adobe.

## Passaggio 4: confrontare il numero di ID universali con il numero di indirizzi e-mail con hash {#compare-id-count}

I segmenti devono essere disponibili nell’DSP entro 24 ore. Dopo che l’DSP ha ricevuto i dati del segmento, il conteggio del pubblico dovrebbe essere visibile entro nove (9) ore.

Verifica nella libreria del pubblico (disponibile quando crei o modifichi un pubblico da [!UICONTROL Audiences] > [!UICONTROL All Audiences] o nelle impostazioni di posizionamento) che il segmento sia disponibile e si stia popolando, quindi confronta il numero di ID universali con il numero di indirizzi e-mail con hash originali. Per informazioni sulle percentuali di traduzione degli ID accettabili e sul motivo per cui i conteggi dei segmenti possono variare, consulta &quot;[Varianze di dati tra ID e-mail e ID universali](#universal-ids-data-variances).&quot;

## Risoluzione dei problemi

Per risolvere i problemi relativi al tasso di traduzione e al conteggio degli utenti, consulta &quot;[Supporto per l&#39;attivazione degli ID universali](/help/dsp/audiences/universal-ids.md).&quot;

Per risolvere i problemi relativi alla procedura di conversione, contatta il team dell&#39;account Adobe o `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Informazioni sulle origini del pubblico di prime parti](/help/dsp/audiences/sources/source-about.md)
>* [Gestione delle origini del pubblico per attivare i tipi di pubblico con ID universale](source-manage.md)
>* [Supporto per l&#39;attivazione di ID universali](/help/dsp/audiences/universal-ids.md)
>* [Informazioni su Gestione dell&#39;audience](/help/dsp/audiences/audience-about.md)
