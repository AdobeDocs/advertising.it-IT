---
title: Informazioni sui gruppi di prodotti di acquisto
description: Scopri come acquistare gruppi di prodotti nelle campagne di acquisto.
exl-id: ae270935-1464-4393-8b8c-745fee077522
feature: Search Campaign Management
source-git-commit: 4ed0d225dafcb07e8a563ef7e723cd247da5e1a9
workflow-type: tm+mt
source-wordcount: '722'
ht-degree: 0%

---

# Informazioni sui gruppi di prodotti di acquisto

*[!DNL Google Ads]e [!DNL Microsoft® Advertising] solo campagne di acquisto*

Nelle campagne di acquisto, i gruppi di prodotti, non le parole chiave, determinano i prodotti nell’account del centro commerciale per cui vengono visualizzati gli annunci di acquisto. Ogni gruppo di prodotti è basato su un singolo attributo di prodotto (ad esempio categoria, tipo di prodotto, marchio, condizione, ID prodotto o etichette personalizzate) e utilizza la stessa offerta per tutti i prodotti corrispondenti. Puoi includere o escludere offerte per i prodotti di ogni gruppo.

Puoi configurare i gruppi di prodotti a livello di gruppo di annunci per determinare quali prodotti negli account del centro commerciale vengono visualizzati negli annunci commerciali per il gruppo di annunci. Anche se il gruppo di annunci non include entità pubblicitarie, la rete pubblicitaria visualizza comunque gli annunci per i prodotti.

Se lo stesso prodotto è incluso in più campagne, il network pubblicitario utilizza innanzitutto la priorità della campagna per determinare quale campagna (e l’offerta associata) è idonea per l’asta degli annunci. Se tutte le campagne hanno la stessa priorità, la campagna con l’offerta più elevata è idonea.

