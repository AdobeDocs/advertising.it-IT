---
title: '[!UICONTROL Google AI Max Search Term Combination Report]'
description: Informazioni su [!UICONTROL Google AI Max Search Term Combination Report].
feature: Search Reports, Search Specialty Reports
source-git-commit: a595c7d6245fa5d65e704e88230f2eab0a336e72
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%
---
# [!UICONTROL Google AI Max Search Term Combination Report]

*Applicabile a [!DNL Google Ads] account con campagne abilitate solo per IA max*

[!UICONTROL Google AI Max Search Term Combination Report] mostra come le query di ricerca specifiche vengono mappate su titoli generati dall&#39;intelligenza artificiale e pagine di destinazione dinamiche e su azioni di conversione per annunci in campagne abilitate per [!DNL Google Ads AI Max] all&#39;interno di account specificati. Il rapporto include due fogli:

* [!UICONTROL AI Max Search Term] foglio: prestazioni di combinazioni di annunci e pagine di destinazione specifiche basate sulle ricerche effettuate all&#39;interno della rete di ricerca. Il foglio include dati su impression, clic e costi, nonché eventuali metriche di conversione facoltative con tracciamento [!DNL Google Ads] specificate nelle impostazioni del rapporto. Per impostazione predefinita, i dati includono una riga per ogni combinazione di termine di ricerca, titolo e pagina di destinazione che ha ricevuto almeno un’impression nell’intervallo di dati specificato. Per impostazione predefinita, le righe sono in ordine crescente per campagna e quindi per un’altra colonna a tua scelta.

  Utilizzare questo foglio per analizzare l&#39;intento e le prestazioni degli elementi annuncio risultanti per query in modo da creare elenchi di parole chiave negativi affidabili.

* <!-- [!UICONTROL Search Term x Conversion Action] sheet? -->Foglio [!UICONTROL AI Max Search Term #1]: dati di conversione tracciati da [!DNL Google Ads] per azione di conversione per ogni termine di ricerca e tipo di corrispondenza. Ogni riga include l&#39;azione di conversione, il numero di conversioni e il valore di conversione, nonché qualsiasi altra metrica di conversione facoltativa [!DNL Google Ads] tracciata specificata nelle impostazioni del report. Per impostazione predefinita, i dati includono una riga per ogni combinazione di termine di ricerca e azione di conversione nell’intervallo di dati specificato. Le righe sono nello stesso ordine delle righe del primo foglio.

  <!-- Should it be this?  The sheet includes the number of conversions and the conversion value, all conversions and the all conversions value, and cross-device conversions. -->

  Utilizza questo foglio per comprendere in che modo ogni termine di ricerca ha determinato le conversioni, suddivise per azione di conversione.

<!-- We're pulling data directly from GGL and not storing it, so no limitations on our end WRT date range. -->

## Colonne predefinite

Per le descrizioni di tutte le colonne predefinite e personalizzate, vedere &quot;[Colonne report per report speciali](specialty-report-columns.md).&quot;

<!-- VERIFY -- probably more will be included by default -->

* [!UICONTROL Event Date]
* [!UICONTROL Account Name]
* [!UICONTROL Network Campaign ID]
* [!UICONTROL Campaign Name]
* [!UICONTROL Ad Group Name]
* [!UICONTROL Search Term]
* [!UICONTROL Headline 1]
* [!UICONTROL Headline 2]
* [!UICONTROL Landing Page]
* [!UICONTROL Impressions]
* [!UICONTROL Clicks]
* [!UICONTROL Cost]
* [!UICONTROL Conversion Action] (incluso automaticamente nel foglio [!UICONTROL AI Max Search Term #1], anche se non viene incluso esplicitamente)
* [!UICONTROL Conversions] (incluso automaticamente nel foglio [!UICONTROL AI Max Search Term #1], anche se non viene incluso esplicitamente)
* [!UICONTROL Conversions Value] (incluso automaticamente nel foglio [!UICONTROL AI Max Search Term #1], anche se non viene incluso esplicitamente)

>[!MORELIKETHIS]
>
>* [Informazioni sui report speciali](specialty-report-about.md)
>* [Gestisci report pianificati](/help/search-social-commerce/new-ui/reports/management/report-manage.md)
>* [Impostazioni report speciali](specialty-report-settings.md)
>* [Colonne report per report speciali](specialty-report-columns.md)
