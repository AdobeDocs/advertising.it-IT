---
title: Converti ID utente da [!DNL ActionIQ] a ID universali
description: Scopri come consentire all’DSP di acquisire i  [!DNL ActionIQ]  segmenti di prime parti.
feature: DSP Audiences
source-git-commit: 91b08bf54f067666c9c27949ff740639738887d0
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# Converti ID utente da [!DNL ActionIQ] in ID universali

*funzionalità Beta*

Utilizza l&#39;integrazione DSP con la piattaforma dati cliente [!DNL ActionIQ] per convertire i tuoi indirizzi e-mail con hash in ID universali per annunci pubblicitari mirati.

Sono disponibili <!-- NN --> passaggi per condividere i dati da [!DNL ActionIQ] con DSP:

1. [Crea un&#39;origine pubblico in DSP](#source-create).

1. ?

## Passaggio 1: creare un’origine di pubblico nell’DSP {#source-create}

1. [Crea un&#39;origine pubblico](source-manage.md) per importare i tipi di pubblico nell&#39;account DSP o in un account inserzionista, specificando i [formati ID universali](source-about.md) in cui convertire gli identificatori utente.

1. Dopo aver creato l&#39;origine del pubblico, condividere la chiave del codice sorgente con l&#39;utente [!DNL ActionIQ].

## Passaggio 2:

## Passaggio 3:

1. Verifica nella libreria del pubblico (disponibile quando crei o modifichi un pubblico da [!UICONTROL Audiences] > [!UICONTROL All Audiences] o nelle impostazioni di posizionamento) che il segmento si stia popolando e confronta il numero di ID universali con il numero di indirizzi e-mail con hash originali.

   I segmenti devono essere disponibili nell’DSP entro 24 ore. Dopo che l’DSP ha ricevuto i dati del segmento, il conteggio del pubblico dovrebbe essere visibile entro nove (9) ore. Per informazioni sulle percentuali di traduzione degli ID accettabili e sul motivo per cui i conteggi dei segmenti possono variare, consulta &quot;[Varianze di dati tra ID e-mail e ID universali](#universal-ids-data-variances).&quot;

I segmenti vengono aggiornati ogni 24 ore.

## Risoluzione dei problemi

Per risolvere i problemi relativi al tasso di traduzione e al conteggio degli utenti, consulta &quot;[Supporto per l&#39;attivazione degli ID universali](/help/dsp/audiences/universal-ids.md).&quot;

Per risolvere i problemi relativi alla procedura di conversione, contatta il team dell&#39;account Adobe o `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Informazioni sulle origini del pubblico di prime parti](/help/dsp/audiences/sources/source-about.md)
>* [Gestione delle origini del pubblico per attivare i tipi di pubblico con ID universale](source-manage.md)
>* [Converti ID utente da [!DNL Adobe Real-Time CDP] a ID universali](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Converti ID utente da [!DNL Tealium] a ID universali](/help/dsp/audiences/sources/source-tealium.md)
>* [Informazioni su Gestione dell&#39;audience](/help/dsp/audiences/audience-about.md)
