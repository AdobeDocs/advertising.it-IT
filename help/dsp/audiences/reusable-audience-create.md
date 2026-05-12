---
title: Creare un pubblico riutilizzabile
description: Scopri come creare tipi di pubblico riutilizzabili costituiti da segmenti di pubblico e altri tipi di pubblico salvati. Facoltativamente, utilizza un agente di pubblico assistito da intelligenza artificiale descrivendo il pubblico di destinazione in prompt in linguaggio naturale; l’agente suggerisce segmenti di terze parti e crea espressioni di pubblico da utilizzare come target o esclusioni.
feature: DSP Audiences
exl-id: 5f4a0abb-c285-4452-a6c3-a91d5281df9b
TQID: https://experienceleague.adobe.com/KhAxVTvMx4yBz3tfDtng3nOur2IodZAFFHMUQM1lKhQ
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: a4b509995f362ed81e00485409b0c729b5130e35
workflow-type: tm+mt
source-wordcount: 1667
ht-degree: 0%

---

# Creare un pubblico riutilizzabile

<!-- "Saved audience" is used in UI (where?), but "saved" is a state, not a type. "Reusable audience" sounds better in a description. "Audience template" isn't right, either, since it implies you can edit it on the fly to create a new, different audience. Some other term? -->

Puoi salvare e gestire i tipi di pubblico riutilizzabili, ovvero gruppi di segmenti di pubblico e anche altri tipi di pubblico salvati, che puoi utilizzare come target o esclusioni per più posizionamenti. Crea i tipi di pubblico manualmente o utilizza l’agente del pubblico assistito da intelligenza artificiale per generare nuovi tipi di pubblico riutilizzabili utilizzando tutti i segmenti di prime e terze parti disponibili, in base ai requisiti dichiarati.

>[!NOTE]
>
>(Per gli inserzionisti per i quali DSP converte gli ID e-mail con hash in segmenti RampID LiveRamp) I segmenti RampID di prime parti non collegati a un posizionamento attivo, pianificato o in pausa vengono messi in pausa. Nell’elenco dei segmenti, il segmento viene indicato come &quot;In pausa automatica&quot;.

## Creare manualmente un pubblico riutilizzabile

1. Nel menu principale, fare clic su **[!UICONTROL Audiences]** > **[!UICONTROL All Audiences]**.

1. Sopra la tabella dati, fare clic su **[!UICONTROL Create]**.

1. Nelle impostazioni [!UICONTROL New Audience]:

   1. Immettere un **[!UICONTROL Audience Name]** univoco.

   1. (Facoltativo) Deselezionare l&#39;opzione su **[!UICONTROL Share with all advertisers in my account]**.

      Quando condividi un pubblico, questo diventa disponibile come target o come esclusione per tutti gli inserzionisti all’interno dell’account. Tuttavia, i singoli segmenti nel pubblico sono disponibili solo per gli utenti a cui i segmenti sono condivisi. Ad esempio, se condividi un pubblico contenente segmenti di Adobe Analytics con un inserzionista che non è mappato allo stesso account [!DNL Analytics], il segmento non viene visualizzato in anteprima nel pubblico per tale inserzionista. Solo i segmenti disponibili per l’inserzionista vengono visualizzati in anteprima nel pubblico.

   1. Fare clic su **[!UICONTROL Save]**.

1. Fare clic sul pulsante **[!UICONTROL Switch to manual mode]** nel pannello di destra.

   L’opzione IA è l’impostazione predefinita.

