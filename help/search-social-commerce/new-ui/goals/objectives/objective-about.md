---
title: (Nuova interfaccia) Informazioni sugli obiettivi
description: Scopri gli obiettivi per raggiungere gli obiettivi aziendali.
feature: Search Objectives, Search Optimization
hide: true
exl-id: 4e417307-1403-4420-85f9-2fa04c253b58
source-git-commit: df5d34c7d86174107278e0cd4f5a99329a21ca61
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 0%

---

# (Nuova interfaccia) Informazioni sugli obiettivi

*funzionalità Beta*

Gli obiettivi sono obiettivi che un inserzionista stabilisce per soddisfare i propri obiettivi aziendali, ad esempio per massimizzare i profitti o per raggiungere un obiettivo di vendita specifico. Gli obiettivi di Advertising Search, Social, Commerce e Advertising DSP sono i seguenti:

* Ogni portfolio Search, Social e Commerce deve avere un obiettivo in modo che la funzionalità di ottimizzazione possa creare modelli di clic e di ricavo per il portfolio.

* In DSP, gli obiettivi vengono visualizzati come obiettivi personalizzati per gli account DSP collegati agli account Search, Social e Commerce. Ogni pacchetto che utilizza gli obiettivi di ottimizzazione &quot;ROAS (Highest Return on Ad Spend)&quot; o &quot;CPA (Lowest Cost per Acquisition)&quot; deve includere un obiettivo personalizzato che contribuisca a raggiungere l’obiettivo di ottimizzazione generale.

Un obiettivo è costituito dalle metriche di conversione da tracciare e ottimizzare e dai relativi pesi di tali metriche. Ad esempio, supponiamo che una rivista online con due livelli di abbonamento online e un livello di abbonamento a stampa e l’obiettivo &quot;massimizzare i profitti&quot; disponga di tre metriche: &quot;abbonamenti online di base&quot; con un valore di 20 USD, &quot;abbonamenti online premium&quot; con un valore di 40 USD e &quot;abbonamenti a stampa&quot; con un valore di 30 USD. Se la rivista vuole dare peso in base al valore monetario una tantum dell’abbonamento, allora i pesi relativi delle metriche saranno rispettivamente 1, 2 e 1,5.

Per ogni metrica nell’obiettivo, puoi:

* Configura pesi separati per le conversioni dai dispositivi mobili.

* Etichettare la metrica come metrica [!UICONTROL Goal] o metrica [!UICONTROL Assist].

* Applica consigli sul peso alle metriche.

>[!NOTE]
>* (Cerca, Social e Commerce) Puoi associare un obiettivo a un portfolio quando [crei il portfolio](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-create.md) o in seguito [modificando le impostazioni del portfolio](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-edit.md).
>* (Inserzionisti con account DSP collegati ad account Search, Social e Commerce) In Advertising DSP puoi selezionare un obiettivo come [obiettivo di ottimizzazione personalizzato](/help/dsp/campaign-management/packages/package-settings.md) per un pacchetto con velocità a livello di pacchetto.
>* Puoi utilizzare lo stesso obiettivo per più portfolio Search, Social e Commerce e/o più pacchetti DSP.
>* Le metriche per ogni obiettivo nella visualizzazione [!UICONTROL Objectives] non includono i dati di DSP.

## Metriche disponibili

Nei tuoi obiettivi puoi includere uno qualsiasi dei seguenti elementi:

* Metriche tracciate da Adobe Advertising con il [pixel di tracciamento delle conversioni di Adobe Advertising](/help/search-social-commerce/tracking/conversion-tracking-advertising.md).

* [Metriche tracciate dagli inserzionisti dai file del feed di conversione](/help/search-social-commerce/tracking/conversion-tracking-about.md).<!-- Search only, or might DSP-only clients also have these? -->

* (Inserzionisti con [!DNL Adobe Analytics for Advertising]) [Metriche di conversione e coinvolgimento del sito sincronizzate da Adobe Analytics](/help/integrations/analytics/overview.md).

  In Search, Social e Commerce, le seguenti [metriche di coinvolgimento sito](/help/integrations/analytics/analytics-data-in-advertising.md) vengono automaticamente incluse negli algoritmi di offerta portfolio: `timespent_secs_1stvisit`, `timespent_secs_total`, `pageviews_1stvisit`, `pageviews_total` e `bounces`.

* [!DNL Google] metriche:<!-- Search only, or might DSP-only clients also have these? -->

   * [[!DNL Google Ads] conversioni tracciate](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md) da [!DNL Google Ads] account sincronizzati.

   * (Inserzionisti con [[!DNL Google Analytics] integrazioni](/help/search-social-commerce/admin/data-sources/data-source-about.md)) Visualizzazioni di pagina, Sessioni, Frequenza di rimbalzo (calcolata come rimbalzi/sessioni) e Durata della sessione.

     In Search, Social e Commerce, queste metriche vengono automaticamente incluse negli algoritmi di offerta del portfolio.

## Opzione per caricare gli obiettivi nelle reti di annunci

Facoltativamente, puoi [caricare gli obiettivi per i portfolio dell&#39;account in [!DNL Google Ads] e/o [!DNL Microsoft Advertising] come conversioni](/help/search-social-commerce/tools/objective-upload-to-networks.md) in modo da poterli utilizzare per l&#39;ottimizzazione a livello di campagna o di gruppo di annunci. Quando abiliti l’opzione, Cerca, Social e Commerce trasmette quotidianamente i dati dei ricavi ponderati a livello di ID EF (ID clic) alla rete di annunci. Omette qualsiasi metrica tracciata dalla rete di annunci.

>[!MORELIKETHIS]
>
>* [Crea un obiettivo](objective-create.md)
>* [Modifica un obiettivo](objective-edit.md)
>* [Eliminare un obiettivo](objective-delete.md)
>* [Applicare consigli sul peso a un obiettivo](objective-apply-weight-recommendations.md)
>* [Impostazioni obiettivo](objective-settings.md)
