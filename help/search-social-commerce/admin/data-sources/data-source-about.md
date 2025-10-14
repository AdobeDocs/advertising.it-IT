---
title: Informazioni sulla sincronizzazione delle metriche di conversione  [!DNL Google Analytics]
description: Scopri come sincronizzare [!DNL Google Analytics] le metriche di conversione per l'ottimizzazione e il reporting.
role: User, Admin
exl-id: 32d0ba22-5c27-4f50-9886-1c09d2da952c
feature: Search Admin, Search Data Sources
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# Informazioni sulla sincronizzazione di [!DNL Google Analytics] metriche di conversione

Search, Social e Commerce possono sincronizzare le metriche di conversione per un account [!DNL Google Analytics] specifico, la proprietà e la visualizzazione combinata per l&#39;ottimizzazione e il reporting. Le [visualizzazioni di pagina](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=page_tracking&amp;jump=ga_pageviews), [sessioni](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_sessions), [Percentuale di mancato recapito](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_bouncerate) (calcolate come mancati recapiti/sessioni) e [Durata sessione](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_sessionduration) sono incluse automaticamente. Puoi includere fino a 16 metriche aggiuntive per origine dati.

>[!NOTE]
>
>Gli utenti di Advertising DSP possono utilizzare le metriche di conversione come obiettivi personalizzati e nei rapporti.

L&#39;utilizzo di tutte le API per i trasferimenti di dati viene valutato per un progetto nell&#39;account [!DNL Google Analytics] applicabile. È possibile visualizzare le quote per questo progetto in [the [!DNL Google API Console]](https://console.developers.google.com/apis/api/analytics-json.googleapis.com/quotas). Consulta la documentazione di [!DNL Google Analytics] per ulteriori informazioni sulle [quote e limiti di chiamata per le richieste API di reporting](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas).

I passaggi seguenti descrivono il processo di sincronizzazione dei dati di conversione da [!DNL Google Analytics].

1. [Eseguire le attività preliminari](data-source-prerequisites.md)

   * Implementa un token di Adobe Advertising (parametro della stringa di query `ef_id`) negli URL della pagina di destinazione per tutti gli account pubblicitari applicabili.

   * Acquisire il token di Adobe Advertising (parametro stringa di query `ef_id`) in un [!DNL Custom Dimension] in [!DNL Google Analytics].

1. (Amministratore dell&#39;account agenzia, responsabile dell&#39;account agenzia, responsabile dell&#39;account di [!DNL Adobe] e solo utenti amministratore) [Crea un&#39;origine dati per [!DNL Google Analytics] account, proprietà e combinazione di visualizzazioni](data-source-configure.md).

   Per integrare le metriche per più proprietà o per più viste per una singola proprietà, imposta un’origine dati separata per ciascuna.

   Una volta configurata l’origine dati, Search, Social e Commerce estraggono i dati ogni giorno, a partire dalle 05:00 nel fuso orario dell’inserzionista. Una volta disponibili le metriche, puoi includerle nelle viste di gestione delle campagne e del portfolio e nei rapporti, e utilizzarle negli obiettivi di ottimizzazione, in base alle esigenze.

>[!MORELIKETHIS]
>
>* [Prerequisiti per la configurazione di un&#39;origine dati [!DNL Google Analytics] &#x200B;](data-source-prerequisites.md)
>* [Configurare una visualizzazione  [!DNL Google Analytics] come origine dati](data-source-configure.md)
>* [Modifica origine dati [!DNL Google Analytics] &#x200B;](data-source-edit.md)
>* [Sospendi la sincronizzazione di un&#39;origine dati](data-source-pause.md)
>* [Autentica nuovamente un&#39;origine dati [!DNL Google Analytics] &#x200B;](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] impostazioni origine dati](data-source-settings.md)
>* [Appendice - Disponibile [!DNL Google Analytics] metriche](data-source-ga-metrics.md)