1. Creare il pubblico:

   >[!NOTE]
   >
   >Mentre generi il pubblico, nel pannello a destra vengono aggiornati dettagliati [dati sulle dimensioni del pubblico](audience-about.md)

   * Per creare manualmente la logica del segmento, utilizzando i segmenti disponibili nelle schede [[!UICONTROL Third Party Segments], [!UICONTROL First Party Segments], [!UICONTROL Adobe Segments], [!UICONTROL Custom Segments] e [!UICONTROL Saved Audiences]](audience-settings.md), eseguire le operazioni seguenti.

      * (Facoltativo) Cerca un nome di segmento, una descrizione o un percorso.

        I risultati della ricerca includono segmenti basati sui termini esatti utilizzati. Quando si inseriscono più termini, tutti i termini devono essere trovati per un segmento.

      * Per aggiungere il primo segmento, individualo nel pannello a sinistra e seleziona la casella di controllo accanto al nome del segmento.

      * Per aggiungere un segmento a un gruppo di segmenti esistente:

         1. Fai clic sul gruppo di segmenti nel pannello di destra.

         1. (Facoltativo) Modificare la logica del gruppo in *[!UICONTROL Include Any]*, *[!UICONTROL Include All]* o *[!UICONTROL Exclude All]*, in base alle esigenze.

            *[!UICONTROL Exclude All]* non è disponibile per il primo gruppo di segmenti. Per un pubblico che include solo esclusioni, crea questo pubblico come *[!UICONTROL Include Any]* e quindi, all&#39;interno di un posizionamento, seleziona tale pubblico dal menu Tipi di pubblico esclusi.

         1. Individua il nuovo segmento nel pannello a sinistra e seleziona la casella di controllo accanto al nome del segmento.

            Il gruppo di segmenti viene aggiornato automaticamente con il nuovo segmento.

      * Per aggiungere un nuovo gruppo di segmenti:

         1. Fai clic su **[!UICONTROL + New Group]** nel pannello di destra.

            1. (Facoltativo) Modificare la logica tra il gruppo precedente e il nuovo gruppo in *[!UICONTROL And]* o *[!UICONTROL Or]*, in base alle esigenze.

            1. Individuate i segmenti per il nuovo gruppo nel pannello a sinistra e selezionate le caselle di controllo accanto ai nomi dei segmenti.

            1. (Facoltativo) Modificare la logica del gruppo in *[!UICONTROL Include Any]*, *[!UICONTROL Include All]* o *[!UICONTROL Exclude All]*, in base alle esigenze.

   * Per utilizzare la logica dei segmenti da un pubblico esistente:

      1. Copia la logica del segmento dal pubblico esistente in uno dei seguenti modi:

         * Nella visualizzazione Tutti i tipi di pubblico, posizionare il cursore sulla riga del pubblico e quindi fare clic su **[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]**.

         * Nelle impostazioni per il pubblico esistente, nella parte superiore del pannello di logica del segmento, fai clic su **[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]**.

         * In un editor di testo, crea manualmente la logica del segmento utilizzando ID segmento alfanumerici e [sintassi booleana](audience-segment-logic-syntax.md) e copiala negli Appunti.

      1. Fare clic su **[!UICONTROL paste in an audience rule to begin building]**, incollare la logica del segmento esistente nel campo di input, quindi fare clic su **[!UICONTROL Apply]**.

         >[!NOTE]
         >
         >Se il pubblico include già una logica di segmento, l’operazione Incolla nella logica Nuovo segmento sovrascrive la logica esistente.

1. Fare clic su **[!UICONTROL Create]**.

## Creare un pubblico riutilizzabile utilizzando l’intelligenza artificiale generativa

*funzionalità Beta*

*Supporto solo per la lingua inglese*

>[!NOTE]
>
>Questa funzione è in modalità beta ed è soggetta a modifiche. Assicurati che l’espressione del pubblico generato rappresenti il pubblico desiderato prima di crearlo e utilizzarla per i posizionamenti.

<!-- Later:  Audiences built using generative AI have the indicator [icon] in **[!UICONTROL Audiences] > [!UICONTROL All Audiences]**. -->

1. Nel menu principale, fare clic su **[!UICONTROL Audiences]** > **[!UICONTROL All Audiences]**.

1. Sopra la tabella dati, fare clic su **[!UICONTROL Create]**.

1. Nelle impostazioni [!UICONTROL New Audience]:

   1. Immettere un **[!UICONTROL Audience Name]** univoco.

   1. (Facoltativo) Deselezionare l&#39;opzione su **[!UICONTROL Share with all advertisers in my account]**.

      Quando condividi un pubblico, questo diventa disponibile come target o come esclusione per tutti gli inserzionisti all’interno dell’account. Tuttavia, i singoli segmenti nel pubblico sono disponibili solo per gli utenti a cui i segmenti sono condivisi. Ad esempio, se condividi un pubblico contenente segmenti di Adobe Analytics con un inserzionista che non è mappato allo stesso account [!DNL Analytics], il segmento non viene visualizzato in anteprima nel pubblico per tale inserzionista. Solo i segmenti disponibili per l’inserzionista vengono visualizzati in anteprima nel pubblico.

   1. Fare clic su **[!UICONTROL Save]**.

