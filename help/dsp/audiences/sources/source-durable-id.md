---
title: Attivare i segmenti autenticati dai partner ID durevoli
description: Scopri come attivare i tipi di pubblico autenticati tramite una soluzione ID durevole.
feature: DSP Audiences
exl-id: c56a54c7-5300-4cda-96d0-82d86e76ee39
source-git-commit: 9ca42d078c0d0b6a08d521c8465eca69c2affce5
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 0%

---

# Attivare i segmenti autenticati dai partner ID durevoli

*Funzione beta*

Per attivare i tipi di pubblico autenticati tramite una soluzione ID durevole all’interno di Advertising DSP, i segmenti devono essere tradotti in [!DNL RampIDs], riconoscibili in un ambiente accessibile. Puoi eseguire questa operazione:

* Sfruttare l’integrazione DSP con [!DNL Adobe Real-Time Customer Data Profile (CDP)] e [!DNL Adobe-LiveRamp Retrieval API].

* Invio manuale di segmenti autenticati a DSP dal [!DNL LiveRamp] [!DNL Connect] dashboard.

## Attività

1. Per entrambe le opzioni, contatta `adcloud-support@adobe.com` per abilitare le seguenti impostazioni in DSP, che ti consentiranno di eseguire il targeting dei segmenti autenticati nelle campagne DSP una volta [tutti i passaggi del flusso di lavoro di attivazione sono completati](source-about.md#workflow-sources):

   1. [!DNL LiveRamp] [!DNL RampID] configurazione della campagna prima della condivisione dei segmenti da [!DNL Real-Time CDP].

   1. A livello di account &quot;[!UICONTROL LiveRamp segments]&quot; opzione.

1. (Utenti che condividono manualmente i segmenti autenticati da [!DNL LiveRamp]) Completa i seguenti passaggi nella sezione [!DNL LiveRamp] [!DNL Connect] dashboard:

   1. Attiva il riquadro di destinazione **[!DNL AAC API 1P Onboarding]**.

   1. Imposta [!DNL Identifier Settings] a **[!DNL Ramp ID]** solo.

      ![Impostazioni identificatore](/help/dsp/assets/liveramp-tile-settings.png)

   1. (Facoltativo) Se desideri comunque ricevere gli identificatori basati su cookie, crea un secondo [!DNL AAC API 1P Onboarding] riquadro di destinazione con &quot;[!DNL Cookies]&quot;[!DNL IDFA],&quot; e &quot;[!DNL AAID]&quot; selezionato.

## Tecniche consigliate per il test e la convalida dei dati

* **Target [!DNL RampID]segmenti basati su cookie e segmenti basati su segmenti in campagne separate.**

   * Le impostazioni della campagna consentono di assegnare la priorità a un solo identificatore.

   * Attualmente, [!DNL RampIDs] non sono recuperabili durante gli eventi sul sito. Ciò significa che alcuni obiettivi personalizzati, come CPA e ROAS più bassi, non sono disponibili con l’utilizzo di segmenti autenticati. Utilizza segmenti basati su cookie solo se disponi di un KPI (Key Performance Indicator) restrittivo.

* **Crea un posizionamento in entrambe le [!DNL RampID] e campagne basate su cookie.**

   * Esegui il targeting dei segmenti condivisi da [!DNL LiveRamp] utilizzando il processo standard di attivazione dei segmenti.

   * Collabora con il tuo team di supporto Adobe Advertising per convalidare la corretta distribuzione dei dati.

Per ulteriori informazioni sull’integrazione DSP con [!DNL LiveRamp], contatto `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Informazioni sull’attivazione dei segmenti autenticati da Audience Sources](source-about.md)
>* [Creare una sorgente di pubblico per attivare il pubblico di prime parti](source-create.md)
>* [Impostazioni origine pubblico](source-settings.md)
>* [Adobe Advertising DSP Connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Informazioni sulla gestione dell&#39;audience](/help/dsp/audiences/audience-about.md)

