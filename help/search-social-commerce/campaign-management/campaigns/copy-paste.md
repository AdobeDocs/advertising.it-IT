---
title: Creare e modificare i dati della campagna in blocco utilizzando Copia e Incolla
description: Scopri come gestire i dati della campagna in blocco utilizzando la funzione di copia e incolla.
exl-id: 2ae1b02f-46ac-4ea8-aa9f-9e26ccaf63d0
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---

# Creare e modificare i dati della campagna in blocco utilizzando Copia e Incolla

Solo *[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads], [!DNL Yandex] e [!DNL Baidu] account esistenti*

*[!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] e [!UICONTROL Ads] visualizzazioni*

È possibile copiare fino a 10.000 righe dalle viste [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] e [!UICONTROL Ads] e incollarle in [!DNL Microsoft Excel] o in un altro editor per modificare qualsiasi campo non ID. È quindi possibile copiare le [!DNL Excel] righe e incollarle nuovamente nella visualizzazione come dati separati da tabulazioni per apportare le modifiche. La funzionalità utilizza gli Appunti del computer.

Puoi utilizzare questa funzione per modificare gli oggetti campagna esistenti (con i campi ID ) e per creare nuovi oggetti campagna senza i campi ID.

## Copiare righe di dati

1. Nel menu principale, fare clic su **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nei sottomenu, fare clic su **[!UICONTROL Live]> \[[!UICONTROL Campaigns] \| [!UICONTROL Ad Groups] \| [!UICONTROL Keywords] \| [!UICONTROL Ads]\]**.

1. Selezionare la casella di controllo accanto a ogni riga da copiare.

   Puoi copiare fino a 10.000 righe.

1. Nella barra degli strumenti sopra la tabella dati fare clic su ![Altro](/help/search-social-commerce/assets/more.png "Altro") e quindi su **[!UICONTROL Copy]**.

   In alternativa, è possibile utilizzare il comando di tastiera &quot;copia&quot; del sistema operativo, ad esempio **[!DNL Ctrl+C]** per [!DNL Microsoft Windows] o **[!DNL Command-C]** per [!DNL Apple Mac].

1. Nella finestra di dialogo [!UICONTROL Copy to Clipboard], fare clic su **[!UICONTROL Continue]**. Quando i dati sono pronti per la copia, fare clic su **[!UICONTROL Copy]**.

1. Incollare le righe in [!DNL Excel] o in un altro editor.

## Modificare e creare righe di dati

1. Modificare i dati in base ai seguenti requisiti:

   * I dati incollati devono includere una riga di intestazione e i valori dell&#39;oggetto campagna necessari. Vedere le colonne del bulksheet richieste per [Baidu](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-baidu.md), [Google Ads](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md), [Microsoft Advertising](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md), [Naver](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md), [Yahoo! Visualizza rete](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-display-network.md), [Yahoo! Giappone](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-japan.md) e [Yandex](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yandex.md). L&#39;ordine delle colonne non ha importanza.

      * Per gli oggetti esistenti che si desidera modificare, è necessario includere tutte le colonne ID rilevanti, i nomi delle entità e l&#39;attributo da modificare. Non modificare l&#39;ID numerico dell&#39;oggetto.

      * Per i nuovi oggetti campagna, includi tutti i nomi e gli attributi di entità rilevanti, ma non gli ID oggetto (che vengono generati automaticamente). Ad esempio, se crei un nuovo annuncio, lascia vuoto il campo [!UICONTROL Ad ID]. La rete di annunci crea automaticamente un ID quando inserisci l’oggetto.

   * Il valore in una colonna non obbligatoria può essere nullo (vuoto), ma ogni riga deve avere lo stesso numero di valori separati da tabulazioni.

1. Salva i dati come valori separati da tabulazioni.

## Incollare le righe di dati nelle visualizzazioni di gestione delle campagne

>[!NOTE]
>
>Se le righe incollate contengono dati identici a quelli delle entità esistenti o che duplicano un&#39;entità esistente, i dati duplicati vengono ignorati.

1. In [!DNL Excel] o in un altro editor, copiare le righe separate da tabulazioni pertinenti.

1. Nel menu principale di Ricerca, Social e Commerce, fare clic su **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Apri la visualizzazione in cui incollare i dati (**[!UICONTROL Live]> \[[!UICONTROL Campaigns] \| [!UICONTROL Ad Groups] \| [!UICONTROL Keywords] \| [!UICONTROL Ads]\]**).

1. Nella barra degli strumenti sopra la tabella dati fare clic su ![Altro](/help/search-social-commerce/assets/more.png "Altro") e quindi su **[!UICONTROL Paste]**.

   In alternativa, è possibile utilizzare il comando &quot;incolla&quot; della tastiera del sistema operativo, ad esempio **[!DNL Ctrl+V]** per [!DNL Microsoft Windows] o **[!DNL Command-V]** per [!DNL Apple Mac].

1. Incollare i dati nella casella di input, quindi fare clic su **[!UICONTROL Process]**.

1. (Facoltativo) Immettere ulteriori dettagli:

   * (Se **[!UICONTROL Additional Details]** è compresso) Fare clic su ![Apri](/help/search-social-commerce/assets/chevron-up.png "Apri") per espandere i dettagli.

   * Immettere un **[!UICONTROL Job Name]** facoltativo e/o un **[!UICONTROL Job Description]** facoltativo.

1. Fare clic su **[!UICONTROL Post Now]**.


>[!MORELIKETHIS]
>
>* [Informazioni sulla gestione dei dati della campagna tramite bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)
>* [Modificare le impostazioni direttamente in una riga](/help/search-social-commerce/common-tasks/settings-edit-within-row.md)
>* [Gestisci campagne](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
>* [Gestisci gruppi di annunci](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
>* [Gestisci parole chiave](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
>* [Gestione annunci](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md)
