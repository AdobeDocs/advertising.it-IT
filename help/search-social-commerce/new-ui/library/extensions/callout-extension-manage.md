---
title: Gestire le estensioni di callout condivise di Google Ads
description: Scopri come creare, modificare ed eliminare le estensioni di callout condivise di Google Ads.
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
source-git-commit: 10d7adc3b3ced812ee1281139a23a573df2beeef
workflow-type: tm+mt
source-wordcount: '685'
ht-degree: 0%
---
# Gestisci estensioni callout condivise di [!DNL Google Ads]

Solo *[!DNL Google Ads]account*

Un&#39;estensione del callout è un testo informativo su un prodotto, un servizio o una promozione offerti dal sito, visualizzato con un annuncio testuale. La rete di annunci potrebbe mostrare 2-4 callout con un annuncio.

È possibile creare il testo e le impostazioni del callout condiviso a livello di account per un account di Google Ads [sincronizzato](/help/search-social-commerce/new-ui/manage/accounts/api-accounts/api-account-manage.md). I callout nella libreria non vengono utilizzati con gli annunci fino a quando non li associ a una campagna o a un gruppo di annunci supportato nella rete di ricerca.

Per rendere i tuoi annunci pubblicitari visibili con i callout, assegna almeno due callout per campagna o gruppo di annunci. I callout a livello di gruppo di annunci sostituiscono i callout a livello di campagna.

## Informazioni sulle visualizzazioni [!UICONTROL Callouts] e [!UICONTROL Associations] {#callout-view-about}

In **[!UICONTROL Library]>[!UICONTROL Extensions]**, la scheda **[!UICONTROL Callouts]** elenca i callout condivisi a livello di account. Nella scheda **[!UICONTROL Associations]** sono elencate le associazioni tra estensioni ed entità account.

La visualizzazione di queste schede richiede l&#39;autorizzazione [!UICONTROL View Extensions]. La creazione, la modifica e l&#39;eliminazione di callout nonché la creazione o l&#39;eliminazione di associazioni richiedono l&#39;autorizzazione [!UICONTROL Edit Extensions].

Per conoscere il numero massimo di estensioni per account, consulta la [documentazione di Google Ads sui limiti dell&#39;account](https://support.google.com/google-ads/answer/6372658).

### Azioni disponibili

* [Creare un callout condiviso](#callout-create)

* [Modifica impostazioni callout condivisi](#callout-edit)

* [Elimina callout condivisi](#callout-delete)

* [Associare callout condivisi a campagne e gruppi di annunci](ad-extension-association-manage.md#callout-associate)

* [Eliminare le associazioni di estensione](ad-extension-association-manage.md#association-delete)

* [Copia tutti i dati nelle righe selezionate negli Appunti](#copy-to-clipboard)

## Creare un callout condiviso {#callout-create}

1. Nel menu principale fare clic su **[!UICONTROL Library]>[!UICONTROL Extensions]** e quindi sulla scheda **[!UICONTROL Callouts]**.

1. Fare clic su **[!UICONTROL Create Callout]**.

1. In **[!UICONTROL Basic Settings]**, selezionare [!DNL Google Ads] e l&#39;account.

1. Immetti le [impostazioni callout condivisi](#shared-callout-settings).

1. Fare clic su **[!UICONTROL Review and Save]**.

1. Controlla le impostazioni. Per modificare un&#39;impostazione, fare clic su **[!UICONTROL Edit]** nella sezione applicabile.

1. Fare clic su **[!UICONTROL Create]**.

Dopo aver creato il callout, [associarlo a una campagna o a un gruppo di annunci](ad-extension-association-manage.md#callout-associate).

## Modifica impostazioni callout condivisi {#callout-edit}

È possibile modificare un callout condiviso alla volta. Non puoi modificarne la data di inizio dopo averla creata.

1. Nel menu principale fare clic su **[!UICONTROL Library]>[!UICONTROL Extensions]** e quindi sulla scheda **[!UICONTROL Callouts]**.

1. Selezionare la casella di controllo accanto a un callout.

1. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL Edit]**.

1. Modifica le [impostazioni callout condivisi](#shared-callout-settings).

1. Fare clic su **[!UICONTROL Review and Save]**, rivedere le impostazioni e quindi fare clic su **[!UICONTROL Update]**.

## Elimina callout condivisi {#callout-delete}

1. Nel menu principale fare clic su **[!UICONTROL Library]>[!UICONTROL Extensions]** e quindi sulla scheda **[!UICONTROL Callouts]**.

1. Selezionare la casella di controllo accanto a ogni callout condiviso da eliminare.

   Per informazioni sulla selezione di più righe, vedere &quot;[Selezionare più righe](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

1. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL Delete]**.

1. Nel messaggio di conferma, fare clic su **[!UICONTROL Confirm]**.

Per rimuovere un&#39;associazione senza eliminare il callout condiviso dalla libreria, [eliminare l&#39;associazione](ad-extension-association-manage.md#association-delete).

## Copia tutti i dati nelle righe selezionate negli Appunti {#copy-to-clipboard}

Copiare le informazioni visibili nelle righe selezionate, in base ai filtri applicati e alle colonne visibili nella vista. Le informazioni vengono salvate come valori separati da tabulazioni (TSV).

1. Selezionare la casella di controllo accanto a ogni riga di cui si desidera copiare i dati.

1. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL Copy]**.

## Impostazioni callout condivisi {#shared-callout-settings}

Per ulteriori criteri e motivi per la disapprovazione del callout, vedere [Requisiti del callout di Google Ads](https://support.google.com/adspolicy/answer/1054212).

**[!UICONTROL Callout Text]:** Il testo da visualizzare. Può contenere fino a 25 caratteri a byte singolo o 12 caratteri a byte doppio. Non può includere punti esclamativi o punteggiatura all&#39;inizio del testo.

**[!UICONTROL Start Date]:** (facoltativo; solo creazione) La prima data in cui il callout può essere visualizzato. Il valore predefinito è il giorno corrente. Per specificare una data futura, immetterla nel formato MM/GG/AAAA o utilizzare il selettore data. La data di inizio è di sola lettura per i callout esistenti.

**[!UICONTROL End Date]:** (facoltativo) ultima data in cui è possibile visualizzare il callout. Per impostazione predefinita, il callout può essere visualizzato indefinitamente. Per specificare una data di fine, immetterla in formato MM/GG/AAAA o utilizzare il selettore data.

**[!UICONTROL Mobile Preference]:** (facoltativo) consente a [!DNL Google Ads] di provare a visualizzare l&#39;estensione agli utenti di dispositivi mobili anziché agli utenti di desktop o tablet. In caso contrario, l’estensione può essere visualizzata su qualsiasi tipo di dispositivo. [!DNL Google Ads] non garantisce che l&#39;estensione verrà visualizzata sul tipo di dispositivo preferito.

## Dati sulle prestazioni per i callout {#callout-performance}

Search, Social e Commerce mappano i clic su un’estensione dell’annuncio e le conversioni risultanti alla parola chiave associata all’annuncio in cui viene visualizzata l’estensione. I dati sui costi e sui clic a livello di estensione non sono disponibili in Search, Social e Commerce.

È possibile visualizzare il costo a livello di estensione e fare clic sui dati nell&#39;interfaccia [!DNL Google Ads].

>[!MORELIKETHIS]
>
>* [Gestione estensioni sitelink condivise](sitelink-extension-manage.md)
>* [Gestire le associazioni di estensione dell&#39;annuncio](ad-extension-association-manage.md)
