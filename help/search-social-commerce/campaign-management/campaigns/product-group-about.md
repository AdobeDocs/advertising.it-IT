---
title: Informazioni sui gruppi di prodotti di acquisto
description: Scopri come acquistare gruppi di prodotti nelle campagne di acquisto.
exl-id: ae270935-1464-4393-8b8c-745fee077522
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '721'
ht-degree: 0%

---

# Informazioni sui gruppi di prodotti di acquisto

Solo *[!DNL Google Ads]e [!DNL Microsoft Advertising] campagne acquisti*

Nelle campagne di acquisto, i gruppi di prodotti, non le parole chiave, determinano i prodotti nell’account del centro commerciale per cui vengono visualizzati gli annunci di acquisto. Ogni gruppo di prodotti è basato su un singolo attributo di prodotto (ad esempio categoria, tipo di prodotto, marchio, condizione, ID prodotto o etichette personalizzate) e utilizza la stessa offerta per tutti i prodotti corrispondenti. Puoi includere o escludere offerte per i prodotti di ogni gruppo.

Puoi configurare i gruppi di prodotti a livello di gruppo di annunci per determinare quali prodotti negli account del centro commerciale vengono visualizzati negli annunci commerciali per il gruppo di annunci. Anche se il gruppo di annunci non include entità pubblicitarie, la rete pubblicitaria visualizza comunque gli annunci per i prodotti.

Se lo stesso prodotto è incluso in più campagne, il network pubblicitario utilizza innanzitutto la priorità della campagna per determinare quale campagna (e l’offerta associata) è idonea per l’asta degli annunci. Se tutte le campagne hanno la stessa priorità, la campagna con l’offerta più elevata è idonea.

