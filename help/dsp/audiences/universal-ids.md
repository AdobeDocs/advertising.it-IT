---
title: Supporto per l’attivazione di ID universali
description: Scopri come importare i segmenti ID universali, creare segmenti personalizzati per monitorare gli ID universali e convertire altri identificatori utente nei segmenti di prime parti in ID universali per il targeting senza cookie.
feature: DSP Audiences
exl-id: e238537b-217f-44bb-8a69-8adc83dbdfb9
source-git-commit: c1f4df1d5c3f6b32597f59285f25bf0b9da5fb91
workflow-type: tm+mt
source-wordcount: '1388'
ht-degree: 0%

---

# Supporto per l’attivazione di ID universali

<!-- Once we have CDP support for ID5 and can set up activation via sources, then maybe I can move this info into "About Sources" and "About Audiences." Or maybe make this the go-to page, removing info from those other pages? -->

*Funzione beta*

L’DSP supporta ID universali basati sulle persone per il targeting senza cookie a dispositivo singolo (non tra dispositivi) tra i formati digitali supportati dall’DSP.

* Puoi inviare manualmente i [[!DNL LiveRamp] [!DNL RampIDs]] direttamente all&#39;DSP utilizzando il [!DNL LiveRamp] [!DNL Connect] dashboard. Consulta &quot;[Importare manualmente segmenti autenticati da [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md).&quot;

* L’DSP può acquisire i segmenti di prime parti composti da ID e-mail con hash incorporati nella piattaforma di dati cliente (CDP) e convertirli in [!DNL LiveRamp] [!DNL RampIDs] e [!DNL Unified ID 2.0 (UID2.0)] ID. Per ulteriori informazioni sulle piattaforme dati del cliente supportate, sulle funzioni disponibili per ciascun tipo di ID universale supportato e sui relativi flussi di lavoro, consulta la sezione &quot;[Informazioni sulle origini del pubblico di prime parti](/help/dsp/audiences/sources/source-about.md).&quot;

* Puoi creare segmenti personalizzati che tengono traccia degli utenti associati agli ID universali ID5 esposti agli annunci da dispositivi desktop e mobili e che visitano specifiche pagine web. ID5 utilizza un modello probabilistico per assegnare un ID derivato da vari segnali utente e del browser. Per le istruzioni del caso, vedere &quot;[Creare e implementare un segmento personalizzato](/help/dsp/audiences/custom-segment-create.md).&quot;

* Segmenti di terze parti da [!DNL Eyeota] e alcuni altri fornitori possono includere automaticamente gli ID ID5, oltre agli utenti tracciati dai cookie o dagli ID dispositivo. I dettagli del segmento includono la dimensione per ciascun tipo. Si applica la tariffa d’uso abituale per ciascun segmento, indicata accanto al nome del segmento; non vengono addebitate tariffe aggiuntive per gli ID5.

## Generazione di rapporti per tipo di ID universale

* **Rapporti personalizzati:** I dati su costi, impression, clic, conversione e frequenza per tipo di ID universale sono disponibili nei rapporti personalizzati.

* **[!DNL Analytics]rapporti:** Inserzionisti con [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) che hanno implementato tutti i passaggi richiesti può visualizzare le conversioni view-through per tipo di ID universale in [!DNL Analytics].

  >[!IMPORTANT]
  >
  >Per una corretta attribuzione della conversione, assicurati che gli URL di clickthrough per gli annunci includano sia [ID EF e AMO ID](/help/integrations/analytics/ids.md).

* **Dettagli del segmento:** Per tutti i tipi di segmento, i dettagli del segmento includono la dimensione del pubblico per tipo di ID universale e per tipo di dispositivo tracciato da cookie o ID dispositivo.

## Come indirizzare un pubblico con ID universale nei posizionamenti

>[!NOTE]
>
>Non puoi modificare i tipi di ID di destinazione in un posizionamento live. Se necessario, puoi duplicare un posizionamento live e modificare i tipi di ID di destinazione nel nuovo posizionamento.

In un posizionamento nuovo, pianificato o in pausa, effettuare le seguenti operazioni:

1. In [!UICONTROL Geo-Targeting] , specificare le aree geografiche di destinazione. Ogni partner ID universale consente il targeting degli utenti solo in aree geografiche specifiche e solo i tipi di ID idonei sono disponibili nel [!UICONTROL Targeting] impostazioni.

