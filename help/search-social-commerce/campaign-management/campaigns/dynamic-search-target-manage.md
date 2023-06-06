---
title: Gestisci [!DNL Google Ads] target di ricerca dinamica
description: Scopri come creare e gestire [!DNL Google Ads] destinazioni di ricerca dinamica.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 0%

---

# Gestisci [!DNL Google Ads] target di ricerca dinamica

*[!DNL Google Ads]solo account*

Puoi creare, modificare e cambiare lo stato dei target di ricerca dinamica per le campagne che utilizzano la rete di ricerca.

>[!NOTE]
>
>Puoi creare e modificare grandi quantità di dati di destinazione contemporaneamente caricando [file di bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) e pubblicarli sulla rete di annunci.

## Creare un [!DNL Google Ads] destinazione di ricerca dinamica

Puoi creare destinazioni di ricerca dinamica per definire le pagine dei siti web (ovvero i domini utilizzati negli URL di visualizzazione degli annunci) il cui contenuto viene utilizzato per indirizzare gli annunci di ricerca dinamica nello stesso gruppo di annunci.

Puoi eseguire il targeting per tutti i criteri o per un massimo di tre criteri singoli.

>[!NOTE]
>
>Per tenere traccia delle prestazioni nel modo migliore, crea un’&quot;[!UICONTROL All Targets]&quot; target per un solo gruppo di annunci per campagna.

>[!TIP]
>
>Per creare più componenti account contemporaneamente, utilizza [bulksheet delle campagne](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nei sottomenu, fare clic su **[!UICONTROL Live]>[!UICONTROL Auto Targets]**.

1. Nella barra degli strumenti sopra la tabella dati, fai clic su ![Crea](/help/search-social-commerce/assets/add.png "Crea").

1. Seleziona la rete di annunci, l’account, la campagna e il gruppo di annunci, quindi fai clic su **[!UICONTROL Continue]**.

1. Specifica la [impostazioni destinazione ricerca dinamica](#dynamic-search-target-settings).

1. Clic **[!UICONTROL Post]**.

## Modifica [!DNL Google Ads] impostazioni destinazione ricerca dinamica

Puoi modificare lo stato o l’offerta massima per un [!DNL Google Ads] destinazione di ricerca dinamica. Non puoi modificare i criteri di destinazione.

>[!TIP]
>
>Per modificare grandi quantità di dati contemporaneamente, utilizza [bulksheet delle campagne](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nei sottomenu, fare clic su **[!UICONTROL Live]>[!UICONTROL Auto Targets]**.

1. Selezionare la casella di controllo accanto a ogni riga da modificare.

   Per suggerimenti sulla selezione di più righe, vedere &quot;[Seleziona più righe](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

1. Nella barra degli strumenti sopra la tabella dati, fai clic su ![Modifica](/help/search-social-commerce/assets/edit.png "Modifica").

1. Specifica la [impostazioni destinazione ricerca dinamica](#dynamic-search-target-settings).

   Per più destinazioni, le modifiche vengono applicate a tutte le destinazioni selezionate. Per [!UICONTROL Bid field], sono disponibili opzioni per modificare i valori esistenti in un valore specificato o per aumentare o diminuire l&#39;importo di una percentuale specificata o di un importo monetario, con un limite.

1. Salvare i dati:

   * (Destinazioni singole) Fai clic su **[!UICONTROL Post]**.

   * (Più gruppi di annunci) Fai clic su **[!UICONTROL Post Now]**.

## Modificare lo stato di [!DNL Google Ads] target di ricerca dinamica

Puoi mettere in pausa qualsiasi target di ricerca dinamica attivo in un tipo di campagna supportato per interromperne l’utilizzo per gli annunci di ricerca dinamica nello stesso gruppo di annunci. In seguito puoi utilizzarli come destinazioni modificando lo stato dell’annuncio in Attivo.

Puoi anche eliminare qualsiasi destinazione dinamica.

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nei sottomenu, fare clic su **[!UICONTROL Live]>[!UICONTROL Auto Targets]**.

1. (Facoltativo) Filtra l’elenco per includere target dinamici specifici.

1. Effettuare una delle seguenti operazioni:

   * Per modificare lo stato di una destinazione dinamica, fare clic su nella **[!UICONTROL Status]** e modificare lo stato.

   * Per eliminare una o più destinazioni dinamiche, effettuare le seguenti operazioni:

      1. Selezionare la casella di controllo accanto a ogni destinazione dinamica che si desidera eliminare.
      Per suggerimenti sulla selezione di più righe, vedere &quot;[Seleziona più righe](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      1. Nella barra degli strumenti, fai clic su ![Altro](/help/search-social-commerce/assets/more.png "Altro") e seleziona **[!UICONTROL Delete]**.

      1. Nel messaggio di conferma, fai clic su **[!UICONTROL Delete]**.


## [!DNL Google Ads] impostazioni destinazione ricerca dinamica {#dynamic-search-target-settings}

### [!UICONTROL Auto-Target Details]

**[!UICONTROL Auto-targets]:** (Obbligatorio se non si specifica un dominio del sito web e una lingua nel [!UICONTROL DSA Options] sezione; sola lettura per destinazioni esistenti) Target di ricerca dinamica per il gruppo di annunci:

* *[!UICONTROL All Targets]* (impostazione predefinita): esegue il targeting di tutte le pagine indicizzate.

* *\[Destinazioni specifiche\]:* Definisce fino a tre criteri per le pagine indicizzate. Quando selezioni questa opzione, devi specificare i criteri specificando le categorie di informazioni e i valori specifici per i quali indirizzare gli annunci (ad esempio, &quot;URL contiene shoes.example.com&quot;). Per specificare più criteri, fare clic su **[!UICONTROL + And]**. I criteri di destinazione includono:

   * *[!UICONTROL Category]:* Per visualizzare gli annunci per le pagine indicizzate con un [!DNL Google Ads] categoria di contenuto.

   * *[!UICONTROL URL]:* Per mostrare annunci per pagine indicizzate con un URL specifico, dove il valore può essere incluso ovunque all’interno dell’URL.

   * *[!UICONTROL Page Title]:* Per visualizzare annunci per pagine indicizzate con testo specifico nel titolo della pagina.

   * *[!UICONTROL Page Content]:* Per mostrare annunci per pagine indicizzate con contenuto specifico.

**Stato:** Stato delle impostazioni di destinazione:

* *[!UICONTROL Active]* (impostazione predefinita): abilita l&#39;offerta.

* *[!UICONTROL Paused]:* Disabilita la licitazione.

* *[!UICONTROL Deleted]* (solo destinazioni esistenti): elimina le impostazioni di destinazione.

### [!UICONTROL Bids]

**[!UICONTROL Bid]:** Il costo massimo per clic (CPC) di un annuncio o il costo per 1000 impression (CPM) di un annuncio, come applicabile per la rete di annunci e il modello di prezzo della campagna. Questo valore sostituisce il valore a livello di gruppo di annunci.

>[!NOTE]
>
>Se il target si trova in un portafoglio ottimizzato, l’offerta CPC specificata viene applicata per un giorno. Successivamente, la funzionalità di ottimizzazione posiziona le offerte in base ai propri calcoli.

>[!MORELIKETHIS]
>
>* [Informazioni su [!DNL Google Ads] target di ricerca dinamica](dynamic-search-target-about.md)

