---
title: Creare un pubblico riutilizzabile utilizzando l’intelligenza artificiale generativa
description: Scopri come creare tipi di pubblico riutilizzabili in Adobe Advertising DSP utilizzando l’agente di pubblico assistito da intelligenza artificiale. Descrive il pubblico di destinazione in prompt in linguaggio naturale; l’agente suggerisce segmenti di terze parti e crea espressioni di pubblico da utilizzare come target o esclusioni.
feature: DSP Audiences
hidefromtoc: true
hide: true
source-git-commit: 86053178969de362dda0c135ff8c85b9ec9f674e
workflow-type: tm+mt
source-wordcount: '986'
ht-degree: 0%

---

# Creare un pubblico riutilizzabile utilizzando l’intelligenza artificiale generativa

*funzionalità Beta*

*Richieste solo in lingua inglese*

<!-- I thought it was all segment types? -->

<!-- Redo the legacy file to include the new info. It's probably cleanest to keep it as two separate procedures (gen AI and manually) rather than one big, long procedure. -->

Utilizza l’agente del pubblico assistito da AI per generare nuovi tipi di pubblico riutilizzabili utilizzando tutti i segmenti di terze parti disponibili, in base ai requisiti dichiarati. Puoi utilizzare i tipi di pubblico come target o esclusioni per più posizionamenti.

<!-- Later:  Audiences built using generative AI have the indicator [icon] in **[!UICONTROL Audiences] > [!UICONTROL All Audiences]**. -->

>[!NOTE]
>
>Questa funzione è in modalità beta ed è soggetta a modifiche. Assicurati che l’espressione del pubblico generato rappresenti il pubblico desiderato prima di crearlo e utilizzarla per i posizionamenti.

1. Nel menu principale, fare clic su **[!UICONTROL Audiences]** > **[!UICONTROL All Audiences]**.

1. Sopra la tabella dati, fare clic su **[!UICONTROL Create]**.

1. Immettere un **[!UICONTROL Audience Name]** univoco.

1. (Facoltativo) Deselezionare l&#39;opzione su **[!UICONTROL Share with all advertisers in my account]**.

   Quando condividi un pubblico, questo diventa disponibile come target o come esclusione per tutti gli inserzionisti all’interno dell’account. Tuttavia, i singoli segmenti nel pubblico sono disponibili solo per gli utenti a cui i segmenti sono condivisi.

1. Fare clic su **[!UICONTROL Save]**.

