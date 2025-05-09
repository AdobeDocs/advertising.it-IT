---
title: Configura una visualizzazione  [!DNL Google Analytics]  come origine dati
description: Scopri come configurare un’origine dati da una visualizzazione  [!DNL Google Analytics] .
role: User, Admin
exl-id: 9e299e42-4971-49ea-a515-54a97eb13e0d
feature: Search Admin, Search Data Sources
source-git-commit: 26a4451fb09f2a42ac60ba123ddf0cf38323312d
workflow-type: tm+mt
source-wordcount: '568'
ht-degree: 0%

---

# Configurare una visualizzazione [!DNL Google Analytics] come origine dati

*Solo amministratori di agenzia, account manager di agenzia, account manager di Adobe e amministratori*

È possibile creare un&#39;origine dati per ogni account, proprietà e combinazione di visualizzazioni di [!DNL Google Analytics].

Per integrare le metriche per più proprietà o per più viste per una singola proprietà, imposta un’origine dati separata per ciascuna.

1. [Esegui tutti i prerequisiti per l&#39;integrazione di  [!DNL Google Analytics] account](data-source-prerequisites.md).

1. Nel menu principale, fare clic su **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Data Source Setup]**.

1. Nella barra degli strumenti sopra la tabella dati, fare clic su ![Crea](/help/search-social-commerce/assets/add.png "Crea").

1. Nella finestra di dialogo [!UICONTROL Deployment Prerequisites], selezionare la casella di controllo per confermare che la dimensione personalizzata &quot;ef_id&quot; richiesta è implementata nell&#39;account [!DNL Google Analytics], quindi fare clic su **[!UICONTROL Continue]**.

   Alcuni prerequisiti possono essere stati eseguiti da altri ruoli dell’organizzazione. Se hai domande sui prerequisiti, rivolgiti al team del tuo account Adobe.

1. Immettere le [impostazioni dell&#39;origine dati](data-source-settings.md):

   1. Nella sezione **[!UICONTROL Connect to [!DNL Google Analytics]]** eseguire le operazioni seguenti.

      1. Immettere l&#39;ID numerico per l&#39;account [!DNL Google Analytics].

      1. Immettere l&#39;indirizzo di posta elettronica da utilizzare per accedere ai dati per questa origine dati. L&#39;indirizzo di posta elettronica deve essere registrato in un account [!DNL Google] e disporre delle autorizzazioni di lettura e analisi per l&#39;account [!DNL Google Analytics]. Consulta le [istruzioni per assegnare le autorizzazioni utente in [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587).

         >[!TIP]
         >
         >Per accertarsi che solo specifiche proprietà e visualizzazioni di [!DNL Google Analytics] siano disponibili in Adobe Advertising, accedi utilizzando un indirizzo e-mail che abbia accesso solo a tali proprietà e visualizzazioni.

         >[!NOTE]
         >
         >Se successivamente modifichi la password per questo account e-mail, tutte le connessioni aperte all’account e-mail vengono chiuse. Per riprendere la sincronizzazione dei dati, tornare a questa pagina e [autenticare](data-source-reauthenticate.md).

      1. Seleziona la casella di controllo per autorizzare Adobe Advertising ad accedere alle metriche per l’account.

      1. Fare clic su **[!UICONTROL Authenticate]**.

   1. Nella sezione [!UICONTROL Account Details], specifica la proprietà e la visualizzazione per le metriche da importare. Inoltre, specifica la dimensione personalizzata compilata con il valore del parametro della stringa di query &quot;ef_id&quot;.

   1. Nella sezione [!UICONTROL Import Metrics], specifica le metriche da includere nei feed.

      Impossibile rimuovere [!UICONTROL Pageviews], [!UICONTROL Sessions], [!UICONTROL Bounces] o [!UICONTROL Session Duration], che sono inclusi automaticamente. Puoi aggiungere fino a 16 metriche o metriche valide aggiuntive senza dati.

      >[!WARNING]
      >
      >[!DNL Google Analytics] consente fino a 10 metriche in un singolo feed di dati. Search, Social e Commerce possono supportare fino a due feed con un totale di 20 metriche, ma l&#39;utilizzo di un secondo feed raddoppia le chiamate API a [!DNL Google Analytics]. Se disponi di molte metriche, seleziona solo quelle che desideri utilizzare negli obiettivi per l’ottimizzazione. Ulteriori informazioni sulle [quote e sui limiti di chiamata per le richieste API a  [!DNL Google Analytics]](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas).

   1. Nella sezione [!UICONTROL Metric Tag] immettere il nome del tag da aggiungere a ogni metrica per l&#39;origine dati.

1. In alto a destra, fare clic su **[!UICONTROL Post]**.

   L&#39;origine dati è denominata &quot;AccountName > PropertyName > ViewName&quot; e viene attivata automaticamente. Per mettere in pausa l&#39;origine dati, vedere &quot;[Sospendere un feed da un Data Source](data-source-pause.md).&quot;

   Le metriche sono disponibili il giorno successivo al completamento della sincronizzazione dati giornaliera, che inizia alle 05:00 nel fuso orario dell’inserzionista. Una volta disponibili, le metriche sono visibili in [[!UICONTROL Admin] > [!UICONTROL Conversions]](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md). Ogni nuova metrica di conversione è denominata &quot;`ga:backEndMetricName_propertyID_viewID`&quot;, dove &quot;backEndMetricName&quot; è il nome della metrica utilizzato dall&#39;API. Il nome visualizzato per ogni nuova metrica di conversione è &quot;`friendlyMetricName_ga:MetricTag`&quot;, dove &quot;friendlyMetricName&quot; è il nome della metrica visualizzato in [!DNL Google Analytics] e &quot;MetricTag&quot; è il [!UICONTROL Metric Tag] definito nelle impostazioni dell&#39;origine dati.

   Puoi aggiungere le metriche direttamente alle viste di gestione delle campagne e del portfolio, ai rapporti e agli obiettivi di ottimizzazione.

>[!MORELIKETHIS]
>
>* [Informazioni sulla sincronizzazione [!DNL Google Analytics] metriche di conversione](data-source-about.md)
>* [Prerequisiti per la configurazione di un&#39;origine dati [!DNL Google Analytics] ](data-source-prerequisites.md)
>* [Modifica origine dati [!DNL Google Analytics] ](data-source-edit.md)
>* [Sospendi la sincronizzazione di un&#39;origine dati](data-source-pause.md)
>* [Autentica nuovamente un&#39;origine dati [!DNL Google Analytics] ](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] impostazioni origine dati](data-source-settings.md)
>* [Appendice - Disponibile [!DNL Google Analytics] metriche](data-source-ga-metrics.md)
