---
title: ID Adobe Advertising utilizzati da [!DNL Analytics]
description: ID Adobe Advertising utilizzati da [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ff20b97e-27fe-420e-bd55-8277dc791081
source-git-commit: e24cc514018ee67c485e884c4d57d051293ebf6a
workflow-type: tm+mt
source-wordcount: '864'
ht-degree: 0%

---

# ID Adobe Advertising utilizzati da [!DNL Analytics]

*Inserzionisti con una sola integrazione Adobe Advertising-Adobe Analytics*

*Applicabile ad Advertising DSP e[!DNL Advertising Search, Social, & Commerce]*

Adobe Advertising utilizza due ID per il tracciamento delle prestazioni nel sito: *EF ID* e *AMO ID*.

Quando si verifica un’impression pubblicitaria, Adobe Advertising crea i valori AMO ID e EF ID e li memorizza. Quando un visitatore che ha visto un annuncio entra nel sito senza fare clic su un annuncio, [!DNL Analytics] chiama questi valori da Adobe Advertising tramite il codice JavaScript [!DNL Analytics for Advertising]. Per il traffico view-through, [!DNL Analytics] genera un ID supplementare (`SDID`) utilizzato per unire l&#39;ID EF e l&#39;AMO ID in [!DNL Analytics]. Per il traffico click-through, questi ID vengono inclusi nell’URL della pagina di destinazione utilizzando i parametri della stringa di query `ef_id` e `s_kwcid` (per l’AMO ID).

Adobe Advertising distingue tra una voce di click-through o di view-through per il sito web utilizzando i seguenti criteri:

* Una voce view-through viene acquisita quando un utente visita il sito dopo aver visualizzato un annuncio ma non facendo clic su di esso. [!DNL Analytics] registra un view-through se sono soddisfatte due condizioni:

   * Il visitatore non ha click-through per un annuncio [!DNL DSP] o [!DNL Search, Social, & Commerce] durante l&#39;[intervallo di lookback su clic](/help/integrations/analytics/prerequisites.md#lookback-a4adc).

   * Il visitatore ha visto almeno un annuncio [!DNL DSP] durante l&#39;[intervallo di lookback delle impression](/help/integrations/analytics/prerequisites.md#lookback-a4adc). L’ultima impression viene passata come view-through.

* Una voce di click-through viene acquisita quando un visitatore del sito fa clic su un annuncio prima di entrare nel sito. [!DNL Analytics] acquisisce un click-through quando si verifica una delle seguenti condizioni:

   * L’URL include un EF ID e un AMO ID aggiunti all’URL della pagina di destinazione da Adobe Advertising.

   * L’URL non contiene codici di tracciamento, ma il codice JavaScript di Adobe Advertising rileva un clic negli ultimi due minuti.

![Integrazione [!DNL Analytics] basata su visualizzazioni di Adobe Advertising](/help/integrations/assets/a4adc-view-through-process.png)

*Figura 1: integrazione [!DNL Analytics] basata su Adobe Advertising*

![Integrazione [!DNL Analytics] basata su URL con clic su Adobe Advertising](/help/integrations/assets/a4adc-click-through-process.png)

*Figura 2: integrazione [!DNL Analytics] basata su URL di clic di Adobe Advertising*

<!-- ## Adobe Advertising EF IDs -->

{{$include /help/_includes/ef-id.md}}

### ID EF Dimension in [!DNL Analytics]

Nei report [!DNL Analytics], è possibile trovare i dati ID EF cercando la dimensione [!UICONTROL EF ID] e utilizzando la metrica [!UICONTROL EF ID Instance].

Gli ID EF sono soggetti al limite di identificatori univoci di 500.000 in Analysis Workspace. Una volta raggiunto il valore 500k, tutti i nuovi codici di tracciamento vengono segnalati con il titolo a riga singola &quot;[!UICONTROL Low Traffic]&quot;. A causa della possibilità di mancanza di fedeltà di reporting, gli ID EF non sono classificati e non è consigliabile utilizzarli per segmenti o rapporti in [!DNL Analytics].

<!-- ## ## Adobe Advertising AMO IDs {#amo-id} -->

{{$include /help/_includes/amo-id.md}}

### Metodi per implementare AMO ID {#amo-id-implement}

Il parametro viene aggiunto agli URL di tracciamento in uno dei seguenti modi:

* (Consigliato) Quando la funzione di inserimento lato server è implementata.

   * Clienti DSP: il pixel server aggiunge automaticamente il parametro s_kwcid ai suffissi della pagina di destinazione quando un utente finale visualizza un annuncio con pixel di Adobe Advertising.

   * Clienti Search, Social e Commerce:

      * Per gli account [!DNL Google Ads] e [!DNL Microsoft Advertising] con l&#39;impostazione [!UICONTROL Auto Upload] abilitata per l&#39;account o la campagna, il pixel server aggiunge automaticamente il parametro s_kwcid ai suffissi della pagina di destinazione quando un utente finale fa clic su un annuncio con il pixel di Adobe Advertising.

      * Per le altre reti di annunci o per gli account [!DNL Google Ads] e [!DNL Microsoft Advertising] con l&#39;impostazione [!UICONTROL Auto Upload] disabilitata, aggiungi manualmente il parametro ai [parametri di aggiunta a livello di account](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}, che lo aggiungono agli URL di base.

* Quando la funzione di inserimento lato server non è implementata:

   * Clienti DSP: il [codice JavaScript](javascript.md) registra automaticamente i click-through e i view-through. Se un browser non supporta i cookie di terze parti, puoi comunque tenere traccia delle conversioni basate su clic per i seguenti tipi di annunci:

      * Per [!DNL Flashtalking] tag annuncio, inserisci manualmente macro aggiuntive per &quot;[Aggiungi [!DNL Analytics for Advertising] Macro a [!DNL Flashtalking] Tag annuncio](/help/integrations/analytics/macros-flashtalking.md).&quot; **Nota:** questa procedura non è necessaria se l&#39;organizzazione ha una relazione diretta con [!DNL Flashtalking] e si utilizzano macro di passaggio dati per tenere traccia dei parametri di tracciamento di `s_kwcid` e `ef_id` in base alla documentazione di supporto di [!DNL Flashtalking] all&#39;indirizzo [https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros](https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros).

      * Per [!DNL Google Campaign Manager 360] tag annuncio, inserisci manualmente macro aggiuntive per &quot;[Aggiungi [!DNL Analytics for Advertising] Macro a [!DNL Google Campaign Manager 360] Tag annuncio](/help/integrations/analytics/macros-google-campaign-manager.md).&quot;

   * Clienti Search, Social e Commerce:

      * Per gli annunci ([!DNL Google Ads] e [!DNL Microsoft Advertising]), aggiungi manualmente il parametro AMO ID ai suffissi della pagina di destinazione, idealmente a [livello account](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}, a meno che non sia necessario il tracciamento diverso per i singoli componenti account.

      * Per gli annunci su tutte le altre reti pubblicitarie, aggiungi manualmente il parametro AMO ID ai [parametri di aggiunta a livello di account](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}, che lo aggiungono agli URL di base.

Per implementare la funzione di inserimento lato server o per determinare l’opzione migliore per la tua azienda, rivolgiti al team del tuo account Adobe.

### AMO ID Dimension in [!DNL Analytics]

Nei rapporti di Analytics, puoi trovare i dati AMO ID cercando la dimensione [!UICONTROL AMO ID] e utilizzando la metrica [!UICONTROL AMO ID Instances]. La dimensione [!UICONTROL AMO ID] ospita tutti i valori AMO ID acquisiti, mentre la metrica [!UICONTROL AMO ID Instances] indica la frequenza con cui un valore AMO ID è stato acquisito dal sito. Ad esempio, se lo stesso annuncio di ricerca è stato fatto clic quattro volte ma Analytics ha tracciato sette voci di sito, [!UICONTROL AMO ID Instances] sarebbe sette (7) e [!UICONTROL Clicks] sarebbe quattro (4).

Per qualsiasi reporting o controllo all’interno di [!DNL Analytics], la best practice consiste nell’utilizzare l’AMO ID insieme alla relativa istanza corrispondente. Per ulteriori informazioni, vedere &quot;[Convalida dati Click-through per [!DNL Analytics for Advertising]](data-variances.md#data-validation)&quot; in &quot;Varianze di dati previste tra [!DNL Analytics] e Adobe Advertising.&quot;

## Informazioni sulle classificazioni di Analytics

In [!DNL Analytics], una [classificazione](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html?lang=it) è un elemento di metadati per un determinato codice di tracciamento, ad esempio Account, Campagna o Annuncio. Adobe Advertising categorizza i dati non elaborati di Adobe Advertising utilizzando le classificazioni in modo da poter visualizzare i dati in diversi modi (ad esempio per tipo di annuncio o campagna) quando si generano i rapporti. Le classificazioni costituiscono la base del reporting di Adobe Advertising in [!DNL Analytics] e possono essere utilizzate con le metriche AMO, ad esempio [!UICONTROL Adobe Advertising Cost], [!UICONTROL Adobe Advertising Impressions] e [!UICONTROL AMO Clicks], nonché con eventi nel sito personalizzati e standard come [!UICONTROL Visits], [!UICONTROL Leads], [!UICONTROL Orders] e [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [Panoramica di [!DNL Analytics for Advertising]](overview.md)
>* [Varianze di dati previste tra [!DNL Analytics] e Adobe Advertising](data-variances.md)
