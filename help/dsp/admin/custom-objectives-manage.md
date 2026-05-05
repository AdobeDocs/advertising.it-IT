---
title: Gestire gli obiettivi personalizzati
description: Scopri come definire gli eventi di successo che consentono di raggiungere gli obiettivi di ottimizzazione a livello di pacchetto.
role: User, Admin
feature: DSP Optimization, DSP Packages
source-git-commit: e2746d58fa512f032a1e4ff851d23876cd63fc93
workflow-type: tm+mt
source-wordcount: '1312'
ht-degree: 0%

---

# Gestire gli obiettivi personalizzati

*Disponibile per gli account DSP collegati ad account Search, Social e Commerce*

Gli obiettivi definiscono gli eventi di successo che un inserzionista imposta per soddisfare i suoi obiettivi aziendali. Gli obiettivi sono disponibili per i pacchetti DSP come [obiettivi personalizzati](/help/dsp/campaign-management/packages/package-settings.md). Ogni pacchetto che utilizza l&#39;obiettivo di ottimizzazione &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"] o &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot; deve includere un obiettivo personalizzato per consentire il raggiungimento dell&#39;obiettivo di ottimizzazione complessivo.

Un obiettivo è costituito dalle metriche (proprietà) da tracciare e ottimizzare e dai relativi pesi di tali metriche. Ciascun obiettivo può includere:

* **[!UICONTROL Goal]metriche**, che rappresentano le metriche di successo principali di un inserzionista. In genere includono i risultati aziendali di base di un pacchetto, ad esempio Ricavi, Lead o Vendite. Ogni obiettivo deve avere almeno una metrica di obiettivo.

* Metriche **[!UICONTROL Assist]facoltative** che assistono, prevedono, precedono o contribuiscono alle metriche dell&#39;obiettivo guida. Alcuni esempi includono le metriche di coinvolgimento, come unità di test e prove.

  Puoi consentire a [!DNL Adobe AI] di assegnare e aggiornare automaticamente gli eventi di assistenza ponderati per massimizzare gli eventi obiettivo. Se preferisci assegnare metriche di assistenza ponderate personalizzate, DSP può facoltativamente consigliare metriche di assistenza basate sui dati sulle prestazioni passati di Adobe Advertising e Adobe Analytics. Puoi scegliere se applicare o meno i consigli.

Tutte le modifiche alle opzioni degli obiettivi vengono registrate a livello di campo e sono elencate in un registro delle modifiche.

>[!PREREQUISITES]
>
>Prima di poter creare gli obiettivi, l’account DSP deve essere collegato a un account Search, Social e Commerce con lo stesso ID organizzazione Adobe Experience Cloud, anche se non sei un cliente Search, Social e Commerce. Se il tuo account DSP non è collegato a un account [!DNL Search, Social, & Commerce], contatta il team del tuo account Adobe.

>[!NOTE]
>
>* Advertising Search, Social e Commerce utilizzano anche gli obiettivi. Ogni portfolio Search, Social e Commerce deve avere un obiettivo in modo che la funzionalità di ottimizzazione possa creare modelli di clic e di ricavo per il portfolio.
>* Puoi utilizzare lo stesso obiettivo per più pacchetti DSP e/o più portfolio Search, Social e Commerce.

## Metriche disponibili

Nei tuoi obiettivi puoi includere uno qualsiasi dei seguenti elementi:

* Metriche tracciate da Adobe Advertising con il [pixel di tracciamento delle conversioni di Adobe Advertising](/help/search-social-commerce/tracking/conversion-tracking-advertising.md).

* (Inserzionisti con [!DNL Adobe Analytics for Advertising]) [Metriche di conversione e coinvolgimento del sito sincronizzate da Adobe Analytics](/help/integrations/analytics/overview.md).

<!-- Do DSP-only clients have these? * [Advertiser-tracked metrics from conversion feed files](/help/search-social-commerce/tracking/conversion-tracking-about.md).  -->

## Stato obiettivo

