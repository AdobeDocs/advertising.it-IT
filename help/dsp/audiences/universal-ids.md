---
title: Supporto per l’attivazione di ID universali
description: Scopri come importare i segmenti ID universali, creare segmenti personalizzati per monitorare gli ID universali e convertire altri identificatori utente nei segmenti di prime parti in ID universali per il targeting senza cookie.
feature: DSP Audiences
exl-id: e238537b-217f-44bb-8a69-8adc83dbdfb9
source-git-commit: 8a8f19c7db95c0eda05a3262eeaf4c8a0aeaaa64
workflow-type: tm+mt
source-wordcount: '1500'
ht-degree: 0%

---

# Supporto per l’attivazione di ID universali

<!-- Once we have CDP support for ID5 and can set up activation via sources, then maybe I can move this info into "About Sources" and "About Audiences." Or maybe make this the go-to page, removing info from those other pages? -->

*funzionalità Beta*

L’DSP supporta ID universali basati sulle persone per il targeting senza cookie a dispositivo singolo (non tra dispositivi) tra i formati digitali supportati dall’DSP.

* È possibile inviare manualmente il [[!DNL LiveRamp] [!DNL RampIDs]] autenticato direttamente all&#39;DSP utilizzando il dashboard [!DNL LiveRamp] [!DNL Connect]. Vedi &quot;[Importa manualmente segmenti autenticati da [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md).&quot;

* DSP può acquisire i segmenti di prime parti composti da ID e-mail con hash generati nella tua piattaforma di dati cliente (CDP) e convertirli in [!DNL LiveRamp] [!DNL RampIDs] e [!DNL Unified ID 2.0 (UID2.0)] ID. Per ulteriori informazioni sulle piattaforme dati del cliente supportate, sulle funzionalità disponibili per ogni tipo di ID universale supportato e sui flussi di lavoro correlati, vedi &quot;[Informazioni sulle origini del pubblico di prime parti](/help/dsp/audiences/sources/source-about.md)&quot;.

* Puoi creare segmenti personalizzati che tengono traccia degli utenti associati agli ID universali ID5 esposti agli annunci da dispositivi desktop e mobili e che visitano specifiche pagine web. ID5 utilizza un modello probabilistico per assegnare un ID derivato da vari segnali utente e del browser. Per istruzioni, consulta &quot;[Creare e implementare un segmento personalizzato](/help/dsp/audiences/custom-segment-create.md).&quot;

* I segmenti di terze parti di alcuni fornitori possono includere automaticamente ID universali oltre agli utenti tracciati dai cookie o dagli ID dispositivo. Ad esempio, i segmenti da [!DNL Eyeota] possono includere automaticamente gli ID ID5, mentre i segmenti da [!DNL Lotame] possono includere gli ID UID2.0. I dettagli del segmento includono la dimensione per ciascun tipo. Si applica la tariffa d’uso abituale per ciascun segmento, indicata accanto al nome del segmento; non vengono addebitate tariffe aggiuntive per gli ID5.

## Generazione di rapporti per tipo di ID universale

* **Rapporti personalizzati:** I dati relativi a costo, impression, clic, conversione e frequenza per tipo di ID universale sono disponibili nei rapporti personalizzati.

* **[!DNL Analytics]report:** Gli inserzionisti con [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) che hanno implementato tutti i passaggi richiesti possono visualizzare le conversioni view-through per tipo di ID universale in [!DNL Analytics].

  >[!IMPORTANT]
  >
  >Per una corretta attribuzione della conversione, assicurati che gli URL di clickthrough per gli annunci includano sia l&#39;ID [EF che l&#39;AMO ID](/help/integrations/analytics/ids.md).

* **Dettagli segmento:** Per tutti i tipi di segmento, i dettagli del segmento includono la dimensione del pubblico per tipo di ID universale e per tipo di dispositivo monitorato da cookie o ID dispositivo.

## Come indirizzare un pubblico con ID universale nei posizionamenti

>[!NOTE]
>
>Non puoi modificare i tipi di ID di destinazione in un posizionamento live. Se necessario, puoi duplicare un posizionamento live e modificare i tipi di ID di destinazione nel nuovo posizionamento.

In un posizionamento nuovo, pianificato o in pausa, effettuare le seguenti operazioni:

1. Nella sezione [!UICONTROL Geo-Targeting], specifica le aree geografiche di destinazione. Ogni partner ID universale consente il targeting degli utenti solo in aree geografiche specifiche e solo i tipi di ID idonei sono disponibili nelle impostazioni [!UICONTROL Targeting].

