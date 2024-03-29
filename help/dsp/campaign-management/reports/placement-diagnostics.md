---
title: Visualizzare i rapporti di diagnostica del posizionamento
description: Scopri come diagnosticare i problemi relativi alla configurazione e alla velocità del posizionamento.
feature: DSP Placements
exl-id: 95e88c9c-09f2-44f1-9d6c-3fe533963f9a
source-git-commit: 1f8fd9d267aba0858b18c0b5a9b4a693e2b62468
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# Visualizzare i rapporti di diagnostica del posizionamento

<!-- Does this really belong in the Campaign Management > Reports section or in the Placements section? -->

I rapporti di diagnostica possono essere utili per diagnosticare i problemi relativi alla configurazione e al ritmo del posizionamento una volta che una campagna è attiva.

## Informazioni nei report di diagnostica del posizionamento

* **[!UICONTROL Change Log]:** Mostra le modifiche alle impostazioni di posizionamento chiave, come il nome, lo stato e l’offerta massima. Ogni voce include la data e il nome utente della persona che ha apportato la modifica.

* **[!UICONTROL Ad Approvals]:** Mostra se gli annunci sono stati approvati o rifiutati dai provider di inventario. Facoltativamente, puoi modificare lo stato di un annuncio (ad esempio, mettere in pausa un annuncio rifiutato) o aprire le impostazioni dell’annuncio.

* **[!UICONTROL Non Bids]:** Mostra il motivo per cui l&#39;DSP non ha fatto un&#39;offerta per il posizionamento.

## Aprire i report di diagnostica posizionamento

1. Aprire il rapporto Diagnostica:

   1. Apri le impostazioni di posizionamento:

      1. Nel menu principale, fai clic su **[!UICONTROL Campaigns]**.

      1. Fai clic sul nome della campagna, quindi fai clic su **[!UICONTROL Placements]**.

      1. Accanto al nome del posizionamento, fate clic su  **[!UICONTROL ...]** > **[!UICONTROL Edit]**.

   1. In alto a destra, fai clic su ![Diagnostica posizionamento](/help/dsp/assets/placement-diagnostics.png).

1. Effettua una delle seguenti operazioni:

   * Per visualizzare il registro delle modifiche:

      1. Clic **[!UICONTROL Change Log]**.

      1. (Facoltativo) Filtra i risultati del rapporto:

         * Nel menu data, modificare il periodo del rapporto dal valore predefinito Ultimi 14 giorni a un altro periodo (*[!UICONTROL Last 30 days],* *[!UICONTROL Last 60 days],* *[!UICONTROL Last 90 days],* o *[!UICONTROL Last 1 year]*).

         * Nel menu a sinistra, filtra il rapporto in base a un nome utente specifico.

         * Nel menu a destra, filtra il rapporto in base a un’impostazione di posizionamento specifica.

   * Per visualizzare lo stato delle approvazioni di annunci:

      1. In alto a destra, fai clic su **[!UICONTROL Ad Approvals]**.

      1. (Facoltativo) Per mettere in pausa o attivare l’annuncio, fai clic sull’interruttore di stato (![Interruttore di stato](/help/dsp/assets/status-switch.png)) nella colonna Annuncio).

      1. (Facoltativo) Per aprire le impostazioni di un annuncio, fai clic su **[!UICONTROL View Ad]** accanto all’annuncio.

   * Per capire perché l&#39;DSP non ha fatto un&#39;offerta per il posizionamento:

      1. In alto a destra, fai clic su **[!UICONTROL Non Bids]**.

      1. (Facoltativo) Per modificare l’intervallo di date, fai clic nel campo data e seleziona una data o un intervallo di date diverso.

<!-- Later, add link to >* Definitions for NBRs (Reading No Bid Reports (NBRs)) -->

>[!MORELIKETHIS]
>
>* [Tipi di rapporti sulle prestazioni nelle visualizzazioni di Campaign Management](campaign-reports-about.md)
>* [Visualizza il rapporto Previsione posizionamento](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [Impostazioni di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md)
