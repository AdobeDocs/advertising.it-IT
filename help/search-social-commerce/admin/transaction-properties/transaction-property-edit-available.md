---
title: Modificare le proprietà della transazione disponibili nelle visualizzazioni e nei report di gestione
description: Scopri come rendere le proprietà delle transazioni disponibili nelle visualizzazioni e nei rapporti di gestione.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 0%

---

# Modificare le proprietà della transazione disponibili nelle visualizzazioni e nei report di gestione

Quando Adobe Advertising traccia un [proprietà transazione](/help/search-social-commerce/glossary.md#s-t) per un inserzionista, inizialmente è escluso dalle viste obiettivi portfolio, report e gestione. Per rendere visibile una proprietà, è necessario renderla disponibile in modo esplicito e quindi modificare facoltativamente il nome visualizzato predefinito, ovvero il nome visualizzato. L&#39;unica eccezione è che le conversioni tracciate da [!DNL Google Ads], [!DNL Google Analytics], e [!DNL Microsoft® Advertising] i tag di tracciamento degli eventi universali sono automaticamente disponibili e visibili.

Allo stesso modo, puoi nascondere una proprietà dalle viste obiettivi portfolio, report e gestione. Quando nascondi una proprietà precedentemente visibile, questa viene rimossa da tutte le metriche derivate che la contengono.

Dall&#39;elenco delle proprietà disponibili, ogni utente con accesso ai dati dell&#39;inserzionista può personalizzare le proprietà visualizzate per le visualizzazioni e i report di gestione, incluse o omettendo proprietà specifiche a propria scelta.

1. Nel menu principale, fai clic su **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Transaction Properties]**.

   Vengono elencate tutte le proprietà di transazione raccolte per l&#39;inserzionista e tutti i nomi diversi specificati per la visualizzazione.

1. (Facoltativo) Filtra l’elenco:

   * Per cercare un nome di proprietà o un nome visualizzato specifico, fare clic su ![Ricerca](/help/search-social-commerce/assets/search.png "Ricerca"), immettere la parola o la stringa nel campo di immissione, quindi premere **[!DNL Enter]** chiave.

      È possibile cercare le stringhe che appaiono in qualsiasi punto della frase, ad esempio la prima lettera o le ultime tre lettere, e i termini di ricerca non sono [distinzione tra maiuscole e minuscole](/help/search-social-commerce/glossary.md#c-d).

   * Per cercare le proprietà in base alla loro disponibilità nelle visualizzazioni e nei rapporti di gestione, fai clic su ![Filtro](/help/search-social-commerce/assets/filter.png "Filtro"), e seleziona il filtro **[!UICONTROL Show in UI and Reports]**. Quindi seleziona **[!UICONTROL Show]** (per visualizzare le proprietà disponibili da includere nei report e nelle visualizzazioni di gestione) o **[!UICONTROL Hide]** (per visualizzare le proprietà non disponibili nelle visualizzazioni report e gestione).

1. Modificare le proprietà disponibili per le visualizzazioni e i report di gestione:

   * Per mostrare o nascondere una singola proprietà, fare clic sull&#39;opzione nella **[!UICONTROL Show in UI and Reports]** per modificare l&#39;impostazione.

   * Per mostrare o nascondere più proprietà, effettuare le seguenti operazioni:

      1. Selezionare la casella di controllo accanto a ciascuna proprietà.

         Per suggerimenti sulla selezione di più righe, vedere &quot;[Seleziona più righe](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      1. Nella barra degli strumenti sopra la tabella dati, fai clic su ![Spettacolo](/help/search-social-commerce/assets/show.png "Spettacolo") per visualizzare le proprietà o ![Nascondi](/help/search-social-commerce/assets/hide.png "Nascondi") per nascondere le proprietà.

      1. Per nascondere le proprietà, nel messaggio di conferma fai clic su **[!UICONTROL Yes]** per nascondere le proprietà, inclusa la loro rimozione da eventuali metriche derivate che contengono le proprietà.

1. (Facoltativo) [Modificare il nome visualizzato nelle intestazioni di colonna](transaction-property-edit-display-name.md) per una qualsiasi delle proprietà.

   Il nome visualizzato predefinito per ogni proprietà visibile è il nome della proprietà così come è scritto nei dati recuperati.

>[!NOTE]
>
>Se Adobe Advertising raccoglie dati per le nuove proprietà, le nuove proprietà, ad eccezione delle conversioni tracciate da [!DNL Google Ads], [!DNL Google Analytics], e [!DNL Microsoft® Advertising] tag di tracciamento degli eventi universali: vengono automaticamente esclusi dalle visualizzazioni e dai rapporti di gestione fino a quando non vengono inclusi. Nuove conversioni tracciate da [!DNL Google Ads], [!DNL Google Analytics], e [!DNL Microsoft® Advertising] i tag di tracciamento degli eventi universali sono sempre disponibili automaticamente.

>[!MORELIKETHIS]
* [Informazioni sulla gestione delle proprietà di transazione di un inserzionista](transaction-property-about.md)
* [Visualizzare le proprietà della transazione tracciate per un inserzionista](transaction-property-view-tracked.md)
* [Modificare il nome visualizzato per una proprietà di transazione](transaction-property-edit-display-name.md)

