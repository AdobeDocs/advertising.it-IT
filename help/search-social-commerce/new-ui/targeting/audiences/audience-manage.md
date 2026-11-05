---
title: Gestire i tipi di pubblico
description: Scopri la libreria dei tipi di pubblico e come gestire i tipi di pubblico supportati per Google Ads e Microsoft Advertising.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
    internal-label: Campaign management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
source-git-commit: 7e7dcde9fb195e04025a1a8d89e792ff562b053f
workflow-type: tm+mt
source-wordcount: '630'
ht-degree: 0%
---
# Gestire i tipi di pubblico

Solo *[!DNL Google Ads]e [!DNL Microsoft Advertising] account*

Un pubblico è un gruppo di utenti che puoi utilizzare come [target](audience-targets-manage.md) o [esclusione](audience-exclusions.md) per campagne e gruppi di annunci supportati nella stessa rete di annunci. La rete di annunci determina la dimensione del pubblico che deve essere targetizzabile.

## Informazioni sulla visualizzazione [!UICONTROL Library] {#audience-view-about}

Nella visualizzazione [!UICONTROL Targeting] > [!UICONTROL Audiences] > [!UICONTROL Library] sono elencati i tipi di pubblico per l&#39;inserzionista selezionato. Per visualizzare i tipi di pubblico [!DNL Google Ads] e [!DNL Microsoft Advertising], selezionare **[!UICONTROL All Other Network]** dal menu **[!UICONTROL Network]**.

La libreria include [!DNL Google Ads] tipi di pubblico basati su dati cliente, di mercato e simili e [!DNL Microsoft Advertising] tipi di pubblico di remarketing, remarketing dinamico, personalizzato, customer match, in-market e simili.

La visualizzazione dei dati richiede l&#39;autorizzazione [!UICONTROL View Audiences]. La selezione delle righe e l&#39;eliminazione dei tipi di pubblico supportati richiede l&#39;autorizzazione [!UICONTROL Edit Audience Library].

### Azioni disponibili

<!--
Restricted to internal beta users:

* [Create a customer match audience from a customer data list](#audience-customer-list-create)

* [Create a Google Ads audience from Adobe audiences](#audience-adobe-create)

* [Create a Microsoft Advertising dynamic remarketing audience](#audience-dynamic-create)

* [Update a customer match audience using a customer data list](#audience-customer-list-edit)

* [Edit a dynamic remarketing audience](#audience-dynamic-edit)
-->

* [Eliminare un pubblico di remarketing dinamico](#audience-delete)

* [Copia tutti i dati nelle righe selezionate negli Appunti](#copy-to-clipboard)

## Origini dati del pubblico {#audience-data-sources}

Puoi utilizzare i tipi di pubblico in base alle seguenti origini dati:

* **Segmenti di pubblico di Adobe:** gli inserzionisti con account Adobe Audience Manager o Adobe Analytics con consenso possono utilizzare [!DNL Google Ads] tipi di pubblico con corrispondenza cliente in base ai segmenti [!DNL Adobe] esistenti.

  * Per gli inserzionisti con account [!DNL Analytics] che non dispongono di Audience Manager, il pubblico utilizza gli ID utente di [!DNL Analytics] segmenti condivisi con Adobe CX Enterprise.

  * Per gli inserzionisti con account Audience Manager, il pubblico utilizza gli ID utente dei segmenti Audience Manager con Search, Social e Commerce come destinazione. Possono includere [!DNL Analytics] segmenti pubblicati in Adobe CX Enterprise e segmenti creati utilizzando la Libreria tipi di pubblico di Adobe CX Enterprise.

  L&#39;account [!DNL Google Ads] deve essere [idoneo per customer match](https://support.google.com/adspolicy/answer/6299717) e ha acconsentito a [segmenti ID utente](https://support.google.com/google-ads/answer/9199250). L’account dell’inserzionista in Search, Social e Commerce deve essere configurato anche per consentire la creazione di tipi di pubblico in base ai clienti. Contatta il team del tuo account Adobe per abilitare questa funzione.

  [!DNL Adobe] i dati dei segmenti e i file di sincronizzazione dei cookie per i tipi di pubblico basati su dati del cliente vengono sincronizzati con [!DNL Google Ads] al giorno.

* **Elenchi e-mail di Adobe Campaign:** Il team dell&#39;account di Adobe può aiutarti a configurare un flusso di lavoro per creare e aggiornare un pubblico con corrispondenza cliente [!DNL Google Ads] da un elenco e-mail in [!DNL Campaign]. Il flusso di lavoro è configurato in [!DNL Campaign], non nella libreria del pubblico. Consulta &quot;[Creare un pubblico di corrispondenza cliente da un elenco e-mail di Adobe Campaign](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-campaign-email-list.md).&quot;

* **Elenchi dati cliente:** Gli inserzionisti con account idonei [!DNL Google Ads] o [!DNL Microsoft Advertising] possono utilizzare i tipi di pubblico di corrispondenza cliente basati su file CSV contenenti identificatori primari dai sistemi CRM (Customer Relationship Management).

* **Elenchi di remarketing dinamico:** gli inserzionisti con [!DNL Microsoft Advertising] account possono utilizzare tipi di pubblico in base agli utenti che hanno recentemente interagito con i loro prodotti, ad esempio i visualizzatori di prodotti o gli acquirenti precedenti. Questi tipi di pubblico richiedono il tag di conversione JavaScript e di tracciamento del pubblico della rete di annunci sulle relative pagine web.

  I tipi di pubblico di remarketing dinamico possono essere utilizzati con campagne di acquisto sulle reti di ricerca e pubblico per effettuare il retargeting degli utenti con annunci di prodotti e con campagne di ricerca per indirizzare nuovamente gli utenti con annunci di testo e annunci di ricerca dinamici.

  >[!NOTE]
  >
  >I modificatori di offerte per i target del pubblico di remarketing dinamico non sono ottimizzati nei portfolio con l&#39;impostazione [!UICONTROL Auto-optimize Bid Adjustment Values].

>[!NOTE]
>
>Search, Social e Commerce non memorizzano i dati dei clienti caricati o i dati dei clienti dai segmenti [!DNL Adobe] utilizzati per creare o modificare un pubblico.

<!--
Restricted to internal beta users: audience creation and library editing.

## Create a customer match audience from a customer data list {#audience-customer-list-create}

*[!DNL Google Ads] and [!DNL Microsoft Advertising] accounts that are eligible for customer match only*

For [!DNL Microsoft Advertising], the file can include email addresses. For [!DNL Google Ads], the file can include email addresses, mailing addresses, telephone numbers, user IDs, or mobile device IDs.

Creating and editing library audiences requires the [!UICONTROL Edit Audience Library] permission in addition to internal beta access.

1. Prepare a CSV file with the customer data in the required format.

   First and last names, email addresses, and telephone numbers must be hashed using SHA-256. Follow the network's formatting requirements for the selected identifier type. See the [Google Ads formatting guidelines](https://support.google.com/google-ads/answer/7476159) or the [Microsoft Advertising instructions for preparing customer match lists](https://help.ads.microsoft.com/#apex/ads/en/56921).

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Library]** tab.

1. Select **[!UICONTROL All Other Network]** from the **[!UICONTROL Network]** menu.

1. Click **[!UICONTROL Create Audience]**.

1. In **[!UICONTROL Basic Settings]**, select the ad network and account.

1. In **[!UICONTROL Data Source]**, select the customer-list option.

1. Enter the **[!UICONTROL Audience Name]** and select the **[!UICONTROL Data Upload Type]**:

   * ([!DNL Microsoft Advertising]) **[!UICONTROL Emails]**.

   * ([!DNL Google Ads]) **[!UICONTROL Emails, Phones, and/or Mailing Addresses]**, **[!UICONTROL User IDs]**, or **[!UICONTROL Mobile Device IDs]**.

     User ID lists are available only to eligible [!DNL Google Ads] advertisers in the U.S. who are opted in for user ID segments.

1. (Mobile device ID lists only) Select the **[!UICONTROL OS Type]** and enter the **[!UICONTROL App ID]**.

   For an Android app, use its package name in [!DNL Google Play], such as `com.example.game` from `https://play.google.com/store/apps/details?id=com.example.game`. For an iOS app, use its application ID from the [!DNL App Store], such as `id284882215`. Your development team can provide the ID.

1. In **[!UICONTROL Select File]**, select the CSV file from your device or network.

1. Select the check box to indicate that you agree with the [!DNL Adobe] and ad network privacy policies.

1. ([!DNL Google Ads]; optional) If you do business in the European Economic Area (EEA) or United Kingdom (UK) and have collected all required user consents, select the consent check box to send the consent status as **[!UICONTROL GRANTED]** for advertising and ad personalization.

   If you leave the check box unselected, the consent status is sent as **[!UICONTROL UNSPECIFIED]**. [!DNL Google Ads] ignores data for EEA and UK users with an unspecified consent status, which can cause data discrepancies and performance issues.

1. Click **[!UICONTROL Upload File]** and wait for the upload to finish.

1. Configure any remaining audience settings, including **[!UICONTROL Membership Days]** when available.

   Membership days specify how long a user's cookie stays in the audience. Use the length of time for which you expect the ad to remain relevant. Customer lists don't expire unless you enter a value.

1. Click **[!UICONTROL Review and Save]**.

1. Review the settings. To change a setting, click **[!UICONTROL Edit]** in the applicable section.

1. Click **[!UICONTROL Create]**.

The ad network may take up to 24 hours to process the file. See the [Google Ads documentation on customer match and its limitations](https://support.google.com/displayvideo/answer/9539301).

## Create Google Ads customer match audiences from Adobe audiences {#audience-adobe-create}

*Advertisers with an Adobe Advertising-Adobe Audience Manager or Adobe Advertising-Adobe Analytics integration only*

Each [!DNL Adobe] audience can be used for only one [!DNL Google Ads] audience. Each new audience has the same name as the original [!DNL Adobe] audience.

1. Complete the prerequisites:

   1. Ask an [!DNL Adobe] administrator or account manager to enable customer match audiences for the advertiser.

   1. Implement the [Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=it){target="_blank"} version 2.0 or higher.

   1. Deploy the following tag as high as possible on the advertiser's webpages from which the audience should be tracked:

      `<script src="//pixel.everesttech.net/rlsa/<Advertising_Cloud_UserID>" type="text/javascript"> </script>`

      Replace `Advertising_Cloud_UserID` with the advertiser's unique numeric user ID.

   1. Have an authorized user [configure synchronization with the advertiser's organization account in Adobe CX Enterprise](/help/search-social-commerce/admin/sync-adobe-audiences.md).

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Library]** tab.

1. Select **[!UICONTROL All Other Network]** from the **[!UICONTROL Network]** menu, and then click **[!UICONTROL Create Audience]**.

1. In **[!UICONTROL Basic Settings]**, select [!DNL Google Ads] and the account.

1. In **[!UICONTROL Data Source]**, select the Adobe audience option.

1. In **[!UICONTROL Adobe Audience]**, select one or more available segments. You can search the list.

   Segments already used for another [!DNL Google Ads] audience aren't available. If you select multiple segments, a separate audience is created for each segment.

1. Select the available customer list user ID option in **[!UICONTROL Audience Type]**.

1. Select the check box to indicate that you agree with the [!DNL Adobe] and ad network privacy policies.

1. Configure any remaining audience settings, including **[!UICONTROL Membership Days]** when available.

   Remarketing lists have a maximum duration of 540 days. Customer lists don't have a maximum duration; enter 10000 to indicate that the cookie never expires.

1. Click **[!UICONTROL Review and Save]**, review the settings, and then click **[!UICONTROL Create]**.

Search, Social, & Commerce automatically pushes a [!DNL Google] tracking URL back to each source segment so that [!DNL Google] can track the audience. [!DNL Google] may take up to 24 hours to process the audience.

>[!TIP]
>
>For real-time segmentation, use Audience Manager-created audiences. [!DNL Analytics] segments synced to Adobe CX Enterprise may have smaller populations because they're synced daily. Users who qualify for a segment may not be included until the next day.

## Create a Microsoft Advertising dynamic remarketing audience {#audience-dynamic-create}

You can create multiple dynamic remarketing audiences using the same tracking tag.

1. Implement the [Microsoft Advertising universal event tracking (UET) tag with the required product ID and page type parameters](https://help.ads.microsoft.com/#apex/ads/en/56910/1/#exp85) on the relevant webpages. Identify the tag's name.

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Library]** tab.

1. Select **[!UICONTROL All Other Network]** from the **[!UICONTROL Network]** menu, and then click **[!UICONTROL Create Audience]**.

1. In **[!UICONTROL Basic Settings]**, select [!DNL Microsoft Advertising] and the account.

1. In **[!UICONTROL Data Source]**, select the dynamic remarketing list option.

1. Enter the **[!UICONTROL Audience Name]**.

1. In **[!UICONTROL Tag Name]**, select the UET tag on the webpages whose users comprise the audience.

1. In **[!UICONTROL Whom to add to your audience]**, select **[!UICONTROL General Visitors]**, **[!UICONTROL Product Searchers]**, **[!UICONTROL Product Viewers]**, **[!UICONTROL Past Buyers]**, or **[!UICONTROL Shopping Cart Abandoners]**.

1. Configure any remaining audience settings, including **[!UICONTROL Membership Days]** when available. For dynamic remarketing audiences, membership can range from 1-180 days.

1. Click **[!UICONTROL Review and Save]**, review the settings, and then click **[!UICONTROL Create]**.

Dynamic remarketing audiences are eligible for targeting once they include at least 300 users.

## Update a customer match audience using a customer data list {#audience-customer-list-edit}

You can update customer match audiences created from data files, but not [!DNL Google Ads] audiences created from [!DNL Adobe] audiences. You can add or delete members, or replace all existing members. You can't edit multiple library audiences at once.

1. Prepare a CSV file in the required format, using the same data type as the original list. For mobile device IDs, use the same app and operating system.

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Library]** tab.

1. Select **[!UICONTROL All Other Network]** from the **[!UICONTROL Network]** menu.

1. Select the check box next to one audience, and then click **[!UICONTROL Edit]** in the bulk actions toolbar.

1. In **[!UICONTROL Select Action]**, select:

   * **[!UICONTROL Add]:** Add members from the uploaded file who aren't already in the audience.

   * **[!UICONTROL Delete]:** Remove members in the uploaded file from the audience.

   * **[!UICONTROL Replace]:** Replace all existing audience members with the uploaded data.

1. In **[!UICONTROL Select File]**, select the CSV file, accept the privacy policies, and configure the applicable consent setting.

1. Click **[!UICONTROL Upload File]** and wait for the upload to finish.

1. Click **[!UICONTROL Review and Save]**, review the settings, and then click **[!UICONTROL Update]**.

The ad network may take a while to process audience updates.

## Edit a dynamic remarketing audience {#audience-dynamic-edit}

You can change a [!DNL Microsoft Advertising] dynamic remarketing audience's name, UET tag, and visitor type. You can't change its membership duration or edit multiple library audiences at once.

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Library]** tab.

1. Select **[!UICONTROL All Other Network]** from the **[!UICONTROL Network]** menu.

1. Select the check box next to one dynamic remarketing audience, and then click **[!UICONTROL Edit]** in the bulk actions toolbar.

1. Edit the **[!UICONTROL Audience Name]**, **[!UICONTROL Tag Name]**, or **[!UICONTROL Whom to add to your audience]**.

1. Click **[!UICONTROL Review and Save]**, review the settings, and then click **[!UICONTROL Update]**.
-->

## Eliminare un pubblico di remarketing dinamico {#audience-delete}

Puoi eliminare [!DNL Microsoft Advertising] tipi di pubblico di remarketing dinamico uno alla volta. Non puoi eliminare altri tipi di pubblico [!DNL Google Ads] o [!DNL Microsoft Advertising] dalla libreria.

1. Nel menu principale fare clic su **[!UICONTROL Targeting]>[!UICONTROL Audiences]** e quindi sulla scheda **[!UICONTROL Library]**.

1. Selezionare **[!UICONTROL All Other Network]** dal menu **[!UICONTROL Network]**.

1. Seleziona la casella di controllo accanto a un pubblico di remarketing dinamico.

1. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL Delete]**.

1. Nel messaggio di conferma, fare clic su **[!UICONTROL Confirm]**.

## Copia tutti i dati nelle righe selezionate negli Appunti {#copy-to-clipboard}

Copiare le informazioni visibili nelle righe selezionate, in base ai filtri applicati e alle colonne visibili nella vista. Le informazioni vengono salvate come valori separati da tabulazioni (TSV).

1. Selezionare la casella di controllo accanto a ogni riga di cui si desidera copiare i dati.

1. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL Copy]**.

>[!MORELIKETHIS]
>
>* [Gestione dei target del pubblico per campagne e gruppi di annunci](audience-targets-manage.md)
>* [Gestire le esclusioni di pubblico per campagne e gruppi di annunci](audience-exclusions.md)