1. In [!UICONTROL Audience Targeting] eseguire le operazioni seguenti:

   1. In [!UICONTROL Included Audiences] , selezionare il segmento per il quale i dati utente sono stati convertiti in ID universali.

      Se lo desideri, puoi includere altri segmenti.

   1. In [!UICONTROL Targeting] impostazioni:

      1. Seleziona il tipo di ID universale di destinazione.

         L’impostazione include le opzioni &quot;[!UICONTROL Legacy IDs]&quot; e &quot;[!UICONTROL Universal ID],&quot; che può includere le opzioni secondarie &quot;[!UICONTROL ID5],&quot; &quot;[!UICONTROL RampID],&quot; e &quot;[!UICONTROL Unified ID2.0].&quot; I target geografici selezionati determinano le opzioni secondarie disponibili.

         Puoi selezionare entrambi &quot;[!UICONTROL Legacy IDs]&quot; e &quot;[!UICONTROL Universal ID],&quot; ma è possibile selezionare un solo tipo di ID universale per posizionamento. Quando selezioni sia ID legacy che ID universali, viene data la preferenza di offerta agli ID universali.

      1. Se necessario, accettare i termini del contratto di servizio per l&#39;utilizzo degli ID universali.

         Prima di poter convertire i dati in un nuovo tipo ID, un utente nell’account DSP deve accettare i termini del contratto di assistenza. I termini devono essere accettati una sola volta per tipo di ID, per account.

Consulta &quot;[Impostazioni di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md).&quot;

## Best practice per il test e la convalida dei dati

Utilizza le seguenti best practice per [!DNL RampID]segmenti basati su e segmenti basati su ID5, per i quali è disponibile la misurazione Adobe Analytics.

