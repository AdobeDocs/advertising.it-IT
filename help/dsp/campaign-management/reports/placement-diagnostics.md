---
title: Visualizzare i rapporti diagnostici di posizionamento
description: Scopri come diagnosticare i problemi con la configurazione del posizionamento e la velocità.
feature: DSP Placements
exl-id: 95e88c9c-09f2-44f1-9d6c-3fe533963f9a
source-git-commit: 1a98b3ba7c37a768825e9e48db7d847f12daa9a0
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---

# Visualizzare i rapporti diagnostici di posizionamento

<!-- Does this really belong in the Campaign Management > Reports section or in the Placements section? -->

I seguenti strumenti possono aiutarti a diagnosticare i problemi di configurazione del posizionamento e di gestione dei percorsi una volta che una campagna è attiva:

* **[!UICONTROL Change Log]:** Mostra le modifiche alle impostazioni di posizionamento chiave, ad esempio nome, stato e offerta massima. Ogni voce include la data e il nome utente della persona che ha apportato la modifica.
* **[!UICONTROL Ad Approvals]:** Indica se gli annunci sono stati approvati o rifiutati dai provider di inventario. Facoltativamente, puoi modificare lo stato di qualsiasi annuncio (ad esempio, mettere in pausa un annuncio rifiutato) o aprire le impostazioni dell’annuncio.
* **[!UICONTROL Non Bids]:** Mostra perché DSP non ha fatto offerte sul posizionamento.

1. Apri il rapporto Diagnostica :
   1. Apri le impostazioni di posizionamento:
      1. Nel menu principale, fai clic su **[!UICONTROL Campaigns]**.
      1. Fai clic sul nome della campagna, quindi fai clic su **[!UICONTROL Placements]**.
      1. Accanto al nome del posizionamento, fai clic su  **[!UICONTROL ...]** > **[!UICONTROL Edit]**.
   1. In alto a destra, fai clic su ![Diagnostica posizionamento](/help/dsp/assets/placement-diagnostics.png) o **[!UICONTROL Diagnostic]**.
1. Effettua una delle seguenti operazioni:
   * Per visualizzare il registro delle modifiche:
      1. Clic **[!UICONTROL Change Log]**.
      1. (Facoltativo) Filtrare i risultati del rapporto:
         * Nel menu della data , modifica il periodo del rapporto da Ultimi 14 giorni predefiniti a un altro periodo (*[!UICONTROL Last 30 days],* *[!UICONTROL Last 60 days],* *[!UICONTROL Last 90 days],* o *[!UICONTROL Last 1 year]*).
         * Nel menu a sinistra, filtra il rapporto per uno specifico nome utente.
         * Nel menu a destra, filtra il rapporto in base a un’impostazione di posizionamento specifica.
   * Per visualizzare lo stato delle approvazioni degli annunci:
      1. In alto a destra, fai clic su **[!UICONTROL Ad Approvals]**.
      1. (Facoltativo) Per mettere in pausa o attivare l&#39;annuncio, fai clic sull&#39;interruttore di stato (![Interruttore di stato](/help/dsp/assets/status-switch.png)) nella colonna Annuncio).
      1. (Facoltativo) Per aprire le impostazioni per un annuncio, fai clic su **[!UICONTROL View Ad]** accanto all’annuncio.
   * Per capire perché DSP non ha fatto offerte sul posizionamento:
      1. In alto a destra, fai clic su **[!UICONTROL Non Bids]**.
      1. (Facoltativo) Per modificare l’intervallo di date, fai clic nel campo data e seleziona una data o un intervallo di date diverso.

<!-- Later, add link to >* Definitions for NBRs (Reading No Bid Reports (NBRs)) -->

>[!MORELIKETHIS]
>
>* [Informazioni sui report in-Platform](campaign-reports-about.md)
>* [Impostazioni di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md)

