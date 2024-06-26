---
title: Utilizzo dell’integrazione DSP con [!DNL Adobe] [!DNL Real-time CDP]
description: Scopri come consentire all’DSP di acquisire [!DNL Adobe] [!DNL Real-time CDP] segmenti di prime parti.
feature: DSP Audiences
exl-id: cb1da95b-0d19-4450-8770-6c383248ddae
source-git-commit: 7963623d20686553629e2aa7ad76b4fd48403555
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 0%

---

# Converti ID utente da [!DNL Adobe Real-Time CDP] agli ID universali

*Funzione beta*

Utilizzare l’integrazione DSP con [il [!DNL Adobe Real-Time Customer Data Platform (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=it), che fa parte di Adobe Experience Platform, per convertire i tuoi indirizzi e-mail con hash in ID universali per la pubblicità mirata.

1. (Per convertire gli indirizzi e-mail in [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; inserzionisti con [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)a) Impostare il tracciamento per [!DNL Analytics] misurazione:

   1. (Se non lo hai già fatto) Completa tutto [prerequisiti per l&#39;implementazione [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) e [AMO ID e EF ID negli URL di tracciamento](/help/integrations/analytics/ids.md).

   1. Registrati con il partner ID universale e implementa sulle tue pagine web un codice ID universale che corrisponda alle conversioni dagli ID sui browser Web per desktop e dispositivi mobili (ma non sulle app mobili) ai view-through:

      * **Per [!DNL RampIDs]:** Devi distribuire un tag JavaScript aggiuntivo sulle pagine web per far corrispondere le conversioni dagli ID sui browser web desktop e mobili (ma non sulle app mobili) alle view-through. Contatta il tuo Account Team di Adobi, che ti fornirà le istruzioni per registrarti a un [!DNL LiveRamp] [!DNL LaunchPad] tag da [!DNL LiveRamp] Soluzioni per il traffico di autenticazione. La registrazione è gratuita, ma è necessario firmare un accordo. Dopo la registrazione, il team dell’account Adobe genererà e fornirà un tag univoco per l’organizzazione da implementare sulle pagine web.

1. [Creare un’origine di pubblico](source-manage.md) per importare tipi di pubblico sul tuo account DSP o su un account inserzionista. Puoi scegliere di convertire gli identificatori utente in uno qualsiasi dei [formati ID universali disponibili](source-about.md).

   Le impostazioni di origine includono una chiave di origine generata automaticamente, che verrà utilizzata nel passaggio successivo.

1. In Adobe Experience Platform, configura una connessione di destinazione Advertising DSP utilizzando [!UICONTROL Source Key] generato nelle impostazioni di origine dell’DSP.

   Per istruzioni su come attivare la connessione di destinazione DSP, selezionare i segmenti e accedere alle autorizzazioni di controllo, vedi &quot;[Connessione Adobe Advertising Cloud DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).&quot;

   L’hashing degli indirizzi e-mail di origine deve essere eseguito utilizzando l’algoritmo SHA-256.

1. Dopo aver completato tutti i passaggi, verifica nella libreria del pubblico (disponibile quando crei o modifichi un pubblico da [!UICONTROL Audiences] > [!UICONTROL All Audiences] o nelle impostazioni di posizionamento) che il segmento viene popolato entro 24 ore. Confronta il numero di ID universali con il numero di indirizzi e-mail con hash originali.

   Il tasso di conversione degli indirizzi e-mail con hash in ID universali deve essere superiore al 90%. Ad esempio, se invii 100 indirizzi e-mail con hash dalla piattaforma dati del cliente, questi devono essere tradotti in più di 90 ID universali. Un tasso di traduzione pari o inferiore al 90% è un problema. Per ulteriori informazioni sulle possibili variazioni dei conteggi dei segmenti, consulta la sezione &quot;[Cause delle varianze di dati tra ID e-mail e ID universali](#universal-ids-data-variances).&quot;

   Per assistenza nella risoluzione dei problemi, contatta il team del tuo account di Adobe oppure `adcloud-support@adobe.com`.

I segmenti vengono aggiornati ogni 24 ore. Tuttavia, l’inclusione in un segmento scade dopo 30 giorni per impostazione predefinita o dopo un periodo di scadenza specificato dal cliente. Aggiorna i segmenti inviandoli nuovamente da Real-Time CDP prima della scadenza. Per richiedere la scadenza di un segmento personalizzato, contatta il team dell’account Adobe.

>[!MORELIKETHIS]
>
>* [Informazioni sulle origini del pubblico di prime parti](/help/dsp/audiences/sources/source-about.md)
>* [Gestire le origini del pubblico per attivare i tipi di pubblico con ID universale](source-manage.md)
>* [Connessione Adobe Advertising DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [Panoramica del catalogo delle destinazioni](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [Supporto per l’attivazione di ID universali](/help/dsp/audiences/universal-ids.md)
>* [Informazioni su Gestione dell&#39;audience](/help/dsp/audiences/audience-about.md)
