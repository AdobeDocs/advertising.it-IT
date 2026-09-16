---
title: Diagnosticare i problemi di prestazioni e consegna utilizzando [!UICONTROL Troubleshooting Agent] assistito da IA
description: Scopri come utilizzare l’agente di risoluzione dei problemi assistito da AI per diagnosticare i problemi di spesa, ritmo e consegna per i pacchetti e i posizionamenti di DSP.
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
source-git-commit: 31ddb7928ca4e43132087b73829af55ae6315b0d
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 0%
---
# Diagnosticare i problemi di prestazioni e consegna utilizzando [!UICONTROL Troubleshooting Agent] assistito da IA

[!UICONTROL Troubleshooting Agent] assistito da IA identifica i fattori che limitano le prestazioni e fornisce consigli per risolvere i problemi. [!UICONTROL Troubleshooting Agent] può:

* Informazioni sulla diagnosi dei problemi di prestazioni e consegna per un pacchetto live o un posizionamento selezionato:

  * (Solo posizionamenti) Problemi di spesa, tra cui sovraccarico, sottoutilizzo e mancata spesa. L&#39;agente valuta i relativi fattori di ritmo, offerta, targeting e budget-cap come parte della diagnosi.

  * (Solo pacchetti) Problemi di prestazioni, tra cui un CPA in aumento o un ROAS in calo. L’agente non diagnostica le metriche di coinvolgimento come CTR, CPC, clic o impression.

  Ogni conversazione copre una singola diagnosi per un singolo pacchetto o posizionamento. Quando l&#39;agente consegna il risultato, inizia una nuova conversazione per porre domande su un problema diverso, su un pacco o su un posizionamento diverso.

  L’agente non può modificare le impostazioni, né creare o modificare campagne o componenti di campagne. Inoltre, non è in grado di diagnosticare i problemi relativi a un pacchetto o posizionamento in pausa, completato, archiviato o pianificato.

* Cerca contenuti concettuali e pratici nella [Guida di Advertising DSP](/help/dsp/home.md) e (per gli inserzionisti che utilizzano Advertising Creative) nella [Guida di Advertising Creative](/help/creative/home.md), allo stesso modo dell&#39;[interfaccia di Chat Agile](/help/dsp/agent-chat.md). Puoi chiedere informazioni su gestione campagne, ottimizzazione, gestione dell’audience, offerte, rapporti e altre funzioni del prodotto.

>[!IMPORTANT]
>
>Le risposte generate dall’intelligenza artificiale possono essere imprecise o fuorvianti. Verifica sempre le risposte e le origini prima di utilizzarle per le decisioni che influiscono su costi o sforzi.

## Query di esempio

>[!NOTE]
>
>Non è necessario specificare un intervallo di date. Se non ne includi uno, l&#39;agente seleziona un valore predefinito ragionevole in base al tipo di problema.

### Posizionamenti: problemi di spesa

* Il mio collocamento ha smesso di spendere ieri anche se l&#39;affare è attivo. Perché?

* Perché questo posizionamento è stato sottoutilizzato negli ultimi 5 giorni?

* Siamo a metà del volo e siamo in ritardo. Perché?

### Pacchetti: problemi di prestazioni

* Perché il CPA è aumentato per questo pacchetto nell&#39;ultima settimana?

* Perché il ROAS è rifiutato per questo pacchetto?

>[!TIP]
>
>Se hai in mente un CPA target, includilo nella query (ad esempio, &quot;diagnostica il CPA rispetto a un target di 50 $&quot;). Se non ne specifichi una, l’agente utilizza una destinazione predefinita.

### Caratteristiche del prodotto:

* Come si crea un posizionamento?

* Quali opzioni di targeting sono disponibili in Adobe DSP?

* Come si allega un annuncio a un posizionamento?

* Quali sono le conseguenze dell’utilizzo delle diverse opzioni di andamento nelle impostazioni di posizionamento?

* Quando dovrei usare ogni tipo di obiettivo di ottimizzazione?

* Perché i posizionamenti programmatici garantiti (PG) non forniscono impression?

* Quali rapporti includono dati a livello di famiglia?

* Qual è la differenza tra un&#39;esperienza con targeting e un&#39;esperienza non con targeting in [!DNL Creative]?

* Come si crea un tag annuncio per un&#39;esperienza [!DNL Creative]?

## Inviare una query per un pacchetto o posizionamento live

Puoi porre più domande in un messaggio, ma solo un messaggio alla volta. Attendi una risposta prima di inviarne un’altra.

1. Nel menu principale, fare clic su **[!UICONTROL Campaigns]**.

1. Fai clic sul nome della campagna.

1. Effettuare una delle seguenti operazioni:

   * (Per i pacchetti) Nella visualizzazione [!UICONTROL Packages], fare clic su **[!UICONTROL ...]** > **[!UICONTROL Troubleshooting Agent]** accanto al nome del pacchetto.

   * (Per i posizionamenti) Nel sottomenu, fare clic su **[!UICONTROL Placements]**. Accanto al nome del posizionamento, fare clic su **[!UICONTROL ...]** > **[!UICONTROL Troubleshooting Agent]**.

1. Immetti la query e fai clic su ![Invia richiesta](/help/dsp/assets/submit-prompt.png "Invia richiesta").

   <!-- For more information, see "[Writing prompts](#writing-prompts)." -->

   Per le query sulle prestazioni e sulla consegna, la risposta include fattori che limitano le prestazioni e fornisce consigli per risolvere i problemi.

   Per le query di documentazione, la risposta include citazioni in linea e un elenco **[!UICONTROL Documentation Sources]** in basso. Possono inoltre essere visualizzate domande e suggerimenti di follow-up.

1. (Solo query di documentazione; facoltativo) Per aprire una pagina utilizzata come origine dati, eseguire una delle operazioni seguenti:

   * Fare clic sulla citazione numerata.

   * Fare clic su **[!UICONTROL Documentation Sources]** per visualizzare un elenco di tutte le pagine citate nella risposta, quindi fare clic sul collegamento della pagina.

1. (Facoltativo) Valuta la risposta utilizzando l’icona delle miniature in alto o in basso.

>[!TIP]
>
>Per chiedere informazioni su un problema diverso o su un pacchetto o un posizionamento diverso, inizia una nuova conversazione.
