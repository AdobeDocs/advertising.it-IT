---
title: Risolvere i problemi di prestazioni e consegna tramite l’assistente AI
description: Utilizza l’agente di risoluzione dei problemi dell’Assistente AI di Adobe Advertising DSP per diagnosticare i problemi di spesa, velocità e consegna per i pacchetti e i posizionamenti DSP.
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
source-git-commit: 0f6d32b5409cc95f09d0b0f28cdeee72a7861892
workflow-type: tm+mt
source-wordcount: '808'
ht-degree: 0%
---
# Risolvere i problemi di prestazioni e consegna tramite l’Assistente AI

*funzionalità Beta*

*Supporto solo per la lingua inglese*

L’agente di risoluzione dei problemi di AI Assistant identifica i fattori che limitano le prestazioni dei pacchetti e dei posizionamenti live e fornisce istruzioni dettagliate e raccomandazioni basate sui dati storici per risolvere i problemi. L’agente di risoluzione dei problemi può aiutare a diagnosticare i seguenti tipi di problemi di prestazioni e consegna:

* (Solo posizionamenti) Problemi di spesa, tra cui sovraccarico, sottoutilizzo e mancata spesa. L&#39;agente valuta i relativi fattori di ritmo, offerta, targeting e budget-cap come parte della diagnosi.

* (Solo pacchetti) Problemi di prestazioni, tra cui un CPA in aumento o un ROAS in calo. L’agente non diagnostica le metriche di coinvolgimento come CTR, CPC, clic o impression.

Ogni conversazione copre una singola diagnosi per un singolo pacchetto o posizionamento. Quando l&#39;agente consegna il risultato, inizia una nuova conversazione per porre domande su un problema diverso, su un pacco o su un posizionamento diverso.

L’agente non può modificare le impostazioni, creare o modificare campagne o componenti di campagne, o diagnosticare problemi per un pacchetto o posizionamento in pausa, completato, archiviato o pianificato.

>[!IMPORTANT]
>
>Le risposte generate dall’intelligenza artificiale possono essere imprecise o fuorvianti. Verifica sempre le risposte e le origini prima di utilizzarle per le decisioni che influiscono su costi o sforzi.

## Query di esempio

### Risoluzione dei problemi di spesa per il posizionamento

* Il mio collocamento ha smesso di spendere ieri anche se l&#39;affare è attivo. Perché?

* Perché questo posizionamento è stato sottoutilizzato negli ultimi 5 giorni?

* Siamo a metà del volo e siamo in ritardo. Perché?

### Risoluzione dei problemi relativi alle prestazioni del pacchetto

* Perché il CPA è aumentato per questo pacchetto nell&#39;ultima settimana?

* Perché il ROAS è rifiutato per questo pacchetto?

## Inviare una query dall’Assistente IA

Puoi porre più domande in un messaggio, ma solo un messaggio alla volta. Attendi una risposta prima di inviarne un’altra.

1. In alto a destra, fare clic su ![Chat con agenti](/help/dsp/assets/agent-chat.png "Chat con agenti").

