---
title: Opzioni di tracciamento delle conversioni per Search, Social e Commerce
description: Scopri le opzioni di tracciamento delle conversioni per Search, Social e Commerce.
exl-id: 263da6a4-8d72-4882-8784-290a3be6f8fa
feature: Search Tracking
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '821'
ht-degree: 0%

---

# Opzioni di tracciamento delle conversioni per Search, Social e Commerce

Search, Social e Commerce possono utilizzare i dati di conversione tracciati nei seguenti modi:

* **Conversioni tracciate dall&#39;Adobe Advertising:** L&#39;inserzionista inserisce un tag di tracciamento delle conversioni di Adobe Advertising in ogni pagina di conversione. Il tag invia i dati di conversione a un server di tracciamento. Puoi utilizzare il pixel legacy di terze parti o il più recente pixel di prime parti. Vedi &quot;[Confronto di ciascun metodo di tracciamento delle conversioni](#conversion-tracking-comparison).&quot;

* **Conversioni Adobe Analytics:** l&#39;inserzionista utilizza il tracciamento di Adobe Analytics per tutte le conversioni. Questa opzione richiede un’integrazione Adobe Advertising-Adobe Analytics. Per ulteriori informazioni, vedere &quot;[Tracciamento conversione Adobe Analytics](conversion-tracking-analytics.md)&quot;.

* **[!DNL Google Analytics]conversioni:** L&#39;inserzionista utilizza il tag [!DNL Google Analytics] per monitorare tutte le conversioni. Per ulteriori informazioni sulle conversioni sincronizzate automaticamente, vedere &quot;[[!DNL Google Ads] dati di conversione in Search, Social e Commerce](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)&quot;.

* **Conversioni tracciate dall&#39;inserzionista:** (solo client Search, Social e Commerce) L&#39;inserzionista fornisce a Search, Social e Commerce un file di feed con qualsiasi combinazione di dati di conversione online e offline. Consulta &quot;[Tracciamento delle conversioni utilizzando un feed EF ID](feed-efid.md)&quot; e &quot;[Tracciamento delle conversioni utilizzando un feed ID transazione](feed-transaction-id.md).&quot;

## Confronto di ciascun metodo di tracciamento delle conversioni {#conversion-tracking-comparison}

Poiché i criteri dei cookie del browser continuano a essere più rigidi, è importante comprendere le attuali funzionalità di tracciamento e identificare le opzioni migliori per il lungo termine.