1. Creare il pubblico:

   1. Inserisci una o più richieste per descrivere le caratteristiche del pubblico da includere ed escludere. Per inviare ogni richiesta, fare clic su ![Invia richiesta](/help/dsp/assets/submit-prompt.png "Invia richiesta").

      Per ulteriori informazioni, vedere &quot;[Prompt di scrittura](#writing-prompts)&quot; e &quot;[Best practice per la creazione di una descrizione del pubblico](#audience-brief-best-practices).&quot;

      Se applicabile, l’agente consiglia filtri di segmento aggiuntivi per aiutarti a creare una descrizione più efficace del pubblico. Puoi accettare o rifiutare i suggerimenti.

      Man mano che l’agente del pubblico trova i segmenti rilevanti, crea un’espressione di pubblico booleana basata sui criteri. Chiede inoltre la tua approvazione prima di cercare i segmenti corrispondenti per assemblare il pubblico. Facoltativamente, puoi ignorare la richiesta e continuare a specificare altri criteri di pubblico.

   1. Quando l’agente del pubblico presenta un’espressione del pubblico che descrive adeguatamente il pubblico, chiedi all’agente del pubblico di procedere con l’assemblaggio del pubblico.

      È possibile immettere &quot;procedere&quot;, &quot;ok&quot;, &quot;ok&quot;, &quot;sì&quot; o un&#39;altra parola simile. L’agente elenca tutti i segmenti suggeriti per ogni caratteristica (ad esempio, &quot;Genitori&quot;). Espandi qualsiasi caratteristica per visualizzare i dettagli dei singoli segmenti suggeriti per tale caratteristica.

   1. (Se necessario) Specificare criteri aggiuntivi. Quando l’agente del pubblico presenta un’espressione del pubblico che soddisfa tutti i criteri, indica all’agente del pubblico di procedere con l’assemblaggio del pubblico.

      Per assemblare il pubblico, immetti &quot;procedi&quot;, &quot;ok&quot;, &quot;sì&quot; o un&#39;altra parola simile. L’agente elenca tutti i segmenti suggeriti per ogni caratteristica (ad esempio, &quot;Genitori&quot;). Espandi qualsiasi caratteristica per visualizzare i dettagli dei singoli segmenti suggeriti per tale caratteristica.

1. Quando si è soddisfatti del pubblico assemblato, fare clic su **[!UICONTROL Create]** per creare il pubblico specificato.

   >[!NOTE]
   >
   >In seguito non puoi modificare il pubblico utilizzando l’agente pubblico. Al contrario, [modifica manualmente l&#39;espressione del pubblico](/help/dsp/audiences/reusable-audience-edit.md).

### Nozioni di base sui prompt di scrittura {#writing-prompts}

<!-- Change heading level for this whole section to fit under AI procedure -->

#### Cosa deve includere un prompt?

* Utilizza un linguaggio chiaro e descrittivo per descrivere il pubblico target.

   * Puoi immettere frasi complete o solo una stringa di caratteristiche. La punteggiatura non è necessaria tranne quando necessario per maggiore chiarezza.

   * In generale, i prompt non distinguono tra maiuscole e minuscole.

   * L’agente del pubblico riconosce i sinonimi più comuni.

* Sii specifico e fornisci dettagli su tutte le caratteristiche del pubblico che desideri includere ed eventuali caratteristiche che desideri escludere specificamente. Maggiore è il numero di dettagli forniti, maggiori sono le possibilità di ottenere risultati che soddisfino le tue esigenze.

* Identifica posizioni, tipi di dispositivi e fornitori di dati da includere o escludere.

* Fornisci in alternativa dettagli per perfezionare i criteri e l’espressione del pubblico generato prima di salvare il pubblico.

* Scopri come richiedere tramite sperimentazione.

  Se il prompt non è chiaro, l’agente del pubblico richiederà solo un altro prompt, quindi puoi riprovare.

  L’agente del pubblico non salva automaticamente un’espressione del pubblico generata come pubblico. È possibile salvare un pubblico solo facendo clic sul pulsante [!UICONTROL Create], che si trova all&#39;esterno dell&#39;area di richiesta, in modo da poter annullare le modifiche che non si desidera mantenere.

Consulta &quot;[Best practice per la creazione di una descrizione del pubblico](#audience-brief-best-practices)&quot; per ulteriori modi per ottimizzare i prompt per i tipi di pubblico.

<!--
Consider starting by asking for what you should include.

you can give thumbs up or down to [what exactly?].

Verify what info is carried over from session to session and what starts from scratch.

-->

#### Cosa non puoi includere in un prompt?

* Riferimenti a espressioni di pubblico esistenti.

* Testo in lingue diverse dall&#39;inglese.

#### Esempi di risposte dell’agente del pubblico e come rispondere

Quando l’agente del pubblico necessita di una risposta da parte tua, puoi rispondere utilizzando parole chiave nella richiesta o sinonimi comuni.

#### L’agente del pubblico ti pone una domanda

`If you are okay with the proposed expression, I can start searching segments for each of the traits (based on the search filters above), and assemble the matching segments into the audience. Would you like me to proceed?`

La tua risposta affermativa: &quot;procedere&quot;, &quot;ok&quot;, &quot;ok&quot;, &quot;sì&quot;, o un&#39;altra parola simile

Puoi anche ignorare la richiesta e continuare a specificare altri criteri di pubblico.

##### L’agente del pubblico ti chiede di scegliere tra più opzioni

`Would you like to:`
`1) Proceed with this expression,`
`2) Get maximum reach alternatives, or`
`3) Modify the expression manually?`

Risposta: `1`, `proceed`, `2`, `maximum reach` e così via.

Puoi anche ignorare la richiesta e continuare a specificare altri criteri di pubblico.

### Best practice per la creazione di una descrizione del pubblico {#audience-brief-best-practices}

Un resoconto del pubblico è un resoconto strategico che definisce il pubblico target di una campagna. Un resoconto ben strutturato aiuta l’agente del pubblico di DSP a identificare i segmenti più rilevanti per assemblare il pubblico di destinazione.

#### Componenti essenziali di un’efficace descrizione del pubblico

Includi il maggior numero possibile di tipi di attributi di pubblico dall’elenco seguente nella tua descrizione. Specifica gli attributi da escludere.

<!--
 What about these:

* Device specifications
* Presence in audiences from specific third-party data providers
* Presence of a universal ID
* Target cost per thousand (CPM) impressions or a total target cost

-->

* **Dati demografici**

  Include attributi come fascia di età, genere, stato civile, composizione della famiglia (dimensione della famiglia, presenza di bambini, famiglie multigenerazionali).

* **Indicatori socioeconomici**

  Stabilisce la capacità finanziaria attraverso le fasce di reddito familiare (HHI), il livello di istruzione, la qualifica professionale/lavorativa, lo status occupazionale e lo status di proprietà del domicilio.

* **Parametri geografici**

  Definisce l’ambito di ubicazione, compresi paese/paesi, regione (EMEA, APAC, NA), densità di popolazione (urbana/suburbana/rurale).

* **Interessi e affinità**

  Identifica passioni e preferenze come hobby (sport, arti, attività all’aperto), modelli di consumo dei media, affinità tra marchi e attività lifestyle (viaggi, ristoranti, intrattenimento).

* **Psicografie**

  Acquisisce mentalità e valori che includono aspirazioni (ricerca di uno status, miglioramento di se stessi), valori fondamentali (sostenibilità, innovazione, tradizione), tratti della personalità (soggetti che assumono rischi, primi utilizzatori) e motivazioni di acquisto.

* **Segnali comportamentali**

  Azioni osservabili che includono il comportamento d’acquisto (frequenza di acquisto, preferenze del canale, brand loyalty), il comportamento online (visite al sito web, coinvolgimento con i contenuti, attività social media) e il comportamento offline (visite al negozio, partecipazione a eventi, iscrizioni).

* **Intento di mercato**

  Identifica la fattibilità dell’acquisto attraverso le categorie di prodotti/servizi oggetto della ricerca, la tempistica dell’acquisto (immediato, a breve termine, a lungo termine) e gli eventi vita rilevanti che attivano le decisioni di acquisto.

* **Fase vita**

  L&#39;attuale fase comprende la fase della carriera (studente, entry-level, mid-carriera, dirigente, pensionato), la fase della famiglia (sposi, nuovi genitori, nidi vuoti) e le transizioni di vita principali.

#### Esempio di descrizione ben strutturata del pubblico per una campagna di ricerca di potenziali clienti

Di seguito è riportato un esempio di una descrizione dettagliata del pubblico per una campagna di sensibilizzazione e sperimentazione per un servizio di abbonamento a un kit per un pasto premium:

`The target audience consists of adults aged 28-45 (60% female, 40% male) with household incomes of $85K or more, college-educated professionals living in the USA. Psychographically, they are health-conscious individuals who value convenience and quality, aspire to be home cooks, and are food enthusiasts seeking better work-life balance. They actively engage with cooking and culinary content, follow health and wellness trends, shop at farmers markets, and prefer organic foods. Behaviorally, they are online grocery shoppers who use subscription services, dine out at restaurants 2+ times per week, and engage with food content on social media. They are currently in-market for meal planning solutions and food subscription services, with many focused on weight management and healthy eating programmes. The audience includes young families with children and dual-income households, as well as career-focused professionals. The brief excludes current subscribers and those following vegan/vegetarian diets as the initial launch focuses on protein-centric meal plans.`

>[!MORELIKETHIS]
>
>* [Informazioni su Gestione dell&#39;audience](audience-about.md)
>* [Impostazioni pubblico](audience-settings.md)
>* [Sintassi per la logica dei segmenti di pubblico](audience-segment-logic-syntax.md)
>* [Provider di dati di terze parti disponibili](third-party-data-providers.md)
>* [Creare e implementare un segmento personalizzato](custom-segment-create.md)
>* [Crea e implementa un segmento [!UICONTROL CCPA Opt-Out-of-Sale]](ccpa-opt-out-segment-create.md)
>* [Impostazioni posizionamento](/help/dsp/campaign-management/placements/placement-settings.md)
