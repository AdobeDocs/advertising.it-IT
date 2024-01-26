---
title: Visualizza il rapporto Previsione posizionamento
description: Visualizza il numero di impression, la spesa e l’offerta massima ottimale previste per una particolare strategia di targeting per un posizionamento.
feature: DSP Placements
exl-id: 6ff228b2-b656-493e-a299-98c7a68a0f51
source-git-commit: 61ca25565e09bbce505d6f5cb0e5e8b7214eb1e0
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 0%

---

# Visualizza il rapporto Previsione posizionamento

<!-- Does this really belong in the Campaign Management > Reports section or in the Placements section? -->

Lo strumento di previsione del posizionamento mostra il numero previsto di impression, la spesa e l’offerta massima ottimale per una particolare strategia di targeting. La previsione viene calcolata in base al magazzino complessivo disponibile con il posizionamento e gli utenti univoci disponibili.

>[!NOTE]
>
>* Non viene generata alcuna previsione per i posizionamenti con targeting solo programmatico garantito (PG) perché la disponibilità e la spesa sono deterministiche.

## Informazioni nella previsione

La previsione include le seguenti informazioni:

* **[!UICONTROL Summary]:**

   * **[!UICONTROL Estimated CPM]:** Il costo stimato per mille impression (eCPM) che le impostazioni di targeting possono prevedere di raggiungere.

   * **[!UICONTROL Budget]:** Budget stimato per le impostazioni di targeting.

   * **[!UICONTROL Impression]:** Numero stimato di impression per le impostazioni di targeting.

* **[!UICONTROL Budget Yield Curve]:** Il numero stimato di impression che il posizionamento può fornire a diversi livelli di budget se tutte le altre impostazioni di targeting sono uguali.

* **[!UICONTROL Max Bid Yield Curve]:** La spesa stimata per il posizionamento a diversi livelli di offerta massima, quando tutte le altre impostazioni di targeting sono le stesse.

* **[!UICONTROL Message]:** Fornisce informazioni sull&#39;output previsto, inclusi gli scenari in cui non è stato possibile generare la previsione. Inoltre, evidenzia eventuali impostazioni di targeting riviste ma non considerate in tale scenario a causa di una mancanza di dati.

### Calcolo budget

* Per i posizionamenti non assegnati a un pacchetto, il budget di posizionamento viene utilizzato per i calcoli. All’interno di un volo viene calcolato lo stesso budget complessivo.

* Per i posizionamenti all’interno di un pacchetto, il budget assegnato al posizionamento viene utilizzato per i calcoli. Durante il volo viene calcolato il budget assegnato al posizionamento, che viene incluso nel messaggio.

* Per i posizionamenti aggiunti a un pacchetto in volo, il budget viene diviso in parti uguali in base al numero di posizionamenti. Quando il posizionamento diventa attivo, viene calcolato il budget assegnato dal pacchetto.

## Requisiti

* Spesa minima: $25 al giorno o equivalente in valuta locale per posizionamento.

* Spesa massima: $ 15.000 al giorno o l&#39;equivalente in valuta locale per posizionamento.

* Offerta massima minima, Offerta massima: è presente un’offerta massima minima (per la curva di rendimento del budget) e un’offerta massima (per la curva di rendimento dell’offerta massima) per tipo di posizionamento. Questi valori sono veri a livello globale e non tengono conto delle varianti regionali. A volte, questi valori possono essere troppo alti o bassi per l’area di destinazione.

* Dati storici: la previsione di posizionamento è disponibile quando sono disponibili dati storici sufficienti. Di seguito sono riportati alcuni esempi di casi in cui i dati storici potrebbero essere insufficienti:

   * Il posizionamento esegue il targeting di una nuova area geografica per la campagna.

   * Il posizionamento esegue il targeting di una nuova offerta di inventario per la campagna.

   * Il posizionamento utilizza un nuovo tipo di annuncio per la campagna.

     Un posizionamento è in genere una raccolta di più modelli di annunci definiti dalle piattaforme lato offerta. Pertanto, anche se il posizionamento esiste da molto tempo, il modello di annuncio sottostante può essere nuovo e lo strumento di previsione non sarà in grado di effettuare la previsione.

## Apri il rapporto Previsione posizionamento

1. Nel menu principale, fai clic su **[!UICONTROL Campaigns]**.

1. Fai clic sul nome della campagna, quindi fai clic su **[!UICONTROL Placements]**.

1. Accanto al nome del posizionamento, fate clic su  **[!UICONTROL ...]** > **[!UICONTROL Edit]**.

1. Individua il **[!UICONTROL Forecast]** in alto a destra. Se necessario, fai clic su ![Previsione](/help/dsp/assets/placement-forecast.png).

   >[!NOTE]
   >
   >* A volte la previsione potrebbe non essere disponibile a causa della cache del browser. In questo caso, cancella la cache e riprova.

>[!MORELIKETHIS]
>
>* [Informazioni sui rapporti sulle prestazioni nelle visualizzazioni di Campaign Management](campaign-reports-about.md)
>* [Visualizzare i rapporti di diagnostica del posizionamento](/help/dsp/campaign-management/reports/placement-diagnostics.md)
>* [Impostazioni di posizionamento](/help/dsp/campaign-management/placements/placement-settings.md)
