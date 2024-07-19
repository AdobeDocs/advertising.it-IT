---
title: Creare parole chiave negative
description: Scopri come creare parole chiave negative per campagne di ricerca e gruppi di annunci.
exl-id: afe786bf-eda8-4590-b471-3fb696c420de
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---

# Creare parole chiave negative

Solo *[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] e [!DNL Baidu] account esistenti*

È possibile creare parole chiave negative per un gruppo di annunci di ricerca o una campagna che esegue il targeting della ricerca o della rete di visualizzazione/nativa. Le parole chiave negative non attivano gli annunci.

>[!NOTE]
>È inoltre possibile creare e modificare le parole chiave negative nelle [impostazioni gruppo di annunci](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) e [impostazioni campagna](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md).

>[!TIP]
>Per creare più parole chiave negative contemporaneamente, utilizzare [bulksheet campagna](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Nel menu principale, fare clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nei sottomenu, fare clic su **[!UICONTROL Live]> [!UICONTROL Keywords] >[!UICONTROL Negatives]**.

1. Nella barra degli strumenti sopra la tabella dati, fare clic su ![Crea](/help/search-social-commerce/assets/add.png "Crea"), quindi fare clic su **[!UICONTROL Campaign]** per creare parole chiave negative a livello di campagna o su **[!UICONTROL Ad Group]** per creare parole chiave negative a livello di gruppo di annunci.

1. Selezionare la rete di annunci, l&#39;account, la campagna e, se pertinente, il gruppo di annunci, quindi fare clic su **[!UICONTROL Continue]**.

1. Immettete le parole chiave negative. Utilizzare la seguente sintassi, senza il segno meno (`-`):

   * Corrispondenza ampia negativa: `keyword` (non supportata da [!DNL Microsoft Advertising])

   * Corrispondenza frase negativa: `"keyword"`

   * Corrispondenza esatta negativa: `[keyword]`

   Separare più valori con virgole o immetterli su righe separate. È possibile immettere o incollare fino a 2.000 parole chiave negative in un&#39;unica operazione. Consulta anche i seguenti requisiti e restrizioni:

   * Lunghezza massima dei caratteri: [!DNL Baidu]: 30 byte singolo o 15 byte doppio; [!DNL Microsoft Advertising]: 100 byte singolo o 50 byte doppio; [!DNL Google Ads] e [!DNL Yahoo! Japan Ads]: 80 byte singolo o 40 byte doppio.

   * [!DNL Baidu] consente un solo tipo di corrispondenza per parola chiave per gruppo di annunci. Ad esempio, il gruppo di annunci 1 non può includere sia `"keyword"` che `[keyword]`.

   * [!DNL Google Ads]: ogni parola chiave non può essere costituita da più di 10 parole e può includere solo lettere, cifre e i seguenti caratteri speciali: spazio `# $ & _ - " [ ] ' + . / :`

   * [!DNL Yandex]: ogni parola chiave può avere un massimo di sette parole, escluse le parole non significative. Ogni [!DNL Yandex ad group] può includere un massimo di 200 parole chiave.

1. Fare clic su **[!UICONTROL Post]**.

>[!MORELIKETHIS]
>
>* [Informazioni sulle parole chiave](keyword-about.md)
>* [Gestire le parole chiave disponibili](keyword-manage.md)
>* [Modifica lo stato delle parole chiave e delle parole chiave negative](keyword-status-edit.md)