1. Genera la query:

   * Immettere una query personalizzata.

   * Per visualizzare esempi di query, fare clic su **[!UICONTROL Troubleshoot]** per espandere la sezione.

     1. (Facoltativo) Per copiare il testo di una query di esempio nel campo di input:

        1. Fai clic sull’esempio.

        1. (Facoltativo) Modifica il testo in base alle tue esigenze.

   Per ulteriori informazioni sulle query, vedere &quot;[Best practice per la scrittura di query e prompt](ai-assistant-about.md#writing-queries).&quot;

   >[!NOTE]
   >
   >* Se non specifichi un intervallo di date, l’agente seleziona un valore predefinito ragionevole in base al tipo di problema. Ad esempio, se chiedi informazioni sulle metriche della campagna senza specificare un intervallo di date, i risultati si riferiscono alla durata della campagna.
   >* Se hai in mente un CPA target, includilo nella query (ad esempio, &quot;diagnostica il CPA rispetto a un target di 50 $&quot;). Se non ne specifichi una, l’agente utilizza una destinazione predefinita.

1. Fai clic su ![Invia query](/help/dsp/assets/submit-prompt.png "Invia query") o premi il tasto **Invio** sulla tastiera.

1. Se l’Assistente AI richiede ulteriori informazioni, forniscile.

>[!TIP]
>
>Per chiedere informazioni su un problema diverso o su un pacchetto o un posizionamento diverso, [avvia una nuova conversazione](#conversation-new).

## Invia una query dalla visualizzazione [!UICONTROL Packages] o [!UICONTROL Placements]

Puoi porre più domande in un messaggio, ma solo un messaggio alla volta. Attendi una risposta prima di inviarne un’altra.

1. Nel menu principale, fare clic su **[!UICONTROL Campaigns]**.

1. Fai clic sul nome della campagna.

1. Effettua una delle seguenti operazioni:

   * (Per i pacchetti) Nella visualizzazione [!UICONTROL Packages], fare clic su **[!UICONTROL ...]** > **[!UICONTROL Troubleshooting Agent]** accanto al nome del pacchetto.

   * (Per i posizionamenti) Nel sottomenu, fare clic su **[!UICONTROL Placements]**. Accanto al nome del posizionamento, fare clic su **[!UICONTROL ...]** > **[!UICONTROL Troubleshooting Agent]**.

1. Genera la query:

   * Immettere una query personalizzata.

   * Per visualizzare esempi di query, fare clic su **[!UICONTROL Troubleshoot]** per espandere la sezione.

     1. (Facoltativo) Per copiare il testo di una query di esempio nel campo di input:

        1. Fai clic sull’esempio.

        1. (Facoltativo) Modifica il testo in base alle tue esigenze.

   Per ulteriori informazioni sulle query, vedere &quot;[Best practice per la scrittura di query e prompt](ai-assistant-about.md#writing-queries).&quot;

   >[!NOTE]
   >
   >* Se non specifichi un intervallo di date, l’agente seleziona un valore predefinito ragionevole in base al tipo di problema. Ad esempio, se chiedi informazioni sulle metriche della campagna senza specificare un intervallo di date, i risultati si riferiscono alla durata della campagna.
   >* Se hai in mente un CPA target, includilo nella query (ad esempio, &quot;diagnostica il CPA rispetto a un target di 50 $&quot;). Se non ne specifichi una, l’agente utilizza una destinazione predefinita.

1. Fai clic su ![Invia query](/help/dsp/assets/submit-prompt.png "Invia query") o premi il tasto **Invio** sulla tastiera.

1. Se l’Assistente AI richiede ulteriori informazioni, forniscile.

>[!TIP]
>
>Per chiedere informazioni su un problema diverso o su un pacchetto o un posizionamento diverso, [avvia una nuova conversazione](#conversation-new).

## Avvia una nuova conversazione {#conversation-new}

Ogni conversazione (o thread di query) viene salvata separatamente in modo da poter distinguere le conversazioni precedenti.

1. Nella parte superiore della [chatbox](#ai-assistant-open), fai clic su ![Avvia una nuova conversazione](/help/dsp/assets/new-selection.png "Avvia una nuova conversazione").

1. [Invia una query](#query-submit).

## Espandi e riduci a icona la chatbox

1. Nella parte superiore della [chatbox](#ai-assistant-open), fai clic su ![Accedi a schermo intero](/help/dsp/assets/fullscreen.png "Accedi a schermo intero") per accedere alla modalità a schermo intero.

1. Per ripristinare la modalità pannello della chatbox, fare clic su **[!UICONTROL < Back>]**.

>[!MORELIKETHIS]
>
>* [Informazioni sull&#39;Assistente IA in Advertising DSP](ai-assistant-about.md)
>* [Operazioni con le conversazioni precedenti dell&#39;Assistente IA](previous-conversations.md)
