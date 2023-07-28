---
title: Gestisci [!DNL Google Ads] posizionamenti
description: Scopri come creare e gestire i posizionamenti che possono essere offerti per [!DNL Google Ads] gruppi di annunci.
exl-id: 91fee1eb-d1d5-4a1b-b1a6-369b98269100
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%

---

# Gestisci [!DNL Google Ads] posizionamenti

*[!DNL Google Ads]solo account*

Puoi creare e modificare i posizionamenti per i gruppi di annunci in [tipi di campagna supportati](/help/search-social-commerce/introduction/supported-inventory.md) che si rivolgono alla rete di visualizzazione all&#39;interno di un [account di rete dell&#39;annuncio sincronizzato](/help/search-social-commerce/campaign-management/accounts/ad-network-account-about.md)

## Crea [!DNL Google Ads] posizionamenti

>[!TIP]
>
>Per creare più posizionamenti contemporaneamente, utilizza [bulksheet delle campagne](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nei sottomenu, fare clic su **[!UICONTROL Live]> [!UICONTROL Placements] >[!UICONTROL Placements]**.

1. 
   1. Nella barra degli strumenti sopra la tabella dati, fai clic su ![Crea](/help/search-social-commerce/assets/add.png "Crea").

1. Seleziona la rete di annunci, l’account, la campagna e il gruppo di annunci, quindi fai clic su **[!UICONTROL Continue]**.

1. Configurare [impostazioni di posizionamento](#placement-settings).

1. Clic **[!UICONTROL Post]**.

## Modifica [!DNL Google Ads] posizionamenti

>[!TIP]
>
>Per modificare più posizionamenti contemporaneamente, utilizza [bulksheet delle campagne](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nei sottomenu, fare clic su **[!UICONTROL Live]> [!UICONTROL Keywords] >[!UICONTROL Keywords]**.

1. Selezionare la casella di controllo accanto a ogni riga da modificare.

   Per suggerimenti sulla selezione di più righe, vedere &quot;[Seleziona più righe](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

1. Nella barra degli strumenti sopra la tabella dati, fai clic su ![Modifica](/help/search-social-commerce/assets/edit.png "Modifica") .

1. Modifica il [impostazioni di posizionamento](#placement-settings).

   Per più posizionamenti, le modifiche vengono applicate a tutti i posizionamenti selezionati. Per alcuni campi alfanumerici è possibile modificare i valori esistenti in un valore specificato, sostituire una stringa esistente con una stringa specificata, aggiungere un prefisso specificato all&#39;inizio di ogni valore o aggiungere un suffisso alla fine di ogni valore. Per alcuni campi monetari, è possibile modificare i valori esistenti in un valore specificato oppure aumentare o diminuire l&#39;importo di una percentuale o di un importo monetario specificato, con un limite.

1. Salvare i dati:

   * (Posizionamenti singoli) Fai clic su **[!UICONTROL Post]**.

   * (Più posizionamenti) Fai clic su **[!UICONTROL Post Now]**.

## Impostazioni di posizionamento {#placement-settings}

### [!UICONTROL Placement Details]

**[!UICONTROL Placements]:** Siti sulla rete di contenuti in cui l’annuncio può essere visualizzato. Immetti un URL valido, ad esempio www.example.com, example.com o www.example.com/shoes/kids. Per specificare più stringhe, separarle con virgole o immetterle su righe separate. L&#39;URL non può includere un punto interrogativo (`?`). **Nota:** È possibile [escludi posizionamenti sito web](placement-negative-create.md) dal [!UICONTROL Placements] > [!UICONTROL Negatives] visualizza e nelle impostazioni del gruppo di annunci e della campagna.

**[!UICONTROL Status]:** Lo stato di visualizzazione del posizionamento: *Attivo* (per abilitare le offerte; impostazione predefinita), *In pausa* (per disabilitare l&#39;offerta), oppure *Eliminato* (per eliminare il posizionamento; solo posizionamenti esistenti).

### [!UICONTROL Bids]

**[!UICONTROL Bid]:** (Facoltativo) Il costo massimo per clic (CPC) o il costo per mille impression visualizzabili (vCPM) per l’annuncio basato sul posizionamento, a seconda della strategia di offerta della campagna. Questo valore sostituisce l&#39;offerta a livello di gruppo di annunci.

<!-- If the placement is in a standard optimized portfolio, then the specified bid is applied for one day. Afterward, the optimization capability places bids according to its own calculations. -->

### [!UICONTROL Tracking URLs]

<!-- **[!UICONTROL Base URL]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

<!-- note -->

{{$include /help/_includes/base-url-google-note.md}}

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

>[!MORELIKETHIS]
>
>* [Informazioni sui posizionamenti](placement-about.md)
>* [Creare posizionamenti negativi](placement-negative-create.md)
>* [Modificare lo stato dei posizionamenti e dei posizionamenti negativi](placement-status-edit.md)
