---
title: Autentica di nuovo un [!DNL Google Analytics] origine dati
description: Scopri come autenticare nuovamente un [!DNL Google Analytics] origine dati se si modifica la password associata o se il certificato scade.
role: User, Admin
exl-id: 9233e004-8607-444a-ba99-f63cb83a8b7a
source-git-commit: ec7d7f5531c038eb772339a36d13208fc97d2728
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---

# Autentica di nuovo un [!DNL Google Analytics] origine dati

*Solo amministratori di agenzia, account manager di agenzia, account manager di Adobe e amministratori*

Se si modifica la password per l&#39;account di posta elettronica utilizzato per un&#39;origine dati o se [!DNL OAuth] il certificato per l&#39;account scade, quindi tutte le connessioni aperte all&#39;account di posta elettronica vengono chiuse e sarà necessario ripetere l&#39;autenticazione per riprendere la sincronizzazione dei dati.

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Data Source Setup]**.

1. Selezionare la casella di controllo accanto all&#39;origine dati che si desidera riautenticare.

1. Nella barra degli strumenti sopra la tabella dati, fai clic su ![Modifica](/help/search-social-commerce/assets/edit.png "Modifica").

1. Modifica il [impostazioni origine dati](data-source-settings.md):

   1. In [!UICONTROL Connect to Google Analytics] eseguire le operazioni seguenti.

      1. (Se necessario) Immetti un nuovo indirizzo e-mail da utilizzare per accedere ai dati per questa origine dati. L’indirizzo e-mail deve essere registrato in un [!DNL Google] e disporre delle autorizzazioni di &quot;lettura e analisi&quot; per [!DNL Google Analytics] account. Consulta la [istruzioni per l’assegnazione delle autorizzazioni utente in [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587).

         >[!TIP]
         >
         >Per assicurarsi che solo specifici [!DNL Google Analytics] Le proprietà e le visualizzazioni sono disponibili in Search, Social e Commerce; effettua l’accesso utilizzando un indirizzo e-mail che abbia accesso solo a tali proprietà e visualizzazioni.

   1. Seleziona la casella di controllo per autorizzare Search, Social e Commerce ad accedere alle metriche per l’account.

   1. Clic **[!UICONTROL Re-Authenticate]**.

1. Clic **[!UICONTROL Post]**.

>[!MORELIKETHIS]
>
>* [Informazioni sulla sincronizzazione [!DNL Google Analytics] metriche di conversione](data-source-about.md)
>* [Prerequisiti per la configurazione di un [!DNL Google Analytics] origine dati](data-source-prerequisites.md)
>* [Configurare un [!DNL Google Analytics] visualizzare come origine dati](data-source-configure.md)
>* [Modifica un [!DNL Google Analytics] origine dati](data-source-edit.md)
>* [Sospendere la sincronizzazione di un&#39;origine dati](data-source-pause.md)
>* [[!DNL Google Analytics] impostazioni origine dati](data-source-settings.md)
>* [Appendice - Disponibile [!DNL Google Analytics] metriche](data-source-ga-metrics.md)