La visualizzazione [!UICONTROL Settings] > [!UICONTROL Custom Objectives] indica lo stato di ogni obiettivo. I valori possono includere:

* *[!UICONTROL Waiting]*: l&#39;obiettivo è in stato di bozza fino alla generazione dei consigli.

* *[!UICONTROL Active]*: l&#39;obiettivo è salvato e utilizzabile.

## Stato consigli

* *[!UICONTROL Not Initiated]*: non è stato richiesto alcun consiglio.

* *[!UICONTROL Generating]*: generazione dei consigli in corso.

* *[!UICONTROL Ready]*: i consigli sono disponibili per l&#39;applicazione.

* *[!UICONTROL Error]*: impossibile generare i consigli.

## Creare un obiettivo

1. Nel menu principale, fare clic su **[!UICONTROL Settings]>[!UICONTROL Custom Objectives]**.

1. In alto a destra, fare clic su **[!UICONTROL Create]**.

1. Immettere le [impostazioni obiettivo](#custom-objective-settings).

   Quando si sceglie l&#39;offerta automatica, è possibile assegnare proprietà (metriche) all&#39;obiettivo come metriche &quot;[!UICONTROL Goal]&quot;. Per le offerte personalizzate, puoi assegnare le proprietà come metriche &quot;[!UICONTROL Goal]&quot; o &quot;[!UICONTROL Assist]&quot; ponderate, ma devi includere almeno una metrica di obiettivo.

   Le etichette per obiettivi e assistenza non influiscono sull’ottimizzazione. Solo i pesi delle metriche incluse influiscono sull’ottimizzazione.

1. (Obiettivi con offerte personalizzate; facoltativo) Per generare le metriche di assistenza consigliate in base ai dati sulle prestazioni passati, fai clic su **[!UICONTROL Generate]** nella sezione inferiore. In **[!UICONTROL Generate Recommendation]**, fare clic su **[!UICONTROL Generate]**.

   La generazione delle metriche consigliate richiede fino a 20 minuti. Durante la generazione dei consigli, lo stato dell&#39;obiettivo personalizzato è *[!UICONTROL Waiting]*. Una volta generati i consigli, puoi &quot;[visualizzare e applicare gli eventi di assistenza consigliati](#view-apply-recommendations).&quot;

1. (Se non hai generato consigli) In alto a destra, fai clic su **[!UICONTROL Save]**.

Nelle [impostazioni del pacchetto DSP](/help/dsp/campaign-management/packages/package-settings.md) per i pacchetti che utilizzano l&#39;obiettivo di ottimizzazione &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"] o &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot;, il nome dell&#39;obiettivo è ora incluso nell&#39;elenco [!UICONTROL Custom Goals]. Quando si seleziona l&#39;obiettivo come obiettivo personalizzato per un pacchetto, l&#39;elenco [!UICONTROL Conversion Metric] include tutte le metriche dell&#39;obiettivo.

## Modificare una finalità

1. Nel menu principale, fare clic su **[!UICONTROL Settings]>[!UICONTROL Custom Objectives]**.

1. Nella riga fare clic su **...*** > **[!UICONTROL Edit]**.

1. Modificare le [impostazioni obiettivo](#custom-objective-settings).

1. (Quando i consigli sono disponibili; facoltativo) Visualizza e facoltativamente applica le metriche consigliate:

   1. Nella sezione inferiore, fare clic su **[!UICONTROL View Recommendations]**.

   1. Per applicare un consiglio, effettuare una delle seguenti operazioni:

      * Fai clic su **[!UICONTROL Apply]** accanto al consiglio.

      * Modificare manualmente il consiglio, quindi fare clic su **[!UICONTROL Apply]** accanto al consiglio.

   1. Fare clic su **[!UICONTROL Close]** per chiudere l&#39;elenco [!UICONTROL Recommendations].

   Le modifiche diventano effettive dopo la sincronizzazione delle impostazioni delle finalità.

1. (Obiettivi con offerte personalizzate; facoltativo) Per generare metriche di assistenza consigliate in base ai dati sulle prestazioni passati, fai clic su **[!UICONTROL Generate]** nella sezione inferiore. In **[!UICONTROL Generate Recommendation]**, fare clic su **[!UICONTROL Generate]**.

   La generazione delle metriche consigliate richiede fino a 20 minuti. Durante la generazione dei consigli, lo stato dell&#39;obiettivo personalizzato è *[!UICONTROL Waiting]*. Una volta generati i consigli, puoi &quot;[visualizzare e applicare gli eventi di assistenza consigliati](#view-apply-recommendations).&quot;

1. Se non hai generato nuovi consigli, fai clic su **[!UICONTROL Save]** in alto a destra.

## Visualizzare e applicare gli eventi di assistenza consigliati {#view-apply-recommendations}

*Obiettivi con offerte personalizzate*

È possibile visualizzare i consigli e applicarli facoltativamente quando lo stato obiettivo è *[!UICONTROL Active]* e il [!UICONTROL Recommendation Status] è *[!UICONTROL Ready]*.

1. Nel menu principale, fare clic su **[!UICONTROL Settings]>[!UICONTROL Custom Objectives]**.

1. Nella riga fare clic su **...*** > **[!UICONTROL Edit]**.

1. Nella sezione inferiore, fare clic su **[!UICONTROL View Recommendations]**.

1. (Facoltativo) Per applicare un consiglio, effettuate una delle seguenti operazioni:

   * Fai clic su **[!UICONTROL Apply]** accanto al consiglio.

   * Modificare manualmente il consiglio, quindi fare clic su **[!UICONTROL Apply]** accanto al consiglio.

1. Fare clic su **[!UICONTROL Close]** per chiudere l&#39;elenco [!UICONTROL Recommendations].

1. In alto a destra, fare clic su **[!UICONTROL Save]**.

   Le modifiche diventano effettive dopo la sincronizzazione delle impostazioni delle finalità.

## Visualizzare il registro delle modifiche per un obiettivo personalizzato

1. Nel menu principale, fare clic su **[!UICONTROL Settings]>[!UICONTROL Custom Objectives]**.

1. Nella riga fare clic su **...*** > **[!UICONTROL Change Log]**.

<!--

Not used as of 2/6. If added, verify and edit:

## Delete an objective

You can delete an objective that's not assigned to a package.

1. In the main menu, click **[!UICONTROL Settings] > [!UICONTROL Custom Objectives]**.

1. In the row, click **...*** > **[!UICONTROL Delete]**.

1. In the confirmation message, click **[!UICONTROL Confirm]**.

-->

## Impostazioni obiettivo personalizzate {#custom-objective-settings}

<!-- Are we going to keep the heading "Properties" rather than "Metrics" (or Events, which is mentioned in the UI? Need a consistent naming convention. Ideally, it should be the same as the new SSC UI. -->

| Sezione | Parametro | Descrizione |
|---------|-----------|-------------|
| Dettagli di base | AMOClient | ID Adobe Advertising univoco dell’inserzionista. |
| Dettagli di base | Nome obiettivo | Nome dell&#39;obiettivo.<br><br>Tutti i nomi degli obiettivi per Advertising DSP devono essere preceduti dal prefisso &quot;ADSP_&quot; (senza distinzione maiuscole/minuscole), ad esempio &quot;ADSP_Registrations&quot;. Utilizzare un nome facile da identificare quando si desidera assegnarlo a un pacchetto. |
|  | Descrizione | (Facoltativo) Una descrizione dell&#39;obiettivo. La descrizione viene visualizzata quando si posiziona il cursore sul nome nell&#39;elenco Obiettivi personalizzati. Se non si include una descrizione, il nome dell&#39;obiettivo viene ripetuto. |
| Strategia di offerta |  | La strategia di offerta dell’obiettivo, che determina i tipi di eventi che è possibile configurare:<ul><li><b>[!UICONTROL Automated Bidding]:</b> Assegnare proprietà (metriche) all&#39;obiettivo come [!DNL goal] metriche. [!DNL Adobe AI] assegna e aggiorna automaticamente gli eventi di assistenza ponderata per massimizzare gli eventi obiettivo utilizzando un approccio funnel bilanciato.</li><li><b>[!UICONTROL Custom Bidding]:</b> Imposta la tua strategia di offerta assegnando le proprietà come eventi &quot;[!DNL goal]&quot; o &quot;[!DNL assist]&quot; ponderati. Utilizza questa opzione avanzata per le strategie predefinite.</li></ul>La modifica della strategia di offerta cancella tutte le metriche selezionate in precedenza. |
| Proprietà | [!UICONTROL Available Metrics] | Tutte le metriche tracciate per l’inserzionista. Per aggiungere una metrica come obiettivo, fare clic su <b>[!UICONTROL Goal]</b> accanto al nome della metrica. ([!UICONTROL Custom Bidding] solo) Per aggiungere una metrica che supporti le metriche obiettivo assegnate, fare clic su <b>[!UICONTROL Assist]</b> accanto al nome della metrica.<br><br><b>Note:</b> [!DNL Analytics] eventi personalizzati seguono questa convenzione di denominazione: `custom_event_[*event #*]_[*Analytics report suite ID*]`. Esempio: `custom_event_16_examplersid.` [!DNL Analytics] dimensioni e segmenti non sono disponibili per l&#39;ottimizzazione Adobe Advertising.<br><br><b>Suggerimento:</b> Per ottenere prestazioni ottimali, le metriche combinate nell&#39;obiettivo personalizzato (obiettivo) devono avere un totale di almeno dieci conversioni al giorno. In caso contrario, la best practice prevede di aggiungere all’obiettivo ulteriori metriche di conversione di supporto, come pagine di prodotti o avvii dell’applicazione. Consulta [Best practice per la creazione di un obiettivo personalizzato](#custom-goal-best-practices) per le linee guida. |
|  | Metriche selezionate | Il nome di ciascuna metrica di conversione inclusa nell’obiettivo. Effettua una delle seguenti operazioni:<ul><li>Per aggiungere una metrica come obiettivo, fare clic su <b>[!UICONTROL Goal]</b> accanto al nome della metrica nella colonna [!UICONTROL Available Metrics].</li><li>([!UICONTROL Custom Bidding] solo strategia) Per aggiungere una metrica che supporti le metriche obiettivo assegnate, fare clic su <b>[!UICONTROL Assist]</b> accanto al nome della metrica nella colonna [!UICONTROL Available Metrics]. Quindi inserisci il peso numerico della metrica rispetto ad altre metriche nell’obiettivo. Il peso deve essere compreso tra 0,001 e 1 e può includere decimali. Lo spessore predefinito è 1.</li><li>([!UICONTROL Custom Bidding] solo strategia) Per modificare il peso di una metrica di assistenza, fare clic all&#39;interno del campo e immettere il peso numerico della metrica rispetto ad altre metriche nell&#39;obiettivo. Il peso deve essere maggiore di zero (0) e può includere decimali. Lo spessore predefinito è 1.</li><li>Per rimuovere una metrica dall&#39;obiettivo, posizionare il cursore sul nome della metrica e fare clic su **[!UICONTROL X]**./li></ul>**Note:**<ul><li>Assicurati che le diverse metriche e i loro pesi abbiano un senso relativo. Ad esempio, non è possibile confrontare direttamente un conteggio con un importo in dollari.</li><li>Variazioni relative di grandi dimensioni tra i pesi oggettivi possono causare una temporanea volatilità delle prestazioni, in modo da monitorare le prestazioni dopo la modifica.</li></ul>. |

>[!MORELIKETHIS]
>
>* [Obiettivi di ottimizzazione e modalità di utilizzo](/help/dsp/optimization/optimization-goals.md)
>* [Best practice per gli obiettivi personalizzati](/help/dsp/optimization/custom-goal.md)
>* [Impostazioni pacchetto](/help/dsp/campaign-management/packages/package-settings.md)
>* [Gestione conversioni](/help/dsp/admin/conversion-metrics-manage.md)
