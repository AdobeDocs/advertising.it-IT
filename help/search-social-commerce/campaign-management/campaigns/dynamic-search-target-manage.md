---
title: Gestisci [!DNL Google Ads] destinazioni ricerca dinamica
description: Scopri come creare e gestire  [!DNL Google Ads] destinazioni di ricerca dinamiche.
exl-id: 5ea68cab-677f-4c7e-8776-24d6546f0b15
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 0%

---

# Gestisci [!DNL Google Ads] destinazioni di ricerca dinamica

Solo *[!DNL Google Ads]account*

Puoi creare, modificare e cambiare lo stato dei target di ricerca dinamica per le campagne che utilizzano la rete di ricerca.

>[!NOTE]
>
>Puoi creare e modificare grandi quantità di dati di destinazione contemporaneamente caricando [file bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) e pubblicandoli nella rete di annunci.

## Crea una destinazione di ricerca dinamica [!DNL Google Ads]

Puoi creare destinazioni di ricerca dinamica per definire le pagine dei siti web (ovvero i domini utilizzati negli URL di visualizzazione degli annunci) il cui contenuto viene utilizzato per indirizzare gli annunci di ricerca dinamica nello stesso gruppo di annunci.

Puoi eseguire il targeting per tutti i criteri o per un massimo di tre criteri singoli.

>[!NOTE]
>
>Per tenere traccia in modo ottimale delle prestazioni, crea una destinazione &quot;[!UICONTROL All Targets]&quot; per un solo gruppo di annunci per campagna.

