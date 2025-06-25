---
title: Modificare le metriche di conversione disponibili nelle visualizzazioni e nei rapporti di gestione
description: Scopri come rendere disponibili le metriche di conversione nelle visualizzazioni e nei rapporti di gestione.
feature: Conversions
exl-id: de3d288a-5fec-4479-92cf-7754390e21bb
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 0%

---

# Modificare le metriche di conversione disponibili nelle visualizzazioni e nei rapporti di gestione

Quando Adobe Advertising tiene traccia di una metrica di [conversione](/help/search-social-commerce/glossary.md#c-d) per un inserzionista, inizialmente viene esclusa dalle visualizzazioni degli obiettivi del portfolio, dei report e della gestione. Per rendere visibile una metrica di conversione, devi renderla esplicitamente disponibile e quindi, facoltativamente, modificare il nome visualizzato predefinito, che è il nome visualizzato. L&#39;unica eccezione è che le conversioni tracciate dai tag di tracciamento eventi universali [!DNL Google Ads], [!DNL Google Analytics] e [!DNL Microsoft Advertising] sono automaticamente disponibili e visibili.

Allo stesso modo, puoi nascondere una metrica di conversione dalle viste degli obiettivi del portfolio, dei rapporti e della gestione. Quando nascondi una metrica di conversione precedentemente visibile, questa viene rimossa da tutte le metriche derivate che la contengono.

Dall’elenco delle metriche di conversione disponibili, ogni utente con accesso ai dati dell’inserzionista può personalizzare le metriche visualizzate per le visualizzazioni di gestione e i rapporti, includendo o omettendo metriche specifiche a propria scelta.

1. Nel menu principale, fare clic su **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Conversions]**.

   Sono elencate tutte le metriche di conversione raccolte per l’inserzionista e tutti i nomi diversi specificati per la visualizzazione.

1. (Facoltativo) Filtra l’elenco:

   * Per cercare un nome di metrica o un nome visualizzato specifico, fare clic su ![Cerca](/help/search-social-commerce/assets/search.png "Cerca"), immettere la parola o la stringa nel campo di input, quindi premere il tasto **[!DNL Enter]**.

     È possibile cercare stringhe che appaiono in qualsiasi punto all&#39;interno della frase, ad esempio la prima lettera o le ultime tre lettere, e i termini di ricerca non sono [con distinzione tra maiuscole e minuscole](/help/search-social-commerce/glossary.md#c-d).

   * Per cercare le metriche di conversione in base alla disponibilità nelle visualizzazioni e nei report di gestione, fare clic su ![Filtro](/help/search-social-commerce/assets/filter.png "Filtro") e selezionare il filtro **[!UICONTROL Show in UI and Reports]**. Selezionare quindi **[!UICONTROL Show]** (per visualizzare le metriche di conversione disponibili da includere nei report e nelle visualizzazioni di gestione) o **[!UICONTROL Hide]** (per visualizzare le metriche di conversione non disponibili nei report e nelle visualizzazioni di gestione).

1. Modificare le metriche di conversione disponibili per le visualizzazioni e i rapporti di gestione:

   * Per mostrare o nascondere una singola metrica, fare clic sull&#39;opzione nella colonna **[!UICONTROL Show in UI and Reports]** per modificare l&#39;impostazione.

   * Per mostrare o nascondere più metriche, effettua le seguenti operazioni:

      1. Seleziona la casella di controllo accanto a ciascuna metrica di conversione.

         Per suggerimenti sulla selezione di più righe, vedere &quot;[Selezionare più righe](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

      1. Nella barra degli strumenti sopra la tabella dati, fai clic su ![Mostra](/help/search-social-commerce/assets/show.png "Mostra") per mostrare le metriche o su ![Nascondi](/help/search-social-commerce/assets/hide.png "Nascondi") per nasconderle.

      1. (Per nascondere le metriche) Nel messaggio di conferma, fare clic su **[!UICONTROL Yes]** per nascondere le metriche, inclusa la loro rimozione da qualsiasi metrica derivata che contiene le metriche.

1. (Facoltativo) [Modifica il nome visualizzato nelle intestazioni di colonna](conversion-metric-edit-display-name.md) per qualsiasi metrica di conversione.

   Il nome visualizzato predefinito per ogni metrica di conversione visibile è il nome della metrica come viene digitato nei dati recuperati.

>[!NOTE]
>
>Se Adobe Advertising raccoglie dati per nuove metriche di conversione, le nuove metriche, ad eccezione delle conversioni monitorate da [!DNL Google Ads], [!DNL Google Analytics] e [!DNL Microsoft Advertising] tag di tracciamento eventi universali, vengono automaticamente escluse dalle visualizzazioni di gestione e dai report fino a quando non vengono incluse. Le nuove conversioni tracciate dai tag di tracciamento degli eventi universali [!DNL Google Ads], [!DNL Google Analytics] e [!DNL Microsoft Advertising] sono sempre disponibili automaticamente.

>[!MORELIKETHIS]
>
>* [Informazioni sulla gestione delle metriche di conversione di un inserzionista](conversion-metric-about.md)
>* [Visualizza le metriche di conversione rilevate per un inserzionista](conversion-metric-view-tracked.md)
>* [Modificare il nome visualizzato per una metrica di conversione](conversion-metric-edit-display-name.md)
