---
title: Creare parole chiave negative
description: Scopri come creare parole chiave negative per campagne di ricerca e gruppi di annunci.
exl-id: 683e5395-cb65-4d7f-a981-7fc9f84d4192
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---

# Creare parole chiave negative

*[!DNL Baidu], [!DNL Google Ads] e [!DNL Microsoft® Advertising], e [!DNL Yahoo! Japan Ads] solo account*

È possibile creare parole chiave negative per un gruppo di annunci di ricerca o una campagna che esegue il targeting della ricerca o della rete di visualizzazione/nativa. Le parole chiave negative non attivano gli annunci.

>[!NOTE]
>È inoltre possibile creare e modificare le parole chiave negative nel [impostazioni gruppo di annunci](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) e [impostazioni della campagna](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md).

>[!TIP]
>Per creare più parole chiave negative contemporaneamente, utilizzare [bulksheet delle campagne](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nei sottomenu, fare clic su **[!UICONTROL Live]> [!UICONTROL Keywords] >[!UICONTROL Negatives]**.

1. Nella barra degli strumenti sopra la tabella dati, fai clic su ![Crea](/help/search-social-commerce/assets/add.png "Crea")e quindi fare clic su **[!UICONTROL Campaign]** per creare parole chiave negative a livello di campagna o **[!UICONTROL Ad Group]** per creare parole chiave negative a livello di gruppo di annunci.

1. Seleziona la rete di annunci, l’account, la campagna e (se pertinente) il gruppo di annunci, quindi fai clic su **[!UICONTROL Continue]**.

1. Immettete le parole chiave negative. Utilizza la sintassi seguente, senza il segno meno (`-`):

   * Corrispondenza ampia negativa: `keyword` (non supportato da [!DNL Microsoft® Advertising])

   * Corrispondenza frase negativa: `"keyword"`

   * Corrispondenza esatta negativa: `[keyword]`

   Separare più valori con virgole o immetterli su righe separate. È possibile immettere o incollare fino a 2.000 parole chiave negative in un&#39;unica operazione. Consulta anche i seguenti requisiti e restrizioni:

   * Lunghezza massima carattere: [!DNL Baidu]: 30 a byte singolo o 15 a byte doppio; [!DNL Microsoft® Advertising]: 100 a byte singolo o 50 a byte doppio; [!DNL Google Ads] e [!DNL Yahoo! Japan Ads]: 80 a byte singolo o 40 a byte doppio.

   * [!DNL Baidu] consente un solo tipo di corrispondenza per parola chiave per gruppo di annunci. Ad esempio, il gruppo di annunci 1 non può includere entrambi `"keyword"` e `[keyword]`.

   * [!DNL Google Ads]: ogni parola chiave non può essere composta da più di 10 parole e può includere solo lettere, cifre e i seguenti caratteri speciali: spazio `# $ & _ - " [ ] ' + . / :`

   * [!DNL Yandex]: ogni parola chiave può avere un massimo di sette parole, escluse le parole non significative. Ogni [!DNL Yandex ad group] può includere un massimo di 200 parole chiave.

1. Clic **[!UICONTROL Post]**.

>[!MORELIKETHIS]
>
>* [Informazioni sulle parole chiave](keyword-about.md)
>* [Gestire le parole chiave per le offerte](keyword-manage.md)
>* [Modificare lo stato delle parole chiave e delle parole chiave negative](keyword-status-edit.md)
