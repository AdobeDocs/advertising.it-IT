---
title: Autentica nuovamente un'origine dati  [!DNL Google Analytics]
description: Scopri come autenticare nuovamente un'origine dati  [!DNL Google Analytics]  se modifichi la password associata o se il certificato scade.
role: User, Admin
exl-id: 624f0f0e-3f2f-45b1-b3dc-c1b107b4736f
feature: Search Admin, Search Data Sources
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 0%

---

# Autentica nuovamente un&#39;origine dati [!DNL Google Analytics]

*Solo amministratori di agenzia, account manager di agenzia, Adobi e amministratori*

Se si modifica la password dell&#39;account di posta elettronica utilizzato per un&#39;origine dati o se il certificato [!DNL OAuth] dell&#39;account scade, tutte le connessioni aperte all&#39;account di posta elettronica verranno chiuse e sarà necessario ripetere l&#39;autenticazione per riprendere la sincronizzazione dei dati.

1. Nel menu principale, fare clic su **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Data Source Setup]**.

1. Selezionare la casella di controllo accanto all&#39;origine dati che si desidera riautenticare.

1. Nella barra degli strumenti sopra la tabella dati, fare clic su ![Modifica](/help/search-social-commerce/assets/edit.png "Modifica").

1. Modifica le [impostazioni dell&#39;origine dati](data-source-settings.md):

   1. Nella sezione [!UICONTROL Connect to Google Analytics] eseguire le operazioni seguenti.

      1. (Se necessario) Immetti un nuovo indirizzo e-mail da utilizzare per accedere ai dati per questa origine dati. L&#39;indirizzo di posta elettronica deve essere registrato in un account [!DNL Google] e disporre delle autorizzazioni di lettura e analisi per l&#39;account [!DNL Google Analytics]. Consulta le [istruzioni per assegnare le autorizzazioni utente in [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587).

         >[!TIP]
         >
         >Per accertarsi che solo specifiche proprietà e visualizzazioni di [!DNL Google Analytics] siano disponibili in Search, Social e Commerce, effettuare l&#39;accesso utilizzando un indirizzo e-mail che abbia accesso solo a tali proprietà e visualizzazioni.

   1. Seleziona la casella di controllo per autorizzare Search, Social e Commerce ad accedere alle metriche per l’account.

   1. Fare clic su **[!UICONTROL Re-Authenticate]**.

1. Fare clic su **[!UICONTROL Post]**.

>[!MORELIKETHIS]
>
>* [Informazioni sulla sincronizzazione [!DNL Google Analytics] metriche di conversione](data-source-about.md)
>* [Prerequisiti per la configurazione di un&#39;origine dati [!DNL Google Analytics] ](data-source-prerequisites.md)
>* [Configurare una visualizzazione  [!DNL Google Analytics] come origine dati](data-source-configure.md)
>* [Modifica origine dati [!DNL Google Analytics] ](data-source-edit.md)
>* [Sospendi la sincronizzazione di un&#39;origine dati](data-source-pause.md)
>* [[!DNL Google Analytics] impostazioni origine dati](data-source-settings.md)
>* [Appendice - Disponibile [!DNL Google Analytics] metriche](data-source-ga-metrics.md)