1. Nella sezione [!UICONTROL Audience Targeting] eseguire le operazioni seguenti:

   1. Nell&#39;impostazione [!UICONTROL Included Audiences], selezionare il segmento per il quale i dati utente sono stati convertiti in ID universali.

      Se lo desideri, puoi includere altri segmenti.

   1. Nelle impostazioni [!UICONTROL Targeting]:

      1. Seleziona il tipo di ID universale di destinazione.

         L&#39;impostazione include le opzioni &quot;[!UICONTROL Legacy IDs]&quot; e &quot;[!UICONTROL Universal ID]&quot;, che possono includere le opzioni secondarie &quot;[!UICONTROL ID5]&quot;, &quot;[!UICONTROL RampID]&quot; e &quot;[!UICONTROL Unified ID2.0]&quot;.&quot; I target geografici selezionati determinano le opzioni secondarie disponibili.

         È possibile selezionare sia &quot;[!UICONTROL Legacy IDs]&quot; che &quot;[!UICONTROL Universal ID]&quot;, ma è possibile selezionare un solo tipo di ID universale per posizionamento. Quando selezioni sia ID legacy che ID universali, viene data la preferenza di offerta agli ID universali.

      1. Se necessario, accettare i termini del contratto di servizio per l&#39;utilizzo degli ID universali.

         Prima di poter convertire i dati in un nuovo tipo ID, un utente nell’account DSP deve accettare i termini del contratto di assistenza. I termini devono essere accettati una sola volta per tipo di ID, per account.

Consulta &quot;[Impostazioni posizionamento](/help/dsp/campaign-management/placements/placement-settings.md).&quot;

## Best practice per il test e la convalida dei dati

Utilizza le seguenti best practice per i segmenti basati su [!DNL RampID] e per i segmenti basati su ID5, per i quali è disponibile la misurazione Adobe Analytics.

