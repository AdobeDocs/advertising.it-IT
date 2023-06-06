---
title: Informazioni sulla sincronizzazione [!DNL Google Analytics] metriche di conversione
description: Informazioni sulla sincronizzazione [!DNL Google Analytics] metriche di conversione per ottimizzazione e reporting.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# Informazioni sulla sincronizzazione [!DNL Google Analytics] metriche di conversione

Search, Social e Commerce possono sincronizzare le metriche di conversione per un [!DNL Google Analytics] combinazione di account, proprietà e visualizzazione per l&#39;ottimizzazione e il reporting. [Visualizzazioni pagina](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=page_tracking&amp;jump=ga_pageviews), [Sessioni](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_sessions), [Percentuale non recapitate](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_bouncerate) (calcolato come mancati recapiti/sessioni) e [Durata sessione](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_sessionduration) sono inclusi automaticamente. Puoi includere fino a 16 metriche aggiuntive per origine dati.

>[!NOTE]
>
>Gli utenti di Advertising DSP possono utilizzare le metriche di conversione come obiettivi personalizzati e nei rapporti.

L’utilizzo di tutte le API per i trasferimenti di dati viene valutato in un progetto nella [!DNL Google Analytics] account. È possibile visualizzare le quote per questo progetto in [il [!DNL Google API Console]](https://console.developers.google.com/apis/api/analytics-json.googleapis.com/quotas). Consulta [!DNL Google Analytics] per ulteriori informazioni su [quote e limiti di chiamata per la generazione di rapporti sulle richieste API](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas).

I passaggi seguenti descrivono il processo di sincronizzazione dei dati di conversione da [!DNL Google Analytics].

1. [Eseguire le attività preliminari](data-source-prerequisites.md)

   * Implementare un token pubblicitario Adobe (`ef_id` query string parameter) negli URL della pagina di destinazione per tutti gli account pubblicitari applicabili.

   * Acquisisci il token pubblicitario dell’Adobe (`ef_id` query string parameter) in una [!DNL Custom Dimension] in [!DNL Google Analytics].

1. (Amministratore del conto di agenzia, responsabile del conto di agenzia, [!DNL Adobe] account manager e amministratori (solo utenti) [Creare un’origine dati per [!DNL Google Analytics] combinazione di account, proprietà e visualizzazione](data-source-configure.md).

   Per integrare le metriche per più proprietà o per più viste per una singola proprietà, imposta un’origine dati separata per ciascuna.

   Una volta configurata l’origine dati, Search, Social e Commerce estrae i dati ogni giorno, a partire dalle 05:00 nel fuso orario dell’inserzionista. Una volta disponibili le metriche, puoi includerle nelle viste di gestione delle campagne e del portfolio e nei rapporti, e utilizzarle negli obiettivi di ottimizzazione, in base alle esigenze.

>[!MORELIKETHIS]
>
>* [Prerequisiti per la configurazione di un [!DNL Google Analytics] origine dati](data-source-prerequisites.md)
>* [Configurare un [!DNL Google Analytics] visualizzare come origine dati](data-source-configure.md)
>* [Modifica un [!DNL Google Analytics] origine dati](data-source-edit.md)
>* [Sospendere la sincronizzazione di un&#39;origine dati](data-source-pause.md)
>* [Autentica di nuovo un [!DNL Google Analytics] origine dati](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] impostazioni origine dati](data-source-settings.md)
>* [Appendice - Disponibile [!DNL Google Analytics] metriche](data-source-ga-metrics.md)

