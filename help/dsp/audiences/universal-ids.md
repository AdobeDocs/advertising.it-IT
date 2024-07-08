---
title: Supporto per l'attivazione di ID universali
description: Scopri informazioni sul supporto per importare i segmenti di ID universali, creare segmenti personalizzati per tenere traccia degli ID universali e convertire altri identificatori utente nei segmenti di prime parti in ID universali per targeting senza cookie.
feature: DSP Audiences
exl-id: e238537b-217f-44bb-8a69-8adc83dbdfb9
source-git-commit: ea50b94ebc6d27fda9c0bd9f61da16750fa58f83
workflow-type: tm+mt
source-wordcount: '1403'
ht-degree: 0%

---

# Supporto per l&#39;attivazione di ID universali

<!-- Once we have CDP support for ID5 and can set up activation via sources, then maybe I can move this info into "About Sources" and "About Audiences." Or maybe make this the go-to page, removing info from those other pages? -->

*Beta funzionalità*

DSP supporta ID universali basati sulle persone per targeting senza cookie, a dispositivo singola (non tra dispositivo) nei formati digitali supportati da DSP.

* È possibile inviare manualmente il [ ] autenticato[!DNL LiveRamp] [!DNL RampIDs]direttamente a DSP utilizzando la [!DNL LiveRamp] [!DNL Connect] dashboard. Consulta &quot;[Importa manualmente i segmenti autenticati da [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)&quot;.

* DSP possibile inserire i segmenti di prime parti, costituiti da ID e-mail con hash creati all&#39;interno della piattaforma CDP (Customer Data Platform) e convertire a [!DNL LiveRamp] [!DNL RampIDs] e [!DNL Unified ID 2.0 (UID2.0)] ID. Per ulteriori informazioni sulle piattaforme di dati dei clienti supportate, sulle funzionalità disponibili per ogni tipo di ID universale supportato e sui flussi di lavoro correlati, vedi &quot;[Informazioni sulle origini](/help/dsp/audiences/sources/source-about.md) del pubblico di prime parti&quot;.

* Puoi creare segmenti personalizzati che tengono traccia degli utenti associati agli ID universali ID5 che sono esposti agli annunci da desktop e dispositivi mobili e che visita pagine web specifiche. ID5 utilizza un modello probabilistico per assegnare un ID derivato da vari segnali utente e segnali browser. Per istruzioni, consulta &quot;[Crea e implementare un segmento](/help/dsp/audiences/custom-segment-create.md) personalizzato&quot;.

* I segmenti di terze parti di alcuni fornitori possono includere automaticamente ID universali oltre agli utenti tracciati da cookie o ID dispositivo. Ad esempio, i segmenti da [!DNL Eyeota] possono includere automaticamente ID ID5 e i segmenti da [!DNL Lotame] possono includere ID UID2.0. I dettagli del segmento includono le dimensioni per ogni tipo. Si applica la tariffa di utilizzo abituale per ciascun segmento, indicata accanto al nome del segmento; non vengono addebitati costi aggiuntivi per gli ID ID5.

## Generazione di rapporti per tipo di ID universale

* **Rapporti personalizzati:** i dati su costi, impression, clic, conversione e frequenza per tipo di ID universale sono disponibili nei rapporti personalizzati.

* **[!DNL Analytics]rapporti:** gli inserzionisti che [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) hanno implementato tutti i passaggi necessari possono visualizzare le conversioni view-through in base al tipo di ID universale in [!DNL Analytics].

  >[!IMPORTANT]
  >
  >Per un corretto attribuzione di conversione, assicurati che gli URL click-through per i tuoi annunci includano sia l&#39;EF [ID che l&#39;AMO ID](/help/integrations/analytics/ids.md).

* **Dettagli segmento:** per tutti i tipi di segmento, i dettagli del segmento includono le dimensioni dell&#39;audience in base al tipo di ID universale e al tipo di dispositivo tracciato dai cookie o dagli ID dispositivo.

## Come Target un pubblico ID universale nei posizionamenti

>[!NOTE]
>
>Non è possibile modificare i tipi di ID con targeting in un posizionamento live. Se necessario, puoi duplicare un posizionamento live e modificare i tipi di ID con target nel nuovo posizionamento.

In un posizionamento nuovo, pianificato o in pausa, eseguire le operazioni seguenti:

1. In questa [!UICONTROL Geo-Targeting] sezione specificare le aree geografiche da destinazione. Ogni partner di ID universale consente di utente targeting solo in aree geografiche specifiche e nelle impostazioni sono disponibili solo tipi [!UICONTROL Targeting] di ID idonei.

1. [!UICONTROL Audience Targeting] Nella sezione eseguire le operazioni seguenti:

   1. Nell&#39;impostazione [!UICONTROL Included Audiences] , seleziona il segmento per il quale i dati utente sono stati convertiti in ID universali.

      Se lo desideri, puoi includere segmenti aggiuntivi.

   1. [!UICONTROL Targeting] Nelle impostazioni:

      1. Seleziona il tipo di ID universale da destinazione.

         L&#39;impostazione include le opzioni &quot;[!UICONTROL Legacy IDs]&quot; e &quot;[!UICONTROL Universal ID]&quot;, che possono includere le opzioni secondarie &quot;[!UICONTROL ID5]&quot;, &quot;[!UICONTROL RampID]&quot; e &quot;[!UICONTROL Unified ID2.0].&quot; Le destinazioni geografiche selezionate determinano le sottoopzioni disponibili.

         È possibile selezionare sia &quot;[!UICONTROL Legacy IDs]&quot; che &quot;[!UICONTROL Universal ID]&quot;, ma è possibile selezionare un solo tipo di ID universale per posizionamento. Quando selezioni sia gli ID precedenti che gli ID universali, la preferenza di offerta viene assegnata agli ID universali.

      1. (Se necessario) Accettare i termini di servizio per l&#39;utilizzo di ID universali.

         Prima di poter convertire i dati a un nuovo tipo di ID, un utente del DSP account deve accettare i termini del contratto di servizio. I termini devono essere accettati una sola volta per tipo di ID, per account.

Consulta &quot;[Posizionamento Impostazioni](/help/dsp/campaign-management/placements/placement-settings.md)&quot;.

## Best practice per il test e la convalida dei dati

Utilizza le seguenti best practice per [!DNL RampID]i segmenti basati su base di e ID5, per i quali è disponibile la misurazione Adobe Analytics.

* Circa 24 ore dopo l&#39;attivazione di un segmento, controllate il conteggio degli ID convertiti per il segmento entro [!UICONTROL Audiences] > [!UICONTROL All Audiences]. Se il numero di ID è imprevisto, contatta il team dell&#39;account Adobe Systems.

  Per ulteriori informazioni su come può variare il conteggio dei segmenti, consulta &quot;[Cause delle varianze dei dati tra ID e-mail e ID](#universal-ids-data-variances) universali&quot;.

* Non modificare i pacchetti e i posizionamenti esistenti. Tuttavia, se non disponi di un budget incrementale per testare gli ID universali, riduci i budget originali per finanziare i test.

* Copia i pacchetti e gli inserimenti originali, regola i budget in base alle dimensioni del test, modifica i tipi di pubblico per utilizzare [!DNL RampID]segmenti basati su (per gli utenti autenticati) o segmenti basati su ID5 (per utenti non autenticati) e verifica che i nuovi pacchetti e posizionamenti spendano l&#39;intero budget.

   * Per confrontare le prestazioni dei segmenti basati su ID universale con le prestazioni dei posizionamenti targeting altri identificatori di pubblico, come cookie o ID mobile advertising, crea una campagna con un posizionamento basato su ID universale separato e un posizionamento basato su ID legacy.

     Per un test di retargeting completo, destinazione sia i RampID per gli utenti autenticati che gli ID5 per gli utenti non autenticati.

     Ottenere le migliori prestazioni non dovrebbe essere il confronto principale. Determina invece quali ID stanno scalando bene, il che potrebbe informare l&#39;ottimizzazione e le allocazioni di budget in un secondo momento. L&#39;obiettivo a lungo termine è quello di recuperare le impressioni e le traffico del sito perse quando i cookie sono obsoleti.

   * Per confrontare la copertura totale dei browser, destinazione nello stesso posizionamento segmenti basati su ID universali e segmenti legacy basati su ID. Utilizza le stesse impostazioni della campagna del caso d&#39;uso precedente, tranne per il fatto che non è necessario suddividere il budget della campagna.

     La preferenza di offerta viene assegnata agli ID universali, ma gli ID legacy ricevono offerte quando gli ID universali non sono disponibili. Assicurati di confrontare la copertura in diversi browser (inclusi Effetto cromatura, Safari e Mozilla).

     >[!NOTE]
     >
     >Il limite di frequenza si applica a un ID individuale. Quando un utente ha più tipi di ID, potresti raggiungere tale utente più del previsto.

* Ricorda che la copertura per i segmenti di pubblico autenticati è naturalmente inferiore alla copertura per i segmenti basati su cookie e che l&#39;utilizzo di opzioni di targeting aggiuntive riduce ulteriormente la tua copertura. Sii prudente nell&#39;utilizzare targeting granulari, in particolare unendo più target con istruzioni AND.

## Cause delle varianze di dati tra ID e-mail e ID universali {#universal-ids-data-variances}

* ID e-mail con hash convertiti in ID ID5:

  Il modello probabilistico ha un varianza di errore di +/- 5%. Ciò significa che può sovrastimare o sottostimare il conteggio del pubblico del 5%.

* ID e-mail con hash tradotti in [!DNL RampIDs]:

   * Quando più profili utilizzano lo stesso ID e-mail, il numero di segmenti DSP può essere inferiore al conteggio dei profili all&#39;interno della piattaforma di dati dei clienti. Ad esempio, in Adobe Photoshop è possibile creare un account aziendale e un account personale utilizzando un unico ID e-mail. Ma se entrambi i profili appartengono alla stessa persona, i profili vengono mappati su un ID e-mail e corrispondentemente su uno [!DNL RampID].

   * A [!DNL RampID] può essere aggiornato a un nuovo valore. Se [!DNL LiveRamp] non riconosce un ID e-mail o non è in grado di mapparlo a un ID e-mail esistente [!DNL RampID] , ne assegna uno nuovo [!DNL RampID] all&#39;ID e-mail. In futuro, quando possono mappare l&#39;ID e-mail a un altro [!DNL RampID] o possono raccogliere ulteriori informazioni sullo stesso ID e-mail, aggiornano il [!DNL RampID] a un nuovo valore. [!DNL LiveRamp]si riferisce a questa azione come aggiornamento da un &quot;derivato&quot; [!DNL RampID] a un &quot;mantenuto&quot;. [!DNL RampID] Tuttavia, DSP non ottiene mappature tra derivato e gestito [!DNL RampIDs] e pertanto non può rimuovere la versione precedente del RampID dal segmento DSP. In questo caso, il conteggio dei segmenti può essere superiore al conteggio del profilo.

     Esempio: un utente accede al [!DNL Adobe] sito Web e visita la pagina Photoshop. Se [!DNL LiveRamp] non dispone di informazioni esistenti sull&#39;ID e-mail, gli assegnano un derivato [!DNL RampID], ad esempio D123. Quindici giorni dopo, il utente visita la stessa pagina, ma [!DNL LiveRamp] ha aggiornato il [!DNL RampID] durante quei 15 giorni e ha riassegnato il [!DNL RampID] a M123. Anche se il segmento della piattaforma di dati cliente &quot;Photoshop Enthusiast&quot; ha un solo ID e-mail per il utente, il segmento DSP ha due RampID: D123 e M123.

## Risoluzione dei problemi

Se non vedi utente conteggi o se le dimensioni del pubblico sono basse, controlla quanto segue:

* Se utilizzi [!DNL Flashtalking] annunci OR [!DNL Google Campaign Manager 360] , assicurati che agli URL click-through dei tuoi annunci vengano aggiunte le macro corrette. Vedere le macro per [[!DNL Flashtalking] annunci](/help/integrations/analytics/macros-flashtalking.md) e [[!DNL Google Campaign Manager 360] annunci](/help/integrations/analytics/macros-google-campaign-manager.md).

* Assicurati che sul tuo sito web sia implementato il codice ID partner specifico per l&#39;ID corretto in modo che corrisponda agli eventi e alle esposizioni annuncio sul sito. Collabora con il tuo [!DNL LiveRamp] rappresentante o [!DNL ID5] rappresentante, in base alle esigenze.

* (Per [!DNL RampIDs] e [!DNL UID 2.0] ID) Assicurati che l&#39;origine [dati DSP sia configurata correttamente](/help/dsp/audiences/sources/source-manage.md#source-settings) e che i conteggi utente siano compilati per i segmenti di pubblico generati.

* Se la copertura è inferiore al previsto, verifica che la logica del segmento di pubblico non sia troppo granulare.

* Assicurati che le impostazioni della campagna, del pacchetto e della posizionamento siano corrette.<!-- wording-->

Se non riesci a risolvere il problema, contatta il team dell&#39;account Adobe Systems.

>[!MORELIKETHIS]
>
>* [Informazioni sulle origini di pubblico di prima parte](/help/dsp/audiences/sources/source-about.md)
>* [Gestire le origini di pubblico per attivare Audiences ID universale](/help/dsp/audiences/sources/source-manage.md)
>* [Crea e implementare un segmento personalizzato](/help/dsp/audiences/custom-segment-create.md)
>* [Importa manualmente i segmenti autenticati da [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Informazioni su Gestione dell&#39;audience](/help/dsp/audiences/audience-about.md)
>* [Posizionamento Impostazioni](/help/dsp/campaign-management/placements/placement-settings.md)
