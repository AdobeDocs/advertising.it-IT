---
title: Informazioni sull’Assistente IA in Advertising DSP
description: Scopri come utilizzare l’assistente di DSP AI per la risoluzione dei problemi relativi a pacchetti e posizionamenti, la generazione di rapporti e la ricerca di aiuto per l’utilizzo del prodotto.
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 8bab50fe8bf737d208d059d89b2592e16bc40c69
workflow-type: tm+mt
source-wordcount: '751'
ht-degree: 0%
---
# Informazioni sull’Assistente IA in Advertising DSP

L’Assistente AI in DSP è un’interfaccia di conversazione che consente di eseguire qualsiasi flusso di lavoro agente disponibile in DSP da una singola chatbox. È possibile creare una nuova attività o richiedere assistenza per continuare un&#39;attività precedente.

La cronologia delle conversazioni viene mantenuta per tutti i flussi di lavoro e ogni conversazione viene automaticamente denominata. Le query non sono condivise con altri utenti.

<!-- Update this:  ![Example of a query and response](/help/dsp/assets/agent-chat-response.png "Example of a query and response") -->

## Flussi di lavoro supportati

I seguenti flussi di lavoro possono aiutarti a svolgere il tuo lavoro in modo più efficace:

<!-- And links to all sections/pages -->

