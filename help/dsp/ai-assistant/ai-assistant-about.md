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
source-git-commit: ffe7424d4e225a95b279b06a7df3b85bf0cbcdbf
workflow-type: tm+mt
source-wordcount: '575'
ht-degree: 0%
---
# Informazioni sull’Assistente IA in Advertising DSP

L’Assistente AI in DSP è un’interfaccia di conversazione che consente di eseguire qualsiasi flusso di lavoro agente disponibile in DSP da una singola chatbox. È possibile creare una nuova attività o richiedere assistenza per continuare un&#39;attività precedente.

La cronologia delle conversazioni viene mantenuta per tutti i flussi di lavoro e ogni conversazione viene automaticamente denominata. Le query non sono condivise con altri utenti.

<!-- Update this:  ![Example of a query and response](/help/dsp/assets/agent-chat-response.png "Example of a query and response") -->

## Flussi di lavoro supportati

I seguenti flussi di lavoro possono aiutarti a svolgere il tuo lavoro in modo più efficace:

<!-- And links to all sections/pages -->

| Funzionalità | Descrizione | Risposte |
| --- | --- | --- |
| [Risoluzione dei problemi](troubleshooting-agent.md) | (Funzione Beta) Diagnostica i problemi di prestazioni e consegna per un pacchetto live o un posizionamento selezionato.<ul><li>Solo posizionamenti: esegui la diagnosi di sovraccarico, sottoutilizzo e mancata spesa. L&#39;agente valuta i fattori relativi al ritmo, alle offerte, al targeting e al tetto di budget.</li><li>Solo pacchetti: diagnosticare problemi di prestazioni, tra cui un CPA in aumento o un ROAS in calo. L’agente non diagnostica le metriche di coinvolgimento come CTR, CPC, clic o impression.</li></ul>Ogni conversazione copre una diagnosi per un pacchetto o posizionamento. Dopo aver ricevuto un risultato, avvia una nuova conversazione per diagnosticare un altro problema, pacchetto o posizionamento.<br><br>L&#39;agente non può modificare le impostazioni né creare o modificare campagne o componenti della campagna. Inoltre, non è in grado di diagnosticare pacchetti o posizionamenti sospesi, completati, archiviati o pianificati. | La risposta include fattori che limitano le prestazioni e fornisce consigli per risolvere i problemi. |
| [Informazioni](insights-agent.md) | (Funzione Beta) Ottieni metriche della campagna e rapporti completi senza creare manualmente un rapporto. Puoi porre domande semplici su una metrica specifica, ad esempio spesa o CPA per una campagna, oppure chiedere un rapporto più complesso per una dimensione specifica (ad esempio una singola campagna, posizionamento o pubblico) o tra dimensioni diverse (per raggruppamenti per campagna e inserzionista). Puoi scaricare i risultati come file CSV. | Vengono visualizzate le prime righe del report, con collegamenti per visualizzare in anteprima il report completo e scaricare il report come file di valori separati da virgola (.csv) di [!DNL Microsoft Excel]. |
| [Ricerca nella documentazione del prodotto](documentation-search.md) | Cerca contenuti concettuali e pratici nella [Guida di Advertising DSP](/help/dsp/home.md) e, per gli inserzionisti con Advertising Creative, nella [Guida di Advertising Creative](/help/creative/home.md). Le risposte si basano solo su ciò che è documentato per questi prodotti in [Experience League](https://experienceleague.adobe.com/it/docs/advertising).<br><br>Chiedi informazioni su gestione campagne, ottimizzazione, gestione dell&#39;audience, offerte, rapporti e altre caratteristiche del prodotto. | La risposta include le citazioni in linea e un elenco [!UICONTROL Documentation Sources] espandibile in basso. Fai clic su una citazione o un elenco di fonti per aprire la pagina pertinente.<br><br>La risposta può includere anche domande e suggerimenti per aiutarti a perfezionare la tua query e a trovare ulteriori informazioni. |

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
