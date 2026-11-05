---
title: Gestire le estensioni di sitelink condivise
description: Scopri come creare, modificare ed eliminare le estensioni di sitelink condivise.
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
source-wordcount: '1127'
ht-degree: 0%
---
# Gestire le estensioni di sitelink condivise

Solo *[!DNL Google Ads]e [!DNL Microsoft Advertising] account*

Un sitelink è un collegamento di testo aggiuntivo in un elenco di annunci di testo. Utilizza i sitelink per indirizzare gli utenti direttamente a pagine specifiche del sito. La rete di annunci determina quali sitelink visualizzare in base alla loro rilevanza per l’annuncio.

Facoltativamente, puoi includere un testo descrittivo per ciascun sitelink. La rete di annunci può anche visualizzare la copia dagli annunci esistenti nell&#39;account quando è altamente pertinente per il sitelink. [!DNL Google Ads] potrebbe mostrare 2-6 sitelink in un annuncio desktop e fino a quattro in un annuncio mobile. [!DNL Microsoft Advertising] può mostrare due, quattro o sei sitelink con descrizioni o 4-6 senza descrizioni.

Puoi creare il testo e le impostazioni del sitelink condiviso a livello di account per un [account di rete dell&#39;annuncio sincronizzato](/help/search-social-commerce/new-ui/manage/accounts/api-accounts/api-account-manage.md). I collegamenti di sito nella libreria non vengono utilizzati con gli annunci fino a quando non vengono associati alle entità account.

## Informazioni sulle visualizzazioni [!UICONTROL Sitelinks] e [!UICONTROL Associations] {#sitelink-view-about}

In **[!UICONTROL Library]>[!UICONTROL Extensions]**, la scheda **[!UICONTROL Sitelinks]** elenca i sitelink condivisi a livello di account. Nella scheda **[!UICONTROL Associations]** sono elencate le associazioni tra estensioni ed entità account.

La visualizzazione di queste schede richiede l&#39;autorizzazione [!UICONTROL View Extensions]. La creazione, la modifica e l&#39;eliminazione di sitelink e la creazione o l&#39;eliminazione di associazioni richiedono l&#39;autorizzazione [!UICONTROL Edit Extensions].

Consulta la guida di ad network per il numero massimo di estensioni per [account Google Ads](https://support.google.com/google-ads/answer/6372658) e per [account Microsoft Advertising](https://help.ads.microsoft.com/#apex/3/en/52001).

### Azioni disponibili

* [Creare un sitelink condiviso](#sitelink-create)

* [Modifica impostazioni sitelink condiviso](#sitelink-edit)

* [Eliminare i sitelink condivisi](#sitelink-delete)

* [Associa collegamenti a siti condivisi ad account, campagne e gruppi di annunci](ad-extension-association-manage.md#sitelink-associate)

* [Eliminare le associazioni di estensione](ad-extension-association-manage.md#association-delete)

* [Copia tutti i dati nelle righe selezionate negli Appunti](#copy-to-clipboard)

## Creare un sitelink condiviso {#sitelink-create}

1. Nel menu principale fare clic su **[!UICONTROL Library]>[!UICONTROL Extensions]** e quindi sulla scheda **[!UICONTROL Sitelinks]**.

1. Fare clic su **[!UICONTROL Create Sitelink]**.

1. In **[!UICONTROL Basic Settings]**, selezionare la rete di annunci e l&#39;account.

1. Immetti le [impostazioni del collegamento a sito condiviso](#shared-sitelink-settings).

1. Fare clic su **[!UICONTROL Review and Save]**.

1. Controlla le impostazioni. Per modificare un&#39;impostazione, fare clic su **[!UICONTROL Edit]** nella sezione applicabile.

1. Fare clic su **[!UICONTROL Create]**.

Dopo aver creato il sitelink, [associalo a un account, una campagna o un gruppo di annunci](ad-extension-association-manage.md#sitelink-associate).

## Modifica impostazioni sitelink condiviso {#sitelink-edit}

Puoi modificare un sitelink condiviso alla volta. Non puoi modificarne la data di inizio dopo averla creata.

1. Nel menu principale fare clic su **[!UICONTROL Library]>[!UICONTROL Extensions]** e quindi sulla scheda **[!UICONTROL Sitelinks]**.

1. Selezionare la casella di controllo accanto a un sitelink.

1. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL Edit]**.

1. Modifica le [impostazioni di collegamento a sito condiviso](#shared-sitelink-settings).

1. Fare clic su **[!UICONTROL Review and Save]**, rivedere le impostazioni e quindi fare clic su **[!UICONTROL Update]**.

È inoltre possibile modificare **[!UICONTROL Base URL]** o **[!UICONTROL Tracking Template]** di un sitelink direttamente nella tabella dati facendo clic sul relativo valore.

## Eliminare i sitelink condivisi {#sitelink-delete}

1. Nel menu principale fare clic su **[!UICONTROL Library]>[!UICONTROL Extensions]** e quindi sulla scheda **[!UICONTROL Sitelinks]**.

1. Seleziona la casella di controllo accanto a ciascun sitelink condiviso da eliminare.

   Per suggerimenti sulla selezione di più righe, vedere &quot;[Selezionare più righe](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL Delete]**.

1. Nel messaggio di conferma, fare clic su **[!UICONTROL Confirm]**.

Per rimuovere un&#39;associazione senza eliminare il sitelink condiviso dalla libreria, [eliminare l&#39;associazione](ad-extension-association-manage.md#association-delete).

## Copia tutti i dati nelle righe selezionate negli Appunti {#copy-to-clipboard}

Copiare le informazioni visibili nelle righe selezionate, in base ai filtri applicati e alle colonne visibili nella vista. Le informazioni vengono salvate come valori separati da tabulazioni (TSV).

1. Selezionare la casella di controllo accanto a ogni riga di cui si desidera copiare i dati.

1. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL Copy]**.

## Impostazioni del sitelink condiviso {#shared-sitelink-settings}

Per ulteriori criteri e motivi di disapprovazione del sitelink, consulta [Requisiti del sitelink di Google Ads](https://support.google.com/adspolicy/answer/1054210) e [Requisiti del sitelink di Microsoft Advertising](https://help.ads.microsoft.com/#apex/ads/en/ext60206).

### [!UICONTROL Sitelink]

**[!UICONTROL Link Name]:** Testo da visualizzare per il collegamento. Può contenere fino a 25 caratteri a byte singolo o 12 caratteri a byte doppio. Il testo del collegamento deve essere univoco all’interno dell’account o della campagna.

>[!NOTE]
>
>([!DNL Google Ads]) Il testo esistente di 35 caratteri viene visualizzato negli annunci di desktop e tablet, ma non nei dispositivi mobili.

**[!UICONTROL Status]:** Lo stato di visualizzazione del sitelink: **[!UICONTROL Active]** o **[!UICONTROL Deleted]** per i sitelink esistenti. I nuovi sitelink sono attivi per impostazione predefinita.

**[!UICONTROL Description Line 1], [!UICONTROL Description Line 2]:** Testo aggiuntivo che la rete di annunci potrebbe visualizzare sotto il testo del collegamento. Per includere una descrizione, immettere entrambi i campi. Ciascuno può contenere fino a 35 caratteri a byte singolo o 17 caratteri a byte doppio.

**[!UICONTROL Start Date]:** (Facoltativo; solo creazione) La prima data in cui il sitelink può essere visualizzato. Il valore predefinito è il giorno corrente. Per specificare una data futura, immetterla nel formato MM/GG/AAAA o utilizzare il selettore data. La data di inizio è di sola lettura per i sitelink esistenti.

**[!UICONTROL End Date]:** (facoltativo) ultima data in cui è possibile visualizzare il sitelink. Per impostazione predefinita, il sitelink può essere visualizzato indefinitamente. Per specificare una data di fine, immetterla in formato MM/GG/AAAA o utilizzare il selettore data.

**[!UICONTROL Mobile Preference]:** (facoltativo) consente alla rete di provare a visualizzare l&#39;estensione agli utenti di dispositivi mobili anziché agli utenti di desktop o tablet. Per impostazione predefinita, questa opzione non è abilitata e l’estensione può essere visualizzata su qualsiasi tipo di dispositivo. La rete non garantisce che l’estensione verrà visualizzata sul tipo di dispositivo preferito.

### [!UICONTROL URL Options]

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

**[!UICONTROL Tracking Template]:** (Facoltativo) L&#39;URL di tracciamento, inclusi i reindirizzamenti del dominio di destinazione e i parametri di tracciamento, con l&#39;URL della pagina di destinazione finale incorporato in un parametro. Ad esempio, `https://www.trackingservice.example.com/?url={lpurl}&source={network}&id=5`.

In questa visualizzazione, i valori immessi per [!UICONTROL Base URL] e [!UICONTROL Tracking Template] devono iniziare con `http://` o `https://` e non possono contenere spazi.

* Quando le impostazioni della campagna includono **[!UICONTROL EF Redirect]** e **[!UICONTROL Auto Upload]**, Search, Social e Commerce prefissano automaticamente il proprio codice di reindirizzamento e di tracciamento quando si salva il record.

* Per i parametri che incorporano l&#39;URL finale, consulta la [documentazione di Microsoft Advertising](https://help.ads.microsoft.com/#apex/3/en/56799) o i parametri &quot;Solo modello di tracciamento&quot; nella [documentazione di Google Ads ValueTrack](https://support.google.com/google-ads/answer/6305348).

* È possibile includere parametri URL e parametri personalizzati a livello di campagna, separati da e commerciali (`&`), reindirizzamenti e tracciamento di terze parti.

* Il modello di tracciamento al livello più granulare sostituisce i modelli ai livelli più elevati.

>[!NOTE]
>
>* Per gli account con URL finali, l’URL di base può contenere reindirizzamenti all’interno del dominio o del sottodominio della pagina di destinazione, ma non all’esterno del dominio della pagina di destinazione. La rete di annunci estrae il dominio per creare l’URL di visualizzazione.
>* ([!DNL Google Ads]) Ogni sitelink in una campagna o in un gruppo di annunci deve avere una pagina di destinazione univoca con circa l&#39;80% di contenuto univoco. Non utilizzare i collegamenti a più ancoraggi sulla stessa pagina come pagine di destinazione di sitelink separate.
>* ([!DNL Google Ads]) Quando si aggiorna un modello di tracciamento a livello di sitelink o parola chiave, gli annunci pertinenti vengono inviati nuovamente per la revisione. L’aggiornamento a livello di account, campagna o gruppo di annunci non invia nuovamente gli annunci.
>* ([!DNL Microsoft Advertising]) È possibile aggiornare i modelli di tracciamento a qualsiasi livello senza inviare nuovamente gli annunci per l&#39;approvazione.
>* ([!DNL Google Ads]) Evitare le macro, che non vengono sostituite dai clic provenienti da origini che abilitano il tracciamento parallelo. Se sono necessarie macro, il team dell’account Adobe collabora con l’Assistenza clienti o con il team di implementazione per aggiungerle.

## Dati sulle prestazioni per i sitelink {#sitelink-performance}

Search, Social e Commerce mappano i clic su un’estensione dell’annuncio e le conversioni risultanti alla parola chiave associata all’annuncio in cui viene visualizzata l’estensione. I dati sui costi e sui clic a livello di estensione non sono disponibili in Search, Social e Commerce.

In [!UICONTROL Transaction Report], un valore [!UICONTROL Link Type] di `sl:<Sitelink text>`, ad esempio `sl:See Current Offers`, identifica una transazione da un sitelink anziché dall&#39;annuncio stesso. Vedi &quot;[Rapporto transazioni](/help/search-social-commerce/new-ui/reports/management/basic-advanced/transaction-report.md).&quot;

Puoi visualizzare i costi a livello di estensione e fare clic sui dati nell’interfaccia della rete di annunci.

>[!MORELIKETHIS]
>
>* [Gestione estensioni callout condivise di Google Ads](callout-extension-manage.md)
>* [Gestire le associazioni di estensione dell&#39;annuncio](ad-extension-association-manage.md)
