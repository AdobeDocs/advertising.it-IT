---
title: Gestisci  [!DNL Google Ads]  posizionamenti
description: Scopri come creare e gestire posizionamenti che possono essere offerti per  [!DNL Google Ads]  gruppi di annunci.
exl-id: 80cb6fc6-e778-4b19-9e52-e0b57bde0d73
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 0%

---

# Gestisci [!DNL Google Ads] posizionamenti

Solo *[!DNL Google Ads]account*

Puoi creare e modificare i posizionamenti per i gruppi di annunci in [tipi di campagne supportati](/help/search-social-commerce/introduction/supported-inventory.md) che eseguono il targeting della rete di visualizzazione in un [account di rete di annunci sincronizzato](/help/search-social-commerce/campaign-management/accounts/ad-network-account-about.md)

## Crea [!DNL Google Ads] posizionamenti

>[!TIP]
>
>Per creare più posizionamenti contemporaneamente, utilizza [bulksheet campagna](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Nel menu principale, fare clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nei sottomenu, fare clic su **[!UICONTROL Live]> [!UICONTROL Placements] >[!UICONTROL Placements]**.

1. 
   1. Nella barra degli strumenti sopra la tabella dati, fare clic su ![Crea](/help/search-social-commerce/assets/add.png "Crea").

1. Selezionare la rete di annunci, l&#39;account, la campagna e il gruppo di annunci, quindi fare clic su **[!UICONTROL Continue]**.

1. Configura le [impostazioni di posizionamento](#placement-settings).

1. Fare clic su **[!UICONTROL Post]**.

## Modifica [!DNL Google Ads] posizionamenti

>[!TIP]
>
>Per modificare più posizionamenti contemporaneamente, utilizza [bulksheet campagna](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Nel menu principale, fare clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nei sottomenu, fare clic su **[!UICONTROL Live]> [!UICONTROL Keywords] >[!UICONTROL Keywords]**.

1. Selezionare la casella di controllo accanto a ogni riga da modificare.

   Per suggerimenti sulla selezione di più righe, vedere &quot;[Selezionare più righe](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Nella barra degli strumenti sopra la tabella dati, fare clic su ![Modifica](/help/search-social-commerce/assets/edit.png "Modifica").

1. Modifica le [impostazioni di posizionamento](#placement-settings).

   Per più posizionamenti, le modifiche vengono applicate a tutti i posizionamenti selezionati. Per alcuni campi alfanumerici è possibile modificare i valori esistenti in un valore specificato, sostituire una stringa esistente con una stringa specificata, aggiungere un prefisso specificato all&#39;inizio di ogni valore o aggiungere un suffisso alla fine di ogni valore. Per alcuni campi monetari, è possibile modificare i valori esistenti in un valore specificato oppure aumentare o diminuire l&#39;importo di una percentuale o di un importo monetario specificato, con un limite.

1. Salvare i dati:

   * (Posizionamenti singoli) Fare clic su **[!UICONTROL Post]**.

   * (Più posizionamenti) Fare clic su **[!UICONTROL Post Now]**.

## Impostazioni di posizionamento {#placement-settings}

### [!UICONTROL Placement Details]

**[!UICONTROL Placements]:** siti nella rete di contenuti in cui può essere visualizzato l&#39;annuncio. Immetti un URL valido, ad esempio www.example.com, example.com o www.example.com/shoes/kids. Per specificare più stringhe, separarle con virgole o immetterle su righe separate. L&#39;URL non può includere un punto interrogativo (`?`). **Nota:** puoi [escludere i posizionamenti del sito Web](placement-negative-create.md) dalla visualizzazione [!UICONTROL Placements] > [!UICONTROL Negatives] e dalle impostazioni del gruppo di annunci e della campagna.

**[!UICONTROL Status]:** Lo stato di visualizzazione del posizionamento: *Attivo* (per abilitare l&#39;offerta; impostazione predefinita), *In pausa* (per disabilitare l&#39;offerta) o *Eliminato* (per eliminare il posizionamento; solo i posizionamenti esistenti).

### [!UICONTROL Bids]

**[!UICONTROL Bid]:** (facoltativo) il costo massimo per clic (CPC) o il costo per mille impression visualizzabili (vCPM) per l&#39;annuncio basato sul posizionamento, a seconda della strategia di offerta della campagna. Questo valore sostituisce l&#39;offerta a livello di gruppo di annunci.

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
>* [Crea posizionamenti negativi](placement-negative-create.md)
>* [Modifica lo stato dei posizionamenti e dei posizionamenti negativi](placement-status-edit.md)
