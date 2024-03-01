---
title: Attivare i segmenti autenticati dai partner Universal ID
description: Scopri come attivare i tipi di pubblico autenticati tramite una soluzione ID universale.
feature: DSP Audiences
exl-id: c56a54c7-5300-4cda-96d0-82d86e76ee39
source-git-commit: 5d031fe746dc5051320e5d2092f9148b5a8a1bd5
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 0%

---

# Attivare i segmenti autenticati dai partner Universal ID

Per attivare i tipi di pubblico autenticati tramite una soluzione ID universale in Advertising DSP, i segmenti devono essere tradotti in [!DNL RampIDs], riconoscibili in un ambiente che può essere oggetto di offerte. A tale scopo, puoi effettuare le seguenti operazioni:

* Sfruttare l’integrazione dell’DSP con [!DNL Adobe Real-Time Customer Data Platform (CDP)] e [!DNL Adobe-LiveRamp Retrieval API].

* Invio manuale di segmenti autenticati all’DSP dal [!DNL LiveRamp] [!DNL Connect] dashboard.

## Attività

1. Per entrambe le opzioni, contatta `adcloud-support@adobe.com` per abilitare le seguenti impostazioni in DSP, che consentiranno di eseguire il targeting dei segmenti autenticati nelle campagne DSP una volta [tutti i passaggi nel flusso di lavoro di attivazione sono completati](source-adobe-rtcdp.md):

   * [!DNL LiveRamp] [!DNL RampID] configurazione della campagna prima della condivisione del segmento da [!DNL Real-Time CDP]

   * A livello di account &quot;[!UICONTROL LiveRamp segments]Opzione &quot;

1. (Gli utenti condividono manualmente i segmenti autenticati da [!DNL LiveRamp]a) Completa i seguenti passaggi nella [!DNL LiveRamp] [!DNL Connect] dashboard:

   1. Attiva il riquadro di destinazione **[!DNL AAC API 1P Onboarding]**.

   1. Imposta [!DNL Identifier Settings] a **[!DNL Ramp ID]** solo.

      ![Impostazioni identificatore](/help/dsp/assets/liveramp-tile-settings.png)

   1. (Facoltativo) Se desideri ricevere comunque gli identificatori basati su cookie, crea un secondo [!DNL AAC API 1P Onboarding] riquadro di destinazione con &quot;[!DNL Cookies],&quot; &quot;[!DNL IDFA],&quot; e &quot;[!DNL AAID]&quot; selezionato.

## Best practice per il test e la convalida dei dati

* **Target [!DNL RampID]segmenti basati su e segmenti basati su cookie in campagne separate.**

   * Le impostazioni della campagna consentono di assegnare una sola priorità a un identificatore.

   * Attualmente, [!DNL RampIDs] non sono recuperabili durante gli eventi nel sito. Ciò significa che alcuni obiettivi personalizzati, come CPA più bassi e ROAS, non sono disponibili con l’utilizzo di segmenti autenticati. Utilizza i segmenti basati su cookie solo se disponi di un KPI delle prestazioni restrittivo.

* **Creare un posizionamento in entrambi [!DNL RampID] e campagne basate su cookie.**

   * Esegui il targeting dei segmenti condivisi da [!DNL LiveRamp] utilizzando il processo di attivazione del segmento standard.

   * Collabora con il tuo team di supporto Adobi Advertising per verificare la corretta distribuzione dei dati.

Per ulteriori informazioni sull’integrazione dell’DSP con [!DNL LiveRamp], contatto `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Informazioni sull’attivazione di segmenti autenticati da origini pubblico](source-about.md)
>* [Creare un’origine di pubblico per attivare tipi di pubblico di prime parti](source-create.md)
>* [Impostazioni origine pubblico](source-settings.md)
>* [Connessione Adobe Advertising DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Informazioni su Gestione dell&#39;audience](/help/dsp/audiences/audience-about.md)
