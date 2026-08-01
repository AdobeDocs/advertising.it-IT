---
title: Gestione annunci
description: Scopri come creare e gestire gli annunci, inclusi i tipi di annunci disponibili.
feature: Search Campaign Management
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 730b474b83ae4df47c18f93adfec62b1dc9b8a16
workflow-type: tm+mt
source-wordcount: 1732
ht-degree: 0%

---

# Gestione annunci

*funzionalità Beta*

Solo *[!DNL Google Ads], [!DNL LY Ads], [!DNL Microsoft Advertising], [!DNL Yandex] e [!DNL Baidu] account esistenti*

Un annuncio appartiene a un gruppo di annunci e contiene il contenuto visualizzato dagli utenti, ad esempio titolo, descrizione, immagine o altri elementi creativi, a seconda della rete e del tipo di annuncio.

Dopo aver [reso accessibile un account di rete tramite una connessione API](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md) e dopo che Search, Social e Commerce hanno sincronizzato i dati dell&#39;account con la rete di annunci, puoi creare annunci per un tipo di campagna [supportato](/help/search-social-commerce/introduction/supported-inventory.md). Puoi anche modificare e cambiare lo stato degli annunci.

Per informazioni dettagliate sulle funzionalità disponibili per ogni rete di annunci, vedi &quot;[Inventario supportato](/help/search-social-commerce/introduction/supported-inventory.md).&quot;

## Informazioni sulla visualizzazione [!UICONTROL Ads] {#ad-view-about}

La visualizzazione [!UICONTROL Manage] > [!UICONTROL Ads] elenca tutti gli annunci nella visualizzazione filtrata per l&#39;account dell&#39;inserzionista selezionato.

### Azioni disponibili