| Metodo di tracciamento | Descrizione | Limitazioni | Vantaggi | Consigliato? |
|----|----|----|----|----|
| Adobe Analytics | Gli inserzionisti con [Adobe Analytics per Advertising](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) importano automaticamente i propri [!DNL Analytics] eventi standard e personalizzati in Adobe Advertising per il reporting e l&#39;ottimizzazione. | <ul><li>[!DNL Safari] consente solo un lookback di conversione di sette giorni, che viene reimpostato nelle visite ripetute del sito durante l&#39;intervallo di lookback.</li><li> Limitazioni simili sono previste in [!DNL Chrome] nel 2024.</li></ul> | <ul><li>Integrazione perfetta con [!DNL Analytics]</li> <li>Visualizza dati di ricerca a pagamento in [!DNL Analytics] Analysis Workspace</li><li>Vantaggi oltre la ricerca a pagamento</li></ul> | Sì |
| Pixel Adobe Advertising legacy | Gli inserzionisti aggiungono un’immagine di Adobe Advertising legacy o pixel JavaScript alle proprie pagine di conversione. Il pixel viene attivato quando un utente che ha fatto clic su un annuncio raggiunge la pagina. Questo metodo si basa su cookie di terze parti. | <ul><li>[!DNL Safari] blocca tutto il tracciamento delle conversioni utilizzando questo metodo.</li><li>Limitazioni simili sono previste in [!DNL Chrome] nel 2024.</li></ul> | Il pixel è già implementato. Tuttavia, è comunque necessario [implementare il tag di mappatura ITP aggiuntivo](itp-conversion-mapping-tag.md).<br><br>Consiglio: passa al pixel di prime parti. | No |
| Adobe Advertising Pixel di prime parti | Gli inserzionisti eseguono le seguenti operazioni: <ul><li>Implementa la libreria JavaScript per il servizio [Adobe Experience Cloud ID (ECID)](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) nell&#39;intero sito.</li><li>Aggiungi i [tag JavaScript di Adobe Advertising con mappatura ITP](itp-conversion-mapping-tag.md) a qualsiasi pagina che potrebbe essere una pagina di destinazione da un clic di ricerca (idealmente, su tutte le pagine, poiché le pagine di destinazione possono cambiare nel tempo). Il tag consente agli Adobi Advertising di tenere traccia di un evento di conversione che si verifica su una pagina e che converte numeri elevati in notazione scientifica nella pagina di destinazione.</li><li>Aggiungi l&#39;Adobe Advertising [Tag di tracciamento conversione di JavaScript v3](format-conversion-tag-jsv3.md) alle pagine di conversione.</li></ul> | <ul><li>[!DNL Safari] consente solo un lookback di conversione di sette giorni, che viene reimpostato nelle visite ripetute del sito durante l&#39;intervallo di lookback.</li><li>Limitazioni simili sono previste in [!DNL Chrome] nel 2022.</li></ul> | [!DNL Safari] tiene traccia delle conversioni durante il lookback di sette giorni. Poiché il lookback viene reimpostato nelle visite ripetute al sito durante l&#39;intervallo di lookback, la limitazione non interessa tutti gli utenti [!DNL Safari]. | No |
| Feed EFID | Gli account di ricerca dell’inserzionista sono impostati per generare URL di destinazione/URL finali con ID univoci di Adobe Advertising (token). Quando un utente fa clic su un annuncio, Adobe Advertising crea un ID univoco (`EFID`) e lo visualizza alla fine dell&#39;URL finale. Il client system dell’inserzionista acquisisce l’EFID come identificatore univoco per le conversioni risultanti dal clic e lo invia all’Adobe Advertising in un feed di ricavi che include l’EFID, la data della transazione e la metrica di conversione. Adobe Advertising utilizza quindi l’EFID per far corrispondere la conversione al clic originale. | <ul><li>L’inserzionista deve disporre di un modo per acquisire l’EFID e inviare quotidianamente feed automatizzati agli Adobi Advertising.</li><li>Le conversioni possono essere tracciate fino a 180 giorni (per Adobe Advertising) o in base ai limiti del sistema dell’inserzionista.</li></ul> | <ul><li>Questo metodo utilizza dati di conversione di prima parte, pertanto non è interessato da limitazioni dei cookie di terze parti.</li><li>Le conversioni online e offline possono essere inviate in un unico feed.</li><li>Per il sito non sono necessari tag o modifiche al codice.</li></ul> | Sì |
| Feed ID transazione [feed combinato] | Gli inserzionisti aggiungono pixel di Adobe Advertising che includono un parametro per un ID transazione univoco (`ev_transid=&lt;transid&gt;`) alle proprie pagine Web e Adobe Advertising acquisisce l&#39;ID transazione univoco creato quando il pixel viene attivato. Il client dell&#39;inserzionista acquisisce anche [!UICONTROL Transaction ID] e invia all&#39;Adobe Advertising un feed di ricavi per le conversioni offline con valori [!UICONTROL Transaction ID] corrispondenti | <ul><li>Se l&#39;inserzionista utilizza il pixel legacy, che [!DNL Safari] blocca l&#39;attivazione, l&#39;ID non viene acquisito per l&#39;utilizzo di dati offline.</li><li>Il feed non è automatizzato.</li></ul> | <ul><li>Se si implementa il pixel di prime parti, [!UICONTROL Transaction ID] verrà acquisito in [!DNL Safari].</li><li>Fornisce il tracciamento degli eventi di conversione offline/approvati.</li></ul> | No |
| [!DNL Google] conversioni | Le conversioni tracciate con [!DNL Google Analytics] tag vengono importate automaticamente in Adobe Advertising tramite una connessione API. Ogni nome di conversione ha un prefisso `&quot;GGL_&quot;`. | <ul><li>[!DNL Google] in genere non tiene traccia dei dati offline.</li><li>[!DNL Microsoft Advertising] conversioni non sono incluse.</li></ul> | [!DNL Google] utilizza l&#39;apprendimento automatico per estrapolare &quot;[conversioni modellate](https://support.google.com/google-ads/answer/10081327).&quot; | No |

<!--
| [!DNL Microsoft Advertising] Conversions | Conversions tracked with [!DNL Microsoft Advertising] universal event tags (UET) are automatically imported to Adobe Advertising via an API connection. Each conversion name has a &quot;???&quot; prefix. | [!DNL Microsoft Advertising] typically doesn't track offline data. [!DNL Google] conversions aren't included. | ?? | No |
-->

>[!MORELIKETHIS]
>
>* [Informazioni su Adobi Advertising di tag per il tracciamento delle conversioni](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Tracciamento delle conversioni di Adobe Analytics](/help/search-social-commerce/tracking/conversion-tracking-analytics.md)
>* [Tracciamento delle conversioni tramite un feed EF ID](/help/search-social-commerce/tracking/feed-efid.md)
>* [Tracciamento delle conversioni tramite un feed ID transazione](/help/search-social-commerce/tracking/feed-transaction-id.md)
