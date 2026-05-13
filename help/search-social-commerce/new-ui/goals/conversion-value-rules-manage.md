---
title: (Nuova interfaccia) Gestisci [!DNL Google Ads] regole valore di conversione
description: Scopri come visualizzare e gestire le regole del valore di conversione  [!DNL Google Ads]  in Search, Social e Commerce.
feature: Conversions
source-git-commit: 1113c9f6ff8446d075dc9b90441f4119eb657598
workflow-type: tm+mt
source-wordcount: '1844'
ht-degree: 0%

---

# (Nuova interfaccia) Gestisci [!DNL Google Ads] regole valore di conversione

*funzionalità Beta*

[!DNL Google Ads] [regole del valore di conversione](https://support.google.com/google-ads/answer/10518330) ti consentono di regolare i valori degli eventi di conversione in base alle informazioni dell&#39;utente, inclusi il tipo di dispositivo, la posizione e il segmento di pubblico. Con Google Smart Bidding puoi utilizzare le regole per le offerte basate sul valore nelle campagne di ricerca, visualizzazione, acquisto e prestazione massima. Per le campagne con strategie di offerta Maximize Conversions (Massimizza conversioni) e Target ROAS, gli algoritmi [!DNL Google Ads] inizieranno a preferire le conversioni con un valore più alto.

Le regole dei valori di conversione a livello di campagna sostituiscono le regole a livello di conto. Quando una conversione soddisfa più regole del valore di conversione, viene applicata solo una delle regole. Di solito viene applicata la regola più specifica, ma consulta la [[!DNL Google Ads] documentazione sulle priorità per i diversi tipi di condizioni della regola](https://support.google.com/google-ads/answer/10520348).

## Visualizzazione e funzionalità di [!UICONTROL Conversion Value Rules]

Search, Social e Commerce sincronizzano automaticamente le regole del valore di conversione dagli account [!DNL Google Ads]. Tutte le regole create nell&#39;interfaccia [!DNL Google Ads] vengono sincronizzate entro 24 ore e sono disponibili nella visualizzazione [!UICONTROL Goals] > [!UICONTROL Conversion Value Rules].

Alcuni account possono gestire le regole del valore di conversione:

* Negli account per i quali vengono tracciate le conversioni a livello del singolo account o della campagna, puoi [creare](#google-conversion-value-rule-create), [modificare](#google-conversion-value-rule-edit) e [modificare lo stato](#google-conversion-value-rule-change-status) delle regole a livello di account e di campagna.

  Gli account possono essere collegati agli account manager [!DNL Google Ads], ma non possono utilizzare il tracciamento delle conversioni tra account diversi (le cui conversioni vengono tracciate in tutti gli account dell&#39;account manager).

* Negli account che utilizzano il tracciamento delle conversioni tra account, le regole a livello di account e di campagna vengono ereditate dall’account manager e sono di sola lettura.

## Regole del valore di conversione con i portfolio Search, Social e Commerce

Quando l&#39;account dell&#39;inserzionista è configurato per caricare gli obiettivi Search, Social e Commerce in [!DNL Google Ads] e si include una campagna che utilizza una regola del valore di conversione in un portfolio con un obiettivo, [!DNL Google Ads] applica la regola del valore di conversione al valore di conversione originale specificato nell&#39;obiettivo. Di conseguenza, i dati di conversione in Search, Social e Commerce sono diversi da quelli in [!DNL Google Ads].

Ad esempio, supponiamo che l’obiettivo utilizzi una singola metrica di conversione &quot;Lead&quot; e dia alle conversioni da dispositivi mobili un peso di 10 e alle conversioni da dispositivi non mobili un peso di 10. Search, Social e Commerce contano un evento da entrambi i tipi di dispositivi come una (1) conversione e attribuiscono il valore di conversione come 10. Tuttavia, supponiamo che una campagna in tale portfolio utilizzi una regola del valore di conversione &quot;Se il dispositivo è mobile, moltiplicalo per 2&quot;. Quando viene tracciato un evento di lead mobili per tale campagna, [!DNL Google Ads] attribuisce anche il conteggio di conversione come uno (1) ma il valore di conversione come (10 x 2) = 20.

Per ulteriori informazioni sulle regole, inclusi i valori di conversione originali prima dell&#39;applicazione delle regole, vedere il report delle regole del valore di conversione [in [!DNL Google Ads]](https://support.google.com/google-ads/answer/10519848).

## Crea una regola del valore di conversione [!DNL Google Ads] {#google-conversion-value-rule-create}

È possibile creare regole del valore di conversione a livello di account e di campagna in [!DNL Google Ads] account per i quali vengono tracciate le conversioni a livello di singolo account o inferiore. Non è possibile creare regole per i conti con conversioni tra conti diversi che vengono tracciati a livello di conto principale.

Ogni regola include fino a due condizioni, nonché l’adeguamento del valore di conversione da applicare quando le condizioni vengono soddisfatte. Tutte le regole in un account devono utilizzare lo stesso tipo di condizioni primarie e (facoltative) secondarie. Ad esempio, se la regola 1 include la condizione primaria &quot;Pubblico&quot; e la condizione secondaria &quot;Posizione&quot;, tutte le altre regole nell’account devono avere la condizione principale &quot;Pubblico&quot;. Quando le altre regole includono una condizione secondaria, deve essere &quot;Posizione&quot;.

Puoi creare più regole a livello di campagna per ogni campagna. Tuttavia, [!DNL Google Ads] non consente ancora di creare nuove regole a livello di account al di fuori dell&#39;editor [!DNL Google Ads] quando esiste già una regola a livello di account. Per creare regole aggiuntive a livello di account, accedere direttamente a [!DNL Google Ads] e utilizzare l&#39;editor [!DNL Google Ads].

**Nota:** le regole del valore di conversione a livello di campagna hanno la precedenza sulle regole a livello di account e a una conversione è possibile applicare una sola regola. Per ulteriori informazioni, vedere [come [!DNL Google Ads] determina quale regola viene applicata a una conversione quando questa soddisfa le condizioni per più regole](https://support.google.com/google-ads/answer/10520348).

1. Nel menu principale, fare clic su **[!UICONTROL Goals]>[!UICONTROL Conversion Value Rules]**.

   Per impostazione predefinita, la scheda **[!UICONTROL Campaign]** è selezionata per mostrare tutte le regole a livello di campagna.

1. (Facoltativo) Per creare una regola a livello di account, fare clic sulla scheda **[!UICONTROL Account]**.

1. Nella barra degli strumenti, fare clic su **[!UICONTROL Create Campaign Rule]** (dalla scheda [!UICONTROL Campaign]) o su **[!UICONTROL Create Account Rule]** (dalla scheda [!UICONTROL Account]).

1. Seleziona la rete di annunci e l’account. Per le regole a livello di campagna, seleziona anche la campagna. Quindi fare clic su **[!UICONTROL Next]**.

1. Configura le [impostazioni della regola di conversione](#google-ads-conversion-value-rule-settings).

   Devi configurare una condizione primaria e una regolazione del valore. Facoltativamente, puoi configurare una condizione secondaria.

   All&#39;interno di una condizione, più destinazioni o esclusioni vengono unite utilizzando l&#39;operatore booleano `OR`, in modo che qualsiasi opzione possa essere soddisfatta per avviare una regolazione del valore. Quando si include una condizione secondaria, la condizione secondaria viene unita alla condizione principale utilizzando l&#39;operatore booleano `ALL`, pertanto entrambe le condizioni devono essere soddisfatte per avviare la regolazione del valore. Esempio: se \[Location is Algeria OR Tunisia\] AND \[Device is Mobile OR Tablet\], aggiungere 1.5.

   **Nota:** tutte le regole in un account devono utilizzare lo stesso tipo di condizioni primarie e (facoltative) secondarie. Ad esempio, se la regola 1 include la condizione primaria &quot;Pubblico&quot; e la condizione secondaria &quot;Posizione&quot;, tutte le altre regole nell’account devono avere la condizione principale &quot;Pubblico&quot;. Quando le altre regole includono una condizione secondaria, deve essere &quot;Posizione&quot;.

1. Fare clic su **[!UICONTROL Review and Save]** per rivedere le impostazioni.

1. Fare clic su **[!UICONTROL Save]**.

## Modifica una regola del valore di conversione [!DNL Google Ads] {#google-conversion-value-rule-edit}

Puoi modificare una regola del valore di conversione in account/campagne per i quali le conversioni vengono tracciate a livello di singolo account o inferiore. Non è possibile modificare una regola per un account con conversioni tra account diversi che vengono tracciate a livello di account principale.

1. Nel menu principale, fare clic su **[!UICONTROL Goals]>[!UICONTROL Conversion Value Rules]**.

   Per impostazione predefinita, la scheda **[!UICONTROL Campaign]** è selezionata per mostrare tutte le regole a livello di campagna.

1. (Facoltativo) Per visualizzare tutte le regole a livello di account, fare clic sulla scheda **[!UICONTROL Account]**.

1. Selezionare la casella di controllo accanto alla regola.

1. Nella barra degli strumenti Azioni in blocco fare clic su (/help/search-social-commerce/assets/edit-new.png &quot;Modifica&quot;).

1. Modifica le [impostazioni della regola di conversione](#google-ads-conversion-value-rule-settings).

   Non è possibile modificare i tipi di condizione per una regola esistente, ma è possibile modificare le condizioni e le regolazioni dei valori.

   Devi configurare una condizione primaria e una regolazione del valore. Facoltativamente, puoi configurare una condizione secondaria.

   **Nota:** se aggiungi una condizione secondaria, deve essere dello stesso tipo di condizione delle altre regole nell&#39;account. Ad esempio, se la regola 1 altre regole nel conto hanno la condizione secondaria &quot;Ubicazione&quot;, quando le altre regole includono una condizione secondaria, la condizione secondaria deve essere &quot;Ubicazione&quot;. Quando si include una condizione secondaria, la condizione secondaria viene unita alla condizione principale utilizzando l&#39;operatore booleano `ALL`, pertanto entrambe le condizioni devono essere soddisfatte per avviare la regolazione del valore.

1. Fare clic su **[!UICONTROL Review and Save]** per rivedere le impostazioni.

1. Fare clic su **[!UICONTROL Save]**.

## Modifica dello stato di una regola del valore di conversione [!DNL Google Ads] {#google-conversion-value-rule-change-status}

Puoi mettere in pausa, attivare o eliminare una regola del valore di conversione negli account e nelle campagne per i quali vengono tracciate le conversioni a livello del singolo account.

1. Nel menu principale, fare clic su **[!UICONTROL Goals]>[!UICONTROL Conversion Value Rules]**.

   Per impostazione predefinita, la scheda **[!UICONTROL Campaign]** è selezionata per mostrare tutte le regole a livello di campagna.

1. (Facoltativo) Per visualizzare tutte le regole a livello di account, fare clic sulla scheda **[!UICONTROL Account]**.

1. Selezionare la casella di controllo accanto a ogni riga da modificare.

1. Nella barra degli strumenti delle azioni in blocco,

   * Per attivare (abilitare) le regole in pausa, fare clic su **[!UICONTROL ...]>[!UICONTROL Activate]**.

   * Per sospendere le regole attive, fare clic su **[!UICONTROL ...]>[!UICONTROL Pause]**.

   * Per eliminare le regole attive o in pausa, fare clic su ![Elimina](/help/search-social-commerce/assets/delete.png "Elimina").

1. Nel messaggio di conferma, fare clic su **[!UICONTROL Confirm]**.

## Impostazioni regola valore di conversione [!DNL Google Ads] {#google-conversion-value-rule-settings}

| Sezione | Parametro | Descrizione |
|---|---|---|
| [!UICONTROL Select Campaign] | [!UICONTROL Network] | La rete di annunci. |
| | [!UICONTROL Account] | L’account di rete dell’annuncio. |
| | [!UICONTROL Campaign] | (Solo regole del valore di conversione a livello di campagna) La campagna pubblicitaria. |
| [!UICONTROL Conditions] > [!UICONTROL Primary Condition] | \[Tipo condizione\] | (Sola lettura per le regole esistenti) Il tipo di condizione che deve essere soddisfatta per attivare una rettifica di valore:<ul><li>*[!UICONTROL Device]:* Per eseguire il targeting di tutti o di tipi di dispositivi specifici.</li><li>*[!UICONTROL Location]:* Per eseguire il targeting per tutti i paesi e i territori oppure per eseguire il targeting ed escludere posizioni specifiche.</li><li>*[!UICONTROL Audiences]:* Per eseguire il targeting di tutti o di tipi di pubblico specifici</li></ul>**Nota:** tutte le regole in un account devono utilizzare lo stesso tipo di condizioni primarie e (facoltative) secondarie. Ad esempio, se la regola 1 include la condizione primaria &quot;Pubblico&quot; e la condizione secondaria &quot;Posizione&quot;, tutte le altre regole nell’account devono avere la condizione principale &quot;Pubblico&quot;. Quando le altre regole includono una condizione secondaria, deve essere &quot;Posizione&quot;. |
| | \[Tipo di condizione\] > [!UICONTROL Device] e [!UICONTROL Device Level] | (Solo condizioni del dispositivo) Quali tipi di dispositivi sono destinati a:<ul><li>*[!UICONTROL All devices]:** Per eseguire il targeting di tutti i tipi di dispositivi.</li><li>*[!UICONTROL Select devices]:* Per specificare uno o più tipi di dispositivi di destinazione: *[!UICONTROL Desktop]:*, *[!UICONTROL Mobile]* e *[!UICONTROL Tablet]:*.</li></ul>All&#39;interno di una condizione, più destinazioni vengono unite utilizzando l&#39;operatore booleano `OR`, in modo che sia possibile soddisfare qualsiasi opzione per avviare la regolazione del valore. Esempio: se \[Device is Mobile OR Tablet\], aggiungere 1.5. |
| | \[Tipo di condizione\] > [!UICONTROL Location] e [!UICONTROL Location Level] | (Solo condizioni di posizione) I target di posizione e le esclusioni:<ul><li>*[!UICONTROL All countries and territories]:* Per eseguire il targeting per tutti i paesi e le posizioni oppure per eseguire il targeting ed escludere posizioni specifiche.</li><li>*[!UICONTROL Enter a location]:* Per eseguire il targeting ed escludere posizioni specifiche.</li></ul><ul><li>Per espandere una posizione o una posizione secondaria, fare clic su `>` dopo il nome.</li><li>Per aggiungere una destinazione, selezionarla una volta per mostrare un segno di spunta verde.</li><li>Per escludere una destinazione, selezionarla una seconda volta per mostrare una **[!UICONTROL X]** rossa.</li><li>Per rimuovere una destinazione o un’esclusione, effettua una delle seguenti operazioni:<ul><li>Fai clic su ![Elimina](/help/search-social-commerce/assets/delete.png "Elimina") accanto all&#39;elemento nella colonna [!UICONTROL Selections].</li><li>Selezionare la destinazione finché non viene visualizzato alcun segno di spunta o [!UICONTROL X].</li></ul></li></ul>All&#39;interno di una condizione, più destinazioni o esclusioni vengono unite utilizzando l&#39;operatore booleano `OR`, in modo che qualsiasi opzione possa essere soddisfatta per avviare una regolazione del valore. Esempio: se \[Location is Algeria OR Tunisia\], aggiungi 1.5. |
| | \[Tipo di condizione\] > [!UICONTROL Audience] e [!UICONTROL Audience Level] | (Solo condizioni di pubblico) Il pubblico è destinato a:<ul><li>*[!UICONTROL All audience segments]:* Per eseguire il targeting di tutti i [!DNL Google Ads] segmenti di pubblico.</li><li>*[!UICONTROL Enter audience segments]:* Per eseguire il targeting di [!DNL Google Ads] segmenti di pubblico specifici.</li></ul><ul><li>Per espandere una categoria o una sottocategoria nei segmenti, fare clic su `>` dopo il nome.</li><li>Per aggiungere una destinazione, selezionarla.</li><li>Per rimuovere una destinazione, deselezionare la destinazione o fare clic su ![Elimina](/help/search-social-commerce/assets/delete.png "Elimina") accanto all&#39;elemento nella colonna [!UICONTROL Selection].</li></ul>All’interno di una condizione, più destinazioni o esclusioni vengono unite utilizzando l’operatore booleano OR, in modo che possa essere soddisfatta qualsiasi opzione per avviare una regolazione del valore. Esempio: se \[Audience is Bargain Travelers OR Family Vacationers\], aggiungi 1.5.<br><br>**Nota:** una volta salvato un target di pubblico, puoi aggiungere altri tipi di pubblico ma non rimuoverli all&#39;esterno dell&#39;editor [!DNL Google Ads]. Se devi rimuovere una destinazione pubblico, accedi direttamente a [!DNL Google Ads] e utilizza l&#39;editor [!DNL Google Ads]. |
| [!UICONTROL Conditions] > [!UICONTROL Secondary Condition] | \[Tipo condizione\] | (Facoltativo; sola lettura per le regole esistenti) Il tipo di condizione che deve essere soddisfatta per attivare una rettifica di valore. Quando si include una condizione secondaria, la condizione secondaria viene unita alla condizione principale utilizzando l&#39;operatore booleano `ALL`, pertanto entrambe le condizioni devono essere soddisfatte per avviare la regolazione del valore. Esempio: se \[Location is Algeria OR Tunisia\] AND \[Device is Mobile OR Tablet\], aggiungere 1.5.<br><br>Per le descrizioni, vedere le voci relative alle condizioni primarie.<br><br>**Nota:** tutte le regole di un account devono utilizzare lo stesso tipo di condizioni primarie e (facoltative) secondarie. Ad esempio, se la regola 1 include la condizione primaria &quot;Pubblico&quot; e la condizione secondaria &quot;Posizione&quot;, tutte le altre regole nell’account devono avere la condizione principale &quot;Pubblico&quot;. Quando le altre regole includono una condizione secondaria, deve essere &quot;Posizione&quot;. |
| [!UICONTROL Value Adjustment] | [!UICONTROL Adjustment Operation] e [!UICONTROL Adjustment Value] | Specificare il tipo di adeguamento, quindi immettere un valore positivo:<ul><li>*[!UICONTROL Add]:* Aggiunge il valore specificato al valore di conversione passato. Il valore deve essere maggiore di zero (0).</li><li>*[!UICONTROL Multiply]:* moltiplica il valore di conversione passato per il valore specificato. Il valore deve essere compreso tra 0,5 e 10.</li></ul> |

<!--
>[!MORELIKETHIS]
>
>* 
-->