Per ulteriori informazioni su [!DNL Google] campagne e annunci di acquisto, consulta &quot;[Implementare [!DNL Google Ads] campagne di acquisto](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md)&quot; e [Documentazione di Google Ads](https://support.google.com/google-ads/answer/3455481?visit_id=638205553638977410-2592024034&amp;rd=1). Per ulteriori informazioni su [!DNL Microsoft®] campagne di acquisto, consulta &quot;[Implementare [!DNL Microsoft® Advertising] campagne di acquisto](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md)&quot; e [[!DNL Microsoft® Advertising] documentazione](https://help.bingads.microsoft.com/#apex/3/en/50903/1-500).

>[!NOTE]
>
>Supporto non disponibile per [!DNL Google Ads] elenco dei gruppi nelle campagne performance max, che sostituiscono le campagne smart shopping. Per gestire e visualizzare i dati per l&#39;elenco dei gruppi, utilizzare [!DNL Google Ads] editor.

## Gerarchia dei gruppi di prodotti

Prima di poter creare gruppi di prodotti con attributi specifici per un gruppo di annunci, devi creare un gruppo di prodotti completo denominato &quot;[!UICONTROL All Products].&quot; Da questo gruppo di prodotti principale, è possibile creare gruppi di prodotti secondari per sottoinsiemi di prodotti e i nipoti dai gruppi di prodotti secondari. Dopo aver creato il primo gruppo di prodotti figlio per un gruppo di annunci, viene creato un altro gruppo di prodotti denominato &quot;[!UICONTROL Everything Else]&quot; viene creato automaticamente utilizzando l’offerta del gruppo di annunci predefinito. Man mano che aggiungi più gruppi di prodotti, il[!UICONTROL Everything Else]&quot; viene modificato di conseguenza in modo che costituisca tutti i prodotti che non rientrano in un altro gruppo di prodotti.

All’interno di un gruppo di annunci, puoi creare fino a sette livelli di gruppi di prodotti (escluso &quot;[!UICONTROL All Products]&quot;) per includere o escludere dalla gara, con uno o più gruppi di prodotti che hanno come target lo stesso attributo in ogni livello (ad esempio, [!UICONTROL Brand]=Acme per un gruppo di prodotti e [!UICONTROL Brand]=AcmePlus per un altro allo stesso livello). I gruppi di prodotti padre sono denominati suddivisioni e il livello di suddivisione più basso è denominato unità. Puoi impostare le offerte e i modelli di tracciamento, o escludere completamente le offerte, a livello di unità. L’intero set di gruppi di prodotti attivi per un gruppo di annunci viene applicato in modo gerarchico per determinare i prodotti idonei. Ad esempio, se suddividi [!UICONTROL All Products] in [!UICONTROL Brand]=AcmeBasic e [!UICONTROL Brand]=AcmePlus e quindi suddividere ulteriormente ciascuno di questi gruppi di prodotti in [!UICONTROL Condition]=Nuove e impostate le offerte; solo i nuovi prodotti con i marchi AcmeBasic e AcmePlus possono essere pubblicizzati o esclusi dagli annunci.

![Esempio di un set di gruppi di prodotti](/help/search-social-commerce/assets/product-group-list.png "Esempio di un set di gruppi di prodotti")

![Esempio di gerarchia di gruppi di prodotti](/help/search-social-commerce/assets/product-group-tree.png "Esempio di gerarchia di gruppi di prodotti")

## Il [!UICONTROL Product Groups] visualizza

È possibile creare e modificare gruppi di prodotti ed eliminare gruppi di prodotti e i relativi gruppi di prodotti figlio nel [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups] visualizzazione.

## Tracciamento e dati sulle prestazioni per i gruppi di prodotti di acquisto

(Account/campagne con &quot;[!UICONTROL EF Redirect]&quot; (opzione di tracciamento) Per consentire a Search, Social e Commerce di tracciare le conversioni per gruppi di prodotti, [generare URL di tracciamento per gruppi di prodotti utilizzando lo strumento URL di tracciamento;](/help/search-social-commerce/tools/click-tracking-url-generate.md), quindi eseguire una delle operazioni seguenti:

* (Obbligatorio per [!DNL Google Ads]; best practice per [!DNL Microsoft® Advertising]) Aggiungi l&#39;URL di tracciamento al [!DNL Tracking Template] nell’impostazione account, campagna o gruppo di prodotti. Per semplificare la manutenzione, aggiungili al livello più alto possibile. Eventuali parametri di accodamento specificati per l’account o la campagna non sono inclusi.

  >[!CAUTION]
  >
  >([!DNL Microsoft® Advertising]) Utilizza questa opzione solo se non includi gli URL di tracciamento di Ricerca, Social e Commerce in una colonna personalizzata all’interno del feed del prodotto. Se esegui entrambe le operazioni, gli URL includeranno due reindirizzamenti e causeranno collegamenti interrotti.

* ([!DNL Microsoft® Advertising] solo ) Aggiungi l’URL di tracciamento ai dati di prodotto all’interno di [!DNL Microsoft® Merchant Center] account. A tal fine, includi l’URL di tracciamento, insieme al valore in `link` o `mobile_link` in una colonna personalizzata denominata [`bingads_redirect`](https://help.ads.microsoft.com/#apex/3/en/51084/0) all’interno del feed del prodotto. Gli URL generati con questo metodo non includono parametri di tracciamento specificati nelle impostazioni dell’account o della campagna in Search, Social &amp; Commerce.

Puoi visualizzare i dati sui gruppi di prodotti in [il [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/product-group-report.md).

>[!MORELIKETHIS]
>
>* [Gestire i gruppi di prodotti](product-group-manage.md)
>* [[!DNL Google Ads] impostazioni gruppo di prodotti](product-group-settings-google.md)
>* [Implementare [!DNL Google Ads] campagne di acquisto](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md)
>* [[!DNL Microsoft® Advertising] impostazioni gruppo di prodotti](product-group-settings-microsoft.md)
>* [Implementare [!DNL Microsoft® Advertising] campagne di acquisto](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md)