1. Creare il pubblico:

   Per gli utenti con autorizzazioni beta, l’opzione IA è l’impostazione predefinita. Per [assemblare autonomamente il pubblico](/help/dsp/audiences/reusable-audience-create.md), fare clic sul pulsante &quot;Passa alla modalità manuale&quot; nella parte inferiore.

   1. Inserisci una o più richieste per descrivere le caratteristiche del pubblico da includere ed escludere. Per inviare ogni richiesta, fare clic su ![Invia richiesta](/help/dsp/assets/submit-prompt.png "Invia richiesta").

      Per ulteriori informazioni, vedere &quot;[Prompt di scrittura](#writing-prompts)&quot; e &quot;[Procedure consigliate per la creazione di un resoconto del pubblico](#audience-brief-best-practices).&quot;

      Quando l’agente di IA trova segmenti rilevanti, crea un’espressione di pubblico in base ai criteri. Chiede inoltre la tua approvazione prima di cercare i segmenti corrispondenti per assemblare il pubblico.

      Facoltativamente, puoi ignorare la richiesta e continuare a specificare altri criteri di pubblico.

   1. Quando l’agente di intelligenza artificiale presenta un’espressione di pubblico che descrive adeguatamente il pubblico, indica all’agente di intelligenza artificiale di procedere con l’assemblaggio del pubblico.

      È possibile immettere &quot;procedere&quot;, &quot;ok&quot;, &quot;ok&quot;, &quot;sì&quot; o un&#39;altra parola simile.

1. (Se necessario) Specificare criteri aggiuntivi. Quando l’agente di intelligenza artificiale presenta un’espressione di pubblico che soddisfa tutti i criteri, indica all’agente di intelligenza artificiale di procedere con l’assemblaggio del pubblico.

1. Quando si è soddisfatti del pubblico assemblato, fare clic su **[!UICONTROL Create]** per creare il pubblico specificato.

   >[!NOTE]
   >
   >In seguito non puoi modificare il pubblico utilizzando l’agente di intelligenza artificiale. Al contrario, [modifica manualmente l&#39;espressione del pubblico](/help/dsp/audiences/reusable-audience-edit.md).

## Scrittura dei prompt {#writing-prompts}

### Cosa deve includere un prompt?

* Utilizza un linguaggio chiaro e descrittivo per descrivere il pubblico target.

  In generale, i prompt non distinguono tra maiuscole e minuscole e la punteggiatura non è necessaria se non per fornire chiarezza.

* Sii specifico e fornisci dettagli su tutte le caratteristiche del pubblico che desideri includere ed eventuali caratteristiche che desideri escludere specificamente. Maggiore è il numero di dettagli forniti, maggiori sono le possibilità di ottenere risultati che soddisfino le tue esigenze.

* Identifica posizioni, tipi di dispositivi e fornitori di dati da includere o escludere.

* Fornisci in alternativa dettagli per perfezionare i criteri e l’espressione del pubblico generato prima di salvare il pubblico.

* Scopri come richiedere tramite sperimentazione.

  L’agente del pubblico non salva automaticamente un’espressione del pubblico generata come pubblico. È possibile salvare un pubblico solo facendo clic sul pulsante [!UICONTROL Create], che si trova all&#39;esterno dell&#39;area di richiesta, in modo da poter annullare le modifiche che non si desidera mantenere.

Consulta &quot;[Procedure consigliate per la creazione di un resoconto del pubblico](#audience-brief-best-practices)&quot; per ulteriori modi per ottimizzare i prompt per i tipi di pubblico.

<!-- I think these are happening later:

DSP uses "smart" defaults based on the user's previous audiences (all user-created audiences or only ones created via AI prompting?)

you can use a predefined prompt (fill in the blanks, and some fields might have selectors where you can choose values)

Over time, DSP XXXX defaults [clarify this]

 onsider starting by asking for a general template, which contains placeholder values that you can replace with your desired values. The default template is something like "Create a xxx with NNN xxx."

you can give thumbs up or down to [what exactly?]. Verify what info is carried over from session to session and what starts from scratch.

-->

### Cosa non puoi includere in un prompt?

* Riferimenti a espressioni di pubblico esistenti.

* Testo in lingue diverse dall&#39;inglese.

### Esempi di risposte dell’agente di IA e come rispondere

Quando l’agente IA necessita di una risposta da parte tua, puoi rispondere utilizzando parole chiave nella richiesta o termini comuni equivalenti.

#### Risposta dell’agente di IA che ti pone una domanda

`If you are okay with the proposed expression, I can start searching third party segments for each of the traits (based on the search filters above), and assemble the matching segments into the audience. Would you like me to proceed?`

La tua risposta affermativa: &quot;procedere&quot;, &quot;ok&quot;, &quot;ok&quot;, &quot;sì&quot;, o un&#39;altra parola simile

Puoi anche ignorare la richiesta e continuare a specificare altri criteri di pubblico.

#### Risposta dell’agente di IA che richiede di scegliere tra più opzioni

```
Would you like to:
1) Proceed with this expression,
2) Get maximum reach alternatives, or
3) Modify the expression manually?
```

Risposta: `1`, `proceed`, `2`, `maximum reach` e così via.

Puoi anche ignorare la richiesta e continuare a specificare altri criteri di pubblico.

## Procedure consigliate per la creazione di un resoconto del pubblico {#audience-brief-best-practices}

Un resoconto del pubblico è un resoconto strategico che definisce il pubblico target di una campagna. Un resoconto ben strutturato aiuta l’agente del pubblico di DSP a identificare i segmenti più rilevanti per assemblare il pubblico di destinazione.

### Componenti essenziali per un resoconto efficace del pubblico

#### Attributi del pubblico

Includi il maggior numero possibile di tipi di attributi dall’elenco seguente nella tua descrizione. Specifica gli attributi da escludere.

<!-- What about these:

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

### Esempio di resoconto ben strutturato del pubblico per una campagna di prospezione

Di seguito è riportato un esempio di una descrizione dettagliata del pubblico per una campagna di sensibilizzazione e sperimentazione per un servizio di abbonamento a un kit per un pasto premium:

`The target audience consists of adults aged 28-45 (60% female, 40% male) with household incomes of $85K or more, college-educated professionals living in the USA. Psychographically, they are health-conscious individuals who value convenience and quality, aspire to be home cooks, and are food enthusiasts seeking better work-life balance. They actively engage with cooking and culinary content, follow health and wellness trends, shop at farmers markets, and prefer organic foods. Behaviorally, they are online grocery shoppers who use subscription services, dine out at restaurants 2+ times per week, and engage with food content on social media. They are currently in-market for meal planning solutions and food subscription services, with many focused on weight management and healthy eating programmes. The audience includes young families with children and dual-income households, as well as career-focused professionals. The brief excludes current subscribers and those following vegan/vegetarian diets as the initial launch focuses on protein-centric meal plans.`

>[!MORELIKETHIS]
>
>* [Duplica un pubblico riutilizzabile](/help/dsp/audiences/reusable-audience-duplicate.md)
>* [Modifica un pubblico riutilizzabile](/help/dsp/audiences/reusable-audience-edit.md)
>* [Visualizza dettagli su un pubblico riutilizzabile](/help/dsp/audiences/reusable-audience-view-details.md)
>* [Condividi un pubblico riutilizzabile](/help/dsp/audiences/reusable-audience-share.md)
>* [Esporta un pubblico riutilizzabile](/help/dsp/audiences/reusable-audience-export.md)
>* [Copia negli Appunti la chiave del segmento per un pubblico riutilizzabile](/help/dsp/audiences/reusable-audience-clipboard.md)
>* [Eliminare un pubblico riutilizzabile](/help/dsp/audiences/reusable-audience-delete.md)
