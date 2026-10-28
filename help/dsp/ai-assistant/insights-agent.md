---
title: Creare rapporti con l’assistente AI
description: Scopri come utilizzare l’agente di approfondimenti dell’Assistente AI di Adobe Advertising DSP per eseguire query sulle metriche della campagna, generare rapporti e scaricare file CSV.
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
source-wordcount: '594'
ht-degree: 0%
---
# Creare rapporti con l’Assistente AI

*funzionalità Beta*

*Supporto solo per la lingua inglese*

Utilizza l’agente di insights dell’Assistente AI per ottenere metriche e rapporti completi per campagne, componenti della campagna, esperienze Advertising Creative, inserzionisti e destinazioni di annunci senza creare manualmente un rapporto. Puoi porre domande semplici su una metrica specifica, ad esempio spesa o CPA per una campagna, oppure chiedere un rapporto più complesso per una dimensione specifica (ad esempio una singola campagna o pubblico) o tra dimensioni diverse (per raggruppamenti per ogni campagna e inserzionista). Puoi scaricare i risultati come file CSV.

>[!IMPORTANT]
>
>Le risposte generate dall’intelligenza artificiale possono essere imprecise o fuorvianti. Verifica sempre le risposte e le origini prima di utilizzarle per le decisioni che influiscono su costi o sforzi.

## Query di esempio

* Quanto ha speso [Nome campagna] la settimana scorsa?

* Quante conversioni ha ottenuto [Nome campagna] questo mese?

* Visualizza il CPA per pacchetto per [Nome campagna].

* Quali posizionamenti sono in ritardo di oltre il 20%?

* Confronta la spesa netta per tutte le campagne e i pacchetti negli ultimi 15 giorni.

## Inviare una query

Puoi porre più domande in un messaggio, ma solo un messaggio alla volta. Attendi una risposta prima di inviarne un’altra.

1. In alto a destra, fare clic su ![Chat con agenti](/help/dsp/assets/agent-chat.png "Chat con agenti").

1. Genera la query:

   1. Effettuare una delle seguenti operazioni:

      * Immettere una query personalizzata.

      * Per visualizzare esempi di query:

        1. Fare clic su **[!UICONTROL Insights]** per espandere la sezione.

        1. (Facoltativo) Per copiare il testo di una query di esempio nel campo di input:

           1. Fai clic sull’esempio.

           1. (Facoltativo) Modifica il testo in base alle tue esigenze.

   1. (Facoltativo) Per concentrare la query su un valore di dimensione specifico, ad esempio una campagna specifica, è possibile inserire il cursore nel punto in cui si desidera visualizzare il valore di dimensione, fare clic su ![Menziona un&#39;entità](/help/dsp/assets/prompt-entity.png "Menziona un&#39;entità"), selezionare la dimensione, quindi selezionare il valore di dimensione.

      Ad esempio, per la dimensione [!UICONTROL Campaign], puoi selezionare da un elenco di tutte le campagne su cui generare il rapporto.

      Le dimensioni disponibili includono:

      * Entità campagna: [!UICONTROL Campaign], [!UICONTROL Package], [!UICONTROL Placement], [!UICONTROL Ad]
      * Inserzionista: [!UICONTROL Advertiser]
      * Entità Advertising Creative: [!UICONTROL Experience]
      * Destinazioni annuncio: [!UICONTROL Audience], [!UICONTROL City], [!UICONTROL Country], [!UICONTROL State], [!UICONTROL DMA], [!UICONTROL Retargeting Pixel], [!UICONTROL Device OS], [!UICONTROL Device Browser], [!UICONTROL Device Type], [!UICONTROL Zip Code]

   Per ulteriori informazioni sulle query, vedere &quot;[Best practice per la scrittura di query e prompt](ai-assistant-about.md#writing-queries).&quot;

1. Fai clic su ![Invia query](/help/dsp/assets/submit-prompt.png "Invia query") o premi il tasto **Invio** sulla tastiera. Se l&#39;agente richiede informazioni aggiuntive, fornire le informazioni richieste.

   Vengono visualizzate le prime righe del rapporto, con collegamenti per visualizzare in anteprima il rapporto completo e scaricarlo.

   Vengono visualizzate alcune righe del rapporto generato.

>[!TIP]
>
>Per chiedere informazioni su un problema diverso o su un pacchetto o un posizionamento diverso, [avvia una nuova conversazione](#conversation-new).

## Scaricare o visualizzare in anteprima un rapporto completo dalla chatbox

* Per scaricare una copia del report completo, fare clic su ![Esporta](/help/dsp/assets/download.png "Esporta").

  Il file viene scaricato come file con valori separati da virgola (.csv) di [!DNL Microsoft Excel] in base alla normale procedura del browser. Il nome file è &quot;DSP_Insights_Report_&lt;job_number>&quot;.

* Per visualizzare l&#39;anteprima del report completo in un pannello laterale, fare clic su ![Anteprima](/help/dsp/assets/agent-chat-preview.png "Anteprima"). Per scaricare il report dall&#39;anteprima, fare clic su ![Esporta](/help/dsp/assets/download.png "Esporta").

  Se scarichi il report, verrà scaricato come file con valori separati da virgola (.csv) di [!DNL Microsoft Excel] in base alla normale procedura del browser. Il nome file è &quot;DSP_Insights_Report_&lt;job_number>&quot;.

## Avvia una nuova conversazione {#conversation-new}

Ogni conversazione, o thread di query, viene salvata separatamente in modo da poter distinguere le conversazioni precedenti.

1. Nella parte superiore della [chatbox](#ai-assistant-open), fai clic su ![Avvia una nuova conversazione](/help/dsp/assets/new-selection.png "Avvia una nuova conversazione").

1. [Invia una query](#query-submit).

## Espandi e riduci a icona la chatbox

1. Nella parte superiore della [chatbox](#ai-assistant-open), fai clic su ![Accedi a schermo intero](/help/dsp/assets/fullscreen.png "Accedi a schermo intero") per accedere alla modalità a schermo intero.

1. Per ripristinare la modalità pannello della chatbox, fare clic su **[!UICONTROL < Back>]**.

>[!MORELIKETHIS]
>
>* [Informazioni sull&#39;Assistente IA in Advertising DSP](ai-assistant-about.md)
>* [Operazioni con le conversazioni precedenti dell&#39;Assistente IA](previous-conversations.md)
