---
title: Utilizzo dell'integrazione di DSP con  [!DNL Adobe] [!DNL Real-time CDP]
description: Scopri come abilitare DSP per acquisire i  [!DNL Adobe] [!DNL Real-time CDP] segmenti di prime parti.
feature: DSP Audiences
exl-id: cb1da95b-0d19-4450-8770-6c383248ddae
TQID: https://experienceleague.adobe.com/Ggt-YiAoGurfI5eET66xJwMBTSq-w5FO7wH60WZshEk
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: 50af5a8fc6e5e82268489259073e27911ca5a45c
workflow-type: tm+mt
source-wordcount: 596
ht-degree: 0%

---

# Converti ID utente da [!DNL Adobe Real-Time CDP] in ID universali

Utilizza l&#39;integrazione di DSP con [the [!DNL Adobe Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=it), che fa parte di Adobe Experience Platform, per convertire gli ID utente, inclusi gli indirizzi e-mail con hash, i cookie e gli ID mobile advertising, in ID universali per la pubblicità mirata.

1. (Per convertire gli ID utente in [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; inserzionisti con [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) Impostare il tracciamento per la misurazione di [!DNL Analytics]:

   1. (Se non lo hai già fatto) Completa tutti i [prerequisiti per l&#39;implementazione [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) e l&#39;[AMO ID e EF ID negli URL di tracciamento](/help/integrations/analytics/ids.md).

   1. Registrati con il partner ID universale e implementa sulle tue pagine web un codice ID universale che corrisponda alle conversioni dagli ID sui browser Web per desktop e dispositivi mobili (ma non sulle app mobili) ai view-through:

      * **Per [!DNL RampIDs]:** è necessario distribuire un tag JavaScript aggiuntivo nelle pagine Web per far corrispondere le conversioni dagli ID nei browser Web desktop e mobile (ma non nelle app mobili) alle view-through. Contatta il team del tuo account Adobe, che ti fornirà le istruzioni per registrarti per un tag [!DNL LiveRamp] [!DNL LaunchPad] da [!DNL LiveRamp] soluzioni traffico autenticazione (ats.js). La registrazione è gratuita, ma è necessario firmare un accordo. Dopo la registrazione, il team dell’account Adobe genererà e fornirà un tag univoco per l’organizzazione da implementare sulle pagine web.

1. [Crea un&#39;origine pubblico](source-manage.md) per importare i tipi di pubblico nel tuo account DSP o in un account inserzionista. Puoi scegliere di convertire gli identificatori utente in uno qualsiasi dei [formati ID universali disponibili](source-about.md).

   Le impostazioni di origine includono una chiave di origine generata automaticamente, che verrà utilizzata nel passaggio successivo.

1. In Adobe Experience Platform, configura una connessione di destinazione Advertising DSP utilizzando [!UICONTROL Source Key] generato nelle impostazioni di origine di DSP.

   L’hashing degli indirizzi e-mail deve essere eseguito utilizzando l’algoritmo SHA-256.

   Per istruzioni sull&#39;attivazione della connessione di destinazione DSP, l&#39;attivazione dei tipi di pubblico e la convalida dell&#39;esportazione dei dati, vedere &quot;[Connessione Adobe Advertising DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html?lang=it)&quot;.

   >[!NOTE]
   >
   >La connessione legacy, che include il supporto solo per indirizzi e-mail con hash, è ora denominata &quot;[Connessione legacy Adobe Advertising Cloud DSP](https://experienceleague.adobe.com/it/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection-legacy). Se utilizzi già la connessione legacy, non è necessario apportare immediatamente alcuna modifica. Tuttavia, la connessione legacy verrà alla fine rimossa.

1. Verifica nella libreria del pubblico (disponibile quando crei o modifichi un pubblico da [!UICONTROL Audiences] > [!UICONTROL All Audiences] o nelle impostazioni di posizionamento) che il segmento si stia popolando e confronta il numero di ID universali con il numero di ID utente originali.

   I segmenti dovrebbero essere disponibili in DSP entro 24 ore. Dopo che DSP ha ricevuto i dati del segmento, il conteggio del pubblico dovrebbe essere visibile entro nove (9) ore. Per informazioni sulle percentuali di traduzione degli ID accettabili e sul motivo per cui i conteggi dei segmenti possono variare, consulta &quot;[Varianze di dati tra ID e-mail e ID universali](#universal-ids-data-variances).&quot;

I segmenti vengono aggiornati ogni 24 ore. Tuttavia, l’inclusione in un segmento scade dopo 30 giorni per impostazione predefinita o dopo un periodo di scadenza specificato dal cliente. Aggiorna i segmenti inviandoli nuovamente da Real-Time CDP prima della scadenza. Per richiedere la scadenza di un segmento personalizzato, contatta il team del tuo account Adobe.

## Risoluzione dei problemi

Per risolvere i problemi relativi al tasso di traduzione e al conteggio degli utenti, consulta &quot;[Supporto per l&#39;attivazione degli ID universali](/help/dsp/audiences/universal-ids.md).&quot;

Per risolvere i problemi relativi alla procedura di conversione, contatta il team dell&#39;account Adobe o `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Informazioni sulle origini del pubblico di prime parti](/help/dsp/audiences/sources/source-about.md)
>* [Gestisci origini pubblico per attivare il pubblico con ID universale](source-manage.md)
>* [Connessione Adobe Advertising DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html?lang=it)
>* Adobe Experience Platform [Panoramica del catalogo delle destinazioni](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html?lang=it)
>* [Supporto per l&#39;attivazione degli ID universali](/help/dsp/audiences/universal-ids.md)
>* [Informazioni su Gestione dell&#39;audience](/help/dsp/audiences/audience-about.md)
