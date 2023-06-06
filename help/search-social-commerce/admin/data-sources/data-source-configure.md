---
title: Configurare un [!DNL Google Analytics] visualizzare come origine dati
description: Scopri come configurare un’origine dati da un [!DNL Google Analytics] visualizzazione.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '576'
ht-degree: 0%

---

# Configurare un [!DNL Google Analytics] visualizzare come origine dati

*Solo amministratori di agenzia, account manager di agenzia, account manager di Adobe e amministratori*

Puoi creare una sola origine dati per [!DNL Google Analytics] combinazione di account, proprietà e visualizzazione.

Per integrare le metriche per più proprietà o per più viste per una singola proprietà, imposta un’origine dati separata per ciascuna.

1. [Eseguire tutti i prerequisiti per integrare [!DNL Google Analytics] account](data-source-prerequisites.md).

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Data Source Setup]**.

1. Nella barra degli strumenti sopra la tabella dati, fai clic su ![Crea](/help/search-social-commerce/assets/add.png "Crea").

1. In [!UICONTROL Deployment Prerequisites] , selezionare la casella di controllo per confermare che la dimensione personalizzata &quot;ef_id&quot; richiesta sia implementata in [!DNL Google Analytics] e quindi fare clic su **[!UICONTROL Continue]**.

   Alcuni prerequisiti possono essere stati eseguiti da altri ruoli dell’organizzazione. Se hai domande sui prerequisiti, rivolgiti al team del tuo account Adobe.

1. Inserisci il [impostazioni origine dati](data-source-settings.md):

   1. In **[!UICONTROL Connect to [!DNL Google Analytics]]** eseguire le operazioni seguenti.

      1. Immetti l’ID numerico per [!DNL Google Analytics] account.

      1. Immettere l&#39;indirizzo di posta elettronica da utilizzare per accedere ai dati per questa origine dati. L’indirizzo e-mail deve essere registrato in un [!DNL Google] e disporre delle autorizzazioni di &quot;lettura e analisi&quot; per [!DNL Google Analytics] account. Consulta la [istruzioni per l’assegnazione delle autorizzazioni utente in [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587).

         >[!TIP]
         >
         >Per assicurarsi che solo specifici [!DNL Google Analytics] Le proprietà e le visualizzazioni sono disponibili in Adobe Advertising. Accedi utilizzando un indirizzo e-mail che abbia accesso solo a tali proprietà e visualizzazioni.

         >[!NOTE]
         >
         >Se successivamente modifichi la password per questo account e-mail, tutte le connessioni aperte all’account e-mail vengono chiuse. Per riprendere la sincronizzazione dei dati, torna a questa pagina e [riautentica](data-source-reauthenticate.md).

      1. Seleziona la casella di controllo per autorizzare Adobe Advertising ad accedere alle metriche per l’account.

      1. Clic **[!UICONTROL Authenticate]**.
   1. In [!UICONTROL Account Details] , specificare la proprietà e la visualizzazione per le metriche da importare. Inoltre, specifica la dimensione personalizzata compilata con il valore del parametro della stringa di query &quot;ef_id&quot;.

   1. In [!UICONTROL Import Metrics] , specifica le metriche da includere nei feed.

      Impossibile rimuovere [!UICONTROL Pageviews], [!UICONTROL Sessions], [!UICONTROL Bounces], o [!UICONTROL Session Duration], inclusi automaticamente. Puoi aggiungere fino a 16 metriche o metriche valide aggiuntive senza dati.

      >[!WARNING]
      >
      >[!DNL Google Analytics] consente fino a 10 metriche in un singolo feed di dati. Search, Social e Commerce possono supportare fino a due feed con un totale di 20 metriche, ma l’utilizzo di un secondo feed raddoppia le chiamate API a [!DNL Google Analytics]. Se disponi di molte metriche, seleziona solo quelle che desideri utilizzare negli obiettivi per l’ottimizzazione. Ulteriori informazioni su [quote e limiti di chiamata per le richieste API a [!DNL Google Analytics]](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas).

   1. In [!UICONTROL Metric Tag] , inserisci il nome del tag da aggiungere a ciascuna metrica per l’origine dati.


1. In alto a destra, fai clic su **[!UICONTROL Post]**.

   L&#39;origine dati è denominata &quot;AccountName > PropertyName > ViewName&quot; e viene attivata automaticamente. Per mettere in pausa l’origine dati, vedi &quot;[Sospendere un feed da un’origine dati](data-source-pause.md).&quot;

   Le metriche sono disponibili il giorno successivo al completamento della sincronizzazione dati giornaliera, che inizia alle 05:00 nel fuso orario dell’inserzionista. Una volta disponibili, le metriche sono visibili in [[!UICONTROL Admin] > [!UICONTROL Transaction Properties]](/help/search-social-commerce/admin/transaction-properties/transaction-property-about.md). Ogni nuova proprietà di transazione è denominata &quot;`ga:backEndMetricName_propertyID_viewID`,&quot; dove &quot;backEndMetricName&quot; è il nome della metrica utilizzato dall’API. Il nome visualizzato per ogni nuova proprietà di transazione è &quot;`friendlyMetricName_ga:MetricTag`,&quot; dove &quot;friendlyMetricName&quot; è il nome della metrica visualizzato in [!DNL Google Analytics] e &quot;MetricTag&quot; è il [!UICONTROL Metric Tag] definito nelle impostazioni dell’origine dati.

   Puoi aggiungere le metriche direttamente alle viste di gestione delle campagne e del portfolio, ai rapporti e agli obiettivi di ottimizzazione.

>[!MORELIKETHIS]
>
>* [Informazioni sulla sincronizzazione [!DNL Google Analytics] metriche di conversione](data-source-about.md)
>* [Prerequisiti per la configurazione di un [!DNL Google Analytics] origine dati](data-source-prerequisites.md)
>* [Modifica un [!DNL Google Analytics] origine dati](data-source-edit.md)
>* [Sospendere la sincronizzazione di un&#39;origine dati](data-source-pause.md)
>* [Autentica di nuovo un [!DNL Google Analytics] origine dati](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] impostazioni origine dati](data-source-settings.md)
>* [Appendice - Disponibile [!DNL Google Analytics] metriche](data-source-ga-metrics.md)