* [Creare un annuncio](#ad-create)

* [Rinominare un annuncio dalla riga](#ad-rename)

* [Modificare le impostazioni degli annunci](#ad-edit)

* [Modificare o eliminare lo stato di un annuncio](#ad-status)

* [Gestisci i report di visualizzazione dati dalla visualizzazione [!UICONTROL Ads]](#ad-reports)

## Tipi di annunci disponibili {#ad-types}

Puoi creare e gestire i tipi di annunci supportati per i gruppi di annunci all’interno di un account di rete di annunci sincronizzato:

* **Annunci di testo o annunci di testo espansi** per un gruppo di annunci in una campagna che esegue il targeting della rete di ricerca. Gli annunci di testo possono includere parametri di tracciamento facoltativi che sostituiscono i parametri a livello di gruppo di annunci o di campagna. A seconda della rete di annunci, puoi creare annunci di testo espansi/estesi o annunci di testo standard.

* **annunci di pubblico** nativi tra dispositivi per [!DNL Microsoft Advertising] campagne in [!DNL Microsoft Audience Network]. Sono disponibili due opzioni per gli annunci di pubblico, in base alle impostazioni della campagna:

  * Se la campagna è collegata a un negozio di centri commerciali, lascia che la rete di annunci generi automaticamente annunci basati su feed per la campagna, utilizzando le informazioni sul prodotto del negozio. Non è necessario creare annunci basati su feed per la campagna, ma è necessario creare gruppi di annunci con targeting utente.

  * Se la campagna non è collegata a un account del centro commerciale, crea annunci di pubblico basati su immagini utilizzando il formato di annuncio reattivo, che include più risorse di testo e immagini. La rete di annunci assembla gli annunci utilizzando le combinazioni più efficaci di elementi pubblicitari e li visualizza su siti come [!DNL MSN], [!DNL Outlook.com] e [!DNL Microsoft Edge].

* **Annunci di sola chiamata** per [!DNL Google Ads] campagne nella rete di ricerca. Gli annunci di sola chiamata sono annunci di testo che includono un numero di telefono. Facoltativamente, puoi utilizzare un numero di inoltro assegnato a [!DNL Google Ads] per il reporting avanzato delle chiamate.

  >[!NOTE]
  >
  >Al momento non è possibile creare o modificare annunci di sola chiamata. Puoi visualizzare, modificare lo stato o eliminare un annuncio di sola chiamata esistente.

* **Annunci di ricerca dinamica espansi** (ora denominati solo &quot;annunci di ricerca dinamica&quot; sulle reti di annunci) per [!DNL Google Ads] e [!DNL Microsoft Advertising] gruppi di annunci di ricerca dinamica nelle campagne di ricerca. Gli annunci per ricerca dinamica utilizzano il contenuto del sito web, invece delle parole chiave, per decidere quando visualizzare gli annunci. La rete di annunci genera dinamicamente il titolo, sceglie l’URL della pagina di destinazione e l’URL di visualizzazione e genera automaticamente l’URL finale.

  Per ulteriori informazioni sugli annunci per ricerca dinamica, consulta la [[!DNL Google Ads] documentazione](https://support.google.com/google-ads/answer/2471185) e la [[!DNL Microsoft Advertising] documentazione](https://help.ads.microsoft.com/#apex/ads/en/56794).

* **Annunci multimediali** per [!DNL Microsoft Advertising] campagne di ricerca. Gli annunci multimediali sono annunci di grandi dimensioni di immagini che vengono visualizzati in posizioni prominenti della linea principale e della barra laterale e viene visualizzato un solo annuncio multimediale per pagina. Possono includere più risorse di testo e immagini, come annunci reattivi, e la rete di annunci assembla gli annunci utilizzando le combinazioni più efficaci di elementi pubblicitari. Gli annunci multimediali non sostituiscono i posizionamenti degli annunci di testo.

* Righe promozione per **[!DNL Microsoft Advertising]annunci di prodotti (acquisti)** sulla rete di acquisti. Gli annunci commerciali utilizzano i prodotti nel tuo feed di prodotto [!DNL Microsoft Merchant Center] esistente, invece delle parole chiave, per decidere come e dove visualizzare gli annunci. Gli URL della copia e della pagina di destinazione dell’annuncio vengono generati automaticamente dalle informazioni sul prodotto nel feed, ma puoi facoltativamente impostare linee di promozione da includere per il gruppo di annunci.

  Per ulteriori informazioni sugli annunci dei prodotti, consulta la [documentazione di Microsoft Advertising](https://help.ads.microsoft.com/#apex/3/en/51082).

* **Annunci di ricerca reattivi** per [!DNL Google Ads] e [!DNL Microsoft Advertising] campagne nella rete di ricerca. La rete di annunci assembla dinamicamente annunci di ricerca responsive basati su testo da un set di titoli e descrizioni di annunci, favorendo combinazioni con prestazioni ottimali. L’annuncio include fino a tre titoli, due descrizioni e un URL personalizzabile dall’URL di base e dai campi opzionali percorso1 e percorso2. Facoltativamente, puoi fissare i titoli e le descrizioni degli annunci a posizioni specifiche.

  >[!NOTE]
  >
  >[!DNL Google Ads] non fornisce dati al di fuori dei propri editor nativi sulle combinazioni di testo visualizzate come annunci. Per ulteriori informazioni sul reporting per ogni combinazione di testo, consulta la [documentazione di Google Ads](https://support.google.com/google-ads/answer/7684791).

### Dati sulle prestazioni a livello di annuncio

I dati a livello di annuncio sono disponibili per la maggior parte dei tipi di annuncio.

Tuttavia, non è disponibile per [!DNL Google Ads] campagne Dynamic Search Ad (DSA), Prestazioni massime, Smart Shopping e [!DNL YouTube]. Sono previste discrepanze tra il totale dei dati a livello di annuncio per una campagna e il totale dei dati per la campagna.

| Rete di annunci/Campagna/Tipo di annuncio | Disponibilità dei dati |
|---|---|
| [!DNL Google Ads] annuncio di ricerca dinamica (DSA) | Campagna, gruppo di annunci |
| [!DNL Google Ads] prestazioni max | Campagna |
| [!DNL Google Ads] acquisti, acquisti avanzati | Campagna, gruppo di annunci |
| [!DNL Google Ads] [!DNL YouTube] | Campagna, gruppo di annunci |

## Creare un annuncio {#ad-create}

<!-- Verify that this note is still applicable -->

>[!NOTE]
>
>* Non è necessario creare annunci di prodotti per le campagne di acquisto; la rete di annunci li crea automaticamente. Per le campagne di acquisto [!DNL Microsoft Advertising], tuttavia, è possibile definire facoltativamente le linee di promozione da includere negli annunci.
>* Impossibile creare [!DNL Google Ads] annunci di sola chiamata.

>[!TIP]
>
>Per creare un numero elevato di annunci contemporaneamente, utilizza [bulksheet campagna](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Ads]**.

1. Fare clic su **[!UICONTROL Create Ads]**.

1. Nel passaggio **[!UICONTROL Basic Settings]**, seleziona la rete, l&#39;account, la campagna, il gruppo di annunci e il tipo di annuncio.

   Per ulteriori informazioni sui tipi di annunci disponibili, vedere &quot;[Tipi di annunci disponibili](#ad-types).&quot;

1. Specifica le impostazioni rimanenti per un [annuncio di testo Baidu](ad-settings-baidu-text.md), [annuncio di ricerca dinamica espanso di Google Ads](ad-settings-google-dsa.md) (denominato solo &quot;annuncio di ricerca dinamica&quot; in Google Ads), [annuncio di ricerca responsive di Google Ads](ad-settings-google-rsa.md), [annuncio di ricerca dinamica espanso di Microsoft Advertising](ad-settings-microsoft-dsa.md), [annuncio multimediale di Microsoft Advertising](ad-settings-microsoft-multimedia.md), [annuncio di prodotto Microsoft Advertising](ad-settings-microsoft-product.md), [annuncio di ricerca responsive di Microsoft (audience)](ad-settings-microsoft-responsive.md), [annuncio di ricerca responsive di Advertising](ad-settings-microsoft-rsa.md) o [Yandex impostazioni dell&#39;annuncio di testo](ad-settings-yandex-text.md).

   >[!NOTE]
   >
   >(Campagne con tracciamento delle conversioni di Adobe Advertising) Se le impostazioni dell’account o della campagna specificano il tracciamento solo a livello di parola chiave, Search, Social e Commerce non generano il tracciamento per gli annunci.

1. Fare clic su **[!UICONTROL Review and Save]**.

1. Se necessario, fai clic su ![Modifica](/help/search-social-commerce/assets/edit-new.png "Modifica") **[!UICONTROL Edit]** e modifica le impostazioni dell&#39;annuncio.

1. Fare clic su **[!UICONTROL Create]**.

1. <!-- Add link to where to generate this once available to users-->(Acquisti nelle campagne con tracciamento delle conversioni di Adobe Advertising; facoltativo) Per tenere traccia dei clic sull’annuncio, aggiungi manualmente un URL di tracciamento alle impostazioni dell’account, della campagna o del gruppo di prodotti.

## Rinominare un annuncio {#ad-rename}

Rinominare rapidamente un annuncio senza aprire le impostazioni complete dell’annuncio.

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Ads]**.

1. Posizionare il cursore sulla riga dell&#39;annuncio e fare clic su **[!UICONTROL ...]>[!UICONTROL Rename]**.

1. Modificare il nome e quindi fare clic su **[!UICONTROL Apply]**.

## Modificare le impostazioni degli annunci {#ad-edit}

>[!NOTE]
>
>* I seguenti tipi di annunci sono *mutable*, il che significa che è possibile modificare la copia o l&#39;immagine dell&#39;annuncio e mantenere lo stesso ID annuncio: tutti i tipi di annunci [!DNL Google Ads] ad eccezione degli annunci di ricerca dinamica e [!DNL Microsoft Advertising] annunci di testo espansi.
>* Tutti gli altri annunci supportati sono *non modificabili*, il che significa che la modifica della copia o dell&#39;immagine dell&#39;annuncio elimina l&#39;annuncio esistente e ne crea uno nuovo. Le prestazioni del nuovo annuncio possono essere volatili per un paio di settimane, mentre Search, Social e Commerce raccolgono dati sufficienti per l’ottimizzazione.
>* Impossibile modificare il contenuto di un annuncio di prodotto, ad eccezione della riga di promozione per [!DNL Microsoft Advertising] annunci di prodotto. Tuttavia, puoi sospendere o eliminare un annuncio.
>* Impossibile modificare [!DNL Google Ads] annunci di sola chiamata. Tuttavia, puoi metterne in pausa o eliminarne una.
>* Puoi modificare un solo annuncio alla volta.

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Ads]**.

1. Seleziona la casella di controllo accanto all’annuncio.

1. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL Edit]**.

1. Nel passaggio **[!UICONTROL Ad Details]**, modifica [Annuncio di testo Baidu](ad-settings-baidu-text.md), [Annuncio di ricerca dinamica espanso di Google Ads](ad-settings-google-dsa.md) (ora denominato solo &quot;annuncio di ricerca dinamica&quot; in Google Ads), [Annuncio di ricerca responsive di Google Ads](ad-settings-google-rsa.md), [Annuncio di ricerca dinamica espanso di Microsoft Advertising](ad-settings-microsoft-dsa.md), [Annuncio multimediale Microsoft Advertising](ad-settings-microsoft-multimedia.md), [Annuncio di prodotto Microsoft Advertising](ad-settings-microsoft-product.md), [Annuncio di ricerca responsive di Microsoft (pubblico)](ad-settings-microsoft-responsive.md), [Annuncio di ricerca responsive di Advertising](ad-settings-microsoft-rsa.md), oppure [Impostazioni annuncio testo Yandex](ad-settings-yandex-text.md).

1. Fare clic su **[!UICONTROL Review and Save]**.

1. Se necessario, fai clic su ![Modifica](/help/search-social-commerce/assets/edit-new.png "Modifica") **[!UICONTROL Edit]** e modifica le impostazioni dell&#39;annuncio.

1. Fare clic su **[!UICONTROL Update]**.

## Modificare lo stato di un annuncio {#ad-status}

Cambia rapidamente lo stato di un annuncio senza aprire le impostazioni complete dell’annuncio.

Puoi mettere in pausa qualsiasi annuncio attivo su una rete di annunci supportata per disabilitare le offerte su di esso. In seguito puoi riprendere l’offerta riportando lo stato attivo.

Puoi anche eliminare qualsiasi annuncio attivo o in pausa. Gli annunci eliminati vengono eliminati dalla rete di annunci. Sono ancora visibili quando li includi nel filtro dati, ma non puoi modificarli.

### Attivare o mettere in pausa un annuncio

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Ads]**.

1. Seleziona la casella di controllo per la riga dell’annuncio.

1. Nella barra degli strumenti delle azioni in blocco, modifica lo stato:

   * Per attivare un annuncio in pausa, fare clic su **[!UICONTROL Activate]**.

   * Per sospendere un annuncio attivo, fare clic su **[!UICONTROL Pause]**.

### Eliminare un annuncio

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Ads]**.

1. Seleziona la casella di controllo per la riga dell’annuncio.

1. Nella barra degli strumenti Azioni in blocco fare clic su **[!UICONTROL Delete]**.

1. Nel messaggio di conferma, fare clic su **[!UICONTROL Confirm]**.

## Gestisci i report di visualizzazione dati dalla visualizzazione [!UICONTROL Ads] {#ad-reports}

Generare un report che includa le righe di dati per uno o più annunci nella visualizzazione [!UICONTROL Ads], quindi scaricare il report come file del foglio di lavoro di Microsoft Excel (formato XLXS). Il report include tutte le colonne visibili nella visualizzazione.

Puoi eliminare qualsiasi rapporto generato.

Vedere anche &quot;[(Interfaccia precedente) Scaricare dati da una visualizzazione di gestione campagne](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md)&quot; e &quot;[(Interfaccia precedente) Eliminare un report di dati sulle prestazioni o un file di bulksheet dal menu [!UICONTROL Downloads]](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md).&quot;

### Generare un rapporto con le righe di dati filtrate

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Ads]**.

1. Specifica gli annunci di cui desideri scaricare i dati:

   * Per scaricare i dati per annunci specifici, seleziona le caselle di controllo accanto agli annunci.

   * Per scaricare i dati per tutti gli annunci, non è necessario selezionare alcuna casella di controllo. Tutti gli annunci sono inclusi per impostazione predefinita.

1. Nella barra degli strumenti sopra la tabella dati, fare clic su ![Scarica report](/help/search-social-commerce/assets/download.png "Scarica report") **[!UICONTROL Reports]**.

1. Nelle impostazioni di [!UICONTROL Grid Reports], immettere un nome di report univoco, quindi fare clic su **[!UICONTROL Generate]**.

   Per impostazione predefinita, il file è denominato &quot;ad_AAAAMMGG_NNNN&quot;, dove &quot;NNNN&quot; è il numero del processo sequenziale (ad esempio &quot;ad_20250402_1326).

   Il file viene aggiunto all&#39;elenco [!UICONTROL Recently Generated].

1. (Facoltativo) Per scaricare il file una volta completato, fai clic su ![Scarica](/help/search-social-commerce/assets/download.png "Scarica") accanto al nome del file.

   Il file viene scaricato in base alla normale procedura del browser.

### Scaricare un rapporto completato

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Ads]**.

1. Nella barra degli strumenti sopra la tabella dati, fare clic su ![Scarica report](/help/search-social-commerce/assets/download.png "Scarica report") **[!UICONTROL Reports]**.

1. Nell&#39;elenco [!UICONTROL Recently Generated] della finestra di dialogo [!UICONTROL Grid Reports], fare clic su ![Scarica](/help/search-social-commerce/assets/download.png "Scarica") accanto al nome del file.

   Il file viene scaricato in base alla normale procedura del browser.

### Eliminare un rapporto completato

1. Nel menu principale, fare clic su **[!UICONTROL Manage]>[!UICONTROL Ads]**.

1. Nella barra degli strumenti sopra la tabella dati, fare clic su ![Scarica report](/help/search-social-commerce/assets/download.png "Scarica report") **[!UICONTROL Reports]**.

1. Nell&#39;elenco [!UICONTROL Recently Generated] della finestra di dialogo [!UICONTROL Grid Reports], fare clic su ![Elimina](/help/search-social-commerce/assets/delete-new.png "Elimina") accanto al nome del file.

>[!MORELIKETHIS]
>
>* [[!DNL Baidu] impostazioni annuncio testo](ad-settings-baidu-text.md)
>* [[!DNL Google Ads] impostazioni annuncio ricerca dinamica espansa](ad-settings-google-dsa.md)
>* [[!DNL Google Ads] impostazioni degli annunci di ricerca responsive](ad-settings-google-rsa.md)
>* [[!DNL Microsoft Advertising] impostazioni annuncio ricerca dinamica espansa](ad-settings-microsoft-dsa.md)
>* [[!DNL Microsoft Advertising] impostazioni annunci multimediali](ad-settings-microsoft-multimedia.md)
>* [[!DNL Microsoft Advertising] impostazioni annuncio prodotto](ad-settings-microsoft-product.md)
>* [[!DNL Microsoft Advertising] impostazioni annuncio reattivo (pubblico)](ad-settings-microsoft-responsive.md)
>* [[!DNL Microsoft Advertising] impostazioni degli annunci di ricerca responsive](ad-settings-microsoft-rsa.md)
>* [[!DNL Yandex] impostazioni annuncio testo](ad-settings-yandex-text.md)