Per ulteriori informazioni sulle [!DNL Google] campagne e annunci di acquisto, consulta &quot;[Implementare [!DNL Google Ads] campagne di acquisto](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)&quot; e la [documentazione di Google Ads](https://support.google.com/google-ads/answer/3455481?visit_id=638205553638977410-2592024034&rd=1). Per ulteriori informazioni sulle [!DNL Microsoft] campagne di acquisto, consulta &quot;[Implementare [!DNL Microsoft Advertising] campagne acquisti](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)&quot; e la [[!DNL Microsoft Advertising] documentazione](https://help.bingads.microsoft.com/#apex/3/en/50903/1-500).

>[!NOTE]
>
>Il supporto non è disponibile per [!DNL Google Ads] gruppi di elenchi nelle campagne con prestazione massima, che sostituiscono le campagne di acquisto intelligente. Per gestire e visualizzare i dati per l&#39;elenco dei gruppi, utilizzare l&#39;editor [!DNL Google Ads].

## Gerarchia dei gruppi di prodotti

Prima di poter creare gruppi di prodotti con attributi specifici per un gruppo di annunci, è necessario creare un gruppo di prodotti completo denominato &quot;[!UICONTROL All Products]&quot;. Da questo gruppo di prodotti principale, è possibile creare gruppi di prodotti secondari per sottoinsiemi di prodotti e i nipoti dai gruppi di prodotti secondari. Dopo aver creato il primo gruppo di prodotti figlio per un gruppo di annunci, viene creato automaticamente un altro gruppo di prodotti denominato &quot;[!UICONTROL Everything Else]&quot; utilizzando l&#39;offerta del gruppo di annunci predefinito. Quando si aggiungono altri gruppi di prodotti, il gruppo &quot;[!UICONTROL Everything Else]&quot; viene regolato di conseguenza in modo che costituisca tutti i prodotti che non fanno parte di un altro gruppo di prodotti.

All&#39;interno di un gruppo di annunci, è possibile creare fino a sette livelli di gruppi di prodotti (escluso &quot;[!UICONTROL All Products]&quot;) per includere o escludere la partecipazione, con uno o più gruppi di prodotti che utilizzano lo stesso attributo in ogni livello (ad esempio, [!UICONTROL Brand]=Acme per un gruppo di prodotti e [!UICONTROL Brand]=AcmePlus per un altro allo stesso livello). I gruppi di prodotti padre sono denominati suddivisioni e il livello di suddivisione più basso è denominato unità. Puoi impostare le offerte e i modelli di tracciamento, o escludere completamente le offerte, a livello di unità. L’intero set di gruppi di prodotti attivi per un gruppo di annunci viene applicato in modo gerarchico per determinare i prodotti idonei. Ad esempio, se si suddivide [!UICONTROL All Products] in [!UICONTROL Brand]=AcmeBasic e [!UICONTROL Brand]=AcmePlus e poi si suddivide ulteriormente ciascuno di questi gruppi di prodotti in [!UICONTROL Condition]=nuovi e si impostano le offerte, solo i nuovi prodotti con i marchi AcmeBasic e AcmePlus possono essere pubblicizzati o esclusi dagli annunci.

![Esempio di set di gruppi di prodotti](/help/search-social-commerce/assets/product-group-list.png "Esempio di set di gruppi di prodotti")

![Gerarchia di gruppi di prodotti di esempio](/help/search-social-commerce/assets/product-group-tree.png "Gerarchia di gruppi di prodotti di esempio")

## Visualizzazione [!UICONTROL Product Groups]

È possibile creare e modificare i gruppi di prodotti ed eliminare i gruppi di prodotti e i relativi gruppi di prodotti figlio nella visualizzazione [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups].

## Tracciamento e dati sulle prestazioni per i gruppi di prodotti di acquisto

(Account/campagne con l&#39;opzione di tracciamento &quot;[!UICONTROL EF Redirect]&quot;) Per consentire a Search, Social e Commerce di tenere traccia delle conversioni per i gruppi di prodotti, [genera URL di tracciamento per i gruppi di prodotti utilizzando lo strumento URL di tracciamento](/help/search-social-commerce/tools/click-tracking-url-generate.md), quindi effettua una delle seguenti operazioni:

* (Obbligatorio per [!DNL Google Ads]; best practice per [!DNL Microsoft Advertising]) Aggiungi l&#39;URL di tracciamento al campo [!DNL Tracking Template] nell&#39;impostazione dell&#39;account, della campagna o del gruppo di prodotti. Per semplificare la manutenzione, aggiungili al livello più alto possibile. Eventuali parametri di accodamento specificati per l’account o la campagna non sono inclusi.

  >[!CAUTION]
  >
  >([!DNL Microsoft Advertising]) Utilizzare questa opzione solo se gli URL di tracciamento di Search, Social e Commerce non sono inclusi in una colonna personalizzata all&#39;interno del feed del prodotto. Se esegui entrambe le operazioni, gli URL includeranno due reindirizzamenti e causeranno collegamenti interrotti.

* ([!DNL Microsoft Advertising] solo) Aggiungi l&#39;URL di tracciamento ai dati di prodotto nell&#39;account [!DNL Microsoft Merchant Center]. A tale scopo, includere l&#39;URL di tracciamento, insieme al valore nel campo `link` o `mobile_link`, a seconda dei casi, in una colonna personalizzata denominata [`bingads_redirect`](https://help.ads.microsoft.com/#apex/3/en/51084/0) all&#39;interno del feed del prodotto. Gli URL generati con questo metodo non includono parametri di tracciamento specificati nelle impostazioni dell’account o della campagna in Search, Social &amp; Commerce.

Puoi visualizzare i dati sui gruppi di prodotti in [ il [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/product-group-report.md).

>[!MORELIKETHIS]
>
>* [Gestione dei gruppi di prodotti](product-group-manage.md)
>* [[!DNL Google Ads] impostazioni gruppo di prodotti](product-group-settings-google.md)
>* [Implementa [!DNL Google Ads] campagne acquisti](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)
>* [[!DNL Microsoft Advertising] impostazioni gruppo di prodotti](product-group-settings-microsoft.md)
>* [Implementa [!DNL Microsoft Advertising] campagne acquisti](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)