* Circa 24 ore dopo l&#39;attivazione di un segmento, controlla il conteggio degli ID convertiti per il segmento entro [!UICONTROL Audiences] > [!UICONTROL All Audiences]. Se il conteggio ID non è previsto, contatta il team dell’account Adobe.

  Consulta &quot;[Varianze di dati tra ID e-mail e ID universali](#universal-ids-data-variances)&quot; per ulteriori informazioni sulle possibili variazioni dei conteggi dei segmenti.

* Non modificare pacchetti e posizionamenti esistenti. Tuttavia, se non disponi di budget incrementale per testare gli ID universali, riduci i budget originali per finanziare i test.

* Copia i pacchetti e i posizionamenti originali, regola i budget in base alle dimensioni del test, modifica i tipi di pubblico in modo da utilizzare i segmenti basati su [!DNL RampID] (per gli utenti autenticati) o i segmenti basati su ID5 (per gli utenti non autenticati) e verifica che i nuovi pacchetti e posizionamenti utilizzino l’intero budget.

   * Per confrontare le prestazioni dei segmenti universali basati su ID con quelle dei posizionamenti mirati ad altri identificatori di pubblico, come cookie o ID mobile advertising, crea una campagna con un posizionamento separato basato su ID universali e un posizionamento basato su ID legacy.

     Per un test di retargeting completo, esegui il targeting sia dei RampID per gli utenti autenticati che dell’ID5s per gli utenti non autenticati.

     Ottenere le prestazioni migliori non dovrebbe essere il confronto principale. Determina invece quali ID vengono scalati correttamente, il che potrebbe influenzare l’ottimizzazione e le allocazioni di budget in un secondo momento. L’obiettivo a lungo termine è quello di compensare le impression perse e il traffico del sito quando i cookie sono obsoleti.

   * Per confrontare la portata totale del browser, effettua il targeting dei segmenti universali basati su ID e dei segmenti legacy basati su ID nello stesso posizionamento. Utilizza le stesse impostazioni della campagna del caso d’uso precedente, tranne per il fatto che non è necessario dividere il budget della campagna.

     La preferenza di offerta viene data agli ID universali, ma gli ID legacy ricevono le offerte quando gli ID universali non sono disponibili. Assicurati di confrontare la portata in diversi browser (inclusi Chrome, Safari e Mozilla).

     >[!NOTE]
     >
     >Il limite di frequenza si applica a un singolo ID. Quando un utente ha più tipi di ID, puoi raggiungerlo più di quanto previsto.

* Ricorda che la portata dei segmenti di pubblico autenticati è naturalmente inferiore a quella dei segmenti basati su cookie e che l’utilizzo di opzioni di targeting aggiuntive riduce ulteriormente la portata. Presta attenzione all’utilizzo del targeting granulare, in particolare unendo più target con istruzioni AND.

## Varianze di dati tra ID e-mail e ID universali {#universal-ids-data-variances}

### Livelli accettabili di varianza

Il tasso di conversione degli indirizzi e-mail con hash in ID universali deve essere superiore al 90%; il tasso di traduzione per [!DNL RampIDs] in particolare deve essere del 95% se tutti gli indirizzi e-mail con hash sono univoci. Ad esempio, se invii 100 indirizzi e-mail con hash dalla piattaforma dati del cliente, questi devono essere tradotti in almeno 95 [!DNL RampIDs] o più di altri tipi di ID universali. Un tasso di traduzione più basso può indicare un problema. Per possibili spiegazioni, vedere &quot;[Cause della varianza](#universal-ids-data-variances-causes&quot;.

Per [!DNL RampIDs], contatta il tuo Account Team Adobe per ulteriori indagini se i tassi di traduzione sono inferiori al 70%.

### Cause della varianza {#universal-ids-data-variances-causes}

* ID e-mail con hash tradotti in ID5:

  Il modello probabilistico ha una varianza di errore di +/- 5%. Ciò significa che può sovrastimare o sottostimare il conteggio del pubblico del 5%.

* ID e-mail con hash tradotti in [!DNL RampIDs]:

   * Quando più profili utilizzano lo stesso ID e-mail, il conteggio dei segmenti DSP può essere inferiore al conteggio dei profili nella piattaforma di dati del cliente. Ad esempio, in Adobe Photoshop puoi creare un account aziendale e un account personale utilizzando un singolo ID e-mail. Ma se entrambi i profili appartengono alla stessa persona, allora i profili vengono mappati a un ID e-mail e in modo corrispondente a un [!DNL RampID].

   * È possibile aggiornare [!DNL RampID] a un nuovo valore. Se [!DNL LiveRamp] non riconosce un ID e-mail o non può mapparlo su un [!DNL RampID] esistente nel suo database, assegna un nuovo [!DNL RampID] all&#39;ID e-mail. In futuro, quando sarà possibile mappare l&#39;ID e-mail a un altro [!DNL RampID] o raccogliere ulteriori informazioni sullo stesso ID e-mail, aggiornerà [!DNL RampID] a un nuovo valore. [!DNL LiveRamp] fa riferimento a questa azione come aggiornamento da un [!DNL RampID] &quot;derivato&quot; a un [!DNL RampID] &quot;mantenuto&quot;. Tuttavia, l&#39;DSP non riceve mappature tra [!DNL RampIDs] derivato e mantenuto e pertanto non può rimuovere la versione precedente del RampID dal segmento DSP. In questo caso, il conteggio dei segmenti può essere maggiore del conteggio dei profili.

     Esempio: un utente accede al sito Web [!DNL Adobe] e visita la pagina Photoshop. Se [!DNL LiveRamp] non ha informazioni esistenti sull&#39;ID e-mail, gli assegna un [!DNL RampID] derivato, ad esempio D123. Quindici giorni dopo, l&#39;utente visita la stessa pagina, ma [!DNL LiveRamp] ha aggiornato [!DNL RampID] durante questi 15 giorni e ha riassegnato [!DNL RampID] a M123. Anche se il segmento &quot;Photoshop Enthusiast&quot; della piattaforma di dati cliente ha un solo ID e-mail per l’utente, il segmento DSP ha due RampID: D123 e M123.

## Risoluzione dei problemi

Se non vedi il numero di utenti o se le dimensioni del pubblico sono basse, verifica quanto segue:

* Se utilizzi [!DNL Flashtalking] o [!DNL Google Campaign Manager 360] annunci, accertati che gli URL di click-through degli annunci siano collegati con le macro corrette. Visualizza le macro per [[!DNL Flashtalking] annunci](/help/integrations/analytics/macros-flashtalking.md) e [[!DNL Google Campaign Manager 360] annunci](/help/integrations/analytics/macros-google-campaign-manager.md).

* Assicurati che sul tuo sito web sia implementato il codice corretto e universale specifico per il partner ID, in modo che corrisponda agli eventi nel sito e alle esposizioni degli annunci. Lavora con il tuo rappresentante [!DNL LiveRamp] o [!DNL ID5] come necessario.

* (Per [!DNL RampIDs] e [!DNL UID 2.0] ID) Assicurati che l&#39;origine dati [DSP sia configurata correttamente](/help/dsp/audiences/sources/source-manage.md#source-settings) e che i conteggi degli utenti siano compilati per i segmenti di pubblico generati.

* Se la portata è inferiore a quanto previsto, controlla che la logica del segmento di pubblico non sia troppo granulare.

* Verificare che le impostazioni della campagna, del pacchetto e del posizionamento siano corrette.<!-- wording-->

Se non riesci a risolvere il problema, contatta il team del tuo account Adobe.

>[!MORELIKETHIS]
>
>* [Informazioni sulle origini del pubblico di prime parti](/help/dsp/audiences/sources/source-about.md)
>* [Gestione delle origini del pubblico per attivare i tipi di pubblico con ID universale](/help/dsp/audiences/sources/source-manage.md)
>* [Creare e implementare un segmento personalizzato](/help/dsp/audiences/custom-segment-create.md)
>* [Importa manualmente segmenti autenticati da [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Informazioni su Gestione dell&#39;audience](/help/dsp/audiences/audience-about.md)
>* [Impostazioni posizionamento](/help/dsp/campaign-management/placements/placement-settings.md)
