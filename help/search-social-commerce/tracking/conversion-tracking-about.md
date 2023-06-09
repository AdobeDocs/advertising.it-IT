---
title: Opzioni di tracciamento delle conversioni per Ricerca, Social e Commerce
description: Scopri le opzioni di tracciamento delle conversioni per Search, Social e Commerce.
source-git-commit: 5dadb0bea063f454dcfde46c0a4cc747290767c8
workflow-type: tm+mt
source-wordcount: '837'
ht-degree: 0%

---

# Opzioni di tracciamento delle conversioni per Ricerca, Social e Commerce

Search, Social e Commerce possono utilizzare i dati di conversione tracciati nei seguenti modi:

* **Adobe di conversioni tracciate dalla pubblicità:** L’inserzionista inserisce un tag Adobe Advertising di tracciamento delle conversioni in ogni pagina di conversione. Il tag invia i dati di conversione a un server di tracciamento. Puoi utilizzare il pixel legacy di terze parti o il più recente pixel di prime parti. Consulta &quot;[Confronto di ciascun metodo di tracciamento delle conversioni](#conversion-tracking-comparison).&quot;

* **Conversioni Adobe Analytics:** L&#39;inserzionista utilizza il tracciamento di Adobe Analytics per tutte le conversioni. Questa opzione richiede un’integrazione Adobe Advertising-Adobe Analytics. Consulta &quot;[Tracciamento delle conversioni Adobe Analytics](conversion-tracking-analytics.md)&quot; per ulteriori informazioni.

* **[!DNL Google Analytics]conversioni:** L’inserzionista utilizza [!DNL Google Analytics] per tenere traccia di tutte le conversioni. Consulta &quot;[[!DNL Google Ads] dati di conversione in Search, Social e Commerce](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)&quot; per ulteriori informazioni sulle conversioni sincronizzate automaticamente.

* **Conversioni tracciate dagli inserzionisti:** (Solo per client Search, Social e Commerce) L’inserzionista fornisce a Search, Social e Commerce un file di feed con qualsiasi combinazione di dati di conversione online e offline. Consulta &quot;[Tracciamento delle conversioni tramite un feed EF ID](feed-efid.md)&quot; e &quot;[Tracciamento delle conversioni tramite un feed ID transazione](feed-transaction-id.md).&quot;

## Confronto di ciascun metodo di tracciamento delle conversioni {#conversion-tracking-comparison}

Poiché i criteri dei cookie del browser continuano a essere più rigidi, è importante comprendere le attuali funzionalità di tracciamento e identificare le opzioni migliori per il lungo termine.

| Metodo di tracciamento | Descrizione | Limitazioni | Vantaggi | Consigliato? |
|----|----|----|----|----|
| Adobe Analytics | Inserzionisti con [Adobe Analytics per la pubblicità](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) importa automaticamente i [!DNL Analytics] eventi standard e personalizzati di Adobe Advertising per il reporting e l’ottimizzazione. | <ul><li>[!DNL Safari] consente solo un lookback di conversione di sette giorni, che viene reimpostato sulle visite ripetute del sito durante l’intervallo di lookback.</li><li> Prevedi limitazioni simili in [!DNL Chrome] nel 2024.</li></ul> | <ul><li>Integrazione perfetta con [!DNL Analytics]</li> <li>Vedi dati di ricerca a pagamento in [!DNL Analytics] Analysis Workspace</li><li>Vantaggi oltre la ricerca a pagamento</li></ul> | Sì |
| Pixel Adobe Advertising legacy | Gli inserzionisti aggiungono alle pagine di conversione l’immagine di Adobe Advertising legacy o i pixel JavaScript. Il pixel viene attivato quando un utente che ha fatto clic su un annuncio raggiunge la pagina. Questo metodo si basa su cookie di terze parti. | <ul><li>[!DNL Safari] blocca tutto il tracciamento delle conversioni utilizzando questo metodo.</li><li>Prevedi limitazioni simili in [!DNL Chrome] nel 2024.</li></ul> | Il pixel è già implementato. Tuttavia, è comunque necessario [implementare il tag di mappatura ITP aggiuntivo](itp-conversion-mapping-tag.md).<br><br>Consiglio: passa al pixel di prime parti. | No |
| Adobe Advertising First-party Pixel | Gli inserzionisti eseguono le seguenti operazioni: <ul><li>Implementare la libreria JavaScript per [Servizio Adobe Experience Cloud ID (ECID)](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) sull&#39;intero sito.</li><li>Aggiungi l&#39;Adobe Advertising [Tag JavaScript con mappatura ITP](itp-conversion-mapping-tag.md) su qualsiasi pagina che potrebbe essere una pagina di destinazione da un clic di ricerca (idealmente, su tutte le pagine, poiché le pagine di destinazione possono cambiare nel tempo). Il tag consente agli Adobi Advertising di tenere traccia di un evento di conversione che si verifica su una pagina e che converte numeri elevati in notazione scientifica nella pagina di destinazione.</li><li>Aggiungi l&#39;Adobe Advertising [Tag per il tracciamento della conversione JavaScript v3](format-conversion-tag-jsv3.md) alle pagine di conversione.</li></ul> | <ul><li>[!DNL Safari] consente solo un lookback di conversione di sette giorni, che viene reimpostato sulle visite ripetute del sito durante l’intervallo di lookback.</li><li>Prevedi limitazioni simili in [!DNL Chrome] nel 2022.</li></ul> | [!DNL Safari] tiene traccia delle conversioni durante il lookback di sette giorni. Poiché il lookback viene reimpostato sulle visite ripetute del sito durante l’intervallo di lookback, la limitazione non influisce su tutti [!DNL Safari] utenti. | No |
| Feed EFID | Gli account di ricerca dell’inserzionista sono impostati per generare URL di destinazione/URL finali con ID univoci di Adobe Advertising (token). Quando un utente fa clic su un annuncio, in Adobe Advertising viene creato un ID univoco (`EFID`) e la visualizza alla fine dell’URL finale. Il client system dell’inserzionista acquisisce l’EFID come identificatore univoco per le conversioni risultanti dal clic e lo invia all’Adobe Advertising in un feed di ricavi che include l’EFID, la data della transazione e la proprietà di conversione. Adobe Advertising utilizza quindi l’EFID per far corrispondere la conversione al clic originale. | <ul><li>L’inserzionista deve disporre di un modo per acquisire l’EFID e inviare quotidianamente feed automatizzati agli Adobi Advertising.</li><li>Le conversioni possono essere tracciate fino a 180 giorni (per Adobe Advertising) o in base ai limiti del sistema dell’inserzionista.</li></ul> | <ul><li>Questo metodo utilizza dati di conversione di prima parte, pertanto non è interessato da limitazioni dei cookie di terze parti.</li><li>Le conversioni online e offline possono essere inviate in un unico feed.</li><li>Per il sito non sono necessari tag o modifiche al codice.</li></ul> | Sì |
| Feed ID transazione [feed combinato] | Gli inserzionisti aggiungono pixel pubblicitari di Adobe che includono un parametro per un ID transazione univoco (`ev_transid=&lt;transid&gt;`) alle loro pagine web e Adobe Advertising acquisisce l’ID transazione univoco creato quando il pixel viene attivato. Il sistema client dell’inserzionista acquisisce anche [!UICONTROL Transaction ID] e invia all’Adobe Advertising un feed di ricavi per conversioni offline con corrispondenza [!UICONTROL Transaction ID] valori | <ul><li>Se l’inserzionista utilizza il pixel legacy, che [!DNL Safari] blocca l’attivazione, quindi l’ID non viene acquisito da utilizzare per i dati offline.</li><li>Il feed non è automatizzato.</li></ul> | <ul><li>Se implementi il pixel di prime parti, allora [!UICONTROL Transaction ID] viene acquisito in [!DNL Safari].</li><li>Fornisce il tracciamento degli eventi di conversione offline/approvati.</li></ul> | No |
| Conversioni Google | Conversioni tracciate con [!DNL Google Analytics] I tag vengono importati automaticamente in Adobe Advertising tramite una connessione API. Ogni nome di conversione ha una `&quot;GGL_&quot;` prefisso. | <ul><li>Google in genere non tiene traccia dei dati offline.</li><li>Le conversioni Microsoft® Advertising non sono incluse.</li></ul> | Google utilizza l’apprendimento automatico per estrapolare &quot;[conversioni modellate](https://support.google.com/google-ads/answer/10081327).&quot; | No |

<table style="table-layout:auto">

<!--
| Microsoft Advertising Conversions | Conversions tracked with Microsoft Advertising universal event tags (UET) are automatically imported to Adobe Advertising via an API connection. Each conversion name has a &quot;???&quot; prefix. | Microsoft Advertising typically doesn't track offline data. Google conversions aren't included. | ?? | No |
-->

>[!MORELIKETHIS]
>
>* [Informazioni sui tag di tracciamento delle conversioni di Adobe Advertising](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Tracciamento delle conversioni Adobe Analytics](/help/search-social-commerce/tracking/conversion-tracking-analytics.md)
>* [Tracciamento delle conversioni tramite un feed EF ID](/help/search-social-commerce/tracking/feed-efid.md)
>* [Tracciamento delle conversioni tramite un feed ID transazione](/help/search-social-commerce/tracking/feed-transaction-id.md)
