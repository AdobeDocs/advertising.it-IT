---
title: Creare e modificare i dati della campagna in blocco utilizzando Copia e Incolla
description: Scopri come gestire i dati della campagna in blocco utilizzando la funzione di copia e incolla.
exl-id: 2ae1b02f-46ac-4ea8-aa9f-9e26ccaf63d0
feature: Search Campaign Management
source-git-commit: c2a1ce841a9dc99c57239f817dbd2065b91cdfb9
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---

# Creare e modificare i dati della campagna in blocco utilizzando Copia e Incolla

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads], [!DNL Yandex], ed esistenti [!DNL Baidu] solo account*

*[!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], e [!UICONTROL Ads] visualizzazioni*

È possibile copiare fino a 10.000 righe dalla [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], e [!UICONTROL Ads] visualizzazioni e incollarle in [!DNL Microsoft Excel] o un altro editor per modificare qualsiasi campo non ID. È quindi possibile copiare [!DNL Excel] e incollarle nuovamente nella visualizzazione come dati separati da tabulazioni per apportare le modifiche. La funzionalità utilizza gli Appunti del computer.

Puoi utilizzare questa funzione per modificare gli oggetti campagna esistenti (con i campi ID ) e per creare nuovi oggetti campagna senza i campi ID.

## Copiare righe di dati

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nei sottomenu, fare clic su **[!UICONTROL Live]> \[[!UICONTROL Campaigns] \| [!UICONTROL Ad Groups] \| [!UICONTROL Keywords] \| [!UICONTROL Ads]\]**.

1. Selezionare la casella di controllo accanto a ogni riga da copiare.

   Puoi copiare fino a 10.000 righe.

1. Nella barra degli strumenti sopra la tabella dati, fai clic su ![Altro](/help/search-social-commerce/assets/more.png "Altro")e quindi fare clic su **[!UICONTROL Copy]**.

   In alternativa, è possibile utilizzare il comando &quot;copia&quot; della tastiera del sistema operativo, ad esempio **[!DNL Ctrl+C]** per [!DNL Microsoft Windows] o **[!DNL Command-C]** per [!DNL Apple Mac].

1. In [!UICONTROL Copy to Clipboard] , fai clic su **[!UICONTROL Continue]**. Quando i dati sono pronti per essere copiati, fai clic su **[!UICONTROL Copy]**.

1. Incolla le righe in [!DNL Excel] o un altro editor.

## Modificare e creare righe di dati

1. Modificare i dati in base ai seguenti requisiti:

   * I dati incollati devono includere una riga di intestazione e i valori dell’oggetto campagna necessari. Per informazioni, consulta le colonne richieste del bulksheet. [Baidu](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-baidu.md), [Google Ads](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md), [Microsoft Advertising](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md), [Naver](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md), [Yahoo! Rete di visualizzazione](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-display-network.md), [Yahoo! Giappone](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-japan.md), e [Yandex](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yandex.md). L&#39;ordine delle colonne non ha importanza.

      * Per gli oggetti esistenti che si desidera modificare, è necessario includere tutte le colonne ID rilevanti, i nomi delle entità e l&#39;attributo da modificare. Non modificare l&#39;ID numerico dell&#39;oggetto.

      * Per i nuovi oggetti campagna, includi tutti i nomi e gli attributi di entità rilevanti, ma non gli ID oggetto (che vengono generati automaticamente). Ad esempio, se crei un nuovo annuncio, lascia [!UICONTROL Ad ID] campo vuoto. La rete di annunci crea automaticamente un ID quando inserisci l’oggetto.

   * Il valore in una colonna non obbligatoria può essere nullo (vuoto), ma ogni riga deve avere lo stesso numero di valori separati da tabulazioni.

1. Salva i dati come valori separati da tabulazioni.

## Incollare le righe di dati nelle visualizzazioni di gestione delle campagne

>[!NOTE]
>
>Se le righe incollate contengono dati identici a quelli delle entità esistenti o che duplicano un&#39;entità esistente, i dati duplicati vengono ignorati.

1. In entrata [!DNL Excel] o un altro editor, copia le righe separate da tabulazioni pertinenti.

1. Nel menu principale di Ricerca, Social e Commerce, fai clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Apri la visualizzazione in cui incollare i dati (**[!UICONTROL Live]> \[[!UICONTROL Campaigns] \| [!UICONTROL Ad Groups] \| [!UICONTROL Keywords] \| [!UICONTROL Ads]\]**).

1. Nella barra degli strumenti sopra la tabella dati, fai clic su ![Altro](/help/search-social-commerce/assets/more.png "Altro")e quindi fare clic su **[!UICONTROL Paste]**.

   In alternativa, è possibile utilizzare il comando &quot;incolla&quot; della tastiera del sistema operativo, ad esempio **[!DNL Ctrl+V]** per [!DNL Microsoft Windows] o **[!DNL Command-V]** per [!DNL Apple Mac].

1. Incollare i dati nella casella di input, quindi fare clic su **[!UICONTROL Process]**.

1. (Facoltativo) Immettere ulteriori dettagli:

   * (If **[!UICONTROL Additional Details]** è compresso) Fare clic su ![Apri](/help/search-social-commerce/assets/chevron-up.png "Apri") per espandere i dettagli.

   * Immetti un valore facoltativo **[!UICONTROL Job Name]** e/o opzionale **[!UICONTROL Job Description]**.

1. Clic **[!UICONTROL Post Now]**.


>[!MORELIKETHIS]
>
>* [Informazioni sulla gestione dei dati della campagna tramite bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)
>* [Modificare le impostazioni direttamente all&#39;interno di una riga](/help/search-social-commerce/common-tasks/settings-edit-within-row.md)
>* [Gestire le campagne](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
>* [Gestire i gruppi di annunci](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
>* [Gestire le parole chiave](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
>* [Gestione annunci](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md)