* Circa 24 ore dopo l’attivazione di un segmento, controlla il conteggio degli ID convertiti per il segmento in [!UICONTROL Audiences] > [!UICONTROL All Audiences]. Se il conteggio ID non è previsto, contatta il team dell’account Adobe.

  Consulta &quot;[Cause delle varianze di dati tra ID e-mail e ID universali](#universal-ids-data-variances)&quot; per ulteriori informazioni sulle possibili variazioni dei conteggi dei segmenti.

* Non modificare pacchetti e posizionamenti esistenti. Tuttavia, se non disponi di budget incrementale per testare gli ID universali, riduci i budget originali per finanziare i test.

* Copia i pacchetti e i posizionamenti originali, regola i budget in base alle dimensioni del test, cambia il pubblico da utilizzare [!DNL RampID]Segmenti basati su (per utenti autenticati) o segmenti basati su ID5 (per utenti non autenticati) e verifica che i nuovi pacchetti e posizionamenti utilizzino l’intero budget.

   * Per confrontare le prestazioni dei segmenti universali basati su ID con quelle dei posizionamenti mirati ad altri identificatori di pubblico, come cookie o ID mobile advertising, crea una campagna con un posizionamento separato basato su ID universali e un posizionamento basato su ID legacy.

     Per un test di retargeting completo, esegui il targeting sia dei RampID per gli utenti autenticati che dell’ID5s per gli utenti non autenticati.

     Ottenere le prestazioni migliori non dovrebbe essere il confronto principale. Determina invece quali ID vengono scalati correttamente, il che potrebbe influenzare l’ottimizzazione e le allocazioni di budget in un secondo momento. L’obiettivo a lungo termine è quello di compensare le impression perse e il traffico del sito quando i cookie sono obsoleti.

   * Per confrontare la portata totale del browser, effettua il targeting dei segmenti universali basati su ID e dei segmenti legacy basati su ID nello stesso posizionamento. Utilizza le stesse impostazioni della campagna del caso d’uso precedente, tranne per il fatto che non è necessario dividere il budget della campagna.

     La preferenza di offerta viene data agli ID universali, ma gli ID legacy ricevono le offerte quando gli ID universali non sono disponibili. Assicurati di confrontare la portata in diversi browser (tra cui Chrome, Safari e Mozilla).

     >[!NOTE]
     >
     >Il limite di frequenza si applica a un singolo ID. Quando un utente ha più tipi di ID, puoi raggiungerlo più di quanto previsto.

* Ricorda che la portata dei segmenti di pubblico autenticati è naturalmente inferiore a quella dei segmenti basati su cookie e che l’utilizzo di opzioni di targeting aggiuntive riduce ulteriormente la portata. Presta attenzione all’utilizzo del targeting granulare, in particolare unendo più target con istruzioni AND.

## Cause delle varianze di dati tra ID e-mail e ID universali {#universal-ids-data-variances}

* ID e-mail con hash tradotti in ID5:

  Il modello probabilistico ha una varianza di errore di +/- 5%. Ciò significa che può sovrastimare o sottostimare il conteggio del pubblico del 5%.

* ID e-mail con hash tradotti in [!DNL RampIDs]:

   * Quando più profili utilizzano lo stesso ID e-mail, il conteggio dei segmenti DSP può essere inferiore al conteggio dei profili nella piattaforma di dati del cliente. Ad esempio, in Adobe Photoshop puoi creare un account aziendale e un account personale utilizzando un singolo ID e-mail. Ma se entrambi i profili appartengono allo stesso segmento, allora i profili vengono mappati su un ID e-mail e in modo corrispondente su uno [!DNL RampID].

   * A [!DNL RampID] può essere aggiornato a un nuovo valore. Se [!DNL LiveRamp] non riconosce un ID e-mail o non può mapparlo su un [!DNL RampID] nel proprio database, quindi assegna un nuovo [!DNL RampID] all’ID e-mail. In futuro, quando potranno mappare l’ID e-mail su un altro [!DNL RampID] oppure possono raccogliere ulteriori informazioni sullo stesso ID e-mail, aggiornano il [!DNL RampID] a un nuovo valore. [!DNL LiveRamp] si riferisce a questa azione come aggiornamento da un &quot;derivato&quot; [!DNL RampID] a un &quot;mantenuto&quot; [!DNL RampID]. Tuttavia, l’DSP non riceve mappature tra derivato e mantenuto [!DNL RampIDs] e quindi non può rimuovere la versione precedente della RampID dal segmento DSP. In questo caso, il conteggio dei segmenti può essere maggiore del conteggio dei profili.

     Esempio: un utente accede a [!DNL Adobe] e visita la pagina Photoshop. Se [!DNL LiveRamp] non dispone di informazioni esistenti sull’ID e-mail, quindi gli assegnano un derivato [!DNL RampID], diciamo D123. Quindici giorni dopo, l’utente visita la stessa pagina, ma [!DNL LiveRamp] ha aggiornato il [!DNL RampID] durante tali 15 giorni e ha riassegnato il [!DNL RampID] a M123. Anche se il segmento &quot;Photoshop Enthusiast&quot; della piattaforma di dati cliente ha un solo ID e-mail per l’utente, il segmento DSP ha due RampID: D123 e M123.

## Risoluzione dei problemi

Se non visualizzi il numero di utenti o se le dimensioni del pubblico sono basse, verifica quanto segue:

* Se usa [!DNL Flashtalking] o [!DNL Google Campaign Manager 360] annunci, quindi accertati che agli URL di click-through degli annunci siano state aggiunte le macro corrette. Vedere le macro per [[!DNL Flashtalking] annunci](/help/integrations/analytics/macros-flashtalking.md) e [[!DNL Google Campaign Manager 360] annunci](/help/integrations/analytics/macros-google-campaign-manager.md).

* Assicurati che sul tuo sito web sia implementato il codice corretto e universale specifico per il partner ID, in modo che corrisponda agli eventi nel sito e alle esposizioni degli annunci. Utilizzare [!DNL LiveRamp] o [!DNL ID5] se necessario.

* (Per [!DNL RampIDs] e [!DNL UID 2.0] ID) Assicurati che il tuo [L’origine dati dell’DSP è configurata correttamente](/help/dsp/audiences/sources/source-settings.md)e che i conteggi degli utenti siano compilati per i segmenti di pubblico generati.

* Se la portata è inferiore a quanto previsto, controlla che la logica del segmento di pubblico non sia troppo granulare.

Se non riesci a risolvere il problema, contatta il team del tuo account Adobe.

>[!MORELIKETHIS]
>
>* [Creare un’origine di pubblico per attivare i tipi di pubblico con ID universale](/help/dsp/audiences/sources/source-create.md)
>* [Converti ID utente da [!DNL Adobe Real-Time CDP] agli ID universali](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Converti ID utente da [!DNL Tealium] agli ID universali](/help/dsp/audiences/sources/source-tealium.md)
>* [Creare e implementare un segmento personalizzato](/help/dsp/audiences/custom-segment-create.md)
>* [Importare manualmente segmenti autenticati da [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Informazioni su Gestione dell&#39;audience](/help/dsp/audiences/audience-about.md)
>* [Impostazioni di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md)

<!--
>* [Convert User IDs from [!DNL Optimizely] to Universal IDs](/help/dsp/audiences/sources/source-optimizely.md)
-->