>[!TIP]
>
>Per creare più componenti account contemporaneamente, utilizza [bulksheet campagna](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Nel menu principale, fare clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nei sottomenu, fare clic su **[!UICONTROL Live]>[!UICONTROL Auto Targets]**.

1. Nella barra degli strumenti sopra la tabella dati, fare clic su ![Crea](/help/search-social-commerce/assets/add.png "Crea").

1. Selezionare la rete di annunci, l&#39;account, la campagna e il gruppo di annunci, quindi fare clic su **[!UICONTROL Continue]**.

1. Specificare le [impostazioni della destinazione di ricerca dinamica](#dynamic-search-target-settings).

1. Fare clic su **[!UICONTROL Post]**.

## Modifica impostazioni destinazione di ricerca dinamica [!DNL Google Ads]

È possibile modificare lo stato o l&#39;offerta massima per una destinazione di ricerca dinamica [!DNL Google Ads]. Non puoi modificare i criteri di destinazione.

>[!TIP]
>
>Per modificare grandi quantità di dati contemporaneamente, utilizzare [bulksheet campagna](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Nel menu principale, fare clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nei sottomenu, fare clic su **[!UICONTROL Live]>[!UICONTROL Auto Targets]**.

1. Selezionare la casella di controllo accanto a ogni riga da modificare.

   Per suggerimenti sulla selezione di più righe, vedere &quot;[Selezionare più righe](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Nella barra degli strumenti sopra la tabella dati, fare clic su ![Modifica](/help/search-social-commerce/assets/edit.png "Modifica").

1. Specificare le [impostazioni della destinazione di ricerca dinamica](#dynamic-search-target-settings).

   Per più destinazioni, le modifiche vengono applicate a tutte le destinazioni selezionate. Per [!UICONTROL Bid field], sono disponibili opzioni per modificare i valori esistenti in un valore specificato o per aumentare o diminuire l&#39;importo di una percentuale o importo monetario specificato, con un limite.

1. Salvare i dati:

   * (Destinazioni singole) Fare clic su **[!UICONTROL Post]**.

   * (Più gruppi di annunci) Fare clic su **[!UICONTROL Post Now]**.

## Cambia lo stato di [!DNL Google Ads] destinazioni di ricerca dinamica

Puoi mettere in pausa qualsiasi target di ricerca dinamica attivo in un tipo di campagna supportato per interromperne l’utilizzo per gli annunci di ricerca dinamica nello stesso gruppo di annunci. In seguito puoi utilizzarli come destinazioni modificando lo stato dell’annuncio in Attivo.

Puoi anche eliminare qualsiasi destinazione dinamica.

1. Nel menu principale, fare clic su **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nei sottomenu, fare clic su **[!UICONTROL Live]>[!UICONTROL Auto Targets]**.

1. (Facoltativo) Filtra l’elenco per includere target dinamici specifici.

1. Effettuare una delle seguenti operazioni:

   * Per modificare lo stato di una destinazione dinamica, fare clic nella colonna **[!UICONTROL Status]** e modificare lo stato.

   * Per eliminare una o più destinazioni dinamiche, effettuare le seguenti operazioni:

      1. Selezionare la casella di controllo accanto a ogni destinazione dinamica che si desidera eliminare.

     Per suggerimenti sulla selezione di più righe, vedere &quot;[Selezionare più righe](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

      1. Nella barra degli strumenti, fare clic su ![Altro](/help/search-social-commerce/assets/more.png "Altro") e selezionare **[!UICONTROL Delete]**.

      1. Nel messaggio di conferma, fare clic su **[!UICONTROL Delete]**.

## [!DNL Google Ads] impostazioni destinazione di ricerca dinamica {#dynamic-search-target-settings}

### [!UICONTROL Auto-Target Details]

**[!UICONTROL Auto-targets]:** (obbligatorio quando non si specifica un dominio e una lingua del sito Web nella sezione [!UICONTROL DSA Options] della campagna; di sola lettura per le destinazioni esistenti) Destinazioni di ricerca dinamica per il gruppo di annunci:

* *[!UICONTROL All Targets]* (impostazione predefinita): esegue il targeting di tutte le pagine indicizzate.

* *\[Destinazioni specifiche\]:* Imposta fino a tre criteri per le pagine indicizzate. Quando selezioni questa opzione, devi specificare i criteri specificando le categorie di informazioni e i valori specifici per i quali indirizzare gli annunci (ad esempio, &quot;URL contiene shoes.example.com&quot;). Per specificare più criteri, fare clic su **[!UICONTROL + And]**. I criteri di destinazione includono:

   * *[!UICONTROL Category]:* Per visualizzare annunci per pagine indicizzate con una categoria di contenuto [!DNL Google Ads] specifica.

   * *[!UICONTROL URL]:* Per visualizzare annunci per pagine indicizzate con un URL specifico, in cui il valore può essere incluso in qualsiasi punto dell&#39;URL.

   * *[!UICONTROL Page Title]:* Per visualizzare annunci per pagine indicizzate con testo specifico nel titolo della pagina.

   * *[!UICONTROL Page Content]:* Per visualizzare annunci per pagine indicizzate con contenuto specifico.

**Stato:** Lo stato delle impostazioni di destinazione:

* *[!UICONTROL Active]* (impostazione predefinita): abilita l&#39;offerta.

* *[!UICONTROL Paused]:* Disabilita l&#39;offerta.

* *[!UICONTROL Deleted]* (solo destinazioni esistenti): elimina le impostazioni di destinazione.

### [!UICONTROL Bids]

**[!UICONTROL Bid]:** il costo massimo per clic (CPC) di un annuncio o il costo per 1000 impression (CPM) di un annuncio, come applicabile per la rete di annunci e il modello di prezzo della campagna. Questo valore sostituisce il valore a livello di gruppo di annunci.

>[!NOTE]
>
>Se il target si trova in un portafoglio ottimizzato, l’offerta CPC specificata viene applicata per un giorno. Successivamente, la funzionalità di ottimizzazione posiziona le offerte in base ai propri calcoli.

>[!MORELIKETHIS]
>
>* [Informazioni [!DNL Google Ads] destinazioni di ricerca dinamica](dynamic-search-target-about.md)
