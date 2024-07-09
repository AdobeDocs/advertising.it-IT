---
title: "Converti ID utente da [!DNL ActionIQ] agli ID universali"
description: "Scopri come consentire all’DSP di acquisire [!DNL ActionIQ] segmenti di prime parti."
feature: DSP Audiences
source-git-commit: 8a8f19c7db95c0eda05a3262eeaf4c8a0aeaaa64
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---

# Converti ID utente da [!DNL ActionIQ] agli ID universali

*Funzione Beta*

Utilizzare l’integrazione DSP con [!DNL ActionIQ] customer data platform per convertire i tuoi indirizzi e-mail con hash in ID universali per annunci pubblicitari mirati.

Ci sono <!-- NN --> passaggi per condividere i dati da [!DNL ActionIQ] con DSP:

1. [Creare un’origine di pubblico in DSP](#source-create).

1. ?

## Passaggio 1: creare un’origine di pubblico nell’DSP {#source-create}

1. [Creare un’origine di pubblico](source-manage.md) per importare tipi di pubblico nel tuo account DSP o in un account inserzionista, specificando [formati ID universali](source-about.md) in cui desideri convertire gli identificatori utente.

1. Dopo aver creato l&#39;origine del pubblico, condividi la chiave del codice sorgente con [!DNL ActionIQ] utente.

1. 
   <!-- ActionIQ-specific step(s) -->

1. Verifica nella libreria del pubblico (disponibile quando crei o modifichi un pubblico da ) [!UICONTROL Audiences] > [!UICONTROL All Audiences] o nelle impostazioni di posizionamento) che il segmento si sta popolando e confrontare il numero di ID universali con il numero di indirizzi e-mail con hash originali.

   I segmenti devono essere disponibili nell’DSP entro 24 ore. Dopo che l’DSP ha ricevuto i dati del segmento, il conteggio del pubblico dovrebbe essere visibile entro nove (9) ore.

   Per informazioni sui tassi accettabili di traduzione degli ID e sul perché i conteggi dei segmenti possono variare, consulta la sezione &quot;[Varianze di dati tra ID e-mail e ID universali](#universal-ids-data-variances).&quot;

   Per assistenza nella risoluzione dei problemi, contatta il team del tuo account di Adobe oppure `adcloud-support@adobe.com`.

I segmenti vengono aggiornati ogni 24 ore.

## Passaggio 2:

>[!MORELIKETHIS]
>
>* [Informazioni sulle origini del pubblico di prime parti](/help/dsp/audiences/sources/source-about.md)
>* [Gestire le origini del pubblico per attivare i tipi di pubblico con ID universale](source-manage.md)
>* [Converti ID utente da [!DNL Adobe Real-Time CDP] agli ID universali](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Converti ID utente da [!DNL Tealium] agli ID universali](/help/dsp/audiences/sources/source-tealium.md)
>* [Informazioni su Gestione dell&#39;audience](/help/dsp/audiences/audience-about.md)