| Funzionalità | Descrizione | Query di esempio | Risposte |
| --- | --- | --- | --- |
| [Risoluzione dei problemi](troubleshooting-agent.md) | Diagnosticare i problemi di prestazioni e consegna per un pacchetto live o un posizionamento selezionato.<ul><li>Solo posizionamenti: esegui la diagnosi di sovraccarico, sottoutilizzo e mancata spesa. L&#39;agente valuta i fattori relativi al ritmo, alle offerte, al targeting e al tetto di budget.</li><li>Solo pacchetti: diagnosticare problemi di prestazioni, tra cui un CPA in aumento o un ROAS in calo. L’agente non diagnostica le metriche di coinvolgimento come CTR, CPC, clic o impression.</li></ul>Ogni conversazione copre una diagnosi per un pacchetto o posizionamento. Dopo aver ricevuto un risultato, avvia una nuova conversazione per diagnosticare un altro problema, pacchetto o posizionamento.<br><br>L&#39;agente non può modificare le impostazioni né creare o modificare campagne o componenti della campagna. Inoltre, non è in grado di diagnosticare pacchetti o posizionamenti sospesi, completati, archiviati o pianificati. | Questioni relative al posizionamento della spesa:<ul><li>Il mio collocamento ha smesso di spendere ieri anche se l&#39;affare è attivo. Perché?</li><li>Perché questo posizionamento è stato sottoutilizzato negli ultimi 5 giorni?</li><li>Siamo a metà del volo e siamo in ritardo. Perché?</li></ul>Problemi relativi alle prestazioni del pacchetto:<ul><li>Perché il CPA è aumentato per questo pacchetto nell&#39;ultima settimana?</li><li>Perché il ROAS è rifiutato per questo pacchetto?</li></ul> | La risposta include fattori che limitano le prestazioni e fornisce consigli per risolvere i problemi. |
| [Informazioni](insights-agent.md) | Ottieni metriche della campagna e rapporti completi senza creare manualmente un rapporto. Puoi porre domande semplici su una metrica specifica, ad esempio spesa o CPA per una campagna, oppure chiedere un rapporto più complesso per una dimensione specifica (ad esempio una singola campagna, posizionamento o pubblico) o tra dimensioni diverse (per raggruppamenti per campagna e inserzionista). Puoi scaricare i risultati come file CSV. | <ul><li>Quanto ha speso [Nome campagna] la settimana scorsa?<li>Quante conversioni ha ottenuto [Nome campagna] questo mese?</li><li>Quali posizionamenti sono in ritardo di oltre il 20%?</li></li>Visualizza il CPA per pacchetto per [Nome campagna]</li></ul> | Vengono visualizzate le prime righe del report, con collegamenti per visualizzare in anteprima il report completo e scaricare il report come file di valori separati da virgola (.csv) di [!DNL Microsoft Excel]. |
| [Ricerca nella documentazione del prodotto](documentation-search.md) | Cerca contenuti concettuali e pratici nella [Guida di Advertising DSP](/help/dsp/home.md) e, per gli inserzionisti con Advertising Creative, nella [Guida di Advertising Creative](/help/creative/home.md). Le risposte si basano solo su ciò che è documentato per questi prodotti in [Experience League](https://experienceleague.adobe.com/it/docs/advertising).<br><br>Chiedi informazioni su gestione campagne, ottimizzazione, gestione dell&#39;audience, offerte, rapporti e altre caratteristiche del prodotto. | <ul><li>Come si allega un annuncio a un posizionamento?</li><li>Quali opzioni di targeting sono disponibili in Adobe DSP?</li><li>Quali sono le conseguenze dell’utilizzo delle diverse opzioni di andamento nelle impostazioni di posizionamento?</li><li>Quali rapporti includono dati a livello di famiglia?</li><li>Come si crea un tag annuncio per un&#39;esperienza [!DNL Creative]?</li></ul> | La risposta include le citazioni in linea e un elenco [!UICONTROL Documentation Sources] espandibile in basso. Fai clic su una citazione o un elenco di fonti per aprire la pagina pertinente.<br><br>La risposta può includere anche domande e suggerimenti per aiutarti a perfezionare la tua query e a trovare ulteriori informazioni. |

## Apri Assistente IA {#ai-assistant-open}

* In alto a destra, fare clic su ![Chat con agenti](/help/dsp/assets/agent-chat.png "Chat con agenti").

## Espandi la chatbox

1. Nella parte superiore della [chatbox](#ai-assistant-open), fai clic su ![Accedi a schermo intero](/help/dsp/assets/fullscreen.png "Accedi a schermo intero") per accedere alla modalità a schermo intero.

1. Per ripristinare la modalità pannello della chatbox, fare clic su **[!UICONTROL < Back>]**.

<!-- 

No ability to narrow down list of child entities for a selected parent as of 10/26/26.

## Submit a query {#query-submit}

1. [Open AI Assistant](#ai-assistant-open).

1. Build the query:

   * To see examples of queries by topic and optionally copy one to use:
   
     1. Click **[!UICONTROL Learn]**, **[!UICONTROL Troubleshoot]**, or **[!UICONTROL Insights]** to expand the section.
     
     1. (Optional) To copy the text of an example query into the input field:
     
        1. Click the example.
        
        1. (Optional) Edit the text to suit your needs. 

   * To enter your own query:
   
     1. (Insights and troubleshooting queries only; optional) To focus your query on a specific dimension value, such as a specific campaign, click ![Mention an entity](/help/dsp/assets/prompt-entity.png "Mention an entity"), select the dimension, and then select the dimension value.
     
        For example, for the dimension [!UICONTROL Campaign], you can select from a list of all your campaigns to report on.
        
        Available dimensions include:
        
        * Campaign entities: [!UICONTROL Campaign], [!UICONTROL Package], [!UICONTROL Placement], [!UICONTROL Ad]
        * The advertiser: [!UICONTROL Advertiser]
        * Advertising Creative entities: [!UICONTROL Experience]
        * Ad targets: [!UICONTROL Audience], [!UICONTROL City], [!UICONTROL Country], [!UICONTROL State], [!UICONTROL DMA], [!UICONTROL Retargeting Pixel], [!UICONTROL Device OS], [!UICONTROL Device Browser], [!UICONTROL Device Type], [!UICONTROL Zip Code]

     1. Enter your query, and then click ![Submit query](/help/dsp/assets/submit.png "Submit query") or press the **Enter** key on your keyboard.
        
   You can ask multiple questions in one message, but only one message at a time. Wait for a response before sending another.

   >[!NOTE]
   >
   >* (Troubleshooting and insight queries) If you don't specify a date range, then the agent selects a reasonable default based on the type of issue. For example, if you ask about campaign metrics without specifying a date range, then the results are for the duration of the campaign.
   >* (Troubleshooting queries) If you have a target CPA in mind, then include it in your query (for example, "diagnose CPA against a target of $50"). If you don't specify one, then the agent uses a default target.

1. If AI Assistant asks for additional information, provide it.

1. (Product documentation queries only; optional) To open a page used as a data source for the response, do either of the following:

   * Click the numbered citation.

   * Click **[!UICONTROL Documentation Sources]** to show a list of all pages cited in the response, and then click the page link.

>[!IMPORTANT]
>
>AI-generated responses may be inaccurate or misleading. Always verify responses and sources before using them for decisions that affect cost or effort.

>[!TIP]
>
>To ask another query that you want to be saved as a separate thread, [start a new conversation](#conversation-new).

## (Insight queries) Download or preview a full report from the chatbox

* To download a copy of the full report, click ![Export](/help/dsp/assets/download.png "Export").

   The file is downloaded as a [!DNL Microsoft Excel] comma-separated values file (.csv) according to your browser's normal procedure. The filename is "DSP_Insights_Report_<job_number>."

* To preview the full report in a side panel, click ![Preview](/help/dsp/assets/agent-chat-preview.png "Preview"). To download the report from the preview, click ![Export](/help/dsp/assets/download.png "Export").

   If you download the report, it's downloaded as a [!DNL Microsoft Excel] comma-separated values file (.csv) according to your browser's normal procedure. The filename is "DSP_Insights_Report_<job_number>."

## Start a new conversation {#conversation-new}

Each conversation, or query thread, is saved separately so you can distinguish between your previous conversations.

1. At the top of the [chatbox](#ai-assistant-open), click ![Start a new conversation](/help/dsp/assets/new-selection.png "Start a new conversation").

1. [Submit a query](#query-submit).

 -->

<!--

## Work with previous conversations

### List previous conversations

1. At the top of the [chatbox](#ai-assistant-open), click ![Threads history](/help/dsp/assets/threads.png "Threads history").

### Open a previous conversation

1. At the top of the [chatbox](#ai-assistant-open), click ![Threads history](/help/dsp/assets/threads.png "Threads history").

1. Click the conversation entry.

To repeat the same topic verbatim, copy the key details into a new conversation. Otherwise, you can ask AI Assistant to repeat a finite task within a specific conversation.

### Rename a previous conversation

1. At the top of the [chatbox](#ai-assistant-open), click ![Threads history](/help/dsp/assets/threads.png "Threads history").

1. Next to the conversation entry, click **[!UICONTROL ...] > [!UICONTROL Rename]**.

1. Edit the conversation name, and then click **[!UICONTROL Save]**.

-->

## Best practice per la scrittura di query e prompt {#writing-queries}

* **Cancella e specifica**. Utilizzare domande complete (&quot;Come effettuare la sottoscrizione a un inventario su richiesta?&quot;), frasi di attività (&quot;Sottoscrivere un inventario su richiesta&quot;) o frasi di argomento (&quot;Inventario su richiesta&quot;).

* **Non combinare diversi tipi di richieste nella stessa query** a meno che non si desideri che vengano archiviate nella stessa conversazione.

* **Includi intervalli di date quando pertinente** per limitare i dati desiderati.

* **Corrispondenza con i termini dell&#39;interfaccia utente** quando possibile per le funzionalità del prodotto (ad esempio &quot;campagne&quot; o &quot;offerte&quot;).

  Per le azioni più comuni, ad esempio &quot;aggiungi&quot;, &quot;allega&quot; o &quot;assegna&quot;, è possibile utilizzare i sinonimi.

* **Aggiungi dettagli** per limitare o ampliare i risultati. Se necessario, perfeziona le domande di follow-up.

* **Non preoccuparti di segni di punteggiatura e maiuscole** tranne quando influiscono sul significato.

>[!MORELIKETHIS]
>
>* [Crea rapporti tramite l&#39;assistente AI](insights-agent.md)
>* [Risolvere i problemi relativi a prestazioni e consegna tramite l&#39;assistente AI](troubleshooting-agent.md)
>* [Crea un pubblico riutilizzabile](/help/dsp/audiences/reusable-audience-create.md)
>* [Cerca la documentazione del prodotto utilizzando l&#39;Assistente AI](documentation-search.md)
>* [Operazioni con le conversazioni precedenti dell&#39;Assistente IA](previous-conversations.md)
