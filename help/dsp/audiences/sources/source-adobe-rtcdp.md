---
title: Utilizzo dell'integrazione DSP con  [!DNL Adobe] [!DNL Real-time CDP]
description: Scopri come consentire all’DSP di acquisire i  [!DNL Adobe] [!DNL Real-time CDP] segmenti di prime parti.
feature: DSP Audiences
exl-id: cb1da95b-0d19-4450-8770-6c383248ddae
source-git-commit: 3a641db6b145e67e6e1f1daca271dd524973e075
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 0%

---

# Converti ID utente da [!DNL Adobe Real-Time CDP] in ID universali

*funzionalità Beta*

Utilizza l&#39;integrazione DSP con [the [!DNL Adobe Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=it), che fa parte di Adobe Experience Platform, per convertire gli indirizzi e-mail con hash in ID universali per la pubblicità mirata.

1. (Per convertire gli indirizzi e-mail in [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; inserzionisti con [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) Impostare il tracciamento per la misurazione di [!DNL Analytics]:

   1. (Se non lo hai già fatto) Completa tutti i [prerequisiti per l&#39;implementazione [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) e l&#39;[AMO ID e EF ID negli URL di tracciamento](/help/integrations/analytics/ids.md).

   1. Registrati con il partner ID universale e implementa sulle tue pagine web un codice ID universale che corrisponda alle conversioni dagli ID sui browser Web per desktop e dispositivi mobili (ma non sulle app mobili) ai view-through:

      * **Per [!DNL RampIDs]:** è necessario distribuire un tag JavaScript aggiuntivo nelle pagine Web per far corrispondere le conversioni dagli ID nei browser Web desktop e mobile (ma non nelle app mobili) alle view-through. Contatta il team dell&#39;account Adobe, che ti fornirà le istruzioni per registrarti per un tag [!DNL LiveRamp] [!DNL LaunchPad] da [!DNL LiveRamp] soluzioni traffico autenticazione. La registrazione è gratuita, ma è necessario firmare un accordo. Dopo la registrazione, il team dell’account Adobe genererà e fornirà un tag univoco per l’organizzazione da implementare sulle pagine web.

1. [Crea un&#39;origine di pubblico](source-manage.md) per importare i tipi di pubblico nel tuo account DSP o in un account inserzionista. Puoi scegliere di convertire gli identificatori utente in uno qualsiasi dei [formati ID universali disponibili](source-about.md).

   Le impostazioni di origine includono una chiave di origine generata automaticamente, che verrà utilizzata nel passaggio successivo.

1. In Adobe Experience Platform, configura una connessione di destinazione Advertising DSP utilizzando [!UICONTROL Source Key] generato nelle impostazioni di origine DSP.

   Per istruzioni su come attivare la connessione di destinazione DSP, selezionare i segmenti e accedere alle autorizzazioni di controllo, vedere &quot;[Connessione Adobe Advertising Cloud DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).&quot;

   L’hashing degli indirizzi e-mail di origine deve essere eseguito utilizzando l’algoritmo SHA-256.

1. Verifica nella libreria del pubblico (disponibile quando crei o modifichi un pubblico da [!UICONTROL Audiences] > [!UICONTROL All Audiences] o nelle impostazioni di posizionamento) che il segmento si stia popolando e confronta il numero di ID universali con il numero di indirizzi e-mail con hash originali.

   I segmenti devono essere disponibili nell’DSP entro 24 ore. Dopo che l’DSP ha ricevuto i dati del segmento, il conteggio del pubblico dovrebbe essere visibile entro nove (9) ore. Per informazioni sulle percentuali di traduzione degli ID accettabili e sul motivo per cui i conteggi dei segmenti possono variare, consulta &quot;[Varianze di dati tra ID e-mail e ID universali](#universal-ids-data-variances).&quot;

I segmenti vengono aggiornati ogni 24 ore. Tuttavia, l’inclusione in un segmento scade dopo 30 giorni per impostazione predefinita o dopo un periodo di scadenza specificato dal cliente. Aggiorna i segmenti inviandoli nuovamente da Real-Time CDP prima della scadenza. Per richiedere la scadenza di un segmento personalizzato, contatta il team dell’account Adobe.

## Risoluzione dei problemi

Per risolvere i problemi relativi al tasso di traduzione e al conteggio degli utenti, consulta &quot;[Supporto per l&#39;attivazione degli ID universali](/help/dsp/audiences/universal-ids.md).&quot;

Per risolvere i problemi relativi alla procedura di conversione, contatta il team dell&#39;account Adobe o `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Informazioni sulle origini del pubblico di prime parti](/help/dsp/audiences/sources/source-about.md)
>* [Gestione delle origini del pubblico per attivare i tipi di pubblico con ID universale](source-manage.md)
>* [Connessione Adobe Advertising DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [Panoramica del catalogo delle destinazioni](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [Supporto per l&#39;attivazione di ID universali](/help/dsp/audiences/universal-ids.md)
>* [Informazioni su Gestione dell&#39;audience](/help/dsp/audiences/audience-about.md)
