---
title: Visualizza il report di posizionamento [!UICONTROL Diagnostics]
description: Scopri come diagnosticare i problemi relativi alla configurazione e alla velocità del posizionamento.
feature: DSP Placements
exl-id: 95e88c9c-09f2-44f1-9d6c-3fe533963f9a
TQID: https://experienceleague.adobe.com/aRELxvUfrIZVu7-qzxO8QfrlMGNP17YJk0ru04oRFQQ
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: a4886037-b6d8-40e1-aeab-edeb7649d7d3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 306
ht-degree: 0%

---

# Visualizza il report di posizionamento [!UICONTROL Diagnostics]

<!-- Does this really belong in the Campaign Management > Reports section or in the Placements section? -->

I rapporti di diagnostica possono essere utili per diagnosticare i problemi relativi alla configurazione e al ritmo del posizionamento una volta che una campagna è attiva.

## Informazioni nel report di posizionamento [!UICONTROL Diagnostics]

* **[!UICONTROL Change Log]:** mostra le modifiche alle impostazioni di posizionamento chiave, ad esempio il nome, lo stato e l&#39;offerta massima. Ogni voce include la data e il nome utente della persona che ha apportato la modifica.

* **[!UICONTROL Ad Approvals]:** Indica se gli annunci sono stati approvati o rifiutati dai provider di inventario. Facoltativamente, puoi modificare lo stato di un annuncio (ad esempio, mettere in pausa un annuncio rifiutato) o aprire le impostazioni dell’annuncio.

* **[!UICONTROL Non Bids]:** mostra il motivo per cui DSP non ha fatto offerte per il posizionamento.

## Apri il report di posizionamento [!UICONTROL Diagnostics]

1. Apri il report [!UICONTROL Diagnostics]:

   1. Apri le impostazioni di posizionamento:

      1. Nel menu principale, fare clic su **[!UICONTROL Campaigns]**.

      1. Fare clic sul nome della campagna e quindi su **[!UICONTROL Placements]**.

      1. Accanto al nome del posizionamento, fare clic su **[!UICONTROL ...]** > **[!UICONTROL Edit]**.

   1. In alto a destra, fai clic su ![Diagnostica posizionamento](/help/dsp/assets/placement-diagnostics.png).

1. Effettua una delle seguenti operazioni:

   * Per visualizzare il registro delle modifiche:

      1. Fare clic su **[!UICONTROL Change Log]**.

      1. (Facoltativo) Filtra i risultati del rapporto:

         * Nel menu data modificare il periodo del report da Ultimi 14 giorni predefinito a un altro periodo (*[!UICONTROL Last 30 days],* *[!UICONTROL Last 60 days],* *[!UICONTROL Last 90 days],* o *[!UICONTROL Last 1 year]*).

         * Nel menu a sinistra, filtra il rapporto in base a un nome utente specifico.

         * Nel menu a destra, filtra il rapporto in base a un’impostazione di posizionamento specifica.

   * Per visualizzare lo stato delle approvazioni di annunci:

      1. In alto a destra, fare clic su **[!UICONTROL Ad Approvals]**.

      1. (Facoltativo) Per mettere in pausa o attivare l&#39;annuncio, fare clic sull&#39;opzione di stato (![Opzione di stato](/help/dsp/assets/status-switch.png)) nella colonna Annuncio.

      1. (Facoltativo) Per aprire le impostazioni di un annuncio, fare clic su **[!UICONTROL View Ad]** accanto all&#39;annuncio.

   * Per capire perché DSP non ha fatto un&#39;offerta per il posizionamento:

      1. In alto a destra, fare clic su **[!UICONTROL Non Bids]**.

      1. (Facoltativo) Per filtrare il posizionamento in base a un target di offerta privato specifico, seleziona l’offerta. <!-- Admin users only: Optionally filter the deal by one or more regions ([!UICONTROL US-EAST], [!UICONTROL US-WEST]) [!UICONTROL EU-WEST], [!UICONTROL HKG]) by selecting the regions. -->

      1. (Facoltativo) Per modificare l’intervallo di date, fai clic nel campo data e seleziona una data o un intervallo di date diverso.

<!-- Later, add link to >* Definitions for NBRs (Reading No Bid Reports (NBRs)) -->

>[!MORELIKETHIS]
>
>* [Tipi di report sulle prestazioni nelle visualizzazioni di gestione delle campagne](campaign-reports-about.md)
>* [Visualizza il report di previsione del posizionamento](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [Impostazioni posizionamento](/help/dsp/campaign-management/placements/placement-settings.md)
